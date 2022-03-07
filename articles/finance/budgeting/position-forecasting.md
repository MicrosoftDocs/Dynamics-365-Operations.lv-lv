---
title: Pozīciju prognozēšana
description: Izdevumi, kas ir saistīti ar darbiniekiem, bieži veido lielu daļu no organizācijas izmaksām. Pozīciju prognozēšana ļauj jums plānot šos izdevumus un iekļaut tos budžetu plānošanā.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d43d0f92e666dd512fc6f2681aa8c7b6446edd5c
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595490"
---
# <a name="position-forecasting"></a>Pozīciju prognozēšana

[!include [banner](../includes/banner.md)]

Izdevumi, kas ir saistīti ar darbiniekiem, bieži veido lielu daļu no organizācijas izmaksām. Pozīciju prognozēšana ļauj jums plānot šos izdevumus un iekļaut tos budžetu plānošanā.

## <a name="position-forecasting-in-budget-planning"></a>Pozīciju prognozēšana budžeta plānošanā

[![Pozīcijas prognozēšanas komponenti.](./media/graphic-top.png)](./media/graphic-top.png) 

Pozīciju prognozēšanai tiek izmantotas trīs galvenās sastāvdaļas, lai nodrošinātu precīzas budžeta summas pozīciju izdevumiem. Pēc tam šīs summas var ievest budžeta plānā budžeta aprēķiniem. 

Galvenais komponents ir **prognozes pozīcija**, kas atspoguļo visus izmaksu datus, kas ir saistīti ar vienu pozīciju. Var izveidot vairākas prognozes pozīcijas versijas, piešķirot dažādu budžeta plāna scenāriju katrai versijai. Vairākas versijas ļauj izmantot iteratīvu pieeju budžeta plānošanai un ļauj salīdzināt iespēju scenārijus. Katrai prognozes pozīcijai ir atbilstošais amats personāla vadībā.

**Budžeta izmaksu elements** ir iestatīšanas komponents, kas pārstāv konkrētu izmaksu, kas ir saistīta ar amatu, piemēram, algu, darba devēja apmaksājamo veselības apdrošināšanu, mobilā tālruņa atvieglojumus un tā tālāk. Budžeta izmaksu elements ietver galveno kontu, kas tiek izmantots aprēķināšanas izmaksām un opcijām. Katru budžeta izmaksu elementu var piešķirt vairākām prognozes pozīcijām. 

**Atlīdzības grupa** ir izvēles iestatīšanas komponents, kas tiek izmantots, lai lietotu budžeta izmaksu elementu kopu un apmaksas aprēķinus pozīcijām, kurām ir līdzīgas apmaksas īpašības. Atlīdzības grupa var ietvert apmaksas likmju atlīdzības režģi. Kad grupa ir piešķirta prognozes pozīcijai, līmeni un darbību režģī var piešķirt prognozes pozīcijas peļņai. Izmaksu elementu kopa tiek pievienota automātiski.

### <a name="position-forecasting-processes"></a>Pozīciju prognozēšanas procesi

[![Pozīcijas prognozēšanas procesu ilustrācijas.](./media/graphic1b.png)](./media/graphic1b.png) 

Tipiskā pozīcijas prognozēšanas procesā vispirms tiek izveidoti iestatīšanas komponenti (budžeta izmaksu elementi un atlīdzības grupas). Prognozes pozīcijas tiek ģenerētas pamatojoties uz esošajām pozīcijām. Pēc tam varat veikt pielāgojumus. Piemēram, varat pievienot vai beigt pozīcijas, mainīt apmaksas likmes un atvieglojumu izmaksas un pievienot algas palielinājumus. Var izveidot vairākas prognozes pozīcijas versijas, atvieglojot dažādu budžeta plānošanas scenāriju salīdzināšanu. Pēc tam varat ietvert prognozes pozīcijas budžeta plānos un ieviest izmaksas no prognozes pozīcijām kā budžeta plāna rindas.

Varat izveidot papildu prognozes pozīcijas versijas, kad budžeta plāni tiek pārskatīti. Šīs jaunas versijas dod pamatu grozījumu veikšanai.

## <a name="position-forecasting-setup"></a>Pozīcijas prognozēšanas iestatīšana
[![Ilustrāciju marķēšanas iestatījumi.](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budžeta izmaksu elementi

Budžeta izmaksu elementi tiek izmantoti, lai noteiktu izmaksu informāciju prognozes pozīcijai. Šī informācija ietver izmaksu tipu, izmaksu aprēķina veidu un vai izmaksas tiek attiecinātas uz vairākiem datumiem, kad prognozes pozīcija tiek iekļauta budžeta plānā. 

Īpaši lauki nosaka budžeta izmaksu elementa uzvedību. Katrs budžeta izmaksu elements ir piešķirts budžeta izmaksu tipam **Ienākumi**, **Atvieglojumi**, **Nodokļi** vai **Citi**. Budžeta izmaksu tipi tiek galvenokārt izmantoti, lai aprēķinātu kopsummas. Vērtība **Prognozes pozīcijas ignorēšana** norāda, vai summas elementā var modificēt prognozes pozīcijai. Lauks **Sadalījuma metode** tiek izmantots, kad prognozes pozīcija tiek pievienota budžeta plānam. Varat sadalīt izmaksu summu atsevišķās budžeta plāna rindās ar dažādiem datumiem, pamatojoties uz mēneša, ceturkšņa, nedēļas vai divām nedēļām. Atlasot sākuma datumu, jūs piešķirat izmaksas kā vienu summu sākuma datumā, kas ir iestatīts prognozes pozīcijai. 

Budžeta izmaksu elementa izmaksu summas aprēķinā tiek izmantoti spēkā stāšanās datumi, lai nodrošinātu tādus pašus izmaksu elementus, kuri tiks izmantoti dažādos periodos. Viens galvenais konts tiek piešķirts katrā periodā kopā ar procentiem vai gada summu, kas norāda izmaksu summu. Budžeta izmaksu elementam var izmantot procentu no citiem izmaksu elementiem vai gada summas, bet ne abus. Varat arī norādīt gada ierobežojumu. 

Ja izmaksu elements ir balstīts uz procentuālo daudzumu, ir jānorāda budžeta izmaksu elementi, kas tiek izmantoti kā aprēķina pamats.

**Piemērs** 

Jodi organizācija sniedz apmācības atvieglojumu, kas ir 5 procenti no darbinieka pamatalgas. Jodi vēlas izveidot budžeta izmaksu elementu šīm izmaksām. Viņa izveido jaunu budžeta izmaksu elementu un piešķir budžeta izmaksu tipu **Atvieglojums**.

Jodi nevēlas mainīt atvieglojumu summu vadītājiem. Tādēļ viņa atlasa **Neatļaut izmaksu izmaiņas** laukā **Prognozes pozīcijas ignorēšana**. Organizācija vēlas piešķirt šīs izmaksas vienmērīgi katru mēnesi. Tāpēc Jodi atlasa **Ceturkšņa** laukā **Sadalījuma metode**. 

Pēc tam Jodi pievieno izmaksu aprēķina rindu, iestata datumus un galveno kontu un ievada **5,00** kā procentuālo vērtību. Organizācijai ir 5000 $ ierobežojums gadā šim atvieglojumam. Tāpēc Jodi ievada šo summu kā gada ierobežojumu. 

Visbeidzot, Jodi pievieno visus ieņēmumu izmaksu elementus, kas tiek izmantoti pamata algā kā aprēķina pamats. Tagad budžeta izmaksu elements ir gatavs izmantošanai.

### <a name="compensation-groups"></a>Atlīdzības grupas

Atlīdzības grupas var izmantot, lai grupētu prognozes pozīcijas ar līdzīgiem atlīdzības atribūtiem. Tās var izmantot arī, lai definētu prognozes pozīcijas ieņēmumus un gada pieaugumus un lai piešķirtu kopējo budžeta izmaksu elementu kopu. 

Atlīdzības grupu pamata funkcija ir piešķirt budžeta izmaksu elementu kopu prognozes pozīcijai Tāpēc atlīdzības grupas var izmantot, lai pievienotu kopējās izmaksas, piemēram, atvieglojumu plānus un nodokļus. Vadītājam, kas veido prognozes pozīciju, nav jāzina visi pievienojamie izmaksu elementi. Tā vietā, izmaksu elementus var pievienot, atlasot atlīdzības grupu. Elementi tiek pievienoti atlīdzības grupas iestatījumiem cilnē **Budžeta izmaksu elementi**. 

Atlīdzības grupas var norādīt peļņas likmes prognozes pozīcijai. Varat iestatīt grupu, lai izmantotu stundas vai gada algas pamatu prognozes pozīcijas peļņas aprēķināšanai. Cilnē **Atlīdzības likmju tabulas** apmaksas likmju atlīdzības režģis nosaka peļņu, kas tiek pievienota prognozes pozīcijai, ņemot vērā piešķirto līmeni un darbību. Šie režģi var būt balstīti uz esošajiem kompensācijas režģiem Personāla vadībā. Var arī varat izveidot jaunus kompensāciju režģus budžeta plānošanai. 

Spēkā stāšanās datumi un beigu datumi atlīdzības likmju tabulās ļauj mainīt apmaksas likmes jebkurā datumā. Šī funkcija ir noderīga, ja sarunu struktūrvienība ir vienojusies par vispārēju visaptverošu palielinājumu budžeta cikla vidū. Šādā gadījumā jūs maināt esošas tabulas beigu datumu uz datumu pirms likmes maiņas datuma un pievienojat jaunu likmju tabulu, kas stājas spēkā jaunajā datumā. Ja jaunas likmju tabulas izveides laikā atlasāt opciju **Izveidot jaunu atlīdzības režģi no esoša režģa**, varat atlasīt esošu likmju tabulu no moduļa Personāla vadība. Izveidotajā likmju tabulā opcija **Masveida izmaiņas** ļauj izmantot procentuālo vai vienotās summas pieaugumu vai samazinājumu visām likmēm režģī. 

Atlīdzības grupas lauki **Pieauguma grafiks** un **Pieauguma datums** tiek izmantoti, kad ir jāizveido algas pieaugumi, jo amati pāriet no vienas darbības uz nākamo. Gada algas pieaugums ir tipisks scenārijs. Pieauguma grafiks nosaka, vai posma pieaugumam tiek lietots amata gadadienas datums vai viens vispārīgs datums. Pieauguma grafiks attiecas uz visām prognozes pozīcijām atlīdzības grupā. 

Ieņēmumu izmaksu elements, kas atlasīts atlīdzības grupā, tiek lietots, kad veidojat peļņu prognozes pozīcijām grupā, tostarp to pamata algu un darbības palielinājumus. Lauks **Atlīdzības fiksētā sistēma** saista atlīdzības grupu ar atlīdzības fiksēto sistēmu personāla vadībā. Šī saite var piešķirt informāciju par darbinieka fiksēto atlīdzību prognozes pozīcijai, un tādēļ varat precīzāk veikt budžeta plānošanu. Atcerieties, ka atlīdzības režģa (līmeņu un darbību) struktūrai atlīdzības grupai ir jāatbilst fiksētās atlīdzības sistēmas struktūrai. Pretējā gadījumā sistēma nevar pareizi saistīt atlīdzības grupu un fiksēto atlīdzības sistēmu.

## <a name="creating-forecast-positions"></a>Prognozes pozīcijas izveide
[![Ilustrācija: iezīmēšana "izveidot prognožu pozīcijas."](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Prognozes pozīciju izveide esošajiem amatiem

Lai nodrošinātu visprecīzāko budžeta plānošanu, varat izveidot prognozes amatus, izmantojot detalizētu informāciju no esošajiem amatiem neatkarīgi no tā, vai amats pašlaik ir vai nav aizpildīts. 

Funkcija **Pievienot esošos amatus** parāda visus organizācijas amatus. Iestatot **No** datumu, varat mainīt amatu sarakstu, lai tajā ir amati, kas pastāvējusi kādā datumā agrāk vai parasti nākotnē (piemēram, nākamā budžeta cikla sākumu). Atlasiet budžeta plānošanas procesu un budžeta plāna scenāriju, atlasiet amatus sarakstā un pēc tam noklikšķiniet uz **Labi**, lai izveidotu prognozes pozīcijas atlasītajiem amatiem. Ievērojiet, ka var izveidot tikai vienu prognozes pozīciju katram esošajam amatam budžeta plānošanas procesā un scenārijā. Tomēr, varat izveidot papildu versijas, piešķirot citus budžeta plāna scenārijus. 

Ja budžeta izmaksu elementi tika piešķirti amatam personāla vadībā, tie budžeta izmaksu elementi tiek piešķirti arī prognozes pozīcijai un izmanto noklusētās summas. Lauks **Piešķirtais darbinieks** prognozes pozīcijā ir iestatīts uz tā darbinieka vārdu, kas ir piešķirts šim amatam, ja darbinieks ir piešķirts. Šis lauks ir vienkāršs teksta lauks. Tiešā saite netiek izveidota. 

Atlasot budžeta izmaksu elementu, fiksētās atlīdzības gada summa tiek piešķirta prognozes pozīcijai, izmantojot atlasīto izmaksu elementu, pie nosacījuma, ka piešķirtajam darbiniekam ir fiksētās atlīdzības sistēma. Ja darbiniekam nav fiksētas atlīdzības sistēmas vai ja nav piešķirts neviens darbinieks, budžeta izmaksu elementam tiek izmantota noklusējuma summa. 

Kad opcija **Piešķirt atlīdzības grupu** ir iestatīta uz **Jā**, ja darbiniekam, kurš ir piešķirts amatam, ir pakāpeniska fiksētas atlīdzības sistēma, kas ir saistīta ar atlīdzības grupu (kā aprakstīts iepriekš), līmenis un darbība no darbinieka tiek piešķirti prognozes pozīcijai, kā arī atlīdzības grupai. Peļņas budžeta izmaksu elements no atlīdzības grupas tiek pievienots prognozes pozīcijai, un tiek izmantota apmaksas likme atlīdzības grupas līmenī un darbībā. 

Opcijas **Piešķirt atlīdzības grupu** iestatīšana ir svarīgāka par opcijas **Budžeta izmaksu elementu piešķiršana** iestatīšanu. Abus iestatījumus var lietot vienlaikus. 

[![Diagramma "Piešķirt atlīdzības grupu"](./media/graphic4.png)](./media/graphic4.png) 

Varat arī piešķirt gadadienas datumu. Atlasītais datums (pielāgotais sākuma datums, darbinieka sākuma datums, nodarbinātības sākuma datums vai darba stāža datums) no piešķirtā darbinieka pēc tam tiek iestatīts kā prognozes pozīcijas gadadienas datums un tiek izmantots informācijai un kad tiek ģenerēti algas pieaugumi.

### <a name="creating-new-forecast-positions"></a>Jaunu prognozes pozīciju izveide

Jaunas prognozes pozīcijas var izveidot divos veidos: kopējot esošo prognozes pozīciju un izveidojot pilnīgi jaunu prognozes pozīciju. 

Kad prognozes pozīcija ir atlasīta, atlasiet **Kopēt atlasīto prognozes pozīciju**, lai izveidotu jaunu prognozes pozīciju, kas ir budžeta stāvoklī **Piedāvātais**. Šai prognozes pozīcijai ir visi tie paši dati kā prognozes pozīcijai, kas tika kopēta, izņemot piešķirto darbinieku un visas piezīmes par budžeta izmaksu elementiem. Ņemiet vērā, ka atbilstošs jauns amats tiek izveidots arī personāla vadībā. Šai pozīcijai ir apraksts par **Izveidot pēc prognozes**. 

Varat arī izveidot pilnīgi jaunu prognozes pozīciju. Atlasiet esošo darbu un atlasiet arī budžeta plānošanas procesu un budžeta plāna scenāriju. Pēc tam varat pievienot citas detaļas, ko vēlaties pievienot. Vēlreiz, jauns amats vienlaicīgi tiek veidots personāla vadībā.

## <a name="working-with-forecast-positions"></a>Darbs ar prognozes pozīcijām
[![Ilustrāciju iezīmēšana "pārveidot prognožu pozīcijas."](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Vairākas prognozes pozīcijas versijas

Jūs varat modificēt prognožu pozīcijas, lai piemērotu zināmas izmaiņas budžeta ciklam vai modelētu ierosinātas izmaiņas. Izplatīta prakse ir izveidot prognožu pozīciju bāzlīnijas kopu vairākas, izveidot to prognožu pozīciju kopijas un pēc tam izmantot šīs kopijas dažādu izmaiņu kopu modelēšanai. Kopijas tiek piešķirtas citam budžeta plāna scenārijam, bet līdz brīdim, kad tiek veiktas izmaiņas, tās ir citāda ziņā identiskas prognozes pozīcijām, no kurām tie ir kopēti. Oriģināli un kopijas koplieto vienu un to pašu pozīciju Personāla vadībā. 

Šo funkcionalitāti nodrošina funkcija **Kopēt scenārijā**. Ņemiet vērā, ka katrai Personāla vadības pozīcijai var būt tikai viena prognozes pozīcija katrā budžeta plāna scenārijā.

### <a name="modifying-forecast-positions"></a>Prognožu pozīciju modificēšana

Izmaiņas, kas veiktas budžeta pozīcijām, ir ierobežotas ar šīm prognožu pozīcijām. Izmaiņas neietekmē amatu ierakstus Personāla vadībā. Lielākā daļa izmaiņu ir ierobežotas arī ar rediģējamo prognozes pozīciju. Citiem vārdiem sakot, izmaiņas attiecas tikai uz budžeta plānošanas procesu un budžeta plāna scenāriju, kuri ir piešķirti. Izņēmumi ir izmaiņas laukos, ko pozīcija koplieto procesos un scenārijos. Šie lauki ietver laukus cilnē **Vispārējā** un cilnē **Finanšu dimensijas**. Kad šie lauki mainās, jaunās vērtības attiecas uz pozīciju visos budžeta plānošanas scenārijos. Tāpēc šie lauki ļauj ātri atjaunināt visas versijas.

#### <a name="budget-cost-elements"></a>Budžeta izmaksu elementi

Budžeta izmaksu elementi sniedz galveno informāciju budžeta plāniem: budžeta summu un galveno kontu. Budžeta summa ir summa, kas tiek nosūtīta uz budžeta plānu, kad plānā tiek iekļauta prognozes pozīcija. Budžeta summa tiek aprēķināta un to nevar mainīt tieši. Šī summa ir gada summa vai gada summas pamata elementu procentuālais aprēķins (kā definēts budžeta izmaksu elementa iestatījumos). Summa pēc tam tiek reizināta ar dienu skaitu elementa datumu diapazonā (no sākuma datuma līdz beigu datumam) un arī pēc **Pilnas slodzes ekvivalenta** (FTE) vērtības prognozes pozīcijai. 

Piemēram, budžeta izmaksu elementa rindai no 2017. gada 1. janvāra līdz 2017. gada 30. jūnijam ikgadējā summa ir 100 000 un FTE vērtība **0,50** tiek aprēķināta kā 100 000 x (181 diena ÷ 365 dienas) x 0,50 = 24 794,52. 

Budžeta izmaksu elementa rindas ir jāpārrēķina, kad FTE vērtība tiek nomainīta prognozes pozīcijā. Rindas ir jāpārrēķina arī, kad mainās aktivizācijas datumi vai aiziešanas pensijā datumi. Izmaiņas šajos datumus var izraisīt budžeta izmaksu elementa sākuma un beigu datumu atjaunināšanu, jo tiem jābūt prognozes pozīcijas datumu diapazonā. Kad pārrēķins ir nepieciešams, kļūst pieejama poga **Pārrēķināt** un tiek parādīts ziņojums "Nepieciešams aprēķins". Pārrēķins vajadzīgs arī tad, ja pievienojat vai noņemat budžeta izmaksu elementu.

**Piemērs** 

Organizācija apsver divas iespējas, kā samazināt grāmatveža pozīcijas izmaksas. Viena iespēja ir izbeigt pozīciju kādā gada daļā. Cita iespēja ir mainīt amatu uz nepilna laika amatu visa gada garumā. Breds ir izveidojis prognozes pozīciju esošajam grāmatveža amatam bāzes scenārijā. Breds kopē šo bāzlīnijas prognozes pozīciju scenārijā A, iestata aiziešanas pensijā datumu uz 31. maiju un pārrēķina. Pēc tam Breds kopē bāzlīnijas prognozes pozīciju scenārijā B, maina FTE vērtību uz **0,50**, un veic pārrēķinu. Tagad Bredam ir trīs versijas, katrai no kurām ir izmaksu kopsummas, kas ir saskaņotas ar iespējam.

#### <a name="assigning-a-compensation-group"></a>Atlīdzības grupas piešķiršana

Pirmoreiz piešķirot atlīdzības grupu prognozes pozīcijai, tiek pievienoti noklusējuma budžeta izmaksu elementi no atlīdzības grupas. Ja izmaksu elementi jau ir piešķirti prognozes pozīcijai, šie izmaksu elementi paliek. Ja atlīdzības grupa jau ir piešķirta un tika mainīta, esošie budžeta izmaksu elementi tiek noņemti un aizstāti ar kopu no atlīdzības grupas. 

Atlasot kompensācijas līmeni un darbību, tiek pievienots ieņēmumu budžeta izmaksu elements (kā noteikts atlīdzības grupā). Gada summa tiek aprēķināta, izmantojot likmi atlasītajā līmenī un darbībā un gada stundas atlīdzības grupā (vai gada algai — visu summu līmenī un darbībā). Un atkal, šī summa tiek reizināta ar izmaksu elementa rindas datumu diapazonu un prognozes pozīcijas FTE vērtību.

#### <a name="generating-increases"></a>Palielinājumu ģenerēšana

Gada pieaugumus (vienu katrā kalendārajā gadā) var izveidot automātiski prognozes pozīcijām, kurām ir piešķirta uz darbību balstīta atlīdzības grupa. Noklikšķiniet uz **Ģenerēt palielinājumus**, lai pievienotu ieņēmumu budžeta izmaksu elementu nākamajā augstākajā darbībā. Jaunu ieņēmumu budžeta izmaksu elementa sākuma datums ir plānotais pieauguma datums, kas tiek rādīts prognozes pozīcijās. Šis datums tiek iestatīts no atlīdzības grupas vienā no diviem veidiem. Ja atlīdzības grupas pieauguma grafiks ir iestatīts uz **Vispārīgais datums**, pieauguma datums tiek norādīts atlīdzības grupā. Ja pieauguma grafiks ir iestatīts uz **Gadadiena**, tiek izmantots gadadienas lauks prognozes pozīcijā un budžeta cikls nodrošina gadu. Ja budžeta ciklā ir vairāki kalendārie gadi, tiek pievienoti vairāki palielinājumi. 

Pašreizējā ieņēmumu budžeta izmaksu elementa beigu datums tiek atjaunināts, izmantojot dienu pirms pieauguma datuma. Pārrēķina process tiek izmantots automātiski, ģenerējot palielinājumus. Tāpēc nav nepieciešams pārrēķināt manuāli. 

Ja noklikšķināsit uz **Ģenerēt palielinājumus** otro reizi, process tiks izpildīts vēlreiz, bet papildu ieraksti netiek pievienoti. Tiek izveidots tikai viens pieaugums kalendārajā gadā.

#### <a name="changes-from-other-pages"></a>Izmaiņas no citām lapām

Atjauninājumi prognožu pozīcijās var arī nākt no citām vietām, piemēram, budžeta izmaksu elementa un kompensācijas grupas iestatījumu lapām. Varat arī modificēt prognožu pozīcijas, izmantojot masveida atjaunināšanas procesu. 

Iestatījumu lapā **Budžeta izmaksu elements** ir pieejamas divas opcijas: **Pievienot pozīcijām** un **Atjaunināt pozīcijas**. Opcija **Pievienot pozīcijām** pievieno budžeta izmaksu elementu atlasītajām prognožu pozīcijām. Ja šis elements jau ir piešķirts prognozes pozīcijai, šī prognozes pozīcija tiek izlaista. Opcija **Atjaunināt pozīcijas** lieto pašreizējās vērtības (galveno kontu, procentiem, gada summu utt.) atlasītajām prognožu pozīcijām. 

Katram procesam ir līdzīga lapa, kur varat atlasīt prognozes pozīcijas. Lapā **Pievienot pozīcijām** tiek parādītas visas prognožu pozīcijas, kas ir pieejamas atlasei, bet lapā **Atjaunināt pozīcijas** tiek parādītas tikai tās prognožu pozīcijas, kurām jau ir piešķirts budžeta izmaksu elements. (Tāpēc lapā **Atjaunināt pozīcijas** varat uzzināt, kurām budžeta pozīcijām jau ir pievienots izmaksu elements.) Lai ietvertu prognozes pozīcijas atjaunināšanā, tās ir jāpārvieto no augšējā režģa uz apakšējo režģi. 

Ņemiet vērā, ka funkcija **Mainīt datumus** cilnē **Izmaksu aprēķins** nekavējoties maina budžeta izmaksu elementa sākuma un beigu datumus prognožu pozīcijās. Atlasāmās opcijas nav pieejamas. 

Lapā **Atlīdzības grupa** funkcija **Atjaunināt pozīcijas likmes** lieto pašreizējās atlīdzības likmes tabulas likmes prognožu pozīcijām, kas ir piešķirtas grupai. Likmes tiek atjauninātas, un papildu izmaksu elementu rindas tiek pievienotas jebkurām jaunām likmju tabulas rindām (pamatojoties uz datumiem). Tomēr budžeta izmaksu elementi un pieauguma datumi netiek atjaunināti. Var atlasīt, kuru budžeta plānošanas procesu un budžeta plāna scenāriju atjaunināt. Tāpēc varat atjaunināt vienu scenāriju, bet atstāt citus scenārijus neizmainītus salīdzināšanas nolūkiem. 

Atlasot prognožu pozīcijas un pēc tam noklikšķinot uz **Masveida atjaunināšana**, var pievienot vai mainīt vairāk nekā vienu budžeta pozīciju vienlaicīgi. Ir pieejamas daudzas opcijas. Viena opcija cilnē **Finanšu dimensijas** nedaudz atšķiras no citām un ir saistīta ar budžeta izmaksu elementiem. Varat pievienot budžeta izmaksu elementus, iestatot opciju **Budžeta noklusējuma vērtības** uz **Jā**. Ja nav atlasīts neviens budžeta izmaksu elements, bet **Budžeta noklusējuma vērtības** ir iestatītas uz **Jā**, tiek noņemti visi budžeta izmaksu elementi, kas pašlaik ir piešķirti. 

Pārrēķina process tiek automātiski izmantots jebkurās izmainītās prognozes pozīcijās.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Prognožu pozīciju ieviešana budžeta plānos

[![Ilustrāciju iezīmēšana "Pievienot budžeta plānam."](./media/graphic6-1024x327.png)](./media/graphic6.png)

Prognožu pozīciju izveides un modificēšanas mērķis ir tās pievienot budžeta plāniem tā, lai budžeta plānos būtu ietvertas visprecīzākās budžeta summas. Pastāv divas metodes, kā pievienot prognožu pozīcijas budžeta plāniem. Var izmantot ģenerēšanas procesu vai atlases procesu budžeta plānā.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Budžeta plāna ģenerēšana no prognozes pozīcijām

Funkcija **Ģenerēt budžeta plānu no prognozes pozīcijām** izveido vai atjaunina budžeta plānus, lai tie būtu budžeta summas un FTE skaiti no prognozes pozīcijām. Budžeta summas no prognozes pozīcijām kļūst par budžeta plāna rindas summām un tiek apkopotas pēc finanšu dimensiju vērtībām un spēkā stāšanās datuma. Ģenerēšanas process piešķir avota prognozes pozīciju budžeta plāna rindai. Lai skatītu pozīciju, varat pievienot prognozes pozīciju kā rindu budžeta plāna izkārtojumā vai izmantot pieprasījumu **Budžeta plāna rindas**. Lai izlaistu šo uzdevumu, iestatiet opciju **Ietvert pozīciju budžeta plāna rindā** uz **Nē**. 

Budžeta plāna FTE scenāriju var atlasīt, lai ietvertu FTE skaitu budžeta plānā. Varat atlasīt tikai daudzuma tipa scenārijus, kas ir iekļauti mērķa budžeta plāna izkārtojumā. Ja atlasāt FTE scenāriju, jānorāda arī FTE galvenais konts. Šis konts tiek izmantots, lai izveidotu daudzuma budžeta plāna rindas. 

Budžeta plānošanas process un budžeta plāna scenārijs, kas atlasīti avotā, nosaka mērķa scenārija budžeta plānošanas procesu un scenāriju. Tā kā šie atribūti ir piešķirti prognožu pozīcijām, tie ir jāsinhronizē budžeta plānā. Tāpēc šos atribūtus nevar rediģēt mērķī. 

Citiem ģenerēšanas procesiem ir pieejamas trīs opcijas:

-   **Izveidot jaunu budžeta plānu** — izveidojiet jaunu plānu, kuram ir atribūti, kas atlasīti sadaļā **Mērķis**.
-   **Aizstāt esošo budžeta plāna scenāriju** — dzēsiet visus datus mērķa budžeta plānā atlasītajā budžeta plāna scenārijā un izveidojiet jaunas rindas, kurās ir atlasītās prognozes pozīcijas dati.
-   **Atjaunināt esošo budžeta plāna scenāriju un pievienot jaunus datus** — atjauniniet esošās rindas mērķa plānā, kas atbilst avota rindām, un pievienojiet arī jaunas rindas jauniem datiem. Atbilstības pamatā ir Virsgrāmatas konts, datums, budžeta klase un citas vērtības, piemēram, prognozes pozīcija. Visas rindas, kurām ir pozīcijas numurs, kas atbilst avota pozīcijas numuram, tiek aizstātas ar jaunām rindām no avota.

### <a name="selecting-forecast-positions"></a>Prognožu pozīciju atlasīšana

Var pievienot arī prognozes pozīcijas budžeta summas tieši budžeta plānam. Izmantojiet funkciju **Pievienot pozīcijas** virs budžeta plāna rindām, lai atlasītu iekļaujamās budžeta pozīcijas. 

Budžeta plāna scenāriji, ko var atlasīt kā avotu, ir ierobežoti ar scenārijiem, kuri ir iekļauti plāna izkārtojumā. Viena opcija cilnē **Mērķis** cilnē ļauj norādīt, ka FTE scenārijs un galvenais konts ir pieejami, lai iekļautu FTE skaitu, tomēr tie nav nepieciešami. 

Šis atlases process darbojas līdzīgi opcijai **Atjaunināt esošo budžeta plāna scenāriju un pievienot jaunus datus** ģenerēšanas procesam. Visas esošās budžeta plāna rindas, kur tiek pievienota prognozes pozīcija, tiek noņemtas un aizstātas ar jaunām rindām, kuru pamatā ir pašreizējais prognozes pozīcijas stāvoklis.

#### <a name="date-options"></a>Datuma opcijas

Ģenerēšanas procesā un atlases procesā sākuma datums budžeta izmaksu elementa rindā nosaka atbilstošā budžeta plāna rindas spēkā stāšanās datumu. Laukā **Sadalījuma metode** budžeta izmaksu elementu iestatīšanas lapā norāda sadalījuma metodi:

-   **Sākuma datums** — budžeta izmaksu elementa sākuma datums tiek izmantots kā budžeta plāna rindas spēkā stāšanās datums.
-   **Ikmēneša** — budžeta summa ir vienmērīgi dalīta ar mēnešu skaitu datumu diapazonā, lai izveidotu tipisku ikmēneša summu, kas tiek piešķirta katra mēneša pirmajā dienā. Ja pirmais periods ir daļējs mēnesis, šī mēneša summa tiek reizināta ar dienu skaitu, kurā izmaksas ir aktīvas tajā mēnesī, un rezultāts tiek piešķirts sākuma datumam. Summa par pēdējo mēnesi ir starpība starp kopējo budžeta summu un visu pārējo mēnešu summu. Tāpēc noapaļošana var ietekmēt pēdējā mēneša summu.
-   **Ceturkšņa** — šī metode ir tāda pati kā **Ikmēneša**, bet šie aprēķini tiek veikti trīs mēnešu periodiem.
-   **Iknedēļas** — loģika līdzinās **Ikmēneša** un **Ceturkšņa** metožu loģikai. Budžeta summa tiek vienmērīgi dalīta ar nedēļu skaitu datumu diapazonā, lai izveidotu tipisku iknedēļas summu, kas tiek piešķirta katras nedēļas pirmajā dienā. Ja pirmais periods ir daļēja nedēļa, šīs nedēļas summa tiek reizināta ar dienu skaitu, kuru izmaksas ir aktīvas tajā nedēļā, un rezultāts tiek piešķirts sākuma datumam. Summa par pēdējo nedēļu ir starpība starp kopējo budžeta summu un visu pārējo nedēļu summu. Tāpēc noapaļošana var ietekmēt pēdējās nedēļas summu.
-   **Divu nedēļu** — šī metode ir tāda pati kā **Iknedēļas**, bet šie aprēķini tiek veikti divu nedēļu periodiem.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Budžeta plāna rindu, kurām ir prognožu pozīcijas, maiņa

Budžeta plāna rindas rāda budžeta summu avotu (prognozes pozīcijas numuru), bet nav saistītas. Tāpēc prognozes pozīcijas izmaiņas netiek parādītas budžeta plāna rindā, un izmaiņas budžeta plāna rindā tiek parādītas prognozes pozīcijā. Ja maināt prognozes pozīciju un vēlaties iekļaut budžeta plānā atjauninājumus, prognozes pozīcija jāiekļauj plānā vēlreiz. Tomēr atcerieties, ka šis process noņem visas rindas, kur šī prognozes pozīcija tiek piešķirta. Tāpēc jebkuras izmaiņas, kuras veicāt šajās rindās, tiek noņemtas. 

Lai redzētu, kuros budžeta plānos prognozes pozīcija tika iekļauta, jūs varat ģenerēt pārskatu **Prognozes pozīcijas pēc budžeta plāna**. Vai arī prognozes pozīcijā varat atvērt papildinformāciju **Saistītie budžeta plāni**, lai apskatītu plānus.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
