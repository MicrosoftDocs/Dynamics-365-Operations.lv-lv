---
title: ER funkciju saraksts datu vākšanas kategorijā
description: Šajā tēmā ir sniegta informācija par datu apkopošanas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686297"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="b6bf6-103">ER funkciju saraksts datu vākšanas kategorijā</span><span class="sxs-lookup"><span data-stu-id="b6bf6-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6bf6-104">Elektronisko pārskatu (ER) datu apkopošanas funkcijas tiek izmantotas, lai veiktu skaitīšanu un summēšanu ER formātā, kas tiek palaists, pamatojoties uz datiem par izvadi, kas jau ir ģenerēti **teksta** vai **XML** formātā.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="b6bf6-105">Šī pieeja tiek izmantota, lai palīdzētu uzlabot izpildīto ER formāta veiktspēju, lai ģenerētos dokumentos ievadītu kopsummu vērtības, un citiem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="b6bf6-106">Šajā tēmā ir sniegts šo funkciju kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="b6bf6-107">Atbalstīto funkciju saraksts</span><span class="sxs-lookup"><span data-stu-id="b6bf6-107">List of supported functions</span></span>

| <span data-ttu-id="b6bf6-108">Funkcija</span><span class="sxs-lookup"><span data-stu-id="b6bf6-108">Function</span></span> | <span data-ttu-id="b6bf6-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b6bf6-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="b6bf6-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="b6bf6-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="b6bf6-111">Šī funkcija atgriež vērtību *Ierakstu saraksts*, kurā ir to vērtību saraksts, ko atgrieza formāta elementu rekvizīts **Ievāktā datu atslēgas vērtība** un kas tika savākts, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā, un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b6bf6-112">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b6bf6-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="b6bf6-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="b6bf6-114">Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b6bf6-115">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b6bf6-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="b6bf6-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="b6bf6-117">Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b6bf6-118">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b6bf6-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="b6bf6-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="b6bf6-120">Šī funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā ER formāta elementa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="b6bf6-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="b6bf6-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="b6bf6-122">Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b6bf6-123">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b6bf6-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="b6bf6-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="b6bf6-125">Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b6bf6-126">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6bf6-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b6bf6-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b6bf6-127">Additional resources</span></span>

[<span data-ttu-id="b6bf6-128">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="b6bf6-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b6bf6-129">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="b6bf6-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="b6bf6-130">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="b6bf6-130">Electronic reporting formula language</span></span>](er-formula-language.md)
