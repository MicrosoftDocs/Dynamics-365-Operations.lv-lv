---
title: Galvenes modulis
description: Šajā tēmā aplūkoti galvenes moduļi un aprakstīta lapu galveņu izveide risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: afdc12230ebad3d5db59c384b2f1066d2c7929339f282ed4880ff967b1fd2d8b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712794"
---
# <a name="header-module"></a>Galvenes modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti galvenes moduļi un aprakstīta lapu galveņu izveide risinājumā Microsoft Dynamics 365 Commerce.

Pakalpojumā Dynamics 365 Commerce, lapas galvene ir konfigurēta kā lapas fragments, kas ietver galveni, promo reklāmkarogu un sīkfailu piekrišanas moduļus. 

Galvenes modulī ir iekļauts vietnes logotips, saites uz navigācijas hierarhiju, saites uz citām lapām vietnē, groza ikonas modulis, vēlmju simbols, pierakstīšanās opcijas un meklēšanas josla. Galvenes modulis tiek automātiski optimizēts ierīcei, izmantojot kuru, vietne tiek skatīta (citiem vārdiem sakot, darbvirsmas ierīcei vai mobilajai ierīcei). Piemēram, mobilajā ierīcē navigācijas josla ir sakļauta pogā **Izvēlne** (kas dažreiz tiek saukta par *hamburgeru izvēlni*).

Attēlā zemāk redzams galvenes moduļa piemērs sākumlapā.

![Galvenes moduļa piemērs.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Galvenes moduļa rekvizīti

Galvenes modulis atbalsta šādus rekvizītus: **Logotipa attēls**, **Logotipa saite** un **Mana konta saites**. 

Rekvizīti **Logotipa attēls** un **Logotipa saites** tiek izmantoti, lai definētu logotipu lapā. Plašāku informāciju skatiet sadaļā [Logotipa pievienošana](add-logo.md). 

Rekvizīts **Mana konta saites** var tikt izmantots, lai definētu konta lapas, kuras vietnes īpašnieks vēlas parādīt tiešās saites virsrakstā.

## <a name="modules-that-are-available-within-a-header-module"></a>Galvenes modulī pieejamie moduļi

Šādus moduļus var izmantot galvenes modulī.

- **Navigācijas izvēlne** – navigācijas izvēlnē ir atspoguļota kanāla navigācijas hierarhija un citas statiskās navigācijas saites. Papildinformāciju skatiet šeit: [Navigācijas izvēlnes modulis](nav-menu-module.md).

- **Meklēšana** — meklēšanas modulis ļauj lietotājiem ievadīt meklēšanas nosacījumus preču meklēšanai. Noklusējuma meklēšanas lapas URL un meklēšanas vaicājuma parametri ir jānorāda sadaļā **Vietnes iestatījumi \> Paplašinājumi**. Meklēšanas modulim ir rekvizīti, kas ļauj izlaist meklēšanas pogu vai etiķeti pēc nepieciešamības. Meklēšanas modulis atbalsta arī automātiskās ieteikšanas opcijas, piemēram, preci, atslēgvārdu un kategoriju meklēšanas rezultātus.

- **Groza ikona** — groza ikonu modulis attēlo groza ikonu, kas parāda preču skaitu grozā jebkurā laikā. Plašāku informāciju skatiet [Groza ikonas modulis](cart-icon-module.md).

- **Vietas atlasītājs** — vietas atlasītāja modulis ļauj lietotājiem pārlūkot dažādas iepriekšdefinētas vietas, ņemot vērā tirgu, reģionus un lokalizāciju. Plašāku informāciju skatiet sadaļā [Vietas atlasītāja modulis](site-selector.md).

- **Veikalu atlasītājs** — veikalu atlasītāja moduli var iekļaut galvenes moduļa veikalu atlasītāja slotā. Tas ļauj lietotājiem pārlūkot un atrast tuvumā esošos veikalus. Lietotāji var arī norādīt vēlamo veikalu. Šis veikals pēc tam būs redzams galvenē. Kad veikalu atlasītāja modulis ir iekļauts galvenes modulī, tā rekvizītam **Režīms** jābūt iestatītam uz **Atrast veikalus**. Plašāku informāciju skatiet sadaļā [Veikalu atlasītāja modulis](store-selector.md).

> [!NOTE]
> - Atbalsts groza ikonas moduļa izmantošanai galvenes moduļos ir pieejams kā Dynamics 365 Commerce versija 10.0.11 laidienā.
> - Atbalsts vietnes atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams kā Dynamics 365 Commerce versija 10.0.14 laidienā.
> - Atbalsts veikala atlasītāja moduļa izmantošanai galvenes moduļos ir pieejams kā Dynamics 365 Commerce versija 10.0.15 laidienā.

## <a name="header-module-in-the-adventure-works-theme"></a>Virsraksta modulis Adventure Works tēmā

Adventure Works tēmā virsraksta modulis atbalsta rekvizītu **Mobilais logotips**. Šis rekvizīts iespējo logotipa norādīšanu mobilajām skatījumu vietām. Rekvizīts **Mobilais logotips** ir pieejams kā moduļa definīcijas paplašinājums.

> [!IMPORTANT]
> Adventure Works tēma ir pieejama Dynamics 365 Commerce versijas 10.0.20 laidienā.

## <a name="create-a-header-fragment-for-a-page"></a>Lapas galvenes fragmenta izveide

Lai izveidotu galvenes fragmentu, veiciet šādas darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jauns fragments** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Noklusējuma konteiners** un pēc tam rekvizītu rūtī pa labi iestatiet rekvizītu **Platums** uz **Aizpildīt ekrānu**.
1. Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduļus **Sīkdatņu piekrišana**, **Galvene** un **Veicināšanas reklāmkarogs** un pēc tam atlasiet **Labi**.
1. Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.
1. Dialoglodziņā **Ziņojums** pievienojiet tekstu un saites reklāmas saturam un pēc tam atlasiet **Labi**.
1. Moduļa **Sīkdatņu piekrišana** rekvizītu rūtī pievienojiet un konfigurējiet tekstu un saiti uz vietnes konfidencialitātes lapu.
1. Galvenes moduļa slotā **Navigācijas izvēlne** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Navigācijas izvēlne** un pēc tam atlasiet **Labi**.
1. Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Navigācijas izvēlnes avots** atlasiet **Mazumtirdzniecības serveris**.
1. Navigācijas izvēlnes moduļa rekvizītu rūts sadaļā **Statiski izvēlnes vienumi** atlasiet **Pievienot izvēlnes vienumu**, un pēc tam atlasiet **Izvēlnes elements**. 
1. Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma teksts** ievadiet "Kontaktpersona."
1. Dialoglodziņā **Izvēlnes vienums** sadaļā **Izvēlnes vienuma saites mērķis** atlasiet **Pievienot saiti**.
1. Dialoglodziņā **Pievienot saiti** atlasiet URL saites "Kontaktpersonas" lapai un pēc tam atlasiet **Labi**.  
1. Dialoglodziņā **Izvēlnes vienums** atlasiet **Labi**.
1. Galvenes moduļa slotā **Meklēt** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēt** un pēc tam atlasiet **Labi**.
1. Meklēšanas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības.
1. Galvenes moduļa slotā **Groza ikona** slotā atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Groza ikona** un pēc tam atlasiet **Labi**.
1. Groza ikonas moduļa rekvizītu rūtī konfigurējiet rekvizītus pēc vajadzības. Ja vēlaties, lai groza ikona parāda groza kopsavilkumu (to sauc arī par mini grozu), kad lietotāji uz to norāda, atlasiet **Rādīt mini grozu**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.

1. Moduļa **Noklusējuma lapa** slotā **Galvene** pievienojiet jūsu izveidoto kājenes fragmentu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Akcijas reklāmkaroga modulis](add-alert.md)

[Navigācijas izvēlnas modulis](nav-menu-module.md) 

[Piekrišana sīkfailiem](cookie-consent-module.md)

[Kājenes modulis](author-footer-module.md)

[Vietņu atlasītāja modulis](site-selector.md)

[Veikalu atlasītāja modulis](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
