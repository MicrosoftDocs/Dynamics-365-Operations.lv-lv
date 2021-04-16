---
title: Valūtas maiņas kursu importēšana
description: Šajā tēmā sniegta informācija par prasībām ārvalstu valūtas atsauces kursu importēšanai, ko publicē maiņas kursu nodrošinātāji.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 20b8496bc3074eae6535eea4cfe0b254f2773e6a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823744"
---
# <a name="import-currency-exchange-rates"></a>Valūtas maiņas kursu importēšana

[!include [banner](../includes/banner.md)]

Ja juridiskā persona ir saņēmusi rēķinus ārvalstu valūtās, ārvalstu valūta ir jākonvertē lokālajā valūtā. Tas nozīmē, ka ir nepieciešami jaunākie dažādu valūtu maiņas kursi. Šajā tēmā ir sniegts pārskats par iestatījumiem un apstrādi, kas ir nepieciešami, lai importētu ārvalstu valūtu maiņas kursus, kurus internetā ir publicējuši maiņas kursu nodrošinātāji, piemēram, Eiropas Centrālā banka un Krievijas Centrālā banka.

Tālāk esošajās sadaļās ir aprakstīta informācijas plūsma, kas tiek izmantota ārvalstu valūtu maiņas kursu importēšanas iestatīšanai un apstrādei.

## <a name="configure-an-exchange-rate-provider"></a>Maiņas kursu nodrošinātāja konfigurēšana
Lai varētu importēt maiņas kursus, vispirms ir jāiestata informācija, kas ir nepieciešama maiņas kursu nodrošinātājiem. Izmantojiet lapu **Konfigurēt maiņas kursu nodrošinātājus**, lai atlasītu maiņas kursu nodrošinātājus. Dynamics 365 Finance demonstrācijas datu kopā ir ietverti maiņas kursu nodrošinātāji. Tālāk esošajā tabulā ir sniegts lapā pieejamo vadīklu apraksts.

| Lauks | Apraksts                   |
|-----------|-----------------------------------|
| **Nosaukums**  | Maiņas kursu nodrošinātāja nosaukums.                                                                                                                                                                                     |
| **Atslēga**   | Nodrošinātājam nepieciešamās katras konfigurācijas informācijas daļas unikālais identifikators. Šī informācija tiek automātiski pievienota katram maiņas kursu nodrošinātājam, kurš tiek pievienots. |
| **Value** | Informāciju par katru atslēgu. Šī informācija tiek pievienota katram maiņas kursu nodrošinātājam, kurš tiek pievienots.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valūtas maiņas kursu importēšana
Varat importēt maiņas kursus no maiņas kursu nodrošinātāju avota un tos pievienot lapai **Valūtas maiņas kursi**. Izmantojiet lapu **Importēt valūtas maiņas kursus**, lai importētu maiņas kursus. Tālāk esošajā tabulā ir sniegti to failu apraksti, kas ir nepieciešami, lai veiksmīgi pabeigtu importēšanas procesu.

| Lauks | Apraksts                   |
|-----------|-----------------------------------|
| **Maiņas kursa tips**                 | Maiņas kursa tips.                                                                                                                                                                                                                                                                                                                                                      |
| **Maiņas kurus nodrošinātājs**             | Maiņas kursu nodrošinātājs.                                                                                                                                                                                                                                                                                                                                                  |
| **Importēt uz**                       | Izmantojot šo parametru, tiek norādīts, vai importēt datus par šodienu vai konkrētu datumu diapazonu. Ja vēlaties izmantot datumu diapazonu, ievadiet vai atlasiet sākuma un beigu datumu.                                                                                                                                                                                                                |
| **Izveidot nepieciešamos valūtu pārus**    | Izmantojot šo izvēles rūtiņu, tiek kontrolēta valūtu pāru automātiskā izveide gadījumā, ja importētie valūtu pāri nepastāv. Šī opcija, iespējams, nav pieejama dažiem nodrošinātājiem.                                                                                                                                                                                               |
| **Ignorēt esošos maiņas kursus**   | Izmantojot šo izvēles rūtiņu, tiek kontrolēta valūtu pāra esošā maiņas kursa atjaunināšana gadījumā, ja jau pastāv maiņas kurss konkrētā datumā. Ja šī izvēles rūtiņa nav atzīmēta un jau pastāv cits maiņas kurss konkrētajos datumos, jaunais maiņas kurss netiek importēts.                                                                                       |
| **Novērst importēšanu uz valsts svētku dienām** | Izmantojot šo izvēles rūtiņu, tiek kontrolēts tas, vai ir jāimportē maiņas kurss datumā, kas ir svētku diena. Piemēram, ja šī izvēles rūtiņa ir atzīmēta un kā maiņas kursu nodrošinātājs tiek izmantota Eiropas Centrālā banka, sistēmā netiek atjaunināts maiņas kurss valsts svētku dienā, kas attiecas uz pašreizējo juridisko personu. Šī opcija, iespējams, nav pieejama dažiem nodrošinātājiem. |
| **Maiņas kurss no iepriekšējās dienas** | Šī izvēles rūtiņa ir pieejama, ja iespējojat līdzekli **ECB importēšana uz pašreizējo vai iepriekšējo datumu** lapā **Līdzekļu pārvaldība**. Šī izvēles rūtiņa ir pieejama tikai nodrošinātājam, *Eiropas Centrālajai bankai*. Atzīmējiet šo izvēles rūtiņu, lai importētu valūtas maiņas kursu, ko Eiropas Centrālā banka ir publicējusi iepriekšējā darba dienā aptuveni plkst. 16:00 pēc Centrāleiropas laika. Pēc noklusējuma šī izvēles rūtiņa ir atzīmēta. Notīriet šo izvēles rūtiņu, lai importētu valūtas maiņas kursu, kas ir publicēts tajā pašā darba dienā.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]