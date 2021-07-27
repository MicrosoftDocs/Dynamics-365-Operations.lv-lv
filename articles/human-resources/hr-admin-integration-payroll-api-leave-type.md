---
title: Atvaļinājuma veids
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu atvaļinājuma veida elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: a99d53805efd7ee2001217ea3154d46b5d5e66cd
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314439"
---
# <a name="leave-type"></a>Atvaļinājuma veids

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts atvaļinājuma veida elements programmai Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šī entītija sniedz informāciju par šo atvaļinājuma veidu.

Fiziskais nosaukums: mshr_essleavetypeentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Atvaļinājuma tipa ID**</br>mshr_leavetypeid</br>*Virkne* | Tikai lasāms | Atvaļinājuma tipa ID. |
| **Apraksts**</br>mshr_description</br>*Virkne* | Tikai lasāms | Atvaļinājuma veida apraksts. |
| **Kategorija**</br>mshr_category</br>*mshr_LeaveTypeCategory opciju kopa* | Tikai lasāms | Atvaļinājuma tipa kategorija. |
| **Nepieciešams iemesla kods**</br>mshr_isreasoncoderequired</br>*mshr_NoYes opciju kopa* | Tikai lasāms | Nosaka, vai atvaļinājuma tipam ir nepieciešams pamatojuma kods. |
| **Atvaļinājuma vienotība**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit opciju kopa* | Tikai lasāms | Šī atvaļinājuma tipa vienotība. |
| **Iespējot pusi dienas**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes opciju kopa* | Definē, vai šim atvaļinājuma tipam ir aktivizēta puse dienas. |
| **Datu apgabala ID**</br>mshr_dataareaid_id</br>*Virkne* | Tikai lasāms | Norāda juridisko personu (uzņēmumu). |
| **Atvaļinājuma tipa elements**</br>mshr_essleavetypeentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbā atvaļinājuma veidu. |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Atbilde**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
