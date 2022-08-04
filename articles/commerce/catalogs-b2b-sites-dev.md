---
title: Commerce katalogu paplašināmības ietekme B2B pielāgojumiem
description: Šajā rakstā ir aprakstīta Commerce katalogu paplašināmības ietekme uz sadaļā B2B funkciju Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 06d304226270c9c63c6907190dc1038a38f70e44
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136805"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Commerce katalogu paplašināmības ietekme B2B pielāgojumiem

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīta Commerce katalogu paplašināmības **ietekme uz sadaļā B2B** funkciju Microsoft Dynamics 365 Commerce.

Ja interesējaties par kataloga konteksta paplašināšanas līdz pielāgotiem scenārijiem, pielāgojumi, iespējams, būs jāatjaunina. Šis atjauninājums seko standarta procesam, kam seko debitori, jo to pielāgošana var automātiski neatbalstīs jaunākos līdzekļus pēc jaunināšanas. Ja pielāgošanā tiek iekļauts kāds jauns līdzeklis vai kļūdas labojumi to pieredzi, pielāgošanas kodu ieteicams atbilstoši atjaunināt. Šis atjauninājums ir līdzīgs izmaiņām, ko Microsoft, iespējams, ir veikusi attiecībā uz pamatkodu.

Pārskatiet pielāgošanas gadījumus, kas seko, lai noteiktu, vai pielāgojumi jāatjaunina.

> [!NOTE]
> - Visiem preču programmas programmēšanas interfeisiem (API) ir jābūt izprotamiem katalogā. Tādēļ ir ļoti svarīgi pieņemt CatalogID **parametru**.
> - Noklusējuma katalogs (**CatalogID**=**0**) nav derīgs katalogs parakstītiem "bizness-biznesam" (B2B) lietotājiem. Tādēļ visi API izsaukumi, kas pieņem "0" vai lieto noklusējuma vērtību, neizdosies, jo vietas lietotājiem nav piekļuves katalogam 0. Lai saņemtu pareizo pieredzi, debitora API izsaukumi ir jāatjaunina tā, lai tie izdotu kataloga ID, kas tika atlasīts kataloga uztvērējā. Ja izmantojat noklusējuma vērtību un lietotājs pārslēdz katalogus, vietnei ir jānodrošina dati atlasītajam katalogam. Tāpēc, lai atbilstu API, kas tiek darbināti no commerce pamatkoda, pielāgotiem API ir jāpalaiž atlasītais katalogs.

Šādiem pielāgošanas gadījumiem nepieciešami izstrādes atjauninājumi:

- **1. gadījums.** Debitors iepazīstina ar savu datu [darbību,](e-commerce-extensibility/data-actions.md) kas izsauc ar preci saistītu API vai datu darbību. Ir jāveic šādas atjaunināšanas darbības:

    1. Ja datu darbība izmanto tiešo API zvanu, atjauniniet datu darbību tā, lai tā pārietu uz kataloga ID, kā parādīts šajā piemēra attēlā.

        ![Atjauninātā datu darbība, kas atbilst kataloga ID.](./media/customization1_a.png)

    1. Ja datu darbība pielāgošanas iekšienē izsauc citu ar preci saistītu datu darbību, kods ir jāatjaunina tā, lai tas atbilst dažiem jauniem parametriem, piemēram **, requestContext**. Parametrs **requestContext** tiek izmantots, lai izgūtu pašreizējā kataloga ID, kā parādīts šajā piemēra attēlā.

        ![Atjauninātā datu darbība, kas atbilst jaunajam parametram.](./media/customization1_b.png)

- **2. gadījums:** debitoram ir [ignorēta datu darbība](e-commerce-extensibility/data-action-overrides.md). Ir jāveic šāda atjaunināšanas darbība:

    - Atjaunināt datu darbību 1. gadījumam.

- **3. gadījums.** Debitoram ir skata paplašinājums, skripta papildu modulis vai modulī [,](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) kas ietver API izsaukumus vai datu darbības. Ir jāveic šāda atjaunināšanas darbība:

    - Atjauniniet kodu 1. gadījumam, kā parādīts šajā piemēra ilustrācijā.

       ![Atjauninātais kods, kas atbilst jaunajam parametram.](./media/customization3.png)

- **4. gadījums:** debitors izmanto **getById** API izsaukumu. Ir jāveic šāda atjaunināšanas darbība:

    - Pārejiet uz **getByIds API izsaukumu**, **jo getById** PIECEL izsaukumam ir daži ierobežojumi un tā neatbalsta kataloga apzināšanu.

- **5. gadījums:** debitoram ir datu darbība, kas izgūst informāciju par vairākām precēm, kas, iespējams, ir no dažādiem katalogiem. Ir jāveic šāda atjaunināšanas darbība:

    - Sadalīt API izsaukumus pēc kataloga ID. Piemēram, groza API grozā var būt preces no dažādiem katalogiem. Preču rindas ir jāgrupē pēc kataloga ID, un tām ir atsevišķi jāizsauc API katram katalogam, kā parādīts šajā piemēra attēlā.

        ![Atjaunināta datu darbība, kas grupē preču rindas pēc kataloga ID.](./media/customization5.png)

## <a name="additional-resources"></a>Papildu resursi

[Commerce katalogu izveide B2B vietnēm](catalogs-b2b-sites.md)

[Bieži uzdotie jautājumi par Commerce katalogiem B2B vietnēm](catalogs-b2b-sites-FAQ.md)

[Kataloga izdošanas modulis](catalog-picker.md)
