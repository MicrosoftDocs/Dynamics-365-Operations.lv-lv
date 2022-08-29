---
title: Pabeigto preču fiziski pieejams pirms grāmatošanas žurnālos
description: Kad saražotais krājums ir reģistrēts kā pabeigts, tas tiek reģistrēts kā pieejams tālākai fiziskai apstrādei, un tiek grāmatots viens vai vairāki žurnāli. Šajā rakstā ir aprakstīts, kā atlikto maksājumu žurnālu grāmatojumi, iespējojot to apstrādi ar pakešuzdevumu ziņojumu rindā.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7a8327552d9e6c38721fdac9ee1795e61f90f329
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266501"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Pabeigto preču fiziski pieejams pirms grāmatošanas žurnālos

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kad darbinieks ziņo par saražotā krājuma pabeigšanu, sistēma reģistrē to kā pieejamu turpmākai fiziskajai apstrādei (piemēram, nosūtīšanai vai izvietošanas ceļam). Šī procesa laikā tiek grāmatots arī viens vai vairāki žurnāli (piemēram, pārskats kā pabeigts žurnāls, izdošanas saraksta žurnāls un maršruta kartes žurnāls). Ja vēlaties savus krājumus padarīt fiziski pieejamus pirms visu grāmatojumu apstrādes, var iestatīt sistēmu atlikt žurnāla grāmatojumus. Atlikto maksājumu grāmatošana tad tiek pārvaldīta ar pakešuzdevumu, kas apstrādās grāmatojumus, ko pieļauj sistēmas resursi.

Šajā attēlā parādīts, kā žurnālu grāmatošanas procesi tiek izsaukti gan ar, gan bez atliktas grāmatošanas.

![Pabeigtais process ar atlikto maksājumu žurnāla grāmatošanu un bez tā.](media/deferred-posting-flowchart.png "Pabeigtais process ar atlikto maksājumu žurnāla grāmatošanu un bez tā")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Ieslēgt atlikto maksājumu žurnāla grāmatošanu jūsu sistēmā

Pirms atlikto maksājumu žurnāla grāmatošanas ir jābūt ieslēgtai savā sistēmā. Administratori var izmantot līdzekļu [pārvaldības darbvietu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu funkcijas statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Ražošanas kontrole*
- **Funkcionalitātes nosaukums:** *(priekšskatījums) Pirms grāmatošanas žurnālos fiziski pieejamās pabeigtās preces*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Iestatīt žurnāla grāmatošanas opcijas pabeigšanai

Darbinieki var ziņot, ka krājumi ir pabeigti, izmantojot jebkuru no šiem klientiem:

- Tīmekļa klients
- Noliktavas pārvaldības mobilā programma
- Ražošanas izpildes interfeiss

Tīmekļa klients izmanto tādu pašu grāmatošanas metodes konfigurāciju kā mobilo programmu Noliktavas pārvaldība. Tomēr grāmatošanas metode, ko lieto ražošanas izpildes interfeiss, jākonfigurē atsevišķi.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Iestatiet žurnāla grāmatošanas opcijas tīmekļa klientam un noliktavas pārvaldības mobilajai programmai

Mobilajā programmā darbinieki ziņo, ka krājumi ir pabeigti, atverot mobilās ierīces izvēlnes vienumu, **kur darba izveides procesa** *·* *vērtība ir Ziņot, kā pabeigtu vai Ziņot, kā pabeigtu, un izvietošana.* Tīmekļa klientā darbinieki ziņo, ka krājumi ir pabeigti no **visu ražošanas pasūtījumu** saraksta lapas vai **no lapas Ražošanas pasūtījums (detalizēta** informācija). Varat konfigurēt uzņēmuma līmeņa noklusējuma metodi un arī iestatīt noliktavai raksturīgās ignorēšanas pēc prasības.

Izmantojiet šo procedūru, lai konfigurētu uzņēmumā plaši izmantoto noklusējuma grāmatošanas metodi vienumu pabeigšanai no tīmekļa klienta vai no mobilās programmas Noliktavas pārvaldība.

1. Pārejiet uz **ražošanas kontroles iestatījuma \>\> ražošanas kontroles parametriem**.
1. Cilnes Žurnāli **sadaļā Ziņot kā pabeigtu** žurnālu iestatiet **grāmatošanas** **metodes** lauku uz vienu no šīm vērtībām:

    - *Tūlītējā* – kad krājums ir fiziski pabeigts, sistēma pilnībā apstrādā visus saistītos žurnālu grāmatojumus, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.
    - *Atlikts* – kad krājums ir ziņots kā pabeigts, sistēma atzīmē pabeigto krājumu kā fiziski pieejamu un pievieno žurnāla grāmatojumus ziņojumu rindai. Sistēma negaida, kamēr grāmatojumi būs pilnībā apstrādāti, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.

Izmantojiet šo procedūru, lai konfigurētu noliktavai raksturīgos ignorējumus noklusējuma grāmatošanas metodei, kas ir konfigurēta ražošanas **kontroles parametru** lapā.

1. Dodieties uz **Noliktavas pārvaldības \> Iestatījuma \> Krājumu \> sadalījuma Noliktavas**.
1. Atlasiet noliktavu, ko vēlaties iestatīt.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnes **Noliktava** sadaļā Ražošanas pasūtījumi **iestatiet** laukā Grāmatošanas **metode** vienu no šīm vērtībām:

    - *Mantot* - atlasītā noliktava manto iestatījumu no ražošanas **kontroles parametru** lapas.
    - *Tūlītējā* – kad krājums ir fiziski pabeigts, sistēma pilnībā apstrādā visus saistītos žurnālu grāmatojumus, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.
    - *Atlikts* – kad krājums ir ziņots kā pabeigts, sistēma atzīmē pabeigto krājumu kā fiziski pieejamu un pievieno žurnāla grāmatojumus ziņojumu rindai. Sistēma negaida, kamēr grāmatojumi būs pilnībā apstrādāti, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Iestatīt ražošanas izpildes interfeisa žurnāla grāmatošanas opcijas

Izmantojiet šo procedūru, lai konfigurētu grāmatošanas metodi, kas tiek izmantota, kad krājumi ir pabeigti no ražošanas izpildes interfeisa.

1. Pārejiet uz **Sadaļu Ražošanas kontroles \> iestatījumi \> Ražošanas izpildes ražošanas \> pasūtījuma noklusētie iestatījumi**.
1. Cilnes Ziņot **kā pabeigtu sadaļā** Ziņot **kā** **pabeigtu** žurnālu lauku Grāmatošanas metode iestatiet uz vienu no šīm vērtībām:

    - *Tūlītējā* – kad krājums ir fiziski pabeigts, sistēma pilnībā apstrādā visus saistītos žurnālu grāmatojumus, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.
    - *Atlikts* – kad krājums ir ziņots kā pabeigts, sistēma atzīmē pabeigto krājumu kā fiziski pieejamu un pievieno žurnāla grāmatojumus ziņojumu rindai. Sistēma negaida, kamēr grāmatojumi būs pilnībā apstrādāti, pirms tas atzīmē pabeigto krājumu kā fiziski pieejamu.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Ieplānot ziņojumu procesora pakešuzdevumu atlikto grāmatojumu apstrādāšana

Ziņojumu procesora pakešuzdevums ir atbildīgs par žurnāla grāmatojumu apstrādi pēc tam, kad tie ir ievietoti rindā. Lai nodrošinātu žurnāla grāmatojumu apstrādi, šis darbs jākonfigurē tā, lai tas tiktu veikts regulārā intervālā. Lai iestatītu nepieciešamo pakešuzdevumu, izmantojiet tālāk norādītās darbības.

1. Dodieties uz **sistēmas administrēšanas \> ziņojumu procesora \> ziņojumu procesoru**.
1. Kopsavilkuma cilnē **Parametri** iestatiet ziņojumu rindas **lauku** uz *Ražošana*.
1. Kopsavilkuma cilnes **Fonā cilnē Palaist** iestatiet opciju Pakešapstrāde **uz** *Jā*. Pēc tam iestatiet periodisku grafiku un konfigurējiet citus iestatījumus pēc vajadzības. Iestatījumi darbojas tāpat, kā tie darbojas citu veidu fona [darbiem programmā](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Atlikto grāmatojumu norises izsekošana

Atliktie žurnālu grāmatojumi tiek ievietoti rindā kā ziņojumu procesora *ziņojumi,* kas gaida, līdz tos apstrādā ziņojumu *procesors*. Ziņojumu procesors jāiestata, lai palaistu kā ieplānotu pakešuzdevumu. Lai skatītu atliktos grāmatošanas ziņojumus, kas ir vai tiks apstrādāti ar ziņojumu procesoru, **dodieties uz Ražošanas \> kontroles ražošanas \> pasūtījumu atliktā ražošanas pasūtījuma grāmatošanu**.

### <a name="message-grid-columns-and-filters"></a>Ziņojumu režģa kolonnas un filtri

Varat izmantot laukus atliktās ražošanas pasūtījumu **grāmatošanas lapas augšpusē**, lai palīdzētu atrast visus jūsu meklētos konkrētos ziņojumus.

Pieejami tālāk norādītie filtri.

- **Ziņojuma tips** – norāda režģī parādīto ziņojumu tipu.
- **Ziņojuma stāvoklis** – norāda režģī rādīto ziņojumu stāvokli. Pastāv sekojošos valstu:

    - *Ievietots rindā* – Ziņojumu ir gatavs ziņojuma procesora apstrādei.
    - *Apstrādāts* – Ziņojuma procesors veiksmīgi apstrādāja ziņojumu.
    - *Atcelts* – ziņojumu neizdevās apstrādāt pēdējā mēģinājuma laikā, un lietotājs to atcēla.
    - *Neizdevās* - ziņojumu neizdevās apstrādāt pēdējā mēģinājuma laikā. Sistēma izmēģinās neizdevušos ziņojumus trīs reizes. Pēc tam tas atstās un atstās paziņojumu neizdevušās *stāvoklī*. Ņemiet vērā, ka ziņojumu nevar atcelt manuāli vai rediģēt līdz pēdējam no šiem trim mēģinājumiem.

- **Zīņojuma saturs** - Šis filtrs veic pilnu teksta meklēšanu ziņojuma saturam. (Režģī nav parādīts ziņojuma saturs.) Filtrs visbiežāk apzīmē īpašos simbolus (piemēram, defises) kā atstarpes rakstzīmes, un tas apstrādā visas atstarpes rakstzīmes kā Būla VAI operatorus. Piemēram, ja meklējat noteiktu vērtību, `journalid` kas ir vienāda ar *USMF-123456*, sistēma atradīs visus ziņojumus, kuros ir "USMF" vai "123456". Šādā gadījumā, iespējams, rezultātu saraksts būs garš. Tāpēc labāk ir ievadīt tikai *123456*, jo tiks iegūti precīzāki rezultāti.

Sarakstu var arī kārtot un filtrēt, atlasot jebkuru no kolonnu virsrakstiem un ievadot kritērijus nolaižamajā dialoglodziņā.

### <a name="view-the-message-log-message-content-and-details"></a>Apskatīt ziņojumu žurnālu, ziņojuma saturu un detalizētu informāciju

Detalizētu informāciju par ziņojumu var **atrast** **·**, atlasot to režģī un pēc tam ziņojumu režģa cilnē Atlasot cilni Žurnāls vai Neapstrādāts saturs, kur tiek rādīts katrs apstrādes notikums.

Rīkjosla cilnē **Žurnāls** ietver šādas pogas:

- **Žurnāls** – izvēlieties šo pogu, lai parādītu apstrādes rezultātus. Šī poga ir īpaši noderīga, ja **ziņojumiem ir** *apstrādes rezultāta vērtība* Neizdevās un jūs vēlaties uzzināt apstrādes kļūmes iemeslus.
- **Komplekts** – vairākas ziņojumu apstrādes operācijas var tikt izpildītas kā daļa no vienas un tās pašas pakešapstrādes. Izvēlieties šo pogu, lai aplūkotu šos detalizētos datus. Piemēram, var redzēt, vai dažiem ziņojumiem pastāv atkarības, kurām nepieciešams specifisks apstrādes pasūtījums.

### <a name="manually-process-or-cancel-a-message"></a>Manuāli apstrādāt vai atcelt ziņojumu

Jūs varat manuāli apstrādāt vai atcelt ziņojumu pēc pieprasījuma, atkarībā no tā pašreizējā stāvokļa. Atlasiet režģī ziņojumu un pēc tam darbību **rūtī** atlasiet **Apstrādāt** vai Atcelt.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Iestatīt biznesa notikumus, lai piegādātu brīdinājumus par nesekmīgiem apstrādes rezultātiem

Varat iestatīt biznesa notikumus [, kas jūs brīdina](../../fin-ops-core/dev-itpro/business-events/home-page.md) par neizdevušās apstrādes rezultātiem. Dodieties uz **sistēmas administrēšanas \> iestatīšanas \>\> biznesa notikumu** biznesa notikumu katalogu un aktivizējiet biznesa notikumu, ko sauc par ziņojumu *procesora ziņojumu*.

Kā aktivizēšanas procesa daļu jums tiek piedāvāts norādīt, vai notikums ir specifisks vienai juridiskajai personai vai attiecas uz visām juridiskajām personām. Tiek prasīts norādīt arī galapunkta **nosaukuma** vērtību. Šī vērtība ir jādefinē vispirms.

> [!NOTE]
> Ja lauks **Kad rodas biznesa** *Microsoft Power Automate* notikums ir iestatīts (*piemēram, HTTPS* vietā), **galapunkta** nosaukuma vērtība tiek automātiski izveidota Piegādes ķēžu pārvaldībā, balstoties uz *Microsoft Power Automate* iestatījumiem.
