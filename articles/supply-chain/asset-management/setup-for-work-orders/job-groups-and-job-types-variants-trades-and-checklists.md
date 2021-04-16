---
title: Uzturēšanas darba tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu amatu un uzturēšanas kontrolsaraksti
description: Šajā tēmā aprakstītas darba tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu amati un uzturēšanas kontrolsaraksti Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb73fb36ee31d93b2121437d57d959ba6c01a337
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842277"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Uzturēšanas darba tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu amatu un uzturēšanas kontrolsaraksti

[!include [banner](../../includes/banner.md)]

 

Katram līdzeklim ir piesaistīts līdzekļa tips. Līdzekļa tipi definē uzturēšanas darba tipus (tādējādi arī uzturēšanas darbus), kurus var veikt līdzekļos. Izveidojot darba pasūtījumu, jums ir jāatlasa uzturēšanas darba tips. Jūs varat atlasīt vienīgi tos uzturēšanas darba tipus, kuri ir saistīti ar līdzeklim izmantotā līdzekļa tipa iestatījumu.

Lai iegūtu grafisku pārskatu par līdzekļiem un uzturēšanas darbu tipiem un to savienojumu ar darba pasūtījumiem, skatiet [Funkcionālās atrašanās vietas un līdzekļi](../overview/functional-locations-and-objects.md).

Uzturēšanas darba tipa variantus var iestatīt uzturēšanas darba tipā. Ar uzturēšanas darba tipa variantiem definē darba tipa variācijas, piemēram, izmērus (mazs, vidējs vai liels), laikposmus (katru nedēļu, reizi divās nedēļās, viens mēnesis vai divi mēneši) un konfigurācijas (zema standarta, elastīgs vai augstas veiktspējas).

Uzturēšanas darbu amatiem nodrošina informāciju par profesionālu tirdzniecību, piemēram, mehāniskajiem, elektroniskajiem un hidrauliskajiem amatiem. Uzturēšanas darba amatam var iestatīt kompetences prasības. Visu uzturēšanas darbu tirdzniecību var izmantot saistībā ar visiem uzturēšanas darbu tipiem. Uzturēšanas darba tipa variantu un/vai uzturēšanas darba tirdzniecību darba pasūtījumā var atlasīt pēc izvēles.

Katram uzturēšanas darba tipam var izveidot uzturēšanas darba tipa uzstādīšanas variantus. Piemēram, ja jums ir uzturēšanas darba tips ar nosaukumu **Serviss**, jūs varat izveidot šādas variācijas šim uzturēšanas darba tipam: **Smagās automašīnas 30 000 km**, **automašīnas 30 000 km** un **furgoni 30 000 km**.

Uzturēšanas darbu tipa kategorijas tiek izmantotas, lai ievāktu uzturēšanas darbu tipu grupu pārskata nolūkiem. Uzturēšanas darbu tipu kategorijas var ietvert **Kalibrēšana**, **Pārbaude**, **Apskate** un **Instrumentācija**.

Uzturēšanas kontrolsarakstu veidnes un uzturēšanas kontrolsarakstu mainīgie lielumi tiek izmantoti, lai iestatītu uzturēšanas kontrolsarakstus. Uzturēšanas kontrolsaraksti tiek iestatīti uzturēšanas darbu tipiem un izmantoti darba pasūtījumos.

Vispirms jūs iestatāt nepieciešamo uzturēšanas darbu tipu kategorijas, uzturēšanas darbu tipu variantus un uzturēšanas darbu amatus. Tad jūs varat izveidot uzturēšanas darbu tipus. Visbeidzot lapā **Uzturēšanas darba tipa noklusējumi** jūs izveidojat visas uzturēšanas darbu tipu variācijas, kuras ir nepieciešamas jūsu aprīkojumam. Šajā lapā jūs varat arī iestatīt prognozes, uzturēšanas kontrolsarakstus un rīkus vairākiem uzturēšanas darbu tipiem.

> [!NOTE]
> Uzturēšanas darba tipu var saistīt tikai ar vienu uzturēšanas darba tipa kategoriju.

## <a name="create-a-maintenance-job-type-category"></a>Izveidot uzturēšanas darba tipa kategoriju

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu tipu kategorijas**.
2. Atlasiet **Jauns**.
3. Laukā **Uzturēšanas darba tipa kategorija** ievadiet uzturēšanas darba tipa kategorijas ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Pēc uzturēšanas darbu tipu kategoriju piesaistīšanas uzturēšanas darbu tipiem lauks **Darbu tipi** uzrāda to uzturēšanas darbu skaitu, kuri ir saistīti ar šo uzturēšanas darbu kategoriju.

![Uzturēšanas darba tipa kategoriju lapa](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Izveidot uzturēšanas darba tipa variantu

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu tipu varianti**.
2. Atlasiet **Jauns**.
3. Laukā **Uzturēšanas darba tipa variants** ievadiet uzturēšanas darba tipa varianta ID.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Kopsavilkuma cilnē **Uzturēšanas darbu tipi** atlasiet **Pievienot**, lai pievienotu uzturēšanas darba tipu.
6. Laukā **Uzturēšanas darba tips** atlasiet uzturēšanas darba tipu.
7. Atkārtojiet 5. līdz 6. darbību, lai uzturēšanas darba tipa variantam pievienotu vairāk uzturēšanas darbu tipu.

    Kopsavilkuma cilnē **Detalizēta informācija** lauks **Darbu tipi** uzrāda to uzturēšanas darbu tipu skaitu, kuri ir pievienoti šim uzturēšanas darbu tipa variantam.

![Uzturēšanas darba veida variantu lapa](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Izveidot uzturēšanas darba amatu

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu amats**.
2. Atlasiet **Jauns**.
3. Laukā **Amats** ievadiet uzturēšanas darba amata ID.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Kopsavilkuma cilnē **Prasmes** atlasiet **Pievienot**, lai pievienotu jaunu prasmi, kuru vajadzētu attiecināt uz uzturēšanas darba amatu.
6. Laukā **Prasme** atlasiet prasmi.
7. Laukā **Līmenis** atlasiet prasmes līmeni.
8. Atkārtojiet 5. līdz 7. darbību, lai uzturēšanas darba amatam pievienotu vairāk prasmju.

    Kopsavilkuma cilnē **Detalizēta informācija** lauks **Prasmes** uzrāda to prasmju skaitu, kuras ir pievienotas šim uzturēšanas darba amatam.

9. Kopsavilkuma cilnē **Sertifikāti** atlasiet **Pievienot**, lai uzturēšanas darba amatam pievienotu sertifikātu.
10. Laukā **Sertifikāta tips** atlasiet sertifikātu.
11. Atkārtojiet 9. līdz 10. darbību, lai uzturēšanas darba amatam pievienotu vairāk sertifikātu.

    Kopsavilkuma cilnē **Detalizēta informācija** lauks **Sertifikāti** uzrāda to sertifikātu skaitu, kuri ir pievienotas šim uzturēšanas darba amatam.

![Uzturēšanas darba amatu lapa](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Izveidot uzturēšanas kontrolsaraksta mainīgo lielumu

Kad uzturēšanas darba tipa noklusējumā izveidojat uzturēšanas kontrolsaraksta rindas, jums ir jāatlasa uzturēšanas kontrolsaraksta tips. **Mainīgais** ir viens uzturēšanas kontrolsaraksta tips. To izmanto, lai definētu iespējamo rezultātu uzturēšanas kontrolsaraksta rindas diapazonā, kas ir saistīts ar darba pasūtījuma rindu. Mainīgais ļauj izveidot iepriekš definētu iznākumu kopu bez vajadzības veikt precīzu mērījumu.

**1. piemērs:** Jūs varat mērīt eļļas līmeni, definējot trīs vērtības: **Līmenis pārāk augsts**, **Līmenis pārāk zems** un **Līmenis diapazona ietvaros**. Katrai vērtībai ir jādefinē, vai vērtības rezultāts ir **Atbilst**, **Neatbilsts** vai **Neviens**.

**2. paraugs:** Jūs veicat vizuālu aprīkojuma elementa pārbaudi, lai izvērtētu nolietojumu.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Uzturēšanas kontrolsaraksti** \> **Uzturēšanas kontrolsarakstu mainīgie**.
2. Atlasiet **Jauns**.
3. Laukā **Mainīgais** ievadiet uzturēšanas kontrolsaraksta mainīgā ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.
5. Kopsavilkuma cilnē **Vispārīgi** atlasiet **Pievienot**, lai mainīgajam pievienotu rindu.

    Laukā **Rindas numurs** automātiski tiek ievadīts rindas sērijas numurs. Pēc visu rindu pievienošanas jūs varat pēc nepieciešamas mainīt rindu numurus. Atlasot rindu un nospiežot **Lejupvērstās bultiņas** taustiņu, nākamais sērijas numurs tiek automātiski ievadīts nākamajā rindā.

6. Laukā **Vērtība** ievadiet vērtības aprakstu.
7. Laukā **Rezultātu** atlasiet rindas rezultātu.

![Uzturēšanas kontrolsaraksta mainīgo lapa](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Izveidot uzturēšanas kontrolsaraksta veidni

Uzturēšanas kontrolsaraksta veidnes var izmantot kā vispārīgu uzdevumu kopu, kuru speciālistam ir jāveic, lai pareizi izpildītu darba pasūtījumu. Atsauces uz veidnēm tiek veidotas no uzturēšanas kontrolsaraksta rindām uzturēšanas darba tipa noklusējumā. Atsauces uz veidnēm var veidot vairākās uzturēšanas darba tipa noklusējumu rindās. Tāpēc jūs varat vienkārši atkārtoti izmantot vispārīgu uzturēšanas kontrolsarakstu uzdevumu kopu. Uzturēšanas kontrolsarakstu veidņu piemēri ietver vispārīgas drošības instrukcijas un vairākus elementus un nosacījumus, kuri ir jāpārbauda noteiktam sūknim vai līdzīgiem konveijera lentes modeļiem.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Uzturēšanas kontrolsaraksti** \> **Uzturēšanas kontrolsarakstu veidnes**.
2. Atlasiet **Jauns**.

    Laukā **Uzturēšanas kontrolsaraksta veidne** automātiski tiek ievadīts veidnes ID.

3. Laukā **Nosaukums** ievadiet uzturēšanas kontrolsaraksta veidni.
4. Kopsavilkuma cilnē **Uzturēšanas kontrolsarakstu rindas** atlasiet **Pievienot**, lai pievienotu veidnes rindu.

    Laukā **Rindas numurs** automātiski tiek ievadīts rindas sērijas numurs. Pēc visu rindu pievienošanas jūs varat pēc nepieciešamas mainīt rindu numurus. Atlasot rindu un nospiežot **Lejupvērstās bultiņas** taustiņu, nākamais sērijas numurs tiek automātiski ievadīts nākamajā rindā.

5. Laukā **Tips** atlasiet uzturēšanas kontrolsaraksta rindas tipu. Katram uzturēšanas kontrolsaraksta tipam kopsavilkuma cilne **Detalizēta rindas informācija** uzrāda saistītus laukus. Ir pieejamas šādas vērtības:

    - **Teksts** – rindai ir teksts, kurā aprakstīts, kas ir jādara. Izmantojiet šo uzturēšanas kontrolsaraksta tipu, ja vēlaties, lai speciālists kaut ko pārbauda vai izmeklē, taču ja jūs nesagaidāt konkrētu (izmērāmu) rezultātu. Pēc tipa atlasīšanas ievadiet nosaukumu vai virsrakstu laukā **Nosaukums**. Laukā **Norādījumi** ievadiet darāmo darbu aprakstu. Ja darbība uzturēšanas sarakstā ir obligāta, iestatiet opciju **Obligāts** uz **Jā**.
    - **Galvene** – rinda tiek izmantota kā galvene, lai grupētu tās uzturēšanas kontrolsaraksta rindas, kuras parādās zem tā. Šis tips ir noderīgs, ja jums ir vairākas uzturēšanas kontrolsaraksta rindas, kuras var iedalīt konkrētās jomās. Galvenes sniedz pārskatu par speciālistu, kurš izpildīs uzturēšanas kontrolsarakstu ar daudzām uzturēšanas kontrolsaraksta rindām. Pēc tipa atlasīšanas ievadiet aprakstošu nosaukumu laukā **Nosaukums**.
    - **Veidne** – rinda tiek izmantota, lai sniegtu atsauci uz esošu veidni. Pēc šī tipa atlasīšanas ievadiet veidnes nosaukumu laukā **Nosaukums**. Laukā **Veidne** atlasiet veidni.
    - **Mainīgais** – rinda tiek izmantota, lai definētu iespējamo rezultātu diapazonā. Informāciju par to, kā uzstādīt uzturēšanas kontrolsaraksta mainīgos, skatiet sadaļu [Izveidot uzturēšanas kontrolsaraksta mainīgo](#create-a-maintenance-checklist-variable) Pēc šī tipa atlasīšanas ievadiet aprakstošu mainīgā nosaukumu laukā **Nosaukums**. Laukā **Mainīgais** atlasiet mainīgo. Laukā **Norādījumi** ievadiet darāmo darbu aprakstu. Ja darbība uzturēšanas sarakstā ir obligāta, iestatiet opciju **Obligāts** uz **Jā**.
    - **Mērījums** – rindu izmanto, lai fiksētu konkrētu mērījumu. Jūs varat uzstādīt mērījumu, kuru vajadzētu saistīt ar iepriekš definētu skaitītāju. Pēc šī tipa atlasīšanas ievadiet veidnes nosaukumu laukā **Nosaukums**. Ja šī darbība uzturēšanas sarakstā ir obligāta, iestatiet opciju **Obligāts** uz **Jā**. Ja vēlaties izmantot mērījuma rindu kā skaitītāja reģistrāciju, atlasiet skaitītāju laukā **Skaitītājs**. Pēc tam saistītais lauks **Vienums** tiek automātiski atjaunināts. Ja esat atlasījuši skaitītāju, laukā **Vērtība** atlasiet atjaunināšanas metodi. Laukos **Min. vērtība** un **Maks. vērtība** ievadiet atļauto vērtības diapazonu. Laukā **Norādījumi** ievadiet darāmo darbu aprakstu.

        > [!NOTE]
        > Jebkura **Mērījuma** tipa rinda, kurai nav skaitītāja uzstādījuma, tiek apstrādāta kā neatkarīga mērījuma reģistrācija, kurai nav nekādas automātiskas sekošanas Asset Management. Tāpat, ja atlasītais skaitītāja tips nav līdzeklī, kas ir saistīts ar darba pasūtījumu, uzturēšanas kontrolsaraksta uzdevums tiek apstrādāts kā neatkarīgs mērījums. Skaitītāja vērtību var mainīt vairākas reizes. Tā nav ievietota, iekams [darba pasūtījuma dzīves cikla stāvoklis](work-order-lifecycle-states.md) nav nomainīts uz stāvokli, kurā opcija **Apstrādāt uzturēšanas kontrolsarakstu** ir iespējota uz **Jā**.

    Kopsavilkuma cilnē **Detalizēta informācija** lauks **Pārbaudes** uzrāda kopējo kontrolsaraksta rindu skaitu jūsu veidnē. Šis numurs ietver ligzdotās rindas jebkurā esošajā veidnē, uz kuru atsaucāties savā veidnē.

![Uzturēšanas kontrolsaraksta veidņu lapa](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Izveidot uzturēšanas darba tipu

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu tipi**.
2. Atlasiet **Jauns**.
3. Laukā **Uzturēšanas darba tips** ievadiet uzturēšanas darba tipu.
4. Laukā **Nosaukums** ievadiet nosaukumu.

    Kopsavilkuma cilnē **Detalizēta informācija** ir uzrādīts pārskat par vairākiem uzturēšanas darbu topu variantiem, sertifikātiem, sekmīgiem darbiem un līdzekļu tipiem, kuri ir izveidoti šim uzturēšanas darba tipam. Laukā **Uzstādījuma rindas** ir parādīts to uzturēšanas darba tipa noklusējuma rindu skaits, kuras ir uzstādītas šim uzturēšanas darba tipam. Laukā **Līdzekļi** ir parādīts to aktīvo līdzekļu skaits, kuri šobrīd izmanto šo uzturēšanas darba tipu.

5. Kopsavilkuma cilnē **Vispārīgi**, laukā **Uzturēšanas darba tipa kategorija** atlasiet uzturēšanas darba tipa kategoriju.
6. Iestatiet opciju **Dīkstāves uzturēšanas dēļ darbības** uz **Jā**, ja uzturēšanas darba tipam ir nepieciešama aprīkojuma uzturēšanas apturēšana pirms darbu var veikt.
7. Kopsavilkuma cilnē **Apraksts**: ievadiet uzturēšanas darba tipa aprakstu.
8. Kopsavilkuma cilnē **Uzturēšanas darba tipa varianti** jūs varat uzturēšanas darba tipam pievienot variantu.
9. Kopsavilkuma cilnēs **Vajadzīgās prasmes** un **Vajadzīgie sertifikāti** jūs varat uzturēšanas darba tipam pievienot prasmes un sertifikāta prasības.
10. Ja nākamais ir jāveic konkrēts uzturēšanas darba tips, pievienojiet to kopsavilkuma cilnē **Nākamie darbi**. Jūs varat arī uzstādīt uzturēšanas darba tipa variantu un amatu, kuri ir saistīti ar uzturēšanas darba tipu. Ja nākamajam darbam ir jāsākas noteiktu dienu skaitu pirms vai pēc darba, kas izmanto šo uzsākto uzturēšanas darba tipu, ievadiet dienu skaitu laukā **Aizturēt uz dienām**. Pozitīvie skaitļi reprezentē dienas pēc attiecīgā darba sākuma, bet negatīvie skaitļi reprezentē dienas pirms ieplānotā attiecīgā darba sākuma. Piemēram, ja ievadāt **5**, nākamais darbs sāksies piecas dienas pēc ar uzturēšanas darba tipu saistītā darba sākuma. Ja ievadāt **-3**, nākamais darbs sāksies trīs dienas pirms ar uzturēšanas darba tipu saistītā darba sākuma.

    > [!NOTE]
    > Ja jūs pievienojat vairāk nekā vienu uzturēšanas darba tipa rindu, rindu kārtība norādīs secību, kādā tās ir jāizpilda. Kārtības sākums ir saraksta augšpusē.

11. Kopsavilkuma cilnē **Līdzekļu tipi** jūs varat uzturēšanas darba tipam pievienot līdzekļu tipus.

![Uzturēšanas darba veidu lapa](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Izveidot uzturēšanas darba tipa noklusējuma rindas un saistītās prognozes, uzturēšanas kontrolsarakstus, rīkus, aprakstu un pielikumus

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu noklusējumi**.

    –vai–

    Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Darbi** \> **Uzturēšanas darbu tipi**, atlasiet uzturēšanas darba tipu un tad atlasiet **Uzturēšanas darba tipa noklusējumi**.

2. Atlasiet **Jauns**.
3. Laukos **Funkcionālais novietojums**, **Līdzekļa tips**, **Ražotājs**, **Modelis** un **Līdzeklis** atlasiet atbilstošās vērtības atkarībā no tā, cik konkrētam ir jābūt uzturēšanas darba tipa noklusējumam.
4. Laukā **Uzturēšanas darba tips** atlasiet uzturēšanas darba tipu, ja tas netika atlasīts automātiski.
5. Laukos **Uzturēšanas darba tipa variants** un **Amats** pēc vajadzības atlasiet uzturēšanas darba tipa variantu un uzturēšanas darba amatu.
6. Atlasiet **Prognoze**.
7. Lapā **Uzturēšanas darba tipa noklusējuma prognoze** jūs varat veikt prognozes par stundām, vienumiem un izmaksām. Atbilstošajās cilnēs atlasiet **Pievienot** un veiciet atlasi, lai izveidot vajadzīgās prognozes uzturēšanas darba tipam.
8. Cilnē **Vienuma prognoze** jūs varat atlasīt inventāra izmērus, kurus vajadzētu uzrādīt vienuma rindā. Atlasiet **Inventārs** \> **Izmēri**, atlasiet izmērus, kurus uzrādīt, iestatiet opciju **Saglabāt uzstādījumu** uz **Jā**, tad atlasiet **Labi**.
9. Cilnē **Vienuma prognoze** atlasiet **Vienums, kurā izmantots**, lai redzētu pārskatu par to, kur Asset Management atlasītajā līnijā vienums ir izmantots attiecībā uz līdzekļiem, uzturēšanas darba tipa noklusējumu, rezerves daļām un darba pasūtījumiem. 

    Kopsavilkuma cilne **Uzturēšanas prognozes kopsumma** uzrādīts pārskats par prognozes kopsummu. Šajā pārskatā ir iekļauts kopējais stundu un izveidoto prognozes rindu skaits.

    > [!NOTE]
    > Lai pārkopētu prognozes uzstādījumu no cita uzturēšanas darba tipa, atlasiet **Kopēt prognozi** un tad atlasiet uzturēšanas darba tipu, no kura kopēt uzstādījumu.

11. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.
12. Aizveriet lapu **Uzturēšanas darba tipa noklusējuma prognoze**, lai atgrieztos lapā **Uzturēšanas darba tipa noklusējumi**.
13. Atlasiet **Uzturēšanas kontrolsaraksts**.
14. Lapā **Uzturēšanas darba tipa noklusējumu kontrolsaraksts** jūs varat izvēlētajam uzturēšanas darba tipa noklusējumam pievienot uzturēšanas kontrolsaraksta rindas. Kopsavilkuma cilnē **Uzturēšanas kontrolsarakstu rindas** atlasiet **Jauna**, lai pievienotu uzturēšanas kontrolsaraksta rindu.

    Rindu numuri tiek automātiski ievadīti laukā **Rindas numurs**, lai norādītu uzturēšanas kontrolsaraksta rindu kārtību. Jūs varat rediģēt rindu numurus pēc vajadzības. Pēc pirmās uzturēšanas kontrolsaraksta rindas izveidošanas atlasiet rindu, tad nospiediet **Lejupvērstās bultiņas** taustiņu, lai zem tās pievienotu rindu. Jūs varat arī atlasīt uzturēšanas kontrolsaraksta rindu un tad atlasīt **Jauna**. Šādā gadījumā jauna rinda tiek pievienota virs atlasītās uzturēšanas kontrolsaraksta rindas.

15. Laukā **Tips** atlasiet rindas tipu un tad pievienojiet informāciju, kas ir saistīta ar uzturēšanas kontrolsaraksta tipu. Lai saņemtu pieejamo tipu un saistīto lauku aprakstu, skatiet sadaļu [Izveidot uzturēšanas kontrolsaraksta veidni](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Lai pārkopētu uzturēšanas kontrolsaraksta uzstādījumu no cita uzturēšanas darba tipa, atlasiet **Kopēt uzturēšanas sarakstu** un tad atlasiet uzturēšanas darba tipu, no kura kopēt uzstādījumu.
    >
    > Jūs varat vienkārši izveidot veidni no esoša uzturēšanas kontrolsaraksta. Pēc tam jūs varat veidni atkārtoti izmantot vairākos uzturēšanas kontrolsarakstos. Jaunā veidne būs aktīvā uzturēšanas kontrolsaraksta precīza kopija. Atlasiet **Izveidot veidni** un tad ievadiet veidnes nosaukumu. Lai aizvietotu esošu uzturēšanas kontrolsarakstu ar vienu rindu, kas atsaucas uz jauno veidni, iestatiet opciju **Aizvietot** ar **Jā**. Jūs varat aplūkot veidnes saturu detalizētās informācijas lapā **Uzturēšanas kontrolsaraksta veidnes**.

16. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.
17. Atgriezieties lapā **Uzturēšanas darba tipa noklusējumi**.
18. Atlasiet **Rīki**.
19. Lapā **Uzturēšanas darba tipa noklusējumu rīki** jūs varat pievienot rīkus (resursus), kurus vajadzētu izmantot uzturēšanas darba tipam. Atlasiet **Jauns** un tad atlasiet rīku laukā **Resurss**.

    > [!NOTE]
    > Lai pārkopētu rīka uzstādījumu no cita uzturēšanas darba tipa, atlasiet **Kopēt rīkus** un tad atlasiet uzturēšanas darba tipu, no kura kopēt uzstādījumu.

20. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.
21. Atgriezieties lapā **Uzturēšanas darba tipa noklusējumi**.
22. Atlasiet **Darba apraksts**.
23. Lapā **Darba apraksts** atlasiet **Rediģēt**, tad pēc vajadzības pievienojiet aprakstu, kas ir saistīts ar atlasīto uzturēšanas darba tipa noklusējumu.
24. Atlasiet **saglabāt**, lai saglabātu aprakstu.

    Ja jūs šeit pievienojat darba aprakstu, tas pārlabo jebkuru aprakstu, kas ir uzstādīts uzturēšanas darba tipam lapā **Uzturēšanas darba tipi**. Ja jūs šeit nepievienojat darba aprakstu, tiek izmantots jebkurš apraksts, kas ir uzstādīts uzturēšanas darba tipam. Apraksti tiek automātiski pārvirzīti uz darba pasūtījumiem, kuros tiek izmantots uzturēšanas darba tips vai uzturēšanas darba tipa noklusējums.

25. Atgriezieties lapā **Uzturēšanas darba tipa noklusējumi**.
26. Lai uzstādītu pielikumus atlasītajai uzturēšanas darba tipa noklusējuma rindai, atlasiet **Pievienot dokumentus**. Pielikumi, kuri ir uzstādīti uzturēšanas darba tipa noklusējuma rindai, tiek automātiski iekļauti darba pasūtījuma rindās, kuras izmanto šā uzturēšanas darba tipa noklusējuma rindu.
27. Atlasiet **Jauns** un tad atlasiet dokumenta tipu.
28. Augšupielādējiet dokumentu vai failu.
29. Uzstādiet laukus lapā **Pielikumi**. Pielikuma uzstādījums izmanto standarta dokumenta uzstādījuma funkcionalitāti.
30. Atlasiet **saglabāt**, lai saglabātu pielikumu.

    > [!NOTE]
    > Pielikumi uzturēšanas darba tipa noklusējuma rindā tiek drukāti kopā ar darba pasūtījuma ziņojumu vienīgi tad, ja pielikumu dokumentu tipi ir atlasīti lapas **Līdzekļu pārvaldības parametri** cilnē **Dokumentu tipi** (**Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Līdzekļu pārvaldības parametri**). Pielikumu piemēri ietver vadlīnijas, kurās paskaidrots, kā pabeigt konkrētu darbu vai iepriekš definētu uzturēšanas kontrolsarakstu (ja neizmantojat uzturēšanas kontrolsaraksta funkcionalitāti uzturēšanas darba tipa noklusējuma rindām).

    Lapā **Uzturēšanas darba tipa noklusējumi** katra rinda uzrāda prognozēto stundu skaitu, kā arī to rindu skaitu, kuras ir izveidotas vienumiem, izmaksām, uzturēšanas kontrolsarakstiem un rīkiem. Laukā **Līdzekļi** ir parādīts to aktīvo līdzekļu skaits, kuri ir saistīti ar uzturēšanas darba tipa noklusējuma rindu.

31. Lai kopētu uzturēšanas darba tipa noklusējumu citā uzturēšanas darba tipa noklusējumā, atlasiet uzturēšanas darba tipa noklusējuma rindu, kuru kopēsit citā uzstādījumā, atlasiet **Kopēt uzstādījumu** un tad atlasiet uzturēšanas darba tipa noklusējumu, kuru kopēt.
32. Lai skatītu to līdzekļu, uzturēšanas plānu vai uzturēšanas ciklu sarakstu, kurus šobrīd izmanto uzturēšanas darba tipa noklusējuma rinda, atlasiet rindu un tad atlasiet **Izmanto**.

![Uzturēšanas darba veida noklusējumu lapa](media/07-setup-for-work-orders.png)

Kad sistēma atlasa pieejamo uzturēšanas darba tipa noklusējumu, kuru būtu jāizmanto darba pasūtījuma rindā, atlase ir balstīta uz līdzekli un saistīto līdzekļa tipa uzstādījumu. Asset Management izskata visus uzturēšanas darba tipa noklusējuma ierakstus, kuri ir saistīti ar to uzturēšanas darba tipu, kurš ir saistīts ar līdzekļa tipu, lai pārbaudītu, vai nav iespējama saderība. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, lai atrastu konkrētāko kombināciju, Asset Management vispirms pārbauda iespējamo saderību laukā **Amats**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Uzturēšanas darba veida variants**. Ja nav atrasta neviena saderība, tas meklē saderību laukā **Uzturēšanas darba tips** un tā tālāk (**Tirdzniecība**, tad **Uzturēšanas darba tipa variants**, tad **Uzturēšanas darba tips**, tad **Līdzeklis**, tad **Modelis**, tad **Ražotājs** un tad **Līdzekļa tips**). Ja nav atrasta saderība, tiek izmantots noklusējuma ieraksts, kurā ir atlasīts vienīgi uzturēšanas darba tips.

Projekta aktivitātes ID tiek automātiski piesaistīts katrai jūsu izveidotajai uzturēšanas darba noklusējuma rindai. Projekta darbība tiek izveidota prognozes projektā, kas ir atlasīts laukā **Uzturēšanas prognozes projekts** lapas **Līdzekļu pārvaldības parametri** cilnē **Līdzekļi**. Projekta darbības nolūks ir pārvaldīt stundu, vienumu un izdevumu prognozes attiecībā uz darba pasūtījumiem. Uzturēšanas darba tipa prognozes tiek automātiski pārvirzītas uz darba pasūtījuma rindu, un tās tiek nokopētas no prognozes projekta darba pasūtījuma projektā, kurš ir izveidots darba pasūtījuma rindai. Projekta darbības nolūks ir pārvaldīt prognozes attiecībā uz darba pasūtījumiem.

Jūs varat uzstādīt pakešuzdevumu, lai atjauninātu uzturēšanas darba tipa noklusējuma atsauces regulāros intervālos, vai jūs varat darbu palaist manuāli. Lai izveidotu pakešuzdevumu vai manuāli palaistu atjauninājumu, atlasiet **Līdzekļu pārvaldība** \> **Periodiski** \> **Preventīvā uzturēšana** \> **Atjaunināt uzturēšanas darba tipa noklusējuma atsauces**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Pārskats par tiem uzturēšanas darbu tipiem, kuri ir saistīti ar līdzekļiem

Pēc tam, kad izveidojat nepieciešamās uzturēšanas darba tipa noklusējuma kombinācijas, jūs varat izmantot lapu **Visi līdzekļi**, lai iegūtu pārskatu par šībrīža uzturēšanas darba tipa noklusējumu, kas ir saistīts ar konkrētu līdzekli. Pārskats uzrāda visas uzturēšanas darba tipa noklusējuma kombinācijas, kuras var izmantot līdzekļa veidā, kurš ir atlasīts līdzeklim. Šīs kombinācijas ietver kombinācijas, kurām ir uzturēšanas darba tipu variantu un uzturēšanas darba amatu variācijas.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.
2. Sarakstā atlasiet līdzekli, kuram skatīti uzturēšana darba tipa kombināciju pārskatu.
3. Darbību rūtī, cilnē **Vispārīgi**, grupā **Saistīta informācija** atlasiet **Uzturēšanas darbu tipi**.

    Lapas **Līdzekļu uzturēšanas darbu tipi** kreisā rūts uzrāda sarakstu ar visām uzturēšanas darba tipa kombinācijām, kuras ir saistītas ar atlasīto līdzekli.

4. Atlasiet uzturēšanas darba tipa kombināciju, lai redzētu saistīto uzstādījumu uzturēšanas kontrolsarakstiem, prognozēm un rīkiem. Ātrās cilnes **Uzturēšanas darbu tipu noklusējumi** sadaļā **Detalizēta informācija** tiek uzrādīts to saistīto uzturēšanas kontrolsarakstu, prognozēto stundu vienumu u.c. skaits, kuri ir saistīti ar atlasīto uzturēšanas darba tipa kombināciju.
5. Lai skatītu detalizētu informāciju atlasītajam uzturēšanas darba tipam, atlasiet **Uzturēšana darbu tipi**.

![Līdzekļu uzturēšanas darba veidu lapa](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Automātiska uzturēšanas darbu tipu prognožu atjaunināšana

Lietojot Līdzekļu pārvaldību, varat automātiski atjaunināt jebkādas izmaiņas uzturēšanas darba tipa prognozēs stundu izmaksām, vienumu izmaksām un izmaksām, kas ir atjaunināts citos moduļos. Tādējādi jūs nodrošināt, ka jūsu uzturēšanas darba tipa prognozes vienmēr izmanto jaunākās izmaksas.

1. Atlasiet **Līdzekļu pārvaldība** \> **Periodiski** \> **Prognoze** \> **Atjaunināt uzturēšanas darbu tipa prognozi**.
2. Dialoglodziņā **Atjaunināt uzturēšanas darba tipa prognozi**, ātrajā cilnē **Iekļaujamie ieraksti** jūs varat pēc vajadzības pievienot konkrētu uzturēšanas darbu tipu izvēli. Atlasiet **Filtrs** un pēc tam **Atlasīt**, lai veiktu atlasi.
3. Ātrajā cilnē **Palaist fonā** jūs varat pēc vajadzības uzstādīt automātisko atjauninājumu kā pakešuzdevumu.
4. Atlasiet **Labi**, lai sāktu prognozes atjaunināšanu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]