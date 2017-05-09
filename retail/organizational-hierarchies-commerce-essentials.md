---
title: "Organizācijas un organizāciju hierarhijas (modulis Komercijas rekvizīti)"
description: "Modulī Komercijas rekvizīti ir pieejami trīs iekšējo organizāciju veidi, ko var definēt, lai palīdzētu organizācijai veikt biznesa procesu vai sasniegt mērķi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 93711977ad8d861ca75ba80ee542ee112c8ddd2f
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organizācijas un organizāciju hierarhijas (modulis Komercijas rekvizīti)

[!include[banner](includes/banner.md)]


Modulī Komercijas rekvizīti ir pieejami trīs iekšējo organizāciju veidi, ko var definēt, lai palīdzētu organizācijai veikt biznesa procesu vai sasniegt mērķi. 

Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi. Organizācijas hierarhija formulē attiecības starp biznesa vienībām, kas veido jūsu organizāciju.

## <a name="organizations"></a>Organizācijas
Programmā Komercijas rekvizīti var definēt trīs iekšējo organizāciju veidus: juridiskas personas, pārvaldības struktūrvienības un komandas. Programmā Microsoft Dynamics AX visām iekšējām organizācijām ir piešķirts tips Puses elements. Tāpēc šīs organizācijas izmanto adrešu grāmatu, lai saglabātu adreses un citu kontaktinformāciju. Puse var būt persona vai organizācija, un tā var piederēt vienai vai vairākām adrešu grāmatām.
### <a name="legal-entities"></a>Juridiskas personas

Juridiskā persona ir organizācija, kurai ir reģistrēta vai likumā noteikta juridiskā struktūra. Juridiskas personas var noslēgt juridiskos līgumus, un tām ir nepieciešams sagatavot pārskatus, lai ziņotu par savu veiktspēju. Uzņēmums programmā Microsoft Dynamics AX ir juridiskas personas tips, un katra juridiskā persona ir saistīta ar uzņēmuma ID. Šī saistība pastāv tāpēc, ka uzņēmuma ID vai DataAreaId izmanto daži datu modeļi, kuros uzņēmumi tiek izmantoti kā datu drošības ierobežojošs kritērijs. Lietotāji var piekļūt tikai tā uzņēmuma datiem, kurš ir pašlaik pieteicies sistēmā.

### <a name="operating-units"></a>Pārvaldības struktūrvienības

Pārvaldības struktūrvienība ir organizācija, kas tiek lietota, lai sadalītu ekonomisko resursu un operatīvo procesu kontroli biznesā. Cilvēkiem pārvaldības struktūrvienībā ir pienākums maksimāli izmantot ierobežotos resursus, uzlabot procesus un atskaitīties par savu sniegumu. Programmā Komercijas rekvizīti pārvaldības struktūrvienību veidi ietver izmaksu centrus, biznesa vienības, vērtību plūsmas nodaļas un mazumtirdzniecības kanālus. Tabulā ir sniegta papildinformācija par katru pārvaldības struktūrvienības veidu.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Pārvaldības struktūrvienības tips** | **Apraksts**                                                                         | **Mērķis**                                                                                                                                 |
| Biznesa vienība           | Pusautonoma pārvaldības struktūrvienība, kura tiek izveidot, lai izpildītu stratēģiskus biznesa mērķus. | Izmantojiet biznesa vienības finanšu pārskatiem, kas attiecas uz nozari vai preču rindu, ko organizācija nodrošina juridiskām personām. |
| Mazumtirdzniecības kanāls          | Pārvaldības struktūrvienība, kas formulē fiziska veikala esamību.                             | Izmantojiet, lai pārvaldītu un kontrolētu vienas vai visu juridisko personu vienu vai vairākus veikalus.                                                               |

## <a name="organizational-hierarchies"></a>Organizācijas hierarhijas
Programmā Komercijas rekvizīti katrai hierarhijai tiek piešķirts nolūks. Hierarhijas mērķis nosaka organizāciju veidus, ko var iekļaut hierarhijā. Mērķis nosaka arī pielietojuma scenārijus, kuros hierarhiju var izmantot. Piemēram, mazumtirdzniecības hierarhiju var izmantot, lai pirktu un pārdotu preces mazumtirdzniecības veikalā. Organizācijas hierarhijā var koplietot parametrus, politiku un transakcijas. Organizācija var mantot vai ignorēt savas pamatorganizācijas parametrus. Tomēr koplietojamie pamatdati, piemēram, preces un adrešu grāmatas, attiecas uz visu organizāciju un tos nevar ignorēt atsevišķu organizāciju gadījumā.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Piemērotākā prakse organizācijas hierarhijas iestatīšanai

Ieviešot organizācijas hierarhiju, ņemiet vērā šādu labāko praksi:
-   Izveidojiet nodaļu, lai definētu juridisko personu un biznesa vienību krustpunktus. Tad varat apvienot datus no nodaļas uz juridisko personu ar likumu noteikto pārskatu vajadzībām un no nodaļas uz biznesa vienību iekšējo pārskatu vajadzībām.
-   Nenosakiet vairākas hierarhijas ar vienādu hierarhijas nolūku vienas juridiskās personas robežās.
-   Neveidojiet katra nolūka hierarhiju. Parasti varat izmantot vienu hierarhiju vairākiem nolūkiem. Piemēram, vienu pārvaldības struktūrvienību hierarhiju var piešķirt visiem ar politiku saistītajiem nolūkiem.
-   Veidojiet līdzsvarotas hierarhijas. Visi hierarhijas zari, kas ir vienādā attālumā no saknes zara, tiek definēti ka līmenis. Līdzsvarotā hierarhijā katrā līmenī var būt tikai viens pārvaldības struktūrvienības veids, un attālums no saknes zara līdz katram līmenim ir nemainīgs. Ja starp nodaļu un juridisko personu vai biznesa vienību ir starpposma līmeņi, līdzsvarotas hierarhijas izveidei var būt nepieciešamas viettura organizācijas.
-   Neveidojiet atsevišķu pārvaldības struktūrvienību hierarhiju, ja juridisko personu struktūra ir arī jūsu darba struktūra. Jaukta juridisko personu un pārvaldības struktūrvienību hierarhija var kalpot abiem nolūkiem.
-   Pirms nopietnu restrukturizācijas scenāriju noteikšanas, izmantojiet hierarhijas spēkā stāšanās datumus, lai veiktu ietekmes analīzi un apstiprināšanas pārbaudi.
-   Saglabājiet hierarhiju kā uzmetumu, ja pirms tās publicēšanas ir jāveic izmaiņas.
-   Ierobežojiet cilvēku skaitu, kam ir atļaujas pievienot vai noņemt organizācijas no hierarhijas ražošanas vidē. Mazāks skaits samazina iespēju, ka var rasties dārgas kļūdas un ir jāveic labojumi.

## <a name="retail-store-management"></a>Mazumtirdzniecības veikala pārvaldība
Tālāk norādītajā tabulā ir aprakstīti programmas Komercijas rekvizīti scenāriji, kuros var izmantot organizācijas hierarhijas.
| Uzdevums                                                                           | Apraksts                                                                                                                                                                                                                                                                                                | Hierarhijas nolūks    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Mazumtirdzniecības preču klāsta pārvaldība                                                      | Norādiet preces, kas ir pieejamas visos mazumtirdzniecības veikalos.                                                                                                                                                                                                                                             | Mazumtirdzniecības preču klāsts    |
| Mazumtirdzniecības papildināšanas pārvaldība                                                    | Grupējiet veikalus, lai papildinātu krājumus atbilstoši papildināšanas nosacījumiem.                                                                                                                                                                                                                                          | Mazumtirdzniecības papildināšana |
| Veikalu pārskata dati                                                         | Grupējiet veikalus pārskatiem.                                                                                                                                                                                                                                                                                | Mazumtirdzniecības pārskati     |
| Krājumu grāmatošana, aprēķinu veikšana vai pārskatu grāmatošana veikalu grupai | Izveidojiet veikalu grupu, ko var piešķirt pakešuzdevumam. Definējot pakešuzdevumu krājumu grāmatošanai, aprēķinu veikšanai vai pārskatu grāmatošanai, varat norādīt, uz kuru hierarhiju attiecas darbs. Kad veikali ir pievienoti hierarhijai vai noņemti no tās, jums nav jāmaina pakešuzdevums. | Mazumtirdzniecības POS grāmatošana   |






