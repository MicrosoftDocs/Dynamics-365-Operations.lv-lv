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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e24c2be8a1b0da3c34919fdb44aa744f8e7fc87c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215416"
---
# <a name="posting-of-online-sales-and-payments"></a>Tiešsaistes pārdošanas un maksājumu grāmatošana

[!include [banner](../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.

Tiešsaistes pārdošanas un maksājumu grāmata ir process divos posmos.

- Tiešsaistes komercijas darījumu datu vilkšana HQ.
- Pasūtījumu sinhronizēšana, lai izveidotu pārdošanas pasūtījumus HQ.

Tiešsaistes darījumu datu vilkšanu var veikt vai nu manuāli palaižot P darbu vai izveidojot periodisku pakešuzdevumu.

### <a name="manually-running-the-p-job"></a>P darba manuāla palaišana

1. Dodieties uz Visas darbvietas > Retail un Commerce IT.
2. Noklikšķiniet uz izplatīšanas grafika.
3. Atlasiet P-0001.
4. Ja nepieciešams, pielāgojiet kanāla datu bāzu grupas.
5. Noklikšķiniet uz Izpildīt tūlīt.
6. Noklikšķiniet uz Jā.

### <a name="scheduling-a-recurring-p-job"></a>Periodiskā P darba plānošana

1. Dodieties uz Visas darbvietas > Retail un Commerce IT.
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

1. Pārejiet uz sadaļu Visas darbvietas > Veikala finanses.
2. Noklikšķiniet uz Sinhronizēt pasūtījumus.
3. Laukā Organizācijas hierarhija atlasiet Veikali pēc reģiona.
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

1. Pārejiet uz sadaļu Visas darbvietas > Veikala finanses.
2. Noklikšķiniet uz Sinhronizēt pasūtījumus.
3. Laukā Organizācijas hierarhija atlasiet Veikali pēc reģiona.
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]