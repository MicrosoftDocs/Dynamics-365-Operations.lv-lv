---
title: "PVN atgūšana, izmantojot izdevumu pārvaldību"
description: "Šajā tēmā ir paskaidrots, kā saņemt atmaksu par attaisnotām pievienotās vērtības nodokļa (PVN) transakcijām."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: lv-lv
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>PVN atgūšana, izmantojot izdevumu pārvaldību

Lai saņemtu atmaksu par attaisnotām pievienotās vērtības nodokļa (PVN) transakcijām, uzņēmumam vai organizācijai jānosaka, jāapkopo, jāpārbauda un jāiesniedz precīza informācija. Šis process ietver vairākus uzdevumus. Atkarībā no jūsu uzņēmuma lieluma tas var ietvert vairākus darbiniekus vai lomas.

Lai atgūtu PVN, izmantojot izdevumu pārvaldības procedūru, ir jāizpilda vairāki priekšnosacījumi.

- Valstīm/reģioniem, kas ir piešķirti izdevumu kategorijām, ir jāizveido nodokļu kodi.
- Katram nodokļa kodam ir jāizveido PVN grupa.
- Katrai PVN grupai ir jāizveido krājuma PVN kods.

Kad priekšnosacījumi ir izpildīti, darbiniekiem jāizpilda tālāk minētās darbības, lai pieprasītu atmaksu par PVN transakcijām.

1. Izdevumu pārskatā ievadiet nodokļa informāciju par kredītkartes transakcijām, lai identificētu piemērojamās PVN atmaksas.
2. Pārliecinieties, vai visa nodokļu informācija ir ievadīta, un pēc tam grāmatojiet izdevumu pārskatu.
3. Apstrādājiet izdevumus, kas ir piemēroti starptautiskai PVN atgūšanai.
4. Nosūtiet PVN atgūšanas datus trešās puses kreditoram, lai aizpildītu starptautiskās atgriešanas formas.
5. Apstrādājiet izdevumus iekšzemes PVN atgūšanai.

Turpmākajās sadaļās ir sniegti piemēri par to, kā Contoso darbiniekiem izpilda katru darbību.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Izdevumu pārskatā ievadiet nodokļa informāciju par kredītkartes transakcijām, lai identificētu piemērojamās PVN atmaksas

Contoso tirdzniecības pārstāve Nensija, kas atrodas ASV, nesen atgriezās no tirdzniecības komandējuma Apvienotajā Karalistē. Ceļojuma laikā viņai radās daži personiskie izdevumi par ēdināšanu, ko viņa samaksāja ar kredītkarti. Nensijai tagad jāizveido izdevumu pārskats, lai saskaņotu savus izdevumus.

Kad Nensija ievada informāciju savā izdevumu pārskatā, viņa lapas **Labot izdevumu pārskatu** laukā **Valsts/reģions** atlasa **Apvienotā Karaliste**. Pēc tam PVN grupu saraksts tiek filtrēts tā, lai tiktu parādītas tikai tās grupas, kas attiecas uz Apvienoto Karalisti. Nensija atlasa PVN grupu **Apvienotā Karaliste 001** un pēc tam krājumu PVN grupā atlasa **Maltītes**. Pēc tam viņa pievieno jaunu transakciju izdevumiem par naktsmītni. Naktsmītnēm Apvienotajā Karalistē ir pieejama tikai viena PVN grupa un krājumu PVN grupa, tādēļ šī informācija tiek automātiski aizpildīta Nensijas izdevumu pārskatā.

Saskaņā ar Contoso politiku visiem izdevumiem ir jāpievieno atbilstoša kvīts. Tādēļ, kad Nensija saglabā savu izdevumu pārskatu, viņa saņem ziņojumu, kurā norādīts, ka viņai jāpievieno kvīts katrai transakcijai, ko viņa uzskaitīja savā izdevumu pārskatā. Nensija apstiprina, ka viņa pievienoja izdevumu pārskatam digitālu katras transakcijas izdevumu kvīts attēlu, un pēc tam iesniedz Savu pārskatu apstiprināšanai. Viņa pēc tam nosūta papīra kvītis apstrādei grāmatvedības nodaļā. Šī komanda nosūtīs PVN atgūšanas datus trešās puses kreditoram, kas aizpildīs starptautiskās PVN atgūšanas veidlapu uzņēmumam Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Pārliecinieties, vai visa nodokļu informācija ir ievadīta, un pēc tam grāmatojiet izdevumu pārskatu

Contoso kreditoru koordinatorei Eiprilai jāievada no izdevumu pārskata visa trūkstošā informācija par nodokļiem, pirms pārskatu var grāmatot. Viņa atver lapu **Detalizēta informācija par izdevumu pārskatu** un redz Nensijas apstiprināto izdevumu pārskatu. Pēc tam Eiprila atver izdevumu pārskatu, lai skatītu detalizētu informāciju par transakcijām. Viņa redz, ka Nensija neievadīja krājumu PVN grupu kādai no transakcijām. Šī informācija nav sniegta, tādēļ Eiprila nevar grāmatot izdevumu pārskatu. Tāpēc Eiprila atver darbplūsmas Izdevumu pārvaldība lapu **Nodokļa konfigurācijas** un atrod krājuma PVN grupu, kas atbilst valstij/reģionam un transakcijas veidam. Eiprila tagad var grāmatot izdevumu pārskatu virsgrāmatā.

Kad Eiprila grāmato izdevumu pārskatu, tiek izveidots PVN atgūšanas darba vienums. Šis darba vienums tiek piešķirts grāmatvedības apstrādes darba grupas darbiniekam. Eiprila saņem ziņojumu, kas apstiprina, ka grāmatošana bija veiksmīga. Šajā ziņojumā parādīts to PVN transakciju skaits, kas tika noteiktas atgūšanai.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Izdevumu, kas ir piemēroti starptautiskai PVN atgūšanai, apstrāde

Contoso grāmatvedības darba grupas darbiniekam Ārnijam ir jāpārbauda, vai visa nepieciešamā informācija par PVN atgūšanu ir iekļauta izdevumu pārskatā. Viņš atver lapu **Izdevumu nodokļu atgūšana** un atlasa Nensijas iesniegto izdevumu pārskatu. Ārnijs pārbauda, vai nepieciešamās kvītis ir pievienotas un ir ievadīta pareizā PVN grupai un krājuma PVN kodi.

Kad Ārnijs saņem papīra kvītis no Nensijas, viņš pārbauda, vai papīra kvītīs sniegtie dati atbilst digitālo kvīšu datiem un pēc tam maina izdevumu pārskata statusu uz **Gatavs atgūšanai**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Nosūtiet PVN atgūšanas datus trešās puses kreditoram, lai aizpildītu starptautiskās atgriešanas formas

Kad Ārnijs ir gatavs nosūtīt izdevumu pārskata datus uz trešās puses kreditoram, kas aizpildīs PVN atgūšanas formu, viņš atver lapu **Izdevumu nodokļu atgūšana**. Viņš filtrē lapu, lai parādītu tikai tos izdevumu pārskatus, kas atzīmēti kā **Gatavs atgūšanai**. Pēc tam Ārnijs atlasa **Fails** &gt; **Eksportēt uz Excel**. PVN informācija no izdevumu pārskatiem tiek eksportēta uz Microsoft Excel darblapu. Ārnijs iesniedz šo darblapu trešās puses kreditoram un ietver ziņojumu, kurā norādīts, ka papīra kvītis tika nosūtītas ar kurjeru.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Apstrādājiet izdevumus iekšzemes PVN atgūšanai

Ārnijam jāpārbauda, vai izdevumu pārskata transakcijas ir piemērotas PVN atgūšanai un vai pārskatiem ir pievienotas digitālas kvītis. Lai sāktu attaisnoto izdevumu apstrādi iekšzemes atgūšanai,Ārnijs atver lapu **Izdevumu nodokļu atgūšana** un atlasa izdevumu pārskatu, kas pieprasa pārbaudi. Viņš pārbauda, vai kvītīs ir norādīts uzņēmuma nosaukums nevis darbinieka vārds. PVN atgūšanas nolūkā kvītis jābūt norādītam uzņēmuma nosaukumam. Pēc tam Ārnijs pārbauda, vai tika izmantota pareizā PVN grupa un krājuma PVN kodi.

Kad Ārnijs saņem papīra kvītis, viņš maina izdevumu pārskata statusu uz **Gatavs atgūšanai**. Pēc tam viņš var aizpildīt atgriešanas formu un iesniegt atbilstošajai nodokļu iestādei. Šajā gadījumā atbilstošā nodokļu iestāde ASV ir Internal Revenue Service (IRS).

