---
title: "Kredīta un iekasēšanas iestatīšana"
description: "Šajā rakstā ir paskaidrots, kā iestatīt iekasēšanas funkcionalitāti."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09296ae02c690fa683d853cc91a5abf243bcafa7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-credit-and-collections"></a>Kredīta un iekasēšanas iestatīšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā iestatīt iekasēšanas funkcionalitāti.

<a name="set-up-aging-period-definitions"></a>Iestatiet vecumstruktūras perioda definīcijas
-------------------------------

Iestatiet vecumstruktūras perioda definīciju. Vecumstruktūras perioda definīcija nosaka kolonnas, kas tiek rādītas sarakstu lapās **Vecas bilances**, **Iekasēšanas aktivitātes** un **Iekasēšanas gadījumi**. Tā definē arī periodus, kas tiek rādīti lapā **Iekasēšana**. Ja ir iestatīta debitoru kopa, kopai tiek izmantota vecumstruktūras perioda definīcija. Ja kopas nav iestatītas, tiek izmantota noklusējuma vecumstruktūras perioda definīcija, kas ir norādīta lapā **Debitoru moduļa parametri**. Ja noklusējuma vecumstruktūras perioda definīcija nav norādīta, tiek izmantota pirmā vecumstruktūras perioda definīcija no lapas **Vecumstruktūras perioda definīcijas**.

## <a name="create-an-aging-snapshot"></a>Izveidot vecumstruktūras momentuzņēmumu
Izveidojiet vecumstruktūras momentuzņēmumu ierakstus visiem debitoriem vai debitoru kopai. Vecumstruktūras momentuzņēmuma informācija tiek rādīta saraksta lapā **Vecas bilances** un lapā **Iekasēšana**. Vispirms ir jāizveido vecumstruktūras momentuzņēmums, un tikai tad varat izmantot saraksta lapu. Saraksta lapā tiek rādīta informācija tikai par tiem debitoriem, kuriem ir izveidots vecumstruktūras momentuzņēmums.

## <a name="optional-set-up-customer-pools"></a>Pēc izvēles: iestatīt debitoru kopas
Lai attēlotu debitoru grupas, varat iestatīt debitoru kopas. Debitoru kopas varat izmantot kā filtrus debitoru informācijai, kas tiek rādīta sarakstu lapās **Iekasēšana**, lapā **Iekasēšana**, vai veidojot vecumstruktūras momentuzņēmumus.

## <a name="optional-create-a-collections-team"></a>Pēc izvēles: izveidot iekasēšanas grupu
Ja vairāki cilvēki jūsu organizācijā veic iekasēšanas darbu, varat izveidot iekasēšanas komandu. Darba grupu varat atlasīt lapā **Debitoru moduļa parametri**. Ja neizveidojat iekasēšanas grupu, tad grupa tiek izveidota automātiski, kad iestatāt iekasēšanas aģentus lapā **Iekasēšanas aģents**.

## <a name="set-up-a-collections-case-category"></a>Iestatīt iekasēšanu notikumu kategorijai
Ja izmantosies gadījumus, lai organizētu savu iekasēšanas darbu, iestatiet gadījumu kategoriju, kuras kategorijas tips ir **Iekasēšana**. Šis iestatījums ir nepieciešams tikai tad, ja lapā **Iekasēšana** vēlaties izmantot gadījumu funkcionalitāti.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Iestatīt žurnālu nosaukumus (segšana, norakstīšana un NSF)
Iestatiet žurnālu nosaukumus, kas tiek izmantoti, kad lapā **Iekasēšana** tiek apstrādātas transakcijas. Šī apstrāde ietver transakcijas segšanu, transakcijas norakstīšanu un nepietiekamu naudas līdzekļu (NSF) maksājuma apstrādi.

| Apraksts | Žurnāla veids     |
|-------------|------------------|
| Apdzīvota vieta  | Debitora maksājums |
| Norakstīšana   | Ikdienas            |
| NSF         | Debitora maksājums |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Iestatīt pamatojuma kodu norakstīšanas transakcijām
Iestatiet noklusējuma pamatojuma kodu, kas tiek izmantots, kad lapā **Iekasēšana** transakcijas tiek norakstītas. Šo kodu varat mainīt norakstīšanas procesa laikā.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Iestatīt mapi e-pasta pielikumiem un izveidot e-pasta veidnes
Ja no lapas **Iekasēšana** sūtīsiet e-pasta ziņojumus, kuriem ir Microsoft Excel pielikumi, šādiem ziņojumiem varat izveidot papildu e-pasta veidnes.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Iestatīt debitoru moduļa parametrus iekasēšanai
Iestatiet debitoru moduļa parametrus, kas tiek rādīti cilnē **Iekasēšana**.

## <a name="optional-set-up-collections-agents"></a>Pēc izvēles: iestatīt iekasēšanas aģentus
Ja vairāki cilvēki jūsu organizācijā veic iekasēšanas darbu, varat iestatīt iekasēšanas aģentus. Iekasēšanas aģents ir darbinieks, kas ir iestatīts kā lietotājs lapā **Lietotāju attiecības**. Lai aģentiem palīdzētu organizēt viņu darbu, iekasēšanas aģentiem varat piešķirt debitoru kopas (debitoru vaicājumus). Iekasēšanas aģenti tiek pievienoti darba grupai, kas ir atlasīta lapā **Debitoru moduļa parametri**. Ja šajā lapā nav atlasīta neviena grupa, automātiski tiek izveidota jauna grupa ar nosaukumu **Iekasēšana**, un iekasēšanas aģenti tiek pievienoti šai grupai.

## <a name="set-up-a-writeoff-account"></a>Iestatīt norakstīšanas kontu
Iestatiet norakstīšanas kontu, kas tiek izmantots virsgrāmatas norakstīšanas ierakstam, kad tiek norakstīta kāda transakcija. Šis konts tiek glabāts debitoru grāmatošanas metodē.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Iestatīt bankas kontu NSF informāciju
Atjauniniet bankas kontus, lai tiem būtu aktuālais žurnāls, kad lapā **Iekasēšana** tiek identificēti NSF maksājumi. Cilnē **Valūtas pārvaldība**, laukā **NSF maksājumu žurnāls** atlasiet kādu maksājumu žurnālu.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Iestatīt Outlook iestatījumus lapas Iekasēšana lietotājiem
Lai darbinieki varētu izveidot aktivitātes vai sūtīt e-pasta ziņojumus, izmantojot lapu **Iekasēšana**, jums ir jāpārbauda, ka ir atlasīta konfigurācijas atslēga **Microsoft Outlook sinhronizācija** un ka šiem darbiniekiem ir iestatīta Outlook sinhronizēšana.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Iestatīt e-pasta un adreses iestatījumus debitoru iekasēšanas kontaktpersonām
Ja vēlaties sūtīt e-pasta ziņojumus kontaktpersonām, kas norādītas formā **Iekasēšana**, iestatiet debitoru kontaktpersonu e-pasta adreses. Iekasēšanas kontaktpersona tiek izmantota kā noklusējuma kontaktpersona lapā **Iekasēšana**. Varat uzstādīt debitora pārskatu adresi, ja pārskatos ir jālieto adrese, kas nav primārā adrese. 

Kopsavilkuma cilnē **Kredīts un iekasēšana** debitoram laukā **Iekasēšanas kontaktpersona** atlasiet to personu debitora organizācijā, kura strādā ar jūsu iekasēšanas aģentu. Šī persona tiek izmantota kā noklusējuma kontaktpersona lapā **Iekasēšana**, un e-pasta ziņojumi tiek sūtīti šai personai. 

> [!NOTE] 
> Ja debitora iekasēšanas kontaktpersona nav norādīta, tiek izmantota debitora primārā kontaktpersona. Ja primārā kontaktpersona nav norādīta, e-pasta ziņojumi tiek sūtīti uz pirmo adresi, kas ir uzskaitīta lapā **Kontaktpersonas**.

## <a name="set-up-email-settings-for-salespeople"></a>Iestatīt e-pasta iestatījumus pārdevējiem
Ja vēlaties sūtīt e-pasta ziņojumus pārdevējiem, kas norādīti lapā **Iekasēšana**, tad iestatiet pārdevēju e-pasta adreses. Iestatiet e-pasta adresi katram tirdzniecības pārstāvim katrā komisijas pārdošanas grupā. Tirdzniecības pārstāvis, kuram ir atzīmēta opcija **Kontaktpersona**, ir noklusējuma pārdevējs, kam tiek sūtīti e-pasta ziņojumi. 

Ja tirdzniecības pārstāvis nav norādīts, tiek izmantots debitora organizācijas primārais pārdevējs. Ja primārais pārdevējs nav norādīts, tad e-pasta ziņojumi tiek sūtīti pirmajam pārdevējam, kas ir norādīts šajā lapā.


Lai iegūtu papildu informāciju, skatiet šādas tēmas:

 - [Atgādinājuma vēstules secības izveide](tasks/create-collection-letter-sequence.md)
 
 - [Atgādinājuma vēstuļu apstrāde](tasks/process-collection-letters.md)
 
 - [Iekasēšanas informācijas pārskatīšana](tasks/review-collections-information.md)


