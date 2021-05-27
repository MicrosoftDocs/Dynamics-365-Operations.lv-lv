---
title: Nevar lietot veidni izlaistai precei
description: Nevar lietot veidni izlaistai precei.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026704"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Nevar lietot veidni, lai izveidotu izlaistu preci

KB numurs: 4612097

## <a name="symptoms"></a>Simptomi

Kad izveidojat jaunu izlaisto preci, izmantojot dialoglodziņu **Jauna izlaistā prece**, var atlasīt veidni. Veidnei jānodrošina noklusējuma iestatījumi daudziem jaunās izlaistās preces laukiem. Tomēr pēc veidnes atlases daži vai visi lauki nav iestatīti.

## <a name="cause"></a>Iemesls

Daudzas Microsoft Dynamics 365 Supply Chain Management lapas ļauj izveidot veidni, kas nosaka sākotnējos iestatījumus ierakstiem, kas tiek rādīti šajās lapās. Vienu no šīm veidnēm varat izveidot, Darbību rūtī atlasot **Ieraksta informāciju** cilnē **Opcijas**. Tomēr izlaistās preces ir daudz sarežģītākas nekā vairums citu ierakstu veidu. Lai gan jūs varat atlasīt **Ieraksta informāciju** lapā **Izlaistās preces** lai izveidotu veidni, un, lai gan varat atlasīt šo veidni, kad izveidojat izlaisto preci, veidne neļaus sniegt prognozētās lauka vērtības jaunajai izlaistajai precei. Tādēļ izlaistajām precēm nevar izmantot "ieraksta informācijas" veidnes. Tā vietā ir jāizveido atvēlētas preču veidnes.

## <a name="resolution"></a>Novēršana

Lai izveidotu preces veidni, darbību rūts cilnē **Produkts** izmantojiet izvēlni **Veidne**, nevis pogu **Ieraksta informācija** cilnē **Opcijas**.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Darbību rūts cilnes **Produkts** grupā **Jauns** atlasiet **Veidne**, un pēc tam, ja nepieciešams, atlasiet **Izveidot personisko veidni** vai **Izveidot koplietotu veidni**.
