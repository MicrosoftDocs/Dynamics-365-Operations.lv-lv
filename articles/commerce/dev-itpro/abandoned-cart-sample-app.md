---
title: Atrast atstātos grozus un nosūtīt debitoriem paziņojumus
description: Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce pielāgot atstāto groza savienotāja parauga programmu, lai noteiktu atstātos grozus un sūtīt atgādinājumu e-pasta paziņojumus debitoriem.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82848f1ff068cea0adfc6ec1b33fc4bb035f78dc
ms.sourcegitcommit: 374bbdde90fc9a68c0799158a50409bfbe8ca64e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353375"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Atrast atstātos grozus un nosūtīt debitoriem paziņojumus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce pielāgot atstāto groza savienotāja parauga programmu, lai noteiktu atstātos grozus un sūtīt atgādinājumu e-pasta paziņojumus debitoriem.

Spēja atgūt ieņēmumus un aizturēt debitorus, izmantojot atstātus groza paziņojumus, ir svarīga iespēja, kas Dynamics 365 Commerce atbalsta. Pielāgojot Commerce atstāto groza savienotāja parauga programmu, mazumtirgotāji var piekļūt iepirkumu groziem sistēmā Retail Server, kas netika modificēti laika logā, ko nosaka mazumtirgotāji. Šos grozus pēc tam var izgūt, palielināt ar produkta un debitora datiem un pārsūtīt trešās puses e-pasta mārketinga nodrošinātājam, kas var ģenerēt e-pasta paziņojumus un nosūtīt tiem klientus.

Atstātais groza e-pasta paziņojums, ka debitori saņem var ietvert šādu informāciju:

- Debitora vārds.
- Debitora uzvārds.
- Debitora e-pasta adrese.
- URL, kas atgriež debitoru grozam.
- Darbības valūta.
- Debitora grozā esošo preču saraksts. Katrai precei ir iekļauta šāda informācija:

    - Preces parādāmais nosaukums
    - Preces ID (izmanto, lai saliktu URL preces apraksta lapā)
    - Preces attēls, ko var automātiski mainīt, lai pielāgotu dažādus skata izmērus
    - Preces attēla alternatīvais teksts
    - Preces vienības cena

## <a name="abandoned-cart-connector-sample"></a>Atstātais groza savienotāja paraugs

Savienotāja modelis, ko korporācija Microsoft nodrošina, izmantojot mazumtirdzniecības programmatūras izstrādes komplektu (SDK), tiek aktivizēta atstāta groza informācija, kas ir izgūta un nosūtīta trešās puses e-pasta mārketinga nodrošinātājam. Šis savienotājs apstrādā sakarus ar mazumtirdzniecības serveri, drošībasm tiek izmantots Azure atslēgas izpildes līdzeklis, tiek plānota groza izgūšana noteiktam laika logam un izgūti pasūtījumi un preču dati. Tajā ir sniegts arī parauga ieviešana integrācijai ar trešās puses e-pasta mārketinga nodrošinātāju. Savienotājs ir izveidots, lai komunicēt [ar Emarsys](https://emarsys.com) ārpus lodziņa. Tomēr to var viegli pielāgot, lai integrētu ar citiem risinājumiem, piemēram, Konstants kontakts, Pasta sūtījums un SendGrid.

Šajā attēlā redzami atstātās groza savienotāja parauga programmas komponenti.

![Atstātās groza savienotāja parauga programmas komponenti](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Dažiem reģioniem ir nepieciešams, lai debitori varētu izvēlēties, vai viņu groza dati tiktu nodoti e-pasta mārketinga nodrošinātājam vai pieprasīt, lai tiktu noņemti viņu dati. Tomēr Korporācija Microsoft nesniedz šīs opcijas debitoriem. Tāpēc, ja plānojat veikt darījumus reģionos, kas tos pieprasa, jums jānodrošina nepieciešamā infrastruktūra un pielāgojumi, lai sekotu klientu preferences un, balstoties uz tiem, neļautu debitora datus nodot jūsu e-pasta platformai. Jādefinē arī process debitora datu tīrīšanai no e-pasta mārketinga sniedzēja pēc debitora pieprasījuma.

## <a name="obtain-the-code-sample"></a>Iegūt koda paraugu

Atstātā groza savienotāja parauga programma ir iekļauta Retail SDK versijā 10.0.16. Kodu var atrast šeit: **\\ RetailSDKCodeSampleExtensionsRetailServerExtensions.AbandonedCartSample \\\\\\\\**. Papildinformāciju par mazumtirdzniecības SDK un to, kur to iegūt, skatiet mazumtirdzniecības [programmatūras izstrādes komplekts (SDK](retail-sdk/retail-sdk-overview.md)).

> [!NOTE]
> Kaut arī parauga kods pirmo reizi ir pieejams versijā 10.0.16, tas ir saderīgs ar versiju 10.0.13 un vēlākiem Retail Server būvējumus.

## <a name="prerequisites-and-dependencies"></a>Priekšnoteikumi un atkarības

Pirms varat izvietot un konfigurēt atstāto groza savienotāja parauga kodu, ir jāizpilda šādi priekšnoteikumi.

### <a name="access-to-commerce-resources"></a>Piekļuve Commerce resursiem

Lai konfigurētu un izvietotu atstāto groza savienotāja programmu, jums jābūt piekļuvei šādiem Commerce resursiem:

- Administratora piekļuve commerce headquarters jūsu videi
- Pieeja vides Microsoft Dynamics Lifecycle Services (LCS) projektam

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Atstātā groza savienotāja programma izmanto Azure Cosmos DB, lai izsekotu iepriekš izgūto grozu ID un laikspiedolus. Varat izmantot azure, Cosmos DB lai pastāv šos datus, vai arī varat pielāgot koda paraugu, lai to integrētu ar citu datu glabāšanas opciju. Papildinformāciju par Azure skatiet Cosmos DB sadaļā Azure [!Cosmos DB](/azure/cosmos-db/introduction)

Ja izmantojat Azure Cosmos DB, pirms parauga palaišanas ir jāizpilda tālāk norādītie priekšnosacījumi.

- Jums ir jābūt aktīvam Azure kontam Cosmos DB. Ja jums nav konta, skatiet sadaļu Datu [bāzes konta izveide](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Jums ir jāizgūst **URI** un **PRIMĀRĀS** atslēgas (**vai SEKUNDĀRĀS** ATSLĒGAs) **vērtības** no Azure Cosmos DB portāla konta atslēgām. Papildinformāciju par to, kā izgūt galapunkta un atslēgas informāciju jūsu Azure Cosmos DB kontam, [skatiet sadaļā Skatīt, kopēt un reģenerēt piekļuves atslēgas un paroles](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Atstātā groza savienotāja programma izmanto atslēgu Key To, lai saglabātu nosaukumus un noslēpumus dažādiem komponentiem, kam nepieciešama droša piekļuve.

Lai iestatītu atslēgu, sekojiet šiem soļiem.

1. Izmantojot portālu, izpildiet [norādījumus, kas atrodas azure steka pārkraušanas centrā, pārvaldīt atslēgu](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true) Uzkrāju.
2. Izveidojiet noslēpumus šādai informācijai:

    - Emarsys lietojumprogrammas interfeisa (API) lietotājvārds un API noslēpums
    - Atstāts groza programmas ID un noslēpums

Atstātā groza savienotāja parauga kodā tiek izmantoti Azure noklusējuma akreditācijas dati, lai piekļūtu atslēgai Loma. Jums jānorāda saraksta **un lasīšanas** **atļaujas** identitātei, kuru plānojat izmantot, lai piekļūtu atslēgas lietotājam.

Papildinformāciju par Azure noklusējuma akreditācijas datiem skatiet sadaļā [DefaultAzureCredential Class](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Izveidot nomniekam atstātu groza savienotāja parauga programmas ID Azure AD

Ir jāizveido atstāta groza savienotāja parauga programmas ID (Azure Active Directory AD) nomniekam. Informāciju par to, kā izveidot programmas ID, skatiet Sadaļā [Portāla lietošana, lai izveidotu lietojumprogrammu Azure AD un pakalpojuma vadītāju, kas var piekļūt resursiem](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Pievienot atstāto groza savienotāja parauga programmas ID mazumtirdzniecības servera API atļauto sarakstam

Pēc tam Retail Server API atļauto sarakstam ir jāpievieno atcelta groza savienotāja parauga programmas ID. Papildinformāciju par to, kā pievienot programmas ID azure atļauto sarakstam, skatiet sadaļā [Pakalpojums pakalpojuma autentifikācijai mazumtirdzniecības serverī](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigurēt atstāto groza savienotāja parauga programmu

Lai konfigurētu atcelto groza savienotāja parauga programmu, **modificējiet appSettings.json** **konfigurācijas failu, kas atrodas direktoriju AbortedCartDetectionSample** saknē. Tabulās ir aprakstīti konfigurācijas faila rekvizīti.

### <a name="keyvaultoptions"></a>Taustiņš KeyVaultOptions

| Rekvizīts    | Apraksts |
| ----------- | ----------- |
| Taustiņš KeyVaultURI | Tās atslēgas Domēna nosaukumu sistēmas (DNS) nosaukums, kas tiek izmantota Azure portālā. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions (tikai mazumtirdzniecības serveri)

| Rekvizīts                                      | Apraksts |
| --------------------------------------------- | ----------- |
| Nomnieka ID                                      | Azure Azure AD nomnieka ID. |
| RetailServerAudienceId                        | Mazumtirdzniecības servera mērķauditorijas ID. Var atstāt noklusēto vērtību. |
| AppIdKeyVaultSecretName                       | Tā noslēpuma nosaukums, ko izveidojāt atstātajiem grozu savienotāja parauga programmas ID. |
| AppSecretKeyVaultSecretName                   | Tā noslēpuma vārds, kas glabā programmas noslēpumu atstātā groza savienotāja parauga programmas ID. |
| RetailServerUrl (tikai mazumtirdzniecības serveris)                               | Retail Server instances URL. Šo vērtību var atrast LCS. |
| OperatingUnitNumber                           | Pārvaldības struktūrvienības numurs (OUN). Šo vērtību varat atrast galvenajā birojā Commerce Headquarters. |
| IncludeAragonedCartsModifiedSinceLastMinutes | Laika loga sākums atstātajiem groziem, kurus vēlaties izgūt. Vērtība tiek izteikta kā minūšu skaits pirms pašreizējā laika. Piemēram, iestatiet šo rekvizītu par 120 **, lai izgūtu visus grozus,** kas pēdējoreiz tika modificēti laikā no pirms 120 **minūtēm līdz laika loga beigām, ko definēja rekvizīts ExcludeArenonedCartsModifiedSinceLastMinutes**. |
| ExcludeAmunonedCartsModifiedSinceLastMinutes | Laika loga beigas atstātajiem groziem, kurus vēlaties izgūt. Vērtība tiek izteikta kā minūšu skaits pirms pašreizējā laika. Piemēram, **ja rekvizīts IncludeAragonedCartsModifiedSinceLastMinutes ir iestatīts** **uz 120, iestatiet šo rekvizītu uz 30** **,** lai izgūtu visus grozus, kas tika modificēti laikā pirms 120 minūtēm līdz 30 minūtēm. Praksē šis rekvizīts nosaka laiku, ko vēlaties gaidīt, pirms grozs tiek deklarēts kā atstāts. |
| ReturnToCartUrl                               | Url grozam jūsu e-komercijas vietnē formātā, kas tiek izmantots **failā app.config**. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions (azureCosmosOptions)

Azure tiek saglabāti atstātās groza izgūšanas darbu statuss, groza IP un modificētie laikspiedoļi Cosmos DB. Pēc noklusējuma konfigurācijas faila iestatījumi norāda uz vietējo Azure emulatora instanci Cosmos DB. Kad izvietojat savienotāju ražošanā, šie iestatījumi ir jāatjaunina, lai tie norāda uz Azure Cosmos DB instanci jūsu Azure abonementā. Lai pārbaudītu vietējos un slāņus, varat izmantot [Azure Emulatorus](/azure/cosmos-db/local-emulator).

| Rekvizīts    | Apraksts |
| ----------- | ----------- |
| EndPointUri (beigu uri) | Galapunkta URI, ko nodrošina Azure vai modulis. |
| PrimaryKey (Primārais taustiņš)  | Primārā atslēga, ko nodrošina Azure vai modulis. |
| DatabaseId  | Datu bāzes ID. Varat atstāt noklusēto vērtību vai nodrošināt savu. |
| ContainerId | Konteinera ID. Varat atstāt noklusēto vērtību vai nodrošināt savu. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Ja integrējat ar e-pasta mārketinga nodrošinātāju, kas nav Emarsys, **ir jāpaplašina IEmailProvider interfeiss**, atbilstoši komunicēt ar šo nodrošinātāju.

| Rekvizīts                      | Apraksts |
| ----------------------------- | ----------- |
| ApiUrl (apiUrl)                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Emarsys izveidotā ārējā notikuma ieraksta ID. Tās kampaņas iestatījumos, kuru **izveidojāt**, lai nosūtītu atstātos groza e-pasta paziņojumus, varat atrast vērtību zem Pogas Trigera iestatījumi. |
| ApiUserNameKeyVaultSecretName | Tās atslēgas nosaukums, kurā tiek glabāts Emarsys API lietotāja vārds. |
| ApiSecretKeyVaultSecretName   | Tās atslēgas nosaukums, kur tiek glabāts Emarsys API noslēpums. |
| EmarsysContactKeyId           | E-pasta kolonnas ID Emarsys kontakta datu bāzē. Noklusējuma vērtība ir **3**, un to nedrīkst mainīt. |

### <a name="mediaoptions"></a>Starpniecības

Ja izmantojat e-komercijas iespējas pakalpojumā Commerce, varat izmantot Commerce ciparparaksta pārvaldību, lai izgūtu preču attēlus. Papildinformāciju par attēlu mainītāja iespējām ciparu līdzekļu pārvaldībā skatiet sadaļā [ImageSettings skata porta konfigurācija](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Rekvizīts                             | Apraksts |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Vietnes ciparu līdzekļu pārvaldnieka saknes URL. Vērtību programmā Commerce Headquarters var atrast **rekvizītu atslēgā Media Server Base URL** **, kas atrodas mazumtirdzniecības un Commerce \> Channel setup \> kanāla** profilos. |
| ImageViewPorts                       | Konteinera zars individuālā skatījuma porta konfigurācijām. |
| ImageViewPorts/skatījums              | Skatījuma definīcija. Izmantojiet šo rekvizītu, lai norādītu skata skata diapazonu pikseļos. Piemēram, parādot šī rekvizīta piejaukums, skatiet **appSettings.json** konfigurācijas failu. |
| ImageViewPorts/imageWidth            | Skatījuma attēla platums pikseļos. |
| imageViewPorts/imageHecaur           | Skatījuma attēla augstums pikseļos. |
| imageViewPorts/useForDefaultImageTag | Truefalse **·**/**·**`<picture>` vērtība, kas norāda, vai ar skatījumu definētās attēla dimensijas ir jāizmanto, ja HTML tags netiek atbalstīts tīmekļa pārlūkam vai e-pasta klientam. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
