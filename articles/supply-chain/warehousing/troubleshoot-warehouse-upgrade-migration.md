---
title: Problēmu novēršana saistībā ar jaunināšanu un migrāciju uz uzlaboto noliktavu pārvaldību
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, jauninot un migrējot uz uzlaboto noliktavu pārvaldību.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993892"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Problēmu novēršana saistībā ar jaunināšanu un migrāciju uz uzlaboto noliktavu pārvaldību

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, jauninot un migrējot uz uzlaboto noliktavu pārvaldību.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Tiek parādīts šāds kļūdas ziņojums: "java.security.cert.certPathValidatorException: sertifikācijas ceļa uzticamības enkurs nav atrasts."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts noliktavu programmā, jo pašparakstītie sertifikāti nav uzticami Android 8+ lokālā vidē.

### <a name="issue-resolution"></a>Problēmas risinājums

Izmantojiet ārēju (publisku) sertificēšanas iestādi (CA). Šīs problēmas labojums ir pieejams noliktavu programmas 1.9.0.0 versijā. Plašāku informāciju par šo problēmu un to, kā to novērst, skatiet šeit: [Noliktavu programmas savienojuma problēmu novēršana](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Kāds ir apstiprinātais process pārejai no pamata noliktavas uz papildu noliktavu?

### <a name="issue-description"></a>Problēmas apraksts

Jūs pašlaik darbojaties ar krājumu pārvaldību un izmantojat pamata krājumu funkcionalitāti, un jūs vēlaties pārvietoties uz papildu noliktavu, lai varētu izmantot mobilās ierīces, viļņus un darbu. Tomēr, mēģinot veikt šo pārvietošanos, rodas problēmas. Piemēram, preces nevar mainīt, jo tās izmanto noliktavas dimensijas (vietne, noliktava un atrašanās vieta), jo precēm ir darījumi ar tiem. Tāpēc jums jāiemācās, kāds ir apstiprinātais process pārejai no pamata noliktavas uz papildu noliktavu.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai iegūtu vairāk informācijas par procesu pārejai no pamata noliktavas uz papildu noliktavu, skatiet sekojošos emuāra ierakstos un dokumentācijā:

- [Iespējot noliktavas pārvaldības procesu esošajām precēm un noliktavām](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS migrācija uz jaunu R3 noliktavu un transportēšanas funkcionalitāti](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 krājumu migrācija](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Jaunināt noliktavas pārvaldību no Microsoft Dynamics AX 2012 uz Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]