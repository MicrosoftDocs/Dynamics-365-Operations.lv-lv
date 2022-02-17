---
title: Darbinieku atvieglojumu plāna algu saraksts
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Darbinieku atvieglojumu plāna izmaksu saraksta entītijai programmā Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068438"
---
# <a name="payroll-worker-benefit-plan"></a>Darbinieku atvieglojumu plāna algu saraksts


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta Darbinieku atvieglojumu plāna izmaksu saraksta entītija Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Apraksts

Šis elements sniedz informāciju par konkrētā darbinieka atvieglojumu plānu.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms</br>Obligāts | Darbinieka unikālais personāla numurs. |
| **Juridiskas personas ID**</br>mshr_legalentityID</br>*Virkne* | Tikai lasāms | Norāda juridisko personu (uzņēmumu). |
| **Perioda ID**</br>mshr_periodid</br>*Virkne* | Tikai lasāms | Perioda identifikators. |
| **Plāna ID**</br>mshr_planid</br>*Virkne* | Tikai lasāms | Plāna identifikators. |
| **Seguma opcija**</br>mshr_coverageoptionid</br>*Virkne* | Tikai lasāms | Vajadzību grupas identifikācija. |
| **Ieturējumu sākuma datums**</br>mshr_deductionstartdatetime</br>*Datuma laika nobīde* | Tikai lasāms | Ieturējumu sākuma datums. |
| **Ieturēšanas beigu datums**</br>mshr_deductionstartdatetime</br>*Datuma laika nobīde* | Tikai lasāms | Ieturēšanas beigu datums. |
| **Statuss**</br>mshr_status</br>*[Darbinieka atvieglojumu plāna statusa opciju kopa](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Tikai lasāms | Atvieglojumu plāna statuss. |
| **Derīgs no**</br>mshr_validfrom</br>*Datuma Laika Nobīde* | Tikai lasāms | Laiks, no kura ir spēkā šis ieraksts. |
| **Derīgs līdz**</br>mshr_validto</br>*Datuma Laika Nobīde* |  Tikai lasāms | Laiks, līdz kuram ir spēkā šis ieraksts. |
| **Plāna tipa ID**</br>mshr_plantypeid</br>*Virkne* | Tikai lasāms | Plāna tipa identifikators. |
| **Plāna veida kods**</br>mshr_plantypecode</br>*[atvieglojumu plāna tipa seguma opciju kopa](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Tikai lasāms | Plāna tipa specifikācija. |
| **Apmaksas periodu skaits**</br>mshr_payperiod</br>*Vesels skaitlis* | Tikai lasāms | Apmaksas periodu skaits, kas parāda, cik bieži atvieglojumu nodrošinātājs vai nodarbinātie tiek apmaksāti. Šī summa tiks izmantota, lai aprēķinātu nodarbinātā gada atvieglojumu algas summu. |
| **Darbinieka summa**</br>mshr_amountemployee</br>*Decimāldaļskaitlis* | Tikai lasāms | Darbinieku skaits vai procentuālā attiecība. |
| **Darba devēja summa**</br>mshr_amountemployer</br>*Decimāldaļskaitlis* | Tikai lasāms | Darbinieku skaits vai procentuālā attiecība. |
| **Primārais lauks**</br>mshr_primaryfield</br>*Virkne* | Sistēmas ģenerēts | Primārais lauks. |
| **Darbinieka ID vērtība** </br>_mshr_fk_worker_id_value</br>*GUID* | Ārējā atslēga: mshr_hcmworkerbaseentity entītijas mshr_hcmworkerbaseentityid. | Sistēmas ģenerēts darbinieka unikālais identifikators. |
| **Perioda ID vērtība**</br> _mshr_fk_period_id_value</br>*GUID* | Ārējā atslēga: mshr_benefitperiodentity entītijas mshr_benefitperiodentityid. | Sistēmas ģenerēts perioda unikālais identifikators. |
| **Plāna ID vērtība**</br> _mshr_fk_plan_id_value</br>*GUID* | Ārējā atslēga: mshr_benefitperiodentity entītijas mshr_benefitperiodentityid. | Sistēmas ģenerēts unikālais plāna identifikators. |
| **Plāna veida ID vērtība**</br> _mshr_fk_plantype_id_value</br>*GUID* | Ārējā atslēga: mshr_benefitplantypeentity entītijas mshr_benefitplantypeentityid. | Sistēmas ģenerēts unikālais plāna identifikators. |
| **Vajadzības opcijas ID vērtība**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Ārējā atslēga: mshr_benefitcoverageoptionentityid entītijas mshr_benefitcoverageoptionentityid. | Sistēmas ģenerēts unikālais plāna identifikators. |
| **Algas darbinieka atvieglojumu plāna entītijas ID vērtība**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Tikai lasāms </br> Sistēmas ģenerēts | Sistēmas ģenerēts unikāls ieraksta identifikators. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Vaicājuma piemērs Darbinieka atvieglojumu plāna algu sarakstam

**Pieprasīt**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Atbilde**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
