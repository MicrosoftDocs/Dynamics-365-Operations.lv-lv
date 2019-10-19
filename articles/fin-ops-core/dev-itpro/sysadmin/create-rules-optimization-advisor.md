---
title: Kārtulu izveide optimizācijas padomniekam
description: Šajā tēmā ir aprakstīts, kā pievienot jaunas kārtulas darbvietai Optimizācijas padomnieks.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180994"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="6e219-103">Kārtulu izveide optimizācijas padomniekam</span><span class="sxs-lookup"><span data-stu-id="6e219-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e219-104">Šajā tēmā ir izskaidrots, kā izveidot jaunas kārtulas darbvietai **Optimizācijas padomnieks**.</span><span class="sxs-lookup"><span data-stu-id="6e219-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="6e219-105">Piemēram, varat izveidot jaunu kārtulu, kas nosaka, kuriem piedāvājuma pieprasījuma (PP) gadījumiem ir tukšs nosaukums.</span><span class="sxs-lookup"><span data-stu-id="6e219-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="6e219-106">Gadījumiem izmantojot nosaukumus, tie ir viegli identificējami un meklējami.</span><span class="sxs-lookup"><span data-stu-id="6e219-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="6e219-107">Šajā piemērā vienkāršoti parādīts, ko var panākt, izmantojot optimizācijas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="6e219-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="6e219-108">*Kārtula* ir atzīme programmas datos.</span><span class="sxs-lookup"><span data-stu-id="6e219-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="6e219-109">Ja tiek izpildīts nosacījums, ko novērtē kārtula, tiek izveidotas iespējas optimizēt procesus vai uzlabot datus.</span><span class="sxs-lookup"><span data-stu-id="6e219-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="6e219-110">Šīs iespējas var izmantot, un papildus var mērīt veikto darbību ietekmi.</span><span class="sxs-lookup"><span data-stu-id="6e219-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="6e219-111">Lai izveidotu jaunu darbvietas **Optimizācijas padomnieks** kārtulu, pievienojiet jaunu klasi, kas paplašina abstrakto klasi **SelfHealingRule**, ievieš interfeisu **IDiagnosticsRule** un kurai ir piešķirts atribūts **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="6e219-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="6e219-112">Šai klasei ir arī jābūt metodei, kam piešķirts atribūts **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="6e219-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="6e219-113">Parasti tiek izmantota metode **opportunityTitle**, ko aplūkosim vēlāk.</span><span class="sxs-lookup"><span data-stu-id="6e219-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="6e219-114">Šo jauno klasi var pievienot pielāgotam modelim, kam ir atkarība no modeļa **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="6e219-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="6e219-115">Tālāk sniegtajā piemērā ieviesto kārtulu dēvē par **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="6e219-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="6e219-116">Abstraktajai klasei **SelfHealingRule** ir abstraktas metodes, kas ir jāievieš pārmantošanas klasēs.</span><span class="sxs-lookup"><span data-stu-id="6e219-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="6e219-117">Pamats ir metode **Novērtēt**, kas atgriež kārtulas identificēto iespēju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="6e219-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="6e219-118">Iespējas var attiekties uz katru juridisko personu vai arī visu sistēmu.</span><span class="sxs-lookup"><span data-stu-id="6e219-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="6e219-119">Iepriekš parādītā metode caurskata uzņēmumus un atlasa PP gadījumus ar tukšiem nosaukumiem metodē **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="6e219-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="6e219-120">Ja tiek atrasts vismaz viens šāds gadījums, tiek izveidota uzņēmuma iespēja ar metodi **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="6e219-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="6e219-121">Ņemiet vērā, ka tabulas **SelfHealingOpportunity** lauka **Dati** tips ir **Konteiners**, tādējādi tas var ietvert visus datus, kas attiecas uz šīs kārtulas loģiku.</span><span class="sxs-lookup"><span data-stu-id="6e219-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="6e219-122">Parametram **OpportunityDate** iestatot pašreizējo laikspiedolu, tiek reģistrēts pēdējā iespējas novērtējuma laiks.</span><span class="sxs-lookup"><span data-stu-id="6e219-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="6e219-123">Iespējas var tikt izveidotas arī kā starpuzņēmumu iespējas.</span><span class="sxs-lookup"><span data-stu-id="6e219-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="6e219-124">Šajā gadījumā uzņēmumu caurskatīšana nav nepieciešama, un iespēja ir jāizveido, izmantojot metodi **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="6e219-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="6e219-125">Tālāk norādītajā kodā ir redzama metode **findRFQCasesWithEmptyTitle**, kas atgriež to PP gadījumu ID, kam ir tukšs nosaukums.</span><span class="sxs-lookup"><span data-stu-id="6e219-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="6e219-126">Vēl divas metodes, kas jāievieš, ir **opportunityTitle** un **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="6e219-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="6e219-127">Pirmā no tām atgriež īsu iespējas nosaukumu, savukārt otrā atgriež detalizētu iespējas aprakstu, kas var ietvert arī datus.</span><span class="sxs-lookup"><span data-stu-id="6e219-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="6e219-128">Metodes **opportunityTitle** atgrieztais nosaukums tiek parādīts darbvietas **Optimizācijas padomnieks** kolonnā **Optimizācijas iespēja**.</span><span class="sxs-lookup"><span data-stu-id="6e219-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="6e219-129">Tas ir redzams arī kā galvene sānu rūtī, kurā parādīta papildinformācija par iespēju.</span><span class="sxs-lookup"><span data-stu-id="6e219-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="6e219-130">Parasti šai metodei tiek piešķirts atribūts **DiagnosticRuleSubscription**, kas izmanto tālāk norādītos argumentus.</span><span class="sxs-lookup"><span data-stu-id="6e219-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="6e219-131">**Diagnostikas apgabals** — tipa **DiagnosticArea** uzskaitījums, kas norāda, kuram lietojumprogrammas apgabalam pieder kārtula, piemēram, **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="6e219-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="6e219-132">**Kārtulas nosaukums** — virkne ar kārtulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6e219-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="6e219-133">Tas tiks parādīts formas **Diagnostikas apstiprināšanas kārtula** kolonnā **Kārtulas nosaukums** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="6e219-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="6e219-134">**Izpildes biežums** — tipa **DiagnosticRunFrequency** uzskaitījums, kas norāda, cik bieži ir jāpalaiž kārtula, piemēram, **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="6e219-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="6e219-135">**Kārtulas apraksts** — virkne, kas sniedz detalizētāku kārtulas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6e219-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="6e219-136">Tas tiks parādīts formas **Diagnostikas apstiprināšanas kārtula** kolonnā **Kārtulas apraksts** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="6e219-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="6e219-137">Atribūts **DiagnosticRuleSubscription** nepieciešams, lai kārtula darbotos.</span><span class="sxs-lookup"><span data-stu-id="6e219-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="6e219-138">Parasti tas tiek izmantots metodei **opportunityTitle**, taču to var piešķirt jebkurai klases metodei.</span><span class="sxs-lookup"><span data-stu-id="6e219-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="6e219-139">Tālāk sniegts piemērs ar ieviešanu.</span><span class="sxs-lookup"><span data-stu-id="6e219-139">The following is an example implementation.</span></span> <span data-ttu-id="6e219-140">Vienkāršībai izmantotas neapstrādātas virknes, taču pareizai ieviešanai ir nepieciešamas etiķetes.</span><span class="sxs-lookup"><span data-stu-id="6e219-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="6e219-141">Metodes **opportunityDetails** atgrieztais apraksts ir redzams sānu rūtī, kurā parādīta papildinformācija par iespēju.</span><span class="sxs-lookup"><span data-stu-id="6e219-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="6e219-142">Tam nepieciešams arguments **SelfHealingOpportunity**, kas ir lauks **Dati**, ko var izmantot papildinformācijas sniegšanai par iespēju.</span><span class="sxs-lookup"><span data-stu-id="6e219-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="6e219-143">Piemērā metode atgriež to PP gadījumu ID, kam ir tukšs nosaukums.</span><span class="sxs-lookup"><span data-stu-id="6e219-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="6e219-144">Divas atlikušās abstraktās metodes, kas jāievieš, ir **provideHealingAction** un **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="6e219-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="6e219-145">**provideHealingAction** atgriež vērtību True, ja ir nodrošināta atjaunošanas darbība, pretējā gadījumā tiek atgriezta vērtība False.</span><span class="sxs-lookup"><span data-stu-id="6e219-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="6e219-146">Ja tiek atgriezta vērtība True, ir jāievieš metode **performAction**, jo pretējā gadījumā tiks parādīta kļūda.</span><span class="sxs-lookup"><span data-stu-id="6e219-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="6e219-147">Metode **performAction** izmanto argumentu **SelfHealingOpportunity**, kurā datus var izmantot darbībai.</span><span class="sxs-lookup"><span data-stu-id="6e219-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="6e219-148">Piemērā darbība manuālai korekcijai atver **PurchRFQCaseTableListPage**.</span><span class="sxs-lookup"><span data-stu-id="6e219-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="6e219-149">Atkarībā no kārtulas specifikas, iespējams, var veikt automātisku darbību, izmantojot iespējas datus.</span><span class="sxs-lookup"><span data-stu-id="6e219-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="6e219-150">Šajā piemērā sistēma varēja automātiski ģenerēt nosaukumus PP gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="6e219-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="6e219-151">Metode **securityMenuItem** atgriež darbību izvēlnes vienuma nosaukumu tā, lai kārtula būtu redzama tikai tiem lietotājiem, kuri var piekļūt darbību izvēlnes vienumam.</span><span class="sxs-lookup"><span data-stu-id="6e219-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="6e219-152">Drošības apsvērumu dēļ noteiktas kārtulas un iespējas var būt noteiktas kā pieejamas tikai autorizētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="6e219-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="6e219-153">Piemērā iespēju var skatīt tikai lietotāji, kuri var piekļūt vienumam **PurchRFQCaseTitleAction**.</span><span class="sxs-lookup"><span data-stu-id="6e219-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="6e219-154">Ņemiet vērā, ka šis darbību izvēlnes vienums tika izveidots šim piemēram un tika pievienots kā ieejas punkts **PurchRFQCaseTableMaintain** drošības privilēģijai.</span><span class="sxs-lookup"><span data-stu-id="6e219-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="6e219-155">Drošības apsvērumu dēļ, lai izvēlnes vienums dabotos pareizi, tam ir jābūt darbības izvēlnes vienumam.</span><span class="sxs-lookup"><span data-stu-id="6e219-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="6e219-156">Citi izvēlnes vienumu tipi, piemēram, **Displeja izvēlnes vienumi**, nedarbosies pareizi.</span><span class="sxs-lookup"><span data-stu-id="6e219-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="6e219-157">Kad kārtula ir kompilēta, izpildiet tālāk norādīto darbu, lai tā tiktu parādīta lietotāja interfeisā (UI).</span><span class="sxs-lookup"><span data-stu-id="6e219-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="6e219-158">Kārtula tiks parādīta formā **Diagnostikas apstiprināšanas kārtula**, kas pieejama, atverot sadaļas **Sistēmas administrēšana** > **Periodiskie uzdevumi** > **Uzturēt diagnostikas apstiprināšanas kārtulu**.</span><span class="sxs-lookup"><span data-stu-id="6e219-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="6e219-159">Lai tā tiktu novērtēta, atveriet sadaļas **Sistēmas administrēšana** > **Periodiskie uzdevumi** > **Ieplānot diagnostikas apstiprināšanas kārtulu** un atlasiet kārtulas biežumu, piemēram, **Katru dienu**.</span><span class="sxs-lookup"><span data-stu-id="6e219-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="6e219-160">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6e219-160">Click **OK**.</span></span> <span data-ttu-id="6e219-161">Lai skatītu jauno iespēju, atveriet sadaļas **Sistēmas administrēšana** > **Optimizācijas padomnieks**.</span><span class="sxs-lookup"><span data-stu-id="6e219-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="6e219-162">Tālāk esošais piemērs ir koda fragments ar kārtulas karkasu, tostarp visām nepieciešamajām metodēm un atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="6e219-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="6e219-163">Tas palīdz jums sākt rakstīt jaunas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="6e219-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="6e219-164"> Piemēra ietvaros izmantotās etiķetes un darbību izvēlnes vienumi ir izmantoti tikai demonstrācijas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="6e219-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="6e219-165">Lai iegūtu papildinformāciju, skatiet īso YouTube video: [Optimizācijas padomnieks programmā Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="6e219-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
