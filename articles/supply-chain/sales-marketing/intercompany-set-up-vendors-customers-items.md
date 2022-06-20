---
title: Kreditoru, debitoru un krājumu iestatīšana starpuzņēmumu tirdzniecībai
description: Šajā rakstā skaidrots, kā iestatīt kreditorus, debitorus un krājumus starpuzņēmumu tirdzniecībai
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
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945760"
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
1. Kad esat pabeidzis starpuzņēmumu parametru iestatīšanu, aizveriet starpuzņēmumu **lapu**, lai atgrieztos atlasītajā debitora papildinformācijā.
1. Izvērsiet kopsavilkuma cilni **Detalizēta informācija par** papildu informāciju un iestatiet izveidot **starpuzņēmumu pasūtījumus uz** *Jā*. Ja vēlaties pasūtījumus piegādāt arī tieši debitoriem, iestatiet tiešo piegādi **uz** Jā *·*.

    > [!NOTE]
    > Ja ir krājumi, ko organizācija uzglabā un piegādā debitoriem, varbūt nevēlaties veidot starpuzņēmumu pasūtījumus automātiski neatkarīgi no tā, vai krājums ir rezervē. Lai dezaktivētu automātisku pasūtījumu ģenerēšanu krājumiem, kas reizēm var būt krājumos, **iestatiet Veidot starpuzņēmumu pasūtījumus uz** *Nē*.

1. Ja vēlaties atļaut netiešu pārdošanas pasūtījumam izveidot papildu rindas, iestatiet netiešā pasūtījuma **rindas uz** Jā *·*. Tas ļauj lietotājam pievienot rindas sākotnējam pārdošanas pasūtījumam no starpuzņēmumu pārdošanas pasūtījuma.

> [!WARNING]
> Ja atļauta netiešā pasūtījuma rindu izveide, tiek atļauti visi papildinājumi oriģinālajā pārdošanas pasūtījumā no starpuzņēmumu pārdošanas pasūtījuma. Pēc tam katrs papildinājums tiek apstrādāts debitoram un pievienots pasūtījumam un rēķinam. Turklāt katrs pārdošanā iesaistītais dokuments tiek drukāts un grāmatots automātiski. Lietotāji netiek brīdināti par papildinājumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
