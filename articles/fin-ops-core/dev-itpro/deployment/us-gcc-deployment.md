---
title: Dynamics 365 Finance un Dynamics 365 Supply Chain Management ASV valdības kopienas mākonī (GCC)
description: Šajā tēmā sniegta informācija par Microsoft Dynamics 365 ASV valdības precēm, kas ir pieejamas kvalificētām valsts un privātām iestādēm.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817469"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance un Dynamics 365 Supply Chain Management ASV valdības kopienas mākonī (GCC)

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Atlasiet Microsoft Dynamics 365 ASV (ASV) valdības preces, kas ir pieejamas kvalificētām valsts un privātām iestādēm. Šie elementi ir ierobežoti ar sekojošo tipu:

- ASV federālās, valsts, vietējās, tribalas un teritoriālā pārvalde
- Privāti uzņēmumi, kas izmanto Dynamics 365 ASV valdību, lai sniegtu risinājumus valsts iestādēm vai kvalificētiem mākoņa kopienas dalībniekiem
- Privātpersonas, kurām ir debitoru dati, uz ko attiecas valdības noteikumi, un Dynamics 365 ASV valdība ir piemērots pakalpojums, lai atbilstu regulēšanas prasībām

Papildinformāciju skatiet [Dynamics 365 ASV valdībā](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Lai pabeigtu sākotnējo inicializēšanu ieviešanas projektam pakalpojumos Lifecycle Services (LCS), izpildiet norādījumus, kas Microsoft Dynamics [sniegti ieviešanas projektā](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Tomēr neizmantojiet saiti uz publisku LCS, kas ir sniegts šajos instrukcijās. Tā vietā izmantojiet šo URL, lai atvērtu LCS ASV valdības kopienas mākonī (GCC): <https://gov.lcs.microsoftdynamics.us>

Kad sākotnējais borts ir pabeigts, sekojiet instrukcijām [projekta](../lifecycle-services/project-onboarding.md) izpildē. Vēlreiz izmantojiet [GCC LCS,](https://gov.lcs.microsoftdynamics.us) nevis publisko LCS.

## <a name="environment-deployment"></a>Vides izvietošana

Pēc projekta pabeigšanas varat pārskatīt LCS papildu iespējas, kas aprakstītas programmu klientiem pakalpojumā [Lifecycle Services (LCS). Finance and Operations](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) Pēc tam pārvietojieties uz vides izvietošanu.

- Lai izvietotu Microsoft pārvaldītas vides, izmantojot LCS, izpildiet [norādījumus pakalpojumā Lifecycle Services (LCS) programmu Finance and Operations](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) debitoriem.
- Mākoņa viesoto vidi skatiet [sadaļu Izstrādes vides izvietošana un](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) piekļuve. Ir jāpabeidz arī resursu pārvaldnieka ietveršanas process saviem savienotājiem, kā aprakstīts Sadaļā Pabeidziet Azure resursu pārvaldnieka darbības procesu ASV valdības [Lifecycle Services](arm-onbarding-us-goverment.md) projektiem.

> [!NOTE]
> ASV valdības LCS projektos tiek atbalstīti tikai Azure valdības specifiskie Azure abonementi.

## <a name="features-that-arent-available"></a>Līdzekļi, kas nav pieejami

Daži līdzekļi nebūs pieejami izvietošanai GCC vai arī tie nebūs pieejami izmantošanai sistēmā Dynamics 365 GCC. Piemēram, Azure DevOps Pakalpojumi GCC nav pieejami. Tomēr var izmantot lokāli Azure DevOps vai Azure DevOps publiskus pakalpojumus. Papildinformāciju par līdzekļu pieejamību skatiet sadaļā [Biznesa programmu ASV valdības līdzekļu](https://aka.ms/BAPFunctionalParity) pieejamība.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Vai Dynamics 365 Finance šī ir un tiek atbalstīta Dynamics 365 Supply Chain Management GCC-High?

Nē. Dynamics 365 Finance un Dynamics 365 Supply Chain Management tiek atbalstītas tikai GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Vai es varētu izmantot publisku Azure DevOps ar Finanšu un piegādes ķēžu pārvaldību GCC?

Jā, varat izmantot publiskos pakalpojumus, ja jums nav prasību risinājumam, ko sertificē federālā riska un autorizācijas Azure DevOps pārvaldības programma (FEDRAMP). Alternatīvi jūs varat izmantot Azure DevOps Serveri.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Vai viesotā vides Tier-1 izstrādes vide var izvietot Azure komerciālajā abonementā?

Nē. GCC [LCS ir jāizmanto Azure valdības](https://gov.lcs.microsoftdynamics.us) abonements, lai izvietotu mākonī viesotu vidi.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Ko darīt, ja ir nepieciešama pakotne no koplietojamās līdzekļu bibliotēkas, taču tā nav pieejama GCC LCS?

Varat lejupielādēt to pašu pakotni no koplietojamās līdzekļu bibliotēkas [publiskā LCS.](https://lcs.dynamics.com) Alternatīvi jūsu partneris var palīdzēt lejupielādēt pakotni.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Vai koda jaunināšanas rīks ir pieejams GCC?

Nē, koda jaunināšanas rīks pašlaik nav pieejams GCC. Tomēr potenciālo klientu projektu var izveidot publiskā [LCS un](https://lcs.dynamics.com) izmantot koda jaunināšanas rīku. Ievērojiet, ka nevarēsiet izvietot vides potenciālo klientu projektos.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Vai mans partneris var atvērt atbalsta biļeti manā vārdā?

Jā. Tomēr, ja jūsu partneris izmanto identitāti, kas nav GCC identitāte, atbalsta biļete tiks novirzīta uz publiskā atbalsta rindu. Iesakām izmantot debitora GCC tiesības LCS, lai atvērtu atbalsta biļeti.

## <a name="see-also"></a>Skatiet arī

- [Dynamics 365 ASV valdība](/power-platform/admin/microsoft-dynamics-365-government)
- [Biznesa programmu ASV valdības līdzekļu](https://aka.ms/BAPFunctionalParity) pieejamība.
- [Lifecycle Services (LCS) lietotāja rokasgrāmata](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Mākoņa izvietošanas pārskats](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
