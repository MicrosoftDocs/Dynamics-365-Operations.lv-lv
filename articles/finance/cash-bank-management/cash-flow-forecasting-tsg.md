---
title: Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā
description: Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā. Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 39860a1960706aae7d223c8d2e810d39edc41b11deb80026925e6655f8e23ee8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747183"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā. Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Kādēļ naudas plūsma tiek rādīta tikai vienai juridiskajai personai?

Naudas plūsmas prognozēšana tiek konfigurēta un aprēķināta katrai juridiskajai personai. Power BI pārskati un naudas plūsmas prognožu spēja rāda rezultātus sadaļā Finance insights.

Naudas plūsmas prognozēšana jāiestata katrai juridiskajai personai, kurai vēlaties skatīt prognozi. Pārskatiet naudas plūsmas prognozes konfigurāciju visās juridiskajās personas. Alternatīvi pārskatiet visu juridisko personu konfigurāciju naudas plūsmas prognozēšanai un pārliecinieties, ka tās ir iestatītas tā, kā paredzēts.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Kādēļ Power BI netiek rādīti visi naudas plūsmas dati?

Pirms naudas plūsmas prognozes var parādīties Power BI skatījumos, ir jāveic vairāki soļi. Pārskatiet sekojošo kontrolsarakstu un pārliecinieties, ka katrs solis ir pabeigts:

- Iestatiet naudas plūsmu katrai juridiskajai personai.
- Virsgrāmatas parametros iestatiet sistēmas valūtu un sistēmas maiņas kursa tipu.
- Iestatiet Virsgrāmatas uzskaites valūtu un maiņas kursa tipu.
- Ievadiet maiņas kursus no darījuma valūtas uz uzskaites valūtu.
- Ievadiet maiņas kursus starp uzskaites valūtu un sistēmas valūtu.
- Ievadiet maiņas kursus starp uzskaites valūtu un katras bankas valūtu.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Kādēļ naudas plūsma Power BI darbojas iepriekšējās versijās, bet tagad ir tukša?

Pārbaudiet, vai Elementu krātuves mērījumi "Naudas plūsmas mērījums V2" un "LedgerCovLiquidityMeasurement" ir konfigurēti. Lai iegūtu papildinformāciju par to, kā strādāt ar datiem entītiju krātuvē, skatiet sadaļu [Power BI integrācija ar Elementu krātuvi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Pārbaudiet, vai ir pabeigtas visas darbības, kas nepieciešamas Power BI satura skatīšanai. Plašāku informāciju skatiet sadaļā [Skaidras naudas pārskata Power BI saturs](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Vai Elementu krātuves elementi ir atsvaidzināti?

Periodiski jāatsvaidzina elementi, lai nodrošinātu, ka dati ir pašreizējie un precīzi. Lai manuāli atsvaidzinātu noteiktu elementu, pārejiet uz sadaļu **Sistēmas administrēšana \> Iestatīšanas \> Elementu krātuve** atlasiet elementu un pēc tam atlasiet **Atsvaidzināt**. Datus var atjaunināt arī automātiski. Lapā **Elementu krātuve** iestatiet opciju **Automātiskā atsvaidzināšana iespējota** uz **Jā**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Kuru aprēķinu metodi lietot, aprēķinot naudas plūsmas prognozes?

Naudas plūsmas prognozes aprēķina metodei ir divas svarīgas atlases opcijas. Opcija **Jauns** aprēķinās naudas plūsmas prognozes jaunajiem dokumentiem un dokumentiem, kas ir mainījušies kopš pēdējā pakešuzdevuma izpildes. Šī opcija darbojas ātrāk, jo apstrādā mazāku dokumentu apakškopu. Opcija **Kopsumma** pārrēķinās naudas plūsmas prognozes katram dokumentam sistēmā. Šīs opcijas pabeigšanai nepieciešams vairāk laika, jo tai ir vairāk darba.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Kā uzlabot naudas plūsmas prognozēšanas periodiskā pakešuzdevuma veiktspēju?

veikt naudas plūsmas prognozi vienu reizi dienā ārpusslodzes stundu laikā, izmantojot aprēķina metodi **Jauns**. Ieteicams izmantot šo pieeju sešas dienas nedēļā. Pēc tam vienu reizi nedēļā palaidiet naudas plūsmas prognozi, izmantojot aprēķina metodi **Kopējais** dienā ar vismazāko aktivitātes daudzumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

