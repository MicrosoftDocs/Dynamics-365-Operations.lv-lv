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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 6ec4c3a0bd86e15ee015fc2e2c49c92b035243b6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009297"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="60320-103">Pusgada nolietojuma konvencijas metodika</span><span class="sxs-lookup"><span data-stu-id="60320-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="60320-104">Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu, izmantojot pusgada konvenciju.</span><span class="sxs-lookup"><span data-stu-id="60320-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="60320-105">Pusgada konvencija aprēķina sešu mēnešu nolietojumu līdzekļa pirmajā un pēdējā ekspluatācijas gadā.</span><span class="sxs-lookup"><span data-stu-id="60320-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="60320-106">Papildinformāciju par nolietojuma konvencijām skatiet rakstā [Nolietojuma metodes un konvencijas](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="60320-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="60320-107">Izmantojot sešu mēnešu nolietojuma konvenciju, sistēma izmanto iegādes gadu vai gadu, kad līdzeklis tika nodots ekspluatācijā, pēc tam aprēķina piecu gadu nolietojumu sākot no šī gada un pēc tam pieskaita sešus mēnešus.</span><span class="sxs-lookup"><span data-stu-id="60320-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="60320-108">Lai ilustrētu šo procesu, apsveriet līdzekli, kas tika iegādāts par cenu 50 000, un nodots ekspluatācijā 2020. gada aprīlī.</span><span class="sxs-lookup"><span data-stu-id="60320-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="60320-109">Pieņemiet arī, ka līdzeklim ir piecu gadu lietošanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="60320-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="60320-110">Pirmais ekspluatācijas gads noslēgsies 2020. gada decembrī, kas nozīmē, ka līdzekļa piecu gadu ekspluatācijas termiņš beigsies 2024. gada decembrī.</span><span class="sxs-lookup"><span data-stu-id="60320-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="60320-111">Pusgada nolietojuma konvencija pamatlīdzekļa ekspluatācijas laikam pievienos sešus mēnešus, kas nozīmē, ka tā lietošanas laiks beigsies 2025. gada jūnijā.</span><span class="sxs-lookup"><span data-stu-id="60320-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="60320-112">Gada nolietojums 50 000/5 = 10 000 mēneša nolietojums 10 000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="60320-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="60320-113">Pirmā gada nolietojums 10 000/2 = 5 000 un nākamā mēneša nolietojums 5 000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="60320-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="60320-114">[![Nolietojuma grafiks pusgada nolietojuma konvencijai](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="60320-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="60320-115">Paplašinātie nolietojuma periodi, kas pievienoti ar pusgada konvenciju, nodrošina precīzāku nolietojuma sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="60320-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="60320-116">Sešu mēnešu konvencija labāk atspoguļo nolietojuma izdevumus, kas ir noderīgi pārskatu sniegšanai peļņas un zaudējumu pārskatā.</span><span class="sxs-lookup"><span data-stu-id="60320-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
