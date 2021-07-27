---
title: Darba pasūtījuma projekta iestatījumi
description: Šajā tēmā ir paskaidrota darba pasūtījuma projekta iestatīšana Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 19cdc33fcc9d1293b235facbaffd1ccf62875217
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360057"
---
# <a name="work-order-project-setup"></a>Darba pasūtījuma projekta iestatījumi

[!include [banner](../../includes/banner.md)]

 

Modulī **Līdzekļu pārvaldība** ir nepieciešama projektu relācija katram darba pasūtījuma uzdevumam. Projekts, kas ir saistīts ar darba pasūtījuma uzdevumu, ļauj izsekot izmaksas dažādiem projektiem, kas saistīti ar Līdzekļu pārvaldību, piemēram, iekšējiem uzturēšanas projektiem, servisa pārvaldības projektiem un investīciju projektiem. 

## <a name="project-setup-for-a-work-order-job"></a>Projekta iestatīšana darba pasūtījuma uzdevumam

Kad izveidojat darba pasūtījuma uzdevumu darba pasūtījumā, projekta iestatīšana modulī **Projekta pārvaldība un uzskaite** un darba pasūtījuma projekta iestatīšana modulī **Līdzekļu pārvaldība** nosaka, kā projektus var izmantot izmaksu kontrolei līdzeklī, kas atlasīts šajā darba pasūtījuma uzdevumā. Šajā sadaļā aprakstītas šādas projekta iestatīšanas daļas, kas tiek izmantotas darba pasūtījumam: pamatprojekts (projekta ID), projekta veids, projekta darbības un finanšu dimensijas.

- Veidojot darba pasūtījuma uzdevumu darba pasūtījumā, tiek automātiski izveidots unikāls projekta ID un saistītas projekta darbības. Tomēr, ja vairāki darba pasūtījuma uzdevumi darba pasūtījumā ietver vienu un to pašu līdzekli, tiem tiek izmantots tas pats projekta ID. Citiem vārdiem sakot, viens projekta ID tiek izveidots katram līdzeklim darba pasūtījumā.

    - Pamatprojekts (projekta ID) darba pasūtījuma uzdevumam tiek atrasts pamatprojekta iestatījumos. (Plašāku informāciju par pamatprojekta iestatījumiem skatiet nākamajā sadaļā.) Piemēram, ja saistāt klientu vai funkcionālo novietojumu ar specifisku pamatprojektu, šis pamatprojekts tiek izmantots katru reizi, kad šim klientam izveidojat darba pasūtījumus vai funkcionālo novietojumu. Ja nesaistāt noteiktu projekta ID, piemēram, ar funkcionālo novietojumu, tiek izmantots nākamais atbilstošais pamatprojekts darba pasūtījuma projekta iestatījumos.
    - Katram projekta veidam ir nepieciešams norādīt projekta veidu. Projekta veids tiek atrasts projekta grupas iestatīšanas iestatījumos. (Papildinformāciju par projekta grupas iestatīšanu skatiet nākamajā sadaļā.) Ja projekta grupas iestatījumos nav atrasta atbilstība, tiek izmantots projekta grupas iestatījums pamatprojektā.
    - Iestatījumi projekta darbību pieprasīšanai prognozēs un žurnālos tiek kopēti no pamatprojekta uz darba pasūtījuma projektu. Opcijas **Stunda**, **Izdevumi** un **Krājuma** ir iestatītas uz **Jā** projektam, kas tiek izmantots kā pamatprojekts, projekta darbība ir obligāta prognozēm un žurnāliem. (Lai piekļūtu šīm opcijām, atlasiet **Projektu pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti** un pēc tam atlasiet projektu, kas tiek izmantots kā pamatprojekts. Opcijas ir sadaļā **Pieprasīt aktivitāti žurnālos**, kopsavilkuma cilnē **Iestatīšana**.)

- Finanšu dimensijas tiek kopētas no līdzekļa un sapludinātas ar pamatprojektu.

Nākamajā sadaļā ir paskaidrots, kā iestatīt pamatprojektus un projektu grupas. Pamatprojekts un pamatgrupas tiek izmantotas, lai kontrolētu darba pasūtījumus. Tās tiek izmantotas arī pārskatiem par darba pasūtījumiem.

## <a name="set-up-work-order-projects"></a>Darba pasūtījumu projektu iestatīšana

Pirms sākat veidot darba pasūtījumus, ir jāiestata darba pasūtījumu projekti. Lapa **Darba pasūtījuma projekta iestatīšana** (**Līdzekļa pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Projekta iestatīšana**) ietver divas cilnes: **Pamatprojekts** un **projekta grupa**.

Cilnē **Pamatprojekts** varat iestatīt projektu relācijas, ko var izmantot, ja projekts nav iestatīts uz līdzeklī, kas atlasīts darba pasūtījuma uzdevumā. Pamatprojekta iestatīšana nav nepieciešama, ja uzņēmums izmanto līdzekļu projektus. Tas ir svarīgi tikai tad, ja vēlaties izmantot darba pasūtījuma projektus līdzekļu projektu vietā. Šādā gadījumā ir jāiestata vismaz viens pamatprojekts.

Cilnē **Projektu grupa** varat iestatīt projektu grupas, ko var saistīt ar darba pasūtījuma veidiem, līdzekļu veidiem un līdzekļiem.

Projektu grupas var izmantot, lai izveidotu noteiktas kategorijas (grupas), kas tiek izmantotas izmaksu kontrolei. Piemēram, izveidojot projektu grupas noteiktiem līdzekļu veidiem vai darba pasūtījuma veidiem, varat veikt detalizētu uzturēšanas izmaksu uzskaiti pēc veida.

Projektu grupas nav obligātas. Ja neiestatāt projektu grupas, pamatprojekts tiek izmantots, lai noteiktu projekta grupu, un pakārtotais projekts tiek izveidots no pamatprojekta projektu grupas.

Iestatīšana nodrošina pilnīgu integrāciju ar moduli **Projektu pārvaldība un uzskaite**. Tāpēc varat izsekot izmaksas, kas saistītas ar darba pasūtījumiem saistītajos projektos. Šajā procedūrā aprakstīta darba pasūtījuma projekta iestatīšana.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Projekta iestatīšana**.
2. Cilnē **Pamatprojekts** atlasiet **Pievienot**.
3. Laukos **Darba pasūtījuma tips**, **Funkcionālais novietojums**, **Līdzekļa veids** un **Līdzeklis** atlasiet jums nepieciešamās vērtības. Katrai rindai, kuru pievienojat, varat iestatīt tikai vienu lauku vai vairākus laukus. Iestatītais lauku skaits nosaka kombināciju, kas tiek izmantota, kad Līdzekļu pārvaldībā tiek atlasīts projekta ID. 

    Ja atlasāt funkcionālo novietojumu, tiek automātiski iekļautas saistītās pakārtotās atrašanās vietas. Ja atlasāt līdzekli, varat izveidot papildu darba pasūtījuma projekta iestatīšanas rindas vienam un tam pašam līdzeklim, bet šim pamatlīdzeklim varat atlasīt dažādus projektus.

4. Laukā **Projekta ID** atlasiet projektu, kam jābūt saistītam ar iestatījumiem, ko izveidojāt 3. darbībā.
5. Ja projekta iestatījumam ir jābūt derīgam tikai ierobežotu laika periodu, laukā **Beigu datums** atlasiet beigu datumu. Pretējā gadījumā atlasiet **Nav**.

    Pēc noklusējuma sākuma datums ir datums, kad pievienojat darba pasūtījuma projektu lapai. To kontrolē lauks **Derīgs no**, kas pēc noklusējuma ir paslēpts. Lai parādītu lauku **Derīgs no**, atlasiet **Skatīt** \> **Visu**. Pēc tam varat izmantot lauku **Derīgs no** kopā ar lauku **Beigu datums**, lai iestatītu ierobežotu derīguma periodu darba pasūtījuma projektam.

    ![Darba pasūtījuma projekta iestatījumu lapa.](media/17-setup-for-work-orders.png)

6. Cilnē **Projekta grupa** atlasiet **Pievienot**.
7. Laukā **Darba pasūtījuma veids** atlasiet darba pasūtījuma veidu.
8. Ja vēlaties, lai projektu grupas saistība būtu konkrētāka, atlasiet līdzekļa veidu laukā **Līdzekļa veids** vai līdzekli laukā **Līdzeklis**.
9. Laukā **Projekta grupa** atlasiet projekta grupu, kas ir jāsaista uz darba pasūtījuma veidu. Piemēram, darba pasūtījuma veids, kura nosaukums ir **Profilaktiskā uzturēšana**, var būt saistīts ar projektu grupu, kuras nosaukums **Prof. uzt.** vai **Iekšējs**. Alternatīvi, darba pasūtījuma veidu **Investīcija**, kas tiek izmantots darba pasūtījumiem, kas ir saistīti ar investīcijām un līdzekļiem, var saistīt ar projekta grupu **Investēt** vai **Investīcija**.
10. Atlasiet **Saglabāt**.

![Darba pasūtījumu projekta iestatīšanas lapa, Pievienot darba pasūtījumu.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Katru reizi, kad tiek izveidota darba pasūtījuma rinda, Līdzekļu pārvaldība meklē projektu grupu, kas jāsaista ar darba pasūtījuma uzdevuma projektu. Meklēšana ir balstīta uz iestatījumiem, kas aprakstīti šajā tēmā. Katrai projekta grupai ir saistīts projekta veids. Projekta grupas, kuru projekta veids ir **Laiks un materiāls** vai **Fiksēta cena**, ir derīgas tikai līdzekļiem, kas ir saistīti ar klienta kontu.
>
> Pamatprojektiem un projektu grupām, kad sistēma atlasa pieejamo darba pasūtījuma projektu vai projektu grupu, atlase ir balstīta uz ierakstiem, ko izveidojāt, izmantojot iepriekšējo procedūru. Līdzekļu pārvaldība izskata ierakstus, kas ir saistīti ar darba pasūtījuma projektu, lai pārbaudītu iespējamo atbilstību. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, darba pasūtījuma pamatprojektam Līdzekļu pārvaldība sākumā pārbauda iespējo atbilstību laukam **Līdzeklis**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Līdzekļa veids**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Funkcionālais novietojums** un tā tālāk. Kā jūs varat redzēt lapas **Darba pasūtījuma projekta iestatīšana** izkārtojumā, šī uzvedība nozīmē, ka, lai atrastu specifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso. Ja atbilstība netiek atrasta, tiek izmantots noklusējuma ieraksts, kurā tiek atlasīts tikai projekta ID. Saistītās projektu grupas atrašanas process ir līdzīgs. Līdzekļu pārvaldība vispirms pārbauda iespējamo atbilstību laukam **Līdzeklis** un tad laukam **Līdzekļa veids**, un tad laukam **Darba pasūtījuma tips**. Ja atbilstība netiek atrasta, tiek izmantots noklusējuma ieraksts, kurā tiek atlasīta tikai projekta grupa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]