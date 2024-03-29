---
title: Kreditora bankas konta izveide
description: Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram.
author: GalynaFedorova
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b201f5eb2bf8eb496a761b6fc6ca729a46a85ce
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677847"
---
# <a name="create-a-vendor-bank-account"></a>Kreditora bankas konta izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.

1. Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.
2. Atlasiet piegādātāju, kam vēlaties izveidot bankas kontu, un tad noklikšķiniet uz saites **Piegādātāja konta ID**.
3. **Darbību rūtī** noklikšķiniet uz **Kreditors**.
4. Noklikšķiniet uz **Bankas konti**.
5. **Sadaļā Darbību rūts** noklikšķiniet uz **Jauns**.
6. Laukā **Bankas konts** ierakstiet vērtību. Šis ID tiks izmantots, lai identificētu bankas kontu kreditora ierakstam.  
7. Laukā **Nosaukums** ierakstiet kādu vērtību.
8. Laukā **Banku grupas** ievadiet vai atlasiet vērtību.
9. Laukā **Maršrutēšanas numura veids** atlasiet opciju. Šis ir maršrutēšanas numura tips, kas tiek izmantots starptautiskajiem maksājumiem.  
10. Laukā **Bankas konta numurs** ierakstiet vērtību.
11. Laukā **SWIFT kods** ievadiet vērtību.
12. Laukā **IBAN** ievadiet vērtību.
    - IBAN numuram ir jābūt pareizajā formātā. Piemēram, varat izmantot DE89370400440532013000.  
    - Bankas konta statuss ir Aktīvs, ja ir sasniegts Aktīvais datums un nav pārsniegts Beigu datums. Tas ir aktīvs arī tad, ja ir tukšs gan lauks Aktīvais datums, gan lauks Beigu datums. Ja gan lauka Aktīvais datums, gan lauka Beigu datums datumi vēl nav pienākuši, tad elektroniskie maksājumi nav pieejami. Citi maksājumu tipi ir pieejami un šis bankas konts ir aktīvs.  
13. Izvērsiet sadaļu **Iestatīšana**.
14. Laukā **Teksta kods** ievadiet vērtību. Šajā laukā ir norādīts kods, kas būs redzams saņēmēja bankas izrakstā.  
15. Laukā **Ziņojums bankai** ierakstiet vērtību.
16. Ievadiet vērtību laukā **Maiņas atsauce**. Šis ir atsauces numurs jebkuram turpmākā vai fiksēta termiņa maiņas kursam.
17. Laukā **Valūta** ievadiet vai atlasiet vērtību. Kad tiek izsniegtas pārbaudes, šajā sadaļā ir sniegts apskats par to statusu (gaida vai apstiprināts).  
18. Izvērsiet sadaļu **Adrese**.
19. Izvērsiet sadaļu **Iepriekšējas piezīmes**.
20. Izvērsiet sadaļu **Kontaktinformācija**.
21. Laukā **Tālrunis** ievadiet vērtību.
22. Aizvērt lapu.
23. Noklikšķiniet uz **Rediģēt**.
24. Izvērsiet sadaļu **Maksājums**.
25. Laukā **Bankas konts** atlasiet kontu, ko tikko izveidojāt.
26. Noklikšķiniet uz **Saglabāt**. Šo adresi var pārmantot no banku grupas, ja tāda ir norādīta, vai šeit varat to pievienot.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]