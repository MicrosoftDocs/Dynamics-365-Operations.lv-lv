---
title: "Ģenerēt finanšu pārskatu"
description: "Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 13bef3abc381a903bf48daa18ef01b07103ef9ea
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="generate-a-financial-report"></a>Ģenerēt finanšu pārskatu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta vispārīga informācija finanšu atskaites ģenerēšanu. 

Lai izveidotu pārskatu, atveriet pārskata definīciju un pēc tam rīkjoslā noklikšķiniet pogu Ģenerēt. Tiks atvērts logs Pārskata rindas statuss, un norādīs jūsu pārskata atrašanās vietu rindā. Pēc noklusējuma, izveidotie pārskati tiks atvērti Tīmekļa skatītājā.
| ![Piezīme](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Piezīme")**Piezīme**        |
|------------------------------------------------------------------------------------------------|
| Atskaites varat ģenerēt tikai mapēs un atrašanās vietās, kurām jums ir piekļuves tiesības. |

Šī tabula sniedz pārskatu ģenerēšanai pieejamo opciju apskatu.

| Opcija                                                                                | Plašāka informācija |
|---------------------------------------------------------------------------------------|----------------------|
| Iestatiet grafiku, lai automātiski izveidotu pārskatu vai pārskatu grupu              |                      |
| Pārbaudīt trūkstošus kontus vai datus pārskatā, un apstipriniet pārskata precizitāti |                      |

Kad veidojat atskaiti, tiek izmantotas opcijas, kuras jūs norādījāt cilnēs Atskaites definīcija . Cilnē Izvade un sadale varat norādīt atskaišu bibliotēkas atrašanās vietu, kas sniedz vieglu veidu, kā šo atskaiti kopīgot.

## <a name="schedule-report-generation"></a> Pārskatu izveides plānošana
Daudziem uzņēmumiem ir pamata kopas ar pārskatiem, kas tiek palaisti iepriekš ieplānotos intervālos, lai saskaņotu ar biznesa procesiem. Jūs var ieplānot regulāru pārskatu izveidi, piemēram, katru dienu, katru nedēļu, katru mēnesi vai reizi gadā. Tas var būt viens pārskats vai pārskatu grupa, kas ietver vairākus uzņēmumus. Ievadiet akreditācijas datus katram norādītajam uzņēmumam, piemēram, pārskata koka definīciju. Ja akreditācijas dati nav derīgi, pārskats parādīs tikai informāciju, kurai jums ir piekļuves tiesības, piemēram, uzņēmums, ko esat reģistrējuši. Vispirms izlasiet izvades informāciju no pārskata grupas, un pēc tam no atsevišķiem pārskatiem.

Kad pārskata grafiki tiek izveidoti un saglabāti, tie tiek parādīti navigācijas rūtī sadaļā Pārskatu grafiki. Jūs varat izveidot mapes, lai sakārtotu pārskatus. Ja viens pārskats grafikā netiek izpildīts, citi pārskati turpinās izpildi.
| ![Svarīgi](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Svarīgi")**Svarīgi**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lai izveidotu, modificētu un dzēstu grafikus, ir nepieciešama veidotāja vai administratora loma. Izpildot pārskatu, kura akreditācijas dati tika izmantoti, lai izveidotu grafiku, tiek izmantoti arī lai izveidotu pārskatu. |

### <a name="create-a-report-schedule"></a>Izveidot pārskata grafiku

1.  Pārskatu veidotājā izvēlnē Fails, noklikšķiniet uz Jauns, un pēc tam atlasiet Pārskata grafiks. Atveras dialoglodziņš Jauns pārskata grafiks.
2.  Sadaļā Iestatījumi, atlasiet atsevišķu pārskatu vai pārskata grupu, lai to ieplānotu. Uzņēmumam vai veidošanas bloku atlasei, ar kuru jūs esat pieteicies šobrīd, ir pieejami tikai pārskati vai pārskata grupas.
3.  Atlasiet izvēles rūtiņu Aktīvs, lai ieslēgtu pārskatu grafiku. Tikai pārskata veidotājs vai administrators var aktivizēt vai deaktivizēt pārskata grafiku.
4.  Noklikšķiniet uz pogas Atļaujas, lai ievadītu uzņēmuma akreditācijas datus. Pēc noklusējuma jūsu pieteikšanās informācija tiek izmantota kompānijai, ko esat reģistrējuši. Ja citi uzņēmumi ir iekļauti, piemēram, pārskata koka definīcijās, atlasiet Izmantot atsevišķus akreditācijas datus, un pēc tam ievadiet jebkura cita uzņēmuma, kas ir iekļauts pārskata grafikā, akreditācijas datus. Jūs varat atlasīt Windows autentifikācija vai katram uzņēmumam ievadīt lietotāja vārdu un paroli. Atlasiet izvēles rūtiņu Akreditācijas datu saglabāšana, lai saglabātu akreditācijas datus šiem uzņēmumiem, un pēc tam noklikšķiniet uz Labi, lai aizvērtu dialoglodziņu.
5.  Sadaļā Biežums, laukā Periodiskuma sākšana atlasiet datumu, kad grafiks ir jāsāk. Pēc noklusējuma tiek atlasīts pašreizējais sistēmas datums klienta datorā.
6.  Laukā Pārskata izpilde, izvēlieties laiku, kad pārskats jāizpilda. Ja ievadāt laiku, kas ir pirms pašreizējā sistēmas laika, pārskats tiek izpildīts nākamajā ieplānotajā datumā.
7.  Apgabalā Periodiskuma modelis, norādiet, cik bieži pārskats tiek izpildīts. Pēc noklusējuma tiek atlasīta opcija Katru dienu ar parametra Intervāls (dienas) vērtību 1. Ir pieejamas arī šādas opcijas: Katru nedēļu, Katru mēnesi un Katru gadu.
8.  Apgabalā Periodiskuma diapazons, atzīmējiet, kad jāpārstāj pārskata izveide.
    -   Nav beigu datuma – pārskata grafiks darbojas nenoteiktu laiku.
    -   Iestatīt gadījumu skaitu – pārskata grafiks tiek izpildīts noteiktu reižu skaitu un pēc tam tiek deaktivizēts.
    -   Beidzas – pārskatu grafiks beidzas norādītajā datumā.

9.  Rīkjoslā noklikšķiniet uz Saglabāt. Dialoglodziņā Saglabāt kā, ievadiet pārskatu grafika unikālu nosaukumu un aprakstu.

Lai kopētu pārskatu grafiku, ir nepieciešama veidotāja vai administratora loma. Pat tad, ja administrators modificē atskaišu grafiku, pārskats satur tā lietotāja akreditācijas datus, kurš izveidoja pārskatu.
### <a name="copy-a-report-schedule"></a>Kopēt pārskata grafiku

1.  Pārskata veidotāja navigācijas rūtī noklikšķiniet uz Pārskatu grafiki, un atveriet pārskata grafiku, kuru nepieciešams nokopēt.
2.  Izvēlnē Fails, noklikšķiniet uz Saglabāt kā, un pēc tam ievadiet grafika jauno nosaukumu un aprakstu dialoglodziņā Saglabāt kā. Noklikšķiniet uz Labi, un jaunais grafiks tiks parādīts navigācijas rūtī.
3.  Jaunajā grafikā, modificējiet laukus un informāciju pēc nepieciešamības, un pēc tam rīkjosla noklikšķiniet uz Saglabāt, vai noklikšķiniet uz Saglabāt izvēlnē Fails.

Lai dzēstu pārskata grafiku, jums ir jābūt atskaišu grafika īpašniekam, vai administratora lomai.
### <a name="delete-a-report-schedule"></a>Dzēst pārskata grafiku

1.  Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz Pārskatu grafiki.
2.  Atlasiet pārskata grafiku, kuru nepieciešams izdzēst, un pēc tam noklikšķiniet uz Dzēst vai nospiediet pogu Dzēst.
3.  Dzēšanas apstiprināšanas dialoglodziņā noklikšķiniet uz Jā, lai neatgriezeniski dzēstu pārskata grafiku. Ja jums nav atļaujas dzēst šo grafiku, tiks parādīts ziņojums un pārskats netiks dzēsts.

### <a name="credentials-and-report-schedules"></a>Akreditācijas dati un pārskata grafiki

Neievadot akreditācijas datus, kas ir nepieciešami visiem uzņēmumiem, kas ir iekļauti pārskatos, saglabājot pārskata grafiku, tiek parādīts šāds ziņojums: "Ievadiet akreditācijas datus uzņēmumiem, kuri ir iekļauti šajā pārskata grafikā. Noklikšķiniet uz pogas Atļaujas, lai ievadītu jūsu akreditācijas datus.

Piemēram, Madara piesakās uzņēmumam A, izmantojot savu lietotājvārdu un paroli. Viņa izveido grafiku pārskatam, kas izmanto pārskata koka definīciju, lai apkopotu datus no vairākiem uzņēmumiem. Saglabājot šo pārskatu grafiku, Madarai tiek piedāvāts ievadīt akreditācijas datus citiem uzņēmumiem, kuri ir norādīti pārskata koka definīcijā. Kad jūsu akreditācijas datu derīguma termiņš beidzas, ietekmētie pārskati atskaišu grafikā netiek izveidoti līdz akreditācijas dati netiek atjaunināti. Pārskata rindā tiek parādīts ziņojums, lai norādītu, ka nepieciešams atjaunināt atļaujas. Pārskata grafiks neizdodas, ja notiek jebkurš no šiem scenārijiem (jo tiem ir nepieciešami akreditācijas dati):
-   Pārskatu kokam tika pievienots jauns uzņēmums atsevišķam pārskatam.
-   Pārskata grupā tika modificēts pārskats.
-   Pārskatu grupai tika pievienots jauns pārskats papildu uzņēmumam.

Lai turpinātu, noklikšķiniet uz pogas Atļaujas dialoglodziņā Pārskatu plānošana, un pēc tam ievadiet atbilstošos akreditācijas datus.

## <a name="missing-account-analysis-feature"></a> Trūkstoša konta analīzes līdzeklis
Jūs varat meklēt finanšu kontus un dimensijas, kas, iespējams, nav norādītas visās rindu definīcijās, pārskata koka definīcijās un pārskatu definīcijas veidošanas bloka grupā. Tas ir noderīgi, ja izveidojat vai atjaunināt vairākus kontu vai veidošanas blokus īsā laika periodā, un vēlaties pārbaudīt, vai visa jaunā informācija tiek iekļauta jūsu pārskatos.

Trūkstošie konti tiek noteikti, izmantojot mazāko un lielāko vērtību no rindas definīcijas vai atskaites koka definīcijas, un pēc tam parāda sarakstu ar kontiem, kas nav rindas definīcijas vai atskaites koka definīcijā, bet kas atrodas finanšu datos. Ja trūkstošs konts ir lielāks vai mazāks par vērtībām rindas definīcijā, šis konts netiek iekļauts norādīto kontu sarakstā.
| ![Padoms](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Padoms")**Padoms**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Pārbaudes nolūkiem, šis process ir jāizpilda pirms ikmēneša pārskatu izveides, kā arī veidojot jaunus veidošanas blokus. |

Pārskatos, kuros ir vērtību diapazoni, ir mazāka trūkstošu kontu varbūtība. Ja iespējams, izmantojiet diapazonus veidošanas blokos, lai iekļautu jaunus kontus, kad tie tiek izveidoti. Ja jebkura pārskata definīcijā kā uzņēmums ir iestatīts @ANY, varat pieteikties noteiktā uzņēmumā un izpildīt trūkstošo kontu analīzi šim uzņēmumam.
| ![Piezīme](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Piezīme")**Piezīme**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja tika pievienots jauns uzņēmums, jums šis jaunais uzņēmums ir jāpievieno atskaišu kokiem jebkurā esošā atskaitē, citādi šis uzņēmums netiks iekļauts trūkstošo kontu analīzē. |

### <a name="run-missing-account-analysis"></a>Palaist trūkstošo kontu analīzes līdzekli

1.  Pārskatu veidotājā noklikšķiniet Rīki, un pēc tam noklikšķiniet uz Trūkstošo kontu analīze.
2.  Laukā Uzņēmuma filtrs, atlasiet uzņēmumu, lai filtrētu rezultātus, vai atlasiet Visas (bez filtra), lai parādītu rezultātus no visiem pieejamajiem uzņēmumiem.
3.  Laukā Dimensiju filtrs, atlasiet dimensiju, lai filtrētu rezultātus, vai izvēlieties Visas (bez filtra), lai skatītu visu dimensiju informāciju, visām pieejamajām dimensijām.
4.  Laukā Grupēt pēc, atlasiet opciju rezultātu kārtošanai. Jūs varat kārtot rezultātus saskaņā ar saistīto veidošanas bloku, vai pēc dimensiju un vērtību kopām.
5.  Pārskatiet attēlotos rezultātus. Atlasot vienumu augšējā rūtī, apakšējā rūtī tiek rādīta papildinformācija par izņēmumu. Tas ietver saistītās dimensijas, vērtības un pārskatus.
6.  Lai atvērtu iesaistīto vienumu, noklikšķiniet uz saistīto ikonu, kas tiek parādīts saraksta rūtī vai ar peles labo pogu noklikšķiniet uz vienuma, un atlasiet Atvērt. Lai atlasītu vairākus vienumus, turiet nospiestu taustiņu Ctrl, atlasot vienumus apakšējā rūtī.
7.  Ja jebkuri vienumi, veidošanas bloki vai pārskati tiek atgriezti, jo tie nav jāiekļauj analīzē, noklikšķiniet ar peles labo pogu uz vienuma, un atlasiet Izslēgt, vai atlasiet izvēles rūtiņu Izslēgt blakus vienumam, lai noņemtu to no saraksta. Neiekļautie vienumu netiek iekļauti sarakstā, kad tas tiek atsvaidzināts. Lai atlasītu vairākus vienumus, turiet nospiestu taustiņu Ctrl, un apakšējā rūtī atlasiet vienumus. Lai skatītu visus vienumus, ieskaitot rezultātus, kas iepriekš tika atlasīti neiekļaušanai analīzē, atlasiet izvēles rūtiņu Parādīt izslēgtos veidošanas blokus un vērtības, un pēc tam noklikšķiniet uz Atsvaidzināt.
8.  Noklikšķiniet uz Atsvaidzināt, lai atsvaidzinātu izņēmumus, kas ir jārisina. Noklikšķiniet uz Jā, lai pilnībā atsvaidzinātu visus rezultātus, vai noklikšķiniet uz Nē, lai veiktu risināmo vienumu daļēju atsvaidzināšanu.
    | ![Piezīme](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Piezīme")**Piezīme**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Forma tiek automātiski atsvaidzināta atveroties, ja vien tā netika atvērta pēdējo 15 minūšu laikā. |

9.  Kad šīs problēmas ir novērstas, noklikšķiniet uz Labi, lai aizvērtu dialoglodziņu.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Tastatūras saīsnes trūkstošu kontu analīzei
Kad palaižat trūkstošo kontu analīzi, ir pieejami tālāk norādītie īsinājumtaustiņi.

| Lai to paveiktu                           | Izmantojiet šo tastatūras saīsni |
|--------------------------------------|----------------------------|
| Filtrēt pēc uzņēmuma                    | Alt+C                      |
| Filtrēt pēc dimensijas                  | Alt+D                      |
| Atlasīt lauku Grupēt pēc            | Alt+G                      |
| Rādīt izslēgtos blokus un vērtības      | Alt+S                      |
| Atsvaidzināt rezultātus                      | Alt+R                      |
| Izslēgt atlasīto veidošanas bloku  | Alt+X                      |
| Izslēgt atlasītās rindas definīciju  | Ctrl+B                     |
| Izslēgt atlasītās dimensijas vērtību | Ctrl+D                     |
| Atvērt atlasītā pārskata definīciju  | Ctrl+R                     |
| Atvērt atlasītās rindas definīciju     | Ctrl+O                     |

 
<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskati](financial-reporting-intro.md)

[Pārskatu veidotāja saskarne](report-designer-interface.md)



