---
title: Dynamics 365 Human Resources infrastruktūras sapludināšana — laidiena 10.0.25 atjauninājums
description: Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 Human Resources izlaidums 10.0.25, kas sniedz pirmo infrastruktūru apvienošanas iespēju vilni.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024571"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktūras sapludināšana — laidiena 10.0.25 atjauninājums

10.0.25 laidiens sniedz pirmo infrastruktūras apvienošanas iespēju vilni. Infrastruktūras apvienošanas laikā Microsoft Dynamics 365 Human Resources tiks apvienota ar Finance and Operations infrastruktūru. Tomēr tas joprojām tiks licencēts kā neatkarīgs pieteikums, piemēram Dynamics 365 Finance un Dynamics 365 Supply Chain Management. Papildinformāciju par infrastruktūras apvienošanu sk [Dynamics 365 Human Resources infrastruktūras apvienošanas FAQ](../human-resources/hr-infrastructure-merge-faq.md).

Apvienošana cilvēkresursu lietotājiem nodrošinās konsekvenci šādos veidos:

- [Vides pārvaldība un integrācijas ir saskanīgas cilvēkresursu un finanšu un operāciju programmās.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Pārvaldiet vidi Microsoft Dynamics Dzīves cikla pakalpojumi, problēmu meklēšana un Regression Suite Automation Tool.
    - Pastāv viena koda bāze, kurā kā daļa no regulārā vienas versijas atjaunināšanas procesa tiek izlaista jauna funkcionalitāte cilvēkresursiem.
    - Veids, kā jauninājumi, atjauninājumi un labojumfaili tiek lietoti vidēs, ir konsekventi.

- [Ir uzlabotas paplašināšanas iespējas.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Jūs varat turpināt lietot Microsoft Power Platform instrumenti, lai paplašinātu pēc vajadzības.
    - Varat paplašināt funkcionalitāti, izmantojot veidlapas, tabulas, metodes un lietojumprogrammu saskarnes (API).
    - Varat izveidot un paplašināt entītijas.

    Papildinformāciju par pieejamajām paplašinājumu opcijām skatiet sadaļā [Pārskats par paplašināmību programmā Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Izveidojiet vienu cilvēkresursu iespēju komplektu programmā Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    10.0.25 laidienā Finance and Operations infrastruktūrā ir pieejamas funkcionālās iespējas, kas pastāvēja tikai cilvēkresursos. Lai klienti varētu izmantot šīs iespējas finanšu un operāciju vidē, funkciju pārvaldībā ir jāiespējo tālāk norādītie cilvēkresursu līdzekļi.

    | Līdzekļa nosaukums | Pārskats | Nodošanas izpildei statuss | 
    |--------------|----------|----------------| 
    | Nodarbinātības gadu skaita aprēķins | Iestatīšanas opcija ļauj atlasīt datumu, kas tiek izmantots **Nostrādāti gadi** aprēķins. | Vispārēji pieejams | 
    | Darbplūsmas pieredzes uzlabojumi | Šis līdzeklis nodrošina uzlabotu lietotāja pieredzi darbplūsmas iesniegšanai un apstiprināšanai. | Vispārēji pieejams | 
    | Veiktspējas pārskatu drukāšana | Varat izdrukāt veiktspējas pārskatus PDF formātā. | Vispārēji pieejams | 
    | Pielāgotas saites iekšā **Vadītāja pašapkalpošanās** | Varat izveidot pielāgotas saites, kas tiek rādītas **Saistītās saites** sadaļa **Vadītāja pašapkalpošanās**. | Vispārēji pieejams | 
    | Starpuzņēmumu kompensācijas skats | Lietotāji var apskatīt kompensācijas plānus **Vadītāja pašapkalpošanās** visām juridiskajām personām, nemainot uzņēmumus. | Vispārēji pieejams | 
    | Konfigurējiet vairākus atlīdzības līmeņus pēc darba\*&dagger; | Darbi tagad atbalsta vairākus atalgojuma līmeņus. | Priekšskatījums | 
    | Uzdevumu pārvaldība\* | Varat izveidot kontrolsarakstus un uzdevumus uzņemšanas, izslēgšanas un pārejas procesam. | Priekšskatījums | 
    | Racionalizēta darbinieku ievade | Šī funkcija nodrošina atjauninātu lietotāja pieredzi esošajā **Strādnieks** lappuse. | Priekšskatījums | 
    | Cilvēkresursu lietotāju pieredzes uzlabojumi | Skatiet tabulu nākamajā sadaļā.  | Priekšskatījums | 

\* Šī funkcija ir jāieslēdz pirms **Cilvēkresursu lietotāju pieredzes uzlabojumi** funkciju.

&dagger; Šo funkciju nevar atspējot pēc tā iespējošanas.

## <a name="human-resource-user-experience-enhancements"></a>Cilvēkresursu lietotāju pieredzes uzlabojumi

| Līdzekļa nosaukums | Pārskats | 
|--------------|----------| 
| Dzēst nodarbinātību | Jūs varat dzēst darbinieka darba līgumu. | 
| Darba ģimenes | Varat izsekot darbu grupai, kas ietver līdzīgu darbu un kam nepieciešama līdzīga apmācība, prasmes, zināšanas un pieredze. | 
| Papildu nodarbinātības jomas | Tika pievienoti šādi lauki: **Nodarbinātības kategorija**, **veids**, un **Nodarbinātības statuss**. | 
| **Strādnieki bez darba** lappuse | Lapā tiek parādīts to darbinieku saraksts, kuriem nav darba reģistra. | 
| Pozīcijas dimensijas lietotāja pieredzes atjauninājums | Ir uzlabota lietotāja pieredze pozīcijas dimensiju piešķiršanai katrai juridiskai personai. | 
| Adreses izmaiņas **Personāla vadība** darba vieta | Šis līdzeklis nodrošina visu to adrešu izmaiņu skaitu, kas notikušas noteiktā dienu skaitā, kā noteikts **Cilvēkresursu parametri** lappuse. | 
| Ierakstu derīguma termiņš beidzas **Personāla vadība** darba vieta | Šis līdzeklis nodrošina to vienumu sarakstu, kuru derīguma termiņš ir beidzies vai beigsies sertifikātiem, identifikācijām, pārbaudēm, pārbaudēm vai pārbaudēm. | 
| **Pozīciju hierarhijas apstiprināšana** lappuse | Tiek pārbaudītas apļveida atsauces pozīcijas līniju hierarhijā. | 
| Valsts specifiska algas informācija | Papildu algas lauki ir pieejami vietnē **Strādnieku nodarbinātība** lapu atkarībā no tās juridiskās personas valsts vai reģiona, kurā darbinieki ir nodarbināti. | 
| Atbilstības ziņošanas uzlabojumi | Papildu ziņošanas opcijas ir pieejamas EEO-1, Vets 4212 un OSHA300a. | 
| Atjauninājumi uz **Personāla vadība** darba vieta | Ir veikti atjauninājumi, lai izsekotu adreses izmaiņām un ierakstiem, kuru derīguma termiņš beidzas. Turklāt jaunās cilnēs ir uzskaita darbinieka un amatu darbības. | 
