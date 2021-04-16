---
title: ER funkciju saraksts datu vākšanas kategorijā
description: Šajā tēmā ir sniegta informācija par datu apkopošanas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748067"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="765aa-103">ER funkciju saraksts datu vākšanas kategorijā</span><span class="sxs-lookup"><span data-stu-id="765aa-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="765aa-104">Elektronisko pārskatu (ER) datu apkopošanas funkcijas tiek izmantotas, lai veiktu skaitīšanu un summēšanu ER formātā, kas tiek palaists, pamatojoties uz datiem par izvadi, kas jau ir ģenerēti **teksta** vai **XML** formātā.</span><span class="sxs-lookup"><span data-stu-id="765aa-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="765aa-105">Šī pieeja tiek izmantota, lai palīdzētu uzlabot izpildīto ER formāta veiktspēju, lai ģenerētos dokumentos ievadītu kopsummu vērtības, un citiem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="765aa-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="765aa-106">Šajā tēmā ir sniegts šo funkciju kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="765aa-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="765aa-107">Atbalstīto funkciju saraksts</span><span class="sxs-lookup"><span data-stu-id="765aa-107">List of supported functions</span></span>

| <span data-ttu-id="765aa-108">Funkcija</span><span class="sxs-lookup"><span data-stu-id="765aa-108">Function</span></span> | <span data-ttu-id="765aa-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="765aa-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="765aa-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="765aa-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="765aa-111">Šī funkcija atgriež vērtību *Ierakstu saraksts*, kurā ir to vērtību saraksts, ko atgrieza formāta elementu rekvizīts **Ievāktā datu atslēgas vērtība** un kas tika savākts, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā, un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="765aa-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="765aa-112">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="765aa-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="765aa-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="765aa-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="765aa-114">Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="765aa-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="765aa-115">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="765aa-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="765aa-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="765aa-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="765aa-117">Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="765aa-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="765aa-118">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="765aa-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="765aa-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="765aa-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="765aa-120">Šī funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā ER formāta elementa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="765aa-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="765aa-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="765aa-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="765aa-122">Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="765aa-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="765aa-123">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="765aa-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="765aa-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="765aa-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="765aa-125">Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="765aa-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="765aa-126">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="765aa-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="765aa-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="765aa-127">Additional resources</span></span>

[<span data-ttu-id="765aa-128">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="765aa-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="765aa-129">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="765aa-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="765aa-130">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="765aa-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]