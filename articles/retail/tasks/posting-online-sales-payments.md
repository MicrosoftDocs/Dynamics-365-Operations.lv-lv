---
title: Tiešsaistes pārdošanas un maksājumu grāmatošana
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864157"
---
# <a name="posting-of-online-sales-and-payments"></a>Tiešsaistes pārdošanas un maksājumu grāmatošana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.

Tiešsaistes pārdošanas un maksājumu grāmata ir process divos posmos.

- Tiešsaistes mazumtirdzniecības darījumu datu vilkšana HQ.
- Pasūtījumu sinhronizēšana, lai izveidotu pārdošanas pasūtījumus HQ.

Tiešsaistes mazumtirdzniecības darījumu datu vilkšanu var veikt vai nu manuāli palaižot P darbu vai izveidojot periodisku pakešuzdevumu.

### <a name="manually-running-the-p-job"></a>P darba manuāla palaišana

1. Dodieties uz Visas darbvietas > Mazumtirdzniecības IT.
2. Noklikšķiniet uz izplatīšanas grafika.
3. Atlasiet P-0001.
4. Ja nepieciešams, pielāgojiet kanāla datu bāzu grupas.
5. Noklikšķiniet uz Izpildīt tūlīt.
6. Noklikšķiniet uz Jā.

### <a name="scheduling-a-recurring-p-job"></a>Periodiskā P darba plānošana

1. Dodieties uz Visas darbvietas > Mazumtirdzniecības IT.
2. Noklikšķiniet uz izplatīšanas grafika.
3. Atlasiet P-0001.
4. Noklikšķiniet uz Izveidot pakešuzdevumu.
5. Noklikšķiniet uz Palaist fonā.
5. Iespējojiet pakešapstrādi.
6. Noklikšķiniet uz Periodiskums..
7. Atlasiet opciju Bez beigu datuma.
8. Laukā Skaits ievadiet intervālu starp izpildēm, izteiktu minūtēs. Parasti tās būtu 5-10.
9. Noklikšķiniet uz Labi.
10. Noklikšķiniet uz Labi.

Pasūtījumus var sinhronizēt vai nu manuāli palaižot darbu "Sinhronizēt pasūtījumus" vai izveidojot periodisku pakešuzdevumu.

### <a name="manually-running-order-synchronization"></a>Pasūtījuma sinhronizācijas manuāla palaišana 

Veiciet šīs darbības, lai vienreiz manuāli palaistu darbu "Sinhronizēt pasūtījumus".

1. Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.
2. Noklikšķiniet uz Sinhronizēt pasūtījumus.
3. Laukā Organizācijas hierarhija atlasiet Mazumtirdzniecības veikali pēc reģiona.
    * Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.  
    * Noklikšķiniet uz bultiņas, lai pievienotu atlasi.  
4. Noklikšķiniet uz cilnes Palaist fonā.
5. Atspējojiet pakešapstrādi.
6. Noklikšķiniet uz Periodiskums.
7. Atlasiet opciju Beidzas pēc
8. Laukā Beidzas pēc, ievadiet 1.
9. Noklikšķiniet uz Labi.
10. Noklikšķiniet uz Labi.

### <a name="scheduling-recurring-order-synchronization"></a>Periodiskas pasūtījuma sinhronizācijas plānošana

Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.
2. Noklikšķiniet uz Sinhronizēt pasūtījumus.
3. Laukā Organizācijas hierarhija atlasiet Mazumtirdzniecības veikali pēc reģiona.
    * Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.  
    * Noklikšķiniet uz bultiņas, lai pievienotu atlasi.  
4. Noklikšķiniet uz cilnes Palaist fonā.
5. Iespējojiet pakešapstrādi
6. Noklikšķiniet uz Periodiskums.
7. Atlasiet opciju Bez beigu datuma.
8. Laukā Skaits ievadiet intervālu starp izpildēm, izteiktu minūtēs. Parasti tās būtu 2-20
9. Noklikšķiniet uz Labi.
10. Noklikšķiniet uz Labi.

## <a name="data-entities-involved-in-the-process"></a>Procesā iesaistītie datu elementi

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
