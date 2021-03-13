---
title: Finanšu ieskati
description: Darbvietā Finanšu ieskati tiek izmantots pakalpojums Microsoft Power BI, lai apkopotu finanšu izpildes pamatrādītājus (KPI), diagrammas un finanšu pārskatus.
author: kweekley
manager: AnnBe
ms.date: 05/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 9aaf24147900c890a14c60ab969da7124c538911
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115732"
---
# <a name="financial-insights"></a>Finanšu ieskati

[!include [banner](../includes/banner.md)]

Darbvietā **Finanšu ieskati** tiek izmantots pakalpojums Microsoft Power BI, lai apkopotu finanšu izpildes pamatrādītājus (KPI), diagrammas un finanšu pārskatus. Power BI ir iegults programmā. Darbvieta **Finanšu ieskati** ir paredzēta analītisku pārskatu veidošanai. Personas visā organizācijā var skatīt, pētīt, izprast un rīkoties. 

**Finanšu ieskati** apvieno virsgrāmatas un apakšgrāmatu datus, lai nodrošinātu visaptverošāku informāciju par organizācijas finanšu veselību.

> [!NOTE]
> Šajā dokumentā tiek izmantota tālāk norādītā Power BI terminoloģija.
> 
> - **Pārskats** — viens .pbix fails, kurā visās cilnēs ir saglabāti visi vizuālie dati.
> - **Lapa** — cilne vienā .pbix failā. Katrā lapā var būt viens vizuālo datu vienums vai vairāki.
> - **Vizuālie dati** — viens datu avots, piemēram, kartīte, KPI, diagramma, grafiks, matrica vai finanšu pārskats. Lapā, kurā kā vizuālie dati ir finanšu pārskats, nevar būt citu vizuālo datu to datu lieluma dēļ, par ko tiek sniegts pārskats.

Pašlaik darbvieta **Finanšu ieskati** tiek izmantota, lai skatītu aktīvās juridiskās personas vai visu juridisko personu datus. Turpmākajos laidienos darbvieta tiks attīstīta par vietu, kurā varēsit izmantot pakalpojumu Power BI vizuālo datu rediģēšanai un izveidei.

Darbvietā **CFO apskats** parādīti tie paši vizuālie dati, kas redzami darbvietā **Finanšu ieskati**, taču tās galvenais nolūks ir ļaut jums skatīt un filtrēt datus esošos pārskatos. Turpmākajos laidienos darbvietai **Finanšu ieskati** varēsit pievienot jaunus vizuālos datus. Jaunie vizuālie dati var arī būt pieejami darbvietās, kas paredzētas citām lomām, piemēram, projektu vadītāja vai kreditoriem maksājamo parādu vadītāja lomai. Darbvietā **CFO apskats** joprojām tiek rādīti visu juridisko personu dati neatkarīgi no juridiskajām personām, kam lomai ir piekļuve.

## <a name="dynamics-365-finance-setup"></a>Dynamics 365 Finance iestatīšana
**Virsgrāmata**

Galvenā konta tips un galvenā konta kategorijas tiek izmantotas, lai aizpildītu atbilstošos noklusējuma galvenos kontus tipa **Bilance** finanšu pārskatos un dažādajos tipa **Peļņas vai zaudējumu aprēķins** finanšu pārskatos darbvietā **Finanšu ieskati**.

Lapā **Galvenie konti** jums ir jādefinē galvenais konts tā, lai tam tiktu piešķirts viens no tālāk norādītajiem tipiem.

- Ieņēmumi
- Expense
- Līdzekļi
- Pasīvs
- Kapitāls

Galvenajiem kontiem nedrīkst piešķirt nevienu citu galvenā konta tipu, piemēram, **Bilance** vai **Peļņa un zaudējumi**. Pārskati nevar noteikt galvenā konta tipu, kad ir piešķirti citi galvenā konta tipi, jo tie nav pietiekami fragmentāri. Galvenā konta tips ir jānosaka, lai pasīvus un ieņēmumus finanšu pārskatos varētu parādīt kā pozitīvas summas.

Lai galvenais konts tiktu parādīts finanšu pārskatos un būtu iekļauts dažādos citos vizuālajos datos, piemēram, KPI, katram kontam ir jābūt piešķirtai galvenā konta kategorijai. Galvenā konta kategorijas ir uzlabotas, lai tās ietvertu rādīšanas secību. Rādīšanas secība darbvietā **Finanšu ieskati** tiek izmantota īpaši finanšu pārskatiem. Pēc tam, kad rediģējat vai pievienojat jaunu galvenā konta kategoriju, varat mainīt opcijas **Rādīšanas secība** vērtību, lai noteiktu secību, kādā galvenā konta kategorijas jārāda finanšu pārskatā. Ja rādīšanas secība jāmaina daudzām galvenā konta kategorijām, varat izmantot līdzekli Atvērt programmā Excel, lai ātri rediģētu un publicētu izmaiņas programmā.

## <a name="entity-store"></a>Elementu krātuve
Darbvietas **Finanšu ieskati** dati tiek atgādāti no elementu krātuves (**Sistēmas administrēšana** \> **Iestatīšana** \> **Elementu krātuve**). Ja atverat darbvietu **CFO apskats** vai **Finanšu ieskati** un vizuālajos datos ir redzams tālāk norādītais brīdinājuma ziņojums, jums ir jāatjaunina elementi.

![Brīdinājums!](./media/Cantdisplay.png)

Lai skatītu datus darbvietās **Finanšu ieskati** un **CFO apskats**, jums ir jāatjaunina tālāk norādītie elementi.

- BudgetActivityMeasure
- Finanšu pārskatu darbību dati — 3. versija 
- CustCollectionsBIMeasurements
- LedgerActivityMeasure
- LedgerCovLiquidityMeasurement
- Pirkšanas kubs
- Pārdošanas kubs

Iepriekšējā laidienā elementi LedgerActivityMeasure un VendPaymentBIMeasure tika izmantoti datiem darbvietā **CFO apskats**. Tomēr tos vairs neizmanto pašreizējā laidienā.

Varat definēt ciklisku pakešuzdevumu, lai regulāri atjauninātu elementu datus. Tā kā katrs elements atjaunināšanas laikā tiek pilnībā izveidots no jauna, uzmanīgi atlasiet elementu atjauninājumu laiku un biežumu. Primārais elements, kas tiek izmantots finanšu pārskatiem, ir elements FinancialReportingTransactionData. Tāpēc, iespējams, izlemsit šo elementu atjaunināt biežāk.

## <a name="security"></a>Drošība
Pašlaik iegultajos Power BI pārskatos ietvertos datus nevar ierobežot, nodrošinot datus tikai par tām juridiskajām personām, kurām lietotājs var piekļūt. Tāpēc iegulto Power BI pārskatu kontrolei tiek izmantoti pienākumi, kas tiek konfigurēti drošības iestatījumos. Pienākumi, kas ir definēti, ļauj piekļūt visu juridisko personu datiem vai tikai aktīvā uzņēmuma datiem. Tālāk esošajā tabulā ir parādīti esošie pienākumi un tiem piešķirtās lomas. Pienākumus var noņemt vai piešķirt dažādām lomām atbilstoši organizācijas prasībām.

| Nodoklis                                    | Lomas | Apraksts |
|-----------------------------------------|-------|------------|
| Skatīt CFO apskata darbvietu             | Finanšu direktors | Šis pienākums nodrošina piekļuvi darbvietai CFO apskats. Pēc noklusējuma aktīvais uzņēmums tiek izmantots kā filtrs. Tomēr varat pievienot visas juridiskās personas neatkarīgi no tā, vai lietotājam ir piekļuve citām juridiskajām personām. |
| Skatīt pašreizējā uzņēmuma finanšu ieskatus | <ul><li>Grāmatvedis</li><li>Uzskaites vadītājs</li><li>Uzskaites supervizors</li><li>Auditors</li><li>Budžeta pārvaldnieks</li><li>Iestādes vadītājs</li><li>Finanšu direktors</li><li>Finanšu kontrolieris</li></ul> | Šis pienākums nodrošina piekļuvi darbvietai Finanšu ieskati. Pēc noklusējuma aktīvais uzņēmums tiek izmantots kā filtrs. Nevar pievienot citas juridiskās personas. |
| Skatīt starpuzņēmumu finanšu ieskatus   | Programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 šis pienākums nav piešķirts lomai. Nākamajā laidienā šis pienākums tiks piešķirts lomai Finanšu direktors. | Šis pienākums nodrošina piekļuvi darbvietas CFO apskats izvēlnes vienumam. Pēc noklusējuma aktīvais uzņēmums tiek izmantots kā filtrs. Tomēr varat pievienot visas juridiskās personas neatkarīgi no tā, vai lietotājam ir piekļuve citām juridiskajām personām. |


## <a name="financial-reporting-vs-financial-insights"></a>Darbvietu “Finanšu pārskati” un “Finanšu ieskati” salīdzinājums
Lai gan darbvietā **Finanšu ieskati** ir ietverti finanšu pārskati, tā neaizstāj finanšu pārskatus programmā. Noklusējuma finanšu pārskati darbvietā **Finanšu ieskati** ir ierobežoti, un tajā nav ietverti visu veidu finanšu pārskati. Finanšu pārskati joprojām ir galvenais rīks normatīvu finanšu pārskatu noformēšanai, izveidei un ģenerēšanai.

Tālāk esošajā salīdzinājuma diagrammā tiks parādītas atšķirības starp šīm divām opcijām.


|                                                          | Finanšu pārskatu veidošana                                               | Finanšu ieskati |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Rediģēt noklusējuma pārskatus**                                 | Jā                                                               | Nav |
| **Izveidot jaunus pārskatus**                                   | Jā                                                               | Nav |
| **Drukāt pārskatus**                                        | Jā                                                               | Nav |
| **Eksportēt programmā Excel**                                      | Jā                                                               | Ierobežoti Eksportē neapstrādātos datus uz programmu Excel, nav formatēts pārskats |
| **Atbalsts pārskatu veidošanas hierarhijai/organizācijas hierarhijai**   | Jā                                                               | Nav |
| **Pārskats par apakšgrāmatu datiem**                             | Jā Ierobežoti Tikai kreditoram un debitoram                              | Jā Kreditors, debitors, kreditoru/debitoru grupas, kreditoru/debitoru adreses u. c. |
| **Pārskata valūta**                                   | Jā Uzskaites valūta un pārvēršana pārskata valūtā       | Nē Tikai uzskaites valūta |
| **Drošība**                                             | Jā Atbilstoši Finanšu pārskatu veidošanas koka drošībai | Ierobežoti Skatiet pārskatus par visiem uzņēmumiem (neatkarīgi no Finance and Operations drošības) vai tikai aktīvo uzņēmumu |
| **Atbalsts atšķirīgiem kontu plāniem un finanšu gadiem** | Jā                                                               | Nav |
| **Pārskats par ārējiem datiem**                              | Nav                                                                | Nav |
| **Atbalsta konsolidācijas**                               | Jā                                                               | Ierobežoti Var izveidot pārskatu par vairākiem uzņēmumiem, taču izmanto tikai uzskaites valūtu |

Papildus lietotāja interfeisam oriģinālajā darbvietā **CFO apskats**, tagad ir pieejami jauni KPI, diagrammas un finanšu pārskati. Ir pieejami tālāk norādītie finanšu pārskati.

- Apgrozījuma bilance
- Bilance
- Peļņas vai zaudējumu aprēķins pēc reģiona
- Peļņas vai zaudējumu aprēķins — faktiskie pret budžeta
- Peļņas vai zaudējumu aprēķins ar novirzēm
- 12 mēnešu tendenču peļņas vai zaudējumu aprēķins
- Izdevumu trīs gadu tendence
- Izdevumi pēc kreditora
- Pārdošana pēc debitora

## <a name="edit-visuals"></a>Vizuālo datu rediģēšana
Sākotnējā darbvietas **Finanšu ieskati** laidienā nevar rediģēt nekādus vizuālos datus. Turpmākajos laidienos lietotāji, kuriem būs atbilstošas drošības atļaujas, varēs izveidot jaunus vizuālos datus, kopēt esošos vizuālos datus un rediģēt vizuālos datus. Lai gan .pbix faili, kas satur pārskatus, ir pieejami kā resursi, nav ieteicams rediģēt noklusējuma pārskatus. Tiks veiktas papildu izmaiņas datu modelī, noklusējuma pārskatos un pielāgotajos finanšu pārskata vizuālajos datos, kas tiek izmantoti finanšu pārskatu izveidei. Tāpēc, lai varētu izmantot nākamajā laidienā ietvertos jaunos līdzekļus un datu modeļa izmaiņas, būs jāatkārto visas noklusējuma pārskatu izmaiņas, kas būs veiktas, izmantojot programmu Microsoft Power BI Desktop.

## <a name="filtering"></a>Filtrēšana
Lietotāji var filtrēt pārskatu, izmantojot kreisajā pusē esošo rūti **Filtrs**. Šī ir tā pati rūts, kas ir pieejama programmā Power BI Desktop. Ir dažādu līmeņu filtrēšana, un dažu veidu filtrēšana var nebūt pieejama atkarībā no tā, ko esat atlasījis lapā (cilnē), vai no tā, vai izmantojat detalizētas apskates iespējas.

- **Pārskata līmeņa filtri** — šie filtri tiek lietoti visiem vizuālajiem datiem visās lapās (cilnēs).
- **Lapas līmeņa filtri** — šie filtri tiek lietoti visiem vizuālajiem datiem aktīvajā cilnē. Šie filtri tiek lietoti papildus pārskata līmeņa filtriem.
- **Vizuālo datu līmeņa filtri** — šie filtri tiek lietoti tikai atlasītajiem vizuālajiem datiem. Šie filtri tiek lietoti papildus lapas līmeņa filtriem.
- **Detalizētās rādīšanas filtrs** — šis filtrs filtrē no “avota” vizuālajiem datiem, kas tiek lietoti pašreizējiem vizuālajiem datiem, kad veicat detalizētu rādīšanu no avota vizuālajiem datiem uz pašreizējiem vizuālajiem datiem.

![Filtrēšanas opcijas](./media/filter.png)

Lai noņemtu konkrētu filtra vērtību, atlasiet tai blakus esošo dzēšgumijas simbolu. Nenoņemiet filtru, atlasot vienumu X. Ja atlasīsit X, filtrētais lauks tiks noņemts kā filtra opcija. Ja nejauši noņemat lauku no filtra, aizveriet darbvietu un pēc tam to atkal atveriet. No jauna tiks lietoti noklusējuma filtra iestatījumi.

Kad pirmoreiz atverat darbvietas, aktīvā juridiskā persona pēc noklusējuma tiek izmantota kā pārskata līmeņa filtrs. Atkarībā no savām drošības atļaujām lietotāji, iespējams, varēs pievienot citas juridiskās personas vai mainīt filtrā atlasīto noklusējuma juridisko personu.

Ir nepieciešams filtrs **Finanšu kalendārs**, lai vizuālajiem datiem tiktu izmantots pareizais kalendārs. Pēc noklusējuma pārskata līmeņa filtrs ir iestatīts uz aktīvās juridiskās personas finanšu kalendāru. Ja filtru mainīsit uz finanšu kalendāru, kam ir atšķirīgs sākuma vai beigu datums, sākuma bilances netiks iekļautas. Tādēļ tipa **Bilance** finanšu pārskatos netiks rādītas pareizās bilances. Ja filtrā atlasīsit papildu finanšu kalendāru, tiks iegūta papildu kolonnu kopa. Katrā papildu kolonnu kopā parādītas cita finanšu kalendāra summas.

Ir nepieciešams arī filtrs **Grāmatošanas līmenis**. Pēc noklusējuma filtrs tiek iestatīts uz Pašreizējais. Varat filtrā atlasīt papildu grāmatošanas līmeņus, lai parādītu apkopotās summas.

Filtri ir pieejami arī laukiem **Datums** un **Finanšu gads**. Parasti šie filtri tiek lietoti lapas līmenī. Pēc noklusējuma filtrā **Datums** izmantots relāciju datums, ko varat mainīt. Varat arī noņemt relāciju datuma filtru un izmantot filtru **Finanšu gads**.

## <a name="currency"></a>Valūta

Visos vizuālajos datos, kas sniedz pārskatu par virsgrāmatas datiem, summas parādītas uzskaites valūtā. Tāpēc, filtrējot juridisko personu, jāuzmanās, lai tiktu iekļautas tikai juridiskās personas ar vienādu uzskaites valūtu. Pretējā gadījumā dati tiks apkopoti dažādās valūtās.

Visos vizuālajos datos, kas sniedz pārskatu par apakšgrāmatu datiem, piemēram, vizuālajos datos **Naudas plūsmas prognoze** un **Pirmie 10**, summas parādītas sistēmas valūtā. Sistēmas valūta un sistēmas maiņas kursa tips ir definēts lapā **Sistēmas parametri**.

Vizuālajos datos **Bilance pēc bankas konta** summas norādītas bankas kontu valūtās.

## <a name="dimensions"></a>Dimensijas

Noklusējuma finanšu pārskatos nav ietvertas nekādas finanšu dimensijas, un tajos fokuss ir tikai uz galveno kontu. Finanšu dimensiju atbalsts būs pieejams turpmākajos laidienos, kad pārskati kļūs rediģējami. Organizācijas tad varēs filtrēt finanšu dimensiju vērtības.

Dažos finanšu pārskatos ir dimensijas, kuru pamatā ir apakšgrāmatu transakcijas. Jauno finanšu pārskatu mērķis ir iespējot filtrēšanu dimensijām, kas nav iestatītas kā finanšu dimensijas. Piemēram, izmantojot noklusējuma pārskatu Izdevumi pēc kreditora, varat rezultātus paplašināt tālāk par galveno kontu, lai redzētu bilances pa kreditoriem. Kreditors nav iestatīts kā finanšu dimensija. Sistēma atgriežas sākotnējā apakšgrāmatas transakcijā, lai atrastu kreditoru.

Noklusējuma pārskatos tiek izmantotas tālāk norādītās dimensijas. Neviena no šīm dimensijām nav finanšu dimensija.

- Kreditors
- Kreditoru grupa
- Debitors
- Debitoru grupa
- Valsts/reģions
- Administratīvais apgabals/novads
- Pilsēta

> [!IMPORTANT] 
> Ja vairāku kreditoru vai debitoru transakcijas apkoposit vienā dokumentā, izmantojot finanšu žurnālus, dati būs nepareizi. Pārskati nevar noteikt, kurš kreditors vai debitors ir saistīts ar noteiktu virsgrāmatas kontu žurnāla ierakstā, jo šī informācija netiek saglabāta visur. Tāpēc nav ieteicams vairākus kreditorus, debitorus, pamatlīdzekļus vai projektus ievadīt vienā dokumentā.

## <a name="drill-on-data"></a>Detalizēta datu rādīšana

Izmantojot Power BI, ir pieejami dažādi detalizētās rādīšanas līmeņi. Katram līmenim ir cits nosaukums un funkcionalitāte. Var arī detalizēti rādīt rindas un kolonnas. Šajā sadaļā tiek aplūkotas dažādas opcijas, kā piemēru izmantojot finanšu pārskatu **Apgrozījuma bilance** un parādot, kā detalizēti rādīt rindas. Tā pati funkcionalitāte ir arī kolonnām. Ir tikai jānomaina iestatījums **Rādīt detalizēti**.

Tālāk esošajā attēlā pārskats **Apgrozījuma bilance** ir sakļauts līdz augstākajam rindu hierarhijas līmenim, galvenā konta tipam.

![Apgrozījuma bilances izraksts](./media/trial-balance.png)

Lai skatītu nākamo hierarhijas līmeni, galvenā konta kategorijas, lauku **Rādīt detalizēti** iestatiet uz **Rindas** un pēc tam atlasiet pogu **Izvērst** (trešā poga pēc lauka Rādīt detalizēti). Tādējādi tiek izvērstas visas galvenā konta kategorijas. Pašlaik pakalpojumā Power BI nevar izvērst tikai vienu rindu vai kolonnu un vienlaikus joprojām skatīt visas pārējās rindas vai kolonnas.

![Apgrozījuma bilances detalizēta izpēte rindās](./media/trial-balance2.png)

Lai izvērstu galvenos kontus visām rindām, vēlreiz izmantojiet pogu **Izvērst**. Taču, lai detalizēti rādītu galvenos kontus tikai vienai rindai, vispirms atlasiet pogu **Rādīt detalizēti** (viena lejupvērstā bultiņa loga labajā pusē) un pēc tam atlasiet detalizēti rādāmo rindu. Tālāk esošajā attēlā redzams rezultāts, kas tiek iegūts, kad pēc pogas **Rādīt detalizēti** atlasīšanas tiek atlasīta rinda **Pārdošana**.

![Apgrozījuma bilances izvēršanas poga](./media/trial-balance3.png)

Kad esat detalizēti parādījis vienu rindu un vēlaties atgriezties pilnajā apgrozījuma bilancē, ir jānoklikšķina vairākas reizes. Izmantojot pogu **Rādīt vispārīgi** (pirmā poga pēc lauka **Rādīt detalizēti**) vispārīgi rāda tikai kategorijas **Pārdošana** kontekstā, kā parādīts tālāk esošajā attēlā.

![Apgrozījuma bilances detalizētas izpētes poga](./media/trial-balance4.png)

Varat turpināt izmantot pogu **Rādīt vispārīgi**, lai atgrieztos augstākajā rindu kopsavilkuma līmenī.

Pakalpojumā Power BI ir pieejama arī poga, kas sniedz iespēju pāriet uz nākamo hierarhijas līmeni (otrā poga pēc lauka **Rādīt detalizēti**). Izmantojot šo pogu, rezultāts atšķiras no tā, kas tiek iegūts ar pogu **Izvērst** (trešā poga pēc lauka **Rādīt detalizēti**), kuru izmanto hierarhijas izvēršanai. Izvēršot hierarhiju, tā tiek saglabāta pārskatā. Piemēram, kā parādīts iepriekš, ja izvēršat galvenā konta tipu, pārskatā joprojām ir redzams galvenā konta tips. Taču, kad pārejat uz nākamo hierarhijas līmeni, pārskatā vairs netiek rādīta vecākhierarhija, kā parādīts tālāk esošajā attēlā.

![Apgrozījuma bilances detalizētas izpētes atpakaļgaitas poga](./media/trial-balance5.png)

Lai skatītu detalizētu informāciju par transakcijām apkopotajās bilancēs, varat atlasīt dažas summas, lai veiktu detalizēto rādīšanu programmā Finance and Operations.

Veicot detalizēto rādīšanu no finanšu pārskatiem, jūs tiekat novirzīts uz uzskaites avota pārlūku (ASE — Accounting Source Explorer), nevis dokumentu transakcijām. ASE nerāda tikai uzskaites ierakstus virsgrāmatā. Šis pārlūks parāda detalizētu informāciju par apakšgrāmatas transakciju. Tādējādi jūs iegūstat daudz detalizētāku informāciju par sākotnējo transakciju un varat izmantot to analīzei. Piemēram, varat redzēt, kurš bija kreditors vai debitors, ko debitors iegādājās vai kreditors pārdeva un pat to, kāds projekts bija transakcijā.

Uz pārlūku ASE tiek pārsūtīti tālāk norādītie filtri no finanšu pārskatiem, lai pārlūkā ASE tiktu parādītas apkopotas transakcijas.

Tālāk norādīti obligātie lauki filtrēšanai.

- Juridiska persona
- Finanšu kalendārs
- Gads
- Galvenā konta ID

Tālāk norādīti izvēles lauki filtrēšanai.

- Ceturksnis
- mēnesis;
- Periods

Pietiekami neizvēršot rindu, detalizētā rādīšana nedarbojas. Piemēram, ja izvēršat tikai līdz galvenā konta kategorijai, pārlūkā ASE nevarat rādīt detalizēti bilanci, jo pārlūkā ASE galvenais konts ir obligāts lauks filtrēšanai.

Ja pārāk daudz izvēršat rindu, uz pārlūku ASE netiek nosūtīti finanšu pārskatu papildu filtri. Tādēļ skaitļos var rasties atšķirības. Piemēram, ja finanšu pārskata Peļņas vai zaudējumu aprēķins pēc reģiona rindas izvēršat līdz valstij vai reģionam, pārlūkā ASE valsts vai reģions netiek iekļauts kā filtrs.

> [!NOTE]
> Finanšu pārskata rindas vai kolonnas varat parādīt detalizētāk, nekā ASE pašlaik atbalsta filtrēšanai. Tāpēc dažās situācijās detalizētu ASE transakciju summa neatbildīs bilancei, kam veicat detalizēto rādīšanu. Šo funkcionalitāti turpinās uzlabot.

## <a name="hierarchies"></a>Hierarhijas

Noklusējuma finanšu pārskatos datu detalizētai rādīšanai un izvēršanai tiek izmantotas divas hierarhijas. Viena hierarhija ir rindām, bet otra — kolonnām. abas hierarhijas iepriekš definētas finanšu pārskata noformējumā. Lielākajai daļai finanšu pārskatu rindas hierarhija ir **Galvenā konta tips** \> **Galvenā konta kategorijas** \> **Galvenais konts**. Tomēr dažos pārskatos ir papildu lauki, piemēram, Valsts un Reģions. Hierarhijas papildu mezglu pamatā ir katras transakcijas apakšgrāmatas dati.

Kolonnām hierarhija ir vērsta uz juridiskajām personām un finanšu periodiem. Lielākajai daļai finanšu pārskatu kolonnas hierarhija ir **Juridiska persona** \> **Finanšu kalendārs** \> **Finanšu gads** \> **Ceturksnis** \> **Periods**.

Pašlaik finansu pārskati neatbalsta organizāciju hierarhijas, kas ļauj apkopot datus.

## <a name="data-limitations"></a>Datu ierobežojumi
Finanšu pārskatu vizuālajiem datiem ir ierobežots parādāmo rindu skaits. Pašlaik ierobežojums ir iestatīts uz 30 000. Pārsniedzot šo ierobežojumu, vizuālajiem datiem tiks parādīts brīdinājuma simbols, lai paziņotu jums par šo situāciju.

![Datu ierobežojumi](./media/data-limit.png)

Ja tiek pārsniegts maksimālais skaits, finanšu pārskatā redzamās kopsummas ir nepareizas, jo vizuālajos datos nav ielādētas visas rindas.

### <a name="empty-rows"></a>Tukšas rindas
Power BI nenodrošina tukšu rindu paslēpšanas un rādīšanas opciju. Ja rindā nav nekādu datu, šī rinda netiek rādīta vizuālajos datos.


## <a name="additional-resources-for-power-bi"></a>Papildu resursi pakalpojumam Power BI

Tālāk norādītajos resursos esošā informācija nav nepieciešama, lai iespējotu iegultos pārskatus darbvietai **CFO apskats** vai **Finanšu ieskati** ražošanas vidē. Taču tā ir noderīga izstrādes laukiem un gadījumā, ja vēlaties iegult savus Power BI pārskatus.

- [Piekļūšana analītiskajām darbvietām un pārskatiem 1 lodziņa vidē](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/)

- [Analīzes pievienošana darbvietām, izmantojot Power BI Embedded](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)
