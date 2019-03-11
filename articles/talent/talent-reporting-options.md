---
title: Talent pārsk. veidoš. iesp.
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izveidot jaunus pārskatus.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305372"
---
# <a name="reporting-options-in-talent"></a>Pārskatu veidošanas iespējas programmā Talent

[!include [banner](includes/banner.md)]

**Informācija par vidi**

Šī problēma attiecas uz visām vidēm.

**Simptoms**

Debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izveidot jaunus pārskatus.

**Izejas plūsma**

Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.

**Risinājums**

- Core HR datus, ko sūta uz Common Data Service programmām, var ziņot Power BI Desktop, lietojot PowerApps CDS savienotāju. Common Data Service programmām satur Core HR datu apakškopu. Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent. Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.
- Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.

**Ilgterm. risināj.**

Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service programmām tiks iekļauti vēl dati un elementi.
