---
title: "Talent pārsk. veidoš. iesp."
description: "Šajā tēmā paskaidrots, kā atrisināt probl., ja debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izveidot jaunus pārskatus."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Talent pārsk. veidoš. iesp.

[!include [banner](includes/banner.md)]

**Informācija par vidi**

Šī problēma attiecas uz visām vidēm.

**Simptoms**

Debitors vēlas pielāgot Microsoft Dynamics 365 for Talent pārskatus vai izv. jaunus pārskatus.

**Izsniegt**

Lietotājs nevar pielāgot iegultos Microsoft Power BI pārskatus.

**Risinājums**

- Core HR datus, ko sūta uz Common Data Service programmām, var ziņot Power BI Desktop, lietojot PowerApps CDS savienotāju. Common Data Service programmām satur Core HR datu apakškopu. Plašāku inform. par Power BI un inf. paneļiem sk. sad. [Power BI pārskatu un inf. paneļu izveide ar PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektr. pārsk. veidošana (ER) ir pieej. dažiem pārskatiem Talent. Debitoriem paredzētu pielāgošanu var veikt, izmantojot ER konfig. opcijas.
- Datus var eksportēt uz Microsoft Excel vai Microsoft Word, izmantojot dažādus datu elementus, kurus Talent nodrošina ar Microsoft Office integrāciju.

**Ilgterm. risināj.**

Būs pieejamas pap. Power BI opcijas, un pakalpojumā Common Data Service programmām tiks iekļaui vēl dati un elementi.

