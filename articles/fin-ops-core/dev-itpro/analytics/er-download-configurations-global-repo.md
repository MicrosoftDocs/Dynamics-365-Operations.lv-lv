---
title: Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija
description: Šajā rakstā skaidrots, kā lejupielādēt elektronisko pārskatu (ER) konfigurācijas no Konfigurācijas pakalpojuma globālā repozitorija.
author: kfend
ms.date: 06/02/2020
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
ms.openlocfilehash: 3bbc341d1668e54fcb4034263a7e142166a94b05
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273314"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā lejupielādēt [elektronisko pārskatu (ER) konfigurācijas](general-electronic-reporting.md#Configuration) no konfigurācijas pakalpojuma globālā repozitorija. Papildinformāciju skatiet [Microsoft Dynamics 365 Finanšu – regulēšanas pakalpojumi, konfigurācijas pakalpojums](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Atvērt konfigurācijas repozitoriju

1. Pieteikties Dynamics 365 finanšu programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.
3. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
3. Elementā **Microsoft** atlasiet **Repozitoriji**.

    ![Elektronisko pārskatu darbvieta.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar veidu **Globāls**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:

    1. Atlasiet **Pievienot**, lai pievienotu jaunu repozitoriju.
    2. Atlasiet **Globāls** kā repozitorija veidu un pēc tam atlasiet **Izveidot repozitoriju**.
    3. Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.
    4. Ievadiet repozitorija nosaukumu un aprakstu un pēc tam atlasiet **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    5. Režģī atlasiet jauno repozitoriju ar veidu **Globāls**.

5. Atlasiet **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.

    ![Repozitoriju lapas konfigurēšana.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Vienas atsevišķas konfigurācijas importēšana

1. Lapā **Konfigurācijas repozirotiji** konfigurāciju kokā atlasiet vēlamo ER konfigurāciju.
2. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
3. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.

    > [!NOTE]
    > Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā Finance instancē.

    ![Konfigurācijas repozitorija lapa, konfigurācijas kopsavilkuma cilne.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Filtrēto konfigurāciju importēšana

1. Lapā **Konfigurāciju repozitoriji** konfigurāciju kokā izvērsiet kopsavilkuma cilni **Filtrēt**.
2. Režģī **Tagi** pievienojiet visus nepieciešamos tagus.
3. Laukā **Valsts/reģiona piemērojamība** atlasiet attiecīgos valstu/reģionu kodus un pēc tam atlasiet  **Lietot filtru**.

    > [!NOTE]
    > Kopsavilkuma cilnes **Konfigurācijas** rāda visas konfigurācijas, kas atbilst norādītajiem atlases nosacījumiem.

4. Kopsavilkuma cilnē **Konfigurācijas** atlasiet **Importēt**, lai lejupielādētu filtrētās konfigurācijas no Globālā repozitorija uz pašreizējo instanci.
5. Kopsavilkuma cilnē **Konfigurācijas** atlasiet **Atiestatīt filtru**, lai notīrītu norādītos atlases nosacījumus.

    ![Konfigurācijas repozitorija lapa, kopsavilkuma cilne Versijas, importēšanas poga.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Papildinformāciju skatiet šī raksta saistīto resursu sarakstā.

> [!NOTE]
> ER konfigurācijas var konfigurēt kā atkarīgas no citām konfigurācijām. Tāpēc kopā ar izvēlēto konfigurāciju var automātiski importēt citas konfigurācijas. Plašāku informāciju par konfigurācijas atkarībām skatiet [Noteikt atkarību no ER konfigurācijām citos komponentos](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

