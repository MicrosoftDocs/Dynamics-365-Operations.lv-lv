---
title: "Veikala pasūtījumu izpildes apskats"
description: "Šajā tēmā ir sniegts apskats par veikala pasūtījumu izpildi."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: e0aa0e576f88fd497472aa4141704a66d51605c3
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2017

---

# <a name="store-order-fulfillment"></a>Veikala pasūtījumu izpilde

Daudzi mazumtirgotāji vēlas optimizēt pasūtījumu izpildi, ļaujot veikaliem izpildīt pasūtījumus. Pasūtījumu izpildīšana veikala līmenī var palīdzēt atvieglot krājumu pārsniegšanas scenārijus noteiktam veikalam, vai šāda izpildīšana var būt nepieciešama no loģistikas viedokļa gadījumos, kad veikalam ir papildu jauda vai tas atrodas tuvākā nosūtīšanas attālumā līdz debitoram. Lai risinātu šo vajadzību, pārdošanas punktā ir pieejama vienotās pasūtījumu izpildes operācija.

Pasūtījumiem, kurus paredzēts izpildīt noteiktā veikalā, pasūtījuma virsrakstā vai rindās ir norādīta šī veikala noliktava. 

Pasūtījumu izpildes operācija pārdošanas punktā nodrošina vienu darba apgabalu attiecīgajā pārdošanas punktā, kuru var izmantot pasūtījumu apstrādāšanai. Tas ietver visu — sākot no pasūtījuma pieņemšanas līdz pasūtījuma kā nosūtīta atzīmēšanai vai izdošanai veikalā. 

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Piekļuve vienotajai pasūtījumu izpildei pārdošanas punktā

Pasūtījumu izpildi, [Operācijas ID 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), var izmantot, lai piekļūtu veikala pasūtījumu izpildes darba apgabalam pārdošanas punktā. 

Standarta konfigurācijā pasūtījumu izpildes operācijai nav pašai savas atļaujas, bet nākotnē lietotāji varēs izmantot atļauju **Ļaut izgūt pasūtījumu**, lai izsauktu šo operāciju no pārdošanas punkta.

Veikala līmenī ir pieejams konfigurācijas iestatījums, kurš nosaka, vai pasūtījuma rinda pārdošanas punktā ir jāpieņem manuāli. Ja šī konfigurācijas opcija nav iestatīta, pasūtījuma rindas tiks pieņemtas pēc noklusējuma. Ja šī konfigurācijas opcija ir ieslēgta, lietotājiem pārdošanas punktā ir nepieciešams atlasīt atļauju **Atļaut pieņemt pasūtījumu**, lai pieņemtu pasūtījumus no šī pārdošanas punkta.
Pasūtījuma rindas pārdošanas punktā var arī noraidīt. Pasūtījuma rindas noraidīšana norāda, ka tā netiks izpildīta šajā veikalā, un attiecīgā pasūtījuma rinda tiek sūtīta atpakaļ, lai to pārpiešķirtu citam veikalam vai noliktavai. Pasūtījuma rindas noraidīšanas atļauja tiek piešķirta ar atļauju **Atļaut pasūtījumu noraidīt**. 

## <a name="order-fulfillment-operation-parameters"></a>Pasūtījumu izpildes operācijas parametri

Pasūtījumu izpilde nodrošina standarta komplektācijā ietvertos parametrus, kurus operācijai var lietot, kad šī operācija tiek izsaukta pārdošanas punktā. Ja ir konfigurēts parametrs **Visi pasūtījumi**, kad tiek lietota šī operācija, tiek rādīti visi pasūtījumi. Parametrs **Nosūtāmie pasūtījumi** rāda tikai pasūtījumus, kas ir jānosūta no veikala, un parametrs **Izdodamie pasūtījumi** rāda pasūtījumus, kurus ir paredzēts izdot veikalā. 

## <a name="orders-for-fulfillment"></a>Izpildāmie pasūtījumi

Pasūtījumu izpildes operācija rāda tikai pasūtījumus, kas tiks izdoti pašreizējā veikalā vai tiks nosūtīti no pašreizējā veikala. Izmantojot pasūtījumu izpildes operāciju, netiek rādīti pasūtījumi, ko paredzēts izpildīt citos veikalos. 

## <a name="line-selection"></a>Rindas atlase

Rindas var atlasīt, darbību rūtī izmantojot funkciju **Atlasīt**. Kad funkcija **Atlasīt** ir aktivizēta, apstrādei var atlasīt vairākas rindas. Atlasīto rindu atlasi varat notīrīt, noklikšķinot uz tās pašas rindas vēlreiz. 

## <a name="line-details"></a>Rindas informācija

Rindas informāciju var parādīt, izmantojot rindas informācijas uznirstošo izvēlni. Ja tiek izmantota šī izvēlne, tiek nodrošinātas divas cilnes, lai parādītu papildinformāciju par atlasīto rindu. Pirmajā cilnē **Rindas informācija** tiek rāda detalizēta informācija par pašu rindu, piemēram, pasūtītais un atlikušais daudzums. Tiek sniegta papildinformācija, tostarp izdotais, iepakotais un rēķinā iekļautais daudzums, kā arī piegādes veids un piegādes adrese. Cilnē **Pasūtījuma informācija** ir sniegta pasūtījuma virsraksta informācija, tostarp debitors, debitora ID, pasūtījuma numurs, pasūtījuma kopsumma un bilance.

Ja ir atlasītas vairākas rindas, pasūtījuma rindas informācijas uznirstošā izvēlne norāda tikai to, ka ir atlasītas vairākas rindas. Lai parādītu detalizētu informāciju par atsevišķu rindu, noņemiet rindu atzīmes, līdz atliek tikai viena rinda. 

## <a name="pending-order-lines"></a>Gaidošo pasūtījumu rindas

Vienotā pasūtījumu izpilde ietver spēju pieņemt pasūtījumus manuāli. Pēc noklusējuma veikalā izpildāmie pasūtījumi jau ir pieņemti. Taču, ja biznesa procesi nosaka, ka pasūtījumi ir jāpieņem darbiniekam veikala līmenī, manuālo pieņemšanu var ieslēgt mazumtirdzniecības veikala līmenī. Lai aktivizētu pasūtījuma pieņemšanu, dodieties uz **Retail** > **Kanāli** > **Mazumtirdzniecības veikali** > **Visi mazumtirdzniecības veikali**. Atveriet nepieciešamo veikalu un cilnē **Vispārīgi** atrodiet apakšvirsrakstu **Pasūtījumu izpilde**. Šim apakšvirsrakstam ir opcija **Manuāla pieņemšana**, kas pēc noklusējuma ir iestatīta uz **Nē**. Šo opciju iestatot uz **Jā** un izmaiņas sinhronizējot ar kanāla datu bāzi, pasūtījumu rindām var veikt pieņemšanas procesu.

Darbinieki, kuriem ir atļauja **Atļaut pieņemt pasūtījumu**, var atvērt pasūtījumu izpildi un atlasīt rindas pieņemšanai. Kad rindas ir pieņemtas, to stāvoklis no **Gaida** mainās uz **Pieņemts** un var turpināties pārējais pasūtījumu izpildes process. Ja ir ieslēgta opcija **Manuāla pieņemšana**, pasūtījumi tiek apstrādāti tikai pēc to pieņemšanas. 

Pasūtījumiem, ko paredzēts izdot veikalā, nekad nav stāvokļa **Gaida**. Tas tiek darīts tādēļ, lai nepieļautu scenāriju, kad debitors ierodas veikalā, bet pasūtījuma rindu nevar apstrādāt, jo nav pieejams darbinieks, kuram ir atbilstoša atļauja.

## <a name="accepted-order-lines"></a>Pieņemtās pasūtījumu rindas

Pasūtījumiem, kuriem rindas statuss ir **Pieņemts**, var turpināties pārējais pasūtījumu izpildes process pārdošanas punktā. Kad pasūtījums ir pieņemts, visas atlikušās darbības var veikt attiecībā pret pasūtījuma rindu. 

Piemēram, pieņemtu pasūtījuma rindu var atlasīt un pēc tam izdot tiešā veidā, nevis izpildot izdošanu un iepakošanu.

## <a name="line-actions"></a>Rindas darbības

### <a name="pick"></a>Izdot

Darbību kategorija **Izdot** ir paredzēta, lai palīdzētu veikt pasūtījumu rindu izdošanu no plauktiem. Izdošanas darbību var veikt tikai pasūtījumu rindām, kas iepriekš ir pieņemtas. 

**Darbība: Izdošana**

- Iegūtais POS statuss: Izdošana
- Iegūtais iekšējās uzskaites daļas statuss: Bez izmaiņām

Pēc pasūtījuma pieņemšanas rindas var atlasīt un atzīmēt kā **Izdošana**. Rindas atzīmēšana kā **Izdošana** ir veids, kā norādīt, ka šai rindai jau tiek veikts izdošanas darbs. Tādējādi netiek pieļauts, ka divi darbinieki vienlaikus mēģina izdot vienas un tās pašas pasūtījuma rindas.  

**Darbība: Drukāt izdošanas sarakstu**

- Iegūtais statuss: Izdošana
- Iegūtais iekšējās uzskaites daļas statuss: Bez izmaiņām

Lai palīdzētu darbiniekiem veikt izdošanas procesu, izdošanas sarakstus pārdošanas punktā var drukāt. Darbinieks, kas veic izdošanu, var ņemt līdzi izdrukātu izdošanas sarakstu un manuāli atzīmēt izdotās preces šajā sarakstā, līdzko tās tiek izdotas. 

Izdošanas saraksta formāts tiek konfigurēts programmā Dynamics 365 for Retail un tiek pievienots ieejas plūsmas profilam. Papildinformāciju par to, kā iestatīt ieejas plūsmas profilus, skatiet šeit: [Ieejas plūsmas veidnes un drukāšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

Ja ir atlasītas rindas un šīm rindām tiek drukāts izdošanas saraksts, tās tiek automātiski atjauninātas uz statusu **Izdošana**. 

**Darbība: Atzīmēt kā izdotu**

- Iegūtais statuss: Izdots vai Daļēji izdots
- Iegūtais iekšējās uzskaites daļas statuss: Izdots vai Daļēji izdots

Kad fiziskais izdošanas process ir izpildīts, rindas var atzīmēt kā **Izdots**. Atlasot rindu un atzīmējot to kā **Izdots**, tiek veikts reāllaika izsaukums atjaunināt šo pasūtījuma rindu programmā Dynamics 365 for Retail. Kad rinda pārdošanas punktā tiek atzīmēta kā **Izdots**, tās statuss iekšējās uzskaites daļā arī tiek atjaunināts uz **Izdots** un krājumu transakcijas norāda, ka krājumu daudzums ir samazinājies par norādīto daudzumu.

Kad pasūtījumi tiek apstrādāti laika gaitā, daļējus daudzumus var apstrādāt konkrētai rindai. Ja ir atlasīta kāda rinda, tiek veikta darbība **Atzīmēt kā izdotu** un daudzums ir lielāks par vienu, lietotājam tiek parādīts aicinājums norādīt daudzumu. Atlikušais daudzums, ko ir paredzēts izdot, tiek aizpildīts automātiski. Ja norādītais daudzums ir mazāks par atlikušo daudzumu, rindas statuss mainās uz **Daļēji izdots**. Kad šī pasūtījuma rinda tiek atjaunināta iekšējās uzskaites daļā, tā atspoguļo arī daļēji izdoto statusu un krājumu atjaunināšanai tiek izmantots lietotāja ievadītais daudzums. 

Ja pasūtījuma rinda tiek izdota kļūdaini, izdošanas procesa anulēšana šai pasūtījuma rindai ir jāveic iekšējās uzskaites daļā. Pārdošanas punktā pašlaik netiek atbalstīta nekāda izdošanas anulēšanas darbība. 

Pasūtījumu rindas no dažādiem pasūtījumiem var atlasīt un atzīmēt kā **Izdošana**, izdrukāt vienā un tajā pašā izdošanas sarakstā vai atzīmēt kā **Izdots**. 

### <a name="pack"></a>Iepakot

Pasūtījumu rindas var iepakot jebkurā brīdī pēc tam, kad attiecīgā pasūtījuma rinda ir pieņemta. 

**Darbība: Drukāt pavadzīmi**

- Iegūtais statuss: Iepakots vai Daļēji iepakots
- Iegūtais iekšējās uzskaites daļas statuss: Piegādāts vai Daļēji piegādāts

Šī darbība rindas atzīmē kā iepakotas vai daļēji iepakotas un izdrukā pavadzīmi. Pavadzīmi var drukāt, lai validētu preces, kas ir iepakotas kopā. Pavadzīmes formāts tiek konfigurēts programmā Dynamics 365 for Retail un tiek pievienots ieejas plūsmas profilam. Papildinformāciju par to, kā iestatīt ieejas plūsmas profilus, skatiet šeit: [Ieejas plūsmas veidnes un drukāšana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Darbība: Atzīmēt kā iepakotu**

- Iegūtais statuss: Iepakots vai Daļēji iepakots
- Iegūtais iekšējās uzskaites daļas statuss: Piegādāts vai Daļēji piegādāts

Darbību **Atzīmēt kā iepakotu** var izmantot, lai norādītu, ka rindas ir iepakotas, nedrukājot pavadzīmi. Gan darbība **Drukāt pavadzīmi**, gan darbība **Atzīmēt kā iepakotu** izveido krājumu transakcijas iekšējās uzskaites daļā. Iepakošanas rindas pārdošanas punktā izraisa pavadzīmju žurnālu ģenerēšanu iekšējās uzskaites daļā. 

Ja kāda pasūtījuma rinda ir iepakota kļūdaini, attiecīgais pavadzīmju žurnāls ir jāizlabo iekšējās uzskaites daļā. 

Vienlaikus var iepakot tikai rindas, kas atrodas vienā un tajā pašā pasūtījumā un kam ir vienāds piegādes veids.

Pašlaik opcija veikalā izdodamo rindu atzīmēšanai kā **Iepakots** ir atspējota. Šī iespēja tiks pievienota turpmākā laidienā. Pavadzīmes izveidošanas process tiks uzlabots, lai atbalstītu trešās personas nosūtīšanas informācijas iekļaušanu pavadzīmes procesā.

### <a name="pick-up"></a>Izdošana

Pasūtījumus, ko paredzēts izdot veikalā, var izdot tiešā veidā, līdzko tie ir izgūti pārdošanas punktā. Uz pasūtījumiem, ko paredzēts izdot veikalā, neattiecas pieņemšana. 

**Darbība: Izdot**

- Iegūtais statuss: Iekļauts rēķinā vai Daļēji iekļauts rēķinā
- Iegūtais iekšējās uzskaites daļas statuss: Iekļauts rēķinā vai Daļēji iekļauts rēķinā

Ja kāda rinda tiek atlasīta izdošanai no vienotās pasūtījumu izpildes, viss pasūtījums tiek ielādēts pārdošanas punktā un tiek atzīmēts viss atlasītās rindas daudzums. Pārdošanas punkta transakciju skatā tiek ielādētas arī citas rindas no šī pasūtījuma, bet to daudzums ir atzīmēts kā nulle. 

Kad izdošanai paredzētās rindas ir ielādētas transakciju skatā, maksu par transakciju var iekasēt kā parasti. 

Rindas, kas ir pilnībā iekļautas rēķinā, izmantojot izdošanu, vairs nav redzamas vienotajā pasūtījumu apstrādē. Rindas, kas ir izdotas daļēji, joprojām tiek rādītas vienotajā pasūtījumu izpildē līdz brīdim, kad tās ir izdotas pilnā apmērā. 

Ja kāda rinda ir izdota kļūdaini, ir jāveic atgriešana, lai labotu šo kļūdu.  

Vienlaikus var izdot tikai rindas, kas atrodas vienā un tajā pašā pasūtījumā un kam ir vienāds piegādes veids. 

### <a name="shipping"></a>Piegāde

Pasūtījumu rindas, ko paredzēts nosūtīt no veikala, var apstrādāt ar vienoto pasūtījumu izpildi, izmantojot darbību **Nosūtīt**. Ja kanāla līmenī ir konfigurēta manuāla pasūtījuma rindas pieņemšana, pasūtījumi pirms nosūtīšanas ir jāpieņem. Kad pasūtījuma rinda ir pieņemta un tās statuss ir **Gaida** vai tai ir cits statuss, rindas var nosūtīt. 

**Darbība: Nosūtīt**

- Iegūtais statuss: Iekļauts rēķinā vai Daļēji iekļauts rēķinā
- Iegūtais iekšējās uzskaites daļas statuss: Iekļauts rēķinā vai Daļēji iekļauts rēķinā

No vienotās pasūtījumu izpildes nosūtītās rindas tiek iekļautas rēķinā no iekšējās uzskaites daļas — līdzīga kā gadījumā, kad pasūtījums tiek iekļauts rēķinā tieši no iekšējās uzskaites daļas. Rindas, kas tiek sūtītas no vienotās pasūtījumu izpildes, netiek ielādētas transakciju skatā, un šo rindu nosūtīšanas laikā netiek veikta nekāda maksas iekasēšana. 

Pasūtījumu rindas, kas ir nosūtītas pilnībā, vairs nav redzamas vienotajā pasūtījumu izpildē. Daļēji nosūtītas rindas joprojām tiek rādītas vienotajā pasūtījumu izpildē līdz brīdim, kad tās ir nosūtītas pilnā apmērā. 

Vienlaikus var sūtīt tikai rindas no tā paša pasūtījuma. Ja vienā un tajā pašā pasūtījumā esošajām rindām ir dažādi piegādes režīmi, šīs rindas joprojām var atlasīt nosūtīšanai vienlaikus. 

### <a name="reject"></a>Noraidīt

Rindas vai daļējas rindas var noraidīt. Šī opcija ļauj mainīt rindu piešķiri, no iekšējās uzskaites daļas rindas pārpiešķirot citam veikalam vai noliktavai. Rindas var noraidīt tikai tādā gadījumā, ja tās vēl nav izdotas vai iepakotas. Lai noraidītu rindu, kas jau ir izdota vai iepakota, šai rindai no iekšējās uzskaites daļas ir nepieciešams anulēt izdošanu vai anulēt iepakošanu. 

**Darbība: Noraidīt**

- Iegūtais statuss: Noraidīts
- Iegūtais iekšējās uzskaites daļas statuss: Bez izmaiņām 

Noraidītās pasūtījumu rindas var skatīt no darbvietas **Pārdošanas pasūtījuma apstrāde un pieprasījums**. Darbvietā notīriet personu filtru, lai skatītu visas noraidītās pasūtījumu rindas dažādos veikalos. Cilnē **Noraidītās pasūtījumu rindas**, kas atrodas zem sadaļas **Pasūtījumi un izlase**, tiek rādīta detalizēta informācija par pasūtījumu rindām. Turklāt lietotāji var noklikšķināt uz pogas **Noraidītās pasūtījumu rindas** zem sadaļas **Kopsavilkums**, lai pārietu uz pārdošanas pasūtījumu skatu. Tajā tiek rādīti visi pasūtījumi, kuros ir viena vai vairākas noraidītās pasūtījumu rindas. Ja ir iespējota opcija Sadalīto pasūtījumu pārvaldība (Distributed Order Management — DOM), šie noraidītie pasūtījumi tiks automātiski pārpiešķirti izpildīšanai atbilstošajiem veikaliem, taču šīs pasūtījumu rindas var pārpiešķirt arī manuāli. Lai to izdarītu, atlasiet rindu, kurai **Izpildes statuss** tiek rādīts kā **Noraidīts**, un pēc nepieciešamības mainiet vietu/noliktavu. Noklikšķiniet uz nolaižamās izvēlnes **Atjaunināt rindu** un noklikšķiniet uz **Atiestatīt izpildes statusu**, lai atkarībā no pasūtījumu izpildes iestatījumiem šo izpildes statusu no **Noraidīts** mainītu uz **Pieņemts** vai **Gaida**. Pēc izpildes statusa atiestatīšanas veikala darbinieki šīs pasūtījuma rindas var skatīt pārdošanas punktā.

## <a name="line-quantity-tracking"></a>Rindas daudzuma izsekošana

Vienu pasūtījuma rindu, kuras daudzums ir vairāk nekā viens, var apstrādāt laika gaitā, tādējādi pasūtījuma rindām izveidojot vairākus apakšstāvokļus. Piemēram, ja kādam būvniekam ir projekts, kurā ir nepieciešami 500 dēļi, bet projekta gaitā šim būvniekam vienlaikus var izdot vai piegādāt tikai dažus dēļus, vienlaikus varētu pastāvēt gan izdotie, gan iepakotie, gan nosūtītie daudzumi. 

Katru reizi, kad tiek atlasīta kāda rinda, atlikušais daudzums šai rindai tiek aizpildīts automātiski, lai pieņemtu, ka atlikušais daudzums tiek apstrādāts. Izmantojot iepriekš minēto piemēru — ja 200 dēļi jau ir izdoti un izdošanai tiek atlasīta dēļu rinda, kā daudzums automātiski tiek aizpildīts atlikušais daudzums jeb 300 dēļi. Tāpat notiek, ja 200 dēļi jau ir iekļauti rēķinā. Šajā gadījumā automātiski tiek aizpildīts tikai atlikušais daudzums. 

Turpinot izmantot iepriekš minēto piemēru — ja 200 dēļi ir atzīmēti kā iepakoti un tiek atlasīta sūtīšana, automātiski tiek aizpildīts pilnais daudzums jeb 500 dēļi. Ja tiek sūtīti tikai 200 dēļi, sistēma pieņem, ka tiek sūtīti iepriekš iepakotie dēļi, un tiek samazināts iepakotais daudzums. Ja tiek sūtīts 201 dēlis, šis skaits vispirms tiek atņemts no iepakoto dēļu skaita, un viens atlikušais dēlis tiek atņemts no atlikušā daudzuma. 

## <a name="line-statuses"></a>Rindu statusi

Pasūtījumu rindām pārdošanas punktā ir vairāki statusi, kas atspoguļo pasūtījuma rindas stāvokli. Ne vienmēr statuss pārdošanas punktā sakrīt ar statusu iekšējās uzskaites daļā. Pasūtījuma rindas statusu var apskatīt, izmantojot pārdošanas punkta pasūtījumu izpildes operācijas. Iekšējās uzskaites daļā pasūtījumu rindas var apskatīt no attiecīgā pasūtījuma informācijas. Pasūtījuma informācijai var piekļūt, dodoties uz **Retail** > **Debitori** > **Visi debitoru pasūtījumi**. Lai apskatītu detalizētu informāciju par pasūtījumu, atlasiet **Pasūtījuma ID**. Pasūtījuma informācijā atlasiet cilni **Pārdošanas pasūtījums** un pēc tam zem apakšvirsraksta **Skatīt** atlasiet **Detalizēts statuss**. 

**Gaida** — pasūtījumu rindām, kas ir piešķirtas kādam veikalam, bet kas vēl nav pieņemtas, ir statuss **Gaida**, kad tās apskata no pārdošanas punkta. Rindām, kas gaida pieņemšanu pārdošanas punktā, iekšējās uzskaites daļā ir statuss **Pasūtījuma apstrādāšana**.

**Pieņemts** — pasūtījumu rindām, kas ir manuāli pieņemtas vai automātiski pieņemtas, ir statuss **Pieņemts**, kad tās apskata no pārdošanas punkta. Rindas ar statusu **Pieņemts** iekšējās uzskaites daļā tiek rādītas kā **Pasūtījuma apstrādāšana**.

**Izdošana** — rindām, kas pašlaik tiek izdotas veikala līmenī, ir statuss **Izdošana**. Šīs pašas rindas, tās skatot no iekšējās uzskaites daļas, tiek rādītas kā **Pasūtījuma apstrādāšana**.

**Izdots** un **Daļēji izdots** — rindām, kas ir izdotas vai daļēji izdotas, pārdošanas punktā ir statuss **Izdots** vai **Daļēji izdots**. Šīs pašas rindas iekšējās uzskaites daļā arī tiek rādītas ar statusu **Izdots** vai **Daļēji izdots**.

**Iepakots** un **Daļēji iepakots** — rindām, kas ir iepakotas vai daļēji iepakotas, pārdošanas punktā ir statuss **Iepakots** vai **Daļēji iepakots**. Šīs pašas rindas iekšējās uzskaites daļā arī tiek rādītas ar statusu **Piegādāts** vai **Daļēji piegādāts**.

**Daļēji iekļauts rēķinā** — rindām, kas ir daļēji izdotas vai daļēji nosūtītas, gan pārdošanas punktā, gan iekšējās uzskaites daļa ir statuss **Daļēji iekļauts rēķinā**.

**Iekļauts rēķinā** — rindas, kas ir pilnīgi iekļautas rēķinā, pārdošanas punktā vairs netiek rādītas izpildei. Iekšējās uzskaites daļā šo rindu statuss ir **Iekļauts rēķinā**.

## <a name="order-fulfillment-filtering"></a>Pasūtījuma izpildes filtrēšana

Pasūtījumu izpilde pārdošanas punktā ietver filtrēšanu, lai palīdzētu lietotājam ērti atrast nepieciešamo. Filtrus var mainīt, izmantojot darbību rūti, kas atrodas ekrāna **Pārdošanas punkts** apakšā. Pēc noklusējuma tiek lietots filtrs **Piegādes veids**, pamatojoties uz veidu, kā attiecīgā operācija ir iestatīta. Ja operācija ir iestatīta ar parametru **Visi pasūtījumi**, šis filtrs tiek lietots, kad piekļūstat pasūtījumu izpildei. Tas pats attiecas uz parametriem **Izdot veikalā** un **Nosūtīt no veikala**. Tālāk ir uzskaitīti citi filtri, kurus var lietot pasūtījumu izpildes skatīšanai.

  - Debitora numurs
  - Debitora nosaukums
  - Debitora e-pasts
  - Pasūtījuma numurs
  - Piegādes veids
  - Kvīts numurs
  - Kanāla atsauces ID
  - Sākotnējā veikala numurs
  - Rindas statuss
  - Veidošanas datums
  - Piegādes datums
  - Saņemšanas datums

