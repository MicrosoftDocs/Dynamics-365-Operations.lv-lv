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
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647899"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Ģenerējiet rēķina rindas, kad importējat kreditora rēķinus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā aprakstīta funkcionalitāte automātiskai rēķinu rindu ģenerēšana kreditoru rēķinos, kad tiek importēti rēķini.

Dažreiz kreditoru rēķinos ir ierobežota informācija, piemēram, informācija par saņēmēju un apakšsummas. Tomēr tie nesatur informāciju par rindas krājumiem. Kad jūs importējiet rēķinus, sistēma var automātiski ģenerēt rēķina rindas, pamatojoties uz informāciju par atbilstošo pirkšanas pasūtījumu.

Lai iespējotu automātisku rēķina rindu izveidi, veiciet šādus soļus.

1.  Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
2.  Cilnē **Kreditoru rēķinu automatizācija** sadaļā **Automātiska importēto rēķinu rindas izveide** iestatiet opciju **Automātiski izveidot rēķina rindas** uz **Jā**. 
4.  Laukā **Izvēlēties noklusējuma daudzumu automātiskai rēķinu rindu izveidei** atlasiet daudzumu, kas sistēmai jāizmanto, lai automātiski ģenerētu rēķina rindas:

    - **Pasūtītais daudzums** – Sistēma ģenerēs rindas no pirkšanas pasūtījuma rindām. Šī vērtība ir noklusējuma vērtība.
    - **Produktu ieejas plūsmas daudzums** – sistēma izmantos pirkšanas pasūtījumu numurus, lai atrastu atbilstošās produktu ieejas plūsmas. Pēc tam tā izmantos produktu ieejas plūsmas daudzumus, lai ģenerētu rēķina rindas.

## <a name="data-entity-changes"></a>Datu entītījas izmaiņas

Lai atbalstītu šajā tēmā aprakstīto funkcionalitāti, ir uzlabota **Kreditoru rēķina galvenes** datu entītija. Ir pievienoti trīs lauki:

- **HeaderOnlyImport** - šim laukam ir jābūt iestatītam uz **Jā**, lai sistēma ģenerētu rēķinu virsrakstu rindas.
- **PurchIdRange** – pirkšanas pasūtījumu numuru saraksts. Rēķinu numuri var būt diapazons, piemēram, **INV0001..INV0009** (kur divi punktpunkti atdala diapazona sākumu un beigas) vai atsevišķas vērtības, piemēram, **INV0001, INV0003, INV0006**. Visiem pirkšanas pasūtījumiem ir jāpieder pie viena kreditora konta rēķina galvenē. Pretējā gadījumā tiks parādīts šāds kļūdas ziņojums: "Neizdevās ģenerēt rēķina rindas. Pirkšanas pasūtījumiem ir atšķirīgi kreditora konti."
- **PackingslipRange** – produktu ieejas plūsmu numuru saraksts. Kreditora rēķina rindas var izveidot no produktu ieejas plūsmas. Tomēr produktu ieejas plūsmu numuri parasti nav iekļauti kreditora rēķinos. Šajā laukā ievadiet tikai produktu ieejas plūsmas numurus, ja jūs skaidri varat identificēt, kuras produktu ieejas plūsmas ir kurām specifiskiem rēķiniem. Rēķina rindas var izveidot no produktu ieejas plūsmas. Un, ja tiek izmantots šis lauks, iestatījums **Izvēlēties noklusējuma daudzumu automātiskai rēķinu rindu izveidei** lapā **Kreditoru parametri** tiek ignorēts. 

**Ierobežojums**: ja ievadīsiet vairākus produktu ieejas plūsmas numurus, tiks izveidoti vairāki nenokārtoti kreditora rēķini ar vienādu rēķina numuru. Pirms rēķina turpmākas apstrādes tās ir jākonsolidē manuāli. Turpmākajos laidienos mēs plānojam aktivizēt sistēmu automātiskai rēķinu konsolidēšanai, lai ierobežojums tiktu noņemts.

Visām preču ieejas plūsmām ir jāpieder pie viena kreditora konta rēķina galvenē.

## <a name="result"></a>Rezultāts

Ja sistēma veiksmīgi ģenerē rindas, kreditora rēķina automatizācijas vēsturē tiek reģistrēts šāds ziņojums: "Automātiski izveidot rēķina rindas: Izdevās."

Ja sistēma neģenerē rindas, tiek reģistrēts šāds kļūdas ziņojums: "Automātiski izveidot rēķina rindas: Neizdevās."
