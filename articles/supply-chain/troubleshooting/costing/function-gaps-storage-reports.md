---
title: Funkcionālas starpības starp krājuma vērtības / klasifikācijas pēc terminiem atskaitēm un to glabāšanas versijām
description: Funkcionālas starpības starp krājuma vērtības / klasifikācijas pēc terminiem atskaitēm un to glabāšanas versijām
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686658"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funkcionālas starpības starp krājuma vērtības / klasifikācijas pēc terminiem atskaitēm un to glabāšanas versijām

[Krājumu novecošanās pārskata uzglabāšanas](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) un [Krājumu vērtības uzglabāšanas pārskata](/dynamics365/supply-chain/cost-management/inventory-value-report-storage) līdzekļi iespējo Supply Chain Management, lai parādītu lielus krājumu darbību apjomus. Katrā gadījumā pārskata rezultāti tiek saglabāti pārlūkošanai un eksportēšanai, atšķirībā no šo pārskatu neuzglabāšanas versijām. Tomēr dažas funkcionalitātes, kas pastāv šo pārskatu neuzglabāšanas versijās, glabāšanas versijās nepastāv. Sekojošās apakšsadaļās ir apkopotas atšķirības un sniegti risinājumi.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Krātuves pārskatos netiek iekļautas apakšsummas, pat ja tās ir iespējotas pārskata izkārtojumā

Apakšsummas var radīt problēmas, ja rezultāts tiek eksportēts, it īpaši, ja lietotāji maina ieraksta secību.

Lai pārbaudītu apakšsummas, varat eksportēt rezultātu uz Microsoft Excel. Vai arī, ja vēlaties pārbaudīt apakšsummas Supply Chain Management, izmantojiet [Līdzekļu pārvaldību](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview), lai iespējotu *Jauno režģu kontroli* un *Grupēšanu režģos* līdzekļus, kas nodrošina daudz elastīgāku veidu, kā apskatīt jebkuras grupas apakšsummu pēc kolonnas. Plašāku informāciju skatiet sadaļā [Režģa iespējas](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Krājumu vērtības uzglabāšanas pārskats neatbalsta virsgrāmatas konta informāciju

Varat palaist apgrozījuma bilanci, lai iegūtu krājumu kontu bilanci un salīdzināt to ar **Krājumu vērtības uzglabāšanas** pārskatu.
