---
title: Prognozes, darba pasūtījumi un projekti
description: Šajā tēmā tiek paskaidrotas prognozes un darba pasūtījuma integrācija ar Projektu pārvaldību un uzskaites moduli modulī Līdzekļu pārvaldība.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bf211e9f256a7489cdc3c38ed2d2198bd1dd6789
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813825"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognozes, darba pasūtījumi un projekti

[!include [banner](../../includes/banner.md)]

 

Modulī Līdzekļu pārvaldība integrācija ar **Projektu pārvaldību un uzskaites** moduli palīdz izmaksu kontroles optimizācijai, ļaujot lietotājiem izsekot izmaksas par uzturēšanas darba tipa prognozēm un darba pasūtījumu uzdevumiem.

Lai izsekotu uzturēšanas darba tipa prognozes, ir neieciešami divi iestatījumi:

1. Atlasiet projektu **Pamatlīdzekļu pārvaldība** > **Iestatīšana** > **Pamatlīdzekļu pārvaldības parametri** un pēc tam cilnē **Līdzekļi** > **Projekts** kopsavilkuma cilnē, **Uzturēšanas prognozes projekta** laukā atlasiet projektu.

2. Veidojot uzturēšanas darba tipa noklusējuma rindu, automātiski tiek izveidots darbības numurs **Uzturēšanas darba tipa noklusējumi** lapai, (**Līdzekļu pārvaldība** > **Iestatīšana** > **Uzdevumi** > **Uzturēšanas darba tipa noklusējumi**).

Uzturēšanas darba tipa prognozes kalpo diviem mērķiem: 

- Jūs varat izsekot izmaksām par apkopes darba tipa prognozēm **Projektu vadības un uzskaites** modulī. 
- Prognozes tiek automātiski pārceltas darba pasūtījuma uzdevuma projektā, izvēloties uzturēšanas darba tipu darba pasūtījuma uzdevumu.

Lai izsekotu izmaksas par darba pasūtījumu uzdevumiem, sākumā jums ir jāiestata darba pasūtījumu projekti. Plašāku informāciju skatiet sadaļā [Darba pasūtījumu projekta iestatīšana](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Darba pasūtījumu uzdevumu projekti

Veidojot darba pasūtījuma uzdevumu, darba pasūtījuma projektu nosaka pamatprojekta iestatīšana darba pasūtījumiem sadaļā **Darba pasūtījumu projekta iestatīšana** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**).

Darba pasūtījuma uzdevumu projektus veido, izmantojot šādas darba pasūtījuma informācijas kombināciju:

- Darba pasūtījumam ir atlasīts darba pasūtījuma tips. 
- Funkcionālais novietojums atbilst līdzeklim darba pasūtījuma uzdevumā
- Līdzeklim atbilstošs Līdzekļa tips darba pasūtījuma uzdevumā  
- Darba pasūtījumā iestatītais paredzamais sākuma un beigu laiks.  

Daļa no šīs informācijas var nebūt atrodama darba pasūtījumā. Tādēļ darba pasūtījuma pamatprojekta meklēšana tiek veikta, izmantojot pieejamo datu kombināciju un atlasot projekta ID, kas atbilst darba pasūtījuma datiem.

Piemēram, sekojošajā ilustrācijā, ņemot vērā to, ka ir iestatīts **Kravas automašīnas programmas** līdzekļa tips, katrs darba pasūtījuma uzdevums, kas tiek izveidots ar **Kravas automašīnas programmas** līdzekļa tipu, būs projekta ID 000186 apakšprojekts.

![1. attēls](media/01-integration-to-pma.png)

Projekta ID, kas ir paredzēts darba pasūtījuma uzdevumā, un saistītā aktivitātes numura mērķis, ir izsekot izmaksas, kas ir saistītas ar darba pasūtījuma uzdevumu un līdzekli, kas tam atlasīts **Projekta vadības un uzskaites** modulī. (Lai skatītu projekta ID un aktivitātes numuru, atlasiet **Pamatlīdzekļu pārvaldība** > **Kopīgie** > **Darba pasūtījumi** > **Visi darba pasūtījumi** un pēc tam atlasiet darba pasūtījumu. **Rindas detaļas** kopsavilkuma cilnē lauks **Projekta ID** rāda projekta ID, un **Aktivitātes numurs** lauks rāda aktivitātes numuru.) Lai iegūtu vairāk informācijas par izmaksu kontroli Pamatlīdzekļu pārvaldībā, skatiet [Izmaksu un datumu kontrole](../controlling-and-reporting/cost-and-date-control.md).

Sekojošā ilustrācija rāda grafisku pārskatu par darba pasūtījumu projektiem un atbilstošām projektu aktivitātēm.

![2. attēls](media/02-integration-to-pma.png)

Darba pasūtījumā veidojot jaunu darba pasūtījuma uzdevumu, automātiski uzdevumam tiek izveidots darba pasūtījuma projekts. Finanšu dimensijas līdzeklim, kas atbilst darba pasūtījuma uzdevumam, automātiski tiek pārceltas uz darba pasūtījuma projektu.

Projekta aktivitāte, kas izveidota darba pasūtījuma uzdevumam, ir tam pievienota saistīta informācija. Šī informācija ir par uzturēšanas darba tipu, uzturēšanas darba tipa variantu un tirdzniecību. Tie ir noderīgi, ja, piemēram, no darba pasūtījuma izveidojat pirkšanas pasūtījumu (skatiet [Sagāde](../work-orders/procurement.md)) vai izmantojat moduli **Projektu pārvaldība un uzskaite** laika reģistrācijai.

Ja līdzeklis tika instalēts funkcionālajā novietojumā, bet vēlāk tiek instalēts citā funkcionālajā novietojumā, finanšu dimensijas, kas atbilst jaunajam funkcionālajam novietojumam, tiek automātiski atjaunināti līdzeklī. Pēc tam, veidojot darba pasūtījuma uzdevumu līdzeklim, darba pasūtījuma projekts darba pasūtījuma uzdevumam automātiski iegūs finanšu dimensijas, kas tagad atbilst līdzeklim. Tādēļ, kad izmantojat funkcionālos novietojumus, izmaksas vienmēr var tikt izsekotas funkcionālajos novietojumos, kuros līdzeklis ticis instalēts jebkurā noteiktajā laikā. Finanšu dimensiju automātiskā atjaunināšana palīdz nodrošināt pilnīgu izmaksu izsekojamību projekta kontrolei un pārskatu veidošanai.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Darba pasūtījumu projekti, darba pasūtījumu dzīves cikla stāvokļi, projekta posmi un projektu tipi

Lai palīdzētu nodrošināt pareizu darba pasūtījumu dzīves cikla stāvokļu izmantošanu un atbilstošus projekta posmus darba pasūtījumiem, ņemiet vērā atkarības attiecībā uz moduli **Projektu pārvaldība un uzskaite**:

- Modulī **Projektu pārvaldība un uzskaite** projektu posmi iestatīti projektu veidiem sadaļā **Projektu pārvaldības un uzskaites parametri**.  
- Sadaļā **Projektu pārvaldības un uzskaites parametri** izmantojiet atbilstošā projekta posma izvēles rūtiņas visiem projektu tipiem, kurus izmantosiet. Tālāk redzamajās ilustrācijās pieci posmi (**Izveidots**, **Novērtēts**, **Ieplānots**, **Procesā** un **Pabeigts**) tika atlasīti projektu tipiem **Laiks un materiāls** un **Iekšējais**. Šie pieci posmi atbilst gan iekšējiem uzturēšanas darbiem, gan pakalpojumu uzturēšanas darbiem.
- **Līdzekļu pārvaldības** modulī projektu veidi ir definēti projekta grupās, kas iestatītas **Darba pasūtījuma projekta iestatīšanas** lapā > **Projektu grupa** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**).  
- Projektu grupas, kas tiek iestatītas sadaļā **Darba pasūtījuma projekta iestatīšana**, izmanto, veidojot darba pasūtījumus. Izveidojot darba pasūtījumu, darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.  
- Katram darba pasūtījuma dzīves cikla stāvoklim ir atbilstošs projekta posms.  
- Projekta posms, kas atbilst darba pasūtījuma dzīves cikla stāvoklim, ir jādefinē kā aktīvs posms projekta grupai, kas ir noteikts darba pasūtījuma projektā. Darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.
- Veidojot jaunu darba pasūtījumu, darba pasūtījuma projekta automātiskā piešķiršana balstās uz iestatīšanu sadaļā **Darba pasūtījuma projekta iestatīšana**.  

Sekojošās ilustrācijas parāda saistības starp darba pasūtījumu projektu grupām, atbilstošajiem projektu tipiem, projektu posmiem un darba pasūtījumu dzīves cikla stāvokļiem.

![3. attēls](media/03-integration-to-pma.png)

![4. attēls](media/04-integration-to-pma.png)

![5. attēls](media/05-integration-to-pma.png)

Papildinformāciju par darba pasūtījumu veidu iestatīšanu skatiet sadaļā [Darba pasūtījumu projektu iestatīšana](../setup-for-work-orders/work-order-project-setup.md). Lai iegūtu vairāk informācijas par to, kā izveidot darba pasūtījumu dzīves cikla stāvokļus, skatiet sadaļu [Darba pasūtījuma dzīves cikla stāvokļi](../setup-for-work-orders/work-order-lifecycle-states.md).

Sekojošajā ilustrācijā redzams grafisks pārskats par dažādiem projektiem, kas izveidoti **Līdzekļu pārvaldības** modulī, lai iespējotu integrāciju ar **Projektu vadības un uzskaites** moduli. Tas arī rāda darba procesus, ar kuriem projekti ir saistīti.

![6. attēls](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]