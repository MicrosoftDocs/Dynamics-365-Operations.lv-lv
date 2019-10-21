---
title: Talent pārsk. veidoš. iesp.
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Talent pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009356"
---
# <a name="reporting-options-in-talent"></a>Pārskatu veidošanas iespējas programmā Talent

[!include [banner](includes/banner.md)]

**Informācija par vidi**

Šī problēma attiecas uz visām vidēm.

**Simptoms**

Debitors vēlas pielāgot Microsoft Dynamics 365 Talent pārskatus vai izveidot jaunus pārskatus.

**Problēma**

Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.

**Risinājums**

- Par Core HR datiem, kas plūst uz Common Data Service, var ziņot, izmantojot PowerApps Common Data Service savienotāju ar Power BI Desktop. Ņemiet vērā, ka Common Data Service satur Core HR datu apakškopu. Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent. Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.
- Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.

**Ilgterm. risināj.**

Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.
