---
title: "Iestatīt drošību Power BI saturam Izmaksu uzskaites analīze"
description: "Šajā tēmā ir paskaidrots, kā var ieviest izmaksu uzskaites piekļuves līmeņa drošību rindas līmeņa drošībai pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, kuriem tiem ir piešķirta piekļuve."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ea4ee6cfdca6e65f289db32ca41305a39b186033
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Iestatīt drošību Power BI saturam Izmaksu uzskaites analīze

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā var ieviest izmaksu uzskaites piekļuves līmeņa drošību rindas līmeņa drošībai pakalpojumā Microsoft Power BI. Šī funkcionalitāte palīdz nodrošināt to, ka lietotāji var skatīt tikai tos Power BI datus, kuriem tiem ir piešķirta piekļuve.

<a name="overview"></a>Pārskats
--------

Microsoft Power BI saturam **Izmaksu uzskaites analīze** tiek izmantota Power BI rindas līmeņa drošība, lai ierobežotu lietotāja piekļuvi. Drošība balstās uz piekļuves līmeņu organizācijas hierarhiju, kas tiek iestatīta Izmaksu uzskaites parametros. Plašāku informāciju par Power BI saturu **Izmaksu uzskaites analīze** skatiet sadaļā [Power BI saturs Izmaksu uzskaites analīze](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Iestatīšana
Lai ieviestu piekļuves līmeņa drošību pakalpojumā Power BI, Power BI satura īpašniekam jāveic šādas darbības. **Piezīme.** Lietotājs, kurš publicē Power BI saturu **Izmaksu uzskaites analīze**, automātiski kļūst par īpašnieku. Tikai īpašnieks var iestatīt drošību pakalpojumā Power BI. Turklāt, kamēr īpašnieks nav pievienojis citus lietotājus vietnē PowerBI.com, neviens, izņemot īpašnieku, nevar skatīt datus Power BI saturā **Izmaksu uzskaites analīze**.

1.  Publicējiet definīciju failu pakalpojumā Power BI.
2.  Pierakstieties vietnē PowerBI.com.
3.  Atrodiet datu kopu Power BI saturam **Izmaksu uzskaites analīze**.
4.  Atveriet drošības lapu. 

    [![Drošības lapas aizvēršana](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Loma **Izmaksu objekta kontrolieris** jau ir izveidota. Pievienojiet citus dalībniekus, kuri ietilpst izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā. 

    [![Dalībnieku pievienošana](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Lietotāji, kuri tiek pievienoti lomai **Izmaksu objekta kontrolieris**, redzēs tikai datus, kurus tiem ir atļauja skatīt, saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņu organizācijas hierarhijā. **Piezīme.** Rindas līmeņa drošība attiecas uz tādiem elementiem un pārskatiem programmā Microsoft Dynamics 365 for Finance and Operations, kuri ir iegulti no pakalpojuma Power BI.

## <a name="updating-security"></a>Drošības atjaunināšana
Ja izmaksu uzskaitē tiek veikti piekļuves līmeņa drošības atjauninājumi un jūs vēlaties, lai tie tiktu atspoguļoti pakalpojumā Power BI, ir jāatjaunina elementu krātuve Power BI saturam **Izmaksu uzskaites analīze**. Pēc tam, kad ir pabeigta elementu krātuves atjaunināšana no Finance and Operations, ir jāatjaunina artefakti vietnē PowerBI.com. Plašāku informāciju par to, kā veikt elementu krātuves atjaunināšanu, skatiet sadaļā [Elementu krātuves atjaunināšana](power-bi-integration-entity-store.md#update-entity-store). Power BI satura **Izmaksu uzskaites analīze** īpašniekam arī jāveic elementu krātuves atjaunināšana, ja jaunajiem lietotājiem tiek piešķirta piekļuve organizācijas hierarhijai. Turklāt īpašniekam jāpievieno jaunie lietotāji lomai **Izmaksu objekta kontrolieris** vietnē PowerBI.com, lai uz tiem attiektos rindas līmeņa drošība.

## <a name="disabling-security"></a>Drošības atspējošana
Mēs pieņemam, ka jūsu organizācija vēlas ierobežot datu piekļuvi. Ja kāda iemesla dēļ, izpildot izmaksu uzskaiti, drošības parametri ir atspējoti, tā vietā īpašniekam ir jāpievieno lietotāji lomai **Izmaksu grāmatvedis** pakalpojumā Power BI. Ja maināt drošību no iespējota stāvokļa uz atspējotu stāvokli, ieteicams noņemt lietotājus no lomas **Izmaksu objekta kontrolieris**. Drošības atkārtotas iespējošanas gadījumā ieteicams veikt pretējas darbības. Lietotājiem var būt abas lomas. Kopīga piekļuve ir abu lomu apvienojums. Power BI satura **Izmaksu uzskaites analīze** gadījumā lietotājiem, kuriem ir kopīga piekļuve, ir neierobežota pieeja datiem. Ja jūsu mērķis ir īstenot ierobežotu piekļuvi, lietotājiem ir jāpiešķir tikai loma **Izmaksu objekta kontrolieris**. Šie rindas līmeņa drošības atjauninājumi stājas spēkā nekavējoties. Ietekmētajiem lietotājiem ir jāatsvaidzina pārlūkprogrammas.

## <a name="additional-resources"></a>Papildu resursi
Lai uzzinātu papildinformāciju par Power BI rindas līmeņa drošību, skatiet rakstu [Drošības pārvaldība jūsu modelim pakalpojumā Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




