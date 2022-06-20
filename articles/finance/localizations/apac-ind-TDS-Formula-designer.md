---
title: TDS aprēķinu formulas veidotājs
description: Šajā rakstā sniegts piemērs tam, kā tiek aprēķināts ieturētais nodoklis avotā (TDS), pamatojoties uz formulu, kas noteikta katrai TDS nodokļa kodam TDS grupā, kas pievienota darbībai.
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
ms.openlocfilehash: 1196f7258c898a55f3f29ddce7457e6f527185d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889866"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS aprēķinu formulas veidotājs

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts piemērs tam, kā tiek aprēķināts ieturētais nodoklis avotā (TDS), pamatojoties uz formulu, kas noteikta katram TDS nodokļa kodam. TDS nodokļu kodi ir definēti TDS grupā, kas pievienota darījumam. Pirms TDS formulu izstrādāšanas izpildiet pamata iestatījumu, kas nepieciešams TDS, kā norādīts šajos soļos. 

- Iestatiet TDS komponenta grupas, izmantojot **Ieturēto nodokļu komponentu grupas** lapu. 
- Iestatiet TDS komponentus un pievienojiet TDS komponentu grupu TDS komponentiem, izmantojot **Ieturētā nodokļa komponentu** lapu. 
- Iestatiet TDS nodokļu kodus un pievienojiet TDS komponentus nodokļu kodiem, izmantojot **Ieturētā nodokļa kodu** lapu. 
- Iestatiet TDS nodokļu grupas, izmantojot **Ieturēto nodokļu grupas** lapu. Pēc tam pievienojiet TDS nodokļu kodus nodokļu grupai un definējiet formulu, izmantojot **Formulas veidotāja** lapu. 

**Parauga formula**

Šajā piemērā TDS grupa, Noma, ir pievienota pirkšanas rēķinam, kas izveidots kreditoram A. Rēķina summa ir $100 000. Skatiet šo tabulu, lai skatītu rēķina TDS aprēķinu.

| TDS grupa                                                   | TDS nodokļu kodi, kas pievienoti TDS grupai | Vērtība              | Apliekamais pamats (formulas veidotājs) | Aprēķina izteiksme (formulas veidotājs) | Pamatsumma | Aprēķinātā TDS summa |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Īre                                                         | TDS (TDS Komponents-TDS)                | 10%                | Bruto summa                      |                                            | 100,000      | 10,000                 |
| Piemaksa (TDS komponents-Piemaksa)                         | 10%                                     | Izņ. bruto summa | +TDS                              |                   10000                    | 1000        |                       |
| PE-Cess (TDS komponents-PE-Cess)                            | 2%                                      | Izņ. bruto summa | +TDS+Piemaksa                    |                   11000                    | 220         |                       |
| SHE Cess (TDS komponents-SHE Cess)                          | 1%                                      | Izņ. bruto summa | +TDS+Piemaksa                    |                   11000                    | 110         |                       |
| **Kopsumma** **TDS** **aprēķināts** **rēķinam** | **11,330**                               |                    |                                   |                                            |             |                       |

Dokumentu ieraksti tiek veidoti šādi.

| Konts           | Debetkarte  | Kredītkarte |
| ----------------- | ------ | ------ |
| Īre              | 100,000 |        |
| Kreditors A          |        | 100,000 |
| Kreditors A          | 11,330  |        |
| Maksājamais TDS       |        | 10,000  |
| Maksājamā piemaksa |        | 1000   |
| Maksājamais PE-Cess   |        | 220    |
| Maksājamais SHE Cess  |        | 110    |
