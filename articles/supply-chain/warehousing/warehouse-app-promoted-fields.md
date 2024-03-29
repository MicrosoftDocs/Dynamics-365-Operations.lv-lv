---
title: Konfigurējiet veicinātos laukus darbībām mobilajā programmā Warehouse Management
description: Šajā rakstā ir aprakstīts, kā veicināt un izcelt konkrētu informāciju par jebkuru uzdevumu plūsmu uzdevumu plūsmām mobilajā programmā Noliktavas pārvaldība.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepSelectPromotedFields, WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e2d65f20febaf9bd1d143414054b121f8decb7c0
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689835"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Konfigurējiet veicinātos laukus darbībām mobilajā programmā Warehouse Management

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šajā rakstā aprakstītie līdzekļi attiecas tikai uz jauno noliktavas pārvaldības mobilo programmu. Tie neietekmē veco noliktavas programmu, kas tagad tiek novecojusi.

Šajā rakstā ir aprakstīts, kā veicināt un izcelt konkrētu informāciju par jebkuru uzdevumu plūsmu uzdevumu plūsmām mobilajā programmā Noliktavas pārvaldība. Šī iespēja var palīdzēt pievērst darbinieku uzmanību vissvarīgākajiem laukiem, kad tie darbojas ar plūsmu. Katram procesa solim administratori var atlasīt, kurus laukus veicināt un kurus laukus iezīmēt.

## <a name="enable-promoted-fields-in-your-system"></a>Iespējojiet veicinātos laukus savā sistēmā

Ja jūs palaižat Supply Chain Management versiju 10.0.28 vai agrāk, tad, pirms varat iestatīt reklamēto lauku, jums ir jāveic tālāk norādītās darbības, lai iespējotu nepieciešamos līdzekļus un ģenerētu nepieciešamos lauku nosaukumus mobilajā programmā Noliktavas pārvaldība. Ja jūs palaižat Piegādes ķēdes pārvaldības versiju 10.0.29 vai jaunāku versiju, šīs funkcijas ir obligātas un tās nevar izslēgt, tādēļ varat izlaist šo procedūru.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**. (Skatiet [Līdzekļu pārvaldības apskats](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai iegūtu papildinformāciju par šo lapu.)
1. Pārliecinieties, vai *jūsu sistēmai ir ieslēgta* noliktavas programmas darbību norādījumu funkcija. Šis līdzeklis ir priekšnosacījums līdzeklim *Warehouse programmas veicinātie lauki*. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 tas ir obligāts un to nevar izslēgt. Papildinformāciju par līdzekli *Warehouse programmas darbību norādījumi* skatiet sadaļā [Warehouse Management mobilās lietojumprogrammas darbību nosaukumu pielāgošana un instrukcijas](mobile-app-titles-instructions.md).
1. Pārliecinieties, vai *jūsu sistēmai ir ieslēgta noliktavas* programmas reklamēto lauku funkcija. Šī ir šajā rakstā aprakstītā funkcija. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 tas ir obligāts un to nevar izslēgt.
1. Atjauniniet lauku nosaukumus Warehouse Management mobilajā programmā, apmeklējot **Warehouse Management \> Iestatījums \> Mobilā ierīce \> Warehouse programmas lauku nosaukumi** un atlasot **Izveidot noklusējuma iestatījumus**. Atkārtojiet šo darbību katrai juridiskajai personai (uzņēmumam), kas izmanto mobilo programmu Noliktavas pārvaldība. Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurēt veicinātos laukus no izvēlnes raksturīgās pārlabošanas

Izmantojiet šo procedūru, lai iestatītu veicinātos laukus.

1. Izveidojiet izvēlnei raksturīgu pārlabošanu atbilstošai izvēlnei un darbību, kā tas ir aprakstīts sadaļā [Pielāgot darbību nosaukumus un instrukcijas mobilajai programmai Warehouse Management](mobile-app-titles-instructions.md).
1. Atrodiet to **Soļa ID** un **Izvēlnes elementu nosaukumu** vērtību kombināciju, ko vēlaties rediģēt, un pēc tam atlasiet vērtību kolonnā **Soļa ID**.
1. Lapā, kas tiek parādīta kopsavilkuma cilnē **Atlasīt veicinātos laukus**, rīkjoslā atlasiet **Atlasīt laukus**.
1. Dialoglodziņā **Veicinātie lauki** atlasiet laukus, kurus vēlaties veicināt. Var arī iezīmēt līdz diviem atlasītajiem laukiem. Izceltie lauki Warehouse Management mobilajā programmā tiks rādīti treknrakstā. Atlasot laukus, ņemiet vērā faktu, ka daži ekrāni var būt tik lieli, lai rādītu tikai augšējos vai divus veicinātos laukus. Piemēru, kurā parādīts, kā izmantot šos iestatījumus, skatiet tālāk šī raksta scenāriju.

    > [!NOTE]
    > Saraksts **Pieejamie lauki** ir ierobežots ar laukiem, kas var parādīties izvēlnes elementam. Tomēr citi faktori (piemēram, krājumu sastāvs) nosaka, vai lauks faktiski parādās Warehouse Management mobilajā programmā. Ja esat konfigurējis veicinātos laukus, tad Warehouse Management mobilās programmas galvenajā lapā tiks rādīti tikai atlasītie lauki. Tomēr darbinieki joprojām var apskatīt atlikušos laukus detalizētas informācijas lapā.

1. Atlasiet **Labi**, lai piemērotu jūsu iestatījumus. Atlasītie lauki ir uzskaitīti kopsavilkuma cilnē **Atlasīt veicinātos laukus**.

## <a name="example-scenario"></a>Piemērs

### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai izmantotu norādītos parauga ierakstus un vērtības, lai darbotos šajā scenārijā, jums ir jāizmanto sistēma, kur ir instalēti [standarta](../../fin-ops-core/fin-ops/get-started/demo-data.md) demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigurēt pārdošanas izdošanu, izmantojot atbalstītos soļus numura zīmes darbībā

Šajā procedūrā numura zīmes darbībā iestatīsiet izvēlnes vienumam **Pārdošanas izdošana** veicinātos un izceltos laukus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Atrodiet darbības ID, kas ir nosaukts *LicensePlateId*, un izvēlieties to.
1. Darbību rūtī atlasiet **Pievienot darbības konfigurāciju**.
1. Nolaižamajā dialoglodziņā izmantojiet lauku **Izvēlnes elements**, lai atrastu un atlasītu *Pārdošanas izdošanu*.
1. Atlasiet **Labi**.
1. Parādās tikko izveidotās pārlabošanas detalizētas informācijas lapa. Kopsavilkuma cilnē **Atlasīt veicinātos laukus**, rīkjoslā atlasiet **Atlasīt laukus**.
1. Dialoglodziņā **Veicinātie lauki** var atlasīt laukus, kurus vēlaties veicināt un izcelt. Sarakstā **Pieejamie lauki** atrodiet un atlasiet šādus laukus un izmantojiet pogas, lai pārvietotu tos uz sarakstu **Atlasītie lauki**:

    - Atrašanās vieta
    - Krājums
    - Preces nosaukums
    - Krājumu statuss

1. Izmantojiet pogas ar augšupvērsto un lejupvērsto bultiņu, lai pielāgotu lauku secību sarakstā **Atlasītie lauki**. Warehouse Management mobilajā programmā šie lauki tiks parādīti tādā kārtībā, kā iestatīts šeit.
1. Atlasiet lauku **Novietojums**, un tad atlasiet **Izcelt**.
1. Atlasiet **Labi**, lai saglabātu konfigurāciju.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Skatiet veicinātos laukus mobilajā programmā Warehouse Management

Šajā procedūrā atvēriet mobilo programmu Warehouse Management un veiciet darbības, lai skatītu laukus, kurus esat veicinājāt un izcelāt iepriekšējā procedūrā.

1. Microsoft Dynamics 365 Supply Chain Management izveidojiet pārdošanas pasūtījumu, kam būs nepieciešama izdošanas darbība, lai izdotu no novietojuma, kam ir izsekota numura zīme. Tad atlasiet pārdošanas pasūtījumu, kuru tikko izlaidāt noliktavā. Pierakstiet ģenerēto darba ID.
1. Atvēriet Warehouse Management mobilo programmu pierakstieties noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot *24* kā lietotāja ID un *1* kā paroli.)
1. Izvēlieties **Nosūtīšanas** izvēlni un tad izvēlieties **Pārdošanas izdošanas** izvēlnes elementu.
1. Sekojiet datu ievades instrukcijām uz ekrāna, lai ievadītu darba ID, kas tika izveidots 1. darbībā.
1. Darbībā, kas ietver tekstu **Skenēt numura zīmi**, jums ir jāredz detalizētas informācijas lapā veiktās izmaiņas. Lauki parādās tādā secībā, kā iestatīts veicinātajiem laukiem, un lauks **Novietojums** tiek parādīts treknrakstā.
