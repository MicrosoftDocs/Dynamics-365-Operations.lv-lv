---
title: Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem
description: Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce izveidot pielāgotas lapas, kas apstrādā Azure Active Directory (Azure AD) bizness–patērētājs (B2C) nomnieku lietotāju pielāgotas pierakstīšanās gadījumus.
author: brianshook
manager: annbe
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fe2a716d370c350c0c7e034835ff755f1ec9c6a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001949"
---
# <a name="set-up-custom-pages-for-user-logins"></a>Pielāgotu lapu iestatīšana lietotāja pieteikšanās gadījumiem


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce izveidot pielāgotas lapas, kas apstrādā Azure Active Directory (Azure AD) bizness–patērētājs (B2C) nomnieku lietotāju pielāgotas pierakstīšanās gadījumus.

## <a name="overview"></a>Pārskats

Lai izmantotu pielāgotās lapas, kas ir autorizētas Dynamics 365 Commerce, lai apstrādātu lietotāja pierakstīšanās plūsmas, ir jāiestata Azure AD politikas, kas tiks raksturotas Commerce vidē. Varat konfigurēt Azure AD B2C politikas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana", izmantojot Azure AD B2C programmu. Tādējādi Azure AD B2C nomnieka un politiku nosaukumi var tikt raksturoti nodrošināšanas procesa laikā, kas tiek veikts Commerce videi, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

Pielāgotās Commerce lapas var veidot, izmantojot pierakstīšanos, parakstīšanos, konta profila rediģēšanu vai paroles atiestatīšanas moduli. Šīm pielāgotajām lapām publicētie lapu URL jāraksturo Azure AD B2C politikas konfigurācijās Azure portālā.

## <a name="set-up-b2c-policies"></a>B2C politiku iestatīšana

Pēc tam, kad esat iestatījis savu Azure AD B2C nomnieku un saistījis to ar savu Commerce vidi, dodieties uz **Azure AD B2C** lapu Azure portālā un izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.

![Lietotāja plūsmas (politikas) komanda izvēlnē](./media/B2C_CustomPage_PoliciesMenu.png)

Tagad varat konfigurēt lietotāja pierakstīšanās plūsmas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana".

### <a name="configure-the-sign-up-and-sign-in-policy"></a>"Parakstīšanās un pierakstīšanās" politikas konfigurēšana

Lai konfigurētu "Parakstīšanās un pierakstīšanās" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Ieteiktais** atlasiet politiku **Parakstīšanās un pierakstīšanās**.
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
> Politikas nosaukums būs pilnībā raksturots Commerce vidē. (**B2C\_1\_** prefikss tiks iekļauts raksturojumā.) Politikas nevar pārdēvēt pēc tam, kad tās izveidotas. Ja aizstājat esošu politiku savai Commerce videi, varat izdzēst sākotnējo politiku un izveidot jaunu politiku ar tādu pašu nosaukumu. Vai arī, ja vide jau ir nodrošināta, varat iesniegt jauno politikas nosaukumu, izmantojot pakalpojuma pieprasījumu.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

### <a name="configure-the-profile-editing-policy"></a>"Profila rediģēšanas" politikas konfigurēšana

Lai konfigurētu "Profila rediģēšanas" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Ieteiktais** atlasiet politiku **Profila rediģēšana**.
1. Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_EditProfile**).
1. Sadaļā **Identitātes nodrošinātāji** atlasiet identitātes nodrošinātājus, ko izmantot šai politikai. Jāatlasa vismaz **Pierakstīšanās lokālajā kontā**.
1. Kolonnā **Ievākt atribūtu** atlasiet izvēles lodziņus **E-pasta adreses** un **Uzvārds**.
1. Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Identitātes nodrošinātājs**, **Uzvārds** un **Lietotāja objekta ID**.
1. Atlasiet **Labi**, lai izveidotu politiku.
1. Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.
1. Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

### <a name="configure-the-password-reset-policy"></a>"Paroles atiestatīšanas" politikas konfigurēšana

Lai konfigurētu "Paroles atiestatīšanas" politiku, veiciet tālāk minētās darbības.

1. Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Priekšskatījums** atlasiet politiku **Paroles atiestatīšana v1.1**.

    ![Paroles atiestatīšana v1.1 politika atlasīta priekšskatījuma cilnē](./media/B2C_ForgetPassword_Menu.png)

1. Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_ForgetPassword**).
1. Sadaļā **identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.
1. Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Uzvārds** un **Lietotāja objekta ID**.

    ![Atlasītās prasības](./media/B2C_ForgetPassword_Attributes.png)

1. Atlasiet **Labi**, lai izveidotu politiku.
1. Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.
1. Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.

Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu. Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.

## <a name="build-the-custom-pages"></a>Pielāgoto lapu izveide

Lai izveidotu pielāgotās lapas lietotāja pierakstīšanās gadījumu apstrādāšanai, veiciet tālāk minētās darbības.

1. Commerce autorēšanas rīkos dodieties uz savu vietni.
1. Izveidošanai izmantojiet tālāk minētās piecas veidnes un piecas lapas.

    - Veidne **Pierakstīšanās** un lapa, kas izmanto pierakstīšanās moduli.
    - Veidne **Parakstīšanās** un lapa, kas izmanto parakstīšanās moduli.
    - Veidne **Paroles atiestatīšana** un lapa, kas izmanto paroles atiestatīšanas moduli.
    - Veidne **Paroles atiestatīšanas verifikācija** un lapa, kas izmanto paroles atiestatīšanas verifikācijas moduli.
    - Veidne **Profila rediģēšana** un lapa, kas izmanto konta profila rediģēšanas moduli

Izveidojot lapas, sekojiet tālāk minētajiem norādījumiem.

- Katrai lapai vai modulim izmantojiet izkārtojumu un stilu, kas vislabāk atbilst jūsu biznesa vajadzībām.
- Publicējiet visas lapas un URL, kas jāizmanto Azure AD B2C iestatījumā.
- Pēc lapu un URL publicēšanas ievāciet URL, kas jāizmanto Azure AD B2C politikas konfigurācijām. Katram URL, kad tas tiek izmantots, tiks pievienots piedēklis **?preloadscripts=true**.

> [!IMPORTANT]
> Neizmantojiet atkārtoti tādas universālas galvenes un kājenes, kurām ir relatīvas saites. Tā kā šīs lapas izmantošanas laikā tiks viesotas Azure AD B2C domēnā, visām saitēm jāizmanto tikai absolūtie URL.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C politiku konfigurēšana ar pielāgotu lapas informāciju 

Azure portālā atgriezieties lapā **Azure AD B2C** un pēc tam izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>"Pierakstīšanās un parakstīšanās" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Pierakstīšanās un parakstīšanās" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Pierakstīšanās un parakstīšanās** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet izkārtojumu **Vienotā pierakstīšanās un parakstīšanās lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.
1. Atlasiet izkārtojumu **Lokālā konta parakstīšanās lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.
1. Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.

    1. Atribūtiem **E-pasta adrese**, **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Nepieciešama verifikācija**.
    1. Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Pēc izvēles**.

    ![Lokālā konta parakstīšanās lapas politikas konfigurēšana](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>"Profila rediģēšanas" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Profila rediģēšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Profila rediģēšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet izkārtojumu **Profila rediģēšanas lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu profila rediģēšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.
1. Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.

    1. Atribūtiem **E-pasta adrese** un **Vārds** atlasiet **Nē** laukā **Nepieciešama verifikācija**.
    1. Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Pēc izvēles**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>"Paroles atiestatīšanas" politikas atjaunināšana ar pielāgotu lapas informāciju

Lai atjauninātu "Paroles atiestatīšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.

1. Iepriekš konfigurētās **Paroles atiestatīšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.
1. Atlasiet izkārtojumu **Jauna paroles lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu paroles atiestatīšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.
1. Atlasiet izkārtojumu **Konta verifikācijas lapa**.
1. Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.
1. Laukā **Pielāgots lapas URI** ievadiet pilnu paroles atiestatīšanas verificēšanas URL. Iekļaujiet priedēkli **?preloadscripts=true**. Piemēram, ievadiet ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etiķetēm un aprakstiem paredzētu noklusējuma teksta virkņu pielāgošana

Sākuma komplektā pierakstīšanās moduļi ir iepriekš aizpildīti ar etiķetēm un aprakstiem paredzētām noklusējuma teksta virknēm. Programmatūras izstrādes komplektā (SDK) varat pielāgot šīs virknes, atjauninot vērtības global.json failā, kas paredzēts, lai pierakstītos modulī.

Piemēram, aizmirstās paroles saites noklusējuma teksts ir **Aizmirsta parole?**. Tālāk parādīts šis noklusējuma teksts pierakstīšanās lapā.

![Noklusējuma teksts aizmirstas paroles saitei pierakstīšanās lapā](./media/B2C_SignUp_ModuleFace.png)

Tomēr sākuma komplekta pierakstīšanās moduļa global.json failā varat rediģēt tekstu, lai būtu **Aizmirsāt paroli?**, kā parādīts tālāk redzamajā ilustrācijā.

![Atjauninātais saites teksts pierakstīšanās moduļa global.json failā](./media/B2C_CustomizingStringsForModule.png)

Pēc global.json faila atjaunināšanas un savu izmaiņu publicēšanas jaunais saites teksts parādīsies pierakstīšanās modulī gan Commerce, gan arī aktuālajā pierakstīšanās lapā.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jaunas e-komercijas vietnes izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Tiešsaistes vietnes saistīšana ar kanālu](associate-site-online-store.md)

[robots.txt failu pārvaldība](manage-robots-txt-files.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)
