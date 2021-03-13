---
title: Atlīdzības apstrāde
description: Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju.
author: andreabichsel
manager: tfehr
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5cf5b8cd297f1686998688979a736f47f7d100c4
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113447"
---
# <a name="process-compensation"></a>Atlīdzības apstrāde

Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju. Šajā rakstā ir sniegta informācija par fiksētās atlīdzības sistēmu atlīdzības apstrādes pamata plūsmu, neņemot vērā darbinieka sniegumu.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Jaunu atlīdzības summu plānošana un ietveršana budžetos
Lai saviem darbiniekiem piešķirtu nopelnu palielinājumu, katrai nodaļai ir jāiestata fiksēts palielinājuma budžets: Atlīdzību pārvaldība > Saites > Nopelnu palielinājuma mērķi. (Šo formu var atvērt arī no nodaļas sadaļas: Organizācija > Nodaļas.) Šeit varat tālāk norādīt, vai darbiniekiem, kas ir noteiktu arodbiedrību dalībnieki vai atrodas noteiktā atrašanās vietā, ir jāsaņem atšķirīgs palielinājuma procents. Lauki **Budžets** un **Valūta** ir informatīvi. Tos var izmantot, lai norādītu budžeta valūtas summu.

## <a name="set-up-the-compensation-process"></a>Atlīdzības apstrādes iestatīšana
Procesa notikums ļauj norādīt atlīdzības apstrādes parametrus. Tas ietver arī izvērtējamo datumu periodu atlīdzības summu noteikšanai un datumu, kurā jaunajām atlīdzības summām jāstājas spēkā.

Pēc izvēles varat ietvert fiksētās maksas likmes nolīgšanas datumu, ja kāda no fiksētās atlīdzības sistēmām izmanto nolīgšanas kārtulu Procenti. Šajās sistēmās ikviens, kurš tika pieņemts pēc cikla sākuma datuma un pirms fiksētās maksas likmes nolīgšanas datuma, saņems 100% no aprēķinātā nopelna vai vispārējā palielinājuma. Ikviens, kas tika nolīgts pēc fiksētās maksas likmes nolīgšanas datuma un pirms cikla beigu datuma, saņems daļu no sava aprēķinātā palielinājuma, pamatojoties uz to, cik dienas no kopējā cikla dienu skaita tie bija nodarbināti. Piemēram, ja cikls ir no 1. janvāra līdz 31. decembrim un no 1. aprīļa sākas fiksētās maksas likmes nolīgšanas datums, darbinieks, kurš tiek pieņemts martā, saņems pilnu aprēķināto palielinājumu, bet darbinieks, kurš tiek pieņemts 1. jūlijā, saņems aptuveni pusi no aprēķinātā palielinājuma.

Apstrādes notikuma **Punkts laikā** datums tiek izmantots, apstrādājot tikai noteiktas mainīgās atlīdzības sistēmas, un tas nav šeit aplūkots. **Pārskatīt termiņš** ir termiņš, kad jāveic visi ieteikumi, lai jauna atlīdzības summas var ielādēt darbinieka ierakstā. Pārskatīšanas datums ir tikai informatīvs.

Pēc apstrādes notikuma parametru saglabāšanas varat noklikšķināt uz pogas **Iestatījumi** un norādīt iekļaujamās sistēmas, kad tiek izpildīts šis process, un to, kuras fiksētās atlīdzības darbības ir jāveic katrai sistēmai.

Noklikšķiniet uz pogas **Pievienot** cilnē **Sistēmas**, lai apstrādes notikumam pievienotu atlīdzības sistēmu. Kolonnas **Izmantot citus līdzekļus**, **Līdzekļu faktors** un **Līdzekļu apraksts** tiek izmantotas tikai mainīgās atlīdzības sistēmām un nav aplūkotas šajā rakstā.

Saglabājiet ierakstu un pēc tam noklikšķiniet uz pogas **Pievienot** cilnē **Darbības**, lai atlasītajai sistēmai pievienotu fiksētās atlīdzības darbības. Izmantojiet opciju **Iespējot ieteikumus**, lai ievadītu summu, kas atšķiras no darbībai aprēķinātā algas palielinājuma. Lai aprēķinātu darbību, kuras pamatā ir iepriekšējās darbības rezultāts, un saistītu vairākas atlīdzības darbības, atzīmējiet opciju **Izmantot iepriekšējo rezultātu**. Fiksētās atlīdzības darbības ir atlīdzības loģikas veidi, kam varat dot aprakstošus nosaukumus. Līmeņa un joslas sistēmām varat pievienot tikai tālāk norādīto veidu fiksētās atlīdzības darbības.

| Fiksētās atlīdzības darbības veids | Funkcionalitāte                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kapitāls                        | Kapitāla darbības salīdzinās darbinieka samaksas likmi no cikla beigu datuma ar zemāko atskaites punktu un darbinieka darbā norādīto līmeni. Ja darbinieka apmaksas likme ir mazāka par minimālo atsauces punktu, tiks aprēķināts palielinājums, kas nepieciešams, lai darbinieku novirzītu uz minimālo punktu diapazonā.                                                                                |
| Nopelni                         | Nopelnu darbības aprēķinās palielinājumu, pamatojoties uz darbinieka apmaksas likmi no cikla beigu datuma, un palielinājuma procentus, kas atrodami fiksētā palielinājuma budžetā darbinieka nodaļai, arodbiedrībai un atrašanās vietai.                                                                                                                                                                                         |
| Vispārējs                       | Vispārīgās darbības aprēķinās palielinājumu, pamatojoties uz procentu, vai arī piešķirs darbiniekiem pamatsummu. Tas tiek noteikts, pamatojoties uz sadaļas **Fiksēta atlīdzība** iestatījumiem cilnē **Vispārīgi**.                                                                                                                                                                                                                        |
| Izplatīšana                     | Veicināšanas pasākumi sniedz konkrētu atrašanās vietu, kur var piešķirt pieaugumu, tāpēc noteikti atlasiet opciju **Iespējot ieteikumus**, lai varētu ievadīt ieteikums darbiniekiem, kuri saņems veicināšanas pasākumus.  Darbiniekiem bez ieteikta palielinājuma darbība **Paaugstināšana amatā** netiks pievienota viņu fiksētās atlīdzības ierakstiem.                                                                       |
| Citu līmeņu maiņa            | Iepriekšējā piemērā **Pazemināšana** ir nosaukums darbībai **Fiksēta atlīdzība** ar tipu **Citu līmeņu maiņa**. Tas ģenerē 0 (nulle izmaiņas) vadlīniju palielinājumu, tādēļ varat ievadīt ieteikto summu, lai koriģētu darbinieka algas likmi. (Noteikti atzīmējiet opciju **Iespējot ieteikumus**.) Darbiniekiem bez ieteikuma šī darbība netiks pievienota fiksētās atlīdzības ierakstiem. |

Pakāpju sistēmai var pievienot tikai sadaļas **Fiksēta atlīdzība** darbības ar tipu Pakāpe.

| Fiksētās atlīdzības darbības veids | Funkcionalitāte                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Solis                           | Cilnē Vispārīgi norāda, vai šai darbībai jāpārvieto darbiniek uz priekšu par nulle darbībām, vienu darbību vai divām darbībām.                                                                                  |
|                                | **Nulle darbības** — darbinieks saņems pašreizējas darbības algas likmi.                                                                                                                      |
|                                | **Viena darbība** — sistēma pārbauda, vai darbinieks jau ir sava līmeņa pēdējā atsauces punktā.                                                                                             |
|                                | **Divas darbības** — sistēma pārvietos darbinieku uz priekšu par divām darbībām pašreizējā līmenī. Ja darbinieks sasniedz pēdējo līmeņa atsauces punktu, sistēma darbinieku var pārvietot tikai par vienu vai nulle darbībām. |

## <a name="run-the-compensation-process"></a>Atlīdzības procesa palaišana
Kad apstrādes notikumam ir iestatīti nepieciešamie datumu lauki, sistēmas un darbības, lapā **Apstrādes notikums** varat noklikšķināt uz **Palaist procesu**. Tiks atvērts dialogs **Palaist atlīdzības apstrādes notikumus**. Šajā dialogā noklikšķiniet uz opcijas **Rādīt pārstrādes rezultātus**, lai skatītu, kā atlīdzības summas tika aprēķinātas katram darbiniekam. Noklikšķinot uz **Labi**, tiks palaists atlīdzības process visiem darbiniekiem, kuri atlasītajos atlīdzības plānos ir no cikla beigu datumam.

## <a name="view-the-process-results"></a>Apstrādes rezultātu skatīšana
Lai skatītu apstrādes rezultātus, atveriet lapu **Procesa rezultāti**. Katru reizi, kad tiek palaists procesa notikums, tiek izveidots jauns atlīdzības notikums. Šādā veidā var veikt izmēģinājuma palaides, veikt korekcijas un vairākkārt palaist atlīdzības notikumu, lai redzētu, kā dažādas izmaiņas ietekmē darbinieku atlīdzību.

Lapā **Apstrādes rezultāti** ir ietverta informācija par apstrādes izpildi, tostarp informācija par to, kad izpilde notika, lietotāju, kurš palaida apstrādi, un to, vai apstrādes izpildes laikā radās kļūdas. Varat arī atlasīt opciju **Bloķēts**, lai atspējotu pogu **Ielādēt atlīdzību** un nevienam neļautu ielādēt atlīdzības notikumus darbinieka ierakstos. Noklikšķinot uz pogas **Darbinieku rezultāti**, tiks parādīts to darbinieku saraksts, kas iekļauti palaidē.

Opcija **Darbinieku rezultāti** parāda informāciju par pašu apstrādi, kā arī visām apstrādes procesa laikā veiktajām atlīdzības darbībām. Sadaļā **Fiksēta atlīdzība** būs ieraksts katrai atlīdzības sistēmas apstrādes notikumā iekļautajai darbībai. Kolonnās **Pašreizējais norādījums** un **Ieteikums** būs redzama papildinformācija par sadaļā **Fiksēta atlīdzība** atlasīto darbību. Ja darbībai ir atzīmēta opcija **Iespējot ieteikumus**, ieteikumu lauki ir rediģējami. Tas ļaus manuāli koriģēt darbinieka summas. Ņemiet vērā, ka, ja apstrādes notikumā atzīmējāt **Izmantot iepriekšējo rezultātu**, jums ir manuāli jāatjaunina visas atkarīgo darbību summas.

Kad ir pārskatītas darbinieka atlīdzības summas un ir veiktas visas ieteicamo vērtību korekcijas, varat mainīt opciju **Statuss** rindā **Darbinieka notikums**, lai norādītu, vai notikums ir apstiprināts vai ir jāignorē. Ja vēlaties, varat dzēst visas izmaiņas, kas veiktas darbinieka ieteikumā, noklikšķinot uz pogas **Pārrēķināt**. Tas pašreizējam darbinieka notikumam iestatīs statusu Ignorēt un izveidos jaunu darbinieka notikumu ar pārrēķinātajām vērtībām.

## <a name="loading-approved-compensation-changes"></a>Apstiprināto atlīdzības izmaiņu ielāde
Kad viena vai vairāku darbinieku notikumu statuss ir atjaunināts uz Apstiprināts, tos var ielādēt darbinieku fiksētās atlīdzības ierakstos. To var izdarīt, lapā **Darbinieku rezultāti** atsevišķi atlasot katru darbinieka notikumu un noklikšķinot uz pogas **Ielādēt darbinieka atlīdzību** vai lapā **Apstrādes rezultāti** noklikšķinot uz **Ielādēt atlīdzību**, lai vienlaikus ielādētu visus apstiprinātos darbinieka notikumus.

Dialogā **Atlīdzības ielāde** noklikšķinot uz **Labi**, lapā **Darbinieku fiksētā atlīdzība** tiks pievienotas atlīdzības darbības rindas ar vērtību, kas nav nulle.
