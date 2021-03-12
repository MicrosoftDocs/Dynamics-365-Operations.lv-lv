---
title: Elektronisko pārskatu konfigurāciju izveide pakalpojumā RCS un to augšupielāde globālajā repozitorijā
description: Šajā tēmā skaidrots, kā izveidot elektronisko pārskatu (ER) konfigurāciju Microsoft Regulatory Configuration Services (RCS) un augšupielādēt to globālajā repozitorijā.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: ef12c911c8953b181db1c0eff0874a3d8cfcb3da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005752"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER konfigurāciju izveide Regulatory Configuration Services (RCS) un to augšupielāde globālajā repozitorijā

[!include [banner](../includes/banner.md)]

Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai veidotu elektroniska pārskata (ER) konfigurācijas un publicētu tās, lai tās varētu izmantot jūsu organizācija.

Tālāk aprakstītajās procedūrās ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot atvasinātu Elektroniskā pārskata (EK) versiju, kas ir konfigurēta RCS instancē, un pēc tam augšupielādēt atvasināto konfigurāciju globālajā repozitorijā. 

Lai varētu veikt šīs procedūras, ir jāizpilda šādi priekšnosacījumi:

- Piekļūstiet RCS instancei.
- Izveidojiet aktīvu konfigurācijas nodrošinātāju. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Jums ir arī jāpārliecinās, ka RCS vide ir nodrošināta jūsu uzņēmumam.

1. Programmā Finance and Operations dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektroniskie pārskat**.
2. Ja jūsu uzņēmumā nav nodrošināta neviena RCS vide, atlasiet **Regulatory services — Configuration external** un pēc tam izpildiet norādījumus, lai tādu nodrošinātu.

Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapas vietrādi URL, lai piekļūtu tai, atlasot pierakstīšanās opciju.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Izveidot atvasinātu konfigurācijas versiju RCS

1. Darbvietas **Elektroniskajā pārskatā** pārbaudiet, vai jūsu organizācijai ir aktīvs konfigurācijas nodrošinātājs. 
2. Atlasiet **Pārskatu konfigurācijas**.
3. Atlasiet konfigurāciju, no kuras vēlaties atvasināt jauno versiju. Varat izmantot filtra lauku virs koka skata, lai sašaurinātu meklēšanu.
4. Atlasiet **Izveidot konfigurāciju** \> **Atvasināt no nosaukuma**.
5. Ievadiet nosaukumu un aprakstu un pēc tam atlasiet **Izveidot konfigurāciju**, lai izveidotu jaunu atvasinātu versiju.
6. Atlasiet tikko atvasināto konfigurāciju, pievienojiet versijas aprakstu un pēc tam atlasiet **Labi**. Konfigurācijas statuss ir nomainīts uz **Pabeigts**.

![Jauna konfigurācijas versija RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kad konfigurācijas statuss ir mainīts, var tikt parādīts pārbaudes kļūdas ziņojums, kas saistīts ar savienotajām lietojumprogrammām. Lai izslēgtu pārbaudi, cilnes **Konfigurācijas** darbību rūtī atlasiet **Lietotāja parametri** un pēc tam opciju **Izlaist validāciju konfigurācijas statusa maiņai un pārbāzei** iestatītu uz **Jā** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfigurācijas augšupielāde globālajā repozitorijā

Lai koplietotu jaunu vai atvasinātu konfigurāciju ar savu organizāciju, varat to augšupielādēt globālajā repozitorijā.

1. Atlasiet konfigurācijas pabeigtu versiju un pēc tam atlasiet **Augšupielādēt repozitorijā**.
2. Atlasiet opciju **Globāli (Microsoft)** un pēc tam atlasiet **Augšupielādēt**.

    ![Augšupielādēt repozitorija opcijās](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**. 
4. Atjauniniet versijas aprakstu pēc nepieciešamības un pēc tam atlasiet **Labi**. 

Konfigurācijas statuss ir atjaunināts uz **Kopīgot**, un konfigurācija ir augšupielādēta globālajā repozitorijā. No turienes ar to var strādāt šādos veidos:

- Importējiet to savā Dynamics 365 instancē. Papildinformāciju skatiet [(ER) Konfigurāciju importēšana no RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Koplietot to ar trešo pusi vai ārēju organizāciju, skatiet [RCS Koplietot elektronisko pārskatu (ER) konfigurācijas ar ārējām organizācijām](rcs-global-repo-share-configuration.md)

    ![Atvasinātā Intrastat Contoso konfigurācijas versija globālajā krātuvē](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Konfigurācijas dzēšana no globālā repozitorija
Lai dzēstu jūsu organizācijas izveidoto konfigurāciju, veiciet tālāk norādītās darbības.

1. **Elektroniskā pārskata** darbvietā pārbaudiet, vai jūsu konfigurācijas nodrošinātājs ir **Aktīvs**. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Aktīvajam konfigurācijas nodrošinātājam atlasiet **repozitoriju**.
3. Atlasiet repozitorija veidu **Globāls** un atlasiet **Atvērt**.
4. Kopsavilkuma cilnē **Filtrs** atrodiet konfigurāciju, ko vēlaties dzēst, izmantojot funkciju **Filtrs**.
5. Kopsavilkuma cilnē **Versija** atlasiet konfigurācijas versiju, ko vēlaties dzēst, un pēc tam atlasiet **Dzēst**:

    ![Konfigurācijas dzēšana no globālā repozitorija](media/RCS_Delete_from_GlobalRepo.JPG)

6. Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**.

    ![Konfigurācijas versijas dzēšanas apstiprinājuma ziņojums](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigurācijas versija tiek dzēsta un tiek parādīts apstiprinājuma ziņojums. 

> [!NOTE]
> Konfigurācijas var dzēst tikai konfigurāciju nodrošinātājs, kas tās izveidoja. Ja konfigurācija ir koplietota ar citu organizāciju, tad pirms tās dzēšanas, konfigurācijas koplietošana ir jāatceļ.
 
