---
title: Krājumu redzamības pievienojumprogrammas pārskats
description: Šajā tēmā skaidrots, kas ir Krājumu redzamība un apraksta tās funkcijas.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dfc1bc0d457d0b0b2632aa2e2e5ba6a3c2f3fae7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575175"
---
# <a name="inventory-visibility-add-in-overview"></a>Krājumu redzamības pievienojumprogrammas pārskats

[!include [banner](../includes/banner.md)]

Krājumu uztveramības pievienojumprogramma (vēl dēvēta par *Krājumu redzamību*) ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību. Tāpēc tā nodrošina globālu krājumu skatījumu.

Ārējās sistēmas piekļūst pakalpojumam ar RESTful API. Tādā veidā tie var vai nu vaicāt rīcībā esošo informāciju par dotajām dimensiju kopām, vai veikt izmaiņas krājumos dažādos pielāgotos datu avotos.

Kā mikropakarakstu, kas ir izveidots Microsoft Dataverse, Krājumu redzamība nodrošina paplašināmību. Jūs varat izmantot Power Apps, lai izveidotu programmas. Varat lietot arī Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa prasībām.

Krājumu redzamību var integrēt ar vairākām trešās personas sistēmām, iestatot konfigurācijas opcijas standartizētām krājumu dimensijām un iestatot darbību tipus. Krājumu redzamība atbalsta arī pielāgotu paplašināmību, izmantojot konfigurējamus aprēķinātos daudzumus.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Pievienojumprogrammas Krājumu redzamība integrācija ar Dynamics 365 Supply Chain Management

Integrētais risinājums izvelk krājumu datus no Dynamics 365 Supply Chain Management un nepārtraukti izseko krājumu izmaiņas. Papildinformāciju skatiet sadaļā [Instalēt un iestatīt krājuma redzamību](inventory-visibility-setup.md) un [Krājuma redzamības konfigurēšana](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Iegūt krājumu globālo skatu

Integrētais risinājums ļauj definēt savus datu avotus un centralizēt krājumu datus. Papildinformāciju skatiet sadaļā [Krājuma redzamības konfigurēšana](inventory-visibility-configuration.md).

Ir divas pieejas jūsu krājumu skatīšanai:

- Iesniedziet vaicājumu, izmantojot augstas veiktspējas API. Šis API var atgriezt tuvu reāllaika krājumu datus tieši no kešatmiņas instances. Līgumus un paraugus var atrast [Krājumu redzamības publiskā API](inventory-visibility-api.md).
- Skatīt skatīt rīcībā esošo krājumu sarakstu. Šis saraksts periodiski tiek sinhronizēts no kešatmiņas instances un ir redzams Dataverse. Papildinformāciju skatiet [Krājumu uztveramības programma](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Vieglās rezervācijas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Vieglā rezervācija tiek piemērota, kad uzņēmumam jārezervē noteikts preču daudzums, lai atbalstītu, piemēram, pārdošanas pasūtījuma izpildi, kas novērš pārdošanu pārāk daudz. Kad pārdošanas pasūtījums ir izveidots un apstiprināts Supply Chain Management vai citās pasūtījumu pārvaldības sistēmās, pieprasījums rezervēt daudzumu tiek nosūtīts uz Krājumu redzamību. Krājumu redzamība ļauj rezervēt preces, kurām ir dimensijas detaļas un specifiski krājumu darbību tipi. (Papildinformāciju skatiet [Krājumu redzamības programma](inventory-visibility-power-platform.md).) Kad daudzums ir veiksmīgi rezervēts, rezervācijas ID tiek atgriezts. Šo rezervācijas ID varat izmantot, lai saistītu atpakaļ ar oriģinālo pasūtījumu Supply Chain Management vai citās pasūtījumu pārvaldības sistēmās.

Šī funkcionalitāte ir izveidota, lai rezervācija Krājumu redzamībā nemainīs kopējo daudzumu. Tā vietā tas tikai atzīmē rezervēto daudzumu. (Šī iemesla dēļ to sauc par *vieglo rezervāciju*.) Viegli rezervēto daudzumu var kompensēt, kad preces tiek patērētas Supply Chain Management vai trešās puses sistēmā, vēlreiz izsaucot API, lai veiktu daudzuma ieturējumu un atjauninātu kopējo daudzumu Krājumu redzamībai. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
