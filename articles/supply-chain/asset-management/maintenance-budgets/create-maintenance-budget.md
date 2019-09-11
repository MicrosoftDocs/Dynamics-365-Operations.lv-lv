---
title: Uzturēšanas budžetu izveide
description: Šajā tēmā ir paskaidrots, kā izveidot uzturēšanas budžetu programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2c748fd230796643f1ed6279743da532e7cb320
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874812"
---
# <a name="create-maintenance-budgets"></a>Uzturēšanas budžetu izveide

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]



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

![1. attēls](media/01-maintenance-budgets.png)

Jūs varat arī izveidot jaunu uzturēšanas budžetu, kopējot esošu budžetu. Kopējamo budžetu atlasiet lapā **Uzturēšanas budžeti**, tad atlasiet **Kopēt**. Šī pieeja ir noderīga, piemēram, ja esat izveidojis budžetu vienam mēnesim un vēlaties to kopēt citiem mēnešiem.

> [!NOTE]
> Uzturēšanas budžetā tiek aprēķinātas tikai budžeta izmaksas, balstoties uz uzturēšanas grafika rindām. Lai aprēķinātu faktiskās izmaksas tam pašam periodam, šo aprēķinu var veikt lapā **Līdzekļu izmaksu kontrole**. 
