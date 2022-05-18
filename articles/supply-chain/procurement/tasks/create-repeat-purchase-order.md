---
title: Atkārtota pirkšanas pasūtījuma izveide
description: Šajā tēmā parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu, kopējot rindas no iepriekšēja pirkšanas pasūtījuma dokumenta jaunā vai esošā pirkšanas pasūtījumā.
author: GalynaFedorova
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be4eca824794b8d45c7a6f40cb68aff7c4a53cd0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671145"
---
# <a name="create-a-repeat-purchase-order"></a>Atkārtota pirkšanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu, kopējot rindas no iepriekšēja pirkšanas pasūtījuma dokumenta jaunā vai esošā pirkšanas pasūtījumā. Atkārtotu pasūtījumu izveidošanai pastāv divas metodes. Varat izmantot darbības, kas no darbību rūts ir pieejamas dokumenta līmenī, vai varat izmantot rindas detaļu darbības. Dokumenta līmeņa darbības galvenokārt ir paredzētas jaunu pirkšanas pasūtījumu izveidošanai, pievienojot rindas un virsraksta informāciju no cita pasūtījuma, kamēr rindas detaļu darbība galvenokārt ir paredzēta rindu pievienošanai jau esošam pasūtījumam. Šajā ceļvedī rādīto piemēru var izmantot paraugdatu uzņēmumā USMF. Šo uzdevumu parasti veic pirkšanas aģents.


## <a name="create-a-new-repeat-purchase-order"></a>Izveidot jaunu atkārtotu pirkšanas pasūtījumu
1. Navigācijas rūtī dodieties uz **Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**. Vispirms mēs izmēģināsim opciju informācijas kopēšanai uz jaunu pasūtījumu.  
2. Atlasiet **Jauns**.
3. Laukā **Kreditora konts** ievadiet `US-101`.
4. Atlasiet **Labi**.
5. Darbību rūtī atlasiet **Pirkšanas pasūtījums**.
6. Atlasiet **No visiem**. Šī ir lapa, kurā no esošajiem pasūtījumiem varat kopēt uz savu pasūtījumu. Veidam, kādā rindas tiek kopētas, pastāv dažādas opcijas, un pastāv dažādi dokumentu veidi, no kuriem varat kopēt. Vispirms mēs apskatīsim opcijas tam, kā rindas tiek kopētas. 
7. Izvērsiet sadaļu **Parametri**.

    - Lauks **Daudzuma koeficients** ir noderīgs, ja vēlaties izmantot daudzumu, kas atšķiras no tā, kas ir pasūtījumā, no kura kopējat. Piemēram, ja vēlaties pasūtīt divreiz lielāku daudzumu, nekā norādīts rindās, no kurām kopējat, tad šajā laukā būtu jāievada '2', un pēc tam sistēma pievienotu rindas, kur sākotnējais daudzums ir dublēts.  
    - Lauks **Apgriešanas zīme** arī atbalsta pasūtītā daudzuma maiņu, mainot daudzuma zīmi pasūtījuma rindām, kas tiek pievienotas. Tas var būt noderīgi, ja ir nepieciešams atsaukt kādu transakciju, izveidojot pasūtījuma rindas, kuras anulē šo transakciju. Šī iespēja tiek atlasīta automātiski, kad lapa tiek atvērta no darbības **Izveidot kredītnotu**.  
    - Opcija **Kopēt maksas** ļauj kopēt maksas uz jauno pasūtījumu no dokumenta, no kura kopējat pasūtījuma rindas.  
    - Opcija **Pārrēķināt cenas** izmanto esošās cenas un atlaides, nevis kopē tās no dokumenta, no kura kopējat citu informāciju.  
    - Opcija **Kopēt precīzi** izveido precīzu kopiju ar visām vērtībām visos laukos pasūtījuma dokumenta galvenē un rindās. Ja šī opcija nav atlasīta, tad daudzos laukos saistībā ar kreditoru un precēm tiek lietotas noklusējuma vērtības, gluži kā tad, ja jauno pasūtījumu jūs veidotu manuāli. Piemēram, ja pasūtījumā, ko kura kopējat, bija ignorēts noklusējuma rēķina konts kreditoram, tas šis pats rēķina konts tiktu kopēts uz jūsu pasūtījumu. Ja nav izvēlēta opcija **Kopēt precīzi**, jūsu pasūtījumam tiks izmantots piegādātāja noklusējuma rēķina konts.  
    - Opcija **Dzēst pirkuma rindas** ļauj dzēst visas pirkšanas pasūtījuma rindas, kas jau ir pirkšanas pieprasījumā, uz kuru kopējat, pirms piemērot jaunās rindas. Šī opcija ir jālieto uzmanīgi, jo tā dzēš visas pastāvošās rindas bez papildu brīdinājuma.  
    - Ja atlasāt opciju **Kopēt pasūtījuma galveni**, jaunajam pasūtījumam galvenes informācija nav jāveido manuāli. Ņemiet vēra, ka šī opcija ar kreditoru saistītajiem laukiem liks izmantot noklusējuma vērtības. Ja dokumentam, no kura kopējat, ir nenoklusējuma vērtības, ko vēlaties kopēt, izmantojiet arī opciju **Kopēt precīzi**.   
    - Pastāv dažādi dokumentu avotiem, no kuriem varat kopēt, un katram šajā lapā ir atsevišķa sadaļa. Piemēram, sadaļa **Pirkšanas pasūtījumi** ļauj kopēt no esošiem pirkšanas pasūtījumiem.  

8. Sadaļā **Pirkšanas pasūtījumi** atlasiet rindas, ko vēlaties kopēt starpliktuvē. Ir iespējams atlasīt papildu pirkšanas pasūtījumu rindas no citiem pirkšanas pasūtījumiem un arī tās kopēt uz savu pasūtījumu. Ir iespējams arī pievienot rindas no citu veidu pirkšanas dokumentiem. Nākamajās dažās darbības ir apskatītas šīs dažādās opcijas.  
9. Izvērsiet sadaļu **Apstiprinājums**. Šeit varat atlasīt pirkšanas pasūtījumu apstiprinājumus, no kuriem kopēt. Pirkšanas pasūtījuma apstiprinājumi tiek identificēti ar saistīto pirkšanas žurnāla ID vai pirkšanas pasūtījuma ID.  
10. Izvērsiet sadaļu **Produktu saņemšanas**. Šeit varat atlasīt produktu ieejas plūsmas žurnālus, no kuriem kopēt. Produktu ieejas plūsmas žurnāli tiek identificēti ar produktu ieejas plūsmas dokumentu vai pirkšanas pasūtījuma ID.   
11. Izvērsiet sadaļu **Rēķini**. Šeit varat atlasīt kreditoru rēķinus, no kuriem kopēt. Rēķini tiek identificēti ar rēķina dokumentu vai pirkšanas pasūtījuma ID.   
12. Izvērsiet sadaļu **Atlasītās rindas vai kopējamā galvene**. Šajā skatā tiek rādīts kopsavilkums par visiem dokumentiem un rindām, kas ir atlasītas kopēšanai uz jūsu pasūtījumu.   
13. Atlasiet **Labi**. Rindas, ko atlasījāt, ir iekopētas jūsu jaunajā pirkšanas pasūtījumā.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopēt rindas uz esošu pirkšanas pasūtījumu  

Tā vietā, lai kopētu visu pasūtījumu, biežāk tiek izveidots jauns pirkšanas pasūtījums (PP) un aizpildīta informācija šī PP virsrakstā, un pēc tam kopētas atsevišķas rindas no esošajiem pasūtījumiem.  

1. Atlasiet rindu **Pirkšanas pasūtījums**.
2. Atlasiet **No visiem**. Tiek atvērta iepriekš parādītajai identiska lapa, bet ir atlasītas citādas opcijas, kad tā tiek atvērta no pasūtījuma rindu skata. Apskatīsim parametrus.   
3. Izvērsiet sadaļu **Parametri**.

    - Opcija **Dzēst pirkšanas rindas** nav atlasīta. Tas nozīmē, ka uz savu pasūtījumu varat kopēt jaunas rindas, noņem esošās rindas.   
    - Arī opcija **Kopēt pasūtījuma galveni** nav atlasīta, jo pievienojam pasūtījumam tikai papildu rindas.   
    - Šajā piemērā mēs kopēsim rindas no esoša pirkšanas pasūtījuma.   

4. Atlasiet vēlamā pirkšanas pasūtījuma rindu. Ņemiet vērā, ka ir atlasīta arī vienīgā pasūtījuma rinda, kas atrodas šajā pirkšanas pasūtījumā (PO).  
5. Atlasiet **Labi**. Jūsu pirkšanas pasūtījumam ir pievienota papildu pasūtījuma rinda.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]