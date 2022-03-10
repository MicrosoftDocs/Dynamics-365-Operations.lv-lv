---
title: Pārvieto vidējo vērtību
description: Slīdošā vidējā metode ir pastāvīgo izmaksu aprēķināšanas metode, kuras pamatā ir vidējā vērtība un kuras ietvaros krājumu izdošanas izmaksas nemainās, kad mainās pirkšanas izmaksas. Starpība tiek kapitalizēta, pamatojoties uz proporcionālu aprēķinu. Atlikusī summa tiek iekļauta izdevumos.
author: AndersGirke
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6721c01fd0ad3eec30de99dee3b5e98de6bd3b52
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567539"
---
# <a name="moving-average"></a>Pārvieto vidējo vērtību

[!include [banner](../includes/banner.md)]

Slīdošā vidējā metode ir pastāvīgo izmaksu aprēķināšanas metode, kuras pamatā ir vidējā vērtība un kuras ietvaros krājumu izdošanas izmaksas nemainās, kad mainās pirkšanas izmaksas. Starpība tiek kapitalizēta, pamatojoties uz proporcionālu aprēķinu. Atlikusī summa tiek iekļauta izdevumos.

Ja lietojat slīdošā vidējā metodi, netiek atbalstīta krājumu nosegšana un krājumu iezīmēšana. Krājumu slēgšana neietekmē preces, kam kā krājumu modeļu grupa ir iestatīta slīdošā vidējā metode, un neizraisa nekādu segšanas darbību ģenerēšanu starp transakcijām.

Tālāk ir norādīti priekšnoteikumi, lai izmantotu slīdošās vidējās izmaksas kā izmaksu aprēķināšanas metodi.

1. Lapā **Krājumu modeļu grupas** iestatiet krājumu modeļu grupu, kam ir atlasīta vērtība **Slīdošais vidējais** laukā **Krājumu modelis**.

    > [!NOTE]
    > Pēc noklusējuma, ja ir atlasīta opcija **Slīdošais vidējais**, tiek atlasīti arī lauki **Grāmatot fiziskos krājumus** un **Grāmatot finanšu krājumus**.

1. Lapā **Grāmatošana** piešķiriet kontus **Cenas atšķirība slīdošajam vidējam**. Konts **Cenas atšķirība slīdošajam vidējam** tiek izmantots, kad izmaksas ir jāsedz proporcionāli. Tas notiek šādos divos scenārijos:
    - Pastāv izmaksu atšķirība pirkšanas ieejas plūsmas dokumentā un pirkšanas rēķinā, jo pastāv atšķirība starp sākotnējo krājumu daudzumu un pašreizējo rīcībā esošo daudzumu.
    - Darījumi noved krājumus no negatīva līdz nullei, un pastāv atšķirība starp darījuma izmaksām un pašreizējām slīdošā vidējā izmaksām.

1. Lapā **Grāmatošana** piešķiriet kontus kontiem **Cenas atšķirība slīdošajam vidējam** cilnē **Krājumi**. Konts **Izmaksu pārvērtēšana slīdošajam vidējam** tiek izmantots, kad vēlaties pielāgot preces slīdošā vidējā izmaksas jaunai vienības cenai.

1. Lapā **Izlaistās preces** piešķiriet precei slīdošā vidējā krājumu modeļu grupu.

    > [!NOTE]
    > Krājumu slēgšanas process izraisa tikai uzskaites perioda slēgšanu. Tā neietekmē preces, kam ir piešķirts slīdošā vidējā krājumu modeļu grupa.

## <a name="convert-to-the-moving-average-costing-method"></a>Konvertēšana uz slīdošā vidējā izmaksu aprēķināšanas metodi

Preces var konvertēt slīdošā vidējā krājumu novērtēšanas metodes izmantošanai. Šāda veida konvertēšana parasti tiek veikta gada beigās pēc pašreizēja gada pēdējā mēneša slēgšanas. Tas tiek izdarīts, izmantojot preces pašreizējo izmaksu aprēķināšanas modeli. Varat mainīt krājumu izmaksu aprēķināšanas metodi no izmaksu aprēķināšanas metodes, kuras pamatā ir vidējās izmaksas vai standarta izmaksas, uz metodi, kuras pamatā ir slīdošais vidējais.

Ja maināt izmaksu aprēķināšanas metodi no standarta izmaksu aprēķināšanas metodes uz slīdošā vidējā metodi, ir jāizpilda tālāk norādītie uzdevumi.

1. Veiciet korekcijas, lai samazinātu krājumu daudzumu un vērtības līdz 0 (nullei).
1. Kad krājumu vērtība un daudzums ir 0 (nulle), mainiet krājumu modeļu grupu uz slīdošā vidējā grupu.
1. Veiciet korekcijas, lai atjaunotu krājumu daudzumu un vērtību.

Krājumu izmaksu aprēķināšanas metodi nevar mainīt no slīdošā vidējā metodes uz metodi Pirmie iekšā, pirmie ārā (FIFO), Pēdējie iekšā, pirmie ārā (LIFO) vai svērtā vidējā metodi.

> [!NOTE]
> Konvertēšana no standarta izmaksām uz slīdošām svērtajām vidējām izmaksām ir manuāls process.

Tālāk sniegtajos piemēros ir parādīta ietekme, ko rada slīdošā vidējā izmaksu aprēķināšanas metodes izmantošana. Ir pieejamas četras konfigurācijas.

- Pirkšanas pasūtījums un izdevumos proporcionāli iekļauto izmaksu atšķirība
- Preču un krājumu korekcija, izmantojot slīdošo vidējo
- Slīdošā vidējā izmantošana ražošanā
- Slīdošā vidējā izmantošana transakcijās ar atpakaļejošu datumu

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Pirkšanas pasūtījums un izdevumos proporcionāli iekļauto izmaksu atšķirība

Izmantojot slīdošo vidējo, preces izmaksas tiek noteiktas pēc pirkšanas ieejas plūsmas. Ja, grāmatojot pirkšanas rēķinu, pastāv izmaksu atšķirības pirkšanas ieejas plūsmas dokumentā un pirkšanas rēķinā, starpība tiek proporcionāli koriģēta pašlaik krājumos esošajām precēm un visa atlikusī summa tiek iekļauta izdevumos.

Šajā piemērā tiek izveidots un saņemts pirkšanas pasūtījums, kurā norādītās izmaksas neatbilst grāmatotajā pirkšanas rēķinā norādītajām izmaksām.

1. Izveidojiet pirkšanas pasūtījumu, norādot daudzumu 2 un vienības cenu 10,00.
1. Izveidojiet preces pirkšanas ieejas plūsmas dokumentu.
1. Izveidojiet pārdošanas pasūtījumu, norādot daudzumu 1 un vienības cenu 10,00.
1. Izveidojiet pirkšanas rēķinu, norādot daudzumu 2 un vienības cenu 12,00.

Grāmatojot pirkšanas rēķinu, vienības cenu atšķirība 2,00 tiek grāmatota kontā Cenas atšķirība slīdošajam vidējam. Tā notiek tāpēc, ka tika nopirktas divas preces, radot izmaksas 20,00. Viena no precēm tika pārdota par vienības cenu 10,00. Tika grāmatos pirkšanas rēķins ar vienības cenu 12,00 un daudzumu 2. Nevar grāmatot preces vienības cenu 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Preču un krājumu korekcija, izmantojot slīdošo vidējo

Ja ir nepieciešams koriģēt preces slīdošās vidējās izmaksas, var veikt krājumu korekciju no šodienas datuma. Preces slīdošās vidējās izmaksas nevar labot, izmantojot krājumu korekciju ar atpakaļejošu datumu. Nevar izmantot izmaksu plūsmu secīgās transakcijās.

Šajā piemērā tiek koriģētas preces slīdošās vidējās izmaksas.

1. Atlasiet preci, kam vēlaties koriģēt slīdošās vidējās izmaksas. 

 > [!NOTE]
 > Lapā **Pārvērtēšana vidējās vērtības pārvietošanai** tiek pārbaudīti pieejamie preces krājumi. Atlasītās preces grāmatotais daudzums ir 1, grāmatotā vērtība ir 12,00, grāmatotās vienības izmaksas ir 12,00 un vienības izmaksas ir 12,00.
    
1. Atjauniniet lauka **Vienības izmaksas** vērtību uz 16,00. Sistēmā tiek aprēķinātas pārējo lauku vērtības.
1. Korekcija tiek grāmatota.

> [!NOTE]
> Slīdošā vidējā izmaksas var koriģēt tikai no šodienas datuma.

Lapā **Dokumenta segšanas darbības** varat redzēt, ka kontā Izmaksu pārvērtēšana slīdošajam vidējam ir grāmatota korekcija 4,00.

## <a name="moving-average-with-production"></a>Slīdošā vidējā izmantošana ražošanā

Slīdošo vidējo var izmantot saražotajiem krājumiem. Ja plānojat izmantot slīdošā vidējā metodi ražošanas vidē, atlasiet **Lietot novērtēto izmaksu cenu** lapā **Ražošanas kontroles parametri**. Tas nozīmē, ka faktiskās MK aprēķina izmaksu cenas vietā tiek izmantota novērtēšanas laikā aprēķinātā izmaksu cena.

## <a name="moving-average-with-a-backdated-transaction"></a>Slīdošā vidējā izmantošana transakcijās ar atpakaļejošu datumu

Transakcijām ar atpakaļejošu datumu tiek piešķirtas pašreizējas slīdošās vidējās izmaksas, un tiek atjaunināti preces fiziskie krājumi, taču netiek ietekmētas preces vidējās slīdošās izmaksas. Šajā slīdošā vidējā izmantošanas piemērā tiek grāmatota vidējās slīdošās vērtības preces transakcija ar atpakaļejošu datumu.

1. Izveidojiet krājumu korekciju slīdošā vidējā precei, norādot daudzumu 1 un izmaksas 20,00.
1. Preces krājumu transakciju vēsture satur tālāk norādīto.
    - Krājumu transakcija ar daudzumu 1, izmaksām 16,00, grāmatošanas datumu 15. janvāris un transakcijas datumu 15. janvāris.
    - Krājumu korekcija ar daudzumu 1, izmaksām 20,00, grāmatošanas datumu 1. janvāris un transakcijas datumu 15. janvāris.
1. Grāmatojiet korekciju.

Lapā **Krājumu darbības** ir redzams, ka izdevumos ir iekļauta summa 4,00, jo preces pašreizējās slīdošās vidējās izmaksas ir 16,00. Varat grāmatot ar atpakaļejošu datumu, taču izmaksu atšķirība tiek iekļauta izdevumos, tāpēc netiek ietekmētas slīdošās vidējās izmaksas.

## <a name="negative-inventory-balances"></a>Negatīvās krājumu bilances

Darījumi tiek apstrādāti dažādi atkarībā no tā, vai jaunais rīcībā esošais daudzums pēc darījuma ir negatīvs, nulle vai pozitīvs.

### <a name="new-balance-is-negative-or-zero"></a>Jauna bilance ir negatīva vai nulle

Ja jaunais rīcībā esošais daudzums ir negatīvs vai nulle, darījums tiek izmaksāts par pašreizējām vidējām izmaksām. Ja pastāv starpība starp pirkšanas cenu un pašreizējām vidējām izmaksām, tā tiek iegrāmatota **Cenas atšķirība slīdošajam vidējam**.

### <a name="new-balance-is-positive"></a>Jauna bilance ir pozitīva

Ja pēc darījuma jaunais rīcībā esošais daudzums ir pozitīvs, darījums tiek sadalīts divās daļās un izmaksāts atšķirīgi, kā tas ir apkopots šajā tabulā.

| Daļa | Apraksts |
|---|---|
| Daudzums no negatīva līdz nullei | Krājumi izmanto krājuma pašreizējās slīdošā vidējā izmaksas, nevis darījuma izmaksas šai saņemšanas daudzuma daļai, kas palielina rīcībā esošo bilanci no negatīva līdz nullei. Starpība starp transakcijas izmaksām un pašreizējām slīdošā vidējā izmaksām tiek iegrāmatota **Cenas atšķirība slīdošajam vidējam**. |
| Daudzums no nulles līdz pozitīvam | Krājumi izmanto transakcijas izmaksas šai saņemšanas daudzuma daļai, kas palielina rīcībā esošo bilanci no nulles līdz pozitīvam.                                                  |

## <a name="inventory-value-report"></a>Krājumu vērtības pārskats

Šajā slīdošā vidējā izmantošanas piemērā tiek drukāts krājumu vērtības pārskats, lai atvieglotu preces pašreizējās vidējās slīdošās vērtības aprēķinu. Krājumu vērtības pārskatā var hronoloģiskā secībā iekļaut transakcijas kopā ar izmaksām, lai atvieglotu preces slīdošo vidējo izmaksu aprēķinu. Pārskatā ir redzamas preces slīdošās vidējās izmaksas. Dialoglodziņā **Krājumu vērtības pārskati** datumu intervāls ļauj atlasīt vērtību **Darījuma laiks** vai **Grāmatošanas datums**, lai norādītu pārskata kārtošanas veidu. Parasti pārskats tiek drukāts, izmantojot opciju **Grāmatošanas datums**. Opcija **Darījuma laiks** atbilst faktiskajam datumam, kad tiek ziņots par transakciju un tiek atjauninātas preces slīdošās vidējās izmaksas. Varat drukāt krājumu vērtības pārskatu, izmantojot kārtošanas opciju **Darījuma laiks**, ja vēlaties skatīt slīdošo vidējo izmaksu aprēķinu laika gaitā. Tālāk esošajā tabulā ir redzamas tās prece transakcijas, kam tiek drukāts pārskats, izmantojot kārtošanas opciju **Darījuma laiks**.

| Darījuma laiks | Datums         | Darījuma veids           | Daudzums | Summa | Vidējās vienības izmaksas |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktobris    | Sākuma bilance          | 0        | 0,00   | 0,00              |
| 8. oktobris        | 28. septembris | Ieejas plūsma ar atpakaļejošu datumu          | 1        | 16,00  | 16,00             |
| 3. oktobris        | 3. oktobris    | Pirkšanas ieejas plūsma           | 2        | 20,00  | 12,00             |
| 5. oktobris        | 5. oktobris    | Pārdošanas pasūtījums                | -1       | -10,00 | 13,00             |
| 7. oktobris        | 7. oktobris    | Pirkšanas rēķins           |          | 2,00   | 14,00             |
| 8. oktobris        | 8. oktobris    | Vidējās pārvērtēšanas pārvietošana |          | 4.00   | 16.00             |
|                  | 31. oktobris   | Summa                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Virsgrāmatu nevar saskaņot ar krājumiem, izmantojot opciju **Transakciju laika kārtošana**. Pārskats ir jādrukā, izmantojot opciju **Grāmatošanas datums**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]