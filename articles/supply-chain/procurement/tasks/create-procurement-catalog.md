---
title: Sagādes kataloga izveide
description: Šajā tēmā ir paskaidrots, kā izveidot sagādes katalogu.
author: kamaybac
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9bec131798a67695bc3ea27cbbdea404d4494382e25e97b2931508ec7d52fca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746919"
---
# <a name="create-a-procurement-catalog"></a>Sagādes kataloga izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot sagādes katalogu. Šo uzdevumu parasti veic sagādes speciālists. Jūs arī uzzināsiet, kā darbinieki var izmantot katalogu, kad viņi veido pieprasījumu. Lai varētu izveidot katalogu, jūsu sistēma ir jābūt sagādes kategoriju hierarhijai. Jaunais katalogs pārmanto šo hierarhiju, kā arī visas preces, kas atrodas šajā hierarhijā. Šo ceļvedi varat izmantot demonstrācijas datu uzņēmumā USMF, kur sagādes kategoriju hierarhija ir pieejama, kā arī procedūras darbībās izmantotajos piemēros.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Pārliecinieties, ka pastāv sagādes kategoriju hierarhija
1. Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Sagādes kategorijas**. Sagādes kategoriju hierarhija ir pieejama USMF demonstrācijas datu uzņēmumā, un preces ir pievienotas kategorijai **Biroja aparatūra/datori**. Ja šo procedūru izpildāt kā uzdevuma ceļvedi, ir nepieciešams atbloķēt šo ceļvedi, ja vēlaties pārlūkot kategoriju. Ja hierarhija nebija pieejama, jums tā būtu jāizveido, noklikšķinot uz **Jauns**. To var izdarīt tikai vienu reizi.  
2. Aizvērt lapu.

## <a name="create-a-catalog"></a>Kataloga izveidošana
1. Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Katalogi > Sagādes katalogi**.
2. Atlasiet **Jauns sagādes katalogs**, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Atlasiet **Labi**.
5. Koka struktūrā izvērsiet vienumu **KORP. SAGĀDES KATEGORIJAS**.
6. Koka struktūrā izvērsiet vienumu **BIROJA APARATŪRA**.
7. Koka struktūrā atlasiet vienumu **Datori**.

  - Preces no sagādes kategorijas tiek parādītas sarakstā. Ja vēlaties kategorijai pievienot kādu preci, tas ir jādara lapā **Sagādes kategoriju hierarhija** vai lapā **Detalizēta informācija par krājumu**.  
  - **Noklusējuma** atjaunināšanas tips nosaka, vai sagādes kategoriju hierarhijai pievienotās jaunās preces katalogā kļūst redzamas uzreiz. Ja atjaunināšanas tips ir iestatīts uz **Dinamisks**, izmaiņas ir redzamas nekavējoties. Ja atjaunināšanas tips ir **Statisks**, jaunās preces kļūst redzamas tikai personām, kas katalogu lieto pēc tam, kad katalogs ir pārpublicēts. Darbība **Publicēt** ir pieejama darbību rūtī lapas augšdaļā. Ja preces tiek noņemtas no sagādes kategoriju hierarhijas, šīs izmaiņas kļūst redzamas nekavējoties, neatkarīgi no vērtības laukā **Noklusējuma** atjaunināšanas tips.  

8. Darbību rūtī atlasiet **Kategoriju navigācija** un pārliecinieties, vai ir atlasīta opcija **Iespējot**.
9. Atlasiet **Aktivizēt katalogu**.
10. Aizvērt lapu.

## <a name="make-the-catalog-visible"></a>Padarīt katalogu redzamu
1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas**.
2. Atlasiet **Sagādes politika USMF**. Ir jāatlasa pirkšanas politika tai juridiskajai personai, kurā ar jūsu lietotāja profilu saistītajam nodarbinātajam ir atļauts pasūtīt preces. In the USMF demo data, the Admin user is connected to the worker called **Jūlija Funderburka**, un viņa pēc noklusējuma pasūta preces uzņēmumā USMF.  
3. Atlasiet katalogu, ko tikko izveidojāt.
4. Atlasiet **Labi**.

## <a name="use-the-catalog"></a>Lietot katalogu
1. Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Atlasiet **Labi**.
5. Atlasiet **Pievienot preces**.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Lai filtrētu šīs preces, varat lietot kreisajā pusē esošo kategoriju hierarhiju vai filtru saraksta augšpusē.  
7. Atlasiet **Pievienot rindām**.
8. Atlasiet **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]