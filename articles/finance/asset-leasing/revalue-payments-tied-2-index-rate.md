---
title: Ar indeksa likmi saistīto nomas maksājumu pārvērtēšana
description: Šajā rakstā ir aprakstīta korekcija, kas tiek veikta, lai nomātu saistības attiecībā uz lietošanas tiesību (RUB) līdzekli, ja mainās mainīgi nomas maksājumi indeksa likmes maiņas dēļ.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903252"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Ar indeksa likmi saistīto nomas maksājumu pārvērtēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta korekcija, kas ir veikta saistībā ar nomas saistībām par lietošanas tiesības (RUB) līdzekli, ja mainās mainīgi nomas maksājumi indeksa likmes maiņas dēļ. Nomas saistības un LLT tiks pielāgotas kontam, ņemot vērā jaunās maksājumu summas. Saskaņā ar uzskaites standartu kodifikācijas tēmu 842 (ASC 842), kas ir standarts vispārpieņemtajos uzskaites principos ASV (US GAAP), mainīgie maksājumi tiek mainīti tikai, ja maksājumi pieaug vai samazinās indeksa likmes maiņas dēļ, ja vien nav citas naudas plūsmu izmaiņas. Šīs papildu izmaiņas var ietvert nomas noteikumu izmaiņas, kas saistītas ar procentu likmēm. Papildinformāciju skatiet šeit: ASC 842-10-55-225 un starptautisko finanšu pārskatu standarta 16 (IFRS 16) 42(b) rindkopa.

## <a name="adjust-lease-payments"></a>Nomas maksājumu koriģēšana

Ar indeksa likmi saistīto nomas maksājumu pārvērtēšanai veiciet tālāk norādītās darbības.

1. Lai izpildītu nomas indeksa pārvērtēšanas procesu, dodieties uz **Līdzekļu noma \> Periodisks \> Indeksa likmes pārvērtēšana**.

    Tiek parādīta lapa **Indeksa likmes pārvērtēšana**, un tā parāda visus iepriekšējos nomas indeksa pārvērtēšanas procesus, kas ir izpildīti. Šajā lapā iekļautā informācija ietver procesa ID, kas tika ģenerēts no numuru sērijas iestatījumiem, juridisko personu, koriģēto nomas grāmatu skaitu, kopējo saistību korekciju IFRS 16 nomai un kopējās mainīgās izmaksas, kas tika koriģētas ASC 842 nomām.

2. Lai izpildītu pārvērtēšanu, darbību rūtī atlasiet **Nomas indeksa pārvērtēšana**.

    Tiek parādīts dialoglodziņš **Indeksa pārvērtēšanas parametri**. Šeit varat filtrēt un atlasīt, kuras nomas, nomas grupas vai citi kritēriji jāizmanto, kad atlasāt nomas, kas jāpārvērtē. Turklāt cilnē **Izpildīt fonā** varat iestatīt indeksa pārvērtēšanas procesu tā, lai tas darbotos partijā.

4. Atlasiet filtrus, lai atlasītu nomas, kas jāiekļauj fona apstrādē, un pēc tam atlasiet **Labi**.

    Tiek parādīts dialoglodziņš **Indeksa likmes pārvērtēšanas priekšskatījums**, kurā ir parādītas nomas, kas tiks pārvērtētas. Tas parāda arī līdzekļu un saistību korekcijas vai mainīgo maksājumu korekcijas.

5. Lai novērstu iespēju, ka noma tiktu pārvērtēta, atlasiet nomas, kas **ir** jāpārvērtē. Ja neatlasāt nevienu nomu, visas nomas tiks pārvērtētas. Kad esat pabeidzis, atlasiet **Labi**, lai pārvērtētu nomas maksājumus.
6. Lai skatītu darījumus, kas tika izveidoti noteiktam indeksa pārvērtēšanas procesam, atlasiet procesa ID un pēc tam atlasiet **Darījumi**.

    Tiek parādīts dialoglodziņš, kurā ir detalizēta informācija par darījumiem, kas tika izveidoti apstrādes laikā.

> [!NOTE]
> Var pārvērtēt tikai nomas, kam pārvērtēšanas datums ir pirms sistēmas datuma vai tajā. Sistēma automātiski ignorē visas nomas, kurām pārvērtēšanas datums ir vēlāks nekā sistēmas datums.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 nomas — indeksa pārvērtēšana

Lai skatītu nomas pārvērtēšanas procesa ietekmi uz ASC 842 nomām, atveriet maksājumu grafiku nomai. Lapā tiek rādīti tikai tie mainīgie maksājumi, kas veikti pārvērtēšanas datumā vai pēc tā, tika mainīti indeksa pārvērtēšanas dēļ. Amortizācijas un nolietojuma grafiki paliek nemainīgi. Kad izveidojat rēķinu ar mainīgu maksājumu, mainīgais maksājums tiek debitēts mainīgā maksājuma grāmatošanas kontā. Arī mainīgā maksājuma summa tiek pievienota kredīta ierakstam, kas ir grāmatots tieši kreditoram, vai grāmatots maksājamo notu kontā atkarībā no nomas grāmatas iestatījuma.

Maksājumu grafika rindas nomas informācijas lapā tiek automātiski atjauninātas ar jaunu rindu, kas norāda jauno indeksa likmi. Turklāt kolonna rāda, vai rinda ir izveidota manuāli vai izmantojot indeksa pārvērtēšanas procesu.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 nomas — indeksa pārvērtēšana

Lai skatītu nomas pārvērtēšanas procesa ietekmi uz IFRS 16 nomām, atveriet nomas informāciju koriģētajai nomai. Lauki **Nomas termiņš** un **Līdzekļa lietderīgās lietošanas laiks** ir atjaunināti, lai atspoguļotu laika posmu no sākuma datuma vai modifikācijas datuma līdz pārvērtēšanas datumam. Turklāt maksājumu grafika rindas ir atjauninātas, lai atspoguļotu jaunos nomas maksājumus, jauno indeksa likmi un to, kā rinda tika izveidota.

Varat skatīt tikko izveidoto maksājumu grafiku, kas sākas pārvērtēšanas datumā, un parādīt kopējo atjaunināto maksājuma summu. Jauns nomas saistību amortizācijas grafiks un līdzekļu nolietojuma grafiks arī ir izveidots, lai atspoguļotu koriģēto maksājumu grafiku.

Žurnāla ieraksts automātiski iegrāmatoja korekcijas žurnāla ierakstu kontā izmaiņām nomas maksājumos, kas saistīti ar indeksa pārvērtēšanu.

> [!NOTE]
> **·** **·** **Ja** detalizētās informācijas par nomu lapas kopsavilkuma cilnē Vispārīgi ir iespējota opcija Sadalījuma maksājuma summa un saistītā grāmata ir IFRS 16, indeksa pārvērtēšanas process **automātiski** pievienos ierakstu dialoglodziņā Maksājuma summas sadalījumam. Šī summa atspoguļos izmaiņas, kas tika veiktas maksājumam indeksa pārvērtēšanas dēļ. Ieraksts tiks atzīmēts kā Lietots **IRFS 16 indeksa pārvērtēšanā**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
