---
title: Pirkšanas līguma izveide
description: Šajā tēmā aprakstīta pirkšanas līguma izveide.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fb3d397b277429954ef91e13445189fe21560b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237207"
---
# <a name="create-a-purchase-agreement"></a>Pirkšanas līguma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīta pirkšanas līguma izveide. Parasti to veic pirkšanas pārvaldnieks. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākt, jāiestata pirkšanas līgumu klasifikācijas. Kad esat izveidojis vienošanos, to var izmantot, veidojot PP, un šādi pirkšanas līguma nosacījumi tiks kopēti virsrakstā un jebkurās pasūtījuma rindās, kuras līgums ietekmē.


## <a name="create-a-new-purchase-agreement"></a>Jauna pirkšanas līguma izveide
1. Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Pirkšanas līgumi >Pirkšanas līgumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Piegādātāja konts** atlasiet nolaižamo izvēlni un atlasiet vēlamā ieraksta rindu.
4. Laukā **Pirkšanas līguma klasifikācija** atlasiet nolaižamo izvēlni un atlasiet vēlamā ieraksta rindu.
5. Izvērsiet kopsavilkuma cilni **Vispārīgi**.
6. Laukā **Izbeigšanās datums** ievadiet datumu.

    - Beigu datums būs noklusējuma datums visām saistību rindām un noteiks, cik ilgi katra saistība ir spēkā.  

7. Laukā **Dokumenta nosaukums** ierakstiet pirkšanas līguma nosaukumu.

    - Lauku **Noklusējuma saistības** atstājiet iestatītu kā **Produkta daudzuma saistības** (vai mainiet, ja tas tā nav iestatīts).  
    - Noklusējuma saistību vērtība nosaka jūsu opcijas līguma rindās. Ja jums ir nepieciešams jauns saistību tips, veidojot līguma rindas, ir jāmaina noklusējuma saistības virsrakstā. Ir 4 saistību veidi: **Produkta daudzuma saistības** noteiktam produkta daudzumam, **Produkta vērtības saistības** noteiktam produkta valūtas daudzumam, **Produkta kategorijas vērtības saistības** noteiktai valūtas summai iepirkuma kategorijā, kad vērtība var būt kataloga vienumam vai ne kataloga vienumam, **Vērtības saistība** noteiktam valūtas daudzumam, ko var sasniegt noteiktam produktam vai iepirkumu kategorijai.  

8. Atlasiet **Labi**.

## <a name="add-a-commitment"></a>Saistību pievienošana
1. Atlasiet **Pievienot rindu**.
2. Laukā **Vienuma numurs** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.
3. Laukā **Daudzums** ierakstiet kādu skaitli. Tas ir kopējais daudzums, kuru vienojāties iegādāties no kreditora.  
4. Laukā **Vienības cena** ievadiet kādu skaitli.
5. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
6. Opciju **Ir iestatīts maksimālais** iestatiet kā **Jā**. Opcija **Ir iestatīts maksimālais** ierobežo saistības izmantošanu. Varat iegādāties tikai daudzumu, kas norādīts laukā **Daudzums** rindai.  

## <a name="add-header-conditions"></a>Virsraksta nosacījumu pievienošana
1. Darbību rūtī atlasiet **Opcijas**.
2. Atlasiet **Mainīt skatu**.
3. Atlasiet **Galvenes skats**.
4. Izvērsiet sadaļu **Noteikumi**.
5. Laukā **Maksājumu metode** nolaižamajā sarakstā atlasiet vēlamo ierakstu. Maksājuma nosacījumi no kreditora konta tiek šeit rādīti pēc noklusējuma.  
6. Laukā **Piegādes metode** nolaižamajā sarakstā atlasiet vēlamo ierakstu.
7. Laukā **Piegādes noteikumi** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.

## <a name="confirm-and-activate-the-agreement"></a>Līguma apstiprināšana un aktivizēšana
1. Darbību rūtī atlasiet **Pirkšanas līgums**.
2. Atlasiet **Apstiprināšana**. Iestatiet opciju **Atzīmēt līgumu kā spēkā esošu** kā **Jā**.  
3. Atlasiet **Labi**.
4. Darbību rūtī atlasiet **Pirkšanas līgums**.
5. Atlasiet **Pirkšanas līguma apstiprinājumi**. Opcija **Priekšskatījums/drukāt** ļauj drukāt pirkšanas līgumu, ko pēc tam drukāt un nosūtīt piegādātājam. Ja atjaunināt līgumu vēlāk un atkārtoti to apstiprināt, abas versijas tiks parādītas šeit.  
6. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]