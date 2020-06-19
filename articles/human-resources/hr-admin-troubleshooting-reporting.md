---
title: Pārskatu veidošanas opcijas
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431019"
---
# <a name="reporting-options"></a>Pārskatu veidošanas opcijas

**Informācija par vidi**

Šī problēma attiecas uz visām vidēm.

**Simptoms**

Debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.

**Problēma**

Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.

**Risinājums**

- Par Human Resources datiem, kas plūst uz Common Data Service, var ziņot, izmantojot Power Apps Common Data Service savienotāju ar Power BI Desktop. Ņemiet vērā, ka Common Data Service satur Human Resources datu apakškopu. Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektroniskā ziņošana (Electronic reporting — ER) ir pieejama dažiem pārskatiem Human Resources. Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.
- Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Human Resources nodrošina, izmantojot Microsoft Office integrāciju.

**Ilgterm. risināj.**

Būs pieejamas papildu Power BI opcijas, un pakalpojumā Common Data Service tiks iekļauti vairāk datu un elementu.
