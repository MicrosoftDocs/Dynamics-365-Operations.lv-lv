---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu.
author: ChrisGarty
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdddd26a662e9334f6d3c9806871df5b58ec03c7
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934913"
---
# <a name="workflow-faq"></a>Bieži uzdotie jautājumi par darbplūsmām

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kāpēc darba vienuma noraidīšanas gadījumā tiek saņemti vairāki paziņojumi?
Darba vienuma noraidīšanas gadījumā šis darba vienums tiek pabeigts ar statusu Noraidīts. Tiek izveidots cits darba vienums, kas tiek piešķirts veidotājam. Tas nozīmē, ka veidotājs saņem paziņojumu par noraidīto darba vienumu, bet lietotājs, kas ir piešķirts jaunajam izmaiņu pieprasījuma darba vienumam, saņem atsevišķu paziņojumu. 

Katrs paziņojums ir saistīts ar atšķirīgu darba vienumu, taču to līdzība var radīt apjukumu. Mēs meklējam veidus, kā uzlabot šo situāciju nākamajā laidienā.

## <a name="why-are-my-workflow-exports-failing"></a>Kāpēc manas darbplūsmas tiek eksportētas neveiksmīgi?
Pašlaik darbplūsmas eksportēšanas līdzeklī ir noteikts ierobežojums, kas neļauj darbplūsmas nosaukumiem pārsniegt 48 rakstzīmes. Izmantojot nosaukumu, kas ir garāks par 48 rakstzīmēm, var rasties kļūda “Serveris nevarēja autentificēt pieprasījumu” un/vai iespējamība, ka faila eksportēšana netiks ļauta bez faila tipa. Detalizēta informācija ir pieejama šajā emuāra ziņā: [Darbplūsmas eksportēšanas problēmu risināšana](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Vai darbplūsmas iesniedzējs var arī apstiprināt šo darbplūsmu?
Jā, darbplūsmas iesniedzējs var arī apstiprināt šo darbplūsmu, ja tā ir attiecīgi konfigurēta. Lai nepieļautu šādu uzvedību, vienumu **Sistēmas administrēšana > Darbplūsma > Darbplūsmas parametri > Vispārīgi > Apstiprinātājs > Aizliegt iesniedzējam veikt apstiprināšanu** iestatiet uz **Jā**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Vai varu darbplūsmām pievienot brīdinājumus, lai lietotājiem sniegtu paziņojumus?
Tālāk ir norādītas daži galvenās jomas, kas ir jāņem vērā saistībā ar brīdinājumu pievienošanu darbplūsmām, lai sniegtu paziņojumus.
- Brīdinājumu salīdzinājums ar darbplūsmas paziņojumu mehānismiem
    - Brīdinājumus var iestatīt ierakstu izmaiņām. Darbplūsmas maina ierakstus, tādēļ var iestatīt brīdinājumu saistībā ar darbplūsmas izraisītām ieraksta izmaiņām. Taču, tā kā darbplūsmām ir citādas iebūvētās paziņojumu opcijas, brīdinājumu izmantošana nav ideāla.
- Standarta paziņojumi no darbplūsmām 
    - Darbplūsmām ir iebūvēti e-pasta ziņojumi. Debitors var konfigurēt paziņojumus, lai lietotājiem tiktu nosūtīti e-pasta paziņojumi. Šie paziņojumi neizraisa darbību centra ziņojumu rādīšanu lietotājiem.
    - Kādā no turpmākajiem atjauninājumiem mēs pievienosim darbību centra ziņojumu, lai lietotājam tiktu piešķirts darbplūsmas darba vienums. 
- Paziņojumu pievienošana darbplūsmām
    - Noteiktiem lietotājiem nevar izveidot darbību centra ziņojumus, piemēram, ziņojumu, kas ir izveidots no darbplūsmas iekš X++.
    - [Darbplūsmām ir biznesa notikumi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), kurus debitors varētu izmantot, lai aktivizētu meklēto paziņojumu sniegšanu ar Flows.   

Īsumā — ja lietotājs nesaņem nepieciešamo paziņojumu no darbību centra, kad šim lietotājam ir piešķirts kāds darbplūsmas darba elements, tad papildu vai atšķirīgu paziņojumu sniegšanai ir jāizmanto [darbplūsmas biznesa notikumi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) un Microsoft Power Automate.

## <a name="workflow-editor-has-trouble-starting-under-adfs"></a>Darbplūsmas redaktoram ir problēmas, uzsākot palaišanu ar ADFS 
Darbojoties Active Directory Federation Services (AD FS) ietvaros jauninātā vidē, darbplūsmas redaktoram var rasties palaišanas problēmas. Ja tā notiek, pārliecinieties, vai URL "https://dynamicsaxworkfloweditor/" tiek pievienota ADFS iestatījumu rekvizītam **Microsoft Dynamics 365 for Operations lokāli — Darbplūsma — Vietējā programma**.
