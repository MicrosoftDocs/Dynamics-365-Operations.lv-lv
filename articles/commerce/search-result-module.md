---
title: Meklēšanas rezultātu modulis
description: Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
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
ms.openlocfilehash: dc4a01e520379a74ca3b21c1d588531412e762be
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647516"
---
# <a name="search-results-module"></a>Meklēšanas rezultātu modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

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

Lai pievienotu meklēšanas rezultātu moduli kategorijas lapai, veiciet tālāk minētās darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** ievadiet nosaukumu **Meklēt rezultātus** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Atpakaļceļš** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits**.
1. Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēšanas rezultāti** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī **Meklēšanas rezultāti** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits** un pēc tam iestatiet visus citus nepieciešamos meklēšanas rezultātu modulim. Iestatot šos rekvizītus veidnē, pārliecinieties, ka visi konkrētas kategorijas lapas pielāgojumi automātiski ietvers šos iestatījumus.
1. Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu veidni.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni **Meklēšanas rezultāti**, ievadiet **Kategorijas lapa** opcijai **Lapas nosaukums** un pēc tam atlasiet **Labi**. Tā kā visas vērtības ir iestatītas veidnē, lapa ir gatava publicēšanai.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Meklēšanas rezultātu moduļa krājumu apzināšanas iespējošana

Klienti parasti sagaida, ka e-Commerce vietne visā pārlūkošanas laikā būs informēta par krājumiem, lai viņi varētu izlemt, ko darīt, ja produktam nav krājumu. Meklēšanas rezultātu modulis var tikt uzlabots, tādējādi tajā iekļauti krājumu dati un sniegta šāda pieredze:

- Rādiet krājumu pieejamības etiķeti kopā ar precēm.
- Paslēpt preces, kas atrodas ārpus noliktavas.
- Meklēšanas rezultātu saraksta beigās rādīt preces, kas ir ārpus krājuma.
    
Lai iespējotu šo pieredzi, ir jākonfigurē tālāk minētie Commerce Headquarters priekšnosacījumu iestatījumi.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Iespējot līdzekli Uzlabota e-Commerce produktu atklāšana ar informāciju par krājumiem

> [!NOTE]
> Līdzeklis **Uzlabota e-Commerce produktu atklāšana ar informāciju par krājumiem** ir pieejams Commerce versijā 10.0.20 laidienā.

Lai iespējotu līdzekli **Uzlabota e-Commerce produktu atklāšana ar informāciju par krājumiem** programmā Commerce Headquarters, veiciet šīs darbības.

1. Dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.
1. Mēklējiet līdzekli **Iespējot līdzekli Uzlabota e-Commerce produktu atklāšana ar informāciju par krājumiem**, un pēc tam iespējojiet to.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigurējiet darbu Preču īpašību aizpildīšana ar krājumu līmeni

Darbs **Preču īpašību aizpildīšana ar krājumu līmeni** izveido jaunu preces īpašību, lai tvertu krājumu pieejamību, un pēc tam iestata šo atribūtu uz pēdējo krājumu līmeņa vērtību katrai vispārējai precei. Tā kā krājuma pieejamība precei vai preču klāstam, kas tiek pārdots bez izmaiņām, ļoti ieteicams plānot darbu kā pakešuzdevumu.

Lai konfigurētu darbu **Preču īpašību aizpildīšana ar krājumu līmeni** programmā Commerce Headquarters, sekojiet šiem soļiem.

1. Dodieties uz **Retail un Commerce \> Retail un Commerce IT \> Preces un krājumi**.
1. Atlasiet **Preču īpašību aizpildīšana ar krājumu līmeni**.
1. Dialoglodziņā **Preču īpašību aizpildīšana ar krājumu līmeni** veiciet šādas darbības:

    1. Sadaļas **Parametri** laukā **Preces īpašības un tipa nosaukums** norādiet tās atvēlētās preces īpašības nosaukumu, kas tiks izveidota, lai tvertu krājumu pieejamību.
    1. Cilnes **Parametri** laukā **Krājumu pieejamība, pamatojoties uz** lauku atlasiet daudzumu, uz kura krājumu līmeņa aprēķinam jābūt balstītam (piemēram, **Fiziski pieejamais**).
    1. Sadaļā **Palaist fonā** konfigurējiet darbu, lai tas darbotos fonā, un pēc izvēles ieslēdziet **Pakešapstrādes** opciju. 

> [!NOTE]
> Lai veiktu konsekventu krājumu līmeņa aprēķinu PDP un produktu saraksta lapās jūsu e-commerce vietnē, noteikti atlasiet vienu un to pašu daudzuma opciju gan iestatījumam **Krājumu pieejamība, pamatojoties uz** Commerce Headquarters un iestatījumam **Krājumu līmenis, pamatojoties uz** Commerce vietņu veidotājā. Papildinformāciju par krājumu iestatījumiem vietņu veidotājā skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Konfigurēt jaunas preces atribūtu

Kad darbs **Preču īpašību aizpildīšana ar krājumu līmeni** ir aizpildīts, e-Commerce vietnē jākonfigurē jaunizveidotās preces atrubūts, kur vēlaties iespējot krājumu apzināšanu meklēšanas rezultātu modulim.

Lai konfigurētu jaunas preces atrubūtu Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības** un atlasiet e-Commerce vietni.
1. Atlasiet un atveriet saistīto atribūtu grupu, pievienojiet tai jaunizveidotās preces īpašības un pēc tam aizveriet lapu.
1. Atlasiet **Atribūtu metadatu iestatīšana**, atlasiet jaunizveidotās preces īpašību un pēc tam slēdziet atribūtu **Rādīt kanālā**, **Izgūstams**, **Var precizēt** un **Var iegūt vaicājumu** opcijas.

> [!NOTE]
> Precēm, kas tiek rādītas meklēšanas rezultātu modulī, krājumu līmenis tiek ievadīts preču šablona līmenī, nevis atsevišķā varianta līmenī. Ir tikai divas iespējamās vērtības: "pieejams" un "nav noliktavā". Faktiskais vērtību teksts tiek iegūts no definīcijas [krājumu līmeņa profils](inventory-buffers-levels.md). Šablona prece tiek uzskatīta par krājumu tikai tad, ja visi tās varianti ir krājumos. Varianta krājumu līmenis tiek noteikts, pamatojoties uz preces krājumu līmeņa profila definīciju. 

Kad visi iepriekšējie konfigurācijas soļi ir pabeigti, meklēšanas rezultātu lapu uzlabotāji parādīs uz krājumiem balstītu filtru, un meklēšanas rezultātu modulis izgūs krājumu datus aiz ēnas. Varat konfigurēt iestatījumu **Krājumu iestatījumi preču saraksta lapām** Commerce vietņu veidotājā, lai kontrolētu to, kā meklēšanas rezultātu modulis rāda preces, kas atrodas ārpus noliktavas. Papildinformāciju skatiet [Krājumu iestatījumu lietošana](inventory-settings.md).

## <a name="additional-resources"></a>Papildu resursi

[Noklusējuma kategorijas reklāmas mērķlapas un meklēšanas rezultātu lapas pārskats](category-search-page-overview.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Ātrā skata modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
