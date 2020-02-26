---
title: Jauns dokumentu lietotāja interfeiss biznesa dokumentu pārvaldībā
description: Šajā tēmā ir sniegta informācija par to, kā izmantot jauno dokumentu lietotāja interfeisu (UI) elektroniskā pārskata (ER) struktūras biznesa dokumentu pārvaldības līdzeklī.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957067"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Jauns dokumentu lietotāja interfeiss biznesa dokumentu pārvaldībā

[!include [banner](../includes/banner.md)]

Biznesa dokumentu pārvaldība ļauj iznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft Office 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu. Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu. Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).

Jaunais dokumentu lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams. **Biznesa dokumenta** apgabals parāda tikai tās veidnes, kas ir pieejamas pašreizējam nodrošinātājam.

Poga **Jauns dokuments** ļauj lietotājiem izveidot un rediģēt veidni elektroniskā pārskata (ER) formāta konfigurācijā, kas pieder citam nodrošinātājam. Šīs tēmas piemērā nodrošinātājs ir Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā

Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.

Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.

1. Darbvietas **Lïdzekĺu pārvaldība** cilnē **Jauns** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.
2. Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.
3. Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Citiem nodrošinātājiem piederošu veidņu rediģēšana

1. Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)

2. Dialoglodziņā atlasiet dokumentu, kas jālieto kā veidne, un pēc tam atlasiet **Izveidot dokumentu**.

    ![Dialoglodziņš biznesa dokumenti](./media/BDM_overview_new_template2.png)

3. Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams. Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam. Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam. Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.
4. Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.
5. Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.
6. Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.

    ![Dialoglodziņš Dokumenta izveide](./media/BDM_overview_new_template3.png)

Pogu **Jauns dokuments** lieto, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, kas pieder citam nodrošinātājam. Šajā piemērā nodrošinātājs ir Microsoft. Atlasot **Jauns dokuments**, jūs varat rezēt visas veidnes, kas pieder pašreizējiem un citiem nodrošinātājiem. Pēc veidnes atlasīšanas tā ir atvērta rediģēšanai. Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.

Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).
