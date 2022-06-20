---
title: Problēmu novēršanas analītiskie pārskati
description: Šajā rakstā ir izskaidrots, kā novērst problēmas un veikt tajā problēmas, ja debitora datu izmaiņas neparādās neviena no debitora darbvietām.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6ae8931679feb2103172eb1a21649734acd995
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902232"
---
# <a name="troubleshoot-analytic-reports"></a>Problēmu novēršanas analītiskie pārskati


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
