---
title: Elektronisko rēķinu izrakstīšanas iestatījumi
description: Šajā rakstā sniegts elektronisko rēķinu izrakstīšanas iestatīšanas un konfigurēšanas procesa apskats.
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
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272185"
---
# <a name="electronic-invoicing-setup"></a>Elektronisko rēķinu izrakstīšanas iestatījumi

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts elektronisko rēķinu izrakstīšanas iestatīšanas un konfigurēšanas procesa apskats. Iestatīšanas soļi jāveic šeit norādītajā secībā. Ja solis ir obligāts, bet jūs to izlaižat, funkcionalitāte nedarbosies pareizi, un vairākas kļūmes radīsies turpmāko darbību vai kad izmantojat funkcionalitāti. 

Pirms sākat, pārliecinieties, vai visi galvenie komponenti ir pareizi iestatīti, vai esat pierakstījies regulēšanas konfigurācijas pakalpojumam (RCS) un ir RCS instance un Microsoft Dynamics vai elektronisko rēķinu izrakstīšanas pievienojumprogramma ir instalēta jūsu 365 Finansēm Dynamics 365 Supply Chain Management vai videi. Papildinformāciju skatiet sadaļā Elektronisko [rēķinu izrakstīšana un instalēšana](e-invoicing-install-add-in-microservices-lcs.md).

Tālāk iestatiet Azure resursus, kas ir nepieciešami elektronisko rēķinu izrakstīšanai, lai tie darbotos. Papildinformāciju skatiet sadaļā [Azure resursu iestatīšana elektronisko rēķinu izrakstīšanai](e-invoicing-set-up-azure-resources.md).

Kad galvenie komponenti ir konfigurēti, strādājiet ar RCS, lai iestatītu elektronisko rēķinu izrakstīšanas galvenos loģiskos komponentus. Nosakiet, nosakiet pakalpojumu vides skaitu, ko uzturēsiet. Šādā veidā definējiet loģiskos datus un konfigurācijas nodalīšanas, lai nodrošinātu, ka jums ir robeža starp izstrādes vai testēšanas vidi un ražošanas vidēm. Lai iestatītu savu izstrādes procesu elastīgā veidā, jums var būt nepieciešamas vairākas atsevišķas izstrādes un testēšanas vides. Papildus pakalpojumu vides noteikšanai iestatiet saiti uz jūsu biznesa programmām, piemēram, Finanšu vai piegādes ķēdes pārvaldību, tieši no RCS, lai iestatītu parametrus, kas ir nepieciešami pareizai darbībai ar Elektronisko rēķinu izrakstīšanu. Papildinformāciju par vidēm skatiet [sadaļā Pakalpojumu vides](e-invoicing-service-environments.md).

Kad viss ir iestatīts, jūs varat izveidot savus globalizācijas līdzekļus, kas nosaka dažādus scenārijus elektronisko dokumentu apstrādei un datu pārveidošanai vai dokumentu importēšanai no Globālā repozitorija. Papildinformāciju par to, kā strādāt ar globalizācijas līdzekļiem, skatiet darbs [ar globalizācijas līdzekļiem](e-invoicing-working-globalization-features.md).

Ja jūsu scenārijiem nepieciešama integrācija ar e-pastu SharePoint vai apstrādāt ienākošos elektroniskos dokumentus, [skatiet](e-invoicing-process-incoming-electronic-documents.md) Apstrādājiet ienākošos elektroniskos dokumentus, lai iegūtu informāciju par to, kā iestatīt un izmantot šos kanālus.
