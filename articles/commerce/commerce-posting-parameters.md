---
title: Commerce grāmatošanas parametri
description: Šajā tēmā aprakstīti parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649180"
---
# <a name="commerce-posting-parameters"></a>Commerce grāmatošanas parametri

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā aprakstīti parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai Microsoft Dynamics 365 Commerce. Commerce grāmatošanas parametri atrodas commerce headquarters, kas atrodas **Retail un Commerce \> Headquarters iestatīšanas \> Parametru \> Commerce parametru grāmatošanā \>**.

## <a name="periodic-discount-parameters"></a>Periodiskās atlaides parametri

Šajā tabulā uzskaitīti periodiskie atlaižu parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Grāmatot periodisko atlaidi | Šī opcija kontrolē, vai periodiskie piedāvājumi tiek grāmatoti Virsgrāmatas kontos. Periodiskās atlaides ietver komplekta atlaides, daudzuma atlaides un atlaižu piedāvājumus. Kad šis parametrs ir iespējots, papildu laukus var iestatīt sadaļā **Periodiskās** atlaides. |
| Virsgrāmatas konta veids | <p>Atlasiet konta tipu, kas tiek izmantots periodisko atlaižu grāmatošanai:</p><ul><li>**Standarta** - sistēma šajā lapā neizmanto ar atlaidi saistītos laukus. Tā vietā tā izmanto kontus, kas ir definēti **Programmas** Commerce Headquarters grāmatošanas lapā (Krājumu **vadības iestatījumu grāmatošanas \>\>\> grāmatošanas formas**).</li><li>**Periodisks** — sistēma izmanto Commerce atlaižu kontus, kas ir norādīti šīs lapas ar atlaidēm saistītajos laukos. Ja atlasāt šo opciju, jānorāda Virsgrāmatas (VG) konts katram piedāvājuma tipam (atlaide, komplekta piedāvājums, daudzums un slieksnis). Iestatot katru atlaidi, var definēt kontu. Ja atlaižu konta grāmatošanas funkcija tiek izmantota atlaižu iestatījumu lapā, tiek veikts papildu debeta ieraksts un kredīta ieraksts, lai pārklasificētu atlaižu grāmatošanu no Commerce atlaides VG konta atlaides VG kontā. Papildinformāciju skatiet sadaļā [Mazumtirdzniecības atlaides](retail-discounts-overview.md).</li></ul> |
| Grāmatot infokodu atlaidi | Šī opcija vairs netiek izmantota standarta Commerce risinājumā un tiks nolietota. |
| Grāmatot periodiskās pasūtījumu atlaides | Šī opcija kontrolē, vai mazumtirdzniecības periodiskās atlaides tiek grāmatotas Virsgrāmatā debitoru pasūtījumiem un zvanu centra pasūtījumiem. |

## <a name="inventory-update-parameters"></a>Krājumu atjaunināšanas parametri

Šajā tabulā uzskaitīti krājumu atjaunināšanas parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Ja partijas numuri nav atrasti, izmantot noklusējuma partijas ID | Šī opcija kontrolē, vai krājumiem, kam ir iespējota pakešveida partija, tiek izmantots noklusētais partijas ID, ja nav atrasti partijas numuri un ir atļauti negatīvi krājumi. |
| Noklusējuma partijas ID | Partijas numurs, ko izmantot, **ja nav atrasti krājumu partijas numuri un ir iespējots parametrs Izmantot noklusējuma partijas** ID, ja nav atrasti partijas numuri. |

## <a name="aggregation-parameters"></a>Apkopošanas parametri

Šajā tabulā uzskaitīti apkopojuma parametri, kas ir specifiski finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Noguldījums seifā | Iespējojiet šo parametru, lai apkopotu visas darbības izraksta grāmatošanas laikā un izveidotu vienu rindu žurnāla grāmatošanai, nevis atsevišķai rindai katram nomest. |
| Noguldījums bankā | Iespējojiet šo parametru, lai apkopotu visas darbības izraksta grāmatošanas laikā un izveidotu vienu rindu žurnāla grāmatošanai, nevis atsevišķai rindai katram nomest. |
| Pārdošanas transakcijas | Aktivizējiet šo parametru, lai konsolidētu darbības kā daļu no darbību pārskata grāmatošanas procesa. Ieteicams aktivizēt šo parametru. Tā iepriekš tika nosaukta **dokumentu darbībām**. |
| Neapkopot atgriešanas | Ja ir atlasīta šī opcija, grāmatojot mazumtirdzniecības pārskatu, katra atgriešanas darbība tiks grāmatota kā atsevišķs pārdošanas pasūtījums. |

## <a name="batch-processing-parameters"></a>Pakešapstrādes parametri

Šajā tabulā uzskaitīti pakešapstrādes parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Maksimālais paralēlo priekšrakstu skaits | Šis lauks nosaka pakešuzdevumu skaitu, kas tiek izmantoti vairāku izrakstu grāmatošanai. |
| Maksimālais pavedienu skaits pasūtījumu apstrādei katram pārskatam | Šis lauks parāda maksimālo pavedienu skaitu, ko pārskata grāmatošanas pakešuzdevums izmanto, lai izveidotu un izrakstītu rēķinu pārdošanas pasūtījumus vienam pārskatam. Kopējais pavedienu skaits, ko izmanto izraksta grāmatošanas procesā **, tiek aprēķināts, reizinot šī parametra vērtību ar paralēlā izraksta grāmatošanas parametra maksimālo skaitu**. Ja šī parametra vērtība ir pārāk liela, tā var negatīvi ietekmēt izrakstu grāmatošanas procesa veiktspēju. |
| Maksimālais transakcijas rindu skaits, kas iekļauts apkopojumā | Šis lauks definē to darbību rindu skaitu, kas iekļautas vienā uzkrātajā darbībā pirms jaunas darbības izveides. Apkopotās darbības tiek izveidotas, balstoties uz dažādiem apkopojuma kritērijiem, piemēram, debitoru, biznesa datumu vai finanšu dimensijām. Ņemiet vērā, ka rindas no vienas darbības netiks sadalītas dažādās uzkrātās darbībās. Tāpēc rindu skaits apkopotajā darbībā var būt nedaudz lielāks vai mazāks, balstoties uz faktoriem, piemēram, atšķirīgu preču skaitu. |
| Maksimālais pavedienu skaits veikala transakciju pārbaudei | Šis lauks nosaka maksimālo pavedienu skaitu, kas tiek izmantots darbību pārbaudei. Darbību apstiprināšana ir nepieciešama darbība, kas jāveic pirms darbības var vilkt uz pārskatiem. Dāvanu kartes kopsavilkuma cilnē Dāvanu karte, **·** **·** **kas atrodas lapā Commerce parameters**, ir jādefinē arī dāvanu kartes prece, pat ja organizācija neizmanto dāvanu kartes. |

Tabulā uzskaitītas iepriekšējās tabulas parametru ieteicamās vērtības. Šīs vērtības ir jāpārbauda un jāpiemēro izvietojuma konfigurācijai un pieejamai infrastruktūrai. Vērtības, kas pārsniedz ieteicamās vērtības, var nelabvēlīgi ietekmēt citu pakešveida apstrādi, un tās ir jāpārbauda.

| Parametrs | Ieteicamā vērtība | Detalizēti |
|-----------|-------------------|---------|
| Maksimālais paralēli grāmatojamo pārskatu skaits | <p>Iestatiet šo parametru uz pakešuzdevumu skaitu, kas pieejami pakešuzdevumu grupai, kas palaiž pārskata **darbu**.</p><p>**Vispārīga kārtula:** reizināt Application Object Server (AOS) virtuālo serveru skaitu ar pakešuzdevumu skaitu, kas ir pieejami katrā AOS virtuālajā serverī.</p> | Šis parametrs nav piederīgs, ja ir **iespējota mazumtirdzniecības pārskatu funkcija - padeves** funkcija. |
| Maksimālais pavedienu skaits pasūtījumu apstrādei katram pārskatam | Sāciet testēt vērtības ar **4**. Parasti vērtība nedrīkst pārsniegt **8**. | Šis parametrs nosaka pavedienu skaitu, kas tiek izmantots pārdošanas pasūtījumu veidojiet un iegrāmatošanai. Tas parāda pavedienu skaitu, kas ir pieejams grāmatošanai vienā pārskatā. |
| Maksimālais transakcijas rindu skaits, kas iekļauts apkopojumā | Sāciet testēt vērtības ar **1000**. Atkarībā no Commerce Headquarters konfigurācijas mazāki pasūtījumi, iespējams, būs jums līdz ar veiktspēju. | Šis parametrs nosaka rindu skaitu, kas ir iekļautas katrā pārdošanas pasūtījumā izraksta grāmatošanas laikā. Kad šis skaitlis ir sasniegts, rindas tiks sadalītas jaunā pasūtījumā. Pārdošanas rindu skaits nav tieši vienāds ar jūsu norādīto skaitu, jo sadalīšana notiek pārdošanas pasūtījuma līmenī. Tomēr skaitlis būs tuvu iestatītā numuram. Šis parametrs tiek izmantots, lai ģenerētu pārdošanas pasūtījumus mazumtirdzniecības transakcijām, kurām nav nosaukta debitora. |
| Maksimālais pavedienu skaits veikala transakciju pārbaudei | Ieteicams iestatīt šo parametru uz **4** un palielināt to tikai tad, ja sasniegt pieņemamu veiktspēju. Pavedienu skaits, ko izmanto šis process, nevar pārsniegt procesoru skaitu, kas ir pieejams pakešu serverim. Ja pavedienu skaits ir pārāk liels, var tikt ietekmēta cita pakešapstrāde. | Šis parametrs kontrolē darbību skaitu, kas konkrētā veikalā var vienlaicīgi tikt validētas. |

> [!NOTE]
> Visi iestatījumi un parametri, kas ir saistīti ar izrakstu grāmatojumiem un kas ir definēti mazumtirdzniecības veikaliem un lapā **Commerce parametri**, ir lietojami uzlabotajam izrakstu grāmatošanas līdzeklim.

## <a name="invoice-parameters"></a>Rēķina parametri

Šajā tabulā uzskaitīti rēķina parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Žurnāla nosaukums | Maksājumu žurnāla nosaukums, ko izmanto, kad tiek izveidoti debitoru maksājumu žurnāli pārdošanas pasūtījumu maksājumiem. Šis iestatījums attiecas uz visiem pasūtījumu maksājumiem, kas tiek grāmatoti pārdošanas punktā (POS), zvanu centrā un e-komercijas kanāla pasūtījumos. |
| Konta nosaukums | Maksājuma konta nosaukums. |
| Piešķirt dimensijām prioritāti pēc maksāšanas metodes | Ja ir iespējots šis karodziņš, maksājumu žurnāliem ir prioritāte pār dimensijām no maksāšanas metodes, nevis no veikala dimensijām. |
| Nodokļu aprēķina izturēšanās | Šis parametrs norāda darbību, kad izrakstu grāmatošanas laikā izveidotie pārdošanas pasūtījumi tiek norādīti rēķinā:<ul><li>**Pārrēķināt** – aprēķiniet nodokļus vēlreiz.</li><li> **Nepārrēķināt** — izmantojiet POS aprēķinātās nodokļu summas.</li></ul> |
| Žurnāla nosaukums | Žurnāla nosaukums, ko izmanto, kad tiek izveidots debitoru maksājumu žurnāls atmaksām. Šis iestatījums attiecas uz visiem pasūtījumu maksājumiem, kas tiek grāmatoti POS, zvanu centra un e-komercijas kanāla pasūtījumiem. |

## <a name="statement-parameters"></a>Izraksta parametri

Šajā tabulā uzskaitīti pārskata parametri, kas raksturīgi finanšu un fizisko darbību grāmatošanai.

| Parametrs | Apraksts |
|-----------|-------------|
| Rezervēt krājumus aprēķināšanas laikā | Kad šis parametrs ir iespējots, izraksta aprēķins īslaicīgi rezervē krājumus līdz pārskata grāmatošanai. Šis parametrs pēc noklusējuma ir atspējots, lai palīdzētu uzlabot izraksta aprēķina veiktspēju. Atjaunināto krājumu informāciju var aprēķināt, izmantojot pakešuzdevumu **Grāmatot** krājumus. Ņemiet vērā, **ka pakešuzdevums** Grāmatot krājumu vairs netiek [izmantots, ja mazumtirdzniecības](trickle-feed.md) veikala darbībām ir iespējota no mazumtirdzniecības veikala atkarīga pasūtījuma izveide. |
| Atspējot nepieciešamo uzskaiti | Šis karodziņš atspējo skaitīšanu grāmatošanas laikā programmā Commerce Headquarters. |
| Pārrēķināt finanšu dimensijas, kļūdai | Ja šis parametrs ir iespējots, finanšu dimensijas var atkārtoti novērtēt sekojošai izrakstu grāmatošanai, ja izrakstu grāmatošana neizdodas. |
| Izmantot finanšu dimensijas no atgriešanas veikala | Ja šis parametrs ir iespējots, var izveidot saistītos atgriešanas pārdošanas pasūtījumus, kuros tiek lietotas veikala finanšu dimensijas, nevis oriģinālās darbības finanšu dimensijas. |
| Atsaistīt ienākumus | Kad šis parametrs ir iespējots, pārskats var izveidot negrāmatotās pārdošanas atgriešanu kā diskrētās atgriešanas. Pēc noklusējuma šis parametrs ir atspējots, un ieteicams to deaktivizēt. |
| Deaktivizēt noapaļošanas starpības grāmatošanu | Šis parametrs atspējo noapaļošanas starpības grāmatošanu starp darbības maksājumu un bruto summu maksājumu apstrādes laikā. |
| Automātiski nokārtot klientu noguldījumus | Ja šis parametrs ir iespējots, debitoru depozīti, kas tiek grāmatoti mazumtirdzniecības izraksta grāmatošanas laikā, tiek nosegti ar debitora atvērtajām transakcijām. |
| Iespējot un izmantot kases pārvaldības saskaņošanu no POS | Ja šis parametrs ir iespējots, sistēmā POS tiek veikta kases pārvaldības saskaņošana, un, lai izveidotu izrakstu rindas, vērtības tiek nodotas mazumtirdzniecības finanšu pārskata grāmatošanai. |
| Virsgrāmatas dokumenta detaļu līmenis | Šis parametrs nosaka detalizētības līmeni, kas virsgrāmatas dokumentā ir iekļauts atlasītajām darbībām, kas radušās no POS. Darbību tipos ietilpst ienākumi, izdevumi un atlaides. Atlaidēm šis parametrs tiek ņemts vērā tikai tad, ja konta numurs periodiskai atlaidei un konta numurs parastai atlaidei nav vienādi. Ja vien nav nepieciešama detalizēta informācija **,** kopsavilkums ir šo grāmatojumu ieteicamā vērtība. Ja ir definēta kopsavilkuma līmeņa grāmatošana, **transactionDiscountTrans.RecID** netiks aizpildīts. Commerce 10.0.27 versijas laidienā šis karodziņš tika pārdēvēts un pārvietots. Tā iepriekš tika nosaukts **kā Detalizācijas** līmenis un bija krājumu **atjaunināšanas** sadaļā. |
