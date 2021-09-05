---
title: Noliktavas programmas instalēšana un savienošana
description: Šajā tēmā ir paskaidrots, kā instalēt noliktavas programmu katrā jūsu mobilajā ierīcē un konfigurēt to, lai izveidotu savienojumu ar Microsoft Dynamics 365 Supply Chain Management vidi. Varat katru ierīci konfigurēt manuāli vai importēt savienojuma iestatījumus, izmantojot failu vai skenējot QR kodu.
author: MarkusFogelberg
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 094d7f0f5642653c6e059952783041b1430e98d6
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384639"
---
# <a name="install-and-connect-the-warehouse-app"></a>Noliktavas programmas instalēšana un savienošana

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šajā tēmā ir aprakstīts, kā konfigurēt veco Warehouse programmu (kas tagad ir novecojusi). Ja vēlaties skatīt informāciju par jaunās lietotnes Warehouse Management mobile konfigurēšanu (pašreiz publiskā priekšskatījumā), skatiet sadaļu lietotnes [Warehouse Management mobile instalēšana un savienošana](install-configure-warehouse-management-app.md).

> [!NOTE]
> Šajā tēmā aprakstīts, kā konfigurēt noliktavas lietotni mākoņa izvietojumiem. Ja meklējat informāciju par to, kā konfigurēt noliktavas lietotni lokālajiem izvietojumiem, skatiet [Warehousing lokālajiem izvietojumiem](../../fin-ops-core/dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Noliktavas programma ir pieejama Google Play veikalā un Microsoft Store. Tā tiek nodrošināta kā savrups komponents. Tāpēc tā ir jālejupielādē katrā ierīcē un pēc tam jākonfigurē, lai izveidotu savienojumu ar Microsoft Dynamics 365 Supply Chain Management vidi.

Šajā tēmā ir paskaidrots, kā instalēt noliktavas programmu katrā jūsu mobilajā ierīcē un konfigurēt to, lai izveidotu savienojumu ar Supply Chain Management vidi. Varat katru ierīci konfigurēt manuāli vai importēt savienojuma iestatījumus, izmantojot failu vai skenējot QR kodu.

## <a name="system-requirements"></a>Sistēmas prasības

Noliktavas programma ir pieejama Windows un Android operētājsistēmās. Lai varētu lietot šīs programmas jaunāko versiju, mobilajās ierīcēs ir jābūt instalētai kādai no tālāk norādītajām operētājsistēmām:

- Windows 10 (universālā Windows platforma \[UWP\]) rudens veidotāju atjauninājums 1709 (būvējums 10.0.16299) vai jaunāka versija
- Android 4.4 vai jaunāka versija

> [!NOTE]
> Ja ir jāatbalsta vecākas Windows ierīces, kas nevar palaist jaunāko Windows versiju, jūs joprojām varat lejupielādēt Microsoft Store noliktavas programmas versiju 1.6.3.0. Šī versija darbosies Windows 10 (UWP) novembra atjauninājumā 1511 (būvējums 10.0.10586) vai jaunākā versijā. Tomēr ņemiet vērā, ka šī noliktavas programmas versija neatbalsta savienojumu iestatījumu masveida izvietošanu. Tāpēc ir [manuāli jākonfigurē savienojums](#config-manually) katrā ierīcē, kurā darbojas šī programmas versija.

## <a name="get-the-warehouse-app"></a>Noliktavas programmas iegūšana

Lai lejupielādētu programmu, izmantojiet vienu no šīm saitēm:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations - Warehousing Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing - Dynamics 365 Google Play veikalā](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Mazākiem izvietojumiem, iespējams, vēlēsities instalēt programmu no katras ierīces attiecīgā veikala un pēc tam manuāli konfigurēt savienojumu ar jūsu izmantotajām vidēm. Tomēr, noliktavas programmas versijā 1.7.0.0 un jaunākās, varat arī automatizēt programmu izvietošanu un/vai konfigurāciju. Šī pieeja varētu būt ērta, ja pārvaldāt daudzas ierīces un izmantojat mobilās ierīces pārvaldības un mobilās lietojumprogrammas pārvaldības risinājumu, piemēram, [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Papildinformāciju par Intune izmantošanu, lai pievienotu lietojumprogrammas, skatiet [Programmu pievienošana Microsoft Intune](/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory

Lai noliktavas programma varētu mijiedarboties ar noteiktu Supply Chain Management serveri, pakalpojumā Azure Active Directory (Azure AD) ir jāreģistrē tīmekļa pakalpojuma lietojumprogramma Supply Chain Management nomniekam. Nākamajā procedūrā ir parādīts viens šī uzdevuma izpildes veids. Lai iegūtu detalizētu informāciju un alternatīvas, skatiet saites procedūras beigās.

1. Tīmekļa pārlūkā dodieties uz vietni [https://portal.azure.com](https://portal.azure.com/).
1. Ievadiet tā lietotāja vārdu un paroli, kuram ir piekļuve Azure abonementam.
1. Azure portāla kreisajā navigācijas rūtī atlasiet **Azure Active Directory**.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Pārliecinieties, ka strādājat ar Azure AD instanci, kas izmantota programmatūrā Supply Chain Management.
1. Sarakstā **Pārvaldīt** atlasiet **Programmu reģistrācijas**.

    ![Programmu reģistrācijas.](media/app-connect-azure-register.png "Programmu reģistrācijas")

1. Rīkjoslā atlasiet **Jauna reģistrācija**, lai atvērtu vedni **Lietojumprogrammas reģistrācija**.
1. Ievadiet lietojumprogrammas nosaukumu, atlasiet opciju **Konti tikai šajā organizatoriskajā direktorijā** un pēc tam atlasiet **Reģistrs**.

    ![Lietojumprogrammas reģistrācijas vednis.](media/app-connect-azure-register-wizard.png "Lietojumprogrammas reģistrācijas vednis")

1. Tiek atvērta jūsu jaunā programmas reģistrācija. Pierakstiet **Lietojumprogrammas (klienta) ID** vērtību, jo tā būs nepieciešama vēlāk. Šis ID turpmāk šajā tēmā tiks dēvēts kā *klienta ID*.

    ![Lietojumprogrammas (klienta) ID.](media/app-connect-azure-app-id.png "Lietojumprogrammas (klienta) ID")

1. Sarakstā **Pārvaldīt** atlasiet **Sertifikāts & noslēpumi**. Pēc tam atlasiet vienu no tālāk norādītajām pogām, atkarībā no tā, kā vēlaties konfigurēt programmu autentifikācijai. (Papildinformāciju skatiet sadaļā [Autentificēt, izmantojot sertifikātu vai klienta noslēpumu](#authenticate) šīs tēmas turpinājumā.)

    - **Augšupielādēt sertifikātu** – augšupielādēt sertifikātu, ko izmantot kā noslēpumu. Ir ieteicams izmanto šo pieeju, jo tā ir drošāka un to var arī pilnīgāk automatizēt. Ja izmantojat noliktavas programmu Windows ierīcēs, pierakstiet **Nospiedums** vērtību, kas tiek parādīta pēc sertifikāta augšupielādes. Šī vērtība būs nepieciešama, konfigurējot sertifikātu Windows ierīcēs.
    - **Jauns klienta noslēpums** – izveidojiet atslēgu, ievadot atslēgas aprakstu un ilgumu sadaļā **Paroles**, un pēc tam atlasiet **Pievienot**. Izveidojiet atslēgas kopiju un glabājiet to drošībā.

    ![Sertifikāts & noslēpumi.](media/app-connect-azure-authentication.png "Sertifikāts & noslēpumi")

Papildinformāciju par to, kā iestatīt tīmekļa pakalpojuma lietojumprogrammas Azure AD, skatiet tālāk norādītos resursus:

- Instrukcijas, kurās parādīts, kā izmantot Windows PowerShell, lai Azure AD iestatītu tīmekļa pakalpojumu lietojumprogrammas, skatiet [Kā: izmantot Azure PowerShell, lai izveidotu pakalpojuma vadītāju ar sertifikātu](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Pilnīgu informāciju par to, kā manuāli izveidot tīmekļa pakalpojumu lietojumprogrammu programmā Azure AD, skatiet tālāk norādītās tēmas:

    - [Īsa pamācība: lietojumprogrammas reģistrācija platformā Microsoft Identity](/azure/active-directory/develop/quickstart-register-app)
    - [Kā: izmantot portālu, lai izveidotu Azure AD lietojumprogrammu un pakalpojuma vadītāju, kas var piekļūt resursiem](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Izveidot un konfigurēt lietotāja kontu programmatūrā Supply Chain Management

Lai jūsu Azure AD lietojumprogrammu varētu izmantot Supply Chain Management, rīkojieties šādi.

1. Izveidojiet lietotāju, kas atbilst noliktavas programmas lietotāja akreditācijas datiem:

    1. Programmatūrā Supply Chain Management dodieties uz sadaļu **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
    1. Izveidojiet lietotāju.
    1. Piešķiriet noliktavas mobilās ierīces lietotāju.

    ![Piešķiriet noliktavas mobilās ierīces lietotāju.](media/app-connect-app-users.png "Piešķiriet noliktavas mobilās ierīces lietotāju")

1. Saistiet savu Azure AD lietojumprogrammu ar noliktavas programmas lietotāju:

    1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Azure Active Directory lietojumprogrammas**.
    1. Izveidojiet rindu.
    1. Ievadiet klienta ID, kuram veicāt piezīmi iepriekšējā sadaļā, piešķiriet tam nosaukumu un atlasiet tikko izveidoto lietotāju. Ieteicams atzīmēt visas jūsu ierīces. Pēc tam, to nozaudēšanas gadījumā, varēsit viegli liegt to piekļuvi Supply Chain Management, izmantojot šo lapu.

    ![Azure Active Directory lietojumprogrammas.](media/app-connect-aad-apps.png "Azure Active Directory pieteikumi")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentificēt, izmantojot sertifikātu vai klienta noslēpumu

Autentifikācija ar Azure AD nodrošina drošu veidu, kā pievienot mobilo ierīci Supply Chain Management. Autentifikāciju var veikt, izmantojot klienta noslēpumu vai sertifikātu. Ja importēsit savienojuma iestatījumus, ieteicams izmantot sertifikātu nevis klienta noslēpumu. Tā kā klienta noslēpums vienmēr ir jāglabā drošībā, to nevar importēt no savienojuma iestatījumu faila vai QR koda, kā aprakstīts tālāk šajā tēmā.

Sertifikātus var izmantot kā noslēpumus, lai pierādītu lietojumprogrammas identitāti, kad tiek pieprasīta pilnvara. Sertifikāta publiskā daļa tiek augšupielādēta programmu reģistrācijā Azure portālā, savukārt pilnais sertifikāts ir jāizvieto katrā ierīcē, kurā ir instalēta noliktavas programma. Jūsu organizācija ir atbildīga par sertifikāta pārvaldību attiecībā uz rotāciju un tā tālāk. Varat izmantot pašparakstītus sertifikātus, bet vienmēr izmantojiet neeksportējamus sertifikātus.

Sertifikātam ir jābūt pieejamam lokāli katrā ierīcē, kurā tiek palaista noliktavas programma. Papildinformāciju par to, kā pārvaldīt Intune kontrolēto ierīču sertifikātus, ja lietojat Intune, skatiet sadaļā [Sertifikātu izmantošana autentifikācijai programmā Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurējiet lietojumprogrammu, importējot savienojuma iestatījumus

Lai atvieglotu lietojumprogrammas uzturēšanu un izvietošanu daudzās mobilajās ierīcēs, savienojuma iestatījumus var importēt tā vietā, lai tos manuāli ievadītu katrā ierīcē. Šajā sadaļā ir paskaidrots, kā izveidot un importēt iestatījumus.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Savienojuma iestatījumu faila vai QR koda izveidošana

Varat importēt savienojuma iestatījumus no faila vai QR koda. Abām pieejām vispirms ir jāizveido iestatījumu fails, kas izmanto JavaScript Object Notation (JSON) formātu un sintaksi. Failā jābūt ietvertam savienojumu sarakstam, kas satur atsevišķus pievienojamos savienojumus. Tālāk esošajā tabulā apkopoti parametri, kas ir jānorāda savienojuma iestatījumu failā.

| Parametrs | apraksts |
| --- | --- |
| ConnectionName | Norādiet savienojuma iestatījumu nosaukumu. Maksimālais garums ir 20 rakstzīmes. Tā kā šī vērtība ir unikāls savienojuma iestatījumu identifikators, pārliecinieties, vai tas sarakstā ir unikāls. Ja ierīcē jau pastāv savienojums ar tādu pašu nosaukumu, importētā faila iestatījumi to ignorēs. |
| ActiveDirectoryClientAppId | Norādiet klienta ID, kuru pierakstījāt, iestatot Azure AD, sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Norādiet Supply Chain Management saknes vietrādi URL. |
| ActiveDirectoryTenant | Norādiet Azure AD domēna nosaukumu, kuru izmantojat ar Supply Chain Management serveri. Šīs vērtības forma ir `https://login.windows.net/<your-Azure-AD-domain-name>`. Tālāk minēts piemērs: `https://login.windows.net/contosooperations.onmicrosoft.com`. Papildinformāciju par to, kā atrast Azure AD domēna nosaukumu, skatiet sadaļā [Svarīgu lietotāja ID atrašana](/partner-center/find-ids-and-domain-names). |
| Uzņēmums | Norādiet to juridisko personu programmatūrā Supply Chain Management, ar kuru lietojumprogrammai ir jāizveido savienojums. |
| ConnectionType | (Neobligāti) Norādiet, vai savienojuma iestatījumam jāizmanto sertifikāts vai klienta noslēpums, lai izveidotu savienojumu ar vidi. Derīgās vērtības ir *"certificate"* un *"clientsecret"*. Noklusējuma vērtība ir *"certificate"*.<p>**Piezīme:** klienta noslēpumus nevar importēt.</p> |
| IsEditable | (Neobligāti) Norādiet, vai programmas lietotājs var rediģēt savienojuma iestatījumus. Derīgās vērtības ir *"true"* un *"false"*. Noklusējuma vērtība ir *"true"*. |
| IsDefault | (Neobligāti) Norādiet, vai savienojums ir noklusējuma savienojums. Savienojums, kas ir iestatīts kā noklusējuma savienojums, tiks automātiski iepriekš atlasīts, atverot programmu. Kā noklusējuma savienojumu var iestatīt tikai vienu savienojumu. Derīgās vērtības ir *"true"* un *"false"*. Noklusējuma vērtība ir *"false"*. |
| CertificateThumbprint | (Neobligāti) Windows ierīcēm var norādīt sertifikāta savienojuma nospiedumu. Android ierīcēs programmas lietotājam ir jāatlasa sertifikāts, kad savienojums tiek izmantots pirmo reizi. |

Tālāk esošajā piemērā ir parādīts derīgs savienojuma iestatījumu fails, kas satur divus savienojumus. Kā redzat, savienojumu saraksts (ar nosaukumu *"ConnectionList"* failā) ir objekts ar masīvu, kas saglabā katru savienojumu kā objektu. Katrs objekts ir jāietver figūriekavās ({}) un jāatdala ar komatu, un masīvs ir jāietver kvadrātiekavās (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Informāciju varat saglabāt kā JSON failu, vai ģenerēt QR kodu ar tādu pašu saturu. Ja saglabāsit informāciju kā failu, ieteicams to saglabāt, izmantojot noklusējuma nosaukumu, *connections.json*, it īpaši, ja to saglabāsit noklusējuma atrašanās vietā katrā mobilajā ierīcē.

### <a name="save-the-connection-settings-file-on-each-device"></a>Savienojuma iestatījumu faila saglabāšana katrā ierīcē

Parasti tiek izmantots ierīču pārvaldības rīks vai skripts, lai sadalītu savienojuma iestatījumu failus katrai ierīcei, ko pārvaldāt. Ja, saglabājot savienojuma iestatījumu failu katrā ierīcē, izmantojat noklusējuma nosaukumu un atrašanās vietu, noliktavas programma to automātiski importēs pat pirmajā palaišanas reizē pēc programmas instalēšanas. Ja failam izmantojat pielāgotu nosaukumu vai atrašanās vietu, programmas lietotājam pirmās palaišanas reizē ir jānorāda vērtības. Tomēr pēc tam programma turpinās izmantot norādīto nosaukumu un atrašanās vietu.

Katru reizi, kad programma tiek startēta, tā atkārtoti importē savienojuma iestatījumus no iepriekšējās atrašanās vietas, lai noteiktu, vai ir veiktas kādas izmaiņas. Programma atjauninās tikai tos savienojumus, kam ir tādi paši nosaukumi kā savienojumiem savienojuma iestatījumu failā. Lietotāja izveidotie savienojumi, kas izmanto citus nosaukumus, netiks atjaunināti.

Savienojumu nevar noņemt, izmantojot savienojuma iestatījumu failu.

Kā jau minēts, noklusējuma faila nosaukums ir *connections.json*. Noklusējuma faila atrašanās vieta ir atkarīga no tā, vai izmantojat Windows ierīci vai Android ierīci:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Parasti ceļi tiek izveidoti automātiski pēc programmas pirmās palaišanas reizes. Tomēr tos var izveidot manuāli, ja savienojuma iestatījumu fails pirms instalēšanas ir jāpārsūta uz ierīci.

> [!NOTE]
> Ja programma ir atinstalēta, noklusējuma ceļš un tā saturs tiek noņemts.

### <a name="import-the-connection-settings"></a>Savienojuma iestatījumu importēšana

Lai importētu savienojuma iestatījumus no faila vai QR koda, rīkojieties šādi.

1. Atveriet noliktavas programmu savā mobilajā ierīcē.
1. Dodieties uz **Savienojuma iestatījumi**.
1. Opciju **Izmantot demonstrācijas režīmu** iestatiet uz _Nē_.

    ![Izmantot demonstrācijas režīma opciju.](media/app-connect-app-demo-mode.png "Izmantot demonstrācijas režīma opciju")

1. Atlasiet **Atlasīt failu** vai **Skenēt QR kodu**, atkarībā no tā, kā vēlaties importēt iestatījumus:

    - Ja importējat savienojuma iestatījumus no faila, iespējams, programma jau ir atradusi failu, ja pēc saglabāšanas tika izmantots noklusējuma nosaukums un noklusējuma atrašanās vieta. Pretējā gadījumā atlasiet **Atlasīt failu**, pārlūkojiet failu jūsu lokālajā ierīcē un atlasiet to. Ja atlasīsit pielāgotu atrašanās vietu, programma to saglabās un automātiski izmantos nākamreiz.
    - Ja importējat savienojuma iestatījumus, skenējot QR kodu, atlasiet **Skenēt QR kodu**. Programma pieprasa atļauju izmantot ierīces kameru. Pēc atļaujas piešķiršanas, kamera tiek startēta, lai to izmantotu skenēšanai. Atkarībā no ierīces kameras kvalitātes un QR koda sarežģītības, var izrādīties grūti iegūt pareizu skenējumu. Šādā gadījumā mēģiniet samazināt QR koda sarežģītību, ģenerējot tikai vienu savienojumu katram QR kodam. (Pašlaik QR koda skenēšanai var izmantot tikai ierīces kameru.)

    ![Savienojuma iestatījumu importēšana.](media/app-connect-app-select-file.png "Savienojuma iestatījumu importēšana")

1. Kad savienojuma iestatījumi ir veiksmīgi ielādēti, lapas augšējā kreisajā stūrī atlasiet pogu **Atgriezties** (kreisā bultiņa).

    ![Savienojuma iestatījumu ielādēšana.](media/app-connect-app-settings-loaded.png "Savienojuma iestatījumu ielādēšana")

1. Ja izmantojat Android ierīci un autentifikācijai izmantojat sertifikātu, ierīce piedāvā izvēlēties sertifikātu.

    ![Izvēlēties Android ierīcē piedāvāto sertifikātu.](media/app-connect-app-choose-cert.png "Izvēlēties Android ierīcē piedāvāto sertifikātu")

1. Programma izveido savienojumu ar jūsu Supply Chain Management serveri un parāda pierakstīšanās lapu.

    ![Pierakstīšanās lapa.](media/app-connect-sign-in.png "Pierakstīšanās lapa")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Lietojumprogrammas manuāla konfigurēšana

Ierīcē instalēto programmu var manuāli konfigurēt, lai izveidotu savienojumu ar Supply Chain Management serveri, izmantojot Azure AD lietojumprogrammu.

1. Atveriet noliktavas programmu savā mobilajā ierīcē.
1. Dodieties uz **Savienojuma iestatījumi**.
1. Opciju **Izmantot demonstrācijas režīmu** iestatiet uz _Nē_.

    ![Demonstrācijas režīms izslēgts.](media/app-connect-app-select-file.png "Demonstrācijas režīms izslēgts")

1. Pieskarieties laukā **Atlasīt savienojumu**, lai izvērstu iestatījumus, kas nepieciešami savienojuma datu manuālai ievadīšanai.

    ![Manuālā savienojuma lauki.](media/app-connect-manual-connect.png "Manuālā savienojuma lauki")

1. Ievadiet sekojošo informāciju:

    - **Izmantot klienta noslēpumu** – iestatiet šo opciju uz _Jā_, lai izmantotu klienta noslēpumu autentificējoties Supply Chain Management. Iestatiet to uz _Nē_, lai autentifikācijai izmantotu sertifikātu. (Papildinformāciju skatiet [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).)
    - **Savienojuma nosaukums** — ievadiet jaunā savienojuma nosaukumu. Šis nosaukums tiks parādīts laukā **Atlasīt savienojumu** nākamajā reizē, kad atvērsit savienojuma iestatījumus. Jūsu ievadītajam nosaukumam jābūt unikālam. (Citiem vārdiem sakot, tam ir jābūt atšķirīgam no visiem pārējiem ierīcē saglabātajiem savienojumu nosaukumiem, ja tajā tiek saglabāti citi savienojumu nosaukumi.).
    - **Active direktorija klienta ID** – ievadiet klienta ID, kuru pierakstījāt, iestatot Azure AD sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Active direktorija klienta noslēpums** – šis lauks ir pieejams tikai tad, ja opcija **Izmantot klienta noslēpumu** ir iestatīta uz _Jā_. Ievadiet klienta noslēpumu, kuru pierakstījāt, iestatot Azure AD, sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Active direktorija sertifikāta nospiedums** – šis lauks ir pieejams Windows ierīcēs tikai tad, ja opcija **Izmantot klienta noslēpumu** ir iestatīta uz _Nē_. Ievadiet sertifikāta nospiedumu, kuru pierakstījāt, iestatot Azure AD, sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Active direktorija resurss** – norādiet Supply Chain Management saknes vietrādi URL.

        > [!NOTE]
        > Nebeigt šo vērtību ar slīpsvītru (/).

    - **Aktīvs direktorija nomnieks** – ievadiet Azure AD nomnieku, kuru izmantojat ar Supply Chain Management serveri. Šīs vērtības forma ir `https://login.windows.net/<your-Azure-AD-domain-name>`. Tālāk minēts piemērs: `https://login.windows.net/contosooperations.onmicrosoft.com`. Papildinformāciju par to, kā atrast Azure AD domēna nosaukumu, skatiet sadaļā [Svarīgu lietotāja ID atrašana](/partner-center/find-ids-and-domain-names).

        > [!NOTE]
        > Nebeigt šo vērtību ar slīpsvītru (/).

    - **Uzņēmums** – ievadiet to juridisko personu programmatūrā Supply Chain Management, ar kuru lietojumprogrammai ir jāizveido savienojums.

1. Lapas augšējā labajā stūrī atlasiet pogu **Saglabāt**.
1. Ja izmantojat Android ierīci un autentifikācijai izmantojat sertifikātu, ierīce piedāvā izvēlēties sertifikātu.
1. Programma izveido savienojumu ar jūsu Supply Chain Management serveri un parāda pierakstīšanās lapu.

## <a name="remove-access-for-a-device"></a>Ierīces piekļuves liegšana

Gadījumā, ja ierīce ir nozaudēta vai apdraudēta, ir jāliedz šīs ierīces piekļuve programmatūrai Supply Chain Management. Tālāk ir aprakstītas ieteicamā piekļuves liegšanas procesa darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Azure Active Directory lietojumprogrammas**.
1. Dzēsiet rindu, kas atbilst ierīcei, kuras piekļuvi vēlaties liegt. Pierakstiet noņemtajai ierīcei izmantoto klienta ID, jo vēlāk tas būs nepieciešams.

    Ja esat reģistrējis tikai vienu klienta ID un vairākas ierīces izmanto to pašu klienta ID, jums šīm ierīcēm ir jāiedala jauni savienojuma iestatījumi. Pretējā gadījumā tās zaudēs piekļuvi.

1. Pierakstieties Azure portālā vietnē [https://portal.azure.com](https://portal.azure.com/).
1. Kreisās puses navigācijas rūtī atlasiet **Active Directory** un pārliecinieties, vai atrodaties pareizajā direktorijā.
1. Sarakstā **Pārvaldīt** atlasiet **Programmu reģistrācijas** un pēc tam atlasiet konfigurējamo lietojumprogrammu. Lapā **Iestatījumi** tiek parādīta konfigurācijas informācija.
1. Pārliecinieties, vai lietojumprogrammas klienta ID atbilst klienta ID, kuru pierakstījāt 2. darbībā.
1. Rīkjoslā atlasiet **Dzēst**.
1. Parādītajā apstiprinājuma ziņojumā atlasiet **Jā**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
