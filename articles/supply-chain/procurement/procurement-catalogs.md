---
title: Sagādes katalogu apskats
description: Šajā rakstā ir detalizēti aprakstīts, kā iepirkumu speciālisti var iestatīt un uzturēt sagādes katalogus. Sagādes katalogos ir noteikti krājumi un pakalpojumi, ko uzņēmuma darbinieki var pasūtīt iekšējai lietošanai.
author: mkirknel
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06713d4f1ca1fe1c3feafe314da3a155fa7cd126
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865308"
---
# <a name="procurement-catalogs-overview"></a>Sagādes katalogu apskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir detalizēti aprakstīts, kā iepirkumu speciālisti var iestatīt un uzturēt sagādes katalogus. Sagādes katalogos ir noteikti krājumi un pakalpojumi, ko uzņēmuma darbinieki var pasūtīt iekšējai lietošanai.

Iepirkumu speciālisti var izveidot un uzturēt krājumu katalogus un pakalpojumus, kas var tikt iegādāti uzņēmuma iekšējai lietošanai. Pēc katalogu iestatīšanas uzņēmuma darbinieki var izveidot pirkšanas pieprasījumus, lai veiktu pasūtījumus no tiem. Katalogus var izmantot, lai pastiprinātu pirkšanas politikas tā, lai darbinieki var pasūtīt tikai tos krājumus un pakalpojumus, kas atļauti atbilstoši pirkšanas juridiskajai personai. Izveidojot sagādes katalogu, jāveic tālāk norādītie uzdevumi.

-   Pirms izveidot katalogu, konfigurēt savu sagādes kategoriju hierarhiju.
-   Nosakiet, kuras preces darbinieki var pasūtīt. Varat rādīt vai paslēpt konkrētas kataloga mezglā ietvertās preces vai arī visas mezglā ietvertās preces.
-   Nosakiet nepieciešamo sagādes katalogu skaitu. Piekļuvi sagādes katalogam nosaka kataloga ierobežojuma nosacījumi, ko konfigurējat juridiskajai personai un pārvaldības struktūrvienībai, kurai piešķirts darbinieks.

Vairāki faktori nosaka preces, kuras darbinieki var pasūtīt, kā arī sagādes kategorijas, kuras tie var izmantot, izveidojot pirkšanas pieprasījumus.

-   Kategorijas piekļuves ierobežojuma nosacījumi pirkšanas politikā nosaka, kuras sagādes kategorijas ir pieejamas pirkšanas pieprasījumā. Ja nav definēts neviens nosacījums, ir pieejamas visas sagādes kategorijas.
-   Darbinieki var pasūtīt preci tikai tad, ja tā ir aktīvajā jūsu organizācijai paredzētajā sagādes katalogā un tad, ja tā ir iespējotajā mezglā un nav paslēpta. Precei ir jābūt arī kategorijā, kurai var piekļūt konkrēts darbinieks saskaņā ar kategorijas piekļuves ierobežojuma nosacījumiem.
-   Kataloga ierobežojuma nosacījumi norāda izmantoto katalogu. Ja nav definēts neviens kataloga ierobežojuma nosacījums, tikai kategorijas piekļuves nosacījumi nosaka preces, kuras darbinieki var pasūtīt pieprasījumā.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk esošajā tabulā ir aprakstīti uzdevumi, kās jāizpilda, pirms iepirkumu speciālists var izveidot sagādes katalogu.

| Uzdevums                                                | Loma               | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iestatiet sagādes kategoriju hierarhiju.            | Pirkšanas vadītājs | Sagādes kategoriju hierarhijas klasificē krājumus vai transakcijas pārskatiem un analīzei. Izmantojot sagādes kategoriju hierarhiju, uzņēmumi var stratēģiski pārvaldīt kategorijas, preces, piegādātājus un citus sagādes faktorus no centrālas vietas. Visai organizācijai tiek noteikta viena sagādes kategoriju hierarhija. Kataloga pamatā ir sagādes kategoriju hierarhija: kategorijas hierarhijā kļūst par mezgliem katalogā. Jūsu katalogā ir iekļauti kreditori un preces. |
| Pievienojiet sagādes kategorijām kreditorus un preces. | Pirkšanas vadītājs | Kad jūsu organizācijai ir izveidota sagādes kategoriju hierarhija, katru sagādes kategoriju var saistīt ar noteiktiem piegādātājiem, precēm u.c. Šīs saistības tiek automātiski iekopētas katalogā.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Kataloga iestatīšana
Pēc priekšnosacījumu izpildes varat iestatīt katalogus. Var izveidot vienu katalogu, ko izmanto visa organizācija vai vairākus katalogus, kas lieto dažādas nodaļas organizācijā. Ja izveidojat vienu katalogu visai organizācijai, piekļuvi katalogam uzraudzīs iepirkuma ierobežojuma nosacījumi.  

Katalogs nosaka, kuras preces ir pieejamas, veidojot pirkšanas pieprasījumu, taču kategorijas piekļuves politikas nosacījumus var izmantot, lai lietotu papildu ierobežojumus. Tā kā mezgli katalogā ir sagādes kategorijas, tos var ignorēt, izmantojot kategoriju piekļuves ierobežojumu nosacījumus. Šādā gadījumā šajā kategorijā ietvertās preces darbinieki nevar izmantot pieprasījumos. Kategorijas piekļuves ierobežojumu nosacījumus var definēt lapā **Pirkšanas ierobežojumi**. Tālāk esošajā tabulā aprakstīti uzdevumi, kas jāveic, lai iestatītu katalogu.

| Uzdevums                                                   | Loma             | Apraksts                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidojiet jaunu katalogu.                                  | Pirkšanas aģents | Veidojot katalogu, jānorāda kataloga nosaukums un apraksts. Varat arī definēt, vai katalogs jāatjaunina manuāli vai automātiski, un norādiet kataloga īpašnieku.                                                                                                                                      |
| Uzraugiet, vai preces ir pieejamas katalogā. | Pirkšanas aģents | Tā kā preces tiek mantotas no sagādes kategorijām, tās visas parādās atbilstošos kataloga mezglos. Varat kontrolēt, vai visas preces mezglā tiks paslēptas vai parādītas, izmantojot katalogu pirkšanas pieprasījumā Varat arī kontrolēt, vai atsevišķas preces mezglā tiks paslēptas vai parādītas. |
| Publicējiet katalogu.                                   | Pirkšanas aģents | Pirms katalogs ir pieejams darbiniekiem tā izmantošanai pieprasījumā, jums jādefinē kataloga ierobežojumu nosacījumi, kataloga statuss jāiestata uz **Aktīvs** un jāpublicē katalogs. Varat deaktivizēt katalogus, ko vēlaties padarīt nepieejamus lietotājiem.                                              |

Atjauninājumi tiek publicēti automātiski vai manuāli atkarībā no opcijas, ko atlasāt kataloga laukā **Noklusējuma atjaunināšanas tips**, lapā **Katalogi**. Katalogiem ir pieejami šādi noklusējuma atjaunināšanas tipi.

-   **Dinamisks** — katalogs tiek atjaunināts automātiski ikreiz, kad tas ir mainīts.
-   **Statisks** — katalogus ir jāatjaunina manuāli.
-   **Abi** — ja katalogs ietver preču kategorijas, kurām ir noklusējuma atjaunināšanas tips **Statisks**, tas jāatjaunina manuāli, atjauninot šīs kategorijas. Ja katalogs ietver preču kategorijas, kurām ir noklusējuma atjaunināšanas tips **Dinamisks**, tas tiek atjaunināts automātiski ikreiz, kad tas ir mainīts.


<a name="additional-resources"></a>Papildu resursi
--------

[Sagādes kategoriju hierarhijas iestatīšana (uzdevuma ceļvedis)](tasks/set-up-procurement-category-hierarchy.md)



