<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Optimālās pārklāto atlaižu kombinācijas noteikšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Optimālās pārklāto atlaižu kombinācijas noteikšana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja atlaides pārklājas, ir jānosaka pārklāto atlaižu kombinācija, kas rada vismazāko transakcijas kopsummu vai lielāko kopējo atlaidi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja atlaides summa mainās atbilstoši nopirkto preču cenai, piemēram, parastās mazumtirdzniecības atlaides “pērc 1, saņem 1 X procentu atlaidi” (BOGO) gadījumā, šim procesam ir jāveic kombināciju optimizēšana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šis raksts attiecas uz programmu Microsoft Dynamics AX 2012 R3 ar KB 3105973 (2015. gada 2. novembra laidiens) vai jaunāku tās versiju un programmu Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai noteiktu kombinācijas atlaides, kas pārklājas, un tās laicīgi piemērotu, esam ieviesuši metodi, kā lietot atlaides, kas pārklājas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī metode tiek dēvēta par <bpt id="p1">**</bpt>robežvērtības ranžēšanu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Robežvērtības ranžēšana tiek izmantota, ja iespējamo pārklāto atlaižu kombināciju novērtēšanai nepieciešamais laiks pārsniedz sliekšņvērtību, ko var konfigurēt lapā <bpt id="p1">**</bpt>Mazumtirdzniecības parametri<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Robežvērtības ranžēšanas metodes ietvaros tiek aprēķināta katras pārklātās atlaides vērtība, izmantojot kopīgo preču atlaides vērtību.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pēc tam pārklātās atlaides tiek lietotas secībā no lielākās relatīvās vērtības līdz mazākajai relatīvajai vērtībai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detalizētu informāciju par jauno metodi skatiet sadaļā “Robežvērtība” šī raksta turpinājumā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Robežvērtības ranžēšana netiek lietota, ja citas transakcijā ietvertās preces neietekmē preces atlaides summas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, šī metode netiek lietota divām parastajām atlaidēm vai parastajai atlaidei un vienas preces daudzuma atlaidei.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Atlaižu piemēri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vienai preču kopai varat izveidot neierobežotu skaitu mazumtirdzniecības atlaižu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taču, tā kā nepastāv nekāds ierobežojums, mēģinot aprēķināt dažādām precēm lietojamās atlaides, var rasties veiktspējas problēmas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk sniegtajā piemērā ir detalizētāk atainota šī problēma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1. piemēra ietvaros tiek apstrādātas divas preces un divas pārklātas atlaides.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. piemērā ir atainots, kā problēma attīstās, ja tiek pievienotas papildu preces.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1. piemērs: divas preces un divas atlaides</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī piemēra ietvaros, lai varētu saņemt katru atlaidi, ir nepieciešamas divas preces, un atlaides nevar kombinēt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēra ietvaros izmantoto atlaižu veids ir <bpt id="p1">**</bpt>Labākā cena<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Abas preces ir piemērotas abām atlaidēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tālāk ir norādītas abas atlaides.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Divu labāko cenas atlaižu piemērs</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jebkurām divām precēm labākā no šīm divām atlaidēm ir atkarīga no abu preču cenas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja abu preču cenas ir vienādas vai gandrīz vienādas, 1. atlaide ir labāka.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ja vienas preces cena ir daudz mazāka par otras preces cenu, 2. atlaide ir labāka.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Lūk, matemātiskā kārtula šo divu atlaižu savstarpējai novērtēšanai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kārtula atlaižu novērtēšanai</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kad 1. preces cena ir vienāda ar divām trešdaļām no 2. preces cenas, tad abas atlaides ir vienādas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī piemēra ietvaros 1. atlaides faktiskā procentuālā vērtība mainās diapazonā no dažiem procentiem (ja abu preču cenas ļoti atšķiras) līdz 25 procentiem (ja abu preču cenas ir vienādas).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. atlaides faktiskā procentuālā vērtība ir nemainīga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tā vienmēr ir 20 procenti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tā kā 1. atlaides faktiskā procentuālā vērtība var būt lielāka vai mazāka nekā 2. atlaide, tas, labākā atlaide ir atkarīga no abu preču cenas pirms atlaides lietošanas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī piemēra ietvaros aprēķinu var veikt ātri, jo tiek lietotas tikai divas atlaides un tikai divām precēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pastāv tikai divas iespējamās kombinācijas: viens 1. atlaides lietojums vai viens 2. atlaides lietojums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nav jāaprēķina nekādas permutācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Katras atlaides vērtība tiek aprēķināta, izmantojot abas preces, un tiek lietota labākā atlaide.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. piemērs: četras preces un divas atlaides</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Turpinājumā tiek lietotas četras preces un tās pašas divas atlaides.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visas četras preces ir piemērotas abām atlaidēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pastāv divpadsmit iespējamās kombinācijas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēra beigās transakcijai tiek lietotas divas atlaides vienā no trim kombinācijām: divi 1. atlaides lietojumi, divi 2. atlaides lietojumi vai viens 1. atlaides un viens 2. atlaides lietojums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai atainotu iespējamās kombinācijas, tiek aplūkotas divas dažādas četru preču kopas ar dažādām cenām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visām četrām precēm ir viena cena $ 15,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā gadījumā labākā atlaižu kombinācija ir divi 1. atlaides lietojumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Divām precēm ir pilna cena, un divām ir 50 procentu atlaide.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transakcijas kopsumma ar atlaidi ir $ 45 (15 + 15 + 7,50 + 7,50), kas ir par $ 15 (25 procentiem) mazāka nekā kopsumma bez atlaides $ 60.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. atlaide ir tikai $ 12 (20 procenti).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Divas preces maksā $ 20 katra, viena prece maksā $ 15 un viena prece maksā $ 5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šādā gadījumā labākā atlaižu kombinācija ir viens 2. atlaides lietojums un viens 1. atlaides lietojums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk esošajās tabulās ir norādītas atlaides.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai nolasītu tabulās sniegto informāciju, izmantojiet vienu preci no rindas un vienu preci no kolonnas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Piemēram, 1. atlaides tabulā, kombinējot divas preces ar cenu $ 20, iegūstat atlaidi $ 10.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2. atlaides tabulā, kombinējot preci ar cenu $ 15 un preci ar cenu $ 5, iegūstat atlaidi $ 4.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Piemērs, kur ir izmantotas četras preces tām pašam divām atlaidēm</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Vispirms ir jānosaka vislielākā atlaide, ko var iegūt jebkurām divām precēm, lietojot jebkuru atlaidi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Divās tabulās ir norādītas atlaides summas visām divi preču kombinācijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabulu kopējās daļas atbilst gadījumiem, kad prece tiek kombinēta pati ar sevi, kas nav iespējams, vai divu preču apgrieztajai kombinēšanai, kas rada tādu pašu atlaides summu un ko var ignorēt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aplūkojot tabulas, varat konstatēt, ka 1. atlaide divām precēm ar cenu $ 20 ir lielākā atlaide, kas ir pieejama, lietojot jebkuru atlaidi visām četrām precēm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Šī atlaide pirmajā tabulā ir iezīmēta zaļā krāsā.) Tādējādi atliek tikai prece ar cenu $ 15 un prece ar cenu $ 5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vēlreiz aplūkojot abas tabulas, varat konstatēt, ka, šīm divām precēm lietojot 1. atlaidi, tiek iegūta atlaide $ 2,50, bet, tām lietojot 2. atlaidi, tiek iegūta atlaide $ 4.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tāpēc tiek izvēlēta 2. atlaide.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kopējā atlaide ir $ 14.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai atvieglotu šī piemēra vizualizēšanu, tālāk ir sniegtas divas papildu tabulas, kurās ir redzamas visu iespējamo divu preču kombināciju faktiskās atlaides procentuālās vērtības gan 1., gan 2. atlaidei.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ir ietverta tikai puse no kombināciju saraksta, jo šīm divām atlaidēm nav svarīgi, kādā secībā abām precēm tiek lietota atlaide.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Lielākā faktiskā atlaide (25 procenti) ir iezīmēta zaļā krāsā, un mazākā faktiskā atlaide (10 procenti) ir iezīmēta sarkanā krāsā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Faktiskās atlaides procentuālais daudzums visām divu preču kombinācijām abām atlaidēm</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ja cenas atšķiras un ir jāsalīdzina divas atlaides vai vairāk, vienīgais veids, kā garantēt vislabākās atlaižu kombinācijas izvēli, ir novērtēt abas atlaides un tās salīdzināt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visas iespējamās kombinācijas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šajā sadaļā tiek turpināts iepriekšējā sadaļā apskatītais piemērs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tiek pievienotas papildu preces un vēl viena atlaide un noteikts, cik daudz kombināciju ir jāaprēķina un jāsalīdzina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tālāk esošajā tabulā ir norādīts iespējamo atlaižu kombināciju skaits atbilstoši preču daudzuma palielinājumam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabulā ir atainots divu pārklātu atlaižu gadījums, kā tas ir aprakstīts iepriekšējā piemērā, fan trīs pārklātu atlaižu gadījums.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Novērtējamo iespējamo atlaižu kombināciju skaits drīz vien kļūst tik liels, ka pat ātrdarbīgs dators nespēj veikt aprēķinu un salīdzinājumu tik ātri, cik ir vajadzīgs, strādājot ar mazumtirdzniecības transakcijām.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Iespējamo atlaižu kombināciju skaits, palielinoties preču daudzumam</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ja tiek lietots vēl lielāks daudzums vai vēl vairāk pārklāto atlaižu, tad kopējais iespējamo atlaižu kombināciju skaits drīz vien sasniedz miljonus, un kombināciju novērtēšanai un vislabākās iespējamās kombinācijas izvēlei drīz vien ir vajadzīgs daudz ilgāks laiks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mazumtirdzniecības cenas noteikšanas programmā ir veiktas dažas optimizācijas, lai samazinātu novērtējamo kombināciju skaitu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taču, tā kā pārklāto atlaižu skaits un transakcijās ietvertais daudzums nav ierobežots, vienmēr, kad pastāv pārklātās atlaides, ir jānovērtē ļoti daudz kombināciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šo problēmu palīdz novērst robežvērtības ranžēšanas metode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Robežvērtības metode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lai novērstu eksponenciāli pieaugošā novērtējamo kombināciju daudzuma problēmu, ir pieejama optimizācijas metode, kas nodrošina katras atlaides vērtības aprēķināšanu katrai kopīgajai precei preču kopā, kurai var lietot divas atlaides vai vairāk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šī vērtība tiek dēvēta par kopīgo preču atlaides <bpt id="p1">**</bpt>robežvērtību<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Robežvērtība ir vidējais kopējās atlaides summas palielinājums katrai precei, lietojot kopīgajām precēm katru atlaidi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Robežvērtība tiek aprēķināta, aprēķinot kopējo atlaides summu (DTotal), atņemot atlaides summu bez kopīgajām precēm (DMinus<ph id="ph1">\\</ph> Shared) un dalot iegūto starpību ar kopīgo preču skaitu (ProductsShared).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Formula robežvērtības aprēķināšanai</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kad ir aprēķināta katras atlaides robežvērtība kopīgo preču kopā, tad kopīgajām precēm tiek lietotas visas atlaides secībā no lielākās robežvērtības līdz mazākajai robežvērtībai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šīs metodes ietvaros ikreiz pēc atsevišķas atlaides instances lietošanas netiek salīdzinātas visas atlikušās atlaižu iespējas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tā vietā tiek vienu reizi salīdzinātas pārklātās atlaides, kas pēc tam tiek lietotas noteiktajā secībā.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Netiek veikta papildu salīdzināšana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sliekšņvērtību programmatūras pārslēgšanai uz robežvērtības metodi varat konfigurēt lapas <bpt id="p2">**</bpt>Mazumtirdzniecības parametri<ept id="p2">**</ept> cilnē <bpt id="p1">**</bpt>Atlaide<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pieņemamais kopējās atlaides parēķina laiks atšķirtas dažādās mazumtirdzniecības nozarēs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taču parasti šis laiks ir no dažiem desmitiem milisekunžu līdz vienai sekundei.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>