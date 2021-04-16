---
title: Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats
description: Šajā tēmā sniegts Microsoft Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842702"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā sniegts Microsoft Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats.

Dynamics 365 Commerce ir integrēšana ar Teams, lai palīdzētu klientiem un viņu darbiniekiem uzlabot produktivitāti, sinhronizējot uzdevumu pārvaldību starp divām programmām. Efektīvi uzdevumu pārvaldība, ko Commerce and Teams integrācija nodrošina veikalu vadītājiem un darbiniekiem izveidot uzdevumu sarakstus, piešķirt uzdevumus vairākiem veikaliem un izsekot uzdevumu statusu veikalos no jebkura programmas.

Commerce and Teams integrācija ir pieejama Commerce versijā 10.0.18 laidienā.

## <a name="key-features"></a>Galvenie līdzekļi

Šeit ir dažas galvenās funkcijas, ko nodrošina Commerce un Microsoft Teams integrācija:

- Nodrošināt brigādes, izmantojot labi definētas informācijas priekšrocības no Commerce, piemēram, organizācijas struktūru un informāciju par veikaliem, darbiniekiem, atļaujām un biznesa kontekstu.
- Ērti sinhronizējiet notiekošās izmaiņas (piemēram, jaunu veikalu pievienošana vai jaunu darbinieku nolīgšana) starp Commerce un Teams, bet paturēt Commerce kā galveno organizācijas struktūras datu avotu.
- Integrējiet uzdevumu pārvaldību starp Commerce un Teams, lai palīdzētu uzglabāt darbiniekus, veikalu vadītājus, reģionālos vadītājus un saziņas vadītājus, vadīt uzdevumu pārvaldību no jebkuras lietojumprogrammas.

## <a name="prerequisites-for-using-integration-features"></a>Integrācijas līdzekļu lietošanas priekšnoteikumi

Pirms varat sākt izmantot Microsoft Teams integrācijas līdzekļus, jābūt šādiem priekšnosacījumiem:

- Microsoft 365 Business Standard licence (šī licence ietver Teams.)
- Azure Active Directory (Azure AD) konti visiem veikala vadītājiem un darbiniekiem
- Pārdošanas punkta (POS) sistēmas, kas ir konfigurētas ar Azure AD autentifikāciju

## <a name="conceptual-architecture"></a>Konceptuāla arhitektūra

Šajā attēlā redzama Dynamics 365 Commerce un Microsoft Teams konceptuālā arhitektūra un integrācija, izmantojot Sanfrancisko veikalu kā piemēru. Gan brigādes, gan Commerce POS programma izmanto Microsoft Planner kā repozitoriju, lai no Teams publicētie uzdevumi tiktu parādīti POS programmā, un veikala programmas ekspromta uzdevumos, kas izveidoti POS programmā, tiek parādīti Teams, kā rezultātā ir viengabala uzdevumu pārvaldības pieredze starp programmām.    

![Commerce un Teams integrācijas arhitektūra](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Papildu resursi

[Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju](enable-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)
