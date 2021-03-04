---
title: Atjaunināto ER konfigurāciju versiju importēšana
description: Šajā tēmā ir paskaidrots, kā importēt atjauninātās elektronisko pārskatu (ER) konfigurāciju versijas no konfigurācijas pakalpojuma globālā repozitorija.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679514"
---
# <a name="import-updated-versions-of-er-configurations"></a>Atjaunināto ER konfigurāciju versiju importēšana

[!include [banner](../includes/banner.md)]

Elektroniskā pārskata (ER) [repozitoriji](general-electronic-reporting.md#Repository) tiek izmantoti, lai koplietotu [ER konfigurācijas](general-electronic-reporting.md#Configuration). Varat [importēt](download-electronic-reporting-configuration-lcs.md) ER konfigurācijas no dažādiem repozitorijiem savā Microsoft Dynamics 365 Finance instancē. Importējot ER konfigurācijas, [konfigurācijas nodrošinātāji](general-electronic-reporting.md#Provider) var publicēt jaunas [versijas](general-electronic-reporting.md#component-versioning) repozitorijus, lai tos varētu koplietot.

Šajā tēmā ir paskaidrots, kā importēt atjauninātās ER konfigurāciju versijas no konfigurācijas pakalpojuma globālā repozitorija. Plašāku informāciju skatiet [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurācijas pakalpojums](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Pieejamo atjaunināto versiju pārskatīšana

1. Pierakstieties programmatūrā Finance, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Importēt konfigurāciju versiju atjauninājumus**.

    ![Lokalizācijas konfigurāciju lapa](./media/er-download-updated-versions-global-repo1.png)

4. Dialoglodziņa **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** laukā **Izpildes režīms** atlasiet **Tikai pieejamos atjauninājumus**. Tad atl. **Labi**. 

    ![Izpildes režīma lauks iestatīts uz Tikai pieejamos atjauninājumus](./media/er-download-updated-versions-global-repo2.png)

5. Pārskatiet saņemtos ziņojumus. Šie ziņojumi sniedz tālāk norādīto informāciju par ER konfigurācijām pašreizējā Finance instancē un to, kā tās salīdzināt ar globālā repozitorija saturu:

    - Kopējais ER konfigurāciju skaits
    - ER konfigurācijas, kas neatrodas globālajā repozitorijā
    - ER konfigurācijas, kurām jaunākā versija jau ir pieejama pašreizējā Finance instancē (skatiet visu ER konfigurāciju sarakstu, atlasot saiti **Ziņojuma informācija**.)

        ![“Šo konfigurāciju jaunākās versijas jau ir importētas” ziņojums un ziņojuma informācija](./media/er-download-updated-versions-global-repo3.png)

    - ER konfigurācijas, kurām jaunākā versija jau ir pieejama globālajā repozitorijā un var tikt importēta pašreizējā Finance instancē (skatiet visu ER konfigurāciju sarakstu, atlasot saiti **Ziņojuma informācija**.)

        ![“Pieejamie atjauninājumi” ziņojums un ziņojuma informācija](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Pieejamo atjaunināto versiju importēšana

1. Pierakstieties programmatūrā Finance, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Importēt konfigurāciju versiju atjauninājumus**.
4. Dialoglodziņa **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** laukā **Izpildes režīms** atlasiet **Importēt jaunākos atjauninājumus**, lai importētu ER konfigurācijas jaunākās versijas no globālā repozitorija pašreizējā Finance instancē.
5. Lai ieplānotu pakešuzdevumu importēšanai, kopsavilkuma cilnē **Palaist fonā** iestatiet opciju **Pakešapstrāde** uz **Jā**. Importēšanu var atkārtot periodiski, konfigurējot nepieciešamo periodiskumu.

    ![Izpildes režīma lauks iestatīts uz Importēt jaunākos atjauninājumus](./media/er-download-updated-versions-global-repo5.png)

6. Atlasiet **Labi**.
7. Lai uzzinātu, kādas konfigurāciju versijas ir importētas, veiciet vienu no šīm darbībām:

    - Ja importēšana tiek veikta interaktīvi, neizmantojot pakešuzdevumu, pārskatiet saņemtos ziņojumus.

        ![Interaktīvās importēšanas laikā saņemtie ziņojumi](./media/er-download-updated-versions-global-repo6.png)

    - Ja importēšana tiek veikta pakešveida režīmā, rīkojieties šādi:

        1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
        2. Meklējiet un atlasiet **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** darbu un pēc tam darbību rūts cilnē **Pakešuzdevums** atlasiet **Pakešuzdevumu vēsture**, lai skatītu darba vēsturi.
        3. Lapā **Pakešuzdevumu vēsture** atlasiet **Žurnāls**. Tad, saņemtajā ziņojumā atlasiet **Ziņojuma informācija**, lai skatītu darbu žurnālu.

        ![Darbu žurnāls](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Nav ieteicams ieplānot periodisku pakešuzdevumu, lai importētu atjauninātās ER konfigurāciju versijas tieši no globālā repozitorija ražošanas vidē, jo importētās versijas nekavējoties būs pieejamas lietošanai. Tā vietā izmantojiet iespēju ER konfigurāciju versijas izvietot smilškastes vidē. Pēc tam tos var novērtēt smilškastes vidē, pirms tie tiek izvietoti ražošanas vidē.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]