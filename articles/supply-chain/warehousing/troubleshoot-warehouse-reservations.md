---
title: Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645124"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.

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

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Tiek parādīts šāds kļūdas ziņojums: "Jāpiešķir kopumam, noslodzes rindām ir jānorāda dimensijas virs novietojuma. Lai piešķirtu šīs dimensijas, rezervējiet un atkārtoti izveidojiet noslodzes rindu."

### <a name="issue-description"></a>Problēmas apraksts

Kad izmantojat krājumu, kam ir "partija virs" rezervāciju hierarhija (ar **Partijas numura** dimensiju, kas novietota *virs* **Novietojuma** dimensijas), **Izlaist uz noliktavu** komanda lapā **Kravas plānošanas rīks** daļējam daudzumam nestrādā. Šis kļūdas ziņojums tiek parādīts, un nav izveidots neviens darbs daļējam daudzumam.

Tomēr, ja izmantojat krājumu, kam ir "partija zem" rezervāciju hierarhija (ar **Partijas numura** dimensiju, kas novietota *zem* **Novietojuma** dimensijas), varat izlaist kravu no lapas **Kravas plānošanas rīks** daļējam daudzumam.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Ja jūs ievietojat dimensiju virs **Novietojuma** dimensijas rezervāciju hierarhijā, tas ir jānorāda pirms izdošanas uz noliktavu. Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums laikā, kad tiek veikti izsniegumi uz noliktavu no kravas plānošanas rīka. Daļējus daudzumus nevar izlaist, ja nav norādīta viena vai vairākas dimensijas virs **Novietojuma**.

Papildu informāciju skatiet [Elastīga noliktavas līmeņa dimensijas rezervēšanas politika](flexible-warehouse-level-dimension-reservation.md).
