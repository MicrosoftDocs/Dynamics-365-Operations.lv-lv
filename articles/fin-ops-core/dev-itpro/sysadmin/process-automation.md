---
title: Procesu automatizācija
description: Šī tēma sniedz detalizētu informāciju par to, kā procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: e3babed18caefff16105f70a0b15b8b8cf0f08eb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568214"
---
# <a name="process-automation"></a>Procesu automatizācija

[!include[banner](../includes/banner.md)]

Procesu automatizācija ļauj vienkārši plānot procesus, ko veiks pakešu serveris. Ieplānotā darba atjauninātais kalendāra skats ļauj lietotājiem skatīt un rīkoties ar plānoto un pabeigto darbu.

## <a name="administration"></a>Administrācija

Centrālā administrēšanas lapa visu procesu automatizācijām ir atrodama Sistēmas administrēšanas modulī, kas atrodas izvēlnē **Iestatījumi**. Šajā lapā tiks uzskaitīti visi automatizētie procesi (sērijas), kas ir iestatīti sistēmā. Tas arī ļaus jums pievienot jaunu procesu automatizācijas tieši no šīs lapas. Pēc sērijas iestatīšanas varat pārvaldīt katru šī saraksta sēriju. Varat izvēlēties rediģēt visu sēriju, dzēst to, skatīt visus gadījumus saraksta skatā vai atspējot sēriju, ja vēlaties pauzēt plānoto darbu. 

Visi procesi, kas ir atspējoti līdzekļu pārvaldībā, netiks rādīti, kad līdzeklis ir atspējots. Turklāt procesu automatizācijas plānošanas programma neplāno nekādus gadījumus vai fona procesus atspējotam līdzeklim. No jauna iespējojot šo līdzekli, visi ieplānotie gadījumi vai fona procesi pagātnē tiek nekavējoties palaisti.

## <a name="calendar-view"></a>Kalendāra skats

Viens no procesa automatizācijas galvenajiem ieguvumiem ir iespēja redzēt plānoto darbu vienkāršā kalendāra skatā.  Šis skats ļauj jums skatīt darbu nedēļas laikā. Šis skats tiks rādīts **Procesa automatizācijas** lapas labajā pusē. Tas tiks aizpildīts ar atlasītās sērijas ieplānoto darbu. 

[![Procesu automatizācijas kalendārs](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Gadījumu izmaiņas

Katru gadījumu var modificēt, neietekmējot ar tām izveidoto sēriju definētos citus gadījumus. Ieplānotā darba gadījumus var rediģēt no kalendāra skata, atlasot pogu **Skatīt/rediģēt** un atlasot **Gadījums**. Šī lapa ļauj jums piekļūt visiem iestatījumiem, kas sākotnēji tika parādīti sēriju iestatīšanas vednī, un sniedz iespēju atlasītajam gadījumam veikt vienreizējas izmaiņas. Ieplānotā darba gadījumu var izslēgt arī, atlasot pogu **Atspējot** no kalendāra skata.

## <a name="developer-documentation"></a>Izstrādātāja dokumentācija

Procesu automatizācijas struktūra ļauj izstrādātājiem paplašināt procesu automatizācijas struktūru. Šī [Procesu automatizācijas struktūras](../process-automation/process-automation-framework.md) dokumentācija sniedz informāciju par to, kā varat izveidot pielāgotus procesus, kas ir nepieciešami, lai palaistu pakešu serveri, kas paredzēts procesu automatizācijas vednim, un automātiski tiek rādīti kalendāra skatā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]