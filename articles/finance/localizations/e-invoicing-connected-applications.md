---
title: Savienotās programmas
description: Šajā tēmā skaidrots, kā elektronisko rēķinu izrakstīšanai iestatīt pievienotos pieteikumus.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371920"
---
# <a name="connected-applications"></a>Savienotās programmas

[!include [banner](../includes/banner.md)]

Saistītās programmas ir Microsoft instances un Dynamics 365 Finance kuras, iespējams Dynamics 365 Supply Chain Management, vēlēsities sasniegt, izmantojot regulēšanas konfigurācijas pakalpojumu (RCS). Izmantojot savienotās programmas, jūs varat konfigurēt daļu no jūsu globalizācijas funkcijas Finanšu vai piegādes ķēžu pārvaldībā, lai izveidotu Elektronisko rēķinu izrakstīšanas scenāriju darbu.

Kad izvietojat savu globalizācijas līdzekli, iestatīšanas informāciju, kas ir piemērojama jūsu Finanšu vai piegādes ķēdes pārvaldības programmai, var publicēt tieši no RCS uz atbilstošo pievienoto programmu.

Finanšu vai piegādes ķēdes pārvaldības parametru pieejamība RCS ir noderīga, kad jums ir vairākas programmas vides, piemēram, lietotāju pieņemšanas pārbaude (UAT) un ražošanas vides, un jūs vēlaties saglabāt iestatījumu konsekventu, izvietojot vienus un tos pašus parametrus dažādās vidēs.

## <a name="create-a-connected-application"></a>Izveidojiet pievienotu pievienojumprogrammu

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. **Lapas Vides iestatījums** darbību rūtī atlasiet Saistītās **programmas**.
4. Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.
5. Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.
6. Laukā **Veids** atlasiet **Dynamics 365 Finance**.
7. Laukā **Programma** ievadiet vides URL, ar kuru veidot savienojumu.
8. Laukā **Nomnieks** ievadiet vides nomnieku.
9. Atlasiet **Saglabāt**.
10. Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi. Tad aizveriet lapu.

## <a name="link-connected-applications-to-environments"></a>Saistīt savienotās programmas ar vidēm

1. Lai videi **piešķirtu pievienoto** programmu **, lapā** Vides iestatījums atlasiet Jauns.
2. Laukā **Savienotā programma** atlasiet savienoto lietojumprogrammu.
3. Laukā **Pakalpojuma vide** atlasiet darba pasūtījuma pakalpojuma vidi.
4. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.