---
title: Konfigurēt pakalpojumu vides un savienotās programmas
description: Šajā rakstā ir sniegta informācija, kā konfigurēt jūsu pakalpojumu vides un pievienotās programmas.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269537"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigurēt pakalpojumu vides un savienotās programmas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kā konfigurēt jūsu pakalpojumu vides un pievienotās programmas. Šim procesam ir trīs soļi. 1. solis ir obligāts, un 2. un 3. darbība nav obligāta.

## <a name="step-1-create-a-service-environment"></a>1. darbība: pakalpojumu vides izveide

Kad jūs izveidojat savu pakalpojumu vidi, definējiet lietotāju sarakstu, kas var tajā izvietot globalizācijas līdzekļus. Pēc izvēles dažiem scenārijiem definējiet ārējo programmu sarakstu, kas var sazināties ar elektronisko rēķinu izrakstīšanas pakalpojumu. Iestatiet numuru secības, ja izmantosiet tās scenārijos.

Lai veiktu šo darbību, skatiet [pakalpojumu vides](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2. darbība: sertifikātu un slepeno vienumu pievienošana

Pievienojiet atsauci atslēgai laties Microsoft Azure un noslēpumiem, lai tos izmantotu scenārijos. Šis solis ir obligāts, ja darbības konveijera apstrādē izmanto sertifikātus un noslēpumus ciparparakstam vai komunikācijai ar ārējiem tīmekļa pakalpojumiem.

Lai veiktu šo darbību, skatiet debitora [sertifikātus un noslēpumus](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3. darbība: pievienoto programmu konfigurēšana

Lai iestatītu komunikāciju starp Dynamics 365 Dynamics 365 Supply Chain Management finansēm vai programmām un elektronisko rēķinu izrakstīšanu, jākonfigurē Finanšu vai piegādes ķēdes pārvaldība, lai veidotu izsaukumu uz Elektronisko rēķinu izrakstīšanu un sagatavotu biznesa datus vienotā struktūrā, kas var tikt pārvērsta nepieciešamajā elektroniskajā formātā. Programmām arī pareizi jāapstrādā pakalpojuma atbildes. Varat pabeigt šo konfigurāciju tieši jūsu Finanšu vai piegādes ķēdes pārvaldības vidē, vai varat pabeigt to Regulēšanas konfigurācijas pakalpojumā (RCS). Ja konfigurāciju aizpildīsiet RCS, varat to izvietot jūsu Finanšu vai piegādes ķēdes pārvaldības vidē. Šajā solī reģistrēsiet pievienoto programmu parametru izvietošanai.

Lai pabeigtu šo soli, skatiet Piesaistītās [programmas](e-invoicing-connected-applications.md).
