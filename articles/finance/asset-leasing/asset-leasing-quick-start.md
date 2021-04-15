---
title: Līdzekļu nomas sākšana
description: Šajā tēmā ir aprakstīta līdzekļu nomas iespēja un veicamās darbības, lai izveidotu līdzekļu nomu un skatītu to informāciju.
author: moaamer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d5b51e89ec0e64182671872573ec0140939a836
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814132"
---
# <a name="asset-leasing-get-started"></a>Līdzekļu nomas sākšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta līdzekļu nomas iespēja un veicamās darbības, lai izveidotu līdzekļu nomu un skatītu to informāciju. Tēmā ir definēta arī terminoloģija, kas tiek izmantota lietotāja interfeisā un dokumentācijā. Līdzekļu noma ir papildu iespēja finanšu darbību pārvaldībai, izsekošanai un automatizēšanai nomātajiem līdzekļiem Microsoft Dynamics 365 Finance. Līdzekļu noma atbilst starptautiskajiem grāmatvedības standartiem (16. SFPS) un ASV vispārpieņemtajiem grāmatvedības principiem (ASC 842). Līdzekļu noma notver un apstrādā nomu informāciju un palīdz ģenerēt žurnāla ierakstus, izmantojot nomas dzīves ciklu, no sākotnējās atzīšanas, ikmēneša žurnālu ierakstiem līdz nomas vērtības samazinājumam un pārtraukšanai. Līdzekļu noma ir integrēta ar citiem Dynamics 365 Finance komponentiem, tostarp pamatlīdzekļiem, kreditoriem un virsgrāmatu.

Lai iegūtu vairāk informācijas par grāmatvedības standartiem, skatiet 16. SFPS standarta dokumentāciju un ASV vispārpieņemtos grāmatvedības principus ASC 842.

## <a name="asset-leasing-elements"></a>Līdzekļu nomas elementi
Diagrammā ir parādīti nomas biznesa procesa galvenie elementi.

[![Līdzekļu nomas elementi](./media/overview-01.png)](./media/overview-01.png)

Iznomāts līdzeklis ietver šādus galvenos komponentus:

- **Nomas līgums** — iznomātājam pieder līdzeklis un viņš piekrīt nomniekam iznomāt līdzekli uz noteiktu laika periodu apmaiņā pret periodiskiem nomas maksājumiem. Papildus juridiskajam līgumam starp iznomātāju un nomnieku, nomas līgumā tiek ietverti pārvaldības lēmumi, piemēram, atjaunošanas opcijas izmantošana un īpašumtiesību maiņa.

- **Nomas aprēķins un klasifikācija pēc grāmatvedības standarta** — nomas aprēķinā un klasifikācijā tiek noteikts grāmatvedības standarts, kas tiks piemērots sākotnējā un turpmākajā novērtēšanā, kā arī klasifikācijas tests, kas nosaka nomas veidu. Noma var tikt klasificēta kā finanšu noma, operatīvā noma, īstermiņa noma vai nelielas vērtības noma. Sistēma arī aprēķina nākotnes minimālo nomas maksājumu neto pašreizējo vērtību, lai veiktu novērtēšanu un klasifikāciju.

- **Nomas darījumi** — līdzekļu noma atbalsta bilances nomas līdzekļa lietošanas tiesību sākotnējo atzīšanu, kā arī turpmāku novērtēšanu gan bilances nomas, gan ārpusbilances nomas gadījumā. Sākotnējās atzīšanas darījums nosaka nākotnes minimālo nomas maksājumu neto pašreizējo vērtību. Šie dati tiek izmantoti, lai noteiktu sākotnējo līdzekļa lietošanas tiesību un nomas saistību vērtību, kas ietekmē organizācijas bilanci. Ikmēneša nomas darījumu turpmākā novērtēšana ietver nomas saistību procentu uzkrāšanu, kas palielina nomas saistības. Tas arī nosaka nomas maksājumu uzkrājumu, kas samazina nomas saistības, un kas vēlāk tiks maksāts iznomātājam. Novērtējumā ietilpst arī līdzekļa lietošanas tiesību amortizācija.

  Ārpusbilances nomas gadījumā sistēma aprēķina lineārās nomas izdevumus atkarībā no tā, kas ir mazāks: aktīva saimnieciskā dzīve vai nomas termiņš. Nomas pielāgojumi novērtē līguma izmaiņas, piemēram, nomas termiņa pagarināšanu un darījumu ar vērtības samazinājumu, kas izmanto līdzekļa lietošanas tiesības neatlīdzināmiem izdevumiem.

  Līdzekļu noma tiek integrēta virsgrāmatā, lai nodrošinātu, ka visi iegrāmatotie nomas darījumi atjaunina kontu plānu. Līdzekļu noma tiek integrēta kreditoros, lai izsekotu iznomātāju rēķiniem kreditoros un veiktu nākotnes maksājumus no tiem. Integrācija pamatlīdzeklī ļauj izsekot nomai pamatlīdzekļu reģistrā un grāmatot līdzekļa lietošanas tiesību darījumus, tajā skaitā sākotnējo atzīšanu, nolietojumu un līdzekļa vērtības samazinājumu tieši pamatlīdzekļos.   

## <a name="asset-leasing-components"></a>Līdzekļu nomas komponenti 
Līdzekļu nomas kartes nomā informāciju, maksājumu grafikus, sākuma un beigu datumus un maksājumu biežumu. Kā arī automatizē aprēķinus neto pašreizējai vērtībai, ikmēneša nomas maksājumiem, procentiem un nomas amortizācijai. Atkarībā no konfigurācijas sistēma veic nomas klasifikācijas testus. Sistēma izveido un grāmato arī atbilstošos nomas darījumus, kuru pamatā ir izmantotā grāmatvedības standarta definētais regulējums.

Diagrammā ir parādīta nomas grāmata, nomas līgums, aprēķinātais maksājumu grafiks, nomas un nomas grāmatu klasifikācijas testi un attiecīgie grāmatvedības darījumi.

[![Noma, nomas grāmata un maksājumu grafiks](./media/overview-02.png)](./media/overview-02.png)

- **Nomas grāmata** — nomas grāmatā ir iekļauta visa nomas līguma informācija, piemēram, nomas noteikumi, patiesā vērtība un nomas maksājumi. Tā ietver arī jūsu izmantoto grāmatvedības standartu, nomas veidu un sliekšņus, kas tiek ņemti vērā nomas klasifikācijas testā. Nomas grāmatā ietverti arī nomas darījumi, kas iegrāmatoti virsgrāmatā. 
  
- **Noma** — nomā atrodas līdzekļa nomas informācija, kas ir līdzekļu nomas pamats, nomas informācijas avots ir nomas līgums un vadības lēmums, kas tiek pieņemti ārpus programmas Dynamics 365 Finance. Līdzekļa patiesā vērtība ir cena, kas tiks maksāta par līdzekli novērtēšanas datuma darījumā. Šī vērtība var būt atkarīga no līdzekļa veida, tirgus apstākļiem un citiem kritērijiem, kas var tikt ņemti vērā novērtējumā. Līdzekļa patiesā vērtība tiks ņemta vērā klasifikācijas testa vienādojumā.

- **Līdzekļa lietderīgās lietošanas laiks** — attēlo līdzekļa atlikušos lietderīgās lietošanas laika periodus no nomas sākuma datuma. Līdzekļa lietderīgās lietošanas laiks tiks ņemta vērā klasifikācijas testa vienādojumā. Tas atšķiras no lietderīgā lietošanas laika, kas definēts pamatlīdzekļos.

- **Salīdzināmā aizņēmuma procentu likme** — šī ir procentu likme, kas tiks izmantota neto pašreizējās vērtības aprēķināšanai. Sistēma izmantos netiešo likmi, ja tā ir definēta nomas datos, nomas maksājumu neto pašreizējo vērtību aprēķināšanai. Ja netiešā likme nav definēta, sistēma izmantos salīdzināmā aizņēmuma procentu likmi.

- **Priekšsamaksas veids** — šis ir nomas maksājums, kas jāveic vai nu maksājuma perioda sākumā, vai perioda beigās. Tas varētu būt avansa maksājums vai priekšsamaksa (nomas maksājuma perioda sākumā) vai apmaksājama priekšsamaksa (nomas maksājuma perioda beigās).

  Pirmo mēnesi uzskata par periodu, kura vērtība ir nulle, par maksājumu avansā; pirmo mēnesi uzskata par parāda pirmo periodu.

- **Pievienošanas intervāls** — norāda periodu skaitu, kurā procenti tiek pievienoti gadā. Tas varētu būt reizi mēnesī (12 periodi gadā), reizi ceturksnī (4 periodi gadā), pusgadā (2 periodi gadā), vai reizi gadā (1 periods gadā). Periodu skaits tiks ņemts vērā neto pašreizējās vērtības aprēķinā.

- **Sākuma datums** — šis ir datums, kad iznomātājs padara līdzekli pieejamu nomniekam. Visi nomas aprēķini un darījumi tiks balstīti uz sākuma datumu. Sākuma datumam vajadzētu būt perioda sākumā (pirmais mēnesis), lai nodrošinātu turpmāko aprēķinu pareizību. Varat izmantot lauku **Līguma parakstīšanas datums**, lai ievadītu faktisko datumu, kad līgums tika parakstīts.

- **Nomas termiņš** — tas ir nomas perioda ilgums mēnešos.

> [!NOTE] 
> Nomas termiņa definīcija ir balstīta uz periodu skaitu vai intervāliem maksājumu grafika rindās. Definētais intervālu skaits tiks konvertēts uz mēnešiem.

- **Maksājumu grafika rinda** — tver nomas maksājumus pa periodiem. Tā arī nosaka, vai atjaunošanas periods tiks izmantots un ietverts sākotnējā līdzekļa lietošanas tiesību un nomas saistību novērtējumā. Varat definēt nomas apmaksas maksājumu sākuma datumu un perioda intervālus, tādējādi norādot nomas ilgumu, kas var būt dienas, mēneši vai gadi.

- **Maksājumu biežums** — norāda, vai maksājums ir jāveic reizi mēnesī, reizi ceturksnī, pusgadā vai reizi gadā. Beigu datums tiek aprēķināts automātiski, pamatojoties uz sākuma datumu un ievadīto periodu skaitu.

- **Maksājumu grafiks** — šī ir aprēķinātā neto pašreizējā vērtība, pamatojoties uz nomas maksājumu aptverto laika ilgumu, maksājumu summu, saliktajiem periodiem un priekšsamaksas veidu.

- **Periodi** — tie ir nomas periodi, kas atspoguļo pievienošanas intervālu un priekšsamaksas veidu. Pievienošanas intervāls nosaka, kā periodi tiks sadalīti. Varat iestatīt šādus pievienošanas intervālus:

  - Reizi mēnesi, 12 periodi gadā
  - Reizi ceturksnī, 4 periodi gadā
  - Reizi pusgadā, 2 periodi gadā
  - Reizi gadā, 1 periods gadā

Pirmais periods sāksies ar nulles periodu, ja priekšsamaksas veids ir priekšsamaksa. Pretējā gadījumā pirmais periods sāksies ar viens, ja priekšsamaksas veids ir parāds.

- **Mēneši** — norāda kalendāro mēnešu skaitu, kas pārsniedz nomas ilgumu. Maksājuma summa ir maksājamā summa, kas definēta maksājumu biežumā. Aprēķinātā neto pašreizējā vērtība ir neto pašreizējā vērtība, kas balstīta uz nomas maksājumiem periodos, pievienošanas intervāliem un salīdzināmā aizņēmuma procentu likmi.

> [!NOTE] 
> Neto pašreizējā vērtība tiek aprēķināta, pamatojoties uz diskontētās naudas plūsmas vienādojumu.

- **Grāmatas** — šis ir iepriekš konfigurēts iestatījums, kas tiks saistīts ar katru nomu. Grāmatā ir definēts piemērotais grāmatvedības standarts, nomas veidi un slieksnis, kas tiek izmantots kā klasifikācijas testu pamats. Klasifikācijas testus izmanto automātiskai nomas veida piešķiršanai.

- **Uzskaites ietvars** — parāda atlasītās grāmatvedības standartu, vai nu 16. SFPS, vai ASC 842, kas tiek atbalstīts. Grāmatvedības standarts ir norādīts ar nomu saistītajā grāmatā. Grāmatvedības standarts noteiks virsgrāmatas kontus, kas tiks norādīti grāmatošanas metodē.

- **Nomas veidi** — norāda, kurš no abiem nomas veidiem tiks izmantots, finanšu noma vai operatīvā noma. Finanšu nomas ietvaros riski un atlīdzības, kas saistītas ar iznomāto līdzekli, tiek pārsūtītas nomniekam. Operatīvās nomas ietvaros riski un atlīdzības, kas saistītas ar iznomāto līdzekli, paliek iznomātājam. Trešā opcija ir automatizēta nomas veida identifikācija, finanšu vai operatīvā, pamatojoties uz grāmatā definētajiem sliekšņiem. Šī automātiskā identifikācija tiek veikta nomas pārklasificēšanas testa laikā.

- **Sliekšņi** — tiek izmantots nomas klasifikācijas testos, lai noteiktu līdzekļa klasifikāciju:

  - **Nomas termiņš** — šī ir lietderīgā lietošanas laika procentuālā vērtība, kas jāizmanto klasifikācijas testā. Sistēma klasificēs nomu kā finanšu, ja nomas veids ir iestatīts uz automātisks un ja nomas termiņa līdzekļa lietderīgās lietošanas laiks ir lielāks vai vienāds ar šeit norādīto procentuālo vērtību.

  - **Neto pašreizējā vērtība** — šī ir līdzekļa patiesās vērtības procentuālā vērtība, kas jāizmanto klasifikācijas testā. Sistēma klasificēs nomu kā finanšu, ja nomas veids ir iestatīts uz automātisks un ja turpmāko nomas maksājumu neto pašreizējā vērtība pār līdzekļa patieso vērtību ir lielāka vai vienāda ar šeit norādīto procentuālo vērtību.

  - **Īstermiņa noma** — ja nomas termiņš ir mazāks vai vienāds ar definēto vērtību, noma tiks klasificēta kā īstermiņa noma.

  - **Mazvērtīgs** — ja līdzekļa patiesā vērtība ir mazāka vai vienāda ar definēto vērtību, noma tiks klasificēta kā nelielas vērtības noma.

  - **Nomas klasifikācija un darījumi** — nomas klasifikācija ir automātisks process, lai klasificētu nomas, pamatojoties uz grāmatās noteiktajiem sliekšņiem papildus citiem klasifikācijas testa kritērijiem, lai noteiktu, vai noma ir finanšu noma, operatīvā noma, īstermiņa noma vai nelielas vērtības noma. To izmanto arī, lai noteiktu, vai tiek ievērots atliktās nomas maksas process.

Klasifikācijas testi ietver īpašumtiesību nodošanu, pirkšanas opciju, nomas termiņu, neto pašreizējo vērtību un unikālu līdzekli. Diagramma attēlo nomas klasifikācijas testus.

[![Nomas klasifikācijas testi](./media/overview-03.png)](./media/overview-03.png)

Katrs nomas veids dažādu nomas darījumu uzskaiti veic atšķirīgi. Darījumi ietver sākotnējo atzīšanu, procentu izdevumus, nomas maksājumu un nomas nolietojumu, un tie ir balstīti uz grāmatvedības standartiem, kuriem sekojat (16. SFPS vai ASC 842). Virsgrāmatas konti ir definēti nomas grāmatošanas metodē katram darījuma veidam un uzskaites ietvaram.

## <a name="asset-leasing-transactions"></a>Līdzekļu nomas darījumi

#### <a name="initial-recognition"></a>Sākotnējā atzīšana 
Iznomātā līdzekļa sākotnējā atzīšana izmanto neto pašreizējo aprēķināto vērtību, lai to varētu grāmatot bilancē. Uzskaites ieraksts šim darījumam tiek ģenerēts automātiski. Šis darījums debetē līdzekļa lietošanas tiesību kontu un kreditē operatīvo nomas saistību kontu, kā aprakstīts tālāk. Ja pamatlīdzeklis ir saistīts ar nomu, sākotnējās atzīšanas ieraksts tiks atainots kā pamatlīdzekļa iegāde. Šajā scenārijā ir jādefinē pamatlīdzekļu grāmatošanas metode, lai iegrāmatotu līdzekļa lietošanas tiesību kontu. 

> [!NOTE]
> Operatīvās nomas tiek atbalstītas, izmantojot tikai ASV vispārpieņemtos grāmatvedības principus ASC 842.

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operatīvā noma saskaņā ar ASV vispārpieņemtajiem grāmatvedības principiem            |     Līdzekļa lietošanas tiesības        |     Operatīvās nomas saistības     |
|     Finanšu noma saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem      |     Līdzekļa lietošanas tiesības        |     Finanšu nomas saistības       |

#### <a name="lease-liability-amortization-interest-expense"></a>Nomas saistību amortizācija (procentu izdevumi) 
Nomas procenti tiek atzīti, aprēķinot procentus nomas sākuma bilancei, perioda nomas maksājumam, procentu aizņēmuma likmei un pievienošanas intervāla periodiem gadā. Procentu summa palielina operatīvās nomas saistību kontu to kreditējot, kas tiks atspoguļots organizācijas bilancē. Darījums ietver arī debeta ierakstu procentu izdevumu kontā, kas atspoguļots finanšu nomu peļņas un zaudējumu aprēķinā, kā arī operatīvo nomu izdevumu kontā.

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operatīvās nomas saistības ieraksts saskaņā ar ASV vispārpieņemtajiem grāmatvedības principiem ASC 842    |     Nomas izdevumi         |     Operatīvās nomas saistības         |
|     Finanšu nomas saistības ieraksts saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem      |     Procentu izdevumi          |     Finanšu nomas saistības           |

#### <a name="accrued-lease-payment"></a>Uzkrātais nomas maksājums
Uzkrātais nomas maksājums tiek atzīts par nomas līdzekļa maksājumu, kas tiek apstrādāts kā maksājuma darījums no bankas vai kases kontiem. Nomas maksājums samazina nomas saistības, debetējot nomas saistību kontu pret, vai nu kreditora apakšgrāmatu, ja iznomātājs ir definēts kā kreditors, vai grāmatojot kredīta pusi parādzīmju maksājumu virsgrāmatas kontā, maksājumu izpildot pret kreditoru vai parādzīmēm.

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operatīvā noma saskaņā ar ASV vispārpieņemtajiem grāmatvedības principiem              |  Operatīvās nomas saistības    |   Kreditoru saistības (apakšgrāmata)/parādzīmes  |
|     Finanšu noma saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem        |  Finanšu nomas saistības      |   Kreditoru saistības (apakšgrāmata)/parādzīmes  |

#### <a name="asset-depreciation"></a>Līdzekļu nolietojums
Līdzekļa lietošanas tiesību nolietojums tiek aprēķināts atkarībā no tā, kurš ir mazāks — līdzekļa lietderīgās lietošanas laiks vai nomas termiņš. ASV vispārpieņemto grāmatvedības principu darbības līzinga (ASC 842) nolietojuma aprēķināšanas metode ir balstīta uz lineārās nomas izdevumu un procentu summas starpību. Finanšu nomas nolietojums tiek aprēķināts, izmantojot standarta lineāro metodi. Nomas nolietojums ietekmē peļņas un zaudējuma aprēķinu, debetējot procentu izdevumus. Bilanci ietekmē finanšu nomu uzkrātais līdzekļa lietošanas tiesību konts. Ja noma ir saistīta ar pamatlīdzekli, nolietojuma darījumi tiks izpildīti tikai no pamatlīdzekļu moduļa. 

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operatīvā noma saskaņā ar ASV vispārpieņemtajiem grāmatvedības principiem              |  Nomas izdevumi                |   Līdzekļa lietošanas tiesību uzkrātais nolietojums     |
|     Finanšu noma saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem        |   Līdzekļa lietošanas tiesību izdevumu amortizācija   |   Līdzekļa lietošanas tiesību uzkrātais nolietojums    |

#### <a name="short-term-lease"></a>Īstermiņa noma
Īstermiņa noma tiek atzīta kā izdevumi, ietekmējot organizācijas peļņas vai zaudējumu aprēķinu. Ģenerētais nomas maksājums debetē nomas izdevumu kontu un kreditē parādzīmes vai kreditora apakšgrāmatas kontu.

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Īstermiņa nomas ieraksts saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem     |  Nomas izdevumi                |   Kreditoru saistības (apakšgrāmata)/parādzīmes  |

#### <a name="low-value-lease"></a>Nelielas vērtības noma
Nelielas vērtības noma tiek atzīta kā izdevumi, kas ietekmē jūsu organizācijas peļņas vai zaudējumu aprēķinu. Ģenerētais nomas maksājums debetē nomas izdevums un kreditē parādzīmes vai kreditora apakšgrāmatas kontu.

|     Veids                                          |     Debetkarte                     |     Kredītkarte                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Nelielas vērtības nomas ieraksts saskaņā ar SFPS un ASV vispārpieņemtajiem grāmatvedības principiem      |  Nomas izdevumi                |   Kreditoru saistības (apakšgrāmata)/parādzīmes  |


#### <a name="index-revaluation"></a>Indeksa pārvērtēšana
Šis ir līdzekļu nomas konts mainīgiem nomas maksājumiem, kas novērtēti ar indeksa likmi. Indeksa likmes svārstību radītās izmaiņas nomas maksājumos veido nomas pielāgojumu saskaņā ar 16. SFPS. Nomas saistības un līdzekļa lietošanas tiesības tiks pielāgotas kontam, ņemtu vērā jaunos maksājumus. 

|     Veids                                          |     Debetkarte                             |     Kredītkarte                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Indeksa pārvērtēšanas ieraksts saskaņā ar SFPS pieauguma gadījumā  |  Līdzekļa lietošanas tiesības       |   Operatīvās nomas saistības |
|   Indeksa pārvērtēšanas ieraksts saskaņā ar SFPS samazinājuma gadījumā  |  Operatīvās nomas saistības  |   Līdzekļa lietošanas tiesības      |

Ja maksājumi mainās indeksa likmes izmaiņu dēļ, mainās tikai mainīgie maksājumi, ja vien nav papildu izmaiņas naudas plūsmās, piemēram, izmaiņas nomas nosacījumos, kas saistīti ar procentu likmēm saskaņā ar ASV vispārpieņemtajiem grāmatvedības principiem ASC 842.

#### <a name="lease-adjustment"></a>Nomas korekcija
Līdzekļu noma ļauj koriģēt nomas, ja tiek mainīti nomas nosacījumi, noma tiek pagarināta vai, ja ir papildu apstākļi, saskaņā ar kuriem nomai ir nepieciešamas korekcijas. Nomas korekcijas tiek grāmatotas, lai palielinātu vai samazinātu līdzekļa lietošanas tiesības un nomas saistības. Korekcijas procesā tiek ņemti vērā saistību amortizācijas un līdzekļu bilances pārnesumu beigu atlikumi korekcijas datumā. Kad noma ir saistīta ar pamatlīdzekli, līdzekļa lietošanas tiesību korekcija tiks grāmatota, izmantojot pamatlīdzekļos piešķirto ID. 

|     Veids                                          |     Debetkarte                             |     Kredītkarte                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Nomas korekciju ieraksts SFPS un ASV vispārpieņemtajiem grāmatvedības principiem pieauguma gadījumā     |  Līdzekļa lietošanas tiesības       |   Operatīvās nomas saistības |
|   Nomas korekciju ieraksts SFPS un ASV vispārpieņemtajiem grāmatvedības principiem samazinājuma gadījumā     |  Operatīvās nomas saistības  |   Līdzekļa lietošanas tiesības      |


#### <a name="lease-impairment"></a>Nomas vērtības samazinājums
Tas atspoguļo līdzekļa lietošanas tiesību bilances pārnesuma samazinājumu. Norādiet vērtības samazinājuma summu, darījuma datumu un atlikušos periodus. Atlikušās līdzekļa lietošanas tiesības tiks amortizēts pēc lineārās metodes. Nomas vērtības samazinājuma loģika ņem vērā līdzekļa pārnešanas vērtību, kas pastāv līdzekļu nolietojuma grafikā.  

|     Veids                                          |     Debetkarte                             |     Kredītkarte                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Vērtības samazinājuma ieraksts SFPS un ASV vispārpieņemtajiem grāmatvedības principiem           |  Vērtības samazinājuma izdevumi                   |    Līdzekļa lietošanas tiesības     |

>[!NOTE]
> Ja noma ir saistīta ar pamatlīdzekli, nomas vērtības samazinājums ir jāgrāmato no pamatlīdzekļiem, jo līdzekļu nolietojums tiek palaists no pamatlīdzekļu moduļa.

**Divkāršā valūta** — nomas darījumi var tikt grāmatoti valūtā, kas nav uzskaites un pārskata valūta. Valūtas maiņas kurss ir definēts virsgrāmatas sākuma datumā. Valūtas maiņas kursus var mainīt, iestatot lauku **Fiksēta likme** uz **Jā**, kad veidojat nomu. Ievadot nomas darījumus, sākotnējās atzīšanas un turpmākie nolietojuma darījumi izmantos valūtas maiņas kursu no sākuma datuma. Turpmākie maksājumu un procentu darījumi izmantos pašreiz aktīvo valūtas maiņas kursu. 

## <a name="create-an-asset-lease"></a>Līdzekļa nomas izveide
Lai izveidotu jaunu nomu, veiciet tālāk norādītās darbības. 

1. Lai izmantotu **Līdzekļu noma**, tas ir jāaktivizē, izmantojot darbvietu **Līdzekļu pārvaldība**. No darbvietas **Līdzekļu pārvaldība** atlasiet **Visi**, lai visi līdzekļi tiktu uzskaitīti lapā. Atlasiet **Līdzekļu noma** un pēc tam atlasiet **Iespējot tūlīt**.
2. Doties uz **Līdzekļu noma > Kopējs > Nomas kopsavilkums**. Kopsavilkuma cilnē **Vispārīgi**, iestatiet obligātos laukus. 
   - **Detalizēta informācija par nomu**
   - **Līdzekļa lietderīgās lietošanas laiks (mēnešos)**
   - **Nomas grupa**
   - **Salīdzināmā aizņēmuma procentu likme (%)**
   - **Pievienošanas intervāls**
   - **Gada maksājuma veids**
   - **Valūta**
   - **Sākuma datums**

3. Dodieties uz kopsavilkuma cilnes **Maksājumu grafika rindas** un ievadiet maksājuma rindu, pēc tam atlasiet **Izveidot grafikus**.

4. Atlasiet **Grāmatas**. 

5. Pārslēdzieties uz kopsavilkuma cilni **Vispārīgi**. Tiek aprēķinātas **Sākotnējās līdzekļa lietošanas tiesības** un **Nomas saistības**. 

6. Kopsavilkuma cilnē dodieties uz **Nomas klasifikācijas tests**, lai pārbaudītu lauka **Nomas veids** vērtību. 

   Automātiski tiek klasificēts **Nomas veids**, pamatojoties uz kritērijiem, kas definēti lapā **Grāmatas**.

7.  Dodieties uz **Maksājumu grafiks** sadaļu **Funkcija**.  

   Lapa **Maksājumu grafiks** norāda turpmākos maksājumu grafikus nomas ID. Atlasiet **Apstiprināt grafiku**, lai varētu grāmatot **Sākotnējās atzīšana** darījumus. 

[![Sākotnējās atzīšanas funkcija](./media/overview-13.png)](./media/overview-13.png)

8. Atlasiet **Sākotnējā atzīšana**, lai izveidotu sākotnējo atzīšanas žurnālu. 

9. Atlasiet **Līdzekļu nomas žurnāls**, lai grāmatotu sākotnējās atzīšanas darbības. 

   No maksājumu grafika varat atvērt informācijas lapu, kas parāda līdzekļa lietošanas tiesību darījumus. 
 
   Procentu summu, kas aprēķināta katram periodam, parāda **Nomas saistību amortizācijas grafiks**.
   
10. Izveidojiet žurnālu un pēc tam dodieties uz **Līdzekļu nomas žurnāls**. Arī procentu darījumi tiek parādīti **Nomas saistību amortizācijas grafikā**.

   Lapa **Līdzekļu nolietojuma grafiks** parāda nolietojuma darbības atlasītajiem nomas ID. 

   [![LLT darījumu lapa](./media/overview-20.png)](./media/overview-20.png)

   Lapa **LLT darījumi** parāda sākotnējo atzīšanu, uzkrāto nolietojumu un līdzekļa bilanci. 

   Lapā **Nomas saistību darījumi** tiek parādīta sākotnēja atzīšana, nomas procentu maksājums, nomas maksājums un nomas saistību bilance. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
