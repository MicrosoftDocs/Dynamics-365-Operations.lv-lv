---
title: Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība
description: Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML).
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770074"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML). 

Pēc preču ieteikumu iespējošanas stāsies spēkā noklusējuma iestatījumi; šie parametri darbosies, lai varētu strādāt daudzām vajadzībām. Ieteicams ieplānot kādu laiku, lai novērtētu, vai rezultāti atbilst preču pārdošanas kustībai. Pirms atkārtotas testēšanas ieteicams dažas dienas novērtēt rezultātus pirms parametru mainīšanas pēc nepieciešamības. 

## <a name="understanding-recommendation-list-parameters"></a>Ieteikumu saraksta parametru izprašana

Pirms mainīt parametrus, uzziniet, kā tie ietekmēs tālāk minētos rezultātus.

### <a name="trending-product-list"></a>Populāru preču saraksts

Preču sarakstam **Populārs** ir divi parametri, ko var mainīt: ![Populāru preču saraksta noklusējuma parametru piemērs](./media/exampletrendingparameters.png)
1. **Iekļaut jaunas preces no pēdējām X dienām** — preces, kas ir pievienotas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai atlasītu preču kandidātus. Attēla noklusētā vērtība norāda, ka preces, kas ir līdz 180 dienas vecas, var izmantot populāru preču sarakstā.
1. **Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces. Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu populāru preču sarakstā. 

### <a name="best-selling-product-list"></a>Vispirktāko preču saraksts

Atkarībā no jūsu biznesa, vispirktākais var dot atšķirīgus rezultātus nekā populārs, kaut gan tie abi izmanto transakciju datus, lai pasūtītu preces. Tā kā vispirktākajam nav izslēgšanas, pamatojoties uz sortimenta datumu, vispirktākais joprojām var izcelt ļoti populāras, vecākās preces, kas var būt izmestas no populāro preču saraksta. 

Preču sarakstam **Vispirktākais** ir viens parametrs, ko var mainīt.

![Vispirktāko preču saraksta noklusējuma parametra piemērs](./media/examplebestsellingparameters.PNG)
1. **Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces. Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu vispirktāko preču sarakstā. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Preču manuāla pievienošana ieteikumu sarakstiem vai noņemšana no tiem

### <a name="for-new-trending-or-best-selling"></a>Sarakstiem Jauns, Populārs vai Vispirktākais

1.  Dodieties uz **Mazumtirdzniecība** > **Preču ieteikumi** > **Ieteikuma parametri**.
1.  Mazumtirdzniecības koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.
1.  Atlasiet sarakstu, kuram pievienot vai noņemt preces.
1.  Lai tabulai pievienotu preces, atlasiet **Pievienot rindu**. 
1.  Sadaļā preces kolonna meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai preču sarakstā Jauns](./media/examplenewlistconfiguration1.png)
1.  Kolonnas rindas veidā atlasiet vienu no divām opcijām:
    -   **Iekļaut** — forsē preci uz saraksta priekšgalu
    -   **Izslēgt** — noņem preci no parādīšanās sarakstā ![Piemērs preces iekļaušanai vai izslēgšanai no preču saraksta Jauns](./media/examplenewlistconfiguration2.png)
1.  Mainot **Rādīšanas secība**, tiks mainīta secība, kādā prece, kas atzīmēta ar **Iekļaut**, parādīsies sarakstā.
    - Ja divām precēm ir tāda pati vērtība **Rādīšanas secība**, šo divu rezultātu galīgā secība var atšķirties no tās, kas ir birojā.
1.  Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet **Noņemt**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Sarakstiem Pircējiem patīk vai Bieži iegādāts kopā

**Bieži iegādāts kopā** vai **Pircējiem patīk** sarakstu kontekstā mašīnmācība tiek izmantota, lai analizētu patērētāju pirkšanas paradumus un ieteiktu saistītās preces, kas parasti tiek iegādātas kopā, izveidojot unikālu sākuma preci. 
 
**Sākuma prece** ir prece, kurai vēlaties ģenerēt rezultātus. Manuāli pielāgotu ieteikumu sarakstu kontekstā jūs pievienojat vai noņemat šīs preces rezultātus. 

Veiciet tālāk minētās darbības, lai manuāli pievienotu vai noņemtu rezultātus sākuma precei.
1.  Atlasiet **Sākuma prece**. 
1.  Kolonnā **Prece** meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai sarakstā Bieži iegādāts kopā](./media/exampleFBTlistconfiguration1.png)
1. Kolonnā **Rindas veids** atlasiet vienu no divām opcijām:
    - **Iekļaut** — forsē preci uz saraksta priekšgalu
    - **Izslēgt** — noņem preci no parādīšanās sarakstā     
![Piemērs preces iekļaušanai vai izslēgšanai no saraksta Bieži iegādāts kopā](./media/exampleFBTlistconfiguration2.png)
1.  Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet Noņemt.


## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Preču ieteikumu iespējošana](enable-product-recommendations.md)

[Preču ieteikumu sarakstu pievienošana lapām](add-reco-list-to-page.md)
