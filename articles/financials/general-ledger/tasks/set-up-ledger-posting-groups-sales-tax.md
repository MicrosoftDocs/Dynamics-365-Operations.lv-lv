--- 
title: "Virsgrāmatas grāmatošanas grupu izveide pievienotās vērtības nodoklim"
description: "PVN tiek aprēķināts un iegrāmatots galvenajos kontos, kas ir norādīti Virsgrāmatas grāmatošanas grupās."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 15421da6f325dfee22a303e9fe83a0e72895fa08
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Virsgrāmatas grāmatošanas grupu izveide pievienotās vērtības nodoklim

[!include [task guide banner](../../includes/task-guide-banner.md)]

PVN tiek aprēķināts un iegrāmatots galvenajos kontos, kas ir norādīti Virsgrāmatas grāmatošanas grupās. Virsgrāmatas grāmatošanas grupas ir piesaistītas katram PVN kodam. Varat iestatīt atsevišķas Virsgrāmatas grāmatošanas grupas katram PVN kodam, izmantot vienu virsgrāmatas grāmatošanas grupu visiem PVN kodiem vai PVN kodiem piešķirt vairākas Virsgrāmatas grāmatošanas grupas. Šis paraugs izmanto DEMF demonstrācijas uzņēmumu. 

1. Pārejiet uz sadaļu Nodokļi > Iestatījumi > PVN > Virsgrāmatas grāmatošanas grupas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Virsgrāmatas grāmatošanas grupa.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Maksājamais PVN atlasiet galveno kontu izejošiem PVN, kas ir jāmaksā nodokļu iestādei.
    * PVN tiek iekasēts nodokļu iestādes vietā, ja pārdodat ar nodokli apliekamas preces un pakalpojumus.  
6. Laukā Saņemtais PVN atlasiet galveno kontu ienākošajiem nodokļiem, kas ir saņemti no nodokļu iestādes.
    * Kreditori iekasē nodokli nodokļu iestādes vārdā, ja pērkat ar nodokli apliekamas preces un pakalpojumus. Šis lauks nav pieejams, ja lapā Virsgrāmatas parametri ir atlasīta opcija Lietot PVN nodokļu nosacījumus. Tā vietā PVN, kas tiek maksāts kreditoriem, tiek debetēts tajā pašā kontā, kurā pirkums.   
7. Laukā Importa nodokļa izdevumi atlasiet galveno kontu, lai grāmatotu ieturamos importa nodokļus, kurus kreditori nav paziņojuši vai snieguši nodokļu iestādei kā daļu no ES atgriezeniskā GST/HST.
    * Transakcijā izmantotajam PVN grupas PVN kodam jāatlasa opcija Importa nodoklis.  Šis lauks nav pieejams, ja lapā Virsgrāmatas parametri ir atlasīta opcija Lietot PVN nodokļu nosacījumus.   
8. Laukā Maksājamais importa nodoklis atlasiet galveno kontu, kurā grāmatot ienākošos importa nodokļus, kas ir jāmaksā nodokļu iestādēm.
    * Lai iegrāmatotu importa nodokli, ir jāatlasa opcija Importa nodoklis PVN grupas PVN kodā. Ja opcija Lietot PVN nodokļu kārtulas ir atlasīta Virsgrāmatas parametros, nobīde tiek grāmatota transakcijas izdevumu kontā.   
9. Laukā Apmaksas konts atlasiet galveno kontu, kurā tiks grāmatota neto bilance no Virsgrāmatas kontiem, kas norādīti laukos Maksājamais importa nodoklis un Saņemamais PVN.
    * Bilance tiks izveidota, kad tiks palaists uzdevums PVN apmaksai un grāmatošanai.  Ja nodokļu iestāde maksājumu periodam ir saistīta ar kreditora kontu, bilance tiek grāmatota uz kreditora kontu.   
10. Laukā Kreditora termiņatlaide atlasiet galveno kontu, kurā grāmatot termiņatlaides PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu.
    * Tas nav obligāti un, ja nav ievadīts neviens konts, tiks izmantots termiņatlaižu kodu galvenais konts. Ja izmantojat PVN grupu opciju PVN atgriešana termiņatlaidēs, var būt noderīgi izmantot atšķirīgus kontus Virsgrāmatas grāmatošanas grupām.  
11. Laukā Debitora termiņatlaide atlasiet galveno kontu, kurā grāmatot termiņatlaides PVN kodiem, kas saistīti ar šo Virsgrāmatas grāmatošanas grupu.
    * Tas nav obligāti un, ja nav ievadīts neviens konts, tiks izmantots termiņatlaižu kodu galvenais konts. Ja izmantojat PVN grupu opciju PVN atgriešana termiņatlaidēs, var būt noderīgi izmantot atšķirīgus kontus Virsgrāmatas grāmatošanas grupām.  
12. Noklikšķiniet uz Saglabāt.


