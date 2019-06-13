<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="lv-LV">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Šajā tēmā ir aprakstīta Microsoft Dynamics 365 for Retail izmaksu konfigurācijas sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Organizācijām ieteicams izmantot vairākus izmaksu komponentus, lai noteiktu optimālu pasūtījuma izpildes vietu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Daži no šiem izmaksu komponentiem ir piegādes izmaksas, apstrādes izmaksas un iepakojuma izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Šo izmaksu kombinācija tiek aprēķināta tādēļ, lai noteiktu izpildes vietu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kad Microsoft Dynamics 365 for Retail pirmā sadalīto pasūtījumu pārvaldības (DOM) iterācija optimizē izpildes vietām piešķirtos pasūtījumus, tiek ņemts vērā tikai attālums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai gan attālums var tikt saistīts ar izmaksām, tas nav tas pats, kas izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Piemēram, vienā attālumā piegādes pa nakti izmaksas ir lielākas nekā piegādes trīs vai septiņu dienu laikā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmantojot izmaksu konfigurācijas funkciju, mazumtirgotāji var definēt un konfigurēt papildu izmaksu komponentus, kas tiks aprēķināti un ņemti vērā, nosakot optimālo vietu pasūtījumu rindu izpildei.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kad izmaksu komponenti ir konfigurēti, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs izmanto tikai šīs izmaksu definīcijas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Attāluma komponents netiek uzskatīts par izmaksām.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Tomēr, ja neviens izmaksu komponents nav konfigurēts, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs neizmanto attāluma komponentu kā izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Izmaksu komponentu iestatīšana</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sistēmā var definēt divu veidu galvenos izmaksu komponentus: <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Cits<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Abiem izmaksu komponentu veidiem tiek atbalstītas vairākas aprēķinu bāzes, kā parādīts tālāk sniegtajā tabulā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Izmaksu komponenta veids</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Aprēķina bāze</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Piegāde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Vienkāršs</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Diferencēts</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Cits</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Pārdošanas pasūtījums</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Pārdošanas rinda</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Vieta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Piegādes izmaksu komponenta veids</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> un piegādes izmaksu aprēķina bāzes kombinācijas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Vienkārša</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja tiek izmantots izmaksu komponenta veids <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> un aprēķina bāze <bpt id="p2">**</bpt>Vienkārša<ept id="p2">**</ept>, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izmaksu faktors<ept id="p1">**</ept> — ievadiet unikālu izmaksu faktora identifikatoru.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Apraksts<ept id="p1">**</ept> — ievadiet izmaksu faktora nosaukumu un aprakstu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Sākuma datums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Beigu datums<ept id="p2">**</ept> — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Aktīvs<ept id="p1">**</ept> — norāda, vai izmaksu faktors ir aktīvs.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Uzņēmums<ept id="p1">**</ept> — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Piegādes veidi<ept id="p1">**</ept> — norāda piegādes veidus, kam izmaksas tiek konfigurētas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Aprēķina veids<ept id="p1">**</ept> — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Fiksēts<ept id="p1">**</ept> — piegādes veidam tiek izmantotas fiksētās izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atlasot šo aprēķina veidu lauks <bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> tiek izmantots fiksēto izmaksu aprēķināšanai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Attāluma vienība<ept id="p1">**</ept> — piegādes veida izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā <bpt id="p2">**</bpt>Izmaksas<ept id="p2">**</ept>, reizinot attālumu starp piegādes adresi un atrašanās vietām.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku <bpt id="p2">**</bpt>Aprēķina veids<ept id="p2">**</ept>, lai aprēķinātu piegādes veida izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Sadalīta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Ja tiek izmantots izmaksu komponenta veids <bpt id="p1">**</bpt>Piegāde<ept id="p1">**</ept> un aprēķina bāze <bpt id="p2">**</bpt>Sadalīta<ept id="p2">**</ept>, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šajā kombinācijā attālums ir balstīts uz sadalītu attālumu diapazonu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Izmaksu faktors<ept id="p1">**</ept> — ievadiet unikālu izmaksu faktora identifikatoru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Apraksts<ept id="p1">**</ept> — ievadiet izmaksu faktora nosaukumu un aprakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Noklusējuma izmaksas<ept id="p1">**</ept> — norāda izmaksas, kas jāizmanto piegādes veidam tad, ja attālums starp piegādes adresi un atrašanās vietu nav nevienā no piegādes veida sadalītajiem attālumiem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Sākuma datums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Beigu datums<ept id="p2">**</ept> — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktīvs<ept id="p1">**</ept> — norāda, vai izmaksu faktors ir aktīvs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Uzņēmums<ept id="p1">**</ept> — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Piegādes veidi<ept id="p1">**</ept> — norāda piegādes veidus, kam izmaksas tiek konfigurētas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Attāluma veids<ept id="p1">**</ept> — norāda, vai sadalītais attālums jāaprēķina kā antenas attālums vai ceļa attālums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Attāluma vienības<ept id="p1">**</ept> — norāda vienību, kas jāizmanto sadalītā attāluma aprēķināšanā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Attāluma sākums<ept id="p1">**</ept> — norāda sadalītā attāluma diapazona sākumu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Attāluma beigas<ept id="p1">**</ept> — norāda sadalītā attāluma diapazona beigas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Aprēķina veids<ept id="p1">**</ept> — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas un sadalītais attālums.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fiksēts<ept id="p1">**</ept> — piegādes veidam tiek izmantotas fiksētās izmaksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Atlasot šo aprēķina veidu lauks <bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> tiek izmantots fiksēto izmaksu aprēķināšanai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Attāluma vienība<ept id="p1">**</ept> — piegādes veida un sadalītā attāluma izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā <bpt id="p2">**</bpt>Izmaksas<ept id="p2">**</ept>, reizinot attālumu starp piegādes adresi un atrašanās vietām.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku <bpt id="p2">**</bpt>Aprēķina veids<ept id="p2">**</ept>, lai aprēķinātu piegādes veida izmaksas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Definējot sadalītos attālumus, sistēma pārbauda, vai netrūkst kāda attāluma un vai nav tādu attālumu, kas pārklājas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Visiem sadalītajiem attālumiem piegādes veidam jāizmanto vienāds attāluma veids.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Cits izmaksu komponenta veids</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida <bpt id="p1">**</bpt>Cits<ept id="p1">**</ept> un cita ar piegādes izmaksām nesaistīta izmaksu veida kombinācijas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas pasūtījums</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmaksu komponenta veida <bpt id="p1">**</bpt>Cits<ept id="p1">**</ept> un cita izmaksu veida <bpt id="p2">**</bpt>Pārdošanas pasūtījums<ept id="p2">**</ept> kombinācija tiek izmantota, lai pārdošanas pasūtījuma līmenī definētu ar piegādi nesaistītas izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Izmaksu faktors<ept id="p1">**</ept> — ievadiet unikālu izmaksu faktora identifikatoru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Apraksts<ept id="p1">**</ept> — ievadiet izmaksu faktora nosaukumu un aprakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Sākuma datums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Beigu datums<ept id="p2">**</ept> — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktīvs<ept id="p1">**</ept> — norāda, vai izmaksu faktors ir aktīvs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> — pārdošanas pasūtījuma līmenī norāda ar piegādi nesaistīto izmaksu vērtību.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas rinda</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Izmaksu komponenta veida <bpt id="p1">**</bpt>Cits<ept id="p1">**</ept> un cita izmaksu veida <bpt id="p2">**</bpt>Pārdošanas rinda<ept id="p2">**</ept> kombinācija tiek izmantota, lai pārdošanas pasūtījuma rindas līmenī definētu ar piegādi nesaistītas izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Izmaksu faktors<ept id="p1">**</ept> — ievadiet unikālu izmaksu faktora identifikatoru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Apraksts<ept id="p1">**</ept> — ievadiet izmaksu faktora nosaukumu un aprakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Sākuma datums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Beigu datums<ept id="p2">**</ept> — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktīvs<ept id="p1">**</ept> — norāda, vai izmaksu faktors ir aktīvs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> — pārdošanas pasūtījuma rindas līmenī norāda ar piegādi nesaistīto izmaksu vērtību.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Vieta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Izmaksu komponenta veida <bpt id="p1">**</bpt>Cits<ept id="p1">**</ept> un cita izmaksu veida <bpt id="p2">**</bpt>Vieta<ept id="p2">**</ept> kombinācija tiek izmantota, lai atsevišķai vietai vai vietu grupai definētu ar piegādes izmaksām nesaistītas izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Izmaksu faktors<ept id="p1">**</ept> — ievadiet unikālu izmaksu faktora identifikatoru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Apraksts<ept id="p1">**</ept> — ievadiet izmaksu faktora nosaukumu un aprakstu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Sākuma datums<ept id="p1">**</ept> un <bpt id="p2">**</bpt>Beigu datums<ept id="p2">**</ept> — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktīvs<ept id="p1">**</ept> — norāda, vai izmaksu faktors ir aktīvs.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izpildes vietu grupa<ept id="p1">**</ept> — norāda vietu grupu, kurai tiek definētas ar piegādi nesaistītās izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Izpildes vieta<ept id="p1">**</ept> — norāda vietu, kurai tiek definētas ar piegādi nesaistītās izmaksas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ja aprēķina kritērijos ir iestatīta atrašanās vieta, izpildes vietu un izpildes vietu grupu nevar norādīt vienā rindā.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Izmaksas<ept id="p1">**</ept> — izpildes grupas vai izpildes vietas līmeņos norāda ar piegādi nesaistīto izmaksu vērtību.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lai DOM palaišanas laikā šīs izmaksas tiktu ņemtas vērā, izmaksu faktors ir jāpievieno attiecīgajam izpildes profilam.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>