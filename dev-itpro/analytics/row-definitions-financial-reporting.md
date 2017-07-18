---
title: "Rindas definīcijas finanšu atskaišu veidotājā"
description: "Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē. Rindas definīciju var kombinēt ar kolonnas definīcijām, atskaišu koka definīcijām un atskaites definīcijām, lai izveidotu veidošanas bloku grupu, kuru var izmantot vairāki uzņēmumi."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 6d4697af6f7467f25a461fae4e9320402f83b0e3
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="row-definitions-in-financial-report-designer"></a>Rindas definīcijas finanšu atskaišu veidotājā

[!include[banner](../includes/banner.md)]


Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē. Rindas definīciju var kombinēt ar kolonnas definīcijām, atskaišu koka definīcijām un atskaites definīcijām, lai izveidotu veidošanas bloku grupu, kuru var izmantot vairāki uzņēmumi.

<a name="create-a-row-definition"></a>Izveidojiet rindas definīciju
-----------------------

1.  Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.
2.  Izvēlnē **Fails** noklikšķiniet uz **Jauns** un pēc tam noklikšķiniet uz **Rindas definīcija**. Lai iegūtu papildu informāciju par katras šūnas saturu, skatiet [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Rindas definīcijas atvēršana
1.  Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.
2.  Veiciet dubultklikšķi uz tās rindas definīcijas, kuru vēlaties atvērt.
3.  Lai apskatītu veidošanas blokus, kas ir saistīti ar rindas definīciju, ar peles labo pogu noklikšķiniet uz rindas definīcijas un tad atlasiet **Asociācijas**.

## <a name="contents-of-a-row-definition"></a>Rindas definīcijas saturs
Rindas definīcijas var ietvert līdz 20 000 finanšu dimensiju rindu, kā arī tālāk minēto informāciju.

-   Aprakstošs teksts, kas piešķir atskaitei jēgu, izveidojot sadaļu virsrakstus, rindas un atstarpes, piemēram, **Skaidra nauda** vai **Kopējie ieņēmumi**.
-   Saites uz finanšu datiem, kas var ietvert dimensiju vērtības programmatūrā Microsoft Dynamics 365 for Finance and Operations **Piezīme.** Varat iestatīt rindas definīciju, lai izgūtu datus no finanšu dimensiju sistēmas ikreiz, kad tiek ģenerēts pārskats.
-   Rindu kopsummas un formulas, kuru pamatā ir saistītie finanšu dati

Parasti katra rinda rindas definīcijā satur vienu no šiem informācijas tipiem:

-   Atsauces uz finanšu dimensiju sistēmu
-   Kopsummas vai uz datiem balstīti aprēķini
-   Formatēšana

Rindas definīcijā informāciju var ievadīt divos veidos:

-   Informāciju manuāli ievadīt jaunā rindas definīcijā. Plašāku informāciju skatiet sadaļā [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).
-   Izmantot atskaišu veidotāju, lai rindas informāciju izgūtu tieši no finanšu dimensijām. Plašāku informāciju skatiet sadaļā “Saistītās formulas/rindas/vienības”, rakstā [Modificēt rindu definīcijas šūnas](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Dimensiju pievienošana rindas definīcijai
Dimensija ir datu un vērtību krustpunkts. Atskaišu veidotājā datus un vērtības varat grupēt. Pēc tam transakcijas varat detalizētāk klasificēt un analizēt. Varat izmantot dialoglodziņu **Ievietot rindas no dimensijām**, lai vienlaicīgi rindas definīcijai pievienotu vairākas rindas. Dialoglodziņā katrai dimensijai attēlo vienu kolonnu. Nākamajā tabulā ir aprakstīta informācija, ko varat norādīt katrai dimensijai.

| Opcija                | Apraksts                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensija             | Modelis, kas identificē dimensiju, kura jāpievieno rindas definīcijai. Šajā modelī ir ietverta viena zīme & un viena restītes zīme (\#) atbilstoši katrai dimensiju pozīcijai. Parasti visas (&) zīmes tiek izmantotas galvenā konta dimensijai, un visas numura zīmes tiek izmantotas citām dimensijām. |
| Dimensijas diapazona sākums | Pirmā vērtība šai dimensijai, kuru pievienot rindas definīcijai.                                                                                                                                                                                                                 |
| Dimensijas diapazona beigas   | Pēdējā vērtība šai dimensijai, kuru pievienot rindas definīcijai.                                                                                                                                                                                                                  |

Lai rindas definīcijai pievienotu dimensijas, izpildiet šādas darbības.

1.  Atskaišu veidotājā noklikšķiniet uz **Rindas definīcijas** un atveriet modificējamo rindas definīciju.
2.  Izvēlnē **Rediģēšana** noklikšķiniet uz **Ievietot rindas no dimensijām**.
3.  Dialoglodziņa **Ievietot rindas no dimensijām** rindā **Dimensijas** atlasiet šūnu dimensijai, kuru pārsūtīt uz rindas definīciju, un pēc tam noklikšķiniet uz **Visas &&&**.
4.  Lai rindas definīcijai ļautu izmantot tikai noteiktu dimensijas vērtību diapazonu, dimensijas sākuma vērtību ievadiet šūnā **Dimensijas diapazona sākums** un pēc tam dimensijas beigu vērtību ievadiet šūnā **Dimensijas diapazona beigas**. Lai atlasītajai dimensijai iekļautu visas vērtības, atstājiet šīs šūnas tukšas. **Piezīme.** . Aizstājējzīmes (\* vai ?) dimensiju diapazonos var neatgriezt visus vēlamos rezultātus atkarībā no tā, kā ERP datu bāzē tiek apkopoti dati.
5.  Laukā **Sākuma rindas kods** norādiet rindas kodu pirmajai dimensijas vērtībai, kas jāpievieno rindas definīcijai.
6.  Laukā **Pieauguma solis katrā rindā** norādiet atstarpi starp secīgiem rindu kodiem. Piemēram, ja pirmās rindas kods ir 100 un pieauguma vērtība ir 30, pirmo jauno rindu kodi ir 100, 130, 160, 190 un 220. Izmantojiet pieauguma vērtību, kas nodrošina pietiekami daudz vietas jaunu formāta un formulas rindu ievietošanai.
7.  Noklikšķiniet uz **Labi**. Katrai no atlasītajām dimensijas vērtībām rindas definīcijai tiek pievienota viena rinda.

## <a name="adjust-rounding-in-a-row-definition"></a>Noapaļošanas koriģēšana rindas definīcijā
Ja jums ir bilance, kur summas tiek noapaļotas, tad kopsummas var nesakrist. Šāda problēma var rasties, ja, piemēram, jūs bilances atskaitē izmantojat noapaļošanas opciju un arī atskaites definīcijai ir norādīta noapaļošana. Varat rindas definīcijā izmantot opciju **Noapaļošanas korekcija**, lai sabalansētu bilanču summas. Varat noapaļošanu izslēgt vai to modificēt atskaites definīcijas cilnē **Iestatījumi**. Sekojošajā tabulā redzams, kā šīs summas tiek noapaļotas. Ja noapaļošana ir ieslēgta, šīs tabulas 100. un 200. rindas kopsummas atšķiras.

| Rindas kods | Summas bez noapaļošanas | Summa ar noapaļošanu līdz pilniem tūkstošiem |
|----------|--------------------------|-----------------------------------------|
| 100      | 3600                    | 4.                                       |
| 200      | 3700                    | 4.                                       |
| KOPĀ    | 7300                    | 8.                                       |

Lai koriģētu bilances noapaļošanu, izpildiet šādas darbības.

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Noapaļošanas korekcija**.
3.  Dialoglodziņā **Noapaļošanas korekcijas** ievadiet tālāk minētās vērtības.
    -   **Noapaļošanas korekcijas rinda** — rindas kods tai rindai, kura ir jāpielāgo bilances izlīdzināšanai.
    -   **Kopējo aktīvu rinda** — rindas kods rindai bilancē, kas satur kopējo aktīvu summu.
    -   **Saistību un kapitāla kopsummas rinda** — rindas kods rindai bilancē, kas satur kopējo saistību un kapitāla summu.
    -   **Korekcijas summas ierobežojums** — pozitīvs vesels skaitlis, kas norāda automātisko korekciju ierobežojumu. Šī summa tiek salīdzināta ar faktisko noapaļošanas starpības absolūto vērtību.

    **Piezīme:** šie rindu kodi ir jāsaista ar jūsu finanšu datiem. Citiem vārdiem sakot, rindas šūnā **Saite uz finanšu dimensijām** jābūt dimensijas vērtībai. **Neatsaucieties** uz apraksta (**DESC**), aprēķina (**CALC**) vai kopsavilkuma (**TOT**) rindu.

Kad noapaļošana ir ieslēgta, jūsu bilances summas tagad tiks izlīdzinātas. **Piezīme:** korekcijas ierobežojums tiek piemērots, pamatojoties uz opciju **Noapaļošanas precizitāte**, kas ir norādīta pārskata definīcijā. Piemēram, ja atskaites summas noapaļojat līdz tūkstošiem un laukā **Korekcijas summas ierobežojums** ievadāt **2**, tad brīdinājuma ziņojums tiek parādīts, kad laukā **Noapaļošanas korekcijas rinda** esošā vērtība tiek palielināta vai samazināta par vairāk nekā 2000.

## <a name="format-row-and-column-text"></a>Rindu un kolonnu teksta formatēšana
Savu pārskatu izskatu varat pielāgot, mainot fontus un izmantojot teksta formatēšanu. Nākamajās sadaļās ir paskaidrots, kā formatēt atskaišu rindu un kolonnu izskatu.

### <a name="manage-font-styles"></a>Fontu stilu pārvaldība

Savai atskaitei varat veidot un modificēt fontu stilus. Pēc tam šos stilus varat lietot dokumentam vai konkrētai atskaites rindai vai kolonnai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Fonta stila izveide</td>
<td><ol>
<li>Pārskatu veidotāja izvēlnē <strong>Formāts</strong> noklikšķiniet uz <strong>Stili un formatējums</strong>.</li>
<li>Dialoglodziņā <strong>Stili un formatējums</strong> noklikšķiniet uz <strong>Jauns</strong> un pēc tam ievadiet unikālu nosaukumu jaunajam stilam.</li>
<li>Veiciet fontu atlasi un tad noklikšķiniet uz <strong>Labi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Fonta stila modificēšana</td>
<td><ol>
<li>Pārskatu veidotāja izvēlnē <strong>Formāts</strong> noklikšķiniet uz <strong>Stili un formatējums</strong>.</li>
<li>Dialoglodziņā <strong>Stili un formatējums</strong> atlasiet modificējamo stilu un pēc tam noklikšķiniet uz <strong>Modificēt</strong>.</li>
<li>Veiciet fontu atlasi un tad noklikšķiniet uz <strong>Labi</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Fonta stila pielietošana</td>
<td><ol>
<li>Atskaišu veidotājā, definīcijā vai kolonnas definīcijā, vai galvenēs un kājenēs atlasiet vienu vai vairākas šūnas.</li>
<li>Atlasiet fonta stilu rīkjoslas sarakstā <strong>Stils</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Rindas teksta formatēšana

Rindas definīcijā norādītais formatējums ignorē visu formatējumu, kas ir norādīts kolonnas definīcijā un atskaites definīcijā. Teksta formātu varat modificēt, izmantojot formatēšanas rīkjoslas vadīklas. Šīs vadīklas ir standarta Microsoft Windows vadīklas.

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Atlasiet formatējamās šūnas. Lai atlasītu vairākas šūnas, atlasīšanas laikā turiet taustiņu Ctrl.
3.  Noklikšķiniet uz piemērojamā formāta rīkjoslas pogas. Piemēram, lai izveidotu rindas atkāpi, atlasiet rindu un pēc tam rīkjoslā noklikšķiniet uz **Palielināt atkāpi** ![Palielināt atkāpi](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Palielināt atkāpi").

### <a name="adjust-columns-while-you-design-reports"></a>Kolonnu pielāgošana pārskatu veidošanas laikā

Lai atvieglotu iespēju apskatīt kolonnas, ar kurām strādājat rindas definīcijā, varat pielāgot kolonnas platumu, ka arī paslēpt (minimizēt) vai parādīt kolonnas apskates rūtī. Jūsu veiktās modifikācijas ietekmē tikai kolonnu izskatu ekrānā. Tās neietekmē šo kolonnu formatējumu atskaitēs.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Kolonnas platuma maiņa apskates rūtī

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Izvēlnē **Formāts** atlasiet **Kolonnas platums**.
3.  Dialoglodziņā **Kolonnas platums** ievadiet kādu vērtību un pēc tam noklikšķiniet uz **Labi**. Lai mainītu kolonnas platumu, varat arī vilkt kolonnas virsraksta šūnas labo malu.

### <a name="hide-columns-in-the-view-pane"></a>Kolonnu paslēpšana apskates rūtī

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Atlasiet kolonnu vai kolonnas, kuras vēlaties minimizēt.
3.  Veiciet klikšķi ar peles labo pogu un tad noklikšķiniet uz **Paslēpt**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Visu paslēpto kolonnu rādīšana apskates rūtī

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Ar peles labo pogu noklikšķiniet uz minimizētās kolonnas, kuru vēlaties parādīt, un pēc tam noklikšķiniet uz **Parādīt**.


<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskati](financial-reporting-intro.md)




