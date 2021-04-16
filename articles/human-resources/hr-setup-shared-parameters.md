---
title: Konfigurēt koplietotos parametrus
description: Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: abcaf42a2e8b227e2c7c1b07ed61ea005832667a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802387"
---
# <a name="configure-shared-parameters"></a>Konfigurēt koplietotos parametrus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.

Uzņēmumi koplieto dažu veidu ierakstus, piemēram, amatu ierakstus. Šiem ierakstiem ir jāiestata koplietojamie parametri. Piemēram, lapu **Personāla vadības kopīgie parametri** var izmantot, lai iestatītu Personāla vadības parametrus juridiskām personām. 

Lapā **Personāla vadības kopīgie parametri** parametri tiek grupēti apgabalos, pamatojoties uz to funkcionalitāti. 

### <a name="previously-released-functionality"></a>Iepriekš izlaistā funkcionalitāte
Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus. Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju. Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**. Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **cilne Saites** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**. Var ievadīt vienkāršu kodu un aprakstu. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Ja lietojat programmu Dynamics 365 Human Resources
Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus. Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju. Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**. Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**. Var ievadīt vienkāršu kodu un aprakstu. 

Cilnē **Numuru sērijas** var atlasīt numuru sērijas, kas tiek izmantotas šiem ierakstiem: Personāla numurs, Amats, Lietotāja pieprasījuma ID, I-9 dokuments, Kandidāts, Diskusija, Atvieglojumu ID un Personāla darbība (ja ir aktivizēts šis ieraksta tips). Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas**. Lai atrastu šo lapu, lietojiet lapu meklēšanas funkciju. 

Cilnē **Amati** norādiet, vai jauni amati ir pieejami piešķiršanai pēc noklusējuma:

-   **Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī. Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.
-   **Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī. Ja šī opcija ir atlasīta, kļūstot pieejamam katram jaunam amatam būs jāatver forma **Amats** un pēc tam cilnē **Vispārīgi** jāievada datums **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri.


[!INCLUDE[footer-include](../includes/footer-banner.md)]