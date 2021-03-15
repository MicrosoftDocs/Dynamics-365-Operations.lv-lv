---
title: Kalendāri un vispārējā plānošana
description: Šajā tēmā ir sniegts pārskats par piegādes ķēdes kalendāriem un to, kā tie ietekmē vispārējo plānošanu.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bbbd60ddfd46904374a2cf3ad4a09f96805bd2bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001803"
---
# <a name="calendars-and-master-planning"></a>Kalendāri un vispārējā plānošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par piegādes ķēdes kalendāriem un to, kā tie ietekmē vispārējo plānošanu.  Ir sniegti paskaidrojumi par dažādiem kalendāriem, ko izmanto vispārējās plānošanas programmā, tostarp, kā tie ietekmē nosūtīšanas un saņemšanas datumus plānotajos pasūtījumos. Visbeidzot, ir sniegti ieteikumi par kalendāru piešķiršanu, izmantošanu un atjaunināšanu.

## <a name="definition-of-a-calendar"></a>Kalendāra definēšana

Varat definēt kalendāru, kas tiks izmantots jūsu organizācijā, lapā **Organizācijas administrēšana > Iestatījumi > Kalendāri > Kalendāri**. 

Katrs datuma ieraksts kalendārā var būt **atvērts** vai **slēgts**, vai **pamatkalendāra**. Tas ir noteikts lapas **Darba laiki** kolonnā **Kontrole**. Katram datumam: 
- **Atvērts** — norāda, ka atlasītajā dienā tiek veikts darbs. Kalendārs tiks atjaunināts saskaņā ar darba laika veidni.
- **Slēgts** — norāda, ka attiecīgajā dienā darbs netiek veikts. 
- **Pamatkalendāra** — norāda, ka konkrētajā datumā tiks pārmantoti darba laiki un iestatījums “atvērts/slēgts” no pamatkalendāra. Tādēļ, kad pamatkalendārs tiek atjaunināts, atlasītais kalendārs pārmantos darbības laikus no tā. 

Datumiem, kuriem atlasīts iestatījums Slēgts, automātiski tiks piešķirta izvēles rūtiņa **Slēgts izsniegšanai**. Datumiem, kuriem atlasīts iestatījums Atvērts, varat manuāli atlasīt opciju **Slēgts izsniegšanai**. Tas norāda, ka attiecīgajā datumā tiek veikts darbs, bet netiek veikta nosūtīšana. 

## <a name="calendars-that-affect-master-planning"></a>Kalendāri, kas ietekmē vispārējo plānošanu

### <a name="calendar-for-a-coverage-group"></a>Kalendārs vajadzības grupai
Vajadzības grupa norāda kopīgu parametru kopumu, kas tiek izmantots, lai papildinātu krājumus, kas pieder noteiktai vajadzības grupai. 

Lai pievienotu kalendāru vajadzības grupai, atveriet sadaļu **Vispārējā plānošana > Iestatījumi > Vajadzība > Vajadzības grupas**. Atrodiet vajadzības grupu, kurai vēlaties piešķirt kalendāru, un pēc tam atlasiet to laukā **Kalendārs**.

Vajadzības grupu var piešķirt dažādās lapās: 
    - Krājuma lapā **Detalizēta informācija par izlaistajām precēm**. Lai skatītu krājuma vajadzības grupu, atveriet sadaļu **Preču informācijas pārvaldība > Preces > Izlaistās preces** un atlasiet krājumu, lai dotos uz lapu **Detalizēta informācija par izlaistajām precēm**. Krājuma vajadzības grupu var redzēt kopsavilkuma cilnē **Plāns**.
    - Lapā **Krājumu vajadzība**. Lapā Detalizēta informācija par izlaistajām precēm noklikšķiniet uz **Krājumu vajadzība**, lai atvērtu lapu Krājumu vajadzība. Pārskata cilnē var redzēt dažādus papildināšanas parametrus atkarībā no vietas, noliktavas un preču dimensijām. Vajadzības grupa katram krājumam tiks pārmantota no vajadzības grupas lapā **Detalizēta informācija par izlaistajām precēm**. To var ignorēt, izmantojot vienumu **Lietot noteiktus iestatījumus** vai **Ignorēt grupas iestatījums** cilnē **Vispārīgi**.
    - Lapā **Vispārējās plānošanas parametri**. Ja krājumam iepriekšējās lappusēs nav iestatīta vajadzības grupa, vispārējai plānošanai tiks izmantota vispārējā vajadzības grupa, kas iestatīta vispārējās plānošanas parametros. Tas tiek iestatīts sadaļas **Vispārējā plānošana > Iestatījumi > Vispārējās plānošanas parametri** laukā **Vispārējā vajadzības grupa**. 

### <a name="calendar-for-a-vendor"></a>Kalendārs kreditoram
Lai norādītu kreditora darbdienas, kreditoram var piešķirt pirkšanas kalendāru kreditora lapā **Pirkšanas pasūtījuma noklusējuma informācija**. 

Lai iestatītu kalendāru kreditoram, ir jāizveido kalendārs sadaļā **Organizācijas administrēšana > Kalendāri > Kalendāri**. Kad kalendārs ir izveidots, tas ir jāpiešķir kreditoram. Atveriet sadaļu **Parādi kreditoriem > Kreditori > Visi kreditori** un atlasiet kreditoru, kuram vēlaties piešķirt kalendāru. Pēc tam kreditora lapā, kopsavilkuma cilnē **Pirkšanas pasūtījuma noklusējuma informācija** piešķiriet jaunu pirkšanas kalendāru, izmantojot nolaižamo izvēlni. 

Kalendārā kreditoram ir norādītas dienas, kurās tie pieņem pirkšanas pasūtījumu iesniegšanu, un datumi, kad tie var piegādāt pasūtījumus jūsu uzņēmumam. Tādēļ pasūtījumu datumi pirkšanas pasūtījumiem kreditoram ar pirkšanas kalendāru būs datumi, kas kalendārā ir iestatīti kā atvērti. Piegādes datumi šiem pasūtījumiem arī būs atvērtajās dienas un tādējādi ietekmēs nopirktā krājuma izpildes laiku. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Nopirktā krājuma izpildes laika noteikšana

Lai norādītu krājuma pirkšanas izpildes laiku (un to, vai jāņem vērā tikai darbdienas) krājumam, ir jāatver preces pasūtījuma noklusēto iestatījumu lapa, kas atrodas sadaļā **Preču informācijas pārvaldība > Preces > Izlaistās preces**, un jāatlasa **Pasūtījuma noklusējuma iestatījumi**. 

> [!Note]
> **Darbdienas** zem pirkšanas izpildes laika norāda kreditora darbdienas. Piemēram, kalendārs piegādei tikai otrdienās ar izpildes laiku 10 dienas un atlasītu darbdienu izvēles rūtiņu norāda, ka krājuma piegādei būs nepieciešamas 10 nedēļas (10 otrdienas).
Tādējādi lielākajā daļā gadījumu nav ieteicams izvēlēties darbdienas pirkšanas pasūtījumu izpildes laikam.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Izpildes laiku noteikšana tirdzniecības līgumu lapā

Vispārējo plānošanu var iestatīt, lai tiktu iekļauti visi kreditoru tirdzniecības līgumi. Tirdzniecības līgumi ir fiksētas cenas vai atlaižu līgumi, kas ir iestatīti vienam vai vairākiem debitoriem vai kreditoriem atsevišķu vai vairāku preču pārdošanai vai pirkšanai. Atveriet sadaļu **Vispārējā plānošana > Iestatījumi > Vispārējās plānošanas parametri** un cilnē **Plānotie pasūtījumi** atlasiet **Meklēt tirdzniecības līgumus**, lai iekļautu tirdzniecības līgumus, veicot plānošanu. Vispārējā plānošana var atlasīt kreditoru ar vērtību **Minimālais izpildes laiks** vai **Zemākā vienības cena**.

### <a name="calendar-for-a-warehouse"></a>Kalendārs noliktavai
Noliktavai var piešķirt kalendāru, lai norādītu atvērtus saņemšanas un nosūtīšanas datumus. Ja noliktavai nav piešķirts kalendārs, tiek pieņemts, ka tā ir atvērta visos datumos. 

> [!Note]
> Kalendāra piešķiršana tranzīta noliktavai nerada nekādu ietekmi. Tranzīta noliktavas izmanto pārsūtīšanas pasūtījumu atbalstam. Atbilstīgos nosūtīšanas vai saņemšanas datumus pasūtījumiem nosaka atvērtās dienas nosūtīšanas noliktavas un saņemšanas noliktavas, kā arī piegādes veida kalendārā.

#### <a name="closed-for-pickup-policy"></a>Politika attiecībā uz slēgšanu izsniegšanai
Lai norādītu, ka noliktava ir atvērta saņemšanai, bet izsniegšana nav iespējama, var izmantot vienumu **Politika attiecībā uz slēgšanu izsniegšanai** noliktavas kalendārā. Tas attiecas arī uz izsniegšanu debitoriem. 

### <a name="transport-calendar"></a>Transportēšanas kalendārs 
Lai norādītu datumus, kas pieejami pārsūtīšanas pasūtījumiem no noliktavas, kas norādīta laukā **No noliktavas**, var piešķirt kalendāru laukā **Transportēšanas kalendārs**. Var iestatīt transportēšanas kalendāru katram piegādes veidam vai katram piegādes veidam un nosūtīšanas noliktavai. Transportēšanas kalendāru iestata sadaļā **Pārdošana un mārketings > Iestatījumi > Sadale > Piegādes veidi**. Atlasiet piegādes veidu un noklikšķiniet uz pogas **Transportēšanas kalendārs**.

Var izveidot rindu katrai noliktavai un katram piegādes veidam, ja kalendārs ir pievienots kolonnā **Transportēšanas kalendārs**. Tiks norādīts transportēšanas kalendārs, kas tiks lietots, kad preces tiks sūtītas no noliktavas, izmantojot attiecīgo piegādes veidu. Lai lietotu transportēšanas kalendāru visiem sūtījumiem, kuriem tiek izmantots attiecīgais piegādes veids, rindu var izveidot, nenorādot noliktavu.  Tas ietekmēs visus sūtījumus, kuriem tiek izmantots attiecīgais piegādes veids, neatkarīgi no noliktavas. 

Ja nav piešķirts transportēšanas kalendārs, tiek pieņemts, ka transportēšanai ir atvērti visi datumi.

### <a name="calendar-for-a-customer"></a>Kalendārs debitoram
Lai norādītu datumus, kad debitors var saņemt piegādes, debitoram var piešķirt saņemšanas kalendāru. Ja debitoram nav piešķirts neviens kalendārs, tiek pieņemts, ka debitors var saņemt pasūtījumu visos datumos. Tas ietekmēs saņemšanas datumu pārdošanas pasūtījuma rindās. Ja atlasāt datumu pārdošanas pasūtījuma rindās, kas nav iestatīts kā “atvērts” debitora kalendārā, sistēma norādīs, ka saņemšanas datums nav derīgs. 

Ņemiet vērā, ka var iekļaut tikai vienu kalendāru katram debitoram. Ja nepieciešams ietvert kalendāru katrai no vairākām debitora adresēm, var izveidot vienu debitoru katrai adresei un pēc tam piešķirt attiecīgo kalendāru. 

Pieprasīto saņemšanas datumu pārdošanas pasūtījuma rindās ietekmē debitora kalendārs un piegādes datuma kontroles metode. Informāciju par to, kā tiek aprēķināts agrākais piegādes datums, varat izlasīt sadaļā [Pasūtījumu solīšana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Nosūtīšanas kalendārs juridiskai personai
Lai norādītu datumus, kuros juridiskā persona var nosūtīt preces, varat iestatīt nosūtīšanas kalendāru sadaļā **Organizācijas administrēšana > Organizācijas > Juridiskas personas**. Atlasiet juridisko personu un pievienojiet kalendāru cilnes **Starptautiskā tirdzniecība un loģistika** laukā **Nosūtīšanas kalendārs**. Nosūtīšanas kalendārs darbosies kā noklusējuma iestatījumu avots visiem juridiskās personas noliktavas kalendāriem. 

## <a name="how-calendars-affect-dates-in-planning"></a>Kā kalendāri ietekmē datumus plānošanā

### <a name="order-date-of-a-planned-purchase-order"></a>Pasūtījuma datums plānotajam pirkšanas pasūtījumam 
Pasūtījuma datums plānotajā pirkšanas pasūtījumā norāda datumu, kad veikts pasūtījums. Tas būs atvērts datums gan kreditora kalendārā, gan vajadzības grupas kalendārā. Dažreiz kreditoriem ir nepieciešama dažu dienu rezerve starp datumu, kad tie saņem pirkšanas pasūtījumu, un datumu, kad tie var nosūtīt preces. Šie datumi tiek norādīti kreditora rezerves dienās. Tomēr, ja nopirktais krājums tiek piešķirts vajadzības grupai ar rezerves dienām, šīs rezerves dienas pārlabos kreditora rezerves dienas.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Piegādes datums plānotajam pirkšanas pasūtījumam
Pirkuma saņemšanas datums norāda datumu, kad saņemsit preces. Tas būs atvērts datums kalendārā. Tālāk ir minēti kalendāri (secībā no augstākās līdz zemākajai prioritātei), kas tiks ņemti vērā, lai norādītu, kurās dienas var saņemt pirkšanas pasūtījumu: 
1. Kreditora kalendārs
1. Vajadzības grupas kalendārs
1. Noliktavas kalendārs saņēmējai noliktavai

Ņemiet vērā, ka vajadzības grupas kalendāru var iestatīt dažādas lapās, un tiek ievērota šāda prioritāšu secība:
1. Krājumu vajadzības grupa lapā **Krājumu vajadzība**
1. Krājumu vajadzības grupa lapā **Detalizēta informācija par izlaistajām precēm**
1. Noklusējuma krājumu vajadzības grupa sadaļā **Vispārējās plānošanas parametri**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Nosūtīšanas datums plānotajam pārsūtīšanas pasūtījumam
Veidojot pārsūtīšanas pasūtījumu no vienas noliktavas uz otru, nosūtīšanas datums un saņemšanas datums ir iekļauts pārsūtīšanas pasūtījuma galvenē kopā ar noliktavu “No” un noliktavu “Uz”. Starpība starp šiem diviem datumiem ir paredzamais transportēšanas laiks (dienās) starp noliktavām.

Nosūtīšanas datums plānotajam pārsūtīšanas pasūtījumam norāda datumu, kurā preces tiek nosūtītas no noliktavas “No”. Kalendāri, kurus izmanto, lai norādītu pieejamo nosūtīšanas datumu, ir minēti tālāk pēc prioritātes: 
1. Noliktavas kalendārā noliktavai “No”
1. Vajadzības grupas kalendārs (regresa secību šim kalendāram skatiet iepriekš) Ja ir iestatīts noliktavas kalendārs, nosūtīšanas datums būs atvērts datums kalendārā. Ja nav iestatīts noliktavas kalendārs, tiks izmantots vajadzības grupas kalendārs. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Saņemšanas datums plānotajam pārsūtīšanas pasūtījumam
Saņemšanas datums pārsūtīšanas pasūtījumam norāda datumu, kurā preces tiek saņemtas noliktavā “Uz”.

Kalendāri, kurus izmanto, lai norādītu saņemšanas datumu, ir minēti tālāk pēc prioritātes: 
1. Vajadzības grupas kalendārs 
1. Noliktavas kalendārs noliktavai “Uz” Ja ir iestatīts vajadzības kalendārs, saņemšanas datums būs atvērts datums kalendārā. Ja nav iestatīts vajadzības grupas kalendārs, tiks izmantots noliktavas kalendārs. 

Meklējot nosūtīšanas un saņemšanas datumus plānotajai pārsūtīšanai, tiks ņemtas vērā arī rezerves, kuras noteicis lietotājs attiecībā uz nosūtīšanu un saņemšanu. 

## <a name="using-calendars-in-master-planning"></a>Kalendāru izmantošana vispārējā plānošanā

### <a name="assignment-of-scm-calendars"></a>SCM kalendāru piešķiršana
Ir svarīgi iestatīt kalendārus, lai identificētu uzņēmuma darbdienas. Labākais ieviešanas veids ir iestatīt kalendāru katram elementam ar dažādām darbdienām. Citiem vārdiem sakot, visi ārējie kalendāri (debitoru, kreditoru) un visi iekšējie kalendāri (noliktavu, vajadzības grupu un piegādes veidu), kas saistīti ar uzņēmumu.

### <a name="recommendation-on-warehouse-calendars"></a>Ieteikumi attiecībā uz noliktavas kalendāriem
Ir ieteicams izmantot vienu kalendāru katrai noliktavai, lai iekļautu konkrētas izmaiņas, kuras ietekmē tikai attiecīgo noliktavu. Piemēram, divām vai vairākām noliktavām varētu būt tādas pašas darbdienas, bet atšķirīga izsniegšanas politika. Šādā gadījumā kalendārs katrai no noliktavām ar attiecīgo izsniegšanas politiku ir labākais ieviešanas veids, lai sistēmā tiktu iekļauti labākie datumi plānotajiem pirkšanas, pārsūtīšanas un ražošanas pasūtījumiem. Ja nav iestatīti noliktavas kalendāri, juridiskās personas kalendāru var izmantot kā noklusējuma iestatījumu avotu noliktavas kalendāram. 

### <a name="recommendation-of-coverage-group-calendars"></a>Ieteikums attiecībā uz vajadzības grupu kalendāriem
Attiecībā uz vajadzības grupas kalendāru ir svarīgi ņemt vērā aspektus, kuriem ir pārlabojoša darbība saistībā ar saņemšanas datumiem vispārējā plānošanā. Tādēļ ir ieteicams to izmantot uzmanīgi. It īpaši tas ir noderīgi gadījumā, kad papildināšana jāveic noteiktās nedēļas dienās. 

### <a name="updating-scm-related-calendars"></a>Ar SCM saistītu kalendāru atjaunināšana
Lai gan ir svarīgi, ka visi atbilstīgie kalendāri tiek piešķirti attiecīgajā vietā (kreditors, debitors, noliktava, piegādes veids vai vajadzības grupa), ir svarīgi arī tos atjaunināt, lai tajos būtu redzamas izmaiņas. Sistēma noteiks ražošanas, pārsūtīšanas, pirkšanas un pārdošanas pasūtījumu datumus atkarībā no piešķirto kalendāru kombinācijas. Labākā prakse ir noskaidrot, kurš ir atbildīgs par kalendāru piešķiršanu un atjaunināšanu atbilstošajos apgabalos. Ja darbdienās rodas bojājumi vai citas neparastas izmaiņas, ir ļoti svarīgi atbilstoši atjaunināt kalendārus. Visi uzdevumi, kuri ir atkarīgi no kalendāriem, piemēram, vispārējā plānošana un ražošanas plānošana, ir jāpalaiž atkārtoti pēc kalendāru atjaunināšanas. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]