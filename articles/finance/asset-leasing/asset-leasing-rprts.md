---
title: Līdzekļu nomas pārskati
description: Šajā tēmā ir uzskaitīti un īsi aprakstīti pārskati, kas ir pieejami Līdzekļu nomā.
author: moaamer
manager: Ann Beebe
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bc4bac1a422a7505ef4c66b9c3b79a3d754cc4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971482"
---
# <a name="asset-leasing-reports"></a>Līdzekļu nomas pārskati

[!include [banner](../includes/banner.md)]

Šajā tēmā ir uzskaitīti un īsi aprakstīti pārskati, kas ir pieejami Līdzekļu nomā. Lielākā daļa pārskatu tiek rādīti, izpildot tālāk norādītās darbības vai darbības, kas ir ļoti līdzīgas, kā norādīts. 

- Lai skatītu lielāko daļu līdzekļu nomas pārskatu, dodieties uz **Līdzekļa līzings > Vaicājumiem un pārskati > Nomas pārskati** un pēc tam atlasiet pārskatu, ko skatīt. Pārskatiem, kam nepieciešams cits atlases ceļš, darbības, lai atvērtu pārskatu, ir ietvertas attiecīgā pārskata aprakstā. 
- Kad atlasāt drukājamo pārskatu, tiks atvērta parametru lapa, kas ļaus filtrēt informāciju, kas iekļauta pārskatā. Ievadiet filtra kritērijus un pēc tam atlasiet **Labi**, lai ģenerētu pārskatu. Ģenerētajā pārskatā tiks parādīta informācija, kas atbilst norādītajiem filtriem.

## <a name="asset-movement"></a>Pamatlīdzekļu pārvietošana
Līdzekļu pārvietošanas pārskats kalpo kā termiņa pagarināšanas pārskats katras nomas līdzekļa lietošanas tiesību bilancēm. Šis pārskats ļauj skatīt nomas līdzekļu darījumus noteiktā periodā. Pārskatā ir ietverti tālāk norādītie lauki. 

|     Pārskata lauki                  |     Apraksts                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Sākuma datums              |     Nomas pirmās versijas sākuma datums.                     |   
|     Nomas termiņš                     |     Nomas pirmās versijas termiņš.                            |
|     Īstermiņa noma               |     Ja noma ir klasificēta kā īstermiņa noma, tā tiks parādīta kā **Jā**.         |
|     Nelielas vērtības noma                |     Ja noma ir klasificēta kā nelielas vērtības noma, tā tiks parādīta kā **Jā**.          |
|     Sākotnējās līdzekļa lietošanas tiesības     |     Līdzekļa lietošanas tiesību oriģinālā vērtība no sākotnējās atzīšanas žurnāla ieraksta.      |
|     Sākuma bilance              |     Līdzekļa lietošanas tiesību atlikusī vērtība, sākot ar **No datuma**.                         |
|     Nolietojuma izdevumi par periodu    |     Nolietojuma izdevumu summa, kas ņemta no pārskatam definētā datumu diapazona.        |
|     Uzkrātais nolietojums       |     Uzkrātā nolietojuma summa, sākot ar **No datuma**.                               |
|     Vērtības samazinājums                     |     Līdzekļa vērtības samazinājuma summa, kas ņemta no pārskatam definētā datumu diapazona.               |
|     Modifikācijas                  |     Līdzekļa lietošanas tiesību korekciju summa starp datumu parametriem.                            |
|     Atlikusī vērtība                 |     Līdzekļa lietošanas tiesību atlikusī beigu vērtība, kas ir uzkrātā nolietojuma neto vērtība, sākot ar **Līdz datumam**.    |

## <a name="differences-report"></a>Pārskats par atšķirībām
Pārskatā par atšķirībām parādītas atšķirības starp informāciju, kas ielādēta nomas importa struktūrā, un informāciju, kas pašlaik atrodas sistēmā. Tas ļauj salīdzināt, kas tika koriģēts, atjaunināts vai pievienots, izmantojot nomas importēšanas struktūru.  

Pārskata vērtības atšķirsies atkarībā no atlasītās nomas. Pārskatā tiks parādīti tikai tie lauki, kas atšķiras no tā, kas pašlaik ir sistēmā un kas ir sagatavošanas posmu tabulās. Vecā vērtība ir tā, kas vai nu pašlaik ir sistēmā, vai arī iepriekš bija sistēmā, atkarībā no tā, vai ir palaists importēšanas process. Jaunā vērtība rāda vērtību, kas ir sagatavošanas posma tabulā un kas aizstās veco vērtību.

## <a name="five-years-undiscounted-payment-forecast"></a>Maksājumu (bez atlaides) prognoze pieciem gadiem
Piecu gadu maksājumu (bez atlaides) prognozes pārskats parāda prognozētos nomas maksājumus (bez atlaides), kas jāsamaksā nākamajos piecos gados no datuma, kas norādīts pārskata parametros. Pārskatā ir ietverti tālāk norādītie lauki. 

|     Pārskata lauki         |     Apraksts                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Nomas apraksts     |     Nomas apraksts no nomas virsraksta.                                                      |
|     Nomas ID              |     Unikālais nomas ID.                                                                              |
|     Rezervēšana                  |     Nomas grāmata, kas saistīta ar grāmatas ID.                                                         |
|     Klasifikācija        |     Nomas klasifikācija.                                                                  |
|     Grāmatošanas līmenis         |     Slānis, kurā noma tiek grāmatota.                                                         |
|     Valūta              |     Nomas valūta.                                                                        |
|     Pašreizējos               |     Visu nomas maksājumu summa, kas maksājama nākamo 12 mēnešu laikā no pārskata datuma.          |
|     13–24 mēneši          |     Visu nomas maksājumu summa, kas maksājama starp 13. un 24. mēnesi no pārskata datuma.           |
|     25–36 mēneši          |     Visu nomas maksājumu summa, kas maksājama starp 25. un 36. mēnesi no pārskata datuma.           |
|     37–48 mēneši          |     Visu nomas maksājumu summa, kas maksājama starp 37. un 48. mēnesi no pārskata datuma.           |
|     49–60 mēneši          |     Visu nomas maksājumu summa, kas maksājama starp 49. un 60. mēnesi no pārskata datuma.           |
|     Pēc tam            |     Visu nomas maksājumu summa, ko maksājama 61. mēnesī no pārskata datuma vai pēc tam.              |

## <a name="gaap-cash-flows-report"></a>Vispārpieņemto grāmatvedības principu naudas plūsmu pārskats
Vispārpieņemto grāmatvedības principu atklāšanas pārskats atbilst ASV vispārpieņemto grāmatvedības prasību atklāšanas prasībām, kas norādītas 842-20-50-4(g)(1). Lai skatītu šo pārskatu, dodieties uz **Līdzekļu līzings > Vaicājumi un atskaites > Atklāšana > Vispārpieņemtie grāmatvedības standarti — naudas plūsmas**. 

|     Pārskata lauki                                 |     Apraksts                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     No datuma <br> Līdz datumam                        |     Definē datumu diapazonu, kas tiek izmantots, lai ierobežotu pārskatā iekļauto informāciju.      |
|     Juridiska persona                                  |     Juridiska persona, kas saistīta ar nomu.                                      |
|     Nomas veids                                    |     Nomas klasifikācija pēc finansējuma vai darbības.           |
|     Nomas ID                                      |     Unikālais nomas ID.                                                      |
|     Nomas apraksts                             |     Nomas apraksts no nomas virsraksta.                              |
|     Nomas grāmata                                    |     Nomas grāmata, uz kuru atsaucas rinda.                        |
|     Grāmatošanas līmenis                                 |     Katra pamatlīdzeklim piesaistītā grāmata ir iestatīta noteiktam grāmatošanas līmenim, kuram ir vispārējā nolietojuma mērķis.                          |
|     Nomas grupa                                   |     Grupa, kurai piesaistīta noma.                                     |
|     Valūta                                      |     Darījumā lietotās valūtas saīsinājums. Visi pārskati konvertēs darījuma valūtu uz pārskata valūtu.                      |
|     Finanšu noma — darbības naudas plūsmas         |     Kopējo grāmatoto mainīgo maksājumu kopsumma un kopējie procentu maksājumi, kas grāmatoti no amortizācijas grafika starp datuma parametriem.        |
|     Finanšu noma — finanšu naudas plūsmas           |     Kopējo galveno maksājumu summa no amortizācijas grafika starp datuma parametriem.       |
|     Operatīvā noma — darbības naudas plūsmas       |     Visu grāmatoto nomas maksājumu summa un grāmatoto mainīgo maksājumi starp datuma parametriem.            |

## <a name="lease-balances-forecast"></a>Nomas bilances prognoze
Nomas bilances prognoze norāda informāciju tieši no saistību amortizācijas grafika un līdzekļu nolietojuma grafika. Pārskatā tiek parādīts paredzamo nomas saistību prognozētais lielums un līdzekļa lietošanas tiesības laika periodā, ietverot visus šo nomu paredzamos izdevumus. Pārskatā ir ietverti tālāk norādītie lauki.

|     Pārskata lauki                 |     Apraksts                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Sākuma bilance             |     Sākuma bilance nomas amortizācijas grafikā par periodu, kas ietver pārskata sākuma datumu.            |
|     Sākotnējā atzīšana           |     Ja nomas sākuma datums ietilpst pārskatam definētajā datumu diapazonā, šajā kolonnā tiks parādīta sākotnējās atzīšanas žurnāla ieraksta saistību konta vērtība.      |
|     Maksājumi                      |     Nomas maksājumu summa, kas iekļaujas pārskatam definētajā datumu diapazonā.                               |
|     Intereses                      |     Nomas procentu izdevumu summa, kas iekļaujas pārskatam definētajā datumu diapazonā.                    |
|     Beigu bilance                |     Saistību bilance, sākot ar nomu, sākot ar **Līdz datumam**.                                                             |
|     Īstermiņa saistības          |     Īstermiņa saistību summa nomas amortizācijas grafikā, sākot ar **Līdz datumam**.                           |
|     Ilgtermiņa saistības           |     Ilgtermiņa saistību summa nomas amortizācijas grafikā, sākot ar **Līdz datumam**.                            |
|     Sākotnējā atlikusī vērtība      |     "Sākotnējā atlikusī vērtība" nomas līdzekļa aprēķināšanas grafikā par periodu, kas ietver pārskata sākuma datumu      |
|     Sākotnējā atzīšana           |     Ja nomas sākuma datums iekrīt starp pārskata datumu parametriem, šajā kolonnā tiks parādīta sākotnējās atzīšanas žurnāla ieraksta līdzekļu konta vērtība.            |
|     Nolietojuma izmaksas          |     Nomas aprēķināto izdevumu summa, kas iekļaujas pārskatam definētajā datumu diapazonā.                  |
|     Beigu bilance                |     Līdzekļa bilance, sākot ar nomu, sākot ar **Līdz datumam**.                                                              |
|     Kapitāla korekcija             |     Sākuma bilance mīnus sākuma atlikusī vērtība.                                                             |

## <a name="lease-commencements-report"></a>Nomas sākuma pārskats
Nomas sākuma pārskats parāda visas nomas, kas sāktas noteiktā datumu diapazonā, ietverot sākotnējās saistības un līdzekļa lietošanas tiesību bilances. Pārskatā ir ietverti tālāk norādītie lauki. 

|     Pārskata lauki                 |     Apraksts                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Sākuma datums             |     Žurnāla ieraksta sākotnējās atzīšanas datums, kas bija grāmatots šai nomas versijai.         |
|     Sākotnējo saistību summa      |     Saistību summa no sākotnējās atzīšanas žurnāla ieraksta.                                  |
|     Sākotnējā līdzekļa summa          |     Līdzekļa summa no sākotnējās atzīšanas žurnāla ieraksta.                                      |

## <a name="lease-modification-report"></a>Nomas izmaiņu pārskats
Nomas izmaiņu pārskats parāda visas nomas, kas ir izmainītas noteiktā datumu diapazonā. Pārskatā ir parādīts arī lietotājs, kurš koriģēja nomu, un kopējā koriģēto saistību summa. Pārskatā ir ietverti tālāk norādītie lauki. 

|     Pārskata lauki                 |     Apraksts           |
|---------------------------------  |-------------------------  |
|     Koriģēja                   |     Tās personas lietotājvārds, kura veica izmaiņas nomā.                                |
|     Korekcijas liktenis               |     Datums, kurā tika grāmatots korekcijas žurnāla ieraksts.                        |
|     Korekcijas                   |     Jebkura korekcijas žurnāla ieraksta summa, kas grāmatota nomas saistību kontā starp datuma parametriem. Kredīti tiks parādīti pozitīvi, bet debeti būs negatīvi.       |
|     Peļņas (zaudējumu) summa            |     Jebkura korekcijas žurnāla ieraksta summa, kas grāmatota nomas peļņas/zaudējumu kontā starp datuma parametriem. Kredīti tiks parādīti pozitīvi, bet debeti būs negatīvi.       |
|     Nesadalītā peļņa             |     Jebkura korekcijas žurnāla ieraksta summa, kas grāmatota nomas nesadalītās peļņas kontā starp datuma parametriem.      |
|     Beigu saistību bilance      |     Atlikušo saistību bilance, sākot ar nomas datuma korekciju.           |

## <a name="lease-movement-report"></a>Nomas kustības pārskats
Nomas kustības pārskats kalpo kā termiņa pagarināšanas pārskats katras nomas saistību bilancēm. Šis pārskats ļauj lietotājam skatīt nomas saistību darījumus noteiktā periodā.

|     Pārskata lauki             |     Apraksts                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Sākuma datums         |     Nomas pirmās versijas sākuma datums.    |
|     Nomas termiņš                |     Nomas pirmās versijas termiņš.           |
|     Atlikušie maksājumi        |     Maksājumu skaits, kas nomai vēl nav grāmatoti.                       |
|     Sākuma bilance         |     Visu darījumu summa, kas ietekmē nomas saistības, kas radušās pirms pārskata sākuma datuma.             |
|     Sākotnējā atzīšana       |     Jebkuru nomas sākotnējās atzīšanas darījumu summa, kas grāmatota pārskatam definētajā datumu diapazonā.     |
|     Maksājumi                  |     Nomas maksājumu darījumu summa, kas grāmatota pārskatam definētajā datumu diapazonā. Vērtības šajā kolonnā tiks parādītas kā negatīvas summas, jo maksājumi samazina nomas saistību bilanci.  |
|     Intereses                  |     Nomas procentu pieaugums, kas grāmatots pret nomu pārskatam definētajā datumu diapazonā.            |
|     Korekcijas               |     Nomas grāmatoto koriģēšanas darījumu summa pārskatam definētajā datumu diapazonā.                               |
|     Beigu bilance            |     Visu to nomas saistību darījumu bilance, kas grāmatoti, sākot ar pārskata **Līdz datumam**.                  |

## <a name="lease-transactions-report"></a>Nomas darījumu pārskats
Nomas darījumu pieprasījums parāda visus žurnāla ierakstus, kas ir izveidoti, izmantojot Līdzekļa nomu. Katrs žurnāla ieraksts ir saistīts ar grāmatas ID, no kura tas tika izveidots. Tas ļauj viegli saistīt žurnāla ierakstu ar atbilstošu nomu. Nomas darījumu pieprasījums darbojas veidā, kas ir līdzīgs Virsgrāmatas lapai **Dokumenta darījumi**.

## <a name="weighted-average-discount-rate-report"></a>Svērtās vidējās atlaižu likmes pārskats
Svērtās vidējās atlaižu likmes pārskats atbilst ASV vispārpieņemtajiem grāmatvedības principiem, kas norādīti ASC 842-20-50-4(g)(4) par svērto vidējo atlaižu likmi. Lai skatītu šo pārskatu, dodieties uz **Līdzekļa noma > Vaicājumi un pārskati > Atklāšana > Svērtā vidējā atlaižu likme**. Pārskatā ir ietverti tālāk norādītie lauki. 

|     Pārskata lauki                     |     Apraksts                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Sākuma datums                        |     Šajā pārskatā tiks iekļautas visas nomas, kas ir sāktas datuma parametrā **Sākot ar** vai pirms tā. Šis pārskats ir jāpalaiž, sākot ar atklājamā perioda pēdējo dienu.      |
|     Juridiska persona                      |     Juridiska persona, kas ir saistīta ar nomu.                           |
|     Nomas ID                          |     Unikālais nomas ID.                                                  |
|     Nomas apraksts                 |     Nomas apraksts no nomas virsraksta.                          |
|     Rezervēšana                              |     Parādītās nomas noteikts grāmatas veids.                                                                                                                                            |
|     Grāmatošanas līmenis                     |     Katra pamatlīdzeklim piesaistītā grāmata ir iestatīta noteiktam grāmatošanas līmenim, kuram ir vispārējā nolietojuma mērķis.      |
|     Nomas grupa                       |     Grupa, kurai pieder noma.                                 |
|     Atlaides likme                     |     Likme, kas tiek izmantota nomas maksājumu atlaidei.                             |
|     Valūta                          |     Darījumā lietotās valūtas saīsinājums. Visi pārskati konvertēs darījuma valūtu uz pārskata valūtu.  |
|     Atlikušie nomas maksājumi          |     Neapmaksāto nomas maksājumu kopsumma no maksājuma grafika, kas atlikusi no datuma **Sākot ar**.            |
|     Atlikušie svērtie maksājumi       |     Atlikušie nomas maksājumi, kas ir reizināti ar izmantoto atlaižu likmi.   |
