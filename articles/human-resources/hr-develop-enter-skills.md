---
title: Ievadīt prasmes
description: Darbi un vadītāji var ievadīt prasmes programmā Dynamics 365 Human Resources.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693008"
---
# <a name="enter-skills"></a>Ievadīt prasmes

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbiniekiem, kandidātiem vai kontaktpersonām varat ievadīt mērķa prasmes vai faktiskās prasmes programmā Dynamics 365 Human Resources. Mērķa prasme ir prasme, ko persona plāno sasniegt. Faktiskā prasme ir prasme, kas personai piemīt pašlaik.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Izveidot darbplūsmu, lai automātiski apstiprinātu prasmes

Lai ievadītu prasmes bez apstiprinājuma, jāizveido darbplūsma, lai automātiski apstiprinātu prasmes.

> [!NOTE]
> Darbinieku ievadītās prasmes vienmēr pieprasa vadītāja apstiprinājumu. Šī darbplūsma automātiski apstiprina tikai tās prasmes, ko ievada vadītāji savu darbinieku vārdā.

1. Darbvietā **Personāla vadība** atlasiet **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.

3. Atlasiet **Jauns**.

4. Darbības rūtī **Izveidot darbplūsmu** atlasiet **Darbinieka prasmes**.

   [![Atlasīt Darbinieka prasmju darbplūsmu.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Dialoglodziņā **Atvērt šo failu?** atlasiet **Atvērt**. Kad tiek piedāvāts, ievadiet savus akreditācijas datus.

6. Darbplūsmas redaktorā atlasiet darbplūsmas elementu **Apstiprināt prasmes** un velciet to uz kanvu.

   [![Atlasīt Apstiprināt prasmes darbplūsmas elementu.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Saistiet **Sākuma** elementu ar **Apstiprināt prasmes 1** elementu un pēc tam saistiet **Apstiprināt prasmes 1** elementu ar **Beigu** elementu. Jums var būt nepieciešams ritināt uz leju, lai skatītu **Beigu** elementu. Varat to vilkt tuvāk citiem elementiem.

   [![Saistīt darbplūsmas elementus.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Veiciet dubultklikšķi uz **Apstiprināt prasmes 1** darbplūsmas elementu, un pēc tam ar peles labo pogu noklikšķiniet uz **1. solis** elementu. Ar peles labo pogu noklikšķiniet uz elementu **1. solis** un pēc tam atlasiet **Rekvizīti**.

9. Logā **Rekvizīti** atlasiet **Nosacījums**, kas atrodas kreisās puses navigācijas joslā.

10. Atlasiet **Izpildīt šo soli, ja ir spēkā šāds nosacījums**.

11. Atlasīt **Pievienot nosacījumu**. Pēc **Kur** atlasiet **Darbinieku pašapkalpošanās prasmes**, un pēc tam atlasiet **Darbinieku pašapkalpošanās prasmes.Persona**. Pēc **ir** atlasiet **lauku** un pēc tam atlasiet **Lietotāja attiecības ar personu.Persona**.

    [![Norādīt nosacījumu.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Atlasiet **Piešķire** navigācijas joslā pa kreisi.

13. Cilnē **Piešķires tips** atlasiet **Hierarhija**.

14. Cilnes **Hierarhijas atlase** laukā **Hierarhijas tips:** atlasiet **Vadības hierarhija**.

    [![Norādīt vadības hierarhiju.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Atlasiet **Aizvērt**, atlasiet **Darbplūsma** kanvas navigācijā un pēc tam atlasiet **Saglabāt un aizvērt**.

Lai iegūtu vairāk informācijas par darbplūsmu izveidi, skatiet [Darbplūsmas sistēmas apskats](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Ievadīt darbinieka prasmes

1. Atlasīt darbinieku.

2. Lapas **Darbinieks** darbību joslā atlasiet **Persona** un pēc tam atlasiet **Prasmes**.

3. Lapā **Prasmes** aizpildiet šādus laukus katrai prasmei:

   - **Prasme**: atlasiet prasmi.
   - **Līmeņa tips**: atlasiet **Faktiski** prasmei, kas darbiniekam jau ir, vai atlasiet **Mērķis** prasmei, uz kuru darbinieks strādā.
   - **Līmenis**: atlasiet līmeni darbinieka prasmēm.
   - **Līmeņa datums**: atlasiet datumu, noklikšķiniet uz kalendāra rīku.
   - **Eksaminētājs**: ja nepieciešams, atlasiet eksaminētāju no saraksta. Savu meklēšanu var filtrēt.
   - **Gadu pieredze**: ievadiet pieredzes gadus.
   - **Pārbaudīts**: ja prasme ir pārbaudīta, atzīmējiet izvēles rūtiņu.
   - **Pārbaudīja**: ievadiet pārbaudītāja vārdu.

4. Kad prasmes ir ievadītas, atlasiet **Saglabāt**.

## <a name="see-also"></a>Skatiet arī

[Konfigurēt prasmes](hr-develop-skills.md)<br>
[Kartēt prasmes](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
