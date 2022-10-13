---
title: Finance Insights sākumlapa
description: Finance Insights nodrošina konfigurējamus un paplašināmus modeļus, lai palīdzētu jums precīzi un inteliģenti prognozēt jūsu uzņēmuma naudas plūsmu, prognozēt, kad saņemsiet maksājumu par neapmaksātajiem ieņēmumiem, un ģenerēt budžeta priekšlikumu, kas var paātrināt budžeta procesu. Visi šie līdzekļi ir balstīti uz inteliģentiem algoritmiskās mācīšanās modeļiem.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643882"
---
# <a name="finance-insights-home-page"></a>Finance Insights sākumlapa

[!include [banner](../includes/banner.md)]

Finanšu ieskatījumi sniedz konfigurējamus un paplašināmus risinājumus, lai palīdzētu jums intelligently prognozēt uzņēmuma naudas plūsmu, prognozējot, kad saņemat maksājumus neapmaksātiem debitoriem, un ģenerēt budžeta priekšlikumu, kas var palīdzēt paātrināt budžeta procesu. Šīs funkcijas izmanto viedas mašīnas apmācību veidnes, lai veidotu modeļus, izmantojot jūsu nodrošinātos datus (tostarp datus no trešās personas, piemēram, biroja plaša patēriņa pārskata informāciju). Šīs inteliģentas iespējas informē par lēmumu pieņemšanu un palīdz veikt darbības, lai efektīvi atbildētu uz pašreizējiem un paredzamiem biznesa darījumiem. Jūs esat atbildīgs par visiem datiem, kas tiek izmantoti finanšu ieskatos vai to rezultāts.

> [!NOTE]
> Finanšu ieskati ir pieejami izvietošanai Amerikas Savienotajās Valstīs, Kanādā, Apvienotajā Karalistē, Eiropā, Klusā okeāna, Japānas, Austrālijā un Jaunzēlande. Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem.

## <a name="prerequisites"></a>Priekšnosacījumi

Šajā sadaļā uzskaitītas prasības Finance Insights izmantošanai. Ja iespējams, tiek nodrošinātas saites uz papildu informācijas avotiem.

### <a name="system-requirements"></a>Sistēmas prasības

Lai priekšskatītu Finance Insights, ir nepieciešama 2. līmeņa vide (daudzlodziņu). Lai iegūtu pilnīgu informāciju par vidi, skatiet sadaļu [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versijas prasības

Šis raksts attiecas uz Microsoft Dynamics 365 Finanšu versiju 10.0.21 vai jaunāku versiju.

### <a name="license-requirements"></a>Licences prasības

Finanšu ieskati izmanto kredītus AI Builder, lai izveidotu finanšu prognozes. Visas šim licences, kas nepieciešamas, tiek iekļautas nomnieka licencē. Katrs Dynamics 365 finanšu nomnieks katru mēnesi nodrošina 20 000 AI Builder kredītus. Ja biznesa vajadzībām nepieciešami papildu kredīti, tos var iegādāties tieši no uzņēmuma vajadzībām AI Builder.

### <a name="historical-data-requirements"></a>Vēsturiskās datu prasības

Lai pareizi iemācītu algoritmiskās mācīšanās modeli, kas tiek izmantots debitoru maksājumu prognožu funkcijai, ir nepieciešami debitoru rēķini vismaz viena gada apjomā. Naudas plūsmas prognozēm ieteicams izmantot trīs vēsturisko datu gadus. Vēsturiskā budžeta un/vai faktisko budžetu trīs gadi ir ieteicami inteliģentam budžeta priekšlikumiem.

## <a name="configure-finance-insights"></a>Finance Insights konfigurēšana

Konfigurācijas soļi ir jāveic pirms Finanšu ieskatu lietošanas. Lai iegūtu papildinformāciju par to, kā konfigurēt finanšu ieskatus, skatiet sadaļu [Finanšu ieskatu konfigurēšana](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Datu integrētāja projekta izveide

Ir jāizveido datu integrētāja projekts, lai dati, ko datora apmācības modelis ģenerē, varētu ieplūst Dynamics 365 finansēs. Šī projekta izveidošanas darbības skatiet sadaļā [Datu integrēšanas projekta izveide](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Finance Insights iespēju iespējošana

Kad konfigurācijas darbības ir pabeigtas un ir iestatīti demonstrācijas dati, ir jāieslēdz un jāiestata katra iespēja, ko plānojat izmantot: debitoru maksājumu prognozes, naudas plūsmas prognozes un budžeta priekšlikumi.

### <a name="enable-customer-payment-predictions"></a>Debitora maksājumu prognožu iespējošana
Ja izmantojat demonstrācijas datus, lai pārbaudītu debitoru maksājumu prognozes, iespējams, būs jāimportē papildu demonstrācijas dati, lai veiksmīgi izveidotu AI modeli. 

Lai iespējotu Debitoru maksājumu prognozes, jāveic soļu kopums, lai izveidotu iekārtu apmācības modeli, kas izmanto jūsu organizācijas datus, lai ģenerētu prognozes par to, kad debitori, iespējams, apmaksā neapmaksātu rēķinus un kad konkrēti rēķini, iespējams, tiks apmaksāti. Plašāku informāciju un konkrētas veicamās darbības skatiet sadaļā [Debitoru maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Naudas plūsmas prognozēšanas iespējošana
Lai iespējotu naudas plūsmas prognozēšanu, ir jāpabeidz darbības, lai izveidotu algoritmiskās mācīšanās modeli, kas izmanto jūsu organizācijas datus, lai izveidotu naudas plūsmas prognozes. Plašāku informāciju un konkrētas veicamās darbības skatiet sadaļā [Naudas plūsmas prognozēšanas iespējošana](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Budžeta priekšlikumu iespējošana

Budžeta priekšlikumu līdzeklis izmanto algoritmiskās mācīšanās modeli kopā ar organizācijas vēsturiskajiem datiem, lai ģenerētu budžeta priekšlikumu. Ģenerētais priekšlikums var palīdzēt sākt budžeta izveides procesu, kas ir efektīvāks par manuālu procesu. Informāciju par specifiskajiem soļiem, lai iespējotu šo līdzekli, skatiet Iespējot [budžeta priekšlikumus](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Finance Insights līdzekļu izmantošana

### <a name="using-customer-payment-predictions"></a>Debitora maksājumu prognožu izmantošana

- Lai uzzinātu, kā debitora maksājumu prognozes var sniegt informāciju, kas ir nepieciešama proaktīvi sākt kolekcijas aktivitātes, skatiet Sadaļā [Debitora maksājuma prognozēšana](use-customer-payment-predictions.md).
- Lai iegūtu informāciju, kas var palīdzēt novērtēt prognozēšanas modeļa efektivitāti pēc tam, kad esat sācis izmantot līdzekli, skatiet sadaļu [Sākotnējā debitora maksājuma prognozēšanas modeļa izvērtēšana](evaluate-payment-prediction.md).
- Lai iegūtu informāciju, kas var palīdzēt koriģēt datus, kuri tiek izmantoti prognozēšanas izveidei, un tādējādi var palīdzēt uzlabot tās efektivitāti, skatiet sadaļu [Prognozēšanas modeļa uzlabošana](improve-model.md).
- Lai uzzinātu vairāk par AI prognozēšanas modeļu rezultātiem, skatiet sadaļu [Algoritmiskās mācīšanās modeļu rezultāti](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Naudas plūsmas prognožu izmantošana

Naudas plūsmas prognozēšanas spēja var palīdzēt precīzāk novērtēt jūsu finansiālo situāciju. Intelligent naudas plūsmas prognozēšana ir veidota, pamatojoties uz dynamics 365 Finanšu esošo naudas plūsmas prognozēšanas funkcionalitāti. Lai pārskatītu esošo iespēju, skatiet sadaļu [Skaidras naudas plūsmas prognozēšana](../cash-bank-management/cash-flow-forecasting.md).

- Lai uzzinātu par jaunajām iespējām naudas plūsmas prognozēs, skatiet naudas [plūsmas prognozi](cash-flow-forecast-intro.md).
- Lai iegūtu informāciju par ārējo datu importēšanu, lai iekļautu tos savā naudas plūsmas prognozē, skatiet sadaļu [Ārēju datu izmantošana naudas plūsmas prognozēs](external-data-in-cash-flow.md). 
- Informāciju par to, kā izmantot mākslīgā intelekta modeli, lai projicētu naudas plūsmu tuvākajā laikā, skatiet sadaļu [Finansiālais stāvoklis](cash-position.md).
- Lai iegūtu informāciju par naudas plūsmas pozīciju un naudas plūsmas prognožu saglabāšanu momentuzņēmumos, kā arī lai salīdzinātu momentuzņēmumus ar faktiskajiem datiem, skatiet sadaļu [Momentuzņēmumu apskats](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budžeta priekšlikuma izmantošana

Informāciju par budžeta izveides paātrināšanu skatiet sadaļā [Budžeta priekšlikumi](budget-proposals.md). 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
