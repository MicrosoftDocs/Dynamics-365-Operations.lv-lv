---
title: Power BI satura pakotnes Izmaksu uzskaites analīze drošības iestatīšana
description: Šajā tēmā ir paskaidrots, kā varat pārnest moduļa Izmaksu uzskaite piekļuves līmeņa drošību uz rindas līmeņa drošību pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, attiecībā uz kuriem viņiem ir piešķirtas piekļuves tiesības.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1cd378a58d4a4fe4388238f97e84a8e2b07937b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551464"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Power BI satura pakotnes Izmaksu uzskaites analīze drošības iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā varat pārnest moduļa Izmaksu uzskaite piekļuves līmeņa drošību uz rindas līmeņa drošību pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, attiecībā uz kuriem viņiem ir piešķirtas piekļuves tiesības.

## <a name="overview"></a>Pārskats

Lai ierobežotu lietotāja piekļuvi Microsoft Power BI saturam pakotnei **Izmaksu uzskaites analīze**, tiek izmantota Power BI rindas līmeņa drošība. Drošība balstās uz piekļuves līmeņu organizācijas hierarhiju, kas tiek iestatīta Izmaksu uzskaites parametros. Papildinformāciju par Power BI satura pakotni **Izmaksu uzskaites analīze** skatiet rakstā [Power BI satura pakotne Izmaksu uzskaites analīze](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Iestatījumi
Lai ieviestu piekļuves līmeņa drošību pakalpojumā Power BI, Power BI satura pakotnes īpašniekam ir jāizpilda tālāk norādītās darbības.

> [!NOTE]
> Lietotājs, kurš publicē Power BI satura pakotni **Izmaksu uzskaites analīze**, automātiski kļūst par tās īpašnieku. Tikai īpašnieks var iestatīt drošību pakalpojumā Power BI. Turklāt, kamēr īpašnieks nav pievienojis citus lietotājus vietnē PowerBI.com, neviens cits, izņemot īpašnieku, nevar skatīt Power BI satura pakotnē **Izmaksu uzskaites analīze** ietvertos datus.

1. Publicējiet definīciju failu pakalpojumā Power BI.
2. Pierakstieties vietnē PowerBI.com.
3. Atrodiet Power BI satura pakotnes **Izmaksu uzskaites analīze** datu kopu.
4. Atveriet drošības lapu.

    ![Drošības lapas atvēršana](./media/CA-picture-1.png)

5. Loma **Izmaksu objekta kontrolieris** jau ir izveidota. Pievienojiet citus dalībniekus, kuri ietilpst izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.

    ![Dalībnieku pievienošana](./media/CA-picture-2.png)

Lietotāji, kuri tiek pievienoti lomai **Izmaksu objekta kontrolieris**, redzēs tikai datus, kurus tiem ir atļauja skatīt, saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.

> [!NOTE]
> Microsoft Dynamics 365 for Finance and Operations elementiem un pārskatiem, kas ir iegulti no pakalpojuma Power BI, tiek lietota rindas līmeņa drošība.

## <a name="updating-security"></a>Drošības atjaunināšana
Ja tiek veikti moduļa Izmaksu uzskaite piekļuves līmeņa drošības atjauninājumi un vēlaties tos lietot pakalpojumā Power BI, ir jāatjaunina Power BI satura pakotnes **Izmaksu uzskaites analīze** elementu krātuve. Pēc tam, kad ir pabeigta elementu krātuves atjaunināšana no Finance and Operations, ir jāatjaunina artefakti vietnē PowerBI.com. Plašāku informāciju par to, kā veikt elementu krātuves atjaunināšanu, skatiet sadaļā [Elementu krātuves atjaunināšana](power-bi-integration-entity-store.md#update-entity-store). Power BI satura pakotnes **Izmaksu uzskaites analīze** īpašniekam ir jāatjaunina elementu krātuve arī tad, ja jauniem lietotājiem tiek piešķirtas tiesības piekļūt organizācijas hierarhijai. Turklāt īpašniekam jāpievieno jaunie lietotāji lomai **Izmaksu objekta kontrolieris** vietnē PowerBI.com, lai uz tiem attiektos rindas līmeņa drošība.

## <a name="disabling-security"></a>Drošības atspējošana
Mēs pieņemam, ka jūsu organizācija vēlas ierobežot datu piekļuvi. Ja, izpildot moduli Izmaksu uzskaite, kāda iemesla dēļ ir atspējoti drošības parametri, tā vietā īpašniekam ir jāpievieno lietotāji lomai **Izmaksu grāmatvedis** pakalpojumā Power BI. Ja maināt drošību no iespējota stāvokļa uz atspējotu stāvokli, ieteicams noņemt lietotājus no lomas **Izmaksu objekta kontrolieris**. Drošības atkārtotas iespējošanas gadījumā ieteicams veikt pretējas darbības. Lietotājiem var būt abas lomas. Kopīga piekļuve ir abu lomu apvienojums. Power BI satura pakotnes **Izmaksu uzskaites analīze** gadījumā lietotāji, kuriem ir piešķirta kopīga piekļuve, var piekļūt datiem bez ierobežojumiem. Ja jūsu mērķis ir īstenot ierobežotu piekļuvi, lietotājiem ir jāpiešķir tikai loma **Izmaksu objekta kontrolieris**. Šie rindas līmeņa drošības atjauninājumi stājas spēkā nekavējoties. Ietekmētajiem lietotājiem ir jāatsvaidzina pārlūkprogrammas.

## <a name="additional-resources"></a>Papildu resursi
Papildinformāciju par Power BI rindas līmeņa drošību skatiet rakstā [Modeļa drošības pārvaldība modelim pakalpojumā Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).
