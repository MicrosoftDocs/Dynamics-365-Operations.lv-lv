---
title: Pārskats par kreditora rēķiniem
description: Šajā rakstā ir sniegta vispārīga informācija par kreditoru rēķiniem.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 565e45a1c396b9144b4a6437056a0040b2fbde1d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228757"
---
# <a name="vendor-invoices-overview"></a>Kreditoru rēķinu pārskats

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Šajā rakstā ir sniegta vispārīga informācija par kreditoru rēķiniem. Kreditoru rēķini ir maksājuma pieprasījumi par precēm un pakalpojumiem. Kreditoru rēķini var būt rēķini par notiekošiem pakalpojumiem, vai to pamatā var būt pirkšanas pasūtījumi par noteiktiem krājumiem un pakalpojumiem.

## <a name="vendor-invoices"></a>Kreditora rēķini

Kreditora rēķins no pirkšanas pasūtījuma tiek izveidots, kad preces vai pakalpojumi tiek saņemti saskaņā ar kreditoram iesniegtu pirkšanas pasūtījumu. Kreditora rēķinā tiek ietverts virsraksts un viena vai vairākas rindas ar krājumiem vai pakalpojumiem. Kreditora rēķins tiek izmantots ciklā “produktu ieejas plūsmas pirkšanas pasūtījums–kreditora rēķins”.

Lai gan daži kreditoru rēķini ir saistīti ar pirkšanas pasūtījumu, kreditoru rēķini var ietvert arī rindas, kas neatbilst pirkšanas pasūtījuma rindām. Varat arī izveidot kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumu. Šie kreditora rēķini var atspoguļot notiekošos pakalpojumus, piemēram, utilītas rēķinu. Ja pievienojat notiekošo pakalpojumu, nav nepieciešams atsaukties uz pirkuma pasūtījumu.

Kreditora rēķinu var ievadīt vairākos veidos:

- Reģistrējot kreditora rēķinu, varat ātri ievadīt rēķinus, kam nav izveidota atsauce uz pirkšanas pasūtījumu, tādējādi nodrošinot izdevumu uzkrājumu. Izmantojot kreditora rēķinu apstiprināšanas žurnālu, varat atlasīt un grāmatot šos rēķinus kreditora bilancē, tādējādi atceļot uzkrājumu.
- Kreditoru rēķinu žurnāls jums ļauj ar vienu darbību ātri ievadīt rēķinus, kam nav atsauces uz pirkšanas pasūtījumu.
- Kopā ar kreditoru rēķinu kopu kreditoru rēķinu reģistrs jums ļauj ātri ievadīt rēķinus, lai uzkrātu izdevumus. Vēlāk varat atvērt saistītos pirkšanas pasūtījumus, lai grāmatotu rēķinu pret izdevumu kontu.
- Lapa **Atvērtie kreditoru rēķini** un **Gaidošie kreditoru rēķini** jums ļauj izveidot kreditoru rēķinus no apstiprinātajiem pirkšanas pasūtījumiem.

Nākamajā diskusijā ir sniegts vairāk informācijas par to, kā lietot lapu **Atvērtie kreditoru rēķini** vai **Gaidošie kreditoru rēķini**, lai no pirkšanas pasūtījuma izveidotu kreditora rēķinu.

## <a name="understanding-invoice-line-quantities"></a>Rēķina rindu daudzumu saprašana

Kad kādu kreditora rēķinu atverat no saistīta pirkšanas pasūtījuma, sistēma no šī pirkšanas pasūtījuma izveido rēķina rindas. Pēc noklusējuma sistēma ņem daudzumus no produktu ieejas plūsmas. Taču varat izmantot jebkuru no šādām noklusējuma uzvedībām:

- **Tagad saņemamais daudzums** — izmantojiet šo opciju daļējiem sūtījumiem. Noklusējuma vērtība laukā **Daudzums** tiks iestatīta uz daudzumu, kas norādīts pirkšanas **pasūtījuma** laukā Saņemt tagad.
- **Pasūtītais daudzums** — izmantojiet šo opciju pilnīgiem sūtījumiem. Noklusētā vērtība laukā **Daudzums** tiks iestatīta uz daudzumu, kas norādīts pirkšanas **pasūtījuma** laukā Pasūtīts.
- **Reģistrētais daudzums** — izmantojiet šo opciju, ja krājumam ir nepieciešama reģistrācija, kā norādīts lapā **Krājumu modeļu grupas**. Lauka **Daudzums** noklusējuma vērtība ir reģistrētais fiziskais atjaunināšanas daudzums.
- **Produktu ieejas plūsmas daudzums** — izmantojiet šo opciju, ja pasūtījumam jau ir saņemta produktu ieejas plūsma. Noklusējuma vērtība laukā **Daudzums** ir pieejamo produktu ieejas plūsmu kopējais daudzums.
- **Reģistrētais daudzums un pakalpojumi** — izmantojiet šo opciju, ja daudzumi ir reģistrēti saņemšanas žurnālos attiecībā uz uzkrātajiem krājumiem vai krājumiem, kas nav uzkrāti. Šajā opcijā ir ietverti arī pakalpojumi neatkarīgi no tā, vai tie ir reģistrēti.

Ja jūsu juridiskā persona izmanto rēķinu salīdzināšanu, tad daudzumu salīdzināšanas rezultātus varat skatīt kolonnā **Produktu ieejas plūsmas daudzuma atbilstība**. Lai apskatītu daudzumu salīdzināšanas rezultātus, varat izmantot arī pogu **Detalizēta informācija par atbilstību** darbību rūts cilnē **Pārskatīt**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Pirkšanas pasūtījumā nebijušas rindas pievienošana

Varat pievienot kreditora rēķinam rindu, kas netika iekļauta pirkšanas pasūtījumā. Tādā gadījumā atlasiet krājuma kodu vai sagādes kategoriju. Pēc tam rindai varat pievienot daudzumus, cenas un summas. Šī rinda tiks iekļauta tikai atbilstības ierobežojumos rēķinu kopsummām.

## <a name="submitting-a-vendor-invoice-for-review"></a>Kreditora rēķina iesniegšana pārskatīšanai

Lai pārvaldītu kreditoru rēķinu pārskatīšanas procesu, organizācijā var tikt izmantotas darbplūsmas. Pārskatīšanu darbplūsmā var pieprasīt rēķina virsrakstam, rēķina rindai vai abiem vienumiem. Darbplūsmas vadīklas tiek piemērotas virsrakstam vai rindai atkarībā no tā, kurš apgabals bija fokusā, kad atlasījāt vadīklu. Tā vietā, **lai** pogu Grāmatot **, poga Iesniegt**, izmantojot pārskatīšanas procesu, sūta kreditora rēķinu.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Novērst rēķina iesniegšanu darbplūsmā 

Tālāk ir sniegti vairāki veidi, kā var novērst rēķina iesniegšanu darbplūsmā.

- **Rēķina kopsumma un reģistrētā kopsumma nav vienādas.** Lietotājs, kas iesniedza rēķinu, saņems brīdinājumu, ka kopsummas nav vienādas. Šis brīdinājums sniedz lietotājam iespēju labot bilances, pirms tie atkārtoti iesniedz rēķinu darbplūsmas sistēmā. Šī **funkcija** **·** **·** **ir** pieejama, ja aizliegt iesniegšanai darbplūsmā, ja rēķina kopsumma un reģistrētā rēķina kopsumma nav vienādi ar parametru līdzekļu pārvaldības lapā un opcija Darbplūsma, kad rēķina kopsumma un reģistrētā kopsumma nav vienāda ar parametru lapā Kreditoru parametri. 
- **Rēķinā ir nepiešķirtas izmaksas.** Lietotājs, kas iesniedza rēķinu, saņems brīdinājumu, ka rēķinam ir nepiešķirtas maksas. Šādā veidā lietotājs var labot rēķinu, pirms tas atkārtoti iesniegts darbplūsmas sistēmā. Šī **funkcija** **·** **ir pieejama, ja opcija Aizliegt iesniegšanu darbplūsmai, ja kreditoru rēķinu parametrā kreditoru rēķinu parametrā ir nesadalītas maksas, un** **opcija** Darbplūsma, kad kreditoru parametru lapā pastāv nesadalītas maksas.
- **Rēķinā ir tāds pats rēķina numurs kā citam iegrāmatotam rēķinam.** Lietotājs, kas iesniedza rēķinu, saņems brīdinājumu, ka atrasts rēķins ar dublikāta numuru. Lietotājs var labot dublikāta numuru, pirms tas atkārtoti iesniedz rēķinu darbplūsmas sistēmā. Brīdinājums tiks parādīts, ja parametrs **Pārbaudīt rēķina numuru, kas izmantots** parametrā Parādi kreditoriem, ir iestatīts uz **Noraidīt dublikātu**. Šis līdzeklis ir pieejams, ja parametrs **Aizliegt iesniegšanu darbplūsmā, ja rēķina numurs jau pastāv izliktā rēķinā, un jūsu sistēma nav iestatīta pieņemt rēķinu dublikātu numurus** ir ieslēgts lapā **Līdzekļu pārvaldība**.
- **Rēķinā ir rinda, kurā rēķina daudzums ir mazāks par saskaņoto preču ieejas plūsmas daudzumu.** Lietotājs, kurš iesniedz rēķinu vai mēģina to grāmatot, saņems ziņojumu, ka daudzumi nav vienādi. Šis ziņojums sniedz lietotājam iespēju labot vērtības, pirms tie atkārtoti iesniedz rēķinu darbplūsmas sistēmā. Šī funkcija **ir pieejama, ja kreditoru rēķinu grāmatošanas** **·** **·** **bloķēšana** un iesniegšana darbplūsmas parametram līdzekļu pārvaldības lapā un bloķēt grāmatošanu un iesniegšanu darbplūsmas parametram lapā Kreditoru parametri ir ieslēgta.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Kreditoru rēķinu salīdzināšana ar produktu ieejas plūsmām

Jūs varat ievadīt un saglabāt informāciju par kreditora rēķiniem, kā arī saskaņot rēķina rindas ar produktu ieejas plūsmu rindām. Turklāt rindai varat salīdzināt arī daļējus daudzumus.

Varat izveidot kreditora rēķinu, kurš ir balstīts uz produktu ieejas plūsmas rindā norādītajiem krājumiem, kas ir saņemti līdz pašreizējam datumam, pat ja visi konkrētā pirkšanas pasūtījumā norādītie krājumi vēl nav saņemti. Piemēram, šo opciju varat lietot, ja kreditors sūta vienu rēķinu mēnesī, kurš ietver visas piegādes, ko tas ir izsūtījis attiecīgajā mēnesī. Katra produktu ieejas plūsma attēlo pirkšanas pasūtījumā norādīto krājumu daļēju vai pilnīgu piegādi.

Kad rēķins ir darbplūsmā, apstiprinātājs var atjaunināt rēķina daudzumus, lai tie atbilstu vērtībai laukā **Product-receipt-quantity-to-match**. Lai to izdarītu, atlasiet līdzekli **Atjaunināt rēķina daudzumus, lai tie atbilstu produktu ieejas plūsmas daudzumiem** darbvietā **Līdzekļu pārvaldība** un atlasiet **Iespējot**. Ja apstiprinātājs darbplūsmas procesā ir noņēmis visas atbilstības no rēķina rindas visām produktu ieejas plūsmām, rēķina rinda tiks dzēsta. Ja šis līdzeklis nav iespējots, rēķinu daudzumi netiek atjaunināti rēķiniem darbplūsmā.

Kad grāmatojat rēķinu, katra krājuma daudzums laukā **Rēķina atlikums** tiek atjaunināts, ņemot vērā kopējo saņemto daudzumu, kas ir norādīts atlasītajās produktu ieejas plūsmās. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pirkšanas pasūtījumā ir 0 (nulle), tad pirkšanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0, tad pirkšanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.

Šajā opcijā tiek pieņemts, ka pirkšanas pasūtījumam ir grāmatota vismaz viena produktu ieejas plūsma. Kreditora rēķina pamatā ir šīs produktu ieejas plūsmas, un rēķinā tiek parādīts plūsmās esošais daudzums. Rēķina finanšu informācija ir balstīta uz informāciju, kas tiek ievadīta, kad grāmatojat rēķinu.

Plašāku informāciju skatiet šeit: [Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Konfigurējiet automatizētu uzdevumu kreditora rēķina darbplūsmai, lai grāmatotu kreditora rēķinu, izmantojot pakešuzdevumu

Kreditora rēķina darbplūsmai var pievienot automatizētu grāmatošanas uzdevumu, lai rēķini tiktu apstrādāti partijā. Rēķinu grāmatošana partijā ļauj turpināt darbplūsmas procesu, negaidot, kamēr tiek pabeigta grāmatošana, kas uzlabo visu darbplūsmai iesniegto uzdevumu vispārējo veiktspēju.

Lai iegrāmatotu kreditora rēķinu partijā, lapā **Līdzekļu pārvaldība**, ieslēdziet parametru **Kreditora rēķina partijas grāmatošana**. Kreditoru rēķinu darbplūsmas tiek konfigurētas, atverot **Kreditori > Uzstādīšana > Kreditoru darbplūsmas**.

Varat skatīt uzdevumu **Grāmatot kreditora rēķinu, izmantojot partiju** darbplūsmas redaktorā, neskatoties uz to, vai ir aktivizēts līdzekļa parametrs **Kreditora rēķina partijas grāmatošana**. Kad līdzekļa parametrs nav aktivizēts, rēķins, kas ietver parametru **Grāmatot kreditora rēķinu, izmantojot pakešuzdevumu** netiks apstrādāts darbplūsmā, kamēr parametrs nebūs iespējots. Uzdevumu **Grāmatot kreditora rēķinu, izmantojot partiju** nedrīkst izmantot tajā pašā darbplūsmā, kurā automatizēto uzdevumu **Grāmatot kreditora rēķinus**. Turklāt uzdevumam **Grāmatot kreditora rēķinu, izmantojot partiju** ir jābūt pēdējam elementam darbplūsmas konfigurācijā.

Varat norādīt rēķinu numuru, ko iekļaut partijā, un stundu skaitu, kas jāgaida pirms partijas pārveidošanas, dodoties uz **Kreditori > Uzstādīšana > Kreditoru parametri > Rēķins > Rēķinu darbplūsma**. 

## <a name="working-with-multiple-invoices"></a>Darbs ar vairākiem rēķiniem

Jūs varat vienlaikus strādāt ar vairākiem rēķiniem un grāmatot tos visus vienlaicīgi. Ja ir jāizveido vairāki rēķini, izmantojiet lapu **Gaidošie kreditoru rēķini**. Ja jāgrāmato un jādrukā vairāki kreditoru rēķini, izmantojiet rēķinu **apstiprināšanas žurnālu**. Ja izmantojat rēķinu **apstiprināšanas** žurnālu, pirkšanas pasūtījumam ir jāiegrāmato vismaz viena produktu ieejas plūsma, un pirkšanas pasūtījuma rēķins ir jāiegrāmato rēķinu reģistrā. Rēķina finanšu informācija tiek ņemta no rēķina, kas ir grāmatots reģistrā.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Lietošanā esošu kreditoru rēķinu atkopšana

Kamēr kreditora rēķins tiek lietots, cits lietotājs to nevar rediģēt. Taču rēķina stāvoklis reizēm var norādīt, ka rēķins tiek lietots, lai gan tas netiek aktīvi rediģēts. Piemēram, iespējams, programma ir pārstājusi reaģēt, kamēr rēķins tika rediģēts, vai kāds lietotājs ir nejauši atstājis rēķinu atvērtu programmā.

Varat izmantot lapu **Atkopt kreditoru rēķinus**, lai atkoptu vai izlaistu kreditoru rēķinus, kas tiek lietoti vairāk nekā četras stundas, un tos varētu rediģēt. Šo lapu var atvērt no navigācijas **Periodiskais uzdevums** vai elementa darbvietā **Kreditora rēķina ieraksts**. Kad rēķins ir atkopts, tas ir pieejams rediģēšanai lapā **Kreditora rēķins**.

Lapai **Atkopt kreditoru rēķinus** varat piekļūt tikai tad, ja jums ir piešķirts drošības pienākums un privilēģija **Atkopt lietošanā esošus kreditoru rēķinus**. Turklāt ir jābūt ieslēgtam parametram **Atļaut kreditoru rēķinu atkopšanu** lapā **Parādu kreditoriem parametri**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Darbplūsmas statusa atiestatīšana kreditoru rēķiniem no Neatkopjama uz Melnraksts

Darbplūsmas instancei, kas apturēta, jo radās neatkopjama kļūda, būs darbplūsmas statuss **Neatkopjama**. Ja kreditora rēķina darbplūsmas statuss ir **Neatkopjama**, varat atiestatīt to uz **Melnraksts**, atlasot **Atsaukt**. Pēc tam varat rediģēt kreditora rēķinu. Šī funkcija ir pieejama, ja ir ieslēgts parametrs **Atiestatīt darbplūsmas statusu kreditora rēķiniem no “Neatkopjama” uz “Melnraksts”** lapā **Līdzekļu pārvaldība**.

Varat izmantot lapu **Darbplūsmas vēsture**, lai atiestatītu darbplūsmas statusu uz **Melnraksts**. Varat atvērt šo lapu no **Kreditora rēķins** vai no navigācijas **Kopīgi > Vaicājumi > Darbplūsma**. Lai atiestatītu darbplūsmas statusu uz **Melnraksts**, atlasiet **Atsaukt**. Varat arī atiestatīt darbplūsmas statusu uz Melnraksts, atlasot darbību **Atsaukt** lapā **Kreditora rēķins** vai **Gaidošie kreditoru rēķini**. Kad darbplūsmas statuss tiek atiestatīts uz **Melnraksts**, tas kļūst pieejams labošanai lapā **Kreditora rēķins**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Rēķina kopsummas skatīšana lapā Gaidošie kreditoru rēķini

Varat skatīt rēķina kopsummu lapā **Gaidošie kreditoru rēķini**, iespējojot parametru **Parādīt rēķina kopsummu gaidošo kreditoru rēķinu sarakstā** lapā **Kreditoru parametri**. 

## <a name="vendor-open-transactions-report"></a>Kreditoru atvērto darījumu pārskats

Pārskats **Atvērtās kreditora darbības** sniedz detalizētu informāciju par katra kreditora atvērtajām darbībām jūsu norādītajā datumā. Šo pārskatu bieži izmanto audita procedūras laikā, lai pārbaudītu bilances starp kreditoru grāmatas darbībām un Virsgrāmatas konta darbībām.

Katrai darbībai pārskats ietver sekojošo detalizēto informāciju:

- Rēķina numurs
- Darījuma datums
- Dokumenta numurs
- Darījuma summa darījuma valūtā un uzskaites valūtā
- Kredīta atlikums darījuma valūtā un uzskaites valūtā
- Debeta atlikums darījuma valūtā un uzskaites valūtā
- Starpsumma uzskaites valūtā
- Maksājuma izpildes termiņš

### <a name="filter-the-data-on-the-report"></a>Filtrēt pārskatā parādītos datus

Veidojot pārskatu **Kreditora atvērtās darbības**, ir pieejami tālāk norādītie noklusējuma parametri. Izmantojot tos, varat filtrēt pārskatā ietveramos datus.

- **Izslēgt turpmāko segšanu** – atzīmējiet šo izvēles rūtiņu, lai izslēgtu darbības, kas nosegtas pēc datuma, kas ievadīts laukā **Atvērtās darbības pa**.
- **Atvērtās darbības pa** – ievadiet datumu, lai iekļautu darbības, kas ir atvērtas no šī datuma. Ja datums nav ievadīts, šis lauks ir iestatīts uz maksimālo datumu. (Maksimālais datums ir vēlākais datums, kuru sistēma akceptēs, 2154. gada 31. decembris.) Pēc noklusējuma nākošajā pārskata izpildes reizē šis lauks tiks iestatīts uz pēdējo datumu, kas tajā ievadīts.

Varat izmantot filtrus laukā **Ieraksti, kurus iekļaut** tālākai darbību datu ierobežošanai, kas tiek iekļauti pārskatā.

## <a name="additional-resources"></a>Papildu resursi

- [Iestatīt kreditoru rēķinu ierobežojumus](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Kreditora rēķina reģistrēšana rēķinu žurnālā](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
