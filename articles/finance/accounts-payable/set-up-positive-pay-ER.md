---
title: Iestatīt un ģenerēt pozitīvo maksājumu failus, izmantojot elektroniskos pārskatus
description: Šajā tēmā skaidrots, kā iestatīt pozitīvo maksājumu, izmantojot elektroniskos pārskatus.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544552"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Iestatīt pozitīvo maksājumu failus, izmantojot elektroniskos pārskatus

Iestatiet pozitīvo maksājumu, lai izveidotu elektronisku čeku sarakstu, kas tiek iesniegts bankai. Kad čeks ir iesniegts bankai, banka to salīdzina ar čeku sarakstu. Ja čeks atbilst čekam sarakstā, banka to dzēš. Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronisko pārskatu izveides konfigurācijas iestatīšana

1. Dodieties uz **elektronisko darbvietu \> pārskatu**.
2. Microsoft **konfigurācijas nodrošinātāja** elementā atlasiet **Repositories**.
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Ja ir jāizveido savienojums ar repozitoriju, dialoglodziņā atlasiet zilo saiti.
5. Konfigurācijas sarakstā atrodiet un atlasiet Pozitīvā maksājuma **modeļa pozitīvā \> maksājuma formātu**.
6. Kopsavilkuma cilnē **Versijas** atlasiet jaunāko versiju un pēc tam atlasiet **Importēt**.

## <a name="set-up-a-positive-pay-format"></a>Iestatīt pozitīvā maksājuma formātu

1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldības \> iestatījuma \> pozitīvajiem maksājuma formātiem**.
2. Atlasiet **Jauna**.
3. Iestatiet maksājuma **formāta un** apraksta **laukus**.
4. Atzīmējiet **izvēles rūtiņu Vispārējs elektroniskā** eksporta formāts.
5. Iestatiet eksporta **formāta konfigurācijas lauku** pozitīvā **maksājuma formātā**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Pozitīvā maksājuma formāta piešķiršana bankas kontam

1. Dodieties uz **skaidras naudas un bankas pārvaldības \> banku kontiem \> Bankas konti**.
2. Atveriet bankas kontu.
3. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku Pozitīvā **maksājuma formāts** uz iepriekš izveidoto formātu.
4. Laukā Pozitīvā **maksājuma sākuma datums** iestatiet pašreizējo datumu.

## <a name="generate-a-positive-pay-file"></a>Ģenerēt pozitīvā maksājuma failu

1. Dodieties uz **skaidras naudas un bankas pārvaldības \> bankas kontu \> bankas kontiem**.
2. Atveriet bankas kontu, kam ir iestatīti pozitīvais pārskaitījums.
3. Atlasiet Pārvaldīt **maksājumu pozitīvā \> maksājuma \> pozitīvā maksājuma failu**.
4. **Iestatiet beigu datuma** lauku. Tiks iekļauti čeki, kas tika ģenerēti pirms šī datuma.

Rezultātā iegūtais XML fails tiks lejupielādēts.
