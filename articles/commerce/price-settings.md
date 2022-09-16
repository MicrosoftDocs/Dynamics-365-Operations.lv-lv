---
title: Izcenojuma iestatījumi
description: Šajā dokumentā ir aprakstīti dažādie cenu noteikšanas un atlaižu pārvaldības iestatījumi galvenajā birojā Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474047"
---
# <a name="pricing-settings"></a>Izcenojuma iestatījumi

[!include [banner](../includes/banner.md)]

Šajā dokumentā ir aprakstīti dažādie cenu noteikšanas un atlaižu pārvaldības iestatījumi galvenajā birojā Microsoft Dynamics 365 Commerce. Šie iestatījumi sniedz iespēju organizācijām noteikt cenu noteikšanas uzvedību savā Commerce risinājumā, lai apmierinātu noteiktas biznesa vajadzības.

## <a name="company-level-pricing-settings"></a>Uzņēmuma līmeņa cenu noteikšanas iestatījumi

Lielākā daļa cenu noteikšanas iestatījumu ir uzņēmuma līmenī, un tos var atrast **commerce parametru \> cenās un atlaidēs**.

### <a name="best-price-and-compound-concurrency-control-model"></a>Labākās cenas un salikšanas vienlaicīguma kontroles modelis

Labākais **cenas un saliktā vienlaicīguma** kontroles modeļa **iestatījums** **nosaka**, kā cenu noteikšanas programma apstrādā vairākas atlaides labākā cenas vai saliktās vienlaicīguma režīmā. 

Ja parametrs **prioritātes ietvaros ir iestatīts uz Labāko cenu un Salikto,** nekad nevienojot prioritātes, **visas** saliktās atlaides ar vienādu cenu noteikšanas prioritāti tiek saliktas. Saliktais rezultāts tad sacenšas **ar** jebkurām vislabākajām cenu atlaidēm, kam ir vienāda cenu noteikšanas prioritāte, tiek piemērota labākā cena, un visas atlaides, kam ir zemāka cenu noteikšanas prioritāte, tiek ignorētas.

Ja parametrs iestatīts **tikai uz labāko cenu pēc prioritātes,** vienmēr salikts starp prioritātēm, **visas** saliktās atlaides tiek apstrādātas kā **labākās cenas** atlaides. Cenu noteikšanas prioritātes ietvaros iegūst tikai viena atlaide. Ja viena atlaide ir labākā **cena** **vai** saliktā atlaide, **·** **tā** tiek salikta ar visām papildu labākās cenas vai saliktajām atlaidēm, kam ir zemāka cenu noteikšanas prioritāte.

### <a name="discount-compound-behavior"></a>Saliktas atlaides darbība

Atlaides **saliktās funkcionalitātes** iestatījums nosaka, kā cenu noteikšanas programma aprēķina vairākas saliktās atlaides.

Ja parametrs ir **iestatīts** kā Salikts, akumulatīvā veidā virs citas atlaides tiek piemērota viena atlaide. Ja sākotnējā cenā tā iestatīta **kā** Salikts, visas atlaides tiek apstrādātas neatkarīgi viena no otras un pielietotas tai pašai sākotnējai cenai.

Piemēram, jūs vēlaties salikt 10 procentu atlaidi un 20 procentu atlaidi precei, kuras sākotnējā cena ir $100. Iestatot parametra Atlaides **salikto darbību** vērtību **kā** Salikts, beigu cena tiks $72 (100 90&times;% &times; 80 USD). Iestatot to kā Salikts **uz oriģinālo cenu**, beigu cena tiks $70 (100 USD – $10 – $20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Iespējot apstākļus starp ekskluzīvu slieksni un citām periodiskām atlaidēm

Ja iespējot **konkurences starp ekskluzīvo slieksni un citiem periodiskajiem atlaižu parametriem ir iestatīts** **uz** Jā, cenu noteikšanas programma nodrošina ekskluzīvu sliekšņa atlaižu sacenojumu ar ekskluzīvām sliekšņa atlaidēm. Joprojām tiek piemērota cenu noteikšanas prioritāte. Vislabākās cenas **un saliktās** **sliekšņa** atlaides uzvedība saglabājas tāpat kā. Citiem vārdiem sakot, viņi nesacenšas ar atlaidēm, kas nav sliekšņa atlaides.

### <a name="manual-line-discount-and-system-discount"></a>Manuālā rindas atlaide un sistēmas atlaide

Manuāla **rindas atlaides un sistēmas atlaides iestatījums** nosaka, kā cenu noteikšanas programma izmanto manuālu rindas atlaidi un sistēmas atlaidi tai pašai rindai. Manuālo rindas atlaidi var salikt virs sistēmas atlaides, vai arī tā var aizstāt sistēmas atlaidi. Kad manuālā rindas atlaide un sistēmas atlaide ir salikta, aprēķina loģika ievēro Atlaides saliktās funkcionalitātes **iestatījumu**. Manuālā kopējā atlaide, kas attiecas uz visu pasūtījumu, neatbilst šis iestatījums.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Saglabāt vienumus tajā pašā pārdošanas rindā atlaides cenas noapaļošanai

Dažkārt daudzuma atlaides summas summu nevar dalīt ar kvalificēšanas daudzumu (piemēram, ja atlaides summa trīs $10 iegādātajām vienībām). Šajos gadījumos atlaides cenas noapaļošanas iestatījums Paturēt vienā pārdošanas rindā esošos krājumus nosaka to, **kā** tiek lietota cenu noteikšanas programma un tiek izplatīta atlaides summa. Ja parametrs ir iestatīts **kā** Jā, atlaides summa tiek piemērota kā visa un netiek sadalīta. Ja iestatījums ir Nē, atlaides **summa** tiek dalīta starp kvalificējamo daudzumu un noapaļota. Piemēram, trīs $10 atlaides summa tiek dalīta $3.33 vienai vienībai, $3.33 izslēgta otrajai vienībai un $3.34 trešajai vienībai.

### <a name="apply-discounts-to-key-in-price-products"></a>Piemērot atlaides atslēgai cenas precēs

Iestatījums **Lietot atlaides atslēgai cenu preces nosaka, vai atlaides var piemērot kopā ar "atslēgas** cenām", kas ir ievadītas pārdošanas punktā (POS). Atslēga **cenas iestatījumos** preces konfigurācijā nosaka, vai un kā prece atbalsta atslēgas cenu.

### <a name="apply-discounts-to-price-overrides"></a>Piemērot atlaides cenas ignorēšanas gadījumos

Iestatījums **Lietot atlaides cenu pārlabošanai** nosaka, vai atlaides var lietot kopā ar cenu ignorēšanu.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Atlaižu izplatīšana par lētākajām atlaidēm

Komplekta atlaižu, kas izmanto "lētāko" aprēķina veidu, gadījumā, ja tiek izmantots iestatījums **Sadalīt atlaides par lētākajām atlaidēm, nosaka,** vai cenu noteikšanas programma sadala atlaidi starp rindām.

Ja parametrs ir iestatīts **uz** Nē, atlaide tiek piemērota tikai lētākajām rindām. Piemēram, ja "2. iegāde" ir pieejama 1 bezmaksas komplekta atlaide, lētākais krājums būs bezmaksas, un pārējie divi krājumi paliks par pilnu cenu. Šajā gadījumā debitors, kurš atgriež gan pilnas cenas krājumus, joprojām saņem trešo krājumu bez maksas. Šī scenārija dēļ mazumtirgotājam var rasties zaudējumi.

Ja parametrs ir iestatīts **kā** Jā, cenu noteikšanas programma sadala atlaidi visās piemērojamos rindās. Šis iestatījums var palīdzēt samazināt atgriešanu zaudējumus.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Manuāli aprēķināt vairāku rindu cenas un atlaides

Manuāli **aprēķināt vairākrindu cenas un atlaides iestatījums** kontrolē, vai cenu noteikšanas programma izmanto aizkavētu cenu un atlaižu aprēķinu POS programmai un zvanu centra kanālam. **Ja** parametrs ir iestatīts uz Jā, cenu noteikšanas programma nekavējoties neaprēķina daudzrindu atlaides (piemēram, daudzuma atlaides, sliekšņa atlaides un komplekta atlaides) vienmēr, kad pārdošanas pasūtījums tiek izveidots vai rediģēts POS programmā vai zvanu centra kanālā.

> [!NOTE]
> Commerce versijā 10.0.30 **un vecākā versijā manuāli aprēķināt vairākrindu cenas un atlaides iestatījums** kontrolē tikai zvanu centra kanālu. Ja funkcionalitātes **profilā tiek manuāli aprēķināti** vairāki krājumu atlaižu iestatījumi, POS programmā tiek kontrolēta cenu aprēķina funkcionalitāte. Commerce versijā 10.0.31 abi iestatījumi tiek apvienoti viena uzņēmuma līmeņa iestatījumā.

### <a name="retention-period-in-days"></a>Saglabāšanas perioda dienu skaits

**Iestatījums** Saglabāšanas periods dienās norāda, cik dienas pēc beigu datuma (ja ir iestatīts beigu datums) vai atspējotais datums (ja beigu datums nav iestatīts) atlaide ir sistemātiski jādzēš. Ja parametrs ir iestatīts **uz 0** (nulle), automātiskā dzēšana nenotiek.

> [!NOTE]
> Commerce versijā 10.0.30 un agrākā versijā šis iestatījums tiek nosaukts kā dienu skaits, **pēc kura jādzēš termiņa beigu atlaides**.

### <a name="coupon-bar-code"></a>Kupona svītrkods

Kupona **svītrkoda iestatījums** nosaka, kurš specifisks svītrkods tiek izmantots kupona svītrkodu ģenerēšanas laikā. Lietotāji var izvēlēties vienu no iepriekš definētajiem svītrkodiem, kas ir konfigurēti svītrkodu **iestatīšanas** lapā. Papildinformāciju par svītrkodiem un svītrkodu maskām skatiet [sadaļā Svītrkodu iestatīšana](set-up-bar-codes.md) un [svītrkodu masku iestatīšana](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Atgrieztajiem darījumiem kupona kods ir jālieto manuāli

Lai **atgrieztu darbības, iestatījums Kupona kods ir** jālieto manuāli, lai atgrieztu tikai tās darbības, kurām nav paredzēta pārdošanas kvīts. Iestatiet parametru kā **Nē**, ja darbībai automātiski ir jālieto kuponu kodi. Iestatiet to kā **Jā**, ja darbībai ir manuāli jāpievieno kuponu kodi.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Izmantot organizācijai iestatītos pārdošanas līgumus

Pasūtījumiem "bizness-biznesam" (B2B), **·** **ja** organizācijas parametram iestatītie pārdošanas līgumi ir iestatīti uz Jā, cenu noteikšanas programma izmanto pārdošanas līgumus, kas organizācijai definēti lietotāja debitoru hierarhijā, lai noteiktu cenu, pamatojoties uz līgumu. Ja parametrs **ir iestatīts uz Nē** vai arī nav definēta debitoru hierarhija, cenu noteikšanas programma meklē pārdošanas līgumus, kas lietotājam definēti, lai noteiktu cenu, pamatojoties uz līgumu. Papildinformāciju par debitoru hierarhijām B2B e-komercijai [skatiet sadaļā B2B biznesa partneru pārvaldība, izmantojot debitoru hierarhijas](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Kanāla līmeņa cenu noteikšanas iestatījumi

Izmantojot tālāk norādītos iestatījumus, organizācijas var kontrolēt cenu noteikšanu noteiktos pārdošanas kanālos.

### <a name="enable-order-price-control"></a>Iespējot pasūtījuma cenu kontroli

Parametrs **Iespējot** pasūtījuma cenu kontroli atrodas **kopsavilkuma** cilnē Vispārīgi zvanu **centra konfigurācijas** lapā. Iestatījums nosaka, vai cenu noteikšanas programma ierobežo cenas ignorēšanas operāciju zvanu centra kanālā. Tas darbojas kopā ar iestatījumu **Atļaut cenu koriģēt** preces līmeni.

Ja pasūtījuma cenu kontrole ir izslēgta, jebkurš zvanu centra lietotājs var veikt cenu izmaiņas pārdošanas rindās zvanu centra kanālā neatkarīgi no tā, vai atbilstošajām precēm ir atļauta cenas korekcija.

Ja pasūtījuma cenu kontrole ir ieslēgta, tikai preces, **·** **kuru** parametrs Atļaut cenu koriģēšanu ir iestatīts uz Jā, atļaujiet cenas ignorēšanu zvanu centra kanāla pārdošanas pasūtījumos, un atbilstošajās pārdošanas rindās ir jānorāda pamatojuma kods. Zvanu centra lietotājs var **mainīt** **pārdošanas cenu tikai līdz izmaksu uzcenojuma procentuālajai vērtībai, kas ir noteikta mazumtirdzniecības un Commerce \> Channel iestatīšanas \> zvanu centra iestatījuma \> ignorēšanas atļaujās.** Ja cenas ignorēšana pārsniedz šo procentuālo vērtību, lietotājam ir jāiesniedz pieprasījums, kas pēc tam tiek apstrādāts, izmantojot iepriekš definētu Commerce darbplūsmu pārskatīšanai un apstiprināšanai. Papildinformāciju par Commerce darbplūsmām skatiet darbplūsmas [sistēmas pārskatā](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Preču līmeņa cenu noteikšanas iestatījumi

Šie iestatījumi ievieš cenu noteikšanas noteikumus preču līmenī un var tikt atrasti organizācijas preces **konfigurācijas** lapā.

### <a name="allow-price-adjust"></a>Atļaut cenas korekciju

Ja parametrs **Atļaut** cenu koriģēšanu ir **iestatīts** uz Jā, zvanu centra kanāla pārdošanas pasūtījumos precei var tikt piemērota cenas ignorēšana.

### <a name="key-in-price"></a>Ievadīt cenu

Atslēga **cenu iestatījumos** nosaka, vai atslēgas cena ir obligāta, kad prece tiek pievienota PĀRDOŠANAS transakcijai POS. Tas arī definē atbilstošus cenu vērtību ierobežojumus.

### <a name="zero-price-valid"></a>Nulles cena ir derīga

Nulles **cenas** derīgs iestatījums nosaka, vai iepriekš definētas, sistēmas aprēķinātas vai manuāli koriģētas preces pārdošanas cenas var būt 0 (nulle). Ja ir atļauta nulles **cena**, iestatiet parametru kā Jā. Šo iestatījumu var arī norādīt kategoriju līmenī no Commerce preču hierarhijas.

### <a name="prevent-all-discounts"></a>Neatļaut nekādas atlaides

Iestatot parametru **Neļaut visas atlaides** vērtību **uz Jā**, jūs neļausiet precei piemērot visus atlaižu tipus (tostarp manuālās atlaides). Šo iestatījumu var arī norādīt kategoriju līmenī no Commerce preču hierarhijas.

> [!NOTE]
> Šis iestatījums neierobežo cenas ignorēšanas operāciju, jo šī operācija iestata cenu un nav apstrādāta kā atlaide.

### <a name="prevent-manual-discounts"></a>Neatļaut manuālas atlaides

Iestatot parametru **Novērst manuālās atlaides** uz **Jā**, tiek novērsta manuāla rindas vai darbības atlaižu pielietošana precei. Pārējās atlaides joprojām var lietot. Šo iestatījumu var arī norādīt kategoriju līmenī no Commerce preču hierarhijas.

> [!NOTE]
> Šis iestatījums neierobežo cenas ignorēšanas operāciju, jo šī operācija iestata cenu un nav apstrādāta kā atlaide.

### <a name="prevent-retail-discounts"></a>Novērst mazumtirdzniecības atlaides

Ja parametrs **Novērst mazumtirdzniecības atlaides ir iestatīts** **uz** Jā, **·** **precei** nevar piemērot vienkāršas, **daudzuma**, sliekšņa, **·** **komplekta** un nosūtīšanas atlaides. Pārējās atlaides (ieskaitot manuālās atlaides) joprojām var tikt piemērotas.

### <a name="prevent-tender-based-discounts"></a>Novērst uz norēķiniem balstītas atlaides

Ja parametrs **Novērst no norēķinu atkarīgas** atlaides **ir** iestatīts uz Jā, **precei** nevar piemērot uz norēķinu balstītu atlaidi. Pārējās atlaides (ieskaitot manuālās atlaides) joprojām var tikt piemērotas.

Mazumtirgotāji bieži izvēlas izslēgt dažas preces, piemēram, jaunas preces vai pieprasījuma preces, no preču atlaidēm (piemēram, vienkāršām atlaidēm un daudzuma atlaidēm). Tomēr, iespējams, viņi vēl aizvien vēlēsieties piemērot uz norēķiniem balstītas atlaides, ja debitors maksā, izmantojot vēlamos norēķinus. Lai sasniegtu šo rezultātu, **mazumtirgotāji var iestatīt parametrus Novērst visas atlaides un Novērst no norēķinu atkarīgas** **·** **atlaides** uz Nē **un** **parametrus Novērst mazumtirdzniecības atlaides un Neatļaut manuālas** **atlaides uz Jā.**

## <a name="deprecated-or-removed-settings"></a>Novecojuši vai noņemti iestatījumi

Tālāk minētajiem cenu noteikšanas iestatījumiem ir noņemta vai ieplānota noņemšana no programmas Dynamics 365 Commerce.

| Iestatījums | Nolietojuma vai noņemšanas pamatojums | Nolietojuma vai noņemšanas statuss |
|---------|-----------------------------------|-------------------------------|
| Atlaižu pārklāšanās apstrāde | Mēs nodājām šo iestatījumu Commerce parametros, lai kontrolētu to, kā meklē cenu noteikšanas programma, un nosaka vislabāko piemēroto atlaižu kombināciju. Labākais **atlaides opcija** liek izmantot visas iespējamās atlaižu kombinācijas cenu aprēķināšanas laikā. Labākā **veiktspējas** opcija ir optimizēta opcija, kas izmanto heiristisku algoritmu un robežvērtīgās vērtības rangu metodi, lai laikus noteiktu prioritātes, novērtēt un noteikt labāko kombināciju. Līdzsvarotā **aprēķina** opcija koda bāzē darbojas tāpat kā labākā **veiktspēja**. Tādēļ tā pamatā ir dublēta opcija. Lai palīdzētu uzlabot veiktspēju, cenu noteikšanas programma ir atjaunināta tā, lai tā kā standarta opcija **izmanto** tikai labāko veiktspēju. Tādēļ šis iestatījums vairs nav piemērojams. | Novecojis 10.0.21 versijā un tiks noņemts 2022. gada oktobris. |
| Atļaut cenu korekcijas, lai palielinātu preču cenu | Mēs nodrošināti šo iestatījumu, lai kontrolētu, vai cenu pielāgošanas funkcija var palielināt preču cenas. Ja parametrs ir izslēgts, organizācijas var izmantot cenu korekcijas funkciju tikai preces vienības cenas iestatīšanai, lai tā būtu zemāka nekā pamata cena un tirdzniecības līguma pārdošanas cena. Šo iestatījumu novecojuši, jo cenu korekcijas funkcija ir atjaunināta, lai tā atbalsta lodziņā divvirzienu korekcijas (palielināšanos vai samazināšanos). | Novecojis 10.0.30 versijā un tiks noņemts 2023. gada oktobris. |
| Iespējot mazumtirdzniecības veikala cenu pārskatu | Mēs nodājām šo iestatījumu, **lai** kontrolētu, vai cenu pārskata funkcija ir pieejama veikala konfigurācijas lapā. Šis iestatījums ir novecojis, jo veikala konfigurācijas lapa ir **atjaunināta, lai tā vienmēr nodrošinātu cenu pārskatu** kā standarta funkciju. | Novecojis 10.0.31 versijā un tiks noņemts 2023. gada oktobris. |
| Lietot šodienas datumu, lai aprēķinātu cenas | Cenu Dynamics 365 Supply Chain Management noteikšanas programma atbalsta cenu noteikšanu, kas ir balstīta uz pieprasīto nosūtīšanas datumu vai pieprasīto saņemšanas datumu kopā ar šodienas datumu. Commerce cenu noteikšanas programma atbalsta tikai cenu aprēķinu, kas ir balstīts uz šodienas datumu. Debitoriem, kuri izmanto piegādes ķēžu pārvaldības un komercijas iespējas, mēs sniedzām šo iestatījumu un ieteicam klientiem vienmēr to **iestatīt** uz Jā, lai abas cenu noteikšanas programmas varētu strādāt kopā. Novecojuši šie iestatījumi, jo tie būtiski nemaina aprēķina darbību un tādēļ ir lieki. | Novecojis 10.0.31 versijā un tiks noņemts 2023. gada oktobris. |
| Maksimālā cena | Šo iestatījumu esam norādījis funkcionalitātes profilā, lai kontrolētu, vai tikai preces, kuru pārdošanas cena ir zemāka par norādīto maksimālo cenu, var pārdot caur POS konkrētos veikalos. Mēs novecojuši šis iestatījums, jo līdzekļa lietošana ir zema. | Novecojis 10.0.31 versijā un tiks noņemts 2023. gada oktobris. |
| Piemērot atlaides vienības cenai | Šis iestatījums bija paredzēts, lai kontrolētu, vai cenas un atlaides cenu aprēķināšanas laikā tiek noapaļotas vienības cenas līmenī vai pārdošanas rindas līmenī. Mēs to novecojuši, jo tie netiek patērēti nekur pašreizējā kodu bāzē. | Novecojis 10.0.31 versijā un tiks noņemts 2023. gada oktobris. |
| Manuāli aprēķināt vairāku krājumu atlaides | Mēs no nodrošināti šo iestatījumu, lai kontrolētu, vai cenu noteikšanas programma izmanto aizkavētu cenu aprēķinu mazumtirdzniecības veikala kanālam. **Ja** parametrs ir iestatīts uz Jā, cenu noteikšanas programma nekavējoties neaprēķina daudzrindu atlaides (piemēram, daudzuma atlaides, sliekšņa atlaides un komplekta atlaides) vienmēr, kad pārdošanas pasūtījums tiek izveidots vai rediģēts POS programmā. Mēs nolēmām konsolidēt šo iestatījumu ar līdzīgu iestatījumu Commerce parametros, lai izveidotu parametrļa kontroli. | Novecojis 10.0.31 versijā un tiks noņemts 2023. gada oktobris. |

Pilnu noņemto vai novecojušu līdzekļu sarakstu Dynamics 365 Commerce [skatiet sadaļā Noņemtie vai novecojušie līdzekļi Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
