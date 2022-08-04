---
title: Elektronisko pārskatu konfigurāciju izveide pakalpojumā RCS un to augšupielāde globālajā repozitorijā
description: Šajā rakstā skaidrots, kā izveidot elektronisko pārskatu (ER) konfigurāciju Microsoft regulēšanas konfigurācijas pakalpojumos (RCS) un augšupielādēt to Globālajā repozitorijā.
author: JaneA07
ms.date: 01/11/2021
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
ms.openlocfilehash: f73f7189ad82d85169a4e0df573dd26dab8bb009
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070606"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER konfigurāciju izveide Regulatory Configuration Services (RCS) un to augšupielāde globālajā repozitorijā

[!include [banner](../includes/banner.md)]

Varat izmantot Microsoft Regulatory Configuration Services (RCS), lai veidotu elektroniska pārskata (ER) konfigurācijas un publicētu tās, lai tās varētu izmantot jūsu organizācija.

Tālāk aprakstītajās procedūrās ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot atvasinātu Elektroniskā pārskata (EK) versiju, kas ir konfigurēta RCS instancē, un pēc tam augšupielādēt atvasināto konfigurāciju globālajā repozitorijā. 

Lai varētu veikt šīs procedūras, ir jāizpilda šādi priekšnosacījumi:

- Ir piekļuve jūsu organizācijas RCS videi.
- Izveidojiet aktīvu konfigurācijas nodrošinātāju un padariet to aktīvu. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Jums ir jānodrošina, lai RCS vide būtu nodrošināta jūsu uzņēmumam. Ja jūsu organizācijai nav nodrošināta RCS instance, varat to darīt, izmantojot šādus soļus:

1. Finanšu un operāciju programmā dodieties uz organizācijas administrēšanas **darbalauku** \> **elektronisko** \> **pārskatu sniegšanu**.
2. Sadaļā **Saistītās saites/ Ārējās saites** atlasiet Regulēšanas **pakalpojumi –** konfigurācija un pēc tam sekojiet instrukcijām, lai **pierakstītos**, lai to nodrošinātu.

Ja RCS vide jau ir nodrošināta jūsu organizācijai, izmantojiet lapas vietrādi URL, lai tai piekļūtu, un atlasiet **pierakstīšanās** opciju.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Izveidot atvasinātu konfigurācijas versiju RCS

> [!NOTE]
> Ja šī ir pirmā reize, kad lietojāt RCS, jums nebūs pieejama neviena konfigurācija, no kuras iegūt. Jums būs jāimportē konfigurācija no globālā repozitorija. Plašāka informācija pieejama rakstā [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Pierakstīties RCS** un atlasiet Elektronisko pārskatu **darbvietu**.
2. Pārbaudiet, vai jums ir aktīvs konfigurācijas nodrošinātājs jūsu uzņēmumam, kas ir iestatīts kā aktīvs (skatiet priekšnosacījumus). 
3. Atlasiet **Pārskatu konfigurācijas**.
4. Atlasiet konfigurāciju, no kuras vēlaties atvasināt jauno versiju. Varat izmantot filtra lauku virs koka skata, lai sašaurinātu meklēšanu.
5. Atlasiet **Izveidot konfigurāciju** \> **Atvasināt no nosaukuma**.
6. Ievadiet nosaukumu un aprakstu un pēc tam atlasiet **Izveidot konfigurāciju**, lai izveidotu jaunu atvasinātu versiju ar statusu Melnraksts.
7. Atlasiet jauno atvasināto konfigurāciju un, ja nepieciešams, veiciet papildu izmaiņas konfigurācijas formātā. 
8. Kad izmaiņas ir pabeigtas, nepieciešams iestatīt **konfigurācijas izmaiņu** **statusu** uz Pabeigts, lai varētu to publicēt repozitorijā. Atlasiet **Labi**.

![Jauna konfigurācijas versija RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Kad konfigurācijas statuss ir mainīts, var tikt parādīts pārbaudes kļūdas ziņojums, kas saistīts ar savienotajām lietojumprogrammām. Lai izslēgtu pārbaudi, cilnes **Konfigurācijas** darbību rūtī atlasiet **Lietotāja parametri** un pēc tam opciju **Izlaist validāciju konfigurācijas statusa maiņai un pārbāzei** iestatītu uz **Jā** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfigurācijas augšupielāde globālajā repozitorijā

Lai kopīgotu jaunu vai atvasinātu konfigurāciju ar jūsu organizāciju, varat to augšupielādēt globālajā repozitorijā, veicot šādas darbības:

1. Atlasiet konfigurācijas pabeigtu versiju un pēc tam atlasiet **Augšupielādēt repozitorijā**.
2. Atlasiet opciju **Globāli (Microsoft)** un pēc tam atlasiet **Augšupielādēt**.

    ![Augšupielādēt repozitorija opcijās.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**. 
4. Atjauniniet versijas aprakstu pēc nepieciešamības un pēc tam atlasiet **Labi**. Pēc izvēles varat arī augšupielādēt versiju pievienotajā programmā vai GIT repozitorijā.  

Konfigurācijas statuss tiek atjaunināts uz **Koplietots**, un konfigurācija tiek augšupielādēta globālajā repozitorijā. Augšupielādētās konfigurācijas melnraksta versija arī tiek izveidota, un to var izmantot, ja nepieciešamas turpmākas izmaiņas.

Kad konfigurācija ir augšupielādēta globālajā repozitorijā, varat ar to strādāt šādos veidos:

- Importējiet to savā Dynamics 365 instancē. Papildinformāciju skatiet [(ER) Konfigurāciju importēšana no RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Koplietot to ar trešo pusi vai ārēju organizāciju, skatiet [RCS Koplietot elektronisko pārskatu (ER) konfigurācijas ar ārējām organizācijām](rcs-global-repo-share-configuration.md)

    ![Atvasinātā Intrastat Contoso konfigurācijas versija globālajā repozitorijā.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Konfigurācijas dzēšana no globālā repozitorija
Lai dzēstu jūsu organizācijas izveidoto konfigurāciju, veiciet tālāk norādītās darbības.

1. **Elektroniskā pārskata** darbvietā pārbaudiet, vai jūsu konfigurācijas nodrošinātājs ir **Aktīvs**. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Aktīvajam konfigurācijas nodrošinātājam atlasiet **repozitoriju**.
3. Atlasiet repozitorija veidu **Globāls** un atlasiet **Atvērt**.
4. Kopsavilkuma cilnē **Filtrs** atrodiet konfigurāciju, ko vēlaties dzēst, izmantojot funkciju **Filtrs**.
5. Kopsavilkuma cilnē **Versija** atlasiet konfigurācijas versiju, ko vēlaties dzēst, un pēc tam atlasiet **Dzēst**:

    ![Konfigurācijas dzēšana no globālā repozitorija.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Apstiprinājuma ziņojuma lodziņā atlasiet **Jā**.

    ![Konfigurācijas versijas dzēšanas apstiprinājuma ziņojums.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigurācijas versija tiek dzēsta un tiek parādīts apstiprinājuma ziņojums. 

> [!NOTE]
> Konfigurācijas var dzēst tikai konfigurāciju nodrošinātājs, kas tās izveidoja. Ja konfigurācija ir koplietota ar citu organizāciju, tad pirms tās dzēšanas, konfigurācijas koplietošana ir jāatceļ.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

