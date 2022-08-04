---
title: Detalizētas bankas darbību saskaņošanas iestatīšanas process
description: Detalizēta bankas darbību saskaņošana ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar Microsoft Dynamics bankas darbībām 365 Finanšu programmā. Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana.
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a155174ad3bb815b4f0e6f7ffd893ebf7792bd8
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151886"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Detalizētas bankas darbību saskaņošanas iestatīšanas process

[!include [banner](../includes/banner.md)]

Detalizēta bankas darbību saskaņošana ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar Microsoft Dynamics bankas darbībām 365 Finanšu programmā. Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana.  

Pirms detalizētās bankas darbību saskaņošanas funkcionalitātes lietošanas ir jāizpilda vairāki sagatavošanās darbi. Papildinformāciju par bankas izrakstu importa iestatīšanu skatiet rakstā [Iestatīt papildu bankas saskaņošanas importēšanas procesu](set-up-advanced-bank-reconciliation-import-process.md).  Tālāk ir aprakstītas prasības saskaņošanas procesa iestatīšanai.

## <a name="transaction-codes"></a>Transakciju kodi
Transakciju kodus var izmantot kā daļu no bankas darbību saskaņošanas atbilstības kārtulām. Transakciju kodi palīdz noteikt tikai viena tipa atbilstošās transakcijas programmatūrā Finance un jūsu bankas izrakstā. Lai veiktu šāda veida saskaņošanu, vispirms ir jādefinē transakciju tipi, kas tiek izmantoti bankas transakcijām programmā Finance, un pēc tam šie tipi ir jākartē ar jūsu bankā izmantotajiem izraksta transakciju kodiem. Bankas transakciju tipus var definēt lapā **Bankas transakcijas veids**. Šī ir arī tā vietā, kur jūs definējat galveno kontu, kuru izmantot ar attiecīgo transakcijas tipu saistītajiem grāmatojumiem. 

Kad esat definējis bankas transakciju kodus, varat tos piesaistīt elektroniskajos bankas izrakstos izmantotajiem transakciju kodiem. Šī kartēšana notiek, izmantojot lapu **Transakciju kodu kartēšana**. Transakciju kodu kartējums katram bankas kontam tiek izpildīts atsevišķi.

## <a name="matching-rules-and-matching-rule-sets"></a>Atbilstības kārtulas un atbilstības kārtulu kopas
Atbilstības kārtulas sniedz jums iespēju definēt Finance bankas transakciju un bankas izraksta transakciju automātiskas saskaņošanas kārtulas. Atbilstības kārtulu iestatīšana tiek veikta lapā **Saskaņošanas atbilstības kārtulas**. Papildinformāciju skatiet rakstā [Iestatīt bankas saskaņošanas atbilstības kārtulas](set-up-bank-reconciliation-matching-rules.md). 

Lai definētu atbilstības kārtulu grupu, kas tiek secīgi izpildīta bankas darbību saskaņošanas procesa laikā, tiek izmantotas atbilstības kārtulu kopas.  Atbilstības kārtulu kopas tiek konfigurētas lapā **Saskaņošanas atbilstības kārtulu kopas**.

## <a name="cash-and-bank-management-parameters"></a>Kases un bankas vadības parametri
Lapā **Kases un bankas vadības parametri** pastāv vairāki detalizētās bankas darbību saskaņošanas procesam specifiski parametri.  Opcija **Rādīt izraksta rindas summu formātā debets/kredīts** maina summu skatu lapā **Bankas izraksts**. Ja šī opcija ir atzīmēta, tad bankas izraksta transakciju summas tiek rādītas atsevišķās debeta un kredīta kolonnās. Ja tā nav atzīmēta, bankas izraksta transakciju summas tiek rādītas vienā summu kolonnā ar atbilstošo zīmi. 

Parametru lapā iestatītajām validēšanas opcijām ir prioritāte pār atbilstības kārtulām veiktajām atlasēm. Piemēram, jūs nevarat manuāli vai automātiski noteikt atbilstību dokumentiem, kas neietilpst parametru lapā iestatītajā datumu atšķirības diapazonā. Turklāt gadījumā, ja ir atzīmēta opcija **Pārbaudīt transakcijas veida kartējumu**, lai varētu veikt Finance bankas transakciju un bankas izraksta transakciju manuālu vai automātisku atbilstības noteikšanu, šīm transakcijām ir jābūt kartētām. 

Jums ir arī jākonfigurē nepieciešamo numuru sērijas lapā **Kases un bankas vadības parametri**.  Cilnē **Numuru sērijas** iestatiet numuru sēriju kodus atsaucēm **Lejupielādes ID, Izraksta ID, Saskaņošanas ID un Bankas darbību saskaņošana**.

## <a name="bank-account-reconciliation-options"></a>Bankas kontu saskaņošanas opcijas
Vispirms jums ir jāiespējo detalizētā bankas darbību saskaņošana attiecīgajam bankas kontam. Kad detalizētā bankas darbību saskaņošanas funkcionalitāte ir iespējota, lapā **Bankas konts** ir pieejamas vairākas papildu opcijas. 

Funkcionalitāte **Lietot bankas izrakstus kā elektronisko maksājumu apstiprinājumu** bankas darbību saskaņošanas funkcionalitāti integrē elektronisko maksājumu statusos. Ja tā ir iespējota, tiek automātiski izveidots bankas dokuments, kad elektroniskā maksājuma statuss ir iestatīts uz **Nosūtīts**. Turklāt pēc maksājumu atbilstības noteikšanas, saskaņošanas un grāmatošanas elektroniskā maksājuma statuss no **Nosūtīts** tiek mainīts uz **Saņemts**. 

Lauks **Bankas konta nosaukumu izrakstos** ir nosaukums, kas tiek izmantots bankas kontam jūsu elektroniskajos bankas izrakstos. Šis nosaukums tiek lietots, kad nepieciešams noteikt, kādas transakcijas importēt bankas kontam no izraksta, kurā var būt iekļauta informācija par vairākiem bankas kontiem. 

Opcija **Saskaņot pēc importēšanas** automātiski validē šo bankas izrakstu, izveido jaunu bankas saskaņošanu un darblapu, ka arī izpilda noklusējuma atbilstības kārtulu kopu. Šī funkcionalitāte procesu automatizē līdz vietai, kur transakciju atbilstība ir jānosaka manuāli. Importēšanas laikā bankas konta iestatījums tiek pārslēgts uz noklusējuma vērtībām.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
