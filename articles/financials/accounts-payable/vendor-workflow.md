---
title: Kreditora darbplūsma
description: Modificējiet kreditora informāciju un izmantojiet darbplūsmu, lai to apstiprinātu.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 112f9d6adeee583a63da8ab700d7adc179de2c1d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835314"
---
# <a name="vendor-workflow"></a>Kreditora darbplūsma

[!include [banner](../includes/banner.md)]

Izmantojot kreditora darbplūsmu, konkrētos laukos veiktās izmaiņas pirms to pievienošanas kreditoram tiek nosūtītas apstiprināšanai uz darbplūsmu.

## <a name="set-up-the-vendor-workflow"></a>Kreditora darbplūsmas iestatīšana

Jums ir jāiespējo darbplūsmas līdzeklis, lai jūs varētu to izmantot.

1. Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
2. Cilnes **Vispārīgi** kopsavilkuma cilnē **Kreditoru apstiprināšana** iestatiet opcijas **Iespējot kreditoru apstiprināšanas** vērtību **Jā**.
3. Laukā **Datu elementu uzvedība** atlasiet uzvedību, kura ir jāizmanto, importējot datus.

    - **Atļaut izmaiņas bez apstiprinājuma** – datu elements var atjaunināt kreditora ierakstu, neveicot tā apstrādi darbplūsmā.
    - **Noraidīt izmaiņas** – kreditora ierakstam izmaiņas nevar veikt. Importēšana nebūs veiksmīga laukiem, kuri ir iespējoti darbplūsmai.
    - **Izmaiņu piedāvājumu izveide** – visi lauki tiks mainīti, izņemot tos laukus, kuri ir iespējoti darbplūsmai. Šo lauku jaunās vērtības tiks pievienots kreditoram kā piedāvātās izmaiņas, un darbplūsma tiks sākta automātiski.

4. Kreditora lauku sarakstā atlasiet izvēles rūtiņu **Iespējot** katram laukam, kas ir jāapstiprina, lai varētu veikt izmaiņas.
5. Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa darbplūsmas**.
6. Atlasiet **Jauns**.
7. Atlasiet **Piedāvāto kreditora izmaiņu darbplūsma**. 
8. Iestatiet darbplūsmu tā, lai tā atbilstu jūsu apstiprināšanas procesam. Darbplūsmas elements **Darbplūsmas apstiprināšana piedāvātajai kreditora izmaiņai** piemēros izmaiņas kreditoram.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Kreditora informācijas maiņa un izmaiņu iesniegšana darbplūsmā

Mainot lauku, kurš ir iespējots darbplūsmai, tiek parādīta lapa **Piedāvātās izmaiņas**. Šajā lapā tiek rādīta lauka sākotnējā vērtība un jūsu ievadītā jaunā vērtība. Laukā, kurā veicāt izmaiņas, tiek atjaunota tā sākotnējā vērtība. Statusa ziņojums arī informē, ka jūsu veiktās izmaiņas nav iesniegtas. 

Katrreiz, kad maināt lauku, kurš ir iespējots darbplūsmai, šis lauks tiek pievienots sarakstam lapā **Piedāvātās izmaiņas**. Lai atmestu laukam piedāvātās vērtības, izmantojiet pogu **Atmest** pie sarakstā esošā lauka. Lai atmestu visas izmaiņas, izmantojiet pogu **Atmest visas izmaiņas** pogas apakšdaļā. Atlasiet **Labi**, lai aizvērtu lapu.

Ja ir vismaz viena piedāvātā izmaiņa, darbību rūtī tiek rādītas divas papildu cilnes: **Piedāvātās izmaiņas** un **Darbplūsma**.

1. Atlasiet cilni **Piedāvātās izmaiņas**, lai atvērtu lapu **Piedāvātās izmaiņas**, un pārskatiet veiktās izmaiņas.
2. Atlasiet cilni **Darbplūsma \> Iesniegt, lai iesniegtu izmaiņas darbplūsmā**.

    Lapas statuss tiek mainīts uz **Izmaiņas, kas gaida apstiprinājumu**.

Darbplūsma atbilst standarta darbplūsmas procesam sistēmā Microsoft Dynamics 365 for Finance and Operations. Apstiprinātājs tiek novirzīts uz lapu **Kreditors**, kurā viņš vai viņa var pārskatīt izmaiņas lapā **Piedāvātās izmaiņas** lapu un pēc tam atlasīt cilni **Darbplūsma \>Apstiprināt**, lai apstiprinātu darbplūsmu. Kad apstiprināšana ir pilnībā pabeigta, lauki tiek atjaunināti atbilstoši jūsu piedāvātajām vērtībām.
