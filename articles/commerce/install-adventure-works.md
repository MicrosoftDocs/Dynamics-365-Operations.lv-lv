---
title: Adventure Works dizaina instalēšana
description: Šajā rakstā ir aprakstīts, kā instalēt Adventure Works tēmu Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274291"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works dizaina instalēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā instalēt Adventure Works tēmu Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works tēma un moduļi ir pieejami Dynamics 365 Commerce versijas 10.0.20 laidienā. Tās ir pieejamas no Microsoft AppSource.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms Adventure Works tēmas instalēšanas ir nepieciešama Dynamics 365 Commerce vide (Commerce versija 10.0.20 vai jaunāka), kas iekļauj Retail Cloud Scale Unit (RCSU), Commerce tiešsaistes programmatūras izstrādes komplektu (SDK) un Commerce moduļu bibliotēku. Informāciju par To, kā instalēt Commerce SDK un moduļu bibliotēku, [skatiet izstrādes vides iestatīšana](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Instalēšanas darbības

### <a name="install-the-adventure-works-theme-in-your-application"></a>Instalējiet Adventure Works tēmu savā programmā

Adventure Works tēmu pakotne ir pieejama plūsmā **dynamics365-commerce**, kā **@msdyn365-commerce-theme/adventureworks-theme-kit**. Tomēr, lai arī Adventure Works tēmu pakotne ir daļa no šīs plūsmas, tā atrodas citā nosaukumvietā. Tādēļ jums ir jāveic šīs darbības, lai pievienotu reģistra ierakstus nosaukumvietai.

1. Atjauniniet failu **.npmrc** tā, lai tajā būtu šāds reģistra ieraksts (ja ievadne vēl nav iekļauta):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Atjauniniet failu **.yarnrc** tā, lai tajā būtu šāds reģistra ieraksts (ja ievadne vēl nav iekļauta):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Lai instalētu pakotni vietējā vidē, palaidiet komandu no komandas uzvednes, `yarn add THEME_PACKAGE@VERSION`**kur THEME_PACKAGE** ir tēmu pakotne (@msdyn365-commerce-theme/adventureworks-theme-kit) **un VERSIJA** ir izmantotās moduļu bibliotēkas versijas numurs. Ir svarīgi, lai tēmas pakotnes versijas un moduļu bibliotēka saskan. Lai atrastu pareizo izmantojamais moduļa bibliotēkas versijas numuru, atveriet package.json **failu un nosakiet sākuma pakotnes** **vērtību zem atkarības sadaļas**. Šajā piemērā package.json fails izmanto moduļa bibliotēkas versiju 9.32 Dynamics 365 Commerce, kas kartē uz versiju 10.0.22 izlaidi.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Šajā piemērā parādīts, kā izpildīt komandu `yarn add`, lai pievienotu Adventure Works tēmas versiju 9.32. Komanda automātiski atjaunina package.json failu, lai tas ietver atkarību.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Papildinformāciju par moduļa bibliotēkas versijas atjaunināšanu skatiet SDK un [moduļu bibliotēkas atjauninājumos](e-commerce-extensibility/sdk-updates.md). 

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
