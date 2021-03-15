---
title: Lean manufacturing darba šūnu definēšana
description: Darba šūna ir specifiska resursu grupu forma, kuru var izmantot lean manufacturing procesa aktivitātēs.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96c65690b7d67bffc2cf09c4ea34c84755f8530a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001553"
---
# <a name="define-lean-manufacturing-work-cells"></a>Lean manufacturing darba šūnu definēšana

[!include [banner](../../includes/banner.md)]

Darba šūna ir specifiska resursu grupu forma, kuru var izmantot lean manufacturing procesa aktivitātēs. Darba šūnām ir ievades un izvades vietas un noslodzes definīcija, pamatojoties uz ražošanas plūsmas modeli. Lai uzzinātu vairāk par lean manufacturing darba šūnu pamatkonceptiem un noslodzes aprēķiniem, skatiet tehniskos dokumentus par Lean manufacturing. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF


## <a name="create-a-work-cell"></a>Izveidojiet darba šūnu. 
1. Dodieties uz Organizācijas administrēšana > Resursi > Resursu grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Resursu grupa ierakstiet kādu vērtību.
    * Darba šūnas ID ir sistemātisks kods, un tam jābūt unikālam attiecīgajai juridiskajai personai.  
4. Apraksta laukā ierakstiet vērtību.
    * Apraksts ietver darba šūnas nosaukumu vai virsrakstu.  
5. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Darba šūna atrodas vienā noteiktā vietā. Gan ievades un izvades noliktavai, gan arī novietojumam jāatrodas šajā vietā.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Laukā Ražošanas vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet ražošanas vienību, kurai pieder šī darba šūna.  
9. Atzīmējiet izvēles rūtiņu Darba šūna.
    * Lai izmantotu resursu grupu kā lean manufacturing darba šūnu, ir jābūt atzīmētai izvēles rūtiņai Darba šūna.  Ņemiet vērā, ka šo rekvizītu nevar mainīt pēc resursu grupas izveidošanas.  
10. Laukā Ievades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Attiecībā uz uzskaiti un materiālu kontroli materiāli, kas atrodas ražotnē, parasti tiek iekļauti noteiktā virtuālajā noliktavā. Tomēr, ja vēlaties papildināt novietojumus, izmantojot noliktavas darbu, tiem jāietilpst saņemšanas izejmateriālu noliktavā.  
12. Laukā Ievades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Ievērojiet, ka procesa aktivitātei ievades vieta var tikt pārrakstīta vispārēji vai noteiktai precei vai preces variantam, definējot izdošanas darbības, kas tiek iekļautas procesa aktivitātē. Darba šūnas ievades vietas nedrīkst būt atkarīgas no numura zīmes.  
14. Laukā Izvades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Vairākās aktivitātes ražošanas plūsmās vai ražošanas rindās tā bieži vien ir nākamās darba šūnas ievades noliktava vai pārdošanas vai tranzīta noliktava, uz kuru prece parasti tiek nosūtīta pēc ražošanas procesa. Atcerieties, ka, modelējot lean manufacturing procesus, transports parasti ir uzskatāms par atkritumiem, kā arī transporta iekļaušana pārskatos.  
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Laukā Izvades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Ražošanas plūsmā ar vairākām procesa aktivitātēm tā bieži vien ir nākamās darba šūnas ievades vieta.  
18. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
19. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
20. Izvērsiet vai sakļaujiet sadaļu Operācija.
    * Ir jānorāda Izpildes laika kategorija, lai iespējotu racionālo Kanban darbu izmaksu aprēķinu un apstrādi.  
21. Laukā Izpildes laika kategorija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
22. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Izpildes laika izmaksu kategorija tiek izmantota standarta izmaksu aprēķināšanā un atgriezeniskā izmaksu aprēķināšanā.  
23. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
24. Izvērsiet vai sakļaujiet sadaļu Kalendāri.
25. Noklikšķiniet uz Pievienot.
26. Laukā Kalendārs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
27. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Parasti noteiktas vietas darba šūnas izmanto vienu darba laika kalendāru. Ja darba šūnām var būt atsevišķi darba laiki, darba šūnai var būt nepieciešams izveidot īpašu darba laika kalendāru. Ņemiet vērā, ka kalendārā jābūt definētam standarta darba laikam, izmantojot to lean manufacturing darba šūnai, jo noslodzes definīcija parasti ir saistīta ar darba dienas standarta darba laiku.  
28. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
29. Izvērsiet vai sakļaujiet sadaļu Darba šūnas noslodze.
30. Noklikšķiniet uz Pievienot.
31. Laukā Ražošanas plūsmas modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
32. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šai procedūrai ir nepieciešams ražošanas plūsmas modeļa tips Caurlaide, lai parādītu caurlaides noslodzes definīciju.  
33. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
34. Laukā Noslodzes periods atlasiet opciju.
    * Iespēju klāstā ietilpst: Standarta darbdiena — noslodze tiek izteikta ar darba laika kalendāra standarta darbdienas garumu darba šūnai. Katrai dienai kalendārā tiek noteikts faktiskais darba laiks un, pamatojoties uz šiem datiem, tiek aprēķināta faktiskā pieejamā noslodze.   Nedēļa — atļauj nedēļas noslodzi. Netiek veikta korekcija, izmantojot faktisko darba laiku.   Mēnesis — atļauj mēneša noslodzi. Netiek veikta korekcija, izmantojot faktisko noslodzi.   Parasti standarta darbdiena tiek izmantota dienas periodiem, un nedēļas noslodze tiek izmantota nedēļas noslodzes periodiem.  
35. Laukā Vidējais caurlaides daudzums ievadiet skaitli.
    * Ņemiet vērā, ka racionālā operācija nekad netiek veidota maksimālajai iespējamajai noslodzei ideālos apstākļos. Tā vietā noslodze vienmēr ir jādefinē operācijām tipiskos apstākļos.  
36. Laukā Vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
37. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
38. ResolveChanges vienumam Vienība.

## <a name="add-a-financial-dimension"></a>Finanšu dimensijas pievienošana
1. Izvērsiet vai sakļaujiet sadaļu Finanšu dimensijas.
    * Ņemiet vērā, ka ražošanas plūsmā definētās finanšu dimensijas ignorē noteiktas darba šūnas finanšu dimensiju.    Atlasei pieejamās finanšu dimensijas ir atkarīgas no jūsu sistēmas finanšu dimensijām. Tālāk minētie soļi atbilst demonstrācijas datu kopai uzņēmumā USMF. Izmantojot atšķirīgus datus, soļi var nebūt pielietojami.  
2. Laukā CostCenter noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Dimensijas, kas ir jāatlasa lean manufacturing darba šūnām, ir atkarīgas no finanšu dimensiju ieviešanas uzskaites modelī noteiktai juridiskajai personai.  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā ItemGroup noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="save"></a>Saglabāt
1. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]