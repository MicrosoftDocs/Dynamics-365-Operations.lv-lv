---
title: Tuvu reāllaikam datu integrācija starp Finance and Operations un Common Data Service.
description: Šajā tēmā ir sniegts apskats par integrāciju starp Microsoft Dynamics 365 for Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797232"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Tuvu reāllaikam datu integrācija starp Finance and Operations un Common Data Service.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Pašreizējā digitālajā pasaulē biznesa ekosistēmas izmanto Microsoft Dynamics 365 komplektu kopumā. Tā kā dati no cilvēkiem, debitoriem, operācijām un lietu interneta (IoT) ierīcēm saplūst vienā avotā, pastāv iespēja izmantot digitālās atgriezeniskās saites cilpas. Lai sasniegtu šo pieredzi, būtiska ir integrācija starp programmām Dynamics 365 for Finance and Operations un Dynamics 365 for Customer engagement. Customer Engagement programmas ir veidotas uz pakalpojuma Common Data Service. Integrācija starp Finance and Operations datiem ar Common Data Service ļauj Customer engagement programmām saskaņoti un raiti sazināties ar Finance and Operations.

Finance and Operations un Common Data Service nodrošina tuvu reāllaikam datu sinhronizāciju starp Finance and Operations un Customer engagement programmām, izmantojot duālā ieraksta struktūru. Segums ir plašs un aptver 28 Finance and Operations svarīgākās jomas. Mērķis ir nodrošināt "One Dynamics 365" lietotāja pieredzi, izmantojot nevainojamas datu plūsmas, kas savieno biznesa procesus dažādās programmās.

![Arhitektūras pārskata diagramma](media/dual-write-overview.jpg)

Debitoriem ir pieejamas šādas vērtību propozīcijas:

+ [Organizācijas hierarhija Common Data Service](dual-write-organization.md)
+ [Uzņēmuma koncepts Common Data Service](dual-write-company.md)
+ [Integrētie debitoru pamatdati](dual-write-customer.md)
+ [Integrētie kreditora pamatdati](dual-write-vendor.md)
+ Vienoti preces pamatdati

## <a name="system-requirements"></a>Sistēmas prasības

Sinhronām divvirziena tuvu reāllaikam datu plūsmām ir nepieciešamas šādas versijas:

+ Microsoft Dynamics 365 for Finance and Operations versija 10.0.4 (2019. gada jūlijs) ar 28. platformas atjauninājumu vai jaunāka versija
+ Microsoft Dynamics 365 for Customer Engagement platformas versija 9.1 (4.2) vai jaunāka versija

## <a name="setup-instructions"></a>Iestatīšanas instrukcijas

Izpildiet tālāk norādītās darbības, lai iestatītu programmas Finance and Operations un pakalpojuma Common Data Service integrāciju.
    
1. Informāciju par duālā ieraksta sistēmas iestatīšanu skatiet rakstu [soli pa solim rokasgrāmata](https://aka.ms/dualwrite-docs) par duālā ieraksta priekšskatījuma paziņošanu.
2. Lejupielādējiet un instalējiet risinājumu no [Finance and Operations, Common Data Service un Customer engagement integrācijas](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer grupas. Pakotnē ir pieci risinājumi:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Ievērojiet izpildes kārtību, lai [sinhronizētu sākotnējos atsauces datus ](dual-write-initial.md).
4. Ja rodas duālā ieraksta sinhronizācijas problēmas, skatiet rakstu [Datu integrācijas problēmu novēršanas rokasgrāmata](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Jūs nevarat palaist duālo ierakstu un [No potenciālā klienta līdz skaidrai naudai](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) blakus vienu otram. Ja jūs izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, jums tas ir jāatinstalē. Jums ir arī jāatspējo debitoru un kreditoru duālā ieraksta veidnes, kas ir daļa no risinājuma No potenciālā klienta līdz skaidrai naudai.
