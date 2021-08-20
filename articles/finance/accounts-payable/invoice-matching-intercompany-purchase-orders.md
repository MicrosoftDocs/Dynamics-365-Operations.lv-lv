---
title: Rēķinu salīdzināšana un starpuzņēmumu pirkšanas pasūtījumi
description: Pērkošo juridisko personu, kas ir iesaistīta starpuzņēmumu tirdzniecības transakcijā, var iestatīt kreditoru rēķinu salīdzināšanas lietošanai. Tādā gadījumā, lai varētu grāmatot starpuzņēmumu kreditoru rēķinus, ir jābūt ievērotām gan starpuzņēmumu tirdzniecības, gan kreditoru rēķinu salīdzināšanas grāmatošanas prasībām.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: roschlom
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afa7021278d5dc8ba307ae1cf72504d08660f7ce34dea86ce2e8ca2a709366b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737386"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Rēķinu salīdzināšana un starpuzņēmumu pirkšanas pasūtījumi

[!include [banner](../includes/banner.md)]

Pērkošo juridisko personu, kas ir iesaistīta starpuzņēmumu tirdzniecības transakcijā, var iestatīt kreditoru rēķinu salīdzināšanas lietošanai. Ja lauks **Grāmatot rēķinu ar neatbilstībām** veidlapā **Kreditoru parametri** ir iestatīts uz **Pieprasīt apstiprinājumu**, tiks veikta rēķinu salīdzināšanas validācija. Tādā gadījumā, lai varētu grāmatot starpuzņēmumu kreditoru rēķinus, ir jābūt ievērotām gan starpuzņēmumu tirdzniecības, gan kreditoru rēķinu salīdzināšanas grāmatošanas prasībām.

Šīs tēmas piemēros tiek izmantoti šādi starpuzņēmumu tirdzniecības iestatījumi:
-   Pirkuma fabrika ir juridiskā persona, kas veic pirkumu.
-   Pārdošanas fabrika ir juridiskā persona, kas veic pārdošanu.
-   Klients 4020 eksistē Pārdošanas Fabrikā.
-   Kreditors 3024 eksistē Pirkuma Fabrikā.
-   Uzņēmumā Pirkuma fabrika ir norādīta starpuzņēmumu informācija par kreditoru 3024. Uzņēmums Pārdošanas fabrika ir norādīts kā debitora uzņēmums, un debitors 4020 ir norādīts kā debitora konts, kas atbilst juridiskajai personai Pirkuma fabrika.
-   Uzņēmumā Pārdošanas fabrika ir norādīta starpuzņēmumu informācija par debitoru 4020. Uzņēmums Pirkšanas fabrika ir norādīts kā kreditora uzņēmums, un kreditors 3024 ir norādīts kā kreditora konts, kas atbilst juridiskajai personai Pārdošanas fabrika.

Piemēros Pirkuma fabrikai tiek lietoti šādi kreditoru rēķinu salīdzināšanas iestatījumi:
-   Lapā Kreditoru moduļa parametri ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes.
-   Lapā Kreditoru moduļa parametri lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu.
-   Cenas tolerance procentos juridiskajai personai ir 2 procenti.

## <a name="example-price-matching-and-intercompany-trade"></a>Piemērs. Cenu salīdzināšana un starpuzņēmumu tirdzniecība
Starpuzņēmumu kreditoru rēķina un starpuzņēmumu debitora rēķina neto summām ir jābūt vienādām. Šī nosacījuma prioritāte ir augstāka par jebkuriem piemērojamajiem rēķinu salīdzināšanas apstiprinājumiem vai cenu tolerances procentiem. Piemēram, izpildiet tālāk aprakstītās darbības.
1.  Uzņēmumā Pirkuma fabrika izveidojiet pārdošanas pasūtījumu SO888 debitoram 4020. Pirkuma fabrikā tiek automātiski izveidots starpuzņēmumu pirkšanas pasūtījums ICPO222 kreditoram 3024, un Pārdošanas fabrikā tiek automātiski izveidots pārdošanas pasūtījums ICSO888.
2.  Pārdošanas fabrikā reģistrējiet, ka krājumi ir saņemti, un iegrāmatojiet pavadzīmi. ICSO888 statuss nomainās uz Piegādāts. ICPO222 statuss nomainās uz Saņemts.
3.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO888. Vienības cena ir 0,45 un tiek atjauninātas 100 vienības.
4.  Pirkuma fabrikā izveidojiet rēķins attiecībā uz ICPO222. Neto cenu no 45,00 jūs nejauši maināt uz 54,00. Tiek parādīta ikona, lai norādītu, ka cena pārsniedz atļauto 2 procentu cenas toleranci.
5.  Lapā Rēķinu salīdzināšanas detalizēta informācija atlasiet opciju, lai apstiprinātu grāmatojumu ar salīdzināšanas neatbilstībām. Lapā Kreditora rēķins noklikšķiniet uz Labi. Ja kreditora rēķins nebūtu starpuzņēmumu kreditora rēķins, grāmatošana būtu veiksmīga. Taču, tā kā jūs strādājat ar starpuzņēmumu kreditoru rēķinu, grāmatošana ir nesekmīga. Starpuzņēmumu tirdzniecībai starpuzņēmumu pārdošanas pasūtījuma rēķinu kopsummai ir jābūt vienādai ar rēķinu kopsummām atbilstošajā starpuzņēmumu pirkšanas pasūtījumā. Lai atrisinātu šo problēmu, labojiet neto cenu rēķinā, šo neto cenu mainot atpakaļ uz noklusējuma summu 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Piemērs. Daudzuma salīdzināšana ar starpuzņēmumu tirdzniecību
Starpuzņēmumu pirkšanas pasūtījuma un starpuzņēmumu pārdošanas pasūtījuma daudzumiem ir jābūt vienādiem. Šīs prasības prioritāte ir augstāka par jebkuriem piemērojamajiem rēķinu salīdzināšanas apstiprinājumiem. Šajā piemērā tiek izmantoti šādi papildu iestatījumi attiecībā uz starpuzņēmumu tirdzniecību:
-   Pirkuma fabrikā pirkšanas pasūtījuma darbības politika attiecībā uz kreditoru 3024 ir iestatīta tā, lai automātiski grāmatotu gan sākotnējo debitora rēķinu, gan starpuzņēmumu kreditoru rēķinu.

Šajā piemērā tiek izmantoti šādi papildu iestatījumi attiecībā uz kreditoru rēķinu salīdzināšanu Pirkuma fabrikai:
-   Lapā Krājumu modeļu grupas modeļa grupai, kuru izmanto krājums B-R14, ir atlasīta opcija Saņemšanas prasības.
-   Rīcībā esošais krājuma B-R14 daudzums ir 0 (nulle).

Piemēram, izpildiet tālāk aprakstītās darbības.
1.  Uzņēmumā Pirkuma fabrika izveidojiet pārdošanas pasūtījumu SO999 debitoram 4020. Pasūtījumā ir viena krājuma rinda: 100 baterijas (krājums B-R14) ar vienas vienības cenu 1,00. Pirkuma fabrikā tiek automātiski izveidots starpuzņēmumu pirkšanas pasūtījums ICPO333 kreditoram 3024, un Pārdošanas fabrikā tiek automātiski izveidots pārdošanas pasūtījums ICSO999.
2.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO999. Grāmatošana ir nesekmīga, jo šīs preces krājumi ir beigušies un vēl nav saņemti. Tāpēc finanšu informāciju nevar atjaunināt.
3.  Pārdošanas fabrikā reģistrējiet, ka krājums ir saņemts, un grāmatojiet pavadzīmi attiecībā uz ICSO999. Pirkuma fabrikā tiek automātiski grāmatota produktu ieejas plūsma attiecībā uz ICPO333. Pirkuma fabrikā saņemtais daudzums krājumam B-R14 mainās uz 100.
4.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO999. Grāmatošana ir sekmīga abās juridiskajās personās. Pirkuma fabrikā daudzums, kas ir iegādāts krājumam B-R14, mainās uz 100.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]