---
title: PADLEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota PADLEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562689"
---
# <a name="padleft-er-function"></a><span data-ttu-id="3020b-103">PADLEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="3020b-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3020b-104">`PADLEFT` funkcija norādītā garuma *Virknes* vērtību, kurā norādītās virknes sākumā ir ievadītas norādītās rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="3020b-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3020b-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="3020b-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="3020b-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="3020b-106">Arguments</span></span>

<span data-ttu-id="3020b-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3020b-107">`text`: *String*</span></span>

<span data-ttu-id="3020b-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="3020b-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="3020b-109">`length`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="3020b-109">`length`: *Integer*</span></span>

<span data-ttu-id="3020b-110">*Vesela skaitļa* vērtība, kas apzīmē rakstzīmju galīgo skaitu ievadītajā virknē.</span><span class="sxs-lookup"><span data-stu-id="3020b-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="3020b-111">`padding chars`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3020b-111">`padding chars`: *String*</span></span>

<span data-ttu-id="3020b-112">Rakstzīmes, kas jāizmanto ievadīšanai.</span><span class="sxs-lookup"><span data-stu-id="3020b-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="3020b-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="3020b-113">Return values</span></span>

<span data-ttu-id="3020b-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3020b-114">*String*</span></span>

<span data-ttu-id="3020b-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="3020b-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3020b-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="3020b-116">Example</span></span>

<span data-ttu-id="3020b-117">`PADLEFT ("1234", 10, "`&nbsp;`")` atgriež teksta virkni **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="3020b-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3020b-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3020b-118">Additional resources</span></span>

[<span data-ttu-id="3020b-119">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="3020b-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]