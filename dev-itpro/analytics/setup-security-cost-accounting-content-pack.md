---
title: "Izmaksu uzskaites analīze Power BI satura drošības iestatīšana"
description: "Šajā tēmā ir paskaidrots, kā var izplatīt piekļuves līmeņa drošību rindu līmeņa drošības Microsoft Power BI izmaksu uzskaitē. Šī funkcionalitāte palīdz garantēt, ka lietotāji redz tikai varas BI dati, kas tiem nodrošina piekļuvi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Izmaksu uzskaites analīze Power BI satura drošības iestatīšana

Šajā tēmā ir paskaidrots, kā var izplatīt piekļuves līmeņa drošību rindu līmeņa drošības Microsoft Power BI izmaksu uzskaitē. Šī funkcionalitāte palīdz garantēt, ka lietotāji redz tikai varas BI dati, kas tiem nodrošina piekļuvi.

<a name="overview"></a>Pārskats
--------

**Izmaksu uzskaites analīze** Microsoft Power BI saturu izmanto strāvas BI rindu līmeņa drošības ierobežot lietotāju piekļuvi. Drošības pamatā ir izmaksu uzskaites parametros ir iestatīt piekļuves līmeni organizācijas hierarhijai. Plašāku informāciju par **izmaksu uzskaites analīze** Power BI saturu, sk [izmaksu uzskaites analīze Power BI saturu](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Iestatīšana
Izplatīt jauda BI piekļuves līmeņa drošību, jaudu BI satura īpašnieks nedrīkst rīkojieties šādi. **Piezīme:** lietotājs, kas publicē **izmaksu uzskaites analīze** Power BI saturs automātiski kļūst par īpašnieku. Tikai īpašnieks var uzstādīt drošības varas BI. Turklāt, līdz brīdim, kad īpašnieks pievieno citiem lietotājiem PowerBI.com, neviens izņemot īpašnieks var redzēt visus datus **izmaksu uzskaites analīze** BI enerģijas saturu.

1.  Definīcijas failu publicēšana Power BI.
2.  Pieteikties līdz PowerBI.com.
3.  Atrast datu kopu par **izmaksu uzskaites analīze** BI enerģijas saturu.
4.  Atveriet lapu drošības. 

    [![Atverot lapu drošība](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  **Izmaksas objekta kontrolieris** lomu jau ir izveidots. Pievienot citus dalībniekus, kuri ir daļa no izmaksu uzskaites piekļuves līmeņa organizācijas hierarhijai. 

    [![Dalībnieku pievienošana](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Lietotājiem, kuri pievienoti **izmaksas objekta kontrolieris** lomu redzēs tikai tos datus, kurus viņiem atļauts apskatīt saskaņā ar definīciju izmaksu uzskaites piekļuves līmeņa organizācijas hierarhijai. **Piezīme:** rindu līmeņa drošība attiecas uz flīzēm un ziņo Microsoft Dynamics 365 operācijām, kas iegultas no varas BI.

## <a name="updating-security"></a>Atjaunināšanu, drošības
Ja atjauninājumi tiek veikti drošības piekļuves līmeni izmaksu uzskaitē un varas BI, lai atspoguļotu šos atjauninājumus, jums ir jāatjaunina entītiju veikalu **izmaksu uzskaites analīze** BI enerģijas saturu. Pēc pabeigšanas uzņēmums veikals update no Dynamics 365 operācijām, jums ir jāatjaunina artefakti uz PowerBI.com. Lai iegūtu plašāku informāciju par entītiju veikalā atjauninājumu, skatiet [Update entītiju veikala](power-bi-integration-entity-store.md#update-entity-store). Īpašnieks, **izmaksu uzskaites analīze** Power BI saturs arī ir jādara entītiju veikalā atjauninājumu, ja jauniem lietotājiem ir piešķirta piekļuve sistēmai organizācijas hierarhijai. Turklāt īpašnieks nedrīkst pievienot jaunus lietotājus, lai **izmaksas objekta kontrolieris** PowerBI.com, tāpēc tos pielieto šo rindu līmeņa drošības lomas.

## <a name="disabling-security"></a>Atspējot drošības
Mēs pieņemam, ka jūsu organizācija vēlas ierobežot piekļuvi datiem. Ja kāda iemesla dēļ drošības parametri tiek atspējoti, palaižot izmaksu uzskaites, īpašnieks nedrīkst pievienot lietotājus, kuriem ir **izmaksu grāmatvede** lomu varas BI vietā. Ja maināt drošības iespējots valsts atspējotajā stāvoklī, tā ir laba ideja, lai noņemt lietotājus no **izmaksas objekta kontrolieris** lomu. Un otrādi, ja jūs atkārtoti iespējot drošību. Lietotāji var piederēt gan lomas. Kopīga pieeja ir Savienības abām lomām. Gadījumā, ja **izmaksu uzskaites analīze** Power BI satura kopīgu pieeju lietotājiem ir neierobežota piekļuve datiem. Ja jūsu mērķis ir piemērot ierobežotas pieejamības, lietotāji, jāpiešķir tikai tiem **izmaksas objekta kontrolieris** lomu. Šo rindu līmeņa drošības atjauninājumus stājas spēkā nekavējoties. Ieinteresētos lietotājus būtu atsvaidziniet pārlūkprogrammu.

## <a name="additional-resources"></a>Papildu resursi
Lai uzzinātu vairāk par varas BI rindu līmeņa drošību, skatiet [pārvaldītu drošību jūsu modeli Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


