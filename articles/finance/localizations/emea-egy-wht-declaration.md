---
title: Ieturētā nodokļa deklarācija Ēģiptei
description: Šajā tēmā paskaidrots, kā konfigurēt un ģenerēt ieturētā nodokļa deklarācijas Ēģiptei.
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574338"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Ieturētā nodokļa deklarācija Ēģiptei (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Pārskats
Šajā tēmā ir paskaidrots, kā iestatīt un ģenerēt ieturētā nodokļa deklarāciju un ieturētā nodokļa deklarācijas veidlapas Nr. 41 un 11 juridiskajām personām Ēģiptē 

Visiem Ēģiptes uzņēmumiem ir jāsagatavo veidlapa Nr. 41, kurā apkopoti visi nodokļi, kas tiek paturēti no vietējiem piegādātājiem un pakalpojumu sniedzējiem. Papildus veidlapai Nr. 41 ir jāizveido veidlapa Nr. 11, lai detalizētu visus ieturētos nodokļus no ārvalstu pakalpojumu sniedzējiem. 

**Ieturētā nodokļa deklarācijas** pārskatā programmā Dynamics 365 Finance ir iekļauti tālāk minētie pārskati.

- Deklarācijas veidlapa Nr. 41
- Deklarācijas veidlapa Nr. 11.
    
    
## <a name="prerequisites"></a>Priekšnosacījumi
Juridiskās personas primārajai adresei ir jāatrodas Ēģiptē.
Darbvietā **Līdzekļu pārvaldība** ir jāiespējo tālāk norādītais līdzeklis.

   - **Globālais ieturētais nodoklis**

Papildinformāciju par līdzekļu iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Atveriet **Nodoklis** > **Iestatīšana** > **Parametri** > **Virsgrāmatas parametri** un cilnē **Ieturētais nodoklis** iestatiet **Iespējot globālo ieturēto nodokli** uz **Jā**.
2. Darbvietā **Elektronisko pārskatu sniegšana** no repozitorija importējiet elektronisko pārskatu formātus:

    - WHT deklarācija Excel (EG)

    > [!NOTE]
    > Iepriekš minētais formāts ir balstīts uz **Nodokļu deklarēšanas modeli** un tas izmanto **Nodokļu deklarācijas modeļa kartējumu**. Šī papildu konfigurācija tiek importēta automātiski.

Papildinformāciju par elektronisko pārskatu konfigurāciju importēšanu skatiet sadaļā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde

WHT deklarācijas veidlapu no Ēģiptes īstenošana ir balstīta uz elektronisko pārskatu (ER) konfigurācijām. Papildinformāciju par konfigurējamām pārskata iespējām un koncepcijām skatiet sadaļā [Elektronisko pārskatu sniegšana](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Informācijai par ražošanas un lietotāju pieņemšanas testēšanas (UAT) vidēm skatiet instrukcijas tēmā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Lai ģenerētu ieturētās deklarācijas Ēģiptes juridiskajā personām, jāielādē šādas konfigurācijas:

- Nodokļu deklarācijas model.version.82.xml vai jaunāka versija
- Nodokļu deklarācijas modeļa mapping.version.82.133.xml vai jaunāka versija
- WHT deklarācijas Excel (EG).version.82.21 vai jaunāka versija

Pēc ER konfigurāciju lejupielādes no Lifecycle Services (LCS) vai globālā repozitorija pabeigšanas veiciet tālāk minētās darbības.

1. Pārejiet uz darbvietu **Elektroniskie pārskati** un atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
1. Lapas **Konfigurācijas** darbību rūtī atlasiet **Valūta > Ielādēt no XML faila**.
1. Augšupielādējiet visus failus tādā secībā, kādā tie ir uzskaitīti iepriekšējās biļetenos. Kad visas konfigurācijas ir augšupielādētas, konfigurācijas kokam ir jābūt redzamam programmā Finance.

## <a name="set-up-application-specific-parameters"></a>Programmai raksturīgu parametru iestatīšana

Programmai raksturīgo parametru opcija ļauj lietotājiem izveidot kritērijus, kā nodokļu darījumi tiek klasificēti un aprēķināti katrā ģenerētā pārskata rindā atkarībā no **ieturētā nodokļa krājumu grupas** konfigurācijas vai citiem kritērijiem, kas noteikti uzmeklēšanas definīcijā.

Ieturētās deklarācijas veidlapā Nr. 41 ir iekļauta noteikta kolonna, kur ieturētā nodokļa darījums ir jāklasificē saskaņā ar nodokļu iestādes klasifikāciju ar nosaukumu **Atlaides koda veids**. Tā vietā, lai šīs jaunās klasifikācijas iekļautu kā jaunus ierakstu datus, grāmatojot darbības, klasifikācijas tiks noteiktas, pamatojoties uz dažādām uzmeklēšanām, kas ieviestas **Konfigurācijas** > **Programmai specifisku parametru iestatīšana** > **Iestatīšana**, lai izpildītu ieturēšanas pārskatu prasības Ēģiptei. 

Šī konfigurācija tiek izmantota, lai klasificētu darījumus Ieturētās deklarācijas veidlapas Nr. 41 pārskatā:

- **DiscountTaxTypeLookup** -> kolonna Nr. 18 

Veiciet tālāk norādītās darbības, lai iestatītu dažādās uzmeklēšanas, kas tiek izmantotas WHT deklarācijas un saistīto grāmatu pārskatu ģenerēšanai. 

1. Darbvietā **Elektronisko pārskatu sniegšana** atlasiet **Konfigurācijas** > **Iestatījumi**, lai iestatītu kārtulas, kas nosaka, kā identificēt to, kā darījumi tiek klasificēti WHT deklarācijas pārskatā. 
2. Atlasiet pašreizējo versiju un kopsavilkuma cilnē **Uzmeklēšanas** atlasiet uzmeklēšanas nosaukumu. Piemēram, **DiscountTaxTypeLookup**. Šī uzmeklēšana identificē nodokļu iestādes pieprasīto atlaižu veidu sarakstu.
3. Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot** un jaunajā rindā kolonnā **Uzmeklēšanas rezultāti** atlasiet saistīto rindu, kas apzīmē klasifikāciju **18. kolonnā**.
4. Kolonnā **Ieturētā nodokļa krājumu grupa** atlasiet saistīto kodu, kas tiek izmantots klasifikācijas identificēšanai. Piemēram, **Atļautā atlaide**.  
5. Atkārtojiet 3. un 4. darbību visām pieejamajām uzmeklēšanām.
6. Vēlreiz atlasiet **Pievienot**, lai ietvertu galīgo ieraksta rindu, un kolonnā **Uzmeklēšanas rezultāti** atlasiet **Nav attiecināms**. 
7. Atlikušajās kolonnās atlasiet **Nav tukšs**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Virsgrāmatas parametru iestatīšana

Lai izveidotu WHT deklarācijas veidlapas pārskatus Microsoft Excel, definējiet ER formātu lapā **Virsgrāmatas parametri**.

1. Atveriet **Nodoklis** > **Iestatīšana** > **Virsgrāmatas parametri**.
2. Cilnes **Ieturētais nodoklis** laukā **WHT deklarācijas formāta kartēšana** atlasiet **WHT deklarācija Excel (EG)**. Ja šo lauku atstājat tukšu, standarta PVN pārskats tiks ģenerēts SSRS formātā.


![Deklarācijas veidlapa](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Ģenerēt ieturētās deklarācijas veidlapas
Ieturētā nodokļa deklarācijas veidlapas sagatavošanas un iesniegšanas process noteiktam periodam ir balstīts uz ieturētā nodokļa darījumiem, kas grāmatoti apmaksas un iegrāmatošanas maksājuma nodokļa darba laikā. Plašāku informāciju par globālo ieturēto nodokli skatiet sadaļā [Globālais ieturētais nodoklis](../general-ledger/global-withholding-tax-overview.md).

Lai ģenerētu nodokļu deklarācijas pārskatu, veiciet tālāk norādītās darbības.

1. Atveriet **Nodoklis** > **Deklarācijas** > **Ieturētais nodoklis** > **Ieturētā nodokļa maksājums*.
2. Atlasiet apmaksas periodu un pēc tam atlasiet pārskata sākuma datumu. 
3. Ievadiet darījuma datumu un pēc tam atlasiet **Labi**.
4. Atvērtajā dialoglodziņā atlasiet vienu vai vairākus veidlapu veidus **Veidlapa Nr. 41**, **Veidlapa Nr. 11** vai **Neviens**. Ja atlasāt **Neviens**, tiek ģenerēts standarta pārskats. 
5. Atlasiet valodu. Visi pārskati tiek tulkoti **en-us** un **ar-eg**.
6. Ievadiet bankas filiāli un nosaukumu, kur tiks veikts nodokļu maksājums.
7. Atlasiet biznesa veidu un tad ievadiet čeka un dokumenta numurus. 
8. Ievadiet entītijas veidu. 
9. Ievadiet tās personas vārdu, kas reģistrēta, lai piešķirtu formu, un atlasiet **Labi**, lai apstiprinātu pārskata ģenerēšanu. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
