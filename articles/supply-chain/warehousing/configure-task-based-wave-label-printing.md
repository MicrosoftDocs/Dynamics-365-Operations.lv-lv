---
title: Plānot kopuma etiķešu drukāšanu kopuma laikā
description: Šajā tēmā ir aprakstīts, kā iestatīt un izmantot funkcionalitāti uz uzdevumu balstītai kopuma etiķešu drukāšanai.
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 4883f8a548645436e17b933d87d4ee6330570d48
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777869"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Plānot kopuma etiķešu drukāšanu kopuma laikā

[!include [banner](../../includes/banner.md)]

Izmantojiet līdzekli *Uz uzdevumu balstītas kopuma etiķetes drukāšana* kā daļu no jūsu kopuma procesa, lai palīdzētu uzlabot efektivitāti, un lai sistēma izveidotu kopuma etiķetes un strādātu atsevišķos uzdevumos.

Kopuma etiķešu drukāšanas konfigurācijas process ir sarežģīts, un tas balstās uz precīzu konfigurāciju un pamatdatiem. Nereti kopuma etiķešu ierakstu ģenerēšana neizdodas, un, kad tas notiek, visa kopuma apstrāde tiek atgriezta atpakaļ. Līdzeklis *Uz uzdevumiem balstīta kopuma etiķetes drukāšana* palīdz izvairīties no atkārtotas darba un darba rindu izveides katru reizi, kad tiek nepareizi drukāta kopuma etiķete.

Izmantojot līdzekli *Uz uzdevumiem balstīta kopuma etiķetes drukāšana*, sistēma vispirms izveido darbu un darba rindas. Pēc tam tā izveido un drukā kopuma etiķetes. Visbeidzot, ja kopuma etiķetes ir pareizi izveidotas, tā izdod darbu un kopumu izdošanai.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Līdzekļa pārvaldībā ieslēdziet līdzekli Uz uzdevumiem balstīta kopuma etiķetes drukāšana

Lai izmantotu šajā tēmā aprakstītos līdzekļus, tie sistēmai ir jāieslēdz. Izmantojiet [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lai iespējotu līdzekļus šādā secībā:

1. *Kopuma etiķešu drukāšana* — šis līdzeklis ir nepieciešams, lai kopuma etiķešu drukāšanai iespējotu kopuma apstrādes metodi.
1. *Organizācijas darba bloķēšana* - šis līdzeklis ir nepieciešams gan manuālai, gan automātiskai ieplānotā darba izveidošanai. (No Piegādes ķēdes pārvaldības versijas 10.0.21, šī funkcija ir obligāta, tāpēc tā ir ieslēgta pēc noklusējuma un to nevar atkal izslēgt.)
1. *Uz uzdevumiem balstīta kopuma etiķetes drukāšana* — šis līdzeklis ir nepieciešams, lai sadalītu kopuma etiķetes drukāšanu ar atsevišķu darbības jomu.

## <a name="manually-enable-the-new-wave-step-method"></a>Manuāli iespējot jauno kopuma darbības metodi

Vispirms izveidojiet jaunu kopuma darbības metodi un iespējojiet to paralēlā, asinhronā uzdevuma apstrādē.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Darbību rūtī atlasiet **Atkārtoti ģenerēt metodi**. Ievērojiet, ka *waveLabelPrinting* ir pievienots kopuma procesa metožu sarakstam, ko varat izmantot nosūtīšanas kopuma veidnēs.
1. Atlasiet ierakstu, kur lauks **Metodes nosaukums** ir iestatīts uz *waveLabelPrinting*, un pēc tam Darbību rūtī atlasiet **Uzdevuma konfigurācija**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Noliktava** – izvēlieties noliktavu, ko izmantosiet darba izveides apstrādes plānošanai. (Ja testēšanas nolūkos izmantojat demonstrācijas datus, varat atlasīt noliktavu *24*.)
    - **Maksimālais pakešuzdevumu skaits** – norādiet maksimālo pakešuzdevumu skaitu. Vairumā gadījumu vērtībai ir jābūt no *8* līdz *16*. Tomēr mēs iesakām eksperimentēt, lai atrastu optimālu iestatījumu saviem scenārijiem.
    - **Kopuma apstrādes partijas** grupa – atlasiet atvēlēto kopuma apstrādes partijas grupu, lai optimizētu partijas rindas apstrādi.

Tagad varat atjaunināt esošu kopuma veidni, lai tā izmanto kopuma apstrādes metodi *Kopuma etiķetes drukāšana*. Alternatīvi varat izveidot jaunu kopuma veidni, kas to izmanto.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Saraksta rūtī atlasiet kopuma veidni, kas jāatjauno. (Ja testēšanas nolūkos izmantojat demonstrācijas datus, varat atlasīt *24 Piegādes noklusējums*.)
1. Kopsavilkuma cilnē **Metodes** kolonnā **Atlikušās metodes**, atlasiet rindu, kur lauks **Nosaukums** ir iestatīts uz *waveLabelPrinting*.
1. Atlasiet **pievienot** (bultiņas pa labi pogu), lai pārvietotu atlasīto rindu uz kolonnu **Atlasītās metodes**.
1. Laukā **Kopuma darbības kods** ievadiet kopuma darbības kodu, kas tiks izmantots, lai savienotu kopuma veidni ar kopuma etiķetes veidni.

## <a name="set-wave-task-processing-threshold-data"></a>Iestatīt kopuma uzdevuma apstrādes sliekšņa datus

Pirmo reizi, kad tiek palaists kopuma process, izmantojot jebkuru uzdevumu apstrādi, sistēma izveido noklusējuma kopuma uzdevumu apstrādes sliekšņa datus. Šie dati tiek izmantoti, lai kontrolētu, vai kopuma apstrāde darbosies asinhroni un būs uz uzdevumiem balstīta, lai tā paralēli varētu apstrādāt un radīt kopuma etiķetes.

Noklusējuma dati sākotnēji izmanto *1* sliekšņa vērtību minimālajam darba ID skaitam (`MinimumWorkThresholdForLabelPrinting`). Tādēļ, kad sistēma apstrādā kopumu, kam ir vairāk nekā viens darba ID, atsevišķā transakcija tiks izmantota kopuma etiķešu apstrāde, pamatojoties uz uzdevumu. Šos datus var manuāli ievietot vai atjaunināt `WHSWaveTaskProcessingThresholdParameters` tabulā testēšanas vidēs. Lai mainītu šis iestatījums ražošanas vidē, jums ir jāsazinās ar Microsoft Support, lai pieprasītu atjauninājumu.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Izmaiņas kopuma apstrādes loģikā, kad tiek izmantota uz uzdevumu balstīta kopuma etiķetes drukāšana

Ja kopuma etiķetes apstrāde pārsniedz kopuma uzdevuma apstrādes slieksni, tiek sākta uz uzdevumu balstīta apstrāde. Nākamajā kopuma apstrādē, kas atbilst kopuma veidnei, kopuma etiķešu drukāšana tiks palaista savrupā *ttsbegin*/*ttscommit* transakcijā tūlīt pēc darba izveides. Ja kopuma veidnē darba izlaišana (atbloķēšana) ir konfigurēta automātiskai palaišanai, tas notiek tikai pēc kopuma etiķešu drukāšanas procesa veiksmīgas pabeigšanas.

Ja kopuma etiķešu ģenerēšana neizdodas (piemēram, ja darba daudzums tiek pārvērsts neveiksmīgā kopuma etiķetes daudzumā un rodas kļūda), neizdodas tikai atbilstošā transakcija. Iepriekš izveidotais darbs paliek iesaldēts. Lai labotu kļūdas un drukātu kopuma etiķetes, izpildiet šīs darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Režģī atlasiet atbilstošo kopumu.
1. Darbību rūts cilnē **Kopums**, grupā **Drukāt** atlasiet **Kopuma etiķetes**.
1. Lai nosūtītu etiķetes drukāšanai, izpildiet ekrānā redzamos norādījumus.
1. Darbību rūts cilnes **Kopums** grupā **Kopums** atlasiet **Izlaist**, lai manuāli izlaistu darbu atlasītajam kopumam.

## <a name="additional-resources"></a>Papildu resursi

- [Kopuma etiķešu drukāšana](configure-wave-label-printing.md)
- [Darba izveides plānošana kopuma laikā](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
