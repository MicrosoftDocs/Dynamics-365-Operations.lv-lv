---
title: Veidnes MK izveide
description: "Veidnes MK var izveidot, izmantojot vairākas metodes."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a>Veidnes MK izveide   

[!include [banner](../includes/banner.md)]


Veidnes MK var izveidot, izmantojot jebkuru no tālāk aprakstītajām metodēm. Visām metodēm lauki **Sākuma datums** un **Beigu datums** ir neobligāti un paredzēti tikai informācijai.

## <a name="create-a-template-bom-manually"></a>Manuāla veidnes MK izveide

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.

2.  Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.

3.  Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Manuāli**.

4.  Laukā **Krājuma kods** ievadiet **MK** tipa krājumu.

5.  Laukā **Nosaukums** ievadiet veidnes nosaukumu.

6.  Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.

7.  Noklikšķiniet uz **OK**.

Tiek izveidots jauns, tukšs veidnes MK.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Veidnes MK izveide uz citas veidnes MK pamata

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.

2.  Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.

3.  Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Veidnes MK**.

4.  Laukā **Atsauces numurs** atlasiet jau izveidotu veidnes MK, kuru kopēt uz jauno veidnes MK.

5.  Laukā **Nosaukums** ievadiet veidnes nosaukumu.

6.  Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.

7.  Noklikšķiniet uz **OK**.

Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst rindām oriģinālajā veidnes MK.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Veidnes MK izveide uz krājuma MK pamata

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.

2.  Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.

3.  Sadaļā **Kopēt MK rindas no atsauces** atlasiet **MK**.

4.  Laukā **Atsauces numurs** atlasiet MK versiju. Krājums ar tipu MK tiek kopēts laukā **Krājuma kods**.

5.  Laukā **Nosaukums** ievadiet veidnes nosaukumu.

6.  Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.

7.  Noklikšķiniet uz **OK**.

Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā**Materiālu komplekti** esošajām MK rindām.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Veidnes MK izveide uz ražošanas MK pamata

1.  Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.

2.  Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.

3.  Sadaļā **Kopēt MK rindas no atsauces** atlasiet **Ražošana**.

4.  Laukā **Atsauces numurs** atlasiet ražošanas MK.

5.  Laukā **Nosaukums** ievadiet veidnes nosaukumu.

6.  Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.

7.  Noklikšķiniet uz **OK**.

Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā **MK** esošajām MK rindām.

## <a name="see-also"></a>Skatiet arī

[Veidnes MK ](template-boms.md)

  



