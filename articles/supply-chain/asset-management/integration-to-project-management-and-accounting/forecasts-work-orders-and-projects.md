---
title: Prognozes, darba pasūtījumi un projekti
description: Šajā tēmā tiek paskaidrotas prognozes un darba pasūtījuma integrācija ar Projektu pārvaldību un uzskaites moduli modulī Līdzekļu pārvaldība.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886820"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognozes, darba pasūtījumi un projekti

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Modulī Līdzekļu pārvaldība tiek veikta integrācija ar **Projektu pārvaldību un uzskaites** moduli izmaksu kontroles optimizācijai, ļaujot lietotājiem izsekot izmaksas par uzturēšanas darba tipa prognozēm un darba pasūtījumu uzdevumiem.

Lai izsekotu uzturēšanas darba tipa prognozes, ir jāveic divi iestatījumi:

1. Atlasiet projektu sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu pārvaldības parametri** >  saite **Līdzekļi** > **Projekts** FastTab > lauks **Uzturēšanas prognozes projekts**.

2. Sadaļā **Uzturēšanas darba tipa noklusējumi**, veidojot uzturēšanas darba tipa noklusējuma rindu, rindai automātiski tiek izveidots darbības numurs (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbi** > **Uzturēšanas darba tipa noklusējumi**).

Uzturēšanas darba tipa prognozes kalpo diviem mērķiem: varat izsekot izmaksas par uzturēšanas darba tipa prognozēm modulī **Projektu pārvaldība un uzskaite**. Turklāt prognozes tiek automātiski pārceltas darba pasūtījuma uzdevuma projektā, izvēloties uzturēšanas darba tipu darba pasūtījuma uzdevumam.

Lai izsekotu izmaksas par darba pasūtījumu uzdevumiem, sākumā jums ir jāiestata darba pasūtījumu projekti. Procedūras aprakstam skatiet rakstu [Darba pasūtījuma projekta iestatīšana](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Darba pasūtījumu uzdevumu projekti

Veidojot darba pasūtījuma uzdevumu darba pasūtījumam, darba pasūtījuma projektu nosaka pamatprojekta iestatīšana darba pasūtījumiem sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**.

Darba pasūtījuma uzdevumu projektus veido, izmantojot šādas darba pasūtījuma informācijas kombināciju:

- Darba pasūtījumam ir atlasīts tips Darba pasūtījums 
- Funkcionālais novietojums atbilst līdzeklim darba pasūtījuma uzdevumā
- Līdzeklim atbilstošs Līdzekļa tips darba pasūtījuma uzdevumā  
- Darba pasūtījumā iestatītais Paredzamais sākuma un beigu laiks.  

Iespējams, ne visa iepriekš minētā informācija ir atrodama darba pasūtījumā. Tādēļ darba pasūtījuma pamatprojekta meklēšana tiek veikta, izmantojot pieejamo datu kombināciju un atlasot projekta ID, kas atbilst darba pasūtījuma datiem.

Piemērs. Tālāk redzamajā ilustrācijā līdzekļa tipa iestatījums “Kravas automašīnu programma” nozīmē, ka katrs darba pasūtījuma uzdevums, kas izveidots, izmantojot šo līdzekļa tipu, būs Projekta ID “000186” apakšprojekts.

![1. attēls](media/01-integration-to-pma.png)

Projekta ID darba pasūtījuma uzdevumā un atbilstošās darbības numura mērķis (**Līdzekļu pārvaldība** > **Bieži lietotie** > **Darba pasūtījumi** > **Visi darba pasūtījumi** > sarakstā atlasiet darba pasūtījumu > **Rindas informācija** FastTab > lauks **Projekta ID** un lauks **Darbības numurs**) ir modulī **Projektu pārvaldība un uzskaite** izsekot izmaksas, kas saistītas ar darba pasūtījuma uzdevumu un atlasīto līdzekli darba pasūtījuma uzdevumā. 

Tālāk redzamajā ilustrācijā varat redzēt grafisku pārskatu par darba pasūtījumu projektiem un atbilstošām projektu aktivitātēm.

![2. attēls](media/02-integration-to-pma.png)

Darba pasūtījumā veidojot jaunu darba pasūtījuma uzdevumu, automātiski uzdevumam tiek izveidots darba pasūtījuma projekts. Finanšu dimensijas līdzeklim, kas atbilst darba pasūtījuma uzdevumam, automātiski tiek pārceltas uz darba pasūtījuma projektu. Projekta darbībai, kas izveidota darba pasūtījuma uzdevumam, ir atbilstoša tai pievienotā informācija par uzturēšanas darba tipu, uzturēšanas darba tipa variantu un tirdzniecību. Šie dati ir noderīgi, ja, piemēram, no darba pasūtījuma izveidojat pirkšanas pasūtījumu (skatiet [Sagāde](../work-orders/procurement.md)) vai izmantojat moduli **Projektu pārvaldība un uzskaite** laika reģistrācijai.  

Ja līdzeklis tika instalēts funkcionālajā novietojumā un šis līdzeklis vēlāk tiek instalēts citā funkcionālajā novietojumā, finanšu dimensijas, kas atbilst jaunajam funkcionālajam novietojumam tiek automātiski atjaunināti līdzeklim. Pēc tam, veidojot darba pasūtījuma uzdevumu līdzeklim, darba pasūtījuma projekts darba pasūtījuma uzdevumam automātiski iegūs finanšu dimensijas, kas tagad atbilst līdzeklim. Tas nozīmē, ka izmantojot funkcionālos novietojumus, vienmēr var izsekot izmaksas funkcionālajos novietojumos, kuros līdzeklis ticis instalēts jebkurā noteiktajā laikā. Finanšu dimensiju automātiskā atjaunināšana nodrošina pilnīgu izmaksu izsekojamību projekta kontrolēšanai un pārskatu veidošanai.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Darba pasūtījumu projekti, darba pasūtījumu dzīves cikla stāvokļi, projekta posmi un projektu tipi

Lai nodrošinātu pareizu darba pasūtījumu dzīves cikla stāvokļu izmantošanu un atbilstošus projekta posmus darba pasūtījumiem, ņemiet vērā atkarības attiecībā uz moduli **Projektu pārvaldība un uzskaite**:

- Modulī **Projektu pārvaldība un uzskaite** projektu posmi iestatīti projektu veidiem sadaļā **Projektu pārvaldības un uzskaites parametri**.  
- Sadaļā **Projektu pārvaldības un uzskaites parametri** neaizmirstiet atlasīt atbilstošā projekta posma izvēles rūtiņas visiem projektu tipiem, kurus plānojat izmantot. Tālāk redzamajā ilustrācijā pieci posmi **Izveidots** - **Novērtēts** - **Ieplānots** - **Procesā** - **Pabeigts** tika atlasīti projektu tipiem “Laiks un materiāls” un “Iekšējais”. Šie pieci posmi atbilst gan iekšējai uzturēšanai, gan pakalpojumu uzturēšanas darbiem.  
- Sadaļā **Līdzekļu pārvaldība** projektu tipi ir noteikti pēc projektu grupām, ko iestatāt veidlapā **Darba pasūtījuma projekta iestatīšana** > saite **Projekta grupa**.  
- Projektu grupu iestatīšana sadaļā **Darba pasūtījuma projekta iestatīšana** izmanto, veidojot darba pasūtījumus. Izveidojot darba pasūtījumu, darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.  
- Katram darba pasūtījuma dzīves cikla stāvoklim ir atbilstošs projekta posms.  
- Projekta posms, kas atbilst darba pasūtījuma dzīves cikla stāvoklim, ir jādefinē kā aktīvs posms projekta grupai, kas noteikta darba pasūtījuma projektā. Darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.  
- Veidojot jaunu darba pasūtījumu, darba pasūtījuma projekta automātiskā piešķiršana balstās uz iestatīšanu sadaļā **Darba pasūtījuma projekta iestatīšana** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbu pasūtījumi** > **Projektu iestatīšana**).  

Saistības starp darba pasūtījumu projektu grupām, atbilstošajiem projektu tipiem, projektu posmiem un darba pasūtījumu dzīves cikla stāvokļiem ir parādīti tālāk redzamajās ilustrācijās.  

![3. attēls](media/03-integration-to-pma.png)

![4. attēls](media/04-integration-to-pma.png)

![5. attēls](media/05-integration-to-pma.png)

Skatiet rakstu [Darba pasūtījuma projekta iestatīšana](../setup-for-work-orders/work-order-project-setup.md), kā iestatīt darba pasūtījumu projektus un [Darba pasūtījumu dzīves cikla stāvokļi ](../setup-for-work-orders/work-order-lifecycle-states.md) kā izveidot darba pasūtījumu dzīves cikla stāvokļus.

Tālāk redzamajā ilustrācijā ir sniegts grafisks pārskats par dažādiem projektiem, kas izveidoti modulī **Līdzekļu pārvaldība**, lai atļautu integrāciju ar moduli **Projektu vadība un uzskaite**, kā arī par darba procesiem, kuriem atbilst projekti.

![6. attēls](media/06-integration-to-pma.png)

