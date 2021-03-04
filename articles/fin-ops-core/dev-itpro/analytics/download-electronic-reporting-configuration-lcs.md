---
title: Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services
description: Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 719b277fb828ea2085ea80bc4a36c2af3412f66b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683309"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronisko pārskatu veidošanas konfigurācijas lejupielāde no Lifecycle Services

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā lejupielādēt jaunāko [Elektroniskās ziņošanas (Electronic reporting - ER) konfigurācijas](general-electronic-reporting.md#Configuration) versiju no [Koplietojamo līdzekļu bibliotēka](../lifecycle-services/asset-library.md) programmā Microsoft Dynamics Lifecycle Services (LCS).

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu veidošana**.
3. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
4. Elementā **Microsoft** atlasiet **Repozitoriji**.

    [![Microsoft elements lokalizācijas konfigurāciju lapā](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:

    1. Atlasiet **Pievienot**, lai pievienotu repozitoriju.
    2. Atlasiet **LCS** kā repozitorija tipu.
    3. Atlasiet **Izveidot repozitoriju**.
    4. Ja tiek parādīta uzvedne par autorizāciju, izpildiet ekrānā redzamos norādījumus.
    5. Ievadiet repozitorija nosaukumu un aprakstu.
    6. Atlasiet **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    7. Režģī atlasiet jauno repozitoriju ar tipu **LCS**.

6. Atlasiet **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.

    [![Repozitoriju lapas konfigurēšana](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Ja rodas problēmas, piekļūstot LCS repozitorijam, lai lejupielādētu konfigurāciju no koplietojamo līdzekļu bibliotēkas LCS, varat tai vietā lejupielādēt konfigurācijas no [Globālā krātuve](er-download-configurations-global-repo.md) .

7. Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.
8. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
9. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo instanci.

    > [!NOTE]
    > Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā instancē.

    [![Konfigurācijas repozitorijas lapa.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Plašāku informāciju skatiet ar šo tēmu saistīto tēmu sarakstā.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]