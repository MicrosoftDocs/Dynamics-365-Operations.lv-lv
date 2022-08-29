---
title: Elektronisko pārskatu veidošanas konfigurācijas lejupielāde no Lifecycle Services
description: Šajā rakstā ir izskaidrots, kā lejupielādēt elektronisko pārskatu (ER) konfigurācijas no Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277822"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronisko pārskatu veidošanas konfigurācijas lejupielāde no Lifecycle Services

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots [, kā lejupielādēt jaunāko elektronisko pārskatu (ER) konfigurāciju versiju no koplietojamās līdzekļu bibliotēkas pakalpojumos](general-electronic-reporting.md#Configuration)[...](../lifecycle-services/asset-library.md)Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> LCS kā ER konfigurāciju glabāšanas repozitorija izmantošana ir [novecojusi](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Papildinformāciju skatiet [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu veidošana**.
3. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
4. Elementā **Microsoft** atlasiet **Repozitoriji**.

    [![Microsoft elements lokalizācijas konfigurāciju lapā.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:

    1. Atlasiet **Pievienot**, lai pievienotu repozitoriju.
    2. Atlasiet **LCS** kā repozitorija tipu.
    3. Atlasiet **Izveidot repozitoriju**.
    4. Ja tiek parādīta uzvedne par autorizāciju, izpildiet ekrānā redzamos norādījumus.
    5. Ievadiet repozitorija nosaukumu un aprakstu.
    6. Atlasiet **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    7. Režģī atlasiet jauno repozitoriju ar tipu **LCS**.

6. Atlasiet **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.

    [![Repozitoriju lapas konfigurēšana.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Ja rodas problēmas, piekļūstot LCS repozitorijam, lai lejupielādētu konfigurāciju no koplietojamo līdzekļu bibliotēkas LCS, varat tai vietā lejupielādēt konfigurācijas no [Globālā krātuve](er-download-configurations-global-repo.md) .

7. Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.
8. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
9. Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo instanci.

    > [!NOTE]
    > Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā instancē.

    [![Konfigurācijas repozitorijas lapa.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Papildinformāciju skatiet šī raksta saistīto tēmu sarakstā.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
