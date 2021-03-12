---
title: Izejošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993982"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Izejošo noliktavas operāciju problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas izejošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Tiek parādīts šāds kļūdas ziņojums: "Pārdošanas pasūtījumu nevarēja izlaist."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma var rasties vairāku iemeslu dēļ. Piemēram, pasūtījums ir kredīta pārvaldības aizturēšana, un nevienu sūtījumu nevar izveidot, kamēr nav ievadīta derīga pasta adrese visām pārdošanas rindām, kas ir saistītas ar pārdošanas pasūtījumu. Pretējā gadījumā ir paredzēta pasūtījuma aizturēšana, kas jāadresē, lai pasūtījumu varētu nodot izpildei noliktavā. Šis aizturējums var būt specifisks pasūtījumam, vai tas var būt klienta kontā.

### <a name="issue-resolution"></a>Problēmas risinājums

Pievienojiet vai atjauniniet adresi pārdošanas pasūtījumā un pasūtījuma rindās un pēc tam izlaidiet pasūtījumu uz noliktavu. Pasūtījumus var izlaist noliktavā tikai tad, ja tiem ir derīga piegādes adrese (katram adreses formāta iestatījumam **Organizācijas administrēšanas** modulī).

Izmeklējiet pasūtījuma aizturēšanu un risināt šos jautājumus. Pēc tam noņemiet aizturēšanu no pasūtījuma vai klienta un izlaidiet pasūtījumu uz noliktavu.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Tiek saņemts šāds ziņojums: "Sūtījums kravai 1% ir apstiprināts." Tomēr neviena rinda netiek grāmatota.

### <a name="issue-description"></a>Problēmas apraksts

Sūtījums tika apstiprināts kravā, bet nav notikusi grāmatošana.

### <a name="issue-resolution"></a>Problēmas risinājums

Sūtījuma apstiprināšana neietekmē grāmatošanu. Tas tikai atjaunina sūtījuma un kravas statusu. Grāmatošanai jābūt atsevišķā procesā.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Tiek parādīts šāds kļūdas ziņojums: "Tieša nosūtīšana nevar apstrādāt noliktavas 1%, jo tajā ir iespējota noliktavas pārvaldība. Lūdzu, norādiet citu noliktavu, kas nav iespējota noliktavas pārvaldībai."

### <a name="issue-description"></a>Problēmas apraksts

Krājums tiek pievienots pārdošanas rindai tiešajai piegādei no noliktavas, kas ir aktivizēta noliktavas pārvaldībai (WMS). Šis kļūdas ziņojums tiek parādīts, atjauninot pārdošanas rindu. 

### <a name="issue-resolution"></a>Problēmas risinājums

Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Pašlaik WMS neatbalsta tiešo piegādi. Tāpēc, lai izmantotu tiešo piegādi, jāatlasa WMS krājums un noliktava.
