---
title: "Grāmatošana, izmantojot atvasinātās grāmatas"
description: "Šajā rakstā ir aprakstīts, kā izmantot atvasinātās grāmatas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9f20fbc908e6e12a60c0126836eea4e92314cfcd
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="post-with-derived-books"></a>Grāmatošana, izmantojot atvasinātās grāmatas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā izmantot atvasinātās grāmatas.

Grāmatojot darbības grāmatai, kurā iekļautas atvasinātās grāmatas, atvasināto grāmatu darbības tiek automātiski grāmatotas žurnālos, pirkšanas pasūtījumos vai brīva teksta rēķinos. Tomēr, sagatavojot primārās grāmatas darbības žurnālā Pamatlīdzekļi, atvasināto darbību summas var skatīt un modificēt pirms to grāmatošanas.
-   Noteikti konti, piemēram, PVN un debitoru vai kreditoru konti, tiek atjaunināti tikai vienreiz ar primārās grāmatas grāmatojumiem. Atvasinātās grāmatas darbības tiek grāmatotas kontos, kas definēti atvasinātajai grāmatai lapā Pamatlīdzekļu grāmatošanas metodes.
-   Iegāde bieži tiek lietota kā atvasināto grāmatu darbības tips. To lieto, ja pamatlīdzeklim nepieciešams pielietot grāmatu un atvasināto grāmatu, sākot no pamatlīdzekļa iegādes datuma.
-   Uz darbības tipu var attiekties arī citas vērtības. Piemēram, ja primārajai grāmatai un atvasinātajām grāmatām ir vienādi pārdošanas vai izslēgšanas intervāli, visi pamatlīdzekļu darbību tipi ir pieejami atvasinātās grāmatas iestatīšanai.

> [!WARNING]
> Atvasinātajā grāmatā iegrāmatotā nolietojuma summa ir tāda pati kā primārajā grāmatā iegrāmatotā summa. Ja nolietojuma metodes atšķiras starp grāmatām, nedrīkst ģenerēt nolietojuma darbības, lietojot atvasinātu procesu. |

## <a name="example"></a>Paraugs 
Tālāk sniegtajā informācijā ir aprakstīts, kā iestatīt iegādes darbības, izmantojot atvasinātās grāmatas funkcionalitāti.

1.  Izveidojiet grāmatas lapā Grāmatas.
    -   Grāmata uzskaitei: 1. VM, pašreizējais grāmatošanas līmenis
    -   Grāmata nodokļu aprēķinam: 2. VM, nodokļu grāmatošanas līmenis

2.  1. VM, noklikšķiniet uz cilnes Atvasinātas grāmatas. Laukā Grāmata atlasiet 2. VM un laukā Darbības tips atlasiet Iegāde.

Pēc tam grāmatas var pievienot specifiskiem pamatlīdzekļiem. 

Grāmatojot pamatlīdzekļa iegādi, izmantojot grāmatu 1. VM, iegāde tiek grāmatota ne tikai grāmatā 1. VM, bet arī atvasinātajā grāmatā 2. VM. Abu pamatlīdzekļu grāmatu statuss tiek mainīts uz Atvērts.

> [!NOTE]                                                                                                         
> Ja atvasinātās grāmatas netiek lietotas, pamatlīdzekļa iegāde jāgrāmato gan grāmatai 1. VM, gan grāmatai 2. VM.

Papildu informāciju skatiet tēmā [Atvasinātās grāmatas](derived-books.md).



