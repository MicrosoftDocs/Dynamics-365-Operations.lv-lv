---
title: Atvaļinājuma pieprasījuma darbplūsmas izveide
description: Izveidojiet atvaļinājumu un prombūtnes pieprasījumu darbplūsmu, lai konsekventi pārvaldītu atvaļinājumu pieprasījumus sistēmā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855091"
---
# <a name="create-a-leave-request-workflow"></a>Atvaļinājuma pieprasījuma darbplūsmas izveide

> [!Important]
> Šajā rakstā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem atsevišķi Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat sistēmā Dynamics 365 Human Resources izveidot darbplūsmu, lai konsekventi pārvaldītu savus atvaļinājuma un prombūtnes pieprasījumus. **Atvaļinājumu un prombūtnes** darbplūsma ļauj:

- Definēt uzdevumus
- Noteikt, kam ir jāpabeidz uzdevumi
- Norādīt, kurš var apstiprināt vai noraidīt pieprasījumus

## <a name="create-a-leave-and-absence-request-workflow"></a>Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas izveide

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.

3. Atlasiet **Jauna** un pēc tam atlasiet **Atvaļinājuma un prombūtnes pieprasījums**. 

4. Kad parādās ziņojuma lodziņš **Vai atvērt šo failu?**, atlasiet **Atvērt** un piesakieties ar sava uzņēmuma akreditācijas datiem.

5. Izmantojiet darbplūsmas redaktoru, lai izveidotu jūsu atvaļinājuma pieprasījumu darbplūsmu. Lai iegūtu vairāk informācijas par darbu ar darbplūsmām, skatiet [Darbplūsmas apskatu izveide](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

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

- Izmantojiet **Pamatojuma kodu** nosacījuma pārskatā, lai maršrutētu slimības atvaļinājuma pieprasījumus ar iemesla kodu **Ķirurģija** uz PV apstiprināšanai, bet visus pārējos pamatojuma kodus pāradresētu vadītājam. Papildinformāciju par nosacījuma priekšrakstiem skatiet [Konfigurēt nosacījuma lēmumus darbplūsmā](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Izmantojiet **Iesniedza personāla vadības nodaļa** un **Iesniedza vadītājs**, lai automātiski apstiprinātu atvaļinājumu pieprasījumus, ko šīs lomas iesniedz darbinieku vārdā. Plašāku informāciju par šīm automātiskajām darbībām skatiet [Konfigurēt apstiprināšanas procesus darbplūsmā](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Izmantojiet **Atvaļinājuma veidu** nosacījuma pārskatā vai automātiskajās darbībās, lai kontrolētu, kā darbplūsma maršrutē pieprasījumus ar noteiktiem atvaļinājumu veidiem.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
