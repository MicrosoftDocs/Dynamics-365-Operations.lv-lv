---
title: Pasūtījumu uzmeklēšanas modulis
description: Šajā rakstā ir apskatīts pasūtījumu uzmeklēšanas modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a891de4a1da6641a02b8316d16ac2e9a8180fac1
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734256"
---
# <a name="order-lookup-module"></a>Pasūtījumu uzmeklēšanas modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīts pasūtījumu uzmeklēšanas modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.

Pasūtījumu uzmeklēšanas modulis nodrošina veidlapu, kuru klienti var lietot, lai uzmeklētu pasūtījumus, kurus tie veikuši e-komercijas vietnē. To izmanto kā daļu no līdzekļa [Viesu izrakstīšanās pasūtījuma uzmeklēšana](order-lookup-guest.md). Pasūtījuma uzmeklēšanas moduli var izmantot, lai uzmeklētu pasūtījumus, kuri iesniegti ar e-komercijas vietni, mazumtirdzniecības pārdošanas punktu (POS) vai zvanu centru. Veidlapa var izgūt pasūtījumus, kurus iesnieguši gan viesi, gan reģistrēti lietotāji.

Šajā attēlā parādīts piemērs veidlapai, kura tiek atveidota pasūtījuma uzmeklēšanas modulī. Klientiem aizpildot veidlapu un atlasot **Atrast pasūtījumu**, viņus pārvirza uz pasūtījuma informācijas lapu.

![Pasūtījuma uzmeklēšanas moduļa veidlapa lapā.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Pasūtījuma uzmeklēšanas moduļa rekvizīti

| Rekvizīta nosaukums     | Vērtība     | Apraksts |
|-------------------|-----------|-------------|
| Virsraksts           | Teksts      | Galvene, kas tiek rādīta veidlapas augšpusē (piemēram, "Atrast pasūtījumu"). |
| Bagātināts teksts         | Bagātināts teksts | Neobligāts skaidrojošais teksts, kas tiek rādīts zem virsraksta. |
| Pasūtījuma statusa veids | Uzskaitījums      | <p>Atlasiet informācijas veidu, kuru veidlapa pieprasīs no klienta līdztekus pasūtījuma apstiprinājuma ID. Pašlaik tiek atbalstītas šādas vērtības:</p><ul><li><b>E-pasts</b> — Veidlapa ietvers lauku, kurā klienti var ievadīt e-pasta adresi, kura tika izmantota, veicot pasūtījumu.</li><li><b>Nav</b> — Veidlapa nepieprasīs nekādu citu informāciju, izņemot pasūtījuma apstiprināšanas ID.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Pasūtījuma uzmeklēšanas moduļa pievienošana lapai

Pasūtījumu uzmeklēšanas moduli var pievienot jebkuras jūsu e-komercijas vietnes lapas pamattekstam. Ja vēlaties lietot pasūtījuma uzmeklēšanas moduli, lai iespējotu viesu izrakstīšanās pasūtījuma uzmeklēšanu, pārliecinieties, ka pievienojat to lapai, kurai nav vajadzīga lietotāja pieteikšanās. Lai atrastu lapas iestatījumu **Vajadzīga pieteikšanās** Commerce vietnes veidotāja koka skatā, atlasiet logu **Noklusējuma lapa (obligāti)** un paskatieties uz labās rūts apakšdaļu.


> [!NOTE]
> Lai iespējotu pasūtījuma uzmeklēšanas līdzekli, nodrošiniet, lai **licences konfigurācijas atslēgās** atslēga Piedāvājums **būtu** > **iespējota**.
>
> ![Jāaktivizē piedāvājumu licences atslēgas konfigurācija.](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Papildu resursi

[Viesu izrakstīšanās pasūtījuma uzmeklēšanas iespējošana](order-lookup-guest.md)

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
