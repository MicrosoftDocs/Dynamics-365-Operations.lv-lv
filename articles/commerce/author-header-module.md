---
title: Galvenes modulis
description: Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885482"
---
# <a name="header-module"></a>Galvenes modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti galvenes moduļi un aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Virsraksta modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas tiks rādīti lapas galvenē. Piemēram, tas var ietvert jūsu vietnes logotipu, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē un meklēšanas joslu.

Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (tas ir, darbvirsmas ierīcei vai mobilajai ierīcei). Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).

## <a name="properties-of-a-header"></a>Galvenes rekvizīti

Tāpat kā vispārējie konteineri, galvenes modulis atbalsta **virsraksta** un **platuma** rekvizītu.

Virsraksta modulim ir vairāki sloti. Piemēram, sloti ir informācijas ziņojumam, navigācijas izvēlnei, logotipam, meklēšanas joslai, groza ikonai, vēlmju saraksta ikonai un konta informācijai. Katrs slots atbalsta noteiktu moduļu kopu.

## <a name="modules-that-are-available-in-a-header-module"></a>Galvenes modulī pieejamie moduļi

Šādus moduļus var izmantot galvenes modulī.

- **Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites. Kanāla navigācijas hierarhiju var konfigurēt programmā Dynamics 365 Retail. Konfigurētie elementi tiek parādīti kā galvenes navigācija. Turklāt var tikt konfigurētas statiskas navigācijas saites, un var tikt nodrošinātas relatīvas saites uz citām lapām E-komercijas vietnē. Galveni var līdzināt pa kreisi, pa labi vai centrēt.
- **Groza ikona** — groza ikona ir īpaša ikona, kas apzīmē grozu. Tā tiek parādīta virsrakstā un norāda elementu skaitu grozā. Saite uz groza lapu jāpievieno groza ikonai, lai klientus varētu novirzīt uz groza lapu, kad viņi mijiedarbojas ar ikonu.
- **Vēlmju saraksta ikona** — virsrakstā ir parādīta vēlmju saraksta ikona, un tā norāda elementu skaitu, kas pievienoti klienta vēlmju sarakstam. Šai ikonai ir jāpievieno saite uz vēlmju sarakstu, lai klientus var novirzīt uz vēlmju saraksta lapu, kad viņi mijiedarbojas ar ikonu.
- **Pierakstīšanās modulis** – pierakstīšanās modulis ir redzams virsrakstā. Tas ļauj klientiem vai nu pierakstīties savā kontā, vai reģistrējieties kontam. Ja klients jau ir pierakstījies, moduli var konfigurēt, lai rādītu saites uz konta lapu, pasūtījuma vēstures lapu vai citu lapu.
- **Logotipa modulis** — šis modulis rāda logotipu, kas apzīmē mazumtirgotāju un zīmolu. Tas ir attēls, kuram ir saite. Parasti saite ir konfigurēta tā, ka tā varētu novirzīt uz sākumlapu, tāpēc klienti var ātri atgriezties sākumlapā no jebkuras vietnes lapas.
- **Brīdinājums** — galvenē tiek parādīts brīdinājums, un tas tiek izmantots, lai atspoguļotu iekļauto ziņojumu, kas attiecas uz visām vietnes lapām. Piemēram, brīdinājumā var tikt parādīts ziņojums “Ikgadējā izpārdošana beidzas pēc 10 dienām”.
- **Meklēšanas josla** — meklēšanas josla ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai. Modulim jābūt konfigurētam ar meklēšanas rezultātu lapas vietrādi URL. Vaicājuma virknes parametru var konfigurēt (noklusējuma vērtība ir **“q”**). Meklēšanas joslai ir automātiskās piedāvāšanas slots, kurā ir jāpievieno automātiskās piedāvāšanas modulis.
- **Automātiskā piedāvāšana** – automātiskās piedāvāšanas modulis rāda automātiski piedāvātos rezultātus. Šie rezultāti var būt atslēgvārdi, preces vai kategorijas, kur ir atrasts meklējamais termins.

## <a name="create-a-header-module"></a>Galvenes moduļa izveide

Lai izveidotu galvenes moduli, veiciet šādas darbības.

1. Izveidojiet lapas fragmentu, kas ietver galvenes moduli.
1. Pievienojiet moduļus slotiem virsrakstu modulī.
1. Atjauniniet katra moduļa iestatījumus.
1. Saglabājiet lapas fragmentu. 
1. Pārbaudiet lapu un publicējiet to.

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Noklusējuma lapā lapas fragmentu, kas ietver virsraksta moduli, pievienojiet galvenei, kas atrodas galvenajā slotā.
1. Saglabājiet veidni. 
1. Pārbaudiet veidni un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
