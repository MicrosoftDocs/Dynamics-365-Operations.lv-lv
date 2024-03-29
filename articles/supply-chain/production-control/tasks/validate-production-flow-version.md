---
title: Ražošanas plūsmas un versijas pārbaude
description: Šajā procedūrā tiek parādīts, kā izveidot Lean ražošanā jaunu ražošanas plūsmu un pirmo versiju.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d87aa427c2bc3868e255c97ea11fd4e79456eef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573589"
---
# <a name="validate-a-production-flow-and-version"></a>Ražošanas plūsmas un versijas pārbaude

[!include [banner](../../includes/banner.md)]

Šajā procedūrā tiek parādīts, kā izveidot Lean ražošanā jaunu ražošanas plūsmu un pirmo versiju. Priekšnosacījumi: ir jādefinē Lean ražošanas parametrus un klases laika mērvienības. Jums arī ir nepieciešams definēt Vērtību plūsmu un Ražošanas uzdevumu grupu. Skatiet tehniskos dokumentus par Lean ražošanas procesu, lai iepazītos ar ražošanas plūsmu un aktivitāšu koncepciju. Šī procedūra attiecas uz juridisko personu USMF demonstrācijas datos. Tomēr, pieņemot, ka juridiskā persona ir konfigurēta Lean ražošanas procesā, var izmantot citas juridiskas personas.


## <a name="create-a-production-flow"></a>Ražošanas plūsmas izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Lean ražošanas plūsma > Ražošanas plūsmas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Vērtību plūsma ir pārvaldības struktūrvienība, kas aptver visas vērtību plūsmas darbības un plūsmas.   Šajā posmā pārvaldības struktūrvienības ir ierobežotas ar juridisku personu un tām nav papildu funkcionalitātes.  
7. Laukā Ražošanas uzdevumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Ražošanas uzdevumu grupas ļauj definēt materiālu, darbaspēku un NP kontu ražošanas procesam. Lai saistītu uzskaites kontekstu ar ražošanas plūsmu, ir jāatlasa ražošanas uzdevumu grupa.  
9. Noklikšķiniet uz Saglabāt.

## <a name="create-a-production-flow-version"></a>Ražošanas plūsmas versijas izveide
1. Noklikšķiniet uz Pievienot.
2. Laukā Beigu datums ievadiet datumu un laiku.
    * Versijas Beigu datumu var atjaunināt jebkurā laikā, pat aktīvām versijām. Lietojiet versijas beigu datumu, lai plānotu versijas izslēgšanu.  
3. Noklikšķiniet uz OK.
4. Sarakstā atzīmējiet atlasīto rindu.
5. Laukā Mērvienība ierakstiet vērtību.
6. Atlasiet Izgatavošanas laika vienība.
7. Laukā Vidējais izgatavošanas laiks ievadiet skaitli.
    * Ražošanas plūsmas versijas izgatavošanas kontrolei definējiet mērķtiecīgo vidējo izgatavošanas laiku.   Izgatavošana ir definēta kā daudzums noteiktā laika periodā.  Šajā piemērā izgatavošanas laiks ir 0,2 stundas uz 10 gabaliem. 8 stundu darba laikā tas atbilst dienas caurlaides jaudai 400 gabali.  
8. Laukā Daudzums vienā ciklā ievadiet skaitli.
9. Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija par versiju.
10. Laukā Minimālais izgatavošanas laiks ievadiet skaitli.
    * Minimālajam izgatavošanas laikam jābūt mazākam par vai vienādam ar vidējo izgatavošanas laiku.  
11. Laukā Maksimālais izgatavošanas laiks ievadiet skaitli.
    * Maksimālajam izgatavošanas laikam jābūt augstākam par vai vienādam ar vidējo izgatavošanas laiku.  
12. Ievadiet Faktiskā cikla laika perioda dienu skaitu.
    * Faktiskā cikla laika periods ir dienu skaits, kuru laikā darbi tiek apkopoti no faktiskās minūtes atpakaļ, lai aprēķinātu faktisko cikla laiku. Vērtību var mainīt jebkurā brīdī un tā tiek izmantota tikai faktisko cikla laiku aprēķināšanai.  
13. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]