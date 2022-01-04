---
title: Konfigurēt novirzīšanas darbības mobilo ierīču izvēlnes vienumos
description: Šajā tēmā aprakstīts, kā konfigurēt izvēlnes elementu novirzīšanu, lai darbinieki varētu novietot pašreizējo uzdevumu, veikt citu uzdevumu un pēc tam atgriezties pie sākotnējā uzdevuma, nezaudējot informāciju.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 874abbdf7c0938a7ad4cc66e23dd01d901a1f0d3
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920352"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Konfigurēt novirzīšanas darbības mobilo ierīču izvēlnes vienumos

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šajā tēmā aprakstītie līdzekļi attiecas tikai uz jauno Warehouse Management mobile programmu. Tie neietekmē veco noliktavas programmu, kas tagad tiek novecojusi.

Šajā tēmā aprakstīts, kā konfigurēt izvēlnes elementu novirzīšanu, lai darbinieki varētu novietot pašreizējo uzdevumu, veikt citu uzdevumu un pēc tam atgriezties pie sākotnējā uzdevuma, nezaudējot informāciju.

Novirzīšana ir atsevišķs izvēlnes elements, ko var atvērt, veicot galveno uzdevumu. Novirzīšanas beigās darbinieks tiek atgriezts vietā, kur atstāj galveno uzdevumu. Konfigurācijas laikā ir jānorāda izvēlnes vienums, kam jādarbojas kā novirzīšanai. Jūs arī atlasāt, kuras lauku vērtības no galvenā uzdevuma automātiski jāpārsūta (jākopē) uz novirzīšanu un jāievada tur. Tāpēc jums ir jāsaprot, kur uzdevumu plūsmā vēlaties, lai novirzīšana būtu pieejama darbiniekiem. Jums jānodrošina arī, lai informācija, kas jākopē uzdevumu plūsmā, būtu pieejama šajā uzdevumu plūsmas darbībā.

## <a name="enable-detours-in-your-system"></a>Iespējot novirzīšanu jūsu sistēmā

Lai iespējotu nepieciešamos līdzekļus, pirms varat konfigurēt mobilo ierīču izvēlnes elementu darbību novirzīšanu,, ir jāveic tālāk norādītās darbības un jāģenerē nepieciešamie lauku nosaukumi mobilajā programmā Warehouse Management.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Darbvietā [**Līdzekļu pārvaldība** darbvieta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iespējojiet līdzekli, kas ir uzskaitīts šādā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Programmas Warehouse darbību norādījumi*

    Papildinformāciju par līdzekli *Warehouse programmas darbību norādījumi* skatiet sadaļā [Warehouse Management mobilās lietojumprogrammas darbību nosaukumu pielāgošana un instrukcijas](mobile-app-titles-instructions.md). Šis līdzeklis ir priekšnosacījums līdzeklim *Warehouse Management programmas novirzīšana*.

1. Iespējojiet līdzekli, kas ir uzskaitīts tālāk minētajā veidā:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Līdzekļa nosaukums:** *Warehouse management programmas novirzīšana*

    Šis līdzeklis ir līdzeklis, kas ir aprakstīts šajā tēmā.

1. Atjauniniet lauku nosaukumus Warehouse Management mobilajā programmā, apmeklējot **Warehouse Management \> Iestatījums \> Mobilā ierīce \> Warehouse programmas lauku nosaukumi** un atlasot **Izveidot noklusējuma iestatījumus**. Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).
1. Atkārtojiet iepriekšējo darbību katrai juridiskajai personai (uzņēmumam), kur izmantojat mobilo programmu Warehouse Management.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigurēt novirzīšanu no izvēlnes raksturīgās pārlabošanas

Izmantojiet šo procedūru, lai iestatītu novirzīšanu no izvēlnes raksturīgas pārlabošanas.

1. Izveidojiet izvēlnei raksturīgu pārlabošanu atbilstošai izvēlnei un darbību, kā tas ir aprakstīts sadaļā [Pielāgot darbību nosaukumus un instrukcijas mobilajai programmai Warehouse Management](mobile-app-titles-instructions.md).
1. Atrodiet to **Soļa ID** un **Izvēlnes elementu nosaukumu** vērtību kombināciju, ko vēlaties rediģēt, un pēc tam atlasiet vērtību kolonnā **Soļa ID**.
1. Lapā, kas tiek parādīta kopsavilkuma cilnē **Pieejamās novirzīšanās (izvēlnes vienumi)**, varat norādīt izvēlnes elementu, kam jādarbojas kā novirzīšana. Var arī atlasīt, kuras lauku vērtības no galvenā uzdevuma automātiski jākopē uz un no novirzīšanas. Piemērus, kas parāda, kā izmantot šos iestatījumus, skatiet tālāk šīs tēmas scenārijos.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>1. scenārija paraugs: pārdošanas izdošana, ja pieprasījums par novietojumu darbojas kā novirzīšana

Šajā scenārijā ir parādīts, kā konfigurēt pieprasījumu par atrašanās vietu kā novirzīšanu ar darbinieku vadītu pārdošanas izdošanas uzdevumu plūsmu. Šī novirzīšana iespējos darbiniekus meklēt visas numura zīmes atrašanās vietā, no kuras tie tiek izdoti, un izdot numura zīmi, ko vēlas izmantot izdošanas pabeigšanai. Šis novirzīšanas tips var būt noderīgs, ja svītrkods ir bojāts un tāpēc skenera ierīce to nevar nolasīt. Vai arī tas var noderēt, ja darbiniekam ir jāuzzina, kas patiesībā atrodas sistēmā. Ņemiet vērā, ka šis scenārijs darbojas tikai tad, ja izdodat no numura zīmes kontrolētiem novietojumiem.

### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai izmantotu norādītos parauga ierakstus un vērtības šī scenārija izmantošanai, jāizmanto sistēma, kurā instalēti standarta demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Izveidot izvēlnei raksturīgo pārlabošanu un konfigurēt 1. scenārija novirzīšanu

Šajā procedūrā numura zīmes darbībā kofigurēsiet izvēlnes vienumam **Pārdošanas izdošana** novirzīšanu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Atrodiet darbības ID, kas ir nosaukts *LicensePlateId*, un izvēlieties to.
1. Darbību rūtī atlasiet **Pievienot darbības konfigurāciju**.
1. Nolaižamajā dialoglodziņā izmantojiet lauku **Izvēlnes elements**, lai atrastu un atlasītu *Pārdošanas izdošanu*.
1. Atlasiet **Labi**.
1. Parādās tikko izveidotās pārlabošanas detalizētas informācijas lapa. Kopsavilkuma cilnē **Pieejamās novirzīšanas (izvēlnes vienumi)** rīkjoslā atlasiet **Pievienot**.
1. Dialoglodziņā **Pievienot novirzīšanu** kā novirzīšanu atlasiet **Novietojuma pieprasījums**, kas būs pieejams mobilajā programmā Warehouse Management.
1. Atlasiet **Labi**.
1. Kopsavilkuma cilnē **Pieejamās novirzīšanas (izvēlnes vienumi)** atlasiet tikko pievienoto novirzīšanu un pēc tam atlasiet **Atlasīt laukus nosūtīšanai** rīkjoslā.
1. Dialoglodziņā **Atlasīt laukus nosūtīšanai**, norādiet informāciju, kas jānosūta uz un no novirzīšanas. Šajā scenārijā jūs ļaujat darbiniekiem izmantot atrašanās vietu, kas viņiem ir jāatlasa kā ievade, lai veiktu novietojuma pieprasījuma novirzīšanu. Tādēļ sadaļā **Nosūtīt no pārdošanas izdošanas** atlasiet **Pievienot** rīkjoslā, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādas vērtības:

    - **Kopēt no pārdošanas izdošanas:** *Novietojums*
    - **Ielīmēt novietojuma pieprasījumā:** *Novietojums*

1. Tā kā šajā scenārijā novirzīšana ir konfigurēta numura zīmes darbībā, darbiniekiem būs noderīgi, ja darbinieki no pieprasījuma var novietot numura zīmi atpakaļ galvenajā plūsmā. Tādēļ sadaļā **Atgriezt no novietojuma pieprasījuma** atlasiet **Pievienot** rīkjoslā, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādas vērtības:

    - **Kopēt no novietojuma pieprasījuma:** *Numura zīme*
    - **Ielīmēt pārdošanas izdošanā:** *Numura zīme*

1. Atlasiet **Labi**.

Tagad novirzīšana ir pilnībā konfigurēta. Poga **Novietojuma pieprasījums** novirzīšanas uzsākšanai paradīsies numura zīmes darbībā izvelnes elementam **Pārdošanas izdošana**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Pabeidziet pārdošanas izdošanu mobilajā ierīcē un izmantojiet novirzīšanu

Šajā procedūrā izpildīsiet pārdošanas izdošanu, izmantojot mobilo programmu Warehouse Management. Jūs izmantosiet novirzīšanu, ko tikko konfigurējāt, lai atrastu numura zīmi, ko izmantosiet izdošanas darbības pabeigšanai.

1. Microsoft Dynamics 365 Supply Chain Management izveidojiet pārdošanas pasūtījumu, kam būs nepieciešama izdošanas darbība, lai izdotu no novietojuma, kam ir izsekota numura zīme. Tad atlasiet pārdošanas pasūtījumu, kuru tikko izlaidāt noliktavā. Pierakstiet ģenerēto darba ID.
1. Atvēriet Warehouse Management mobilo programmu pierakstieties noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot *24* kā lietotāja ID un *1* kā paroli.)
1. Izvēlieties **Nosūtīšanas** izvēlni un tad izvēlieties **Pārdošanas izdošanas** izvēlnes elementu.
1. Sekojiet datu ievades instrukcijām uz ekrāna, lai ievadītu darba ID, kas tika izveidots 1. darbībā.
1. Darbībā, kas ietver tekstu **Skenēt numura zīmi**, atveriet darbību izvēlni. Jums vajadzētu redzēt jaunu pogu, kas ir apzīmēta ar **Novietojuma pieprasījums**. Bultiņa augšējā kreisajā stūrī norāda, ka poga startēs novirzīšanu. Atlasiet **Novietojuma pieprasījums**.
1. Novirzīšana ir sākta. Nākamajā lapā apstipriniet novietojumu, kas tika kopēts no galvenās plūsmas.
1. Novietojumā pieejamo numura zīmi sarakstā pieskaries numura zīmei, ko vēlaties kopēt atpakaļ galvenajā plūsmā. Pēc tam atlasiet pogu **Atpakaļ**.
1. Jūs esat atgriezies pārdošanas izdošanas galvenajā plūsmā, un numura zīme tika kopēta atpakaļ uz to no novirzīšanas. Apstipriniet vērtību, lai turpinātu ar nākamo darbību.
1. Tagad varat pabeigt atlikušo standarta plūsmu, ievadot pieprasītās datu ievades instrukcijas.

Noliktavas darbs tagad ir pabeigts. Darbinieks sekmīgi atvēra novirzīšanu, lai veiktu sekundāro uzdevumu (pieprasījumu par novietojumu), nepazaudējot vietu galvenajā uzdevumā, un atgrieza informāciju, kas bija nepieciešama galvenā uzdevuma izpildei.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>2. scenārija paraugs: krājuma pieprasījums ar pārvietošanas un koriģēšanas novirzīšanām

Šajā scenārijā ir parādīts, kā konfigurēt pārvietošanu un pielāgojumus kā vairākas novirzīšanas novietojuma pieprasījuma uzdevumu plūsmā. Šī iespēja var būt noderīga situācijās, kad darbinieks ierodas novietojumā, atrod, ka krājums novietojumā atšķiras no sistēmā reģistrētā un tādēļ ir jāpielāgo vai jāpārvieto preces.

Pieprasījumu par novietojumu var aizstāt ar noliktavas vienības pieprasījumu vai arī ar krājumu pieprasījumu.

### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai izmantotu norādītos parauga ierakstus un vērtības šī scenārija izmantošanai, jāizmanto sistēma, kurā instalēti standarta demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Izveidot izvēlnei raksturīgo pārlabošanu un konfigurēt 2. scenārija novirzīšanu

Šajā procedūrā numura zīmes darbībā kofigurēsiet izvēlnes vienumam **Pārdošanas izdošana** novirzīšanu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Atrodiet un atlasiet darbības ID, kas ir nosaukts *LocationInquiryList*.

    > [!NOTE]
    > Lai izmantotu krājuma pieprasījumu, nevis pieprasījumu par novietojumu, atlasiet rindu, kur darbības ID ir nosaukts *ItemInquiryList*. Lai izmantotu numura zīmes pieprasījumu, atlasiet rindu, kur darbības ID ir nosaukts *LPInquiryList*.

1. Darbību rūtī atlasiet **Pievienot darbības konfigurāciju**.
1. Nolaižamajā dialoglodziņā izmantojiet lauku **Izvēlnes elements**, lai atrastu un atlasītu *Novietojuma pieprasījums*.
1. Atlasiet **Labi**.
1. Parādās tikko izveidotās pārlabošanas detalizētas informācijas lapa. Kopsavilkuma cilnē **Pieejamās novirzīšanas (izvēlnes vienumi)** rīkjoslā atlasiet **Pievienot**.
1. Dialoglodziņā **Pievienot novirzīšanu** kā novirzīšanu atlasiet **Pārvietošana**, kas būs pieejams mobilajā programmā Warehouse Management.
1. Atlasiet **Labi**.
1. Kopsavilkuma cilnē **Pieejamās novirzīšanas (izvēlnes vienumi)** atlasiet tikko pievienoto novirzīšanu un pēc tam atlasiet **Atlasīt laukus nosūtīšanai** rīkjoslā.
1. Dialogā **Atlasīt laukus nosūtīšanai**, norādiet informāciju, kas jānosūta uz un no novirzīšanas. Šajā scenārijā ir paredzams, ka darbinieki meklēs novietojumus, kas ir kontrolēti no numura zīmes. Tāpēc būs lietderīgi kopēt numura zīmi no pieprasījuma uz **Pārvietošana** novirzīšanu. Sadaļā **Nosūtīt no pārdošanas izdošanas** atlasiet **Pievienot** rīkjoslā, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādas vērtības:

    - **Kopēt no novietojuma pieprasījuma:** *Novietojums*
    - **Ielīmēt Pārvietošanā:** *Atrašanās vieta/Noliktavas vienība*

    Šajā novirzīšanā nav paredzēts kopēt jebkādu informāciju, jo galvenā plūsma bija pieprasījums, kurā papildu darbības nav nepieciešamas.

1. Atlasiet **Labi**.

Tagad novirzīšana ir pilnībā konfigurēta. Poga **Pārvietošana** novirzīšanas uzsākšanai paradīsies numura zīmes darbībā izvelnes elementam **Novietojuma pieprasījums**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Veiciet pieprasījumu par novietojumu mobilajā ierīcē un izmantojiet novirzīšanu

Šajā procedūrā veiksiet pieprasījumu par novietojumu, izmantojot mobilo programmu Warehouse Management. Tad izmantosiet šo novirzīšanu, lai pabeigtu preču kustību.

1. Atvēriet Warehouse Management mobilo programmu pierakstieties noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot *24* kā lietotāja ID un *1* kā paroli.)
1. Izvēlieties **Krājumi** izvēlni un tad izvēlieties **Novietojuma pieprasījums** izvēlnes elementu.
1. Ievadiet novietojumu, par kuru vaicāt, piemēram, *FL-001*.
1. Kad tiek parādīts saraksts, pieskarties un turiet vienu no tajā redzamajām kartēm, lai parādītu pieejamās novirzīšanas.
1. Atlasīt **Pārvietošana**.
1. Ievērojiet, ka numura zīme ir kopēta no atlasītās kartes. Apstipriniet vērtību.
1. Tagad ir iespējams sekot standarta uzdevumu plūsmai, lai pabeigtu kustību. Kad darbs ir pabeigts, atveriet darbību izvēlni un atlasiet **Atcelt**.
1. Jūs esat atgriezies uz lapu **Novietojuma pieprasījums**. Ņemiet vērā, ka vērtības netiek atjauninātas automātiski. Tādēļ lapa ir jāatsvaidzina manuāli, lai redzētu izmaiņas no pārvietošanas novirzīšanas.
