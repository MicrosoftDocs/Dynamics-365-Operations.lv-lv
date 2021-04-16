---
title: Saskaņot bankas izrakstus, izmantojot detalizēto bankas darbību saskaņošanu
description: Līdzeklis Detalizētā bankas darbību saskaņošana sniedz iespēju importēt elektroniskus bankas izrakstus un tos automātiski saskaņot ar bankas transakcijām programmā Microsoft Dynamics 365 Finance. Šajā tēmā ir paskaidrots šis saskaņošanas process.
author: saraschi2
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e5b097d667186a849b23814917d0d6f837c25de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835008"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Saskaņot bankas izrakstus, izmantojot detalizēto bankas darbību saskaņošanu

[!include [banner](../includes/banner.md)]

Līdzeklis Detalizētā bankas darbību saskaņošana sniedz iespēju importēt elektroniskus bankas izrakstus un tos automātiski saskaņot ar bankas transakcijām programmā Dynamics 365 Finance. Šajā tēmā ir paskaidrots šis saskaņošanas process.  

<a name="import-an-electronic-bank-statement"></a>Importēt elektronisku bankas izrakstu
-----------------------------------

Bankas izrakstus varat importēt, izmantojot darbību **Importēt izrakstu** lapā **Bankas izraksti**. Bankas konts tiek identificēts bankas izrakstā, izmantojot bankas konta rekvizītos iestatīto vērtību kombinācijas. Šīs vērtības ietver bankas nosaukumu, bankas konta numuru, maršrutēšanas numuru, Pasaules Starpbanku finanšu telekomunikāciju sabiedrības (Society for Worldwide Interbank Financial Telecommunication — SWIFT) kodu un starptautisko bankas konta numuru (International Bank Account Number — IBAN). 

Varat augšupielādēt bankas izrakstu, kurā ir informācija par vienu vai vairākiem kontiem. Ja ir vairāki konti, konti var piederēt dažādām juridiskām personām.

-   Lai importētu vienu bankas izraksta failu par vienu kontu, opciju **Vairāku bankas kontu izrakstu importēšana visām juridiskajām personām** iestatiet uz **Nē**, un atlasiet bankas kontu, kas ir saistīts ar šo izrakstu. Noklikšķiniet uz **Pārlūkot**, lai atlasītu saistīto bankas izraksta failu, un pēc tam noklikšķiniet uz **Augšupielādēt**.
-   Lai importētu vienu bankas izraksta failu par vairākiem kontiem, opciju **Vairāku bankas kontu izrakstu importēšana visām juridiskajām personām** iestatiet uz **Jā**. Noklikšķiniet uz **Pārlūkot**, lai atlasītu saistīto bankas izraksta failu, un pēc tam noklikšķiniet uz **Augšupielādēt**.

Ja nevienu izraksta elektronisko failu nevar saistīt ar bankas kontu vai ja tas ir saistīts ar vairākiem kontiem, izmantojot identifikācijas laukus, tie netiks importēti. Tomēr joprojām var importēt citus izrakstus failā. Pēc tam lietotājs saņem ziņojumu, ka bankas izrakstu importēšana neizdevās noteiktiem bankas kontiem. Ņemiet vērā, ka lietotājam, kas importē bankas izraksta failu, jābūt piekļuvei juridiskai personai, lai importētu izrakstus no juridiskās personas bankas kontiem. 

Programmā Finance ar vienu darbību varat augšupielādēt arī vairākus izrakstu failus, izmantojot zip failu. Lai importētu vairākus bankas izraksta failus vairākiem kontiem, apvienojiet visus bankas izrakstu failus vienā zip failā. Dialoglodziņā **Importēt bankas izrakstus** opciju **Vairāku bankas kontu izrakstu importēšana visām juridiskajām personām** iestatiet uz **Jā**. Noklikšķiniet uz **Pārlūkot**, lai atlasītu zip failu, kurā atrodas bankas izrakstu faili, un pēc tam noklikšķiniet uz **Augšupielādēt**. Importēšanas process atpazīst zip failu un augšupielādē katru tajā iekļauto izrakstu, neatkarīgi no juridiskās personas bankas konta.

Ir pieejama opcija **Saskaņot pēc importēšanas**. Ja šī opcija ir iestatīta uz **Jā**, tad pēc bankas izraksta augšupielādēšanas sistēma automātiski validē šo bankas izrakstu, izveido jaunu bankas darbību saskaņošanu un darblapu un izpilda noklusējuma atbilstības kārtulu kopu. Šī funkcionalitāte procesu automatizē līdz vietai, kur transakciju atbilstība ir jānosaka manuāli.

## <a name="validate-the-bank-statement"></a>Pārbaudīt bankas izrakstu
Lai pārbadītu izrakstu, lapā **Bankas izraksti** noklikšķiniet uz **Pārbaudīt**. Lai bankas izrakstus varētu saskaņot, tos ir nepieciešams pārbaudīt. Šī darbība tiek izpildīta automātiski, ja importēšanas laikā opcija **Saskaņot pēc importēšanas** tika iestatīta uz **Jā**. 

Banka izraksta validēšana pārbauda šādu informāciju:

-   Bankas izraksts atbilst atlasītajam bankas kontam.
-   Bankas izraksta valūta atbilst atlasītā bankas konta valūtai.
-   Izraksta sākuma bilance ir vienāda ar šī bankas konta iepriekšējā izraksta slēguma bilanci.
-   Datums nepārklājas ar cita bankas izraksta datumu tam pašam bankas kontam.
-   Šī bankas konta izrakstu datumos nepastāv pārtraukumi.
-   Izraksta rindu datumi atrodas starp bankas izraksta sākuma datumu un beigu datumu.
-   Sākuma atlikumu un kopsavilkuma rindu summas ir vienādas ar beigu bilanci.

Kad pārbaude ir pabeigta, bankas izraksta statuss tiek mainīts uz **Pārbaudīts**. Lai bankas izrakstu varētu saskaņot, to ir nepieciešams pārbaudīt.

## <a name="reconcile-the-bank-statement"></a>Saskaņot bankas izrakstu
Pēc elektroniska bankas izraksta importēšanas un šī izraksta validēšanas lapā **Bankas izraksti**, varat saskaņot bankas izrakstu, izmantojot lapas **Bankas darbību saskaņošana** un **Bankas darbību saskaņošanas darblapa**. 

Lapā **Bankas darbību saskaņošana** noklikšķiniet uz **Jauns**, lai izveidotu jaunu saskaņošanu, un pēc tam atlasiet importētā izraksta bankas kontu. Bankas kontam var būt tikai viena atvērta bankas saskaņošana. Pēdējais datums nosaka bankas izraksta transakcijas un Operations bankas transakcijas, kas tiek iekļautas šajā saskaņošanas darblapā. Kā beigu datums pēc noklusējuma tiek izmantots pašreizējais sistēmas datums, bet saskaņošanai šo datumu varat mainīt. Atlikusī virsraksta informācija automātiski tiek ņemta no izraksta. Šī darbība tiek izpildīta automātiski, ja importēšanas laikā opcija **Saskaņot pēc importēšanas** tika iestatīta uz **Jā**. 

Lapā **Bankas darbību saskaņošana** noklikšķiniet uz **Darblapa**, lai atvērtu lapu **Bankas darbību saskaņošanas darblapa**. Ja opcija **Saskaņot pēc importēšanas** tika iestatīta uz **Jā**, tad šai saskaņošanai automātiski tiek izpildīta noklusējuma atbilstības kārtulu kopa. Lai atbilstības kārtulas palaistu manuāli, noklikšķiniet uz **Palaist atbilstības kārtulas** un atlasiet atbilstības kārtulu kopas vai atbilstības kārtulas, ko palaist attiecībā pret bankas transakcijām. Ja jums ir jāapstrādā daudz transakciju, šo darbību varat izpildīt kā pakešuzdevumu. 

Lapā **Bankas darbību saskaņošanas darblapa** ir četri režģi, kuros atrodas transakcijas. Abos augšējos režģos ir redzamas transakcijas no bankas izraksta un Operations, kam vēl nav noteikta atbilstība. Abos apakšējos režģos ir redzamas transakcijas, kurām ir noteikta atbilstība. Cilnē **Detalizēta bankas izraksta transakcijas informācija** ir redzama detalizēta informācija par augšējā režģī atlasīto bankas izraksta transakciju, kurai nav noteikta atbilstība. 

Bankas izraksta transakcijām atbilstību var noteikt vai saskaņošanu var veikt trīs veidos:

-   Transakcijām noteikt atbilstību Operations bankas darbībām.
-   Transakcijām noteikt atbilstību anulēšanas bankas izraksta transakcijai.
-   Transakcijas atzīmēt kā **Jauns**, lai vēlāk tās varētu grāmatot kā bankas transakciju programmā Finance.

Lai manuāli noteiktu transakciju atbilstību, atlasiet transakcijas režģī **Bankas izraksta transakcijas**, atlasiet atbilstošās transakcijas režģī **Operāciju bankas transakcijas** un pēc tam noklikšķiniet uz **Saskaņot**. Atlasītās transakcijas no augšējiem režģiem, kas paredzēti transakcijām, kurām nav noteiktas atbilstības, tiek pārvietotas uz apakšējiem režģiem transakcijām, kurām ir atrastas atbilstības. Turklāt tiek atjauninātas kopsummas, kurām ir un nav atrasta atbilstība. Jums var būt transakciju atbilstības viena pret vienu, daudzas pret vienu un daudzas pret daudzām. Atbilstībām ir jāievēro kārtulas par atļautajām datumu atšķirībām un transakcijas tipu kartēšanu. Šīs kārtulas ir iestatītas lapā **Skaidras naudas un bankas pārvaldības parametri**.

Jūsu saskaņošanā var rasties sīknaudas starpības. Varat noteikt atbilstību vienai bankas izraksta transakcijai un vienai Operations bankas transakcijai, kam pastāv sīknaudas starpības, ja sīknaudas starpība nepārsniedz pielaides summu, kura ir definēta šī bankas konta laukā **Atļautā sīknaudas starpība**. Summa ir norādīta laukā **Labojuma summa** atbilstošā Operations bankas darbībā. Ja bankas darbību saskaņošana ir atzīmēta kā saskaņota, korekcijas tiek automātiski grāmatotas, izmantojot galveno kontu, kas tiek definēts saistīto bankas darbību tipā. Korekcijas netiek atbalstītas dokumentu tipiem **Pārbaude** un **Depozīts**. 

Bankas izraksta transakciju anulēšanām atbilstība tiek noteikta, izmantojot saskaņošanas darblapu. Divām izraksta rindām var noteikt atbilstību, ja to summas ir pretējas un ja viena no transakcijām ir atzīmēta kā anulēšana. Atbilstības kārtulu varat iestatīt arī darbībai **Notīrīt anulēšanas izraksta rindas**.

Anulētajām Operations bankas transakcijām saskaņošana ir jāveic, izmantojot lapu **Operations bankas transakcijas**. Divām Operations bankas transakcijām saskaņošanu varat veikt kopā, ja dokumentos ir vienāds bankas konts, dokumenta tips un maksājuma atsauce, un ja tām ir pretējas summas. Var arī saskaņot vienu atceltu čeku, lai nepieļautu šo transakciju parādīšanu saskaņošanas darblapā. 

Ja pastāv jaunas bankas uzsāktas transakcijas, piemēram, procentu maksājumi, komisijas maksas un nodevas, kas vēl nav norādītas programmā Finance, varat tās pievienot ar atlasīto bankas izraksta saskaņošanu saistītajam žurnālam. Atlasiet bankas izraksta transakciju režģī **Bankas izraksta transakcijas** tām transakcijām, kam nav noteikta atbilstība, un pēc tam noklikšķiniet uz **Atzīmēt kā jaunu**. Transakcijas statuss tiek iestatīts uz **Jauns**, un šī transakcija tiek pārvietota uz režģi **Bankas izraksta transakcijas** tām transakcijām, kam ir noteikta atbilstība. Transakcijas, kas ir atzīmētas kā **Jauns**, jūs vēlāk grāmatosiet no lapas **Bankas izraksts**. 

Transakcijām, kam ir nepareizi noteikta atbilstība, šo atbilstību varat atcelt. Atlasiet atbilstošo bankas izraksta transakciju un pēc tam noklikšķiniet uz **Atcelt atbilstības noteikšanu**. Visas saistītās transakcijas tiek pārceltas atpakaļ uz augšējiem režģiem transakcijām, kam nav noteikta atbilstība, un tiek atjauninātas kopsummas, kam ir un nav noteikta atbilstība. 

Kad saskaņošanas process ir pabeigts, jums šī bankas darbību saskaņošanas darblapa ir jāatzīmē kā saskaņota.  Šis process automātiski grāmatos korekciju summas, izmantojot lapā **Bankas transakcijas tips** iestatītos kontus.  Bankas darbību saskaņošanu izrakstam var atzīmēt kā saskaņotu jebkurā laikā, pat ja pastāv bankas izraksta rindas, kas vēl nav saskaņotas.  Nesaskaņotās transakcijas tiks automātiski pārvietotas uz nākamo saskaņošanas darblapu kā nesaskaņotas bankas izraksta transakcijas, kurām jāveic saskaņošana.  Ņemiet vērā, ka pēc tam, kad bankas izraksta saskaņošana ir atzīmēta kā saskaņota, to vairs nevar atsaukt.  Saskaņošana vairs nebūs rediģējama, un jūs vairs nevarēsit šai saskaņošanai veikt atjauninājumus.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Grāmatot jaunas transakcijas, kas ir saistītas ar saskaņošanu
Bankas izraksta transakcijas, kas saskaņošanas darblapā tika atzīmētas kā **Jauns**, tiek grāmatotas lapā **Bankas izraksts**. Lapā **Bankas izraksts** atlasiet izraksta ID, lai skatītu detalizētu informāciju par šo izrakstu. Izvēlnē **Uzskaite** varat izmantot opcijas **Skatīt sadales** un **Skatīt uzskaiti**, lai skatītu detalizētu informāciju par jaunajām transakcijām un saistītajiem virsgrāmatas ierakstiem. Atlasiet opciju **Grāmatot**, lai bankas izraksta rindas, kuras bija atzīmētas kā **Jauns**, grāmatotu virsgrāmatā. Ņemiet vērā, ka katram bankas izrakstam grāmatošanu var veikt tikai vienu reizi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]