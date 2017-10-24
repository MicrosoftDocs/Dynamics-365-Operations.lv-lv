--- 
title: "Atgādinājuma vēstules secības izveide"
description: "Izmantojiet šo uzdevumu ceļvedi, lai izveidotu atgādinājuma vēstuļu sēriju."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-collection-letter-sequence"></a>Atgādinājuma vēstules secības izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo uzdevumu ceļvedi, lai izveidotu atgādinājuma vēstuļu sēriju. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Iestatīt atgādinājuma vēstuļu secību.
2. Noklikšķiniet uz Jauns.
3. Laukā Atgādinājuma vēstuļu sērija ievadiet sērijas ID, kas pārstāvēs sēriju. Tas tiks izmantots, kad iestatīsit grāmatošanas metodi.
4. Apraksta laukā ierakstiet vērtību.
    * Maksāšanas nosacījumi nav obligāti. Ja ievadāt vērtību šeit, atgādinājuma vēstules papildmaksas rēķinā tiks izmantoti šie maksāšanas nosacījumi, nevis debitoram saglabātie maksāšanas nosacījumi.  
5. Laukā Atgādinājuma vēstules kods atlasiet kodu pirmajai atgādinājuma vēstulei, ko vēlaties nosūtīt.
    * Pirmā atgādinājuma vēstule tiek izveidota atbilstoši rēķina apmaksas termiņam, vērtībai, ko šai rindai ievadāt pagarinājuma periodam laukā Dienas, un atbilstoši citai informācijai, ko ievadāt šai rindai.  
6. Apraksta laukā ierakstiet vērtību.
    * Papildmaksas valūta pēc noklusējuma tiek ņemta no debitora valūtas norādes. Šis valūtas kods var atšķirties no rēķina valūtas.  
7. Noklikšķiniet uz Pievienot, lai pievienotu nākamo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā
    * Daudzos gadījumos pirmā atgādinājuma vēstule ir tikai brīdinājums. Varat pievienot papildmaksas, ja tādas nepieciešamas.  
8. Laukā Atgādinājuma vēstules kods atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.
9. Laukā Apraksts ierakstiet kādu vērtību.
10. Laukā Galvenais konts atlasiet ieņēmumu kontu, kas tiks izmantots papildmaksām.
11. Ievadiet papildmaksu, kas jāattiecina, grāmatojot šo atgādinājuma vēstuli.
12. Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet krājuma PVN grupu, ja papildmaksai jāaprēķina PVN.  
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Ievadiet minimālo kavējuma bilanci, kuru nepieciešams sasniegt pirms atgādinājuma vēstules nosūtīšanas.
15. Ievadiet pieļaujamo pagarinājuma dienu skaitu.
    * Šis ir dienu skaits pēc apmaksas datuma, pēc kuru paiešanas var tikt ģenerēta atgādinājuma vēstule. Aprēķinos izmantotais apmaksas datums ir atkarīgs no atgādinājuma vēstules pozīcijas atgādinājuma vēstuļu secībā: ⦁ 1. atgādinājuma vēstules pagarinājuma periods ir saistīts ar rēķinā norādīto apmaksas termiņu.  ⦁ 2. un turpmāko atgādinājuma vēstuļu pagarinājuma periods ir saistīts ar datumu, kurā atkarībā no atlases lapas Debitoru parādu parametri laukā Atjaunināt atgādinājuma vēstules kodu ir iegrāmatota vai izdrukāta iepriekšējā atgādinājuma vēstule.  
16. Noklikšķiniet uz Pievienot, lai pievienotu pēdējo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā.
    * Atgādinājuma vēstuļu sērijai varat pievienot līdz pieciem atgādinājuma vēstuļu kodiem.  
17. Laukā Atgādinājuma vēstules kods atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.
18. Laukā Apraksts ierakstiet kādu vērtību.
19. Laukā Galvenais konts norādiet vēlamās vērtības.
20. Ievadiet skaitli laukā Papildmaksas valūta.
21. Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
22. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
23. Ievadiet skaitli laukā Minimālā nokavētā bilance.
24. Ievadiet skaitli laukā Dienas.
25. Atzīmējiet šo izvēles rūtiņu, lai apturētu papildu piegādes un rēķinu piesūtīšanu klientam.
    * Lai kontu atbloķētu, rēķinu izrakstīšanā atlasiet Nē un debitoru lapā atlasiet piegādes aizturēšanas lauku.  
26. Izvērsiet kopsavilkuma cilni Piezīme.
27. Ievadiet tekstu, kuru saturēs atgādinājuma vēstules ar atlasīto atgādinājuma vēstuļu kodu.
    * Varat iztulkot šo tekstu vairākās valodās, izmantojot izvēlni Tulkojumi, kas atrodas virs piezīmes lodziņa.  


