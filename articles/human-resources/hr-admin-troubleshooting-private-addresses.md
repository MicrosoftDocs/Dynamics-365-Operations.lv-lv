---
title: Piekļuve privātām adresēm atbilstoši drošības lomai
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors nevar piekļūt privātajām adresēm.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419522"
---
# <a name="access-to-private-addresses-by-security-role"></a>Piekļ. priv. adresēm atbilstoši droš. lomai

**Izsniegt**

Pēc tam, kad debitors dublē drošības lomu un pierakstās ar šo jauno lomu, tas nevar skatīt adreses, kas tika atzīmētas kā privātas.

**Izšķirtspēja**

Lai atrisinātu probl., debitoram ir jāveic šādas darbības attiecībā uz dublēto droš. lomu.

1. Dod. uz **Organizācijas admin. \> Globālā adrešu grām. \> Globālās adrešu grām. parametri**.
2. Cilnē **Privāto vietu drošība** pārvietojiet jaunu drošības lomu no saraksta **Pieejamās lomas** uz sarakstu **Atlasītās lomas**.
3. Atlasiet **Saglabāt**.

![Lapa Glob. adrešu grām. parametri](media/GAD-parameters.png)
