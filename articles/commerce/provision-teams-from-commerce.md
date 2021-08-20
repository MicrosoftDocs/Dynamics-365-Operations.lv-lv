---
title: Microsoft Teams nodrošināšana no Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīts, kā nodrošināt Microsoft Teams, izmantojot organizācijas Dynamics 365 Commerce datus.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 715b18acb10edebafe60805393cbc16c5be513ef3605cf7a575ff98362443bb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766437"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Microsoft Teams nodrošināšana no Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā nodrošināt Microsoft Teams, izmantojot organizācijas Dynamics 365 Commerce datus.

Dynamics 365 Commerce piedāvā ērtu veidu, kā nodrošināt Teams, ja vēl neesat iestatījis grupas saviem mazumtirdzniecības veikaliem. Izmantojot pareizi definētas informācijas priekšrocības no Commerce, ko vēlaties izmantot programmā Teams, varat palīdzēt veikala darbiniekiem sākt darbu Teams. Šajā informācijā ir iekļauta organizācijas hierarhija, veikalu nosaukumi, darbinieku informācija un Azure Active Directory (Azure AD) konti. 

Teams nodrošinājuma procesam ir divas galvenās darbības:

1. Programmā Teams izveidojiet grupu katram mazumtirdzniecības veikalam un pievienojiet veikala darbiniekus kā atbilstošās grupas dalībniekus. Ja darbinieks ir saistīts ar vairāk nekā vienu mazumtirdzniecības veikalu, šo faktu atspoguļos grupas dalība. Tiks izveidota sakaru grupa, kurā iekļauti reģionālie vadītāji kā dalībnieki, lai palīdzētu publicēt uzdevumus no Teams.
1. Augšupielādējiet organizācijas hierarhiju no Commerce uz Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Nodrošināt Teams Commerce headquarters

Pirms Microsoft Teams nodrošināšanas izpildiet šos uzdevumus:

- Apstipriniet, ka visi reģionālie vadītāji ir pazinuši sakaru vadītājus.
- Apstipriniet, ka katra veikala vadītāja un darbinieka Azure konts ir saistīts ar šī vadītāja vai darbinieka darbinieka ierakstu programmā Commerce Headquarters.

Lai nodrošinātu programmu Teams komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.
1. Darbību rūtī atlasiet **Grupu nodrošināšana**. Ir izveidots pakešuzdevums ar nosaukumu **Grupu nodrošināšana**.
1. Dodieties uz **Sistēmas administrēšana \> Uzziņas \> Pakešdarbi** un atrodiet pēdējo darbu ar aprakstu **Teams nodrošināšana**. Uzgaidiet, kamēr šis darbs tiks pabeigts.

> [!TIP]
> Ja neviens no jūsu reģionālajiem vadītājiem, veikalu vadītājiem un veikala darbiniekiem nav saistīts ar brigādes licenci, varat saņemt šādu kļūdas ziņojumu: "Neizdevās izgūt lietotājam atbildīgās sku kategorijas." Lai labotu problēmu, darbību rūtī atlasiet **Sinhronizēt grupas un dalībniekus**.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Pārbaudīt Teams nodrošinājumu Teams administrēšanas centrā

Lai apstiprinātu Microsoft Teams nodrošināšanu Microsoft Teams administrēšanas centrā, sekojiet šiem soļiem.
    
1. Dodieties uz [Teams administrēšanas centru](https://admin.teams.microsoft.com/) un piesakieties kā sava e-komercijas nomnieka administrators.
1. Kreisajā navigācijas rūtī atlasiet **Teams**, lai to izvērstu, un pēc tam atlasiet **Pārvaldīt grupas**.
1. Pārliecinieties, vai katram Commerce mazumtirdzniecības veikalam ir izveidota viena grupa.
1. Atlasiet grupu un apstipriniet, ka veikala darbinieki ir tai pievienoti kā dalībnieki.
1. Kreisajā navigācijas rūtī atlasiet **Lietotāji** un apstipriniet, ka visi veikala darbinieki visos veikalos ir pievienoti kā lietotāji.

Šajā attēlā parādīts **Grupu pārvaldības** lapas piemērs Teams administrēšanas centrā.

![Grupu pārvaldības lapas piemērs Grupu administrēšanas centrā.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Augšupielādējiet organizācijas hierarhiju no Commerce uz Teams
    
Commerce organizācijas hierarhiju var izmantot, lai publicētu uzdevumus visos vai atlasītajiem Microsoft Teams veikaliem, kas izmanto vienādu hierarhijas struktūru.

Lai augšupielādētu Commerce organizācijas hierarhiju uz Teams, veiciet tālāk norādītās darbības.
    
1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanālu iestatījumi \> Microsoft Teams integrācijas konfigurācija**.
1. Atlasiet **Lejupielādes mērķa hierarhija** un pēc tam atlasiet **Mazumtirdzniecības veikali pēc reģiona**, lai lejupielādētu komatatdalīto vērtību (CSV) failu organizācijas hierarhijā.
1. Instalējiet Microsoft Teams PowerShell moduli, izpildot norādītās darbības sadaļā [Instalēt Microsoft Teams Power Shell](/microsoftteams/teams-powershell-install).
1. Kad tiek parādīta uzvedne Teams PowerShell logā, piesakieties, nomniekam izmantojot Azure AD administratora kontu.
1. Sekojiet soļiem sadaļā [Iestatīt savas grupas mērķa hierarhiju](/microsoftteams/set-up-your-team-hierarchy), lai augšupielādētu CSV failu mērķa hierarhijai.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Pārbaudiet, vai organizācijas hierarhija tika augšupielādēta Teams

Pārbaudiet, vai organizācijas hierarhija tika augšupielādēta Microsoft Teams, rīkojieties šādi.

1. Piesakieties Teams kā saziņas pārvaldītājs.
1. Navigācijas rūtī pa kreisi atlasiet **Uzdevumi pēc plānotāja**.
1. Cilnē **Publicētie saraksti** izveidojiet jaunu sarakstu, kam ir fiktīvs uzdevums.
1. Atlasiet **Publicēt**. Organizācijas hierarhijai ir jābūt parādītai dialoglodziņā **Atlasīt, kas tiks publicēts**, kā parādīts piemērā šajā ilustrācijā.

![Organizācijas hierarhijas piemērs dialoglodziņā Atlasīt, kas tiks publicēts.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju](enable-teams-integration.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)