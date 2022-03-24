---
title: ieturētā nodokļa kodu iestatīšana TDS nodokļu tipam
description: Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) nodokļa kodus.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 03d8b7d4992fbb49a873f14e1ce1f0c816cef202
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407464"
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
