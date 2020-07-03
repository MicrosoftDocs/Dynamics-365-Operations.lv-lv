---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411277"
---
# <a name="cart-module"></a>Groza modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos. Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.

Groza modulis atbalsta pierakstīšanās un viesa norēķinu. Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**. Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.

Groza modulis veido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne. 

Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē.

![Groza moduļa piemērs](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Groza moduļa rekvizīti un sloti

Groza modulim ir rekvizīts **Virsraksts**, ko var iestatīt vērtībām, piemēram, **Iepirkumu grozs** un **Preces jūsu grozā**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduļi, ko var izmantot groza modulī

- **Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī. Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS). Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).

## <a name="module-properties"></a>Moduļa rekvizīti

Groza moduļa iestatījumiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).
- **Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**. Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API. Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Groza moduļa pievienošana lapā

Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Lapas fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jaunas lapas fragments** atlasiet moduli **Grozs**.
1. Sadaļā **Lapas fragmenta nosaukums** ievadiet nosaukumu **Groza fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Grozs**.
1. Rekvizītu rūts labajā pusē atlasiet zīmuļa simbolu, ievadiet virsraksta tekstu laukā un pēc tam atlasiet atzīmes simbolu.
1. Slotā **Grozs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet veidnes nosaukumu.
1. Struktūras kokā atlasiet slotu **Pamatteksts**, atlasiet daudzpunktess (**...**) un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Atlasīt lapas fragmentu** atlasiet fragmentu **Groza fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni, ievadiet lapas nosaukumu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Veikalu atlasītāja modulis](store-selector.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modulis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)
