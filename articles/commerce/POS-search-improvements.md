---
title: Preču meklēšana un debitoru meklēšana pārdošanas punktā (POS)
description: Šajā tēmā ir sniegts apskats par preču un debitoru meklēšanas funkcionalitātes uzlabojumiem programmā Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 10c843670a280c86790185c8a39cb2943e2838f9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413973"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Preču meklēšana un debitoru meklēšana pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

Modern pārdošanas punkts (Modern Point of Sale — MPOS) un Mākoņa pārdošanas punkts (Cloud Point of Sale — CPOS) nodrošina ērtu preču un debitoru meklēšanas funkcionalitāti. Tā kā meklēšanas josla vienmēr atrodas MPOS un CPOS logu augšpusē, darbinieki var ātri meklēt preces un debitorus.

Darbinieki var meklēt preces noteiktos preču klāstos un katalogos, kas ir saistīti ar pašreizējo veikalu. Viņi var meklēt arī preču klāstos un katalogos, kas ir saistīti ar jebkuru citu uzņēmumā ietilpstošo veikalu. Tāpēc kasieri var pārdot un atgriezt preces, kas neietilpst veikala preču klāstā. Līdzīgi arī darbinieki var meklēt debitorus, kas ir saistīti ar pašreizējo veikalu vai jebkuru citu attiecīgā uzņēmuma veikalu. Turklāt darbinieki var meklēt debitorus, kas ir saistīti ar citu uzņēmumu pamatorganizācijā.

## <a name="product-search"></a>Preču meklēšana

Pēc noklusējuma preču meklēšana tiek veikta veikala preču klāstā. Šī tipa meklēšana tiek saukta par *lokālo preču meklēšanu*. Taču darbinieki var vienkārši pārslēgties uz jebkuru katalogu, kas ir saistīts ar pašreizējo veikalu, vai arī meklēt citā veikalā. Šī tipa meklēšana tiek saukta par *attālo preču meklēšanu*. Lai mainītu katalogu, lapas kreisajā pusē atlasiet pogu **Kategorijas**. Tiek parādīta rūts, šīs rūts augšpusē atlasiet pogu **Mainīt katalogu** un pēc tam atlasiet kādu no pieejamajiem katalogiem, lai to pārlūkotu. Sistēma meklēs preces atlasītajā katalogā.

Lapā **Mainīt katalogu** darbinieki var vienkārši atlasīt jebkuru veikalu vai meklēt preces visos veikalos.

![Kataloga maiņa](./media/Changecatalog.png "Kataloga maiņa")

Lokālā preču meklēšana meklē tālāk uzskaitītajos preču rekvizītos.

- Preces numurs
- Preces nosaukums
- Apraksts
- Dimensijas
- Svītrkods
- Meklēšanas nosaukums

### <a name="enhancements-to-local-product-searches"></a>Lokālās preču meklēšanas uzlabojumi

Lokālās preču meklēšanas funkcionalitāte tagad ir lietotājam vēl draudzīgāka. Ir veikti tālāk norādītie uzlabojumi.

- Meklēšanas joslai ir pievienotas preču un debitoru nolaižamās izvēlnes, lai pirms meklēšanas darbinieki varētu atlasīt **Prece** vai **Debitors**. Pēc noklusējuma ir atlasīta **Prece**, kā parādīts nākamajā ilustrācijā.
- Meklēšanai ar vairākiem atslēgvārdiem (t.i., meklēšanai, kur tiek izmantoti meklējamie vārdi) mazumtirgotāji var konfigurēt, vai meklēšanas rezultātos ietvert arī rezultātus, kas atbilst *jebkuram* meklētajam vārdam, vai ietvert tikai rezultātus, kas atbilst *visiem* meklētajiem vārdiem. Šīs funkcionalitātes iestatījums ir pieejams POS funkcionalitātes profilā, jaunā grupā ar nosaukumu **Preču meklēšana**. Noklusējuma iestatījums ir **Meklēt atbilstību jebkuram meklētajam vārdam**. Šis iestatījums ir arī ieteicamais iestatījums. Kad tiek izmantots iestatījums **Meklēt atbilstību jebkuram meklētajam vārdam**, kā meklēšanas rezultāti tiek atgrieztas visas preces, kas pilnīgi vai daļēji atbilst vienam vai vairākiem no meklētajiem vārdiem. Šie rezultāti tiek automātiski kārtoti augošā secībā pēc precēm, kurām ir visvairāk atslēgvārdu atbilstību (pilnīgu vai daļēju).

    Iestatījums **Meklēt atbilstību visiem meklētajiem vārdiem** atgriež tikai tās preces, kas atbilst visiem meklētajiem vārdiem (pilnīgi vai daļēji). Šis iestatījums noder, ja preču nosaukumi ir gari un darbinieki meklēšanas rezultātos vēlaties redzēt tikai ierobežotu preču skaitu. Taču šī tipa meklēšanai ir divi tālāk norādītie ierobežojumi.

    - Meklēšana tiek veikta pēc atsevišķiem preču rekvizītiem. Tiek atgrieztas, piemēram, tikai tās preces, kurām ir visi meklētie atslēgvārdi vismaz vienā preces rekvizītā.
    - Dimensijas netiek meklētas.

- Tagad mazumtirgotāji var konfigurēt preču meklēšanu, lai rādītu meklēšanas ieteikumus, kamēr lietotāji raksta preču nosaukumus. Šai funkcionalitātei ir pieejams jauns iestatījums POS funkcionalitātes profilā, grupā ar nosaukumu **Preču meklēšana**. Šis iestatījums saucas **Rādīt meklēšanas ieteikumus rakstīšanas laikā**. Šī funkcionalitāte var palīdzēt darbiniekiem ātri atrast meklētās preces, jo viņiem nav nepieciešams visu nosaukumu ievadīt manuāli.
- Preču meklēšanas algoritms meklētos vārdus tagad meklē arī preces rekvizītā **Meklēšanas nosaukums**.

![Preču ieteikumi](./media/Productsuggestions.png "Preču ieteikumi")

## <a name="customer-search"></a>Debitora meklēšana

Debitora meklēšana tiek lietota, lai dažādos nolūkos atrastu debitorus. Piemēram, kasieri var vēlēties apskatīt debitora vēlmju sarakstu vai pirkumu vēsturi vai pievienot debitoru kādai transakcijai. Meklēšanas algoritms salīdzina meklējamos vārdus ar vērtībām, kas pastāv šādos debitora rekvizītos:

- Vārds
- E-pasta adrese
- Tālruņa numurs
- Lojalitātes programmas kartes numurs
- Adrese
- Konta numurs

No šiem rekvizītiem vārds nodrošina lielāko elastību vairāku atslēgvārdu meklēšanai, jo algoritms atgriež visus debitorus, kuri atbilst kādam no meklētajiem atslēgvārdiem. Debitori, kas atbilst vislielākajam skaitam atslēgvārdu, tiek rādīti rezultātu augšpusē. Šī darbība palīdz kasieriem situācijās, kad viņi veic meklēšanu, ievadot pilnu vārdu un uzvārdu, bet uzvārds un vārds sākotnējās datu ievades laikā ir apmainīti vietām. Tomēr veiktspējas apsvērumu dēļ visiem citiem rekvizītiem tiek saglabāta meklēšanas atslēgvārdu secība. Tāpēc, ja meklēšanas atslēgvārdu secība neatbilst secībai, kurā tiek glabāti dati, netiks atgriezts neviens rezultāts.

Pēc noklusējuma debitora meklēšana tiek veikta debitoru adrešu grāmatās, kuras ir saistītas ar veikalu. Šī tipa meklēšana tiek saukta par *lokālo debitoru meklēšanu*. Taču darbinieki debitorus var meklēt arī globāli. Citiem vārdiem sakot — viņi var meklēt gan uzņēmuma veikalos, gan visās pārējās juridiskajās personās. Šī tipa meklēšana tiek saukta par *attālo debitoru meklēšanu*.

Lai meklētu globāli, darbinieki var atlasīt lapas apakšā esošo pogu **Filtrēt rezultātus** un pēc tam atlasīt opciju **Meklēt visos veikalos**, kā parādīts nākamajā ilustrācijā. Šajā gadījumā tiek atgriezti ne tikai debitori. Tiek atgrieztas arī visu tipu puses, kas veido daļu no jebkuras adrešu grāmatas galvenajā pārvaldē. Šo pušu klāstā ietilpst darbinieki, kreditori, kontaktpersonas un konkurenti.

> [!NOTE]
> Lai saņemtu attālās debitoru meklēšanas rezultātus, ir jāievada vismaz četras rakstzīmes.

Attālajā debitoru meklēšanā debitora ID netiek rādīts debitoriem no citām juridiskajām personām, jo pašreizējā uzņēmumā šīm personām debitora ID nav izveidots. Taču, ja darbinieks atver debitora detalizētās informācijas lapu, tad sistēma šai pusei automātiski ģenerē debitora ID, kā arī attiecīgo debitoru piesaista veikala debitoru adrešu grāmatām. Tāpēc šis debitors būs redzams vēlāk veiktajos lokālajos veikala meklējumos.

![Debitora globāla meklēšana](./media/Globalcustomersearch.png "Debitora globāla meklēšana")

### <a name="enhancements-to-local-customer-search"></a>Lokālās debitoru meklēšanas uzlabojumi

Ir vienkāršota meklēšana, kas ir balstīta uz tālruņa numuru. Tagad šī meklēšana ignorē speciālās rakstzīmes, piemēram, atstarpes, defises un iekavas, kas varētu būt pievienotas, izveidojot debitoru. Tāpēc kasieriem meklēšanas laikā nav jāraizējas par tālruņa numura formātu. Piemēram, ja debitora tālruņa numurs tika ievadīts kā **123-456-7890**, kasieris šo debitoru var meklēt, ierakstot **1234567890**, vai ievadot tālruņa numura pirmos dažus ciparus.

> [!NOTE]
> Klientam var būt vairāki tālruņu numuri un vairāki e-pasta ziņojumi. Klienta meklēšanas algoritms meklē arī šos sekundāros e-pasta ziņojumus un tālruņu numurus, bet klientu meklēšanas rezultātu lapa parāda tikai primāro e-pasta adresi un tālruņa numuru. Tas var izraisīt neskaidrību, jo atgrieztā klienta rezultāti nerāda meklēto e-pastu vai tālruņa numuru. Turpmākajā izlaidumā mēs plānojam uzlabot klienta meklēšanas rezultātu ekrānu, lai parādītu šo informāciju.

Tradicionālā debitoru meklēšana var būt laikietilpīga, jo tā meklē vairākos laukos. Tā vietā kasieri tagad var meklēt pēc viena debitora rekvizīta, piemēram, vārda, e-pasta adreses vai tālruņa numura. Debitoru meklēšanas algoritma izmantotie rekvizīti kopā tiek saukti par *debitoru meklēšanas kritērijiem*. Sistēmas administrators vienu vai vairākus kritērijus var ērti konfigurēt kā saīsnes, kas būs redzamas POS. Tā kā meklēšanai tiek izmantots tikai viens kritērijs, tiek rādīti tikai saistītie meklēšanas rezultāti, un veiktspēja ir daudz labāka par standarta debitoru meklēšana veiktspēju. Nākamajā attēlā ir parādītas POS pieejamās debitoru meklēšanas saīsnes.

![Debitora meklēšanas saīsnes](./media/SearchShortcutsPOS.png "Debitora meklēšanas saīsnes")

Lai iestatītu meklēšanas kritērijus kā saīsnes, administratoram ir jāatver lapa **Commerce parametri** programmā Commerce un pēc tam cilnē **POS meklēšanas kritēriji** ir jāatlasa visi kritēriji, kas ir jārāda kā saīsnes.

![Konfigurēt meklēšanas saīsnes](./media/ConfigureShortcutsAX.png "Konfigurēt meklēšanas saīsnes")

> [!NOTE]
> Ja pievienojat pārāk daudz saīšņu, POS meklēšanas joslas nolaižamā izvēlne kļūt pārblīvēta, un tas var ietekmēt darbinieku meklēšanas ērtumu. Ieteicams pievienot tikai tik daudz saīšņu, cik nepieciešams.

Lauks **Rādīšanas secība** nosaka secību, kādā POS tiek rādītas šīs saīsnes. Rādītie kritēriji ir standarta versijas rekvizīti, kurus debitoru meklēšanas algoritms izmanto debitoru meklēšanai. Taču partneri var pievienot pielāgotus rekvizītus kā meklēšanas saīsnes. Lai pievienotu pielāgotus rekvizītus kā meklēšanas saīsnes, sistēmas administratoram ir jāpaplašina paplašināmais uzskaitījums, kas tiek izmantots debitoru meklēšanas kritērijiem, un pēc tam partnera pielāgotie rekvizīti ir jāatzīmē kā saīsnes. Partneri ir atbildīgi par koda rakstīšanu, lai atrastu rezultātus, kad meklēšanai tiek izmantotas partneru pielāgotās saīsnes.

> [!NOTE]
> Pielāgots rekvizīts, kas tiek pievienots uzskaitījumam, neietekmē standarta debitoru meklēšanas algoritmu. Citiem vārdiem sakot — debitoru meklēšanas algoritms nemeklēs pielāgotajā rekvizītā. Lietotāji meklēšanai var izmantot pielāgotu rekvizītu tikai tad, ja šis pielāgotais rekvizīts ir pievienots kā saīsne vai ja tiek ignorēts noklusējuma meklēšanas algoritms.

Gaidāmajā Commerce laidienā mazumtirgotāji kā noklusējuma debitora meklēšanas režīmu POS varēs iestatīt **Meklēt visos veikalos**. Šī konfigurācija var būt noderīga gadījumos, kad debitori, kas tika izveidoti ārpus POS, ir nekavējoties jāmeklē (piemēram, vēl pirms sadales darba izpildes). POS funkcionalitātes profilā būs pieejama jauna opcija **Noklusējuma debitora meklēšanas režīms**. Iestatiet tai vienumu **Ieslēgts**, lai iestatītu noklusējuma meklēšanas režīmam opciju **Meklēt visos veikalos**. Līdz ar katru debitora meklēšanas mēģinājumu tiks veikts reāllaika pieprasījums uz galveno biroju.

Lai palīdzētu novērst negaidītas veiktspējas problēmas, šī konfigurācija tiek slēpta aiz būvējumu izsniegšanas karodziņa ar nosaukumu **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Tādēļ, lai parādītu iestatījumu **Noklusējuma debitora meklēšanas režīms** lietotāja interfeisā (UI), mazumtirgotājam jāizveido atbalsta biļete tā lietotāju pieņemšanas pārbaudes (UAT) un ražošanas vidēm. Pēc tam, kad biļete ir saņemta, tehniskā grupa strādās ar mazumtirgotāju, lai pārliecinātos, ka mazumtirgotājs veic testēšanu vidēs, kas nav ražošanas vides, lai novērtētu veiktspēju un īstenotu visas nepieciešamās optimizācijas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]