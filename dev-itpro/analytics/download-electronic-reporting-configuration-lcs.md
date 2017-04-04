---
title: "Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services"
description: "Šajā tēmā ir paskaidrots, kā lejupielādēt elektroniskā pārskata (ER) sastāvi no Microsoft Dynamics Lifecycle Services (LCS)."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services

Šajā tēmā ir paskaidrots, kā lejupielādēt elektroniskā pārskata (ER) sastāvi no Microsoft Dynamics Lifecycle Services (LCS).

Šī apmācība palīdzēs jums veikt elektronisko atskaišu veidošanas (ER) konfigurāciju jaunāko versiju lejupielādi no Microsoft Dynamics Lifecycle Services (LCS).

1.  Pierakstieties programmā Dynamics 365 for Operations, izmantojot vienu no šīm lomām:
    -   Elektroniskā pārskata izstrādātājs
    -   Elektronisko pārskatu veidošanas funkcionālais konsultants
    -   Sistēmas administrators

2.  Dodieties uz **organizācijas administrācija**&gt;**elektroniskās ziņošanas**.
3.  Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft**.
4.  Elementā **Microsoft** noklikšķiniet uz **Repozitoriji**. [![Update-er-from-LCS-for-MS-Open-MS-Repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Lapā **Konfigurācijas repozitoriji**, režģī atlasiet esošu repozitoriju ar tipu **LCS**. Ja šis repozitorijs netiek parādīts režģī, rīkojieties šādi:
    1.  Noklikšķiniet uz **Pievienot**, lai pievienotu jaunu repozitoriju.
    2.  Atlasiet **LCS** kā repozitorija tipu.
    3.  Noklikšķiniet uz **Izveidot repozitoriju**.
    4.  Ievadiet repozitorija nosaukumu un aprakstu.
    5.  Noklikšķiniet uz **Labi**, lai apstiprinātu jauno repozitorija ierakstu.
    6.  Režģī atlasiet jauno repozitoriju ar tipu **LCS**.

6.  Noklikšķiniet uz **Atvērt**, lai skatītu ER konfigurāciju sarakstu atlasītajam repozitorijam. [![Update-er-from-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Konfigurāciju koka skata kreisajā rūtī atlasiet nepieciešamo ER konfigurāciju.
8.  Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas nepieciešamo versiju.
9.  Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no LCS uz pašreizējo Dynamics 365 for Operations instanci. **Piezīme.** Poga **Importēt** nav pieejama ER konfigurācijas versijām, kuras jau ir pašreizējā Dynamics 365 for Operations instancē. [![Update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Piezīme.** Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Plašāku informāciju skatiet sarakstu saistītus rakstus par šo tēmu.

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)


