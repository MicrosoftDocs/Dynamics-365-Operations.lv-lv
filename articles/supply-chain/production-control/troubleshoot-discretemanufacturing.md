---
title: Problēmu novēršana saistībā ar atsevišķo ražošanu
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar atsevišķo ražošanu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b0073cb2c3e3d6b9218caf20c394c8c0ca67b796
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966209"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Problēmu novēršana saistībā ar atsevišķo ražošanu

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar atsevišķo ražošanu.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Tiek parādīts šāds kļūdas ziņojums: "pašlaik tiek izmantoti noliktavas pārvaldības procesi. Ja darba rindas vēl nav reģistrētas, varat atcelt izveidoto darbu un jebkuras noslodzes vai sūtījuma rindas un pēc tam turpināt izdošanas vai nosūtīšanas procesu."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma rodas, ja mēģināt rezervēt vai izlaist darbu rindai, bet krājuma darbības statuss ir *Izdots*, kas norāda, ka materiāls ir izdots.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai novērstu šo problēmu, izpildiet vienu no sekojošajām darbībām.

- Mainīt ražošanas pasūtījuma statusu atpakaļ uz *Prognozētu* vai *Izlaistu*.
- Atveriet lapu ar detalizētu informāciju par attiecīgās ražošanas pasūtījumu. Darbības rūtī cilnē **Noliktava**, kas atrodas grupā **Apturēt**, atlasiet opciju **Apturēt un neizdot**, lai atceltu visu izdoto darbību izdošanu. Pēc tam atlasiet **Noņemt apturēšanu**, lai apstrādātu ražošanas pasūtījumu.

Piedāvājam paskaidrojumu par funkcijām *Neizdot* un *Apturēt*:

- **Neizdot** – šī funkcija anulē krājumu darbību statusu materiālu komplekta (MK) rindās un formulas rindās, kuru statuss ir no *Izdots* *Pēc pasūtījuma*. Kad darbs ar izejmateriālu izdošanu ir pabeigts, rindu statuss ir iestatīts uz *Izdots*. Šis statuss neļauj atiestatīt ražošanas pasūtījumu uz statusu *Izveidots* . Šādā gadījumā varat izmantot funkciju *Neizdot*, lai atgrieztu darbības no statusa *Izdots* un pēc tam atiestatītu ražošanas pasūtījumu uz statusu *Izveidots*.
- **Apturēt** – šī funkcija iestata **Apturēts** karodziņu ražošanas pasūtījumā, lai nepieļautu statusa atjaunināšanu pasūtījumā. **Apturēts** karodziņu varat atrast kopsavilkuma cilnē **Noliktava** ražošanas pasūtījuma informācijas lapā.

> [!NOTE]
>
> - Pogas ir redzamas tikai tad, kad ražošanas pasūtījums tiek izveidots krājumiem, kas ir iespējoti noliktavas procesiem.
> - Grupa **Apturēt** ir redzama tikai cilnē **Noliktava**, kas atrodas ražošanas pasūtījuma informācijas lapas darbības rūtī. Tā nav redzama kopsavilkuma cilnē **Noliktava**, kas atrodas **Ražošanas pasūtījumu** saraksta lapā.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Salīdzināšanas resursa nosaukums netiek atjaunināts pēc darbinieka nosaukuma maiņas globālajā adrešu grāmatā.

### <a name="issue-description"></a>Problēmas apraksts

Ja maināt darbinieka nosaukumu globālajā adrešu grāmatā, salīdzināšanas resursa nosaukums netiek atjaunināts.

### <a name="issue-resolution"></a>Problēmas risinājums

Šis scenārijs pašlaik netiek atbalstīts. Lai labotu problēmu, ir manuāli jāatjaunina resursa nosaukums.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Veidojot jaunu ražošanas pasūtījumu, es nesaņemu šādu paziņojumu: "Vai ievietot aktīvo materiālu komplekta versiju un maršrutu?"

### <a name="issue-description"></a>Problēmas apraksts

Kad izveidojat jaunu ražošanas pasūtījumu, pēc krājuma numura ievadīšanas **Vietnes** un **Noliktavas** lauki tiek automātiski iestatīti uz noklusējuma vietu un noliktavu, kas tiek definēta lapā **Noklusējuma pasūtījuma iestatījumi** pabeigtām precēm. Turklāt aktīvais MK numurs un maršruta numurs tiek ievadīts automātiski. Netiek saņemts šāds ziņojums, kas aicina norādīt šīs vērtības:

> Vai ievietot aktīvo versiju materiālu komplektam un maršrutam?

### <a name="issue-resolution"></a>Problēmas risinājums

Netiek prasīts ievietot MK un maršrutu numurus, ja atlasāt preci, kurai vietne un noliktava ir definēta lapā **Noklusējuma pasūtījuma iestatījumi**. Jūs tiekat brīdināts tikai tad, ja šīs vērtības nav definētas atlasītajā precē.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Ražošanas pasūtījumi netiek parādīti Marķējuma lapā.

### <a name="issue-description"></a>Problēmas apraksts

Daži ražošanas pasūtījumi netiek parādīti **Marķējuma** lapā.

### <a name="issue-resolution"></a>Problēmas risinājums

Preces, kurām ir šāda konfigurācija, nav pieejamas marķēšanai. Tāpēc tie netiks parādīti **Marķējuma** lapā:

- Preces tiek definētas kā *pieļaujamā svara* veida preces.
- Tās ir iespējotas papildu noliktavas procesiem.
- Tās ir konfigurētas, lai tās kontrolētu pēc *Standarta izmaksu* principa.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Kad mēģinu pabeigt ražošanas pasūtījumu, tiek parādīts šāds kļūdas ziņojums: "Aprēķinot MK consumptionCost vērtībai jābūt negatīvai, izsniedzot no krājuma."

Šī problēma tika labota laidienā 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Kad ražošanas pasūtījuma statuss tiek mainīts no Ziņots kā pabeigts uz Beigt, tiek parādīts šāds kļūdas ziņojums: "Atjaunināt konfliktu. Standarta izmaksas nesakrīt ar finanšu krājumu vērtību pēc atjaunināšanas" un "Radās kritiska kļūda funkcijā InventCostMovement.checkVariance."

Šī problēma rodas tādēļ, ka pamatā esošos datus mainīja cits process. Process mēģinās atjaunināt datus līdz piecām reizēm. Ja konflikts pēc pieciem mēģinājumiem joprojām pastāv, tiks parādīti šādi kļūdu ziņojumi:

> Atjaunināt konfliktu. Standarta izmaksas nesakrīt ar finanšu krājumu vērtību pēc atjaunināšanas.

> Funkcijā InventCostMovement.checkVariance ir radusies kritiska kļūda.

Tas tiek darīts ar nolūku. Lai mazinātu šo problēmu, atsāciet pakešuzdevumu. Tam jāpabeidz darboties.

Ja pakešuzdevums pēc atsākšanas pastāvīgi cieš neveiksmi, pārbaudiet, vai Virsgrāmatas noklusējuma valūtas noapaļošanas precizitāte atbilst noapaļošanai, kas tiek piemērota vērtībām InventSum tabulā. Ja noapaļošanas precizitāte ir mainīta uz neatbilstošu vērtību, jums, iespējams, tā ir jāmaina uz atbilstošu vērtību. Meklēt **ModifiedDateTime**. Šādā gadījumā vērtība parasti rāda, ka noapaļošanas precizitāte nesen tika mainīta.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Izlaižot uz noliktavu, tiek parādīts šāds kļūdas ziņojums: "Krājumu RM nevarēja pilnībā rezervēt. Pārliecinieties, vai ir pieejams pilns daudzums vai rezervējiet krājumus manuāli, ja lauks Rezervācija MK rindā ir iestatīts uz Manuāli vai Sākts. Nevarēja izlaist pasūtījumu nosūtīšanai uz noliktavu, jo dažus materiālus nevarēja rezervēt." Tomēr statuss tiek atjaunināts uz Izlaists.

### <a name="issue-description"></a>Problēmas apraksts

Ja ne visi MK rindu krājumi ir fiziski pieejami, kad tiek nodots ražošanas pasūtījums, un **Izlaist uz noliktavu** politika ir iestatīta uz *Pieprasīt pilnu rezervāciju* ražošanas pasūtījumā, tiek parādīts šāds kļūdas ziņojums:

> Krājumu RM nevarēja pilnībā rezervēt. Pārliecinieties, vai ir pieejams pilns daudzums vai rezervējiet krājumus manuāli, ja lauks Rezervācija MK rindā ir iestatīts uz Manuāli vai Sākts. Nevarēja izlaist pasūtījumu nosūtīšanai uz noliktavu, jo dažus materiālus nevarēja rezervēt.

### <a name="issue-resolution"></a>Problēmas risinājums

Šī darbība ir pēc dizaina, un tā darbojas, kā paredzēts.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Kad mēģinu pabeigt ražošanas pasūtījumu un pabeigt, tiek parādīts šāds kļūdas ziņojums: "Kopējais derīgais daudzums, kas ražošanas uzdevumam ir pabeigts, būs %1. Daudzums pēdējai operācijai sastāda 0.00 kopumā."

### <a name="issue-description"></a>Problēmas apraksts

Kad ražošanas pasūtījumā mēģināt grāmatot pārskatu kā pabeigtu žurnālu, tiek parādīts šāds kļūdas ziņojums:

> Kopējais derīgais pabeigtais ražošanas daudzums būs %1. Daudzums pēdējai operācijai sastāda 0.00 kopumā.

### <a name="possible-cause"></a>Iespējamais iemesls

Šī problēma rodas, ja daudzumi, kas tika grāmatoti pēdējās operācijās, bija nepareizi. Piemēram, ja ražošana ir sākta, bet daudzums, kas ir jāuzsāk, netiek piešķirts, maršruta kartes žurnāls tiks grāmatots bez jebkādām rindām. Lai apstiprinātu situāciju, atveriet ražošanas pasūtījumu un pēc tam darbības rūtī cilnē **Skats** atlasiet **Maršruta karte**.

### <a name="workaround"></a>Kļūdas apiešanas risinājums

Šo problēmu varat novērst, grāmatojot papildu žurnālus darbībām, kurām žurnāli netika pareizi grāmatoti. Restartējiet ražošanas pasūtījumu un atlasiet, lai grāmatotu papildu žurnālus. Veicot šo darbību, ražošanas pasūtījums netiks sākts, bet tiks grāmatoti žurnāli. Pēc tam maršruta kartei ir jāparāda iegrāmatotie daudzumi un ir jābūt iespējai pabeigt ražošanas pasūtījumus veiksmīgi.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Vai var ziņot par ražošanas pasūtījumu kā pabeigtu, kad ziņoju par brāķa daudzumu, bet ne, kamēr es pārskatu laika vai materiālu daudzumu?

Nevar ziņot par brāķa daudzumu ražošanas pasūtījumā, ja arī neziņojat par derīgo daudzumu. Šis scenārijs **netiek** atbalstīts. Ja mēģināsit beigt ražošanas pasūtījumu un tiks parādīts šāds kļūdas ziņojums, pārskats par pabeigtu atjaunināšanu būs neveiksmīgs.

> Trūkst pabeigto krājumu daudzuma.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Vai var izsekot gatavo preču sērijas numurus pret patērēto preču sērijas numuriem?

Nevar izsekot gatavo preču sērijas numurus ar materiālu sērijas numuriem, ko ražošanas pasūtījums patērē, lai izveidotu šīs pabeigtās preces. Šis scenārijs pašlaik netiek atbalstīts. Risinājums ir izveidot ražošanas pasūtījumus 1 daudzumam.
