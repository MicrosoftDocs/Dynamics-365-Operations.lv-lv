---
title: Abonementa darbplūsmas apskats
description: Šajā tēmā ir sniegts apskats par abonementa darbplūsmu.
author: sorenva
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cbb986b9e7496975df076f473b828a023548560
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670669"
---
# <a name="subscription-workflow-overview"></a>Abonementa darbplūsmas apskats 

[!include [banner](../includes/banner.md)]


Jūs esat abonementa administrators apgaismojuma uzņēmumā, kurš piedāvā abonementu apgaismojuma ierīču apkopei. Klients sazinās ar jūsu uzņēmumu, lai iegādātos gada abonementu apgaismojuma ierīču apkopei.

## <a name="setting-up-subscriptions"></a>Abonementu iestatīšana

Lai iestatītu abonementu, vispirms jums ir jāizveido abonementu grupa jaunajam pakalpojumu līgumam vai ir jāapstiprina, ka šāda abonementu grupa jau pastāv. Ja abonementu grupa jau pastāv, jums tā ir jāiestata, lai klientam reizi gadā tiktu izrakstīts rēķins un lai pārdošanas ieņēmumus uzkrātu par katru gada mēnesi. Plašāku informāciju par to, kā iestatīt abonementus, skatiet tēmā [Abonementu grupu iestatīšana](set-up-subscription-groups.md).

Kad abonementu grupa ir izveidota, varat izveidot abonementu. Plašāku informāciju par to, kā izveidot pakalpojumu abonementus, skatiet tēmā [Pakalpojumu abonementu izveidošana no abonementu grupas](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Abonementu transakciju izveidošana un modificēšana

Pēc abonementa iestatīšanas varat izveidot abonēšanas maksas transakciju pirmajam rēķina periodam, kas ir viens gads. Transakciju veids ir **Regulārs**. Tādēļ varat izveidot tikai tādas abonementu transakcijas, kur datums No un datums Līdz atbilst periodiem, kurus iepriekš izveidojāt formā **Periodu veidi**. Plašāku informāciju par maksas transakcijām skatiet tēmā [Abonēšanas maksas transakciju izveidošana](create-subscription-fee-transactions.md).

Kad savam klientam esat iestatījis abonementu, jūs atceraties, ka esat vienojies par 10 procentu atlaidi visām pakalpojumu piedāvājumu cenu sistēmā iestatītajām cenām. Tādēļ jums ir jāsamazina izveidotās transakcijas maksas cena.

Vēlāk tajā pašā dienā jūsu klienta kontaktpersona jums zvana, lai pastāstītu, ka, lai gan viņi joprojām vēlas noslēgt līgumu par apgaismojuma ierīču apkopi, tajā pašā gadā viņi vēlāk plāno ieviest jaunas apgaismojuma ierīces. Tādēļ apkopes segums viņiem ir nepieciešams tikai līdz 2013. gada oktobrim. Lai samazinātu klienta abonementa mēnešu skaitu, jūs izveidojat jaunu abonēšanas maksas transakciju ar veidu **Dienu skaita samazināšana**. Plašāku informāciju par dienu skaita samazināšanu skatiet tēmā [Abonēšanas maksu dienu skaita samazināšana](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Rēķinu izrakstīšana un uzkrāšana saistība ar abonementu transakcijām

Tagad jūs esat pabeidzis abonementa iestatīšanu un varat klientam par to izrakstīt rēķinu. Plašāku informāciju par to, kā izrakstīt rēķinu par abonementiem, skatiet tēmā [Abonementu transakciju rēķinu izrakstīšana](invoice-subscription-transactions.md).

Pēc divām dienām klients zvana, lai paziņotu, ka rēķins par abonementu ir jāizraksta ASV dolāros, nevis eiro. Tādēļ jūs izveidojat kredīta notu, un jūs izveidojat arī jaunu abonementa transakciju ar pareizo valūtu. Plašāku informāciju par to, kā kreditēt abonementu transakcijas, skatiet tēmā [Abonementu transakciju kreditēšana](credit-subscription-transactions.md).

Katra mēneša beigās viena mēneša ienākumus no debitora abonementa var uzkrāt uz peļņas un zaudējumu kontu un NP kontiem. Plašāku informāciju par to, kā uzkrāt ieņēmumus abonementiem, skatiet tēmā [Abonementu ieņēmumu uzkrāšana](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]