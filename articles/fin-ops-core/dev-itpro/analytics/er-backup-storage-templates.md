---
title: Elektronisko pārskatu veidņu dublējumkopiju glabāšana
description: Šajā rakstā skaidrots, kā izmantot elektronisko pārskatu (ER) dublējuma krātuvi veidņu atgūšanai.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.custom: 27621
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable
ms.openlocfilehash: 61e6119c50ee79d8623d1b49d273fb8c07f88944
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281908"
---
# <a name="backup-storage-of-er-templates"></a>ER veidņu dublējumkopijas

[!include [banner](../includes/banner.md)]

Biznesa lietotāji izmanto [Elektronisko pārskatu (EP)](general-electronic-reporting.md), lai konfigurētu izejošo dokumentu formātus saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. Konfigurēti ER formāti var izmantot iepriekš definētas veidnes, lai izveidotu izejošos dokumentus dažādos formātos Microsoft Excel, piemēram Microsoft Word, darbgrāmatās, dokumentos vai PDF dokumentos. Veidnes ir aizpildītas ar datiem, kam ir nepieciešams ģenerēto dokumentu konfigurētais darbplūsmas.

Katru konfigurētu formātu var publicēt kā EP risinājuma daļu noteiktu izejošo dokumentu ģenerēšanai. Katru ER risinājumu var eksportēt no viena finanšu un operāciju gadījuma un importēt citā instancē.

ER struktūra izmanto dokumentu pārvaldības [konfigurēšanas sistēmu,](../../fin-ops/organization-administration/configure-document-management.md) lai pašreizējai finanšu un operāciju instancei saglabātu nepieciešamās veidnes. Atkarībā no ER struktūras iestatījumiem, Microsoft Azure Blob āšanas vai Microsoft SharePoint mapi var atlasīt kā fizisko primāro glabāšanas vietu veidnēm. (Papildinformāciju skatiet [Elektroniskā pārskata (EP) struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).) DocuValue tabulā ir atsevišķs ieraksts katrai veidnei. Katrā ierakstā **AccessInformation** lauks saglabā veidnes faila ceļu, kas atrodas konfigurētajā glabāšanas vietā.

Kad pārvaldāt finanšu un operāciju instances, iespējams, varat izlemt migrēt pašreizējo instanci uz citu vietu. Piemēram, jūs varat migrēt savu ražošanas instanci uz jaunu sandbox vidi. Ja konfigurējāt ER struktūru, lai saglabātu veidnes BLOB krātuvē, DocuValue tabula jaunajā sandbox vidē attiecas uz BLOB uzglabāšanas instanci ražošanas vidē. Tomēr šai instancei nevar piekļūt no smilškastes vides, jo migrēšanas process neatbalsta artefaktu migrāciju BLOB krātuvē. Tāpēc, ja mēģināt palaist ER formātu, kas izmanto veidni, lai ģenerētu biznesa dokumentus, tiek veikts izņēmums, un jūs tiekat informēts par trūkstošajām veidnēm. Varat arī izmantot ER tīrīšanas rīku, lai dzēstu un pēc tam atkārtoti importētu ER formāta konfigurāciju, kas satur veidni. Tā kā jums varētu būt vairāki ER formāta konfigurācijas, šis process var būt laikietilpīgs.

Lai varētu veidot biznesa dokumentus, veidnes ir iespējams izveidot, izveidojot veidnes rezerves veidnes, lai tās būtu vienmēr pieejamas.

> [!NOTE]
> Šo funkciju var izmantot tikai tad, ja BLOB krātuve ir izvēlēta kā fiziska glabāšanas vieta ER veidnēm.

## <a name="automated-recovery-and-notification"></a>Automātiskā atkopšanās un paziņojums

Šim līdzeklim katra jaunā ER formāta konfigurācijas veidne pašreizējā vidē tiek automātiski saglabāta veidņu dublējuma glabāšanas vietā (ERDocuDatabaseStorage datu bāzes tabula), kad parādās šādi notikumi:

- Jūs importējat jaunu ER formāta konfigurāciju, kas satur veidni.
- Pabeidziet ER formāta konfigurācijas versiju, kas ietver veidni.

Veidņu dublējuma kopijas tiek migrētas uz jaunu finanšu un operāciju instanci, kā daļu no programmu datu bāzes.

Ja ir nepieciešama ER formāta veidne, lai varētu izveidot izejošos dokumentus, apstrādāt kreditoru maksājumus, ieskaitot maksājumu konsultāciju un kontroles pārskatu ģenerēšanu, piemēram, bet vajadzīgā veidne nav atrodama primārajā glabāšanas vietā, šādi notiek notikumi:

- Ja veidne ir pieejama dublējuma glabāšanas vietā, tā tiek automātiski ņemta no dublējuma glabāšanas vietas, atjaunota primārajā glabāšanas vietā un tiek izmantota pašreizējai izpildei.
- Katrs lietotājs, kuram ir piešķirta **Elektroniskās pārskatu izstrādātāja** vai **sistēmas administratora** loma, tiek informēts par trūkstošo veidnes izdošanu, izmantojot darbību centru. Ziņojums, kas tiek parādīts, ir atkarīgs no vērtības, **kas tiek automātiski izpildīta, atjaunojot bojātas** veidnes partijas parametrā:

    - Ja šis parametrs ir iestatīts kā **izslēgts**, ziņojums iesaka sākt pakešveida apstrādi, lai automātiski LABOTU līdzīgas problēmas citiem er formāta konfigurācijas veidnēm. Ziņojumā ir ietverta saite, ko var izmantot, lai sāktu pakešveida apstrādi.
    - Ja šis parametrs ir iestatīts kā **on**, paziņojums paziņo jums, ka trūkstošās veidnes problēma ir atklāta un ka jauns pakešapstrādes process, **atjaunot sarautas veidnes no iekšējās datu bāzes** dublējumkopijas, ir automātiski plānotais. Šī Pakešapstrāde automātiski noteiks līdzīgas problēmas citām veidnēm.

Lai iestatītu parametru **Automātiski izpildīt procedūru, lai atjaunotu bojātas veidnes partijā**, veiciet tālāk norādītās darbības.

1. Finansēs un operācijās atveriet lapu **Organizācijas administrēšanas \> elektronisko pārskatu \> konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **lietotāja parametri** Iestatiet nepieciešamo vērtību **automātiski palaist procedūru, kā atjaunot bojātas veidnes partijas** parametrā.

> [!NOTE]
> Šis parametrs ir definēts kā lietojumprogrammas lietotājs un reģistrēts uzņēmums.

![ER konfigurāciju lapa.](./media/GER-BackupTemplates-1.png)

Sekojošajā attēlā ir parādīts ziņojuma piemērs, kas parādās, parametrs **Automātiski izpildīt procedūru, kas tiek veikta, atjaunojot bojātas veidnes partijas** ir iestatīts uz **Ieslēgts**.

![Kreditora maksājumu žurnāla rinda.](./media/GER-BackupTemplates-2.png)

Sekojošajā attēlā ir parādīts pakešveida apstrādes process **Atjaunot bojātās veidnes no iekšējās datu bāzes dublēšanas** lapā **Pakešuzdevums**.

![Lapa Pakešuzdevumi.](./media/GER-BackupTemplates-3.png)

Izpildes žurnāls pabeigtajām **atjaunošanas sarautajām veidnēm, kas atrodas iekšējās** datu bāzes dublēšanas pakešuzdevuma procesā, ietver informāciju par veidnēm, kas atjaunotas no dublējuma glabāšanas vietas uz primāro krātuves vietu.

![Pakešuzdevumu vēstures lapa.](./media/GER-BackupTemplates-4.png)

Pēc noklusējuma automātiski tiek izveidotas to veidņu dublējumkopijas, kas atrodas ER formāta konfigurācijās. Lai beigtu izveidot veidņu dublējumkopijas, iestatiet opciju **Pārtraukt veidot veidnes dublējumkopijas** uz **Jā** lapas **Elektroniskie pārskatu parametri** cilnē **Pielikumi**. Šo lapu varat atvērt, izmantojot darba vidi **Elektroniskais pārskats**.

Ja iestatāt opciju **Pārtraukt veidot veidņu dublējumkopijas** uz **Jā** un nevēlaties paturēt dublējumkopijas, kas iepriekš tika veidotas no veidnēm, atlasiet **Iztīrīt dublējumu krātuvi** lapā **Elektronisko pārskatu parametri**.

Ja jūs jauninājāt vidi uz finansēm un operāciju versiju 10.0.5 (2019. gada oktobris) un vēlaties migrēt uz jaunu vidi, kas ietver ER formāta konfigurācijas, kuras var darbināt, **·** **pirms** migrācijas atlasiet Aizpildīt dublējuma krātuvi Elektronisko pārskatu parametru lapā. Šī poga sāk visu pieejamo veidņu dublējumkopijas izveidošanas procesu, lai tos varētu uzglabāt ar ER dublējuma glabāšanas vietu veidnēm.

![Elektronisko pārskatu veidošanas parametru lapa.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Manuāla atkopšanās

Dodieties uz **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Atjaunot bojātās veidnes**, lai manuāli iniciētu iespēju atjaunot ER veidnes no dublējuma glabāšanas vietas uz primāro glabāšanas vietu. Pirms sākat šo procesu, lapā **Atjaunot bojātās veidnes** varat norādīt, vai tā tiks veikta interaktīvi, vai arī tiks plānota pakešveida apstrāde.

## <a name="supported-deployments"></a>Atbalstītie izvietojumi

Finanšu un operāciju versijā 10.0.5 ER veidņu dublējuma glabāšanas funkcija ir pieejama tikai mākoņa izvietošanā.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)

[Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
