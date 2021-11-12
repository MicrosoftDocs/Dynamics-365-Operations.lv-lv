---
title: Konfigurējiet veicinātos laukus darbībām mobilajā programmā Warehouse Management
description: Šajā tēmā ir aprakstīts, kā veicināt un izcelt konkrētu informāciju par jebkuru posmu uzdevumu plūsmās Warehouse Management mobilajai lietojumprogrammai.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 05ca38e366331c2132bb46eddf77ae2ef371256b
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678646"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Konfigurējiet veicinātos laukus darbībām mobilajā programmā Warehouse Management

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: GA with 10.0.23 -->

> [!IMPORTANT]
> Šajā tēmā aprakstītie līdzekļi attiecas tikai uz jauno Warehouse Management mobile programmu. Tie neietekmē veco noliktavas programmu, kas tagad tiek novecojusi.

Šajā tēmā ir aprakstīts, kā veicināt un izcelt konkrētu informāciju par jebkuru posmu uzdevumu plūsmās Warehouse Management mobilajai lietojumprogrammai. Šī iespēja var palīdzēt pievērst darbinieku uzmanību vissvarīgākajiem laukiem, kad tie darbojas ar plūsmu. Katram procesa solim administratori var atlasīt, kurus laukus veicināt un kurus laukus iezīmēt.

## <a name="enable-promoted-fields-in-your-system"></a>Iespējojiet veicinātos laukus savā sistēmā

Lai iespējotu nepieciešamos līdzekļus, pirms varat iestatīt atbalstītos laukus, ir jāveic tālāk norādītās darbības un jāģenerē nepieciešamie lauku nosaukumi mobilajā programmā Warehouse Management.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Darbvietā [**Līdzekļu pārvaldība** darbvieta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iespējojiet līdzekli, kas ir uzskaitīts šādā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Programmas Warehouse darbību norādījumi*

    Papildinformāciju par līdzekli *Warehouse programmas darbību norādījumi* skatiet sadaļā [Warehouse Management mobilās lietojumprogrammas darbību nosaukumu pielāgošana un instrukcijas](mobile-app-titles-instructions.md). Šis līdzeklis ir priekšnosacījums līdzeklim *Warehouse programmas veicinātie lauki*.

1. Iespējojiet līdzekli, kas ir uzskaitīts tālāk minētajā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Warehouse programmas veicinātie lauki*

    Šis līdzeklis ir līdzeklis, kas ir aprakstīts šajā tēmā.

1. Atjauniniet lauku nosaukumus Warehouse Management mobilajā programmā, apmeklējot **Warehouse Management \> Iestatījums \> Mobilā ierīce \> Warehouse programmas lauku nosaukumi** un atlasot **Izveidot noklusējuma iestatījumus**. Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).
1. Atkārtojiet iepriekšējo darbību katrai juridiskajai personai (uzņēmumam), kur izmantojat mobilo programmu Warehouse Management.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurēt veicinātos laukus no izvēlnes raksturīgās pārlabošanas

Izmantojiet šo procedūru, lai iestatītu veicinātos laukus.

1. Izveidojiet izvēlnei raksturīgu pārlabošanu atbilstošai izvēlnei un darbību, kā tas ir aprakstīts sadaļā [Pielāgot darbību nosaukumus un instrukcijas mobilajai programmai Warehouse Management](mobile-app-titles-instructions.md).
1. Atrodiet to **Soļa ID** un **Izvēlnes elementu nosaukumu** vērtību kombināciju, ko vēlaties rediģēt, un pēc tam atlasiet vērtību kolonnā **Soļa ID**.
1. Lapā, kas tiek parādīta kopsavilkuma cilnē **Atlasīt veicinātos laukus**, rīkjoslā atlasiet **Atlasīt laukus**.
1. Dialoglodziņā **Veicinātie lauki** atlasiet laukus, kurus vēlaties veicināt. Var arī iezīmēt līdz diviem atlasītajiem laukiem. Izceltie lauki Warehouse Management mobilajā programmā tiks rādīti treknrakstā. Atlasot laukus, ņemiet vērā faktu, ka daži ekrāni var būt tik lieli, lai rādītu tikai augšējos vai divus veicinātos laukus. Piemēru, kas parāda, kā izmantot šos iestatījumus, skatiet tālāk šīs tēmas scenārijā.

    > [!NOTE]
    > Saraksts **Pieejamie lauki** ir ierobežots ar laukiem, kas var parādīties izvēlnes elementam. Tomēr citi faktori (piemēram, krājumu sastāvs) nosaka, vai lauks faktiski parādās Warehouse Management mobilajā programmā. Ja esat konfigurējis veicinātos laukus, tad Warehouse Management mobilās programmas galvenajā lapā tiks rādīti tikai atlasītie lauki. Tomēr darbinieki joprojām var apskatīt atlikušos laukus detalizētas informācijas lapā.

1. Atlasiet **Labi**, lai piemērotu jūsu iestatījumus. Atlasītie lauki ir uzskaitīti kopsavilkuma cilnē **Atlasīt veicinātos laukus**.

## <a name="example-scenario"></a>Piemērs

### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai izmantotu norādītos parauga ierakstus un vērtības šī scenārija izmantošanai, jāizmanto sistēma, kurā instalēti standarta demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

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
