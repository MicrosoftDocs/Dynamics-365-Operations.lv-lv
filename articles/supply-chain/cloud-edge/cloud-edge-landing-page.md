---
title: Izmantojiet apjoma vienības, lai palīdzētu palielināt Supply Chain Management darba slodzi
description: Šajā tēmā ir sniegta informācija par mākoņa un malas mēroga vienībām ražošanas un noliktavas pārvaldības darba slodzēm.
author: cabeln
ms.date: 04/13/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c47088edd89413d196e904bc7eaa115585bf8464
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899147"
---
# <a name="use-scale-units-to-help-increase-resilience-for-supply-chain-management-workloads"></a>Izmantojiet apjoma vienības, lai palīdzētu palielināt Supply Chain Management darba slodzi

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Mēroga vienības iespējas korporācijas Microsoft Dynamics 365 Supply Chain Management ir pieejamas saskaņā ar noteikumiem, kas nosaka pakalpojuma izmantošanu. Papildinformāciju skatiet šeit: [Microsoft Dynamics Juridiskā informācija](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Iespējojot mākoņa un malas mēroga vienības, jūs apstiprināt, ka jūs saprotat, ka daži dati, kas ir saistīti ar mākoņa un malas mēroga vienību konfigurāciju un apstrādi, var tikt glabāti datu centrā, kas atrodas Amerikas Savienotajās Valstīs. Lai iegūtu plašāku informāciju par mākoņa un malas skalas vienību datu apstrādi, skatiet tālāk šīs tēmas sadaļā [Datu apstrāde skalas vienību pārvaldības laikā](#data-processing-management).

## <a name="core-value-proposition-for-scale-units"></a>Kodola vērtības piedāvājums mēroga vienībām

Uzņēmumiem, kas strādā ar ražošanu un sadali, ir jābūt iespējai palaist galvenos biznesa procesus 24/7, bez pārtraukumiem un pēc mēroga. Mākoņa un malas mēroga vienības ļauj uzņēmumiem darbināt galvenos nepieciešamos ražošanas un noliktavas procesus bez pārtraukumiem, pat tad, ja reizēm rodas tīkla savienojamības vai latentuma problēmas.

Mākoņa un malas mēroga vienības iespējo ražotnes un noliktavu izpildes darba slodžu sadalījumu starp dažādām vidēm. Šī funkcionalitāte var palīdzēt uzlabot veiktspēju, novērst pakalpojumu traucējumus un palielināt darbspējas laiku. Mēroga vienības tiek nodrošinātas ar šādām pievienojumprogrammām jūsu Supply Chain Management abonementam:

- Mākoņa mēroga vienības pievienojumprogramma pakalpojumam Dynamics 365 Supply Chain Management (*pieejama 2021. gada aprīlī*)
- Malas mēroga vienības pievienojumprogramma pakalpojumam Dynamics 365 Supply Chain Management (*drīz pieejama*)

Darba slodzes iespējas tiek pastāvīgi izlaistas, izmantojot inkrementālos uzlabojumus.

## <a name="scale-units-and-dedicated-workloads"></a>Mēroga vienības un specializētās darba slodzes

Mēroga vienības paplašina centrālo Supply Chain Management centrmezgla vidi, pievienojot īpašu apstrādes noslodzi. Mēroga vienības var palaist mākonī. Vai arī tās var tikt palaistas uz malas uz vietas jūsu vietējā iestādē.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ar mēroga vienībām":::

Mēroga vienības nodrošina piešķirtajām darba slodzēm noturību, uzticamību un mērogu. Malas skalas vienības var īslaicīgi atvienot no mākoņa centrmezgla vides, un darbinieki turpina strādāt ar piešķirtajām darba slodzes daļām.

Jēdziens *Darba slodze* ir noteikts biznesa funkcionalitātes kopums, ko var ņemt vērā un deleģēt mēroga vienībai. Lai gan noliktavas pārvaldības darba slodze ir izlaista, ražošanas izpildes darba slodze joprojām tiek priekšskatīta.

Varat konfigurēt centrmezgla vidi un mākoņveida skalas vienības atlasītajām darba slodzēm, izmantojot [Mēroga vienību pārvaldnieka portālu](https://sum.dynamics.com). Varat arī piešķirt vairākas darba slodzes uz vienu mēroga vienību. Papildinformāciju par pašreizējā laidienā mākoņa mēroga vienību priekšnosacījumiem un ierobežojumiem skatiet tālāk šīs tēmas sadaļā [Mākoņa skalas vienību priekšnosacījumi un ierobežojumi](#cloud-scale-unit-prerequisites).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Īpašas noliktavas vadības darba slodzes iespējas mēroga vienībās

Noliktavas pārvaldības darba slodze ir pirmā sadalītā darba slodze mēroga vienībām, kas ir nodotas izpildei vispārējai pieejamībai.

Noliktavas pārvaldībai mēroga vienības nodrošina šādas iespējas:

- Sistēma var apstrādāt atlasītās kopuma metodes pārdošanas pasūtījumiem un pieprasījuma papildināšanai.
- Noliktavas darbinieki var palaist pārdošanas un pieprasījuma papildināšanas noliktavas darbu, izmantojot Warehouse Management mobile programmu.
- Noliktavas darbinieki var uzzināt par rīcībā esošajiem krājumiem, izmantojot Warehouse Management mobile programmu.
- Noliktavas darbinieki var izveidot un palaist krājumu kustības, izmantojot Warehouse Management mobile programmu.
- Noliktavas darbinieki var reģistrēt pirkšanas pasūtījumus un veikt atlikšanu, izmantojot Warehouse Management mobile programmu.

Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Īpašas ražošanas izpildes darba slodzes iespējas mēroga vienībās

Ražošanas darba slodzes pirmais izlaidums pašlaik ir priekšskatījumā un nodrošina šādas iespējas:

- Iekārtu operatori un ražotnes uzraudzības iestādes var piekļūt operāciju ražošanas plānam.
- Iekārtu operatori var uzturēt plāna atjaunināšanu, izpildot diskrētus un procesa ražošanas darbus.
- Ražotnes vadītājs var koriģēt darbības plānu.
- Darbinieki var piekļūt ierašanās un aiziešanas reģistrācijas laikam un apmeklējumam, lai nodrošinātu pareizu darbinieka algas aprēķinu.

Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Apsvērumi pirms sadalītās, hibrīdu topoloģijas iespējošanas pakalpojumam Supply Chain Management

Iespējojot sadalīto hibrīdu topoloģiju, jūs pārslēdzat savu Supply Chain Management mākoņa vidi tā, lai tā darbotos kā centrmezgls. Varat arī saistīt papildu vides, kas mākonī vai malā ir konfigurētas kā mēroga vienības.

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

Korporācija Microsoft pārvieto visas Supply Chain Management mākoņa vides no IaaS modeļa uz topoloģiju, kas ir viesota Service Fabric. Šī pārvietošana uzlabo mērogojamību un atvieglo pakalpojumu pārvaldību. Tāpēc izvietošanas un uzturēšanas operācijas ir ātrākas. Tāpat pakalpojuma komponenti tiek migrēti uz mikropakošanas pakalpojumu koncepciju, un pakalpojuma viesošanas modelis [pāriet](https://docs.microsoft.com/virtualization/windowscontainers/about/containers-vs-vm) no virtuālās mašīnas (VM) modeļa uz vieglu, izolētu arhitektūru.

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

Iespējojot Dynamics 365 vidi, lai atbalstītu sadali, hibrīdu topoloģiju mākoņa un malas skalas vienībām, daži pārvaldības pakalpojumi tiek viesoti tikai Amerikas Savienotajās Valstīs līdzīgi kā LCS. Šī darbība ietekmē atsevišķas administratīvās un konfigurācijas informācijas pārsūtīšanu un uzglabāšanu, ko izmanto [Mēroga vienību pārvaldnieka portāls](https://sum.dynamics.com). Daži piemēri:

- Jūsu nomnieka nosaukumi un ID
- Jūsu LCS projekta ID
- Administratora un projekta īpašnieka e-pasta adreses, kas tiek izmantotas pierakstīšanās laikā
- Vides ID centrmezglam un mēroga vienībām
- Darba slodzes konfigurācijas, tostarp juridisko personu un iestāžu nosaukumi un fiziskās adreses, lai topoloģiju varētu rādīt ģeogrāfiskā kartē
- Apkopotie rādītāji (piemēram, latentuma un caurlaides dati), kas tiks rādīti kartes analīzes lapā, lai palīdzētu jums izvēlēties vispiemērotāko mērogu vienību lietojumu

Dati, kas tiek pārsūtīti un glabāti ASV datu centros, tiks dzēsti saskaņā ar Microsoft datu glabāšanas politikām. Jūsu konfidencialitāte ir svarīga korporācijai Microsoft. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboarding-in-two-stages"></a>Pievienošana divos posmos

Pievienošanas procesam sadalītajai, hibrīdu topoloģijai ir divi posmi. Pirmā posma laikā jums ir jāapstiprina pielāgojumi, lai nodrošinātu, ka tie darbojas sadalītā topoloģijā, kam ir mēroga vienības. Smilškastēs un ražošanas vidēs tiek pārvietotas tikai otrā posmā.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>1. posms: Novērtējiet pielāgojumus vienas kastes izstrādes vidē

Pirms sākat smilškastes vai ražošanas vides pievienošanu, ieteicams izstrādes iestatījumos pārlūkot mēroga vienības, piemēram, vienas kastes vidē (ko sauc arī par 1. pakāpes vidi), lai varētu validēt procesus, pielāgojumus un risinājumus. Šā posma laikā dati un pielāgojumi tiks pielietoti vienas kastes vidēm. Viena vide ieņem centrmezgla lomu, otra ieņem mēroga vienības lomu. Šis iestatījums nodrošina labāko veidu, kā identificēt un risināt problēmas. Jaunāko pirmstermiņa piekļuves (PEAP) būvējumu var izmantot arī, lai pabeigtu šo posmu.

1. posmā jālieto [mēroga vienību izvietošanas rīki vienas kastes izstrādes vidēm](https://github.com/microsoft/SCMScaleUnitDevTools). Šie rīki ļauj konfigurēt centrmezgla un mēroga vienības vienā vai divās atsevišķās vienas kastes vidēs. Rīki GitHub ir pieejami kā binārais laidiens un avota kods. Izpētiet projektu Wiki, kas ietver [Pakāpeniskas lietošanas rokasgrāmata](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), kurā aprakstīts, kā rīki tiek lietoti.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>2. posms: pievienojumprogrammu ieguve un izvietošana jūsu smilškastes un ražošanas vidēs

Lai vienu no jūsu smilškastes vai ražošanas vidēm varētu pievienot jaunajai topoloģijai, ir jāiegūst pievienojumprogrammas vienai vai vairākām mākoņa mēroga vienībām (un nākotnē malas mēroga vienībām). Pievienojumprogrammas piešķirs atbilstošus projekta un vides slotus pakalpojumā [LCS](https://lcs.dynamics.com/), lai varētu izvietot mēroga vienības vides.

> [!NOTE]
> Mēroga vienību pievienojumprogrammas nav savienotas ar ierobežotu lietotāju skaitu, bet tās var izmantot jebkurš lietotājs esošajā abonementā, balstoties uz administratora piešķirtajām lomām.

Mēroga vienības tiek piedāvātas vairākās noliktavas vienībās (NV) un cenu noteikšanas opcijās. Tāpēc varat izvēlēties opciju, kas vislabāk atbilst jūsu plānotā mēneša transakciju apjomam un veiktspējas prasībām.

Ievades līmeņa SKU ir pazīstama kā *Pamata* un vēl spēcīgāka SKU ir pazīstama kā *Standarta*. Katra SKU ir iepriekš ielādēta ar noteiktu mēneša transakciju skaitu. Tomēr ikmēneša transakciju budžetu var palielināt, katram SKU pievienojot pārsnieguma pievienojumprogrammas.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Pievienojumprogrammas mākoņa mēroga vienībām":::

> [!TIP]
> Lai identificētu izmērus, kas vislabāk atbilst jūsu vajadzībām, sazinieties ar partneri un Microsoft, lai izprastu nepieciešamo mēneša transakciju lielumu.

Katras mēroga vienības pievienojumprogrammas pirkšana ne tikai dod mēneša transakciju apjomu, bet arī sniedz jums īpašu vides slotu skaitu LCS. Katrai mākoņa skalas vienības pievienojumprogrammai ir tiesības izmantot vienu jaunu ražošanas slotu un vienu jaunu smilškastes slotu. Pievienošanas procesa laikā tiks pievienots jauns LCS projekts, kam ir šie sloti. Slotu lietošanas tiesības ir piesaistītas tā, lai sloti tiktu izmantoti kā mēroga vienības, kam ir mākoņa centrmezgls.

Pārtēriņa pievienojumprogrammas nedod jums tiesības izmantot jaunas vides slotus.

Ja vēlaties iegūt vairāk smilškastes vides, varat iegādāties papildu parastos smilškastes slotus. Pēc tam korporācija Microsoft var palīdzēt iespējot šos slotus kā smilškastes skalas vienības hibrīdu topoloģijai.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Ieslēgt sadalīto hibrīdu topoloģiju pakalpojumam Supply Chain Management

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Atlasiet savu LCS projekta nomnieku un detalizētu pievienošanas procesu

Pēc tam, kad esat pabeidzis plānot, kā jūs pievienosiet sadalīto hibrīdu topoloģiju pakalpojumam Supply Chain Management, jūs izmantosiet [Mēroga vienības pārvaldnieka portāls](https://aka.ms/SCMSUM), lai sāktu pievienošanas procesu. Portālā atlasiet cilni **Dynamics 365 nomnieki**. Šī cilne parāda to nomnieku sarakstu, kuros ir iekļauts jūsu konts un kuros esat LCS projekta īpašnieks vai vides administrators.

Ja jūsu meklētais nomnieks nav sarakstā, dodieties uz [LCS](https://lcs.dynamics.com/v2) un pārliecinieties, ka jūs esat vai nu vides administrators, vai arī LCS projekta īpašnieks šim nomniekam. Tikai Azure Active Directory (Azure AD) atlasītā nomnieka konts ir autorizēts pabeigt reģistrēšanu.

> [!NOTE]
> Pēc izmaiņu veikšanas pakalpojumā LCS var paiet līdz 30 minūtēm līdz nomnieku saraksts atspoguļo izmaiņas.

Katram nomniekam saraksts parāda pievienošanas statusu.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Nomnieku saraksts Dynamics 365 nomnieku cilnē":::

Atlasiet **Noklikšķiniet šeit, lai sāktu darbu**, lai pieprasītu LCS nomnieka pievienošanu. Jums ir jāpiekrīt noteikumiem. Jums ir arī jāsniedz uzņēmuma e-pasta adrese, kur Microsoft var nosūtīt paziņojumus, kas saistīti ar pievienošanas procesu.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Reģistrēšanās iesniegums nomniekam":::

Korporācija Microsoft pārskatīs jūsu pieprasījumu un sniegs informāciju par nākamajām darbībam, sūtot e-pastu uz adresi, kuru sniedzat reģistrēšanās veidlapā. Korporācija Microsoft cieši sadarbojas ar jums, lai aktivizētu mēroga vienības jūsu biznesa scenārijā hibrīdu topoloģijā.

Kad pievienošana ir pabeigta, varat izmantot portu, lai konfigurētu mēroga vienības un darba slodzes.

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Pārvaldīt mākoņa mēroga vienības un darba slodzes, izmantojot portālu Skale Unit Manager

Dodieties uz [portālu Skale Unit Manager](https://aka.ms/SCMSUM) un piesakieties, izmantojot savu nomnieka kontu. Lapā **Konfigurēt mēroga vienības** varat pievienot centrmezgla vidi, ja tā jau nav norādīta sarakstā. Pēc tam varat atlasīt centrmezglu, ko vēlaties konfigurēt ar mēroga vienībām un darba slodzēm.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Mēroga vienības un darba slodzes pārvaldības pieredze":::

Lai pievienotu vienu vai vairākas mēroga vienības, kas ir pieejamas jūsu abonementos, atlasiet **Pievienot mēroga vienības**.

Lai pievienotu noliktavas pārvaldības darba slodzi kādai no jūsu mēroga vienībām, cilnē **Definētās darba slodzes** izmantojiet pogu **Izveidot darba slodzi**. Katrai darba slodzei jānorāda to procesu konteksts, kas piederēs šai darba slodzei. Noliktavas pārvaldības darba slodzei konteksts ir noteikta noliktava noteiktā vietā un juridiskajā personā.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Darba slodzes izveide":::

> [!TIP]
> Laika gaitā inkrementāli uzlabojumi tiks pievienoti Mēroga vienību pārvaldnieka pieredzei, lai atvieglotu dzīves cikla pārvaldības operācijas. Pašreizējās versijas specifiskās iespējas ir dokumentētas pievienošanas rokasgrāmatā, kas ir pieejama klientiem, kuri ir pievienošanas procesā sadalītajai hibrīdu tipiloģijai pakalpojumam Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
