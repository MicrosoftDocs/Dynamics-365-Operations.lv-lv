---
title: Talent paplašināšana ar Power Apps un Power Automate
description: Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e89347829ccd6569d568db42c79b5fea2316ba3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527030"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Paplašināšana ar Power Apps un Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti paplašināmības scenāriju piemēri programmai Microsoft Dynamics 365 Human Resources, kuros tiek izmantota programmatūra Microsoft Power Apps un Microsoft Power Automate. Varat importēt ar katru piemēru saistīto risinājumu pakotni savā Power Apps vidē. Pēc tam varat izmantot pakotnes kā vadlīnijas vai kā sākumpunktu, lai īstenotu scenārijus, kas attiecas uz jūsu organizāciju.

> [!IMPORTANT]
> Ja vēlaties izmantot šajā tēmā aprakstītās veidnes un programmas nemainītā veidā, pārbaudiet tās un pārliecinieties, ka tās aptver visus scenārijus, kas raksturīgi jūsu ieviešanai.

## <a name="prerequisites"></a>Priekšnosacījumi

- Lai importētu pakotnes, lietotājiem ir jābūt atļaujai **Vides veidotājs**.
- Lai eksportētu vai importētu programmas, lietotājiem jābūt Power Apps 2. plāna licencei vai Power Apps 2. plāna izmēģinājuma licencei.

## <a name="integration-with-microsoft-365-power-automate"></a>Integrācija ar Microsoft 365, Power Automate

Programmu **Integrācija ar Microsoft 365** var izmantot, lai iegūtu grupas informāciju lietotājiem, kuri ir pierakstījušies, no programmas Microsoft 365. Tajā ir atsauces uz Human Resources darbiniekiem, lai izvilktu darbinieka identifikācijas veidus. Vadītāji var pārbaudīt darbinieku ID veidu beigu datumus. Ja darbinieka ID veida termiņš drīz beigsies, viņi var arī nosūtīt atgādinājumu pa e-pastu. Power Automate integrējas Power Apps, lai nosūtītu šo atgādinājumu. Apstiprinājums tiks nosūtīts atpakaļ Power Apps no Power Automate, kad atgādinājums ir nosūtīts. Identifikācijas veidi ietver autovadītāja apliecību, pasi un citus pieņemamus ID veidus.

Šo programmu varat paplašināt citos scenārijos. Piemēram, to var izmantot, lai rādītu darba grupas atvaļinājumu informāciju, kalendāra notikumus un ar darba grupu saistītus notikumus.

Lai lejupielādētu programmu **Integrācija ar Microsoft 365, Power Automate**, dodieties uz [Integrācija ar Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft lejupielāžu centrā.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL savienojums un izpilde

Veidne **Power Automate – SQL savienojums un izpilde** izveido savienojumu ar Microsoft SQL Server un nodrošina SQL vaicājumu izpildi.

Lai arī šī veidne lasa un atjaunina SQL tabulas, varat to izvērst un izmantot citos scenārijos. Piemēram, to var izmantot, lai aizpildītu sagatavošanas tabulu pakalpojumā Common Data Service ar ierakstiem no SQL Server un periodiski sinhronizētu sagatavošanas tabulu, izmantojot inkrementālu sadali no SQL Server.

Detalizēts vaicājums ir integrēts ar plūsmu, lai iespējotu datu transformāciju un inkrementālo sadali.

Lai lejupielādētu veidni **Power Automate – SQL savienojums un izpilde**, ejiet uz [Power Automate – SQL savienojums un izpilde](https://go.microsoft.com/fwlink/?linkid=2081789) Microsoft lejupielādes centrā.

## <a name="additional-resources"></a>Papildu resursi

[Risinājums Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]