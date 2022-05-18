---
title: Konfigurēt prasmes
description: Varat izsekot darbinieka prasmes programmā Dynamics 365 Human Resources. Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7c853ad71aecd7f5d214c02da97f7956ff2391df
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695961"
---
# <a name="configure-skills"></a>Prasmju konfigurēšana

> [!IMPORTANT]
> Šajā tēmā atzīmētā funkcionalitāte pašlaik finanšu infrastruktūras personāla vadības debitoriem ir pieejama.  


Varat izsekot darbinieka prasmes programmā Dynamics 365 Human Resources. Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.

Izsekojamo prasmju piemēri ietver:

- Supervizora — spēja uzraudzīt citu darbu.
- Vadības — spēja vadīt darbiniekus un uzņēmuma domēnus.
- Plānošanas — spēja raudzīties nākotnē, formulēt redzējumu paziņojumus un īstenot tos dzīvē.
- HTML — spēja rakstīt HTML kodu.

Ja vēl neesat iestatījis prasmju tipus un novērtējuma modeļus, daži ir jāpievieno pirms prasmju izveides.

Tālāk norādītās personas var ievadīt darbinieka prasmes:

- Darbinieki var ievadīt prasmes paši Darbinieku pašapkalpošanās sistēmā. Šīm prasmēm nepieciešams vadītāja apstiprinājums.
- Vadītāji var ievadīt darbinieku prasmes. Varat izveidot darbplūsmu, kas automātiski apstiprina šīs prasmes.

## <a name="create-a-skill-type"></a>Prasmes tipa izveide

Prasmju tipi ir kategorijas, kurās ietilpst atsevišķas prasmes, piemēram, Administrēšana vai Pārdošana.

1. **Darbinieku attīstības** darbvietā atlasiet **Saites**.

2. Zem **Kompetences iestatījumiem** atlasiet **Prasmju tipi**.

3. Atlasiet **Jauns**.

4. Aizpildiet tālāk aprakstītos laukus:

   - **Prasmju tips**: ievadiet prasmju tipa nosaukumu.
   - **Apraksts**: ievadiet prasmju tipa aprakstu.

5. Atlasiet **Saglabāt**.

## <a name="create-a-rating-model"></a>Izveidot vērtēšanas modeli

Vērtēšanas modeļi palīdz novērtēt personas faktisko prasmju līmeni, to prasmju līmeni, ko šai personai būtu jācenšas sasniegt, vai prasmju līmeni, kas ir nepieciešams darbam. Katram līmenim vērtēšanas modelī tiek piešķirts koeficients.

1. **Darbinieku attīstības** darbvietā atlasiet **Saites**.

2. Zem **Kompetences iestatījumiem** atlasiet **Vērtēšanas modeļi**.

3. Atlasiet **Jauns**.

4. Aizpildiet tālāk aprakstītos laukus:

   - **Vērtējums**: ievadiet vērtēšanas modeļa nosaukumu, piemēram, **Prasmes**.
   - **Apraksts**: ievadiet vērtēšanas modeļa aprakstu, piemēram, **Prasmju novērtējumi**.

5. Sadaļā **Līmeņi** atlasiet **Jauns**. Katram līmenim, kuru vēlaties pievienot, aizpildiet šādus laukus:

   - **Līmenis**: ievadiet līmeņa nosaukumu.
   - **Apraksts**: ievadiet līmeņa aprakstu.
   - **Koeficients**: ievadiet koeficienta vērtību no 0 līdz 9. Koeficienti palīdz normalizēt rādītājus prasmēm, kas izmanto dažādu vērtēšanas modeļus. Katram līmenim jābūt unikālam koeficentam. Līmeņiem ar augstākām koeficienta vērtībām ir lielāka nozīme vērtēšanas modelī.

   Ja nepieciešams, turpiniet pievienot līmeņus. Katram vērtējuma modelim var ievadīt ne vairāk kā 10 līmeņus.

6. Atlasiet **Saglabāt**.

## <a name="create-a-skill"></a>Prasmes izveide

Lai varētu piešķirt kādu prasmi vai izveidot prasmju kartēšanas meklēšanu vai prasmju profilu, par šīm prasmēm ir jāievada informācija lapā **Prasmes**. Katrai prasmei varat atlasīt prasmju tipu un vērtēšanas modeli.

1. **Darbinieku attīstības** darbvietā atlasiet **Saites**.

2. Zem **Kompetences iestatījumiem** atlasiet **Prasmes**.

3. Atlasiet **Jauns**.

4. Aizpildiet tālāk aprakstītos laukus:

   - **Prasme**: ievadiet prasmes nosaukumu.
   - **Apraksts**: ievadiet prasmes aprakstu.
   - **Vērtējums**: atlasiet vērtējuma modeli, ko vēlaties izmantot šai prasmei.
   - **Prasmes tips**: atlasiet no prasmju tipu saraksta.

5. Atlasiet **Saglabāt**.

## <a name="see-also"></a>Skatiet arī

[Ievadīt prasmes](hr-develop-enter-skills.md)<br>
[Kartēt prasmes](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
