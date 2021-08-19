---
title: Programmai atbilstošo metadatu sagatavošana izmantošanai RCS un ER
description: Šajā tēmā ir paskaidrots, kā sagatavot programmai atbilstošus metadatus izmantošanai pakalpojumā Regulatory Configuration Service (RCS) un elektroniskajos pārskatos ( Electronic Reporting — ER).
author: NickSelin
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9136bd3db2aee1447d6af3b3c47b908177cee966aba630490cc6e72072525d29
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735602"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>Programmai atbilstošo metadatu sagatavošana izmantošanai RCS un ER

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegti šādi uzdevumu piemēri:

- [RCS izmantojamo programmas metadatu sagatavošana](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](#access-application-metadata-by-using-an-er-configuration)
- [Piekļuve programmas metadatiem, izmantojot saistītās programmas](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>RCS izmantojamo programmas metadatu sagatavošana

Nākamajā procedūrā ir parādīts, kā lietotājs, kas ir **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs** var izveidot jaunu elektronisko pārskatu (Electronic reporting — ER) konfigurāciju, kurā ir programmas metadati un ko izmanto ER modeļa kartēšanas konfigurāciju veidošanai pakalpojumā Regulatory configuration service (RCS). Parauga ER modeļa kartēšanas konfigurācija, ko izveido šajā piemērā, tiks izmantota piekļūšanai ārējās tirdzniecības transakcijām.

Šajā piemērā izmantosim pakalpojumu RCS, lai izveidotu ER risinājumu programmai, kas tiks izmantota, lai ģenerētu elektroniskus dokumentus, kuros ir informācija no ārējās tirdzniecības uzņēmējdarbības jomas. Lai norādītu noteiktu kartēšanu starp ER datu modeli un nepieciešamo datu avotiem, pakalpojumā RCS jums ir nepieciešama piekļuve programmas metadatiem. Tādēļ ER risinājuma veidošanas procesā jums ir jākonfigurē jauna ER metadatu konfigurācija, kas ietver visus metadatus, kuri pašlaik ir nepieciešami ER pārskatu veidošanai atlasītajai uzņēmējdarbības jomai.

> [!NOTE]
> Šajā piemērā jūs izveidosit konfigurāciju parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā.

1. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda procedūra [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Atlasiet **Metadatu konfigurācijas**.
4. Atlasiet **Izveidot konfigurāciju**.
5. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet nosaukumu. Šim piemēram ievadiet **Ārējās tirdzniecības metadati**.
6. Atlasiet **Izveidot konfigurāciju**.
7. Atlasiet **Noformētājs**.
8. Atlasiet **Pievienot**.

    > [!NOTE]
    > Varat atlasīt visus metadatus vai nu visai programmai, vai atlasītajiem modeļiem vai moduļiem. Abos gadījumos ņemiet vērā, ka automātiski tiks pievienoti šādi metadati: ierakstu tabulas, uzskaitījumi un paplašinātie datu tipi (EDT). Ja ir nepieciešami papildu metadatu tipi, tie ir jāpievieno manuāli.

    Jums ir jāpievieno daži ar ārējās tirdzniecības transakcijām saistīti metadati un manuāli jāatlasa metadatu vienumi.

9. Atlasiet **Pievienot datu avotu \> Tabulas ieraksti**.
10. Filtrējiet **Intrastat** vērtību laukā **Nosaukums**.
11. Atlasiet **Intrastat** tabulas ierakstu.
12. Atlasiet **Labi**.

    Jums ir jāpievieno metadatu informācija par Intrastat ierakstu tabulu.

13. Koka struktūrā atlasiet **Tabulas ieraksti Intrastat \> \>Relācijas \> IntrastatCommodity (Tabulas ieraksti EcoResCategory)**.
14. Atlasiet **Pievienot metadatus**.

    > [!NOTE]
    > Metadati par nepieciešamajām relācijām atlasītajai ierakstu tabulai ir jāpievieno manuāli.

15. Atlasiet **Pievienot datu avotu**.
16. Atlasiet **Uzskaitījums**.
17. Filtrējiet **IntrastatDirection** vērtību laukā **Nosaukums**.
18. Atlasiet uzskaitījuma ierakstu **IntrastatDirection**.
19. Atlasiet **Labi**.
20. Atlasiet **Saglabāt**.
21. Aizvērt lapu.
22. Pabeidziet metadatu konfigurācijas melnraksta versiju, kā norādīts tālāk.

    1. Atlasiet **Mainīt statusu \> Pabeigts**.
    2. Atlasiet **Labi**.
    3. Atlasiet 1. pabeigto versiju.

23. Eksportējiet pabeigtās metadatu konfigurācijas versiju no programmas XML faila veidā, kā norādīts tālāk.

    1. Atlasiet **Maiņa \> Eksportēt kā XML failu**.
    2. Atlasiet **Labi**.

Izveidotā ER metadatu konfigurācija tiek saglabāta kā fails **Ārējās tirdzniecības metadati.xml**. Tagad varat importēt to pakalpojumā RCS, lai to varētu izmantot kā metadatu avotu ārējās tirdzniecības biznesa domēnam. Balstoties uz šo informāciju, varat norādīt kartēšanu starp programmas metadatiem un ER datu modeli.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Piekļuve programmas metadatiem, izmantojot ER konfigurāciju

Šī procedūra parāda, kā RCS lietotājs, kuram ir loma **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs**, var izveidot jaunu ER modeļa kartēšanu, izmantojot programmas metadatus. Programmas metadatiem jāpiekļūst, izmantojot ER metadatu konfigurāciju, kas ietver metadatu paraugu kopu, lai piekļūtu ārējās tirdzniecības transakcijām.

Lai varētu izpildīt šo procedūru, vispirms ir jāveic tālāk norādītās procedūras.

- [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [RCS izmantojamo programmas metadatu sagatavošana](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda procedūra [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importējiet ER metadatu konfigurāciju, kas satur programmas metadatus un kas ir konfigurēta elektronisko dokumentu ģenerēšanai ārējās tirdzniecības uzņēmējdarbībai. Jūs izveidojāt šo ER metadatu konfigurāciju un eksportējāt to kā XML failu procedūrā [RCS izmantojamo programmas metadatu sagatavošana](#prepare-application-metadata-that-can-be-used-in-rcs), kas norādīta iepriekš šajā tēmā.

    1. Atlasiet **Metadatu konfigurācijas**.
    2. Atlasiet **Maiņa**.
    3. Atlasiet **Ielādēt no XML faila**.
    4. Pārlūkojiet un atlasiet failu **Ārējās tirdzniecības metadati.xml**.
    5. Atlasiet **Labi**.
    6. Aizvērt lapu.

4. Izveidojiet datu modeļa konfigurāciju, kā norādīts tālāk.

    1. Atlasiet **Pārskatu konfigurācijas**.
    2. Atlasiet **Izveidot konfigurāciju**.
    3. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Ārējās tirdzniecības modelis**.
    4. Atlasiet **Izveidot konfigurāciju**.
    5. Atlasiet **Noformētājs**.
    6. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.

        1. Laukā **Nosaukums** ierakstiet **Sakne**.
        2. Atlasiet **Pievienot**.
    
    7. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.

        1. Laukā **Nosaukums** ierakstiet **Transakcija**.
        2. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
        3. Atlasiet **Pievienot**.
 
    8. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.

        1. Laukā **Nosaukums** ierakstiet **Preces kods**.
        2. Laukā **Vienuma veids** atlasiet **Virkne**.
        3. Atlasiet **Pievienot**.

    9. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.

        1. Laukā Nosaukums ierakstiet **Rēķinā iekļautā summa**.
        2. Laukā **Vienuma veids** atlasiet **Reāls**.
        3. Atlasiet **Pievienot**.

    10. Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.

        1. Laukā **Nosaukums** ierakstiet **Datums**.
        2. Laukā **Vienuma veids** atlasiet **Datums**.
        3. Atlasiet **Pievienot**.
 
    11. Atlasiet **Pievienot \> Saknes atsauce**.
    12. Atlasiet **Labi**.
    13. Atlasiet **Saglabāt**.
    14. Aizvērt lapu.
    15. Atlasiet **Mainīt statusu \> Pabeigts**.
    16. Atlasiet **Labi**.

5. Izveidojiet modeļa kartēšanas konfigurāciju, kā norādīts tālāk.

    1. Atlasiet **Izveidot konfigurāciju**.
    2. Nolaižamā dialoglodziņa laukā **Jauns** ievadiet **Uz datu modeli “Ārējās tirdzniecības modelis” balstīta modeļa kartēšana**.
    3. Laukā **Nosaukums** ievadiet **Ārējās tirdzniecības kartēšana**.
    4. Atlasiet **Izveidot konfigurāciju**.
    5. Kopsavilkuma cilnē **Priekšnosacījumi** atlasiet **Rediģēt**.
    6. Atlasiet **Jauns**.
    7. Laukā **Priekšnosacījuma komponenta veids** atlasiet **Konfigurācija**.
    8. Atlasiet konfigurāciju **Ārējās tirdzniecības metadati**.
    9. Atlasiet **Saglabāt**. Ņemiet vērā, ka konfigurācijas **Ārējās tirdzniecības metadati** 1. versijai ir pievienota atsauce. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.
    10. Aizvērt lapu.
    11. Atlasiet **Noformētājs**.
    12. Atlasiet **Noformētājs**.
    13. Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.
    14. Atlasiet **Pievienot sakni**.
    15. Laukā **Nosaukums** ievadiet **Intrastat**.
    16. Atlasiet **Intrastat** tabulas ierakstus.
    17. Atlasiet **Labi**.

        > [!NOTE]
        > Tika piedāvātas tikai 2 tabulas, jo tikai 2 tabulas bija pievienotas pašlaik izmantotajai metadatu kopai.

    18. Atlasiet **Saistīt**.
    19. Kokā atlasiet **Intrastat \> AmountMST**.
    20. Kokā atlasiet **Transakcija = Intrastat \> Rēķinā iekļautā summa**.
    21. Atlasiet **Saistīt**.
    22. Kokā atlasiet **Intrastat \> TransDate**.
    23. Kokā atlasiet **Transakcija = Intrastat \> Datums**.
    24. Atlasiet **Saistīt**.
    25. Kokā atlasiet **Intrastat \> \>Relācijas \> IntrastatCommodity \> Kods**.
    26. Kokā atlasiet **Transakcija = Intrastat \> Preces kods**.
    27. Atlasiet **Saistīt**.
    28. Atlasiet **Validēt**.

        > [!NOTE]
        > Pēc validācijas pabeigšanas, esat veiksmīgi saistījis datu modeļa elementus ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par programmas metadatiem no atsauces ER metadatu konfigurācijas.

    29. Atlasiet **Saglabāt**.

Ja vēlaties, varat paplašināt esošo metadatu kopu programmā. Pēc tam jūs varat eksportēt ER metadatu konfigurācijas jauno pabeigto versiju, importēt to pakalpojumā RCS un atjaunināt konfigurācijas priekšnosacījumus konfigurētā modeļa kartēšanas konfigurācijai, lai tie attiektos uz importēto metadatu konfigurācijas jauno versiju.

> [!NOTE]
> Šī metode, kā iegūt informāciju par programmas metadatiem, ir vienīgā pieejamā metode programmām, kas ir izvietotas lokāli (proti, kad ir izmantots lokālas biznesa datu \[LBD\] vai vietējais izvietošanas modelis programmai).

## <a name="access-application-metadata-by-using-connected-applications"></a>Piekļuve programmas metadatiem, izmantojot saistītās programmas

Šī procedūra parāda, kā RCS lietotājs, kuram ir loma **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs**, var izveidot jaunu ER modeļa kartēšanu, izmantojot programmas metadatus. Programmas metadatiem jāpiekļūst tiešsaistē, izmantojot ar RCS saistīto programmu. Parauga ER modeļa kartēšana jākonfigurē piekļuvei ārējās tirdzniecības transakcijām.

Lai izpildītu šo procedūru, vispirms rīkā RCS izpildiet procedūru [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md). Ja vēl neesat izpildījis iepriekš šajā tēmā aprakstīto procedūru [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](#access-application-metadata-by-using-an-er-configuration) dodieties uz lapu [Elektronisko pārskatu uzdevumu ceļvedis izmantošanai Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), lai jau laikus lejupielādētu un lokāli saglabātu šādas ER konfigurācijas: **Ārējās tirdzniecības metadati.xml**, **Ārējās tirdzniecības modelis.xml** un **Ārējās tirdzniecības kartēšana.xml**.


### <a name="get-required-er-configurations"></a>Nepieciešamo ER konfigurāciju iegūšana

Ja esat jau izpildījis darbības, kas ir aprakstītas iepriekš šājā tēmā norādītajā procedūrā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](#access-application-metadata-by-using-an-er-configuration), jums jau ir visas nepieciešamās ER konfigurācijas (ārējās tirdzniecības metadatu, modeļa un kartēšanas konfigurācijas) pašreizējā RCS instancē. Šādā gadījumā šo procedūru varat izlaist.

1. Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Ielādējiet konfigurācijas failus **Ārējās tirdzniecības metadati.xml** **Ārējās tirdzniecības modelis.xml** un **Ārējās tirdzniecības kartēšana.xml**, kas katra atkārto tālāk norādīto darbību ķēdi.

    1. Atlasiet **Maiņa**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot** un atlasiet failu.
    4. Atlasiet **Labi**.

### <a name="register-the-connection-with-the-application"></a>Reģistrējiet savienojumu ar programmu

1. Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.
2. Atlasiet **Savienotās programmas**.
3. Pārliecinieties, ka konfigurētā programma ir balstīta uz Microsoft Azure un ka tā ir pieejama RCS lietotājiem. Pašreizējam RCS lietotājam ir arī jābūt piekļuvei konfigurētajai programmai un ir jābūt reģistrētam kā šīs programmas lietotājam ar lomu, kas dod viņam privilēģijas piekļūt programmas metadatiem.
4. Atlasiet **Jauns**.
5. Laukā **Nosaukums** ievadiet **MyConnectedApp** kā savienotās programmas nosaukumu.
6. Laukā **Programma** norādiet programmas vietrādi URL.
7. Laukā **Nomnieks** norādiet programmas nodrošinātāju.
8. Atlasiet **Saglabāt**. 
9. Kad pārbaudāt savienojums ar konfigurēto programmu, lapā **Savienojuma izveide ar attālo programmu** atlasiet saiti **Atlasīt šeit, lai izveidotu savienojumu ar atlasīto attālo programmu**. 
10. Atlasiet **Pārbaudīt savienojumu**, lai validētu piekļuvi konfigurētajai programmai.
11. Atlasiet **Aizvērt**.

Kad šī procedūra ir pabeigta un savienojuma validācija ir izdevusies, pašreizējā režģī konfigurētajai programmai tiks atjaunināta versija un nomnieka informācija.

### <a name="review-the-existing-model-mapping-configuration"></a>Esošās modeļa kartēšanas konfigurācijas pārskatīšana

1. Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Kokā atlasiet **Ārējās tirdzniecības modelis \> Ārējās tirdzniecības kartēšana**.
4. Atlasiet kopsavilkuma cilni **Priekšnosacījumi**.

    > [!NOTE]
    > Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.

4. Atlasiet **Noformētājs**.
5. Atlasiet **Noformētājs**.
6. Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.
7. Atlasiet **Pievienot sakni**.
8. Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.

    > [!NOTE]
    > Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.

9. Atlasiet **Atcelt**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Savienotās programmas piešķiršana modeļa kartēšanai

1. Atlasiet **Rediģēt**.
2. Laukā **Savienotā programma** atlasiet programmu **MyConnectedApp.**

    > [!NOTE]
    > Šī kartēšana attiecas uz atlasītās savienotās programmas metadatiem. Ja kartēšana attiecas vienlaikus uz metadatu konfigurāciju un uz savienoto programmu, tiks izmantoti savienotās programmas metadati.

3. Atlasiet **Noformētājs**.
4. Atlasiet **Noformētājs**.
5. Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.
6. Atlasiet **Pievienot sakni**.
7. Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.

    > [!NOTE]
    > Šobrīd tiek piedāvātas vairāk nekā divas programmas tabulas, jo šī kartēšana izmanto visus tai piešķirtās savienotās programmas metadatus.

8. Atlasiet **Atcelt**.
9. Atlasiet **Validēt**.

Datu modeļa elementus tagad esat veiksmīgi saistījis ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par kartēšanai piešķirtās savienotās programmas metadatiem.

Ja ir jānovērtē šī modeļa kartēšana, izmantojot citas versijas programmas metadatus, reģistrējiet citu savienoto programmu, piešķiriet to šai modeļa kartēšanai un validējiet to ar jauniem metadatiem.

## <a name="additional-resources"></a>Papildu resursi

Vai arī varat atskaņot uzdevuma ceļvedi **RCS izmantojamo programmas metadatu sagatavošana** programmā, kā arī uzdevuma ceļvežus **Piekļuve programmas metadatiem, izmantojot ER konfigurāciju** un **Piekļuve programmas metadatiem, izmantojot saistītas programmas** rīkā RCS. Šos uzdevumu ceļvežus var lejupielādēt lapā [Elektronisko pārskatu uzdevumu ceļvedis izmantošanai Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]