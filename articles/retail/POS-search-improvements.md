---
title: "Preču meklēšana un debitoru meklēšana POS"
description: "Šajā tēmā ir sniegts apskats par uzlabojumiem, kas ir ieviesti programmas Dynamics 365 for Retail preču un debitoru meklēšanas funkcionalitātē."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5f6f9a02b20549a75941d367c1b46e3439360078
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Apskats par preču un debitoru meklēšanu pārdošanas punktā

Modern pārdošanas punkts (MPOS) un Mākoņa pārdošanas punkts (CPOS) nodrošina ērtu meklēšanas funkcionalitāti, kas veikala darbiniekiem ļauj ātri atrast preces un debitorus. Meklēšanas josla vienmēr atrodas MPOS un CPOS augšpusē, lai darbinieki varētu ātri atrast preces un debitorus.

Darbinieki preces var meklēt preču klāstos un katalogos, kas ir saistīti ar pašreizējo veikalu, kā arī preču klāstos un katalogos, kas ir saistīti ar jebkuru citu attiecīgā uzņēmuma veikalu. Tāpēc kasieri var pārdot un atgriezt preces, kas neietilpst veikala preču klāstā. Līdzīgi arī darbinieki var meklēt debitorus, kas ir saistīti ar pašreizējo veikalu vai jebkuru citu attiecīgā uzņēmuma veikalu. Turklāt darbinieki var meklēt debitorus, kas ir saistīti ar citu uzņēmumu pamata organizācijā.

## <a name="product-search"></a>Preču meklēšana 

Pēc noklusējuma preču meklēšana tiek veikta veikala preču klāstā. Šī tipa meklēšana tiek saukta par *lokālo preču meklēšanu*. Taču darbinieki var vienkārši pārslēgties uz jebkuru katalogu, kas ir saistīts ar pašreizējo veikalu, vai arī meklēt citā veikalā. Šī tipa meklēšana tiek saukta par *attālo preču meklēšanu*. Lai mainītu katalogu, lapas kreisajā pusē atlasiet pogu **Kategorijas**. Tiek parādīta rūts, šīs rūts augšpusē atlasiet pogu **Mainīt katalogu** un pēc tam atlasiet kādu no pieejamajiem katalogiem, lai to pārlūkotu. Sistēma meklēs preces atlasītajā katalogā.

Lapā **Mainīt katalogu** darbinieki var vienkārši atlasīt jebkuru veikalu vai meklēt preces visos veikalos.

![Kataloga mainīšana](./media/Changecatalog.png "Kataloga mainīšana")
 
Lokālā preču meklēšana meklē tālāk uzskaitītajos preču rekvizītos.

- Preces numurs
- Preces nosaukums
- Apraksts
- Dimensijas
- Svītrkods
- Meklēšanas nosaukums

### <a name="enhancements-to-local-product-searches"></a>Lokālās preču meklēšanas uzlabojumi

Lokālās preču meklēšanas funkcionalitāte ir padarīta lietotājam draudzīgāka. Ir veikti tālāk norādītie uzlabojumi.

- Meklēšanas joslai ir pievienotas preču un debitoru nolaižamās izvēlnes, lai pirms meklēšanas darbinieki varētu atlasīt **Prece** vai **Debitors**. Pēc noklusējuma ir atlasīta **Prece**, kā parādīts nākamajā ilustrācijā.
- Meklēšanai ar vairākiem atslēgvārdiem (t.i., meklēšanai, kur tiek izmantoti meklējamie vārdi) mazumtirgotāji var konfigurēt, vai meklēšanas rezultātos ietvert arī rezultātus, kas atbilst jebkuram meklētajam vārdam, vai ietvert tikai rezultātus, kas atbilst visiem meklētajiem vārdiem. Šis iestatījums ir pieejams POS funkcionalitātes profilā, zem jaunas grupas ar nosaukumu **Preču meklēšana**. Noklusējuma iestatījums ir **Meklēt atbilstību jebkuram meklētajam vārdam**. Šis iestatījums ir arī ieteicamais iestatījums. Ja tiek lietots iestatījums **Meklēt atbilstību jebkuram meklētajam vārdam**, tad rezultātos tiek rādītas visas preces, kas pilnīgi vai daļēji atbilst vienam vai vairākiem meklētajiem vārdiem, un šie rezultāti tiek automātiski kārtoti augošā secībā, sākot ar precēm, kam atbilst visvairāk atslēgvārdu (pilnīgi vai daļēji).

    Iestatījums **Meklēt atbilstību visiem meklētajiem vārdiem** atgriež tikai tās preces, kas atbilst visiem meklētajiem vārdiem (pilnīgi vai daļēji). Šis iestatījums noder, ja preču nosaukumi ir gari un darbinieki meklēšanas rezultātos vēlaties redzēt tikai ierobežotu preču skaitu. Taču šī tipa meklēšanai ir divi tālāk norādītie ierobežojumi.

    - Meklēšana tiek veikta pēc atsevišķiem preču rekvizītiem. Tiek atgrieztas, piemēram, tikai tās preces, kurām ir visi meklētie atslēgvārdi vismaz vienā preces rekvizītā.
    - Dimensijas netiek meklētas.

- Tagad mazumtirgotāji var konfigurēt preču meklēšanu, lai rādītu meklēšanas ieteikumus, kamēr lietotāji raksta preču nosaukumus. Jauns iestatījums šai funkcionalitātei ir pieejams POS funkcionalitātes profilā, zem grupas ar nosaukumu **Preču meklēšana**. Šis iestatījums saucas **Rādīt meklēšanas ieteikumus rakstīšanas laikā**. Šī funkcionalitāte var palīdzēt darbiniekiem ātri atrast meklētās preces, jo viņiem nav nepieciešams visu nosaukumu ievadīt manuāli.
- Preču meklēšanas algoritms meklētos vārdus tagad meklē arī preces rekvizītā **Meklēšanas nosaukums**.

![Preču ieteikumi](./media/Productsuggestions.png "Preču ieteikumi")

## <a name="customer-search"></a>Debitora meklēšana

Debitora meklēšana tiek lietota, lai dažādos nolūkos atrastu debitorus. Piemēram, kasieri var vēlēties apskatīt debitora vēlmju sarakstu vai pirkumu vēsturi vai pievienot debitoru kādai transakcijai. Vairāku atslēgvārdu meklēšanas gadījumā debitoru meklēšanas algoritms atgriež visus debitorus, kas atbilst kādam no meklētajiem atslēgvārdiem. Taču debitori, kas atbilst vislielākajam skaitam atslēgvārdu, tiek rādīti rezultātu augšpusē. Šī uzvedība ir vienāda ar veidu, kā rezultātus rāda pārējās meklēšanas programmas. Tās vispirms rāda rezultātus, kas atbilst lielākajam skaitam meklēto vārdu, un pēc tam tās rāda rezultātus, kas meklētajiem atslēgvārdiem atbilst daļēji. Šī uzvedība kasieriem palīdz situācijās, kur viņi meklēšanai izmanto vairākus atslēgvārdus, bet vienā no atslēgvārdiem ir pareizrakstības kļūda.

Pēc noklusējuma debitora meklēšana tiek veikta debitoru adrešu grāmatās, kuras ir saistītas ar veikalu. Šī tipa meklēšana tiek saukta par *lokālo debitoru meklēšanu*. Taču darbinieki debitorus var meklēt arī globāli. Citiem vārdiem sakot — viņi var meklēt gan uzņēmuma veikalos, gan visās pārējās juridiskajās personās. Šī tipa meklēšana tiek saukta par *attālo debitoru meklēšanu*.

Lai meklētu globāli, darbinieki var atlasīt lapas apakšā esošo pogu **Filtrēt rezultātus** un pēc tam atlasīt opciju **Meklēt visos veikalos**, kā parādīts nākamajā ilustrācijā. Šajā gadījumā tiek atgriezti ne tikai debitori. Tiek atgrieztas arī visu tipu puses, kas veido daļu no jebkuras adrešu grāmatas galvenajā pārvaldē. Šo pušu klāstā ietilpst darbinieki, kreditori, kontaktpersonas un konkurenti.

> [!NOTE]
> Lai saņemtu attālās debitoru meklēšanas rezultātus, ir jāievada vismaz četras rakstzīmes.

Attālajā debitoru meklēšanā debitora ID netiek rādīts debitoriem no citām juridiskajām personām, jo pašreizējā uzņēmumā šīm personām debitora ID nav izveidots. Taču, ja darbinieks atver debitora detalizētās informācijas lapu, tad sistēma šai pusei automātiski ģenerē debitora ID, kā arī attiecīgo debitoru piesaista veikala debitoru adrešu grāmatām. Tāpēc šis debitors būs redzams vēlāk veiktajos lokālajos veikala meklējumos.

![Globālā debitoru meklēšana](./media/Globalcustomersearch.png "Globālā debitoru meklēšana")

### <a name="enhancements-to-local-customer-searches"></a>Lokālās debitoru meklēšanas uzlabojumi

Lokālie debitoru meklējumi darbiniekiem palīdz ātri atrast debitorus pēc tālruņa numura. Darbiniekiem nav jāieraksta nekādas speciālas rakstzīmes, kas ir pievienotas debitora tālruņa numuram, piemēram, atstarpes, defises vai iekavas. Lai gan kasieri tālruņa numurus var glabāt jebkādā formātā (piemēram, tie var ietvert iekavas, defises, simbolus un citas rakstzīmes), debitorus viņi var meklēt, ierakstot daļēju tālruņa numuru. Ja tālruņa numura ievadīšanas laikā kasieris ietvēra speciālās rakstzīmes, citi kasieri šo debitoru var atrast, ierakstot ciparus, kas ir redzami aiz speciālajām rakstzīmēm. Piemēram, ja debitora tālruņa numurs tika ievadīts kā **123-456-7890**, tad kasieris šo debitoru var meklēt, ierakstot **123**, **456**, **7890** vai **1234567890**, vai daļēji ievadot tālruņa numura pirmos dažus skaitļus.

