---
title: izveidot pārdošanas pasūtījumus;
description: Šajā procedūrā ir parādīts, kā izveidot pārdošanas pasūtījumu.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5746fa0ab9fd7ef3e288adc88a755324309a27c0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566315"
---
# <a name="create-sales-orders"></a>izveidot pārdošanas pasūtījumus;

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pārdošanas pasūtījumu. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Pārdošanas pasūtījumus parasti izveido pārdošanas pasūtījumu apstrādātājs. 

## <a name="enter-sales-order-header-details"></a>Ievadiet pārdošanas pasūtījuma virsraksta informāciju
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.
4. Sarakstā atrodiet un atlasiet debitora ierakstu.
    - Šim piemēram atlasiet debitora numuru US-004.  
5. Atlasiet **Labi**.

## <a name="enter-sales-order-line-details"></a>Ievadīt pārdošanas pasūtījuma rindas informāciju
    
Jūsu organizācijas pārdotās preces var tikt piedāvātas dažādos variantos, kas atšķiras pēc dimensijām, piemēram, konfigurācijas, krāsas, izmēra un stila. Tāpat preces var būt iestatītas noliktavas dimensiju lietošanai, piemēram, vietām, noliktavām un paletēm, kā arī izsekošanas dimensiju lietošanai, piemēram, partijām un sērijas numuriem. Kad tiek piešķirtas šīm dimensijas, jums pasūtījuma rindā ir jāatlasa vērtības šīm dimensijām. Lai uzlabotu pasūtījuma izveides efektivitāti, iespējams, attiecīgo dimensiju laukus vēlaties pievienot pasūtījuma režģim.
    
1. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pārdošanas pasūtījuma rinda**.
2. Atlasiet **Dimensijas**.
    
    Šajā piemērā atlasiet dimensijas Krāsa, Vieta un Noliktava. Jūsu atlasītās dimensijas būs redzamas pārdošanas pasūtījuma režģī. Ja vēlaties, lai jūsu atlases saglabātos, opcijai **Saglabāt iestatījumus** norādiet vērtību Jā.
    
3. Atlasiet **Labi**.
4. Laukā **Krājuma kods** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.
5. Šim piemēram atlasiet krājuma kodu T0004.
    - Ja krājums ir daļa no pārdošanas kategorijas, šī krājuma nosaukums automātiski tiks parādīts laukā Pārdošanas kategorija.  
    - Ja preču dimensiju laukos jau ir kāda vērtība, tas ir tāpēc, ka šī vērtība tika kopēta no preces ieraksta, kur tā bija definēta kā noklusējuma preces dimensija. Noklusējuma vērtību varat mainīt jebkurā laikā.   
6. Laukā **Krāsa** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Laukā **Daudzums** ierakstiet kādu skaitli.
    - Ja krājums tiek pārdots citās vienībās, nevis tajās, kādās tas tika iegādāts, ražots un glabāts, un ja preces ierakstā ir iestatīta pārdošanas mērvienība, šī vērtība tiks rādīta laukā **Vienība**. Šo vērtību varat mainīt jebkurā laikā.   
    - Ja laukā **Vieta** jau ir kāda vērtība, šī vērtība tika kopēta no pasūtījuma virsraksta vai no pasūtījuma iestatījumiem, kas ir saistīti ar šo preci. Šo vērtību varat mainīt jebkurā laikā. Ja šis lauks ir tukšs, atlasiet kādu vērtību.   
    - Ja laukā **Vienības cena** jau ir kāda vērtība, šī vērtība tika kopēta no derīga tirdzniecības līguma vai no preces ieraksta. (Vienības cenas izcelsme var būt arī pārdošanas līgums, bet procedūra pārdošanas pasūtījumu izveidošanai no pārdošanas līgumiem atšķiras no šeit parādītās.) Ja šis lauks ir tukšs, ievadiet kādu vērtību.   
    - Laukā **Atlaide** ir norādīta atlaides summa uz vienu preces vienību. Lai aprēķinātu kopējo rindas atlaides summu, šī atlaides vērtība tiek reizināta ar rindas daudzumu. Ja laukā **Atlaide** jau ir kāda vērtība, šī vērtība tika kopēta no derīga tirdzniecības līguma. Ja šis lauks ir tukšs, bet jūs vēlaties debitoram piešķirt rindas atlaidi, ievadiet kādu vērtību.  
    - Laukā **Atlaide procentos** ir procentuāla vērtība, par kādu jāsamazina rindas kopējā bruto summa.  Ja laukā **Atlaide procentos** jau ir kāda vērtība, tā tika kopēta no derīga tirdzniecības līguma. Ja šis lauks ir tukšs, bet jūs vēlaties debitoram piešķirt rindas atlaidi, ievadiet kādu vērtību. 
    - Laukā **Neto summa** ir vērtība, kas tiek aprēķināta, pamatojoties uz atlaižu koriģēto rindas daudzumu un vienības cenu.  Aprēķināto vērtību varat ignorēt un pārrakstīt uz citu.  

## <a name="review-the-order-totals"></a>Pārskatīt pasūtījuma kopsummas
1. **Darbību rūtī** atlasiet **Pārdošanas pasūtījums**.
2. Atlasiet **Kopsummas**.
    
    Lapā **Kopsummas** tiek rādīta detalizēta informācija par visu pasūtījumu. Šī informācija ietver apakšsummas apjomu, kas ir visu rindas neto summu kopsumma, koriģēta atbilstoši beigu rindas atlaidēm, kopējā rēķina summa, kas ir apakšsummas apjoms, koriģēts atbilstoši beigu pasūtījuma līmeņa atlaidei, papildmaksas un PVN, debitora kredīta limita situācija un citas summas. Rēķina summa ir summa, kas tiks rādīta debitora rēķina dokumentā.  
    
3. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]