---
title: Fiksētās atlīdzības plānu izveidošana
description: Šajā tēmā ir aprakstīti komponenti, kas ir jāiestata, lai varētu izveidot fiksētas atlīdzības plānu un reģistrēt darbiniekus.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable, HcmCompensationWorkspace
audience: Application User
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 05f4748f66f4027972aabf53e7a1c237b8dbb543
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693064"
---
# <a name="create-a-fixed-compensation-plans"></a>Fiksētās atlīdzības plānu izveidošana


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fiksēta atlīdzība attiecas uz darbinieka regulāro bruto algu vai darba samaksu. Šajā tēmā ir aprakstīti komponenti, kas ir jāiestata, lai varētu izveidot fiksētas atlīdzības plānu un reģistrēt darbiniekus.

Fiksētas atlīdzības summas saviem darbiniekiem var aprēķināt, pamatojoties uz tādiem faktoriem kā sniegums, reģions un budžeta palielinājums. Dynamics 365 Human Resources atbalsta darbības, pakāpes un indeksa atlīdzības veidus.

## <a name="fixed-compensation-components"></a>Fiksētas atlīdzības komponenti
### <a name="compensation-levels"></a>Atlīdzības līmeņi

Lai iestatītu atlīdzību par dažādiem darbiem, tādējādi nodrošinot, ka darbiniekiem, kuri veic šos darbus, tiek samaksāts godīgi, varat izmantot **Atlīdzības līmeņus**. Lapā **Atlīdzības līmeņi** varat iestatīt atlīdzības līmeņus, kas ir nepieciešami katrai darbībai, pakāpei un indeksu plānam. Izmantojiet pogu **Augšup** un **Lejup**, lai iestatītu līmeņus pareizā secībā atbilstoši to veidam. Iestatot atlīdzības līmeņus par darbu, tiek nodrošināts, ka visiem darbiniekiem, kas veic šo darbu, tiek maksāta vienāda līmeņa atlīdzība.

### <a name="reference-points"></a>Atsauces punkti

**Atsauces punkti** ir kolonnas režģī, kas nosaka atlīdzību diapazonus katram līmenim. Atlīdzības līmenis ir rinda režģī. Tipiski pakāpju plāna atsauces punkti ir minimālā, vidējā un maksimālā atlīdzība. Atsauces punkti ir jāizveido lapā **Atsauces punkta iestatījumi**.

### <a name="compensation-grids"></a>Kompensāciju režģi

Pēc līmeņu un atsauces punktu iestatīšanas tos var apvienot, lai izveidotu **Atlīdzības režģi**. Lapā **Atlīdzību režģi** definējiet informāciju par režģi. Piemēram, norādiet, kādam nolūkam režģi paredzēts izmantot, kāda veida plānā tas tiks lietots un kuri atsauces punkti vai kolonnas ir nepieciešami režģī. Kad šī informācija ir ievadīta, noklikšķiniet uz **Atlīdzības struktūra**, lai režģim pievienotu līmeņus un summas. 

**Padoms.** Izmantojiet funkciju **Masveida izmaiņas** atlīdzību struktūrā, lai iestatītu sākotnējās summas, un pēc tam palieliniet procentuāli vai pēc summas dažādos līmeņos vai atsauces punktos.

### <a name="pay-frequencies"></a>Algas izmaksas biežums

**Apmaksas biežums** tiek izmantots, lai definētu, kā darbinieka alga tiek norādīta (piemēram $10 stundā vai 50 000 gadā), un stundu, nedēļas, mēneša (12 mēnešu) un gada likmju pārveidi. Piemēram, uzņēmums, kas izmanto 38 stundu darba nedēļu darbiniekiem, kam maksā par nostrādātajām stundām, iestata algas izmaksas biežumu, kas ir stundu likme 1, nedēļas likme 38, mēneša likme 164,6666666667 un gada likme 1976. Šāda pārveide tiek izmantota, lai aprēķinātu dažādas samaksas likmes, kas ir ietvertas darbinieku fiksētas atlīdzības ierakstos.

## <a name="fixed-compensation-plans"></a>Fiksētas atlīdzības struktūras
Varat izveidot fiksētas atlīdzības plānu, lai apvienotu visus komponentus, ko esat konfigurējis. Lai izveidotu fiksētas atlīdzības plānu, atveriet lapu **Fiksētas atlīdzības plāni**. Šeit varat piešķirt plānam nosaukumu un aprakstu, atlasīt, kāda veida plāns tas ir (darbību, pakāpju vai indeksa), atlasīt algas izmaksas biežumu, ko izmantosit darbinieka algas izmaksai(summa stundā, summa gadā un tā tālāk), un iestatīt atsevišķas opcijas, kas kontrolē, kā tiek apstrādāta atlīdzība. 

Izmantojot iestatījumu **Tolerance ārpus diapazona**, varat norādīt, cik stingri jānodrošina, ka atlīdzības summas ir starp minimālo un maksimālo summu. Tolerance **Stingri** paredz, ka atlīdzība būs diapazonā, kas definēts noteiktajam līmenim. Tolerance **Nestingri** brīdina, ja atlīdzības summa ir ārpus diapazona, bet ļauj turpināt. Ja iestatāt toleranci **Nav**, varat ievadīt jebkuru atlīdzības summu darbiniekam, un nesaņemsit brīdinājumus vai kļūdas ziņojumus. 

Izmantojot iestatījumu **Nolīgšanas kārtula**, varat norādīt, ka visiem darbiniekiem ir jāsaņem vienāds palielinājums neatkarīgi no datuma, kurā tie tika pieņemti darbā (**Nolīgšanas kārtula** = **Nav**), vai ka darbiniekiem ir jāsaņem procenti no piemaksas, ņemot vērā, cik ilgi tie bija nodarbināti cikla laikā (**Nolīgšanas kārtula** = **Procenti**). 

**Diapazona izmantošanas matrica** ir noderīga, ja vēlaties vai nu samazināt laiku, kas nepieciešams darbiniekiem, lai sasniegtu viņiem iestatītā diapazona vidus punktu, vai palielināt laiku, kas nepieciešams darbiniekiem, lai sasniegtu maksimālo atsauces punktu diapazonā. Piemēram, ja vēlaties, lai darbiniekiem, kam ir iestatīts diapazons 110 % ar maksimālo robežvērtību 25 %, bet kam ir sasniegta minimālā robežvērtība 25 %, tiktu samaksāti tikai 80 % no mērķa atlīdzības, lai viņi tik ātri nesasniedz maksimālo robežvērtību. 

Kad ir noteikta fiksētas atlīdzības plāna pamatinformācija, varat iestatīt plānam atlīdzības struktūru. Noklikšķiniet uz **Iestatīt atlīdzību**. Tiek atvērts dialoga slīdnis ar trim opcijām:

-   **izveidojiet jaunu atlīdzības režģi**, atlasot atsauces punkta iestatījumus un piešķirot režģim nosaukumu;
-   **Izveidojiet jaunu atlīdzības režģi**, izveidojot esoša režģa kopiju, ko var izmantot kā sākuma punktu;
-   **Izmantojiet esošu atlīdzības režģi**, kas jau ir definēts. Visi atlīdzības plāni, kas izmanto vienu režģi, saņems atjauninājumus, ja attiecīgais režģis tiek rediģēts.

Kad esat atlasījis opciju, atveras lapa **Atlīdzības struktūra**, kurā varat veikt izmaiņas jaunajā vai esošajā atlīdzības režģī.

## <a name="fixed-compensation-enrollment"></a>Reģistrācija fiksētai atlīdzībai
### <a name="determine-who-is-eligible-for-the-plan"></a>Noteikšana, kurš ir piemērots plānam

Reģistrējot darbiniekus fiksētas atlīdzības plānam, vispirms ir jānosaka, kurš ir piemērots atlīdzībai, kas noteikta plānā. Līdz brīdim, kad tiek noteikta piemērotība, nevarēsit plānu piešķirt visiem darbiniekiem. Lai iestatītu piemērotību, atveriet lapu **Piemērotības kārtulas**. Šajā lapā varat izveidot jaunu piemērotība kārtulu savam atlīdzības plānam un noteikt kritērijus, kādiem darbiniekam ir jāatbilst, lai varētu tikt reģistrēts plānam. Piemērotības kritērijos var ietvert tādus vienumus kā nodaļa, arodbiedrība, atlīdzības reģions (atrašanās vieta), darbs, darba funkcija, darba veids vai atlīdzības līmenis. Darbinieki var tikt reģistrēti atlīdzības plānam tikai tad, ja tie atbilst visiem nosacījumiem, kas iestatīti piemērotības kārtulā. 

**Piezīme.** Piemērotības kārtulas tiek lietotas, lai noteiktu piemērotību gan fiksētas, gan mainīgās atlīdzības plānam. 

Piemērotības kārtulā tiek ņemta vērā konkrētu ieraksta **Darbs**, **Amats** un **Darbinieks** lauku vērtība, lai noteiktu, vai darbinieks piemērots atlīdzības plānam.

-   Lapā **Darbs** piemērotības kārtulā tiek ņemta vērā šādu lauku vērtība:
    -   lauka **Darbs** vērtība;
    -   cilnē **Darbu klasifikācija** lauka **Funkcija** un **Darba veids** vērtība;
    -   cilnē **Atlīdzība** lauka **Līmenis** vērtība;
-   lapā **Pozīcijas** piemērotības kārtulā tiek ņemta vērā lauka **Nodaļa** un **Atlīdzības reģions** vērtība.

Piemērotības kārtulā tiek ņemtas vērā arī arodbiedrības, kas ir saistītas ar darbinieku (lapas **Darbinieki** cilnē **Darbinieks** noklikšķiniet uz **Personīgā informācija** &gt; **Arodbiedrības**).

### <a name="define-fixed-compensation-actions"></a>Fiksētas atlīdzības darbību definēšana

Lapa **Fiksētās atlīdzības darbības** tiek izmantota, kad iestatāt darbiniekam fiksētu atlīdzību vai lietojat tai izmaiņas. Fiksētas atlīdzības darbības ļauj sniegt aprakstošu nosaukumu darbību veidiem, ko var veikt darbinieks ar lomu Atlīdzību un atvieglojumu vadītājs. Dažādiem darbību veidiem ir īpaša loģika, lai tos varētu izmantot noteiktos laikos. 

Piemēram, ja darbiniekam ir iestatīta fiksētā atlīdzība, var izmantot tikai darbība, kam ir veids **Pieņemt darbā/Atkārtoti pieņemt darbā**. Šajā gadījumā ieteicams izveidot trīs dažādas darbības veidam **Pieņemt darbā/Atkārtoti pieņemt darbā** un piešķirt tām nosaukumu **Pieņemt darbā**, **Atkārtoti pieņemtu darbā** un **Pārcelt**. Pēc tam ir aprakstošāks paskaidrojums, kāpēc fiksētā atlīdzība tika piešķirta darbiniekam vai mainīta.

### <a name="enroll-the-employee"></a>Darbinieka reģistrēšana

Tagad var piešķirt darbiniekam fiksētas atlīdzības plānu. Lapā **Darbinieki** atlasiet darbinieku, ko reģistrēt atlīdzības plānam. Darbību rūtī noklikšķiniet uz **Atlīdzība** &gt; **Fiksēts plāns**. Tagad varat izveidot jaunu fiksētas atlīdzības darbību šim darbiniekam. 

**Piezīme**. **Atlīdzības plāna** laukā tiek rādīti tikai tie plāni, kuriem darbinieks ir piemērots saskaņā ar piemērotības nosacījumiem, kas tika iestatīti katram plānam. Ja plānam nav iestatīta neviena piemērotības kartula, neviens darbinieks nebūs piemērots šim plānam. 

Sistēma pārbaudīs, vai atlīdzības summa, kas norādīta atlīdzības plānā ar pakāpes vai indeksa veidu, ir starp noteikto darbinieka darba atlīdzības līmeņa minimālo un maksimālo atsauces punktu. Ja atlīdzības summa ir ārpus atļautā diapazona, atkarībā no tolerances līmeņa, kas ir iestatīts fiksētas atlīdzības plānā, tiek parādīts brīdinājums vai kļūdas ziņojums.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
