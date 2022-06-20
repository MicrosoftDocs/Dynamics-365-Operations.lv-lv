---
title: Dynamics 365 Human Resources infrastruktūras sapludināšana — laidiena 10.0.25 atjauninājums
description: Šajā rakstā ir sniegta informācija par Microsoft Dynamics 365 Human Resources release 10.0.25, kas sniedz pirmo spēju kopumu infrastruktūras saplūdē.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6be51c894d801ca0e7d211f1a6aeff0d68727662
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868088"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktūras sapludināšana — laidiena 10.0.25 atjauninājums

10.0.25 izpilde atved pirmo spēju kopumu infrastruktūras sapludināšanas laikā. Infrastruktūras sapludināšanas laikā korporācija Microsoft Dynamics 365 Human Resources tiks sapludināta ar Finanšu un operāciju infrastruktūru. Tomēr tā turpinās būt licencēta kā neatkarīgs pieteikums, piemēram, Dynamics 365 Finanses un Dynamics 365 Supply Chain Management. Papildinformāciju par infrastruktūras sapludināšanu skatiet infrastruktūras sapludināšanas [Dynamics 365 Human Resources FAQ](../human-resources/hr-infrastructure-merge-faq.md).

Sapludināšana nodrošinās personāla vadības lietotāju konsekvenci šādos veidos:

- [Vides pārvaldība un integrācijas ir saskaņotas starp cilvēkresursu un finanšu un operāciju programmām.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Pārvaldiet vides pakalpojumos Microsoft Dynamics Lifecycle Services, izdošanas meklēšanā un Regression Suite Automation Tool.
    - Ir viena koda bāze, kur personāla vadības jaunā funkcionalitāte ir izlaista kā daļa no parastā vienas versijas atjaunināšanas procesa.
    - Veids, kā vidēs tiek pielietoti jauninājumi, atjauninājumi un labojumfaili, ir konsekventi.

- [Paplašināmības opcijas ir uzlabotas.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - Varat turpināt lietot rīkus, lai Microsoft Power Platform paplašinātu, kā nepieciešams.
    - Funkcionalitāti var paplašināt ar formām, tabulām, metodēm un programmas programmēšanu interfeisiem (API).
    - Varat izveidot un paplašināt elementus.

    Papildinformāciju par pieejamām paplašinājuma opcijām skatiet [pārskatā par paplašināmību programmā Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Izveidojiet vienu personāla vadības spēju kopu programmā Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    10.0.25. laidienā funkcionālās iespējas, kas pastāvēja tikai cilvēkresursos, ir padarītas pieejamas Finanšu un operāciju infrastruktūrai. Lai debitori izmantotu šīs iespējas finanšu un operāciju vidē, līdzekļa Līdzekļu pārvaldībā ir jāiespējo tālāk minētie personāla vadības līdzekļi.

    | Līdzekļa nosaukums | Pārskats | Nodošanas izpildei statuss | 
    |--------------|----------|----------------| 
    | Nodarbinātības gadu skaita aprēķins | Iestatīšanas opcija ļauj atlasīt datumu, kas tiek lietots pakalpojumu **gadu aprēķinam**. | Vispārēji pieejams | 
    | Darbplūsmas pieredzes uzlabojumi | Šis līdzeklis nodrošina uzlabotu lietotāja pieredzi darbplūsmas iesniegšanas un apstiprinājumu veikšanā. | Vispārēji pieejams | 
    | Veiktspējas pārskatu drukāšana | Jūs varat izdrukāt veiktspējas pārskatus PDF formātā. | Vispārēji pieejams | 
    | Pielāgotās saites **pārvaldnieka pašapkalpošanās pakalpojumā** | Varat izveidot pielāgotas saites, kas tiek parādītas **pārvaldnieka pašapkalpošanās** **sadaļā Saistītās saites**. | Vispārēji pieejams | 
    | Starpuzņēmumu kompensācijas skats | Lietotāji var skatīt kompensāciju plānus **pārvaldnieka pašapkalpošanās** sistēmā visām juridiskajām personām bez nepieciešamības mainīt uzņēmumus. | Vispārēji pieejams | 
    | Konfigurēt vairākus atlīdzības līmeņus pēc darba\*&dagger; | Darbi tagad atbalsta vairākus atlīdzības līmeņus. | Priekšskatījums | 
    | Uzdevumu pārvaldība\* | Varat izveidot kontrolsarakstus un uzdevumus par to, kā tas iet uz darbu, izslēgšanas un pārejas procesam. | Priekšskatījums | 
    | Racionalizēta darbinieku ievade | Šis līdzeklis nodrošina atjauninātu lietotāja pieredzi esošajā darbinieka **lapā**. | Priekšskatījums | 
    | Cilvēkresursu lietotāju pieredzes uzlabojumi | Skatiet tabulu nākamajā sadaļā.  | Priekšskatījums | 

\* Šī funkcija ir jāieslēdz pirms personāla vadības **lietotāju pieredzes uzlabojumu funkcijas**.

&dagger; Pēc šī līdzekļa iespējošanas to nevar atspējot.

## <a name="human-resource-user-experience-enhancements"></a>Personāla vadības lietotāju pieredzes uzlabojumi

| Līdzekļa nosaukums | Pārskats | 
|--------------|----------| 
| Dzēst nodarbinātību | Ir iespējams izdzēst darbinieka nodarbinātību. | 
| Ģimenes ar amatu | Var izsekot darbu grupu, kurā iesaistīts līdzīgs darbs un kam nepieciešama līdzīga apmācība, prasmes, zināšanas un kompetence. | 
| Papildu nodarbinātības lauki | Tika pievienoti šādi lauki: **Nodarbinātības kategorija**, **Nodarbinātības** tips un **Nodarbinātības statuss**. | 
| **Darbinieki bez nodarbinātības** lapas | Lapā parādīts to darbinieku saraksts, kuriem nav nodarbinātības ieraksta. | 
| Pozīciju dimensijas lietotāju pieredzes atjaunināšana | Lai piešķirtu pozīciju dimensijas juridiskajām personām, ir lielāka lietotāja pieredze. | 
| Adreses izmaiņas personāla vadības **darbvietā** | Šī funkcija sniedz visu adreses izmaiņu skaitu, kas radās norādīto dienu skaitu, kā norādīts personāla vadības **parametru** lapā. | 
| Personāla vadības darbvietā beigbeigs **ierakstu** skaits | Šī funkcija sniedz to krājumu sarakstu, kuriem ir beidzies derīguma termiņš vai kuru derīgums beigsies sertifikātiem, identifikācijām, pārbaudēm, izvērtēšanām vai testiem. | 
| **Pozīciju hierarhijas pārbaudes** lapa | Ir veikta riņķveida atsauču pārbaude pozīciju rindu hierarhijā. | 
| Valstij raksturīgā algu informācija | Papildu algas lauki ir pieejami darbinieku **nodarbinātības** lapā atkarībā no tās juridiskās personas valsts vai reģiona, kurā darbinieki ir nodarbināti. | 
| Saskaņotības pārskatu uzlabojumi | Ir pieejamas papildu pārskatu opcijas EEO-1, Vets 4212 un OSHA300a. | 
| Personāla pārvaldības darbvietas **atjauninājumi** | Ir veikti atjauninājumi, lai izsekotu adrešu izmaiņas un ierakstus, kuru skaits beidzas. Turklāt jaunās cilnes sarakstam pie darbinieka un amata darbības. | 
