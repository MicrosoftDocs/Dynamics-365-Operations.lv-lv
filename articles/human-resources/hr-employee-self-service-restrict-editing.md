---
title: Ierobežot personiskās informācijas rediģēšanu
description: Ierobežot darbinieku kontaktinformācijas rediģēšanu Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052029"
---
# <a name="restrict-editing-of-personal-information"></a>Ierobežot personiskās informācijas rediģēšanu

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Šajā tēmā aprakstīts, kā ierobežot darbiniekus no kontaktinformācijas Dynamics 365 Human Resources rediģēšanas. Iespējams, vēlēsieties neļaut darbiniekiem rediģēt noteiktu kontaktinformāciju, piemēram, viņu uzņēmuma atrašanās vietu vai e-pasta adresi.

> [!NOTE]
> Lai izmantotu šo funkciju, vispirms aktivizējiet **(Priekšskatījums) Ierobežot darbiniekus no adreses un kontaktinformācijas pievienošanas vai rediģēšanas**, lai atlasītu līdzekļu pārvaldības nolūkus. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).<br><br>![Iespējot priekšskatījuma līdzekli](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Izvēlieties informāciju, ko darbinieks var pievienot vai rediģēt

1. Human Resources atlasiet **Personāla pārvaldība**, atlasiet **Saites**, un pēc tam atlasiet **Personāla vadības parametri**.

   ![Dodieties uz Cilvēkresursu parametri](./media/hr-employee-self-service-human-resources-parameters.png)

2. Lapā **Cilvēkresursu parametri** atlasiet cilni **Darbinieku pašapkalpošanās**.

   ![Atlasiet Darbinieku pašapkalpošanās pakalpojumu](./media/hr-employee-self-service-tab.png)

3. Cilnē **Darbinieku pašapkalpošanās** noņemiet visu informāciju sadaļā **Adrese un kontaktinformācija**, ka nevēlaties darbiniekus pievienot vai rediģēt. Šajā piemērā nepārbaudījām **Uzņēmuma** kontaktinformāciju.

   ![Ierobežot uzņēmuma kontaktinformācijas rediģēšanu](./media/hr-employee-self-service-restrict-business.png)

4. Atlasiet **Saglabāt**.

   ![Saglabāt izmaiņas](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Darbinieku pieredze

Kad darbinieki ir ierobežojuši pievienot vai rediģēt kontaktinformāciju, viņi var redzēt šo informāciju, bet to nevar mainīt.

Šajā piemērā, kur darbiniekiem ir ierobežota **Uzņēmuma** kontaktinformācijas rediģēšana, viņi joprojām var skatīt informāciju Darbinieku pašapkalpošanās sadaļā:

![Skatīt biznesa kontaktpersonas papildinformāciju](./media/hr-employee-self-service-restrict-view.png)

Tomēr, kad viņi izvēlas uzņēmuma kontaktpersonas informāciju, rūts **Rediģēt adresi** tiek parādīta kā tikai lasāma, un tās nevar mainīt nevienu no laukiem.

![Detalizēta informācija par uzņēmuma kontaktpersonu tiek rādīta kā tikai lasāma](./media/hr-employee-self-service-restrict-read-only.png)

Turklāt, ja tās atlasa **Pievienot**, lai pievienotu jaunu adresi, tās nevar atlasīt **Uzņēmumu** no **Nolūks** nolaižamās izvēles rūtiņas.

![Darbinieks nevar pievienot Uzņēmuma adresi](./media/hr-employee-self-service-restrict-add.png)

Darbinieki iegūst tādu pašu pieredzi, atlasot **Kontaktinformācija** **Personiskās informācijas** lapā un pievienojot jaunu adresi. Nolaižamais lodziņš **Nolūks** rāda tikai tos informācijas tipus, ko var pievienot. 

![Darbinieks nevar atlasīt Uzņēmumu nolaižamajā sarakstā Nolūks](./media/hr-employee-self-service-restrict-purpose.png)

Tagad **Detalizēta kontaktinformācija par kontaktpersonu** rāda režģī **Nolūku**.

![Nolūka rādīšana kontaktinformācijas režģī](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Skatiet arī

[Darbinieka un vadītāja patstāvīgi izmantojama pakalpojuma pārskats](hr-employee-manager-self-service-overview.md)<br>
[Konfigurēt Human Resources parametrus](hr-setup-parameters.md)<br>
[Rediģēt personisko informāciju](hr-employee-manager-self-service-edit-personal-information.md)