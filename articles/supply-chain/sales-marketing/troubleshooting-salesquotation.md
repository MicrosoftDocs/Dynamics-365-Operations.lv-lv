---
title: Pārdošanas piedāvājumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824754"
---
# <a name="troubleshoot-sales-quotations"></a>Pārdošanas piedāvājumu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar pārdošanas piedāvājumiem.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Nevar izmainīt pārdošanas piedāvājuma pārdošanas daudzumu pakalpojumu krājumam.

### <a name="issue-description"></a>Problēmas apraksts

Mēģinot iestatīt pārdošanas daudzumu (**SalesQty** lauks) pārdošanas piedāvājuma rindas krājuma tipam *Pakalpojums*, tiks parādīts šāds ziņojums: “Lauka Daudzums atjaunināšana nav atļauta.”

### <a name="issue-resolution"></a>Problēmas risinājums

Pārdošanas daudzumu nevar iestatīt precēm, kas ir pakalpojumu krājumi. Piemēram, ja piedāvājat krājuma instalēšanas pakalpojumu, nav jēgas ierakstīt daudzumu, jo fiziska krājuma nav. Ir tikai pakalpojums.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]