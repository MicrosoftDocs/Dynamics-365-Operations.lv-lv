---
title: Konfigurēt numuru sērijas noliktavas plūsmām
description: Šajā tēmā ir sniegts pārskats par funkcionalitāti, kas nodrošina numuru sērijas paplašinājumus noliktavas vienību ID, kopuma etiķešu ID, konteineru ID un preču transporta pavadzīmju ID.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: fa4074c23baa74983f4922d2d09d7da81c943bfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973839"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Konfigurēt numuru sērijas noliktavas plūsmām

[!include [banner](../includes/banner.md)]

Līdzeklis *Numuru sērijas paplašinājumi* pievieno jaunu konfigurācijas lapu numuru sēriju iestatīšanai. Tā iespējo GS1 regulēto ID elastīgu konfigurāciju, ieskaitot GS1 prefiksus un kontrolciparus (modulis 10), un ievieš garuma ierobežojumu esošajām numuru sērijām.

Standarta numuru sērijas segmenti nav piemēroti GS1 ieviešanai, jo nav aprēķināts kontrolcipars, un uzņēmuma GS1 prefikss ir jāatjaunina manuāli.

Līdzeklis pievieno šādu funkcionalitāti:

- Preču transporta pavadzīmes (BOL) ID var ģenerēt iepriekš.
- Seriālā pārvadāšanas konteinera koda (SSCC) numuriem var ģenerēt unikālu numuru sēriju.
- GS1 atbilstošas numuru sērijas var izveidot BOL un SSCC numuriem. Līdzeklis pievieno standarta atbalstu noliktavas vienību ID, konteineru ID, kopuma etiķešu ID un BOL ID.
- Noliktavas vienību ID numuru konfigurācija ir elastīga. Piemēram, varat iekļaut vai izslēgt programmas identifikatorus (AI), kā sākt ar nullēm (00).

Šī funkcionalitāte ļauj efektīvāk atbalstīt kastu marķēšanu un pielāgot jaunus sistēmas ģenerētus numurus.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Ieslēgt līdzekli Numuru sērijas paplašinājumi

Lai varētu izmantot līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Numuru sērijas paplašinājumi*

## <a name="set-up-the-feature"></a>Līdzekļa iestatīšana

Lai sistēmā iestatītu numuru sērijas paplašinājumus, veiciet tālāk norādītās darbības.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Cilnes **Vispārīgi** laukā **GS1 uzņēmuma prefikss** ievadiet uzņēmuma GS1 prefiksu. Šī vērtība ietekmēs visas numuru sērijas, kur GS1 prefikss ir iekļauts kā segments.
1. Ja vēlaties ģenerēt BOL numurus kopuma etiķetēm, cilnē **Pārskati** atlasiet izvēles rūtiņu **Ģenerēt BOL numuru, drukājot kopuma etiķetes**.

    > [!NOTE]
    > Šī izvēles rūtiņa ir pieejama tikai tad, ja [kopuma etiķešu drukāšanas](configure-wave-label-printing.md) funkcionalitāte ir ieslēgta.

1. Doties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Numuru sērijas paplašinājumi**
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**. Tiek izveidota GS1 atbilstoša BOL numura sērija un trīs veidu SSCC numuru sērijas. Visas šīs numuru sērijas ņem vērā jūsu uzņēmuma GS1 prefiksa garumu.

    Papildinformāciju par to, kā pielāgot šīs noklusējuma numuru sērijas un/vai pievienot jaunas sērijas, skatiet nākamajā sadaļā. Jebkuru no šīm sērijām varat arī noņemt, ja tās nav nepieciešamas.

1. Atgriezties sadaļā **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Cilnē **Numuru sērijas** atlasiet atbilstošo numura sērijas paplašinājumu, ko izmantot, lai ģenerētu numurus noliktavas vienību ID, kopuma etiķešu ID, konteineru ID (šajā gadījumā atlasiet atbilstošo **SSCC-18 numura** sēriju) un/vai BOL ID (šajā gadījumā atlasiet **BOL** sēriju). Pēc noklusējuma numuru sērijas paplašinājumi tiek atbalstīti tikai šiem četriem ID veidiem.

Nākamā reize, kad vienai no šīm numuru sērijām tiks ģenerēts jauns numurs, tiks izmantota jaunā loģika.

> [!NOTE]
> Ja neatlasāt noliktavas vienību ID numura sērijas paplašinājumu, tad tiks izmantoti pašreizējie noteikumi noliktavas vienību ID ģenerēšanai. Pretējā gadījumā tiks izmantota jūsu atlasītā numuru sērija. Pārējiem ID tiks izmantota vienkārša numura sērija, līdz jūs tiem piemērosiet numura sērijas paplašinājumu.

## <a name="create-and-edit-number-sequences"></a>Izveidot un rediģēt numuru sērijas

Iepriekšējā sadaļā tika ģenerēta numuru sēriju noklusējuma kopa. Šajā sadaļā ir paskaidrots, kā definēta katra numura sērija. Tajā ir arī paskaidrots, kā izveidot pielāgotas sērijas un kā rediģēt noklusējuma vai pielāgotās sērijas.

Lai izveidotu un rediģētu numuru sērijas, veiciet tālāk norādītās darbības.

1. Doties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Numuru sērijas paplašinājumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Numura sērijas paplašinājums** ievadiet jaunās sērijas nosaukumu. Ievadiet aprakstu laukā **Apraksts**.
1. Kopsavilkuma cilnē **Segmenti**, izmantojiet rīkjoslas pogas, lai izveidotu numerācijas formātu, pievienojot, dzēšot un kārtojot segmentus. Katrai rindai laukā **Segments** piešķiriet segmenta veidu, lai definētu šī segmenta nolūku un saturu. Šajā tabulā aprakstīti pieejamie segmentu veidi.

    | Segmenta veids | apraksts |
    |---|---|
    | Konstante | Šis segmenta veids pievieno vienādu konstantes tekstu katram ģenerētajam numuram sērijā. Laukā **Vērtība** ievadiet nepieciešamo tekstu. Lauks **Garums** tiek automātiski atjaunināts uz laukā **Vērtība** ievadīto teksta garumu. |
    | Numuru sērija | Laukā **Vērtība** ievadiet numura zīmi (*\#*) katrai rakstzīmei, kas jāparāda ģenerētajā sērijā. Pati numura sērija var ģenerēt garākus numurus, bet tiks rādītas tikai labās puses rakstzīmes. Lauks **Garums** tiek automātiski atjaunināts uz laukā **Vērtība** ievadīto numura zīmes numuru.<p>Lai atbilstu GS1 prasībām attiecībā uz SSCC-18 numuriem, pārliecinieties, ka šī segmenta garums ir 16 mīnus jūsu GS1 prefiksa garums.</p> |
    | GS1 prefikss | Šis segmenta veids pievieno vērtību, kas ir iestatīta laukā **GS1 uzņēmuma prefikss**, lapā **Noliktavas pārvaldības parametri**. Lauks **Vērtība** rāda vērtību, kas ir iestatīta lapā **Noliktavas pārvaldības parametri**, un lauks **Garums** rāda rakstzīmju skaitu vērtībā. Gan lauks **Vērtība**, gan lauks **Garums** ir tikai lasāms. |
    | Pieteikuma identifikators | Laukā **Vērtība** ievadiet pieteikuma identifikatoru, kā norādīts atbilstošajā GS1 politikā šim numura sērijas veidam. Piemēram, ievadiet *00*, priekš SSCC vai *420* priekš BOL. Lauks **Garums** tiek automātiski atjaunināts uz laukā **Vērtība** ievadīto identifikatora garumu. |
    | Iepakojuma tips | Krājumiem, kurus var skaidri identificēt, šis segmenta veids pievieno lauka vērtību no atbilstošās vienības secības grupas (no lapas **Vienību secību grupas** ). (Šī darbība atbilst esošajai noliktavas vienību ID loģikai.) Noliktavas vienībām, kas ietver vairākas noliktavas vienības (SKU), šis segmenta veids pēc noklusējuma pievieno *0* (nulli). Šim segmenta veidam lauks **Vērtība** vienmēr tiek iestatīts uz *P*, un lauks **Garums** vienmēr tiek iestatīts uz *1*.|
    | Kontrolcipars | Šis segmenta veids pievieno kontrolciparu, kas ir moduļa 10 aprēķins. (Šī darbība atbilst esošajai noliktavas vienību ID loģikai.) Šim segmenta veidam lauks **Vērtība** vienmēr tiek iestatīts uz jumtiņa (*^*), un lauks **Garums** vienmēr tiek iestatīts uz *1*. |

1. Lai skatītu galīgo numura formāta paraugu, pārbaudiet lauku **Formāts**, kas atrodas kopsavilkuma cilnes **Segmenti** apakšā.
