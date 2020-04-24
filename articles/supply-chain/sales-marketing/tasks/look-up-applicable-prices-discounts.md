---
title: Attiecināmo cenu un atlaižu pārlūkošana
description: Šajā procedūrā parādīts, kā atrast cenu un/vai atlaidi precei, kas pašlaik derīga noteiktam debitoram, neizveidojot pārdošanas pasūtījumu.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ea4c7db203d0b47c59b241c9d89c69c71cf6cb1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211932"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Attiecināmo cenu un atlaižu pārlūkošana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā atrast cenu un/vai atlaidi precei, kas pašlaik derīga noteiktam debitoram, neizveidojot pārdošanas pasūtījumu. Procedūra palīdz veikt konkrētu piemēru, un, lai atlasītu nepieciešamās vērtības, ir nepieciešams sekot piemēram, izmantojot USMF demonstrācijas uzņēmumu.


## <a name="find-the-applicable-price"></a>Piemērojamās cenas atrašana
1. Dodieties uz sadaļu Pārdošana un mārketings > Cenas un atlaides > Atrast cenas.
2. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet debitoru US-001.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Krājuma kods ierakstiet T0004.
    * Pēc noklusējuma lauka Daudzums vērtības iestatījums ir 1. Tomēr, ja zināt konkrētas preces pasūtījuma apjomu, ko veiks debitors, tad ievadiet tā vērtību. Šī informācija ir būtiska, ja tirdzniecības līgumos ar debitoru pastāv daudzumu pārtraukumi, t.i., preces cena ir atkarīga no minimālā iepirktā daudzuma.  
6. Laukā Datums ievadiet datumu, kad debitors plāno veikt pasūtījumu. 
    * Datums var būt šodienas datums vai jebkurš datums nākotnē.  
    * Sistēma tagad atgriež cenu, kura atbilst atlasītajai precei, kad atlasītais debitors to pērk atlasītajā datumā un norādītajā daudzumā. Šajā piemērā, ja debitors US-001 pērk 1 preces T0004 vienību šodien, tam būs jāmaksā 350 CAD par vienību. Šī cena tiek ņemta no esošā un aktīvā tirdzniecības līguma ar debitoru.      Citi lauki lapā sniedz papildinformāciju par preces cenu un preces izmaksām (ja iestatīts preču šablonā), un aprēķināto ienesīgumu.  
    * Ja ir atlasīta opcija Rādīt saistītās preces variantus, tas nozīmē, ka ir papildu tirdzniecības līgumi preces variantiem.  
7. Atzīmējiet izvēles rūtiņu Rādīt saistītos preces variantus.
    * Preču variantu saraksts tiek parādīts kopā ar informāciju par to dimensijām.  
8. Sarakstā iezīmējiet Baltās krāsas rindu.
    * Ņemiet vērā, ka preces cena tagad atšķiras no iepriekš parādītās, kad dimensijas nebija norādītas.  
9. Noklikšķiniet uz Skatīt pārdošanas cenas.
    * Lapā Cena (pārdošana) tiek parādīti visi tirdzniecības līgumi, kas attiecas uz preci, tostarp tās variantiem.  
10. Aizvērt lapu.

## <a name="find-the-applicable-discount"></a>Piemērojamās atlaides atrašana
Pārliecinieties, ka laukā Debitora konts ir norādīts klienta numurs US-001    
1. Laukā Krājuma kods ierakstiet T0012.
    * Pārliecinieties, ka laukā Daudzums vērtība ir iestatīta uz 1.  
    * Parādītās papildinformācijas par cenu noteikšanu precei T0012 dati nāk no viena vai vairākiem tirdzniecības līgumiem: vienības cena ir 1000 CAD un atlaides procents ir 5.  
2. Daudzuma laukā iestatiet vērtību 20.
    * Palielināts pasūtījuma daudzums nodrošinās, ka rindas atlaide, kas tiks piedāvāta debitoram, manīsies no 5 uz 7 procentiem.  
    * Neto summa tiek aprēķināta, pamatojoties uz vienības cenu, atlaidi un kopējo daudzumu.  
3. Noklikšķiniet uz Skatīt rindas atlaidi.
    * Precei T0012 ir divi rindas atlaides līgumi, kuros 5 procentu atlaide norādīta pasūtījuma rindas daudzumam no 1 līdz 10 un 7 procentu atlaide pasūtījuma daudzumam virs 10. Ievērojiet, ka atlaides tiek lietots preču grupai, šajā piemērā, Grupas kodam 01, kura daļa ir prece T0012.  
4. Aizvērt lapu.

