---
title: POS atļauju grupu izveide
description: Šajā rakstā ir izskaidrots, kā izveidot POS atļauju grupu.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277965"
---
# <a name="create-pos-permission-groups"></a>POS atļauju grupu izveide

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izveidot POS atļauju grupu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT. Šis uzdevums ir paredzēts tirdzniecības operāciju pārvaldnieka lomai.

1. Navigācijas rūtī ejiet uz **Moduļi > Mazumtirdzniecība un tirdzniecība > Darbinieki > Atļauju grupas**.
2. Atlasiet **Jauns**.
3. Laukā **POS atļauju grupas ID** ierakstiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Atlasiet **Jā** laukā **Skatīt pulksteņa ierakstus**. Tagad var iespējot vai atspējot dažādas atļaujas POS atļauju grupā. Daļai atļauju var iestatīt vērtību, kas tiks izmantota, lai novērtētu, vaI POS lietotājs var veikt darbību. Šajā uzdevuma ceļvedī iespējosit dažas atļaujas, ko var piešķirt kasierim.  
6. Atlasiet **Jā** laukā **Atļaut izveidot pasūtījumu**.
7. Atlasiet **Jā** laukā **Atļaut rediģēt pasūtījumu**.
8. Atlasiet **Jā** laukā **Atļaut izgūt pasūtījumu**.
9. Atlasiet **Jā** laukā **Atļaut paroles maiņu**.
10. Atlasiet **Jā** laukā **Atļaut aklo aizvēršanu**.
11. Atlasiet **Saglabāt**. Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas tirdzniecības kanāliem. 
12. Navigācijas rūtī ejiet uz **Moduļi > Cilvēkresursi > Amati > Amati**.
13. Tagad POS atļauju grupu piešķirsim darbam. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Atlasiet **Rediģēt**.
15. Izvērsiet sadaļu **Amata klasifikācija**.
16. Laukā POS atļauju grupa ievadiet vai atlasiet vērtību. Šīs POS atļauju grupas iestatījumus izmantos visi darbinieki ar šim darbam atbilstošu amatu, ja vien darbinieku POS atļaujas netika ignorētas to amata līmenī.  
17. Atlasiet **Saglabāt**. Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas kanāliem.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
