--- 
title: "Sagādes kataloga izveide"
description: "Šajā ceļvedī ir parādīts, kā izveidot sagādes katalogu."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Sagādes kataloga izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ceļvedī ir parādīts, kā izveidot sagādes katalogu. Šo uzdevumu parasti veic sagādes speciālists. Jūs arī uzzināsiet, kā darbinieki var izmantot katalogu, kad viņi veido pieprasījumu. Lai varētu izveidot katalogu, jūsu sistēma ir jābūt sagādes kategoriju hierarhijai. Jaunais katalogs pārmanto šo hierarhiju, kā arī visas preces, kas atrodas šajā hierarhijā. Šo ceļvedi varat izmantot demonstrācijas datu uzņēmumā USMF, kur sagādes kategoriju hierarhija ir pieejama, kā arī procedūras darbībās izmantotajos piemēros.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Pārliecinieties, ka pastāv sagādes kategoriju hierarhija
1. Pārejiet uz Sagāde un avoti > Sagādes kategorijas.
    * Sagādes kategoriju hierarhija ir pieejama USMF demonstrācijas datu uzņēmumā, un preces ir pievienotas kategorijai Biroja aparatūra/datori. Ja šo procedūru izpildāt kā uzdevuma ceļvedi, ir nepieciešams atbloķēt šo ceļvedi, ja vēlaties pārlūkot kategoriju. Ja hierarhija nebija pieejama, jums tā būtu jāizveido, noklikšķinot uz Jauns. To var izdarīt tikai vienu reizi.  
2. Aizvērt lapu.

## <a name="create-a-catalog"></a>Kataloga izveidošana
1. Pārejiet uz sadaļu Sagāde un avoti > Katalogi > Sagādes katalogi.
2. Noklikšķiniet uz Jauns sagādes katalogs, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Noklikšķiniet uz Labi.
5. Koka struktūrā izvērsiet vienumu “KORP. SAGĀDES KATEGORIJAS”.
6. Koka struktūrā izvērsiet vienumu “BIROJA APARATŪRA”.
7. Koka struktūrā atlasiet vienumu “Datori”.
    * Preces no sagādes kategorijas tiek parādītas sarakstā. Ja vēlaties kategorijai pievienot kādu preci, tas ir jādara lapā Sagādes kategoriju hierarhija vai lapā Detalizēta informācija par krājumu.  
    * Noklusējuma atjaunināšanas tips nosaka, vai sagādes kategoriju hierarhijai pievienotās jaunās preces katalogā kļūst redzamas uzreiz. Ja atjaunināšanas tips ir iestatīts uz Dinamisks, izmaiņas ir redzamas nekavējoties. Ja atjaunināšanas tips ir Statisks, jaunās preces kļūst redzamas tikai personām, kas katalogu lieto pēc tam, kad katalogs ir pārpublicēts. Darbība Publicēt ir pieejama darbību rūtī lapas augšdaļā. Ja preces tiek noņemtas no sagādes kategoriju hierarhijas, šīs izmaiņas kļūst redzamas nekavējoties, neatkarīgi no vērtības laukā Noklusējuma atjaunināšanas tips.  
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Noklikšķiniet uz Slēpt.
10. Darbību rūtī noklikšķiniet uz Kategoriju navigācija.
11. Noklikšķiniet uz Atspējot.
12. Darbību rūtī noklikšķiniet uz Kategoriju navigācija.
13. Noklikšķiniet uz Iespējot.
14. Noklikšķiniet uz Aktivizēt katalogu.
15. Aizvērt lapu.

## <a name="make-the-catalog-visible"></a>Padarīt katalogu redzamu
1. Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas.
2. Atlasiet vienumu Sagādes politika USMF.
    * Ir jāatlasa pirkšanas politika tai juridiskajai personai, kurā ar jūsu lietotāja profilu saistītajam nodarbinātajam ir atļauts pasūtīt preces. USMF demonstrācijas datos lietotājs ar lomu Administrators ir savienots ar nodarbināto, kuru sauc Jūlija Funderburka, un viņa pēc noklusējuma pasūta preces uzņēmumā USMF.  
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Atlasiet katalogu, ko tikko izveidojāt.
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.
7. Aizvērt lapu.

## <a name="use-the-catalog"></a>Lietot katalogu
1. Dodieties uz sadaļu Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Pievienot preces.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Lai filtrētu šīs preces, varat lietot kreisajā pusē esošo kategoriju hierarhiju vai filtru saraksta augšpusē.  
7. Noklikšķiniet uz Pievienot rindām.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
9. Noklikšķiniet uz Pievienot rindām.
10. Noklikšķiniet uz OK.


