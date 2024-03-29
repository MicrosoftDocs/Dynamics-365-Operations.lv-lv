---
title: Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas
description: Varat ļaut darbiniekiem pirkt un pārdot atvaļinājumu Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9db86f2a482e7a1c1eee854958cb3f097d6baf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888822"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Atvaļinājuma iegādes un pārdošanas politiku pārvaldība

>[!Important]
>Šajā rakstā atzīmētā funkcionalitāte pašlaik ir pieejama klientiem atsevišķi Dynamics 365 Human Resources. Daļa vai visa funkcionalitāte būs pieejama kā daļa no nākamā laidiena Finance infrastruktūrā pēc Finance laidiena 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat nodrošināt, ka darbinieki var nopirkt un pārdot atvaļinājumu, izveidojot atvaļinājuma pirkšanas un pārdošanas politiku. Šīs politikas var konfigurēt, lai izmantotu darbplūsmu apstiprinājumiem, iestatīt maksimālās summas un likmes un iestatīt likmes pirkšanai un pārdošanai. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Ļaujiet darbiniekiem pirkt un pārdot atvaļinājumu

1. Lapā **Atvaļinājumu un prombūtnes parametri** atlasiet **Jā** opcijai **Ļaut darbiniekiem pirkt atvaļinājumu** un **Ļaut darbiniekiem pārdot atvaļinājumu**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Atvaļinājuma iegādes un pārdošanas politikas izveide

1. Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**. 

2. Atlasiet **Atvaļinājuma pirkšanas un pārdošanas politika**.

3. Atlasiet **Jauns**.

4. Ievadiet politikai **Nosaukums** un **Apraksts** sadaļā **Atvaļinājuma pirkšanas un pārdošanas politika**. 

5. Atlasiet **Politikas veids**. 

   Pieejamie politikas veidi ir **Summa** un **Stundas nedēļā**. Atlasiet **Summa**, lai ievadītu **Fiksētā summa** maksimālajai summai, par kuru darbinieki var pirkt un pārdot. Atlasot **Stundas nedēļā**, darba laiks, kas noteikts darbiniekam piešķirtajā darba laika kalendārā, tiek izmantots, lai noteiktu maksimālo politikas summu. 

6. Atlasiet politikai **Sākuma datums** and **Beigu datums**. Pieprasījumi pirkt vai pārdot atvaļinājumu būs pieejami iesniegšanai tikai šajā laika posmā. 

7. Atlasiet **Darbplūsmas ID** politikai. Visi pirkšanas un pārdošanas pieprasījumi izmantos šo darbplūsmu pārskatīšanai un apstiprināšanai. 

8. Sadaļā **Pirkšanas politika** atlasiet **Pilna laika ekvivalents** (FTE), lai proporcionāli pārvērtētu maksimālo summu, pamatojoties uz darbinieka amatā noteikto FTE. Ja politikas veids ir **Summa**, ievadiet **Maksimālā fiksētā summa**. 

9. Atlasiet **Pievienot**, lai pievienotu atvaļinājuma veidus darbiniekiem, kuri iegādājas atvaļinājumu. Politikai var pievienot vairākus atvaļinājuma veidus. 

10. Lai noteiktu maksimālo summu, ko darbinieks var nopirkt, ievadiet **Nodarbinātības mēnešu skaits** atvaļinājuma veidu, kas ļauj definēt dažādu nodarbinātības mēnešu skaitu. 

11. Ievadiet **Maksimālā summa** atvaļinājuma veidam. 

12. Ievadiet **Kurss**, pie kāda darbinieks nopirks atvaļinājumu. 

13. Pēc izvēles ievadiet **Pelnīšanas kods**, kas jāizmanto atvaļinājuma pirkšanai. 

14. Pēc izvēles iestatiet, vai lietot FTE, lai noteiktu atvaļinājuma veida maksimālo summu. 

15. Lai izveidotu pārdošanas politiku, izpildiet no 8. līdz 14. solim sadaļā **Pārdošanas politika**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Atvaļinājuma pirkšanas un pārdošanas politikas pievienošana atvaļinājuma un prombūtnes plānam

1. Lapā **Atvaļinājums un prombūtne** atlasiet atvaļinājumu un prombūtnes plānu.

2. Sadaļā **Noteikumi** select **Atvaļinājuma pirkšanas un pārdošanas politika**.

## <a name="see-also"></a>Skatiet arī

[Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)</br>
[Konfigurēt atvaļinājumu un kavējumu veidus](hr-leave-and-absence-types.md)</br>
[Uzkrāt atvaļinājumu un kavējumu plānus](hr-leave-and-absence-accrue.md)</br>
[Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
