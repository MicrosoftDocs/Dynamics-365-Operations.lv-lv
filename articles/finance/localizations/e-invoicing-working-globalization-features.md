---
title: Globalizācijas funkcionalitātes komponenti
description: Šajā tēmā sniegts pārskats par globalizācijas līdzekļu komponentiem.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 87d7dd231b9ccda7761c91f129659c18039f3299
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371962"
---
# <a name="globalization-feature-components"></a>Globalizācijas funkcionalitātes komponenti

[!include [banner](../includes/banner.md)]

Globalizācijas līdzeklis ir komponentu kopa, kas nosaka noteikumus datu pārvēršanai elektronisko pārskatu (ER) konfigurācijās. Šie komponenti ietver norādījumus par elektronisko dokumentu apstrādi un pēc tam to nosūtīšanu uz ārējiem kanāliem vai saņemšanu no tiem. Tās ietver arī nosacījumus, kas nosaka, kad funkcija darbojas ienākošajiem biznesa datiem.

Visi komponenti ir atkarīgi viens no otra. Globalizācijas funkcijas ļauj viegli izveidot un uzturēt šo atkarību, kā arī atbalstīt komponentu kopas dzīves cikla pārvaldību un versiju šanu.

## <a name="access-electronic-invoicing-feature-components"></a>Piekļuve elektronisko rēķinu izrakstīšanas funkcijas komponentiem 

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.

    Globalizācijas līdzekļiem ir vairāki komponenti. Elektronisko **rēķinu izrakstīšanas funkciju** lapa ietver atsevišķu cilni katram komponentam.

    - **Versija** — šis komponents atbalsta funkcijas dzīves cikla pārvaldību. To var izmantot, lai pārvaldītu dažādu funkcionalitātes versiju statusu.
    - **Konfigurācijas – šis komponents** ļauj pārvaldīt, skatīt un rediģēt saistīto ER formātu un formātu kartēšanas konfigurācijas, kas tiek izmantotas apstrādes konveijerā.
    - **Iestatījumi** — šis komponents ļauj globalizācijas pakalpojumu lietotājiem, piemēram, e-rēķinu pakalpojumam, pārvaldīt saistītā līdzekļa versijas iestatīšanu. Tādēļ tas atbalsta elastīgu komunikācijas uzbūvi un atbildes noteikumus.
    - **Vides – šis komponents ļauj globalizācijas** pakalpojumu lietotājiem, piemēram, e-rēķinu izrakstīšanas pakalpojumam, pārvaldīt vidi, kur tiek izmantota funkcijas versijas iestatīšana. Tas arī ļauj tiem piešķirt autorizāciju lietotājiem, kuriem būs piekļuve līdzekļa versijas iestatījumam.
    - **Organizācijas – šis komponents** ļauj lietotājiem koplietot šo līdzekli ar ārējām organizācijām.
    - **Tagi** - šis komponents ļauj jums etiķetes funkcijas, ko var izmantot globalizācijas zilā izdrukā atsaucei.
