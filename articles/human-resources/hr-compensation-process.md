---
title: Atlīdzības apstrāde
description: Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7c72f866886f320d8a7fa22d6ccfa7e43284b5bf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071743"
---
# <a name="process-compensation"></a>Atlīdzības apstrāde


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Atlīdzības apstrāde dod iespēju aprēķināt jaunas bāzes atlīdzības summas jūsu darbiniekiem, pamatojoties uz kapitāla korekcijām, nopelnu palielinājuma mērķiem un veiktspēju. Šajā tēmā ir sniegta informācija par fiksētās atlīdzības sistēmu atlīdzības apstrādes pamata plūsmu, neņemot vērā darbinieka sniegumu.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Jaunu atlīdzības summu plānošana un ietveršana budžetos
Lai saviem darbiniekiem piešķirtu nopelnu palielinājumu, katrai nodaļai ir jāiestata fiksēts palielinājuma budžets: **Atlīdzību pārvaldība** >  **Saites** > **Nopelnu palielinājuma mērķi**. (Šo formu var atvērt arī no nodaļas sadaļas: **Organizācija**  > **Nodaļas**.) Varat tālāk norādīt, vai darbiniekiem, kas ir noteiktu arodbiedrību dalībnieki vai atrodas noteiktā atrašanās vietā, ir jāsaņem atšķirīgs palielinājuma procents. Lauki **Budžets** un **Valūta** ir informatīvi. Tos var izmantot, lai norādītu budžeta valūtas summu.

## <a name="set-up-the-compensation-process"></a>Atlīdzības apstrādes iestatīšana
Lapā **Atlīdzību procesi** varat norādīt atlīdzību apstrādes parametrus. Tas ietver arī izvērtējamo datumu periodu atlīdzības summu noteikšanai un datumu, kurā jaunajām atlīdzības summām jāstājas spēkā.

Pēc izvēles varat ietvert **fiksētās maksas likmes nolīgšanas datumu**, ja kāda no fiksētās atlīdzības sistēmām izmanto nolīgšanas kārtulu Procenti. Šajās sistēmās ikviens, kurš tika pieņemts pēc **cikla sākuma** datuma un pirms **fiksētās maksas likmes nolīgšanas datuma**, saņems 100% no aprēķinātā nopelna vai vispārējā palielinājuma. Ikviens, kas tika nolīgts pēc **fiksētās maksas likmes nolīgšanas datuma** un pirms **cikla beigu datuma**, saņems daļu no sava aprēķinātā palielinājuma, pamatojoties uz to, cik dienas no kopējā cikla dienu skaita tie bija nodarbināti. Piemēram, ja cikls ir no 1. janvāra līdz 31. decembrim un no 1. aprīļa sākas fiksētās maksas likmes nolīgšanas datums, darbinieks, kurš tiek pieņemts martā, saņems pilnu aprēķināto palielinājumu, bet darbinieks, kurš tiek pieņemts 1. jūlijā, saņems aptuveni pusi no aprēķinātā palielinājuma.

Apstrādes notikuma **Punkts laikā** datums tiek izmantots, apstrādājot tikai noteiktas mainīgās atlīdzības sistēmas, un tas nav šeit aplūkots. **Pārskatīt termiņš** ir termiņš, kad jāveic visi ieteikumi, lai jauna atlīdzības summas var ielādēt darbinieka ierakstā. Pārskatīšanas datums ir tikai informatīvs.

Pēc apstrādes notikuma parametru saglabāšanas varat noklikšķināt uz pogas **Iestatījumi**, lai atlasītu iekļaujamās sistēmas, kad tiek izpildīts šis process, un to, kuras fiksētās atlīdzības darbības ir jāveic katrai sistēmai.

Noklikšķiniet uz pogas **Pievienot** cilnē **Sistēmas**, lai apstrādes notikumam pievienotu atlīdzības sistēmu. Kolonnas **Izmantot citus līdzekļus**, **Līdzekļu faktors** un **Līdzekļu apraksts** tiek izmantotas tikai mainīgās atlīdzības sistēmām un nav aplūkotas šajā tēmā.

Saglabājiet ierakstu un pēc tam noklikšķiniet uz pogas **Pievienot** cilnē **Darbības**, lai atlasītajai sistēmai pievienotu fiksētās atlīdzības darbības. Izmantojiet opciju **Iespējot ieteikumus**, lai ievadītu summu, kas atšķiras no darbībai aprēķinātā algas palielinājuma. Lai aprēķinātu darbību, kas balstīta iepriekšējās darbības rezultātā, lai saistītu vairākas atlīdzību darbības, atzīmējiet opciju **Lietot iepriekšējo rezultātu**. Fiksētās atlīdzību darbības ir atlīdzību loģikas veidi, kuriem varat piešķirt aprakstoŠis nosaukumus. Kategoriju **un** **grupu** plāniem var pievienot tikai tās fiksētās atlīdzības darbības, kuru tips ir šāds:

| Fiksētās atlīdzības darbības veids | Funkcionalitāte                  |
|-------------------------------|-------------------------------------------------------------------------|
| Kapitāls                        | Kapitāla darbības salīdzinās darbinieka samaksas likmi no cikla beigu datuma ar zemāko atskaites punktu un darbinieka darbā norādīto līmeni. Ja darbinieka apmaksas likme ir mazāka par minimālo atsauces punktu, tiks aprēķināts palielinājums, kas nepieciešams, lai darbinieku novirzītu uz minimālo punktu diapazonā.                                                                                |
| Nopelni                         | Nopelnu darbības aprēķinās palielinājumu, pamatojoties uz darbinieka apmaksas likmi no cikla beigu datuma, un palielinājuma procentus, kas atrodami fiksētā palielinājuma budžetā darbinieka nodaļai, arodbiedrībai un atrašanās vietai.                                                                                                                                                                                         |
| Vispārējs                       | Vispārīgās darbības aprēķinās palielinājumu, pamatojoties uz procentu, vai arī piešķirs darbiniekiem pamatsummu. Tas tiek noteikts, pamatojoties uz sadaļas **Fiksēta atlīdzība** iestatījumiem cilnē **Vispārīgi**.                                                                                                                                                                                                                        |
| Izplatīšana                     | Paaugstināšanas darbības nodrošina nodēvētu vietu, kurā varat piešķirt pieaugumus. Atzīmējiet opciju **Iespējot rekomendāciju**, lai ievadītu rekomendāciju par darbiniekiem, kuri saņems paaugstinājumu.  Darbiniekiem bez ieteikta palielinājuma darbība **Paaugstināšana amatā** netiks pievienota viņu fiksētās atlīdzības ierakstiem.                                                                       |
| Citu līmeņu maiņa            | Iepriekšējā piemērā **Pazemināšana** ir nosaukums darbībai **Fiksēta atlīdzība** ar tipu **Citu līmeņu maiņa**. Tas ģenerē 0 (nulle izmaiņas) vadlīniju palielinājumu, tādēļ varat ievadīt ieteikto summu, lai koriģētu darbinieka algas likmi. (Atlasiet opciju **Iespējot ieteikumus**.) Darbiniekiem bez ieteikuma šī darbība netiks pievienota fiksētās atlīdzības ierakstiem. |

Pakāpju sistēmai var pievienot tikai sadaļas **Fiksēta atlīdzība** darbības ar tipu Pakāpe.

| Fiksētās atlīdzības darbības veids | Funkcionalitāte                |
|--------------------------------|------------------------------|
| Solis                           | Cilnē **Vispārīgi** norādiet, vai šai darbībai jāpārvieto darbiniek uz priekšu par nulle darbībām, vienu darbību vai divām darbībām.                                                                                  |
|                                | **Nulle darbības** — darbinieks saņems pašreizējas darbības algas likmi.                                                                                                                      |
|                                | **Viena darbība** — sistēma pārbauda, vai darbinieks jau ir sava līmeņa pēdējā atsauces punktā.                                                                                             |
|                                | **2 soļi** - Darbinieks virzīsies uz priekšu divus soļus pašreizējā līmenī. Darbinieks var veikt tikai vienu vai nulles soli, ja sasniedz pēdējo atskaites punktu savam līmenim. |

## <a name="run-the-compensation-process"></a>Atlīdzības procesa palaišana
Kad apstrādes notikumam ir iestatīti nepieciešamie datumu lauki, sistēmas un darbības, lapā **Apstrādes notikums** varat noklikšķināt uz **Palaist procesu**, tādējādi tiks atvērts dialoglodziņš **Palaist atlīdzību procesa notikumus**. Noklikšķiniet uz opcijas **Rādīt pārstrādes rezultātus**, lai skatītu, kā atlīdzības summas tika aprēķinātas katram darbiniekam. Noklikšķinot uz **Labi**, tiks palaists atlīdzības process visiem darbiniekiem, kuri atlasītajos atlīdzības plānos ir no cikla beigu datumam.

## <a name="view-the-process-results"></a>Apstrādes rezultātu skatīšana
Lai skatītu apstrādes rezultātus, atveriet lapu **Procesa rezultāti**. Katru reizi, kad tiek palaists procesa notikums, tiek izveidots jauns atlīdzības notikums. Šādā veidā var veikt izmēģinājuma palaides, veikt korekcijas un vairākkārt palaist atlīdzības notikumu, lai redzētu, kā dažādas izmaiņas ietekmē darbinieku atlīdzību.

Lapā **Apstrādes rezultāti** ir ietverta informācija par apstrādes izpildi, tostarp informācija par to, kad izpilde notika, lietotāju, kurš palaida apstrādi, un to, vai apstrādes izpildes laikā radās kļūdas. Atlasiet opciju **Bloķēts**, lai atspējotu pogu **Ielādēt atlīdzību** un nevienam neļautu ielādēt atlīdzības notikumus darbinieka ierakstos. Noklikšķinot uz pogas **Darbinieku rezultāti**, tiks parādīts to darbinieku saraksts, kas iekļauti palaidē.

Opcija **Darbinieku rezultāti** parāda informāciju par pašu apstrādi, kā arī visām apstrādes procesa laikā veiktajām atlīdzības darbībām. Sadaļā **Fiksēta atlīdzība** būs ieraksts katrai atlīdzības sistēmas apstrādes notikumā iekļautajai darbībai. Kolonnās **Pašreizējais norādījums** un **Ieteikums** būs redzama papildinformācija par sadaļā **Fiksēta atlīdzība** atlasīto darbību. Ja darbībai ir atzīmēta opcija **Iespējot ieteikumus**, **ieteikumu** lauki ir rediģējami. Tas ļaus manuāli koriģēt darbinieka summas. Ņemiet vērā, ka, ja apstrādes notikumā atzīmējāt **Izmantot iepriekšējo rezultātu**, jums ir manuāli jāatjaunina visas atkarīgo darbību summas.

Kad ir pārskatītas darbinieka atlīdzības summas un ir veiktas visas ieteicamo vērtību korekcijas, varat mainīt opciju **Statuss** rindā **Darbinieka notikums**, lai norādītu, vai notikums ir apstiprināts vai ir jāignorē. Ja vēlaties, varat dzēst visas izmaiņas, kas veiktas darbinieka ieteikumā, noklikšķinot uz pogas **Pārrēķināt**. Tas pašreizējam darbinieka notikumam iestatīs statusu Ignorēt un izveidos jaunu darbinieka notikumu ar pārrēķinātajām vērtībām.

## <a name="loading-approved-compensation-changes"></a>Apstiprināto atlīdzības izmaiņu ielāde
Kad viena vai vairāku darbinieku notikumu statuss ir atjaunināts uz **Apstiprināts**, tos var ielādēt darbinieku fiksētās atlīdzības ierakstos. To var izdarīt, lapā **Darbinieku rezultāti** atsevišķi atlasot katru darbinieka notikumu un noklikšķinot uz pogas **Ielādēt darbinieka atlīdzību** vai lapā **Apstrādes rezultāti** noklikšķinot uz **Ielādēt atlīdzību**, lai vienlaikus ielādētu visus apstiprinātos darbinieka notikumus.

Dialogā **Atlīdzības ielāde** noklikšķinot uz **Labi**, lapā **Darbinieku fiksētā atlīdzība** tiks pievienotas atlīdzības darbības rindas ar vērtību, kas nav nulle.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
