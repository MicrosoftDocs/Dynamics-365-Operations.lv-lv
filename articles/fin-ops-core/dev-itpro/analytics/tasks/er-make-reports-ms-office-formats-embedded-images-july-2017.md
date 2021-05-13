---
title: Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli
description: Šajā tēmā paskaidrots, kā izstrādāt konfigurācijas, kas ģenerē elektronisko pārskatu dokumentus Excel un Word formātos, kas satur ģenerētu iegultus attēlus.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944561"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli

[!include [banner](../../includes/banner.md)]

Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu." Šīs procedūrās aprakstā ir paskaidrots, kā izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai ģenerētu iegultus attēlus saturošus Microsoft Excel vai Word dokumentus. Šajā procedūrā izveidosit nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Šīs darbības var izpildīt, izmantojot USMF datu kopu. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Pirms sākšanas, lejupielādējiet un saglabājiet tālāk norādītos failus: 

| Apraksts                                          | Faila nosaukums                   |
|------------------------------------------------------|-----------------------------|
| ER datu modeļa konfigurācija                          | [cheques.xml modelis](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER formāta konfigurācija                              | [Čeku drukāšanas formāts.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Uzņēmuma logo attēls                                   | [Uzņēmuma logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Paraksta attēls                                      | [Paraksta attēls.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatīva paraksta attēls                          | [Paraksta attēls 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word veidne maksājumu čeku drukāšanai  | [Čeka veidne Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a>pārbaudiet priekšnoteikumus;  
 1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.  
 2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".   
 3. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.  
 
## <a name="add-a-new-er-model-configuration"></a>Pievienot jaunu ER modeļa konfigurāciju  
 1. Tā vietā, lai izveidotu jaunu modeli, varat ielādēt ER modeļa konfigurācijas failu (Model for cheques.xml), kuru saglabājāt iepriekš. Šis fails satur parauga datu modeli maksājumu čekiem un datu modeļa kartējumu uz programmas Dynamics 365 for Operations datu komponentiem.   
 2. Kopsavilkuma cilnē Versijas noklikšķiniet uz Mainīt.   
 3. Noklikšķiniet uz Ielādēt no XML faila.  
 4. Noklikšķiniet uz Pārlūkot un pēc tam atlasiet Model for cheques.xml.   
 5. Noklikšķiniet uz OK.  
 6. Ielādētais modelis tiks izmantots kā datu avots informācijai, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.  

## <a name="add-a-new-er-format-configuration"></a>Jaunas ER formāta konfigurācijas pievienošana  
 1. Tā vietā, lai izveidotu jaunu formātu, varat ielādēt ER formāta konfigurācijas failu (Cheques printing format.xml), kuru saglabājāt iepriekš. Šis fails satur formāta parauga izkārtojumu, lai izdrukātu čekus, izmantojot iepriekš izdrukātu formu un šī formāta kartējumu uz datu modeli 'Čeku modelis'.   
 2. Noklikšķiniet uz Mainīt.  
 3. Noklikšķiniet uz Ielādēt no XML faila.  
 4. Noklikšķiniet uz Pārlūkot un atlasiet failu Cheques printing format.xml.   
 5. Noklikšķiniet uz OK.  
 6. Koka struktūrā izvērsiet “Čeku modelis”.  
 7. Kokā atlasiet 'Model for cheques\Cheques printing format'.  
 8. Ielādētais formāts tiks izmantots, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.   

## <a name="configure-er-user-parameters"></a>ER lietotāju parametru konfigurēšana  
 1. Darbību rūtī noklikšķiniet uz Konfigurācijas.  
 2. Noklikšķiniet uz Lietotāja parametri.  
 3. Laukā Palaist iestatījumus atlasiet Jā.  
  Ieslēdziet karodziņu 'Palaist melnrakstu', lai startētu atlasītā formāta melnraksta versiju, nevis pabeigto.  
 4. Noklikšķiniet uz OK.  

## <a name="configure-cash--bank-management-parameters"></a>Kases un bankas vadības parametru konfigurēšana  
 1. Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.  
 2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.  
 3. Darbību rūtī noklikšķiniet uz Iestatīt.  
 4. Noklikšķiniet uz Pārbaudīt.  
 5. Izvērsiet sadaļu Iestatīšana.  
 6. Noklikšķiniet uz Rediģēt.  
 7. Laukā Uzņēmuma logotips atlasiet Jā.  
 8. Noklikšķiniet uz Uzņēmuma logotips.  
 9. Noklikšķiniet uz Mainīt.  
 10. Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Company logo.png.   
 11. Noklikšķiniet uz Saglabāt.  
 12. Aizvērt lapu.  
 13. Izvērsiet sadaļu Paraksts.  
 14. Laukā Drukāt pirmo parakstu atlasiet Jā.  
 15. Noklikšķiniet uz Mainīt.  
 16. Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image.png.   
 17. Izvērsiet sadaļu Kopijas.  
 18. Laukā Ūdenszīme atlasiet opciju.  
 19. Laukā Vispārīgs elektroniskās eksportēšanas formāts atlasiet Jā.  
 20. Atlasiet konfigurāciju “Čeku drukāšanas forma”.  
 21. Tagad atlasītais ER formāts tiks izmantots čeku drukāšanai.  
 22. Noklikšķiniet uz Pievienot.  
 23. Noklikšķiniet uz Jauns.  
 24. Noklikšķiniet uz Fails.  
 25. Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image 2.png.   
 26. Aizvērt lapu.  
 27. Aizvērt lapu.  
 28. Aizvērt lapu.  
 29. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.  
 30. Laukā Atļaut darījuma pārbaudes izveidi neaktīviem bankas kontiem atlasiet Jā.  
 31. Noklikšķiniet uz Saglabāt.  
 32. Aizvērt lapu.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
