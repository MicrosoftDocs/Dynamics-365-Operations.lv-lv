---
title: Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas
description: Varat ļaut darbiniekiem pirkt un pārdot atvaļinājumu Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429017"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas

[!include [banner](includes/preview-feature.md)]

Varat nodrošināt, ka darbinieki var nopirkt atvaļinājumu, izveidojot atvaļinājuma pirkšanas politiku.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Ļaujiet darbiniekiem pirkt un pārdot atvaļinājumu

1. Lapā **Atvaļinājumu un prombūtnes parametri** atlasiet **Jā** opcijai **Ļaut darbiniekiem pirkt atvaļinājumu**. 

## <a name="create-a-buy-leave-policy"></a>Atvaļinājuma pirkšanas izveide

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**. 

2. Atlasiet **Atvaļinājuma pirkšanas un pārdošanas politika**.

3. Atlasiet **Jauns**.

4. Ievadiet politikai **Nosaukums** un **Apraksts** sadaļā **Atvaļinājuma pirkšanas un pārdošanas politika**. 

5. Atlasiet **Politikas veids**. 

   Pieejamie politikas veidi ir **Summa** un **Stundas nedēļā**. Atlasiet **Summa**, lai ievadītu **Fiksētā summa** maksimālajai summai, par kuru darbinieki var pirkt un pārdot. Atlasot **Stundas nedēļā**, darba laiks, kas noteikts darbiniekam piešķirtajā darba laika kalendārā, tiek izmantots, lai noteiktu maksimālo politikas summu. 

6. Atlasiet politikai **Sākuma datums** and **Beigu datums**. Pieprasījumi pirkt vai pārdot atvaļinājumu būs pieejami iesniegšanai tikai šajā laika posmā. 

7. Sadaļā **Pirkšanas politika** atlasiet **Pilna laika ekvivalents** (FTE), lai proporcionāli pārvērtētu maksimālo summu, pamatojoties uz darbinieka amatā noteikto FTE. Ja politikas veids ir **Summa**, ievadiet **Maksimālā fiksētā summa**. 

8. Atlasiet **Pievienot**, lai pievienotu atvaļinājuma veidus darbiniekiem, kuri iegādājas atvaļinājumu. Politikai var pievienot vairākus atvaļinājuma veidus. 

9. Lai noteiktu maksimālo summu, ko darbinieks var nopirkt, ievadiet **Nodarbinātības mēnešu skaits** atvaļinājuma veidu, kas ļauj definēt dažādu nodarbinātības mēnešu skaitu. 

10. Ievadiet **Maksimālā summa** atvaļinājuma veidam. 

11. Ievadiet **Kurss**, pie kāda darbinieks nopirks atvaļinājumu. 

12. Pēc izvēles ievadiet **Pelnīšanas kods**, kas jāizmanto atvaļinājuma pirkšanai. 

13. Pēc izvēles iestatiet, vai lietot FTE, lai noteiktu atvaļinājuma veida maksimālo summu. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Atvaļinājuma pirkšanas un pārdošanas politikas pievienošana atvaļinājuma un prombūtnes plānam

1. Lapā **Atvaļinājums un prombūtne** atlasiet atvaļinājumu un prombūtnes plānu.

2. Sadaļā **Noteikumi** select **Atvaļinājuma pirkšanas un pārdošanas politika**.

## <a name="see-also"></a>Skatiet arī

[Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)</br>
[Konfigurēt atvaļinājumu un kavējumu veidus](hr-leave-and-absence-types.md)</br>
[Uzkrāt atvaļinājumu un kavējumu plānus](hr-leave-and-absence-accrue.md)</br>
[Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)

