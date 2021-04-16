---
title: Vispārējās plānošanas iestatīšanas vednis
description: Šajā tēmā ir aprakstītas dažādas svarīgas stratēģijas un parametri, kas tiek izmantoti vispārējās plānošanas iestatīšanai.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 770800e63de73c60e0e811734d4273ff2392620f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829695"
---
# <a name="master-planning-setup-wizard"></a>Vispārējās plānošanas iestatīšanas vednis

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts ceļvedis **Vispārējās plānošanas iestatīšanas vednim**. Tajā ir paskaidrots, kā tiek aprēķināti parametru ieteikumi, kā arī sniegti piemēri, kas parāda, kā dažādi uzņēmumi iestata vispārējo plānošanu, pamatojoties uz to biznesa vajadzībām.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

Videoklips [Galvenais plānošanas iestatīšanas vednis programmā Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (parādīts iepriekš) ir ietverts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams vietnē YouTube.


## <a name="specific-requirements-of-your-company"></a>Jūsu uzņēmuma specifiskās prasības

Vedņa pirmajā lapā tiek jautāts par jūsu uzņēmuma īpašajām prasībām. Jūsu atbildēm uz šiem jautājumiem nav jābūt precīzām, bet jums ir jāspēj norādīt aptuvenu krājumu un plānoto pasūtījumu skaitu, kas būs juridiskajai personai. Jūsu atbildes tiek izmantotas, lai konfigurētu parametrus, kas attiecas uz jūsu juridisko personu, nevis tikai uz atlasīto vispārējo plānu. Turpmākajās sadaļās aprakstīti aprēķinātie parametri un izmantotās formulas.

### <a name="number-of-threads"></a>Pavedienu skaits

- **Ja ražojat kādu no šiem krājumiem:** Pavedienu skaits = Plānoto pasūtījumu skaits ÷ 1000
- **Ja neražojat nevienu no šiem krājumiem:** Pavedienu skaits = Krājumu skaits ÷ 1000

Ja aprēķinātais pavedienu skaits pārsniedz 75 procentus no pieejamā pavedienu skaita, tas tiek ierobežots 75 procentu apmērā no pavedienu skaita, kas ir pieejams katram debitoram. (Katram debitoram tiks noteikts pieejamo pavedienu skaits.)

Papildinformāciju skatiet sadaļā [Pavedienu skaits](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Komplekta lielums

Komplekta lielums tiks iestatīts uz **1**. Šī vērtība bieži vien ir vislabākā vērtība, jo tā palīdz uzlabot vispārējās plānošanas izpildi.

Papildinformāciju skatiet sadaļā [Uzdevumu skaits palīga uzdevumu komplektā](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Apstiprināšanas komplekta lielums

- **Ja ražojat kādu no krājumiem:** apstiprināšanas komplekta lielums tiks iestatīts uz lielāko no šīm divām vērtībām: **10** un komplekta aprēķins
- **Ja neražojat nevienu no krājumiem:** apstiprināšanas komplekta lielums tiks iestatīts uz lielāko no šīm divām vērtībām: **50** un komplekta aprēķins

Komplekta aprēķins = (Plānoto pasūtījumu skaits × (Apstiprināšanas laika periods ÷ Vajadzības laika periods) ÷ Pavedienu skaits) ÷ 10

### <a name="cache-size"></a>Kešatmiņas lielums

Kešatmiņas lielums tiks iestatīts uz **Maksimums**. Šī vērtība bieži vien ir vislabākā vērtība, jo tā palīdz uzlabot vispārējās plānošanas izpildi.

Papildinformāciju skatiet sadaļu [Iedalīt laiku darbiem darbu komplektā](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Ražošanas iestatīšana

Ja ražojat krājumus, vēlāk vednī tiks parādīta lapa **Ražošanas iestatīšana**.

## <a name="scope-of-the-current-plan"></a>Pašreizējā plāna tvērums

Vedņa lapā **Pašreizējā plāna tvērums** jūs atbildat uz jautājumiem, kas saistīti ar to, cik tālu turpmāk vispārējā plānošanā tiks izskatītas un aprēķinātas dažādas prasības. Katrā jautājumā tiek jautāts, vai vēlaties izmantot funkciju un kā to konfigurēt.

Piemēram, budžeta plāna funkcijai vednis vaicā: "Vai vēlaties izmantot budžeta plānu vispārējā plānošanā, lai plānotie pasūtījumi tiktu ieteikti tā, lai izpildītu prognozēto pieprasījumu?"

Pieejamas šādas opcijas:

- **Nē** — vispārējā plānošana neieteiks plānotos pasūtījumus, lai izpildītu prognozi. Cilnē **Laika periodi** lapā **Vispārējie plāni** (**Vispārējā plānošana \> Iestatīšana \> Plāni \> Vispārējie plāni**) vednis iestatīs opciju **Budžeta plāns (laika periods)** uz **Jā** un dienu skaitu iestatīs uz **0** (nulle). Šis iestatījums ignorēs laika periodu, kas ir norādīts vajadzību grupā. Tā kā dienu skaits ir iestatīts uz **0** (nulle), šī funkcija netiks izmantota.
- **Jā, kā definēts šajā vispārējā plānā** — kļūst pieejams lauks, kur var ievadīt dienu skaitu, ko vispārējā plānošana ieteiks plānotajiem pasūtījumiem, lai izpildītu prognozēto pieprasījumu. Vednis iestatīs opciju **Budžeta plāns (laika periods)** uz **Jā** un dienu skaitu iestatīs uz to dienu skaitu, kas ir ievadīts laukā **Budžeta plāns** cilnē **Laika periodi** lapā **Vispārējie plāni**. Šis iestatījums ignorēs vērtības, kas ir iestatītas vajadzību grupās.
- **Jā, kā definēts vajadzībā**— vednis iestatīs opciju **Budžeta plāns (laika periods)** uz **Nē.** Laika periodi, kas norādīti vajadzību grupā, tiks izmantoti, lai norādītu, cik ilgi tiks plānota prognoze.

Atlikušajos jautājumos šajā lapā un atbildēs uz tiem tiek ievērota tā pati shēma:

- **Nē** — opcija **Budžeta plāns (laika periods)** tiks iestatīta uz **Jā**, bet dienu skaits tiks iestatīts uz **0** (nulle).
- **Jā, kā definēts vispārējā plānā**— Opcija **Budžeta plāns (laika periods)** tiks iestatīta uz **Jā**. Ievadīto dienu skaits tiks izmantots un ignorēs vērtības, kas ir iestatītas vajadzību grupās.
- **Jā, kā definēts vajadzību grupā**— opcija **Budžeta plāns (laika periods)** tiks iestatīta uz **Nē**.

Plašāku informāciju skatiet nodaļā [Darbu plānošana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Plānošanas opcijas

Lapa **Plānošanas opcijas** tiek parādīta tikai tad, ja atbildējāt **Jā** uz jautājumu "Vai ražojat kādu no plānotajiem krājumiem? " vedņa pirmajā lapā.

Jūsu atbilde uz pirmo jautājumu šajā lapā ("Vai jums ir nepieciešams ieplānot operācijas, kas sadalītas atsevišķos darbos?") nosaka plānošanas metodi lapas **Vispārējie plāni** cilnē **Vispārējie plāni**.

- **Jā** — tiks izmantota darbu plānošana.
- **Nē** — tiks izmantota operāciju plānošana.

Plašāku informāciju skatiet nodaļās [Operāciju plānošana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) un [Darbu plānošana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Pieprasījuma un piedāvājuma atjauninājumi

Jautājumi lapā **Pieprasījuma un piedāvājuma atjauninājumi** ir saistīti ar apstiprināšanu, darbības ziņojumiem un kavēšanos.

Vispārējās plānošanas iestatījumi tiks atjaunināti, pamatojoties uz jūsu atbildēm saskaņā ar to pašu shēmu, kas aprakstīta iepriekšējā sadaļā:

- **Nē** — opcija **Laika periods** lapā **Vispārējie plāni** tiks iestatīta uz **Jā**, bet dienu skaits tiks iestatīts uz **0** (nulle).
- **Jā, kā definēts vispārējā plānā**— opcija **Laika periods** tiks iestatīta uz **Jā**. Ievadīto dienu skaits tiks izmantots un ignorēs vērtības, kas ir iestatītas vajadzību grupās.
- **Jā, kā definēts vajadzību grupā**— opcija **Laika periods** tiks iestatīta uz **Nē**.

Aprēķinātajām aizkavēm jūsu atbildes uz jautājumiem vednī atjauninās atbilstošos parametrus lapas **Vispārējie plāni** cilnē **Aprēķinātā aizkavēšanās**.

## <a name="summary-of-your-changes"></a>Jūsu veikto izmaiņu kopsavilkums

Vedņa pēdējā lapā ir redzamas izmaiņas, kas ir ieteicamas, pamatojoties uz jūsu atbildēm. Tajā ir redzama gan iestatījuma vērtība (**Pašreizējais iestatījums**), gan vedņa ieteiktā vērtība (**Jauna konfigurācija**).

Varat arī modificēt parametrus jaunajā konfigurācijā. Parametri tiek sadalīti parametros, kas attiecas uz jūsu juridisko personu un parametros, kas attiecas tikai uz atlasīto vispārējo plānu. Lai skatītu visus iestatījuma parametrus, kurus var mainīt, izmantojot vedni, lapas apakšdaļā atlasiet **Rādīt visus parametrus**. Pēc tam parametrus var mainīt.

Visbeidzot, atlasot **Pabeigt**, tiek lietota jaunā konfigurācija. Ja atlasāt **Atcelt**, neviena no veiktajām izmaiņām netiek lietota.

## <a name="examples"></a>Piemēri

Šajā sadaļā ir aprakstīts, kā iestatīt divus fiktīvus uzņēmumus, lai parādītu, kā iestatījums var mainīties atkarībā no katra uzņēmuma vajadzībām.

### <a name="example-1-contoso-manufacturer"></a>1. piemērs: Contoso Manufacturer

Contoso Manufacturer ir ražošanas uzņēmums, kas ražo skaļruņus. Tas no dažādiem piegādātājiem iepērk dažādus izejmateriālus un komponentus, ko izmanto galīgajiem skaļruņiem. Šeit ir dažas tā piegādes un ražošanas īpašības:

- Pēdējiem krājumiem, kurus uzņēmums ražo, ir materiālu komplekta (MK) struktūra.
- Visas gala preces un komponentus plāno, izmantojot vispārējo plānošanu. Manuālā plānošana nav veikta.
- Katra galīgā krājuma ražošanai tiek noteikts operāciju maršruts.
- Ražotne ražo gala krājumus. Tam ir noteikts skaits frēzēšanas un urbšanas mašīnu, kas tiek izmantotas komponentu apstrādei. Šīm mašīnām ir jāapstrādā dažādie komponenti.
- Ir daudz piegādātāju. Vidējais krājumu izpildes laiks ir viena nedēļa. Krājumu grupai no tā paša piegādātāja būs septiņu nedēļu izpildes laiks.

Vednī Contoso Manufacturer tiek ievadītas šādas vērtības:

- **Vajadzība:**

    - **Jautājums:** "Vai vēlaties norādīt jūsu plānošanas diapazona dienu skaitu?"
    - **Atbilde:** "Jā, kā definēts vajadzību grupās."

    Tā kā krājumu izpildes laiks ir ļoti atšķirīgs, Contoso nav jāplāno visi krājumi tajā pašā periodā nākotnē. Krājumu vajadzību grupas ir izveidotas. Krājumi ar līdzīgu izpildes laiku tiek piešķirti tai pašai vajadzības grupai. Plānošanas diapazons katrai vajadzību grupai (tas ir, vajadzības laika periods) ir aptuveni izpildes laiks plus vienas nedēļas rezerve. Vispārējā plānošana pēc tam nodrošina, ka krājumi tiek plānoti iepriekš, pamatojoties uz to izpildes laiku.

    Tādēļ šim piemēram tiks izveidotas divas vajadzību grupas. Vienai vajadzību grupai būs divu nedēļu vajadzības laika periods, bet otrai būs astoņu nedēļu vajadzības laika periods.

    Ja kā atbilde ir atlasīts **Jā, kā tas ir definēts šajā vispārējā plānā** ievadīto dienu skaitam vajadzētu pārsniegt visu krājumu garāko izpildes laiku. Tomēr, tā kā daudzi krājumi nav jāplāno tik tālu iepriekš, daudzi plānotie pasūtījumi tiks aprēķināti, bet nekad netiks izmantoti. Tādēļ vispārējās plānošanas izpildes laiks palielināsies.

- **Plānošana:**

    - **Jautājums:** "Vai jums ir nepieciešams plānot operācijas, kas sadalītas atsevišķos darbos?"
    - **Atbilde:** "Jā."

    Contoso Manufacturing ir jāplāno un jāieplāno atsevišķie darbi, kas tiks veikti ražotnē. Tāpēc uzņēmums izmantos darbu plānošanu.

- **Noslodze:**

    - **Jautājums:** "Vai vēlaties plānot, izmantojot resursu noslodzi?"
    - **Atbilde:** "Jā, kā definēts šajā vispārējā plānā." Tiek ievadītas **10 dienas**.

    Malšanas un urbšanas iekārtu skaits ir ierobežots. Ražošanas plānošanā ir jāņem vērā šis ierobežojums un laikus jāorganizē darbi atbilstoši resursu noslodzei. Citiem vārdiem sakot, ieplānotie darbi tiks pārplānoti, pamatojoties uz resursu ierobežojumiem. Plānošanā tiks izmantots izpildes laiks papildus definētajam periodam. (Plānotie ražošanas pasūtījumi var pārklāties.) Tā kā krājumu ražošanas izpildes laiks ir septiņas dienas, resursu noslodze vispārējās plānošanas laikā tiks izskatīta 10 dienu laikā.

- **Secība:**

    - **Jautājums:** "Vai vēlaties sakārtot secībā plānotos pasūtījumus, izmantojot preces secības vērtības?"
    - **Atbilde:** "Jā, kā definēts vajadzību grupās."

    Katra galīgā krājuma ražošanai tiek noteikts maršruts. Tāpēc vispārējā plānošana laikus ieplāno pasūtījumus atbilstoši definētajiem maršrutiem.

- **Izvēršana:**

    - **Jautājums:** "Vai vēlaties plānot pasūtījumus visiem materiālu komplekta elementiem (plāns primārajiem krājumiem un visiem pakārtotajiem krājumiem)?"
    - **Atbilde:** "Jā, kā definēts vajadzību grupās."

    Ir jāplāno visi krājumi, kas tiek izmantoti ražošanā. Tā kā krājumiem ir ļoti atšķirīgi izpildes laiki, vispārējā plānošana nodrošinās labāku veiktspēju, kad tā izmanto vajadzību grupas. Atkal, var ievadīt vienas nedēļas rezervi, un izvēršanu var veikt tādam pašam laikam kā vajadzība.

### <a name="example-2-contoso-retailer"></a>2. piemērs: Contoso Retailer

Contoso Retailer ir izplatīšanas uzņēmums modes industrijā. Tas izmanto vispārējo plānošanu, lai aprēķinātu, kad ir jāievieto pirkšanas pasūtījumi, pamatojoties uz prognozēto pārdošanas apjomu. Šeit ir dažas tā īpašības:

- Contoso Retailer izmanto pieprasījuma apjoma prognozi, lai paredzētu pārdošanu. Pirkšanas pasūtījumi tiks plānoti saskaņā ar šo prognozi.
- Veikalos tiek izmantots pieprasījums papildināšanai.
- Izpildes laiks no galvenās noliktavas līdz katram veikalam ir aptuveni divas nedēļas visiem krājumiem.

Vednī Contoso Retailer tiek ievadītas šādas vērtības:

- **Pieprasījuma apjoma prognoze:**

    - **Jautājums:** "Vai vēlaties izmantot budžeta plānu vispārējā plānošanā, lai plānotie pasūtījumi tiktu ieteikti tā, lai izpildītu prognozēto pieprasījumu?"
    - **Atbilde:** "Jā, kā definēts šajā vispārējā plānā."

    Contoso ir iekļāvis pieprasījuma apjoma prognozi, lai prognozētu tā pārdošanu. Tāpēc vispārējā plānošanā ir jāiesaka plānotie pasūtījumi, lai izpildītu prognozi.

- **Apstiprināšana:**

    - **Jautājums:** "Vai vēlaties, lai vispārējā plānošana automātiski apstiprinātu plānotos pasūtījumus pasūtījumu dokumentos, piemēram, ražošanas vai pirkšanas pasūtījumos?"
    - **Atbilde:** "Jā, kā definēts šajā vispārējā plānā." Tiek ievadīta **1 diena**.

    Tā kā Contoso Retailer izveidos pirkšanas pasūtījumus tieši no plānotajiem pirkšanas pasūtījumiem, tas ir lietderīgi, ja plānotie pirkšanas pasūtījumi tiks automātiski apstiprināti. Tā kā uzņēmums veic vispārējo plānošanu katru dienu, vienas dienas apstiprināšanas laika periods automātiski apstiprinās visus pasūtījumus, kas ir nepieciešami nākamajai dienai.

- **Apstiprinātie pieprasījumi:**

    - **Jautājums:** "Vai vēlaties iekļaut pieprasījumu no apstiprinātajiem pieprasījumiem, lai papildinātu mazumtirdzniecības veikalus?"
    - **Atbilde:** "Jā, kā definēts šajā vispārējā plānā." Tiek ievadīta **1 diena**.

    Contoso izmanto apstiprinātos pieprasījumus no saviem veikaliem, lai izveidotu plānotos pirkšanas pasūtījumus šo veikalu papildināšanai. Tā kā vispārējā plānošana tiek palaista katru dienu, plānošanā tiks iekļauti pieprasījumi no pēdējās dienas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]