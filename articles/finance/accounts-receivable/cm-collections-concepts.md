---
title: Kolekciju pārvaldības galvenie jēdzieni
description: Šajās tēmās definēti iekasēšanas pārvaldības galvenie jēdzieni.
author: JodiChristiansen
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 508723752ec7ae5f48e52c728b6ef526ec49e4e2
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723028"
---
# <a name="collections-management-key-concepts"></a>Kolekciju pārvaldības galvenie jēdzieni

[!include [banner](../includes/banner.md)]

Pirms sākat iekasēšanas darbību iestatīšanu vai apstrādi, jums ir jāsaprot tālāk norādītās koncepcijas.

- Debitora vecumstruktūru momentuzņēmumi satur vecu bilances informāciju par noteiktu laika periodu.
- Iekasēšanas debitoru kopa palīdz organizēt darbu.
- Iekasēšanas aģentiem var būt savas debitoru kopas.
- Sarakstu lapās ir sakārtoti iekasēšanas debitori, aktivitātes un gadījumi.
- Visa iekasēšanas informācija par noteiktu debitoru ir pieejama vienā lapā, un šajā lapā varat veikt darbības.
- Procentus un nodevas var atcelt, atjaunot vai mainīt vienā darbībā.
- Norakstīšanas transakcijas var izveidot, veicot vienu darbību.
- Nepietiekamu naudas līdzekļu (NSF) maksājumus var apstrādāt, veicot vienu darbību.

Šajā tēmā ir aprakstīts katrs jēdziens.

## <a name="customer-aging-snapshots"></a>Debitora vecumstruktūru momentuzņēmumi

Vecumstruktūras momentuzņēmums satur vecas debitora bilances par noteiktu laika periodu. Šī informācija tiek rādīta saraksta lapā **Vecas bilances** un lapā **Iekasēšana**. Lai varētu skatīt informāciju par iekasēšanas saraksta lapām (**Novecojušas bilances**, **iekasēšanas darbības** un **Iekasēšanas gadījumi**), ir jāizveido vecumstruktūras momentuzņēmums.

Katra debitora vecumstruktūras momentuzņēmums satur vecumstruktūras momentuzņēmuma virsrakstu un datu ierakstus, kas atbilst katram vecumstruktūras periodam vecumstruktūras perioda definīcijā.

Vecumstruktūras momentuzņēmuma virsraksts satur debitora konta kopsummu apmaksai, kredīta limitu, pavadzīmes summu, pārdošanas pasūtījuma summu, apstrīdēto transakciju skaitu un apstrīdēto transakciju kopsummu. Šo summu aprēķinā tiek ietvertas visas debitora transakcijas. Kopsumma apmaksai, kredīta limits, pavadzīmes summa un pārdošanas pasūtījuma summa tiek rādīti papildinformācijas rūtī **Kredīta informācija** lapā **Iekasēšana**.

Katram vecumstruktūras periodam vecumstruktūras perioda definīcijā tiek izveidots vecumstruktūras momentuzņēmuma ieraksts. Katrs vecumstruktūras momentuzņēmuma datu ieraksts satur vecumstruktūras perioda ID un to transakciju kopsummu, kuru datumi ietilpst vecumstruktūras periodā. Transakcijas tiek piešķirtas vecumstruktūras periodam, piemēram, 30 dienas pēc izpildes termiņa. Datums ir relatīvs attiecībā pret **Vecumstruktūras** datuma vērtību, kas ir norādīta, izveidojot vecumstruktūras momentuzņēmumu. Šī informācija tiek rādīta saraksta lapā **Vecas bilances** un lapas **Iekasēšana** papildinformācijas rūtī **Vecas bilances**.

## <a name="collections-customer-pools"></a>Iekasēšanas debitoru kopas

Debitoru kopas ir vaicājumi, kas nosaka debitoru ierakstu grupu. Varat izmantot šos grupētos ierakstus, lai skatītu informāciju par iekļautajiem debitoru kodiem un lai pārvaldītu to kolekcijas vai novecošanas procesus. Jūs varat izmantot debitoru kopas, lai filtrētu informāciju iekasēšanas sarakstu lapās. Debitoru kopas varat arī izmantot, lai filtrētu debitoru kontus, kas tiek iekļauti vecumstruktūras momentuzņēmumu izveidošanas laikā.

## <a name="collections-agents"></a>Iekasēšanas aģenti

Pēc noklusējuma lietotāji var skatīt visu debitora informāciju iekasēšanas sarakstu lapās. Iekasēšanas aģentu ierakstus var izmantot, lai noteiktu debitoru kopas, kas ir pieejamas informācijas filtrēšanai iekasēšanas sarakstu lapās un lapā **Iekasēšana**.

Iekasēšanas aģenti strādā ar debitoriem, lai nodrošinātu, ka maksājumi tiek saņemti savlaicīgi. Viņi ir darbinieki, kas ir piešķirti lietotājiem lapā **Lietotāja iestatījumi**.

## <a name="collections-list-pages"></a>Iekasēšanas sarakstu lapas

Tālāk ir norādītas sarakstu lapas, kas palīdz sakārtot iekasēšanas informāciju.

- **Vecas bilances** — saraksta lapas kolonnās tiek parādītas debitoru bilances un vecās summas pēc vecumstruktūras perioda. Šī informācija tiek uzglabāta vecumstruktūras momentuzņēmumā. Vecumstruktūras periodus nosaka vecumstruktūras perioda definīcija, kas tiek lietota. Vecumstruktūras perioda definīcija ir aizgūta no debitoru kopas, ja tā ir norādīta kopas vaicājumam. Ja kopai nav vecumstruktūras perioda definīcijas, tiek izmantota noklusējuma vecumstruktūras perioda definīcija, kas ir norādīta lapā **Debitoru parādu parametri**. Ja noklusējuma vecumstruktūras perioda definīcija nav norādīta, tiek izmantota pirmā vecumstruktūras perioda definīcija no lapas **Vecumstruktūras perioda definīcijas**.
- **Kolekciju aktivitātes** — saraksta lapas kolonnās tiek rādītas aktivitātes, kas ir norādītas kā iekasēšanas aktivitātes. Šīs aktivitātes tiek izveidotas, izmantojot lapu **Iekasēšana**. Jūs izmantojat aktivitātes, lai izsekotu ar iekasēšanu saistīto darbu.
- **Atgādinājumu gadījumi** — saraksta lapas kolonnās tiek rādīta informācija par gadījumiem, kuru gadījuma kategorijas gadījuma veids ir **Iekasēšana**.

### <a name="aging-snapshots"></a>Vecumstruktūras momentuzņēmumi

Pirms varat skatīt informāciju iekasēšanas sarakstu lapās, ir jāizveido vecumstruktūras momentuzņēmums. Tiek rādīta informācija tikai par tiem debitoriem, kam ir izveidots vecumstruktūras momentuzņēmums. Saraksta lapā rādītos ierakstus var papildus filtrēt tālāk norādītajā veidā.

- Pēc noklusējuma lietotāji var piekļūt visiem debitoriem, kuriem ir vecumstruktūras momentuzņēmums.
- Ja pastāv debitoru kopas, lietotājam ir jābūt iestatītam kā iekasēšanas aģentam, lai viņš varētu izmantot kopas informācijas filtrēšanai iekasēšanas sarakstu lapās. Ir pieejama informācija tikai par debitoriem, kuri ir ietverti atlasītajā debitoru kopā.
- Ja lietotājs ir iestatīts kā iekasēšanas aģents, iekasēšanas saraksta lapās ir pieejamas tikai tās kopas, kas ir atlasītas konkrētajam iekasēšanas aģentam. Ja iekasēšanas aģentam lapā **Iekasēšanas aģents** ir atlasīta opcija **Ļaut aģentam skatīt visas debitoru kopas**, šim aģentam ir pieejamas visas kopas.

## <a name="collections-page"></a>Lapa Iekasēšana

Jūs varat izmantot lapu **Iekasēšana**, lai skatītu, pārvaldītu un izmantoto debitora iekasēšanas informāciju, aktivitātes un gadījumus.

Lapas augšējā sadaļā ir redzami atlasītā debitora gadījumi, vidējā sadaļā tiek rādītas debitora transakcijas un apakšējā sadaļa rāda debitora aktivitātes. Varat izveidot iekasēšanas gadījumus, lai izsekotu iekasēšanas informāciju par vienu vai vairākām transakcijām un aktivitātēm. Augšējā un apakšējā sadaļā redzamo informāciju var filtrēt pēc gadījuma.

Papildinformācijas rūtī tiek rādītas atlasītā debitora vecās bilances un kredīta limita informācija. Šī informācija tiek glabāta vecumstruktūras momentuzņēmumā. Ja nepieciešams, var atjaunināt vecumstruktūras momentuzņēmumu, izmantojot pašreizējo informāciju.

Darbību rūts satur pogas, kas ļauj skatīt saistīto informāciju par atlasīto debitoru, gadījumu, transakciju vai aktivitāti. Varat arī veikt vispārīgas darbības, piemēram, mainīt transakcijas iekasēšanas statusu, sūtīt e-pasta ziņojumus, izmantojot integrāciju ar jūsu e-pasta pakalpojumu sniedzējs, izmaksāt debitoriem kompensāciju, apstrādāt NSF maksājumus un norakstīt neiekasējamās bilances.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Procentu un nodevu atcelšana, atjaunošana vai anulēšana

Var atcelt, atjaunot vai anulēt veselus procentu paziņojumus vai procentu paziņojumos ietvertas maksas un transakciju procentus. Varat to izdarīt saraksta lapas **Visi debitori** darbību rūts cilnē **Apkopot**, noklikšķinot uz **Procentu paziņojums**, **Darbību procenti** vai **Maksa**.

Šīs korekcijas ietekmē tikai procentu paziņojumus un tajos ietvertos procentus un maksas. Lai iegūtu informāciju par to, kā norakstīt visas maksas, ko debitors ir parādā, skatiet šīs tēmas sadaļu [Norakstīšanas transakciju izveide](#creating-write-off-transactions).

Plašāku informāciju skatiet šeit: Procentu koda ar diapazonu izveidošana un šeit: Procentu apstrāde.

## <a name="creating-write-off-transactions"></a>Norakstīšanas transakciju izveide

Jūs varat norakstīt bojātos parādus , atlasot **Norakstīt** lapā **Iekasēšana** un iekasēšanas saraksta lapas.

Norakstot debitora transakcijas, visas debitora transakcijas tiek automātiski iezīmētas segšanai. Norakstītā summa ir atkarīga no iezīmēto transakciju neto summas. Vispārējā žurnālā tiek izveidota norakstīšanas transakcija, un tas var ietvert ne vairāk kā trīs veidu žurnāla rindas.

- Pirmā veida žurnāla rinda satur debitora norakstīšanas ierakstu. Ja iezīmētās transakcijas satur vairākas valūtas koda, dimensijas un grāmatošanas profila kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda.
- Otrā veida žurnāla rinda satur virsgrāmatas norakstīšanas ierakstu. Ja iezīmētās transakcijas satur vairākas valūtas koda, dimensijas un grāmatošanas profila kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda.
- Trešā veida žurnāla rinda satur virsgrāmatas norakstīšanas informāciju par PVN. Šī žurnāla rinda tiek izveidota tikai tad, ja lapā **Debitoru parādu parametri** ir atlasīta opcija **Atdalīt PVN**. Ja iezīmētās transakcijas satur vairākas maksājamā PVN konta, dimensijas un PVN koda kombinācijas, katrai kombinācijai tiek izveidota atsevišķa žurnāla rinda. Norakstīšanas transakcija tiek izveidota transakcijas valūtā. Plašāku informāciju skatiet šeit: Debitora norakstīšanas žurnāla izveide

## <a name="process-nsf-payments"></a>NSF maksājumu apstrāde

Varat apstrādāt NSF maksājumus, lapā **Iekasēšana** atlasot **NSF maksājums**. Atlasot šo pogu, maksājums tiek atcelts. Ja debitoram ir jāmaksā NSF maksa, maksājumu žurnālā tiek izveidota maksas transakcija. Maksas summa balstās uz automātisko maksu iestatījumiem. Automātiskās maksas, kas attiecas uz NSF maksājumiem, ir atkarīgas no maksu grupas, kas ietekmētajam bankas kontam ir atlasīta lapā **Bankas konti**.

## <a name="additional-resources"></a>Papildu resursi

[Debitora kredīta pārvaldības parametru iestatīšana](./cm-credit-mgmt-setup.md)

[Debitora kredīta pārvaldības informācijas iestatīšana](./cm-setup-information.md)

[Kredīta pārvaldības informācijas pievienošana debitoram](./cm-add-credit-mgmt-information-customer.md)

[Debitoru kredītu grupas](./cm-customer-credit-groups.md)

[Debitora kredīta limita korekcijas](./cm-credit-limit-adjustments.md)

[Kredīta aizturēšana pārdošanas pasūtījumiem](./cm-sales-order-credit-holds.md)

[Debitoru kredīta pārvaldības periodiskie uzdevumi](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
