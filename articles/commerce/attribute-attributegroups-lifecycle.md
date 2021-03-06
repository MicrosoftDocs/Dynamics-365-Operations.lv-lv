---
title: Atribūtu un atribūtu grupu pārvaldība
description: Šajā tēmā aprakstīts, kā izmantot atribūtus, lai sniegtu veidu, kā aprakstīt preci un tās īpašības, izmantojot lietotāja definētos laukus.
author: ashishmsft
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: a49a0d05a55e72b5dae17933d38d03287a01d5ee
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936808"
---
# <a name="manage-attributes-and-attribute-groups"></a>Atribūtu un atribūtu grupu pārvaldība

[!include [banner](includes/banner.md)]

*Atribūti* nodrošina veidu, kā tālāk aprakstīt preci un tās raksturīgās iezīmes, izmantojot lietotāja definētos laukus (piemēram, **Atmiņas lielums**, **Cietā diska apjoms**, **Ir saderīgs ar Energy Star** un tā tālāk). Atribūtus var saistīt ar dažādām Commerce vienībām, piemēram, preču kategorijām un kanāliem, tiem var iestatīt noklusētās vērtības. Ja preces ir saistītas ar preču kategorijām vai kanāliem, tās pārmanto atribūtus un noklusējuma vērtības. Noklusējuma vērtības var būt ignorētas individuālas preces līmenī, kanāla līmenī vai katalogā.


Piemēram, parastam televizoram var būt tālāk minētie atribūti.

| Kategorija   | Atribūts                | Pieļaujamās vērtības          | Noklusētā vērtība |
|------------|--------------------------|-----------------------------|---------------|
| TV un Video | Zīmols                    | Jebkura derīga zīmola vērtība       | Neviens          |
| TV         | Ekrāna izmērs              | 20–80 collas                | Neviens          |
|            | Vertikālā izšķirtspēja      | 480i, 720p, 1080i, vai 1080p | 1080p         |
|            | Ekrāna atsvaidzes intensitāte      | 60 Hz, 120 Hz, vai 240 Hz       | 60 Hz          |
|            | HDMI ievades              | 0–10                        | 3             |
|            | DVI ievades               | 0–10                        | 1             |
|            | Kompozītie ievadi         | 0–10                        | 2             |
|            | Komponentās ievades         | 0–10                        | 1             |
| LCD        | 3D gatavs                 | Jā vai Nē                   | Jā           |
|            | 3D iespējots               | Jā vai Nē                   | Nav            |
| Plazmas     | Ekspluatācijas temperatūra no      | 32–110 grādiem              | 32            |
|            | Ekspluatācijas temperatūra līdz        | 32–110 grādiem              | 100           |
| Projekcijas | Kineskopa garantija | 6, 12, vai 18 mēneši         | 12.            |
|            | \# kineskopu skaits   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Atribūti un to veidi

Atribūti ir balstīti uz *atribūtu veidiem*. Atribūta veids norāda datu veidu, ko var ievadīt noteiktam atribūtam. Tiek atbalstīti šādi atribūtu veidi:

- **Valūta** – šis veids atbalsta valūtas vērtību. Tas var būt saistīts (var atbalstīt vērtību diapazonu) vai palikt atvērts.
- **DateTime** – šis veids atbalsta datuma un laika vērtības. Tas var būt saistīts vai palikt atvērts.
- **Decimāldaļa** – šis veids atbalsta skaitliskās vērtības, kas ietver decimāldaļskaitļus. Tas atbalsta arī mērvienības. Tas var būt saistīts vai palikt atvērts.
- **Vesels skaitlis** – šis veids atbalsta skaitliskas vērtības. Tas atbalsta arī mērvienības. Tas var būt saistīts vai palikt atvērts.
- **Teksts** – šis veids atbalsta teksta vērtības. Tas atbalsta arī iepriekš definētu iespējamo vērtību kopu (jeb *uzskaitījumu*).
- **Būla** – šis veids atbalsta binārās vērtības (**true** vai **false**).
- **Atsauce** – šis veids satur atsauces uz citiem atribūtiem.

### <a name="set-up-attribute-types"></a>Iestatīt atribūtu tipus

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Dodieties uz **Preču informācijas pārvaldība** &gt; **Iestatīšana** &gt; **Kategorijas un atribūti** &gt; **Atribūtu veidi**.
3. Izveidojiet divus atribūtu veidus **Teksts**, iestatiet opcijai **Pamatlīdzekļu saraksts** vērtību **Jā** un pēc tam pievienojiet vērtību sarakstu.

    - Vienam atribūta veidam piešķiriet nosaukumu **Lēcu forma** un pievienojiet šādas vērtības: **Ovāla**, **Kvadrāta** un **Taisnstūra**.
    - Otram atribūta veidam piešķiriet nosaukumu **Saulesbriļļu zīmols** un pievienojiet šādas vērtības: **Ray ban**, **Aviator** un **Oakley**.

![Atribūtu tipi](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Iestatīt atribūtu

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Dodieties uz **Preču informācijas pārvaldība** &gt; **Iestatīšana** &gt; **Kategorijas un atribūti** &gt; **Atribūti**.
3. Izveidojiet atribūtu ar nosaukumu **Lēcas**.
4. Iestatiet laukam **Atribūta veids** vērtību **Lēcu forma**.

![Atribūti](media/Attribute.png)

## <a name="attribute-metadata"></a>Atribūta metadati

*Atribūta metadati* ļauj atlasīt opcijas, lai norādītu katra preces atribūta izturēšanos. Piemēram, varat norādīt, vai atribūti ir obligāti, vai tos var izmantot meklēšanā un kā filtru.

Precēm atribūtu metadatu iestatījumus var ignorēt kanāla līmenī. Šī iespēja tiks apspriestas tālāk šajā tēmā.

Iespējams pamanījāt, ka lapā **Atribūti** ir ietvertas opcijas, kas ir saistītas ar atribūtu metadatiem. Sadaļā **Atribūtu metadati attiecībā uz POS** viena opcija, kam ir nosaukums **Var precizēt**, ietekmē atribūta vērtību izturēšanos pārdošanas punktā (POS) vai veidu, kā sistēma apstrādā šīs atribūta vērtības. Tikai atribūti, kam opcijai **Var precizēt** var iestatīt vērtību **Jā**, parādīsies precizēšanai vai preču filtrēšanai POS.

Tālāk ir sniegtas pārējās lapā **Atribūti** pieejamās atribūtu metadatu opcijas.

- Meklējams
- Izgūstams
- Var veidot vaicājumu
- Kārtojams
- Atļaut vairākas vērtības
- Ignorēt burtu reģistru un formatējumu
- Pilnīga atbilstība

Šīs opcijas ir sākotnēji paredzētas, lai uzlabotu tiešsaistes tīmekļa vitrīnas meklēšanas funkcionalitāti. Lai gan Commerce standarta komplektācija nav ietverta tiešsaistes tīmekļa vitrīna, tajā ir ietverts eCommerce publicēšanas programmatūras izstrādes komplekts (SDK). Debitori var izmantot šo SDK produktu ievietošanai vēlamajā meklēšanas indeksā. Lai gan preču dati tika importēti, debitori joprojām var atšķirt meklējamos datus, vaicājumā ietveramos datus utt. Tādā veidā var veidot optimālu indeksu, nodrošinot, ka viņu indekss attiecas tikai uz to, kas, *viņuprāt*, ir jāindeksē.

Informāciju par šo pārējo opciju mērķi skatiet rakstā [Server 2013 SharePoint meklēšanas shēmas apskats](/SharePoint/search/search-schema-overview).

## <a name="filter-settings-for-attributes"></a>Atribūtu filtra iestatījumi

Atribūtu filtra iestatījumi ļauj definēt to, kā atribūtu filtri tiek rādīti POS. Lai piekļūtu atribūta filtra iestatījumiem, lapā **Atribūti** atlasiet atribūtu un pēc tam darbību rūtī atlasiet **Filtra iestatījumi**.

Lapa **Filtra rādīšanas preferences** ietver šādus laukus:

- **Nosaukums** – pēc noklusējuma šis lauks ir iestatīts uz atribūta nosaukumu. Tomēr vērtību var mainīt.
- **Rādīšanas opcija** – ir pieejamas tālāk uzskaitītās opcijas.

    - **Viena vērtība** – opcija ir pieejama šādiem atribūtu veidiem: **Būla**, **Valūta**, **Decimāldaļa**, **Vesels skaitlis** un **Teksts**. Šī opcija ļauj klientā atlasīt vienu vērtību šiem atribūtiem precizēšanas nolūkā.
    - **Vairākas vērtības** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa**, **Vesels skaitlis** un **Teksts**. Šī opcija ļauj klientā atlasīt vairākas vērtības šim atribūtam precizēšanas nolūkā.

- **Rādīšanas vadība** – ir pieejamas tālāk uzskaitītās opcijas.

    - **Saraksts** – šī opcija ir pieejama visiem atribūtu veidiem.
    - **Diapazons** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.
    - **Slīdnis** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.
    - **Slīdnis ar joslām** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.

- **Sliekšņa vērtība** – šis iestatījums ir nepieciešams, ja atlasījāt **Diapazons** kā displeja vadības veidu. Vērtības var definēt, kā atdalītāju izmantojot semikolu (;).

    Piemēram, izmantojot filtru **Iepakojuma tilpums**, sliekšņa vērtība var būt **10; 20; 50; 100; 200; 500; 1000; 5000**. Šajā gadījumā POS rādīs tālāk minētos diapazonus. Diapazonus, kam nav preču, tiks parādīti pelēkoti.

    - Mazāk nekā 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 vai vairāk

![Atribūtu filtra iestatījumi](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Atribūtu grupas

Kad atribūti ir definēti, tos var piešķirt atribūtu grupām. *Atribūtu grupa* tiek lietota, lai grupētu atsevišķus komponenta vai apakškomponenta atribūtus preces konfigurēšanas modelī. Atribūtu varat iekļaut arī vairākās atribūtu grupās. Atribūtu grupas var palīdzēt lietotājiem konfigurēt preces, jo dažādas atlases tiek sakārtotas noteiktā kontekstā. Atribūtu grupas varat no jauna piešķirt kategorijām vai kanāliem.

Atribūtiem var iestatīt arī noklusējuma vērtības, kas tiek iekļautas atribūtu grupā. Piemēram, pievienojiet atribūtu grupai krāsas atribūtu un atlasiet **Zila** kā atribūta noklusējuma vērtību. Šajā gadījumā, ja atribūtu grupa tiek pievienota precei, kas ietver krāsu kā vienu no tās atribūtiem, **Zils** parādās kā noklusējuma krāsa attiecīgajai precei.

![Atribūtu grupas](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Izveidot atribūtu grupu

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Dodieties uz **Preču informācijas pārvaldība** &gt; **Iestatīšana** &gt; **Kategorijas un atribūti** &gt; **Atribūtu grupas**.
3. Izveido atribūtu grupu ar nosaukumu **Modernas saulesbrilles**.
4. Pievienojiet šādus atribūtus: **Lēcu forma** un **Saulesbriļļu zīmols**.

### <a name="assign-attribute-groups-to-categories"></a>Atribūtu grupu piešķiršana kategorijām

Vienu vai vairākas atribūtu grupas var saistīt ar kategoriju mezgliem šāda veida mazumtirdzniecības kategoriju hierarhijās: Commerce preču hierarhija, kanāla navigācijas kategoriju hierarhija un papildu preču kategoriju hierarhija. Kad preces ir sadalītas kategorijās, tās manto atribūtus, kas ir iekļauti atribūtu grupās.

![Preču hierarhija — preču atribūtu grupas](media/AGRetailProdHierarchy.PNG)

Izpildiet tālāk minētās darbības, lai piešķirtu atribūtu grupas kategorijām Commerce preču hierarhijā.

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Kategoriju un produktu pārvaldība** &gt; **Commerce produktu hierarhija**.
3. Atlasiet **modes navigācijas hierarhiju**.
4. Sadaļā **Vīriešu apģērbi** atlasiet kategoriju **Bikses**, kopsavilkuma cilnē atlasiet **Preču atribūtu grupas** un pēc tam pievienojiet atribūtu grupu ar nosaukumu **Vīriešu siksnas**.
5. Atlasiet kategoriju **Modernas saulesbrilles** un pārbaudiet jaunos atribūtu grupas **Modernas saulesbrilles** atribūtus, atlasot **Skatītu atribūtus**.

    Atribūtu grupā jābūt parādītam jaunajam atribūtam **Lēcu forma** un **Saulesbriļļu zīmols**.

6. Sadaļā **Vīriešu apģērbi** atlasiet kategoriju **Bikses**, pārbaudiet atribūtu grupas **Vīriešu siksnas** atribūtus, atlasot **Skatīt atribūtus**.

    Atribūtu grupā ir jārāda atribūti **Vīriešu siksnu zīmols**, **Siksnas audums** un **Siksnas lielums**.

> [!NOTE]
> Šo procedūru var izmantot arī, lai piešķirtu atribūtu grupas kategorijām kanāla navigācijas kategoriju hierarhijā un papildu preču kategoriju hierarhijā. 2. darbībā izmantojiet tālāk norādītos navigācijas ceļus.
>
> - Mazumtirdzniecība un komercija &gt; Kategorijas un preču pārvaldība &gt; Kanāla navigācijas kategorijas
> - Mazumtirdzniecība un komercija &gt; Kategorijas un preču pārvaldība &gt; Papildu preču kategorijas

### <a name="assign-attribute-groups-to-stores"></a>Atribūtu grupu piešķiršana veikaliem

Vienu vai vairākas atribūtu grupas var saistīt ar vienu vai vairākiem veikaliem veikalu hierarhijā. Kad preces ir bagātinātas noteiktiem veikaliem, tās manto atribūtus, kas ir iekļauti atribūtu grupās.

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **Kanālu kategorijas un preču īpašības**.
3. Atribūtu grupu piešķiršana Hjūstonas kanālam

    1. Atlasiet kanālu **Hjūstona**.
    2. Kopsavilkuma cilnē **Atribūtu grupa** atlasiet **Pievienot** un pēc tam laukā **Nosaukums** atlasiet **SharePointProvisionedProductAttributeGroup**.
    3. Vēlreiz atlasiet **Pievienot** un pēc tam laukā **Nosaukums** atlasiet **Vīriešu siksnas**.
    4. Vēlreiz atlasiet **Pievienot** un pēc tam laukā **Nosaukums** atlasiet **Modernas saulesbrilles**.

        > [!NOTE]
        > Opcija ļauj norādīt, ka šim kanālam ir jāmanto atribūtu grupas no tā pamata kanāla hierarhijā. Ja opcijai **Mantot** iestatīsiet **Jā**, atvasinātā kanāla mezgls pārmantos atribūtu grupas un visus atribūtus no šīm atribūtu grupām.

4. Iespējiet atribūtus, tā, lai tie būtu pieejami kanālā Hjūstona, veicot tālāk minētās darbības.

    1. Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.
    2. Atlasiet kategorijas mezglu **Mode** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.
    3. Atlasiet kategorijas mezglu **Modes aksesuāri**, atlasiet kategoriju **Modernas saulesbrilles** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.
    4. Atlasiet kategorijas mezglu **Vīriešu apģērbi**, atlasiet kategoriju **Bikses** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.

![Kanālu kategorijas un preču īpašības — atribūtu grupas](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Atribūta vērtību ignorēšāna

Preču līmenī var ignorēt atsevišķu preču atribūtu noklusējuma vērtības. Atribūtu noklusējuma vērtības arī var ignorēt atsevišķām precēm noteiktos katalogos, kas ir paredzēti specifiskiem kanāliem.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Atsevišķas preces atribūtu vērtību ignorēšana

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Dodieties uz **Mazumtirdzniecība un komercija** &gt; **Kategoriju un preču pārvaldība** &gt; **Izpildei nodotās preces pēc kategorijas**.
3. Atlasiet kategoriju mezglu **Mode** &gt; **Modes aksesuāri** &gt; **Modernas saulesbrilles**.
4. Režģī atlasiet nepieciešamo preci. Pēc tam darbību rūts grupas **Iestatīšana** cilnē **Prece** atlasiet **Preces īpašības**.
5. Kreisajā rūtī atlasiet atribūtu un pēc tam labajā rūtī atjauniniet tā vērtību.

![Preces detalizētas informācijas lapa — preču īpašību grupas](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Kataloga preču atribūtu vērtību ignorēšana

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Dodieties uz **Mazumtirdzniecība un komercija** &gt; **Kataloga pārvaldība** &gt; **Visi katalogi**.
3. Atlasiet katalogu **Fabrikam Base Catalog**.
4. Atlasiet kategoriju mezglu **Mode** &gt; **Modes aksesuāri** &gt; **Modernas saulesbrilles**.
5. Kopsavilkuma cilnē **Preces** atlasiet vajadzīgo preci un pēc tam atlasiet **Atribūti** virs preču režģa.
6. Tālāk minētajās kopsavilkuma cilnēs atjauniniet nepieciešamo atribūtu vērtības.

    - Koplietotie preces plašsaziņas līdzekļi
    - Koplietotās preces īpašības
    - Kanāla plašsaziņas līdzekļi
    - Kanāla preces īpašības

    > [!NOTE]
    > Ja tiek izveidots koplietots preces datu nesējs un koplietotas preces īpašības, tie tiek lietoti visām precēm.

![Kataloga preču īpašību grupas](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Kanāla preču atribūtu vērtību ignorēšana

1. Pierakstieties uzskaites daļas klientā kā preču pārvaldnieks.
2. Pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **Kanālu kategorijas un preču īpašības**.
3. Atlasiet kanālu **Hjūstona**.
4. Kopsavilkuma cilnē **Preces** atlasiet vajadzīgo preci un pēc tam atlasiet **Atribūti** virs preču režģa.

    > [!NOTE]
    > Ja neviena prece nav pieejama, pievienojiet preces kopsavilkuma cilnē **Preces** atlasot **Pievienot** un pēc tam dialoglodziņā **Preču pievienošana** atlasot vēlamās preces.

5. Tālāk minētajās kopsavilkuma cilnēs atjauniniet nepieciešamo atribūtu vērtības.

    - Koplietotie preces plašsaziņas līdzekļi
    - Koplietotās preces īpašības
    - Kanāla plašsaziņas līdzekļi
    - Kanāla preces īpašības

    > [!NOTE]
    > Ja tiek izveidots koplietots preces datu nesējs un koplietotas preces īpašības, tie tiek lietoti visām precēm.


[!INCLUDE[footer-include](../includes/footer-banner.md)]