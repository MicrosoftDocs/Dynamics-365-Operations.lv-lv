---
title: "Faktiskā vidējo izmaksu cena"
description: "Krājumu tuvu process atrisina saņemšanas darbībām, pamatojoties uz krājumu novērtēšanas metode, kas atlasīts preču modeļa grupas krājuma izejas plūsmas darbībām. Tomēr pirms krājumu tuvu darboties, sistēma aprēķina darbojas vidējās izmaksu cenas, kas parasti tiek lietota, kad jautājums tiek grāmatotas."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Faktiskā vidējo izmaksu cena

Krājumu tuvu process atrisina saņemšanas darbībām, pamatojoties uz krājumu novērtēšanas metode, kas atlasīts preču modeļa grupas krājuma izejas plūsmas darbībām. Tomēr pirms krājumu tuvu darboties, sistēma aprēķina darbojas vidējās izmaksu cenas, kas parasti tiek lietota, kad jautājums tiek grāmatotas.

Sistēmas aprēķiniem tas darbojas vidējā izmaksu cena krājumam, izmantojot šādu formulu: paredzamā cena = (fiziskais apjoms + finanšu apjoms) ÷ (fiziskais daudzums + finanšu daudzuma)

## <a name="using-the-running-average-cost-price"></a>Faktiskās vidējo izmaksu cenas izmantošana
Tabulā ir redzams, kad sistēma grāmato krājumu darbības, izmantojot darbojas vidējās izmaksu cenas, un, kad tā izmanto izmaksu cenu, kas ir definēts krājumu šablona ieraksta vietā.

| Nosacījums                                               | Sistēma izmanto paredzamo darbojas vidējās izmaksu cenas | Sistēma izmanto izmaksu cenu, kas ir definēts krājumu šablonā. |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Gan skaitītājs\* un saucējs\*\* ir pozitīvi.  | Jā                                                      | Nav                                                                |
| Numerators\*, saucējs\*\*, vai abas ir negatīvs. | Nav                                                       | Jā                                                               |
| Saucējs\*\* ir 0 (nulle).                        | Nav                                                       | Jā                                                               |

\*Numerators = (fiziskais apjoms + finanšu apjoms) \*\*saucējs = (fiziskais daudzums + finanšu daudzuma) **Piezīme:** ja **iekļaut fizisko vērtību** opcija nav atlasīts krājumam, sistēma izmanto 0 (nulle), gan fiziskā apjoma, gan fizisko daudzumu. Informāciju par šo opciju skatiet šeit: [Iekļaut fizisko vērtību](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Paaugstinātas cenas noteikšanas nepieļaušana
Retos gadījumos sistēma cenas vairākus jautājumus, pirms tai ir pietiekami apliecinājumi par pamatu cenu. Šāds scenārijs var izraisīt pārāk augstu faktisko vidējo izmaksu cenas aprēķināšanu. Taču ir pieejamas darbības, kuras var veikt, lai nepieļautu paaugstinātas cenas noteikšanu vai lai samazinātu tās ietekme, ja tas tomēr notiek. **Scenārijs** Tālāk norādītās transakcijas rodas saistībā ar krājumu, kam ir atlasīta opcija **Iekļaut fizisko vērtību**.

1.  Finansiāli tiek saņemts 100 vienību daudzums par cenu USD 100,00.
2.  Finansiāli tiek izdots 200 vienību daudzums.
3.  Fiziski tiek saņemts 101 vienības daudzums par cenu USD 202,00.

Pārbaudot aprēķināto faktisko krājuma vidējo izmaksas cenu, paredzamā izmaksu cena ir USD 1,51. Tā vietā jūs atradīsiet lēstajiem darbojas vidējās USD 102.00, kas ir pamatota uz šādu formulu: paredzamā cena = \[202 + -(100)\] ÷ \[101 + -(100)\] = 102 ÷ 1 = 102 šo cenu pastiprinājums rodas tāpēc, ka, izdodot 200 krājumi ir finansiāli 2 soli, sistēmai jābūt cenu 100 krājumi pirms tā ir jebkādus atbilstošos ieņēmumus. Šī situācija izraisa negatīvu krājumu. Sistēma pēc tam lēš vienības cenu, par USD 1.00, kā mēs varētu sagaidīt. Tomēr, saņemot atbilstošo 100 vienību ieejas plūsmas, to vienas vienības cena ir USD 2,00. **Piezīme.** Kaut gan plūsmas rada negatīvus krājumus, krājumi ir pozitīvi, kad tiek aprēķināta plūsmas cena. Tādēļ tiek izmantota faktiskā vidējo izmaksas cena, nevis krājuma galvenajā ierakstā. Šajā brīdī sistēma ir krājumu vērtības nobīde no USD 100.00. Lai gan korespondējošā vērtība tika aprēķināta par 100 vienībām, kur vienas vienības korespondējošā vērtību ir USD 1,00, krājumā ir tikai viena vienība. Tāpēc korespondējošo vērtība USD 100,00 tiek piešķirta šai vienai vienībai. Rezultātā novērtēto izmaksu cena tiek aprēķināta pārāk augsta. **Piezīme.** Salīdzinājumam ievērojiet, ka 2. un 3. darbība aprakstītajā scenārijā tiek atsaukta, 200 vienību krājums tiek izsniegts ar vienības cenu USD 1,51 un vienai vienībai saglabājas cena USD 1,51. Tā kā šis paaugstinātās cenas noteikšanas scenārijs var rasties, ja ir iesaistīti negatīvi krājumi, no tās ir grūti izvairīties tālāk minētajos gadījumos.

-   Jānovērtē rīcībā esošo vērtību un daudzumu izejas plūsmas cenas.
-   Jāpielāgo izejas un ieejas plūsmas rīcībā esošās vērtības un daudzumi.
-   Biznesa modelis ļauj izsūtīt vai noteikt cenu vairāk vienībām nekā reāli pastāv.
-   Jāapstiprina visas iesniegtās ienākošās plūsmas vērtības un daudzumi.

Ja biznesa modelis pieļauj tālāk aprakstīto procedūru izmantošanu, tās var palīdzēt izvairīties no daudzuma ar negatīvu vērtību, kas izraisa paaugstinātas cenas noteikšanas scenāriju.

-   Ja krājumam ir atlasīta opcija **Iekļaut fizisko vērtību**, noņemiet izvēles rūtiņas **Negatīvi fiziskie krājumi** atlasi lapā **Krājuma modeļu grupas**.
-   Ja krājumam opcija **Iekļaut fizisko vērtību,** *netiek* atlasīta, noņemiet izvēles rūtiņas **Negatīvi finansiālie krājumi** atlasi lapā **Krājuma modeļu grupas**.

Papildus ņemiet vērā, ka fizisko krājumu maksimālo korespondējošo vērtību ierobežo fizisko transakciju skaits un fiziskās un finanšu cenas starpība. Ar nosacījumu, ka visas fiziskās transakcijas tiek finansiāli atjauninātas, fiziskā vērtība nevar paaugstināties līdz ārkārtas līmenim. Visbeidzot, ņemiet vērā, ka paaugstināšanās efekts būtiski samazinās, ja uzkrātā korespondējošā vērtība tiek piemērota vairākām nevis tikai vienai rīcībā esošajai vienībai.


