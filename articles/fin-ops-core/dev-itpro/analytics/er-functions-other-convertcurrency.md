---
title: CONVERTCURRENCY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONVERTCURRENCY elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: fb8f7f28f5a9bb27402544efcffa6393238e38d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744371"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="fce4e-103">CONVERTCURRENCY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fce4e-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fce4e-104">`CONVERTCURRENCY` funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītas naudas summas konvertēšanai no norādītās avota valūtas norādītajā mērķa valodā, izmantojot norādītā uzņēmuma iestatījumus norādītajā datumā.</span><span class="sxs-lookup"><span data-stu-id="fce4e-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce4e-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="fce4e-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="fce4e-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="fce4e-106">Arguments</span></span>

<span data-ttu-id="fce4e-107">`amount`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="fce4e-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="fce4e-108">Skaitliska vērtība, kas apzīmē naudas summu, kura ir jākonvertē.</span><span class="sxs-lookup"><span data-stu-id="fce4e-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="fce4e-109">`source currency`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fce4e-109">`source currency`: *String*</span></span>

<span data-ttu-id="fce4e-110">Avota valūtas kods.</span><span class="sxs-lookup"><span data-stu-id="fce4e-110">The code of the source currency.</span></span>

<span data-ttu-id="fce4e-111">`target currency`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fce4e-111">`target currency`: *String*</span></span>

<span data-ttu-id="fce4e-112">Mērķa valūtas kods.</span><span class="sxs-lookup"><span data-stu-id="fce4e-112">The code of the target currency.</span></span>

<span data-ttu-id="fce4e-113">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="fce4e-113">`date`: *Date*</span></span>

<span data-ttu-id="fce4e-114">*Datuma* vērtība, kas apzīmē datumu, kas tiek izmantots, lai noteiktu konversijas valūtas kursu.</span><span class="sxs-lookup"><span data-stu-id="fce4e-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="fce4e-115">`company`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fce4e-115">`company`: *String*</span></span>

<span data-ttu-id="fce4e-116">*Virknes* vērtība, kas apzīmē tā uzņēmuma kodu, kurš nodrošina konversijai izmantotos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="fce4e-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="fce4e-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="fce4e-117">Return values</span></span>

<span data-ttu-id="fce4e-118">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="fce4e-118">*Real*</span></span>

<span data-ttu-id="fce4e-119">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fce4e-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="fce4e-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="fce4e-120">Example</span></span>

<span data-ttu-id="fce4e-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` atgriež viena eiro ekvivalentu ASV dolāros pašreizējās sesijas datumā, balstoties uz uzņēmuma **DEMF** iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="fce4e-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fce4e-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fce4e-122">Additional resources</span></span>

[<span data-ttu-id="fce4e-123">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="fce4e-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]