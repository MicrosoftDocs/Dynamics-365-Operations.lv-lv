---
title: Sūtījumu krājumu īpašumtiesību maiņa, pamatojoties uz ražošanas pieprasījumu
description: Šajā procedūrā parādīts kā nomainīt sūtījuma krājumu īpašnieku no kreditora uz jūsu juridisko personu, ja ražošanā ir pieprasījums pēc krājuma.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433048"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Sūtījumu krājumu īpašumtiesību maiņa, pamatojoties uz ražošanas pieprasījumu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts kā nomainīt sūtījuma krājumu īpašnieku no kreditora uz jūsu juridisko personu, ja ražošanā ir pieprasījums pēc krājuma. Šī īpašumtiesību maiņa notiek, izveidojot un grāmatojot krājumu īpašumtiesību izmaiņu žurnālu. Īpašumtiesību izmaiņu žurnāla rindas var izveidot manuāli, vai, kā norādīts šajā ierakstā, pamatojoties uz esošo ražošanas pieprasījumu. Parasti ražotnes vadītājs veic šo uzdevumu. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat savus datus, pārliecinieties, ka ir izpildīti šādi priekšnosacījumi: krājumu žurnāla nosaukums, kas ir iestatīta krājumu īpašumtiesību izmaiņai, fiziski reģistrēti kreditoram piederoši rīcībā esoši krājumi, un viena vai vairākas ražošanas pasūtījuma rindas materiālam. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

> [!NOTE]
> Ārējo sūtījumu procesi netiek atbalstīti iebūvētajā versijā, un automātiskā īpašumtiesību žurnāla apstrāde netiek atbalstīta.

## <a name="create-an-inventory-ownership-journal"></a>Izveidot krājumu īpašumtiesību žurnālu
1. Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Krājumu īpašumtiesību izmaiņas.
2. Noklikšķiniet uz Jauns.
    * Krājumu īpašumtiesību izmaiņu žurnāls tiek izmantots, lai mainītu sūtījuma krājumu īpašnieku no kreditora uz pašreizējo juridisko personu. Šī īpašnieka maiņa tiek veikta, nododot rīcībā esošos krājumus, kas pieder kreditoram, un pēc tam saņemot šos krājumus pašreizējā juridiskajā personā.  
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
    * Jūs varat atlasīt tikai krājumu žurnālu nosaukumus ar žurnāla tipu Īpašumtiesību izmaiņa.  
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Funkcijas.
6. Noklikšķiniet uz Izveidot žurnāla rindas no ražošanas pasūtījumiem.
    * Jūs varat sākt īpašumtiesību izmaiņas procesu, nosūtot vaicājumu visām ražošanas līnijām, kurām ir patēriņa izejvielu pieprasījums.  
7. Laukā Ietveramie krājumu izejas plūsmu statusi atlasiet opciju.
    * Šī iespēja ļauj filtrēt pēc krājumu darbību izejas plūsmas statusa. Piemēram, jūs varat izveidot žurnāla rindas krājumiem ar statusiem Izdots un fiziski rezervēts.  
8. Izvērsiet sadaļu Iekļaujamie ieraksti.
    * Šī sadaļa ļauj jums pielietot papildu filtrēšanu. Piemēram, jūs varat atlasīt noteiktu izejmateriālu reģistrēšanas datumu.  
9. Noklikšķiniet uz OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Grāmatot krājumu īpašumtiesību izmaiņu žurnālu
1. Noklikšķiniet uz Grāmatot.
    * Kad žurnāls ir grāmatots, kreditora krājumi tiek nodoti, izmantojot atsauci "Īpašumtiesību maiņa”. Krājumi tiek saņemti kā rīcībā esoši, izmantojot krājuma darbību, kas tiek atjaunināta ar pirkšanas pasūtījuma produktu ieejas plūsmu. Ņemiet vērā, ka tiek izveidotas tikai darbības, kas ir saistītas ar grāmatoto žurnālu. Netiek izveidotas nekādas paredzētās Krājumu darbības.  
2. Noklikšķiniet uz OK.
3. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]