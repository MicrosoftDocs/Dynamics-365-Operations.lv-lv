---
title: Elektronisko pārskatu konfigurāciju koplietošana RCS/globālā repozitorija ar ārējām organizācijām
description: Šajā rakstā skaidrots, kā koplietot elektronisko pārskatu (ER) konfigurācijas Microsoft regulēšanas konfigurācijas pakalpojumos (RCS)/globālajā repozitorijā tieši ar ārējām organizācijām.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 976a86aee75581d1afa764bea049b6c0eaecf9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888928"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Koplietot elektronisko pārskatu (ER) konfigurācijas Regulatory Configuration Services (RCS) globālā repozitorijā tieši ar ārējām organizācijām

[!include [banner](../includes/banner.md)]

Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai koplietotu elektroniskos pārskatu (ER) konfigurācijas un pēc tam publicētu tās ārējām organizācijām.

Tālāk sniegtajos procedūru aprakstos ir paskaidrots kā RCS lietotājs var dalīties ar ER konfigurācijas versiju, kas ir konfigurēta kā RCS instance ar ārēju organizāciju. Lai varētu veikt šīs procedūras, ir jāizpilda šādi priekšnosacījumi:

- Piekļūstiet RCS instancei.
- Izveidojiet aktīvu konfigurācijas nodrošinātāju. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Izveidojiet un augšupielādējiet jaunu ER konfigurācijas versiju. Papildinformāciju skatiet šeit: [Jauna elektroniskā pārskata (ER) konfigurācijas versijas izveide un augšupielāde](rcs-global-repo-upload.md).

Jums ir arī jāpārliecinās, ka RCS vide ir nodrošināta jūsu uzņēmumam.

1. Finanšu un operāciju programmā dodieties uz organizācijas administrēšanas **darbalauku** \> **elektronisko** \> **pārskatu sniegšanu**.
2. Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration external** un pēc tam izpildiet norādījumus, lai tādu nodrošinātu.

Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu tai, atlasot pierakstīšanās opciju.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Pārbaudiet konfigurāciju, ko vēlaties koplietot

Sekojiet šiem soļiem, lai pārbaudītu, vai konfigurācija, kuru vēlaties koplietot, jau ir augšupielādēta globālajā repozitorijā.

1. **Elektroniskā pārskata** darbvietā atlasiet **Repozitoriji** jūsu konfigurācijas nodrošinātājam.

    ![Konfigurācijas nodrošinātāji.](media/1_RCS_Repo_for_config_provider.JPG)

2. Atlasiet **Globālais repozitorijs** \> **Atvērt**.
3. Meklējiet konfigurāciju, ko vēlaties koplietot. Varat izmantot filtra lauku, lai sašaurinātu meklēšanu. Ja jūs nevarat atrast konfigurāciju globālajā repozitorijā, sekojiet soļiem, lai [izveidotu un augšupielādētu jaunu elektronisko pārskatu (ER) konfigurācijas versiju](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>ER konfigurāciju koplietošana ar ārējām organizācijām

Kad konfigurācijas nodrošinātājs ir izveidojis konfigurāciju, to var tieši koplietot ar ārējām organizācijām, izmantojot **Kopīgots ar** kopsavilkuma lapā **globālās konfigurācijas repozitorijs**.

1. **Elektroniskā pārskata** darbvietā atlasiet **Repozitoriji** jūsu konfigurācijas nodrošinātājam.
2. Atlasiet **Globālais repozitorijs** \> **Atvērt**. 
3. Atlasiet konfigurāciju, ko vēlaties koplietot.
4. Kopsavilkuma cilnē **Kopīgots ar** atlasiet **Organizācija**.

    ![Koplietots izmantojot kopsavilkuma cilni.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Dialoglodziņā ievadiet ārējās organizācijas domēna nosaukumu un pēc tam atlasiet **Labi**.

    ![Koplietošanas konfigurācijas versija ar ārējo organizācijas dialoglodziņu.](media/1_RCS_Repo_for_Share_with_form.JPG)

Konfigurācija tiek koplietota ar ārējo organizāciju un ir pieejama šai organizācijai globālajā repozitorijā. No turienes to var importēt organizācijas RCS instancē vai tā finanšu un operāciju programmu instancēs.

6. Lai atceltu konfigurāciju, kas iepriekš bijusi koplietota ar ārēju organizāciju, atlasiet konfigurāciju un noklikšķiniet uz **pārtraukt koplietošanu** un pēc tam atlasiet **Labi**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]