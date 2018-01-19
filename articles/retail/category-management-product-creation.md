---
title: "Preču kategoriju pārvaldība un veidošana"
description: "Šajā tēmā ir aprakstīti mazumtirdzniecības preču kategoriju pārvaldības funkcionalitātei veiktie uzlabojumi. Šie uzlabojumi preču pārvaldniekiem ļauj izmantot korelāciju starp mazumtirdzniecības preču hierarhiju un izlaisto preču detalizēto informāciju."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 2aa9f913b7faac393c4b403c6c36b99cc9acc80c
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="2d174-104">Preču kategoriju pārvaldība un veidošana</span><span class="sxs-lookup"><span data-stu-id="2d174-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="2d174-105">Mazumtirdzniecības preču kategoriju pārvaldības funkcionalitātei veiktie uzlabojumi preču pārvaldniekiem ļauj izmantot korelāciju starp mazumtirdzniecības preču hierarhiju un izlaisto preču detalizēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="2d174-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="2d174-106">Lai skatītu šos uzlabojumus, darbvietā **Kategorija un preču pārvaldība** atlasiet **Mazumtirdzniecības preču hierarhija**, tādējādi atverot lapu **Jauna mazumtirdzniecības preču kategorijas struktūra**.</span><span class="sxs-lookup"><span data-stu-id="2d174-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="2d174-107">Iepriekšējos laidienos preču rekvizīti bija iedalīti pamata preču rekvizītos un mazumtirdzniecības preču rekvizītos, pamatojoties uz to piemērojamību.</span><span class="sxs-lookup"><span data-stu-id="2d174-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="2d174-108">Mazumtirdzniecības preču rekvizīti bija *globāli*.</span><span class="sxs-lookup"><span data-stu-id="2d174-108">Retail product properties were *global*.</span></span> <span data-ttu-id="2d174-109">Citiem vārdiem sakot — katram attiecīgajam preces rekvizītam viena un tā pati vērtība tiek koplietota visās juridiskajās personās.</span><span class="sxs-lookup"><span data-stu-id="2d174-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="2d174-110">Pamata preču rekvizīti bija *atkarīgi no juridiskajās personas*.</span><span class="sxs-lookup"><span data-stu-id="2d174-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="2d174-111">Citiem vārdiem sakot — attiecīgais preču rekvizīts dažādās juridiskajās personās varēja atšķirties, pamatojoties uz atsevišķajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="2d174-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="2d174-112">Līdz ar šo uzlabojumu ieviešanu preču rekvizītiem mazumtirdzniecības preču kategorijā mēs turpinām laukus atdalīt, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.</span><span class="sxs-lookup"><span data-stu-id="2d174-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="2d174-113">Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanas visās juridiskajās juridiskās personās, uz varat tos pārvaldīt konkrētai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="2d174-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="2d174-114">Pēc nepieciešamības vienkārši atlasiet **Skatīt/rediģēt visām juridiskajām personām** vai **Skatīt/rediģēt konkrētai juridiskajai personai**.</span><span class="sxs-lookup"><span data-stu-id="2d174-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="2d174-115">Turklāt preču pārvaldnieki var definēt noklusējuma vērtības attiecībā uz preču rekvizītu papildu kopu atsevišķas kategorijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="2d174-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="2d174-116">Šīs rekvizītu vērtības prece pārmanto, ņemot vērā to saistību ar kategoriju, kāda pastāv preces izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="2d174-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="2d174-117">Atlasīt rekvizītus, lai atjauninātu preces no mazumtirdzniecības preču kategorijas formas</span><span class="sxs-lookup"><span data-stu-id="2d174-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="2d174-118">Lai atlasītu, kuri atjauninātie preču rekvizīti ir jāvirza uz saistītajām precēm, varat izmantot loģiskos grupēšanas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="2d174-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="2d174-119">Preču pārvaldnieki šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="2d174-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

