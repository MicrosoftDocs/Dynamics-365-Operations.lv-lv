---
title: Paziņojums par atvieglojumiem
description: Atvieglojumu pārskata pārskats izskaidro darbiniekam pašlaik reģistrētos atvieglojumus.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 46f7358684502a4bf05854fbcb5cca9a1eb2c87c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548059"
---
# <a name="benefit-statement"></a>Paziņojums par atvieglojumiem

**Atvieglojumu pārskata** pārskats izskaidro darbiniekam pašlaik reģistrētos atvieglojumus. Pārskatam var piekļūt darbinieks tieši vai atvieglojumu administrators. **Atvieglojumu pārskats** sniedz sarakstu ar darbinieka reģistrētajiem atvieglojumiem, vajadzības opcijām, izmaksām un visiem reģistrētajiem apgādājamajiem vai saņēmējiem. Pārskatu var drukāt vienam vai vairākiem darbiniekiem.

> [!NOTE]
Darbvietā **Līdzekļu pārvaldība** ir jāiespējo līdzeklis **Atvieglojumu pārskats**. Lai to paveiktu, Līdzekļu pārvaldībā jābūt ieslēgtam **Atvieglojumu pārvaldības** līdzeklim. 


## <a name="importing-the-benefit-statement"></a>Atvieglojumu pārskata importēšana 

Pirms **Atvieglojumu pārskats** ir pieejams, jums jāimportē **Atvieglojumu pārskats**, izmantojot pārskata konfigurāciju. Lai to paveiktu, veiciet tālāk norādītās darbības:

1.  Dodieties uz **Sistēmas administrēšanas** darbvietu.

2.  Atlasiet elementu **Elektroniskie pārskati**.

3.  Dodieties uz **Konfigurācijas nodrošinātājiem** un atlasiet **Repozitorijui**.

  ![Atlasiet Repozitoriji.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Sarakstā atlasiet **HR resursi** un pēc tam atlasiet **Atvērt**.

    ![Konfigurācijas repozitoriji.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Atlasiet **Atvieglojumu pārskata modeli** kreisajā rūtī un izvērsiet to, lai tiktu parādīts **Atvieglojumu pārskata formāts**.

6.  Atlasiet **Atvieglojumu pārskata formātu** kreisajā rūtī.

7.  Ekrāna labajā pusē būs kopsavilkuma cilne **Versijas**. Atlasiet **Importēt**.

    ![Kopsavilkuma cilne Versijas.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Ģenerēt Atvieglojumu pārskatu kā PDF failu

Pēc noklusējuma **Atvieglojumu pārskats** tiks drukāts kā Microsoft Word dokuments. Lai drukātu PDF formātā, **Elektronisko pārskatu adresātā** jākonfigurē PDF opcija . 

1. Lai to izdarītu, dodieties uz **Sistēmas administrēšanas darbvietu** > **Elektroniskie pārskati** > **Saistītās saites** > **Elektronisko pārskatu adresāts**.

1.  Atlasiet **Jauns**.

2.  Laukā **Atsauce** atlasiet formātu **Atvieglojumu pārskata formāts**.

3.  Kopsavilkuma cilnē **Faila adresāts** atlasiet **Jauns**.

4.  Laukā **Nosaukums** ievadiet **Atvieglojumu pārskats PDF**.

5.  Laukā **Faila komponenta nosaukums** ievadiet vai atlasiet **Atvieglojumu pārskats**.

6.  Atlasiet izvēles rūtiņu , lai **Pārveidotu par PDF**.

7.  Atlasiet **Iestatījumi** no izvēlnes elementa. 

    ![Faila adresāts.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Atlasiet kopsavilkuma cilni **Fails** un pēc tam atlasiet **Iespējots**.

9.  Atlasiet **Labi**.
   
> [!NOTE]
> Atvieglojumu pārvaldības līdzeklis ir priekšskatījumā. Ir zināms problēma, izmantojot e-pasta adresāta iestatījumu **Elektronisko pārskatu adresāta** pārskatā. Iespējams, ka saņemsit kļūdas ziņojumu, un e-pasta ziņojumu nevar nosūtīt.

**Atvieglojumu pārskatu** var ģenerēt no šādām lapām:

-   **Atvieglojumu pārvaldības darbvieta** > **Saites** > **Pārskati** > **Atvieglojumu pārskats**

-   **Darbinieki (mantojuma forma)** > **Personiskās informācijas cilne** > **Atvieglojumu pārskats**

-   **Racionalizēta darbinieka ieraksts** > **Atvieglojumu pārskati** > **Atvieglojumu pārskats**

-   **Darbinieka pašapkalpošanās** > **Atvieglojumi** > **Skatīt atvieglojumu pārskatu**

> [!NOTE]
>  Piekļuvi **Atvieglojumu pārskatam** **Darbinieku pašapkalpošanās** sadaļā kontrolē privilēģija **Skatīt atvieglojumu pārskatu**. Tas ir **Darbinieku pašapkalpošanās atvieglojumu** pienākums. Šī privilēģija darbiniekiem tiek piešķirta pēc noklusējuma.

## <a name="report-contents"></a>Pārskata saturs

**Atvieglojumu pārskats** drukā darbinieka apstiprināto plānu atlases, ieskaitot visus atceltos plānus. Tālāk redzamajā attēlā parādīts pārskata piemērs. 

![Pārskats par atvieglojumu pārskatu.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Pārskatā tiks parādīts **Plāns**, **Vajadzības opcijas**, **Darbinieka izmaksas** un **Darba devēja izmaksas**. Pārskatā tiks iekļauti arī visi segtie apgādājamie. Ja plānā tam ir piesaistīti saņēmēji, tiek parādīta saņēmēja un to sadales prioritāte un procenti.

**Atvieglojumu pārskata** pārskatu var izdrukāt vairākiem darbiniekiem vienlaicīgi, izmantojot **Iekļaujamos ierakstus**, lai kopsavilkuma cilni iekļautu **Atvieglojumu pārskata** lapā.
