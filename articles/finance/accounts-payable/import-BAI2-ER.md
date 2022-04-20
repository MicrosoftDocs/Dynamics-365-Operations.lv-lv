---
title: Iestatīt detalizēto bankas darbību saskaņošanas importēšanu, izmantojot elektroniskos pārskatus
description: Šajā tēmā skaidrots, kā izmantot elektroniskos pārskatus, lai iestatītu detalizēto bankas darbību saskaņošanas importa procesu ATTIECĪBĀ UZ 2 pārskatiem.
author: panolte
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
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544556"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Iestatīt detalizēto bankas darbību saskaņošanas importēšanu, izmantojot elektroniskos pārskatus

[!include [banner](../includes/banner.md)]

Detalizētās bankas darbību saskaņošanas funkcija ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar bankas Microsoft Dynamics darbībām 365 Finansēs. Šajā tēmā skaidrots, kā iestatīt importa funkcionalitāti jūsu KURU KURU bankas izrakstiem.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronisko pārskatu izveides konfigurācijas iestatīšana

1. Dodieties uz **elektronisko darbvietu \> pārskatu**.
2. Microsoft **konfigurācijas nodrošinātāja** elementā atlasiet **Repositories**.
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Ja ir jāizveido savienojums ar repozitoriju, dialoglodziņā atlasiet zilo saiti.
5. Konfigurācijas sarakstā atrodiet BANKAS izraksta **modeļa BANKAS \> izraksta modeli NO BAI2**.
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
