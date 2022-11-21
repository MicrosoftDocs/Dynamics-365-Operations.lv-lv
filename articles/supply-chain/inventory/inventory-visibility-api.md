---
title: Inventory Visibility publiskie API
description: Šajā rakstā ir aprakstītas publiskās API, ko nodrošina krājumu redzamība.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762839"
---
# <a name="inventory-visibility-public-apis"></a>Inventory Visibility publiskie API

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas publiskās API, ko nodrošina krājumu redzamība.

Krājumu redzamības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus. Tas atbalsta četrus galvenos mijiedarbības tipus:

- Iegrāmatojot pievienojumprogrammas rīcībā esošās izmaiņas no ārējās sistēmas
- Rīcībā esošo krājumu daudzumu iestatīšana vai ignorēšana pievienojumprogrammai no ārējās sistēmas
- Iegrāmatojot pievienojumprogrammā rezervācijas notikumus no ārējās sistēmas
- Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas

Tālāk esošajā tabulā ir norādītas pieejamās API:

| Ceļš | Metode | Apraksts |
|---|---|---|
| /api/vide/{environmentId}/rīcībā esošs | Amats | [Izveidot vienu rīcībā esošo izmaiņu notikumu](#create-one-onhand-change-event)|
| /api/vide/{environmentId}/rīcībā esošs/lielapjoma | Amats | [Izveidot vairākus izmaiņu notikumus](#create-multiple-onhand-change-events) |
| /api/vide/{environmentId}/rīcībā esošs/{inventorySystem}/lielapjoma | Amats | [Iestatīt/ignorēt rīcībā esošos daudzumus](#set-onhand-quantities) |
| /api/vide/{environmentId}/rīcībā esošs/rezervēt | Grāmatot | [Viena mīkstās rezervācijas notikuma izveide](#create-one-reservation-event) |
| /api/vide/{environmentId}/rīcībā esošs/rezervēt/lielapjoma | Grāmatot | [Izveidojiet vairākus neobligātās rezervācijas notikumus](#create-multiple-reservation-events) |
| /api/vide//onhand/{environmentId} unreserve | Grāmatot | [Viena mīkstās rezervācijas notikuma atcelšana](#reverse-one-reservation-event) |
| /api/vide//onhand/unreserve/{environmentId} bulk | Grāmatot | [Vairāku neobligātās rezervācijas notikumu atcelšana](#reverse-multiple-reservation-events) |
| /api/vide//onhand/{environmentId} changeschedule | Grāmatot | [Izveidojiet vienu ieplānotu rīcībā esošu izmaiņu](inventory-visibility-available-to-promise.md) |
| /API/vide//onhand/changeschedule/{environmentId} bulk | Grāmatot | [Vairāku rīcībā esošu izmaiņu izveide ar datumiem](inventory-visibility-available-to-promise.md) |
| /api/vide/{environmentId}/rīcībā esošs/indeksa vaicājums | Grāmatot | [Vaicājums, izmantojot izlikšanas metodi](#query-with-post-method) (ieteicams) |
| /api/vide/{environmentId}/rīcībā esošs | Iegūt | [Vaicājums, izmantojot iegūšanas metodi](#query-with-get-method) |
| /api/vide//onhand/{environmentId} exactquery | Grāmatot | [Precīzs vaicājums, izmantojot izlikšanas metodi](#exact-query-with-post-method) |
| /API/vide//piešķiršana{environmentId}/<wbr> piešķiršana | Grāmatot | [Viena piešķīruma notikuma izveide](inventory-visibility-allocation.md#using-allocation-api) |
| /api/vide//piešķiršana{environmentId}/<wbr> nepiešķiršana | Grāmatot | [Viena nepiešķirta notikuma izveide](inventory-visibility-allocation.md#using-allocation-api) |
| /API/Vide//Sadale/{environmentId} Pārdale<wbr> | Grāmatot | [Viena pārdales notikuma izveide](inventory-visibility-allocation.md#using-allocation-api) |
| /API/Vide//Piešķiršana{environmentId}/<wbr> Patēriņš | Grāmatot | [Viena patērētā notikuma izveide](inventory-visibility-allocation.md#using-allocation-api) |
| /api/vide//piešķiršana{environmentId}/<wbr> vaicājums | Grāmatot | [Vaicājuma sadalījuma rezultāts](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Ceļa {environmentId} daļa ir vides ID pakalpojumā Microsoft Dynamics Lifecycle Services.
> 
> Lielapjoma API var atgriezt ne vairāk kā 512 ierakstus katram pieprasījumam.

Microsoft ir nodrošinājusi standarta *Pastnieka* pieprasījuma kolekciju. Jūs variet importēt šo kolekciju savā *Pastnieka* programmatūrā, izmantojot šādu koplietojamu saiti: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Atrast galapunktu atbilstoši Lifecycle Services videi

Krājumu redzamības mikropakalpojums ir izvietots Microsoft Azure Service Fabric vairākās atrašanās vietās un reģionos. Šobrīd nav centrālā galapunkta, kas var automātiski novirzīt jūsu pieprasījumu uz atbilstošo ģeogrāfisko vietu un reģionu. Tāpēc informācijas vienības jāveido vietrādī URL, izmantojot šādu modeli:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Reģiona saīsinātais nosaukums ir atrodams dzīves cikla pakalpojumu vidē. Tālāk esošajā tabulā ir norādīti pieejamie reģioni.

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
| Indijas centrālā daļa       | CIN               |
| Dienvidindija         | grēks               |
| Šveices ziemeļi   | nch               |
| Šveices rietumi    | wch               |
| Francija uz dienvidiem        | SFR               |
| Austrumāzija           | Eas               |
| Dienvidaustrumāzija     | Jūras              |
| Aae ziemeļi           | nae               |
| Norvēģijas austrumi         | Īno               |
| Norvēģijas rietumi         | WNO               |
| Dienvidāfrikas rietumi   | WZA               |
| Dienvidāfrika uz ziemeļiem  | NZA               |

Salas numurs ir vieta, kur pakalpojumā Service Fabric ir izvietota jūsu dzīves cikla pakalpojumu vide. Pašlaik nav iespējams iegūt šo informāciju no lietotāja puses.

Microsoft ir izveidojis lietotāja interfeisu (UI) risinājumā Power Apps, lai varētu iegūt pilnu mikropakalpojuma galapunktu. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikācija

Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu redzamības pievienojumprogrammas publisko API. Tāpēc, izmantojot programmu, ir jāizveido *Azure Active Directory (Azure AD) marķieris* ar Azure AD lietotni. Pēc tam ir jāizmanto Azure AD marķieris, lai iegūtu *piekļuves pilnvaras* no drošības pakalpojuma.

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
        | Darbības joma         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.Noklusējuma    |

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
    - Vērtībai `context` ir jābūt Lifecycle Services vides ID, kurā vēlaties izvietot pievienojumprogrammu.
    - Iestatiet pārējās vērtības, kā parādītas piemērā.

1. Paņemt piekļuves marķieri (`access_token`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Metode:** `POST`
    - **HTTP galvene:** iekļaut API versiju. (Atslēga ir `Api-Version`, un vērtība ir `1.0`.)
    - **Pamatteksta saturs:** iekļaut JSON pieprasījumu, ko izveidojāt iepriekšējā darbībā.

    Kā atbilde jāsaņem pieejas marķieris (`access_token`). Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu Krājumu redzamības API. Lūk, piemērs.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Izmantojot *Pastnieka* pieprasījumu kolekciju, lai izsauktu krājumu redzamības publiskos API, katram pieprasījumam ir jāpievieno uzrādītāja marķieris. Lai atrastu savu uzrādītāja marķieri, atlasiet cilni **Autorizācija** zem pieprasījuma URL, atlasiet tipu **Uzrādītāja Marķieris** un kopējiet piekļuves marķieri, kas tika ienests pēdējā solī. Šī raksta turpmākajās sadaļās tiks izmantots, lai attēlotu marķieri, `$access_token` kas tika iegūts pēdējā darbībā.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Izveidot rīcībā esošus izmaiņu notikumus

Rīcībā esošo izmaiņu notikumu izveidošanai ir divi API:

- Viena ieraksta izveide: `/api/environment/{environmentId}/onhand`
- Izveidot vairākus ierakstus: `/api/environment/{environmentId}/onhand/bulk`

Tabulā ir apkopota katra JSON pamatteksta lauka nozīme.

| Lauka ID | Apraksts |
|---|---|
| `id` | Unikāls ID noteiktam izmaiņu notikumam. Ja atkārtota iesniegšana notiek pakalpojuma kļūmes dēļ, šis ID tiek izmantots, lai nodrošinātu, ka viens un tas pats notikums sistēmā netiek uzskaitīts divreiz. |
| `organizationId` | Ar notikumu saistītās organizācijas identifikators. Tas attiecas uz risinājuma Supply Chain Management organizācijām vai datu apgabala ID. |
| `productId` | Preces identifikators. |
| `quantities` | Daudzumam ir jābūt mazākam par rīcībā esošo daudzumu. Piemēram, ja plauktam ir pievienotas 10 jaunas grāmatas, vērtība būs `quantities:{ shelf:{ received: 10 }}`. Ja no plaukta ir noņemtas vai pārdotas trīs grāmatas, vērtība būs `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots. Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota. Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām. Ja nav norādīta `dimensionDataSource` vērtība, jūs vaicājumos varat izmantot tikai [pamata dimensijas](inventory-visibility-configuration.md#data-source-configuration-dimension). |
| `dimensions` | Dinamisks atslēgu/vērtību pāra kopums. Vērtības ir kartētas uz dažām Supply Chain Management dimensijām. Tomēr jūs varat arī pievienot pielāgotas dimensijas (piemēram, *Avots*), lai norādītu, vai notikums nāk no Supply Chain Management vai ārējas sistēmas. |

> [!NOTE]
> Parametri `siteId` un `locationId` veido [dalījuma konfigurāciju](inventory-visibility-configuration.md#partition-configuration). Tāpēc tie ir jākonkretizē dimensijās, kad izveidojat rīcībā esošu izmaiņu notikumus, kopu vai kad pārlabojat rīcībā esošus daudzumus vai veidojat rezervāciju notikumus.

Nākamajās apakšsadaļās ir sniegti piemēri, kuros parādīts, kā izmantot šos API.

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

Šajā piemērā parādīts parauga pamatteksta saturs. Šajā piemērā uzņēmumam ir pārdošanas punkta (POS) sistēma, kas apstrādā veikala transakcijas un līdz ar to krājumu izmaiņas. Klients jūsu veikalā ir atgriezis sarkanu T-kreklu. Lai atspoguļotu izmaiņas, jūs publicējat vienu izmaiņu notikumu *T-krekla* izstrādājumam. Šis notikums palielinās *T-krekla* preces daudzumu par 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
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
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
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

Šis API var izveidot izmaiņu notikumus, tāpat kā [viena notikuma API](#create-one-onhand-change-event). Vienīgā atšķirība ir tā, ka šis API var vienlaikus izveidot vairākus ierakstus. `Path``Body` Tāpēc vērtības atšķiras. Šim API `Body` sniedz ierakstu masīvu. Maksimālais ierakstu skaits ir 512. Tāpēc pieejamo izmaiņu lielapjoma API var vienlaikus atbalstīt līdz pat 512 izmaiņu notikumiem. 

Piemēram, mazumtirdzniecības veikala POS iekārta apstrādāja šādas divas transakcijas:

- Viens viena sarkana T-krekla atgriešanas pasūtījums
- Viens pārdošanas darījums ar trim melniem T-krekliem

Šādā gadījumā abus krājumu atjauninājumus varat iekļaut vienā API zvanā.

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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Iestatīt/ignorēt rīcībā esošos daudzumus

Izmantojot *Iestatīto rīcībā esošo* API, tiek ignorēti norādītā produkta pašreizējie dati. Šī funkcionalitāte parasti tiek izmantota, lai veiktu krājumu uzskaites atjauninājumus. Piemēram, ikdienas krājumu skaitīšanas laikā veikals var konstatēt, ka faktiskais rīcībā esošais sarkanā T-krekla krājums ir 100. Tāpēc POS ienākošais daudzums ir jāatjaunina uz 100 neatkarīgi no tā, kāds bija iepriekšējais daudzums. Varat izmantot šo API, lai ignorētu esošo vērtību.

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

Šajā piemērā parādīts parauga pamatteksta saturs. Šī API darbība atšķiras no to API darbības, kas aprakstītas [šī raksta sadaļā Funkcijas izmaiņu notikumu](#create-onhand-change-event) izveide. Šajā piemērā *T-krekla* preces daudzums būs iestatīts uz 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Izveidot rezervācijas notikumus

Lai izmantotu *Reserve* API, jums ir jāieslēdz rezervēšanas līdzeklis un jāpabeidz rezervācijas konfigurācija. Papildinformāciju (tostarp datu plūsmu un scenārija paraugu) skatiet sadaļā [Rezervācijas konfigurācija (neobligāti)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Izveidot vienu rezervācijas notikumu

Rezervāciju var veikt pret citiem datu avota iestatījumiem. Lai konfigurētu šāda veida rezervāciju, vispirms konkretizējiet datu avotu parametrā `dimensionDataSource`. Parametrā `dimensions` norādiet dimensijas atbilstoši dimensiju iestatījumiem mērķa datu avotā.

Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

Ja vēlaties atsaukt rezervāciju vai rezervēt norādītos krājumu daudzumus, iestatiet daudzumu uz negatīvu vērtību un iestatiet parametru `ifCheckAvailForReserv`, lai `False` izlaistu validāciju. Ir arī īpašs unreserve API, lai to izdarītu. Atšķirība ir tikai tajā, kā tiek sauktas abas API. Ir vieglāk atsaukt konkrētu rezervācijas notikumu, izmantojot `reservationId`*unreserve* API. Papildinformāciju skatiet sadaļā [Viena rezervācijas pasākuma](#reverse-reservation-events) rezervēšana.

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

Tālāk sniegtajā piemērā ir parādīta veiksmīga atbilde.

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

## <a name="reverse-reservation-events"></a>Atcelšanas gadījumi

Unreserve *API* kalpo kā apgrieztā darbība rezervācijas [*·*](#create-reservation-events) notikumiem. Tas nodrošina veidu, kā atcelt rezervācijas notikumu, ko `reservationId` norāda rezervācijas daudzums, vai samazināt rezervācijas daudzumu.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a> Viena rezervācijas notikuma atcelšana

Kad rezervācija ir izveidota, atbildes pamattekstā tiks iekļauts testaments `reservationId`. Lai atceltu rezervāciju, jums ir jānorāda tas pats, kā arī tas pats `reservationId``organizationId``dimensions`, kas tiek izmantots rezervācijas API zvanam. Visbeidzot, norādiet `OffsetQty` vērtību, kas norāda vienumu skaitu, kas jāatbrīvo no iepriekšējās rezervācijas. Rezervāciju var pilnībā vai daļēji atcelt atkarībā no norādītā `OffsetQty`. Piemēram, ja *tika rezervētas 100 vienumu vienības, varat norādīt*, lai noņemtu `OffsetQty: 10` 10 *no* sākotnējās rezervētās summas.

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

Tālāk norādītais kods parāda ķermeņa satura piemēru.

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

Šis kods parāda veiksmīgas atbildes struktūras piemēru.

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
> Atbildes pamattekstā, ja `OffsetQty` tas ir mazāks vai vienāds ar rezervācijas daudzumu, `processingStatus` būs "panākumi *"* un `totalInvalidOffsetQtyByReservId` būs *0*.
>
> Ja `OffsetQty` ir lielāks par rezervēto summu, `processingStatus` būs "daļējsSuccess *"* un būs starpība starp `totalInvalidOffsetQtyByReservId` rezervēto summu un `OffsetQty` to.
>
>Piemēram, ja rezervācijas daudzums *ir 10* un `OffsetQty` tās vērtība *ir 12*, `totalInvalidOffsetQtyByReservId` tā būtu *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a> Vairāku rezervācijas gadījumu atcelšana

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

*Izmantojiet rīcībā esošo vaicājuma API, lai ienestu pašreizējos rīcībā* esošos krājumu datus par saviem produktiem. Šo API varat izmantot ikreiz, kad jums ir jāzina krājumi, piemēram, kad vēlaties pārskatīt produktu krājumu līmeni savā e-komercijas vietnē vai kad vēlaties pārbaudīt produktu pieejamību reģionos vai tuvējos veikalos un noliktavās. API pašlaik atbalsta vaicājumus līdz pat 5,000 atsevišķiem vienumiem pēc `productID` vērtības. Katrā vaicājumā var norādīt arī vairākas `siteID` vērtības un vērtības `locationID`. Maksimālo robežu nosaka ar šādu vienādojumu:

*NumOf(SiteID) NumOf(LocationID) \* <= 100*.

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

- `organizationId` Jābūt tikai vienai vērtībai, bet tā joprojām ir masīvs.
- `productId` varētu saturēt vienu vai vairākas vērtības. Ja tas ir tukšs masīvs, visas preces tiks atgrieztas.
- Inventory Visiblity dalīšanā tiek izmantoti `siteId` un `locationId`. Varat norādīt vairāk nekā vienu `siteId` un `locationId` vērtību *Rīcībā aesošā* pieprasījumā. Pašreizējā laidienā jānorāda gan `siteId`, gan `locationId` vērtības.

Ieteicams izmantot šo parametru `groupByValues`, lai sekotu konfigurācijai indeksēšanai. Papildinformāciju skatiet [Preču indeksa hierarhijas konfigurēšana](./inventory-visibility-configuration.md#index-configuration).

`returnNegative` nosaka, vai rezultāti satur negatīvus ierakstus.

> [!NOTE]
> Ja esat iespējojis rīcībā esošo izmaiņu grafiku un solījumu pieejamības (ATP) līdzekļus, vaicājumā var iekļaut arī Būla parametru `QueryATP`, kas kontrolē, vai vaicājuma rezultātos ir iekļauta ATP informācija. Papildinformāciju un piemērus skatiet sadaļā [Krājumu redzamība rīcībā esošie izmaiņu grafiki, kas ir pieejami solīšanai](inventory-visibility-available-to-promise.md).

Šajā piemērā parādīts parauga pamatteksta saturs. Tas parāda, ka varat vaicāt rīcībā esošajiem krājumiem no vairākām atrašanās vietām (noliktavām).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Tālāk sniegtajā piemērā ir parādīts, kā vaicāt visiem produktiem noteiktā vietnē un atrašanās vietā.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
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

Tālāk ir sniegts parauga iegūšanas URL. Šis saņemšanas pieprasījums ir tieši tāds pats kā iepriekš sniegtais grāmatošanas paraugs.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a> Rīcībā esošs precīzs vaicājums

Rīcībā esošie precīzie vaicājumi līdzinās parastiem rīcībā esošiem vaicājumiem, taču tie ļauj norādīt kartēšanas hierarhiju starp vietni un atrašanās vietu. Piemēram, jums ir šādas divas vietnes:

- 1. vietne, kas ir kartēta uz atrašanās vietu A
- 2. vietne, kas ir kartēta uz atrašanās vietu B

Parastam rīcībā esošam vaicājumam, ja norādāt `"siteId": ["1","2"]` un, krājumu redzamība automātiski vaicās rezultātu šādām vietnēm un `"locationId": ["A","B"]` atrašanās vietām:

- 1. vieta, atrašanās vieta A
- 1. vieta, atrašanās vieta B
- 2. vieta, atrašanās vieta A
- 2. vieta, atrašanās vieta B

Kā redzat, parastais rīcībā esošais vaicājums neatpazīst, ka atrašanās vieta A pastāv tikai 1. vietā, bet atrašanās vieta B pastāv tikai 2. vietā. Tāpēc tas rada liekus jautājumus. Lai pielāgotos šai hierarhiskajai kartēšanai, varat izmantot rīcībā esošu precīzu vaicājumu un vaicājuma pamattekstā norādīt atrašanās vietas kartējumus. Šādā gadījumā jūs vaicāsit un saņemsit rezultātus tikai par 1. vietni, atrašanās vietu A un 2. vietu, atrašanās vietu B.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a> Precīzs vaicājums, izmantojot izlikšanas metodi

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Šī pieprasījuma pamattekstā ir neobligāts parametrs. `dimensionDataSource` Ja tas nav iestatīts, `dimensions` in `filters` tiks uzskatīts par *pamata izmēriem*. Parametram `filters` ir četri vajadzīgie logi: `organizationId`, `productId`, `dimensions` un `values`.

- `organizationId` Jābūt tikai vienai vērtībai, bet tā joprojām ir masīvs.
- `productId` varētu saturēt vienu vai vairākas vērtības. Ja tas ir tukšs masīvs, visas preces tiks atgrieztas.
- Masīvā`dimensions`, un `siteId` tie ir nepieciešami, `locationId` bet var parādīties kopā ar citiem elementiem jebkurā secībā.
- `values` varētu saturēt vienu vai vairākus atšķirīgus vērtību kopumus, kas atbilst `dimensions`.

`dimensions` in `filters` tiks automātiski pievienots `groupByValues`.

`returnNegative` nosaka, vai rezultāti satur negatīvus ierakstus.

Šajā piemērā parādīts parauga pamatteksta saturs.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Tālāk sniegtajā piemērā ir parādīts, kā vaicāt visiem produktiem vairākās vietnēs un atrašanās vietās.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Pieejams solīšanai

Varat iestatīt krājumu redzamību, lai jūs varētu ieplānot turpmākās rīcībā esošās izmaiņas un aprēķināt ATP daudzumus. ATP ir krājuma daudzums, kas ir pieejams un ko var apsolīt klientam nākamajā periodā. ATP aprēķina izmantošana var ievērojami palielināt jūsu pasūtījuma izpildes iespējas. Informāciju par to, kā iespējot šo līdzekli un kā mijiedarboties ar krājumu redzamību, izmantojot tā API, pēc tam, kad līdzeklis ir iespējots, skatiet sadaļā [Krājumu redzamība rīcībā pieejami izmaiņu grafiki un pieejamība solīšanai](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Sadalījums

Ar sadalījumu saistītie API atrodas krājumu [redzamības sadalījumā](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
