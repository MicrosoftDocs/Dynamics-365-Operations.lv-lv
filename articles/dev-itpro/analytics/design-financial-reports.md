---
title: "Skatīt un izveidot finanšu pārskatus"
description: "Šajā rakstā ir sniegti vingrinājumi, kas palīdzēs jums apgūt finanšu pārskatu skatīšanu un veidošanu programmatūrā Microsoft Dynamics 365 for Finance and Operations."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86597a81b4dcfb14cbc88667fbb1db214133c6e5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-design-financial-reports"></a>Skatīt un izveidot finanšu pārskatus

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir sniegti vingrinājumi, kas palīdzēs jums apgūt finanšu pārskatu skatīšanu un veidošanu programmatūrā Microsoft Dynamics 365 for Finance and Operations. Finanšu pārskatu veidošanas ietvaros tiek izmantota programmatūras Dynamics 365 for Finance and Operations pārskatu skatīšanas funkcionalitāte un no viena klikšķa pārskatu veidotājs, kas sniedz iespēju izveidot un rediģēt finanšu pārskatus.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>1. uzdevums. Noklusējuma finanšu pārskata ģenerēšana un pārlūkošana
-----------------------------------------------------------

Šajā uzdevumā tiks ģenerēts un pārskatīts esošs noklusējuma pārskats. Šajā pārskatā ir ietverti visi konti un to rekvizīti (atribūti) kontiem. Jums būs jāpāriet uz transakcijas detalizētas informācijas sadaļu, piemērojot dimensiju filtrus un mainot valūtu pārskatā. Vispirms atjaunināsim finanšu pārskatu dimensiju attēlošanas secību. Tas ļauj izvēlēties, kā dimensijas rādīt ne tikai finanšu pārskatu izstrādes un skatīšanas laikā.

1.  Dodieties uz lapu **Finanšu dimensijas konfigurācija programmu integrēšanai**, kas atrodas Virsgrāmatas sadaļā **Kontu plāna dimensijas**.
2.  Pārvietojiet dimensijas, lai izveidotu šādu secību:
    1.  galvenais konts;
    2.  biznesa vienība;
    3.  izmaksu centrs.
    4.  Nodaļa

    Piezīme. Citas dimensijas var palikt tādā secībā, kādā tās pašlaik atrodas.
3.  Saglabājiet dimensiju konfigurāciju. Tagad ģenerēsim pārskatu un pārskatīsim tajā datus.
4.  Dodieties uz lapu **Finanšu pārskati**, kas atrodas Virsgrāmatas sadaļā **Pieprasījumi un pārskati**.
5.  Atlasiet rindu pārskatam ar nosaukumu **VG dati — noklusējuma.**
6.  Atlasiet **Rediģēt.** Piezīme. Jums tiks piedāvāts lejupielādēt viena klikšķa pārskata veidotāju un pieteikties. Lai pieteiktos, lietojiet savus akreditācijas datus.
7.  Mainiet pamata gadu uz 2012. un izvēlieties **Ģenerēt**. Ģenerējot pārskatu no pārskata veidotāja, tas tiks atvērts jaunā pārlūkprogrammas cilnē. Pārskatu varat pārlūkot jaunajā pārlūkprogrammas cilnē, vai arī pāriet uz sākotnējo pārlūkprogrammas cilni un atvērt pārskatu no tās, atlasot to no saraksta **Finanšu pārskati**.
8.  Atvērtajā pārskatā atlasiet vienu no summām, lai pārietu uz detalizētas parskata konta informācijas lapu.
9.  Konta detalizētas informācijas lapā atlasiet kontu ar datiem un **pārejiet uz pārskata transakciju līmeni**. Pārskata transakciju līmenī var apskatīt rekvizītus (atribūtus), kas iekļauti šajā pārskata noformējumā. Atkarībā no transakcijas un konta var tikt parādīta tikai daļa atribūtu vai visi atribūti.
10. Aizveriet pārskata transakciju līmeni.
11. Atlasiet to pašu vai citu kontu un pēc tam atlasiet vienumu **Atvērt dokumentu transakcijas.** Dokumentu transakcijas tiek filtrētas pēc perioda, gada, konta un atlasītā konta dimensiju kombinācijas. No dokumenta transakcijām varat izvēlēties pārskatīt citu informāciju par transakciju.
12. Aizveriet dokumentu transakcijas. Finanšu pārskatā varat skatīt datus par citu periodu un gadu vai ar piemērotiem dažādiem atribūtiem un dimensijām. Lai to izdarītu, izmantojiet **Pārskata opcijas**.
13. Atlasiet **Pārskata opcijas**.
14. Atlasiet **Pievienot dimensiju filtru** un izvēlieties **Biznesa vienība**.
15. Laukā ievadiet 001 un atlasiet **Labi**. Pārskatā tagad tiek rādīti tikai biznesa vienības 001 dati. Šis ir pārskata personalizēts skats un nav pieejams citiem lietotājiem.
16. Aizveriet filtrēto pārskatu. Finanšu pārskati var tikt rādīti jebkurā valūtā, kas ir pievienota programmatūrā Dynamics 365 for Finance and Operations.
17. Atlasiet **Valūta** un pēc tam atlasiet **EUR.** Pārskata summas tagad tiek rādītas eiro. Visi pārskata noformējumā iekļautie valūtu kodi un simboli tagad tiek rādīti lietotajā valūtā. Ja valūtai nav definēts valūtas simbols, valūtas simbols netiek rādīts.
18. Aizveriet pārskatu **VG dati**.
19. Aizveriet lapu **Finanšu pārskata veidotājs**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>2. uzdevums. Papildu konta rekvizītu pievienošana pārskata noformējumam
Šajā uzdevumā tiks modificēts esošais noklusējuma pārskats. Tiks atjaunināta gan rindu definīcija, lai iekļautu visus kontus, gan kolonnas definīcija, lai iekļautu konta atribūtus. Kad atjaunināšana ir pabeigta, varat ģenerēt un pārskatīt jaunizveidoto pārskatu. Sāksim ar sarakstu Finanšu pārskati.

1.  Dodieties uz lapu **Finanšu pārskati**, kas atrodas Virsgrāmatas sadaļā Pieprasījumi un pārskati.
2.  Atlasiet rindu pārskatam ar nosaukumu **Kopsavilkuma apgrozījuma bilance — noklusējuma.**
3.  Atlasiet **Rediģēt**. Pārskatu veidotājā tiks atvērta **Kopsavilkuma apgrozījuma bilance — noklusējuma**.
4.  Atlasiet **Fails** un pēc tam **Saglabāt kā** un nosauciet pārskatu Detalizēta apgrozījuma bilance ar atribūtiem. Piezīme. Ikreiz, kad tiek izveidots jauns pārskats, izmantojot pārskatu veidotāju, programmatūrā Dynamics 365 for Finance and Operations tiek atjaunināts finanšu pārskatu saraksts.
5.  No pārskata definīcijas atlasiet rindas definīcijas ikonu, lai atvērtu **Apgrozījuma bilance — noklusējuma rindas definīcija**.
6.  Saglabājiet rindas definīciju kā **Detalizēta apgrozījuma bilance ar atribūtiem**.
7.  Novietojiet kursoru 50. rindā, atlasiet **Rediģēt** un pēc tam atlasiet **Ievietot rindas no dimensijām**. Ievietojot rindas no dimensijām, varat izvēlēties, kādas dimensijas vēlaties iekļaut rindas definīcijā. Šajā uzdevumā mēs izveidosim rindas definīciju, izmantojot galveno kontu.
8.  Pārliecinieties, vai sadaļā **Galvenais konts** ir iekļautas visas rakstzīmes “&”, un atlasiet **Labi**. Tagad rindas definīcija satur visus juridiskās personas USMF galvenos kontus.
9.  Ritiniet lejup līdz 11110. rindai un dzēsiet 11110. rindu.
10. 11080. rindā atlasiet **---(summas ar pasvītrojumu)**.
11. 11140. rindas kolonnā B ierakstiet **Visu kontu kopējā**.
12. Kolonnas C nolaižamajā sarakstā atlasiet **TOT**.
13. Kolonnā D ierakstiet **50:11080**.
14. **Saglabājiet** rindas definīciju. Rindas definīcijā tagad ir visi konti, kā arī kopsummas rinda, lai kopā pievienotu visus kontus. Tālāk atjaunināsim kolonnas definīciju, lai iekļautu papildu konta atribūtus.
15. No pārskata definīcijas **Detalizēta apgrozījuma bilance ar atribūtiem** atlasiet kolonnas definīcijas ikonu, lai atvērtu kolonnas definīciju **Kopsavilkuma apgrozījuma bilance — noklusējuma**.
16. Saglabājiet kolonnas definīciju kā **Detalizēta apgrozījuma bilance ar atribūtiem**. Kolonnas definīcija satur finanšu datu kolonnas, apraksta kolonnu un aprēķina kolonnu. Mēs pievienosim kolonnas definīcijai atribūtu kolonnas, lai nodrošinātu papildu informāciju par kontiem.
17. Kolonnas definīcijai tiks pievienoti šādi atribūti:
    -   Žurnāla numurs;
    -   Žurnāla apraksts.
    -   Transakcijas datums
    -   Izveidoja
    -   Pēdējos labojumus veicis

18. Kolonnā I izvēlēties **ATTR** kā kolonnas veidu. Pēc tam atlasiet **žurnāla numurs** kā atribūta kategoriju.
19. Turpiniet, pievienojot kolonnas atlikušajiem atribūtiem.
20. Rindā **2. virsraksts** pievienojiet aprakstu katrai jaunajai kolonnai, kas tika pievienota.
21. Saglabājiet kolonnas definīciju. Tagad, kad rindas definīcija un kolonnas definīcija ir atjaunināta, tās nepieciešams pievienot pārskata definīcijai.
22. No pārskata definīcijas **Detalizēta apgrozījuma bilance ar atribūtiem** atlasiet vienumu Detalizēta apgrozījuma bilance ar atribūtiem gan rindas definīcijai, gan kolonnas definīcijai.
23. Mainiet pamata gadu uz **2012.**
24. **Saglabājiet** pārskata definīciju un **ģenerējiet** to. Kad pārskata ģenerēšana tiek pabeigta un tas tiek atvērts, varat pārskatīt pārskatu, kā to darījāt pirmajā uzdevumā. Pārlūkojiet dažādus kontus, lai redzētu, kā tiek parādīti papildu atribūti.
25. Aizveriet pārskatu **Detalizēta apgrozījuma bilance ar atribūtiem**.
26. Aizveriet lapu **Finanšu pārskata veidotājs**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>3. uzdevums. Daudzdimensiju pārskatu izveide, izmantojot pārskata koku
Šajā uzdevumā tiks modificēts esošais noklusējuma pārskats. Tiks izveidots pārskata koks un pievienota pārskata definīcija, lai izveidotu Izmaksu centrs/nodaļu ieņēmumu pārskats. Kad atjaunināšana ir pabeigta, varat izveidot Izmaksu centrs/nodaļu ieņēmumu pārskats un pārskatīt pārskatu, izmantojot pārskata koku. Sāksim ar sarakstu Finanšu pārskati.

1.  Dodieties uz lapu **Finanšu pārskati**, kas atrodas Virsgrāmatas sadaļā Pieprasījumi un pārskati.
2.  Atlasiet rindu pārskatam ar nosaukumu **Ienākumu pārskats — noklusējuma.**
3.  Atlasiet **Rediģēt**. Pārskatu veidotājā tiks atvērts **Ieņēmumu pārskats — noklusējuma**.
4.  Izvēlnē **Fails** norādiet uz **Jauns** un pēc tam noklikšķiniet uz **Pārskata koka definīcija**.
5.  Izvēlnē **Rediģēšana** noklikšķiniet uz **Ievietot pārskatu veidošanas vienības no dimensijām**.
6.  Notīriet izvēles rūtiņas visām dimensijām, izņemot **Izmaksu centrs**.
7.  Noklikšķiniet laukā **No dimensijas** izmaksu centra dimensijai, ierakstiet **007** un pēc tam nospiediet taustiņu Tab. Laukā **Līdz dimensijai** ierakstiet **018**.
8.  **Saglabājiet** iegūto koku ar nosaukumu **Izmaksu centri pēc nodaļas.** Kad pārskata koks ir izveidots, modificējiet pārskata koku, lai ietvertu trīs jaunas apkopojuma vienības: Mārketings, Operācijas un Mazumtirdzniecība.
9.  Izvēlnē **Logs** noklikšķiniet uz **Izmaksu centri pēc nodaļas**. (Ja pārskata koks tiek aizvērts, atlasiet to navigācijas rūtī no sadaļas Pārskata koka definīcijas.)
10. Noklikšķiniet uz otrā vienuma **Tirdzniecības rādītāji** un pēc tam noklikšķiniet uz ikonas **Ievietot pārskata vienības**.
11. Tukšajā rindā veiciet dubultklikšķi uz elementu kolonnas un atlasiet **USMF**.
12. Kolonnā B un C ierakstiet **Mārketings**.
13. Noklikšķiniet uz piektā vienuma **Pakalpojumu darbības** un pēc tam noklikšķiniet ar peles labo pogu. **Atlasiet Ievietot pārskata vienības**.
14. Atkārtojiet 11. darbību.
15. Kolonnā B un C ierakstiet **Operācijas**.
16. Noklikšķiniet uz divpacmitā vienuma **Izpārdošana** un pēc tam noklikšķiniet ar peles labo pogu. Atlasiet **Ievietot pārskata vienības**.
17. Atkārtojiet 11. darbību.
18. Kolonnā B un C ierakstiet **Mazumtirdzniecība**. Ievērojiet, ka vienības Mārketings, Operācijas un Mazumtirdzniecība tiek rādītas vienā līmenī ar pašreizējām apkopojuma vienībām. Pēc tam tiek kārtotas jaunās vienības. Pārskata vienības kārto, noklikšķot ar peles labo pogu, pārvietojot augšup vai lejup vai velkot un nometot.
19. Pārbaudiet, vai trešā vienība **Tirdzniecības rādītāji** ir aktīva un pēc tam noklikšķiniet ar peles labo pogu.
20. Atlasiet **Pazemināt pārskata vienību**. Ievērojiet, ka vienība tagad tiek rādīta kā vienības **Mārketings** apakšvienība.
21. Noklikšķiniet uz ceturtās vienības **Mārketings** **Kampaņa** un pēc tam noklikšķiniet ar peles labo pogu.
22. Atlasiet **Pazemināt pārskata vienību**.
23. Grafiskajā attēlojumā noklikšķiniet uz **Pakalpojumu darbības**. Nospiediet un turiet nospiestu peles kreiso pogu, vienlaicīgi velkot vienību līdz apkopojumam **Operācijas**. Atlaidiet kreiso peles pogu, lai nomestu vienību apkopojumā Operācijas. Atkārtojiet šo darbību arī vienībai **Ražošana, Kvalitātes kontrole, Loģistika, Sagāde un Administrēšana**.
24. Iestatiet **Izpārdošana**, **Super**, **Tirdzniecības centrs** un **Tiešsaistes** kā **Mazumtirdzniecība** bērnelementu, pazemināt to pozīciju vai velkot un nometot tos.
25. Saglabājiet izveidoto kārtību. Kad pārskata koks ir izveidots un sakārtots, to var pievienot pārskata definīcijai.
26. Izvēlnē **Logs** atlasiet **Ieņēmumu pārskats — noklusējuma**, lai atvērtu pārskata definīciju.
27. Noklikšķiniet uz nolaižamās bultiņas **Koka veids** un atlasiet **Pārskata koks**.
28. Noklikšķiniet uz nolaižamās bultiņas Koks un atlasiet **Izmaksu centri pēc nodaļas**.
29. Mainiet pamata gadu uz **2012**, **saglabājiet** izmaiņas un **ģenerējiet** pārskatu. Kad pārskata ģenerēšana tiek pabeigta un tas tiek atvērts, varat to pārskatīt.
30. Atlasiet nolaižamo sarakstu **Pārskata koks**, lai skatītu pārskata vienības. Varat arī rakties pārskata rindā, lai skatītu visas bilances pārskata koka visām vienībām.
31. Aizveriet pārskatu **Ieņēmumu pārskats — noklusējuma**.
32. Aizveriet lapu **Finanšu pārskata veidotājs**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>4. uzdevums. Konsolidēta pārskata izveide, izmantojot organizācijas hierarhiju
Šajā uzdevumā tiks modificēts esošais noklusējuma pārskats. Pievienojiet organizācijas hierarhiju pārskata definīcijai, lai izveidotu konsolidētu ieņēmumu pārskatu un bilanci. Kad atjaunināšana ir pabeigta, varat ģenerēt un pārskatīt konsolidēto pārskats un pārskatīt to, izmantojot pārskata koku. Sāksim ar sarakstu Finanšu pārskati.

1.  Dodieties uz lapu **Finanšu pārskati**, kas atrodas Virsgrāmatas sadaļā Pieprasījumi un pārskati.
2.  Atlasiet rindu, kas attiecas uz pārskatu ar nosaukumu **Bilance un ieņēmumu pārskats viens otram blakus — noklusējuma**.
3.  Atlasiet **Rediģēt**. Pārskatu veidotājā tiks atvērts **Bilance un ieņēmumu pārskats viens otram blakus — noklusējuma**.
4.  Atlasiet **Fails** &gt; **Saglabāt kā** un piešķiriet pārskatam nosaukumu **Konsolidēta bilance un ieņēmumu pārskats viens otram blakus**.
5.  Mainiet pamata gadu uz 2012.
6.  Noklikšķiniet uz nolaižamās bultiņas Koka veids un atlasiet **Organizācijas hierarhijas**.
7.  Noklikšķiniet uz nolaižamās bultiņas Koka veids un atlasiet **Contoso krājumi**.
8.  Saglabājiet izmaiņas un ģenerējiet pārskatu. Ja tiek piedāvāts, atlasiet visas pārskata vienības. Kad pārskata ģenerēšana tiek pabeigta un tas tiek atvērts, varat to pārskatīt.
9.  Atlasiet **Pārskata opcijas**.
10. Atlasiet **Pievienot dimensiju filtru** un izvēlieties **Nodaļa**.
11. Laukā ievadiet **022** un atlasiet **Labi**.
12. Aizveriet filtrēto pārskatu.
13. Atlasiet nolaižamo sarakstu **Pārskata koks**, lai skatītu pārskata vienības. Varat arī rakties pārskata rindā, lai skatītu visas bilances pārskata koka visām vienībām.
14. Aizveriet pārskatu **Konsolidēta bilance un ieņēmumu pārskats viens otram blakus**.
15. Aizveriet lapu **Finanšu pārskata veidotājs**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>5. uzdevums. Līdzās atvērtu nodaļu pārskata izveide
Šajā uzdevumā izveidosiet jaunu pārskatu. Pārskats ir līdzās atvērtu nodaļu ieņēmumu pārskats. Varat izmantot esošu rindas definīciju, bet izveidot jaunu pārskata definīciju un jaunu kolonnas definīciju, kas izmanto dimensiju filtrus. Sāksim ar sarakstu Finanšu pārskati.

1.  Dodieties uz lapu **Finanšu pārskati**, kas atrodas Virsgrāmatas sadaļā Pieprasījumi un pārskati.
2.  Atlasiet **Jauns**. Pārskata veidotājs atvērsies ar atvērtu tukšu pārskata definīciju. Vispirms izveidojiet kolonnas definīciju.
3.  Izveidojiet jaunu kolonnas definīciju, noklikšķinot uz **Fails**, pēc tam noklikšķinot uz **Jauna** un pēc tam noklikšķinot uz **Kolonnas definīcija**.
4.  **Kolonnā A** izvēlēties **DESC** kā kolonnas veidu.
5.  **Kolonnā B** izvēlēties **FD** kā kolonnas veidu.
6.  Veiciet dubultklikšķi laukā **Dimensiju filtrs**.
7.  Logā **Dimensija** veiciet dubultklikšķi uz kolonnas **Nodaļa**.
8.  Dialoga sadaļā Atsevišķa vai diapazons noklikšķiniet uz **daudzpunktes** pie lauka **No**, lai parādītu nodaļu sarakstu.
9.  Atlasiet nodaļu **022**, **Tirdzniecība un mārketings** un pēc tam noklikšķiniet uz **Labi**.
10. Atkārtojiet 5.–8. darbību 23.–25. nodaļai.
11. Rindas **2. galvene** katrā kolonnā FD ierakstiet šādu nodaļu aprakstu:
    -   kolonnā B — Pārdošana un mārketings;
    -   kolonnā C — Operācijas;
    -   kolonnā D — Finanses;
    -   kolonnā E — IT.

12. Saglabājiet kolonnas definīciju kā Līdzās atvērtas nodaļas. Tā kā mēs izmantojam esošo rindas definīciju, pārskata definīciju tagad var modificēt, lai izmantotu jaunizveidoto kolonnas definīciju un esošo rindas definīciju.
13. Izvēlnē **Logs** atlasiet **Jauna pārskata definīcija**, lai atvērtu pārskata definīciju.
14. Atlasiet **Ieņēmumu pārskats — noklusējuma** kā rindas definīciju un **Līdzās atvērtas nodaļas** kā kolonnas definīciju.
15. Saglabājiet pārskata definīciju ka **Līdzās atvērtu nodaļu ieņēmumu pārskats**.
16. Mainiet pamata gadu uz **2012**.
17. Mainiet detalizācijas līmeni uz **Finanšu, konta un transakcijas**.
18. **Saglabājiet** veiktās izmaiņas un **ģenerējiet** pārskatu. Kad pārskata ģenerēšana tiek pabeigta un tas tiek atvērts, varat to pārskatīt.

## <a name="additional-resources"></a>Papildu resursi
[Finanšu pārskati](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Skatīt finanšu pārskatus](../../financials/general-ledger/view-financial-reports.md) 
[Emuārs Dynamics finanšu pārskatus sastādīšana](http://blogs.msdn.com/b/dynamics_financial_reporting/)




