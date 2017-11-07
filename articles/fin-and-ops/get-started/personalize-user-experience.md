---
title: "Personalizēt lietotāja pieredzi"
description: "Šajā tēmā skaidrots, kā personalizēt programmatūru Microsoft Dynamics 365 for Finance and Operations."
author: RobinARH
manager: AnnBe
ms.date: 08/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dbc80ff756a5286a98489f1f1403959d9b18ebe6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="personalize-the-user-experience"></a>Personalizēt lietotāja pieredzi

[!include[banner](../includes/banner.md)]


Šajā tēmā skaidrots, kā personalizēt programmatūru Microsoft Dynamics 365 for Finance and Operations.

Programmatūrā Microsoft Dynamics 365 for Finance and Operations ir pieejami daudzi personalizēšanas veidi. Dažas personalizācijas ir no opciju saraksta iestatīšanas lapā veiktās atlases. Dažas personalizēšanas darbības ir netiešas, piemēram, Finance and Operations seko režģa kolonnu platumam, ja to koriģējat, un kopsavilkuma ciļņu izvēršanas/sakļaušanas stāvoklim. Citas personalizācijas ir tiešas. Tiešajām personalizācijām jūs ieejat interaktīvās personalizēšanas režīmā un modificējat lapas izskatu, tieši pārvaldot to, kā elementi tiek parādīti vai darbojas lapā. 

Jebkura veida personalizēšana, ko lietotājs veic programmatūrā Finance and Operations, attiecas tikai uz šo lietotāju neatkarīgi no uzņēmuma, ar kuru lietotājs mijiedarbojas. Izmaiņas, ko lietotājs veic lapā, neietekmē citus lietotājus sistēmā.

## <a name="systemwide-options-for-the-current-user"></a>Sistēmas līmeņa opcijas pašreizējam lietotājam
Navigācijas joslā jūs atradīsiet zobrata attēlu, kas tiek saukts par izvēlnes pogu **Iestatījumi**. Atverot izvēlni **Iestatījumi**, parādīsies vairākas opcijas. Atlasot **Opcijas** atvērsies lietotāja lapa **Opcijas**. Ir pieejamas četras opciju cilnes: 

-   **Vizuāls**: izvelieties lapas krāsu dizainu un elementu noklusējuma izmēru.
-   **Preferences**: izvēlieties noklusējuma iestatījumus, kas tiek lietoti ikreiz, kad atverat programmatūru Finance and Operations, tostarp uzņēmuma, sākotnējās lapas un noklusējuma skata/rediģēšanas režīma iestatījumus (kas nosaka, vai lapa ir bloķēta skatīšanai vai atvērta rediģēšanai ikreiz, kad to atverat). Var atrast arī valodas, laika joslu un datumu, laiku un skaitļu formātu opcijas. Visbeidzot, šajā lapā ir vairākas dažādas preferences, kas atšķirsies dažādos laidienos.
-   **Konts**: norādiet lietotāja ID un citas ar kontu saistītas opcijas.
-   **Darbplūsma**: izvēlieties ar darbplūsmu saistītas opcijas.

## <a name="implicit-personalizations"></a>Netiešas personalizācijas
Netiešas personalizācijas ir tās personalizācijas, ko veicat vienkārši, izmantojot atsevišķas vadīklas, kas atcerēsies savu pašreizējo redzamo stāvokli. 

**Režģa kolonnas**: pielāgojiet saraksta kolonnu platumu, atlasot esošo izmēra maiņas joslu pa kreisi vai pa labi no virsraksta kolonnas un pavirzot to pa kreisi vai pa labi līdz nepieciešamajam platumam. Programmatūrā Finance and Operations tiek saglabāts vēlamais platums, un tas tiek izmantots šīs kolonnas rādīšanai ikreiz, kad atverat lapu ar šo sarakstu. 

**Kopsavilkuma cilnes**: dažām lapām ir paplašināmās sadaļas, ko sauc par kopsavilkuma cilnēm. Programmatūrā Finance and Operations tiek saglabāta informācija par to, kuras kopsavilkuma cilnes ir izvērstas un kuras kopsavilkuma cilnes ir sakļautas. Katru reizi, kad atgriezīsieties šajā lapā, tās pašas kopsavilkuma cilnes tiks izvērstas vai sakļautas, atkarībā no tā, kā jūs pēdējo reizi tās lietojāt. Šajā rakstā mēs izskaidrosim, kā mainīt kopsavilkuma ciļņu sadaļu secību. Dažos gadījumos kopsavilkuma cilnes sakļaušana var uzlabot veiktspēju, jo šādā gadījumā programmatūrā Finance and Operations nav jāizgūst informācija par šo kopsavilkuma cilni, kamēr tā nav izvērsta. 

**Papildinformācija**: dažām lapām ir sadaļa ar nosaukumu Papildinformācijas rūts. Šī rūts satur tikai lasāmu informāciju, kas saistīta ar pašreizējo lapas tēmu. Katru sadaļu papildinformācijas rūtī sauc par papildinformāciju. Papildinformāciju varat izvērst vai sakļaut, un šis stāvoklis tiek saglabāts programmatūrā Finance and Operations. Dažos gadījumos papildinformācijas sakļaušana var uzlabot veiktspēju, jo šādā gadījumā programmatūrā Finance and Operations nav jāizgūst informācija par šo papildinformāciju, kamēr tā nav izvērsta.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Tiešas personalizācijas, izmantojot rīkjoslu Personalizēšana
Katrai personai un uzņēmumam ir savi uzskati par to, kuri dati ir viņiem vissvarīgākie, vai kuri dati nav nepieciešami viņu uzņēmējdarbības veidam. Iespējas pielāgot to, kā informācija tiek kārtota, izmantota un pat paslēpta, ir ļoti svarīgs faktors, kā personalizēt programmatūras Finance and Operations lietošanu un padarīt to efektīvu. 

Tiešā personalizēšana ir personalizēšana, ko veicat ar tiešu mērķi mainīt lapas elementa izskatu vai darbību, izvēloties personalizēšanas izvēlni. Visparastākais tiešās personalizēšanas veids ir personalizēšana, ar labo peles pogu noklikšķinot uz elementa un atlasot vienumu **Personalizēt**. (Ņemiet vērā, ka var personalizēt visus lapā esošos elementus.) Ja izvēlaties šo personalizēšanas metodi, tiek parādīts elementa rekvizītu logs. 

[![Elementa rekvizītu personalizēšana](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Šādā veidā jūs personalizējat elementu savā lapā, ja vēlaties vienkārši mainīt elementa etiķetes, paslēpt elementu, lai tas nebūtu redzams lapā (nekādi dati netiek mainīti, vienkārši netiek rādīta kāda informācija), iekļaut informāciju kopsavilkuma cilnes sadaļā (ja elements ir kopsavilkuma cilnē), izlaist lauku tabulēšanas laikā vai aizliegt datu mainīšanu, atzīmējot tos kā “Nerediģēt”. 

Ja vēlaties pārvietot vai paslēpt elementus vai veikt vairākas izmaiņas, varat izmantot rīkjoslu Personalizēšana, kas pieejama elementu rekvizītu logā, izvēloties **Personalizēt šo formu**. Rīkjosla Personalizēšana ir pieejama arī formas darbību rūtī, cilnes **Opcijas** grupā Personalizēt. Atlasiet **Personalizēt šo formu**, un būs redzama rīkjosla Personalizēšana. 

[![Rīkjosla Personalizēšana](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Rīkjoslā Personalizēšana ir pieejamas vairākas personalizēšanas darbības. Izvēlieties **Atlases** rīku, ja vēlaties atlasīt un mainīt daudzu elementu rekvizītus atsevišķi. Pirmkārt, noklikšķiniet uz Atlases rīka un pēc tam noklikšķiniet uz elementa, kura rekvizītus vēlaties mainīt. Atlasot elementu, tiks atvērts elementa rekvizītu logs un jūs varat mainīt jebkurus šī elementa rekvizītus. Šo procesu var atkārtot citiem formas elementiem, kuri ir personalizējami. Dažos gadījumos varat atlasīt elementu un redzēt, ka dažus no rekvizītiem nevar mainīt. Tas nozīmē, ka, pamatojoties uz to, kā tiek izmantots pašreizējais elements, Finance and Operations nevar jums ļaut mainīt šo rekvizītu. Piemēram, jūs nevarat paslēpt lauku, kas ir obligāts. 

Izvēlieties **Pārvietošanas** rīku, kad vēlaties atlasīt un pārvietot elementu uz citu vietu pašreizējā elementu grupā. (Elementu nevar pārvietot ārpus tā pamata grupas). Pirmkārt, noklikšķiniet uz Pārvietošanas rīka un pēc tam noklikšķiniet uz elementa, kuru vēlaties pārvietot Kad noklikšķināt uz pārvietojamā elementa, programmatūrā Finance and Operations šī forma tiek skenēta, lai noteiktu, kur šo elementu var pārvietot, un izveidotu vairākas “nomešanas zonas”, kuras tiek apzīmētas ar krāsainu, treknu līniju blakus apgabalam, kur elementu var nomest, kad šo elementu velkat pašreizējās grupas ietvaros. 

Izvēlieties **Paslēpšanas** rīku, lai atlasītu un paslēptu elementu. Lai paslēptu elementu, vienkārši izvēlieties Paslēpšanas rīku un noklikšķiniet uz elementa, ko vēlaties paslēpt. Kad jūs izvēlaties Paslēpšanas rīku, visi pašlaik paslēptie elementi kļūs redzami un tiks parādīti ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal parādīt redzamus. Izvēlieties Atlases rīku, lai redzētu, kā lapa izskatīsies, kad atlasītie elementi būs paslēpti. Izvēlieties **Kopsavilkuma** rīku, kad vēlaties, lai kopsavilkuma cilnes kopsavilkuma apgabalā tiktu parādīts skaitliskais vai virknes lauks. Kopsavilkuma rīks attieksies tikai uz laukiem, kas ir ietverti kopsavilkuma sadaļā. Kad izvēlaties kopsavilkuma rīku, programmatūrā Finance and Operations tiek parādīti visi lauki, kas ir atlasīti kā kopsavilkuma lauki, ietverot tos ēnotā konteinerā. Var interaktīvi pievienot vai noņemt laukus no kopsavilkuma cilnes kopsavilkuma, noklikšķinot uz attiecīgā lauka. 

Izvēlieties **izlaišanas** rīku, lai noņemtu elementu no lapas tastatūras tabulācijas secības. Kad izvēlaties izlaišanas rīku, visi pašlaik izlaistie elementi tiek parādīti ēnotā konteinerā, lai jūs varētu tos vēlreiz izvēlēties un ietvert tabulācijas secībā, atlasot kādu no izlaistajiem elementiem. 

Izvēlieties **Rediģēšanas** rīku, lai atzīmētu elementu kā rediģējamu vai nerediģējamu. Kad jūs izvēlaties Rediģēšanas rīku, visi nerediģējamie elementi kļūs redzami ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal padarīt rediģējamus. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus. Šie lauki tiks parādīti ar slēdzenes ikonu blakus tiem. 

Izvēlieties **Pievienošanas** rīku, lai pievienotu lauku savai lapai. Ar pievienošanas rīku nevar izveidot jaunu lauku, bet var pievienot laukus, kas ir daļa no pašreizējās lapas definīcijas, bet nav redzami lapā. Kad jūs izvēlaties Pievienošanas rīku, vispirms atlasiet grupu vai apgabalu, kur vēlaties pievienot lauku. Dialoglodziņā parādīsies lauku saraksts, kas saistīti ar atlasīto sadaļu. No šī dialoglodziņa varat atlasīt vienu vai vairākus pievienojamos laukus un noklikšķināt uz Ievietot. Ja vēlāk vēlaties noņemt lauku, kuru esat pievienojis iepriekš, atkārtojiet šo procesu, bet vienkārši notīriet lauku, kuru esat pievienojis iepriekš. 

Izvēlieties pogu **Pārvaldīt**, lai skatītu ar visām pašreizējas lapas personalizēšanas darbībām saistīto pārvaldības opciju sarakstu. 

Izvēlieties vienumu **Notīrīt**, lai atiestatītu lapas noklusējuma instalēto stāvokli. Tādējādi tiek noņemti visas pašreizējās lapas personalizēšanas iestatījumi. Nav pieejama atsaukšanas darbība, tāpēc izmantojiet šo opciju tikai gadījumā, ja esat pārliecināts, ka vēlaties atiestatīt lapu. 

Izvēlieties **Importēt**, lai izmantotu personalizāciju no personalizēšanas faila, kuru jūs vai kāds cits iepriekš izveidojis šai lapai. Importējot personalizāciju, tiks notīrītas jebkuras personalizācijas, ko esat veicis savā lapā un tā vietā tiks izmantotas visas personalizācijas no atlasītā faila. Ja vēlaties saglabāt vai koplietot personalizāciju, atlasīsiet opciju **Eksportēt**, lai saglabātu personalizācijas failā. 

Izvēlieties pogu **Aizvērt**, lai aizvērtu rīkjoslu un atgrieztu lapu iepriekšējā interaktīvā stāvoklī. 

Ar Personalizācijas rīkjoslu, saglabāšana notiek netieši. Jūsu personalizācijas stājas spēkā uzreiz pēc to veikšanas un nav nepieciešams noklikšķināt uz pogas **Saglabāt**. Dažos gadījumos, atlasot kādu no rīkiem, blakus kādam elementam tiek rādīta slēdzenes ikona. Tas nozīmē, ka, lai lapa darbotos pareizi, nevarat mainīt ar atlasīto rīku saistītos rekvizītus. Atverot rīkjoslu Personalizēšana, lapa kļūst neinteraktīva. Tajā nevar ievadīt datus vai izvērst vai sakļaut sadaļas.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Tiešā personalizēšana: elementa vai saraksta pievienošana darbvietai
Dažās lapās ar sarakstiem būs pieejams papildu personalizēšanas līdzeklis — tas atrodas darbību rūtī, cilnes Opcijas grupā Personalizēt. Atlasiet **Pievienot darbvietai**, lai atvērtu nolaižamo sarakstu, kas sniedz iespēju parādīt informāciju darbvietas pašreizējā sarakstā (filtrētu un kārtotu vai pēc noklusējuma) kā sarakstu vai kā kopsavilkuma elementu (kuru var izmantot, lai rādītu krājumu skaitu sarakstā). 

[![Pievienošana darbvietai](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Lai pievienotu sarakstu darbvietai, vispirms kārtojiet vai filtrējiet sarakstu ar tādu informāciju, kuru jūs vēlētos redzēt savā darbvietā, un pēc tam atzīmējiet dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Saraksts** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Saraksts**, atvērsies dialoglodziņš, kas ļauj izvēlēties kolonnas, kuras vēlaties redzēt sarakstā un saraksta etiķete, kā tā parādīsies darbvietā. 

Lai pievienotu elementu darbvietai, vispirms filtrējiet sarakstu, lai tajā būtu dati, kurus vēlaties apkopot (vai vēlaties tiem ātri piekļūt). Pēc tam atveriet nolaižamo dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Elements** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Elements**, tiks atvērts dialoglodziņš, ļaujot sniegt elementam etiķeti un izlemt, vai rūtī tiks parādīts skaits. Novietojot darbvietā, elements ļauj atvērt pašreizējo lapu no darbvietas, un rādīt informācijas sarakstu, kas saistīta ar šo elementu. 

Kad saraksts vai elements tiek pievienots darbvietai, varat atvērt šo darbvietu un atkārtoti sakārtot sarakstu vai elementu grupā, kurā tas ir novietots.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Tieša personalizēšana: kopsavilkuma pievienošana no darbvietas informācijas panelim
Dažās darbvietās ir ietverti skaitīšanas elementi (elementi, uz kuriem ir skaitļi), ko vēlaties redzēt arī informācijas panelī. Darbvietā ar peles labo pogu noklikšķiniet uz skaitīšanas elementa un atlasiet vienumu **Personalizēt**. Atlasiet **Piespraust informācijas panelim**. Nākamreiz pārejot uz (un atsvaidzinot) atlasīto informācijas paneli, jūs redzēsiet šo skaitli zem šīs darbvietas navigācijas elementa informācijas panelī.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Tiešā personalizēšana: sava informācijas paneļa personalizēšana
Informācijas panelis bieži ir pirmā lapa, ko redzat, atverot programmatūru Finance and Operations. Informācijas paneli var personalizēt, lai pārdēvētu darbvietas navigācijas elementus, parādītu tikai elementus, ko vēlaties redzēt, pārdēvētu elementus vai sakārtotu elementus secībā, kādā vēlaties tos redzēt. Lai personalizētu informācijas paneli, atlasiet jebkuru elementu un noklikšķiniet ar peles labo pogu, lai atvērtu konteksta izvēlni. Konteksta izvēlnē atlasiet **Personalizēt**. Ja atlasītais elements ir tas, ko vēlaties paslēpt, vai pārdēvēt, vai izlaist, jūs varat veikt izmaiņas tieši parādītajā rekvizītu logā. Ja vēlaties sakārtot elementus, atlasiet **Personalizēt šo formu** rekvizītu logā, lai atvērtu rīkjoslu Personalizēšana. Pēc tam elementu izkārtošanai var izmantot Pārvietošanas rīku.

## <a name="administration-of-personalization"></a>Personalizēšanas administrēšana
Pēc lapas personalizēšanas savas personalizācijas varat kopīgot ar citiem lietotāja lietotājiem, eksportējot personalizēto lapu. Pēc tam varat lūgt citiem lietotājiem pāriet uz šo personalizēto lapu un importēt jūsu izveidoto personalizēšanas failu.

Lietotāji ar administratora privilēģijām lapā **Personalizācija** var arī pārvaldīt personalizācijas citiem lietotājiem. Šai lapai ir četras cilnēs: 

- **Sistēma** – varat īslaicīgi atspējot vai izslēgt visas personalizācijas sistēmā. Tādā gadījumā jūs personalizācijas nedzēšat. Tā vietā jūs tikai atiestatāt visas lapas uz to noklusējuma stāvokli. Ja vēlāk personalizācijas no jauna iespējojat, katrai lietotāja lapai tiek atjaunotas visas personalizācijas. Varat arī dzēst visas personalizācijas visiem lietotājiem. Ņemiet vērā, ka, dzēšot personalizācijas, nevar automātiski atkārtoti iespējot personalizācijas no sistēmas. Tādēļ, pirms veicat šo darbību, ir jāpārliecinās, ka ir eksportētas visas personalizācijas, kuras vēlāk varētu būt nepieciešams importēt.
- **Lietotāji** – varat norādīt, vai katrs lietotājs var veikt netiešu personalizēšanu vai tiešu personalizēšanu. Varat arī norādīt, vai katrs lietotājs var veikt netiešu vai tiešu personalizēšanu konkrētā lapā. Visbeidzot, varat importēt, eksportēt, vai dzēst personalizācijas katram lietotājam.
- **Importēt** – varat importēt personalizāciju vienam vai vairākiem lietotājiem. Šī cilne ir jāizmanto pēc tam, kad esat izveidojis personalizāciju kādā lapā vai darbvietā, un pēc tam šo personalizāciju esat eksportējis kā personalizēšanas failu. Lai importētu savu personalizēšanas failu un to lietotu vienam vai vairākiem lietotājiem, visu lietotāju sarakstā atlasiet atsevišķus lietotājus vai filtrējiet sarakstu pēc noteiktas lomas un pēc tam atlasiet lietotājus šajā lomā. Kad esat atlasījis lietotājus, kuri izmantos jūsu personalizāciju, noklikšķiniet uz **Importēt** un atlasiet savu personalizēšanas failu. Personalizācija tiks validēta un visiem atlasītajiem lietotājiem tiks lietota nākamajā reizē, kad viņi atvērs atlasīto lapu.
- **Notīrīt** – varat notīrīt lapas vai darbvietas personalizācijas vienam vai vairākiem lietotājiem. Vispirms atlasiet lapu vai darbvietu, kurai notīrīt personalizācijas. Pēc tam visu lietotāju sarakstā atlasiet atsevišķus lietotājus vai filtrējiet pēc noteiktas lomas un pēc tam atlasiet lietotājus šajā lomā. Kad esat atlasījis gan lapu vai darbvietu, gan lietotājus, noklikšķiniet uz **Notīrīt**. Tiek notīrītas visas personalizācijas, ko atlasītie lietotāji ir lietojuši atlasītajai lapai vai darbvietai. Šo darbību nevar atsaukt. Taču, ja lapai vai darbvietai ir saglabāta personalizācija, šo personalizāciju var importēt atkārtoti.

## <a name="personalization-of-inventory-dimensions"></a>Krājumu dimensiju personalizēšana

Kad personalizējat krājumu dimensiju iestatījumus lapā, ņemiet vērā iestatījumus, kas izveidoti, izmantojot opciju **Parādīt dimensijas**. Piemēram, ja veicat personalizēšanu ar mērķi paslēpt partijas numuru krājumu dimensijas kolonnu, un kolonna tiek parādīta nākamreiz, kad tiek atvērta lapa, iespējamais iemesls var būt tas, ka dimensiju parādīšanas iestatījumi nosaka, kādas krājumu dimensiju kolonnas tiek parādītas. 

Dimensiju parādīšanas iestatījumi tiek lietoti visās lapās, un šiem iestatījumiem ir virsroka pār jebkādiem personalizētiem krājumu dimensiju lauku iestatījumiem atsevišķās lapās. 

Piemēram, lai netiktu rādīta partijas numuru krājumu dimensijas kolonna, šī dimensija ir jānotīra kā daļa no tabulas opcijas **Parādīt dimensijas**. Šīs izmaiņas attiektos ne tikai uz konkrēto lapu, bet uz visām lapām.

