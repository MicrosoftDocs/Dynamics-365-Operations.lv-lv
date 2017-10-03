--- 
title: "Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai"
description: "Šajā procedūrā ir parādīts, kā iestatīt vienumu izvēlnē Mobilā ierīce."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7ce132b590fffb753948e663763b8f3ef576ac36
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā iestatīt vienumu izvēlnē Mobilā ierīce. Šajā piemērā izvēlnes vienums tiek lietots, lai veiktu darbu ar tipu Pirkšanas pasūtījums. Ar izvēlnes vienumu saistītā darba klase nosaka, kurš darbs ir derīgs. Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Parasti šo procedūru izpilda noliktavas pārvaldnieks.


## <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide
1. Dodieties uz sadaļu Mobilās ierīces izvēlnes vienumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.
    * Ievadiet unikālu vērtību. Varat ierakstīt, piemēram, POMove. Atcerieties šo vērtību, jums tā vēlāk būs nepieciešama.  
4. Laukā Virsraksts ierakstiet kādu vērtību.
    * Tas ir nosaukums, kas tiks rādīts mobilajā ierīcē. Varat ierakstīt, piemēram, PO pārvietošana.  
5. Laukā Režīms atlasiet "Darbs".
6. Laukā Izmantot esošo darbu atlasiet Jā.
    * Šis mobilās ierīces izvēlnes elements tiek izmantots, lai veiktu esošu darbu. Tādēļ šī vērtība jums ir jāiestata uz Jā.  
    * Lauks Rādīt krājumu statusu nosaka, vai noliktavas darbiniekam mobilajā ierīcē tiks parādīts rīcībā esošo krājumu statuss.  
7. Laukā Novirzītājs atlasiet vienumu Sistēmas grupēšana.
    * Kad kaut ko atlasāt laukā Novirzītājs, šīs lapas sadaļā Vispārīgi kļūst redzami papildu lauki. Rādītie lauki ir atkarīgi no jūsu veiktās atlases. Kad atlasāt Sistēmas grupēšana, tiek pievienoti divi jauni lauki. Tie ir paskaidroti tālāk.  
8. Laukā Sistēmas grupēšana atlasiet “WorkPoolId”.
    * Kad noliktavas darbinieki atver šo izvēlnes elementu, viņiem tiek lūgts skenēt darbu kopas ID. Visi darbu pasūtījumi ar šo darbu kopas ID un atvērtām darbu pasūtījuma rindām, kurās šim izvēlnes elementam ir pievienota viena no darbu klasēm, tiks padoti lietotājam.  
9. Laukā Sistēmas grupēšanas etiķete ierakstiet vērtību.
    * Šis ir teksts, kas tiek rādīts lietotājam mobilajā ierīcē. Varat ierakstīt, piemēram, Darbu kopa.  
10. Laukā Ignorēt noliktavas vienību izvietojot atlasiet Jā.
    * Šī opcija noliktavas darbiniekiem ļauj ignorēt mērķa noliktavas vienības numura zīmi, kad krājumi tiek izvietoti no numura zīmes atkarīgā novietojumā.  
11. Laukā Grupēt izvietošanu atlasiet Jā.
    * Ja visiem darbu pasūtījumiem izvietošanas rindās ir tas pats novietojums, tad lietotājs saņems vienu kombinētu izvietošanas instrukciju visām rindām.  
    * Audita veidnes ID: darba audita veidne jums ļauj norādīt, ka darba process kādam izvēlnes elementam ir jāpārtrauc, lai varētu izpildīt citu operāciju. Piemēram, ja šis izvēlnes elements ir paredzēts ienākošam darbam, tad audita veidnē var tikt pieprasīts, lai darbinieks pārbaudītu temperatūru. Procesa pārtraukšanas brīdis ir norādīts audita veidnē un tas var būt, piemēram, brīdis, kad darbs tiek sākts vai pabeigts, vai brīdis, kad tiek mainīts darba statuss.  
12. Izvērsiet sadaļu Darba klases.
13. Noklikšķiniet uz Jauns.
14. Laukā Darba klases ID ierakstiet “Pirkšana”.
    * Darbu veidne ierobežo darbu, kam šo izvēlnes elementu var izmantot. Šajā gadījumā tā tiks izmantota atvērtajām darbu pasūtījuma rindām, kam ir pirkšanas darba klases ID.  
15. Noklikšķiniet uz Saglabāt.

## <a name="set-up-work-confirmation"></a>Darba apstiprinājuma iestatīšana
1. Noklikšķiniet uz vienuma Darba apstiprinājuma iestatīšana.
2. Laukā Darba tips atlasiet vienumu “Izdošana”.
3. Atzīmējiet izvēles rūtiņu Automātiskā apstiprināšana.
    * Darba instrukcija ar darba tipu Izdošana tiks apstiprināta automātiski. Šī instrukcija netiks parādīta lietotājam.  
4. Noklikšķiniet uz Jauns.
5. Laukā Darba tips atlasiet vienumu “Izvietošana”.
6. Atzīmējiet izvēles rūtiņu Novietojuma apstiprināšana.
    * Kad krājums tiek nolikts, noliktavas darbiniekam tiek lūgts izpildīt novietojuma apstiprinājuma skenēšanu.  
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.
9. Aizvērt lapu.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Izvēlnes elementa pievienošana mobilās ierīces izvēlnei
1. Dodieties uz sadaļu Mobilās ierīces izvēlne.
2. Noklikšķiniet uz Rediģēt.
3. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "ienākošs".
    * Jūs vēlaties atrast izvēlni, kuru izmantojat ienākošajiem izvēlnes elementiem. Uzņēmumā USMF tā tiek saukta par Ienākošais.  
4. Kokā atlasiet "vērtība".
5. Noklikšķiniet uz bultiņas, kas rāda pa labi.
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.


