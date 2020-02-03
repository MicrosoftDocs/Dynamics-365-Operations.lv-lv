---
title: ALLITEMS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ALLITEMS elektroniskā pārskata (ER) funkcija.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917446"
---
# <span data-ttu-id="9377d-103"><a name="ALLITEMS">ALLITEMS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="9377d-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9377d-104">`ALLITEMS` funkcija darbojas kā atmiņas izvēle un atgriež jaunu izplātu *Ierakstu saraksta* vērtību kā ierakstu sarakstu, kas attēlo visus vienumus, kuri atbilst norādītajam ceļam.</span><span class="sxs-lookup"><span data-stu-id="9377d-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="9377d-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="9377d-105">Syntax</span></span>

```
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="9377d-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9377d-106">Arguments</span></span>

<span data-ttu-id="9377d-107">`path`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="9377d-107">`path`: *Record list*</span></span>

<span data-ttu-id="9377d-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="9377d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9377d-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9377d-109">Return values</span></span>

<span data-ttu-id="9377d-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="9377d-110">*Record list*</span></span>

<span data-ttu-id="9377d-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="9377d-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9377d-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="9377d-112">Usage notes</span></span>

<span data-ttu-id="9377d-113">Šis ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar *Ierakstu saraksta* datu tipu.</span><span class="sxs-lookup"><span data-stu-id="9377d-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="9377d-114">Tādiem datu elementiem kā ceļa virkne un datums elektronisko pārskatu (ER) izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.</span><span class="sxs-lookup"><span data-stu-id="9377d-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="9377d-115">Nav ieteicams izmantot šo funkciju transakciju datu avotiem, kas var saturēt lielu datu apjomu.</span><span class="sxs-lookup"><span data-stu-id="9377d-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="9377d-116">Tā vietā apsveriet iespēju izmantot funkciju [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="9377d-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="9377d-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="9377d-117">Example 1</span></span>

<span data-ttu-id="9377d-118">Ja `SPLIT("abcdef" , 2)` ievadāt kā datu avotu **DS**, izteiksme `COUNT( ALLITEMS (DS))` atgriež **3.**</span><span class="sxs-lookup"><span data-stu-id="9377d-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9377d-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="9377d-119">Example 2</span></span>

<span data-ttu-id="9377d-120">Ja ievadāt **Vend** kā datu avotu *Ierakstu saraksta* datu tipam, kas attiecas uz lietojumprogrammas tabulu VendTable, izteiksme `ALLITEMS (Vend.'<Relations'.ContactPerson)` atgriež saplātu ierakstu sarakstu, kam ir tabulas **ContactPerson** struktūra, un tajā ir visas kontaktpersonas, kurām var piekļūt, izmantojot **ContactPerson. contactforparty = = VendTable. Party** relāciju, un kuras ir pieejamas visiem kreditoriem no kreditoru atsauces tabulas.</span><span class="sxs-lookup"><span data-stu-id="9377d-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9377d-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9377d-121">Additional resources</span></span>

[<span data-ttu-id="9377d-122">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="9377d-122">List functions</span></span>](er-functions-category-list.md)