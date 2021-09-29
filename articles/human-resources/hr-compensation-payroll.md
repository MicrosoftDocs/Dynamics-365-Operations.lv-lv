---
title: Gatavs apmaksai
description: Šajā tēmā ir parādīts, kā atzīmēt darbinieku kā gatavu maksāt risinājumā Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80bba5446eb7a87d96a7da4ae856cb5ca114ce52
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483786"
---
# <a name="ready-to-pay"></a>Gatavs apmaksai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

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

## <a name="known-issues"></a>Zināmās problēmas

- Līdzekļu pārvaldībā jums jāatspējo iespēja **Racionalizēts darbinieka ieraksts**. Ja izmantojat šo funkciju, kompensācijas pārvaldības darbvietā darbs nedarbosies pareizi.
- Lapā **Darbinieks** cilnes **Alga** grupa  **Gatavs maksāt** ir pieejama jebkurai lietotāja lomai. 

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
