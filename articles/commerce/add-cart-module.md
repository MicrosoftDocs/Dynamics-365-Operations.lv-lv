---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 33db06ecfa2a8fa93cde3c4f1b31d6b30bfd0c34
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/07/2020
ms.locfileid: "4414207"
---
# <a name="cart-module"></a>Groza modulis

[!include [banner](includes/banner.md)]

Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Groza modulis parāda krājumus, kas ir pievienoti grozam, pirms debitors turpina ar norēķināšanos. Modulis arī parāda pasūtījuma kopsavilkumu un ļauj klientam piemērot vai noņemt veicināšanas kodus.

Groza modulis atbalsta pierakstīšanās un viesa norēķinu. Tas atbalsta arī saiti **Atgriezties pie iepirkšanās**. Jūs varat konfigurēt maršrutu šo saiti sadaļā **Vietnes iestatījumi \> Paplašinājumi \> Maršruti**.

Groza modulis atveido datus, pamatojoties uz groza ID, kas ir visā vietnē pieejama pārlūka sīkdatne. 

Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē.

![Groza moduļa piemērs Fabrikam vietnē](./media/cart2.PNG)

Attēlā zemāk redzams groza lapas piemērs Fabrikam vietnē. Šajā piemērā ir norādīta papildmaksa par rindas krājumu.

![Groza moduļa piemērs ar apstrādes komisiju rindas krājumam](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Groza moduļa rekvizīti un sloti

| Rekvizīts | Vērtības | Apraksts |
|----------------|--------|-------------|
| Virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Groza virsraksts, piemēram, "Iepirkumu soma", vai "Preces jūsu grozā". |
| Rādīt “Nav krājumā” kļūdas | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, groza lapā būs redzamas ar krājumu saistītas kļūdas. Ieteicams iestatīt šo rekvizītu kā **Patiess**, ja vietnē tiek lietotas krājumu pārbaudes. |
| Rādīt rindu vienību piegādes izmaksas | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, groza rindas krājumi rādīs piegādes izmaksas, ja šī informācija ir pieejama. Šis līdzeklis netiek atbalstīts Fabrikam tēmā, jo lietotāji atlasa piegādi tikai izrakstīšanās plūsmā. Tomēr šo līdzekli var ieslēgt citās darbplūsmās, ja tas ir piemērojams. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduļi, ko var izmantot groza modulī

- **Teksta bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī. Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS). Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.
- **Veikala atlasītājs** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Tas ļauj lietotājiem ievadīt atrašanās vietu, lai atrastu tuvuma esošos veikalus. Plašāku informāciju par šo moduli skatiet [Veikala atlasītāja modulis](store-selector.md).

## <a name="module-properties"></a>Moduļa rekvizīti

Groza moduļa iestatījumiem ir šādi iestatījumi, kurus var konfigurēt sadaļā **Vietnes iestatījumi \> Paplašinājumi**.

- **Maksimālais daudzums** — šis rekvizīts tiek izmantos, lai norādītu katras preces maksimālo skaitu, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumi** — papildinformāciju par to, kā lietot krājumu iestatījumus, skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).
- **Atgriezties pie iepirkšanās** — šis rekvizīts tiek izmantots, lai norādītu maršrutu saitei **Atgriezties pie iepirkšanās**. Maršrutu var konfigurēt vietnes līmenī, ļaujot mazumtirgotājiem aizvest debitoru uz sākumlapu vai jebkuru citu vietnes lapu.

> [!IMPORTANT]
> Dynamics 365 Commerce 10.0.14 laidienā un vēlākos laidienos preces grozā tiek apkopotas, pamatojoties uz iestatījumiem, kas definēti tiešsaistes funkcionalitātes profilā tiešsaistes veikalam programmā Commerce Headquarters. Papildinformāciju par to, kā izveidot tiešsaistes funkcionalitātes profilu un iestatīt rekvizītus, kas nepieciešami apkopošanai, skatiet sadaļā [Tiešsaistes funkcionalitātes profila izveide](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Groza modulis izgūst preču informāciju, izmantojot Commerce Scale Unit API. Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Groza moduļa pievienošana lapā

Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jauns fragments** atlasiet moduli **Grozs**.
1. Sadaļā **Fragmenta nosaukums** ievadiet nosaukumu **Groza fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Grozs**.
1. Rekvizītu rūts labajā pusē atlasiet zīmuļa simbolu, ievadiet virsraksta tekstu laukā un pēc tam atlasiet atzīmes simbolu.
1. Slotā **Grozs** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veikalu atlasītājs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet veidnes nosaukumu.
1. Struktūras kokā atlasiet slotu **Pamatteksts**, atlasiet daudzpunktess (**...**), un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Atlasīt fragmentu** atlasiet fragmentu **Groza fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni, ievadiet lapas nosaukumu un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md)

[Izveidot tiešsaistes funkcionalitātes profilu](online-functionality-profile.md)
