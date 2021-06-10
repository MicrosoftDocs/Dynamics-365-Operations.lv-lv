---
title: Tehniskās versijas un tehnisko preču kategorijas
description: Šajā tēmā ir sniegta informācija par tehnisko versiju koncepciju. Tehniskās versijas nodrošina, ka dažādi produkta stāvokļi un to dati tiek saglabāti un dzēsti, un tos var vizualizēt sistēmā.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3509763c03ecc0e847c72828d14b172401df75b0
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115149"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Tehniskās versijas un tehnisko preču kategorijas

[!include [banner](../includes/banner.md)]

Tehniskie produkti attīstās to produktu dzīves cikla laikā daudzu iemeslu dēļ. Piemēram, var tikt ieviestas izmaiņas, lai uzlabotu produktu funkcionālo darbību, mainīt komponentu, jo piegādātājs vairs to nepiedāvā, reaģēt uz jauniem atklājumiem vai labot kļūdas sākotnējā dizainā. Ir arī daudz iemeslu, kāpēc šīs izmaiņas ir jāuzglabā kā daļa no notiekošā produkta, tādā veidā, ka iepriekšējie dati netiek pārrakstīti. Tālāk ir norādītas dažas no šiem iemesliem.

- Jūs vēlaties izsekot, kā produkts ir ražots un piegādāts jūsu klientiem iepriekšējos dzīves cikla stāvokļos.
- Pirms izmaiņu apstiprināšanas un piemērošanas ir nepieciešams izpildes laiks.
- Jūs vēlaties, lai katrai izmaiņai būtu laikspiedols, un vēlaties, lai iepriekš izgatavotos produktus varētu piegādāt atsevišķi.

*Tehniskās versijas* nodrošina, ka dažādi produkta stāvokļi un to dati tiek saglabāti un dzēsti, un tos var vizualizēt sistēmā. Šī koncepcija palīdz uzturēt konsekvenci, bloķēt materiālu komplektu (MK) ražošanai, likvidēt mainīgumu un viegli identificēt izmaiņas.

Parasti tiek lietota kārtula *forma-atbilstība-funkcija*, lai noteiktu, vai izmaiņām ir nepieciešams jauns produkts, jauna versija vai esošas versijas atjauninājums. Katrs no šiem trim terminiem šīs kārtulas nosaukumā attiecas uz noteiktu daļas aspektu, kas palīdz inženieriem saskaņot daļas ar vajadzībām. Kārtula forma-atbilstība-funkcija palielina dizaina izmaiņu elastību, jo, lai mainītu daļu, ir nepieciešama minimāla dokumentācija un dizaina izmaksas, ar nosacījumu, ka tiek uzturēta produkta piemērotība, forma un funkcija.

- **Atbilstība** attiecas uz daļu vai līdzekli, ar kuru veidot savienojumu, savienoties ar vai pievienoties citam līdzeklim, vai arī daļai no montāžas. Atbilstība ļauj daļai atbilst vajadzīgajām montāžas pielaidēm, lai tā varētu būt noderīga.
- **Forma** attiecas uz daļas vai montāžas raksturlielumiem, piemēram, ārējiem izmēriem, svaru, izmēru un vizuālo izskatu. Forma ir aspekts, ko visvairāk ietekmē inženiera estētiskā izvēle. Tā ietver korpusu, šasiju un vadības paneli, kas kļūst par produkta ārējo "seju".
- **Funkcija** ir kritērijs, kas tiek ievērots, kad daļa efektīvi un droši veic tās noteikto mērķi. Piemēram, elektronikas produktā funkcija var būt atkarīga no izmantotajiem cietvielu komponentiem un programmatūras vai aparātprogrammatūras. Bieži tas var būt atkarīgs arī no izvēlētā pievienojuma funkcijām. Divi visbiežāk sastopamie iemesli, kāpēc pievienojums var neizdoties funkciju kritērijos ir slikti novietoti vai slikti noslogoti porti un maldinošas vai trūkstošas etiķetes. 

## <a name="engineering-versions"></a>Tehniskās versijas

Kad izmantojat tehniskos produktus, katram produktam ir vismaz viena tehniskā versija. Veidojot tehnisko produktu, sākotnējā tehniskā versija tiek izveidota automātiski. Katra tehniskā versija saglabā šai versijai raksturīgos tehniskos datus. Tālāk ir sniegti daži šādu datu piemēri:

- Versijas numurs un iepriekšējās versijas numurs (ja piemērojams)
- Spēkā stāšanās datums un beigu datums
- Produkta versijas aktīvais statuss, kas norāda, vai versiju var izlaist un izmantot dirījumiem (papildu informācijai skatiet [Produkta gatavība](product-readiness.md) .)
- Inženiertehniskais uzņēmums, kas izveidoja produktu un kam pieder produkts (Plašāku informāciju skatiet [Tehnisko uzņēmumu un datu īpašumtiesību kārtulas](engineering-org-data-ownership-rules.md).)
- Saistītie tehniskie dokumenti, piemēram, montāžas rokasgrāmata, lietotāja instrukcijas, attēli un saites
- Tehniskie atribūti (Plašāku informāciju skatiet sadaļā [Tehniskie atribūti un tehnisko atribūtu meklēšana](engineering-attributes-and-search.md).)
- Materiālu komplekts (MK) inženiertehniskajām precēm
- Procesa ražošanas preču formulas
- Tehnisko MK maršruti

Šos datus var atjaunināt esošajā versijā vai izveidot jaunu versiju, izmantojot *tehnisko izmaiņu pasūtījumu*. (Papildu informāciju skatiet [Pārvaldiet tehnisko produktu izmaiņas](engineering-change-management.md).) Ja izveidojat jaunu produkta versiju, sistēma kopē visus ar tehniskajiem datiem saistītos datus jaunajai versijai. Pēc tam varat modificēt datus šai jaunajai versijai. Šādā veidā var izsekot konkrētus datus katrai secīgai versijai. Lai salīdzinātu atšķirības starp secīgām tehniskajām versijām, pārbaudiet tehnisko izmaiņu pasūtījumu, kas ietver izmaiņu veidus, kas norāda visas izmaiņas.

Kā jau teikts, veidojot tehnisko produktu, sākotnējā tehniskā versija tiek izveidota automātiski. Šīs versijas versijas numurs atbilst versijas numura kārtulai, kas definēta ša produkta tehniskajā kategorijā. Lai pārietu uz nākamo versiju, produkts ir jāpievieno tehnisko izmaiņu pasūtījumam kā rinda, un lauku **Ietekme** ir jāiestata uz *Jauna versija*. Tehnisko izmaiņu pasūtījumā tiks iekļauta detalizēta informācija par pašreizējās versijas izmaiņām nākamajā versijā.

Ņemiet vērā, ka tehniskais produkts vienlaicīgi var būt tikai vienā tehnisko izmaiņu pasūtījumā. Šis ierobežojums nodrošina datu precizitāti un palīdz novērst pārklāšanos vai pretrunīgas izmaiņas produktā. Ievērojiet arī, ka lauks **Inženieris** tehnisko izmaiņu pasūtījuma skatā **Virsraksts** tiek parādīts inženieris, kas atbild par tehnisko izmaiņu pasūtījumu. Ja inženieris pieder komandai, kas definēta sistēmā, lauks **Atbildīgais** parāda šīs grupas vadītāju.

## <a name="track-versions-in-transactions"></a>Izsekošanas versijas darījumos

Kad izmantojat tehnisko izmaiņu pārvaldību, jūsu preces šablona dati vienmēr ietver vienu vai vairākas tehniskās versijas. Uzstādot tehniskos produktus, varat izvēlēties, vai tehniskā versija arī ir daļa no *loģistikajiem darījumiem*. (Papildinformāciju skatiet sadaļu [Iestatiet tehnisko produktu kategorijas](#product-category) tālāk šajā tēmā.) Ja loģistikas ietekme ir nozīmīga, tā atšķiras atkarībā no produkta un uzņēmuma. Dažreiz tiek izmantota tikai pēdējā produkta versija. Tāpēc, kad tiek ieviesta jauna versija, iepriekšējo versiju vairs nevar izmantot. Citos gadījumos ir nepieciešama iepriekšējā versija loģistikas darījumos, lai pārvarētu šādus izaicinājumus:

- Loģistikas struktūrvienībai ir jānosūta divi produkta gabali klientam. Šādā gadījumā ir jāizlemj, vai vēlaties vai ļausiet nosūtīt divas atšķirīgas versijas.
- Vēlāk tiek atklāts, ka rodas problēma un vai tā ir saistīta ar konkrētām izmaiņām. Šādā gadījumā var būt noderīgi precīzi noteikt, kura versija tika nosūtīta katrā pasūtījumā.
- Uzņēmumi parasti vēlas nosūtīt vecās versijas vispirms, lai izņemtu tās no krājumiem. Jo īpaši zemas kvalitātes produktiem šo pieeju bieži var pārvaldīt, nosakot jaunās versijas efektivitāti, kas saistīta ar prognozēm par to, kad vecās versijas krājums tiks noplicināts. Tomēr dažreiz, iespējams, nevar veikt šo salīdzināšanu, vai arī jūs varat uzskatīt, ka krājumu līmeņa prognožu nenoteiktība ir pārāk augsta.

Lēmums par to, vai padarīt versijas redzamas krājumos, ir atkarīgs no iepriekš minētajiem faktoriem, kā arī no uzņēmuma prakses un citiem apsvērumiem, kas raksturīgi katram uzņēmumam. Varat norādīt *tehnisko produktu kategorijas* izturēšanos. Pēc tam tas tiks attiecināts uz visiem produktiem, kas izveidoti no šīs kategorijas, visiem uzņēmumiem, kam produkts tiek izlaists.

Produkti, kas ir iestatīti tā, lai tiem būtu loģistikas ietekme, katram darījumam ir jānorāda tehniskā versija. Lai gan sistēma piedāvās *visjaunāko aktīvo versiju*, varat atlasīt no visām aktīvajām versijām, kas ir pieejamas uzņēmumam. Produkti, kas ir iestatīti tā, lai tiem nebūtu loģistikas ietekmes, darījumiem nav jānorāda tehniskā versija. Tomēr sistēma izmanto visjaunāko aktīvo versiju. Piemēram, pievienojot produktu ražošanas MK, tiks izmantota jaunākā versija un, palaižot vispārējo plānošanu, tiks pieņemta jaunākā versija.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Iestatīt tehnisko produktu kategorijas

Tehnisko produktu kategorija sniedz pamatu noteikta tehniskā produkta izveidei. Katra kategorija izveido noklusējuma vērtību un politiku kopu. Tāpēc, veidojot tehnisko produktu, vispirms atlasiet kategoriju, no kuras to izveidot.

Ņemiet vērā, ka jauns kategoriju hierarhijas veids (*tehnisko produktu hierarhija*) tiek iestatīts automātiski. Kategorijas varat izveidot manuāli, pārejot uz **Tehniko izmaiņu pārvaldība \> Iestatīšana \> Detalizēta informācija par tehnisko produktu kategoriju**.

Katra tehnisko produktu kategorija nosaka to tehnisko produktu noklusējuma uzvedību, kuri ir izveidoti, pamatojoties uz šo kategoriju. Pēc tam, kad ir izveidots tehniskais produkts, jūs nevarat mainīt tā tehnisko produkta kategoriju. Tomēr, ja atlasāt nepareizo kategoriju, varat dzēst produktu un pēc tam to izveidot atkārtoti.

Kad tiek izveidota tehisko produktu kategorija, nevar mainīt šādus iestatījumus:

- Inženiertehniskais uzņēmums
- Preces veids
- Preces apakštips
- Preces dimensijas grupa
- Konfigurēšanas tehnoloģija
- Versijas numura kārtula

Citi iestatījumi var pārmantot noklusētās vērtības, kas iestatītas tehnisko produktu kategorijai. Tomēr, saskaņā ar sistēmas kārtulām, šīs vērtības var mainīt.

Lai strādātu ar tehnisko produktu kategorijām, dodieties uz **Tehniko izmaiņu pārvaldība \> Iestatīšana \> Detalizēta informācija par tehnisko produktu kategoriju**. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai izveidotu jaunu kategoriju, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai rediģētu esošu kategoriju, atlasiet to saraksta rūtī, atlasiet **Jauns** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai dzēstu esošu kategoriju, atlasiet to saraksta rūtī un pēc tam darbības rūtī atlasiet vienumu **Dzēst**.

### <a name="header"></a>Galvene

Iestatiet tālāk norādītos laukus preces tehniskās kategorijas virsrakstā.

| Lauks | Apraksts |
|---|---|
| Vārds, uzvārds | Ievadiet tehnisko produktu kategoriju. |
| Inženiertehniskais uzņēmums | Atlasiet inženiertehnisko uzņēmumu, kurā var izveidot šīs tehnisko produktu kategorijas un kur tās tiks uzturētas. |

### <a name="details-fasttab"></a>Detalizētas informācijas kopsavilkuma cilne

Iestatiet tālāk norādītos laukus preces tehniskās kategorijas kopsavilkuma cilnē **Detalizēta informācija**.

| Lauks | Apraksts |
|---|---|
| Preces veids | Atlasiet, vai kategorija attiecas uz produktiem vai pakalpojumiem. |
| Ražošanas veids | Šis lauks parādās tikai tad, ja esat iespējojis [formulu izmaiņu pārvaldību](manage-formula-changes.md) jūsu sistēmā. Atlasiet ražošanas tipu, uz kuru attiecas šī inženiertehniskā preču kategorija:<ul><li>**Plānošanas krājums** - izmantojiet šo inženiertehnisko kategoriju, lai paveiktu formulas izmaiņu pārvaldību plānošanas krājumiem. Plānošanas krājumiem tiek lietotas formulas. Tie ir līdzīgi formulas krājumiem, taču tos izmanto, lai ražotu tikai līdzproduktus un blakusproduktus, bet ne pabeigtās preces. Formulas tiek lietotas ražošanas procesa laikā.</li><li>**MK** – izmantojiet šo inženiertehnisko kategoriju, lai pārvaldītu tehniskās preces, kuras neizmanto formulas, un parasti (bet ne vienmēr) ietver MK.</li><li>**Formula** - izmantojiet šo inženiertehnisko kategoriju, lai paveiktu formulas izmaiņu pārvaldību pabeigtajām precēm. Šiem krājumiem būs formula, bet ne MK. Formulas tiek lietotas ražošanas procesa laikā.</li></ul> |
| Pieļaujamais svars | Šī opcija parādās tikai tad, ja esat iespējojis [formulu izmaiņu pārvaldību](manage-formula-changes.md) jūsu sistēmā. Tas ir pieejams tikai tad, ja lauks **Ražošanas tips** ir iestatīts uz *Plānošanas krājums* vai *Formula*. Iestatiet šo opciju uz *Jā*, ja izmantosit šo inženiertehnisko kategoriju, lai pārvaldītu krājumus, kuriem ir nepieciešams atbalsts pieļaujamam svaram. |
| Izsekošanas versijas darījumos | Atlasiet, vai produkta versijai ir jābūt apzīmogotai visiem darījumiem (loģistikas ietekme). Piemēram, ja izsekojat versiju darījumos, katrs pārdošanas pasūtījums parāda, kura konkrētā produkta versija tika pārdota šajā pārdošanas pasūtījumā. Ja versija netiek izsekota darījumos, pārdošanas pasūtījumi nerādīs, kura konkrētā versija tika pārdota. Tā vietā tie vienmēr rāda jaunāko versiju.<ul><li>Ja šī opcija ir iestatīta uz *Jā*, produktam tiek izveidots preces šablons, un katra produkta versija būs variants, kas izmanto *versijas* produkta dimensiju. Lauks **Produkta apakštips** tiek automātiski iestatīts uz *Preces šablons*, un laukā **Preces dimensijas grupa** jums ir jāatlasa produkta dimensiju grupa, kur *versijas* dimensija ir aktīva. Tiks attēlotas tikai tās produkta dimensiju grupas, kurās *versija* ir aktīva dimensija. Varat izveidot jaunas produkta dimensiju grupas, atlasot pogu **Rediģēt** (zīmuļa simbols).</li><li>Ja šī opcija ir iestatīta uz *Nē*, *versijas* produkta dimensija netiks izmantota. Pēc tam varat izvēlēties, vai izveidot produktu vai preces šablonu, kas izmanto citas dimensijas.</li></ul><p>Šī opcija bieži tiek izmantota produktiem, kuriem ir izmaksu atšķirība starp versijām, vai produktiem, kuriem attiecībā uz klientu tiek piemēroti atšķirīgi nosacījumi. Tāpēc ir svarīgi norādīt, kura versija tika izmantota katrā darījumā.</p> |
| Preces apakštips | Atlasiet, vai kategorija atradīs preces vai preces šablonus. Preču šabloniem tiks lietotas preču dimensijas.
| Preces dimensijas grupa | Iestatījums **Atsekošanas versijas darījumos** palīdz izvēlēties produkta dimensijas grupu. Ja norādītajā vēlaties izsekot versijas darījumiem, tiks rādītas tās produktu dimensiju grupas, kurās tiek izmantota *versijas* dimensija. Pretējā gadījumā tiks attēlotas tikai tās produkta dimensiju grupas, kurās *versijas* dimensija netiek izmantota. |
| Preces dzīves cikla stāvoklis izveides laikā | Iestatiet noklusējuma produktu dzīves cikla stāvokli, kas nepieciešams, kad tas tiek izveidots pirmo reizi. Papildinformāciju skatiet šeit: [Produktu dzīves cikla stāvokļi un darījumi](product-lifecycle-state-transactions.md). |
| Versijas numura kārtula | Atlasiet versijas numura kārtulu, kas attiecas uz kategoriju:<ul><li>**Manuāli** — katrai jaunajai versijai izvēlieties versijas numuru.</li><li>**Automātiski** — sistēma iestata versijas numuru, pamatojoties uz jūsu definēto formātu. Iestatot formātu, izmantojiet numura zīmi (\#) tā , lai tā norādītu ciparu un jebkuru citu rakstzīmi, lai attēlotu konstantu vērtību. Piemēram, definējot formātu kā *V-\#\#*, pirmā versija būs "V-01", otrā versija būs "V-02", un tā tālāk.</li><li>**Saraksts** — sistēma paņem nākamo numuru no iepriekš definēto pielāgoto vērtību saraksta.</li></ul> |
| Īstenot spēkā stāšanos | Atlasiet, vai tehnisko versiju efektivitāti datumiem jābūt blakusesošiem, vai var būt pārtraukumi un pārklāšanās. Šis iestatījums ietekmē veidu, kādā varat izmantot laukus **Spēkā no** un **Spēkā līdz** katrai tehniskajai versijai, uz kuru attiecas kategorija.<ul><li>Ja šī opcija ir iestatīta uz *Jā*, katrai versijai ir jānorāda **Spēkā no** vērtība, un starp versijām nav pieļaujami ne pārklājumi, ne pārrāvumi. Katras hehniskās versijas datumu diapazons ir tieši saistīts ar iepriekšējām un nākamajām tehniskajām versijām, ja tādas ir. Šādā gadījumā visjaunākā versija tiek izmantota vienmēr, un vecākas versijas vairs netiek lietotas.</li><li>Ja šī opcija ir iestatīta uz **Nē**, tehniskajām versijām nav ierobežojumu attiecībā uz efektivitāti, un ir atļauti gan pārklājumi, gan pārrāvumi. Šādā gadījumā vienlaicīgi var būt aktīvas vairākas versijas, un var strādāt ar jebkuru aktīvu versiju.</li></ul><p>Šī opcija ietekmē arī MK un maršrutus, kas ir saistīti ar produkta versiju. Plašāku informāciju skatiet šīs tēmas sadaļā [Izveidot savienojumu ar MK un maršrutiem tehniskajām versijām](#boms-routes).</p> |
| Lietot numura kārtulas nomenklatūru | Iestatiet šo opciju kā *Jā*, lai iespējotu produkta numura definēšanas kārtulas, izmantojot numuru sērijas, tehnisko atribūtu nosaukumus un vērtības un teksta konstantes kā segmentus. Lai izveidotu vai modificētu kārtulas, atlasiet pogu **Rediģēt**. |
| Lietot nosaukuma kārtulas nomenklatūru | Iestatiet šo opciju kā *Jā*, lai iespējotu kārtulas nosaukuma definēšanai, izmantojot tehnisko atribūtu nosaukumus, tehnisko atribūtu vērtības un teksta konstantes kā segmentus. Lai izveidotu vai modificētu kārtulas, atlasiet pogu **Rediģēt**. |
| Lietot apraksta kārtulas nomenklatūru | Iestatiet šo opciju kā *Jā*, lai iespējotu kārtulas apraksta definēšanai, izmantojot tehnisko atribūtu nosaukumus, tehnisko atribūtu vērtības un teksta konstantes kā segmentus. Lai izveidotu vai modificētu kārtulas, atlasiet pogu **Rediģēt**. |

### <a name="attributes-fasttab"></a>Atribūtu kopsavilkuma cilne

Kopsavilkuma cilnē **Atribūti** izmantojiet režģi, lai iestatītu tehniskos atribūtus, kas attiecas uz šai kategorijai piederošajiem produktiem. Informāciju par to, kā izveidot tehniskos atribūtus skatiet sadaļā [Tehniskie atribūti un tehnisko atribūtu meklēšana](engineering-attributes-and-search.md).

Izmantojiet pogu kopsavilkuma cilnē **Atribūti**, lai režģī pievienotu, noņemtu un kārtotu atribūtus.

Ja maināt atribūtu atlasi tehniskajai kategorijai un jau pastāv produkti, kuru pamatā ir šī kategorija, jums jāizlemj, vai lietot izmaiņas šajos produktos. Ja vēlaties, lai esošie produkti atspoguļotu izmaiņas, atlasiet **Atjaunināt esošos produktus** kopsavilkuma cilnē **Atribūti**.

Katrai rindai, kuru pievienojat režģim, iestatiet tālāk norādītos laukus.

| Lauks | Apraksts |
|---|---|
| Vārds, uzvārds | Atlasiet pievienojamo atribūtu. |
| Vērtība | Atlasiet atribūta noklusējuma vērtību. |
| Obligāts | Atribūtiem *Būla* veida, ja šī opcija ir iestatīta uz *Jā*, lietotājiem ir jāiestata atribūts *Jā*. Ja šī opcija ir iestatīta uz *Nē*, lietotāji var iestatīt atribūtu vai nu uz *Jā* vai uz *Nē*. Citiem datu veidiem šīs opcijas iestatījums ir tikai informatīvs. |
| Partijas atribūts | Atlasiet, vai atribūts jāizplata, izmantojot partijas funkcionalitāti. |

### <a name="readiness-policy-fasttab"></a>Gatavības politikas kopsavilkuma cilne

Lietojiet lauku **Precu gatavības politika**, lai atlasītu gatavības politiku, kam vajadzētu attiekties uz šai inženiertehniskajai kategorijai piederošajām precēm. Papildinformāciju skatiet sadaļā [Produktu gatavība](product-readiness.md).

> [!NOTE]
> **Preču gatavības politikas** lauks nedaudz atšķiras, ja sistēmā ir ieslēgta *Preču gatavības pārbaudes* funkcija. (Šī funkcija ļauj piemērot gatavības politiku standarta precēm, kas \[nav inženiertehniskās\] preces). Papildinformāciju skatiet [Gatavības politiku piešķiršana standarta un inženiertehniskajām precēm](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Laidiena politikas kopsavilkuma cilne

Lietojiet lauku **Produktu laidiena politika**, lai atlasītu laidiena politiku, kas attiecas uz šai kategorijai piederošajiem produktiem. Plašāku informāciju skatiet sadaļā [Izlaist produkta struktūras](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>MK un maršrutu pievienošana tehniskajām versijām

Iestatījums **Ieviest efektivitāti** ir svarīgs MK un maršrutu savienojumam ar katru tehnisko versiju. Varat aktivizēt vairākus MK vai maršrutus katram produktam tikai tad, ja ir atšķirība kādā no šiem iestatījumiem:

- Preces dimensija
- Daudzums
- Vieta
- Efektivitātes datumi

Tehniskie MK un maršruti tiek veidoti no tehniskās versijas, kur tie tiek piemēroti. Tās var atpazīt, atzīmējot izvēles rūtiņu **Tehniskā kontrole**. Strādājot ar tehniskajiem MK un maršrutiem, parasti tos neprojektē, lietojot dažādus daudzumus. Parasti katrai vietai arī netiks projektēti dažādi MK. Turklāt attiecībā uz tehniskajiem MK un maršrutiem, efektivitātes datumi vienmēr tiek ņemti no tehniskās versijas. Tāpēc tehniskajai versijai, tās MK un maršrutam būs vienādi efektīvitātes datumi.

Produktiem, kuros tiek izmantota *versijas* produkta dimensija (kopā ar loģistikas ietekmi uz darījumiem), versija tiek pievienota arī MK un maršrutiem. Šī darbība palīdz diferencēt MK un secīgu versiju maršrutus neatkarīgi no iestatījuma **Ieviešanas efektivitāte**.

Produktiem, kuros netiek izmantota *versijas* produkta dimensija (bez loģistikas ietekmes uz darījumiem), versija netiek pievienota arī MK vai maršrutiem. Tāpēc nebūs atšķirības starp MK un secīgu versiju maršrutiem. Šādā gadījumā ir ieteicams iestatīt opciju **Ieviest efektivitāti** uz *Jā*. Šādā veidā varat novērst tehnisko versiju pārklāšanos un aktivizēt arī jaunākās versijas MK un maršrutu, neveicot iepriekšējās versijas MK un maršruta deaktivizēšanu. Ja opcija **Ieviest efektivitāti** ir iestatīta uz *Jā*, šādā gadījumā, lai varētu aktivizēt jaunāko versiju, manuāli jāinaktivē iepriekšējo versiju MK un maršruti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
