---
title: Krājumu redzamības pievienojumprogrammas pārskats
description: Šajā tēmā skaidrots, kas ir Krājumu redzamība un apraksta tās funkcijas.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: defbcdc7ada4471345f8c728522e15f16a8bec8f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344292"
---
# <a name="inventory-visibility-add-in-overview"></a>Krājumu redzamības pievienojumprogrammas pārskats

[!include [banner](../includes/banner.md)]

Krājumu uztveramības pievienojumprogramma (vēl dēvēta par *Krājumu redzamību*) ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību. Tāpēc tā nodrošina globālu krājumu skatījumu.

Ārējās sistēmas piekļūst pakalpojumam ar RESTful API. Tādā veidā tie var vai nu vaicāt rīcībā esošo informāciju par dotajām dimensiju kopām, vai veikt izmaiņas krājumos dažādos pielāgotos datu avotos.

Kā mikropakarakstu, kas ir izveidots Microsoft Dataverse, Krājumu redzamība nodrošina paplašināmību. Jūs varat izmantot Power Apps, lai izveidotu programmas. Varat lietot arī Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa prasībām.

Krājumu redzamību var integrēt ar vairākām trešās personas sistēmām, iestatot konfigurācijas opcijas standartizētām krājumu dimensijām un iestatot darbību tipus. Krājumu redzamība atbalsta arī pielāgotu paplašināmību, izmantojot konfigurējamus aprēķinātos daudzumus.

## <a name="supported-features"></a>Atbalstītie līdzekļi

### <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Pievienojumprogrammas Krājumu redzamība integrācija ar Dynamics 365 Supply Chain Management

Integrētais risinājums izvelk krājumu datus no Dynamics 365 Supply Chain Management un nepārtraukti izseko krājumu izmaiņas. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas iestatīšana](inventory-visibility-setup.md).

### <a name="get-a-global-view-of-inventory"></a>Iegūt krājumu globālo skatu

Integrētais risinājums ļauj definēt savus datu avotus un centralizēt krājumu datus. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas konfigurēšana](inventory-visibility-configuration.md).

Ir divas pieejas jūsu krājumu skatīšanai:

- Iesniedziet vaicājumu, izmantojot augstas veiktspējas API. Šis API var atgriezt tuvu reāllaika krājumu datus tieši no kešatmiņas instances. Līgumus un paraugus var atrast [Krājumu redzamības publiskā API](inventory-visibility-api.md).
- Skatīt skatīt rīcībā esošo krājumu sarakstu. Šis saraksts periodiski tiek sinhronizēts no kešatmiņas instances un ir redzams Dataverse. Papildinformāciju skatiet [Krājumu uztveramības programma](inventory-visibility-power-platform.md).

### <a name="soft-reservations"></a>Vieglās rezervācijas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Vieglā rezervācija tiek piemērota, kad uzņēmumam jārezervē noteikts preču daudzums, lai atbalstītu, piemēram, pārdošanas pasūtījuma izpildi, kas novērš pārdošanu pārāk daudz. Kad pārdošanas pasūtījums ir izveidots un apstiprināts Supply Chain Management vai citās pasūtījumu pārvaldības sistēmās, pieprasījums rezervēt daudzumu tiek nosūtīts uz Krājumu redzamību. Krājumu redzamība ļauj rezervēt preces, kurām ir dimensijas detaļas un specifiski krājumu darbību tipi. (Papildinformāciju skatiet [Krājumu redzamības programma](inventory-visibility-power-platform.md).) Kad daudzums ir veiksmīgi rezervēts, rezervācijas ID tiek atgriezts. Šo rezervācijas ID varat izmantot, lai saistītu atpakaļ ar oriģinālo pasūtījumu Supply Chain Management vai citās pasūtījumu pārvaldības sistēmās.

Šī funkcionalitāte ir izveidota, lai rezervācija Krājumu redzamībā nemainīs kopējo daudzumu. Tā vietā tas tikai atzīmē rezervēto daudzumu. (Šī iemesla dēļ to sauc par *vieglo rezervāciju*.) Viegli rezervēto daudzumu var kompensēt, kad preces tiek patērētas Supply Chain Management vai trešās puses sistēmā, vēlreiz izsaucot API, lai veiktu daudzuma ieturējumu un atjauninātu kopējo daudzumu Krājumu redzamībai. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
