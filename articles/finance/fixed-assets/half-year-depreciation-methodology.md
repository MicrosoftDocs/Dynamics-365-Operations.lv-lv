---
title: Pusgada nolietojuma konvencijas metodika
description: Šajā rakstā ir aprakstīta metode, kuru pamatlīdzekļi izmanto nolietojuma aprēķināšanai, lietojot pusgada konvenciju, kas aprēķina sešus nolietojuma mēnešus pamatlīdzekļa pirmā un pēdējā lietošanas gada laikā.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879600"
---
# <a name="half-year-depreciation-convention-methodology"></a>Pusgada nolietojuma konvencijas metodika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīta metode, kas tiek lietota pamatlīdzekļos nolietojuma aprēķinam, lietojot pusgada konvenciju. Pusgada konvencija aprēķina sešu mēnešu nolietojumu līdzekļa pirmajā un pēdējā ekspluatācijas gadā. Papildinformāciju par nolietojuma konvencijām skatiet rakstā [Nolietojuma metodes un konvencijas](Fixed-asset-depreciation-conventions.md). 

Izmantojot sešu mēnešu nolietojuma konvenciju, sistēma izmanto iegādes gadu vai gadu, kad līdzeklis tika nodots ekspluatācijā, pēc tam aprēķina piecu gadu nolietojumu sākot no šī gada un pēc tam pieskaita sešus mēnešus. Lai ilustrētu šo procesu, apsveriet līdzekli, kas tika iegādāts par cenu 50 000, un nodots ekspluatācijā 2020. gada aprīlī. Pieņemiet arī, ka līdzeklim ir piecu gadu lietošanas ilgums.

Pirmais ekspluatācijas gads noslēgsies 2020. gada decembrī, kas nozīmē, ka līdzekļa piecu gadu ekspluatācijas termiņš beigsies 2024. gada decembrī. Pusgada nolietojuma konvencija pamatlīdzekļa ekspluatācijas laikam pievienos sešus mēnešus, kas nozīmē, ka tā lietošanas laiks beigsies 2025. gada jūnijā. 

> Gada nolietojums 50 000/5 = 10 000 mēneša nolietojums 10 000/12 = 833,33 <br>
> Pirmā gada nolietojums 10 000/2 = 5 000 un nākamā mēneša nolietojums 5 000/9 = 555,56

   [![Nolietojuma grafiks pusgada nolietojuma konvencijai.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Paplašinātie nolietojuma periodi, kas pievienoti ar pusgada konvenciju, nodrošina precīzāku nolietojuma sadalījumu. Sešu mēnešu konvencija labāk atspoguļo nolietojuma izdevumus, kas ir noderīgi pārskatu sniegšanai peļņas un zaudējumu pārskatā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
