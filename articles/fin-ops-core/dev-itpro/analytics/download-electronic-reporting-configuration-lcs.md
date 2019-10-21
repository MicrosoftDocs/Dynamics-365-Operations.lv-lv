---
title: Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services
description: Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174125"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no portāla Microsoft Dynamics Lifecycle Services (LCS).

Šajā apmācībā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (ER) konfigurāciju jaunāko versiju no portāla Microsoft Dynamics Lifecycle Services (LCS).

1. Pierakstieties programmā, izmantojot vienu no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

2. Dodieties uz **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana**.
3. Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
4. Elementā **Microsoft** noklikšķiniet uz **Repozitoriji**.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:

    1. Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu repozitoriju.
    2. Atlasiet **LCS** kā repozitorija tipu.
    3. Noklikšķiniet uz **Izveidot repozitoriju**.
    4. Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.
    5. Ievadiet repozitorija nosaukumu un aprakstu.
    6. Noklikšķiniet uz **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    7. Režģī atlasiet jauno repozitoriju ar tipu **LCS**.

6. Noklikšķiniet uz **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.
8. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
9. Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo instanci.

    > [!NOTE]
    > Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā instancē.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Plašāku informāciju skatiet ar šo tēmu saistīto rakstu sarakstā.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
