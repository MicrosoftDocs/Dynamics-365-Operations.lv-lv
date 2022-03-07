---
title: Nevar pārvietot numura zīmi, ja ir atļauta tukša izejas plūsma un tukša ieejas plūsma
description: Nevarat pārvietot numura zīmi, ja sērijas numuram ir atļauta tukša izejas plūsma un tukša ieejas plūsma. To var novērst, padarot sērijas numura lauku par neobligātu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476976"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Nevarat pārvietot numura zīmi, ja sērijas numuram ir atļauta tukša izejas plūsma un tukša ieejas plūsma.

## <a name="symptoms"></a>Simptomi

Nevarat pārvietot numura zīmi, izmantojot izvēlnes elementu **Pārvietošana**, ja sērijas numuram izsekošanas dimensijas grupā ir iestatījumi *Tukša izejas plūsma atļauta* un *Tukša ieejas plūsma atļauta* un ja ir vairākas numuru zīmes vienā atrašanās vietā, no kurām dažām ir sērijas numurs, bet dažām nav.

## <a name="resolution"></a>Novēršana

Šī problēma tiks labota ar izmaiņām, kas izvietotas [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Ar šīm izmaiņām lauks **Sērijas numurs** kļūs par neobligātu, ja būs atļauta tukša ieejas un izejas plūsma.
