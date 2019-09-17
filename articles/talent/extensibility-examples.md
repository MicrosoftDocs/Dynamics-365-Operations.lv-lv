---
title: Talent paplašināšana, izmantojot PowerApps un Microsoft Flow — paraugsituācijas
description: Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 for Talent, kuros tiek izmantota programmatūra Microsoft PowerApps un Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0b455a8194f58b41a349f004ceda8183c7ee3f7c
ms.sourcegitcommit: 9f94eff93d29bc27352569824e00bbccc2f961b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/22/2019
ms.locfileid: "1781446"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Talent paplašināšana, izmantojot PowerApps un Microsoft Flow — paraugsituācijas

Šajā tēmā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 for Talent, kuros tiek izmantota programmatūra Microsoft PowerApps un Microsoft Flow. Varat importēt ar katru piemēru saistīto risinājumu pakotni savā PowerApps vidē. Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.

> [!IMPORTANT]
> Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmu nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.


## <a name="prerequisites"></a>Priekšnosacījumi

- Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.
- Lai eksportētu vai importētu programmas, lietotājiem jābūt PowerApps 2. plāna licencei vai PowerApps 2. plāna izmēģinājuma licencei.

## <a name="flow--form-connect"></a>Flow — Forms savienojums

Veidni **Flow — Forms savienojums** var izmantot, lai nolasītu datus no pakalpojuma Microsoft Forms un saglabātu tos Common Data Service elementā.

Šo veidni var paplašināt, lai to varētu izmantot citiem scenārijiem. Daži piemēri:

- Kandidātu novērtējumu tveršana.
- Rezultātu tveršana no kursu anketām.
- Intervijām paredzētu jautājumu bibliotēkas veidošana personāla vadības administratoriem.
- Kandidāta intervijas procesa novērtējuma tveršana

Programmā Microsoft Dynamics 365: Attract formas var parādīt kandidātu portālā, un kandidāti var aizpildīt datus. Formas var arī iegult kā aktivitātes darba veidnē.

Kad kandidāts iesniedz formu, Microsoft Flow tver formas iesniegšanu, nolasa datus un saglabā tos Common Data Service elementā.

Lai lejupielādētu veidni **Flow — Forms savienojums** un pielāgoto elementu struktūru, atveriet [Flow — Forms savienojums](https://go.microsoft.com/fwlink/?linkid=2081988) Microsoft lejupielādes centrā.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Uz PowerApps nodoto parametru iniciēšana un izvilkšana

Veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** var izmantot kā sākumpunktu jebkuram PowerApps scenārijs, kas attiecas uz Attract. Tajā ietilpst visi noklusējuma parametri, kurus nodod Attract, piemēram, **Darba pieteikums**, **Kandidāta ID** un **Darba ID**.

Šo veidni var izmantot, lai izgūtu kandidātu novērtējuma veidlapu, lai par pieņemšanu darbā atbildīgais vadītājs varētu redzēt kandidāta aizpildīto novērtējumu.

Programmas, kas tiek izveidotas, izmantojot PowerApps, var iegult darba veidnē programmā Attract.

Lai lejupielādētu veidni **Uz PowerApps nodoto parametru iniciēšana un izvilkšana** un pielāgoto elementu struktūru, atveriet [Uz PowerApps nodoto parametru iniciēšana un izvilkšana](https://go.microsoft.com/fwlink/?linkid=2081991) Microsoft lejupielādes centrā.

## <a name="integration-with-office-365"></a>Integrācija ar Office 365

Programmu **Integrācija ar Office 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft Office 365. Tā izmanto atsauces uz nodarbinātajiem programmā Talent, lai iegūtu ierašanās un aiziešanas informāciju un ierakstus par izņēmumiem. Ierašanās un aiziešanas informācija tiek glabāta pielāgotos Common Data Service elementos. Tiek pieņemts, ka šī informācija tiek aizpildīta no trešo pušu sistēmām, izmantojot integrāciju.

Šo programmu var paplašināt, lai to varētu izmantot citiem scenārijiem. Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.

Lai lejupielādētu programmu **Integrācija ar Office 365** un pielāgoto elementu struktūru, atveriet [Integrācija ar Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielādes centrā.

## <a name="flow--email-notification"></a>Sūtīt — e-pasta paziņojums

Veidni **Flow — e-pasta paziņojums** var izmantot e-pasta paziņojumu scenārijiem. To var izmantot, lai aktivizētu paziņojuma e-pastus kandidātiem, kurus darbā pieņemšanas grupa noraida jebkurā personāla atlases procesa posmā.

Šo veidni var paplašināt, lai izsekotu kandidāta posma izmaiņām visā personāla atlases procesā un nosūtītu paziņojumus darbā pieņemšanas grupai un kandidātam.

Parasti elementiem, kas tiek glabāti Common Data Service, var iestatīt plūsmas, lai nosūtītu paziņojumus par notikumiem, kas notiek programmās Core HR, Attract vai Dynamics 365 Talent: Onboard.

Lai lejupielādētu veidni **Flow — e-pasta paziņojums**, atveriet [Plūsma — e-pasta paziņojums](https://go.microsoft.com/fwlink/?linkid=2082103) Microsoft lejupielādes centrā.

## <a name="flow--sql-connect-and-execute"></a>Plūsmas — SQL savienojums un izpilde

Veidne **Flow — SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.

Lai gan šī veidne ir izveidota, lai lasītu un atjauninātu SQL tabulas, to var paplašināt, lai to varētu izmantot citiem scenārijiem. Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.

Lai lejupielādētu veidni **Flow — SQL savienojums un izpilde**, atveriet [Flow — SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.

## <a name="flow--sharepoint-integration"></a>Flow — SharePoint integrācija

Veidni **Flow — SharePoint integrācija** var izmantot, lai nolasītu datus no Microsoft SharePoint saraksta, salīdzinātu sarakstu ar lauka vērtībām jebkuram Common Data Service elementam un nosūtītu salīdzinājuma rezultātus kā paziņojuma e-pastu. 

Organizācijai var būt steidzami nepieciešams noteikts prasmju kopums. Šīs prasmes var saglabāt SharePoint kā SharePoint sarakstu. Kandidātam piesakoties tādam darbam, kuram ir izveidots saraksts ar nepieciešamo prasmju kopumu, ja pastāv būtiska atbilstība starp kandidāta prasmēm un SharePoint saglabātajām prasmēm, tiek nosūtīts paziņojuma e-pasts. Šādā veidā amati, kas ir nepieciešami steidzami, tiek aizpildīti ātrāk, jo paziņojumi palīdz atlases darbiniekiem paplašināt kandidātu meklējumus un sadarboties darbā pieņemšanas jomā visā organizācijā.

Šo veidni var paplašināt, lai to varētu izmantot jebkurā scenārijā, kas ietver SharePoint integrāciju.

Lai lejupielādētu veidni **Flow — SharePoint integrācija**, atveriet [Plūsma — SharePoint integrācija](https://go.microsoft.com/fwlink/?linkid=2082109) Microsoft lejupielādes centrā.

## <a name="referral-app"></a>Atsauces programma
Varat izmantot atsauces programmu, lai pievienotu kandidātus kopīgai darbinieku kopai. Iesniedzot kandidātu, ieteicējs var ievadīt **Vārdu**, **Uzvārdu**, **E-pastu** un **Linkedln vietrādi URL**. Pēc tam kandidāts avota metadati tiek aizpildīti ar ieteicēja informāciju.

Šo programmu var iegult Darbinieku pašapkalpošanās (ESS) portālā atsauču iesniegšanai, vai arī to var izmantot kā hipersaiti uzņēmuma portālā un palaist kā savrupu programmu.

Lai lejupielādētu **Atsauces programmu**, dodieties uz [Dynamics 365 for Talent paplašināmības risinājumu: Atsauces programma](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) Microsoft lejupielāžu centrā. Varat importēt šo programmu un pielāgot to, lai pievienotu papildu funkcionalitāti.

## <a name="additional-resources"></a>Papildu resursi

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Programmu migrēšana starp nomniekiem un vidēm](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
