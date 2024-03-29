---
title: Drošības iestatīšana Power BI saturam “Izmaksu uzskaites analīze”
description: Šajā rakstā skaidrots, kā var ieviest piekļuves līmeņa drošību Izmaksu uzskaitē rindas līmeņa drošībai Microsoft Power BI.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267938"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Drošības iestatīšana Power BI saturam “Izmaksu uzskaites analīze”

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā var ieviest piekļuves līmeņa drošību Izmaksu uzskaitē rindas līmeņa drošībai Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, attiecībā uz kuriem viņiem ir piešķirtas piekļuves tiesības.

## <a name="overview"></a>Pārskats

Lai ierobežotu lietotāja piekļuvi Microsoft Power BI saturam pakotnei **Izmaksu uzskaites analīze**, tiek izmantota Power BI rindas līmeņa drošība. Drošība balstās uz piekļuves līmeņu organizācijas hierarhiju, kas tiek iestatīta Izmaksu uzskaites parametros. Papildinformāciju par Power BI satura pakotni **Izmaksu uzskaites analīze** skatiet rakstā [Pakalpojuma Power BI satura pakotne Izmaksu uzskaites analīze](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Iestatījumi
Lai ieviestu piekļuves līmeņa drošību pakalpojumā Power BI, Power BI satura pakotnes īpašniekam ir jāizpilda tālāk norādītās darbības.

> [!NOTE]
> Lietotājs, kurš publicē Power BI satura pakotni **Izmaksu uzskaites analīze**, automātiski kļūst par tās īpašnieku. Tikai īpašnieks var iestatīt drošību pakalpojumā Power BI. Turklāt, kamēr īpašnieks nav pievienojis citus lietotājus vietnē PowerBI.com, neviens cits, izņemot īpašnieku, nevar skatīt Power BI satura pakotnē **Izmaksu uzskaites analīze** ietvertos datus.

1. Publicējiet definīciju failu pakalpojumā Power BI.
2. Pierakstieties vietnē PowerBI.com.
3. Atrodiet Power BI satura pakotnes **Izmaksu uzskaites analīze** datu kopu.
4. Atveriet drošības lapu.

    ![Drošības lapas atvēršana.](./media/CA-picture-1.png)

5. Loma **Izmaksu objekta kontrolieris** jau ir izveidota. Pievienojiet citus dalībniekus, kuri ietilpst izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.

    ![Dalībnieku pievienošana.](./media/CA-picture-2.png)

Lietotāji, kuri tiek pievienoti lomai **Izmaksu objekta kontrolieris**, redzēs tikai datus, kurus tiem ir atļauja skatīt, saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā.

> [!NOTE]
> Elementiem un pārskatiem, kas ir iegulti no pakalpojuma Power BI, tiek lietota rindas līmeņa drošība.

## <a name="updating-security"></a>Drošības atjaunināšana
Ja tiek veikti moduļa Izmaksu uzskaite piekļuves līmeņa drošības atjauninājumi un vēlaties tos lietot pakalpojumā Power BI, ir jāatjaunina Power BI satura pakotnes **Izmaksu uzskaites analīze** elementu krātuve. Pēc tam, kad ir pabeigta elementu krātuves atjaunināšana, ir jāatjaunina artefakti vietnē PowerBI.com. Plašāku informāciju par to, kā veikt elementu krātuves atjaunināšanu, skatiet sadaļā [Power BI integrācija ar Elementu krātuvi](power-bi-integration-entity-store.md#update-entity-store). Power BI satura pakotnes **Izmaksu uzskaites analīze** īpašniekam ir jāatjaunina elementu krātuve arī tad, ja jauniem lietotājiem tiek piešķirtas tiesības piekļūt organizācijas hierarhijai. Turklāt īpašniekam jāpievieno jaunie lietotāji lomai **Izmaksu objekta kontrolieris** vietnē PowerBI.com, lai uz tiem attiektos rindas līmeņa drošība.

## <a name="disabling-security"></a>Drošības atspējošana
Mēs pieņemam, ka jūsu organizācija vēlas ierobežot datu piekļuvi. Ja, izpildot moduli Izmaksu uzskaite, kāda iemesla dēļ ir atspējoti drošības parametri, tā vietā īpašniekam ir jāpievieno lietotāji lomai **Izmaksu grāmatvedis** pakalpojumā Power BI. Ja maināt drošību no iespējota stāvokļa uz atspējotu stāvokli, ieteicams noņemt lietotājus no lomas **Izmaksu objekta kontrolieris**. Drošības atkārtotas iespējošanas gadījumā ieteicams veikt pretējas darbības. Lietotājiem var būt abas lomas. Kopīga piekļuve ir abu lomu apvienojums. Power BI satura pakotnes **Izmaksu uzskaites analīze** gadījumā lietotāji, kuriem ir piešķirta kopīga piekļuve, var piekļūt datiem bez ierobežojumiem. Ja jūsu mērķis ir īstenot ierobežotu piekļuvi, lietotājiem ir jāpiešķir tikai loma **Izmaksu objekta kontrolieris**. Šie rindas līmeņa drošības atjauninājumi stājas spēkā nekavējoties. Ietekmētajiem lietotājiem ir jāatsvaidzina pārlūkprogrammas.

## <a name="additional-resources"></a>Papildu resursi
Papildinformāciju par Power BI rindas līmeņa drošību skatiet rakstā [Modeļa drošības pārvaldība modelim pakalpojumā Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
