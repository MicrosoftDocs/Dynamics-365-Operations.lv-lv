---
title: Kopuma darbību kodi
description: Šajā tēmā sniegts kopuma darbību kodu apskats, un kā tie tiek izmantoti.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992361"
---
# <a name="wave-step-codes"></a>Kopuma darbību kodi

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Par kopuma darbību kodiem

Kopuma darbību kodi ir kodi, ko lietotāji var iestatīt un izmantot, lai saistītu konkrētas kopuma metodes atbilstošajai veidnei. Veidnēs ir ietvertas papildināšanas, konteinerizēšanas, etiķešu drukāšanas, noslodzes veidošanas un kārtošanas veidnes.

Kad netiek lietoti kopuma darbību kodi, lietotājiem jāievada brīvs teksts, lai atsauktos uz noteiktu veidni no kopuma metodes instances. Brīvajam tekstam ir nosliece uz kļūdu, jo lietotājiem ir jāpārliecinās, vai kopuma darbību teksts, ko lietotāji pievieno noteiktai kopuma darbību metodei kopuma veidnē, tieši atbilst kopuma darbību tekstam mērķa veidnē.

Kopuma darbību kodi noteiktam kopuma darbību tipam ir iestatīti atsevišķā lapā. Katrai kopuma darbību metodes instancei kopuma veidnē, kas pieprasa kopuma darbību kodu, nolaižamajā sarakstā jābūt atlasītam kopuma darbību kodam. Atlase nolaižamajā sarakstā aizstāj brīvā teksta ievadi un palīdz samazināt cilvēka kļūdas risku un ietekmi. Iestatīšanas kodus lieto, lai veidotu saiti uz kopuma darbību metodi kopuma veidnē uz metodi mērķa veidnē.

> [!NOTE]
> Kopuma soļu kodu funkcijas lietošana ir neobligāta, un uzņemšana ir uz juridisku personu. Tādēļ, ja noteikta juridiska persona izmanto šo funkciju, visi esošie kopuma darbību kodi šai juridiskajai personai tiek jaunināti uz jauno struktūru.

## <a name="setup-demo"></a>Iestatīt demonstrāciju 

Šai demonstrācijai ir jābūt instalētiem demo datiem, un jums ir jāizmanto **USMF** demo datu uzņēmums.

### <a name="enable-wave-step-codes"></a>Iespējot kopuma darbību kodus

Sekojiet šiem soļiem, lai ieslēgtu kopuma darbību kodu līdzekli.

1. Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.
2. Cilnē **Vispārīgi** **Kopuma apstiprināšana** kopsavilkuma cilnē iestatiet opciju **Iespējot kopumu kodus** vērtību uz **Jā**.

Visi esošie kopuma darbību brīvie teksti tiek jaunināti uz jauno struktūru. Pēc tam, kad šis jauninājums ir izpildīts juridiskai personai, opcija **Iespējot kopuma darbību kodus** vairs nav pieejama **Noliktavas pārvaldības parametru** lapā.

Pārbaudes tiek veiktas jaunināšanas laikā, un, ja jaunināšana neizdodas, saņemsiet kļūdas ziņojumu. Jaunināšana var neizdoties, jo pastāv šādi konflikti:

- Pastāv kopuma darbību brīvā teksta dublikāts.
- Pastāv pielāgojumi.
- Kopuma darbību brīvais teksts, kas ir saistīts ar metodes instanci, neatbilst paredzētajam veidnes tipam.

Pēc tam, kad esat atrisinājis konfliktus, kas ir identificēti pārbaudes laikā, varat palaist jaunināšanas procesu.

Kad jaunināšana ir sekmīga, **Kopuma darbību kodu** lapa (**Noliktavas pārvaldība\>Iestatīšana \>Kopumi \>Kopuma darbību kodi**) kļūst pieejama. Šajā lapā ir uzskaitīti kopuma darbību kodi, kas tika atjaunināti, kad kopuma darbību kodu līdzeklis tika ieslēgts.

### <a name="create-new-wave-step-codes"></a>Izveidot jauna kopuma darbību kodus

Varat izmantot lapu **Kopuma darbību kodi**, lai izveidotu un dzēstu kopuma darbību kodus.

Katram jaunam kopuma darbību kodam un ar to saistītajam ID ir jābūt unikālam visos kopuma darbību tipos, un tie ir jādefinē konkrētam kopuma darbību tipam.

### <a name="apply-wave-step-codes"></a>Pielietot kopuma darbību kodus

Pēc tam, kad esat definējis piemērotus kopuma darbību kodus, tos var lietot kopuma procesa metodēm.

Lai pielietotu kopuma darbību kodus, dodieties uz atbilstošo mērķa veidni. Šeit ir mērķa veidnes, kam kopuma darbību kodi ir izveidoti, lai norādītu uz:

- **Papildināšanas veidnes.:** Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes
- **Noslodzes būvējuma veidnes:** Noliktavas pārvaldība \>Iestatīšana \>noslodzes kompilācijas veidnes \> 
- **Kārtot veidnes:** Noliktavas pārvaldība \>Iestatīšana \>Iepakošana \>Nosūtīšanas kārtošanas veidnes
- **Konteinerizēšanas veidnes:** Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru būvējuma veidnes
- **Etiķešu drukāšanas veidnes:** Noliktavas pārvaldība \>Uzstādīšana \>Dokumenta maršrutēšana \>Kopuma etiķešu veidnes

Šajā sarakstā iekļautās veidnes tiek piemērotas, kad tās ir norādītas no kopuma procesa metodes, kas ir atlasītas kopuma veidnēs. Kad kopuma darbību kods procesa metodē kopuma veidnē atbilst tā darbību kodam vienā no veidņu tipiem, tiek lietota veidne.

### <a name="sample-scenario"></a>Piemēra situācija

Šī procedūra palīdz garantēt, ka izveidotā papildināšanas veidne tiks lietota kopuma veidnei.

1. Dodieties uz **Noliktavas pārvaldība \>Iestatīšana \>Kopumi \>Kopuma darbību kodi** un izveidojiet kopuma darbību kodu **Papildināšanas** tipam.
2. Dodieties uz **Noliktavu pārvaldība\> Iestatīšana \> Papildināšana \> Papildināšanas veidnes** un izveidojiet papildināšanas veidni.
3. Papildināšanas veidnē atlasiet kopuma darbības kodu, ko izveidojāt **Papildināšanas** tipam.
4. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \>Kopumi \>Kopuma veidnes** un atlasiet kopuma veidni, ko plānojat izmantot.
5. Veidnē kopsavilkuma cilnē **Metodes** atlasiet **Papildināšanas** metodi.
6. Laukā **Kopuma darbības kodi** atlasiet kopuma darbības kodu, ko izvēlējāties papildināšanas veidnē.
