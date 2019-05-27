---
title: Atgādinājuma vēstuļu apstrāde
description: Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549633"
---
# <a name="process-collection-letters"></a>Atgādinājuma vēstuļu apstrāde

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes**.
2. Noklikšķiniet uz **Rediģēt**.
3. Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību. Ja atgādinājuma vēstules par transakcijām nevēlaties ģenerēt, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.  
4. Izvērsiet tabulas ierobežojumu cilni, lai mainītu veidu, kā tiek apstrādātas atgādinājuma vēstules. Ja šajā laukā ir iestatīts **Jā**, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.  

## <a name="create-collection-letters"></a>Izveidot atgādinājuma vēstules
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules**.
2. Atlasiet transakciju veidus, par ko apkoposit vēstules. Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.  
2. Laukā **Atgādinājuma vēstule** atlasiet opciju.
3. Ievadiet atgādinājuma vēstules datumu.
4. Atlasiet grāmatošanas metodi, ja mainījāt **Izmantot grāmatošanas metodi no** uz **Atlasīt**. Ir divas grāmatošanas profilu opcijas:   
   - **Konts** — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi.   
   - **Atlasīt** — lietojiet grāmatošanas metodi, kuru atlasījāt laukā **Grāmatošanas metode**.  
5. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
6. Noklikšķiniet uz **Filtrēt**.
7. Laukā **Kritērijs** ievadiet debitora ID. Piemēram, ievadiet US-001.
8. Noklikšķiniet uz **Labi**.
9. Noklikšķiniet uz **Labi**.

## <a name="print-collection-letters"></a>Atgādinājuma vēstuļu izdruka
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules**.
2. Laukā **Statuss** atlasiet **Izveidots**.
3. Laukā **Drukāts** atlasiet **Nav drukāts**.
4. Klikšķiniet **Drukāt**.
5. Noklikšķiniet uz **Atgādinājuma vēstules piezīmes**.
6. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
7. Ievadiet grāmatošanas robeždatumu.
8. Noklikšķiniet uz **Labi**, lai drukātu atgādinājuma vēstuli.
9. Grāmatojiet atgādinājuma vēstuli.
   1. Noklikšķiniet uz **Grāmatot**.
   2. Ievadiet atgādinājuma vēstules grāmatošanas datumu.
   3. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
   4. Noklikšķiniet uz **Labi**.
   5. Laukā **Statuss** atlasiet **Iegrāmatots**.
   6. Laukā **Drukāts** atlasiet opciju.

## <a name="control-collection-letters-at-the-customer-level"></a>Atgādinājuma vēstuļu pārvaldība debitora līmenī
Varat arī iestatīt atgādinājuma vēstules debitora līmenī, un tādējādi tiks izsekots katras transakcijas atgādinājuma vēstules kods, bet atgādinājuma vēstuļu apstrādes pamatā būs viens atgādinājuma vēstuļu līmenis, kas saglabāts par debitoru. Viena atgādinājuma vēstule ietvers visas debitora nokavētās transakcijas. Tā kā pagarinājuma dienas tagad tiek izsekotas debitora līmenī, nākamā atgādinājuma vēstule netiek nosūtīta, līdz nav pagājis nākamās atgādinājuma vēstules nosūtīšanai noteiktais pagarinājuma dienu skaits, pat ja transakcijas tiek nokavētas pēc pēdējās atgādinājuma vēstules nosūtīšanas. Šī iespēja samazina katram klientam nosūtāmo atgādinājuma vēstuļu skaitu. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Debitora iestatīšana atgādinājuma vēstuļu pārvaldībai debitora līmenī
1.  Dodieties uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru parādu parametri** un noklikšķiniet uz cilnes **Iekasēšana**. 
2.  Mainiet parametra **Izveidot atgādinājuma vēstuli katram** vērtību uz **Debitoram**. 
3.  Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules**. Katram debitoram tiks izveidota tikai viena atgādinājuma vēstule ar visām nokavētajām transakcijām.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu
Ja maksājumus un kredītrēķinus iekļaujat transakcijās, kas tiks iekļautas atgādinājuma vēstulēs, var būt tādi maksājumi vai kredītrēķini, kas aktivizēs atgādinājuma vēstules izveidi. Izmainot parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu** vērtību, varat pārvaldīt, kā maksājumi un kredītrēķini ietekmē atgādinājuma vēstules kodu. 

Lai ignorētu maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu, rīkojieties, kā norādīts tālāk.
1. Dodieties uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru parādu parametri** un noklikšķiniet uz cilnes **Iekasēšana**. 
2. Mainiet parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu vērtību** uz **Jā**.
