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
ms.openlocfilehash: d4e76f3b6231b6f307173fa176360daf775c8a7950bc4ab2f2162c768102c369
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717418"
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

![Pakešuzdevumi.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]