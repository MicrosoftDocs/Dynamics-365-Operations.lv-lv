---
title: "Sūtījums"
description: "Šajā tēmā ir paskaidrots, kā izmantot ienākošo sūtījumu krājumu procesus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 01ab473951bc04c68a0248b37041a116eebcaea9
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="consignment"></a>Sūtījums

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā izmantot ienākošo sūtījumu krājumu procesus.

Sūtījuma krājumi ir krājumi, kas pieder kreditoram, bet tiek glabāti jūsu bāzes vietā. Kad esat gatavs patērēt vai izmantot krājumu, jūs pārņemat krājuma īpašumtiesības. Šajā tēmā ir ietverta informācija par to, kā fiziski saņemt krājumus, kas ir kreditora īpašumā, neveidojot virsgrāmatas transakcijas, kā sākt ražošanas procesu, kad krājumus, kas ir kreditora īpašumā, var fiziski rezervēt, un kā mainīt izejmateriālu īpašumtiesības, lai patēriņu spētu apstrādāt kā daļu no ražošanas pasūtījuma apstrādes. Ir arī informācija par to, kā kreditori var pārraudzīt to krājumu patēriņu, izmantojot kreditoru sadarbības interfeisu. Papildinformāciju par to, kā iespējot un konfigurēt ienākošo sūtījumu procesus, skatiet [Sūtījuma iestatīšana](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Sūtījuma procesa pārskats
Šajā piemēra scenārijā uzņēmumam USMF ir sūtījuma līgums ar kreditoru US-104 par izejmateriālu M9211CI.

1.  Sūtījuma papildināšanas pasūtījums tiek veidots manuāli USMF, pamatojoties uz paredzamo pieprasījumu. Pasūtījums tiek veidots kreditoram US-104, un krājumam MS9211CI tiek pievienota rinda.
2.  Kreditors tiek informēts par paredzamo piegādi. Tas var notikt vienā no trim veidiem:
    -   Kāds, kurš strādā USMF, nosūtīta pasūtījuma informāciju kreditoram.
    -   Kreditors var pārraudzīt paredzamos rīcībā esošos krājumus, izmantojot kreditoru sadarbības interfeisu.
    -   Kāds, kurš strādā USMF, filtrē datus lapā **Rīcībā esošie krājumi**, lai parādītu kreditoram US-104 tikai tos ierakstus, kuru saņemšanas statuss ir **Pasūtīts**, un tad nosūta šo informāciju kreditoram.

3.  Krājumi tiek piegādāti no US-104 uz USMF.
4.  Kad materiāli nonāk USMF, sūtījuma papildināšanas pasūtījums tiek atjaunināts ar produktu ieejas plūsmu. Tiek ierakstīti tikai kreditora īpašumā esošu krājumu fiziskie daudzumi. Netiek izveidota neviena virsgrāmatas darbība, jo krājumi joprojām pieder kreditoram.
5.  Kreditors uzrauga atjauninājumus fiziski rīcībā esošiem krājumus, izmantojot lapu **Rīcībā esošie sūtījuma krājumi**.
6.  Kad fiziskie krājumi ir rīcībā esoši, ražošanas process rezervē kreditora īpašumā esošos krājumus, un sāk gatavo preču ražošanas pasūtījumu, kas patērēs izejmateriālu M9211CI.
7.  Rezervēto izejmateriālu, kas būs jāpatērē ražošanā, īpašnieks tiek mainīts no US-104 uz USMF. Tas tiek darīts, izmantojot Krājumu īpašumtiesību maiņas žurnālu. Šis process izveido pirkšanas pasūtījumus, kur lauks **Izcelsme** ir iestatīts uz **Sūtījums**.
8.  Kreditors uzrauga patēriņu (īpašumtiesību maiņa) lapā **No sūtījuma krājumiem saņemtās preces**, un izraksta rēķinu, balstoties uz līgumiem starp diviem uzņēmumiem.
9.  Ražošanas process patērē izejmateriālu, izmantojot ražošanas izdošanas sarakstu. Fiziskā rezervācija tiek automātiski atjaunināta, lai atspoguļotu, ka rīcībā esošie krājumi pieder USMF.
10. Rēķins no US-104 tiek apstrādāts, salīdzinot ar pirkšanas pasūtījumiem, kas tika automātiski ģenerēti, apstrādājot krājumu īpašumtiesību izmaiņu žurnālu. Maksājums tika veikts kreditoram US-104 par krājumu, kas tika patērēts.

USMF veic papildu periodiskus procesus:

-   Starp dažādām noliktavām kreditora īpašumā esošu krājumu fiziska kustība tiek apstrādāta, izmantojot pārsūtīšanas žurnālu.
-   Fiziski rīcībā esošais krājums tiek atjaunināts, izmantojot žurnālu **Inventarizācijas**. Kreditors var izmantot inventarizāciju, lai atjaunotu rīcībā esošos krājumus, ja ir atļauja to darīt.

Kreditors US-104 var pārraudzīt atjauninājumus, izmantojot lapu **Rīcībā esošie sūtījuma krājumi**.

## <a name="consignment-replenishment-orders"></a>Sūtījuma papildināšanas pasūtījumi
Sūtījuma papildināšanas pasūtījums ir dokuments, kas tiek izmantots, lai pieprasītu un sekotu līdzi produktu krājumu daudzumiem, ko kreditors plāno piegādāt noteiktā datumu intervālā, izveidojot pasūtīto krājumu darbības. Parasti tas tiks balstīts uz prognozi un konkrēto produktu faktisko pieprasījumu. Krājumu, kas tiks saņemts atbilstoši sūtījuma papildināšanas pasūtījumam, paliek kreditora īpašumā. Tiek ierakstītas tikai rīcībā esošas preces, kas attiecas uz fiziskās ieejas plūsmas atjaunināšanu, tādēļ notiek virsgrāmatas darbību grāmatošana. Dimensija **Īpašnieks** tiek izmantota, lai atdalītu informāciju par krājumu, kas pieder kreditoram, un kas pieder saņēmēja juridiskajai personai. Kamēr pilnais rindu daudzums nav bijis saņemts vai atcelts, sūtījuma papildināšanas pasūtījuma rindām ir statuss **Atvērts pasūtījums**. Kad pilnais daudzums ir saņemts vai atcelts, statuss tiek mainīts uz **Pabeigts**. Fizisko rīcībā esošo krājumu, kas ir saistīts ar sūtījuma papildināšanas pasūtījumu var ierakstīt, izmantojot Reģistrācijas procesu, kā arī Produktu ieejas plūsmas atjaunināšanas procesu. Reģistrāciju var veikt kā daļu no krājumu saņemšanas procesa, vai manuāli atjauninot pasūtījuma rindas. Ja tiek izmantots Produktu ieejas plūsmas atjaunināšanas process, produktu ieejas plūsmas žurnālā tiek veikts ieraksts, ko var izmantot, lai kreditoriem apstiprinātu preču saņemšanu. 

[![consignment-replenishment-order](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Krājumu īpašumtiesību izmaiņu žurnāls
Krājumu īpašumtiesību izmaiņu žurnāls tiek izmantots, lai mainītu krājumu īpašnieku no kreditora uz saņemošo juridisko personu. Netiek izveidotas nekādas paredzētās krājumu darbības žurnālam. Ņemiet vērā, ka tiek izveidotas tikai krājumu darbības, kas ir saistītas ar grāmatoto žurnālu. Kad tiek grāmatots žurnāls?

-   Kreditora īpašumā esošie krājumi tiek izsniegti, izmantojot atsauci **Īpašumtiesību izmaiņa** ar statusu **Pārdots**.
-   Rīcībā esošus krājumus saņem juridiska persona, kas tos patērē, izmantojot produktu ieejas plūsmas atjaunināto krājumu darbību pirkšanas pasūtījumā. Tas iestata pasūtījuma statusu uz **Saņemts**. Pirkšanas pasūtījumiem, kas tiek izmantoti sūtījumam, lauks **Izcelsme** ir iestatīts uz **Sūtījums**.

Pēc pasūtījuma rindas izveidošanas nav iespējams atjaunināt sūtījuma pirkšanas pasūtījuma rindu daudzumu. 

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Kreditora sadarbība sūtījuma procesos
Kreditora sadarbības interfeisā ir trīs lapas, kas ir saistītas ar ienākošā sūtījuma procesu:

-   **Pirkšanas pasūtījumi,** **kas patērē sūtījuma krājumu** — rāda detalizētu pirkšanas pasūtījuma informāciju, kas attiecas uz īpašumtiesību maiņu no sūtījuma procesa.
-   **No sūtījuma krājumiem saņemtās preces** - rāda informāciju par krājumiem un daudzumiem, kuru produktu ieejas plūsmas tika atjauninātas, īpašumtiesības izmaiņas procesa laikā.
-   **Rīcībā esošie sūtījuma krājumi** - rāda informāciju par sūtījuma krājumiem, kurus paredzēts piegādāt, un krājumus, kas jau fiziski ir pieejami debitora vietā.





