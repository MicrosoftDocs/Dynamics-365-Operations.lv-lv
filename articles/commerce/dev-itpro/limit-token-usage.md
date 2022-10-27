---
title: Ierobežot maksājuma marķiera izmantošanu
description: Šajā rakstā ir aprakstīta funkcija, kas ierobežo maksājumu marķieru lietošanu Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709375"
---
# <a name="limit-payment-token-usage"></a>Ierobežot maksājuma marķiera izmantošanu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīta funkcija, kas ierobežo maksājumu marķieru lietošanu Microsoft Dynamics 365 Commerce. Marķiera lietošana ir ierobežota pārdošanas pasūtījuma tvērumā vai, ja tiek piešķirta debitora atļauja, tā tiek saglabāta kā karte failā.

## <a name="key-terms"></a>Galvenie termini

| Termiņš | Apraksts |
|---|---|
| Marķieris | Xml BLOB, uz kuru ir atsauce Dynamics 365 sistēmā, kas glabā maksājuma atsauces darbību nolūkiem. |
| Karte failā | Saglabāts kartes atsauces marķieris, kas ir iepriekš saskaņots ar turpmāku izmantošanu Sistēmā Dynamics 365 vai maksājumu vārtejā un kas ir specifisks debitora kontam. |

Maksājuma marķiera lietošanas ierobežojumi attiecas uz jebkuru vidi, kas izmanto maksājumu vārtejas pakalpojumu, kurā tiek nodarbināti periodiski marķieri. [Sistēmas Dynamics 365 maksājumu savienotājs, kas atrodas ārpus lodziņa, izmanto](adyen-connector.md) periodisko maksājumu marķierus, lai veiktu sekojošās pasūtījuma darbības, piemēram, autorizācijas korekcijas un atkārtotas autorizācijas.

Lai palīdzētu kontrolēt, kā šie periodiskie maksājumu marķieri tiek izmantoti visā sistēmā, **ierobežot** maksājumu marķiera lietošanu līdz pasūtījuma konteksta funkcijai ierobežo periodisku marķieru izmantošanu pārdošanas pasūtījuma darbības jomu sistēmā. Kad šī funkcija ir iespējota, funkcija modificē Commerce Headquarters lietotāja interfeisu (UI), atjauninot maksājuma ievades lapas un ierobežojot iespēju atlasīt pagātnes debitora maksājumu atsauces lietošanai jaunās darbību instancēs.

Šī funkcija palīdz nodrošināt dažu maksājumu izsniedzēju, piemēram, Visa, lietošanas noteikumus. Visa pamata [noteikumos un Visa](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) preču un pakalpojumu noteikumos Visa norāda, ka maksājumu marķieru izmantošanu vajadzētu ierobežot ar darījuma darbības jomu, ja vien kartes īpašnieks nevienojas citādi.

Funkcija **Ierobežot maksājuma marķiera izmantošanu** pasūtījuma kontekstam ir svarīga tikai tad, ja izmantojat maksājumu vārtejas pakalpojumu, kas izmanto periodiska maksājuma marķiera atsauces.

## <a name="enable-the-feature"></a>Līdzekļa iespējošana

Lai iespējotu **maksājuma marķiera lietošanas ierobežojumu līdz pasūtījuma konteksta līdzeklim, Commerce Headquarters** **\> savā vidē dodieties uz darbalauku līdzekļu pārvaldību,** **atrodiet un atlasiet Ierobežot maksājuma marķiera lietošanu, lai sarakstā izveidotu pasūtījuma kontekstu,** un pēc tam atlasiet Iespējot tūlīt **.**

## <a name="limit-payment-token-usage"></a>Ierobežot maksājuma marķiera izmantošanu

Kad šī funkcija ir iespējota, Commerce headquarters lapas, kas tiek izmantotas maksājuma metodes tveršanai, atjauninās to, kā tās atsauces uz debitora maksāšanas metodēm, kas ir debitora failā. Šis atjauninājums galvenokārt ietekmēs divas operācijas jomas:

- Kā debitora karte failā tiek ievadīta debitora vārdā
- Kā maksājuma informācija attiecībā pret debitoru tiek glabāta turpmākiem pārdošanas pasūtījumu maksājumu ierakstiem

Kad debitors darījumus izmanto Commerce kanālos, maksājuma detaļas tiek saglabātas pārdošanas pasūtījuma kontekstā. Pārdošanas pasūtījuma konteksts ierobežo maksājuma marķieri, lai tas netiks izmantots kā maksājuma atsauce attiecībā uz debitora ierakstu maksājumu lapās jauniem vai rediģētiem pārdošanas pasūtījumu maksājumiem programmā Commerce Headquarters.

### <a name="payment-form-changes"></a>Maksājuma formas izmaiņas

Ja zvanu centrs vai Commerce headquarters lietotājs veic maksājumu debitoram attiecībā pret pārdošanas pasūtījumu, maksājumu lapā ir detalizēta informācija par maksājuma metodes atlasi. Ja ir **iespējota** funkcija Ierobežot maksājuma marķiera lietošanu pasūtījuma kontekstā, ja lietotājs maksājuma lapā atlasa plus zīmi (**+**), tiek rādīti tikai saglabāti "karte failā" ieraksti. Izmaiņām ir nepieciešams, lai zvanu centrs vai Commerce headquarters **lietotājs** ievadītu pilnu informāciju par maksājumiem, ko debitors ir sniedzis, aizpildot jaunās pārdošanas pasūtījuma darbības lapā Ievadīt debitora maksājuma informāciju.

Numura lauka vērtību sarakstā ir iekļautas **tikai** atsauces uz kartēm, kas saistītas ar debitoru, kurš ir uz faila pieejamais karte. Tas filtrē jebkuras pagājušo maksājumu atsauces, kas nav tvērumā pārdošanas pasūtījumam.

Pluszīme (**+**) **laukā** Numurs paliek pieejama, un to var izmantot, lai ievadītu maksājuma informāciju, ko debitors sniedzis darbībai, kas saistīta ar apstrādā atlasīto pārdošanas pasūtījumu.

### <a name="how-cards-on-file-work"></a>Kā darbojas kartes failā

Ja ir **iespējots** līdzeklis Ierobežot maksājuma marķiera lietošanu pasūtījuma kontekstam, karte failā ir atkārtojoša maksājuma marķieris, kas tiek saglabāts attiecībā pret debitora ierakstu un nav ierobežots ar pārdošanas pasūtījuma darbības jomu. Karte failā sniedz ātru atsauci Commerce Headquarters lietotājiem, kad tie aizpildīs maksājumu lapu jaunam pārdošanas pasūtījuma maksājumam. Šī marķiera atsauce ir piemērojama tikai Dynamics 365 videi. Tiešsaistes kanāliem, iFrame kas izmanto maksājumu vārtejas pakalpojumu, kas ļauj lietotājiem saglabāt maksājuma metodi turpmākai lietošanai maksājumu modulī, maksājumu vārteja droši saglabā šīs atsauces kā atsevišķu atsauci uz Dynamics 365 karti failā.

Piemēram, ja Maksājumu savienotājs Ahaen tiek izmantots tiešsaistes kanālā, debitori, Dynamics 365 Commerce iFrame kas ievada savu kredītkartes informāciju maksājumu modulī, redz tikai vārtejas pakalpojuma saglabātās kartes atsauces par nākamo tiešsaistes pirkumu, kad tie tiek autentificēti. Viņi neredzat Dynamics 365 vidē saglabāto karti failā kā opciju maksājuma modulī iFrame. Līdzīgā veidā, kad pircēji pasūta, izmantojot zvanu centru, to tiešsaistes saglabātās kartes atsauces netiek uzrādītas kā zvanu centra lietotāja opcijas. Zvanu centra lietotājs redz tikai iepriekšējo karti faila atsaucēs no Dynamics 365 sistēmas (kā debitors ir piekritis), lai saglabātu nākotnes pasūtījumiem.

Commerce Headquarters lietotāji var saglabāt debitora failā karti, noklikšķinot uz Mazumtirdzniecības **un Commerce \> Customers un** atlasot debitora konta ierakstu. Sadaļā Klientu **iestatīšana \> lietotāji**, kuriem ir atļauja apstrādāt maksājumu lapas, var izmantot kredītkaršu ierakstu lapu, lai ievadītu maksājuma karti, **kura** tiks saglabāta failā turpmākām darbībām. Šī operācija palīdz ietaupīt laiku, kad debitoram tiek apstrādāti turpmākie pārdošanas pasūtījumu maksājumi. Zvanu centram un Commerce headquarters lietotājiem ir jāievada karte ar faila kartes informāciju tikai tad, ja debitors piekrīt turpmākām darbībām izmantot kartes atsauci.

Izvēles **rūtiņa Saglabāt turpmākai lietošanai** Commerce Headquarters maksājumu lapu apakšā ļauj lietotājiem saglabāt karti failā turpmākai lietošanai. Šī izvēles rūtiņa ir jāizmanto tikai tad, ja debitors piekrīt izmantot karti failā turpmākām darbībām. Varat rādīt vai ierobežot **izvēles rūtiņu Saglabāt** **·** **·** **izmantošanai nākotnē, izmantojot opciju Atļaut debitora karti failā, kas atrodas cilnē Maksājums, kas atrodas** programmas Commerce Headquarters lapā Zvanu centra parametri. Kad šī opcija ir iestatīta uz **Jā**, Commerce Headquarters **lietotāji**, kuriem ir atļauja apstrādāt maksājumu lapas, var saglabāt karti failā, izmantojot izvēles rūtiņu Saglabāt lietošanai nākotnē. Kad opcija ir iestatīta uz **Nē**, šī izvēles rūtiņa nav pieejama Commerce Headquarters lietotājiem, kuriem ir atļauja apstrādāt maksājumu lapas. **Opciju Atļaut** debitora karti failam var izmantot, ja jūsu uzņēmums vēlas ierobežot periodisku marķieru lietošanu programmā Commerce Headquarters, bet tā vēl nevēlas atļaut faila kartes uzturēšanu, neveicot procedūru, kas nodrošina debitora atļaujas piešķiršanu.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Commerce Headquarters lapas, kurās tiek realizēti periodiskie marķieru ierobežojumi

Marķiera ierobežojuma punktu skaitīšana ietekmē tālāk norādītos commerce headquarters apgabalus, ja ir iespējota šī funkcija:

- Debitora maksājuma informācija pārdošanas **pasūtījuma maksājumiem \> Ievadiet \> debitora maksājumu**
- Nepārtrauktie pasūtījumi
- Iemaksu maksājumi
- Debitoru kredītkartes maksājumi

### <a name="manage-payment-tokens-archiving-or-removal"></a>Pārvaldīt maksājumu marķierus (arhivēšana vai noņemšana)

Maksājumu marķieri, kas tika izveidoti, pirms bija iespējots karodziņš Ierobežot maksājuma marķieru lietošanu uz pasūtījuma konteksta līdzekli (vai arī, ja funkcija tika atspējota) sistēmā paliks "nepārtraucts" un var tikt norādīti atsaucei commerce headquarters maksājumu lapas atlases **sarakstos**. Šos marķierus regulāri var noņemt divos programmas Commerce Headquarters veidos:

- Izmantojiet lapu **Arhīva kredītkartes transakciju dati**, lai iestatītu darbu, kas regulāri arhivē vai arhivē maksājuma marķierus. Ja iestatāt opciju **Dzēst datus bez** **arhivēšanas** **uz Jā, marķieri, kas atbilst minimālajam darbību vecuma (dienās)** iestatījumam, tiks dzēsti. Papildinformāciju skatiet sadaļā Kredītkaršu [darbību datu arhivēšana](archive-cc-data.md).
- Izmantojiet jauno kredītkaršu dzēšanas marķieru lapu (**·** **\> debitoru uzziņas un pārskati Dzēst kredītkartes marķierus \>), kas ļauj palaist vai iestatīt pakešuzdevumu, kas dzēš maksājumu marķierus.\>** Iestatiet šādus parametrus:

    - Minimālajam **marķiera vecums dienās vērtībai** jābūt 90 vai vairāk.
    - Darbību **fona iestatījumos var** izmantot, lai definētu periodiskuma **vai** **brīdinājumu** iestatījumus.
    - Pakešuzdevumu grupu var piešķirt, lai palaistu uzdevumu specifiskai grupai.
    - Ja opcija **Privāts** ir iestatīta uz **Jā**, to var palaist tikai lietotājs, kas veido šo darbu.
    - Jā iestatījums **opcijai** **Kritiskais** darbs nodrošina, ka sistēma aktīvi izseko darba statusu.

Dzēstos marķierus nevar izgūt. Iestatiet lauku **Minimālais marķiera** vecums dienās uz diapazonu, kas ir piemērots jūsu vides garākajam darbības dzīves ciklam (no autorizācijas uz tveršanu vai atmaksu).

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](payments-retail.md)

[Norēķināšanās modulis](../add-checkout-module.md)

[Maksājumu modulis](../payment-module.md)
