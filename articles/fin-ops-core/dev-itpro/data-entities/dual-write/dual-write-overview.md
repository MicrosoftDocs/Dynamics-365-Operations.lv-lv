---
title: Gandrīz reāllaika datu integrācija ar Common Data Service
description: Šajā tēmā ir sniegts apskats par integrāciju starp Finance and Operations un Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019902"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Gandrīz reāllaika datu integrācija ar Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Pašreizējā digitālajā pasaulē biznesa ekosistēmas izmanto Microsoft Dynamics 365 programmas kopumā. Tā kā dati no cilvēkiem, debitoriem, operācijām un lietu interneta (IoT) ierīcēm saplūst vienā avotā, pastāv iespēja izmantot digitālās atgriezeniskās saites cilpas. Lai iegūtu šo pieredzi, būtiska ir integrācija starp Finance and Operations programmām un citām Dynamics 365 programmām. Dažas programmas ir veidotas uz pakalpojuma Common Data Service. Integrācija starp Finance and Operations programmu datiem ar Common Data Service ļauj programmām saskaņoti un raiti sazināties ar Finance and Operations.

Finance and Operations programmas un Common Data Service nodrošina tuvu reāllaikam datu sinhronizāciju starp Finance and Operations programmām un citām Dynamics 365 programmām, izmantojot duālā ieraksta struktūru. Segums ir plašs un aptver programmas 28 svarīgākās jomas. Mērķis ir nodrošināt "One Dynamics 365" lietotāja pieredzi, izmantojot nevainojamas datu plūsmas, kas savieno biznesa procesus dažādās programmās.

![Arhitektūras pārskata diagramma](media/dual-write-overview.jpg)

Ir pieejamas šādas vērtību propozīcijas:

+ [Organizācijas hierarhija Common Data Service](organization-mapping.md)
+ [Uzņēmuma koncepts Common Data Service](company-data.md)
+ [Integrētie debitoru pamatdati](customer-mapping.md)
+ [Integrētā virsgrāmata](ledger-mapping.md)
+ [Vienotā preču pieredze](product-mapping.md)
+ [Integrētie kreditora pamatdati](vendor-mapping.md)
+ [Integrētās vietas un noliktavas](sites-warehouses-mapping.md)
+ [Integrētie nodokļu pamatdati](tax-mapping.md)

## <a name="system-requirements"></a>Sistēmas prasības

Sinhronām divvirziena tuvu reāllaikam datu plūsmām ir nepieciešamas šādas versijas:

+ Microsoft Dynamics 365 for Finance and Operations versija 10.0.4 (2019. gada jūlijs) ar 28. platformas atjauninājumu vai jaunāka versija
+ Microsoft Dynamics 365 for Customer Engagement platformas versija 9.1 (4.2) vai jaunāka versija

## <a name="setup-instructions"></a>Iestatīšanas instrukcijas

Izpildiet tālāk norādītās darbības, lai iestatītu Finance and Operations programmu un Common Data Service integrāciju.
    
1. Informāciju par duālā ieraksta sistēmas iestatīšanu skatiet rakstu [soli pa solim rokasgrāmata](https://aka.ms/dualwrite-docs) par duālā ieraksta priekšskatījuma paziņošanu.
2. Lejupielādējiet un instalējiet risinājumu [Fin OPS un CDS/CE integrācija, izmantojot Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer grupā. Pakotnē ir pieci risinājumi:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Ievērojiet izpildes kārtību, lai [sinhronizētu sākotnējos atsauces datus ](initial-sync.md).
4. Ja rodas duālā ieraksta sinhronizācijas problēmas, skatiet rakstu [Datu integrācijas problēmu novēršanas rokasgrāmata](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Jūs nevarat palaist duālo ierakstu un [No potenciālā klienta līdz skaidrai naudai](../../../../supply-chain/sales-marketing/prospect-to-cash.md) blakus vienu otram. Ja jūs izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, jums tas ir jāatinstalē. Jums ir arī jāatspējo debitoru un kreditoru duālā ieraksta veidnes, kas ir daļa no risinājuma No potenciālā klienta līdz skaidrai naudai.
