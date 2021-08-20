---
title: Iestatīt meitasuzņēmuma juridisko personu konsolidācijai
description: Šajā tēmā paskaidrots, kā strādāt ar kontu plānu uzņēmum konsolidācijai.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: fbec5ad8fa5e17b75859c07ee64a66c9568c97d3d18b6a7616a64303d3a33f10
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727963"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Iestatīt meitasuzņēmuma juridisko personu konsolidācijai

[!include [banner](../includes/banner.md)]

Metode, ko izmantojat, lai sagatavotu meitasuzņēmuma kontus konsolidācijai, daļēji ir atkarīgs no tā, kādā mērā kontu plāna struktūra meitasuzņēmuma juridiskajā personā atspoguļo kontu plānu konsolidētajā juridiskajā personā.

Pirms sākat konsolidāciju kā daļu no perioda slēgšanas, veiciet perioda slēgšanas sagatavošanās darbus, bet neslēdziet meitasuzņēmuma kontus, līdz konsolidācija ir pabeigta. Papildinformāciju par perioda beigu slēgšanu skatiet šeit: [Slēgt virsgrāmatu perioda beigās](close-general-ledger-at-period-end.md) un [Slēgt finanšu gadu](tasks/close-fiscal-year.md).

> [!NOTE]
>  Ieteicams izmantot Management Reporter programmai Microsoft Dynamics 365 Finance, lai apvienotu finanšu rezultātus vairākām juridiskām personām konsolidētā formātā. Management Reporter ļauj izveidot konsolidētus finanšu pārskatus starp juridiskajām personām, izmantot Excel, lai importētu konsolidēšanas datus no citiem avotiem, un pārvērst summas jebkurā pārskatu valūtā bez vajadzības veikt konsolidācijas procesu Dynamics 365 Finance.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Kartēt meitasuzņēmuma galvenos kontus konsolidētajos galvenajos kontos

Ja kontu plāns meitasuzņēmuma juridiskajā personā neatbilst kontu plānam konsolidētajā juridiskajā personā, varat kartēt galvenos kontus meitasuzņēmumā uz galvenajiem kontiem konsolidētajā juridiskajā personā.

1. Sadaļā *meitasuzņēmums* dodieties uz **Virsgrāmata \>Iestatīšana** \> **Kontu plāns \> Kontu plāns**.
2. Atlasiet kontu plānu. Kopsavilkuma cilnē **Galvenie konti** atlasiet galveno kontu un pēc tam atlasiet **Rediģēt**.
3. Atlasiet katru meitasuzņēmuma galveno kontu, kas ir jākartē uz konsolidēto galveno kontu. Kopsavilkuma cilnas **Vispārīgi** laukā **Konsolidācijas konts** ievadiet konsolidētās juridiskās personas kontu, uz kuru jāpārsūta atlasītā meitasuzņēmuma galvenā konta bilance vai darījumi. Varat ievadīt to pašu konsolidēto galveno kontu vairākiem meitasuzņēmuma kontiem.

    > [!NOTE]
    > Ja meitasuzņēmumu kartēto kontu galveno kontu veidi atšķiras no konsolidētās juridiskās personas kontu galveno kontu veidiem, kontu vērtības, kuru galvenā konta veids ir **Kopsumma**, konsolidācijas laikā tiek pārrakstītas.

4. Sagatavojiet ziņojumus un finanšu pārskatus konsolidētajai juridiskajai personai, kas balstītas uz finanšu dimensijām. Izpildiet zemāk norādītās darbības, lai kartētu finanšu dimensijas, kas tiek izmantotas meitasuzņēmuma kontos konsolidētās juridiskās personas finanšu dimensijām:

    1. Sadaļā *meitasuzņēmuma juridiskā persona* dodieties uz **Virsgrāmata \> Iestatīšana \> Finanšu dimensijas \> Finanšu dimensijas**, atlasiet finanšu dimensiju un pēc atlasiet **Finanšu dimensijas vērtības**.
    2. Atlasiet finanšu dimensijas vērtību, ko kartēt uz citu finanšu dimensijas vērtību konsolidētajā juridiskajā personā.
    3. Kopsavilkuma cilnes **Vispārīgi** laukā **Grupas dimensija** ievadiet finanšu dimensiju konsolidētajā juridiskajā personā. Konsolidācijas laikā šī finanšu dimensija tiks piešķirta darījumiem un bilancēm, kas lieto atlasīto finanšu dimensiju meitasuzņēmuma juridiskajā personā. Finanšu dimensijas, kuras šeit ievadāt, jāizmanto konsolidētajā juridiskajā personā. Varat piešķirt finanšu dimensiju, ko izmanto kā grupas finanšu dimensiju vairākām meitasuzņēmuma finanšu dimensijām.

5. Ja konsolidēšanu veicat tiešsaistē, izpildiet tālāk minētās darbības, lai nodrošinātu, ka pārsūtīšanas notiek, kā esat paredzējis.

    1. Sadaļā *konsolidētā juridiskā persona* dodieties uz **Virsgrāmata \> Periodiski \> Konsolidēt \> Konsolidēt \[Eksportēt uz\]**, lai atvērtu lapu **Konsolidēt \[Tiešsaistē\]**.
    2. Cilnē **Kritēriji** atlasiet izvēles rūtiņu **Izmantot konsolidācijas kontu**.
    3. Cilnē **Finanšu dimensijas** atlasiet atbilstošās finanšu dimensijas.
    4. Katrai finanšu dimensijai, ko atlasāt, ievadiet numuru laukā **Segmentu secība**, lai norādītu secību, kādā tiek parādītas dimensijas.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Saglabājiet vienu kontu diagrammu gan meitasuzņēmumā, gan konsolidētajā juridiskajā personā

Galvenajiem kontiem meitasuzņēmuma juridiskajā personā varētu būt tādi paši kontu numuri un tā pati kontu diagrammas struktūra kā galvenajiem kontiem konsolidētajā juridiskajā personā. Šajā gadījumā jums nav manuāli jākartē meitasuzņēmuma galvenie konti uz galvenajiem kontiem konsolidētajā juridiskajā personā.

Pirms sākat konsolidāciju, izpzildiet tālāk norādītās darbības.

1. Sadaļā *konsolidētā juridiskā persona* dodieties uz **Virsgrāmata \> Periodiski \> Konsolidēt \> Konsolidēt \[Eksportēt uz\]**, lai atvērtu lapu **Konsolidēt \[Tiešsaistē\]**.
2. Atzīmējiet izvēles rūtiņu **Izmantot konsolidācijas kontu**. Konsolidācijas laikā darījumi un bilances tiks automātiski pārsūtītas uz pareizo kontu.

> [!NOTE]
> Ja kont neatbilst, konsolidācija tiek apturēta un jūs saņemat ziņojumu.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Izveidot kontu diagrammu konsolidētajai juridiskajai personai, pamatojoties uz esošo kontu diagrammu

Konsolidāciju varat veikt pat tad, ja ir kontu diagramma konsolidētajā juridiskajā personā jau ir izveidota.

- Ja ir ieplānota konta struktūra, ko vēlaties izmantot konsolidētajā juridiskajā personā, varat kartēt meitasuzņēmumu kontus uz šo struktūru.
- Ja nekartējat meitasuzņēmuma kontus, konsolidētās juridiskās personas konti tiek izveidoti automātiski, tiklīdz meitasuzņēmuma dati tiek pārsūtīti uz konsolidēto juridisko personu. Šie konti ir balstīti uz galveno kontu. Turpmākos datus uzkrāj kontos konsolidētajā juridiskajā personā, kam ir tāds pats konta numurs kā meitasuzņēmuma kontos.

Neatkarīgi no tā, vai konti ir kartēti, notīriet izvēles rūtiņu **Izmantot konsolidācijas kontu** lapā **Konsolidēt** konsolidētajā juridiskajā personā, pirms jūs darbināt šāda veida konsolidāciju.

> [!NOTE]
> Šo metodi iespējams izmantot kontu diagrammas izveidošanai konsolidētajā juridiskajā personā no kādas meitasuzņēmuma juridiskās personas kontu diagrammas. (Plašāku informāciju skatiet [Konsolidācijas kontu grupas un papildu konsolidācijas konti](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Pēc tam piešķiriet atbilstošu konsolidācijas konversijas principu katram konsolidētam galvenajam kontam un izpildiet konsolidāciju visām meitasuzņēmuma juridiskajām personām.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]