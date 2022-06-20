---
title: Grāmatot izmaksu konta uzskaites principu
description: Šajā rakstā sniegts pārskats par grāmatvedību konta uzskaites principam.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 998a30786b3f457b24b6e3c755b2c00967adbd4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879168"
---
# <a name="post-to-charge-account-accounting-principle"></a>Grāmatot izmaksu konta uzskaites principu

Grāmatošanas *konta uzskaites* princips ļauj jums konts un vieglāk saskaņot visas atšķirības, kas rodas vienības cenā starp fizisku grāmatošanu un finanšu grāmatošanu, iegādāto krājumu netiešajām izmaksām vai pirkšanas pasūtījuma maksām. 

Divas konfigurācijas Kreditoru maksu kodiem **maksu** kodu lapā (**\>\> Kreditoru maksu iestatījuma maksu kods**) var radīt pirkšanas pasūtījumu, kas ietekmē krājumu līdzekļu novērtēšanu:

- Papildmaksu **kodiem** *·* **·** *·*, kur lauka Debeta tips iestatījums ir Krājums un Lauks Kredīta tips ir iestatīts uz Virsgrāmatas kontu. Virsgrāmatas konts, kas atlasīts kā izmaksu konts, darbojas kā krājumu variācijas konts.
- Papildmaksu **kodiem** *·* **·** *, kur lauks Debeta tips ir iestatīts uz Krājums un Lauks Kredīta tips ir iestatīts uz Debitors/* Kreditors, maksa tiks novērtēta kā materiālu izmaksas un krājuma krājumu variācijas konts tiks izmantots.

## <a name="european-special-accounting-rule"></a>Eiropas īpašais uzskaites noteikums

Eiropā principu "grāmatot *, lai iekasētu* maksu no uzskaites" bieži izmanto, lai iekļautu īpašu uzskaites nosacījumu. Piemēram, krājumu izmaiņu uzskaitei parasti tiek izmantota viena no šīm metodēm:

- **Pārdošanas metodes izmaksas** – standarta krājumu grāmatošanas metodes konfigurācija atbalsta šo metodi. Nav *nepieciešams grāmatošanas* maksas konta uzskaites princips.
- **Izdevumu metodes raksturs –** mazākās organizācijas bieži izmanto šo metodi. Parasti tas ietver tālāk norādītās darbības.

    1. Saņemšanas laikā preces vai pakalpojumi pilnībā tiek pilnībā saistīti ar izdevumiem.
    2. Perioda beigās tiek veikta cikla inventarizācija.
    3. Manuāla daudzuma un vērtības korekcija, kas grāmatota krājumos. (Korespondējošais konts ir krājumu novirzes konts, kas korespondē izdevumus, kas tika iegrāmatoti 1. darbībā. Tāpēc jūs redzat krājumu vērtības izmaiņas tikai šajā kontā.)

Grāmatošanas *uz maksu konta* princips ļauj jums pilnībā automatizēt abus grāmatojumus. Šādā veidā var koriģēt manuālo perioda beigu slēgšanas korekciju grāmatojumu.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Iespējot grāmatošanas konta uzskaites principu

Lai iespējotu grāmatošanas *konta uzskaites principu*, sekojiet šiem soļiem.

1. Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
2. Cilnes Rēķins **kopsavilkuma** cilnē Rēķins **iestatiet** opciju Grāmatot **virsgrāmatas izmaksu kontā** uz *Jā*.
3. Aizvērt lapu.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Priekšnoteikumi un ieteicamie parametri grāmatošanas izmaksu konta uzskaites principam

Ja plānojat ņemt vērā pirkšanas izmaksas un krājumu novirzes, jābūt šādiem priekšnoteikumiem:

- Kreditoru parametru **lapas** **·** **\>\>** **(** Parādi kreditoriem iestatījuma Parādi kreditoriem parametri) cilnē Rēķins opcijai Grāmatot virsgrāmatas maksas kontā jābūt iestatītai uz *Jā.*
- Lapā Krājumu **modeļu grupas** (**\>\>** Izmaksu pārvaldība Krājumu uzskaites politiku iestatījums Krājumu modeļu grupas) *visām* atbilstošām modeļu grupām, kas ietver krājumus, kas iekļauti pirkšanas pasūtījumā, ir jāiestata visas tālāk norādītās opcijas:

    - Grāmatot fiziskos krājumus
    - Grāmatot finanšu krājumus
    - Uzkrājumu saistības produktu ieejas plūsmā

- **Sagādes un** avotu **parametru** lapas cilnē Piegāde (**Sagādes \>\>** un avotu iestatīšanas sagādes un avotu parametri) **opcijai** Ģenerēt produktu ieejas plūsmas maksas ir jābūt iestatītai uz *Jā.*
- Cilnes Krājumu **uzskaite lapā** **Krājumu** un noliktavas pārvaldības parametri (**\>\>** Krājumu vadības iestatījuma krājumu un noliktavas vadības parametri) **opcijai** Grāmatot pavadzīmi Virsgrāmatā jābūt iestatītai uz *Jā.*
- **Grāmatošanas lapas cilnē** Pirkšanas **pasūtījums** (**\> Krājumu vadības iestatījumu \>\>** grāmatošanas grāmatošana), galvenie konti, kas attiecas uz katru atbilstošo krājumu, jānorāda katram no šiem grāmatošanas tipiem:

    - Pirkšanas izdevumi, kas nav iekļauti rēķinos
    - Produkta pirkšanas izdevumi
    - Krājumu novirze

## <a name="example-scenario-1-change-in-unit-cost-price"></a>1. scenārijs: izmaiņas vienības izmaksu cenā

Šī piemēra scenārijam ir šādi priekšnosacījumi:

- Izmaksu aprēķināšanas modelis "Pirmais ārā", "pirmais ārā" (First in, first out – FIFO)

Šajā procedūrā sniegts piemērs, kas parāda, kas notiek, ja pirkšanas pasūtījumā maināt vienības izmaksu cenu.

1. Izveidojiet pirkšanas pasūtījumu daudzumam 1 krājumam ar vienības cenu 100,00.
2. Apstipriniet pirkšanas pasūtījumu.
3. Grāmatojiet produktu ieejas plūsmu pirkšanas pasūtījumam.
4. Pārbaudīt dokumentu produktu ieejas plūsmā. Tabulā ir parādīts parauga dokuments.

    | Grāmatošanas tips | Galvenais konts | Galvenā konta nosaukums | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Vai fiziskais/finanšu? | Summa |
    |---|---|---|---|---|---|---|---|
    | Pirkšana, krājumu novirze | 600170 | Krājumu novirzes materiāli | Izdevumi | Kredīts | Nē | Fizisks | -100,00 |
    | Saņemto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Jā | Fizisks | 100.00 |
    | Pirkšanas izdevumi, kas nav iekļauti rēķinos | 600180 | Materiālu ieejas plūsmas | Izdevumi | Debets | Jā | Fizisks | 100.00 |
    | Pirkšana, uzkrāšana | 200140 | Uzkrātie pirkšanas pasūtījumi | Saistības | Kredīts | Jā | Fizisks | -100,00 |

5. Grāmatojiet rēķinu pirkšanas pasūtījumam, kas atjaunina vienības cenu 110,00.
6. Pārbaudiet dokumentu rēķinā. Tabulā ir parādīts parauga dokuments.

    | Grāmatošanas tips | Galvenais konts | Galvenā konta nosaukums | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Vai fiziskais/finanšu? | Summa |
    |---|---|---|---|---|---|---|---|
    | Pirkšana, krājumu novirze | 600170 | Krājumu novirzes materiāli | Izdevumi | Kredīts | Nē | Finanšu | -10,00 |
    | Saņemto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Jā | Finanšu | -100,00 |
    | Pirkšanas izdevumi, kas nav iekļauti rēķinos | 600180 | Materiālu ieejas plūsmas | Izdevumi | Debets | Jā | Finanšu | -100,00 |
    | Pirkšana, uzkrāšana | 200140 | Uzkrātie pirkšanas pasūtījumi | Saistības | Kredīts | Jā | Finanšu | 100.00 |
    | Rēķinā iekļauto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Nē | Finanšu | 110.00 |
    | Produkta pirkšanas izdevumi | 600180 | Materiālu ieejas plūsma | Izdevumi | Kredīts | Nē | Finanšu | 110.00 |
    | Kreditora bilance | 211000 | Parādi kreditoriem tirdzniecība | Saistības | Kredīts | Nē | Finanšu | -110.00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>2. piemērs: maksas un netiešās izmaksas pirkšanas pasūtījumā

Šī piemēra scenārijam ir šādi priekšnosacījumi:

- FIFO izmaksu aprēķināšanas modelis
- **1. papildmaksu kods:** 10% debeta krājumu un kredīta Virsgrāmatas konts
- **2. izmaksu kods: debeta** krājums un kredīta debitors/kreditors par 10,00 proporcionālu
- **Netiešās izmaksas:** 2,00% pievienotas pirkšanas cenai

Šajā procedūrā sniegts piemērs, kas parāda, kas notiek, ja pirkšanas pasūtījumā tiek iekļautas maksas un netiešās izmaksas.

1. Izveidojiet pirkšanas pasūtījumu daudzumam 1 krājumam ar vienības cenu 100,00.
2. Pievienojiet vienu izmaksu kodu 10 procentiem, kas debetē krājumu un kreditē Virsgrāmatu.
3. Pievienojiet vienu papildmaksu kodu 10,00, kas debetē krājumu un kreditē debitoru/kreditoru.
4. Piešķiriet maksas pirkšanas pasūtījuma rindām.
5. Apstipriniet pirkšanas pasūtījumu.
6. Grāmatojiet produktu ieejas plūsmu pirkšanas pasūtījumam.
7. Pārbaudīt dokumentu produktu ieejas plūsmā. Tabulā ir parādīts parauga dokuments.

    | Grāmatošanas tips | Galvenais konts | Galvenā konta nosaukums | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Fiziska vai finanšu | Summa |
    |---|---|---|---|---|---|---|---|
    | Pirkšana, krājumu novirze | 600170 | Krājumu novirzes materiāli | Izdevumi | Kredīts | Nē | Fizisks | -110.00 |
    | Plānotās piesaistītās netiešās izmaksas | 600520 | Iesvērtās netiešās izmaksas | Izdevumi | Kredīts | Jā | Fizisks | -2.40 |
    | Pirkuma transportēšanas izdevumi | 600120 | Kravas pārvadāšanas/transportēšanas izmaksas | Izdevumi | Kredīts | Nē | Fizisks | -10,00 |
    | Saņemto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Jā | Fizisks | 122.40 |
    | Pirkšanas izdevumi, kas nav iekļauti rēķinos | 600180 | Materiālu ieejas plūsmas | Izdevumi | Debets | Jā | Fizisks | 110.00 |
    | Pirkšana, uzkrāšana | 200140 | Uzkrātie pirkšanas pasūtījumi | Saistības | Kredīts | Jā | Fizisks | -110.00 |

8. Grāmatojiet pirkšanas pasūtījuma rēķinu.
9. Pārbaudiet dokumentu rēķinā. Tabulā ir parādīts parauga dokuments.

    | Grāmatošanas tips | Galvenais konts | Galvenā konta nosaukums | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Vai fiziskais/finanšu? | Summa |
    |---|---|---|---|---|---|---|---|
    | Pirkšana, krājumu novirze | 600170 | Krājumu novirzes materiāli | Izdevumi | Kredīts | Nē | Finanšu | 0,00 |
    | Plānotās piesaistītās netiešās izmaksas | 600520 | Iesvērtās netiešās izmaksas | Izdevumi | Debets | Jā | Finanšu | 2.40 |
    | Piesaistītās netiešās izmaksas | 600520 | Iesvērtās netiešās izmaksas | Izdevumi | Debets | Nē | Finanšu | -2.40 |
    | Saņemto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Kredīts | Jā | Finanšu | -110.00 |
    | Pirkšanas izdevumi, kas nav iekļauti rēķinos | 600180 | Materiālu ieejas plūsmas | Izdevumi | Kredīts | Jā | Finanšu | -110.00 |
    | Pirkšana, uzkrāšana | 200140 | Uzkrātie pirkšanas pasūtījumi | Saistības | Debets | Jā | Finanšu | 110.00 |
    | Rēķinā iekļauto pirkto materiālu izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Debets | Nē | Finanšu | 110.00 |
    | Produkta pirkšanas izdevumi | 600180 | Materiālu ieejas plūsma | Izdevumi | Kredīts | Nē | Finanšu | 110.00 |
    | Kreditora bilance | 211000 | Parādi kreditoriem tirdzniecība | Saistības | Kredīts | Nē | Finanšu | -110.00 |
