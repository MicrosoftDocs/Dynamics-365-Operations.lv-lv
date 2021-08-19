---
title: Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem
description: Šajā tēmā skaidrots jaunās nodokļu funkcionalitātes atbalsts pārsūtīšanas pasūtījumiem, izmantojot nodokļu aprēķināšanas pakalpojumu.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1c47c327841b8c712220e440e2aa6b4fe2b31b4a1ccd03dc0a200dbeb7394071
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721693"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegta informācija par nodokļu aprēķināšanu un integrācijas grāmatošanu pārsūtīšanas pasūtījumos. Šī funkcionalitāte ļauj jums iestatīt nodokļu aprēķinu un grāmatošanu pārsūtīšanas pasūtījumos krājumu pārsūtīšanai. Saskaņā ar Eiropas Savienības (ES) pievienotās vērtības nodokļa (PVN) noteikumiem krājumu pārsūtīšana tiek uzskatīta par piegādi Kopienas iekšienē un iegādi Kopienas iekšienē.

Lai konfigurētu un lietotu šo funkcionalitāti, ir jāveic trīs galvenās darbības:

1. **RCS iestatījumi**: regulēšanas konfigurācijas pakalpojumā iestatiet nodokļu līdzekli, nodokļu kodus un nodokļu kodu piemērojamību nodokļa koda noteikšanai pārsūtīšanas pasūtījumos.
2. **Finanšu iestatīšana**: programmā Microsoft Dynamics 365 Finance līdzekļa **Nodoklis** pārsūtīšanas pasūtījumā iestatiet krājumu nodokļu pakalpojumu parametrus un iestatiet galvenos nodokļu parametrus.
3. **Krājumu iestatīšana**: iestatiet krājumu konfigurāciju pārsūtīšanas pasūtījumu darījumiem.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Nodokļu un pārsūtīšanas pasūtījumu darījumu RCS iestatīšana

Veiciet šīs darbības, lai iestatītu nodokli, kas ir iesaistīts pārsūtīšanas pasūtījumā. Šeit parādītajā piemērā pārsūtīšanas pasūtījums ir no Nīderlandes uz Beļģiju.

1. Lapā **Nodokļu līdzekļi**, cilnē **Versijas** atlasiet melnraksta līdzekļa versiju un pēc tam atlasiet **Rediģēt**.

    ![Atlasot Rediģēt.](../media/tax-feature-support-01.png)

2. Lapā **Nodokļu līdzekļu iestatījums** cilnē **Nodokļu kodi** atlasiet **Pievienot**, lai izveidotu jaunus nodokļu kodus. Šajā piemērā ir izveidoti trīs nodokļu kodi: **NL-Neapliekamais**, **BE-RC-21** un **BE-RC+21**.

    - Kad pārsūtīšanas pasūtījums tiek nosūtīts no noliktavas Nīderlandē, tiek piemērots Nīderlandes PVN atbrīvotā nodokļa kods (**NL-Neapliekamais**).
      
        Izveidojiet nodokļu kodu **NL-Neapliekamais**.
        1. Atlasiet **Pievienot** ievadiet **NL-Neapliekamais** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Pārsledziet **Ir neapliekams** uz **Jā** sadaļā **Vispārējais**.

        ![NL-Neapliekamā nodokļa kods.](../media/tax-feature-support-02.png)

    - Kad pārsūtīšanas pasūtījums tiek saņemts Beļģijas noliktavā, atgriezeniskās maksas mehānisms tiek piemērots, izmantojot **BE-RC-21** un **BE-RC+21** nodokļu kodus.
        
        Izveidojiet nodokļa kodu **BE-RC-21**.      
        1. Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Ievadiet **-21** laukā **Nodokļa likme**.
        6. Pārsledziet **Ir apgrieztā maksa** uz **Jā** sadaļā **Vispārējais**.
        7. Atlasiet **Saglabāt**.

        ![BE-RC-21 nodokļa kods apgrieztām maksām.](../media/tax-feature-support-03.png)
        
        Izveidojiet nodokļa kodu **BE-RC+21**.
        1. Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Ievadiet **21** laukā **Nodokļa likme**.
        6. Atlasiet **Saglabāt**.

        ![BE-RC+21 nodokļa kods apgrieztām maksām.](../media/tax-feature-support-04.png)

3. Nosakiet nodokļa kodu piemērojamību.

    1. Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet kolonnas, kas ir jāizmanto, lai izveidotu piemērojamības tabulu.

        > [!NOTE]
        > Noteikti pievienojiet tabulai kolonnas **Biznesa process** un **Nodokļu virziens**. Abas kolonnas ir būtiskas nodokļu funkcionalitātei pārsūtīšanas pasūtījumos.

    2. Pievienot piemērojamības noteikumus. Laukus **Nodokļu kodi**, **Nodokļu grupa** un **Krājumu nodokļu grupa** nedrīkst atstāt tukšus.
        
        Pievienojiet jaunu kārtulu pārsūtīšanas pasūtījuma kravai.
        1. Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.
        2. Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.
        3. Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.
        4. Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.
        5. Laukā **Nodokļu virziens** atlasiet **Izvade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma nosūtīšanai.
        6. Laukā **Nodokļa kodi** atlasiet **NL-Neapliekamais**.
        7. Laukā **Nodokļu grupa** un **Krājuma nodokļu grupa** ievadiet saistīto nodokļa grupu un krājumu nodokļa grupu, kas ir definēta jūsu Finanšu sistēmā.
        
        Pievienojiet citu kārtulu pārsūtīšanas pasūtījuma saņemšanai.
        1. Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.
        2. Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.
        3. Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.
        4. Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.
        5. Laukā **Nodokļu virziens** atlasiet **Ievade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma saņemšanai.
        6. Laukā **Nodokļu kodi** atlasiet **BE-RC+21** un **BE-RC-21**.
        7. Laukā **Nodokļu grupa** un **Krājuma nodokļu grupa** ievadiet saistīto nodokļa grupu un krājumu nodokļa grupu, kas ir definēta jūsu Finanšu sistēmā.

        ![Lietojamības kārtulas.](../media/image5.png)

4. Pabeidziet un publicējiet jauno nodokļu līdzekļu versiju.

    [![Jaunas versijas statusa maiņa.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Pārsūtīšanas pasūtījumu darījumu Finance iestatīšana

Veiciet šīs darbības, lai iespējotu un iestatītu nodokļus pārsūtīšanas pasūtījumiem.

1. Francija dodieties uz **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Sarakstā atrodiet un atlasiet līdzekli **Nodoklis pārsūtīšanas pasūtījumā** un pēc tam atlasiet **Aktivizēt tūlīt**, lai to ieslēgtu.

    > [!IMPORTANT]
    > Līdzeklis **Nodoklis pārsūtīšanas pasūtījumā** ir pilnībā atkarīgs no nodokļu pakalpojuma. Tādēļ to var ieslēgt tikai pēc nodokļu pakalpojumu instalēšanas.

    ![Līdzeklis Nodoklis pārsūtīšanas pasūtījumā.](../media/image7.png)

3. Iespējojiet nodokļu pakalpojumu un atlasiet biznesa procesu **Krājums**.

    > [!IMPORTANT]
    > Šī darbība ir jāveic katrai Finance juridiskajai personai, kur vēlaties, lai pārsūtīšanas pasūtījumos būtu pieejams nodokļu pakalpojums un funkcionalitāte nodokļiem.

    1. Doties uz **Nodoklis** \> **Iestatījums** \> **Nodokļa konfigurācija** \> **Nodokļu pakalpojuma iestatījumi**.
    2. Laukā **Biznesa process** atlasiet **Krājumi**.

    ![Biznesa procesa lauka iestatīšana.](../media/image8.png)

4. Pārbaudiet, vai ir iestatīts apgrieztās maksas mehānisms. Dodieties uz **Virsgrāmata** \> **Iestatījums** \> **Parametri** un pēc tam cilnē **Apgrieztā maksa** pārbaudiet, vai opcija **Iespējot apgriezto maksu** ir iestatīta uz **Jā**.

    ![Aktivizēt apgrieztās maksas opciju.](../media/image9.png)

5. Pārbaudiet, vai saistītie nodokļu kodi, nodokļu grupas, krājumu nodokļu grupas un PVN reģistrācijas numuri ir iestatīti Finance atbilstoši nodokļu pakalpojuma vadlīnijām.
6. Iestatiet pagaidu tranzīta kontu. Šī darbība ir nepieciešama tikai tad, ja nodoklis, kas tiek lietots pārsūtīšanas pasūtījumam, nav piemērojams ar nodokli neapliekamam vai atgriezenisko maksājumu mehānismam.

    1. Pārejiet uz sadaļu **Nodokļi** \> **Iestatījumi** \> **PVN** \> **Virsgrāmatas grāmatošanas grupas**.
    2. Laukā **Pagaidu tranzīts** atlasiet Virsgrāmatas kontu.

    ![Atlasot pagaidu tranzīta kontu.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Iestatīt pamata krājumus pārsūtīšanas pasūtījuma darījumiem

Veiciet šīs darbības, lai iestatītu pamata krājumus pārsūtīšanas pasūtījumu darījumu iespējošanai.

1. Izveidojiet piegādes un nosūtīšanas vietas noliktavām dažādās valstīs vai reģionos un pievienojiet katras vietas primāro adresi.

    1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Noliktava** \> **Vietas**.
    2. Atlasiet **Jauns**, lai izveidotu vietu, kuru vēlāk piešķirsit noliktavai.
    3. Atkārtojiet 2. darbību visām pārējām vietām, kas ir jāizveido.

    > [!NOTE]
    > Vienai no izveidotajām vietnēm ir jābūt nosauktai **Tranzīts**. Vēlākās šīs procedūras darbībās šī vieta ir jāpiešķir tranzīta noliktavai, lai ar nodokļiem saistītos krājumu dokumentus varētu grāmatot “nosūtīšanas” un “saņemšanas” transakcijās pārsūtīšanas pasūtījumiem. Tranzīta vietas adrese nav atbilstoša nodokļu aprēķinam. Tādēļ to var atstāt tukšu.

    ![Vietu iestatīšana.](../media/image11.png)

2. Izveidot piegādes, tranzīta un nosūtīšanas noliktavas. Jebkura adreses informācija, kas tiek uzturēta noliktavā, nodokļu aprēķināšanas laikā ignorēs vietas adresi.

    1. Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Noliktava** \> **Noliktavas**.
    2. Atlasiet **Jauns**, lai izveidotu vietu un piešķir to atbilstošajai vietai.
    3. Atkārtojiet 2. darbību, lai izveidotu noliktavu katrai vietai pēc vajadzības.

    ![Noliktavu iestatīšana.](../media/image12.png)

    > [!NOTE]
    > Piegāde no noliktavas pārsūtīšanas pasūtījuma darījumiem laukā **Tranzīta noliktava** ir jāatlasa tranzīta noliktava.
    >
    > ![Tranzīta noliktavas atlasīšana.](../media/image13.png)

3. Pārbaudiet, vai krājumu grāmatošanas konfigurācija ir iestatīta pārsūtīšanas pasūtījumu darījumiem.

    1. Doties uz **Krājumu vadība** \> **Iestatīšana** \> **Grāmatojums** \> **Grāmatošana**.
    2. Cilnē **Krājumi** pārbaudiet, vai Virsgrāmatas konts ir iestatīts gan **Krājumu izejas plūsmas**, gan **Krājumu ieejas plūsmas** grāmatošanai.

        ![Krājumu izejas un krājumu ieejas plūsmas grāmatošanas iestatīšana.](../media/image14.png)

    3. Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību maksājumu** grāmatošanai.

        ![Starpvienību maksājumu grāmatošanas iestatīšana.](../media/image15.png)

    4. Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību ieņēmumi** grāmatošanai.

        ![Starpvienību ieņēmumu grāmatošanas iestatīšana.](../media/image16.png)
