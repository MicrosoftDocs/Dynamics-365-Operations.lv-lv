---
title: "Personalizēt lietotāja pieredzi"
description: "Šajā rakstā ir paskaidrots, kā jūs varat personalizēt Microsoft Dynamics 365 operācijām."
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
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Personalizēt lietotāja pieredzi

Šajā rakstā ir paskaidrots, kā jūs varat personalizēt Microsoft Dynamics 365 operācijām.

Pastāv daudzi veidi personalizācijas Microsoft Dynamics 365 operācijām. Dažas personalizācijas ir no opciju saraksta iestatīšanas lapā veiktās atlases. Dažiem personalizācijas ir netieša, piemēram, Dynamics 365 operācijām pārraudzītu režģa kolonnu platumus ja jums pielāgot un izvērsta vai sakļauta valsts FastTabs. Citas personalizācijas ir tiešas. Tiešajām personalizācijām jūs ieejat interaktīvās personalizēšanas režīmā un modificējat lapas izskatu, tieši pārvaldot to, kā elementi tiek parādīti vai darbojas lapā. 

Visas personalizācijas, jebkura veida, ko lietotājs veic ar Dynamics 365 operācijām ir tikai, ka lietotājam neatkarīgi no uzņēmuma, kas lietotājam mijiedarbojoties ar. Izmaiņas, ko lietotājs veic lapā, neietekmē citus lietotājus sistēmā.

## <a name="systemwide-options-for-the-current-user"></a>Pašreizējam lietotājam veikt opcijas
Navigācijas joslā jūs atradīsiet zobrata attēlu, kas tiek saukts par izvēlnes pogu **Iestatījumi**. Atverot izvēlni **Iestatījumi**, parādīsies vairākas opcijas. Atlasot **Opcijas** atvērsies lietotāja lapa **Opcijas**. Tur atradīsiet četras opciju cilnes: **Vizuāls**, **Preferences**, **Konts** un **Darbplūsma**.

-   **Vizuāls: **izmantojiet, lai izvēlētos savas lapas krāsu dizainu un elementu noklusējuma izmēru.
-   **Preferences:** šeit var izvēlēties noklusējumus par katru reizi, kad atverat Dynamics 365 operācijām, ieskaitot uzņēmumu, sākotnējās lappuses un noklusējuma skatīt/rediģēt režīmā (kas nosaka, ja lapu apskatei slēgta vai atvērta rediģēšanai ikreiz, kad atverat to). Var atrast arī valodas, laika joslu un datumu, laiku un skaitļu formātu opcijas. Visbeidzot, šajā lapā ir vairākas dažādas preferences, kas atšķirsies dažādos laidienos.
-   **Konts: **izmantot, lai sniegtu savu lietotāja ID un citas ar kontu saistītas opcijas.
-   **Darbplūsma: **šeit var izvēlēties ar darbplūsmu saistītas opcijas.

## <a name="implicit-personalizations"></a>Netiešas personalizācijas
Netiešas personalizācijas ir tās personalizācijas, ko veicat vienkārši, izmantojot atsevišķas vadīklas, kas atcerēsies savu pašreizējo redzamo stāvokli. 

**Režģa kolonnas:** saraksta kolonnu platumu var pielāgot, atlasot esošo izmēra maiņas joslu pa kreisi vai pa labi no virsraksta kolonnas un pavirzot to pa kreisi vai pa labi līdz nepieciešamajam platumam. Dinamika 365 operācijām saglabās platumu, kas jums patīk un parādīt šai kolonnai ka platums, katru reizi atverot lapu ar šo sarakstu. 

**Kopsavilkuma cilnes:** dažām lapām ir paplašināmās sadaļas, ko sauc par kopsavilkuma cilnēm. Dinamika 365 operācijām tiks glabāti kura FastTabs ir paplašinātas un kura FastTabs ir sabrukušas. Katru reizi, kad atgriezīsieties šajā lapā, tās pašas kopsavilkuma cilnes tiks izvērstas vai sakļautas, atkarībā no tā, kā jūs pēdējo reizi tās lietojāt. Šajā rakstā mēs izskaidrosim, kā mainīt kopsavilkuma ciļņu sadaļu secību. Dažos gadījumos sabrukšanas FastTab var uzlabot veiktspēju, jo Dynamics 365 operācijām nav nepieciešams izgūt informāciju par šī FastTab līdz FastTab ir izvērsta. 

**Papildinformācija:** dažām lapām ir sadaļa ar nosaukumu papildinformācijas rūts. Šī rūts satur tikai lasāmu informāciju, kas saistīta ar pašreizējo lapas tēmu. Katru sadaļu papildinformācijas rūtī sauc par papildinformāciju. Var izvērst vai sakļaut lodziņš faktu un dinamiku 365 operācijām saglabās jūsu vēlmēm. Dažos gadījumos saplokošo lodziņš faktu var uzlabot veiktspēju, jo Dynamics 365 operācijām nav nepieciešams izgūt informāciju par šo faktu lādi līdz faktu lodziņš tiek paplašināts.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Tiešas personalizācijas, izmantojot rīkjoslu Personalizēšana
Katrai personai un uzņēmumam ir savi uzskati par to, kuri dati ir viņiem vissvarīgākie, vai kuri dati nav nepieciešami viņu uzņēmējdarbības veidam. Spēja pielāgot veidu, kā jūsu informācija ir pasūtītās sarunājušies ar, vai pat slēptās ir svarīgi prasmei veidot dinamiku 365 operācijām personīgo un ražošanas pieredzi. 

Nepārprotamu personalizācijas ir tās personalizācijas, ko veicat tieši ar nolūku mainīt izskatu vai uzvedību elements vai lapu, izvēloties personalizēšanas izvēlnē. Nepārprotamu personalizācijas visvienkāršākā veida ir vieta, kur jūs ar peles labo pogu noklikšķiniet uz elementa un atlasiet **personalizēšana**. (Ievērojiet, ka ne visi elementi jūsu lapā var personalizēt). Kad izvēlaties šo metodi, personalizācija, jūs redzēsiet elementa rekvizītu logā. 

[![Personalizējot elementa rekvizīti](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Šādā veidā jūs personalizējat elementu savā lapā, ja vēlaties vienkārši mainīt elementa etiķetes, paslēpt elementu, lai tas nebūtu redzams lapā (nekādi dati netiek mainīti, vienkārši netiek rādīta kāda informācija), iekļaut informāciju kopsavilkuma cilnes sadaļā (ja elements ir kopsavilkuma cilnē), izlaist lauku tabulēšanas laikā vai aizliegt datu mainīšanu, atzīmējot tos kā “Nerediģēt”. 

Ja vēlaties pārvietot vai paslēpt elementus vai veikt vairākas izmaiņas, varat izmantot rīkjoslu Personalizēšana, kas pieejama elementu rekvizītu logā, izvēloties **Personalizēt šo formu**. Rīkjosla Personalizēšana ir pieejama arī formas darbību rūtī cilnes **Opcijas** grupā Personalizēt. Atlasiet **Personalizēt šo formu** un jūs redzēsiet rīkjoslu Personalizēšana. 

[![Personalizācijas rīkjoslu](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Personalizācijas rīkjoslā ir personalizācija darbību skaits. Izvēlieties **Atlases** rīku, ja vēlaties atlasīt un mainīt daudzu elementu rekvizītus atsevišķi. Pirmkārt, noklikšķiniet uz Atlases rīka un pēc tam noklikšķiniet uz elementa, kura rekvizītus vēlaties mainīt. Atlasot elementu, tiks atvērts elementa rekvizītu logs un jūs varat mainīt jebkurus šī elementa rekvizītus. Šo procesu var atkārtot citiem formas elementiem, kuri ir personalizējami. Dažos gadījumos varat atlasīt elementu un redzēt, ka dažus no rekvizītiem nevar mainīt. Tas nozīmē, ka, pamatojoties uz to, kā pašreizējais elements tiek izmantots, Dynamics 365 operāciju nevar ļaut mainīt šo īpašumu. Piemēram, jūs nevarat paslēpt lauku, kas ir obligāts. 

Izvēlieties **Pārvietošanas** rīku, kad vēlaties atlasīt un pārvietot elementu uz citu vietu pašreizējā elementu grupā. (Elementu nevar pārvietot ārpus tā pamata grupas). Pirmkārt, noklikšķiniet uz Pārvietošanas rīka un pēc tam noklikšķiniet uz elementa, kuru vēlaties pārvietot Noklikšķinot uz elementa, kuru vēlaties pārvietot, Dynamics 365 operācijām skenēs form jāsaprot, kur šis elements var tikt pārvietota un izveidot virkni "nolaišanas zonas", kas liecina, kā krāsas, treknrakstu līnija pie apgabala, kur elements var tikt izbeigta, velciet elementu ap pašreizējo grupas ietvaros. 

Izvēlieties **Paslēpšanas** rīku, lai atlasītu un paslēptu elementu. Lai paslēptu elementu, vienkārši izvēlieties Paslēpšanas rīku un noklikšķiniet uz elementa, ko vēlaties paslēpt. Kad jūs izvēlaties Paslēpšanas rīku, visi pašlaik paslēptie elementi kļūs redzami un tiks parādīti ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal parādīt redzamus. Izvēlieties Atlases rīku, lai redzētu, kā lapa izskatīsies, kad atlasītie elementi būs paslēpti. Izvēlieties **Kopsavilkuma** rīku, kad vēlaties, lai kopsavilkuma cilnes kopsavilkuma apgabalā tiktu parādīts skaitliskais vai virknes lauks. Kopsavilkuma rīks attieksies tikai uz laukiem, kas ir ietverti kopsavilkuma sadaļā. Izvēloties kopsavilkuma līdzeklis, Dynamics 365 operācijām liecina visi lauki, kas atlasīti kopsavilkuma lauku, ko ieskāva viņus iekrāsotajā konteinerā. Var interaktīvi pievienot vai noņemt laukus no kopsavilkuma cilnes kopsavilkuma, noklikšķinot uz attiecīgā lauka. 

Izvēlieties **Skip** rīku, lai noņemtu elementu no lapas tastatūras tabulēšanas secība. Izvēloties izlaist rīks, visi pašlaik izlaistos elementi tiks parādīta ēnota traukā, tāpēc, ka jūs varat izvēlēties tos vēlreiz, lai padarītu tos daļa tabulēšanas secību, atlasot izlaistos elements. 

Izvēlieties **Rediģēšanas** rīku, lai atzīmētu elementu kā rediģējamu vai nerediģējamu. Kad jūs izvēlaties Rediģēšanas rīku, visi nerediģējamie elementi kļūs redzami ēnotā konteinerā, tādējādi varat izvēlēties, kurus elementus atkal padarīt rediģējamus. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus. Šie lauki tiks parādīti ar slēdzenes ikonu blakus tiem. 

Izvēlieties **Pievienošanas** rīku, lai pievienotu lauku savai lapai. Ar pievienošanas rīku nevar izveidot jaunu lauku, bet var pievienot laukus, kas ir daļa no pašreizējās lapas definīcijas, bet nav redzami lapā. Kad jūs izvēlaties Pievienošanas rīku, vispirms atlasiet grupu vai apgabalu, kur vēlaties pievienot lauku. Dialoglodziņā parādīsies lauku saraksts, kas saistīti ar atlasīto sadaļu. No šī dialoglodziņa varat atlasīt vienu vai vairākus pievienojamos laukus un noklikšķināt uz Ievietot. Ja vēlāk vēlaties noņemt lauku, kuru esat pievienojis iepriekš, atkārtojiet šo procesu, bet vienkārši notīriet lauku, kuru esat pievienojis iepriekš. 

Izvēlieties **pārvaldīt** pogas, lai redzētu iespēju sarakstu pārvaldība saistībā ar visiem personalizācijas pašreizējā lappusē. 

Izvēlieties **skaidri**, lai atiestatītu lapu uz tās noklusējuma uzstādītas valsts. Tiks dzēsti visi personalizācijas pašreizējā lapā. Nav atsaukt darbības, tātad tikai Izmantojiet šo opciju, ja esat pārliecināts, ka vēlaties atiestatīt jūsu lapā. 

Izvēlieties **Importēt**, lai izmantotu personalizāciju no personalizēšanas faila, kuru jūs vai kāds cits iepriekš izveidojis šai lapai. Importējot personalizāciju, tiks notīrītas jebkuras personalizācijas, ko esat veicis savā lapā un tā vietā tiks izmantotas visas personalizācijas no atlasītā faila. Ja vēlaties saglabāt vai koplietot personalizāciju, atlasīsiet opciju **Eksportēt**, lai saglabātu personalizācijas failā. 

Izvēlieties pogu **Aizvērt**, lai aizvērtu rīkjoslu un atgrieztu lapu iepriekšējā interaktīvā stāvoklī. 

Ar Personalizācijas rīkjoslu, saglabāšana notiek netieši. Jūsu personalizācijas stājas spēkā uzreiz pēc to veikšanas un nav nepieciešams noklikšķināt uz pogas **Saglabāt**. Dažos gadījumos jūs redzēsiet slēdzenes ikona blakus elementam, atlasot rīku. Tas nozīmē, ka pasūtījuma lapu, lai strādātu kā pareizi, nevar modificēt rekvizītus, kas saistīti ar atlasīto rīku. Atverot rīkjoslu Personalizēšana, lapa kļūst neinteraktīva. Tajā nevar ievadīt datus vai izvērst vai sakļaut sadaļas.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Tiešā personalizēšana: elementa vai saraksta pievienošana darbvietai
Dažās lapās ar sarakstiem darbību rūtī būs pieejams papildu personalizēšanas līdzeklis cilnes Opcijas grupā Personalizēt. Atlasiet **Pievienot darbvietai**, lai atvērtu nolaižamo sarakstu, kas sniedz iespēju parādīt informāciju pašreizējā sarakstā (filtrētu un kārtotu vai pēc noklusējuma) Darbvietā kā sarakstu vai kopsavilkuma elementu (ko var izmantot, lai rādītu krājumu skaitu sarakstā). 

[![Add to workspace](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Lai pievienotu sarakstu darbvietai, vispirms kārtojiet vai filtrējiet sarakstu ar tādu informāciju, kuru jūs vēlētos redzēt savā darbvietā, un pēc tam atzīmējiet dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Saraksts** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Saraksts**, atvērsies dialoglodziņš, kas ļauj izvēlēties kolonnas, kuras vēlaties redzēt sarakstā un saraksta etiķete, kā tā parādīsies darbvietā. 

Lai pievienotu elementu darbvietai, vispirms filtrējiet sarakstu, lai tajā būtu dati, kurus vēlaties apkopot (vai vēlaties tiem ātri piekļūt). Pēc tam atveriet nolaižamo dialoglodziņu Pievienot darbvietai. Pēc tam atlasiet vajadzīgo darbvietu un atlasiet **Elements** nolaižamajā sarakstā Prezentācija. Ja atlasāt **Elements**, tiks atvērts dialoglodziņš, ļaujot sniegt elementam etiķeti un izlemt, vai rūtī tiks parādīts skaits. Novietojot darbvietā, elements ļauj atvērt pašreizējo lapu no darbvietas, un rādīt informācijas sarakstu, kas saistīta ar šo elementu. 

Kad saraksts vai elements tiek pievienots darbvietai, varat atvērt šo darbvietu un atkārtoti sakārtot sarakstu vai elementu grupā, kurā tas ir novietots.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Tieša personalizēšana: kopsavilkuma pievienošana no darbvietas informācijas panelim
Dažas darbvietas iekļauj skaitu flīzes (flīzes ar skaitļiem, uz tiem), kas arī jūs vēlētos redzēt uz jūsu dashboard. Darbvietu, noklikšķiniet ar peles labo pogu skaitu flīzes un atlasiet **personalizēšana**. Atlasiet **Piespraust informācijas panelim**. Nākamreiz pārejot uz (un atsvaidzinot) atlasīto informācijas paneli, jūs redzēsiet šo skaitli zem šīs darbvietas navigācijas elementa informācijas panelī.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Tiešā personalizēšana: sava informācijas paneļa personalizēšana
Paneļa bieži ir pirmajā lapā, jūs redzēsiet, atverot Dynamics 365 operācijām. Informācijas paneli var personalizēt, lai pārdēvētu darbvietas navigācijas elementus, parādītu tikai elementus, ko vēlaties redzēt, pārdēvētu elementus vai sakārtotu elementus secībā, kādā vēlaties tos redzēt. Lai personalizētu informācijas paneli, atlasiet jebkuru elementu un noklikšķiniet ar peles labo pogu, lai atvērtu konteksta izvēlni. Konteksta izvēlnē atlasiet **Personalizēt**. Ja atlasītais elements ir tas, ko vēlaties paslēpt, vai pārdēvēt, vai izlaist, jūs varat veikt izmaiņas tieši parādītajā rekvizītu logā. Ja vēlaties sakārtot elementus, atlasiet **Personalizēt šo formu** rekvizītu logā, lai atvērtu rīkjoslu Personalizēšana. Pēc tam elementu izkārtošanai var izmantot Pārvietošanas rīku.

## <a name="administration-of-personalization"></a>Personalizēšanas administrēšana
Ir iespējams personalizēt lapu un koplietot to ar citiem lietotājiem, vienkārši eksportējot personalizētu lapu un lūdzot citus lietotājus naviģēt uz personalizētu lapu un importēt personalizēšanas failu, ko esat izveidojis. Ja lietotājam ir administratora tiesības, viņš var arī pārvaldīt citu lietotāju personalizācijas lapā **Personalizēšanas iestatījumi**. Pārvietojieties uz b lapu. Lapā **Personalizēšana** jūs atradīsiet divas cilnes — vienu ar nosaukumu **Sistēma** un vienu ar nosaukumu** Lietotāji**. 

**Sistēma:** te var īslaicīgi atspējot vai "izslēgt" visas personalizācijas sistēmā. Tas nedzēš personalizācijas, bet gan atiestata visas formas uz noklusēto stāvokli. Personalizācijas var vēlāk atkārtoti iespējot, lai visas personalizācijas atkārtoti lietotu katra lietotāja formām. Varat arī dzēst visas personalizācijas visiem lietotājiem. Ņemiet vērā, ka, dzēšot personalizācijas, nevar automātiski atkārtoti iespējot personalizācijas no sistēmas. Pārliecinieties, ka eksportējāt personalizācijas, ko vēlaties vēlāk importēt, pirms šīs darbības veikšanas. 

**Lietotāji:** te varat izlemt katram lietotājam, vai viņš var veikt netiešu vai tiešu personalizēšanu. Varat arī izlemt, vai katrs lietotājs drīkst veikt tiešu vai netiešu personalizēšanu konkrētā formā. Visbeidzot, varat importēt, vai eksportēt, vai dzēst personalizācijas katram lietotājam. 

**Piezīme:** sākotnējā laidienā personalizēšanas administrēšana nodrošina tikai katra lietotāja pārvaldību.


