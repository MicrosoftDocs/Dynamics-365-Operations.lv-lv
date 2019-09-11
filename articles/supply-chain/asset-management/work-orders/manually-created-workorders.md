---
title: Manuāli izveidoti darba pasūtījumi
description: Šajā tēmā ir paskaidrots, kā manuāli izveidot darba pasūtījumus programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875776"
---
# <a name="manually-created-work-orders"></a>Manuāli izveidoti darba pasūtījumi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Ir divi veidi, kādos var manuāli izveidot darba pasūtījumus:

- sadaļā **Visi darba pasūtījumi** vai **Aktīvi darba pasūtījumi**  
- sadaļās **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**.  

## <a name="create-work-order"></a>Izveidot darba pasūtījumu

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Noklikšķiniet uz pogas **Jauns**.

3. nolaižamajā sarakstā **Izveidot darba pasūtījumu** atlasiet darba pasūtījuma tipu.

4. Ja nepieciešams, atlasiet aprakstu.

5. Atlasiet darba pasūtījumam līdzekli, kā arī uzturēšanas darba tipu.

>[!NOTE]
>Atlasot līdzekli, var būt pieejamas trīs cilnes: Cilne **Mani līdzekļi** satur līdzekļus, kas ir saistīti ar funkcionālo novietojumu, kurš jums (speciālistam, kurš ir pieteicies sistēmā) var būt piešķirts (uzstādīts [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md)). Ja speciālistam sadaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md) nav uzstādīts funkcionālais novietojums, cilne **Mani līdzekļi** nebūs redzama. Cilnē **Aktīvie līdzekļī** ir iekļauts visu līdzekļu saraksts ar līdzekļa dzīves cikla statusu "Aktīvs". Cilne **Līdzekļu skats** parāda funkcionālo novietojumu koku un šajos novietojumos uzstādītos līdzekļus.

6. Ja nepieciešams, atlasiet opcijas **Uzturēšanas darba tipa variants** un **Amats**.

7. Ja nepieciešams, jūs varat mainīt darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.

8. Attiecīgajos laukos atlasiet paredzamo sākumu un beigu datumu.

9. Noklikšķiniet uz **Labi**, lai izveidotu jaunu darba pasūtījumu.

10. Ja nepieciešams, rediģējiet darba pasūtījumu laukā **Visi darba pasūtījumi**.

- Laukā **Visi darba pasūtījumi** jūs varat darba pasūtījumam pievienot vairākus līdzekļus Detalizētajā skatā, pievienojot rindas kopsavilkuma cilnē **Darba pasūtījuma uzturēšanas darbi**.  Līdzeklī jūs varat atlasīt vienīgi tos uzturēšanas darbu tipus, kuri ir definēti līdzeklim atlasītajā līdzekļa tipā.  
- Ja esat mainījis līdzekļa servisa līmeni vai līdzekļa kritiskos faktorus pēc tam, kad tie izmantoti darba pasūtījumā (skatīt [Līdzekļa servisa līmeņi](../setup-for-objects/object-priorities.md) un [Līdzekļu kritiskie faktori](../setup-for-objects/object-criticalities.md)), servisa līmenis vai kritiskie faktori darba pasūtījumā netiek atjaunināti.
- Darba pasūtījuma kritiskie faktori tiek atkārtoti aprēķināti katru reizi, kad darba pasūtījuma rinda tiek pievienota darba pasūtījumam vai dzēsta no tā.
- Detalizētajā skatā **Visi darba pasūtījumi** > skatā **Galvene** > ātrajā cilnē grafiks **Schedule** jūs varat atlasīt atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu laukos **Atbildīgā grupa** vai **Atbildīgais**. Šos uzstādījumus var mainīt, kamēr vien darba pasūtījums ir aktīvs, piemēram, ja mainās darba pasūtījuma dzīves cikla stāvoklis. Automātiskā atlase, kas veikts darba pasūtījuma izveides laikā, tiek balstīta uzstādījumā sadaļā **Atbildīgie uzturēšanas speciālisti**. Ja pievienojat vai dzēšat darba pasūtījuma darbus pēc tam, kad izveidojāt darba pasūtījumu, un lauki **Atbildīgo grupa** un **Atbildīgais** ir tukši, kad atjaunināt darba pasūtījumu, programma Asset Management meklē iespējamo atbildīgu uzstādīšanas veidlapā atbildīgajai uzturēšanas speciālistu grupai vai atbildīgajam uzturēšanas speciālistam. Ja lauki **Atbildīgo grupa** vai **Atbildīgais** jau ir aizpildīti, kad atjaunināt darba pasūtījumu, netiek veiktas nekādas izmaiņas. 

- Sadaļā **Uzturēšanas stāvoklis** jūs varat veikt aprēķinu par to, kā iegūt pārskatu par darba slodzi attiecībā uz ienākošajiem un pabeigtajiem darba pasūtījumiem.   

- Ātrajā cilnē **Rindas detalizēta informācija**, izmantojiet laukus **Platums** un **Garums**, lai pievienotu ģeogrāfiskās koordinātas līdzeklim, kas atlasīts darba pasūtījuma darbā.  

## <a name="create-related-work-order"></a>Izveidot saistītu darba pasūtījumu

Jūs varat izveidot saistītu darba pasūtījumu esošam darba pasūtījumam, ja, piemēram, vēlaties strādāt ar primāriem un sekundāriem darba pasūtījumiem. Jauns darba pasūtījums ir balstīts darba pasūtījuma darbā no esoša darba pasūtījuma.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu, kuram vēlaties izveidot saistītu darba pasūtījumu.

3. Noklikšķiniet uz **Saistīts darba pasūtījums**.

4. Nolaižamajā dialogā **Izveidot saistītu darba pasūtījumu** atlasiet darba pasūtījuma darbu, kuram vēlaties izveidot saistītu darba pasūtījumu laukā **Darba pasūtījuma darbs**.

5. Laukā **Uzturēšanas darba tips** atlasiet uzturēšanas darba tipu un, ja nepieciešams, saistītā uzturēšanas darba tipa variantu un amatu laukos **Uzturēšanas darba tipa variants** un **Amats**.

6. Ja šis ir pirmais saistītais darba pasūtījums, ko veicat, noklikšķiniet uz radiopogas **Jauns darba pasūtījums**.

7. Atbilstošajos laukos atlasiet opcijas **Darba pasūtījuma tips** un **Apraksts**.

8. Ja nepieciešams, mainiet darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.

9. Atbilstošajos laukos ievadiet paredzamos sākuma un beigu datumus.

10. Noklikšķiniet uz **Labi**. Jaunais saistītais darba pasūtījums tiek rādīts sarakstā **Visi darba pasūtījumi**.

11. Ja jūs izveidojat saistītu darba pasūtījumu darba pasūtījumam, kuram jau ir saistīti darba pasūtījumi, jūs varat pievienot darba pasūtījumu jau saistītam darba pasūtījumam. Tas tiek izdarīts, 6. darbībā noklikšķinot radiopogu **Pievienot saistītam darba pasūtījumam**. Pēc tam jūs atlasāt saistītu darba pasūtījumu, kuram vēlaties pievienot jaunu darba pasūtījuma darbu. Pēc nepieciešamības rediģējiet laukus **Servisa līmenis**, **Paredzamais sākums** un **Paredzamās beigas** un noklikšķiniet uz **Labi**. Darba pasūtījuma darbs ir pievienots esošam saistītam darba pasūtījumam.


![1. attēls](media/03-work-orders.png)

**Piezīme:** Ja iestatījāt saistītā darba pasūtījuma masku, dodoties uz **Līdzekļa pārvaldības parametri** > **Darba pasūtījumi** saite > lauks **Saistīta darba pasūtījuma maska**, darba pasūtījuma ID tiks izveidoti atbilstoši maskas uzstādījumam. Ja nav uzstādīta neviena saistīta darba pasūtījuma maska, saistītiem darba pasūtījumiem tiks izmantots nākamais pieejamais darba pasūtījuma ID.

## <a name="copy-work-order"></a>Kopēt darba pasūtījumu

Ir iespējams ātri izveidot jaunu darba pasūtījumu no esoša darba pasūtījuma. Tādējādi darbs ar darba pasūtījumiem atšķiras no darba pasūtījumu izveides, kuri ir balstīti uzturēšanas plānos. Tas ir noderīgi, ja jums ir, piemēram, darba pasūtījums, kas satur daudzus darba pasūtījuma darbus ar dažādiem darbiem atšķirīgiem līdzekļiem, kurus vajadzētu pabeigt regulāros intervālos.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu, no kura vēlaties kopēt saturu.

3. Noklikšķiniet uz **Kopēt darba pasūtījumu**. Tiek parādīts darba pasūtījuma uzstādījums no atlasītā darba pasūtījuma. Ja nepieciešams, jūs varat dažus laukus rediģēt.

4. Noklikšķiniet uz **Labi**, lai izveidotu jaunu darba pasūtījumu.

5. Ja nepieciešams, rediģējiet darba pasūtījumu laukā **Visi darba pasūtījumi**.

>[!NOTE]
>Kad ir izveidots jauns darba pasūtījums, daļa informācijas tiek kopēta tieši no esošā darba pasūtījuma. Informācija, kas attiecas uz prognozēm, rīkiem, uzturēšanas kontrolsarakstiem, funkcionālo novietojumu, adresēm un plānošanu, netiek kopēta, bet tiek inicializēta no pašreizējā uzstādījuma programmā Asset Management. Tādējādi, ja šajos datos tika veiktas izmaiņas laikā no pirmā darba pasūtījuma izveides datuma līdz darba pasūtījuma kopēšanas laikam, šīs izmaiņas tiek iekļautas jaunajā darba pasūtījumā, kuru izveidojāt. Piemēri ir izmaiņas prognozēs vai atjauninātos uzturēšanas kontrolsarakstos.


![2. attēls](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Izveidojiet uzturēšanas pieprasījumā balstītu darba pasūtījumu

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas pieprasījumi** > **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.

2. Atlasiet uzturēšanas pieprasījumu, kuram vēlaties izveidot darba pasūtījumu, un noklikšķiniet uz **Rediģēt**.

3. Laukā **Visi pieprasījumi** noklikšķiniet uz **Darba pasūtījums**.

4. Aizpildiet nolaižamo lauku **Darba pasūtījums**. Ja uzturēšanas darba tips ir atlasīts uzturēšanas pieprasījumā, jūs varat atlasīt citu uzturēšanas darba tipu, ja nepieciešams, kad izveidojat darba pasūtījumu.

5. Noklikšķiniet uz **Labi**. Tiks parādīts ziņojums, ka darba pasūtījums ir izveidots.

6. Ja vēlaties redzēt, kuri darba pasūtījumi ir savienoti ar uzturēšanas pieprasījumu, atlasiet uzturēšanas pieprasījumu sarakstos **Visi uzturēšanas pieprasījumi** vai **Aktīvi uzturēšanas pieprasījumi** un noklikšķiniet uz pogas **Darba pasūtījumi**.


![3. attēls](media/05-work-orders.png)


>[!NOTE]
>Darba pasūtījumus var arī izveidot automātiski, ieplānojot uzturēšanas plāna darbus vai līdzeklī uzstādot "Automātiskās izveides" uzturēšanas plānus vai uzturēšanas ciklus. Darba pasūtījumi, kas izveidoti no uzturēšanas pieprasījumiem opcijā **Uzturēšanas grafiks**, tiek izveidoti ar uzturēšanas darba tipiem, kas atlasīti uzturēšanas pieprasījumos. 

