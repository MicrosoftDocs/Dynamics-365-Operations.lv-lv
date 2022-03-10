---
title: Ģenerējiet rēķina rindas, kad importējat kreditora rēķinus
description: Šajā tēmā aprakstīta funkcionalitāte automātiskai rēķinu rindu ģenerēšana kreditoru rēķinos, kad tiek importēti rēķini.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e452bda02c814b78c4bb48140b07f0113ab4a571
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358318"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Ģenerējiet rēķina rindas, kad importējat kreditora rēķinus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā aprakstīta funkcionalitāte automātiskai rēķinu rindu ģenerēšana kreditoru rēķinos, kad tiek importēti rēķini.

Dažreiz kreditoru rēķinos ir ierobežota informācija, piemēram, informācija par saņēmēju un apakšsummas. Tomēr tie nesatur informāciju par rindas krājumiem. Importējot rēķinus, rēķina rindas tiks ģenerētas automātiski, pamatojoties uz informāciju par atbilstošo pirkšanas pasūtījumu.

Lai iespējotu automātisku rēķina rindu izveidi, veiciet šādus soļus.

1.  Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
2.  Cilnē **Kreditoru rēķinu automatizācija** sadaļā **Automātiska importēto rēķinu rindas izveide** iestatiet opciju **Automātiski izveidot rēķina rindas** uz **Jā**. 
4.  Laukā **Izvēlēties noklusējuma daudzumu automātiskai rēķina rindu izveidei** atlasiet daudzumu, kas jāizmanto, lai automātiski ģenerētu rēķina rindas:

    - **Pasūtītais daudzums** – rindas tiks ģenerētas no pirkšanas pasūtījuma rindām. Šī vērtība ir noklusējuma vērtība.
    - **Produktu ieejas plūsmas daudzums** – pirkšanas pasūtījuma numurs tiks izmantots, lai atrastu atbilstošās produktu ieejas plūsmas. Pēc tam tā izmantos produktu ieejas plūsmas daudzumus, lai ģenerētu rēķina rindas.

## <a name="data-entity-changes"></a>Datu entītījas izmaiņas

Lai atbalstītu šajā tēmā aprakstīto funkcionalitāti, ir uzlabota **Kreditoru rēķina galvenes** datu entītija. Ir pievienoti trīs lauki:

- **HeaderOnlyImport** – šis lauks ir jāiestata uz **Jā**, lai ģenerētu rindas rēķinu virsrakstiem.
- **PurchIdRange** – pirkšanas pasūtījumu numuru saraksts. Rēķinu numuri var būt diapazons, piemēram, **INV0001..INV0009** (kur divi punktpunkti atdala diapazona sākumu un beigas) vai atsevišķas vērtības, piemēram, **INV0001, INV0003, INV0006**. Visiem pirkšanas pasūtījumiem ir jāpieder pie viena kreditora konta rēķina galvenē. Pretējā gadījumā tiks parādīts šāds kļūdas ziņojums: "Neizdevās ģenerēt rēķina rindas. Pirkšanas pasūtījumiem ir atšķirīgi kreditora konti."
- **PackingslipRange** – produktu ieejas plūsmu numuru saraksts. Kreditora rēķina rindas var izveidot no produktu ieejas plūsmas. Tomēr produktu ieejas plūsmu numuri parasti nav iekļauti kreditora rēķinos. Šajā laukā ievadiet tikai produktu ieejas plūsmas numurus, ja jūs skaidri varat identificēt, kuras produktu ieejas plūsmas ir kurām specifiskiem rēķiniem. Rēķina rindas var izveidot no produktu ieejas plūsmas. Ja šis lauks tiek izmantots, lapas Kreditoru parametri **lauka Izvēlēties noklusējuma daudzumu automātiskās rēķina rindu izveides** lauka **Izvēlēties noklusējuma daudzumu iestatījums** tiek ignorēts. 

**Ierobežojums**: ja ievadīsiet vairākus produktu ieejas plūsmas numurus, tiks izveidoti vairāki nenokārtoti kreditora rēķini ar vienādu rēķina numuru. Pirms rēķina turpmākas apstrādes tās ir jākonsolidē manuāli. Turpmākajos laidienos mēs plānojam automātiski konsolidēt rēķinus, tāpēc ierobežojums tiks noņemts.

Visām preču ieejas plūsmām ir jāpieder pie viena kreditora konta rēķina galvenē.

## <a name="result"></a>Rezultāts

Ja rindas ir veiksmīgi ģenerētas, kreditora rēķinu automatizācijas vēsturē tiek reģistrēts šāds ziņojums: "Automātiski izveidot rēķina rindas: izdevās."

Ja rindas netiek ģenerētas, tiek reģistrēts šāds kļūdas ziņojums: "Automātiski izveidot rēķina rindas: neizdevās."
