---
title: "Detalizētās bankas darbību saskaņošanas pārskats"
description: "Papildu bankas saskaņošana ļauj importēt elektronisko bankas izraksti un automātiski saskaņot ar bankas darbībām programmā Microsoft Dynamics 365 operācijām.  Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana."
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
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Detalizētās bankas darbību saskaņošanas pārskats

Papildu bankas saskaņošana ļauj importēt elektronisko bankas izraksti un automātiski saskaņot ar bankas darbībām programmā Microsoft Dynamics 365 operācijām.  Šajā rakstā ir paskaidrota saskaņošanas procesu iestatīšana.  

Ir vairāki gabali, kas jāiestata pirms izmantojot papildu bankas saskaņojuma funkcionalitāti. Plašāku informāciju par bankas pārskatu importa iestatīšanu, skatiet [iestatītu bankas pārskatu importēšanu](set-up-advanced-bank-reconciliation-import-process.md).  Prasībām, izveidota saskaņošanas process ir detalizēti aprakstīta zemāk.

## <a name="transaction-codes"></a>Darbību kodi
Transakcijas kodus var izmantot kā daļu no bankas saskaņojumu atbilstības kārtulas.  Darījumu kodi palīdzēs saskaņot tikai tāda paša veida darījumiem starp Dynamics 365 operācijām un jūsu bankas konta paziņojumā.  Lai veiktu šāda veida atbilstību, ir vispirms definētu darbību tipus, bankas darbībām no Dynamics 365 operācijām izmantotā tad kartēt šos tipus paziņojumu darījumu kodus izmanto jūsu bankas.  Transakciju tipus Dynamics 365 operācijas bankas darbībām ir definētas **bankas darbības tipa** lapā.  Tas ir arī, kur var noteikt galveno kontu, kas jālieto grāmatojumiem, kas saistīti ar darbības tipu. 

Pēc tam, kad savu dinamiku 365 operācijas bankas darījumu kodi ir definēti, tad kartēt tos izmanto elektronisko bankas izrakstu transakcijas kodus.  Šīs kartēšanas procedūra tiek veikta izmantojot **darījuma koda kartēšanas** lapā.  Darījuma kods kartēšanas pabeigšanas atsevišķi katram bankas kontam.

## <a name="matching-rules-and-matching-rule-sets"></a>Atbilstības kārtulas un atbilstības kārtulu kopas
Atbilstības kārtulas ļauj definēt kritērijus automātisku saskaņošanu starp Dynamics 365 banku operācijas darījumus un bankas izraksta transakcijām.  Iestatīt atbilstošo noteikumu tiek veikta **saskaņošanas atbilstības kārtulas** lapā.  Lai iegūtu papildinformāciju, skatiet [bankas saskaņojumu atbilstības kārtulas iestatīt](set-up-bank-reconciliation-matching-rules.md). 

Atbilstības kārtulu kopas tiek izmantotas, lai norādītu grupu atbilstības kārtulas, kas tiek izpildīti bankas saskaņošanas procesa laikā.  Atbilstības kārtulu kopas tiek konfigurēts, **saskaņošanas atbilstības kārtulu kopas** lapā.

## <a name="cash-and-bank-management-parameters"></a>Kases un bankas vadības parametri
Pastāv īpašas papildu bankas saskaņošanas procesa parametru skaits **naudas un bankas vadības parametrus** lapā.  **Parādīt paziņojumu rindas summa debeta/kredīta** mainās summas uzskata par **bankas paziņojuma** lapā.  Ja ir atlasīta šī opcija, bankas paziņojumu darījumu summas tiks parādīts atsevišķā debeta un kredīta kolonnās.  Ja nav atlasīts, bankas paziņojumu darījumu summas tiks parādīta vienotu summu kolonnā ar attiecīgu zīmi. 

Validēšanas opcijas iestatiet parametru lapā ignorēt selekciju noteikt atbilstības kārtulas.  Piemēram, jūs nevarat manuāli vai automātiski saskaņot dokumentus ārpus iestatīt parametrus lapā datumu atšķirība.  Arī tad, ja iespēja **transakcijas tipu kartēšana pārbaudīt** ir atlasīta, transakciju tipus ir kartēts starp Dynamics 365 operācijas bankas darbībai un bankas izraksta transakciju darbības secību manuāli vai automātiski saskaņot. 

Arī ir jākonfigurē nepieciešamo numuru sērijas par **naudas un bankas vadības parametrus** lapu.  Par **numuru sērijas** cilnē iestatiet numuru sēriju kodus Download **ID, paziņojums ID, saskaņot ID un bankas saskaņojuma** atsauces.

## <a name="bank-account-reconciliation-options"></a>Bankas kontu saskaņošanas opcijas
Vispirms ir jāiespējo papildu bankas saskaņojums par bankas kontu.  Vairākas papildu opcijas ir pieejamas **bankas konta** lapa, kad papildu bankas saskaņošanas funkcija tiek iespējota. 

**Izmantot bankas kontu izrakstus, kā apstiprinājums par elektronisko maksājumu** funkcionalitāti integrē bankas saskaņojuma funkcionalitāti ar elektronisko maksājumu statusiem.  Kad šī atslēga ir aktivizēta, bankas dokumentu automātiski tiks izveidota elektronisko maksājumu statuss ir iestatīts **Sent**.  Turklāt elektronisko maksājumu statuss tiks atjaunināts no **Sent** uz **Received** pēc tam, kad maksājums ir saskaņota, saskaņota un grāmatots. 

**Bankas konta nosaukumu pārskatos** lauks ir nosaukums, ko izmanto bankas konta uz elektronisko banku pārskatiem.  Šis nosaukums tiek lietots nosakot kādas darbības importēt bankas konta izrakstā, kas var saturēt informāciju vairākus bankas kontus. 

Iespēja **saskaņot pēc importa** tiks automātiski apstiprināt bankas izrakstā, izveidot jaunu bankas saskaņojumu un darblapas un palaist noklusējumā atbilstošus noteikumu kopu.  Šī funkcionalitāte automatizē procesu līdz vietai, no darbībām, kas ir manuāli saskaņotas.  Banku kontu iestatījumu noklusējuma importēšanas.


