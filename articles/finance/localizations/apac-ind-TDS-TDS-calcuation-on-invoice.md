---
title: TDS aprēķins rēķinos
description: Šajā rakstā sniegta atsauce darbībām, kur ieturētais nodoklis avotā (TDS) tiek aprēķināts rēķina līmenī.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855368"
---
# <a name="tds-calculation-on-invoices"></a>TDS aprēķins rēķinos

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegta atsauce darbībām, kur ieturētais nodoklis avotā (TDS) tiek aprēķināts rēķina līmenī.

| Sērijas numurs | Darījuma veids                                 | Transakciju summa | Lapas nosaukums un atlases ceļš                                 | Konta tips un korespondējošā konta tips                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Pirkums, kas veikts no kreditora/reģistrācijas izdevumiem   | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu apstiprināšanas žurnāla lapa (Kreditori > Rēķini > Rēķinu apstiprināšana), Rēķinu žurnāla lapa (Parādi kreditoriem > Rēķini > Rēķinu žurnāls) | Virsgrāmata (dr.), kreditors (kr.)  Ieturētais nodoklis kreditora virsgrāmatas kombinācijai tiek aprēķināts tikai tad, ja Virsgrāmatas konta grāmatošanas tips ir **Pirkšana**  **skaidrā naudā**. |
| 2.            | Pirkums, kas veikts no debitora/reģistrācijas izdevumiem | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Virsgrāmata (dr.), debitors (kr.)                                 |
| 3.            | Pamatlīdzekļa pirkšana no kreditora              | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu reģistrācijas žurnāla lapa (Kreditori > Rēķini > Rēķinu reģistrācija), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Pamatlīdzekļu (Dr.) kreditors (Kr.)                             |
| 4.            | Pamatlīdzekļa pirkšana no debitora            | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Pamatlīdzekļu (Dr.) debitora (Kr.)                           |
| 5.            | Pirkšanas rēķins (maksājamais TDS)                  |                    | Pirkšanas pasūtījuma lapa (Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi) |                                                              |
| 6.            | Pārdošanas rēķins (saņemamie TDS)                  |                    | Pārdošanas pasūtījumu lapa (Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi), Brīva teksta rēķina lapa (Debitori > Rēķini > Visi brīvā teksta rēķini) |                                                              |
