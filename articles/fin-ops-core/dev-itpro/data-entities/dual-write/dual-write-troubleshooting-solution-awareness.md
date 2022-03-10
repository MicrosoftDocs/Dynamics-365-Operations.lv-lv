---
title: Problēmu novēršana saistībā ar risinājuma apzināšanos
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājumu apzināšanos.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f83a064bfc8896bdf76bcd38f9187ed0e1ea56cf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062317"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Problēmu novēršana saistībā ar risinājuma apzināšanos

[!include [banner](../../includes/banner.md)]





Šajā tēmā ir sniegta problēmu novēršanas informācija divu rakstu integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājuma apzināšanos.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="error-on-the-dual-write-page"></a>Kļūda duālā ieraksta lapā

Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:

*Elements ar nosaukumu 'msdyn\_dualwriteentitymap' ar namemapping = 'Loģisks' netika atrasts MetadataCache.*

Lai novērstu šo problēmu, pārliecinieties, vai programmā Dataverse ir instalēts duālā ieraksta pamata risinājums. Risinājumu apzināšanai duālais ieraksts ir priekšnoteikums.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]