---
title: Krājumu aizturēšana
description: Šajā rakstā ir sniegts pārskats par krājuma bloķēšanu, kas ir kvalitātes pārbaudes procesa elements Supply Chain Management. Krājuma bloķēšanu var izmantot, lai nepieļautu krājumu apstrādi vai patēriņu.
author: yufeihuang
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83b5417dc24af85f09e6713f2b12fdc358f61d54
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334691"
---
# <a name="inventory-blocking"></a>Krājumu aizturēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par krājuma bloķēšanu, kas ir kvalitātes pārbaudes procesa elements Supply Chain Management. Krājuma bloķēšanu var izmantot, lai nepieļautu krājumu apstrādi vai patēriņu.

Varat bloķēt krājumu vienības tālāk norādītajos veidos.

- Manuāli
- Izveidojot kvalitātes pārbaudes pasūtījumu
- Izmantojot procesu, kas ģenerē kvalitātes pasūtījumu
- Izmantojot krājuma statusa aizturēšanu

## <a name="blocking-items-manually"></a>Manuāla krājumu aizturēšana

Varat aizturēt noteiktu krājuma daudzumu, izveidojot transakciju lapā **Krājumu aizturēšana**. Manuāli var aizturēt tikai rīcībā esošos krājumus. Attiecībā uz manuāli aizturētajiem daudzumiem jums ir jāizlemj, vai plānošanas aktivitātes ietver paredzētās ieejas plūsmas kā paredzētos rīcībā esošo daudzumu. Paredzētās ieejas plūsmas ir aizturētie krājumi, kas būs pieejami kā rīcībā esošie krājumi pēc pārbaudes pabeigšanas. Varat uzturēt paredzēto datumu. Pēc noklusējuma krājumiem, kas ir aizturēti, izmantojot kvalitātes pārbaudes pasūtījumu, ir atlasīta opcija **Plānotie ieņēmumi**. Varat atcelt manuālu aizturēšanu pēc daudzuma, dzēšot transakciju lapā **Krājumu aizturēšana**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Krājumu aizturēšana, izveidojot kvalitātes pārbaudes pasūtījumu

Var norādīt krājumus, kas ir jāpārbauda, izveidojot kvalitātes pārbaudes pasūtījumu lapā **Kvalitātes pasūtījumi**. Izveidojot kvalitātes pārbaudes pasūtījumu, tiek aizturēts norādītais krājuma daudzums. Ar kvalitātes pārbaudes pasūtījumu saistītais paraugu ņemšanas plāns nosaka tikai pārbaudāmo krājumu daudzumu, nevis aizturēto daudzumu. Kvalitātes pārbaudes pasūtījumā ievadītais daudzums ir aizturētais daudzums neatkarīgi no daudzuma, kas saskaņā ar paraugu ņemšanas plānu ir jānosūta pārbaudei.

> [!NOTE]
> Vispārējā plānošanā netiek atbalstīta gan partijas beigu datuma, gan bloķēšanas krājumu statusa funkciju izmantošana. Tas var novest pie rīcībā esošo krājumu dubultas izslēgšanas, kas var notikt vispārējās plānošanas laikā. Ieteicams paļauties uz partijas atgriešanas kodiem, nevis krājumu statusu, lai bloķētu partijas ar beigušos derīgumu.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Krājumu aizturēšana, izmantojot procesu, kas ģenerē kvalitātes pārbaudes pasūtījumu

Ja kvalitātes pārbaudes procesā ir norādīts, ka krājums ir jāpārbauda, tiek automātiski aizturēts attiecīgs krājuma daudzums. Tāpēc, kad tiek automātiski ģenerēts kvalitātes pārbaudes pasūtījums, ar kvalitātes pārbaudes pasūtījumu saistītais krājuma paraugu ņemšanas plāns nosaka gan aizturēto krājumu daudzumu, gan pārbaudāmo daudzumu. Ja lapā **Krājumu iztveršana** ir atlasīta opcija **Pilna aizturēšana**, pārbaudes laikā tiek aizturēts viss, piemēram, pirkšanas pasūtījuma daudzums neatkarīgi no krājuma paraugu ņemšanas daudzuma.

### <a name="example"></a>Piemērs

Šajā piemērā kvalitātes pārbaudes pasūtījums tiek ģenerēts, kad pirkšanas pasūtījuma pavadzīme ir iegrāmatota. Lapā **Kvalitātes piesaistes** jūs norādījāt, ka kvalitātes pārbaudes pasūtījumu aktivizē pirkšanas pasūtījuma pavadzīmes grāmatošana.

|Iestatīšana |Lietotāja darbība |Rezultāts |
|----|---|---|
| Kvalitātes saistība nosaka, ka, grāmatojot pirkšanas pasūtījuma pavadzīmi, ir jāģenerē kvalitātes pārbaudes pasūtījums. Kvalitātes pārbaudes pasūtījuma krājuma paraugu ņemšanas iestatījumi nosaka, ka ir jāpārbauda 10% no pirkšanas pasūtījuma rindā norādīta daudzuma. Turklāt, tā kā krājuma paraugu ņemšanas iestatījumos ir atlasīta opcija **Pilna aizturēšana**, pārbaudes laikā ir jāaiztur viss pirkšanas pasūtījuma rindā norādītais daudzums neatkarīgi no pārbaudei nosūtītā daudzuma. | Pavadzīme ir iegrāmatota | Kvalitātes pārbaudes pasūtījums ir izveidots. Pārbaudei tiek nosūtīti desmit procenti no krājuma pirkšanas pasūtījuma daudzuma. Viss pirkšanas pasūtījuma rindu daudzums ir bloķēts. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Krājumu aizturēšana, izmantojot krājuma statusa aizturēšanu

Varat norādīt, kuri krājumu statusi ir aizturēšanas statusi, izmantojot parametru **Krājuma bloķēšana** lapā **Krājumu statusi**. Krājumu statusus nevar izmantot kā ražošanas pasūtījumu, pārdošanas pasūtījumu, pārsūtīšanas pasūtījumu, izejošo transakciju vai projekta integrācijas aizturēšanas statusus. Izejošam darbam izmantojiet vienības, kam krājuma statuss ir Pieejams. Ja krājumu statuss ir **Bojāts** un šiem krājumiem tiek veikta vispārējā plānošana, šie krājumi tiek uzskatīti par trūkstošiem un krājumi tiek automātiski papildināti.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Uzmanieties, bloķējot krājumus, kas izmanto gan krājuma statusa aizturēšanu, gan kvalitātes pasūtījuma aizturēšanu

Varat izveidot kvalitātes pasūtījumu, kas saistīts ar krājumiem, kuriem ir krājuma statuss, kam ir iespējots **Krājumu aizturēšanas** parametrs. Šajā gadījumā kvalitātes pasūtījums izveidos papildu krājuma bloķēšanas ierakstu papildus tam, kas izveidots ar krājuma statusu. Tā kā kvalitātes pasūtījuma krājuma bloķēšanai būs iespējots parametrs **Paredzamo saņemšanu**, tas ģenerē papildu *Pasūtītā krājuma* darbību, kas arī tiek bloķēta ar tā krājumu statusu. Šī kombinācija var radīt problēmas, izprotot ģenerētās krājumu darbības nozīmes, jo tas parādīsies, it kā kopējais bloķētais daudzums pārsniegtu kopējo rīcībā esošo daudzumu. Ļauj pārbaudīt darbības, piemēram, ieejas plūsmas 10 vienības A0001 ar kvalitātes pasūtījumu, kas veidots, lai paraugs būtu 1 gabals. Uzvedība ir atkarīga arī no tā, vai opcija **Rezervēt pasūtītos krājumus** ir iespējota lapā **Krājumu un noliktavas pārvaldības parametri**.

>[!NOTE]
>Ja izmantojat krājumu statusa aizturēšanas un kvalitātes pasūtījumus kopā, ļoti ieteicams iespējot opciju **Rezervēt pasūtītos krājumus**.

### <a name="example-with-reserve-ordered-items-enabled"></a>Piemērs ar iespējotiem "Rezervēt pasūtītajiem krājumiem"

Kad ir iespējota funkcija **Rezervēt pasūtītos krājumus**, visām krājumu bloķēšanas darbībām būs statuss *Rezervēts fiziski* vai *Rezervēts pasūtījumā*.

| Krājuma darbības atsauce | Saņemšana | Izsniegt | Daudzums | Vieta | Noliktava | Krājumu statuss | Novietojums | Numura zīme | Komentārs |
|---|---|---|---|---|---|---|---|---|---|
| Pirkuma pasūtījums | Nopirkts | | 10 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | | 
| Krājumu aizturēšana | | Rezervēts fiziski | -9 gab. | 2 | 24 | Bloķēšana | | | Krājuma statusa aizturēšanas ģenerētā darbība |
| Krājumu aizturēšana | | Rezervēts fiziski | -1 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | Darbība, kas ģenerēta, bloķējot kvalitātes pasūtījumu iztveršanu |
| Krājumu aizturēšana | Pasūtīts | | 1 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | Paredzamo ieejas plūsmu no kvalitātes pasūtījuma iztveršanas bloķēšanas |
| Krājumu aizturēšana | | Rezervēts pasūtījumos | 1 gab. | 2 | 24 | Bloķēšana | | | Krājuma statusa aizturēšanas ģenerētā darbība

### <a name="example-with-reserve-ordered-items-disabled"></a>Piemērs ar atspējotiem "Rezervēt pasūtītajiem krājumiem"

Ja ir deaktivizēta funkcija **Rezervēt pasūtītos krājumus**, paredzamos ieņēmumus nevar rezervēt, jo to statuss ir *Pasūtīts*, tāpēc dažas bloķēšanas statuss tiks atstāts *Pēc pasūtījuma*.

| Krājuma darbības atsauce | Saņemšana | Izsniegt | Daudzums | Vieta | Noliktava | Krājumu statuss | Novietojums | Licences plate | Komentārs |
|---|---|---|---|---|---|---|---|---|---|
| Pirkuma pasūtījums | Nopirkts | | 10 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | |
| Krājumu aizturēšana | | Rezervēts fiziski | -9 gab. | 2 | 24 | Bloķēšana | | | Krājuma statusa aizturēšanas ģenerētā darbība |
| Krājumu aizturēšana | | Rezervēts fiziski | -1 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | Darbība, kas ģenerēta, bloķējot kvalitātes pasūtījumu iztveršanu |
| Krājumu aizturēšana | Pasūtīts | | 1 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | Paredzamo ieejas plūsmu no kvalitātes pasūtījuma iztveršanas bloķēšanas |
| Krājumu aizturēšana | | Pasūtīts | 1 gab. | 2 | 24 | Bloķēšana | RECV | receiptLp1 | Krājuma statusa aizturēšanas ģenerētā darbība

Šajos divos gadījumos ievērojiet darbības statusa un dimensiju starpību. Tāpēc ieteicams iespējot opciju **Rezervēt pasūtītos krājumus**.

## <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory"></a>Sagaidāmā saņemšana no kvalitātes pārbaudes pasūtījumiem, kas izmanto aizturēto krājumu paraugus — atspējošana

Lai vienkāršotu krājumu darbības kvalitātes pasūtījumu gadījumā, kuri krājumu paraugs ir bloķēts kā krājumu statusa sekas, sistēma nodrošina funkciju, kas deaktivizē paredzamo saņemšanu no šādiem kvalitātes pasūtījumiem. Tā kā gaidāmā saņemšana nekavējoties tiek bloķēta ar krājuma statusa bloķēšanu, šo izmaiņu dēļ rīcībā esošo krājumu samazinājums netiek samazināts.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt *šo funkcionalitāti, meklējot opciju Atspējot sagaidāmās ieejas plūsmas no kvalitātes pasūtījumiem, kuru paraugs ir bloķēts* krājumu līdzeklis līdzekļu [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="additional-resources"></a>Papildu resursi

[Izveidot un uzturēt krājuma bloķēšanu](tasks/create-maintain-inventory-blocking.md)

[Kvalitātes pārvaldības procesi](quality-management-processes.md)

[Preču kvalitātes pārbaude](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]