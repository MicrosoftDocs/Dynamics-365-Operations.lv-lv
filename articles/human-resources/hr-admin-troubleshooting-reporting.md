---
title: Pārskatu veidošanas opcijas
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463290"
---
# <a name="reporting-options"></a>Pārskatu veidošanas opcijas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Informācija par vidi**

Šī problēma attiecas uz visām vidēm.

**Simptoms**

Debitors vēlas pielāgot Microsoft Dynamics 365 Human Resources pārskatus vai izveidot jaunus pārskatus.

**Izsniegt**

Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.

**Risinājums**

- Par Human Resources datiem, kas plūst uz Dataverse, var ziņot, izmantojot Power Apps Dataverse savienotāju ar Power BI Desktop. Ņemiet vērā, ka Dataverse satur Human Resources datu apakškopu. Plašāku informāciju par Power BI un informācijas paneļiem skatiet sadaļā [Power BI pārskatu un informācijas paneļu izveide ar Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektroniskā ziņošana (Electronic reporting — ER) ir pieejama dažiem pārskatiem Human Resources. Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.
- Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Human Resources nodrošina, izmantojot Microsoft Office integrāciju.

**Ilgterm. risināj.**

Būs pieejamas papildu Power BI opcijas, un pakalpojumā Dataverse tiks iekļauti vairāk datu un elementu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]