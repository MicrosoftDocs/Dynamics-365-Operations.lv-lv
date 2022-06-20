---
title: Atvaļinājuma pieprasījums
description: Šajā rakstā ir sniegta detalizēta informācija un piemēram vaicājums par atvaļinājuma pieprasījuma elementu sadaļā Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899677"
---
# <a name="leave-request"></a>Atvaļinājuma pieprasījums


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta atvaļinājuma pieprasījuma elements Dynamics 365 Human Resources.

### <a name="description"></a>Apraksts

Šī entītija sniedz informāciju par atvaļinājuma pieprasījumu.

Fiziskais nosaukums: mshr_essleaverequestentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Pieprasījuma ID**</br>mshr_requestid</br>*Virkne* | Tikai lasāms | Pieprasījuma ID. |
| **Atvaļinājuma tipa ID**</br>mshr_leavetypeid</br>*Virkne* | Tikai lasāms | Atvaļinājuma tipa ID. |
| **Datums**</br>mshr_leavedate</br>*Datuma Laika Nobīde* | Tikai lasāms | Atvaļinājuma pieprasījuma datums. |
| **Summa**</br>mshr_amount</br>*Decimāldaļskaitlis* | Tikai lasāms | Atvaļinājuma pieprasījuma summa. |
| **Puse dienas tips**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition opciju kopa* | Tikai lasāms | Puse dienas atvaļinājuma tips. |
| **Komentārs**</br>mshr_comment</br>*Virkne* | Tikai lasāms | Pievienot komentāru pieprasījumam. |
| **Statuss**</br>mshr_status</br>*mshr_status opciju kopa* | Tikai lasāms | Pieprasījuma statuss. |
| **Datums**</br>mshr_requestdate</br>*Datuma Laika Nobīde* | Tikai lasāms | Pieprasījuma datums. |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs. |
| **Iemeslu koda ID**</br>mshr_reasoncodeid</br>*Virkne* | Tikai lasāms | Iemeslu koda ID. |
| **Datu apgabala ID**</br>mshr_dataareaid</br>*Virkne* | Tikai lasāms | Norāda juridisko personu (uzņēmumu). |
| **Primārais lauks**</br>mshr_primaryfield</br>*GUID* | Tikai lasāms</br>Sistēmas ģenerēts | |
| **Atvaļinājuma tipa elements**</br>mshr_essleaverequestentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbā atvaļinājuma pieprasījumu. |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Atbilde**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
