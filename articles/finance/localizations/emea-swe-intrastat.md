---
title: Zviedrijas Intrastat
description: Šajā tēmā ir ietverta informācija par Intrastat pārskatiem Zviedrijā.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 1031b93950e44fe3b1b6254bf1503b4c09d6fd10
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727403"
---
# <a name="swedish-intrastat"></a>Zviedrijas Intrastat

[!include[banner](../includes/banner.md)]

Lapa **Intrastat** tiek izmantota, lai veidotu un paziņotu informāciju par tirdzniecību starp Eiropas Savienības (ES) valstīm. Zviedrijas Intrastat deklarācija satur informāciju par preču tirdzniecību pārskatam.

Zviedrijas Intrastat deklarācijā ir iekļauti šādi lauki:

   - Partnera valsts ISO kods
   - Darbības kods
   - Preču kods
   - Papildu vienība
   - Lielums
   - Rēķina summa

## <a name="set-up-intrastat"></a>Iestatīt Intrastat

Importējiet pēdējo elektronisko pārskatu (ER) konfigurāciju versiju:

   - Intrastat modelis
   - Intrastat pārskats
   - Intrastat (SE)

Plašāka informācija pieejama rakstā [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

1. Microsoft Dynamics 365 Finanšu gadā dodieties uz **TaxSetupForeign** > **·** > **tirdzniecības parametriem**.
2. Kopsavilkuma cilnē **Elektroniskie pārskati** cilnē **Intrastat** laukā **Failu formātu kartēšana** atlasiet **Intrastat (SE)**.
3. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
4. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.
5. **Transakcijas kods** – izvēlieties transakcijas kodu īpašuma pārsūtīšanai. Varat izmantot šo kodu transakcijām, kas izraisa faktisko vai plānoto īpašuma pārsūtīšanu attiecībā uz kompensāciju (finansiālu vai cita veida). To izmanto arī labojumiem. Uzņēmumi Zviedrijā izmanto viena cipara darbības kodus.
6. Laukā **Kredīta nota** izvēlieties transakcijas kodu preču atgriešanai.
7. Cilne **Valsts/reģiona rekvizīti**, lauks **Valsts/reģions** uzskaita visas valstis vai reģionus, ar kuriem jūsu organizācija veic darījumus. Katrai ES dalībvalstij laukā **Valsts/reģiona tips** atlasiet **ES**, lai valsts vai reģions parādītos Intrastat pārskatā.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Preču parametru iestatīšana Intrastat deklarācijai

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet preci.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Prece** izvēlieties atbilstošo preces kodu.
4. Kopsavilkuma cilnes **Krājumu pārvaldība** laukā **Neto svars**  ievadiet preces svaru kilogramos.
5. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Intrastat arhivēšana** un atlasiet laukus, kas jāsalīdzina, kad tiek apkopota Intrastat informācija. Zviedrijas Intrastat atlasiet šādus laukus:

    - Prece
    - Darbības kods
    - Virziens
    - Valsts/reģions
    - Labojums
    - Rēķins

## <a name="intrastat-transfer"></a>Intrastat pārsūtīšana

Lapā **Intrastat** darbību rūtī varat atlasīt **Pārsūtīt**, lai automātiski pārsūtītu informāciju par EK iekšējo tirdzniecību no pārdošanas pasūtījumiem, brīva teksta rēķiniem, pirkšanas pasūtījumiem, kreditora rēķiniem, kreditora produktu ieejas plūsmām, projekta rēķiniem un pārsūtīšanas pasūtījumiem. Tiks pārsūtīti tikai dokumenti, kuriem kā adresāta valsts vai reģions (nosūtīšanai) vai sūtījumam (ierašanai) ir ES valsts.

Alternatīvi transakcijas variet ievadīt manuāli, darbību rūtī atlasot **Jauns**.

### <a name="generate-an-intrastat-report"></a>Ģenerēt Intrastat pārskatu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
3. Dialoglodziņā **Intrastat pārskats** iestatiet tālak norādītos laukus.

    | Lauks            | Apraksts                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | No datuma        | Atlasiet pārskata sākuma datumu.                                                                                               |
    | Līdz datumam          | Atlasiet pārskata beigu datumu.                                                                                                 |
    | Ģenerēt failu    | Iestatiet šo opciju kā **Jā**, lai ģenerētu .txt failu Intrastat pārskatam.                                                       |
    | Faila nosaukums        | Ievadiet .txt faila nosaukumu.                                                                                                    |
    | Ģenerēt pārskatu  | Iestatiet šo opciju kā **Jā**, lai ģenerētu .xlsx failu Intrastat pārskatam.                                                     |
    | Pārskata faila nosaukums | Ievadiet .xlsx faila nosaukumu.                                                                                                   |
    | Virziens        | Atlasiet **Saņemšanas** pārskatam par EK iekšējām saņemšanas. Atlasiet **Nosūtīšanas** pārskatam par EK iekšējām nosūtīšanām. |

4. Atlasiet **Labi**, un pārskatiet ģenerētos pārskatus.

## <a name="example"></a>Paraugs

Šis piemērs parāda, kā grāmatot Intrastat saņemto un nosūtīto. Tas izmanto **DEMF** juridisku personu.

### <a name="preliminary-setup"></a>Iepriekšēja iestatīšana

1. Atveriet **Organizācijas administrēšana** > **Organizācija** > **Juridiskās personas** un atlasiet juridisko personu **DEMF**.
2. Kopsavilkuma cilnē **Addreses** atlasiet **Rediģēt** un pēc tam laukā **Valsts/reģions** atlasiet **SWE (Zviedrija)**.
3. Importējiet pēdējo ER konfigurāciju versiju:

    - Intrastat modelis
    - Intrastat pārskats
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Transakciju kodu izveide

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Transakcijas** **kods** ievadiet **1**.
4. Laukā **Nosaukums** ievadiet **Parastas transakcijas**.
5. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
2. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **1**.
3. Kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **Intrastat (SE)**.
4. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
5. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** pārbaudie, vai atlasījāt **Intrastat**.
6. Cilnē **Valsts/reģiona rekvizīti** atlasiet **Jauns**.
7. Laukā **Puses valsts/reģions** atlasiet **SWE**.
8. Laukā **Valsts/reģiona tips** atlasiet **Iekšzemes**.
9. Laukā **Puses valsts/reģions** atlasiet **DEU** un pēc tam laukā **Valsts/reģiona tips** atlasiet **EU**.

### <a name="set-up-product-information"></a>Preces informācijas iestatīšana

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet **D0001**.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **100 200 30**.
4. Kopsavilkuma cilnes **Pārvaldīt krājumu** sadaļā **Svara mērījumi** laukā **Neto svars** ievadiet **5**.
5. Darbību rūtī atlasiet **Saglabāt**.

### <a name="change-the-site-address"></a>Vietnes adreses maiņa

1. Atveriet **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Vietnes**.
2. Režģī atlasiet **1**.
3. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
4. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **SWE**.
5. Atlasiet **Labi**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Pārdošanas pasūtījuma izveide ar ES debitoru

1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņā **Izveidot pārdošanas pasūtījumu**, kopsavilkuma cilnē **Debitors**, sadaļā **Debitors**, laukā **Debitora konts** atlasiet **DE-015**.
4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Glabāšanas dimensijas** laukā **Vieta** atlasiet **1**.
5. Laukā **Noliktava** atlasiet **11**.
6. Atlasiet **Labi**.
7. Cilnē **Rindas** kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **10**.
8. Kopsavilkuma cilnē **Rindas informācija** cilnē **Ārējā tirdzniecība** gādājiet, lai automātiski tiktu iestatīti lauki **Transakcijas kods** un **Prece**.
9. Darbību rūtī atlasiet **Saglabāt**.
10. Darbību rūts cilnē **Rēķins**, sadaļā **Ģenerēt** atlasiet **Rēķins**.
11. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
12. Atlasiet **Labi**, lai iegrāmatotu rēķinu.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Pārsūtiet transakciju uz Intrastat žurnālu un pārskatiet rezultātu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**.
4. Atlasiet **Filtrēt**.
5. **Intrastat filtra** dialoglodziņa cilnē **Diapazons** atlasiet pirmo rindu un pārliecinieties, vai lauks **Lauks** ir iestatīts uz **Datumu**.
6. Laukā **Kritēriji** atlasiet pašreizējo datumu.
7. Lai aizvērtu dialoglodziņu **Intrastat filtrs**, atlasiet **Labi**.
8. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Intrastat (pārsūtīšana)** un pārskatiet rezultātu. Rindā atlasiet pirmo izveidoto pārdošanas pasūtījumu.

    ![Intrastat žurnāla rindas pārdošanas pasūtījumam](media/swe_intrastat_journal_sales_order.png)

9. Atlasiet darbības rindu un tad atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju.

    ![Intrastat žurnāla rindas informācija pārdošanas pasūtījumam](media/swe_intrastat_journal_sales_order_line_details.png)

10. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
11. Dialoglodziņā **Intrastat pārskats** kopsavilkuma cilnes **Parametri** sadaļā **Datums** atlasiet izveidotā pārdošanas pasūtījuma mēnesi.
12. Sadaļā **Eksporta** **opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**. Pēc tam laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
13. Atlasiet opcijai **Izveidot pārskatu** iestatījumu **Jā**. Pēc tam laukā **Pārskata faila nosaukums** ievadiet nepieciešamo nosaukumu.
14. Laukā **Virziens** atlasiet **Nosūtīšana**.
15. Atlasiet **Labi**, un pārskatiet ģenerēto pārskatu .txt formātā. Nākamajā tabulā ir parādītas vērtības atskaites piemērā.

    | Partnera valsts ISO kods | Darbības kods | Preču kods | Papildu vienība | Lielums | Rēķina summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Pārskatiet ģenerēto pārskatu Excel formātā.

    ![Intrastat pārskats](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pirkšanas pasūtījuma izveide** laukā **Kreditora konts** atlasiet **DE-001**.
4. Atlasiet **Labi**.
5. Cilnē **Virsraksts** kopsavilkuma cilnē **Ārējā** **tirdzniecība** laukam **Transakcijas kods** jābūt **1**.
6. Cilnē **Rindas** kopsavilkuma cilnes **Pirkšanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **D0001**. Laukā **Daudzums** ievadiet **6**.
7. Darbību rūts cilnē **Pirkšana**, grupā **Darbības** atlasiet **Apstiprināt**.
8. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
9. Darbību rūtī atlasiet **Noklusējuma vērtība No**. Laukā **Noklusējuma daudzums rindām** atlasiet **Pasūtītais daudzums**. Pēc tam atlasiet **Labi**.
10. Kopsavilkuma cilnes **Kreditora rēķina virsraksts** sadaļā **Rēķina identifikācija** laukā **Numurs** ievadiet **0001**.
11. Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu žurnālu.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Intrastat deklarācijas izveide saņemšanas darbībām

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Kreditora rēķins** uz **Jā**.
4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

    ![Intrastat žurnāls pirkšanas pasūtījumam](media/swe_intrastat_journal_purchase_order.png)

5. Pārskatiet pirkšanas pasūtījuma cilni **Vispārīgi**.

    ![Intrastat žurnāla rindas informācija pirkšanas pasūtījumam](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
7. Dialoglodziņā **Intrastat pārskats** kopsavilkuma cilnes **Parametri** sadaļā **Datums** atlasiet izveidotā pārdošanas pasūtījuma mēnesi.
8. Sadaļā **Eksporta** **opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**. Pēc tam laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
9. Atlasiet opcijai **Izveidot pārskatu** iestatījumu **Jā**. Pēc tam laukā **Pārskata faila nosaukums** ievadiet nepieciešamo nosaukumu.
10. Laukā **Virziens** atlasiet **Saņemšana**.
11. Atlasiet **Labi**, un pārskatiet ģenerēto pārskatu .txt formātā. Nākamajā tabulā ir parādītas vērtības atskaites piemērā.

    | Partnera valsts ISO kods | Darbības kods | Preču kods | Papildu vienība | Lielums | Rēķina summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Pārskatiet ģenerēto pārskatu Excel formātā.

    ![Intrastat saņemšanas pārskats](media/swe_intrastat_arrivals_report.png)
