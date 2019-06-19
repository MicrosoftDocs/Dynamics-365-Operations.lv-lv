---
title: Multikanālu papildu automātiskās maksas
description: Šajā tēmā ir aprakstītas iespējas pārvaldīt pasūtījuma papildu maksas mazumtirdzniecības kanāla pasūtījumiem, izmantojot papildu automātisko maksu līdzekļus.
author: hhaines
manager: annbe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: 47829a6fcae37e03510929dc46b942455016df0b
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577873"
---
# <a name="omni-channel-advanced-auto-charges"></a>Multikanālu papildu automātiskās maksas

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par to, kā konfigurēt un izvietot papildu automātisko maksu līdzekli, kas ir pieejams Dynamics 365 for Retail versijā 10.0.

Ja ir iespējoti papildu automātisko maksu līdzekļi, jebkurā atbalstītajā mazumtirdzniecības kanālā (pārdošanas punktā (POS), zvanu centrā un tiešsaistē) izveidotajiem pasūtījumiem var izmantot ERP lietojumprogrammā definētās [automātisko maksu](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigurācijas gan galvas, gan rindas līmeņa saistītajām maksām.

Laidienos pirms Dynamics 365 for Retail versijas 10.0 [automātisko maksu](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfigurācijas ir pieejamas tikai pasūtījumiem, kas ir izveidoti e-komercijas un zvanu centra kanālos. Versijā 10.0 un jaunākās versijās automātisko maksu konfigurācijas var izmantot POS sistēmā izveidotiem pasūtījumiem. Tādējādi var pārdošanas transakcijām sistemātiski pievienot papildu papildmaksas.

Laidienos pirms versijas 10.0, veicot POS transakciju Piegādāt visu vai Piegādāt atlasīto, POS lietotājam tiek prasīts manuāli ievadīt piegādes maksu. Lai gan programmas papildmaksu iespējas tiek izmantotas attiecībā uz to, kā maksas tiek ierakstītas pasūtījumā, netiek nodrošināts sistemātisks aprēķins — maksu vērtības aprēķinam tiek izmantota lietotāja ievadītā vērtība. Maksas var pievienot tikai kā vienu ar piegādi saistītu maksu kodu, un pēc maksu izveides, tā nevar viegli rediģēt vai mainīt POS sistēmā.

Versijā 10.0 un jaunākās versijās joprojām ir pieejama iespēja izmantot manuālas piegādes maksu pievienošanas uzvednes. Ja organizācija neiespējo parametru **Papildu automātiskās maksas**, tiek izmantotas tādas pašas POS sistēmas uzvednes ar aicinājumu manuāli ievadīt maksas.

Papildu automātisko maksu līdzeklis sniedz POS lietotājiem iespēju izmantot jebkuru definēto papildmaksu sistemātisku aprēķinu, pamatojoties uz automātisko maksu iestatījumu tabulām. Turklāt lietotāji var pievienot vai rediģēt neierobežotu skaitu papildu maksu un nodevu jebkurai POS pārdošanas transakcijai galvas vai rindas līmenī (skaidrā naudā apmaksātam pasūtījumam bez piegādes vai debitora pasūtījumam).

## <a name="enabling-advanced-auto-charges"></a>Papildu automātisko maksu iespējošana

Lapā **Retail \> Mazumtirdzniecības iestatīšana \> Parametri \> Mazumtirdzniecības parametri** dodieties uz cilni **Klientu pasūtījumi**. Kopsavilkuma cilnē **Maksas** opcijai **Izmantot papildu automātiskās maksas** iestatiet vērtību **Jā**.

![Parametrs Papildu automātiskās maksas](media/advancedchargesparameter.png)

Kad ir iespējotas papildu automātiskās maksas, izveidojot debitora pasūtījumu Piegādāt visu vai Piegādāt atlasīto, lietotājiem vairs netiek parādīta uzvedne ar norādi manuāli ievadīt piegādes maksu POS terminālī. POS pasūtījuma maksas tiek sistemātiski aprēķinātas un pievienotas POS transakcijai (ja tiek atrasta izveidotā pasūtījuma kritērijiem atbilstoša automātisko maksājumu tabula). Lietotāji var arī manuāli pievienot vai uzturēt galvas vai rindas līmeņa maksas, izmantojot jaunās POS operācijas, ko var pievienot POS ekrāna izkārtojumiem.

Kad ir iespējotas papildu automātiskās maksas, vairs netiek izmantoti esošie vienumu **Piegādes maksu kods** un **Atmaksāt piegādes maksas** parametri sadaļā **Mazumtirdzniecības parametri**. Šie parametri tiek lietoti tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Nē**.

Pirms šī līdzekļa iespējošanas noteikti veiciet savu darbinieku pārbaudi un apmācību, jo tādējādi tiks mainīta biznesa procesu plūsma piegādes vai citu maksu aprēķināšanai un pievienošanai POS pārdošanas pasūtījumiem. Pārliecinieties, vai saprotat procesa plūsmas ietekmi uz transakciju izveidi POS sistēmā. Papildu automātisko maksu iespējošana minimāli ietekmē zvanu centra un e-komercijas pasūtījumus. Zvanu centra un e-komercijas lietojumprogrammas darbojas tāpat kā iepriekš attiecībā uz automātisko maksājumu tabulu izmantošanu, lai aprēķinātu pasūtījuma papildu maksas. Zvanu centra kanāla lietotāji joprojām var manuāli rediģēt jebkuru sistēmas aprēķināto automātisko maksu galvas vai rindas līmenī vai manuāli pievienot papildu papildmaksas galvas vai rindas līmenī.

## <a name="additional-pos-operations"></a>POS papildu operācijas

Lai nodrošinātu papildu automātisko maksu pareizu darbību POS lietojumprogrammu vidē, ir pievienotas jaunas POS operācijas. Šīs operācijas ir jāpievieno jūsu [POS ekrāna izkārtojumiem](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) un jāizvieto POS ierīcēs, kad izvietojat papildu automātiskās maksas. Ja šīs operācijas netiek pievienotas, lietotāji nevar pārvaldīt vai uzturēt POS transakciju papildmaksas un nevar nekādā veidā pielāgot vai mainīt maksu vērtības, kas ir sistemātiski aprēķinātas, pamatojoties uz automātisko maksu konfigurācijām. Ir ieteicams izvietot POS izkārtojumā vismaz operāciju **Pārvaldīt maksas**.

Tālāk ir norādītas jaunās operācijas.

- **142. Pārvaldīt maksas** — izmantojiet šo operāciju, lai sniegtu POS lietotājiem iespēju skatīt un rediģēt papildmaksas POS transakcijām, kas tika pievienotas manuāli vai sistemātiski, izmantojot automātisko maksu aprēķinus.
- **141. Pievienot galvenes maksas** — izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot galvenes līmeņa papildmaksu jebkurai POS pārdošanas transakcijai (un atlasīt izmantojamo maksu kodu).
- **140. Pievienot rindas maksas** — izmantojiet šo operāciju, lai sniegtu lietotājam iespēju manuāli pievienot rindas līmeņa papildmaksu jebkurai POS pārdošanas transakcijas rindai (un atlasīt izmantojamo maksu kodu).
- **143. Pārrēķināt maksas** — izmantojiet šo operāciju, lai pārdošanas transakcijas maksas pārrēķinātu pilnībā. Visas lietotāja iepriekš pārrakstītās automātiskās maksas tiek pārrēķinātas, pamatojoties uz pašreizējo groza konfigurāciju.

Tāpat kā visām POS operācijām, arī šai operācijai var izveidot drošības konfigurācijas, lai pieprasītu, ka vadītājam ir jāapstiprina operācijas izpilde.

Ir svarīgi atzīmēt, ka iepriekš uzskaitītās POS operācijas var pievienot POS izkārtojumam arī tad, ja parametrs **Izmantot papildu automātiskās maksas** ir atspējots. Šādā gadījumā organizācijas vēl joprojām iegūst papildu priekšrocības, kas ļauj skatīt manuāli pievienotās maksas un rediģēt tās, izmantojot operāciju **Pārvaldīt maksas**. Lietotāji var izmantot arī POS transakciju operāciju **Pievienot virsraksta maksas** un **Pievienot rindas maksas** arī tad, ja parametrs **Izmanto papildu automātiskās maksas** ir atspējots. Ja parametrs **Izmantot papildu automātiskās maksas** ir atspējots, izmantošanas gadījumā operācijai **Pārrēķināt maksas** ir zemāka funkcionalitāte. Šajā gadījumā neviena vērtība netiks pārrēķināta, un visas transakcijai manuāli pievienotās maksas tiks atiestatītas uz $0,00.

## <a name="use-case-examples"></a>Lietošanas gadījumu piemēri

Šajā sadaļā ir aprakstīti lietošanas gadījumu piemēri, lai palīdzētu jums saprast, kā konfigurēt un izmantot automātiskās maksas un papildmaksas mazumtirdzniecības kanāla pasūtījumu kontekstā. Šajos piemēros ir aprakstīta lietojumprogrammas darbība gadījumā, ja ir iespējots parametrs **Izmantot papildu automātiskās maksas**.

### <a name="auto-charges-header-charges-example"></a>Galvas līmeņa automātisko maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs

Mazumtirgotājs vēlas automātiski pievienot transportēšanas maksas, kad jebkurā mazumtirdzniecības kanālā tiek izveidotas transakcijas, kurām ir nepieciešama preču piegāde debitoram. Mazumtirgotājs piedāvā 2 piegādes metodes: pa zemi un pa gaisu. Ja debitors izvēlas piegādi pa zemi un pasūtījuma vērtība ir mazāka nekā 100 USD, mazumtirgotājs vēlas iekasēt no debitora transportēšanas maksu 10,00 USD apmērā. Ja pasūtījuma vērtība ir lielāka nekā 100 USD un debitors izvēlas piegādi pa zemi, debitoram nav jāmaksā nekādas papildu transportēšanas maksas. Ja debitors izvēlas piegādi pa gaisu visiem pasūtījumiem neatkarīgi no to kopējās vērtības, tiek iekasēta transportēšanas maksa 20,00 USD apmērā.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Šī scenārija ietvaros ir jākonfigurē divas automātisko maksu tabulas.

Pārejiet uz sadaļu **Kreditori \> Maksu iestatīšana \> Automātiskās maksas**.

Konfigurējiet divas dažādas galvas līmeņa automātiskās maksas. Konfigurēt vienu maksu piegādes pa zemi režīmam un vienu maksu piegādes pa gaisu režīmam. Šī scenārija ietvaros konfigurējiet tās lietošanai visiem debitoriem.

Lai konfigurētu piegādes pa zemi maksas, lapas **Automātiskās maksas** rindu sadaļā definējiet maksu 10.00 USD apmērā, kas ir jālieto pasūtījumiem, kuru vērtība ir no 0,01 USD līdz 100 USD. Izveidojiet citu maksu rindu, lai norādītu, ka pasūtījumiem, kuru vērtība ir lielāka nekā 100,01 USD, netiek lietotas nekādas maksas.

![Automātisko maksu piemērs](media/headerchargesexample.png)

Lai konfigurētu piegādes pa gaisu maksas, formas Automātiskās maksas rindu sadaļā definējiet maksu 20,00 USD apmērā, kas ir jālieto visiem pasūtījumiem (kuru vērtība ir no 0,01 USD līdz 9 999 999 USD).

Nosūtiet izmaiņas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

#### <a name="sales-processing-for-this-scenario"></a>Pārdošanas transakciju apstrāde šim scenārijam

Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkuram POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotajam debitora pasūtījumam vai pārdošanas transakcijai, kam galvas līmenī ir iestatīta piegāde pa zemi vai pa gaisu, tiek izmantotas šīs maksas, un šādā gadījumā tās tiek automātiski lietotas pārdošanas darbībai.

Pašlaik maksas tiek lietotas visām pārdošanas transakcijām, kas ir izveidotas juridiskajai personai, kura izmanto šos piegādes režīmus, jo nav pieejama funkcionalitāte, kas sniedz iespēju norādīt, ka automātiskās maksas konfigurācija ir jālieto tikai noteiktam pārdošanas kanālam.

POS un e-komercijas scenārijos pasūtījumos nav skaidri definētas galvas, tāpēc galvas līmeņa maksas tiek lietotas tikai tad, ja visām transakcijas pārdošanas rindām ir iestatīts viens un tas pats piegādes režīms. Ja POS vai e-komercijas sistēmā izveidotajām transakcijām ir iestatīti jaukti izpildes režīmi, tiek izvērtētas un lietotas tikai rindas līmeņa automātiskās maksas.

Zvanu centra scenārijos lietotājs var kontrolēt piegādes režīma iestatījumu pasūtījuma galvā, tāpēc šiem pasūtījumiem tiek lietotas galvas līmeņa maksas pat tad, ja dažas no pārdošanas rindām ir konfigurētas cita piegādes režīma izmantošanai. Zvanu centra pasūtījumu galvas līmeņa maksas vienmēr tiek noteiktas, pamatojoties uz piegādes režīmu, kas ir definēts pārdošanas pasūtījuma galvas līmenī.

### <a name="auto-charges-line-charges-example"></a>Rindas līmeņa automātisko maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs 

Mazumtirgotājs vēlas no debitora iekasēt papildu maksu par iestatīšanu gadījumā, ja debitors iegādājas noteiktu datora modeli. Šim datoram ir nepieciešamas obligātas papildu iestatīšanas darbības, kuras mazumtirgotājs veic debitora vietā. Mazumtirgotājs ir informējis debitorus par to, ka par šo iestatīšanu tiek ņemta papildu maksa. Mazumtirgotājs vēlas finanšu pārskatu izveides nolūkos pārvaldīt ar šīs iestatīšanas maksas atsevišķi no preču pārdošanas cenas. Iegādājoties šo konkrēto datoru jebkurā mazumtirdzniecības kanālā, no debitora tiek iekasēta iestatīšanas maksa 19,99 USD apmērā.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Šī scenārija ietvaros ir jākonfigurē viena rindas līmeņa automātisko maksu tabula.

Pārejiet uz sadaļu **Kreditori \> Maksu iestatīšana \> Automātiskās maksas**.

Nolaižamajā izvēlnē **Līmenis** iestatiet vērtību **Rinda** un izveidojiet jaunu automātisko maksājumu ierakstu visiem debitoriem un konkrētajai precei vai preču grupai, par kuru tiks iekasēta iestatīšanas maksa.

![Automātisko maksu piemērs](media/linechargesexample.png)

Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

#### <a name="sales-processing-for-this-scenario"></a>Pārdošanas transakciju apstrāde šim scenārijam

Kad ir izpildītas iepriekš aprakstītās konfigurēšanas darbības un izmaiņas ir ieviestas kanāla datu bāzē, jebkurš POS sistēmas, zvanu centra vai e-komercijas kanālā izveidotais debitora pasūtījums vai pārdošanas transakcija, kurā tiek pasūtīta šī prece, izraisa rindas līmeņa maksas sistemātisku pievienošanu pasūtījuma kopsummai.

Pašlaik maksas tiek lietotas jebkurai pārdošanas rindai, kas atbilst rindas līmeņa automātisko maksu konfigurācijai konkrētajai juridiskajai personai, jo nav pieejama funkcionalitāte, kas sniedz iespēju konfigurēt rindas līmeņa automātiskās maksas lietošanu tikai noteiktam pārdošanas kanālam.

### <a name="manual-header-charges-example"></a>Manuālu galvas līmeņa maksu piemērs

#### <a name="use-case-scenario-description"></a>Lietošanas gadījuma scenārija apraksts

Mazumtirgotājs ievieš parastā procesa izņēmumu, piedāvājot nodrošināt īpašu preču piegādi uz mājām debitoriem, kas pasūta preces veikalā. Mazumtirgotājs un debitors ir vienojušies pa to, ka debitors par šo pakalpojumu maksās papildu apstrādes maksu 25 USD. Pasūtījuma pieņēmējam ir jāpievieno šī papildu maksa transakcijai. Tā kā šī ir vienota maksa un tā nav saistīta ne ar vienu atsevišķu pasūtījumā ietverto preci, tiek lietota galvas līmeņa maksa.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu **Debitori \> Maksu iestatīšana \> Maksas**, lai definētu scenārijam piemērotu maksu kodu.

![Maksu piemērs](media/chargesexample.png)

Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, maksu koda opcijas **Piegādes maksa** vērtību iestatiet uz **Jā**. Ja šo maksu ir arī atļauts sistemātiski atlīdzināt, veicot atgriešanas transakciju POS lietojumprogrammā, iestatiet opcijas **Atmaksājams** vērtību **Jā**. Karodziņš **Atmaksājams** tiek lietots tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**.

Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

[POS ekrāna izkārtojumā](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) ir jākonfigurē operācija **Pievienot galvas līmeņa maksu**, lai šo operāciju (141. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu. Ekrāna izkārtojuma izmaiņas ir jāizplata mazumtirdzniecības kanālā, kā arī izmantojot sadales grafika funkciju.

#### <a name="sales-processing-of-manual-header-charges"></a>Manuālo galvas līmeņa maksu apstrāde pārdošanas laikā

Lai izpildītu scenāriju POS lietojumprogramma, POS lietotājs izveido pārdošanas transakciju kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas. Pirms maksājuma iekasēšanas lietotājam ir izpilda operācija **Pievienot galvas līmeņa maksu**, kas prasa lietotājam atlasīt maksu kodu un ievadīt maksu vērtību. Kad lietotājs ir pabeidzis šo procesu, maksa tiek pievienota pārdošanas pasūtījumam kā galvas līmenī maksa.

Šo procesu var lietot zvanu centrā, izmantojot esošo līdzekli **Maksas**, kas ir pieejams rīkjoslas cilnē **Pārdot**. Lapā **Uzturiet maksas** lietotājs var pievienot jaunu maksu rindu pasūtījuma galvai.

### <a name="manual-line-charges-example"></a>Manuālu rindas līmeņa maksu piemērs

#### <a name="use-case-scenario"></a>Lietošanas gadījuma scenārijs

Debitors ir pieprasījis, lai 2 no 5 pārdošanas pasūtījumā ietvertajiem krājumiem tiktu iesaiņoti kā dāvanas. Mazumtirgotājs piedāvā šo papildu pakalpojumu, iekasējot maksu 2,00 USD apmērā par katru krājumu. Pasūtījuma pieņēmējam ir jāpievieno šīs maksas konkrētajiem krājumiem, kas ir jāiesaiņo kā dāvanas.

#### <a name="setup-and-configuration"></a>Iestatīšana un konfigurēšana

Nodrošiniet, ka šī scenārija ietvaros izmantotais maksu kods ir pareizi konfigurēts, pārejot uz sadaļu **Debitori \> Maksu iestatīšana \> Maksas**, lai definētu scenārijam piemērotu maksu kodu.

Ja maksa ir jāapstrādā kā ar piegādi saistīta maksa, lai varētu lietot ar piegādi saistītas atlaides vai akcijas, iestatiet maksu koda opcijas **Piegādes maksa** vērtību **Jā**. Ja maksu ir arī atļauts sistemātiski atlīdzināt, veicot atgriešanas transakciju POS lietojumprogrammā, iestatiet opcijas **Atmaksājams** vērtību **Jā**. Karodziņš **Atmaksājams** tiek lietots tikai tad, ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**.

Nosūtiet maksas uz Retail Server/kanāla DB, lai tās varētu lietot POS sistēmā, izpildot darbu **1040 sadales grafiks**.

Operācija **Pievienot rindas līmeņa maksu** ir jākonfigurē [POS ekrāna izkārtojumā](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) tā, lai šo operāciju (140. operāciju) varētu izsaukt, izmantojot lietotajam POS sistēmā pieejamu pogu. Ekrāna izkārtojuma izmaiņas ir jāizplata mazumtirdzniecības kanālā, kā arī izmantojot sadales grafika funkciju.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Manuālas rindas līmeņa maksas apstrāde pārdošanas laikā

Lai izpildītu scenāriju POS lietojumprogramma, POS lietotājs izveido pārdošanas transakciju kā parasti, pievienojot tai preces un jebkādas citas konfigurācijas. Pirms maksājuma iekasēšanas lietotājam POS krājumu saraksta ekrānā ir jāatlasa konkrētā rinda, kurai tiks lietota maksa, un jāizpilda operācija **Pievienotu rindas līmeņa maksu**. Lietotājam tiek prasīts atlasīt maksu kodu un ievadīt maksu vērtību. Kad lietotājs ir pabeidzis šo procesu, maksa tiek saistīta ar attiecīgo rindu un pievienota pasūtījuma kopsummai kā rindas līmenī maksa. Lietotājs var atkārtot šos procesu, lai pievienotu papildu maksas citām transakcijas krājumu rindām, ja tas ir nepieciešams.

Tādu pašu procesu var lietot zvanu centrā, izmantojot funkciju Uzturēt maksas, kas ir pieejama nolaižamajā izvēlnē **Finanšu dati** lapas **Pārdošanas pasūtījums** sadaļā **Pārdošanas pasūtījuma rindas**. Tādējādi tiek atvērta lapa **Uzturēt maksas**, kurā lietotājs var pievienot transakcijai jaunu rindai raksturīgu maksu.

## <a name="additional-features"></a>Papildu līdzekļi

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Maksu rediģēšana POS pārdošanas transakcijas ietvaros

[POS ekrāna izkārtojumam](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) ir jāpievieno operācija **Pārvaldīt maksas** (142), lai lietotājs varētu skatīt un rediģēt vai pārlabot jebkuras sistēmas aprēķinātās vai manuāli izveidotās galvas vai rindas līmeņa maksas. Ja operācija netiek pievienota, lietotāji nevar pielāgot POS transakcijas maksu vērtību, kā arī nevar skatīt detalizētu informāciju par maksām, piemēram, ar maksām saistīto maksu koda veidu.

POS sistēmas lapā **Pārvaldīt maksas** lietotājs var skatīt detalizētu informāciju gan par galvas līmeņa, gan par rindas līmeņa maksām. Lietotājs var izmantot šajā lapā pieejamo funkciju **Rediģēt**, lai mainītu iekasēto summu noteiktā maksu rindā. Kad ir manuāli pārrakstīta maksu rinda, tā netiek sistemātiski pārrēķināta, ja vien lietotājs neuzsāk operāciju **Pārrēķināt maksas**.

Ja iestatīšanas lapā **Mazumtirdzniecības parametri** ir konfigurēta opcija **Maksu pārlabošanas iemesla kods**, pēc maksu izmainīšanas POS lietojumprogrammā lietotājam tiek prasīts norādīt iemesla kodu.

Ja tiek noteikti pārrakstītu maksu iemeslu kodi, tiek nodrošināts arī jauns pārskats, kurā var pārskatīt un auditēt šīs pārlabošanas. Pārskats ir pieejams sadaļā **Mazumtirdzniecība \> Pieprasījumi un pārskati \> Maksu pārlabošanas vēsture**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Maksu atmaksāšana POS atgriešanas transakcijas ietvaros

Ja ir iestatīta parametra **Izmantot papildu automātiskās maksas** vērtība **Jā**, vairs netiek lietota esošā mazumtirdzniecības parametra **Atmaksāt piegādes maksas** vērtība. Lai norādītu, kuras maksas ir sistemātiski jāatmaksā debitoram, izmantojot papildu automātiskās maksas, pārliecinieties, vai saistītais maksu kods ir konfigurēts kā **Atmaksājams** iestatīšanas lapā **Maksu kods**. Pārliecinieties, vai iestatījumi ir sinhronizēti ar jūsu mazumtirdzniecības kanāla datu bāzēs, izmantojot sadales grafika apstrādi.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Maksu atmaksāšana atgriešanas pasūtījuma transakcijas ietvaros

Maksas netiek sistemātiski atmaksātas programmā Retail izveidoto **atgriešanas pasūtījumu** ietvaros. Kad tiek izveidots **atgriešanas pasūtījums**, lietotājiem ir jāatlasa opcija **Kopēt maksas**. Ja nav atlasīta opcija **Kopēt maksas**, netiek automātiski atgrieztas sākotnējā pārdošanas transakcijā ietvertās maksas. Ja ir atlasīta opcija **Kopēt maksas**, visas maksas tiek kopētas uz atgriešanas pasūtījumu un lietotājs var manuāli rediģēt vai noņemt jebkuras maksas, kuras viņš nevēlas atmaksāt. Zvanu centra atgriešanas pasūtījumu apstrādes procesā pašlaik netiek ņemts vērā karodziņš **Atmaksājams** iestatījumu sadaļā **Maksu kods**.

### <a name="configuring-pos-receipts-to-show-charges"></a>POS kvīšu konfigurēšana maksu parādīšanai

Lai nodrošinātu papildu automātisko maksu funkcionalitātes atbalstu, kvīts rindai un kājenei ir pievienoti tālāk norādītie kvīts elementi.

- **Rindas piegādes maksas** — šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par noteiktiem maksu kodiem, kas ir lietoti pārdošanas rindai. Šeit tiek rādīti tikai tie maksu kodi, kas ir atzīmēti ar maksu veida karodziņu **Piegāde** lapā **Maksu kods**
- **Citas rindas maksas** — šo rindas līmeņa elementu var izmantot, lai iegūtu kopsavilkumu par visu ar piegādi nesaistītu maksu kodiem, kas ir lietoti šai pārdošanas rindai. Tie ir maksu kodi, kas nav atzīmēti ar karodziņu **Piegāde** lapā**Maksu kods**.
- **Detalizēta informācija par pasūtījuma piegādes maksām** — šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas iestatīšanas lapā **Maksu kods** ir atzīmēti ar maksu veida karodziņu **Piegāde**.
- **Pasūtījuma piegādes maksas** — šis kājenes līmeņa elements rāda ar piegādi saistīto maksu vērtību dolāros.
- **Detalizēta informācija par citām pasūtījuma maksām** — šis kājenes līmeņa elements rāda to pasūtījumam lietoto maksu kodu aprakstus, kas nav atzīmēti kā ar piegādi saistītas maksas.
- **Citas pasūtījuma maksas** — šis kājenes līmeņa elements rāda ar citu, ar piegādi nesaistīto maksu vērtību dolāros.

Organizācijai ir ieteicams pievienot kvīts kājenei arī brīvā teksta laukus, lai definētu apgabalus, kur tiks veidoti kopsavilkumi par maksām.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Maksu aprēķināšanas liegšana līdz POS pasūtījuma pabeigšanai

Dažas organizācijas var izvēlēties pirms maksu parēķināšanas uzgaidīt, līdz lietotājs ir pabeidzis visu pārdošanas rindu pievienošanu POS transakcijai. Lai nepieļautu maksu aprēķināšanu, kamēr POS transakcijai tiek pievienoti krājumi, iespējojiet parametru **Manuāls maksas aprēķins** veikalam izmantotajā **funkcionalitātes profilā**. Ja ir iespējots šis parametrs, kad POS lietotājs ir pabeidzis preču pievienošanu POS transakcijai, viņam ir jāizmanto operācija **Aprēķināt kopsummas**. Pēc tam operācija **Aprēķināt kopsummas** aktivizē jebkuru pasūtījuma galvas vai rindas līmeņa automātisko maksu aprēķinu, ja tas ir attiecināms.

### <a name="charges-override-reports"></a>Maksu ignorēšanas pārskati

Ja lietotāji manuāli ignorē aprēķinātās maksas vai pievieno transakcijai manuālas maksas, šie dati būs pieejami auditēšanai pārskatā **Maksu ignorēšanas vēsture**. Pārskats ir pieejams sadaļā **Mazumtirdzniecība \> Pieprasījumi un pārskati \> Maksu ignorēšanas vēsture**. Ir svarīgi atzīmēt, ka šim pārskatam nepieciešamie dati tiek importēti no kanāla datu bāzes uz HQ, izmantojot "P" sadales grafika darbus. Tāpēc informācija par POS veiktajām ignorēšanas darbībām tūlītēji var nebūt pieejama šajā pārskatā, bet tikai tad, kad ar šo darbu HQ ir augšupielādēti saglabātie darbību dati.
