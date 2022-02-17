---
title: Dynamics 365 Finance un Dynamics 365 Supply Chain Management ASV valdības kopienas mākonī (PLSP)
description: Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 ASV valdības produktiem, kas ir pieejami kvalificētām valdības un privātām struktūrām.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062290"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance un Dynamics 365 Supply Chain Management ASV valdības kopienas mākonī (PLSP)

[!include [banner](../includes/banner.md)]



Izvēlieties Microsoft Dynamics 365 Amerikas Savienoto Valstu (ASV) valdības produktus, kas ir pieejami kvalificētām valdības un privātām struktūrām. Šīs vienības ir ierobežotas līdz šādiem veidiem:

- ASV federālās, valsts, vietējās, cilšu un teritoriālās valdības struktūras
- Privātas entītijas, kas izmanto Dynamics 365 US Government, lai nodrošinātu risinājumus valsts iestādēm vai kvalificētiem mākoņkopas dalībniekiem
- Privātas entītijas, kurām ir klientu dati, uz kuriem attiecas valdības noteikumi, un Dynamics 365 US Government ir piemērots pakalpojums, lai izpildītu normatīvās prasības

Informāciju skatiet [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Lai pabeigtu sākotnējo uzsēdināšanu lifecycle services (LCS) īstenošanas projektam Microsoft Dynamics, izpildiet norādījumus, kas sniegti [uz kuģa īstenošanas projektā](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Tomēr neizmantojiet saiti uz publisko LKS, kas ir sniegta šajos norādījumos. Tā vietā izmantojiet šo URL, lai atvērtu LCS ASV valdības kopienas mākonim (GCC):<https://gov.lcs.microsoftdynamics.us>.

Kad sākotnējā iebrauciens ir pabeigts, izpildiet projekta borta [norādījumus](../lifecycle-services/project-onboarding.md). Vēlreiz izmantojiet [LKS GCC](https://gov.lcs.microsoftdynamics.us), nevis publisko LKS.

## <a name="environment-deployment"></a>Vides izvietošana

Kad esat pabeidzis projekta ieeju, varat pārskatīt LCS papildu iespējas, kas aprakstītas [lifecycle Services (LCS) finance and operations programmu klientiem](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Pēc tam pārejiet uz vides izvietošanu.

- Lai izvietotu Microsoft pārvaldītas vides, izmantojot LCS, izpildiet finanšu un operāciju programmu klientu [dzīves cikla pakalpojumu (LCS) norādījumus](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Mākoņa mitinātas vides skatiet rakstā [Izstrādes vides izvietošana un piekļuve tiem](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Ir arī jāpabeidz resursu pārvaldnieka pieteikšanās process saviem savienotājiem, kā aprakstīts sadaļā [Azure Resource Manager onboarding process ASV valdības dzīves cikla pakalpojumu projektiem](arm-onbarding-us-goverment.md).

> [!NOTE]
> ASV valdības LKS projektiem tiek atbalstīti tikai Azure Government specifiski Azure abonementi.

## <a name="features-that-arent-available"></a>Līdzekļi, kas nav pieejami

Daži līdzekļi nebūs pieejami izvietošanai GCC, vai arī tie nebūs pieejami izmantošanai ar Dynamics 365 GCC. Piemēram, Azure DevOps pakalpojumi nebūs pieejami PLSP. Tomēr var izmantot gan klātienes, Azure DevOps gan sabiedriskos Azure DevOps pakalpojumus. Detalizētu informāciju par līdzekļu pieejamību skatiet [business applications US Government līdzekļu pieejamība](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Vai ir Dynamics 365 Finance un Dynamics 365 Supply Chain Management tiek atbalstīts GCC-High?

Nē. Dynamics 365 Finance un Dynamics 365 Supply Chain Management tiek atbalstīti tikai PLSP.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Vai es varu izmantot publisko Azure DevOps ar finanšu un piegādes ķēdes pārvaldību PLSP?

Jā, jūs varat izmantot sabiedriskos Azure DevOps pakalpojumus, ja jums nav prasību attiecībā uz risinājumu, ko sertificējusi Federālā riska un autorizācijas pārvaldības programma (FEDRAMP). Varat arī izmantot Azure DevOps serveri.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Vai es varu izvietot mākonī izvietotu vides 1. līmeņa izstrādes vidi Azure komerciālajā abonementā?

Nē. Programmā [LCS for GCC](https://gov.lcs.microsoftdynamics.us) ir jāizmanto Azure Government abonements, lai izvietotu mākonī viesotu vidi.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Ko es varu darīt, ja man ir nepieciešama pakotne no koplietojamo līdzekļu bibliotēkas, bet tā nav pieejama LCS GCC?

To pašu pakotni var lejupielādēt no koplietojamo līdzekļu bibliotēkas [publiskajā LKS](https://lcs.dynamics.com). Vai arī jūsu partneris var palīdzēt jums lejupielādēt paketi.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Vai kods jaunināšanas rīks ir pieejams GCC?

Nē, koda jaunināšanas rīks pašlaik nav pieejams GCC. Tomēr varat izveidot potenciālo klientu projektu [publiskajā LKS](https://lcs.dynamics.com) un izmantot koda jaunināšanas rīku. Ņemiet vērā, ka potenciālo klientu projektos nevarēsit izvietot vides.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Vai mans partneris var atvērt atbalsta biļeti manā vārdā?

Jā. Tomēr, ja jūsu partneris izmanto identitāti, kas nav GCC identitāte, atbalsta biļete tiks novirzīta uz valsts atbalsta rindu. Mēs iesakām izmantot klientu GCC tiesības LKS, lai atvērtu atbalsta biļetes.

## <a name="see-also"></a>Skatiet arī

- [Dynamics 365 ASV valdība](/power-platform/admin/microsoft-dynamics-365-government)
- [Biznesa lietojumprogrammas ASV valdības līdzekļu pieejamība](https://aka.ms/BAPFunctionalParity).
- [Lifecycle Services (LCS) lietotāja rokasgrāmata](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Mākoņa izvietošanas pārskats](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
