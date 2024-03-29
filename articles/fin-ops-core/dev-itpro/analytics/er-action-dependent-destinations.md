---
title: Konfigurēt no darbības atkarīgus ER adresātus
description: Šajā rakstā skaidrots, kā konfigurēt no darbības atkarīgus adresātus elektroniskajam pārskata (ER) formātam, kas ir konfigurēts nosūtīšanas dokumentu ģenerēšanai.
author: kfend
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: babd123e4c8007e3adc545bb92a2dc83bab93f4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286253"
---
# <a name="configure-action-dependent-er-destinations"></a>Konfigurēt no darbības atkarīgus ER adresātus

[!include [banner](../includes/banner.md)]

Jūs varat konfigurēt [adresātus katram elektroniskā pārskata (ER)](electronic-reporting-destinations.md) formāta konfigurācijas izvades [komponentam (mapei vai failam),](general-electronic-reporting.md)[kas](general-electronic-reporting.md#Configuration) tiek izmantots, lai ģenerētu izejošo dokumentu. Lietotāji, kas izmanto šī tipa ER formātu un kuriem ir atbilstošas piekļuves tiesības, izpildlaikā var mainīt arī konfigurētos adresāta iestatījumus.

Microsoft Dynamics 365 Finanšu **versijā 10.0.17** un jaunākā versijā ER formātu var palaist, nodrošināt darbības kodu, ko lietotājs izpilda, palaižot šo ER [formātu](er-apis-app10-0-17.md). Piemēram, **Debitoru parādu** modulī Drukas pārvaldības iestatījumos varat atlasīt ER formātu, kas ģenerē noteiktu biznesa dokumentu, piemēram, brīva teksta rēķinu. Pēc tam varat atlasīt **Skatīt**, lai priekšskatītu rēķinu, vai **Drukāt**, lai nosūtītu to uz printeri. Ja izpildlaikā lietotāja darbība ir izpildītā ER formātam, var konfigurēt dažādus ER adresātus dažādām lietotāja darbībām. Šajā rakstā ir skaidrots, kā konfigurēt ER adresātus šī tipa ER formātam.

## <a name="make-action-dependent-er-destinations-available"></a>Konfigurēt no darbības atkarīgus ER adresātus

Lai esosajā Finance Instance konfigurētu no darbības atkarīgus ER adresātus un iespējotu [jaunu](er-apis-app10-0-17.md) ER API, atveriet [Līdzekļu pārvaldības](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) darbvietu un iespējojiet funkciju **Konfigurēt noteiktus ER adresātus, kas jāizmanto dažādām PM darbībām**. Lai izpildlaikā [noteiktiem](#reports-list-wave1) pārskatiem izmantotu konfigurētus ER adresātus, iespējojiet funkciju **Maršruta izvades PM pārskati, pamatojoties uz ER adresātiem, kas ir raksturīgi lietotāja darbībai (1. kopums)**.

## <a name="configure-action-dependent-er-destinations"></a>Konfigurēt no darbības atkarīgus ER adresātus

Iespējojot funkciju **Konfigurēt noteiktus ER adresātus, ko izmantot dažādām PM darbībām**, jūs varat konfigurēt no darbībām atkarīgus ER adresātus **Elektronisko pārskatu adresāta lapas** kopsavilkuma cilnē **Faila galamērķis**. Katram komponentam jūs varat pievienot ierakstu un iespējot noteiktus ER adresātus. Katram ierakstam jānorāda tā dokumenta tips, kam ir jālieto konfigurētie ER adresāti. Laukā **Dokumenta tips** atlasiet vienu no šīm vērtībām:

- Atlasiet **Elektronisks**, lai pielietotu konfigurētos adresātus, ja izpildlaikā nav norādīts lietotāja darbības kods.
- Atlasiet **Drukas pārvaldība**, lai pielietotu konfigurētos adresātus, ja izpildlaikā nav norādīts lietotāja darbības kods.
- Atlasiet **Jebkurš**, lai pielietotu konfigurētos adresātus, neatkarīgi no tā, vai izpildlaikā ir norādīts lietotāja darbības kods.

Ja atlasāt **Drukas pārvaldības** dokumenta tipu, jānorāda lietotāja darbības, kam jālieto konfigurētie ER mērķi. Laukā **Drukas pārvaldības darbība** atlasiet vienu no šīm vērtībām:

- Atlasiet **Skatīt**, lai pielietotu konfigurētos adresātus, ja izpildlaikā ir norādīta lietotāja darbība **Skatīt**.
- Atlasiet **Drukāt**, lai pielietotu konfigurētos adresātus, ja izpildlaikā ir norādīta lietotāja darbība **Drukāt**.
- Atlasiet **Nosūtīt**, lai pielietotu konfigurētos adresātus, ja izpildlaikā ir norādīta lietotāja darbība **Nosūtīt**.

> [!NOTE]
> Vienam mērķa ierakstam var atlasīt vairākas darbības.

Atlasot **Jebkuru** dokumenta tipu, laukā **Drukas pārvaldības darbība** kā lietotāja darbība automātiski tiek atlasīta funkcija **Automātiski**, un notiek šāda darbība:

- Ja izpildlaikā nav norādīts lietotāja darbības kods, tiek piemērotas visi konfigurētie ER mērķi.
- Ja izpildlaikā tiek nodrošināts lietotāja darbības kods, tiek lietots ER adresāts, kas ir iepriekš definēts konkrētai darbībai, **neatkarīgi no tā, vai tas ir aktivizēts**:

    - Ja izpildlaikā ir sniegta darbība **Skatīt**, tiek lietots ER mērķis **Ekrāns**.
    - Ja izpildlaikā ir sniegta darbība **Nosūtīt**, tiek lietots ER mērķis **E-pasts**.
    - Ja izpildlaikā ir sniegta darbība **Drukāt**, tiek lietots ER mērķis **Printeris**.

Piemēram, **Brīvā teksta rēķinu (Excel)** ER formātu var izmantot, lai drukātu [brīva teksta rēķinu](../../../finance/accounts-receivable/create-free-text-invoice-new.md), kad to grāmatojat. Lai maršrutētu ģenerēto dokumentu, ir jākonfigurē ER adresāti šim ER formātam. Piemēram, jums var būt nepieciešams konfigurēt šos ER adresātus, lai ģenerētajā dokumentā veiktu šādas darbības:

- Arhivējiet dokumentu, ja ER formāts tiek palaists, bet netiek norādīts darbības kods (piemēram, kad dokuments tiek nosūtīts elektroniski).
- Priekšskatiet dokumentu tīmekļa pārlūkprogrammā, kad lietotājs veic darbību **Skatīt**.
- Arhivējiet un drukājiet dokumentu, kad lietotājs veic darbību **Drukāt**.
- Arhivējiet dokumentu un nosūtiet to pa e-pastu kā izejošā e-pasta ziņojuma pielikumu, kad lietotājs veic darbību **Nosūtīt**.

Šajā attēlā parādīts, kā var sasniegt šo ER adresātu konfigurēšanu kā atsevišķu mērķa ierakstu kopu, kad katrs ieraksts ir konfigurēts atsevišķai lietotāja darbībai:

![Elektronisko pārskatu mērķa lapa, kam ir no darbības atkarīgi mērķa iestatījumi ER formātam, ja katrs mērķa ieraksts ir konfigurēts atsevišķa lietotāja darbībai.](./media/er-destination-action-dependent-01.png)

Šajā attēlā parādīts, kā var sasniegt šo ER adresātu konfigurēšanu kā atsevišķu mērķa ierakstu kopu, kad katrs ieraksts ir konfigurēts atsevišķai lietotāja darbībai:

![Elektronisko pārskatu mērķa lapa, kam ir no darbības atkarīgi mērķa iestatījumi ER formātam, ja katrs mērķa ieraksts ir konfigurēts atsevišķa lietotāja darbībai.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Ja darbības kods ir norādīts palaistajā ER formātā, bet šim darbības kodam nav konfigurēti adresāti, tiek pielietota [noklusējuma](electronic-reporting-destinations.md#default-behavior) mērķa uzvedība.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Konfigurēt no darbības atkarīgus ER adresātus izpildlaikā

Ja ER formāts tiek palaists, ja lietotāju darbības ir nodrošinātas ar lietotājiem, kuriem ir atbilstošās [atļaujas](electronic-reporting-destinations.md#security-considerations), lai izpildlaikā mainītu konfigurētos mērķa iestatījumus, tiek parādīts dialoglodziņš, kas sniedz opciju mainīt konfigurētos adresāta iestatījumus. Šis dialoglodziņš nav obligāts, un tā izskats ir atkarīgs no tā, kā ir ieviests zvans, ko ER struktūra veic, lai palaistu ER formātu. Ja parādās šis dialoglodziņš, ER adresāti tajā tiks aktivizēti saskaņā ar lietotāja sniegto darbību.

**Šajā ilustrācijā parādīts elektronisko pārskatu formāta mērķa dialoglodziņa piemērs, kas parādās, kad tiek grāmatots brīva teksta rēķins**[...](../../../finance/accounts-receivable/create-free-text-invoice-new.md)**un šī formāta brīvā teksta rēķina (Excel)** ER formāts tiek palaists, lai ģenerētu šo dokumentu, **ja printera** darbība tika nodrošināta un ER adresāti tika konfigurēti šim formātam, kā parādīts iepriekš šajā rakstā.

![Dialoglodziņš, ar kuru tiek sniegta opcija inicializācijas konfigurēto ER adresātu maiņai darbinātajā ER formātā.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Ja jūs konfigurējat ER adresātus vairākiem ER formāta komponentiem, opcija tiks piedāvāta atsevišķi katram konfigurētam ER formāta komponentam.

## <a name="verify-the-provided-user-action"></a>Pārbaudīt sniegto lietotāja darbību

Veicot konkrētu lietotāja darbību, varat pārbaudīt, kāda lietotāja darbība ir nodrošināta palaistam ER formātam. Šī pārbaude ir svarīga, kad jākonfigurē no darbībām atkarīgie ER adresāti, bet neesat pārliecināts, kurš lietotāja darbības kods, ja tāds ir, tiek nodrošināts. Piemēram, kad sākat grāmatot brīva teksta rēķinu un iestatāt opciju **Drukāt rēķinu** uz **Jā**, , dialoglodziņā **Grāmatot brīva teksta rēķinu** varat iestatīt opciju **Izmantot drukas pārvaldības adresātu** uz **Jā** vai **Nē**.

Izpildiet šīs darbības, lai pārbaudītu nodrošināto lietotāja darbības kodu.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri** iestatiet opciju [Palaist iestatījumus](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) uz **Jā** un pēc tam atlasiet **Labi**.
4. Izpildiet lietotāja darbības, izpildot ER formātu. Ņemiet vērā, ka šis parametrs ir ER lietotājam raksturīgs un uzņēmumam raksturīgs.
5. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas atkļūdošanas žurnāli**.
6. **Konfigurācijas atkļūdošanas žurnālu** lapā filtrējiet ER izpildes žurnālus, lai atrastu žurnālu ER formāta palaišanai.
7. Pārskatiet žurnāla ierakstus, kuros jābūt ierakstam, kas norāda sniegto lietotāja darbības kodu, ja ir bijusi nodrošināta kāda darbība ER formāta palaišanai.

    ![Elektronisko pārskatu palaišanas žurnālu lapa, kas satur informāciju par lietotāja darbības kodu, kas ir nodrošināts ER formāta filtrētai palaišanai.](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Biznesa dokumentu saraksts (1. kopums)</a>

Tālāk norādīto biznesa dokumentu sarakstu kontrolē funkcija, **PM pārskatu maršruta izvade, pamatojoties uz ER adresātiem, kas ir lietotāja darbībai raksturīgi (1. kopums)**:

- Debitora rēķins (brīvā teksta rēķins)
- Debitora rēķins (pārdošanas rēķins)
- Pirkuma pasūtījums
- Pirkšanas pasūtījuma pirkšanas pieprasījums
- Pārdošanas pasūtījuma apstiprinājums
- Atgādinājuma vēstules piezīme
- Procentu paziņojums
- Kreditora maksājuma pievienošana
- Piedāvājuma pieprasījums

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)

[Elektronisko atskaišu veidošanas struktūras API izmaiņas atjauninājumam Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
