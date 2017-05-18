---
title: "Importēt valūtas maiņas kursus"
description: "Ja juridiskā persona ir saņēmusi rēķinus ārvalstu valūtās, ārvalstu valūta ir jākonvertē lokālajā valūtā. Tas nozīmē, ka ir nepieciešami jaunākie dažādu valūtu maiņas kursi. Šajā tēmā ir sniegts pārskats par iestatījumiem un apstrādi, kas ir nepieciešami, lai importētu ārvalstu valūtu maiņas kursus, kurus internetā ir publicējuši maiņas kursu nodrošinātāji, piemēram, Eiropas Centrālā banka un Krievijas Centrālā banka."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2b484acdce456de2b45407464267bb3ba083e2ce
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="import-currency-exchange-rates"></a>Importēt valūtas maiņas kursus

[!include[banner](../includes/banner.md)]


Ja juridiskā persona ir saņēmusi rēķinus ārvalstu valūtās, ārvalstu valūta ir jākonvertē lokālajā valūtā. Tas nozīmē, ka ir nepieciešami jaunākie dažādu valūtu maiņas kursi. Šajā tēmā ir sniegts pārskats par iestatījumiem un apstrādi, kas ir nepieciešami, lai importētu ārvalstu valūtu maiņas kursus, kurus internetā ir publicējuši maiņas kursu nodrošinātāji, piemēram, Eiropas Centrālā banka un Krievijas Centrālā banka.

Tālāk esošajās sadaļās ir aprakstīta informācijas plūsma, kas tiek izmantota ārvalstu valūtu maiņas kursu importēšanas iestatīšanai un apstrādei.

## <a name="configure-an-exchange-rate-provider"></a>Maiņas kursu nodrošinātāja konfigurēšana
Lai varētu importēt maiņas kursus, vispirms ir jāiestata informācija, kas ir nepieciešama maiņas kursu nodrošinātājiem. Izmantojiet lapu **Konfigurēt maiņas kursu nodrošinātājus**, lai atlasītu maiņas kursu nodrošinātājus. Daži maiņas kursu nodrošinātāji ir ietverti Microsoft Dynamics 365 for Operations demonstrācijas datu kopā. Tālāk esošajā tabulā ir sniegts lapā pieejamo vadīklu apraksts.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lauks** | **Apraksts**                                                                                                                                                                                                             |
| **Nosaukums**  | Maiņas kursu nodrošinātāja nosaukums.                                                                                                                                                                                     |
| **Atslēga**   | Nodrošinātājam nepieciešamās katras konfigurācijas informācijas daļas unikālais identifikators. Šī informācija tiek automātiski pievienota par katru maiņas kursu nodrošinātāju, ko pievienojat, noklikšķinot uz pogas **Pievienot**. |
| **Vērtība** | Informāciju par katru atslēgu. Šī informācija tiek pievienota par katru maiņas kursu nodrošinātāju, ko pievienojat, noklikšķinot uz pogas **Pievienot**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importēt valūtas maiņas kursus
Lapā **Valūtas maiņas kursi** varat importēt maiņas kursus no maiņas kursu nodrošinātāju avota un iestatīt tos. Izmantojiet lapu **Importēt valūtas maiņas kursus**, lai importētu maiņas kursus. Tālāk esošajā tabulā ir sniegti to failu apraksti, kas ir nepieciešami, lai veiksmīgi pabeigtu importēšanas procesu.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lauks**                              | **Apraksts**                                                                                                                                                                                                                                                                                                                                                             |
| **Maiņas kursa tips**                 | Maiņas kursa tips.                                                                                                                                                                                                                                                                                                                                                      |
| **Maiņas kurus nodrošinātājs**             | Maiņas kursu nodrošinātājs.                                                                                                                                                                                                                                                                                                                                                  |
| **Importēt uz**                       | Izmantojot šo parametru, tiek norādīts, vai importēt datus par šodienu vai datumu diapazonu. Ja vēlaties izmantot datumu diapazonu, ievadiet vai atlasiet sākuma un beigu datumu.                                                                                                                                                                                                                |
| **Izveidot nepieciešamos valūtu pārus**    | Izmantojot šo izvēles rūtiņu, tiek kontrolēta valūtu pāru automātiskā izveide gadījumā, ja importētie valūtu pāri nepastāv. Šī opcija, iespējams, nav pieejama dažiem nodrošinātājiem.                                                                                                                                                                                               |
| **Ignorēt esošos maiņas kursus**   | Izmantojot šo izvēles rūtiņu, tiek kontrolēta valūtu pāra esošā maiņas kursa atjaunināšana gadījumā, ja jau pastāv maiņas kurss konkrētā datumā. Ja šī izvēles rūtiņa nav atzīmēta un jau pastāv cits maiņas kurss konkrētajos datumos, jaunais maiņas kurss netiek importēts.                                                                                       |
| **Novērst importēšanu uz valsts svētku dienām** | Izmantojot šo izvēles rūtiņu, tiek kontrolēts tas, vai ir jāimportē maiņas kurss datumā, kas ir valsts svētku diena. Piemēram, ja šī izvēles rūtiņa ir atzīmēta un kā maiņas kursu nodrošinātājs tiek izmantota Eiropas Centrālā banka, sistēmā netiek atjaunināts maiņas kurss valsts svētku dienā, kas attiecas uz pašreizējo juridisko personu. Šī opcija, iespējams, nav pieejama dažiem nodrošinātājiem. |






