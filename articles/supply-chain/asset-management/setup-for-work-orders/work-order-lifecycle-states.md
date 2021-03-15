---
title: Darba pasūtījumu dzīves ciklu stāvokļi
description: Šajā tēmā ir paskaidroti darba pasūtījuma dzīves cikla stāvokļi līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2a8052942ff97c9e8033d5915723e82c42f964c8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021583"
---
# <a name="work-order-lifecycle-states"></a>Darba pasūtījumu dzīves ciklu stāvokļi


[!include [banner](../../includes/banner.md)]

 

Darba pasūtījuma dzīves cikla stāvokļi definē stāvokļus, kurus darba pasūtījums var iziet. Piemēri ietver tādus stāvokļus kā **Izveidots**, **Ieplānots**, **Notiek izpilde** un **Pabeigts**. Darba pasūtījuma dzīves cikla stāvokļus var manuāli atjaunināt darba pasūtījumā, kā arī tie var tikt atjaunināti automātiski (piemēram, darba pasūtījuma plānošanas laikā).

Darba pasūtījuma dzīves cikla stāvokļi, kas nepieciešami jūsu darba pasūtījumiem, ir jāpievieno atbilstošajiem projekta posmiem lapā **Projekta pārvaldības un uzskaites parametri** (**Projekta pārvaldība un uzskaite** \> **Projekta pārvaldības un uzskaites parametri**). Vispirms jūs iestatāt projekta posmus lapā Projektu pārvaldība un uzskaite. Pēc tam līdzekļu pārvaldībā jūs iestatāt darba pasūtījuma dzīves cikla stāvokļus un darba pasūtījuma dzīves cikla modeļus.

Tālāk esošajā tabulā ir aprakstītas opcijas, kas atrodas sadaļās **Darba pasūtījums** un **Grafiks**, kopsavilkuma cilnē **Vispārīgi**, lapā **Darba pasūtījuma dzīves cikla stāvoklis** (**Līdzekļa pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Dzīves cikla stāvokļi**).

![Darba pasūtījumu dzīves ciklu stāvokļu lapa](media/09-setup-for-work-orders.png)

| Opcijas nosaukums                   | Apraksts |
|-------------------------------|-------------|
| Aktīvie                        | Iestatiet šo opciju uz **Jā**, ja darba pasūtījumam jābūt aktīvam, kamēr tas ir šajā dzīves cikla stāvoklī. |
| Pievienot rindu                      | Iestatiet šo opciju uz **Jā**, ja darba pasūtījumam var pievienot darba pasūtījuma uzdevumus, kas ir šajā dzīves cikla stāvoklī. |
| Dzēst                        | Iestatiet šo opciju uz **Jā**, ja darba pasūtījumu var dzēst, kamēr tas ir šajā dzīves cikla stāvoklī. |
| Dzēst rindu                   | Iestatiet šo opciju uz **Jā**, ja no darba pasūtījuma var dzēst darba pasūtījuma uzdevumus, kas ir šajā dzīves cikla stāvoklī. |
| Atļaut plānošanu              | Iestatiet šo opciju uz **Jā**, ja darba pasūtījumu var ieplānot, kamēr tas ir šajā dzīves cikla stāvoklī. |
| Iestatīt faktisko sākumu              | Iestatiet šo opciju uz **Jā**, ja lietotājam ir nepieciešams piedāvāt atlasīt faktisko darba pasūtījuma sākuma datumu un laiku, kad tas ir atjaunināts šajā dzīves cikla stāvoklī. |
| Iestatīt faktiskās beigas                | Iestatiet šo opciju uz **Jā**, ja lietotājam ir nepieciešams piedāvāt atlasīt faktisko darba pasūtījuma beigu datumu un laiku, kad tas ir atjaunināts šajā dzīves cikla stāvoklī. |
| Grāmatot žurnālus                 | Iestatiet šo opciju uz **Jā**, ja ir nepieciešams automātiski publicēt darba pasūtījuma žurnālus, kad darba pasūtījums ir atjaunināts šajā dzīves cikla stāvoklī. Ja rodas kļūda žurnāla publicēšanas laikā, tiks parādīt ziņojums un darba pasūtījuma dzīves cikla stāvokļa atjauninājums tiks atcelts. Lai skatītu darba pasūtījuma žurnāla rindas, atlasiet **Līdzekļa pārvaldība** \> **Kopējs** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi**, **Aktīvie darba pasūtījumi** vai **Mani aktīvie darba pasūtījumi**, atlasiet darba pasūtījumu sarakstā un tad atlasiet **Žurnāli**. Šī automātiskās darba pasūtījuma žurnāla publicēšanas iestatīšana noteiktā dzīves cikla stāvoklī ir tāda pati kā, ja atlasāt **Publicēt žurnālus** lapā **Darba pasūtījuma žurnāli**.<p>**Piezīme.** Ja iestatāt šo opciju uz **Jā**, žurnāli tiek automātiski publicēti, ja nav iestatīta apstiprināšanas darbplūsma. Ja jūsu uzņēmums izmanto žurnāla apstiprinājuma iestatīšanu, kas ir konfigurēta lapā **Žurnāla apstiprinājums** (**Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Žurnāli** \> **Žurnāla apstiprinājums**), pārvaldniekam vai darbiniekam ir jāapstiprina un jāpublicē patēriņa reģistrācijas.</p> |
| Apstrādāt uzturēšanas kontrolsarakstu | Iestatiet šo opciju uz **Jā**, ja ir jāapstrādā visi uzturēšanas kontrolsaraksti, kad darba pasūtījums tiek atjaunināts šajā dzīves cikla stāvoklī. Šīs apstrādes ietvaros tiek iegrāmatotas visas skaitītāja reģistrācijas, kas veiktas apkopes kontrolsarakstā, un tiek novērtēts visu apkopes kontrolsarakstu rezultāts. Tiek novērtētas uzturēšanas kontrolsaraksta rindas, kuru rezultāti ir **Sekmīgi** un **Nesekmīgi**, un, ja kaut vienas rindas rezultāts ir nesekmīgs, viss uzturēšanas kontrolsaraksts līdzekļu pārvaldībā tiek atzīmēts kā **Nesekmīgs**. |
| Pabeigts                         | Iestatiet šo opciju uz **Jā**, ja darba pasūtījuma uzdevuma grafika statuss visiem darba pasūtījuma uzdevumiem, kas izveidoti darba pasūtījumā, automātiski ir jāatjaunina uz statusu **Gatavs**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli. |
| Sākšana                         | Iestatiet šo opciju uz **Jā**, ja darba pasūtījuma uzdevuma grafika statuss visiem darba pasūtījuma uzdevumiem, kas izveidoti darba pasūtījumā, automātiski ir jāatjaunina uz statusu **Sākts**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli. |
| Beigt                           | Iestatiet šo opciju uz **Jā**, ja darba pasūtījuma uzdevuma grafika statuss visiem darba pasūtījuma uzdevumiem, kas izveidoti darba pasūtījumā, automātiski ir jāatjaunina uz statusu **Pabeigts**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli. |
| Dzēst grafika rindas         | Iestatiet šo opciju uz **Jā**, ja plānošana visiem darba pasūtījuma uzdevumiem, kas izveidoti darba pasūtījumā, kas jau ir ieplānots, ir jādzēš, kad darba pasūtījums tiek atjaunināts šajā dzīves cikla stāvoklī. Citiem vārdiem, līdzekļa noslodzes rezervācijas, saistītais uzturēšanas speciālists un saistītie rīki tiks dzēsti. Piemēram, jūs iestatāt šo opciju uz **Jā** darba pasūtījuma dzīves cikla stāvoklī, kura nosaukums **Novērtēts**. Pēc tam, kad darba pasūtījums tiek atgriezts uz šo cikla stāvokli, jo ir nepieciešama pārplānošana, šajā darba pasūtījumā var dzēst plānošanu. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Projekta posmu un darba pasūtījuma dzīves cikla stāvokļu iestatīšana

1. Atlasiet **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.
2. Cilnē **Projekta posms** katram posmam, ko vēlaties izmantot, atzīmējiet izvēles rūtiņu pie katra projekta veida, kas nepieciešams darba pasūtījumiem. Projekta veidi nosaka noteikumus par atļautajiem finanšu uzdevumiem. Finanšu uzdevumu piemēri ietver prognozes izveidi, novērtējumu izveidi un sākuma bilanču izveidi.

    > [!IMPORTANT]
    > Ja projekta veidam nav atlasīts projekta posms, bet projekta posms tiek izmantots darba pasūtījuma dzīves cikla stāvoklī, darba pasūtījuma projekti netiks atjaunināti atbilstošā veidā.

3. Aizveriet veidlapu **Projektu pārvaldības un uzskaites parametri**.
4. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Dzīves cikla stāvokļi**.
5. Atlasiet **Jauns**, lai izveidotu jaunu darba pasūtījuma dzīves cikla stāvokli.
6. Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.
7. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnes **Detalizēta informācija** laukā **Dzīves cikla modeļi** ir parādīts to darba pasūtījumu dzīves cikla modeļu skaits, kuri izmanto dzīves cikla stāvokli.

8. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Darba pasūtījums** atlasiet funkcijas, kurām vajadzētu būt pieejamām šajā dzīves cikla stāvoklī, iestatot atbilstošās opcijas uz **Jā**. Opciju aprakstu skatiet šajā tēmā iepriekš esošajā tabulā.
9. Sadaļas **Projekts** laukā **Posms** atlasiet projekta posmu, kas ir saistīts ar šo dzīves cikla stāvokli.
10. Sadaļā **Projekts** iestatiet opciju **Slēgt darbības** uz **Jā** ja projekta darbības, kas saistītas ar katru darba pasūtījuma uzdevumu, ir nepieciešams automātiski slēgt, kad darba pasūtījums ir šajā dzīves cikla stāvoklī.

    > [!NOTE]
    > Lai atrastu projekta darbības numuru, kas ir saistīts ar darba pasūtījuma uzdevumu, atlasiet **Līdzekļu pārvaldība** \> **Kopējs** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi**, **Aktīvie darba pasūtījumi** vai **Mani aktīvie darba pasūtījumi**. Atveriet darba pasūtījumu un pēc tam atlasiet darba pasūtījuma uzdevumu. Darbības numurs ir redzams laukā **Darbības numurs**, kas atrodas sadaļā **Projekts** (cilnē **Vispārīgi**, kas atrodas kopsavilkuma cilnē **Detalizēta informācija par rindu**).

11. Sadaļā **Prognoze** iestatiet opcijas **Kopēt stundas prognozi**, **Kopēt krājuma prognozi** un/vai **Kopēt izdevumu prognozi** opciju uz **Jā**, ja darba pasūtījuma projekta prognozes ir nepieciešams automātiski kopēt darba pasūtījuma žurnālos, kad darba pasūtījums ir šajā dzīves cikla stāvoklī.
12. Sadaļā **Grafiks** iestatiet vienu no opcijām uz **Jā**, ja darba pasūtījuma grafika statuss ir jāatjaunina, kad darba pasūtījums ir šajā dzīves cikla stāvoklī. Opciju **Gatavs**, **Sākt**, **Pabeigt** un **Dzēst grafika rindas** aprakstus skatiet tabulā, kas atrodama iepriekš šajā tēmā.

    > [!NOTE]
    > Lai skatītu grafika rindas, kas ir saistītas ar darba pasūtījuma uzdevumiem, atlasiet **Līdzekļu pārvaldība** \> **Kopējs** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi**, **Aktīvie darba pasūtījumi** vai **Mani aktīvie darba pasūtījumi**. Atveriet darba pasūtījumu, kopsavilkuma cilnē **Darba pasūtījuma uzdevumi** atlasiet darba pasūtījuma uzdevumu un skatiet saistītu informāciju kopsavilkuma cilnē **Detalizēta informācija par cilni**. Laukā **Statuss**, kas atrodas cilnē **Grafiks**, redzams darba pasūtījuma uzdevuma statuss. Lauku **Statuss** var iestatīt uz šādām vērtībām: **Ieplānots**, **Gatavs**, **Sākts**, **Apturēts** un **Pabeigts**.

13. Sadaļas **Uzturēšanas pieprasījumi** laukā **Dzīves cikla stāvoklis** atlasiet uzturēšanas pieprasījuma dzīves cikla stāvokli, ar kuru ir jāatjaunina saistītie uzturēšanas pieprasījumi. Šis atjauninājums tiek veikts automātiski. To var darīt tikai tad, ja uzturēšanas pieprasījuma dzīves cikla modelis ir atlasīts uzturēšanas pieprasījuma dzīves cikla modelī, kas tiek izmantots uzturēšanas pieprasījumam.
14. Sadaļā **Līdzeklis** iestatiet opciju **Atjaunināt līdzekļa MK** uz **Jā**, ja visi krājumi, kas tiek izmantoti darba pasūtījumā, būtu automātiski jāatjaunina lapā **Līdzekļa MK**, kad darba pieprasījums tiek atjaunināts šajā dzīves cikla stāvoklī. Šis iestatījums var būt nozīmīgs, ja, piemēram, darba pasūtījuma dzīves cikla stāvoklis nosaka darba pasūtījumu kā pabeigtu vai beigušos.
15. Sadaļā **Darba pasūtījumu kopa** iestatiet opciju **Dzēst kopas atsauci** uz **Jā**, ja darba pasūtījumi, kas atrodas šajā dzīves cikla stāvoklī, automātiski jāizdzēš no darba pasūtījumu kopām.
16. Kopsavilkuma cilnē **Validēt** atlasiet validācijas veidus, kas jāaktivizē šajā dzīves cikla stāvoklī, iestatot atbilstošās opcijas uz **Jā**. Pēc tam laukā **Veids** katram atlasītajam pārbaudes veidam atlasiet ziņojuma veidu, kas jārāda, ja obligātie lauki, kas ir saistīti ar pārbaudes veidu, nav pārbaudīti. Ja atlasāt **Kļūda**, darba pasūtījuma dzīves cikla stāvokļa atjaunināšana tiek atcelta, līdz piesaistītais obligātais lauks ir atjaunināts darba pasūtījumā.

    - Opcijas **Dīkstāve uzturēšanas dēļ**, **Uzturēšanas kontrolsaraksts**, **Kļūmes simptoms**, **Kļūmes iemesls** un **Kļūmes novēršana** ir saistītas ar opcijām sadaļā **Obligāts**, kas atrodas lapā **Darba pasūtījuma veidi** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Darba pasūtījuma veidi**). Lai aktivizētu šīs pārbaudes, atbilstošās opcijas ir arī jāiestata uz **Jā** darba pasūtījuma veidā, kas tiek izmantots darba pasūtījumam.
    - Ja opcija **Uzturēšanas kontrolsaraksts** ir iestatīta uz **Jā**, kas attiecas uz dzīves cikla stāvokli, ar kuru tiek atjaunināts darba pasūtījums, pārbaude tiek veikta, lai pārbaudītu, vai uzturēšanas kontrolsaraksta rindas, kas atzīmētas kā **Obligātas**, ir reģistrētas kā **Atzīmēta** vai **Nav piemērojama**. Ja nav veikta neviena no šīm reģistrācijām obligātajās rindās, tiek parādīts informatīvs, kļūdas vai brīdinājuma ziņojums, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli.
    - Ja opcija **Fiksētās izmaksas** ir iestatīta uz **Jā**, dzīves cikla stāvoklī, ar kuru tiek atjaunināts darba pasūtījums, tiek aprēķināta kopējā fiksēto izmaksu summa (tas ir, izdevumu kopējā summa, ko juridiskā persona ir apņēmusies maksāt) katram darba pasūtījuma uzdevumam. Ziņojums tiek parādīts, ja fiksētā izmaksu summa ir lielāka par 0 (nulli). Jūs atlasāt izmaksu saistību veidus, kas ir iekļauti kopsavilkuma cilnē **Izmaksu saistības**, kas atrodas cilnē **Izmaksu kontrole** lapā **Projektu pārvaldības un uzskaites parametri** (**Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Projektu pārvaldības un uzskaites parametri**).
    - Ja opcija **Dīkstāve uzturēšanas dēļ** ir iestatīta uz **Jā**, kas attiecas uz dzīves cikla stāvokli, ar kuru tiek atjaunināts darba pasūtījums, uzturēšanas dīkstāves pārbaude tiek veikta ar darba pasūtījumu saistītajā līdzeklī. Ja uzturēšanas dīkstāves reģistrācija ir veikta, bet nav reģistrācija **Pabeigta**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli, tiek parādīts ziņojums.
    - Ja standarta projekta iestatīšana neietver visus posmus, kas nepieciešami līdzekļi pārvaldības iestatīšanai, varat iestatīt lietotāja definētus projekta posmus cilnē **Projekta posms** lapā **Projektu vadības un uzskaites parametri**. Tālāk esošajā attēlā redzama cilne **Projekta posms** lapā **Projektu vadības un uzskaites parametri**.

    ![Dažādu projekta tipu projekta posmus iestatīšanas lapa](media/10-setup-for-work-orders.png)

> [!NOTE]
> Ja dzīves cikla stāvoklis, uz kuru atjaunināt darba pasūtījumu, ir neaktīvs, žurnāli, kas ir saistīti ar darba pasūtījumu, bet vēl nav grāmatoti, tiek automātiski dzēsti. Tas palīdz nodrošināt neizmantoto datu automātisku tīrīšanu. (Dzīves cikla stāvoklis ir neaktīvs, ja opcija **Aktīvs** tam ir iestatīta uz **Nē** kopsavilkuma cilnē **Vispārīgi**, kas atrodas lapā **Darba pasūtījuma dzīves cikla stāvoklis**.)
>
> Tomēr, ja jūs manuāli iestatāt darba pasūtījumu tā, lai tas nebūtu aktīvs, žurnāli, kas ir saistīti ar darba pasūtījumu, bet vēl nav publicēti, **netiek** automātiski dzēsti. (Lai manuāli padarītu darba pasūtījumu neaktīvu, atlasiet **Līdzekļu pārvaldība** \> **Kopējs** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**. Atveriet darba pasūtījumu un pārslēdzieties uz skatu **Virsraksts**. Kopsavilkuma cilnē **Vispārīgi** atlasiet **Rediģēt** un tad iestatiet opciju **Aktīvs** uz **Nē**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Relācijas starp darba pasūtījuma dzīves cikla modeļiem, darba pasūtījuma veidiem un darba pasūtījuma dzīves cikla stāvokļiem

Dzīves cikla modeļi attiecas uz darbplūsmām, un dzīves cikla stāvokļi tiek atlasīti dzīves cikla modelī secīgā kārtībā. Dzīves cikla modeļi ir iestatīti darba pasūtījuma veidos. Darba pasūtījuma veidi nosaka darbplūsmu un darbplūsmu lielumu vai apjomu. Piemēram, **Uzturēšana**, kas ir standarta darba pasūtījuma veids, var būt saistīta ar darba pasūtījuma dzīves cikla modeli, kuram ir daudz cikla stāvokļu. Turpretī jums, iespējams, ir darba pasūtījuma veids **Labojošs**, kas tiek izmantots darba pasūtījumiem, kas nav plānoti, vai darba pasūtījumiem, kur uzdevums ir pabeigts, pirms darba pasūtījums ir izveidots, steidzamas situācijas dēļ. Šis darba pasūtījuma veids var būt saistīts ar darba pasūtījuma dzīves cikla modeli, kuram ir tikai daži dzīves cikla stāvokļi.

Veidu lietošanas pamatojums ir tāds, ka, ja veids ir definēts, piemēram, darba pasūtījumam vai līdzeklim, saistītie darba procesi (dzīves cikla stāvokļi) tiek definēti automātiski. Papildinformāciju par darba pasūtījumu veidu iestatīšanu skatiet sadaļā [Darba pasūtījumu veidi](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Dzīves cikla stāvokļi, dzīves cikla modeļi un veidi attiecas ne tikai uz darba pasūtījumiem, bet arī uz funkcionālajiem novietojumiem, līdzekļiem un uzturēšanas pieprasījumiem.

Tālāk esošajā attēlā redzama relācija starp darba pasūtījuma veidiem, dzīves cikla modeļiem un dzīves cikla stāvokļiem.

![Darba pasūtījuma tipa lapa salīdzinājumā ar Darba pasūtījuma dzīves cikla modeļu lapu](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Darba pasūtījuma dzīves cikla modeļi

Kad esat izveidojis darba pasūtījuma dzīves cikla stāvokļus, kas nepieciešami darba pasūtījumiem, tos var iedalīt darba pasūtījuma dzīves cikla modeļos. Ir jāizveido vismaz viens standarta dzīves cikla modelis.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Dzīves cikla modeļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu darba pasūtījuma dzīves cikla modeli.
3. Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnē **Detalizēta informācija** laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti šajā līdzekļa dzīves cikla modelī. Laukā **Darba pasūtījuma veidi** ir parādīts to darba pasūtījumu veidu skaits, kuri izmanto šo dzīves cikla modeli.

5. Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet dzīves cikla stāvokļus, kuri būtu jāiekļauj dzīves cikla modelī:

    - Lai iekļautu dzīves cikla stāvokli dzīves cikla modelī, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi](media/12-setup-for-work-orders.png), lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai iekļautu visus pieejamos dzīves cikla stāvokļus dzīves cikla modelī, atlasiet pogu **Atlasīt visus pieejamos posmus** ![Atlasīt visus pieejamos posmus](media/13-setup-for-work-orders.png). Visi dzīves cikla stāvokļi tiek pārvietoti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai dzīves cikla modelim noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogui ![Bultiņa pa kreisi](media/14-setup-for-work-orders.png), lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.

6. Atlasiet **Dzīves cikla stāvokļa atjauninājumi**, lai definētu, kuri dzīves cikla stāvokļi var sekot atlasītajam dzīves cikla stāvoklim.
7. Kopsavilkuma cilnes **Atjauninājumi** laukā **Ieplānotais stāvoklis** atlasiet dzīves cikla stāvokli, kas vienmēr jāatlasa darba pasūtījumam, kuram pabeigta darba pasūtījuma plānošana, neatkarīgi no iepriekšējā darba pasūtījuma dzīves cikla stāvokļa.
8. Laukā **Neieplānotais dzīves cikla stāvoklis** atlasiet dzīves cikla stāvokli, kas vienmēr jāatlasa darba pasūtījumam, ja tiek dzēsta darba pasūtījuma plānošana.
9. Saglabājiet darba pasūtījuma dzīves cikla modeli.

![Darba pasūtījuma dzīves cikla modeļu lapa](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]