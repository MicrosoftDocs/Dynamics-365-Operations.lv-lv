---
title: Intrastat saņemtā un nosūtītā grāmatošana
description: Šajā rakstā sniegts piemērs, kurā parādīts, kā grāmatot Intrastat saņemšanas un nosūtīšanas.
author: anasyash
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: aef20f0261e103be7fe231a7efb39751ab4d1151
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862969"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Intrastat saņemtā un nosūtītā grāmatošana

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegts piemērs, kurā parādīts, kā grāmatot Intrastat saņemšanas un nosūtīšanas. Piemērā tiek izmantota **ITCO** juridiskā persona.

## <a name="setup"></a>Iestatīt

1. Importējiet pēdējo elektronisko pārskatu (ER) konfigurāciju versiju:

    - Intrastat modelis
    - Intrastat pārskats
    - Intrastat (IT)

    Plašāka informācija pieejama rakstā [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Microsoft Dynamics 365 Finansēs definējiet šādas numuru sērijas kā nepārtrauktas: **Numerācija\_ 397**, **Aiko\_ kods 16403**, **Ierašana\_ 407** un **PUR\_ ES**.

    1. Atveriet **Organizācijas administrēšana** > **Numuru sērijas** > **Numuru sērijas**.
    2. Režģī atlasiet vienu no numuru sērijas kodiem.
    3. Darbību rūtī atlasiet **Rediģēt**.
    4. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Iestatīšana** iestatiet opcijas **Pastāvīgi** vērtību uz **Jā**.
    5. Darbību rūtī atlasiet **Saglabāt**.

3. Iestatiet noliktavas adresi.

    1. Dodieties uz **Noliktavas vadība** &gt; **Iestatīšana** &gt; **Noliktava** &gt; **Noliktavas**.
    2. Sarakstā atlasiet noliktavu Nr. **11**.
    3. Kopsavilkuma cilnē **Adrese** atlasiet **Pievienot**.
    4. Dialoglodziņa **Jauna** **adrese** laukā **Nosaukums** **vai** **apraksts** ievadiet **Galvenā**.
    5. Laukā **Valsts/reģions** atlasiet **ITA (Itālija)**.
    6. Laukā **Pilsēta** izvēlieties **Aprilia**.
    7. Atlasiet **Labi**.

4. Iestatiet transakciju kodus.

    1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
    2. Atlasiet **Jauns** un iestatiet transakcijas kodu īpašuma pārsūtīšanai.

        - Laukā **Transakcijas kods** ievadiet **1**.
        - Laukā **Nosaukums** ievadiet **Īpasuma pārsūtīšana**.

    3. Atlasiet **Jauns** un iestatiet transakcijas kodu īpašuma atgriešanai.

        - Laukā **Transakcijas** **kods** ievadiet **2**.
        - Laukā **Nosaukums** ievadiet **Preču atgriešana**.

5.  Iestatīt starptautiskās tirdzniecības parametrus.

    1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
    2. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **1**.
    3. **Kredīta notas** laukā atlasiet **2**.
    4. Laukā **Pārdošanas pārskata periods** atlasiet **Mēnesis**.
    5. Laukā **Pirkšanas pārskata periods** atlasiet **Mēnesis**.
    6. Kopsavilkuma cilnē **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **Intrastat (IT)**.
    7. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats**.
    8. Kopsavilkuma cilnes **Preču kodu hierarhija** laukā **Kategoriju hierarhija** atlasiet **Intrastat**.
    9. Kopsavilkuma cilnē **Statistiskā vērtība** iestatiet opciju **Drukāt un eksportēt statistikas datus** uz **Jā**.
    10. Cilnē **Valsts/reģiona rekvizīti** pārbaudiet, vai pastāv šādas rindas.

        | **Puse/valsts/reģions** | **Intrastat kods** | **Valūta** | **Valsts/reģiona veids** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Iekšzemes                |
        | SMR                      | SM                 | EUR          | Īpašs vietējs        |

    11. Rīkjoslā atlasiet **Jauns**, lai izveidotu tālāk minēto rindu.

        | **Puse/valsts/reģions** | **Intrastat kods** | **Valūta** | **Valsts/reģiona veids** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | ES                      |

6. Iestatiet numurus atbrīvošanai no PVN.

    1. Atveriet **Nodoklis** > **Iestatīšana** > **PVN** > **PVN reģistrācijas numuri**.
    2. Darbību rūtī atlasiet **Jauns**, lai izveidotu tālāk minētās rindas.

        | **Valsts/reģions** | **PVN reģistrācijas numurs** | **Uzņēmuma nosaukums** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE VENDOR        |
        | DNK                | DK0987654321          | Klienta ER      |

7. Iestatiet kreditora adresi.

    1. Dodieties uz **Kreditori** &gt; **Kreditori** &gt; **Visi kreditori**.
    2. Režģī atlasiet **UE Vendor**.
    3. Kopsavilkuma cilnē **Adreses** atlasiet **Pievienot**.
    4. Dialoglodziņa **Jauna adrese** laukā **Apraksts vai nosaukums** ievadiet **Vācija**.
    5. Laukā **Valsts/reģions** atlasiet **DEU**.
    6. Atlasiet **Labi**, lai izveidotu jaunu adresi.
    7. Kopsavilkuma cilnes **Rēķins un piegāde** sadaļā **PVN** laukā **PVN reģistrācijas numurs** atlasiet **Visi** un atlasiet **DE1234567890**.
    8. Darbību rūtī atlasiet **Saglabāt**.

8. Iestatiet klientu adreses.

    1. Atveriet **Debitori** > **Debitori** > **Visi debitori**.
    2. Režģī atlasiet **ITCO-000001**.
    3. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
    4. Dialoglodziņa **Jauna adrese** laukā **Apraksts vai nosaukums** ievadiet **Sanmarīno**.
    5. Laukā **Valsts/reģions** atlasiet **SMR**.
    6. Atlasiet **Labi**, lai izveidotu jaunu adresi.
    7. Kopsavilkuma cilnes **Rēķins un piegāde** sadaļā **Rēķins** laukā **Rēķina konts** atlasiet **ITCO-000001**.
    8. Laukā **Numuru sēriju grupa** atlasiet **IT\_VENDOM**.
    9. Darbības rūtī atlasiet **Saglabāt** un aizveriet lapu.
    10. Lapas **Visi debitori** režģī atlasiet **ITCO-000002**.
    11. Kopsavilkuma cilnē **Adreses** atlasiet **Pievienot**.
    12. Dialoglodziņa **Jauna adrese** laukā **Apraksts vai nosaukums** ievadiet **Dānija**.
    13. Laukā **Valsts/reģions** atlasiet **DNK**.
    14. Atlasiet **Labi**, lai izveidotu jaunu adresi.
    15. Kopsavilkuma cilnes **Pārdošanas demogrāfiskie dati** laukā **Valūta** atlasiet **DKK**.
    16. Kopsavilkuma cilnē **Rēķins un piegāde** sadaļas **PVN** laukā **PVN grupa** atlasiet **IT\_PUREU**.
    17. Laukā **PVN reģistrācijas numurs** atlasiet **Visi** un pēc tam atlasiet **DK0987654321**.
    18. Darbību rūtī atlasiet **Saglabāt**.

9. Iestatiet kategoriju hierarhiju.

    1. Atveriet **Preču informācijas pārvaldība** > **Iestatīšana** > **Kategorijas un atribūti** > **Kategoriju hierarhijas**.
    2. Režģī atlasiet **Intrastat**.
    3. Darbību rūtī atlasiet **Jauns kategorijas zars**.
    4. Laukā **Nosaukums** ievadiet **Pakalpojums**.
    5. Laukā **Kods** ievadiet **123456**.
    6. Darbību rūtī atlasiet **Saglabāt**.

10. Iestatiet preces.

    1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
    2. Režģī atlasiet **ITEM**.
    3. Kopsavilkuma cilnē **Pirkums** sadaļas **Administrēšana** laukā **Kreditors** atlasiet **ITCO-000001**.
    4. Kopsavilkuma cilnē **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Prece** atlasiet **\[100 200 30\] Speaker**.
    5. Sadaļas **Izcelsme** laukā **Valsts/reģions** atlasiet **DEU**.
    6. Laukā **Štats/province** atlasiet **BE**.
    7. Kopsavilkuma cilnē **Krājumu pārvaldība** sadaļas **Neto mērījumi** laukā **Neto svars** ievadiet **5**.
    8. Darbību rūtī atlasiet **Saglabāt**.
    9. Lapā **Izlaistās preces** režģī atlasiet **Pakalpojuma vienība**.
    10. Kopsavilkuma cilnē **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Prece** atlasiet **\[123456\] pakalpojums**.
    11. Darbību rūtī atlasiet **Saglabāt**.

11. Iestatiet transportēšanas metodes.

    1. Atveriet **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transportēšanas metode**.
    2. Darbību rūtī atlasiet **Jauns**, lai izveidotu tālāk minētās transportēšanas metodes.

        | **Transportēšana** | **Apraksts** |
        |---------------|-----------------|
        | 1             | Ceļš            |
        | 2             | Gaiss             |

12. Iestatiet piegādes veidu.

    1. Pārejiet uz sadaļu **Sagāde un avoti** > **Iestatījumi** > **Izplatīšana** > **Piegādes veidi**.
    2. Darbību rūtī atlasiet **Jauns**.
    3. Laukā **Piegādes veids** ievadiet **1**.
    4. Laukā **Apraksts** ievadiet **Kravas automašīna**.
    5. Kopsavilkuma cilnē **Ārējā tirdzniecība** laukā **Transportešana** atlasiet **Ceļš**.
    6. Darbību rūtī atlasiet **Saglabāt**.

13. Iestatiet piegādes nosacījumus.

    1. Atveriet **Kreditori** > **Iestatījumi** > **Piegādes nosacījumi**.
    2. Sarakstā atlasiet **CFR**.
    3. Kopsavilkuma cilnes **Vispārīgi** laukā **Intrastat kods** ievadiet **1**.

## <a name="post-arrivals-for-intrastat"></a>Intrastat saņemšanas grāmatošana

### <a name="purchase-goods-by-using-a-purchase-order"></a>Preču iegāde, izmantojot pirkšanas pasūtījumu

Šī piemēra daļa parāda, kā izmantot pirkšanas pasūtījumu preču (krājumu) pirkšanai no Eiropas Savienības (ES) valstīm.

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2.  Darbību rūtī atlasiet **Jauns**.
3.  Dialoglodziņa **Pirkšanas pasūtījuma izveide** laukā **Kreditora konts** atlasiet **UE kreditors**.
4.  Kopsavilkuma cilnes **Administrēšana** laukā **Valoda** atlasiet **it**.
5.  Atlasiet **Labi**.
6.  Skatā **Virsraksts** kopsavilkuma cilnē **Ārējā** **tirdzniecība** laukam **Transakcijas kods** jābūt **1**.
7.  Laukam **Izcelsmes/adresāta apgabals** jābūt **RM**.
8.  Kopsavilkuma cilnē **Piegāde** sadaļas **Piegāde** laukā **Piegādes veids** atlasiet **1**.
9.  Laukā **Piegādes nosacījumi** atlasiet **CFR**.
10. Skatā **Rindas** kopsavilkuma cilnes **Pirkšanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **Prece**.
11. Laukā **Vieta** atlasiet **1**.
12. Laukā **Noliktava** atlasiet **11**.
13. Laukā **Daudzums** ievadiet **10**.
14. Laukā **Vienības cena** ievadiet **100**.
15. Cilnē **Iestatījumi** sadaļas **PVN** laukā **Krājumu PVN grupa** atlasiet **22%EU**.
16. Darbību rūts cilnē **Pirkšana**, grupā **Darbības** atlasiet **Apstiprināt**.
17. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
18. Darbību rūtī atlasiet **Noklusējuma vērtība No**.
19. Laukā **Noklusējuma daudzums rindām** atlasiet **Pasūtītais daudzums** un **Labi**.
20. Kopsavilkuma cilnes **Kreditora rēķina virsraksts** sadaļā **Rēķina identifikācija** laukā **Numurs** ievadiet **0001**.
21. Sadaļas **Rēķina datumi** laukā **Rēķina datums** atlasiet **7/9/2021**.
22. Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu žurnālu.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Pirkšanas pakalpojumi, izmantojot kreditora rēķinu

Šī piemēra daļa parāda, kā izmantot kreditora rēķinu pakalpojumu pirkšanai no ES valstīm.

1. Atveriet **Kreditori** > **Rēķini** > **Rēķinu žurnāls**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Nosaukums** atlasiet **VEND\_EUINV**.
4. Darbību rūtī atlasiet **Rindiņas**.
5. Laukā **Datums** ievadiet **7/9/2021**.
6. Laukā **Konta veids** atlasiet **Kreditors**.
7. Laukā **Konts** atlasiet **UE kreditors**.
8. Laukā **Rēķina datums** atlasiet **7/9/2021**.
9. Laukā **Rēķins** ievadiet **ITA-0004**.
10. Laukā **Kredīts** ievadiet **120000**.
11. Laukā **Korespondējošā konta** **veids** atlasiet **Virsgrāmata**.
12. Laukā **Korespondējošais konts** atlasiet **110130**.
13. Laukā **PVN grupa** atlasiet **IT\_PUREU**.
14. Laukā **Krājumu PVN grupa** atlasiet **22%EU**.
15. Cilnē **Ārējā tirdzniecība** veiciet tālāk minēto.

    1. Laukā **Transakcijas kods** atlasiet **1**.
    2. Laukā **Transportēšana** atlasiet **2. Pa gaisu**.
    3. Laukā **Prece** atlasiet **\[123456\] Pakalpojums**.
    4. Laukā **Valsts/reģions** atlasiet **ITA**.
    5. Laukā **Štats/province** atlasiet **LAZ**.
    6. Laukā **Izcelsmes/adresāta valsts** atlasiet **LT**.


16. Darbību rūtī atlasiet **Grāmatot**.
17. Izveidojiet Intrastat deklarāciju saņemšanas darbībām.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Kreditora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

   ![Intrastat žurnāla lapa, cilne Pārskats.](media/ita_intrastat_journal_vendor_invoice.png)

18. Pārskatiet pirkšanas pasūtījuma cilni **Vispārīgi**.

    ![Intrastat žurnāla rindas informācija pirkšanas pasūtījumam](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Pārskatiet kreditora rēķina cilni **Vispārīgi**.

    ![Intrastat žurnāla rindas detalizēta informācija kreditora rēķinam](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Ģenerējiet Intrastat pārskatu saņemšanai.

    1. Darbību rūtī atlasiet **Izvade** > **Pārskats**.
    2. **Intrastat pārskata** dialoglodziņā sadaļas **Datums** laukā **Sākuma datums** atlasiet **7/1/2021**.
    3. Laukā **Beigu datums** atlasiet **7/31/2021**.
    4. Sadaļā **Eksporta opcijas** iestatiet opciju **Ģenerēt failu** un **Ģenerēt pārskatu** uz **Jā**.
    5. Laukā **Faila nosaukums** ievadiet **Saņemšanas fails**.
    6. Laukā **Pārskata faila nosaukums** ievadiet **Saņemšanas pārskats**.
    7. Laukā **Virziens** atlasiet **Saņemšana**.
    8. Laukā **Atsauces numurs** ievadiet **123456**.
    9. Atlasiet **Labi**, lai ģenerētu Intrastat pārskatu un Intrastat failu un tos pārskatītu.

    Šajā attēlā parādīts Intrastat pārskata piemērs.

    ![Intrastat saņemšanas pārskats.](media/ita_intrastat_arrivals_report.png)

    Šajā attēlā parādīts Intrastat faila piemērs.

    ![Intrastat saņemšanas fails.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Intrastat nosūtīšanas grāmatošana

### <a name="sell-goods-by-using-a-sales-order"></a>Preču pārdošana, izmantojot pārdošanas pasūtījumu

Šī piemēra daļa parāda, kā izmantot pārdošanas pasūtījumu preču (krājumu) pārdošanai Eiropas Savienības (ES) valstīm.

1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pārdošanas pasūtījuma izveide** laukā **Klienta konts** atlasiet **ITCO-000002**.
4. Atlasiet **Labi**.
5. Skatā **Virsraksts** kopsavilkuma cines **Piegāde** sadaļas **Dažāda piegādes informācija** laukā **Piegādes veids** atlasiet **1. Kravas automašīna**.
6. Laukā **Piegādes nosacījumi** atlasiet **CFR**.
7. Skatā **Rindas** kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **ITEM**.
8. Laukā **Daudzums** ievadiet **50**.
9. Laukā **Vieta** atlasiet **1**.
10. Laukā **Noliktava** atlasiet **11**.
11. Laukā **Vienības cena** ievadiet **250**.
12. Kopsavilkuma cilnē **Rindas informācija**, cilnē **Iestatījumi** sadaļas **Sales tax** laukā **Krājumu PVN grupa** atlasiet **22%EU**.
13. Darbību rūtī atlasiet **Saglabāt**.
14. Darbību rūtī cilnes **Rēķins** grupā **Izveide** atlasiet **Rēķins**, lai izveidotu pasūtījuma rēķinu.
15. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Parametri** sadaļā **Parametri** laukā **Daudzums** atlasiet **Visi**.
16. Kopsavilkuma cilnes **Iestatījumi** laukā **Rēķina** **datums** atlasiet **7/9/2021**.
17. Atlasiet **Labi**.
18. Pārskatiet Intrastat žurnāla rindas.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu. Kredīta notas transakcija ir atzīmēta kā labojums, un tai ir negatīva rēķina summa.

        ![Intrastat žurnāla lapa](media/ita_intrastat_journal_sales_order.png)

        ![Intrastat žurnāla rindas informācija pārdošanas pasūtījumam](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Preču atgriešana, izmantojot kredīta notu

Šī piemēra daļa parāda, kā izmantot kredīta noru preču (krājumu) atgriešanai no Eiropas Savienības (ES) valstīm.

1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pārdošanas pasūtījuma izveide** laukā **Klienta konts** atlasiet **ITCO-000002**.
4. Atlasiet **Labi**.
5. Skatā **Virsraksts** kopsavilkuma cines **Piegāde** sadaļas **Dažāda piegādes informācija** laukā **Piegādes veids** atlasiet **1. Kravas automašīna**.
6. Laukā **Piegādes nosacījumi** atlasiet **CFR**.
7. Kopsavilkuma cilnes **Ārējā tirdzniecība** laukā **Transakcijas kods** atlasiet **2**.
8. Cilnē **Rindas** kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **ITEM**.
9. Laukā **Daudzums** ievadiet **-10**.
10. Laukā **Vieta** atlasiet **1**.
11. Laukā **Noliktava** atlasiet **11**.
12. Laukā **Vienības cena** ievadiet **250**.
13. Kopsavilkuma cilnē **Rindas informācija**, cilnē **Iestatījumi** sadaļas **Sales tax** laukā **Krājumu PVN grupa** atlasiet **22%EU**.
14. Sadaļas **Atgrieztais pasūtījums** laukā **Atgrieztā laidiena ID** atlasiet iepriekš izveidoto laidienu.
15. Darbību rūtī atlasiet **Saglabāt**.
16. Darbību rūtī cilnes **Rēķins** grupā **Izveide** atlasiet **Rēķins**, lai izveidotu pasūtījuma rēķinu.
17. Kopsavilkuma cilnē **Parametri** sadaļas **Parametrs** laukā **Daudzums** atlasiet **Visi**.
18. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Iestatījumi** laukā **Rēķina** **datums** atlasiet **7/9/2021**.
19. Atlasiet **Labi**, lai iegrāmatotu rēķinu.
20. Pārskatiet Intrastat žurnāla rindas.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu. Kredīta notas transakcija ir atzīmēta kā labojums, un tai ir negatīva rēķina summa.

    ![Intrastat žurnāla kredīta nota](media/ita_intrastat_journal_credit_note.png)

    ![Intrastat žurnāla rindas detalizēta informācija kredīta notai](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Preču pārdošana Sanmarīno, izmantojot pārdošanas pasūtījumu

Šī piemēra daļa parāda, kā izmantot pārdošanas pasūtījumu preču (krājumu) iegādei Sanmarīno.

1. Ejiet uz **Debitori** > **Pasūtījumi** > **Visi pārdošanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pārdošanas pasūtījuma izveide** laukā **Klienta konts** atlasiet **ITCO-000001**.
4. Atlasiet **Labi**.
5. Skatā **Virsraksts** kopsavilkuma cines **Piegāde** sadaļas **Dažāda piegādes informācija** laukā **Piegādes veids** atlasiet **1**.
6. Laukā **Piegādes nosacījumi** atlasiet **CFR**.
7. Cilnē **Rindas** kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **ITEM**.
8. Laukā **Daudzums** ievadiet **30**.
9. Laukā **Vieta** atlasiet **1**.
10. Laukā **Noliktava** atlasiet **11**.
11. Laukā **Vienības cena** ievadiet **200**.
12. Darbību rūtī atlasiet **Saglabāt**.
13. Darbību rūtī cilnes **Rēķins** grupā **Izveide** atlasiet **Rēķins**, lai izveidotu pasūtījuma rēķinu.
14. Kopsavilkuma cilnē **Parametri** sadaļas **Parametrs** laukā **Daudzums** atlasiet **Visi**.
15. Dialoglodziņa **Rēķina grāmatošana** kopsavilkuma cilnes **Iestatījumi** laukā **Rēķina** **datums** atlasiet **7/9/2021**.
16. Atlasiet **Labi**, lai iegrāmatotu rēķinu.
17. Pārskatiet Intrastat žurnāla rindas.

    1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
    2. Darbību rūtī atlasiet **Pārsūtīt**.
    3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Debitora rēķins** uz **Jā**.
    4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

   ![Intrastat žurnāls Sanmarīno](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Intrastat žurnāla rindas detalizēta informācija Sanmarīno](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Izveidojiet Intrastat deklarāciju nosūtīšanas darbībām.

    1. Dodieties uz **Nodokļi** &gt; **Deklarācijas** &gt; **Ārējā tirdzniecība** &gt; **Intrastat**.
    2. Darbību rūtī atlasiet **Rezultāts** &gt; **Pārskats**.
    3. **Intrastat pārskata** dialoglodziņā sadaļas **Datums** laukā **Sākuma datums** atlasiet **7/1/2021**.
    4. Laukā **Beigu datums** atlasiet **7/31/2021**.
    5. Sadaļā **Eksporta opcijas** iestatiet opciju **Ģenerēt failu** un **Ģenerēt pārskatu** uz **Jā**.
    6. Laukā **Faila nosaukums** ievadiet **Nosūtīšanas fails**.
    7. Laukā **Pārskata faila nosaukums** ievadiet **Nosūtīšanas pārskats**.
    8. Laukā **Virziens** atlasiet **Nosūtīšana**.
    9. Laukā **Atsauces numurs** ievadiet **98754**.
    10. Atlasiet **Labi**, lai ģenerētu Intrastat pārskatu un Intrastat failu.

        Šajā attēlā parādīts izdrukāta Intrastat pārskata piemērs.

        ![Intrastat pārskats](media/ita_intrastat_report_for_dispatches.png)

        Šajā attēlā parādīts izdrukāta Intrastat faila piemērs.

        ![Intrastat fails nosūtīšanai](media/ita_intrastat_file_for_dispatches.png)
