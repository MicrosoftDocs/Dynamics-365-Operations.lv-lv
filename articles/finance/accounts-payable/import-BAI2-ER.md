---
title: Iestatīt detalizēto bankas darbību saskaņošanas importēšanu, izmantojot elektroniskos pārskatus
description: Šajā rakstā ir izskaidrots, kā izmantot elektroniskos pārskatus, lai iestatītu detalizēto bankas darbību saskaņošanas importa procesu.
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
ms.openlocfilehash: d24e117b21e291dba1e41d9fa15187b84ff795cf
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752725"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Iestatīt detalizēto bankas darbību saskaņošanas importēšanu, izmantojot elektroniskos pārskatus

[!include [banner](../includes/banner.md)]

Detalizētās bankas darbību saskaņošanas funkcija ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar bankas Microsoft Dynamics darbībām 365 Finansēs. Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem. Bankas izraksta importēšanas iestatījumi ir dažādi, un tie ir atkarīgi no jūsu elektroniskā bankas izraksta formāta. Microsoft Dynamics 365 Finanses atbalsta trīs bankas pārskatu formātus: ISO20022, MT940 un BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronisko pārskatu izveides konfigurācijas iestatīšana

1. Dodieties uz **elektronisko darbvietu \> pārskatu**.
2. Microsoft **konfigurācijas nodrošinātāja** elementā atlasiet **Repositories**.
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Ja ir jāizveido savienojums ar repozitoriju, dialoglodziņā atlasiet zilo saiti.
5. Konfigurācijas sarakstā atrodiet detalizēto **bankas darbību saskaņošanas izraksta modeli \> ABR BAI2 formātu**.
6. **Atlasiet BAI2** formātu.
7. Kopsavilkuma cilnē **Versijas** atlasiet jaunāko versiju un pēc tam atlasiet **Importēt**.

## <a name="set-up-the-bank-statement-format"></a>Iestatīt bankas izraksta formātu

1. Dodieties uz **skaidras naudas un bankas pārvaldības \> iestatīšanas \> detalizēto bankas darbību saskaņošanas \> iestatījumu bankas izraksta formātu**.
2. Atlasiet **Jauna**.
3. Iestatiet izraksta **formātu un** nosaukuma **laukus**.
4. Atzīmējiet **izvēles rūtiņu Vispārējs elektroniskās importēšanas** formāts.
5. Iestatiet importa **formāta konfigurācijas** lauku **UZ NO2** formātu.

## <a name="set-up-the-bank-account"></a>Iestatīt bankas kontu

1. Atveriet sadaļu **Kases un bankas vadība \> Banku konti \> Banku konti**.
2. Atveriet bankas kontu.
3. Kopsavilkuma cilnē **Saskaņošana** iestatiet opciju Detalizēta bankas **darbību saskaņošana uz** **Jā**.
4. Iestatiet pārskata **formāta** lauku uz iepriekš **izveidotu ESAT2** formātu.

## <a name="import-the-bank-statement"></a>Importēt bankas izrakstu

1. Dodieties uz **kases un bankas pārvaldības bankas \> izrakstu saskaņošanas bankas \> izrakstiem**.
2. Bankas izrakstu lapas **augšpusē atlasiet Importēt izrakstu** **.**
3. **Iestatiet bankas konta** lauku bankas kontā izrakstā.
4. Iestatiet pārskata **formāta** lauku uz iepriekš **izveidotu ESAT2** formātu.
5. Atlasiet **Pārlūkot** un atlasiet **EXE** failu.
6. Atlasiet **Augšupielādēt**.
7. Atlasiet **Labi,** lai importētu atlasīto failu.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Bankas izrakstu formātu un tehnisko izkārtojumu paraugi
Tālāk ir sniegti detalizētās bankas darbību saskaņošanas importētā faila tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili: [Failu piemēru importēšana](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

