---
title: "Pārdošanas punkta (POS) uzlabojumi serializētām precēm"
description: "Šajā tēmā ir uzskaitīti uzlabojumi, kas ir ieviesti serializētām precēm, lai jums palīdzētu ietaupīt laiku un strādāt produktīvāk."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 17cd46ba9ee972c92db8950eea1cd258d67c2e92
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Pārdošanas punkta (POS) uzlabojumi serializētām precēm

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Pārskats

Pamatojoties uz iestatījumiem programmā Retail Headquarters, preces var klasificēt kā serializētas vai neserializētas. Ja preces ir serializētas, tad katram krājumam var piešķirt unikālu numuru, kas palīdz sekot līdzi garantijām, izsekot krājumus un apstiprināt īpašumtiesības. Lai gan spēja serializētām precēm piešķirt sērijas numurus pastāvēja jau mūsu Modern/Mākoņa pārdošanas punktā (Point of Sale — POS), ir pievienoti daži uzlabojumi, lai palīdzētu kasieriem ietaupītu laiku un strādāt produktīvāk.

## <a name="pos-improvements"></a>POS uzlabojumi

- **Pirms norēķināšanās sērijas numuri nav nepieciešami** — iepriekš kasierim, kurš transakcijai pievienoja serializētu preci, bija jānorāda sērijas numurs. Šī prasība radīja problēmas tādos klientu apkalpošanas scenārijos, kad kasieriem un pārdevējam bija iespēja veikt preču papildu pārdošanu. Līdz maksājuma darbībai preces grozā bieži vien tika atjauninātas. Tāpēc katru reizi, kad kasieris pievienoja jaunu preci, sistēma viņam vai viņai prasīja norādīt sērijas numuru. Sērijas numura dialoglodziņā tagad ir poga **Pievienot vēlāk**. Tādēļ pārdevēji var krājumu pievienot transakcijai, bet krājuma sērijas numuru var norādīt vēlāk. Pārdevēji var ātri pievienot un aizstāt grozā esošos serializētos krājumus, un pēc tam sērijas numuru norādīt tieši pirms norēķināšanās. Ja kādai serializētajai precei sērijas numurs nav norādīts, tad kasierim, kas mēģina pabeidziet transakciju, tiek parādīts kļūdas ziņojums. Tas ziņo, ka kasierim pirms turpināšanas ir jānorāda trūkstošie sērijas numuri.

    Katram serializētajam krājumam, kura sērijas numurs tika izlaists, zem transakcijas rindas tiek parādīts komentārs. Šis komentārs ziņo, ka krājumam nav norādīts sērijas numurs. Tāpēc kasieris var ātri atrast krājumus, kuriem trūkst sērijas numuru.

    Jauna operācija **Pievienot sērijas numuru** arī nodrošina sērijas numuru tādiem krājumiem, kam sērijas numuru trūkst. Kad sērijas numurs ir norādīts, to nevar rediģēt. Kasierim ir nepieciešams anulēt rindu un pievienot preci vēlreiz.
    
- **Klientu pasūtījumu veikšanai sērijas numuri nav nepieciešami** — klientu pasūtījumus var veikt vienā veikalā un izpildīt no cita veikala. Kasierim, kurš veic klienta pasūtījumu, sērijas numurs nav jānorāda. Sērijas numurs tiks norādīts izdošanas vai savākšanas darbības laikā. Taču sērijas numurs ir jānorāda visiem rindu krājumiem, kuriem ir atlasīts piegādes tips **Iznest**. Pretējā gadījumā transakciju nevar pabeigt.
- **Serializētās preces transakcijas ekrānā nav apkopotas** — lapas **Funkcionalitātes profils** lauku grupas **Terminālis** iestatījums **Apkopot preces** jums ļauj transakcijas ekrānā apkopot vienādās neserializētās preces. Ja vienādās preces tiek apkopotas, transakciju režģī tās ir vienkāršāk redzamas. Taču, tā kā sērijas numuri parasti ir unikāli un pārdevējiem sērijas numuri ir jāievada tikai tad, kad notiek norēķināšanās, iestatījums **Apkopot preces** neattiecas uz serizalizētajām precēm. Tāpēc, ja ir atlasīts iestatījums **Apkopot preces**, serializētās preces transakcijas ekrānā netiks apkopotas.
- **Spēja meklēt žurnālus pēc sērijas numura** — tagad žurnālus var papildus meklēt pēc sērijas numura. Lai to izdarītu, atveriet operāciju “Žurnāli” un programmas joslā nospiediet pogu “Detalizētā meklēšana”. Izmantojot pogu “Pievienot filtru”, filtru var lietot arī sērijas numuru meklēšanai.

