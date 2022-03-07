---
title: Operāciju plānošanas opcijas
description: Šajā tēmā ir aprakstītas operāciju plānošanas opcijas. Operāciju plānošanu var lietot, lai sniegtu vispārēju ražošanas procesa novērtējumu laika periodam.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb0ee3020c5cfd17e82282e8fddb8f9c6dcdfee
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566747"
---
# <a name="operations-scheduling-options"></a>Operāciju plānošanas opcijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas operāciju plānošanas opcijas. Operāciju plānošanu var lietot, lai sniegtu vispārēju ražošanas procesa novērtējumu laika periodam.

Operāciju plānošana aprēķina šādu informāciju ražošanas pasūtījumam:

-   Ražošanas pasūtījumam un katrai operācijai tiek iestatīti sākuma un beigu datumi
-   Operācijām tiek piešķirti resursi.

To, kā tiek aprēķināti ražošanas grafiki, nosaka vairāki iestatījumi. Šos iestatījumus definējiet lapā **Operāciju plānošana**. Tālāk ir aprakstītas plānošanas opcijas.

## <a name="operations-scheduling"></a>Operāciju plānošana
### <a name="scheduling-direction"></a>Plānošanas virziens

Plānošanas virziens ir plānošanas procesa pamatā. Ražošanu var plānot uz priekšu un atpakaļ no jebkura datuma atkarībā no laika un plānošanas prasībām.

-   **Turpvērstā plānošana**— jūs varat plānot ražošanas sākšanu pēc iespējas agrāk. Ražošanu var sākt šodien, rīt vai noteiktā datumā nākotnē. Ražošanu tiek plānots sākt agrākajā iespējamā datumā, un tā tiek plānota uz priekšu līdz agrākajam iespējamajam beigu datumam.
-   **Atpakaļejošā plānošana** — jūs varat plānot ražošanas sākšanu pēc iespējas vēlāk. Grafiks tiek balstīts uz datumu, kad ražošana jāpabeidz un tiek skaitīts atpakaļ līdz pēdējam iespējamajam datumam, kad ražošanu var sākt un pabeigt noteiktajā beigu datumā.

Pieejamas šādas opcijas

-   **No šodienas uz priekšu** — plānojiet uz priekšu no pašreizējā datuma. (Pašreizējais datums ir sistēmas datums.)
-   **Uz priekšu no plānotā sākuma** — plānojiet uz priekšu no agrākā sākuma datuma. Ja nepastāv iepriekšēja plānošana, tad plānošanas virziens ir uz priekšu no pašreizējā datuma.
-   **No plānošanas datuma uz priekšu** — plānojiet uz priekšu no datuma, kas norādīts laukā **Plānošanas datums**. Ja nenorādīsit plānošanas datumu, tad plānošanas virziens ir uz priekšu no pašreizējā datuma.
-   **Atpakaļ no piegādes datuma** — plānojiet atpakaļ no ražošanas pasūtījumam norādītā piegādes datuma. Ja esat atlasījis šo opciju, bet piegādes datums nav norādīts, piegādes datums ir pašreizējais datums.
-   **Atpakaļ no plānotā beigu datuma** — plānojiet no iepriekš aprēķinātā beigu datuma atpakaļ. Ja nav iepriekšējās plānošanas, beigu datums ir pašreizējais datums.
-   **No plānošanas datuma atpakaļ** — plānojiet atpakaļ no datuma, kas norādīts laukā **Plānošanas datums**. Ja nenorādīsit plānošanas datumu, tad tiek izmantots pašreizējais datums. Periods atpakaļ no plānošanas datuma ražošanas pasūtījumam tiek aprēķināts pēdējoreiz, kad vajadzība tika aprēķināta. Ja ražošanas pasūtījumam nav norādīts datums, tiek izmantots pašreizējais sistēmas datums.
-   **Atpakaļ no aizkavēšanās datuma** — plānojiet atpakaļ no aizkavēšanās datuma, kas aprēķināts ražošanas pasūtījumam pēdējoreiz, kad vajadzība tika aprēķināta. Ja ražošanas pasūtījumam nav norādīts aizkavēšanās datums, tiek izmantots pašreizējais sistēmas datums.
-   **Tāpat kā pēdējā plānošanā** — attiecībā uz operāciju plānošanu un darbu plānošanu, atlasītais plānošanas virziens un datums tiek saglabāti. Tādējādi šo opciju var atlasīt turpmākajām plānošanām. Ja ražošanas pasūtījumam nav iepriekšējas plānošanas, plānošana notiek atpakaļejošā virzienā no pašreizējā sistēmas datuma.
-   **No rītdienas uz priekšu** — plānojiet no pašreizējā datuma plus viena diena uz priekšu.
-   **Uz priekšu no iepriekšējā darba** — šī opcija ir būtiska tikai darbu plānošanā. Ja operāciju plānošanai atlasa šo plānošanas virzienu, ražošanas pasūtījums tiek plānots no pašreizējā datuma uz priekšu. Darbu plānošanā plānošana ir izveidota vienam darbam, un visi pārējie ražošanas darbi tiek plānoti, pamatojoties uz šo darbu.
-   **Atpakaļ no iepriekšējā darba** — šī opcija ir būtiska tikai darbu plānošanā. Atlasot šo plānošanas virzienu operāciju plānošanai, plānotie pasūtījumi tiek plānoti atpakaļ no pašreizējā datuma. Darbu plānošanā plānošana ir izveidota vienam darbam, un visi pārējie ražošanas darbi tiek plānoti, pamatojoties uz šo darbu.

### <a name="scheduling-date"></a>Plānošanas datums

Plānošanas virzieniem **No plānošanas datuma uz priekšu** un **No plānošanas datuma atpakaļ** lietotais datums. Plānošana tiek veikta atpakaļ vai uz priekšu no šī datuma. Plašāku informāciju skatiet iepriekšējā sadaļā “Plānošanas virziens”.

### <a name="recalculate-bom-levels"></a>Pārrēķināt MK līmeņus

Ja atlasāt **Pārrēķināt MK līmeņus**, atlasītie materiālu komplektu (MK) līmeņi tiks pārrēķināti, lai palīdzētu nodrošināt pareizu plānošanas secību.

## <a name="limitations"></a>Ierobežojumi
### <a name="finite-capacity"></a>Ierobežota noslodze

Plānošana ir atkarīga no tādu resursu pieejamības, kas nepieciešami, lai pabeigtu ražošanu. Ja noslodze ir nepietiekama, ražošanas pasūtījumi var aizkavēties vai pat tikt apturēti. Ja operāciju plānošanai tiek lietota ierobežota noslodze, tiek ņemtas vērā esošās noslodzes rezervācijas, kas veiktas attiecīgajiem resursiem, un šī noslodze tiek rādīta kā nepieejama. Ražošanas pasūtījums tiek plānots, pamatojoties uz nepieciešamo resursu noslodzes pieejamību. Operāciju plānošanai tiek izmantota norādītā operāciju secība, lai noteiktu operāciju secību ražošanas maršrutā. Operāciju plānošana rezervē noslodzi resursu grupās, pamatojoties uz darbības laikiem, kas definēti ražošanas maršrutā. Resursu grupu noslodze ir tādu noslodžu summa, kuras ir pieejamas visiem resursiem attiecīgajās resursu grupās.

### <a name="finite-material"></a>Ierobežots materiāls

Plānošana ir atkarīga arī no ražošanai nepieciešamo materiālu pieejamības. Nepietiekama sastāvdaļu pieejamība var izraisīt arī ražošanas aizturi. Plānošanu var balstīt arī uz materiālu izmantošanu. Vienkārši norādiet materiālus, kuriem jābūt pieejamiem ražošanā, nevis materiālus, kas nav kritiski. Šāda veida plānošana tiek dēvēta arī par plānošanu ar ierobežotu materiālu. Norādot ierobežotus materiālus, ražošana tiek plānota, pamatojoties uz to, vai materiāli ir pieejami. **Piezīme.** Optimizējot pēc noslodzes un materiāliem, ražošana tiek aprēķināta atbilstīgi abiem ierobežojumiem. Tiek ņemta vērā noslodzes un materiālu pieejamība, un ražošanas pasūtījuma operāciju sākumu nevar plānot, kamēr noslodze un materiāli nav pieejami tajā pašā laikā un nepieciešamajā daudzumā. Atzīmējiet šo izvēles rūtiņu, ja plānošanas laikā materiāli jāuzskata par ierobežotiem. Ja materiālu daudzums ir ierobežots, tiks apsvērta materiālu pietiekamība šim laikam. Citiem vārdiem sakot, plānošanā tiek apsvērti turpmākie datumi, kas tiek aprēķināti krājumiem. Plānošana rezervē izejvielas un izvērš pašreizējo ražošanas uzdevumu. Ja plānošana notiek vairākas reizes, tikai pirmā plānošana palaiž izvēršanu un veic rezervēšanas. Ja jūs izdarāt izmaiņas ražošanas MK vai maršrutā, tad nākošā plānošana palaiž izvēršanu. Attiecībā uz izvēršanu tiek pieņemts, ka materiāli ir nepieciešami tajā pašā dienā. Tā kā ražošana nav plānota vispārējā grafika plānošanas laikā, pašreizējais datums tiek izmantots kā labākais novērtējums, kad krājumi būs pieejami. Izvēršana tad pārbauda, vai krājumi ir pieejami. Ja krājumi ir pieejami, ražošanas vajadzību var izpildīt. Ja krājumi līdz pašreizējam datumam nav pieejami, tiek ģenerēts plānotais pasūtījums un tam tiek veikta korespondējošā atlase. Ja plānotajam pasūtījumam ir iestatīta automātiskā apstiprināšana, plānotais pasūtījums pirkšanai vai ražošanai tiek apstiprināts automātiski. Ražošanas statuss tiek automātiski nomainīts uz dialoglodziņa **Vajadzības grupas** laukā **Pieprasītais ražošanas statuss** norādīto statusu. Ja izvēles rūtiņa ir notīrīta, materiāli vienmēr tiek uzskatīti par pieejamiem. Līdz ar to plānošana neņem vērā, vai materiāli būs pieejami pieprasījuma laikā.

### <a name="finite-property"></a>Ierobežoti rekvizīti

Atzīmējiet šo izvēles rūtiņu, ja darbu plānošanā ir jāiekļauj resursu rekvizīti.

### <a name="keep-production-unit"></a>Paturēt ražošanas vienību

Atlasiet, vai plānošanas programmai ir jāieplāno tikai resursi, kuri jau ir norādīti ražošanas vienībai.

### <a name="keep-warehouse-from-resource"></a>Glabāt noliktavā no resursa

Atlasiet, vai plānošanas programmai ir jāieplāno tikai resursi, kuri ir saistīti ar ievades noliktavu, kas norādīta resursam.

## <a name="references"></a>Atsauces
### <a name="schedule-references"></a>Plānot atsauces

Ja atsauces ir atkarīgas no ražošanas pasūtījumiem, tās tiek dēvētas arī par apakšražošanas uzdevumiem. Apakšražošanas uzdevumus var ieplānot ražošanas pasūtījuma plānošanas ietvaros. Atzīmējiet šo izvēles rūtiņu, ja apakšražošanas uzdevumu plānošanas pamatā jābūt galvenās ražošanas plānošanai. Kas attiecas uz galveno ražošanu, pārklājušies ražošanas uzdevumi tiek plānoti uz priekšu un pamatā esošie ražošanas uzdevumi tiek plānoti atpakaļ. Ražošanas pasūtījumu atsauces varat apskatīt lapas **Ražošanas pasūtījumi** laukā **Atsauces līmenis**.

### <a name="synchronize-references"></a>Sinhronizēt atsauces

Atsauces var sinhronizēt ar ražošanas pasūtījumu. Ja izvēlēta šī opcija, apakšražošanas tiek pārvietotas un saskaņotas, tiklīdz ražošanas pasūtījuma plānā tiek izdarītas izmaiņas. Ja ražošanas pasūtījumam ir viens vai vairāki apakšražošanas uzdevumi, varat plānot apakšražošanas uzdevumus kopā ar galveno ražošanu. Šādā gadījumā galveno ražošanu nevar sākt, kamēr nav pabeigti saistītie apakšražošanas uzdevumi. Tādējādi atzīmējiet šo izvēles rūtiņu, ja apakšražošanas uzdevumu plānošanas pamatā jābūt atlasītās ražošanas sākuma un beigu laikam. Šo izvēles rūtiņu var atzīmēt tikai tad, ja izvēles rūtiņa **Plānot atsauces** arī ir atzīmēta.

## <a name="cancellation"></a>Atcelšana
### <a name="cancel-queue-time"></a>Atcelt gaidīšanas laiku

Atzīmējiet šo izvēles rūtiņu, lai plānošanā neiekļautu gaidīšanas laiku.

### <a name="cancel-setup"></a>Atcelt iestatījumus

Atzīmējiet šo izvēles rūtiņu, lai plānošanā neiekļautu uzstādīšanas laiku.

### <a name="cancel-process"></a>Atcelt procesu

Atzīmējiet šo izvēles rūtiņu, lai plānošanā neiekļautu izpildes laiku.

### <a name="cancel-overlap"></a>Atcelt pārklāšanos

Atzīmējiet šo izvēles rūtiņu, lai plānošanā neiekļautu pārklāšanās laiku.

### <a name="cancel-transport"></a>Atcelt transportēšanu

Atzīmējiet šo izvēles rūtiņu, lai plānošanā neiekļautu tranzīta laiku.

## <a name="set-default"></a>Iestatīt noklusējumu
Pašreizējās vērtības var saglabāt kā noklusējuma vērtības. Ir divas opcijas:

-   Iestatīt kā manu noklusējumu
-   Iestatīt kā noklusējumu visiem


## <a name="additional-resources"></a>Papildu resursi

[Operāciju plānošana](operations-scheduling.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]