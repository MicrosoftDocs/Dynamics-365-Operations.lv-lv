---
title: Darbību nosaukumu un instrukciju pielāgošana Warehouse Management mobile programmai
description: Šajā tēmā ir aprakstīts, kā izveidot un rādīt pielāgotas instrukcijas katrai uzdevumu plūsmai, ko iestatāt programmai Warehouse Management mobile.
author: Mirzaab
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ffd433427b2c5011740a7ee54c93713689945df3
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902251"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Darbību nosaukumu un instrukciju pielāgošana Warehouse Management mobile programmai

> [!IMPORTANT]
> Šajā tēmā aprakstītie līdzekļi attiecas tikai uz jauno Warehouse Management mobile programmu. Tie neietekmē veco noliktavas programmu, kas tagad tiek novecojusi.

Šajā tēmā ir aprakstīts, kā izveidot un rādīt pielāgotas instrukcijas katrai uzdevumu plūsmai, ko iestatāt programmai Warehouse Management mobile. Kad noliktavas darbinieki saņem labi rakstītas instrukcijas, viņi var nekavējoties sākt izmantot jaunas plūsmas, neprasot iepriekšējas apmācības. Šis līdzeklis nodrošina šādus uzlabojumus:

- **Iestatiet darbiniekus ātrāk, ļaujot viņiem ievērot vienkāršas instrukcijas katrai darbībai.** Katrs plūsmas solis nodrošina norādījumus, kas ļauj rindas darbiniekiem izprast uzdevumu.
- **Nodrošināt instrukcijas, kas atbilst jūsu procesiem.** Rakstiet savas instrukcijas, lai atbilstu biznesa un noliktavas procesiem. Piemēram, varat veidot terminoloģijai jūsu fizisko telpu un vietējos saīsinājumus.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Ieslēgt programmas Warehouse darbību norādījumu līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Programmas Warehouse darbību norādījumi*

## <a name="step-titles-and-step-instructions-in-the-app"></a>Soļi un darbību instrukcijas programmā

Katru uzdevumu plūsmas soli programmā Warehouse Management mobile identificē darbības ID. Turklāt katram solim ir nosaukums, ikona un instrukcijas. (Lai iegūtu vairāk informācijas, skatiet [Piešķirt darbību ikonas un nosaukumus programmai Warehouse Management mobile](step-icons-titles.md).)

### <a name="step-titles"></a>Soļu nosaukumi

*Soļa nosaukums* ir īss apraksts, kas darbiniekam ir jāveic soļa laikā. Kā parādīts šajā ilustrācijā, tas tiek parādīts kā liels teksts ekrāna augšpusē.

![Darbības virsraksta piemērs programmā Warehouse Management mobile](media/wma-step-title.png "Darbības virsraksta piemērs programmā Warehouse Management mobile")

> [!TIP]
> Lielā teksta lieluma dēļ ir jāmēģina saglabāt darbību nosaukumus pēc iespējas ātrāk. Pretējā gadījumā teksts var tikt samazināts. Tomēr garajiem nosaukumiem darbinieki vēl aizvien var nospiest un aizturēt nosaukumu, lai atvērtu dialoglodziņu, kurā parādīts pilns teksts.

### <a name="step-instructions"></a>Darbību instrukcijas

*Soļa norāde* ir garāks apraksts, kas sniedz papildu informāciju par to, ko darbiniekam vajadzētu darīt soļa laikā. Tas tiek parādīts uznirstošajā dialoglodziņā, kā parādīts šajā ilustrācijā.

![Darbības instrukcijas piemērs programmā Warehouse Management mobile](media/wma-step-instructions.png "Darbības instrukcijas piemērs programmā Warehouse Management mobile")

Kad solis ir atvērts, darbības instrukcija tiek parādīta automātiski. Darbinieki to var noraidīt, piespiežot jebkur ārpus uznirstošā dialoglodziņa. Turklāt dialoglodziņā ir iekļauta izvēles rūtiņa **Nerādīt atkārtoti**, lai darbinieki varētu atlasīt, lai neļautu instrukcijas parādīties nākamajā reizē, kad viņi veic to pašu uzdevumu.

## <a name="load-the-default-setup"></a>Ielādēt noklusējuma iestatījumus

Kad vispirms ieslēdzat *Warehouse programmas darbību instrukciju* līdzekli, sistēmā nebūs pielāgojamu darbību nosaukumu vai instrukciju. Tāpēc vispirms ir jāielādē noklusējuma iestatījums. Noklusētais iestatījums sniedz tekstus visiem pieejamajiem darbību ID katrā atbalstītajā valodā. Lai ielādētu noklusējuma iestatījumus, veiciet šīs darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**. Lapa tiek aizpildīta ar standarta soļiem.

## <a name="customize-step-titles-and-instructions"></a>Soļu nosaukumu un instrukciju pielāgošana

Lai pielāgotu nosaukumu un/vai instrukcijas solim jebkurā valodā, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.

    Lapā **Mobilās ierīces darbības** ir uzskaitīti visi soļi, kas ir pieejami jūsu sistēmai. Katru darbības ID var koplietot starp jebkuru mobilās ierīces izvēlnes elementu skaitu. Ja darbības ID tiek koplietots starp vairākiem izvēlnes elementiem, visiem šiem izvēlnes elementiem tiek rādīts vienāds nosaukums un instrukcijas. Tomēr ir iespējams izveidot ignorējumus, lai pielāgotu nosaukumu un instrukcijas specifiskiem izvēlnes elementiem. (Papildinformāciju skatiet nākamajā sadaļā.)

    Režģī ir iekļautas tālāk minētās kolonnas.

    - **Izvēlnes krājuma nosaukums** — rindas, kur šī kolonna ir tukša, izmanto noklusējuma soļa nosaukumu un instrukcijas, kas attiecas uz visiem mobilās ierīces izvēlnes vienumiem, kam nav noteikta ignorēšana. Rindām, kur šī kolonna ir iestatīta uz izvēlnes krājuma nosaukumu, ir prioritāte, kas attiecas tikai uz norādīto izvēlnes elementu.
    - **Soļa ID** - soļa unikālais ID.
    - **Ievades nosaukums** - nosaukums, kas tiek rādīts, kad programma pieprasa jaunu informāciju. Parasti lapas lauki ir tukši (t.i., tiem nav iepriekš noteiktu vērtību).
    - **Apstiprināšanas nosaukums** – nosaukums, kas tiek rādīts, kad programma pieprasa sistēmā jau uzglabātas vērtības apstiprināšanu. Parasti lapas laukiem ir iepriekš iestatītas vērtības.

1. Atrodiet to **Soļa ID** un **Izvēlnes elementu nosaukumu** vērtību kombināciju, ko vēlaties rediģēt, un atlasiet vērtību kolonnā **Soļa ID**. Atvērtajā lapā ir uzskaitīti visi pieejamie tulkojumi atlasītā soļa nosaukumam un instrukcijai.
1. Lai pielāgotu tekstu jebkurai valodai, veiciet vienu no šīm darbībām. Abas opcijas ļauj labot tekstus esošajām valodām. Tomēr tikai pirmā opcija ļauj pievienot tekstus jaunām valodām, bet tikai otra opcija ļauj jums apskatīt un rediģēt tekstus visām esošajām izvēlnes raksturīgām atlasītās valodas ignorēm.

    - Rīkjoslā atlasiet **Pievienot**, lai atvērtu dialoglodziņu, kur varat pievienot vai rediģēt tekstus jebkurai atbalstītajā valodā. Iestatiet **Atsauces valodas** lauku valodai, kurai vēlaties apskatīt vērtības. Vērtības ir parādītas kreisajā kolonnā. Iestatiet **Tulkojumu valodas** lauku valodā, kas jāpievieno vai jāpielāgo. Kolonnā labajā pusē labojiet **Ievades virsraksta**, **Ievades instrukcijas**, **Apstiprināšanas nosaukumu** un **Instrukciju apstiprinājuma** lauku vērtības pēc nepieciešamības. Pēc tam atlasiet **Labi**.
    - Režģī atrodiet un atlasiet rindu, kur lauks **Valoda** ir iestatīts uz valodu, ko vēlaties rediģēt. Rīkjoslā atlasiet **Skatīt &lt;šī soļa valodas&gt; tulkojumus**, lai atvērtu dialoglodziņu, kurā var rediģēt tekstus visiem pieejamajiem izvēlētās valodas ignorējumiem. Dialoglodziņā ir iekļauts režģis, kurā ir rindas abiem standarta tekstiem (kur lauks **Izvēlnes elementa nosaukums** ir tukšs) un katram pieejamajam ignorēšanas tekstam (kur **Izvēlnes elementa nosaukuma** lauks ir iestatīts uz nosaukumu izvēlnes elementam, uz kuru attiecas ignorēšana). Kolonnā labajā pusē labojiet **Ievades virsraksta**, **Ievades instrukcijas**, **Apstiprināšanas nosaukumu** un **Instrukciju apstiprinājuma** lauku vērtības pēc nepieciešamības. Pēc tam atlasiet **Labi**.

1. Turpiniet darbu, līdz esat definējis katru nepieciešamo nosaukumu un instrukciju katrai nepieciešamajā valodā.

## <a name="add-menu-specific-overrides"></a>Pievienot izvēlnei raksturīgus ignorējumus

Kā tika norādīts iepriekšējā sadaļā, katram darbības ID varat izveidot jebkuru izvēlnei raksturīgo ignorējumu skaitu. Jūs variet izmantot šo spēju rediģēt un mainīt instrukcijas, lai tā labāk atbilst jūsu lokālajam biznesa procesam noteiktam izvēlnes elementam. Piemēram, pārdošanas izdošanai, ja uzņēmums parasti nodrošina darba ID darbiniekiem drukātā dokumentā, varat sniegt norādi, ka darbiniekiem jāsākas, skenējot darba ID.

Katra ignorēšana attiecas uz noteiktu mobilās ierīces izvēlnes vienumu un var ietvert jebkādu tulkojumu skaitu. Ja izvēlnes elementam nav ignorēšanas, izvēlnes elements izmanto standarta tekstus. Ja valodai nav definēts ignorēšanas tulkojums, tiek izmantoti standarta teksti pat tiem izvēlnes elementiem, kur ignorēšana ir definēta citām valodām.

Lai izveidotu un konfigurētu ignorējumu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Režģī atrodiet un atlasiet rindu, lai izveidotu ignorēšanu.
1. Darbību rūtī atlasiet **Pievienot darbības konfigurāciju**.
1. Nolaižamajā dialoglodziņā **Pievienot darbību konfigurāciju** iestatiet lauku **Izvēlnes vienums** uz tās mobilās ierīces izvēlnes vienuma nosaukumu, uz kuru attiecas ignorēšana. Pēc tam atlasiet **Labi**.
1. Redzama lapa parāda visus tekstus, kas ir pieejami jaunajai ignorēšanai. Sākotnēji tiek izveidota tikai viena valoda. Visas pārējās valodas turpinās izmantot standarta tekstus, ja vien šeit neieskaitīsiet šīs valodas. Rediģējiet tekstus un pievienojiet jaunas valodas atbilstoši aprakstam iepriekšējā sadaļā.
