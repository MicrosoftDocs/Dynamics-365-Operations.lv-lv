---
title: Problēmu novēršana saistībā ar risinājuma apzināšanos
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājumu apzināšanos.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172625"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Problēmu novēršana saistībā ar risinājuma apzināšanos

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājuma apzināšanos.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="error-on-the-dual-write-page"></a>Kļūda duālā ieraksta lapā

Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:

*Elements ar nosaukumu 'msdyn\_dualwriteentitymap' ar namemapping = 'Loģisks' netika atrasts MetadataCache.*

Lai novērstu šo problēmu, pārliecinieties, vai programmā Common Data Service ir instalēts duālā ieraksta pamata risinājums. Risinājumu apzināšanai duālais ieraksts ir priekšnoteikums.
