---
title: Bieži uzdotie jautājumi par tehnisko izmaiņu pārvaldību
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par tehnisko izmaiņu pārvaldības līdzekli.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69232eed8520bafeb734ffad43b333bf9e36909e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018689"
---
# <a name="engineering-change-management-faq"></a>Bieži uzdotie jautājumi par tehnisko izmaiņu pārvaldību

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par tehnisko izmaiņu pārvaldības līdzekli.

## <a name="should-i-track-the-version-in-transactions"></a>Vai izsekot versiju darījumos?

Veidojot tehnisko izmaiņu kategoriju, lapa **Tehnisko izmaiņu kategorijas informācija** nodrošina opciju ar nosaukumu **Izsekot versiju darījumos**. Kas ir šis iestatījums un ko tas dara?

- Ja iestatāt opciju **Izsekot versiju darīumos** uz *Jā*, lauks **Dimensiju grupa** tiks filtrēts tā, lai tiktu rādītas tikai dimensiju grupas, kur versija ir aktīva dimensija.
- Ja iestatāt opciju **Izsekot versiju darīumos** uz *Nē*, lauks **Dimensiju grupa** tiks filtrēts tā, lai tiktu rādītas tikai dimensiju grupas, kur versijas dimensija **nav** aktīva dimensija.

### <a name="if-you-track-the-version-in-transactions"></a>Ja izsekojat versiju darījumos

Tehniskām kategorijām, kur esat atlasījis dimensiju grupu, kur versija ir aktīva dimensija, jūs izsekosiet versijas šīs kategorijas preču darījumos. Šajā gadījumā tehniskais produkts būs preces šablons, un katra produkta versija būs preces variants, kas izmanto versijas produkta dimensiju. Pārējās dimensijas var lietot kopā ar versijas dimensiju.

Šajā gadījumā katra tehniskā versija tiks uzskatīta par variantu visos procesos. Tāpēc, ja darbībā ir specifisks variants (lai varētu noteikt, kurš variants tika pārdots vai nopirkts), ir jāpārvalda katras versijas krājumi, vispārējais plāns nodrošinās piegādi katrai versijai utt. Ja jūs atceļat versiju no tirgus, jums ir manuāli jāpielāgo tās sākuma un beigu datumi, lai tie atspoguļotu izmaiņas. Jāpārvalda arī krājumi, lai pārliecinātos, vai noliktavās nav neizmantotu krājumu versiju.

Lai gan šai opcijai ir nepieciešams vairāk pārvaldības darba, tas ir ieteicams, ja nepieciešama katrā darbībā izmantoto konkrēto versiju augsta izsekošana.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Ja neizsekojat versiju darījumos

Tehniskām kategorijām, kur esat atlasījis dimensiju grupu, kur versija **nav** aktīva dimensija, jūs **neizsekosiet** versijas šīs kategorijas preču darījumos. Šajā gadījumā, ja neizmantojat nevienu citu dimensiju, tehniskā prece būs atšķirīga prece. Precei joprojām tiks izmantota versija un varat pārvaldīt informāciju par noteiktām versijām (piemēram, par to materiālu komplektu \[MK] un maršrutu), bet nevarēsit izsekot, kura noteiktā versija tika izmantota katrā darījumā. Sākuma un beigu datumi norāda katras versijas derīgumu.

Šo opciju ir daudz vieglāk pārvaldīt, jo, ja vēlaties mainīt vienu versiju uz citu, jums tikai ir jāveic nepieciešamās izmaiņas izmaiņu kārtībā un pēc tam jāatjaunina tehniskajā versijā sākuma un beigu datums. Tad ražošanas procesi saņem nepieciešamo MK un maršrutu precei (un tai specifiskajai versijai).

Lielākā daļa organizāciju izvēlas šo opciju, jo tā nodrošina versiju un izmaiņu pārvaldību, bet nepievieno papildu atbalstu versijas izsekošanai katrā darījuma, krājumos un vispārējās plānošanas laikā.

## <a name="which-fields-are-copied-to-the-released-item-template"></a>Kuri lauki tiek kopēti izlaistajā preču veidnē?

Kad tehniskais uzņēmums izveido tehnisko preci, šī prece tiek izveidota kā izlaistā prece tehniskajā uzņēmumā. Izveidotā izlaistā prece ir balstīta uz atlasītās *izlaistā krājuma veidnes*. (Izlaistā krājuma veidne pati ir jau izlaista prece.) Izlaistā krājuma veidne tiek izmantota arī tad, kad prece tiek izlaista operatīvajam uzņēmumam. Katrā gadījumā izlaistā krājuma veidne nosaka lielāko daļu no izlaistās preces lauka vērtībām, un šīs vērtības ir no saistītās lapas **Izlaistās preces informācija**.

Tabulās ir parādīti lauki, kas kopēti šo procesu laikā.

| Kopsavilkuma cilne | Lauki, kas tiek kopēti, veidojot produktus tehniskajā uzņēmumā | Lauki, kas ir kopēti, izlaižot operatīvajam uzņēmumam |
|---|---|---|
| **Vispārējā daļa** | Visi lauki **Administrēšana** sadaļā | Lauki, kas ir nokopēti tehniskajam uzņēmumam |
| **Pirkšana** | Visi lauki | Visi lauki, izņemot **Vienība** |
| **Pārdot** | Visi lauki šajās sadaļās: **Pārdošanas pasūtījums**, **Administrācija**, **Taksācija**, **Cenas atjaunināšana**, **Pamata pārdošanas cena**, **Maksas**, **Atlaides** un **Alternatīvā prece** | Visi vienādi lauki, kas ir nokopēti tehniskajam uzņēmumam, izņemot **Vienība** |
| **Ārējā tirdzniecība** | Visi lauki | Visi lauki |
| **Pārvaldīt krājumus** | Visi lauki un sadaļas, *izņemot* **Fiziskās dimensijas** un **Pieļaujamais svars** | Visi vienādi lauki, kas ir nokopēti tehniskajam uzņēmumam, izņemot **Vienība** |
| **Inženieris**, **Plāns**, **Pārvaldīt izmaksas**, **Pārvaldīt projektus**, **Finanšu dimensijas** un **Noliktava** | Visi lauki | Visi lauki, izņemot **BOM Vienība** |
| **Preces varianti** | Visi lauki **Noklusējuma preces variants** sadaļā | Lauki, kas ir nokopēti tehniskajam uzņēmumam |

Papildus iepriekšējā tabulā parādītajiem laukiem visi noklusējuma pasūtījuma iestatījumi tiek kopēti no izlaistā krājuma veidnes gan tad, kad prece ir izveidota tehniskajā uzņēmumā, gan tad, kad tā ir nodota izpildei operatīvajam uzņēmumam. (Lai skatītu izlaisto krājumu veidnes noklusējuma pasūtījuma iestatījumus, atveriet atbilstošo lapu **Detalizēta informācija par izlaistajām precēm** un pēc tam darbību rūtī cilnē **Pārvaldīt krājumus** atlasiet **Noklusējuma pasūtījuma iestatījumi**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Vai jāizveido atsevišķa juridiska persona, kas paredzēta tehniskajiem produktiem vai jāizmanto esoša juridiska persona?

Jūsu biznesa prasības nosaka, vai jums ir jāizveido jauna juridiska persona tehniskajam precēm.

Veidojot atsevišķu tehnisko uzņēmumu, jūs varat saglabāt šos datus atsevišķi un pēc tam pievienot modifikācijas, kas nepieciešamas vietējiem operatīvajiem uzņēmumiem. Šādā veidā var sasniegt šādus mērķus:

- Paturēt atsevišķu elementu, kurā tiek veidoti un pārvaldīti tehniskie produkti.
- Neļaut tehniskā produktu parādīšanu kopā ar pārējām izlaistajām precēm, līdz tās ir gatavas un izlaistas.
- Skaidri izšķirt datus, ko nosaka tehniskie un lokālie dati.

No otras puses, jums varbūt vajadzētu izmantot esošo juridisko personu kā tehnisko uzņēmumu, ja uz jums attiecas šādi nosacījumi:

- Jūsu sistēmā ir tikai viena juridiska persona, un/vai jums nav nepieciešama skaidra nošķiršana starp produktiem, kas tiek ražoti.
- Jūs nevēlaties dublēt dažus datus, piemēram, resursu grupas, resursus, operācijas un (iespējams) vietnes.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Kas ir nomenklatūra tehniskajām versijām un variantiem?

Tehnisko preču un preču variantu nomenklatūra darbojas šādā veidā:

- Tehniskajai precei (t.i., atšķirīgai precei, ja netiek izmantotas dimensijas, vai preču šablonam, ja tiek izmantota kāda dimensija), numura noteikuma nomenklatūra ir definēta tehnisko preču kategorijā. Pastāv opcija izmantot numuru sēriju, teksta konstantes, atribūtu nosaukumus un vērtības.
- Katram tehniskās preces variantam (ja jūsu tehniskā prece ir preces šablons, varianti ir iestatīti tehnisko preču kategorijā, kur norādāt dimensiju grupu), numuru noteikumu tabula katram variantam ir definēta dimensiju grupā. Šajā gadījumā var izmantot šablona preces ID un dimensijas vērtības un nosaukumus.
