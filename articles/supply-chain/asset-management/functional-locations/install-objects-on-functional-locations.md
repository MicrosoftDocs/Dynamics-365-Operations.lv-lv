---
title: Līdzekļu uzstādīšana funkcionālajos novietojumos
description: Šajā tēmā izskaidrots, kā uzstādīt līdzekļus funkcionālajos novietojumos Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8619c6cde484c41ec01e96eb4626366f1955b5d4
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811830"
---
# <a name="install-assets-on-functional-locations"></a>Līdzekļu uzstādīšana funkcionālajos novietojumos

[!include [banner](../../includes/banner.md)]

 

Pēc funkcionālo novietojumu struktūru izveidošanas nākamā darbība ir uzstādīt līdzekļus attiecīgajos funkcionālajos novietojumos. Šajā tēmā izskaidrots, kā uzstādīt līdzekļus šajos funkcionālajos novietojumos Līdzekļu pārvaldībā. Papildinformāciju par līdzekļu izveidi skatiet sadaļā [Ievads līdzekļos](../objects/introduction-to-objects.md).

Ja esat izveidojis līdzekļu struktūru, visai līdzekļu struktūrai jābūt instalētai funkcionālajā novietojumā. Tāpēc funkcionālajā novietojumā var atlasīt tikai primāros līdzekļus (augstākā līmeņa līdzekļus, kuriem nav primārā līdzekļa). Arī visi saistītie sekundārie līdzekļi (pakārtotie aktīvi) tiks instalēti funkcionālajā novietojumā. Kad esat uzstādījis līdzekļus funkcionālajā novietojumā, funkcionālā novietojuma finanšu dimensijas var tikt automātiski pārsūtītas uz tiem atkarībā no iestatījumiem funkcionālā novietojuma veidā, kas ir atlasīts funkcionālajam novietojumam. Papildinformāciju par funkcionālo novietojumu veidu iestatīšanu skatiet sadaļā [Funkcionālo novietojumu veidi](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Līdzekļu veidus var iestatīt funkcionālā novietojuma veidā, kas tiek izmantots funkcionālajam novietojumam. Šajā gadījumā, instalējot līdzekļus funkcionālajā novietojumā, tikai primārie līdzekļi, kam ir tāds pats līdzekļa veids, tiek rādīti to līdzekļu sarakstā, kurus var uzstādīt funkcionālajā novietojumā.

Kad esat uzstādījis līdzekļus funkcionālajā novietojumā, pēc vajadzības varat aizstāt primāro līdzekli vai līdzekļu struktūru. Tāpat kā uzstādot līdzekļus, ir jāatlasa primārais līdzeklis, kuru aizstāt. Tiks aizstāti arī visi saistītie pakārtotie līdzekļi. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Līdzekļu struktūras uzstādīšana funkcionālajā novietojumā

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Funkcionālie novietojumi** \> **Visi funkcionālie novietojumi** vai **Aktīvie funkcionālie novietojumi**.
2. Atlasiet funkcionālo novietojumu, kurā uzstādīt līdzekli.
3. Atlasiet **Uzstādīt līdzekli**.

    Sadaļā **Atribūti** tiek parādīts saraksts ar līdzekļu atribūtu prasībām, kas ir iestatītas funkcionālā novietojuma veidam, kurš atlasīts funkcionālajam novietojumam. Atribūti paredzēti tikai informatīviem nolūkiem. Sistēma nevalidē atribūtus attiecībā uz līdzekļu atribūtiem, kas iestatīti līdzeklim, kuru uzstādāt. Šī validācija ir jāveic pēc tam, kad esat atlasījis līdzekli laukā **Līdzeklis**.

4. Laukā **Līdzeklis** atlasiet primāro līdzekli, kas jāuzstāda. Visi saistītie pakārtotie līdzekļi tiek automātiski iekļauti instalācijā.

    Sadaļā **Līdzekļu atribūti** pa labi no līdzekļa saraksta ir parādīti līdzekļu atribūti, kas ir saistīti ar atlasīto līdzekli.

5. Laukā **Ir spēkā** atlasiet datumu un laiku, no kura līdzekļa uzstādīšana ir spēkā. Pēc minētā datuma un laika līdzekļa un saistīto pakārtoto līdzekļu izmaksas tiks saistītas ar funkcionālo novietojumu.

    > [!NOTE]
    > Līdzekļa atribūti, kas iestatīti līdzeklim, tiek pievienoti sadaļai **Atribūti**. Piemēram, atribūta prasība **Svars** ir pievienota kā prasība gan līdzeklim, gan funkcionālajam novietojumam. Ja līdzeklim ir tāda paša veida atribūtu prasības kā funkcionālajam novietojumam, līdzekļa atribūtu prasību vērtības tiek ievadītas laukos **Vērtība**. Tāpēc varat validēt līdzekļa vērtības attiecībā uz atribūtu prasībām, kas ir iestatītas funkcionālajā novietojumā. Funkcionālajā novietojumā iestatētās atribūtu prasības ir marķētas ar atzīmi.

6. Atlasiet **Labi**.

    > [!NOTE]
    > Lai mainītu līdzekļa instalāciju, uzstādot to jaunā funkcionālā novietojumā, izpildiet šīs procedūras 1. – 6. darbību. Kad esat uzstādījis līdzekli jaunā funkcionālā novietojumā, līdzeklis tiek automātiski atinstalēts no iepriekšējā funkcionālā novietojuma. Visi aktīvie uzturēšanas pieprasījumi vai darba pasūtījumi, kas izveidoti līdzeklim pirms tā uzstādīšanas jaunā funkcionālajā novietojumā, **Netiek** automātiski pārsūtīti uz jauno funkcionālo novietojumu. Ja šie uzturēšanas pieprasījumi un darba pasūtījumi joprojām ir nepieciešami pamatlīdzeklim, tie ir atkārtoti jāizveido manuāli pēc tam, kad līdzeklis ir uzstādīts jaunajā atrašanās vietā.

7. Lai skatītu sarakstu ar visiem līdzekļiem, tostarp pakārtotajiem līdzekļiem, kas ir uzstādīti funkcionālajā novietojumā, atlasiet funkcionālo novietojumu lapā **Visi funkcionālie ovietojumi** un pēc tam atlasiet vienumu **Līdzekļi**.
8. Lai skatītu sarakstu ar aktīvajiem uzturēšanas pieprasījumiem, aktīvajiem darba pasūtījumiem vai defektu reģistrācijām, kas ir saistītas funkcionālajā novietojumā uzstādītajiem līdzekļiem, atlasiet funkcionālo novietojumu lapā **Visi funkcionālie novietojumi** un pēc tam atlasiet **Pieprasījumi**, **Darba pasūtījumi** vai **Defekti**.

> [!NOTE]
> Mainot ar līdzekļiem saistītus datus, tie automātiski tiek atjaunināti funkcionālajā novietojumā, kurā uzstādīts līdzeklis. Šī automātiskā atjaunināšana attiecas uz izmaiņām uzturēšanas pieprasījumos, darba pasūtījumos, līdzekļu defektu reģistrācijās, dīkstāve uzturēšanas dēļ reģistrācijās un līdzekļu mēru reģistrācijās.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Automātiska viena līdzekļa izveide funkcionālajā novietojumā

Varat iestatīt funkcionālā novietojuma stadijas un funkcionālā novietojuma veidus, lai apstrādātu automātisku *viena* līdzekļa izveidi funkcionālajā novietojumā. Līdzeklis iegūst tādu pašu ID un nosaukumu kā funkcionālais novietojums. Šī funkcionalitāte var būt noderīga, ja apkalpojat uzturēšanu lielam, statiskam līdzeklim, piemēram, ēkai.

Pirms varat automātiski izveidot līdzekli funkcionālajā novietojumā, jābūt pieejamiem šādiem iestatījumu datiem:

- Izveidojiet funkcionālā novietojuma veidu, lai apstrādātu automātisku līdzekļa izveidi. Laukā **Līdzekļa veids** atlasiet līdzekļa veidu. Papildinformāciju skatiet sadaļā [Funkcionālo novietojumu veidi](../setup-for-functional-locations/functional-location-types.md).
- Izveidojiet funkcionālā novietojuma dzīves cikla stāvokli, lai apstrādātu automātisku līdzekļa izveidi. Iestatiet opciju **Izveidot līdzekli** uz **Jā**. Papildinformāciju skatiet sadaļā [Funkcionālo novietojumu dzīves cikla stāvokļi](../setup-for-functional-locations/functional-location-stages.md).

Kad iestatīšanas dati ir pieejami, varat izveidot līdzekli.

1. Lapā **Visi funkcionālie novietojumi** pārliecinieties, vai vēlamais funkcionālais novietojums, kurā līdzeklis tiks izveidots automātiski, izmanto šim nolūkam izveidoto funkcionālā novietojuma veidu.
2. Sarakstā atlasiet funkcionālo novietojumu.
3. Atlasiet **Atjaunināt funkcionālā novietojuma stāvokli** un pēc tam atlasiet dzīves cikla stāvokli, kuru izveidojāt šim nolūkam. Tagad funkcionālajā novietojumā tiek automātiski uzstādīts viens līdzeklis. Šim līdzeklim ir tāds pats nosaukums kā funkcionālajam novietojumam.
