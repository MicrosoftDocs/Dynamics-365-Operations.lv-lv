---
title: Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem
description: Šajā tēmā aprakstīts, kā veidot pielāgotas lapas risinājumā Microsoft Dynamics 365 Commerce, kuras apstrādā pielāgotu pieteikšanos Azure Active Directory (Azure AD) lietotājiem un no biznesa uz patērētāju (B2C) vērstiem nomniekiem.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d4a1c2f45d77c3ff9a7bb4dffaf12d877dc04e69
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936784"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā veidot pielāgotas lapas risinājumā Microsoft Dynamics 365 Commerce, kuras apstrādā pielāgotu pieteikšanos Azure Active Directory (Azure AD) lietotājiem un no biznesa uz patērētāju (B2C) vērstiem nomniekiem.

Lai izmantotu pielāgotās lapas, kas ir autorizētas Dynamics 365 Commerce, lai apstrādātu lietotāja pierakstīšanās plūsmas, ir jāiestata Azure AD politikas, kas tiks raksturotas Commerce vidē. Varat konfigurēt Azure AD B2C politikas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana", izmantojot Azure AD B2C programmu. Tādējādi Azure AD B2C nomnieka un politiku nosaukumi var tikt raksturoti nodrošināšanas procesa laikā, kas tiek veikts Commerce videi, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

Pielāgotās Commerce lapas var veidot, izmantojot pierakstīšanos, parakstīšanos, konta profila rediģēšanu, paroles atiestatīšanu vai vispārīgu AAD moduli. Šīm pielāgotajām lapām publicētie lapu URL jāraksturo Azure AD B2C politikas konfigurācijās Azure portālā.

> [!WARNING] 
> Azure AD B2C atiestata veco (mantojuma) lietotāju plūsmas uz 2021. gada 1. augustu. Tādēļ jums jāplāno migrēt savas lietotāja plūsmas uz jauno ieteicamo versiju. Jaunā versija nodrošina līdzekļu pārību un jaunas funkcijas. Papildinformāciju skatiet sadaļā [Lietotāju darbplūsmas Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).

>Ar ieteiktajām B2C lietotāju plūsmām ir jāizmanto Commerce versijas 10.0.15 vai jaunāka moduļa bibliotēka. Var izmantot arī noklusējuma lietotāja politikas lapas, kas tiek piedāvātas Azure AD B2C, un atļaut pievienot fona attēlu, logotipu un fona krāsu izmaiņas, kas saistītas ar uzņēmuma zīmolu. Kaut arī vairāk izstrādes spēju ir ierobežotas, noklusējuma lietotāju politikas lapas nodrošina Azure AD B2C politikas funkcionalitāti, neizveidojot un nekonfigurējot atvēlētās pielāgotās lapas. 

## <a name="set-up-b2c-policies"></a>B2C politiku iestatīšana

Pēc tam, kad esat iestatījis savu Azure AD B2C nomnieku un saistījis to ar savu Commerce vidi, dodieties uz **Azure AD B2C** lapu Azure portālā un izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.

![Lietotāja plūsmas (politikas) komanda izvēlnē](./media/B2C_CustomPage_PoliciesMenu.png)

Tagad varat konfigurēt lietotāja pierakstīšanās plūsmas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana".

### <a name="configure-the-sign-up-and-sign-in-policy"></a>"Parakstīšanās un pierakstīšanās" politikas konfigurēšana

Lai konfigurētu "Parakstīšanās un pierakstīšanās" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma**, atlasiet **Pierakstīties un reģistrēties**, un pēc tam cilnē **Ieteiktais** atlasiet **Izveidot**.
1. Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_SignInSignUp**).
1. Sadaļā **Identitātes nodrošinātāji** atlasiet identitātes nodrošinātājus, ko izmantot šai politikai. Jāatlasa vismaz **Parakstīšanās e-pastā**.
1. Kolonnā **Ievākt atribūtu** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds** un **Uzvārds**.
1. Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Identitātes nodrošinātājs**, **Uzvārds** un **Lietotāja objekta ID**.

    ![Atlasītie atribūti un prasības](./media/B2C_SignInSignUp_Attributes.png)

1. Atlasiet **Labi**, lai izveidotu politiku.
1. Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.
1. Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.

    ![Jaunās politikas rekvizītu lapa](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Politikas nosaukums būs pilnībā raksturots Commerce vidē. (Prefikss **B2C\_1\_** tiks iekļauts raksturojumā.) Politikas nevar pārdēvēt pēc tam, kad tās izveidotas. Ja aizstājat esošu politiku savai Commerce videi, varat izdzēst sākotnējo politiku un izveidot jaunu politiku ar tādu pašu nosaukumu. Vai arī, ja vide jau ir nodrošināta, varat iesniegt jauno politikas nosaukumu, izmantojot pakalpojuma pieprasījumu.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

### <a name="configure-the-profile-editing-policy"></a>"Profila rediģēšanas" politikas konfigurēšana

Lai konfigurētu "Profila rediģēšanas" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma**, atlasiet **Profila rediģēšana**, un pēc tam cilnē **Ieteiktais** atlasiet **Izveidot**.
1. Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_EditProfile**).
1. Sadaļā **Identitātes nodrošinātāji** atlasiet identitātes nodrošinātājus, ko izmantot šai politikai. Jāatlasa vismaz **Pierakstīšanās lokālajā kontā**.
1. Kolonnā **Ievākt atribūtu** atlasiet izvēles lodziņus **Vārds** un **Uzvārds**.
1. Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Identitātes nodrošinātājs**, **Uzvārds** un **Lietotāja objekta ID**.
1. Atlasiet **Labi**, lai izveidotu politiku.
1. Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.
1. Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

### <a name="configure-the-password-reset-policy"></a>"Paroles atiestatīšanas" politikas konfigurēšana

Lai konfigurētu "Paroles atiestatīšanas" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma**, pēc tam atlasiet **Paroles atiestatīšanas** opciju un izvēlieties cilni **Ieteicamais** un noklikšķiniet uz **Izveidot**.
1. Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_ForgetPassword**).
1. Sadaļā **identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.
1. Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Uzvārds** un **Lietotāja objekta ID**.
1. Atlasiet **Labi**, lai izveidotu politiku.
1. Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.
1. Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

## <a name="build-the-custom-pages"></a>Pielāgoto lapu izveide

Atvēlētie Azure AD moduļi ir ietverti Commerce, lai izveidotu pielāgotas Azure AD lapas B2C lietotāju politikām. Lapas var veidot īpaši katras lietotāja politikas lapas izkārtojumam, izmantojot galvenos Azure AD B2C moduļus, kas detalizēti tālāk. Pēc izvēles **AAD vispārējo** moduli var izmantot visiem lapu izkārtojumiem un politikām Azure AD B2C (pat lapu izkārtojuma opcijām politikās, kas nav uzskaitītas tālāk). 

- Lapai raksturīgie Azure AD moduļi ir piesaistīti datu ievades vienumiem, ko atveido Azure AD B2C. Šie moduļi sniedz lielāku kontroli pār elementu novietošanu jūsu lapās. Tomēr, iespējams, ir jāveido vairāk lapu un moduļu paplašinājumu, lai noteiktu novirzes, kas pārsniedz tālāk aprakstītos noklusējuma iestatījumus.
- **AAD vispārējais** modulis izveido elementu "div" Azure AD B2C, lai atveidotu visus elementus lietotāja politikas lapas izkārtojumā, sniedzot lielāku elastīgumu lapas B2C funkcijām, bet mazāku pozicionēšanas un noslīdēšanas kontroli (lai gan CSS var izmantot, lai saskaņotu lapas izskatu un darbību).

Varat izveidot vienu lapu ar **AAD vispārējo** moduli un izmantot to visām lietotāja politikas lapām vai arī izveidot noteiktas lapas, izmantojot atsevišķus Azure AD moduļus pierakstīšanās, reģistrēšanās, profila rediģēšanai, paroles atiestatīšanai un paroles atiestatīšanas pārbaudei. Varat izmantot arī abus komplekta izkārtojumus, izmantojot konkrētas Azure AD lapas norādītajiem lapu izkārtojumiem un vispārējo AAD moduļa lapu atlikušajiem lapu izkārtojumiem šajās vai citās lietotāju politikas lapās.

Lai uzzinātu vairāk par Azure AD moduļiem, kas tiek piegādāti ar moduļu bibliotēku, lasiet vairāk [Identitātes pārvaldības lapās un moduļos](identity-mgmt-modules.md).

Lai izveidotu pielāgotās lapas ar konkrētiem identitātes moduļiem lietotāja pierakstīšanās gadījumu apstrādāšanai, veiciet tālāk minētās darbības.

1. Dodieties uz savu vietni Commerce vietņu veidotājā.
1. Izveidojiet šādas piecas veidnes un lapas (ja nav jau jūsu vietnē):
    - Veidne **Pierakstīšanās** un lapa, kas izmanto pierakstīšanās moduli.
    - Veidne **Parakstīšanās** un lapa, kas izmanto parakstīšanās moduli.
    - Veidne **Paroles atiestatīšana** un lapa, kas izmanto paroles atiestatīšanas moduli.
    - Veidne **Paroles atiestatīšanas verifikācija** un lapa, kas izmanto paroles atiestatīšanas verifikācijas moduli.
    - Veidne **Profila rediģēšana** un lapa, kas izmanto konta profila rediģēšanas moduli.

Izveidojot lapas, sekojiet tālāk minētajiem norādījumiem.

- Katrai lapai vai modulim izmantojiet izkārtojumu un stilu, kas vislabāk atbilst jūsu biznesa vajadzībām.
- Publicējiet visas lapas un URL, kas jāizmanto Azure AD B2C iestatījumā.
- Pēc lapu un URL publicēšanas ievāciet URL, kas jāizmanto Azure AD B2C politikas konfigurācijām. Katram URL, kad tas tiek izmantots, tiks pievienots piedēklis **?preloadscripts=true**.

> [!IMPORTANT]
> Lapas, uz ko izveidotas atsauces Azure AD B2C, ir pieejamas tieši no Azure AD B2C nomnieka domēna. Neizmantojiet atkārtoti tādas universālas galvenes un kājenes, kurām ir relatīvas saites. Tā kā šīs lapas izmantošanas laikā tiks viesotas Azure AD B2C domēnā, visām saitēm jāizmanto tikai absolūtie URL. Ir ieteicams izveidot noteiktu virsrakstu un kājeni ar absolūtiem vietrāžiem URL savām pielāgotajām Azure AD lapām, izmantojot jebkurus noņemtos Commerce raksturīgos moduļus, kuriem nepieciešams savienojums ar Retail Server. Piemēram, izlases, meklēšanas joslas, pierakstīšanās saites un groza moduļus nedrīkst ietvert ne uz vienu lapu, kas tiks izmantota Azure AD B2C lietotāju plūsmās.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C politiku konfigurēšana ar pielāgotu lapas informāciju 

Azure portālā atgriezieties lapā **Azure AD B2C** un pēc tam izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>"Pierakstīšanās un parakstīšanās" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Pierakstīšanās un parakstīšanās" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Pierakstīšanās un parakstīšanās** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet izkārtojumu **Vienotā pierakstīšanās un parakstīšanās lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija** atlasiet versiju **2.1.0** vai jaunāku (nepieciešama moduļu bibliotēka Commerce versijai 10.0.15 vai jaunākai versijai).
1. Atlasiet **Saglabāt**.
1. Atlasiet izkārtojumu **Lokālā konta parakstīšanās lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija** atlasiet versiju **2.1.0** vai jaunāku (nepieciešama moduļu bibliotēka Commerce versijai 10.0.15 vai jaunākai versijai).
1. Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.
    1. Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** kolonnā **Nepieciešama verifikācija**.
    1. **E-pasta adreses** atribūtam ir ieteicams atstāt kolonnā **Nepieciešama verifikācija** atlasīto noklusējuma vērtību uz **Jā**. Šī opcija nodrošina, lai lietotāji, kuri pierakstās ar norādīto e-pasta adresi, apstiprinātu, ka viņiem pieder e-pasta adrese.
    1. Atribūtiem **E-pasta adrese**, **Vārds** un **Uzvārds** atlasiet **Nē** kolonnā **Pēc izvēles**.
1. Atlasiet **Saglabāt**.

    ![Lokālā konta parakstīšanās lapas politikas konfigurēšana](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>"Profila rediģēšanas" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Profila rediģēšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Profila rediģēšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet **Profila rediģēšanas lapas** izkārtojumu (var būt nepieciešams ritināt līdzās citām izkārtojuma opcijām atkarībā no ekrāna).
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu profila rediģēšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija** atlasiet versiju **2.1.0** vai jaunāku (nepieciešama moduļu bibliotēka Commerce versijai 10.0.15 vai jaunākai versijai).
1. Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.
    1. Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** kolonnā **Pēc izvēles**.
    1. Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** kolonnā **Nepieciešama verifikācija**.
1. Atlasiet **Saglabāt**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>"Paroles atiestatīšanas" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Paroles atiestatīšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Paroles atiestatīšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet izkārtojumu **Lapa Aizmirsu paroli**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu paroles atiestatīšanas verificēšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija** atlasiet versiju **2.1.0** vai jaunāku (nepieciešama moduļu bibliotēka Commerce versijai 10.0.15 vai jaunākai versijai).
2. Atlasiet **Saglabāt**.
3. Atlasiet izkārtojumu **Lapa Nomainīt paroli**.
4. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
5. Laukā **Pielāgots lapas URI** ievadiet pilnu paroles atiestatīšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Laukā **Lapas izkārtojuma versija** atlasiet versiju **2.1.0** vai jaunāku (nepieciešama moduļu bibliotēka Commerce versijai 10.0.15 vai jaunākai versijai).
7. Atlasiet **Saglabāt**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etiķetēm un aprakstiem paredzētu noklusējuma teksta virkņu pielāgošana

Moduļa bibliotēkā pierakstīšanās moduļi ir iepriekš aizpildīti ar etiķetēm un aprakstiem paredzētām noklusējuma teksta virknēm. Virknes var pielāgot tā moduļa rekvizītu rūtī, pie kura strādājat. Papildu virknēm lapā (piemēram, **Aizmirsta parole?** saites tekstu vai **Izveidot konta izsaukumu** darbības tekstam) būs nepieciešams izmantot Commerce programmatūras izstrādes komplektu (SDK) un atjaunināt vērtības global.json failā pierakstīšanās modulim.

Piemēram, aizmirstās paroles saites noklusējuma teksts ir **Aizmirsta parole?**. Tālāk parādīts šis noklusējuma teksts pierakstīšanās lapā.

![Noklusējuma teksts aizmirstas paroles saitei pierakstīšanās lapā](./media/B2C_SignUp_ModuleFace.png)

Tomēr moduļa bibliotēkas pierakstīšanās moduļa global.json failā varat rediģēt tekstu, lai būtu **Aizmirsāt paroli?**, kā parādīts tālāk redzamajā ilustrācijā.

![Atjauninātais saites teksts pierakstīšanās moduļa global.json failā](./media/B2C_CustomizingStringsForModule.png)

Pēc global.json faila atjaunināšanas un savu izmaiņu publicēšanas jaunais saites teksts parādīsies pierakstīšanās modulī gan Commerce, gan arī aktuālajā pierakstīšanās lapā.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]