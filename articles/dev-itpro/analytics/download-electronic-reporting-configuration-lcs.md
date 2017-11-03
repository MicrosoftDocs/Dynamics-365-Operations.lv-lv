---
title: "Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services"
description: "Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no Microsoft Dynamics Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā lejupielādēt elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas no Microsoft Dynamics Lifecycle Services (LCS).

Šī apmācība palīdzēs jums veikt elektronisko atskaišu veidošanas (ER) konfigurāciju jaunāko versiju lejupielādi no Microsoft Dynamics Lifecycle Services (LCS).

1.  Pierakstieties programmatūrā Dynamics 365 for Finance and Operations, izmantojot kādu no tālāk norādītajām lomām.
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
9.  Noklikšķiniet uz **Importēt**, lai lejupielādētu atlasīto versiju no pakalpojuma LCS uz pašreizējo programmatūras Dynamics 365 for Finance and Operations instanci. **Piezīme.** Poga **Importēt** nav pieejama ER konfigurācijas versijām, kas jau ir ietvertas pašreizējā programmatūras Dynamics 365 for Finance and Operations instancē. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Piezīme.** Atkarībā no ER iestatījumiem konfigurācijas tiek apstiprinātas pēc to importēšanas. Jūs varat saņemt paziņojumu par konstatētajām neatbilstības problēmām. Šīs problēmas ir jāatrisina, pirms varat izmantot importēto konfigurācijas versiju. Plašāku informāciju skatiet ar šo tēmu saistīto rakstu sarakstā.

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)




