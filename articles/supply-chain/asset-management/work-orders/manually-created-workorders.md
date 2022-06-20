---
title: Manuāli izveidotie darba pasūtījumi
description: Šajā rakstā skaidrots, kā izveidot darba pasūtījumus manuāli Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb29c5e7170011b95151d9aaf2a96a570563096d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902087"
---
# <a name="manually-created-work-orders"></a>Manuāli izveidotie darba pasūtījumi

[!include [banner](../../includes/banner.md)]


Ir divi veidi, kādos var manuāli izveidot darba pasūtījumus:

- Lapā **Visi darba pasūtījumi** vai **Aktīvi darba pasūtījumi**. 
- Lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**. 

## <a name="create-work-order"></a>Izveidot darba pasūtījumu

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**

2. Atlasiet **Jauns**.

3. Dialogā **Izveidot darba pasūtījumu** atlasiet darba pasūtījuma veidu laukā **Darba pasūtījuma veids**.

4. Ja nepieciešams, atlasiet **Apraksts**.

5. Atlasiet līdzekli laukā **Līdzeklis**.

>[!NOTE]
>Atlasot līdzekli, **Līdzeklis** nolaižamajā sarakstā var būt pieejamas trīs cilnes: 

- **Aktīvie līdzekļi** - Šajā cilnē ir iekļauts visu līdzekļu saraksts ar līdzekļa dzīves cikla statusu "Aktīvs". 
- **Līdzekļu skats** - Šī cilne parāda funkcionālo novietojumu koku un tajos uzstādītos līdzekļus.
- **Mani līdzekļi** - Šajā cilnē ir ietverti līdzekļi, kas ir saistīti ar funkcionālajiem novietojumiem, ko jums (darbiniekam, kurš ir pieteicies sistēmā) var tikt piešķirts. (Informāciju par iestatīšanu skatiet [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).) Ja speciālistam nav iestatīti funkcionālie novietojumi [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md), tad cilne **Mani līdzekļi** nav pieejama. 

6. Laukā **Uzturēšanas darba tips** atlasiet darba pasūtījuma uzturēšanas darba veidu.

7. Ja nepieciešams, atlasiet opcijas **Uzturēšanas darba tipa variants** un **Amats**.

8. Ja nepieciešams, jūs varat mainīt darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.

9. Attiecīgajos laukos atlasiet datumus **Paredzamais sākums** un **Paredzamās beigas**.

10. Noklikšķiniet uz **Labi**, lai izveidotu darba pasūtījumu.

11. Sarakstu lapā **Visi darba pasūtījumi** jūs varat labot darba pasūtījumu, kā nepieciešams.

Ņemiet vērā šādus punktus:

- Detalizētajā skatā **Visi darba pasūtījumi** sarakstu lapā jūs varat darba pasūtījumam pievienot vairākus līdzekļus, pievienojot rindas kopsavilkuma cilnē **Darba pasūtījuma uzturēšanas darbi**. Līdzeklī jūs varat atlasīt vienīgi tos uzturēšanas darbu tipus, kuri ir definēti līdzekļa veidā, kas ir atlasīts līdzeklī.  

- Ja maināt līdzekļa servisa līmeni vai līdzekļa kritiskumu pēc tam, kad esat to jau izmantojis līdzekli darba pasūtījumā, servisa līmenis vai kritiskums darba pasūtījumā netiek attiecīgi atjaunināts. Lai iegūtu papildinformāciju par servisa līmeņiem un kritiskumu, skatiet [Līdzekļu servisa līmeņi](../setup-for-objects/object-priorities.md) un [Līdzekļa kritiskuma veidi](../setup-for-objects/object-criticalities.md).

- Kritiskums darba pasūtījumā tiek pārrēķināts katru reizi, kad darba pasūtījuma darbs tiek pievienots vai dzēsts darba pasūtījumā.

- Detalizētajā skatā **Visi darba pasūtījumi** > cilnē **Galvene** > ātrajā cilnē **Grafiks** laukos **Atbildīgā grupa** vai **Atbildīgais** jūs varat atlasīt atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu. Šos iestatījumus var mainīt, kamēr darba pasūtījums ir aktīvs. Piemēram, tos var mainīt, ja mainās darba pasūtījuma dzīves cikla stāvoklis. Automātiskā atlase, kas ir veikts darba pasūtījuma izveides laikā, tiek balstīta uzstādījumā lapā **Atbildīgie uzturēšanas speciālisti**. Ja pievienojat vai dzēšat darba pasūtījuma darbus pēc tam, kad izveidojāt darba pasūtījumu, un ja lauki **Atbildīgo grupa** un **Atbildīgais** ir tukši, kad atjaunināt darba pasūtījumu, programma Līdzekļu pārvaldība mēģina atrast atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu iespējamai sakritībai uzstādīšanas veidlapā. Ja lauki **Atbildīgo grupa** vai **Atbildīgais** jau ir iestatīti, kad atjaunināt darba pasūtījumu, netiek veiktas nekādas izmaiņas. Papildinformāciju par atbildīgiem uzturēšanas speciālistiem un speciālistu grupām, skatiet nodaļā [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).

- Lapā [Uzturēšanas stāvoklis](../controlling-and-reporting/maintenance-status.md) jūs varat veikt aprēķinu par to, kā iegūt pārskatu par darba slodzi ienākošajiem un pabeigtajiem darba pasūtījumiem.  

- Lapas **Visi darba pasūtījumi** detalizētajā skatā, kopsavilkuma cilnē **Detalizētā informācija par rindu** jūs var izmantot laukus **Platums** un **Garums**, lai pievienotu ģeogrāfiskās koordinātes līdzeklim, kas atlasīts darba pasūtījuma darbā.  


## <a name="create-related-work-order"></a>Izveidot saistītu darba pasūtījumu

Jūs varat izveidot darba pasūtījumu, kas ir saistīts ar esošo darba pasūtījumu. Šī spēja ir noderīga, ja, piemēram, vēlaties strādāt ar primāriem un sekundāriem darba pasūtījumiem. Jauns darba pasūtījums ir balstīts darba pasūtījuma darbā no esoša darba pasūtījuma.

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**

2. Atlasiet darba pasūtījumu, lai tam izveidotu saistīto darba pasūtījumu.

3. Darbību rūtī cilnē **Darba pasūtījums** grupā **Jauns** atlasiet **Saistīts darba pasūtījums**.

4. Dialogā **Izveidot saistītu darba pasūtījumu** laukā **Darba pasūtījuma darbs** atlasiet darba pasūtījuma darbu, kuram vēlaties izveidot saistītu darba pasūtījumu.

5. Atlasiet uzturēšanas darba veidu laukā **Uzturēšanas darba veids**.

6. Laukos **Uzturēšanas darba tipa variants** un **Amats** atlasiet saistīto uzturēšanas darba veida variantu un amatu, kā nepieciešams.

7. Ja šis darba pasūtījums ir pirmais saistītais darba pasūtījums, kas tika izveidots atlasītajam darba pasūtījumam, rīkojieties šādi:
    1. Atlasiet **Jauns darba pasūtījums** opciju.
    2. Atlasiet darba pasūtījuma veidu laukā **Darba pasūtījuma veids**.
    3. Laukā **Apraksts** ievadiet aprakstu.
    4. Ja nepieciešams, laukā **Servisa līmenis** mainiet darba pasūtījuma servisa līmeni.
    5. Laukos **Paredzamais sākums** un **Paredzamas beigas** atlasiet paredzamos sākuma un beigu datumus.
    6. Atlasiet **Labi**. Jaunais saistītais darba pasūtījums tiek rādīts lapā **Visi darba pasūtījumi**.  

8. Ja darba pasūtījumam, kuram jūs veidojat šo saistīto darba pasūtījumu, jau ir saistīti darba pasūtījumi, veiciet tālāk norādītās darbības, lai pievienotu jaunu darba pasūtījuma darbu esošam saistītajam darba pasūtījumam:
    1. Atlasiet opciju **Pievienot saistītam darba pasūtījumam**.
    2. Laukā **Darba pasūtījums** atlasiet saistītu darba pasūtījumu, kuram vēlaties pievienot jaunu darba pasūtījuma darbu.
    3. Ja nepieciešams, laukā **Servisa līmenis** mainiet darba pasūtījuma servisa līmeni.
    4. Laukos **Paredzamais sākums** un **Paredzamas beigas** pēc nepieciešamības mainiet paredzamos sākuma un beigu datumus.
    5. Atlasiet **Labi**. Darba pasūtījuma darbs ir pievienots esošam saistītam darba pasūtījumam.

Attēlā tālāk ir parādīts sarakstu dialoga **Izveidot saistīto darba pasūtījumu** piemērs.

![1. attēls.](media/03-work-orders.png)

>[!NOTE]
>Ja iestatījāt saistītā darba pasūtījuma masku **Līdzekļa pārvaldības parametri** > **Darba pasūtījumi** cilne > **Saistīta darba pasūtījuma maska** lauks, darba pasūtījuma ID tiek izveidoti atbilstoši maskas uzstādījumam. Ja nav uzstādīta neviena saistīta darba pasūtījuma maska, saistītiem darba pasūtījumiem tiks izmantots nākamais pieejamais darba pasūtījuma ID

## <a name="copy-a-work-order"></a>Kopēt darba pasūtījumu.

Jūs varat ātri izveidot jaunu darba pasūtījumu no esoša darba pasūtījuma. Tādējādi darbs ar darba pasūtījumiem atšķiras no darba pasūtījumu izveides, kuri ir balstīti uz [uzturēšanas plāni](../preventive-and-reactive-maintenance/maintenance-plans.md). Tas ir noderīgi, ja, piemēram, darba pasūtījums satur daudzus darba pasūtījuma darbus un dažādiem darbiem jābūt pabeigtiem atšķirīgos līdzekļos regulāros intervālos.

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**

2. Atlasiet darba pasūtījumu, no kura kopēt saturu.

3. Darbību rūtī cilnē > **Darba pasūtījums** > grupā **Jauns** atlasiet **Kopēt darba pasūtījumu**.

4. Tiek parādīts darba pasūtījuma uzstādījums no atlasītā darba pasūtījuma. Ja nepieciešams, jūs varat rediģēt dažus laukus.

5. Atlasiet **Labi**, lai izveidotu jaunu darba pasūtījumu.

6. Sarakstu lapā **Visi darba pasūtījumi** jūs varat labot darba pasūtījumu, kā nepieciešams.

>[!NOTE]
>Kad ir izveidots jauns darba pasūtījums, daļa informācijas tiek kopēta tieši no esošā darba pasūtījuma. Informācija par prognozēm, rīkiem, uzturēšanas kontrolsarakstiem, funkcionālo novietojumu, adresēm un plānošanu netiek kopēta. Tā vietā tas tiek inicializēts no pašreizējiem Līdzekļu pārvaldības iestatījumiem. Tāpēc, ja šī informācija tika mainīta starp laiku, kad tika izveidots pirmais darba pasūtījums, un laiku, kad veicāt darba pasūtījuma kopiju, izmaiņas tiek iekļautas jaunajā darba pasūtījumā. Piemēri iekļauj izmaiņas prognozēs un uzturēšanas kontrolsarakstu atjauninājumus.

Attēlā zemāk ir parādīts dialoglodziņš **Kopēt darba pasūtījumu**.

![2. attēls.](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Izveidojiet darba pasūtījumu balstītu uz uzturēšanas pieprasījumu

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas pieprasījumi** > **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.

2. Atlasiet uzturēšanas pieprasījumu, kuram izveidot darba pasūtījumu, un noklikšķiniet uz **Rediģēt**.

3. Darbību rūtī cilnē > **Uzturēšanas pieprasījums** > grupā **Jauns** atlasiet **Darba pasūtījums**.

4. Dialogā **Darba pasūtījums** iestatiet laukus. Ja uzturēšanas darba veids ir atlasīts uzturēšanas pieprasījumā, jūs varat atlasīt citu uzturēšanas darba veidu, ja nepieciešams, kad izveidojat darba pasūtījumu.

5. Atlasiet **Labi**. Ziņojums jūs informē, ka ir izveidots darba pasūtījums.

6. Lai skatītu darba pasūtījumus, kas ir savienoti ar uzturēšanas pieprasījumu, atlasiet uzturēšanas pieprasījumu sarakstu lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvi uzturēšanas pieprasījumi**. Pēc tam darbību rūtī cilnē **Uzturēšanas pieprasījums** grupā **Skatīt** atlasiet **Darba pasūtījumi**.


Attēlā zemāk ir parādīts dialoglodziņš **Izveidot darba pasūtījumu**.

![3. attēls.](media/05-work-orders.png)


>[!NOTE]
>Ja jūs vēlāties, lai darba pasūtījumi izveidotos automātiski, jūs varat ieplānot uzturēšanas plāna darbus vai līdzeklī uzstādīt "Automātiskā izveide" [uzturēšanas plāni](../preventive-and-reactive-maintenance/maintenance-plans.md) vai [uzturēšanas cikli](../preventive-and-reactive-maintenance/maintenance-rounds.md). Darba pasūtījumiem, kas ir izveidoti no uzturēšanas pieprasījumiem sarakstu lapā **Viss uzturēšanas grafiks**, ir uzturēšanas darba veidi, kas ir atlasīti uzturēšanas pieprasījumos.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]