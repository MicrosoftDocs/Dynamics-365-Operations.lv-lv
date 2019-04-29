---
title: Talent klients atvienojas
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitors tiek atvienots no vides un nav zināms, kāpēc.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "859924"
---
# <a name="talent-client-disconnects"></a>Talent klients atvienojas

[!include [banner](includes/banner.md)]

**Informācija par vidi** 

Šāda problēma var rasties visās vidēs.
 
**Simptoms** 

Debitors tiek atvienots no vides un nav zināms, kāpēc. Debitors saņem vienu no šādiem kļūdu ziņojumiem:

- Savienojums tika zaudēts. Nokl. uz Aizv., lai turp. darbu.
- Šķiet, ka ir zaudēts savienojums ar tīklu; lai mēģinātu vēlreiz, noklikšķiniet uz Mēģināt vēlreiz.

**Sarkans karodziņš**

Šī problēma parasti rodas, ja lietotāji ir ieviešanas posmā, salīdzina informāciju ražošanas un testēšanas vidēs un aizmirst, ka tie pārslēdzas starp sesijām. Ja lietotāji ir šajā posmā, viņiem, visticamāk, rodas šī problēmu.

**Izejas plūsma** 

**Pārlūkprogrammu veidi:** Google Chrome, Internet Explorer un Microsoft Edge

Lietotāji tiek atvienoti no platformas Microsoft Dynamics 365 for Talent, ja vienlaicīgi ir atvērtas divas dažādas sesijas ar vienu un to pašu lietotāju un vienu un to pašu pārlūkprogrammas veidu. (Piemēram, lietotājs A skata gan 1. vidi, gan 2. vidi pārlūkprogrammā Chrome.) Nav svarīgi, vai lietotāji atver citus pārlūkprogrammas logus vai dažādas cilnes. Ja tiek izmantoti tie paši lietotāja akreditāc. dati, lai vienlaicīgi pierakstītos gan 1. vidē, gan 2. vidē tajā pašā pārlūkprogrammas tipā, Talent atvieno vienu no sesijām.

**Risinājums**

Pārliec., ka vienlaicīgi ir atvērta tikai viena vide konkrētam pārlūkpr. tipam. Lietotāji var atvērt vairākas sesijas tajā pašā vidē (t.i., vairākas cilnes tajā pašā pārlūkprogr.).

Lietotājiem, kuri vienlaicīgi vēlas pārvietoties starp divām vidēm, ir jāatver katra vide, izmantojot citu pārlūkpr. tipu. (Piemēram, lietotājs A var skatīt 1. vidi pārlūkprogrammā Chrome un 2. vidi pārlūkprogrammā Microsoft Edge.)
