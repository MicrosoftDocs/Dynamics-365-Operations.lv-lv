---
title: Debitora darbplūsma
description: Šajā tēmā ir sniegta informācija par debitora darbplūsmu. Jūs maināt noteiktus debitora informācijas laukus un pēc tam, izmantojot darbplūsmu, nosūtāt izmaiņas apstiprināšanai, pirms tās tiek pievienotas debitora informācijai.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5998a492e12cb93aeec029c6e56f811f8b90055a
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459511"
---
# <a name="customer-workflow"></a>Debitora darbplūsma

[!include [banner](../includes/banner.md)]

Šī debitora darbplūsma ir pievienota versijai 8.0.4. Varat mainīt noteiktus debitora informācijas laukus un pēc tam, izmantojot darbplūsmu, nosūtīt izmaiņas apstiprināšanai, pirms tās tiek pievienotas debitora informācijai.

## <a name="set-up-the-customer-workflow"></a>Iestatīt debitora darbplūsmu

Lai varētu izmantot debitora darbplūsmas līdzekli, tas vispirms ir jāiespējo.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
2. Lai iespējotu līdzekli, atveriet cilnes **Vispārīgie iestatījumi** kopsavilkuma cilni **Debitora apstiprinājums** un opcijai **Iespējot klienta apstiprinājumus** iestatiet opciju **Jā**.
3. Laukā **Datu elementa režīms** atlasiet datu elementu vēlamo izturēšanos datu importēšanas brīdī. Ir pieejamas šādas iespējas.

    - **Atļaut izmaiņas bez apstiprinājuma** – elements var atjaunināt klienta ierakstu, neapstrādājot to ar darbplūsmu.
    - **Noraidīt izmaiņas** – klienta ierakstā nevar veikt izmaiņas. Laukos, kam ir iespējota darbplūsma, importēšana neizdosies.
    - **Izveidot izmaiņu priekšlikumus** – tiks mainīti visi lauki, izņemot laukus, kam ir iespējota darbplūsma. Šo lauku jaunās vērtības tiks pievienotas debitora informācijai kā piedāvātās izmaiņas, un tiks automātiski sākta darbplūsma.

4. Pēc tam debitora lauku sarakstā atlasiet izvēles rūtiņu **Iespējot** pie katra lauka, kas jāapstiprina pirms izmaiņu veikšanas.
5. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu darbplūsmas**.
6. Atlasiet **Jauna**.
7. Atlasiet **Piedāvāto klienta izmaiņu darbplūsma**. 
8. Iestatiet darbplūsmu atbilstoši jūsu apstiprināšanas procesam. Izmaiņas tiks piemērotas debitora informācijai, izmantojot darbplūsmas apstiprināšanas elementu **Darbplūsmas apstiprinājums piedāvātajām klienta izmaiņām**.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Debitora informācijas mainīšana un izmaiņu iesniegšana darbplūsmā

Mainot lauku, kam ir iespējota darbplūsma, tiek parādīta lapa **Piedāvātās izmaiņas**. Šajā lapā tiek rādīta lauka sākotnējā vērtība un jūsu ievadītā jaunā vērtība. Jūsu izmainītajam laukam tiek atjaunota sākotnējā vērtība. Lapā tiek parādīts statusa ziņojums, informējot, ka jūsu veiktās izmaiņas nav iesniegtas.

Mainot lauku, kam ir iespējota darbplūsma, attiecīgais lauks katru reizi tiek pievienots piedāvāto izmaiņu sarakstam. Lai atmestu lauka piedāvāto vērtību, izmantojiet pogu **Atmest**, kas sarakstā ir blakus laukam. Lai atmestu visas izmaiņas, izmantojiet pogu **Atmest visas izmaiņas**, kas atrodas lapas apakšā. Atlasiet **Labi**, lai aizvērtu lapu.

Ja ir piedāvātas vismaz vienas izmaiņas, darbību rūtī tiek rādītas divas papildu izvēlnes: **Piedāvātās izmaiņas** un **Darbplūsma**.

1. Lai atvērtu lapu **Piedāvātās izmaiņas** un pārskatītu izmaiņas, atlasiet **Piedāvātās izmaiņas**.
2. Lai iesniegtu izmaiņas darbplūsmā, atlasiet **Darbplūsma \> Iesniegt**.

    Lapas statuss tiek mainīts uz **Izmaiņas, kas gaida apstiprinājumu**.

Darbplūsma atbilst programmas standarta darbplūsmu procesam. Apstiprinātājs tiek virzīts uz lapu **Debitors**, kurā var pārskatīt izmaiņas lapā **Piedāvātās izmaiņas** un pēc tam atlasīt **Darbplūsma \> Apstiprināt**, lai apstiprinātu darbplūsmu. Kad apstiprināšana ir pilnībā pabeigta, lauki tiek atjaunināti atbilstoši jūsu piedāvātajām vērtībām.
