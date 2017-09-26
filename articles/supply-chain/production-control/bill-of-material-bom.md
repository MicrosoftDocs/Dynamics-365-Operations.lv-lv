---
title: "Materiālu komplekti un formulas"
description: "Šajā rakstā ir sniegta informācija par materiālu komplektu (MK) un formulām, kuras veido preču un preču variantu definīcijas centrālo daļu. MK un formulas norāda konkrētas preces nepieciešamos materiālus jeb komponentus. Formulas norāda arī līdzproduktus un blakusproduktus, kas tiek saņemti noteiktā ražošanas kontekstā."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5a23acfa95bb93dbc5990bf3839bbc629f15cc2f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="bills-of-materials-and-formulas"></a>Materiālu komplekti un formulas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par materiālu komplektu (MK) un formulām, kuras veido preču un preču variantu definīcijas centrālo daļu. MK un formulas norāda konkrētas preces nepieciešamos materiālus jeb komponentus. Formulas norāda arī līdzproduktus un blakusproduktus, kas tiek saņemti noteiktā ražošanas kontekstā. 

<a name="bills-of-materials"></a>Materiālu komplekti
------------------

Materiālu komplekts (MK) nosaka komponentus, kas nepieciešami, lai saražotu preci. Komponenti var būt izejmateriāli, daļēji pabeigtas preces vai sastāvdaļas. Dažos gadījumos MK var norādīt pakalpojumus. Tomēr MK parasti raksturo nepieciešamos *materiālu resursus*.  

Ja tas ir apvienots ar maršrutu vai ražošanas plūsmu, kas apraksta operācijas un resursus, kuri nepieciešami, lai izveidotu preces, MK ir pamats preces novērtēto izmaksu aprēķināšanai.  

MK ir atsevišķs elements, kuru apraksta tālāk uzskaitītā informācija.:

-   MK ID
-   MK nosaukums
-   MK rindas, kas apraksta komponentus un sastāvdaļas
-   MK versijas, kas definē preci un periodu, kuram var izmantot MK

Viens MK apraksta vienu līmeni, kas tiek identificēts ar unikālu ID. Komponentiem var būt savi MK, kurus norāda MK versijas. Var parādīt un rediģēt visu MK hierarhiju noteiktai precei MK koka struktūras veidotājā.

### <a name="formulas-co-products-and-by-products"></a>Formulas, līdzprodukti un blakusprodukti

Formula ir MK apakštips, kas parasti tiek izmantots apstrādes ražošanai. Papildus komponentiem un sastāvdaļām formula apraksta līdzproduktus un blakusproduktus. Faktiskajā versijā formulas līdzproduktu un blakusproduktu definīcijai ir nepieciešama formulas versija. Formula parasti ir definēta vienai konkrētai pabeigtajai precei (formula vai plānošanas krājums), kas tiek definēta formulas versijā.

### <a name="boms-in-the-product-lifecycle"></a>MK preces dzīves ciklā

Preces dzīves ciklā dažādu iemeslu dēļ var tikt izveidoti daudzi MK veidi:

-   **Uzmetuma/projekta MK** — šis MK sniedz nepieciešamo materiālu novērtējuma melnrakstu projektēšanas sākumposmā un palīdz iegūt aptuvenu novērtējumu attiecībā uz izmaksām un novērtētajām preces īpašībām. Šis MK parasti netiek izmantots uzņēmuma resursu plānošanā (ERP).
-   **Konstruēšanas MK** — šis MK parasti tiek izmantots, projektējot preces, kas balstītas uz esošo preču portfeļiem. Konstruēšanas MK ir strukturēti, lai vienkāršotu projektēšanas procesu un grupētu kompleksas preces konstruēšanas moduļos. Vienkāršām precēm ir iespējami konstruēšanas MK faktiskajam ražošanas procesam. Tomēr citām precēm konstruēšanas MK ir jāpārveido par faktiskās ražošanas MK. MK hierarhijā konstruēšanas MK parasti attēlo fantomi. Lai arī konstruēšanas MK var izmantot ražošanas operāciju plānošanai un izpildei, šī pieeja var izraisīt efektivitātes samazināšanos, jo īpaši atkārtotām operācijām, ja tiek izveidoti daudzi pasūtījumi.
-   **Plānošanas MK** — šis MK tiek izmantots, lai veiktu plānošanu materiālu vajadzībām. Komponentu un sastāvdaļu pieprasījumu aprēķina, pamatojoties uz pabeigto preču pieprasījumu. Tāpat kā izmaksu aprēķināšanas MK, arī plānošanas MK var atspoguļot konkrētu materiālu sajaukumu, kas tiek izmantots periodā.
-   **Ražošanas MK** — tas ir faktiskais MK, kas tiek izmantots noteiktai ražošanai. Ražošanas MK ir jāņem vērā faktiskie resursi, kas tiek izmantoti produkta ražošanai. Veidojot ražošanas pasūtījumu, partijas pasūtījumu vai Kanban, vairāki MK līmeņi, kuri ir norādīti ar fantomiem, tiek sakļauti vienā līmenī un sadalīti pa operācijām attiecīgajam pasūtījumam.
-   **Izmaksu aprēķināšanas MK** — MK tiek izmantots, lai aprēķinātu preces novērtētās izmaksas. Piemēram, izmaksu aprēķināšanas MK var izmantot, ja tiek izmantotas standarta izmaksas vai tiek aprēķinātas noteiktas preces novērtētās plānotās izmaksas. Izmaksu aprēķināšanas MK var attiekties uz tādu konkrētu materiālu un resursu sajaukumu, kurus paredzēts izmantot. Tādējādi izmaksu aprēķināšanas MK var izmantot, lai izveidotu reprezentatīvas novērtētās izmaksas par periodu un palīdzētu izvairīties no novirzēm laika gaitā.

MK tipi, kuri tiek faktiski izmantoti ieviešanā, ir atkarīgi no ieviešanas, kā arī no uzņēmējdarbības scenārijiem un prasībām. Vienkāršas ieviešanas gadījumos plānošanas MK, ražošanas MK un izmaksu aprēķināšanas MK var modelēt kā vienu MK. Vidēs, kurās bieži notiek tehnoloģiskas izmaiņas un ir vairāki alternatīvi maršruti, visticamāk, būs nepieciešama lielāka MK veidu kopa.

### <a name="approval-of-boms-and-formulas"></a>MK apstiprināšana un formulas

Katru MK un formulu var atsevišķi apstiprināt vai neapstiprināt. Parasti, MK vai formulas apstiprināšana notiek, kad tiek apstiprināta pirmā atbilstošā MK versija. Tomēr dažos uzņēmējdarbības scenārijos šie apstiprinājumi var būt dažādas darbības procesa gaitā un var ietvert dažādus procesu īpašniekus.  

Ņemiet vērā, ka gadījumā, ja MK ir neapstiprināts, visas saistītās MK versijas arī ir neapstiprinātas.

## <a name="bom-and-formula-versions"></a>MK un formulas versijas
Lai noteiktu MK vai formulu saistītu ar preces variantu, ko var saražot, ir jāizveido MK versija vai formulas versija. MK versiju un formulas versiju derīgumu var ierobežot pēc perioda, daudzuma, vietas, noteiktām preces dimensijām un citiem kritērijiem. Formulas versijām ir papildu svarīgi atribūti, piemēram, ienesīgums, līdzproduktu un blakusproduktu definīcijas un izmaksu sadales norādījumi attiecīgajai formulai.

### <a name="approval-of-bom-and-formula-versions"></a>MK un formulas versiju apstiprināšana

Pirms MK versiju var izmantot plānošanā vai ražošanas procesā, tā ir jāapstiprina. Apstiprinot MK versiju, tiek apstiprināts arī saistītais MK atkarībā no lietotāja veiktās atlases un autentifikācijas tiesībām. Ņemiet vērā, ka MK versiju var apstiprināt tikai tad, ja ir apstiprināts saistītais MK.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Noklusējuma MK vai formulas versijas aktivizēšana

Lai iestatītu noteiktu MK vai formulu kā noklusējuma MK versiju vai formulas versiju, kas tiks izmantota vispārējai plānošanai vai izmantota, lai izveidotu ražošanas pasūtījumus, ir jāaktivizē attiecīgā versija. Kad tiek aktivizēta kāda versija, tiek verificēta šīs versijas unikalitāte attiecībā uz attiecīgajiem ierobežojumiem (piemēram, periodu, vietu vai daudzumu). Ja versijai, kuru mēģināt aktivizēt, ir konflikts ar jau aktīvo versiju, jūs saņemat kļūdas ziņojumu. Pēc tam ir jādeaktivizē konfliktējošā versija vai jāmodificē versijas ierobežojumi (parasti — periods), lai novērstu neviennozīmīgu aktivizēšanu.

### <a name="product-change-with-case-management"></a>Preces izmaiņas, izmantojot gadījumu pārvaldību

Preces izmaiņu gadījums jaunu vai mainītu MK vai MK versiju apstiprināšanai un aktivizēšanai nodrošina vienkāršu veidu, kā skatīt MK versiju ierobežojumu apskatu. Var arī apstiprināt un aktivizēt MK un formulas, kas ir saistītas ar noteiktām izmaiņām vienam aktivizēšanas datumam.

### <a name="alternative-bom-versions"></a>Alternatīvas MK versijas

Dažreiz aktīvo MK versiju vai formulas versiju nedrīkst izmantot prognozēm, pārdošanai vai pamata precei. Šajā gadījumā varat izvēlēties noteiktu apstiprinātu MK kā daļu no prasības (budžeta rinda, pārdošanas rinda vai MK rinda), ja alternatīvajam MK vai formulai pastāv apstiprināta MK versija vai formulas versija.  

Veidojot plānotos pasūtījumus, ražošanas pasūtījumus vai Kanban, plānotājs vai ražotnes vadītājs var izmantot apstiprinātu MK versiju, kas ir spēkā pieprasītajā plānotās ražošanas datumā, lai plānotu vai ražotu noteiktu preci. Izmantotajai MK versijai nav jābūt aktivizētai kā noklusējuma MK versijai.

## <a name="bom-and-formula-lines"></a>MK un formulas rindas
MK rinda tiek izveidota katram materiālam, pakalpojumam vai sastāvdaļai. Rinda nosaka norādītā preces varianta plānoto patēriņu un arī nosaka dažādus atribūtus, kas ir saistīti ar plānoto patēriņu.  

MK rindām var būt šādi rindu tipi: **Krājums**, **Fantoms**, **Pieprasīta piegāde**, **Kreditors**.

### <a name="item"></a>Krājums

Atlasiet rindas **Krājums** materiāliem vai pakalpojumiem, kuri tiek patērēti tieši un kuriem nav nepieciešama papildu izvēršana vai pieprasīta piegāde.

### <a name="phantom"></a>Fantoms

Atlasiet rindas tipu **Fantoms**, ja vēlaties izvērst jebkurus MK rindā esošus zemākā līmeņa MK krājumus. Vispārējā plānošanā, plānoto izmaksu aprēķinā vai tāda ražošanas pasūtījuma novērtēšanā, kuram tiek izmantotas MK rindas ar tipu **Fantoms**, pamata MK rinda, kas attiecas uz preces variantu, kuram ir fantoma MK, tiek aizstāta ar komponentu krājumiem, kas norādīti kā MK rindas attiecīgajā MK, saskaņā ar piemērojamo aktīvo MK versiju attiecīgajam preces variantam. Ja preces variantam ir piemērojams aktīvais maršruts, attiecīgā maršruta operācijas tiek sapludinātas pamata maršrutā.  

Ņemiet vērā, ka fantomi parasti tiek izmantoti, lai vienkāršotu tehnisko procesu. Fantoma MK plaša izmantošana daudzos līmeņos ietekmē veiktspēju, jo īpaši ļoti atkārtojošos ražošanas scenārijos. Lai uzlabotu veiktspēju, ir jāizvairās no fantomu hierarhijām ar daudziem līmeņiem. Tā vietā izmantojiet iepriekš izvērstus ražošanas MK un maršrutus.

### <a name="pegged-supply"></a>Pieprasīta piegāde

Atlasiet rindas tipu **Pieprasīta piegāde**, ja vēlaties izveidot pakārtoto ražošanas uzdevumu, MK rindas notikuma Kanban vai tiešu pirkšanas pasūtījumu visiem preces variantiem, uz kuriem ir atsauce MK rindā. Pakārtots ražošanas uzdevums, notikuma Kanban vai pirkšanas pasūtījums tiek izveidots, kad tiek novērtēts ražošanas pasūtījums. Nepieciešamie krājumu daudzumi tiek automātiski rezervēti patērēšanas ražošanas pasūtījumam.

### <a name="vendor"></a>Piegādātājs

Atlasiet rindas tipu **Kreditors**, ja ražošanas procesā tiek izmantots apakšuzņēmējs un vēlaties, lai apakšuzņēmējam tiktu automātiski izveidots pakārtots ražošanas uzdevums vai pirkuma pasūtījums.  

**Piezīme par apakšuzņēmēja operācijām MK.** Pakalpojums vai darbs, ko veic apakšuzņēmējs, jāizveido kā pakalpojumu krājums, kas tiek izsekots krājumos. Pakalpojumu krājums ir jāpievieno pamata krājumam kā MK rinda. Maršrutam jāsatur operācija, kas piešķirta apakšuzņēmēja operāciju resursiem.




