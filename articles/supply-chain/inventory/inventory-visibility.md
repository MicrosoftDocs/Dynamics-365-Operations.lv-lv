---
title: Krājumu uztveramības pievienojumprogramma
description: Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt krājumu uztveramības pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910429"
---
# <a name="inventory-visibility-add-in"></a>Krājumu uztveramības pievienojumprogramma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Krājumu uztveramības pievienojumprogramma ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību.

Visa informācija, kas saistīta ar rīcībā esošajiem krājumiem, tiek eksportēta uz pakalpojumu gandrīz reāllaikā, izmantojot zema līmeņa SQL integrāciju. Ārējās sistēmas piekļūst pakalpojumam, izmantojot RESTful API, lai vaicātu rīcībā esošo informāciju par noteiktajām dimensiju kopām, tādējādi izgūstot pieejamo rīcībā esošo pozīciju sarakstu.

Krājumu uztveramība ir Microsoft Dataverse iebūvēts pakalpojums, kas nozīmē, ka varat to pagarināt, izveidojot Power Apps un pielietojot Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa vajadzībām. Var arī jaunināt indeksu, lai veiktu krājumu vaicājumus.

Krājumu uztveramība nodrošina konfigurācijas opcijas, kas ļauj to integrēt ar vairākām trešās puses sistēmām. Tā atbalsta standartizētu krājumu dimensiju, pielāgoto paplašināšanos un standartizētu, konfigurējamu aprēķināto daudzumu.

Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Krājumu uztveramības pievienojumprogrammu Dynamics 365 Supply Chain Management un kā izmantot tās programmas programmēšanas interfeisu (API).

## <a name="install-the-inventory-visibility-add-in"></a>Instalēt krājumu uztveramības pievienojumprogrammu

Jums ir jāinstalē Krājumu uztveramības pievienojumprogramma, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu lietojumprogrammu dzīves ciklu Dynamics 365 Finance and Operations.

Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms instalējat Krājumu uztveramības pievienojumprogrammu, jums ir jādara sekojošais:

- Iegūt LCS ieviešanas projektu, kurā ir vismaz viens izvietošanas vides objekts.
- Pārliecinieties, ka pievienojumprogrammu pārskata iestatīšanas priekšnoteikumi, kas sniegti [Pievienojumprogrammu pārskatā](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) ir pabeigti. Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.
- Sazinieties ar krājumu redzamības grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu šādus trīs nepieciešamos failus:
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - `Inventory Visibility Integration.zip` (Ja jūsu darbinātā Supply Chain Management versija ir agrāka nekā versija 10.0.18)
- Izpildiet sadaļā [Ātrā sākšana: reģistrējiet programmu ar Microsoft identitātes platformu](/azure/active-directory/develop/quickstart-register-app) sniegtās instrukcijas, lai reģistrētu programmu un pievienotu AAD klienta noslēpumu atbilstoši Azure abonementam.
    - [Lietojumprogrammas reģistrācija](/azure/active-directory/develop/quickstart-register-app)
    - [Pievienot klienta noslēpumu](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - Opcijas **Programmas (klienta) ID**, **Klienta noslēpums** un **Nomnieka ID** tiks izmantots sekojošās darbībās.

> [!NOTE]
> Pašlaik atbalstītās valstis un reģioni ietver Kanādu, Amerikas Savienotās Valstis un Eiropas Savienību (ES).

Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar krājumu redzamības preču darba grupu.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Iestātīt Dataverse

Lai iestatītu Dataverse, rīkojieties, kā norādīts tālāk.

1. Pievienojiet pakalpojumu principu savam nomniekam:

    1. Instalējiet Azure AD PowerShell moduli v2, kā aprakstīts [Pakalpojuma Azure Active Directory instalēšana PowerShell grafikam](/powershell/azure/active-directory/install-adv2).
    1. Izpildiet šādu PowerShell komandu.

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. Izveidot programmas lietotāju, lai noteiktu krājumu redzamību Dataverse šeit:

    1. Atveriet Dataverse vides URL.
    1. Dodieties uz **Papildu iestatījumi \> Sistēma \> Drošība \> Lietotāji** un izveidojiet programmas lietotāju. Izmantojiet skata izvēlni, lai mainītu lapas skatu uz **Programmas lietotāji**.
    1. Atlasiet **Jauns**. Iestatiet Programmas ID uz *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Saglabājot izmaiņas, objekta ID tiks ielādēts automātiski.) Šo nosaukumu var pielāgot. Piemēram, to var mainīt uz *Krājumu redzamība*. Pēc pabeigšanas atlasiet **Saglabāt**.
    1. Atlasiet **Piešķirt lomu** un pēc tam atlasiet **Sistēmas administrators**. Ja ir loma ar nosaukumu **Common Data Service Lietotājs**, atlasiet to arī.

    Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Ja jūsu noklusētā valoda Dataverse nav **Angļu**:

    1. Pārejiet uz **Papildu iestatījums \> Administrēšana \> Valodas**,
    1. Atlasiet **Angļu (ValodasKods=1033)** un atlasiet **Lietot**.

1. Importēt `Inventory Visibility Dataverse Solution.zip` failu, kas ietver Dataverse ar konfigurāciju saistītos elementus un Power Apps:

    1. Doties uz lapu **Risinājumi**.
    1. Atlasiet **Importēt**.

1. Importēt konfigurācijas jaunināšanas trigera plūsmu:

    1. Doties uz lapu Microsoft Flow.
    1. Pārliecinieties, vai pastāv savienojums ar nosaukumu *Dataverse (mantojums)*. (Ja tāda nav, izveidojiet to.)
    1. Importēt `Inventory Visibility Configuration Trigger.zip` failu. Pēc tā importēšanas trigeris parādīsies zem **Manas plūsmas**.
    1. Inicializējiet tālāk norādītos četrus mainīgos, pamatojoties uz vides informāciju:

        - Azure nomnieka ID
        - Azure Lietojumprogrammas klienta ID
        - Azure Lietojumprogrammas klienta noslēpums
        - Krājumu redzamības galapunkts

            Papildinformāciju par šo mainīgo skatiet tālāk šīs tēmas sadaļā [Krājumu redzamības integrācijas iestatīšana](#setup-inventory-visibility-integration).

        ![Konfigurācijas trigeris](media/configuration-trigger.png "Konfigurācijas trigeris")

    1. Atlasiet **Ieslēgt**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Pievienojumprogrammas instalēšana

Lai instalētu Krājumu uztveramības pievienojumprogrammu, jums jārīkojas šādi:

1. Pierakstieties portālā [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.
1. Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
1. Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**, kur varat atrast Dataverse vides nosaukumu.
1. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.

    ![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")

1. Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**. Tiek atvērts pieejamo pievienojumprogrammu saraksts.
1. Atlasiet no saraksta **Krājumu redzamība**.
1. Ievadiet vērtības savai video šādiem laukiem:

    - **AAD Lietojumprogrammas (klienta) ID**
    - **AAD nomnieka ID**

    ![Pievienot iestatīšanas lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")

1. Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.
1. Atlasiet **Instalēt**. Pievienojumprogrammu statuss tiks rādīts kā **Instalē**. Kad tas ir izdarīts, atsvaidziniet lapu, lai redzētu statusa maiņu uz **Instalēts**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Pievienojumprogrammas atinstalēšana

Lai atinstalētu pievienojumprogrammu, atlasiet **Atinstalēt**. Kad atsvaidzināsiet LCS, Krājumu uztveramības pievienojumprogramma tiks noņemta. Atinstalēšanas process noņems pievienojumprogrammu reģistrāciju un arī sāks darbu, lai notīrītu visus pakalpojumā saglabātos biznesa datus.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Patērēt rīcībā esošos krājumu datus no Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Izvietot Krājumu redzamības integrācijas pakotni

Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu. Pēc tam izvietojiet pakotni LCS.

> [!NOTE]
> Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē. Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.
> 
> Kods ir iekļauts Supply Chain Management versijā 10.0.18. Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.

Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas. (Pēc noklusējuma tās ir iespējotas.)

| Līdzekļa apraksts | Koda versija | Pārslēgt klasi |
|---|---|---|
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā | 10.0.11 | InventUseDimOfInventSumToggle |
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana

1. Programmā Supply Chain Management atveriet **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietu un iespējojiet **Krājumu redzamības integrācijas** līdzekli.
1. Pārejiet uz sadaļu **Krājumu pārvaldība \> Iestatījumi \> Krājumu redzamības integrēšanas parametri** un ievadiet URL, kurā palaižat Krājumu redzamību.

    Atrodiet LCS vides Azure reģionu un pēc tam ievadiet vietrādi URL. URL ir šāda veidlapa:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Piemēram, ja esat Eiropā, jūsu videi būs viens no šiem vietrāžiem URL:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    Pieejami šādi reģioni.

    | Azure reģions | Reģiona īsais nosaukums |
    |---|---|
    | Austrālijas austrumi | eau |
    | Austrālijas dienvidaustrumi | seau |
    | Kanādas centrālā daļā | cca |
    | Kanādas austrumi | eca |
    | Ziemeļeiropa | neu |
    | Rietumeiropa | weu |
    | ASV austrumi | eus |
    | ASV rietumi | wus |

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu. Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Krājumu redzamības pievienojumprogrammas publiskais API

Krājumu redzamības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus. Tas atbalsta trīs galvenos mijiedarbības tipus:

- Iegrāmatojot pievienojumprogrammas rīcībā esošās izmaiņas no ārējās sistēmas
- Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas
- Automātiska sinhronizācija ar Supply Chain Management rīcībā esošiem krājumiem

Automātiskā sinhronizācija nav daļa no publiskā API. Tā vietā tā tiek apstrādāta fonā vidēm, kurās ir iespējota krājumu redzamības pievienojumprogramma.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Autentifikācija

Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu redzamības pievienojumprogrammu. Tāpēc, izmantojot programmu, ir jāizveido *Azure Active Directory (Azure AD) marķieris* ar Azure AD lietotni. Pēc tam ir jāizmanto Azure AD marķieris, lai iegūtu *piekļuves pilnvaras* no drošības pakalpojuma.

Lai iegūtu drošības pakalpojuma pilnvaru, rīkojieties šādi:

1. Pieteikties Azure portālā un izmantot to, lai atrastu `clientId` un `clientSecret` savai Supply Chain Management programmai.
1. Panest marķieri Azure Active Directory (`aadToken`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Metode** - `GET`
    - **Pamatteksta saturs (formas dati)**:

        | key | vērtība |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Jums jāsaņem `aadToken` atbilde, kas ir līdzīga šim piemēram.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Formulējiet JSON pieprasījumu, kas ir līdzīgs šim:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Kur:
    - Vērtībai `client_assertion` jābūt `aadToken` tai, kas saņemta iepriekšējā solī.
    - Vērtībai `context` ir jābūt vides ID, kur vēlaties izvietot pievienojumprogrammu.
    - Iestatiet visas citas vērtības, kā parādītas piemērā.

1. Iesniedziet HTTP pieprasījumu ar šādiem rekvizītiem:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Metode** - `POST`
    - **HTTP virsraksts** - iekļaut API versiju (atslēga ir `Api-Version` un vērtība ir `1.0`)
    - **Pamatteksts** - iekļaut JSON pieprasījumu, ko izveidojāt iepriekšējā darbībā.

1. `access_token` jūs saņemsiet atbildē. Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu krājumu redzamības API. Tālāk ir minēts piemērs.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Pieprasījuma paraugs

Jūsu atsaucei šeit ir http pieprasījuma paraugs, jūs varat izmantot jebkuru rīku vai kodēšanas valodu, lai nosūtītu šo pieprasījumu, piemēram,  ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

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
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Konfigurēt krājumu uztveramības API

Pirms pakalpojuma izmantošanas ir jāpabeidz konfigurācijas, kas aprakstītas sekojošās apakšsadaļās. Konfigurācija var atšķirties atkarībā no jūsu vides datiem. Tā galvenokārt ietver četras daļas:

- [Sadalīšana](#partitioning)
- [Dimensiju konfigurācijas](#dimension-configurations)
- [Indeksācija](#indexing)
- [Pielāgots mērījums](#custom-measurement)

#### <a name="partitioning"></a>Sadalīšana

Sadalīšana var būtiski ietekmēt Krājumu uztveramības API veiktspēju. Ir ieteicams definēt shēmu, kas ļauj izmantot mazus datu grupējumus, vienlaikus atļaujot jēgpilnus datu vaicājumus.

`organizationId` (`dataAreaId` Supply Chain Management) vienmēr būs daļa no sadalīšanas, un pēc noklusējuma Krājumu uztveramība ir iestatīta uz sadalījumu pēc dimensijām kā *Vietne + Atrašanās vieta*. Tas nozīmē, ka pakalpojumi vienmēr ir jāvaicā ar šīm filtriem definētajām dimensijām.

> [!NOTE]
> *Vietne* un *Atrašanās vieta* ir divas galvenās noklusējuma dimensijas Krājumu uztveramībai. Supply Chain Management šīs dimensijas tiek sauktas par *Vietni* (`InventSiteId`) un *Noliktavu* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensiju konfigurācijas

Krājumu uztveramība nodrošinās vispārēju noklusējuma dimensiju sarakstu, lai iespējotu vairāku avotu sistēmu integrāciju.

Sekojošajā tabulā ir minētas krājumu dimensijas, kas būs noklusējuma dimensiju nosaukumi Krājumu uztveramībai.

| Dimensiju veids | Dimensijas nosaukums |
|---|---|
| Produkts | `ColorId` |
| Produkts | `SizeId` |
| Produkts | `StyleId` |
| Produkts | `ConfigId` |
| Izsekošana | `BatchId` |
| Izsekošana | `SerialId` |
| Novietojums | `LocationId` |
| Novietojums | `SiteId` |
| Krājumu statuss | `StatusId` |
| Specifiska noliktava | `WMSLocationId` |
| Specifiska noliktava | `WMSPalletId` |
| Specifiska noliktava | `LicensePlateId` |

> [!NOTE]
> Dimensijas tips, kas norādīts iepriekšējā tabulā, ir tikai atsaucei. Nav nepieciešams definēt dimensijas tipu Krājumu uztveramībai.

Ja pielāgota dimensija pastāv un tai ir jāplūst uz noklusēto vērtību, kad to patērē Krājuma uztveramība, varat konfigurēt **Pielāgoto dimensiju** nosaukumu Krājuma uztveramībā.

Ārējās sistēmas piekļūst Krājumu uztveramībai, izmantojot REST API, kas iespējo rīcībā esošo informāciju par norādītajām dimensiju kopām. Lai to izdarītu, Krājumu uztveramība ļauj konfigurēt *ārējā kanāla datu avotu* un avota dimensiju uz *mērķa dimensijām* Krājumu uztveramībā.

Mērķa dimensijām jābūt vienai no sekojošajām:

- Noklusētās dimensijas Krājumu pārredzamībai
- Pielāgotas dimensijas

Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām.

#### <a name="indexing"></a>Indeksācija

Vairākumā gadījumu rīcībā esošie krājumi būs ne tikai visaugstākajā "kopējā" līmenī, bet, iespējams, vēlēsities apskatīt apkopotos rezultātus, pamatojoties uz krājumu dimensijām.

Krājumu pārredzamība nodrošina elastību, ļaujot iestatīt indeksus, kas ir balstīti uz dimensiju vai dimensiju kombināciju.

> [!NOTE]
> Pašlaik varat konfigurēt tikai līdz pieciem indeksiem. Jums ir rūpīgi jāapsver, kuru dimensiju vai dimensiju kombināciju izmantosiet pirms ieviešanas, lai nodrošinātu, ka tā atbilst jūsu biznesa vajadzībām. Piemēram, ja vēlaties vaicāt preces šādi:

- Vaicāt apkopotos rīcībā esošos produktus pēc *Krāsas* un *Izmēra* dimensijām.
- Dažos gadījumos jūs vienkārši vēlaties veikt vaicājumu par preci kopumā.

Ir divi indeksi, kas definēti kā:

- `["ColorId", "SizeId"]`
- `[]`

Tukšas iekavas tiks apkopotas, pamatojoties uz produkta ID nodalījumā.

Indeksēšana definē, kā varat grupēt rezultātus, pamatojoties uz `groupBy` vaicājuma iestatījumu. Šādā gadījumā, ja nedefinējat nevienu `groupBy` vērtību, kopsummas tiks iegūtas pēc `productid`. Pretējā gadījumā, ja definējat `groupBy` kā `groupBy=ColorId&groupBy=SizeId`, jūs saņemsiet atpakaļ vairākas rindas, pamatojoties uz atšķirīgām krāsu un izmēru kombinācijām sistēmā.

Vaicājuma kritērijus var ievietot pieprasījuma pamattekstā.

Šeit ir parauga vaicājums produktam ar krāsu un izmēru kombināciju.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

Laukam `filters` pašreiz tikai `ProductId` atbalsta vairākas vērtības. Ja `ProductId` masīvs ir tukšs, tiks pieprasīti visi produkti.

#### <a name="custom-measurement"></a>Pielāgots mērījums

Noklusējuma mērījumu daudzumi ir saistīti ar Supply Chain Management. Tomēr, iespējams, vēlēsieties daudzumu, kas veidots no noklusēto mērījumu kombinācijas. Lai to paveiktu, var izveidot pielāgoto daudzumu konfigurāciju, kas tiks pievienota rīcībā esošo vaicājumu izvadei.

Funkcionalitāte vienkārši ļauj definēt mērvienību kopu, kas tiks pievienota, un/vai mēru kopa, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.

Piemēram, ar šādu vaicājuma nosacījumu, jūs konfigurēsit pielāgoto mērījumu daudzumu kā `MyCustomAvailableforReservation`, kas tiks patērēts patēriņa sistēmai.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Patēriņa sistēma | Aprēķinātie līdzekļi | Datu avots | Modifikators | Modifikatora aprēķina tips |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Papildinājums |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Papildinājums |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Atņemšana |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Papildinājums |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Atņemšana |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Papildinājums |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Papildinājums |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Atņemšana |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Atņemšana |

Ar to vaicājums uz pielāgoto mērījumu daudzumu atgriezīs tālāk norādīto izvadi.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` izvade tiek balstīta uz aprēķina iestatījumu pielāgotos mērījumos kā:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Rīcībā esošo izmaiņu grāmatošana

Precīzais vietrādis URL, uz kuru tiks izlikts pasākums, būs atkarīgs no jūsu ģeogrāfiskā reģiona. Tam būs šāds formāts:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Kad šis vietrādis URL ir autentificēts, to var izmantot kopā ar HTTP `POST` metodi, lai nosūtītu rīcībā esošo izmaiņu notikumus pakalpojumam.

Īpašu galveni izmanto, lai sazinātos ar Dynamics 365 pakalpojumiem, izmantojot HTTP pieprasījumus, kas norāda Supply Chain Management instances vides ID, ar kuru ir saistīti dati. Piemēram:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 1. piemērs

Šajā piemērā ir parādīts scenārijs, kur tiks iestatīta dimensiju konfigurācija risinājumā Power Apps.

Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos. Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 2. piemērs

Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas. Ja `dimensionDataSource` lauks ir nulle, tukša vai baltstarpa, visām dimensijām ir jābūt pamata dimensijām.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON dokumenta lauku rekvizīti

Iepriekš sniegtajos JSON vaicājuma piemēru laukos ir rekvizīti, kas norādīti šajā tabulā.

| Lauka kods | Apraksts |
|---|---|
| `id` | Unikāls ID noteiktam izmaiņu notikumam. Šis ID tiek izmantots, lai nodrošinātu, ka, ja grāmatošanas laikā sakari ar pakalpojumu neizdodas, notikuma atkārtota iesniegšana nenozīmē, ka viens un tas pats notikums sistēmā tiek skaitīts divas reizes. |
| `organizationId` | Ar notikumu saistītās organizācijas identifikators. Tas attiecas uz Supply Chain Management organizācijām vai datu apgabala ID. |
| `productId` | Attiecīgā produkta identifikators. |
| `quantity` | Daudzums, par kādu ir jāmaina rīcībā esošais krājums. Piemēram, ja plauktam pievienoti 10 jauni beigeļi, šī vērtība ir 10. Ja 3 beigeļi tiks noņemti no plaukta vai pārdoti, šī vērtība būs -3. |
| `dimensionDataSource` | Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots. Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota. Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām. Ja `dimensionDataSource` nav norādīts, jūsu vaicājumos var izmantot tikai vispārīgās noklusējuma dimensijas.   |
| `dimensions` | Dinamisks atslēgu/vērtību pāru kopums. Tās tiks kartētas uz dažām Supply Chain Management dimensijām, bet varat pievienot arī pielāgotas dimensijas (piemēram *Avotu)*, kas var norādīt, ka notikums tika saņemts no Supply Chain Management vai ārējas sistēmas. |

### <a name="querying-current-on-hand"></a>Pašreizējo rīcībā esošo krājumu vaicājums

Pašreizējo rīcībā esošo krājumu vaicājuma galapunkts būs līdzīgs vietrādis URL:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Ar HTTP `POST` metodi tiks veikts vaicājums.

#### <a name="current-on-hand-query-example-1"></a>Pašreizējais rīcībā esošais vaicājums 1. piemērs

Šajā piemērā ir parādīts scenārijs, kurā jau ir iestatīta dimensiju konfigurācija risinājumā Power Apps.

Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos. Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām. Varat norādīt `DimensionDataSource` `filters` un norādīt pielāgotās dimensijas gan `filters`, gan `groupByValues`. Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Pašreizējais rīcībā esošais vaicājums 2. piemērs

Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas. Ja `dimensionDataSource` lauks sadaļā `filters` ir nulle, tukšs vai kā atstarpe, visām dimensijām ir jābūt pamata dimensijām.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Piemēra atgriešanas rezultāts

Iepriekšējos piemēros parādītie vaicājumi var atgriezt, piemēram, šādu rezultātu.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Ievērojiet, ka daudzuma lauki ir strukturēti kā mērvienību vārdnīca un to saistītās vērtības.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]