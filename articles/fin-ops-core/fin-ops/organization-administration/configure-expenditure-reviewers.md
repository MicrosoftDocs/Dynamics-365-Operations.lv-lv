---
title: Konfigurēt izdevumu pārskatītājus
description: Šajā tēmā ir aprakstīts, kā izmantot izdevumu pārskatītājus, lai dinamiski atlasītu lietotāju, kam piešķirts darbplūsmas uzdevums, apstiprinājums vai manuāls lēmums.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070150"
---
# <a name="configure-expenditure-reviewers"></a>Konfigurēt izdevumu pārskatītājus
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Dinamisko izdevumu pārskatītājus varat iestatīt izdevumu maršrutēšanai, lai veiktu pārskatīšanu, pamatojoties vai nu uz lietotāju, kurš ir nozīmēts projekta lomai vai finanšu dimensijai, kurā šie izdevumi tiek iekasēti. Darbplūsmas process izmanto norādīto projekta lomu vai finanšu dimensijas īpašnieku, lai noteiktu, kam maršrutēt izdevumus.

Varat definēt vienu vai vairākas izdevumu pārskatītāju konfigurācijas un tad atlasīt konfigurāciju, veidojat darbplūsmu. Izdevumu pārskatītāju vērtības katrai juridiskajai personai jūsu organizācijā var konfigurēt. Pēc izdevumu pārskatītāju konfigurāciju definēšanas ir jāpiešķir šī konfigurācija. Izdevumu pārskatītājus var piešķirt darbplūsmas uzdevumiem, apstiprinājumiem un manuāliem lēmumiem.

> [!NOTE]
> Lai arī izdevumu pārskatītāji nav obligāti, tie var palīdzēt vienkāršot darbplūsmas konfigurēšanu. Piemēram, nav jāizveido nosacījuma lēmums, lai pārbaudītu katru izmaksu centra dimensiju, un pēc tam nav jāizveido cits elements, lai piešķirtu apstiprinājumu vai uzdevumu noteiktam lietotājam vai lietotāju grupām. Tā vietā varat konfigurēt izmaksu centra dimensijas īpašnieku un izmantot izdevumu pārskatītāju, lai dinamiski atlasītu pareizo lietotāju. Šādā veidā, kad mainās izmaksu centru īpašnieks vai piešķire, ir jāatjaunina finanšu dimensijas lauks **Īpašnieks**.

## <a name="types-of-expenditure-reviewers"></a>Izdevumu pārskatītāju veidi

Ne visas darbplūsmas atbalsta izdevumu pārskatītāju koncepciju. Pēc noklusējuma var konfigurēt izdevumu pārskatītājus pirkšanas pieprasījumiem, pirkšanas pasūtījumiem, kreditora rēķiniem un izdevumu pārskatiem. Katram no šiem darbplūsmas tipiem nepieciešams konfigurēt izdevumu pārskatītājus atsevišķā lapā, kas ir raksturīga funkcionalitātei un modulim. Katram atbalstītjam dokumentam izdevumu pārskatītājus var izmantot vai nu ar virsraksta līmeņa darbplūsmām, vai arī ar rindas līmeņa darbplūsmām.

Tabulā ir parādīts, kur jākonfigurē izdevumu pārskatītājs katram atbalstītajā dokumentam.

| Attaisnoj. dokuments | Navigācijas ceļš |
|----------|-----------------|
| Izdevumu pārskati | Izdevumu pārvaldība \> Iestatījums \> Politikas \> Izdevumu pārskatītāji |
| Pirkšanas pasūtījumi | Sagāde un ieguve \> Iestatījums \> Politikas \> Pirkšanas pasūtījumu izdevumu pārskatītāji |
| Pirkšanas pieprasījumi | Sagāde un ieguve \> Iestatījums \> Politikas \> Pirkšanas pieprasījuma izdevumu pārskatītāji |
| Kreditora rēķini | Doties uz Parādi kreditoriem \> Politikas iestatīšana \> Kreditora rēķina izdevumu pārskatītāji |

## <a name="expenditure-reviewer-assignments"></a>Izdevumu pārskatītāju piešķires

Katram izdevumu pārskatītājam ir pieejami divi piešķires tipi: *projektu sadales* un *organizāciju sadales*. Projektu sadalei var atlasīt starp projektu iestādēm un finanšu dimensijām. Organizāciju sadalei var atlasīt finanšu dimensijas.

Projekta iestādes ietver projekta vadītāju, projekta kontrolieri un projekta pārdošanas vadītāju. Šīs iestādes tiek definētas projektā tieši, atlasot darbinieku atbilstošos laukos.

Finanšu dimensijas kontrolē kontu struktūras katrā juridiskajā persona. Katrai juridiskajai personai var atlasīt, kuras finanšu dimensijas tiks izmantotas ar izdevumu pārskatītāju. Dimensijas var būt no projekta (šajā gadījumā atlasiet dimensijas cilnē **Projektu sadale** ) vai no dokumenta (šajā gadījumā atlasiet dimensijas cilnē **Organizāciju sadale** ). Laukā **Īpašnieks** lapā **Finanšu dimensiju vērtības** varat atlasīt darbinieku katrai finanšu dimensijai.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>1. piemērs: izdevumu pārskatītājs, pamatojoties uz organizāciju sadalēm

Jūs strādājat uzņēmumā Contoso Appliances, un jūsu organizācijā ir seši departamenti un 10 izmaksu centri. Kad tiek iesniegts jauns pirkšanas pieprasījums, vispirms jāapstiprina no nodaļas vadītāja un pēc tam no izmaksu centra pārvaldnieka.

Šim piemēram jūs konfigurējat divus *pirkšanas pieprasījumu izdevumu pārskatītājus*:

- Pirmajam pārskatītājam nosaucat departamentu un pēc tam cilnē **Organizācijas sadales** atlasiet finanšu dimensiju **Nodaļa**. 
- Otrajām pārskatītājam nosaucat izmaksu centr un pēc tam cilnē **Organizācijas sadales** atlasiet finanšu dimensiju **Izmaksu centrs**.

Konfigurējot darbplūsmu, ir jāizveido divas apstiprināšanas darbības. Pirmā ir nodaļai, otrā ir izmaksu centram. Katram apstiprinājuma elementam atlasiet **Dalībnieks** laukā **Piešķires tips** cilnē **Uz lomas balstīts**, atlasiet **Izdevumu dalībnieki** laukā **Dalībnieka tips** un pēc tam laukā **Dalībnieks** atlasiet atbilstošo dalībnieku.

Kad pirkšanas pieprasījums ir izveidots, pirkšanas pieprasījuma rindām tiek piešķirtas nodaļas un izmaksu centra finanšu dimensijas. Kad darbplūsma ir iesniegta, sistēma vispirms novērtē pirkšanas pieprasījuma nodaļu un piešķir apstiprinājuma elementu lietotājam, kurš ir saistīts ar darbinieku, kuru atlasījāt nodaļai. Kad pirmā apstiprināšanas darbība ir pabeigta, sistēma novērtē otro apstiprināšanas darbību un piešķir otro apstiprināšanas elementu lietotājam, kurš ir saistīts ar darbinieku, kuru izvēlējāties izmaksu centram.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>2. piemērs: izdevumu pārskatītājs, pamatojoties uz projektu sadalēm

Jūs strādājat Contoso Appliances pakalpojumu nodaļā. Organizācijai nepieciešams, lai projektu vadītājam katram pirkšanas pasūtījumam būtu jāapstiprina izdevumi. Turklāt projekta izmaksu centra vadītājam tas ir jāapstiprina. Apstiprinājumus var veikt vienlaicīgi. Jebkurā gadījumā abiem lietotājiem ir jāapstiprina pirkšanas pasūtījums, pirms darbplūsma var turpināties.

Šajā piemērā jūs izveidojat vienu *pirkšanas pasūtījuma izdevumu pārskatītāju*, kura nosaukums ir **PM un Izmaksu centrs**. Atzīmējiet izvēles rūtiņu **Projekta vadītājs** un iestatiet opciju **Izmaksu centra dimensija** uz **Jā** cilnē **Projekta sadales** lapā **Pirkšanas pasūtījuma izdevumu pārskatītājs**. Kā konfigurācijas daļa jums ir jānodrošina, lai lauks **Projekta vadītājs** būtu iestatīts visiem projektiem un ka īpašnieks ir noteikts visiem izmaksu centriem lapā **Finanšu dimensijas vērtības**.

Konfigurējot darbplūsmu, nepieciešams viens apstiprinājuma elements. Atlasiet **Dalībnieks** laukā **Piešķires tips**. Pēc tam cilnē **Uz lomas balstīts** atlasiet **Izdevumu dalībnieki** laukā **Dalībnieka tips** un laukā **Dalībnieks** atlasiet projekta vadītāju un izmaksu centru. Lai nodrošinātu, ka darbplūsmu nevar turpināt, kamēr nav apstiprināts gan projekta vadītājs, gan izmaksu centra īpašnieks darbplūsmu, iestatiet lauku **Pabeigšanas politika** uz **Visi apstiprinātāji**.

Kad pirkšanas pasūtījums ir izveidots, jābūt norādītam laukam **Projekts**. Ja nepieprasa projektu visiem pirkšanas pasūtījumiem, pirms apstiprināšanas darbības palaišanas darbplūsmai jāpievieno nosacījuma lēmums, lai pārbaudītu projektu. Pēc tam sistēma novērtē projektu, kas ir norādīts pirkšanas pasūtījumam, un piešķir apstiprinājuma elementu lietotājam, kurš ir saistīts ar darbinieku laukā **Projekta pārvaldnieks**. Turklāt sistēma izveido uzdevumu un piešķir to lietotājam, kurš ir saistīts ar darbinieku, kuru atlasa laukā **Īpašnieks** izmaksu centram no projekta. Ievērojiet, ka šajā piemērā tiek izmantots projekta izmaksu centrs, nevis pirkšanas pasūtījuma izmaksu centrs.

## <a name="set-up-expenditure-reviewers"></a>Izdevumu pārskatītāju iestatīšana

Šajā piemērā ir parādīts, kā konfigurēt pirkšanas pieprasījuma izdevumu pārskatītāju. Lai konfigurētu citus izdevumu pārskatītāju tipus, nomainiet navigācijas ceļu 1. darbībā ar atbilstošu ceļu no tabulas sadaļā [Izdevumu pārskatītāju tipi](configure-expenditure-reviewers.md#types-of-expenditure-reviewers), iepriekš šajā tēmā.

1. Dodieties uz **Sagāde un ieguve \> Iestatījums \> Politikas \> Pirkšanas pieprasījuma izdevumu pārskatītāji**.
2. Lapā **Pirkšanas pieprasījumu izdevumu pārskatītāji** atlasiet **Jauns**.
3. Laukā **Nosaukums** ievadiet izdevumu recenzenta konfigurācijas nosaukumu, piemēram, **izmaksu centrs**.
4. Kopsavilkuma cilnē **Juridiskās personas izdevumu pārskatītāji** atlasiet konfigurējamu juridisko personu.
5. Projektu sadalei katrai projekta iestādei atzīmējiet izvēles rūtiņu un atlasiet **Jā** katrai finanšu dimensijai, ko vēlaties iespējot. 
6. Organizācijas sadalei cilnē **Organizācijas sadales** katrai finanšu dimensijai, ko vēlaties iespējot, atlasiet **Jā**.
7. Atkārtojiet 4.-6. darbību katrai papildu juridiskai personai.

## <a name="assign-owners-to-financial-dimensions"></a>Piešķirt īpašniekus finanšu dimensijām

Lai finanšu dimensijai piešķirtu īpašnieku, izpildiet tālāk aprakstītās darbības.

1. Pārejiet uz sadaļu **Virsgrāmata \> Kontu plāns \> Dimensijas \> Finanšu dimensijas**.
2. Sarakstā izvēlieties finanšu dimensiju, kam piešķirt īpašniekus.
3. Atlasīt **Dimensiju vērtības**.
4. Atlasiet **Labot**, lai veiktu izmaiņas dimensiju vērtībās.
5. Sarakstā izvēlieties dimensijas vērtību, kam piešķirt īpašnieku.
6. Laukā **Īpašnieks** atlasiet darbinieku, kuram piešķirt šo dimensijas vērtību.

## <a name="configure-project-distributions"></a>Konfigurēt projekta sadales

Lai projekta iestādes piešķirtu noteiktam projektam, rīkojieties šādi.

1. Dodieties uz **Projektu vadība un uzskaite \> Projekti \> Visi projekti**.
2. Atlasiet projektu, kuram jāpiešķir iestādes.
3. Atlasiet **Labot**, lai veiktu izmaiņas projektā.
4. Kopsavilkuma cilnē **Vispārīgi** sadaļā **Atbildīgais** pēc vajadzības atlasiet darbinieku laukiem **Pārdošanas pārvaldnieks**, **Projekta vadītājs** un **Projekta kontrolleris**.
5. Kopsavilkuma cilnē **Finanšu dimensijas** atlasiet projektam nepieciešamās finanšu dimensijas.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Izdevumu pārskatītāju nozīmēšana darbplūsmas uzdevumam

Šis piemērs parāda, kā konfigurēt pirkšanas pieprasījuma darbplūsmu tā, lai tā izmanto pirkšanas pieprasījuma izdevumu pārskatītāju. Lai konfigurētu citus darbplūsmu tipus, darbplūsmas lapa, kas jāatver 1. darbībā, var būt modulī **Izdevumu pārvaldība** vai **Kreditoru parādi** moduļa **Sagādes un avotu** vietā.

Lai piešķirtu pirkšanas pieprasījuma izdevumu pārskatītājus darbplūsmas uzdevumu, izpildiet šīs darbības.

1. Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu darbplūsmas**.
2. Veiciet dubultklikšķi uz esošas darbplūsmas vai izveidojiet jaunu darbplūsmu.
3. Darbplūsmas redaktorā rūtī **Darbplūsma** atlasiet uzdevumu, kam piešķirt izdevumu pārskatītāja konfigurāciju. Pēc tam sadaļā **Transakciju rūts**, grupā **Rādīt** atlasiet **Rekvizīti**.
4. Lapas **Rekvizīti** kreisajā rūtī atlasiet **Piešķire**.
5. Cilnē **Piešķires tips** atlasiet **Dalībnieks**.
6. Cilnē **Uz lomas balstīts** laukā **Dalībnieka tips** atlasiet **Izdevumu dalībnieki**. Pēc tam laukā **Dalībnieks** atlasiet izdevumu pārskatītāju konfigurāciju, lai izmantot to šim darbplūsmas uzdevumam.
