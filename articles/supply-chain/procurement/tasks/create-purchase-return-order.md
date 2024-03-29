---
title: Pirkšanas atgriešanas pasūtījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot pirkuma atgriešanas pasūtījumu, izmantojot darbību Kredīta nota, lai rindas no kreditora rēķina dokumenta kopētu jaunā PP.
author: GalynaFedorova
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 841229434fc278224f85d8d6782f80a31f4e23a9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678720"
---
# <a name="create-a-purchase-return-order"></a>Pirkšanas atgriešanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pirkuma atgriešanas pasūtījumu, izmantojot darbību Kredīta nota, lai rindas no kreditora rēķina dokumenta kopētu jaunā PP. Tajā ir arī parādīts, kā apstiprināt pasūtījumu un apstrādāt preču sūtījumu atpakaļ kreditoram. Šajā procedūrā rādīto piemēru var izmantot paraugdatu uzņēmumā USMF. Šo uzdevumu parasti veic pirkšanas aģents.

## <a name="create-a-new-purchase-return-order"></a>Izveidot jaunu pirkuma atgriešanas pasūtījumu
1. Pārejiet uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**. Vispirms ir jāizveido jauns pirkšanas pasūtījums, ko izmantot kā pirkuma atgriešanas pasūtījumu.  
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** ievadiet "US-102".
4. Noklikšķiniet uz **Labi**.
5. **Darbību rūtī** noklikšķiniet uz **Pirkšana**.
6. Noklikšķiniet uz **Kredīta nota**. Šī ir lapa, kurā no esoša kreditora rēķina varat kopēt uz savu atgriešanas pasūtījumu. Šī ir tā pati lapa, kas tiek izmantota citām kopēšanas darbībām. Bet, tā kā mēs to atvērām no darbības Kredīta nota, šī lapa ir konfigurēta tā, lai atbalstītu atgriešanas pasūtījuma izveidošanu, kas kompensē kreditoru rēķinus.  
7. Izvērsiet sadaļu **Parametri**.
    - Automātiski ir atlasīta opcija **Mainīt zīmi uz pretējo**, un to nevar mainīt. Tādējādi tiek nodrošināts, ka šiem daudzumiem tiek mainīta zīme un pievienotās pasūtījuma rindas kompensēs kreditora rēķinu.  
    - Automātiski ir atlasīta opcija **Kopēt maksas**, un to nevar mainīt. Tas nozīmē, ka maksas no kreditora rēķina tiek pievienotas pirkuma atgriešanas pasūtījumam, lai kompensētu sākotnējo maksu. Vēlāk ir iespējams modificēt izmaiņas pasūtījuma virsrakstā un rindās.  
    - Automātiski ir atlasīta opcija **Kopēt precīzi**, un to nevar mainīt. Tādējādi tiek nodrošināts, ka tiek izveidota precīza kopija no vērtībām visos attiecīgā kreditora rēķina virsraksta un rindu laukos. Tas nozīmē, ka pirkuma atgriešanas pasūtījums tiek izveidots ar vērtībām, kas atbilst visiem kreditora rēķina dokumentā lietotajiem nosacījumiem. 
    - Opcija **Dzēst pirkšanas rindas** pirms jauno rindu pievienošanas dzēš visas pirkšanas pasūtījuma rindas, kas jau pastāv pirkšanas pasūtījumā. Šajā piemērā mēs pirkuma atgriešanas pasūtījumam vēl neesam pievienojuši nevienu rindu, tāpēc tam nebūtu nekādas ietekmes. Šī opcija ir jālieto uzmanīgi, jo tā dzēš visas pastāvošās rindas bez papildu brīdinājuma.  
    * Automātiski ir atlasīta opcija **Kopēt pasūtījuma virsrakstu**, un to nevar mainīt. Tādējādi tiek nodrošināts, ka informācija tiek kopēta no kreditora rēķina un lietota pirkuma atgriešanas pasūtījuma virsrakstā. Tas ir noderīgi, jo palīdz nodrošināt, ka pirkuma atgriešanas pasūtījums kompensē rēķinu, izmantojot līdzīgus nosacījumus.  
8. Sakļaujiet sadaļu **Parametri**.
9. Izvērsiet sadaļu **Rēķini**. Šī lapa ir atvērta no darbības Kredīta nota, tāpēc vienīgā pieejamā opcija ir kopēt informāciju no kreditora rēķiniem. Šajā cilnē ir parādīti visi pieejamie rēķini attiecīgajam kreditora kontam, kas ir norādīts iepriekš izveidotajā pirkuma atgriešanas pasūtījumā.   Rēķini tiek identificēti ar rēķina dokumentu vai pirkšanas pasūtījuma ID.
10. Atrodiet kreditora rēķinu, kas ir identificēts ar rēķina numuru AP-0006, un izceliet tā rindu, noklikšķinot uz jebkura šīs rindas lauka.
11. Atlasiet rindu, noklikšķinot uz šīs rindas izvēles rūtiņas. Ņemiet vērā, ka kreditora rēķinā pieejamās rindas tiek automātiski atlasītas kopā ar pasūtījumu. Šim konkrētajam kreditora rēķinam ir 2 pasūtījuma rindas. Šajā piemērā mēs atgriezīsim daļu no otrās rindas daudzuma.
12. Izceliet otro rindu (rindu ar krājumu M0006), noklikšķinot uz jebkura lauka šajā rindā.
13. Laukā **Daudzums** mainiet daudzumu uz 10. Šis ir daudzums, kuru mēs atgriezīsim kreditoram. 
14. Izceliet pirmo rindu (rindu ar krājumu M0005), noklikšķinot uz jebkura lauka šajā rindā.
15. Noņemiet atzīmi šīs rindas izvēles rūtiņai. Uz jūsu pasūtījumu tiks kopētas tikai jūsu atlasītās rindas.
16. Sakļaujiet sadaļu **Rēķini**.
17. Izvērsiet sadaļu **Atlasītās rindas vai kopējamā galvene**. Šajā skatā tiek rādīts kopsavilkums par visiem dokumentiem un rindām, ko atlasījāt kopēšanai uz savu pasūtījumu.  
18. Sakļaujiet sadaļu **Atlasītās kopējamās rindas vai virsraksts**.
19. Noklikšķiniet uz **Labi**. Jūsu atlasītā rinda tagad ir pārkopēta uz jūsu pirkuma atgriešanas pasūtījumu. Laukā **Daudzums** tiek rādīts -10.   
20. Sadaļā **Pirkšanas pasūtījuma rinda** noklikšķiniet uz **Krājumi**.
21. Noklikšķiniet uz **Atzīmēšana**. Izveidotā pasūtījuma rinda ir atzīmēta pret krājumu transakciju no kreditora rēķina. Tādējādi tiek nodrošināts, ka kreditoram atgrieztie krājumi ir tie paši krājumi, kas no kreditora iepriekš tika saņemti. Pastāv situācijas, kur atzīmēšana nenotiek, piemēram, ja krājums jau ir atzīmēts kā Patērēts vai ja prece ir tāda, kam netiek lietota atzīmēšana.  

22. Noklikšķiniet uz **Labi**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Apstiprināt un reģistrēt preču sūtījumu
1. Noklikšķiniet uz **Darbības > Apstiprināt**.
2. **Darbību rūtī** noklikšķiniet uz **Saņemt**.
3. Nokl. **Pr. ieejas pl**.
    - Šī lapa tiek lietota, lai reģistrētu produktu ieejas plūsmu pirkšanas pasūtījumiem, kā arī lai apstrādātu preču atgriešanu atpakaļ kreditoram. Pasūtījumu rindas ar negatīvu daudzumu nozīmē, ka preces ir paredzēts atgriezt kreditoram, un no šīs lapas ģenerējamo dokumentu šim lietojumam var izmantot kā pavadzīmi.   
    - Šim piemēram laukā **Daudzums** atlasiet Pasūtītais daudzums. Tādējādi tiek nodrošināts, ka sūtījums tiks apstrādāts visam pasūtītajam daudzumam, ar kādu šīs pasūtījuma rindas tika izveidotas.   
4. Laukā **Prod. ieejas pl.** ierakstiet vērtību. Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.  
5. Noklikšķiniet uz **Labi**. Tagad preces ir reģistrētas kā nosūtītas pirkuma atgriešanas pasūtījumā, un ir izveidots produktu ieejas plūsmas žurnāls. Produktu ieejas plūsmas darbību var izmantot, lai pārskatītu ar pirkšanas pasūtījumu izveidotos žurnālus un redzētu, kas un kad tika saņemts vai atgriezts.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]