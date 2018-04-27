---
title: "Apskats par debitoru pasūtījumiem"
description: "Šajā tēmā ir sniegta informācija par debitoru pasūtījumiem pārdošanas punktā Retail Modern POS (MPOS). Debitoru pasūtījumi tiek saukti arī par īpašajiem pasūtījumiem. Šajā tēmā ir iekļauta diskusija par saistītajiem parametriem un transakciju plūsmām."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a>Apskats par debitoru pasūtījumiem

[!INCLUDE [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par debitoru pasūtījumiem pārdošanas punktā Retail Modern POS (MPOS). Debitoru pasūtījumi tiek saukti arī par īpašajiem pasūtījumiem. Šajā tēmā ir iekļauta diskusija par saistītajiem parametriem un transakciju plūsmām.

Visaptveroša kanāla mazumtirdzniecības pasaulē daudzi mazumtirgotāji nodrošina iespēju izmantot debitoru pasūtījumus jeb īpašos pasūtījumus, lai izpildītu dažādas preču un izpildes prasības. Tālāk uzskaitīti daži tipiski scenāriji.

-   Debitors vēlas, lai preces tiek piegādātas uz konkrētu adresi konkrētā datumā.
-   Debitors preces vēlas saņemt tādā veikalā vai atrašanās vietā, kas atšķiras no veikala vai atrašanās vietas, kur debitors šīs preces iegādājās.
-   Debitors vēlas, lai klienta nopirktās preces tiktu izdotas kādam citam.

Mazumtirgotāji debitoru pasūtījumus izmanto arī ar mērķi mazināt pārdošanas zudumus, kurus pretējā gadījumā izraisītu krājumu deficīts, jo preces var piegādāt vai izdot dažādos laikos vai vietās.

## <a name="set-up-customer-orders"></a>Iestatīt debitoru pasūtījumus
Tālāk ir aprakstīti daži no parametriem, ko var iestatīt lapā **Mazumtirdzniecības parametri**, lai definētu debitoru pasūtījumu izpildi.

-   **Noklusējuma depozīts procentos** — norādiet summu, kas debitoram ir jāsamaksā kā depozīts, lai pasūtījumu varētu apstiprināt. Noklusējuma depozīta summa tiek aprēķināta kā procenti no pasūtījuma vērtības. Atkarībā no privilēģijām veikala darbinieks var spēt ignorēt šo summu, izmantojot funkciju **Depozīta ignorēšana**.
-   **Atcelšanas maksa procentos** — ja debitora pasūtījuma atcelšanas gadījumā tiek piemērota maksa, norādiet šīs maksas summu.
-   **Atcelšanas maksas kods** — ja debitora pasūtījuma atcelšanas gadījumā tiek piemērota maksa, šī maksa pārdošanas pasūtījuma tiek apzīmēta ar maksas kodu. Izmantojiet šo parametru, lai definētu atcelšanas maksas kodu.
-   **Nosūtīšanas maksas kods** — mazumtirgotāji var iekasēt papildu maksu par preču nosūtīšanu debitoram. Šīs nosūtīšanas maksas summa pārdošanas pasūtījumā tiek apzīmēta ar maksas kodu. Izmantojiet šo parametru, lai nosūtīšanas maksas kodu kartētu uz nosūtīšanas maksām debitora pasūtījumā.
-   **Atmaksāt nosūtīšanas maksas** — norādiet, vai ar debitora pasūtījumu saistītās nosūtīšanas maksas tiek atmaksātas.
-   **Maksimālā summa bez apstiprināšanas** — ja nosūtīšanas maksas tiek atmaksātas, norādiet maksimālo nosūtīšanas maksas atmaksu summu dažādos atgriešanas pasūtījumos. Ja šī summa ir pārsniegta, lai turpinātu atmaksāšanas procesu, ir nepieciešams vadītāja veikts pārlabojums. Lai izpildītu tālāk norādītos scenārijus, nosūtīšanas maksu atmaksa var pārsniegt sākotnēji samaksāto summu.
    -   Maksas tiek lietotas pārdošanas pasūtījuma galvenes līmenī, un gadījumā, ja tiek atgriezts kāds daudzums no ražošanas rindas, maksimālo šīm precēm atļauto atmaksu par nosūtīšanas maksām un daudzumu nevar noteikt veidā, kas ir piemērots visiem mazumtirdzniecības debitoriem.
    -   Nosūtīšanas maksas rodas katrai nosūtīšanas instancei. Ja debitors preces atgriež vairākas reizes, bet mazumtirgotāja politikā ir noteikts, ka atgriešanas nosūtīšanas maksu sedz mazumtirgotājs, tad nosūtīšanas maksas pārsniedz faktiskās nosūtīšanas maksas.

## <a name="transaction-flow-for-customer-orders"></a>Transakciju plūsma debitoru pasūtījumiem
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Izveidot debitora pasūtījumu pārdošanas punktā Retail Modern POS

1.  Pievienojiet transakcijai debitoru.
2.  Pievienojiet grozam preces.
3.  Noklikšķiniet uz **Izveidot debitora pasūtījumu** un pēc tam atlasiet pasūtījuma tipu. Pasūtījuma tips var būt **Debitora pasūtījums** vai **Piedāvājums**.
4.  Noklikšķiniet uz **Nosūtīt atlasīto** vai **Nosūtīt visu**, lai preces nosūtītu uz adresi debitora kontā, norādiet pieprasīto nosūtīšanas datumu un norādiet nosūtīšanas maksas.
5.  Noklikšķiniet uz **Izdot atlasīto** vai **Izdot visu**, lai atlasītu preces, kas tiks izdotas no pašreizējā veikala vai cita veikala norādītajā datumā.
6.  Iekasējiet depozīta summu, ja ir nepieciešams depozīts.

### <a name="edit-an-existing-customer-order"></a>Rediģēt esošu debitora pasūtījumu

1.  Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.
2.  Atrodiet un atlasiet rediģējamo pasūtījumu. Lapas apakšpusē noklikšķiniet uz **Rediģēt**.

### <a name="pick-up-an-order"></a>Izdot pasūtījumu

1.  Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.
2.  Atlasiet izdodamo pasūtījumu. Lapas apakšpusē noklikšķiniet uz **Izdošana un iepakošana**.
3.  Noklikšķiniet uz **Izdot**.

### <a name="cancel-an-order"></a>Atcelt pasūtījumu

1.  Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.
2.  Atlasiet atceļamo pasūtījumu. Lapas apakšpusē noklikšķiniet uz **Atcelt**.

#### <a name="create-a-return-order"></a>Izveidot atgriešanas pasūtījumu

1.  Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.
2.  Atlasiet atgriežamo pasūtījumu, atlasiet rēķinu šim pasūtījumam un pēc tam atlasiet preču rindu, kuras preces jāatdod.
3.  Lapas apakšpusē noklikšķiniet uz **Atgriezt pasūtījumu**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asinhrona transakciju plūsma debitoru pasūtījumiem
Debitoru pasūtījumus no pārdošanas punkta (point of sale — POS) klienta var izveidot gan sinhronajā režīmā, gan asinhronajā režīmā.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Iespējot debitoru pasūtījumu izveidošanu asinhronajā režīmā

1.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profils** &gt; **Funkcionalitātes profili**.
2.  Kopsavilkuma cilnē **Vispārīgi** opcijai **Izveidot debitora pasūtījumu asinhronā režīmā** iestatiet vērtību **Jā**.

Kad opcija **Izveidot debitora pasūtījumu asinhronā režīmā** ir iestatīta uz **Jā**, debitoru pasūtījumi vienmēr tiek veidoti asinhronajā režīmā, pat tad, ja ir pieejams pakalpojums Retail Transaction Service (RTS). Ja šī opcija ir iestatīta uz **Nē**, tad debitoru pasūtījumi vienmēr tiek veidoti sinhronajā režīmā, izmantojot RTS. Kad debitoru pasūtījumi tiek veidoti asinhronajā režīmā, tie tiek izvilkti un ievietoti programmatūrā Dynamics 365 for Retail, izmantojot vilkšanas (Pull — P) darbus. Kad manuāli vai pakešuzdevuma apstrādes ietvaros tiek palaista funkcija **Sinhronizēt pasūtījumus**, programmatūrā Dynamics 365 for Retail tiek izveidoti atbilstošie pārdošanas pasūtījumi.

<a name="see-also"></a>Skatiet arī
--------

[Hibrīdie debitoru pasūtījumi](hybrid-customer-orders.md)




