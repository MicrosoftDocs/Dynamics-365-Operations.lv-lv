---
title: Atliktā manuālās krājumu kustības apstrāde
description: Šajā tēmā ir aprakstīts, kā izmantot atlikto manuālo krājumu kustības apstrādi Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a15c913c876e961c6824c1e8812ab2be2d6ffa4333cd0d4e6f80cae8bac79394
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746751"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Atliktā manuālās krājumu kustības apstrāde

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot atlikto manuālo krājumu kustības apstrādi Microsoft Dynamics 365 Supply Chain Management.

Atliktā apstrāde ļauj noliktavas darbiniekiem turpināt darīt citu darbu, fonā apstrādājot izvietošanas operāciju. Atliktā apstrāde noder arī tad, ja serverim var būt neregulāri vai neplānoti palielinājumi apstrādes laikā, un palielinātais apstrādes laiks var ietekmēt nodarbinātā produktivitāti. Darba veids *Krājumu kustība* tagad ir pievienots darba veidu kopai, ko šis līdzeklis atbalsta.

Fona apstrāde tiek sasniegta, izmantojot [līdzekli Procesa noliktavas programmas notikumi](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Lai padarītu šo līdzekli pieejamu, ieslēdziet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md): Tās jāslēdz šādā secībā:

1. Organizācijas mēroga darba aizturēšana
1. Apstrādāt noliktavas programmas notikumus
1. Atliktas izvietošanas operācijas
1. Krājumu manuālas pārvietošanas operācijas atliktā apstrāde

## <a name="configure-the-work-processing-policies"></a>Darba apstrādes politiku konfigurēšana

Lai izmantotu atlikto apstrādi, ir jāuzstāda un jāizmanto darba apstrādes politika. Atliktās izvietošanas apstrādei [Noliktavas darba atliktā apstrāde](deferred-put.md) atbalsta šādus darba veidus: *Pārdošanas pasūtījums*, *Pārsūtīšanas pasūtījuma problēma* un *Papildināšana*. Līdzeklisn *Atliktās manuālo krājumu kustības operācijas apstrāde* pievieno jaunu darba veidu: *Krājumu kustība*.

Lai iestatītu darba apstrādes politiku, veiciet šīs darbības.

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba apstrādes politikas**.
1. Sarakstā atlasiet esošu politiku vai izveidojiet jaunu politiku, atlasot **Jauns** darbības rūtī. Katras politikas virsrakstam ir šādi lauki:

    - **Darba apstrādes politikas nosaukums** - darba apstrādes politikas nosaukums.
    - **Apraksts:** - darba apstrādes politikas apraksts.

1. Kopsavilkuma cilnē **Apstrādes nosacījumi** iestatiet noteikumu kolekciju, uz kuriem attiecas politika. Izmantojiet pogas rīkjoslā, lai pievienotu vai noņemtu noteikumus pēc nepieciešamības. Katrai kārtulai iestatiet tālāk norādītos laukus.

    - **Darba pasūtījuma veids** – atlasiet darba veidu, uz kuru attiecas politika.
    - **Operācija** - izvēlieties operāciju, ko politika tiek izmantota apstrādāt. Ja laukā **Darba pasūtījuma veids** esat atlasījis *Krājumu kustība*, šis lauks nav jāiestata, jo gan izdošanas operācijas, gan izvietošanas operācijas tiek apstrādātas kā viens notikums.
    - **Darba apstrādes metode** - izvēlieties metodi, kas tiek izmantota darba rindas apstrādei. Ja atlasīsiet *Tūlītēju*, darbība atgādina darbību, kad nav darba apstrādes politikas, ko izmanto rindas apstrādāšanai. Atlasot *Atlikts*, sistēma piemēros atlikto apstrādi, kas izmanto pakešuzdevumu struktūru.
    - **Atliktās apstrādes slieksnis** – ja šis lauks tiek iestatīts uz *0* (nulle), slieksnis nepastāv. Šajā gadījumā, ja iespējams, izmanto *Atlikts* apstrādes metodi. Ja konkrētās sliekšņvērtības aprēķins ir zemāks par sliekšņvērtību, tiek izmantota *Tūlītējā* metode. Pretējā gadījumā izmanto *Atlikto* metodi, ja ir iespējams. Ar pārdošanu un pārsūtīšanu saistītiem darbiem sliekšņvērtību aprēķina kā saistīto avota noslodzes rindu skaitu, kuras tiek apstrādātas attiecīgajam darbam. Papildināšanas darbiem sliekšņvērtība tiek aprēķināta kā darba rindu skaits, ko darbs papildina. Iestatot sliekšņvērtību, piemēram, *5* pārdošanai nodrošiniet, lai mazāki darbi, kam ir mazāk nekā piecas sākotnējā avota noslodzes rindas, neizmantos atlikto apstrādi, bet lielāki darbi to izmantos. Sliekšņvērtība ir spēkā tikai tad, ja lauks **Darba apstrādes metode** ir iestatīts uz *Atlikts*.
    - **Atliktās apstrādes partijas grupa** - norādiet pakešizpildes grupu, kas tiek izmantota apstrādei. Ja laukā *Darba pasūtījuma veids* esat atlasījis **Krājumu kustību**, šis lauks nav jāiestata, jo ir atlasīta pakešuzdevumu grupa dialoglodziņā **Apstrādāt noliktavas programmas notikumus**.

## <a name="assign-the-work-creation-policy"></a>Darba izveides politikas piešķiršana

Sīkāku informāciju par to, kā piešķirt darba izveides politiku, skatiet [Atliktā noliktavas darba apstrādē](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Iestatiet pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus

Lai izmantotu procesu *Atliktā manuālās krājumu kustības operācijas apstrāde*, iestatiet ieplānotu pakešuzdevumu.

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt noliktavas programmas notikumus**.
1. Dialoglodziņā **Apstrādāt noliktavas programmas notikumus**, kopsavilkuma cilnē **Palaist fonā** iestatiet opciju **Pakešapstrāde** uz *Jā*.
1. Atlasiet **Periodiskums** un iestatiet izpildes grafiku, kas atbilst jūsu uzņēmuma prasībām.
1. Atlasiet **Labi** katrā dialoglodziņā.

## <a name="inquire-about-the-warehouse-app-events"></a>Uzziņas par noliktavas programmas notikumiem

Varat skatīt notikumu rindu un notikuma ziņojumus, ko ģenerē noliktavas programma, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.

Notikuma ziņojuma *Krājumu kustība* statuss būs *Rindā ievietots*, kad tie tiek izveidoti pirmo reizi. Šis statuss norāda, ka pakešuzdevums **Apstrādāt noliktavas programmas notikumus** tupinās notikumu ziņojumus un apstrādās tos. Kad statuss ir atjaunināts uz *Pabeigts*, visi saistītie notikumi tiek dzēsti no rindas.

Visi *Krājumu kustības* notikumi tiek uzkrāti vienā kolekcijā katram notikuma veidam un noliktavai.

Pakešuzdevums apstrādās noliktavas programmas notikumus atbilstoši dialoglodziņā **Apstrādāt noliktavas programmas notikumus** iestatīto atkārtošanos. Tāpēc, līdz ziņojums tiek apstrādāts, noliktavas ID ir iespējams atrast, meklējot laukā **Identifikators**.

Ziņojuma detalizēta informācija satur detalizētu informāciju par kustību (piemēram, atrašanās vietas "no" un "uz").

Papildinformāciju skatiet sadaļā [Noliktavas programmas notikumu apstrāde](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobilās ierīces izvēlnes konfigurēšana, lai izlaistu atliktās apstrādes politiku

Detalizētu informāciju par to, kā konfigurēt mobilās ierīces izvēlni atliktās apstrādes politikas izlaišanai, skatiet [Noliktavas darba atliktā apstrāde](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Ietekme uz slēgtiem darba datumiem

Sīkāku informāciju par ietekmi uz slēgtiem darba datumiem skatiet [Noliktavas darba atliktā apstrādē](deferred-put.md).

## <a name="additional-resources"></a>Papildu resursi

- [Atlikta noliktavas darba apstrāde](deferred-put.md)
- [Noliktavas programmas notikumu apstrāde](warehouse-app-events.md)
- [Mobilo ierīču iestatīšana darbam noliktavā](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
