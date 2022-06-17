---
title: Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana
description: Šajā rakstā ir paskaidrots, kā konfigurēt atgriešanas apmaiņu programmā Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: f33c674e4110b4e45ac58e499a65da2509b00046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845797"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana

[!include [banner](includes/banner.md)]

Iepriekšējās Dynamics 365 Commerce versijās atgriešana pret klientu pasūtījumiem tika apstrādāta, izmantojot atgriešanas pasūtījuma dokumentu komponentā Headquarters. Tomēr atgriešanas pasūtījuma dokumentu var izmantot, lai apstrādātu tikai preces, kas tiek atgrieztas. Atgrieztās preces tiek norādītas ar negatīvu daudzumu atgriešanas pasūtījuma rindās. Turpretim pārdošanu norāda ar pozitīvu daudzumu. Tomēr atgriešanas pasūtījuma dokuments neatbalsta pozitīvas daudzuma vērtības. Šī ierobežojuma dēļ iepriekšējās programmas versijas neatbalstīja scenārijus, kuru ietvaros preču apmaiņa tika veikta, izmantojot atgriešanas pasūtījuma dokumentu.

Tomēr ir pievienota funkcionalitāte, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek veikta apmaiņa atgriešanas pasūtījumos. Tagad programmā Commerce atgriešanas pasūtījuma dokumenta vietā tiek izmantots pārdošanas pasūtījuma dokuments, lai apstrādātu šādas transakcijas.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Commerce konfigurēšana, lai atbalstītu apmaiņu atgriešanas pasūtījumos

> [!NOTE]
> Commerce versijā 10.0.20 un jaunākās versijās ir pieejams jauns līdzeklis ar nosaukumu “Vienotā atgriešanas apstrādes pieredze programmā POS”. Ja iespējosit šo līdzekli, tālāk norādītās iestatīšanas darbības nebūs nepieciešamas. **Apstrādāt atgriešanas pasūtījumus kā pārdošanas pasūtījumus** kļūs par neatgriezeniski konfigurētu iestatījumu, un to nevarēs mainīt.

Veiciet šīs darbības, lai sistēmā konfigurētu atbalstu atgriešanas pasūtījumu maiņai (ja nav iespējots līdzeklis **Vienotā atgriešanas apstrādes pieredze programmā POS**).

1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce parametri**. Kopsavilkuma cilnē **Debitoru pasūtījumi** opcijai **Apstrādāt atgriešanas pasūtījumus kā pārdošanas pasūtījumus** atlasiet iestatījumu **Jā**.
2. Palaidiet darbu **Globālās konfigurācijas sadales grafiks** (**1110**).

## <a name="make-an-exchange"></a>Apmaiņas veikšana

Pēc tam, kad sistēma ir konfigurēta, kā aprakstīts iepriekšējā sadaļā, pārdošanas punkta (POS) lietotājs joprojām atlasa pārdošanas pasūtījumu vai pārdošanas rēķinu, lai apstrādātu atgriešanu kā iepriekšējās programmas versijās. Tomēr pēc atgriezto krājumu pievienošanas grozam lietotājs varēs pievienot grozam jaunas pārdošanas rindas.

Šīm jaunajām pārdošanas rindām lietotājam ir jādefinē visi atribūti, kas vajadzīgi, lai apstrādātu debitora pasūtījuma rindu. Šie atribūti ietver piegādes veidu un izpildes vietu. Par transakciju paredzētais maksājums ir atgriešanas pasūtījuma rindu un pārdošanas pasūtījuma rindu neto vērtība. Kad darījumam atbilstošais maksājums tiks samaksāts, atgriešanas pasūtījums tiks grāmatots kā pārdošanas pasūtījuma dokuments programmā Headquarters un sistēma nekavējoties iekļaus rēķinā atgriešanas rindas.

Lai nodrošinātu labāku piekļuvi dažādām groza summām, grozā ir pievienoti trīs jauni summu lauki. Var izmantot ekrāna veidotāju, lai nodrošinātu šo lauku pieejamību POS lietotāja interfeisā (UI).

- **Piemērotais depozīts** — depozīta summa, kuru attiecina uz transakciju, kad lietotājs veic debitora pasūtījuma savākšanu. Ja nav veikta depozīta ignorēšana un ir konfigurēts 10 procentu depozīts, šajā laukā norādītā summa ir 90 procenti no kopējās debitora pasūtījuma summas.
- **Iznesto preču summa** — kopējā tādu rindu summa, kurām piegādes veids tika iestatīts kā **Iznest**, izveidojot vai rediģējot debitora pasūtījumu vai debitoru pasūtījuma apmaiņas laikā. Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.
- **Atgriešanas summa** — kopējā tādu rindu summa, kurās ir negatīvas summas debitora pasūtījuma apmaiņas laikā. Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
