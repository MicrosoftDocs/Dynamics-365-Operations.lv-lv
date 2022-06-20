---
title: Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ
description: Šis raksts sniedz atbildes uz bieži uzdotiem jautājumiem par un Microsoft Dynamics 365 Commerce Microsoft Teams integrāciju.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 02f10e446349803ce5629fed0be4176f2df2be0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869131"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ

[!include [banner](includes/banner.md)]

Šis raksts sniedz atbildes uz bieži uzdotiem jautājumiem par un Microsoft Dynamics 365 Commerce Microsoft Teams integrāciju.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Kurš veikalā kļūst par grupas īpašnieku, nodrošināt Teams no Commerce? 

Visi veikala vadītāji automātiski tiek pievienoti atbilstošajai komandas grupai kā īpašnieki, lai tie varētu veikt tādas darbības kā privāta kanāla pievienošana un dalībnieku pievienošana vai dzēšana. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Kā programmā Commerce Headquarters darbiniekam piešķirt lomu "sakaru pārvaldnieks"? 

Komunikācijas vadītāji var Microsoft Teams izveidot un publicēt uzdevumu sarakstus. Organizācijas darbiniekiem, kuriem ir jākļūst par sakaru pārvaldniekiem, programmā Commerce headquarters ir jābūt piešķirtai lomai "Mazumtirdzniecības uzdevumu pārvaldnieks".

Lai piešķirtu mazumtirdzniecības uzdevumu pārvaldnieka lomu darbiniekam programmā Commerce Headquarters, izpildiet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Nodarbinātie \> Lietotāji**.
1. Atlasiet darbinieku.
1. Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**.
1. Dialoglodziņā lomu **Piešķirt lomas lietotājam** atlasiet lomu **Mazumtirdzniecības uzdevumu vadītājs** un pēc tam atlasiet **Labi**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Kā var izveidot noteiktu organizācijas hierarhiju, kurā veikt Microsoft Teams augšupielādi?

Programmā Commerce Headquarters katra organizācijas hierarhija ir saistīta ar vienu vai vairākiem nolūkiem. Pārliecinieties, ka ar hierarhiju, kuru vēlaties nodrošināt Microsoft Teams ir saistīts ar **Mazumtirdzniecības pārskatu** mērķi, kā parādīts nākamajā piemēra attēlā. 

![Organizācijas hierarhijas nolūka piemērs programmā Commerce Headquarters.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Kā iespējot mazumtirdzniecības veikala darbinieku pieteik anos Commerce Point Of Sale (POS) izmantojot Azure Active Directory (Azure AD)?

Informāciju par to, kā konfigurēt Commerce POS pierakstīšanās pieredzi autentifikācijas lietošanai Azure AD, skatiet sadaļā [Iespējot Azure Active Directory, autentifikāciju, lai pierakstītos POS](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Kā kartēt veikalus un atbilstošās grupas programmā Commerce Headquarters, ja mana organizācija jau ir izveidojusi Microsoft Teams grupas?

Informāciju par veikalu un grupu kartēšanu, ja pastāv iepriekšējas darba grupas, skatiet sadaļā Kartēt veikalus un atbilstošās darba grupas, ja uzņēmumā ir [iepriekš esošas darba grupas Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Kā notīrīt Microsoft Graph API marķieri, kas saglabāts sesijas krātuvē?

Lietotājam, kurš ir pieteicies pārdošanas punktā (POS), izmantojot Azure Active Directory (Azure AD) kontu, ir jāizrakstās no POS vai jāaizver programma, lai notīrītu sesijas krātuvi. 

> [!TIP]
> Ieteicams ieteicams vienmēr saglabāt darbiniekus, kas bloķē POS termināli vai izrakstīties no sesijas, ja netiek izmantots terminālis. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Kas notiek, ja veikalā nav veikala pārvaldnieku?

Ja veikalam nav pārvaldnieku, veikalam vai Teams grupām netiks izveidota grupa. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Kas notiek, ja veikala vadītājs atstāj uzņēmumu?

Ikviens, kam ir īpašnieka loma, var pievienot jaunu veikala pārvaldnieku programmā Commerce Headquarters un nodrošināt Teams, lai jaunajam vadītājam būtu nepieciešamās grupas Teams privilēģijas. 

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju](enable-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)
