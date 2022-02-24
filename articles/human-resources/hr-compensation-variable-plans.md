---
title: Mainīgās atlīdzības plānu izveide
description: Mainīgā atlīdzība veido darbinieka nestandarta algu, piemēram, prēmijas vai samaksu uzņēmuma akcijās. Šajā rakstā ir aprakstīti komponenti, kas ir jāiestata, lai varētu izmantot mainīgo atlīdzību un darbinieku reģistrēt mainīgās atlīdzības plānā.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 85e64c4186c7782391a3db6dc4deb3fab0ea9f4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419487"
---
# <a name="create-variable-compensation-plans"></a>Mainīgās atlīdzības plānu izveide

Mainīgā atlīdzība veido darbinieka nestandarta algu, piemēram, prēmijas vai samaksu uzņēmuma akcijās. Šajā rakstā ir aprakstīti komponenti, kas ir jāiestata, lai varētu izmantot mainīgo atlīdzību un darbinieku reģistrēt mainīgās atlīdzības plānā.

Mainīgās atlīdzības summas saviem darbiniekiem var aprēķināt, ņemot vērā vairākus faktorus, piemēram, darbinieka sniegumu, darbinieka kompensācijas līmeni un nodaļas sniegumu.

## <a name="variable-compensation-components"></a>Aainīgās atlīdzības komponenti
### <a name="create-compensation-types"></a>Atlīdzības veidu izveide

**Mainīgās atlīdzības veidi** ir nepieciešams komponents. Izmantojot mainīgās atlīdzības veidus, var aprakstīt mainīgās atlīdzības veidus, ko jūsu organizācijā izmaksā. Tie arī ļauj norādīt, vai atlīdzība tiks izmaksāta skaidrā naudā vai citā veidā, piemēram, izmantojot krājumus.

### <a name="describe-vesting-rules"></a>Izmaksas nosacījumu aprakstīšana

Ja nepieciešams, uzņēmumi var iestatīt **Izmaksas nosacījumus**. Izmaksas nosacījumos tiek aprakstīts, kā laika gaitā jāsadala mainīgās atlīdzības. Piemēram, izmaksu nosacījumā var būt norādīts, ka darbinieks saņems 25 procentus no viņa vai viņas kopējās atlīdzības katru gadu četru gadu laikā. Izmaksas nosacījumiem ir tikai informatīvs nolūks.

## <a name="variable-compensation-plans"></a>Atlīdzības mainīgās daļas struktūras
**Mainīgās atlīdzības plāns** satur mainīgās atlīdzības aprēķina kārtulas, metodes un noklusētās vērtības attiecīgajiem darbiniekiem. Kad veidojat mainīgās atlīdzības plānu, ir jāiestata mainīgās atlīdzības tips. Mainīgās atlīdzības tips nosaka, vai sistēma kā atlīdzību aprēķina valūtas summu vai vienību skaitu. Jums jāiestata arī aprēķina metode.

-   **Noteiktā laikā** — mainīgās atlīdzības aprēķina pamatā ir fiksēta atlīdzība, kas darbiniekam ir jāizmaksā noteiktā datumā. Šis datums tiek norādīts procesa notikumā, kad tiek apstrādātas jaunas atlīdzības summas.
-   **Salikts** — atlīdzības summa tiek aprēķināta katrai unikalajai fiksētas atlīdzības izmaksu likmei, kas procesa notikumā darbiniekam bija iestatita no perioda sākuma datuma līdz perioda beigu datumam. Pēc tam likmes tiek saskaitītas, lai noteiktu gala atlīdzību. Piemēram, cikla laikā darbinieks tika pārcelts citā amatā, kam paredzēta citāda izmaksu likme. Šajā gadījumā mainīgā atlīdzība tiek pielāgota atbilstoši laika periodam, kad darbiniekam bija paredzēta katra izmaksu likme.

Mainīgās atlīdzības summu var izteikt vai nu procentos no darbinieka parastās pamata izpeļņas, vai arī kā vienību skaita kopu.

-   Atlasiet opciju **Pamatsummas procenti**, lai ievadiet noklusējuma procentuālo vērtību, un pēc tam norādiet, vai pamatsumma ir darbinieka fiksētā izmaksu likme vai atskaites punkts darbinieka atlīdzības līmenim. Atlīdzības līmenis tiek iestatīts darbinieka darbam. Vienu atsauces punktu no atlīdzības struktūras var iestatīt kā atskaites punktu fiksētās atlīdzības plānā. Sistēma izmanto atlīdzības līmeni no darbinieka darba un veido tam krustenisko atsauci ar atskaites punktu, kas ir norādīts darbinieka fiksētas atlīdzības plānā, lai atrastu darbinieka atlīdzības līmeņa kontroles punkta summu. Pēc tam kā atlīdzības pamatsumma tiek izmantota kontroles punkta summa, nevis darbinieka fiksēto izmaksu likme.
-   Atlasiet opciju **Vienību skaits**, lai ievadītu noklusējuma vienību skaitu, katras vienības vērtību un vienības vērtības valūtu, ja atlīdzības plāns ir bezskaidras naudas atlīdzībai (piemēram, 200 vienības krājuma, kas tiek novērtētas 40 USD vērtībā), vai tikai vienību skaitu, ja atlīdzības plāns katrai skaidras naudas atlīdzībai. Naudas atlīdzības gadījumā darbinieks saņems norādīto vienību skaitu tajā valūtā, kas tiek izmantota viņa vai viņas fiksētas atlīdzības plānā (piemēram, 500 vienības ar vērtību 1 USD). Relācijas “viens pret vienu” kontroli var izmantot, lai norādītu, vai starp vienību skaitu un vienības vērtību pastāv tiešs “viens pret vienu” kartējums. Kad veidojat mainīgās atlīdzības plānu izmaksām skaidrā naudā, izmantojot vienību skaitu, šī opcija automātiski tiek bloķēta uz **Jā**, un vienības vērtība ir **1,0000**.

Izmantojot iestatījumu **Nolīgšanas kārtula**, varat norādīt, vai visiem darbiniekiem ir jāsaņem vienāds palielinājums neatkarīgi no datuma, kurā viņi tika pieņemti darbā (**Nolīgšanas kārtula** = **Nav**), vai arī šiem darbiniekiem ir jāsaņem procenti no atlīdzības atkarībā no tā, cik ilgi viņi bija nodarbināti cikla laikā (**Nolīgšanas kārtula** = **Procenti**). 

**Līdzekļu faktors** — ļauj koriģēt darbinieku atlīdzību, ņemot vērā darbinieka nodaļas sniegumu. Veiktspējas rādītājus katrai nodaļai var iestatīt lapas **Nodaļas** sadaļā **Saistītās formas** &gt; **Atlīdzība** &gt; **Veiktspēja**. Atlīdzība, ko saņem attiecīgās nodaļas darbinieki, ir atkarīga no vērtības laukā **Sasniegtie mērķa procenti**, kas norāda nodaļas sniegumu.

-   Ja nodaļas sniegums ir 100 procenti, atlīdzība šīs nodaļas darbiniekiem tiek aprēķināta, ņemot vērā procentuālo vērtību, kas ir iestatīta laukā **Izmaksa pie 100%**.
-   Ja nodaļas sniegums ir lielāks par 100 procentiem, sistēma pievieno procentu likmi, kas ir iestatīta laukā **Katram 1% virs mērķa**, procentu likmei, kas ir iestatīta laukā **Izmaksa pie 100%**, līdz tiek sasniegta vērtība, kas ir iestatīta laukā **Augstākā pieļaujamā izmaksa**.
-   Ja nodaļas sniegums ir mazāks par 100 procentiem, sistēma atņem procentu likmi, kas ir iestatīta laukā **Katram 1% zem mērķa**, no procentu likmes, kas ir iestatīta laukā **Izmaksa pie 100%**, līdz tiek sasniegta vērtība, kas ir iestatīta laukā **Zemākā pieļaujamā izmaksa**.

Varat iestatīt **tolerances līmeņus** no sliekšņa procentuālajām vērtībām. Tādējādi tiks parādīts brīdinājuma ziņojums, ja tolerances rezultātā procentuālā vērtība pārsniedz procentuālās vērtības slieksni. 

Pēc noklusējuma sistēma meklē nodaļu, kas ir iestatīta darbinieka amatam. Taču dažu darbinieku atlīdzība var būt atkarīga no vairāku nodaļu snieguma. Tādā gadījumā dažādas nodaļas un atlīdzības procentuālo vērtību, kas tiek piešķirta atkarībā no katras nodaļas snieguma, var iestatīt darbinieka mainīgās atlīdzības reģistrācijas lapā. Papildinformāciju skatiet sadaļā “Mainīgās atlīdzības reģistrācija”. 

Tolerance tiek izmantota tikai tad, ja atlīdzības procesa laika tika atlasīta opcija **Alga par rezultātiem**. 

Cilnē **Līmeņu ignorēšana** varat ignorēt atlīdzības noklusējuma procentuālo vērtību vai vienību skaitu, pamatojoties uz darbinieka atlīdzības līmeni. Ja vienums **Iespējot ignorēšanu līmeņiem** ir iestatīts uz **Jā** tiem darbiniekiem, kuri ir reģistrēti mainīgās atlīdzības plānam, tad sistēma ņem līmeni no darbinieka darba un pēc tam meklē to līmeņu ignorēšanas tabulā, lai šim līmenim noteiktu procentuālo vērtību vai vienību skaitu. Ja līmeņu ignorēšanas tabulā līmenis nav atrodams, tiek izmantota noklusējuma procentuālā vērtība vai vienību skaits no cilnes **Vispārīgi**. Procentuālo vērtību un vienību skaitu var ignorēt arī darbinieka mainīgās atlīdzības plāna reģistrācijā.

## <a name="variable-compensation-enrollment"></a>Atlīdzības mainīgās daļas reģistrācija
### <a name="determine-who-is-eligible-for-the-plan"></a>Noteikšana, kurš ir piemērots plānam

Kad esat gatavi reģistrēt darbiniekus mainīgās atlīdzības plānam, vispirms ir jānosaka, kurš ir piemērots atlīdzībai, kas noteikta plānā. Līdz brīdim, kad tiek noteikta piemērotība, nevarēsit plānu piešķirt visiem darbiniekiem. Lai iestatītu piemērotību, atveriet lapu **Piemērotības nosacījumi**. Šajā lapā varat izveidot jaunu piemērotības kārtulu atlīdzības plānam un noteikt kritērijus, kādiem darbiniekam ir jāatbilst, lai varētu tikt reģistrēts atlīdzības plānam. Piemērotības kritērijos var ietvert tādus vienumus kā nodaļa, arodbiedrība, atlīdzības reģions (atrašanās vieta), darbs, darba funkcija, darba veids vai atlīdzības līmenis. Darbinieki var tikt reģistrēti atlīdzības plānam tikai tad, ja tie atbilst **visiem** kritērijiem, kas iestatīti piemērotības kārtulā. 

**Piezīme.** Piemērotības kārtulas tiek lietotas, lai noteiktu piemērotību gan fiksētas, gan mainīgās atlīdzības plānam. Piemērotības kārtulās tiek izmantota lauka Darbs, Amats un Darbinieks vērtība, kā arī darbinieku ieraksti, lai noteiktu, vai darbinieks ir piemērots atlīdzības plānam.

- Lapā **Darbs**:
  -   lauka **Darbs** vērtība;
  -   lauka **Funkcija** un **Darba veids** vērtība cilnē **Darbu klasifikācija**;
  -   lauka **Līmenis** vērtība cilnē **Atlīdzība**;
- lapā **Amati**: lauka **Nodaļa** un **Atlīdzības reģions** vērtība;
- lapā <strong>Darbinieki</strong>: informācija par darbinieku arodbiedrībām, kas darbiniekam ir piesaistītas lapā <strong>Personīgā informācija</strong> &gt; <strong>Arodbiedrības</strong> cilnē *<strong><em>Darbinieks</em></strong>*.

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Reģistrācijas mainīgās atlīdzības plānam iespējošana

Lapā **Mainīgās atlīdzības plāni** iestatiet opciju **Iespējot reģistrāciju** uz **Jā**, lai atļautu piemērotu darbinieku reģistrāciju plānam.

### <a name="enroll-the-employee"></a>Darbinieka reģistrēšana

Tagad varat reģistrēt darbiniekus mainīgās atlīdzības plānam. Lai darbinieku reģistrētu, dodieties uz lapu **Darbinieki** un atlasiet darbinieku. Pēc tam darbību rūtī noklikšķiniet uz **Atlīdzība** &gt; **Reģistrācija mainīgam plānam**. 

**Piezīme.** Mainīgās atlīdzības plānā opcija **Reģistrācija** jāiestata uz **Jā**. Laukā **Plāns** tiek rādīti tikai tie plāni, kuriem darbinieks ir piemērots, balstoties uz šiem plāniem iestatītajām piemērotības kārtulām. Ja plānam piemērotības kārtula nav iestatīta, neviens darbinieks nav piemērots šim plānam. 

Pārliecinieties, ka lauka **Spēkā stāšanās datums** vērtība ir iestatīta pareizi. Ja mainīgās atlīdzības plānam tiek izmantota aprēķina metode **Kompozīts**, tad darbinieka atlīdzības aprēķināšanas laikā varētu tikt ņemts vērā reģistrācijas spēkā stāšanās datums. 

Var izmantot cilni **Prioritātes**, lai darbiniekam ignorētu noteiktas vērtības. Piemēram, ja plānā opcija **Nolīgšanas kārtula** ir iestatīta uz **Procenti** un darbinieka darbā pieņemšanas procentu aprēķina laikā ir jāizmanto cits darbā pieņemšanas datums, tad darbā pieņemšanas datumu varat iestatīt laukā **Nolīgšanas kārtulas datums**. Atkarībā no plāna iestatījumi noteiktam darbiniekam varat ignorēt arī lauka **Piemaksas procenti** vai lauka **Vienību skaits** vērtību. Šīs vērtības joprojām tiks aprēķinātas, ņemot vērā nolīgšanas kārtulu, veiktspējas faktorus un citus plāna iestatījumus. 

Vērtības **Organizatoriskās prioritātes** tiek izmantotas, lai darbinieka atlīdzību pamatotu ar vienas vai vairāku nodaļu sniegumu. Dažādām nodaļām sadalīto procentuālo vērtību kopsummai ir jābūt 100 procentiem. Tiek ņemts vērā arī darbinieka individuālais sniegums. Šie iestatījumi tiek izmantoti tikai tad, ja atlīdzības procesa izpildes laikā tiek atlasīta opcija **Alga par rezultātiem**.



