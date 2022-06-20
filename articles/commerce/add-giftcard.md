---
title: Dāvanu kartes modulis
description: Šajā rakstā ir ietverti dāvanu karšu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc3d51b9891469b8bb0fa38ae2bcd0b27eee56f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869494"
---
# <a name="gift-card-module"></a>Dāvanu kartes modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietverti dāvanu karšu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem. Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes. SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju. Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).

> [!NOTE]
> SVS un Givex dāvanu karšu izrakstīšanas atbalsts norēķinu plūsmas laikā ir pieejams Dynamics 365 Commerce 10.0.11 laidienā. 

Ir pieejami divi dāvanu kartes moduļi:

- **Dāvanu karte** – Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu. 
- **Dāvanu kartes bilances pārbaude** – Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci. Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.

> [!NOTE]
> Dāvanu kartes bilances pārbaudes modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.

Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.

![Dāvanu kartes moduļa piemērs.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

- **Rādīt papildu laukus** – šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma. Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu. Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.

    Tālāk ir norādītas atbalstītās vērtības:

    - PIN
    - Beigu datums
    - PIN un beigu datums 
    - Neviens

- **Iespējojiet vieslietotājiem** - ja šis rekvizīts ir iespējots, viesa lietotāji var izpirkt vai pārbaudīt dāvanu karšu bilances. Šis rekvizīts pieprasa, lai programmā Commerce headquarters tiktu iespējota anonīma (viesa) piekļuve dāvanu kartēm. Papildinformāciju skatiet sadaļā [Dāvanu karšu maksājumu iespējošana viesa norēķiniem](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Rekvizīts **Iespējot vieslietotājiem** ir pieejams kā Commerce 10.0.21 laidiena versijā. Nepieciešams, lai būtu instalēta Commerce moduļa bibliotēkas pakotnes versija 9.31.

## <a name="site-settings-for-gift-card-modules"></a>Vietas iestatījumi dāvanu karšu moduļiem

Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**. Šis iestatījums atbalsta trīs vērtības:
- **Dynamics 365 dāvanu karte** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.
- **SVS un GIVEX dāvanu kartes** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.
- **Dynamics 365, SVS un GIVEX dāvanu kartes** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.

> [!IMPORTANT]
> Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.11 versijā, un tie ir nepieciešami tikai tad, ja ir nepieciešams atbalsts SVS vai Givex dāvanu kartēm. Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Paplašināt iekšējās dāvanu kartes, kas ir izmantojamas E-commerce veikalos

Pēc noklusējuma iekšējās dāvanu kartes nav optimizētas izmantošanai E-commerce veikalos. Tāpēc, pirms atļaut maksājumu veikšanai izmantot iekšējās dāvanu kartes, tās ir jākonfigurē ar paplašinājumiem, kas palīdz padarīt tās drošākas. Šeit ir dāvanu karšu zonas, kas jāpaplašina, pirms atļaujat iekšējās dāvanu kartes izmantot ražošanā:

- **Dāvanu kartes numurs** — numuru sērijas tiek izmantotas, lai ģenerētu dāvanu karšu numurus iekšējām dāvanu kartēm. Tā kā numuru sērijas var viegli prognozēt, ir jāpaplašina dāvanu karšu numuru ģenerēšana, lai izsniegtajiem dāvanu karšu numuriem tiktu izmantotas nejaušā veidā kriptogrāfiski drošas virknes.
- **GetBalance** - **GetBalance** API tiek izmantots, lai iegūtu dāvanu kartes bilances. Pēc noklusējuma šis API ir publisks. Ja PIN kods nav nepieciešams, lai iegūtu dāvanu karšu bilances, pastāv risks, ka uzbrucējs var izmantot **GetBalance** API, lai mēģinātu uzmeklēt dāvanu karšu numurus, kuriem ir bilances. Ieviešot gan PIN prasības iekšējām dāvanu kartēm, gan API droseli, jūs varat palīdzēt samazināt risku.
- **PIN** — pēc noklusējuma iekšējās dāvanu kartes neatbalsta PIN. Ir jāpaplašina iekšējās dāvanu kartes tā, lai būtu nepieciešams PIN, lai meklētu bilances. Šo funkcionalitāti var izmantot arī, lai bloķētu dāvanu kartes pēc neveiksmīgiem mēģinājumiem ievadīt PIN.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Iespējot dāvanu karšu maksājumus viesa norēķināšanai

Pēc noklusējuma dāvanu karšu maksājumi nav iespējoti viesa (anonīma) norēķināšanai. Lai iespējotu tos, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanālu iestatījumi \> POS iestātīšana \> POS \> POS operacijas**.
1. Atlasiet un turiet režģa virsrakstu (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet **Ievietot kolonnas**.
1. Dialoglodziņā **Ievietot kolonnas** atzīmējiet izvēles rūtiņu **AllowAnonymousAccess**.
1. Atlasiet **Atjaunināt**.
1. Operācijām **520** (Dāvanu kartes bilance) un **214** iestatiet **AllowAccessmousAccess** vērtību uz **1**.
1. Atlasiet **Saglabāt**.
1. Palaidiet plānotāja darbu **1090**, lai sinhronizētu izmaiņas ar kanālu datu bāzi. 

## <a name="add-a-gift-card-module-to-a-page"></a>Dāvanu kartes moduļa pievienošana lapā

Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
