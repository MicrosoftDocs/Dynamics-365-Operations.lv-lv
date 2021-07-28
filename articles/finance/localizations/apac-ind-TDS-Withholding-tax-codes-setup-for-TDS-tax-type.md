---
title: ieturētā nodokļa kodu iestatīšana TDS nodokļu tipam
description: Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) nodokļa kodus.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 57de382c6d363a6c1d87cf734e9aedb32d6009a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349932"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>ieturētā nodokļa kodu iestatīšana TDS nodokļu tipam

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) nodokļa kodus.

1. Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> ieturētā nodokļa kodi**.

    [![Ieturēto nodokļu kodi lapa.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Darbību rūtī atlasiet **Jauns**, lai izveidotu ieturētā nodokļa kodu TDS, un ievadiet nepieciešamo informāciju.
3. Kopsavilkuma cilnes **Vispārīgi** laukā **Nodokļu tips** atlasiet **TDS**, lai nodokļu kodu kategorizētu kā TDS nodokļa kodu.
4. Laukā **Norēķinu periods** atlasiet TDS norēķinu periodu TDS nodokļa kodam.
5. Laukā **Galvenais konts** atlasiet virsgrāmatas kontu, kurā jāgrāmato TDS summa.
6. Laukā **Debitoru konts** atlasiet debitoru kontu, kurā jāgrāmato TDS summa, kas ir ieturēta pārdošanas darījumos.

    Lauks **Izcelsme** automātiski tiek iestatīts kā **Procenti no bruto summas**, un vērtību nevar mainīt.

    > [!NOTE]
    > TDS nodokļu tipa nodokļu kodiem nevar iestatīt izcelsmi **Procenti no neto summas**.

7. Laukā **ieturētā nodokļa komponents** atlasiet ieturētā TDS nodokļa komponentu TDS nodokļu kodam.
8. Darbību rūtī atlasiet **Vērtības**, lai atvērtu lapu **ieturētā nodokļa vērtības**.
9. Laukā **Sākuma datums** ievadiet TDS vērtības sākuma datumu. Laukā **Beigu datums** ievadiet beigu datumu.

    > [!NOTE]
    > Lauki **Minimālais limits**, **Augšējais limits** un **Izņemot %** nav pieejami TDS nodokļu tipa nodokļu kodiem.

10. Laukā **Vērtība** ievadiet TDS nodokļa kodam izmantojamo TDS procentuālo vērtību.
11. Aizveriet lapu **ieturētā nodokļa vērtības**, lai atgrieztos **ieturētā nodokļa kodu** lapā.

    > [!NOTE]
    > Poga **Limiti** lapā **ieturētā nodokļa kodi** nav pieejama TDS nodokļa tipa nodokļa kodiem.

12. Aizvērt lapu.
