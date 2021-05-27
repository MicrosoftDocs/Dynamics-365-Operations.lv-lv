---
title: Debitora atvienošanās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors tiek atvienots no vides un nav zināms, kāpēc.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db0e8efec1a5a6f01c9b7c4d9334a959fc42886b
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027991"
---
# <a name="client-disconnects"></a>Klienta atvienošanās

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

Lietotāji tiek atvienoti no Microsoft Dynamics 365 Human Resources, ja vienlaicīgi ir atvērtas divas dažādas sesijas ar vienu un to pašu lietotāju un vienu un to pašu pārlūkprogrammas veidu. (Piemēram, lietotājs A skata gan 1. vidi, gan 2. vidi pārlūkprogrammā Chrome.) Nav svarīgi, vai lietotāji atver citus pārlūkprogrammas logus vai dažādas cilnes. Ja tiek izmantoti tie paši lietotāja akreditācijas dati, lai vienlaicīgi pierakstītos gan 1. vidē, gan 2. vidē un tā paša veida pārlūkprogrammā, Human Resources atvieno vienu no sesijām.

**Risinājums**

Pārliec., ka vienlaicīgi ir atvērta tikai viena vide konkrētam pārlūkpr. tipam. Lietotāji var atvērt vairākas sesijas tajā pašā vidē (t.i., vairākas cilnes tajā pašā pārlūkprogr.).

Lietotājiem, kuri vienlaicīgi vēlas pārvietoties starp divām vidēm, ir jāatver katra vide, izmantojot citu pārlūkpr. tipu. (Piemēram, lietotājs A var skatīt 1. vidi pārlūkprogrammā Chrome un 2. vidi pārlūkprogrammā Microsoft Edge.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]