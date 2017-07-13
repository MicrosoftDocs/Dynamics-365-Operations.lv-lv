---
title: "Atlīdzības apstrāde"
description: "Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6e30357b0bca8745b69bff19a55828b180c3b829
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="process-compensation"></a>Atlīdzības apstrāde
Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju. Šajā emuāra ziņā tiek skaidrota fiksētas atlīdzības plāna atlīdzības apstrādes pamata plūsma bez faktoringa veiktspējas.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Jaunu atlīdzības summu plānošana un ietveršana budžetos
Lai saviem darbiniekiem piešķirtu nopelnu pielikumu, katrai nodaļai ir jāiestata fiksēts pielikuma budžets : Kompensāciju pārvaldība > Saites > Nopelnu palielinājuma mērķi. (Varat arī atvērt šo formu no nodaļas: Organizācija > Nodaļas.) Šeit varat turpmāk noteikt, vai darbiniekiem, kas ir noteiktu arodbiedrību dalībnieki vai atrodas noteiktā atrašanās vietā, vajadzētu saņemt citu palielinājuma procentu. Lauki **Budžets** un **Valūta** ir informatīvi. Tos var izmantot, lai norādītu budžeta valūtas summu.

## <a name="set-up-the-compensation-process"></a>Atlīdzības apstrādes iestatīšana
Procesa notikums ļauj norādīt atlīdzības apstrādes parametrus. Tas ietver datumu periodu, kad jānovērtē atlīdzības summu noteikšana.  un datumu, kad jāstājas spēkā jaunajām atlīdzības summām.

Pēc izvēles var ietvert fiksētu algu pēc novērtētā nomas datuma, ja kāds no fiksētās atlīdzības plāniem izmanto darbā pieņemšanas nosacījumu vai procentus. Šajos plānos ikvienam, kurš tika pieņemts pēc cikla sākuma datuma un pirms fiksētā algas pēc novērtētā nomas datuma, saņems 100% no aprēķinātā nopelna vai vispārējā palielinājuma. Ikviens, kas tika nolīgts pēc fiksētā algas pēc novērtētā nomas datuma un pirms cikla beigu datuma, saņems daļu no sava aprēķinātā palielinājuma, pamatojoties uz to, cik dienas no kopējā cikla dienu skaita tie bija nodarbināti. Piemēram, ja mūsu cikls ir no 1. janvāra līdz 31. decembrim un no 1. aprīļa sākas fiksētās maksas likmes nolīgšanas datums, darbinieks, kurš tiek pieņemts martā, saņems pilnu aprēķināto palielinājumu, bet darbinieks, kurš tiek pieņemts 1. jūlijā, saņems aptuveni pusi no aprēķinātā palielinājuma.

Apstrādes notikuma **Punkts laikā** datums tiek izmantots, tikai apstrādājot noteiktus mainīgās atlīdzības plānus, un nav ietverts šajā emuāra ziņā. **Pārskatīt termiņš** ir termiņš, kad jāveic visi ieteikumi, lai jauna atlīdzības summas var ielādēt darbinieka ierakstā. Pārskatīšanas datums ir tikai informatīvs.

Kad apstrādes notikuma parametri tiek saglabāti, varat noklikšķināt uz pogas **Iestatījumi** un norādīt plānus, kuros iekļaut šo apstrādes izpildi, un to, kuras fiksētās atlīdzības darbības ir jāveic katram plānam.

Noklikšķiniet uz pogas **Pievienot** augšējā cilnē un pievienojiet atlīdzības plānu apstrādes notikumam. Kolonna **Izmantot citus līdzekļus**, **Līdzekļu faktors** un **Līdzekļu apraksts** tiek izmantota tikai mainīgās atlīdzības plāniem un nav ietverta šajā tēmā.

Saglabājiet ierakstu un pēc tam noklikšķiniet uz pogas **Pievienot** apakšējā cilnē, lai fiksētās atlīdzības darbības pievienotu atlasītajam plānam. Izmantojiet opciju Iespējot ieteikumus, lai varētu ievadīt citu summu, kas nav iekļauta apstrādei aprēķinātajā algas palielinājumā. Ja darbību vēlaties aprēķināt, pamatojoties uz iepriekšējās darbības rezultātiem, un saistīt vairākas atlīdzības darbības, atlasiet opciju Izmantot iepriekšējo rezultātu. Fiksētās atlīdzības darbības ir kompensācijas loģikas veidi, kam varat dot aprakstošus nosaukumus. Līmeņa un joslas plāniem varat pievienot tikai tālāk minēto veidu fiksētās atlīdzības darbības.

| Fiksētās atlīdzības veids | Funkcionalitāte                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kapitāls                        | Kapitāla darbības salīdzinās darbinieka samaksas likmi no cikla beigu datuma ar zemāko atskaites punktu un darbinieka darbā norādīto līmeni. Ja darbinieka samaksas likme ir mazāka par minimālo atsauces punktu, tiks aprēķināts palielinājums, kas nepieciešams, lai darbinieku novirzītu uz minimālo punktu diapazonā.                                                                                |
| Nopelni                         | Nopelnu darbības aprēķinās pieaugumu, pamatojoties uz darbinieka algas likmi no cikla beigu datuma, un pieauguma procentus, kas atrodami darbinieka nodaļas fiksēts pielikuma budžetā, arodbiedrībā un atrašanās vietā.                                                                                                                                                                                         |
| Vispārējs                       | Vispārīgas darbības aprēķinās pieaugumu, pamatojoties uz procentiem, vai piešķirs darbiniekiem pamatsummu. Tas tiek noteikts, pamatojoties uz cilnes Vispārīgi sadaļā Fiksēta atlīdzība esošajiem iestatījumiem.                                                                                                                                                                                                                        |
| Izplatīšana                     | Veicināšanas pasākumi sniedz konkrētu atrašanās vietu, kur var piešķirt pieaugumu, tāpēc noteikti atlasiet opciju **Iespējot ieteikumus**, lai varētu ievadīt ieteikums darbiniekiem, kuri saņems veicināšanas pasākumus.  Darbiniekiem bez ieteikta palielinājuma veicināšanas pasākums netiks pievienots viņu fiksētās atlīdzības ierakstiem.                                                                       |
| Citu līmeņu maiņa            | Iepriekšējā piemērā Pazemināšana ir mūsu fiksētas atlīdzības darbības nosaukums ar cita veida līmeņa izmaiņām. Tas ģenerē 0 (nulle izmaiņas) vadlīniju palielinājumu, tādēļ varat ievadīt ieteikto summu, lai koriģētu darbinieka algas likmi. (Noteikti atlasiet opciju **Iespējot ieteikumus**.) Darbiniekiem bez ieteikuma šī darbība netiks pievienota fiksēto kompensāciju ierakstiem. |

Pakāpes plānam fiksēto kompensāciju darbības var pievienot tikai ar veidu Pakāpe.

| Fiksētās atlīdzības darbības veids | Funkcionalitāte                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Solis                           | Cilnē Vispārīgi norāda, vai šai darbībai jāpārvieto darbiniek uz priekšu par nulle darbībām, vienu darbību vai divām darbībām.                                                                                  |
|                                | **Nulle darbības** — darbinieks saņems pašreizējas darbības algas likmi.                                                                                                                      |
|                                | **Viena darbība** — sistēma pārbauda, vai darbinieks jau ir sava līmeņa pēdējā atsauces punktā.                                                                                             |
|                                | **Divas darbības** — sistēma pārvietos darbinieku uz priekšu par divām darbībām pašreizējā līmenī. Ja darbinieks sasniedz pēdējo līmeņa atsauces punktu, sistēma darbinieku var pārvietot tikai par vienu vai nulle darbībām. |

## <a name="run-the-compensation-process"></a>Atlīdzības procesa palaišana
Kad apstrādes notikumam ir iestatīti nepieciešamie datumu lauki, plāni un darbības, notikuma apstrādes lapā varat noklikšķināt uz **Palaist procesu**. Tādējādi tiek atvērts dialogs Palaist atlīdzības procesu notikumus. Šajā dialogā noklikšķiniet uz opcijas **Rādīt pārstrādes rezultātus**, lai skatītu, kā atlīdzības summas tika aprēķinātas katram darbiniekam. Noklikšķinot uz **Labi**, tiks palaists atlīdzības process visiem darbiniekiem, kuri atlasītajos atlīdzības plānos ir no cikla beigu datumam.

## <a name="view-the-process-results"></a>Apstrādes rezultātu skatīšana
Lai skatītu apstrādes rezultātus, atveriet lapu **Procesa rezultāti**. Katru reizi, kad tiek palaists procesa notikums, tiek izveidots jauns atlīdzības notikums. Šādā veidā var veikt izmēģinājuma palaides, veikt korekcijas un vairākkārt palaist atlīdzības notikumu, lai redzētu, kā dažādas izmaiņas ietekmē darbinieku atlīdzību.

Procesa rezultātu lapā ir ietverta informācija par procesa izpildi, tostarp, kad izpilde notika, lietotājs, kurš sāka procesu, un vai procesa izpildes laikā radās kļūdas. Varat arī atlasīt opciju **Bloķēts**, lai atspējotu pogu **Ielādēt atlīdzību** un nevienam neļautu ielādēt atlīdzības notikumus darbinieka ierakstos. Noklikšķinot uz pogas **Darbinieku rezultāti**, tiks parādīts to darbinieku saraksts, kas iekļauti palaidē.

Darbinieka rezultāti parāda informāciju par procesu, kā arī visām atlīdzības darbībām, kas veiktas procesā. Sadaļa Fiksēta atlīdzība satur katras procesa notikuma atlīdzības plānam iekļautās darbības ierakstu. Kolonnas Pašreizējā vadlīnija un Ieteikumi parādīs papildinformāciju par sadaļā Fiksēta atlīdzība atlasīto darbību. Ja darbībai ir atlasīta opcija Iespējot ieteikumus, ieteikumu lauki būs rediģējami. Tas ļaus manuāli koriģēt darbinieka summas. Piezīme. Ja procesa notikumā atlasījāt opciju Izmantot iepriekšējo rezultātu, ir manuāli jāatjaunina visas atkarīgo darbību summas.

Kad darbinieku atlīdzības summas ir pārskatītas un visas ieteicamo vērtību korekcijas ir veiktas, varat mainīt opciju **Statuss** rindā **Darbinieka notikums**, lai norādītu, vai notikums tika apstiprināts vai ir jāignorē. Ja vēlaties, varat dzēst visas izmaiņas, kas veiktas darbinieka ieteikumā, noklikšķinot uz pogas **Pārrēķināt**. Tas pašreizējam darbinieka notikumam iestatīs statusu Ignorēt un izveidos jaunu darbinieka notikumu ar pārrēķinātajām vērtībām.

## <a name="loading-approved-compensation-changes"></a>Apstiprināto atlīdzības izmaiņu ielāde
Pēc tam, kad viena vai vairāku darbinieku notikumu statuss tika atjaunināts uz Apstiprināts, tos var ielādēt darbinieka fiksētās kompensācijas ierakstos. To var izdarīt, darbinieka rezultātu lapā atsevišķi atlasot katru darbinieka notikumu un noklikšķinot uz pogas Ielādēt darbinieka atlīdzību vai procesa rezultātu lapā noklikšķinot uz pogas **Ielādēt atlīdzību**, lai vienlaicīgi ielādētu visus apstiprinātos darbinieka notikumus.

Dialogā **Atlīdzības ielāde** noklikšķinot uz **Labi**, lapā **Darbinieku fiksētā atlīdzība** tiks pievienotas atlīdzības darbības rindas ar vērtību, kas nav nulle.

