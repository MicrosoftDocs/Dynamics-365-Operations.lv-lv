---
title: Piegādātāja konta izveidošana
description: Šajā procedūrā parādīts, kā izveidot kreditora kontu un pievienot adresi un kontaktinformāciju.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aca23db2a0cc86a2c12ea74d3b1e491643b7efec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207696"
---
# <a name="create-a-vendor-account"></a>Piegādātāja konta izveidošana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot kreditora kontu un pievienot adresi un kontaktinformāciju. Procedūrā netiek parādīts, kā aizpildīt visus laukus iepirkuma un finanšu mērķiem. Lai uzzinātu vairāk par šiem laukiem, lūdzu, izlasiet lauku aprakstus. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Kreditoru kontus parasti izveido sagādes speciālists vai debitoru parādu personāls.


## <a name="create-a-vendor-account"></a>Kreditora konta izveide
1. Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** ierakstiet vērtību.
    - Vērtībā var tikt ierakstīta automātiski. Ja tā, varat izlaist šo darbību.  
    - Varat izveidot kreditora kontus personai vai organizācijai. Tas ietekmēs, kādi lauki ir pieejami. Šajā piemērā mēs izveidosim kreditora kontu kādai organizācijai.   
4. Ievadiet vai atlasiet vērtību laukā **Nosaukums**. Ja kreditors ir jau reģistrēts jūsu sistēmā, var izmantot nolaižamo sarakstu un atlasīt to šajā laukā un jauns kreditora konts pārmantos jau reģistrētā konta adresi un kontaktinformāciju.
5. Laukā **Grupa** ievadiet vai atlasiet kādu vērtību. Kreditoru grupa tiek izmantota, lai grupētu kreditorus, kuriem ir kopīgs kāds no šiem parametriem: apmaksas nosacījumi, apmaksas termiņš, krājumu grāmatošanas virsgrāmatas konti — tostarp pārdošanas nodokļa grupa, noklusējuma virsgrāmatas konti, preču filtra kodi vai piegādes apjoma prognozes konfigurācija.
6. Laukā **Darbinieku skaits** ierakstiet kādu skaitli.
7. Laukā **Organizācijas numurs** ierakstiet vērtību.

## <a name="add-an-address"></a>Adreses pievienošana
1. Izvērsiet sadaļu **Adreses**.
2. Noklikšķiniet uz **Pievienot**.
3. Laukā **Nolūks** ievadiet vai atlasiet kādu vērtību. Varat atzīmēt vienu vai vairākus nolūkus. Tie tiek izmantoti, lai atlasītu pareizo adresi konkrētam nolūkam. Piemēram, ja nolūks ir "Rēķins", šī adrese tiks izmantota, sūtot rēķinus.
4. Laukā **Nosaukums vai apraksts** ierakstiet vērtību.
5. Laukā **Valsts/reģions** ievadiet vai atlasiet kādu vērtību. Ievadiet adreses detaļas. Atlasītā valsts/reģions noteiks laukus, kuri tiks piedāvāti, atbilstoši valsts/reģiona adreses formātam. 
6. Noklikšķiniet uz **Labi**.

## <a name="add-contact-information"></a>Kontaktinformācijas pievienošana
1. Izvērsiet sadaļu **Kontaktinformācija**.
2. Noklikšķiniet uz **Pievienot**.
3. Laukā **Apraksts** ierakstiet kādu vērtību.
4. Atlasiet opciju laukā **Tips**.
5. Ierakstiet vērtību laukā **Kontaktpersonas tālrunis/adrese**. Varat atzīmēt izvēles rūtiņu Primārs, ja šī ir primārā kontaktpersona.  
6. Noklikšķiniet uz **Saglabāt**.
7. Aizvērt lapu.
8. Aizvērt lapu.

