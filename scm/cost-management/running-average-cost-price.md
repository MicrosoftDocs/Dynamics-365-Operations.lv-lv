---
title: "Faktiskā vidējo izmaksu cena"
description: "Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53690038068d7a2cae43585fd2eb896d662ee3e4
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="running-average-cost-price"></a>Faktiskā vidējo izmaksu cena

[!include[banner](../includes/banner.md)]


Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Taču pirms krājumu slēgšanas izpildes sistēmā tiek aprēķināta faktiskā vidējo izmaksu cena, kas parasti tiek izmantota, iegrāmatojot izdošanas transakcijas.

Sistēma novērtē šo esošo vidējo izmaksu cenu par krājumu, izmantojot šādu formulu: 

Novērtētā cena = (Fiziskā summa + Finansiālā summa) ÷ (Fiziskais daudzums + Finansiālais daudzums)

## <a name="using-the-running-average-cost-price"></a>Faktiskās vidējo izmaksu cenas izmantošana
Tālāk esošajā tabulā ir norādīts, kādos gadījumos sistēmā tiek iegrāmatotas krājumu transakcijas, izmantojot faktisko vidējo izmaksu cenu, un kādos gadījumos tās vietā tiek izmantota izmaksu cena, kas ir definēta krājuma šablona ierakstā.

| Nosacījums                                               | Sistēmā tiek izmantota aprēķinātā faktiskā vidējo izmaksu cena | Sistēmā tiek izmantota izmaksu cena, kas ir definēta krājuma šablonā |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Gan skaitītājs\*, gan saucējs\*\* ir pozitīvs skaitlis.  | Jā                                                      | Nav                                                                |
| Gan skaitītājs\*, gan saucējs\*\* ir negatīvi skaitļi. | Nav                                                       | Jā                                                               |
| Saucējs ir\*\* 0 (nulle).                        | Nav                                                       | Jā                                                               |

\* Skaitītājs = (Fiziskā summa + Finansiālā summa) \*\* Saucējs = (Fiziskais daudzums + Finansiālais daudzums) 

**Piezīme.** Ja krājumam nav izvēlēta opcija **Iekļaut fizisko vērtību**, tad sistēma izmanto 0 (nulli) gan fiziskajai summai, gan fiziskajam daudzumam. Informāciju par šo opciju skatiet šeit: [Iekļaut fizisko vērtību](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Paaugstinātas cenas noteikšanas nepieļaušana
Retos gadījumos sistēmā tiek noteikta vairāku izdošanu cena, pirms ir pieejams pietiekams ieejas plūsmu daudzums, pēc kura var noteikt cenu. Šāds scenārijs var izraisīt pārāk augstu faktisko vidējo izmaksu cenas aprēķināšanu. Taču ir pieejamas darbības, kuras var veikt, lai nepieļautu paaugstinātas cenas noteikšanu vai lai samazinātu tās ietekme, ja tas tomēr notiek. **Scenārijs** Tālāk norādītās transakcijas rodas saistībā ar krājumu, kam ir atlasīta opcija **Iekļaut fizisko vērtību**.

1.  Finansiāli tiek saņemts 100 vienību daudzums par cenu USD 100,00.
2.  Finansiāli tiek izdots 200 vienību daudzums.
3.  Fiziski tiek saņemts 101 vienības daudzums par cenu USD 202,00.

Pārbaudot aprēķināto faktisko krājuma vidējo izmaksas cenu, paredzamā izmaksu cena ir USD 1,51. Tās vietā tiek rādīta aprēķinātā faktiskā vidējā cena USD 102,00, kas ir iegūta, izmantojot šādu formulu: aprēķinātā cena = \[202 + (–100)\] ÷ \[101 + (–100)\] = 102 ÷ 1 = 102. Šo cenas palielinājumu izraisa tas, ka tad, kad 2. darbības ietvaros finansiāli tiek izdotas 200 krājuma vienības, sistēmā ir jāaprēķina 100 krājuma vienību cena, pirms ir pieejamas atbilstošas ieejas plūsmas. Šī situācija izraisa negatīvu krājumu. Pēc tam sistēmā tiek aprēķināta vienības cena USD 1,00, kā ir paredzams. Tomēr, saņemot atbilstošo 100 vienību ieejas plūsmas, to vienas vienības cena ir USD 2,00. 

**Piezīme.** Kaut gan plūsmas rada negatīvus krājumus, krājumi ir pozitīvi, kad tiek aprēķināta plūsmas cena. Tādēļ tiek izmantota faktiskā vidējo izmaksas cena, nevis krājuma galvenajā ierakstā. Tagad sistēmā krājumu korespondējošā vērtība ir USD 100,00. Lai gan korespondējošā vērtība tika aprēķināta par 100 vienībām, kur vienas vienības korespondējošā vērtību ir USD 1,00, krājumā ir tikai viena vienība. Tāpēc korespondējošo vērtība USD 100,00 tiek piešķirta šai vienai vienībai. Rezultātā novērtēto izmaksu cena tiek aprēķināta pārāk augsta. 

**Piezīme.** Salīdzinājumam ievērojiet, ka 2. un 3. darbība aprakstītajā scenārijā tiek atsaukta, 200 vienību krājums tiek izsniegts ar vienības cenu USD 1,51 un vienai vienībai saglabājas cena USD 1,51. Tā kā šis paaugstinātās cenas noteikšanas scenārijs var rasties, ja ir iesaistīti negatīvi krājumi, no tās ir grūti izvairīties tālāk minētajos gadījumos.

-   Jānovērtē rīcībā esošo vērtību un daudzumu izejas plūsmas cenas.
-   Jāpielāgo izejas un ieejas plūsmas rīcībā esošās vērtības un daudzumi.
-   Biznesa modelis ļauj izsūtīt vai noteikt cenu vairāk vienībām nekā reāli pastāv.
-   Jāapstiprina visas iesniegtās ienākošās plūsmas vērtības un daudzumi.

Ja biznesa modelis pieļauj tālāk aprakstīto procedūru izmantošanu, tās var palīdzēt izvairīties no daudzuma ar negatīvu vērtību, kas izraisa paaugstinātas cenas noteikšanas scenāriju.

-   Ja krājumam ir atlasīta opcija **Iekļaut fizisko vērtību**, noņemiet izvēles rūtiņas **Negatīvi fiziskie krājumi** atlasi lapā **Krājuma modeļu grupas**.
-   Ja krājumam opcija **Iekļaut fizisko vērtību,** *netiek* atlasīta, noņemiet izvēles rūtiņas **Negatīvi finansiālie krājumi** atlasi lapā **Krājuma modeļu grupas**.

Papildus ņemiet vērā, ka fizisko krājumu maksimālo korespondējošo vērtību ierobežo fizisko transakciju skaits un fiziskās un finanšu cenas starpība. Ar nosacījumu, ka visas fiziskās transakcijas tiek finansiāli atjauninātas, fiziskā vērtība nevar paaugstināties līdz ārkārtas līmenim. Visbeidzot, ņemiet vērā, ka paaugstināšanās efekts būtiski samazinās, ja uzkrātā korespondējošā vērtība tiek piemērota vairākām nevis tikai vienai rīcībā esošajai vienībai.




