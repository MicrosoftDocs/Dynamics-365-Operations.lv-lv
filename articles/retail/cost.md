---
title: Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)
description: Šajā tēmā ir aprakstīta Dynamics 365 Retail izmaksu konfigurācijas sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b5e3e1997f3d3b61b7b3c7486f5531e386293537
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019443"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)

[!include [banner](../includes/banner.md)]

Organizācijām ieteicams izmantot vairākus izmaksu komponentus, lai noteiktu optimālu pasūtījuma izpildes vietu. Daži no šiem izmaksu komponentiem ir piegādes izmaksas, apstrādes izmaksas un iepakojuma izmaksas. Šo izmaksu kombinācija tiek aprēķināta tādēļ, lai noteiktu izpildes vietu.

Kad Dynamics 365 Retail pirmā sadalīto pasūtījumu pārvaldības (DOM) iterācija optimizē izpildes vietām piešķirtos pasūtījumus, tiek ņemts vērā tikai attālums. Lai gan attālums var tikt saistīts ar izmaksām, tas nav tas pats, kas izmaksas. Piemēram, vienā attālumā piegādes pa nakti izmaksas ir lielākas nekā piegādes trīs vai septiņu dienu laikā.

Izmantojot izmaksu konfigurācijas funkciju, mazumtirgotāji var definēt un konfigurēt papildu izmaksu komponentus, kas tiks aprēķināti un ņemti vērā, nosakot optimālo vietu pasūtījumu rindu izpildei.

Kad izmaksu komponenti ir konfigurēti, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs izmanto tikai šīs izmaksu definīcijas. Attāluma komponents netiek uzskatīts par izmaksām. Tomēr, ja neviens izmaksu komponents nav konfigurēts, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs neizmanto attāluma komponentu kā izmaksas.

## <a name="set-up-cost-components"></a>Izmaksu komponentu iestatīšana

Sistēmā var definēt divu veidu galvenos izmaksu komponentus: **Piegāde** un **Cits**.

Abiem izmaksu komponentu veidiem tiek atbalstītas vairākas aprēķinu bāzes, kā parādīts tālāk sniegtajā tabulā.

<table>
<thead>
<tr>
<th>Izmaksu komponenta veids</th>
<th>Aprēķina bāze</th>
</tr>
</thead>
<tbody>
<tr>
<td>Piegāde</td>
<td>
<ul>
<li>Vienkāršs</li>
<li>Diferencēts</li>
</ul>
</td>
</tr>
<tr>
<td>Cits</td>
<td>
<ul>
<li>Pārdošanas pasūtījums</li>
<li>Pārdošanas rinda</li>
<li>Vieta</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Piegādes izmaksu komponenta veids

Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida **Piegāde** un piegādes izmaksu aprēķina bāzes kombinācijas. Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Vienkārša

Ja tiek izmantots izmaksu komponenta veids **Piegāde** un aprēķina bāze **Vienkārša**, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma.

Šai kombinācijai ir jāiestata tālāk norādītie lauki.

- **Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.
- **Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.
- **Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu. Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.
- **Aktīvs** — norāda, vai izmaksu faktors ir aktīvs. DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.
- **Uzņēmums** — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors. Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.
- **Piegādes veidi** — norāda piegādes veidus, kam izmaksas tiek konfigurētas.
- **Aprēķina veids** — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas. Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.

    - **Fiksēts** — piegādes veidam tiek izmantotas fiksētās izmaksas. Atlasot šo aprēķina veidu lauks **Izmaksas** tiek izmantots fiksēto izmaksu aprēķināšanai.
    - **Attāluma vienība** — piegādes veida izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā **Izmaksas**, reizinot attālumu starp piegādes adresi un atrašanās vietām.

- **Izmaksas** — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku **Aprēķina veids**, lai aprēķinātu piegādes veida izmaksas.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Sadalīta

Ja tiek izmantots izmaksu komponenta veids **Piegāde** un aprēķina bāze **Sadalīta**, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma. Šajā kombinācijā attālums ir balstīts uz sadalītu attālumu diapazonu.

Šai kombinācijai ir jāiestata tālāk norādītie lauki.

- **Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.
- **Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.
- **Noklusējuma izmaksas** — norāda izmaksas, kas jāizmanto piegādes veidam tad, ja attālums starp piegādes adresi un atrašanās vietu nav nevienā no piegādes veida sadalītajiem attālumiem.
- **Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu. Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.
- **Aktīvs** — norāda, vai izmaksu faktors ir aktīvs. DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.
- **Uzņēmums** — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors. Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.
- **Piegādes veidi** — norāda piegādes veidus, kam izmaksas tiek konfigurētas.
- **Attāluma veids** — norāda, vai sadalītais attālums jāaprēķina kā antenas attālums vai ceļa attālums.
- **Attāluma vienības** — norāda vienību, kas jāizmanto sadalītā attāluma aprēķināšanā.
- **Attāluma sākums** — norāda sadalītā attāluma diapazona sākumu.
- **Attāluma beigas** — norāda sadalītā attāluma diapazona beigas.
- **Aprēķina veids** — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas un sadalītais attālums. Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.

    - **Fiksēts** — piegādes veidam tiek izmantotas fiksētās izmaksas. Atlasot šo aprēķina veidu lauks **Izmaksas** tiek izmantots fiksēto izmaksu aprēķināšanai.
    - **Attāluma vienība** — piegādes veida un sadalītā attāluma izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā **Izmaksas**, reizinot attālumu starp piegādes adresi un atrašanās vietām.

- **Izmaksas** — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku **Aprēķina veids**, lai aprēķinātu piegādes veida izmaksas.

> [!NOTE]
> - Definējot sadalītos attālumus, sistēma pārbauda, vai netrūkst kāda attāluma un vai nav tādu attālumu, kas pārklājas.
> - Visiem sadalītajiem attālumiem piegādes veidam jāizmanto vienāds attāluma veids.

### <a name="other-cost-component-type"></a>Cits izmaksu komponenta veids

Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida **Cits** un cita ar piegādes izmaksām nesaistīta izmaksu veida kombinācijas. Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas pasūtījums

Izmaksu komponenta veida **Cits** un cita izmaksu veida **Pārdošanas pasūtījums** kombinācija tiek izmantota, lai pārdošanas pasūtījuma līmenī definētu ar piegādi nesaistītas izmaksas.

Šai kombinācijai ir jāiestata tālāk norādītie lauki.

- **Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.
- **Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.
- **Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu. Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.
- **Aktīvs** — norāda, vai izmaksu faktors ir aktīvs. DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.
- **Izmaksas** — pārdošanas pasūtījuma līmenī norāda ar piegādi nesaistīto izmaksu vērtību.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas rinda

Izmaksu komponenta veida **Cits** un cita izmaksu veida **Pārdošanas rinda** kombinācija tiek izmantota, lai pārdošanas pasūtījuma rindas līmenī definētu ar piegādi nesaistītas izmaksas.

Šai kombinācijai ir jāiestata tālāk norādītie lauki.

- **Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.
- **Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.
- **Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu. Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.
- **Aktīvs** — norāda, vai izmaksu faktors ir aktīvs. DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.
- **Izmaksas** — pārdošanas pasūtījuma rindas līmenī norāda ar piegādi nesaistīto izmaksu vērtību.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Izmaksu komponenta veids = Cits; Cits izmaksu veids = Vieta

Izmaksu komponenta veida **Cits** un cita izmaksu veida **Vieta** kombinācija tiek izmantota, lai atsevišķai vietai vai vietu grupai definētu ar piegādes izmaksām nesaistītas izmaksas.

Šai kombinācijai ir jāiestata tālāk norādītie lauki.

- **Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.
- **Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.
- **Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu. Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.
- **Aktīvs** — norāda, vai izmaksu faktors ir aktīvs. DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.
- **Izpildes vietu grupa** — norāda vietu grupu, kurai tiek definētas ar piegādi nesaistītās izmaksas.
- **Izpildes vieta** — norāda vietu, kurai tiek definētas ar piegādi nesaistītās izmaksas.

    > [!NOTE]
    > Ja aprēķina kritērijos ir iestatīta atrašanās vieta, izpildes vietu un izpildes vietu grupu nevar norādīt vienā rindā.

- **Izmaksas** — izpildes grupas vai izpildes vietas līmeņos norāda ar piegādi nesaistīto izmaksu vērtību.

> [!IMPORTANT]
> Lai DOM palaišanas laikā šīs izmaksas tiktu ņemtas vērā, izmaksu faktors ir jāpievieno attiecīgajam izpildes profilam.
