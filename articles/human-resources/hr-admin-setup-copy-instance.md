---
title: Instances kopēšana
description: Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20a2ffb44f9b99800146e3365e6f0d6df8e9a75e
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324266"
---
# <a name="copy-an-instance"></a>Instances kopēšana

_**Attiecas uz:** savrupas infrastruktūras personāla vadība_ 

> [!NOTE]
> Sākot no 2022. gada jūnija, cilvēkresursu vides var izvietot tikai finanšu un operāciju programmas infrastruktūrai. Papildinformāciju skatiet finanšu [un operāciju infrastruktūras sadaļu Personāla vadības nodrošināšana](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finanšu un operāciju infrastruktūra neatbalsta kopijas instances funkciju. Varat izvietot jaunas vides un izmantot datu bāzes kustības, lai izveidotu kopijas. Papildinformāciju par pašapkalpošanās izvietošanu skatiet pārskatu [par pašapkalpošanās izvietošanu](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Papildinformāciju par datu bāzes kustību finanšu un operāciju infrastruktūrai skatiet datu bāzes [pārvietošanas operāciju mājas lapā](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi. Ja jums ir cita smilškastes vide, varat arī kopēt datu bāzi no šīs vides uz mērķtiecīgu smilškastes vidi.

Lai kopētu instanci, ņemiet vērā šādus padomus:

- Human Resources instancei, ko vēlaties pārrakstīt, jābūt smilškastes videi.

- Vidēm, no kurām un uz kurām kopējat, jābūt tajā pašā reģionā. Nevar kopēt starp reģioniem.

- Jums ir jābūt administratoram mērķa vidē, lai varētu pierakstīties tajā pēc instances kopēšanas.

- Kopējot Human Resources datu bāzi, netiek kopēti Microsoft Power Apps vidē esošie elementi (programmas vai dati). Informāciju par to, kā kopēt elementus Power Apps vidē, skatiet [Vides kopēšana](/power-platform/admin/copy-environment). Power Apps videi, ko vēlaties pārrakstīt, jābūt smilškastes videi. Jums ir jābūt globālā nomnieka administratoram, lai mainītu Power Apps ražošanas vidi uz smilškastes vidi. Papildinformāciju par Power Apps vides mainīšanu skatiet [Instances pārslēgšana](/dynamics365/admin/switch-instance).

- Ja nokopējat instanci savā smilškastes vidē un vēlaties integrēt smilškastes vidi ar Dataverse, ir atkārtoti jāizmanto pielāgoti lauki Dataverse tabulām. Skatiet [Lietot pielāgotus laukus Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Human Resources datu bāzes kopēšanas sekas

> [!Note]
> Sākot no 2022. gada, Microsoft Azure dokumenti BLOB krātuvē tiek iekļauti, kopējot ražošanas vidi uz kases vides. Visi pievienotie dokumenti un veidnes tiks kopēti no avota vides uz mērķa vidi.

Kopējot Human Resources datu bāzi, notiek tālāk minētie notikumi.

- Kopēšanas process izdzēš esošo datu bāzi mērķa vidē. Kad kopēšanas process ir pabeigts, esošo datu bāzi nevar atgūt.

- Mērķa vide nebūs pieejama, kamēr kopēšanas process nebūs pabeigts.

- Visi lietotāji, izņemot tos, kuriem ir drošības loma Sistēmas administrators, un citi iekšējo pakalpojumu lietotāju konti nav pieejami. Lietotājs Administrators var dzēst datus, pirms citi lietotāji ir atļauti atpakaļ sistēmā.

- Administratoram ir jāveic nepieciešamās konfigurācijas izmaiņas, piemēram, integrācijas galapunktu atkārtota pieslēgšana noteiktiem pakalpojumiem vai URL.

## <a name="copy-the-human-resources-database"></a>Human Resources datu bāzes kopēšana

Lai pabeigtu šo uzdevumu, vispirms kopējiet instanci un pēc tam pierakstieties Microsoft Power Platform administrēšanas centrā, lai kopētu savu Power Apps vidi.

> [!WARNING]
> Kopējot instanci, mērķa instancē datu bāze tiek dzēsta. Šī procesa laikā mērķa instance nav pieejama.

1. Pierakstieties LCS un atlasiet LCS projektu, kas satur instanci, ko vēlaties kopēt.

2. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.

3. Atlasiet instanci, kas jākopē, un pēc atlasiet **Kopēt**.

4. Uzdevumrūtī **Kopēt instanci** atlasiet instanci, kuru pārrakstīt, un pēc tam atlasiet **Kopēt**. Uzgaidiet, līdz **lauks Kopēt** statusu tiks atjaunināts uz **Pabeigts**.

   ![[Atlasīt pārrakstāmo instanci.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Atlasiet **Power Platform** un pierakstieties Microsoft Power Platform administrēšanas centrā.

   ![[Atlasiet Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Atlasiet Power Apps vidi, kas jākopē, un pēc atlasiet **Kopēt**.

Papildinformāciju par vides Power Apps kopēšanu skatiet sadaļā [Vides kopēšana](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Kad kopēšanas process ir pabeigts, pierakstieties mērķa instancē un iespējojiet Dataverse integrāciju. Papildinformāciju un instrukcijas skatiet [Pakalpojuma Dataverse integrācijas konfigurēšana](./hr-admin-integration-common-data-service.md).

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

Daži no šiem elementiem netiek kopēti, jo tie ir videi specifiski. Piemēram, ieraksti **BatchServerConfig** un **SysCorpNetPrinters**. Citi elementi netiek kopēti atbalsta biļešu apjoma dēļ. Piemēram:

- E-pasta kopijas var tikt nosūtītas, jo SMTP joprojām ir iespējots lietotāja pieņemšanas testēšanas (smilškastes) vidē.

- Nederīgi integrācijas ziņojumi var tikt nosūtīti, jo pakešuzdevumi joprojām ir iespējoti.

- Lietotāji var būt iespējoti, pirms administratori var veikt pēcatsvaidzināšanas tīrīšanas darbības.

Turklāt, kopējot instanci, mainās tālāk minētie statusi.

- Visi lietotāji, izņemot tos, kuriem ir loma Sistēmas administrators, ir iestatīti kā **Atspējoti**.

- Visi pakešuzdevumi, izņemot dažus sistēmas uzdevumus, ir iestatīti uz **Aizturēt**.

## <a name="environment-admin"></a>Vides administrators

Visi mērķa smilškastes vides lietotāji, ieskaitot administratorus, tiek aizstāti ar avota vides lietotājiem. Pirms instances kopēšanas, pārliecinieties, ka esat administrators avota vidē. Ja ne, jūs nevarat pieteikties mērķa kastē vidē pēc kopēšanas pabeigšanas.

Visi lietotāji, kuri nav administratori, ir atspējoti mērķa smilškastes vidē, lai novērstu neatļautu pierakstīšanos smilškastes vidē. Ja, nepieciešams, administratori var no jauna iespējot lietotājus.

## <a name="apply-custom-fields-to-dataverse"></a>Lietot pielāgotus laukus Dataverse

Ja nokopējat instanci savā smilškastes vidē un vēlaties integrēt smilškastes vidi ar Dataverse, ir atkārtoti jāizmanto pielāgoti lauki Dataverse tabulām.

Katram pielāgotajam laukam, kas ir pakļauts Dataverse tabulām, veiciet šādas darbības:

1. Dodieties uz pielāgoto lauku un atlasiet **Rediģēt**.

2. Noņemiet opciju **Iespējots** lauks katrai cdm_* entītijai, kurai ir iespējots pielāgots lauks.

3. Atlasiet **Lietot izmaiņas**.

4. Vēlreiz atlasiet **Rediģēt**.

5. Atlasiet opciju **Iespējots** lauks katrai cdm_* entītijai, kurai ir iespējots pielāgots lauks.

6. Vēlreiz atlasiet **Lietot izmaiņas**.

Noņemšana, izmaiņu lietošana, atkārtota atlase un atkārtota izmaiņu veikšana pieprasa atjaunināt shēmu Dataverse, lai iekļautu pielāgotos laukus.

Plašāku informāciju par pielāgotajiem laukiem, skatiet rakstā [Darbs ar pielāgotiem laukiem un to izveide](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Skatiet arī

[Human Resources nodrošināšana](hr-admin-setup-provision.md)</br>
[Noņemt instanci](hr-admin-setup-remove-instance.md)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
