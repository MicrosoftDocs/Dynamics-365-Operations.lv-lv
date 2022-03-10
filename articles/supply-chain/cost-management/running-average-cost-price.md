---
title: Faktiskā vidējo izmaksu cena
description: Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092193"
---
# <a name="running-average-cost-price"></a>Faktiskā vidējo izmaksu cena

[!include [banner](../includes/banner.md)]

Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas.

Sistēma novērtē šo esošo vidējo izmaksu cenu par krājumu, izmantojot šādu formulu:

Novērtētā cena = (Fiziskā summa + Finansiālā summa) ÷ (Fiziskais daudzums + Finansiālais daudzums)

## <a name="default-item-cost"></a>Noklusējuma preces izmaksas

Izlaista produkta noklusējuma preces izmaksas var konfigurēt vienā no diviem veidiem **Izlaista produkta informācija** lappuse:

- Izveidojiet standarta maksu, atlasot **Preces cena** iekš **Uzstādīt** grupa uz **Pārvaldiet izmaksas** Darbības rūts cilne. Ja izmantojat šo metodi, jums ir jāizmanto standarta izmaksu izmaksu versija, un maksa ir jāaktivizē.
- Definējiet izlaista produkta noklusējuma preces pašizmaksu, ievadot vērtību laukā **Cena** lauks uz **Pārvaldiet izmaksas** FastTab.

Papildus cenas ievadīšanai vai izveidošanai varat atlasīt **Izmantojiet jaunāko pašizmaksu** izvēles rūtiņa uz **Pārvaldiet izmaksas** FastTab of the **Izlaista produkta informācija** lappuse. Šādā gadījumā sistēma automātiski atjauninās **Cena** publicējot finanšu atjauninājumu. Piemēram, ja ievietojat pirkuma pasūtījuma rēķinu, laukā tiks iestatīta pirkuma cena no šī rēķina.

Ja jums ir izmaksu cena aktīvajā izmaksu aprēķināšanas versijā un jūs ievadāt cenu uz **Pārvaldiet izmaksas** FastTab, sistēma izmantos cenu no aktīvās izmaksu aprēķināšanas versijas, pirms tā izmantos cenu, kas definēta **Pārvaldiet izmaksas** FastTab.

## <a name="using-the-running-average-cost-price"></a>Faktiskās vidējo izmaksu cenas izmantošana

Tālāk esošajā tabulā ir norādīts, kādos gadījumos sistēmā tiek iegrāmatotas krājumu transakcijas, izmantojot faktisko vidējo izmaksu cenu, un kādos gadījumos tās vietā tiek izmantota izmaksu cena, kas ir definēta krājuma šablona ierakstā.

| Nosacījums | Sistēmā tiek izmantota aprēķinātā faktiskā vidējo izmaksu cena | Sistēma izmanto noklusējuma preces pašizmaksu |
| --- | --- | --- |
| Gan skaitītājs\*, gan saucējs\*\* ir pozitīvs skaitlis. | Jā | Nē |
| Gan skaitītājs\*, gan saucējs\*\* ir negatīvi skaitļi. | Nē | Jā |
| Saucējs ir\*\* 0 (nulle). | Nē | Jā |

\* Skaitītājs = (fiziskā summa + finanšu summa)  
\*\* Saucējs = (fiziskais daudzums + finanšu daudzums)

> [!NOTE]
> Ja **Iekļaujiet fizisko vērtību** opcija precei nav atlasīta, sistēma izmanto 0 (nulle) gan fiziskajam, gan fiziskajam daudzumam. Informāciju par šo opciju skatiet šeit: [Iekļaut fizisko vērtību](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Paaugstinātas cenas noteikšanas nepieļaušana

Retos gadījumos sistēmā tiek noteikta vairāku izdošanu cena, pirms ir pieejams pietiekams ieejas plūsmu daudzums, pēc kura var noteikt cenu. Šāds scenārijs var izraisīt pārāk augstu faktisko vidējo izmaksu cenas aprēķināšanu. Taču ir pieejamas darbības, kuras var veikt, lai nepieļautu paaugstinātas cenas noteikšanu vai lai samazinātu tās ietekme, ja tas tomēr notiek.

**Scenārijs:** Tālāk norādītās transakcijas notiek ar vienumu, kuru esat atlasījis **Iekļaujiet fizisko vērtību** opcija priekš:

1. Finansiāli tiek saņemts 100 vienību daudzums par cenu USD 100,00.
2. Finansiāli tiek izdots 200 vienību daudzums.
3. Fiziski tiek saņemts 101 vienības daudzums par cenu USD 202,00.

Pārbaudot aprēķināto faktisko krājuma vidējo izmaksas cenu, paredzamā izmaksu cena ir USD 1,51. Tā vietā jūs atradīsit aptuveno tekošo vidējo vērtību USD 102.00, kuras pamatā ir šāda formula:

Paredzamā cena =\[ 202 + (-100)\] ÷\[ 101 + (-100)\] = 102 ÷ 1 = 102

Šis cenu pastiprinājums rodas tāpēc, ka, 2. darbībā finansiāli izsniedzot 200 vienības, sistēmai ir jānosaka cena par 100 precēm, pirms tai ir saņemti atbilstoši ieņēmumi. Šī situācija izraisa negatīvu krājumu. Pēc tam sistēma aprēķina vienības cenu USD 1.00, kā jūs varētu gaidīt. Tomēr, saņemot atbilstošo 100 vienību ieejas plūsmas, to vienas vienības cena ir USD 2,00.

> [!NOTE]
> Lai gan emisijas rada negatīvu krājumu, krājumi ir pozitīvi, kad tiek aprēķināta emisijas cena. Tādēļ tiek izmantota faktiskā vidējo izmaksas cena, nevis krājuma galvenajā ierakstā. Tagad sistēmā krājumu korespondējošā vērtība ir USD 100,00. Lai gan šī nobīde tika izveidota vairāk nekā 100 vienību, kur katrai bija USD 1.00 vienības nobīde, tagad jums ir tikai viena vienība. Tāpēc korespondējošo vērtība USD 100,00 tiek piešķirta šai vienai vienībai. Rezultātā novērtēto izmaksu cena tiek aprēķināta pārāk augsta.
>
> Salīdzinājumam ņemiet vērā: ja scenārijā 2. un 3. darbība tiek mainīta, 200 vienības tiks izsniegtas par vienības cenu USD 1.51, bet viena vienība paliks par vienības cenu USD 1.51. Tā kā šis paaugstinātās cenas noteikšanas scenārijs var rasties, ja ir iesaistīti negatīvi krājumi, no tās ir grūti izvairīties tālāk minētajos gadījumos.
>
> - Jānovērtē rīcībā esošo vērtību un daudzumu izejas plūsmas cenas.
> - Jāpielāgo izejas un ieejas plūsmas rīcībā esošās vērtības un daudzumi.
> - Biznesa modelis ļauj izsūtīt vai noteikt cenu vairāk vienībām nekā reāli pastāv.
> - Jāapstiprina visas iesniegtās ienākošās plūsmas vērtības un daudzumi.

Ja biznesa modelis pieļauj tālāk aprakstīto procedūru izmantošanu, tās var palīdzēt izvairīties no daudzuma ar negatīvu vērtību, kas izraisa paaugstinātas cenas noteikšanas scenāriju.

- Ja izvēlaties **Iekļaujiet fizisko vērtību** vienuma opciju, notīriet **Fiziski negatīvs inventārs** izvēles rūtiņa uz **Preču modeļu grupas** lappuse.
- Ja krājumam opcija **Iekļaut fizisko vērtību,** **netiek** atlasīta, noņemiet izvēles rūtiņas **Negatīvi finansiālie krājumi** atlasi lapā **Krājuma modeļu grupas**.

Papildus ņemiet vērā, ka fizisko krājumu maksimālo korespondējošo vērtību ierobežo fizisko transakciju skaits un fiziskās un finanšu cenas starpība. Ar nosacījumu, ka visas fiziskās transakcijas tiek finansiāli atjauninātas, fiziskā vērtība nevar paaugstināties līdz ārkārtas līmenim. Visbeidzot, ņemiet vērā, ka paaugstināšanās efekts būtiski samazinās, ja uzkrātā korespondējošā vērtība tiek piemērota vairākām nevis tikai vienai rīcībā esošajai vienībai.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Izvairieties no nulles pašizmaksas problēmām

Kad **Iekļaujiet fizisko vērtību** opcija nav atlasīta **Preču modeļu grupa** lapā, krājumu problēmai var būt nulles pašizmaksa, ja krājumos nav finansiāli atjauninātu kvīšu. Lai izvairītos no šī scenārija, apsveriet tālāk norādītās iespējas.

- Izvēlieties **Iekļaujiet fizisko vērtību** opcija uz **Preču modeļu grupa** lappuse. Šī opcija novērsīs nulles pašizmaksu par problēmu, ja kvīts tiek fiziski atjaunināta. Ja neatļausiet negatīvus fiziskos krājumus, problēmas aprēķinās vidējo vidējo vērtību no fiziski atjauninātajiem darījumiem.
- Izveidojiet noklusējuma preces pašizmaksu, aktivizējot izmaksu aprēķināšanas versiju, kurai ir standarta izmaksas, vai ievadiet cenu **Pārvaldiet izmaksas** FastTab of the **Izlaista produkta informācija** lappuse. Šī opcija ir vislabākā, ja **Iekļaujiet fizisko vērtību** opcija nav atlasīta **Preču modeļu grupa** lapu, jo sistēmai vienmēr būs jāizmanto rezerves cena.
- Izvēlieties **Izmantojiet jaunāko pašizmaksu** opcija uz **Pārvaldiet izmaksas** FastTab of the **Izlaista produkta informācija** lappuse. Šī opcija saglabās **Cena** lauks tiek atjaunināts katru reizi, kad finansiāli atjaunināt kvīti. Ja atlasāt šo opciju, bet neievadāt noklusējuma cenu vai neaktivizējat maksu standarta izmaksu aprēķināšanas versijā, jums joprojām var būt nulles maksa par problēmu.

Ja jums ir darījumu darījumi ar nulles izmaksām, *Inventāra slēgšana un regulēšana* process koriģēs pašizmaksu, izveidojot korekciju pēc čeku finansiālās atjaunināšanas. Ņemiet vērā, ka finanšu periods, kurā tiek veikts šis atjauninājums, var atšķirties no finanšu perioda, kad preces tika fiziski saņemtas vai izdotas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
