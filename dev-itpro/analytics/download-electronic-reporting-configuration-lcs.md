---
title: "Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services"
description: "Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e2f3a352ca70472de838271fdedfede575cb839d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no Microsoft Dynamics Lifecycle Services (LCS).

Šī apmācība palīdzēs jums veikt elektronisko atskaišu veidošanas (ER) konfigurāciju jaunāko versiju lejupielādi no Microsoft Dynamics Lifecycle Services (LCS).

1.  Pierakstieties programmā Dynamics 365 for Operations, izmantojot vienu no šīm lomām:
    -   Elektroniskā pārskata izstrādātājs
    -   Elektronisko pārskatu veidošanas funkcionālais konsultants
    -   Sistēmas administrators

2.  Dodieties uz **Organizācijas administrēšana** &gt; **Elektronisko pārskatu veidošana**.
3.  Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
4.  Elementā **Microsoft** noklikšķiniet uz **Repozitoriji**. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:
    1.  Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu repozitoriju.
    2.  Atlasiet **LCS** kā repozitorija tipu.
    3.  Noklikšķiniet uz **Izveidot repozitoriju**.
    4. Ja tiek pieprasīts, izpildiet autorizācijas norādījumus.
    5.  Ievadiet repozitorija nosaukumu un aprakstu.
    6.  Noklikšķiniet uz **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    7.  Režģī atlasiet jauno repozitoriju ar tipu **LCS**.

6.  Noklikšķiniet uz **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.
8.  Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
9.  Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo Dynamics 365 for Operations instanci. **Piezīme.** Poga **Importēt** nav pieejama ER konfigurācijas versijām, kuras jau ir pašreizējā Dynamics 365 for Operations instancē. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Piezīme.** Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Plašāku informāciju skatiet ar šo tēmu saistīto rakstu sarakstā.

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)




