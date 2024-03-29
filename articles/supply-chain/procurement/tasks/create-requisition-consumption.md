---
title: Patēriņa pieprasījuma izveide
description: Šajā rakstā aprakstīts pieprasījuma izveides process.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4fc4a9f0dbd5c413300d27640512df69df30122
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888475"
---
# <a name="create-a-requisition-for-consumption"></a>Patēriņa pieprasījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā rakstā aprakstīts pieprasījuma izveides process. Tajā parādīti dažādi veidi, kā meklēt preces sagādes katalogā un kā pievienot preci, kas nav katalogā. Pirms sākt šo procedūru, jums ir jāiestata pirkšanas ierobežojumus uz Patēriņš kā pieprasījumu noklusējuma tipu. Šo procedūru var izmēģināt, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus. Šo procedūru var veikt tikai no lietotāja profila, kas ir iestatīts kā darbinieks. Šo uzdevumu parasti veic darbinieks. **Darbinieka** pieņemšanas darbā drošības loma ļaus veikt uzdevumus, vai, ja izmantojat USMF, varat pieteikties kā **Alicia**.


## <a name="create-a-new-requisition"></a>Jauna pieprasījuma izveide
1. Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Manis sagatavotie pirkšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** dodiet pieprasījumam nosaukumu.
4. Laukā **Pieprasītais datums** ievadiet datumu. Pēc noklusējuma, pieprasījuma datums un uzskaites datums tiek kopēti uz pirkšanas pieprasījuma rindām. Tos var mainīt rindas līmenī. Pieprasītais datums ir pieprasītais piegādes datums.  
5. Laukā **Uzskaites datums** ievadiet datumu. Uzskaites datums tiek izmantots, lai grāmatotu uzskaites ierakstu virsgrāmatā un pārbaudītu pieejamos budžeta līdzekļus.  
6. Atlasiet **Labi**.
7. Laukā **Iemesls** atlasiet opciju no nolaižamās izvēlnes. Darījuma pamatojuma iemesls, ko atlasījāt, pēc noklusējuma tiek parādīts pirkšanas pieprasījuma rindās, bet to var mainīt rindas līmenī.  
8. Atlasiet iemeslu.
9. Laukā **Detalizēta informācija** ievadiet aprakstošu pieprasījuma pamatojumu.

## <a name="add-a-line-to-the-requisition"></a>Rindas pievienošana pieprasījumam
1. Atlasiet **Pievienot rindu**. Ir divi veidi, kā pievienot rindas pirkšanas pieprasījumam. Ja jūs jau zināt preces numuru vai jau zināt, ka jūs pieprasāt preci, kas nav preču katalogā, tad varat pievienot rindu tieši ar **Pievienot rindu**. Cits veids ir izmantot **Pievienot preces**, kur varat izmantot meklēšanu un filtrēšanu, lai atrastu vienumus preču katalogā.    
2. Atlasiet tikko izveidoto rindu.
    - Pieprasītājs ir darbinieks, kas ir pieprasījis šo pieprasījumu.   
    - Pēc noklusējuma persona, kas sagatavo pieprasījumu, ir darbinieks, kurš ir to pieprasījis. Jums ir jābūt atļaujai sagatavot pieprasījuma rindu cita darbinieka vārdā. Ja jums ir šādas atļaujas, tad šajā uzmeklēšanā parādīsies citi darbinieki.  
3. Laukā **Krājuma kods** ierakstiet vērtību. Krājumus, kas ir pieejami izvēlei, ierobežo kategorijas piekļuves ierobežojumi un pērkošas juridiskās personas sagādes katalogs.   
4. Laukā **Daudzums** ierakstiet kādu skaitli.

## <a name="add-more-products-to-the-requisition"></a>Vairāku preču pievienošana pieprasījumam
1. Atlasiet **Pievienot preces**. Tā ir opcija, kur var meklēt preces preču katalogā.    
2. Laukā **Atrast sagādes kategorijas līmeni** ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam atlasiet **Enter**. Piemēram, ievadiet `comput`.  
3. Izmantojiet saīsni **InvokeDefaultButton**.
4. Izmantojiet **Filtrēt**, lai filtrētu preču sarakstu atlasītajā kategorijā.
5. Atlasiet preces karti, ko vēlaties pievienot pieprasījumam.
6. Atlasiet **Pievienot rindām**.
7. Laukā **Daudzums** ierakstiet kādu skaitli.
8. Laukā **Atrast sagādes kategorijas līmeni** ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam atlasiet **Enter**. Piemēram, ievadiet `High` (marķieri).  
9. Izmantojiet saīsni **InvokeDefaultButton**.
10. Atlasiet **Pievienot rindām neuzskaitītas preces**, lai pievienotu preci, kas nav norādīta sagādes katalogā.
11. Laukā **Preces nosaukums** ierakstiet vērtību.
12. Laukā **Vienība** ierakstiet vērtību.
13. Atlasiet **Labi**.
14. Laukā **Krājuma apraksts** pievienojiet preces aprakstu.
15. Laukā **Daudzums** ierakstiet kādu skaitli.
16. Laukā **Vienības cena** ievadiet kādu skaitli. Ja jūs zināt cenu konkrētam kreditoram (kuru atlasījāt laukā Kreditora konts), tad šo cenu var ievadīt.   
17. Laukā **Kreditora konts** atveriet nolaižamo sarakstu, lai atlasītu opciju. Kreditori, kas ir pieejamai šajā laukā, ir atkarīgi no pirkšanas ierobežojumiem un statusa, kurš kreditoram ir pašreizējai kategorijai. Kā alternatīvu kreditora atlasei šeit, varat atlasīt **Ieteikt kreditoru**.    
18. Sarakstā atlasiet kreditoru, kuru vēlaties izmantot.
19. Laukā **Ārējais krājuma kods** ierakstiet kādu vērtību. Tas ir preces atsauces numurs, kas ir zināms kreditoram. Piemēram, tas varētu būt preces krājumu kods kreditora katalogā.  
20. Atlasiet **Labi**.

## <a name="distribute-amounts"></a>Sadaliet summas
1. Atlasiet **Finanses**.
2. Atlasiet **Sadalījuma summas**. Šajā procesā ir parādīts, kā sadalīt pirmās rindas izmaksas starp 2 kontiem. To var izdarīt arī vēlāk, ja pieprasījums tiks pārskatīts.  
3. Atlasiet **Sadalīt**, lai izveidotu sadales rindu.
4. Laukā **Virsgrāmatas konts** atlasiet pirmo izmaksu centru, kam jāuzņemas daļa no izmaksām.
5. Atlasiet citu sadales rindu.
6. Laukā Virsgrāmatas konts norādiet otro izmaksu centru.
7. Atlasiet **Sadalīt vienādi**.
8. Aizvērt lapu.

## <a name="view-line-details"></a>Skatīt rindu detalizētu informāciju
1. Pārslēdziet sadaļas **Detalizēta rindas informācija** paplašinājumu.

## <a name="submit-the-requisition"></a>Pieprasījuma iesniegšana
1. Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.
2. Atlasiet **Iesniegt**.
3. Aizvērt lapu.
4. Laukā **Komentārs** ierakstiet piezīmi pieprasījuma apstiprinātājam.
5. Atlasiet **Iesniegt**.
6. Aizvērt lapu.
7. Atsvaidziniet lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]