---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā sniegtas atbildes uz dažiem bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266637"
---
# <a name="financial-reporting-faq"></a>Bieži uzdotie jautājumi par finanšu pārskatu veidošanu

Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Kā var ierobežot piekļuvi pārskatam, izmantojot koka drošību?

Šajā piemērā parādīts, kā ierobežot piekļuvi pārskatam, izmantojot koka drošību.

USMF demonstrācijas uzņēmumam ir **bilances pārskats**, kuram nedrīkstētu piekļūt visi finanšu pārskatu lietotāji. Varat izmantot koka drošību, lai ierobežotu piekļuvi atsevišķam pārskatam, ļaujot piekļūt tikai konkrētiem lietotājiem.

1. Pierakstieties programmā Financial Reporter Report Designer.
2. Lai izveidotu jaunu koka definīciju, atlasiet **Fails \> Jauns \> Koka definīcija**.
3. Veiciet dubultskārienu vai dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.
4. Atlasiet **Lietotāji un grupas**.
5. Atlasiet lietotājus vai grupas, kam vajadzīga piekļuve šim pārskatam.
6. Atlasiet **Saglabāt**.
7. Pārskata definīcijā pievienojiet jaunu koka definīciju.
8. Koka definīcijā atlasiet **Iestatījums**. Pēc tam sadaļā **Pārskata vienību atlase** atlasiet **Iekļaut visas vienības**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Kā noteikt, kuri konti neatbilst manām bilancēm?

Ja jums ir pārskats, kurā nav atbilstošu bilanču, veiciet tālāk norādītās darbības, lai identificētu visus kontus un novirzes.

### <a name="in-financial-reporter-report-designer"></a>Programmā Financial Reporter Report Designer

1. Izveidojiet jaunu rindas definīciju.
2. Atlasiet **Rediģēt \> Ievietot rindas no dimensijām**.
3. Atlasiet **MainAccount**.
4. Atlasiet **Labi**.
5. Saglabājiet rindas definīciju.
6. Izveidojiet jaunu kolonnas definīciju.
7. Izveidojiet jaunu pārskata definīciju.
8. Atlasiet **Iestatījumi** un noņemiet atzīmi šai opcijai.
9. Ģenerējiet pārskatu. 
10. Eksportējiet pārskatu uz Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>Programmā Dynamics 365 Finance

1. Dodieties uz **Virsgrāmata \> Pieprasījumi un pārskati \> Apgrozījuma bilance**.
2. Iestatiet tālāk norādītos laukus.

    - **Sākuma datums** — ievadiet finanšu gada sākuma datumu.
    - **Beigu datums** — ievadiet datumu, kuram ģenerējat pārskatu.
    - **Finanšu dimensija** — iestatiet šo lauku kā **Galvenā konta kopa**.

3. Atlasiet **Aprēķināt**.
4. Eksportējiet pārskatu uz programmu Excel.

Tagad jābūt iespējai no Financial Reporter Excel pārskata kopēt datus uz pārskatu **Apgrozījuma bilance**, lai varētu salīdzināt kolonnas **Beigu bilance**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Kad rīkā Report Designer izveidoju pārskatu vai ģenerēju finanšu pārskatu, saņemu šādu ziņojumu: “Operāciju neizdevās pabeigt datu nodrošinātāja struktūras problēmas dēļ.” Kā reaģēt?

Ziņojums norāda, ka radās problēma, sistēmai mēģinot izgūt finanšu metadatus no data mart laikā, kad izmantojāt rīku Financial Reporting. Uz šo problēmu var reaģēt divos tālāk norādītajos veidos.

- Pārskatiet datu integrācijas statusu, rīkā Report Designer dodoties uz **Rīki \> Integrācijas statuss**. Ja integrācija ir nepilnīga, uzgaidiet, līdz tā tiks pabeigta. Pēc tam vēlreiz mēģiniet veikt darbību, ko veicāt, kad saņēmāt ziņojumu.
- Sazinieties ar atbalsta dienestu, lai identificētu un novērstu šo problēmu. Iespējams, sistēmā ir nekonsekventi dati. Atbalsta tehniskie darbinieki var palīdzēt identificēt šo problēmu serverī un atrast konkrētos datus, kurus var būt nepieciešams atjaunināt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
