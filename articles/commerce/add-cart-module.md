---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154021"
---
# <a name="cart-module"></a>Groza modulis

[!include [banner](includes/banner.md)]

Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos. Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.

Groza modulis atbalsta pierakstīšanās un viesa norēķinu. Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**. Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.

Groza modulis veido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne.

## <a name="cart-module-properties-and-slots"></a>Groza moduļa rekvizīti un sloti

Groza modulim ir rekvizīts **Virsraksts**, ko var iestatīt vērtībām, piemēram, **Iepirkumu grozs** un **Preces jūsu grozā**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduļi, ko var izmantot groza modulī

- **Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī. Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS). Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Store Selector modulī.](store-selector.md)

## <a name="cart-module-settings"></a>Groza moduļa iestatījumi

Groza moduļiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos. Šī krājuma pārbaude tiek veikta gadījumā, kad prece tiks nosūtīta, gan gadījumā, kad prece tiks saņemta veikalā. Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas.
- **Krājumu buferis** — šis rekvizīts tiek izmantots, lai norādītu krājuma bufera numuru. Krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti. Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama. Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.
- **Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**. Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API. Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Groza moduļa pievienošana lapā

Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet fragmentu ar nosaukumu **Groza fragments** un pievienojiet jaunajam fragmentam groza moduli.
1. Pievienojiet virsrakstu groza modulim.
1. Pievienojiet veikala atlasītāja moduli groza modulim.
1. Saglabājiet fragmentu, pabeidziet to rediģēt un publicējiet šo fragmentu.
1. Izveidojiet veidni ar nosaukumu **Groza veidne** un pievienojiet groza fragmentu, ko tikko izveidojāt.
1. Saglabājiet veidni, pabeidziet to rediģēt un publicējiet šo veidni.
1. Izveidojiet lapu, kas izmanto jauno veidni.
1. Saglabājiet un priekšskatiet lapu.
1. Pabeidziet rediģēt lapu un šo lapu publicējiet.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Veikala atlasītāja modulis](store-selector.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
