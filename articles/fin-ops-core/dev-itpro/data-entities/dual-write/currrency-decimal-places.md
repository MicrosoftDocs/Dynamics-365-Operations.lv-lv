---
title: Valūtas datu tipa migrācija duālajai rakstīšanai
description: Šajā tēmā aprakstīts, kā mainīt decimāldaļu skaitu, ko duālā rakstīšana atbalsta valūtai.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: c4f663ae36f7d4ea3db9888e618f2fe3bf8c3256
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748951"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="cf9ca-103">Valūtas datu tipa migrācija duālajai rakstīšanai</span><span class="sxs-lookup"><span data-stu-id="cf9ca-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cf9ca-104">Varat palielināt decimāldaļu skaitu, kas tiek atbalstītas ne vairāk kā 10 valūtas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="cf9ca-105">Noklusējuma ierobežojums ir četras decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-105">The default limit is four decimal places.</span></span> <span data-ttu-id="cf9ca-106">Palielinot decimāldaļu skaitu, jūs palīdzēsiet novērst datu zudumu, kad izmantojat duālo rakstīšanu, lai sinhronizētu datus.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="cf9ca-107">Decimāldaļu skaita pieaugums ir izvēles izmaiņa.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="cf9ca-108">Lai to īstenotu, jums ir jāpieprasa palīdzība no Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="cf9ca-109">Decimāldaļu skaita maiņas procesam ir divi soļi:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="cf9ca-110">Pieprasīt migrāciju no Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="cf9ca-111">Mainīt decimāldaļu skaitu Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="cf9ca-112">Finance and Operations programmai un Dataverse ir jāatbalsta tas pats decimāldaļu skaits valūtas vērtībās.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="cf9ca-113">Pretējā gadījumā datu zudums var rasties gadījumā, kad šī informācija tiek sinhronizēta starp programmām.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="cf9ca-114">Migrācijas process pārkonfigurē valūtas un maiņas kursa vērtību saglabāšanas veidu, bet nemaina nekādus datus.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="cf9ca-115">Kad migrācija ir pabeigta, valūtas kodu un izcenojumu decimāldaļu skaits var tikt palielināts, un datiem, ko lietotāji ievada un skata, var būt vairāk decimāldaļas precizitātes.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="cf9ca-116">Migrācija nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-116">Migration is optional.</span></span> <span data-ttu-id="cf9ca-117">Ja jums varētu būt noderīgs atbalsts vairāk decimāldaļām, mēs iesakām jums apsvērt migrāciju.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="cf9ca-118">Organizācijas, kurām nav nepieciešamas vērtības, kurām ir vairāk nekā četras decimāldaļas, nav jāmigrē.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="cf9ca-119">Migrācijas pieprasīšana no Microsoft</span><span class="sxs-lookup"><span data-stu-id="cf9ca-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="cf9ca-120">Esošo valūtas lauku glabāšana programmā Dataverse nevar atbalstīt vairāk par četrām decimāldaļām.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="cf9ca-121">Tāpēc migrācijas procesa laikā valūtas vērtības tiek pārkopētas uz jaunajiem iekšējiem laukiem datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="cf9ca-122">Šis process notiek nepārtraukti, līdz visi dati ir migrēti.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="cf9ca-123">Iekšēji migrācijas beigās jaunie glabāšanas tipi aizvieto vecos glabāšanas tipus, bet datu vērtības netiek mainītas.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="cf9ca-124">Valūtas lauki var atbalstīt līdz 10 decimāldaļām.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="cf9ca-125">Migrācijas procesa laikā Dataverse var turpināt tikt izmantots bez pārtraukumiem.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="cf9ca-126">Tajā pašā laikā valūtas maiņas kursi tiek modificēti tā, lai tie atbalstītu līdz 12 decimāldaļām pašreizējo 10 vietā.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="cf9ca-127">Šī izmaiņa ir nepieciešama, lai abās programmās ir vienāds decimāldaļu skaits gan Finance and Operations programmā, gan Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="cf9ca-128">Migrācija nemaina nekādus datus.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-128">Migration doesn't change any data.</span></span> <span data-ttu-id="cf9ca-129">Kad valūtas un maiņas kursu lauki ir pārveidoti, administratori var konfigurēt sistēmu, lai izmantotu līdz 10 decimāldaļām valūtas laukiem, norādot katras darījuma valūtas un cenu decimāldaļu skaitu.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="cf9ca-130">Pieprasīt migrāciju</span><span class="sxs-lookup"><span data-stu-id="cf9ca-130">Request a migration</span></span>

<span data-ttu-id="cf9ca-131">Lai padarītu šo līdzekli pieejamu, nosūtiet ziņojumu uz e-pastu **CDSExpandDecimal@microsoft.com** un iekļaujiet sekojošo informāciju:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="cf9ca-132">**Tēma:** pieprasīt iespējot paplašinātu decimālo atbalstu \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="cf9ca-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="cf9ca-133">**Pamatteksts:** es vēlos iespējot izvērstu decimālo atbalstu manai organizācijai \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="cf9ca-134">Microsoft pārstāvis sazināsies ar jums divu vai trīs darbdienu laikā, lai izklāstītu nākamos soļus.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="cf9ca-135">Kad jūs pieprasāt migrāciju, jums ir jāapzinās šādas detaļas un tās atbilstoši jāplāno:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="cf9ca-136">Laiks, kas nepieciešams, lai migrētu datus, ir atkarīgs no datu apjoma sistēmā.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="cf9ca-137">Lielu datu bāzu migrācija var ilgt vairākas dienas.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="cf9ca-138">Datu bāzes lielums īslaicīgi palielinās, kamēr notiek migrācija, jo indeksiem ir nepieciešama papildu vieta.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="cf9ca-139">Lielākā daļa papildu vietas tiek atbrīvotas, kad migrācija ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="cf9ca-140">Migrācijas procesa laikā, ja rodas kļūdas, kas novērš migrācijas pabeigšanu, sistēma veido brīdinājumus Microsoft atbalstam, lai atbalsta personāls varētu iejaukties.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="cf9ca-141">Tomēr pat, ja migrācijas laikā rodas kļūdas, Dataverse ir pilnībā pieejams regulārai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="cf9ca-142">Migrācijas process nav atgriezenisks.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="cf9ca-143">Decimāldaļu skaita mainīšana</span><span class="sxs-lookup"><span data-stu-id="cf9ca-143">Changing the number of decimal places</span></span>

<span data-ttu-id="cf9ca-144">Pēc migrācijas pabeigšanas Dataverse var saglabāt skaitļus, kuriem ir vairāk decimāldaļu.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="cf9ca-145">Administratori var izvēlēties, cik decimāldaļu tiek izmantotas noteiktiem valūtas kodiem un cenu noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="cf9ca-146">Microsoft Power Apps, Power BI un Power Automate lietotāji pēc tam var skatīt un izmantot skaitļus, kuriem ir vairāk decimāldaļu.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="cf9ca-147">Lai veiktu šīs izmaiņas, ir jāatjaunina šādi iestatījumi programmā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="cf9ca-148">**Sistēmas iestatījumi: valūtas precizitāte cenu noteikšanai** — lauks **Iestatīt valūtas precizitāti, kas tiek izmantota cenu noteikšanai visā sistēmā** nosaka, kā valūta mainīsies organizācijā, atlasot **Cenu noteikšanas precizitāti**.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="cf9ca-149">**Biznesa pārvaldība: valūtas** – lauks **Valūtas precizitāte** ļauj norādīt pielāgotu decimāldaļu skaitu noteiktai valūtai.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="cf9ca-150">Ir pieejama alternatīva organizācijas mēroga iestatījumam.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="cf9ca-151">Ir daži ierobežojumi:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-151">There are some limitations:</span></span>

+ <span data-ttu-id="cf9ca-152">Nevar konfigurēt elementa valūtas lauku tabulā.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="cf9ca-153">Varat norādīt vairāk nekā četras decimāldaļas tikai **Cenu noteikšanai** un **Darījuma valūtas** līmeņos.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="cf9ca-154">Sistēmas iestatījumi: cenu valūtas precizitāte</span><span class="sxs-lookup"><span data-stu-id="cf9ca-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="cf9ca-155">Pēc migrācijas pabeigšanas administratori var iestatīt valūtas precizitāti.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="cf9ca-156">Dodieties uz **Iestatījumi \> Administrēšana** un atlasiet **Sistēmas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="cf9ca-157">Pēc tam cilnē **Vispārīgi** mainiet lauka **Iestatīt valūtas precizitāti, kas ir izmantota cenu noteikšanā visā sistēmā** vērtību, kā parādīts sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Valūtas sistēmas iestatījumi](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="cf9ca-159">Biznesa pārvaldība: Valūtas</span><span class="sxs-lookup"><span data-stu-id="cf9ca-159">Business Management: Currencies</span></span>

<span data-ttu-id="cf9ca-160">Ja vēlaties, lai konkrētas valūtas precizitātes atšķirtos no valūtas precizitātes, kas tiek izmantota cenu noteikšanai, varat mainīt to.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="cf9ca-161">Dodieties uz **Iestatījumi \> Biznesa pārvaldība**, atlasiet **Valūtas** un atlasiet valūtu, ko vēlaties mainīt.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="cf9ca-162">Pēc tam iestatiet **Valūtas precizitātes** lauku uz vēlamo decimāldaļu skaitu, kā parādīts sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Noteiktas lokalizācijas valūtu iestatījumi](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="cf9ca-164">tabulas: valūtas lauks</span><span class="sxs-lookup"><span data-stu-id="cf9ca-164">tables: Currency column</span></span>

<span data-ttu-id="cf9ca-165">Decimāldaļu skaits, ko var konfigurēt noteiktiem valūtas laukiem, ir ierobežots līdz četriem.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]