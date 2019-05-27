---
title: Gada beigu slēgšana
description: Šajā tēmā ir aprakstīti nepieciešamie iestatījumi un darbības, kas ir jāveic, lai izpildītu Virsgrāmatas gada slēgšanas procesu.
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ec2316dd259cd12a5cab187b08dbd17ca100572
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567241"
---
# <a name="year-end-close"></a>Gada beigu slēgšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti nepieciešamie iestatījumi un darbības, kas ir jāveic, lai izpildītu Virsgrāmatas gada slēgšanas procesu. 

Finanšu gada beigās ir jāizpilda gada slēgšanas process, lai sākuma bilances pārsūtītu uz jauno gadu. Vairumā organizāciju gada beigu slēgšanas process tiek izpildīts vairākas reizes. Pirmo reizi tas tiek darīts, lai pārvietotu bilances uz jauno finanšu gadu. Pēc tam gada beigu slēgšanu var izpildīt vēlreiz tik reižu, cik tas ir nepieciešams, lai pārvietotu bilances no koriģējošajiem ierakstiem uz jauno finanšu gadu. 

Gada beigu slēgšanas procesa laikā var tikt izveidotas divu veidu transakcijas. Vienmēr tiek izveidota sākuma transakcija, kas tiek izmantota, lai izveidotu sākuma bilances jaunajā finanšu gadā. Sākuma transakcija parāda bilances Virsgrāmatas konta bilances jaunajā finanšu gadā un bilances no peļņas un zaudējumu Virsgrāmatas konta bilancēm nesadalītās peļņas Virsgrāmatas kontā jaunā finanšu gadā. Pēc izvēles tiek izveidota slēgšanas transakcija, kas līdz nullei samazina peļņas un zaudējumu kontu bilances slēdzamajā finanšu gadā.

## <a name="prepare-to-run-the-year-end-close"></a>Sagatavošanās gada beigu slēgšanas izpildei
Pirms gada beigu slēgšanas procesa izpildes pārbaudiet tālāk norādītos iestatījumus. 

Lapā **Galvenais konts**:

-   Pārbaudiet, vai katram galvenajam kontam ir pareizi definēta lauka **Galvenā konta tips** vērtība. Lauks Galvenā konta tips tiek izmantots, lai noteiktu, vai galvenā konta bilance tiek turpmāk lietota kā sākuma bilance vai tiek slēgta nesadalītajā peļņā sākuma transakcijas ietvaros.
-   Lauku **Sākuma konts** var izmantot, lai gada beigu slēgšanas laikā galvenā konta bilanci pārsūtītu uz jaunu galveno kontu. Jauno galveno kontu var norādīt laukā **Sākuma konts**. Parasti tas tiek izmantots bilances galvenajiem kontiem gadījumā, ja galvenais konts ir deaktivizēts un jaunajam finanšu gadam tiek izmantots jauns galvenais konts.

Lapas **Virsgrāmatas parametri** sadaļā **Finanšu gada slēgšana**

-   Opcija **Dzēst gada slēgš. darbības** tiek izmantota, lai norādītu, vai, atkārtoti izpildot gada beigu slēgšanu, ir jādzēš iepriekšējās gada beigu slēgšanas laikā sistēmā ģenerētā sākuma transakcija. Ja ir iestatīta šīs opcijas vērtība **Jā**, iepriekšējā sākuma transakcija tiek dzēsta un tiek izveidota jauna sākuma transakcija, pamatojoties uz pašreizējām bilancēm. Ja ir iestatīta šīs opcijas vērtība **Nē**, iepriekšējā sākuma transakcija tiek saglabāta un tiek izveidota papildu sākuma transakcija, lai pārvietotu turpmākai lietošanai bilances no koriģējošajām transakcijām, kas ir grāmatotas pēc iepriekšējās gada beigu slēgšanas.
-   Opcija **Izveidot slēguma darbības pārsūtīšanas laikā** tiek izmantota, lai slēdzamajā finanšu gadā izveidotu slēgšanas transakcijas, kas līdz nullei samazina peļņas un zaudējumu kontu bilances. Ja ir iestatīta šīs opcijas vērtība **Jā**, tiek izveidota gan sākuma darbība, gan slēgšanas darbība. Ja ir iestatīta šīs opcijas vērtība **Nē**, finanšu gadā tiek izveidota tikai sākuma transakcija, kas pārsūta bilances. Peļņas un zaudējumu konta bilances paliek finanšu gada beigās.
-   Opcija **Iestatīt finanšu gada statusu kā neatgriezeniski slēgtu** tiek izmantota, lai iestatītu finanšu gada neatgriezeniskas slēgšanas statusu. Izmantojiet šo iestatījumu piesardzīgi, jo nevienu periodu, kam ir neatgriezeniskas slēgšanas statuss, nevar atkārtoti atvērt, tāpēc finanšu gadā nevar grāmatot korekcijas. Ir ieteicams iestatīt šis opcijas vērtību **Nē**.
-   Opcija **Jānorāda dokumenta numurs** tiek izmantota, lai norādītu, vai, izpildot gada beigu slēgšanas procesu, ir obligāti jānorāda dokumenta numurs. Ir ieteicams norādīt, ka dokumenta numurs ir obligāti jāievada, lai varētu viegli identificēt sākuma transakciju.

Lapā **Finanšu kalendārs**

-   Pirms gada beigu slēgšanas izpildes ir jābūt izveidotam nākamajam finanšu gadam. Nākamais finanšu gads ir nepieciešams, lai izveidotu sākuma bilances sākuma periodā.

Lapā **Virsgrāmatas kalendārs**

-   Pēc izvēles: katram slēdzamā finanšu gada finanšu periodam var iestatīt statusu **Aizturēts**, lai nepieļautu jaunu transakciju ievadi. Kad ir identificēti koriģējošie ieraksti, aizturētos periodus var atkārtoti atvērt, lai grāmatotu koriģējošos ierakstus, pat tad, ja jau ir izpildīts gada beigu slēgšanas process.

## <a name="define-year-end-close-templates"></a>Gada beigu slēgšanas veidņu definēšana
Pēc sistēmas konfigurēšanas var izpildīt gada beigu slēgšanas procesu. Lapā **Gada beigu slēgšana** var definēt veidni juridisko personu grupai, kam tiks izpildīts gada beigu slēgšanas process. Veidne tiek atkārtoti lietota katrā gada beigu slēgšanas procedūrā, taču to var modificēt atbilstoši organizācijas izmaiņām. 

Vispirms norādiet veidnes parametru **Grupas nosaukums** un atlasiet finanšu gadu. Grupas nosaukumam ir jāatbilst iekļautajai juridisko personu grupai.  Piemēram, veidnes var iestatīt, pamatojoties uz ģeogrāfiskās atrašanās vietas, izmantojot atsevišķas grupas, kas ir izveidotas Ziemeļamerikas juridiskajām personām, EMEA juridiskajām personām un APAC juridiskajām personām. 

Pēc tam veidnei var pievieno juridiskās personas. Juridiskās personas var pievienot, atlasot organizācijas hierarhiju vai juridiskās personas. Ja tiek atlasīta organizācijas hierarhija, veidnei tiek pievienotas tikai tās hierarhijā iekļautās juridiskās personas, kas izmanto atlasīto fiskālo kalendāru. Ja atlasāt veidnei pievienojamās juridiskās personas, tiek pievienotas tikai tās juridiskās personas, kas izmanot vienu un to pašu finanšu kalendāru. Viens un tas pats fiskālais kalendārs ir nepieciešams, jo gada beigu slēgšana tiek izpildīta, atlasot finanšu gadu, kas var atšķirties dažādos kalendāros. 

Pēc juridisko personu pievienošanas definējiet katras juridiskās personas nesadalītās peļņas galvenos kontus. Lauks **Pēdējās gada beigu slēgšanas datums** tiek atjaunināts ikreiz, kad juridiskajai personai tiek izpildīta gada beigu slēgšana. 

Cilne **Finanšu dimensija** tiek izmantota, lai definētu, kuras finanšu dimensijas tiks izmantotas sākuma transakcijā. Ņemiet vērā, ka definētie iestatījumi attiecas tikai uz to juridisko personu, kas ir atlasīta režģī **Juridiskās personas**. Šie iestatījumi ir jāatkārto ar katru režģī iekļauto juridisko personu. 

Opcija **Pārsūtīt bilances dimensijas** tiek izmantota, lai definētu, vai sākuma transakcijās ir jāsaglabā bilances kontos grāmatoto transakciju finanšu dimensijas. Ir ieteicams iestatīt šīs opcijas vērtību **Jā**. Opcija **Pārsūtīt peļņas un zaudējumu dimensijas** tiek izmantota, lai definētu, kuras peļņas un zaudējumu kontā grāmatoto transakciju finanšu dimensijas ir jāpārsūta uz nesadalītās peļņas galveno kontu. Vispirms identificējiet ar atlasīto juridisko personu saistītās finanšu dimensijas. Tas attiecas uz visām finanšu dimensijām, kas ir izmantotas grāmatošanai šī gada laikā, pat tad, ja finanšu dimensija nav ietverta aktīvā konta struktūrā. Pēc tam iestatiet katrai dimensijai opciju **Slēgt vienu** vai **Slēgt visu**.  Noklusējuma iestatījums ir **Slēgt visu**, kas nodrošina grāmatoto transakciju sākotnējo finanšu dimensiju vērtību saglabāšanu un izmantošanu nesadalītās peļņas konta sākuma bilanču izveidei. Katrai unikālajai finanšu dimensiju vērtību kombinācijai tiek izveidota atsevišķa nesadalītās peļņas sākuma bilance. Ja ir atlasīta opcija **Slēgt vienu**, visas ar šo finanšu dimensiju grāmatotās transakcijas tiek summētas nesadalītās peļņas sākuma bilancē tai dimensijas vērtībai, kas ir ievadīta laukā aiz opcijas **Slēgt vienu**. Piemēram, pieņemsim, ka visas finanšu gada transakcijas tika grāmatotas, izmantojot konta struktūru Galvenais konts — Nodaļa. Veidnes finanšu dimensijas Nodaļa sadaļā ir atlasīta opcija **Slēgt vienu** un ir ievadīta vērtība 100. Ja visu nodaļā Nr. 200, 300 un 400 grāmatoto transakciju ieņēmumu kopsumma ir $ 100 00, tiek izveidota viena nesadalītās peļņas sākuma bilance — 100. Ja atlasāt opciju **Slēgt vienu** un atstājat finanšu dimensijas vērtību tukšu, nesadalītajā peļņā tiek grāmatotas visas transakcijas, kurām šī dimensijas vērtība ir tukša. 

Gada beigu slēgšanas process nav atkarīgs no kontu struktūrām. Tā ir tāpēc, ka kontu struktūras var tikt mainītas finanšu gada laikā un šo izmaiņu dēļ dažreiz nevar identificēt saistīto konta struktūru.  Izveidojot sākuma transakcijas, turpmākai lietošanai tiek pārvietotas bilances ar finanšu dimensijām, kas ir definētas gada beigu slēgšanas veidnē. Sākuma bilanču ierakstos var būt iekļautas finanšu dimensijas, kas vairs nav ietvertas pašreizējā konta struktūrā, un segmentu kombinācijas, kas vairs nav derīgas pašreizējā konta struktūrā. Ja organizācija vēlas izslēgt finanšu dimensiju no nesadalītās peļņas sākuma bilances, iestatiet finanšu dimensijai opciju **Slēgt vienu** un atstājiet dimensijas vērtību tukšu.

## <a name="run-the-year-end-close-process"></a>Gada beigu slēgšanas procesa izpilde
Pēc gada beigu slēgšanas veidņu izveides gada beigu slēgšanas procesu var aktivizēt, darbību rūtī izvēloties opciju **Izpildīt finanšu gadu**. Atlasiet visas juridiskās personas vai juridisko personu apakškopu no veidnes, kurai ir jāizpilda gada beigu slēgšana. Pirmo reizi finanšu gada laikā izpildot gada beigu slēgšanu, iespējams, izvēlēsities visas juridiskās personas, lai izveidotu visu juridisko personu sākuma bilances. Atkārtoti izpildot gada beigu slēgšanu, varat izvēlēties izpildīt procesu tikai tām juridiskajām personām, kam ir grāmatoti koriģējošie ieraksti. 

Atlasiet finanšu gadu, kam vēlaties izpildīt gada beigu slēgšanu. Ja finanšu gada pēdējam periodam ir vairāki slēgšanas periodi, kļūst pieejams lauks **Perioda nosaukums**, lai varētu atlasīt, kurā slēgšanas periodā grāmatot slēgšanas transakciju gadījumā, ja ir iestatīta slēgšanas transakcijas izveide. 

Ievadiet dokumenta numuru, kas ir vai nav obligāti jāievada atkarībā no iestatījumiem sadaļā Virsgrāmatas parametri. Visiem Virsgrāmatas ierakstiem, kas ir atlasīti gada beigu slēgšanas procesam, tiek izmantots viens un tas pats dokumenta numurs. Dokumenta numurs netiek ģenerēts, izmantojot numuru sēriju. Ir ieteicams ievadīt dokumenta numuru pat tad, ja tas nav obligāti jāievada. Dokumenta numura ievadīšana atvieglo sākuma transakcijas atrašanu jaunajā finanšu gadā. Ja dokumenta numurs netiek ievadīts, sākuma transakcijas dokuments ir tukšs. 

Ja vēlaties atsaukt iepriekš veiktu atlasītā finanšu gada beigu slēgšanu, iestatiet opcijas **Atsaukt iepriekšējo slēgšanu** vērtību **Jā**. Gada beigu slēgšana tiek atsaukta, taču procesu var atkārtoti izpildīt jebkurā brīdī. Ja atsaucat gada beigu slēgšanu, nav pieejams lauks **Pēdējās gada beigu slēgšanas datums**. 

Gada beigu slēgšanas process pēc noklusējuma tiek veikts pakešveida režīmā. Ir ieteicams izpildīt procesu pakešveida režīmā, lai lietotājs varētu veikt citas darbības. Pēc gada beigu slēgšanas procesa pabeigšanas lauks **Pēdējās gada beigu slēgšanas datums** tiek atjaunināts, norādot sesijas datumu.

Papildinformāciju skatiet šeit: [Slēgt virsgrāmatu perioda beigās](close-general-ledger-at-period-end.md) un [Slēgt finanšu gadu](tasks/close-fiscal-year.md).



