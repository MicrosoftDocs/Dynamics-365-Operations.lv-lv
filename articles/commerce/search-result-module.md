---
title: Meklēšanas rezultātu modulis
description: Šajā rakstā ir apskatīti meklēšanas rezultātu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a087c213d4a7094f75da8c20e4ccc14fc52444ce
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027095"
---
# <a name="search-results-module"></a>Meklēšanas rezultātu modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti meklēšanas rezultātu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Meklēšanas rezultātu modulis atgriež preču meklēšanas rezultātus un piemērojamo preču rafinētāju sarakstu. Meklēšanas rezultātu moduļus Dynamics 365 Commerce vietnēs var izmantot, lai atveidotu lapas šādiem scenārijiem:

- Meklēšanas rezultāti, ko uzsāka lietotāja meklēšana
- Meklēšanas rezultāti, kas norāda noteiktu preču kopu, piemēram, "Pirkt līdzīgas preces"
- Preču saraksti, kas pieder noteiktai kategorijai

Papildinformāciju par kategoriju un meklēšanas rezultātu lapām skatiet [Noklusējuma kategorijas ielādes lapa un meklēšanas rezultātu lapas apskats](category-search-page-overview.md).

Sekojošajā attēlā redzams kategorijas meklēšanas rezultātu lapas piemērs Fabrikam vietnē.

![Meklēšanas rezultātu lapas piemērs Fabrikam vietnē.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Meklēšanas rezultātu moduļa rekvizīti

Tabulā zemāk uzskaitīti meklēšanas rezultātu moduļu rekvizīti un to vērtības un apraksti.

| Rekvizīts | Vērtības | Apraksts |
|----------|--------|-------------|
| Vienumi lapā | Vesels skaitlis | Krājumu skaits, kas jāparāda katrā lapā. |
| Atļaut balstīties uz PDP | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, kad lietotājs atlasa preci meklēšanas rezultātu lapā, atpakaļceļa navigācija uz preces informācijas lapu, kas ir atvērta, parādīs saiti "Atpakaļ uz rezultātiem". |
| Izvērst precizētājus | **Viss**, **1**, **2**, **3**, or **4** | Galveno rafinētāju skaits, kas jāizvērš, kad lapa ir ielādēta. Piemēram, ja šis rekvizīts ir iestatīts uz **3**, tiks izvērsti pirmie trīs rafinētāji lapā. |
| Paslēpt kategoriju hierarhijas attēlojumu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, lapā parādītā kategoriju hierarhija tiks paslēpta. Šis rekvizīts būtu jāiestata uz **Patiess**, ja izmantojat [atpakaļceļa moduli](add-breadcrumb.md), lai rādītu kategoriju hierarhiju.|
| Meklēšanas rezultātos iekļaut produkta atribūtus | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, meklēšanas rezultātos precēm tiks atgriezti atribūti. Lai arī šos atribūtus var parādīt Commerce vietnē, nepieciešams paplašinājums.|
| Rādīt piederības cenas | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, preču piederības cenas tiks rādītas meklēšanas rezultātos, kad lietotājs, kurš ir pierakstījies, pārlūko lapu. |
| Atjaunināt precizētāju paneli | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts uz **Patiess**, precizētāju panelis tiks atjaunināts, kad tiks atlasīti precizētāji. Šajā režīmā daži daudzkārtējas atlases precizētāji, atjauninot precizētāju paneli, darbosies kā vienas atlases precizētāji. |

> [!IMPORTANT]
> Commerce versijas 10.0.16 laidienā un jaunākos laidienos konfigurāciju **Rādīt piederības cenas** var izmantot, lai lapā parādītu piederības cenas lapā.
>
> Commerce versijas 10.0.20 laidienā un jaunākās versijās konfigurācija **Atjaunināt precizētāju paneli** var izmantot, lai atjauninātu precizētāju paneli precizētāju atlases laikā.

## <a name="supported-modules"></a>Atbalstītie moduļi

Meklēšanas rezultātu modulis atbalsta [ātro skatu moduli](quick-view-module.md), kas ļauj lietotājiem skatīt preces informāciju un pievienot vienumus grozam no meklēšanas rezultātu lapas.

## <a name="add-a-search-results-module-to-a-category-page"></a>Pievienot meklēšanas rezultātu moduli kategorijas lapai

Lai vietas veidotājā kategorijas lapai pievienotu meklēšanas rezultātu moduli, veiciet šos soļus.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** ievadiet nosaukumu **Meklēt rezultātus** un pēc tam atlasiet **Labi**.
1. Pamatteksta **slotā** atlasiet daudzpunkti (...) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet noklusējuma lapas **moduli** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **moduļa** galvenajā **slotā** atlasiet daudzpunkti (...) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (...) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Atpakaļcēlums **un** pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Atpakaļceļš** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits**.
1. Konteinera slotā **atlasiet** daudzpunkti (...) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet meklēšanas rezultātu **moduli** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Meklēšanas rezultāti** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits** un pēc tam iestatiet visus citus nepieciešamos meklēšanas rezultātu modulim. Iestatot šos rekvizītus veidnē, pārliecinieties, ka visi konkrētas kategorijas lapas pielāgojumi automātiski ietvers šos iestatījumus.
1. Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu veidni.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņa Izveidot **jaunu lapu sadaļā** Lapas nosaukums ievadiet **Kategorijas** lapu **un pēc** tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties veidni atlasiet** izveidoto **meklēšanas** rezultātu veidni un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** lapas izkārtojumu (piemēram, Elastīgs **izkārtojums**) un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jums ir jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Meklēšanas rezultātu moduļa krājumu apzināšanas iespējošana

Klienti galvenokārt plāno, ka e-komercijas vietne būs krājumos informēti pārlūkošanas pieredzes laikā, lai varētu izlemt, ko darīt, ja precei nav krājumu. Meklēšanas rezultātu moduli var konfigurēt, lai iekļautu krājumu datus un nodrošinātu šādu pieredzi:

- Rādiet krājumu pieejamības etiķeti kopā ar preci.
- Paslēpt preču sarakstā preces, kas atrodas ārpus noliktavas.
- Rādiet rezerves preces preču saraksta beigās.
- Filtrēt preces meklēšanas rezultātos pēc krājumu līmeņa.

Lai iespējotu šo pieredzi, vispirms aktivizējiet uzlaboto e-komercijas **preču noteikšanu,** lai tas būtu krājumos izprotams līdzekļu **pārvaldības darbvietā**.

> [!NOTE]
> Uzlabotā **e-Commerce preču noteikšana,** kas būs krājumu informācijas līdzeklis, ir pieejama Commerce versijā 10.0.20 vai jaunākā versijā.

Krājumu informācijas preču meklēšanā tiek izmantotas preču īpašības, lai iegūtu krājumu pieejamības informāciju. Kā šīs funkcionalitātes priekšnosacījums ir jāizveido atvēlētās preču īpašības, tiem jāievada krājumu dati un tās ir jāpievieno tiešsaistes kanālam. 

Lai izveidotu atvēlētas preces īpašības, kas atbalstītu krājumu zināto meklēšanas rezultātu moduli, sekojiet šiem soļiem.

1. Galvenajā birojā dodieties uz sadaļu **Mazumtirdzniecība un commerce \> Retail un Commerce IT \> preces un krājumi**.
1. Atlasiet un atveriet **aizpildīt preču īpašības ar krājuma līmeni**.
1. Dialoglodziņā ievadiet šādu informāciju:

    1. Laukā **Preces īpašības un tipa nosaukums** norādiet tās atvēlētās preces īpašības nosaukumu, kas tiks izveidota, lai iegūtu krājumu datus.
    1. Laukā **Krājumu pieejamība, pamatojoties** uz lauku, atlasiet daudzuma tipu, uz kura krājumu līmeņa aprēķinam jābūt balstītam (piemēram, Pieejams **fiziski**). 

1. Fonā palaidiet darbu. Sakarā ar to, ka preču krājumu papildu izmaiņas notiekchannel vidē, mēs stingri iesakām jums plānot šo darbu kā pakešuzdevumu.

> [!NOTE]
> Lai veiktu konsekventu krājumu līmeņa aprēķinu starp lapām un moduļiem jūsu e-komercijas vietnē, noteikti atlasiet vienu un to **pašu** daudzuma tipu gan krājumu pieejamībai, gan iestatīšanai commerce **headquarters**, gan krājumu līmenī, pamatojoties uz iestatījumiem Commerce Site Builder. Papildinformāciju par krājumu iestatījumiem vietņu veidotājā skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

Lai konfigurētu preces īpašības tiešsaistes kanālam, sekojiet šiem soļiem. 

1. Galvenajā birojā dodieties uz sadaļu **Mazumtirdzniecības un Commerce \>\> kanāla iestatīšanas kanāla kategorijas un preces īpašības**.
1. Atlasiet tiešsaistes kanālu, lai iespējotu krājumu informācijas meklēšanas rezultātu moduli.
1. Atlasiet un atveriet saistīto atribūtu grupu un pēc tam pievienojiet tai jaunizveidotās preces īpašības.
1. Commerce versijām pirms 10.0.27 laidiena atlasiet **Iestatīt atribūtu metadatus**,**atlasiet** jaunizveidotās preces īpašības un pēc tam slēdziet kanāla atribūtu Rādīt, **Izgūšanu**, **Var** precizēt un **opcijas** Var būt vaicājumā.
1. Dodieties uz **grafiku \> Mazumtirdzniecība un Commerce Retail un Commerce IT \> sadale** un palaidiet **1150 (kataloga)** darbu. Ja plānojat **aizpildīt** preču īpašības ar krājumu līmeņa darbu kā pakešuzdevumu, ieteicams arī ieplānot 1150 darbu kā pakešuzdevumu, kas darbojas ar vienādu frekvenci.

> [!NOTE]
> Precēm, kas tiek rādītas meklēšanas rezultātu modulī, krājumu līmenis tiek rādīts preču šablona līmenī, nevis atsevišķā varianta līmenī. Ir tikai divas iespējamās vērtības: "pieejams" un "nav noliktavā". Faktiskā vērtības iezīme tiek izgūta no krājumu līmeņa [profila](inventory-buffers-levels.md) definīcijas. Šablona prece tiek uzskatīta par krājumu tikai tad, ja visi tās varianti ir krājumos.

Kad visi iepriekšējie konfigurācijas soļi ir pabeigti, meklēšanas rezultātu lapu uzlabotāji parādīs uz krājumiem balstītu filtru, un meklēšanas rezultātu modulis izgūs krājumu datus aiz ēnas. Varat konfigurēt iestatījumu **Krājumu iestatījumi preču saraksta lapām** Commerce vietņu veidotājā, lai kontrolētu to, kā meklēšanas rezultātu modulis rāda preces, kas atrodas ārpus noliktavas. Papildinformāciju skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

## <a name="additional-resources"></a>Papildu resursi

[Noklusējuma kategorijas reklāmas mērķlapas un meklēšanas rezultātu lapas pārskats](category-search-page-overview.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Ātrā skata modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
