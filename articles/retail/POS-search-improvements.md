---
title: "Preču meklēšana un debitoru meklēšana POS"
description: "Šajā tēmā ir sniegts apskats par uzlabojumiem, kas ir ieviesti programmas Microsoft Dynamics 365 for Retail preču un debitoru meklēšanas funkcionalitātē."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b055ae09e87434f9e43c558e2a43d0467d70aaed
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Apskats par preču un debitoru meklēšanu pārdošanas punktā

[!INCLUDE [banner](includes/banner.md)]

Modern pārdošanas punkts (Modern Point of Sale — MPOS) un Mākoņa pārdošanas punkts (Cloud Point of Sale — CPOS) nodrošina ērtu preču un debitoru meklēšanas funkcionalitāti. Tā kā meklēšanas josla vienmēr atrodas MPOS un CPOS logu augšpusē, darbinieki var ātri meklēt preces un debitorus.

Darbinieki var meklēt preces noteiktos preču klāstos un katalogos, kas ir saistīti ar pašreizējo veikalu. Viņi var meklēt arī preču klāstos un katalogos, kas ir saistīti ar jebkuru citu uzņēmumā ietilpstošo veikalu. Tāpēc kasieri var pārdot un atgriezt preces, kas neietilpst veikala preču klāstā. Līdzīgi arī darbinieki var meklēt debitorus, kas ir saistīti ar pašreizējo veikalu vai jebkuru citu attiecīgā uzņēmuma veikalu. Turklāt darbinieki var meklēt debitorus, kas ir saistīti ar citu uzņēmumu pamatorganizācijā.

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

Lokālās preču meklēšanas funkcionalitāte tagad ir lietotājam vēl draudzīgāka. Ir veikti tālāk norādītie uzlabojumi.

- Meklēšanas joslai ir pievienotas preču un debitoru nolaižamās izvēlnes, lai pirms meklēšanas darbinieki varētu atlasīt **Prece** vai **Debitors**. Pēc noklusējuma ir atlasīta **Prece**, kā parādīts nākamajā ilustrācijā.
- Meklēšanai ar vairākiem atslēgvārdiem (t.i., meklēšanai, kur tiek izmantoti meklējamie vārdi) mazumtirgotāji var konfigurēt, vai meklēšanas rezultātos ietvert arī rezultātus, kas atbilst *jebkuram* meklētajam vārdam, vai ietvert tikai rezultātus, kas atbilst *visiem* meklētajiem vārdiem. Šis iestatījums ir pieejams POS funkcionalitātes profilā, jaunā grupā ar nosaukumu **Preču meklēšana**. Noklusējuma iestatījums ir **Meklēt atbilstību jebkuram meklētajam vārdam**. Šis iestatījums ir arī ieteicamais iestatījums. Kad tiek izmantots iestatījums **Meklēt atbilstību jebkuram meklētajam vārdam**, kā meklēšanas rezultāti tiek atgrieztas visas preces, kas pilnīgi vai daļēji atbilst vienam vai vairākiem no meklētajiem vārdiem. Šie rezultāti tiek automātiski kārtoti augošā secībā pēc precēm, kurām ir visvairāk atslēgvārdu atbilstību (pilnīgu vai daļēju).

    Iestatījums **Meklēt atbilstību visiem meklētajiem vārdiem** atgriež tikai tās preces, kas atbilst visiem meklētajiem vārdiem (pilnīgi vai daļēji). Šis iestatījums noder, ja preču nosaukumi ir gari un darbinieki meklēšanas rezultātos vēlaties redzēt tikai ierobežotu preču skaitu. Taču šī tipa meklēšanai ir divi tālāk norādītie ierobežojumi.

    - Meklēšana tiek veikta pēc atsevišķiem preču rekvizītiem. Tiek atgrieztas, piemēram, tikai tās preces, kurām ir visi meklētie atslēgvārdi vismaz vienā preces rekvizītā.
    - Dimensijas netiek meklētas.

- Tagad mazumtirgotāji var konfigurēt preču meklēšanu, lai rādītu meklēšanas ieteikumus, kamēr lietotāji raksta preču nosaukumus. Šai funkcionalitātei ir pieejams jauns iestatījums POS funkcionalitātes profilā, grupā ar nosaukumu **Preču meklēšana**. Šis iestatījums saucas **Rādīt meklēšanas ieteikumus rakstīšanas laikā**. Šī funkcionalitāte var palīdzēt darbiniekiem ātri atrast meklētās preces, jo viņiem nav nepieciešams visu nosaukumu ievadīt manuāli.
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

### <a name="enhancements-to-local-customer-search"></a>Lokālās debitoru meklēšanas uzlabojumi

Ir vienkāršota meklēšana, kas ir balstīta uz tālruņa numuru. Tagad šī meklēšana ignorē speciālās rakstzīmes, piemēram, atstarpes, defises un iekavas, kas varētu būt pievienotas, izveidojot debitoru. Tāpēc kasieriem meklēšanas laikā nav jāraizējas par tālruņa numura formātu. Viņi debitorus var arī meklēt, ierakstot daļēju tālruņa numuru. Ja tālruņa numurā ir speciālās rakstzīmes, to var atrast arī, meklējot numurus, kas tiek rādīti aiz speciālajām rakstzīmēm. Piemēram, ja debitora tālruņa numurs tika ievadīts kā **123-456-7890**, kasieris šo debitoru var meklēt, ierakstot **123**, **456**, **7890** vai **1234567890**, vai ievadot tālruņa numura pirmos dažus ciparus.

Tradicionālā debitoru meklēšana var būt laikietilpīga, jo tā meklē vairākos laukos. Tā vietā kasieri tagad var meklēt pēc viena pielāgota rekvizīta, piemēram, nosaukuma, e-pasta adreses vai tālruņa numura. Debitoru meklēšanas algoritma izmantotie rekvizīti kopā tiek saukti par *debitoru meklēšanas kritērijiem*. Sistēmas administrators vienu vai vairākus kritērijus var ērti konfigurēt kā saīsnes, kas būs redzamas POS. Tā kā meklēšanai tiek izmantots tikai viens kritērijs, tiek rādīti tikai saistītie meklēšanas rezultāti, un veiktspēja ir daudz labāka par standarta debitoru meklēšana veiktspēju. Nākamajā attēlā ir parādītas POS pieejamās debitoru meklēšanas saīsnes.

![Debitoru meklēšanas saīsnes](./media/SearchShortcutsPOS.png "Debitoru meklēšanas saīsnes")

Lai meklēšanas kritērijus iestatītu kā saīsnes, administratoram ir jāatver lapa **Mazumtirdzniecības parametri** programmatūrā Microsoft Dynamics 365 for Finance and Operations, un pēc tam cilnē **POS meklēšanas kritēriji** jāatlasa visi kritēriji, kas ir jārāda kā saīsnes.

![Meklēšanas saīšņu konfigurēšana](./media/ConfigureShortcutsAX.png "Meklēšanas saīšņu konfigurēšana")

> [!NOTE]
> Ja pievienojat pārāk daudz saīšņu, POS meklēšanas joslas nolaižamā izvēlne kļūt pārblīvēta, un tas var ietekmēt darbinieku meklēšanas ērtumu. Ieteicams pievienot tikai tik daudz saīšņu, cik nepieciešams.

Lauks **Rādīšanas secība** nosaka secību, kādā POS tiek rādītas šīs saīsnes. Rādītie kritēriji ir standarta versijas rekvizīti, kurus debitoru meklēšanas algoritms izmanto debitoru meklēšanai. Taču partneri var pievienot pielāgotus rekvizītus kā meklēšanas saīsnes. Lai pievienotu pielāgotus rekvizītus kā meklēšanas saīsnes, sistēmas administratoram ir jāpaplašina paplašināmais uzskaitījums, kas tiek izmantots debitoru meklēšanas kritērijiem, un pēc tam partnera pielāgotie rekvizīti ir jāatzīmē kā saīsnes. Partneri ir atbildīgi par koda rakstīšanu, lai atrastu rezultātus, kad meklēšanai tiek izmantotas partneru pielāgotās saīsnes.

> [!NOTE]
> Pielāgots rekvizīts, kas tiek pievienots uzskaitījumam, neietekmē standarta debitoru meklēšanas algoritmu. Citiem vārdiem sakot — debitoru meklēšanas algoritms nemeklēs pielāgotajā rekvizītā. Lietotāji meklēšanai var izmantot pielāgotu rekvizītu tikai tad, ja šis pielāgotais rekvizīts ir pievienots kā saīsne vai ja tiek ignorēts noklusējuma meklēšanas algoritms.

