---
title: "Piegādes alternatīvas"
description: "Pārdošanas pasūtījumu ņēmēji var izmantot lapu Piegādes alternatīvas, lai uzzinātu par alternatīvām pasūtījumu izpildes iespējām."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b2ecf2d5b14dac28a26fe172807ae2931cb4c3ca
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-alternatives"></a>Piegādes alternatīvas

[!include[banner](../includes/banner.md)]


Pārdošanas pasūtījumu ņēmēji var izmantot lapu Piegādes alternatīvas, lai uzzinātu par alternatīvām pasūtījumu izpildes iespējām.

Programmas Microsoft Dynamics 365 for Operations versijā 1611 (2016. gada novembris) pārdošanas pasūtījumu ņēmēji var izmantot lapu **Piegādes alternatīvas**, lai uzzinātu par alternatīvām pasūtījumu izpildes iespējām. Pārveidotais lapas izkārtojums sniedz labāku pārskatu par visām alternatīvajām iespējām. Tas arī ļauj pasūtījuma ņēmējiem palūkoties ārpus pašreizējā uzņēmuma attiecībā uz izpildes iespējām. Tagad tie var skatīt gan starpuzņēmumu iespējas, gan iespējas no ārējiem kreditoriem. Sakārtojot iespējas pēc piegādes datuma, pārdošanas pasūtījumu ņēmēji var skatīt viedo piegādes alternatīvu sarakstu. Turklāt parametri palīdz tiem labāk pārvaldīt ieteiktās piegādes. Tā kā transportēšanas laiks var ietekmēt piegādes datumus, pārdošanas pasūtījumu ņēmēji var izpētīt dažādas transportēšanas iespējas, kuras piedāvā pārvadātāji. Tā kā katram ieteikumam tiek parādīta detalizēta informācija, pasūtījumu ņēmēji var pieņemt pamatotus lēmumus tieši no lapas **Piegādes alternatīvas**.

## <a name="open-the-delivery-alternatives-page"></a>Lapas Piegādes alternatīvas atvēršana
Varat atvērt lapu **Piegādes** **alternatīvas** no pārdošanas pasūtījuma rindas.

1.  Noklikšķiniet uz **Preces un piegāde** &gt; **Piegādes alternatīvas**.
2.  Noklikšķiniet uz **Rindas informācija** &gt; **Piegāde** &gt; **Piegādes alternatīvas.**

Atvērt lapu **Piegādes alternatīvas** var, arī atverot darbvietu **Pārdošanas pasūtījuma apstrāde un pieprasījums** un pēc tam noklikšķinot uz **Pasūtījumi un izlase** &gt; **Kavētu pasūtījumu rindas** &gt; **Piegādes alternatīvas** **Piezīme.** Lapu **Piegādes alternatīvas** var atvērt tikai tad, ja ir ievēroti abi šādi nosacījumi:

-   Tiek aizpildīta visa obligātā pārdošanas rindas informācija.
-   Laukam **Piegādes datuma kontrole** ir iestatīta cita vērtība, nevis **Nav**.

## <a name="delivery-date-control-methods"></a>Piegādes datuma kontroles metodes
Piegādes datuma kontroles metode paredz, kā sistēma nosaka piegādes datumus, kā tiek aprēķinātas piegādes alternatīvas un kāda informācija ir redzama. Ņemiet vērā, ka piegādes datu kontrole ņem vērā kalendārus. Tādēļ tālāk minētie kalendāri var ietekmēt ieteikto saņemšanas datumu: Noliktavas kalendārs, Transportēšanas kalendārs, Kreditoru kalendārs un Debitoru kalendārs. Tabulā ir aprakstīta katra piegādes datuma kontroles metode.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Metode</strong></td>
<td><strong>Apraksts</strong></td>
</tr>
<tr class="even">
<td><strong>Nav</strong></td>
<td><ul>
<li>Piegādes alternatīvas pārdošanas rindām netiek atbalstītas. Šī opcija izslēdz piegādes datu kontroli.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Pārdošanas izpildes laiks</strong></td>
<td><ul>
<li>Piegādes alternatīvas tiek aprēķinātas, pamatojoties uz iepriekš noteiktu pārdošanas izpildes laiku. Transportēšanas dienas tiek aprēķinātas, balstoties uz piegādes veidu.</li>
<li>Piegādes alternatīvas ietver noliktavas, kurās ir rīcībā esoši krājumi, un piedāvājuma/pieprasījuma pasūtījumus.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Piegādes alternatīvas tiek aprēķinātas, pamatojoties uz loģiku Pieejams solīšanai (ATP). Tiek ņemta vērā pašreizējā pieejamība un paredzamā pieejamība nākotnē. Transportēšanas dienas tiek aprēķinātas, balstoties uz piegādes veidu.</li>
<li>Piegādes alternatīvas ietver noliktavas, kurās ir rīcībā esoši krājumi, un piedāvājuma/pieprasījuma pasūtījumus.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + Izejas plūsmas rezerve</strong></td>
<td><ul>
<li>Piegādes alternatīvas tiek aprēķinātas tāpat kā ATP metodei, bet aprēķinā tiek iekļauta izejas plūsmas rezerve.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Piegādes alternatīvas tiek aprēķinātas, pamatojoties uz loģiku Pieejams iegādei (CTP). MRP izvēršana tiek izmantota, lai noteiktu pieejamību. Ņemiet vērā, ka CTP vismaz nobīda piegādes datumus līdz pārdošanas izpildes laikam. Transportēšanas dienas tiek aprēķinātas, balstoties uz piegādes veidu.</li>
<li>Piegādes alternatīvas ietver ieteikumus attiecībā uz šādām noliktavām:
<ul>
<li>Pašreizējā noliktava</li>
<li>Noklusējuma noliktava</li>
<li>Visas noliktavas, kurām ir pieejami rīcībā esoši krājumi</li>
<li>Visas noliktavas, kurām ir piedāvājumu pasūtījumi</li>
<li>Visas noliktavas, kurām ir aktīvas materiālu komplektu (MK) versijas</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Informācijas par piegādes alternatīvām skatīšana
Šajā sadaļā ir aprakstīta informācija par piegādes alternatīvām, kas ir pieejama katrā lapas **Piegādes alternatīvas** cilnē.

### <a name="products"></a>Preces

Šajā cilnē ir parādīts kopsavilkums par preci un detalizēta informācija par pašreizējo pārdošanas rindu.

### <a name="delivery-alternatives"></a>Piegādes alternatīvas

Šajā cilnē ir parādīts piegādes alternatīvu saraksts, kas ir sakārtots pēc saņemšanas datiem. Virs saraksta varat atlasīt, uz kurām opcijām balstīt ieteikumus. Varat arī atlasīt piegādes veidu, kas nosaka transportēšanas dienas. Pieejamas šādas opcijas

-   **Ietvert citus preces variantus** — šī opcija ir pieejama precēm, kurām ir preces varianti. Tā ietvers piegādes alternatīvas citiem preces variantiem. Šī opcija nav pieejama CTP.
-   **Iekļaut daļēju daudzumu** — pēc noklusējuma tiek iekļauti tikai ieteikumi, kas atbilst pārdošanas rindas pilnajam daudzumam. Atlasiet šo opciju, lai iekļautu ieteikumus, kuri tikai daļēji atbilst pasūtījuma rindai. Šī opcija ir noderīga, ja debitors pieprasa agrāku piegādes datumu un pieņem daļēju piegādi.
-   **Iekļaut vēlākus datumus** — pēc noklusējuma tiek parādīti tikai ieteikumi, kas ir labāki (agrāki) nekā pašreizējie datumi pārdošanas rindās. Atlasiet šo opciju, lai iekļautu vēlākus datumus. Šī opcija var būt noderīga situācijās, kurās prioritāte ir parametriem, kas nav datums. Piemēram, prioritāte var tikt piešķirta noteiktam kreditoram vai noliktavai.
-   **Piegādes veids** — atlasiet vēlamo piegādes veidu, lai optimizētu transporta laiku un izmaksas. Jūs nekavējoties redzēsit ietekmi uz ieteiktajām piegādes alternatīvām. Tādēļ ir viegli salīdzināt alternatīvas.
-   **Ietvert sagādi** — izvēloties sagādi, ieteiktajās piegādes alternatīvās ir ietvertas opcijas sagādei gan no ārējiem kreditoriem, gan citiem uzņēmumiem (starpuzņēmumu). Opcija **Ietvert sagādi** tiek atbalstīta tikai ATP un ATP + Izejas plūsmas rezerves piegādes datuma kontrolei. Ir ietvertas sagādes opcijas no preces noklusējuma pirkšanas kreditora un visiem preces apstiprinātajiem piegādātājiem.
-   Ārējiem kreditoriem aprēķins balstās uz pirkšanas izpildes laiku.
-   Starpuzņēmumu gadījumā aprēķinā tiek ņemts vērā, kas ir pieejams no avotu uzņēmuma, pamatojoties uz piegādes datuma kontroli avotu uzņēmumā.
-   **Piegādes veids** (attiecas uz sagādi)
    -   **Krājumi** — preces tiek sūtītas no avotu noliktavas uz pārdošanas rindas vietu/noliktavu. Pēc tam tās tiek nosūtītas no attiecīgās noliktavas debitoram.
    -   **Tiešā piegāde** — preces tiek sūtītas tieši no avotu noliktavas debitoram.

### <a name="availability-information"></a>Informācija par pieejamību

Informācija šajā cilnē ir saistīta ar piegādes alternatīvo rindu, kas tiek atlasīta. Atkarībā no piegādes datuma kontroles pārdošanas rindai tiek rādīta šāda informācija:

-   **Pārdošanas izpildes laiks**
    -   **Pieejams šodien** — parāda pašreizējos fiziski rīcībā esošos, fiziski rezervētos un pieejamos fiziskos krājumus.
    -   **Parametri** — rāda krājumu vienību un pārdošanas izpildes laiku.

-   **ATP + Izejas plūsmas rezerve**
    -   **Pieejams šodien** — parāda pašreizējos fiziski rīcībā esošos, fiziski rezervētos un pieejamos fiziskos krājumus.
    -   **Parametri** — rāda krājumu vienību un pārdošanas izpildes laiku.
    -   **Pieejamība nākotnē** — parāda grafisko attēlojumu attiecībā uz atlasītās atrašanās vietas un noliktavas pašreizējo un nākotnes pieejamību sadaļā **Piegādes alternatīvas**. Lai skatītu detalizētāku informāciju par turpmāko preces pieejamību, varat klikšķināt uz diagrammas kolonnām. Slīdnis rāda sarakstu ar attiecīgajiem pieprasījuma un piegādes pasūtījumiem ATP periodā.

-   **CTP**
    -   **Pieejams šodien** — parāda pašreizējos fiziski rīcībā esošos, fiziski rezervētos un pieejamos fiziskos krājumus.
    -   **Parametri** — rāda krājumu vienību un pārdošanas izpildes laiku.
    -   **Izvēršana** — rāda atlasītās piegādes alternatīvas piegādes izvēršanu. Varat izmantot vienumu **Iestatījumi**, lai mainītu laukus un krājumu dimensijas, kas parādītas izvēršanā.

### <a name="impact-of-selected-alternative"></a>Atlasītās alternatīvas ietekme

Šī cilne izceļ atlasītās piegādes alternatīvas ietekmi. Noklikšķinot uz **Labi**, pārdošanas rinda tiek atjaunināta ar izceltajām vērtībām ATLASĪTAJĀS kolonnās. Ņemiet vērā, ka gadījumā, ja atlasītajai piegādes alternatīvai daudzums ir mazāks nekā daudzums pārdošanas rindā, tiek izveidots piegādes grafiks un pasūtījuma rinda tiek sadalīta divās rindās: viena rinda ir paredzēta atlasītajam daudzumam un otra rinda — atlikušajam daudzumam. Varat arī atjaunināt komerciālo rindu tā, lai tā atbilst grafika rindām un ietekmē cenu noteikšanu.

<a name="see-also"></a>Skatiet arī
--------

[Pasūtījumu solīšana](delivery-dates-available-promise-calculations.md)





