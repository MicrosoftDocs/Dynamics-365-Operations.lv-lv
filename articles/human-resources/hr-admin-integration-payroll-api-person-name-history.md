---
title: Personas vārda un uzvārda vēsture
description: Šajā rakstā ir sniegta detalizēta informācija un piemēram vaicājums par personas vārda vēstures elementu sadaļā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875776"
---
# <a name="person-name-history"></a>Personas vārda un uzvārda vēsture


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts personas vārda vēstures elements sadaļā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Apraksts

Šis elements sniedz informāciju par konkrētās personas vārda un uzvārda vēsturi.

> [!IMPORTANT] 
> **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** un **NameValidTo** lauki vairs nebūs pieejami šim elementam. Tie irnoņemti, nodrošinot, ka ir tikai viens datuma efektīvais datu avots, kas atbalsta šo elementu.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_Veids_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Vārds**</br>mshr_firstname</br>*Virkne* | Tikai lasāms | Vārds. |
| **Uzvārda prefikss**</br>mshr_lastnameprefix</br>*Virkne*) | Tikai lasāms | Uzvārda prefikss. |
| **Uzvārds**</br>mshr_lastname</br>*Virkne*) | Tikai lasāms | Uzvārds. |
| **Otrais vārds**</br>mshr_middlename</br>*Virkne*) | Tikai lasāms | Otrais vārds. |
| **Derīgs līdz**</br>mshr_validto</br>*Virkne*) | Tikai lasāms | Datums, l​īdz kuram vārds ir spēkā. |
| **Puses numurs**</br>mshr_partynumber</br>*Virkne* | Tikai lasāms | Lietotājam lasāms, sistēmas ģenerēts unikāls personas identifikators. |
| **Primārais lauks**</br>mshr_primaryfield</br>*Virkne* | Tikai lasāms | Ieraksta unikālais identifikators. |
| **Personas vārda un uzvārda vēstures elementa ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu ierakstu. |

## <a name="relations"></a>Saites

| Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| Nav attiecināms | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Nav attiecināms | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Payroll darbinieka vaicājuma piemērs

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Atbilde**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
