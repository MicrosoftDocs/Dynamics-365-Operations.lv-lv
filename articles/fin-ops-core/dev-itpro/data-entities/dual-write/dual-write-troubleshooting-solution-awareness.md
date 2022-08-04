---
title: Problēmu novēršana saistībā ar risinājuma apzināšanos
description: Šajā rakstā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt novērst problēmas, kas saistītas ar risinājumu apzināšanu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6866956efcc76a7da6c3aa5fb36058de78d5472e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111304"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Problēmu novēršana saistībā ar risinājuma apzināšanos

[!include [banner](../../includes/banner.md)]





Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp finanšu un operāciju programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar risinājuma apzināšanos.

> [!IMPORTANT]
> Dažas no problēmām, kurām šajā rakstu adresēs var būt nepieciešama sistēmas administratora loma vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="error-on-the-dual-write-page"></a>Kļūda duālā ieraksta lapā

Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:

*Elements ar nosaukumu 'msdyn\_dualwriteentitymap' ar namemapping = 'Loģisks' netika atrasts MetadataCache.*

Lai novērstu šo problēmu, pārliecinieties, vai programmā Dataverse ir instalēts duālā ieraksta pamata risinājums. Risinājumu apzināšanai duālais ieraksts ir priekšnoteikums.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
