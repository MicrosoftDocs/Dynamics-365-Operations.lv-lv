---
title: Iestatīt ER formāta parametrus juridiskai personai
description: Šajā tēmā izskaidrots, kā iestatīt elektronisko pārskatu (ER) formātu parametrus juridiskai personai.
author: NickSelin
ms.date: 10/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9b57c6165e5de4a115818a135ed1455e3b05e3f0
ms.sourcegitcommit: 4b7e9d074e368a08d2f75482b722dce0c69a4bbd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/02/2021
ms.locfileid: "7733467"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Iestatīt ER formāta parametrus juridiskai personai

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Priekšnosacījumi

Lai veiktu šīs darbības, vispirms ir jāpabeidz darbības, kas aprakstītas tēmā [Konfigurēt ER formātus, lai izmantotu parametrus, kas konkretizēti juridiskai personai](er-app-specific-parameters-configure-format.md).

Lai izpildītu šīs tēmas piemērus, ir jābūt piekļuvei Microsoft Dynamics 365 Finance vienai no šādām lomām:

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

## <a name="import-er-configurations"></a>ER konfigurāciju importēšana
Lai importētu ER konfigurācijas, rīkojieties šādi. 

1. Pierakstieties savā vidē.
2. Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.
3. Atlasiet **Pārskatu konfigurācijas**.
4. Importējiet uz pašreizējo Finance instanci konfigurācijas, kas tika eksportētas no Regulatory Configuration Services (RCS), kad izpildījāt darbības no tēmas [Konfigurēt ER formātus, lai izmantotu parametrus, kas konkretizēti juridiskai personai](er-app-specific-parameters-configure-format.md). Veiciet šīs darbības katrai [Elektroniskās ziņošanas (ER)](general-electronic-reporting.md) konfigurācijai šādā secībā: datu modelis, modeļa kartēšana un formāti.

    1. Atlasiet **Apmaiņa \> Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, lai atlasītu failu nepieciešamajai ER konfigurācijai XML formātā.
    3. Atlasiet **Labi**.

    Šajā attēlā ir parādītas konfigurācijas, kurām jums ir jābūt, kad esat beiguši.

    ![ER konfigurāciju lapa.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>DEMF uzņēmuma parametru iestatīšana

Varat izmantot ER struktūru, lai iestatītu programmai specifiskus parametrus ER formātam.

1. Atlasiet **DEMF** juridisko personu.
2. Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.
3. Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.

    ![ER programmai specifisku parametru lapa, lai iestatītu parametrus.](./media/GER-AppSpecParms-LookupForm.PNG)

    Lapā **Programmai specifiski parametri** varat konfigurēt noteikumus datu avotam **Atlasītājs** formātā **Formēt, lai uzzinātu, kā atrast LE datus**.

    Ja bāzes ER formātā būs vairāki veida **Uzmeklēšana** datu avoti, jums jāatlasa vēlamais datu avots kopsavilkuma cilnē **Pārlūki** pirms varat sākt konfigurēt kārtulu kopu datu avotam.

    Katram datu avotam varat konfigurēt atsevišķas kārtulas katrai atlasītā ER formāta versijai.

    Visu kārtulu kopa visiem uzmeklēšanas datu avotiem, kuri ir pieejami atlasītajā bāzes ER formāta versijā, veido programmai raksturīgus parametrus attiecībā uz ER formātu.

4. Atlasiet ER formāta versiju **1.1.1**.
5. Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot**.
6. Jaunā ieraksta laukā **Kods** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu.

    Uzmeklēšana parāda atlases nodokļu kodu sarakstu. Šis saraksts tiek atgriezts, izmantojot datu avotu **Model.Data.Tax**, kas ticis konfigurēts bāzes ER formātā. Tā kā šis datu avots ietver lauku **Nosaukums**, uzmeklēšanas laikā parādās katra nodokļu koda nosaukums.

    ![ER programmas specifisko parametru lapa, koda lauka pārlūkošana.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Atlasiet nodokļa kodu **VAT19**.
8. Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu. Uzmeklēšana parāda atlases TaxationLevel formāta uzskaitījuma vērtību sarakstu.

    Ņemiet vērā, ka, ja vācu valoda ir izvēlēta kā vēlamā lietotāja valoda, kurā esat pieteicies, tad uzmeklēšanas vērtību marķējums būs vācu valodā ar nosacījumu, ka tās ir pārtulkotas bāzes ER formātā. Turklāt, ja uzmeklēšanas datu avota marķējums ir tulkots, šis marķējums tiks parādīts lietotāja vēlamajā valodā cilnē **Pārlūki**.

    ![Informācijas iegūšanas lauks vācu valodā tulkots ER programmas parametru lapā.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Atlasiet vērtību **Parastā taksācija**.

    Pievienojot šo ierakstu, tiek definēta šāda kārtula: Vienmēr, kad tiek pieprasīts uzmeklēšanas datu avots **Atlasītājs** un nodokļa kods **VAT19** tiek nodots kā arguments, **Regulārā aplikšana ar nodokli** tiks atgriezta kā pieprasītais aplikšanas ar nodokli līmenis.

10. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet nodokļu kodu **InVAT19**.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Regulārā aplikšana ar nodokli**.

11. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet nodokļu kodu **VAT7**.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Samazinātā taksācija**.

12. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet nodokļu kodu **InVAT7**.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Samazinātā taksācija**.

13. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet nodokļu kodu **THIRD**.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav taksācijas**.

14. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet nodokļu kodu **InVAT10**.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav taksācijas**.

15. Atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Laukā **Kods** atlasiet opciju **\* Nav tukšs\***.
    2. Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Cita**.

    Pievienojot šo pēdējo ierakstu, tiek definēta šāda kārtula: Vienmēr, kad nodokļa kods, kas tiek nodots kā arguments, neizpilda nevienu no iepriekšējām kārtulām, uzmeklēšanas datu avots atgriezīs **Citu** kā pieprasīto taksācijas līmeni.

    ![Pēdējais ieraksts, kas pievienots ER programmas specifisko parametru lapā.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. Laukā **Statuss** atlasiet **Pabeigts**.

    Palaižot ER formāta versiju ar statusu **Pabeigts** vai **Koplietots**, šai kārtulu kopai jābūt ar statusu **Pabeigta**. Pretējā gadījumā bāzes ER formāta izpilde tiks pārtraukta, kad formāts mēģinās ielādēt datus no šīs kārtulu kopas, kamēr tiks palaists uzmeklēšanas datu avots **Atlasītājs**.

    Palaižot ER formāta versiju ar statusu **Uzmetums**, bāzes formāts var piekļūt šai noteikumu kopai neatkarīgi no tās statusa.

17. Atlasiet **Saglabāt**.
18. Aizveriet lapu **Programmai specifiski parametri**.

## <a name="run-the-er-format-in-the-demf-company"></a>DEMF uzņēmumā palaidiet ER formātu
Lai palaist ER formātu DEMF kompānijā, veiciet šīs darbības: 

1. Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.
2. Darbību rūtī atlasiet **Palaist**.
3. Parādītajā dialoglodziņā atlasiet **Labi**.
4. Lejupielādējiet izveidoto pārskatu un saglabājiet to lokāli.

    Ģenerētajā pārskatā ievērojiet, ka nodokļa koda **InVAT7** kopsavilkums ir uzlikts līmenī **Samazināts** un ka nodokļa kodu **VAT19** un **InVA19** kopsavilkumi ir iekļauti līmenī **Regulārs**. Šo darbību nosaka konfigurācija no juridiskās personas atkarīgā kārtulu kopā.

5. Dodieties uz **Nodokļi \> Netiešie nodokļi \> PVN \> PVN kodi**.
6. Atlasiet nodokļa kodu **InVAT7**.
7. Darbību rūtī, cilnē **PVN kods**, grupā **Pieprasījumi** atlasiet **Iegrāmatots PVN,** lai skatītu informāciju par nodokļa vērtību un piemēroto nodokļa likmi katram nodokļa kodam.

    ![Grāmatota PVN lapa.](./media/GER-AppSpecParms-Statement.PNG)

8. Aizveriet lapu **Grāmatotais PVN**.

## <a name="set-up-parameters-for-the-usmf-company"></a>USMF uzņēmuma parametru iestatīšana
Lai iestatītu parametrus USMF uzņēmumam, izpildiet šādas darbības: 

1. Atlasiet **USMF** juridisko personu.
2. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
3. Konfigurācijas kokā izvērsiet vienumu **Modelis, lai uzzinātu parametru izsaukumus**, izvērsiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus** un atlasiet formātu **Formāts, lai uzzinātu, kā meklēt LE datus**.
4. Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.
5. Atlasiet atlasītā ER formāta versiju **1.1.1**.
6. Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot**.
7. Jaunā ieraksta laukā **Kods** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu.

    Pārlūks tagad parāda nodokļu kodu sarakstu **USMF** uzņēmuma nodokļiem atlasei.

    ![USMF uzņēmuma nodokļa nodokļu kodi.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Atlasiet nodokļa kodu **EXEMPT**.
9. Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav aplikšanas ar nodokli**.
10. Atlasiet **Pievienot**.
11. Jaunā ieraksta **Kods** atlasiet opciju **\* Nav tukšs\***.
12. Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Regulāra taksācija**.
13. Laukā **Statuss** atlasiet **Pabeigts**.
14. Atlasiet **Saglabāt**.

    ![ER programmai specifisku parametru lapa.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. Aizveriet lapu **Programmai specifiski parametri**.

## <a name="run-the-er-format-in-the-usmf-company"></a>USMF uzņēmumā palaidiet ER formātu
Lai palaist ER formātu USMF kompānijā, veiciet šīs darbības:

1. Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.
2. Darbību rūtī atlasiet **Palaist**.
3. Parādītajā dialoglodziņā atlasiet **Labi**.
4. Lejupielādējiet izveidoto pārskatu un saglabājiet to lokāli.

    Ģenerētajā pārskatā ievērojiet, ka jūs atkārtoti izmantojāt to pašu ER formātu citai juridiskajai personai, bet neveicot nekādus pielāgojumus ER formātā.

## <a name="reuse-legal-entitydependent-parameters"></a>Atkārtoti izmantojiet no juridiskās personas atkarīgos parametrus

### <a name="duplicate-existing-parameters"></a>Dublēt esošos parametrus

#### <a name="export-parameters"></a>Eksporta parametri
Lai eksportētu parametrus, veiciet tālāk norādītās darbības:

1. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.
4. Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.
5. Atlasiet ER formāta versiju **1.1.1**.
6. Darbību rūtī atlasiet **Eksportēt**.
7. Lejupielādējiet izveidoto failu un saglabājiet to lokāli.

    Programmai raksturīgo parametru konfigurētais iestatījums tagad ir eksportēts kā XML fails.

#### <a name="import-parameters"></a>Importa parametri
Lai importētu parametrus, veiciet tālāk norādītās darbības:

1. Atlasiet ER formāta versiju **1.1.2**.
2. Darbību rūtī atlasiet **Importēt**.
3. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties ignorēt esošos lietojumprogrammai raksturīgos parametrus šai formāta versijai.
4. Atlasiet **Pārlūkot**, lai atrastu failu, kas satur eksportētos programmai raksturīgos parametrus versijai **1.1.1**
5. Atlasiet **Labi**.

    Tagad ER formāta versijai **1.1.2** formāta 1.2. versijai ir tie paši programmai raksturīgie parametri, kurus sākotnēji konfigurējāt versijai **1.1.1**.

##### <a name="applicability-considerations"></a>Piemērojamības apsvērumi

Ņemiet vērā, ka programmai specifiskie ER formāta parametri ir atkarīgi no juridiskās personas. Lai atkārtoti izmantotu programmai specifiskos parametrus, kas ir konfigurēti vienai juridiskajai personai citā juridiskā personā, tie ir jāeksportē, kad esat pieteicies pirmajā juridiskajā personā, un pēc tam tie jāimportē pēc pieteikšanās otrā juridiskajā personā. Pēc tam importējiet tos pēc pieteikšanās citā juridiskajā persona.

Varat arī izmantot šo eksporta-importa pieeju, lai pārsūtītu ER formātam piesaistītos programmas parametrus, kas sākotnēji tika konfigurēti vienā Finance instancē citai Finance instancei.

Ja konfigurējat programmai raksturīgos parametrus vienai ER formāta versijai un pēc tam importējat vēlāku šī formāta versiju pašreizējā finanšu instancē, esošie programmai raksturīgie parametri importētajā versijā netiks piemēroti, ja izmantojat **Iepriekšējo ER formātu līdzekļa versiju izmantot programmai noteiktus parametrus**. Papildinformāciju skatiet šīs tēmas turpinājumā esošajā sadaļā [Esošo paramteru atkāŗtota izmantošana](#reuse-existing-parameters).

Ņemiet vērā arī to, ka, atlasot failu importēšanai, programmai specifisko parametru struktūra šajā failā tiek salīdzināta ar atbilstošā **Uzmeklēšanas** tipa datu avota struktūru, kas atlasīta importēšanai. Importēšana tiek veikta, kad katrs programmai specifiskais parametrs atbilst atbilstošā datu avota struktūrai, kas ir atlasīta importēšanai. Ja struktūras nesakrīt, saņemsit brīdinājuma ziņojumu, kurā teikts, ka importēšanu nevar veikt. Ja vēlaties, lai imports tiktu veikts, esošie programmai specifiskajam parametri atlasītajam ER formātam tiks notīrīti, un tie būs jāiestata no sākuma.

### <a name="reuse-existing-parameters"></a>Atkāŗtoti izmantot esošos parametrus

Sākot ar Dynamics 365 Finance versiju 10.0.23, jūs varat atkārtoti izmantot programmai raksturīgos parametrus, kas ir konfigurēti vienai ER formāta versijai, kad palaižat augstākas tā paša formāta versijas. Lai to izdarītu, **Līdzekļu pārvaldības** darbvietā iespējojiet līdzekli **Izmantot programmas raksturīgos parametrus no iepriekšējām ER formātu versijām**. Ja šī funkcija ir iespējota un jūs darbināt vienu ER formāta versiju, kas mēģina nolasīt programmai raksturīgos parametrus, ER mēģinās atrast programmai raksturīgus parametrus, kas ir konfigurēti palaistai šī formāta versijai. Vai arī, ja tie nav pieejami, tuvākajai šī formāta mazākajai versijai.

> [!NOTE]
> Jūs varat atkārtoti izmantot programmai raksturīgos parametrus tikai pašreizējās juridiskās personas jomā.
>
> Izpildlaikā radās kļūda, palaižot augstāka ER formāta versiju, kas mēģina atkārtoti izmantot programmai raksturīgos parametrus, kas ir konfigurēti tā paša formāta zemākai versijai un vismaz viena **Uzmeklēšanas** tipa datu avota struktūrai, kurai ir mainīta augstāka formāta versija.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Attiecības starp programmai specifiskajiem parametriem un ER formātu

Attiecības starp ER formātu un tā programmai specifiskajiem parametriem ir noteiktas ar no ER formāta instances neatkarīgu unikālu identifikācijas kodu. Tāpēc, noņemot ER formātu no Finance, lietojumprogrammai raksturīgie parametri, kas konfigurēti ER formātam, tiek saglabāti pašreizējā Finance instancē. Tiem var piekļūt, kad tiek atkal importēts bāzes ER formāts šajā Finance instancē.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Piekļūt programmai specifiskajiem parametriem, izmantojot ER struktūru

Iepriekšējā piemērā, lietojot ER struktūru, jums ir pieejami programmai specifiskie parametri ER formātā. Izmantojot šo pieeju, nevar ierobežot piekļuvi noteiktiem ER formātam specifiskiem parametriem. Ja jums ir jāpiemēro šādi ierobežojumi, veiciet šādas darbības. 

1. Vai nu atkārtoti izmantojiet esošu izvēlnes elementu **ERSolutionAppSpecificParametersDesigner**, vai ieviesiet savu izvēlnes elementu **ERSolutionAppSpecificParametersDesigner**.

    ![ERSolutionAppSpecificParametersDesigner izvēlnes elementu parādīšana.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Izpildiet kādu no šīm darbībām:

    1. Izveidojiet jaunu izvēlnes elementu pogu un saistiet to ar atbilstošo ierakstu no tabulas **ERSolutionTable**, iestatot tās rekvizītu **Datu avots** uz **ERSolutionTable.**

        ![Jaunu izvēlnes elementu iestatījumu parādīšana.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Izveidojiet vienkāršu pogu un pārlabojiet metodi **Noklikšķināts**, kā tas redzams piemērā.

        Izmantojot šo pieeju, varat norādīt unikālu risinājuma ID (kas definēts, izmantojot vērtību **GUID** vērtību), lai ļautu piekļūt tikai konkrētam ER formāta un sekojošām kopijām, kas no tās iegūtas.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Papildu resursi

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[ER formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu](er-app-specific-parameters-configure-format.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
