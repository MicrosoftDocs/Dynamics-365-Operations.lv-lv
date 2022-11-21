---
title: Detalizētas banku darbību saskaņošanas importēšanas iestatīšana, izmantojot elektroniskos pārskatus
description: Šajā rakstā ir paskaidrots, kā izmantot elektroniskos pārskatus, lai iestatītu detalizēto bankas darbību saskaņošanas importēšanas procesu.
author: angelad116
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: bfc1c2021387ed35e6ccb513167e896eddef2eaf
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759605"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Detalizētas banku darbību saskaņošanas importēšanas iestatīšana, izmantojot elektroniskos pārskatus

[!include [banner](../includes/banner.md)]

Uzlabotās bankas saskaņošanas funkcija ļauj importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar bankas darījumiem programmā Microsoft Dynamics 365 Finance. Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem. Bankas izraksta importēšanas iestatījumi ir dažādi, un tie ir atkarīgi no jūsu elektroniskā bankas izraksta formāta. Microsoft Dynamics 365 Finance atbalsta trīs bankas izrakstu formātus: ISO20022, MT940 un BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronisko pārskatu veidošanas konfigurācijas iestatīšana

1. Dodieties uz Darbvietas **\> elektroniskie pārskati**.
2. Microsoft **konfigurācijas nodrošinātāja** elementā atlasiet **Repozitoriji**.
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Ja ir jāizveido savienojums ar repozitoriju, dialoglodziņā atlasiet zilo saiti.
5. Konfigurāciju sarakstā atrodiet paplašinātā **bankas saskaņošanas pārskata modeļa ABR \> BAI2 formātu**.
6. **Atlasiet BAI2** formātu.
7. Kopsavilkuma **cilnē Versijas** atlasiet jaunāko versiju un pēc tam atlasiet **Importēt**.

>[!NOTE]
>**BAI2** bankas izraksta modelis vēlāk būs novecojis. 

## <a name="set-up-the-bank-statement-format"></a>Bankas izraksta formāta iestatīšana

1. Pārejiet uz formātu **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Bankas izlīguma \> papildu iestatīšana**.
2. Atlasiet **Jauna**.
3. Iestatiet **formātu Paziņojums** un **Nosaukums**.
4. Atzīmējiet izvēles rūtiņu **Vispārējs elektroniskās importēšanas formāts**.
5. Iestatiet **lauka Importēt formāta konfigurāciju** uz **BAI2** formātu.

## <a name="set-up-the-bank-account"></a>Bankas konta iestatīšana

1. Atveriet sadaļu **Kases un bankas vadība \> Banku konti \> Banku konti**.
2. Atveriet bankas kontu.
3. Kopsavilkuma **cilnē Saskaņošana** opcijai Bankas papildu saskaņošana **iestatiet** vērtību **Jā**.
4. Laukā Paziņojuma formāts **iestatiet** iepriekš **izveidoto BAI2** formātu.

## <a name="import-the-bank-statement"></a>Bankas izraksta importēšana

1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldības \> bankas izrakstu saskaņošana \> Bankas izraksti**.
2. Lapas Bankas pārskati **augšdaļā** atlasiet **Importa pārskats**.
3. Pārskatā laukā Bankas konts **iestatiet** uz bankas kontu.
4. Laukā Paziņojuma formāts **iestatiet** iepriekš **izveidoto BAI2** formātu.
5. Atlasiet **Pārlūkot** un BAI **failu**.
6. Atlasiet **Augšupielādēt**.
7. Atlasiet **Labi**, lai importētu atlasīto failu.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Bankas izrakstu formātu un tehnisko izkārtojumu paraugi
Tālāk ir sniegti detalizētās bankas darbību saskaņošanas importētā faila tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili: [Failu piemēru importēšana](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

