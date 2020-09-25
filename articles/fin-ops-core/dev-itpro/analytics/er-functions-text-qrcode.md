---
title: QRCODE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota QRCODE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: f634976d83fb4066a953b7ab09c963214415e29b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743762"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="5857c-103">QRCODE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="5857c-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5857c-104">`QRCODE` funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="5857c-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5857c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="5857c-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="5857c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="5857c-106">Arguments</span></span>

<span data-ttu-id="5857c-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="5857c-107">`text`: *String*</span></span>

<span data-ttu-id="5857c-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="5857c-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5857c-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="5857c-109">Return values</span></span>

<span data-ttu-id="5857c-110">*Konteiners*</span><span class="sxs-lookup"><span data-stu-id="5857c-110">*Container*</span></span>

<span data-ttu-id="5857c-111">Iegūtā binārā plūsma.</span><span class="sxs-lookup"><span data-stu-id="5857c-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="5857c-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="5857c-112">Example</span></span>

<span data-ttu-id="5857c-113">Varat konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu izejošo dokumentu Microsoft Office formātā (Excel darbgrāmatas vai Word dokumenti), izmantojot iepriekš definētu veidni.</span><span class="sxs-lookup"><span data-stu-id="5857c-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="5857c-114">Šī veidne var saturēt objektu **Attēls** (Excel darbgrāmata) vai **Attēla satura vadīklu** (Word dokuments) kā QR koda attēla vietturi.</span><span class="sxs-lookup"><span data-stu-id="5857c-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="5857c-115">Jums jāpievieno konfigurētajam ER formātam **Šūnas** elements, kas tiks izmantots šī viettura aizpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="5857c-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="5857c-116">Lai norādītu, kāda informācija tiks glabāta QR kodā, jums ir jādefinē saistījums šim **Šūnas** elementam.</span><span class="sxs-lookup"><span data-stu-id="5857c-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="5857c-117">Piemēram, varat konfigurēt šādu saistījumu, kā tādu, kas satur šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="5857c-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="5857c-118">Palaižot konfigurēto ER formātu, datu avota **model.ListOfShelfLabels** lauka **LabelText** teksta vērtība tiks izmantota, lai ģenerētu QR koda attēlu.</span><span class="sxs-lookup"><span data-stu-id="5857c-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="5857c-119">Šis attēls aizstās QR koda attēla vietturi dokumenta veidnē, izmantojot, lai ģenerētu izejošo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5857c-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="5857c-120">Ja šis ģenerētā dokumenta attēls tiek skenēts, tas atgriež tekstu, kas tika ņemts no datu avota **model.ListOfShelfLabels** lauka **LabelText**.</span><span class="sxs-lookup"><span data-stu-id="5857c-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="5857c-121">Vairāk informācijas skatiet rakstā [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="5857c-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5857c-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5857c-122">Additional resources</span></span>

[<span data-ttu-id="5857c-123">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="5857c-123">Text functions</span></span>](er-functions-category-text.md)
