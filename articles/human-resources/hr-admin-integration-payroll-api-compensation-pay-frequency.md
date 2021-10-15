---
title: Atlīdzības algas biežums
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Atlīdzības algas biežuma elementam programmā Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b864d0db8ff1b380749b6099fa74a40045932b67
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559665"
---
# <a name="compensation-pay-frequency"></a>Atlīdzības algas biežums

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Atlīdzības algu biežuma elementam programmā Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Apraksts

Šis elements sniedz informāciju par maksājuma likmes konvertēšanu par norādīto atlīdzības maksājumu biežumu.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_Veids_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Gada algas kursa konvertēšana**</br>mshr_annualconversionfactor</br>*Decimāls* | Tikai lasāms | Gada pārvēršanas koeficients maksājuma biežumam. |
| **Apraksts**</br>mshr_description</br>*Virkne* | Tikai lasāms | Pārveidošanas koeficienta apraksts. |
| **Stundas algas kursa konvertēšana**</br>mshr_hourlyconversionfactor</br>*Decimāls* | Tikai lasāms | Stundas pārvēršanas koeficients maksājuma biežumam. |
| **Mēneša algas kursa konvertēšana**</br>mshr_monthlyconversionfactor</br>*Decimāls* | Tikai lasāms | Ikmēneša pārvēršanas koeficients maksājuma biežumam. |
| **Apmaksas likmes konvertēšana**</br>mshr_payrateconversion</br>*Virkne* | Tikai lasāms | Unikāla virkne konversijas kursa identificēšanai. |
| **Periods**</br>mshr_period</br>*perioda opciju kopa* | Tikai lasāms | Galvenais periods dotās algas kursa konvertēšanai. |
| **Nedēļas algas kursa konvertēšana**</br>mshr_weeklyconversionfactor</br>*Decimāls* | Tikai lasāms | Nedēļas pārvēršanas koeficients maksājuma biežumam. |
| **Datu apgabala ID**</br>mshr_dataareaid</br>*Virkne* | Tikai lasāms | Juridiskā persona (uzņēmums). |
| **Atlīdzības algas biežuma elementa ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu ierakstu. |

## <a name="example-query-for-payroll-employee"></a>Payroll darbinieka vaicājuma piemērs

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Atbilde**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
