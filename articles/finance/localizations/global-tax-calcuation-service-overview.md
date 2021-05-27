---
title: Nodokļu aprēķins (priekšskatījums)
description: Šajā tēmā ir izskaidrots nodokļu aprēķina iespēju vispārējais tvērums un iezīmes.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021936"
---
# <a name="tax-calculation-preview"></a>Nodokļu aprēķins (priekšskatījums)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Nodokļu aprēķins ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu. Nodokļu programma ir pilnībā konfigurējama. Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu. Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.

Nodokļu aprēķins ir integrēts ar Dynamics 365 Finance un Dynamics 365 Supply Chain Management. Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.

Nodokļu aprēķins ir uz mikroservisu balstīta nodokļu programma, kas piedāvā eksponenciālu mērogošanu. Tas var palīdzēt veikt šādus uzdevumus:

- Konfigurējiet nodokļu aprēķinu, izmantojot Regulatory Configuration Service (RCS). RCS ir uzlabota elektronisko pārskatu (Electronic reporting - ER) veidotāja versija un ir pieejama kā savrups pakalpojums.
- Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu kodus un likmes.
- Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu reģistrācijas numuru.
- Konfigurējiet nodokļu aprēķina veidotāju, lai definētu formulas un nosacījumus.
- Kopīgojiet nodokļu noteikšanas un aprēķināšanas risinājumu visām juridiskajām personām.

Lai izmantotu nodokļu aprēķināšanas pakalpojumu, instalējiet nodokļu aprēķina pakalpojuma pievienojumprogrammu savam projektam pakalpojumā Microsoft Dynamics Lifecycle Services (LCS). Pēc tam pabeidziet iestatīšanu RCS un iespējojiet nodokļu aprēķināšanas pakalpojumu Finance un Supply Chain Management. Papildinformāciju skatiet sadaļā [Sākt darbu ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Pieejamība

Nodokļu aprēķins ir pieejams tikai smilškastes vidē un izvēlētajiem debitoriem, izmantojot publisku priekšskatījuma programmu. Visbeidzot, tas kļūs plaši pieejams visiem debitoriem un ražošanas vidēs.

Arī turpmāk tiks piegādāti jauni līdzekļi, tāpēc noteikti iepazīstieties ar visjaunāko dokumentāciju, lai uzzinātu par atbalstīto funkciju segumu un darbības jomu.

Nodokļu aprēķins ir izvietots tālāk redzamajās Azure ģeogrāfiskās lapās. Tas tiks izvietots arī vairākās Azure ģeogrāfiskās vietās atbilstoši debitoru vajadzībām:

- ASV
- Eiropa

> [!NOTE]
> Nodokļu aprēķins neatbalsta Dynamics 365 lokālas izvietošanas. Tas neatbalsta arī agrākas versijas, piemēram, Dynamics AX 2012.

## <a name="feature-highlights"></a>Līdzekļu iezīmēšana

- Konfigurējama nodokļu matrica, lai automātiski noteiktu un aprēķinātu nodokli
- Atbalstīt vairākus nodokļa reģistrācijas numurus
- Pārsūtīšanas pasūtījuma atbalsts nodokļu noteikšanai un aprēķinam
- Pārsūtīšanas pasūtījuma atbalsts vairāku nodokļa reģistrācijas numuru noteikšanai

## <a name="supported-transactions"></a>Atbalstītie darījumi

Nodokļu aprēķinu var iespējot juridiska persona un darījums. Tālāk ir norādīti atbalstītie darījumi.

- Pārdošanas process

    - Pārdošanas piedāvājums
    - Pārdošanas pasūtījums
    - Apstiprināšana
    - Izdošanas saraksts
    - Pavadzīme
    - Pārdošanas rēķins
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Virsraksta papildmaksa
    - Rindas papildmaksas pieprasījums

- Pirkšanas process

    - Pirkuma pasūtījums
    - Apstiprināšana
    - Saņemšanas saraksts
    - Produktu ieejas plūsma
    - Pirkšanas rēķins
    - Virsraksta papildmaksas pieprasījums
    - Rindas papildmaksas pieprasījums
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Pirkšanas pieprasījums
    - Pirkšanas pieprasījuma rindas papildmaksas pieprasījums
    - Piedāvājuma pieprasījums
    - Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums
    - Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums

- Krājumu process

    - Pārvietošanas pasūtījums – nosūtīšana
    - Pārsūtīšanas pasūtījums – saņemšana

## <a name="related-resources"></a>Saistītie resursi

[Darba sākšana ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md)

[Vairāki PVN reģistrācijas numuri](./emea-multiple-vat-registration-numbers.md)

[Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam](./tasks/tax-feature-support-for-transfer-order.md)

[Kā veidot paplašinājumu nodokļu pakalpojumā](./tax-service-add-data-fields-tax-integration-by-extension.md)