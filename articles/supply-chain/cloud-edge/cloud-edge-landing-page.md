---
title: Mēroga vienības izdalītā hibrīda topoloģijā
description: Šajā tēmā ir sniegta informācija par mākoņa un malas mēroga vienībām ražošanas un noliktavas pārvaldības darba slodzēm.
author: Mirzaab
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5ec846b294cd9ca62ff15a5306e012813c77e306
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676356"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Mēroga vienības izdalītā hibrīda topoloģijā

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Mēroga vienības iespējas korporācijas Microsoft Dynamics 365 Supply Chain Management ir pieejamas saskaņā ar noteikumiem, kas nosaka pakalpojuma izmantošanu. Papildinformāciju skatiet šeit: [Microsoft Dynamics Juridiskā informācija](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Iespējojot mākoņa un malas mēroga vienības, jums tiks prasīts apstiprināt, ka jūs saprotat, ka daži dati, kas ir saistīti ar mākoņa un malas mēroga vienību konfigurāciju un apstrādi, var tikt glabāti datu centrā, kas atrodas Amerikas Savienotajās Valstīs. Lai iegūtu plašāku informāciju par mākoņa un malas skalas vienību datu apstrādi, skatiet tālāk šīs tēmas sadaļā [Datu apstrāde skalas vienību pārvaldības laikā](#data-processing-management).

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Galvenās vērtības priekšlikums izdalītajai hibrīda topoloģijai

Uzņēmumiem, kas strādā ar ražošanu un sadali, ir jābūt iespējai palaist galvenos biznesa procesus 24/7, bez pārtraukumiem un pēc mēroga. Izdalītā hibrīda topoloģija ļauj uzņēmumiem palaist galvenos/kritiskos ražošanas un noliktavu procesus bez traucējumiem pat, ja jāsaskaras ar īslaicīgām tīkla savienojuma vai latentuma problēmām.

Ar izdalītā hibrīda topoloģiju tiek ieviests *mēroga vienību* koncepts, kas ļauj veikala grīdas un noliktavas izpildes darba slodzes izdalīt dažādās vides. Šī funkcionalitāte var palīdzēt uzlabot veiktspēju, novērst pakalpojumu traucējumus un palielināt darbspējas laiku. Mēroga vienības tiek nodrošinātas ar šādām pievienojumprogrammām jūsu Supply Chain Management abonementam:

- Mākoņa mēroga vienības pievienojumprogramma programmai Dynamics 365 Supply Chain Management
- Malas mēroga vienības pievienojumprogramma programmai Dynamics 365 Supply Chain Management

Darba slodzes iespējas tiek pastāvīgi izlaistas, izmantojot inkrementālos uzlabojumus.

## <a name="scale-units-and-dedicated-workloads"></a>Mēroga vienības un specializētās darba slodzes

Mēroga vienības paplašina centrālo Supply Chain Management centrmezgla vidi, pievienojot īpašu apstrādes noslodzi. Mēroga vienības var palaist mākonī. Alternatīvi viņi var darboties uz [malas](cloud-edge-edge-scale-units-lbd.md), lokāli jūsu lokālajā telpā.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ar mēroga vienībām.":::

Mēroga vienības nodrošina piešķirtajām darba slodzēm noturību, uzticamību un mērogu. Malas skalas vienības var īslaicīgi atvienot no mākoņa centrmezgla vides, un darbinieki turpina strādāt ar piešķirtajām darba slodzes daļām.

Jēdziens *Darba slodze* ir noteikts biznesa funkcionalitātes kopums, ko var ņemt vērā un deleģēt mēroga vienībai. Lai gan noliktavas pārvaldības darba slodze ir izlaista, ražošanas izpildes darba slodze joprojām tiek priekšskatīta.

Varat konfigurēt centrmezgla vidi un mākoņveida skalas vienības atlasītajām darba slodzēm, izmantojot [Mēroga vienību pārvaldnieka portālu](https://sum.dynamics.com). Varat arī piešķirt vairākas darba slodzes uz vienu mēroga vienību. Papildinformāciju par pašreizējā laidienā mākoņa mēroga vienību priekšnosacījumiem un ierobežojumiem skatiet tālāk šīs tēmas sadaļā [Mākoņa skalas vienību priekšnosacījumi un ierobežojumi](#cloud-scale-unit-prerequisites).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Īpašas noliktavas vadības darba slodzes iespējas mēroga vienībās

Noliktavas pārvaldības darba noslodze ļauj noliktavas operācijām veikt mērogu un darbību elastīgā vidē, izmantojot izolētus uzturēšanas logus. Noliktavas pārvaldības darba noslodze atbalsta lielāko daļu uzņēmuma pārkraušanas centra noliktavas pārvaldības procesu. Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Īpašas ražošanas izpildes darba slodzes iespējas mēroga vienībās

Ražošanas darba slodze nodrošina šādas iespējas:

- Iekārtu operatori un ražotnes uzraudzības iestādes var piekļūt operāciju ražošanas plānam.
- Iekārtu operatori var uzturēt plāna atjaunināšanu, izpildot diskrētus un procesa ražošanas darbus.
- Ražotnes vadītājs var koriģēt darbības plānu.
- Darbinieki var piekļūt ierašanās un aiziešanas reģistrācijas laikam un apmeklējumam, lai nodrošinātu pareizu darbinieka algas aprēķinu.

Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Apsvērumi, pirms iespējojat sadalīto topoloģiju piegādes ķēžu pārvaldībai

Iespējojot izplatīto topoloģiju, jūs pāriet uz piegādes ķēdes pārvaldības mākoņa vidi, lai tā darbojas kā pārkraušanas mezgls. Varat arī saistīt papildu vides, kas mākonī vai malā ir konfigurētas kā mēroga vienības.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Mākoņskalas mērvienību priekšnosacījumi un ierobežojumi

Pašreizējā mēroga vienību izlaidumā dažas iespējas vēl nav pieejamas, bet tās var tikt pievienotas inkrementālām izlaidumiem laika gaitā.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Jums ir jābūt licencētam Supply Chain Management debitoram

Lai ieslēgtu sadalīto topoloģiju, jums Supply Chain Management licencei. Jūsu esošā mākoņa vide kļūs par centrmezglu jūsu hibrīdu topoloģijā. Varat norādīt gan smilškastes vides, gan ražošanas vides kā centrmezgla vides, kā arī varat pievienot mēroga vienības saskaņā ar jūsu iegādātajām pievienojumprogrammām.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Jūsu esošais projekts ir jāpārvalda, izmantojot LCS globālo komercversiju

Esošajam Microsoft Dynamics Lifecyle Services (LCS) projektam jāatbilst šādām versijas prasībām:

- Projekts ir jāpārvalda, izmantojot LCS globālo komercversiju vietnē [lcs.dynamics.com](https://lcs.dynamics.com).
- LCS lokālās versijas (piemēram, [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) un [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) netiek atbalstītas.
- Nav atbalstītas valsts LCS mākoņa versijas.
- LCS Mooncake versija netiek atbalstīta.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Jūsu pašreizējai ražošanas videi ir jābūt pašapkalpošanās tipam LCS

Jūsu pašreizējai ražošanas videi jābūt atzīmētam ar tipu **Pašapkalpošanās** pakalpojumā LCS. Šis tips norāda, ka jūsu LCS projekta nomnieks jau ir pārveidots tā, lai tas atbalsta Azure Service Fabric viesošanas modeli.

> [!IMPORTANT]
> Vides tipi, kas darbojas kā infrastruktūras pakalpojums (infrastructure as a service - IaaS), netiek atbalstīti. Šīs vides parasti tiek pievienotas veidam **Microsoft pārvaldītās** pakalpojumā LCS. Ja jums ir šī tipa vide, sazinieties ar Microsoft kontaktpersonu, lai izprastu migrācijas laika skalu uz **Pašapkalpošanās** tipu.

Korporācija Microsoft pārvieto visas Supply Chain Management mākoņa vides no IaaS modeļa uz topoloģiju, kas ir viesota Service Fabric. Šī pārvietošana uzlabo mērogojamību un atvieglo pakalpojumu pārvaldību. Tāpēc izvietošanas un uzturēšanas operācijas ir ātrākas. Tāpat pakalpojuma komponenti tiek migrēti uz mikropakošanas pakalpojumu koncepciju, un pakalpojuma viesošanas modelis [pāriet](/virtualization/windowscontainers/about/containers-vs-vm) no virtuālās mašīnas (VM) modeļa uz vieglu, izolētu arhitektūru.

Visbeidzot, viena un tā pati uz Service Fabric balstīta konteinerizēta pakalpojumu infrastruktūra nodrošinās gan mākoņa, gan malas pakalpojuma instances neatkarīgi no tā, vai instance ir centrmezgls mākonī vai mēroga vienība mākonī vai malā.

Pirms varat pāriet uz hibrīdu topoloģiju, kas atbalsta mēroga vienības, projekta nomniekam ir jāpāriet uz Service Fabric viesoto modeli. Turklāt ir jāpārkonvertē jebkura vide, kas darbosies kā centrmezgls.

> [!TIP]
> Lai saņemtu uzziņas par sava LCS projekta nomnieka statusu, skatiet vides tipu paklpojumā [LCS](https://lcs.dynamics.com/) vai sazinieties ar savu partneri vai Microsoft kontaktpersonu.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Vietējo biznesa datu (lokālās) vides netiek atbalstītas kā mēroga vienību centrmezgli

Lokālās vides nevar darboties kā mēroga vienību centrmezgli. Centrmezgla vidēm vienmēr jābūt mākoņa viesotām.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Apjoma vienību pārvaldības iespējas ir ierobežotas

Pārvaldības iespējas, kas var palīdzēt ar darba slodzi, ir ierobežotas. Dažas pārvaldības operācijas netiek atbalstītas pašapkalpošanās veidā, un, iespējams, jums ir jāpieprasa atbalsts jūsu partnerim vai Microsoft kontaktpersonai. Kā piemēru var minēt dažas darba slodzes kustības starp mēroga vienībām un pagaidu ad hoc kustības katastrofu scenārijos.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Rādītāji un mērījumi vēl nav pieejami

Rādītāji un mērvienības, kas var palīdzēt atlasīt labāko programmu mēroga vienībām, vēl nav pieejami. Strādājiet ar Microsoft kontaktpersonu vai ieviešanas partneri, lai izvēlētos izdevīgāko programmu.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Datu apstrāde mēroga vienību pārvaldības laikā

Iespējojot Dynamics 365 vidi, lai atbalstītu dalīto topoloģiju mākoņa un malas skalas vienībām, daži pārvaldības pakalpojumi tiks viesoti tikai Amerikas Savienotajās Valstīs līdzīgi kā LCS. Šī darbība ietekmē atsevišķas administratīvās un konfigurācijas informācijas pārsūtīšanu un uzglabāšanu, ko izmanto [Mēroga vienību pārvaldnieka portāls](https://sum.dynamics.com). Daži piemēri:

- Jūsu nomnieka nosaukumi un ID
- Jūsu LCS projekta ID
- Administratora un projekta īpašnieka e-pasta adreses, kas tiek izmantotas pierakstīšanās laikā
- Vides ID centrmezglam un mēroga vienībām
- Darba slodzes konfigurācijas, tostarp juridisko personu un iestāžu nosaukumi un fiziskās adreses, lai topoloģiju varētu rādīt ģeogrāfiskā kartē
- Apkopotie rādītāji (piemēram, latentuma un caurlaides dati), kas tiks rādīti kartes analīzes lapā, lai palīdzētu jums izvēlēties vispiemērotāko mērogu vienību lietojumu

Dati, kas tiek pārsūtīti un glabāti ASV datu centros, tiks dzēsti saskaņā ar Microsoft datu glabāšanas politikām. Jūsu konfidencialitāte ir svarīga korporācijai Microsoft. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Piegādes ķēžu pārvaldības sadalītā topoloģija

### <a name="try-out-the-distributed-hybrid-topology"></a>Mēģiniet veikt izplatīto topoloģiju

Notiek process, kad notiek izvietošana sadalītajā topoloģijā, ir divi posmi. Pirmā posma laikā jums ir pamēģiniet [risinājumu](cloud-edge-try-out.md) un validējiet pielāgojumus, lai pārliecinātos, ka tie darbojas sadalītā topoloģijā, kas ietver apjoma vienības. (Lai validāciju izdarītu, varat lietot esošās izstrādes vides.) Pēc tam varat turpināt ar otro pakāpi, kur iegūstat ražošanas vides.

## <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Atlasiet savu LCS projekta nomnieku un detalizētu pievienošanas procesu

Mēroga vienības tiek piedāvātas vairākās noliktavas vienībās (NV) un cenu noteikšanas opcijās. Tāpēc varat izvēlēties opciju, kas vislabāk atbilst jūsu plānotā mēneša transakciju apjomam un veiktspējas prasībām.

> [!TIP]
> Lai identificētu izmērus, kas vislabāk atbilst jūsu vajadzībām, sazinieties ar ieviešanas partneri un Microsoft, lai saprastu ikmēneša darbības lielumu, kas nepieciešams.

Ievades līmeņa SKU ir pazīstama kā *Pamata* un vēl spēcīgāka SKU ir pazīstama kā *Standarta*. Katra SKU ir iepriekš ielādēta ar noteiktu mēneša transakciju skaitu. Tomēr ikmēneša transakciju budžetu var palielināt, katram SKU pievienojot pārsnieguma pievienojumprogrammas.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Pievienojumprogrammas mākoņa mēroga vienībām.":::

> [!NOTE]
> Mēroga vienību pievienojumprogrammas nav savienotas ar ierobežotu lietotāju skaitu. Tie ir pieejami jebkuriem lietotājiem jūsu esošajā abonementā (ja jūsu administrators ir piešķīris lietotājiem nepieciešamās lomas).

Katras mēroga vienības pievienojumprogrammas pirkšana ne tikai dod mēneša transakciju apjomu, bet arī sniedz jums īpašu vides slotu skaitu LCS. Katrai mākoņa skalas vienības pievienojumprogrammai ir tiesības izmantot vienu jaunu ražošanas slotu un vienu jaunu smilškastes slotu. Pievienošanas procesa laikā tiks pievienots jauns LCS projekts, kam ir šie sloti. Slotu lietošanas tiesības ir piesaistītas tā, lai sloti tiktu izmantoti kā mēroga vienības, kam ir mākoņa centrmezgls.

Pārtēriņa pievienojumprogrammas nedod jums tiesības izmantot jaunas vides slotus.

Ja vēlaties iegūt vairāk smilškastes vides, varat iegādāties papildu parastos smilškastes slotus. Pēc tam korporācija Microsoft var palīdzēt iespējot šos slotus kā smilškastes skalas vienības hibrīdu topoloģijai.


Kad esat beidzis plānošanu, kā dosties uz sadalīto topoloģiju piegādes ķēžu pārvaldībai, jūs izmantosiet Mēroga vienības pārvaldnieka portālu, [lai](https://aka.ms/SCMSUM) sāktu pārdošanas procesu. Portālā atlasiet cilni **Dynamics 365 nomnieki**. Šī cilne parāda to nomnieku sarakstu, kuros ir iekļauts jūsu konts un kuros esat LCS projekta īpašnieks vai vides administrators.

Ja jūsu meklētais nomnieks nav sarakstā, dodieties uz [LCS](https://lcs.dynamics.com/v2) un pārliecinieties, ka jūs esat vai nu vides administrators, vai arī LCS projekta īpašnieks šim nomniekam. Tikai Azure Active Directory (Azure AD) atlasītā nomnieka konts ir autorizēts pabeigt reģistrēšanu.

> [!NOTE]
> Pēc izmaiņu veikšanas pakalpojumā LCS var paiet līdz 30 minūtēm līdz nomnieku saraksts atspoguļo izmaiņas.

Katram nomniekam saraksts parāda pievienošanas statusu.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Nomnieku saraksts Dynamics 365 nomnieku cilnē.":::

Atlasiet **Noklikšķiniet šeit, lai sāktu darbu**, lai pieprasītu LCS nomnieka pievienošanu. Jums ir jāpiekrīt noteikumiem. Jums ir arī jāsniedz uzņēmuma e-pasta adrese, kur Microsoft var nosūtīt paziņojumus, kas saistīti ar pievienošanas procesu.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Reģistrēšanās iesniegums nomniekam.":::

Korporācija Microsoft pārskatīs jūsu pieprasījumu un sniegs informāciju par nākamajām darbībam, sūtot e-pastu uz adresi, kuru sniedzat reģistrēšanās veidlapā. Korporācija Microsoft cieši sadarbojas ar jums, lai aktivizētu mēroga vienības jūsu biznesa scenārijā hibrīdu topoloģijā.

Kad pievienošana ir pabeigta, varat izmantot portu, lai konfigurētu mēroga vienības un darba slodzes.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a> Pārvaldīt mēroga vienības un darba slodzi, izmantojot portālu Mērvienību vadītājs

Dodieties uz [portālu Skale Unit Manager](https://aka.ms/SCMSUM) un piesakieties, izmantojot savu nomnieka kontu. Lapā **Konfigurēt mēroga vienības** varat pievienot centrmezgla vidi, ja tā jau nav norādīta sarakstā. Pēc tam varat atlasīt centrmezglu, ko vēlaties konfigurēt ar mēroga vienībām un darba slodzēm.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Mēroga vienību pārvaldnieka portāls, Konfigurējiet mēroga vienību lapu.":::

Lai pievienotu vienu vai vairākas mēroga vienības, kas ir pieejamas jūsu abonementos, atlasiet **Pievienot mēroga vienības**.

Lai pievienotu noliktavas pārvaldības darba slodzi kādai no jūsu mēroga vienībām, cilnē **Definētās darba slodzes** izmantojiet pogu **Izveidot darba slodzi**. Katrai darba slodzei jānorāda to procesu konteksts, kas piederēs šai darba slodzei. Noliktavas pārvaldības darba slodzei konteksts ir noteikta noliktava noteiktā vietā un juridiskajā personā.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Definējiet darba noslodzes dialogu.":::

#### <a name="manage-workloads"></a><a name="manage-workloads"></a> Pārvaldīt darba slodzi

Kad ir iespējota viena vai vairākas darba noslodzes, izmantojiet opciju Pārvaldīt darba slodzi, **lai sāktu un pārvaldītu procesus, piemēram, tos**, kas ir uzskaitīti šajā tabulā.

| Apstrādāšana | Apraksts |
|---|---|
| Pauzēt mēroga vienības sakarus | Pauzēt konveijera ziņojumus starp pārkraušanas vietu un mēroga vienību. Šis process apturēs sakarus un pāries datu konveijeru starp pārkraušanas punktu un mēroga vienībām. Šis process ir jāpalaiž pirms piegādes ķēdes pārvaldības apkalpošanas operācijas palaišanas pārkraušanas centrā vai mēroga vienībā, bet jūs to varat izmantot arī citās situācijās. |
| CV apjoma vienības sakarus | Atsākt konveijera ziņojumus starp pārkraušanas vietu un mēroga vienību. Iespējams, ka jums būs jāizmanto šis process, piemēram, pēc piegādes ķēžu apkalpošanas operācijas palaišanas pārkraušanas centrā vai mēroga vienībā. |
| Jaunināt darba noslodzes | Sinhronizēt jaunu funkcionalitāti starp pārkraušanas centra un mēroga vienības darba slodzēm. Iespējams, ka jums būs jāizmanto šis process, piemēram, kad apkalpošana ir radījusi datu apmaiņas vaicājumu maiņu un/vai ir pievienojusi jaunas tabulas vai laukus darba noslodzei. |
| Pārsūtīt darba slodzi uz apjoma vienību | Plānojiet darba noslodzi, kas pašreiz darbojas pārkraušanas punktu, kas jāpārvieto uz mēroga vienību. Kad šis process ir palaists, datu sinhronizācija notiks, un gan pārkraušanas punktu, gan mēroga vienību tiks iestatīta mainīt darba noslodzes īpašumtiesības. |
| Pārsūtīt mēroga vienību uz pārkraušanas centru | Plānojiet darba noslodzi, kas pašreiz darbojas mēroga vienībā, lai to pārceltu uz pārkraušanas punktu. Kad šis process ir palaists, datu sinhronizācija notiks, un gan pārkraušanas punktu, gan mēroga vienību tiks iestatīta mainīt darba noslodzes īpašumtiesības.
| Ārkārtas pāreja uz pārkraušanas mezglu | <p>Nekavējoties pārsūtiet esošo darba noslodzi uz pārkraušanas centru. *Šis process mainīs īpašumtiesības tikai datiem, kas pašlaik ir pieejami pārkraušanas centrā.*</p><p><strong>Brīdinājums.</strong> Šis process var izraisīt datu zudumu nesinhronizētiem datiem un biznesa apstrādes kļūmi. Tāpēc tā ir jāizmanto tikai noslogotos gadījumos, kur biznesa procesi ir jāapstrādā pārkraušanas punktu, jo mēroga vienībai ir pārtraukums, ko pieņemamā laikā nevar samazināt.</p> |
| Ideoloģija - izplatītā topoloģija | Noņemiet mēroga vienības izvietojumu un palaidiet tikai pārkraušanas centrā bez darba noslodzes apstrādes. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Mēroga vienības un darba slodzes pārvaldības pieredze.":::

> [!TIP]
> Laika gaitā inkrementāli uzlabojumi tiks pievienoti Mēroga vienību pārvaldnieka pieredzei, lai atvieglotu dzīves cikla pārvaldības operācijas. Pašreizējās versijas specifiskās iespējas tiek dokumentētas izvietošanas rokasgrāmatā, kas ir pieejama klientiem, kuri ir piegādes ķēdes pārvaldības sadalītās topoloģijas procesā. <!-- KFM: Add a link to the handbook when it is published -->

## <a name="feature-management-considerations-for-workloads"></a>Līdzekļu pārvaldības apsvērumi attiecībā uz darba slodzēm

Šajā sadaļā skaidroti daži svarīgi aspektiem, kas ir jāņem vērā, kad instalējat darba slodzi, pievienojiet līdzekļus vai noņemiet funkcijas sadalītās topoloģijas izvietošanā. Vairāki scenāriji var ietekmēt to, vai pēc izmaiņu [veikšanas](#manage-workloads) būs jāveic darba noslodzes jaunināšana. Tomēr tas parasti nepieciešams, atjauninot vai pievienojot jaunus datu apmaiņas vaicājumus un/vai kad pievienojat jaunas tabulas vai laukus iepriekš instalētajām darba noslodzei.

### <a name="mandatory-features-for-installing-a-workload"></a>Obligātie līdzekļi darba slodzes instalēšanai

Kad instalējat darba slodzi, instalēšanas process izveido darba noslodzes definīciju, kas satur informāciju par datu tabulām, ko izmanto, kad dati tiek sinhronizēti starp divām izvietošanām. Darba noslodzes definīcijas izveide tiek automātiski apstrādāta, pamatojoties uz funkcijām, kas pašlaik ir iespējotas līdzekļu [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Šajā tabulā ir uzskaitīti līdzekļi, kas ir jāiespējo, lai ģenerētu darba noslodzes definīcijas, kas nepieciešamas noliktavas vai ražošanas darba noslodzes palaišanai.

| Obligāta funkcija | Darba slodze |
|---|---|
| Automātiska GUID piešķiršana WHS lietotāja izveidei | Noliktava |
| Organizācijas mēroga darba aizturēšana | Noliktava |
| Sūtījuma kopuma etiķetes detalizētā informācija | Noliktava |
| Mērogotās vienības atbalsts noliktavas programmas darbu sarakstiem | Noliktava |
| Ražošanas izpilde | Ražošana |

Kad izvietojat darba slodzi [, izmantojot mēroga vienību izvietošanas rīkus vienas kastes izstrādes vidēm vai mēroga vienību pārvaldnieka portālam, visas obligātās funkcijas tiks automātiski aktivizētas](https://github.com/microsoft/SCMScaleUnitDevTools)[...](https://sum.dynamics.com). Tomēr, ja veiksiet manuālu testa izvietošanu, kam trūkst viena vai vairākas obligātas funkcijas, darba slodzes instalēšana neizdosies, un jūs saņemsit ziņojumu, kurā būs uzskaitīti trūkstošie līdzekļi. Pēc tam šie līdzekļi ir manuāli jāiespējo un atkārtoti jāaktivizē darba noslodzes instalēšana.

### <a name="enabling-or-disabling-features-that-have-data-synchronization-dependencies"></a>Iespējo vai deaktivizē funkcijas, kurām ir datu sinhronizācijas atkarības

Līdzekļi, kas ietekmē sinhronizēto datu atlasi starp pārkraušanas vietu un tā mēroga vienībām, ietekmē arī to, kā tiek izveidota darba noslodzes definīcija. Tāpēc ir svarīgi, lai šie līdzekļi tiktu iespējoti pirms darba slodzes instalēšanas. Ja iespējosiet šī tipa līdzekli slodzes lietošanas laikā, jums ir jāģenerē darba noslodzes definīcija, [palaižot darba noslodzes jaunināšanu](#manage-workloads) pēc funkcijas iespējošanas. Tāpat arī, ja atspējosit funkciju, kam ir datu sinhronizācijas atkarības darba slodzes izpildes laikā, ir jāpalaiž darba noslodzes jaunināšana, [lai](#manage-workloads) noņemtu atbilstošo datu sinhronizācijas informāciju no darba noslodzes definīcijas.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
