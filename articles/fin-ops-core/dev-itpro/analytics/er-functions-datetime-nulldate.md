---
title: NULLDATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLDATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563466"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="451c8-103">NULLDATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="451c8-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="451c8-104">`NULLDATE` funkcija atgriež *Datuma* vērtību, kas apzīmē **nulles** datumu (1900. gada 1. janvāris).</span><span class="sxs-lookup"><span data-stu-id="451c8-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="451c8-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="451c8-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="451c8-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="451c8-106">Return values</span></span>

<span data-ttu-id="451c8-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="451c8-107">*Date*</span></span>

<span data-ttu-id="451c8-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="451c8-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="451c8-109">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="451c8-109">Example 1</span></span>

<span data-ttu-id="451c8-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` atgriež **nulles** datumu, 1900. gada 1. janvāri, kā **"1900-01-01"**, pamatojoties uz norādīto pielāgoto formātu.</span><span class="sxs-lookup"><span data-stu-id="451c8-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="451c8-111">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="451c8-111">Example 2</span></span>

<span data-ttu-id="451c8-112">Izteiksme `IF( Invoice.DocumentDate = NULLDATE(), true, false)` atgriež **True**, ja lauka **DocumentDate** vērtība ir vienāda ar **nulles** datumu.</span><span class="sxs-lookup"><span data-stu-id="451c8-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="451c8-113">Šajā piemērā **Rēķins** ir elektronisko pārskatu (ER) datu avots ar veidu **Finanšu/Tabulas ieraksti**, un tas atsaucas uz tabulu CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="451c8-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="451c8-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="451c8-114">Additional resources</span></span>

[<span data-ttu-id="451c8-115">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="451c8-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]