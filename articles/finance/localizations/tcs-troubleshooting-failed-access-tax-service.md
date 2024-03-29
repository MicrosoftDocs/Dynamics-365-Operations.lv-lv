---
title: Neizdevās piekļūt nodokļu pakalpojumam
description: Šajā rakstā skaidrots, kā novērst problēmu, kas radās, piekļūstot nodokļu aprēķina pakalpojumam.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 65d819b97be3d1238bc0ecfc201b4e24edac8616
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861227"
---
# <a name="failed-to-access-tax-service"></a>Neizdevās piekļūt nodokļu pakalpojumam

[!include [banner](../includes/banner.md)]


Šajā rakstā ir izskaidrots, kā labot nodokļu aprēķināšanas pakalpojuma kļūdu "Neizdevās piekļūt nodokļu pakalpojumiem".

## <a name="symptoms"></a>Simptomi

Microsoft Dynamics 365 Finanses, dodieties uz nodokļu **iestatījumu** \> **nodokļa** \> **konfigurācijas nodokļu** \> **pakalpojuma parametriem.** Cilnē Vispārīgi **iespējojiet** opciju Iespējot **nodokļu aprēķināšanu**. Ja pēc tam mēģiniet atlasīt vērtību laukā **Līdzekļa iestatījuma** nosaukums, rodas kļūda. Kļūdas ziņojums norāda, "Neizdevās piekļūt nodokļu pakalpojumiem."

## <a name="cause"></a>Iemesls

Šī kļūda rodas, jo finanses nevar piekļūt nodokļu aprēķina pakalpojumam.

## <a name="resolution"></a>Novēršana 

1. Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).
2. Vides lapas **cilnē Vides pievienojumprogrammas** atrodiet krājumu Nodokļu **aprēķins** **un pārskatiet tā** statusu. Statusam ir jābūt **Instalēšana vai** Instalēts **·**. Ja nodokļu aprēķina pakalpojuma pievienojumprogramma nav instalēta, saņemsit kļūdas ziņojumu.

## <a name="mitigation"></a>Mazinājums

1. LCS finanšu **lapā**, kas atrodas **Power Platform integrācijas sadaļā**, atlasiet **Instalēt jaunu pievienojumprogrammu**.
2. Ritināt līdz lapas apakšai un atlasiet nodokļu aprēķina **pievienojumprogrammu**, lai to instalētu.
3. Atgriezieties finanšu vidē un mēģiniet piekļūt nodokļu aprēķina pakalpojumam.

> [!NOTE]
> Pirms nodokļu aprēķina pakalpojuma instalēšanas pārskatiet nodokļu aprēķina [pakalpojuma priekšnosacījumus](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Ja nevarat instalēt pievienojumprogrammu, jo **Power platform integrācijas** sadaļa nav pieejama, [skatiet pievienojumprogrammas pārskatu](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Ja pēc pievienojumprogrammas instalēšanas joprojām rodas kļūda, sazinieties ar sistēmas administratoru.
