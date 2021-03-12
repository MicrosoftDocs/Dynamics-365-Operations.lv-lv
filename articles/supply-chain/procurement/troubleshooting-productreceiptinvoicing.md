---
title: Produktu ieejas plūsmu un rēķinu izrakstīšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar produktu ieejas plūsmām un rēķinu izrakstīšanu.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999057"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Produktu ieejas plūsmu un rēķinu izrakstīšanas problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar produktu ieejas plūsmām un rēķinu izrakstīšanu.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Nevar grāmatot vairāk par vienu rēķinu pirkšanas pasūtījuma rindai ar kategorijām atbilstošajiem krājumiem.

Grāmatojot rēķinus, daudzums ir obligāts. Tāpēc, ja pilnam rindas daudzumam ir izrakstīts rēķins par tikai daļēju summu, jūs nevarēsit izrakstīt rēķinu atlikušajai summai citā rēķinā.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Pirkšanas pasūtījuma apstiprināšanas laikā tiek parādīts kļūdas ziņojums “Objekta atsauce nav iestatīta” vai kreditora rēķina iegrāmatošanas laikā rodas izņēmums “Izsaukšanas mērķis atgriež izņēmumu”.

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā.

Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā, ja dažādām produktu ieejas plūsmu rindām ir dažādi uzskaites datumi.

Iepriekšējās Microsoft Dynamics 365 Supply Chain Management versijās šajā situācijā konsolidācija tika atļauta. Tomēr praksē pastāv nosliece uz kļūdu. Izveidotais pirkšanas pasūtījuma rindu uzskaites datums nedrīkst atšķirties no uzskaites datuma produktu ieejas plūsmas rindās, no kurām tika izveidotas šīs pirkšanas pasūtījuma rindas. (Pirkšanas pasūtījuma rindu uzskaites datums atbilst uzskaites datumam pirkšanas pasūtījuma galvenē.) Tāpēc vairāku produktu ieejas plūsmu konsolidēšana vienā pirkšanas pasūtījumā vairs netiek atļauta.

Uzskaites datums tiek izmantots, piemēram, budžeta rezervācijām un apgrūtinājumam. Tāpēc tas jāsaglabā pārejas periodā no produktu ieejas plūsmas uz pirkšanas pasūtījumu.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Kad produktu ieejas plūsmas ir atceltas, darījumus var grāmatot aizturētajā Virsgrāmatas kontā.

### <a name="issue-description"></a>Problēmas apraksts

Ja produktu ieejas plūsma ir atcelta, sistēma ļauj grāmatot darījumus aizturētajos Virsgrāmatas kontos, pat ja galvenie konti ir aizturēti.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Lapā **Kreditoru parametri** cilnē **Vispārīgi** pārliecinieties, vai opcija **Grāmatot produktu ieejas plūsmu Virsgrāmatā** ir iestatīta uz *Jā*.
1. Izveidojiet pirkšanas pasūtījumu un pievienojiet pasūtījuma rindu, kurā preces daudzums ir *1 000*.
1. Apstipriniet pirkšanas pasūtījumu.
1. Grāmatojiet produktu ieejas plūsmu un pārbaudiet dokumentus.
1. Aizturiet attiecīgos galvenos kontus, *200140* un *140200*.
1. Atceliet grāmatoto produktu ieejas plūsmu.
1. Ievērojiet, ka darījumus var grāmatot aizturētajos Virsgrāmatas kontos.

### <a name="issue-resolution"></a>Problēmas risinājums

Darījumus var grāmatot aizturētajos Virsgrāmatas kontos, kad produktu ieejas plūsmas ir atceltas, jo šī darbība ļauj labot grāmatojumus.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja nav izveidots finanšu dokuments produktu ieejas plūsmas laikā.

Ja krājumu modeļu grupu opcija **Uzkrāt saistības produktu ieejas plūsmā** ir iestatīta uz *Nē*, grāmatošana Virsgrāmatā netiks veikta. Tomēr fizisks notikums tiks ierakstīts, lai veiktu uzskaiti apakšgrāmatā, un šim notikumam nepieciešams dokumenta numurs. Šis dokumenta numurs ir dokumenta numurs, uz kuru ir atsauce krājumu darījumā.

Ieteicams iestatīt opciju **Uzkrāt saistības produktu ieejas plūsmā** uz *Jā*, kā aprakstīts šajā emuāra ierakstā: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Virsgrāmatas iestatījumā nav ieslēgta Grāmatošana izmaksu kontā.

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
1. Cilnē **Rēķins** iestatiet opciju **Grāmatot Virsgrāmatas izmaksu kontā** uz *Jā*.
1. Doties uz **Krājumu vadība \> Iestatīšana \> Grāmatojums \> Grāmatošana**.
1. Cilnē **Pirkšanas pasūtījums** pārliecinieties, vai visas preces pirkšanas izdevumu rindas ir izdzēstas.
1. Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Izveidojiet pirkšanas pasūtījumu. Laukā **Kreditora konts** atlasiet *1001 Acme Office Supplies*.
1. Pievienojiet pirkšanas pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *D0011 Laser Projector*
    - **Vieta:** *1*
    - **Noliktava:** *11*
    - **Daudzums:** *4*

1. Darbību rūts cilnē **Pirkšana**, grupā **Darbība** atlasiet **Apstiprināt**.
1. Darbību rūtī cilnes **Saņemt** grupā **Ģenerēt**, atlasiet **Produktu ieejas plūsma**.
1. Dialoglodziņā **Produktu ieejas plūsmas grāmatošana** laukā **Produktu ieejas plūsma**, ievadiet patvaļīgu numuru un pēc tam atlasiet **Labi**.
1. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
1. Laukā **Numurs** ievadiet patvaļīgu numuru kā rēķina numuru.
1. Atjauniniet atbilstības statusu un grāmatojiet.
1. Ievērojiet, ka tagad, ģenerējot rēķinu no pirkšanas pasūtījuma, tiek parādīta šāda kļūda: “Konta numurs darbības veidam Preces pirkšanas izdevumi nepastāv.”

### <a name="issue-resolution"></a>Problēmas risinājums

Tas ir atkarīgs no rēķinu un rēķinu grupu parametru iestatījumiem. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas izmaksu un krājumu izmaiņu uzskaite](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
