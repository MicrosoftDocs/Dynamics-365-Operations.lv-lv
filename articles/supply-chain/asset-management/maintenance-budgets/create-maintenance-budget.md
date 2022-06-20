---
title: Uzturēšanas budžetu izveide
description: Šajā rakstā skaidrots, kā izveidot uzturēšanas budžetu Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858045"
---
# <a name="create-maintenance-budgets"></a>Uzturēšanas budžetu izveide

[!include [banner](../../includes/banner.md)]

 



Uzturēšanas budžeti tiek izmantoti, lai iegūtu pārskatu par profilaktiskās uzturēšanas izmaksām. Budžeta rindas tiek aprēķinātas, balstoties uz uzturēšanas grafika rindām, kam ir paredzēts sākuma datums budžeta perioda laikā.

Uzturēšanas budžeti ir balstīti uz izmaksu veidiem, ko lieto programmā Asset Management: **Profilaktiskas**, **Labojošas** un **Ieguldījumi**. Budžeta izmaksas ieguldījumu uzturēšanai ir iekļautas aktīvajiem līdzekļiem, kam aizvietošanas datums ir budžeta periodā un ir saistīta aizstāšanas vērtība. Labojošas uzturēšanas budžeta izmaksas tiek iekļautas, ja pagātnes labošanas datums ir iekļauts budžeta aprēķinā. Tādā gadījuma labošanas izmaksas no iepriekšējā perioda tiek aprēķinātas tam pašam nākotnes periodam, kam aprēķināts uzturēšanas budžetu.

## <a name="create-a-maintenance-budget"></a>Uzturēšanas budžeta izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Pieprasījumi** \> **Uzturēšanas budžets** \> **Budžets**.
2. Atlasiet **Izveidot budžetu**.
3. Laukā **Uzturēšanas budžets** ievadiet budžeta ID.
4. Ievadiet aprakstu laukā **Apraksts**.
4. Kopsavilkuma cilnē **Periods** laukumā **Datums no** un **Datums līdz** ievadiet budžeta perioda sākuma un beigu datumu.
5. Lai iekļautu labošanas budžeta izmaksas, kas aprēķinātas, balstoties uz faktiskajam izmaksām iepriekšējā periodā, laukā **Labošanas datums no** ievadiet sākuma datumu periodam, no kura ir jāiekļauj šīs izmaksas.
6. Atkarībā no detalizācijas līmeņa budžetā iestatiet vajadzīgās opcijas kopsavilkuma cilnēs **Grupēt pēc**.
7. Atlasiet **Labi**.
8. Atlasiet **Budžeta rindas** lapā **Uzturēšanas budžeta rindas**, kur varat skatīt visas budžeta rindas, kas ir izveidotas periodam.
9. Lai apstiprinātu budžetu, atlasiet to lapā **Uzturēšanas budžeti**, tad atlasiet **Apstiprināt** Dialoglodziņā **Apstiprināt budžetu** atlasiet **Labi**. Jūsu vārds tiek ievadīts laukā **Apstiprināja** lapā **Uzturēšanas budžeti**.

    > [!NOTE]
    > Kad esat apstiprinājis uzturēšanas budžetu, varat pārrēķināt vai precizēt saistītās rindas lapā **Uzturēšanas budžeta rindas**, ja vien pirms tam neesat noņēmis apstiprinājumu. Lai noņemtu uzturēšanas budžeta apstiprinājumu, atlasiet to lapā **Uzturēšanas budžeti**, tad atlasiet **Apstiprināt**. Dialoglodziņā **Apstiprināt budžetu** atlasiet **Labi**.

![Uzturēšanas budžeti.](media/01-maintenance-budgets.png)

Jūs varat arī izveidot jaunu uzturēšanas budžetu, kopējot esošu budžetu. Kopējamo budžetu atlasiet lapā **Uzturēšanas budžeti**, tad atlasiet **Kopēt**. Šī pieeja ir noderīga, piemēram, ja esat izveidojis budžetu vienam mēnesim un vēlaties to kopēt citiem mēnešiem.

> [!NOTE]
> Uzturēšanas budžetā tiek aprēķinātas tikai budžeta izmaksas, balstoties uz uzturēšanas grafika rindām. Lai aprēķinātu faktiskās izmaksas tam pašam periodam, šo aprēķinu var veikt lapā **Līdzekļu izmaksu kontrole**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]