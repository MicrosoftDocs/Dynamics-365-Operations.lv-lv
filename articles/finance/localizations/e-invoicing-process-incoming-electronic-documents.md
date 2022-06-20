---
title: Ienākošo elektronisko dokumentu apstrāde
description: Šajā rakstā sniegts pārskats par ienākošo elektronisko dokumentu apstrādi.
author: dkalyuzh
ms.date: 02/28/2022
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
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910013"
---
# <a name="processing-of-incoming-electronic-documents"></a>Ienākošo elektronisko dokumentu apstrāde

[!include [banner](../includes/banner.md)]

Ienākošos elektroniskos dokumentus, piemēram, kreditora elektroniskos rēķinus, var importēt un apstrādāt divos veidos:

- Faili tiek izgūti no ārējiem kanāliem un pārsūtīti tieši uz jūsu pievienoto programmu. Tur tie notiek papildus transformācija un tad tiek importēti datu bāzē.
- Faili atrodas pirmapstrāde Elektronisko rēķinu izrakstīšanas pakalpojumā un pēc tam nodoti jūsu pievienotajā programmā.

Elektronisko rēķinu izrakstīšana atbalsta divus kanālus ienākošajiem dokumentiem: e-pasta ziņojumiem un Microsoft SharePoint mapēm.

Ir twp iestatījumu tipi, lai norādītu, vai dokumenti tiek pakļauti pirmapstrādei vai arī tie tiek nodoti tieši saistītajā programmā:

- **Datu kanāls** – Sistēma paies dokumentu tieši uz pievienoto programmu.
- **Datu kanāls ar apstrādes konveijeru** – Jūs varat iestatīt papildu darbības, kas tiks palaistas pirms dokumenta pārsūtīšanas uz pievienoto programmu.

Informāciju par to, kā iestatīt scenārijus ienākošo elektronisko dokumentu apstrādei dažādiem kanāliem, skatiet Konfigurēt [e-pasta kanālu](e-invoicing-configure-email.md) un [Konfigurēt SharePoint kanālu](e-invoicing-configure-sharepoint-channel.md).
