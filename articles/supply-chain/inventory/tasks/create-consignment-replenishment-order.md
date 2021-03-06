---
title: Sūtījuma papildināšanas pasūtījuma izveide
description: Šajā tēmā aprakstīts, kā izveidot sūtījuma papildināšanas pasūtījumu, kur varat izsekot paredzamo piegādi no piegādātāja jūsu sūtījumu krājumos.
author: sherry-zheng
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d2030277e0810bebef9356136b0e11effc6d5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834029"
---
# <a name="create-a-consignment-replenishment-order"></a>Sūtījuma papildināšanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot sūtījuma papildināšanas pasūtījumu, kur varat izsekot paredzamo piegādi no piegādātāja jūsu sūtījumu krājumos. Tajā ir arī parādīts kā reģistrēt preču saņemšanu, lai sūtījumu krājums ir reģistrēts kā rīcībā esošos krājums, kas pieder kreditoram. Šo procedūru parasti veic sagādes speciālists. Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

## <a name="create-a-consignment-replenishment-order"></a>Sūtījuma papildināšanas pasūtījuma izveide
1. Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Sūtījums > Sūtījuma papildināšanas pasūtījums**.
2. Atlasiet **Jauns**.
3. Laukā **Piegādātāja konts** atlasiet piegādātāju **US-104** (jums jāizvēlas piegādātājs, kas ir reģistrēts kā īpašnieks lapā **krājumu īpašnieki** ). 
4. Atlasiet **Labi**.
5. Atlasiet **Pievienot rindu**.
6. Laukā **Vienuma numurs** ierakstiet `M9211CI` (jums ir jāatlasa vienums, kas iestatīts sūtījuma krājumam).
7. Laukā **Daudzums** ierakstiet kādu skaitli.
8. Laukā **Pieprasītais piegādes datums** ievadiet datumu. Pieprasītos un apstiprinātos datumus izmanto MRP programma preču saņemšanas paredzēšanai.  
9. Laukā **Apstiprinātais piegādes datums** ievadiet datumu.
10. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
11. Atlasiet cilni **Krājumu izmēri**.
12. Lai parādītu īpašnieku laukā **Krājumu izmēru īpašnieks**, atsvaidziniet lapu. Kreditors US-104 tagad ir norādīts kā īpašnieks.  

## <a name="check-the-inventory-transaction-status"></a>Pārbaudiet krājumu darbības statusu
1. Atlasiet **Krājumi**.
2. Atlasiet **Darbības**.
3. Vajadzīgajā rindā ņemiet vērā, ka lauks **Saņemšana** ir iestatīts kā **Pasūtīts**.  
4. Aizvērt lapu.

## <a name="receive-items"></a>Saņemt krājumus
1. Atlasiet **Preču ieejas plūsma**.
2. Laukā **Ārējā produkta saņemšana** ierakstiet vērtību.
3. Laukā **Daudzums** ievadiet skaitli, kas mazāks par tur parādīto skaitli. 
4. Atlasiet **Labi**.

## <a name="check-the-on-hand-inventory"></a>Pārbaudiet rīcībā esošo krājumu
1. Atlasiet **Krājumi**.
2. Atlasiet **Rīcībā**.
3. Atlasiet **Pārskats**. Krājumus, kas tika saņemti kā sūtījumu krājumi, kas pieder kreditoram, ir pieejami rīcībā esoši. Sūtījuma papildināšanas pasūtījuma atlikušais daudzums tiek rādīts laukā **Pasūtīts pavisam**.  
4. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]