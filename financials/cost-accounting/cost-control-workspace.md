---
title: Izmaksu kontroles darbvieta
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Izmaksu kontrole. Šī darbvieta ir vieta, kur vadītāji, kuri ir atbildīgi par izmaksu objekta vai izmaksu objektu kopas kontroli vienas vai vairāku dimensiju ietvaros, var centralizēti piekļūt pārskatiem."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5c5f06d1a518963738e446b5032261059d98bf13
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017

---

# <a name="cost-control-overview"></a>Pārskats par darbvietu Izmaksu kontrole 

[!include[banner](../includes/banner.md)]

Darbvieta **Izmaksu kontrole** ir vieta, kur vadītāji, kuri ir atbildīgi par izmaksu objekta vai izmaksu objektu kopas kontroli vienas vai vairāku dimensiju (piemēram, izmaksu centru un produktu grupu) ietvaros, var centralizēti piekļūt pārskatiem. Šajā darbvietā ietvertos pārskatus pilnībā pārvalda izmaksu grāmatveži, tāpēc var nodrošināt pārskatiem izmantoto datu un izkārtojumu saskaņošanu visā organizācijā.

## <a name="cost-control-workspace-configuration"></a>Izmaksu kontroles darbvietas konfigurācija

Izmaksu grāmatveži var definēt tik daudz pārskatu konfigurāciju, cik ir nepieciešams, lai iegūtu vajadzīgo datu salikumu vai izkārtojumu. Pārskata konfigurācija sastāv no sešām sadaļām, kura katra nodrošina vajadzīgā datu salikuma atlasi vai vajadzīgo izkārtojumu.

Lai konfigurētu izmaksu kontroles darbvietu, noklikšķiniet uz **Izmaksu uzskaite** \> **Iestatīšana** \> **Izmaksu kontroles darbvietas konfigurācija**.

### <a name="general"></a>Vispārējs

Kopsavilkuma cilnē **Vispārīgi** varat izveidot unikālu pārskata izkārtojumu. Pārskata nosaukums ir unikāls identifikators, ko lietotāji var atpazīt darbvietā **Izmaksu kontrole**. Varat arī norādīt to, vai pārskats ir paredzēts koplietošanai vai izmaksu grāmatvežu iekšējai lietošanai.

| Lauks       | apraksts |
|-------------|-------------|
| Vārds, uzvārds        | Ievadiet unikālu izkārtojuma nosaukumu. |
| apraksts | Ievadiet detalizētu aprakstu. |
| Publicēts   | Ja ir iestatīta šī lauka vērtība **Jā**, pārskatu darbvietā **Izmaksu kontrole** var skatīt jebkurš lietotājs, kuram ir piešķirta kāda no tālāk norādītajām lomām.<ul><li>Izmaksu uzskaites pārvaldnieks</li><li>Izmaksu grāmatvedis</li><li>Izmaksu grāmatvedības darbinieks</li><li>Izmaksu objekta kontrolieris</li></ul>Ja ir iestatīta šī lauka vērtība **Nē**, pārskatu darbvietā **Izmaksu kontrole** var skatīt tikai tie lietotāji, kuriem ir piešķirta kāda no tālāk norādītajām lomām.<ul><li>Izmaksu uzskaites pārvaldnieks</li><li>Izmaksu grāmatvedis</li><li>Izmaksu grāmatvedības darbinieks</li></ul> |

### <a name="data-filtering"></a>Datu filtrēšana

Kopsavilkuma cilnē **Datu filtrēšana** varat definēt pārskata pamata datus. Lietotājiem šajā pārskatā tiek rādītas vērtības, kas tiek iegūtas pēc avota datu apstrādes.

| Lauks                                                             | apraksts |
|-------------------------------------------------------------------|-------------|
| Izmaksu uzskaites virsgrāmata                                            | **Izmaksu uzskaites virsgrāmata**, kas tiek izmantota pārskata izveidei. Vērtība ir atkarīga no lauka **Izmaksu vadības ierīce** vērtības. |
| Izmaksu vadības ierīce                                                 | No atlasītās vērtības ir atkarīgs tas, kura izmaksu kontroles virsgrāmata un kuri izmaksu objekti tiks izmantoti pārskata izveidei. |
| Statistisko dimensiju hierarhija, Izmaksu elementu dimensiju hierarhija | Darbvietas **Izmaksu kontrole** konfigurācijas ieraksts var nodrošināt pārskatu par beznaudas vai naudas vērtībām, taču nevis vienā izkārtojumā. Atlasiet lauka **Izmaksu elementu dimensiju hierarhija**, lai veidotu pārskatu par naudas vērtībām. Atlasiet lauka **Statistisko dimensiju hierarhija**, lai veidotu pārskatu par beznaudas vērtībām. No atlasītā dimensiju hierarhijas ieraksta ir atkarīga pārskata veidošanas un apkopojuma līmeņu struktūra.<blockquote>[!NOTE]<br>Lai līdzās parādītu naudas un beznaudas vērtības, varat eksportēt datus uz programmu Microsoft Excel izmantošanai ar Microsoft Power BI satura pakotni.</blockquote> |
| Izmaksu objektu dimensiju hierarhija                                   | Atlasiet definētā pārskata mērķim piemērotas izmaksu objekta dimensijas hierarhiju. |
| Budžeta sākotnējā versija                                           | Atlasiet tās budžeta versijas ID, kas šī pārskata kontekstā ir sākotnējais budžets. |
| Budžeta pārskatītā versija                                            | Atlasiet tās budžeta versijas ID, kas šī pārskata kontekstā tiek izmantota kā sākotnējais budžets. |

### <a name="assign-calculation-records"></a>Piešķirt aprēķina ierakstus

Pieskaitāmo izmaksu aprēķina ietvaros tiek veiktas vairākas aprēķinu darbības ar avota datiem, piemēram, izmaksu izturēšanās klasifikācija, izmaksu sadale un izmaksu sadalījums. Gadījumā, ja tiek iegūti trūkstoši avota dati vai ir jāmaina nosacījumi, vienam finanšu periodam var veikt vairākus pieskaitāmo izmaksu aprēķinus. Katrs pieskaitāmo izmaksu aprēķins tiek saglabāts ar unikālu ID. Izmaksu grāmatvedis var atlasīt noteiktu pieskaitāmo izmaksu aprēķina ID. Pārskata lietotājiem, piemēram, vadītājiem, pieskaitāmo izmaksu aprēķina rezultāti tiek rādīti darbvietā **Izmaksu kontrole**.

| Lauks                  | apraksts |
|------------------------|-------------|
| Kalendārais finanšu periods | Atlasiet finanšu kalendāra periodu, kam ir jāpiešķir pieskaitāmo izmaksu aprēķina ID.<blockquote>[!NOTE]<br>Laukā norādītie finanšu periodi ir iegūtu no finanšu kalendāra, kas ir saistīts ar izmaksu uzskaites virsgrāmatu.</blockquote> |
| Faktiskā versija         | Atlasiet atbilstošo pieskaitāmo izmaksu aprēķina ID. |
| Budžeta versija         | Atlasiet atbilstošo pieskaitāmo izmaksu aprēķina ID. |
| Pārskatītā budžeta versija | Atlasiet atbilstošo pieskaitāmo izmaksu aprēķina ID. |

### <a name="fiscal-periods-per-column"></a>Finanšu periodi pēc kolonnas

Kopsavilkuma cilnē **Finanšu periodi pēc kolonnas** izmaksu grāmatvedis var izvēlēties finanšu periodu, kas ir jārāda pārskata izkārtojumā.

Atlasītajās kolonnās esošās vērtības tiek reizinātas ar kopsavilkuma cilnē **Finanšu periodi pēc kolonnas** atlasītajām vērtībām.

| Lauks                | apraksts |
|----------------------|-------------|
| Pašreizējais periods       | Tiek parādīta pašreizējā finanšu perioda bilance.<blockquote>[!NOTE]<br>Pēc noklusējuma pašreizējais periods tiek noteikts pēc sesijas datuma. Darbvietā **Izmaksu kontrole** var atlasīt noteiktu finanšu periodu. Šādā gadījumā pašreizējais periods tiek noteikts pēc atlasītās vērtības.</blockquote> |
| Iepriekšējais periods      | Tiek parādīta iepriekšējā finanšu perioda bilance. Tiek izmantota šāda formula:<br>Pašreizējais finanšu periods – 1<blockquote>[!NOTE]<br>Pēc noklusējuma iepriekšējais periods tiek noteikts pēc sesijas datuma. Darbvietā **Izmaksu kontrole** kā pašreizējo periodu var atlasīt noteiktu finanšu periodu. Šādā gadījumā tiek atbilstoši pārrēķināta lauka **Iepriekšējais periods** vērtība.</blockquote> |
| No gada sākuma         | Tiek rādīta vērtība no gada sākuma. Tiek izmantota šāda formula:<br>YearToDate (pašreizējais finanšu periods)<blockquote>[!NOTE]<br>Pēc noklusējuma pašreizējais periods tiek noteikts pēc sesijas datuma. Darbvietā **Izmaksu kontrole** var atlasīt noteiktu finanšu periodu. Šādā gadījumā pašreizējais periods tiek noteikts pēc atlasītās vērtības un tiek atbilstoši atjaunināta lauka **No gada sākuma** vērtība.</blockquote> |
| Vidējais no gada sākuma | Tiek rādīta vidējā vērtība no gada sākuma. Tiek izmantota šāda formula:<br>(YearToDate [pašreizējais finanšu periods]) ÷ (Count [pašreizējais finanšu periods])<p><strong>Piemērs</strong></p><ul><li>**Statisko dimensiju elements:** Pilnas slodzes darbinieki</li><li>**Pašreizējais datums:** 03.21.2017.</li><li>**Periods:** 1. finanšu periods, 2. finanšu periods, 3. finanšu periods</li><li>**Lielums:** 10, 10, 12</li></ul>Šajā gadījumā **Vidējais no gada sākuma** = (10 + 10 + 12) ÷ 3 = 10,67<p>Lauka **Vidējais no gada sākuma** vērtību var aprēķināt izmaksu elementu dimensiju elementiem un statistisko dimensiju elementiem.</p><blockquote>[!NOTE]<br>Pēc noklusējuma pašreizējais periods tiek noteikts pēc sesijas datuma. Darbvietā **Izmaksu kontrole** var atlasīt noteiktu finanšu periodu. Šādā gadījumā pašreizējais periods tiek noteikts pēc atlasītās vērtības un tiek atbilstoši atjaunināta lauku **No gada sākuma** un **Vidējais no gada sākuma** vērtības.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Kolonnas, ko rādīt izmaksām

Kopsavilkuma cilnē **Kolonnas, ko rādīt izmaksām** izmaksu grāmatvedis var izvēlēties, kuras kolonnas ir jāietver pārskata izkārtojumā. Ir pieejamas trīs kategorijas: Fiksētas izmaksas, Mainīgas izmaksas un Neklasificētas izmaksas.

| Lauks                 | apraksts |
|-----------------------|-------------|
| Fiksētas izmaksas            | Šī veida kolonnā tiek rādītas fiksētās izmaksas, pamatojoties uz atlasīto pieskaitāmo izmaksu aprēķina ID.<blockquote>[!NOTE]<br>Ja tiek atlasīts finanšu perioda pieskaitāmo izmaksu aprēķina ID, šī veida kolonnā tiek rādīta tikai bilance.</blockquote> |
| Mainīgas izmaksas         | Šī veida kolonnā tiek rādītas mainīgās izmaksas, pamatojoties uz atlasīto pieskaitāmo izmaksu aprēķina ID.<blockquote>[!NOTE]<br>Ja tiek atlasīts finanšu perioda pieskaitāmo izmaksu aprēķina ID, šī veida kolonnā tiek rādīta tikai bilance.</blockquote> |
| Fiksētas un mainīgas izmaksas | Šī veida kolonnā tiek rādītas fiksētās un mainīgās izmaksas, pamatojoties uz atlasīto pieskaitāmo izmaksu aprēķina ID.<blockquote>[!NOTE]<br>Ja tiek atlasīts finanšu perioda pieskaitāmo izmaksu aprēķina ID, šī veida kolonnā tiek rādīta tikai bilance.</blockquote> |
| Kopējās izmaksas            | Šī veida kolonnā tiek rādītas kopējās izmaksas (neklasificētās izmaksas, fiksētās izmaksas un mainīgās izmaksas).<blockquote>[!NOTE]<br>Šī veida kolonnā vienmēr tiek rādīta bilance.</blockquote> |
| Neklasificētas izmaksas     | Šī veida kolonnā tiek rādītas neklasificētās izmaksas.<blockquote>[!NOTE]<br>Šo kolonnu var izmantot, lai pārbaudītu, vai pieskaitāmo izmaksu aprēķina ietvaros ir pareizi klasificētas visas izmaksas un vai ir jāpielāgo izmaksu izturēšanās nosacījumi.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Kolonnas, ko rādīt budžetā paredzētajām izmaksām

Kopsavilkuma cilnē **Kolonnas, ko rādīt budžetā paredzētajām izmaksām** izmaksu grāmatvedis var izvēlēties, kuras kolonnas ir jārāda atlasīto budžeta versiju pārskatos. Sākotnējam un pārskatītajam budžetam var veikt atsevišķu atlasi.

> [!NOTE]
> Tālāk norādīto lauku funkcionalitāte ir vienāda gan sākotnējā, gan pārskatītā budžeta gadījumā, tāpēc šie lauki ir paskaidroti tikai vienreiz.

| Lauks                     | apraksts |
|---------------------------|-------------|
| Budžets                    | Tiek rādītas budžeta bilances atbilstoši atlasītajām kolonnām.<blockquote>[!NOTE]<br>Bilances tiek aprēķinātas, pamatojoties uz budžeta versijām, kas ir atlasītas kopsavilkuma cilnē **Datu filtrēšana**.</blockquote> |
| Budžeta novirze           | Tiek aprēķināta un parādīta budžeta un faktiskās bilances starpība. Tiek izmantota šāda formula:<br>budžeta bilance – faktiskās bilance |
| Budžeta novirze, %      | Tiek aprēķināta un parādīta budžeta un faktiskās bilances starpība procentos. Tiek izmantota šāda formula:<br>(budžeta bilance – faktiskā bilance) ÷ budžeta bilance |
| Novirzes perioda slieksnis | Iestatiet naudas summas novirzes slieksni pašreizējam periodam. Ja slieksnis tiek pārsniegts, attiecīgā rinda darbvietā **Izmaksu kontrole** tiek iezīmēta sarkanā krāsā.<blockquote>[!NOTE]<br>Šis lauks attiecas tikai uz izmaksu elementiem, kas ir saistīti ar izdevumiem.</blockquote> |
| Novirzes gada slieksnis   | Iestatiet naudas summas novirzes slieksni attiecīgajam gadam. Ja slieksnis tiek pārsniegts, attiecīgā rinda darbvietā **Izmaksu kontrole** tiek iezīmēta sarkanā krāsā. |
| Novirzes sliekšņa % vērtība      | Iestatiet novirzes slieksni procentos. Ja slieksnis tiek pārsniegts, attiecīgā rinda darbvietā **Izmaksu kontrole** tiek iezīmēta sarkanā krāsā.<blockquote>[!NOTE]<br>Tas pats slieksnis procentos attiecas uz pašreizējo periodu un gadu.</blockquote> |

## <a name="cost-control-workspace"></a>Izmaksu kontroles darbvieta

Darbvieta **Izmaksu kontrole** ir izstrādāta kā tīmekļa portāls. Tāpēc visiem vadītājiem, kuri ir atbildīgi par izmaksu objektu, var piešķirt piekļuves tiesības, kā tas ir aprakstīts tēmā [Piekļuves tiesību definēšana izmaksu objektu kontrolieriem](access-rights-cost-object-controller.md).

Lietotājiem, piemēram, vadītājiem, pieejamo pārskatu saraksts ir atkarīgs no opcijas **Publicēts** iestatījuma lapā **Izmaksu kontroles darbvietas konfigurācijas**.

![Pārskats, kas lietotājiem tiek rādīts darbvietā Izmaksu kontrole](./media/report-cost-control.png)

Vadītājs var atlasīt parādāmo finanšu kalendāra periodu. Noklusējuma pašreizējais periods tiek noteikts, izmantojot sesijas datumu.

Vērtības finanšu kalendāra periodā ir atkarīgas no pārskata nosaukuma un finanšu kalendāra, kas ir atlasīts izmaksu uzskaites virsgrāmatai, kura ir saistīta ar pārskata nosaukumu lapā **Izmaksu kontroles darbvietas konfigurācijas**.

Izmaksu objektu dimensiju hierarhijā lietotāji var atlasīt apkopojuma līmeni, kas ir jāizmanto bilanču rādīšanai. Iespējojot piekļuves līmeņa drošību, varat kontrolēt atļaujas, ļaujot lietotājiem atlasīt tikai tos hierarhijas līmeņus, kuriem viņi ir saņēmuši piekļuves tiesības. Tāpēc lietotājiem tiek rādītas tikai tās apkopotās bilances, kurām viņiem ir piešķirtas piekļuves tiesības.

### <a name="add-or-remove-columns"></a>Pievienot vai noņemt kolonnas

Lietotāji var pielāgot pārskatā ietvertās kolonnas atbilstoši savām prasībām.

### <a name="view-details"></a>Skatiet papildinformāciju

Lietotāji var skatīt detalizētu informāciju par darbvietā rādītajām bilancēm. Ja lietotājs atlasa izmaksu elementu dimensiju hierarhijas mezglu un pēc tam noklikšķina uz **Skatīt papildinformāciju**, tiek parādīts dialoglodziņš **Detalizēta informācija par izmaksu elementu** ar detalizētu informāciju par attiecīgo mezglu.

Režģī tiek rādīts katrs ar izmaksu elementu dimensiju hierarhijas mezglu saistītais izmaksu elements un tā vērtības. Režģī redzamās kolonnas atbilst darbvietas iestatījumiem.

Divās diagrammās tiek rādīts kopsavilkums par faktiskās un budžeta bilances starpību un budžeta novirzi pēc perioda.

![Diagrammas, kurās ir redzams kopsavilkums par faktiskās un budžeta bilances starpību un budžeta novirzi pēc perioda](./media/cost-element-details-operations.png)

Lietotāji var noklikšķināt uz **Izmaksu ieraksti**, lai skatītu detalizētu informāciju par ierakstu, ja tas ir nepieciešams.

![Izmaksu ieraksti](./media/cost-entries.png)

Piemēram, īre ir izdevums, kas tiek sadalīts pa izmaksu centriem. Lietotājs, kurš vēlas iegūt informāciju par īres izdevumiem, kas attiecas uz viņa izmaksu centru, var skatīt detalizētu informāciju par īres aprēķina veidu.

Ja lietotājs lapā **Izmaksu ieraksti** noklikšķina uz **Sadalījuma pamats**, tiek parādīts dialoglodziņš. Pēc tam lietotājs var piešķirt sadalījuma pamatu kārtulai un skatīt atbilstošos statistikas mērus, kas ir reģistrēti par attiecīgo periodu.

Tālāk esošajā piemērā sadalījuma pamata tips ir **Formulas sadalījuma pamats** un tiek izmantota norādītā formula. Ir norādīti faktori, ar kuriem tiek definēta formula. Turklāt režģī ir redzams aprēķins, kas tiek veikts katram izmaksu objektam.

![Aprēķini katram izmaksu objektam](./media/cost-entries-allocation-base.png)

Skatiet arī 

[Piekļuves tiesību definēšana izmaksu objektu kontrolieriem](access-rights-cost-object-controller.md)



