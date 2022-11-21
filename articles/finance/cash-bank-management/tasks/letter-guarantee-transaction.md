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
ms.openlocfilehash: 30e21c11b067f6def127f3eab026d7255ab1ca29
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779939"
---
# <a name="letter-of-guarantee-transaction"></a>Garantijas vēstules darījums

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts garantijas vēstules process.



Pirms šīs procedūras jābūt pabeigtiem tālāk minētajiem uzdevumiem:

- Iestatiet bankas iestādes un garantijas vēstules grāmatošanas profilus.

- Izveidojiet bankas iestādes līgumu garantijas vēstulei.



Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Pārdošanas pasūtījuma ar garantijas vēstuli izveide
1. Pārejiet uz sadaļu **Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Klienta konts**.
4. Izvērsiet sadaļu Vispārīgi.
5. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā **Bankas dokumenta veids** atlasiet **Garantijas vēstule**.
10. Noklikšķiniet uz **Labi**.
11. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
12. Laukā **Vienības cena** ievadiet kādu skaitli.
13. Izvērsiet sadaļu Detalizēta informācija par rindu.
14. Noklikšķiniet uz cilnes Piegāde.
    * Piezīme. Atlasiet Piegādes datuma kontrole = Nav  
15. **Laukā Pieprasītais nosūtīšanas datums** ievadiet datumu.
16. **Laukā Apstiprināts nosūtīšanas datums** ievadiet datumu.

## <a name="process-letter-of-guarantee_request"></a>Garantijas vēstules pieprasījuma apstrāde
1. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
2. Noklikšķiniet uz **Garantijas** vēstule.
3. Darbību rūtī noklikšķiniet uz **Garantijas** vēstule.
4. Noklikšķiniet uz **Pieprasījums**, lai atvērtu nomešanas dialoglodziņu.
5. Laukā **Tips** ievadiet vai atlasiet vērtību.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Ievadiet skaitli laukā **Vērtība**.
8. **Laukā Derīguma termiņš** ievadiet datumu un laiku.
9. Noklikšķiniet uz **Labi**.
10. Aizvērt lapu.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Garantijas vēstules iesniegšanas bankā process
1. Dodieties uz **Skaidras naudas un bankas vadība > Garantijas vēstules > Garantijas** vēstules.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Noklikšķiniet uz **Iesniegt bankai**, lai atvērtu nomešanas dialoglodziņu.
4. Ievadiet vai atlasiet vērtību laukā **Bankas konts**.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Labi**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Garantijas vēstules saņemšanas no bankas process
1. Noklikšķiniet uz **Saņemt no bankas**, lai atvērtu nomešanas dialoglodziņu.
2. Laukā **Bankas numurs** ierakstiet vērtību.
    * Pārbaudiet vērtības aprēķinātajos **laukos Piemale** un **Izdevumi**.  
3. Noklikšķiniet uz **Labi**.
4. Izvērsiet sadaļu Darbības.
    * Pārbaudiet ierakstu Saņemt no bankas.  
5. Noklikšķiniet, lai sekotu saitei laukā Žurnāla **partijas numurs**.
6. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet žurnāla ierakstu grāmatojumu.  
7. Aizvērt lapu.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Garantijas vēstules izsniegšanas saņēmējam process
1. Pārejiet uz sadaļu **Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet uz **Garantijas** vēstule.
5. Darbību rūtī noklikšķiniet uz **Garantijas** vēstule.
6. Noklikšķiniet uz **Piešķirt saņēmējam**, lai atvērtu nomešanas dialoglodziņu.
7. Noklikšķiniet uz **Labi**.
8. Dodieties uz **Skaidras naudas un bankas vadība > Garantijas vēstules > Garantijas** vēstules.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz **Piešķirt saņēmējam**, lai atvērtu nomešanas dialoglodziņu.
11. Noklikšķiniet uz **Labi**.
12. Izvērsiet sadaļu Darbības.
    * Pārbaudiet ierakstu Nodot saņēmējam.  

## <a name="process-letter-of-guarantee_increase-value"></a>Garantijas vēstules vērtības palielināšanas process
1. Pārejiet uz sadaļu **Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet uz **Garantijas** vēstule.
5. Darbību rūtī noklikšķiniet uz **Garantijas** vēstule.
6. Noklikšķiniet uz **Palielināt vērtību**, lai atvērtu nomešanas dialoglodziņu.
7. **Laukā Pievienojamā** vērtība ievadiet skaitli.
8. Noklikšķiniet uz **Labi**.
9. Dodieties uz **Skaidras naudas un bankas vadība > Garantijas vēstules > Garantijas** vēstules.
10. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
11. Noklikšķiniet uz **Palielināt vērtību**, lai atvērtu nomešanas dialoglodziņu.
12. Noklikšķiniet uz **Labi**.
13. Izvērsiet sadaļu Darbības.
    * Pārbaudiet ierakstu Palielināt vērtību.  
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Noklikšķiniet, lai sekotu saitei laukā Žurnāla **partijas numurs**.
16. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet grāmatotos žurnāla ierakstus.  

## <a name="process-letter-of-guarantee_liquidate"></a>Garantijas vēstules iznīcināšanas process
1. Pārejiet uz sadaļu **Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
4. Noklikšķiniet uz **Garantijas** vēstule.
5. Darbību rūtī noklikšķiniet uz **Garantijas** vēstule.
6. Noklikšķiniet uz **Likvidēt**, lai atvērtu nomešanas dialoglodziņu.
7. Noklikšķiniet uz **Labi**.
8. Dodieties uz **Skaidras naudas un bankas vadība > Garantijas vēstules > Garantijas** vēstules.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz **Likvidēt**, lai atvērtu nomešanas dialoglodziņu.
11. Noklikšķiniet uz **Labi**.
12. Izvērsiet sadaļu Darbības.
    * Pārbaudiet ierakstu Likvidēt.  
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Noklikšķiniet, lai sekotu saitei laukā Žurnāla **partijas numurs**.
15. Noklikšķiniet uz **Rindas**.
    * Pārbaudiet grāmatotos žurnāla ierakstus.  
16. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
