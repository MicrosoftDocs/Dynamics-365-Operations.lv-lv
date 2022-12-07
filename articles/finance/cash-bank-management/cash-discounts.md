---
title: Termiņatlaides
description: Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi.  Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b75637bfb38c13591223ff11be36d958b3972d4f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804141"
---
# <a name="cash-discounts"></a>Termiņatlaides

[!include [banner](../includes/banner.md)]

Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi. Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā. 

## <a name="cash-discounts"></a>Termiņatlaides

Termiņatlaides debitoriem vai kreditoriem var izveidot termiņatlaižu **lapā**. Izmantojot lauku Nākamais atlaižu **kods**, var arī definēt termiņatlaižu sērijas, kas seko cita citai, kad beidzas termiņatlaides iepriekšējie datumi. Papildinformāciju skatiet tālāk šī raksta sadaļā "Piemērs: termiņatlaižu sērija". Ja rēķins, kredīta transakcija (maksājums vai kredīta nota) vai tie abi tiek ievadīti valūtā, kas nav juridiskās personas uzskaites valūta, tad termiņatlaide tiek aprēķināta, izmantojot valūtas maiņas kursu, kurš ir balstīts uz maksājuma vai kredīta notas datumu. Ja rēķins un kredīta dokuments tiek ievadīti dažādās juridiskajās personās un ja uzskaites valūtas šīm juridiskajām personām atšķiras, tad valūtas maiņas kurss tiek ņemts no rēķina juridiskās personas attiecīgā kredīta dokumenta datumā. Papildinformāciju skatiet tālāk šī raksta sadaļā "Piemērs: termiņatlaižu maiņas kursi".

## <a name="defaulting-order-of-cash-discount-main-account"></a>Termiņatlaides galvenā konta pasūtījuma noklusējuma secība

Ja rēķins ir segts laikā, lai saņemtu termiņatlaidi, šī termiņatlaide tiek automātiski grāmatota uz termiņatlaides galveno kontu atbilstoši šādai noklusējuma prioritātei:
1.  Galvenais konts, kas norādīts laukā **Alternatīvās termiņatlaides**  **konts** lapā Debitoru atvērto darbību kārtošanu vai lapā **Nosegt atvērtās** darbības.
2.  Galvenais konts, kas norādīts **Klienta**  **termiņatlaides** laukā vai Virsgrāmatas grāmatošanas grupas laukā Kreditora termiņatlaide, kas ir piešķirts rēķina PVN kodam. Iestatiet Virsgrāmatas grāmatošanas grupas lapā **Virsgrāmatas grāmatošanas grupas** un piešķiriet tās PVN kodiem **PVN kodu** lapā.
3.  Galvenais **grāmatošanas**  **·**  **konts** termiņatlaižu lapā, laukā Galvenais konts debitora atlaidēm vai galvenais konts kreditoru atlaižu laukam termiņatlaides kodam, kas ir segtā rēķinā.
4.  Galvenais konts termiņatlaidēm, kā norādīts lapā **Automātisko darbību** konti.

## <a name="example-series-of-cash-discounts"></a>Piemērs. Termiņatlaižu sērijas
Iestatiet trīs termiņatlaižu kodus šādā veidā:
-   Kods 5D10% – 10% termiņatlaide, ja summa tiek samaksāta 5 dienu laikā.
-   Kods 10D5% – 5% termiņatlaide, ja summa tiek samaksāta 10 dienu laikā.
-   Kods 14D2% – 2% termiņatlaide, ja summa tiek samaksāta 14 dienu laikā.

Laukā **Nākamais atlaides** kods:
-   Kodam 5D10% atlasiet 10D5%
-   Kodam 10D5% atlasiet 14D2%.
-   Kodam 14D2% lauku Nākamais atlaižu kods atstājiet tukšu.

Maksājuma datumam pārsniedzot iepriekšējo rēķinā norādītās termiņatlaides datumu, šīs trīs termiņatlaides seko cita citai. Apmaksājot rēķinu, tiek piešķirta tikai viena termiņatlaide, pamatojoties uz to, kurš termiņatlaides datums šajā termiņatlaižu secībā tiek ievērots.

## <a name="example-exchange-rates-for-cash-discounts"></a>Piemērs. Valūtas maiņas kursi termiņatlaidēm
Jūsu juridiskās personas uzskaites valūta ir EUR, un šāds valūtas maiņas kurss ir norādīts attiecībā uz USD:
-   1. februāris = 110
-   1. marts = 80

Rēķins par 1000 USD ar termiņatlaides nosacījumiem 20D2% tiek grāmatots 15. februārī. Rēķina summa uzskaites valūtā ir 1100 EUR. Maksājums par 980 USD šim rēķinam tiek nosegts 1. martā. Termiņatlaides summa ir 20 USD. Maksājuma summa uzskaites valūtā ir 784 EUR. Termiņatlaides uzskaites valūtas summa tiek aprēķināta, izmantojot valūtas maiņas kursu no 1. marta: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Ja opcija **Aprēķināt termiņatlaides daļējiem maksājumiem ir atlasīta lapās**  **·**  **Debitoru** parādi vai Parādi kreditoriem parametri, tiek izmantots valūtas maiņas kurss, kas ir spēkā attiecībā uz katra daļējā maksājuma datumu. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
