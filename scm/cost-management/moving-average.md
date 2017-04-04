---
title: "Pārvieto vidējo vērtību"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-17 15 - 16 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e75016694e63dbc26f8d4c4ae73204966ca28dcf
ms.lasthandoff: 03/29/2017


---

# <a name="moving-average"></a>Pārvieto vidējo vērtību



Tālāk ir norādīti priekšnoteikumi, lai izmantotu slīdošās vidējās izmaksas kā izmaksu aprēķināšanas metodi.
1.  Lapā **Krājumu modeļu grupas** iestatiet krājumu modeļu grupu, kam ir atlasīta lauka **Krājumu modelis** vērtība Pārvieto vidējo vērtību.
    | **Piezīme. **                                                                                                                                |
    |-----------------------------------------------------------------------------------------------------------------------------------------|
    | Pēc noklusējuma, Ja ir atlasīta opcija Pārvieto vidējo vērtību, tiek atlasīti arī lauki **Grāmatot fiziskos krājumus** un **Grāmatot finanšu krājumus**. |

2.  Lapā **Grāmatošana** piešķiriet kontus **Cenas atšķirība vidējās vērtības pārvietošanai** un **Izmaksu pārvērtēšana vidējās vērtības pārvietošana** cilnē **Krājumi**. Konts **Cenas atšķirība vidējās vērtības pārvietošanai** tiek izmantots, ja izmaksas ir proporcionāli jāiekļauj izdevumos. To izraisa izmaksu atšķirības pirkšanas ieejas plūsmas dokumentā un pirkšanas rēķinā, kā arī atšķirības starp sākotnējo krājumu daudzumu un pašreizējo rīcībā esošo daudzumu. Izmantojiet kontu **Izmaksu pārvērtēšana vidējās vērtības pārvietošanai**, ja vēlaties koriģēt preces slīdošās vidējās izmaksas, piešķirot jaunu vienības cenu.
3.  Lapā **Izlaistās preces** piešķiriet precei slīdošā vidējā krājumu modeļu grupu.

| **Piezīme. **                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Krājumu slēgšanas process izraisa tika uzskaites perioda slēgšanu. Tā neietekmē preces, kam ir piešķirts slīdošā vidējā krājumu modeļu grupa. |

## <a name="convert-to-the-moving-average-costing-method"></a>Konvertēšana uz slīdošā vidējā izmaksu aprēķināšanas metodi
Preces var konvertēt slīdošā vidējā krājumu novērtēšanas metodes izmantošanai. Šāda veida konvertēšana parasti tiek veikta gada beigās pēc pašreizēja gada pēdējā mēneša slēgšanas. Tas tiek izdarīts, izmantojot preces pašreizējo izmaksu aprēķināšanas modeli. Varat mainīt krājumu izmaksu aprēķināšanas metodi no izmaksu aprēķināšanas metodes, kuras pamatā ir vidējās izmaksas vai standarta izmaksas, uz metodi, kuras pamatā ir slīdošais vidējais. Ja maināt izmaksu aprēķināšanas metodi no standarta izmaksu aprēķināšanas metodes uz slīdošā vidējā metodi, ir jāizpilda tālāk norādītie uzdevumi.
1.  Veiciet korekcijas, lai samazinātu krājumu daudzumu un vērtības līdz 0 (nullei).
2.  Kad krājumu vērtība un daudzums ir 0 (nulle), mainiet krājumu modeļu grupu uz slīdošā vidējā grupu.
3.  Veiciet korekcijas, lai atjaunotu krājumu daudzumu un vērtību.

Krājumu izmaksu aprēķināšanas metodi nevar mainīt no slīdošā vidējā metodes uz metodi Pirmie iekšā, pirmie ārā (FIFO), Pēdējie iekšā, pirmie ārā (LIFO) vai svērtā vidējā metodi.
| **Piezīme. **                                                                      |
|-------------------------------------------------------------------------------|
| Konvertēšana no standarta izmaksām uz slīdošām svērtajām vidējām izmaksām ir manuāls process. |

Tālāk sniegtajos piemēros ir parādīta ietekme, ko rada slīdošā vidējā izmaksu aprēķināšanas metodes izmantošana. Ir pieejamas četras konfigurācijas.
-   Pirkšanas pasūtījums un izdevumos proporcionāli iekļauto izmaksu atšķirība
-   Preču un krājumu korekcija, izmantojot slīdošo vidējo
-   Slīdošā vidējā izmantošana ražošanā
-   Slīdošā vidējā izmantošana transakcijās ar atpakaļejošu datumu

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Pirkšanas pasūtījums un izdevumos proporcionāli iekļauto izmaksu atšķirība
Izmantojot slīdošo vidējo, preces izmaksas tiek noteiktas pēc pirkšanas ieejas plūsmas. Ja, grāmatojot pirkšanas rēķinu, pastāv izmaksu atšķirības pirkšanas ieejas plūsmas dokumentā un pirkšanas rēķinā, starpība tiek proporcionāli koriģēta pašlaik krājumos esošajām precēm un visa atlikusī summa tiek iekļauta izdevumos. Šajā piemērā tiek izveidots un saņemts pirkšanas pasūtījums, kurā norādītās izmaksas neatbilst grāmatotajā pirkšanas rēķinā norādītajām izmaksām.
1.  Izveidojiet pirkšanas pasūtījumu, norādot daudzumu 2 un vienības cenu 10,00.
2.  Izveidojiet preces pirkšanas ieejas plūsmas dokumentu.
3.  Izveidojiet pārdošanas pasūtījumu, norādot daudzumu 1 un vienības cenu 10,00.
4.  Izveidojiet pirkšanas rēķinu, norādot daudzumu 2 un vienības cenu 12,00.

Grāmatojot pirkšanas rēķinu, vienības cenu atšķirība 2,00 tiek grāmatota kontā Cenas atšķirība vidējās vērtības pārvietošanai. Tā notiek tāpēc, ka tika nopirktas divas preces, radot izmaksas 20,00. Viena no precēm tika pārdota par vienības cenu 10,00. Iepirkuma rēķins iegrāmatots 12.00 ar daudzumu 2 vienības cenu. Produkta vienības cenu nevar iegrāmatot 14.00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Preču un krājumu korekcija, izmantojot slīdošo vidējo
Ja ir nepieciešams koriģēt preces slīdošās vidējās izmaksas, var veikt krājumu korekciju no šodienas datuma. Preces slīdošās vidējās izmaksas nevar labot, izmantojot krājumu korekciju ar atpakaļejošu datumu. Nevar izmantot izmaksu plūsmu secīgās transakcijās. Šajā piemērā tiek koriģētas preces slīdošās vidējās izmaksas.
1.  Atlasiet preci, kam vēlaties koriģēt slīdošās vidējās izmaksas.
    | **Note**                                                                                    |
    |---------------------------------------------------------------------------------------------|
    | * * Mainīgā vidējā pārvērtēšanu * * lapas izskata pieejamo produktu krājumu. |

    Atlasītās preces grāmatotais daudzums ir 1, grāmatotā vērtība ir 12,00, grāmatotās vienības izmaksas ir 12,00 un vienības izmaksas ir 12,00.
2.  Atjauniniet lauka **Vienības izmaksas** vērtību uz 16,00. Sistēmā tiek aprēķinātas pārējo lauku vērtības.
3.  Korekcija tiek grāmatota.

| **Piezīme. **                                                        |
|-----------------------------------------------------------------|
| Slīdošās vidējās izmaksas var koriģēt tikai no šodienas datuma. |

Lapā **Dokumenta segšanas darbības** varat redzēt, ka kontā Izmaksu pārvērtēšana vidējās vērtības pārvietošanai ir grāmatota korekcija 4,00.

## <a name="moving-average-with-production"></a>Slīdošā vidējā izmantošana ražošanā
Slīdošo vidējo var izmantot saražotajiem krājumiem. Ja jūs plānojat izmantot slīdošo vidējo ražošanas vidē, **izmantot paredzamo izmaksu cenu** slīdni ar * * ražošanas kontroles parametri * * lapā vajadzētu būt selcted. Tas nozīmē, ka faktiskās MK aprēķina izmaksu cenas vietā tiek izmantota novērtēšanas laikā aprēķinātā izmaksu cena.

## <a name="moving-average-with-a-backdated-transaction"></a>Slīdošā vidējā izmantošana transakcijās ar atpakaļejošu datumu
Transakcijām ar atpakaļejošu datumu tiek piešķirtas pašreizējas slīdošās vidējās izmaksas, un tiek atjaunināti preces fiziskie krājumi, taču netiek ietekmētas preces vidējās slīdošās izmaksas. Šajā slīdošā vidējā izmantošanas piemērā tiek grāmatota vidējās slīdošās vērtības preces transakcija ar atpakaļejošu datumu.
1.  Izveidojiet krājumu korekciju slīdošā vidējā precei, norādot daudzumu 1 un izmaksas 20,00.
2.  Preces krājumu transakciju vēsture satur tālāk norādīto.
    -   Krājumu transakcija ar daudzumu 1, izmaksām 16,00, grāmatošanas datumu 15. janvāris un transakcijas datumu 15. janvāris.
    -   Krājumu korekcija ar daudzumu 1, izmaksām 20,00, grāmatošanas datumu 1. janvāris un transakcijas datumu 15. janvāris.

3.  Grāmatojiet korekciju.

Lapā **Krājumu darbības** ir redzams, ka izdevumos ir iekļauta summa 4,00, jo preces pašreizējās slīdošās vidējās izmaksas ir 16,00. Varat grāmatot ar atpakaļejošu datumu, taču izmaksu atšķirība tiek iekļauta izdevumos, tāpēc netiek ietekmētas slīdošās vidējās izmaksas.

## <a name="inventory-value-report"></a>Krājumu vērtības pārskats
Šajā slīdošā vidējā izmantošanas piemērā tiek drukāts krājumu vērtības pārskats, lai atvieglotu preces pašreizējās vidējās slīdošās vērtības aprēķinu. Krājumu vērtības pārskatā var hronoloģiskā secībā iekļaut transakcijas kopā ar izmaksām, lai atvieglotu preces slīdošo vidējo izmaksu aprēķinu. Pārskatā ir redzamas preces slīdošās vidējās izmaksas. Dialoglodziņa **Krājumu vērtības pārskati** laukā Datumu intervāls varat atlasīt vērtību **Darījuma laiks** vai **Grāmatošanas datums**, lai norādītu pārskata kārtošanas veidu. Parasti pārskats tiek drukāts, izmantojot opciju **Grāmatošanas datums**. Opcija **Darījuma laiks** atbilst faktiskajam datumam, kad tiek ziņots par transakciju un tiek atjauninātas preces slīdošās vidējās izmaksas. Varat drukāt krājumu vērtības pārskatu, izmantojot kārtošanas opciju **Darījuma laiks**, ja vēlaties skatīt slīdošo vidējo izmaksu aprēķinu laika gaitā. Tālāk esošajā tabulā ir redzamas tās prece transakcijas, kam tiek drukāts pārskats, izmantojot kārtošanas opciju **Darījuma laiks**.

| Darījuma laiks | Datums         | Darījuma veids           | Daudzums | Summa | Vidējās vienības izmaksas |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktobris    | Sākuma bilance          | 0        | 0,00   | 0,00              |
| 8. oktobris        | 28. septembris | Ieejas plūsma ar atpakaļejošu datumu          | formāts 1. proc.        | 16,00  | 16,00             |
| 3. oktobris        | 3. oktobris    | Pirkšanas ieejas plūsma           | 2        | 20,00  | 12,00             |
| 5. oktobris        | 5. oktobris    | Pārdošanas pasūtījums                | -1       | -10,00 | 13,00             |
| 7. oktobris        | 7. oktobris    | Pirkšanas rēķins           |          | 2,00   | 14,00             |
| 8. oktobris        | 8. oktobris    | Vidējās pārvērtēšanas pārvietošana |          | 4,00   | 16,00             |
|                  | 31. oktobris   | KOPĀ                      | 2        | 32,00  | 16,00             |

 

| **Piezīme. **                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kārtošanas opciju **Darījuma laiks** nevar izmantot virsgrāmatas un krājumu saskaņošanai. Pārskats ir jādrukā, izmantojot opciju **Grāmatošanas datums**. |




