---
title: Atmaksas apstrāde zvanu centros
description: Šajā tēmā skaidrots, kā atmaksas tiek ģenerētas, izmantojot zvanu centrus, kad tiek izveidotas atgriešanas, vai kad pasūtījumi vai pasūtījuma rindas tiek atceltas.
author: hhainesms
manager: annbe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd49835a24dc6ec429ac4b01f363f1be937628ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214732"
---
# <a name="refund-payment-processing-in-call-centers"></a>Atmaksas apstrāde zvanu centros

Šajā tēmā skaidrots, kā atmaksas tiek ģenerētas, izmantojot zvanu centrus, kad tiek izveidotas atgriešanas, vai kad pasūtījumi vai pasūtījuma rindas tiek atceltas.

Lietotājs, kurš izveidot atmaksas pasūtījumu klientam kā zvanu centra lietotājs Microsoft Dynamics 365 Commerce galvenajā birojā, izmanto lapu **Atmaksas pasūtījums**, lai izveidotu sākotnējo materiālu atgriezes autorizāciju (RMA). AKA definē preces, ko klients vēlas atgriezt vai apmainīt, un tas izveido saistītu atgriešanas pārdošanas pasūtījumu, kam ir **Atgrieztā pasūtījuma** tips. Šis saistītais atgrieztais pasūtījums tiek izmantots, lai izsekotu atgriezto krājumu un visu iegrāmatoto kredīta notu vai maksājumu atmaksu grāmatošanu.

Ja opcijas **Iespējot pasūtījuma pabeigšanu** iestatījums ir **Jā** zvanu centra kanālam, zvanu centra lietotājam, kas izveido AKA, ir jāpalaiž pasūtījuma pabeigšanas apstrādes plūsma, **Atgriešanas pasūtījuma** lapā atlasot **Pabeigts**. Funkcija **Pabeigts** nodrošina aprēķinātu atgriešanas darbību kopsavilkumu, kas ieskicē paredzēto atmaksas summu. Turklāt, kad tas ir pareizi konfigurēts, tas sistemātiski izveido atmaksas maksājuma rindu pret atgriezto pasūtījumu.

Zvanu centra loģika nosaka maksājuma metodi atmaksas maksājuma rindai, pamatojoties uz maksājuma metodi, kas tika izmantota oriģinālajam pasūtījumam. Ja izveidotais atgriešanas pasūtījums nav saistīts ar sākotnējo pasūtījumu, tiek lietota noklusējuma maksāšanas metode, kas tiek ņemta no sistēmas parametra.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Kā zvanu centrs nosaka, kuru maksājuma metodi piemērot atgriešanas pasūtījumam

Zvanu centrs izmanto oriģinālā pasūtījuma maksājuma metodi, lai noteiktu maksājuma metodi, kas jālieto atgriešanas pasūtījumam. Šeit aprakstīts, kā šis process darbojas šādām oriģinālajām maksāšanas metodēm:

- **Parasts** (skaidras naudas) vai **Čeks** - Kad izveidotais atgriešanas pasūtījums atsaucas uz sākotnējo pasūtījumu, par kuru tika samaksāts, izmantojot parasto (skaidras naudas) vai čeka maksājuma veidu, zvanu centra lietojumprogramma atsaucas uz konfigurācijām **Zvanu centra atmaksas metožu** lapā. Šī lapa iespējo organizācijas pēc pasūtījuma valūtas definēt, kā atmaksas tiek izsniegtas klientiem par pasūtījumiem, kas sākotnēji tika apmaksāti, izmantojot parasto vai čeku maksājuma tipu. **Zvanu centra atmaksas metožu** lapa arī ļauj organizācijām atlasīt, vai klientam tiek nosūtīts sistēmas ģenerēts atmaksas čeks vai arī klienta konta kredīts ir izveidots attiecībā pret iekšējo klienta konta bilanci. Šajos scenārijos zvanu centra loģikai ir atsauce uz atgriešanas pasūtījuma valūtu, un pēc tam izmanto **Mazumtirdzniecības maksājuma metodes** vērtību noteiktai valūtai, lai izveidotu atmaksas maksājuma rindu atgriešanas pasūtījumam. Vēlāk klienta parādu (AR) maksājumu žurnāls, kas izmanto kartēto AR maksājumu metodi, ir saistīts ar valūtu.

    Šajā attēlā redzama scenārija konfigurācija, kurā klients atgriež preces no pārdošanas pasūtījuma, kas ir saistīts ar USD valūtu un kas sākotnēji tika apmaksāts, izmantojot parasto vai čeka maksājuma tipu. Šajā scenārijā klientam tiks izsniegta atmaksa, izmantojot sistēmas ģenerētu atmaksas čeku. **REF-CHK** AR maksājuma metode ir konfigurēta kā atmaksas čeka maksājuma tips.

    ![Zvanu centra atmaksas metožu konfigurācija parastajiem un čeka sākotnējiem maksājumiem](media/callcenterrefundmethods.png)

- **Kredītkarte** - kad izveidotais atgriešanas pasūtījums atsaucas uz sākotnējo pasūtījumu, kas tika apmaksāts, izmantojot kredītkarti, zvanu centra loģika atmaksas maksājumiem piemēro to pašu sākotnējo kredītkarti atgriešanas pasūtījumam.
- **Lojalitātes karte** - kad izveidotais atgriešanas pasūtījums atsaucas uz sākotnējo pasūtījumu, kas tika apmaksāts, izmantojot klienta lojalitātes karti, zvanu centra loģika atmaksas maksājumiem piemēro atmaksu tai pašai lojalitātes kartei.
- **Dāvanu karte** (iekšēja) – kad izveidotais atgriešanas pasūtījums atsaucas uz oriģinālo pasūtījumu, kas tika apmaksāts, izmantojot izsniegtu dāvanu karti no Dynamics 365 Commerce (iekšējā dāvanu kartes funkcionalitāte), zvanu centra loģika atmaksas maksājumiem piemēro atmaksas summu uz to pašu sākotnējo dāvanu kartes numuru.
- **Dāvanu karte** (ārējs) – Kad izveidotais atgriešanas pasūtījums atsaucas uz oriģinālo pasūtījumu, kas tika apmaksāts, izmantojot ārēju trešās puses dāvanu karti, zvanu centra loģika atmaksas maksājumiem piemēro noklusējuma atgriešanas maksājuma metodi, kas ir noteikta **Zvanu centra parametru** lapas cilnē **AKA/Atgriešana**.

Ja sākotnējā pasūtījuma maksājuma tips nav zināms kāda iemesla dēļ vai arī sākotnējā pasūtījuma apmaksai tika izmantotas vairākas maksājuma metodes, zvanu centra loģika piemēro noklusējuma atgriešanas maksājuma metodi, kas ir noteikta **Zvanu centra parametru** lapas cilnē **AKA/Atgriešana**.

Šajā ilustrācijā parādīts **Maksājuma metodes** lauks **AKA/Atgriešanas** cilnē **Zvanu centra parametru** lapā.

![Maksājuma metodes lauks AKA/Atgriešanas cilnē Zvanu centra parametru lapā](media/callcenterrefundparameters.png)

> [!NOTE]
> Iepriekš aprakstītie atmaksas apstrādes noteikumi attiecas arī uz pasūtījumiem vai pasūtījumu rindām, kuras zvanu centra lietotājs atceļ programmā Commerce Headquarters. Ja pasūtījuma vai specifisku pasūtījuma rindu atcelšana rada pārmaksas, tiek izmantoti tie paši noteikumi, lai ģenerētu atmaksas maksājuma rindas.

Parasti atgriešanas pasūtījums iziet caur standarta procesu, kur tiek saņemts krājums (vai norakstīts), pavadzīme tiek grāmatota attiecībā pret atgriešanas pasūtījumu, un tad atgriešanas pasūtījumam tiek palaists rēķina grāmatošanas process. Atgriešanas pasūtījums ir saistīts un sistemātiski ģenerēts kā daļa no atgriešanas pasūtījuma izveides procesa. Parastos scenārijos maksājumu atmaksas netiek izsniegtas klientiem līdz brīdim, kad tiek grāmatots rēķins par pārdoto preču atgriešanas pasūtījumu.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Kas notiek, kad rēķins tiek grāmatots atgriešanas pasūtījumā

Sekojošais scenārijs skaidro, kas notiek, kad rēķins tiek grāmatots atgriešanas pasūtījumā:

- Ja atmaksa atgriešanas pasūtījumā ir paredzēta kredītkartei, tiek izsaukta papildu loģika, kad tiek grāmatots rēķins. Šī loģika izsauc maksājuma apstrādātāju, lai atmaksātu maksājumu klienta kredītkartē. Arī klienta maksājuma atmaksas dokuments tiek izveidots un sistemātiski iegrāmatots attiecībā pret klienta kontu. Šis maksājumu žurnāls tiks nosegts pret atgriešanas pasūtījuma kredīta notas dokumentu.
- Ja izdodamā atmaksa ir paredzēta čeku maksājuma tipam, tiek izveidots klienta maksājuma dokuments, kas izmanto AR maksājuma metodi, un tas ir manuāli jāgrāmato vai jādrukā pirms maksājuma dokumenta grāmatošanas klienta kontā. Lai apstrādātu atmaksas čeku, lietotāji var izmantot **Klienta maksājumu žurnāla** lapu sadaļā Klientu parādi vai specializēto **Atmaksas čeku apstrādes** lapu sadaļās Mazumtirdzniecība un Komercija.
- Ja atmaksa, kas ir jāizsniedz, ir paredzēta iekšējai dāvanu kartei vai lojalitātes programmas kartes maksājuma veidam, kad tiek izrakstīts rēķins par atgriešanas pasūtījumu, atmaksas maksājuma dokuments tiek izveidots un grāmatots attiecībā pret klienta kontu. Šis rēķina izrakstīšanas solis arī pievieno atmaksas summu atpakaļ klienta iekšēji izsekotās dāvanu kartes bilancei vai lojalitātes programmas punktu bilancei.
- Ja maksāšanas metode, kas izmanto **Klienta** funkciju (piemēram, klienta kontu), ir saistīta ar atgriešanas pasūtījumu, kredīta limita validācijas tiek ignorētas, kad maksājums tiek apstrādāts. Šajā kontekstā netiek izveidots vai grāmatots neviens maksājuma dokuments. Kad klienta maksājuma tips tiek izmantots atgriešanas pasūtījumā, kredīta notas dokuments, ko rēķinu grāmatošanas process izveido, darbojas kā klienta kredīta dokuments un norāda atmaksu klienta AR bilancē.

## <a name="advance-credit"></a>Avansa kredīts

Kad lietotājs apstrādā atgriešanas pasūtījumus kā zvanu centra lietotājs zvanu centrā, kur **Iespējot pasūtījuma pabeigšanas** funkcija ir iestatīta uz **Jā**, izņēmums iepriekš aprakstītajam atmaksas maksājumu grāmatošanas procesam var notikt, ja zvanu centra lietotājs, kurš veido atgriešanas pasūtījumu, iestata **Avansa kredīta** opciju uz **Jā** **Zvanu centra parametru** lapas cilnē **AKA/Atgriešana**. Šajā gadījumā maksājuma atmaksa notiek nekavējoties pēc tam, kad atgriešanas pasūtījums ir veiksmīgi iesniegts, izmantojot funkciju **Iesniegt** lapā **Atgriešanas kopsavilkums**. Sistēma nekavējoties izveido priekšapmaksas klienta maksājuma dokumentu atgriešanas vērtībai, pat ja pats atgriešanas pasūtījums vēl nav iekļauts rēķinā. Šo pieeju var izmantot gadījumos, kad organizācijai klientu apkalpošanas problēmu dēļ ir iepriekš jāizdod atmaksa, un tā nevēlas, lai pirms atmaksu izsniegšanas tiktu saņemti atgrieztie krājumi.

## <a name="replacement-orders"></a>Aizstāšanas pasūtījumi

Kad atgriešanas pasūtījums ir izsniegts **Aizstāšanas pasūtījuma** funkciju var izmantot, lai klientam ģenerētu jaunu pārdošanas pasūtījumu. Šo pieeju var izmantot apmaiņas scenārijos. **Aizstāšanas pasūtījuma** funkcija izveido citu pārdošanas pasūtījumu jaunajiem krājumiem, kas jānosūta, bet krusteniskā atsauce saite uz **AKA/Atgriešanas** cilni **Zvanu centra parametru** lapā saista aizvietošanas pasūtījumu, AKA un atgriezto pasūtījumu.

Apstrādājot maksājumus ar aizstāšanas pasūtījumu, organizācijām ir divas opcijas:

- Atmaksāt klientam atgriešanas pasūtījumu, balstoties uz sākotnējo maksājuma metodi, un tad iekasēt atsevišķu maksājumu par aizvietošanas pasūtījumu. Lai izmantotu šo opciju, nav nepieciešama papildu konfigurācija.
- Iestatiet opciju **Lietot kredītu** uz **Jā** cilnē **AKA/Atgriešana** lapā **Zvanu centra parametri**. Šajā gadījumā klienta maksājuma metode tiek sistemātiski pielietota gan atgriešanas pasūtījumam, gan aizvietošanas pasūtījumam. Šī opcija var palīdzēt novērst jebkura ārējā atmaksas maksājuma izsniegšanu. Tas arī palīdz novērst jebkādu darbības maksājumu apstrādi. Tas var būt noderīgi gadījumos, kad tiek apstrādāta vienmērīga apmaiņa un organizācija dod priekšroku kredīta dokumenta izmantošanai, kas tiek ģenerēta, kad atgriešanas pasūtījumam ir izrakstīts rēķins par rēķinu, kas izveidots ar aizvietošanas pasūtījumu. Ja opcija **Lietot kredītu** ir iestatīta uz **Jā**, organizācijai pēc abu finanšu dokumentu ģenerēšanas manuāli jānosedz kredīta nota attiecībā pret aizstāšanas pasūtījuma rēķinu.

Iestatījums **Jā** opcijai **Lietot kredītu** ir piemērojams tikai tad, kad atgriešanas pasūtījums tiks saistīts ar aizstāšanas pasūtījumu. Šajā gadījumā klienta maksājuma metode, kas tiks izmantota, lai sistemātiski maksātu par atgriešanu un maiņas pasūtījumu, ir definēta laukā **Lietot kredītu maksājumu metodi**, kas atrodas lapā **Zvanu centra parametri** cilnē **AKA/Atgriešana**. Šajā laukā var atlasīt tikai **Klienta** funkcijas maksājuma tipu.

> [!NOTE]
> Atgriešanas pasūtījumam, kuram nav saistīta aizstāšanas pasūtījuma, iestatījums **Jā** opcijai **Lietot kredītu** neietekmē atgriešanas pasūtījuma maksājuma loģiku, jo šis iestatījums attiecas tikai uz aizvietošanas pasūtījumiem.

![Lauks Lietot kredītu maksājuma metodi AKA/Atgriešanas cilnē Zvanu centra parametru lapā](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Ja lietotāji, kas izveido aizstāšanas pasūtījumu plānu, lai izmantotu opciju **Lietot kredītu**, tiem nav jāpalaiž funkcija **Pabeigts** atgriešanas pasūtījumā, pirms viņi iestata opciju **Lietot kredītu** uz **Jā**. Kad funkcija **Pabeigts** ir palaista, atmaksas maksājums tiek aprēķināts un pielietots atgriešanas pasūtījumam. Jebkurš mēģinājums iestatīt opciju **Lietot kredītu** uz **Jā**, ja atmaksas maksājums jau ir aprēķināts un piemērots, neaktivizēs atmaksas maksājuma pārrēķinu, un laukā **Lietot kredītu maksājumu metodi** atlasītā maksāšanas metode netiks pielietota. Ja šajā kontekstā ir jāizmanto opcija **Lietot kredītu**, lietotājam ir jāizdzēš aizvietošanas pasūtījums un AKA, un pēc tam jāsāk no jauna un jāizveido jauna AKA. Šoreiz lietotājam ir jānodrošina, lai pirms funkcijas **Pabeigts** palaišanas opcija **Lietot kredītu** būtu iestatīta uz **Jā**.

## <a name="payment-overrides-for-call-center-returns"></a>Maksājumu ignorēšana zvanu centra atgriešanas gadījumos

Lai gan zvanu centra loģika sistemātiski nosaka atmaksas metodi iepriekš aprakstītajā veidā, dažreiz lietotāji var vēlēties ignorēt šos maksājumus. Piemēram, lietotājs var rediģēt vai noņemt esošās atmaksas rindas un pielietot jaunas maksājumu rindas. Sistēmas aprēķinātos atmaksas maksājumus var mainīt tikai lietotāji, kuriem ir pareizās labošanas atļaujas. Šīs atļaujas var konfigurēt **Ignorēt atļaujas** Retail un Commerce lapās. Lai ignorētu atmaksas maksājumu, lietotājam ir jābūt saistītam ar drošības lomu, kur opcija **Atļaut alternatīvu maksājumu** ir iestatīta uz **Jā** lapā **Ignorēt atļaujas**.

![Atļaut alternatīvu maksāšanas opciju lapā Ignorēt atļaujas](media/overridepermissions.png)

Vai arī organizācija var iestatīt opciju **Atļaut maksājuma ignorēšanu** uz **Jā** lapā **Zvanu centra parametri** cilnē **AKA/Atgriešana**. Šajā gadījumā laukā **Drošības ignorēšanas kods** ir jāatlasa kods. Drošības ignorēšanas kods ir burtciparu kods, kas ir jāpārvalda ārēji, jo lietotāji to nevar skatīt programmā Commerce Headquarters pēc to iestatīšanas. Drošības ignorēšanas kodu jāzina tikai dažiem galvenajiem, uzticamākajiem cilvēkiem organizācijā. Ja opcija **Atļaut maksājuma ignorēšanu** ir iestatīta uz **Jā** un ja jebkuri lietotāji, kuriem nav pareizo lomu atļauju, mēģinās mainīt atgriešanas pasūtījuma maksājuma metodi, lietotājiem būs iespēja ievadīt drošības ignorēšanas kodu. Ja viņi to nezina vai arī vadītājs vai galvenais vadītājs nevar to ievadīt lapā, viņi nevarēs ignorēt atgriešanas maksājuma metodi.

> [!NOTE]
> Ja drošības ignorēšanas kods ir pazaudēts vai aizmirsts, organizācijai tas būs jāatiestata, definējot jaunu drošības ignorēšanas kodu laukā **Drošības ignorēšanas kods**, kas atrodas lapā **Zvanu centra parametri** cilnē **AKA/Atgriešana**.

![Maksājuma ignorēšanas parametri AKA/Atgriešanas cilnē Zvanu centra parametru lapā](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Pirms organizācijas mēģina ignorēt atmaksas maksājumus, kas izmanto kredītkaršu maksājumu veidus, tām ir jāpārbauda, vai to kredītkaršu procesors ļauj veikt nesavienotu atgriešanu. Daudziem procesoriem atmaksas ir jāgrāmato atpakaļ sākotnējā kartē. Jebkurš mēģinājums izsniegt atmaksu kartei, kam nav iepriekšējas tveršanas, var izraisīt procesora grāmatošanas kļūmes.

## <a name="additional-resources"></a>Papildu resursi

[Maksāšanas metodes zvanu centros](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]