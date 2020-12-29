---
title: Pārdošanas piedāvājumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432733"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="b23b8-103">Pārdošanas piedāvājumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="b23b8-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="b23b8-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="b23b8-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="b23b8-105">Nevar izmainīt pārdošanas piedāvājuma pārdošanas daudzumu pakalpojumu krājumam.</span><span class="sxs-lookup"><span data-stu-id="b23b8-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b23b8-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="b23b8-106">Issue description</span></span>

<span data-ttu-id="b23b8-107">Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums: “Lauka Daudzums atjaunināšana nav atļauta.”</span><span class="sxs-lookup"><span data-stu-id="b23b8-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b23b8-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="b23b8-108">Issue resolution</span></span>

<span data-ttu-id="b23b8-109">Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi.</span><span class="sxs-lookup"><span data-stu-id="b23b8-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="b23b8-110">Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo fiziska krājuma nav.</span><span class="sxs-lookup"><span data-stu-id="b23b8-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="b23b8-111">Ir tikai pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="b23b8-111">There is only a service.</span></span>

