---
title: Ienākošie un izejošie līdzekļi
description: Šajā tēmā paskaidrots, kā reģistrēt ienākošos un izejošos līdzekļus Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847555"
---
# <a name="inbound-and-outbound-assets"></a>Ienākošie un izejošie līdzekļi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ja jūsu uzņēmums veic labošanas darbus vai uzturēšanas darbus līdzekļiem, kas saņemti no citām atrašanās vietām vai debitoriem, Līdzekļu pārvaldība var izsekot gan ienākošos līdzekļus, kas ir ceļā uz jūsu uzņēmumu, gan uz izejošos līdzekļus, kas tiek atgriezti.

> [!NOTE]
> Ja vēlaties izmantot ienākošos un izejošos dzīves cikla stāvokļus, lai pārvaldītu līdzekļus, kas ienāk un tiek atgriezti, jums ir jāiestata uzturēšanas pieprasījumu dzīves cikla stāvokļi un dzīves cikla modeļi šo darbību atbalstīšanai. Papildinformāciju skatiet sadaļā [Uzturēšanas pieprasījumu iestatīšana](../setup-for-maintenance-requests/requests.md).

Līdzekļu pārvaldības iestatījumi nosaka, vai varat strādāt ar ienākošajiem un izejošajiem līdzekļiem.

## <a name="register-assets-as-inbound"></a>Reģistrēt līdzekļus kā ienākošos

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Aktīvie uzturēšanas pieprasījumi**.
2. Atlasit uzturēšanas pieprasījumu.
3. Atlasiet **Atjaunināt uzturēšanas pieprasījuma stāvokli**.
4. Atlasiet **Ienākošais** (vai cits dzīves cikla stāvoklis, ko esat izveidojis ienākošajiem līdzekļiem) un pēc tam atlasiet **Labi**.

![1. attēls](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Reģistrēt ienākošos līdzekļus kā saņemtus

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Ienākošie/izejošie** \> **Ienākošie līdzekļi**.
2. Atlasiet līdzekli vai uzturēšanas pieprasījumu.
3. Atlasiet **Saņemt līdzekļus**.
4. Laukā **Saņemts** ievadiet datumu un laiku. Tad atl. **Labi**. Ieraksts tiek noņemts saraksta lapā **Ienākošie līdzekļi**.

![2. attēls](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Reģistrēt līdzekļus kā izejošos

Kad esat pabeidzis uzturēšanas vai labošanas darbu, līdzekli var reģistrēt kā atgrieztu.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Aktīvie uzturēšanas pieprasījumi**.
2. Atlasit uzturēšanas pieprasījumu.
3. Atlasiet **Atjaunināt uzturēšanas pieprasījuma stāvokli**.
4. Atlasiet **Izejošie** (vai cits dzīves cikla stāvoklis, ko esat izveidojis izejošajiem līdzekļiem) un pēc tam atlasiet **Labi**.

## <a name="register-outbound-assets-as-delivered"></a>Reģistrēt izejošos līdzekļus kā piegādātus

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Ienākošie/izejošie** \> **Izejošie līdzekļi**.
2. Atlasiet līdzekli vai uzturēšanas pieprasījumu.
3. Atlasiet **Piegādātie līdzekļus**.
4. Laukā **Piegādāts** ievadiet datumu un laiku. Tad atl. **Labi**. Ieraksts tiek noņemts saraksta lapā **Izejošie līdzekļi**.
