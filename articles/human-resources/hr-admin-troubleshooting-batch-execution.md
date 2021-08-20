---
title: Iestrēgušu pakešuzdevumu atiestatīšana
description: Šajā tēmā ir paskaidrots, kā atrisināt problēmas, kas saistītas ar iestrēgušajiem pakešuzdevumiem.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: c8b80406991bab6ba87fc8e38b9e49391921d98df5dbf223561848157f8f419d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738347"
---
# <a name="reset-stuck-batch-jobs"></a>Iestrēgušu pakešuzdevumu atiestatīšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Izsniegt

Microsoft Dynamics 365 Human Resources var rasties problēmas ar pakešuzdevumiem, kas ir iestrēguši stāvoklī **Izpilde** vai **Atcelšana** un nav pabeigti.

## <a name="resolution"></a>Novēršana

Ja pakešuzdevums ir iestrēdzis stāvoklī **Izpilde** vai **Atcelšana**, varat atiestatīt statusu, liekot atcelt darbu. Pēc pakešuzdevuma atcelšanas to var atiestatīt, iestatot statusu **Gaida**. Pēc tam tas tiks atkal paņemts izpildei nākamajā plānotajā pakešizpildes reizē.

1. Darbvietā **Sistēmas administrēšana** atlasiet lapu **Saites** un atlasiet **Pakešuzdevumi**.

2. Saraksta lapā **Pakešuzdevumi** atlasiet darbu, kas ir jāatiestata.

3. Darbību lentē atlasiet **Piespiedu atcelšana** un apstipriniet darbību.

   > [!NOTE]
   > Darbība **Piespiedu atcelšana** ir pieejama tikai tad, ja atlasītajam pakešuzdevumam ir statuss **Izpilde** vai **Atcelšana** un šim darbam netiek palaisti pakešveida izpildes vai atcelšanas procesi.

4. Uz darbības lentesatlasiet **Mainīt statusu**.

5. Lapā **Atlasīt jaunu statusu** atlasiet **Gaida** un pēc tam atlasiet **Labi**.

   ![Atlasīt jaunu pakešuzdevuma statusu.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Skatiet arī

[Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba laika](hr-admin-troubleshooting-batch-jobs.md)<br>
[Veiktspējas optimizēšana, izmantojot automātiskās tīrīšanas uzdevumus](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
