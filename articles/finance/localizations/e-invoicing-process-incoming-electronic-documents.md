---
title: Ienākošo elektronisko dokumentu apstrāde
description: Šajā rakstā sniegts pārskats par ienākošo elektronisko dokumentu apstrādi.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277307"
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
