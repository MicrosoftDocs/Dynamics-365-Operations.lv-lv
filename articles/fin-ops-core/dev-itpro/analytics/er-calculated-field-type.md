---
title: Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.
description: Šī tēma sniedz informāciju par to, kā izmantot Aprēķināto lauka tipu ER datu avotiem.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1c2c13cd3f165826e0d5b5ac901ffa61895301e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569205"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.

[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā var izveidot Elektronisko pārskatu (ER) datu avotu, izmantojot **Aprēķināto lauka** tipu. Šis datu avots var saturēt ER izteiksmi, ko aktivizējot, var kontrolēt ar parametra argumentu vērtībām, kas konfigurētas saistījumā, kas izsauc šo datu avotu. Konfigurējot šāda datu avota parametru izsaukumus, var atkārtoti izmantot vienu datu avotu daudzos saistījumos, kas samazina kopējo datu avotu skaitu, kas ir jākonfigurē ER modeļu kartēšanas vai ER formātos. Tas arī vienkāršo konfigurēto ER komponentu, kas samazina uzturēšanas izmaksas, kā arī izmaksas, kas saistītas ar citiem patērētājiem.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.

- Piekļuve vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir bijusi nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.

| **Saturs**                           | **Faila nosaukums**                                        |
|---------------------------------------|------------------------------------------------------|
| Parauga ER datu modeļa konfigurācija    | [Modelis, lai uzzinātu parametru izsaukumus.versija.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Parauga ER metadatu konfigurācija      | [Metadati, lai uzzinātu parametru izsaukumus.versija.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Parauga ER modeļa kartējuma konfigurācija | [Kartēšana, lai uzzinātu parametru izsaukumus.versija.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Parauga ER formāta konfigurācija        | [Formāts, lai uzzinātu parametru izsaukumus.versija.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Piesakieties savā RCS instancē.
Šajā piemērā jūs izveidosiet konfigurāciju parauga uzņēmumam “Litware, Inc.”. Pirmkārt, lai izpildītu šīs darbības RCS instancē, ir jāizpilda sekojošie soļi procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana ar aktīvu statusu](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Importējiet lejupielādētās konfigurācijas uz RCS šādā secībā: datu modelis, metadati, modeļa kartēšana, formāts. Veiciet šādas darbības katrai ER konfigurācijai:

    1. Atlasiet **Mainīt**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, un tad atlasiet nepieciešamo ER konfigurāciju XML formātā.
    4. Atlasiet **Labi**.

## <a name="review-the-provided-er-solution"></a>Pārskatiet sniegto ER risinājumu.

### <a name="review-model-mapping"></a>Pārskatiet modeļa kartēšanu.

1. Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2. Atlasiet **Kartēšana, lai uzzinātu parametru izsaukumus**.
3. Atlasiet **Noformētājs**.
4. Atlasiet **Noformētājs**.  
   
    Šī ER modeļa kartēšana ir veidota, lai veiktu šādas darbības:

    - Izgūt nodokļu kodu sarakstu (**Nodokļu** datu avots), kas atrodas tabulā **TaxTable**.
    - Izgūt nodokļu transakciju kodu sarakstu (**Trans** datu avots), kas atrodas tabulā **TaxTrans**:
    
        - Grupēt ienesto transakciju sarakstu (**Gr** datu avots) pēc nodokļu koda.
        - Aprēķināt apkopotās vērtības grupētām transakcijām pēc nodokļu koda:

            - Nodokļu bāzes vērtību summa.
            - Nodokļu vērtību summa.
            - Piemērotās nodokļa likmes minimālā vērtība.

    Modeļa kartēšana šajā konfigurācijā implementē pamatdatu modeli jebkuram no šajā modelī izveidotajiem ER formātiem un ir izpildīts Finance and Operations. Tādējādi **Nodokļu** un **Gr** datu avotu saturs ir pakļauts ER formātiem, piemēram, abstraktiem datu avotiem.

    ![Modeļa kartēšanas veidotāja lapa, kurā parādīti Tax un Gr datu avoti](media/er-calculated-field-type-01.png)

5.  Aizveriet lapu **Modeļa kartējuma noformētājs**.
6.  Aizveriet lapu **Modeļa kartēšana**.

### <a name="review-format"></a>Pārskata formāts

1. Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2. Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.
3. Atlasiet **Noformētājs**. Šī ER formāta kartēšana ir veidota, lai veiktu šādas darbības:

    - Izveidot nodokļu paziņojumu xml formātā.
    - Parādīt sekojošos nodokļu līmeņus nodokļu pārskatā: parasts, samazināts un nav.
    - Parādīt vairākas detaļas katrā nodokļu līmenī, kam katrā līmenī ir dažāds šo detaļu skaits.

    ![Formāta veidotāja lapa](media/er-calculated-field-type-02.png)

4. Atlasīt **Kartēšana**.
5. Izvērst **modeli**, **datus** un **kopsavilkuma** elementus. 

    Aprēķinātā lauka **Model.Data.Summary.Level** ir izteiksme, kas atgriež nodokļu līmeņa kodu (**Parasts**, **Samazināts**, **Nav** vai **cits**) kā teksta vērtība jebkuram nodokļa kodam, ko var izgūt no **Model.Data.Summary** datu avota izpildes laikā.

    ![Formāta veidotāja lapa, kas uzrāda Dara model modeļa detaļas, lai apgūtu parametru izsaukumus.](media/er-calculated-field-type-03.png)

6. Izvērsiet **Modeli**.**Data2** krājums.
7. Izvērsiet **Modeli**.**Data2.Summary2** krājums.
   
    **Modeļa**.**Data2. Summary2** datu avots ir konfigurēts, lai grupētu **Model.Data.Summary** kopsavilkuma datu avota transakcijas detalizētu informāciju pēc taksācijas līmeņa (atgriezis **Model.Data.Summary.Level** aprēķinātais lauks) un aprēķinātu apkopojumus.

    ![Formāta veidotāja lapa, kas rāda detalizētu informāciju par Model.Data2.Summary2 datu avotu.](media/er-calculated-field-type-04.png)

8. Pārskatīt aprēķināto lauku **Modelis**.**Data2.Level1**, **Modelis**.**Data2.Level2** un **Modelis**.**Data2. Level3.** Šie aprēķinātie lauki tiek izmantoti **Modeļa** filtrēšanai.**Data2.Summary2** ieraksti saraksts un atgriezt tikai tos ierakstus, kas atbilst noteiktam nodokļu līmenim.
9. Aizveriet lapu **Formāta veidotājs**.

## <a name="create-a-derived-format"></a>Atvasināta formāta izveide
Varat uzlabot norādīto formātu, pievienojot vienu aprēķināto lauku, lai filtrētu nepieciešamo nodokļu līmeni, nevis izmantotu esošos trīs laukus: **Modelis**.**Data2.Level1**, **Modelis**.**Data2.Level2** un **Modelis**.**Data2.Level3**. Nepieciešamo nodokļu līmeni var norādīt vietā, kur tiks izsaukts šis jaunais aprēķinātais lauks.

1. Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2. Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.
3. Atlasiet **Izveidot konfigurāciju**.
4. Atlasiet **Atvasināt no nosaukuma: formatēt, lai uzzinātu parametru izsaukumus, Microsoft**.
5. Laukā **Nosaukums** ievadiet **Formāts parametru izsaukumu (klentu) apgūšanai**.
6. Atlasiet **Izveidot konfigurāciju**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigurēt parametru aprēķināto lauku, kas atgriež ierakstu sarakstu.

### <a name="start-adding-a-new-calculated-field"></a>Sākt pievienot jaunu aprēķināto lauku

1. Atlasiet **Noformētājs**.
2. Atlasiet **Izvērst/sakļaut**, lai izvērstu visus formāta vienumus.
3. Atlasiet **Kartēšana**.
4. Izvērsiet **Modelis** vienumu.
5. Atlasiet **Model.Data2** vienumu.
6. Atlasiet **Pievienot**.
7. Atlasiet **Funkcijas\\Aprēķinātais lauks**.
8. Laukā **Nosaukums** ievadiet **Līmeņi**.
9. Atlasiet **Rediģēt formulu**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definējiet aprēķinātā lauka pievienošanas parametru

1. Atlasiet **Parametri**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.
4. Laukā **Tips** atlasiet **Virkne**.

    Lai norādītu parametra argumenta tipu, var izmantot tikai primitīvos datu tipus. Tāpēc **Ierakstu saraksts**, **Ieraksts** un **Uzskaitījums** tipus šim nolūkam nevar izmantot.

    Maksimālais parametru skaits, ko var norādīt vienam aprēķinātajam laukam, ir 8.

    ![Parametru datu avota saraksts](media/er-calculated-field-type-05.png)

5. Atlasiet **Labi**.

Pievienojot šo parametru, jūs norādiet nosacījumu, kam jābūt, lai izsauktu šo aprēķināto lauku. Kad izsaucat šo aprēķināto lauku, ir jānorāda **Nodokļu līmeņa** parametra arguments kā vērtība ar **Virknes** formātu.

   Pārliecinieties, vai nosakāt parametrus tikai tiem aprēķinātajiem laukiem, kas atrodas konteinerā (vai nu **Ierakstu sarakstā**, **Ierakstā** vai **Konteinerā**).

   Konfigurētais parametrs ir pieejams datu avotu sarakstā šim aprēķinātajam laukam. Varat pievienot parametru konfigurētajai izteiksmei, atlasot **Pievienot datu avotu**.

   ![Datu avota lauki](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definēt aprēķinātā lauka pievienošanas izteiksmi

1. Laukā **Fomula** ievadiet: 

    **KUR (\@. Summary2, \@. Summary2. grupēts. līmenis =**
    
2. Atlasiet **Nodokļu līmeņa** parametru datu avotu sarakstā.
3. Atlasiet **Pievienot datu avotu**.
4. Laukā **Formula** pabeidziet izteiksmi ar:  

    **KUR(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. Atlasiet **Saglabāt**.

    ![Datu avota lauka informācija](media/er-calculated-field-type-07.png)

6. Aizveriet lapu **Formāta veidotājs**.

### <a name="finish-adding-a-new-calculated-field"></a>Pabeigt pievienot jaunu aprēķināto lauku

- Atlasiet **Labi**.

Lapā **Formāta veidotājs** konfigurētajam parametru aprēķinātajam laukam **Līmeņi** nepieciešams **Virknes** arguments.

![Izvērsts aprēķināto lauku līmeņu saraksts](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Izmantojiet konfigurēto aprēķināto lauku saistījuma formāta elementiem

1. Atlasiet **Model.Data2.Levels**, lai atlasītu konfigurēto aprēķināto lauku.
2. Atlasiet **Statement.Taxation.Regular** formāta elementu.
3. Atlasiet **Saistīt**.
4. Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota **Level1** aizstāšanu ar jauno avotu **Līmeņi** visos atlasītā formāta elementa ligzdotu formātu elementos.

    Piemērotais saistījums ir izveidots kā izsaukums aprēķinātajam parametru laukam. Pēc noklusējuma saistītā formāta elementa nosaukums tiek izmantots kā arguments parametru aprēķinātajam laukam šādos apstākļos:

      - Aprēķinātais lauks ir konfigurēts, lai izmantotu vienu parametru.
      - Šī parametra datu tips ir definēts kā **Virkne.**

    Ja saistītā formāta elementa nosaukums ir tukšs, lietotajā saistījumā tiek izmantots šī elementa datu avota nosaukums.

5. Atlasiet **Statement.Taxation.Reduced** formāta elementu.
6. Atlasiet **Saistīt**.
7. Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota **Level2** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.
8. Atlasiet **Statement.Taxation.None** formāta elementu.
9. Atlasiet **Saistīt**.
10. Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota **Level3** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.

   Norādot aprēķinātā lauka parametru argumentu XML elementam, kas apzīmē nodokļu līmeni (piemēram, **Model.Data2.Levels("Reduced")** kā teksta vērtība), jums nav jādara tas pats ligzdotajiem XML atribūtiem — to saistījumi automātiski mantos argumenta vērtību, kas definēta pamatlīmenī (**Model.Data2.Levels.aggregated.Base**, nevis **Model.Data2.Levels("Reduced").aggregated.Base**).

Jebkura parametra aprēķinātā lauka atkārtotie izsaukumi netiek atbalstīti.

Varat atlasīt **Rediģēt formulu** un mainīt noklusējuma argumenta aprēķināto parametru, kas lietots atlasītajā saistījumā. Ja šī argumenta nav, tas var radīt kļūdas izpildes laikā — lietotāji tiek informēti par šādu situāciju, kad pašreizējais formāts ir apstiprināts.

![Apstiprinājuma brīdinājuma paziņojums](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Konfigurēt parametru aprēķināto lauku, lai atgrieztu ierakstu.
Kad aprēķinātais parametru lauks atgriež ierakstu, jums ir jāatbalsta atsevišķu šī ieraksta lauku saistījums, lai formatētu elementus. Šādos gadījumos nebūs pamata saistījuma, kas ietver argumenta vērtību, lai izsauktu aprēķināto parametru lauku — šī vērtība ir jādefinē viena ieraksta lauka saistījumā.

### <a name="start-adding-a-new-calculated-field"></a>Sākt pievienot jaunu aprēķināto lauku

1. Atlasīt **Model.Data2** vienumu.
2. Atlasiet **Pievienot**.
3. Atlasiet **Funkcijas\\Aprēķinātais lauks**.
4. Laukā **Nosaukums** ievadiet **LevelRecord**.
5. Atlasiet **Rediģēt formulu**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definēt aprēķinātā lauka pievienošanas parametru

1. Atlasiet **Parametri**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.
4. Laukā **Tips** atlasiet **Virkne**.
5. Atlasiet **Labi**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definēt aprēķinātā lauka pievienošanas izteiksmi

1. Laukā **Formula** ievadiet šādu izteiksmi:  
    
    **FIRSTORNULL (\@.Līmeņi(**

2. Atlasiet **Nodokļu līmenis** parametru.
3. Atlasiet **Pievienot datu avotu**.
4. Laukā **Formula** pievienojiet **'Nodokļu līmenis'))**, ko ievadījāt 1. solī, lai pabeigtu izteiksmi:  
    
    **FIRSTORNULL (\@.Līmenis('Nodokļu līmenis'))**

5. Atlasiet **Saglabāt**.
6. Aizveriet lapu **Formāta veidotājs**.

### <a name="finish-adding-a-new-calculated-field"></a>Pabeigt pievienot jaunu aprēķināto lauku

-   Atlasiet **Labi**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Izmantojiet konfigurēto aprēķināto lauku, lai saistītu formāta elementus.

1. Izvērsiet **Model.Data2.LevelRecord**, lai atlasītu konfigurēto aprēķināto lauku.
2. Izvērsiet **Model.Data2.LevelRecord.aggregated** konfigurēto aprēķinātā lauka konteineru.
3. Atlasiet **Model.Data2.LevelRecord.aggregated.Base** lauku.
4. Atlasiet **Statement.Taxation.None** formāta elementu.
5. Atlasiet **Atsaistīt**.
6. Atlasiet **Statement.Taxation.None.Base** formāta elementu.
7. Atlasiet **Saistīt**.
8. Atlasiet **Rediģēt formulu**.
9. Mainiet izteiksmi uz **Model.Data2.LevelRecord("None").aggregated.Base**.

![Atjauninātā izteiksme](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Noņemt aprēķinātos laukus, kas netiek lietoti

1. Atlasiet **Model.Data2.Level1**.
2. Atlasiet **Dzēst**.
3. Atlasiet **Model.Data2.Level2**.
4. Atlasiet **Dzēst**.
5. Atlasiet **Model.Data2.Level3**.
6. Atlasiet **Dzēst**.
7. Atlasiet **Saglabāt**.

  > [!NOTE]
  > Jūs atkārtoti izmantojāt to pašu aprēķināto lauku **Model.Data2.Levels** formāta saistījumos. Ir daudz vieglāk lietot un uzturēt vienu aprēķināto lauku, nekā darīt to pašu vairākiem līdzīgiem laukiem.

8. Aizveriet lapu **Formāta veidotājs**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Pabeigta atvasinātā formāta pielāgota versija

1. Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.
2. Atlasiet **Pabeigt**.

## <a name="export-completed-version-of-a-derived-format"></a>Eksportēt atvasinātā formāta pabeigtu versiju.

1. Atlasiet **Formatēt, lai uzzinātu parametru izsaukumu (pielāgots)** formātu konfigurācijas kokā.
2. Kopsavilkuma cilnē **Versijas** atlasiet pabeigto versiju 1.1.1.
3. Atlasiet **Maiņa**.
4. Atlasiet **Eksportēt kā XML failu**.
5. Saglabājiet lejupielādēto konfigurāciju lokāli XML formātā.

## <a name="test-er-formats"></a>Testa ER formāti 
Jūs varat palaist sākotnējos un uzlabotos ER formātus, lai pārliecinātos, ka konfigurētie parametru aprēķinātie lauki darbojas pareizi.

### <a name="import-er-configurations"></a>ER konfigurāciju importēšana
Jūs varat importēt pārskatītās konfigurācijas no RCS, izmantojot **RCS** tipa ER repozitoriju. Ja esat jau izgājis darbības tēmā, [Importēt elektronisko pārskatu (EP) konfigurācijas no Regulatory Configuration Services (RCS)](rcs-download-configurations.md), izmantojiet konfigurēto ER repozitoriju, lai importētu konfigurācijas, kas iepriekš šajā tēmā jau apspriestas. Pretējā gadījumā rīkojieties sekojoši:

1. Atlasiet **DEMF** uzņēmumu un noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Importējiet konfigurācijas no Microsoft Download Center šādā secībā: datu modelis, modeļa kartēšana, formāts. Veiciet šādas darbības katrai ER konfigurācijai:

    1. Atlasiet **Mainīt**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atlasītu nepieciešamo ER konfigurāciju XML formātā.
    4. Atlasiet **Labi**.

4. Importēt eksportētā **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)** formāta no RCS pabeigtās 1.1.1. versijas:

    1. Atlasiet **Mainīt**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atlasītu lokāli saglabāto failu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)** XML formātā.
    4. Atlasiet **Labi**.

### <a name="run-er-formats"></a>Palaidiet ER formātus

1. Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.
2. Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.
3. Atlasiet **Palaist** visaugstākajā lentē.
4. Saglabāt lokāli ģenerēto izvadi.
5. Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)**.
6. Atlasiet **Palaist** visaugstākajā lentē.
7. Saglabāt lokāli ģenerēto izvadi. 
8. Salīdziniet ģenerēto rezultātu saturu.

## <a name="additional-resources"></a>Papildu resursi

- [Formulas veidotājs elektronisko pārskatu veidošanā (ER)](general-electronic-reporting-formula-designer.md)
- [Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]