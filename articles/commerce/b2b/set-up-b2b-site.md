---
title: B2B e-komercijas vietnes iestatīšana
description: Šajā tēmā aprakstīts, kā iestatīt uzņēmums-uzņēmums (B2B) e-komercijas vietni programmā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 31266f84270f170e172eadea75a90397c5a6e8e6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691922"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B e-komercijas vietnes iestatīšana

[!include [banner](../../includes/banner.md)]

Uzņēmums-uzņēmums (B2B) e-komercijas vietnes nodrošina dažas galvenās iespējas, kas optimizē darbplūsmu B2B lietotājam. Šajā tēmā aprakstīts, kā iestatīt B2B e-komercijas vietni programmā Microsoft Dynamics 365 Commerce. Tajā aplūkoti moduļi un vietas iestatījumi, kas jākonfigurē, lai iespējotu B2B raksturīgos scenārijus.

## <a name="prerequisites"></a>Priekšnosacījumi

- Lai iestatītu B2B e-komercijas vietni, ir jāiespējo un jākonfigurē noteikti programmas Commerce Headquarters līdzekļi, kā aprakstīts šajā tēmā.
- Galveno pieredzi, piemēram, preču pamanīšanu, preču informācijas lapas, grozu un pārbaudi, darbina tie paši moduļi, kas tiek izmantoti uzņēmums-patērētājs (B2C) e-komercijas vietnēm. Vietnes autoriem ir jāiepazīstas ar visiem moduļiem, ko Dynamics 365 Commerce atbalsta. Papildinformāciju skatiet [Moduļu bibliotēkas pārskats](../starter-kit-overview.md).
- Šajā tēmā tiek pieņemts, ka vietas autori izprot Commerce vietnes veidotāja pamatelementus, veidnes, fragmentus un lapas, tādējādi tie var iespējot B2B līdzekļus e-komercijas vietnēm.

## <a name="site-level-settings"></a>Vietnes līmeņa iestatījumi

Jūs varat piekļūt vietnes līmeņa iestatījumiem vietnes veidotājā, **Vietnes iestatījumi \> Paplašinājumi**. Nākamie divi vietnes līmeņa iestatījumi attiecas uz B2B scenārijiem:

- **Iespējot debitora konta maksājumus** – šis rekvizīts ļauj lietotājiem maksāt par pasūtījumiem, izmantojot debitora kontus. Pieejamās vērtības ir **Iespējots B2B debitoriem**, **Iespējots B2C debitoriem**, **Iespējots visiem debitoriem** un **Atspējots visiem debitoriem**. Ja jūsu B2B vietne atbalsta debitoru kontus, jums jāatlasa **Iespējots B2B debitoriem**.
- **Iespējot pasūtījuma daudzuma ierobežojumus** – šis rekvizīts ļauj iestatīt krājumu skaita ierobežojumus, ko var pasūtīt katrai precei vai kategorijai. Pieejamās vērtības ir **Iespējots B2B debitoriem**, **Iespējots B2C debitoriem**, **Iespējots visiem debitoriem** un **Atspējots visiem debitoriem**.

> [!NOTE]
> Jauninot uz pēdējo moduļa bibliotēkas versiju, jums jāizpilda papildu darbības, lai nodrošinātu, ka jūsu vidē ir pieejami iepriekš aprakstītie vietnes iestatījumi. Papildinformāciju skatiet [Faila app.settings.json atjaunināšana](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Biznesa partnera pierakstīšanās lapu izveide

Lai kļūtu par biznesa partneri, lietotājiem vispirms jāiesniedz biznesa partnera pieprasījums. Saite uz biznesa partnera pieprasījuma lapu būs pieejama B2B sākumlapā, lai lietotāji varētu sākt procesu. Kad lietotāji iesniedz biznesa partnera pieprasījumu, viņi saņems apstiprinājumu, ka pieprasījums ir iesniegts. 

### <a name="create-a-business-partner-request-page"></a>Biznesa partnera pieprasījuma lapas izveide

Modulis **Partnera pierakstīšanās** biznesa partnera pieprasījuma lapā tiek izmantots, lai uzsāktu lietotāju pieprasījumus, lai kļūtu par biznesa partneriem. Šis modulis ļauj jums apkopot informāciju par lietotāju, kas ir nepieciešama pierakstīšanās procesam. Turklāt modulis **Uzņēmuma konta adrese** tiek izmantots, lai tvertu lietotāja adresi.

Lai iestatītu un konfigurētu biznesa partnera pieprasījumu lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izveidojiet veidni ar nosaukumu **Pierakstīšanās**. Šajā veidnē jāiekļauj tālāk minētie moduļi:

    - Partnera reģistrācija
    - Atpakaļceļš
    - Galvene
    - Kājene
    - Satura bloks
    - Teksta bloks
    - Produktu kolekcija

1. Izmantojiet veidni **Pierakstīšanās**, lai izveidotu lapu ar nosaukumu **Biznesa partnera pieprasījums**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz sākumlapu un ievadiet **Sākums** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Partnera pierakstīšanās** zem moduļa **Atpakaļceļš**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Kļūt par biznesa partneri**.
1. Slotā **Partnera pierakstīšanās** pievienojiet moduli **Uzņēmuma konta adrese**.
1. Slotā **Konteiners** pievienojiet moduli **Teksta bloks** zem moduļa **Partnera pierakstīšanās**. Šeit varat noteikt definēt pierakstīšanās procesa noteikumus un nosacījumus.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.

### <a name="create-a-business-partner-request-confirmation-page"></a>Biznesa partnera pieprasījuma apstiprināšanas lapas izveide

Pēc biznesa partnera pieprasījuma iesniegšanas lietotājam ir jāparāda apstiprinājuma lapa, lai atzītu iesniegšanu. 

Lai iestatītu un konfigurētu pieprasījumu apstiprināšanas lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet veidni **Pierakstīšanās**, ko iepriekš izveidojāt, lai izveidotu lapu ar nosaukumu **Partnera pieprasījuma apstiprināšana**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Satura bloķēšana**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Pieprasījums iesniegts**. Laukā **Bagātinātais teksts** ievadiet **Jūsu pieprasījums ir iesniegts**. Sadaļā **Saites** konfigurējiet saiti uz sākumlapu un ievadiet **Atpakaļ uz iepirkšanos** kā saites tekstu.
1. Pievienojiet vēl vienu moduli **Konteiners** un pievienojiet tam moduli **Preču kolekcija**.
1. Konfigurējiet moduli **Preču kolekcija** ar rekomendāciju vai kategoriju sarakstu, kuru vēlaties rādīt lapā.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.

Lai pievienotu saiti pieprasījumu apstiprināšanas lapai vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Atveriet iepriekš izveidoto lapu **Biznesa partnera pieprasījums** un atlasiet **Rediģēt**. 
1. Atlasiet moduļa slotu **Partnera pierakstīšanās**. Rekvizītu rūtī zem **Saite uz pierakstīšanās apstiprinājuma lapu** konfigurējiet saiti uz iepriekš izveidoto biznesa partnera pieprasījuma lapu. 
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Biznesa partnera pieprasījuma saites uz sākumlapu pievienošana

Kad biznesa partnera pieprasījuma pierakstīšanās un apstiprinājuma lapas ir izveidotas, pierakstīšanās lapai jābūt pieejamai, izmantojot sākumlapas saiti. Varat izpildīt šo uzdevumu, pievienojot saiti jebkuram modulim **Satura bloķēšana** sākumlapā.

Lai pievienotu biznesa partnera pieprasījuma saiti sākumlapai vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Atveriet savas vietnes sākumlapu un atlasiet **Rediģēt**.
1. Atlasiet moduļa slotu **Satura bloķēšana**. Moduļa rekvizītu rūtī zem **Saites** konfigurējiet saiti uz biznesa partnera pieprasījuma lapu, ko iepriekš izveidojāt, un ievadiet **Pierakstīties, lai kļūtu par biznesa partneri** vai līdzīgu tekstu kā saites tekstu. Pievienojiet atbilstošu attēlu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="account-management-landing-page"></a>Konta pārvaldības mērķlapa

Konta pārvaldības ielādes lapā ir iekļauta visa konta pārvaldības informācija, kas nepieciešama gan B2B, gan B2C e-komercijas vietnēm. Šo lapu var apskatīt tikai lietotāji, kas ir pierakstījušies.

Lai izveidotu un konfigurētu B2B konta pārvaldības ielādes lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izveidojiet veidni ar nosaukumu **Konta pārvaldība**. Šajā veidnē jāiekļauj tālāk minētie moduļi:

    - Galvene
    - Kājene
    - Atpakaļceļš
    - Konta sveiciena elements
    - Konta vispārīgais elements
    - Konta adreses elements
    - Konta vēlmju saraksta elements
    - Konta adreses elements
    - Konta lojalitātes programmas elements
    - Konta klienta bilances elements
    - Konta pasūtījuma veidņu elements
    - Organizācijas lietotāji
    - Biznesa organizāciju saraksts
    - Klienta konta bilance
    - Pasūtījuma veidnes rindas
    - Pasūtījuma veidnes saraksts
    - Konta rēķina elements
    - Rēķinu saraksts
    - Rēķina informācija

1. Izmantojiet veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Mans konts**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. 
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz sākumlapu un ievadiet **Sākums** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Sveiciena elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Laipni lūdzam**.
1. Slotā **Galvenais** pievienojiet vēl vienu moduli **Konteiners** (**2. konteiners**). Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. Iestatiet vērtību **Rādītie apakšelementi** uz **Divi**. 
1. Slotā **2. konteiners** pievienojiet moduli **Konta vispārīgais elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Mans profils**. Sadaļā **Saites** konfigurējiet saiti uz lapu **Mans profils**. 
1. Slotā **2. konteiners** pievienojiet vēl vienu moduli **Konta vispārīgais elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Pasūtījumu vēsture**. Sadaļā **Saites** konfigurējiet saiti uz lapu Pasūtījumu vēsture.
1. Slotā **Galvenais** pievienojiet vēl vienu moduli **Konteiners** (**3. konteiners**). Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. Iestatiet vērtību **Rādītie apakšelementi** uz **Divi**. 
1. Slotā **3. konteiners** pievienojiet moduli **Konta adreses elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Mana adrese**. Sadaļā **Saites** konfigurējiet saiti uz lapu **Mana adrese**. 
1. Slotā **3. konteiners** pievienojiet moduli **Konta vēlmju saraksta elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Mans vēlmju saraksts**. Sadaļā **Saites** konfigurējiet saiti uz lapu **Mans vēlmju saraksts**.
1. Slotā **Galvenais** pievienojiet vēl vienu moduli **Konteiners** (**4. konteiners**). Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. Iestatiet vērtību **Rādītie apakšelementi** uz **Divi**. 
1. Slotā **4. konteiners** pievienojiet moduli **Organizācijas lietotāji**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Organizācijas lietotāji**. 
1. Slotā **4. konteiners** pievienojiet moduli **Konta debitora bilances elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Konta kredīts**. 
1. Slotā **Galvenais** pievienojiet vēl vienu moduli **Konteiners** (**5. konteiners**). Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. Iestatiet vērtību **Rādītie apakšelementi** uz **Divi**. 
1. Modulī **5. konteiners** pievienojiet moduli **Konta pasūtījuma veidņu elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Pasūtījuma veidnes**. 
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

> [!NOTE] 
> Dažas sadaļas, ko pievienojāt 13.–18. darbībā, neparādīsies pamatnē "tas, ko redzat, ir tas, ko iegūsiet" (WYSIWIG) vietnes veidotājā, jo tām nepieciešams pierakstīties B2B kontā.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Debitora bilances lapu un moduļu izveide un konfigurēšana 

Debitoru kontus var izmantot, lai maksātu par pasūtījumiem. Pieejamo bilanci debitora kontā var skatīt no lietotāja konta pārvaldības lapas.

### <a name="create-a-customer-balance-page"></a>Debitora bilances lapas izveide 

Pirms lietotāji, kas pierakstījušies B2B, var skatīt savu debitora bilanci, jāizveido debitora bilances lapa. 

Lai izveidotu debitora bilances lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Debitora bilance**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet vēl vienu moduli **Konteiners** (**3. konteiners**). Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**. Iestatiet vērtību **Rādītie apakšelementi** uz **Divi**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Debitora konta bilances elements**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Konta bilance**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.
1. Atveriet iepriekš izveidoto konta pārvaldības ielādes lapu (**Mans konts**).
1. Moduļa **Konta debitora bilances elements** rekvizītu rūtī pievienojiet saiti uz debitora bilances lapu. 
1. Saglabājiet un publicējiet lapu.

Debitora bilances lapa tagad ir izveidota, un lietotāji var tai piekļūt no konta pārvaldības informācijas lapas.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Norēķinu lapas konfigurēšana, lai debitora bilanci varētu izmantot kā maksājuma veidu

Lai debitora bilanci varētu izmantot kā maksājuma veidu, ir jāiespējo modulis **Debitora konta maksājums**. Šis modulis jāpievieno norēķinu lapai kā maksājuma veids. Informāciju par to, kā konfigurēt norēķinu lapu un moduļus, kas nepieciešami norēķiniem, tostarp visu maksājuma informāciju, skatiet [Norēķināšanās modulis](../add-checkout-module.md).

Pēc tam, kad esat konfigurējis norēķināšanās lapu, jums ir jāpievieno modulis **Debitora konta maksājums** maksājumu sadaļai, un pēc tam saglabājiet un publicējiet lapu. Tad B2B lietotāji varēs pierakstīties e-komercijas vietnē un izmantot savu pieejamo debitoru bilanci pasūtījumiem norēķināšanās laikā.

Turklāt sadaļā **Vietnes veidotājs \> Paplašinājumi** jums jānodrošina, ka rekvizīts **Iespējot debitora konta maksājumus** ir iestatīts uz **Iespējots B2B debitoriem**.

## <a name="create-order-template-pages"></a>Pasūtījuma veidņu lapu izveide

B2B e-komercijas vietnei var būt iestatītas divas pasūtījuma veidnes lapas: pasūtījumu veidņu saraksta lapa un pasūtījuma veidnes rindu lapa.

Pasūtījuma veidņu saraksta lapa rāda visu pieejamo pasūtījuma veidņu sarakstu. Tā ir iestatīta, izmantojot moduli **Pasūtījuma veidņu saraksts**. Pasūtījuma veidņu saraksta lapa ļauj jums izveidot vai dzēst veidni un pievienot krājumus veidnē grozam.

Pasūtījuma veidnes rindu lapa parāda pasūtījuma veidnes detaļas, kas ir atlasītas pasūtījumu veidņu saraksta lapā. Tā ir iestatīta, izmantojot moduli **Pasūtījuma veidņu rindas**. Kad lietotājs atlasa veidnes nosaukumu pasūtījuma veidņu saraksta lapā, tiek parādīta pasūtījuma veidnes rindu lapa un detalizēta informācija par veidni. Lietotājs pēc tam var apskatīt un rediģēt vienības veidnē.

### <a name="create-an-order-templates-list-page"></a>Pasūtījuma veidņu saraksta lapas izveide

Lai izveidotu pasūtījuma veidņu saraksta lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Pasūtījuma veidnes**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Pasūtījuma veidņu saraksts**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.
1. Atveriet iepriekš izveidoto konta pārvaldības ielādes lapu (**Mans konts**).
1. Moduļa **Konta pasūtījuma veidņu elements** rekvizītu rūtī zem **Saites** konfigurējiet saiti uz pasūtījuma veidņu sarakstu, ko tikko izveidojāt.
1. Saglabājiet un publicējiet lapu.

Pasūtījuma veidņu saraksta lapa tagad ir izveidota, un lietotāji var tai piekļūt no konta pārvaldības informācijas lapas.

### <a name="create-an-order-template-lines-page"></a>Pasūtījuma veidnes rindu lapas izveide

Lai izveidotu pasūtījuma veidnes rindu lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Pasūtījuma veidnes rindas**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Pasūtījuma veidnes rindas**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.

## <a name="onboard-business-partner-users"></a>Onboard biznesa partnera lietotāji

Organizācijas lietotāju lapa ļauj biznesa partnera organizācijas administratoram pievienot papildu lietotājus no šīs organizācijas B2B e-komercijas vietnei. Tas tiek iestatīts, izmantojot moduli **Biznesa organizāciju saraksts**. Organizācijas lietotāju lapā administrators var pievienot vai noņemt lietotājus, definēt konta bilances un pieprasīt pārskatus lietotājam.

Lai izveidotu organizācijas lietotāju lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Organizācijas lietotāji**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Biznesa organizāciju saraksts**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Organizācijas lietotāji**.
1. Moduļa **Biznesa organizāciju saraksts** rekvizītu rūtī iespējojiet rekvizītus **Tabulas šķirošana** un **Tabulas lapu numerācija**. Iestatiet lapu numerācijas skaitu uz **5**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.
1. Atveriet iepriekš izveidoto konta pārvaldības ielādes lapu (**Mans konts**).
1. Moduļa **Organizācijas lietotāju elements** rekvizītu rūtī zem **Saites** konfigurējiet saiti uz organizācijas lietotāju lapu, ko tikko izveidojāt. 
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="create-invoice-pages"></a>Rēķina lapu izveide

Rēķinu saraksta lapa rāda visu pieejamo rēķinu sarakstu. Tā ir iestatīta, izmantojot moduli **InvoicesList**. No rēķinu saraksta lapas lietotāji var apmaksāt vai pieprasīt rēķinus. 

Rēķina detalizētas informācijas lapa parāda detalizētu informāciju par rēķinu, kas ir atlasīts rēķinu saraksta lapā. Tā ir iestatīta, izmantojot moduli **Rēķina informācija**. Kad lietotājs rēķinu saraksta lapā atlasa rēķina ID, tiek parādīta rēķina informācijas lapa un tā sniedz detalizētu informāciju par rēķinu.

### <a name="create-an-invoices-list-page"></a>Rēķinu saraksta lapas izveide

Lai izveidotu rēķinu saraksta lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Rēķinu saraksts**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **InvoicesList**. Moduļa rekvizītu rūts sadaļā **Galvene** ievadiet **Rēķini**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.
1. Atveriet iepriekš izveidoto konta pārvaldības ielādes lapu (**Mans konts**).
1. Moduļa **Konta rēķinu elements** rekvizītu rūtī zem **Saites** konfigurējiet saiti uz rēķinu saraksta lapu, ko tikko izveidojāt. 
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="create-an-invoice-details-page"></a>Rēķina detalizētās informācijas lapas izveide

Lai izveidotu rēķina detalizētas informācijas lapu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Izmantojiet iepriekš izveidoto veidni **Konta pārvaldība**, lai izveidotu lapu ar nosaukumu **Rēķina detalizēta informācija**.
1. Slotā **Galvene** pievienojiet galvenes fragmentu, kas ir iepriekš konfigurēts ar vietnes galveni.
1. Slotā **Kājene** pievienojiet kājenes fragmentu, kas ir iepriekš konfigurēts ar vietnes kājeni.
1. Slotā **Galvenais** pievienojiet moduli **Konteiners**. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** pievienojiet moduli **Atpakaļceļš**. Moduļa rekvizītu rūtī sadaļā **Saites** konfigurējiet saiti uz konta pārvaldības ielādes lapu un ievadiet **Mans konts** kā saites tekstu. Pēc tam konfigurējiet saiti uz rēķinu saraksta lapu un ievadiet **Rēķinu saraksti** kā saites tekstu.
1. Slotā **Konteiners** pievienojiet moduli **Rēķina informācija**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Publicējiet lapas vietrādi URL.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Pievienot ātrās pievienošanas moduli groza lapai

Ātrās pievienošanas modulis nodrošina veidu, kā ātri pievienot grozam vairākus krājumus, izmantojot krājumu ID (zināmu arī kā noliktavas vienības \[SKU\] ID). Ātrās pievienošanas modulis tiek pievienots vietnes groza lapai.

Lai pievienotu ātrās pievienošanas moduli groza lapai programmā Commerce vietnes veidotājs, veiciet tālāk norādītās darbības.

1. Dodieties uz **Veidnes** un atlasiet jūsu vietnes groza lapas veidni.
1. Atlasiet **Rediģēt**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Ātrā pievienošana** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet jūsu vietnes groza lapu.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Rekvizītu rūtī modulim **Konteiners** zem **Platums** atlasiet **Aizpildīt konteineru**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Ātrā pievienošana** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

> [!NOTE] 
> Ātrās pievienošanas modulis ir pieejams Commerce versijas 10.0.17 laidienā. Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>Pievienot lielapjoma pirkšanas moduli preču informācijas lapai

Lielapjoma pirkšanas modulis preču informācijas lapā (PDP) nodrošina uz matricu balstītu pieredzi, kas ļauj pircējam ātri pievienot grozam vairākus preces variantus. Ja vietas lietotājam jākārto vairāki vienas preces varianti, šī pieredze izslēdz nepieciešamību atlasīt preču dimensiju kombināciju, definēt daudzumu, pievienot variantu grozam un pēc tam atkārtot procesu citām preču dimensiju kombinācijām.

Lai pievienotu lielapjoma pirkšanas moduli PDP Commerce site Builder, sekojiet šiem soļiem.

1. Dodieties **uz** veidnēm un atlasiet jūsu vietnes PDP veidni.
1. Atlasiet **Rediģēt**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā Pievienot **moduli atlasiet** lielapjoma pirkšanas **moduli un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties **uz** lapām un atlasiet jūsu vietnes PDP.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Moduļa Konteiners rekvizītu **rūtī**, zem **platums**, atlasiet Aizpildīt **konteineru**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā Pievienot **moduli atlasiet** lielapjoma pirkšanas **moduli un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

> [!NOTE] 
> Lielapjoma pirkšanas modulis ir pieejams commerce versijā 10.0.24. Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](../starter-kit-overview.md)

[SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Autorēšanas lapas pārskats](../authoring-home-overview.md)

[Pārskats par veidnēm un izkārtojumiem](../templates-layouts-overview.md)

[Darbs ar fragmentiem](../work-with-fragments.md)

[Jaunas vietnes lapas pievienošana](../add-new-page.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Satura bloka modulis](../add-hero-module.md)

[Preču kolekciju modulis](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
