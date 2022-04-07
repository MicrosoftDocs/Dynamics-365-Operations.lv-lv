---
title: Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide
description: Izveidojiet atvaļinājumu pirkšanas un pārdošanas pieprasījumu darbplūsmu, lai konsekventi pārvaldītu pirkšanas un pārdošanas atvaļinājumu pieprasījumus sistēmā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f200fec48dc6bff2702b962c47cbd6951c5921c
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509421"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide


>[!Important]
>Šajā tēmā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem savrupā programmā Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat sistēmā Dynamics 365 Human Resources izveidot darbplūsmu, lai konsekventi pārvaldītu atvaļinājuma pirkšanas un pārdošanas pieprasījumus. **Atvaļinājuma pirkšanas un pārdošanas** darbplūsma ļauj:

- Definēt uzdevumus
- Noteikt, kam ir jāpabeidz uzdevumi
- Norādīt, kurš var apstiprināt vai noraidīt pieprasījumus

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.

3. Atlasiet **Jauns** un pēc tam atlasiet **Atvaļinājuma pirkšanas un pārdošanas pieprasījums**. 

4. Kad parādās ziņojuma lodziņš **Vai atvērt šo failu?**, atlasiet **Atvērt** un piesakieties ar sava uzņēmuma akreditācijas datiem.

5. Izmantojiet darbplūsmas redaktoru, lai izveidotu jūsu atvaļinājuma pieprasījumu darbplūsmu. Lai iegūtu vairāk informācijas par darbu ar darbplūsmām, skatiet [Darbplūsmas apskatu izveide](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas datu elementi

Jūs varat izmantot tālāk norādītos datu elementus, lai izveidotu nosacījuma vai automātiskus apstiprinājumus darbplūsmās atvaļinājumu pirkšanas un pārdošanas pieprasījumiem:

- **Daudzums**
- **Atvaļinājuma iegādes un pārdošanas politika**
- **Uzņēmums**
- **Izveidots**
- **Izveidošanas datums un laiks**
- **Beigu datums**
- **Atvaļinājuma veids**
- **Modificēja:**
- **Modificēšanas datums un laiks**
- **Pieprasījuma ID**
- **Sākuma datums**
- **Statuss** 
- **Iesniegšanas datums**
- **Iesniedza**
- **Iesniedza personāla vadības nodaļa**
- **Iesniedza vadītājs**
- **Iesniegts vārdā**
- **Darbinieks**

## <a name="workflow-examples"></a>Darbplūsmas piemēri

Šie piemēri parāda, kā var izveidot dažādus darbplūsmas nosacījumu veidus, izmantojot šos datu elementus:

- Izmantojiet **Iesniedza personāla vadības nodaļa** un **Iesniedza vadītājs**, lai automātiski apstiprinātu atvaļinājumu pirkšanas un pārdošanas pieprasījumus, ko šīs lomas iesniedz darbinieku vārdā. Plašāku informāciju par šīm automātiskajām darbībām skatiet [Konfigurēt apstiprināšanas procesus darbplūsmā](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Izmantojiet **Atvaļinājuma veidu** nosacījuma pārskatā vai automātiskajās darbībās, lai kontrolētu, kā darbplūsma maršrutē pieprasījumus ar noteiktiem atvaļinājumu veidiem.

## <a name="see-also"></a>Skatiet arī

[Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)<br>
[Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
