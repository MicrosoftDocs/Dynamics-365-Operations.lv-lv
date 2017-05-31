---
title: "PV parametru iestatīšana juridiskām personām"
description: "Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f93d548adc4ae81eb89ac7c01cdae79d20b763aa
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>PV parametru iestatīšana juridiskām personām

[!include[banner](includes/banner.md)]


Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.

Uzņēmumi koplieto dažu veidu ierakstus, piemēram, amatu ierakstus. Šiem ierakstiem ir jāiestata koplietojamie parametri. Piemēram, lapu **Personāla vadības kopīgie parametri** var izmantot, lai iestatītu Personāla vadības parametrus juridiskām personām. 

Lapā **Personāla vadības kopīgie parametri** parametri tiek grupēti apgabalos, pamatojoties uz to funkcionalitāti. 

Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus. Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju. Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**. Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**. Var ievadīt vienkāršu kodu un aprakstu. 

Cilnē **Numuru sērijas** var atlasīt numuru sērijas, kas tiek izmantotas šiem ierakstiem: Personāla numurs, Amats, Lietotāja pieprasījuma ID, I-9 dokuments, Kandidāts, Diskusija, Atvieglojumu ID un Personāla darbība (ja ir aktivizēts šis ieraksta tips). Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas**. Lai atrastu šo lapu, lietojiet lapu meklēšanas funkciju. 

Cilnē **Amati** norādiet, vai jauni amati ir pieejami piešķiršanai pēc noklusējuma:

-   **Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī. Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.
-   **Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī. Ja šī opcija ir atlasīta, kļūstot pieejamam katram jaunam amatam būs jāatver forma **Amats** un pēc tam cilnē **Vispārīgi** jāievada datums **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri.


<a name="see-also"></a>Skatiet arī
--------

[Uzņēmumam raksturīgo PV parametru iestatīšana](set-up-company-specific-hr-parameters.md)




