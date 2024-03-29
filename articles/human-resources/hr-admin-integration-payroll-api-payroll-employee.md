---
title: Algots darbinieks
description: Šajā rakstā ir sniegta detalizēta informācija un piemēra vaicājums darbinieka algas elementam sadaļā Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07fbc76b997600b2c076c00a63d1f6d865326d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872215"
---
# <a name="payroll-employee"></a>Algots darbinieks


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts darbinieka algas elements Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_payrollemployeeentity.

### <a name="description"></a>Apraksts

Šis elements sniedz informāciju par darbinieku. Pirms šī elementa lietošanas jāiestata [algas integrācijas parametri](hr-admin-integration-payroll-api-parameters.md).

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** un **NameValidTo** lauki vairs nebūs pieejami šim elementam. Tas nodrošina, ka ir tikai viens datuma efektīvais datu avots, kas atbalsta šo elementu.
>Šie lauki būs pieejami **DirPersonNameHistoricalEntity**, kas tika izlaists Platformas atjauninājumā 43. No  **PayrollEmployeeEntity** uz **DirPersonNameHistoricalEntity** ir OData relācija. 

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Juridiskas personas ID**</br>mshr_legalentityid</br>*Virkne* | Tikai lasāms | Norāda juridisko personu (uzņēmumu). |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs. |
| **Darba attiecību uzsākšanas datums**</br>mshr_employmentstartdate</br>*Datuma laika nobīde* | Tikai lasāms | Darbinieka nodarbinātības sākuma datums. |
| **Nodarbinātības beigu datums**</br>mshr_employmentenddate</br>*Datuma laika nobīde* | Tikai lasāms |Darbinieka nodarbinātības beigas.  |
| **Dzimšanas datums**</br>mshr_birthdate</br>*Datuma Laika Nobīde* | Tikai lasāms | Darbinieka dzimšanas datums. |
| **Dzimums**</br>mshr_gender</br>[mshr_hcmpersongender opciju kopa](hr-admin-integration-payroll-api-gender.md) | Tikai lasāms | Darbinieka dzimums. |
| **Nodarbinātības veids**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype opciju kopa](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Tikai lasāms | Nodarbinātības veids. |
| **Identifikācijas veida ID**</br>mshr_identificationtypeid</br>*Virkne* |Tikai lasāms | Darbiniekam definētais identifikācijas veids. |
| **Identifikācijas numurs uz**</br>mshr_identificationnumber</br>*Virkne* | Tikai lasāms |Darbiniekam definētais identifikācijas numurs. |
| **Gatavs apmaksai**</br>mshr_readytopay</br>[mshr_noyes opciju kopa](hr-admin-integration-payroll-api-no-yes.md) | Tikai lasāms | Norāda, vai darbinieks ir atzīmēts kā gatavs maksāt. |
| **Payroll darbinieka elementa ID**</br>mshr_payrollemployeeentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu darbinieku. |

## <a name="relations"></a>Saites

|Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Payroll darbinieka vaicājuma piemērs

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Atbilde**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
