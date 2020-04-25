---
title: Uzturēšanas grafika izmaksas
description: Šajā tēmā ir paskaidrotas uzturēšanas grafika izmaksas programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8feea75bb223bdbd013b11cdf3a63d504afb04f5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208206"
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

6. Cilnē **Uzturēšanas grafika izmaksas** darbības rūts grupās **Grupēt pēc...** noklikšķiniet uz attiecīgajām pogām, lai uzrādītu nepieciešamo izmaksu aprēķina informācijas līmeni. Atlasītās darbības rūts grupas pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

7. Noklikšķiniet uz pogas **Aprēķināt izmaksas**, ja vēlaties veikt jaunu izmaksu aprēķinu.

Nākamajā attēlā ir redzami uzturēšanas grafika izmaksu aprēķina rezultāti.

![1. attēls](media/17-preventive-maintenance.png)

