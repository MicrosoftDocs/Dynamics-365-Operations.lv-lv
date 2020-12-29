---
title: Izveidot uzturēšanas pieprasījumus
description: Šajā tēmā izskaidrots, kā izveidot uzturēšanas pieprasījumu Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 22d5e371c386abc71946bf64ed8792647f78cf1b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432840"
---
# <a name="create-maintenance-requests"></a>Izveidot uzturēšanas pieprasījumus

[!include [banner](../../includes/banner.md)]

 

Uzturēšanas pieprasījumus var izmantot, ja uzturēšanas darbinieki vai ražošanas darbinieki atklāj, ka aprīkojumam nepieciešams remonts, bet remonta darbus nevar veikt uzreiz.

**Piemērs:** kamēr uzturēšanas darbiniece veic remontu, viņa atklāj, ka ir nepieciešama cita līdzekļa tajā pašā atrašanās vietā apkope. Taču uzturēšanas darbiniecei nav ne laika, ne nepieciešamo rezerves daļu, lai veiktu remonta darbus. Tāpēc viņa izveido uzturēšanas pieprasījumu līdzeklim un ievada īsu problēmas aprakstu.

Sadaļa **Aktīvie uzturēšanas pieprasījumi** rūtī **Saistītā informācija**, kas atrodas lapas **Visi līdzekļi** vai **Aktīvie līdzekļi** labajā pusē (**Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**) rāda aktīvos uzturēšanas pieprasījumus, kas ir pievienoti atlasītajam līdzeklim.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Dialoglodziņā **Izveidot pieprasījumu** laukā **Uzturēšanas pieprasījuma veids** atlasiet uzturēšanas pieprasījuma veidu. Tiek ieteikts noklusētais veids.
4. Laukā **Apraksts** ievadiet nosaukumu vai virsrakstu, kas īsumā apraksta uzturēšanas pieprasījumu.
5. Laukā **Funkcionālais novietojums** un **Līdzeklis** atlasiet funkcionālo novietojumu vai līdzekli, vai arī funkcionālā novietojuma un līdzekļa kombināciju pēc vajadzības. Varat izveidot uzturēšanas pieprasījumu, neatlasot līdzekli, un līdzekli var pievienot uzturēšanas pieprasījumam vēlāk. Ja uzturēšanas darbinieks, kurš ir pierakstījies, ir saistīts ar resursu, kas saistīts ar līdzekli, automātiski tiek iestatīts lauks **Līdzeklis**.

    Ja atlasītajam līdzeklim jau ir pievienots uzturēšanas pieprasījums, dialoglodziņa **Izveidot pieprasījumu** augšpusē tiek parādīta ziņojumu josla, lai informētu jūs par esošā uzturēšanas pieprasījuma ID. Ziņojumu josla arī informē jūs, ja uz līdzekli attiecas garantijas līgums.

6. Laukā **Pakalpojumu līmenis** atlasiet pakalpojumu līmeni, kas norāda pieprasījuma steidzamību.
7. Ja atlasījāt līdzekli 5. solī, varat izmantot laukus **Kļūmes simtoms**, **Kļūmes apgabals** un **Kļūmes veids**, lai izveidotu kļūmes reģistrāciju.
8. Ja uzturēšanas pieprasījums ir izraisījis uzturēšanas dīkstāvi, ievadiet sākuma datumu un dīkstāves laiku.

    Lauks **Sācis...** tiek automātiski iestatīts uz jūsu vārda.

10. Lauks **Faktiskais sākums** automātiski tiek iestatīts uz pašreizējo datumu un laiku. Tomēr, jūs varat mainīt vērtību pēc nepieciešamības.
11. Laukā **Piezīmes** ievadiet visas nepieciešamās papildu piezīmes.
12. Atlasiet **Labi**.

![Izveidot uzturēšanas pieprasījumu](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Turpmāka uzturēšanas pieprasījumu apstrāde

Pēc uzturēšanas pieprasījuma izveides, bet pirms tā pārveidošanas par darba pasūtījumu, tajā ir jāatjaunina dažāda informācija. Parasti šo uzdevumu pabeidz plānotājs vai cits administratīvais darbinieks.

- Lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** atlasiet pieprasījumu, ar kuru strādāt, un pēc tam atlasiet **Rediģēt.**

Detalizētas informācijas skatā varat atjaunināt dažādu informāciju. Daži piemēri:

- Atlasiet un pārbaudiet līdzekli. Ja vēlāk ir jāatlasa cits līdzeklis, varat iestatīt opciju **Līdzeklis verificēts** uz **Nē.**
- Atlasiet atbildīgo uzturēšanas darbinieku grupu un/vai atbildīgo uzturēšanas darbinieku. Papildinformāciju par nepieciešamajiem iestatījumiem skatiet sadaļā [Atbildīgie uzturēšanas darbinieki](../setup-for-maintenance-requests/responsible-workers.md).
- Atlasiet uzturēšanas darba veidu un, ja šī informācija ir būtiska, saistīto uzturēšanas darba variantu un darba tirdzniecību.
- Laukos **Platums** un **Garums** ievadiet ģeogrāfiskās koordinātas. Visas koordinātas, kas tiek pievienotas uzturēšanas pieprasījumam, tiek automātiski pārsūtītas uz saistīto darba pasūtījumu. 

![Uzturēšanas pieprasījuma atjaunināšana](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Ja atlasāt līdzekli, veidojot uzturēšanas pieprasījumu, varat līdzeklim pievienot vienu kļūmi. Pēc uzturēšanas pieprasījuma izveides varat pievienot vairāk kļūmju — kā nepieciešams. Lai pievienotu kļūmes, atlasiet **Līdzekļa kļūme** lapā **Visi uzturēšanas pieprasījumi**.
