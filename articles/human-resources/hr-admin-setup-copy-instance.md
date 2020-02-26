---
title: Instances kopēšana
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009760"
---
# <a name="copy-an-instance"></a>Instances kopēšana

Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi. Ja jums ir cita smilškastes vide, varat arī kopēt datu bāzi no šīs vides uz mērķtiecīgu smilškastes vidi.

Lai kopētu instanci, jāpārliecinās, ka ievērots tālāk minētais.

- Human Resources instancei, ko vēlaties pārrakstīt, jābūt smilškastes videi.

- Vidēm, no kurām un uz kurām kopējat, jābūt tajā pašā reģionā. Nevar kopēt starp reģioniem.

- Jums ir jābūt administratoram mērķa vidē, lai varētu pierakstīties tajā pēc instances kopēšanas.

- Kopējot Human Resources datu bāzi, netiek kopēti Microsoft PowerApps vidē esošie elementi (programmas vai dati). Informāciju par to, kā kopēt elementus PowerApps vidē, skatiet [Vides kopēšana](https://docs.microsoft.com/power-platform/admin/copy-environment). PowerApps videi, ko vēlaties pārrakstīt, jābūt smilškastes videi. Jums ir jābūt globālā nomnieka administratoram, lai mainītu PowerApps ražošanas vidi uz smilškastes vidi. Papildinformāciju par PowerApps vides mainīšanu skatiet [Instances pārslēgšana](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Human Resources datu bāzes kopēšanas sekas

Kopējot Human Resources datu bāzi, notiek tālāk minētie notikumi.

- Kopēšanas process izdzēš esošo datu bāzi mērķa vidē. Kad kopēšanas process ir pabeigts, esošo datu bāzi nevar atgūt.

- Mērķa vide nebūs pieejama, kamēr kopēšanas process nebūs pabeigts.

- Dokumenti Microsoft Azure Blob krātuvē netiek kopēti no vienas vides uz citu. Tādējādi visi pievienotie dokumenti un veidnes netiks kopētas un paliks avota vidē.

- Nebūs pieejami visi lietotāji, izņemot administratora un citu iekšējo pakalpojumu lietotāju kontus. Tādējādi administrators var dzēst vai aptumšot datus, pirms citi lietotāji drīkst ienākt atpakaļ sistēmā.

- Administratoram ir jāveic nepieciešamās konfigurācijas izmaiņas, piemēram, integrācijas galapunktu atkārtota pieslēgšana noteiktiem pakalpojumiem vai URL.

## <a name="copy-the-human-resources-database"></a>Human Resources datu bāzes kopēšana

Lai pabeigtu šo uzdevumu, vispirms kopējiet instanci un pēc tam pierakstieties Microsoft Power Platform administrēšanas centrā, lai kopētu savu PowerApps vidi.

> [!WARNING]
> Kopējot instanci, mērķa instancē datu bāze tiek dzēsta. Šī procesa laikā mērķa instance nav pieejama.

1. Pierakstieties LCS un atlasiet LCS projektu, kas satur instanci, ko vēlaties kopēt.

2. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.

3. Atlasiet instanci, kas jākopē, un pēc atlasiet **Kopēt**.

4. Uzdevumrūtī **Kopēt instanci** atlasiet instanci, kuru pārrakstīt, un pēc tam atlasiet **Kopēt**. Uzgaidiet, līdz lauka **Kopēšanas statuss** vērtība tiek atjaunināta uz **Pabeigts**.

   ![[Instances atlasīšana pārrakstīšanai](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Atlasiet **Power Platform** un pierakstieties Microsoft Power Platform administrēšanas centrā.

   ![[Atlasiet Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Atlasiet PowerApps vidi, kas jākopē, un pēc atlasiet **Kopēt**.

7. Kad kopēšanas process ir pabeigts, pierakstieties mērķa instancē un iespējojiet Common Data Service integrāciju. Papildinformāciju un instrukcijas skatiet [Common Data Service integrācijas konfigurēšana](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Datu elementi un statusi

Kopējot Human Resources instanci, tālāk minētie datu elementi netiek kopēti:

- E-pasta adreses tabulā **LogisticsElectronicAddress**

- Pakešuzdevumu vēsture tabulās **BatchJobHistory**, **BatchHistory** un **BatchConstraintHistory**

- Vienkāršā pasta pārsūtīšanas protokola (Simple Mail Transfer Protocol — SMTP) parole tabulā **SysEmailSMTPPassword**

- SMTP releja serveris tabulā **SysEmailParameters**

- Drukas pārvaldības iestatījumi tabulās **PrintMgmtSettings** un **PrintMgmtDocInstance**

- Videi specifiski ieraksti tabulās **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** un **BatchServerGroup**

- Dokumentu pielikumi tabulā DocuValue. Šie pielikumi ietver jebkuras Microsoft Office veidnes, kas tika pārrakstītas avota vidē

- Savienojuma virkne tabulā **PersonnelIntegrationConfiguration**

Daži no šiem elementiem netiek kopēti, jo tie ir videi specifiski. Piemēram, ieraksti **BatchServerConfig** un **SysCorpNetPrinters**. Citi elementi netiek kopēti atbalsta biļešu apjoma dēļ. Piemēram, var tikt nosūtīti dublēti e-pasta ziņojumi, jo lietotāja pieņemšanas testēšanas (smilškastes) vidē joprojām ir iespējots SMTP; var tikt nosūtīti nederīgi integrācijas ziņojumi, jo aizvien ir iespējoti pakešuzdevumi, un lietotāji var būt iespējoti pirms administratori var veikt pēcatsvaidzināšanas dzēšanas darbības.

Turklāt, kopējot instanci, mainās tālāk minētie statusi.

- Visi lietotāji, izņemot administratorus, ir iestatīti uz **Atspējots**.

- Visi pakešuzdevumi, izņemot dažus sistēmas uzdevumus, ir iestatīti uz **Aizturēt**.

## <a name="environment-admin"></a>Vides administrators

Visi mērķa smilškastes vides lietotāji, ieskaitot administratorus, tiek aizstāti ar avota vides lietotājiem. Pirms instances kopēšanas, pārliecinieties, ka esat administrators mērķa vidē. Ja neesat, nevarēsiet pierakstīties mērķa smilškastes vidē pēc tam, kad kopēšana tiks pabeigta.

Visi lietotāji, kuri nav administratori, ir atspējoti mērķa smilškastes vidē, lai novērstu neatļautu pierakstīšanos smilškastes vidē. Ja, nepieciešams, administratori var no jauna iespējot lietotājus.
