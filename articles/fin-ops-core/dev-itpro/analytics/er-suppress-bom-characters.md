---
title: Izveidot ER konfigurācijas, lai likvidētu MK rakstzīmes ģenerētos failos
description: Šajā tēmā skaidrots, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus, kas likvidētu baita pasūtījuma zīmes (MK) rakstzīmes.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9260db2edab75c9876ddf5af99bee4ff174c64e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568977"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="549a6-103">Izveidot ER konfigurācijas, lai likvidētu MK rakstzīmes ģenerētos failos</span><span class="sxs-lookup"><span data-stu-id="549a6-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="549a6-104">Varat noformēt [elektronisko pārskatu (Electronic Reporting — ER)](general-electronic-reporting.md) [risinājumu](er-quick-start1-new-solution.md), lai ģenerētu izejošos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="549a6-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="549a6-105">Lai izveidotu dokumentus kā teksta vai XML failus, risinājumā jāietver ER [konfigurācija](general-electronic-reporting.md#Configuration), kas satur ER [formāta](general-electronic-reporting.md#FormatComponentOutbound)komponentu.</span><span class="sxs-lookup"><span data-stu-id="549a6-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="549a6-106">Lai norādītu [rakstzīmju kodēšanas veidu](https://docs.microsoft.com/windows/win32/intl/character-sets), kas apzīmē rakstzīmju kopu ģenerētos failos, ER formātam jāsatur **Kopējā\\Faila** formāta elements.</span><span class="sxs-lookup"><span data-stu-id="549a6-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="549a6-107">Lai konfigurētu ER formāta komponentu, jāatver izveidotās ER konfigurācijas [melnraksta](general-electronic-reporting.md#component-versioning) versija ER formāta noformētājā un jāpievieno **Kopējais\\Faila** elements.</span><span class="sxs-lookup"><span data-stu-id="549a6-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="549a6-108">Laukā **Kodēšana** norādiet izpildlaikā ģenerēto izejošo failu kodēšanas veidu, izmantojot šo komponentu.</span><span class="sxs-lookup"><span data-stu-id="549a6-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="549a6-109">Ja formāts ietver nepareizu kodēšanas nosaukumu, saglabājot izmaiņas formāta iestatījumos, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="549a6-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Saknes elementu pievienošana Formātu noformētāja lapā](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="549a6-111">Ja kā kodēšanas veidu norādāt **UTF-8**, **UTF-16** vai **UTF-32**, kļūst pieejama opcija **Likvidēt MK rakstzīmes**.</span><span class="sxs-lookup"><span data-stu-id="549a6-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="549a6-112">Iestatiet šo opciju kā **Jā**, lai likvidētu [baitu pasūtījuma atzīmes (MK) rakstzīmes](https://docs.microsoft.com/globalization/encoding/byte-order-mark) izejošos failos, kas tiek ģenerēti izpildlaikā,kad tiek palaists rediģējams ER formāts.</span><span class="sxs-lookup"><span data-stu-id="549a6-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="549a6-113">Ja atstājat tukšu lauku **Kodēšana**, tad tiek izmantota **UTF-8** noklusējuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="549a6-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Opcijas Likvidēt MK rakstzīmes iestatīšana lapā Formāta veidotājs](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="549a6-115">Lai pārskatītu izpildlaika funkcionalitāti, izpildiet attiecīgo procedūru.</span><span class="sxs-lookup"><span data-stu-id="549a6-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="549a6-116">Piemēram, izpildiet darbības tēmā [XML elementu XML elementu izpildes atliktā izpilde ER formātos](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="549a6-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="549a6-117">Kad esat izpildījis soļus sadaļā [Modificēt formātu, lai aprēķins būtu balstīts uz šīs tēmas ģenerēto izvades](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output)sadaļu, izpildiet šīs papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="549a6-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="549a6-118">Norādiet UTF kodējumu:</span><span class="sxs-lookup"><span data-stu-id="549a6-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="549a6-119">Atlasiet **Pārskata** elementu **Kopējā\\Faila** tipā.</span><span class="sxs-lookup"><span data-stu-id="549a6-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="549a6-120">**Kodēšanas** laukā norādiet **UTF-8** kodēšanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="549a6-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="549a6-121">Ģenerēt XML failu, kas satur MK rakstzīmi:</span><span class="sxs-lookup"><span data-stu-id="549a6-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="549a6-122">Iestatiet opciju **Likvidēt MK rakstzīmes** uz **Nē**, lai ģenerētajos XML failos iekļautu MK rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="549a6-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="549a6-123">Izpildiet soļi kopsavilkuma [XML elementa Izpildes atliktajā maksājuma sadaļā, lai izmantotu aprēķināto kopsummu](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tēmas sadaļā [XML elementu izpildes atliktais izpilde ER formātos](er-defer-xml-element.md), un saglabājiet ģenerēto failu kā **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="549a6-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="549a6-124">Ģenerēt XML failu, kas nesatur MK rakstzīmi:</span><span class="sxs-lookup"><span data-stu-id="549a6-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="549a6-125">Iestatiet opciju **Likvidēt MK rakstzīmes** uz **Jā**, lai likvidētu MK rakstzīmes ģenerētajos XML failos.</span><span class="sxs-lookup"><span data-stu-id="549a6-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="549a6-126">Izpildiet soļi kopsavilkuma [XML elementa Izpildes atliktajā maksājuma sadaļā, lai izmantotu aprēķināto kopsummu](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tēmas sadaļā [XML elementu izpildes atliktais izpilde ER formātos](er-defer-xml-element.md), un saglabājiet ģenerēto failu kā **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="549a6-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="549a6-127">Salīdziniet ģenerētos failus failu salīdzinājuma utilītā.</span><span class="sxs-lookup"><span data-stu-id="549a6-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="549a6-128">Pirmā atšķirība, ko pamanīsit, ir faila galvenē.</span><span class="sxs-lookup"><span data-stu-id="549a6-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="549a6-129">Failā SampleXmlReport.xml ir MK rakstzīme, kurā nav SampleXmlReport (1).xml faila.</span><span class="sxs-lookup"><span data-stu-id="549a6-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Salīdziniet ģenerētos failus failu salīdzinājuma utilītā](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="549a6-131">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="549a6-131">See also</span></span>

- [<span data-ttu-id="549a6-132">XML elementu izpildes atlikšana elektronisko pārskatu formātos</span><span class="sxs-lookup"><span data-stu-id="549a6-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]