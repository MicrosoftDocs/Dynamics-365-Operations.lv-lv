---
title: "Atskaišu koka definīcijas finanšu atskaitēs"
description: "Šajā rakstā ir sniegta informācija par atskaišu koku definīcijām. Atkaišu koka definīcija ir atskaites komponents jeb veidošanas bloks, kas palīdz definēt jūsu organizācijas struktūru un hierarhiju."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ec1286f1f3fb75cefd40f3982ec62d5ed078299c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="reporting-tree-definitions-in-financial-reports"></a>Atskaišu koka definīcijas finanšu atskaitēs

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par atskaišu koku definīcijām. Atkaišu koka definīcija ir atskaites komponents jeb veidošanas bloks, kas palīdz definēt jūsu organizācijas struktūru un hierarhiju.

Finanšu atskaišu veidošana atbalsta elastīgu atskaišu veidošanu, tāpēc varat ērti veikt izmaiņas, mainoties jūsu biznesa struktūrai. Atskaites ir veidotas no dažādiem komponentiem jeb veidošanas blokiem. Viens no šiem veidošanas blokiem ir atskaišu koka definīcija. Atskaišu koka definīcija palīdz definēt jūsu organizācijas struktūru un hierarhiju. Tā ir starpdimensiju hierarhiska struktūra, kas ir balstīta uz dimensiju attiecībām jūsu finanšu datos. Tā sniedz informāciju atskaites vienības līmenī un kopsavilkuma līmenī visām kokā esošajām vienībām. Atkaišu koka definīcijas var kombinēt ar kolonnu definīcijām un atskaišu definīcijām, lai izveidotu veidošanas bloku grupu, ko var izmantot vairāki uzņēmumi. Atskaites vienība tiek izmantota katrā organizācijas diagrammas rūtiņā. Pārskatu vienība var būt atsevišķa finanšu datu grupa vai augstāka līmeņa kopsavilkuma vienība, kurā ir ietverta informācija no citām pārskatu vienībām. Pārskata definīcijām, kas satur pārskata koku, tiek ģenerēts viens pārskats katrai pārskata vienībai un kopsavilkuma līmenim. Visas šīs atskaites izmanto rindu un kolonnu definīcijas, kas ir norādītas atskaites definīcijā, ja vien atskaites definīcija nenorāda, ka ir jāizmanto atskaišu koks no rindas definīcijas. Rindu un kolonnu definīcijas ir svarīgas sastāvdaļas finanšu pārskatu dizainā un funkcionalitātē. Pārskata koki paaugstina komponentu pilnvaras, un atbalsta elastīgu pārskatu veidošanu, biznesa struktūrām mainoties. Finanšu atskaites, kas nav balstītas uz atskaišu koku, izmanto tikai dažas finanšu atskaišu veidošanas iespējas. Varat izmantot vairākas atskaišu koka definīcijas kopā ar vienādām rindu un kolonnu definīcijām, lai skatītu jūsu organizācijas datus dažādos veidos.

## <a name="reporting-tree-best-practices"></a>Pārskata koka pieņemtā prakse
Pirms atskaišu koka izveidošanas apsveriet tālāk aprakstītās pieņemtās prakses ievērošanu.

-   Vispirms ir jānosaka, kuras pārskata dimensijas ir nepieciešamas jūsu juridiskajai personai vai uzņēmumam.
-   Apsveriet, kā esat iestatījis savu struktūru, un pēc tam uzzīmējiet jūsu uzņēmuma organizācijas diagrammu. Uzzīmējot organizācijas struktūru, būs vieglāk izlemt to, vai pārskatu vienības jāgrupē vienā vai vairākos pārskatu kokos.
-   Sāciet ar zemāko pieejamo detalizācijas līmeni, piemēram, nodaļas un projekti, kas ir definēti finanšu datos. Detalizācijas līmenim pievienojiet tik daudz rūtiņu, cik nepieciešams, lai parādītu augstāka līmeņa nodaļas vai reģionus. Katra rūtiņa norāda atspoguļo potenciālu pārskata vienību pārskata kokā, ko jūs veidojat.
-   Jāņem vērā arī labākais veids, kā veidot jūsu kokus. Lai ģenerētu atskaišu koku, varat izmantot automatizētu veidošanas procesu, vai atskaišu koku varat izveidot manuāli. Pirms veidot savus kokus, ir svarīgi saprast abas metodes.
-   Var izmantot pārskata vienības, kas ir definētas jūsu finanšu datu sistēmā, lai pārskata koka definīcijai pievienotu pārskata vienības.

## <a name="create-multiple-reporting-trees"></a> Izveidot vairākus pārskata kokus
Var izveidot neierobežotu pārskata koku skaitu, lai skatītu jūsu uzņēmuma datus dažādos veidos. Katrs pārskata koka var saturēt jebkuru nodaļu un kopsavilkuma vienību kombināciju. Pārskata definīcija var vienlaicīgi saturēt saiti tikai uz vienu pārskata koku. Pārkārtojot pārskata vienību struktūru, jūs varat izveidot dažādus pārskata kokus. Pēc tam katram atskaišu kokam varat izmantot tās pašas rindu un kolonnu definīcijas. Šādā veidā varat ātri izveidot dažādus finanšu atskaišu izkārtojumus. Ja izveidojat vairākus atskaišu kokus, jūs katru mēnesi varat izdrukāt finanšu atskaišu sērijas, kas dažādos veidos analizē un uzrāda jūsu uzņēmuma operācijas. Papildinformāciju skatiet atskaites vienību struktūru piemēros šīs raksta nobeigumā.

## <a name="create-a-reporting-tree-definition"></a> Izveidot pārskata koka definīciju
Atskaišu koka definīcija satur kolonnas, kas ir aprakstītas nākamajā tabulā.


| Pārskata koka kolonna |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        Uzņēmums        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          Pārskata vienības uzņēmuma nosaukums. Vērtība <strong>@ANY</strong>, kas parasti tiek piešķirta tikai kopsavilkuma līmenim, sniedz iespēju pārskatu koku izmantot visiem uzņēmumiem. Visiem bērnelementu zariem ir piešķirts attiecīgs uzņēmums.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|       Vienības nosaukums       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   Kods, kas identificē šo pārskata vienību grafiskajā pārskatu kokā. Noteikti izveidojiet unikālu kodēšanas sistēmu, kas darbojas konsekventi un ko lietotājiem ir viegli saprast.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|   Vienības apraksts    |                                                                                                                                                                                                                                                                                                                                                                                                                                                        Pārskata vienības nosaukums tiek parādīts atskaites galvenē vai kājenē, ja ievadāt <strong>UnitDesc</strong> kā kodu, cilnē <strong>Galvenes un kājenes</strong> pārskata definīcijā. Nosaukums parādās pārskata rindas aprakstā, ja ievadāt <strong>UnitDesc</strong>, šūnā <strong>Apraksts</strong> rindas definīcijā.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|      Dimensijas       |                                                                                                                                                                                                                                                                                                                                                                      Pārskata vienība, kas informāciju saņem tieši no finanšu datiem. Tā definē loģisko pozicionēšanu, kā arī konta un saistīto segmentu garumus. Katrai atskaites vienības rindai šajā kolonnā ir nepieciešama dimensija. Varat arī ievietot dimensiju kopsavilkuma vienības rindā (piemēram, izdevumiem, kas ir tieši saistīti ar šo vienību). Ja ievadāt dimensiju kopsavilkuma vienības rindā, tad kontus, kas tiek izmantoti pamata vienībās, nevajadzētu izmantot apakšvienībās. Pretējā gadījumā summas varētu dublēties.                                                                                                                                                                                                                                                                                                                                                                      |
|    Rindu definīcijas    |                                                                                                                                                                                                                                                                                                                                                                                        Rindas definīcijas pārskata vienības nosaukums. Viena un tā pati rindas definīcija tiek izmantota katrā pārskatu koka vienībā. Veidojot pārskatu, šī rindas definīcija tiek izmantota katrā pārskatu vienībā. Rindas definīcijā var ietvert saites uz vairākām finanšu dimensijām. Ja pārskatu kokā ir noradīta rindas definīcija, pārskata definīcijas cilnē <strong>Pārskats</strong> atzīmējiet izvēles rūtiņu <strong>Izmantot pārskatu koka rindas definīciju</strong>.                                                                                                                                                                                                                                                                                                                                                                                        |
|       Rindas saite        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            Pārskatu vienībā izmantojamā rindas saite. Rindas definīcijā rindas saites tiek noteiktas, lai norādītu finanšu dimensijas, uz kurām ir jāizveido saite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|     Ārējā saite     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   Šajā pārskatu vienībā izmantojamā rindas saite. Rindas saites tiek definētas rindas definīcijai, lai identificētu atskaiti, uz kuru veidot saiti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|     Ārējais fails     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              Faila ceļš uz finanšu atskaišu veidošanas darblapu, no kuras iegūt datus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|     Lapas opcijas      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       Šī kolonna kontrolē, vai šīs atskaites vienības detalizētā informācija tiek apspiesta, kad atskaite tiek skatīta vai drukāta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|       Apkopojuma %        | Procentuālais daudzums no atskaites vienības, kas ir jāpiešķir pamatvienībai. Procenti, ko jūs ievadāt šajā kolonnā attiecas uz katru rindas definīcijas rindu, pirms vērtība rindā tiek pievienota pamata pārskatam. Piemēram, ja pakārtotā vienība ir vienlīdzīgi jāsadala starp divām nodaļām, summas katrā rindā tiek reizinātas ar 50 procentiem, pirms to vērtība tiek pieskaitīta nodaļas atskaitei. Vienai atskaites vienībai nevar būt divas pamata vienības. Lai summas no vienas atskaites vienības sadalītu divām pamata vienībām, izveidojiet citu atskaites vienību, kurai ir tāda pati dimensija, lai apkopotu papildu 50 procentus. Ievadiet visu procentu daudzumu bez decimālzīmes. Piemēram, <strong>25</strong> nozīmē 25 procentu piešķiri uz pamata vienību. Ja iekļaujat decimālzīmi (<strong>,25</strong>), tad pamata vienībai tiek piešķirti 0,25 procenti. Lai izmantotu procentuālo vērtību, kas ir mazāka nekā 1 procents, pārskata definīcijā izmantojiet opciju <strong>Atļaut apkopojumu &lt;1%</strong>. Šī opcija ir cilnē <strong>Papildu opcijas</strong>, dialoglodziņā <strong>Pārskatu iestatījumi</strong>. Šim dialoglodziņam jūs piekļūstat, izmantojot pogu <strong>Cits</strong> atskaites definīcijas cilnē <strong>Iestatījumi</strong>. |
|     Vienības drošība     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   Ierobežojumi lietotājiem un grupām, kas var piekļūt informācijai par šo atskaites vienību.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|    Papildu teksts    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               Teksts, kas ir ietverts šajā atskaitē.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

Lai izveidotu atskaišu koka definīciju, izpildiet šādas darbības.

1.  Aizveriet pārskatu veidotāju.
2.  Noklikšķiniet uz **Fails** &gt; **Jauns** &gt; **Pārskatu koka definīcija**.
3.  Noklikšķiniet uz **Rediģēt** &gt; **Ievietot pārskata vienības no dimensijām**.
4.  Dialoglodziņā **Ievietot pārskata vienības no dimensijām**, atlasiet dimensijas vērtības, kuras vēlaties iekļaut pārskata koka definīcijā. Dialoglodziņš **Ievietot pārskata vienības no dimensijām** ir šādas sadaļas.

    | Sadaļa                          | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    |----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Pārskata dimensijas segmentācija | Lai mainītu segmentu skaitu un garumu, izmantojiet pogas **Sadalīt segmentus** un **Apvienot segmentus**. **Piezīme.** Varat apvienot tikai tādus segmentus, kurus jūs sadalījāt. Lai apvienotu vairākas dimensijas, dimensiju vērtībās izmantojiet aizstājējzīmes.                                                                                                                                                                                                          |
    | Iekļaut/rakstzīmju pozīcijas       | Šajā sadaļā ir uzskaitītas dimensijas, kas ir definētas finanšu datos, un ir parādīts rakstzīmju skaits visgarākajā katrai dimensijai definētajā vērtībā. Atzīmējiet dimensijas izvēles rūtiņu, lai šo dimensiju iekļautu atskaišu koka hierarhijā.                                                                                                                                                                                           |
    | Segmenta hierarhija un diapazoni     | Šajā sadaļā ir parādīta dimensiju hierarhija. Jūs varat pārvietot dimensijas sarakstā, lai mainītu to pārskata izveides secību. Laukos **No dimensijas** un **Līdz dimensijai** varat norādīt katras dimensijas vērtību diapazonu. Ja diapazonu nenorādāt, atskaišu kokā tiek iekļautas visas dimensiju vērtības. **Piezīme.** Ja izmantojat vairākas dimensijas, rezultātos tiek atgrieztas tikai tās dimensiju kombinācijas, uz kurām ir grāmatots. |

    Ekrānuzņēmumam, kurā ir parādīts dialoglodziņa **Ievietot atskaišu vienības no dimensijām** piemērs, skatiet sadaļu “Dialoglodziņa Ievietot atskaišu vienības no dimensijām piemērs” tālāk šajā rakstā.
5.  Lai izveidotu papildu segmentus (piemēram, vienu segmentu sadalot divos īsākos segmentos), noklikšķiniet uz nepieciešamās vietas laukā **Rakstzīmes pozīcija** un pēc tam noklikšķiniet uz **Sadalīt segmentus**.
6.  Lai divus segmentus sapludinātu vienā segmentā, noklikšķiniet vienā no sapludināmo segmentu rūtiņām un pēc tam noklikšķiniet uz **Apvienot segmentus**.
7.  Hierarhijas nosaka, kā dimensijas savstarpēji atskaitās, kā arī katras dimensijas diapazonu. Lai mainītu dimensiju hierarhiju, apgabalā **Segmentu hierarhija un diapazoni** atlasiet dimensiju, ko vēlaties pārvietot, un pēc tam noklikšķiniet uz **Pārvietot uz augšu** vai **Pārvietot uz leju**.
8.  Lai norādītu dimensijas vērtību diapazonu, pievienošanai jaunajam pārskata kokam, apgabalā **Segmenta hierarhija un diapazoni** rīkojieties šādi:
    1.  Šīs dimensijas laukā **No dimensijas**, ievadiet pirmo vērtību tās diapazonā.
    2.  Laukā **Līdz dimensijai** ievadiet pēdējo vērtību tās diapazonā.

9.  Atkārtojiet 7. un 8. darbību katrai dimensijai apgabalā **Segmentu hierarhija un diapazoni**.
10. Kad esat pabeidzis definēt veidu, kā jūsu atskaites vienības ir jāievieš jaunajā atskaišu kokā, noklikšķiniet uz **Labi**.
11. Noklikšķiniet uz **Fails** &gt; **Saglabāt**, lai saglabātu pārskatu koku. Ievadiet unikālu nosaukumu un pārskata koka aprakstu, un pēc tam noklikšķiniet uz **Labi**.

### <a name="open-an-existing-reporting-tree-definition"></a>Atveriet esoša pārskata koka definīciju

1.  Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz **Pārskata koka definīcijas**.
2.  Veiciet dubultklikšķi uz pārskata koka nosaukumu sarakstā, lai to atvērtu.
3.  Lai apskatītu veidošanas blokus, kas ir saistīti ar pārskata koku, ar peles labo pogu noklikšķiniet uz pārskata koka un tad atlasiet **Asociācijas**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Apkopot datus pārskatu kokā

Kad izmantojot atskaišu koku, summas no atskaites apakšvienībām varat apkopot atskaites pamata vienības līmenī. Šāda apkopošana tiek saukta par datu apkopošanu. Šādi noteikumi tiek izmantoti, lai pārskata kokā apkopotu summas pamata vienībās:

-   Atskaišu kokā apakšvienībām ir jāsatur dimensijas, izņemot gadījumus, kad atskaišu koks ir viena līmeņa koks. Pamata vienības atskaišu kokā parasti nesatur dimensijas. **Piezīme.** Ja norādāt dimensijas gan apakšvienībām, gan pamata vienībām, varat izraisīt datu dublēšanos šajā atskaitē.
-   Pārskata vienības, kas satur dimensijas pārskata kokā, atbilst dimensijām, kas tiek izmantotas rindu un kolonnu definīcijās. Dimensiju kombinācija nosaka šai vienībai atgrieztās summas. Piemēram, tālāk šajā rakstā sniegtajā 2. piemērā 6. un 7. rinda attiecīgi atgriež vērtības tikai nodaļām 00 un 01.
-   Summas pamata atskaites vienībām, kas atskaišu kokā nesatur dimensijas, tiek noteiktas no apakšvienību atskaites un apkopo summu uz norādīto pamatvienību. Piemēram, ja pamatvienībai (sk. Contoso USA datu apkopošanas piemēru 2. piemērā) ir divas apakšvienībās (022 un 023), un tā nesatur dimensijas, tad atskaite tiek ģenerēta katrai apakšvienībai un pamata vienībai. Pamata kopsumma sastāv no divām apakš-summām.

### <a name="manage-reporting-units"></a>Pārvaldīt pārskata vienības

Katra atskaišu koka definīcija tiek parādīta unikālos skatos. Ir grafisks skats, kurā ir redzama pamatelementu/apakšelementu hierarhija, un darblapas skats, kas parāda konkrētu informāciju par katru atskaites vienību. Grafiskais skats un darblapas skats ir saistīti. Kad kādu atskaites vienību atlasāt vienā skatā, tā tiek atlasīta arī otrā skatā. Varat būvēt starpdimensiju hierarhijas, kas ir balstītas uz dimensiju attiecībām finanšu datos. Kad veidojat atskaišu koka definīciju, tās pašas rindas definīcijas varat izmantot vairākkārt, neatkarīgi no tā, vai ģenerējat nodaļas ieņēmumu pārskatu vai konsolidēto kopsavilkuma ieņēmumu pārskatu. Dimensijas, kas ir definētas rindas definīcijā, var apvienot ar dimensijām atskaišu koka definīcijā, lai nodrošinātu dažādus jūsu organizācijas veiktspējas skatus.

### <a name="reporting-unit-structure"></a> Pārskata vienības struktūra

Finanšu atskaišu veidotājā tiek izmantoti šādi atskaites vienību tipi:

-   Detalizācijas vienība iegūst informāciju tieši no finanšu datiem, no Excel darblapas vai no citas finanšu atskaišu darblapas.
-   Kopsavilkuma vienība apkopo datus no zemāka līmeņa vienībām.

Pamata pārskata vienība ir kopsavilkuma vienība, kas uzkrāj apkopoto informāciju no detalizācijas vienības. Kopsavilkuma vienība var būt gan detalizēta vienība, gan kopsavilkuma vienība. Tādēļ kopsavilkuma vienība informāciju var iegūt no zemāka līmeņa vienības, finanšu datiem vai Excel darblapas. Pamata vienība var būt augstākas pamata vienības apakšvienība. Atskaites apakšvienība var būt detalizēta vienība, kas informāciju iegūst tieši no finanšu datiem vai Excel darblapas. Atskaites apakšvienība var būt arī starpposma kopsavilkuma vienība. Citiem vārdiem sakot, tā var būt pamata vienība kādai zemāka līmeņa vienībai un arī apakšvienība kādai augstāka līmeņa kopsavilkuma vienībai. Visbiežāk izmantotajā atskaites vienību scenārijā pamata vienībām ir tukša šūna kolonnā **Dimensijas**, un apakšvienībām ir saites uz noteiktām vai aizstājējzīmju dimensiju kombinācijām.

### <a name="organize-reporting-units"></a> Organizēt pārskata vienības

Varat mainīt pārskatu koka definīcijas organizācijas struktūru, pārvietojot pārskatu vienības grafiskajā skatā. Atskaišu vienības varat arī pārvietot uz augstāku līmeni atskaišu kokā vai pārcelt tās uz zemāku līmeni.

1.  Pārskatu veidotājā atveriet modificējamo pārskata koka definīciju.
2.  Pārskata koka definīciju grafiskajā skatā atlasiet pārskata vienību.
3.  Velciet vienību uz jauno pozīciju. Varat arī uz vienības noklikšķināt ar peles labo pogu un atlasīt vienumu **Paaugstināt atskaites vienību** vai **Pazemināt atskaites vienību**.
4.  Noklikšķiniet uz **Fails** &gt; **Saglabāt**, lai saglabātu izmaiņas.

### <a name="add-text-about-a-reporting-unit"></a> Pievienojiet tekstu par pārskata vienību

Papildu teksta ieraksts ir statiska teksta virkne līdz 255 rakstzīmju garumā, kas papildina atskaišu koka definīcijas informāciju. Piemēram, papildu teksts var būt īss uzņēmuma apraksts. Jūs varat izveidot līdz pat desmit papildu teksta ierakstiem katrai pārskata vienībai pārskata koka definīcijā. Papildu teksts atskaitē ir redzams tai atskaites vienībai, kurai šis teksts ir piešķirts. Teksta ierakstus varat pievienot no rindas definīcijas kolonnas **Apraksts** un no atskaites definīcijas cilnes **Galvenes un kājenes**.

1.  Pārskatu veidotājā atveriet modificējamo pārskata koka definīciju.
2.  Veiciet dubultklikšķi uz atskaites vienības rindas šūnas **Papildu teksts**.
3.  Dialoglodziņa **Papildu teksts** pirmajā tukšajā rindā ievadiet tekstu. Pirmā rinda, kas satur tekstu, tiek apzīmēta kā UnitText1, neatkarīgi no tās pozīcijas dialoglodziņā **Papildu teksts**.
4.  Lai šai atskaites vienībai pievienotu vairākus teksta ierakstus, ievadiet tekstu tukšajā rindā.
5.  Noklikšķiniet uz **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Noņemiet papildu tekstu no pārskata vienības

1.  Pārskatu veidotājā atveriet modificējamo pārskatu koka definīciju.
2.  Pārskatu vienības rindai veiciet dubultklikšķi uz šūnas **Papildu teksts**.
3.  Dialoglodziņā **Papildu teksts** atlasiet ierakstu, kas jānoņem, un pēc tam noklikšķiniet uz **Notīrīt**. Vai noklikšķiniet uz ieraksta ar peles labo pogu un atlasiet **Izgriezt**.
4.  Noklikšķiniet uz **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Ierobežot piekļuvi pārskata vienībai

Jūs varat neļaut noteiktiem lietotājiem un grupām piekļūt pārskata vienībai. Ierobežojumus varat arī definēt tā, lai attiektos uz atskaites vienības atskaites apakšvienībām.

1.  Pārskatu veidotājā atveriet modificējamo pārskata koka definīciju.
2.  Lai ierobežotu piekļuvi, veiciet dubultklikšķi uz pārskatu vienības rindas šūnas **Vienības drošība**.
3.  Dialoglodziņā **Vienības drošība**, noklikšķiniet uz **Lietotāji un grupas**.
4.  Atlasiet lietotājus vai grupas, kam ir nepieciešama piekļuve šai atskaites vienībai, un pēc tam noklikšķiniet uz **Labi**.
5.  Lai ierobežotu piekļuvi atskaites apakšvienībām, atzīmējiet izvēles rūtiņu **Pievienot drošību atskaites apakšvienībām**.
6.  Noklikšķiniet uz **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Atņemt piekļuvi pārskata vienībai

1.  Pārskatu veidotājā atveriet modificējamo pārskata koka definīciju.
2.  Atskaites vienības rindai veiciet dubultklikšķi uz šūnas **Vienības drošība**, lai noņemtu piekļuvi tai.
3.  Dialoglodziņā **Vienības drošība** atlasiet nosaukumu un pēc tam noklikšķiniet uz **Noņemt**.
4.  Noklikšķiniet uz **OK**.

### <a name="link-to-reports"></a>Izveidot saiti uz atskaitēm

Kad rindas definīcijā esat izveidojis kolonnu **Atskaite** un esat norādījis atskaiti, kuru iekļaut šajā atskaitē, atskaišu koks ir jāatjaunina ar saistīto kolonnu un informāciju par šo atskaiti. Atskaiti var importēt jebkurā atskaišu koka vienībā.

### <a name="identify-the-report-in-a-reporting-tree"></a>Identificēt atskaiti atskaišu kokā

1.  Pārskatu veidotājā atveriet modificējamo pārskata koka definīciju.
2.  Kolonnas **Rindu definīcijas** šūnās iekļautā informācija ir balstīta uz atlasītajā rindā esošo informāciju, jo visās atskaišu koka vienībās ir jāizmanto vienāda rindas definīcija. Veiciet dubultklikšķi uz šūnas **Rindu definīcijas** un pēc tam atlasiet rindas definīciju, kas satur informāciju par šo atskaiti.
3.  Atskaites vienības šūnā **Darblapas saite** atlasiet saites nosaukumu, kas atbilst šai atskaitei.
4.  Atskaites vienības šūnā **Darbgrāmatas vai atskaites ceļš** ievadiet atskaites nosaukumu vai pārlūkojiet, lai atlasītu šo atskaiti.
5.  Lai atskaitē norādītu kādu darblapu, ievadiet šīs darblapas nosaukumu šūnā **Darblapas nosaukums**.
6.  Atkārtojiet 3. līdz 5. darbību katrai atskaites vienībai, kam ir jāsaņem dati no kādas atskaites. Lai nepieļautu, ka jūsu atskaitē tiek rādīti nepareizi dati, pārliecinieties, ka atskaišu koka atbilstošajā vienībā ir redzami pareizie atskaišu nosaukumi.

## <a name="examples"></a>Piemēri
### <a name="reporting-unit-structure--example-1"></a>Atskaites vienības struktūra — 1. piemērs

Šeit ir atskaišu vienību struktūra šādā atskaišu kokā:

-   Atskaites vienība Contoso Japan ir pamata vienība apakšvienībām Contoso Japan Sales un Contoso Japan Consulting.
-   Nodaļa Contoso Japan Sales ir gan apakšvienība vienībai Contoso Japan, gan pamata vienība vienībām Home Sales un Auto Sales.
-   Viszemākā līmeņa detalizācijas atskaites vienības (Home Sales, Auto Sales, Client Services un Operations) apzīmē nodaļas finanšu datos. Šīs pārskata vienības ir diagrammas ēnotais apgabals.
-   Augstāka līmeņa kopsavilkuma vienības apkopo informāciju no detaļu vienībām.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Atskaites vienības struktūra — 2. piemērs

Nākamajā diagrammā ir redzams atskaišu koks, kam ir organizatoriska struktūra, kura ir sadalīta pēc biznesa funkcijas. [![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Dialoglodziņa Ievietot atskaišu vienības no dimensijām piemērs

Nākamajā attēlā ir parādīts dialoglodziņa **Ievietot atskaišu vienības no dimensijām** piemērs. Šajā piemērā rezultāti atgriezīs biznesa vienību, izmaksu centru un nodaļu kombinācijas. [![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png) Iegūtā pārskatu koka definīcija tiek kārtota pēc biznesa vienības, pēc tam pēc izmaksu centra un pēc tam pēc nodaļas. Piektās pārskata vienības dimensija ir **Biznesa vienība = \[001\], Izmaksu centrs = \[\], Nodaļa = \[022\]**, un tā norāda pārskata vienību kontiem, kas atbilst biznesa vienībai 001 un nodaļai 022. [![ReportingTree](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Datu apkopojuma piemēri

Nākamajos piemēros ir parādīta iespējamā informācija, kas tiek izmantota atskaišu koka definīcijā tādiem datiem, kas tiek apkopoti.

#### <a name="example-1"></a>1. piemērs

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>2. piemērs

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

# <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskati](financial-reporting-intro.md)




