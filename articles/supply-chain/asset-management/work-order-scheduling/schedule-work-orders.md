---
title: Plānot darba pasūtījumus
description: Šajā tēmā ir aprakstīts, kā plānot darba pasūtījumus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderSchdulePreviewPart, EntAssetWorkOrderScheduleExclusively, EntAssetWorkOrderSchduleInfoPart, EntAssetWorkOrderScheduleListPage, EntAssetWorkOrderSchedule, EntAssetWorkOrderScheduleDelete
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: becd06c46afd92bf07d9a69147b7768e780aefa57f9045c11698c04154d6ddb8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718063"
---
# <a name="schedule-work-orders"></a>Plānot darba pasūtījumus

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir aprakstīts, kā plānot darba pasūtījumus Līdzekļu pārvaldībā. 

Nepieciešamo stundu skaitu darba pasūtījumam definē prognozēto stundu summa mīnus grāmatotās stundas. Ja ir nepieciešams vairāk laika, prognoze attiecīgi ir jāpielāgo. Sadaļā **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi** varat skatīt vai rediģēt prognozes darba pasūtījumam, atlasot to un noklikšķinot uz **Prognoze** cilnē **Darba pasūtījums**. Kad darba pasūtījumi ir izveidoti un novērtēti, nākamā darbība ir piešķirt tiem uzturēšanas speciālistus un rīkus to izpildei.

Var ieplānot tikai tos darba pasūtījumus, kuriem ir tāds darba pasūtījuma dzīves cikla stāvoklis, kas ļauj ieplānot. Ieplānošanas atļauja tiek iestatīta ar sadaļas **Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Dzīves cikla stāvokļi** > kopsavilkuma cilnes **Vispārīgi** > pārslēgšanas pogu **Atļaut ieplānošanu**.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi**.

2. Sarakstā atlasiet darba pasūtījumus, kurus vēlaties ieplānot. Sarakstu var kārtot, piemēram, pēc **Pašreizējā dzīves cikla stāvokļa**.

3. Cilnē **Vispārīgie iestatījumi** noklikšķiniet uz **Ieplānot**.

4. Dialoglodziņā grafika **Ieplānot darba pasūtījumus** varat pievienot atlases saistībā ar paredzēto sākuma datumu un pakalpojuma līmeni, ja nepieciešams. Ja plānošanas procesam ir jāievēro noslodzes ierobežojumi attiecībā uz resursiem, kas jau ir ieplānoti citiem darbiem, pārliecinieties, ka pārslēgšanas pogas **Līdzeklis**, **Rīks** un **Darbinieks** ir iestatītas uz “Jā”.

    [!NOTE]
    Ja pārslēgšanas pogas **Līdzeklis**, **Rīks** un **Darbinieks** iestatāt uz “Nē”, esošās rezervācijas tiks ignorētas. Informācijas žurnālā tiek parādīts saraksts ar darba pasūtījumu grafikiem, kas pārklājas, un jūs varat noklikšķināt uz ziņojumiem, lai atvērtu darba pasūtījumu un pārplānotu to, ja nepieciešams.

5. Lai skatītu vairāk informācijas par plānošanas procesu, pārslēgšanas pogai **Izvērsts** atlasiet vērtību “Jā”. Tas nozīmē, ka detalizēta informācija par aprēķinātajiem darba pasūtījumu un uzturēšanas speciālistu rādītājiem tiks parādīta informācijas žurnālā.

6. Noklikšķiniet uz **Labi**, lai sāktu plānošanas procesu.

7. Kad plānošana ir pabeigta, informācijas žurnālā tiek parādīts plānoto darba pasūtījumu skaits, kā arī detalizēta informāciju, ja pārslēgšanas poga **Izvērsts** tika iestatīta uz “Jā”.

>[!NOTE]
>Darba pasūtījumi tiek ieplānoti vienā ciklā uz darba pasūtījumu, nevis uz darba pasūtījuma uzdevumu. Dialoglodziņu **Ieplānot darba pasūtījumus** varat atvērt arī tieši sadaļā **Līdzekļu pārvaldība** > **Periodiskās darbības** > **Darba pasūtījumi** > **Ieplānot darba pasūtījumus**. Veiciet atlasi un noklikšķiniet uz **Labi**, lai sāktu darba pasūtījuma plānošanu. Darba pasūtījuma plānošanu ir iespējams iestatīt kā pakešuzdevumu dialoglodziņā **Ieplānot darba pasūtījumus** > kopsavilkuma cilnē **Palaist fonā**.

*Piemērs:* tālāk dotajā attēlā formula, kas ievietota laukā **Paredzētais sākums**, ģenerēs darba pasūtījumu plānošanu visiem darba pasūtījumiem ar paredzēto sākuma datumu nedēļu no šī brīža un vēlāk. Šī formula var būt noderīga, ja palaižat darba pasūtījumu plānošanu pastāvīgi, bet vēlaties pārliecināties, ka darba pasūtījumi, kas ieplānoti nākamajām 5–6 dienām, netiks pārplānoti.

![1. attēls.](media/03-work-order-scheduling.png)

Darba pasūtījuma tips, kas saistīts ar darba pasūtījumiem, var iestatīt plānošanu vienam uzturēšanas speciālistam (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Darba pasūtījumu tipi** > **Viena uzturēšanas speciālists** pārslēgšanas pogai ir iestatīta uz “Jā”). Tas nozīmē, ka, ja darba pasūtījuma tips tiek izmantots darba pasūtījumā, pārslēgšanas poga **Viens uzturēšanas speciālists** automātiski tiek iestatīta uz “Jā” detalizētas informācijas lapā **Visi darba pasūtījumi** > skatā **Virsraksta** > kopsavilkuma cilnē **Ieplānot**. Darba pasūtījuma plānošanas laikā visi darba pasūtījuma uzdevumi, kas izveidoti darba pasūtījumā, pēc tam tiks ieplānoti vienam un tam pašam uzturēšanas speciālistam. Ja nepieciešams, varat rediģēt atlasi ar pārslēgšanas pogu **Viens uzturēšanas speciālists** sadaļā **Visi darba pasūtījumi**, lai atļautu vairāku vai vienu darbinieku ieplānošanu darba pasūtījuma uzdevumiem.

Plānošanas process Līdzekļu pārvaldībā ietver vairākus faktorus plānošanas aprēķinā.

- Aprēķina rādītājus gan darba pasūtījumiem, gan uzturēšanas speciālistiem. Rādītāji darba pasūtījumiem un uzturēšanas speciālistiem tiek iestatīti sadaļā **Līdzekļu pārvaldības parametri**. 
- Tiek pārbaudīts, vai atbilst zināšanas, prasmes un sertifikāti, kas nepieciešami uzdevuma veikšanai. Prasmes un sertifikāti uzturēšanas speciālistiem tiek iestatīti modulī **Cilvēkresursi** modulī (**Cilvēkresursi** > **Darbinieki** > **Darbinieki** > atlasiet sarakstā darbinieku > cilnē **Darbinieks** > ar sadaļas **Zināšanas** > **Prasmes** un **Sertifikāti** pogām). Prasmes un sertifikātus var pievienot arī uzturēšanas darbu tipiem un uzturēšanas darbu darījumiem. Vairāk informācijas par zināšanām un uzturēšanas darbu tipiem lasiet sadaļā [Uzturēšanas darbu tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu darījumi un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Darba pasūtījumu plānošanā izmantotie rādītāji

Darba pasūtījuma uzdevumu rādītāju aprēķināšana ir balstīta uz paredzēto sākuma datumu un darba pasūtījuma pakalpojuma līmeni.

**Sākuma datuma** aprēķins: katram nākotnes datumam, kas aprēķināts no paredzēta sākuma datuma, sākuma datuma rādītājs tiek atņemts un reizināts ar rādītāju, kas tālākajos piemēros ir “10”.

**Kritiskuma** aprēķins: kritiskais rādītājs, kas reizināts ar darba pasūtījuma kritiskumu.

**Pakalpojuma līmeņa** aprēķins: pakalpojuma līmeņa rādītājs tiek dalīts ar pakalpojuma līmeni darba pasūtījumā.

Tālāk norādītajos piemēros kritiskais rādītājs ir “2”, un pakalpojuma līmeņa rādītāji ir “5“ un “100”.

**1. piemērs:**

| Darba pasūtījuma ID | Plānotais sākuma datums | Darba pasūtījuma kritiskums | Darba pasūtījuma pakalpojuma līmenis | Aprēķins               | Skaits      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Rītdien            | 2.                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Divas dienas no šodienas   | 2.                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Divas dienas no šodienas   | 3.                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Darba pasūtījumi tiks ieplānoti tālāk norādītajā secībā: WO-000108 **16**, WO-000108 **18**, WO-000108 **17**.

**2. piemērs:**

| Darba pasūtījuma ID | Plānotais sākuma datums | Darba pasūtījuma kritiskums | Darba pasūtījuma pakalpojuma līmenis | Aprēķins                 | Skaits    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Rītdien            | 2.                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Divas dienas no šodienas   | 2.                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Divas dienas no šodienas   | 3.                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Ja pakalpojuma līmeņa rādītājs tiek palielināts līdz “100”, nevis “5”, tad plānošanas kārtība būs: WO-000108 **18**, WO-000108 **16**, WO-000108 **17**.

Vērtējuma rādītāji, kas attiecas uz aprēķināšanu, kuriem uzturēšanas speciālistiem būtu jāstrādā ar darba pasūtījumiem, ir iestatīti kā skaitļi, kas tiek pievienoti katram uzturēšanas speciālistu aprēķinam darba pasūtījuma plānošanas laikā. Darba pasūtījumam tiek atlasīts uzturēšanas speciālists ar augstāko rādītāju. Tālāk ir sniegts īss apraksts par uzturēšanas speciālistu rādītājiem.

| Uzturēšanas speciālista rezultāts| Apraksts |
|---|---|
| Atbildīgais nodarbinātais | Ja uzturēšanas speciālists tiek atlasīts kā atbildīgais darbinieks darba pasūtījumā, rādītājs tiek pievienots. |
| Atbildīgā uzturēšanas speciālistu grupa | Ja uzturēšanas speciālists tiek atlasīts kā daļā no uzturēšanas speciālistu grupas darba pasūtījumā, rādītājs tiek pievienots. |
| Vēlamais uzturēšanas speciālists         | Ja uzturēšanas speciālists tiek atlasīts kā vēlamais uzturēšanas speciālists līdzeklim, rādītājs tiek pievienots. |
| Vēlamā uzturēšanas speciālistu grupa   | Ja uzturēšanas speciālists ir daļa no vēlamo uzturēšanas speciālistu grupas līdzeklim, rādītājs tiek pievienots.  |
| Vieta  | Ja jūsu uzņēmums izmanto funkcionālos novietojumus, uzturēšanas speciālisti saņem pilnu rādītāju skaitu, ja tie atrodas funkcionālajā novietojumā, kas saistīts ar līdzekli. Ja līdzekļa funkcionālajam novietojumam ir primārais novietojums, uzturēšanas speciālisti šajā funkcionālajā novietojumā saņem 1/2 rādītāju skaita. Ja arī šai atrašanās vietai ir vecākelements, uzturēšanas speciālisti šajā vietā saņem 1/3 rādītāju skaita. Ja arī šai atrašanās vietai ir vecākelements, uzturēšanas speciālisti šajā vietā saņem 1/4 rādītāju skaita un tā tālāk. Ja jūsu uzņēmums izmanto līdzekļu atrašanās vietu, kuru mēs neiesakām, lai aprēķinātu atrašanās vietas rezultātus, tiek izmantota atrašanās vieta, apgabals un zona. Darbinieki saņem pilnu punktu skaitu, ja tie atrodas atrašanās vietā un zonā, kas saistīta ar līdzekli. Ja darbinieka atrašanās vieta atbilst tikai atrašanās vietai un apgabalam, uzturēšanas speciālista vērtējuma rādītājs ir 2/3 no pilna rādītāju skaita. Ja uzturēšanas speciālista atrašanās vieta atbilst tikai atrašanās vietai, uzturēšanas speciālista vērtējuma rādītājs ir 1/3 no pilna rādītāju skaita. |
| Nodarbinātā pieņemšanas datums  | Katram datumam, kad ieplānotais sākuma datums ir vēlāk par paredzēto sākuma datumu, rādītājs tiek noņemts.  |

>[!NOTE]
>Ja rādītājs ir iestatīts kā “0”, šis rādītājs netiek aprēķināts. Tas ir noderīgi, ja, piemēram, plānošanā nevēlaties iekļaut atbildīgu darbinieku.

## <a name="competencies-used-in-work-order-scheduling"></a>Darba pasūtījumu plānošanā izmantotās zināšanas

Prasmju un sertifikātu prasības var tikt iestatītas uzturēšanas darba tipiem (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbi** > **Uzturēšanas darbu tipi**) un uzturēšanas darbu darījumiem (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbi** > **Uzturēšanas darbu darījums**). 

Uzturēšanas darbu tipi un uzturēšanas darbu darījumi tiek atlasīti darba pasūtījuma uzdevumiem. Ja prasmes un sertifikāti tiek atlasīti uzturēšanas darba tipam vai uzturēšanas darba darījumam un tie tiek izmantoti darba pasūtījuma uzdevumam, attiecīgajam darba pasūtījumam tiek ieplānoti tikai tādi uzturēšanas speciālisti, kuriem ir atbilstošas prasmes un sertifikāti.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Darbs ar plānotajiem darba pasūtījumiem, izmantojot Ganta diagrammu

**Ieplānoto darba pasūtījumu Ganta diagramma** sniedz grafisku interfeisu, kur varat skatīt un pārplānot savus darba pasūtījumus.

Lai skatītu un strādātu ar Ganta diagrammu:

1. Dodieties uz **Līdzekļu pārvaldība > Darba pasūtījumi > Plānoto darba pasūtījumu Ganta diagramma**.

1. Lietojiet nolaižamos sarakstus un laukus sadaļā **Iestatījumi**, lai iestatītu, kādu funkcionālo novietojumu, laika posmu un laika skalu, ko parādīt Ganta diagrammā.

1. Atlasiet **Lietot**.

    - Ganta diagrammas atjauninājumi, lai parādītu plānotos darba pasūtījumus, kas atbilst jūsu iestatījumiem. Katru darba pasūtījumu attēlo zils taisnstūris.
    - Lai pārplānotu parādīto darba pasūtījumu, atlasiet un pēc tam velciet to uz atbilstošo jauno datumu un laiku.

1. Ja veicāt izmaiņas, darbības rūtī noklikšķiniet uz **Saglabāt**, lai tās saglabātu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]