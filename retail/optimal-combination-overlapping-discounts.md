---
title: "Noteikt optimālo kombināciju pārklājas atlaides"
description: "Ja atlaides pārklājas, ir jānosaka pārklāšanās atlaides, kas ražos zemāko darījumu kopsummu vai visaugstāko kopējo atlaidi kombinācija. Ja atlaides summa atkarīga cena produktiem, kas pirkti, piemēram, kopējā &quot;iegādāties 1, izkāpiet 1 X procentiem&quot; (BOGO) mazumtirdzniecības atlaidi, šis process kļūst jautājums combinatorial Optimization."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Noteikt optimālo kombināciju pārklājas atlaides

Ja atlaides pārklājas, ir jānosaka pārklāšanās atlaides, kas ražos zemāko darījumu kopsummu vai visaugstāko kopējo atlaidi kombinācija. Ja atlaides summa atkarīga cena produktiem, kas pirkti, piemēram, kopējā "iegādāties 1, izkāpiet 1 X procentiem" (BOGO) mazumtirdzniecības atlaidi, šis process kļūst jautājums combinatorial Optimization.

Šajā rakstā attiecas uz Microsoft Dynamics AX 2012 R3 ar KB 3105973 (izdots 2 novembris 2015) vai vēlāk, un februārī 2016 atbrīvot no Microsoft Dynamics AX. Lai noteiktu kombināciju pārklājas atlaides pieteikties savlaicīgi, un turpināt nodrošināt bagātīgu funkcionalitāti diskontēšanu, kas ir pieejams sistēmā Microsoft Dynamics AX mazumtirdzniecības, esam ieviesuši pārklājas atlaides piemērošanas metodi. Mēs saucam par šo jauno metodi **rezerves vērtības rangu**. Ranga rezerves vērtība tiek izmantota, kad laiku, kas nepieciešams, lai novērtētu iespējamās kombinācijas pārklājas atlaides pārsniedz slieksni, kas ir konfigurējams ar **mazumtirdzniecības parametrus** lapu Dynamics AX. Marginālā vērtības rangu metode, vērtība tiek aprēķināta katra pārklājas atlaides, izmantojot kopīgu produktu atlaides vērtība. Pārklātu atlaides pēc tam tiek piemērotas no augstākās relatīvās vērtības zemākā relatīvā vērtība. Sīkāku informāciju par jauno metodi, skatiet sadaļu "Rezerves vērtība" tālāk šajā rakstā. Ranga rezerves vērtība netiek izmantots, kad atlaižu summas produktam nav skārusi citu produktu darbība. Piemēram, šī metode nav izmantots divu vienkāršu atlaides vai vienkāršu vai atsevišķu produktu daudzuma atlaide.

## <a name="discount-examples"></a>Atlaide piemēri
Dynamics AX produktu kopumu var izveidot neierobežotu skaitu mazumtirdzniecības atlaides. Tomēr tāpēc, ka nav nekādu ierobežojumu, veiktspējas problēmas var rasties, mēģinot aprēķināt atlaides, kas būtu jāizmanto par dažādiem produktiem. Turpinājumā sniegtie piemēri paskaidro sīkāk šo jautājumu. 1. piemērā mēs sākam ar diviem produktiem un divi pārklājas atlaides. Tad 2. piemērā mēs parādīsim, kā jautājums attīstās vairāk produktu tiek pievienots.

### <a name="example-1-two-products-and-two-discounts"></a>1. piemērs: Divi produkti un divām atlaidēm

Šajā piemērā divi produkti ir vajadzīgi, lai pretendētu uz katru atlaides un atlaides nevar apvienot. Šajā piemērā atlaides tiek **labāko cenu** atlaides. Abi produkti piešķirs gan atlaides. Šeit ir divas atlaides. [![Pārklāšanās atlaide kombinētā 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) jebkuru divu produktu labāk par šīm divām atlaidēm ir atkarīga no divu produktu cenas. Kad abi produktu cenas ir vienādu vai gandrīz vienādu, atlaide 1 ir labāka. Kad viena produkta cena ir ievērojami mazāks nekā cita veida produkcijas cenu atlaide 2 ir labāka. Šeit ir matemātiskā tiesiskuma izvērtēšanai šīm divām atlaidēm pret otru: [![Overlapping atlaide kombinētā 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg), ņemiet vērā, ka, kad 1 produkta cena ir vienāda ar divām trešdaļām no 2 produkta cena, divām atlaidēm ir vienāds. Šajā piemērā efektīvu atlaides procentu atlaidi 1 dažādās pāris procentiem (ja šo abu produktu cenas ir tālu viena no otras) maksimums 25 procenti (ja abi produkti ir pašu cenu). Ir noteikta efektīva atlaides procentu atlaidi 2. Tas vienmēr ir 20 procenti. Tāpēc, ka efektīva atlaides procentu atlaidi 1 ir diapazons, kas var būt lielāks vai mazāks nekā atlaide 2, labākais atlaide ir atkarīga no divus programmproduktus, kuru nedrīkst diskontētās cenas. Šajā piemērā aprēķins ir pabeigts ātrāk, jo tikai divas atlaides tiek piemērotas tikai diviem produktiem. Tur ir tikai divas iespējamās kombinācijas: vienu pieteikumu atlaidi 1 vai vienu piemērot atlaidi 2. Nav neviena aprēķināt permutāciju. Katru atlaides vērtība tiek aprēķināta, izmantojot abus produktus, un labākais atlaide tiek izmantots.

### <a name="example-2-four-products-and-two-discounts"></a>2. piemērs: Četriem produktiem un divām atlaidēm

Tālāk, mēs izmantosim četriem produktiem un pašu divām atlaidēm. Visiem četriem produktiem piešķirs gan atlaides. Ir divpadsmit iespējamās kombinācijas. Galu galā divas atlaides piemēros darbības vienā no trim kombinācijas: divus pieteikumus atlaidi 1, divus pieteikumus atlaide atlaide 2 1 un vienu atlaižu piemērošanas 2 vai vienu pieteikumu. Lai ilustrētu iespējamās kombinācijas, mēs apskatīsim divas atšķirīgas četrus produktus, kuros ir atšķirīgas cenas:

-   Visiem četriem produktiem ir tā pati cena, $15.00. Šajā gadījumā labākais atlaižu kombināciju ir divas programmas atlaides 1. Divi produkti būs pilna cena, un divi būs 50 procenti nost. Diskontēta kopējo darījuma $45 (15 + 15 + 7.50 + 7.50), kas ir $15 (25 procenti) ir izslēgta nediskontētā summa $60. 2. atlaide ir tikai $12 (20 procenti).
-   Abi produkti ir $20 katram, vienam produktam ir $15 un viens produkts ir $5. Šajā gadījumā labākais atlaižu kombināciju ir viens pieteikums 2 un vienu atlaižu piemērošanas atlaide 1. Šīs tabulas parāda atlaides.

Lasīt tabulām, izmantojiet vienu no rindas un viena produkta no kolonnas. Piemēram, tabulā 1 atlaidei, ja kombinçjat divus $20 produktus, jūs izkāpt $10. Tabulas 2. atlaides, kad jūs apvienot $5 produkts, un $15 jūs izkāpt $4. [![Pārklāšanās atlaide kombinētā 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) Pirmkārt, mēs atrodam lielāko atlaidi, kas ir pieejama no jebkura divu produktu, izmantojot vai nu atlaidi. Abas tabulas liecina atlaižu summa visām kombinācijām, šo abu produktu. Ēnota daļas tabulas atspoguļo abos gadījumos, kur produkts tiek savienots pārī ar sevi, ko mēs nevaram darīt, vai reversā pāri par divi produkti, ko ražo pats atlaides summa un to var ignorēt. Apskatot tabulas, jūs varat redzēt, ka atlaide 1 divas $20 precēm ir vislielākā atlaide, kas ir pieejams vai nu atlaidi visiem četriem produktiem. (Šī atlaide ir izcelta zaļā krāsā pirmajā tabulā.) Tas atstāj tikai $15 $5 produkts un. Vēlreiz aplūkojot divas tabulas, jūs varat redzēt, šo divu produktu atlaides 1 dod atlaidi $2.50 tā kā atlaide 2 dod atlaidi $4. Tādēļ mēs izvēlamies atlaidi 2. Kopējā atlaide ir $14. Lai padarītu vieglāk iztēloties šo diskusiju, šeit ir divas papildu tabulas, kas liecina, ka efektīva atlaidi procentos visu iespējamo divu produktu kombinācijām, gan atlaides 1 un atlaide 2. Tikai puse kombinācijas saraksts ir iekļauts, jo attiecībā uz šīm divām atlaidēm, šie divi produkti tiek ievietoti atlaižu secība nav nozīmes. Efektīva lielāko atlaidi (25 procenti) ir izcelta zaļā krāsā un zemāko efektīvu atlaižu (10 procenti) ir izcelti sarkanā krāsā. [![Pārklāšanās atlaide kombinētā 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Piezīme:** cenas atšķiras un divu vai vairāku atlaižu konkurēt, vienīgais veids, kā garantēt labāko kombināciju atlaides ir jāizvērtē gan atlaides un salīdzināt tos.

## <a name="total-possible-combinations"></a>Kopā iespējamās kombinācijas
Šajā sadaļā joprojām piemēru no iepriekšējā sadaļā. Mēs pievienot vairāk produktu un citu atlaižu un redzēt, cik kombinācijas aprēķināt un salīdzināt. Tabulā ir parādīts produkta daudzums palielinās skaits iespējamās atlaižu kombinācijas. Tabulā parādīts, kas notiek gan, ja ir divi pārklājas atlaides, tāpat kā iepriekšējā piemērā, un, ja tur ir trīs pārklāšanās atlaides. Iespējamās atlaižu kombinācijas, kas jānovērtē skaits drīz pārsniedz pat ātrs dators var aprēķināt un salīdzināt tik ātri par pieņemamām mazumtirdzniecības darījumiem. [![Pārklāšanās atlaide kombinētā 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) kad pat lielākos daudzumos vai vairāk pārklājošos atlaides tiek piemērotas, iespējamās atlaižu kombinācijas kopējais skaits ātri tērēta miljoniem un laiku, kas nepieciešams, lai novērtētu un ātri izvēlēties labāko iespējamo kombināciju kļūst pamanāmas. Dažiem optimizācijām ir izdarīts mazumtirdzniecības cenu dzinējs samazināt kopējo skaitu kombinācijas, kas jānovērtē. Tomēr jo numuru pārklājas atlaides un daudzumu darījumā nav ierobežota, lielu kombināciju skaits vienmēr būs jāizvērtē, kad pastāv pārklāšanās atlaides. Šis jautājums ir jautājums, kas marginālā vērtības rangu metode adreses.

## <a name="marginal-value-method"></a>Marginālā vērtības metode
Atrisināšanai eksponenciāli pieaugošā skaita kombināciju, kas jānovērtē, optimizācijas pastāv, kas aprēķina vērtību uz vienu kopīgu produktu katru atlaides uz produktiem, ko var piemērot divus vai vairākus atlaides kopumu. Mēs atsaucamies uz šo vērtību kā **rezerves vērtība** kopīgu produktu atlaides. Marginālā vērtība ir vidējā produkta pieaugums kopējā atlaižu summa vienam kad koplietošanas produkti ir iekļauti katra atlaides. Marginālā vērtība tiek aprēķināta, veicot kopīgu produktu bez atlaides summas atskaitīšanas kopējā atlaižu summa (DTotal) (DMinus\\ Shared), un dalot šo starpību ar kopīgu produktu (ProductsShared) skaits. [![Pārklāšanās atlaide kombinētā 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) pēc nakti katru atlaidi par kopīgu produktu komplektu vērtība tiek aprēķināta, atlaides tiek piemērotas kopīgu produktu secībā, izsmeļoši, no malējā augstākā vērtība, robežizmaksu zemāko vērtību. Šai metodei, visas atlikušās atlaižu iespējas nav salīdzināt katru reizi pēc tam, kad uz vienu entitātes gadījumu atlaidi piemēro. Tā vietā pārklājas atlaides salīdzinot vienu reizi un pēc tam piemērotas tādā secībā. Tiek darīts bez papildu salīdzinājumus. Slieksni, lai ieslēgtu rezerves vērtības metodi var konfigurēt **Discount** cilnē **mazumtirdzniecības parametrus** lapā. Pieņemamā laikā aprēķināt kopējo atlaidi, ir atkarīgs no mazumtirdzniecības nozarēs. Tomēr šajā laikā parasti ietilpst diapazonā no desmitiem milisekundes uz vienu sekundi.


