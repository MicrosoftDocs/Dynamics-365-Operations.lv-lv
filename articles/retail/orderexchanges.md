---
title: Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt atgriešanas apmaiņu programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "302579"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana

[!include [banner](includes/banner.md)]

Iepriekšējās Microsoft Dynamics 365 for Retail versijās atgriešana pret klientu pasūtījumiem tika apstrādāta, izmantojot atgriešanas pasūtījuma dokumentu komponentā Retail Headquarters. Tomēr atgriešanas pasūtījuma dokumentu var izmantot, lai apstrādātu tikai preces, kas tiek atgrieztas. Atgrieztās preces tiek norādītas ar negatīvu daudzumu atgriešanas pasūtījuma rindās. Turpretim pārdošanu norāda ar pozitīvu daudzumu. Tomēr atgriešanas pasūtījuma dokuments neatbalsta pozitīvas daudzuma vērtības. Šī ierobežojuma dēļ iepriekšējās Retail versijas neatbalstīja scenārijus, kuru ietvaros preču apmaiņa tika veikta, izmantojot atgriešanas pasūtījuma dokumentu.

Tomēr ir pievienota funkcionalitāte, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek veikta apmaiņa atgriešanas pasūtījumos. Tagad programmā Retail atgriešanas pasūtījuma dokumenta vietā tiek izmantots pārdošanas pasūtījuma dokuments, lai apstrādātu šādas transakcijas.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Retail konfigurēšana, lai atbalstītu apmaiņu atgriešanas pasūtījumos

Izpildiet šīs darbības, lai konfigurētu sistēmu, lai tā atbalstītu apmaiņu atgriešanas pasūtījumos.

1. Dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri**. Kopsavilkuma cilnē **Debitoru pasūtījumi** opcijai **Apstrādāt atgriešanas pasūtījumus kā pārdošanas pasūtījumus** atlasiet iestatījumu **Jā**.
2. Palaidiet darbu **Globālās konfigurācijas sadales grafiks** (**1110**).

## <a name="make-an-exchange"></a>Apmaiņas veikšana

Pēc tam, kad sistēma ir konfigurēta, kā aprakstīts iepriekšējā sadaļā, pārdošanas punkta (POS) lietotājs joprojām atlasa pārdošanas pasūtījumu vai pārdošanas rēķinu, lai apstrādātu atgriešanu kā iepriekšējās Retail versijās. Tomēr pēc atgriezto krājumu pievienošanas grozam lietotājs varēs pievienot grozam jaunas pārdošanas rindas.

Šīm jaunajām pārdošanas rindām lietotājam ir jādefinē visi atribūti, kas vajadzīgi, lai apstrādātu debitora pasūtījuma rindu. Šie atribūti ietver piegādes veidu un izpildes vietu. Par transakciju paredzētais maksājums ir atgriešanas pasūtījuma rindu un pārdošanas pasūtījuma rindu neto vērtība. Ja maksājums par transakciju ir samaksāts, atgriešanas pasūtījums tiks grāmatots kā pārdošanas pasūtījuma dokuments programmā Retail Headquarters un sistēma nekavējoties iekļaus rēķinā atgriešanas rindas.

Lai nodrošinātu labāku piekļuvi dažādām groza summām, grozā ir pievienoti trīs jauni summu lauki. Var izmantot ekrāna veidotāju, lai nodrošinātu šo lauku pieejamību POS lietotāja interfeisā (UI).

- **Piemērotais depozīts** — depozīta summa, kuru attiecina uz transakciju, kad lietotājs veic debitora pasūtījuma savākšanu. Ja nav veikta depozīta ignorēšana un ir konfigurēts 10 procentu depozīts, šajā laukā norādītā summa ir 90 procenti no kopējās debitora pasūtījuma summas.
- **Iznesto preču summa** — kopējā tādu rindu summa, kurām piegādes veids tika iestatīts kā **Iznest**, izveidojot vai rediģējot debitora pasūtījumu vai debitoru pasūtījuma apmaiņas laikā. Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.
- **Atgriešanas summa** — kopējā tādu rindu summa, kurās ir negatīvas summas debitora pasūtījuma apmaiņas laikā. Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.
