---
title: Problēmu novēršanas analītiskie pārskati
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053543"
---
# <a name="troubleshoot-analytic-reports"></a>Problēmu novēršanas analītiskie pārskati

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.

**Iemesls**

Pēc noklusējuma Microsoft Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.

**Izšķirtspēja**

Šo problēmu var izraisīt laika izvēle. Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.

1. Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**. Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.
1. Atrodiet sarakstā darbu **Izvietot mērījumu**.
1. Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.

![Pakešuzdevumi](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]