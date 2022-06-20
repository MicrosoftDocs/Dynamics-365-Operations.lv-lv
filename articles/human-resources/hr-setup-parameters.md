---
title: Human Resources parametru konfigurēšana
description: Šajā rakstā skaidrots, kā iestatīt uzņēmuma parametrus Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd645dcc79672e7f69afe47b803b90a04c22305d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856285"
---
# <a name="configure-human-resources-parameters"></a>Human Resources parametru konfigurēšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dažu cilvēkresursu parametru iestatījumi tiek koplietoti uzņēmumu starpā, savukārt citu parametru iestatījumi ir raksturīgi noteiktam uzņēmumam. Šajā rakstā skaidrots, kā iestatīt uzņēmuma raksturīgos cilvēkresursu parametrus.

Divas lapas tiek izmantotas, lai iestatītu cilvēkresursu parametrus. Parametriem, kas ir kopīgi visiem uzņēmumiem, izmanto lapu **Personāla vadības kopīgie parametri**. Parametriem, kas ir specifiski uzņēmumam (citiem vārdiem sakot, iestatījumi attiecas uz vienu uzņēmumu), izmanto lapu **Personāla vadības parametri**.

![Dodieties uz Cilvēkresursu parametri.](./media/hr-employee-self-service-human-resources-parameters.png)

Lapā **Personāla vadības parametri** iestatījumi ir sadalīti sešās cilnēs:

- **Vispārējā daļa**
- **Personāla atlase** (šī cilne nav iekļauta programmā Dynamics 365 Human Resources)
- **Kompensācija**
- **Numuru sērijas**
- **FMLA**
- **Darbinieku patstāvīgi izmantojamais pakalpojums**
- **Vadītāja pašapkalpošanās**
- **Atvieglojumu pārvaldība**
- **Atvaļinājumi un kavējumi**
- **Maksājuma metodes**

Katra cilne ietver informāciju, kas attiecas uz vienu uzņēmumu.

## <a name="general"></a>Vispārējā daļa

Iestatījumi lapā **Vispārīgi** nosaka informācijas parādīšanos par kavējumu, traumu un slimību un jaunām pieņemšanām darbā. Šīs cilnes iestatījumi definē arī dažus noklusējuma ierakstus, kas parādās darba laikā. It īpaši šī cilne ļauj:

- Atlasiet krāsu, kuru piemērot atvērtajām kavējumu transakcijām.
- Norādīt stilu lapu, kas jāizmanto pārskatiem.
- Iespējot integrāciju starp apmācību kursiem un prombūtnes reģistrēšanu.
- Atlasiet kavējuma kodu, kas tiek izmantots šīs integrācijas kontrolei.
- Norādiet, cik ilgi uzturēt traumas vai slimības gadījumu incidentus.
- Norādiet noklusēto identifikācijas numuru, kas tiek rādīts, pieņemot darbā jaunu darbinieku.
- Norādiet datumu, kas tiek lietots, lai aprēķinātu pakalpojuma gadu. 

![Cilne Vispārīgi.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Personāla atlase

Iestatījumi cilnē **Personāla atlase** definē dokumentu tipus, kas tiek izmantoti sarakstei, kas tiek automātiski nosūtīta kandidātiem. Varat arī norādīt personāla atlases projektu, ko izmanto neapstiprināto pieteikumu saņemšanai.

Periods, kas ir definēts personāla **atlases projekta** vecumstruktūrā, nosaka, kuri personāla atlases projekti ir iekļauti vecumstruktūras projektu elementā Personāla **atlases** **pārvaldības darbvietā**. Pieteikuma termiņa **brīdinājumam** **definētais periods tiek izmantots, lai parādītu personāla atlases projektus, kas tuvojas pieteikuma termiņam pieteikumu beigu termiņam, kurš personāla atlases darbvietā tuvojas elementam.**

Papildinformāciju par pieņemšanu darbā skatiet [Personāla atlases kandidāti](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensācija

Dynamics 365 Finanses cilnes Atlīdzība iestatījumi nosaka, vai lietotājiem jāapstiprina, **vai** viņi vēlas saglabāt informāciju par fiksētās vai mainīgās atlīdzības sistēmu. Ja atzīmējat izvēles rūtiņu **Iespējot saglabāšanas pārbaudi**, ikreiz, kad lietotāji aizver ar atlīdzību saistītu lapu, viņi saņem ziņojumu ar jautājumu, vai viņi vēlas saglabāt ierakstu. Dažas Atlīdzības pārvaldības lapas neļauj lietotājiem dzēst informāciju. Tāpēc prasot lietotājiem apstiprināt, ka viņi vēlas saglabāt informāciju, var ierobežot informācijas daudzumu, kas tiek saglabāts un ko nevar izdzēst vēlāk. Ja izvēles rūtiņa **Iespējot saglabāšanas pārbaudi** ir notīrīta, ieraksti tiek vienmēr saglabāti nekavējoties, iespējams pirms lietotājs ir gatavs. Ja jūs izmantojat veiktspējas pārvaldību, cilne **Atlīdzība** ļauj jums izvēlēties vērtēšanas modeli, ko veiktspējas vērtēšanas laikā lietot modeļa, kas piešķirts atlīdzības plāniem, vietā.

Cilvēkresursu sadaļā varat lietot cilni **Atlīdzība**, lai izvēlētos ierobežot piekļuvi atlīdzības plāniem un iestatīt noklusējuma valūtu.

Papildinformāciju par atlīdzību skatiet [Atlīdzības plānu pārskats](hr-compensation-overview.md).

![Kompensāciju cilne.](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Numuru sērijas

Iestatījumi cilnē **Numuru sērija** nosaka secības, ko izmanto, lai personāla vadības krājumiem automātiski piešķirtu ID, piemēram:

- Programmas
- Kavējumu reģistrācija
- Atlīdzības procesa rezultāti
- Lietu numuri
- Kursi
- Kursu darba kārtība

Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas** (atlasiet uz **Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**).

Plašāku informāciju par numuru secību skatiet [Numuru sērijas pārskats](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Nostrādāto stundu skaits nedrīkst pārsniegt 1250 un nodarbinātības garums nedrīkst pārsniegt 12 mēnešus. Šīs maksimālās vērtības ir saskaņā ar federālo likumu Amerikas Savienotajās Valstīs.

![Cilne Numuru sērijas.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Cilnē FMLA iestatiet FMLA piemērotības prasības un FMLA pilnvaru stundas. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes parametru konfigurēšana](hr-leave-and-absence-parameters.md).

![Cilne FMLA.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Darbinieku patstāvīgi izmantojamais pakalpojums

Iestatījumi cilnē Darbinieku **pašapkalpošanās ietekmē** to, kā darbiniekiem **parādās darbinieku** pašapkalpošanās. Šajā cilnē varat veikt šādus uzdevumus:

- Ievadiet darbinieka pašapkalpošanās **darbvietas** nosaukumu
- Atlasīt, kuru informāciju vadītājs var ievadīt darbiniekiem
- Pievienot darbiniekiem noderīgas saites
- Ierobežot darbinieku kontaktinformācijas pievienošanu vai rediģēšanu. Papildinformāciju skatiet sadaļā [Personas informācijas rediģēšanas](hr-employee-self-service-restrict-editing.md)ierobežošana.

Papildinformāciju par to, kā iestatīt darbinieku **pašapkalpošanos**, skatiet darbinieku [un pārvaldnieka pašapkalpošanās pārskatu](hr-employee-manager-self-service-overview.md).

![Darbinieku pašapkalpošanās cilne.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Vadītāja pašapkalpošanās

Pārvaldnieka pašapkalpošanās **cilnes iestatījumi ietekmē** pārvaldniekus, kas tiek skatīti pārvaldnieka **pašapkalpošanās sadaļā**. Šajā cilnē varat konfigurēt šādas opcijas:

- Ierakstu, kuru skaits beidzas, diapazons
- Informācijas pārvaldnieki var skatīt ierakstus, kuru termiņš beidzas
- Vai vadītāji var skatīt atvērtās pozīcijas paplašinātiem pārskatiem
- Izejas darbinieku skatījumi
- Noderīgas saites vadītājiem

Papildinformāciju par to, kā iestatīt pārvaldnieka **pašapkalpošanos**, skatiet darbinieku [un pārvaldnieka pašapkalpošanās pārskatu](hr-employee-manager-self-service-overview.md).

![Vadītāja pašapkalpošanās cilne.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Atvieglojumu pārvaldība

Cilnē Atvieglojumu **pārvaldība varat** konfigurēt e-pasta opcijas atvieglojumu pārvaldībai. Papildinformāciju par to, kā iestatīt un lietot atvieglojumu pārvaldību, skatiet atvieglojumu [pārvaldības pārskatā](hr-benefits-management-overview.md).

![Cilne Atvieglojumu pārvaldība.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Atvaļinājumi un kavējumi

Papildinformāciju par atvaļinājumu un kavējumu pārskatu skatiet tēmā [Atvaļinājumu un kavējumu pārskats](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Maksājuma metodes

Cilnē **Maksājuma metodes** varat atlasīt maksājumu metodes, ko atbalsta jūsu organizācija. Papildinformāciju par atlīdzību konfigurēšanu skatiet [Atlīdzības plānu pārskats](hr-compensation-overview.md).

![Cilne Maksājuma metodes.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
