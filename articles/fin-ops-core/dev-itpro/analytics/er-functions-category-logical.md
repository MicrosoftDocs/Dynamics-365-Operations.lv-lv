---
title: ER funkciju saraksts loģikas kategorijā
description: Šajā tēmā ir sniegta informācija par loģikas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916641"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="e3bb0-103">ER funkciju saraksts loģikas kategorijā</span><span class="sxs-lookup"><span data-stu-id="e3bb0-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3bb0-104">Elektronisko pārskatu (ER) loģiskās funkcijas var izmantot, lai strādātu ar loģiskām vērtībām un veiktu vairāk nekā vienu salīdzinājumu vienā izteiksmē vai pārbaudītu vairākus nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="e3bb0-105">Šajā tēmā ir sniegts šo funkciju kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="e3bb0-106">Atbalstīto funkciju saraksts</span><span class="sxs-lookup"><span data-stu-id="e3bb0-106">List of supported functions</span></span>

| <span data-ttu-id="e3bb0-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="e3bb0-107">Function</span></span> | <span data-ttu-id="e3bb0-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e3bb0-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="e3bb0-109">And</span><span class="sxs-lookup"><span data-stu-id="e3bb0-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="e3bb0-110">Šī funkcija atgriež *Būla* vērtību **TRUE**, ja visi norādītie nosacījumi ir patiesi.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="e3bb0-111">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="e3bb0-112">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="e3bb0-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="e3bb0-113">Šī funkcija novērtē norādītās izteiksmes vērtību pret norādītajām alternatīvajām opcijām un atgriež pirmās opcijas, kas ir vienāda ar norādītās izteiksmes vērtību, rezultātu.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="e3bb0-114">Pretējā gadījumā tas atgriež neobligātu noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts kā pēdējās funkcijas izsauktais arguments, pirms kura neatrodas opcija.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="e3bb0-115">Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="e3bb0-116">Ja</span><span class="sxs-lookup"><span data-stu-id="e3bb0-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="e3bb0-117">Šī funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="e3bb0-118">Pretējā gadījumā tiek atgriezta otrā norādītā vērtība.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="e3bb0-119">Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="e3bb0-120">Ne</span><span class="sxs-lookup"><span data-stu-id="e3bb0-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="e3bb0-121">Šī funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="e3bb0-122">Vai</span><span class="sxs-lookup"><span data-stu-id="e3bb0-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="e3bb0-123">Šī funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="e3bb0-124">Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="e3bb0-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="e3bb0-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="e3bb0-126">Šī funkcija nosaka, vai norādītā ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="e3bb0-127">Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="e3bb0-128">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e3bb0-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e3bb0-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e3bb0-129">Additional resources</span></span>

[<span data-ttu-id="e3bb0-130">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="e3bb0-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e3bb0-131">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="e3bb0-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="e3bb0-132">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="e3bb0-132">Electronic reporting formula language</span></span>](er-formula-language.md)
