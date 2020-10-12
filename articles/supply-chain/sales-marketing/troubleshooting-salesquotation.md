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
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834391"
---
# <a name="troubleshoot-sales-quotations"></a>Pārdošanas piedāvājumu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Nevar izmainīt pārdošanas piedāvājuma pārdošanas daudzumu pakalpojumu krājumam.

### <a name="issue-description"></a>Problēmas apraksts

Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums: “Lauka Daudzums atjaunināšana nav atļauta.”

### <a name="issue-resolution"></a>Problēmas risinājums

Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi. Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo fiziska krājuma nav. Ir tikai pakalpojums.

