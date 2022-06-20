---
title: Gatavs apmaksai
description: Šajā rakstā ir parādīts, kā atzīmēt darbinieku kā gatavs apmaksāt Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 81c73584e3567d620292227ce4a24c3c0945fa96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862864"
---
# <a name="ready-to-pay"></a>Gatavs apmaksai


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Ja vēlaties atzīmēt darbinieku kā gatavu apmaksai, vispirms aktivizējiet funkcionalitāti **(Priekšskatījums) algu integrācija** līdzekļu pārvaldībā. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

Šī funkcija ļauj cilvēkresursu profesionāļiem izprast, kuri darbinieki ir gatavi algu apstrādei un kuriem ir nepieciešama darbība pirms trešās puses algas sniedzēja patērēšanas.

## <a name="mark-employee-as-ready-to-pay"></a>Atzīmēt darbinieku kā gatavu maksāt

Darbinieka informācijas apkopošana un validēšana var būt laikietilpīga un kļūdaina. Nodrošinot veidu cilvēkresursu profesionāļiem, lai pārskatītu un viegli atjauninātu darbinieka informāciju, Dynamics 365 Human Resources palīdz samazināt laiku, kas tiek patērēts, lai sagatavotos algu apstrādei.

Lai atzīmētu darbinieku kā gatavu apmaksai:

1. Atveriet **Noklikšķiniet uz Atlīdzību pārvaldība**. Darbvietā ir divi elementi: 
    - **Darbinieki, kuri ir gatavi apmaksai**
    - **Darbinieki nav gatavi maksāt**
    ![Kompensācijas pārvaldības darbvieta.](./media/hr-ready-to-pay-1-workspace.png)

2. Atlasiet elementu **Darbinieki, kas nav gatavi maksāt**.

3. Atlasiet apstiprināmos darbiniekus. Cilnē **Alga** grupā **Gatavs maksāt** atlasiet **Pārbaudīt**.
    ![Pārbaudīt darbiniekus.](./media/hr-ready-to-pay-2-validate.png)

4. Lai pārskatītu rezultātus, cilnes **Alga** grupā **Gatavs maksāt** atlasiet **Rezultāti**.

## <a name="validation"></a>Validēšana

Pirms darbinieka atzīmēšanas par gatavu maksāt sistēma veiks profila pilnīguma validāciju.

![Rezultātu pārbaude.](./media/hr-ready-to-pay-3-results.png)

| Validēšana | Detalizētā informācija |
| --- | --- |
| **Adreses mērķa parametrs** | Pārbauda, vai parametrs **Izmantot algas adrešu mērķi** ir atlasīts. |
| **Algas adrese** | Pārbauda, vai darbinieka profilam ir vismaz viena adrese ar nolūku **Algas apmaksas vieta** vai **Algas darba vieta**, un katram nolūkam ir tikai viena adrese. |
| **Nodarbinātība** | Pārbauda, vai darbiniekam ir vismaz viena nodarbinātība (pašreizējā, iepriekšējā vai turpmākā). |
| **Identifikācijas numurs** | Pārbauda, vai parametrs **Izmantot identifikācijas tipus algu apstrādē** lapā **Cilvēkresursu parametri** ir **Jā**, un, ja parametrā norādītais identifikācijas tips ir aizpildīts darbinieka profilā. |
| **Vārds un uzvārds** | Apstiprina, vai ir aizpildīti lauki **Vārds** un **Uzvārds**.|
| **Vieta** | Pārbauda, vai darbiniekam ir piešķirts amats. |
| **Dzimšanas datums** | Apstiprina, ka ir aizpildīts lauks **Dzimšanas datums**. |
| **Kompensācija** | Pārbauda, vai darbinieks ir reģistrēts fiksētās atlīdzības plānā. |

Ja kāda no šīm apstiprināšanām neizdodas, nevar atzīmēt darbinieku kā gatavu maksāt.

Ja lauks **Gatavs maksāt** ir **Nē**, šī ir norāde, ka jāveic darbība, lai nodrošinātu, ka darbinieka profils ir pabeigts. Tas neapturēs datu saskarsmi ar jebkuru datu elementu. 

## <a name="process-automation"></a>Procesu automatizācija

Jūs varat automatizēt visu darbinieku pārbaudi, izmantojot [Procesu automatizāciju](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation). **Atlīdzību pārvaldības** darbvietā dodieties uz **Saites** \> **Parametri** \> **Procesu automatizācija**.

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
