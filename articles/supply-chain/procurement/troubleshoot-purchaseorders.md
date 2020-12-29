---
title: Pirkšanas pasūtījumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pirkšanas pasūtījumiem.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433201"
---
# <a name="troubleshoot-purchase-orders"></a>Pirkšanas pasūtījumu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pirkšanas pasūtījumiem.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Darbību var pabeigt tikai pēc tam, kad rindas numurs ir pilnībā sadalīts.

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Kad pirkšanas pasūtījumi tiek importēti, izmantojot datu pārvaldību, pirkšanas pasūtījuma rindu numuri neseko palielinājumam, kas definēts sistēmas parametros.

### <a name="issue-description"></a>Problēmas apraksts

Pēc noklusējuma automātiski ģenerētie rindu numuri pirkšanas pasūtījuma rindām, kas tiek importētas, izmantojot datu elementu *Pirkšanas pasūtījuma rindas V2*, neizmanto sistēmas rindu numuru palielinājumu, kas norādīts sistēmas parametros. Ja manuāli izveidojat pirkšanas pasūtījumu un pievienojat rindas, izmantojot lietotāja interfeisu (UI), rindu numuri tiek palielināti pareizi. Tomēr, ja izmantojat datu pārvaldības struktūras (DMF), tie netiek pareizi palielināti.

Šī problēma rodas, ja importējat rindas, izmantojot DMF un importētajā elementā vēl nav piešķirti rindu numuri, tad sistēma izmanto DMF metodi to piešķiršanai. Šī metode vienmēr palielina rindu numurus par vienu.

### <a name="issue-workaround"></a>Problēmas aprisinājums

Pārliecinieties, lai vēlamie rindu numuri jau ir norādīti datu elementa rindu numuru laukos, kad importējat pirkšanas pasūtījuma rindas. Šādā gadījumā DMF nepārrakstīs rindu numurus.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta.

Ja izmantojat rēķina kontu, kas atšķiras no debitora konta, noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta, kad tiek izveidots pirkšanas pasūtījums.

Tas tiek darīts ar nolūku. Nodokļu grupas, termiņatlaižu un citas cenu informācijas noklusējuma vērtības ir balstītas uz debitora kontu, nevis uz rēķina kontu.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Pirkšanas pasūtījuma apstiprināšanas laikā tiek parādīts kļūdas ziņojums “Objekta atsauce nav iestatīta” vai kreditora rēķina iegrāmatošanas laikā rodas izņēmums “Izsaukšanas mērķis atgriež izņēmumu”.

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.

### <a name="issue-description"></a>Problēmas apraksts

Tiek parādīts šāds kļūdas ziņojums: “Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.”

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Vai var parādīt tikai manis izveidotos pirkšanas pasūtījumus?

Šī funkcionalitāte pašlaik nav pieejama.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Vai var rezervēt krājumus un izveidot darījumus saistībā ar pirkšanas pasūtījumā reģistrētajiem krājumiem?

### <a name="issue-description"></a>Problēmas apraksts

Pat ja vienības pirkšanas pasūtījumā ir ar stāvokli *Reģistrēts*, krājumus joprojām var rezervēt. Citiem vārdiem, varat izveidot darbības saistībā ar reģistrētajiem krājumiem.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Izveidojiet pirkšanas pasūtījumu.
2. Reģistrējiet pirkšanas pasūtījuma rindas.
3. Ievērojiet, ka varat veikt rezervācijas vai darbības saistībā ar reģistrētajiem krājumiem.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Sagaidāmais rezultāts ir reģistrēto krājumu fiziska saņemšana noliktavā vai krājumos, lai tādējādi tie būtu pieejami rezervēšanai.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Pirkšanas pasūtījumi neatspoguļo juridiskās personas valodas iestatījumus.

### <a name="issue-description"></a>Problēmas apraksts

Preces nosaukums pirkšanas pasūtījumā tiek norādīts sistēmas valodā, nevis valodā, kas iestatīta juridiskajai personai, kurai tika izveidots pirkšanas pasūtījums.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Iestatiet sistēmas valodu uz *EN-US* (ASV angļu valoda).
1. Pārliecinieties, vai pastāv prece, kam preces nosaukuma tulkošanai tiek saglabātas *EN-US* un *DE* (vācu valoda) valoda.
1. Mainiet juridiskās personas valodu uz *DE*.
1. Juridiskajai personai, kurai ir iestatīta *DE* valoda, izveidojiet pirkšanas pasūtījumu, kas ietver preci.
1. Ņemiet vērā, ka preces nosaukums joprojām ir redzams ASV angļu valodā (sistēmas valoda).

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Pirkšanas pasūtījumos prece vienmēr tiek rādīta sistēmas valodā. Pirkšanas pasūtījuma valoda tiek izmantota, kad tiek izveidots apstiprinājumu žurnāls.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Pēc preces elementa apstiprinātais piegādātāju saraksts neļauj mainīt spēkā stāšanās datumu.

### <a name="issue-description"></a>Problēmas apraksts

Precei ir apstiprināts piegādātājs, kura spēkā stāšanās datums ir, piemēram, 2018. gada 11. janvāris (*01/11/2018*) un beigu datums ir *Nekad*. Ja mēģināsit mainīt spēkā stāšanās datumu uz 2018. gada 10. janvāri (*01/10/2018*) vai 2018. gada 12. janvāri (*01/12/2018*), tiks parādīta šāda kļūda:

> Nevar izveidot ierakstu apstiprinātā piegādātāja sarakstā (PdsApproveVendorList). Vērtībai “Termiņa beigas” ir jābūt lielākai vai vienādai ar vērtību “Spēkā esošs”.

### <a name="issue-resolution"></a>Problēmas risinājums

Varat pagarināt tikai periodu, kurā piegādātājs ir apstiprināts. Ir spēkā šādi nosacījumi:

- Lai mainītu spēkā stāšanās datumu tā, ka tas ir agrāks par krājuma kreditora esošajiem ierakstiem (periodiem), jaunā perioda beigu datumam ir jābūt pirms visu esošo ierakstu beigu datumiem.
- Lai mainītu beigu datumu tā, lai tas būtu vēlāks par jebkuru no esošajiem periodiem, spēkā stāšanās datumam jābūt pēc vēlākā beigu datuma jebkurā esošajā ierakstā.
- Lai samazinātu kopējo periodu, kurā kreditors ir apstiprināts, ir jādzēš vai jāmodificē esošie ieraksti. Vai arī importēšanas laikā varat izmantot slēdzi **Saīsināt**. Šis slēdzis dzēš visus esošos ierakstus tabulā apstiprinātajiem piegādātājiem pēc krājuma.

Piemēra scenārijam, kas ir aprakstīts problēmas aprakstā, kur ierakstam ir spēkā stāšanās datums *01/11/2018* un beigu datums *Nekad*, jūs varat importēt jaunu ierakstu, kam ir spēkā stāšanās datums *01/10/2018* un beigu datums *Nekad*. Tomēr jūs nevarat samazināt periodu tā, lai spēkā stāšanās datums tiktu atjaunināts uz *01/12/2018*, izmantojot datu pārvaldību. Šīs izmaiņas jāveic, izmantojot lietotāja interfeisu.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Pēc piegādes adreses maiņas pirkšanas pasūtījuma galvenē piegādes nosaukums netiek sinhronizēts.

### <a name="issue-description"></a>Problēmas apraksts

Pirkšanas pasūtījuma galvenē norādītā adrese tiek atjaunināta uz adresi, kas nav piegādes adrese. Lai gan adrese tiek atjaunināta pirkšanas pasūtījumā, piegādes nosaukums netiek atjaunināts, pamatojoties uz atjaunināto adresi.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Atlasītā adrese ir jāklasificē kā piegādes adrese. Pretējā gadījumā piegādes nosaukums netiek atjaunināts, pamatojoties uz atlasīto adresi.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Vai ir iespējams atrast lietotāju, kurš atcēla pirkšanas pasūtījumu?

Šī informācija tiek izsekota tikai tad, ja pirkšanas pasūtījums ir pakļauts izmaiņu pārvaldībai. Ja izmantojat izmaiņu pārvaldību, jūs varat redzēt, kurš iesniedzis izmaiņas (atcelšanu) un kurš tās apstiprinājis.
