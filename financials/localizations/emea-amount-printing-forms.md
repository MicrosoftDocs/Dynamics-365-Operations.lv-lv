---
title: "Atjaunināt kā summas, kas tiek parādīti ziņojumi un dokumenti"
description: "Šajā tēmā ir sniegta informācija par to, kā atjaunināt kā summas, kas tiek parādīti ziņojumus un citus dokumentus, lai Igaunija, Latvija, Lietuva, Polija, Čehijā, Ungārijā un Krievijā."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 870341b81e49c9fc677052e9ef87a580892f486f
ms.lasthandoff: 03/31/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Atjaunināt kā summas, kas tiek parādīti ziņojumi un dokumenti

Šajā tēmā ir sniegta informācija par to, kā atjaunināt kā summas, kas tiek parādīti ziņojumus un citus dokumentus, lai Igaunija, Latvija, Lietuva, Polija, Čehijā, Ungārijā un Krievijā.

Juridiskām personām, Igaunija, Latvija, Lietuva, Polija, Čehijā, Ungārijā un Krievijā, var uzstādīt pilnu un īstermiņa valūtas vienībās un apakšvienībās nosaukumi. Šos nosaukumus var izmantot, lai pārveidotu kā summas tiek atspoguļotas dokumentos un atskaitēs. Piemēram: summa **LTL 100.20** var tikt skatīti kā **100 lits 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Iestatiet pilnu un īstermiņa valūtas vienībās un apakšvienībās nosaukumus
Pilna un īstermiņa valūtas vienību nosaukumus un apakšvienībās valodas iestatīšanu, izpildiet šādas darbības:

1.  Atvērts **valūtām** lapā.
2.  Izvēlieties valūtu.
3.  Rūtī darbības noklikšķiniet uz **Deklinācija**.
4.  Lai pievienotu vārdu un uzvārdu un īsais nosaukums valodai, noklikšķiniet uz **New** un aizpildīt šādus laukus.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Field**                                                 | **Description**                                                                                                                                                                                                    |
    | **Language**                                              | Atlasiet pašreizējā teksta valodu.                                                                                                                                                                          |
    | **Vienskaitļa nominatīvs (nosaukums vienību lauku grupā pārdošanas pasūtījums)**       | Ievadiet valūtas vienskaitļa formā. Piemēram, vienskaitļa formā litu ir lits.                                                                                                                         |
    | **Daudzskaitļa nominatīvs (nosaukums vienību lauku grupā pārdošanas pasūtījums)**         | Ievadiet valūtas daudzskaitļa formā. Piemēram, ievadiet Litai. **Piezīme**: **vienskaitļa ģenitīvs** un **Daudzskaitļa ģenitīvs** lauki ir pieejami, pamatojoties uz valodu, ko esat atlasījis tabulā **valodas** lauks. |
    | **Vienskaitlis personu jomā (nosaukums daļas lauku grupā pārdošanas pasūtījums)** | Ievadiet valūtas subunit vienskaitļa formā.                                                                                                                                                            |
    | **Daudzskaitļa nominatīvs (nosaukums daļas lauku grupā pārdošanas pasūtījums)**         | Ievadiet valūtas subunit daudzskaitļa formā.                                                                                                                                                              |
    | **Saīsnes nosaukums vienību (īsais nosaukums lauka grupa)**       | Ievadiet ISO kodu, kas identificē ar valūtu. Piemēram, ievadiet LTL, lai identificētu litus.                                                                                                                             |
    | **Saīsnes nosaukumu daļām (īsais nosaukums lauka grupa)**      | Ievadiet valūtas subunit nominālvērtība. Piemēram, ievadiet Centas.                                                                                                                                         |
    | **Conjunction 'and' between units and parts**             | Atlasiet, lai drukātu kopā "un" starp valūtas vienību un vienību daļām. Piemēram, rēķinus vai atskaitēs LTL 100.20 summa tiks parādīts kā 100 lits un 20 Centas.                      |

5.  Click **Save**.



