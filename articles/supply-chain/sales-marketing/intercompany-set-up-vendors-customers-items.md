---
title: Kreditoru, debitoru un krājumu iestatīšana starpuzņēmumu tirdzniecībai
description: Šis raksts skaidro, kā iestatīt kreditorus, debitorus un krājumus starpuzņēmumu tirdzniecībai
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3e1eb7b8673f3af682204b65b33a1d8b61742721
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675042"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Kreditoru, debitoru un krājumu iestatīšana starpuzņēmumu tirdzniecībai

[!include [banner](../../includes/banner.md)]

Lai sagatavotu organizāciju starpuzņēmumu tirdzniecībai, jānorāda kreditori un debitori, ar kuriem jūs tiksiet tirgoti iekšēji. Pēc tam šie kreditori un debitori ir jāsaista ar krājumiem, kas tiks pirkti vai pārdoti.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**.
1. Atlasiet kreditoru, lai definētu kā starpuzņēmumu kreditoru.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Norādiet starpuzņēmumu iestatījuma parametrus kreditora kontam. Šie parametri ietver debitora juridisko personu un kontu, pārdošanas pasūtījumu politikas, pirkšanas pasūtījumu politikas, vērtību kartēšanu un pirkšanas līgumu un pārdošanas līgumu politikas. Norādiet arī, vai izmantot bāzes datu vērtības no kreditora konta vai no debitora konta citā juridiskajā personā.
1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Saraksta lapā **Izlaistās preces** atlasiet krājumus, ko piešķirt kreditoram, lai krājumi būtu pieejami starpuzņēmumu tirdzniecībai. Atveriet lapu **Detalizēta informācija par izlaistajām precēm** katram krājumam. Cilnes **Pirkšana** laukā **Kreditors** ierakstiet kreditora kodu.
1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atlasiet kreditoru, lai definētu kā starpuzņēmumu kreditoru.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Norādiet starpuzņēmumu iestatījuma parametrus debitora kontam. Šie parametri ietver kreditora juridisko personu un kontu, pirkšanas pasūtījumu politikas, pārdošanas pasūtījumu politikas, vērtību kartēšanu un pārdošanas līgumu un pirkšanas līgumu politikas. Varat arī norādīt, vai izmantot bāzes datu vērtības no debitora konta vai no kreditora konta citā juridiskajā personā.
1. **Debitoru** lapas kopsavilkuma cilnē **Rēķins un piegāde** atzīmējiet izvēles rūtiņu **Izveidot starpuzņēmumu pasūtījumus**. Ja vēlaties pasūtījumus piegādāt tieši debitoriem, atzīmējiet izvēles rūtiņu **Tiešā piegāde**.

    > [!NOTE]
    > Ja ir krājumi, ko organizācija uzglabā un piegādā debitoriem, varbūt nevēlaties veidot starpuzņēmumu pasūtījumus automātiski neatkarīgi no tā, vai krājums ir rezervē. Lai deaktivizētu automātisku pasūtījumu izveidi krājumiem, kas reizēm var būt rezervē, noņemiet atzīmi izvēles rūtiņā **Izveidot starpuzņēmuma pasūtījumus**.

1. Ja vēlaties atļaut netieši pārdošanas pasūtījumā izveidot papildu rindas, atzīmējiet izvēles rūtiņu **Izveidot netiešā pasūtījuma rindas**. Tas ļauj lietotājam pievienot rindas sākotnējam pārdošanas pasūtījumam no starpuzņēmumu pārdošanas pasūtījuma.

> [!WARNING]
> Ja atļauta netiešā pasūtījuma rindu izveide, tiek atļauti visi papildinājumi oriģinālajā pārdošanas pasūtījumā no starpuzņēmumu pārdošanas pasūtījuma. Pēc tam katrs papildinājums tiek apstrādāts debitoram un pievienots pasūtījumam un rēķinam. Turklāt katrs pārdošanā iesaistītais dokuments tiek drukāts un grāmatots automātiski. Lietotāji netiek brīdināti par papildinājumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
