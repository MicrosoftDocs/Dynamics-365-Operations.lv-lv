---
title: Pirkšanas līgumi
description: Šajā rakstā ir sniegta informācija par pirkšanas līgumiem. Pirkšanas līgums ir līgums, kas nosaka, ka organizācijai ir jānopērk noteikts daudzums vai jāiztērē noteikta summa, laika gaitā izmantojot vairākus pirkšanas pasūtījumus. Apmaiņā pret šīm saistībām pircējs saņem īpašas cenas un atlaides.
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 188a71ec660787b0b942a3d3bf4967b747c4469f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335891"
---
# <a name="purchase-agreements"></a>Pirkšanas līgumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par pirkšanas līgumiem. Pirkšanas līgums ir līgums, kas nosaka, ka organizācijai ir jānopērk noteikts daudzums vai jāiztērē noteikta summa, laika gaitā izmantojot vairākus pirkšanas pasūtījumus. Apmaiņā pret šīm saistībām pircējs saņem īpašas cenas un atlaides. 

Pirkšanas līgumi var attiekties uz noteiktu preces daudzumu, noteiktu preces summu valūtā vai noteiktu preču summu valūtā kādā sagādes kategorijā. Pārdošanas līguma cenām un atlaidēm ir prioritāte pār cenām un atlaidēm, kas ir norādītas jebkuros jau pastāvošajos tirdzniecības līgumos.  

Lapā **Pirkšanas līgumi** varat izveidot pirkšanas līgumus, pieteikties šiem līgumiem un sekot līdzi pirkšanas līgumiem, kas jau ir noslēgti starp jūsu organizāciju un kreditoriem. Kad esat izveidojis pirkšanas līgumu, varat, piemēram, pasūtīt tieši no tā. Katram pirkšanas līgumam ir derīguma termiņš, ko nosaka persona, kas izveido pirkšanas līgumu. Pirkuma piegādes datumam ir jābūt šī derīguma perioda ietvaros.  

Kad esat izveidojis pirkšanas līgumu, lai tas stātos spēkā, šis līgums ir jāaktivizē. Lai aktivizētu pirkšanas līgumu, opcijai **Atzīmēt līgumu kā spēkā esošu** iestatiet vērtību **Jā**. 

Lai nepieļautu pirkšanas līguma izmantošanu un apstiprināšanu, līguma statusu atzīmējiet kā **Slēgts**. Joprojām varēsiet atjaunināt statusu uz **Spēkā esošs** jebkurā laikā pēc tam, kad šīs izmaiņas veiktas.

## <a name="responsible-workers-on-purchase-agreements"></a>Par pirkšanas līgumiem atbildīgie nodarbinātie

Pirkšanas līguma klasifikācijā varat noteikt primāro atbildīgo nodarbināto un sekundāro atbildīgo nodarbināto. Šīs vērtības pārmantos ar iegūtais pirkšanas līgums. Pirkšanas līgumam nav obligāti jāpievieno atbildīgie nodarbinātie, un pašā pirkšanas līgumā tos var modificēt tieši katram gadījumam atsevišķi. Sekundāro atbildīgo nodarbināto nevar norādīt bez primārā atbildīgā nodarbinātā, taču nav obligāti jābūt sekundārajam atbildīgajam nodarbinātajam. Jūs nevarat norādīt to pašu nodarbināto kā primāro un sekundāro atbildīgo nodarbināto.

> [!IMPORTANT]
> Lai izmantotu atbildīgās puses funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.25, funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.29, tad administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot par pirkšanas līgumu *atbildīgās*[puses līdzekli Līdzekļu pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="commitment-types"></a>Saistību veidi
Katra pirkšanas līguma rinda ir saistības kaut ko nopirkt. Lai izpildītu saistības, varat izmantot rindas no vairākiem pirkšanas pasūtījumiem (PO). Ir četri saistību veidi.

-   **Uz preču daudzumu attiecināmas saistības** — jūs pērkat konkrētu preces daudzumu.
-   **Uz preču vērtību attiecināmas saistības** — jūs pērkat preci par konkrētu valūtas summu.
-   **Uz preces kategorijas vērtību attiecināmās saistības** — jūs pērkat konkrētu valūtas summu kādā sagādes kategorijā. Summa var būt vai nebūt iekļauta katalogā.
-   **Uz vērtību attiecināmās saistības** — jūs pērkat jebkuru preci vai preces par konkrētu valūtas summu jebkurā sagādes kategorijā.

## <a name="pricing-terms-for-purchase-agreements"></a>Cenu noteikšanas nosacījumi pirkšanas līgumiem
Cenu noteikšanas nosacījumi var atšķirties atkarībā no saistību veida. Pirkšanas līgumu ceno noteikšanas nosacījumiem ir prioritāte attiecībā pret jebkuriem citiem cenu noteikšanas nosacījumiem, kas ir noteikti tirdzniecības līgumiem. Šajā tabulā ir aprakstīti ar cenu saistītie lauki, kurus ietekmē katrs saistību veids. Laukus, kuros ir iekļauts vārds **Jā**, var atjaunināt pasūtījuma rindā.

| Saistību veids                   | Vienības cena | Cenas vienība | Atlaides procents | Termiņatlaides summa |
|-----------------------------------|------------|------------|------------------|----------------------|
| Uz preču daudzumu attiecināmas saistības       | Jā        | Jā        | Jā              | Jā                  |
| Uz preču vērtību attiecināmas saistības          |            |            | Jā              |                      |
| Uz preces kategorijas vērtību attiecināmās saistības |            |            | Jā              |                      |
| Uz vērtību attiecināmās saistības                  |            |            | Jā              |                      |

## <a name="policies-for-purchase-agreements"></a>Pirkšanas līgumu ierobežojumi
Šādi ierobežojumi ietekmē veidu, kā darbojas saistība starp pirkšanas līguma saistībām un atbilstošajām pirkšanas pasūtījuma rindām.

-   **Sasniegts maksimums** — kopējais daudzums vai summa visās pasūtījuma rindās nevar pārsniegt to daudzumu vai summu, kas ir norādīti piesaistītajās saistībās.
-   **Cena un atlaide ir fiksēta** — cenai pasūtījuma rindā ir jābūt vienādai ar cenu piesaistītajās saistībās. Ja pasūtījuma rindā tiek mainīta cena, saikne ar saistībām tiek bojāta. Ja saikne ir bojāta, pasūtījuma rinda netiek izmantota saistību pildīšanai.
-   **Minimālā izlaišanas summa un Maksimālā izlaišanas summa** — ja ir norādīta summa, jūs saņemat ziņojumu gadījumā, ja kādā pasūtījuma rindā veicat jebkādas izmaiņas, kuru dēļ pasūtījuma rinda atšķiras no piesaistītajām saistībām.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Pirkšanas līgumu izpildes aprēķini
Izpildes daudzumi un summas tiek rādīti cilnē **Izpilde**, kopsavilkuma cilnē **Detalizēta informācija par rindu**, kas atrodas lapā **Pirkšanas līgumi**.  

Apgabalā **Izpilde** tiek rādīta atlikusī summa vai daudzums, kas ir nepieciešams, lai izpildītu saistības.  

Apgabalā **Līgums** tiek rādīts kopējais daudzums vai kopējā summa, kādai šī pārdošanas līguma rinda ir derīga.  

Pirkšanas pasūtījuma rindām un rēķina rindām, kas tiek izmantotas izpildes aprēķināšanai, varat piekļūt, attiecīgajās rindās vai pirkšanas līguma virsrakstā atlasot darbību **Saistītā informācija**.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Pirkšanas līgumu apstiprinājumi un versiju vēsture
Apstiprinot pirkšanas līgumu, tā pašreizējā versija tiek saglabāta vēstures tabulā un tai tiek piešķirts versijas numurs. Ja maināt pirkšanas līgumu, jūs varat apstiprināt to vēlreiz, lai vēsturē saglabātu citu pirkšanas līguma versiju. Ja neapstiprināt pirkšanas līgumu, joprojām varat to izmantot, lai izmantotu pirkšanas pasūtījumus. Tomēr pirkšanas līguma vēstures informācija netiek saglabāta. Varat priekšskatīt vai drukāt visas līguma versijas. Pēc tam pārskatījumus varat koplietot ar kreditoru, lai saņemtu apstiprinājumu.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Pirkšanas līgumu lietošana pasūtīšanas procesā
Kad veidojat pirkšanas pasūtījumu, varat tam lietot pirkšanas līgumu. Pēc tam informācija no līguma nosacījumiem, piemēram, maksājumu nosacījumi, piegādes nosacījumi un piegādes adrese, tiek kopēta uz pirkšanas pasūtījuma galveni. Ja pirkšanas pasūtījumā ir viena vai vairākas rindas precēm vai kategorijām, uz ko attiecas šis līgums, šajās rindās tiek izmantotas cenas un atlaides no pirkšanas līguma. Summa vai daudzums pasūtījuma rindā tiek izmantots saistību pildīšanai pirkšanas līgumā. Vienā pirkšanas pasūtījumā var iekļaut gan rindas, kas nav saistītas ar pirkšanas līgumu, gan rindas, kas ir saistītas ar pirkšanas līgumu.  

Pirkšanas līgumu varat atlasīt tikai tad, kad veidojat pirkšanas pasūtījumu. Pirkšanas līgumu nevar atlasīt pēc tam, kad pirkšanas pasūtījums jau ir izveidots.  
Noteiktos risinājumos, kur pirkšanas pasūtījumi tiek veidoti netieši, varat kontrolēt, vai Supply Chain Management automātiski meklē piemērojamos pirkšanas līgumus. Piemēram, varat to darīt, ja automātiski apstiprināt plānotos pirkšanas pasūtījumus vai veidojat pirkšanas pasūtījumus, kuru pamatā ir pārdošanas pasūtījumi.

## <a name="matching-policy-on-purchase-agreements"></a>Pirkšanas līgumu atbilstības ierobežojumi
Pirkšanas līguma virsrakstā var definēt rindas atbilstības ierobežojumus. Šie rindu atbilstības ierobežojumi ievēros kreditoru parametru rindas atbilstības ierobežojumi, kad lauks **Atļaut atbilstības ierobežoju ignorēšanu** lapā **Kreditoru parametri** (kopsavilkuma cilnē **Cenas un daudzuma salīdzināšana** ) ir iestatīts **Augstāk par uzņēmuma politiku**. Dokumentos, kas atsaucas uz pirkšanas līgumu, tiks izmantoti rindas atbilstības ierobežojumi, kas definēti pirkšanas līguma virsrakstā, ja vien atbilstošajā krājumā, krājumos un kreditora vai kategoriju pirkšanas politikā nav norādīts citādi.

## <a name="purchase-agreements-and-intercompany-trade"></a>Pirkšanas līgumi un starpuzņēmumu tirdzniecība
Starpuzņēmumu darījumu attiecības var izveidot starp kreditoru kontiem un debitoru kontiem, kas pieder dažādām juridiskajām personām. Kad veidojat pārdošanas pasūtījumu vai pirkšanas pasūtījumu vienai no pusēm, tiek izveidota starpuzņēmumu pasūtījumu ķēde. Pasūtījumu ķēdē pārdošanas pasūtījums un pirkšanas pasūtījums tiek izveidots atbilstošajās juridiskajās personās.  

Varat izveidot pirkšanas līgumu vai pārdošanas līgumu vienai no starpuzņēmumu darījumos iesaistītajām pusēm. Otrai starpuzņēmumu darījumos iesaistītajai pusei varat izveidot atbilstošo pārdošanas līgumu vai pirkšanas līgumu otrā juridiskajā personā.  

Ja izveidojat starpuzņēmumu pirkšanas pasūtījumu, kas izmanto starpuzņēmumu pirkšanas līgumu vienā juridiskajā personā, tad atbilstošais starpuzņēmumu pārdošanas pasūtījums otrajā juridiskajā personā izmanto atbilstošo starpuzņēmumu pārdošanas līgumu. Pārdošanas līguma saistību izpilde tiek sinhronizēta ar pirkšanas līgumu izpildi, tāpat kā starpuzņēmumu pārdošanas pasūtījums tiek sinhronizēts ar starpuzņēmumu pirkšanas pasūtījumu.

## <a name="financial-dimensions-on-purchase-agreements"></a>Pirkšanas līgumu finanšu dimensijas
Finanšu dimensijas varat kopēt pirkšanas līguma dokumentu galvenēs vai atsevišķās rindās. Ja maināt dimensijas līguma virsrakstā vai līguma rindā, šīs izmaiņas neietekmē nekādus izlaistos pasūtījumus, bet tas atspoguļosies visos jaunajos pasūtījumos.

## <a name="additional-resources"></a>Papildu resursi

- [Pirkšanas līguma izveide](tasks/create-purchase-agreement.md)
- [Pirkšanas līguma lietošana, veidojot pirkšanas pasūtījumu](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]