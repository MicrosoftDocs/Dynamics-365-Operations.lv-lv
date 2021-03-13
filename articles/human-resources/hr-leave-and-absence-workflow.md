---
title: Atvaļinājuma pieprasījuma darbplūsmas izveide
description: Izveidojiet atvaļinājumu un prombūtnes pieprasījumu darbplūsmu, lai konsekventi pārvaldītu atvaļinājumu pieprasījumus sistēmā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1907ca9cc578737341e52f89453e3d6ae3d0bec
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115056"
---
# <a name="create-a-leave-request-workflow"></a>Atvaļinājuma pieprasījuma darbplūsmas izveide

Varat sistēmā Dynamics 365 Human Resources izveidot darbplūsmu, lai konsekventi pārvaldītu savus atvaļinājuma un prombūtnes pieprasījumus. **Atvaļinājumu un prombūtnes** darbplūsma ļauj:

- Definēt uzdevumus
- Noteikt, kam ir jāpabeidz uzdevumi
- Norādīt, kurš var apstiprināt vai noraidīt pieprasījumus

## <a name="create-a-leave-and-absence-request-workflow"></a>Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas izveide

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.

3. Atlasiet **Jauna** un pēc tam atlasiet **Atvaļinājuma un prombūtnes pieprasījums**. 

4. Kad parādās ziņojuma lodziņš **Vai atvērt šo failu?**, atlasiet **Atvērt** un piesakieties ar sava uzņēmuma akreditācijas datiem.

5. Izmantojiet darbplūsmas redaktoru, lai izveidotu jūsu atvaļinājuma pieprasījumu darbplūsmu. Lai iegūtu vairāk informācijas par darbu ar darbplūsmām, skatiet [Darbplūsmas apskatu izveide](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas datu elementi

Jūs varat izmantot tālāk norādītos datu elementus, lai izveidotu nosacījuma vai automātiskus apstiprinājumus darbplūsmās atvaļinājumu un kavējumu pieprasījumiem:

- **Daudzums**
- **Komentārs**
- **Uzņēmums**
- **Izveidots**
- **Izveidotais datums un laiks**
- **Beigu datums**
- **Atvaļinājuma tips**
- **Labojis**
- **Modificēšanas datums un laiks**
- **Iemeslu kodi**
- **Pieprasījuma ID**
- **Sākuma datums**
- **Statuss** 
- **Iesniegšanas datums**
- **Iesniedza**
- **Iesniedza personāla vadības nodaļa**
- **Iesniedza vadītājs**
- **Iesniegts vārdā**
- **Darbinieks**
- **Nodarbinātā veids**

Šie piemēri parāda, kā var izveidot dažādus darbplūsmas nosacījumu veidus, izmantojot šos datu elementus:

- Izmantojiet **Pamatojuma kodu** nosacījuma pārskatā, lai maršrutētu slimības atvaļinājuma pieprasījumus ar iemesla kodu **Ķirurģija** uz PV apstiprināšanai, bet visus pārējos pamatojuma kodus pāradresētu vadītājam. Papildinformāciju par nosacījuma priekšrakstiem skatiet [Konfigurēt nosacījuma lēmumus darbplūsmā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- Izmantojiet **Iesniedza personāla vadības nodaļa** un **Iesniedza vadītājs**, lai automātiski apstiprinātu atvaļinājumu pieprasījumus, ko šīs lomas iesniedz darbinieku vārdā. Plašāku informāciju par šīm automātiskajām darbībām skatiet [Konfigurēt apstiprināšanas procesus darbplūsmā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Izmantojiet **Atvaļinājuma veidu** nosacījuma pārskatā vai automātiskajās darbībās, lai kontrolētu, kā darbplūsma maršrutē pieprasījumus ar noteiktiem atvaļinājumu veidiem.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
