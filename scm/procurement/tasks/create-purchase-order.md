--- 
title: "Pirkšanas pasūtījuma izveide"
description: "Šajā procedūrā ir parādīts, kā manuāli izveidot pirkšanas pasūtījumu."
author: FrankDahl
manager: AnnBe
ms.date: 06/07/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0a761834939363a6598b768d3931f9a6278719f3
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā manuāli izveidot pirkšanas pasūtījumu. Raksturīgāka ir pirkšanas pasūtījumu izveide automātiski, vispārējas plānošanas, tiešās piegādes un citu procesu rezultātā. Pirkuma pasūtījumu parasti veic iepirkuma aģenti. Šeit parādītajā piemērā var izmantot USMF demonstrācijas datu uzņēmumā, izmantojot vērtības, kas tiek piedāvātas dažādu posmu piezīmēs.


## <a name="create-the-purchase-order-header"></a>Izveidojiet pirkšanas pasūtījuma virsrakstu
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Atlasiet kreditora kontu US-101.
    * Kad atlasāt kādu kreditoru, pasūtījuma virsrakstā kā noklusējuma vērtības tiek iekopēta detalizētā informācija no kreditora ieraksta, piemēram, adrese, rēķina konts, piegādes nosacījumi un režīms. Šīs vērtības jebkurā laikā varat mainīt.  
4. Izvērsiet sadaļu Vispārīgi.
    * Vietnes lauks kopā ar noliktavas lauku norāda, kur saražotās preces vai pakalpojumi jāpiegādā. Noklusējuma piegādes adrese, kas ievadīta šai vietai. Abus laukus var aizpildīt ar vērtībām, kas ir iestatītas atlasītajam kreditoram vai tās var norādīt manuāli.  
    * Piegādes datuma lauks tiek lietots, lai norādītu, kad saražotās preces un pakalpojumus nepieciešams piegādāt. Jūs varat norādīt vienu piegādes datumu pasūtījumam, vai atsevišķām pasūtījuma rindām var piešķirt unikālus piegādes datumus. Ja šeit norādīto piegādes datumu nevar izpildīt noteiktiem produktiem vai pakalpojumiem, jo tiem ir ilgāki izpildes laiki, šīs rindas tiks veidotas ar vēlāku piegādes datumu.  
5. Sakļaujiet sadaļu Vispārīgi.
6. Izvērsiet sadaļu Administrēšana.
    * Pasūtītāja lauku var izmantot, lai norādītu, kas veic pasūtījumu. To varētu ērtāk koplietot ar kreditoru, gadījumā, ja ir nepieciešams sazināties ar šo personu. Laukam var piešķirt vērtību automātiski, ja pašreizējais lietotāja konts ir saistīts ar nosaukumu lapā Lietotāji.  
7. Sakļaujiet sadaļu Administrēšana.
8. Noklikšķiniet uz OK.
    * Tika izveidots pasūtījuma virsraksts. Strādājot ar pirkšanas pasūtījuma rindām, tiek parādīts tikai virsraksta informācijas kopsavilkums. Ja jums nepieciešams skatīt pārējo informāciju, noklikšķiniet uz Virsraksts.  

## <a name="add-a-purchase-order-line"></a>Pievienojiet pirkšanas pasūtījuma rindu
1. Noklikšķiniet uz Pirkšanas pasūtījuma rinda.
2. Noklikšķiniet uz Dimensijas.
    * Preces var būt variantos, kas atšķiras pēc dimensijām, piemēram, krāsas, izmēra vai stilu. Preces var arī iestatīt, lai izmantotu noliktavas dimensijas, piemēram, vietu un noliktavu. Ir arī papildu izsekošanas dimensijas, piemēram, partiju un sēriju numuri. Pasūtījuma izveides efektivitātes uzlabošanai, jūs varat pievienot dimensiju laukus, kuri parasti tiek izmantoti tieši pasūtījumu režģī.  
3. Atzīmējiet krāsas izvēles rūtiņu.
    * Papildu: Atlasot lauku Saglabāt iestatījumus, jūsu atlasītās dimensijas tiks rādītas pasūtījuma rindas režģī arī nākamo reizi atverot pirkšanas pasūtījuma lapu.  
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods atlasiet T0004.
    * Pasūtījuma rindas tiek veidotas produktiem un pakalpojumiem, norādot krājuma kodu vai kā izdevumus, norādot Sagādes kategoriju.  
    * Sagādes kategorijas lauks tiek izmantots rindu pievienošanai, kur saražotie krājumi tiek iekļautas izdevumos pa tiešo, nevis tiek pieņemti noliktavā. Tas nozīmē, ka, ja jums nepieciešami pirkšanas izdevumi, to var izdarīt, izveidojot pirkšanas pasūtījuma rindu, kas norāda sagādes kategoriju, nevis izveido rindu ar krājuma kodu. Krājumi var būt saistīti ar sagādes kategoriju, un šajā gadījumā rādītajai sagādes kategorijai ir tikai informatīvs raksturs.  
6. Laukā Krāsa ievadiet vai atlasiet kādu vērtību.
    * Vietas un Noliktavas lauki parasti tiek aizpildīti ar vērtībām no pasūtījuma virsraksta, bet tos ir iespējams ignorēt, ja dažas rindas ir nepieciešams piegādāt dažādās vietās.  
7. Laukā Daudzums ievadiet skaitli.
    * Atlasiet daudzumu, kuru vēlaties iegādāties. Daudzuma lauks tiek automātiski aizpildīts ar preces minimālo pasūtījuma daudzumu, ja tas ir iestatīts, vai ar vērtību 1.  
    * Laukā Vienība ir norādīta pasūtītajam daudzumam izmantojamā mērvienība. Parasti vienība tiek automātiski sniegta no pirkšanas vienības preču pamatdatiem, bet jūs to varat mainīt.  
    * Vienības cenas lauks parasti satur vērtību no pirkšanas līguma vai tirdzniecības līguma. Ir iespējams mainīt vienības cenu atsevišķās pasūtījuma rindās, piemēram, ja ar kreditoru tiek panākta vienošanās par unikālu cenu.  
    * Laukā Atlaide ir norādīta atlaides summa uz vienu preces vienību. Šī atlaide tādējādi samazina vienības cenu par atlaides apjomu. Šī atlaide parasti tiek ievadīta automātiski no pirkšanas līgumiem vai tirdzniecības līgumiem, bet to ir iespējams ignorēt atsevišķās rindās, ja ar kreditoru tiek panākta vienošanās par unikālu atlaidi.  
    * Iespējams ievadīt atlaides procentuālo vērtību, kas attiecīgi samazina rindas neto summa. Atlaides procentuālā vērtība parasti tiek ievadīta automātiski no pirkšanas līgumiem vai tirdzniecības līgumiem, bet to ir iespējams ignorēt atsevišķās rindās, ja ar kreditoru tiek panākta vienošanās par unikālu atlaides procentuālo vērtību.  
    * Vērtība laukā Neto summa tiek aprēķināta no citiem laukiem rindā, ieskaitot daudzumu, vienības cenu, atlaidi un atlaides procentuālo vērtību. Ir iespējams mainīt Neto summu, bet lauki Vienības cena, Atlaide un Atlaides procentuālā vērtība ir tukši, un grāmatojot līniju, grāmatotā summa būs proporcionāla neto summai. Parasti Neto summas lauku izmanto tikai rādot rindas neto summu.  
8. Izvērsiet sadaļu Detalizēta informācija par rindu.
9. Noklikšķiniet uz cilnes Piegāde.
    * Katrai pasūtījuma rindai var piešķirt unikālu piegādes datumu. Datums tiek pārmantots no pirkšanas pasūtījuma virsraksta lauka, bet jūs to varat mainīt.  
10. Sakļaujiet sadaļu Detalizēta rindas informācija.

## <a name="review-order-totals"></a>Pārskatiet pasūtījuma kopsummas
1. Noklikšķiniet uz Kopsummas.
    * Ja neredzat kopsummas, noklikšķiniet uz Pirkšanas pasūtījuma cilni darbību joslā.  
    * Šajā dialoglodziņā tiek parādīta visa pasūtījuma kopsumma.  
    * Atlases lauks ļauj jums mainīt kopsummu aprēķināšanas bāzi. Piemēram, jūs varat atlasīt Daudzums produktu ieejas plūsmās, lai rādītu kopsummas, kas attiecas uz preci(-ēm), kas tika saņemtas, vai pasūtīto daudzumu, lai parādītu preču daudzumu, kas tika pasūtītas.  
2. Noklikšķiniet uz OK.


