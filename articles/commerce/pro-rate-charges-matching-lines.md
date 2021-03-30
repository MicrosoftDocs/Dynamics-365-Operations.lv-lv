---
title: Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās
description: Šajā tēmā ir aprakstītas papildu iespējas automātisko maksu aprēķināšanai un piesaistīšanai Commerce kanāla pasūtījumiem, izmantojot papildu automātisko maksu līdzekli.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f458ce6ea4fa3efdfa470e90efa1e267047a8e37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231131"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīta virsraksta līmeņa automātisko maksu grupēšanas un to proporcionālas sadalīšanas komercijas pārdošanas rindās funkcionalitāte. Šī funkcionalitāte ir pieejama transakcijām, kas ir izveidotas pārdošanas punktā (POS) Retail versijā 10.0.1, un pārdošanām, kas ir izveidotas zvanu centrā Retail versijā 10.0.2.

Šī funkcionalitāte ir pieejama tikai tad, ja līdzeklis [papildu automātiskās maksas](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) ir ieslēgts, izmantojot opciju lapā **Commerce parametri**. Turklāt, automātisko maksu uzlaboto aprēķinu metodi var izmantot tikai mazumtirdzniecības pārdošanas pasūtījumiem, kas ir izveidoti, izmantojot komercijas kanālus (POS, zvanu centru un Dynamics e-komercijas platformu).

Šī jaunā funkcionalitāte nodrošina organizācijām lielāku elastību tā, ka virsraksta līmenī automātiskās maksas tiek aprēķinātas un piesaistītas pārdošanas transakcijām.

Par programmas versiju 10.0.1 vecākās versijās virsraksta līmenī automātiskās maksas ar konkrētu piegādes relācijas režīmu tiek aprēķinātas tikai tad, ja tās atbilst piegādes režīmam, kas ir definēts pārdošanas pasūtījuma virsrakstā.

Piemēram, virsraksta līmeņa automātiskās maksas ir definētas piegādes režīmam **99** un **11**. Pasūtījuma virsrakstā tiek izveidots pārdošanas pasūtījums un tiek definēts piegādes režīms **99**. Tomēr dažas pārdošanas rindas ir iestatītas tā, ka tie tiek nosūtīti, izmantojot piegādes režīmu **11**. Šajā gadījumā vērā tiek ņemtas tikai tās virsraksta līmeņa maksas, kas ir saistītas ar piegādes režīmu **99**, un tās tiek piesaistītas pārdošanas pasūtījumam.

Programmā Commerce uz virsraksta līmeņa maksām attiecas papildu līdzeklis, kas ļauj definēt [diferencētas maksas konfigurāciju](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery), kas ir atkarīga no pasūtījuma vērtības. Piemēram, ja pasūtījuma vērtība ir no $50,00 līdz $200,00, organizācija var izvēlēties iekasēt transporta maksu $5,00. Tomēr, ja pasūtījuma vērtība ir no $200,01 līdz $500,00, kravas maksa var būt $4,00.

Dažas organizācijas vēlas iegūt diferencētas maksas aprēķināšanas priekšrocības, kas ir nodrošināts ar virsraksta līmeņa maksām. Tomēr gadījumos, kad ir iesaistīti jaukti piegādes režīmi, tās arī vēlas nodrošināties, ka aprēķinātās maksas ir atkarīgas no atbilstības ar piegādes režīmu, kas ir definēts katrai pārdošanas rindai.

Tagad virsraksta līmeņa automātiskās maksas var konfigurēt tā, lai, aprēķinot maksas, tiek ņemti vērā visi piegādes režīmi pasūtījumā. Šai funkcionalitātei ir nepieciešama sarežģītāka aprēķinu loģika, lai aprēķinātu virsraksta līmeņa maksas. Loģika grupē kopā visus krājumus, kuri ir nosūtīti, izmantojot vienu piegādes režīmu, un, aprēķinot virsraksta līmeņa automātiskās maksas, tā apstrādā šo grupu kā krājumu aprēķina grupu. Krājumiem ar vienu piegādes režīmu automātiskās maksas tiek aprēķinātas pēc krājumu apvienotās pārdošanas vērtības. Šādā veidā tiek noteikta attiecīgā automātiskās maksas pakāpe.

Kad pārdošanas rindām, kas ir nosūtītas, izmantojot vienu piegādes režīmu, ir iegūtas attiecīgās virsraksta līmeņa maksas, aprēķinātās maksas tiek proporcionāli sadalītas pārdošanas rindas līmenī. Tā kā šīs maksas ir rindas līmenī un netiek saglabātas virsraksta līmenī, tiek izveidota precīzāka saite starp krājumu un maksas vērtību, kas tam ir aprēķināta. Šī funkcionalitāte var noderēt daļējas atgriešanas gadījumos, ja organizācija vēlas atmaksāt tikai daļu nevis visu maksu, ja tiek atgriezti tikai daži krājumi.

## <a name="scenarios"></a>Scenāriji

Nākamajos divos piemēra gadījumos ir aprakstīts, kā šīs maksas tiek aprēķināts, gan izmantojot, gan neizmantojot jauno funkcionalitāti.

### <a name="scenario-1"></a>1. scenārijs

Šajā gadījumā tiek aprakstīta funkcionalitāte, ja automātiskās maksas iestatījumos ir iestatīta opcijas **Proporcionāls aprēķins atbilstošajām pārdošanas rindām** vērtība **Nē**. (Funkcionalitāte ir līdzvērtīga virsraksta līmeņa maksas funkcionalitātei programmas versijās, kas ir vecākas par versiju 10.0.1).

Šajā gadījumā organizācija ir definējusi virsraksta līmeņa maksas piegādes relācijas režīmam **99** un **11**. Piegādes režīmam **21** nav konfigurētas automātiskās izmaksas.

![Automātiskās izmaksas piegādes režīmam 99, ja atbilstošās rindas proporcionālā sadalīšana ir izslēgta](media/99_disabled.png)

![Automātiskās izmaksas piegādes režīmam 11, ja atbilstošās rindas proporcionālā sadalīšana ir izslēgta](media/11_disabled.png)

Zvanu centrā ir izveidots pārdošanas pasūtījums, un piegādes režīms ir iestatīts **99**. Šis pasūtījums satur piecus krājumus. Divas pasūtījuma rindas ir konfigurētas izmantot piegādes režīmu **99**, divas rindas ir konfigurēta izmantot piegādes režīmu **11** un viena rinda ir konfigurēta izmantot piegādes režīmu **21**, kā redzams nākamajā tabulā.

| Objekts  | Rindas daudzums | Piegādes režīms | Vienības cena |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11.            | $10            |
| 81332 | 1             | 99            | 50 USD            |
| 81333 | 2             | 11.            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Šajā gadījumā viss pasūtījums tiek izvērtēts, salīdzinot ar piegādes režīma **99** automātiskās maksas tabulu. Visu pārdošanas rindu kopsummu izmanto, lai noteiktu automātiskās maksas konfigurācijas atbilstības pakāpi, un šī maksa tiek saistīta ar pasūtījuma virsraksta līmeni. Šajā piemērā pasūtījuma kopsummas ir $165,00, un $15,00 kravas maksa tiek saistīta ar pasūtījuma virsrakstu. Automātiskās maksas, kas ir konfigurētas piegādes režīmam **11**, netiek nekur norādītas vai piesaistītas.

Šajā gadījumā, ja debitors atgriež dažus pasūtījumā iekļautos krājumus un ja [maksas kods ir konfigurēts tā, ka tas tiks atgriezts](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), kopējā virsraksta līmeņa maksa sistemātiski tiek saistīta ar atmaksu arī tad, ja atgriezti tiek tikai daži krājumi.

### <a name="scenario-2"></a>2. scenārijs

Šajā gadījumā virsraksta līmeņa maksas tiek definētas piegādes relācijas režīmam **99** un **11**. Tomēr šīm automātiskās maksas tabulām ir iestatīta opcijas **Proporcionāls aprēķins atbilstošajām pārdošanas rindām** vērtība **Jā**.

![Automātiskās izmaksas piegādes režīmam 99, ja atbilstošās rindas proporcionālā sadalīšana ir ieslēgta](media/99_enabled.png)

![Automātiskās izmaksas piegādes režīmam 11, ja atbilstošās rindas proporcionālā sadalīšana ir ieslēgta](media/11_enabled.png)

Šajā gadījumā tiek izmantots tas pats pārdošanas pasūtījums, kas satur piecas rindas. Piegādes režīms pasūtījuma virsrakstā ir iestatīts **99**, bet katra krājuma piegādes režīms pārdošanas pasūtījumā ir konfigurēts tā, kā redzams nākamajā tabulā.

| Objekts  | Rindas daudzums | Piegādes režīms | Vienības cena |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11.            | $10            |
| 81332 | 1             | 99            | 50 USD            |
| 81333 | 2             | 11.            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Tā kā automātiskās maksas konfigurācija ir iestatīta proporcionāli sadalīt atbilstošās pārdošanas rindas, sistēma veic tālāk norādītās aprēķināšanas darbības.

1. Visi krājumi ar vienādu piegādes režīmu tiek grupēti kopā, un sistēma aprēķina grupas krājumu kopējo preču vērtību.

    **Piegādes režīms 11**

    - Krājumi 81331, daudzums 1 = $10
    - Krājumi 81333, daudzums 2 = $60 neto ($30 uz vienu vienību)
    - **Kopējā preču vērtība piegādes režīmam 11 = $70**

    **Piegādes režīms 99**

    - Krājumi 81332, daudzums 1 = $50
    - Krājumi 81334, daudzums 3 = neto $30
    - **Kopējā preču vērtība piegādes režīmam 99 = $80**

    **Piegādes režīms 21**

    - Krājumi 81334, daudzums 3 = neto $15
    - **Kopējā preču vērtība piegādes režīmam 21 = $15**

2. Sistēma meklē virsraksta līmeņa automātisko maksu konfigurāciju, kas atbilst debitora un piegādes režīma iestatījumiem katrai krājumu grupai. Ja konfigurācija tiek atrasta, sistēma pārskata pakāpēs sadalīto konfigurāciju, lai atrastu maksu, kura ir jāsaista pēc krājumu piegādes grupas režīmā kopējās preču vērtības.

    **Piegādes režīms 11**

    - Kopējā preces vērtība = $70
    - **Maksas vērtība = $7**

    **Piegādes režīms 99**

    - Kopējā preces vērtība = $80
    - **Maksas vērtība = $15**

    **Piegādes režīms 21**

    - Kopējā preces vērtība = $15
    - **Maksas vērtība = $0** (Šai debitora un piegādes režīma kombinācijai nav konfigurēta neviena automātiskā maksa.)

    ![Piegādes režīma 11 maksas atbilst atzīmētajai pakāpei](media/step2mode11.png)

    ![Piegādes režīma 99 maksas atbilst atzīmētajai pakāpei](media/step2mode99.png)

3. Sistēma aprēķina maksas vērtību, kas jāsaista ar katru rindu, atkarībā no proporcionālās sadalīšanas loģiku, kas ņem vērā rindas proporcionālo vērtību saistībā ar grupas kopējo preču vērtību.

    **Piegādes režīms 11**

    - Maksas vērtība = $7
    - Grupas preču vērtība = $70
    - 1. rindas vērtība = $10 (= 14,2857 procenti no grupas vērtības)
    - 3. rindas vērtība = $60 (= 85,7143 procenti no grupas vērtības)
    - **Rindas maksas par 1. rindu = $1**
    - **Rindas maksas par 3. rindu = $6**

    **Piegādes režīms 99**

    - Maksas vērtība = $15
    - Grupas preču vērtība = $80
    - 2. rindas vērtība = $50 (= 62,5 procenti no grupas vērtības)
    - 4. rindas vērtība = $30 (= 37,5 procenti no grupas vērtības)
    - **Rindas maksas par 2. rindu = $9,38**
    - **Rindas maksas par 4. rindu = $5,62**

    **Piegādes režīms 21**

    - Maksas vērtība = $0
    - Grupas preču vērtība = $15
    - 5. rindas vērtība = $15 (= 100 procenti no grupas vērtības)
    - **Rindas maksas par 5. rindu = $0**

Līdz ar to šajā piemērā krājums 81334 tiks saistīts ar kravas maksu $5,62. Šīs izmaksas var skatīt pārdošanas rindas lapā **Uzturēt maksas**. Nākamajā attēlā ir redzams šīs izskats krājumam 81334.

![Proporcionāli sadalītas maksas pārdošanas rindā krājumam 81334](media/proratedlinecharge.png)

Ja šī aprēķināšanas metode tiek izmantota daļējas atgriešanas gadījumā un ja maksas kods atbilst atgriešanai, tikai maksas daļa, kas ir piešķirta šai rindai, tiks atgriezta krājuma atgriešanas gadījumā.

## <a name="additional-resources"></a>Papildu resursi

[Omni kanāla papildu automātiskās maksas](omni-auto-charges.md)

[Automātisko maksu iespējošana un konfigurēšana katram kanālam](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]