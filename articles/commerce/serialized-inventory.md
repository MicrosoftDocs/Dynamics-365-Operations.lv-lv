---
title: Pārdošanas punkta (POS) uzlabojumi serializētām precēm
description: Šajā rakstā ir uzskaitīti uzlabojumi, kas veikti serializētām precēm, lai palīdzētu jums ietaupīt laiku un būt produktīvākām.
author: ShalabhjainMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 58252279a625bbdaac7192d1e6e538b9b1fd89ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890299"
---
# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Pārdošanas punkta (POS) uzlabojumi serializētām precēm

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Pārskats

Pamatojoties uz iestatījumiem programmā Commerce Headquarters, preces var klasificēt kā serializētas vai neserializētas. Ja preces ir serializētas, tad katram krājumam var piešķirt unikālu numuru, kas palīdz sekot līdzi garantijām, izsekot krājumus un apstiprināt īpašumtiesības. Lai gan spēja serializētām precēm piešķirt sērijas numurus pastāvēja jau mūsu Modern/Mākoņa pārdošanas punktā (Point of Sale — POS), ir pievienoti daži uzlabojumi, lai palīdzētu kasieriem ietaupītu laiku un strādāt produktīvāk.

## <a name="pos-improvements"></a>POS uzlabojumi

- **Pirms norēķināšanās sērijas numuri nav nepieciešami** — iepriekš kasierim, kurš transakcijai pievienoja serializētu preci, bija jānorāda sērijas numurs. Šī prasība radīja problēmas tādos klientu apkalpošanas scenārijos, kad kasieriem un pārdevējam bija iespēja veikt preču papildu pārdošanu. Līdz maksājuma darbībai preces grozā bieži vien tika atjauninātas. Tāpēc katru reizi, kad kasieris pievienoja jaunu preci, sistēma kasierim prasīja norādīt sērijas numuru. Sērijas numura dialoglodziņā tagad ir poga **Pievienot vēlāk**. Tādēļ pārdevēji var krājumu pievienot transakcijai, bet krājuma sērijas numuru var norādīt vēlāk. Pārdevēji var ātri pievienot un aizstāt grozā esošos serializētos krājumus, un pēc tam sērijas numuru norādīt tieši pirms norēķināšanās. Ja kādai serializētajai precei sērijas numurs nav norādīts, tad kasierim, kas mēģina pabeidziet transakciju, tiek parādīts kļūdas ziņojums. Tas ziņo, ka kasierim pirms turpināšanas ir jānorāda trūkstošie sērijas numuri.

    Katram serializētajam krājumam, kura sērijas numurs tika izlaists, zem transakcijas rindas tiek parādīts komentārs. Šis komentārs ziņo, ka krājumam nav norādīts sērijas numurs. Tāpēc kasieris var ātri atrast krājumus, kuriem trūkst sērijas numuru.

    Jauna operācija **Pievienot sērijas numuru** arī nodrošina sērijas numuru tādiem krājumiem, kam sērijas numuru trūkst. Kad sērijas numurs ir norādīts, to nevar rediģēt. Kasierim ir nepieciešams anulēt rindu un pievienot preci vēlreiz.
    
- **Klientu pasūtījumu veikšanai sērijas numuri nav nepieciešami** — klientu pasūtījumus var veikt vienā veikalā un izpildīt no cita veikala. Kasierim, kurš veic klienta pasūtījumu, sērijas numurs nav jānorāda. Sērijas numurs tiks norādīts izdošanas vai savākšanas darbības laikā. Taču sērijas numurs ir jānorāda visiem rindu krājumiem, kuriem ir atlasīts piegādes tips **Iznest**. Pretējā gadījumā transakciju nevar pabeigt.
- **Serializētās preces transakcijas ekrānā nav apkopotas** — lapas **Funkcionalitātes profils** lauku grupas **Terminālis** iestatījums **Apkopot preces** jums ļauj transakcijas ekrānā apkopot vienādās neserializētās preces. Ja vienādās preces tiek apkopotas, transakciju režģī tās ir vienkāršāk redzamas. Taču, tā kā sērijas numuri parasti ir unikāli un pārdevējiem sērijas numuri ir jāievada tikai tad, kad notiek norēķināšanās, iestatījums **Apkopot preces** neattiecas uz serizalizētajām precēm. Tāpēc, ja ir atlasīts iestatījums **Apkopot preces**, serializētās preces transakcijas ekrānā netiks apkopotas.
- **Spēja meklēt žurnālus pēc sērijas numura** — tagad žurnālus var papildus meklēt pēc sērijas numura. Lai to izdarītu, atveriet operāciju “Žurnāli” un programmas joslā nospiediet pogu “Detalizētā meklēšana”. Izmantojot pogu “Pievienot filtru”, filtru var lietot arī sērijas numuru meklēšanai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]