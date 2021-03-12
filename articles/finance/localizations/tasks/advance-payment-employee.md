---
title: EEU-00047 avansa maksājums darbiniekam
description: Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98152c9a0b471977a00ef875dba5d102c1de80f9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990045"
---
# <a name="eeu-00047-advance-payment-to-employee"></a>EEU-00047 avansa maksājums darbiniekam

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt un reģistrēt darbības avansa turētājam. Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Lietuvā. Šis uzdevums ir paredzēts tikai juridiskām personām, kuru primārā adrese ir Polijā, Lietuvā, Latvijā, Igaunijā, Čehijā vai Ungārijā. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-a-new-cash-account"></a>Izveidot jaunu kases kontu
1. Dodieties uz Kases un bankas vadība > Bankas konti > Kases konti.
2. Noklikšķiniet uz Jauns.
3. Laukā Kase ierakstiet kādu vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Numuru sērijas grupa ievadiet vai atlasiet kādu vērtību.
6. Izvērsiet sadaļu Apstiprināšana.
7. Laukā Valūta ievadiet vai atlasiet kādu vērtību.
8. Atlasiet Jā laukā Negatīvs atlikums kasē.
9. Noklikšķiniet uz Saglabāt.

## <a name="create-a-new-journal"></a>Izveidot jaunu žurnālu
1. Pārejiet uz sadaļu Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Klikšķiniet Jauns.
7. Laukā Nosaukums ierakstiet kādu vērtību.
8. Atlasiet opciju laukā Žurnāla veids.
9. Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.
10. Noklikšķiniet uz Saglabāt.

## <a name="create-an-advance-holder-group"></a>Izveidot avansa turētāju grupu
1. Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Avansa turētāju grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Grupa ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.

## <a name="create-an-employee-posting-profile"></a>Izveidot darbinieka grāmatošanas metodi
1. Dodieties uz Parādi kreditoriem > Iestatīšana > Avansa turētāji > Darbinieku grāmatošanas metodes.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vērtību laukā Grāmatošanas metode.
4. Apraksta laukā ierakstiet vērtību.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Atlasiet opciju laukā Derīguma termiņš.
7. Laukā Summu konts norādiet vēlamās vērtības.
8. Noklikšķiniet uz Saglabāt.

## <a name="set-up-advance-holder-parameters"></a>Iestatīt avansa turētāja parametrus
1. Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.
2. Noklikšķiniet uz cilnes Avansa turētāji.
3. Laukā Grāmatošanas metode ievadiet vai atlasiet kādu vērtību.
4. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
5. Laukā Kase ievadiet vai atlasiet kādu vērtību.
6. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
7. Laukā Konta tips atlasiet opciju.
8. Laukā Galvenais konts norādiet vēlamās vērtības.
9. Noklikšķiniet uz cilnes Numuru sērijas.
10. Noklikšķiniet uz Saglabāt.

## <a name="set-up-a-cash-posting-profile"></a>Iestatīt kases grāmatošanas metodi
1. Dodieties uz Kases un bankas vadība > Iestatīšana > Kases grāmatošanas metodes.
2. Noklikšķiniet uz Jauns.
3. Laukā Kases grāmatošana ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Atlasiet opciju laukā Derīguma termiņš.
7. Laukā Galvenais konts norādiet vēlamās vērtības.
8. Noklikšķiniet uz Saglabāt.

## <a name="set-up-cash-and-bank-parameters"></a>Iestatīt kases un bankas parametrus
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Kase.
3. Laukā Kase ievadiet vai atlasiet kādu vērtību.
4. Laukā Kases grāmatošana ievadiet vai atlasiet kādu vērtību.
5. Klikšķiniet Saglabāt.
6. Noklikšķiniet uz cilnes Numuru sērijas.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz Saglabāt.

## <a name="set-up-terms-of-payment"></a>Iestatiet maksājumu nosacījumus
1. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Apmaksas nosacījumi.
2. Noklikšķiniet uz Rediģēt.
3. Atlasiet Jā laukā No avansa turētāja.
4. Noklikšķiniet uz Saglabāt.

## <a name="create-a-new-worker"></a>Izveidot jaunu darbinieku
1. Pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki.
2. Noklikšķiniet uz Jauns.
3. Laukā Vārds ierakstiet kādu vērtību.
4. Laukā Uzvārds ierakstiet kādu vērtību.
5. Laukā Darbinieka ID ierakstiet vērtību.
6. Noklikšķiniet uz Pieņemt darbā jaunu darbinieku.
7. Noklikšķiniet uz Saglabāt.

## <a name="set-up-a-worker-as-an-advance-holder"></a>Iestatīt darbinieku kā avansa turētāju
1. Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.
2. Noklikšķiniet uz Rediģēt.
3. Laukā Grupa ievadiet vai atlasiet kādu vērtību.
4. Atlasiet Jā laukā Avansa turētājs.
5. Noklikšķiniet uz Saglabāt.

## <a name="create-and-post-a-purchase-order-invoice"></a>Izveidot un grāmatot pirkšanas pasūtījuma rēķinu
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vai atlasiet vērtību laukā kreditora konts.
4. Noklikšķiniet uz Labi.
5. Laukā Rindas vai virsraksts atlasiet opciju.
6. Izvērsiet sadaļu Cena un atlaide.
7. Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.
8. Laukā Avansa turētājs ievadiet vai atlasiet kādu vērtību.
9. Laukā Rindas vai virsraksts atlasiet opciju.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
12. Laukā Daudzums ievadiet skaitli.
13. Laukā Vienības cena ievadiet kādu skaitli.
14. Noklikšķiniet uz Saglabāt.
15. Darbību rūtī noklikšķiniet uz Pirkt.
16. Noklikšķiniet uz Apstiprināt.
17. Darbību rūtī noklikšķiniet uz Rēķins.
18. Noklikšķiniet uz Rēķins.
19. Noklikšķiniet uz Noklusējums no: Produktu ieejas plūsmu daudzums, lai atvērtu nolaižamo dialoglodziņu.
20. Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.
21. Noklikšķiniet uz Labi.
22. Laukā Numurs ierakstiet kādu vērtību.
23. Laukā Rēķina apraksts ierakstiet vērtību.
24. Ievadiet datumu laukā Rēķina datums.
25. Ievadiet datumu PVN reģistra datums.
26. Laukā Saņemt dokumenta datumu ievadiet kādu datumu.
27. Noklikšķiniet uz Grāmatot.

## <a name="balance-and-close-advance-holders-transactions"></a>Bilances un avansa turētāju slēgšanas transakcijas
1. Dodieties uz Parādi kreditoriem > Avansa turētāji > Avansa turētāji.
2. Noklikšķiniet uz Transakcijas.
3. Aizvērt lapu.
4. Noklikšķiniet uz Bilance.
5. Noklikšķiniet uz Slēgt no bankas.
6. Atlasiet Jā laukā Automātisks.
7. Laukā Summa pārsūtīšanai. ievadiet kādu skaitli.
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Slēgt no kases.
10. Atlasiet Jā laukā Automātisks.
11. Noklikšķiniet uz OK.
12. Aizvērt lapu.
13. Noklikšķiniet uz Transakcijas.

