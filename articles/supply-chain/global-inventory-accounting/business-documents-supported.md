---
title: Biznesa dokumenti, ko atbalsta Globālā krājumu uzskaite
description: Šajā tēmā uzskaitīti biznesa dokumenti, kurus atbalsta Globālā krājumu uzskaite. Tajā sniegts arī detalizēts piemērs par pirkšanas pasūtījuma dokumentiem.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 44081be35c6737aa0d16b6e11a5fc8f94b41e872
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674454"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Biznesa dokumenti, ko atbalsta Globālā krājumu uzskaite

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Kad Globālās krājumu uzskaites pievienojumprogramma ir pilnībā iestatīta, tā ir gatava apstrādāt ar krājumiem saistītos dokumentus, kas tiek ievadīti programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Atbalstītie biznesa dokumenti

Ir divu veidu biznesa dokumenti:

- **Dokumenti, kuriem ir žurnāls** – šie dokumenti ietver produktu ieejas plūsmu, pirkšanas rēķinu, pavadzīmi un pārdošanas rēķina dokumentus.
- **Dokumenti, kuriem nav žurnāla** - šie dokumenti ietver uzskaites, kustības un krājumu korekciju dokumentus.

Vēlāk šajā tēmā pirkšanas pasūtījumi tiks izmantoti kā piemērs procesa ilustrēšanai.

Šajā tabulā uzskaitīti dokumenti, kurus atbalsta pašreizējais laidiens.

| Dokumenta tips      | Attaisnoj. dokuments        |
|--------------------|-----------------|
| Pirkuma pasūtījums     | Produkta saņemšana |
| Pirkuma pasūtījums     | Rēķins         |
| Pārdošanas pasūtījums        | Pavadzīme    |
| Pārdošanas pasūtījums        | Rēķins         |
| Krājumu žurnāli | Kustība        |
| Krājumu žurnāli | Pielāgojums      |
| Krājumu žurnāli | Inventarizācija        |
| Krājumu žurnāli | Pārnesums        |
| Pārsūtīšanas pasūtījums     | Krava        |
| Pārsūtīšanas pasūtījums     | Saņemt         |

> [!IMPORTANT]
> Globālā krājumu uzskaite asinhroni apstrādā dokumentus, kas ir ievadīti Supply Chain Management. Attiecībā uz problemātiskajiem dokumentiem netiek rādīts neviens kļūdas ziņojums.

## <a name="example-purchase-order"></a>Piemērs: Pirkšanas pasūtījums

### <a name="product-receipt"></a>Produktu saņemšana

Grāmatojiet produktu ieejas plūsmas kā parasti. Lapā **Visi pirkšanas pasūtījumi** atlasiet pirkšanas pasūtījumu un pēc tam darbību rūtī cilnē **Saņemt** atlasiet **Produktu ieejas plūsma**, lai atvērtu lapu **Produktu ieejas plūsmas žurnāls**. Katrai rindai tiek ģenerēts operācijas notikums un Globālās krājumu uzskaites notikums. Tāpēc atlasiet cilni **Rindas** un pēc tam atlasiet **Krājumi \> Notikumi un mērījumi**, lai atvērtu lapu **Notikumi un mērījumi**.

Globālā krājumu uzskaite ir grāmatvedības sistēma, kas ir balstīta uz notikumiem un mērījumiem. Mērījumu rindas režģis lapā **Notikumi un mērījumi** rāda mērījumu sarakstu. Katram mērījumam ir dimensiju saraksts.

Katram operācijas notikumam ir divi mērījumu tipi:

- **Operāciju mērījumi** – šie mērījumi raksturo biznesa dokumentus vispārējos nosacījumos. Viens mērījums ir preču daudzums, izmantojot dokumentā izmantoto mērvienību. Ir arī mērījumi, kas ietekmē krājumu vērtību, piemēram, paplašinātā cena, atlaide, atlaides procenti un rindas maksa.
- **Resursu uzskaites mērījumi** – šie mērījumi ir no krājumu reģistra perspektīvas. Tajos ir aprakstīta dokumenta ietekme uz krājumiem krājumu mērvienībā. Ja ir vairākas krājumu reģistrācijas, ir vairākas resursu uzskaites mērījumu rindas.

Dimensijas ir organizētas šādā veidā:

- **Dualitāte** – dualitāte apraksta aģentus, kas piedalās ekonomiskos notikumos. Ārējiem biznesa dokumentiem primālās dimensijas apraksta juridisko personu, kur dokuments tiek ievadīts, turpretim dubultās dimensijas apraksta kreditoru, debitoru utt. Iekšējiem biznesa dokumentiem (piemēram, pārsūtīšanas pasūtījumiem) duālās dimensijās ir aprakstīta partnerpreču noliktava.
- **Dimensijas tips** – dimensijas tiek iedalītas kategorijās.
- **Dimansija** - dimensijas nosaukums.
- **Dimansijas vērtība** - dimensijas vērtiba.

### <a name="global-inventory-accounting-event"></a>Globālās krājumu uzskaites notikums

Globālā krājumu uzskaite kā ievadi paņem darbības notikumus un mērījumus. Pēc tam tiek veikta atbilstoša uzskaite katrai saistītajai Virsgrāmatai, pamatojoties uz pievienoto valūtu un konvenciju. Varat atlasīt **Globālās krājumu uzskaites notikumus un mērījumus**, lai skatītu Globālās krājumu uzskaites notikumu. Globālās krājumu uzskaites notikums seko tai pašai metodoloģijai kā operāciju notikumi, bet tas izmanto dažādus mērījumus. Ir trīs galvenie mērījumu tipi: preces izmaksu daudzums, preces izmaksas un novirze.

Apakšgrāmatas kontus izmanto, lai tālāk klasificētu mērījumus. Var būt vairākas Virsgrāmatas. Šīs Virsgrāmatas ir saistītas ar juridisko personu, kur dokuments ir ievadīts. Notikumus un mērījumus katrai Virsgrāmatai var skatīt, mainot lauka **Virsgrāmata** vērtību.

### <a name="cost-element"></a>Izmaksu elements

Pamatojoties uz izmaksu elementu politiku, kas ir pievienota Virsgrāmatai, sistēma piešķir izmaksu elementu katram iegrāmatotā operācijas notikuma mērījumam, kas ietekmē krājumu izmaksas. Šie mērījumi ietver paplašinātās cenas, atlaides, atlaides procentus un rindas maksas.

### <a name="measurement-line-details"></a>Mērījumu līnijas informācija

Cilne **Pārskats** parāda pievienoto politiku informāciju. Izmaksu objektu dimensijas rāda izmaksu objektu, pamatojoties uz izmaksu objektu politiku. Īpašas identifikācijas dimensijas rāda partijas numuru, ja izmaksu plūsmas pieņēmums ir *Specifisks — partija*.

### <a name="purchase-invoice"></a>Pirkšanas rēķins

Grāmatojiet rēķinu kā parasti. Pēc tam Darbību rūtī cilnē **Rēķins**, grupā **Žurnāli** atlasiet **Rēķins**, lai atvērtu rēķinu žurnālu. Katrai rindai tiek ģenerēts operācijas notikums un Globālās krājumu uzskaites notikums. Tāpēc atlasiet cilni **Rindas** un pēc tam atlasiet **Krājumi \> Notikumi un mērījumi**, lai atvērtu lapu **Notikumi un mērījumi**. Lapa **Notikumi un mērījumi** parāda to pašu mērījumu tipu. Tomēr, tā kā lapā ir parādīta atšķirīga mērījumu loma un mērvienības modifikators, ietekme uz aģentu (juridisku personu) atšķiras.

Atlasiet **Globālās krājumu uzskaites notikumus un mērījumus**, lai skatītu Globālās krājumu uzskaites notikumu. Krājumu daudzums un izmaksas, kas tagad izplūst no apakšgrāmatas konta *Saņemtās preces, kurām nav izrakstīts rēķins* uz apakšgrāmatas kontu *Iegādāto preču izmaksas*.
