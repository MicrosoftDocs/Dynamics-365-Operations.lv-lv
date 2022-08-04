---
title: Pirkšanas pasūtījuma grāmatošana
description: Šajā rakstā ir aprakstīta pirkšanas pasūtījuma cilne Krājumu grāmatošanas profilu lapā.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151038"
---
# <a name="purchase-order-posting"></a>Pirkšanas pasūtījuma grāmatošana

Pirkšanas **pasūtījuma cilne** lapā Noliktavas grāmatošanas **profili** tiek izmantota, lai kontrolētu, kā pirkšanas pasūtījumi tiek grāmatoti Virsgrāmatā. Divas galvenās aktivitātes, kas pirkšanas pasūtījumam tiek grāmatotas Virsgrāmatā: 

- Produktu saņemšana
- Rēķins

Lai fizisku darbību (produktu ieejas plūsmu) grāmatotu Virsgrāmatā pirkšanas pasūtījumā, jābūt atzīmētām šādām izvēles rūtiņām:

- Izvēles **rūtiņa Grāmatot produktu ieejas plūsmu** Virsgrāmatā **lapā Krājumu un noliktavas pārvaldības** parametri.
- Izvēles **rūtiņas Grāmatot** fiziskos **krājumus un Uzkrāt saistības produktu** ieejas plūsmā lapā **Krājumu modeļu** grupas.

Galvenajiem kontiem jābūt norādītiem lapā Krājumu grāmatošanas **metode** šādiem grāmatošanas tipiem:

- Saņemto pirkumu materiālu izmaksas
- Pirkšanas izdevumi, kas nav saistīti ar rēķiniem
- Pirkšana, uzkrāšana

Lai finanšu darbība (rēķins) tiktu iegrāmatota Virsgrāmatā pirkšanas pasūtījumā, jābūt šādiem nosacījumiem:

- Pirkšanas **pasūtījuma rindā** atlasītā krājuma lapā **Krājumu modeļu grupas** ir jābūt atzīmētai izvēles rūtiņai Grāmatot finanšu krājumus.
- Galvenajiem kontiem jābūt norādītiem lapā Krājumu grāmatošanas **metode** šādiem grāmatošanas tipiem:
  - Rēķinā iekļauto pirkto materiālu izmaksas
  - Produkta pirkšanas izdevumi
  - Pirkšanas tēriņi izdevumu sadaļai
  - Atlaide (pēc izvēles)

## <a name="fixed-receipt-price-posting"></a>Fiksētas saņemtā krājuma cenas grāmatošana

Fiksētas saņemtā **krājuma** **·** **cenu var izmantot kā standarta izmaksu kā alternatīvu opcijai Standarta izmaksas laukā Krājumu modelis, kas atrodas krājuma modeļu** grupu lapā. Galvenā atšķirība ir tā, ka **, izmantojot fiksētu** saņemšanas cenu, pašreizējā izmaksu cena krājumam tiks izmantota pēc krājumu ieejas plūsmas grāmatošanas. Fiksētas saņemšanas cenai nav izmaksu **pārvērtēšanas procesa**; grāmatojot finanšu atjauninājumu, grāmatošanas laikā tiek izmantota pašreizējā izmaksu cena. Ja ieejas plūsmas un rēķina izmaksu cena atšķiras, novirze grāmatos fiksētās saņemtā krājuma cenas peļņas un zaudējumu kontus.

Lai precei izmantotu fiksēto ieejas plūsmas cenu, ir jākonfigurē:

- Lapā Krājumu **modeļu grupas atzīmējiet** izvēles rūtiņu **Grāmatot fiziskos** **krājumus un Fiksētās saņemšanas** cenu. 
- Lapā Krājumu **un noliktavas vadības parametri** atzīmējiet izvēles **rūtiņu Grāmatot pavadzīmi Virsgrāmatā**.
- Lapā Noliktavas **grāmatošanas metode** norādiet galvenos kontus šādiem grāmatošanas tipiem:
  - Fiksētas saņemtā krājuma cenas peļņa
  - Fiksētas saņemtā krājuma cenas zaudējumi
  - Fiksētas saņemtā krājuma cenas korespondējošais konts

Papildinformāciju skatiet fiksētas saņemtā [krājuma cenas.](/supply-chain/cost-management/fixed-receipt-price.md)

## <a name="purchase-charges-and-stock-variation-posting"></a>Pirkšanas papildmaksas un krājumu novirzes grāmatošana

Ja plānojat ņemt vērā pirkšanas izmaksas un krājumu novirzes, rīkojieties sekojošo:

- Cilnes Rēķins **lapā Kreditoru** parametri **atzīmējiet** izvēles **rūtiņu Grāmatot virsgrāmatas** izmaksu kontā.
- **Pirkšanas pasūtījuma rindā** **atlasītā** krājuma lapā Krājumu modeļu grupas atzīmējiet izvēles rūtiņu Grāmatot fiziskos krājumus, **·** **Grāmatot** finanšu krājumus un Uzkrāt saistības produktu ieejas plūsmā.
- Lapā Sagādes **un avotu parametri atzīmējiet** izvēles rūtiņu Ģenerēt **izmaksas produktu ieejas** plūsmā.
- Lapā Krājumu **un noliktavas vadības parametri** atzīmējiet izvēles **rūtiņu Grāmatot pavadzīmi Virsgrāmatā**.

Lapā Krājumu **grāmatošanas metode** jānorāda galvenie konti šādiem grāmatošanas tipiem:

- Pirkšanas izdevumi, kas nav saistīti ar rēķiniem
- Produkta pirkšanas izdevumi
- Krājumu novirze

> [!NOTE]
> Maksas **grāmatošanas** veids netiek izmantots, ja virsgrāmatas parametrā **ir atlasīts parametrs** Grāmatot izmaksu kontā.

Papildinformāciju skatiet maksas konta [uzskaites principa grāmatošanai](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Grāmatošanas metodes konfigurācijas paraugs

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem:

- Kolonna **Klīringa** konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Šajā kontā grāmatotā summa tiek automātiski apgriezta, grāmatojot vēlāku darbību. 
- P **/F kolonna** norāda P fiziskai **grāmatošanai** un **F finanšu** grāmatošanai. 
- Kolonna **Vienāda** norāda, vai galvenais konts noteiktam grāmatošanas tipam parasti ir tāds pats kā cits grāmatošanas tips. Vērtība kolonnā norāda grāmatošanas tipu, kas parasti tiek izmantots.

> [!NOTE]
> Galvenie konti un galveno kontu nosaukumi ir tikai ieteikumi. Ieteicams<!--note from editor: Via Writing Style Guide.--> , ka strādājat ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.


| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Sekot | Apraksts |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Saņemto pirkto materiālu izmaksas | 140100</br>140101 | Materiālu krājumi</br>Piegādātie materiāli, kas nav izrakstīti rēķinā | Līdzeklis | Debets | Jā | P | Rēķinā iekļauto pirkto materiālu izmaksas | Tiek izmantots, kad pirkšanas pasūtījuma produktu ieejas plūsma ir iegrāmatota, korespondējošais konts ir Pirkšanas izdevumi, kas nav iegrāmatoti. Šī konta summa tiek anulēta, grāmatojot pirkšanas pasūtījuma rēķinu. |
| Pirkšanas izdevumi, kas nav saistīti ar rēķiniem | 600180 | Materiālu ieejas plūsmas | Izdevumi | Debets | Jā | P | |Tiek izmantots, kad tiek grāmatota pirkšanas pasūtījuma produktu ieejas plūsma. Ieejas plūsmai tiek izveidoti divi dokumenti, lai atsekotu pirkšanas cenu novirzes, kad tiek izmantotas standarta izmaksas. Konta korespondējošais konts pirmajā dokumentā ir Pirkšanas uzkrājums. Otra dokumenta korespondējošais konts ir saņemto iegādāto materiālu izmaksu un pirkšanas cenas noviržu kontu summa. Šajā kontā grāmatotās summas tiek apgrieztas, grāmatojot pirkšanas pasūtījuma rēķinu. |
| Rēķinā iekļauto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Nē | F  |Saņemto pirkto materiālu izmaksas | Tiek izmantots, kad ir iegrāmatots pirkšanas pasūtījuma rēķins. Korespondējošais konts ir preces pirkšanas izdevumi. Šis konts parāda krājumu jūsu bilancē. Šis konts parasti ir tas pats konts, ko izmanto piegādāto vienību izmaksām un pārdošanas pasūtījumam izrakstīto vienību izmaksām. |
| Produkta pirkšanas izdevumi | 600180 | Materiālu ieejas plūsma | Izdevumi | Kredīts | Jā | F  | |Tiek izmantots, kad ir iegrāmatots pirkšanas pasūtījuma rēķins. Rēķinam tiek izveidoti divi dokumenti, lai sekotu līdzi pirkšanas cenu noviržu izsekošanai, kad tiek izmantotas standarta izmaksas. Korespondējošais konts ir pirkšanas izdevumi, nerēķinots konts, kas tiek izmantots ieejas plūsmas grāmatošanai un atgriezts rēķina grāmatošanas laikā. Parāda izmaksas par krājumiem, kas iegādāti, izrakstot rēķinu, kas nav atspoguļots krājumu kontā bilancē. Šī ir pirkšanas cenas novirzes peļņas un zaudējumu grāmatošana, kuru visbiežāk var redzēt standarta izmaksu krājumu pirkumos.|
| Fiksētas saņemtā krājuma cenas peļņa (Pirkšana, fiksētas saņemtā krājuma cenas peļņa*) | 510310 | Pirkšanas cenas novirze | Izdevumi | Kredīts | Nē | F | Fiksētas saņemtā krājuma cenas zaudējumi | Tiek izmantots, kad pirkšanas pasūtījuma rēķins tiek grāmatots, un rēķinā iekļautā cena atšķiras no krājuma noklusētajām izmaksām. Šo kontu izmanto, kad starpība ir augstāka. Korespondējošais konts ir fiksētas saņemtā krājuma cenas korespondējošais konts. |
| Fiksētas saņemtā krājuma cenas zaudējumi (Pirkšana, fiksētas saņemtā krājuma cenas zaudējumi*) | 510310 | Pirkšanas cenas novirze | Izdevumi | Debets | Nē | F | Fiksētas saņemtā krājuma cenas peļņa | Tiek izmantots, kad pirkšanas pasūtījuma rēķins tiek grāmatots, un rēķinā iekļautā cena atšķiras no krājuma noklusētajām izmaksām. Šo kontu izmanto, ja starpība ir zemāka. Korespondējošais konts ir fiksētas saņemtā krājuma cenas korespondējošais konts. |
| Fiksētas saņemtā krājuma cenas korespondējošais konts (Pirkšana, fiksētas saņemtā krājuma cenas korespondējošais*) | 140900 | Krājumu novirze | Līdzeklis | Abi | Nē | F  | |Tiek izmantots, kad pirkšanas pasūtījuma rēķins tiek grāmatots, un rēķinā iekļautā cena atšķiras no krājuma noklusētajām izmaksām. Šis konts ir korespondējošais konts fiksētās saņemšanas cenas peļņas un zaudējumu kontiem. |
| Maksa | Nav piemērojams | Nav piemērojams | Nav piemērojams | Nav piemērojams | Nav piemērojams | Nav piemērojams | Nav piemērojams | Šis konts vairs netiek lietots. Lietojiet krājumu variāciju. |
| Krājumu novirze | 600170 | Krājumu novirze | Izdevumi | Kredīts | Nē | Abi | | Šis konts tiek izmantots, ja: <ul><li>Vienības cenā pastāv atšķirība starp produktu ieejas plūsmu un rēķinu.</li><li>Izmaksas tiek grāmatotas krājumam.</li><li>Netiešās izmaksas ir<!--note from editor: Edit okay?--> Pievienot iegādātajiem krājumiem. </li><li>Korespondējošais konts ir pirkšanas izdevumi, kas nav rēķina konts.</li></ul> |
| Pirkšana, uzkrāšana | 200140 | Uzkrātie pirkšanas pasūtījumi | Saistības | Kredīts | Y | P | |Tiek izmantots, kad pirkšanas pasūtījuma produktu ieejas plūsma ir iegrāmatota un ir aktivizēta pirkumu summu uzkrāšanas opcija. |
| Saņemšanas brīdī uzkrātais PVN | 250500 | Uzkrātais PVN | Saistības | Kredīts | Y | Abi  | |Šis konts tiek lietots, ja krājumu **un noliktavas** **pārvaldības parametros atlasāt opciju Grāmatot fiziskos** nodokļus un jums ir pirkšanas pasūtījums ar nodokļiem. Summa tiek grāmatota, atjauninot pirkšanas pasūtījumu fiziski (produktu ieejas plūsmu) un atsaucot, kad finansiāli grāmatojat pirkšanas pasūtījumu (rēķins). |
| Pamatlīdzekļa saņemšana (Pamatlīdzekļa debets*) | 180100 | Materiālais pamatlīdzeklis | Līdzeklis | Debets | Nē | Abi | Abi | Šis konts tiek lietots, ja pamatlīdzekļu pirkšanas pasūtījuma rindā atlasāt opciju. Pirkšanas pasūtījuma integrācija ir konfigurēta, lai iegūtu pamatlīdzekli produktu ieejas plūsmas vai rēķina laikā. Papildinformāciju par pamatlīdzekļu pirkšanas pasūtījumu integrāciju skatiet sadaļu Līdzekļu [iegāde ar sagādes palīdzību](/fixed-assets/acquire-assets-procurement). |
| Pirkšanas tēriņi izdevumu sadaļai | 618900 | Dažādi izdevumi | Izdevumi | Debets | Nē | Abi | |Tiek izmantots, grāmatojot produktu ieejas plūsmu vai rēķinu pirkšanas pasūtījumam, kurā krājumi nav uzkrāti vai tiek izmantota sagādes kategorija. |
| Priekšapmaksa | 132190 | Iepriekš apmaksāti izdevumi | Līdzeklis | Debets | Nē | Abi | | Izmanto, apstrādājot priekšapmaksas rēķinu pirkšanas pasūtījumā. |


\* Iekavās redzamās vērtības norāda vērtību, kas tiek izmantota **laukā Grāmatošanas** tips dokumentu **darbību** lapā. Cilnes Vispārīgi **lapā Dokumentu** darbības var **skatīt Grāmatošanas** **tipu**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Pamatlīdzekļu grāmatošana ar pirkšanas pasūtījumiem

Ja izmantojat **moduli Pamatlīdzekļi un plānojat pirkt pamatlīdzekļus, izmantojot pirkšanas pasūtījumus,** **·** **pamatlīdzekļu saņemšanas grāmatošanas tips ir jākonfigurē cilnes Pirkšanas pasūtījums** lapā Krājumu **grāmatošanas** profils. Plašāku informāciju skatiet pamatlīdzekļu [integrācijā un Izveidojiet](/fixed-assets/fixed-asset-integration.md) un [iegūstiet līdzekļus no parādiem kreditoriem](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Pirkšanas pasūtījuma priekšapmaksas rēķina grāmatošana

Ja pirkšanas pasūtījumiem **plānojat izmantot** priekšapmaksas rēķina līdzekli, **·** **·** **nepieciešams atlasīt priekšapmaksas grāmatošanas tipu cilnes Pirkšanas pasūtījums lapā Krājumu grāmatošanas** metode. Papildinformāciju skatiet sadaļu Priekšapmaksas [rēķini pret priekšapmaksām](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Pirkšanas pieprasījuma un pirkšanas pasūtījuma apstiprinājuma grāmatošana

Pirkšanas pieprasījumus un pirkšanas pasūtījuma apstiprinājumus var konfigurēt, lai Virsgrāmatā grāmatotu apgrūtinājumus bez juridiskām saistībām un apgrūtinājumus. Šos grāmatojumus kontrolē grāmatošanas definīcija. Papildinformāciju skatiet par pirkšanas [pasūtījuma apgrūtinājumiem](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Sagādes kategorijas grāmatošana

Kā alternatīvu krājumu grāmatošanas iestatīšanai visiem krājumiem, krājumu grupai vai vienam krājumam, varat iestatīt kategorijas un kontrolēt virsgrāmatas grāmatošanu pēc sagādes kategorijām. Lai iegūtu papildinformāciju par kategoriju iestatīšanu un to piešķiršanu precēm, agrāk [šajā rakstā dodieties](#sample-posting-profile-configuration) uz grāmatošanas metodes konfigurācijas paraugs.

Izmantojot kategorijas ar pirkšanas pasūtījumiem vai kreditoru rēķiniem, **kategoriju hierarhija ir jāpiešķir Sagādes kategoriju** **hierarhijas tipam kategoriju hierarhijas lomu piešķiru** lapā.

### <a name="vendor-invoices-with-procurement-categories"></a>Kreditora rēķini ar sagādes kategorijām

Ja jūsu organizācija izmanto pirkšanas pasūtījumus dažiem pirkumiem, bet ne citiem, jūs varat apstrādāt ar pirkšanas pasūtījumiem nesaist saistītos rēķinus dažādos veidos. Tas ietver žurnālu izmantošana Parādi kreditoriem **vai** **Neizlemto kreditoru rēķinu** lapa, kas tiek izmantota pirkšanas pasūtījumu rēķinu ģenerēšanai. Veidojot rēķinus rēķiniem, kas nav saistīti ar pirkšanas pasūtījumiem, ir nepieciešams izveidot sagādes kategorijas katram izdevumu tipam. Jums ir jākartē kategorija uz pareizo izdevumu kontu lapā Krājumu **grāmatošanas metodes**.

Precīzs kategoriju skaits var atšķirties atkarībā no izdevumu kontu skaita, kas tiek izmantots rēķinu grāmatošanai. Ir nepieciešama vismaz viena sagādes kategorija katram galvenajam kontam, kurā jūs izdevuma nav pirkšanas pasūtījuma rēķini. Daudzām kategorijām var izmantot vienu galveno kontu. Tas var būt noderīgi izmantojamībai, meklēšanai un jūsu lietoto izdevumu veidu pārskatu pārskatiem.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Kreditora rēķinu sagādes kategoriju izmantošanas priekšrocības

Dažas kreditora rēķinu sagādes kategoriju izmantošanas priekšrocības ir:

- Konsekventa lietotāja pieredze: konfigurējot sagādes kategorijas visiem ar pirkšanas pasūtījumiem saistītajiem izdevumiem, lietotāji var tikt kvalificēti vienam rēķinu izrakstīšanas procesam, **izmantojot lapu Neizlemti kreditora rēķini**.
- Uzlabota pārskatu izveides pieredze: konfigurējot sagādes kategorijas visiem krājumiem un visiem ar pirkšanas pasūtījumiem nesaistītajām izmaksām, sagādes tēriņu pārskats analizēs kreditora, kategorijas un citu tēriņu skaitu.
- Saskaņota darbplūsma: kad jūs izmantojiet **Nenokārtoto kreditoru rēķinus**, lai apstrādātu visus rēķinus, jūs varat izveidot konsekventu darbplūsmu un apstiprināšanas procesu, izmantojot vienu darbplūsmu.

## <a name="consignment-inventory-posting"></a>Sūtījuma krājumu grāmatošana

Sūtījuma krājumos tiek izmantota tā pati grāmatošana Virsgrāmatā kā citi pirktie krājumi. Galvenā atšķirība ir tā, ka, saņemot krājumu, Virsgrāmatas darbības netiek ierakstītas. Lai pārsūtītu organizācijas īpašumtiesības, **kad tiek grāmatots** krājumu īpašumtiesību izmaiņu žurnāls, tiek ģenerēts dokuments, lai ierakstītu krājuma izmaksas. Lai iegūtu papildu informāciju, dodieties [uz Iestatiet sūtījumu](/supply-chain/inventory/consignment.md).
