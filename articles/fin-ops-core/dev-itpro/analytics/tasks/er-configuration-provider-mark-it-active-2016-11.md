---
title: Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus
description: Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9428ff1f53928f104df4736911ce34756128da44
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359439"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju elektroniskajiem pārskatiem (Electronic reporting — ER). Katra ER konfigurācija atsauksies uz nodrošinātāju kā konfigurācijas autoru. Šajā piemērā tiek izveidots konfigurēšanas pakalpojuma sniedzējs parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurēšanas pakalpojuma sniedzēji ir kopīgi visiem uzņēmumiem.

## <a name="create-a-provider"></a>Nodrošinātāja izveide
1. Dodieties uz sadaļu **Navigācijas rūts** augšējā kreisajā stūrī un atlasiet **Organizācijas administrēšana.**
2. Dodieties uz **Darbvietas > Elektroniskie pārskati**.
3. Dodieties uz **Saistītās saites > Konfigurācijas nodrošinātāji**.
4. Atlasiet **Jauns**.
    - Nodrošinātāja ierakstam ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu un izlaidiet šo procedūru, ja “Litware, Inc.” (https://www.litware.com) ieraksts jau pastāv.  
5. Laukā Nosaukums ierakstiet `Litware, Inc.`.
6. Laukā Interneta adrese ierakstiet `https://www.litware.com`.
7. Atlasiet **Saglabāt**.
8. Aizvērt lapu.

## <a name="select-as-an-active-provider"></a>Atlasiet kā aktīvu nodrošinātāju
1. Atlasiet pakalpojumu sniedzēju Litware, Inc.
2. Atlasiet **Iestatīt kā aktīvu**.

![Elektronisko pārskatu darbvietas lapa.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]