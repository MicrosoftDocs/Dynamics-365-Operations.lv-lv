---
title: Krājumu redzamības rezervācija
description: Šajā tēmā ir aprakstīts, kā iestatīt rezervēšanas līdzekli, lai izveidotu rezervācijas, patērētās rezervācijas un/vai atceltu norādītos krājumu daudzumus, izmantojot krājumu redzamību.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345153"
---
# <a name="inventory-visibility-reservations"></a>Krājumu redzamības rezervācija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt rezervēšanas līdzekli, lai izveidotu rezervācijas, patērētās rezervācijas un/vai atceltu norādītos krājumu daudzumus, izmantojot krājumu redzamību.

Rezervācijas iezīmē krājumu daudzumu, kas tiks izmantots turpmāk. Veidojot rezervāciju, sistēma neļauj citiem pasūtījumiem rezervēt vai patērēt rezervētās preces, līdz rezervēšana ir patērēta vai nerezervēta. Rezervācijas tiek izveidotas, patērētas un atceltas, izmantojot API izsaukumus Krājumu redzamības pakalpojumam.

Varat pēc izvēles iestatīt sistēmu Microsoft Dynamics 365 Supply Chain Management (un citas trešās personas) tā, lai automātiski kompensētu daudzumu, kas ir rezervēts, izmantojot Krājumu redzamību. Korespondējošais daudzums tiek dzēsts no rezervāciju ierakstiem Krājumu redzamībai.

Ja ieslēdzat rezervācijas iespēju, Supply Chain Management automātiski kļūst gatava korespondējošām rezervācijām, kas veiktas, izmantojot Krājumu redzamību.

> [!NOTE]
> Korespondējošai funkcionalitātei nepieciešama Supply Chain Management versija 10.0.22 vai jaunāka. Ja vēlaties izmantot Krājumu redzamības rezervācijas, ir ieteicams gaidīt, līdz Supply Chain Management ir jaunināta uz 10.0.22 vai jaunāku versiju.

## <a name="turn-on-the-reservation-feature"></a>Ieslēgt rezervēšanas līdzekli

Lai ieslēgtu šo līdzekli, veiciet tālāk minētās darbības.

1. Programmā Power Apps atveriet **Krājumu redzamība**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Līdzekļu pārvaldība** ieslēdziet līdzekli *OnHandReservation*.
1. Pierakstieties Supply Chain Management.
1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu un noliktavas pārvaldības parametri**.
1. Sadaļā **Rezervācijas korespondējošais konts** iestatiet opciju **Aktivizēt rezervāciju korespondējošo kontu** uz *Jā*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Rezervācijas izmantošana Krājumu redzamības pievienojumprogrammai

Izsaucot rezervācijas API, sistēma atzīmē norādīto preču un daudzumu rezervāciju. Jums ir jādefinē rezervāciju hierarhija un jāgrāmato pieprasījumi, kas atbilst rezervāciju hierarhijai. Pēc tam rezervācijas var veikt, tieši nosaucot rezervēšanas API.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurēt rezervāciju hierarhiju

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija var atšķirties no indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai.

Lai konfigurētu vieglās rezervācijas hierarhiju programmā Power Apps, atveriet lapu **Konfigurācija** un pēc tam cilnē **Vieglās rezervācijas kartēšana** iestatiet rezervāciju hierarhiju, pievienojot un/vai modificējot dimensijas un to hierarhijas līmeņus.

### <a name="call-the-reservation-api"></a>Izsaukt rezervēšanas API

Rezervācijas tiek veiktas krājumu redzamības pakalpojumā, iesniedzot GRĀMATOŠANAS pieprasījumu pakalpojuma vietrāža URL, piemēram, `/api/environment/{environment-ID}/onhand/reserve`.

Rezervēšanai pieprasījuma pamattekstam ir jāietver organizācijas ID, preces ID, rezervētie daudzumi un dimensijas. Pieprasījums ģenerē unikālu rezervācijas ID katram rezervācijas ierakstam. Rezervācijas ierakstā ir ietverta preces ID un dimensiju unikālā kombinācija.

Šeit parādīts pieprasījuma pamatteksta piemērs atsaucei.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Korespondējošo kontu rezervācijas programmā Supply Chain Management

Krājumu darbību statusiem, kas ietver noteiktu rezervju korespondējošo modifikatoru, darbības atjaunināšana nobīdīs atbilstošo rezervācijas ierakstu, ja ir spēkā visi šie nosacījumi:

- Krājumu transakcijas rezervācijas ID atbilst rezervēšanas ID rezervēšanas ierakstam Krājumu redzamības pakalpojumā.
- Krājumu transakcijas rezervācijas ID atbilst rezervēšanas ID rezervēšanas ierakstam Krājumu redzamības pakalpojumā.
- Krājumu darbību statusa izmaiņas izraisa korespondējošās darbības rezervācijām, ja krājuma darbības statuss atspoguļo faktu, ka pasūtījuma process ir pabeigts vai izlaists.

Korespondējošais daudzums seko krājumu daudzumam, kas norādīts krājumu darbībās. Korespondējošā darbība stājas spēkā tikai tad, ja Krājumu redzamības pakalpojumā saglabājas rezervētais daudzums.

> [!NOTE]
> Korespondējošā konta funkcionalitāte ir pieejama no versijas 10.0.22

### <a name="set-up-the-reserve-offset-modifier"></a>Iestatīt rezervju korespondējošo kontu modifikatoru

Rezerves korespondējošā konta modifikators nosaka pasūtījuma apstrādes stadiju, kas aktivizē korespondējošās darbības. Statusu izseko pasūtījuma krājumu darbības statuss. Lai iestatītu rezervēšanas korespondējošā konta modifikatoru, veiciet šīs darbības.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu redzamības parametri \> Rezervēšanas korespondējošais konts**.
1. Laukam **Darba pasūtījuma veids** jābūt iestatītam uz vienu no tālāk minētajām vērtībām:

    - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu.
    - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process.

### <a name="set-up-reservation-ids"></a>Rezervāciju ID iestatīšana

Rezervācijas ID unikāli atzīmē rezervēšanas ierakstu Krājumu redzamībai. Programmā Supply Chain Management lietotāji ievieto rezervācijas pasūtījuma rindās, lai atzīmētu korespondējošo kontu atbilstošajam rezervēšanas ierakstam.

Lai iestatītu rezervācijas ID programmā Supply Chain Management, sekojiet šiem soļiem.

1. Atveriet pārdošanas pasūtījumu (piemēram, no lapas **Visi pārdošanas pasūtījumi**).
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet pasūtījuma rindu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** rīkjoslā atlasiet **Atjaunināt rindu \> Krājums \> Krājumu redzamības integrācija**.
1. Ievadiet atbilstīgos rezervēšanas ID.

Krājuma statusa maiņa atbilst korespondējošā modifikatora iestatījumam.
