---
title: "Piekļuves tiesību definēšana izmaksu objektu kontrolieriem"
description: "Šajā tēmā ir sniegta informācija par piekļuves tiesībām izmaksu objektu kontrolieriem."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2ba38ddc5c717df29462e4316dc5045d0eef8c1a
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a>Piekļuves tiesības izmaksu objekta kontrolierim

[!include[banner](../includes/banner.md)]

Darbvieta **Izmaksu kontrole** ir centralizēta vieta, kur pārvaldnieki var skatīt savu izmaksu objektu veiktspēju. Šī darbvieta sniedz pārvaldniekiem iespēju izmantot izmaksu uzskaites datus, lai gan viņi nav izmaksu grāmatveži. Drošības apsvērumu dēļ pārvaldniekiem drīkst nodrošināt piekļuvi tikai tiem izmaksu uzskaites datiem, kas ir saistīti ar konkrēto izmaksu objektu, par kuru viņi ir atbildīgi.

Darbvietā Izmaksu uzskaite ir pieejamas četras unikālas lomas.

| Lomas nosaukums               | Licence      |
|-------------------------|--------------|
| Izmaksu uzskaites pārvaldnieks | Aktivitāte     |
| Izmaksu grāmatvedis         | Operations   |
| Izmaksu grāmatvedības darbinieks   | Operations   |
| Izmaksu objekta kontrolieris  | Grupas dalībnieki |

Šajā tēmā ir paskaidrots, kā piešķirt pārvaldniekam lomu **Izmaksu objekta kontrolieris**.

Ja pārvaldniekam ir piešķirta loma **Izmaksu objekta kontrolieris**, viņš var veikt tālāk norādītās darbības.

- Piekļūt darbvietai **Izmaksu kontrole** (klientā).

    - Veikt detalizētu apskati un skatīt lapas, kas ir saistītas ar detalizēto apskati.

- Piekļūt darbvietai **Izmaksu kontrole** (mobilajā lietojumprogrammā).

> [!NOTE]
> Loma **Izmaksu objekta kontrolieris** nesniedz iespēju kontrolēt to, kuriem izmaksu objektiem lietotājs var piekļūt un par kuriem izmaksu objektiem lietotājs var skatīt datus. Lomas līmeņa drošība tiek nodrošināta, izmantojot dimensiju hierarhijas un piekļuves saraksta hierarhiju.

## <a name="grant-access-rights"></a>Piekļuves tiesību piešķiršana
Tālāk ir sniegts dimensiju hierarhijas piemērs.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija    | Dimensiju hierarhijas veida nosaukums      | Piekļuves sarakstu hierarhija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizācija             | Izmaksu centri | Dimensiju klasifikācijas hierarhija | **Jā**               |

Varat izmantot hierarhijas veidotāja kopsavilkuma cilni **Lietotāji**, lai katrā mezglā ievietotu vienu vai vairākus lietotāja ID.

|                                   | Lietotāji            | Dimensijas elementu diapazons   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Mezgli**                         | **Lietotāja ID**      | **Avota dimensijas elements** | **Mērķa dimensijas elements** |
| Organizācija                      | Bendžamins, Klēra |                           |                         |
| &nbsp;&nbsp;Administrators                 | Aprīlī            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansēt   | Alīsija           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Ārnijs            | CC001                     | CC001                   |
| &nbsp;&nbsp;Ražošana            | Deivids            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Iepakošana | Elēna            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montāža  | Kriss            | CC006                     | CC006                   |

> [!NOTE]
> Izmaksu grāmatveži ir jāpiešķir augstākajam hierarhijas līmenim, lai viņi varētu skatīt visus ierakstus darbvietā Izmaksu uzskaite.

Pirms piekļuves saraksta hierarhijas un tās drošības iestatījumu lietošanas lapas **Izmaksu uzskaites parametri** cilnē **Vispārīgi** ir jāiestata opcijas **Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem** vērtība **Jā** (**Izmaksu uzskaite** > **Iestatīšana** > **Parametri**).

Piekļuves saraksta hierarhijas iestatījumi tiek izmantoti, lai kontrolētu to, kādi dati tiek rādīti tālāk norādītajos apgabalos.

- Darbvietā **Izmaksu kontrole** (klientā)

    - Dati lapās, kas tiek izmantotas padziļinātai apskatei

- Darbvietā **Izmaksu kontrole** (mobilajā lietojumprogrammā)

    - Kartēs norādītās bilances

- Microsoft Power BI

    - Power Bi vizualizācijās attēlotie dati
    - Programmatūras Microsoft Dynamics 365 for Finance and Operation izdevuma Enterprise klientā iegultās datu Power BI vizualizācijas

> [!IMPORTANT]
> - Lai piekļuves saraksta hierarhija varētu ietekmēt datus pakalpojumā Power BI, piekļuves saraksta hierarhija ir jāsavieno pārī ar rindas līmeņa drošību pakalpojumā Power BI. Papildinformāciju skatiet rakstā [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Šajā tēmā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darbvietas **Izmaksu kontrole** lietošanas.

Skatiet arī

- [Izmaksu kontroles darbvieta](cost-control-workspace.md)
- [Dimensiju hierarhija](dimension-hierarchy.md)
- [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

