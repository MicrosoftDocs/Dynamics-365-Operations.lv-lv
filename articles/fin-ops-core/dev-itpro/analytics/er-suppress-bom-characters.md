---
title: Izveidot ER konfigurācijas, lai likvidētu MK rakstzīmes ģenerētos failos
description: Šajā tēmā skaidrots, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus, kas likvidētu baita pasūtījuma zīmes (MK) rakstzīmes.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060823"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Izveidot ER konfigurācijas, lai likvidētu MK rakstzīmes ģenerētos failos

[!include [banner](../includes/banner.md)]

Varat noformēt [elektronisko pārskatu (Electronic Reporting — ER)](general-electronic-reporting.md) [risinājumu](er-quick-start1-new-solution.md), lai ģenerētu izejošos dokumentus. Lai izveidotu dokumentus kā teksta vai XML failus, risinājumā jāietver ER [konfigurācija](general-electronic-reporting.md#Configuration), kas satur ER [formāta](general-electronic-reporting.md#FormatComponentOutbound)komponentu. Lai norādītu [rakstzīmju kodēšanas veidu](https://docs.microsoft.com/windows/win32/intl/character-sets), kas apzīmē rakstzīmju kopu ģenerētos failos, ER formātam jāsatur **Kopējā\\Faila** formāta elements. Lai konfigurētu ER formāta komponentu, jāatver izveidotās ER konfigurācijas [melnraksta](general-electronic-reporting.md#component-versioning) versija ER formāta noformētājā un jāpievieno **Kopējais\\Faila** elements. Laukā **Kodēšana** norādiet izpildlaikā ģenerēto izejošo failu kodēšanas veidu, izmantojot šo komponentu.

> [!NOTE]
> Ja formāts ietver nepareizu kodēšanas nosaukumu, saglabājot izmaiņas formāta iestatījumos, tiek parādīts kļūdas ziņojums.

![Saknes elementu pievienošana Formātu noformētāja lapā](./media/er-suppress-bom-characters-image1.gif)

Ja kā kodēšanas veidu norādāt **UTF-8**, **UTF-16** vai **UTF-32**, kļūst pieejama opcija **Likvidēt MK rakstzīmes**. Iestatiet šo opciju kā **Jā**, lai likvidētu [baitu pasūtījuma atzīmes (MK) rakstzīmes](https://docs.microsoft.com/globalization/encoding/byte-order-mark) izejošos failos, kas tiek ģenerēti izpildlaikā,kad tiek palaists rediģējams ER formāts.

> [!NOTE]
> Ja atstājat tukšu lauku **Kodēšana**, tad tiek izmantota **UTF-8** noklusējuma vērtība.

![Opcijas Likvidēt MK rakstzīmes iestatīšana lapā Formāta veidotājs](./media/er-suppress-bom-characters-image2.gif)

Lai pārskatītu izpildlaika funkcionalitāti, izpildiet attiecīgo procedūru. Piemēram, izpildiet darbības tēmā [XML elementu XML elementu izpildes atliktā izpilde ER formātos](er-defer-xml-element.md). Kad esat izpildījis soļus sadaļā [Modificēt formātu, lai aprēķins būtu balstīts uz šīs tēmas ģenerēto izvades](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output)sadaļu, izpildiet šīs papildu darbības.

1. Norādiet UTF kodējumu:

    1. Atlasiet **Pārskata** elementu **Kopējā\\Faila** tipā.
    2. **Kodēšanas** laukā norādiet **UTF-8** kodēšanas informāciju.

2. Ģenerēt XML failu, kas satur MK rakstzīmi:

    1. Iestatiet opciju **Likvidēt MK rakstzīmes** uz **Nē**, lai ģenerētajos XML failos iekļautu MK rakstzīmes.
    2. Izpildiet soļi kopsavilkuma [XML elementa Izpildes atliktajā maksājuma sadaļā, lai izmantotu aprēķināto kopsummu](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tēmas sadaļā [XML elementu izpildes atliktais izpilde ER formātos](er-defer-xml-element.md), un saglabājiet ģenerēto failu kā **SampleXmlReport.xml**.

3. Ģenerēt XML failu, kas nesatur MK rakstzīmi:

    1. Iestatiet opciju **Likvidēt MK rakstzīmes** uz **Jā**, lai likvidētu MK rakstzīmes ģenerētajos XML failos.
    2. Izpildiet soļi kopsavilkuma [XML elementa Izpildes atliktajā maksājuma sadaļā, lai izmantotu aprēķināto kopsummu](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tēmas sadaļā [XML elementu izpildes atliktais izpilde ER formātos](er-defer-xml-element.md), un saglabājiet ģenerēto failu kā **SampleXmlReport (1).xml**.

4. Salīdziniet ģenerētos failus failu salīdzinājuma utilītā.

    Pirmā atšķirība, ko pamanīsit, ir faila galvenē. Failā SampleXmlReport.xml ir MK rakstzīme, kurā nav SampleXmlReport (1).xml faila.

    ![Salīdziniet ģenerētos failus failu salīdzinājuma utilītā](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Skatiet arī

- [XML elementu izpildes atlikšana elektronisko pārskatu formātos](er-defer-xml-element.md)
