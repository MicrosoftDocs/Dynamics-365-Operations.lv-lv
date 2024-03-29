---
title: Pielāgotu lauku izveide un darbs ar tiem
description: Šajā rakstā parādīts, kā izveidot pielāgotus laukus, izmantojot lietotāja interfeisu, lai pielāgotu programmu jūsu biznesam.
author: jasongre
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: fdb4d0065bd12fc721ce55314c0a46fe8d17c6ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847133"
---
# <a name="create-and-work-with-custom-fields"></a>Pielāgotu lauku izveide un darbs ar tiem

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Lai gan ir plaša lietošanai gatavu lauku kopa dažādu veidu biznesa procesu pārvaldībai, dažkārt uzņēmumam ir nepieciešams sistēmā izsekot papildu informāciju. Lai gan programmētājus var izmantot, lai šos laukus pievienotu kā paplašinājumus izstrādātāja rīkos, pielāgoto lauku līdzeklis atļauj laukus pievienot tieši no lietotāja interfeisa, tādējādi ļaujot jums pielāgot programmu, lai tā atbilstu jūsu biznesa vajadzībām, izmantojot Web pārlūkprogrammu.

*Šim līdzeklim ir piekļuve tikai tiem lietotājiem, kuriem ir īpašas atļaujas.*

Šajā video parādīts, cik viegli ir lapai pievienot pielāgotu lauku: [Pielāgotu lauku pievienošana](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Pielāgoto lauku izveide

Kad esat noteicis, kādu papildu informāciju vēlaties izsekot programmā, attiecīgajā tabulā varat izveidot pielāgoto laiku un sniegt šo jauno lauku lapā.

Tālākajās darbībās aprakstīts process pielāgota lauka izveidei un šī lauka ievietošanai formā.

1. Atveriet formu, kurā nepieciešams pievienot jauno lauku.
2. Tā kā mērķis ir pielāgoto lauku sniegt formā, pielāgoto lauku ieejas punkts ir personalizēšanas pieredzē. Atveriet personalizēšanas rīkjoslu, atlasot vienumu **Opcijas** un pēc tam atlasot vienumu **Personalizēt šo formu**.
3. Noklikšķiniet uz vienuma **Ievietot** un pēc tam uz **Lauks**.
4. Atlasiet to formas reģionu, kurā vēlaties parādīt jauno lauku. Pēc atlases dialoglodziņā **Ievietot laukus** tiks parādīts saraksts ar esošiem laukiem, ko var ievietot atlasītajā formas reģionā.
5. Pārliecinieties, vai interesējošais lauks jau nav sarakstā. Ja tas ir sarakstā, atlasiet šo lauku un noklikšķiniet uz **Ievietot**.
6. Noklikšķiniet uz pogas **Izveidot jaunu lauku** virs saraksta, lai uzsāktu pielāgota lauka izveides procesu. Tiks atvērts dialoglodziņš **Izveidot jaunu lauku**.

    Ja neredzat pogu **Izveidot jaunu lauku**, jums nav nepieciešamo atļauju šī līdzekļa lietošanai.

7. Dialoglodziņā **Izveidot jaunu lauku** ievadiet tālāk norādīto informāciju.
   
    1. Atlasiet datu bāzes tabulu, kurai jāpievieno šis lauks. Ņemiet vērā, ka nolaižamajā sarakstā tiks parādītas tikai tabulas, kas atbalsta pielāgotos laukus. Tehnisko informāciju par atbalstītajām tabulām skatiet tālāk esošajā sadaļā.

    2. Atlasiet jaunā lauka datu tipu. Pieejamie datu tipi ir izvēles rūtiņa, datums, datums un laiks, decimāldaļskaitlis, skaitlis, salasīšanas saraksts un teksts.

        - Ja izvēlaties teksta datu tipu, var arī norādīt maksimālo šajā laukā ievadāmā teksta garumu.
        - Ja izvēlaties salasīšanas saraksta datu tipu, varat arī atlasīt laukam derīgo vērtību kopu.

    3. Norādiet lauka nosaukumu, etiķeti un palīdzības tekstu. Nosaukums atbilst fiziskajam lauka nosaukumam datu bāzē, savukārt etiķete un palīdzības teksts ir teksts, kas šo lauku attēlo lietotāja interfeisā.

8. Ja tas ir vienīgais lauks, kas jums jāizveido šai formai, noklikšķiniet uz **Saglabāt**. Ja nepieciešams izveidot papildu laukus, noklikšķiniet uz **Saglabāt un izveidot jaunu** un pārejiet uz 7. darbību. Ņemiet vērā, ka pašlaik ir noteikts ierobežojums **20 pielāgoto lauku vienā tabulā**.
9. Ja iziesit no dialoglodziņa **Izveidot jaunu lauku**, tiksit novirzīts uz dialoglodziņu **Ievietot laukus**. Visi tikko pievienotie pielāgotie lauki tiks automātiski atzīmēti lauku sarakstā ievietošanai formā.
10. Lai atzīmētos laukus ievietotu atlasītajā formas reģionā, noklikšķiniet uz **Ievietot**.
11. **Neobligāti:** iespējojiet personalizēšanas rīkjoslā režīmu **Pārvietot**, lai jaunos laukus pārvietotu uz vajadzīgo vietu atlasītajā reģionā. Papildinformāciju par to, kā izmantot dažādās personalizēšanas iespējas, lai formu optimāli pielāgotu personīgajam lietojumam, skatiet tēmā [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).

> [!WARNING]
> Spēja ievadīt vērtības pielāgotā laukā, kas pievienots lapai, ir atkarīga no tā, vai ar pielāgoto lauku saistītā tabula ir rediģējama vai tikai lasāma. Kad saistītā tabula ir tikai lasāma, visi ar šo tabulu saistītie lauki, tostarp visi pielāgotie lauki, arī būs tikai lasāmi.


## <a name="sharing-custom-fields-with-other-users"></a>Pielāgoto lauku koplietošana ar citiem lietotājiem

Kad esat izveidojis pielāgotu laiku un sniedzis to lapā, iespējams, šo atjaunināto lapas skatu, kurā ietverts jaunais lauks, vēlaties nodrošināt citiem sistēmas lietotājiem. To var izdarīt divos dažādos veidos, izmantojot produkta personalizēšanas iespējas.

- Ieteicamais maršruts ir **publicēt [saglabāto skatu](saved-views.md)** ar pielāgoto lauku, kas pievienots lapai atbilstošajai lietotāju kopai. Ja saglabāto skatu līdzeklis nav iespējots, sistēmas administrators var pielietot personalizēšanu vēlamajiem lietotājiem no personalizēšanas formas. Papildinformāciju skatiet [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).
- Vai arī varat eksportēt veiktās izmaiņas (dēvētas par *personalizācijām*), nosūtīt tās vienam vai vairākiem lietotājiem un likt katram no šiem lietotājiem importēt izmaiņas. Izmantojot personalizēšanas rīkjoslā esošo opciju **Pārvaldīt**, varat eksportēt un importēt personalizācijas.

## <a name="managing-custom-fields"></a>Pielāgoto lauku pārvaldība

Visus sistēmā esošos pielāgotos laukus var pārvaldīt, izmantojot lapu **Pielāgoti lauki** sistēmas administrēšanas modulī. Izmantojot šo lapu, lietotāji var piekļūt daudzām iespējām, tostarp tālāk norādītajām.

- Visu sistēmā esošo pielāgoto lauku saraksta skatīšana.
- Ierobežota esošo pielāgoto lauku rediģēšana.
- Pielāgoto lauku dzēšana.
- Pielāgoto lauku sniegšana datu elementos.
- Pielāgoto lauku etiķešu un palīdzības teksta tulkojumu nodrošināšana.

### <a name="viewing-all-custom-fields"></a>Visu pielāgoto lauku skatīšana

Lapa **Pielāgoti lauki** nodrošina visu sistēmā definēto pielāgoto lauku redzamību. Atlasiet interesējošo tabulu, un lapa tiks atjaunināta, lai parādītu ar šo tabulu saistītos pielāgotos laukus. Izvēloties pielāgotu lauku no saraksta, varēsit skatīt visu informāciju par lauku.

### <a name="editing-custom-fields"></a>Pielāgoto lauku rediģēšana

Pēc pielāgotā lauka izveides lapā **Pielāgoti lauki** var modificēt tikai noteiktu informāciju par šo pielāgoto lauku.

*Var* modificēt tālāk norādītos atribūtus.

- Iezīme
- Palīdzības teksts
- Garums (teksta laukiem)

*Nevar* rediģēt tālāk norādītos atribūtus.

- Lauka nosaukums
- Datu tips

Turklāt salasīšanas sarakstiem var pārkārtot pielāgotā lauka derīgo vērtību kopu un pievienot jaunas vērtības. Tomēr esošās salasīšanas saraksta lauka vērtības nevar noņemt. Kad esat pabeidzis rediģēt noteiktas tabulas laukus, noteikti noklikšķiniet uz vienuma **Lietot izmaiņas**, lai izmaiņas tiktu saglabātas.

### <a name="exposing-custom-fields-on-data-entities"></a>Pielāgoto lauku sniegšana datu elementos

Var būt svarīgi arī atļaut pielāgotajiem laukiem būt redzamiem datu elementos. Datu elementi tiek izmantoti līdzeklī [Office integrēšanas pārskats](../../dev-itpro/office-integration/office-integration.md), kā arī datu importēšanas/eksportēšanas scenārijiem.

Lai pielāgoto lauku sniegtu datu elementam, veiciet tālāk norādītās darbības.

1. Atlasiet pielāgoto lauku formā **Pielāgoti lauki**.
2. Izvērsiet sadaļu **Elementi**, lai skatītu attiecīgo elementu kopu.
3. Noklikšķiniet uz pogas **Rediģēt**.
4. Modificējiet lauku **Iespējot** atlasīšanai katram elementam, kam ir jāsniedz šis lauks.
5. Noklikšķiniet uz **Lietot izmaiņas**, lai saglabātu veiktās atlases.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Atļauja pielāgotos laukus parādīt citās valodās

Tā kā pielāgotajiem laukiem, iespējams, vajadzēs piekļūt lietotājiem, kuri pārzina dažādas valodas, lapā **Pielāgoti lauki** nodrošināts mehānisms, kas pielāgotā lauka etiķeti un palīdzības tekstu ļauj iztulkot citās valodās.

Tālāk esošajās darbībās aprakstīts pielāgoto lauku tulkošanas process citās valodās.

1. Lapā **Pielāgoti lauki** atlasiet pielāgoto lauku.
2. Darbību rūtī atlasiet pogu **Tulkojumi**. Tiks atvērta nolaižamā izvēlne ar esošajiem šī lauka tulkojumiem.
3. Nolaižamajā izvēlnē **Valoda** parādīta to valodu kopa, kam jau ir nodrošināti tulkojumi.

    Ja vēlaties rediģēt esošu tulkojumu, izvēlnē atlasiet vajadzīgo valodu un modificējiet etiķetes un palīdzības teksta vērtības.

    Ja to nevēlaties darīt, noklikšķiniet uz pogas **Pievienot valodu**, izvēlnē atlasiet vajadzīgo valodu un nodrošiniet tulkotās etiķetes un palīdzības teksta vērtības.

4. Kad esat pabeidzis, noklikšķiniet uz **Labi**.

### <a name="deleting-custom-fields"></a>Pielāgoto lauku dzēšana

Dažos retos gadījumos varat izlemt, ka pielāgotais lauks vairs nav vajadzīgs. Ja tā notiek, sistēmas administrators var izvēlēties dzēst šo lauku no lapas **Pielāgoti lauki**. Lai to izdarītu, pārliecinieties, vai ir atlasīts pareizais lauks, noklikšķiniet uz **Dzēst**, noklikšķiniet uz **Jā**, lai apstiprinātu dzēšanu, pēc tam noklikšķiniet uz **Lietot izmaiņas**.

> [!NOTE]
> Šo darbību nevar atsaukt, un tās rezultātā ar lauku saistītie dati tiks neatgriezeniski izdzēsti no datu bāzes.

## <a name="appendix"></a>Pielikums

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Kāpēc pielāgotajā laukā nevar ievadīt vērtību? 

Ja pielāgotajā laukā nevar ievadīt vērtību, kad lapa ir Rediģēšanas režīmā, iespējams, tabula, pie kuras lauks tika pievienots, pašlaik ir tikai lasāma. Visi tabulas lauki kļūst tikai lasīti tikai tad, ja dublēšanas tabula pašlaik ir konfigurēta, kā tikai lasāma lapā.   

### <a name="who-can-create-custom-fields"></a>Kas var izveidot pielāgotos laukus?

Drošības apsvērumu dēļ pielāgotos laukus pēc noklusējuma var izveidot tikai sistēmas administratori. Taču prasmīgiem lietotājiem, kuriem pēc organizācijas ieskatiem tas ir nepieciešams, sistēmas administrators var piešķirt tiesības izveidot pielāgotos laukus, izmantojot drošības lomu **Prasmīgs izpildlaika pielāgošanas lietotājs**. Lietotāji bez šīs drošības lomas nevarēs izveidot pielāgotos laukus, taču joprojām varēs skatīt citu lietotāju sistēmā pievienotos pielāgotos laukus un mijiedarboties ar tiem.

### <a name="what-tables-support-custom-fields"></a>Kādas tabulas atbalsta pielāgotos laukus?

Veiktspējas un tehnisku iemeslu dēļ pielāgotos laukus pašlaik var pievienot tikai tabulām, kas atbilst tālāk norādītajiem nosacījumiem.

- Tabulai ir jābūt atzīmētai kā vienai no tālāk norādītajām grupām.

    - Grupa
    - WorksheetHeader
    - Galvenā
    - Dažādi
    - Parametrs
    - Atsauce
    - TransactionHeader

- Tabula nedrīkst paplašināt citu tabulu.
- Tabula nedrīkst būt atzīmēta kā sistēmas tabula.
- Tabula nedrīkst būt pagaidu tabula.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Vai es varu norādīt pielāgotus laukus no izstrādātāja rīkiem?  

Pielāgotus laukus var pārvaldīt tikai ar lietotāja interfeisu, un tos nevar norādīt ar kodu. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
