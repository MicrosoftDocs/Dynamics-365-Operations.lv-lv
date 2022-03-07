---
title: Finance Insights sākumlapa (priekšskatījums)
description: Finance Insights nodrošina konfigurējamus un paplašināmus modeļus, lai palīdzētu jums precīzi un inteliģenti prognozēt jūsu uzņēmuma naudas plūsmu, prognozēt, kad saņemsiet maksājumu par neapmaksātajiem ieņēmumiem, un ģenerēt budžeta priekšlikumu, kas var paātrināt budžeta procesu. Visi šie līdzekļi ir balstīti uz inteliģentiem algoritmiskās mācīšanās modeļiem.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f0d709ef81fd43c009bf36aba2d4be949b1a737c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338233"
---
# <a name="finance-insights-home-page-preview"></a>Finance Insights sākumlapa (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights nodrošina konfigurējamus un paplašināmus modeļus, lai palīdzētu jums precīzi un inteliģenti prognozēt jūsu uzņēmuma naudas plūsmu, prognozēt, kad saņemsiet maksājumu par neapmaksātajiem ieņēmumiem, un ģenerēt budžeta priekšlikumu, kas var paātrināt budžeta procesu. Visi šie līdzekļi ir balstīti uz inteliģentiem algoritmiskās mācīšanās modeļiem. Kad šīs jaunās iespējas tiek apvienotas ar automatizāciju kreditoru maksājumos un kolekcijās, tās nodrošina bagātīgu un inteliģentu finanšu sistēmu, kas sekmē lēmumu pieņemšanu un palīdz jums rīkoties, lai efektīvi reaģētu uz pašreizējiem un paredzamajiem izaicinājumiem saistībā ar uzņēmējdarbību.

> [!NOTE]
> Finance Insights priekšskatījums ir pieejams izvietošanai Amerikas Savienotajās Valstīs, Kanādā, Lielbritānijā, Eiropā, Āzijas un Klusā okeāna reģionā, Austrālijā un Jaunzēlandē. Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem. Lai iespējotu Finance Insights ražošanas vidēs, vispirms ražošanas vidē ir jāiespējo [Eksportēšana uz Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) iespējas.

> [!NOTE]
> Šī funkcionalitāte tiek piedāvāta kā priekšskatījuma līdzekļu kopa. Kā priekšskatījuma līdzekli nedrīkst izmantot izveidotos algoritmiskās mācīšanās modeļus, lai vadītu vai ietekmētu biznesa lēmumus vai budžeta priekšlikumus. Šī līdzekļa izmantošanu nosaka [Papildu lietošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2105274).

## <a name="prerequisites"></a>Priekšnosacījumi

Šajā sadaļā uzskaitītas prasības Finance Insights izmantošanai. Ja iespējams, tiek nodrošinātas saites uz papildu informācijas avotiem.

### <a name="legal-requirements"></a>Juridiskās prasības

Lai pieteiktos priekšskatījuma programmai, aizpildiet [Finance Insights priekšskatījuma programmai Dynamics 365 Finance līgumu](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Sistēmas prasības

Lai priekšskatītu Finance Insights, ir nepieciešama 2. līmeņa vide (daudzlodziņu). Lai iegūtu pilnīgu informāciju par vidi, skatiet sadaļu [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versijas prasības

Šis dokuments attiecas uz Finance and Operations programmu (platformas atjauninājums 35) versiju 10.0.11 un jaunākām versijām.

### <a name="historical-data-requirements"></a>Vēsturiskās datu prasības

Lai pareizi iemācītu algoritmiskās mācīšanās modeli, kas tiek izmantots debitoru maksājumu prognožu funkcijai, ir nepieciešami debitoru rēķini vismaz viena gada apjomā.

### <a name="role-and-permission-requirements"></a>Lomu un atļauju prasības

Tiks veiktas izmaiņas korporācijai Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps un Azure. Šajās vidēs ir nepieciešamas pareizās atļaujas. Tālāk ir minēti dažu veicamo izmaiņu piemēri.

- Platformā Microsoft Power Platform tiks izveidota jauna vide.
- Pakalpojumā Azure tiks izveidots krātuves konts, galvenā glabātava un programma.
- Active Directory nomnieka administratoram būs jāautorizē programma AI Builder, lai piekļūtu datu ezeram.
- Līdzeklis tiks ieslēgts programmā Dynamics 365.

Zināšanas par resursu radīšanas un pārvaldīšanas procesu pakalpojumā Azure, Microsoft Dataverse un LCS būss noderīgas, pabeidzot šo procesu.

## <a name="configure-finance-insights"></a>Finance Insights konfigurēšana

Lai varētu izmantot Finance Insights, ir jāpabeidz dažas konfigurēšanas darbības. Papildu informāciju par to, kā konfigurēt Finance Insights, skatiet:
  - Versijām līdz 10.0.19: [Finance Insights konfigurācija (priekšskatījums) – versijām līdz 10.0.19](configure-for-fin-insites.md).
  - Sākot ar versiju 10.0.20 un jaunākām: [Finance Insights konfigurācija (priekšskatījums) – versijai 10.0.20 un jaunākām](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Datu integrētāja projekta izveide

Jums būs jāizveido datu integrēšanas projekts, lai dati, kurus ģenerē algoritmiskās mācīšanās modelis, varētu ieplūst pakalpojumā Dynamics 365 Finance. Šī projekta izveidošanas darbības skatiet sadaļā [Datu integrēšanas projekta izveide](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finance Insights iespēju iespējošana

Kad konfigurācijas darbības ir pabeigtas un ir iestatīti demonstrācijas dati, ir jāieslēdz un jāiestata katra iespēja, ko plānojat izmantot: debitoru maksājumu prognozes, naudas plūsmas prognozes un budžeta priekšlikumi.

### <a name="enable-customer-payment-predictions"></a>Debitora maksājumu prognožu iespējošana
Ja izmantojat demonstrācijas datus, lai pārbaudītu debitoru maksājumu prognozes, iespējams, būs jāimportē papildu demonstrācijas dati, lai veiksmīgi izveidotu AI modeli. 

Lai iespējotu debitoru maksājumu prognozes, ir jāpabeidz darbības, lai izveidotu algoritmiskās mācīšanās modeli, kas izmanto jūsu organizācijas datus, lai ģenerētu prognozes par to, kad klienti varētu apmaksāt neapmaksātos rēķinus un kad noteikti rēķini, visticamāk, tiks apmaksāti. Plašāku informāciju un konkrētas veicamās darbības skatiet sadaļā [Debitoru maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Naudas plūsmas prognozēšanas iespējošana
Lai iespējotu naudas plūsmas prognozēšanu, ir jāpabeidz darbības, lai izveidotu algoritmiskās mācīšanās modeli, kas izmanto jūsu organizācijas datus, lai izveidotu naudas plūsmas prognozes. Plašāku informāciju un konkrētas veicamās darbības skatiet sadaļā [Naudas plūsmas prognozēšanas iespējošana](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Budžeta priekšlikumu iespējošana

Budžeta priekšlikumu līdzeklis izmanto algoritmiskās mācīšanās modeli kopā ar organizācijas vēsturiskajiem datiem, lai ģenerētu budžeta priekšlikumu. Ģenerētais priekšlikums var palīdzēt sākt budžeta izveides procesu, kas ir efektīvāks par manuālu procesu. Konkrētas šī līdzekļa iespējošanas darbības skatiet sadaļā  [Budžeta priekšlikumu iespējošana](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finance Insights līdzekļu izmantošana

### <a name="using-customer-payment-predictions"></a>Debitora maksājumu prognožu izmantošana

Inteliģentā naudas plūsmas prognozēšana tiek veidota, pamatojoties uz esošo naudas plūsmas prognozēšanas funkcionalitāti pakalpojumā Dynamics 365 Finance. Lai pārskatītu esošo iespēju, skatiet sadaļu [Skaidras naudas plūsmas prognozēšana](../cash-bank-management/cash-flow-forecasting.md).

- Lai uzzinātu, kā debitoru maksājumu prognozes var sniegt informāciju, kas nepieciešama proaktīvām parādu piedziņas darbībām, skatiet sadaļu [Debitoru maksājumu prognožu izmantošana](use-customer-payment-predictions.md).
- Lai iegūtu informāciju, kas var palīdzēt novērtēt prognozēšanas modeļa efektivitāti pēc tam, kad esat sācis izmantot līdzekli, skatiet sadaļu [Sākotnējā debitora maksājuma prognozēšanas modeļa izvērtēšana](evaluate-payment-prediction.md).
- Lai iegūtu informāciju, kas var palīdzēt koriģēt datus, kuri tiek izmantoti prognozēšanas izveidei, un tādējādi var palīdzēt uzlabot tās efektivitāti, skatiet sadaļu [Prognozēšanas modeļa uzlabošana](improve-model.md).

Lai uzzinātu vairāk par AI prognozēšanas modeļu rezultātiem, skatiet sadaļu [Algoritmiskās mācīšanās modeļu rezultāti](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Naudas plūsmas prognožu izmantošana

Naudas plūsmas prognozēšanas spēja var palīdzēt precīzāk novērtēt jūsu finansiālo situāciju. 

- Lai uzzinātu par jaunajām naudas plūsmas prognožu iespējām, skatiet sadaļu [Naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).
- Lai iegūtu informāciju par ārējo datu importēšanu, lai iekļautu tos savā naudas plūsmas prognozē, skatiet sadaļu [Ārēju datu izmantošana naudas plūsmas prognozēs](external-data-in-cash-flow.md). 
- Informāciju par to, kā izmantot mākslīgā intelekta modeli, lai projicētu naudas plūsmu tuvākajā laikā, skatiet sadaļu [Finansiālais stāvoklis](cash-position.md).
- Lai iegūtu informāciju par naudas plūsmas pozīciju un naudas plūsmas prognožu saglabāšanu momentuzņēmumos, kā arī lai salīdzinātu momentuzņēmumus ar faktiskajiem datiem, skatiet sadaļu [Momentuzņēmumu apskats](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budžeta priekšlikuma izmantošana

Informāciju par budžeta izveides paātrināšanu skatiet sadaļā [Budžeta priekšlikumi](budget-proposals.md). 

## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
