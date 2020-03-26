---
title: Izdevumu kvīšu apstrāde
description: Šajā tēmā ir sniegta informācija par kvīšu optiskās rakstzīmju atpazīšanas (OCR) apstrādi. Šis līdzeklis ir paredzēts lietotāja pieredzes uzlabošanai, veidojot izdevumu pārskatus programmā Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113690"
---
# <a name="public-preview-expense-receipt-processing"></a>Publiskais priekšskatījums: izdevumu saņemšanas apstrāde

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Izdevumu ieraksts ir uzlabots, ieviešot kvīšu optiskās rakstzīmju pazīšanas (OCR) apstrādi. Šis līdzeklis ir paredzēts lietotāja pieredzes uzlabošanai, veidojot izdevumu pārskatus.

## <a name="key-features"></a>Galvenie līdzekļi

- No kvītīm tiek izgūts tirgotāja nosaukums, datums un kopējā summa.
- Šis līdzeklis mēģina saskaņot nepievienotās kvītis ar nepievienotām izdevumu darbībām.
- Lietotāji var no kvītīm izveidot manuāli ievadītas izdevumu darbības.

## <a name="usage-examples"></a>Lietojuma piemēri

- **Automātiski pievienojiet kvītis, kas, veidojot izdevumu pārskatu, ietver kredītkartes darbības.**

    1. Atveriet darbvietu **Izdevumu pārvaldība**.
    2. Cilnē **Kvītis** pārbaudiet, vai pastāv nepievienotas kvītis. Kvītis varat augšupielādēt arī cilnē **Kvītis**.
    3. Cilnē **Izdevumi** pārbaudiet, vai pastāv nepievienoti izdevumi. Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.
    4. Atlasiet **Jauns izdevumu pārskats**. Ievērojiet, ka tagad, veidojot izdevumu pārskatu, var iekļaut arī izdevumus un kvītis. Ja pievienojat gan izdevumus, gan kvīti,, automātiski tiek aktivizēta kvīšu salīdzināšana ar izdevumiem.

- **Izveidojiet izdevumus vai saskaņojiet kvītī norādītos izdevumus.**

    1. Pievienojiet kvīti izdevumu pārskata cilnē **Kvītis**, atlasot **Pievienot kvītis**.
    2. Zem augšupielādētā kvīts attēla ievērojiet opcijas **Izveidot** un **Saskaņot**.

        - Atlasiet **Izveidot**, lai izveidotu manuāli ievadītu izdevumu darbību, un ievadiet vērtības, kas izgūtas no kvīts.
        - Ja atlasāt **Saskaņot**, sistēma mēģina saskaņot esošus izdevumus ar kvīti.

## <a name="installation"></a>Instalēšana

Šis līdzeklis darbojas kombinācijā ar līdzekli **Izdevumu pārskati jaunā izskatā**, tādējādi vienkāršojot izdevumu funkcionalitāti.

Lai izmantotu šīs uzlabotās izdevumu iespējas, instalējiet Microsoft Dynamics 365 Finance izdevumu pārvaldības pakalpojuma pievienojumprogrammu un ieslēdziet līdzekļus savā instancē. Jūs variet piekļūt pievienojumprogrammai no sava projekta pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).

1. Piesakieties LCS un atveriet vēlamo vidi.
2. Doties **Pilna detalizēta informācija**.
3. Atlasiet **Uzturēt**vai ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.
4. Atlasiet **Instalēt jaunu pievienojumprogrammu**.
5. Atlasiet **Izdevumu pārvaldības pakalpojumi**.
6. Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.
7. Atlasiet **Instalēt**.

Darbvietā **Līdzekļu pārvaldība** aktivizējiet tālāk norādītos līdzekļus.

- Izdevumu pārskati atkārtoti attēloti
- Automātiski saskaņot un izveidot izdevumus no kvīts

Ieslēdzot šos līdzekļus, notiek tālāk minētās darbības.

- Esošā darbvieta **Izdevumu pārvaldība** tiek aizstāta ar jauno darbvietu.
- Tiek pievienots jauns izvēlnes elements izdevumu lauku redzamībai.
- Jūs joprojām varat atvērt bijušo lapu **Izdevumu pārskati**, pārejot uz **Izdevumu pārvaldība > Mani izdevumi > Izdevumu pārskati**.
- Darbplūsmas un visi apstiprinājumi vēl aizvien novirza uz esošo izdevumu pārskatu lapu.
- Kvītis tiks apstrādātas, izmantojot Microsoft Azure Cognitive Services, un tiks izgūti un pievienoti metadati.
- Tiek pievienota opcija, kas ļauj izveidot izdevumu pārskatu, kurā iekļautas saskaņotās nepievienotās kvītis.
- Izdevumu pārskatiem pievienotā opcija ļauj izveidot izdevumu rindu no kvīts vai mēģina saskaņot esošu kvīti ar esošu izdevumu rindu.

Papildu informāciju par līdzekli izdevumu pārskati jaunā izskatā skatiet sadaļā [Izdevumu pārskati jaunā izskatā](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

**Vai Microsoft izmanto manus datus saviem modeļiem?**

Nē, Microsoft ir izveidojusi vispārīgu algoritmiskās mācīšanās modeli savam kvīšu apstrādes pakalpojumam. Šis modelis nav balstīts jūsu augšupielādētajam kvītīm.

**Kur šis līdzeklis ir pieejams un apstrādāts?**

Šobrīd tiek atbalstītas Amerikas Savienotās Valstis.

**Kur nonāk manas kvītis?**

Finance sazināsies ar Cognitive Services, lai izgūtu lauka datus. Cognitive Services saglabās kvīts kopiju līdz pat 24 stundām, kamēr tiek veikta apstrāde. Pēc apstrādes pabeigšanas Cognitive Services kvīti noņems. Kvīts joprojām tiek uzglabāta programmā Finance.

Papildinformāciju skatiet sadaļā [Izpratnes par kvītīm aktivizēšana, izmantojot veidlapu atpazinēja jaunās iespējas](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
