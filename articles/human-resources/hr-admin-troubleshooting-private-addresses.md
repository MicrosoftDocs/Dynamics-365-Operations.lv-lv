---
title: Piekļuve privātām adresēm atbilstoši drošības lomai
description: Šajā rakstā paskaidrots, kā atrisināt problēmu, ja debitors nevar piekļūt privātajām adresēm.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 49f9f50b774df8e215c084bbb493a6be9de6b234
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463940"
---
# <a name="access-to-private-addresses-by-security-role"></a>Piekļ. priv. adresēm atbilstoši droš. lomai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izsniegt**

Pēc tam, kad debitors dublē drošības lomu un pierakstās ar šo jauno lomu, tas nevar skatīt adreses, kas tika atzīmētas kā privātas.

**Izšķirtspēja**

Lai atrisinātu probl., debitoram ir jāveic šādas darbības attiecībā uz dublēto droš. lomu.

1. Dod. uz **Organizācijas admin. \> Globālā adrešu grām. \> Globālās adrešu grām. parametri**.
2. Cilnē **Privāto vietu drošība** pārvietojiet jaunu drošības lomu no saraksta **Pieejamās lomas** uz sarakstu **Atlasītās lomas**.
3. Atlasiet **Saglabāt**.

![Lapa Glob. adrešu grām. parametri](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]