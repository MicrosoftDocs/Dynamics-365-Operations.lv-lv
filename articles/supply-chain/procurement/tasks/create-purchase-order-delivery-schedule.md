---
title: Pirkšanas pasūtījuma izveide ar piegādes grafiku
description: Šajā tēmā ir parādīts, kā izveidot piegādes grafiku pirkšanas pasūtījumam.
author: mkirknel
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c4e8dca93fdf9ee605ffeb63f259389b58a4b36
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433175"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Pirkšanas pasūtījuma izveide ar piegādes grafiku

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir parādīts, kā izveidot piegādes grafiku pirkšanas pasūtījumam. Piegādes grafiks tiek izmantots, kad pasūtījumā vai žurnālā minēto daudzumu ir pieprasīts piegādāt vairākos sūtījumos. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Parasti šo procedūru veic pirkšanas aģents.

## <a name="create-a-delivery-schedule"></a>Piegādes grafika izveide
1. Navigācijas rūtī dodieties uz **Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Kreditora konts** ievadiet `US-101`.
4. Atlasiet **Labi**.
5. Laukā **Krājuma kods** ievadiet `M0001`.
6. Laukā **Daudzums** ievadiet `10`.
7. Atlasiet **Pirkšanas pasūtījuma rinda**.
8. Atlasiet **Piegādes grafiks**.
- Lapā **Piegādes grafiks** jūs varat norādīt sūtījumu skaitu, kādā no kreditora tiks piegādāts viss pasūtījuma rindas daudzums.  
- Pēc noklusējuma sistēma no sākotnējās pirkšanas rindas uz pirmo piegādes grafika rindu kopē kopējo daudzumu un citu piegādes informāciju. Šajā piemērā mēs izveidosim grafiku diviem sūtījumiem, un otrā sūtījuma datumam no pirmā sūtījuma būs nobīde par vienu nedēļu.  
9. Laukā **Daudzums** mainiet daudzumu uz `4`.
10. Atlasiet **Jauns**.
11. Laukā **Daudzums** ievadiet `6` kā atlikušo daudzumu.
- Piegādes datuma laukā atlasiet datumu, kas ir vienu nedēļu pēc pirmās piegādes rindas datuma.  
- Piegādes grafika rindām piešķirtajam kopējam daudzumam varat sekot līdzi, apskatot laukus **Kopsumma** un **Atlicis**. Ja atlikušais daudzums ir nulle, grafikam ir piešķirts viss daudzums no sākotnējās rindas.  
12. Izvērsiet sadaļu **Izmaksu konvertēšana**.
- Šeit pieejamās opcijas jums ļauj kontrolēt veidu, kādā maksas vēlaties sadalīt pa piegādes grafika rindām. Ja atlasāt **Kopēt bruto summas**, tad uz katru piegādes rindu tiek kopēta sākotnējās pasūtījuma rindas maksas summa. Opcija **Piešķirt piegādes rindām** sākotnējās rindas maksu sadala atbilstoši daudzumam katrā piegādes rindā.  
13. Sakļaujiet sadaļu **Izmaksu konvertēšana**.
14. Atlasiet **Labi**.
- Tagad piegādes grafiks ir lietots pasūtījumam.  
- Sākotnējā pasūtījuma rinda, ko tagad sauc par komerciālo rindu, ir pārvērsta par pasūtījuma rindu ar vairākām piegādēm. Tā ir atzīmēta ar atšķirīgu ikonu un darbojas kā piegādes rindu virsraksts.  
15. Atlasiet otro pasūtījuma rindu, kas ir pirmā no abām piegādes rindām.
- Abas jaunās rindas, sauktas par piegādes rindām, veido vienu piegādes grafiku. Pasūtījums tiks apstrādāts pret šīm rindām, nevis sākotnējo rindu. Ja tiek drukāti dokumenti, piemēram, apstiprinājumi, produktu ieejas plūsmu žurnāli vai rēķini, tiek rādītas tikai piegādes rindas.  

## <a name="change-the-delivery-schedule"></a>Mainīt piegādes grafiku
Piegādes rindās norādīto daudzumu varat mainīt. Ja to darāt, komerciālā rinda tiek automātiski atjaunināta uz kopējo daudzumu piegādes rindās.  
1. Pirmās piegādes rindas laukā **Daudzums** mainiet daudzumu no `4` uz `5`.
2. Atlasiet pirmo pasūtījuma rindu (komerciālo rindu).  
- Daudzums komerciālajā rindā ir mainīts uz 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Apstrādāt produktu ieejas plūsmu, izmantojot piegādes grafikus
Lai preču ieejas plūsmas varētu apstrādāt, pirkšanas pasūtījumam ir jābūt apstiprinātam. Šajā piemērā ieejas plūsma tiek ierakstīta tieši pirkšanas pasūtījumā. Plūsmu var arī reģistrēt, kad preces tiek saņemtas noliktavā.  
1. Darbību rūtī atlasiet **Pirkšana**.
2. Atlasiet **Apstiprināt**.
3. Darbību rūtī atlasiet **Saņemt**.
4. Atlasiet **Preču ieejas plūsma**. Laukā **Preču ieejas plūsma** ierakstiet jebkādu vērtību.
- Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.  
- Laukā **Daudzums** atlasiet **Pasūtītais daudzums**. Šī opcija nozīmē, ka ienākošā plūsma tiks apstrādāta daudzumam, ar kādu tika izveidotas šīs pasūtījuma rindas.  
- Pārliecinieties, ka laukam **Drukāt preču ieejas plūsmu** ir iestatīta vērtība **Nē**. Šajā piemērā drukāšana nav nepieciešama.  
5. Izvērsiet sadaļu **Rindas**.
- Ņemiet vērā, kā produktu ieejas plūsma tiek izveidota abām piegādes rindām, nevis sākotnējai pasūtījuma rindai. Ja ieejas plūsma tika reģistrēta noliktavā, tad tā tiktu reģistrēta arī piegādes grafika rindās.  
6. Sakļaujiet sadaļu **Rindas**.
7. Atlasiet **Labi**, lai iegrāmatotu ieejas plūsmu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]