---
title: Preces konfigurācijas modeļa izveide
description: Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568428"
---
# <a name="create-a-product-configuration-model"></a>Preces konfigurācijas modeļa izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.


## <a name="create-a-product-model"></a>Preču modeļa izveide

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Atlasiet **Jauns**.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Laukā **Risinātāja stratēģija** atlasiet opciju.
    * Risinātāja stratēģija nosaka, kā ierobežojumi tiek apstrādāti ierobežojumam atbilstošā preces konfigurācijas modelī. Šī atlase var ietekmēt preces konfigurācijas modeļa veiktspēju.  
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
    * Saknes komponents norāda preces konfigurācijas modeli, bet to var izmantot arī citos preču modeļos.  
1. Atlasiet **Labi**.
1. Laukā **Atkārtoti izmantot konfigurācijas** atlasiet opciju.
    * Ja parametram Atkārtoti izmantot konfigurācijas ir iestatīta opcija Jā, sistēma meklēs identiskas konfigurācijas pēc katras konfigurācijas sesijas un atkārtoti tās izmantos, ja tiks atrasta precīza atbilstība.  

## <a name="add-attributes"></a>Pievienot atribūtus

1. Izvērsiet sadaļu **Atribūti**.
2. Atlasiet **Pievienot**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Risinātāja nosaukums** ierakstiet vērtību.
    * Risinātāja nosaukumu izmanto preču konfiguratora ierobežojumu risinātājs. Tajā nedrīkst būt atstarpes vai īpašas rakstzīmes, izņemot _ (pasvītrojums).  
6. Laukā **Apraksts** ierakstiet kādu vērtību.
    * Apraksta teksts tiek rādīts konfigurācijas lietotājam un tādējādi var palīdzēt, izvēloties atbilstošo atribūta vērtību.  
7. Laukā **Atribūta veids** ievadiet vai atlasiet kādu vērtību.
    * Atribūta tips nosaka, kādas vērtības ir pieejamas atribūtam.  
8. Atzīmējiet izvēles rūtiņu **Iekļaut atkārtotā izmantošanā**.
    * Šī iespēja pieejama tikai tad, ja ir atlasīta opcija Atkārtoti izmantot konfigurācijas. Atribūta iekļaušana atkārtotas izmantošanas izvēles rūtiņā nozīmē, ka šis atribūts tiks ņemts vērā, kad sistēma meklē precīzu atbilstību.  

## <a name="add-subcomponents"></a>Apakškomponentu pievienošna

1. Izvērsiet sadaļu **Apakškomponenti**.
2. Atlasiet **Pievienot**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Risinātāja nosaukums** ierakstiet vērtību.
6. Laukā **Apraksts** ierakstiet kādu vērtību.
7. Laukā **Komponents** ievadiet vai atlasiet kādu vērtību.
    * Katram apakškomponentam jābūt atsaucei uz komponenta definīciju. Šāds noformējums atbalsta atkārtoti izmantojamus komponentus un nodrošina, ka pēc komponenta definēšanas to var izmantot daudzos preču modeļos.  
8. Atlasiet **Saglabāt**.
9. Atlasiet **Detalizēta MK rindas informācija**.
    * Veidlapa Detalizēta informācija par MK rindu ļauj lietotājam izvēlēties obligātos rekvizītus apakškomponentam. Katram rekvizītam var piešķirt fiksētu vērtību, vai to var kartēt uz atribūtu. Kartēšanas uz atribūtu rezultātā MK rindas rekvizītam būs atšķirīgas vērtības atkarībā no konfigurācijas atlases.  
10. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
    * Katrs apakškomponents pārstāv konfigurējamu preces šablonu ar konfigurācijas atbilstoši ierobežojumam tehnoloģiju. Atsaucei tiek izmantots krājuma kods.  
11. Atzīmējiet izvēles rūtiņu **Iestatīt**.
12. Laukā **Aprēķins** atlasiet **Jā**.
    * Aprēķina opcijas iestatīšana nodrošina, ka prece tiks iekļauta, veicot preces izmaksu aprēķinu.  
13. Atlasiet cilni **Iestatījums**.
14. Atzīmējiet izvēles rūtiņu **Iestatīt**.
15. Laukā **Daudzums** ierakstiet kādu skaitli.
    * Daudzuma lauks nosaka, kāds šīs preces dadzums tiks patērēts konfigurētajai precei.  
16. Atzīmējiet izvēles rūtiņu **Iestatīt**.
17. Ievadiet skaitli laukā **Pa sērijām**.
18. Atlasiet **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]