---
title: Trīsvirzienu atbilstības ierobežojumi
description: Šajā rakstā ir sniegti trīsvirzienu atbilstības piemēri.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6d98164766e81625bd9eeb9e504e5f0683151e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904935"
---
# <a name="three-way-matching-policies"></a>Trīsvirzienu atbilstības ierobežojumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti trīsvirzienu atbilstības piemēri.

## <a name="example-three-way-matching-for-items"></a>Piemērs: krājumu trīsvirzienu atbilstība

**Kopsavilkums.** Kens ir kontrolieris juridiskas personas Fabrikam galvenajā birojā. Kens izlemj, ka visiem kreditora rēķiniem, kuru pamatā ir pirkšanas pasūtījumi, ir jānosaka atbilstība pirkšanas pasūtījumu rindām (divvirzienu atbilstība). Tādu krājumu pirkumu rēķiniem, kas tiks izmantoti kā pamatlīdzekļi, ir jānosaka atbilstība gan pirkšanas pasūtījumu rindām, gan produktu ieejas plūsmas dokumenta rindām (trīsvirzienu atbilstība).

Fabrikam vada vairākas juridiskās personas un nodarbina darbiniekus visā pasaulē. Palielinoties transakciju apjomam, palielinās arī ieejas plūsmu un rēķinu neatbilstības. Tas izraisa līdzekļu norakstīšanu. Kreditoru rēķini tiek apmaksāti, taču šī procesa laikā netiek noteiktas neatbilstības gadījumā, ja tiek saņemts mazāk krājumu, nekā tika pasūtīts, vai krājumi netiek saņemti vispār. Palielinās arī izdevumi, jo darbiniekiem darbu veikšanai joprojām ir nepieciešami rīki un citiem materiāli. Kens vēlas pārliecināties, ka kreditori nosūta pasūtītās preces un tās saņem Fabrikam darbinieki. Tāpēc Kenam ir jāizmanto divvirzienu un trīsvirzienu atbilstības metodes visām organizācijas juridiskajām personām. Rēķinu salīdzināšana palīdz nodrošināt, ka var izsekot un atrisināt ar pazudušiem vai nesaņemtiem krājumiem saistītas problēmas. 

Šajā piemērā ietvertie rēķinu salīdzināšanas atbilstības ierobežojumi palīdz personām tālāk norādītajos amatos sasniegt savus mērķus.

-   Kens ir kontrolieris uzņēmumā Fabrikam. Kens var palīdzēt personām organizācija noteikt un atrisināt problēmas, kas ir saistītas ar kreditoru nodrošināto krājumu (preču un pakalpojumu) pasūtīšanu, saņemšanu un maksāšanu par tiem.
-   Filisa un Eiprila ir Fabrikam ASV nodaļas kreditoru departamenta grāmatvedības daļas vadītājas. Viņas var ieviest uzņēmuma politiku un nodrošināt, ka visi rēķini tiek apmaksāti tikai pēc tam, kad tiek noteikta to atbilstība pirkšanas pasūtījumiem un preču un pakalpojumu ieejas plūsmas dokumentiem, ja tas ir attiecināms.
-   Tonijs ir Fabrikam ASV nodaļas ražošanas daļas vadītājs. Tonijs un citi ražošanas daļas darbinieki var nodrošināt, ka tiek saņemti no kreditoriem pasūtītie krājumi un tie tiek reģistrēti, lai darbinieki saņemtu darba veikšanai nepieciešamos rīkus un materiālus.

### <a name="prerequisites"></a>Priekšnosacījumi

-   Plkst. 1. **iestata** atbilstības ierobežojumus juridiskas personas līmenī kā **Trīsvirziena sakritības**.
-   Iestata juridisko personu **kā Jā automātiski** atjaunināt virsraksta atbilstības **statusu**.
-   Plkst. iestata **saskaņotās cenas kopsummu** **lauku juridiskajai personai kā procentuālo vērtību un ievada 15% kā** Tolerances **procentus**.
-   Krājuma 1500 – CNC iestatījuma atbilstības ierobežojumi krājuma līmenī tiek iestatīti uz trīskāršotu **sakritības veidu**. Šis krājums ir līdzeklis, kas tiek izmantots ražošanai uzņēmumā Fabrikam. Tiek noteikta šo krājuma rēķinu atbilstība pirkšanas pasūtījuma rindām, salīdzinot cenas, un ar produktu ieejas plūsmas dokumentiem, salīdzinot daudzumus.
-   Tonijs iesniedz pieprasījumu piecu CNC Milicron mašīnu saņemšanai. Alīsija, Fabrikam pirkšanas pasūtījumu nodaļas darbiniece, izsniedz pirkšanas pasūtījumu juridiskai personai Contoso par krājumu piegādi.

    | Krājuma kods                 | Daudzums | Vienības cena | Neto summa | Maksas kods        | Izmaksu vērtība |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 — CNC Milicron mašīna | 5.        | 8000,00   | 40 000,00  | Sūtīšana un apstrāde | 3000,00      |

-   Ārnijs, Contoso debitoru parādu nodaļas darbinieks, pārskata nedēļas laikā veicamos sūtījumus. Ārnijs atlasa sūtīšanas transakcijas, lai izrakstītu uzņēmumam Fabrikam rēķinu par CNC Milicron mašīnu piegādi. Ārnijs ietver maksu par sūtīšanu un apstrādi. Uzņēmums Fabrikam uzskatīs, ka šī maksa ir ietverta līdzekļa cenā.

### <a name="scenario"></a>Scenārijs

1.  Samijs, Fabrikam saņemšanas nodaļas darbinieks, saņem visas no Contoso nosūtītās mašīnas. Samijs ievada daudzumu 5 produktu ieejas plūsmas dokumentā. Tā kā pirkšanas pasūtījums ir pilnībā saņemts, pirkšanas pasūtījuma statuss tiek mainīts uz Saņemts.
2.  Eiprila, Fabrikam kreditoru nodaļas koordinatore, ievada un pārbauda uzņēmuma Contoso iesniegto rēķinu. Viņa pārbauda tālāk norādīto informāciju.
    -   Krājumiem, kuriem ir nepieciešama trīsvirzienu atbilstība, rēķina rindā norādītais daudzums atbilst saņemtajam daudzumam. Saņemtais daudzums ir norādīts produktu ieejas plūsmas dokumentā, kas tiek salīdzināts ar rēķinu.
    -   Krājumiem, kam nepieciešama divvirzienu vai trīsvirzienu atbilstība, cenas rēķina rindā ietilpst toleranci, kas definēta Microsoft Dynamics 365 Finansēs. Tas attiecas uz tālāk norādītajiem cenu salīdzināšanas tipiem.
        -   Vienības neto cenu salīdzināšana — rēķina rindā norādītā vienības neto cena atbilst pirkšanas pasūtījuma rindā norādītajai vienības neto cenai saskaņā ar pielaides procentuālo vērtību. Šajā piemērā izmantotā vienības neto cenas pielaide ir +8%.
        -   Cenu kopsummu salīdzināšana — rēķina rindā norādītā neto summa atbilst pirkšanas pasūtījuma rindā norādītajai neto summai saskaņā ar pielaides procentuālo vērtību, summu vai procentuālo vērtību un summu. Šajā piemērā izmantotā cenu kopsummu salīdzināšanas pielaide ir +15%.

Contoso izrakstītajā papīra formāta rēķinā ir ietverta tālāk norādītā informācija.

| Krājums                        | Daudzums | Vienības cena | Neto summa |
|-----------------------------|----------|------------|------------|
| 1500 — CNC Milicron mašīna | 5.        | 8100,00   | 40,500.00  |
| Sūtīšana un apstrāde       |          |            | 4,000.00   |
| Nodokļi                         |          |            | 0.00       |
| Summa                       |          |            | 44,500.00  |

Rēķina rindā ir tālāk norādītā informācija.

| Krājums                 | Daudzums | Vienības cena | Rindas neto summa | Atbilstības ierobežojumi    | Salīdzināmais produktu ieejas plūsmas daudzums | Cenas salīdzināšana | Cenas kopsummas saskaņošana |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 — CNC Milicron mašīna | 5.        | 8100,00   | 40 500,00       | Trīsvirzienu atbilstība | Izdevās                         | Izdevās      | Izdevās            |

Tā kā šī rinda atbilst rēķinu salīdzināšanas procesa prasībām, rēķinu var grāmatot.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Piemērs: krājumu un kreditoru kombināciju trīsvirzienu atbilstība
Kopsavilkums. Kens ir kontrolieris juridiskas personas Fabrikam galvenajā birojā. Kens izlemj, ka visiem rēķiniem, kuru pamatā ir pirkšanas pasūtījumi, ir jānosaka atbilstība pirkšanas pasūtījumu rindām (divvirzienu atbilstība). Keisija ir grāmatvede Fabrikam Malaizija nodaļā. Viņa norāda, ka atlasītajiem vienumiem, kas ir pasūtīti no noteiktiem kreditoriem Malaizijā, ir jānosaka atbilstība gan pirkšanas pasūtījuma rindām, gan produktu ieejas plūsmas dokumenta rindām (trīsvirzienu atbilstība). Viņa var arī mainīt noteiktu pirkšanas pasūtījumu atbilstības ierobežojumus, iestatot augstāku atbilstības līmeni. 

Apjomi un summas ir mazi, un ir radušas problēmas saistībā ar piegādi no dažiem kreditoriem Malaizijā. Šo iemeslu dēļ Keisija iestata noteiktu Malaizijā iegūto krājumu un kreditoru kombināciju kontroles līmeni uz trīsvirzienu atbilstību. 

Šajā piemērā ietvertie rēķinu salīdzināšanas atbilstības ierobežojumi palīdz personām tālāk norādītajos amatos sasniegt savus mērķus.
-   Kens ir kontrolieris uzņēmumā Fabrikam. Kens var palīdzēt personām organizācija noteikt un atrisināt problēmas, kas ir saistītas ar kreditoru nodrošināto krājumu (preču un pakalpojumu) pasūtīšanu, saņemšanu un maksāšanu par tiem.
-   Keisija ir grāmatvede Fabrikam Malaizija nodaļā. Viņa var ieviest uzņēmuma politiku un nodrošināt, ka visi rēķini tiek apmaksāti tikai pēc tam, kad tiek noteikta to atbilstība pirkšanas pasūtījuma rindām un preču un pakalpojumu produktu ieejas plūsmas dokumentiem. Viņa var arī paaugstināt noteiktu krājumu kontroles līmeni, iestatot trīsvirzienu atbilstību, lai kontrolētu darbības izmaksas.

### <a name="prerequisites"></a>Priekšnosacījumi

-   Plkst. 1. **iestata** atbilstības ierobežojumus juridiskas personas līmenī kā **divvirzienu atbilstību**.
-   Plkst. iestata **saskaņotās cenas kopsummu** **lauku juridiskajai personai kā procentuālo vērtību un ievada 10%** kā **Tolerances** procentus **·**.
-   Kens iestata visu krājumu vienības cenas pielaidi 2%.
-   Cassie iestata atbilstības **ierobežojumus** krājuma un kreditora kombinācijas līmenī krājumam CONTOSO2500 – datora un kreditora Contoso trīsvirziena **atbilstībai**.
-   Alīsija, pirkšanas pasūtījumu daļas darbiniece Fabrikam, Malaizijas nodaļā, izsniedz pirkšanas pasūtījumus uzņēmumam Contoso par trīs krājumu piegādi, kā tas ir redzams tālāk esošajā tabulā. Kad viņa izveido pirkšanas pasūtījumu, viņa pārraksta atbilstības ierobežojumus **peles** to trīsvirzienu atbilstībai divvirzienu atbilstības vietā.

    | Krājuma kods           | Daudzums | Vienības cena | Neto summa | Atbilstības ierobežojumi (noklusējuma vērtība) | Atbilstības ierobežojumi (pirkšanas pasūtījuma rindā) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 — dators     | 2        | 2500,00   | 5000,00   | Trīsvirzienu atbilstība              | Trīsvirzienu atbilstība                           |
    | MM01 — bezvadu pele | 2        | 40,00      | 80,00      | Divvirzienu atbilstība                | Trīsvirzienu atbilstība                           |
    | USB disks             | 200      | 10,00      | 2000,00   | Divvirzienu atbilstība                | Divvirzienu atbilstība                             |

### <a name="scenario"></a>Scenārijs

1.  Krājumi tiek saņemti. Samijs, Fabrikam Malaizijas nodaļas saņemšanas daļas darbinieks, tiek pārtraukts un uzreiz neiegrāmato produkta ieejas plūsmas dokumentu.
2.  Eiprila, Fabrikam kreditoru nodaļas koordinatore, ievada un pārbauda uzņēmuma Contoso iesniegto rēķinu. Viņa pārbauda tālāk norādīto informāciju.
    -   Krājumiem, kuriem ir nepieciešama trīsvirzienu atbilstība, rēķina rindā norādītais daudzums atbilst saņemtajam daudzumam. Saņemtais daudzums ir norādīts produktu ieejas plūsmas dokumentā, kas tiek salīdzināts ar rēķinu.
    -   Krājumiem, kuriem ir nepieciešama divvirzienu vai trīsvirzienu atbilstība, rēķina rindās norādītās cenas atbilst programmā definētajām pielaidēm. Tas attiecas uz tālāk norādītajiem cenu salīdzināšanas tipiem.
        -   Vienības neto cenu salīdzināšana — rēķina rindā norādītā vienības neto cena atbilst pirkšanas pasūtījuma rindā norādītajai vienības neto cenai saskaņā ar pielaides procentuālo vērtību. Šajā piemērā izmantotā vienības neto cenas pielaide ir +2%.
        -   Cenu kopsummu salīdzināšana — rēķina rindā norādītā neto summa atbilst pirkšanas pasūtījuma rindā norādītajai neto summai saskaņā ar pielaides procentuālo vērtību, summu vai procentuālo vērtību un summu. Šajā piemērā izmantotā cenu kopsummu salīdzināšanas pielaide ir +10%.

Contoso izrakstītajā papīra formāta rēķinā ir ietverta tālāk norādītā informācija.

| Krājums                  | Daudzums | Vienības cena | Neto summa |
|-----------------------|----------|------------|------------|
| PH2500 — dators     | 2        | 2500,00   | 5000,00   |
| MM01 — bezvadu pele | 2        | 41.00      | 82.00      |
| USB disks             | 200      | 10.05      | 2,010.00   |
| Rēķina kopsumma         |          |            | 7,092.00   |

Rēķina rindā ir tālāk norādītā informācija.

| Krājums           | Daudzums | Vienības cena | Rindas neto summa | Atbilstības ierobežojumi    | Salīdzināmais produktu ieejas plūsmas daudzums | Cenas salīdzināšana | Cenas kopsummas saskaņošana |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 — dators     | 2        | 2500,00   | 5000,00        | Trīsvirzienu atbilstība | Neizdevās.                         | Izdevās      | Izdevās            |
| MM01 — bezvadu pele | 2        | 41,00      | 82,00           | Trīsvirzienu atbilstība | Neizdevās.                         | Neizdevās.      | Izdevās            |
| USB disks             | 200      | 10,05      | 2010,00         | Divvirzienu atbilstība   |                                | Izdevās      | Izdevās            |

Pievērsiet uzmanību tālāk norādītajiem krājumiem.
-   Krājuma PH2500 — dators rindas kolonnā Salīdzināmais produktu ieejas plūsmas daudzums ir redzama brīdinājuma ikona, jo nav noteikta rēķina rindas atbilstība produkta ieejas plūsmas dokumentam.
-   Krājuma MM01 — bezvadu pele rindas kolonnā Salīdzināmais produktu ieejas plūsmas daudzums ir redzama brīdinājuma ikona, jo nav noteikta rēķina rindas atbilstība produkta ieejas plūsmas dokumentam. Kolonnā Vienības cenas atbilstība ir redzama brīdinājuma ikona, jo ir pārsniegta vienības neto cenas pielaide 2%.
-   Krājuma USB disks rindas kolonna Salīdzināmais produktu ieejas plūsmas daudzums ir tukša, jo divvirzienu atbilstība nenodrošina rēķina rindā un produkta ieejas plūsmas dokumenta rindā norādīto daudzumu atbilstības noteikšanu.

Ja nepieciešams apstiprinājums rēķinu grāmatošanai ar rēķinu salīdzināšanas neatbilstībām, **·** **pirms** rēķinu grāmatošanas ar cenu salīdzināšanas kļūdām un daudzuma salīdzināšanas kļūdām ir jāatlasa apstiprināt ar salīdzināšanas neatbilstībām. Ja apstiprinājums nav nepieciešams, var turpināt rēķina apstrādi, ja nav radušas citas grāmatošanas kļūdas.


Papildinformāciju skatiet sadaļā [Kreditoru rēķinu salīdzināšanas pārskats](accounts-payable-invoice-matching.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
