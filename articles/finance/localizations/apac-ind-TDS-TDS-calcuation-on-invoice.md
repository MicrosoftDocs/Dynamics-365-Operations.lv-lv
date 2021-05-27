---
title: TDS aprēķins rēķinos
description: Šajā tēmā sniegta atsauce darījumiem, kur No kopējās ienākumu summas atskaitītais nodoklis (TDS) tiek aprēķināts rēķina līmenī.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023422"
---
# <a name="tds-calculation-on-invoices"></a>TDS aprēķins rēķinos

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta atsauce darījumiem, kur No kopējās ienākumu summas atskaitītais nodoklis (TDS) tiek aprēķināts rēķina līmenī.

| Sērijas numurs | Darījuma veids                                 | Transakciju summa | Lapas nosaukums un atlases ceļš                                 | Konta tips un korespondējošā konta tips                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Pirkums, kas veikts no kreditora/reģistrācijas izdevumiem   | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu apstiprināšanas žurnāla lapa (Kreditori > Rēķini > Rēķinu apstiprināšana), Rēķinu žurnāla lapa (Parādi kreditoriem > Rēķini > Rēķinu žurnāls) | Virsgrāmata (dr.), kreditors (kr.)  Ieturētais nodoklis kreditora virsgrāmatas kombinācijai tiek aprēķināts tikai tad, ja Virsgrāmatas konta grāmatošanas tips ir **Pirkšana**  **skaidrā naudā**. |
| 2.            | Pirkums, kas veikts no debitora/reģistrācijas izdevumiem | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Virsgrāmata (dr.), debitors (kr.)                                 |
| 3.            | Pamatlīdzekļa pirkšana no kreditora              | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu reģistrācijas žurnāla lapa (Kreditori > Rēķini > Rēķinu reģistrācija), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Pamatlīdzekļu (Dr.) kreditors (Kr.)                             |
| 4.            | Pamatlīdzekļa pirkšana no debitora            | Debetkarte vai kredītkarte  | Virsgrāmatas žurnālu lapa (Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli), Rēķinu žurnāla lapa (Kreditori > Rēķini > Rēķinu žurnāls) | Pamatlīdzekļu (Dr.) debitora (Kr.)                           |
| 5.            | Pirkšanas rēķins (maksājamais TDS)                  |                    | Pirkšanas pasūtījuma lapa (Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi) |                                                              |
| 6.            | Pārdošanas rēķins (saņemamie TDS)                  |                    | Pārdošanas pasūtījumu lapa (Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi), Brīva teksta rēķina lapa (Debitori > Rēķini > Visi brīvā teksta rēķini) |                                                              |
