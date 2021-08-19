---
title: Personas izglītība
description: Šajā tēmā aprakstīts Personas izglītības elements Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e24188674c7746794c0e531dea21aa9b7f57b3534d4b67298cad19b6bec2a53
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731371"
---
# <a name="person-education"></a>Personas izglītība

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas izglītības elements Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersoneducationentity

## <a name="description"></a>Apraksts

Šajā elementā ir katras personas, kura ir kandidāts, izglītības vēsture. Izglītība ir saistīta ar personas ierakstu, kas rada iespēju izglītību saistīt ar visām citām personai izveidotajām lomām papildus kandidāta ierakstam (darbinieks, darbuzņēmējs utt.).

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas izglītības elementa ID**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls personas izglītības elementa ieraksta identifikators. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Unikāls kandidāta puses (personas) ieraksta identifikators. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts unikāls kandidāta personas ieraksta identifikators. |
| **Kredītu bāze**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Izglītības pakāpes kredītu bāze. |
| **Izpildīti kredīti**<br>mshr_creditscompleted<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | Izglītībai izpildīto kredītu skaits. |
| **Nopelnītie kredīti**<br>mshr_creditsearned<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | To kredītpunktu skaits, kas nopelnīti, lai iegūtu pašreizējo izglītības līmeni. |
| **Nepieciešamie kredīti**<br>mshr_creditsneeded<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | Pašreizējam izglītības līmenim nepieciešamo kredītu skaits. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Kandidāta grāda apraksts. |
| **Izglītības līmeņa ID**<br>mshr_educationlevelid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Izglītības līmeņa ID. | 
| **Izglītības līmeņa ID vērtība**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmeducationdegreeentity elementa mshr_hcmeducationdegreeentityid | Sistēmas ģenerēts identifikators izglītības līmeņa ierakstam. Šis identifikators norāda grādus un izglītības līmeņus, kas definēti organizācijai. |
| **Izglītības nozares ID**<br>mshr_educationdisciplineid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts<br>Ārējā atslēga: EducationDiscipline | Izglītības nozares ID. |
| **Izglītības nozares ID vērtība**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmeducationdisciplineentity mshr_hcmeducationdisciplineentityid | Sistēmas ģenerēts izglītības nozares vai izglītības ieraksta unikālais identifikators. |
| **Sekundārais uzsvars**<br>mshr_secondaryemphasis<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Iegūtā grāda sekundārais uzsvars. |
| **Izglītības iestādes ID**<br>mshr_educationinstitutionid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Apmeklētās izglītības iestādes ID. |
| **Izglītības iestādes ID vērtība**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmeducationinstitutionentity mshr_hcmeducationinstitutionentityid | Sistēmas ģenerēts izglītības iestādes identifikators. |
| **Sākuma datums**<br>mshr_startdate<br>*Datetime* | Lasīt/rakstīt<br>Neobligāti | Iegūtā grāda izglītības sākuma datums. |
| **Beigu datums**<br>mshr_enddate<br>*Datetime* | Lasīt/rakstīt<br>Obligāts | Datums, kurā izsniegti akreditācijas dati. |
| **Ilgums**<br>mshr_duration<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | Izglītības ieraksta laika ilgums. |
| **Ilguma vienība**<br>mshr_durationunit<br>*mshr_periodunit opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Ar izglītības ieraksta ilgumu saistītā laika vienība. |
| **Vidējais baļļu skaits**<br>mshr_gradepointaverage<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | Vidējais grādam iegūtais vērtējums. |
| **Punktu skala**<br>mshr_gradescale<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Vidējam punktu skaitam izmantotā skala. |
| **Piezīmes**<br>mshr_notes<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Piezīmes, ko izmantot darbā pieņēmējam vai personāla atlases darbiniekam. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas tiek izmantots kā elementa ieraksta cits primārais identifikators. Puses numura, izglītības nozares ID, izglītības iestādes ID un izglītības līmeņa ID kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]