---
title: Uzturēšanas grafika izmaksas
description: Šajā rakstā skaidrots uzturēšanas grafika izmaksas Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91481f9bcb778796255fad006c6187916d8e6bb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908748"
---
# <a name="maintenance-schedule-cost"></a>Uzturēšanas grafika izmaksas

[!include [banner](../../includes/banner.md)]

 

Programmā Asset Management jūs varat aprēķināt budžeta izmaksas uzturēšanas grafika rindām. Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamajām izmaksām, piemēram, izmaksām, kas attiecas uz plānotiem preventīviem uzturēšanas darbiem nākamajam gadam. Aprēķini ir balstīti esošās uzturēšanas grafika rindās tipiem "Uzturēšanas plāni" un "Uzturēšanas cikli" un "Uzturēšanas pieprasījumi"

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Uzturēšanas grafika izmaksas**.

2. Dialoglodziņā **Uzturēšanas grafika izmaksas** jūs varat atlasīt opciju **Finansiālā dimensija iestatīta**, ja vēlaties redzēt izmaksas grupētas finansiālās dimensijās.

>[!NOTE]
>Finansiālās dimensijas tiek uzstādītas **Virsgrāmata** > **Kontu plāns** > **Dimensijas** > **Finansiālo dimensiju kopas**.

3. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas grafika rindas attiecībā uz funkcionālo novietojumu. Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

4. Ja vēlaties veikt aprēķinus par konkrētiem līdzekļiem, kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un atlasiet atbilstošos līdzekļus. Ja nepieciešams, jūs varat arī konkretizēt **Paredzamo sākuma** datumu izmaksu aprēķinam vai atlasīt atšķirīgu **Statusu** izmaksu aprēķinam

5. Noklikšķiniet uz **Labi**, lai sāktu izmaksu aprēķināšanu.

6. Cilnē **Uzturēšanas grafika izmaksas** darbību rūts grupās **Grupēt pēc...** noklikšķiniet uz attiecīgajām pogām, lai uzrādītu nepieciešamo izmaksu aprēķina informācijas līmeni. Atlasītās darbību rūts grupas pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

7. Noklikšķiniet uz pogas **Aprēķināt izmaksas**, ja vēlaties veikt jaunu izmaksu aprēķinu.

Nākamajā attēlā ir redzami uzturēšanas grafika izmaksu aprēķina rezultāti.

![1. attēls.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]