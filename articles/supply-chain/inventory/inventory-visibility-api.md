---
title: Krājumu redzamības publiskie API
description: Šajā rakstā ir aprakstīti publiskie API, kas tiek nodrošināti ar krājumu redzamību.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 14812fc201ba1038a78ea3317686dbe189ffa687
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423600"
---
# <a name="inventory-visibility-public-apis"></a>Krājumu redzamības publiskie API

[!include [banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti publiskie API, kas tiek nodrošināti ar krājumu redzamību.

Krājumu redzamības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus. Tas atbalsta četrus galvenos mijiedarbības tipus:

- Iegrāmatojot pievienojumprogrammas rīcībā esošās izmaiņas no ārējās sistēmas
- Rīcībā esošo krājumu daudzumu iestatīšana vai ignorēšana pievienojumprogrammai no ārējās sistēmas
- Iegrāmatojot pievienojumprogrammā rezervācijas notikumus no ārējās sistēmas
- Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas

Tālāk esošajā tabulā ir norādītas pieejamās API:

| Ceļš | Metode | Apraksts |
|---|---|---|
| /api/vide/{environmentId}/rīcībā esošs | Amats | [Izveidot vienu rīcībā esošo izmaiņu notikumu](#create-one-onhand-change-event) |
| /api/vide/{environmentId}/rīcībā esošs/lielapjoma | Amats | [Izveidot vairākus izmaiņu notikumus](#create-multiple-onhand-change-events) |
| /api/vide/{environmentId}/rīcībā esošs/{inventorySystem}/lielapjoma | Amats | [Iestatīt/ignorēt rīcībā esošos daudzumus](#set-onhand-quantities) |
| /api/vide/{environmentId}/rīcībā esošs/rezervēt | Amats | [Izveidot vienu rezervācijas notikumu](#create-one-reservation-event) |
| /api/vide/{environmentId}/rīcībā esošs/rezervēt/lielapjoma | Amats | [Izveidot vairākus rezervēšanas notikumus](#create-multiple-reservation-events) |
| /api/environment/{environmentId} onhand/unreserve | Grāmatot | [Atsaukt vienu rezervācijas notikumu](#reverse-one-reservation-event) |
| /api/environment/{environmentId} onhand/unreserve/bulk | Grāmatot | [Atsaukt vairākus rezervēšanas notikumus](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId} onhand/changeschedule | Grāmatot | [Izveidot vienu plānoto rīcībā esošo izmaiņu](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId} onhand/changeschedule/lielapjoma | Grāmatot | [Izveidot vairākas plānotas rīcībā esošo krājumu izmaiņas](inventory-visibility-available-to-promise.md) |
| /api/vide/{environmentId}/rīcībā esošs/indeksa vaicājums | Grāmatot | [Vaicājums, izmantojot grāmatošanas metodi](#query-with-post-method) |
| /api/vide/{environmentId}/rīcībā esošs | Iegūt | [Vaicājums, izmantojot iegūšanas metodi](#query-with-get-method) |
| /api/vide/sadalījums{environmentId}/sadalījums | Grāmatot | [Izveidot vienu piešķires notikumu](inventory-visibility-allocation.md#using-allocation-api) |
| /api/vide/{environmentId} sadalījums/atdalīšana | Grāmatot | [Izveidot vienu nesadalītu notikumu](inventory-visibility-allocation.md#using-allocation-api) |
| /api/vide/{environmentId} sadalījums/reallocate | Grāmatot | [Izveidot vienu no jauna pārceltiem notikumiem](inventory-visibility-allocation.md#using-allocation-api) |
| /api/vide/sadalījums{environmentId}/patērēšanas | Grāmatot | [Izveidot vienu patērēto notikumu](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/allocation{environmentId}/vaicājums | Grāmatot | [Vaicājuma sadalījuma rezultāts](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Ceļa {environmentId} daļa ir vides ID Microsoft Dynamics pakalpojumā Lifecycle Services (LCS).
> 
> Lielapjoma API var atgriezt maksimāli 512 ierakstus katram pieprasījumam.

Microsoft ir nodrošinājusi standarta *Pastnieka* pieprasījuma kolekciju. Jūs variet importēt šo kolekciju savā *Pastnieka* programmatūrā, izmantojot šādu koplietojamu saiti: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Atrast galapunktu atbilstoši Lifecycle Services videi

Krājumu redzamības mikropakalpojums ir izvietots Microsoft Azure Service Fabric vairākās atrašanās vietās un reģionos. Šobrīd nav centrālā galapunkta, kas var automātiski novirzīt jūsu pieprasījumu uz atbilstošo ģeogrāfisko vietu un reģionu. Tāpēc informācijas vienības jāveido vietrādī URL, izmantojot šādu modeli:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Reģiona īsais nosaukums var tikt atrasts Microsoft Dynamics Lifecycle Services (LCS) vidē. Tālāk esošajā tabulā ir norādīti pieejamie reģioni.

| Azure reģions        | Reģiona īsais nosaukums |
| ------------------- | ----------------- |
| Austrālijas austrumi      | eau               |
| Austrālijas dienvidaustrumi | seau              |
| Kanādas centrālā daļā      | cca               |
| Kanādas austrumi         | eca               |
| Ziemeļeiropa        | neu               |
| Rietumeiropa         | weu               |
| ASV austrumi             | eus               |
| ASV rietumi             | wus               |
| Lielbritānijas dienvidi            | suk               |
| Lielbritānijas rietumi             | wuk               |
| Japānas austrumu daļa          | ejp               |
| Japānas rietumu daļa          | wjp               |
| Brazīlijas dienvidu daļa        | sbr               |
| ASV dienvidu centrālā daļa    | scus              |

Salas numurs ir tas, kur LCS vide tiek izvietota pakalpojumā Service Fabric. Šobrīd nav veida, kā iegūt šo informāciju no lietotāja puses.

Microsoft ir izveidojis lietotāja interfeisu (UI) risinājumā Power Apps, lai varētu iegūt pilnu mikropakalpojuma galapunktu. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikācija

Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu redzamības pievienojumprogrammas publisko API. Tādēļ jums ir jāizveido _Azure Active Directory (Azure AD) marķieris_, izmantojot programmu Azure AD. Pēc tam ir jāizmanto Azure AD marķieris, lai iegūtu _piekļuves pilnvaras_ no drošības pakalpojuma.

Microsoft ir nodrošinājusi standarta *Pastnieka* pieprasījuma kolekciju. Jūs variet importēt šo kolekciju savā *Pastnieka* programmatūrā, izmantojot šādu koplietojamu saiti: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Lai iegūtu drošības pakalpojuma pilnvaru, rīkojieties šādi.

1. Pieteikties Azure portālā un izmantot to, lai atrastu `clientId` un `clientSecret` vērtības savai Dynamics 365 Supply Chain Management programmai.
1. Paņemt Azure AD marķieri (`aadToken`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:

   - **URL:**`https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
   - **Metode:** `GET`
   - **Pamatteksta saturs (veidlapas dati):**

     | Princips           | Vērtība                                            |
     | ------------- | -------------------------------------------------|
     | client_id     | ${aadAppId}                                      |
     | client_secret | ${aadAppSecret}                                  |
     | grant_type    | client_credentials                               |
     | Darbības joma         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

   Kā atbilde jāsaņem Azure AD marķieris (`aadToken`). Tiem vajadzētu līdzināties šādam piemēram.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. Formulējiet JavaScript objekta notācijas (JSON) pieprasījumu, kas ir līdzīgs šim piemēram.

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "{$LCS_environment_id}",
       "context_type": "finops-env"
   }
   ```

   Ņemiet vērā šādus punktus:

   - Vērtībai `client_assertion` jābūt Azure AD marķierim (`aadToken`), ko saņēmāt iepriekšējā darbībā.
   - `context` vērtībai jābūt LCS vides ID, kurā vēlaties izvietot pievienojumprogrammu.
   - Iestatiet pārējās vērtības, kā parādītas piemērā.

1. Paņemt piekļuves marķieri (`access_token`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:

   - **URL:** `https://securityservice.operations365.dynamics.com/token`
   - **Metode:** `POST`
   - **HTTP galvene:** iekļaut API versiju. (Atslēga ir `Api-Version`, un vērtība ir `1.0`.)
   - **Pamatteksta saturs:** iekļaut JSON pieprasījumu, ko izveidojāt iepriekšējā darbībā.

   Kā atbilde jāsaņem pieejas marķieris (`access_token`). Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu Krājumu redzamības API. Šeit parādīts piemērs.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> Izmantojot *Pastnieka* pieprasījumu kolekciju, lai izsauktu krājumu redzamības publiskos API, katram pieprasījumam ir jāpievieno uzrādītāja marķieris. Lai atrastu savu uzrādītāja marķieri, atlasiet cilni **Autorizācija** zem pieprasījuma URL, atlasiet tipu **Uzrādītāja Marķieris** un kopējiet piekļuves marķieri, kas tika ienests pēdējā solī. Šī raksta vēlākās sadaļās tiks `$access_token` izmantots, lai attēlotu marķieri, kas tika ienests pēdējā darbībā.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Izveidot rīcībā esošus izmaiņu notikumus

Rīcībā esošo izmaiņu notikumu izveidošanai ir divi API:

- Viena ieraksta izveide: `/api/environment/{environmentId}/onhand`
- Izveidot vairākus ierakstus: `/api/environment/{environmentId}/onhand/bulk`

Tabulā ir apkopota katra JSON pamatteksta lauka nozīme.

| Lauka kods | Apraksts |
|---|---|
| `id` | Unikāls ID noteiktam izmaiņu notikumam. Ja atkārtota iesniegšana rodas pakalpojuma kļūmes dēļ, šis ID tiek izmantots, lai nodrošinātu, ka viens un tas pats notikums sistēmā netiks uzskaitīts divreiz. |
| `organizationId` | Ar notikumu saistītās organizācijas identifikators. Tas attiecas uz risinājuma Supply Chain Management organizācijām vai datu apgabala ID. |
| `productId` | Preces identifikators. |
| `quantities` | Daudzumam ir jābūt mazākam par rīcībā esošo daudzumu. Piemēram, ja plauktam ir pievienotas 10 jaunas grāmatas, vērtība būs `quantities:{ shelf:{ received: 10 }}`. Ja no plaukta ir noņemtas vai pārdotas trīs grāmatas, vērtība būs `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots. Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota. Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām. Ja nav norādīta `dimensionDataSource` vērtība, jūs vaicājumos varat izmantot tikai [pamata dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dinamisks atslēgu/vērtību pāra kopums. Vērtības ir kartētas uz dažām Supply Chain Management dimensijām. Tomēr jūs varat arī pievienot pielāgotas dimensijas (piemēram, _Avots_), lai norādītu, vai notikums nāk no Supply Chain Management vai ārējas sistēmas. |

> [!NOTE]
> Parametri `siteId` un `locationId` veido [dalījuma konfigurāciju](inventory-visibility-configuration.md#partition-configuration). Tāpēc tie ir jākonkretizē dimensijās, kad izveidojat rīcībā esošu izmaiņu notikumus, kopu vai kad pārlabojat rīcībā esošus daudzumus vai veidojat rezervāciju notikumus.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Izveidot vienu rīcībā esošo izmaiņu notikumu

Šis API izveido vienu rīcībā esošo izmaiņu notikumu.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Šajā piemērā parādīts parauga pamatteksta saturs. Šajā paraugā grāmatojiet *T-krekla* preces izmaiņu notikumu. Šis notikums ir no pārdošanas punkta (POS) sistēmas, un debitors ir atgriezis sarkanu T-kreklu atpakaļ jūsu veikalā. Šis notikums palielinās *T-krekla* preces daudzumu par 1.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Šajā piemērā parādīts parauga pamatteksta saturs bez `dimensionDataSource`. Šajā gadījumā `dimensions` būs [bāzes dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension). Ja ir iestatīts `dimensionDataSource`, `dimensions` var būt vai nu datu avota dimensijas vai bāzes dimensijas.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Izveidot vairākus izmaiņu notikumus

Šis API var izveidot vairākus ierakstus vienlaicīgi. Vienīgās atšķirības starp šo API un [viena notikuma API](#create-one-onhand-change-event) ir `Path` un `Body` vērtības. Šim API `Body` sniedz ierakstu masīvu. Maksimālais ierakstu skaits ir 512, kas nozīmē, ka rīcībā esošo krājumu izmaiņas API vienlaikus var atbalstīt līdz 512 izmaiņu notikumiem.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

Šajā piemērā parādīts parauga pamatteksta saturs.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "posSite1",
            "posLocationId": "posLocation1",
            "posMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_2",
        "dimensions": {
            "siteId": "iv_postman_site",
            "locationId": "iv_postman_location",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Iestatīt/ignorēt rīcībā esošos daudzumus

Izmantojot _Iestatīto rīcībā esošo_ API, tiek ignorēti norādītā produkta pašreizējie dati.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Šajā piemērā parādīts parauga pamatteksta saturs. Šī API uzvedība atšķiras no API funkcionalitātes, kas aprakstītas iepriekš šajā rakstā sadaļā Izveidot rīcībā esošos [izmaiņu](#create-onhand-change-event) notikumus. Šajā piemērā *T-krekla* preces daudzums būs iestatīts uz 1.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "iv_postman_site",
            "posLocationId": "iv_postman_location",
            "posMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Izveidot rezervācijas notikumus

Lai lietotu *API rezervēšanu*, ir jāslēdz rezervācijas funkcija un jāpabeidz rezervācijas konfigurācija. Papildinformāciju skatiet [Rezervācijas konfigurēšana (nav obligāti)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Izveidot vienu rezervācijas notikumu

Rezervāciju var veikt pret citiem datu avota iestatījumiem. Lai konfigurētu šāda veida rezervāciju, vispirms konkretizējiet datu avotu parametrā `dimensionDataSource`. Parametrā `dimensions` norādiet dimensijas atbilstoši dimensiju iestatījumiem mērķa datu avotā.

Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

Ja vēlaties atsaukt rezervāciju vai neatgriezt norādītos krājumu daudzumus, iestatiet daudzumu kā negatīvu vērtību un iestatiet parametru, `ifCheckAvailForReserv``False` lai izlaistu pārbaudi. Ir arī atvēlēts nepieejams API, lai to pašu darītu. Atšķirība ir tikai veids, kādā tiek izsaukti divi API. Ir vienkāršāk atsaukt noteiktu rezervācijas notikumu, izmantojot `reservationId` nepieejamu *API*. Papildinformāciju skatiet sadaļā [_Unreserve viens rezervācijas notikums_](#reverse-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Šajā piemērā parādīts parauga pamatteksta saturs.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Šajā piemērā parādīta veiksmīga atbilde.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Izveidot vairākus rezervēšanas notikumus

Šis API ir [viena notikuma API](#create-reservation-events) lielapjoma versija.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Atsaukt rezervēšanas notikumus

Unreserve *API* darbojas kā rezervācijas notikumu atsauktā [*·*](#create-reservation-events) operācija. Tas nodrošina veidu, kā atsaukt rezervēšanas notikumu, kas norādīts `reservationId` par rezervēšanas daudzumu vai samazināt to.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a> Atsaukt vienu rezervācijas notikumu

Veidojot rezervāciju, tā `reservationId` tiek iekļauta atbildes pamattekstā. Jums ir jānorāda viens un tas `reservationId` pats, lai atceltu rezervēšanu un ietvertu to pašu `organizationId` un `dimensions` izmantoto rezervēšanas API zvanam. Visbeidzot norādiet vērtību `OffsetQty`, kas norāda krājumu skaitu, kuri tiks atbrīvoti no iepriekšējās rezervēšanas. Rezervēšanu var pilnībā vai daļēji atcelt atkarībā no norādītā `OffsetQty`. Piemēram, ja *rezervētas 100* krājumu vienības, `OffsetQty: 10`*varat norādīt, lai atceltu 10* no sākotnējās rezervētās summas.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Šis kods rāda pamatteksta satura piemēru.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Tālāk redzamais kods parāda veiksmīgas atbildes pamatteksta piemēru.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Atbildes pamattekstā, ja rezervēšanas `OffsetQty` daudzums ir mazāks vai vienāds ar to, `processingStatus` būs "*veiksmīgs*" un `totalInvalidOffsetQtyByReservId` būs *0*.
>
> Ja `OffsetQty` tā ir lielāka par rezervēto summu, `processingStatus` būs "*partialSuccess*" `totalInvalidOffsetQtyByReservId`, un tā būs starpība starp rezervēto `OffsetQty` summu un rezervēto summu.
>
>Piemēram, ja rezervēšanas daudzums ir 10 *un* vērtība ir `OffsetQty` 12 *,* tad tā būs `totalInvalidOffsetQtyByReservId` 2 *.*

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a> Atsaukt vairākus rezervēšanas notikumus

Šis API ir [viena notikuma API](#reverse-one-reservation-event) lielapjoma versija.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [      
        {
            id: string,
            organizationId: string,
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Rīcībā esošie vaicājumi

Izmantojiet rīcībā *esošo vaicājumu* API, lai ienestu pašreizējos rīcībā esošos krājumu datus saviem produktiem. API pašlaik atbalsta vaicājumu līdz 5000 atsevišķiem krājumiem pēc `productID` vērtības. Katrs `siteID` vaicājumā `locationID` var norādīt vairākas vērtības. Maksimālo ierobežojumu nosaka ar šādu vienādojumu:

*NumOf(SiteID) \* NumOf(LocationID) < = 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Vaicājums, izmantojot grāmatošanas metodi

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Šī pieprasījuma pamatteksta daļā `dimensionDataSource` joprojām ir neobligāts parametrs. Ja tas nav iestatīts, `filters` tiks apstrādāti kā *bāzes dimensijas*. Parametram `filters` ir četri vajadzīgie logi: `organizationId`, `productId`, `siteId` un `locationId`.

- `organizationId` jāsatur tikai viena vērtība, bet tā joprojām ir masīvs.
- `productId` var ietvert vienu vai vairākas vērtības. Ja tas ir tukšs masīvs, visas preces tiks atgrieztas.
- Inventory Visiblity dalīšanā tiek izmantoti `siteId` un `locationId`. Varat norādīt vairāk nekā vienu `siteId` un `locationId` vērtību *Rīcībā aesošā* pieprasījumā. Pašreizējā laidienā jānorāda gan `siteId`, gan `locationId` vērtības.

Ieteicams izmantot parametru, lai `groupByValues` sekotu jūsu konfigurācijai indeksācijā. Papildinformāciju skatiet [Preču indeksa hierarhijas konfigurēšana](./inventory-visibility-configuration.md#index-configuration).

`returnNegative` nosaka, vai rezultāti satur negatīvus ierakstus.

> [!NOTE]
> Ja esat aktivizējuši rīcībā esošo izmaiņu grafiku un pieejamās uz solīšanai (ATP) funkcijas, `QueryATP` vaicājumā var būt iekļauts arī Būla parametrs, kas kontrolē, vai vaicājuma rezultāti ietver ATP informāciju. Papildinformāciju un piemērus skatiet [sadaļā "Rīcībā esošo krājumu redzamības maiņu grafiki" un "pieejams solīšanai"](inventory-visibility-available-to-promise.md).

Šajā piemērā parādīts parauga pamatteksta saturs.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Šajā piemērā parādīts, kā vaicāt par visām precēm noteiktā vietā un atrašanās vietā.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Vaicājums, izmantojot iegūšanas metodi

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Šeit paraugs iegūst vietrādi URL. Šis saņemšanas pieprasījums ir tieši tāds pats kā iepriekš sniegtais grāmatošanas paraugs.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Pieejams solīšanai

Var iestatīt krājumu redzamību, lai ļautu plānot turpmākās rīcībā esošo izmaiņu veikšanu un aprēķināt ATP daudzumus. ATP ir pieejamais krājuma daudzums, un nākamajā periodā to var solīt debitoram. ATP aprēķina izmantošana var ievērojami palielināt pasūtījuma izpildes spēju. Papildinformāciju par to, kā iespējot šo funkciju un kā mijiedarboties ar krājumu redzamību, izmantojot tā API pēc funkcijas iespējošanas, [skatiet krājumu redzamības rīcībā esošo izmaiņu grafikus un pieejamos solīšanai](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Sadalījums

Ar sadalījumu saistītie API ir novietoti krājumu [redzamības sadalījumā](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
