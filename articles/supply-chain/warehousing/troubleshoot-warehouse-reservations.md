---
title: Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773109"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.

Tēmām, kas ir saistītas ar pakešu un sēriju numuru reģistrācijām, skatiet informāciju par [Noliktavas pakešuzdevumu un sēriju rezervāciju hierarhiju problēmu novēršanu](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Tiek atgriezta sekojošā kļūda: “Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju.”

### <a name="issue-description"></a>Problēmas apraksts

Pārdošanas rindā nevar atrezervēt krājumus, jo uz šo rindu ir atvērts darbs.

### <a name="issue-resolution"></a>Problēmas risinājums

Izpētiet, vai ir atvērts pakošanas grupas darbs, lai atgrieztu krājumu no iepakošanas stacijas uz citu vietu (piemēram, *Baydoor*). Pārskatiet ierakstus lapās **Darba izveides vēstures žurnāls** un **Darba informācija**, lai noteiktu, kas fiziski rezervē krājumus, un pēc tam pabeidziet vai dzēsiet darbu, lai atbrīvotu rezervāciju.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Tiek parādīts šāds kļūdas ziņojums: "Krājumu daudzums - %1 nevarēja atjaunināt, jo krājumam %2 ir nepietiekamu krājumu darbību...."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas. Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:

> Krājumu daudzums -%1 nevarēja atjaunināt %2 krājumu darbību nepietiekamā daudzuma dēļ, kas atbilst dimensijas Lielumam=%3, Krāsai=%4, Papildinājumiem=%5, Vietai=%6, Noliktavai=%7, Novietojumam=%8, Krājuma statusam=pieejams, Numura zīmei=%9, Partijas numuram=%10, Atsauces ID %11, Laidien ID %12.

### <a name="issue-resolution"></a>Problēmas risinājums

Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu. Piemēram, šīs darbības var atvērt kvalitātes pasūtījumus, krājumu bloķēšanas ierakstus vai izdošanas pasūtījumus.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Tiek parādīts šāds kļūdas ziņojums: "Fiziski rīcībā esošo...nevar rezervēt, jo krājumos ir pieejams tikai 0,00."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas. Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:

> Fiziskais rīcībā esošais Vietne=%1, Noliktava=%2, Krājumu statuss=pieejams, Partijas numurs=%3, Īpašnieks=%4: %5 nevar rezervēt, jo krājumos ir pieejamas tikai 0,00.

### <a name="issue-resolution"></a>Problēmas risinājums

Šo problēmu, iespējams, izraisa atvērts darbs. Vai nu pabeidziet darbu, vai saņemiet bez darba izveides. Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu. Piemēram, šīs darbības var būt atvērti kvalitātes pasūtījumi, krājumu bloķēšanas ieraksti vai izdošanas pasūtījumi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
