---
title: Integrācija ar LinkedIn Talent Hub
description: Šajā tēmā ir paskaidrots, kā iestatīt pintegrāciju starp Microsoft Dynamics 365 Human Resources un LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 208998b5c09416407612352da7a8ef5dd9491914
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889984"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integrācija ar LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) ir kandidātu izsekošanas sistēmas (ATS) platforma. Tā ļauj jums izveidot, pārvaldīt un nolīgt darbiniekus vienuviet. Integrējot Microsoft Dynamics 365 Human Resources ar LinkedIn Talent Hub, varat viegli izveidot darbinieku ierakstus Human Resources kandidātiem, kuri ir nolīgti amatam.

## <a name="setup"></a>Iestatīt

Sistēmas administratoram ir jāaizpilda iestatījumi, lai iespējotu integrāciju ar LinkedIn Talent Hub. Vispirms Power Apps vidē jums ir jāiestata lietotājs un drošības loma, lai piešķirtu LinkedIn Talent Hub atbilstošās atļaujas datu rakstīšanai Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Sasaistiet savu vidi ar LinkedIn Talent Hub

1. Atveriet [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Lietotāja nolaižamajā izvēlnē atlasiet **Preces iestatījumi**.

3. Sadaļas papildu navigācijas rūtī kreisajā pusē sadaļas **Papildu** atlasiet **Integrācija**.

4. Atlasiet **Autorizēšana** Microsoft Dynamics 365 Human Resources integrācijai.

5. Lapā **Dynamics 365 Human Resources** atlasiet vidi, lai sasaistītu LinkedIn Talent Hub, un pēc tam atlasiet **Sasaistīt**.

    ![LinkedIn Talent Hub pievienošana](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Var sasaistīt tikai ar vidēm, kurās jūsu lietotāja kontam ir administratora piekļuve gan Human Resources videi, gan saistītajai Power Apps videi. Ja saites lapā Human Resources nav norādīta neviena vide, pārliecinieties, vai jums ir licencētas Human Resources vides šajā nomniekā un vai lietotājam, ar kuru pierakstījāties saites lapā, ir administratora atļaujas gan Human Resources vidē, gan Power Apps vidē.

### <a name="create-a-power-apps-security-role"></a>Izveidojiet Power Apps drošības lomu

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).

2. Sarakstā **Vides** atlasiet vidi, kas saistīta ar Human Resources vidi, ko vēlaties saistīt ar savu LinkedIn Talent Hub instanci.

3. Atlasiet **Iestatījumi**.

4. Izvērsiet mezglu **Lietotāji + atļaujas** un atlasiet **Drošības loma**.

5. Lapas **Drošības lomas** rīkjoslā atlasiet **Jauna loma**.

6. Cilnē **Detalizēta informācija** ievadiet lomas nosaukumu, piemēram, **LinkedIn Talent Hub HRIS integrācija**.

7. Cilnē **Pielāgošana** atlasiet organizācijas līmeņa **Lasīšanas** tālāk minētajiem elementiem.

    - Elements
    - Lauks
    - Saistība

8. Saglabājiet un aizveriet drošības lomu.

### <a name="create-a-power-apps-application-user"></a>Izveidojiet Power Apps programmas lietotāju

Programmas lietotājam jāizveido LinkedIn Talent Hub adapteris, lai piešķirtu atļaujas adapterim rakstīt kandidātu ierakstus Power Apps vidē.

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).

2. Sarakstā **Vides** atlasiet vidi, kas saistīta ar Human Resources vidi, ko vēlaties saistīt ar savu LinkedIn Talent Hub instanci.

3. Atlasiet **Iestatījumi**.

4. Izvērsiet mezglu **Lietotāji + atļaujas** un atlasiet **Lietotāji**.

5. Atlasiet **Pārvaldīt lietotājus Dynamics 365**.

6. Izmantojiet nolaižamo izvēlni virs saraksta, lai mainītu skatu no noklusējuma **Iespējot lietotājus** skata uz **Programmas lietotāji**.

    ![Programmas lietotāju skats](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Rīkjoslā atlasiet **Jauns**.

8. Lapā **Jauns lietotājs** izpildiet šādas darbības:

    1. Mainiet lauka **Lietotāja veids** vērtību uz **Programmas lietotājs**.
    2. Iestatiet lauku **Lietotāja nosaukums** uz **Dynamics365 HR LinkedIn HRIS Integration**.
    3. Iestatiet lauku **Programmas ID** uz **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Ievadiet jebkuru vērtību laukos **Vārds**, **Uzvārds** un **Primārais e-pasts**.
    5. Rīkjoslā atlasiet **Saglabāt \& Aizvērt**.

### <a name="assign-a-security-role-to-the-new-user"></a>Drošības lomas piešķiršana jaunajam lietotājam

Kad esat saglabājis un aizvēris jauno programmas lietotāju iepriekšējā sadaļā, jūs tiekat atgriezts lapā **Lietotāju saraksts**.

1. Lapā **Lietotāju saraksts** mainiet skatu uz **Programmas lietotāji**.

2. Atlasiet programmas lietotāju, ko izveidojāt iepriekšējā sadaļā.

3. Rīkjoslā atlasiet **Pārvaldīt lomas**.

4. Atlasiet drošības lomu, ko iepriekš izveidojāt integrācijai.

5. Atlasiet **Labi**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Pievienojiet programmu Azure Active Directory programmā Human Resources

1. Programmā Dynamics 365 Human Resources atveriet lapu **Azure Active Directory programmas**.
2. Pievienojiet jaunu ierakstu sarakstam iestatiet tālāk norādītos laukus.

    - **Klienta ID**: ievadiet **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Nosaukums**: ievadiet Power Apps iepriekš izveidotās drošības lomas nosaukumu, piemēram, **LinkedIn Talent Hub HRIS integrācija**.
    - **Lietotāja ID**: atlasiet lietotāju, kuram ir atļauja rakstīt datus Personāla vadībā.

### <a name="create-the-table-in-dataverse"></a>Tabulas izveide sistēmā Dataverse

> [!IMPORTANT]
> Integrācija ar LinkedIn Talent Hub ir atkarīga no virtuālajām tabulām pakalpojumā Dataverse programmai Human Resources. Kā priekšnosacījums šai darbībai iestatījumā jums ir jākonfigurē virtuālās tabulas. Papildinformāciju par to, kā konfigurēt virtuālās tabulas, skatiet sadaļā [Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](./hr-admin-integration-common-data-service-virtual-entities.md).

1. Human Resources atveriet lapu **Dataverse integrācija**.

2. Atlasiet cilni **Virtuālās tabulas**.

3. Filtrējiet elementa sarakstu pēc elementa etiķetes, lai atrastu **LinkedIn eksportētais kandidāts**.

4. Atlasiet elementu un pēc tam atlasiet **Ģenerēt/atsvaidzināt**.

## <a name="exporting-candidate-records"></a>Kandidāta ierakstu eksportēšana

Kad iestatīšana ir pabeigta, personāla atlases darbinieki un cilvēkresursu (HR) speciālisti var izmantot funkciju **Eksportēt uz HRIS** LinkedIn Talent Hub, lai eksportētu nolīgto kandidātu ierakstus no LinkedIn Talent Hub uz programmu Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Ierakstu eksportēšana no LinkedIn Talent Hub

Kad kandidāts ir izgājis personāla atlases procesu un ir nolīgts, varat eksportēt kandidāta ierakstu no LinkedIn Talent Hub uz programmu Human Resources.

1. LinkedIn Talent Hub atveriet projektu, kuram esat nolīdzis jauno darbinieku.

2. Atlasiet kandidāta ierakstu.

3. Atlasiet **Mainīt posmu** un pēc tam atlasiet **Nolīgts**.

4. Kandidāta izvēlnē Daudzpunkte (**...**) atlasiet opciju **Eksportēt uz HRIS**.

5. Rūtī **Eksportēt uz HRIS** ievadiet informāciju, kas ir jāeksportē:

    - Laukā **HRIS nodrošinātājs** atlasiet **Microsoft Dynamics 365 Human Resources**.
    - Laukā **Sākuma datums** atlasiet vērtību jaunajam darbiniekam.
    - Laukā **Amats** ievadiet jaunā darbinieka darba amata nosaukumu.
    - Laukā **Atrašanās vieta** ievadiet vietu, kur darbinieks atradīsies.
    - Ievadiet vai apstipriniet darbinieka e-pasta adresi.

![Eksportēšana uz HRIS rūti LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Darbā pieņemšanas pabeigšana programmā Human Resources

Kandidāta ieraksti, kas tiek eksportēti no LinkedIn Talent Hub uz programmu Human Resources, tiek parādīti lapas **Personāla vadība** sadaļā **Kandidāti nolīgšanai**.

1. Human Resources atveriet lapu **Personāla vadība**.

2. Sadaļā **Kandidāti nolīgšanai** atlasītajam kandidātam atlasiet **Nolīgt**.

3. Dialoglodziņā **Nolīgt jaunu darbinieku** pārskatiet ierakstu un pievienojiet visu nepieciešamo informāciju. Varat arī atlasīt amata numuru, uz kuru kandidāts ir nolīgts.

Kad vajadzīgā informācija ir ievadīta, varat turpināt standarta procesus, lai izveidotu darbinieka ierakstus un pieņemtu darbiniekus darbā.

Tālāk norādītā informācija tiek importēta un iekļauta jaunā darbinieka ierakstā:

- Vārds
- Uzvārds
- Darba attiecību uzsākšanas datums
- E-pasta adrese
- Tālruņa numurs

## <a name="see-also"></a>Skatiet arī

[Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]