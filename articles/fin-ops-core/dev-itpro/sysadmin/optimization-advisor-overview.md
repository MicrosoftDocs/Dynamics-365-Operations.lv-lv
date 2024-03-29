---
title: Optimizācijas padomnieka pārskats
description: Šajā rakstā ir aprakstīts, kā var lietot optimizācijas iestatījumu, lai palīdzētu nodrošināt optimālu finanšu un operāciju konfigurāciju.
author: kamaybac
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: f24e8dfecb04f928994bb5a197d32a7279022512
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281361"
---
# <a name="optimization-advisor-overview"></a>Optimizācijas padomnieka pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā var lietot optimizācijas iestatījumu, lai palīdzētu nodrošināt optimālu finanšu un operāciju konfigurāciju.

## <a name="overview"></a>Pārskats

Nepareiza moduļa konfigurācija iestatījumi var negatīvi ietekmēt līdzekļu pieejamību, sistēmas veiktspēju un biznesa procesu sekmīgu norisi. Biznesa datu kvalitāte (piemēram, pareizību, pilnīgumu un datu precizitāti) ietekmē arī sistēmas veiktspēju, kā arī organizācijas lēmumu pieņemšanas iespējas, produktivitāti u. c. faktorus.

Darbvieta **Optimizācijas padomnieks** ir rīks, kas ļauj prasmīgiem lietotājiem, biznesa analītiķiem, funkcionālajiem konsultantiem un IT atbalsta dienesta funkcijām identificēt moduļa konfigurācijas un biznesa datu problēmas. Optimizācijas padomnieks piedāvā labākās moduļa konfigurēšanas prakses un identificē novecojušus vai nepareizus biznesa datus.

Optimizācijas padomnieks periodiski izpilda labākās prakses kārtulu kopu. Ir pieejams noteikumu noklusējuma kopums, tomēr lietotāji var arī izveidot kārtulas, kas ir īpaši paredzētas lietotāju pielāgojumiem, neatkarīgu programmatūras izstrādātāju (ISV) risinājumiem un biznesa datiem. Papildinformāciju par kārtulu veidošanu skatiet sadaļā [Optimizācijas padomnieka kārtulu izveide](./create-rules-optimization-advisor.md).

Ja tiek noteikts kārtulas pārkāpums, tiek ģenerēta optimizācijas iespēja, kas parādās darbvietā **Optimizācijas padomnieks**. Lietotājs var veikt atbilstošos labojumus tieši darbvietā **Optimizācijas padomnieks**.

Iespējas atkarībā no iestatījumu un pārbaudīto datu veida var būt paredzētas noteiktam uzņēmumam, vai arī tās var būt starpuzņēmumu iespējas. Starpuzņēmumu iespējas var skatīt visos uzņēmumos. Lai skatītu noteiktam uzņēmumam paredzētās iespējas, vispirms ir jāatlasa uzņēmums.

Uz optimizācijas iespējām attiecas standarta drošības politikas. Piemēram, optimizācijas iespējas, kas ir saistītas ar moduļa **Noliktavas pārvaldība** konfigurāciju, ir redzamas tikai tiem lietotājiem, kuriem ir piekļuve modulim “Noliktavas pārvaldība” un kuri var mainīt šī moduļa iestatījumus.

Kad jūs izmantojat kādu no optimizācijas iespējām, sistēma aprēķina iespējas ietekmi uz biznesa procesu izpildlaika samazināšanos. Diemžēl, šis līdzeklis nav pieejams visām optimizācijas iespējām.

Lai iegūtu plašāku informāciju par optimizācijas spēcīgāku [informāciju, skatiet īsu optimizācijas iestatījumu programmā Dynamics 365 Finance](https://www.youtube.com/watch?v=MRsAzgFCUSQ) video.

## <a name="optimization-rules"></a>Optimizācijas kārtulas

Lai skatītu pilnu optimizācijas padomnieka kārtulu sarakstu un lai redzētu, cik bieži kārtulas tiek novērtētas, dodieties uz **Sistēmas administrēšana** &gt; **Periodiskie uzdevumi** &gt; **Uzturēt diagnostikas apstiprināšanas kārtulu**. Tiek novērtētas tikai tās kārtulas, kurām ir statuss **Aktīva**. Novērtēšanas biežumam var atlasīt iestatījumus **Katru dienu**, **Katru nedēļu**, **Katru mēnesi** vai **Neplānoti**.

Lai aktivizētu neplānotu kārtulu novērtēšanu vai lai atkārtoti novērtētu periodiskās kārtulas ārpus iepriekš noteiktā grafika, dodieties uz **Sistēmas administrēšana** &gt; **Periodiskie uzdevumi** &gt; **Ieplānot diagnostikas apstiprināšanas kārtulu**. Pēc tam dialoglodziņā **Diagnostikas kārtulas apstiprināšana** atlasiet novērtēšanas biežumu. Visas kārtulas, kurām ir atlasīts norādītais biežums, tiks atkārtoti novērtētas.

Optimizācijas kārtulu pašreizējo kopu var iedalīt tālāk norādītajās kategorijās.

### <a name="module-configuration-and-setup"></a>Moduļa iestatīšana un konfigurēšana

Moduļa “Noliktavas pārvaldība” iestatīšana ir sarežģīts process. Lai atvieglotu procesu un palīdzētu pārbaudīt iestatījumu pareizību, ir ieviestas dažas kārtulas. Piemēram, viena kārtula pārbauda noliktavas novietojuma direktīvas iestatījumus pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu fiksētajiem preces varianta novietojumiem.

Turklāt dažas kārtulas pārbauda, vai iespējotie līdzekļi tiek izmantoti. Piemēram, viena no kārtulām nosaka, vai izmantojat moduli **Vispārējā plānošana**. Ja kārtula nosaka, ka jūs moduli neizmantojat, tiek ģenerēta optimizācijas iespēja, kas ieteiks izslēgt plānošanas procesus.

### <a name="system-configuration"></a>Sistēmas konfigurācija

Ja netiek izmantota īpaša funkcionalitāte, kuras vadībai ir nepieciešama konfigurācijas atslēga, tiek ģenerēta optimizācijas iespēja, kas ieteiks atspējot konfigurācijas atslēgu. Konfigurācijas atslēgu piemēri: **Pieļaujamais svars**, **Budžeta plānošana**, **Projekts** un **Apstiprināto piegādātāju saraksts**.

### <a name="business-data-consistency-and-cleanup"></a>Biznesa datu konsekvence un tīrīšana

Ja pamatdati nav pareizi (piemēram, ja ir pārveidotas nedefinētas mērvienības vai ja pārveidotās mērvienības ir dalītas ar 0 \[nulle\]), tiek ģenerēta optimizācijas iespēja, kas ieteiks izlabot datus. 

Ja jums ir pārāk daudz pakešuzdevumu vēstures ierakstu, novecojušu krājumu, slēgtu rīcībā esošo ierakstu noliktavas iespējotajiem krājumiem u. c. ierakstu vai ja šie ieraksti un krājumi ir pārāk veci, tiek ģenerēta optimizācijas iespēja, kas ieteiks iztīrīt datus. Iztīrot datus, varat palīdzēt uzlabot sistēmas veiktspēju kopumā.

### <a name="best-practices"></a>Noteikumi

Ja jūs neizmantojat dažus no labākās prakses ieteiktajiem biznesa procesiem (piemēram, ja tiek veikta krājumu pirmsslēgšana pirms krājumu slēgšanas vai ja apakšgrāmatas žurnāla partijas pārsūtīšanai tiek izmantota plānota partija), optimizācijas iespējas jūs informēs par labāko praksi un lūgs to ievērot.

## <a name="optimization-opportunities"></a>Optimizācijas iespējas

Lai skatītu optimizācijas iespējas, kas tiek ģenerētas optimizācijas kārtulu novērtēšanas laikā, atveriet darbvietu **Optimizācijas padomnieks**.

Šajā darbvietā, jūs varat skatīt plašāku informāciju par iespēju, atlasot **Papildinformācija**. Ja vēlaties, lai sistēma reaģētu un labotu iestatījumus, iztīrītu datus un veiktu citas darbības un jums pašam nebūtu jāatver atbilstošās lapas, atlasiet **Rīkoties**.

Optimizācijas iespējām nav darbplūsmas. Pēc **Rīkoties** atlasīšanas vai pēc dialoglodziņā **Papildinformācija** nodrošinātā navigācijas ceļa izmantošanas optimizācijas iespēja pazūd no saraksta. Ja labošanas darbība problēmu pilnībā neatrisina, nākamajā kārtulas novērtēšanas reizē iespēja tiks ģenerēta vēlreiz.

Ja iespēja neattiecas uz jūsu lomu, jūs varat atlasīt **Nerādīt manā sarakstā**. Pat ja kārtula, kas ir saistīta ar šo iespēju, vēlāk tiks palaista vēlreiz, jūs neredzēsiet šo iespēju savā sarakstā.

Lai deaktivizētu noteiktu kārtulu novērtēšanu, atlasiet kārtulas ģenerēto iespēju un pēc tam atlasiet **Deaktivizēt analīzi**.

## <a name="additional-resources"></a>Papildu resursi

[Kārtulu izveide optimizācijas padomniekam](./create-rules-optimization-advisor.md)

[Optimizācijas izmaiņas Dynamics 365 finansēs (Video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
