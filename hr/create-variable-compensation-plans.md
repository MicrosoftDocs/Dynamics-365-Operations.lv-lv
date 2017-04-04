---
title: "Mainīgās atlīdzības plānu izveide"
description: "Mainīgā atlīdzība veido darbinieka nestandarta algu, piemēram, prēmijas vai samaksu uzņēmuma akcijās. Šajā tēmā ir aprakstīti komponenti, kas jāiestata pirms varat izmantot mainīgās atlīdzības un darbinieku dalību mainīgās atlīdzības plānu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Mainīgās atlīdzības plānu izveide

Mainīgā atlīdzība veido darbinieka nestandarta algu, piemēram, prēmijas vai samaksu uzņēmuma akcijās. Šajā rakstā ir aprakstīti komponenti, kas ir jāiestata, lai varētu izmantot mainīgo atlīdzību un darbinieku reģistrēt mainīgās atlīdzības plānā.

Mainīgās atlīdzības summas saviem darbiniekiem var aprēķināt, ņemot vērā vairākus faktorus, piemēram, darbinieka sniegumu, darbinieka kompensācijas līmeni un nodaļas sniegumu.

## <a name="variable-compensation-components"></a>Aainīgās atlīdzības komponenti
### <a name="create-compensation-types"></a>Atlīdzības veidu izveide

**Mainīgās atlīdzības veidi **ir nepieciešams komponents. Izmantojot mainīgās atlīdzības veidus, var aprakstīt mainīgās atlīdzības veidus, ko jūsu organizācijā izmaksā. Tie arī ļauj norādīt, vai atlīdzība tiks izmaksāta skaidrā naudā vai citā veidā, piemēram, izmantojot krājumus.

### <a name="describe-vesting-rules"></a>Izmaksas nosacījumu aprakstīšana

Ja nepieciešams, uzņēmumi var iestatīt **Izmaksas nosacījumus**. Garantēšanas noteikumi apraksta, kā mainīgo piešķiršanas būtu jāsadala laika gaitā. Piemēram, garantēšanas noteikumu varētu norādīt, ka darbinieks saņem 25 procenti no viņa vai viņas kopējais balvu katru gadu nākamo četru gadu laikā. Garantēšanas noteikumi ir tikai informatīvs.

## <a name="variable-compensation-plans"></a>Atlīdzības mainīgās daļas struktūras
**Mainīgās atlīdzības plāns** satur mainīgās atlīdzības aprēķina kārtulas, metodes un noklusētās vērtības attiecīgajiem darbiniekiem. Kad veidojat mainīgās atlīdzības plānu, ir jāiestata mainīgās atlīdzības veids. Mainīgās atlīdzības tips nosaka, vai sistēma aprēķina valūtas daudzums vai vienību skaits kā balvu. Jums jāiestata arī aprēķina metode.

-   **Laika posmam,** -mainīgo piešķiršanas aprēķinu pamatā ir noteikta kompensācija, ko darbinieks bija noteiktā datumā. Šis datums ir norādīts procesu gadījumā, ja jaunā kompensācijas summas tiek apstrādāti.
-   **Salikts** — atlīdzības summa tiek aprēķināta katrai unikalajai fiksētas atlīdzības izmaksu likmei, kas procesa notikumā darbiniekam bija iestatita no perioda sākuma datuma līdz perioda beigu datumam. Likmes tiek pievienoti kopā, lai noteiktu galīgo piešķiršanu. Piemēram, ciklā, darbiniekam pārsūtīt uz citu vietu, kas bija dažādi apmaksas likme. Šajā gadījumā mainīgā atlīdzība tiek pielāgota atbilstoši laika periodam, kad darbiniekam bija paredzēta katra izmaksu likme.

Mainīgās atlīdzības summu var izteikt vai nu procentos no darbinieka parastās pamata izpeļņas, vai arī kā vienību skaita kopu.

-   Atlasiet opciju **Pamatsummas procenti**, lai ievadiet noklusējuma procentuālo vērtību, un pēc tam norādiet, vai pamatsumma ir darbinieka fiksētā izmaksu likme vai atskaites punkts darbinieka atlīdzības līmenim. Kompensācijas līmenis ir iestatīts uz darbinieka darbu. Viens no atskaites punktiem no kompensācijas struktūra var iestatīt kā kontroles punktā fiksētā kompensācijas plānu. Sistēma izmanto kompensāciju līmeni no darbinieka darba un norādītu iekšējo atsauci ar kontroles punktā, kas norādīts darbinieka fiksētā kompensācijas plānu kontroles punktu summu atrast darbinieka kompensācijas līmeni. Kontroles punktu summa pēc tam izmantos nevis darbinieka fiksētas samaksas likmes par pamatu piešķiršanas.
-   Atlasiet opciju** Vienību skaits**, lai ievadītu noklusējuma vienību skaitu, katras vienības vērtību un vienības vērtības valūtu, ja atlīdzības plāns ir bezskaidras naudas atlīdzībai (piemēram, 200 vienības krājuma, kas tiek novērtētas 40 USD vērtībā), vai tikai vienību skaitu, ja atlīdzības plāns katrai skaidras naudas atlīdzībai. Par naudas balvu, darbinieks saņem norādītā valūta, kuru izmanto viņa vai viņas fiksētā kompensācijas plānu (piemēram, 500 vienību 1 USD) vienību skaits. Relācija viens pret vienu vadības elementu var izmantot, lai norādītu, vai ir tiešu divpusēju kartēšanu starp vienību skaitu un vienības vērtība. Veidojot naudas bāzes plāna mainīgās atlīdzības plānu, izmantojot vienību skaitu, šī opcija tiek automātiski bloķēta, lai **Jā**, un vienības vērtība ir **1.0000**.

**Nomas noteikuma** iestatījums ļauj norādīt, vai visi darbinieki būtu jāsaņem pats palielinājums, neatkarīgi no laika, viņi bija pieņemti darbā (**nomas noteikuma** = **neviens**), vai vai darbiniekiem vajadzētu saņemt procentos no balvu, kuras pamatā ir darba cikla laikā garumu (**nomas noteikuma** = **procenti**). 

**Sviras** ļauj jums pielāgot darbinieka piešķiršanu, pamatojoties uz darbinieka departamenta darbību. Veiktspējas rādītājus var iestatīt katrai nodaļai **departamentu** lapu, zem **saistītās formas**&gt;**kompensāciju**&gt;**sniegumu**. Piešķiršanas darbiniekiem šajā departamentā saņemtās ir atkarīga no vērtības **procenti no mērķa sasniegt** jomā, kas norāda departamenta darbību:

-   Ja nodaļas sniegums ir 100 procenti, atlīdzība šīs nodaļas darbiniekiem tiek aprēķināta, ņemot vērā procentuālo vērtību, kas ir iestatīta laukā** Izmaksa pie 100%**.
-   Ja nodaļas sniegums ir lielāks par 100 procentiem, sistēma pievieno procentu likmi, kas ir iestatīta laukā **Katram 1% virs mērķa**, procentu likmei, kas ir iestatīta laukā **Izmaksa pie 100%**, līdz tiek sasniegta vērtība, kas ir iestatīta laukā **Augstākā pieļaujamā izmaksa**.
-   Ja nodaļas sniegums ir mazāks par 100 procentiem, sistēma atņem procentu likmi, kas ir iestatīta laukā **Katram 1% zem mērķa**, no procentu likmes, kas ir iestatīta laukā **Izmaksa pie 100%**, līdz tiek sasniegta vērtība, kas ir iestatīta laukā **Zemākā pieļaujamā izmaksa**.

Varat iestatīt** tolerances līmeņus** no sliekšņa procentuālajām vērtībām. Tādējādi tiks parādīts brīdinājuma ziņojums, ja tolerances rezultātā procentuālā vērtība pārsniedz procentuālās vērtības slieksni. 

Pēc noklusējuma sistēma meklē departaments, kas ir iestatīts uz darbinieka amatā. Tomēr balvu par dažiem darbiniekiem var atkarīgs no vairāku struktūrvienību. Šajā gadījumā dažādos departamentos un procentuālo daudzumu piešķiršanas, kas piešķirts katrai nodaļai sniegumu var iestatīt darbinieka mainīgās atlīdzības iesaistīšanās. Lai iegūtu papildinformāciju, skatiet sadaļu "mainīgās atlīdzības iesaistīšanās", kas seko. 

Tolerance tiek izmantota tikai tad, ja atlīdzības procesa laika tika atlasīta opcija** Alga par rezultātiem**. 

**Līmeņos ignorē** zīmne ļauj ignorēt balvu noklusējuma procentuālais daudzums vai vienību skaits, pamatojoties uz darbinieka kompensācijas apmēru. Ja **iespējot ignorē līmeņiem** ir iestatīts uz **Jā** darbiniekiem, kuri ir iesaistījušies mainīgās atlīdzības plānu, sistēma ņem no darbinieka darba līmeni, un tad meklē līmeņu ignorē tabulu, lai noteiktu procentuālo daļu vai vienību līmenī. Ja līmenis nav atrodams līmeni ignorē tabulas, noklusējuma procentuālo daļu vai vienību skaits **vispārējā** tiek izmantots cilnē. Procentuālo daudzumu un vienību skaits var arī ignorēt uz darbinieka iesaistīšanos mainīgās atlīdzības plānā.

## <a name="variable-compensation-enrollment"></a>Atlīdzības mainīgās daļas reģistrācija
### <a name="determine-who-is-eligible-for-the-plan"></a>Noteikšana, kurš ir piemērots plānam

Kad esat gatavi reģistrēt darbiniekus mainīgās atlīdzības plānam, vispirms ir jānosaka, kurš ir piemērots atlīdzībai, kas noteikta plānā. Līdz brīdim, kad tiek noteikta piemērotība, nevarēsit plānu piešķirt visiem darbiniekiem. Lai iestatītu piemērotību, atveriet lapu **Piemērotības nosacījumi**. Šajā lapā varat izveidot jaunu piemērotības kārtulu atlīdzības plānam un noteikt kritērijus, kādiem darbiniekam ir jāatbilst, lai varētu tikt reģistrēts atlīdzības plānam. Piemērotības kritērijos var ietvert tādus vienumus kā nodaļa, arodbiedrība, atlīdzības reģions (atrašanās vieta), darbs, darba funkcija, darba veids vai atlīdzības līmenis. Darbinieki var tikt reģistrēti atlīdzības plānam tikai tad, ja tie atbilst **visiem** kritērijiem, kas iestatīti piemērotības kārtulā. 

**Piezīme.** Piemērotības kārtulas tiek lietotas, lai noteiktu piemērotību gan fiksētas, gan mainīgās atlīdzības plānam. Piemērotības kārtulās tiek izmantota lauka Darbs, Amats un Darbinieks vērtība, kā arī darbinieku ieraksti, lai noteiktu, vai darbinieks ir piemērots atlīdzības plānam.

-   Lapā **Darbs**:
    -   lauka **Darbs** vērtība;
    -   lauka **Funkcija** un **Darba veids** vērtība cilnē **Darbu klasifikācija**;
    -   lauka **Līmenis** vērtība cilnē **Atlīdzība**;
-   lapā **Amati**: lauka **Nodaļa** un **Atlīdzības reģions** vērtība;
-   Par **darbinieku** lapa: darba arodbiedrības informāciju, kas saistīta ar darbinieka saskaņā ar **personisko informāciju**&gt;**darba arodbiedrības** par * * * darbinieks * tab

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Reģistrācijas mainīgās atlīdzības plānam iespējošana

Lapā **Mainīgās atlīdzības plāni** iestatiet opciju **Iespējot reģistrāciju** uz **Jā**, lai atļautu piemērotu darbinieku reģistrāciju plānam.

### <a name="enroll-the-employee"></a>Darbinieka reģistrēšana

Tagad varat reģistrēt darbiniekus mainīgās atlīdzības plānam. Lai darbinieku reģistrētu, dodieties uz lapu **Darbinieki** un atlasiet darbinieku. Pēc tam rūtī darbības noklikšķiniet uz **kompensāciju**&gt;**iesaistīšanās mainīgo plānā**. 

**Piezīme.** Mainīgās atlīdzības plānā opcija **Reģistrācija** jāiestata uz **Jā**. **Plāns** lauks rāda tikai tos plānus, kuru darbinieks ir tiesīgs, pamatojoties uz atbilstības noteikumi, kas iestatīti šie plāni. Ja atbilstības kārtula nav noteikts plāns, nav darbinieku varēs pretendēt uz šo plānu. 

Pārliecinieties, ka **datumā** lauks ir iestatīts pareizi. Ja izmanto mainīgās atlīdzības plānu **Composite** aprēķināšanas metodi, iesaistīšanās spēkā stāšanās varētu uzskatīt par darbinieka piešķiršanas aprēķināšanas laikā. 

Var izmantot **ignorē** tab ignorēt noteiktām vērtībām darbiniekam. Piemēram, ja **nomas noteikumu** ir iestatīts uz **procenti** plāns, un dažādi darbā pieņemšanas brīdī būtu jāizmanto darbinieka darbā pieņemšanas procentu aprēķina laikā, darbā pieņemšanas brīdī var iestatīt **darbā pieņemšanas datums noteikums** laukā. Var ignorēt, vai nu **Award procentiem** vērtību vai **vienību skaits** vērtību par noteiktu darbinieku, atkarībā no plāna iestatījumus. Šīs vērtības būs ņemt vēl nomas noteikums, veiktspējas faktorus un citus iestatījumus plānu. 

**Organizatorisko ignorē** tiek izmantoti viens vai vairāki struktūrvienību darbinieku piešķiršanas pamatā. Procenti, kas tiek sadalīts starp nodaļām vajadzētu kopā 100 procenti. Tiek uzskatīts par darbinieka individuālo sniegumu. Šie iestatījumi tiks lietoti tikai tad, ja **maksāt par sniegumu** ir atlasīts, palaižot kompensācijas process.

<a name="see-also"></a>Skatiet arī
--------

[Atlīdzības plāni](compensation-plans.md)


