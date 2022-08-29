---
title: Konfigurējiet CPOS, lai lietotu pielāgotu Azure AD programmu
description: Šajā rakstā ir izskaidrots, kā konfigurēt Cloud POS (CPOS) lietot pielāgotu Azure Active Directory (Azure AD) programmu.
author: boycez
ms.date: 08/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: baa0c3da25308345037b5dd1b4c5907d6213e7f7
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/03/2022
ms.locfileid: "9223821"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Konfigurējiet CPOS, lai lietotu pielāgotu Azure AD programmu

[!include [banner](includes/banner.md)]

Pēc noklusējuma Cloud POS (CPOS) Microsoft Dynamics 365 Commerce norāda uz reģistrēto pirmās puses Microsoft programmu Azure Active Directory (Azure AD). Tāpēc jūs varat izmantot CPOS bez nepieciešamības veikt izmaiņas Azure AD. Tomēr, iespējams, vēlēsieties norādīt savu CPOS instanci pielāgotajai Azure AD programmai, ko kontrolējiet. Šajā rakstā ir izskaidrots, kā konfigurēt CPOS pielāgotās programmas Azure AD lietošanai.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Pielāgotas mazumtirdzniecības servera programmas iestatīšana programmā Azure AD

Lai izveidotu un konfigurētu pielāgotu Retail Server programmu Azure AD, veiciet šādas darbības.

1. Piesakieties administratora [Azure Active Directory centrā,](https://aad.portal.azure.com) izmantojot jebkuru Azure AD lietotāja kontu. Lietotāja kontam nav jābūt administratora tiesībām.
1. Atlasīt **Azure Active Directory**.
1. Atlasiet **Programmas reģistrācijas un** pēc tam atlasiet **Jauna reģistrācija**, lai atvērtu **dialoglodziņu Reģistrēt** pieteikumu.
1. Iestatiet tālāk norādītos laukus.

    - **Nosaukums** — ievadiet programmas pielāgoto nosaukumu. Piemēram, ievadiet custom **Retail Server**.
    - **Atbalstīt kontu tipus** – atlasīt noklusējuma opciju Konti **tikai šajā organizācijas direktorijā (tikai Microsoft - viens nomnieks).**
    - **URI novirzīšana** — šis lauks nav obligāts. Atstājiet to tukšu.
    - **Pakalpojumu koka ID** – šis lauks nav obligāts. Atstājiet to tukšu.
    
1. Atlasiet **Reģistrēt**. Tiek parādīta jaunās reģistrētās programmas konfigurācijas lapa.
1. Sadaļā Pārskata **pamati \>** atlasiet Pievienot programmas **ID URI un pēc** tam atlasiet **Iestatīt** blakus programmas **ID URI**. Atzīmējiet ieteikto vērtību un pēc tam atlasiet **Saglabāt**, lai akceptētu šo vērtību. 
1. Atlasiet **Pievienot tvērumu un** pēc tam iestatiet sekojošos laukus:

    - **Sfēras** nosaukums – ievadiet pielāgošanas nosaukumu sfērai. Piemēram, ievadiet **Legacy.Access.Full**.
    - **Kas var atļaut** atļauju – norādiet, vai gan administratori, gan lietotāji vai tikai administratori var sniegt atļauju, balstoties uz jūsu organizācijas drošības politiku.
    - **Administratora atļaujas parādāmais vārds** - ievadiet parādāmo nosaukumu. Piemēram, ievadiet Access **Retail Server**.
    - **Administratora atļaujas apraksts** – ievadiet aprakstu. Piemēram, ievadiet " **Sniedz piekļuvi Retail Server API"**.

1. Atlasiet **Pievienot tvērumu,** lai pabeigtu sfēras izveides procesu.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Pielāgotas CPOS programmas iestatīšana programmā Azure AD

Lai izveidotu un konfigurētu pielāgotu CPOS programmu Azure AD, sekojiet šiem soļiem.

1. Piesakieties administratora [Azure Active Directory centrā,](https://aad.portal.azure.com) izmantojot jebkuru Azure AD lietotāja kontu. Lietotāja kontam nav jābūt administratora tiesībām.
1. Atlasīt **Azure Active Directory**.
1. Atlasiet **Programmas reģistrācijas un** pēc tam atlasiet **Jauna reģistrācija**, lai atvērtu **dialoglodziņu Reģistrēt** pieteikumu.
1. Iestatiet tālāk norādītos laukus.

    - **Nosaukums** — ievadiet programmas nosaukumu. Piemēram, ievadiet Custom **Cloud POS**.
    - **Atbalstīt kontu tipus** – atlasīt noklusējuma opciju Konti **tikai šajā organizācijas direktorijā (tikai Microsoft - viens nomnieks).**
    - **URI** virzienmaiņa **- atlasiet vienas lapas lietojumprogrammu (SPA)** nolaižamajā sarakstā un pēc tam ievadiet savu CPOS URI.
    - **Pakalpojumu koka ID** – šis lauks nav obligāts. Atstājiet to tukšu.

1. Atlasiet **Reģistrēt**. Tiek parādīta jaunās reģistrētās programmas konfigurācijas lapa.
1. **Sadaļā Manifests** iestatiet **oauth2AllowIdTokenImplicitFlow** **un oauth2AllowImplicitFlow** parametrus **kā** patiesu, un pēc tam atlasiet **Saglabāt**.
1. Lai pievienotu **divas prasības**, sadaļā Marķiera konfigurācija izpildiet šīs darbības:

    - Atlasiet Pievienot **neobligātu prasību**. Iestatiet marķiera **tipa** lauku uz **ID** un pēc tam atlasiet sida **prasību**. Atlasiet **Pievienot**.
    - Atlasiet Pievienot **neobligātu prasību**. Iestatiet marķiera **tipa** lauku piekļuvei **un** pēc tam atlasiet sida **prasību**. Atlasiet **Pievienot**.

1. **API atļauju sadaļā** atlasiet **Pievienot atļauju**.
1. Cilnē API **mana organizācija izmanto** meklējiet mazumtirdzniecības servera programmu, [ko izveidojāt sadaļā Pielāgota mazumtirdzniecības servera programmas Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) iestatīšana. Pēc tam atlasiet **Pievienot atļaujas**.
1. **Sadaļā Pārskats** atzīmējiet vērtību laukā **Programmas (klienta) ID**.

## <a name="update-the-cpos-configuration-file"></a>Atjaunināt CPOS konfigurācijas failu

Atveriet failu CPOS config.json un veiciet tajā šādus atjauninājumus.

1. Aizstājiet **atslēgas AADClientId** **vērtību ar programmas (klienta) ID** vērtību pielāgotajai CPOS [programmai, ko izveidojāt sadaļā Pielāgota CPOS programmas Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) iestatīšana.
1. Aizstājiet **atslēgas AADRetailServerResourceId** **vērtību ar tās pielāgotās Retail Server** programmas URI [vērtību, kuru izveidojāt sadaļā Pielāgotās mazumtirdzniecības servera programmas Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) iestatīšana.

CPOS izmantos abus parametrus, kad tiek sūtīts pieprasījums Azure AD iegūt drošības marķieri.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Atjaunināt identitātes nodrošinātāju iestatījumus programmā Commerce Headquarters

Pēc tam ir jāatjaunina programmas Commerce Headquarters identitātes nodrošinātāju iestatījumi.

1. Programmā Commerce headquarters atveriet lapu Commerce **koplietojamie** parametri.
1. Cilnes Identitātes **nodrošinātāji** sadaļā **Identitātes** nodrošinātāji atlasiet rindu, uz kuru ir iestatīts lauks Tips, **·** **Azure Active Directory** **un** izdevēja lauks norāda savu Azure AD nomnieku. Šis iestatījums norāda, ka strādāsiet ar pakārtotajiem režģiem, kas satur ar jūsu nomnieku saistītos datus par identitātes Azure AD nodrošinātāju.
1. Sadaļā Balstās **puses** atlasiet **Pievienot**, lai pievienotu rindu.
1. Iestatiet tālāk norādītos laukus.

    - **ClientId** — ievadiet **programmas (klienta) ID** vērtību pielāgotajai CPOS [programmai, ko izveidojāt sadaļā Pielāgotas CPOS programmas Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) iestatīšana.
    - **Tips** – atlasīt **Publisks**.
    - **UserType** – atlasiet **darbinieku**.

1. Atlasiet pievienoto rindu. Servera **resursu ID sadaļa zem sadaļas** **·** **Atkarīgas** puses parāda mazumtirdzniecības servera programmu ID, kuriem var piekļūt no programmas, ko atlasījāt režģī Atkarīgas puses.
1. **Servera resursu ID sadaļā** atlasiet **Pievienot**, lai pievienotu rindu.
1. Laukā **Servera resursa ID** ievadiet programmas ID URI **vērtību pielāgotajai mazumtirdzniecības servera** programmai, [ko izveidojāt sadaļā Pielāgotas mazumtirdzniecības servera programmas Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) iestatīšana.

    > [!IMPORTANT]
    > Visi iepriekšējos soļos minētie lauki ir reģistrjutīgi. Ievadītajām vērtībām precīzi jāatbilst vērtībām, kas ir konfigurētas Azure AD administratora centrā.

1. Dodieties uz **mazumtirdzniecības un commerce \> IT** sadales grafiku un palaidiet **1110** (globālās **konfigurācijas**) darbu.

Tagad jūs varat aktivizēt CPOS ierīces, izmantojot savu Azure AD programmu.

## <a name="additional-resources"></a>Papildu resursi

[Pārdošanas punkta (POS) ierīces aktivizēšana](dev-itpro/retail-device-activation.md)

[Aktivizēšanas kontu pārvaldība un ierīču validēšana](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
