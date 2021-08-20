---
title: Preču dzīves cikla stāvokļi un darījumi
description: Šajā tēmā ir paskaidrots, kā jūs varat kontrolēt, kuri darījumi ir atļauti katram dzīves cikla stāvoklim, jo ​​tehniskā prece iziet tā dzīves ciklu.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 099e8af88d7f6dfaf6268d0ca73a120487920c4c694dc3f540d7ef6a21ddd730
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744158"
---
# <a name="product-lifecycle-states-and-transactions"></a>Preču dzīves cikla stāvokļi un darījumi

[!include [banner](../includes/banner.md)]

Ir svarīgi, ka jūs varat kontrolēt, kuri darījumi ir atļauti katram dzīves cikla stāvoklim, jo ​​tehniskā prece iziet tā dzīves ciklu. Piemēram, preces, kas vēl nav pabeigtas, nevar laist pārdošanas pasūtījumā. Alternatīvi, ja prece ir sasniegusi nolietotu stāvokli, iespējams, vēlēsities kontrolēt šīs preces pieplūdumu.

Tehniskajai precei izmaiņas dzīves cikla stāvoklī ir saistītas ar preces izstrādes versijām. Tāpēc preces dzīves cikla stāvoklis var tikt pievienots arī tehniskajām versijām. Kad preces dzīves cikla stāvoklis ir savienots ar tehnisko versiju, varat izmantot dzīves cikla stāvokli, lai kontrolētu, kuras darbības ir atļautas tehniskajai versijai.

## <a name="create-and-manage-product-lifecycle-states"></a>Preču dzīves cikla stāvokļu izveide un pārvaldīšana

Lai strādātu ar preces lietošanas cikla stāvokļiem, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Preces dzīves cikla stāvoklis**. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai izveidotu jaunu dzīves cikla stāvokli, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai rediģētu esošu dzīves cikla stāvokli, atlasiet to saraksta rūtī, atlasiet **Jauns** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai dzēstu esošo dzīves cikla stāvokli, atlasiet to saraksta rūtī un pēc tam darbības rūtī atlasiet vienumu **Dzēst**.

> [!NOTE]
> Tehniskās preces izmanto tos pašus preces dzīves cikla stāvokļus kā standarta (ne tehniskās) preces. Šajā tēmā aprakstīto **Preču dzīves cikla stāvokļa** lapu varat atvērt arī, dodoties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preces dzīves cikla stāvoklis**. Lai iegūtu vairāk informācijas par preču dzīves cikla stāvokļiem, kas paredzēti gan tehniskajām precēm, gan standarta precēm, skatiet [Preces dzīves cikla stāvokļa apskats](../pim/product-lifecycle.md).

### <a name="header"></a>Galvene

Iestatiet tālāk norādītos laukus preces dzīves cikla stāvokļa virsrakstā.

| Lauks | Apraksts |
|---|---|
| Novads | Ievadiet preču dzīves cikla stāvokļa nosaukumu. |
| Apraksts | Ievadiet preču dzīves cikla stāvokļa aprakstu. |

### <a name="general-fasttab"></a>Cilne Vispārīgi

Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus.

| Lauks | Apraksts |
|---|---|
| Noklusējums, kad tiek izlaista juridiskai personai | Standarta precēm iestatiet šo opciju uz *Jā*, ja šī dzīves cikla stāvoklis ir jālieto visām precēm pēc noklusējuma, kad tās pirmoreiz tiek izlaistas. Iestatiet to uz *Nē*, ja šī dzīves cikla stāvoklis tiks manuāli lietots vēlāk.<p>Šis iestatījums neattiecas uz tehniskajām precēm. Tehniskās preces versijas dzīves cikla stāvoklis, kad tas ir izveidots inženierijas uzņēmumā, ir norādīts IT tehnoloģiju izmaiņu kategorijā. Kad prece ir nodota darbojošajam uzņēmumam, preces dzīves cikla stāvoklis tiek kopēts. Citiem vārdiem sakot, kad tehniskais produkts tiek izlaists darbojošajam uzņēmumam, tai ir tāds pats dzīves cikla stāvoklis, kāds tas bija inženierijas uzņēmumā. Dzīves cikla stāvokli var pārrakstīt darbības uzņēmumā.</p> |
| Ir aktīvs plānošanai | Iestatiet šo opciju uz *Jā*, lai iekļautu preces, kas ir šajā dzīves cikla stāvoklī aprēķinos vispārējās plānošanas un materiālu komplekta (MK) līmeņos. Iestatiet to uz *Nē*, lai neiekļautu šajā dzīves cikla stāvoklī esošas preces no aprēķiniem. |

### <a name="enabled-business-processes-fasttab"></a>Iespējotie biznesa procesu kopsavilkuma cilne

Lietojiet kopsavilkuma cilni **Iespējotie biznesa procesi**, lai kontrolētu, kuri no pieejamajiem biznesa procesiem var tikt izmantoti ar precēm pašreizējā dzīves cikla stāvoklī. Procesi, kas uzskaitīti šajā kopsavilkuma cilnē, tiek automātiski atrasti šādā veidā:

- Pirmā reize, kad saglabājat jaunu dzīves cikla stāvokli, lapa ielādē biznesa procesus, kas pašlaik ir pieejami.
- Ja sistēmai pievienojat jaunus biznesa procesus, varat atjaunināt sarakstu kopsavilkuma cilnē **Iespējotie biznesa procesi** esošam dzīves cikla stāvoklim, darbības rūtī atlasot **Pārbaudīt, vai nav atjauninājumu**.

Šie lauki ir pieejami katram procesam, kas norādīts kopsavilkuma cilnē **Iespējotie biznesa procesi**.

| Lauks | Apraksts |
|---|---|
| Apstrādāšana | Šis tikai lasāmais lauks rāda esoša biznesa procesa nosaukumu. |
| Apstrādāt apgabalu | Šis tikai lasāmais lauks rāda esoša apgabala procesa nosaukumu. |
| Polise | Atlasiet vienu no šīm vērtībām, lai kontrolētu, vai un kā pašreizējais process tiks atļauts šajā dzīves cikla stāvoklī esošajām precēm:<ul><li>**Iespējots** – biznesa process ir atļauts.</li><li>**Bloķēts** – process nav atļauts. Ja lietotājs mēģina izmantot šo procesu precei, kas ir šajā dzīves cikla stāvoklī, sistēma bloķēs mēģinājumu un tā vietā rādīs kļūdu. Piemēram, varat bloķēt nolietotās preces no iegādes.</li><li>**Iespējots ar brīdinājumu** – process ir atļauts, bet tiks parādīts brīdinājums. Piemēram, jūs varētu vēlēties, lai preces prototips tiktu likts ražošanas pasūtījumā, ko izveido izpētes un attīstības nodaļa. Tomēr citām nodaļām ir jāapzinās, ka tām vēl nav jāražo prece.</li></ul> |

Ja pievienojat papildu cikla stāvokļa nosacījumus kā pielāgošanu, šīs kārtulas varat skatīt lietotāja interfeisā (UI), augšējā rūtī atlasot opciju **Atsvaidzināt procesus**. Poga **Atsvaidzināt procesus** ir pieejama tikai administratoriem.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Dzīves cikla stāvokļi izlaistajām precēm un preču variantiem

Precei, kam ir varianti (šablons un varianti), precei (šablons) būs dzīves cikla stāvoklis, un katram variantam var būt arī cits dzīves cikla stāvoklis.

Specifiskiem procesiem, ja variants vai prece ir bloķēta, arī process tiks bloķēts. It īpaši, lai noteiktu, vai process ir bloķēts, sistēma veiks šādas pārbaudes:

- Inženiertehniski kontrolētām precēm:
  - Ja pašreizējā inženierzinātnes versija ir bloķēta, bloķējiet procesu.
  - Ja pašreizējais variants ir bloķēts, bloķējiet procesu.
  - Ja izlaistā prece ir bloķēta, bloķējiet procesu.
- Standarta precēm:
  - Ja pašreizējais variants ir bloķēts, bloķējiet procesu.
  - Ja izlaistā prece ir bloķēta, bloķējiet procesu.

Piemēram, pieņemsim, ka vēlaties pārdot tikai vienu konkrētās preces (t-krekla) variantu (sarkanu) un pašlaik bloķēt visu pārējo variantu pārdošanu. To var ieviest, izmantojot šādu iestatījumu:

- Piešķiriet precei dzīves cikla stāvokli, kas atļauj procesu. Piemēram, piešķiriet t-krekla precei piešķir *Pārdodams* dzīves cikla stāvokli, kas ļauj veikt *Pārdošanas pasūtījuma* procesu.
- Piešķiriet pārdodamajam variantam dzīves cikla stāvokli, kas atļauj procesu. Piemēram, sarkanajam variantam piešķir arī dzīves cikla stāvokli *Pārdodams*.
- Visiem citiem variantiem tiek piešķirts cits dzīves cikla stāvoklis, kur process ir bloķēts. Piemēram, piešķiriet baltu variantu (un visus citus variantus) dzīves cikla stāvokli *Nepārdodams*, kas bloķē *Pārdošanas pasūtījuma* biznesa procesu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
