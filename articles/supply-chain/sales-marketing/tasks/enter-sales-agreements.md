---
title: Pārdošanas līgumu ievade
description: Šajā tēmā ir aprakstīts, kā izveidot pārdošanas līgumu, kas i vienu no jūsu klientiem nopirkt preci par noteiktu summu laika gaitā apmaiņā par īpašām atlaidēm.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee2c1494842c5fd2aa598546ba655c33d6fd3f16
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568307"
---
# <a name="enter-sales-agreements"></a>Pārdošanas līgumu ievade

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot pārdošanas līgumu, kas i vienu no jūsu klientiem nopirkt preci par noteiktu summu laika gaitā apmaiņā par īpašām atlaidēm. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-sales-agreement-header"></a>Pārdošanas līguma virsraksta iestatīšana
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.
4. Laukā **Pārdošanas līguma klasifikācijā** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.
5. Izvērsiet sadaļu **Vispārīgi**.
6. Laukā **Noklusējuma saistības** atlasiet **Preces vērtības saistības**. Saistību veids ir obligāts kritērijs, kas ir jāpiešķir līgumam, lai definētu, kā līgums tiks izpildīts. Izmantojot četrus iepriekš definētus veidus, var iestatīt klienta saistību mērķi, kas tiek izteikts kā daudzums vai vērtība. Daudzuma saistību veidu var lietot tikai noteiktām precēm, bet vērtību veidus var lietot konkrētu vai vispārīga veida preču pārdošanā.  
7. Laukā **Beigu datums** iestatiet datumu un nākotnes vēlamo līguma izbeigšanas datumu.
8. Atlasiet **Labi**.

## <a name="set-up-product-value-commitment-lines"></a>Uz preču vērtību attiecināmo saistību rindu iestatīšana
1. Atlasiet **Pievienot rindu**.
2. Laukā **Vienuma numurs** atlasiet vēlamo ierakstu nolaižamajā izvēlnē. Līgumam izvēlēto saistību veids ietekmē to, kāda veida informāciju var ievadīt līguma rindās. Piemēram, vērtību līgumam ir jānorāda kopējā neto summa (saskaņotajā valūtā), par kuru debitors apņēmās nopirkt no jums preces. Šajā piemērā lauki **Daudzums** un **Vienība** rindā nav pieejami, jo jūs veidojat līgumu, lai klients iegādātos noteiktu preces vērtību.   
3. Laukā **Neto summa** ievadiet naudas summu, ko klients ir iesniedzis pirkumam.
4. Laukā **Atlaides procents** ievadiet procentuālo vērtību, kas tiks piemērota klienta pārdošanas pasūtījuma rindām, kas saistītas ar šo līgumu.
5. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
6. Atlasiet **Jā** laukā **Sasniegts maksimums**.
    - Atlasot **Sasniegts maksimums** nozīmē, ka kopējais pārdošanas pasūtījuma rindu skaits, kas izmanto apņemšanās īpašās cenas, atlaides un/vai maksājuma nosacījumus, nedrīkst pārsniegt apņemšanās norādīto summu.  
    - Minimālā un maksimālā izlaišanas summa norāda to vērtību diapazonu, kas ir jāpārdod katrā pārdošanas pasūtījumā, kas izmanto atlasīto līgumu.   
7. Izvērtiet sadaļu **Pārdošanas līguma virsraksts**. Ja vien līguma statuss nav iestatīts uz **Spēkā**, pārdošanas pasūtījumus nevar saistīt ar līgumu un tādēļ nevar ietekmēt šāda līguma izpildi. Šajā posmā statusu var mainīt manuāli. Tomēr statuss parasti ir jāmaina tad, kad apstiprināt debitora līgumu.  
8. Darbību rūtī atlasiet **Pārdošanas līgums**.
9. Atlasiet **Apstiprināšana**. Pārliecinieties, ka opcija **Atzīmēt līgumu kā spēkā esošu** ir iestatīta uz **Jā**.  
10. Laukā **Drukāt pārskatu** atlasiet **Jā**.
11. Atlasiet **Labi**.
12. Aizvērt lapu. Līgums tagad ir spēkā. Varat sākt saistīt klienta pasūtījumus ar līgumu, lai to ieskaitītu noteiktajā mērķī.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]