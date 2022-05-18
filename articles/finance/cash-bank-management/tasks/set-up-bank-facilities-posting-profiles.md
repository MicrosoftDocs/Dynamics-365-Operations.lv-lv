---
title: Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili
description: Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3568332a7755af9c8c341223fc7ef7e66a1da02
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726327"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili

[!include [banner](../../includes/banner.md)]

Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.



Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF. 




## <a name="general-ledger-parameter"></a>Virsgrāmatas parametrs
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.
2. Izvērsiet sadaļu Bankas dokuments.
3. Atlasiet opciju Iespējot garantijas vēstuli.
4. Laukā Darbību žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz cilnes Numuru sērijas.
    * Numuru sērijas koda definēšana garantijas vēstules numuram un garantijas vēstuļu transakciju atsaucēm  
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.

## <a name="create-bank-facility"></a>Bankas iestādes izveide
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas iestādes.
2. Noklikšķiniet uz Jauns.
3. Laukā Iestādes grupa ievadiet bankas iestāžu grupas nosaukumu garantijas vēstules transakcijai.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz cilnes Iestādes tipi.
7. Noklikšķiniet uz Jauns.
8. Laukā Iestādes tips ievadiet tā bankas iestāžu tipa nosaukumu, kas saistīts ar bankas iestādes līgumu.
9. Laukā Apraksts ierakstiet kādu vērtību.
10. Laukā Iestādes grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā Iestādes būtība atlasiet opciju.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.

## <a name="bank-posting-profile"></a>Bankas grāmatošanas profils
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas dokumentu grāmatošanas metode.
2. Noklikšķiniet uz Jauns.
3. Laukā Konta/grupas numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Apmaksāt konta rēķinus atlasiet galveno norēķinu kontu.
7. Laukā Maksājumu konts atlasiet kontu izdevumu transakcijām.
8. Laukā Uzcenojuma konts atlasiet kontu uzcenojuma transakcijai.
9. Laukā Likvidācijas konts atlasiet likvidācijas kontu garantijas vēstules transakcijai. 
10. Klikšķiniet Saglabāt.
11. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
