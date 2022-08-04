---
title: Kataloga izdošanas modulis
description: Šajā rakstā ir apskatīti kataloga izdošanas moduļi un aprakstīts, kā pievienot tos Microsoft Dynamics 365 Commerce uzņēmumu-biznesam (B2B) e-komercijas vietnēm.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136930"
---
# <a name="catalog-picker-module"></a>Kataloga izdošanas modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti kataloga izdošanas moduļi un aprakstīts, kā pievienot tos Microsoft Dynamics 365 Commerce uzņēmumu-biznesam (B2B) e-komercijas vietnēm.

Kataloga izdošanas modulis ir speciāls konteiners, kas tiek izmantots visu preču katalogu sarakstam, kas B2B vietas lietotājiem ir pieejami iepirkšanās laikā. Pašlaik vairāki katalogi tiek atbalstīti tikai B2B vietām.

Šajā attēlā parādīts kataloga izdošanas moduļa piemērs.

![Piemērs kataloga izdošanas modulim, kurā ir uzskaitīti trīs preču katalogi.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Pievienot kataloga atlasītāja moduli jūsu vietnei

Lai pievienotu kataloga izdošanas moduli jūsu vietnei Commerce Site Builder, sekojiet šiem soļiem.

### <a name="create-a-catalog-picker-page"></a>Izveidot kataloga izdošanas lapu

Vispirms izveidojiet kataloga izdošanas lapu.

1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā Izveidot **jaunu lapas dialoglodziņu** ar lapas nosaukumu **ievadiet** **Kataloga uztvērēju**.
1. Sadaļā **Lapas URL** ievadiet lapas URL un pēc tam atlasiet **Tālāk**.

    ![Izveidojiet jaunu lapas dialoglodziņu.](./media/Create-catalog-picker-page.png)

1. Zem **Izvēlēties veidni**, atlasiet Vispārējs **saturs un** pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** Elastīgs **izkārtojums** un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**.
1. Sadaļā **Kataloga izvēle** atlasiet Galvenais **slots**, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.

    ![Pievieno moduli galvenajam slotam zem Kataloga uztvērējs.](./media/Author-web-page-catalog-picker-1.png)

1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Atlasiet konteinera **slotu**, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet kataloga izvēles **moduli un** pēc tam atlasiet **Labi**.
1. Kataloga atlasītāja **rekvizītu** rūts sadaļā **Virsraksts** **atlasiet** Katalogi un pēc tam ievadiet kataloga atlasītāja lapas virsrakstu.
1. Sadaļā **Virsraksta līmenis** atlasiet virsraksta līmeni un pēc tam atlasiet **Labi**.
1. Zem **bagātinātā** teksta ievadiet tekstu, kas būs redzams kataloga izdošanas lapas augšpusē.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

### <a name="add-a-link-on-your-account-page"></a>Saites pievienošana jūsu konta lapai

Pēc tam sava konta lapā pievienojiet atsauci kataloga atlasītāja **lapai**.

1. Dodieties **uz** Lapas, atrodiet un atlasiet savas vietnes lapu **Mans konts** un pēc tam atlasiet **Rediģēt**.
1. Zem lapas **galvenā** slota atlasiet konta vispārējo elementa **slotu**. 
1. Konta vispārējā **elementa rekvizītu rūtī** sadaļā Saites atlasiet **Pievienot** darbības **saiti un** pēc tam atlasiet Darbība **saiti**.
1. Dialoglodziņā Darbības **saite** zem saites teksta **ievadiet** saites tekstu saitei uz kataloga izdošanas lapu.
1. Sadaļā **Saites mērķis** atlasiet **Pievienot saiti**.
1. Dialoglodziņā Pievienot **saiti atlasiet** Pielāgots lapu **un pēc** tam atlasiet **Tālāk**.
1. Sadaļā **Nosaukums** atlasiet kataloga atlasītāja lapu, atlasiet Lietot **un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Šajā attēlā parādīts kontu lapas piemērs ar atsauci uz kataloga lapu.

![Mana kontu lapa ar saiti uz katalogu.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Pievienot saiti no virsraksta

Beigās pievienojiet saiti no jūsu vietnes virsraksta saviem katalogiem.

1. Dodieties **uz fragmentiem**, atrodiet un atlasiet vietnes virsraksta fragmentu un pēc tam atlasiet **Rediģēt**.
1. Atlasiet slotu **Galvene**. 
1. Virsraksta rekvizītu **rūts** sadaļā Manas konta **saites atlasiet** Pievienot darbības **saiti un** pēc tam atlasiet Darbības **saite**.
1. Dialoglodziņā Darbības **saite** zem saites teksta **ievadiet** saites tekstu saitei uz kataloga izdošanas lapu.
1. Sadaļā **Saites mērķis** atlasiet **Pievienot saiti**.
1. Dialoglodziņā Pievienot **saiti atlasiet** Pielāgots lapu **un pēc** tam atlasiet **Tālāk**.
1. Sadaļā **Nosaukums** atlasiet kataloga atlasītāja lapu, atlasiet Lietot **un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu galvenes fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

Šajā attēlā parādīts e-komercijas vietnes virsraksta piemērs ar saiti uz B2B katalogu.

![E-pasta vietnes virsraksts ar nolaižamo saiti uz katalogu.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Papildu resursi 

[Commerce katalogu izveide B2B vietnēm](catalogs-b2b-sites.md)

[Commerce katalogu paplašināmības ietekme B2B pielāgojumiem](catalogs-b2b-sites-dev.md)

[Bieži uzdotie jautājumi par Commerce katalogiem B2B vietnēm](catalogs-b2b-sites-FAQ.md)

[Konta pārvaldības lapas un moduļi](account-management.md)

[Galvenes modulis](author-header-module.md)
