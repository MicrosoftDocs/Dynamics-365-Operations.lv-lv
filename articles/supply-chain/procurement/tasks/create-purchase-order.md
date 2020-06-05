---
title: Pirkšanas pasūtījuma izveide
description: Šajā tēmā ir parādīts, kā izveidot pirkuma pasūtījumu manuāli.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ed359521dd018047fdbd5312d0cb73d764de925
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383232"
---
# <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir parādīts, kā izveidot pirkuma pasūtījumu manuāli. Raksturīgāka ir pirkšanas pasūtījumu izveide automātiski, vispārējas plānošanas, tiešās piegādes un citu procesu rezultātā. Pirkuma pasūtījumu parasti veic iepirkuma aģenti. Šeit parādītajā piemērā var izmantot USMF demonstrācijas datu uzņēmumā, izmantojot vērtības, kas tiek piedāvātas dažādu posmu piezīmēs.


## <a name="create-the-purchase-order-header"></a>Izveidojiet pirkšanas pasūtījuma virsrakstu
1. Pārejiet uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Atlasiet piegādātāja kontu **US-101**. Kad atlasāt kādu kreditoru, pasūtījuma virsrakstā kā noklusējuma vērtības tiek iekopēta detalizētā informācija no kreditora ieraksta, piemēram, adrese, rēķina konts, piegādes nosacījumi un režīms. Šīs vērtības jebkurā laikā varat mainīt.  
4. Izvērsiet sadaļu **Vispārīgi**.

    - Laukā **Vieta** un laukā **Noliktava** norādīts, uz kurieni jāpiegādā iegādātās preces vai pakalpojumi. Noklusējuma piegādes adrese, kas ievadīta šai vietai. Abus laukus var aizpildīt ar vērtībām, kas ir iestatītas atlasītajam kreditoram vai tās var norādīt manuāli.  
    - Laukā **Piegādes datums** norādīts, kad jāpiegādā iegādātās preces vai pakalpojumi. Jūs varat norādīt vienu piegādes datumu pasūtījumam, vai atsevišķām pasūtījuma rindām var piešķirt unikālus piegādes datumus. Ja šeit norādīto piegādes datumu nevar izpildīt noteiktiem produktiem vai pakalpojumiem, jo tiem ir ilgāki izpildes laiki, šīs rindas tiks veidotas ar vēlāku piegādes datumu.  

5. Izvērsiet sadaļu **Administrēšana**. Laukā **Pasūtīts** var norādīt personu, kas izvieto pieprasījumu. To varētu ērtāk koplietot ar kreditoru, gadījumā, ja ir nepieciešams sazināties ar šo personu. Laukam var piešķirt vērtību automātiski, ja pašreizējais lietotāja konts ir saistīts ar vārdu lapā **Lietotāji**.  
6. Atlasiet **Labi**. Tika izveidots pasūtījuma virsraksts. Strādājot ar pirkšanas pasūtījuma rindām, tiek parādīts tikai virsraksta informācijas kopsavilkums. Ja vēlaties skatīt atlikušo informāciju, atlasiet **Galvene**.  

## <a name="add-a-purchase-order-line"></a>Pievienojiet pirkšanas pasūtījuma rindu
1. Atlasiet **Pirkšanas pasūtījuma rinda**.
2. Atlasiet **Dimensijas**. Preces var būt variantos, kas atšķiras pēc dimensijām, piemēram, krāsas, izmēra vai stilu. Preces var arī iestatīt, lai izmantotu noliktavas dimensijas, piemēram, vietu un noliktavu. Ir arī papildu izsekošanas dimensijas, piemēram, partiju un sēriju numuri. Pasūtījuma izveides efektivitātes uzlabošanai, jūs varat pievienot dimensiju laukus, kuri parasti tiek izmantoti tieši pasūtījumu režģī.  
3. Noklikšķiniet uz izvēles rūtiņu **Krāsa**. Papildu iespēja: ja atlasāt lauku **Saglabāt iestatīšanu**, jūsu izvēlētie izmēri tiks rādīti arī pasūtījumu rindu režģī nākamajā reizē, kad atverat pirkšanas pasūtījuma lapu.  
4. Atlasiet **Labi**.
5. Laukā **Krājuma numurs** atlasiet **T0004**.

    - Pasūtījuma rindas tiek veidotas produktiem un pakalpojumiem, norādot krājuma kodu vai kā izdevumus, norādot Sagādes kategoriju. 
    - Kategorijas lauku **Iepirkums** izmanto, lai pievienotu rindas, kad iegādātie vienumi tiek norakstīti izdevumos, nevis tiek pārnesti uz krājumiem. Tas nozīmē, ka, ja jums nepieciešami pirkšanas izdevumi, to var izdarīt, izveidojot pirkšanas pasūtījuma rindu, kas norāda sagādes kategoriju, nevis izveido rindu ar krājuma kodu. Krājumi var būt saistīti ar sagādes kategoriju, un šajā gadījumā rādītajai sagādes kategorijai ir tikai informatīvs raksturs.  

6. Laukā **Krāsa** ievadiet vai atlasiet vērtību. Parasti lauki **Vieta** un **Noliktava** tiek aizpildīti ar vērtībām no pasūtījuma galvenes, bet ir iespējams ignorēt šos laukus, ja kādas rindas ir jāpiegādā dažādām vietām.  
7. Laukā **Daudzums** ierakstiet kādu skaitli.

    - Atlasiet daudzumu, kuru vēlaties iegādāties. Lauku **Daudzums** automātiski aizpilda ar minimālo pasūtījuma daudzumu produktam, ja tas ticis iestatīts, vai ar vērtību 1.  
    - Lauks **Vienība** norāda mērvienību pasūtītajam daudzumam. Parasti vienība tiek automātiski sniegta no pirkšanas vienības preču pamatdatiem, bet jūs to varat mainīt.  
    - Lauks **Vienības cena** parasti satur vērtību vai nu no pirkšanas līguma, vai tirdzniecības līguma. Ir iespējams mainīt vienības cenu atsevišķās pasūtījuma rindās, piemēram, ja ar kreditoru tiek panākta vienošanās par unikālu cenu.  
    - Laukā **Atlaide** parādīta atlaides summa vienībai. Šī atlaide tādējādi samazina vienības cenu par atlaides apjomu. Šī atlaide parasti tiek ievadīta automātiski no pirkšanas līgumiem vai tirdzniecības līgumiem, bet to ir iespējams ignorēt atsevišķās rindās, ja ar kreditoru tiek panākta vienošanās par unikālu atlaidi.  
    - Iespējams ievadīt atlaides procentuālo vērtību, kas attiecīgi samazina rindas neto summa. Atlaides procentuālā vērtība parasti tiek ievadīta automātiski no pirkšanas līgumiem vai tirdzniecības līgumiem, bet to ir iespējams ignorēt atsevišķās rindās, ja ar kreditoru tiek panākta vienošanās par unikālu atlaides procentuālo vērtību.  
    - Vērtība laukā **Neto summa** tiek aprēķināta no citiem laukiem par rindu, tostarp daudzuma, vienības cenas, atlaides un atlaides procentiem. Neto summu ir iespējams mainīt, bet tad lauki **Vienības cena**, **Atlaide** un **Atlaide procentos** būs tukši, un, ja jūs publicējat rindai, publicētā summa būs proporcionāla neto summai. Parasti lauks **Neto summa** tiek izmantots tikai, lai parādītu rindas neto summu.  

8. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
9. Atlasiet cilni **Piegāde**. Katrai pasūtījuma rindai var piešķirt unikālu piegādes datumu. Datums tiek pārmantots no pirkšanas pasūtījuma virsraksta lauka, bet jūs to varat mainīt.  

## <a name="review-order-totals"></a>Pārskatiet pasūtījuma kopsummas
1. Atlasiet **Kopsummas**.

    - Ja neredzat sadaļu **Kopējie**, atlasiet cilni **Pirkšanas pasūtījums** darbību rūtī.  
    - Šajā dialoglodziņā tiek parādīta visa pasūtījuma kopsumma.  
    - Lauks **Atlase** ļauj jums mainīt pamatus, kā aprēķina kopējos rādītājus. Piemēram, varat izvēlēties **Produktu saņemšanas daudzums**, lai parādītu kopējos daudzumus, kas attiecas uz saņemto produkta(-u) daudzumu, vai **Pasūtītais daudzums**, lai parādītu pasūtītā produkta daudzumu.  

2. Atlasiet **Labi**.

