---
title: "Pirkšanas ierobežojumi"
description: "Šajā rakstā ir sniegta informācija par pirkšanas ierobežojumiem. Pirkšanas ierobežojumi ir nosacījumu kopums, kas kontrolē pieprasījumu procesu. Pirkšanas ierobežojumi palīdz sagādes administratoriem ieviest sagādes stratēģiju, izveidojot politikas struktūru, kas ir saskaņota ar organizācijas stratēģiskajām pirkšanas prasībām."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 675a7a8b0da228e789ee37ca8fe1d0c0ea01c283
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="purchasing-policies"></a>Pirkšanas ierobežojumi

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par pirkšanas ierobežojumiem. Pirkšanas ierobežojumi ir nosacījumu kopums, kas kontrolē pieprasījumu procesu. Pirkšanas ierobežojumi palīdz sagādes administratoriem ieviest sagādes stratēģiju, izveidojot politikas struktūru, kas ir saskaņota ar organizācijas stratēģiskajām pirkšanas prasībām.

Pirkšanas ierobežojumi sastāv no ierobežojuma nosacījumu kopas. Definējot ierobežojuma nosacījumu, vispirms ir jāatlasa nosacījuma tips. Pēc tam izveidojiet nosacījumu nosacījuma tipam, definējot nosacījuma iestatījumus, sākuma datumu un beigu datumu.  

Piemēram, administrators izveido ierobežojumus, atlasa nosacījuma tipu **Kataloga ierobežojums** un pēc tam pievieno to kataloga ierobežojuma nosacījumu politikai. Šis kataloga ierobežojuma nosacījums norāda, ka Adventure katalogs ir jāizmanto iekšējai sagādei. Kad pirkšanas ierobežojumi ir saistīti ar konkrētu organizāciju, šīs organizācijas darbinieki redz Adventure katalogu, veidojot pieprasījumus.

## <a name="assigning-policies-to-organizations"></a>Ierobežojumu piešķiršana organizācijām
Lai ierobežojumi stātos spēkā, tiem jābūt saistītiem ar organizāciju. Pirkšanas ierobežojumi ir saistīti ar hierarhijas nolūku **Sagādes iekšējā kontrole**. Tāpēc pirkšanas ierobežojumi attiecas tikai uz organizācijām hierarhijās, kurām ir hierarhijas nolūks **Sagādes iekšējā kontrole**. Var arī atlasīt organizācijas no juridisko personu nekārtota saraksta tabulā CompanyInfo. Šīs juridiskās personas norādītas ierobežojumu struktūrā kā "Uzņēmumi".

## <a name="determining-which-rule-to-apply"></a>Noteikšana, kādus ierobežojumus lietot
Atkarībā no tā, kā konfigurējāt pirkšanas ierobežojumus, vairāki nosacījumi var ietekmēt organizācijas lietotājus. Sekojošie piemēri parāda dažādus veidus, ko var konfigurēt pirkšanas ierobežojumos un norādīt, kā ierobežojumi tiek lietoti, kad notiek transakcijas.

### <a name="example-1-simple-purchasing-policy-configuration"></a>1. piemērs: vienkārša pirkšanas ierobežojumu konfigurācija

Mazas un ne tik sarežģītas organizācijas var iestatīt pirkšanas ierobežojumus atbilstoši juridiskajai personai un var izmantot tikai uzņēmumu organizācijas hierarhiju.  

Mazam uzņēmumam Fabrikam pirkšanas prasības gandrīz neatšķiras visā organizācijā. Pirkšanas nosacījumi atšķiras tikai starp organizācijas juridiskajām personām. Piemēram, Fabrikam Kanāda darbinieki un Fabrikam ASV darbinieki iegādājas preces un pakalpojumus no dažādiem katalogiem un dažādiem kreditoriem. Tāpēc Fabrikam iestata pirkšanas ierobežojumus juridiskās personas līmenī.  

Fabrikam izveido divus pirkšanas ierobežojumus. A ierobežojums attiecas uz ASV juridisko personu 1111. B ierobežojums attiecas uz Kanādas juridisko personu 2222. Kad juridiskās personas 1111 darbinieks izveido pirkšanas pieprasījumu, ierobežojuma nosacījumi tiek atvasināti no A ierobežojuma. Piemēram, preču katalogs, ko šis darbinieks redz, ir norādīts A ierobežojuma kataloga ierobežojuma nosacījumos.  

Kad juridiskās personas 2222 darbinieks izveido pirkšanas pieprasījumu, ierobežojuma nosacījumi tiek atvasināti no B ierobežojuma  

**Piezīme:** ja juridiskās personas 1111 darbinieks kādu krājumu iegādājas juridiskās personas 2222 darbinieka vārdā, tiek piemēroti tie ierobežojuma nosacījumi, kas ir norādīti juridiskajai personai 2222 (t.i., ierobežojuma nosacījumi no ierobežojumiem B).

### <a name="example-2-complex-purchasing-policy-configuration"></a>2. piemērs: sarežģīta pirkšanas ierobežojumu konfigurācija

Iepriekšējā piemērā, visi pirkšanas nosacījumi tika noteikti vienā organizācijas hierarhijā — Uzņēmumu organizācijas hierarhijā. Tomēr sarežģīta organizācija var definēt ierobežojumus vairākām organizācijas hierarhijām.  


Contoso ir liels uzņēmums, kas pieprasa sarežģītus pirkšanas nosacījumus, lai kontrolētu pieprasījuma procesu. Contoso ir noteicis nosacījumus divām dažādām organizācijas hierarhijām: Nodaļas un Globāla pirkšanas kontrole.  

Ierobežojumi 123 ir definēti Nodaļu organizācijas hierarhijai Pārdošanas Lielbritānijas — Pārdošanas nodaļai. Ierobežojumos 123 pirkšanas pieprasījuma kontroles nosacījumi norāda, ka ierobežojumi jāpiemēro minimāliem pasūtījuma daudzumiem. Šajos nosacījumos ir atlasīta opcija **Ieviest minimālā pasūtījuma daudzuma ierobežojumus**.  

Ierobežojumi 456 ir definēti Globālās iepirkumu kontroles organizācijas hierarhijai Pārdošanas un mārketinga nodaļai. Ierobežojumos 456 pirkšanas pieprasījuma kontroles nosacījumi nenorāda, ka ierobežojumi jāpiemēro minimāliem pasūtījuma daudzumiem. Šajos nosacījumos ir atlasīta opcija **Ieviest minimālā pasūtījuma daudzuma ierobežojumus**.  

Sems darbojas Pārdošanas Lielbritānijas — Pārdošanas nodaļā Contoso Apvienotās Karalistes birojā. Šai nodaļai piemērojami gan Nodaļu un Globālās pirkšanas kontroles organizācijas hierarhijas ierobežojumi. Kad Sems izveido pirkšanas pieprasījumu, sistēmai ir jānosaka, kurus ierobežojumus izmantot. Sistēmas administrators iestata pirkšanas ierobežojumu parametrus, lai norādītu, ka pirkšanas ierobežojumi jāpielieto šādā prioritāšu secībā:

1.  Globāla pirkšanas kontrole
2.  Nodaļa
3.  Uzņēmumi

Tāpēc ierobežojumus 456 piemēro pirkšanas pieprasījumam, ka Sems izveido, un pirkšanas pieprasījumam nav nepieciešams minimālais pasūtījuma daudzums.

## <a name="policy-rules"></a>Ierobežojuma nosacījumi
### <a name="catalog-policy-rule"></a>Kataloga ierobežojuma nosacījumi

Kataloga ierobežojuma nosacījumi nosaka, kuru Sagādes katalogu lietotāji redz, kad viņi izveido pirkšanas pieprasījumus. Ja lietotājam ir piešķirta atļauja pasūtīt preces cita lietotāja vārdā, pieprasījums izmanto kataloga ierobežojuma nosacījumus, kas definēti pieprasītāja juridiskajai personai un pārvaldības struktūrvienībai, lai noteiktu, kuru katalogu rādīt. Pirms varat definēt kataloga ierobežojuma nosacījumus, ir jāizveido un jāpublicē sagādes katalogs.

### <a name="category-access-policy-rule"></a>Kategorijas piekļuves ierobežojuma nosacījumi

Kategorijas piekļuves ierobežojuma nosacījumi nosaka, kurām kategorijām lietotājiem ir piekļuve, kad tiek izveidoti pirkšanas pieprasījumi. Ja nav norādīts neviens nosacījums, pirkšanas pieprasījumam var pievienot sagādes kategorijas.

1.  Atlasiet opciju **Iekļaut mātes uzņēmuma kārtulu**, lai mātes organizācijai izmantotu kategorijas piekļuves ierobežojuma nosacījumu.
2.  Rūtī **Pieejamās kategorijas** atlasiet kategorijas, uz kurām attiecas šis nosacījums. Kad atlasāt kādu kategoriju, visas hierarhijā augstāk esošās kategorijas arī tiek pievienotas sarakstam **Atlasītās kategorijas**.
3.  Atlasiet opciju **Iekļaut apakškategorijas**, lai lietotu nosacījumu visām atlasītās kategorijas apakškategorijām.

### <a name="category-policy-rule"></a>Kategorijas ierobežojuma nosacījumi

Kategorijas ierobežojuma nosacījumi definē, kā lietotāji var atlasīt kreditorus katrai kategorijai. Tie arī definē prasības saņemšanas un rēķina izrakstīšanas procesiem.

### <a name="re-approval-rule-for-purchase-orders"></a>Atkārtotas apstiprināšanas kārtula pirkšanas pasūtījumiem

Atkārtotas apstiprināšanas kārtula ir neobligāts nosacījums, kas nosaka kritērijus, kad mainoties pirkšanas pasūtījumam ir nepieciešams atkārtots apstiprinājums. Atlasītie lauki tiek izvērtēti pirkšanas pasūtījumā darbplūsmā, kad darbplūsmā ir iestatīts noteikums “Nepieciešama pirkšanas pasūtījuma atkārtota apstiprināšana”.

> [!NOTE]
> Mainot apstiprinātu pirkšanas pasūtījumu, kuram ir iespējota izmaiņu pārvaldība, vienmēr tiek atiestatīta uzskaites sadale. Tāpēc jums ir jāņem vērā, ka, ja vēlaties izvairīties no pirkšanas pasūtījuma atkārtotas apstiprināšanas pēc noteiktu lauku izmaiņām, atkārtotai apstiprināšanai nedrīkst atlasīt lauku Uzskaites sadale ir mainījusies. 

### <a name="purchase-requisition-rfq-rule"></a>Pirkšanas pieprasījuma PP nosacījumi

Pirkšanas pieprasījuma PP nosacījumi nosaka kritērijus, kuri ir nepieciešami piedāvājuma pieprasījumam (PP) pirkšanas pieprasījuma rindai. Ja rinda atbilst nosacījumiem, pieprasījuma rindā parādās "neoficiāls PP" vai "oficiāls PP".

### <a name="purchase-requisition-control-rule"></a>Piedāvājuma pieprasījuma kontroles nosacījumi

Pirkšanas pieprasījuma kontroles nosacījumi ir neobligāts noteikums. Izveidojot šī tipa nosacījumus, varat iestatīt opcijas dažādās cilnēs:

-   Cilnē **Darbplūsmas iesniegšana** varat konfigurēt laukus, kas ir jāaizpilda pieprasījuma rindā, lai pieprasījums tiktu iesniegts apstiprināšanai, kad pieprasījuma mērķis ir **Patēriņš**.
-   Cilnē **Pasūtījuma daudzumi** var konfigurēt laukus, kas nepieciešami pirkšanas pieprasījumā saskaņā ar noteiktiem nosacījumiem. Var arī ieviest pasūtījuma daudzumus.
-   Cilnē **Datumi** var konfigurēt, vai uzskaites datums ir tāds pats kā pieprasītais datums
-   Cilnē **Adrese** var definēt, vai lietotājam ir atļauts izveidot jaunas adreses sistēmā, lai tās piemērotu pirkšanas pieprasījumam.

### <a name="requisition-purpose-rule"></a>Pieprasījuma mērķa nosacījumi

Pieprasījuma mērķa nosacījumi ir neobligāts noteikums, kas nosaka pieprasījuma mērķa tipu, kas atļauts konkrētai juridiskai personai. Ja šajos nosacījumos nav norādīts cits nolūks, izveides laikā pieprasījumu mērķis automātiski ir **Patēriņš**.

### <a name="replenishment-category-access-policy-rule"></a>Papildināšanas kategorijas piekļuves ierobežojuma nosacījumi

Papildināšanas kategorijas piekļuves ierobežojuma nosacījumi ir neobligāts noteikums, kas nosaka preces, kas ir pieejamas, lai apmierinātu pieprasījuma pieprasījumu pēc konkrētas juridiskas personas, kad pieprasījuma mērķis ir **Papildināšana**.

### <a name="replenishment-control-rule"></a>Papildināšanas kontroles nosacījumi

Papildināšanas kontroles nosacījumi ir neobligāts noteikums, kas nosaka laukus, kas ir jāaizpilda pieprasījuma rindā, lai pieprasījums tiktu iesniegts apstiprināšanai, kad pieprasījuma mērķis ir **Papildināšana**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Pirkšanas pasūtījuma izveidošana un pieprasījuma konsolidācijas nosacījums

Izmantojot pirkšanas pasūtījuma izveides un pieprasījuma konsolidācijas nosacījumu, tiek definēti ierobežojuma nosacījumus, kas ir jāizmanto, kad pirkšanas pasūtījums tiek ģenerēts no apstiprināta pirkšanas pieprasījuma. Izveidojot šī tipa nosacījumus, varat iestatīt opcijas dažādās cilnēs:

-   Cilnē **Pirkšanas pasūtījuma sadalījums** iespējams definēt kritērijus pirkšanas pieprasījuma rindu sadalīšanai atsevišķos pirkšanas pasūtījumos.
-   Cilnē **Cenu/atlaižu pārsūtīšana** var definēt, kad pārrēķināt cenu līgumu, kad pirkšanas pasūtījums ir izveidots:
    -   **Tikai tad, ja nav tirdzniecības līguma** — cenas un atlaides tiek pārsūtītas no pirkšanas pieprasījuma tikai tad, ja nav piemērojama tirdzniecības līguma vai pamatcenas. Ja krājumam vai kreditoram pastāv tirdzniecības līgums vai pamatcena, cenas un atlaides tiek pārrēķinātas, pamatojoties uz tirdzniecības līgumu vai pamatcenu, un tiek lietotas pirkšanas pasūtījumam. Ja vien nav norādīts citādi, šī ir noklusējuma darbība.
    -   **Vienmēr** — cenas un atlaides vienmēr tiek pārsūtītas no pirkšanas pieprasījuma.

    Varat arī ļaut pieprasītājam mainīt cenu un atlaižu pārsūtīšanas metodi atsevišķām pirkšanas pieprasījuma rindām, neskatoties uz cenu/atlaižu pārsūtīšanas kārtulu, kas ir definēta. Atlasiet opciju **Ļaut manuāli ignorēt pēc pirkšanas pieprasījuma rindas**, ja vēlaties iespējot šo iespēju.
-   Cilnē **Krājuma apraksta pārsūtīšana** var pārsūtīt krājuma aprakstu no pieprasījuma, ja tas tiek izveidots no PP.
-   Cilnē **Cenu tolerance** var noteikt nosacījumus, kas tiek izmantoti, lai maršrutētu apstiprinātos pirkšanas pieprasījumus atpakaļ uz pārskatīšanas procesu, kad sagādes kataloga krājuma cena pieaug. Iestatiet maksimālo summu, līdz kurai neto summa par rindas krājumu pirkšanas pasūtījumā var palielināties laikā starp pirkšanas pieprasījuma apstiprināšanu un brīdi, kad tiek izveidots pirkšanas pasūtījums. Neto summa tiek aprēķināta, izmantojot šādu formulu: (\[daudzums × (vienības cena – atlaide) ÷ cenas vienība\] + pirkšanas papildmaksas) × (100 – atlaids procentos) ÷ 100. Pirkšanas pieprasījuma rindas, kas pārsniedz iestatīto cenas toleranci, tiek aizturētas manuālai apstrādei. Kārtulas, kuras jūs konfigurējat cilnē **Kļūdu apstrāde**, nosaka, kā tiek apstrādātas pirkšanas pieprasījuma rindas.
-   Cilnē **Kļūdu apstrāde** var konfigurēt apstrādes kārtulu, kas tiek piemērota pirkšanas pasūtījumam, ja piegādātāja kļūdas vai cenu tolerances kļūdas dēļ tās validācija neizdodas pirkšanas pasūtījuma izveidošanas laikā. Izvēlieties vienu no šīm opcijām:
    -   **Nav darbības** — pirkšanas pieprasījuma rindas paliek lapā **Nodot izpildei apstiprinātos pirkšanas pieprasījumus**. Pirkšanas pieprasījuma rindu statuss paliek **Apstiprināts**. Tomēr kļūdas jānovērš, pirms pirkšanas pasūtījumu var ģenerēt no pirkšanas pieprasījuma rindām.
    -   **Atcelt pirkšanas pieprasījuma rindu** — pirkšanas pieprasījumu rindas tiek atceltas. Pieprasītājs var izveidot jaunu pirkšanas pieprasījumu par atceltajām rindām, ja viņš vai viņa joprojām vēlas pieprasīt rindas krājumus.
    -   **Izveidot jaunu pirkšanas pieprasījuma rindu** — pirkšanas pieprasījumu rindas tiek atceltas. Pēc tam tiek ģenerēti jauni pirkšanas pieprasījumi, kas satur tikai pirkšanas pieprasījumu rindas, kuru validācija neizdevās. Jaunu ģenerējamo pirkšanas pieprasījumu statuss ir **Melnraksts**. Šos pirkšanas pieprasījumus var no jauna iesniegt izskatīšanai pēc tam, kad validācijas kļūdas ir novērstas. Pirkšanas pieprasījuma rindu sagatavotājs tiek informēts, ka rindas tika atceltas un ka jaunie pirkšanas pieprasījumi tika ģenerēti no pirkšanas pieprasījuma rindām, kuras neizdevās.
-   Cilnē **Manuāla pirkšanas pasūtījuma izveide** definējiet parametrus, kas nosaka, vai pirkšanas pieprasījums ir manuāli jāapstrādā vai tas var automātiski tikt pārvērsts par pirkšanas pasūtījumu. Parametru var lietot iekšējā kataloga krājumiem, ārējā kataloga krājumiem vai krājumiem, kas nav katalogā. Izvēlieties vienu no šīm opcijām:
    -   **Manuāli izveidot pirkšanas pasūtījumus** — manuāli izveidojiet pirkšanas pasūtījumus visiem pirkšanas pieprasījumiem.
    -   **Automātiski izveidot pirkšanas pasūtījumus** — automātiski izveidojiet pirkšanas pasūtījumus visiem apstiprinātajiem pirkšanas pieprasījumiem. Neviens pirkšanas pieprasījums nav aizturēts manuālai pirkšanas pasūtījuma izveidei.
    -   **Automātiski izveidot pirkšanas pasūtījumus, izņemot norādītajos apstākļos** — manuāli izveidot pirkšanas pasūtījumus pirkšanas pieprasījumiem, kas atbilst definētajiem kritērijiem. Visi citi pirkšanas pieprasījumi, kas ir apstiprināti automātiski, tiek pārvērsti par pirkšanas pasūtījumiem. Ja atlasāt **Automātiski izveidot pirkšanas pasūtījumus, izņemot norādītajos apstākļos**, jūs varat pievienot sagādes kategorijas un kreditorus, lai precizētu, kuras apstiprinātās pirkšanas pieprasījuma rindas tiek aizturētas manuālai apstrādei. Šo opciju var lietot iekšējā kataloga krājumiem, ārējā kataloga krājumiem un krājumiem, kas nav katalogā. Atlasot sagādes kategoriju, tiek atlasītas arī visas apakškategorijas šajā sagādes kategorijā. Atlasiet opciju **Visas** noteiktam pirkšanas pieprasījuma rindas tipam, lai aizturētu visas šī tipa rindas manuālai apstrādei.

    Ja vēlaties pirkšanas pasūtījumus automātiski ģenerēt no apstiprinātajiem pirkšanas pieprasījumiem, kad tiek palaists pakešuzdevums pirkšanas pasūtījuma ģenerēšanai, atlasiet opciju **Izpildīt automātisku pirkšanas pasūtījuma izveidi kā pakešuzdevumu**. Šī opcija attiecas tikai uz tiem pirkšanas pieprasījumiem, kam nav nepieciešama manuāla apstrāde. Palaižot automātisko pirkšanas pasūtījuma ģenerēšanu kā pakešuzdevumu, varat ieplānot šo darbību brīdī, kad resursi ir mazāk ierobežoti. Ja pirkšanas pieprasījuma rindās ir atlasīta opcija **Jāveic priekšapmaksa**, atlasiet opciju **Ja pieprasījums ir iestatīts priekšapmaksai**, ja vēlaties aizturēt apstiprinātos pirkšanas pieprasījumus manuālai apstrādei. Pirkšanas pieprasījumus, kas ir aizturēti manuālai apstrādei, var filtrēt tā, lai varētu skatīt tikai tās pirkšanas pieprasījumu rindas, kurām nepieciešama priekšapmaksa.
-   Cilnē **Pieprasījuma konsolidācija** var definēt parametrus, kas nosaka, vai pirkšanas pieprasījumi, ko apstrādā manuāli, var tikt izmantoti pirkšanas pieprasījuma konsolidācijai. Parametru var lietot iekšējā kataloga krājumiem, ārējā kataloga krājumiem vai krājumiem, kas nav katalogā. Izvēlieties vienu no šīm opcijām:
    -   **Neatļaut pieprasījuma konsolidāciju** — apstiprinātās pirkšanas pieprasījuma rindas nav piemērotas pieprasījuma konsolidācijai. Šī opcija ir atlasīta pēc noklusējuma un attiecas tikai uz pirkšanas pieprasījuma rindām, kurām nepieciešama manuāla apstrāde pirkšanas pasūtījuma izveidošanai.
    -   **Vienmēr atļaut pieprasījuma konsolidāciju** — visas apstiprinātās pirkšanas pieprasījuma rindas ir piemērotas pieprasījuma konsolidācijai. **Piezīme:** atlasot opciju **Vienmēr atļaut pieprasījuma konsolidāciju** cilnē **Pieprasījuma konsolidācija** un atlasot opciju **Automātiski izveidot pirkšanas pasūtījumus** cilnē **Manuāla pirkšanas pasūtījuma izveide**, visi pirkšanas pieprasījumi tiek aizturēti manuālai apstrādei.
    -   **Atļaut pieprasījuma konsolidāciju norādītajos apstākļos** — definējiet kritērijus, kas nosaka, vai apstiprinātās pirkšanas pieprasījuma rindas ir piemērotas pieprasījuma konsolidācijai. Katram pirkšanas pieprasījuma rindas veidam varat iestatīt kritērijus pēc sagādes kategorijas un piegādātāja. Ja atlasāt opciju **Atļaut pieprasījuma konsolidāciju norādītajos apstākļos**, varat iestatīt kritērijus pēc sagādes kategorijas un kreditora katram pirkšanas pieprasījuma rindas tipam. Atlasot sagādes kategoriju, tiek atlasītas arī visas apakškategorijas šajā sagādes kategorijā. Ja atlasāt opciju **Visas** noteiktam rindas tipam, visas šī tipa pirkšanas pieprasījuma rindas ir piemērotas pieprasījuma konsolidācijai.





