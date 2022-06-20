---
title: Atvaļinājuma bilance
description: Šajā rakstā ir sniegta detalizētas informācijas un piemēra vaicājums par atvaļinājuma bilances elementu sadaļā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4792c316b8b7af3e86b097029eb281af4a10d113
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899706"
---
# <a name="leave-balance"></a>Atvaļinājuma bilance


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts atvaļinājuma bilances elements Dynamics 365 Human Resources.

### <a name="description"></a>Apraksts

Šis elements sniedz atvaļinājumu bilanci par atvaļinājuma tipu dotam darbiniekam.

Fiziskais nosaukums: mshr_essleavebalanceentities.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs. |
| **Pašreizējā bilance**</br>mshr_balanceavailable</br>*Decimāldaļskaitlis* | Tikai lasāms | Darbinieka pašreizējā bilance. |
| **tips**</br>mshr_balanceavailable</br>*Virkne* | Tikai lasāms | Atvaļinājuma tipa ID. |
| **Uzkrātā likme**</br>mshr_accrualratedescription</br> | Tikai lasāms | Uzkrāšanas likme. |
| **Pēdējā pārnestā summa**</br>mshr_lastcarryforwardamount</br>*Decimāldaļskaitlis* | Tikai lasāms | Pēdējās pārnešanas summa. |
| **Paņemts šogad**</br>mshr_takenthisyear</br>*Decimāldaļskaitlis* | Tikai lasāms | Šogad lietotā atvaļinājuma summa. |
| **Kopā šajā gadā**</br>mshr_totalthisyear</br>*Decimāldaļskaitlis* | Tikai lasāms | Šī gada kopējā summa. |
| **Datu apgabala ID**</br>mshr_dataareaid_id</br>*Virkne* | Tikai lasāms | Norāda juridisko personu (uzņēmumu). |
| **Primārais lauks**</br>mshr_primaryfield</br>*GUID* | Tikai lasāms</br>Sistēmas ģenerēts | |
| **Atvaļinājuma tipa ID**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Tikai lasāms</br>Ārējā atslēga:mshr_essleavetypeentityid mshr_essleavetypeentity elements  | Atvaļinājuma tipa ID |
| **Atvaļinājuma bilances elements**</br>mshr_essleavebalanceentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu bilanci. |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Atbilde**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
