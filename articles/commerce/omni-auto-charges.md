---
title: Omni kanāla papildu automātiskās maksas
description: Šajā rakstā ir aprakstītas iespējas pārvaldīt citas pasūtījuma maksas Commerce kanāla pasūtījumiem, izmantojot papildu automātiskās maksas līdzekļus.
author: hhainesms
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: d44bc4ef61341c394b627ddbe10768d2ddf98de0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292710"
---
# <a name="omni-channel-advanced-auto-charges"></a>Omni kanāla papildu automātiskās maksas

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegta informācija par versiju 10.0 pieejamo papildu automātisko Dynamics 365 for Retail maksu līdzekļu konfigurāciju un izvietošanu.

Ja ir iespējoti papildu automātisko maksu līdzekļi, jebkurā atbalstītajā Commerce kanālā (pārdošanas punktā (POS), zvanu centrā un tiešsaistē) izveidotajiem pasūtījumiem var izmantot ERP lietojumprogrammā definētās [automātisko maksu](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigurācijas gan galvas, gan rindas līmeņa saistītajām maksām.

Laidienos pirms Retail versijas 10.0 [automātisko maksu](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigurācijas ir pieejamas tikai pasūtījumiem, kas ir izveidoti e-komercijas un zvanu centra kanālos. Versijā 10.0 un jaunākās versijās automātisko maksu konfigurācijas var izmantot POS sistēmā izveidotiem pasūtījumiem. Tādējādi var pārdošanas darījumiem sistemātiski pievienot papildu papildmaksas.

Laidienos pirms versijas 10.0, veicot POS darījumu "Piegādāt visu" vai "Piegādāt atlasīto", POS lietotājam tiek prasīts manuāli ievadīt piegādes maksu. Lai gan programmas papildmaksu iespējas tiek izmantotas attiecībā uz to, kā maksas tiek ierakstītas pasūtījumā, netiek nodrošināts sistemātisks aprēķins — maksu vērtības aprēķinam tiek izmantota lietotāja ievadītā vērtība. Maksas var pievienot tikai kā vienu ar piegādi saistītu maksu kodu, un pēc maksu izveides tās nevar viegli rediģēt vai mainīt POS sistēmā.

Versijā 10.0 un jaunākās versijās joprojām ir pieejama iespēja izmantot manuālas piegādes maksu pievienošanas uzvednes. Ja organizācija neiespējo parametru **Papildu automātiskās maksas**, tiek izmantotas tādas pašas POS sistēmas uzvednes ar aicinājumu manuāli ievadīt maksas.

Papildu automātisko maksu līdzeklis sniedz POS lietotājiem iespēju izmantot jebkuru definēto papildmaksu sistemātisku aprēķinu, pamatojoties uz automātisko maksu iestatījumu tabulām. Turklāt lietotājiem būs iespēja pievienot vai rediģēt neierobežotu skaitu papildu maksu un nodevu jebkuram POS darījumam galvas vai līnijas līmenī (skaidras naudas darījumiem vai klientu pasūtījumiem).

## <a name="enable-advanced-auto-charges"></a>Papildu automātisko maksu iespējošana

Lapā **Mazumtirdzniecība un komercija \> Heaquarters iestatīšana \> Parametri \> Commerce parametri** dodieties uz cilni **Klientu pasūtījumi**. Kopsavilkuma cilnē **Maksas** opcijai **Izmantot papildu automātiskās maksas** iestatiet vērtību **Jā**.

![Parametrs Papildu automātiskās maksas.](media/advancedchargesparameter.png)

Kad ir iespējotas papildu automātiskās maksas, izveidojot klienta pasūtījumu Piegādāt visu vai Piegādāt atlasīto, lietotājiem vairs netiek parādīta uzvedne ar norādi manuāli ievadīt piegādes maksu POS terminālī. POS pasūtījuma maksas tiek sistemātiski aprēķinātas un pievienotas POS darījumam (ja tiek atrasta izveidotā pasūtījuma kritērijiem atbilstoša automātisko maksājumu tabula). Lietotāji var arī manuāli pievienot vai uzturēt galvas vai rindas līmeņa maksas, izmantojot jaunās POS operācijas, ko var pievienot POS ekrāna izkārtojumiem.

Kad ir iespējotas papildu automātiskās maksas, vairs netiek izmantoti esošie vienumu **Piegādes maksu kods** un **Atmaksāt piegādes maksas** parametri sadaļā **Commerce parametri**. Šie parametri tiek lietoti tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Nē**.

Pirms iespējot šo opciju, pārliecinieties, ka esat apmācījis un pārbaudījis savus darbiniekus, jo iespējotā opcija mainīs biznesa procesa plūsmu piegādes vai citu maksu aprēķināšanai un pievienošanai POS tirdzniecības pasūtījumiem. Pārliecinieties, vai saprotat procesa plūsmas ietekmi uz darījumu izveidi POS sistēmā. Papildu automātisko maksu iespējošana minimāli ietekmē zvanu centra un e-komercijas pasūtījumus. Zvanu centra un e-komercijas lietojumprogrammas darbojas tāpat, kā iepriekš, attiecībā uz automātisko maksājumu tabulu izmantošanu, lai aprēķinātu pasūtījuma papildu maksas. Zvanu centra kanāla lietotāji joprojām var manuāli rediģēt jebkuru sistēmas aprēķināto automātisko maksu galvas vai rindas līmenī vai manuāli pievienot papildu papildmaksas galvas vai rindas līmenī.

## <a name="add-pos-operations"></a>POS operāciju pievienošana

Lai nodrošinātu papildu automātisko maksu pareizu darbību POS lietojumprogrammu vidē, ir pievienotas jaunas POS operācijas. Šīs operācijas ir jāpievieno jūsu [POS ekrāna izkārtojumiem](/dynamics365/unified-operations/retail/pos-screen-layouts) un jāizvieto POS ierīcēs, kad izvietojat papildu automātiskās maksas. Ja šīs operācijas netiek pievienotas, lietotāji nevar pārvaldīt vai uzturēt POS darījumu papildmaksas un nevar nekādā veidā pielāgot vai mainīt maksu vērtības, kas ir sistemātiski aprēķinātas, pamatojoties uz automātisko maksu konfigurācijām. Ir ieteicams izvietot POS izkārtojumā vismaz operāciju **Pārvaldīt maksas**.

Tālāk ir norādītas jaunās operācijas.

- **142. Pārvaldīt maksas** — izmantojiet šo operāciju, lai sniegtu POS lietotājiem iespēju skatīt un rediģēt papildmaksas POS darījumiem, kas tika pievienotas manuāli vai sistemātiski, izmantojot automātisko maksu aprēķinus.
- **141. Pievienot galvenes maksas** – izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot galvenes līmeņa papildmaksu jebkurai POS pārdošanas darījumam (un atlasīt izmantojamo maksu kodu).
- **140. Pievienot rindas maksas** – izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot rindas līmeņa papildmaksu jebkurai POS pārdošanas darījuma rindai (un atlasīt izmantojamo maksu kodu).
- **143. Pārrēķināt maksas** – izmantojiet šo operāciju, lai pārdošanas darījuma maksas pārrēķinātu pilnībā. Visas lietotāja iepriekš pārrakstītās automātiskās maksas tiek pārrēķinātas, pamatojoties uz pašreizējo groza konfigurāciju.

Tāpat kā visām POS operācijām, arī šai operācijai var izveidot drošības konfigurācijas, lai pieprasītu vadītāja apstiprinājumu operācijas izpildei.

Ir svarīgi atzīmēt, ka iepriekš uzskaitītās POS operācijas var pievienot POS izkārtojumam arī tad, ja parametrs **Izmantot papildu automātiskās maksas** ir atspējots. Šādā gadījumā organizācijas vēl joprojām iegūst papildu priekšrocības, kas ļauj skatīt manuāli pievienotās maksas un rediģēt tās, izmantojot operāciju **Pārvaldīt maksas**. Lietotāji var izmantot arī POS darījumu operāciju **Pievienot virsraksta maksas** un **Pievienot rindas maksas** arī tad, ja parametrs **Izmantot papildu automātiskās maksas** ir atspējots. Ja parametrs **Izmantot papildu automātiskās maksas** ir atspējots, izmantošanas gadījumā operācijai **Pārrēķināt maksas** ir zemāka funkcionalitāte. Šajā gadījumā neviena vērtība netiks pārrēķināta, un visas darījumam manuāli pievienotās maksas tiks atiestatītas uz $0,00.

## <a name="use-case-examples"></a>Lietošanas gadījumu piemēri

Šajā sadaļā ir aprakstīti lietošanas gadījumu piemēri, lai palīdzētu jums saprast, kā konfigurēt un izmantot automātiskās maksas un papildmaksas Commerce kanāla pasūtījumu kontekstā. Šajos piemēros ir aprakstīta lietojumprogrammas darbība gadījumā, ja ir iespējots parametrs **Izmantot papildu automātiskās maksas**.

### <a name="auto-charges-header-charges-example"></a>Galvas līmeņa automātisko maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs

Mazumtirgotājs vēlas automātiski pievienot transportēšanas maksas, kad jebkurā Commerce kanālā tiek izveidoti darījumi, kuriem ir nepieciešama preču piegāde klientam. Mazumtirgotājs piedāvā divas piegādes metodes: pa sauszemi un pa gaisu. Ja debitors izvēlas piegādi pa sauszemi un pasūtījuma vērtība ir mazāka nekā 100 USD, mazumtirgotājs vēlas iekasēt no klienta transportēšanas maksu 10,00 USD apmērā. Ja pasūtījuma vērtība ir lielāka nekā 100 USD un klients izvēlas piegādi pa sauszemi, klientam nav jāmaksā nekādas papildu transportēšanas maksas. Ja klients izvēlas piegādi pa gaisu visiem pasūtījumiem neatkarīgi no to kopējās vērtības, tiek iekasēta transportēšanas maksa 20,00 USD apmērā.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Šim scenārijam ir nepieciešama divu automātisko maksu tabulu konfigurēšana.

Pārejiet uz sadaļu **Debitori \> Izmaksu iestatīšana \> Automātiskās izmaksas**.

Konfigurējiet divas dažādas galvas līmeņa automātiskās maksas. Konfigurēt vienu maksu piegādes pa sauszemi režīmam un vienu maksu piegādes pa gaisu režīmam. Šī scenārija ietvaros konfigurējiet tās lietošanai visiem klientiem.

Lai konfigurētu piegādes pa zemi maksas, lapas **Automātiskās maksas** rindu sadaļā definējiet maksu 10.00 USD apmērā, kas ir jālieto pasūtījumiem, kuru vērtība ir no 0,01 USD līdz 100 USD. Izveidojiet citu maksu rindu, lai norādītu, ka pasūtījumiem, kuru vērtība ir lielāka nekā 100,01 USD, netiek lietotas nekādas maksas.

![Paraugs ar divām automātisko maksu tabulām.](media/headerchargesexample.png)

Lai konfigurētu piegādes pa gaisu maksas, formas Automātiskās maksas rindu sadaļā definējiet maksu 20,00 USD apmērā, kas ir jālieto visiem pasūtījumiem (kuru vērtība ir no 0,01 USD līdz 9 999 999 USD).

Nosūtiet izmaiņas uz Commerce Scale Unit/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

#### <a name="sales-processing-for-this-scenario"></a>Pārdošanas darījumu apstrāde šim scenārijam

Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkuram POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotajam klienta pasūtījumam vai pārdošanas darījumam, kam galvas līmenī ir iestatīta piegāde pa sauszemi vai pa gaisu, tiek izmantotas šīs maksas, un šādā gadījumā tās tiek automātiski lietotas pārdošanas darbībai.

Pašlaik maksas tiek lietotas visiem pārdošanas darījumiem, kas ir izveidoti juridiskajai personai, kura izmanto šos piegādes režīmus, jo nav pieejama funkcionalitāte, kas sniedz iespēju norādīt, ka automātiskās maksas konfigurācija ir jālieto tikai noteiktam pārdošanas kanālam.

POS un e-komercijas scenārijos pasūtījumos nav skaidri definētas galvas, tāpēc galvas līmeņa maksas tiek lietotas tikai tad, ja visām darījuma pārdošanas rindām ir iestatīts viens un tas pats piegādes režīms. Ja POS vai e-komercijas sistēmā izveidotajiem darījumiem ir iestatīti jaukti izpildes režīmi, tiek izvērtētas un lietotas tikai rindas līmeņa automātiskās maksas.

Zvanu centra scenārijos lietotājs var kontrolēt piegādes režīma iestatījumu pasūtījuma galvā, tāpēc šiem pasūtījumiem tiek lietotas galvas līmeņa maksas pat tad, ja dažas no pārdošanas rindām ir konfigurētas cita piegādes režīma izmantošanai. Zvanu centra pasūtījumu galvas līmeņa maksas vienmēr tiek noteiktas, pamatojoties uz piegādes režīmu, kas ir definēts pārdošanas pasūtījuma galvas līmenī.

### <a name="auto-charges-line-charges-example"></a>Rindas līmeņa automātisko maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs 

Mazumtirgotājs vēlas no klienta iekasēt papildu maksu par iestatīšanu gadījumā, ja klients iegādājas noteiktu datora modeli. Šim datoram ir nepieciešamas obligātas papildu iestatīšanas darbības, kuras mazumtirgotājs veic klienta vietā. Mazumtirgotājs ir informējis klientus par to, ka par šo iestatīšanu tiek ņemta papildu maksa. Mazumtirgotājs vēlas finanšu pārskatu izveides nolūkos pārvaldīt ar šīs iestatīšanas maksas atsevišķi no preču pārdošanas cenas. Iegādājoties šo konkrēto datoru jebkurā kanālā, no klienta tiek iekasēta iestatīšanas maksa 19,99 USD apmērā.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Šī scenārija ietvaros ir jākonfigurē vienas rindas līmeņa automātisko maksu tabula.

Pārejiet uz sadaļu **Debitori \> Izmaksu iestatīšana \> Automātiskās izmaksas**.

Nolaižamajā izvēlnē **Līmenis** iestatiet vērtību **Rinda** un izveidojiet jaunu automātisko maksājumu ierakstu visiem klientiem un konkrētajai precei vai preču grupai, par kuru tiks iekasēta iestatīšanas maksa.

![Vienas rindas līmeņa automātisko maksu tabulu piemērs.](media/linechargesexample.png)

Nosūtiet maksas uz Commerce Scale Unit/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

#### <a name="sales-processing-for-this-scenario"></a>Pārdošanas darījumu apstrāde šim scenārijam

Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkurš POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotais klienta pasūtījums vai pārdošanas darījums, kurā tiek pasūtīta šī prece, izraisa rindas līmeņa maksas sistemātisku pievienošanu pasūtījuma kopsummai.

Pašlaik maksas tiek lietotas jebkurai pārdošanas rindai, kas atbilst rindas līmeņa automātisko maksu konfigurācijai konkrētajai juridiskajai personai, jo nav pieejama funkcionalitāte, kas sniedz iespēju konfigurēt rindas līmeņa automātiskās maksas lietošanu tikai noteiktam pārdošanas kanālam.

### <a name="manual-header-charges-example"></a>Manuālu galvas līmeņa maksu piemērs

#### <a name="use-case-scenario-description"></a>Lietošanas gadījuma scenārija apraksts

Mazumtirgotājs ievieš parastā procesa izņēmumu, piedāvājot nodrošināt īpašu preču piegādi uz mājām klientiem, kas pasūta preces veikalā. Mazumtirgotājs un klients ir vienojušies pa to, ka klients par šo pakalpojumu maksās papildu apstrādes maksu 25,00 USD. Pasūtījuma pieņēmējam ir jāpievieno šī papildu maksa darījumam. Tā kā šī ir vienota maksa un tā nav saistīta ne ar vienu atsevišķu pasūtījumā ietverto preci, tiek lietota galvas līmeņa maksa.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu **Debitori \> Maksu iestatīšana \> Maksas**, lai definētu scenārijam piemērotu maksu kodu.

![Maksu piemērs.](media/chargesexample.png)

Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, maksu koda opcijas **Piegādes maksa** vērtību iestatiet uz **Jā**. Ja šo maksu ir arī atļauts sistemātiski atlīdzināt, veicot atgriešanas darījumu POS lietojumprogrammā, iestatiet opcijas **Atmaksājams** vērtību **Jā**. Karodziņš **Atmaksājams** tiek lietots tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**.

Nosūtiet maksas uz Commerce Scale Unit/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

[POS ekrāna izkārtojumā](/dynamics365/unified-operations/retail/pos-screen-layouts) ir jākonfigurē operācija **Pievienot galvas līmeņa maksu**, lai šo operāciju (141. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu. Ekrāna izkārtojuma izmaiņas ir jāizplata kanālā, kā arī izmantojot sadales grafika funkciju.

#### <a name="sales-processing-of-manual-header-charges"></a>Manuālo galvas līmeņa maksu apstrāde pārdošanas laikā

Lai izpildītu scenāriju POS lietojumprogrammā, POS lietotājs izveido pārdošanas darījumu, kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas. Pirms maksājuma iekasēšanas lietotājam ir izpilda operācija **Pievienot galvas līmeņa maksu**, kas prasa lietotājam atlasīt maksu kodu un ievadīt maksu vērtību. Kad lietotājs ir pabeidzis šo procesu, maksa tiek pievienota pārdošanas pasūtījumam kā galvas līmenī maksa.

Šo procesu var lietot zvanu centrā, izmantojot esošo līdzekli **Maksas**, kas ir pieejams rīkjoslas cilnē **Pārdot**. Lapā **Uzturiet maksas** lietotājs var pievienot jaunu maksu rindu pasūtījuma galvai.

### <a name="manual-line-charges-example"></a>Manuālu rindas līmeņa maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs

Klients ir pieprasījis, lai divi no pieciem pārdošanas pasūtījumā ietvertajiem elementiem tiktu iesaiņoti kā dāvanas. Mazumtirgotājs piedāvā šo papildu pakalpojumu, iekasējot maksu 2,00 USD apmērā par katru elementu. Pasūtījuma pieņēmējam ir jāpievieno šīs maksas konkrētajiem elementiem, kas ir jāiesaiņo kā dāvanas.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu **Debitori \> Maksu iestatīšana \> Maksas**, lai definētu scenārijam piemērotu maksu kodu.

Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, iestatiet maksu koda opcijas **Piegādes maksa** vērtību **Jā**. Ja maksu ir atļauts arī sistemātiski atlīdzināt, veicot atgriešanas darījumu POS lietojumprogrammā, iestatiet opcijas **Atmaksājams** vērtību **Jā**. Karodziņš **Atmaksājams** tiek lietots tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**.

Nosūtiet maksas uz Commerce Scale Unit/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

Operācija **Pievienot rindas līmeņa maksu** ir jākonfigurē [POS ekrāna izkārtojumā](/dynamics365/unified-operations/retail/pos-screen-layouts) tā, lai šo operāciju (140. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu. Ekrāna izkārtojuma izmaiņas ir jāizplata kanālā, kā arī izmantojot sadales grafika funkciju.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Manuālas rindas līmeņa maksas apstrāde pārdošanas laikā

Lai izpildītu scenāriju POS lietojumprogrammā, POS lietotājs izveido pārdošanas darījumu, kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas. Pirms maksājuma iekasēšanas lietotājam POS krājumu saraksta ekrānā ir jāatlasa konkrētā rinda, kurai tiks lietota maksa, un jāizpilda operācija **Pievienotu rindas līmeņa maksu**. Lietotājam tiek prasīts atlasīt maksu kodu un ievadīt maksu vērtību. Kad lietotājs ir pabeidzis šo procesu, maksa tiek saistīta ar attiecīgo rindu un pievienota pasūtījuma kopsummai kā rindas līmenī maksa. Lietotājs var atkārtot šos procesu, lai pievienotu papildu maksas citām darījuma elementu rindām, ja tas ir nepieciešams.

Tādu pašu procesu var lietot zvanu centrā, izmantojot funkciju "Uzturēt maksas", kas ir pieejama nolaižamajā izvēlnē **Finanšu dati** lapas **Pārdošanas pasūtījums** sadaļā **Pārdošanas pasūtījuma rindas**. Atlasot šo opciju, tiks atvērta lapa **Uzturēt maksas**, kurā lietotājs var pievienot jaunu līnijas maksu darījumam.

## <a name="additional-features"></a>Papildu iespējas

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Maksu rediģēšana POS pārdošanas darījuma ietvaros

[POS ekrāna izkārtojumam](/dynamics365/unified-operations/retail/pos-screen-layouts) ir jāpievieno operācija **Pārvaldīt maksas** (142), lai lietotājs varētu skatīt un rediģēt vai pārlabot jebkuras sistēmas aprēķinātās vai manuāli izveidotās galvas vai rindas līmeņa maksas. Ja operācija netiek pievienota, lietotāji nevar pielāgot POS darījuma maksu vērtību, kā arī nevar skatīt detalizētu informāciju par maksām, piemēram, ar maksām saistīto maksu koda veidu.

POS sistēmas lapā **Pārvaldīt maksas** lietotājs var skatīt detalizētu informāciju gan par galvas līmeņa, gan par rindas līmeņa maksām. Lietotājs var izmantot šajā lapā pieejamo funkciju **Rediģēt**, lai mainītu iekasēto summu noteiktā maksu rindā. Kad ir manuāli pārrakstīta maksu rinda, tā netiek sistemātiski pārrēķināta, ja vien lietotājs neuzsāk operāciju **Pārrēķināt maksas**.

Ja iestatīšanas lapā **Commerce parametri** ir konfigurēta opcija **Maksu pārlabošanas iemesla kods**, pēc maksu izmainīšanas POS lietojumprogrammā lietotājam tiek prasīts norādīt iemesla kodu.

Ja tiek noteikti pārrakstītu maksu iemeslu kodi, tiek nodrošināts arī jauns pārskats, kurā var pārskatīt un auditēt šīs pārlabošanas. Pārskats ir pieejams sadaļā **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Maksu pārlabošanas vēsture**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Maksu atmaksāšana POS atgriešanas darījuma ietvaros

Ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**, vairs netiek lietota esošā Commerce parametra **Atmaksāt piegādes maksas** vērtība. Lai norādītu, kuras maksas ir sistemātiski jāatmaksā klientam, izmantojot papildu automātiskās maksas, pārliecinieties, vai saistītais maksu kods ir konfigurēts kā **Atmaksājams** iestatīšanas lapā **Maksu kods**. Pārliecinieties, vai iestatījumi ir sinhronizēti ar jūsu Commerce kanāla datu bāzēm, izmantojot sadales grafika apstrādi.

> [!TIP]
> Norādes, kas jums palīdzēs nodrošināt, ka rindas līmeņa atmaksas maksas tiek aprēķinātas, balstoties uz atgrieztā daudzuma, skatiet [Sadaļā "Atmaksas maksas" netiek aprēķinātas, pamatojoties uz atgriezto daudzumu](/troubleshoot/Refund-charges-miscalculated-for-partial-quantity-returned.md).

### <a name="refunding-charges-on-a-return-order-transaction"></a>Maksu atmaksāšana atgriešanas pasūtījuma darījuma ietvaros

Maksas netiek sistemātiski atmaksātas programmā Commerce izveidoto **Atgriešanas pasūtījumu** ietvaros. Kad tiek izveidots **Atgriešanas pasūtījums**, lietotājiem ir jāatlasa opcija **Kopēt maksas**. Ja nav atlasīta opcija **Kopēt maksas**, netiek automātiski atgrieztas sākotnējā pārdošanas darījumā ietvertās maksas. Ja ir atlasīta opcija **Kopēt maksas**, visas maksas tiek kopētas uz atgriešanas pasūtījumu, un lietotājs var manuāli rediģēt vai noņemt jebkuras maksas, kuras viņš nevēlas atmaksāt. Zvanu centra atgriešanas pasūtījumu apstrādes procesā pašlaik netiek ņemts vērā karodziņš **Atmaksājams** iestatījumu sadaļā **Maksu kods**.

### <a name="configuring-pos-receipts-to-show-charges"></a>POS kvīšu konfigurēšana maksu parādīšanai

Lai nodrošinātu papildu automātisko maksu funkcionalitātes atbalstu, kvīts rindai un kājenei ir pievienoti tālāk norādītie kvīts elementi.

- **Rindas piegādes maksas** – šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par noteiktiem maksu kodiem, kas ir lietoti pārdošanas rindai. Šeit tiek rādīti tikai tie maksu kodi, kas ir atzīmēti ar maksu veida karodziņu **Piegāde** lapā **Maksu kods**
- **Citas rindas maksas** – šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par visu ar piegādi nesaistītu maksu kodiem, kas ir lietoti šai pārdošanas rindai. **Citas rindas maksas** ir maksu kodi, kas nav atzīmēti ar karodziņu **Piegāde** lapā **Maksu kods**.
- **Detalizēta informācija par pasūtījuma piegādes maksām** – šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas iestatīšanas lapā **Maksu kods** ir atzīmēti ar maksu veida karodziņu **Piegāde**.
- **Pasūtījuma piegādes maksas** – šis kājenes līmeņa elements rāda ar piegādi saistīto maksu vērtību dolāros.
- **Detalizēta informācija par citām pasūtījuma maksām** – šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas nav atzīmēti kā ar piegādi saistītas maksas.
- **Citas pasūtījuma maksas** – šis kājenes līmeņa elements rāda ar citu, ar piegādi nesaistīto maksu vērtību dolāros.

Organizācijai ir ieteicams pievienot kvīts kājenei arī brīvā teksta laukus, lai definētu apgabalus, kur tiks veidoti kopsavilkumi par maksām.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Maksu aprēķināšanas liegšana līdz POS pasūtījuma pabeigšanai

Dažas organizācijas var izvēlēties pirms maksu parēķināšanas uzgaidīt, līdz lietotājs ir pabeidzis visu pārdošanas rindu pievienošanu POS darījumam. Lai nepieļautu maksu aprēķināšanu, kamēr POS darījumam tiek pievienoti elementi, iespējojiet parametru **Manuāls maksas aprēķins** veikalam izmantotajā **Funkcionalitātes profilā**. Ja ir iespējots šis parametrs, kad POS lietotājs ir pabeidzis preču pievienošanu POS darījumam, viņam ir jāizmanto operācija **Aprēķināt kopsummas**. Pēc tam operācija **Aprēķināt kopsummas** aktivizē jebkuru pasūtījuma galvas vai rindas līmeņa automātisko maksu aprēķinu, ja tas ir attiecināms.

### <a name="charges-override-reports"></a>Maksu ignorēšanas pārskati

Ja lietotāji manuāli ignorē aprēķinātās maksas vai pievieno darījumam manuālas maksas, šie dati būs pieejami auditēšanai pārskatā **Maksu ignorēšanas vēsture**. Pārskats ir pieejams sadaļā **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Maksu pārlabošanas vēsture**. Ir svarīgi atzīmēt, ka šim pārskatam nepieciešamie dati tiek importēti no kanāla datu bāzes uz HQ, izmantojot "P" sadales grafika darbus. Tāpēc informācija par POS veiktajām ignorēšanas darbībām tūlītēji var nebūt pieejama šajā pārskatā, bet tikai tad, kad ar šo darbu HQ ir augšupielādēti saglabātie darbību dati.

## <a name="additional-resources"></a>Papildu resursi

[Automātisko maksu iespējošana un konfigurēšana katram kanālam](auto-charges-by-channel.md)

[Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās](pro-rate-charges-matching-lines.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
