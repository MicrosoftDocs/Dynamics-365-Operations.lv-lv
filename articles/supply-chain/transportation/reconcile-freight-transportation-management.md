---
title: Saskaņot kravu transportēšanas pārvaldībā
description: Šajā tēmā ir izklāstīts kravas saskaņošanas process.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014512"
---
# <a name="reconcile-freight-in-transportation-management"></a>Saskaņot kravu transportēšanas pārvaldībā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir izklāstīts kravas saskaņošanas process.

Kravas saskaņošanu var izpildīt manuāli vai to var iestatīt automātiskai izpildīšanai. Lai izmantotu automātisko kravas saskaņošanu, ir jāiestata audita šablons, kur varat definēt kritērijus, kuri nosaka, kādi kravas rēķini tiek saskaņoti automātiski.

## <a name="the-freight-reconciliation-process"></a>Kravas saskaņošanas process

Kravas pārvadāšanas likmes aprēķina likmes noteikšanas programma, kas ir saistīta ar attiecīgo sūtījumu pārvadātāju. Ja krava ir apstiprināta, tiek ģenerēta kravas pavadzīme un uz to tiek pārsūtītas kravas pārvadāšanas likmes. Kravas pārvadāšanas likmes tiek iedalītas kā papildmaksas attiecīgajam pirmdokumentam (pirkšanas pasūtījumam, pārdošanas pasūtījumam un/vai pārsūtīšanas pasūtījumam) atkarībā no regulārajam norēķinu procesam izmantotajiem iestatījumiem. Kravas saskaņošanas process (kas tiek saukts arī par salīdzināšanas procesu) var sākties, tiklīdz tiek saņemts kravas rēķins no sūtījumu pārvadātāja. Rēķinu var saņemt elektroniski vai papīra formātā. Ja rēķins tiek saņemts papīra formātā, varat ģenerēt elektronisku rēķinu, izmantojot kravas pavadzīmi kā veidni.

[![Kravas saskaņošanas process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuāla saskaņošana

Ja kravu saskaņojat manuāli, tad rēķinā iekļautajai kravai katra rēķina rinda ir jāsalīdzina ar kravas pavadzīmes rindu vai rindām. Šo salīdzināšanu jūs veicat lapā **Kravas pavadzīmes un rēķina salīdzināšana**. Ja rēķina rindas summa neatbilst kravas pavadzīmes summai, jums ir jāatlasa saskaņošanas iemesls šai atšķirībai. Ja saskaņošanai pastāv vairāki iemesli, neatbilstošo summu varat sadalīt starp tiem. Saskaņošanas iemesls nosaka, kā šīs starpību summas tiek grāmatotas virsgrāmatā. Kad ir izpildīta visa rēķina summas saskaņošana, tā tiek iesniegta apstiprināšanai, un pēc tam žurnāls tiek grāmatots. Nākamajā attēlā ir parādīts, kā ģenerēt kravas rēķinu un veikt kravas saskaņošanu.

[![Kravas saskaņošanas uzdevumi](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automātiska saskaņošana

Lai izmantotu automātisko saskaņošanu, jums ir jānorāda saskaņošanas grafiks, kā arī izmantojamie rēķini un sūtījumu pārvadātāji. Rēķinu rindu un kravu pavadzīmju salīdzināšana tiek veikta atbilstoši audita šablona iestatījumiem un kravas pavadzīmes tipam. Kad esat izpildījis automātisko saskaņošanu, jums ir jāapstrādā visi rēķini, kurus sistēma nespēj saskaņot. Pēc tam jums šie rēķini ir jāpārstrādā manuāli, pirms visus rēķinus varat grāmatot maksājumam.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Saskaņot kravas pavadzīmes ar kravas rēķiniem, izmantojot automātisku vai manuālu saskaņošanu

*Saskaņošana* ir process, kurā tiek meklētas kravu pavadzīmes, kas atbilst katram kravas pavadzīmei. To var izdarīt, saskaņojot rēķinu rindas pa vienai (manuāla saskaņošana) vai saskaņojot visus pieejamos rēķinus uzreiz (automātiskā saskaņošana).

### <a name="auto-matching"></a>Automātiskā saskaņošana

Saskaņojot vairākus kravas rēķinus ar vienu kravas pavadzīmi, automātiskās atbilstības process darbojas šādi:

1. Visi saskaņotie kravas rēķini tiek kārtoti pēc summas, un pirmā ir vislielākā summa.
1. Kravas pavadzīmes tiek saskaņotas vienu pa vienam, līdz kravas pavadzīmei nav atlicis pozitīvs daudzums.
1. Atkarībā no audita šablona iestatījumiem un kravas pavadzīmju atlikušās summas, tiek iestatīta atlikusī summa.

### <a name="manual-matching"></a>Manuāla saskaņošana

Visas kravas pavadzīmes ar pozitīvām summām būs pieejamas saskaņošanai. Līdzīgi automātiskajai saskaņošanai lietotājs varēs saskaņot tikai kravas pavadzīmes ar negatīvām summām kravas pavadzīmēm, kas nav pilnībā saskaņotas.

### <a name="example"></a>Paraugs

Pieņemsim, ka jums ir kravas pavadzīme (FB) par summu 1500 un esat izveidojis trīs kravas pavadzīmes kravas pavadzīmes rēķinus ar vienu rēķina rindu katram rēķinam ar šādiem iestatījumiem:

- Sākotnējā kravas pavadzīme (FB): summa 1500
- 1. rēķins (Inv1): summa 1000
- 2. rēķins (Inv2): summa 600
- 3. rēķins (Inv3): summa -100

#### <a name="automatic-matching-result"></a>Automātiska atbilstības rezultāts

Automātiskā saskaņošana tiks izpildīta šādā secībā:

1. Kārtot visus kravas rēķinus dilstošā secībā pēc summas: Inv1 -> Inv2 -> Inv3.
1. Saskaņot Inv1 ar FB. Inv1 ir 1000 saskaņots, un FB atlikusī summa ir 500, tāpēc statuss ir iestatīts uz *Daļēji saskaņots*.
1. Saskaņot Inv2 ar FB. Inv2 ir 500 saskaņoti, un FB atlikusī summa ir 0, tāpēc statuss ir iestatīts uz *Pilnībā saskaņots*.
1. Tā kā FB tagad ir pilnībā saskaņots, Inv3 netiks apstrādāts.

#### <a name="manual-matching-result"></a>Manuālas atbilstības rezultāts

Manuālai saskaņošanai rezultāti mainās atkarībā no atbilstības secības, kā ilustrēts šajos piemēros.

##### <a name="manual-matching-case-1"></a>Manuālas saskaņošanas gadījums 1

Viens veids, kā veikt manuālu atbilstības šajā piemērā ir turpināt šādi:

1. Saskaņot Inv1 ar FB. FB ir 500 saskaņoti, tāpēc statuss ir iestatīts uz *Daļēji saskaņots*.
1. Saskaņot Inv2 ar FB. Inv2 ir 500 saskaņoti, un FB atlikusī summa ir 0, tāpēc statuss ir iestatīts uz *Pilnībā saskaņots*.
1. Manuāli saskaņojot Inv3, jūs neatradīsiet nevienu nesaskaņotu kravu pavadzīmi.

Šis gadījums pamatā ir tāds pats kā automātiskā saskaņošana

##### <a name="manual-matching-case-2"></a>Manuālas saskaņošanas gadījums 2

Viens veids, kā veikt manuālu atbilstības šajā piemērā ir turpināt šādi:

1. Saskaņot Inv3 ar FB. Tagad FB atlikusī summa ir 1600, kas ir tā pati, kas atņemot negatīvos 100 pa virsu 1500. Gan FB, gan Inv3 atbilstošais daudzums ir -100.
1. Saskaņot Inv1 un Inv 2 ar FB vienu pēc otra. FB ir pilnībā saskaņots.

Kā redzams šajā piemērā, atbilstošie kravas rēķini ar negatīvām summām ir jāveic tikai manuāli. Tas nodrošina, ka vienmēr ir iespējams saskaņot kravas pavadzīmes ar negatīvām summām un kravas pavadzīmi, kas nav pilnībā saskaņotas, jo tādējādi var kontrolēt atbilstošo secību.
