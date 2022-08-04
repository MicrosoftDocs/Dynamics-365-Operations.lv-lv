---
title: Cilvēkresursu nodrošināšana finanšu un operāciju infrastruktūras jomā
description: Šajā rakstā skaidrots process, kā finanšu un operāciju infrastruktūrai nodrošināt Dynamics 365 Human Resources jaunu ražošanas vidi korporācijai Microsoft.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178418"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Cilvēkresursu nodrošināšana finanšu un operāciju infrastruktūras jomā

_**Attiecas uz:** Finanšu un operāciju programmas infrastruktūras personāla vadība_ 

> [!NOTE]
> Sākot no 2022. gada, jaunus cilvēkresursu vides nevar nodrošināt savrupos cilvēkresursu infrastruktūras un jaunos Microsoft Dynamics Lifecycle Services (LCS) projektos nevar izveidot tajā. Klienti var izvietot cilvēkresursu vides finanšu un operāciju infrastruktūrai.

Šajā rakstā skaidrots process, kā finanšu un operāciju infrastruktūrai nodrošināt Dynamics 365 Human Resources jaunu ražošanas vidi korporācijai Microsoft.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat nodrošināt jaunu vidi, jābūt veiktiem šādiem priekšnosacījumi:

- Jūs esat iegādājies Personāla vadības līgumu, izmantojot Mākoņa risinājumu nodrošinātāju (DB) vai uzņēmuma arhitektūru (EA). Ja jums ir esošā Dynamics 365 licence, kas jau ietver personāla vadības pakalpojumu plānu, un jūs nevarat izpildīt šajā rakstā norādītās darbības, sazinieties ar atbalsta dienestu.
- Globālais administrators ir pieteicies ar [Microsoft Dynamics Lifecycle Services (LCS) un](https://lcs.dynamics.com) izveidoja jaunu finanšu un operāciju projektu.

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources apgrozījuma vides nodrošināšana

> [!NOTE]
> Sākot no 2022. gada aprīlī, cilvēkresursu izmēģinājuma vides nebūs pieejamas savrupā programmā. Potenciālie debitori, kuri interesējas par cilvēkresursu spēju vērtēšanu finanšu un operāciju programmās, var izmantot bezmaksas 30 dienu izmēģinājuma versiju kopā ar demonstrācijas datiem. Dynamics 365 Finanses ietvers personāla vadības spējas, kas tiek iesniegtas finanšu infrastruktūrasm, sapludinot savrupu programmu. Papildinformāciju skatiet šeit: [HR piedāvājumu sapludināšana sniedz jums iespējas kopā ar debitoriem](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Lai iegūtu vairāk informācijas par Dynamics 365 finanšu izmēģinājuma versijām, [skatiet pakāpeniskas pamācības](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Human Resources vižu plānošana

Pirms jūs izveidojiet pirmo Human Resources vidi, jums uzmanīgi jāplāno jūsu projekta vides vajadzības. Personāla vadības pamata abonements ietver divas vides: ražošanas vidi un noklusējuma standarta pieņemšanas testa (vadīklu) vidi. Atkarībā no projekta sarežģītības, ir opcija iegādāties papildu vides projekta darbību atbalstam.

Šeit ir daži apsvērumi par papildu izvēles vidēm:

- **Datu migrācija** — datu migrācijas aktivitātes iespējo jūsu kastu vides, ko izmantot testēšanas nolūkos visā projektā. Kad ir papildu vide, testēšanas un konfigurēšanas aktivitātes var turpināties, vienlaikus dažādās vidēs veicot datu migrāciju.
- **Integrācija** – konfigurējiet un pārbaudiet integrācijas, kas varētu ietvert dzimtās integrācijas vai pielāgotas integrācijas, piemēram, algas, kandidātu izsekošanas sistēmas vai atvieglojumu sistēmas un nodrošinātājus.
- **Apmācība** – iespējams, ir nepieciešama atsevišķa vide, kas konfigurēta ar apmācību datu kopu, tā, lai varētu ar darbinieku apmācības palīdzību izmantot jauno sistēmu. 
- **Daudzfāžu projekts** – Jums var būt nepieciešama papildu vide, lai atbalstītu konfigurāciju, datu migrāciju, pārbaudi vai citas aktivitātes projekta fāzē, kas tiek plānota pēc sākotnējās projekta darbības.
- **Izstrāde** finanšu un operāciju infrastruktūrai tagad ir iespējams paplašināt risinājumu un izstrādāt savus pielāgojumus. Katram izstrādātājam ir jāizmanto sava izstrādes vide. Papildinformāciju skatiet izstrādes [vides izvietošanai un piekļuvei](/fin-ops-core/dev-itpro/dev-tools/access-instances).
- **ZELTA** – jaunai izvietošanai kopējā prakse ir izmantot atsevišķu ZELTA vidi, kas tiek turēta konfigurāciju un datu migrācijai. Šo vidi var izmantot visā tās īstenošanai, lai atsvaidzinātu citas vides. Tas tiks izmantots, lai izveidotu jaunu ražošanas vidi, kam ir pamata konfigurācija un datu migrācija. Ražošanas vidi finanšu un operāciju infrastruktūras nevar izvietot, kamēr nav pabeigts gatavības tiešsaistes gatavības process. Papildinformāciju skatiet sadaļā [Sagatavošanās tiešā darba vietu sagatavošanai](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Apsverot jūsu vides, mēs iesakām šādu pieeju:
>
> - Izmantojiet noklusējuma standarta pieņemšanas testa (agrāk nosūtāmā kastīte) vidi vai citu vidi, lai veiktu mocku pārslēgšanu pirms ierašanās tiešsaistē.
> - Paturiet detalizētu pārslēgšanas kontrolsarakstu, kas ietver katru datu pakotni, kas ir nepieciešama gala datu migrēšanai uz ražošanas vidi pārslēgšanas laikā. Šis ieteikums ir īpaši svarīgs, ja jums nav atsevišķaS ZELTA vides, kurā glabāt konfigurācijas.
> - Izmantojiet noklusējuma standarta pieņemšanas testa (agrāk nosūtāmā kastīte) vidi vai citu pakāpju 2 vai augstāku vidi kā jūsu testa vidi visā projektā. Ja jums ir nepieciešamas papildu vides, jūsu organizācija var iegādāties tās par papildu izmaksām.

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana

Lai lietotu LCS un pārvaldītu savas Human Resources vides, vispirms ir jāizveido LCS projekts. Ja migrēsit savu cilvēkresursu vidi uz finanšu un operāciju infrastruktūru, ir jāizveido jauns LCS projekts finanšu un operāciju programmām. Papildinformāciju skatiet sadaļā [Personāla vadības vides migrēšana](hr-admin-migrate-overview). Ja jums jau ir LCS projekts citām finanšu un operāciju programmām, varat iespējot Cilvēkresursu līdzekļus Līdzekļu pārvaldības **darbvietā**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kad jaunais klients pierakstās cilvēkresursiem, abonements ietver Ieviešanas projekta darbalauku. Kad debitors aktivizē pakalpojumu, nomnieka administratoram jāpiesakās, <https://lcs.dynamics.com> izmantojot nomnieka kontu. Organizācijai automātiski tiek izveidota projekta darbvieta. Papildinformāciju skatiet pakalpojumā [Lifecycle Services (LCS) finanšu un operāciju programmu debitoriem](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).

> [!NOTE]
> Lai nodrošinātu sekmīgu nodrošināšanu, kontam, kuru izmantojat cilvēkresursu vides nodrošināšana, ir jābūt piešķirtam vai nu sistēmas administratora lomai, vai sistēmas pielāgotāja lomai vidē, **·** **·** Power Apps kas saistīta ar cilvēkresursu vidi. Papildinformāciju par to, kā piešķirt drošības lomas lietotājiem Microsoft Power Platform, skatiet sadaļā [Lietotāja drošības konfigurēšana resursiem](/power-platform/admin/database-security).

Pirms varat sākt izvietot vides, ir jāpabeidz LCS projekta uzņēmuma process. Papildinformāciju skatiet sadaļā [Projekta tablo.](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding) Papildinformāciju par LCS izmantošanu skatiet lifecycle [Services (LCS) lietotāja rokasgrāmatā](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide).

## <a name="deploy-human-resources-environments"></a>Izvietot cilvēkresursu vides

Finanšu un operāciju programmu, tostarp cilvēkresursu, izvietošanai mākonī nepieciešams, lai saprastu vidi un abonementu, kurā jūs izvietojat, kas var veikt uzdevumus un kādus datus un pielāgojumus jums pārvaldīt. Ieteicams izmantot pakalpojuma kontu nosaukta lietotāja vietā, kad izvietojat jaunas vides. Papildinformāciju par to, kā izvietot vides finanšu un operāciju infrastruktūrai, skatiet mākoņa [izvietošanas pārskatā](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Lai cilvēkresursu ražošanas vidi izvietotu finanšu un operāciju infrastruktūrai, jāpabeidz gatavības laukam uz vietas. Papildinformāciju skatiet sadaļā [Sagatavošanās tiešā darba vietu sagatavošanai](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live). Šis process ietver abonementa novērtējumu LCS. Papildinformāciju skatiet sadaļā [Abonementa vērtētājs](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integrēt Microsoft Power Platform ar Cilvēkresursiem

Microsoft Power Platform sistēma nodrošina iespēju komplektu Dynamics 365 programmām, izmantojot Power Platform administrēšanas centru. Personāla vadības datu izmantošanu var integrēt un paplašināt, izmantojot Microsoft Power Platform. Papildinformāciju par to, kā integrēt cilvēkresursus Microsoft Power Platform, skatiet integrāciju [Microsoft Power Platform ar Finanšu un operāciju programmām](/fin-ops-core/dev-itpro/power-platform/overview).

## <a name="supported-geographies"></a>Atbalstītas ģeogrāfiskās vietas

Informāciju par valodām un ģeogrāfiskām lapām, ko atbalsta cilvēkresursi, [skatiet sadaļā Globāls pēc dizaina: uzziniet par atbalstītajām valstīm un valodām](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi

Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Jums ir īpaši jāpiešķir piekļuve citiem programmas lietotājiem. Jums ir jāpievieno lietotāji un jāpiešķir viņiem atbilstošās lomas Human Resources vidē. Plašāku informāciju skatiet tēmā [Jaunu lietotāju izveide](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [Drošības lomu piešķiršana lietotājiem](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Papildu resursi
Papildinformāciju par to, kā izmantot un pārvaldīt projektus LCS finanšu un operāciju programmas infrastruktūras jomā, izmantojot šādus resursus:

- [Lifecycle Services resursi](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS) lietotāja rokasgrāmata](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Pašapkalpošanās izvietošanas pārskats](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Datu bāzes pārvietošanas operāciju mājas lapa](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
