---
title: Atvieglojumu plāna izveide
description: Iestatiet atvieglojumu plānus Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: da11799d3340798067fc03061159896f44750c77
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805734"
---
# <a name="create-a-benefit-plan"></a>Izveidot atvieglojumu plānu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir parādīts, kā iestatīt atvieglojumu plānus Dynamics 365 Human Resources.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Atlasiet **Jauns**.

3. Cilnē **Vispārīgi** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Plāns** | Plāna unikālais identifikators. |
   | **Apraksts** | Plāna apraksts. |
   | **Plāna tips** | Veidojot jaunu plānu, ir jānorāda plāna veids. Plāna veids ir noteikta veida atvieglojumu augsta līmeņa grupēšana. Katrs plāna veids norāda, vai darbinieks var pieteikties vairākos šī veida plānos, vai kontaktpersonas ir saņēmēji vai apgādājamie, un definē seguma opcijas. Varat izveidot jaunus pielāgotus plānu veidus, lai atbilstu jūsu atvieglojumu piedāvājumu vajadzībām. Galvenie atvieglojumu plāna veidi minēti zemāk. <ul><li>401K</li><li>ADD</li><li>Zobārstniecība</li><li>Fitness</li><li>FSA</li><li>Dzīvības</li><li>LTD</li><li>Medicīniskā</li><li>PTO</li><li>STD</li><li>Redze</li></ul> |
   | **Plāna veida kods** | Plāna veida kods. |
   | **Programma** | Norāda programmu, kam pēc izvēles piešķirt plānu. |
   | **Komplekts** | Norāda komplektu, kam pēc izvēles piešķirt plānu. |
   | **Šablons** | Norāda, vai plāns ir vispārējais plāns komplektā, kuram tas ir piešķirts. |
   | **Derīguma sākuma datums un laiks** | Datums un laiks, kurā plāns tik uzsākts. Noklusējuma vērtība ir pašreizējais sistēmas datums. |
   | **Derīguma beigu datums un laiks** | Datums un laiks, kurā plāns tik pabaigts. Noklusējuma vērtība ir 12/31/2154, kas nozīmē nekad. |

4. Atkarībā no izveidojamā plāna veida cilnē **Konfigurācija** nosakiet vērtības tālāk minētajiem laukiem.

   | Plāna tips | Lauks | Apraksts |
   | --- | --- | --- |
   | Ārstniecības (ārstniecība, zobārstniecība, redze, HMO) | COBRA | Norāda, vai plāns ir piemērots Konsolidētajam vispārējā budžeta saskaņošanas likumam (Consolidated Omnibus Budget Reconciliation Act — COBRA). |
   | Ārstniecības (ārstniecība, zobārstniecība, redze, HMO) | HIPAA | Norāda, vai plāns ir piemērots Veselības apdrošināšanas pārnesamības un uzskaitāmības likumam (Health Insurance Portability and Accountability Act — HIPPA). |
   | Ārstniecības (ārstniecība, zobārstniecība, redze, HMO)<br><br>Citi (PTO, Fitness)<br><br>Citas<br><br>Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana)<br><br>Ietaupījumi (piemēram, 401(k))<br><br>FSA | Piemērots priekšnodoklis | Norāda, vai plāna var veikt iemaksas pirms nodokļu piemērošanas. |
   | Ārstniecības (ārstniecība, zobārstniecība, redze, HMO)<br><br>Citi (PTO, Fitness)<br><br>Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana)<br><br>Ietaupījumi (piemēram, 401(k))<br><br>FSA | Grāmatot piemērotu nodokli | Norāda, vai plāna var veikt iemaksas pēc nodokļu piemērošanas. |
   | Ārstniecības (ārstniecība, zobārstniecība, redze, HMO)<br><br>Citi (PTO, Fitness)<br><br>Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana)<br><br>Ietaupījumi (piemēram, 401(k))<br><br>FSA | Līdzstrādnieks | Norāda, kurš veic iemaksas plānā — darbinieks, darba devējs vai abi. |
   | Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Minimālā vajadzība | Minimālā apdrošināšanas seguma summa, kas nepieciešama plānam. |
   | Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Maksimālā vajadzība | Maksimālā apdrošināšanas seguma summa, kas nepieciešama plānam. |
   | Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Izmantot vajadzību pieaugumu | Norāda, vai apstiprināt, ka seguma summa atbilst derīgai pieauguma soļa summai. |
   | Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Inkrementālā summa | Plānam paredzētā apdrošināšanas seguma pieauguma soļa summa. Piemēram, ja pieauguma soļa summa ir 1000, darbiniekam nevar būt $ 200 500 vērta apdrošināšana, tā jānoapaļo uz augšu līdz $ 201 000 vai uz leju līdz $ 200 000. |
   | Ilgstoša invaliditāte<br><br>ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Inkrementāls virziens | Norāda noapaļošanas virzienu — uz augšu vai uz leju, kad vajadzības summa neatbilst inkrementālās summas vērtībai. |
   | ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Apdrošināšanas apliecinājums | Norāda, vai darbiniekam ir jāpierāda atbilstība apdrošināšanai. |
   | ADD (pamata dzīvības apdrošināšana, brīvprātīgā dzīvības apdrošināšana) | Apjoms | Uzskaites valūtas summa. Šis lauks ir aktīvs tikai tad, ja ir atlasīta izvēles rūtiņa Atbilstība apdrošināšanai. |
   | Ietaupījumi (piemēram, 401(k))<br><br>FSA | Minimālais gada ieguldījums | Minimālā iemaksu summa, kas nepieciešama plānam. |
   | Ietaupījumi (piemēram, 401(k))<br><br>FSA | Maksimālais gada ieguldījums | Maksimālā iemaksu summa, kas nepieciešama plānam. |
   | Ietaupījumi (piemēram, 401(k)) | Darba devēja maksimālā gada summa | Maksimālā summa, ko darba devējam atvieglojumu periodā ļauts iemaksāt darbinieka uzkrājumu plānā. Lai lietotu šo lauku, jāatzīmē izvēles rūtiņa Darba devēja atbilstība. |
   | Ietaupījumi (piemēram, 401(k)) | Darba devēja atbilstība | Norāda, vai darba devējs veic iemaksas darbinieka uzkrājumu plānā. |
   | Ietaupījumi (piemēram, 401(k)) | Darba devēja atbilstības procentuālā vērtība | Darbinieka iemaksu procentuālā vērtība, kam atbildīs darba devējs. |
   | Ietaupījumi (piemēram, 401(k)) | Darba devēja atbilstības maksimālā robežvērtība | Maksimālā procentuālā vērtību, kam atbildīs darba devējs. Piemēram, ja darba devējs atbildīs 100% no darbinieka iemaksām līdz 6% no darbinieka algas, darba devēja atbilstības ierobežojums ir 6%. |

5. Cilnē **Iestatīt** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atļaut/turpināt reģistrāciju** | Norāda, vai darbinieki var pieteikties plānā, ja tie atbilst piemērotības prasībām.</br></br>Ja tas ir iestatīts uz Nē, plāns nebūs pieejams darbiniekiem, kad apstrādāsiet atbilstību. |
   | **Automātiska reģistrēšana no iepriekšējā gada** | Norāda, vai automātiski reģistrēt plānā piemērotu darbinieku, ja viņš tika reģistrēts iepriekšējā gadā. |
   | **Automātiska reģistrācija pēc noklusējuma** | Norāda, vai atlasīt plānu reģistrācijai pēc noklusējuma. Plāns nav obligāts, tāpēc darbinieks var mainīt noklusējuma atlasi. |
   | **Slēgts jaunai reģistrācijai** | Norāda, vai ierobežot plānu, ka tas ir piemērots tikai darbiniekiem, kas tika reģistrēti plānā iepriekšējā gadā. |
   | **Obligāts plāns** | Norāda, vai automātiski reģistrēt darbiniekus plānā. Darbinieki nevar mainīt reģistrācijas atlasi. |
   | **Sākuma datums** | Datums, kad uzņēmumā tika izveidots plāns. |
   | **Kreditora konts** (Atvieglojumu sniedzējs) | Kreditors, kuram uzņēmums maksā prēmijas par plānu. |
   | **Nosaukums** (Atvieglojumu sniedzējs) | Kreditora nosaukums. |
   | **Kreditora raksturojums** (Atvieglojumu sniedzējs) | Kreditora raksturojums plānam. Piemēram, uzņēmuma grupas plāna numurs. |
   | **Rezerves raksturojums** (Atvieglojumu sniedzējs) | Kreditora rezerves raksturojums plānam. Piemēram, uzņēmuma konta numurs. |
   | **Valūta** (Atvieglojumu sniedzējs) | Valūta, kas tiek izmantota, lai maksātu prēmijas sniedzējam. |
   | **Izdevumu konts** (Atvieglojumu sniedzējs) | Virsgrāmatas konts, kas tiek izmantots kā izdevumu konts plāna prēmijām. |
   | **Kreditora konts** (Atvieglojumu administrators) | Kreditors, kuram uzņēmums maksā par plāna administrēšanu. Ja plāns administrē pats sevi, atstājiet šo lauku tukšu. |
   | **Nosaukums** (Atvieglojumu administrators) | Atvieglojumu administrēšanas kreditora nosaukums. |
   | **Kreditora raksturojums** (Atvieglojumu administrators) | Administrēšanas kreditora raksturojums plānam. |
   | **Rezerves raksturojums** (Atvieglojumu administrators) | Administrēšanas kreditora rezerves raksturojums plānam. |
   | **Valūta** (Atvieglojumu administrators) | Valūta, kas tiek izmantota, lai maksātu prēmijas atvieglojumu administratoram. |
   | **Izdevumu konts** (Atvieglojumu administrators) | Virsgrāmatas konts, kas tiek izmantots kā izdevumu konts izmaksām, kas saistītas ar plāna administrēšanu. |

6. Pēc nepieciešamības filtrējiet cilnē **Filtri**. Varat filtrēt pēc tālāk minētajiem laukiem.

   - **Biznesa vienība**
   - **Nodaļa**
   - **Juridiska persona**
   - **Vieta**
   - **Ieņemamais amats**

7. Cilnē **Piemērotības kārtulas** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Rindas numurs** | Piemērotības kārtulas rindas numurs. |
   | **Piemērojamības kārtula** | Piemērotības kārtula, ko piemērot atvieglojumu plānam. Šī piemērotības kārtula tiks piemērota attiecīgajam darbības veidam un saistīta ar norādīto seguma gaidīšanas periodu un ieturējumiem. |
   | **Darbības tips** | Darbība, kam pielietot piemērotības kārtulu: atvieglojumu reģistrācija vai atvieglojumu beigu termiņš. |
   | **Vajadzības gaidīšanas periods** | Vērtība no Gaidīšanas perioda veidlapas. Seguma gaidīšanas periods nosaka dienu vai mēnešu skaits, ko darbinieks gaida līdz atvieglojumu segumam vai atvieglojumu beigu termiņam, pamatojoties uz piemērotības kārtulas un darbības veida kritērijiem. |
   | **Ieturējumu gaidīšanas periods** | Vērtība no Gaidīšanas perioda veidlapas. Ieturējumu gaidīšanas periods nosaka dienu vai mēnešu skaits, ko darbinieks gaida līdz atvieglojumu ieturējumiem no algas, pamatojoties uz piemērotības kārtulas un darbības veida kritērijiem. |

8. Atlasiet **Saglabāt**.

## <a name="view-enrolled-workers"></a>Reģistrēto nodarbināto skatīšana

Varat skatīt reģistrētos nodarbinātos, kas reģistrēti atlasītajiem atvieglojumu plānam.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Navigācijas joslas cilnē **Priekšrocības** atlasiet **Reģistrētie darbinieki**.

## <a name="attach-coverage-options"></a>Pievienot vajadzību opcijas

Atlasītajam atvieglojumu plānam varat pievienot seguma opcijas. Seguma opciju pievienošana savieno kopā seguma opcijas likmju un ieturējumu iestatījumus.  Piemērs: ārstniecības plānam lietotājs izvēlētos atlasīt ģimenes seguma opciju.  Viņam būtu jāatlasa saistītā plāna ģimenes likme (iestatīta likmes iestatījumos) un ieturējumi saistītajam plānam (iestatīti likmes iestatījumos). Tas sniedz darba devēja un darbinieka izmaksas atlasītajam segumam. Pēc tam process jāatkārto segumam darbinieks+1 vai darbinieka segumam.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Navigācijas joslas cilnē **Priekšrocības** atlasiet **Pārklājuma opciju pievienošana**.

## <a name="override-eligibility-rules"></a>Piemērotības kārtulas ignorēšana

Varat pievienot plānam nodarbinātos kā izņēmumu no piemērotības kārtulām. Katrs pievienotais nodarbinātais būs piemērots atvieglojumu plānam.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Navigācijas joslas cilnē **Priekšrocības** atlasiet **Piemērotības kārtulas pārlabošana**.

## <a name="view-attached-periods"></a>Pievienoto periodu skatīšana

Varat redzēt pieejamo atvieglojumu periodu sarakstu.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Atlasiet cilni **Periodi** navigācijas joslā.

## <a name="view-plan-description"></a>Skatiet plāna plaprakstu

Varat norādīt plāna aprakstu, lai palīdzētu darbiniekiem izvēlēties atvieglojumus. Plāna apraksts, ko ievadāt šeit, tiek parādīta darbinieku pašapkalpošanās pakalpojumā, uzbīdot kursoru uz plāna seguma opciju sarakstā.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Navigācijas joslas cilnē **Priekšrocības** atlasiet **Plāna apraksts**.

## <a name="view-flex-credit-programs"></a>Skatīt brīvā režīma kredītu programmas

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Atvieglojumu plāni**.

2. Navigācijas joslas cilnē **Priekšrocības** atlasiet **Brīvā režīma kredītprogrammas**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]