---
title: Uz AI-ML balstītu preču ieteikumu rezultātu pielāgošana
description: Šajā rakstā skaidrots, kā pielāgot preču rekomendāciju rezultātus, balstoties uz klienta biznesa inteliģences apmācību (AI-ATTIECĪBĀ UZ).
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74fa013d44e0f113bdf0ce0ca9efeb943926e9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901706"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Uz AI-ML balstītu preču ieteikumu rezultātu pielāgošana


[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā pielāgot preču rekomendāciju rezultātus, balstoties uz jūsu biznesa inteliģences iespējām (AI-ATTIECĪBĀ UZ). 

Pēc preču ieteikumu iespējošanas stāsies spēkā noklusējuma iestatījumi; šie parametri darbosies, lai varētu strādāt daudzām vajadzībām. Ieteicams ieplānot kādu laiku, lai novērtētu, vai rezultāti atbilst preču pārdošanas kustībai. Pirms atkārtotas testēšanas ieteicams dažas dienas novērtēt rezultātus pirms parametru mainīšanas pēc nepieciešamības. 

## <a name="understanding-recommendation-list-parameters"></a>Ieteikumu saraksta parametru izprašana

Pirms mainīt parametrus, uzziniet, kā tie ietekmēs tālāk minētos rezultātus.

### <a name="trending-product-list"></a>"Populāru" preču saraksts

"Populāru" preču sarakstam ir divi maināmi parametri:

![Saraksta "Populāras" noklusējuma parametru piemērs](./media/exampletrendingparameters.png)

1. **Iekļaut jaunas preces no pēdējām X dienām** — preces, kas ir pievienotas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai atlasītu preču kandidātus. Attēla noklusētā vērtība norāda, ka preces, kas ir līdz 180 dienas vecas, var izmantot populāru preču sarakstā.
1. **Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces. Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu populāru preču sarakstā. 

### <a name="best-selling-product-list"></a>"Vispirktāko" preču saraksts

Atkarībā no jūsu biznesa, sarakts "Vispirktākās" var dot atšķirīgus rezultātus nekā populāro preču sarakstus, kaut gan tie abi izmanto transakciju datus, lai pasūtītu preces. Tā kā vispirktākajam nav izslēgšanas, pamatojoties uz sortimenta datumu, vispirktākais joprojām var izcelt ļoti populāras, vecākās preces, kas var būt izmestas no populāro preču saraksta. 

Preču sarakstam "Vispirktākās" ir viens parametrs, ko var mainīt.

![Vispirktāko preču saraksta noklusējuma parametra piemērs.](./media/examplebestsellingparameters.PNG)

1. **Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces. Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu vispirktāko preču sarakstā. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Preču manuāla pievienošana ieteikumu sarakstiem vai noņemšana no tiem

### <a name="for-new-trending-or-best-selling-lists"></a>Sarakstiem "Jaunas", "Populāras" vai "Vispirktākās"

1.  Pārejiet uz **Retail un Commerce** > **Preču ieteikumi** > **Ieteikumu parametri**.
1.  Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.
1.  Atlasiet sarakstu, kuram pievienot vai noņemt preces.
1.  Lai tabulai pievienotu preces, atlasiet **Pievienot rindu**. 
1.  Sadaļā Preces kolonna meklējiet preci pēc **Nosaukuma** vai **Preces numura.**

    ![Piemērs preces meklēšanai sarakstā Jauna prece.](./media/examplenewlistconfiguration1.png)

1.  Kolonnas rindas veidā atlasiet vienu no divām opcijām:
    -   **Iekļaut** — forsē preci uz saraksta priekšgalu
    -   **Izslēgt** — noņem preci no parādīšanās sarakstā
    
    ![Piemērs preces iekļaušanai vai izņemšanai no Jaunas preces saraksta.](./media/examplenewlistconfiguration2.png)

1.  Mainot **Rādīšanas secība**, tiks mainīta secība, kādā prece, kas atzīmēta ar **Iekļaut**, parādīsies sarakstā.
    - Ja divām precēm ir tāda pati vērtība **Rādīšanas secība**, šo divu rezultātu galīgā secība var atšķirties no tās, kas ir birojā.
1.  Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet **Noņemt**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Sarakstiem "Pircējiem patīk" vai "Bieži iegādāts kopā"

"Bieži iegādāts kopā" vai "Pircējiem patīk" sarakstu kontekstā mašīnmācība tiek izmantota, lai analizētu patērētāju pirkšanas paradumus un ieteiktu saistītās preces, kas parasti tiek iegādātas kopā, izveidojot unikālu sākuma preci. 
 
*Sākuma prece* ir prece, kurai vēlaties ģenerēt rezultātus. Manuāli pielāgotu ieteikumu sarakstu kontekstā jūs pievienojat vai noņemat šīs preces rezultātus. 

Veiciet tālāk minētās darbības, lai manuāli pievienotu vai noņemtu rezultātus sākuma precei.
1.  Atlasiet **Sākuma prece**. 
1.  Kolonnā **Prece** meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai sarakstā Bieži iegādāts kopā.](./media/exampleFBTlistconfiguration1.png)
1. Kolonnā **Rindas veids** atlasiet vienu no divām opcijām:
    - **Iekļaut** — forsē preci uz saraksta priekšgalu
    - **Izslēgt** — noņem preci no parādīšanās sarakstā     
![Piemērs preces iekļaušanai vai izslēgšanai no saraksta Bieži iegādāts kopā.](./media/exampleFBTlistconfiguration2.png)
1.  Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet Noņemt.


## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]