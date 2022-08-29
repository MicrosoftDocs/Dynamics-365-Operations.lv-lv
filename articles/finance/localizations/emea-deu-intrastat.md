---
title: Vācijas Intrastat
description: Šajā rakstā ir ietverta informācija par Intrastat deklarāciju Vācijā.
author: AdamTrukawka
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: ae978b28098d92d84415c29bbe76157144f862d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269440"
---
# <a name="german-intrastat"></a>Vācijas Intrastat

[!include [banner](../includes/banner.md)]

Lapa **Intrastat** tiek izmantota, lai veidotu un paziņotu informāciju par tirdzniecību starp Eiropas Savienības (ES) valstīm. Vācijas Intrastat deklarācija satur informāciju par preču tirdzniecību pārskatam. Pārskats tiek formatēts atbilstoši Vācijas varas iestāžu vadlīnijām, kuras ir redzamas lapā [6.2 Failu deklarācijas INSTAT/XML formātā](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html).

Šajā tabulā ir parādīti lauki, kas parādās Vācijas Intrastat deklarācijā.

| Lauki | Nosūta | Ienākošie krājumi |
|-------------------------|-------------------------|-------------------------|
| Atsauces periods | X | X |
| Virziena kods | X | X |
| Intrastat deklarācijas valūta</br>**Piezīme:** Neviena no valūtām nav <em>uzskaites valūta</em>. | X | X |
| Preču kods | X | X |
| Preces nosaukums | X | X |
| Papildu vienības kods | X | X |
| Sūtījuma/adresāta valsts | X | X |
| Neto masa | X | X |
| Daudzums papildu vienībās | X | X |
| Izcelsmes valsts/reģions |  | X |
| Rēķina summa | X |  |
| Statistiskā vērtība | X | X |
| Darījuma raksturs | X | X |
| Transportēšanas veids | X | X |
| Reģiona kods</br>**Piezīme.**</br><ul></br><li>Ja izcelsmes valsts vai reģions ir Vācija un rēķins ir paredzēts nosūtīšanai, tiek parādīts izcelsmes valsts Intrastat kods.</li></br><li>Ja izcelsmes valsts vai reģions nav Vācija un rēķins ir paredzēts nosūtīšanai, tiek parādīts kods **99**.</li></br><li>Ja rēķins ir paredzēts saņemšanai, tiek parādīts valsts Intrastat kods.</li></br></ul> | X | X |
| Osta/Lidosta/Iekšzemes ostas kods | X | X |
| Piegādes nosacījumi | X | X |


## <a name="set-up-intrastat"></a>Iestatīt Intrastat

1. Iestatiet uzņēmuma kodus.

    1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
    2. Kopsavilkuma cilnes **Ārējā tirdzniecība un loģistika** sadaļas **Identifikācija** laukā **DVR** ievadiet Apmaiņas līguma ID. Šis ID būs ietverts šajā atskaitē.
    3. Laukā **PVN numurs eksportam** ievadiet sava uzņēmuma pievienotās vērtības numuru (PVN) eksportam.
    4. Laukā **PVN numurs importam** ievadiet sava uzņēmuma pievienotās vērtības numuru (PVN) importam.
    5. **Intrastat koda** laukā ievadiet Intrastat kodu, kas piešķirts juridiskajai personai.
    6. Kopsavilkuma cilnē **Nodokļa reģistrācija**, laukā **Nodokļa reģistrācijas numurs** ievadiet jūsu uzņēmuma nodokļa reģistrācijas numuru.

    > [!NOTE]
    > Ja jūs ģenerēsiet Intrastat pārskatu filiālēm, laukā **Nodokļa reģistrācijas numurs** ievadiet sava pamatu uzņēmuma nodokļu reģistrācijas numuru.

2. Programmas [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) koplietojamo līdzekļu bibliotēkā lejupielādējiet tālāk norādīto Elektronisko pārskatu (ER) konfigurāciju jaunākās versijas Intrastat deklarācijai.

    - Intrastat modelis
    - Intrastat pārskats
    - INSTAT XML
    - INSTAT XML (DE)

3. Iestatīt starptautiskās tirdzniecības parametrus:

    1. Programmā Dynamics 365 Finanses dodieties uz nodokļu **iestatījuma** > **ārējās** > **tirdzniecības parametriem**.
    2. Kopsavilkuma cilnē **Elektroniskie pārskati** cilnē **Intrastat** laukā **Failu formātu kartēšana** atlasiet **Intrastat XML (DE)**.
    3. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
    4. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.
    5. **Transakcijas kods** – izvēlieties transakcijas kodu īpašuma pārsūtīšanai. Varat izmantot šo kodu transakcijām, kas izraisa faktisko vai plānoto īpašuma pārsūtīšanu attiecībā uz kompensāciju (finansiālu vai cita veida). To izmanto arī labojumiem.
    6. Laukā **Kredīta nota** izvēlieties transakcijas kodu preču atgriešanai.
    7. Laukā **Darbinieks** atlasiet Intrastat pārskata kontaktpersonu. Vai arī cilnē **Kontaktpersona** ievadiet vai atlasiet vērtības laukos **Vārds/uzvārds**, **Tālrunis**, **Fakss**, **E-pasts** un **Tīmekļa adrese**. Šie lauki tiek iekļauti pārskatā.
    8. Laukā **Iestāde** atlasiet Intrastat iestādi.
    9. Dodieties uz **Nodokļi** > **Netiešie nodokļi** > **Tirdzniecības nodokļi** > **Tirdzniecības nodokļu iestādes** un ievadiet iepriekšējā darbībā atlasītajai Intrastat iestādei šādu informāciju:

       - Iestādes identifikācija
       - Adrese
       - Kontaktinformācija

    10. Cilne **Valsts/reģiona rekvizīti**, lauks **Valsts/reģions** uzskaita visas valstis vai reģionus, ar kuriem jūsu organizācija veic darījumus. Katrai valstij vai reģionam laukā **Valsts/reģiona tips** atlasiet **ES**, lai valsts vai reģions parādītos Intrastat pārskatā.

4. Reģiona kodu iestatīšana.

    1. Dodieties uz **Organizācijas administrēšana** > **Globālā adrešu grāmata** > **Adreses** > **Adrešu iestatīšana**.
    2. Cilnes **Novads** laukā **Valsts/reģions** atlasiet **DEU**, un pēc tam atlasiet **Lietot filtru**.
    3. Režģī atlasiet novadu. Laukā **Intrastat kods** ievadiet unikālo Intrastat kodu.

5. Iestatiet preces izcelsmes adresi.

    1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
    2. Režģī atlasiet preci.
    3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **DEU**.

6. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Intrastat arhivēšana** un atlasiet laukus, kas jāsalīdzina, kad tiek apkopota Intrastat informācija. Vācijas Intrastat atlasiet šādus laukus:

    - Prece
    - Valsts/reģions
    - Labojums
    - Virziens
    - Piegādes nosacījumi
    - Rēķins
    - Izcelsmes valsts/reģions
    - Osta
    - Sūtītāja valsts/reģions
    - Sūtītāja stāvoklis
    - Statistikas procedūra
    - Darbības kods
    - Transportēšana
    - PVN reģistrācijas numurs

### <a name="intrastat-transfer"></a>Intrastat pārsūtīšana

Lapas **Intrastat** darbību rūtī varat atlasīt **Pārsūtīt**, lai automātiski pārsūtītu informāciju par iekšējo tirdzniecību kopienā no pārdošanas pasūtījumiem, brīva teksta rēķiniem, pirkšanas pasūtījumiem, kreditora rēķiniem, kreditora produktu čekiem **,** projekta rēķiniem un pārsūtīšanas pasūtījumiem. Tiks pārsūtīti tikai dokumenti, kuriem kā adresāta valsts vai reģions (nosūtīšanai) vai sūtījumam (ierašanai) ir ES valsts.

Alternatīvi transakcijas variet ievadīt manuāli, darbību rūtī atlasot **Jauns**.

### <a name="generate-an-intrastat-report"></a>Ģenerēt Intrastat pārskatu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
3. Dialoglodziņā **Intrastat pārskats** iestatiet tālak norādītos laukus.

    | Lauks | Apraksts |
    |-------------------------|-------------------------|
    | No datuma | Atlasiet pārskata sākuma datumu. |
    | Līdz datumam | Atlasiet pārskata beigu datumu. |
    | Ģenerēt failu | Iestatiet šo opciju kā **Jā**, lai ģenerētu .xml failu. |
    | Faila nosaukums | Atstājiet šo lauku tukšu. Faila nosaukums tiek ģenerēts automātiski, un tas sastāv no **&lt;envelopeId&gt;** XML atzīmes un nosaukuma paplašinājuma **.xml** vērtības.</br>**&lt;envelopeId&gt;** vērtība ir šādu elementu konkatenācija šādā secībā:</br><ol type="1"></br><li>Atzīmes **&lt;interchangeAgreementId&gt;** vērtība</li></br><li>Defise (-)</li></br><li>**&lt;referencePeriod vērtība tagā YYYYMM&gt;**</li></br><li>Defise (-)</li></br><li>**&lt;Vēstules/DateTime/datuma vērtība atzīmē YYYYMMDD&gt;**</li></br><li>Defise (-)</li></br><li>**&lt;Vēstules/DateTime/datuma vērtība atzīmē hhmm&gt;**</li></br></ol> |
    | Virziens | <ul></br><li>Atlasiet **Saņemtie** pārskatam par saņemto iekšējā kopienā.</li></br><li>Atlasiet **Nosūtītie** pārskatam par nosūtīto iekšējā kopienā.</li></br><li>Atlasiet **Abi** pārskatam par saņemto un nosūtīto.</li></br></ul> |
    | Nodokļa reģistrācijas numurs | Ievadiet reģistrācijas numuru, ko izmantot, lai ģenerētu sūtītāja identifikācijas kodu, ja numurs atšķiras no juridiskās personas nodokļa reģistrācijas numura. |


## <a name="example"></a>Paraugs

Šis piemērs parāda, kā grāmatot Intrastat saņemto un nosūtīto. Tas izmanto **DEMF** juridisku personu.

1. Programmas [LCS](https://lcs.dynamics.com/Logon/Index) koplietojamo līdzekļu bibliotēkā lejupielādējiet jaunāko ER konfigurāciju versiju Intrastat deklarācijas formātam:

    - Intrastat modelis
    - Intrastat pārskats
    - Intrastat XML
    - Intrastat XML (DE)

2. Darījumu kodu izveide.

    1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **Transakcijas** **kods** ievadiet **21**.
    4. Laukā **Nosaukums** ievadiet **Preču atgriešana**.
    5. Darbību rūtī atlasiet **Saglabāt**.

3. Iestatiet iestādes identifikācijas numuru.

    1. Ejiet uz **Nodokļi** > **Netiešie nodokļi** > **Tirdzniecības nodokļi** > **Tirdzniecības nodokļu iestādes**.
    2. Sarakstā atlasiet **TA**.
    3. **Iestādes identifikācijas** laukā ievadiet **123**.

4. Reģiona kodu iestatīšana.

    1. Dodieties uz **Organizācijas administrēšana** > **Globālā adrešu grāmata** > **Adreses** > **Adrešu iestatīšana**.
    2. Cilnes **Novads** laukā **Valsts/reģions** atlasiet **DEU**, un pēc tam atlasiet **Lietot filtru**.
    3. Režģī atlasiet **BE** un pēc tam **Intrastat koda** laukā ievadiet **11**.
    4. Darbību rūtī atlasiet **Saglabāt**.

5. Iestatīt starptautiskās tirdzniecības parametrus.

    1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
    2. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **11**.
    3. **Kredīta notas** laukā atlasiet **21**.
    4. Laukā **Iestāde** atlasiet **TA**.
    5. Kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **INSTAT XML (DE)**.
    6. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
    7. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** pārbaudie, vai atlasījāt **Intrastat**.
    8. Cilnē **Valsts/reģiona rekvizīti** atlasiet **Jauns**.
    9. Laukā **Puses valsts/reģions** atlasiet **FRA**.
    10. Laukā **Valsts/reģiona tips** Atlasiet **ES**.

6. Piešķiriet precei preces kodu un iestatiet preces izcelsmi. Pēc tam, atlasot preci, pārdošanas pasūtījumiem un pirkšanas pasūtījumiem automātiski tiks iestatīti lauki **Preces kods**, **Izcelsmes valsts/reģions** un **Izcelsmes vieta**.

    1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
    2. Režģī atlasiet **D0001**.
    3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **920 20 34**.
    4. Sadaļas **Izcelsme** laukā **Valsts/reģions** atlasiet **DEU**.
    5. Kopsavilkuma cilnes **Pārvaldīt krājumu** sadaļā **Svara mērījumi** laukā **Neto svars** ievadiet **12**.
    6. Darbību rūtī atlasiet **Saglabāt**.

7. Piešķiriet transportēšanu piegādes veidam. Atlasot piegādes veidu, transportēšanas kods pasūtījumos tiks iestatīts automātiski.

    1. Pārejiet uz sadaļu **Sagāde un avoti** > **Iestatījumi** > **Izplatīšana** > **Piegādes veidi**.
    2. Sarakstā atlasiet **10**.
    3. Kopsavilkuma cilnes **Ārējā tirdzniecība** laukā **Transports** atlasiet **01**.

8. Izveidojiet pārdošanas pasūtījumu ar ES debitoru.

    1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Dialoglodziņā **Izveidot pārdošanas pasūtījumu**, kopsavilkuma cilnē **Debitors**, sadaļā **Debitors**, laukā **Debitora konts** atlasiet **DE-012**.
    4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Glabāšanas dimensijas** laukā **Vieta** atlasiet **1**.
    5. Laukā **Noliktava** atlasiet **11**.
    6. Atlasiet **Labi**.
    7. Kopsavilkuma cilnes **Ārējā tirdzniecība** cilnes **Galvene** laukā **Osta** atlasiet **53**.
    8. Laukā **Statistikas procedūra** atlasiet **31710**.
    9.  Kopsavilkuma cilnes **Pārdošanas pasūtījuma** **rindas** cilnes **Rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **10**.
    10. Kopsavilkuma cilnes **Rindas informācija** cilnē **Ārējā tirdzniecība** pārliecinieties, ka automātiski tiek iestatīti lauki **Darījuma kods**, **Transports**, **Prece** un **Izcelsmes valsts/reģions**.
    11. Darbību rūtī atlasiet **Saglabāt**.
    12. Darbību rūts cilnē **Rēķins**, sadaļā **Ģenerēt** atlasiet **Rēķins**.
    13. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
    14. Atlasiet **Labi**, lai iegrāmatotu rēķinu.

9.  Pārsūtiet darbību uz Intrastat žurnālu un pārskatiet rezultātu.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Filtrēt**.
    5. **Intrastat filtra** dialoglodziņa cilnē **Diapazons** atlasiet pirmo rindu un pārliecinieties, vai lauks **Lauks** ir iestatīts uz **Datumu**.
    6. Laukā **Kritēriji** atlasiet pašreizējo datumu.
    7. Lai aizvērtu dialoglodziņu **Intrastat filtrs**, atlasiet **Labi**.
    8. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Intrastat (pārsūtīšana)** un pārskatiet rezultātu. Rindā atlasiet pirmo izveidoto pārdošanas pasūtījumu.

        ![Rinda, kas ataino pārdošanas pasūtījumu Intrastat lapā](media/intrastat_deu_1.png)

10. Atlasiet darbības rindu un tad atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju.

    ![Pārdošanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_deu_2.png)

11. Kredīta notas izveide, izmantojot pārdošanas pasūtījumu.

    1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Dialoglodziņā **Izveidot pārdošanas pasūtījumu**, kopsavilkuma cilnē **Debitors**, sadaļā **Debitors**, laukā **Debitora konts** atlasiet **DE-012**.
    4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Glabāšanas dimensijas** laukā **Vieta** atlasiet **1**.
    5. Laukā **Noliktava** atlasiet **11**.
    6. Kopsavilkuma cilnes **Ārējā tirdzniecība** cilnes **Galvene** laukā **Osta** atlasiet **53**.
    7. Laukā **Statistikas procedūra** atlasiet **31710**.
    8. Kopsavilkuma cilnes **Pārdošanas pasūtījuma** **rindas** cilnes **Rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **-2**.
    9. Kopsavilkuma cilnes **Intrastat** kopsavilkuma cilnē **Vispārīgi** laukā **Darbības kods** atlasiet **21**.
    10. Pārliecinieties, ka automātiski ir iestatīti lauki **Transports**, **Prece** un **Izcelsmes valsts/reģions**.
    11. Darbību rūtī atlasiet **Saglabāt**.
    12. Darbību rūts cilnē **Rēķins**, sadaļā **Ģenerēt** atlasiet **Rēķins**.
    13. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
    14. Atlasiet **Labi**, lai iegrāmatotu rēķinu.

12. Pārsūtiet darbību uz Intrastat žurnālu un pārskatiet rezultātu.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Intrastat (pārsūtīšana)** un pārskatiet rezultātu. Jauna rinda, kur laukam **Virziens** ir pievienota iestatīta vērtība **Saņemtie**.            
        Šī rinda parāda preču fizisko atgriešanu.

        ![Rinda preču fiziskai atgriešanai Intrastat lapā](media/intrastat_deu_3.png)

13. Atlasiet darbības rindu un tad atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju.

    ![Detalizēta informācija par preču fizisko atgriešanu Intrastat lapas cilnē Vispārīgi](media/intrastat_deu_4.png)

14. Labojuma izveide, izmantojot pārdošanas pasūtījumu:

    1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Dialoglodziņā **Izveidot pārdošanas pasūtījumu**, kopsavilkuma cilnē **Debitors**, sadaļā **Debitors**, laukā **Debitora konts** atlasiet **DE-012**.
    4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Glabāšanas dimensijas** laukā **Vieta** atlasiet **1**.
    5. Laukā **Noliktava** atlasiet **11**.
    6. Kopsavilkuma cilnes **Ārējā tirdzniecība** cilnes **Galvene** laukā **Osta** atlasiet **53**.
    7. Laukā **Statistikas procedūra** atlasiet **31710**.
    8. Kopsavilkuma cilnes **Pārdošanas pasūtījuma** **rindas** cilnes **Rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **-3**.
    9. Kopsavilkuma cilnes **Intrastat** kopsavilkuma cilnē **Vispārīgi** laukā **Darbības kods** atlasiet **11**.
    10. Pārliecinieties, ka automātiski ir iestatīti lauki **Transports**, **Prece** un **Izcelsmes valsts/reģions**.
    11. Darbību rūtī atlasiet **Saglabāt**.
    12. Pārliecinieties, ka laukam **Darījuma kods** ir atlasīts iestatījums 11.
    13. Darbību rūts cilnē **Rēķins**, sadaļā **Ģenerēt** atlasiet **Rēķins**.
    14. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
    15. Atlasiet **Labi**, lai iegrāmatotu rēķinu.

15. Pārsūtiet darbību uz Intrastat žurnālu un pārskatiet rezultātu:

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Intrastat (pārsūtīšana)** un pārskatiet rezultātu. Ir pievienota jauna rinda, kur **Labojuma** kolonnā tiek parādīta atzīme.

        ![Rinda labojumam Intrastat lapā](media/intrastat_deu_5.png)

16. Atlasiet darbības rindu un tad atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju.

    ![Pārdošanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_deu_6.png)

17. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
18. Dialoglodziņā **Intrastat pārskats** kopsavilkuma cilnes **Parametri** sadaļā **Datums** atlasiet izveidotā pārdošanas pasūtījuma mēnesi.
19. Sadaļā **Eksporta** **opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**.
20. Laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
21. Atlasiet **Labi**, un pārskatiet ģenerēto pārskatu. Nākamajā tabulā ir parādītas vērtības atskaites piemērā.

    | **Nosaukums/vārds, uzvārds**                  | **Pārdošanas rēķins**  |   **Labojums**   | **Kredīta piezīme** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | Atsauces periods           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | referents            | referents            | referents         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11.                 | 11.                 | 11.              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

