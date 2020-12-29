---
title: Talent paplašināšana ar Power Apps un Power Automate
description: Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent - Attract, kas izmanto programmatūras Microsoft Power Apps un Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529638"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talent paplašināšana ar Power Apps un Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Talent: Attract, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate. Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē. Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.

> [!IMPORTANT]
> Ja vēlaties izmantot šajā rakstā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.


## <a name="prerequisites"></a>Priekšnosacījumi

- Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.
- Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.

## <a name="power-automate--form-connect"></a>Power Automate — Formas savienojums

Veidni **Power Automate – Formas savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.

Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem. Daži piemēri:

- Kandidātu novērtējumu tveršana.
- Rezultātu tveršana no kursu anketām.
- Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.
- Kandidāta intervijas procesa novērtējuma tveršana

Programmā Microsoft Dynamics 365: Attract formas var izmantot kandidātu portālā, kur kandidāti aizpilda datus. Formas varat arī iegult kā aktivitātes darba veidnē.

Kad kandidāts iesniedz formu, Microsoft Power Automate tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.

Lai lejupielādētu veidni **Power Automate – formas savienojums** un pielāgoto elementu struktūru, ejiet uz [Power Automate – Formas savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint Integrācija

Veidni **Power Automate – SharePoint Integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu. 

Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums. Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu. Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts. Šādā veidā iespējams ātrāk aizpildīt amatus, kas ir nepieciešami steidzami, jo paziņojumi palīdz atlases darbiniekiem meklēt kandidātus visā organizācijā.

Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.

Lai lejupielādētu veidni **Power Automate – SharePoint Integrācija**, ejiet uz [Power Automate – SharePoint Integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.

## <a name="referral-app"></a>Atsauces programma

Varat izmantot atsauces programmu, lai pievienotu kandidātus kopīgai darbinieku kopai. Iesniedzot kandidātu, ieteicējs var ievadīt datus **Vārds**, **Uzvārds**, **E-pasts** un **LinkedIn vietrādis URL**. Pēc tam kandidāts avota metadati tiek aizpildīti ar ieteicēja informāciju.

Šo programmu var iegult Darbinieku pašapkalpošanās (ESS) portālā atsauču iesniegšanai, vai arī to var izmantot kā hipersaiti uzņēmuma portālā un palaist kā savrupu programmu.

Lai lejupielādētu **Atsauces programmu**, dodieties uz [Dynamics 365 Talent paplašināmības risinājumu: Atsauces programma](https://www.microsoft.com/download/details.aspx?id=58497) Microsoft lejupielāžu centrā. Varat importēt šo programmu un pielāgot to, lai pievienotu papildu funkcionalitāti.

## <a name="additional-resources"></a>Papildu resursi

[Pakalpojums Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Programmu migrēšana starp nomniekiem un vidēm](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
