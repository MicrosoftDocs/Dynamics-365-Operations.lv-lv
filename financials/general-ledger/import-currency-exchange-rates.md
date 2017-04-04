---
title: "Importēt valūtas maiņas kursus"
description: "Ja juridiska persona, kas saņēmusi rēķinus ārvalstu valūtās, ir nepieciešams ārvalstu valūtā konvertē vietējā valūtā. Tas nozīmē, ka ir nepieciešams jaunāko valūtas maiņas kursiem attiecībā uz dažādām valūtām. Šajā tēmā ir sniegts pārskats par nepieciešamos uzstādījumus un apstrādes importēšanai internetā publicēto valūtas kursu sniedzēji, piemēram, Eiropas centrālo banku un Krievijas centrālās bankas ārvalstu valūtas atsauces likmēm."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Importēt valūtas maiņas kursus

Ja juridiska persona, kas saņēmusi rēķinus ārvalstu valūtās, ir nepieciešams ārvalstu valūtā konvertē vietējā valūtā. Tas nozīmē, ka ir nepieciešams jaunāko valūtas maiņas kursiem attiecībā uz dažādām valūtām. Šajā tēmā ir sniegts pārskats par nepieciešamos uzstādījumus un apstrādes importēšanai internetā publicēto valūtas kursu sniedzēji, piemēram, Eiropas centrālo banku un Krievijas centrālās bankas ārvalstu valūtas atsauces likmēm.

Nākamajās sadaļās ir aprakstīts, informāciju, kas tiek izmantota iestatīšanas un apstrādes ārvalstu valūtas maiņas likmēm importa plūsmas.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurēt valūtas kursa nodrošinātājs
Pirms importējat kursus, ir jāuzstāda informācija, kas nepieciešama pakalpojumu sniedzēji, kuri piedāvā kursus. Izmantojiet **konfigurēt kursu sniedzēji** lapu, lai izvēlētos valūtas kursu sniedzēji. Daži pakalpojumu sniedzēji kurss ir iekļautas ar demo datus Microsoft Dynamics 365 operācijām. Šajā tabulā ir sniegti šajā lapā kontroļu apraksti.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Maiņas kursu nodrošinātāja nosaukums.                                                                                                                                                                                     |
| **Atslēga**   | Nodrošinātājam nepieciešamās katras konfigurācijas informācijas daļas unikālais identifikators. Šī informācija tiek automātiski pievienota katram valūtas kursa nodrošinātājam, ko pievienojat, noklikšķinot uz **pievienot** pogu. |
| **Value** | Informāciju par katru atslēgu. Šī informācija tiek pievienota katram valūtas kursa nodrošinātājam, ko pievienojat, noklikšķinot uz **pievienot** pogu.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importēt valūtas maiņas kursus
Varat importēt valūtas maiņas kursu valūtas kursu sniedzēji avots un iestatīt **valūtas kursi** lapā. Lietošanas **importēt valūtas kursi** lapu, lai importētu valūtas maiņas kursus. Tabulā ir sniegti apraksti lauki, kas nepieciešami, lai veiksmīgi pabeigtu importēšanas procesu.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Kursa tipu.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Valūtas kursa nodrošinātājs.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Šis parametrs pārvalda vai importēt no šodienas datumu vai datumu diapazonu. Ja vēlaties izmantot datu diapazonu, ievadiet vai izvēlieties sākuma un beigu datumus.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Šo izvēles rūtiņu, vada automātisko izveidi valūtas pāros, ja nepastāv valūtu pāriem, kas tiek importēti. Šī opcija var nebūt pieejama daži pakalpojumu sniedzēji.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Šo izvēles rūtiņu, pārvalda Atjaunināt esošo maiņas kursu valūtas pāri, kad kurss noteiktam datumam jau pastāv. Ja neatzīmēsit šo izvēles rūtiņu, maiņas kursu konkrētiem datumiem netiek importēti, ja cits kurss jau pastāv.                                                                                       |
| **Prevent import on national holiday** | Šo izvēles rūtiņu, pārvalda valūtas kursa ievešanas datumu, kas ir valsts svētku diena. Piemēram, ja tiek atzīmēta šī izvēles rūtiņa un izmantot Eiropas Centrālās bankas valūtas kursa nodrošinātājs, sistēma netiek atjaunināts valūtas kursu par valsts svētku dienā, kas ir saistīti ar pašreizējās juridiskās personas. Šī opcija var nebūt pieejama daži pakalpojumu sniedzēji. |




