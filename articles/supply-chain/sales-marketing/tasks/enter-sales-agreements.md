--- 
title: "Pārdošanas līgumu ievade"
description: "Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par iepriekš norunāto summu, par to saņemot īpašas atlaides."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a>Pārdošanas līgumu ievade

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par

iepriekš norunāto summu, par to saņemot īpašas atlaides. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-sales-agreement-header"></a>Pārdošanas līguma virsraksta iestatīšana
1. Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Pārdošanas līgumu klasifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Izvērsiet sadaļu Vispārīgi.
9. Laukā Noklusējuma saistības atlasiet Uz preču vērtību attiecināmas saistības.
    * Saistību veids ir obligāts kritērijs, kas ir jāpiešķir līgumam, lai definētu, kā līgums tiks izpildīts. Izmantojot četrus iepriekš definētus veidus, var iestatīt klienta saistību mērķi, kas tiek izteikts kā daudzums vai vērtība. Daudzuma saistību veidu var lietot tikai noteiktām precēm, bet vērtību veidus var lietot konkrētu vai vispārīga veida preču pārdošanā.  
10. Laukā Beigu datums iestatiet datumu nākotnē, kad beidzas līguma termiņš.
11. Noklikšķiniet uz OK.

## <a name="set-up-product-value-commitment-lines"></a>Uz preču vērtību attiecināmo saistību rindu iestatīšana
1. Noklikšķiniet uz Pievienot rindu.
2. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Līgumam izvēlēto saistību veids ietekmē to, kāda veida informāciju var ievadīt līguma rindās. Piemēram, vērtību līgumam ir jānorāda kopējā neto summa (saskaņotajā valūtā), par kuru debitors apņēmās nopirkt no jums preces. Šajā piemērā rindas lauks Daudzums un Vienības nav pieejams, jo debitoram tiek izveidots līgums saistībā ar preces ar konkrētu vērtību iegādi.   
5. Laukā Neto summa ievadiet naudas summu, ko debitors apņēmās samaksāt.
6. Laukā Atlaides procents ievadiet procentuālo vērtību, kas tiks lietota debitora pārdošanas pasūtījuma rindām, kas ir piesaistītas ar šim līgumam.
7. Izvērsiet sadaļu Detalizēta informācija par rindu.
8. Laukā Sasniegts maksimums atlasiet Jā.
    * Atlasot Sasniegts maksimums, visu to pārdošanas pasūtījuma rindu kopsumma, kurās izmanto īpašas saistību cenas, atlaides un/vai maksāšanas nosacījumus, nedrīkst pārsniegt saistībās norādīto summu.  
    * Minimālā un maksimālā izlaišanas summa norāda to vērtību diapazonu, kas ir jāpārdod katrā pārdošanas pasūtījumā, kas izmanto atlasīto līgumu.   
9. Izvērsiet sadaļu Pārdošanas līguma virsraksts.
    * Ja vien līguma statuss nav iestatīts uz Ir spēkā, pārdošanas pasūtījumus nevar saistīt ar līgumu, tādēļ tie nevar sekmēt šī līguma izpildi. Šajā posmā statusu var mainīt manuāli. Tomēr statuss parasti ir jāmaina tad, kad apstiprināt debitora līgumu.  
10. Darbības rūtī noklikšķiniet uz vienuma Pārdošanas līgums.
11. Noklikšķiniet uz Apstiprinājums.
    * Pārliecinieties, vai opcijai Atzīmēt līgumu kā efektīvu ir iestatīts Jā.  
12. Laukā Drukāt pārskatu atlasiet Jā.
13. Noklikšķiniet uz OK.
14. Aizvērt lapu.
    * Tagad līgums ir spēkā un varat sākt piesaistīt līgumam debitora pasūtījumus atbilstoši mērķim.  

