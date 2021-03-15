---
title: Vienības izmaksu cena un atgrieztā laidiena ID
description: Iespējams, vēlēsities, lai atgriezto preču izmaksas būtu vienādas ar preču izmaksām brīdī, kad pārdevāt preces debitoram. To var izdarīt, izmantojot **Atgrieztā laidiena ID**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eff30383e06677793313e8abac0339c6032c2a7f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965834"
---
# <a name="return-cost-price-and-return-lot-id"></a>Vienības izmaksu cena un atgrieztā laidiena ID        

[!include [banner](../includes/banner.md)]



Krājumos atgriezto preču izmaksas aprēķina, izmantojot pašreizējās preču izmaksas. Tomēr, iespējams, vēlēsities, lai atgriezto preču izmaksas būtu vienādas ar preču izmaksām brīdī, kad pārdevāt preces debitoram. To var izdarīt, izmantojot lauku **Atgrieztā laidiena ID** veidlapas **Pārdošanas pasūtījums** kopsavilkuma cilnē **Detalizēta informācija par rindu**.

Piemēram, aplūkosim šādu scenāriju. Jūs izrakstāt debitoram rēķinu. Pēc tam debitors atgriež jums piegādātās preces. Jūs atgriežat preces krājumos. Šādā gadījumā, kreditējot debitoru par atgrieztajām precēm, šo preču izmaksas aprēķina, izmantojot pašreizējās preču izmaksas. Tomēr, ja izmantojat lauku **Atgrieztā laidiena ID**, atgriezto preču izmaksas tiek aprēķinātas, izmantojot izmaksas, kas norādītas sākotnējās pārdošanas debitora rēķinā.

Lai atgriešanai no debitora izmantotu citas izmaksas, nevis pašreizējās izmaksas, lietojiet kādu no šīm metodēm.

## <a name="method-1-manually-enter-the-return-cost-price"></a>1. metode. Manuāla vienības izmaksu cenas ievadīšana

Pēc noklusējuma, pievienojot krājumus atgriešanas pasūtījumam, tie tiek atgriezti krājumos pašreizējā izmaksu cenā. Lai norādītu citu vienības izmaksu cenu, rīkojieties šādi.

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  **Darbību rūts** grupā **Jauns** noklikšķiniet uz **Atgriešanas pasūtījums**.

3.  Veidlapā **Izveidot atgriešanas pasūtījumu** atlasiet debitora kontu un pēc tam noklikšķiniet uz **Labi**.

4.  Formā **Atgriešanas pasūtījums — AKA kods: %1, %2** atlasiet krājumu un pēc tam ievadiet negatīvu daudzumu laukā **Daudzums**.

5.  Noklikšķiniet uz kopsavilkuma cilnes **Detalizēta informācija par rindu**.

6.  Cilnē **Vispārīgi** ievadiet vērtību laukā **Vienības izmaksu cena**. Šī vērtība tiek izmantota, kad preces tiek atgrieztas krājumos. Ja neievadāt vērtību, atgriežot preces krājumos, tiek izmantota pašreizējā izmaksu cena.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>2. metode. Izmaksu cenas automātiska ģenerēšana, pamatojoties uz debitora rēķina rindu

Atgriešanas rindu izveidei vēlams izmantot šo metodi. Lai izmantotu preču izmaksas brīdī, kad pārdevāt preces debitoram, izveidojiet atgriešanas pasūtījumu un norādiet atgriežamo pārdošanas rindu.

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  **Darbību rūts** grupā **Jauns** noklikšķiniet uz **Atgriešanas pasūtījums**.

3.  Veidlapā **Izveidot atgriešanas pasūtījumu** atlasiet debitora kontu un pēc tam noklikšķiniet uz **Labi**.

4.  Formas **Atgriešanas pasūtījums — AKA kods: %1, %2**, sadaļā **Darbību rūts** noklikšķiniet uz vienuma **Atrast pārdošanas pasūtījumu**.

5.  Veidlapā **Atrast pārdošanas pasūtījumu** atlasiet atgriežamo rēķina rindu un pēc tam noklikšķiniet uz **Labi**.
    
    Kopsavilkuma cilnes **Detalizēta informācija par rindu** cilnes **Vispārīgi** laukā **Atgrieztā laidiena ID** ir parādīta vērtība no sākotnējās pārdošanas rindas. Turklāt laukā **Vienības izmaksu cena** tiek parādīta izmaksu vērtība no sākotnējās pārdošanas rindas.

## <a name="cost-calculation-example"></a>Izmaksu aprēķina piemērs

Ja izmantojat lauku **Atgrieztā laidiena ID** atgriešanas pasūtījuma rindā, lai norādītu vienības izmaksu cenu, tiek izmantotas izmaksas atgriešanas pasūtījuma rindā. Ja tiek izmantota krājumu slēgšanas vai pārrēķināšanas funkcionalitāte, izmaksas tiek koriģētas sākotnējā pārdošanas rindā. Izmaksas preču atgriešanas pasūtījuma rindā tiek automātiski koriģētas, lai atspoguļotu tādas pašas izmaksas par gabalu.

1.  Izveidojiet un izlaidiet preci, kuras nosaukums ir Pārbaude. Veidlapā **Detalizēta informācija par izlaistajām precēm** norādiet šādu informāciju:
    
    1.  Kopsavilkuma cilnes **Pārvaldīt izmaksas** laukā **Krājumu grupa** atlasiet grupu **Daļas**.
    
    2.  Kopsavilkuma cilnes **Vispārīgi** laukā **Krājumu modeļu grupa** atlasiet vienumu **DEF**.
    
    3.  Kopsavilkuma cilnē **Pirkšana** laukā **Cena** ierakstiet vērtību 10,00 kā krājuma izmaksu cenu.
    
    4.  **Darbību rūtī** noklikšķiniet uz **Dimensiju grupas**. Laukā **Noliktavas dimensiju grupa** atlasiet **Tikai Vieta un Noliktava**. Laukā **Izsekošanas dimensiju grupa** atlasiet **Nav aktīvu izsekošanas dimensiju**.

2.  Izveidojiet pirkšanas pasūtījumu 10 gabaliem pārbaudāmā krājuma ar cenu 6,00 par gabalu un pēc tam grāmatojiet pirkšanas pasūtījuma rēķinu.
    
    Izveidojiet otro pirkšanas pasūtījumu 10 gabaliem pārbaudāmā krājuma ar cenu 8,00 par gabalu un pēc tam grāmatojiet pirkšanas pasūtījuma rēķinu.

3.  Grāmatojiet pārdošanas pasūtījuma rēķinu par piecu pārbaudes krājuma gabalu pārdošanu.
    
    Šajā gadījumā pārdošanas pasūtījuma rindas izmaksas ir 35,00 (5 gabali \* 7,00 vidējās izmaksas par gabalu).

4.  Izveidojiet atgriešanas pasūtījumu debitoram. Veidlapā **Atrast pārdošanas pasūtījumu** atlasiet rēķina rindu un pēc tam noklikšķiniet uz **Labi**.

5.  Formā **Atgriešanas pasūtījums — AKA kods: %1, %2** pārbaudiet, vai ir ģenerēts atgriešanas pasūtījums, lai atgrieztu pārbaudes krājumu. Atgriešanas pasūtījuma iestatītais daudzums ir -5,00.
    
    Laukā **Atgrieztā laidiena ID** tiek parādīts laidiena ID. Šis laidiena ID tiek ņemts no debitoram pārdotā krājuma sākotnējā pārdošanas pasūtījuma. Laukā **Vienības izmaksu cena** tiek parādīta izmaksu cena no sākotnējās pārdošanas rindas.

6.  Reģistrējiet atgrieztu krājumu saņemšanu.

7.  Grāmatojiet pavadzīmi atgrieztajiem krājumiem.

8.  Iegrāmatojiet rēķinu atgriešanas pasūtījumam. Saraksta lapā **Visi pārdošanas pasūtījumi** atlasiet pārdošanas pasūtījumu, kuram pasūtījuma tips ir **Atgrieztais pasūtījums**.

9.  Atveriet veidlapu **Krājumu darbības**. Pārbaudiet, vai atgriešanas izmaksas ir 7,00 par gabalu, izmantojot vērtību laukā **Vienības izmaksu cena**, ar kopsummu 35,00 laukā **Izmaksu summa**. Varat atvērt formu **Krājumu transakcijas** formā **Atgriešanas pasūtījums — AKA kods: %1, %2**. Režģī **Rindas** noklikšķiniet uz **Krājums** \> **Darbības**.

10. Sadaļā Krājumu un noliktavas pārvaldība izmantojiet veidlapu **Slēgšana un pielāgošana**, lai palaistu procedūru **3. Aizvērt**.
    
    Šī darbība pielāgo izmaksas sākotnējā pārdošanas rindā, kuru aprēķinātā vērtība bija -35,00 (5 gabali \* 7,00), uz -30.00 (5 gabali \* 6,00). Tas ir tādēļ, ka krājumu modeļu grupa izmanto metodi “pirmie iekšā, pirmie ārā” (FIFO) un pirmā pirkšanas pasūtījuma FIFO izmaksas ir 6,00 vienības par gabalu. Turklāt šī darbība pielāgo izmaksas pārdoto preču atgriešanas rindā atbilstoši izmaksām par gabalu sākotnējā pārdošanas rindā. Tādēļ izmaksas atgriešanas rindās tiek pielāgotas no 35,00 uz 30,00.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]