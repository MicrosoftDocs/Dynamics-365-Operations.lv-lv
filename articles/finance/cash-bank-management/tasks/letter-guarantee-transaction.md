---
title: Garantijas vēstules darījums
description: Šajā procedūrā ir aprakstīts garantijas vēstules process.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786aecf69bae3d07ac80a55b4dc835dd8129bd59
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803969"
---
# <a name="letter-of-guarantee-transaction"></a>Garantijas vēstules darījums

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts garantijas vēstules process.



Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:

- Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.

- Izveidojiet bankas iestādes līgumu garantijas vēstulei.



Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Pārdošanas pasūtījuma ar garantijas vēstuli izveide
1. Dodieties uz **debitoru > pasūtījumiem > visiem pārdošanas pasūtījumiem**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Klienta konts**.
4. Izvērsiet sadaļu **Vispārīgi**.
5. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā **Bankas dokumenta** tips atlasiet garantijas **vēstuli**.
10. Noklikšķiniet uz **Labi**.
11. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
12. Laukā **Vienības cena** ievadiet kādu skaitli.
13. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
14. Noklikšķiniet uz **cilnes** Piegāde.

>[!Note] 
>Atlasīt **piegādes datuma kontroli Nav** = **·**  

15. Laukā **Pieprasītais nosūtīšanas** datums ievadiet datumu.
16. Laukā **Apstiprinātais nosūtīšanas** datums ievadiet datumu.

## <a name="process-letter-of-guarantee_request"></a>Garantijas vēstules pieprasījuma apstrāde
1. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
2. Noklikšķiniet **uz garantijas vēstules**.
3. Darbību rūtī noklikšķiniet uz garantijas **vēstules**.
4. Noklikšķiniet **uz Pieprasījums,** lai atvērtu nolaižamo dialogu.
5. Laukā **Tips** ievadiet vai atlasiet vērtību.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Ievadiet skaitli laukā **Vērtība**.
8. Laukā **Beigu datums** ievadiet datumu un laiku.
9. Noklikšķiniet uz **Labi**.
10. Aizvērt lapu.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Garantijas vēstules iesniegšanas bankā process
1. Dodieties uz **"Skaidras naudas un bankas > garantijas vēstules > garantijas vēstulēm**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Lai **atvērtu nolaižamo dialogu**, noklikšķiniet uz Iesniegt bankā.
4. Ievadiet vai atlasiet vērtību laukā **Bankas konts**.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Labi**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Garantijas vēstules saņemšanas no bankas process
1. Lai **atvērtu nomešanas dialogu**, noklikšķiniet uz Saņemt no bankas.
2. Laukā **Bankas** numurs ierakstiet vērtību.
    * Pārbaudiet vērtības aprēķinātajā uzcenojuma **un** izdevumu **laukos**.  
3. Noklikšķiniet uz **Labi**.
4. Izvērsiet sadaļu **Darbības**.
    * Pārbaudiet ierakstu Saņemt no bankas.  
5. Noklikšķiniet, lai sekotu saitei žurnāla **partijas numura** laukā.
6. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet žurnāla ierakstu grāmatojumu.  
7. Aizvērt lapu.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Garantijas vēstules izsniegšanas saņēmējam process
1. Dodieties uz **debitoru > pasūtījumiem > visiem pārdošanas pasūtījumiem**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet **uz garantijas vēstules**.
5. Darbību rūtī noklikšķiniet uz garantijas **vēstules**.
6. Noklikšķiniet **uz Piešķirt saņēmējam,** lai atvērtu nolaižamo dialogu.
7. Noklikšķiniet uz **Labi**.
8. Dodieties uz **"Skaidras naudas un bankas > garantijas vēstules > garantijas vēstulēm**.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet **uz Piešķirt saņēmējam,** lai atvērtu nolaižamo dialogu.
11. Noklikšķiniet uz **Labi**.
12. Izvērsiet sadaļu **Darbības**.
    * Pārbaudiet ierakstu Nodot saņēmējam.  

## <a name="process-letter-of-guarantee_increase-value"></a>Garantijas vēstules vērtības palielināšanas process
1. Dodieties uz **debitoru > pasūtījumiem > visiem pārdošanas pasūtījumiem**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet **uz garantijas vēstules**.
5. Darbību rūtī noklikšķiniet uz garantijas **vēstules**.
6. Noklikšķiniet uz **Palielināt vērtību,** lai atvērtu nolaižamo dialogu.
7. Laukā **Vērtība, kas jāpievieno**, ievadiet skaitli.
8. Noklikšķiniet uz **Labi**.
9. Dodieties uz **"Skaidras naudas un bankas > garantijas vēstules > garantijas vēstulēm**.
10. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
11. Noklikšķiniet uz **Palielināt vērtību,** lai atvērtu nolaižamo dialogu.
12. Noklikšķiniet uz **Labi**.
13. Izvērsiet sadaļu **Darbības**.
    * Pārbaudiet ierakstu Palielināt vērtību.  
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Noklikšķiniet, lai sekotu saitei žurnāla **partijas numura** laukā.
16. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet grāmatotos žurnāla ierakstus.  

## <a name="process-letter-of-guarantee_liquidate"></a>Garantijas vēstules iznīcināšanas process
1. Dodieties uz **debitoru > pasūtījumiem > visiem pārdošanas pasūtījumiem**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet **uz garantijas vēstules**.
5. Darbību rūtī noklikšķiniet uz garantijas **vēstules**.
6. Noklikšķiniet uz **Likvidēt,** lai atvērtu nomešanas dialogu.
7. Noklikšķiniet uz **Labi**.
8. Dodieties uz **"Skaidras naudas un bankas > garantijas vēstules > garantijas vēstulēm**.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz **Likvidēt,** lai atvērtu nomešanas dialogu.
11. Noklikšķiniet uz **Labi**.
12. Izvērsiet sadaļu **Darbības**.
    * Pārbaudiet ierakstu Likvidēt.  
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Noklikšķiniet, lai sekotu saitei žurnāla **partijas numura** laukā.
15. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet grāmatotos žurnāla ierakstus.  
16. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
