---
title: Krājumu aizstāšanas pasūtījuma izveide
description: Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0006ea9ec64cd95a709ec91509cb3a9828df160
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996655"
---
# <a name="create-an-item-replacement-order"></a>Krājumu aizstāšanas pasūtījuma izveide 

[!include [banner](../includes/banner.md)]


Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei. Tomēr, ja vienības tiek apmainīta pirms atgriešanas, vai, ja oriģinālā vienība netiek atgriezta, varat izveidot vienības maiņas pasūtījumu tūlīt pēc atgriešanas pasūtījuma izveidošanas.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Aizstāšanas pasūtījuma izveidošana pēc atgriezta krājuma saņemšanas

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgrieztu pasūtījumu sarakstā, lai atvērtu formu **Atgriešanas pasūtījums — AKA kods: %1, %2**.

3.  Noklikšķiniet uz **Atgriešanas rinda** un pēc tam atlasiet **Krājuma aizstājējs**.

4.  Atlasiet krājumu, ar kuru aizstāt atgriezto krājumu. Ievadiet krājuma specifikācijas un pēc tam noklikšķiniet uz **Lietot**.

5.  Noklikšķiniet uz **Pavadzīme**, lai ģenerētu atgriešanas pasūtījuma pavadzīmi. Atlasītajam aizvietošanas krājumam tiek ģenerēts pārdošanas pasūtījums.
    
    Pēc tam, kad krājuma aizstājējam ir izveidots pārdošanas pasūtījums, automātiski tiek meklēti pārdošanas līgumi, un, ja tiek atrasts piemērojams pārdošanas līgums, tas tiek izmantots pārdošanas pasūtījumam.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Aizstāšanas pasūtījuma izveidošana pirms atgriešanai paredzēta krājuma atgriešanas

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgriešanas pasūtījumu sarakstā, lai atvērtu formu **Atgriešanas pasūtījums — AKA kods: %1, %2**.

3.  Noklikšķiniet uz **Atrast pārdošanas pasūtījumu**, ja vēlaties identificēt atgrieztā krājuma pārdošanas pasūtījumu. Aizpildiet formu **Atrast pārdošanas pasūtījumu** un pēc tam noklikšķiniet uz **Labi**, lai aizvērtu formu un atgrieztos formā **Atgriešanas pasūtījums — AKA kods: %1, %2**. Atgriezto krājumu pārdošanas pasūtījuma rinda tiek kopēta atgriešanas pasūtījumā.

4.  Lai atvērtu veidlapu **Pārdošanas pasūtījuma izveide**, noklikšķiniet uz **Aizstāšanas pasūtījums**.

5.  Atzīmējiet izvēles rūtiņu **Kopēt atgriešanas pasūtījuma rindas**, lai uz šo pārdošanas pasūtījumu pasūtītu detalizētu informāciju no atgriešanas pasūtījuma, ko atlasījāt formā **Atgriešanas pasūtījums — AKA kods: %1, %2**.

6.  Ja nepieciešams, ievadiet vai mainiet detaļas.
    
    Ja 3. darbībā identificējāt pārdošanas pasūtījumu un ja pārdošanas pasūtījuma rinda atgrieztajam krājumam ir saistīta ar pārdošanas līgumu, piemērojamā pārdošanas līguma identifikators krājuma aizstāšanas pasūtījumam tiks automātiski rādīts laukā **Pārdošanas līguma ID**.

7.  Noklikšķiniet uz **Labi**, lai aizvērtu veidlapu **Pārdošanas pasūtījuma izveide** un atvērtu veidlapu **Pārdošanas pasūtījums**, kur varat turpināt ievadīt informāciju par jauno pārdošanas pasūtījumu. Visas piemērojamās atgriešanas pasūtījuma rindas tiks kopētas uz jauno pārdošanas pasūtījumu. 
    
    Ja pārdošanas līguma identifikators tiek automātiski rādīts laukā **Pārdošanas līguma ID**, pārdošanas līgums ir saistīts ar pārdošanas pasūtījuma virsrakstu krājumu aizstāšanas pasūtījumam. Ja ir piemērojama saistība pārdošanas līgumā, kas vēl nav izpildīts, un pārdošanas pasūtījums tiek izveidots pirms pārdošanas līguma termiņa beigām, tiek izveidota saite starp pārdošanas līguma rindu un pārdošanas pasūtījuma rindu. Tādēļ informācija no pārdošanas līguma, piemēram, preces cena, tiek kopēta jaunajā pārdošanas pasūtījuma rindā. 
  


