---
title: Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem
description: Šajā tēmā skaidrots jaunās nodokļu funkcionalitātes atbalsts pārsūtīšanas pasūtījumiem, izmantojot nodokļu aprēķināšanas pakalpojumu.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d95ea6795dc5777bfd37f8fbb3ebc47f2db337a0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689219"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem

[!include [banner](../../includes/banner.md)]

Šajā tēmā sniegta informācija par nodokļu aprēķināšanu un integrācijas grāmatošanu pārsūtīšanas pasūtījumos. Šī funkcionalitāte ļauj jums iestatīt nodokļu aprēķinu un grāmatošanu pārsūtīšanas pasūtījumos krājumu pārsūtīšanai. Saskaņā ar Eiropas Savienības (ES) pievienotās vērtības nodokļa (PVN) noteikumiem krājumu pārsūtīšana tiek uzskatīta par piegādi Kopienas iekšienē un iegādi Kopienas iekšienē.

Lai konfigurētu un lietotu šo funkcionalitāti, ir jāveic trīs galvenās darbības:

1. **RCS iestatījumi**: regulēšanas konfigurācijas pakalpojumā iestatiet nodokļu līdzekli, nodokļu kodus un nodokļu kodu piemērojamību nodokļa koda noteikšanai pārsūtīšanas pasūtījumos.
2. **Dynamics 365 finanšu iestatīšana:** **finanšu** iestatījumā iespējojiet līdzekli Nodoklis pārsūtīšanas pasūtījumā, iestatiet krājumu nodokļu aprēķināšanas pakalpojumu parametrus un iestatiet galvenos nodokļu parametrus.
3. **Krājumu iestatīšana**: iestatiet krājumu konfigurāciju pārsūtīšanas pasūtījumu darījumiem.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Nodokļu un pārsūtīšanas pasūtījumu darījumu RCS iestatīšana

Veiciet šīs darbības, lai iestatītu nodokli, kas ir iesaistīts pārsūtīšanas pasūtījumā. Šeit parādītajā piemērā pārsūtīšanas pasūtījums ir no Nīderlandes uz Beļģiju.

1. Lapā **Nodokļu līdzekļi**, cilnē **Versijas** atlasiet melnraksta līdzekļa versiju un pēc tam atlasiet **Rediģēt**.

2. Lapā **Nodokļu līdzekļu iestatījums** cilnē **Nodokļu kodi** atlasiet **Pievienot**, lai izveidotu jaunus nodokļu kodus. Šajā piemērā ir izveidoti trīs nodokļu kodi: **NL-Neapliekamais**, **BE-RC-21** un **BE-RC+21**.

    - Kad pārsūtīšanas pasūtījums tiek nosūtīts no noliktavas Nīderlandē, tiek piemērots Nīderlandes PVN atbrīvotā nodokļa kods (**NL-Neapliekamais**).
      
        Izveidojiet nodokļu kodu **NL-Neapliekamais**.
        1. Atlasiet **Pievienot** ievadiet **NL-Neapliekamais** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Iestatiet **Ir neapliekams** uz **Jā** sadaļā **Vispārējais**.
        6. Laukā **Neapliekamais kods** ievadiet **EK**.

    - Kad pārsūtīšanas pasūtījums tiek saņemts Beļģijas noliktavā, atgriezeniskās maksas mehānisms tiek piemērots, izmantojot **BE-RC-21** un **BE-RC+21** nodokļu kodus.
        
        Izveidojiet nodokļa kodu **BE-RC-21**.      
        1. Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Ievadiet **-21** laukā **Nodokļa likme**.
        6. Iestatiet **Ir apgrieztā maksa** uz **Jā** sadaļā **Vispārējais**.
        7. Atlasiet **Saglabāt**.
        
        Izveidojiet nodokļa kodu **BE-RC+21**.
        1. Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.
        2. Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.
        3. Atlasiet **Saglabāt**.
        4. Atlasiet **Pievienot** tabulā **Likme**.
        5. Ievadiet **21** laukā **Nodokļa likme**.
        6. Atlasiet **Saglabāt**.

3. Definējiet nodokļu grupu.
    1. Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet rindas lauku **Nodokļu grupa**.
    2. Atlasiet **->** to un pēc tam atlasiet **Labi**.
    3. Atlasiet **Pievienot**, lai pievienotu nodokļu grupu.
    4. Kolonnā **Nodokļu grupa** ievadiet **AR-EU** un pēc tam atlasiet **NL-Neapliekamais** nodokļa kodu.
    5. Atlasiet **Pievienot**, lai pievienotu nodokļu grupu.
    6. Kolonnā **Nodokļu grupa** ievadiet **RC-PVN** un pēc tam atlasiet **BE-RC-21** un **BE-RC+21** nodokļa kodus.
4. Definējiet Krājumu nodokļu grupu.
    1. Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet rindas lauku **Krājumu Nodokļu grupa**.
    2. Atlasiet **->** to un pēc tam atlasiet **Labi**.
    3. Atlasiet **Pievienot**, lai pievienotu krājumu nodokļu grupu.
    4. Kolonnā **Krājumu nodokļu grupa** ievadiet **PILNS**. Atlasiet nodokļu kodus **BE-RC-21**, **BE-RC+21** un **NL-Exempt**.
5. Nosakiet nodokļu grupas piemērojamību.

    1. Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet kolonnas, kas ir jāizmanto, lai izveidotu piemērojamības tabulu.

        > [!NOTE]
        > Noteikti pievienojiet tabulai kolonnas **Biznesa process** un **Nodokļu virziens**. Abas kolonnas ir būtiskas nodokļu funkcionalitātei pārsūtīšanas pasūtījumos.

    2. Pievienot piemērojamības noteikumus. Neatstājiet tukšu lauku **Nodokļu grupa**.
        
        Pievienojiet jaunu kārtulu pārsūtīšanas pasūtījuma kravai.
        1. Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.
        2. Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.
        3. Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.
        4. Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.
        5. Laukā **Nodokļu virziens** atlasiet **Izvade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma nosūtīšanai.
        6. Laukā **Nodokļu grupa** atlasiet **AR-EU**.
        
        Pievienojiet citu kārtulu pārsūtīšanas pasūtījuma saņemšanai.
        
        1. Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.
        2. Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.
        3. Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.
        4. Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.
        5. Laukā **Nodokļu virziens** atlasiet **Ievade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma saņemšanai.
        6. Laukā **Nodokļu grupa** atlasiet **RC-PVN**.

6. Nosakiet krājumu nodokļu grupas piemērojamību.

    1. Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet kolonnas, kas ir jāizmanto, lai izveidotu piemērojamības tabulu.
    2. Pievienot piemērojamības noteikumus. Neatstājiet tukšu lauku **Krājumu Nodokļu grupa**.
        
        Pievienojiet jaunu noteikumu par pārsūtīšanas pasūtījuma nosūtīšanu un saņemšanu.
        1. Lapā **Piemērošanas noteikumi** atlasiet **Pievienot**.
        2. Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.
        3. Laukā **Krājumu Nodokļu grupa** atlasiet **PILNS**.
7. Pabeidziet un publicējiet jauno nodokļu līdzekļu versiju.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Pārsūtīšanas pasūtījumu darījumu Finance iestatīšana

Veiciet šīs darbības, lai iespējotu un iestatītu nodokļus pārsūtīšanas pasūtījumiem.

1. Pakalpojumā Finance dodieties uz **Darbvietas** > **Līdzekļu pārvaldība**.
2. Sarakstā atrodiet un atlasiet līdzekli **Nodoklis pārsūtīšanas pasūtījumā** un pēc tam atlasiet **Aktivizēt tūlīt**, lai to ieslēgtu.

    > [!IMPORTANT]
    > Līdzeklis **Nodoklis pārsūtīšanas pasūtījumā** ir pilnībā atkarīgs no nodokļu aprēķina pakalpojuma. Tādēļ to var ieslēgt tikai pēc nodokļu aprēķina pakalpojumu instalēšanas.

    ![Līdzeklis Nodoklis pārsūtīšanas pasūtījumā.](../media/image7.png)

3. Iespējojiet nodokļu aprēķina pakalpojumu un atlasiet biznesa procesu **Krājums**.

    > [!IMPORTANT]
    > Šī darbība ir jāveic katrai Finance juridiskajai personai, kur vēlaties, lai pārsūtīšanas pasūtījumos būtu pieejams nodokļu aprēķina pakalpojums un funkcionalitāte nodokļiem.

    1. Dodieties uz **Nodoklis** > **Uzstādīšana** > **Nodokļu konfigurācija** > **Nodokļu aprēķina parametri**.
    2. Laukā **Biznesa process** atlasiet **Krājumi**.

4. Pārbaudiet, vai ir iestatīts apgrieztās maksas mehānisms. Dodieties uz **Virsgrāmata** \> **Iestatījums** \> **Parametri** un pēc tam cilnē **Apgrieztā maksa** pārbaudiet, vai opcija **Iespējot apgriezto maksu** ir iestatīta uz **Jā**.

    ![Aktivizēt apgrieztās maksas opciju.](../media/image9.png)

5. Pārbaudiet, vai saistītie nodokļu kodi, nodokļu grupas, krājumu nodokļu grupas un PVN reģistrācijas numuri ir iestatīti Finance atbilstoši nodokļu aprēķina pakalpojuma vadlīnijām.
6. Iestatiet pagaidu tranzīta kontu. Šī darbība ir nepieciešama tikai tad, ja nodoklis, kas tiek lietots pārsūtīšanas pasūtījumam, nav piemērojams ar nodokli neapliekamam vai atgriezenisko maksājumu mehānismam.

    1. Pārejiet uz **Nodokļi** > **Iestatījumi** > **PVN** > **Virsgrāmatas grāmatošanas grupas**.
    2. Laukā **Pagaidu tranzīts** atlasiet Virsgrāmatas kontu.

       ![Atlasot pagaidu tranzīta kontu.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Iestatīt pamata krājumus pārsūtīšanas pasūtījuma darījumiem

Veiciet šīs darbības, lai iestatītu pamata krājumus pārsūtīšanas pasūtījumu darījumu iespējošanai.

1. Izveidojiet piegādes un nosūtīšanas vietas noliktavām dažādās valstīs vai reģionos un pievienojiet katras vietas primāro adresi.

    1. Atveriet **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Vietnes**.
    2. Atlasiet **Jauns**, lai izveidotu vietu, kuru vēlāk piešķirsit noliktavai.
    3. Atkārtojiet 2. darbību visām pārējām vietām, kas ir jāizveido.

    > [!NOTE]
    > Vienai no izveidotajām vietnēm ir jābūt nosauktai **Tranzīts**. Vēlākās šīs procedūras darbībās šī vieta ir jāpiešķir tranzīta noliktavai, lai ar nodokļiem saistītos krājumu dokumentus varētu grāmatot “nosūtīšanas” un “saņemšanas” transakcijās pārsūtīšanas pasūtījumiem. Tranzīta vietas adrese nav atbilstoša nodokļu aprēķinam. Tādēļ to var atstāt tukšu.

    ![Vietu iestatīšana.](../media/image11.png)

2. Izveidot piegādes, tranzīta un nosūtīšanas noliktavas. Jebkura adreses informācija, kas tiek uzturēta noliktavā, nodokļu aprēķināšanas laikā ignorēs vietas adresi.

    1. Dodieties uz **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Noliktavas**.
    2. Atlasiet **Jauns**, lai izveidotu vietu un piešķir to atbilstošajai vietai.
    3. Atkārtojiet 2. darbību, lai izveidotu noliktavu katrai vietai pēc vajadzības.

       ![Noliktavu iestatīšana.](../media/image12.png)

    > [!NOTE]
    > Piegāde no noliktavas pārsūtīšanas pasūtījuma darījumiem laukā **Tranzīta noliktava** ir jāatlasa tranzīta noliktava.
    >
    > ![Tranzīta noliktavas atlasīšana.](../media/image13.png)

3. Pārbaudiet, vai krājumu grāmatošanas konfigurācija ir iestatīta pārsūtīšanas pasūtījumu darījumiem.

    1. Doties uz **Krājumu vadība** > **Iestatīšana** > **Grāmatojums** > **Grāmatošana**.
    2. Cilnē **Krājumi** pārbaudiet, vai Virsgrāmatas konts ir iestatīts gan **Krājumu izejas plūsmas**, gan **Krājumu ieejas plūsmas** grāmatošanai.

        ![Krājumu izejas un krājumu ieejas plūsmas grāmatošanas iestatīšana.](../media/image14.png)

    3. Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību maksājumu** grāmatošanai.

        ![Starpvienību maksājumu grāmatošanas iestatīšana.](../media/image15.png)

    4. Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību ieņēmumi** grāmatošanai.

        ![Starpvienību ieņēmumu grāmatošanas iestatīšana.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
