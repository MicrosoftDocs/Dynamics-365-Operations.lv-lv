---
title: "Detalizētās bankas darbību saskaņošanas pārskats"
description: "Detalizētā bankas darbību saskaņošana jums ļauj importēt elektroniskus bankas izrakstus un automātiski saskaņot tos ar bankas transakcijām programmatūrā Microsoft Dynamics 365 for Operations.  Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6c6b171fbba90b02b80c70783ecfd9ab57beb96d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Detalizētās bankas darbību saskaņošanas pārskats

[!include[banner](../includes/banner.md)]


Detalizētā bankas darbību saskaņošana jums ļauj importēt elektroniskus bankas izrakstus un automātiski saskaņot tos ar bankas transakcijām programmatūrā Microsoft Dynamics 365 for Operations.  Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana.  

Pirms detalizētās bankas darbību saskaņošanas funkcionalitātes lietošanas ir jāizpilda vairāki sagatavošanās darbi. Papildinformāciju par bankas izrakstu importa iestatīšanu skatiet rakstā [Iestatīt bankas izraksta importēšanas procesu](set-up-advanced-bank-reconciliation-import-process.md).  Tālāk ir aprakstītas prasības saskaņošanas procesa iestatīšanai.

## <a name="transaction-codes"></a>Transakciju kodi
Transakciju kodus var izmantot kā daļu no bankas darbību saskaņošanas atbilstības kārtulām.  Transakciju kodi starp Dynamics 365 for Operations un jūsu bankas izrakstu palīdzēs saskaņot tikai transakcijas ar vienādu tipu.  Lai veiktu šāda tipa saskaņošanu, jums vispirms ir jādefinē transakciju tipi, kas tiek izmantoti bankas transakcijām no Dynamics 365 for Operations, un pēc tam šie tipi ir jākartē uz jūsu bankas izraksta transakciju kodiem.  Transakciju tipi Dynamics 365 for Operations banku transakcijām ir definēti lapā **Bankas transakcijas tips**.  Šī ir arī tā vietā, kur jūs definējat galveno kontu, kuru izmantot ar attiecīgo transakcijas tipu saistītajiem grāmatojumiem. 

Kad jūsu Dynamics 365 for Operations bankas transakciju kodi ir definēti, pēc tam šie transakciju kodi ir jākartē uz elektroniskajos bankas izrakstos izmantotajiem transakciju kodiem.  Šī kartēšana notiek, izmantojot lapu **Transakciju kodu kartēšana**.  Transakciju kodu kartējums katram bankas kontam tiek izpildīts atsevišķi.

## <a name="matching-rules-and-matching-rule-sets"></a>Atbilstības kārtulas un atbilstības kārtulu kopas
Atbilstības kārtulas jums ļauj definēt kritērijus automātiskai saskaņošanai starp ynamics 365 for Operations bankas transakcijām un bankas izraksta transakcijām.  Atbilstības kārtulu iestatīšana tiek veikta lapā **Saskaņošanas atbilstības kārtulas**.  Papildinformāciju skatiet rakstā [Iestatīt bankas saskaņošanas atbilstības kārtulas](set-up-bank-reconciliation-matching-rules.md). 

Lai definētu atbilstības kārtulu grupu, kas tiek secīgi izpildīta bankas darbību saskaņošanas procesa laikā, tiek izmantotas atbilstības kārtulu kopas.  Atbilstības kārtulu kopas tiek konfigurētas lapā **Saskaņošanas atbilstības kārtulu kopas**.

## <a name="cash-and-bank-management-parameters"></a>Kases un bankas vadības parametri
Lapā **Kases un bankas vadības parametri** pastāv vairāki detalizētās bankas darbību saskaņošanas procesam specifiski parametri.  Opcija **Rādīt izraksta rindas summu formātā debets/kredīts** maina summu skatu lapā **Bankas izraksts**.  Ja šī opcija ir atzīmēta, tad bankas izraksta transakciju summas tiek rādītas atsevišķās debeta un kredīta kolonnās.  Ja tā nav atzīmēta, bankas izraksta transakciju summas tiek rādītas vienā summu kolonnā ar atbilstošo zīmi. 

Parametru lapā iestatītajām validēšanas opcijām ir prioritāte pār atbilstības kārtulām veiktajām atlasēm.  Piemēram, jūs nevarat manuāli vai automātiski noteikt atbilstību dokumentiem, kas neietilpst parametru lapā iestatītajā datumu atšķirības diapazonā.  Turklāt, ja ir atzīmēta opcija **Validēt transakcijas tipa kartēšanu**, tad transakciju tipiem ir jāveic kartēšana starp Dynamics 365 for Operations bankas transakciju un bankas izraksta transakciju, lai šīm transakcijām varētu manuāli vai automātiski noteikt atbilstību. 

Jums ir arī jākonfigurē nepieciešamo numuru sērijas lapā **Kases un bankas vadības parametri**.  Cilnē **Numuru sērijas** iestatiet numuru sēriju kodus atsaucēm **Lejupielādes ID, Izraksta ID, Saskaņošanas ID un Bankas darbību saskaņošana**.

## <a name="bank-account-reconciliation-options"></a>Bankas kontu saskaņošanas opcijas
Vispirms jums ir jāiespējo detalizētā bankas darbību saskaņošana attiecīgajam bankas kontam.  Kad detalizētā bankas darbību saskaņošanas funkcionalitāte ir iespējota, lapā **Bankas konts** ir pieejamas vairākas papildu opcijas. 

Funkcionalitāte **Lietot bankas izrakstus kā elektronisko maksājumu apstiprinājumu** bankas darbību saskaņošanas funkcionalitāti integrē elektronisko maksājumu statusos.  Ja tā ir iespējota, tiek automātiski izveidots bankas dokuments, kad elektroniskā maksājuma statuss ir iestatīts uz **Nosūtīts**.  Turklāt pēc maksājumu atbilstības noteikšanas, saskaņošanas un grāmatošanas elektroniskā maksājuma statuss no **Nosūtīts** tiek mainīts uz **Saņemts**. 

Lauks **Bankas konta nosaukumu izrakstos** ir nosaukums, kas tiek izmantots bankas kontam jūsu elektroniskajos bankas izrakstos.  Šis nosaukums tiek lietots, kad nepieciešams noteikt, kādas transakcijas importēt bankas kontam no izraksta, kurā var būt iekļauta informācija par vairākiem bankas kontiem. 

Opcija **Saskaņot pēc importēšanas** automātiski validē šo bankas izrakstu, izveido jaunu bankas saskaņošanu un darblapu, ka arī izpilda noklusējuma atbilstības kārtulu kopu.  Šī funkcionalitāte procesu automatizē līdz vietai, kur transakciju atbilstība ir jānosaka manuāli.  Importēšanas laikā bankas konta iestatījums tiek pārslēgts uz noklusējuma vērtībām.




