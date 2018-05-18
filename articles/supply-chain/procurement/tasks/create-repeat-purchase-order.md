--- 
title: "Atkārtota pirkšanas pasūtījuma izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu (PP), rindas no iepriekšēja pirkšanas pasūtījuma dokumenta kopējot uz jaunu PP vai uz esošu PP."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Atkārtota pirkšanas pasūtījuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu (PP), rindas no iepriekšēja pirkšanas pasūtījuma dokumenta kopējot uz jaunu PP vai uz esošu PP. Atkārtotu pasūtījumu izveidošanai pastāv divas metodes. Varat izmantot darbības, kas no darbību rūts ir pieejamas dokumenta līmenī, vai varat izmantot rindas detaļu darbības. Dokumenta līmeņa darbības galvenokārt ir paredzētas jaunu pirkšanas pasūtījumu izveidošanai, pievienojot rindas un virsraksta informāciju no cita pasūtījuma, kamēr rindas detaļu darbība galvenokārt ir paredzēta rindu pievienošanai jau esošam pasūtījumam. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Šo uzdevumu parasti veic pirkšanas aģents.


## <a name="create-a-new-repeat-purchase-order"></a>Izveidot jaunu atkārtotu pirkšanas pasūtījumu
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
    * Vispirms mēs izmēģināsim opciju informācijas kopēšanai uz jaunu pasūtījumu.  
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts ievadiet US-101.
4. Noklikšķiniet uz OK.
5. Darbību rūtī noklikšķiniet uz Pirkšanas pasūtījums.
6. Noklikšķiniet uz No visiem.
    * Šī ir lapa, kurā no esošajiem pasūtījumiem varat kopēt uz savu pasūtījumu. Veidam, kādā rindas tiek kopētas, pastāv dažādas opcijas, un pastāv dažādi dokumentu veidi, no kuriem varat kopēt. Vispirms mēs apskatīsim opcijas tam, kā rindas tiek kopētas.   
7. Izvērsiet sadaļu Parametri.
    * Lauks Daudzuma koeficients ir noderīgs, ja ir nepieciešams izmantot daudzumu, kas atšķiras no daudzuma pasūtījumā, no kura veicat kopēšanu. Piemēram, ja vēlaties pasūtīt divreiz lielāku daudzumu, nekā norādīts rindās, no kurām kopējat, tad šajā laukā būtu jāievada “2”, un pēc tam sistēma pievienotu rindas, kur sākotnējais daudzums ir dublēts.  
    * Lauks Mainīt zīmi uz pretējo atbalsta arī pasūtītā daudzuma mainīšanu, mainot zīmi pievienoto pasūtījuma rindu daudzumam. Tas var būt noderīgi, ja ir nepieciešams atsaukt kādu transakciju, izveidojot pasūtījuma rindas, kuras anulē šo transakciju. Šī opcija tiek atlasīta automātiski, kad lapa tiek atvērta no darbības Izveidot kredīta notu.  
    * Opcija Kopēt maksas jums ļauj uz jauno pasūtījumu kopēt maksas no dokumenta, no kura kopējat pasūtījuma rindas.  
    * Opcija Pārrēķināt cenas izmanto pašreizējās cenas un atlaides, nevis kopē tās no dokumenta, no kura kopējat pārējo informāciju.  
    * Opcija Kopēt precīzi pasūtījuma dokumenta virsrakstā un rindās izveido precīzu kopiju no vērtībām visos laukos. Ja šī opcija nav atlasīta, tad daudzos laukos saistībā ar kreditoru un precēm tiek lietotas noklusējuma vērtības, gluži kā tad, ja jauno pasūtījumu jūs veidotu manuāli. Piemēram, ja pasūtījumā, ko kura kopējat, bija ignorēts noklusējuma rēķina konts kreditoram, tas šis pats rēķina konts tiktu kopēts uz jūsu pasūtījumu. Ja neatlasījāt opciju Kopēt precīzi, tad jūsu pasūtījumā tā vietā tiktu lietots noklusējuma rēķina konts kreditoram.  
    * Opcija Dzēst pirkšanas rindas pirms jauno rindu lietošanas dzēš visas pirkšanas pasūtījuma rindas, kas jau pastāv pirkšanas pasūtījumā, uz kuru veicat kopēšanu. Šī opcija ir jālieto uzmanīgi, jo tā dzēš visas pastāvošās rindas bez papildu brīdinājuma.  
    * Ja lietojat opciju Kopēt pasūtījuma virsrakstu, tad savā jaunajā pasūtījumā jums nav nepieciešams manuāli izveidot virsraksta informāciju. Ņemiet vēra, ka šī opcija ar kreditoru saistītajiem laukiem liks izmantot noklusējuma vērtības. Ja dokumentā, no kura kopējat, nav noklusējuma vērtību, kuras vēlaties kopēt, izmantojiet arī opciju Kopēt precīzi.  
8. Sakļaujiet sadaļu Parametri.
    * Pastāv dažādi dokumentu avotiem, no kuriem varat kopēt, un katram šajā lapā ir atsevišķa sadaļa. Piemēram, atlase Pirkšanas pasūtījums jums ļauj kopēt no pastāvošiem pirkšanas pasūtījumiem.  
9. Noklikšķiniet uz rindas pirkšanas pasūtījumam, kuras ID ir 00015. 
10. Atlasiet rindu, noklikšķinot uz izvēles rūtiņas.
11. Noņemiet atzīmi šīs rindas izvēles rūtiņai, lai tā netiktu kopēta uz jūsu pasūtījumu.
    * Tagad kopēšanai uz jūsu pirkšanas pasūtījumu ir atlasītas 4 rindas. Ir iespējams atlasīt papildu pirkšanas pasūtījumu rindas no citiem pirkšanas pasūtījumiem un arī tās kopēt uz savu pasūtījumu. Ir iespējams arī pievienot rindas no citu veidu pirkšanas dokumentiem. Nākamajās dažās darbības ir apskatītas šīs dažādās opcijas.  
12. Sakļaujiet sadaļu Pirkšanas pasūtījumi.
13. Izvērsiet sadaļu Apstiprinājums.
    * Šeit varat atlasīt pirkšanas pasūtījumu apstiprinājumus, no kuriem kopēt. Pirkšanas pasūtījuma apstiprinājumi tiek identificēti ar saistīto pirkšanas žurnāla ID vai pirkšanas pasūtījuma ID.  
14. Sakļaujiet sadaļu Apstiprinājums.
15. Izvērsiet sadaļu Produktu ieejas plūsmas.
    * Šeit varat atlasīt produktu ieejas plūsmas žurnālus, no kuriem kopēt. Produktu ieejas plūsmas žurnāli tiek identificēti ar produktu ieejas plūsmas dokumentu vai pirkšanas pasūtījuma ID.   
16. Sakļaujiet sadaļu Produktu ieejas plūsmas.
17. Izvērsiet atlasi Rēķini.
    * Šeit varat atlasīt kreditoru rēķinus, no kuriem kopēt. Rēķini tiek identificēti ar rēķina dokumentu vai pirkšanas pasūtījuma ID.   
18. Sakļaujiet sadaļu Rēķini.
19. Izvērsiet sadaļu Atlasītās kopējamās rindas vai virsraksts.
    * Šajā skatā tiek rādīts kopsavilkums par visiem dokumentiem un rindām, kas ir atlasītas kopēšanai uz jūsu pasūtījumu.   
20. Sakļaujiet sadaļu Atlasītās kopējamās rindas vai virsraksts.
21. Noklikšķiniet uz OK.
    * Jūsu atlasītās 4 rindas ir pārkopētas uz jūsu jauno pirkšanas pasūtījumu.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopēt rindas uz esošu pirkšanas pasūtījumu
    * Tā vietā, lai kopētu visu pasūtījumu, biežāk tiek izveidots jauns pirkšanas pasūtījums (PP) un aizpildīta informācija šī PP virsrakstā, un pēc tam kopētas atsevišķas rindas no esošajiem pasūtījumiem.  
1. Noklikšķiniet uz Pirkšanas pasūtījuma rinda.
2. Noklikšķiniet uz No visiem.
    * Tiek atvērta iepriekš parādītajai identiska lapa, bet ir atlasītas citādas opcijas, kad tā tiek atvērta no pasūtījuma rindu skata. Apskatīsim parametrus.   
3. Izvērsiet sadaļu Parametri.
    * Opcija Dzēst pirkšanas rindas nav atlasīta. Tas nozīmē, ka uz savu pasūtījumu varat kopēt jaunas rindas, noņem esošās rindas.   
    * Arī opcija Kopēt pasūtījuma virsrakstu nav atzīmēta, jo mēs pasūtījumam tikai pievienojam papildu rindas.   
4. Sakļaujiet sadaļu Parametri.
    * Šajā piemērā mēs kopēsim rindas no esoša pirkšanas pasūtījuma.   
5. Noklikšķiniet uz rindas pirkšanas pasūtījumam, kuras ID ir 00034. 
6. Atlasiet rindu, noklikšķinot uz izvēles rūtiņas.
    * Ņemiet vērā, ka ir atlasīta arī vienīgā pasūtījuma rinda, kas atrodas šajā pirkšanas pasūtījumā (PO).  
7. Noklikšķiniet uz OK.
    * Jūsu pirkšanas pasūtījumam ir pievienota papildu pasūtījuma rinda.  


