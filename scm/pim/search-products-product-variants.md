---
title: "Meklēt preces un preces variantus pasūtījuma izveides laikā"
description: "Izmantojiet lauku <strong>Krājuma kods </strong>, lai meklētu preces un preču variantus, manuāli izveidojot pārdošanas pasūtījuma vai pirkšanas pasūtījuma rindas.  Tas ļauj jums ātri atrast preces variantus, ja jums ir tikai konfigurācijas virkne, vai vienu no pieejamajām preces dimensijām."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b0f3c1a853f8f5e61dedaf588b6f9d2da3a53b5
ms.lasthandoff: 03/31/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Meklēt preces un preces variantus pasūtījuma izveides laikā

Izmantojiet lauku <strong>Krājuma kods </strong>, lai meklētu preces un preču variantus, manuāli izveidojot pārdošanas pasūtījuma vai pirkšanas pasūtījuma rindas.  Tas ļauj jums ātri atrast preces variantus, ja jums ir tikai konfigurācijas virkne, vai vienu no pieejamajām preces dimensijām.

Dažreiz, ņemot pārāk daudz kaut kas nav labākā situācijā atrasties, un īpaši tad, ja jūs pārdodat produktu, kas ir līdzīgs skaits un mēģināt atcerēties objektu numuros vai produktu meklēšanas nosaukumus, lai atrastu pareizo produktu likt uz pārdošanas pasūtījumu. Var izmantot **krājums** lauku pārdošanas pasūtījuma vai pirkšanas pasūtījuma rindu kā meklēšanas laukā. Jūs varat ievadīt jebkuru preces nosaukuma daļu, kodu vai dimensiju, un iegūt uzmeklēšanu, kas parāda visus vienumus, kas atbilst meklēšanas vārdam.

## <a name="how-search-works"></a>Kā darbojas meklēšana
Meklējot preces vai preces variantus, ir svarīgi saprast, kā meklēšanas līdzeklis atrod preces, kas atbilst jūsu ievadītajam tekstam. Galvenie meklēšanas noteikumi, nodrošinot meklēšanas rezultātus ir:

-   Meklēšanas rezultāti atgriezīs jebkuru atbilstošu ierakstu, neņemot vērā lauku, kurā ir ievadīts meklēšanas teksts.
-   Meklēšanas tekstam ir jāparādās atbilstošajā ierakstā pilnā garumā.
-   Atbilstība notiks pat tad, ja meklēšanas teksts atrodas atbilstošā ieraksta teksta virknes vidū. Tam nav obligāti jāparādās teksta virknes sākumā.
-   Meklēšanas teksts tiek uzskatīts kā vienota teksta virkne pat tad, ja tas satur baltstarpas.

### <a name="examples"></a>Piemēri

Šajos piemēros tiek izmantotas preces un preču varianti, lai parādītu kā meklēšana tiek veikta dažādās situācijās. **Priekšnoteikums:** zem **pārdošanas un mārketinga &gt;Setup &gt;meklēšanas &gt;meklēšanas parametrus**&gt;**meklēšanas tips**, atlasiet **pilna atbilstība** opciju.

| Preces veids     | Preces nosaukums    | Parādīt preces numuru | Krājums | Konfigurācija |
|------------------|-----------------|------------------------|-------------|---------------|
| Atšķirīga prece | SpeakerMidRange | D0001                  | D0001       | NA            |
| Preces variants  | Aktīvs skaļrunis  | D0010:::Melns:         | D0010       | 000005        |
| Preces variants  | Aktīvs skaļrunis  | D0010:::Balts:         | D0010       | Balta         |

Ievadot frāzi "skaļr" laukā **Krājuma kods**, jums tiks parādītas visas iepriekš minētās preces kā uzmeklēšanas rezultāts. Ievadot frāzi "melns" laukā **Krājuma kods**, kā rezultāts jums tiks parādīta otra prece, jo tai laukā parādīt preces numuru ir teksts "melns". Šie divi piemēri parāda, ka meklēšana notiek ne tikai lauka sākumā, atbilstība parādīsies pat tad, ja meklēšanas teksts atrodas atbilstošā ieraksta teksta virknes vidū.  

Ievadot '05', kā rezultātu iegūsiet tikai otro preces variantu, jo tam konfigurācijā ir '05'. Tas parāda, ka meklēšana notiek visos atļautajos laukos lapā **Meklēšanas kritēriji**.  

Ievadot 'skaļr 05', jums netiks parādīti nekādi rezultāti. Tāpēc, ka meklēšana meklē pilnu ievadīto tekstu. Nevar meklēt "skaļr", un pēc tam sašaurināt rezultātus līdz tiem, kas satur '05'.  

Meklēšanas rezultātu skaitu var ierobežot, izmantojot **rezultātu skaits** lauku **pārdošanas un mārketinga &gt;Setup &gt;meklēšanas &gt;meklēšanas parametrus** lapā. Iestatot šo lauku uz 0, tiks atgriezti visi meklēšanas rezultāti. Iestatot to, piemēram, uz 10, tiks atgriezti ne vairāk kā 10 meklēšanas rezultāti.

## <a name="configure-the-product-search"></a>Konfigurēt preču meklēšanu
Pirms varat lietot preču un preču variantu meklēšanas funkciju, sekojiet šiem soļiem, lai konfigurētu preču meklēšanu. [![3 soļi, lai konfigurētu produktu meklēšana\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>1. solis: Iekļaut visus attiecīgās preces un preces variantu identifikatorus un dimensijas meklēšanas kritērijos

Preces un preces variantu identifikatoru un dimensiju piemēri, kurus jūs varat meklēt ir **Preces nosaukums, Krājuma kods**, **Parādīt preces numuru, Konfigurācija, Krāsa, Izmērs, Stils, Meklēšanas nosaukums u.c.**.  

Dodieties uz **pārdošanas un mārketinga &gt;Setup &gt;meklēšanas &gt;meklēšanas kritērijus** lapā. Lapa **Meklēšanas kritēriji** ļauj definēt debitoru, potenciālo klientu un preču meklēšanas kritērijus. Pārliecinieties, ka filtrējat lapu, izmantojot preču meklēšanas kritērijus. To var paveikt, lapas izvēlnē pārslēdzoties uz **Prece**.  

Lai pievienotu displeja produkta numuru meklēšanas kritēriji, noklikšķiniet uz **New** lapas izvēlnē. Tas pievienos jaunu ierakstu **meklēšanas kritērijus** režģi. Atveriet kolonnas uzmeklēšanu **Lauka nosaukums**, un atlasiet **DisplayProductNumber**. Lai pievienotu meklēšanas kritēriju produkta konfigurēšanu, izveidot jaunu ierakstu * * meklēšanas kritērijus * * režģis un izvēlējās **configId**, **lauka nosaukums** kolonnu. Tādā pašā veidā, izveidojiet ierakstu ar **Lauka nosaukumu** **InventColorId** krāsu dimensijai, **InventSizeId** izmēra dimensijai un **InventStyleId** stila dimensijai.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>2. solis: aizpildiet datu bāzes tabulu, kas tiek izmantota preču meklēšanā

Lapā **Meklēšanas kritēriji**, noklikšķiniet uz pogas **Atjaunināt meklēšanas datus**. Dialoglodziņā **Atjaunināt meklēšanas datus** pārliecinieties, ka **Avots** ir iestatīts uz **Prece**, un pēc tam noklikšķiniet uz **Labi**. Sistēma būs apvienot vienā tabulā visi atlasītās meklēšanas kritēriji, kas precizēti 1. solī. Ja jums ir daudz produktu un produktu variantiem, šī darbība var būt diezgan garš un saņemsit brīdinājumu. Ieteicams ieplānot meklēšanas tabulas aizpildīšanu pakešapstrādes serverī laikā, kad serveris nav pārāk aizņemts.  

Kamēr tabula nav aizpildīta, preču meklēšana nesniedz pareizus rezultātus. Ja jūs nesaņemat meklēšanas rezultātus, pārliecinieties, vai šī tabula ir aizpildīta.  

Tabulai jābūt aizpildītai, tikai kad tiek modificēti meklēšanas kritēriji. No jauna izlaistās preces un varianti tiek automātiski pievienoti tabulai. Izdzēstās preces un varianti tiek automātiski noņemti no tabulas.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>3. solis: Iespējot uzmeklēšanu preces meklēšanai pārdošanas un pirkšanas pasūtījuma rindās

Šo funkcionalitāti var iespējot, dodoties uz **pārdošanas un mārketinga &gt;Setup &gt;meklēšanas &gt;meklēšanas parametrus** un iestatījumu **Iespējot pārlūkošanas meklēšanas** uz **Jā** par **vispārējā** tab.  

Pārdošanas pasūtījuma rindas ierakstam noklusējums ir atvērt lapu **Preču meklēšana**, sākot ierakstīt laukā **Krājuma kods**, un pēc tam nospiediet taustiņu **Tab**. Lapa **Preču meklēšana** maina kontekstu pasūtījuma rindas izveides laikā, un var būt uzskatāma par nevajadzīgu iejaukšanos. Ja vēlaties iegūt meklēšanas rezultātus uzmeklēšanā, un nezaudēt kontekstu pasūtījuma rindas izveides laikā, jūs varat izmantot uzmeklēšanas meklēšanu. Ja meklējat preci vai preces variantu, bet neko neatlasāt uzmeklēšanā, un nospiežat taustiņu **Tab**, tiks parādīta lapa **Preču meklēšana**.


