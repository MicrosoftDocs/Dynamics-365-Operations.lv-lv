---
title: Preču identifikatori
description: Šajā tēmā ir sniegta informācija par dažādajiem preču identifikatoru veidiem un ir paskaidrots, kā varat pievienot preču identifikatorus preču datiem.
author: cvocph
manager: AnnBe
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 0aa8baf5802ccdd9a502e2a7d291a76fc4afe932
ms.sourcegitcommit: d91d96c98b31ae59bc82ec91efbb7da86ffb25fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172029"
---
# <a name="product-identifiers"></a>Preču identifikatori

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par dažādajiem preču identifikatoru veidiem un ir paskaidrots, kā varat pievienot preču identifikatorus preču datiem.

Strādājot ar ražotnē vai noliktavā esošajām precēm programmā Microsoft Dynamics ERP vai Microsoft Dynamics CRM, ir vajadzīga efektīva šo preču un preču variantu identificēšanas stratēģija.

## <a name="unique-product-numberproduct-id"></a>Unikāls preces numurs/preces ID

Programmā Dynamics 365 Supply Chain Management preces galvenais identifikators ir preces numurs (unikālais preces ID). Šo numuru var automātiski ģenerēt, izmantojot numuru sēriju, vai manuāli saistīt ar preci. Preču variantu numurus var definēt, izmantojot preču nomenklatūras veidni.

Bieži vien preces numurs nav sākotnēji izveidots programmā Dynamics 365 Supply Chain Management. Tā vietā tas ir saistīts ar preci preču dzīves cikla pārvaldības (product lifecycle management — PLM) sistēmā vai preču datu pārvaldības (product data management — PDM) sistēmā. Šādā gadījumā jūs izmantojat datu elementus, lai importētu preces un preču variantus. Pēc tam Supply Chain Management izmanto visu operāciju numurus.

Ieviešot Supply Chain Management, ir īpaši jāapsver preču numerācijas metode. Efektīva numerācijas sistēma uzlabo loģistikas plūsmas un palīdz nepieļaut kļūdas. Labā preces identifikatorā ir ne vairāk kā 15 rakstzīmes. Ideālā gadījumā tajā ir ne vairāk kā 10 rakstzīmes un ne vairāk kā piecas klasifikācijas rakstzīmes. Varat arī izmantot saīsinātos nosaukumus, lai nodrošinātu ātru meklēšanu. Saīsinātais nosaukums ir papildu nosaukums, kas norāda preces klasifikāciju.

Izmantojot Common Data Service, preču numurs Supply Chain Management ir arī preces numurs Common Data Service. Preču varianti tiek sinhronizēti ar pakalpojumu Common Data Service kā atšķirīgas preces.

## <a name="item-number-and-product-dimensions"></a>Krājuma numurs un preces dimensijas

Krājuma numurs ir preces identifikators, ko lieto noteikta juridiskā persona. Ideālā gadījumā krājuma numuram ir jābūt vienādam ar preces numuru. Ja katrai juridiskajai personai ir atšķirīga nomenklatūra, ir grūti sekot preces kustībai piegādes ķēdē un tiek ieviesti apgrūtinoši etiķešu maiņas un atsauču izveides procesi. Lai nodrošinātu saderību ar vecākām versijām (Microsoft Dynamics AX 2009 un vecākām versijām), esam saglabājuši šo modeli. Taču ir ieteicams likvidēt juridiskajām personām specifiskos identifikatorus, ja vien tas ir iespējam, un to vietā kā galveno identifikatoru izmantot unikālo preces numuru.

Turklāt preces variantu nevar unikāli identificēt, izmantojot krājuma numuru. Tam vienmēr ir nepieciešams krājuma numurs un visas preces dimensijas, kas ir definētas preces šablonā. Šī prasība var sarežģīt un palēnināt identifikācijas procesu. Arī šī iemesla dēļ ir ieteicams krājuma numura vietā lietot unikālo preces numuru, ja vien tas ir iespējams.

Daudzās lapās galvenie identifikatori joprojām ir krājumu numurs un preču dimensijas. Taču meklēšanai var izmantot preču numurus. Sadaļā **Pārdošana un mārketings** &gt; **Iestatījumi** &gt; **Meklēšana** &gt; **Meklēšanas parametri** varat mainīt meklēšanas uzmeklēšanas veidu tā, lai galvenās meklēšanas metodes ietvaros krājumu numuru vietā tiktu izmantoti preču numuri. Ja iestatāt opcijas **Iespējot uzmeklēšanu preču meklēšanā** vērtību **Jā**, uzmeklēšanas rezultātos tiek rādīti ne tikai preču šabloni, bet arī preču varianti. Papildinformāciju skatiet tēmā [Preču un preču variantu meklēšana pasūtījuma izveides laikā](search-products-product-variants.md).

Turklāt varat meklēt un filtrēt pēc preces numura, preces nosaukuma un apraksta, kā arī preces varianta preces dimensiju ID. Kad atlasāt variantu, tiek atlasīts saistītais krājuma numurs un visi preces dimensiju ID. Tādējādi varat vieglāk atrast un atlasīt vajadzīgo variantu. Šo iestatījumu ir ļoti ieteicams izmantot, ja lietojat preču variantus un kā galveno preču identifikatoru izmantojat unikālo preces numuru. Vienīgais izņēmums, iespējams, ir modes nozare, kuras biznesa procesu ietvaros bieži vien pirms varianta atlases ir jāatlasa šablons. Pirms numurēšanas sistēmas ieviešanas ir rūpīgi jānovērtē šīs opcijas izmantošana.

> [!NOTE]
> Preces numuru precei nevar mainīt, ja šai precei pastāv viena vai vairākas transakcijas.

## <a name="product-name-and-description"></a>Preces nosaukums un apraksts

Preces nosaukums un apraksts ir cilvēkiem saprotami preces identifikatori, un tos var uzturēt daudzās valodās. Pēc noklusējuma Supply Chain Management klientā visa informācija par precēm tiek rādīta uzņēmuma noklusējuma valodā, nevis lietotāja valodā. Taču saziņai ar debitoriem un kreditoriem vienmēr tiek izmantoti tulkotie preču nosaukumi un apraksti. Tulkojumi ir atkarīgi no kreditora konta un debitora konta valodas koda.

Preču variantu preču nosaukumus var ģenerēt, izmantojot preču nomenklatūras veidni. Tā kā preču nosaukumiem nav jābūt unikāliem, vairākām precēm var būt vienādi nosaukumi.

## <a name="product-and-item-search-names"></a>Preču un krājumu saīsinātie nosaukumi

Programmatūrā Supply Chain Management ir pieejams papildu saīsinātais nosaukums, ko var izmantot precēm, kā arī krājumiem (izlaisto preču). Šim saīsinātajam nosaukumam nav jābūt unikālam, un to var mainīt pēc preces vai preces varianta izveides. Ir ieteicams izmantot saīsināto nosaukumu, lai meklētu preces pēc kategorijas. Saīsinātie nosaukumi nodrošina ātru meklēšanu, jo īpaši pārdošanas un pirkšanas procesu ietvaros.

Saīsinātajā nosaukumā var ietvert arī kreditora vai debitora preces ID vai kādu citu ārēju preces ID, ja šis ārējais ID ir galvenais preces meklēšanas kritērijs.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Ārēji preču identifikatori (debitoru un kreditoru identifikatori)

Izlaistajām precēm varat uzturēt debitora vai kreditora lietotos krājumu numurus, krājumu nosaukumus un krājumu aprakstus. Atsauces tiek rādītas ārējos dokumentos, piemēram, pārdošanas pasūtījumos, pirkšanas pasūtījumos, pavadzīmēs un rēķinos. Pašreizējā Supply Chain Management versijā ārējās atsauces netiek rādītas pamatdarbību lapās. Vienīgais izņēmums ir kreditora krājuma numurs. Šis numurs tiek rādīts dialoglodziņā **Preces informācija**, ja saistītajai precei ir definēts noklusējuma kreditors.

Varat uzturēt ārējos preču identifikatorus noteiktai izlaistajai precei, izlaistajam preces variantam, debitoram, debitoru grupai, kreditoram vai kreditoru grupai.

Lapā **Izlaistās preces** veiciet vienu no tālāk norādītajām darbībām.

- Ja strādājat ar debitoriem, cilnes **Pārdošana** grupā **Saistītā informācija** atlasiet **Ārējā krājuma apraksts**.
- Ja strādājat ar kreditoriem, cilnes **Pirkšana** grupā **Saistītā informācija** atlasiet **Ārējais krājuma apraksts**.

Lapā **Ārējais krājuma nosaukums** varat saistīt debitora vai kreditora krājuma numuru ar izlaistu preci. Šī saistīšana ir jāveic katrai juridiskajai personai. Var ietvert tālāk norādīto informāciju. Diemžēl pašreizējā Supply Chain Management versijā etiķetes ir nedaudz maldinošas. Taču šīs etiķetes, iespējams, tiks mainītas nākamajās versijās.

| Lauks | Atbilstoša debitora informācija | Atbilstoša kreditora informācija |
|-------|------------------------------------|----------------------------------|
| Ārējais krājuma kods | Debitora krājuma numurs | Kreditora krājuma numurs |
| apraksts | Nosaukums, ko debitors ir saistījis ar krājumu | Nosaukums, ko kreditors ir saistījis ar krājumu |
| Ārējais krājuma teksts | Debitora krājuma apraksts | Kreditora krājumu apraksts |

Ja daudzi debitori vai kreditori izmanto vienu un to pašu krājuma numuru (piemēram, pircēju apvienības vai komercijas grupas gadījumā), varat izveidot debitoru vai kreditoru grupas, lai atvieglotu ārējās preču informācijas uzturēšanu.

- Ja strādājat ar debitoru grupām, pārejiet uz sadaļu **Pārdošana** &gt; **Iestatījumi** &gt; **Krājumi** &gt; **Ārējā krājuma apraksts**, lai izveidotu un uzturētu grupas un saistītos krājumu numurus. Lai saistītu debitorus ar grupu, pārejiet uz sadaļu **Debitoru parādi** &gt; **Debitori** &gt; **Visi debitori** un pēc tam kopsavilkuma cilnē **Pārdošanas pasūtījuma noklusējuma informācija** norādiet lauka **Krājumi — debitoru grupa** vērtību.
- Ja strādājat ar kreditoru grupām, pārejiet uz sadaļu **Sagāde un avoti** &gt; **Iestatījumi** &gt; **Ārējā krājumu apraksta grupa**, lai izveidotu un uzturētu grupas un saistītos krājumu numurus. Lai saistītu kreditorus ar grupu, pārejiet uz sadaļu **Kreditoru parādi** &gt; **Kreditori** &gt; **Visi kreditori** un pēc tam kopsavilkuma cilnē **Pirkšanas pasūtījuma noklusējuma informācija** norādiet lauka **Krājumi — kreditoru grupa** vērtību.
 
## <a name="bar-codes"></a>Svītrkodi

Ja vēlaties preču identifikācijai izmanto svītrkodu skenerus, preces identifikatoram ir jāatbilst izmantotā svītrkodu standarta prasībām. Tāpēc svītrkodos parasti nav ietverts sākotnējais preces numurs, bet ir ietvers numurs, kas ir īpaši ģenerēts izmantošanai ar izvēlēto svītrkodu tehnoloģiju. Varat uzturēt vairākus viena svītrkodu veida svītrkodus. Varat pat saistīt vienu svītrkodu ar vairākām precēm un pēc tam atlasīt faktisko aktīvo saistījumu svītrkoda skenēšanas laikā.

Pirms svītrkodu definēšanas varat definēt vienu vai vairākus svītrkodu iestatījumus. Svītrkodu iestatījumi var palīdzēt pārbaudīt, vai svītrkodi atbilst nepieciešamajām vadlīnijām un tāpēc tos var efektīvi drukāt un skenēt. Varat arī uzturēt īpašus svītrkodus noteiktiem preču daudzumiem.

Ir ieteicams izmantot svītrkoda iestatījumu, lai uzturētu globālās tirdzniecības krājumu numuru (Global Trade Item Number — GTIN) vai Eiropas preču numerācijas (International Article Number — EAN) kodus.

Lai uzturēt svītrkodus, lapas **Izlaistās preces** cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Svītrkodi**.

## <a name="gtin-codes"></a>GTIN kodi

E-komercijas ietvaros ir ļoti svarīgi, lai visas puses savstarpēji saprastos un izmantotu kopīgu preču identifikatoru kopu. Tāpēc dažās nozarēs tiek izmantota globālā krājumu numerācijas sistēma [GTIN](https://www.gs1.org/id-keys/gtin), ko nodrošina GS1.

Iesakām uzturēt GTIN kā svītrkodu. Taču to var uzturēt arī lapā **Krājumi — GTIN**. Lai atvērtu šo lapu, lapas **Izlaistās preces** cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **GTIN kodi**. Ņemiet vērā, ka GTIN netiek uzturēts kā globāls numurs. Tā vietā tas tiek uzturēts noteiktai juridiskajai personai.

Programmatūrā Supply Chain Management noliktavas darbību ietvaros iepakojuma varianti tiek definēti, norādot noteiktas mērvienības. Piemēram, krājums var tikt glabāts atsevišķos gabalos, komplektos pa sešiem, paplātēs pa 18 vai pilnās paletēs. Katram no šiem iepakojuma variantiem tiek definēta noteikta mērvienība. Tā kā GTIN parasti ir saistīts ar preces iepakojuma vienību, lapā **Krājumi — GTIN** varat uzturēt vairākus GTIN kodus katrai precei un mērvienībai. Taču nevarat vairākas reizes izmantot vienu GTIN kodu dažādiem vienas juridiskās personas krājumiem vai preču variantiem.

Lai uzturētu **GTIN kodus**, lapas **Izlaistās preces** cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **GTIN**.

## <a name="external-codes"></a>Ārējie kodi

Ārējos kodus var definēt vairākiem uzņēmumiem. Piemēram, varat definēt ārējos kodus, lai identificētu preces un izlaistās preces. Šos ārējos kodus var izmantot, lai saistītu statistikas kodus vai nodokļu kodus ar izlaistajām precēm un izlaistajiem preču variantiem. Ārējie kodi tiek definēti atbilstoši juridiskajai personai un koda veidam. Tiem ir jābūt unikāliem, salīdzinot juridisko personu, koda veidu un tabulas atsauci.

Diemžēl nepastāv standarta funkcijas, kas sniedz iespēju meklēt preces pēc ārējiem kodiem.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Preču identifikatoru importēšanai un eksportēšanai izmantotie datu elementi

| Elementa nosaukums | Identifikatoru importēšana | Identifikatoru eksportēšana | Komentāri |
|-------------|--------------------|--------------------|----------|
| Preces V2 | Preces numurs, preces saīsinātais nosaukums, preces nosaukums, preces apraksts | Preces numurs, preces saīsinātais nosaukums, preces nosaukums, preces apraksts | Atkarībā no elementa iestatījumiem un preces numura numuru sērijas importēšanas laikā var tikt automātiski izveidots preces numurs. |
| Preces varianti | Preces numurs, preces saīsinātais nosaukums, preces nosaukums, preces apraksts | Preces numurs, preces saīsinātais nosaukums, preces nosaukums, preces apraksts | Atkarībā no preču nomenklatūras veidnes importēšanas laikā var tikt automātiski izveidots preces numurs. Taču varat importēt jebkuru unikālo preces numuru, un šim preces numuram nav jāatbilst preču nomenklatūras veidnes struktūrai. |
| Preces pārrēķini | Preces nosaukums, preces apraksts | Preces nosaukums, preces apraksts | Šis elements izraisa jebkuras valodas pārrakstīšanu. Ņemiet vērā, ka, pārrakstot juridiskās personas primārās valodas nosaukumu vai aprakstu, tiek mainīts arī preces nosaukums un apraksts. |
| Izlaisto preču izveide V2 | Krājuma numurs, preces numurs, krājuma saīsinātais nosaukums| Krājuma numurs, preces numurs, krājuma saīsinātais nosaukums, preces saīsinātais nosaukums, preces nosaukums | Šis elements var radīt sarežģījumus, ja jaunu izlaisto preču izveides laikā tiek izmantotas numuru sērijas. Tiek ņemta vērā gan numuru sērija **Krājuma numurs** , gan numuru sērija **Preces numurs**. Taču numuru sērija **Krājuma numurs** atbilst noteiktai juridiskajai personai, bet numuru sērija **Preces numurs** ir globāla. Tāpēc, izvietojot jaunas izlaistās preces, nav ieteicams izmantot numuru sēriju **Krājuma numurs**. Protams, ka gadījuma, ja elements tiek izmantots esošas preces izlaišanai, elementā ir jānorāda preces numurs. Papildinformāciju skatiet šīs tēmas sadaļā “Preču un krājumu numuru sērijas”. |
| Izlaistie preces varianti | Krājuma numurs, preces dimensijas, preces numurs | Preces numurs, preces saīsinātais nosaukums, preces nosaukums, preces apraksts, preces dimensijas | Līdzīgi kā elementu **Preces varianti**, arī šo elementu var izmantot, lai izveidotu jaunas preces, kuru variantiem tiek izmantota preču nomenklatūras veidne vai precei specifiski preču numuri. |
| Ārējs krājuma apraksts debitoriem | Debitora krājuma numurs, debitora krājuma nosaukums, debitora apraksts, debitora konts | Debitora krājuma numurs, debitora krājuma nosaukums, debitora apraksts, debitora konts | Izmantojot elementu **Ārējā krājumu apraksta debitoru grupas**, debitoru grupu (piemēram, pircēju apvienību) var apvienot vienā grupā. |
| Ārējs krājuma apraksts kreditoriem | Kreditora krājuma numurs, kreditora krājuma nosaukums, kreditora apraksts, kreditora konts | Kreditora krājuma numurs, kreditora krājuma nosaukums, kreditora apraksts, kreditora konts | Izmantojot elementu **Ārējā krājumu apraksta kreditoru grupas**, kreditoru grupu (piemēram, pārdevēju apvienību vai nozares organizāciju) var apvienot vienā grupā. |
| Krājuma svītrkods | Svītrkods | Svītrkods | Ņemiet vērā, ka importēšanas laikā ir jāskata mērķa sistēmā definētais svītrkoda iestatījums. Importētās svītrkodu atsauces tiek pārbaudītas, salīdzinot tās ar svītrkoda iestatījumu, un tās tiek noraidītas, ja svītrkodi neatbilst svītrkoda iestatījumā definētajām prasībām. |
| Ārējie kodi izlaistajām precēm | Ārējais kods | Ārējais kods, ārējo kodu klases, krājuma numurs | Ārējie kodi atbilst noteiktai juridiskajai personai. Importēšanai ir jāizmanto definēta kodu klase. Importējiet kodu klases, izmantojot elementu **Ārējo kodu klases izlaistajām precēm**. |
| Ārējie kodi izlaisto preču variantiem | Ārējais kods | Ārējais kods, ārējo kodu klases, krājuma numurs, preces dimensijas | Ārējie kodi atbilst noteiktai juridiskajai personai. Importēšanai ir jāizmanto definēta kodu klase. Importējiet kodu klases, izmantojot elementu **Ārējo kodu klases izlaistajām precēm**. Lietojot šo elementu, preces varianti tiek norādīti, izmantojot krājuma numuru un preces dimensijas. |
| Izlaisto preces variantu ārējie kodi pēc preces numura identifikatora | Ārējais kods | Ārējais kods, ārējo kodu klases, preces numurs | Ārējie kodi atbilst noteiktai juridiskajai personai. Importēšanai ir jāizmanto definēta kodu klase. Importējiet kodu klases, izmantojot elementu **Ārējo kodu klases izlaistajām precēm**. Lietojot šo elementu, preces varianti tiek norādīti, izmantojot varianta preces numuru. (Sākot ar nākamo nozīmīgo laidienu.) |
| GTIN | Nav attiecināms | Nav attiecināms | Pašlaik nav neviena noteikta elementa, kas tiek izmantots GTIN kodu importēšanai un eksportēšanai. Ir ieteicams tā vietā izmanto elementu **Krājuma svītrkods**. |
| Preces elementa common data service identifikatora elements | Nav attiecināms | Krājuma kods, krājuma saīsinātais nosaukums, preces saīsinātais nosaukums, kreditora krājuma numurs, debitora krājuma numurs, ārējie kodi, GTIN kodi, svītrkodi | Šis elements nodrošina visu identifikatoru apvienošanu vienā datu modelī, varētu viegli eksportēt visus identifikatorus un to saistītos veidus, izmantojot vienu interfeisu. Izmantojiet elementu **Preces elementa identifikatora kods**, lai eksportētu identifikatoru kodus un aprakstus. Izmantojiet elementu **Preču elementu identifikatoru tvērums**, lai identifikatorā eksportētu papildu tvēruma informāciju, piemēram, informāciju par pusi, juridisko personu, daudzumu vai mērvienību. |

### <a name="product-and-item-number-sequences"></a>Preču un krājumu numuru sērijas

Varat definēt divas dažādas numuru secības:

- Numuru sērija **Preces numurs**, kas tiek izmantota globālajam preces numuram
- Numuru sērija **Krājuma numurs**, kas tiek izmantota juridiskās personas krājuma numuram

> [!NOTE]
> Izmantojiet krājuma numuru kā atsevišķu identifikatoru tikai tad, ja migrējat dažādas juridiskās personas no dažādiem avotiem ar dažādām numurēšanas sistēmām. Vienmēr centieties izmantot preces identifikatoru, kas ir unikāls visām juridiskajām personām. Tāpēc iestatiet opcijas **Manuāli** vērtība **Jā** numuru sērijai **Krājuma numurs**. Tādējādi izveides laikā krājuma numurs seko preces numuram. Ja Supply Chain Management nav galvenā jaunā preču numuru sistēma, iestatiet opcijas **Manuāli** vērtību **Jā** gan numuru sērijai **Krājuma numurs**, gan numuru sērijai **Preces numurs**.

Ja preču izveidei izmantojat elementu **Izlaistās preces izveide V2**, to, kā numuru sērijas tiek izmantotas preces numura un krājuma numura izveidei, var ietekmēt vairāki tālāk norādītie iestatījumi.

- Numuru sērijas **Preces numurs** iestatījumi
- Numuru sērijas **Krājuma numurs** iestatījumi
- Krājuma numura kartēšana 
- Preces numura kartēšana

Tālāk esošajā tabulā ir sniegts pārskats par importēšanas un manuālas izveides rezultātiem, izmantojot noteiktus numuru sērijas un lauku kartēšanas iestatījumus.

| Numuru sērija Preces numurs | Numuru sērija Krājuma numurs | Krājuma numura kartēšana | Preces numura kartēšana | Elementa importēšanas rezultāts | Manuālas izveides rezultāts | Nobeigums |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Manuāli = Nē | Manuāli = Nē | Nav kartēšanas gadījumu | Nav kartēšanas gadījumu | Preču numuriem tiek izmantota numuru sērija **Preces numurs**. Krājumu numuriem tiek izmantota numuru sērija **Krājuma numurs**. | Preču numuriem tiek izmantota numuru sērija **Preces numurs**. Krājumu numuriem tiek izmantota numuru sērija **Krājuma numurs**. | Izmantojot šo konfigurāciju, preču numuri sekos preces numuru sērijai un krājumu numuri sekos krājuma numuru sērijai. Tomēr šī konfigurācija nedarbojas, ja ir vairāk nekā viens importējams krājums (rinda). |
| Manuāli = Nē | Manuāli = Jā | Automātiski ģenerēt | Nav kartēšanas gadījumu | Gan preču numuriem, gan krājumu numuriem tiek izmantota numuru sērija **Krājuma numurs**. | Gan preču numuriem, gan krājumu numuriem tiek izmantota numuru sērija **Preces numurs**. | Gan preču numuri, gan krājumu numuri sekos preču numuru sērijai. Šī ir ieteicamā metode, kā importēt lielapjoma preces ar izlaisto preču izveides v2 datu elementu. |
| Manuāli = Nē | Manuāli = Jā | Nav kartēšanas gadījumu | Nav kartēšanas gadījumu | Gan preču numuriem, gan krājumu numuriem tiek izmantota numuru sērija **Preces numurs**. | Gan preču numuriem, gan krājumu numuriem tiek izmantota numuru sērija **Preces numurs**. | Gan preču numuri, gan krājumu numuri izmantos preču numuru sēriju. Tomēr šī konfigurācija nedarbojas, ja ir vairāk nekā viens importējams krājums (rinda). |
| Manuāli = Jā | Nav attiecināms | Nav attiecināms | Automātiski ģenerēt | Tiek parādīts šāds kļūdas ziņojums: “Nevar noteikt numuru sēriju”. | Atbilstoši numuru sērijai **Krājuma numurs** | Importēšanai netiek atbalstīts šis iestatījums. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Preces elementa identifikators (visu preces identifikatoru eksportēšana)

Preču elementu identifikatoru modelis tika izveidots, lai CDS versijā 1.0 varētu nodrošināt visus identifikatorus, kas tiek izmantoti preces norādīšanai. Lai vienkāršotu šo uzdevumu, visi identifikatori tiek apvienoti vienā globālā identifikatoru tabulā, ko var eksportēt kā vienu modeli. Ņemiet vērā, ka šajā CDS versijā netiek izmantots preces identifikatoru modelis. Tāpēc elementam **Preces elementa common data service identifikatora elements** un šim procesam ir ierobežots praktiskais pielietojums un tie, visticamāk, tiks mainīti nākamajos izlaidumos.

Preces identifikatoru tabula ir globāla tabula, kas tiek aizpildīta ar datiem no visām galvenās juridiskās personas atsauces tabulām, izmantojot periodisku pakešuzdevumu. Jums ir jāatlasa juridiskā persona un preču kategoriju hierarhija, lai definētu globālo preces šablona tvērumu. Globālo preces identifikatoru tabulu var ģenerēt tikai tādām precēm, kas ir izlaistas atlasītajai juridiskajai personai un ir ietvertas preču hierarhijā, kura preču kategoriju hierarhijā ir atlasīta lomai **Common data service**.

Šī procesa ietvaros tiek pieņemts, ka preču pamatdatu uzturēšanai galvenokārt tiek izmantota viena centrālā juridiskā persona. (Taču šī juridiskā persona var būt virtuāla juridiskā persona, kas tiek izmantota tikai globālo pamatdatu uzturēšanai.)

Veiciet tālāk norādītās darbības, lai konfigurētu vidi.

1. Atlasiet CDS kategoriju hierarhiju. Ja lapā **Kategoriju hierarhijas lomas saistības** ar lomu **Common data service** nav saistīta neviena hierarhija, ir jāizveido jauna saistība. Atlasiet lomu **Common data service** un pēc tam saistiet to kategoriju hierarhiju, kas atbilst ar CDS sinhronizējamajam preču portfelim.
2. Atlasiet globālo preču pamatdatu juridisko personu. Lapas **Preču informācijas pārvaldības parametri** cilnē **Preces īpašības** atlasiet galveno uzņēmumu, kas galvenokārt tiek izmantots preču un krājumu identifikatoru uzturēšanai.
3. Definējiet eksportējamos identifikatoru kodu veidus un kodus. Pārejiet uz sadaļu **Preču informācijas pārvaldība** &gt; **Iestatījumi** &gt; **Preču identifikatoru kodi**. Lai ģenerētu identifikatoru kodu veidus, atlasiet **Ģenerēt kodus**. Tiek ģenerēts koda tipa ieraksts atbilstoši katram identifikatora veidam, kas ir atrasts atlasītās juridiskās personas datos.

    Ņemiet vērā, ka svītrkodu gadījumā katram svītrkoda iestatījumam tiek ģenerēts atsevišķs koda veids. Ārējo kodu gadījumā katrai ārējo kodu klasei tiek ģenerēts atsevišķs koda veids.

    Tagad varat uzturēt kodu veidu sarakstu. Varat mainīt kodu, nosaukumu un aprakstu. Varat arī dzēst kodu veidus. Dzēstie kodu veidi netiek izmantoti globālo preču elementu identifikatoru tabulu aizpildīšanai.

4. Kad esat pabeidzis preču identifikatoru kodu veidu definēšanu, varat izveidot globālajā tabulā ietvertos identifikatorus, sākot darbu **Izveidot preču elementu identifikatorus** lapā**Preču elementu identifikatoru kodi**. Šis darbs ir jāizpilda kā pakešuzdevums. Šis darbs ir jāiestata kā periodisks pakešuzdevums, lai tabula tiktu aizpildīta atbilstoši jauniem ierakstiem.

Tagad varat izmantot datu elementus **Preces elementa common data service identifikatora elements**, **Preces elementa identifikatora kods** un **Preču elementu identifikatoru tvērums**, lai eksportētu identifikatorus neatkarīgi no mērķa sistēmas.

## <a name="related-topic"></a>Saistītā tēma

[Preces un preces variantu meklēšana pasūtījuma izveides laikā](search-products-product-variants.md)
