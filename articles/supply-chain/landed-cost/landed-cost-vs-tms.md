---
title: Kopējās izmaksas pret Transportēšanas pārvaldību
description: Korporācija Microsoft Dynamics 365 Supply Chain Management nodrošina divus dažādus moduļus darbam ar transportēšanas, Transportēšanas pārvaldību (TMS) un Kopējām izmaksām. Šajā tēmā apkopota funkcionalitāte, kas šiem diviem moduļiem ir kopēja, un iezīmētas to atšķirības.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8c59d7d1887986d308cb591ece077cff9f4648a5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690391"
---
# <a name="landed-cost-vs-transportation-management"></a>Kopējās izmaksas pret Transportēšanas pārvaldību

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management nodrošina divus dažādus moduļus darbam ar transportēšanu: **Transportēšanas pārvaldību** (TMS) un **Kopējām izmaksām**. Šajā tēmā apkopota funkcionalitāte, kas šiem diviem moduļiem ir kopēja, un iezīmētas to atšķirības. Šo informāciju iespējams izmantot, lai izlemtu, kurš modulis vislabāk atbilst jūsu uzņēmējdarbības praksei. Varat atrast, ka dažas uzņēmējdarbības prakses darbojas labāk ar TMS, turpretim citas darbojas vislabāk ar kopējām izmaksām. Pēc tam atkarībā no uzņēmējdarbības vajadzībām var izvēlēties izmantot tikai vienu moduli vai kombinēt šos divus moduļus.

Šī tēma nav visaptverošs pārskats par visām jebkura moduļa funkcijām. Tā vietā tā iezīmē pieejamo funkcionalitāti, kā tā attiecas uz preču transportēšanu no kreditora uz jūsu biznesa noliktavu, kur to var patērēt.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminoloģija, atsauces dati un pārskatu atšķirības

### <a name="terminology-comparison"></a>Terminoloģijas salīdzinājums

TMS un Kopējās izmaksas izmanto dažādus termiņus līdzīgām koncepcijām. Tabulā ir apkopoti šie termini un to izmantošana šajos divos moduļos.

| TMS termiņš | Kopējo izmaksu termiņš | Piezīmes |
|----------|------------------|-------|
| **Ielādēt**<p>*Krava* ir kravu apkopojums, kas vienlaicīgi tiek transportēts uz vienas transportēšanas vienības (piemēram, kravas automašīna vai nosūtīšana). Kravas var būt ienākošās vai izejošās.</p> | **Reiss**<p>Parasti *reiss* ir viens kuģis, kas dodas vienā *ceļojuma* laikā. Reisā var būt vairāki *nosūtīšanas konteineri*, un tajā var būt iekļauti arī ienākošie pasūtījumi no dažādām jūsu organizācijas juridiskajām personām. Reisi var būt tikai ienākošie.</p> | TMS izmanto arī termina *reisa numuru*, kas attiecas uz informācijas lauku, kur varat ievadīt identifikatoru. Tomēr funkcionalitāte nav saistīta ar TMS lauku, un tā nav saistīta ar *reisa* koncepciju Kopējās izmaksās. |
| **Maršruts**<p>*Maršruts* ir fizisks transportēšanas ceļš no izcelsmes uz galamērķi.</p> | **Maršruts**<p>*Ceļojums* ir fizisks transportēšanas ceļš no izcelsmes uz galamērķi. Katrs reiss ir jāpiešķir ceļojumam.</p> | |
| **Maršruta segmenti**<p>Maršrutam var būt vairāki *maršruta segmenti*, katrs no tiem pārstāv ceļojuma soli. Maršrutā var būt iekļauti vairāki pārvadātāji vai pakalpojumi, no kuriem katrs tiek uzskatīts par maršruta segmentu.</p> | **Fāzes**<p>Maršrutam var būt vairākas *fāzes*, katra no tām pārstāv ceļojuma soli. Fāze var būt daļa no transportēšanas, nodokļu apstrādes vai citas aktivitātes.</p> | |
| **Konteineri**<p>*Konteiners* var būt jebkura veida iepakojums vai iepakojums, ko izmanto TMS.</p> | **Nosūtīšanas konteineri**<p>*Pārvadāšanas konteiners* ir burtisks fiziskas pārvadāšanas konteiners, ko zināms no konteinera piegādātajiem konteineriem.</p> | |
| **Preču kodi**<p>TMS (un citās vietās Supply Chain Management) *preču kodi* identificē preces tipus. Tās var ietekmēt tarifus, bīstamu materiālu apstrādi u.c.</p> | **Preču kodi**<p>Kopējās izmaksās *preču kodi* tiek izveidoti juridiskas personas līmenī. Pamatā tās tiek izmantotas tikai pārskatu veidošanai.</p> | Kopējās zemes izmaksas var izmantot arī preču kodus, kas tiek izmantoti TMS un citām Supply Chain Management vietām. Tomēr, Kopējo izmaksu preču kodi tiek izmantoti tikai ar Kopējām izmaksām. |

### <a name="some-reference-data-isnt-shared"></a>Daži atsauces dati netiek koplietoti

TMS un Kopējās izmaksas nekopīgo atsauces datus tādām entītijām kā izmaksu iestatīšana, ceļojumi un fāzes. Ja izmantojat abus moduļus, atkārtoti jāizveido nekopīgotie atsauces dati.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Starpuzņēmumu pārskati nedarbojas tranzīta precēm

Tālāk pārskati nedarbojas kopā ar tranzīta precēm, ko nodrošina Kopējās izmaksas:

- [Starpuzņēmumu tranzītpreču kopsummu pārskats](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Starpuzņēmumu tranzītpreču kopsummu pārskats](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Šie pārskati pieņem, ka preces tiek nodotas tranzītā, tiklīdz tiek izsniegts pārdošanas pavadzīme un ka tās tiek ņemtas inventāra sarakstā no tranzīta saņemšanas brīdī. Tomēr tranzīta preces netiek apstrādātas šādā veidā. Tāpēc, ja izmantojat preces tranzītā un starpuzņēmumu darbībās kopā, šo abu pārskatu rezultāti būs nepareizi.

## <a name="using-the-two-modules-together"></a>Abu moduļu izmantošana kopā

TMS var izmantot gan ienākošajām, gan izejošām operācijām. Kaut arī Kopējās izmaksas nodrošina lielāko daļu no tās pašas pamata funkcionalitātes, kas TMS saņemšanas darbībām, tās arī pievieno dažas funkcionalitātes. Tāpēc, iespējams, vēlēsieties izmantot TMS nosūtīšanas operācijām un Kopējās izmaksas saņemšanas operācijām.

Parasti nav ieteicams izmantot abus moduļus vienlaikus saņemšanas operācijām. Jums vajadzētu izmantot moduli, kas vislabāk atbilst jūsu prasībām. Ja šos divus moduļus izmantojat kopā, tiem nevajadzētu koplietot pirmdokumentus. Piemēram, neizmantojiet vienu un to pašu pirkšanas pasūtījumu gan kravai TMS, gan reisam kopējās izmaksās. It īpaši ir jānodrošina, lai sistēma nebūtu iestatīta izveidot ienākošo kravu automātiski. Ja krājumi no pirkšanas pasūtījumiem ir iekļauti reisā, tos nevar apstrādāt kā daļu no kravas.

## <a name="goods-in-transit"></a>Tranzītpreces

Viena no kopējo izmaksu primārajām funkcijām ir spēja apstrādāt preces tranzītā. Tranzītapstrādes preces ļauj jums paņemt finansiālas īpašumtiesības par nosūtītajām precēm, pirms tās tiek fiziski saņemtas mērķa noliktavā. Tranzīta preču apstrāde bieži vien ir nepieciešama starptautiskajai tirdzniecībai.

### <a name="tms-goods-in-transit-features"></a>TMS tranzīta preču funkcijas

TMS pašlaik neatbalsta tranzīta preču apstrādi.

### <a name="landed-cost-goods-in-transit-features"></a>Kopējās izmaksas tranzīta preču funkcijām

Tranzītapstrādes preces ir galvenā Kopējo izmaksu funkcija un nodrošina šādu funkcionalitāti:

- **Preces tranzīta noliktavās** – Preces tranzīta noliktavā var tikt saistītas ar katru Supply Chain Management noliktavu. Pēc sākotnējā pirkšanas pasūtījuma rēķina nosūtīšanas preces tiek pārsūtītas uz tranzīta noliktavām. Krājumi, kas ir fiziski rezervēti, tajā kļūst pieejami patēriņam, kamēr tie nav saņemti to fiziskajā noliktavā. Tāpēc, izrakstot rēķinu par pirkšanas pasūtījumu, varat saņemt finanšu īpašumtiesības precēm.
- **Preces tranzīta virsgrāmatas kontā** – zemes izmaksas pievieno specifisku virsgrāmatas grāmatošanas kontu pirkšanas pasūtījuma grāmatošanas metodei, lai apstrādātu preces tranzītā. Šīs preces tranzīta virsgrāmatas kontā darbojas kā "rēķinā ne iekļautās preces" tipa konts. Kad oriģinālā pirkšanas pasūtījuma rēķins ir izrakstīts un ir izveidotas tranzītpavešanas preces, tiešā pirkšanas pasūtījuma izmaksas tiek grāmatotas tranzītā virsgrāmatas kontā līdz preču galīgās fiziskās saņemšanas vietā.
- **Izsekošanas kontroles atjauninājumi** – tranzītpasūtījumu preces atbalsta izsekošanas kontroles funkcionalitāti kopējās izmaksās. Izsekošanas kontrole ļauj atjaunināt paredzamo preču saņemšanas datumu, kamēr tie ir tranzītā. Izsekošanas kontrole tad atjaunina reisu un saistītās pirkšanas pasūtījuma rindas. Plānotais piegādes datums pēc tam ir pieejams vispārējai plānošanai un loģistikai.
- **Piegādāto/nepiegādāto darījumu aktivizēšana** – ja starp paredzamajām precēm reisa līnijā un faktiskajām noliktavā saņemtajām precēm rodas novirze, zemes izmaksas to atrisina, izveidojot piegādātos un/vai nepiegādātos darījumus. Pēc tam šīs darbības var pārvaldīt, balstoties uz to, ka vēlaties tās apstrādāt, izmantojot pirkšanas pasūtījumu vai kustības žurnālu. Veiktās un neveiktās darbības sniedz saiti atpakaļ uz reisu, sākotnējo pirkšanas pasūtījumu un jauno kustības žurnālu vai pirkšanas pasūtījumu novirzei.
- **Tranzīta preču pasūtījumi** — ar Kopējām izmaksām tiek ieviests jauns pirmdokuments, kas ir zināms kā *tranzīta preču pasūtījums*. Tranzītu pasūtījumā iekļautās preces ļauj izrakstīt rēķinu sākotnējam pirkšanas pasūtījumam, lai iegūtu finanšu īpašumtiesības uz krājumiem. Kad pirkšanas pasūtījums ir iekļauts rēķinā, katrai pirkšanas pasūtījuma rindai, kas veido krājumu dimensiju kombināciju, tiek izveidots jauns pirmdokuments. Tad preces tiek fiziski pārvietotas uz precēm tranzīta noliktavā, kur tās ir fiziski rezervētas attiecībā uz precēm tranzīta pasūtījumā, un tās nevar patērēt, ja vien nav saņemtas tranzītpasūtījumu preces.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Papildmaksas un nosūtīšanas izmaksas

Viens no vissvarīgākajiem preču nosūtīšanas un nosūtīšanas pārvaldības aspektiem ir ar kravām saistīto papildu izmaksu atzīšana. Šīs pieskaitāmās izmaksas nav tiešās krājumu izmaksas, kas ir saistītas ar pirkšanas pasūtījumu un nosūtīšanas vai reisu. Tā vietā tās ir papildu izmaksas, kas tiek ieviestas ar preču kustības raksturu no kreditora uz jūsu organizāciju. Šīs izmaksas var ietvert kravas pārvadāšanas izmaksas, kas ir saistītas ar preču nosūtīšanu no vienas fiziskās atrašanās vietas uz citu, vai nodokļa izmaksas, kas saistītas ar preču importu no ārzemju kreditora.

Kopējās izmaksas apstrādā šīs izmaksas, izveidojot jaunu izmaksu struktūras tipu, kas pazīstams kā *automātiskās izmaksas*. TMS apstrādā šīs izmaksas, izmantojot papildmaksu funkcionalitāti.

### <a name="tms-charge-and-cost-features"></a>TMS maksa un izmaksu funkcijas

TMS izmanto papildmaksas, lai pārvaldītu papildmaksas kravām, kas tiek piešķirtas saistītajām pirmdokumenta rindām. Šīs papildmaksas var iestatīt pirkšanas pasūtījuma rindas vai pirkšanas pasūtījuma galvenes līmenī.

TMS papildmaksas var iedalīt vai dalīt ar krājumu svaru, tilpumu vai daudzumu. Maksas var dalīt pēc kravas vai piekļuves maksām. Lai TMS izmantotu papildu ieņemšanas metodes, būs nepieciešama tālāka izstrāde.

### <a name="landed-cost-charge-and-cost-features"></a>Kopējo izmaksu maksa un izmaksu funkcijas

Sūtījuma izmaksas nodrošina izmaksu funkciju kopu, kas apstrādā papildu izmaksas, kas saistītas ar preču nosūtīšanu. Šīs izmaksas tiek sauktas par automātiskām izmaksām, un tās tiek piemērotas sākotnējās nosūtīšanas rēķina izrakstīšanas laikā, izmantojot novērtēto izmaksu summu. Katrs izmaksu tips tiek pārvaldīts pēc savas grāmatošanas. Pēc faktisko papildu atbalsta izmaksu rēķinu iegrāmatošanas, novērtētās izmaksas tiek automātiski atjauninātas, lai atspoguļotu faktiskās izmaksas.

Turklāt papildu atbalstu izmaksas, kas ir saistītas ar preču nosūtīšanu, var tikt iekļautas rēķinā reisa laikā no izcelsmes ostas vai jebkurā laikā pēc preču saņemšanas. Šī iespēja nodrošina lielāku elastīgumu preču patēriņam.

Šajā sarakstā ir izcelti daži galvenie maksu un izmaksu funkciju jēdzieni Kopējās izmaksās:

- **Izmaksu apgabals** – izmaksas un maksas var piešķirt dažādiem līmeņiem vai *izmaksu apgabaliem* reisā. Izmaksas var piemērot reisa līmenī un iedalīt katram reisa krājumam. Izmaksas papildus var piemērot konteinera, pirkšanas pasūtījuma, krājuma vai pārsūtīšanas pasūtījuma līmenī. Katru izmaksu maksu var pārvaldīt atsevišķi pa dažādiem apgabaliem un sadalīt pēc krājuma izmaksām.
- **Iedalīšanas metodes** – vairākas iedalīšanas metodes ir pieejamas Kopējās izmaksās. Izmaksu maksas var novērtēt pēc daudzuma, dolāru summas, vērtības, svara, tilpuma, mērījuma vai lietotāja noteikta tilpuma mērījuma.
- **Klīringa/novirzes kontrole** - izmaksu maksas tiek iestatītas kā to pašu izmaksu koda tips, kas atrodas Kopējās izmaksās. Katrs izmaksu koda tips ļauj definēt klīringa kontu prognozētajām izmaksām, kā arī uzkrājumu un pirkšanas cenas novirzes kontus novērtēto izmaksu noviržu pret faktiskajām izmaksām. Sākotnēji grāmatojot novērtētās izmaksas, klīringa kontā ir kredīts. Pēc faktisko rēķinu grāmatošanas tiek grāmatotas faktiskās izmaksu maksas un novērtētās izmaksas tiek debitētas no klīringa konta.

## <a name="matching-freight-bills-and-invoices"></a>Saskaņot kravas pavadzīmes un rēķinus

### <a name="tms-bill-and-invoice-matching-features"></a>TMS rēķinu un rēķinu salīdzināšanas funkcijas

TMS var saskaņot kravu pavadzīmes, kas ietver novērtētās izmaksas un rēķinus ar faktiskajām kravas izmaksām. Rēķinus var saņemt elektroniski vai papīra formātā. Novērtēto izmaksu un faktisko izmaksu atbilstības novirze neietekmē krājumu novērtēšanu.

Plašāku informāciju skatiet [Kravas saskaņošana transportēšanas pārvaldībā](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Kopējo izmaksu rēķinu un rēķinu salīdzināšanas funkcijas

Kopējās izmaksas var saskaņot kravu pavadzīmes ar prognozētajām izmaksu maksām un faktiskās izmaksu maksas var saskaņot ar prognozētajām izmaksām. Rēķina izrakstīšanas laikā kravas pārvadāšanas maksas tiek iekļautas rēķinu žurnālā un novērtētās izmaksas tiek notīrītas no klīringa konta. Turklāt faktiskās izmaksu maksas tiek grāmatotas attiecībā pret krājumam pārdoto preču izmaksām kopā ar noviržu starp prognozētajām izmaksām un faktiskajām izmaksām. Tas pieļauj elastīgumu rēķinu izrakstīšanas procesā.

## <a name="tracking"></a>Izsekošana

Svarīga TMS un Kopējo izmaksu funkcija ir spēja izsekot preces un identificēt, kur tās atrodas ceļojuma vietā no izcelsmes vietas līdz galamērķa noliktavai. Izsekošana ļauj jums sekot un atjaunināt preču atrašanās vietu un laiku, kad tiek plānots saņemt tās noliktavā patēriņam. Papildus preču statusam to ceļojuma laikā, Kopējās izmaksas nodrošina prognozētās un faktiskās dienas katram ceļojuma solim.

### <a name="tms-tracking-features"></a>TMS izsekošanas līdzekļi

TMS nodrošina ierobežotus līdzekļus ienākošo kravu izsekošanai. Tas parāda datumus un ļauj izveidot integrāciju, lai atrastu precīzu pozīciju (piemēram, **Transportēšanas statusa** lapā).

Katram maršruta segmentam var ievadīt paredzamos grafikus un saņemšanas laikus.

### <a name="landed-cost-tracking-features"></a>Kopējo izmaksu izsekošanas funkcijas

Kopējās izmaksas var nodrošināt izsekošanas kontroli katram reisam no izcelsmes ostas līdz galamērķim. Izsekošanas kontrole iestata reisa statusu. Statuss norāda, vai reiss ir kuģošanas laikā, muitas pārbaudes laikā vai vietējā piegādē ceļā uz galo noliktavu. Statusu var iestatīt pirkšanas pasūtījuma rindas, konteinera un reisa galvenes līmenī. Tādējādi jums ir granulētāka kontrole.

Turklāt apstiprinātais plānotais datums, kas ir balstīts uz noteiktu izpildes laiku, tiek saistīts ar katru ceļojuma soli. Apstiprinātie un paredzamie piegādes datumi tiek pievienoti pirkšanas pasūtījuma rindai un precēm tranzīta pasūtījumos, un tos var izmantot vispārējai plānošanai un loģistikai. Papildus paredzamajiem datumiem faktiskos datumus var atjaunināt. Tālākie soļi ceļojuma laikā tiks attiecīgi atjaunināti.

## <a name="multi-leg-journeys"></a>Vairāku fāžu maršruti

Ceļojuma koncepcija identificē, kur preces atrodas procesā, un kontrolē preču statusu, kamēr tās ir tranzītā. Preces var iziet cauri vairākām ceļojuma fāzēm, un dažādas izmaksas var saistīt ar noteiktu fāzi. Piemēri iekļauj kravas pārvadāšanas izmaksas kuģa kuģošanas laikā un vietējās transportēšanas izmaksas par preču transportēšanu no ostas uz galamērķi.

### <a name="tms-multi-leg-journey-features"></a>TMS vairākfāžu ceļojuma funkcijas

TMS maršrutus var sadalīt maršruta segmentos, lai attēlotu vairākfāžu ceļojumus. TMS var piešķirt vietu likmes un papildu maksas atsevišķiem maršruta segmentiem.

Papildinformāciju skatiet [Kravas transportēšanas maršrutu plānošana ar vairākām pieturēm](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Kopējās ceļojuma izmaksas par vairākfāžu ceļojuma funkcijām

Kopējās izmaksas nodrošina struktūru preču pārvietošanai no izcelsmes vietas uz galamērķi, izmantojot vairākas fāzes, kas ir pieturas vai soļi. Kravas tiek kombinētas, lai izveidotu ceļojuma veidnes, kas nosaka preču pārvietošanas veidu no kreditora uz jūsu organizāciju.

Ikvienā ceļojuma posmā var turpmāk definēt katras pirkšanas pasūtījuma rindas statusu un izpildes laikus, kas ir saistīti ar to. Apvienotais izpildes laiks visām beigām tiek izmantots, lai identificētu paredzamo piegādes datumu. Tomēr, lai lietotu vairākfāžu kravas, ir nepieciešama tranzīta kravu apstrāde. Preču pārvadāšana uz reisa tiek pārvaldīta tabulā, kas ir raksturīga Kopējām izmaksām.

## <a name="receiving-by-container"></a>Saņemšana pēc konteinera

Ir svarīgi pārvaldīt, kā preces tiek sadalītas un uzglabātas uz kuģa. Uz kuģa preces var uzglabāt vienā konteinerā vai vairākos konteineros. Kad preces ir saņemtas, tās tiek saņemtas konteineros un dažādus reisa konteinerus var saņemt dažādos laikos vai dažādos datumos.

Gan TMS, gan Kopējās izmaksas nodrošina funkcionalitāti preču saņemšanas pārvaldībai konteinerā. TMS izmanto kravu koncepciju, lai pārvaldītu ar kravas konteineru saistītās preces, pirkšanas pasūtījumus un pārsūtīšanas pasūtījumus. TMS atbalsta saņemšanu, balstoties uz iepakojuma struktūru, kas tiek saņemta ar iepriekšēja nosūtīšanas paziņojuma (ASN) palīdzību. Kopējās sūtījuma izmaksas izmanto pārvadāšanas konteineru koncepciju, lai apstrādātu pirkšanas pasūtījumus un kontrolētu pieskaitāmās izmaksas, kas ir saistītas ar konteineru kuģim.

### <a name="tms-receiving-by-container-features"></a>TMS saņemšana pēc konteinera īpatnībām

TMS atbalsta ienākošos ASN, visus saņemšanas variantus caur Warehouse Management mobile programmu un visas klienta saņemšanas metodes caur Supply Chain Management.

### <a name="landed-cost-receiving-by-container-features"></a>Kopējo izmaksu saņemšana pēc konteinera īpatnībām

Lai atbalstītu saņemšanu pēc konteinera, ar sūtījuma izmaksām tiek izveidoti pārvadāšanas konteinera ieraksti un tiek asociēti pirkšanas pasūtījumi ar noteiktu pārvadāšanas konteineru, izmantojot tā konteinera ID. Pēc tam pieskaitāmās izmaksas var piemērot šim pārvadāšanas konteineram un sadalīt tā, lai tās būtu saistītas ar atbilstošajiem pirkšanas pasūtījumiem.

Konteinerus Kopējās izmaksās var saņemt, izmantojot jaunu ieejas plūsmas tipu, kas pazīstams kā *tranzīta preču saņemšana*, saņemšanas žurnālos vai izmantojot mobilās ierīces saņemšanu. Kad tiek izmantoti saņemšanas žurnāli, daudzumus var inicializēt no precēm tranzīta pasūtījumā vai oriģinālā pirkšanas pasūtījuma rindām konteinerā. Kopējās izmaksas nodrošina divus darba veidus saņemšanai no Warehouse Management mobile programmas.

Kopējās izmaksas nesniedz ASN preču elektroniskajai saņemšanai. Turklāt netiek atbalstītas Warehouse Management mobile programmas plūsmas, kas apstrādā noslodzes saņemšanu, numura zīmes saņemšanu vai jauktu noliktavas vienības saņemšanu.

## <a name="rate-shopping-by-vendor"></a>Novērtēt iepirkšanos pēc kreditora

Iepirkšanās novērtēšana ļauj uzņēmumam atlasīt transportēšanas kreditoru, pamatojoties uz zemāko cenu, ātrāko maršrutu vai abu apsvērumu kombināciju.

### <a name="tms-rate-shopping-features"></a>TMS iepirkšanās novērtēšanas funkcijas

TMS ļauj identificēt kreditora un maršrutēšanas risinājumus ienākošajiem un izejošajiem pasūtījumiem. Piemēram, var norādīt ātrāko ceļu vai vislētāko sūtījuma likmi.

TMS nodrošina pilnapmēra iepirkšanas un kravas optimizāciju, izmantojot likmes un maršruta rīkkopu, elastīgās novērtēšanas opcijas, izmantojot vērtēšanas programmu, vērtēšanas programmu API integrēšanai ar ārējām pusēm un atbalstu tilpuma svaram.

Plašāku informāciju skatiet [Transportēšanas pārvaldības programmas](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Kopējo izmaksu iepirkšanās novērtēšanas funkcijas

Kopējas izmaksas nodrošina tikai ierobežotu atbalstu kreditora cenu pirkšanai. Lai gan jūs varat ievadīt kravas pārvadātāja vērtības, Kopējās izmaksas nesalīdzina tās ar vairākiem kreditoriem.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Autovadītāja reģistrēšanās/izrakstīšanās ar norīkojuma plānošanu

Transportlīdzekļa vadītāja reģistrēšanās/izrakstīšanās funkcijas ļauj sistēmai pārraudzīt saņemšanas un novērst problēmas iekraušanas dokā.

### <a name="tms-driver-check-incheck-out-features"></a>TMS autovadītāja reģistrēšanās/izrakstīšanās funkcijas

TMS ļauj izveidot *norīkojumus*. Noliktavu norīkojumi apzīmē notikumus, kas dokā notiek pirkšanas pasūtījumu saņemšanai, pārdošanas pasūtījuma nosūtīšanai vai ienākošas vai izejošas kravas apstrādei noteiktā datumā un laikā. Tikšanās nodrošina, ka preču iekraušanai un izkraušanasm ir pieejami doki un tie palīdz novērst situācijas, kad vairāki pārvadātāji vienlaicīgi ierodas atrašanās vietā.

Sistēma atbalsta atļaut transportlīdzekļu vadītājiem pārbaudīties pie noteiktām doka durvīm.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Kopējo izmaksu autovadītāja reģistrēšanās/izrakstīšanās funkcijas

Kopējās izmaksas var glabāt novērtējumus par datumu un laiku, kad tiks piegādāts konteiners.

## <a name="transfer-orders-and-additional-costs"></a>Pārsūtīšanas pasūtījumi un papildmaksas

Bieži uzņēmumiem ir jāspēj pārsūtīt preces no noliktavas uz noliktavu. Kad notiek šāda veida pārsūtīšana, izmaksas tiek saistītas ar to un, iespējams, vēlēsieties tās atpazīt. Kopējās izmaksās sūtījuma izmaksas pārsūtīšanas pasūtījumus var pievienot reisam vai kuģim, lai izsekotu preču kustību no vienas noliktavas vai vietas uz citu, prognozēto piegādes laiku un paredzamo piegādes datumu un pievienot papildu izmaksas preču pārsūtīšanai.

### <a name="tms-transfer-order-cost-features"></a>TMS pārsūtīšanas pasūtījuma izmaksu funkcijas

TMS atbalsta kravas transportēšanas maksu izveidi, kas ir saistītas ar pārsūtījumiem. Kaut arī šīs maksas var skatīt pārsūtīšanas pasūtījumā, kopējās izmaksas netiek pievienotas krājumu izmaksām. Kravas saskaņošanu atbalsta izveidot kravas pavadzīmi, pamatojoties uz šīm maksām. Pēc tam šī kravas pavadzīme tiek saskaņota pret kreditora kravas pavadzīmi.

### <a name="landed-cost-transfer-order-cost-features"></a>Kopējo izmaksu pārsūtīšanas pasūtījuma izmaksu funkcijas

Kopējās izmaksas ļauj pievienot pārsūtīšanas pasūtījumus kuģim vai reisam. Šādā veidā pārsūtīšanas pasūtījuma saņemšanas laikā reisam var pievienot nosūtīšanas izmaksas kā krājumu segšanas. Pieskaitāmās izmaksas var tikt iekļautas rēķinā par faktiskajām izmaksām un atsekotas pret reisu, lai atjauninātu pārdoto preču izmaksas. Lai gan pārsūtīšanas pasūtījumos netiek izmantota tranzīta preču apstrāde standarta laidienā, tos var pievienot reisiem. Kopējās izmaksas tiek pievienotas katra krājuma kopējām izmaksām.