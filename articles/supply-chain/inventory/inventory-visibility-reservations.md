---
title: Inventory Visibility rezervācijas
description: Šajā rakstā ir aprakstīts, kā iestatīt rezervēšanas līdzekli, lai izveidotu rezervācijas, patērētas rezervācijas un/vai atceltu norādītos krājumu daudzumus, izmantojot krājumu redzamību.
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
ms.openlocfilehash: 3b74907709ab97ddf4cc829dba324df213ca229f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895733"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility rezervācijas

[!include [banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā iestatīt rezervēšanas līdzekli, lai izveidotu rezervācijas, patērētas rezervācijas un/vai atceltu norādītos krājumu daudzumus, izmantojot krājumu redzamību.

Rezervācijas iezīmē krājumu daudzumu, kas tiks izmantots turpmāk. Veidojot rezervāciju, sistēma neļauj citiem pasūtījumiem rezervēt vai patērēt rezervētās preces, līdz rezervēšana ir patērēta vai nerezervēta. Rezervācijas tiek izveidotas, patērētas un atceltas, izmantojot API izsaukumus Krājumu redzamības pakalpojumam.

Varat pēc izvēles iestatīt sistēmu Microsoft Dynamics 365 Supply Chain Management (un citas trešās personas) tā, lai automātiski kompensētu daudzumu, kas ir rezervēts, izmantojot Krājumu redzamību. Korespondējošais daudzums tiek dzēsts no rezervāciju ierakstiem Krājumu redzamībai.

Ja ieslēdzat rezervācijas iespēju, Supply Chain Management automātiski kļūst gatava korespondējošām rezervācijām, kas veiktas, izmantojot Krājumu redzamību.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Rezervācijas līdzekļa iespējošana un iestatīšana

Lai ieslēgtu šo līdzekli, veiciet tālāk minētās darbības.

1. Piesakieties Power Apps un atveriet **Inventory Visibility**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Līdzekļu pārvaldība** ieslēdziet līdzekli *OnHandReservation*.
1. Pierakstieties Supply Chain Management.
1. Dodieties uz **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietu un iespējojiet *Inventory Visibility integrāciju ar rezervācijas nobīdes* līdzekli (vajadzīga 10.0.22. vai jaunāka versija).
1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**, atveriet **Rezervāciju nobīdes** cilni un veiciet šādus iestatījumus:
    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervāciju nobīdes pārveidotājs** — Atlasiet krājuma transakcijas statusu, kas nobīdīs Inventory Visibility veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Izvēlieties vienu no šīm:
        - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu. Nobīžu daudzums būs izveidotā pasūtījuma daudzums.
        - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process. Novīdes daudzums būs daudzums, kurā krājuma transakcijas statuss atbilstoŠajā pasūtījuma rindā tiek mainīts no *Pasūtījumā* uz *Rezervēts pasūtījums* (vai uz vēlāku statusu).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Rezervācijas izmantošana Krājumu redzamības pievienojumprogrammai

Izsaucot rezervācijas API, sistēma atzīmē norādīto preču un daudzumu rezervāciju. Jums ir jādefinē rezervāciju hierarhija un jāgrāmato pieprasījumi, kas atbilst rezervāciju hierarhijai. Pēc tam rezervācijas var veikt, tieši nosaucot rezervēšanas API.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurēt rezervāciju hierarhiju

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija var atšķirties no indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai.

Lai konfigurētu vieglās rezervācijas hierarhiju Power Apps, atveriet lapu **Konfigurācija** un cilnē **Vieglās rezervācijas hierarhija** iestatiet rezervācijas hierarhiju, pievienojot un/vai pārveidojot dimensijas un to hierarhiju līmeņus.

Jūsu vieglās rezervācijas hierarhijai vajadzētu saturēt komponentus `SiteId` un `LocationId`, jo tie veido dalīšanās konfigurāciju.

Papildinformāciju par rezervāciju konfigurēšanu skatiet rakstā [Rezervāciju konfigurācija](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Izsaukt rezervēšanas API

Rezervācijas tiek veiktas krājumu redzamības pakalpojumā, iesniedzot GRĀMATOŠANAS pieprasījumu pakalpojuma vietrāža URL, piemēram, `/api/environment/{environment-ID}/onhand/reserve`.

Rezervēšanai pieprasījuma pamattekstam ir jāietver organizācijas ID, preces ID, rezervētie daudzumi un dimensijas. Pieprasījums ģenerē unikālu rezervācijas ID katram rezervācijas ierakstam. Rezervācijas ierakstā ir ietverta preces ID un dimensiju unikālā kombinācija.

Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

Ja vēlaties atcelt rezervāciju vai atsaukt konkrētu krājuma daudzumu rezervāciju, iestatiet daudzumu uz negatīvu vērtību, un iestatiet parametru `ifCheckAvailForReserv` uz vērtību `False`, lai izlaistu validāciju.

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

### <a name="set-up-the-reservation-offset-modifier"></a>Rezervācijas nobīdes pārveidotāja iestatīšana

Ja vēl to neesat izdarījuši, iestatiet rezervācijas pārveidotāju, kā aprakstīts sadaļā [Rezervācijas līdzekļa ieslēgšana un iestatīšana](#turn-on).

### <a name="set-up-reservation-ids"></a>Rezervāciju ID iestatīšana

Rezervācijas ID unikāli atzīmē rezervēšanas ierakstu Krājumu redzamībai. Programmā Supply Chain Management lietotāji ievieto rezervācijas pasūtījuma rindās, lai atzīmētu korespondējošo kontu atbilstošajam rezervēšanas ierakstam.

Lai iestatītu rezervācijas ID programmā Supply Chain Management, sekojiet šiem soļiem.

1. Atveriet pārdošanas pasūtījumu (piemēram, no lapas **Visi pārdošanas pasūtījumi**).
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet pasūtījuma rindu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** rīkjoslā atlasiet **Atjaunināt rindu \> Krājums \> Krājumu redzamības integrācija**.
1. Ievadiet atbilstīgos rezervēšanas ID.

Krājuma statusa maiņa atbilst korespondējošā modifikatora iestatījumam.
