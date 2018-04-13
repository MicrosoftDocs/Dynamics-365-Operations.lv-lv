---
title: "Attēlu iestatīšana un pārvaldība Retail Modern POS"
description: "Šajā rakstā ir paskaidroti soļi, kas jāveic, iestatot un pārvaldot attēlus dažādiem elementiem, kas tiek parādīti Retail Modern POS (MPOS)."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed4a7044b577ed6af86f6803f6abd4f9b500b4e7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Attēlu iestatīšana un pārvaldība Retail Modern POS

[!INCLUDE [banner](includes/banner.md)]

Šajā rakstā ir paskaidroti soļi, kas jāveic, iestatot un pārvaldot attēlus dažādiem elementiem, kas tiek parādīti Retail Modern POS (MPOS).

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Multivides bāzes vietrāža URL iestatīšana un multivides veidņu definēšana, lai konfigurētu attēlu vietrāžu URL formātu
-------------------------------------------------------------------------------------------------

Attēli, kas parādās Retail Modern POS (MPOS), jāizvieto ārēji, ārpus Microsoft Dynamics 365 for Retail. Parasti tie ir izvietoti satura vadības sistēmā, satura piegādes tīklā (CDN) vai multivides serverī. Pēc tam MPOS ienes un parāda atbilstošo elementu, piemēram, preču un katalogu, attēlus, piekļūstot mērķa vietrādim URL. Lai ienestu šos ārējos attēlus, MPOS nepieciešams pareizs attēlu vietrāža URL formāts. Nepieciešamo attēlu vietrāžu URL formātu var konfigurēt, iestatot vērtību **Multivides bāzes vietrādis URL** kanāla profilā un izmantojot funkciju **Definēt multivides veidni** katram elementam. Varat arī pārrakstīt elementu apakškopas standarta vietrāža URL formātu, izmantojot funkciju **Rediģēt programmā Excel**. **Svarīga piezīme.** Pašreizējā Dynamics 365 for Retail versijā vietrāža URL formātu vairs nevar iestatīt, izmantojot atribūta **Attēls** XML MPOS elementu atribūtu grupā **Noklusējuma**. Ja jūs esat pazīstami ar Microsoft Dynamics AX 2012 R3 un tagad izmantojat pašreizējo Dynamics 365 for Retail versiju, pārliecinieties, ka attēlu iestatīšanai vienmēr izmantojat jauno funkciju **Definēt multivides veidni**. Neizmantojiet un nemainiet atribūtu **Attēls** elementiem, tostarp precēm, atribūtu grupā **Noklusējuma**. Izmaiņas, ko veicat attēlos tieši atribūtu grupā **Noklusējuma**, netiks atspoguļotas. Šī opcija būs atspējota nākamajos laidienos. Nākamajās procedūrās, kā piemērs, attēli tiek iestatīti elementam Katalogs. Šīs procedūras palīdzēs nodrošināt, ka visiem kataloga attēliem, kas izmanto kopīgo ceļu, netieši iestatīts pareizais attēlu mērķa ceļš. Piemēram, ja ir ārēji iestatīts multivides serveris vai CDN, un vēlaties, lai attēli parādītos MPOS konkrētajam veikalam, funkcija **Definēt multivides veidni** palīdz iestatīt ceļu, kur MPOS var uzmeklēt un iegūt attēlus. **Piezīme:** šajā demonstrācijas datu piemērā multivides serveris ir izvietots mazumtirdzniecības serverī. Tomēr tas var būt arī jebkur ārpus Dynamics 365 for Retail.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Multivides bāzes vietrāža URL iestatīšana kanālam

1.  Atveriet Dynamics 365 for Retail HQ portālu.
2.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **Kanāla profili**. [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Kanāla profilā, ko jūsu veikals izmanto MPOS, atjauniniet lauku **Multivides bāzes vietrādis URL**, norādot sava multivides servera vai CDN pamata vietrādi URL. Bāzes vietrādis URL ir pirmā URL vietrāža daļa, kas ir kopīga visām dažādu elementu attēlu mapēm.[![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Elementa multivides veidnes definēšana

1.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kataloga pārvaldība** &gt; **Kataloga attēli**.
2.  Lapā **Kataloga attēli** darbību rūtī noklikšķiniet uz **Definēt multivides veidni**. Dialoglodziņā **Definēt multivides veidni** laukā **Elements** jābūt pēc noklusējuma atlasītai vērtībai **Katalogs**.
3.  Kopsavilkuma cilnē **Multivides ceļš** ievadiet atlikušo attēla atrašanās vietas ceļu. Multivides ceļš atbalsta **LanguageID** kā mainīgo. Piemēram, demonstrācijas datiem var izveidot mapi **Katalogi** visiem kataloga attēliem zem sava multivides servera multivides bāzes vietrāža URL (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Tad jums var būt mape katrai valodai, piemēram, en-US vai fr-FR, un varat kopēt atbilstošos attēlus zem katras mapes. Ja jums nav dažādu attēlu dažādām valodām, var izlaist mainīto **LanguageID** mapes struktūrā un norādīt tieši uz mapi Katalogi, kurā atrodas kataloga attēli. **Piezīme:** Dynamics 365 for Retail pašreizējā versija atbalsta **{LanguageId}** marķieri elementiem Katalogs, Prece un Kategorija. (Saskaņā ar esošo standartu, kas ir spēkā kopš Microsoft Dynamics AX 6.x, **{LanguageID}** marķieris netiek atbalstīts elementos Debitors un Darbinieks.)
4.  Attēlu faila nosaukuma formāts ir stingri kodēts uz kataloga nosaukumu un to nevar mainīt. Tāpēc pārdēvējiet attēlus tā, lai tiem būtu atbilstoši kataloga nosaukumi, lai palīdzētu nodrošināt, ka MPOS tos apstrādā pareizi.
5.  Laukā **Faila paplašinājums** atlasiet paredzēto faila nosaukuma paplašinājumu, atkarībā no jūsu attēlu tipa. Piemēram, demonstrācijas datos kataloga attēli ir iestatīti uz paplašinājumu .jpg. (Attēlu faili tiek pārdēvēti arī tā, lai tiem būtu kataloga nosaukumi.)
6.  Noklikšķiniet uz **Labi**.
7.  Lai apstiprinātu, ka multivides veidnes attēliem ir pareizi saglabātas lapā **Kataloga attēli** vēlreiz noklikšķiniet uz **Definēt multivides veidni**. Lai apstiprinātu veidni, neaizverot dialoglodziņu **Definēt multivides veidni** var izmantot kopsavilkuma cilni **Ģenerēt attēlu vietrāžus URL programmai Excel**. Pārbaudiet attēla vietrāža URL izskatu un, vai vietrādis URL atbilst veidnes standartam, kas minēts iepriekš. Dialoglodziņā **Definēt multivides veidni** tagad netieši iestatīts attēla ceļš visiem kataloga attēliem, kuros tiek izmantots šis kopējais vietrāža URL ceļš. Šis vietrāža URL ceļš attiecas uz visiem kataloga attēliem, ja vien tie netiek pārrakstīti. Pirmā attēla ceļa daļa tiek ņemta no multivides bāzes vietrāža URL, ko definējāt kanāla profilā. Atlikusī ceļa daļa tiek ņemta no ceļa, ko definējāt multivides veidnē. Divas daļas tiek apvienotas, lai sniegtu pilnu attēla atrašanās vietas vietrādi URL. Piemēram, kataloga nosaukums demonstrācijas datos ir Fabrikam Base Catalog. Tāpēc attēla nosaukumam ir jābūt Fabrikam Base Catalog.jpg, lai tiktu izmantots kataloga nosaukums un. jpg faila nosaukuma paplašinājums, kas ir konfigurēts veidnē. Šajā gadījumā, pēc apvienošanas vietrādis URL būs https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Izpildiet sinhronizēšanas darbus, lai virzītu jaunu veidni uz kanāla datu bāzi, lai MPOS varētu izmantot veidni, lai piekļūtu attēliem.
9.  Lai atjauninātu multivides veidni kataloga attēliem kanāla pusē, noteikti palaidiet **Kataloga darbu 1150** no **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.[![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Attēlu priekšskatīšana no elementa līmeņa
1.  No HQ elementa krājuma lapas var priekšskatīt attēlu, kurā izmantots attēla vietrādis URL, kas tiek atvasināts no multivides veidnes. Šajā piemērā dodieties uz atbilstošo katalogu un pēc tam darbību rūtī noklikšķiniet uz **Multivide** &gt; **Attēli**. Izmantojiet nolaižamo sarakstu, lai atlasītu dažādus veikalus, kuriem varētu būt dažādi kanāla profili.
2.  Lai rediģētu vai noņemtu netiešu multivides veidni, jums ir jāatgriežas dialoglodziņā **Definēt multivides veidni**, kas attiecas uz lapu **Kataloga attēli**.
3.  Var izmantot pogas **Pievienot** un **Noņemt**, lai manuāli mainītu ceļu, kas ir balstīts uz netiešo veidni un lietots noteiktam attēlam. Papildinformāciju skatiet sadaļā "Elementu krājumu multivides veidnes pārrakstīšana" tālāk šajā raksta.
4.  Kad esat pabeidzis attēla priekšskatīšanu un veicis jebkādas nepieciešamās izmaiņas, palaidiet atbilstošā veikala MPOS instanci un skatiet, vai tiek parādīti kataloga attēli.[![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Piezīme:** varat izmantot tādu pašu procedūru visiem pieciem elementiem, kas tiek atbalstīti: Darbinieks, Debitors, Katalogs, Kategorija un Preces. "Kataloga preces" (preces, kas iestatītas kataloga līmenī) un "Kanāla preces" (preces, kas iestatītas kanāla līmenī) izmanto multivides veidni, kas ir iestatīta elementam Preces. Preču multivides veidnei var atlasīt vairākus preču attēlus, lai tos parādītu katrai precei. Jūs varat arī iestatīt noklusējuma attēlu konkrētai precei. Šādā veidā varat novērst tukšus attēlus MPOS un palīdzēt kontrolēt, kurš attēls tiek izmantots kā noklusējuma attēls produkta krājumam. Šajā piemērā, katrai precei ir pieci attēli un pirmais attēls ir iestatīts kā noklusējuma attēls. Preču varianti tiek apstrādāti tāpat, kā pamata preces. Attēla faila nosaukumam ir jābalstās uz preces numuru. Dažas rakstzīmes arī tiek pārslēgtas, kamēr faila nosaukums tiek ģenerēts. Tāpēc būtu labi pārbaudīt faila nosaukumu, izmantojot sadaļu **Ģenerēt attēlu vietrāžus URL programmai Excel**. [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Sinhronizēšanas darbi, lai nosūtītu multivides veidni uz kanāla pusi
Visiem pieciem atbalstītajiem elementiem (Darbinieks, Debitors, Katalogs, Kategorija un Preces) ikreiz, kad jūs atjaunināt dialoglodziņu **Definēt multivides veidni**, lai iestatītu attēlu, pārliecinieties, ka izpildāt Kataloga darbu (1150) no **Mazumtirdzniecības IT** &gt; **Sadales grafiks**. Šis darbs aktivizēs atjaunotās multivides veidnes sinhronizāciju ar kanālu un ļaus MPOS to izmantot. Palaidiet Kataloga darbu (1150), ja veicāt kādu no šādām izmaiņām:

-   Jūs atjaunināt Kataloga attēla multivides veidni no **Kataloga attēli** &gt; **Definēt multivides veidni**.
-   Jūs atjaunināt Darbinieka attēla multivides veidni no **Darbinieka attēli** &gt; **Definēt multivides veidni**.
-   Jūs atjaunināt Debitora attēla multivides veidni no **Debitora attēls** &gt; **Definēt multivides veidni**.
-   Jūs atjaunināt Preces attēla multivides veidni no **Preces attēli** &gt; **Definēt multivides veidni**.
-   Jūs atjaunināt Kategorijas attēla multivides veidni no **Kategorijas attēli** &gt; **Definēt multivides veidni**. Jums ir arī jāpublicē kanāls.

## <a name="overwriting-the-media-template-for-entity-items"></a>Elementa krājumu multivides veidnes pārrakstīšana
Kā minēts iepriekšējā sadaļā, noteiktā elementa multivides veidne atbalsta tikai vienu kopīgu ceļu. Šis ceļš ir balstīts uz konfigurēto multivides pamata vietrādi URL un definēto multivides ceļu. Tomēr daudzos gadījumos mazumtirdzniecības veikals vēlas, lai krājumu apakškopai elementā varētu izmantot attēlus no dažādiem avotiem. Piemēram, veikals izmanto pašviesotu multivides serveri vienai kataloga attēlu kopai un CDN vietrāžus URL citai kopai. Lai pārrakstītu attēla vietrādi URL elementa attēlu multivides veidnē elementa līmenī, varat izmantot funkciju Rediģēt programmā Excel un funkciju Manuāli rediģēt lapā **Priekšskatījums**.

### <a name="overwrite-by-using-edit-in-excel"></a>Pārrakstīšana, izmantojot funkciju Rediģēt programmā Excel

1.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kataloga pārvaldība** &gt; **Kataloga attēli**.
2.  Lapā **Kataloga attēli** noklikšķiniet uz **Definēt multivides veidni**. Dialoglodziņā **Definēt multivides veidni** laukā **Elements** jāatlasa **Katalogs**.
3.  Kopsavilkuma cilnē **Multivides ceļš** ņemiet vērā attēla atrašanās vietu.
4.  Kopsavilkuma cilnē **Ģenerēt attēlu vietrāžus URL programmai Excel** noklikšķiniet uz **Ģenerēt**. **Svarīgi:** kad multivides veidne tiek mainīta, jums jānoklikšķina uz **Ģenerēt** pirms varat izmantot funkciju Rediģēt programmā Excel. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Tagad ir redzams tādu attēla vietrāžu URL priekšskatījums, kas tika ģenerēti, pamatojoties uz pēdējo saglabāto multivides veidni. [![excel2](./media/excel2.png)](./media/excel2.png) **Piezīme.** Vietrāžos URL, kas tiek ģenerēti programmai Excel, tiek izmantots ceļš un definētās multivides veidnes noteikumi. Šie noteikumi ietver failu nosaukumu veidošanas noteikumus. Paredzams, ka esat iestatījis fiziskos attēlus ārpus Dynamics 365 for Retail un attēlus var izgūt no vietrāžiem URL, kas atvasināti no iepriekš definētās veidnes. Šos atvasinātos vietrāžus URL var pārrakstīt, izmantojot funkciju Rediģēt programmā Excel.
5.  Noklikšķiniet uz **Rediģēt programmā Excel**.
6.  Kad ir atvērta darblapa Microsoft Excel, noklikšķiniet uz **Iespējot rediģēšanu**, kad tiek parādīta uzvedne.
7.  Kad tiek parādīta uzvedne, noklikšķiniet uz **Uzticēties šai pievienojumprogrammai** labajā rūtī un uzgaidiet, kamēr pievienojumprogramma tiek instalēta. [![Uzticēties šai pievienojumprogrammai](./media/excel4.jpg)](./media/excel4.jpg)
8.  Ja tiek piedāvāts pierakstīties, ievadiet akreditācijas datus, ko izmantojat, lai pierakstītos HQ. [![Pierakstīšanās uzvedne](./media/excel5.png)](./media/excel5.png)
9.  Kad esat pierakstījies, vajadzētu būt redzamam attēlu vietrāžu URL sarakstam dažādiem kataloga ierakstiem.
10. Rediģējiet, pievienojiet vai noņemiet attēlu vietrāžus URL dažādiem elementu krājumiem.
11. Visiem elementiem, izņemot Preces, attēla vietrādi URL var pārrakstīt. Modificējiet esošo attēla vietrādi URL, lai tas izmantotu jaunu attēla galamērķa vietrādi URL un atjauninātu faila nosaukumu ar jaunu šī attēla faila nosaukumu. Faila nosaukumam ir jābūt unikālam, lai palīdzētu nodrošināt, ka ieraksts ir unikāls. [![Attēla vietrāžu URL pārrakstīšana programmā Excel](./media/excel6.jpg)](./media/excel6.jpg) **Piezīme.** Kad jūs pārrakstāt attēla vietrāžus URL elementiem Preces, izmantojot funkciju Rediģēt programmā Excel vai elementa krājumu lapā, MPOS vienmēr rāda visus multivides veidnes attēlu vietrāžus URL kopā ar pārrakstītajiem attēlu vietrāžiem URL.
12. Kad esat beidzis veikt izmaiņas, noklikšķiniet uz **Publicēt programmā Excel**, lai izveidotu jaunu tiešas saistības ierakstu.
13. Atgriezieties uz HQ un noklikšķiniet uz **Labi**.
14. Palaidiet atbilstošus elementa sinhronizēšanas darbus un pārbaudiet priekšskatījumu elementa lapā vai MPOS.

#### <a name="creating-new-records"></a>Jaunu ierakstu veidošana

Jaunus ierakstus var veidot programmā Excel. Tomēr, pārliecinieties, vai tiek norādīta pareiza informācija. Piemēram, lai izveidotu jaunu ierakstu katalogā, pārliecinieties, vai kataloga ID un kataloga nosaukums ir pareizs un norādiet arī unikālu faila nosaukumu. Unikāls faila nosaukums ir ļoti svarīgs, jo ierakstu unikalitāte programmā Excel tiek apstiprināta publicēšanas laikā. Vispirms nokopējiet informāciju no kataloga, kuram vēlaties izveidot jaunu ierakstu, un kopējiet ierakstu. Jums vienkārši ir jāatjaunina faila nosaukums un vietrādis URL, jo pārējā informācija būs tāda pati. Lai izveidotu jaunus ierakstus elementa Preces krājumiem, izmantojiet to pašu pamata procedūru. No Excel darblapas kopējiet esošu ierakstu precei, kurai izveidojat jaunu ierakstu, un pēc tam aizstājiet attēla vietrādi URL un faila nosaukumu. Pārliecinieties, ka faila nosaukums ir unikāls.

#### <a name="deleting-an-existing-record"></a>Esoša ieraksta dzēšana

Var dzēst tikai pārrakstītus attēla vietrāžu URL ierakstus. Kad attēls ir dzēsts un sinhronizācija ir pabeigta, attēls vairs neparādīsies lapā **Priekšskatījums** vai MPOS. Attēla vietrāža URL ierakstus, kas ir iegūti no multivides veidnes, nevar dzēst, jo šie ieraksti vienmēr, katru reizi tiek atvasināti no multivides veidnes.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Pārrakstīšana no elementa līmeņa lapas Priekšskatījums

Visiem elementiem, izņemot Preces, var pārrakstīt dotā elementā krājuma attēlu vietrādi URL elementa krājuma līmenī no lapas **Priekšskatījums**. Precēm var izmantot elementa lapu "Kataloga preces". Šajā piemērā parādīts, kā pārrakstīt kataloga attēlu.

1.  Noklikšķiniet uz **Katalogi** &gt; **Multivide** &gt; **Attēli**, un atlasiet kataloga attēlu, kurš jāatjaunina.
2.  Noklikšķiniet uz **Pievienot** un ievadiet attēla vietrādi URL, lai pārrakstītu multivides veidnes vietrādi URL.
3.  Ja vēlaties, lai šis attēls būtu redzams katalogam MPOS, to var iestatīt kā noklusējuma attēlu.
4.  Noklikšķiniet uz **Labi**. Attēla vietrādis URL tiek atjaunināts šim kataloga attēlam, un tiek parādīts priekšskatījums. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Jūs varat arī redzēt visu pārrakstīto attēlu vietrāžu URL attēla priekšskatījumu galerijas lapā **Kataloga attēli**.

**[![preview-4](./media/preview-4.png)](./media/preview-4.png)Piezīme.** Pašlaik galerija nerāda attēlu priekšskatījumus multivides veidnes attēlu vietrāžiem URL. Ja elementos Katalogs, Darbinieks, Debitors un Kategorija lietotājs skaidri norāda vietrādi URL, izmantojot šo lapu, mēs iesakām norādīt, kurš attēls ir noklusējuma attēls, jo mazumtirdzniecības servera klientiem tiek rādīts tikai viens attēls uz Katalogu, Debitoru, Darbinieku un Kategoriju. Ja lietotājs nenorāda noklusējuma attēlu, sistēma nosaka noklusējuma attēlu un nosūta to mazumtirdzniecības pakalpojumu izsaucējam (MPOS vai e-Komercija).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Kataloga preces attēlu vietrāža URL pārrakstīšana no lapas Priekšskatījums

Lai pārrakstītu kataloga preču attēlu vietrāža URL, jāizmanto lapa **Priekšskatījums**. Funkcionalitāti Rediģēt programmā Excel izmantot nevar.

1.  Lai pārrakstītu preču attēlus kataloga līmenī, atlasiet katalogu un pēc tam atlasiet preci, kuras attēlu nepieciešams pārrakstīt.
2.  Noklikšķiniet uz **Atribūti**.
3.  Nākamajā lapā atlasiet **Attēls** un tad noklikšķiniet uz **Rediģēt**. Lapa **Priekšskatījums** tiek atvērta kā slīdņa dialoglodziņš.
4.  Noklikšķiniet uz **Pievienot** un pārrakstiet attēla vietrādi URL ar jaunu vietrādi URL.
5.  Noklikšķiniet uz **Labi**. Jūs tagad redzat jauna attēla priekšskatījumu un varat to iestatīt kā noklusējuma attēlu.

**[![cat3](./media/cat3.png)](./media/cat3.png)Piezīme.** Pēc kategorijas attēlu saistīšanas jāpublicē kanāls un jāpalaiž Kanāla darbs, lai palīdzētu nodrošināt, ka izmaiņas tiek publicētas kanāla datu bāzē.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Attēlu, kas parādīsies MPOS bezsaistes režīmā, iestatīšana
MPOS var darboties tiešsaistes režīmā (kad MPOS pieslēgts mazumtirdzniecības serverim) vai bezsaistes režīmā (kad nav mazumtirdzniecības servera vai tīkla savienojamības, un transakcijas tiek saglabātas vietējā bezsaistes datu bāzē). Kad MPOS darbojas bezsaistes režīmā, tas nevar iegūt attēlus no ārējā attēlu servera, lai tos parādītu no mazumtirdzniecības servera, jo mazumtirdzniecības servera savienojamība ir zudusi. Tomēr joprojām var iestatīt attēlus, lai tie tiktu rādīti, kad MPOS darbojas bezsaistes režīmā.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Preču attēlu, kas parādīsies MPOS bezsaistes režīmā, iestatīšana

Preču attēlus, kas jāizmanto bezsaistes režīmā, var iestatīt, augšupielādējot vajadzīgo fizisko attēlu pamata preces attēlā.

1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Preces**.
2.  Atlasiet preci, kurai vēlaties iestatīt bezsaistes attēlu.
3.  Noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz bultiņas labajā stūrī, lai parādītu labo rūti.
4.  Kopsavilkuma cilnē **Preces attēls** noklikšķiniet uz **Mainīt attēlu** un augšupielādējiet fizisko attēlu, ko izmantot atlasītajai precei ir bezsaistes režīmā.
5.  Saglabājiet un aizveriet lapu.
6.  Kamēr MPOS darbojas tiešsaistes režīmā, izpildiet HQ Kataloga darbu, lai pārliecinātos, ka dati tiek sūtīti uz bezsaistes datu bāzi vismaz vienu reizi.
7.  Aktivizējiet MPOS bezsaistes režīmā. Vajadzētu būt redzamam attēlam, ko augšupielādējāt noteiktai precei HQ. [![offline1](./media/offline1.png)](./media/offline1.png)



### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Kataloga, kategorijas, darbinieka un debitora attēlu, kas parādīties MPOS bezsaistes režīmā, iestatīšana

Kataloga, kategorijas, darbinieka un debitora attēlus, kas jāizmanto bezsaistes režīmā, var iestatīt, pievienojot vajadzīgā attēlā galamērķa saiti galerijai un iestatot attēlu kā noklusējuma attēlu atlasītajam elementam.

1.  Dodieties uz katalogu un pēc tam darbību rūtī noklikšķiniet uz **Multivide** &gt; **Attēli**.
2.  Izpildiet darbības sadaļā "**Pārrakstīšana no elementa līmeņa lapas Priekšskatījums**", lai pievienotu ārējo attēla vietrādi URL.
3.  Atzīmējiet šo attēlu kā noklusējuma attēlu katalogam, atzīmējot izvēles rūtiņu pretī Attēlam režģī.
4.  Izpildiet Kataloga darbu. Tagad šis attēls tiks izmantots kā šī kataloga bezsaistes attēls MPOS.
5.  Veiciet līdzīgu procedūru citiem elementiem, piemēram, Kategorijai, Darbiniekam un Debitoram.

[![offline2](./media/offline2.png)](./media/offline2.png)    




