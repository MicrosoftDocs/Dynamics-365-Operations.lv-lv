---
title: Dokumenta stāvokļi un dzīves cikls
description: Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914891"
---
# <a name="document-states-and-lifecycle"></a>Dokumenta stāvokļi un dzīves cikls

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.

## <a name="document-state-descriptions"></a>Dokumenta stāvokļa apraksti

Tēmā [Lapas elementi](page-elements-overview.md) uzskaitīti dažādi dokumentu veidi satura pārvaldības sistēmā (CMS). Šiem dokumentu veidiem autorēšanas rīkā var būt vairāki stāvokļi. Dokumenta stāvokļi palīdz novērst datu konfliktus un ieviest versiju kontroli. Tās nosaka, kurš var mainīt dokumentus, kad to var darīt, un kad citas personas var skatīt izmaiņas.

Tālāk redzamā tabula parāda Commerce iespējamos lapas elementu dokumenta stāvokļus.

| Dokumenta stāvoklis | Apraksts |
|---|---|
| Izrakstījies | Kad CMS elements ir izrakstīts jums, citi autentificēti sistēmas lietotāji to nevar rediģēt. Visas izmaiņas, ko veicat elementā, redzamas tikai jums. |
| Reģistrējies | Kad CMS elements ir reģistrēts, visas izmaiņas ir redzamas citiem autentificētiem sistēmas lietotājiem, un šie lietotāji var izrakstīt elementu un to rediģēt. Katra reģistrācija izveido dokumenta versijas ierakstu elementa vēsturē. |
| Publicēts | Kad CMS elements ir publicēts, tas tiek iestumts jūsu aktuālajā vietnē un internetā kļūst pamanāms ieautentificētiem ārējiem lietotājiem. Elementus var publicēt tikai tad, ja tie ir reģistrēti. |
| Saglabāts | Izmaiņas, kas veiktas izrakstītam CMS elementam, var tikt saglabātas CMS pirms elements ir reģistrēts vai publicēts. Šīs saglabātās izmaiņas nav redzamas citiem autentificētiem sistēmas lietotājiem, kamēr elements nav reģistrēts. Tie nav redzami ārējiem lietotājiem, kamēr elements nav publicēts. |
| Atmestā izrakstīšana | Kad izrakstītais CMS elements tiek atmests, visas saglabātās izmaiņas tiek dzēstas, un elements atgriežas pēdējā reģistrētajā versijā. |

## <a name="additional-resources"></a>Papildu resursi

[Satura pievienošanas veidi](add-manage-content.md)

[Lapas modeļa glosārijs](page-elements-overview.md)

[Darbs ar publicēšanas grupām](publish-groups.md)

[Darbs ar moduļiem](work-with-modules.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Vietnes navigācijas pielāgošana](customize-site-navigation.md)
