---
title: "Iestatīšana kreditoriem"
description: "Šajā tēmā ir aprakstīti informācijas tipi, kuri jānorāda, veidojot jaunu kreditora kontu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0719a49bee069dc49be084a3fbc4ba5eb4883d03
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-vendor-accounts"></a>Iestatīšana kreditoriem

Šajā tēmā ir aprakstīti informācijas tipi, kuri jānorāda, veidojot jaunu kreditora kontu.

Veidojot kreditora kontu, ir jāievada informācija par kreditoru. Šī informācija tiek lietota, lai automātiski ievadītu datus dokumentos un sekotu līdzi aktivitātēm, kas saistītas ar kreditoru. Piemēram, varat konfigurēt šādu informāciju par kreditoru:

-   Piešķiriet kreditoru grupu. Katrs kreditors ir jāpiešķir kreditoru grupai. Kreditoriem kreditoru grupā ir kopīgi parametri. Piemēram, tiem var būt tādi paši maksājuma nosacījumi.
-   Konfigurējiet piegādātāju kataloga importēšanai. Kreditori var sniegt failu, kurā ir to piedāvāto krājumu un pakalpojumu katalogs. Šo failu var augšupielādēt, lai jūsu darbinieki varētu veikt pasūtījumu no kreditora.
-   Piešķiriet kreditoru sagādes kategorijām.
-   Atļaujiet esošam piegādātājam veikt darījumus ar citu juridisko personu savā organizācijā.
-   Iestatiet kreditoram apstrādes aizturēšanu noteiktiem darbību tipiem.
-   Iestatiet kreditora bankas informāciju, lai varat sūtīt maksājumus elektroniski.
-   Iestatiet kreditoram informāciju par nodokļiem piegādi, rēķinu un maksājumu. Pēc noklusējuma šie iestatījumi tiek kopēti jaunizveidotos dokumentos, ko izveidojat šim kreditoram.
-   Iestatiet noklusējuma finanšu dimensijas, kas tiek izmantotas, lai automātiski grāmatotu transakcijas ar kreditoru finanšu kontiem.

Lai paātrinātu kreditoru kontu izveides procesu, var izveidot veidnes. Lai izveidotu veidni, uz **kreditoru** lapas, darbību rūtī noklikšķiniet uz **opcijas**&gt;**ierakstīt info**. Pēc tam noklikšķiniet uz **Uzņēmuma kontu veidne**. Uzņēmuma kontu veidnes tiek koplietotas ar citiem lietotājiem.  

Varat arī izveidot lietotāja veidni savām vajadzībām. Kreditoru, kas ir saistīts ar citiem ierakstiem, piemēram, kontaktpersonām vai precēm, nevar dzēst.

## <a name="vendor-account-numbers"></a>Kreditora kontu numuri
Konta numurs ir kreditora unikāls identifikators. Varat iestatīt kontu numurus tā, lai tie tiktu izveidoti automātiski, veidojot kreditoru. Varat ar konfigurēt numuru sēriju, lai kontu numuri tiktu ievadīti manuāli. Piemēram, varat izmantot kreditora tālruņa numuru kā identifikatoru.

## <a name="vendor-organizations-and-individual-vendors"></a>Kreditoru organizācijas un atsevišķi kreditori
Veidojot jaunu kreditora kontu, ir jāatlasa, vai kreditors ir organizācija vai persona. No atlasītās opcijas ir atkarīga informācija, kas ir jāaizpilda par kreditoru. Personas gadījumā šī informācija ietver vārdu, uzvārdu un amatu. Organizācijas gadījumā šī informācija ietver organizācijas numuru un darbinieku skaitu.

## <a name="addresses"></a>Adreses
Katram kreditoram var definēt vairākas adreses, katra no kurām tiek izmantota dažādiem mērķiem. Piemēram, var izveidot adresi, kuras mērķis ir **Rēķins**. Vai arī, ja kreditoram veiksit maksājumu ar čekiem, varat iestatīt adresi, kuras mērķis ir **Pārvedums**. Ja ir jānorāda adrese, kas tiks lietota naudas pārskaitījumiem uz ārvalstu bankām, mērķis būs **SWIFT**.

## <a name="vendor-contacts"></a>Piegādātāja kontaktpersonas
Varat saglabāt kreditora kontaktpersonas. Šīs kontaktpersonas var izmantot dokumentos, piemēram, pirkšanas pasūtījumos vai piedāvājumu pieprasījumos (PP).  

Pievienot kontaktpersonas kreditoram, **visiem kreditoriem** lapa par **kreditoru** cilni, jo **iestatīt** grupu, noklikšķiniet uz **kontaktus**&gt;**pievienot kontaktpersonas**.  

Varat izveidot jaunas kreditora kontaktpersonas. Vai arī varat kopēt informāciju no citas personas, kas jau ir reģistrēta programmā Microsoft Dynamics 365 for Operations, un rediģēt informāciju pēc nepieciešamības.  

**Piezīme.** Kreditora kontaktpersonas pievienošana nav tas pats, kas attiecīgā kreditora kontaktinformācijas pievienošana. Lai gan varat pievienot kreditora vispārīgo kontaktinformāciju, var būt arī vairāki konkrēti darbinieki, kuri ir attiecīgā uzņēmuma kontaktpersonas un kuriem ir atsevišķa kontaktinformācija.  

Kontaktpersonas ierakstu nevar dzēst, ja uz kontaktpersonu ir atsauce dokumentā. Tā vietā var deaktivizēt kontaktpersonu.  

Kreditora kontaktpersonas var pievienot Microsoft Office 365 saglabātos personiskos kontaktus. Tomēr vispirms ir jāuzstāda sinhronizāciju starp Dynamics 365 operācijām un biroja 365 gan Microsoft Exchange servera sinhronizāciju un Microsoft Outlook iestatīšanas vedni.

## <a name="vendors-in-different-legal-entities"></a>Kreditori dažādās juridiskajās personās
Ja kreditors ir reģistrēts tikai vienai juridiskajai personai jūsu organizācijā un citām juridiskajām personām ir jāreģistrē tas pats kreditors, varat izmantot lapu **Pievienot kreditoru citai juridiskai personai**, lai konfigurētu kreditoru darījumu veikšanai ar citu juridisko personu. Jāatlasa kreditoru grupa, valūta un aizturēšanas statuss kreditoram izvēlētajā juridiskajā personā.  

Ja daudzām juridiskajām personām jūsu organizācijā ir darījumi ar vienu un to pašu kreditoru un katra juridiskā persona uztur atsevišķu kreditora kontu šim kreditoram, var sapludinātu kreditora kontu puses ID. Šādā veidā var kopīgot tādu informāciju kā adrese un darbinieku skaits, lai tā būtu jāatjaunina tikai vienā vietā.  

Lai sapludinātu pušu ID, rīkojieties šādi.

1.  Lapā **Globālā adrešu grāmata** atlasiet adrešu grāmatas ierakstus, kas atspoguļo kreditoru katrā juridiskajā personā, kuru vēlaties iekļaut kartēšanā.
2.  Darbību rūtī noklikšķiniet uz **Sapludināt ierakstus**.

## <a name="agreements"></a>Līgumi
Iestatot kreditora kontu, jūs varat arī reģistrēt līgumus, kas ir noslēgti ar kreditoru. Varat iestatīt cenu un atlaižu līgumus, izmantojot darbības kreditora ierakstā. Varat arī iestatīt pirkšanas līgumu lapā **Pirkšanas līgumi**.

## <a name="putting-a-vendor-on-hold"></a>Apstrādes aizturēšanas noteikšana kreditoram
Varat aizturēt apstrādi kreditoram dažādiem darbību tipiem. Pieejamas šādas opcijas

-   **Nē** — kreditoram nav noteikts neviens aizturējums.
-   **Rēķins** — kreditoram nevar grāmatot nevienu rēķinu.
-   **Visi** — kreditoram ir aizturēti visi darījumu veidi. Šie darbību tipi ietver pirkšanas pieprasījumus, rēķinus un maksājumus.
-   **Maksājums** — šim kreditoram nevar ģenerēt maksājumus.
-   **Pieprasījums** — var tikt izveidoti tikai pirkšanas pieprasījumi. Nevar izveidot citas darbības.
-   **Nekad** — kreditoram nekad netiek aizturētas darbības.

Nosakot kreditoram aizturējumu, varat arī norādīt iemeslu un aizturēšanas statusa beigu datumu. Ja beigu datums netiek ievadīts, kreditora aizturēšanas statuss ilgst nenoteiktu laiku.

## <a name="vendor-invoice-account"></a>Kreditora rēķina saņēmējs
Ja tāda pati rēķina adrese ir vairāk nekā vienam kreditoram vai kreditoram ir izrakstīts rēķins ar trešās puses starpniecību, varat norādīt rēķina kontu kreditora ierakstam. Rēķina konts ir konts, kurā kreditēta rēķina summa, veidojot kreditora rēķinu no pirkšanas pasūtījuma. Neievadot rēķina kontu kreditora ierakstam, kreditora konts tiek izmantots kā rēķina konts.

## <a name="vendor-bank-accounts"></a>Kreditora bankas konti
Ja jāveic maksājumi uz kreditora bankas kontu, varat ievadīt informāciju par kreditora banku un bankas kontiem lapā **Kreditora banka**. Varat arī ievadīt informāciju par validāciju un maksājumiem bankas kontam. Piemēram, varat pievienot darījuma pārbaudes kreditora bankas kontos. Šīs darījuma pārbaudes var izmantot, lai pārbaudītu konta datu precizitāti, piemēram, maršruta numurus un kontu numurus. Jānorāda noklusējuma konts kreditora maksājumiem. Tomēr, veicot faktisko maksājumu, varat mainīt šo kontu uz kādu no citiem kreditora kontiem.

## <a name="ledger-accounts"></a>Virsgrāmatas konti
Varat norādīt noklusējuma kontus, kuri automātiski parādīsies attiecīgā kreditora rēķinu žurnālos. Šī funkcija var noderēt, ja parasti maksājat par viena veida precēm vai pakalpojumiem, ko nodrošina vieni un tie paši kreditori. Norādot noklusējuma kontu, var ātri un efektīvi ievadīt žurnāla ierakstus rēķinu žurnālā. Noklusējuma konti, ko norādāt, netiek izmantoti pirkšanas pasūtījumiem vai kreditoru rēķiniem, kas ir ievadīti lapā **Kreditora rēķins**.  

Noklusējuma konti tiek atlasīti cilnē **Noklusētie konta iestatījumi**, kuru var atvērt, izmantojot cilni **Rēķins** kreditora ierakstā. Šeit atlasītie konti tiek parādīti kreditora kontam filtrēto kontu sarakstā, kad tiek ievadīts žurnāla ieraksts. Vienu no kontiem var iestatīt kā noklusējuma kontu.


