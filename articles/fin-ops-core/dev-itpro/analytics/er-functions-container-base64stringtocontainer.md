---
title: Base64StringToContainer ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota Base64StringToContainer elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754378"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="ebb79-103">Base64StringToContainer ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ebb79-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebb79-104">`BASE64STRINGTOCONTAINER` [funkcija](er-formula-language.md#functions) konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *[Konteiners](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="ebb79-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb79-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ebb79-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="ebb79-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ebb79-106">Arguments</span></span>

<span data-ttu-id="ebb79-107">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ebb79-107">`input`: *String*</span></span>

<span data-ttu-id="ebb79-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="ebb79-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebb79-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ebb79-109">Return values</span></span>

<span data-ttu-id="ebb79-110">*Konteiners*</span><span class="sxs-lookup"><span data-stu-id="ebb79-110">*Container*</span></span>

<span data-ttu-id="ebb79-111">Iegūtā binārā vērtība binārajā lielu objektu (BLOB) formātā.</span><span class="sxs-lookup"><span data-stu-id="ebb79-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ebb79-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ebb79-112">Usage notes</span></span>

<span data-ttu-id="ebb79-113">"Parametrs nav derīgs" izņēmums tiek izmantots, ja ievades virkne nesniedz pareizu bināro-teksta kodēšanas shēmu grupu Base64.</span><span class="sxs-lookup"><span data-stu-id="ebb79-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="ebb79-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ebb79-114">Example</span></span>

<span data-ttu-id="ebb79-115">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="ebb79-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="ebb79-116">Saknes **DocuTypeGroupEnum** *Dynamics 365 for Operations datu avots/ uzskaitījuma tips*, kas attiecas uz **DocuTypeGroup** programmas uzskaitījumu</span><span class="sxs-lookup"><span data-stu-id="ebb79-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="ebb79-117">Saknes **Debitors** *Dynamics 365 for Operations / Tabulas ieraksti* datu avots, kas atsaucas uz lietojuma tabulu **CustTable**</span><span class="sxs-lookup"><span data-stu-id="ebb79-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="ebb79-118">**\#Media** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="ebb79-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="ebb79-119">Tas ir pievienots kā debitora datu avota **Debitori** datu avots.</span><span class="sxs-lookup"><span data-stu-id="ebb79-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="ebb79-120">Tajā ir ietverta izteiksme `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="ebb79-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="ebb79-121">**\#MediaAsBase64String** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="ebb79-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="ebb79-122">Tas ir pievienots kā atvasinātā datu avota **Debitori.'\#Media'** datu avots.</span><span class="sxs-lookup"><span data-stu-id="ebb79-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="ebb79-123">Tajā ir ietverta izteiksme `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="ebb79-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="ebb79-124">**\#lobFomBase64** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="ebb79-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="ebb79-125">Tas ir pievienots kā atvasinātā datu avota **Debitori.'\#Media'** datu avots.</span><span class="sxs-lookup"><span data-stu-id="ebb79-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="ebb79-126">Tajā ir ietverta izteiksme `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="ebb79-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="ebb79-127">Šajā piemērā **\#MediaAsBase64String** datu avots kodē pašreizējā multivides pielikuma bināro saturu kā tekstu, kas apzīmē bināro-teksta kodēšanas shēmu Base64 grupu.</span><span class="sxs-lookup"><span data-stu-id="ebb79-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="ebb79-128">**\#BLOBFomBase64** datu avots atšifrē Base64 virkni un atgriež bināro vērtību BLOB formātā.</span><span class="sxs-lookup"><span data-stu-id="ebb79-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Parauga datu avoti ER Modeļu kartēšanas veidotāja lapā](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="ebb79-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ebb79-130">Additional resources</span></span>

[<span data-ttu-id="ebb79-131">Konteinera funkcijas</span><span class="sxs-lookup"><span data-stu-id="ebb79-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]