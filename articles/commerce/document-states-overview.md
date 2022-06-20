---
title: Dokumenta stāvokļi un dzīves cikls
description: Šajā rakstā ir ietverti dažādi lapu elementu dokumentu veidi Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 04836ecf80fc86ab6abb96e4255779c8c03988d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909462"
---
# <a name="document-states-and-lifecycle"></a>Dokumenta stāvokļi un dzīves cikls

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti dažādi lapu elementu dokumentu veidi Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Dokumenta stāvokļa apraksti

Raksta [Lapas elementos](page-elements-overview.md) ir uzskaitīti dažādi dokumentu tipi satura pārvaldības sistēmā (CMS). Šiem dokumentu veidiem autorēšanas rīkā var būt vairāki stāvokļi. Dokumenta stāvokļi palīdz novērst datu konfliktus un ieviest versiju kontroli. Tās nosaka, kurš var mainīt dokumentus, kad to var darīt, un kad citas personas var skatīt izmaiņas.

Tālāk redzamā tabula parāda Commerce iespējamos lapas elementu dokumenta stāvokļus.

| Dokumenta stāvoklis      | Vietnes veidotāja darbība        | apraksts                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Izrakstīts         | Atlasiet **Rediģēt**.           | Piemērotais dokuments tiek paņemts jums. Kamēr dokuments ir šajā stāvoklī, to nevar mainīt citi autentificēti sistēmas lietotāji, un visas dokumentā veiktās izmaiņas ir redzamas tikai jums. |
| Saglabāts               | Atlasiet **Saglabāt**.           | Paņemtā dokumentā veiktās izmaiņas tiek saglabātas datu bāzē, bet dokuments vēl nav atdots vai publicēts. Saglabātās izmaiņas nav redzamas citiem autentificētiem sistēmas lietotājiem, kamēr autors atlasa **Beigt rediģēšanu**. Tie nav redzami ārējiem lietotājiem, kamēr elements nav publicēts. |
| Atmestā izrakstīšana | Atlasiet **Atmest labojumus**.  | Visas izmaiņas paņemtajā dokumentā tiek atmestas, un krājums tiek atgriezts pēdējā versijā, kas tika pārbaudīta. |
| Reģistrējies          | Atlasiet **Beigt rediģēšanu**. | Rediģētais dokuments ir atdots. Visas izmaiņas ir redzamas citiem autentificētiem sistēmas lietotājiem, un šie lietotāji pēc tam var rediģēt dokumentu. Katra reģistrācija izveido dokumenta versijas ierakstu elementa vēsturē. |
| Publicēts           | Atlasiet **Publicēt**.        | Dokuments tiek publicēts, un izmaiņas tiek atstumtas uz jūsu Live vietni un kļūst atklājamas ārējiem lietotājiem. Krājumus var publicēt tikai tad, ja tie vispirms ir pārbaudīti, atlasot **Beigt rediģēšanu**. |

## <a name="additional-resources"></a>Papildu resursi

[Satura pievienošanas veidi](add-manage-content.md)

[Lapas modeļa glosārijs](page-elements-overview.md)

[Darbs ar publicēšanas grupām](publish-groups.md)

[Šķērskanālu kopīgošanas iespējošana un izmantošana](cross-channel-sharing.md)

[Darbs ar moduļiem](work-with-modules.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Vietnes navigācijas pielāgošana](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]