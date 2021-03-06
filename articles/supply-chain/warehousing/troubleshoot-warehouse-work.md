---
title: Noliktavas darba problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas darbu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837445"
---
# <a name="troubleshoot-warehouse-work"></a>Noliktavas darba problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas darbu programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Nevar pārvietot numura zīmes, kurām ir sērijas numura krājumi, ja izsekošanas dimensiju grupā ir atļautas tukšas izejas un ieejas plūsmas.

### <a name="issue-description"></a>Problēmas apraksts

Numura zīmi nevar pārvietot, izmantojot **Kustības** izvēlnes elementu, ja sērijas numuram ir atļauti *Tukši izejas plūsmas* un *Tukši ieejas plūsmas* iestatījumi izsekošanas dimensiju grupā, un, ja vienā un tajā pašā vietā ir vairākas numura zīmes, dažām, no kurām ir sērijas numuri, un dažām, no kurām nav.

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma tiks labota ar izmaiņām, kas izvietotas [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Šīs izmaiņas padarīs **Sērijas numura** lauku neobligātu, ja ir atļautas tukšas ieejas plūsmas un tukšas izejas plūsmas.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Kad es apstrādāju kustības, es saņemu šādu kļūdas ziņojumu programmā Warehouse Management mobile: "Noliktavas īpašnieks %1 nav atļauts šajā procesā."

### <a name="issue-description"></a>Problēmas apraksts

Kad tiek izmantota Warehouse Management mobile programma, lai veiktu kustības, trūkst **Īpašnieka** izsekošanas dimensijas. Regulārs krājumu pārsūtīšanas žurnāls no Supply Chain Management klienta tiek rādīts, lai darbotos, kā paredzēts, un to var grāmatot tikai tad, ja ir ievadīta **Īpašnieka** dimensija.

### <a name="issue-resolution"></a>Problēmas risinājums

Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Pašlaik noliktavas pārvaldības procesi atbalsta tikai tos krājumus, kas pieder juridiskai personai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]