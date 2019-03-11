---
title: Anal. pārskati netiek atjaun.
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
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
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305281"
---
# <a name="analytic-reports-are-not-updated"></a>Anal. pārskati netiek atjaun.

[!include [banner](includes/banner.md)]

**Izsniegt**

Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.

**Iemesls**

Pēc noklusējuma Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.

**Izšķirtspēja**

Šo problēmu var izraisīt laika izvēle. Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.

1. Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**. Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.
1. Atrodiet sarakstā darbu **Izvietot mērījumu**.
1. Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.

![Pakešuzdevumi](media/batch-jobs.png)
