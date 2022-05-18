---
title: Gada beigu slēgšana
description: Šajā tēmā ir aprakstīti nepieciešamie iestatījumi un darbības, kas ir jāveic, lai izpildītu Virsgrāmatas gada slēgšanas procesu.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 247c3286124da946937c8afd248a275e5a745044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725238"
---
# <a name="year-end-close"></a>Gada beigu slēgšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti nepieciešamie iestatījumi un darbības, kas ir jāveic, lai izpildītu Virsgrāmatas gada slēgšanas procesu.

Finanšu gada beigās ir jāizpilda gada slēgšanas process, lai sākuma bilances pārsūtītu uz jauno gadu. Vairumā organizāciju gada beigu slēgšanas process tiek izpildīts vairākas reizes. Pirmā izpilde pārvieto bilances uz jauno finanšu gadu. Pēc tam procesu var izpildīt vēlreiz tik reižu, cik tas ir nepieciešams, lai pārvietotu bilances no koriģējošajiem ierakstiem uz jauno finanšu gadu.

Gada beigu slēgšanas procesa laikā var tikt izveidotas divu veidu transakcijas. Vienmēr tiek izveidota sākuma transakcija, kas tiek izmantota, lai izveidotu sākuma bilances jaunajā finanšu gadā. Sākuma transakcija parāda bilances Virsgrāmatas konta bilances jaunajā finanšu gadā un bilances no peļņas un zaudējumu Virsgrāmatas konta bilancēm nesadalītās peļņas Virsgrāmatas kontā jaunā finanšu gadā. Pēc izvēles tiek izveidota slēgšanas transakcija, kas līdz nullei samazina peļņas un zaudējumu kontu bilances slēdzamajā finanšu gadā.

## <a name="prepare-to-run-the-year-end-close"></a>Sagatavošanās gada beigu slēgšanas izpildei

Pirms gada beigu slēgšanas procesa izpildes pārbaudiet tālāk norādītos iestatījumus.

Lapā **Galvenais konts**:

- Pārbaudiet, vai lauks **Galvenā konta tips** katram galvenajam kontam ir iestatīts pareizi. Galvenā konta tips noteic, vai galvenā konta bilance tiek turpmāk lietota kā sākuma bilance vai tiek slēgta nesadalītajā peļņā sākuma transakcijas ietvaros.
- Galvenā konta bilanci var pārsūtīt uz jaunu galveno kontu gada beigu slēgšanas laikā. Ievadiet jauno galveno kontu laukā **Sākuma konts**. Parasti šis lauks tiek izmantots bilances galvenajiem kontiem gadījumā, ja galvenais konts ir deaktivizēts un jaunajam finanšu gadam tiek izmantots jauns galvenais konts.

Lapas **Virsgrāmatas parametri** sadaļā **Finanšu gada slēgšana**

- Opcija **Dzēst esošos gada beigu ierakstus, atkārtoti aizverot gadu** tiek izmantota, lai norādītu, vai, atkārtoti izpildot gada beigu slēgšanu, ir jādzēš iepriekšējās gada beigu slēgšanas laikā sistēmā ģenerētā sākuma transakcija. Ja ir iestatīta šīs opcijas vērtība **Jā**, iepriekšējā sākuma un izvēles slēgšanas transakcijas tiek dzēstas un tiek izveidota jauna sākuma vai beigu transakcija, pamatojoties uz pašreizējām bilancēm. Ja ir iestatīta šīs opcijas vērtība **Nē**, iepriekšējā sākuma un izvēles slēgšanas transakcijas tiek saglabātas un tiek izveidota papildu sākuma vai beigu transakcija, lai pārvietotu turpmākai lietošanai bilances no koriģējošajām transakcijām, kas ir grāmatotas pēc iepriekšējās gada beigu slēgšanas.
- Opcija **Izveidot slēgšanas darbības** pārsūtīšanas laikā tiek lietota, lai izveidotu slēguma darbības slēgtajā finanšu gadā, lai visu galveno kontu bilances būtu 0 (nulle). Ja ir iestatīta šīs opcijas vērtība **Jā**, tiek izveidotas gan sākuma darbība, gan slēgšanas darbība. Ja ir iestatīta šīs opcijas vērtība **Nē**, finanšu gadā tiek izveidota tikai sākuma transakcija, kas pārsūta bilances. Galvenā konta bilances paliek finanšu gada beigās.
- Opcija **Iestatīt finanšu gada statusu kā neatgriezeniski slēgtu** tiek izmantota, lai iestatītu finanšu gada neatgriezeniskas slēgšanas statusu. Uzmanīgi lietojiet šo opciju, jo periodus, kuriem ir neatgriezenisks slēgts statuss, nevar atvērt atkārtoti. Tāpēc korekcijas nevar grāmatot finanšu gadā. Kā labākā prakse šī iespēja būtu jāiestata kā **Nē**.
- Opcija **Dokumenta numuram jābūt aizpildītam** ir noņemta. Dokuments ir nepieciešams, kad tiek izpildīts gada beigu slēgšanas process. Tajā laikā dokumenta numurs tiek ievadīts manuāli.

Lapā **Finanšu kalendārs**

- Pirms gada beigu slēgšanas izpildes ir jābūt izveidotam nākamajam finanšu gadam. Pretējā gadījumā sākuma bilances nevar izveidot sākuma periodā.

Lapā **Virsgrāmatas kalendārs**

- Pēc izvēles: katram slēdzamā finanšu gada finanšu periodam var iestatīt statusu **Aizturēts**, lai nepieļautu jaunu transakciju ievadi. Kad ir identificēti koriģējošie ieraksti, aizturētos periodus var atkārtoti atvērt, lai koriģējošos ierakstus varētu grāmatot, pat tad, ja jau ir izpildīts gada beigu slēgšanas process.

Lapā **Gada beigu veidnes slēgšanas iestatīšana**:

- Ja ir ieslēgts līdzeklis **Virsgrāmatas gada beigu uzlabojumu**, gada beigu slēgšanas veidnes iestatīšanas process tiek atdalīts no gada beigu slēgšanas procesa. Veidni var definēt lapā **Gada beigu veidnes slēgšanas iestatījums** (**Virsgrāmata \> Virsgrāmatas iestatījums \> Gada beigu slēgšanas veidnes iestatījums**) vai arī tai var piekļūt no gada beigu slēgšanas procesa.

## <a name="define-year-end-close-templates"></a>Gada beigu slēgšanas veidņu definēšana

Pēc sistēmas konfigurēšanas var izpildīt gada beigu slēgšanas procesu. Lapā **Gada beigu slēgšanas veidnes iestatījums** var definēt veidni juridisko personu grupai, kam tiks izpildīts gada beigu slēgšanas process. Veidne tiek atkārtoti lietota katrā gada beigu slēgšanas procedūrā, taču to var modificēt atbilstoši organizācijas izmaiņām.

Vispirms iestatiet veidnes lauku **Grupas nosaukums** un atlasiet finanšu gadu. Grupas nosaukumam ir jāatbilst iekļautajai juridisko personu grupai. Nosakot juridisko personu grupas, atcerieties, ka juridiskās personas var iekļaut tajā pašā grupā tikai tad, ja tām ir atlasīts viens finanšu kalendārs. Piemēram, veidnes var iestatīt, pamatojoties uz ģeogrāfiskās atrašanās vietas, un atsevišķas grupas var izveidot Ziemeļamerikas juridiskajām personām, Eiropas, Tuvo Austrumu un Āfrikas (EMEA) juridiskajām personām un Āzijas un Klusā okeāna reģiona (APAC) juridiskajām personām.

Pēc tam veidnei var pievieno juridiskās personas. Juridiskās personas var pievienot, atlasot organizācijas hierarhiju vai juridiskās personas. Ja tiek atlasīta organizācijas hierarhija, veidnei tiek pievienotas tikai tās hierarhijā iekļautās juridiskās personas, kas izmanto atlasīto fiskālo kalendāru. Ja atlasāt veidnei pievienojamās juridiskās personas, tiek pievienotas tikai tās juridiskās personas, kas izmanot vienu un to pašu finanšu kalendāru. Viens un tas pats fiskālais kalendārs ir nepieciešams, jo gada beigu slēgšana tiek izpildīta, atlasot finanšu gadu, kas var atšķirties dažādos kalendāros.

Pēc juridisko personu pievienošanas definējiet katras juridiskās personas nesadalītās peļņas galvenos kontus.

Cilne **Finanšu dimensija** tiek izmantota, lai definētu, kuras finanšu dimensijas tiks izmantotas sākuma transakcijā. Ievērojiet, ka šīs cilnes iestatījumi attiecas tikai uz to juridisko personu, kura ir atlasīta režģī **Juridiskās personas**. Šie iestatījumi ir jāatkārto ar katru režģī iekļauto juridisko personu.

Opcija **Pārsūtīt bilances dimensijas** tiek izmantota, lai norādītu, vai sākuma transakcijās ir jāsaglabā bilances kontos grāmatoto transakciju finanšu dimensijas. Kā labākā prakse šī iespēja būtu jāiestata kā **Jā**. Bilances dimensiju iestatījums neietekmē esošās bilances nesadalītās peļņas virsgrāmatas kontos. Šīs bilances tiek noteiktas pēc peļņas un zaudējumu dimensijām, kas definētas nākamajā sadaļā. Piemēram, 2019. finanšu gads bija pirmais gads, kas tika slēgts, un opcija **Aizvērt visu** tika izmantota, lai slēgšanai atlasītu dimensiju **Nodaļa** un **Izmaksu centrs**. Šajā gadījumā katrai nodaļas un izmaksu centra kombinācijai tika izveidots atsevišķs nesadalītās peļņas konts. Ja gada beigu slēgšana ir izpildīta 2020. finanšu gadam, nesadalītā peļņa no iepriekšējā gada paliek tieši tāpat, kā tika grāmatota, pat ja **Pārsūtīšanas bilances dimensijas** ir iestatītas uz **Nē**. Bilances, kas grāmatotas iepriekšējā gada beigu slēgšanas nesadalītā peļņā, nekad netiek mainītas.

Sadaļa **Pārsūtīt peļņas un zaudējumu dimensijas** tiek izmantota, lai norādītu, kuras peļņas un zaudējumu kontos grāmatoto transakciju finanšu dimensijas ir jāpārsūta uz nesadalītās peļņas galveno kontu. Vispirms identificējiet ar atlasīto juridisko personu saistītās finanšu dimensijas. Šīs finanšu dimensijas attiecas uz visām finanšu dimensijām, kas tika izmantotas grāmatošanai šī gada laikā, pat tad, ja finanšu dimensija nav ietverta aktīvā konta struktūrā. Pēc tam iestatiet katrai dimensijai opciju **Slēgt vienu** vai **Slēgt visu**. Noklusējuma opcija ir **Aizvērt visu**. Šī opcija nodrošina grāmatoto transakciju sākotnējo finanšu dimensiju vērtību saglabāšanu un izmantošanu nesadalītās peļņas konta sākuma bilanču izveidei. Katrai unikālajai finanšu dimensiju vērtību kombinācijai tiek izveidota atsevišķa nesadalītās peļņas sākuma bilance. Ja ir atlasīta opcija **Slēgt vienu**, visas grāmatotās transakcijas, kurām ir šī finanšu dimensija, tiek summētas nesadalītās peļņas sākuma bilancē tai dimensijas vērtībai, kas ir ievadīta laukā, kas parādās pēc opcijas **Slēgt vienu**. Piemēram, visas finanšu gada transakcijas tika grāmatotas, izmantojot konta struktūru **Galvenais konts — Nodaļa**. Finanšu dimensijai **Nodaļa** veidnē ir atlasīta opcija **Slēgt vienu** un ir ievadīts **100** kā dimensijas vērtība. Ja visu nodaļā Nr. 200, 300 un 400 grāmatoto transakciju ieņēmumu kopsumma ir $100 000, tiek izveidota viena sākuma bilance opcijai **Nesadalītā peļņa - 100**. Ja atlasāt opciju **Slēgt vienu**, bet atstājat finanšu dimensijas vērtību tukšu, nesadalītajā peļņā tiek grāmatotas visas transakcijas, un dimensijas vērtība būs tukša.

## <a name="run-the-year-end-close-process"></a>Gada beigu slēgšanas procesa izpilde

Pēc tam, kad ir izveidotas gada beigu slēgšanas veidnes, gada beigu slēgšanas procesu var sākt lapā **Gada beigu slēgšana** (**Virsgrāmata \> Perioda slēgšana \> Gada beigu slēgšana**). Pirms gada beigu slēgšanas varat pievienot jaunas gada beigu slēgšanas veidnes vai modificēt esošās veidnes, atlasot **Gada beigu veidnes iestatījums**, lai atvērtu veidņu iestatīšanas lapu.

Atlasiet gada beigu slēgšanas veidni un pēc tam Darbību rūtī atlasiet **Izpildīt gada beigu slēgšanu**. Atlasīt vai nu visas juridiskās personas vai juridisko personu apakškopu no veidnes, kurai ir jāizpilda gada beigu slēgšana. Pirmo reizi finanšu gada laikā izpildot gada beigu slēgšanu, iespējams, izvēlēsities visas juridiskās personas, lai izveidotu sākuma bilances tām visām. Ja esat iepriekš veicis gada beigu slēgšanu, iespējams, vēlēsities to atkārtoti palaist tikai tām juridiskajām personām, kurām grāmatoti koriģējošie ieraksti.

Pēc tam atlasiet finanšu gadu, kam izpildīt gada beigu slēgšanu. Ja finanšu gada pēdējam periodam pastāv vairāk nekā viens slēgšanas periods, kļūst pieejams lauks **Perioda nosaukums**. Varat atlasīt slēgšanas periodu, lai izmantotu slēgšanas darbības grāmatošanai, ja iestatījums ir definēts slēgšanas darbības izveidošanai.

Pēc tam ievadiet dokumenta numuru. Visiem Virsgrāmatas ierakstiem, kas ir atlasīti gada beigu slēgšanas procesam, tiek izmantots viens un tas pats dokumenta numurs. Dokumenta numurs netiek ģenerēts, izmantojot numuru sēriju.

Pēc noklusējuma gada beigu slēgšanas process tiek palaists pakešveida režīmā. Tādēļ pēc tās uzsākšanas varat atgriezties pie citām aktivitātēm.

Tā kā konta struktūras var mainīties visā finanšu gadā, vienmēr nevar noteikt atbilstošu konta struktūru. Tāpēc, gada beigu slēgšanas process nav atkarīgs no kontu struktūrām. Izveidojot sākuma transakcijas, turpmākai lietošanai tiek pārvietotas bilances ar finanšu dimensijām, kas ir definētas gada beigu slēgšanas veidnē. Sākuma bilanču ierakstos būs iekļautas finanšu dimensijas, kas vairs nav ietvertas pašreizējā konta struktūrā, un segmentu kombinācijas, kas vairs nav derīgas pašreizējā konta struktūrā. Ja organizācija vēlas izslēgt finanšu dimensiju no nesadalītās peļņas sākuma bilances, definējiet finanšu dimensiju kā **Slēgt vienu** un atstājiet dimensijas vērtību tukšu.

Kad process ir pabeigts, katrai juridiskas personas un finanšu gada kombinācijai tiek izveidots ieraksts. Tiks parādīti ieraksti tikai tām juridiskajām personām, kurām jums ir piekļuve. Katrs ieraksts ietver sistēmas datumu un laiku, kad process tika palaists, un tiešu saiti ar dokumentiem, kas tika izveidoti gada beigu slēgšanai.

[![Ieraksti, kas izveidoti gada beigu slēgšanas vēstures Kopsavilkuma cilnē gada beigu slēgšanas lapai](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Ja gada beigu slēgšanu izpildāt atkārtoti, jūs redzēsiet vienu vai vairākus ierakstus katrai juridiskas personas kombinācijai un finanšu gadam atkarībā no opcijas **Dzēst esošos gada beigu ierakstus, kad atkārtoti slēdzat gadu** lapā **Virsgrāmatas parametri**:

- Ja opcija ir iestatīta uz **Jā**, dokuments par iepriekšējā gada beigām tiek dzēsts. Ieraksts ir atzīmēts kā **Atcelts**, un uzspiests ar datumu un laiku, kad atcelšana tika veikta. Turklāt saite uz dokumenta numuru tiek noņemta. Kad gada beigu slēgšana ir pabeigta, jaunajam dokumentam, kas tiek izveidots, tiks izveidots jauns ieraksts.
- Ja opcija ir iestatīta uz **Nē**, iepriekšējā gada beigu slēgšanas ieraksts kopā ar saiti uz dokumentu. Katru reizi, kad no jauna tiek palaista gada beigu slēgšana, tiks izveidots jauns ieraksts kopā ar saiti uz jaunajiem dokumentiem.

## <a name="reverse-the-year-end-close-process"></a>Gada beigu slēgšanas procesa atcelšana

Lapā **Gada beigu slēgšana** varat atcelt gada beigu slēgšanu. Atlasiet ierakstu juridiskās personas un finanšu gada kombinācijai, kas jāatceļ, un pēc tam atlasiet **Atcelt gada beigu slēgšanu**. Slēgšanas process dzēš visus atvēršanas un slēgšanas dokumentus, kas tika izveidoti finanšu gadam. Ieraksts ir atzīmēts kā **Atcelts**, un uzspiests ar datumu un laiku, kad atcelšana tika veikta. Turklāt saite uz dokumenta numuru tiek noņemta. Tāpat kā gada beigu slēgšanas process, atcelšana tiek palaista pakešveida režīmā.

Izvēles rutiņa **Rādīt atcelto**, kas ir pieejama virs režģa, ļauj jums slēpt vai parādīt atsaukto gada beigu slēgšanas procesu ierakstus. Pēc tam, kad esiet pabeiguši procesu **Atcelt gada beigu slēgšanu**, iespējams, būs jāatlasa izvēles rūtiņa **Rādīt atcelto**, lai redzētu ierakstu. Varat iestatīt papildu filtrus, lai aplūkotu citu informāciju.

[![Izvēles rūtiņas Rādīt atcelto izmantošana, lai redzētu ierakstus par atsauktajiem gada beigu slēgšanas procesiem lapā Gada beigu slēgšana](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Papildinformāciju skatiet šeit: [Slēgt virsgrāmatu perioda beigās](close-general-ledger-at-period-end.md) un [Slēgt finanšu gadu](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
