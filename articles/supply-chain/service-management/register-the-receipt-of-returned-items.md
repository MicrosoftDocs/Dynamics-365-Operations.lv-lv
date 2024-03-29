---
title: Atgrieztu krājumu saņemšanas reģistrēšana
description: Atgrieztu krājumu saņemšanu varat reģistrēt, izmantojot veidlapu Saņemšanas apskats vai veidlapu Reģistrācija.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4942e455350844ac5614e70fef21b37461540a6
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017294"
---
# <a name="register-the-receipt-of-returned-items"></a>Atgrieztu krājumu saņemšanas reģistrēšana 

[!include [banner](../includes/banner.md)]


Pastāv divas metodes atgriezto krājumu saņemšanas reģistrācijai. Pirmā metode ir noliktavas saņemšanas process, kas izmanto veidlapu **Saņemšanas apskats**. Otrā metode paredz veidlapas **Reģistrācija** izmantošanu.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Atgriezto krājumu saņemšanas reģistrēšana formā Saņemšanas transakciju apskats

Varat izmantot veidlapu **Saņemšanas apskats**, lai atgriešanas sūtījumu identificētu pēc tā atgrieztā krājuma autorizācijas (AKA) koda. Ja ir definēts žurnāla nosaukums cilnē **Iestatījumi** un ir žurnāla rindas, kas atbilst veidlapā **Saņemšanas apskats** atlasītajām rindām, tiek izveidots jauns žurnāla virsraksts, kad noklikšķināt uz **Sākt saņemšanu**.

1.  Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Saņemšanas pārskats**.

2.  Laukā **Iestatījumu nosaukums** atlasiet **Atgriešanas pasūtījums** un pēc tam noklikšķiniet uz **Atjaunināt**.
    

    > [!TIP]
    > <P>Varat izmantot laukus <STRONG>Diapazons</STRONG>, lai sašaurinātu meklēšanas rezultātus. Varat ierakstīt izvēlētos AKA kodu laukā <STRONG>AKA kods</STRONG>, lai iegūtu precīzu rezultātu. Lai noteiktu un saglabātu filtru kopu, kas ierobežo to, kuras ienākošās saņemšanas tiek parādītas, noklikšķiniet uz cilnes <STRONG>Iestatījumi</STRONG>. Pieejamo filtru klāstā ietilpst tipi, noliktavas un doki.</P>

    

    > [!WARNING]
    > <P>Atgrieztos pasūtījumus nedrīkst jaukt ar citiem saņemšanas tipiem veidlapā <STRONG>Saņemšanas apskats</STRONG>. Tāpēc atsauce vienmēr būs pārdošanas pasūtījums, bet iztrūkstošs pārdošanas pasūtījuma ID tiks norādīts žurnāla virsrakstā.</P>



3.  Režģī **Ieejas plūsmas** atrodiet rindu, kas atbilst atgrieztajam krājumam, un pēc tam atzīmējiet izvēles rūtiņu kolonnā **Atlasīt saņemšanai**.

4.  Lai izņemtu noteiktas rindas no atgriezto preču saņemšanas pavadzīmes, piemēram, krājumus no oriģinālā pasūtījuma, kas nebija iekļauti atgrieztajā sūtījumā, noņemiet atzīmes no saistītām izvēles rūtiņām **Atlasīt saņemšanai** tabulā **Rindas** veidlapas apakšdaļā.

5.  Noklikšķiniet uz pogas **Sākt saņemšanu**, lai izveidotu saņemšanas žurnālu.
    

    > [!NOTE]
    > <P>Varat izvēlēties vairākus atgriešanas pasūtījumus un iekļaut tos vienā saņemšanas procesā. Katra atgriešanas pasūtījuma rinda tiks pārkopēta uz atbilstošu vienības pienākšanas žurnāla rindā.</P>

    

    > [!NOTE]
    > <P>Saņemšanas žurnālu varat veidot arī manuāli, izmantojot veidlapu <STRONG>Krājumu saņemšana</STRONG>. 



6.  Noklikšķiniet uz **Krājumu vadība** \> **Žurnāli** \> **Krājumu saņemšana** \> **Krājumu saņemšana**.

7.  Atlasiet tikko izveidoto saņemšanas žurnālu un pēc tam noklikšķiniet uz **Rindas**, lai atvērtu veidlapu **Žurnāla rindas, vietas**.

8.  Cilnē **Vispārīgi** pielāgojiet skaitli laukā **Daudzums**, ja nepieciešams, un pēc tam piešķiriet atgriešanas metodes kodu laukā **Atgriešanas metodes kods**.
    
    Varat arī atzīmēt izvēles rūtiņu **Karantīnas pārraudzība**, lai atgrieztie krājumi tiktu nosūtīti caur pārbaudes procesu karantīnas pasūtījuma kontekstā.
    

    > [!NOTE]
    > <P>Ja atgrieztos krājumus sūtāt caur karantīnu, atgriešanas metodes kodu nevar norādīt.</P>



9.  Noklikšķiniet uz pogas **Validēt**.

10. Ja apstiprināšanas procesā nav kļūdu, noklikšķiniet uz **Grāmatot**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Atgriezto krājumu saņemšanas reģistrēšana formā Reģistrācija

Kā alternatīvu veidlapas **Saņemšanas apskats** izmantošanai varat izmantot veidlapu **Reģistrācija**, lai reģistrētu atgriezto krājumu saņemšanu.

1.  Noklikšķiniet **uz Pārdošanas un mārketinga** \> **pārdoto preču atgriešanas visi** \> **atgriešanas pasūtījumi**. Izveidojiet jaunu atgriešanas pasūtījumu vai atveriet atgriešanas pasūtījumu no saraksta. Kopsavilkuma cilnē **Rindas** atlasiet atgriešanas pasūtījuma rindu. Noklikšķiniet uz **Atjaunināt rindu** un pēc tam noklikšķiniet uz **Reģistrācija**.

2.  Piešķiriet atgriešanas metodes kodu laukā **Atgriešanas metodes kods** un tad noklikšķiniet uz **Labi**.
    

    > [!NOTE]
    > <P>Izmantojot veidlapu <STRONG>Reģistrācija</STRONG>, krājumu nav iespējams nosūtīt pārbaudei kā karantīnas pasūtījumu.</P>



3.  Režģī **Darbības** atlasiet reģistrējamo darījumu.

4.  Režģī **Reģistrēt tagad** noklikšķiniet uz **Pievienot**. Atkārtojiet iepriekšējās divas darbības, līdz visi atgrieztie krājumi ir redzami režģī **Reģistrēt tagad**.

5.  Noklikšķiniet uz **Grāmatot**.

## <a name="see-also"></a>Skatiet arī

[Ieņēmumu apskats (forma)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]