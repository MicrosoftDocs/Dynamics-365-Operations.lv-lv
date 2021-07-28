---
title: Nodokļu komponentu iestatīšana TDS nodokļu veidam
description: Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa komponentus No kopējās ienākumu summas atskaitītā nodokļa (TDS) veidam. Dokumentā ir arī izskaidrots, kā definēt sliekšņa ierobežojumu, kas tiek izmantots katra TDS komponenta TDS aprēķinam.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 70e57a928ecd3f5d10ebd3d0fc3f52870d40fcd9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358174"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Nodokļu komponentu iestatīšana TDS nodokļu veidam

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa komponentus No kopējās ienākumu summas atskaitītā nodokļa (TDS) veidam. TDS komponenti ir TDS, piemaksas, PE-Cess un SHE Cess. Šajā tēmā ir arī izskaidrots, kā definēt slieksni, kas tiek izmantots katra TDS komponenta TDS aprēķinam. Papildus var definēt izņēmumu slieksni, kas tiek izmantots, lai aprēķinātu TDS katram TDS komponentam.

Lai iestatītu TDS komponentus, rīkojieties šādi.

1. Atveriet **Nodoklis \> Iestatīšana \> Ieturētais nodoklis \> Ieturētā nodokļa komponenti**.

    [![Ieturētā nodokļa komponentu lapa.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Laukā **Nodokļu tips** atlasiet **TDS**, lai iestatītu ieturētā nodokļa komponentus TDS nodokļa tipam.
3. Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.
4. Laukā **Ieturētā nodokļa komponents** ievadiet TDS komponenta nosaukumu.
5. Laukā **Ieturētā nodokļa komponentu grupa** atlasiet TDS ieturētā nodokļa komponentu grupu, lai pievienotu TDS komponentu.
6. Kopsavilkuma cilnē **Vispārīgi** laukā **Apraksts** ievadiet TDS komponenta aprakstu.
7. Darbību rūtī atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**, tādējādi varat definēt slieksni, kas tiek izmantots TDS komponenta TDS aprēķinam.
8. Lai definētu periodu, uz kuru attiecas slieksnis, lietojiet laukus **sākuma datums** un **Beigu datums**.
9. Kopsavilkuma cilnē **Vispārīgi**, laukā **Slieksnis** ievadiet sliekšņa summu, kas tiek izmantota TDS komponenta TDS aprēķinam. Nodokli atskaita no kopējās ienākumu summas tikai tad, ja kopējā rēķina summa pārsniedz slieksni.

    Piemēram, ja sliekšņa summa ir 10 000, TDS tiek aprēķināts pēc tam, kad kopējā rēķina summa pārsniedz 10 000 (citiem vārdiem, ja tā ir 10 001 vai lielāka).

10. Laukā **Izņēmuma slieksnis** ievadiet izņēmuma sliekšņa summu, kas tiek izmantota TDS komponenta TDS aprēķinam. Nodokli rēķina rindā atskaita no kopējās ienākumu summas tikai tad, ja summa pārsniedz izņēmuma slieksni.

    Piemēram, ja izņēmuma sliekšņa summa ir 5000, TDS tiek aprēķināts uz noteiktu rēķina rindu, ja rēķina rindas summa pārsniedz 5000 (citiem vārdiem, ja tas ir 5001 vai vairāk).

    [![Sliekšņa lapa.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Izņēmuma sliekšņa summai ir jābūt mazākai par sliekšņa summu vai vienādai ar to.
    >
    > Nodoklis tiek atskaitīts darījumam, ja darījuma summa pārsniedz izņēmuma slieksni, pat ja kopējā rēķina summa nešķērso sliekšņa robežas, kas ir norādītas laukā **Slieksnis**.

11. Aizveriet lapu **Slieksnis**, lai atgrieztos uz lapu **Ieturētā nodokļa komponenti**.
12. Darbību rūtī atlasiet **Kopēt**, lai atvērtu dialoglodziņu **Kopēt ieturētā nodokļa komponentus** tādējādi varat kopēt TDS komponentus, kas tika iestatīti vienam TDS komponentu grupai citā TDS komponentu grupā.
13. Laukā **No** atlasiet TDS komponentu grupu, no kā kopēt TDS komponentus. Laukā **Uz** atlasiet ieturētā nodokļa komponentu grupu, uz kuru kopēt TDS komponentus.

    > [!NOTE]
    > Kopējie TDS komponenti, kas ir pievienoti abām TDS komponentu grupām, netiek nokopēti.

14. Atlasiet **Labi**, lai kopētu un izveidotu TDS komponentus citai TDS komponentu grupai **Ieturētā nodokļa komponentu** lapā.

    [![Kopēt ieturētā nodokļa komponentu dialoglodziņu.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Aizvērt lapu.
