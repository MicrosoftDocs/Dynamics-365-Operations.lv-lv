---
title: Izmantot partijas atgriešanas kodus, lai atzīmētu partijas kā pieejamas vai nav pieejamas
description: Šajā rakstā ir aprakstīts, kā iestatīt un izmantot partijas atgriešanas kodus, lai atzīmētu partijas kā pieejamas vai nav pieejamas izmantošanai vispārējā plānošanā, rezervācijā, izdošanā un/vai nosūtīšanā.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542908"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Izmantot partijas atgriešanas kodus, lai atzīmētu partijas kā pieejamas vai nav pieejamas

Šajā rakstā ir aprakstīts, kā iestatīt un izmantot *partijas atgriešanas kodus*. Katra partijas atgriešanas metodes koda statuss ir Pieejams *vai* *Nav pieejams*. Piešķiriet partijas atgriešanas kodus krājumu partijām, lai norādītu, vai katra partija ir pieejama vispārējai plānošanai, rezervācijai, izdošanai un/vai nosūtīšanai.

Lai lietotu partijas atgriešanas kodus, iestatiet kodus un piešķiriet tos partijām, kuras vēlaties pārvaldīt.

## <a name="set-up-batch-disposition-codes"></a>Iestatīt partijas atgriešanas kodus

Jums jāiestata katru partijas atgriešanas kodu, ko vēlaties izmantot savā sistēmā. Varat izveidot tik daudz kodu, cik vēlaties. (Piemēram, var izveidot kodus, lai identificētu dažādus iemeslus, kādēļ pakete var būt pieejama vai nav pieejama). Tomēr bieži vien ir tikai divi kodi: viens pieejams *un viens — nepieejams* *.* Varat arī izveidot pielāgotus kodus, kas ļauj paketi izmantot dažām operācijām, bet ne citiem.

Sekojiet šiem soļiem, lai iestatītu partijas atgriešanas kodus.

1. Dodieties uz **krājumu pārvaldības iestatījuma \>\> partijas \> atgriešanas šablonu**.
1. Lapā **Partijas atgriešanas šablons** ir uzskaitīti jūsu pašreizējie partijas atgriešanas kodi un tie ļauj tos izveidot, dzēst un rediģēt. Izpildiet kādu no šīm darbībām:

    - Lai rediģētu esošo kodu, atlasiet to saraksta rūtī.
    - Lai izveidotu jaunu kodu, **darbību rūtī** atlasiet Jauns.

1. Iestatiet sekojošos laukus jaunā vai atlasītā koda galvenē:

    - **Partijas atgriešanas kods** - Ievadiet parādāmo koda nosaukumu.
    - **Apraksts** – aprakstiet, kā kods jāizmanto.
    - **Partijas atgriešanas statuss** – atlasiet statusu, kas attiecas uz partijām, kurām ir piešķirts kods:

        - *Nav pieejams* — partijas nevar izmantot vispārējai plānošanai, rezervēšanai, izdošanai vai nosūtīšanai. Atlasot šo vērtību, visas **·** **Kopsavilkuma** cilnē Iestatījumi lietojumprogrammas bloķēt opcijas *tiek* iestatītas uz Jā, un visas **Opcijas Nettable** tiek iestatītas uz *Nē.* Tomēr dažus no šiem iestatījumiem var mainīt, lai pievienotu izņēmumus.
        - *Pieejams* – partijas var izmantot vispārējai plānošanai, rezervēšanai, izdošanai un/vai nosūtīšanai. Kad atlasāt šo vērtību, visas **·** **·** *Opcijas Bloķēt kopsavilkuma cilnē Iestatījumi tiek iestatītas uz Nē*, un visas **Nettable opcijas** tiek iestatītas uz *Jā.* Šie iestatījumi būs tikai nolasāmi, kamēr **partijas atgriešanas statusa** lauks būs iestatīts uz *Pieejams*.

1. Ja partijas **atgriešanas statusa lauks tiek iestatīts uz Nav pieejams, varat pielāgot katras operācijas (rezervē, izdošanas un nosūtīšanas) bloķēšanas** *statusu* katram pasūtījuma tipam (pārdošana, pārsūtīšana un ražošana). Ražošanas pasūtījumiem var izvēlēties bloķēt vai atbloķēt ražošanas izdošanas žurnālu. Var arī bloķēt vai atbloķēt vispārējo plānošanu. Izmantojiet opcijas kopsavilkuma cilnē Iestatījumi **, lai** bloķētu vai atbloķētu katru operāciju pēc jūsu pieprasītās. Iestatiet Opciju **Nettable uz** Jā, lai iespējotu *vispārējo plānošanu, vai iestatiet to* uz Nē *, lai bloķētu* vispārējo plānošanu.

## <a name="assign-batch-disposition-codes-to-batches"></a>Piešķirt partijas atgriešanas kodus partijām

Pēc tam, kad jūs definējiet partijas atgriešanas kodus, kas nepieciešami, sekojiet šiem soļiem, lai piešķirtu tos partijām.

1. Pārejiet uz **noliktavas pārvaldības \> iestatījuma \> krājumu \> partijām**.
1. Atlasiet vienu vai vairākas partijas, kam piešķirt partijas atgriešanas kodu.
1. Darbību rūts cilnē Atiestatīt atlasiet **Atiestatīt** partijas **atgriešanas kodu**.
1. Dialoglodziņā Mainīt **ierobežojumus krājumu** partijas dialoglodziņā iestatiet lauka Jauna partijas atgriešanas kods **nosaukumu uz kodu,** kuru vēlaties piešķirt.
1. Atlasiet **Labi,** lai lietotu jauno iestatījumu un saglabātu izmaiņas.

    **Lapā Partijas tiek** atjauninātas partijas atgriešanas koda un partijas atgriešanas **statusa** kolonnas, **lai tās atspoguļotu jaunos** iestatījumus atlasītajām partijām.

## <a name="master-planning-example"></a>Vispārējās plānošanas piemērs

Šajā piemērā parādīts, kā partijas atgriešanas kodi var ietekmēt vispārējo plānošanu.

Šajā piemērā partijas atgriešanas kodi tiek iestatīti sekojošos gadījumos:

- *Pieejams P:*

    - **Partijas atgriešanas statuss: pieejams** *·*
    - **Nettable:** *Jā*

- *P nav pieejams:*

    - **Partijas atgriešanas statuss:** *nav pieejams*
    - **Neto tabula:** *Nr.*

Ir prece (Product-1 *), kam* ir divas partijas: *partija-A* un *partija-B*. Šīs partijas ir iestatītas šādā veidā:

- *Pakete - A:*

    - **Partijas atgriešanas metodes kods:** *P-Pieejams*
    - **Rīcībā esošo krājumu daudzums:** 1

- *Partija-B:*

    - **Partijas atgriešanas metodes kods:** *P nav pieejams*
    - **Rīcībā esošo krājumu daudzums:** 1

Pastāv pārdošanas pasūtījums (*SO1*) ar daudzumu 2 precei-1 *·*. Piegādes datums ir trīs dienas no šodienas.

Palaiž vispārējo plānošanu un iestata šādas vērtības, kas attiecas uz šo piemēru:

- **Plānotais pasūtījums: pirkšanas** *pasūtījums*
- **Papildināšanas stratēģija:** *prasība*
- **Izpildes laiks:** *0*

Plānošanas palaišanas rezultātā sistēma izmanto pieejamo partiju (pakete-A), lai pārdošanas pasūtījumam SO1 nosegtu 1 *. preci-1* *·*.*·* Tomēr to nevar izmantot partijai B *, jo* šī partija ir atzīmēta kā pieejama plānošanai. Tāpēc, lai nosegtu atlikušo daudzumu, sistēma izveido plānoto pirkšanas pasūtījumu (*PPO1*) jaunai preces Product-1 *partijai*.

Šajā ilustrācijā parādīta plānošanas rezultāta laika skala.

![Piemērs, kas parāda, kā partijas atgriešanas kodi var ietekmēt vispārējo plānošanu.](media/batch-codes-planning-example.png "Piemērs, kas parāda, kā partijas atgriešanas kodi var ietekmēt vispārējo plānošanu")
