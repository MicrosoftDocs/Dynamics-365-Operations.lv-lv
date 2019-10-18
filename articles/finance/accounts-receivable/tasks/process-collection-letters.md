---
title: Atgādinājuma vēstuļu apstrāde
description: Šajā tēmā ir parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178884"
---
# <a name="process-collection-letters"></a>Atgādinājuma vēstuļu apstrāde

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē
1. Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana >Klientu grāmatošanas profili.**
2. Noklikšķiniet uz **Rediģēt**.
3. Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību. Ja atgādinājuma vēstules par transakcijām nevēlaties ģenerēt, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.  
4. Izvērsiet cilni **Tabulas ierobežojumi**, lai mainītu veidu, kādā tiek apstrādātas atgādinājuma vēstules. Ja šajā laukā ir iestatīts **Jā**, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.  

## <a name="create-collection-letters"></a>Izveidot atgādinājuma vēstules
1. Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules**.
2. Atlasiet transakciju veidus, par ko apkoposit vēstules. Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.  
3. Laukā **Atgādinājuma vēstule** atlasiet opciju.
4. Laukā **Atgādinājuma vēstules datums** ievadiet atgādinājuma vēstules datumu.
5. Atlasiet grāmatošanas metodi, ja mainījāt **Izmantot grāmatošanas metodi no** uz **Atlasīt**. Ir divas grāmatošanas profilu opcijas:   

   - **Konts** — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi.   
   - **Atlasīt** — lietojiet grāmatošanas metodi, kuru atlasījāt laukā **Grāmatošanas metode**.  

6. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
7. Atlasiet **Filtrēt**.
8. Laukā **Kritērijs** ievadiet debitora ID. Piemēram, ievadiet US-001.
9. Atlasiet **Labi**.
10. Atlasiet **Labi**.

## <a name="print-collection-letters"></a>Atgādinājuma vēstuļu izdruka
1. Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Atgādinājuma vēstuļu izskatīšana un apstrāde**.
2. Laukā **Statuss** atlasiet **Izveidots**.
3. Laukā **Drukāts** atlasiet **Nav drukāts**.
4. Atlasiet **Drukāt**.
5. Atlasiet **Atgādinājuma vēstules piezīme**.
6. Sadaļā **Parametri** ievadiet grāmatojumu robeždatumu.
7. Izvērsiet sadaļu **Iekļaujamie ieraksti** un ievadiet informāciju atgādinājuma vēstules piezīmē.
8. Atlasiet **Labi**, lai izdrukātu atgādinājuma vēstuli.
9. Grāmatojiet atgādinājuma vēstuli.

    1. Atlasiet **Grāmatot**.
    1. Ievadiet atgādinājuma vēstules grāmatošanas datumu.
    1. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
    1. Atlasiet **Labi**.
    1. Laukā **Statuss** atlasiet **Iegrāmatots**.
    1. Laukā **Drukāts** atlasiet opciju.

## <a name="control-collection-letters-at-the-customer-level"></a>Atgādinājuma vēstuļu pārvaldība debitora līmenī
Varat arī iestatīt atgādinājuma vēstules debitora līmenī, un tādējādi tiks izsekots katras transakcijas atgādinājuma vēstules kods, bet atgādinājuma vēstuļu apstrādes pamatā būs viens atgādinājuma vēstuļu līmenis, kas saglabāts par debitoru. Viena atgādinājuma vēstule ietvers visas debitora nokavētās transakcijas. Tā kā pagarinājuma dienas tagad tiek izsekotas debitora līmenī, nākamā atgādinājuma vēstule netiek nosūtīta, līdz nav pagājis nākamās atgādinājuma vēstules nosūtīšanai noteiktais pagarinājuma dienu skaits, pat ja transakcijas tiek nokavētas pēc pēdējās atgādinājuma vēstules nosūtīšanas. Šī iespēja samazina katram klientam nosūtāmo atgādinājuma vēstuļu skaitu. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Debitora iestatīšana atgādinājuma vēstuļu pārvaldībai debitora līmenī
1.  Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana > Kreditoru parametri** un atlasiet cilni **Atgūšana**. 
2.  Mainiet parametra **Izveidot atgādinājuma vēstuli katram** vērtību uz **Debitoram**. 
3.  Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Atgādinājuma vēstuļu izskatīšana un apstrāde**. Katram debitoram tiks izveidota tikai viena atgādinājuma vēstule ar visām nokavētajām transakcijām.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu
Ja maksājumus un kredītrēķinus iekļaujat transakcijās, kas tiks iekļautas atgādinājuma vēstulēs, var būt tādi maksājumi vai kredītrēķini, kas aktivizēs atgādinājuma vēstules izveidi. Izmainot parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu** vērtību, varat pārvaldīt, kā maksājumi un kredītrēķini ietekmē atgādinājuma vēstules kodu. 

Lai ignorētu maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu, rīkojieties, kā norādīts tālāk.

1. Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana > Kreditoru parametri** un noklikšķiniet uz cilnes **Atgūšana**. 
2. Mainiet parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu vērtību** uz **Jā**.
