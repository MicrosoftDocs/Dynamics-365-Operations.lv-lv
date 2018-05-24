---
title: "Krājumu aizstāšanas pasūtījuma izveidošana"
description: "Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei."
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f0cd629658972f98e2233dfa287940c4444b82a
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="create-an-item-replacement-order"></a>Krājumu aizstāšanas pasūtījuma izveidošana 

[!include [banner](../includes/banner.md)]


Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei. Tomēr, ja vienības tiek apmainīta pirms atgriešanas, vai, ja oriģinālā vienība netiek atgriezta, varat izveidot vienības maiņas pasūtījumu tūlīt pēc atgriešanas pasūtījuma izveidošanas.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Aizstāšanas pasūtījuma izveidošana pēc atgriezta krājuma saņemšanas

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgriešanas pasūtījumu sarakstā, lai atvērtu veidlapu **Atgriešanas pasūtījums — AKA kods: %1, %2**.

3.  Noklikšķiniet uz **Atgriešanas rinda** un pēc tam atlasiet **Krājuma aizstājējs**.

4.  Atlasiet krājumu, ar kuru aizstāt atgriezto krājumu. Ievadiet krājuma specifikācijas un pēc tam noklikšķiniet uz **Lietot**.

5.  Noklikšķiniet uz **Pavadzīme**, lai ģenerētu atgriešanas pasūtījuma pavadzīmi. Atlasītajam aizvietošanas krājumam tiek ģenerēts pārdošanas pasūtījums.
    
    Pēc tam, kad krājuma aizstājējam ir izveidots pārdošanas pasūtījums, automātiski tiek meklēti pārdošanas līgumi, un, ja tiek atrasts piemērojams pārdošanas līgums, tas tiek izmantots pārdošanas pasūtījumam.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Aizstāšanas pasūtījuma izveidošana pirms atgriešanai paredzēta krājuma atgriešanas

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.

2.  Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgriešanas pasūtījumu sarakstā, lai atvērtu veidlapu **Atgriešanas pasūtījums — AKA kods: %1, %2**.

3.  Noklikšķiniet uz **Atrast pārdošanas pasūtījumu**, ja vēlaties identificēt atgrieztā krājuma pārdošanas pasūtījumu. Aizpildiet veidlapu **Atrast pārdošanas pasūtījumu** un pēc tam noklikšķiniet uz **Labi**, lai veidlapu aizvērtu un atgrieztos veidlapā **Atgriešanas pasūtījums — AKA kods: %1, %2**. Atgriezto krājumu pārdošanas pasūtījuma rinda tiek kopēta atgriešanas pasūtījumā.

4.  Lai atvērtu veidlapu **Pārdošanas pasūtījuma izveide**, noklikšķiniet uz **Aizstāšanas pasūtījums**.

5.  Atzīmējiet izvēles rūtiņu **Kopēt atgriešanas pasūtījuma rindas**, lai uz šo pārdošanas pasūtījumu pārsūtītu detalizētu informāciju no atgriešanas pasūtījuma, ko izvēlējāties veidlapā **Atgriešanas pasūtījums — AKA kods: %1, %2**.

6.  Ja nepieciešams, ievadiet vai mainiet detaļas.
    
    Ja 3. darbībā identificējāt pārdošanas pasūtījumu un ja pārdošanas pasūtījuma rinda atgrieztajam krājumam ir saistīta ar pārdošanas līgumu, piemērojamā pārdošanas līguma identifikators krājuma aizstāšanas pasūtījumam tiks automātiski rādīts laukā **Pārdošanas līguma ID**.

7.  Noklikšķiniet uz **Labi**, lai aizvērtu veidlapu **Pārdošanas pasūtījuma izveide** un atvērtu veidlapu **Pārdošanas pasūtījums**, kur varat turpināt ievadīt informāciju par jauno pārdošanas pasūtījumu. Visas piemērojamās atgriešanas pasūtījuma rindas tiks kopētas uz jauno pārdošanas pasūtījumu. 
    
    Ja pārdošanas līguma identifikators tiek automātiski rādīts laukā **Pārdošanas līguma ID**, pārdošanas līgums ir saistīts ar pārdošanas pasūtījuma virsrakstu krājumu aizstāšanas pasūtījumam. Ja ir piemērojama saistība pārdošanas līgumā, kas vēl nav izpildīts, un pārdošanas pasūtījums tiek izveidots pirms pārdošanas līguma termiņa beigām, tiek izveidota saite starp pārdošanas līguma rindu un pārdošanas pasūtījuma rindu. Tādēļ informācija no pārdošanas līguma, piemēram, preces cena, tiek kopēta jaunajā pārdošanas pasūtījuma rindā. 
  



