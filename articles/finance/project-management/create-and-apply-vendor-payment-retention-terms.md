---
title: Izveidot un lietot kreditoru maksājumu ieturējumu nosacījumus
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt un uzturēt ieturējumu nosacījumus kreditoru maksājumiem.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410245"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Izveidot un lietot kreditoru maksājumu ieturējumu nosacījumus

[!include [banner](../includes/banner.md)] 

Kreditora maksājuma ieturējuma nosacījumu iestatīšana projektam ir noderīga, ja jūsu organizācija vēlas saglabāt daļu no kreditoriem veiktajiem maksājumiem. Piemēram, ja vēlaties aizturēt maksājumu kreditoram, līdz piegādātās preces atbilst jūsu vēlmēm. Kreditora maksājuma nosacījumus varat norādīt, kad vienojaties par kreditora līgumu.

## <a name="create-vendor-payment-retention-terms"></a>Kreditora maksājuma ieturējumu nosacījumu izveide

Var ievadīt procentuālo daļu, kas ir jāietur no maksājuma kreditoram, un iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei. Summas tiek automātiski ieturētas no kreditora rēķiniem, līdz ir sasniegts līgumā norādītais pabeigtības stāvoklis. Kad kreditora ieturējumu nosacījumi ir iestatīti, tos var lietot jebkurā projektā šim kreditoram.

Izmantojiet tālāk minētās darbības, lai iestatītu un uzturētu ieturējumu nosacījumus maksājumiem, kas veicami kreditoram. 

1. Dodieties uz **Projektu vadība un uzskaite** > **Ieturējumi** > **Kreditora maksājumu ieturējumu nosacījumi**.
2. Atlasiet **Jauns**, lai pievienotu jaunu kreditora ieturējumu nosacījumu. Jaunā nosacījuma vērtība **Kārtulas ID** tiek ievadīta automātiski. 
3. Ievadiet īsu aprakstu laukā **Apraksts** un kopsavilkuma cilnē **Nosacījumi** atlasiet vienumu **Pievienot rindu**, lai ievadītu terminu vērtības tālāk minētajam.

   - **Piegādāto vienību procentuālā daļa**: ievadiet procentuālo daļu, kuru sasniedzot nosacījums ir jāizpilda. Summas tiek automātiski ieturētas no kreditora rēķiniem, līdz projekta pabeigtības posms ir vienāds ar norādīto procentuālo daļu. Piemēram, ja ievadāt 50,00 procentus, summa tiek saglabāta kā ieturēta līdz brīdim, kad projekta pabeigtība sasniegs 50 procentus.
   - **Uzkrājamie procenti**: ievadiet procentuālo daļu, kas ir ieturama no kreditora rēķina summas. Piemēram, ja ievadāt 10.00, tad 10 procenti no kreditora rēķinu summas tiek ieturēti, līdz projektā ir sasniegts pabeigtības stāvoklis, ko atlasījāt kā iestatītu **Piegādāto vienību procentuālās daļas lauks**.
   - **Procentuālā daļa, kas jānodod izpildei**: atlasiet **Pievienot rindu**, lai ievadītu iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei, kad projektā ir sasniegts pabeigtības stāvoklis.

> [!NOTE]
> Ja dažādos projekta līmeņos ir iestatīti dažādi pabeigtības stāvokļi, katrai ieturējumu kārtulai ievadiet atsevišķu rindu ar kreditora ieturējumu nosacījumiem. Katrā rindā var norādīt atšķirīgu ieturamo procentuālo daļu un atšķirīgu procentuālo daļu, kas ir jānodod izpildei, katrā projekta pabeigtības līmenī.

Kad kreditora ieturējumu nosacījumi ir izveidoti, varat lietot šos nosacījumus projektam.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Kreditora ieturējumu nosacījumu lietošana projektam

1. Dodieties uz **Projektu vadība un uzskaite** > **Projekti** > **Visi projekti** un projektu saraksta lapā atveriet projektu.
2. Kopsavilkuma cilnē **Kreditora līgumi** atlasiet **Pievienot rindu**.
3. Laukā **Konta kods** atlasiet kādu no tālāk minētajām opcijām. 

   - **Tabula**: kreditora ieturējumu nosacījumi attiecas uz vienu kreditoru.
   - **Grupa**: kreditora ieturējumu nosacījumi attiecas uz visiem kreditoriem kreditoru grupā.
   - **Visi**: kreditora ieturējumu nosacījumi attiecas uz visiem kreditoriem.

4. Laukā **Kreditors/kreditoru grupa** atlasiet kreditoru vai kreditoru grupu, uz kuru attiecas kreditora ieturējumu nosacījumi. Šis lauks nav pieejams, ja iepriekšējā transakcijā izvēlējāties **Visi**.
5. Laukā **Kreditora ieturējumu nosacījumi** atlasiet ieturējumu nosacījumus, kurus izveidojāt iepriekšējā procedūrā.
6. Ja projektā kreditoram ir iestatīti “apmaksāt pēc apmaksas” (PWP — pay-when-paid) veida nosacījumi, laukā **PWP sliekšņa procentuālā vērtība** ievadiet projekta sliekšņa procentuālo vērtību.

Kreditora ieturējumu nosacījumi tiek parādīti arī pirkšanas pasūtījumos, ko izveidojat kreditoram.
