---
title: Procentu apstrāde
description: Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4f1ed6d0199235e946d55dfa904246c109acba42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220135"
---
# <a name="process-interest"></a>Procentu apstrāde

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Iestatiet grāmatošanas metodes procentus.
1. **Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Iestatīšana >Klientu grāmatošanas profili**.
2. Noklikšķiniet uz **Rediģēt**.
3. Kopsavilkuma cilnē **Uzstādīšana**, laukā **Procentu kods** ievadiet procentu kodu no nolaižamā saraksta. Ja nevēlaties veikt procentu aprēķinu transakcijām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu. Kopsavilkuma cilne **Tabulas ierobežojumi** ļauj jums mainīt veidu, kādā tiek apstrādāti procenti. Ja šajā laukā ir iestatīts Jā, procenti šai grāmatošanas metodei tiks aprēķināti.  

## <a name="calculate-interest"></a>Aprēķināt procentus
1. **Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Soda nauda >Izveidot soda naudas piezīmes**.
2. Atlasiet transakciju veidus, kuriem aprēķināsit procentus. Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.  
3. Ja iestatāt **Procentus** uz 'Jā', jūs aprēķināsit procentus par procentiem. Pirms šo transakciju pievienošanas, iespējams, vēlēsities pārbaudīt likumus, kas regulē procentu aprēķināšanu procentiem.  
4. Laukā **Datums no** ievadiet datumu, no kura tiks aprēķināti procenti. Ja jums nav konkrēta **Datuma no**, tad visi negrāmatotie procentu paziņojumi tiks atcelti un procenti tiks atkārtoti aprēķināti no darījuma datuma.
5. Laukā **Datums līdz** ievadiet datumu, līdz kuram tiktu aprēķināti procenti.
6. Laukā **Izmantot grāmatošanas profilu no** atlasiet opciju. Ir trīs grāmatošanas profila opcijas:
    - Konts — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi. 
    - Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.
    - Transakcija — izmantot katram procentu paziņojumam atsevišķu grāmatošanas metodi transakcijām, par kurām tiek aprēķināti procenti. Transakcijām, kurām nav piešķirta grāmatošanas metode, tiek izmantota grāmatošanas metode, kura ir norādīta veidlapas Debitoru parametri apgabalā Virsgrāmata un PVN formā.  
7. Izvērtiet cilni **Iekļaujamie ieraksti**.
8. Noklikšķiniet uz **Filtrēt**.
9. Laukā **Kritērijs** ievadiet debitora ID. Piemēram, ievadiet US-001.
6. Noklikšķiniet uz **Labi**.
7. Noklikšķiniet uz **Labi**.

## <a name="print-interest-notes"></a>Drukāt procentu paziņojumus
1. **Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Procenti >Izskatīt un apstrādāt procentu piezīmes**.
2. Laukā **Statuss** atlasiet 'Izveidots'.
3. Laukā **Drukāts** atlasiet 'Nav drukāts'.
4. Noklikšķiniet uz **Drukāt**.
5. Izvērtiet cilni **Iekļaujamie ieraksti**.
6. Noklikšķiniet uz **Labi**.
7. Aizvērt lapu.

## <a name="post-the-interest-note"></a>Procentu paziņojuma grāmatošana
1. Atlasiet procentu paziņojumu, kas ir gatavs grāmatošanai (statuss ir Izveidots).
2. Noklikšķiniet uz **Grāmatot**.
3. Ievadiet procentu paziņojuma grāmatošanas datumu. Lai katram procentu paziņojumam izveidotu Virsgrāmatas transakciju, atlasiet Jā. Ja neatlasāt vērtību Jā, visi debitora procentu paziņojumu procenti tiek uzkrāti un grāmatoti Virsgrāmatā vienā transakcijā.  
4. Izvērtiet cilni **Iekļaujamie ieraksti**.
5. Noklikšķiniet uz **Labi**.
6. Laukā **Statuss** atlasiet 'Iegrāmatots'.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]