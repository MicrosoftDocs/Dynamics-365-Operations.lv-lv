---
title: Darba grupas kalendāra izveide
description: Skatiet un izveidojiet darba grupas kalendārus sadaļā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ee39f35f9d81f47c5438ddf48451d24ab0c0ed3
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065256"
---
# <a name="view-team-and-company-calendars"></a>Skatīt grupas un uzņēmuma kalendārus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Programmā Dynamics 365 Human Resources varat skatīt darba grupas un uzņēmuma kalendārus. Darba grupu kalendāri rāda tiešos pārskatus, kā noteikts rindu hierarhijā.

## <a name="view-your-team-calendar-as-an-employee"></a>Skatīt savas grupas kalendāru kā darbinieks

- **Darbinieku pašapkalpošanās** darbvietā atlasiet **Grupas kavējuma kalendāru** sadaļā **Kopsavilkums**.

## <a name="view-your-team-calendar-as-a-manager"></a>Skatīt savas grupas kalendāru kā pārvaldnieks

1. Darbvietā **Nodarbinātā patstāvīgi izmantojamie pakalpojumi** atlasiet **Mana komanda**.

2. Atlasiet **Atvaļinājums un prombūtne** un pēc tam atlasiet **Skatīt pārvaldnieka prombūtnes kalendāru**.

Pārvaldnieki var piekļūt arī grupas kalendāram no sadaļām **Manas komandas gaidošie prombūtnes pieprasījumi**, **Apstiprinātām brīvdienām** un **Brīvdienu pieprasījumi**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Skatīt prombūtnes pārvaldnieka kalendāru kā prombūtnes pārvaldnieks

> [!NOTE]
> Lai skatītu prombūtnes pārvaldnieka kalendāru, vispirms ir jāieslēdz līdzekli **(Priekšskatījums) prombūtnes pārvaldnieks, lai pārvaldītu atvaļinājumu** Līdzekļu pārvaldībā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

Prombūtnes pārvaldnieka lomas lietotāji kalendārā var skatīt brīvā laika pieprasījumus. Lai piekļūtu atvaļinājuma kalendāram, rīkojieties šādi.

1. Darbtelpā **Darbinieku pašapkalpošanās** atlasiet **Atvaļinājumu pārvaldība** un **Prombūtnes pārvaldnieka kalendārs**.

2. Laukā **Datums** ievadiet vajadzīgos datumus.

3. Pēc vajadzības atjauniniet skata opcijas.

Prombūtnes pārvaldnieku kalendārs rāda visus ierakstus par darbiniekiem, kuri sniedz pārskatu prombūtnes pārvaldniekam atvaļinājumu hierarhijā.

## <a name="view-a-company-calendar"></a>Uzņēmuma kalendāra skatīšana

Personas, kurām ir personāla vadības loma, var skatīt uzņēmuma kalendārus. Uzņēmuma kalendāri parāda visus darbiniekus. Pēc noklusējuma kalendārs rāda šodienas datumu plus 28 dienas, bet varat mainīt datumu diapazonu. Kalendāru var ar filtrēt pēc **Nosaukuma**, **Personāla numura** un **Atvaļinājuma veida**.

1. **Atvaļinājumu un prombūtnes** darbvietā atlasiet cilni **Saites**.

2. Atlasiet **Atvaļinājuma un prombūtnes kalendārs**.

Personāla vadības lomas var piekļūt arī uzņēmuma kalendāram no **Atvaļinājuma un prombūtnes pieprasījumiem**, **Apstiprinātām brīvdienām** un **Brīvdienu pieprasījumiem**. 

Kalendāros tagad ir papildu filtri un opcijas. Visos kalendāros ir skatījuma opcijas:

- Apstiprinātie pieprasījumi
- Gaidošie pieprasījumi
- Darbinieki ar atvaļinājumu pieprasījumiem
- Darbinieki bez atvaļinājumu pieprasījumu
- Darbinieku dzimšanas dienas
- Prombūtnes pieprasījumus 
- Atvaļinājuma pieprasījumi

Kalendāra konfigurācija lapā **Atvaļinājumu un prombūtnes parametri** nosaka pieejamās skatīšanas opcijas.

Kalendārus var filtrēt arī pēc vadītāja vai nodaļas. Primārā pozīcijas piešķire nosaka darbiniekus, kas tiek rādīti, kad šie filtri ir iestatīti. 

> [!IMPORTANT]
> Jūs varat ieslēgt līdzekli **Starpuzņēmumu atvaļinājumu skats** Līdzekļu pārvaldībā. Pēc tam iespējojiet līdzekli lapā **Personāla vadības koplietotajos parametros**, lai rādītu juridisko personu filtru kalendāros. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes parametru konfigurēšana](hr-leave-and-absence-parameters.md).
> 
> Kalendāru var filtrēt pēc juridiskās personas. Lai skatītu visus darbiniekus neatkarīgi no juridiskās personas, nodzēsiet filtru lauku un pēc tam atlasiet **Ievadīt**. 

Lai iegūtu informāciju par kalendāra iestatījumiem, skatiet [Kalendāra parametru konfigurēšana](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
