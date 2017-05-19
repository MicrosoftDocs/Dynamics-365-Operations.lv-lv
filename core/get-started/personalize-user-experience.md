---
title: "Personalizēt lietotāja pieredzi"
description: "Šajā rakstā ir paskaidrots, kā var personalizēt programmatūru Microsoft Dynamics 365 for Operations."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 734bf8a5cd71d218942e1a57fbb6af8fef4dc998
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="personalize-the-user-experience"></a>Personalizēt lietotāja pieredzi

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā var personalizēt programmatūru Microsoft Dynamics 365 for Operations.

Programmatūrā Microsoft Dynamics 365 for Operations ir pieejami daudzi personalizēšanas veidi. Dažas personalizācijas ir no opciju saraksta iestatīšanas lapā veiktās atlases. Dažas personalizēšanas darbības ir netiešas, piemēram, Dynamics 365 for Operations seko režģa kolonnu platumam, ja to koriģējat, un kopsavilkuma ciļņu izvēršanas/sakļaušanas stāvoklim. Citas personalizācijas ir tiešas. Tiešajām personalizācijām jūs ieejat interaktīvās personalizēšanas režīmā un modificējat lapas izskatu, tieši pārvaldot to, kā elementi tiek parādīti vai darbojas lapā. 

Jebkura veida personalizēšana, ko lietotājs veic programmatūrā Dynamics 365 for Operations, attiecas tikai uz šo lietotāju neatkarīgi no uzņēmuma, ar kuru lietotājs mijiedarbojas. Izmaiņas, ko lietotājs veic lapā, neietekmē citus lietotājus sistēmā.

## <a name="systemwide-options-for-the-current-user"></a>Sistēmas līmeņa opcijas pašreizējam lietotājam
Navigācijas joslā jūs atradīsiet zobrata attēlu, kas tiek saukts par izvēlnes pogu **Iestatījumi**. Atverot izvēlni **Iestatījumi**, parādīsies vairākas opcijas. Atlasot **Opcijas** atvērsies lietotāja lapa **Opcijas**. Tur atradīsiet četras opciju cilnes: **Vizuāls**, **Preferences**, **Konts** un **Darbplūsma**.

-   **Vizuāls:**izmantojiet, lai izvēlētos savas lapas krāsu dizainu un elementu noklusējuma izmēru.
-   **Preferences:** šajā cilnē varat izvēlēties noklusējuma iestatījumus, kas tiek lietoti ikreiz, kad atverat programmatūru Dynamics 365 for Operations, tostarp uzņēmuma, sākotnējās lapas un noklusējuma skata/rediģēšanas režīma iestatījumus (kas nosaka, vai lapa ir bloķēta skatīšanai vai atvērta rediģēšanai ikreiz, kad to atverat). Var atrast arī valodas, laika joslu un datumu, laiku un skaitļu formātu opcijas. Visbeidzot, šajā lapā ir vairākas dažādas preferences, kas atšķirsies dažādos laidienos.
-   **Konts:**izmantot, lai sniegtu savu lietotāja ID un citas ar kontu saistītas opcijas.
-   **Darbplūsma:**šeit var izvēlēties ar darbplūsmu saistītas opcijas.

## <a name="implicit-personalizations"></a>Netiešas personalizācijas
Netiešas personalizācijas ir tās personalizācijas, ko veicat vienkārši, izmantojot atsevišķas vadīklas, kas atcerēsies savu pašreizējo redzamo stāvokli. 

**Režģa kolonnas:** saraksta kolonnu platumu var pielāgot, atlasot esošo izmēra maiņas joslu pa kreisi vai pa labi no virsraksta kolonnas un pavirzot to pa kreisi vai pa labi līdz nepieciešamajam platumam. Programmatūrā Dynamics 365 for Operations tiek saglabāts vēlamais platums un tas tiek izmantots šīs kolonnas rādīšanai ikreiz, kad atverat lapu ar šo sarakstu. 

**Kopsavilkuma cilnes:** dažām lapām ir paplašināmās sadaļas, ko sauc par kopsavilkuma cilnēm. Programmatūrā Dynamics 365 for Operations tiek saglabāta informācija par to, kuras kopsavilkuma cilnes ir izvērstas un kuras kopsavilkuma cilnes ir sakļautas. Katru reizi, kad atgriezīsieties šajā lapā, tās pašas kopsavilkuma cilnes tiks izvērstas vai sakļautas, atkarībā no tā, kā jūs pēdējo reizi tās lietojāt. Šajā rakstā mēs izskaidrosim, kā mainīt kopsavilkuma ciļņu sadaļu secību. Dažos gadījumos kopsavilkuma cilnes sakļaušana var uzlabot veiktspēju, jo šādā gadījumā programmatūrā Dynamics 365 for Operations nav jāizgūst informācija par šo kopsavilkuma cilni, kamēr tā nav izvērsta. 

**Papildinformācija:** dažām lapām ir sadaļa ar nosaukumu papildinformācijas rūts. Šī rūts satur tikai lasāmu informāciju, kas saistīta ar pašreizējo lapas tēmu. Katru sadaļu papildinformācijas rūtī sauc par papildinformāciju. Varat izvērst vai sakļaut papildinformāciju, un šis stāvoklis tiek saglabāts programmatūrā Dynamics 365 for Operations. Dažos gadījumos papildinformācijas sakļaušana var uzlabot veiktspēju, jo šādā gadījumā programmatūrā Dynamics 365 for Operations nav jāizgūst informācija par šo papildinformāciju, kamēr tā nav izvērsta.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Tiešas personalizācijas, izmantojot rīkjoslu Personalizēšana
Katrai personai un uzņēmumam ir savi uzskati par to, kuri dati ir viņiem vissvarīgākie, vai kuri dati nav nepieciešami viņu uzņēmējdarbības veidam. Iespējas pielāgot to, kā informācija tiek kārtota, izmantota un pat paslēpta, ir ļoti svarīgs faktors, kas ļauj personalizēt programmatūras Dynamics 365 for Operations lietošanu un padarīt to efektīvu. 

Tiešā personalizēšana ir personalizēšana, ko veicat ar tiešu mērķi mainīt lapas elementa izskatu vai darbību, izvēloties personalizēšanas izvēlni. Visparastākais tiešās personalizēšanas veids ir personalizēšana, ar labo peles pogu noklikšķinot uz elementa un atlasot vienumu **Personalizēt**. (Ņemiet vērā, ka var personalizēt visus lapā esošos elementus.) Ja izvēlaties šo personalizēšanas metodi, tiek parādīts elementa rekvizītu logs. 

[![Elementa rekvizītu personalizēšana](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Šādā veidā jūs personalizējat elementu savā lapā, ja vēlaties vienkārši mainīt elementa etiķetes, paslēpt elementu, lai tas nebūtu redzams lapā (nekādi dati netiek mainīti, vienkārši netiek rādīta kāda informācija), iekļaut informāciju kopsavilkuma cilnes sadaļā (ja elements ir kopsavilkuma cilnē), izlaist lauku tabulēšanas laikā vai aizliegt datu mainīšanu, atzīmējot tos kā “Nerediģēt”. 

Ja vēlaties pārvietot vai paslēpt elementus vai veikt vairākas izmaiņas, varat izmantot rīkjoslu Personalizēšana, kas pieejama elementu rekvizītu logā, izvēloties **Personalizēt šo formu**. Rīkjosla Personalizēšana ir pieejama arī formas darbību rūtī cilnes **Opcijas** grupā Personalizēt. Atlasiet **Personalizēt šo formu** un jūs redzēsiet rīkjoslu Personalizēšana. 

[![Rīkjosla Personalizēšana](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Rīkjoslā Personalizēšana ir pieejamas vairākas personalizēšanas darbības. Izvēlieties **Atlases** rīku, ja vēlaties atlasīt un mainīt daudzu elementu rekvizītus atsevišķi. Pirmkārt, noklikšķiniet uz Atlases rīka un pēc tam noklikšķiniet uz elementa, kura rekvizītus vēlaties mainīt. Atlasot elementu, tiks atvērts elementa rekvizītu logs un jūs varat mainīt jebkurus šī elementa rekvizītus. Šo procesu var atkārtot citiem formas elementiem, kuri ir personalizējami. Dažos gadījumos varat atlasīt elementu un redzēt, ka dažus no rekvizītiem nevar mainīt. Tas nozīmē, ka, pamatojoties uz pašreizējā elementa lietošanas veidu, programmatūrā Dynamics 365 for Operations nevar mainīt šo rekvizītu. Piemēram, jūs nevarat paslēpt lauku, kas ir obligāts. 

Izvēlieties **Pārvietošanas** rīku, kad vēlaties atlasīt un pārvietot elementu uz citu vietu pašreizējā elementu grupā. (Elementu nevar pārvietot ārpus tā pamata grupas). Pirmkārt, noklikšķiniet uz Pārvietošanas rīka un pēc tam noklikšķiniet uz elementa, kuru vēlaties pārvietot Kad noklikšķināt uz pārvietojamā elementa, programmatūrā Dynamics 365 for Operations tiek skenēta veidlapa, lai noteiktu, kur šo elementu var pārvietot, un izveidotu vairākas “nomešanas zonas”, kuras tiek apzīmētas ar krāsainu, treknu līniju blakus apgabalam, kur elementu var nomest, kad velkat elementu pašreizējās grupas ietvaros. 

Izvēlieties **Paslēpšanas** rīku, lai atlasītu un paslēptu elementu. Lai paslēptu elementu, vienkārši izvēlieties Paslēpšanas rīku un noklikšķiniet uz elementa, ko vēlaties paslēpt. Kad jūs izvēlaties Paslēpšanas rīku, visi pašlaik paslēptie elementi kļūs redzami un tiks parādīti ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal parādīt redzamus. Izvēlieties Atlases rīku, lai redzētu, kā lapa izskatīsies, kad atlasītie elementi būs paslēpti. Izvēlieties **Kopsavilkuma** rīku, kad vēlaties, lai kopsavilkuma cilnes kopsavilkuma apgabalā tiktu parādīts skaitliskais vai virknes lauks. Kopsavilkuma rīks attieksies tikai uz laukiem, kas ir ietverti kopsavilkuma sadaļā. Kad izvēlaties kopsavilkuma rīku, programmatūrā Dynamics 365 for Operations tiek parādīti visi lauki, kas ir atlasīti kā kopsavilkuma lauki, ietverot tos ēnotā konteinerā. Var interaktīvi pievienot vai noņemt laukus no kopsavilkuma cilnes kopsavilkuma, noklikšķinot uz attiecīgā lauka. 

Izvēlieties **izlaišanas** rīku, lai noņemtu elementu no lapas tastatūras tabulācijas secības. Kad izvēlaties izlaišanas rīku, visi pašlaik izlaistie elementi tiek parādīti ēnotā konteinerā, lai jūs varētu tos vēlreiz izvēlēties un ietvert tabulācijas secībā, atlasot kādu no izlaistajiem elementiem. 

Izvēlieties **Rediģēšanas** rīku, lai atzīmētu elementu kā rediģējamu vai nerediģējamu. Kad jūs izvēlaties Rediģēšanas rīku, visi nerediģējamie elementi kļūs redzami ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal padarīt rediģējamus. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus. Šie lauki tiks parādīti ar slēdzenes ikonu blakus tiem. 

Izvēlieties **Pievienošanas** rīku, lai pievienotu lauku savai lapai. Ar pievienošanas rīku nevar izveidot jaunu lauku, bet var pievienot laukus, kas ir daļa no pašreizējās lapas definīcijas, bet nav redzami lapā. Kad jūs izvēlaties Pievienošanas rīku, vispirms atlasiet grupu vai apgabalu, kur vēlaties pievienot lauku. Dialoglodziņā parādīsies lauku saraksts, kas saistīti ar atlasīto sadaļu. No šī dialoglodziņa varat atlasīt vienu vai vairākus pievienojamos laukus un noklikšķināt uz Ievietot. Ja vēlāk vēlaties noņemt lauku, kuru esat pievienojis iepriekš, atkārtojiet šo procesu, bet vienkārši notīriet lauku, kuru esat pievienojis iepriekš. 

Izvēlieties pogu **Pārvaldīt**, lai skatītu ar visām pašreizējas lapas personalizēšanas darbībām saistīto pārvaldības opciju sarakstu. 

Izvēlieties vienumu **Notīrīt**, lai atiestatītu lapas noklusējuma instalēto stāvokli. Tādējādi tiek noņemti visas pašreizējās lapas personalizēšanas iestatījumi. Nav pieejama atsaukšanas darbība, tāpēc izmantojiet šo opciju tikai gadījumā, ja esat pārliecināts, ka vēlaties atiestatīt lapu. 

Izvēlieties **Importēt**, lai izmantotu personalizāciju no personalizēšanas faila, kuru jūs vai kāds cits iepriekš izveidojis šai lapai. Importējot personalizāciju, tiks notīrītas jebkuras personalizācijas, ko esat veicis savā lapā un tā vietā tiks izmantotas visas personalizācijas no atlasītā faila. Ja vēlaties saglabāt vai koplietot personalizāciju, atlasīsiet opciju **Eksportēt**, lai saglabātu personalizācijas failā. 

Izvēlieties pogu **Aizvērt**, lai aizvērtu rīkjoslu un atgrieztu lapu iepriekšējā interaktīvā stāvoklī. 

Ar Personalizācijas rīkjoslu, saglabāšana notiek netieši. Jūsu personalizācijas stājas spēkā uzreiz pēc to veikšanas un nav nepieciešams noklikšķināt uz pogas **Saglabāt**. Dažos gadījumos, atlasot kādu no rīkiem, blakus kādam elementam tiek rādīta slēdzenes ikona. Tas nozīmē, ka, lai lapa darbotos pareizi, nevarat mainīt ar atlasīto rīku saistītos rekvizītus. Atverot rīkjoslu Personalizēšana, lapa kļūst neinteraktīva. Tajā nevar ievadīt datus vai izvērst vai sakļaut sadaļas.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Tiešā personalizēšana: elementa vai saraksta pievienošana darbvietai
Dažās lapās ar sarakstiem darbību rūtī būs pieejams papildu personalizēšanas līdzeklis cilnes Opcijas grupā Personalizēt. Atlasiet **Pievienot darbvietai**, lai atvērtu nolaižamo sarakstu, kas sniedz iespēju parādīt informāciju pašreizējā sarakstā (filtrētu un kārtotu vai pēc noklusējuma) Darbvietā kā sarakstu vai kopsavilkuma elementu (ko var izmantot, lai rādītu krājumu skaitu sarakstā). 

[![Pievienošana darbvietai](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Lai pievienotu sarakstu darbvietai, vispirms kārtojiet vai filtrējiet sarakstu ar tādu informāciju, kuru jūs vēlētos redzēt savā darbvietā, un pēc tam atzīmējiet dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Saraksts** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Saraksts**, atvērsies dialoglodziņš, kas ļauj izvēlēties kolonnas, kuras vēlaties redzēt sarakstā un saraksta etiķete, kā tā parādīsies darbvietā. 

Lai pievienotu elementu darbvietai, vispirms filtrējiet sarakstu, lai tajā būtu dati, kurus vēlaties apkopot (vai vēlaties tiem ātri piekļūt). Pēc tam atveriet nolaižamo dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Elements** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Elements**, tiks atvērts dialoglodziņš, ļaujot sniegt elementam etiķeti un izlemt, vai rūtī tiks parādīts skaits. Novietojot darbvietā, elements ļauj atvērt pašreizējo lapu no darbvietas, un rādīt informācijas sarakstu, kas saistīta ar šo elementu. 

Kad saraksts vai elements tiek pievienots darbvietai, varat atvērt šo darbvietu un atkārtoti sakārtot sarakstu vai elementu grupā, kurā tas ir novietots.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Tieša personalizēšana: kopsavilkuma pievienošana no darbvietas informācijas panelim
Dažās darbvietās ir ietverti skaitīšanas elementi (elementi, uz kuriem ir skaitļi), ko vēlaties redzēt arī informācijas panelī. Darbvietā ar peles labo pogu noklikšķiniet uz skaitīšanas elementa un atlasiet vienumu **Personalizēt**. Atlasiet **Piespraust informācijas panelim**. Nākamreiz pārejot uz (un atsvaidzinot) atlasīto informācijas paneli, jūs redzēsiet šo skaitli zem šīs darbvietas navigācijas elementa informācijas panelī.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Tiešā personalizēšana: sava informācijas paneļa personalizēšana
Informācijas panelis bieži ir pirmā lapa, ko redzat, atverot programmatūru Dynamics 365 for Operations. Informācijas paneli var personalizēt, lai pārdēvētu darbvietas navigācijas elementus, parādītu tikai elementus, ko vēlaties redzēt, pārdēvētu elementus vai sakārtotu elementus secībā, kādā vēlaties tos redzēt. Lai personalizētu informācijas paneli, atlasiet jebkuru elementu un noklikšķiniet ar peles labo pogu, lai atvērtu konteksta izvēlni. Konteksta izvēlnē atlasiet **Personalizēt**. Ja atlasītais elements ir tas, ko vēlaties paslēpt, vai pārdēvēt, vai izlaist, jūs varat veikt izmaiņas tieši parādītajā rekvizītu logā. Ja vēlaties sakārtot elementus, atlasiet **Personalizēt šo formu** rekvizītu logā, lai atvērtu rīkjoslu Personalizēšana. Pēc tam elementu izkārtošanai var izmantot Pārvietošanas rīku.

## <a name="administration-of-personalization"></a>Personalizēšanas administrēšana
Ir iespējams personalizēt lapu un koplietot to ar citiem lietotājiem, vienkārši eksportējot personalizētu lapu un lūdzot citus lietotājus naviģēt uz personalizētu lapu un importēt personalizēšanas failu, ko esat izveidojis. Ja lietotājam ir administratora tiesības, viņš var arī pārvaldīt citu lietotāju personalizācijas lapā **Personalizēšanas iestatījumi**. Pārvietojieties uz b lapu. Lapā **Personalizēšana** jūs atradīsiet divas cilnes — vienu ar nosaukumu **Sistēma** un vienu ar nosaukumu**Lietotāji**. 

**Sistēma:** te var īslaicīgi atspējot vai "izslēgt" visas personalizācijas sistēmā. Tas nedzēš personalizācijas, bet gan atiestata visas formas uz noklusēto stāvokli. Personalizācijas var vēlāk atkārtoti iespējot, lai visas personalizācijas atkārtoti lietotu katra lietotāja formām. Varat arī dzēst visas personalizācijas visiem lietotājiem. Ņemiet vērā, ka, dzēšot personalizācijas, nevar automātiski atkārtoti iespējot personalizācijas no sistēmas. Pārliecinieties, ka eksportējāt personalizācijas, ko vēlaties vēlāk importēt, pirms šīs darbības veikšanas. 

**Lietotāji:** te varat izlemt katram lietotājam, vai viņš var veikt netiešu vai tiešu personalizēšanu. Varat arī izlemt, vai katrs lietotājs drīkst veikt tiešu vai netiešu personalizēšanu konkrētā formā. Visbeidzot, varat importēt, vai eksportēt, vai dzēst personalizācijas katram lietotājam. 

**Piezīme:** sākotnējā laidienā personalizēšanas administrēšana nodrošina tikai katra lietotāja pārvaldību.




