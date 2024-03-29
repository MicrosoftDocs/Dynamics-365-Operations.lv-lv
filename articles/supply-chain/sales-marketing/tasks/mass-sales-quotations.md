---
title: Veidot pārdošanas piedāvājumus masveidā
description: Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acb2b49c7cb2024aec1140d04150bd1ab9d75c14
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573373"
---
# <a name="mass-create-sales-quotations"></a>Veidot pārdošanas piedāvājumus masveidā

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem. Šo masveida piedāvājumu izveide ir balstīta uz piedāvājumu veidnēm. Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.


## <a name="create-a-quotation-template"></a>Piedāvājuma veidnes izveidošana
1. Dodieties uz sadaļu Pārdošana un mārketings > Iestatījumi > Piedāvājumi > Veidņu grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Grupas ID ierakstiet ID pēc savas izvēles.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.
7. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.
8. Noklikšķiniet uz Jauns.
9. Laukā Konta veids atlasiet Debitors.
10. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz OK.
    * Lai piedāvājumu pārveidotu par veidni, ir jāveic iestatīšanas darbības piedāvājuma virsrakstā. Tas jādara pirms rindu pievienošanas piedāvājumā.   
12. Darbību rūtī noklikšķiniet uz Opcijas.
13. Noklikšķiniet uz Mainīt skatījumu.
14. Noklikšķiniet uz Virsraksta skatījuma.
15. Izvērsiet sadaļu Iestatīšana.
16. Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.
17. Ierakstiet vērtību laukā Veidnes nosaukums.
18. Laukā Aktīvs atlasiet Jā.
    * Lietojot veidni jaunam pārdošanas piedāvājumam, var izmantot tikai aktīvās veidnes.  
19. Darbību rūtī noklikšķiniet uz Opcijas.
20. Noklikšķiniet uz Mainīt skatījumu.
21. Noklikšķiniet uz Rindas skats.
22. Laukā Krājums ievadiet vai atlasiet kādu vērtību.
23. Laukā Krājums ierakstiet vērtību.
24. Aizvērt lapu.
25. Laukā Atlaides procents ievadiet skaitli.
26. Noklikšķiniet uz Pievienot rindu.
27. Laukā Krājums ievadiet vai atlasiet kādu vērtību.
28. Laukā Krājums ierakstiet vērtību.
29. Aizvērt lapu.
30. Laukā Vienības cena ievadiet jaunu cenu vai mainiet pašreizējo vērtību.
31. Noklikšķiniet uz Pievienot rindu.
32. Laukā Krājums ievadiet vai atlasiet kādu vērtību.
33. Laukā Krājums ierakstiet vērtību.
34. Aizvērt lapu.
35. Laukā Daudzums ievadiet skaitli.
36. Laukā Atlaide ievadiet skaitli.
37. Noklikšķiniet uz Saglabāt.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Veidnes izmantošana viena piedāvājuma izveidei
1. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.
    * Ievērojiet, ka jūsu tikko izveidotais piedāvājums ir atzīmēts kā veidne.  
2. Noklikšķiniet uz Jauns.
3. Laukā Konta veids atlasiet Debitors.
4. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
5. Izvērsiet sadaļu Veidne.
6. Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.
7. Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.
8. Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.
9. Noklikšķiniet uz OK.
    * Ir izveidots jaunais piedāvājums, pamatojoties uz veidnes datiem un nosacījumiem.  
10. Aizvērt lapu.
11. Aizvērt lapu.

## <a name="apply-the-template-to-mass-create-quotations"></a>Veidnes izmantošana piedāvājumu veidošanai masveidā
1. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Piedāvājuma atjaunināšana > Masveida piedāvājumu izveide.
2. Laukā Konta veids atlasiet Debitors.
3. Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.
4. Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.
5. Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.
6. Izvērsiet sadaļu Iekļaujamie ieraksti.
7. Noklikšķiniet uz Filtrēt.
8. Laukā Kritērijs iestatiet filtru, lai aptvertu tādu debitoru diapazonu, kurus vēlaties iekļaut šajā masveida piedāvājumu izveidē. Izmantojiet šādu formātu: "Customer1..CustomerN".
    * Piemēram, varat iestatīt filtru šādi: US-001..US-004  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz OK.
11. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.
    * Pārbaudiet, vai piedāvājumi ir izveidoti visiem debitoriem, kas norādīti masveida atjaunināšanas kārtībā, pamatojoties uz atlasīto veidni.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]