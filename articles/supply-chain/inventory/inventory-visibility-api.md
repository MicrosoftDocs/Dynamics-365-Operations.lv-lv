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
ms.openlocfilehash: 23f4c52b6d1d8c1af927a2c21455d6e24b24408a
ms.sourcegitcommit: 7bcaf00a3ae7e7794d55356085e46f65a6109176
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/26/2022
ms.locfileid: "9357646"
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

Microsoft ir nodrošinājusi standarta *Pastnieka* pieprasījuma kolekciju. Jūs variet importēt šo kolekciju savā *Pastnieka* programmatūrā, izmantojot šādu koplietojamu saiti: <https://www.getpostman.com/collections/ad8a1322f953f88d9a55>.

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

   Kā atbilde jāsaņem pieejas marķieris (`access_token`). Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu Krājumu redzamības API. Tālāk ir minēts piemērs.

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
| `id` | Unikāls ID noteiktam izmaiņu notikumam. Šis ID tiek izmantots, lai nodrošinātu, ka, ja grāmatošanas laikā sakari ar pakalpojumu neizdodas, notikuma atkārtota iesniegšana nenozīmē, ka viens un tas pats notikums sistēmā tiek skaitīts divas reizes un atkārtoti iesniegts. |
| `organizationId` | Ar notikumu saistītās organizācijas identifikators. Tas attiecas uz risinājuma Supply Chain Management organizācijām vai datu apgabala ID. |
| `productId` | Preces identifikators. |
| `quantities` | Daudzumam ir jābūt mazākam par rīcībā esošo daudzumu. Piemēram, ja plauktam ir pievienotas 10 jaunas grāmatas, vērtība būs `quantities:{ shelf:{ received: 10 }}`. Ja no plaukta ir noņemtas vai pārdotas trīs grāmatas, vērtība būs `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots. Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota. Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām. Ja nav norādīta `dimensionDataSource` vērtība, jūs vaicājumos varat izmantot tikai [pamata dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dinamisks atslēgu/vērtību pāra kopums. Vērtības ir kartētas uz dažām Supply Chain Management dimensijām. Tomēr jūs varat arī pievienot pielāgotas dimensijas (piemēram, _Avots_), lai norādītu, vai notikums nāk no Supply Chain Management vai ārējas sistēmas. |

> [!NOTE]
> Parametri `SiteId` un `LocationId` veido [dalījuma konfigurāciju](inventory-visibility-configuration.md#partition-configuration). Tāpēc tie ir jākonkretizē dimensijās, kad izveidojat rīcībā esošu izmaiņu notikumus, kopu vai kad pārlabojat rīcībā esošus daudzumus vai veidojat rezervāciju notikumus.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
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
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
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
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
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

Lai lietotu API *rezervēšanu*, ir jāatver rezervēšanas funkcija un jāpabeidz rezervācijas konfigurācija. Papildinformāciju skatiet [Rezervācijas konfigurēšana (nav obligāti)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Izveidot vienu rezervācijas notikumu

Rezervāciju var veikt pret citiem datu avota iestatījumiem. Lai konfigurētu šāda veida rezervāciju, vispirms konkretizējiet datu avotu parametrā `dimensionDataSource`. Parametrā `dimensions` norādiet dimensijas atbilstoši dimensiju iestatījumiem mērķa datu avotā.

Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

Ja vēlaties atcelt rezervāciju vai atsaukt konkrētu krājuma daudzumu rezervāciju, iestatiet daudzumu uz negatīvu vērtību, un iestatiet parametru `ifCheckAvailForReserv` uz vērtību `False`, lai izlaistu validāciju.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Izveidot vairākus rezervēšanas notikumus

Šis API ir [viena notikuma API](#create-one-reservation-event) lielapjoma versija.

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

## <a name="query-on-hand"></a>Rīcībā esošie vaicājumi

Izmantojiet rīcībā _esošo vaicājumu_ API, lai ienestu pašreizējos rīcībā esošos krājumu datus saviem produktiem. API pašlaik atbalsta vaicājumu līdz 100 atsevišķiem krājumiem pēc `ProductID` vērtības. Katrs `SiteID` vaicājumā `LocationID` var norādīt vairākas vērtības. Maksimālais ierobežojums ir definēts kā `NumOf(SiteID) * NumOf(LocationID) <= 100`.

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

`groupByValues` parametram vajadzētu sekot jūsu indeksēšanas konfigurācijai. Papildinformāciju skatiet [Preču indeksa hierarhijas konfigurēšana](./inventory-visibility-configuration.md#index-configuration).

`returnNegative` nosaka, vai rezultāti satur negatīvus ierakstus.

> [!NOTE]
> Ja esat aktivizējuši rīcībā esošo izmaiņu grafiku un pieejamās uz solīšanai (ATP) funkcijas, `QueryATP` vaicājumā var būt iekļauts arī Būla parametrs, kas kontrolē, vai vaicājuma rezultāti ietver ATP informāciju. Papildinformāciju un piemērus skatiet [sadaļā "Rīcībā esošo krājumu redzamības maiņu grafiki" un "pieejams solīšanai"](inventory-visibility-available-to-promise.md).

Šajā piemērā parādīts parauga pamatteksta saturs.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Šajā piemērā parādīts, kā vaicāt par visām precēm noteiktā vietā un atrašanās vietā.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
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

Šeit ir paraugs iegūt vietrādi URL. Šis saņemšanas pieprasījums ir tieši tāds pats kā iepriekš sniegtais grāmatošanas paraugs.

```txt
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Pieejams solīšanai

Var iestatīt krājumu redzamību, lai ļautu plānot turpmākās rīcībā esošo izmaiņu veikšanu un aprēķināt ATP daudzumus. ATP ir pieejamais krājuma daudzums, un nākamajā periodā to var solīt debitoram. ATP aprēķina izmantošana var ievērojami palielināt pasūtījuma izpildes spēju. Papildinformāciju par to, kā iespējot šo funkciju un kā mijiedarboties ar krājumu redzamību, izmantojot tā API pēc funkcijas iespējošanas, [skatiet krājumu redzamības rīcībā esošo izmaiņu grafikus un pieejamos solīšanai](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Sadalījums

Ar sadalījumu saistītie API ir novietoti krājumu [redzamības sadalījumā](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
