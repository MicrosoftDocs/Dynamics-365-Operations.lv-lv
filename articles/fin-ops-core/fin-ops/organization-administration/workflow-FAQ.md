---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu.
author: ChrisGarty
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe11942ca41dd8c0ca23d94006569c50a4501a52
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065584"
---
# <a name="workflow-faq"></a>Bieži uzdotie jautājumi par darbplūsmām

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

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
    - [Darbplūsmām ir biznesa notikumi](../../dev-itpro/business-events/business-events-workflow.md), kurus debitors varētu izmantot, lai aktivizētu meklēto paziņojumu sniegšanu ar Flows.   

Īsumā — ja lietotājs nesaņem nepieciešamo paziņojumu no darbību centra, kad šim lietotājam ir piešķirts kāds darbplūsmas darba elements, tad papildu vai atšķirīgu paziņojumu sniegšanai ir jāizmanto [darbplūsmas biznesa notikumi](../../dev-itpro/business-events/business-events-workflow.md) un Microsoft Power Automate.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Kāpēc darbplūsmas redaktors nevar sākt ar AD FS?
Darbojoties Active Directory Federation Services (AD FS) ietvaros jauninātā vidē, darbplūsmas redaktoram var rasties palaišanas problēmas. Ja tā notiek, pārliecinieties, vai URL "https://dynamicsaxworkfloweditor/" tiek pievienota ADFS iestatījumu rekvizītam **Microsoft Dynamics 365 for Operations lokāli — Darbplūsma — Vietējā programma**.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Kāpēc es saņemu SQL strupsaķeres darbplūsmas apstrādei? 
Noklusējuma lauka vērtība **Darbplūsmas vienumu skaitam partijā** lapā **Darbplūsmas parametri** ir 0. Vērtība 0 liek mainīt noklusējumu uz 20 vienībām partijā. Uzmanieties, pielāgojot šo vērtību, jo liels vienumu skaits katrā partijā (> 40) var izraisīt SQL strupsaķeri.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Kas ir Darbplūsmas uzlabotās kļūdas līdzeklis?
Darbplūsmas uzlabotās kļūdas līdzeklis versijā 10.0.13 pievieno kļūdu kodus, lai diferencētu dažādas darbplūsmas kļūdu klases. Paziņotie kļūdu ziņojumi lielākoties būs līdzīgi, bet ar nelielām atšķirībām, lai tos padarītu vieglāk saprotamus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
