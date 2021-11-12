---
title: Instalējiet un savienojiet lietotni Warehouse Management mobile
description: Šajā tēmā ir paskaidrots, kā instalēt lietotni Warehosue Management mobile katrā jūsu mobilajā ierīcē un konfigurēt to, lai izveidotu savienojumu ar Microsoft Dynamics 365 Supply Chain Management vidi.
author: MarkusFogelberg
ms.date: 02/03/2021
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
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3a0a8555ac7c523af03401ab84af30f577777995
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647624"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Instalējiet un savienojiet lietotni Warehouse Management mobile

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šajā tēmā aprakstīts, kā konfigurēt jauno lietotni Warehouse Management mobile. Ja vēlaties meklēt informāciju par vecās Warehouse programmas konfigurēšanu (jau novecojusi), skatiet sadaļu [Warehouse lietotnes instalēšana un savienošana](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Šajā tēmā ir paskaidrots, kā instalēt lietotni Warehouse Management mobile katrā jūsu mobilajā ierīcē un konfigurēt to, lai izveidotu savienojumu ar Supply Chain Management vidi. Varat katru ierīci konfigurēt manuāli vai importēt savienojuma iestatījumus, izmantojot failu vai skenējot QR kodu.

## <a name="system-requirements"></a>Sistēmas prasības

Lietotne Warehouse Management mobile ir pieejama Windows un Google Android operētājsistēmām. Lai varētu lietot šo programmu, mobilajā ierīcē ir jābūt instalētai kādai no tālāk norādītajām atbalstītajām operētājsistēmām:

- Windows 10 (universālā Windows platforma \[UWP\]) 2018. gada oktobra veidotāju atjauninājums 1809 (būvējums 10.0.17763) vai jaunāka versija
- Android 4.4 vai jaunāka versija

## <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Pirms izmantojat lietotni, jūsu sistēmā jābūt iespējotai saistītai funkcijai. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Lietotāja iestatījumi, ikonas un darbību nosaukumi jaunajai noliktavas programmai*

## <a name="get-the-warehouse-management-mobile-app"></a>Iegūt lietotni Warehouse Management mobile

Mazākiem izvietojumiem, iespējams, vēlēsities instalēt programmu no katras ierīces attiecīgā veikala un pēc tam manuāli konfigurēt savienojumu ar jūsu izmantotajām vidēm.

Lielākām izvietošanām jūs varat automatizēt programmu izvietošanu un/vai konfigurāciju, kas var būt ērtāk, ja pārvaldāt daudzas ierīces. Piemēram, varat izmantot mobilās ierīces pārvaldības un mobilās lietojumprogrammas pārvaldības risinājumu, piemēram, [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Papildinformāciju par Intune izmantošanu, lai pievienotu lietojumprogrammas, skatiet [Programmu pievienošana Microsoft Intune](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Programmas instalēšana no programmu veikala

Vienkāršākais veids, kā instalēt programmu vienā ierīcē, ir instalēt to no programmu veikala, kas vienmēr nodrošina visjaunāko vispārīgi pieejamo versiju. Programmā Microsoft Intune var arī saņemt programmas no programmu veikaliem. Izmantojiet vienu no šīm saitēm, lai instalētu programmu no programmu veikala:

- **Windows (UWP):** [Warehouse Management Microsoft Store veikalā](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Warehouse Management Google Play veikalā](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Lejupielādēt programmu no programmas Microsoft App Center

Tā vietā, lai lejupielādētu programmu no Microsoft App Center, varat izvēlēties alternatīvu programmas instalēšanai no programmu veikala. Programmu centrs nodrošina instalējamas pakotnes, ko var līdzielādēt. Papildus pašreizējai versijai, programmu centrs ļauj arī lejupielādēt iepriekšējās versijas un sniegt priekšskatījuma versijas ar gaidāmajām funkcijām, kuras varat izmēģināt. Lai lejupielādētu noliktavas pārvaldības mobilās programmas pašreizējās, iepriekšējās vai priekšskatījuma versijas no programmas Microsoft App Center, izmantojiet vienu no šīm saitēm:

- **Windows (UWP):** [Noliktavu pārvaldība (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Norādījumus par lejupielādētas pakotnes instalēšanu Windows ierīcē un nepieciešamo sertifikātu iestatīšanai skatiet sadaļā [Būvējuma instalēšana no App Center](/appcenter/distribution/installation).

- **Android:** [Noliktavu pārvaldība (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Lejupielādējot priekšskatījuma versiju, tās instalēšanai ir jāveic daži papildu soļi. Papildinformāciju skatiet [Testēt Android Programmas](/appcenter/distribution/testers/testing-android).

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

    - **Augšupielādēt sertifikātu** – augšupielādēt sertifikātu, ko izmantot kā noslēpumu. Ir ieteicams izmanto šo pieeju, jo tā ir drošāka un to var arī pilnīgāk automatizēt. Ja izmantojat lietotni Warehouse Management mobile Windows ierīcēs, pierakstiet **Nospiedums** vērtību, kas tiek parādīta pēc sertifikāta augšupielādes. Šī vērtība būs nepieciešama, konfigurējot sertifikātu Windows ierīcēs.
    - **Jauns klienta noslēpums** – izveidojiet atslēgu, ievadot atslēgas aprakstu un ilgumu sadaļā **Paroles**, un pēc tam atlasiet **Pievienot**. Izveidojiet atslēgas kopiju un glabājiet to drošībā.

    ![Sertifikāts & noslēpumi.](media/app-connect-azure-authentication.png "Sertifikāts & noslēpumi")

Papildinformāciju par to, kā iestatīt tīmekļa pakalpojuma lietojumprogrammas Azure AD, skatiet tālāk norādītos resursus:

- Instrukcijas, kurās parādīts, kā izmantot Windows PowerShell, lai Azure AD iestatītu tīmekļa pakalpojumu lietojumprogrammas, skatiet [Kā: izmantot Azure PowerShell, lai izveidotu pakalpojuma vadītāju ar sertifikātu](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Pilnīgu informāciju par to, kā manuāli izveidot tīmekļa pakalpojumu lietojumprogrammu programmā Azure AD, skatiet tālāk norādītās tēmas:

    - [Īsa pamācība: lietojumprogrammas reģistrācija platformā Microsoft Identity](/azure/active-directory/develop/quickstart-register-app)
    - [Kā: izmantot portālu, lai izveidotu Azure AD lietojumprogrammu un pakalpojuma vadītāju, kas var piekļūt resursiem](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Izveidot un konfigurēt lietotāja kontu programmatūrā Supply Chain Management

Lai jūsu Azure AD lietojumprogrammu varētu izmantot Supply Chain Management, rīkojieties šādi.

1. Izveidojiet lietotāju, kas atbilst lietotnes Warehouse Management mobile lietotāja akreditācijas datiem:

    1. Programmatūrā Supply Chain Management dodieties uz sadaļu **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
    1. Izveidojiet lietotāju.
    1. Piešķiriet *Noliktavas mobilās ierīces lietotāja* lomu lietotājam.

    ![Piešķiriet noliktavas mobilās ierīces lietotāju.](media/app-connect-app-users.png "Piešķiriet noliktavas mobilās ierīces lietotāju")

1. Saistiet savu Azure AD lietojumprogrammu ar lietotnes Warehouse Management mobile lietotāju:

    1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Azure Active Directory lietojumprogrammas**.
    1. Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.
    1. Laukā **Klienta ID** ievadiet klienta ID, kuru atzīmējāt iepriekšējā sadaļā.
    1. Laukā **Nosaukums** ievadiet nosaukumu.
    1. Laukā **Lietotāja ID** atlasiet lietotāja ID, ko tikko izveidojāt.

    ![Azure Active Directory lietojumprogrammas.](media/app-connect-aad-apps.png "Azure Active Directory pieteikumi")

> [!TIP]
> Viens no šo iestatījumu izmantošanas veidiem ir izveidot klienta ID Azure katrai fiziskajai ierīcei un pēc tam pievienot katru klienta ID **Azure Active Directory lietojumprogrammu** lapai. Ja ierīce ir nozaudēta, to var viegli noņemt Supply Chain Management, noņemot no lapas klienta ID. (Šī pieeja darbojas, jo savienojuma akreditācijas dati, kas tiek saglabāti katrā ierīcē, norāda arī klienta ID, kā aprakstīts tālāk šajā tēmā.)
>
> Turklāt noklusējuma valodu, numuru formātu un laika joslas iestatījumus katram klienta ID nosaka preferences, kas tiek iestatītas **Lietotāja ID** vērtībai, kas šeit tiek kartēta. Tāpēc jūs varētu izmantot šīs preferences, lai izveidotu noklusējuma iestatījumus katrai ierīcei vai ierīču kolekcijai, balstoties uz klienta ID. Tomēr šie noklusējuma iestatījumi tiks ignorēti, ja tie ir definēti arī *noliktavas programmas lietotāja kontam*, ko darbinieks izmantos, lai pieteiktos ierīcē. (Lai iegūtu papildinformāciju, skatiet sadaļu [Mobilo ierīču lietotāju konti](mobile-device-work-users.md).)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentificēt, izmantojot sertifikātu vai klienta noslēpumu

Autentifikācija ar Azure AD nodrošina drošu veidu, kā pievienot mobilo ierīci Supply Chain Management. Autentifikāciju var veikt, izmantojot klienta noslēpumu vai sertifikātu. Ja importēsit savienojuma iestatījumus, ieteicams izmantot sertifikātu nevis klienta noslēpumu. Tā kā klienta noslēpums vienmēr ir jāglabā drošībā, to nevar importēt no savienojuma iestatījumu faila vai QR koda, kā aprakstīts tālāk šajā tēmā.

Sertifikātus var izmantot kā noslēpumus, lai pierādītu lietojumprogrammas identitāti, kad tiek pieprasīta pilnvara. Sertifikāta publiskā daļa tiek augšupielādēta programmu reģistrācijā Azure portālā, savukārt pilnais sertifikāts ir jāizvieto katrā ierīcē, kurā ir lietotne Warehouse Management mobile. Jūsu organizācija ir atbildīga par sertifikāta pārvaldību attiecībā uz rotāciju un tā tālāk. Varat izmantot pašparakstītus sertifikātus, bet vienmēr izmantojiet neeksportējamus sertifikātus.

Sertifikātam ir jābūt lokāli pieejamam katrā ierīcē, kurā tiek palaista lietotne Warehouse Management mobile. Papildinformāciju par to, kā pārvaldīt Intune kontrolēto ierīču sertifikātus, ja lietojat Intune, skatiet sadaļā [Sertifikātu izmantošana autentifikācijai programmā Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurējiet lietojumprogrammu, importējot savienojuma iestatījumus

Lai atvieglotu lietojumprogrammas uzturēšanu un izvietošanu daudzās mobilajās ierīcēs, savienojuma iestatījumus var importēt tā vietā, lai tos manuāli ievadītu katrā ierīcē. Šajā sadaļā ir paskaidrots, kā izveidot un importēt iestatījumus.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Savienojuma iestatījumu faila vai QR koda izveidošana

Varat importēt savienojuma iestatījumus no faila vai QR koda. Abām pieejām vispirms ir jāizveido iestatījumu fails, kas izmanto JavaScript Object Notation (JSON) formātu un sintaksi. Failā jābūt ietvertam savienojumu sarakstam, kas satur atsevišķus pievienojamos savienojumus. Tālāk esošajā tabulā apkopoti parametri, kas ir jānorāda savienojuma iestatījumu failā.

| Parametrs | apraksts |
|---|---|
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

Parasti tiek izmantots ierīču pārvaldības rīks vai skripts, lai sadalītu savienojuma iestatījumu failus katrai ierīcei, ko pārvaldāt. Ja, saglabājot savienojuma iestatījumu failu katrā ierīcē, izmantojat noklusējuma nosaukumu un atrašanās vietu, lietotne Warehouse Management mobile to automātiski importēs pat pirmajā palaišanas reizē pēc programmas instalēšanas. Ja failam izmantojat pielāgotu nosaukumu vai atrašanās vietu, programmas lietotājam pirmās palaišanas reizē ir jānorāda vērtības. Tomēr pēc tam programma turpinās izmantot norādīto nosaukumu un atrašanās vietu.

Katru reizi, kad programma tiek startēta, tā atkārtoti importē savienojuma iestatījumus no iepriekšējās atrašanās vietas, lai noteiktu, vai ir veiktas kādas izmaiņas. Programma atjauninās tikai tos savienojumus, kam ir tādi paši nosaukumi kā savienojumiem savienojuma iestatījumu failā. Lietotāja izveidotie savienojumi, kas izmanto citus nosaukumus, netiks atjaunināti.

Savienojumu nevar noņemt, izmantojot savienojuma iestatījumu failu.

Kā jau minēts, noklusējuma faila nosaukums ir *connections.json*. Noklusējuma faila atrašanās vieta ir atkarīga no tā, vai izmantojat Windows ierīci vai Android ierīci:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Parasti ceļi tiek izveidoti automātiski pēc programmas pirmās palaišanas reizes. Tomēr tos var izveidot manuāli, ja savienojuma iestatījumu fails pirms instalēšanas ir jāpārsūta uz ierīci.

> [!NOTE]
> Ja programma ir atinstalēta, noklusējuma ceļš un tā saturs tiek noņemts.

### <a name="import-the-connection-settings"></a>Savienojuma iestatījumu importēšana

Lai importētu savienojuma iestatījumus no faila vai QR koda, rīkojieties šādi.

1. Startējiet lietotni Warehouse Management mobile savā mobilajā ierīcē. Pirmo reizi startējot programmu, tiek rādīts sveiciena ziņojums. Atlasiet **Atlasīt savienojumu**.

    ![Sveiciena ziņojums.](media/app-configure-welcome-screen.png "Sveiciena ziņojums")

1. Ja importējat savienojuma iestatījumus no faila, iespējams, programma jau ir atradusi failu, ja pēc saglabāšanas tika izmantots noklusējuma nosaukums un noklusējuma atrašanās vieta. Šajā gadījumā pārejiet uz 4. soli. Pretējā gadījumā atlasiet **Iestatīt savienojumu** un turpiniet ar 3. soli.

    ![Iestatīt savienojumu.](media/app-configure-set-up-connection.png "Iestatīt savienojumu")

1. Dialoglodziņā **Savienojuma iestatīšana** atlasiet **Pievienot no faila** vai **Pievienot no QR koda** atkarībā no tā, kā vēlaties importēt iestatījumus:

    - Ja importējat savienojuma iestatījumus no faila, atlasiet **Pievienot no faila**, pārlūkojiet failu lokālajā ierīcē un atlasiet to. Ja atlasīsit pielāgotu atrašanās vietu, programma to saglabās un automātiski izmantos nākamreiz.
    - Ja importējat savienojuma iestatījumus, skenējot QR kodu, atlasiet **Pievienot no QR kodu**. Programma pieprasa atļauju izmantot ierīces kameru. Pēc atļaujas piešķiršanas, kamera tiek startēta, lai to izmantotu skenēšanai. Atkarībā no ierīces kameras kvalitātes un QR koda sarežģītības, var izrādīties grūti iegūt pareizu skenējumu. Šādā gadījumā mēģiniet samazināt QR koda sarežģītību, ģenerējot tikai vienu savienojumu katram QR kodam. (Pašlaik QR koda skenēšanai var izmantot tikai ierīces kameru.)

    ![Savienojuma iestatīšanas izvēlne.](media/app-configure-connection-setup-flyout.png "Savienojuma iestatīšanas izvēlne")

1. Kad savienojuma iestatījumi ir veiksmīgi ielādēti, tiek parādīts atlasītais savienojums.

    ![Savienojuma iestatījumu ielādēšana.](media/app-configure-select-connection.png "Savienojuma iestatījumu ielādēšana")

1. Ja izmantojat Android ierīci un autentifikācijai izmantojat sertifikātu, ierīce piedāvā izvēlēties sertifikātu.

    ![Izvēlēties Android ierīcē piedāvāto sertifikātu.](media/app-configure-select-certificate.png "Izvēlēties Android ierīcē piedāvāto sertifikātu")

1. Programma izveido savienojumu ar jūsu Supply Chain Management serveri un parāda pierakstīšanās lapu.

    ![Pierakstīšanās lapa.](media/app-configure-sign-in-page.png "Pierakstīšanās lapa")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Lietojumprogrammas manuāla konfigurēšana

Ierīcē instalēto programmu var manuāli konfigurēt, lai izveidotu savienojumu ar Supply Chain Management serveri, izmantojot Azure AD lietojumprogrammu.

1. Startējiet lietotni Warehouse Management mobile savā mobilajā ierīcē.
1. Ja programma tiek startēta **Parauga režīmā**, atlasiet **Savienojuma iestatījumus**. Ja, palaižot programmu, parādās lapa **Pierakstīties**, atlasiet **Mainīt savienojumu**.
1. Atlasiet **Jauna savienojuma iestatīšana**.

    ![Iestatīt savienojumu.](media/app-configure-set-up-connection.png "Iestatīt savienojumu")

1. Atlasiet **Ievadīt manuāli**.

    ![Savienojuma iestatīšanas izvēlne.](media/app-configure-connection-setup-flyout.png "Savienojuma iestatīšanas izvēlne")

    Parādās lapa **Jauns savienojums** un ataino iestatījumus, kas nepieciešami savienojuma datu manuālai ievadīšanai.

    ![Manuālā savienojuma lauki.](media/app-configure-input-manually.png "Manuālā savienojuma lauki")

1. Ievadiet sekojošo informāciju:

    - **Izmantot klienta noslēpumu** – iestatiet šo opciju uz _Jā_, lai izmantotu klienta noslēpumu autentificējoties Supply Chain Management. Iestatiet to uz _Nē_, lai autentifikācijai izmantotu sertifikātu. (Plašāku informāciju skatiet [Izveidojiet Web pakalpojumu programmu Azure Active Directory](#create-service) iepriekš šīs tēmas sadaļā.)
    - **Savienojuma nosaukums** — ievadiet jaunā savienojuma nosaukumu. Šis nosaukums tiks parādīts laukā **Atlasīt savienojumu** nākamajā reizē, kad atvērsit savienojuma iestatījumus. Jūsu ievadītajam nosaukumam jābūt unikālam. (Citiem vārdiem sakot, tam ir jābūt atšķirīgam no visiem pārējiem ierīcē saglabātajiem savienojumu nosaukumiem, ja tajā tiek saglabāti citi savienojumu nosaukumi.)
    - **Active direktorija klienta ID** – ievadiet klienta ID, kuru pierakstījāt, iestatot Azure AD sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Active direktorija klienta noslēpums** – šis lauks ir pieejams tikai tad, ja opcija **Izmantot klienta noslēpumu** ir iestatīta uz _Jā_. Ievadiet klienta noslēpumu, kuru pierakstījāt, iestatot Azure AD, sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Aktīvā direktorija sertifikāta nospiedums** – šis lauks ir pieejams tikai Windows ierīcēm un tikai tad, ja opcija **Izmantot klienta noslēpumu** ir iestatīta uz _Nē_. Ievadiet sertifikāta nospiedumu, kuru pierakstījāt, iestatot Azure AD, sadaļā [Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Azure Active Directory](#create-service).
    - **Active direktorija resurss** – norādiet Supply Chain Management saknes vietrādi URL.

        > [!IMPORTANT]
        > Nebeigt šo vērtību ar slīpsvītru (/).

    - **Aktīvs direktorija nomnieks** – ievadiet Azure AD nomnieku, kuru izmantojat ar Supply Chain Management serveri. Šīs vērtības forma ir `https://login.windows.net/<your-Azure-AD-domain-name>`. Tālāk minēts piemērs: `https://login.windows.net/contosooperations.onmicrosoft.com`. Papildinformāciju par to, kā atrast Azure AD domēna nosaukumu, skatiet sadaļā [Svarīgu lietotāja ID atrašana](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Nebeigt šo vērtību ar slīpsvītru (/).

    - **Uzņēmums** – ievadiet to juridisko personu programmatūrā Supply Chain Management, ar kuru lietojumprogrammai ir jāizveido savienojums.

1. Lapas augšējā labajā stūrī atlasiet pogu **Saglabāt**.
1. Ja izmantojat Android ierīci un autentifikācijai izmantojat sertifikātu, ierīce piedāvā izvēlēties sertifikātu.
1. Programma izveido savienojumu ar jūsu Supply Chain Management serveri un parāda pierakstīšanās lapu.

## <a name="remove-access-for-a-device"></a>Ierīces piekļuves liegšana

Ja ierīce ir nozaudēta vai apdraudēta, ir jāliedz šīs ierīces piekļuve programmatūrai Supply Chain Management. Tālāk ir aprakstītas ieteicamā piekļuves liegšanas procesa darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Azure Active Directory lietojumprogrammas**.
1. Dzēsiet rindu, kas atbilst ierīcei, kuras piekļuvi vēlaties liegt. Pierakstiet noņemtajai ierīcei izmantoto klienta ID, jo vēlāk tas būs nepieciešams.

    Ja esat reģistrējis tikai vienu klienta ID un vairākas ierīces izmanto to pašu klienta ID, jums šīm ierīcēm ir jāiedala jauni savienojuma iestatījumi. Pretējā gadījumā tās zaudēs piekļuvi.

1. Pierakstieties Azure portālā vietnē [https://portal.azure.com](https://portal.azure.com/).
1. Kreisās puses navigācijas rūtī atlasiet **Active Directory** un pārliecinieties, vai atrodaties pareizajā direktorijā.
1. Sarakstā **Pārvaldīt** atlasiet **Programmu reģistrācijas** un pēc tam atlasiet konfigurējamo lietojumprogrammu. Lapā **Iestatījumi** tiek parādīta konfigurācijas informācija.
1. Pārliecinieties, vai lietojumprogrammas klienta ID atbilst klienta ID, kuru pierakstījāt 2. darbībā.
1. Rīkjoslā atlasiet **Dzēst**.
1. Parādītajā apstiprinājuma ziņojumā atlasiet **Jā**.

## <a name="additional-resources"></a>Papildu resursi

- [Mobilās ierīces lietotāja iestatījumi](mobile-device-user-settings.md)
- [Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai](step-icons-titles.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
