---
title: Piegādes veida mainīšana punktā POS
description: Šajā rakstā ir aprakstīts, kā konfigurēt un izmantot piegādes maiņas operāciju sistēmā POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855825"
---
# <a name="change-mode-of-delivery-in-pos"></a>Piegādes veida mainīšana punktā POS

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārdošanas punkta (POS) vidē iestatīt un izmantot funkcionalitāti "mainīt piegādes režīmu". 

Dynamics 365 Commerce versijās 10.0.10 un jaunākās versijās **Mainīt piegādes veidu** operācijas (647) ir pieejamas pievienošanai jūsu POS ekrāna izkārtojumiem.

Piegādes līdzekļa maiņas veids sniedz iespēju mainīt piegādes veidu vienai vai vairākām pārdošanas rindām, kas konfigurētas POS darbībā. Iepriekšējās Commerce versijas jums bija jāiziet cauri pilnām **Nosūtīt visus** vai **Nosūtīt atlasītās** konfigurācijas plūsmām, ja vēlējāties mainīt piegādes veidu esošajā rindā, kas tika konfigurēta nosūtīšanai. Šis process bija laikietilpīgs, un tas varēja izraisīt nejaušas izmaiņas šīs rindas piegādājamo preču izcelsmes vai saņemšanas datumā. Jaunā funkcionalitāte sniedz alternatīvu metodi, kā efektīvi atjaunināt piegādes veidu šajās pārdošanas rindās.

Lai iegūtu vairāk informācijas par to, kā pievienot operāciju pogai, kas atrodas POS pogu režģī, skatiet [Pārdošanas punkta ekrāna izkārtojumus](pos-screen-layouts.md).

Pēc tam, kad šī funkcija ir konfigurēta POS, kad atlasāt **Mainīt piegādes veidu**, jums tiks parādīta saraksta lapa, kas ļaus izvēlēties darbības rindas, kurām vēlaties mainīt piegādes veidu. Varat izvēlēties dažas vai visas rindas vai iziet, neveicot nekādas izmaiņas. Pārdošanas rindas, kas iepriekš konfigurētas sūtījumam, ir vienīgās rindas sarakstā, ko varat mainīt. Ja vēlaties mainīt rindu, kas paredzēta izsniegšanai vai uzkrājuma sūtīšanai, ir jāizmanto **Nosūtīt visas** vai **Nosūtīt atlasītās** darbības. Pretējā gadījumā, ja vēlaties mainīt rindu, kas norādīta kā sūtījums uz saņemšanu vai realizēšanu, ir jāizmanto visas darbības **Saņemt visas**, **Saņemt atlasītās**, **Realizēt visas** vai **Realizēt atlasītās**.

Pēc tam, kad atlasāt rindas, kuras vēlaties mainīt, noklikšķiniet uz **Mainīt piegādes veidu**, lai tiktu piedāvāts izvēlēties piegādes veida opcijas. Ja atlasījāt vairākas rindas, ko mainīt, punktā POS tiek rādīti tikai piegādes veidi, kas ir konfigurēti kā atļaujami visām atlasītajām precēm. Piegādes veidus var konfigurēt, lai atbalstītu noteiktas preces un piegādes adreses. Ja ir piegādes veids, kas ir pieņemams vienai precei un adreses kombinācijai, bet nav pieņemams citai izvēlētai preces un adreses kombinācijai, piegādes veids nav pieejams. Pastāv iespēja, ka rindas jāizvēlas pa vienai, un katrai rindai jāmaina piegādes veids, ja vēlaties atlasīt piegādes veidu vienai precei, ko neatbalsta cita prece.  

Pēc jauna piegādes veida atlases tiek parādīta transakciju lapa. Lai pārskatītu jaunās piegādes veida atlases, atlasiet cilni **Piegāde** transakciju sarakstā.

## <a name="additional-resources"></a>Papildu resursi

[Zvanu centra pasūtījumu izveide](tasks/create-call-center-orders.md)

[Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]