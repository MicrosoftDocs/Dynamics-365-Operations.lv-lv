---
title: Mākoņa un malas mēroga vienības ražošanas un noliktavu pārvaldības darba slodzēm
description: Šajā tēmā ir sniegta informācija par mākoņa un malas mēroga vienībām ražošanas un noliktavas pārvaldības darba slodzēm.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3a23ee452535423684c6d210a448ee768379fa08
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516832"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Mākoņa un malas mēroga vienības ražošanas un noliktavu pārvaldības darba slodzēm

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mākoņa un malas mēroga vienības iespējo ražotnes un noliktavu izpildes darba slodžu sadalījumu starp dažādām vidēm. Šī funkcionalitāte var palīdzēt uzlabot veiktspēju, novērst pakalpojumu traucējumus un palielināt darbspējas laiku. To nodrošina šādas pievienojumprogrammas:

- Mākoņa mēroga vienības pievienojumprogramma programmai Dynamics 365 Supply Chain Management
- Malas mēroga vienības pievienojumprogramma programmai Dynamics 365 Supply Chain Management

Uzņēmumiem, kas strādā ar ražošanu un sadali, ir jābūt iespējai palaist galvenos biznesa procesus 24/7, bez pārtraukumiem un pēc mēroga. Mākoņa un malas mēroga vienības ļauj uzņēmumiem darbināt galvenos nepieciešamos ražošanas un noliktavas procesus bez pārtraukumiem, pat tad, ja reizēm rodas tīkla savienojamības vai latentuma problēmas.

## <a name="public-preview-information"></a>Publiskā priekšskatījuma informācija

Priekšskatījums nodrošina vienu vidi, kas darbojas kā jūsu Dynamics 365 Supply Chain Management vides mākoņveida centrmezgls un vienu vidi, kas darbojas kā mākoņa mēroga vienība.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Priekšskatījuma pieejamība

Mākoņa un malas mēroga vienību priekšskatījums kļūst pieejams esošajiem Supply Chain Management klientiem 2020. gada oktobrī.

Lai piekļūtu oktobra priekšskatījuma izlaidumam 10.0.15/Platformas atjauninājums 39, kas paredzēts izvietošanai jūsu [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) vidē, jums jābūt daļai no priekšskatījuma agrās piekļuves programmas (ko sauc arī par PEAP) risinājumam Supply Chain Management. Varat pievienoties PEAP, ja jau esat dalībnieks plašākajā [Dynamics Insider Program](https://experience.dynamics.com/insider). Vienkārši atlasiet konkrēto programmu ar nosaukumu "Finance & Operations: Preview Early Access Program (PEAP)."

> [!IMPORTANT]
> Mēroga vienības jauda risinājumam Supply Chain Management ir pieejama tikai tad, ja jūs piekrītat [Mākoņa + Malas priekšskatījuma Finance and Operations nosacījumiem](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Priekšskatījuma datu apstrāde

Publiskajā priekšskatījumā daži pārvaldības pakalpojumi tiks viesoti tikai Amerikas Savienotajās Valstīs. Tomēr, kad šis līdzeklis kļūst pieejams, šie pārvaldības pakalpojumi būs pieejami visos reģionos, ko atbalsta Supply Chain Management. Tas ietekmē mēroga vienības pārvaldnieka izmantotās administratīvās informācijas nodošanu un glabāšanu, tostarp:

- Jūsu nomnieka nosaukumi un ID
- Jūsu LCS projekta ID
- Administratoru e-pasta adreses, kas izmantoti, lai pierakstītos
- Vides ID centrmezglam un mēroga vienībām
- Darba slodzes konfigurācijas
- Apkopotie dati (piemēram, latentums un caurlaide), kas tiek parādīti kartēšanas analīzes lapā

Dati, kas tiek pārsūtīti uz ASV datu centriem un glabāti ASV datu centros, tiks dzēsti, kad tiks izslēgtas priekšskatījuma vides.

### <a name="sign-up-for-the-preview"></a>Parakstīšanās priekšskatījumam

Lai pierakstītos mākoņa un malas priekšskatījumā risinājumam Supply Chain Management, jūsu organizācijai jau ir jābūt dinamiskai Supply Chain Management mākoņa videi.

Mēroga vienības iespējas pašlaik ir publiskajā priekšskatījumā. Piesakoties, jums ir jāizmanto lietotāja konts noteiktam nomniekam. Šim nomniekam ir jābūt arī projekta īpašniekam vai arī vides administratoram pakalpojumā LCS aktīvām Dynamics 365 LCS projektam nomniekā.

Piesakoties priekšskatījumam, ir jāatlasa nomnieks un jāizpilda pieteikšanās darbības. Tiklīdz korporācija Microsoft var piešķirt priekšskatījuma noslodzi, mēs jums nosūtīsim e-pastu, kas ietver nodrošināšanas detaļas un veicināšanas (promo) kodus divām vidēm (centrmezgls un mēroga vienība) atbilstošam LCS projektam. Pēc tam jūs varēsiet izvietot divas vides kā 2. līmeņa smilškastes vides. Šīs vides būs derīgas 60 dienas no promo kodu izveidošanas datuma. Jūs nedrīkstat izmantot divas vides, kamēr nav pabeigta nākamajā punktā aprakstītā darbība.

Pēc tam, kad korporācija Microsoft ir apstiprinājusi, ka divas vides ir izvietotas, izmantojot promo kodus, viena no vidēm tiks konfigurēta tā, lai darbotos kā centrmezgls, un otra tiks konfigurēta, lai darbotos kā mēroga vienība. Pēc tam varat konfigurēt mēroga vienības un izvietot atlasītās noliktavas pārvaldības un ražošanas darba slodzes, izmantojot [Mēroga vienību pārvaldnieka portālu](https://aka.ms/SCMSUM).

Priekšskatījuma vides automātiski tiks dzēstas pēc 60 dienām. Tomēr tās var dzēst ātrāk, ja izrādās, ka tās netiek izmantotas. Kad priekšskatījuma vides ir izdzēstas, varat reģistrēties un stāties rindā jaunai priekšskatījuma izvietošanai.

Lai pieteiktos priekšskatījumam, dodieties uz [Mēroga vienības pārvaldnieka portālu](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Ierobežojumi, kas attiecas uz priekšskatījuma periodu

> [!IMPORTANT]
> Šī līdzekļa priekšskatījuma programmas sākotnējā fāzē Microsoft atbalsta tikai tādus centrmezglus, kuros ir mākoņu mēroga vienības, nevis centrmezgli ar malas mēroga vienībām. Malas līmeņa vienības tiek instalētas lokāli, un tās būs pieejamas nākamajā programmas fāzē.

Tā kā mākoņa un malas mēroga vienības ir priekšskatījuma funkcija, ar tām saistītie pakalpojumi pašlaik ir pieejami ierobežotās valstīs un reģionos. Iespējojot mākoņa un malas mēroga vienības, jūs apstiprināt, ka jūs saprotat, ka daži dati, kas ir saistīti ar mākoņa un malas mēroga vienību konfigurāciju un apstrādi, var tikt glabāti datu centrā, kas atrodas Amerikas Savienotajās Valstīs. Iespējojot mākoņa un malas mēroga vienības, jūs piekrītat arī [Mākoņa + Malas priekšskatījumu Finance and Operations nosacījumiem](https://Aka.ms/SCMCnETerms). Lai uzzinātu vairāk par mākoņa un malas mēroga vienībām, skatiet [dokumentāciju](https://aka.ms/scmcne).

Jūsu konfidencialitāte ir svarīga korporācijai Microsoft. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://aka.ms/privacy).

> [!IMPORTANT]
> Dažas biznesa funkcionalitātes netiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes tiek izmantotas mēroga vienībās. Papildinformāciju par funkcionālajām darba slodzēm skatiet tālāk šajā tēmā.

## <a name="scale-units-and-dedicated-workloads"></a>Mēroga vienības un specializētās darba slodzes

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 ar mēroga vienībām":::

Mēroga vienības paplašina centrālo Supply Chain Management centrmezgla vidi, pievienojot īpašu apstrādes noslodzi. Mēroga vienības var palaist mākonī. Vai arī tās var tikt palaistas uz malas jūsu vietējā uzņēmuma iestādē. Mēroga vienības var īslaicīgi atvienot no centrmezgla vides. Kad tās ir pieslēgtas, mēroga vienības saņem visu informāciju, kas nepieciešama, lai palaistu īpašo apstrādi piešķirtajām darba slodzēm.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Mēroga vienības opcijas publiskajā priekšskatījumā":::

Publiskajā priekšskatījumā varat konfigurēt centrmezgla vidi ar atlasītām darba slodzēm mākoņa mēroga vienībā, izmantojot mēroga vienību pārvaldnieka portālu. Priekšskatījuma dalībnieki, kuriem ir piekļuve lokālo biznesa datu (LBD) lokālajai videi, var arī konfigurēt LBD vidi kā malas mēroga vienību.

Darba slodze ir noteikts biznesa funkcionalitātes kopums, ko var ņemt vērā un deleģēt mēroga vienībai. Pašlaik priekšskatījumā ir divi darba slodžu veidi:

- Ražošanas izpilde
- Noliktavas vadība

Katrai mēroga vienībai var piešķirt vienu no katra veida darba slodzēm. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Īpašas ražošanas izpildes darba slodzes iespējas mēroga vienībās

Ražošanas izpildes, mākoņa un malas mēroga vienībām sniedz šādas iespējas pat tad, ja malas vienības nav saistītas ar mākoni:

- Iekārtu operatori un ražotnes uzraudzības iestādes var piekļūt operāciju ražošanas plānam.
- Iekārtu operatori var uzturēt plāna atjaunināšanu, izpildot diskrētus un procesa ražošanas darbus.
- Ražotnes vadītājs var koriģēt darbības plānu.
- Darbinieki var piekļūt ierašanās un aiziešanas reģistrācijas laikam un apmeklējumam, lai nodrošinātu pareizu darbinieka algas aprēķinu.

Plašāku informāciju skatiet [ražošanas mēroga vienības darba slodzes informācijā](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Īpašas noliktavas vadības darba slodzes iespējas mēroga vienībās

Noliktavas vadībai, mākoņa un malas mēroga vienībām sniedz šādas iespējas pat tad, ja malas vienības nav saistītas ar mākoni:

- Atlasīto kopuma metožu apstrāde ir aktivizēta pārdošanas pasūtījumiem un pieprasījuma papildināšanai.
- Noliktavas darbinieki var palaist pārdošanas un pieprasījuma papildināšanas noliktavas darbu, izmantojot noliktavas programmu.
- Noliktavas darbinieki var uzzināt par rīcībā esošajiem krājumiem, izmantojot noliktavas programmu.
- Noliktavas darbinieki var izveidot un palaist krājumu kustības, izmantojot noliktavas programmu.
- Noliktavas darbinieki var reģistrēt pirkšanas pasūtījumus un veikt atlikšanu, izmantojot noliktavas lietojumprogrammu.

Plašāku informāciju skatiet [noliktavas mēroga vienības darba slodzes informācijā](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Jūsu Supply Chain Management vides mēroga vienības

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Izvietojiet mākoņa un malas mēroga vienību priekšskatījumu

Tālāk redzamajā attēlā parādīta pierakstīšanās un nodrošinājuma plūsma mākoņa mēroga vienībām.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Priekšskatīt pieteikšanās darbības":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Atlasiet savu LCS projekta nomnieku un detalizētu priekšskatījuma procesu

Publiskajā priekšskatījumā [Mēroga vienības pārvaldnieka portāls](https://aka.ms/SCMSUM) parāda to nomnieku sarakstu, kuros ir iekļauts jūsu konts un kuros esat LCS projekta īpašnieks vai vides administrators.

Ja jūsu meklētais nomnieks nav šajā sarakstā, dodieties uz [LCS](https://lcs.dynamics.com/v2) un pārliecinieties, ka jūs esat vai nu vides administrators, vai arī LCS projekta īpašnieks šim nomniekam. Ņemiet vērā, ka tikai Azure Active Directory (Azure AD) atlasītā nomnieka konts ir autorizēts pabeigt reģistrēšanu.

> [!NOTE]
> Pēc izmaiņu veikšanas pakalpojumā LCS var paiet līdz 30 minūtēm līdz nomnieku saraksts atspoguļo izmaiņas.

Katram nomniekam saraksts parāda pieteikšanās statusu.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Reģistrēšanās opcija nomniekam":::

Atlasiet saiti **Noklikšķiniet šeit, lai pierakstītos**, lai pieteiktos jūsu LCS nomniekam, kas piedalās priekšskatījumā. Jums ir jāpiekrīt noteikumiem. Jums ir arī jāsniedz uzņēmuma e-pasta adrese, kur Microsoft var nosūtīt paziņojumus, kas saistīti ar priekšskatījuma pieteikšanās procesu.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Reģistrēšanās iesniegums nomniekam":::

Korporācija Microsoft pārskatīs jūsu pieprasījumu un sniegs informāciju par nākamajām darbībam, sūtot e-pastu uz adresi, kuru sniedzat reģistrēšanās veidlapā.

Pēc tam, kad jums ir piešķirta piekļuve priekšskatījuma programmai, jūs saņemsiet divus promo kodus jūsu LCS projektam. Tagad varat izmantot šos promo kodus, lai izvietotu divas vides pakalpojumā LCS. Vidēs jālieto PEAP izlaidums 10.0.15 vai jaunāka versija. Kad esat beidzis piemērot promo kodus, paziņojiet korporācijai Microsoft (saskaņā ar instrukciju), lai varētu pabeigt priekšskatījuma līdzekļu vides iespējošanu. Korporācija Microsoft jums paziņos, kad šī konfigurācijas darbība būs pabeigta.

Tagad varat sākt konfigurēt mēroga vienības un darba slodzes jūsu priekšskatījuma vidē.

> [!IMPORTANT]
> Konfigurējot mākoņa mēroga vienības, varat [veikt visas nepieciešamās darbības portālā Skale Unit Manager](#scale-unit-manager-portal).
<!-- >
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Pārvaldīt mākoņa mēroga vienības un darba slodzes, izmantojot portālu Skale Unit Manager

Dodieties uz [portālu Skale Unit Manager](https://aka.ms/SCMSUM) un piesakieties, izmantojot savu nomnieka kontu. Lapā **Konfigurēt mēroga vienības** varat pievienot centrmezgla vidi, ja tā jau nav norādīta sarakstā. Pēc tam varat atlasīt centrmezglu, ko vēlaties konfigurēt ar mēroga vienībām un darba slodzēm.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Mēroga vienības un darba slodzes pārvaldības pieredze":::

Lai pievienotu vienu vai vairākas mēroga vienības, kas ir pieejamas jūsu topoloģijā, atlasiet **Pievienot mēroga vienības**. Priekšskatījumā ir jābūt redzamai mākoņa mēroga vienībai, kas tika izvietota no viena no promo kodiem, ko saņēmāt kā daļu no priekšskatījuma programmas.

<!-- > [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Lai pievienotu noliktavas pārvaldības vai ražošanas izpildes darba slodzi kādai no jūsu mēroga vienībām, cilnē **Definētās darba slodzes** izmantojiet pogu **Izveidot darba slodzi**. Katrai darba slodzei jānorāda to procesu konteksts, kas piederēs šai darba slodzei. Noliktavas pārvaldības darba slodzei konteksts ir noteikta noliktava noteiktā vietā un juridiskajā personā. Ražošanas izpildes darba slodzei konteksts ir noteikta juridiskā elementa vieta.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Darba slodzes izveide":::

> [!IMPORTANT]
> Portāls Scale Unit Manager priekšskatījumā neļauj noņemt darba slodzi no mēroga vienībām vai noņemt mēroga vienību no centrmezgla pēc tam, kad ir veikta piešķire. Ja jums jānoņem piešķire, sazinieties ar savu kontaktpersonu, lai priekšskatītu programmu pārvaldību.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]