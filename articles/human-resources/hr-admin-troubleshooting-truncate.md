---
title: Izvairīšanās no teksta saīsināšanas amatu hierarhijā un eksportēšana uz Visio
description: Šajā rakstā ir skaidrots, kā novērst problēmu, kas rodas saistībā ar apcirstajiem personu vārdiem un amatiem pozīciju hierarhijā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3663f5689fc0109caad01a285185f9f4ffa6fcca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865387"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Izvairīšanās no teksta saīsināšanas amatu hierarhijā un eksportēšana uz Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

Kad debitors skata amatu hierarhiju programmā Microsoft Dynamics 365 Human Resources, tiek saīsināti personu vārdi un amatu nosaukumi. Tādēļ var būt grūti veikt ekrānuzņēmumu vai izdrukāt un izplatīt hierarhiju.

![Amatu hierarhija.](media/position-h.png)

**Iemesls**

Tas tiek darīts ar nolūku.

**Novēršana**

Diemžēl lietotāji nevar viegli mainīt teksta lielumu. Tomēr amatu hierarhiju var eksportēt no Human Resources un tad to importēt Microsoft Visio. Lai gan šis raksts sarakstīts par Microsoft Dynamics AX 2012, process attiecas arī uz Human Resources: [Amatu hierarhijas eksportēšana uz Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Rīkojieties šādi, lai eksp. uz Visio.

1. Human Resources atveriet saraksta lapu **Pozīcijas**.

    Lai iekļautu papildu informāciju Organizācijas struktūras diagrammā, pievienojiet laukus sarakstā **Amati**, lai tie būtu pieejami, vēlāk izmantojot **Organizācijas diagramas vedni** šajā procedūrā.

2. Darbību rūtī atlasiet pogu **Atvērt, izmantojot Microsoft Office** un pēc tam sadaļā **Eksportēt uz Excel** atlasiet vienumu **Amati**. Vai arī nospiediet Ctrl+T.

    ![Saraksta lapas Amati eksports uz Excel.](media/org-admin.png)

3. Saglabājiet eksportēto Excel failu.

    ![Dialogl. Eksp. uz Excel.](media/export-excel.png)

4. Pakalpojumā Visio atl. **Visio — izveidot jaunu** un atl. veidnes kateg. **Uzņēmums**.

    ![Jauna diagr.](media/new.png)

5. Atl. **Organizācijas diagr. vednis** un tad atl. **Izveidot**.

    ![Organizācijas diagr. vedņa dialogl.](media/orgchart-wizard.png)

6. Atlasiet **Informācija, kas jau ir saglabāta failā vai datu bāzē** un tad atlasiet **Tālāk**.

    ![Organiz. diagr. vednis 1.](media/orgchart-wizard7.png)

7. Izv. **Teksta, Org Plus (\*.txt), vai Excel fails** un tad atl. **Tālāk**.

    ![Organiz. diagr. vednis 2.](media/orgchart-wizard3.png)

8. Pārlūkojiet, lai atlasītu eksportēto Excel failu, kas satur amatu hierarhiju, un tad atlasiet **Tālāk**.

    ![Organiz. diagr. vednis 3.](media/orgchart-wizard2.png)

9. Iest. laukā **Nos.** vienumu **Amats**, iest. laukā **Sniedz pārsk.** vien. **Sniedz pārsk. amatam**, tad atl. **Tālāk**.

    ![Organiz. diagr. vednis 4.](media/orgchart-wizard1.png)

10. Atlasiet laukus, kam jābūt redzamiem katrā zarā, un tad atlasiet **Tālāk**.

    ![Organiz. diagr. vednis 5.](media/orgchart-wizard5.png)

11. Pievienojiet kolonnu **Amats** sarakstā **Formas datu lauki** un tad atlasiet **Tālāk**.

    ![Organiz. diagr. vednis 6.](media/orgchart-wizard6.png)

12. Attēli pašlaik nav pieejami. Tādēļ nākamajā lapā atlasiet **Tālāk**.
13. Atl. **Es vēlos, lai vednis automātiski sadala organizācijas diagrammu pa lappusēm**.

    ![Organiz. diagr. vednis 7.](media/orgchart-wizard4.png)

14. Atl. **Pabeigt**.

    Ja ir amati, kas nav iekļauti struktūrā, tiek parādīts uzaicinājums iekļaut tos diagrammā.

Pakalpojumā Visio ģenerētajā diagrammā katrs vadītājs redzams atsevišķā darblapā.

Pamatojoties uz laukiem, kas atlasīti iekļaušanai diagrammā, katrs zars rāda atbilstošu informāciju, kad tiek ģenerēts Visio fails.

![Hierarh. diagr.](media/hierarchy.png)

**Papildu opcija**

Human Resources var lietot arī darbvietu **Personas**, lai skatītu ar hierarhiju saistīto informāciju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
