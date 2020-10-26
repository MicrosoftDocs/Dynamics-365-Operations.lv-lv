---
title: Sūtījumu konsolidācijas politikas
description: Šajā tēmā sniegts pārskats par funkcionalitāti, kas nodrošina elastīgu sūtījumu konsolidācijas politiku konfigurāciju.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 4afa037ce9e446402128e4908a61ed32a30ebd59
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986954"
---
# <a name="shipment-consolidation-policies"></a>Sūtījumu konsolidācijas politikas

Sūtījumu konsolidācijas process, kas izmanto sūtījuma konsolidācijas politikas, atļauj sūtījuma konsolidāciju automātiskās un manuālās nodošanas noliktavā laikā. Automatizētajai konsolidācijai, kas bija pieejama pirms šīs funkcijas ieviešanas, bija stingri iekodēti lauki un tika pamatota ar lauku **Konsolidēt sūtījumu, pārvietojot uz noliktavu**, kas tika iestatīts noliktavai.

Sūtījuma konsolidācijas politikas tiek izmantotas šādai funkcionalitātei:

- Automatizēts pārvietot uz noliktavu partijas darbs
- **Pārvietot uz noliktavu** komanda pārdošanas pasūtījumā vai pārvietošanas pasūtījumā
- Atvēlētā **Pārvietot uz noliktavu** lapa
- Komanda **Pārvietot uz noliktavu** lapā **Kravu plānošanas rīks**
- Manuālā sūtījumu konsolidācija lapās **Konsolidēt sūtījumus** un **Sūtījuma konsolidācijas rīks**

Pirms tika ieviestas sūtījuma konsolidācijas politikas, konsolidācijas funkcija eksistēja kā iestatījums noliktavas līmenī. Visi pasūtījumi visiem debitoriem no vienas noliktavas tika apstrādāti tā, it kā tiem būtu vienādas konsolidācijas prasības. Sūtījuma konsolidācijas politikas pievieno atbalstu scenārijiem, kad dažādām organizācijām ir dažādas sūtījuma konsolidācijas prasības.

Vaicājumi tiek izmantoti, lai identificētu sūtījuma konsolidācijas politiku, kas tiek piemērota, un tad rediģējamu lauku kopa nosaka, kā noslodzes rindas tiek grupētas sūtīšanas līmenī. (Šis modelis atgādina modeli, kam kopums veidnes seko.) Turklāt katrai politikai ir pievienota opcija **Konsolidēt ar esošo sūtījumu**. Kad šī opcija ir ieslēgta, procedūra *Pārvietot uz noliktavu* atrod sūtījumus konsolidācijai, meklējot no esošajiem sūtījumiem, kas tika izveidoti, pamatojoties uz to pašu konsolidācijas politiku. Šādā gadījumā sistēma atlasīs esošo sūtījumu vai noslodzi, nevis veidos jaunu. Tomēr sistēma konsolidēs tikai ar esošiem sūtījumiem, kuru statuss ir *Atvērts*; sūtījumi, kas pieder pie kopuma izdošanas ar statusu *Pārvietots* vai lielāks, netiks uzskatīti par konsolidācijas mērķiem.

Kad ir pieejamas sūtījumu konsolidācijas politikas, **Konsolidēt sūtījumu pēc pārvietošanas uz noliktavu** iestatījums, kas iepriekš bija pieejams iestatījumu lapā **Noliktavas**, ir paslēpts. Lai palīdzētu jums pāriet uz jauno sūtījumu konsolidācijas funkciju, lapa **Sūtījuma konsolidācijas politikas** izveido noklusējuma politiku, kas automātiski ietver veco esošo noliktavu iestatījumu. Pēc tam, kad ir izveidota noklusētā politika, **Konsolidēt sūtījumu pēc pārvietošanas uz noliktavu** iestatījums iestatījumu lapā **Noliktavas** vairs netiks izskatīts.

Jūs varat izmantot lapu **Pārvietot uz noliktavu**, lai manuāli ignorētu piemērojamo konsolidācijas politiku tādā pašā veidā, kā varat ignorēt izpildes politikas.

Jūs varat izmantot **Pārvietot \> Pārvietot uz noliktavu** komandu lapā **Kravu plānošanas rīks**, lai izveidotu izejošās noslodzes, kas balstītas uz pārdošanas pasūtījumu un pārsūtīšanas pasūtījuma rindām, pirms pārvietojat tās uz noliktavu. Šīs noslodzes izmanto vienu un to pašu konsolidācijas loģiku, kas tika ieviesta kopā ar sūtījumu politiku konsolidāciju.

Jūs varat izmantot lapu **Sūtījuma konsolidācijas rīks**, lai konsolidētu esošos sūtījumus, kas vēl nav apstiprināti, bet ir jau pārvietoti uz noliktavu. Šī funkcionalitāte atbalsta scenārijus, kuros automatizētais izlaišanas process, kam ir sava sūtījuma konsolidācija, ir palaists vairākas reizes dienā, bet iespējamās papildu konsolidācijas tiek manuāli identificētas, pirms sūtījums pārvadātājiem tiek pabeigts apstiprināšanas procesa laikā. Šī funkcionalitāte ļauj konsolidēt izejošos sūtījumus, kas ir izveidoti no pārdošanas pasūtījuma vai pārsūtīšanas pasūtījuma rindām jebkurā laikā pēc sūtījumu pārvietošanas uz noliktavu, bet pirms tie tiek apstiprināti.

**Sūtījuma konsolidācijas rīka** lapa darbojas tāpat kā noslodzes veidošanas rīks, kur varat vienlaicīgi novērtēt vairākus sūtījumus un piešķirt nekonsolidētu pasūtījumu noteiktam sūtījumam. Jūs varat piemērot sūtījumu konsolidācijas veidnes, lai novērtētu piedāvātās konsolidācijas vairākas reizes un apstiprinātu tās. Dažas kārtulas tiek ieviestas, lai nepieļautu nesankcionētu konsolidāciju un brīdinātu par iespējamām kļūdām.

## <a name="overview-of-new-functionality"></a>Jaunas funkcionalitātes apskats

Šajā sadaļā ir aprakstītas lapas, komandas un līdzekļi, kas tiek mainīti vai pievienoti, kad ieslēdzat un izmantojat *Sūtījuma konsolidācijas politikas* līdzekli.

### <a name="shipment-consolidation-policies-page"></a>Sūtījumu konsolidācijas politiku lapa

Politikas atšķiras ar darba pasūtījuma veidu. **Pārdošanas pasūtījumu** veids atspoguļo _Pārdošanas pasūtījuma_ sūtījumus, un **Pārsūtīšanas pasūtījumu** veids atspoguļo _Pārsūtīšanas jautājumu_ sūtījumus.

Katrai sūtījuma konsolidācijas politikai ir vaicājums, kas definē, kad tas tiek lietots, un secības numurs, kas nosaka izpildes kārtību. Konsolidācija tiek lietota katrai unikālajai atlasīto lauku kombinācijai. Papildu sniegtais parametrs tiek izmantots konsolidācijai ar esošajiem (atvērtajiem) sūtījumiem. Politikas tiek novērtētas un piemērotas katru reizi, kad tiek izveidots jauns sūtījums (pirms kopuma apstrādes).

Ja politikai nav neviena obligāta lauka vai arī tas ietver jebkādu aizliegtu lauku, šī politika tiek atzīmēta kā nederīga sadaļā **Atlasītie**. Obligāto un aizliegto lauku saraksts ir stingri kodēts, un to var paplašināt.

Sekojošais saraksts parāda obligātos laukus. Tā kā sūtījumi vienmēr tiek sadalīti, pamatojoties uz šiem laukiem, jūs nevarat grupēt vairākus sūtījumus, kuru laukiem ir atšķirīgas vērtības.

- Pārdošanas pasūtījumos:

    - **Konta numurs:** _WHSShipmentTable.AccountNum_
    - **Piegādes adresāts:** _WHSShipmentTable.DeliveryName_
    - **Pasta adrese (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Noliktava:** _WHSShipmentTable.InventLocationId_

- Pārsūtīšanas pasūtījumiem:

    - **No noliktavas:** _InventTransferTable.InventLocationIdFrom_
    - **Uz noliktavu:** _InventTransferTable.InventLocationIdTo_

Šie lauki nav pieejami visiem dokumentu veidiem. Šie lauki nav redzami lietotāja interfeisā (UI), un tos nevar izmantot konsolidācijai.

- **Sūtījuma ID:** _WHSShipmentTable.ShipmentId_
- **Statuss:** _WHSShipmentTable.ShipmentStatus_
- **Sūtījuma konsolidācijas politika:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Darba transakcijas veids:** _WHSShipmentTable.WorkTransType_
- **Kopuma ID:** _WHSShipmentTable.WaveId_
- **Noslodzes ID:** _WHSShipmentTable.LoadId_
- **Sūtījuma ID:** _WHSLoadLine.ShipmentId_
- **Noslodzes ID:** _WHSLoadLine.LoadId_

Pēc noklusējuma, veidojot politiku, obligāto lauku kopa tiek izmantota kā konsolidācijas lauki. Tomēr sarakstu var modificēt, izmantojot bultiņas pa kreisi un pa labi. (Šis process līdzinās procesam, lai atlasītu metodes kopuma veidnēs.)

Vērtības, ko lietotāji atlasa šiem laukiem, tiks izmantotas visiem jaunajiem, izveidotajiem sūtījumiem, vai arī tās tiks pievienotas esošajiem sūtījumiem konsolidācijas laikā ar šiem sūtījumiem. Ja diviem sūtījumiem ir tāda pati vērtība laukam, kas atlasīts šo sūtījumu konsolidācijai, sūtījumi tiek konsolidēti. Tas pats princips attiecas uz visiem atlasītajiem konsolidācijas laukiem. Ja vērtības atšķiras, otrais sūtījums tiek atmests un tiks atlasīts jaunam sūtījumam. Automatizētās konsolidācijas process sastāv no visu unikālajām vērtību kombinācijām sūtījuma konsolidācijas laukiem un pēc tam piešķir sūtījumu attiecīgajai kombinācijai.

Konsolidācijas procesa laikā neatlasītie lauki tiek ignorēti. Ja diviem sūtījumiem neizvēlētajam laukam ir atšķirīgas vērtības, lauks tiek notīrīts (t.i., tas ir iestatīts uz tukšs). Ja abiem sūtījumiem neatlasītajam laukam ir vienāda vērtība, lauks tiek aizpildīts.

Konsolidācijas lauku saraksts (t.i., lauki, kas tiks notīrīti, ja tiem ir atšķirīgas vērtības) ir stingri kodēti. Sarakstā ir visi lauki, kas ir inicializēti no pārdošanas pasūtījuma vai pārsūtīšanas pasūtījuma rindas, kad tiek izveidots jauns sūtījums. Citiem vārdiem sakot, ja lauks nav inicializēts no pārdošanas pasūtījuma vai pārsūtīšanas pasūtījuma rindas, tas tiek ignorēts, ja esošajam sūtījumam tiek pievienoti jauni dati.

### <a name="release-to-warehouse-page"></a>Lapa Pārvietot uz noliktavu

- Jaunam laukam apakšējā režģī tiek parādīta konsolidācijas politika, kas tika izmantota.
- Jauna poga ļauj manuāli atlasīt un/vai ignorēt konsolidācijas politiku.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Komanda Pārvietot uz noliktavu lapā Kravu plānošanas rīks

- Loģika tika pielāgota, lai tā izmantotu piemērotās konsolidācijas politikas.
- Sūtījumi tagad tiek konsolidēti tikai vienas noslodzes ietvaros.

### <a name="consolidate-shipments-page"></a>Konsolidēt sūtījumu lapa

- Līdzīgu sūtījumu meklēšana (t.i., kandidāti konsolidācijai) tika mainīta, lai tā izmantotu sūtījuma konsolidācijas politikā atlasītos laukus.
- Lauki, kuriem dažādos sūtījumos ir atšķirīgas vērtības, tagad ir iestatīti kā tukši. (Iepriekš tika izmantotas vērtības no atlasītā "pamata" sūtījuma.)

### <a name="shipment-consolidation-workbench-page"></a>Sūtījumu konsolidācijas rīka lapa

- Jauna funkcionalitāte atdarina manuālās konsolidācijas procesu plašākā mērogā.
- Tagad jūs varat atvērt šo lapu, izmantojot izvēlni **Pārvietot uz noliktavu** modulī **Noliktavas pārvaldība**.
- Algoritms analizē esošos sūtījumus, kas vēl nav nosūtīti. Pēc tam tas piedāvā konsolidāciju, pamatojoties uz laukiem, kas atlasīti konsolidācijas politikā.

## <a name="comparison-of-functionality"></a>Funkcionalitātes salīdzināšana

Šajā tabulā ir apkopota informācija par to, kā sūtījumu konsolidācija darbojas, kad neizmantojat sūtījuma konsolidācijas politikas un kad tās izmantojat.

| Bez sūtījuma konsolidācijas politikas | Ar sūtījuma konsolidācijas politikām |
|---|----|
| Nav attiecināms | Pārdošanas vai pārsūtīšanas sūtījumiem, kas ir atlasīti konsolidācijai, ir jābūt tādai pašai konsolidācijas politikai kā izveidotajam sūtījumam, vai arī tiem ir jābūt piešķirtiem atvērtam sūtījumam (ja opcija **Konsolidēt ar esošajiem sūtījumiem** ir ieslēgta). |
| *Pārvietot uz noliktavu* procedūra nemeklē esošos sūtījumus, lai atrastu sūtījumu konsolidācijai. Lai atrastu sūtījumu konsolidācijai, tiek izmantoti tikai tie sūtījumi, kuri ir izveidoti, izmantojot pašreizējo procedūru *Pārvietot uz noliktavu*. | Ja opcija **Konsolidēt ar esošajiem sūtījumiem** ir ieslēgta konsolidācijas politikai, kas pašlaik tiek lietota, procedūra *Pārvietot uz noliktavu* meklē starp esošajiem sūtījumiem, kas tika izveidoti, pamatojoties uz to pašu konsolidācijas politiku, lai atrastu sūtījumu konsolidācijai. Tāpēc, ja jums ir divas politikas, sūtījums, kas tiek veidots, pamatojoties uz 2. politiku, nekad netiks konsolidēts ar sūtījumu, kas tika izveidots, pamatojoties uz 1. politiku. |
| Nav attiecināms | Ja konsolidācijas politikas lauku saraksts ir tukšs vai ja nav iespējams atrast politiku, katram pārdošanas pasūtījumam vai pārsūtīšanas pasūtījuma rindai tiek izveidots jauns sūtījums. |
| Šis konsolidācijas lauks definē unikālo vērtību kombināciju, kas tiek izmantota sūtījumu konsolidācijai *pārsūtīšanas rindai*. (Visi pārējie lauki tiek ignorēti.)<ul><li>Pasūtījuma numurs (OrderNum)</li></ul> | Šie konsolidācijas lauki definē unikālo vērtību kombināciju, kas tiek izmantota sūtījumu konsolidācijai *pārsūtīšanas rindai*. (Visi pārējie lauki tiek ignorēti.)<ul><li>Pasūtījuma numurs (OrderNum)</li><li>Piegādes saņēmējs (DeliveryName)</li><li>Pasta adrese (DeliveryPostalAddress)</li><li>ISO valsts kods (CountryRegionISOCode)</li><li>Adrese (Address)</li><li>Vietne (InventSiteId)</li><li>Noliktava (InventLocationId)</li><li>Sūtījuma pārvadātājs (CarrierCode)</li><li>Pārvadātāja pakalpojums (CarrierServiceCode)</li><li>Piegādes veids (ModeCode)</li><li>Pārvadātāja grupa (CarrierGroupCode)</li><li>Saņemšanas nosacījumi (DlvTermId)</li></ul>Šie lauki ir tikai lauki, kas ir pieejami un inicializēti, kad tiek izveidots jauns sūtījums. |
| Šie konsolidācijas lauki definē unikālo vērtību kombināciju, kas tiek izmantota sūtījumu konsolidācijai *pārdošanas rindai*. (Visi pārējie lauki tiek ignorēti.)<ul><li>Pasūtījuma numurs (OrderNum)</li><li>Debitora atsauce (CustomerRef)</li><li>Debitora pieprasījums (CustomerReq)</li><li>Saņemšanas nosacījumi (DlvTermId)</li></ul> | Šie konsolidācijas lauki definē unikālo vērtību kombināciju, kas tiek izmantota sūtījumu konsolidācijai *pārdošanas rindai*. (Visi pārējie lauki tiek ignorēti.)<ul><li>Pasūtījuma numurs (OrderNum)</li><li>Konta numurs (AccountNum)</li><li>Piegādes saņēmējs (DeliveryName)</li><li>Pasta adrese (DeliveryPostalAddress)</li><li>ISO valsts kods (CountryRegionISOCode)</li><li>Adrese (Address)</li><li>Vietne (InventSiteId)</li><li>Noliktava (InventLocationId)</li><li>Sūtījuma pārvadātājs (CarrierCode)</li><li>Pārvadātāja pakalpojums (CarrierServiceCode)</li><li>Piegādes veids (ModeCode)</li><li>Pārvadātāja grupa (CarrierGroupCode)</li><li>Starpnieka ID (BrokerCode)</li><li>Virziens (LoadDirection)</li><li>Saņemšanas nosacījumi (DlvTermId)</li><li>Debitora atsauce (CustomerRef)</li><li>Debitora pieprasījums (CustomerReq)</li></ul>Šie lauki ir tikai lauki, kas ir pieejami un inicializēti, kad tiek izveidots jauns sūtījums. |
| Nav attiecināms | *Pārdošanas rindai* ir obligāti šādi konsolidācijas lauki , un tos nevar noņemt:<ul><li>Konta numurs (AccountNum)</li><li>Piegādes saņēmējs (DeliveryName)</li><li>Pasta adrese (DeliveryPostalAddress)</li><li>Noliktava (InventLocationId)</li></ul>Pēc noklusējuma šie lauki tiks piešķirti, kad tiks izveidota jauna politika. Tos nevar noņemt. |
| Procedūra *Pārvietot noslodzes uz noliktavu* lapā **Noslodzes plānošanas rīks** izmanto savu atsevišķo kodu, lai izveidotu sūtījumus un kopumus. | Tiek piemērotas sūtījuma konsolidācijas politikas, lai noteiktu, kuri lauki jānovērtē konsolidācijai. Sūtījumi tiek konsolidēti tikai vienas noslodzes ietvaros. |
| Manuāli atlasiet **Konsolidēt sūtījumus** lapā **Visi sūtījumi** un tad izvēlieties "pamata" mērķa sūtījumu. Filtrs ieteiks visus esošos sūtījumus, kuriem ir atbilstošas vērtības vairākiem galvenajiem laukiem. | Manuāli atlasiet **Konsolidēt sūtījumus** lapā **Visi sūtījumi** un tad izvēlieties "pamata" mērķa sūtījumu. Sistēma ieteiks citus esošos sūtījumus, saskaņojot vairāku galveno lauku vērtības, kas ir konfigurētas attiecīgajām sūtījumu konsolidācijas politikām. |
| Varat izmantot komandu **Konsolidēt sūtījumus** lapā **Visi sūtījumi** tikai vienā sūtījumā. | Lapa **Sūtījuma konsolidācijas rīks** palīdz atrast sūtījumu kopu, kas vēl nav iekļauta nosūtītajā stāvoklī. Šie sūtījumi tiek analizēti, pamatojoties uz vairākiem galvenajiem laukiem, kas ir konfigurēti jūsu sūtījuma konsolidācijas politikā. Visi sūtījumi, kuros tika ieteiktas šo lauku vērtības, kas atbilst konsolidācijai.<p>Jūs varat manuāli uzturēt konsolidāciju, noņemot sūtījumus no piedāvātajām konsolidācijām un/vai pievienojot tām sūtījumus. Var rasties vairāki kļūdu veidi, bet dažus no tiem var ignorēt.</p> |
| **Noformējuma piezīme:** Procedūra *Pārdošanas pasūtījumu automātiska pārvietošana uz noliktavu* sadala pārdošanas rindas grupās. Katrai grupai ir sava unikāla **ReleaseToWarehouseId** vērtība, un tā tiek apstrādāta atsevišķi, veicot procedūru *Pārvietot uz noliktavu*. Šī procedūra izveido jaunu darbu neatkarīgi no darba pārtraukuma iestatījumiem. | **Noformējuma piezīme:** Procedūra *Pārdošanas pasūtījumu automātiska pārvietošana uz noliktavu* piešķir vienu un to pašu **ReleaseToWarehouseId** vērtību visām pārdošanas rindām, kas tiek apstrādātas. Visas pārdošanas rindas tiek apstrādātas vienlaicīgi pēc procedūras *Pārvietot uz noliktavu*. Lai nodrošinātu agrāku darbību, ir jākonfigurē darba pārtraukums pēc sūtījuma ID. |

## <a name="additional-resources"></a>Papildu resursi

- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)