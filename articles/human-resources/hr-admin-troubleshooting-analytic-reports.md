---
title: Problēmu novēršanas analītiskie pārskati
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
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
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419577"
---
# <a name="troubleshoot-analytic-reports"></a>Problēmu novēršanas analītiskie pārskati

**Izejas plūsma**

Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.

**Iemesls**

Pēc noklusējuma Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.

**Izšķirtspēja**

Šo problēmu var izraisīt laika izvēle. Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.

1. Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**. Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.
1. Atrodiet sarakstā darbu **Izvietot mērījumu**.
1. Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.

![Pakešuzdevumi](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]