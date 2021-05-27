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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018713"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="c9ebc-103">Ierobežot personiskās informācijas rediģēšanu</span><span class="sxs-lookup"><span data-stu-id="c9ebc-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="c9ebc-104">Šajā tēmā aprakstīts, kā ierobežot darbiniekus no kontaktinformācijas Dynamics 365 Human Resources rediģēšanas.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c9ebc-105">Iespējams, vēlēsieties neļaut darbiniekiem rediģēt noteiktu kontaktinformāciju, piemēram, viņu uzņēmuma atrašanās vietu vai e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="c9ebc-106">Lai izmantotu šo funkciju, vispirms aktivizējiet **(Priekšskatījums) Ierobežot darbiniekus no adreses un kontaktinformācijas pievienošanas vai rediģēšanas**, lai atlasītu līdzekļu pārvaldības nolūkus.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="c9ebc-107">Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="c9ebc-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="c9ebc-108">![Iespējot priekšskatījuma līdzekli](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="c9ebc-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="c9ebc-109">Izvēlieties informāciju, ko darbinieks var pievienot vai rediģēt</span><span class="sxs-lookup"><span data-stu-id="c9ebc-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="c9ebc-110">Human Resources atlasiet **Personāla pārvaldība**, atlasiet **Saites**, un pēc tam atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Dodieties uz Cilvēkresursu parametri](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="c9ebc-112">Lapā **Cilvēkresursu parametri** atlasiet cilni **Darbinieku pašapkalpošanās**.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Atlasiet Darbinieku pašapkalpošanās pakalpojumu](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="c9ebc-114">Cilnē **Darbinieku pašapkalpošanās** noņemiet visu informāciju sadaļā **Adrese un kontaktinformācija**, ka nevēlaties darbiniekus pievienot vai rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="c9ebc-115">Šajā piemērā nepārbaudījām **Uzņēmuma** kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Ierobežot uzņēmuma kontaktinformācijas rediģēšanu](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="c9ebc-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-117">Select **Save**.</span></span>

   ![Saglabāt izmaiņas](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="c9ebc-119">Darbinieku pieredze</span><span class="sxs-lookup"><span data-stu-id="c9ebc-119">Employee experience</span></span>

<span data-ttu-id="c9ebc-120">Kad darbinieki ir ierobežojuši pievienot vai rediģēt kontaktinformāciju, viņi var redzēt šo informāciju, bet to nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="c9ebc-121">Šajā piemērā, kur darbiniekiem ir ierobežota **Uzņēmuma** kontaktinformācijas rediģēšana, viņi joprojām var skatīt informāciju Darbinieku pašapkalpošanās sadaļā:</span><span class="sxs-lookup"><span data-stu-id="c9ebc-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Skatīt biznesa kontaktpersonas papildinformāciju](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="c9ebc-123">Tomēr, kad viņi izvēlas uzņēmuma kontaktpersonas informāciju, rūts **Rediģēt adresi** tiek parādīta kā tikai lasāma, un tās nevar mainīt nevienu no laukiem.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Detalizēta informācija par uzņēmuma kontaktpersonu tiek rādīta kā tikai lasāma](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="c9ebc-125">Turklāt, ja tās atlasa **Pievienot**, lai pievienotu jaunu adresi, tās nevar atlasīt **Uzņēmumu** no **Nolūks** nolaižamās izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Darbinieks nevar pievienot Uzņēmuma adresi](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="c9ebc-127">Darbinieki iegūst tādu pašu pieredzi, atlasot **Kontaktinformācija** **Personiskās informācijas** lapā un pievienojot jaunu adresi.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="c9ebc-128">Nolaižamais lodziņš **Nolūks** rāda tikai tos informācijas tipus, ko var pievienot.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Darbinieks nevar atlasīt Uzņēmumu nolaižamajā sarakstā Nolūks](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="c9ebc-130">Tagad **Detalizēta kontaktinformācija par kontaktpersonu** rāda režģī **Nolūku**.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Nolūka rādīšana kontaktinformācijas režģī](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="c9ebc-132">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="c9ebc-132">See also</span></span>

[<span data-ttu-id="c9ebc-133">Darbinieka un vadītāja patstāvīgi izmantojama pakalpojuma pārskats</span><span class="sxs-lookup"><span data-stu-id="c9ebc-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="c9ebc-134">Konfigurēt Human Resources parametrus</span><span class="sxs-lookup"><span data-stu-id="c9ebc-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="c9ebc-135">Rediģēt personisko informāciju</span><span class="sxs-lookup"><span data-stu-id="c9ebc-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)