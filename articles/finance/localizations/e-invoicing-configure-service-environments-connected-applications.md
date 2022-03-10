---
title: Pakalpojumu vides un saistīto lietojumprogrammu konfigurēšana
description: Šajā tēmā ir sniegta informācija par to, kā konfigurēt pakalpojumu vides un saistītās lietojumprogrammas.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371917"
---
# <a name="configure-service-environments-and-connected-applications"></a>Pakalpojumu vides un saistīto lietojumprogrammu konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par to, kā konfigurēt pakalpojumu vides un saistītās lietojumprogrammas. Šim procesam ir trīs soļi. 1. darbība ir obligāta, un 2. un 3. darbība nav obligāta.

## <a name="step-1-create-a-service-environment"></a>1. darbība: pakalpojuma vides izveide

Veidojot pakalpojumu vidi, definējiet to lietotāju sarakstu, kuri tajā var izvietot globalizācijas līdzekļus. Pēc izvēles dažiem scenārijiem definējiet to ārējo lietojumprogrammu sarakstu, kas var sazināties ar elektronisko rēķinu izrakstīšanas pakalpojumu. Iestatiet numuru sērijas, ja tās izmantosit savos scenārijos.

Lai veiktu šo darbību, skatiet sadaļu [Pakalpojumu vides](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2. darbība: sertifikātu un noslēpumu pievienošana

Pievienojiet atsauci uz atslēgas Microsoft Azure seifu un noslēpumiem, lai tos izmantotu savos scenārijos. Šis solis ir obligāts, ja apstrādes konveijeru darbībās tiek izmantoti sertifikāti un noslēpumi digitālajai parakstīšanai vai saziņai ar ārējiem tīmekļa pakalpojumiem.

Lai pabeigtu šo darbību, skatiet rakstu [Klientu sertifikāti un noslēpumi](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3. darbība: saistīto lietojumprogrammu konfigurēšana

Lai iestatītu saziņu starp Dynamics 365 Finance lietojumprogrammām vai Dynamics 365 Supply Chain Management lietojumprogrammām un elektroniskajiem rēķiniem, ir jākonfigurē Finance vai Supply Chain Management, lai izveidotu zvanu uz elektronisko rēķinu izrakstīšanas pakalpojumu un sagatavotu biznesa datus vienotā struktūrā, kuru var pārveidot nepieciešamajā elektroniskajā formātā. Lietojumprogrammām ir arī pareizi jāapstrādā atbildes no pakalpojuma. Šo konfigurāciju var pabeigt tieši finanšu vai piegādes ķēdes pārvaldības vidē, vai arī to var pabeigt regulatīvās konfigurācijas pakalpojumā (RCS). Ja pabeidzat konfigurāciju RCS, varat to izvietot savā finanšu vai piegādes ķēdes pārvaldības vidē. Šajā solī jūs reģistrēsiet pievienoto lietojumprogrammu parametru izvietošanai.

Lai veiktu šo darbību, skatiet rakstu [Savienotās lietojumprogrammas](e-invoicing-connected-applications.md).
