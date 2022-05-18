---
title: Grāmatu skaits katrā žurnālā
description: Šī tēma apraksta attiecības starp žurnāliem un līdzekļu grāmatām, kad, izmantojot pakešuzdevumu, izveidojat pamatlīdzekļa iegādes vai nolietojuma priekšlikumu. Varat definēt maksimālo grāmatu skaitu, kas ir iekļautas katrai iegādei un nolietojumam.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1e37d40c30d784eea5ba097447f2b2e69920830a
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722385"
---
# <a name="number-of-books-per-journal"></a>Grāmatu skaits katrā žurnālā

[!include [banner](../includes/banner.md)]

Šī tēma apraksta attiecības starp žurnāliem un līdzekļu grāmatām, kad, izmantojot pakešuzdevumu, izveidojat pamatlīdzekļa iegādes vai nolietojuma priekšlikumu. Varat definēt maksimālo grāmatu skaitu, kas ir iekļautas katrai iegādei un nolietojumam, izmantojot laukus sadaļā **Grāmatu skaits žurnālā**, cilnē **Vispārīgi**, kas atrodama lapā **Parametri** (**Pamatlīdzekļi \> Iestatījumi \> Pamatlīdzekļu iestatījumi**). Šie lauki ļauj jums sadalīt pamatlīdzekļu grāmatu skaitu uz iegādes žurnālu un nolietojuma žurnālu.

Iegādes priekšlikumam noklusētā vērtība ir vismaz 10 000 grāmatas. Nolietojuma priekšlikumam noklusētā vērtība ir vismaz 2000 grāmatas.

Piemēram, ja ir 4000 pamatlīdzekļi un ar katru pamatlīdzekli ir saistītas divas grāmatas, viena grāmata tiks grāmatota pašreizējā slānī, un cita grāmata tiks grāmatota nodokļa slānī. Ja iegūstat 4000 pamatlīdzekļus, izmantojot pakešapstrādi, pakešuzdevums, kas izveido vienu pamatlīdzekļu iegādes žurnālu, ietver 4000 līdzekļu grāmatu.

> [!NOTE]
> Izveidotais žurnāls tiks izmantots, līdz pakešuzdevums būs pabeigts.
>
> Atvasinātās grāmatas nav iekļautas maksimālajā grāmatu skaitā žurnālam.

Varat izmantot pakešapstrādi, lai izpildītu nolietojumu tai pašai iegūto līdzekļu kopai. Piemēram, pakešuzdevums izveido divus nolietojuma žurnālus, katrs no tiem ietver 2000 līdzekļu grāmatu. Pirmajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 1 līdz 2000. Otrajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 2001 līdz 4000.

Pakešapstrādes darbs izslēdz slēgtās grāmatas. Piemēram, nolietojuma pakešuzdevumā ir slēgtas 10 no pirmajām 2000 grāmatām ir slēgtas. Pirmajā gadījumā pirmajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 1 līdz 2011. Otrajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 2012 līdz 4000.

> [!NOTE]
> Ja jums ir pamatlīdzekļu ID ar dažādiem atdalītājiem (piemēram, – vai/) un pakešuzdevumos veidojat pamatlīdzekļu darbības, katram atdalītāja tipam ir jāpalaiž atsevišķs pakešuzdevums. Sistēma nevar apstrādāt dažādus atdalītājus vienā pakešuzdevumā.

Grāmatu skaita ierobežojums tiek pielietots, ja tajā pašā žurnālā neeksistē pamatlīdzekļu ID dublikāti. Tomēr, ja pamatlīdzekļa ID ir tas pats, kas grāmatas ID, žurnāla grāmatu skaits var tikt pārsniegts, lai saglabātu pamatlīdzekļa ID tajā pašā žurnālā.

Piemēram, ir 5001 pamatlīdzekļu ID, trīs grāmatas ir saistītas ar katru pamatlīdzekļa ID, un katra pamatlīdzekļu grāmata tiek grāmatota vienā grāmatošanas līmenī. Nolietojums tiek izpildīts trīs mēnešus pēc kārtas bez summēšanas.  Nolietojuma žurnāls tiks izveidots, izmantojot pakešuzdevumu, un sistēma izveidos septiņus žurnālus, kuriem ir 667 pamatlīdzekļu ID un trīs grāmatas katram pamatlīdzekļa ID. Rezultāts būs 2001 grāmata. Tāpēc trijos mēnešos būs 6003 žurnāla rindas, lai tajā pašā žurnālā uzturētu tos pašus pamatlīdzekļu ID. Sistēmā tiks izveidots arī viens žurnāls, kurā ir 332 pamatlīdzekļu ID un trīs grāmatas katram pamatlīdzekļa ID. Trijos mēnešos būs 2988 rindas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
