---
title: Ražošanas plūsmas versijas izveide
description: Šī procedūra ir vērsta uz to, lai izveidotu jaunu ražošanas plūsmas versiju.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b57dbd2516a25b414193ca76367bd8d5c4a1b298
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255065"
---
# <a name="create-a-production-flow-version"></a>Ražošanas plūsmas versijas izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra ir vērsta uz to, lai izveidotu jaunu ražošanas plūsmas versiju. Lai veiktu šo procedūru, ir jādefinē lean manufacturing ražošanas uzdevuma parametrus un klases laika mērvienības. Jums arī ir nepieciešams definēt vērtību plūsmu un ražošanas uzdevumu grupu. Lai uzzinātu vairāk par lean manufacturing ražošanas plūsmām un darbībām, skatiet tehniskos dokumentus par Lean manufacturing programmai Microsoft Dynamics AX. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-production-flow"></a>Ražošanas plūsmas izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet pārvaldības struktūrvienību ar tipu vērtību plūsma. Vērtību plūsma ir pārvaldības struktūrvienība, kas aptver visas vērtību plūsmas darbības un plūsmas. Šajā posmā pārvaldības struktūrvienības ir ierobežotas ar juridisku personu un tām nav papildu funkcionalitātes.  
7. Laukā Ražošanas uzdevumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet ražošanas plūsmai ražošanas uzdevumu grupu. Ražošanas uzdevumu grupas ļauj definēt materiālu, darbaspēku un NP kontu ražošanas procesam. Lai saistītu uzskaites kontekstu ar ražošanas plūsmu, ir jāatlasa ražošanas uzdevumu grupa.  
9. Noklikšķiniet uz Saglabāt.

## <a name="create-a-production-flow-version"></a>Ražošanas plūsmas versijas izveide
1. Noklikšķiniet uz Pievienot.
2. Laukā Beigu datums ievadiet datumu un laiku.
    * Ja nepieciešams, nosakiet versijas beigu datumu. To var atjaunināt jebkurā brīdī, pat aktīvām versijām. To var izmantot, lai plānotu versijas izslēgšanu.  
3. Noklikšķiniet uz OK.
4. Sarakstā atzīmējiet atlasīto rindu.
5. Laukā Mērvienība ierakstiet vērtību.
6. Atrisināt maina izgatavošanas vienību.
7. Laukā Vidējais izgatavošanas laiks ievadiet skaitli.
    * Nosakiet versijas vidējo izgatavošanas laiku. Ražošanas plūsmas versijas izgatavošanas kontrolei definējiet mērķtiecīgo vidējo izgatavošanas laiku. Izgatavošana ir definēta kā daudzums noteiktā laika periodā. Piemēram, izgatavošanas laiks ir 0,2 stundas uz 10 gabaliem. 8 stundu darba laikā tas atbilst dienas caurlaides jaudai 400 gabali.  
8. Laukā Daudzums vienā ciklā ievadiet skaitli.
    * Definējiet daudzumu vienā ciklā, kas saistīts ar vidējo izgatavošanas laiku.  
9. Pārslēdziet sadaļas Detalizēta informācija par versiju paplašinājumu.
10. Laukā Minimālais izgatavošanas laiks ievadiet skaitli.
    * Nosakiet minimālo izgatavošanas laiku. Minimālajam izgatavošanas laikam jābūt mazākam par vai vienādam ar vidējo izgatavošanas laiku.  
11. Laukā Maksimālais izgatavošanas laiks ievadiet skaitli.
    * Maksimālajam izgatavošanas laikam jābūt augstākam par vai vienādam ar vidējo izgatavošanas laiku.  
12. Laukā Faktiskā cikla laika periods (dienas) ievadiet skaitli.
    * Ievadiet Faktiskā cikla laika perioda dienu skaitu. Faktiskā cikla laika periods ir dienu skaits, kuru laikā darbi tiek apkopoti no faktiskās minūtes atpakaļ, lai aprēķinātu faktisko cikla laiku. Vērtību var mainīt jebkurā brīdī un tā tiek izmantota tikai faktisko cikla laiku aprēķināšanai.  
13. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]