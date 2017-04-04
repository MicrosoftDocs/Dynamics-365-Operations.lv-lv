---
title: "Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos"
description: "Šajā tēmā aprakstīta izteiksmes ierobežojumu un tabulas ierobežojumu lietošana. Ierobežojumi, lai kontrolē atribūta vērtības, ko varat atlasīt, kad konfigurējat preces pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam. Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1fe8a0d90a3f707fa7b0fea0310c819ce5040a42
ms.lasthandoff: 03/30/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos

Šajā tēmā aprakstīta izteiksmes ierobežojumu un tabulas ierobežojumu lietošana. Ierobežojumi, lai kontrolē atribūta vērtības, ko varat atlasīt, kad konfigurējat preces pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam. Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus. 

Ierobežojumus izmanto, lai kontrolētu atribūta vērtības, ko var atlasīt, konfigurējot preces pārdošanas pasūtījumam, pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam. Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus.

## <a name="what-are-expression-constraints"></a>Kas ir izteiksmes ierobežojumi?
Izteiksmes ierobežojumus raksturo izteiksme, kas izmanto aritmētiskos un Būla operatorus un funkcijas. Izteiksmes ierobežojums ir rakstīts noteiktai sastāvdaļai preces konfigurācijas modelī. To nevar izmantot atkārtoti vai koplietot ar citu sastāvdaļu. Tomēr sastāvdaļās izteiksmes ierobežojumi var izveidot atsauci uz sastāvdaļās apakšsastāvdaļas atribūtiem.

## <a name="what-are-table-constraints"></a>Kas ir tabulas ierobežojumi?
Tabulas ierobežojumi uzskaita vērtību kombinācijas, kas ir atļautas atribūtiem, konfigurējot preci. Tabulas ierobežojuma definīcijas var izmantot apkopojoši. Veidojot tabulas ierobežojumu sastāvdaļai preču konfigurācijas modelī, jūs izvēlaties tabulas ierobežojuma definīciju. Lai izveidotu kombinācijas, kas ir pieļaujamas, jūs pievienojat specifisku sastāvdaļu atribūtus. Katram atribūta veidam ir specifiska vērtība.

### <a name="example-of-a-table-constraint"></a>Tabulas ierobežojuma piemērs

Šajā piemērā parādīts, kā ierobežot skaļruņa konfigurāciju atbilstoši konkrētai korpusa apdarei un priekšdaļai. Pirmā tabula parāda korpusa apdares un priekšdaļas veidus, kas parasti pieejami konfigurācijai. Tiek definēts vērtības * * korpusa apdare * * un **Priekšējais režģis** atribūtu tipus.

| Atribūta tips | Vērtības                      |
|----------------|-----------------------------|
| Korpusa apdare | Melna, ozolkoka, rožkoka, balta |
| Priekšējais režģis    | Melns, metāla, balts         |

Nākamajā tabulā redzamas kombinācijas, ko definē tabulas ierobežojums **Krāsa un apdare**. Izmantojot šo tabulas ierobežojumu, var konfigurēt skaļruni, kam ir ozolkoka apdare un melns režģis, rožkoka apdare un balts režģis utt.

| Pabeigt         | Režģis                       |
|----------------|-----------------------------|
| Ozola            | Melna                       |
| Rožkoka       | Balta                       |
| Balta          | Melna                       |
| Balta          | Balta                       |
| Melna          | Melna                       |
| melna          | Metāla                       | 

Jūs varat izveidot sistēmas definētus un lietotāja definētus tabulas ierobežojumus. Plašāku informāciju skatiet sadaļā [Sistēmas definēti un lietotāja definēti tabulas ierobežojumi](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Rakstīt ierobežojumus, ir jāizmanto kāda sintakse?
Rakstot ierobežojumus, jāizmanto optimizācijas modelēšanas valodas (OML) sintakse. Sistēma izmanto ierobežojums Risinātājs Solver Microsoft Foundation novērst ierobežojumus.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Vai man izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus?
Varat izmantot vai nu izteiksmes ierobežojumus vai tabulas ierobežojumus atkarībā no tā, kā vēlaties veidot ierobežojumus. Tabulas ierobežojumu varat veidot kā matricu, savukārt izteiksmes ierobežojums ir individuāls paziņojums. Konfigurējot preci, nav svarīgi, kāda veida ierobežojums tiek izmantots. Šajā piemērā parādīta divu metožu atšķirība.  

Ja konfigurējat preces, izmantojot turpmākos ierobežojumu iestatījumus, ir atļautas šādas kombinācijas.

-   Produkts melnā krāsā, 30. vai 50. izmēra
-   Produkts sarkanā krāsā, 20. izmēra

### <a name="table-constraint-setup"></a>Tabulas ierobežojuma iestatīšana

| Krāsa | Izmēri |
|-------|------|
| melna | 30   |
| melna | 50   |
| Sarkans   | 20.   |

### <a name="expression-constraint-setup"></a>Izteiksmes ierobežojuma iestatīšana

(Krāsa == "Melna" un (izmērs == "30" | izmērs == "50")) | (krāsa == "Sarkana" un izmērs = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Vai, rakstot izteiksmes ierobežojumus, lietot operatorus vai infiksālo pieraksti?
Izteiksmes ierobežojums var rakstīt, izmantojot vai nu pieejamos prefiksa operatorus, vai infiksālo pieraksti. Operatoriem **Min**, **Max** un **Abs **nevar lietot infiksālo pieraksti. Šie operatori iekļauti kā standarta operatori lielākajā daļā programmēšanas valodu.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Kādus operatorus un infiksālo pierakstus var lietot, rakstot izteiksmes ierobežojumus?
Tālāk esošajās tabulās uzskaitīti operatori un infiksālā pierakste, ko var lietot, rakstot izteiksmes ierobežojumu sastāvdaļai preces konfigurācijas modelī. Piemēri pirmajā tabulā parāda, kā rakstīt izteiksmi, izmantojot vai nu infiksālo pieraksti vai operatorus.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operators</th>
<th>Apraksts</th>
<th>Sintakse</th>
<th>Piemēri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implies</td>
<td>Tas ir patiess, ja pirmais nosacījums ir nepatiess, otrais nosacījums ir patiess vai abi.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operators:</strong> nozīmē [x! = 0, y &gt;= 0]</li>
<li><strong>Infix pierakstā:</strong> x! = 0-: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Un</td>
<td>Tas ir spēkā tikai tad, ja ir spēkā visi nosacījumi. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Patiess</strong>.</td>
<td>Un [args] infix: &amp;b &amp; ... &amp;z</td>
<td><ul>
<li><strong>Operators:</strong> un [x = = 2, y &lt;= 2]</li>
<li><strong>Infix pierakstā:</strong> x = 2 = &amp;y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vai</td>
<td>Tas ir patiess, ja jebkurš nosacījums ir patiess. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Nepatiess</strong>.</td>
<td>Vai [args] infix: | b | ... | z</td>
<td><ul>
<li><strong>Operators:</strong> vai [x = = 2, y &lt;= 2]</li>
<li><strong>Infix pierakstā:</strong> x = = 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Tas summē nosacījumus. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>0</strong>.</td>
<td>Kā _ arī [args] infix: a + b + … + z</td>
<td><ul>
<li><strong>Operators:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infiksālā pierakste:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Mīnus</td>
<td>Tas noliedz savu argumentu. Tam ir jābūt precīzi vienam nosacījumam.</td>
<td>Minus[expr], infix: -expr</td>
<td><ul>
<li><strong>Operators:</strong> Minus[x] == y</li>
<li><strong>Infiksālā pierakste:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Tas paņem absolūto nosacījuma vērtību. Tam ir jābūt precīzi vienam nosacījumam.</td>
<td>Abs[expr]</td>
<td><strong>Operators:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Reizes</td>
<td>Tas paņem preci no tā nosacījumiem. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>1</strong>.</td>
<td>Laikus [args] infix: * b * … * z</td>
<td><ul>
<li><strong>Operators:</strong> Times[x, y, 2] == z</li>
<li><strong>Infiksālā pierakste:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Jauda</td>
<td>Tas paņem eksponenciāli. Tas piemēro kāpinājumu no labās uz kreiso pusi. (Citiem vārdiem sakot, tas ir labi neasociatīvu.) Tādēļ <strong>Power [a, b, c]</strong> ir līdzvērtīga <strong>jauda [, jauda [b, c]]</strong>. <strong>Power</strong> var lietot tikai tad, ja kāpinātājs ir pozitīva konstante.</td>
<td>Strāvas [args], infix: ^ b ^ … ^ z</td>
<td><ul>
<li><strong>Operators:</strong> Power[x, 2] == y</li>
<li><strong>Infiksālā pierakste:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maks.</td>
<td>Tas dod lielāko nosacījumu. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Bezgalība</strong>.</td>
<td>Max[args]</td>
<td><strong>Operators:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Min.</td>
<td>Tas dod mazāko nosacījumu. Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Bezgalība</strong>.</td>
<td>Min[args]</td>
<td><strong>Operators:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ne</td>
<td>Tas dod sava nosacījuma apgriezto loģiku. Tam ir jābūt precīzi vienam nosacījumam.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>Operators:</strong> ne [x] &amp;ne [y = = 3]</li>
<li><strong>Infiksālā pierakste:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Piemēri nākamajā tabulā parada, kā rakstīt infiksālo pieraksti.

| Infiksālā pierakste    | apraksts                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | Papildinājums                                                                                      |
| X \*y \*z       | Reizināšana                                                                                |
| x - y             | Binārā atņemšana tiek transformēta tāpat kā binārā saskaitīšana, ja ir negatīvā otrā vērtība. |
| x ^ y ^ z         | Kāpinājums, kam ir labās puses asociācija                                                   |
| !x                | Nav Būla                                                                                   |
| x -: y            | Būla saistība                                                                           |
| x | y | z         | Būla vai                                                                                    |
| x & y & z         | Būla un                                                                                   |
| x == y == z       | Vienādība                                                                                      |
| x != y != z       | Noteikts                                                                                      |
| X &lt;y &lt;z   | Mazāks nekā                                                                                     |
| X &gt;y &gt;z   | Lielāks nekā                                                                                  |
| X &lt;= y &lt;= z | Mazāks vai vienāds ar                                                                         |
| X &gt;= y &gt;= z | Lielāks vai vienāds ar                                                                      |
| (x)               | Iekavas ignorē noklusējuma prioritāti.                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Kāpēc mani izteiksmes ierobežojumi nevalidējas pareizi?
Nevar izmantot rezervētus atslēgas vārdus kā risinātāja nosaukumus atribūtiem, sastāvdaļām vai apakšsastāvdaļām preces konfigurācijas modelī. Šeit ir saraksts ar rezervēto atslēgvārdi, ka jūs nevarat izmantot:

-   Augšējā robeža
-   Elements
-   Vienādi
-   Stāvs
-   Ja
-   Mazāks
-   Lielāks
-   Implies
-   Darbu izpildes žurnāls
-   Maks.
-   Min.
-   Mīnus
-   Plus
-   Jauda
-   Laiki
-   Slots
-   Modelis
-   Lēmums
-   Mērķis


<a name="see-also"></a>Skatiet arī
--------

[Veidotu izteiksmi ierobežojumu (uzdevuma norādījumi)](http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/)

[Aprēķinu pievienošana preču konfigurāciju modelim (uzdevuma norādījumi)](http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/)


