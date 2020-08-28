---
title: Procesu automatizācija
description: Šī tēma sniedz detalizētu informāciju par to, kā procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690050"
---
# <a name="process-automation"></a>Procesu automatizācija

[!include[banner](../includes/banner.md)]

Procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris. Ieplānotā darba atjauninātais kalendāra skats ļauj lietotājiem skatīt un rīkoties ar plānoto un pabeigto darbu.

## <a name="administration"></a>Administrācija

Centrālā administrēšanas lapa visu procesu automatizācijām ir atrodama Sistēmas administrēšanas modulī, kas atrodas izvēlnē **Iestatījumi**. Šajā lapā tiks uzskaitīti visi automatizētie procesi (sērijas), kas ir iestatīti sistēmā. Tas arī ļaus jums pievienot jaunu procesu automatizācijas tieši no šīs lapas. Pēc sērijas iestatīšanas varat pārvaldīt katru šī saraksta sēriju. Varat izvēlēties rediģēt visu sēriju, dzēst to, skatīt visus gadījumus saraksta skatā vai atspējot sēriju, ja vēlaties pauzēt plānoto darbu laika periodā. 

Visi procesi, kas ir atspējoti funkciju pārvaldīšanā, netiks rādīti, kad līdzeklis ir atspējots. Turklāt procesu automatizācijas plānošanas programma neplāno nekādus gadījumus vai fona procesus atspējotam līdzeklim. No jauna iespējojot šo līdzekli, visi ieplānotie gadījumi vai fona procesi pagātnē tiek nekavējoties palaisti.

## <a name="calendar-view"></a>Kalendāra skats 
Viens no procesa automatizācijas galvenajiem ieguvumiem ir iespēja redzēt plānoto darbu vienkāršā kalendāra skatā.  Šis skats ļauj jums skatīt darbu nedēļas laikā. Šis skats tiks rādīts **Procesa automatizācijas** lapas labajā pusē. Tas tiks aizpildīts ar atlasītās sērijas ieplānoto darbu. 

[![Procesu automatizācijas kalendārs](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Gadījumu izmaiņas
Katru gadījumu var modificēt, neietekmējot ar tām izveidoto sēriju definētos citus gadījumus. Ieplānotā darba gadījumus var rediģēt no kalendāra skata, atlasot pogu **Skatīt/rediģēt** un atlasot **Gadījums**. Tas ļauj jums piekļūt visiem iestatījumiem, kas sākotnēji tika parādīti sēriju iestatīšanas vednī, un sniedz iespēju atlasītajam gadījumam veikt vienreizējas izmaiņas. Ieplānotā darba gadījumu var izslēgt arī, atlasot pogu **Atspējot** no kalendāra skata. 

## <a name="developer-documentation"></a>Izstrādātāja dokumentācija 
Izstrādātāja dokumentācija pašlaik tiek rakstīta, lai izstrādātājiem ļautu paplašināt procesu automatizācijas struktūru. Šī dokumentācija sniegs informāciju par to, kā varat izveidot pielāgotus procesus, kas ir nepieciešami, lai palaistu pakešu serveris, kas paredzēts procesu automatizācijas vednim, un automātiski tiek rādīti kalendāra skatā.
