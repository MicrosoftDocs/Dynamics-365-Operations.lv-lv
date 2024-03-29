---
title: Atgādinājuma vēstules secības izveide
description: Izmantojiet šo procedūru, lai izveidotu atgādinājuma vēstuļu sēriju.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734163"
---
# <a name="create-a-collection-letter-sequence"></a>Atgādinājuma vēstules secības izveide

[!include [banner](../../includes/banner.md)]

Izmantojiet šo procedūru, lai izveidotu atgādinājuma vēstuļu sēriju. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz **Sadaļu Kredīts un >, > iestatīt atgādinājuma vēstuļu sēriju**.
2. Klikšķiniet **Jauns**.
3. Laukā **Atgādinājuma vēstuļu sērija** ievadiet sērijas ID, kas pārstāvēs sēriju. Tas tiks izmantots, kad iestatīsit grāmatošanas metodi.
4. Laukā **Apraksts** ierakstiet kādu vērtību. Maksāšanas nosacījumi nav obligāti. Ja ievadāt vērtību šeit, atgādinājuma vēstules papildmaksas rēķinā tiks izmantoti šie maksāšanas nosacījumi, nevis debitoram saglabātie maksāšanas nosacījumi.  
5. Laukā **Atgādinājuma vēstules kods** atlasiet kodu pirmajai atgādinājuma vēstulei, ko vēlaties nosūtīt. Pirmā atgādinājuma vēstule tiek izveidota atbilstoši rēķina apmaksas termiņam, vērtībai, ko šai rindai ievadāt pagarinājuma periodam laukā Dienas, un atbilstoši citai informācijai, ko ievadāt šai rindai.  
6. Laukā **Apraksts** ierakstiet kādu vērtību. 
7. Papildmaksas noklusētā valūta ir juridiskas personas valūta. Šis valūtas kods var atšķirties no rēķina valūtas.   
8. Noklikšķiniet uz **Pievienot**, lai pievienotu nākamo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā. Daudzos gadījumos pirmā atgādinājuma vēstule ir tikai brīdinājums. Varat pievienot papildmaksas, ja tādas nepieciešamas.  
9. Laukā **Atgādinājuma vēstules kods** atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.
10. Laukā **Galvenais konts** atlasiet ieņēmumu kontu, kas tiks izmantots papildmaksām.
11. Ievadiet papildmaksu, kas jāattiecina, grāmatojot šo atgādinājuma vēstuli.
12. Laukā **Krājumu PVN grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. Atlasiet krājuma PVN grupu, ja papildmaksai jāaprēķina PVN.  
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Laukā **Minimālais nokavētais atlikums** ievadiet minimālo nokavējuma bilanci, kas nepieciešama pirms inkasācijas vēstules nosūtīšanas.
15. Laukā **Dienas** ievadiet pieļaujamo pagarinājuma dienu skaitu. Šis ir dienu skaits pēc apmaksas datuma, pēc kuru paiešanas var tikt ģenerēta atgādinājuma vēstule. Termiņš, kas tiek izmantots aprēķinam, ir atkarīgs no atgādinājuma vēstules pozīcijas atgādinājuma vēstuļu sērijā:
    - Pagarinājuma periods 1. atgādinājuma vēstulē tiek noteikts pēc rēķina apmaksas datuma.
    - Pagarinājuma periods 2. atgādinājuma vēstulei un turpmākām vēstulēm tiek noteikts pēc datuma, kad iepriekšējā atgādinājuma vēstule tikusi iegrāmatota vai izdrukāta, atkarībā no atlases laukā Atjaunināt atgādinājuma vēstules kodu lapā Debitoru parādu parametri.  
16. Noklikšķiniet uz **Pievienot**, lai pievienotu pēdējo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā. Atgādinājuma vēstuļu sērijai varat pievienot līdz pieciem atgādinājuma vēstuļu kodiem.  
17. Laukā **Atgādinājuma vēstules kods** atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.
18. Laukā **Apraksts** ierakstiet kādu vērtību.
19. Laukā **Galvenais konts** norādiet vēlamās vērtības.
20. Ievadiet skaitli laukā **Papildmaksas valūta**.
21. Laukā **Krājumu PVN grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
22. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
23. Ievadiet skaitli laukā **Minimālā nokavētā bilance**.
24. Ievadiet skaitli laukā **Dienas**.
25. Atlasiet izvēles rūtiņu **Bloķēt**, lai apturētu papildu piegādes un rēķinu piesūtīšanu klientam. Lai atbloķētu kodu, debitoru **lapas** **laukā Rēķina izrakstīšana un piegāde** aizturēta atlasiet **Nē**.  
26. Izvērsiet kopsavilkuma cilni **Piezīme**.
27. Ievadiet tekstu, kuru saturēs atgādinājuma vēstules ar atlasīto atgādinājuma vēstuļu kodu. Šo tekstu var tulkot vairākās valodās, izmantojot **tulkojumu izvēlni** virs piezīmes lodziņa.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
