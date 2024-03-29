---
title: Pakalpojumu uzdevumu pārskats
description: Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā. Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc0dee0747c26b073d750d19328a6a59c234fd3f
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016405"
---
# <a name="service-tasks-overview"></a>Pakalpojumu uzdevumu pārskats

[!include [banner](../includes/banner.md)]

Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā.
Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.

Pakalpojumu uzdevumi tiek veidoti lapā **Pakalpojumu uzdevumi**, un tie tiek saistīti ar konkrētu pakalpojumu līgumu vai pakalpojuma pasūtījumu, veidojot pakalpojumu uzdevumu attiecības. Ikreiz, kad veidojat pakalpojumu uzdevumu attiecības, varat veidot:

-  Iekšējās piezīmes par uzdevumu, piemēram, detalizētas tehniskās prasības uzdevumam, kuras tehniskajiem speciālistiem ir svarīgi zināt.

-  Ārējās piezīmes, kuras var redzēt kreditori. Tās sniedz mazāk tehnisku skaidrojumu par uzdevumu, kas tiek veikts atbilstoši līgumam starp debitoru un pakalpojumu uzņēmumu.

Kad ir izveidotas pakalpojumu uzdevumu attiecības starp pakalpojuma uzdevumu un pakalpojuma pasūtījumu vai pakalpojumu līgumu, varat norādīt pakalpojuma uzdevumu, kad veidojat pakalpojuma pasūtījuma rindas vai pakalpojumu līguma rindas pašreizējajam pakalpojuma pasūtījumam vai pakalpojumu līgumam.

Kad ģenerējat pakalpojumu pasūtījumus no pakalpojumu līguma, varat izmantot katrai pakalpojumu līguma rindai piešķirtos pakalpojumu uzdevumus, lai pakalpojumu pasūtījumos grupētu pakalpojuma pasūtījuma rindas.

## <a name="create-a-service-task"></a>Pakalpojuma uzdevuma izveide

1. Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu uzdevumi**.
2. Izveidojiet jaunu rindu.
3. Ievadiet pakalpojuma ID un aprakstu.

## <a name="example"></a>Piemērs

Tehniskajam speciālistam ir jāveic divi darbi saistībā ar pārnesumkārbu (pakalpojumu objekts GB-1234) debitora vietā. Debitoram tiek izveidots pakalpojumu līgums, un ar darbiem tiek saistītas vairākas darbības. Zemāk redzams pakalpojumu līgums un pakalpojumu līguma rindas šiem diviem darbiem:

### <a name="service-agreement"></a>Pakalpojumu līgums

| Project | Pakalpojumu līgums | apraksts                                  | Grupa   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Pārbaude un dilstošo detaļu nomaiņa — GB-1234 | Prēmija |

### <a name="service-agreement-lines"></a>Pakalpojumu līguma rindas

| apraksts             | Darbības veids | Pakalpojumu objekts | Pakalpojumu uzdevums |
|-------------------------|------------------|----------------|--------------|
| Pārbaude un tīrīšana | Stundas             | GB-1234        | I/C - GB1234 |
| Ceļojums                  | Expense          | GB-1234        | I/C - GB1234 |
| Materiāli               | Objekts             | GB-1234        | I/C - GB1234 |
| Dilstošo detaļu nomaiņa     | Stundas             | GB-1234        | RR - GB1234  |
| GR-1                    | Objekts             | GB-1234        | RR - GB1234  |
| GR-5                    | Objekts             | GB-1234        | RR - GB1234  |

Pakalpojumu līguma rindām šiem diviem darbiem ir pievienoti divi pakalpojumu uzdevumi. Pakalpojumu uzdevumi nosaka darbības, kas pieder katram darbam. Pirmajā gadījumā pakalpojuma uzdevums I/C - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas objekta GB-1234 pārbaudē un tīrīšanā. Otrajā gadījumā pakalpojuma uzdevums RR - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas dilstošo detaļu nomaiņas darba veikšanā.

Pakalpojumu uzdevumu attiecības, kas saista pakalpojumu uzdevumus pie konkrētā līguma, ir šādas:

### <a name="service-tasks"></a>Pakalpojumu uzdevumi

| Pakalpojuma uzdevums | Apraksts                             | Iekšējā piezīme                                                                                                                 | Ārējā piezīme                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Ātrumkārbas GB-1234 pārbaude           | Ātrumkārbas GB-1234 vizuālā un mehāniskā pārbaude un tīrīšana.                                                              | Ātrumkārbas dilstošo detaļu pārbaude |
| RR - GB1234  | GB-1234 detaļu dilstošo detaļu nomaiņa | GR-1 un GR-5 dilstošo detaļu nomaiņa (ātrumkārbām, kas ražotas pirms 2002. gada arī GR-2 detaļas nomaiņa) | Dilstošo detaļu nomaiņa  |

## <a name="group-service-orders"></a>Pakalpojumu pasūtījumu grupēšana

Kad automātiski veidojat pakalpojumu pasūtījumus, kā grupēšanas kritēriju varat izmantot pakalpojumu uzdevumus. Lai pakalpojumu pasūtījumus grupētu pēc pakalpojumu uzdevumiem, definējiet pakalpojumu līgumam, ka pakalpojumu pasūtījumi, kuru pamatā ir pakalpojumu līgums, jāgrupē pēc pakalpojumu uzdevumu ID kā to sākotnējā grupēšanas kritērija.

**Grupēšana pēc pakalpojuma uzdevuma**

1. Noklikšķiniet **uz Pakalpojumu pārvaldības** \> **pakalpojumu līgumi** \> **Pakalpojumu līgumi**.
2. Cilnes **Iestatījumi** laukā **Pakalpojumu pasūtījumu kombinēšana** atlasiet **Pēc pakalpojuma uzdevuma**.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]