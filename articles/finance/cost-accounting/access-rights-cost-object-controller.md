---
title: Izmaksu objekta kontrolieru piekļuves tiesības
description: Šajā rakstā ir sniegta informācija par piekļuves tiesībām izmaksu objektu kontrolleriem.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c40be758c5e5d1d1fb025630ed8321ae46251892
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903194"
---
# <a name="access-rights-for-cost-object-controllers"></a>Izmaksu objekta kontrolieru piekļuves tiesības

[!include [banner](../includes/banner.md)]

Darbvieta **Izmaksu kontrole** ir centralizēta vieta, kur pārvaldnieki var skatīt savu izmaksu objektu veiktspēju. Šī darbvieta sniedz pārvaldniekiem iespēju izmantot izmaksu uzskaites datus, lai gan viņi nav izmaksu grāmatveži. Drošības apsvērumu dēļ pārvaldniekiem drīkst nodrošināt piekļuvi tikai tiem izmaksu uzskaites datiem, kas ir saistīti ar konkrēto izmaksu objektu, par kuru viņi ir atbildīgi.

Darbvietā Izmaksu uzskaite ir pieejamas četras unikālas lomas.

| Lomas nosaukums               | Licence      |
|-------------------------|--------------|
| Izmaksu uzskaites pārvaldnieks | Aktivitāte     |
| Izmaksu grāmatvedis         | Operations   |
| Izmaksu grāmatvedības darbinieks   | Operācijas   |
| Izmaksu objekta kontrolieris  | Grupas dalībnieki |

Šajā rakstā skaidrots, kā piešķirt **izmaksu objekta kontrollera** lomu vadītājam.

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

|             Zari                 | Lietotāji            | Avota dimensijas elements     |   Mērķa dimensijas elements   |
|-----------------------------------|------------------|---------------------------|-------------------------|
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

- Microsoft Power BI:

    - Power BI vizualizācijās redzamie dati
    - Datu Power BI vizualizēšanas, kas ir iegultas Dynamics 365 finanšu klientā

> [!IMPORTANT]
> - Lai piekļuves saraksta hierarhija varētu ietekmēt datus pakalpojumā Power BI, piekļuves saraksta hierarhija ir jāsavieno pārī ar rindas līmeņa drošību pakalpojumā Power BI. Papildinformāciju skatiet rakstā [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Šis raksts parāda priekšnosacījumus, kam jābūt vietā, pirms jūs variet izmantot Izmaksu **kontroles darbvietu**.

Papildu resursi

- [Izmaksu kontroles darbvieta](cost-control-workspace.md)
- [Dimensiju hierarhija](dimension-hierarchy.md)
- [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
