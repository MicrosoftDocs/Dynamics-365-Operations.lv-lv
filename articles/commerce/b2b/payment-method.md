---
title: Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs
description: Šajā tēmā ir aprakstīts, kā konfigurēt klienta konta maksājuma metodi bizness-biznesam (B2B) e-komercijas vietnēs.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 628f3b3b2d86154190dfdcc82b8b391c2facce103f607519514c65b5fba26653
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738057"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt klienta konta maksājuma metodi bizness-biznesam (B2B) e-komercijas vietnēs.

Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem e-komercijas kanālā. Sistēmas iestatīšanas laikā programmā Microsoft Dynamics 365 Commerce ir jākonfigurē katrs maksājuma veids, ko pieņem mazumtirgotājs. Klienta konta (vai “uz kredīta”) maksājuma metodei ir jābūt atbalsītai B2B e-komercijas vietnēs. 

## <a name="prerequisites"></a>Priekšnosacījumi

1. Pievienojiet klienta konta maksāšanas metodi komponentam Commerce Headquarters.
2. Saistiet klienta konta maksāšanas metodi ar e-komercijas kanālu.
3. Pārliecinieties, vai klientam ir iespējots **Atļaut uz kredīta**, komponentā Commerce Headquarters atverot **Retail un Commerce \> Klienti \> Visi klienti \> Maksājuma noklusējuma informācija**. Kā arī pārliecinieties, vai **Kredīta limita** parametri ir iestatīti atbilstoši klientam, atverot **Retail un Commerce \> Klienti \> Visi klienti \> Kredīts un iekasēšana** komponentā Commerce Headquarters. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Klienta konta maksājuma metodes iespējošana Commerce vietnes veidotājā 

Lai iespējotu klienta konta maksājuma metodi Commerce vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Iestatiet rekvizītu **Iespējot klienta konta maksājumus** uz **Iespējot B2B klientiem**. 
1. Atlasiet **Saglabāt un publicēt**.

> [!NOTE]
> Jaunās vietnes iestatījumi stājas spēkā tikai pēc faila app.settings.json atjaunināšanas. Papildinformāciju skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Klienta konta maksājuma metodes iespējošana B2B e-komercijas vietnes norēķināšanās lapā

Lai iespējotu klienta konta maksājuma metodes B2B e-komercijas vietnes norēķināšanās lapā, veiciet tālāk norādītās darbības.

1. Commerce vietnes veidotājā atrodiet un rediģējiet norēķināšanās lapu vai fragmentu, kas satur B2B e-komercijas vietnes norēķināšanās moduli.
1. Slotā **Norēķināšanās sekcijas konteiners** atlasiet **Pievienot moduli** un pēc tam pievienojiet **Klienta konta maksājuma** moduli.
1. Novietojiet **Klienta konta maksājumu** moduli, atlasot daudzpunktes (**...**), un pēc nepieciešamības atlasot **Pārvietot uz augšu** vai **Pārvietot uz leju**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Klienta konta maksājuma metodes iespējošanas un publicēšanas apstiprinājums

Lai apstiprinātu, vai klienta konta maksājuma metode ir iespējota, veiciet tālāk norādītās darbības.

1. Pierakstieties e-komercijas vietnē.
1. Pievienojiet grozam preci.
1. Doties uz norēķināšanās lapu. Jums vajadzētu redzēt jauno **Klienta konta** maksājuma metodi.

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām](org-model.md)

[Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas vietnēs](manage-b2b-users.md)

[Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs](quantity-limits.md)

[SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]