---
title: Izejošo krājumu operācija punktā POS
description: Šajā tēmā ir aprakstītas pārdošanas punkta (POS) izejošo krājumu operāciju iespējas.
author: hhaines
manager: annbe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c3e50d20162340c599fb6719ae6f45654dba990a
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071879"
---
# <a name="outbound-inventory-operation-in-pos"></a>Izejošo krājumu operācija punktā POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce versijā 10.0.10 un jaunākās versijā ienākošās un izejošās operācijas pārdošanas punktā (POS) aizvieto izdošanas un saņemšanas operāciju.

> [!NOTE]
> Versijā 10.0.10 un jaunākās versijās visus jaunos līdzekļus POS lietojumprogrammā, kas ir saistīti ar veikala krājumu saņemšanu no pirkšanas pasūtījumiem un pārsūtīšanas pasūtījumiem, pievienos POS ienākošajai operācijai. Ja jūs pašlaik izmantojat izdošanas un saņemšanas operāciju POS, mēs iesakām jums izstrādāt stratēģiju, lai pārietu no šīs operācijas uz jaunajām ienākošajām un izejošajām operācijām. Lai gan izdošanas un saņemšanas operācija netiks noņemta no preces, vairs netiks veiktas investīcijas no funkcionālās vai veiktspējas perspektīvas pēc versijas 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Priekšnosacījums: Konfigurējiet asinhrono dokumentu struktūru

Izejošā operācija iekļauj veiktspējas uzlabojumus, lai nodrošinātu, ka lietotāji, kuriem ir augsts saņemšanas grāmatojumu apjoms daudzos veikalos vai uzņēmumos un kam ir daudz krājumu dokumentu, var apstrādāt šos dokumentus Commerce Headquarters, nepieredzot taimautus vai kļūmes. Šie uzlabojumi prasa asinhronas dokumentu struktūras izmantošanu.

Izmantojot asinhrono dokumenta struktūru, jūs varat veikt izejošo dokumentu izmaiņas no POS uz Commerce Headquarters un pēc tam pāriet uz citiem uzdevumiem, kamēr notiek fonā notiek apstrāde uz Commerce Headquarters. Lai pārliecinātos, ka grāmatošana bijusi veiksmīga, varat pārbaudīt dokumenta statusu POS dokumentu saraksta lapā **Izejošās operācijas**. POS programmā var arī izmantot izejošo operāciju aktīvo dokumentu sarakstu, lai skatītu visus dokumentus, kurus nevarēja grāmatot Commerce Headquarters. Ja dokuments neizdodas, POS lietotāji var veikt labojumus un pēc tam vēlreiz mēģināt apstrādāt to programmā Commerce Headquarters.

> [!IMPORTANT]
> Pirms uzņēmums mēģina izmantot izejošo operāciju POS, ir jābūt konfigurētai asinhronā dokumenta struktūrai.

Lai konfigurētu asinhronu dokumentu struktūru, veiciet šādas procedūras.

### <a name="create-and-configure-a-number-sequence"></a>Izveidojiet un konfigurējiet numuru sēriju

1. Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Numuru sērijas**.
2. Lapā **Numuru sērijas** izveidojiet numuru sēriju.
3. Laukā **Numuru sērijas kods** un **Nosaukums** ievadiet lietotāja definētās vērtības.
4. Kopsavilkuma cilnē **Atsauces** atlasiet **Pievienot**.
5. Laukā **Apgabals** atlasiet **Commerce parametri**.
6. Laukā **Atsauce** atlasiet **Retail dokumenta operācijas identifikators**.
7. Kopsavilkuma cilnē **Vispārīgi**, sadaļā **Iestatīšana** iestatiet opciju **Nepārtrauki** uz **Nē**, lai nodrošinātu, ka nav veiktspējas problēmu.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Izveidojiet un ieplānojiet divus pakešdarbus dokumentu apstrādes un pārraudzības uzdevumiem

Jūsu izveidotie pakešuzdevumi tiks izmantoti, lai apstrādātu dokumentus, kuriem ir radusies kļūme vai taimauts. Tie tiks izmantoti arī tad, kad aktīvo krājumu dokumentu skaits, kas tiek apstrādāti no POS, pārsniedz sistēmas konfigurēto vērtību.

1. Dodieties uz **Sistēmas administrēšana \> Vaicājumi \> Pakešuzdevumi**.
2. Lapā **Pakešuzdevums** izveidojiet divus pakešuzdevumus:

    - Konfigurējiet vienu darbu, lai tas palaistu klasi **RetailDocumentOperationMonitorBatch**.
    - Konfigurējiet citu darbu, lai tas palaistu klasi **RetailDocumentOperationProcessingBatch**.

3. Ieplānojiet jauno pakešuzdevumu periodisku palaišanu. Piemēram, iestatiet grafiku tā, lai darbi tiktu izpildīti ik pēc piecām minūtēm.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Priekšnoteikums: Pievienojiet izejošo operāciju POS ekrāna izkārtojumam

Lai jūsu organizācija varētu izmantot izejošo operāciju funkcionalitāti, tai ir jākonfigurē POS operācija **Izejošā operācija** vienā vai vairākos [POS ekrāna izkārtojumos](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Pirms jaunās operācijas izvietošanas ražošanas vidē, pārliecinieties, vai ka to rūpīgi pārbaudāt un apmācāt savus lietotājus tās lietošanā.

## <a name="overview"></a>Pārskats

Izejošā operācija ļauj POS lietotājiem veikt šādus uzdevumus:

- Grāmatot sūtījumus pārsūtīšanas pasūtījuma dokumentiem gadījumos, kad lietotāja veikals ir norādītā izejošā noliktava.
- Skatiet informāciju par vēsturiskajiem pārsūtīšanas pasūtījumu sūtījumiem, kurus iegrāmatoja veikals.
- Izveidojiet jaunus izejošo pārsūtīšanas pasūtījumu pieprasījumus.

Kad no POS programmas tiek palaista izejošā operācija, parādās saraksta lapas skats. Šis skats parāda atvērtos pārsūtīšanas pasūtījuma dokumentus, kuros ir krājumu rindas, kuras pašreizējam veikalam ir paredzēts izsūtīt un izpildīt. Lai atrastu dokumenta atlasi, lietotāji var ritināt sarakstu vai izmantot meklēšanas līdzekli.

Izejošo krājumu dokumentu sarakstam ir trīs cilnes.

- **Aktīvs** – Šī cilne parāda pārsūtīšanas pasūtījumus, kuru statuss ir **Pieprasīts** vai **Daļēji nosūtīts**. Pasūtījumi satur rindas vai daudzumus rindās, kas ir jānosūta lietotāja pašreizējam veikalam. Šajā cilnē tiek rādīti arī pasūtījumi, kuru statuss ir **Apstrāde HQ** (tas ir, tie gaida apstiprinājumu veiksmīgai grāmatošanai no Commerce Headquarters) vai **Apstrāde neizdevās** (tas ir, grāmatošana Commerce Headquarters bija neveiksmīga, un lietotājam ir jālabo dati un jāmēģina vēlreiz iesniegt pasūtījumus).
- **Melnraksts** – Šī cilne parāda jaunos izejošo pārsūtīšanas pasūtījumu pieprasījumus, kurus izveidoja lietotāja veikals. Tomēr dokumenti tika saglabāti tikai lokāli. Tie vēl nav iesniegti Commerce Headquarters apstrādei.
- **Pabeigts** – Šī cilne parāda pārsūtīšanas pasūtījuma dokumentu sarakstu, ko veikals ir pilnībā nosūtījis pēdējo septiņu dienu laikā. Šī cilne ir paredzēta tikai informatīviem nolūkiem. Visa informācija par dokumentiem šim veikalam ir tikai lasāmi dati.

Skatot dokumentus jebkurā cilnē, lauks **Statuss** var palīdzēt izprast stadiju, kurā dokuments atrodas.

- **Melnraksts** — Pārsūtīšanas pasūtījuma dokuments ir saglabāts tikai veikala kanāla datu bāzē. Informācija par pārsūtīšanas pasūtījuma pieprasījumu vēl nav iesniegta Commerce Headquarters.
- **Pieprasīts** – Pirkšanas pasūtījums vai pārsūtīšanas pasūtījums ir izveidots Commerce Headquarters un ir pilnībā atvērts. Lietotāja pašreizējais veikals vēl nav apstrādājis nevienu sūtījumu attiecībā pret dokumentu.
- **Daļēji nosūtīts** – Pārsūtīšanas pasūtījuma dokumentam ir viena vai vairākas rindas vai daļēji rindu daudzumi, kas iegrāmatoti kā nosūtīti no izejošās noliktavas. Šīs nosūtītās rindas ir pieejamas saņemšanai, izmantojot ienākošo operāciju.
- **Pilnībā nosūtīts** — Pārsūtīšanas pasūtījumam ir bijušas visas tās rindas un pilnie rindas daudzumi, kurus izejošā noliktava grāmatojusi kā nosūtītus.
- **Notiek** – Šis statuss tiek izmantots, lai informētu ierīces lietotājus, ka dokumentu aktīvi apstrādā cits lietotājs.
- **Apturēts** — Šis statuss tiek parādīts pēc tam, kad tiek atlasīts **Apturēt saņemšanu**, lai īslaicīgi apturētu saņemšanas procesu.
- **Apstrāde HQ** — Dokuments tika iesniegts Commerce Headquarters no POS programmas, taču tas vēl nav veiksmīgi iegrāmatots programmā Commerce Headquarters. Dokumentam tiek veikta asinhronās dokumenta grāmatošana. Pēc tam, kad dokuments ir sekmīgi iegrāmatots Commerce Headquarters, tā statuss ir jāatjaunina, lai tas būtu **Pilnībā saņemts** vai **Daļēji saņemts**.
- **Apstrāde neizdevās** – Dokuments tika iegrāmatots Commerce Headquarters un noraidīts. Rūts **Detalizēta informācija** rāda grāmatošanas kļūmes iemeslu. Dokuments ir jārediģē, lai izlabotu datu problēmas, un pēc tam tas atkārtoti jāiesniedz Commerce Headquarters apstrādei.

Kad sarakstā atlasāt dokumenta rindu, parādās rūts **Detalizēta informācija**. Šajā rūtī tiek rādīta papildu informācija par dokumentu, piemēram, informācija par nosūtīšanu un datumu. Progresa josla rāda, cik daudz vienumu vēl ir jāapstrādā. Ja dokuments nav veiksmīgi apstrādāts programmā Commerce Headquarters, rūts **Detalizēta informācija** rāda kļūmes ziņojumus, kas ir saistīti ar kļūmi.

Dokumentu saraksta lapas skatā varat izvēlēties **Pasūtījuma informāciju** programmas joslā, lai skatītu detalizētu informāciju par dokumentu. Varat arī aktivizēt saņemšanas apstrādi atbilstošajās dokumenta rindās.

Dokumentu saraksta lapas skatā varat izveidot arī jaunu izejošo pārsūtīšanas pasūtījumu veikalam.

## <a name="transfer-order-shipping-process"></a>Pasūtījuma nosūtīšanas pārsūtīšanas process

Pēc pārsūtīšanas pasūtījuma dokumenta atlases cilnē **Aktīvs** varat atlasīt **Pasūtījuma informācija**, lai sāktu izpildes procesu. Tiek parādīts skats **Pilns pasūtījumu saraksts**. Šajā lapā parādītas visas dokumenta rindas, kas satur vienumu. Tas arī rāda detalizētu informāciju par pasūtīto daudzumu.

Katra svītrkoda skenēšana atjaunina daudzumu, kas atrodas laukā **Nosūta tagad** par vienu vienību. Varat arī ievadīt nosūtīšanas daudzumu, atlasot **Nosūtīt preci** programmas joslā, ievadot krājuma ID un pēc tam ievadot daudzumu. Ja vienums tiek kontrolēts ar atrašanās vietu, varat apstiprināt vai iestatīt dokumenta rindas nosūtīšanas vietu.

Skatā **Pilns pasūtījumu saraksts** varat manuāli atlasīt rindu sarakstā un tad atjaunināt daudzumu **Nosūta tagad** atlasītajai rindai rūtī **Detalizēta informācija**.

### <a name="over-delivery-shipping-validations"></a>Pasūtījuma apjoma pārsniegšanas nosūtīšanas validācijas

Validācijas notiek dokumenta rindu saņemšanas procesā. Tās ietver validācijas pasūtījuma apjoma pārsniegšanai. Ja lietotājs mēģina saņemt vairāk krājumu, nekā bija pasūtīts uz pirkšanas pasūtījumu, bet vai nu nav konfigurēta pasūtījuma apjoma pārsniegšana, vai saņemtais daudzums pārsniedz pirkšanas pasūtījuma rindai konfigurēto pasūtījuma apjoma pārsniegšanas toleranci, lietotājs saņem kļūdu, un lietotājam nav atļauts saņemt pārsniegto daudzumu.

### <a name="shipping-location-controlled-items"></a>Nosūtīšanas vieta — kontrolētie vienumi

Ja nosūtītie krājumi tiek kontrolēti ar atrašanās vietu, lietotāji var izvēlēties vietu, no kuras tie vēlas izsniegt krājumus nosūtīšanas procesa laikā. Ieteicams konfigurēt noklusēto izejas plūsmas atrašanās vietu veikala noliktavai, lai padarītu šo procesu efektīvāku. Pat ja noklusējuma atrašanās vieta ir konfigurēta, lietotāji var pēc vajadzības ignorēt izejas plūsmas vietu atlasītās rindās.

Operācija ievēro konfigurāciju **Tukšā kvīts atļauta** noliktavas dimensijā **Atrašanās vieta** un neprasa ievadīt atrašanās vietas dimensiju, ja ir konfigurēta tukša saņemšanas vieta. Ja krājumam nav atļautas tukšas saņemšanas vietas, POS programmā tiek rādīta kļūda, un ir jāieraksta vieta, pirms saņemšanu var grāmatot.

### <a name="ship-all"></a>Nosūtīt visu

Pēc nepieciešamības varat atlasīt **Nosūtīt visu**programmas joslā, lai ātri atjauninātu daudzumu **Nosūta tagad** visām dokumenta rindām uz maksimālo vērtību, kas ir pieejama izpildei šīm rindām.

### <a name="cancel-fulfillment"></a>Atcelt izpildi

Jums vajadzētu izmantot funkciju **Atcelt izpildi** programmas joslā vienīgi tad, ja vēlaties iziet no dokumenta un nevēlaties saglabāt izmaiņas. Piemēram, jūs sākotnēji atlasījāt nepareizu dokumentu un nevēlaties saglabāt nevienu no iepriekšējiem nosūtīšanas datiem.

### <a name="pause-fulfillment"></a>Pauzēt izpildi

Ja jūs izpildīsiet pārsūtīšanas pasūtījumu, varat izmantot funkciju **Apturēt izpildi**, ja vēlaties procesa pārtraukumu. Piemēram, jūs varētu vēlēties veikt citu operāciju no POS, piemēram, zvanīt klientu pārdošanas daļai vai aizkavēt sūtījuma grāmatošanu Commerce Headquarters.

Kad atlasāt **Apturēt izpildi**, dokumenta statuss tiek mainīts uz **Apturēts**. Tāpēc lietotājs zinās, ka dokumentā ir ievadīti dati, bet dokuments vēl nav iesniegts. Kad esat gatavs atsākt izpildes procesu, atlasiet apturēto dokumentu un pēc tam atlasiet **Pasūtījuma informācija**. Jebkādi **Nosūta tagad** daudzumi, kurus iepriekš saglabāja, tiks aizturēti un būs skatāmi skatā **Pilns pasūtījumu saraksts**.

### <a name="finish-fulfillment"></a>Pabeigt izpildi

Pēc tam, kad esat pabeidzis ievadīt visus **Nosūta tagad** daudzumus produktiem, ir programmas joslā jāatlasa **Pabeigt izpildi**.

Kad tiek izmantota asinhronā dokumenta apstrāde, kvīts tiek iesniegta, izmantojot asinhronu dokumenta struktūru. Laiks, kas nepieciešams, lai dokuments tiktu grāmatots, ir atkarīgs no dokumenta izmēra (rindu skaita) un vispārējās apstrādes satiksmes, kas notiek serverī. Parasti šis process notiek dažu sekunžu laikā. Ja dokumenta grāmatošana neizdodas, lietotājam tiek paziņots, izmantojot dokumentu sarakstu **Izejošā operācija** cilnē **Aktīvs**, kur dokumenta statuss tiks atjaunināts uz **Apstrādes kļūme**. Lietotājs var atlasīt neizdevušos dokumentu POS, lai skatītu kļūdu ziņojumus un kļūmes iemeslu rūtī **Detalizēta informācija**. Neizdevies dokuments paliek negrāmatots, un ir nepieciešams, ka lietotājs atgriežas pie dokumenta rindām, POS atlasot **Pasūtījuma informācija**. Pēc tam lietotājam ir jāatjaunina dokuments ar labojumiem, pamatojoties uz kļūdām. Pēc dokumenta izlabošanas lietotājs var vēlreiz mēģināt apstrādāt to, atlasot **Pabeigt izpildi** programmu joslā.

## <a name="create-an-outbound-transfer-order"></a>Izveidojiet izejošās pārsūtīšanas pasūtījumu

No POS lietotāji var izveidot jaunus pārsūtīšanas pasūtījumu dokumentus. Lai sāktu procesu, programmas joslā atlasiet **Jauns**, kad atrodaties galvenajā dokumentu sarakstā **Izejošā operācija**. Pēc tam tiek parādīta uzvedne, lai atlasītu noliktavu vai veikalu **Pārsūtīt uz**, uz kuru jūsu pašreizējais veikals nosūtīs krājumus. Vērtības tiek ierobežotas līdz atlasei, kas definēta veikala izpildes grupas konfigurācijā. Izejošās pārsūtīšanas pieprasījumā jūsu pašreizējais veikals vienmēr būs noliktava **Pārsūtīšana no** pārsūtīšanas pasūtījumam. Šo vērtību nevar mainīt.

Pēc vajadzības varat ievadīt vērtības laukos **Nosūtīšanas datums**, **Saņemšanas datums** un **Piegādes veids**. Varat arī pievienot piezīmi, kas tiks uzglabāta kopā ar pārsūtīšanas pasūtījuma galveni, kā pielikumu dokumentam Commerce Headquarters.

Pēc kājenes informācijas izveides varat pievienot preces pārsūtīšanas pasūtījumam. Lai sāktu vienumu un pieprasīto daudzumu pievienošanu, pārbaudiet svītrkodus vai atlasiet **Pievienot preci**.

Kad izejošā pārsūtījuma pasūtījumā ir ievadītas rindas, jāatlasa **Saglabāt**, lai saglabātu dokumenta izmaiņas lokāli, vai **Iesniegt pieprasījumu**, lai iesniegtu pasūtījuma informāciju Commerce Headquarters turpmākai apstrādei. Ja atlasāt **Saglabāt**, melnraksta dokuments tiek saglabāts kanāla datu bāzē, un izejošā noliktava nevar palaist dokumentu, kamēr tas nav veiksmīgi apstrādāts, izmantojot **Iesniegt pieprasījumu**. Izvēlieties **Saglabāt** tikai tad, ja neesat gatavs iesniegt pieprasījumu Commerce Headquarters apstrādei.

Ja dokuments ir saglabāts lokāli, to var atrast cilnē **Melnraksti** dokumentu sarakstā **Ienākošā operācija**. Kamēr dokumenta statuss ir **Melnraksts**, jūs varat to rediģēt, atlasot **Rediģēt**. Jūs variet atjaunināt, pievienot vai dzēst rindas pēc nepieciešamības. Varat arī dzēst visu dokumentu, kamēr tā statuss ir **Melnraksts**, atlasot **Dzēst** cilnē **Melnraksti**.

Pēc tam, kad melnraksta dokuments ir sekmīgi iesniegts Commerce Headquarters, tas cilnē **Aktīvs**, un tam ir statuss **Pieprasīts**. Pašlaik tikai lietotāji, kas atrodas izejošajā noliktavā, var rediģēt dokumentu, POS programmā atlasot **Izejošā operācija**. Lietotāji ienākošajā noliktavā var skatīt pārsūtīšanas pasūtījumu cilnē **Aktīvs** no dokumentu saraksta **Ienākošā operācija**, taču viņi nevar rediģēt vai dzēst to. Rediģēšanas bloķēšana nodrošina, ka nav konfliktu, jo ienākošais pieprasītājs maina pārsūtīšanas pasūtījumu tajā pašā laikā, kad izejošais nosūtītājs aktīvi veic pasūtījumu izdošanu un nosūtīšanu. Ja pēc pārsūtīšanas pasūtījuma iesniegšanas ir pieprasītas izmaiņas no ienākošā veikala vai noliktavas, ir jākontaktējas ar nosūtītāju un jāievada izmaiņas.

Pēc tam, kad dokumentam ir statuss **Pieprasīts**, tas ir gatavs izpildes apstrādei, ko veic izejošā noliktava. Kad sūtījums tiek apstrādāts, izmantojot izejošo operāciju, pārsūtīšanas pasūtījuma dokumentu statuss tiek atjaunināts no **Pieprasīts** uz **Pilnībā nosūtīts** vai **Daļēji nosūtīts**. Pēc tam, kad dokumentiem ir statuss **Pilnībā nosūtīts** vai **Daļēji nosūtīts**, ienākošais veikals vai noliktava var grāmatot to kvītis, izmantojot ienākošās operācijas saņemšanas procesu.

Pilnībā nosūtītie pārsūtīšanas pasūtījumi tiek pārvietoti uz cilni **Pabeigts** dokumentu sarakstā **Izejošā operācija**. Tur tie septiņas dienas ir redzami lietotājiem izejošajā veikalā vai noliktavā, tikai lasīšanas režīmā.

## <a name="related-topics"></a>Saistītās tēmas

[Ienākošo krājumu operācija punktā POS](pos-inbound-inventory-operation.md)