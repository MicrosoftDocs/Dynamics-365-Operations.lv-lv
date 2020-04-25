---
title: Izveidot funkcionālos novietojumus
description: Šajā tēmā izskaidrots, kā izveidot funkcionālos novietojumus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8ba905224fbbcc5db95820e2b228a0d478e6146
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205409"
---
# <a name="create-functional-locations"></a>Izveidot funkcionālos novietojumus

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā izskaidrots, kā izveidot funkcionālos novietojumus Līdzekļu pārvaldībā.

Veidojot funkcionālo novietojumu struktūru, ņemiet vērā, ka pēc funkcionālā novietojuma izveidošanas to nevar pārvietot no sākotnējās atrašanās vietas. Tas nozīmē, ka pirms sākat to veidošanu Līdzekļu pārvaldībā, rūpīgi apsveriet savu funkcionālo novietojumu struktūru. Ja neesat apmierināts ar funkcionālo novietojumu, varat to izdzēst, ja tas vēl nav izmantots.

Lai varētu strādāt ar funkcionālajiem novietojumiem, sāciet ar funkcionālo novietojumu divu "kategoriju" izveidi:

- Izveidojiet *vienu* noklusējuma funkcionālo novietojumu bez apakšvietām. Šis funkcionālais novietojums tiek izmantots tikai kā līdzekļu standarta atrašanās vieta, kad veidojat jaunus līdzekļus.  
- Izveidojiet funkcionālā novietojuma struktūras, kas nepieciešamas, lai pārvaldītu uzturēšanas darbus jūsu uzņēmumā.

## <a name="create-a-default-functional-location"></a>Noklusējuma funkcionālā novietojuma izveide

Ja izmantojat funkcionālos novietojumus, vispirms izveidojiet vienu noklusējuma atrašanās vietu, kas jāizmanto, veidojot jaunus līdzekļus. Šis funkcionālais novietojums ir tas, ko atlasāt **Līdzekļu pārvaldībā** > **Iestatīšanā** > **Līdzekļu pārvaldības parametros** > **Līdzekļu** saitē > laukā **Noklusējuma funkcionālais novietojums**. Noklusējuma funkcionālo novietojumu var izmantot, kad veidojat jaunus līdzekļus un vēl neesat iestatījis šo līdzekļu funkcionālā novietojuma struktūru.

1. Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Funkcionālie novietojumi** > **Visi funkcionālie novietojumi**.  
2. Laukā **Visi funkcionālie novietojumi**atlasiet **Jauns**.
3. Laukā **Funkcionālais novietojums** ievietojiet ID, piemēram, "0000" vai "Noklusējums", lai norādītu, ka šis ir īpašs funkcionālais novietojums.
4. Laukā **Nosaukums** ievadiet noklusējuma funkcionālā novietojuma nosaukumu.
5. *Neatlasiet* pamatelementu laukā **Pamatelements** — atstājiet šo lauku tukšu.
6. Laukā **Funkcionālā novietojuma veids** atlasiet funkcionālā novietojuma veidu, kas jāizmanto noklusējuma funkcionālajam novietojumam. Papildinformāciju par funkcionālo novietojumu veidu iestatīšanu skatiet [Funkcionālo novietojumu veidi](../setup-for-functional-locations/functional-location-types.md).
7. Atlasiet **Labi**. Jūs nedrīkstat pievienot papildu datus šim funkcionālajam novietojumam, jo to izmanto tikai kā pagaidu atrašanās vietu jauniem līdzekļiem, kamēr uzstādāt līdzekļus jūsu uzņēmuma izmantotajos funkcionālajos novietojumos.

## <a name="create-functional-locations"></a>Izveidot funkcionālos novietojumus

Šī procedūra apraksta, kā jūs izveidojat funkcionālos novietojumus, kas nepieciešami uzturēšanas pārvaldībai jūsu uzņēmumā.

1. Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Funkcionālie novietojumi** > **Visi funkcionālie novietojumi**. Funkcionālo novietojumu varat izveidot no režģa skata vai detalizētas informācijas skata.
2. Atlasiet pogu **Jauns**.
3. Ievadiet ID laukā **Funkcionālais novietojums**.
4. Laukā **Nosaukums** ievadiet funkcionālā novietojuma nosaukumu.
5. Ja funkcionālais novietojums ir pakārtotā atrašanās vieta struktūrā, atlasiet vecākelementa vietu laukā **Vecākelements**.
6. Atlasiet veidu laukā **Funkcionālā novietojuma veids**.
7. Atlasiet **Labi**.
8. Atlasiet funkcionālo novietojumu un noklikšķiniet uz pogas **Rediģēt**, lai pievienotu papildu informāciju.

>[!NOTE]
>Atkarībā no jūsu funkcionālā novietojuma dzīves cikla stāvokļa iestatījumiem, iespējams, ir jāizveido visas pakārtotās atrašanās vietas funkcionālajam novietojumam un pēc tam jāmaina funkcionālā novietojuma dzīves cikla stāvoklis, pirms sākat uzstādīt līdzekļus. Plašāku informāciju par līdzekļu uzstādīšanu skatiet sadaļā [Līdzekļu uzstādīšana funkcionālajos novietojumos](../functional-locations/install-objects-on-functional-locations.md). Lai uzzinātu vairāk par funkcionālā novietojuma dzīves cikla stāvokļu iestatīšanu, skatiet sadaļu [Funkcionālo novietojumu dzīves cikla stāvokļi](../setup-for-functional-locations/functional-location-stages.md).

Detalizētas informācijas skatā redzēsit kopsavilkuma cilnes, kurās var pievienot un rediģēt informāciju par funkcionālo novietojumu.

## <a name="general-information"></a>Vispārīgā informācija

Šajā sadaļā ir sniegts pārskats par pamatelementa un pakārtotā elementa informāciju funkcionālā novietojuma struktūrā. Sadaļā **Detalizēta informācija** ir redzams to līdzekļu atribūtu, uzturēšanas plānu un līdzekļu skaits, kas ir saistīti ar funkcionālo novietojumu. Sadaļā **Krājumi** varat atlasīt vietu un noliktavu, ar kuru ir saistīts funkcionālais novietojums. Vieta un noliktava tiek izmantota saistībā ar darba pasūtījuma krājumu prognozēm. Veidojot krājuma prognozi, automātiski tiek izmantota vietas un noliktavas informācija no līdzekļa funkcionālā novietojuma. Sadaļā **Dzīves cikla stāvoklis** tiek parādīta informācija par funkcionālā novietojuma dzīves cikla stāvokli.

## <a name="installed-assets"></a>Uzstādītie līdzekļi

Plašāku informāciju par līdzekļu uzstādīšanu skatiet sadaļā [Līdzekļu uzstādīšana funkcionālajos novietojumos](../functional-locations/install-objects-on-functional-locations.md). Varat izmantot pogu **Skatīt** šajā kopsavilkuma cilnē, lai kopsavilkuma cilnē parādītu vairāk lauku. Lauki **Derīgs no** un **Apakšlīdzeklis** var tikt parādīti režģī.

## <a name="asset-attribute-requirements"></a>Līdzekļu atribūtu prasības

Šajā kopsavilkuma cilnē varat pievienot īpašas atribūtu prasības līdzekļiem, ko uzstādāt funkcionālajā novietojumā. Šīs prasības ir paredzētas tikai informācijas nolūkos. Tās neliedz jums uzstādīt līdzekļus ar citām atribūtu prasībām. Atlasiet **Pievienot rindu** un atlasiet atribūta veidu. Pēc tam ievietojiet atbilstošo **Vērtību**, atlasiet sliekšņvērtību laukā **Sliekšņvērtības kritēriji** un saglabājiet ierakstu.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Uzturēšanas plāni un uzturēšanas cikli

Šeit varat funkcionālajam novietojumam pievienot uzturēšanas plānus un uzturēšanas ciklus, ieskaitot sākuma datumu. Līdzekļiem, kas uzstādīti funkcionālajā novietojumā, var būt iestatīti citi uzturēšanas plāni. Visus uzturēšanas plānus un uzturēšanas ciklus var izmantot, lai plānotu līdzekļu kalendāra ierakstus funkcionālajam novietojumam un pašlaik tajā uzstādītajiem līdzekļiem.

>[!NOTE]
>Ja atjaunināt līdzekļu veidu, līdzekļu zīmolu un līdzekļu modeļu iestatīšanu uzturēšanas plānos detalizētas informācijas skatā **Visi funkcionālie novietojumi**  > kopsavilkuma cilnā **Uzturēšanas plāni** pēc tam, kad esat ieplānojis uzturēšanas plānus, esošie ar šo funkcionālo novietojumu saistītie uzturēšanas grafika ieraksti tiek automātiski dzēsti. Lai izveidotu jaunus grafika ierakstus, kas atbilst atjauninātajam uzturēšanas plāna iestatījumam funkcionālajā novietojumā, ir jāpalaiž jauns uzturēšanas plāna grafiks minētajam funkcionālajam novietojumam. 

## <a name="address"></a>Adrese

Kopsavilkuma cilnē **Adrese** ievietojiet funkcionālā novietojuma adresi. Adreses funkcionālajos novietojumos ir pārmantotas, t.i., ja apakšvietai nav definēta adrese, tiek izmantota vecākelementa atrašanās vietas adrese.

## <a name="workers"></a>Nodarbinātie

Šajā kopsavilkuma cilnē varat pievienot darbiniekus, kas ir saistīti ar funkcionālo novietojumu, un varat darbiniekam atlasīt funkcionālo novietojumu kā primāro. 

## <a name="attributes"></a>Atribūti

Šajā kopsavilkuma cilnē var iestatīt vērtības funkcionālā novietojuma atribūtiem. Šos atribūtus var izmantot, lai aprakstītu rekvizītus vai raksturlielumus, kas attiecas uz funkcionālo novietojumu, piemēram, struktūras rekvizītus, ēkas veidu, laukumu aprakstus vai atrašanās vietu virs vai zem zemes.

Atlasiet **Pievienot rindu** un atlasiet atribūta veidu. Pēc tam ievietojiet ar atribūta veidu saistīto **Vērtību** un saglabājiet ierakstu.

## <a name="financial-dimensions"></a>Finanšu dimensijas

Funkcionālajam novietojumam varat atlasīt finanšu dimensijas. [Funkcionālo novietojumu veidus](../setup-for-functional-locations/functional-location-types.md) var iestatīt, lai no funkcionālā novietojuma varētu automātiski atjaunināt finanšu dimensijas. Tas nozīmē, ka finanšu dimensijā uzstādītie līdzekļi automātiski saņem funkcionālā novietojuma finanšu dimensijas. Tas noder, ja vēlaties atšķirīgus izmaksu centrus atkarībā no atrašanās vietām.

Kad dati par **Vietu**, **Noliktavu**, **Adresi**un **Finanšu dimensijām** tiek atjaunināti vecākelementa funkcionālajā novietojumā, attiecīgi var atjaunināt saistītos pakārtotos funkcionālos novietojumus, ja atjaunināšanas laikā veicat šādu atlasi. Tiek atvērts dialoglodziņš, kas nodrošina atjaunināšanas opcijas.

## <a name="copy-a-functional-location-structure"></a>Funkcionālā novietojuma struktūras kopēšana

Ja jūsu uzņēmumam ir vairāki funkcionālie novietojumi ar līdzīgām atrašanās vietas struktūrām, varat izmantot kopēšanas funkciju Līdzekļu pārvaldībā, lai ātri izveidotu līdzīgu atrašanās vietu hierarhiju. Kopējot noteiktu funkcionālo novietojumu vai visu struktūru, jaunajai atrašanās vietai vai struktūrai ir tāds pats nosaukums kā tai, kuru kopējāt. Kad kopēšanas procedūra ir pabeigta, varat viegli mainīt nosaukumu vai citus iestatījumus jaunajam funkcionālajam novietojumam, ja jaunajam funkcionālajam novietojumam atlasītais funkcionālā novietojuma dzīves cikla stāvoklis to atļauj.

1. Laukā **Visi funkcionālie novietojumi**atlasiet funkcionālo novietojumu, kuru vēlaties kopēt. Piemēram, jūs atlasāt augšējo atrašanās vietu (vecākelementu), ja vēlaties kopēt visu funkcionālā novietojuma struktūru, ieskaitot apakšvietas.
2. Atlasiet pogu **Kopēt funkcionālo novietojumu**. Atrašanās vieta, kuru atlasījāt saraksta lapā, ir redzama laukā **Kopēt no**.
3. Ievietojiet jaunās atrašanās vietas nosaukumu laukā **Jaunais funkcionālais novietojums**.
4. Laukā **Vecākelements, zem kura jāielīmē** būtu jāievieto vecākelementa ID tikai tad, ja atrašanās vietai, kuru veidojat, jābūt daļai no esošas funkcionālā novietojuma struktūras.
5. Noklikšķiniet uz **Labi**. Jaunā funkcionālā novietojuma struktūra ir redzama laukā **Visi funkcionālie novietojumi**.

>[!NOTE]
>Kopējot funkcionālā novietojuma struktūru, funkcionālā novietojuma dzīves cikla stāvokļi jaunajā struktūrā tiek iestatīti uz "pirmo stāvokli", kuru esat izveidojis funkcionālajiem novietojumiem. Tas, vai varat pārdēvēt vai dzēst funkcionālu novietojumu, izmantojot pogas **Pārdēvēt** un **Dzēst** laukā **Visi funkcionālie novietojumi**, ir atkarīgs no funkcionālā novietojuma pašreizējā dzīves cikla stāvokļa.

## <a name="delete-a-functional-location"></a>Funkcionālā novietojuma dzēšana

Funkcionālais novietojums ar saistītajām apakšvietām var tikt dzēsts, ja nevienā no funkcionālajiem novietojumiem, ko mēģināt dzēst, nav uzstādīts neviens līdzeklis un ja to atļauj pašreizējais funkcionālā novietojuma dzīves cikla stāvoklis.

1. Laukā **Visi funkcionālie novietojumi**atlasiet funkcionālo novietojumu, kuru vēlaties dzēst.
2. Ja nepieciešams, atjauniniet funkcionālo novietojumu uz funkcionālā novietojuma dzīves cikla stāvokli, kas atļauj dzēst funkcionālo novietojumu.
3. Atlasiet **Dzēst**.

>[!NOTE]
>Ja nevarat izdzēst funkcionālo novietojumu, varat veikt dzēšanu, šim nolūkam iestatot funkcionālā novietojuma dzīves cikla stāvokli. Piemēram, varat iestatīt stadiju "Norakstīts" vai "Dzēsts", kas nedrīkst būt aktīva stadija, veidlapā **Funkcionālā novietojuma dzīves cikla stāvokļi**.
