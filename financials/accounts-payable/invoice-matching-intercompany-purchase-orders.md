---
title: "Rēķinu salīdzināšana un starpuzņēmumu pirkšanas pasūtījumi"
description: "Pērkošo juridisko personu, kas ir iesaistīta starpuzņēmumu tirdzniecības transakcijā, var iestatīt kreditoru rēķinu salīdzināšanas lietošanai. Tādā gadījumā, lai varētu grāmatot starpuzņēmumu kreditoru rēķinus, ir jābūt ievērotām gan starpuzņēmumu tirdzniecības, gan kreditoru rēķinu salīdzināšanas grāmatošanas prasībām."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 45d0b24ed0a79176803a6efefc216f7e30fec86c
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Rēķinu salīdzināšana un starpuzņēmumu pirkšanas pasūtījumi

Pērkošo juridisko personu, kas ir iesaistīta starpuzņēmumu tirdzniecības transakcijā, var iestatīt kreditoru rēķinu salīdzināšanas lietošanai. Tādā gadījumā, lai varētu grāmatot starpuzņēmumu kreditoru rēķinus, ir jābūt ievērotām gan starpuzņēmumu tirdzniecības, gan kreditoru rēķinu salīdzināšanas grāmatošanas prasībām.

Šīs tēmas piemēros tiek izmantoti šādi starpuzņēmumu tirdzniecības iestatījumi:
-   Pirkuma fabrika ir juridiskā persona, kas veic pirkumu.
-   Pārdošanas fabrika ir juridiskā persona, kas veic pārdošanu.
-   Klients 4020 eksistē Pārdošanas Fabrikā.
-   Kreditors 3024 eksistē Pirkuma Fabrikā.
-   Fabrikam pirkšanā, starpuzņēmumu informāciju nav norādīts kreditora 3024. Fabrikam pārdošanas nav norādīta kā klienta uzņēmuma un klientu 4020 noradīta Fabrikam pirkšanas juridiskajai personai, kas atbilst debitora kontā.
-   Fabrikam pārdošanas, klientu 4020 nav norādīts starpuzņēmumu informāciju. Fabrikam pirkumu nav norādīta kā kreditoru uzņēmumam un kreditoru 3024 nav norādīta kreditora kontu, kas atbilst Fabrikam pārdošana juridiskai personai.

Piemēros Pirkuma fabrikai tiek lietoti šādi kreditoru rēķinu salīdzināšanas iestatījumi:
-   Lapā Kreditoru moduļa parametri ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes.
-   Lapā Kreditoru moduļa parametri lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu.
-   Cenas tolerance procentos juridiskajai personai ir 2 procenti.

## <a name="example-price-matching-and-intercompany-trade"></a> Piemērs. Cenu salīdzināšana un starpuzņēmumu tirdzniecība
Starpuzņēmumu kreditoru rēķina un starpuzņēmumu debitora rēķina neto summām ir jābūt vienādām. Šī nosacījuma prioritāte ir augstāka par jebkuriem piemērojamajiem rēķinu salīdzināšanas apstiprinājumiem vai cenu tolerances procentiem. Piemēram, izpildiet tālāk aprakstītās darbības.
1.  Fabrikam pirkšanā, veidot pārdošanas pasūtījumu SO888 klientam 4020. Starpuzņēmumu pirkšanas pasūtījuma ICPO222 tiek automātiski izveidota kreditoram 3024 Fabrikam pirkšanas un pārdošanas pasūtījumu ICSO888 automātiski tiek izveidota Fabrikam pārdošanas.
2.  Pārdošanas fabrikā reģistrējiet, ka krājumi ir saņemti, un iegrāmatojiet pavadzīmi. ICSO888 statuss nomainās uz Piegādāts. ICPO222 statuss nomainās uz Saņemts.
3.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO888. Vienības cena ir 0,45 un tiek atjauninātas 100 vienības.
4.  Pirkuma fabrikā izveidojiet rēķins attiecībā uz ICPO222. Neto cenu no 45,00 jūs nejauši maināt uz 54,00. Tiek parādīta ikona, lai norādītu, ka cena pārsniedz atļauto 2 procentu cenas toleranci.
5.  Lapā Rēķinu salīdzināšanas detalizēta informācija atlasiet opciju, lai apstiprinātu grāmatojumu ar salīdzināšanas neatbilstībām. Lapā Kreditora rēķins noklikšķiniet uz Labi. Ja kreditora rēķins nebūtu starpuzņēmumu kreditoru rēķins, tad grāmatošana būtu sekmīga. Taču, tā kā jūs strādājat ar starpuzņēmumu kreditoru rēķinu, grāmatošana ir nesekmīga. Starpuzņēmumu tirdzniecībai starpuzņēmumu pārdošanas pasūtījuma rēķinu kopsummai ir jābūt vienādai ar rēķinu kopsummām atbilstošajā starpuzņēmumu pirkšanas pasūtījumā. Lai atrisinātu šo problēmu, labojiet neto cenu rēķinā, šo neto cenu mainot atpakaļ uz noklusējuma summu 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Piemērs. Daudzuma salīdzināšana ar starpuzņēmumu tirdzniecību
Starpuzņēmumu pirkšanas pasūtījuma un starpuzņēmumu pārdošanas pasūtījuma daudzumiem ir jābūt vienādiem. Šīs prasības prioritāte ir augstāka par jebkuriem piemērojamajiem rēķinu salīdzināšanas apstiprinājumiem. Šajā piemērā tiek izmantoti šādi papildu iestatījumi attiecībā uz starpuzņēmumu tirdzniecību:
-   Pirkuma fabrikā pirkšanas pasūtījuma darbības politika attiecībā uz kreditoru 3024 ir iestatīta tā, lai automātiski grāmatotu gan sākotnējo debitora rēķinu, gan starpuzņēmumu kreditoru rēķinu.

Šajā piemērā tiek izmantoti šādi papildu iestatījumi attiecībā uz kreditoru rēķinu salīdzināšanu Pirkuma fabrikai:
-   Lapā Krājumu modeļu grupas modeļa grupai, kuru izmanto krājums B-R14, ir atlasīta opcija Saņemšanas prasības.
-   Rīcībā esošais krājuma B-R14 daudzums ir 0 (nulle).

Piemēram, izpildiet tālāk aprakstītās darbības.
1.  Fabrikam pirkšanā, veidot pārdošanas pasūtījumu SO999 klientam 4020. Uzdevums satur vienu posteni: 100 baterijas (prece B R14) 1,00 katru vienības cenu. Pirkuma fabrikā tiek automātiski izveidots starpuzņēmumu pirkšanas pasūtījums ICPO333 kreditoram 3024, un Pārdošanas fabrikā tiek automātiski izveidots pārdošanas pasūtījums ICSO999.
2.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO999. Grāmatošana ir nesekmīga, jo šīs preces krājumi ir beigušies un vēl nav saņemti. Tāpēc finanšu informāciju nevar atjaunināt.
3.  Pārdošanas fabrikā reģistrējiet, ka krājums ir saņemts, un grāmatojiet pavadzīmi attiecībā uz ICSO999. Pirkuma fabrikā tiek automātiski grāmatota produktu ieejas plūsma attiecībā uz ICPO333. Pirkuma fabrikā saņemtais daudzums krājumam B-R14 mainās uz 100.
4.  Pārdošanas fabrikā izpildiet rēķina atjaunināšanu attiecībā uz ICSO999. Grāmatošana ir sekmīga abās juridiskajās personās. Pirkuma fabrikā daudzums, kas ir iegādāts krājumam B-R14, mainās uz 100. 




