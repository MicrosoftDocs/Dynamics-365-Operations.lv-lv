---
title: Dynamics 365 globalizācijas pakalpojumi
description: Šajā rakstā sniegts pārskats par Microsoft Dynamics 365 globalizācijas pakalpojumiem.
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278238"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 globalizācijas pakalpojumi

[!include [banner](../includes/banner.md)]

Tālāk norādītos globalizācijas pakalpojumus var konfigurēt, lai paplašinātu iespējas, kas pastāv dažos Microsoft Dynamics 365 tiešsaistes pakalpojumos:

- **Regulatory Configuration Service (RCS)** atbalsta dažādu veidu elektronisko dokumentu un pārskatu konfigurācijas. RCS nodrošina uzlabotu elektronisko pārskatu izrakstīšanas (ER) veidotāja versiju, kur konfigurācijas repozitorijs ir savrups pakalpojums. Plašāku informāciju skatiet [Regulatory Configuration Service](rcs-overview.md).
- **Elektronisko rēķinu izrakstīšana** apvieno konfigurējamus formātus pārveidojumiem, ciparparakstiem un konfigurējamām integrācijām savienojamībai ar ārējiem tīmekļa pakalpojumiem, ieskaitot sertifikāciju un atbildes apstrādi. Plašāku informāciju skatiet [Elektronisko rēķinu izrakstīšana](e-invoicing-service-overview.md).
- **Nodokļu aprēķins** nodrošina lielāku elastīgumu, atbalstaot daudzus nodokļu ID, nodokļu koda noteikšanu, nodokļu aprēķina veidotāju un izpildlaika programmu, lai atbilstu sarežģītiem nodokļu noteikumiem visā pasaulē. Papildinformāciju skatiet sadaļā [Nodokļu aprēķins](global-tax-calcuation-service-overview.md).

Šie globalizācijas pakalpojumi nodrošina nestandarta integrāciju ar šādiem Dynamics 365 tiešsaistes pakalpojumiem.

| Tiešsaistes pakalpojums | RCS | Elektroniskā rēķinu izrakstīšana | Nodokļu aprēķins (priekšskatījums) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Jā | Jā | Jā | 
| Dynamics 365 Supply Chain Management | Jā | Jā | Jā | 
| Dynamics 365 Project Operations | Jā | Jā | Nav attiecināms | 
| Dynamics 365 Commerce | Jā | Nav attiecināms | Nav attiecināms | 

> [!NOTE]
> Tā kā ir atšķirības Azure ģeogrāfisko atrašanās vietu (geos) pieejamībā RCS, šī pakalpojuma konfigurēšana var izraisīt klientu datu pārsūtīšanu ārpus ģeogrāfiskām atrašanās vietām, kas ir atlasītas atbilstošajam Dynamics 365 tiešsaistes pakalpojumam. Papildinformāciju skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/rcs/D365Productavailabilityguide).
