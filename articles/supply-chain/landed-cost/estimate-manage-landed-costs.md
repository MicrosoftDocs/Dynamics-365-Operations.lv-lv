---
title: Novērtēt un pārvaldīt kopējās izmaksas
description: Sistēma izmanto automātisko izmaksu iestatījumu, lai noteiktu savu kopējo izmaksu novērtējumu. Šajā tēmā skaidrots, kā definēt dažādus scenārijus, lai nodrošinātu precīzāku novērtējumu.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: a30c1efd2fa37a5fb192156ab6edf1d57be8cad36c781f236385fc6884bda097
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736699"
---
# <a name="estimate-and-manage-landed-costs"></a>Novērtēt un pārvaldīt kopējās izmaksas

[!include [banner](../../includes/banner.md)]

Sistēma izmanto [automātisko izmaksu iestatījumu](auto-cost-setup.md), lai noteiktu savu kopējo izmaksu novērtējumu. Papildus šajā tēmā skaidrots, kā definēt dažādus scenārijus, lai nodrošinātu precīzāku novērtējumu. Šie scenāriji tiek saglabāti. Tāpēc varat tos pārskatīt vēlāk un salīdzināt ar pārskata faktiskajām izmaksām. Krājuma cenu var arī atjaunināt.

## <a name="set-up-cost-estimates"></a>Izmaksu novērtējumu iestatīšana

### <a name="set-up-cost-templates"></a>Iestatīt izmaksu veidnes

Izmaksu veidnes izveido noklusējuma iestatījumus, kurus lietotāji, kuriem būs iegūts novērtējums, nav obligāti jāzina. Izmaksu veidnes var palīdzēt samazināt aprēķinu procesa sarežģītību, samazinot atlases, kas jāveic lietotājiem, lai iegūtu precīzu novērtējumu. Ja izmantojat standarta izmaksu modeli, varat izmantot izmaksu veidnes, kamēr iestatāt preču izmaksas.

Lai iestatītu izmaksu veidnes, dodieties uz sadaļu **Kopējās izmaksas \> Izmaksu aprēķināšanas iestatījumi \> Izmaksu veidnes**. Izmaksu **Izmaksu veidnes** saraksta rūtī kreisajā pusē ir parādītas visas pašreizējās izmaksu veidnes. Jūs varat izmantot pogas Darbību rūtī, lai izveidotu, dzēstu un rediģētu veidnes.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai veidnei.

| Lauks | Apraksts |
|---|---|
| Izmaksu veidne | Ievadiet unikālu izmaksu veidnes nosaukumu. Šis nosaukums parasti apraksta veidnes faktoru vai izmaksu reizinātāju. |
| Apraksts | Ievadiet izmaksu veidnes aprakstu. |
| Nosūtīšanas uzņēmums | Atlasiet nosūtīšanas uzņēmumu, kas jālieto, kad tiek izmantota veidne. |
| Piegādes veids | Atlasiet piegādes veidu, piemēram, gaiss vai gaiss, kas jāizmanto veidnes lietošanas laikā. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Nosūtīšanas konteinera veids | Atlasiet nosūtīšanas konteinera veidu, kas jālieto, kad tiek izmantota veidne. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Muitas aģents | Muitas brokeris (kreditors), kas jālieto, kad tiek izmantota veidne. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Koeficients | Ievadiet reizinātāju (procentus), kas automātiski jāpiemēro izmaksu novērtējumam, izmantojot veidni. Piemēram, lai novērtētu izmaksu budžetam pievienotu 10 procentus, ievadiet *1,10*. |

### <a name="create-a-cost-estimate"></a>Izmaksu novērtējuma izveide

Lietojiet dialoglodziņu **Izmaksu novērtējums**, lai ģenerētu jaunu izmaksu novērtējumu, kura pamatā ir atlasītā izmaksu veidne, atlasītā krājumu kopa un cita detalizēta informācija par krājumu. Šie iestatījumi tad tiek izmantoti, lai noteiktu novērtētās preču kopējās izmaksas. Šie izmaksu novērtējumi galvenokārt tiek izmantoti darbam ar standarta izmaksu krājumiem. Pievienojot novērtētās zemes izmaksas krājumu standarta izmaksām, ir jāņem vērā mazākās novirzes darbības, kad preces tiek pievienotas reisam, jo standarta izmaksas atspoguļos šo zemes izmaksu prognozes.

Lai atvērtu dialoglodziņu **Izmaksu novērtējums**, dodieties uz sadaļu **Kopējās izmaksas \> Periodiskie uzdevumi \> Izmaksu novērtējums**. Pēc tam katrā kopsavilkuma cilnē iestatiet laukus, kā aprakstīts sekojošās apakšsadaļās. Atlasiet **Labi**, lai izveidotu novērtējumu. **Izmaksu novērtējuma** lapa (**Kopējās izmaksas \> Uzziņas \> Izmaksu novērtējumi**), pēc tam tiek parādīts jūsu jaunais novērtējums, kā aprakstīts tālāk šajā tēmā.

### <a name="settings-on-the-parameters-tab"></a>Iestatījumi cilnē Parametri

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami cilnes **Parametri** dialoglodziņā **Izmaksu novērtējums**.


| Lauks | Apraksts |
|---|---|
| Izmaksu veidne | Atlasiet izmaksu veidni. Ar atlasīto veidni saistītie iestatījumi tiks izmantoti, lai noteiktu lietotās automātiskās izmaksas. |
| Novērtēt datumu | Pēc noklusējuma šis lauks ir iestatīts uz šīs dienas datumu, bet vērtību var mainīt. Norādītais datums tiks izmantots, lai atlasītu atbilstošās pārdošanas cenas, pirkšanas cenas, automātiskās izmaksas un maiņas kursu, ja izmantots nosūtīšanas kurss. |
| Mērījums | Izmaksas var būt atkarīgas no mērījuma. Piemēram, ja tiek izmantota gaisa krava, tiek piemērota apjoma cenu noteikšana. Ja izmaksas ir atkarīgas no mērījuma, ievadiet šī mērījuma vērtību. Pretējā gadījumā ieteicams šo lauku iestatīt uz *1*, ja vien neesat pārliecināts, ka, izmantojot mērījumu, nekas netiek dalīts. Ievadiet decimāldaļskaitli. Vienība ir tā, kas ir definēta piemērojamajā automātisko izmaksu ierakstā. |
| Maršruta veidne | Atlasiet [ceļojuma veidni](multi-leg-journey-setup.md). Šis lauks tiek izmantots, lai noteiktu pareizās automātiskās izmaksas, kas jālieto. |
| No ostas | Osta, no kuras tiks nosūtīti krājumi. Šis lauks ir iestatīts, pamatojoties uz atlasīto ceļojuma veidni. |
| Uz ostu | Osta, no kuras tiks nosūtīti krājumi. Šis lauks ir iestatīts, pamatojoties uz atlasīto ceļojuma veidni. |
| Valūta | Atlasiet valūtu, kurā tiks pirkti krājumi. |
| Konteineri | Ja parasti tiek izmantoti vairāki konteineri, norādiet konteineru skaitu. Tad sistēma izmantos vairāku konteineru izmaksas, kad tā novērtē izmaksas. |
| Folios | Ja parasti tiek lietoti vairāki folio, norādiet daudzumu. (Parasti daudzums ir *1*.) |
| Vieta | Norādiet vietu, kur tiks piegādātas preces. |

### <a name="settings-on-the-items-tab"></a>Iestatījumi cilnē Krājumi

Cilnē **Krājumi** novērtējumam var pievienot tik daudz krājumu, cik nepieciešams. Izmantojiet rīkjoslu, lai pievienotu krājumus režģim vai noņemtu krājumus. Lai atvērtu dialoglodziņu, kurā režģim vai kolonnu noņemšanai varat pievienot dimensiju kolonnas, rīkjoslā atlasiet **Krājumi \> Rādīšanas dimensijas**.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram krājumam.

| Lauks | Apraksts |
|---|---|
| Krājums | Atlasiet krājumu, lai noteiktu tā cenu. (Ja sistēmā vēl nav krājuma, izveidojiet fikttīvu krājumu, pēc izvēles pievienojiet to reisa krājumu izmaksu grupai un pēc tam atstājiet cenu tukšu vai izveidojiet vai mainiet cenu.) |
| Kreditora konts | Atlasiet kreditoru, kuru izmantot šī krājuma novērtējumam. Ja krājumam tiek piešķirts noklusētais kreditors, šis lauks tiek iestatīts automātiski. |
| Daudzums | Atlasiet daudzumu, kuru vēlaties iegādāties. |
| Izmaksu cena | Sistēma izmanto cenu noteikšanas noteikumus, lai atrastu sākotnējo cenu, bet, ja nepieciešams, šo cenu var ignorēt. |
| Pārdošanas cena | Ievadiet preču paredzamo pārdošanas cenu. |
| Mērījums | Ievadiet decimālskaitļa vērtību preču mērījumam. Vienība ir tā, kas iestatīta piemērojamai izlaistai precei. |
| Atjaunināt krājuma svaru/apjomu | Atzīmējiet šo izvēles rūtiņu, lai atjauninātu izlaistās preces svara vai tilpuma mērījumus tā, lai tas atbilstu **Mērījuma** vērtībai, kas tiek ievadīta šai rindai. |
| (Citas dimensijas) | Atkarībā no dimensijām, ko esat atlasījis, lai parādītu, varat redzēt papildu kolonnas informācijai par katru krājumu. |

Lai skatītu vai pielāgotu krājuma apjoma un/vai svara datus, atlasiet krājumu režģī un pēc tam izmantojiet laukus lapas apakšā.

## <a name="manage-estimated-costs"></a>Pārvaldīt novērtētās izmaksas

Lai skatītu un rediģētu izveidotos izmaksu novērtējumus, dodieties uz sadaļu **Kopējās izmaksas \> Izmaksas \> Izmaksu novērtējumi**. Izmaksu **Izmaksu novērtējumi** saraksta rūtī kreisajā pusē ir parādītas visas pašreizējās izmaksu veidnes. Varat izmantot pogas Darbību rūtī, lai strādātu ar atlasīto novērtējumu. Ņemiet vērā, ka nevarat izveidot jaunu izmaksu novērtējumu no **Izmaksu novērtējuma** lapas. Tā vietā izmantojiet dialoglodziņu **Izmaksu novērtējums** (**Kopējās izmaksas \> Periodiskie uzdevumi \> Izmaksu novērtējums**), kā aprakstīts iepriekš šajā tēmā.

**Izmaksu novērtējuma** lapa parāda, kā katra novērtētā izmaksas tika atvasināta. Tas parāda arī novērtētās kopējās izmaksas katram krājumam. Izmaksu novērtējumu var modificēt, izmainot izmaksu cenu un/vai valūtu, kas saistīta ar dažādām precēm. Ir arī iespējams modificēt saistītās reisa izmaksas gan reisa līmenī, gan konteinera līmenī. Ja lietojat šo lapu, lai modificētu izmaksas, izmaksu novērtējumā jums tiks piedāvāts pārrēķināt krājumu novērtētās izmaksas. Kad esat gatavs, varat izmantot novērtējumus, lai atjauninātu izmaksu veidnē esošo krājumu izmaksu cenu.

### <a name="information-on-the-header"></a>Galvenes informācija

Lapas **Izmaksu novērtējums** augšpusē ir parādīti iestatījumi, kas tika lietoti, lai ģenerētu atlasīto izmaksu novērtējumu, kā aprakstīts iepriekšējā sadaļā. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Kopsavilkuma cilnes Rindas iestatījumi un pogas

Kopsavilkuma cilnē **Rindas** tiek uzskaitīti visi krājumi, kas iekļauti pašreizējā novērtējumā. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai rindai.

| Lauks | Apraksts |
|---|---|
| Kreditora konts | Ar krājumu saistītais kreditora konts. |
| Krājums | Krājuma numurs. |
| Daudzums | Krājumu skaits, kas tiek izmantots izmaksu noteikšanai. |
| Izmaksu cena | Izmaksu cena saskaņā ar tirdzniecības līgumu. Šī vērtība tiek izteikta vietējā valūtā. |
| Mērījums | Atsevišķi mērījumi. Vienība ir tā, kas iestatīta piemērojamai izlaistai precei. |
| Novērtētās piegādes izmaksas | Novērtētās kopējā daudzuma kopējās izmaksas. |
| Uz vienu vienību | Novērtētās kopējās izmaksas, dalot ar daudzumu. |
| (Citas dimensijas) | Atkarībā no dimensijām, ko esat atlasījis, lai parādītu, varat redzēt papildu kolonnas informācijai par katru krājumu. |

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Rindu** kopsavilkuma cilnē.

| Poga | Apraksts |
|---|---|
| Pievienot | Pievienojiet krājumus izmaksu novērtējumam. Pēc krājumu pievienošanas darbības rūtī ir jāatlasa **Pārrēķināt**. |
| Aizvākt | Noņemt krājumus no izmaksu novērtējuma. Pēc krājumu noņemšanas darbības rūtī ir jāatlasa **Pārrēķināt**. |
| Reisa izmaksas | Atvērt lapu, kur varat apskatīt un rediģēt dažādus krājuma reisu izmaksu tipus. |
| Krājums \> Dimensiju rādīšana | Atveriet dialoglodziņu, kur režģim var pievienot dimensiju kolonnas vai noņemt kolonnas. |

### <a name="settings-on-the-general-fasttab"></a>Kopsavilkuma cilnes Vispārīgi iestatījumi

Kopsavilkuma cilnē **Vispārīgi** tiek rādīta informācija par preci, kas pašlaik ir atlasīta kopsavilkuma cilnē **Rindas**. Liela daļa šīs informācijas tiek atkārtota kopsavilkuma cilnē **Rindas** un to var rediģēt jebkurā vietā. Tomēr šeit ir pieejama arī papildinformācija. Papildu lauku vērtības ir balstītas uz piemērojamās izlaistās preces iestatījumu.

### <a name="settings-on-the-dimension-fasttab"></a>Kopsavilkuma cilnes Dimensijas iestatījumi

Kopsavilkuma cilnē **Dimensijas** tiek rādītas kopsavilkuma cilnē **Rindas** atlasītā krājuma visu pieejamo krājumu dimensiju vērtības neatkarīgi no dimensijām, kuras esat izvēlējies tajā rādīt. Visas šeit redzamās vērtības ir no piemērojamās izmaksu novērtēšanas veidnes. Izmaksu novērtēšanas veidnē tās nav obligātas.

### <a name="buttons-on-the-action-pane"></a>Pogas darbību rūtī

Lai strādātu ar atlasīto izmaksu budžetu, varat izmantot pogas lapas **Izmaksu novērtējums** darbību rūtī. Tālāk esošajā tabulā ir aprakstītas pieejamās opcijas.

| Darbība | Apraksts |
|---|---|
| Izmaksu pieprasījums | Skatiet visas reisa izmaksas. Izmaksas var skatīt atsevišķa krājuma līmenī pēc vajadzības. |
| Atjaunināt standarta izmaksas | <p>Atjauniniet standarta izmaksas, izmantojot noklusējuma izmaksu aprēķināšanas versiju, kas ir noteikta lapā **Kopējo izmaksu parametri**. Šo versiju var ignorēt.</p><p>**Piezīme:** Ja krājumam ir vairākas krājuma dimensijas (piemēram, dažādi izmēri, krāsas un konfigurācijas), taču šīs dimensijas nav atlasītas novērtējumam, sistēma katrai kombinācijai izveidos nenokārtoto cenu.</p><p>**Svarīgi:** Cenu sadalījums ir izveidots un tiek izmantots, lai noteiktu standarta izmaksu noviržu pēc kopējās izmaksas.</p> |
| Reisa izmaksas | Skatiet un rediģējiet reisa izmaksas visām kravā izmantotajām precēm. |
| Pārrēķināt | Atjauniniet novērtētās kopējās izmaksas pēc reisu izmaksu atjaunināšanas, pievienošanas vai noņemšanas. |
| Bloķēt | Bloķējiet izmaksu novērtējuma ierakstu, lai vairs nevar veikt izmaiņas. |

## <a name="item-cost-price-update"></a>Krājuma izmaksu cenas atjaunināšana

**Krājumu izmaksu cenas atjaunināšanas** periodiskais uzdevums atjaunina visus izmaksu novērtējumus, kas atbilst filtriem, kurus iestatījāt, palaižot uzdevumu. Ietekme ir līdzīga tam, kā atsevišķam novērtējumam atlasot **Atjaunināt standarta izmaksas** darbību rūtī. Tomēr šajā gadījumā atjauninājums attiecas uz visiem atbilstošajiem novērtējumiem.

Lai palaistu periodisko uzdevumu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Kopējās izmaksas \> Periodiskie uzdevumi \> Krājumu izmaksu cenas atjaunināšana**.
1. Dialoglodziņā **Atjaunināt izmaksu cenu no novērtējuma** iestatiet sekojošos laukus, kā nepieciešams, lai ierobežotu atjaunināšanas tvērumu:

    - **Versija** – atjauniniet tikai novērtējumus, kas izmanto noteikto izmaksu versiju.
    - **Vieta** – atjauniniet tikai novērtējumus, kas izmanto noteikto izmaksu vietu.
    - **Izmaksu veidne** – atjauniniet tikai novērtējumus, kas izmanto noteikto veidni.
    - **Uz ostu** – atjauniniet tikai novērtējumus, kas izmanto noteikto "uz" ostu.
    - **Novērtējuma datums** – atjauniniet tikai tos novērtējumus, kuriem ir noteikts datums.

1. Iestatiet opcijas uz **Ierakstiem, kas jāiekļauj** un kopsavilkuma cilni uz **Palaist fonā**, kā ierasts, periodiskiem uzdevumiem.
1. Atlasiet **Labi**, lai palaistu uzdevumu.

> [!NOTE]
> Šis periodiskais uzdevums tiks izpildīts tikai sekmīgi, ja būs pieejama šāda informācija:
>
> - Katrai relevantai precei jābūt definētam **Bruto dziļumam**, **Bruto platumam** un **Bruto augstumam**.
> - Katram atbilstošam kreditoram ir jābūt definētam **No ostas**.
