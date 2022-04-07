---
title: Mobilās ierīces lietotāju konti
description: Šajā tēmā ir aprakstīts, kā iestatīt un pārvaldīt lietotāju kontus, kas darbiniekiem ļauj pieteikties un izmantot noliktavas programmu.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4cb36160e692cc12140b57037d2c9739f7b2ebd
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462675"
---
# <a name="mobile-device-user-accounts"></a>Mobilās ierīces lietotāju konti

[!include [banner](../includes/banner.md)]

Katru reizi, kad darbinieks sāk izmantot noliktavas programmu, tiem jāpiesakās, izmantojot lietotājvārdu un paroli. Visus noliktavas programmas lietotāju skaitu var saistīt ar katru sistēmas darbinieku, un noliktavas parasti tiek saistītas ar katru no šiem noliktavas programmas lietotājiem. Katram darbiniekam tiek konfigurētas arī dažādas opcijas, lai izveidotu noklusējuma iestatījumus un citus iestatījumus, kas saistīti ar noliktavas programmas izmantošana.

## <a name="set-up-the-required-worker-and-employee-records"></a>Iestatīt nepieciešamos darbinieka un darbinieka ierakstus

Pirms varat iestatīt noliktavas programmas lietotājus, katram darbiniekam jābūt kā Supply Chain Management darbiniekam vai strādniekam **Personāla vadības** modulī.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Mobilās ierīces lietotāju kontu iestatīšana

Kad personāla vadības sadaļā ir iestatīti nepieciešamie darbinieki un darbinieki, varat katram no tiem piešķirt noliktavas programmas lietotājus un iestatīt citas opcijas, kas ietekmē programmas lietošanas veidu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Lai rediģētu esošu darbinieku, atlasiet to saraksta rūtī. Lai pievienotu jaunu ierakstu, darbību rūtī atlasiet **Jauns**.
1. Iestatot jaunu darbinieku, rīkojieties šādi:

    1. Laukā **Nodarbinātais** atlasiet mērķa lietotāju darbinieku sarakstā.
    1. Atlasiet **Atlasīt**.
    1. Darbību rūtī atlasiet **Saglabāt**.

1. Noklusējuma profilu var izmantot, lai noliktavas darbinieks iepakošanas stacijā izietu cauri procesam, kas tajā nepieciešams. Alternatīvi noklusējuma profilu var izmantot, lai saglabātu darbiniekam vēlamos profila iestatījumus. Kopsavilkuma cilnē **Profils** iestatiet tālāk minētos laukus:

    - **Konteinera iepakošanas politika** - atlasiet konteinera iepakojuma politiku, kas nosaka, kā jāapstrādā konteineri iepakošanas stacijā. Šeit atlasītā konteinera iepakošanas politika tiks iepriekš atlasīta darbiniekam, kad tas atvērs iepakošanas staciju. Papildinformāciju skatiet šādā grāmatošanas sadaļā: [Uzlabotā iepakošanas funkcionalitāte](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Iepakošanas profila ID** — atlasiet iepakošanas profila ID, kas nosaka izmantotos iepakošanas ierobežojumus un konteinera iestatījumus. Ja atlasītais iepakošanas profila ID ir saistīts ar konteinera iepakošanas politiku, nevarēsit mainīt **Konteinera iepakošanas politikas** iestatījumus šajā lapā.

1. Kopsavilkuma cilnē **Noklusējuma iepakošanas stacija** iestatiet tālāk norādītos laukus, lai definētu noklusējuma iepakošanas staciju, kas ir piemērojama, kad darbinieks pierakstās. Ja nepieciešams, darbinieks var izvēlēties citu iepakošanas staciju.

    - **Vieta** – atlasiet vietu, kur atrodas noklusējuma iepakošanas stacija.
    - **Noliktava** – atlasiet noliktavu, kur atrodas noklusējuma iepakošanas stacija.
    - **Atrašanās vieta** – izvēlieties noklusējuma iepakošanas stacijas atrašanās vietu.

1. Kopsavilkuma cilnē **Lietotāji** varat izveidot jebkuru noliktavas programmas lietotāja kontu skaitu atlasītajam darbiniekam. Katrs konts ir saistīts ar noteiktu noliktavu vai noliktavām. Izmantojiet rīkjoslu, lai pievienotu vai noņemtu lietotāju kontus, atiestatītu atlasītā konta paroli vai piešķirtu noliktavas atlasītajam kontam. Katram lietotāja kontam jūs varat iestatīt tālāk norādītos laukus:

    - **Lietotāja ID** - ievadiet unikālu ID.
    - **Lietotājvārds** - ievadiet ID nosaukumu.
    - **Noklusējuma noliktava** – iestatiet noklusējuma noliktavu, kurā darbinieks parasti strādā. Rīkjoslu var izmantot, lai piešķirtu papildu noliktavas, un darbinieks var pārslēgties no noliktavas uz citu, izmantojot mobilās ierīces izvēlnes vienuma **Mainīt noliktavas** netiešo aktivitāti.
    - **Izvēlnes nosaukums** - atlasiet saknes izvēlni, kas būs darbinieka sākuma lapa. Iespēja iestatīt saknes izvēlni katram darbiniekam ir noderīga, jo tā ļauj kontrolēt izvēlnes struktūru, ko katrs darbinieks var izmantot. Piemēram, izvēlni darbiniekiem, kas ir aktīvi tikai nosūtīšanas apgabalā, var pielāgot uzdevumiem, kas saistīti ar nosūtīšanas operācijām šajā zonā.
    - **Neaktīvs** - atzīmēta izvēles rūtiņa norāda, ka lietotāja konts ir neaktīvs. Ja darbinieks noliktavas programmā rindā ievada nepareizu paroli, lietotāja konts tiek automātiski deaktivizēts. Šo opciju varat atzīmēt arī manuāli. Noņemiet izvēles rūtiņas atzīmi, lai lietotāju atkal aktivizētu.

1. Kopsavilkuma cilnē **Darbs**, iestatiet tālāk minētos laukus:

    - **Atļaut izdošanas atrašanās vietas ignorēšanu** — iestatiet šo opciju kā *Jā*, lai ļautu darbiniekam ignorēt izdošanas soļu novietojumu. Šī iespēja var būt noderīga, ja fiziskie krājumi neatbilst sistēmas ieteicamajam novietojumam.
    - **Atļaut izvietošanas atrašanās vietas ignorēšanu** — iestatiet šo opciju kā *Jā*, lai ļautu darbiniekam ignorēt izvietošanas soļu novietojumu. Šī iespēja var būt noderīga, ja ieteiktā izvietošanas vieta pašlaik ir pilna vai nav pieejama, vai arī sagatavošanas vieta ir mainīta.
    - **Atļaut pārdošanu izdošanas vietā** - iestatiet šo opciju kā *Jā*, lai ļautu darbiniekam veikt pārdošanu, kad tiek izdoti pārdošanas pasūtījumi. Papildinformāciju skatiet [Pārdošanas un pārsūtīšanas pasūtījumu izdošana](over-picking-for-sales-and-transfer-orders.md).
    - **Atļaut pārsūtīšanas pasūtījumu izdošanas vietā** - iestatiet šo opciju kā *Jā*, lai ļautu darbiniekam veikt pārizdošanu, kad tiek izdoti pārsūtīšanas pasūtījumi. Papildinformāciju skatiet [Pārdošanas un pārsūtīšanas pasūtījumu izdošana](over-picking-for-sales-and-transfer-orders.md).
    - **Atļaut krājumu kustību ar saistīto darbu** - iestatiet šo opciju kā *Jā*, lai darbinieks varētu pārvietot krājumus, kas jau ir rezervēti vai jau saistīti ar citu darbu. Papildinformāciju skatiet [Krājumu kustība, ja ar tiem noliktavas pārvaldībā ir saistīts darbs](move-inventory-associated-work.md).
    - **Atļaut manuālu krājumu numuru atrašanās vietu** - iestatiet šo opciju kā *Jā*, lai iespējotu darbiniekam manuālu atkārtotas rezervēšanas iespēju īsās izdošanas laikā. Krājumu atkārtotas atrašanās vietas noteikšana vada darbiniekus izdot krājumus no citas atrašanās vietas. Lai gan automātiska atkārtota atrašanās vieta ir pieejama visiem darbiniekiem, manuālai atkārtotai izvietošanai ir nepieciešami īpaši iestatījumi darbiniekam. Spēja kontrolēt manuālu katra darbinieka atkārtotas atrašanās vietu var palīdzēt, jo tā ļauj kontrolēt redzamību, kas katram darbiniekam ir, piemēram, kad krājumu izdošana no karantīnas vai lielapjoma zonas tiek ierobežota ar uzticamiem darbiniekiem. Papildinformāciju skatiet šajā postā: [Automātiska un manuāla krājumu atkārtota atrašanās vieta īso izdošanas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Ir cikla inventarizācijas uzraugs** - iestatiet šo opciju kā *Jā*, lai darbinieku padarītu par cikla inventarizācijas uzraugu. Šajā gadījumā tūlīt tiks apstiprinātas visas tās cikla inventarizācijas, ko darbinieks veic noliktavas programmā. Lauki **Maksimālais procentuālais ierobežojums**, **Maksimālais daudzuma ierobežojums** un **Maksimālās vērtības ierobežojums** nav apsvērti darbiniekiem, kuriem šī opcija ir iestatīta uz *Jā*.
    - **Maksimālais procentuālais ierobežojums** - Ievadiet vislielāko procentuālo daudzumu, par kādu cikla inventarizācija var atšķirties no paredzētā daudzuma un nav jāsaņem apstiprinājums no cikla inventarizācijas supervizora.
    - **Maksimālais daudzuma ierobežojums** – ievadiet kopējo daudzumu, ko ievadītais daudzums var atšķirties no paredzamā daudzuma (vienībās), bez cikla inventarizācijas supervizora apstiprinājuma.
    - **Maksimālās vērtības ierobežojums** - Ievadiet maksimālo summu, par kādu krājumu izmaksas var atšķirties no paredzētajām izmaksām un nav jāsaņem apstiprinājums no cikla inventarizācijas supervizora.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Ja esat pievienojis jaunu lietotāja kontu, tiek parādīts dialoglodziņš **Iestatīt paroli**, kur varat izveidot vienkāršu paroli, ko lietotājs var izmantot, lai pieteiktos mobilajā programmā. Ievadiet vienkāršo paroli divas reizes un pēc tam atlasiet **Saglabāt paroli**, lai turpinātu.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Iestatīt valodu, numuru formātus un laika joslu katram noliktavas programmas lietotājam

Kad darbinieks pierakstās mobilajā programmā Warehouse Management, valoda, numuru formāti un laika josla mainās, lai atbilstu darbinieka preferences. Konta iestatījumi darbiniekam, kas ir atlasīts sadaļas [Iestatīt mobilās ierīces lietotāja kontus](#set-wma-users) 3. darbībā, nosaka izmantotos iestatījumus. Ja nepieciešams atsevišķs iestatījums katram lietotājam, izmantojiet dažādus darbinieka kontus. Šī procedūra parāda, kā mainīt valodu, numuru formātus un laika joslu katram noliktavas programmas lietotājam.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Atrodiet tā darbinieka vārdu, ko vēlaties iestatīt. Pārliecinieties, vai darbiniekam ir visi nepieciešamie noliktavas programmas lietotāja konti, kas ir uzskaitīti kopsavilkuma cilnē **Lietotāji**. Izveidojiet jaunu darbinieku un/vai pievienojiet noliktavas programmas lietotāja kontus pēc vajadzības, izpildot sadaļā [Iestatīt mobilās ierīces lietotāja kontus](#set-wma-users) norādītās darbības.
1. Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
1. Atlasiet lietotāja kontu, kur kolonna **Persona** parāda 2. solī atrastā darbinieka vārdu.

    > [!IMPORTANT]
    > **Lietotāja ID** vērtības, kas ir norādītas lapā **Lietotāji**, *neattiecas* uz vērtību, kas ir parādīta kopsavilkuma cilnes **Lietotāji** lapā **Darbinieki**, ko atvērāt 1. darbībā.

1. Darbību rūtī atlasiet **Lietotāja opcijas**.
1. Cilnē **Preferences** iestatiet šādus laukus:

    - **Valoda** – atlasiet valodu, kādu darbinieks vēlas. Šis lauks kontrolē arī numura formātu, kas tiek rādīts noliktavas programmā.
    - **Datums, laiks un numura formāts** – atlasiet datuma un laika formātu, kam darbinieks dod priekšroku. Noliktavas programma izmanto skaitļu formātu, kas saistīts ar valodu, kura izvēlēta laukā **Valoda**, nevis šis iestatījums.
    - **Laika josla** – atlasiet laika joslu, kurā darbinieks strādā. Šis lauks ietekmē laikspiedolu visām reģistrācijām, ko darbinieks veic, izmantojot programmu.

> [!NOTE]
> Dažos gadījumos noliktavas programma nevarēs atrast noteiktus darbinieka iestatījumus, kas nosaka valodu, numuru formātus un laika zonu. Ir spēkā šādi nosacījumi:
>
> - Ja programma nav saistīta ar Supply Chain Management vidi (piemēram, pirmo reizi, kad programma tiek startēta pēc tās instalēšanas), tiek izmantota lokālās ierīces valoda. Kad mainās ierīces valoda, mainās arī programmas valoda. Papildinformāciju par valodas konfigurēšanu vietējai ierīcei skatiet jūsu ierīces un/vai operētājsistēmas dokumentācijā.
> - Ja programma ir saistīta ar Supply Chain Management vidi, taču pierakstīšanās darbiniekam nav iestatīta neviena preferences, valoda, numuru formāti un laika josla tiek atlasīta, pamatojoties uz kontu, kas ir saistīts ar klienta ID, kuru ierīce izmanto, lai izveidotu savienojumu ar Supply Chain Management. Papildinformācijai skatiet [Izveidot un konfigurēt lietotāja kontu programmatūrā Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Ja ievērojat, ka reģistrācijām, kas veiktas, izmantojot noliktavas programmu, tiek rādīti nepareizi laika zīmogi, iespējams, būs jāpielāgo laika josla, kas ir iestatīta lietotāja kontam, ko darbinieki izmanto, lai pieteiktos un/vai autentificētos risinājumā Supply Chain Management. Kā tika norādīts iepriekš, laika joslas iestatījums varētu būt no lietotāja konta, kas tiek izmantots, lai pieteiktos noliktavas programmā, kā iestatīts lapā **Darbinieks**. Vai arī, ja lietotāja konts nav iestatīts lapā **Darbinieks**, laika josla tiek ņemta no lietotāja konta, kas ir saistīts ar autentifikācijai izmantoto klienta ID, kā iestatīts pieteikumu **[Azure Active Directory](install-configure-warehouse-management-app.md)** lapā.
