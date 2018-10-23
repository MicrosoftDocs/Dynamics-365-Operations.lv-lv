---
title: "Apakšlīgumu slēgšana"
description: "Šajā sadaļā ir izskaidrots, kā veidot ražošanas apakšlīgumu slēgšanas kritisku analīzi programmā Microsoft Dynamics 365 for Finance and Operations."
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ade3f4ad9878c9e885afc5034334e41897512871
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2018

---

# <a name="subcontracting"></a>Apakšlīgumu slēgšana

[!include [banner](../includes/banner.md)]

Šajā sadaļā ir izskaidrots, kā veidot ražošanas apakšlīgumu slēgšanas kritisku analīzi programmā Microsoft Dynamics 365 for Finance and Operations. Šīs sadaļas pirmajā daļa ir aprakstīta datu iestatīšana. Otrajā daļā ir sniegtas pakāpeniskas norādes par kritiskas analīzes darbībām.

## <a name="target-audience"></a>Mērķauditorija

Šajā sadaļā ir izskaidrots, kā iestatīt apakšlīgumu slēgšanu ražošanā. Esošie dati tiek izmantoti HQUS juridiskajai personai, lai veiktu apakšlīgumu slēgšanas darbību plūsmas pamatfunkcionalitātes iestatīšanu. HQUS juridiskās personas demonstrācijas dati ietver iestatīšanas parametrus, kas ir iepriekš iestatīti, lai atbalstītu kritiskās analīzes darbības. Kaut arī kritiskā analīze ietver galvenos dažādu lomu problemātiskos punktus un problēmas, to var izpildīt sistēmas administrators.

## <a name="demo-scenario"></a>Demonstrācijas scenārijs

HQUS juridiskā persona ražo augstas kvalitātes skaļruņus. Ražošanas procesa gaitā skaļruņi ir pakļauti tālāk aprakstītajiem trīs operāciju līmeņiem.

- **Iepriekšēja montāža** — tiek samontēts skaļruņa korpuss. Pirms operācijas sākšanas materiālu noliktavā tiek izdots korpusa materiāls.
- **Pārklāšana** — kad skaļruņa korpuss ir samontēts, tas ir jāpārklāj. Šo operācija pabeidz kreditors (apakšuzņēmējs). Iepriekš samontētais skaļruņa korpuss kopā ar diviem materiāliem tiek nosūtīts apakšuzņēmējam pārklāšanai.
- **Pabeigšana** — kad apakšuzņēmējs ir pārklājis iepriekš samontēto skaļruņa korpusu, tas tiek atgriezts HQUS juridiskajai personai, lai var pabeigt galīgo skaļruņa montāžu.

Nākamajā attēlā ir redzamas trīs operācijas un visi materiāli, kuri tajās tiek izmantoti.

![Operācija Iepriekšēja montāža, Pārklāšana un Pabeigšana un tajās izmantotie materiāli](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Iestatīt

Pirms kritiskās analīzes uzsākšanas ir jāiestata dati.

### <a name="set-up-the-finished-product"></a>Pabeigtās preces iestatīšana

Šajā sadaļā ir izskaidrots, kā iestatīt izlaisto preci D8100 “Pārklātais korpuss”.

1. Lai atvērtu lapu **Izlaisto preču detalizēta informācija**, atlasiet **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
2. Lai atrastu esošo izlaisto preci, ātrās filtrēšanas laukā ievadiet **D8100**.

    ![Izlaistās preces D8100 filtrēšana izlaisto preču detalizētas informācijas lapā](./media/subcontract02_filtering-released-products.png)

3. Lai atvērtu lapu **Maršruts**, darbību rūts cilnē **Inženieris** atlasiet **Maršruts**.

    Lapā **Maršruts** ir redzamas izlaistās preces D8100 astoņas maršruta versijas. Astoņas maršruta versijas tiek sadalītas četras maršrutos vietā Nr. 1 un Nr. 5. Maršruts 000400 tiek izmantots izmaksu aprēķināšanai, maršruts 00041 tiek izmantots, ja operācija Pārklāšana ir iekšēja operācija, un maršruts 00042 tiek izmantots, ja operācija Pārklāšana ir ārēja operācija.

    ![Astoņu maršruta versijas lapā Maršruts](./media/subcontract03_route-page.png)

4. Augšējās rūts režģī **Versijas** atlasiet maršruta versiju **00042** vietai **5**.
5. Apakšējās rūts režģa cilnē **Pārskats** atlasiet operāciju **20** (**Cbnt CtSc**).

    ![Atlasīta maršruta versijas 00042 operācija 20 vietai Nr. 5](./media/subcontract04_route-version-operation.png)

6. Atlasiet cilni **Vispārēji**.

    Ievērojiet, ka ir iestatīta lauka **Maršruta veids** opcija **Kreditors**. Šī vērtība norāda, ka operācija 20 (Cbnt CtSc) ir apakšlīgumā paredzēta operācija.

    ![Lauka Maršruta veids iestatījums Kreditors cilnē Vispārīgi](./media/subcontract05_general-tab.png)

7. Atlasiet cilni **Resursu pieprasījumi**.

    Parametrus izmanto, lai ražošanas plānošanas laikā atrastu attiecīgo resursu. Ievērojiet, ka operācijai 20 (Cbnt CtSc) ir nepieciešams resurss, kam ir divi parametri **Pārklāšana** un **Pārklāti korpusi**.

    ![Parametrs Pārklāšana un Pārklāti korpusi resursu pieprasījumu cilnē](./media/subcontract06_resource-requirements-tab.png)

8. Lai atvērtu dialoglodziņu **Izmantojamie resursi**, atlasiet **Izmantojamie resursi**.

    Atrasti ir trīs resursi, kas atbilst operācijas resursu pieprasījumiem. Ievērojiet, ka ir resursa 8851 un 8852 veids ir **Kreditors**.

    ![Trīs attiecīgie resursi dialoglodziņā Izmantojamie resursi](./media/subcontract07_applicable-resources-dialog.png)

9. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Izmantojamie resursi**, un atveriet atkal lapu **Maršruts**.
10. Aizveriet lapu **Maršruts**, lai atkal atvērtu lapu **Izlaistās preces detalizēta informācija**.

    ![Izlaistās preces detalizētas informācijas lapa](./media/subcontract08_released-product-details-page.png)

11. Lai atvērtu lapu **MK versijas**, darbību rūts cilnē **Inženieris** atlasiet **MK versijas**.

    Lapā **MK versijas** lapa ir redzami izlaistās preces D8100 četras materiālu komplektu (MK) versijas. MK 000040 izmanto izmaksu aprēķināšanai un plānošanai, MK 000041 izmanto, ja operācija Pārklāšana tiek veikta savā uzņēmumā, un MK 000042 un 000043 izmanto, ja operācija Pārklāšana ir paredzēta apakšlīgumā.

    Ievērojiet, ka krājums S8050 ir krājuma veida **Pakalpojums** prece. Šis krājums pārstāv apakšuzņēmēja darbu.

    ![Četras MK versijas MK versiju lapā](./media/subcontract09_bom-versions-page.png)

12. Lai atvērtu dialoglodziņu **MK rindas rediģēšana**, kopsavilkuma cilnē **Materiālu komplektu rindas** atlasiet **Rediģēt**.

    Kad ražošanas pasūtījums ir izveidots un novērtēts saskaņā ar izlaisto preci D8100, automātiski tiek ģenerēts krājuma S8050 pirkšanas pasūtījums. Šis pirkšanas pasūtījums tiek saistīts ar ražošanas pasūtījumu. Lai pirkšanas pasūtījumi tiktu ģenerēti automātiski, jāiestata lauka **Rindas veids** opcija **Kreditors** un apakšuzņēmējam jāatlasa kreditora konts. Šajā gadījumā kreditora konts ir US-801.

    Ievērojiet, ka MK rinda ir savienota ar darbību Pārklāšana, izmantojot operācijas numuru (šajā gadījumā 20).

    ![Dialoglodziņš MK rinda rediģēšana](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Noliktavā nodarbināto paroļu izveide

Noliktavā nodarbinātajiem, kuri izmanto pārnēsājamu ierīci, ir jānosaka parole.

1. Lai atvērtu lapu **Darba lietotāji**, atlasiet **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
2. Kopsavilkuma cilnē **Lietotāji** atlasiet lietotāja rindu **51**.

    ![Darba lietotāju lapa](./media/subcontract11_work-users-page.png)

3. Atlasiet **Atiestatīt paroli**.
4. Laukā **Parole** un **Apstiprināt paroli** ievadiet **1**.
5. Atlasiet **Iestatīt paroli**.

## <a name="step-by-step-walkthrough"></a>Kritiskā analīze soli pa solim

**Scenārijs un fons**

Ir izveidots preces D8100 “Pārklāts korpuss” 10 gabalu ražošanas pasūtījums. Korpusa pārklāšana ir apakšlīgumā paredzēta operācija, kuru izpilda kreditors US-801 Perfect Coating Solutions. Ražošanas pasūtījums ietver trīs operācijas. Pirmajā operācijā korpuss tiek iepriekš samontēts, operāciju veicot uz vietas uzņēmumā. Iepriekšējai montāžai nepieciešamais materiāls tiek izdots izejmateriālu noliktavā. Kad iepriekšējā montāža ir pabeigta, iepriekš samontētais korpuss tiek nosūtīts uzņēmumam Perfect Coating Solutions kopā ar diviem materiāliem, kuri ir nepieciešami operācijas Pārklāšana izpildei. Kad pārklātais korpuss tiek saņemts atpakaļ no kreditora, pirms ziņojuma par tā pabeigšanu sagatavošanas tas tiek apstrādāts uz vietas uzņēmumā galīgās montāžas operācijā.

1. Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.
2. Lai atvērtu dialoglodziņu **Ražošanas pasūtījumu izveide**, darbību rūtī atlasiet **Jauns ražošanas pasūtījums**.

    ![Dialoglodziņš Ražošanas pasūtījumu izveide](./media/subcontract12_create-production-order-dialog.png)

3. Laukā **Krājuma numurs** atlasiet **D8100**.
4. Kad krājuma numurs ir atlasīts, tiek parādīti krājumu dimensiju lauki. Laukā **Krāsa** atlasiet **Hroms**.

    Tiek parādīts ziņojuma lodziņš ar jautājumu, vai ir jāievada MK aktīvās versijas un maršruts.

    ![Ziņojuma lodziņš](./media/subcontract13_message-box.png)

5. Atlasiet **Jā**. 

    Dialoglodziņa **Ražošanas pasūtījumu izveide** laukā **MK numurs** un **Maršruta numurs** automātiski attiecīgi tiek atlasītas preces D8100 MK aktīvās versijas un maršruts. Šajā gadījumā tiek atlasīts MK **000040** un maršruts **000040**.
    
    > [!NOTE]
    > Gan MK, gan maršruta izmaksu aprēķināšanai un plānošanai izmanto versiju 000040.

6. Laukā **Vieta** atlasiet **5**.
7. Laukā **Noliktava** atlasiet **51**.
8. Laukā **MK numurs** un **Maršruta numurs** automātiski atlasīto vērtību mainiet uz **000042**.

    > [!NOTE]
    > Lai korpusa pārklāšanu ar apakšlīgumu nodotu kreditoram US-801, gan MK, gan maršrutam tiek izmantota versija 000042.

    ![Dialoglodziņā Ražošanas pasūtījumu izveide iestatītās vērtības](./media/subcontract14_create-production-order-dialog-set.png)

9. Lai izveidotu ražošanas pasūtījumu, atlasiet **Izveidot** un atgriezieties lapā **Visi ražošanas pasūtījumi**.

    ![Jauns ražošanas pasūtījums lapā Visi ražošanas pasūtījumi](./media/subcontract15_new-production-order.png)

10. Lai atvērtu dialoglodziņu **Aprēķināšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Aprēķināt**.

    ![Dialoglodziņš Aprēķināšana](./media/subcontract16_estimate-dialog.png)

11. Lai apstiprinātu aprēķinu, atlasiet **Labi** un atgriezieties lapā **Visi ražošanas pasūtījumi**.

    > [!NOTE]
    > Kad ražošanas pasūtījums ir aprēķināts, kreditoram US-801 tiek ģenerēts pakalpojuma krājuma S8050 pirkšanas pasūtījums.

12. Lai atvērtu lapu **MK**, kur var skatīt ražošanas pasūtījuma MK rindas, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **MK**.

    Ievērojiet, ka pakalpojama krājumam S8050 ir pievienota atsauce uz pirkšanas pasūtījumu, kas tika ģenerēts, kad tikai aprēķināts ražošanas pasūtījums.

    ![Ražošanas pasūtījuma MK rindas MK lapā](./media/subcontract17_production-order-bom-lines.png)

13. Lai atgrieztos lapā **Visi ražošanas pasūtījumi**, aizveriet lapu **MK**.
14. Lai atvērtu dialoglodziņu **Darba grafika izveide**, darbību rūts cilnē **Grafiks** atlasiet **Izveidot darbu grafiku**.
15. Norādiet šādas vērtības:

    - Laukā **Plānošanas virziens** atlasiet **Sākot no rītdienas**.
    - Iestatiet opcijas **Ierobežota noslodze** vērtību **Jā**.

    ![Dialoglodziņš Darba grafika izveide](./media/subcontract18_job-scheduling-dialog.png)

16. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Darba grafika izveide**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.
17. Darbību rūts cilnē **Grafiks** atlasiet **Ganta diagramma**, lai atvērtu lapu **Ganta diagramma — resursu skats**.

    Ganta diagramma sniedz vizuālu pārskatu par to, kā tiek izveidots grafiks par ražošanas darbiem, kas saistīti ar resursiem. Ievērojiet, ka ārējā operācija Pārklāšana ietver trīs darbus: procesa darbu, transportēšanas darbu un gaidīšanas laika darbu.

    ![Ganta diagramma lapā Ganta diagramma — resursu skats](./media/subcontract19_gantt-chart.png)

18. Lai atgrieztos lapā **Visi ražošanas pasūtījumi**, aizveriet lapu **Ganta diagramma — resursu skats** lapu.
19. Lai atvērtu dialoglodziņu **Izlaišana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Izlaist**.

    ![Dialoglodziņš Izlaišana](./media/subcontract20_release-dialog.png)

20. Lai dialoglodziņu **Izlaišana** aizvērtu, atlasiet **Labi**.
21. Lai atvērtu dialoglodziņu **Automātiska MK un formulas rindu izlaide**, atlasiet **Ražošanas kontrole \> Regulārie uzdevumi \> Izlaišana uz noliktavu \> Automātiska MK un formulas rindu izlaide**.

    ![Dialoglodziņš Automātiska MK un formulas rindu izlaide](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Lai palaistu automātisko MK un formulas rindu darbu, atlasiet **Labi**.

    Šis darbs izlaiž izejmateriālu izdošanas uz noliktavu darbu.

23. Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.
24. Izmantojiet ātrās filtrēšanas lauku, lai atlasītu ražošanas pasūtījumu, pie kura strādājat.
25. Lai atvērtu lapu **Darbs**, darbību rūts cilnē **Noliktava** atlasiet **Darba detaļas**.

    Ievērojiet, ka lapā ir redzami divi izejmateriālu izdošanas darbu komplekti. Pirmais darbs attiecas uz materiālu M8100 un M8101. Šie materiāli tiek izmantoti operācijā 10. Otrais darbs attiecas uz materiālu M8202 un M8250. Šie materiāli tiek izmantoti operācijā 20, kas ir apakšlīgumā paredzētā darbība.

    ![Divi izejmateriālu izdošanas darbu komplekti lapā Darbs](./media/subcontract22_work-page.png)

26. Lai apstrādātu noliktavas darba operāciju 10, palaidiet noliktavas programmu.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.
28. Izmantojiet ātrās filtrēšanas lauku, lai atlasītu ražošanas pasūtījumu, pie kura strādājat.
29. Lai atvērtu dialoglodziņu **Sākšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Sākt**.
30. Cilnē **Vispārīgi** norādiet tālāk norādītās vērtības.

    - Laukā **No operācijas Nr.** atlasiet **10**.
    - Laukā **Uz operācijas Nr.** atlasiet **10**.

    ![Cilnē Vispārīgi iestatītās vērtības](./media/subcontract23_start-dialog.png)

31. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Sākšana**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.

    Ievērojiet, ka ražošanas pasūtījuma statuss tagad ir **Sākts**. Operācijai 10 nepieciešamie materiāli tiek izmantoti pēc izdošanas saraksta žurnāla automātiskas grāmatošanas. Laika patēriņš darbībai 10 tiek uzskaitīts pēc maršruta karšu žurnāla automātiskas grāmatošanas.

32. Lai apstrādātu noliktavas darba operāciju 20, palaidiet noliktavas programmu.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Lai atvērtu dialoglodziņu **Sākšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Sākt**.
34. Cilnē **Vispārīgi** norādiet tālāk norādītās vērtības.

    - Laukā **No operācijas Nr.** atlasiet **20**.
    - Laukā **Uz operācijas Nr.** atlasiet **20**.
    - Laukā **Daudzums** ievadiet **10**.
    - Iestatiet opcijas **Grāmatot izdošanas sarakstu tagad** vērtību **Nē**.

    ![Cilnē Vispārīgi iestatītās vērtības](./media/subcontract24_general-tab.png)

35. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Sākšana**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.

    Tiek izveidots operācijā Pārklāšana izmantoto materiālu un pakalpojumu krājuma izdošanas saraksts. Pakalpojumu krājums pārstāv apakšlīgumā paredzētās operācijas izmaksas.

36. Darbību rūts cilnē **Skats** atlasiet **Izdošanas saraksts**, lai atvērtu lapu **Izdošanas saraksts**.
37. Atlasiet izdošanas sarakstu, kas nav iegrāmatotas, un pēc tam atlasiet žurnāla numuru, lai skatītu žurnāla rindas.

    ![Žurnāla rindas lapā Izdošanas saraksts](./media/subcontract25_picking-list.png)

38. Darbību rūtī atlasiet **Drukāt** \> **Izdošanas saraksta pārskats**, lai atvērtu dialoglodziņu **Izdošanas saraksta pārskats**.
39. Iestatiet opcijas **Izmantot piegādes pavadzīmes izkārtojumu** vērtību **Jā**.

    ![Dialoglodziņš Izdošanas saraksta pārskats](./media/subcontract26_picking-list-report-dialog.png)

40. Lai ģenerētu pārskatu **Izdošanas saraksts**, atlasiet **Labi**.

    Šajā gadījumā kreditora piegādes pavadzīme tiek drukāta no ražošanas izdošanas saraksta žurnāla. Piegādes pavadzīmē ir norādīti materiāli, kas tiek nosūtīti kreditoram, kurš veic operāciju Pārklāšana.

    ![Izdošanas saraksta pārskats](./media/subcontract27_picking-list-report.png)

41. Lai atgrieztos lapā **Izdošanas saraksts**, aizveriet pārskatu **Izdošanas saraksts**.
42. Darbību rūtī atlasiet **Grāmatot**, lai atvērtu dialoglodziņu **Žurnāla grāmatošana**.

    ![Dialoglodziņš Žurnāla grāmatošana](./media/subcontract28_post-journal-dialog.png)

43. Lai dialoglodziņu **Žurnāla grāmatošana** aizvērtu, atlasiet **Labi**.
44. Atveriet pirkšanas pasūtījumu.

    ![Pirkšanas pasūtījuma lapa](./media/subcontract29_purchase-order-page.png)

45. Darbību rūts cilnē **Pirkums** atlasiet **Apstiprināt**.
46. Atlasiet **Grāmatot**, lai atvērtu dialoglodziņu **Žurnāla grāmatošana**.
47. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Žurnāla grāmatošana**, un atveriet atkal lapu **Pirkšanas pasūtījums**.
48. Mainiet vienības cenu no **33** uz **40**.

    ![Pirkšanas pasūtījuma lapā mainīta vienības cena](./media/subcontract30_unit-price.png)

49. Vēlreiz apstipriniet pirkšanas pasūtījumu.
50. Preces ieejas plūsma.

    ![Dialoglodziņš Preces ieejas plūsmas grāmatošana](./media/subcontract31_posting-product-receipt-dialog.png)

51. Pirkšanas rēķins.
52. Atjauniniet atbilstības statusu.

    ![Kreditora rēķinu lapa](./media/subcontract32_vendor-invoice-page.png)

53. Sniedziet pārskatu, ka prece ir pabeigta.

    ![Dialoglodziņš Pārskata par preces pabeigšanu sniegšana](./media/subcontract33_report-as-finished-dialog.png)

54. Nobeidziet procesu.

    ![Dialoglodziņš Beigšana](./media/subcontract34_end-dialog.png)

55. Izmaksu salīdzinājums.

    ![Izmaksu salīdzinājuma diagrammas](./media/subcontract35_cost-comparison-charts.png)

Trūkstoši datu iestatījumi.

