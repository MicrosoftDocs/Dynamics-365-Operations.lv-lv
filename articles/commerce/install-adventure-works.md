---
title: Adventure Works tēmas instalēšana
description: Šajā tēmā aprakstīts, kā instalēt Adventure Works tēmu Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655852"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works tēmas instalēšana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā instalēt Adventure Works tēmu Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works tēma un moduļi ir pieejami Dynamics 365 Commerce versijas 10.0.20 laidienā. Tās ir pieejamas no Microsoft AppSource.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms Adventure Works tēmas instalēšanas ir nepieciešama Dynamics 365 Commerce vide (Commerce versija 10.0.20 vai jaunāka), kas iekļauj Retail Cloud Scale Unit (RCSU), Commerce tiešsaistes programmatūras izstrādes komplektu (SDK) un Commerce moduļu bibliotēku. Informāciju par To, kā instalēt Commerce SDK un moduļu bibliotēku, skatiet [SDK un moduļa bibliotēkas atjauninājumus](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Instalēšanas darbības

### <a name="install-the-adventure-works-theme-in-your-application"></a>Instalējiet Adventure Works tēmu savā programmā

Adventure Works tēmu pakotne ir pieejama plūsmā **dynamics365-commerce**, kā **@msdyn365-commerce-theme/adventureworks-theme-kit**. Tomēr, lai arī Adventure Works tēmu pakotne ir daļa no šīs plūsmas, tā atrodas citā nosaukumvietā. Tādēļ jums ir jāveic šīs darbības, lai pievienotu reģistra ierakstus nosaukumvietai.

1. Atjauniniet failu **.npmrc** tā, lai tajā būtu šāds reģistra ieraksts (ja ievadne vēl nav iekļauta):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Atjauniniet failu **.yarnrc** tā, lai tajā būtu šāds reģistra ieraksts (ja ievadne vēl nav iekļauta):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Lai instalētu pakotni vietējā vidē, komandu uzvednē izpildiet tālāk norādīto komandu. Šī komanda automātiski atjaunina package.json failu, lai tas ietver atkarību.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

Failā **package.json** atjauniniet tēmas versiju uz noteiktu versiju.

> [!IMPORTANT]
> - Tēmas versijai jāatbilst moduļa bibliotēkas versijai, lai nodrošinātu, ka visi līdzekļi darbojas, kā paredzēts. 
> - Commerce moduļu bibliotēkas un SDK minimālajai versijai jābūt 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Fontu failu pievienošana Adventure Works tēmai

Kad jūsu programmā ir instalēta Adventure Works tēma, jāpievieno tam nepieciešamie fontu faili. Lai pabeigtu šo darbību, kopējiet visus fontu failus no **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** uz partnera programmas publiskās direktorijas ceļu **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Resursu iestatīšana Adventure Works tēmai

Nākošā darbība ir atjaunināt vajadzīgos noklusējuma resursus tēmai. Lai pabeigtu šo darbību, kopējiet saturu no globālā.json faila zem **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** uz partnera programmas global.json failu zem **\src\resources\modules**. Ja **\src\resources** mērķa direktorijs nepastāv, to pilnībā var kopēt no **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** avota direktorija uz **\src** mērķa direktoriju.

### <a name="pull-updates-and-validate-the-theme"></a>Vilkt atjauninājumus un apstiprināt tēmu

Informāciju par to, kā vilkt jaunāko SDK, moduļa bibliotēku un citus atkarību atjauninājumus, skatiet "Vilkt atjauninājumus" sadaļā [SDK un moduļa bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#pull-updates).

Kad jaunākās atkarības ir vilktas uz leju, ir iespējams palaist komandu **dzijas sākums**, lai startējiet Zara serveri savā izstrādes vidē un pārbaudītu jauno Adventure Works tēmu. Pārlūkojiet programmu lokāli, izmantojot vaicājuma virknes parametru `?theme=adventureworks` (piemēram, `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Papildu resursi

[Adventure Works tēma](adventure-works-theme.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
