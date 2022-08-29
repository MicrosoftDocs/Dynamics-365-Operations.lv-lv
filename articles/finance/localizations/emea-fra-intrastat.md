---
title: Francijas Intrastat
description: Šajā rakstā ir ietverta informācija par Intrastat deklarāciju Francijā.
author: AdamTrukawka
ms.date: 07/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 83af3cf304772085c5a6f0943ab5196fcc0208c9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287023"
---
# <a name="french-intrastat"></a>Francijas Intrastat

[!include[banner](../includes/banner.md)]

Uzņēmumiem Francijā, kas ir reģistrēti pievienotās vērtības nodoklim (PVN) un kas veic tirdzniecību ar citām Eiropas Savienības (ES) valstīm jādeklarē preču un pakalpojumu apmaiņa uz Franciju un no tās. Deklarācijas d'exchanges de biens (Preču tirdzniecības deklarācija vai DEB) ir ES pārdošanas saraksta un Intrastat pārskata kombinācija. Šis pārskats ir jāiesniedz katru mēnesi par visu iekšējo preču pārdošanu.

Varat ģenerēt DEB pārskatu vienā no diviem elektroniskā teksta faila formātiem: SAISUNIC 330 vai INTRACOM formātā.

Šajā tabulā redzami lauki, kas ir iekļauti Francijas Intrastat deklarācijā SAISUNIC 330 formātā. Tabulā tiek norādīts arī lauka pārskata līmenis. Lauks var būt **4** (vienkāršots), **1** (pilns) vai abi.

| **Lauks**                   | **Pārskata līmenis** |
|-----------------------------|------------------|
| Atsauces periods         | 4, 1              | 
| Deklarācijas numurs       | 4, 1              |
| Rindas numurs                 | 4, 1              |
| Valsts ISO kods (FR)       | 4, 1              | 
| Papildu kods          | 4, 1              | 
| Siren numurs                | 4, 1              | 
| PVN Debitora kods        | 4, 1              | 
| Virziena kods              | 4, 1              |
| Transakcijas veids            | 4, 1              | 
| Saistību līmenis            | 4, 1              |
| Preču kods              | 1                | 
| Nacionāls NGP                | 1                | 
| Apgabals (Departaments)         | 1                |
| Darījuma raksturs       | 1                | 
| Izcelsmes valsts      | 1                | 
| IIzcelsmes valsts - imports | 1                | 
| Galamērķis - eksports | 1                | 
| Rēķina vērtība               | 4, 1              | 
| Statistiskā vērtība           | 1                |
| Neto svars                  | 1                | 
| Papildu vienības            | 1                |
| Transportēšanas kods              | 1                | 

Šajā tabulā redzami lauki, kas ir iekļauti Francijas Intrastat deklarācijā INTRACOM formātā.
Tabulā tiek norādīts arī lauka pārskata līmenis. Lauks var būt **4** (vienkāršots), **1** (pilns) vai abi.

| **Lauks**                   | **Pārskata līmenis**   | 
|-----------------------------|--------------------|
| Kods                        | 4, 1               | 
| Deklarācijas numurs       | 4, 1               |
| Rindas numurs              | 4, 1               | 
| Siren                       | 4, 1               |
| Apgabals (Departaments)         | 1                  |          
| Transportēšanas kods              | 1                  |          
| Izcelsmes valsts           | 1                  |            
| Darījuma raksturs       | 1                  |             
| Rēķina vērtība               | 4, 1               |             
| Piegādes veidi           | 1                  |           
| Transakcijas veids            | 4, 1               |            
| Saistību līmenis            | 4, 1               |           
| Preču kods              | 1                  |            
| Nacionāls NGP                | 1                  |            
| Neto svars                  | 1                  |            
| Statistiskā vērtība           | 1                  |            
| Papildu vienības            | 1                  |            
| IIzcelsmes valsts - imports | 1                  |            
| Galamērķis - eksports | 1                  |            
| PVN Debitora kods        | 4, 1               |            
| Papildu kods          | 4, 1               |           
| Atsauces periods         | 4, 1               |         

### <a name="set-up-intrastat"></a>Iestatīt Intrastat

1.  Programmas [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) koplietojamo līdzekļu bibliotēkā lejupielādējiet tālāk norādīto Elektronisko pārskatu (ER) konfigurāciju jaunākās versijas Intrastat deklarācijai:

    - Intrastat modelis
    - Intrastat pārskats
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Papildinformāciju skatiet rakstā [Lejupielādēt elektronisko pārskatu konfigurācijas no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Programmā Dynamics 365 Finanses, dodieties uz nodokļu **iestatījuma** > **ārējās** >  **tirdzniecības** > **parametriem** un sekojiet šiem soļiem:

    1. Cilnes **Intrastat** kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **Intrastat INTRACOM (FR)** vai **Intrastat SAISUNIC (FR)**.
    2. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
    3. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.
    4. Kopsavilkuma cilnes **Vispārīgi** laukā **Darbības kods** atlasiet kodu, kas tiek izmantots preču pārsūtīšanai.
    5. Laukā **Kredīta nota** atlasiet kodu, kas tiek izmantots preču atgriešanai.
    6. Laukā **Saistību līmenis eksportēšanai** ievadiet detalizācijas līmeni eksporta pārskatam. Atlasītais līmenis ietekmē pārskatā rādītās rindas. Papildinformāciju skatiet tabulas šī raksta sākumā.

3. Dodieties uz **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**, atlasiet uzņēmumu un pēc tam veiciet tālāk aprakstītās darbības.

    1. Kopsavilkuma cilnē **Reģistrācijas numuri** laukā **NAF kods** ievadiet savu NAF kodu. Papildinformāciju skatiet [FR-00003 NAF kodi un Siret numuri](tasks/fr-00003-naf-codes-siret-numbers.md).
    2. Kopsavilkuma cilnē **Ārējā tirdzniecība un loģistika** sadaļā **Intrastat** iestatiet laukus **PVN reģistrācijas numura eksports** un **PVN reģistrācijas numura imports**.
    3. Kopsavilkuma cilnē **Nodokļa reģistrācija**, laukā **Nodokļa reģistrācijas numurs** ievadiet jūsu uzņēmuma nodokļa reģistrācijas numuru.

4. Lai norādītu NAF kodus un PVN reģistrācijas numurus debitoriem, dodieties uz sadaļu **Kreditori** > **Klienti** > **Visi klienti** un veiciet tālāk aprakstītās darbības.

    1. Atlasīt debitoru.
    2. Kopsavilkuma cilnes **Rēķins un piegāde** sadaļas **PVN** laukā **PVN reģistrācijas numurs** ievadiet debitora PVN reģistrācijas numuru.
    3. Kopsavilkuma cilnē **Tirdzniecība demogrāfiskā informācija** laukā **Francijas Siret** ievadiet uzņēmuma Siret numuru.
    4. Laukā **NAF kods** ievadiet uzņēmuma NAF kodu.
    5. Atkārtojiet šīs darbības citiem debitoriem.

5. Lai norādītu NAF kodus un PVN reģistrācijas numurus kreditoriem, dodieties uz sadaļu **Kreditori** > **Piegādātāji** > **Visi piegādātāji** un veiciet tālāk aprakstītās darbības.

    1. Atlasiet kreditoru.
    2. Kopsavilkuma cilnes **Rēķins un piegāde** sadaļas **PVN** laukā **PVN reģistrācijas numurs** ievadiet kreditora PVN reģistrācijas numuru.
    3. Kopsavilkuma cilnē **Pirkšanas demogrāfiskā informācija** laukā **Francijas Siret** ievadiet uzņēmuma Siret numuru.
    4. Laukā **NAF kods** ievadiet uzņēmuma NAF kodu.
    5. Atkārtojiet šīs darbības citiem kreditoriem.

6. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Intrastat arhivēšana** un atlasiet laukus, kas jāsalīdzina, kad tiek apkopota Intrastat informācija. Francijas Intrastat izvēlieties **Statistikas procedūru**, **Izcelsmes valsti**, **Izcelsmes valsti/reģionu**, **Piegādes nosacījumus**, **Transportēšanu**, **Labojumu**, **Valsti/reģionu**, **Izcelsmes/adresāta apgabalu**, **Virzienu**, **Sūtītāja valsti/reģionu**, **Sūtītāja valsti**, **Valsti**, **Darījumu kodu** un **Preci**.

7. Dodieties uz **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Noliktavas**, atlasiet noliktavu un pēc tam veiciet šādas darbības:

    1. Kopsavilkuma cilnē **Adreses** atlasiet **Pievienot** vai **Rediģēt**.
    2. Dialoglodziņā laukā **Pilsēta** atlasiet noliktavas pilsētu. Jūsu DEB pārskatam pilsētas štats tiks izmantots kā apgabals.

### <a name="ngp-codes"></a>NGP kodi (Francija)

Attiecībā uz DEB pārskatu ražojumu kodifikāciju veido šādi elementi:

  - Astoņciparu CN8 kods, kas attēlo ES tarifu un statistikas nomenklatūru.
  - Ja piemērojams, valsts krājuma kods – vienciparu Nomenclature Générale des Produits (NGP).

2021. gadā NGP attiecas tikai uz trīs produktu veidiem:

  - Daži produkti no govīm, aitām un kazām
  - Kara iekārtas
  - Francijas vīni

 Jums jāiestata NGP kodi un jāpiešķir tos saistītiem produktiem. Pēc tam **NGP** lauks tiek automātiski iestatīts lapā **Intrastat žurnāls**.

#### <a name="set-up-an-ngp-code"></a>Iestatīt NGP kodu

1. Dodieties uz **Nodokļi** > **Iestatīšana** > **Ārējā tirdzniecība** > **Transakciju kodi**.
2. Lai izveidotu NGP kodu, darbību rūtī atlasiet **Jauns**.
3. Laukā **NGP** ievadiet viencipara kodu.
4. Laukā **Apraksts** ievadiet koda aprakstu.

#### <a name="assign-an-ngp-code-to-a-product"></a>Piešķirt produktam NGP kodu

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet preci.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **NGP** izvēlieties atbilstošo NGP kodu.

## <a name="intrastat-journal"></a>Intrastat žurnāls

Lai pārvaldītu darījumus, kas ir attiecināmi uz ārējo tirdzniecību ar ES valstīm, dodieties uz **Nodoklis** > **Deklarācijas** > **Ārējā** **tirdzniecība** > **Intrastat**. Papildinformāciju skatiet tēmā [Pārskats par Intrastat](emea-intrastat.md).

Kolonna **NGP** ir raksturīga Francijai. Tas parāda preces NGP kodu. Ja NGP nav piederīgs precei, parādās **0** (nulle). Varat pielāgot NGP kodu. Izvēlieties darbību un tad cilnē **Vispārīgi** sadaļā **Kodi** laukā **NGP** izvēlieties nepieciešamo NGP kodu.

### <a name="intrastat-transfer"></a>Intrastat pārsūtīšana

Lapā **Intrastat** darbību rūtī varat atlasīt **Pārsūtīt**, lai automātiski pārsūtītu informāciju par EK iekšējo tirdzniecību no pārdošanas pasūtījumiem, brīva teksta rēķiniem, pirkšanas pasūtījumiem, kreditora rēķiniem, kreditora produktu ieejas plūsmām, projekta rēķiniem un pārsūtīšanas pasūtījumiem. Tiks pārsūtīti tikai dokumenti, kuriem kā adresāta valsts vai reģions (nosūtīšanai) vai sūtījumam (ierašanai) ir ES valsts.

Tā kā DEB pārskats ir ES pārdošanas saraksta un Intrastat pārskata kombinācija, tajā iekļautas arī *trīspusējas* darbības, kur tiešā piegāde ir veikta no vienas ES valsts (A puse) uz citu ES valsti (C pusi), un Francijas juridiskā persona (B puse) ir triangulāra darījuma vidū.

### <a name="generate-a-deb-intrastat-report"></a>Ģenerēt DEB (Intrastat) pārskatu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
3. Dialoglodziņā **Intrastat pārskats** iestatiet tālak norādītos laukus.

    | Lauks            | Apraksts                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | No datuma        | Atlasiet pārskata sākuma datumu.                                                                                               |
    | Līdz datumam          | Atlasiet pārskata beigu datumu.                                                                                                 |
    | Ģenerēt failu    | Iestatiet šo opciju kā **Jā**, lai ģenerētu .txt failu.                                                                                 |
    | Faila nosaukums        | Ievadiet .txt faila nosaukumu savam Intrastat pārskatam.                                                                          |
    | Ģenerēt pārskatu  | Iestatiet šo opciju kā **Jā**, lai ģenerētu .xml failu.                                                                                |
    | Pārskata faila nosaukums | Ievadiet nepieciešamo nosaukumu.                                                                                                            |
    | Tikai labojumi | Iestatiet šo opciju uz **Jā**, lai ziņotu tikai par labojumiem. Iestatiet to uz **Nē**, lai pārskatā ziņotu gan parastās darbības, gan korekcijas.         |
    | Virziens        | Atlasiet **Saņemšanas** pārskatam par EK iekšējām saņemšanas. Atlasiet **Nosūtīšanas** pārskatam par EK iekšējām nosūtīšanām. |

## <a name="example"></a>Paraugs

Turpmāk redzamais piemērs parāda, kā iestatīt Francijas Intrastat un strādāt ar DEP pārskatiem. Tas izmanto **DEMF** juridisku personu.

1. Programmas [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) koplietojamo līdzekļu bibliotēkā lejupielādējiet tālāk norādīto ER konfigurāciju jaunākās versijas Intrastat deklarācijas formātam:

    - Intrastat modelis
    - Intrastat pārskats
    - Intrastat INTRACOM (FR)

2. Risinājumā Finance iestatījumos iestatiet darbības kodu:

    1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **Transakcijas kods** ievadiet **11**.
    4. Laukā **Nosaukums** ievadiet **Pirkšana vai pārdošana**.
    5. Darbību rūtī atlasiet **Saglabāt**.

3.  Iestatiet preču hierarhiju:

    1. Atveriet **Preču informācijas pārvaldība** > **Iestatīšana** > **Kategorijas un atribūti** > **Kategoriju hierarhijas**.
    2. Režģī atlasiet **Intrastat**. Pēc tam, darbību rūts cilnē **Kategoriju hierarhija**, grupā **Uzturēt** atlasiet **Rediģēt**.
    3. Darbību rūtī atlasiet **Jauns kategorijas zars**.
    4. Laukā **Nosaukums** ievadiet **Autres Libournais**.
    5. Laukā **Kods** ievadiet **2204 21 42**
    6. Darbību rūtī atlasiet **Saglabāt**.

4. Dodieties uz **Nodoklis** > **Iestatīšana** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri** un izpildiet tālāk norādītās darbības:

    1. Kopsavilkuma cilnes **Intrastat** kopsavilkuma cilnē **Vispārīgi** laukā **Darbības kods** atlasiet **11**.
    2. Kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **Intrastat INTRACOM (FR)**.
    3. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
    4. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.

5. Iestatīt NGP kodu:

    1. Dodieties uz **Nodokļi** > **Iestatīšana** > **Ārējā tirdzniecība** > **Transakciju kodi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **NGP** ievadiet **8**.
    4. Laukā **Apraksta nosaukums** ievadiet **NGP 8**.
    5. Darbību rūtī atlasiet **Saglabāt**.

6. Piešķirt produktam NGP kodu:

    1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
    2. Režģī atlasiet **0001**.
    3. Kopsavilkuma cilnes **Ārējā tirdzniecība** laukā **NGP** atlasiet **8**.
    4. Laukā **Prece** atlasiet **2204 21 42**.
    5. Darbību rūtī atlasiet **Saglabāt**.

7. Izveidojiet pārdošanas pasūtījumu, kas ietver jauno preci:

    1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Dialoglodziņā **Izveidot** **pārdošanas** **pasūtījumu** sadaļā **Klients** laukā **Klienta** **konts** atlasiet **100001**.
    4. Sadaļas **Adrese** laukā **Piegādes adrese**, lai izveidotu adresi, izvēlieties plus zīmi (**+**).
    5. cDialoglodziņa **Jauna adrese** laukā **Apraksta nosaukums** ievadiet **Vācija**.
    6. Laukā **Valsts/reģions** atlasiet **DEU**.
    7. Atlasiet **Labi**.
    8. Dialoglodziņā **Pārdošanas pasūtījuma izveide** atlasiet **Labi**.
    9. Kopsavilkuma cilnes **Pārdošanas** **pasūtījuma rindas** laukā **Preces numurs** atlasiet **0001**.
    10. Darbību rūtī atlasiet **Saglabāt**.
    11. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
    12. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**. Pēc tam atlasiet **Labi**, lai grāmatotu rēķinu.

8.  DEB pārskata izveidošana:

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**:
    2. Sadaļā Darbību rūts. atlasiet **Pārsūtīt**.
    3. Dialoglodziņa **Intrastat (Pārsūtīšana)** sadaļā **Parametri** iestatiet opciju **Debitora rēķins** uz **Jā**. Pēc tam atlasiet **Labi**.
    4. Kārtojiet transakcijas pēc lauka **Datums**. Augšējā transakcija ir rezultāta transakcija. Lauks **NGP** tiek iestatīts automātiski.
    5. Darbību rūtī atlasiet **Rezultāts** &gt; **Pārskats**.
    6. Dialoglodziņā **Intrastat pārskats** kopsavilkuma cilnes **Parametri** sadaļā **Datums** atlasiet izveidotā pārdošanas pasūtījuma mēnesi.
    7. Sadaļā **Eksporta opcijas** iestatiet opciju **Ģenerēt failu** uz **Jā**.
    8. Laukā **Faila nosaukums** ievadiet nepieciešamo nosaukumu.
    9. Atlasiet **Labi**, un pārskatiet pārskatu.

