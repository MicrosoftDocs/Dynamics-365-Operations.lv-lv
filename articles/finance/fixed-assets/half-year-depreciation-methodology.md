---
title: Pusgada nolietojuma konvencijas metodika
description: Šajā tēmā aprakstīta metode, ko pamatlīdzekļi izmanto nolietojuma aprēķināšanai, izmantojot pusgada konvenciju, kas aprēķina sešu mēnešu nolietojumu pamatlīdzekļa pirmā un pēdējā ekspluatācijas gada laikā.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445451"
---
# <a name="half-year-depreciation-convention-methodology"></a>Pusgada nolietojuma konvencijas metodika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu, izmantojot pusgada konvenciju. Pusgada konvencija aprēķina sešu mēnešu nolietojumu līdzekļa pirmajā un pēdējā ekspluatācijas gadā. Papildinformāciju par nolietojuma konvencijām skatiet rakstā [Nolietojuma metodes un konvencijas](Fixed-asset-depreciation-conventions.md). 

Izmantojot sešu mēnešu nolietojuma konvenciju, sistēma izmanto iegādes gadu vai gadu, kad līdzeklis tika nodots ekspluatācijā, pēc tam aprēķina piecu gadu nolietojumu sākot no šī gada un pēc tam pieskaita sešus mēnešus. Lai ilustrētu šo procesu, apsveriet līdzekli, kas tika iegādāts par cenu 50 000, un nodots ekspluatācijā 2020. gada aprīlī. Pieņemiet arī, ka līdzeklim ir piecu gadu lietošanas ilgums.

Pirmais ekspluatācijas gads noslēgsies 2020. gada decembrī, kas nozīmē, ka līdzekļa piecu gadu ekspluatācijas termiņš beigsies 2024. gada decembrī. Pusgada nolietojuma konvencija pamatlīdzekļa ekspluatācijas laikam pievienos sešus mēnešus, kas nozīmē, ka tā lietošanas laiks beigsies 2025. gada jūnijā. 

> Gada nolietojums 50 000/5 = 10 000 mēneša nolietojums 10 000/12 = 833,33 <br>
> Pirmā gada nolietojums 10 000/2 = 5 000 un nākamā mēneša nolietojums 5 000/9 = 555,56

   [![Nolietojuma grafiks pusgada nolietojuma konvencijai](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Paplašinātie nolietojuma periodi, kas pievienoti ar pusgada konvenciju, nodrošina precīzāku nolietojuma sadalījumu. Sešu mēnešu konvencija labāk atspoguļo nolietojuma izdevumus, kas ir noderīgi pārskatu sniegšanai peļņas un zaudējumu pārskatā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]