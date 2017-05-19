---
title: "Saskaņot kravu transportēšanas pārvaldībā"
description: "Šajā rakstā ir izklāstīts kravas saskaņošanas process."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 59c5dd4574aed1bc97fc945c999016be1c399f71
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Saskaņot kravu transportēšanas pārvaldībā

[!include[banner](../includes/banner.md)]


Šajā rakstā ir izklāstīts kravas saskaņošanas process.

Kravas saskaņošanu var izpildīt manuāli vai to var iestatīt automātiskai izpildīšanai. Lai izmantotu automātisko kravas saskaņošanu, ir jāiestata audita šablons, kur varat definēt kritērijus, kuri nosaka, kādi kravas rēķini tiek saskaņoti automātiski.

## <a name="the-freight-reconciliation-process"></a>Kravas saskaņošanas process
Kravas pārvadāšanas likmes aprēķina likmes noteikšanas programma, kas ir saistīta ar attiecīgo sūtījumu pārvadātāju. Ja krava ir apstiprināta, tiek ģenerēta kravas pavadzīme un uz to tiek pārsūtītas kravas pārvadāšanas likmes. Kravas pārvadāšanas likmes tiek iedalītas kā papildmaksas attiecīgajam pirmdokumentam (pirkšanas pasūtījumam, pārdošanas pasūtījumam un/vai pārsūtīšanas pasūtījumam) atkarībā no regulārajam norēķinu procesam izmantotajiem iestatījumiem. Kravas saskaņošanas process (kas tiek saukts arī par salīdzināšanas procesu) var sākties, tiklīdz tiek saņemts kravas rēķins no sūtījumu pārvadātāja. Rēķinu var saņemt elektroniski vai papīra formātā. Ja rēķins tiek saņemts papīra formātā, varat ģenerēt elektronisku rēķinu, izmantojot kravas pavadzīmi kā veidni. 

[![Kravas saskaņošanas process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuāla saskaņošana
Ja kravu saskaņojat manuāli, tad rēķinā iekļautajai kravai katra rēķina rinda ir jāsalīdzina ar kravas pavadzīmes rindu vai rindām. Šo salīdzināšanu jūs veicat lapā **Kravas pavadzīmes un rēķina salīdzināšana**. Ja rēķina rindas summa neatbilst kravas pavadzīmes summai, jums ir jāatlasa saskaņošanas iemesls šai atšķirībai. Ja saskaņošanai pastāv vairāki iemesli, neatbilstošo summu varat sadalīt starp tiem. Saskaņošanas iemesls nosaka, kā šīs starpību summas tiek grāmatotas virsgrāmatā. Kad ir izpildīta visa rēķina summas saskaņošana, tā tiek iesniegta apstiprināšanai, un pēc tam žurnāls tiek grāmatots. Nākamajā attēlā ir parādīts, kā ģenerēt kravas rēķinu un izpildīt kravas saskaņošanu programmatūrā Microsoft Dynamics 365 for Operations. 
[![Kravas saskaņošanas uzdevumi programmatūrā Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automātiska saskaņošana
Lai izmantotu automātisko saskaņošanu, jums ir jānorāda saskaņošanas grafiks, kā arī izmantojamie rēķini un sūtījumu pārvadātāji. Rēķinu rindu un kravu pavadzīmju salīdzināšana tiek veikta atbilstoši audita šablona iestatījumiem un kravas pavadzīmes tipam. Kad esat izpildījis automātisko saskaņošanu, jums ir jāapstrādā visi rēķini, kurus sistēma nespēj saskaņot. Pēc tam jums šie rēķini ir jāpārstrādā manuāli, pirms visus rēķinus varat grāmatot maksājumam.




