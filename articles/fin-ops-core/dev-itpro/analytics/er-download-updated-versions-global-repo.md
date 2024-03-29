---
title: Atjaunināto ER konfigurāciju versiju importēšana
description: Šajā rakstā skaidrots, kā importēt atjauninātās elektronisko pārskatu (ER) konfigurāciju versijas no Konfigurācijas pakalpojuma global repozitorija.
author: kfend
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 0eef9c9a112fd58a43f6c3a85163ccf44bea3d61
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292652"
---
# <a name="import-updated-versions-of-er-configurations"></a>Atjaunināto ER konfigurāciju versiju importēšana

[!include [banner](../includes/banner.md)]

Elektroniskā pārskata (ER) [repozitoriji](general-electronic-reporting.md#Repository) tiek izmantoti, lai koplietotu [ER konfigurācijas](general-electronic-reporting.md#Configuration). Varat importēt [ER](download-electronic-reporting-configuration-lcs.md) konfigurācijas no dažādiem repozitoriju darījumiem savā Microsoft Dynamics 365 Finanšu instancē. Importējot ER konfigurācijas, [konfigurācijas nodrošinātāji var](general-electronic-reporting.md#Provider) publicēt jaunas versiju atkārtotas lietojumprogrammas, lai tos varētu koplietot.

Šajā rakstā skaidrots, kā importēt atjauninātās ER konfigurāciju versijas no Konfigurācijas pakalpojuma globālā repozitorija. Papildinformāciju skatiet [Microsoft Dynamics 365 Finanšu – regulēšanas pakalpojumi, konfigurācijas pakalpojums](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Pieejamo atjaunināto versiju pārskatīšana

1. Pierakstieties programmatūrā Finance, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Importēt konfigurāciju versiju atjauninājumus**.

    ![Lokalizācijas konfigurāciju lapa.](./media/er-download-updated-versions-global-repo1.png)

4. Dialoglodziņa **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** laukā **Izpildes režīms** atlasiet **Tikai pieejamos atjauninājumus**. Pēc tam atlasiet **Labi**. 

    ![Izpildes režīma lauks iestatīts uz Tikai pieejamos atjauninājumus.](./media/er-download-updated-versions-global-repo2.png)

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

    ![Izpildes režīma lauks iestatīts uz Importēt jaunākos atjauninājumus.](./media/er-download-updated-versions-global-repo5.png)

6. Atlasiet **Labi**.
7. Lai uzzinātu, kādas konfigurāciju versijas ir importētas, veiciet vienu no šīm darbībām:

    - Ja importēšana tiek veikta interaktīvi, neizmantojot pakešuzdevumu, pārskatiet saņemtos ziņojumus.

        ![Interaktīvās importēšanas laikā saņemtie ziņojumi.](./media/er-download-updated-versions-global-repo6.png)

    - Ja importēšana tiek veikta pakešveida režīmā, rīkojieties šādi:

        1. Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.
        2. Meklējiet un atlasiet **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** darbu un pēc tam darbību rūts cilnē **Pakešuzdevums** atlasiet **Pakešuzdevumu vēsture**, lai skatītu darba vēsturi.
        3. Lapā **Pakešuzdevumu vēsture** atlasiet **Žurnāls**. Tad, saņemtajā ziņojumā atlasiet **Ziņojuma informācija**, lai skatītu darbu žurnālu.

        ![Darbu žurnāls.](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Nav ieteicams ieplānot periodisku pakešuzdevumu, lai importētu atjauninātās ER konfigurāciju versijas tieši no globālā repozitorija ražošanas vidē, jo importētās versijas nekavējoties būs pieejamas lietošanai. Tā vietā izmantojiet iespēju ER konfigurāciju versijas izvietot smilškastes vidē. Pēc tam tos var novērtēt smilškastes vidē, pirms tie tiek izvietoti ražošanas vidē.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
