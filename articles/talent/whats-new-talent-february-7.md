---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 7. februāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4005a8745e46a23fe16b94cab7b7aeb20f84035
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009766"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 7. februāris)

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="interview-scheduling-enhancements"></a>Interviju plānošanas uzlabojumi
Ir uzlabots viss interviju plānošanas process. Tagad varat skatīt iekšēja kandidāta kalendārā reģistrēto pieejamību un izmantot iekšējā kandidāta kalendāru grafika ieteikumiem. Papildinformāciju skatiet rakstā [Interviju plānošana un atsauksmes](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Darbu publicēšana pakalpojumā LinkedIn — novērsta uzņēmumu neatbilstības problēma
Ir novērsta problēma, kas izraisīja to, ka no programmas Attract pakalpojumā LinkedIn publicētie darbi tika rādīti ar nepareizu uzņēmuma nosaukumu. Papildinformāciju skatiet rakstā [Darbu izveide, apstiprināšana un publicēšana programmā Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Karjeras vietnes vietrāža URL rādīšana sadaļā Administratora iestatījumi
Tagad sadaļas **Administratora iestatījumi** apakšsadaļā **Karjeras vietnes pārvaldība** tiek rādīts karjeras vietnes sākumlapas vietrādis URL.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

**8.1.2134 būvējums**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Vairāku atlīdzības līmeņu atbalsts darbiem
Šīs izmaiņas sniedz iespēju darbam definēt vairāk nekā vienu atlīdzības līmeni un darbiniekam iestatīt fiksētas atlīdzības diapazonus, kas var atšķirties dažādiem plāniem, izmantojot vienu un to pašu darbu. 

Piemēram:    
*Darbs* — grāmatvedības pārvaldnieks, *saistītie atlīdzības līmeņi:* B1 un B2 — katram līmenim ir definēts vērtību diapazons. B1 = min. 50 000, vid. 60 000, maks. 75 000 un B2 = min. 65 000, vid. 74 000, maks. 85 000. Tagad gadījumā, ja veidojat darbinieku fiksēto atlīdzību, pamatojoties uz definētajiem piemērotības nosacījumiem, katrs fiksētās atlīdzības plāns var būt saistīts ar vienu un to pašu darbu un dažādiem šī darba līmeņiem. Tas sniedz iespēju definēt plānus dažādos reģionos/uzņēmumos un tos saistīti ar vienu un to pašu darbu, taču dažādiem diapazoniem bez nepieciešamības izveidot darbu dublikātus, lai iestatītu šīs atšķirības.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Lauka Atlīdzības līmenis pievienošana elementam Darbinieka fiksētā atlīdzība 
Šī jauninājuma ietveros ir atjaunināts elements Darbinieka fiksētā atlīdzība, ietverot tajā lauku **Kompensācijas līmenis**. Šis papildu lauks atvieglo darbinieka fiksētās atlīdzības plānu atjaunināšanu. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Darbu grupas atjaunināšana amatu atjaunināšanas un jaunu amatu izveides laikā
Tagad gadījumā, ja tiek mainīts amata darbs, tiek iestatīta parametra **Darbu grupa** noklusējuma vērtība, pamatojoties uz atlasīto darbu.

### <a name="performance-improvements-when-rendering-workspaces"></a>Veiktspējas uzlabojumi darbvietu atveidošanas laikā
Tagad darbvietās analīzes cilnes tiek ielādētas tikai tad, ja lietotājs piekļūst šīm lapām. Lapas sākotnējās atveidošanas laikā tās augšējā kreisajā stūrī tiek parādīts indikators.
