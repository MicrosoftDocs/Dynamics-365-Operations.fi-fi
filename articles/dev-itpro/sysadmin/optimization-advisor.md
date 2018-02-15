---
title: "Optimointityökalun sääntöjen luominen"
description: "Tässä ohjeaiheessa käsitellään uusien sääntöjen lisäämistä optimointityökaluun."
author: roxanadiaconu
manager: AnnBe
ms.date: 01/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 9cb9343028acacc387370e1cdd2202b84919185e
ms.openlocfilehash: 88739298405343a36ae5bc11f51c666c414e7157
ms.contentlocale: fi-fi
ms.lasthandoff: 01/23/2018

---

# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="1c82f-103">Optimointityökalun sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="1c82f-103">Create rules for Optimization advisor</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1c82f-104">Tässä ohjeaiheessa selitetään, miten **optimointityökalun** uusia sääntöjä luodaan.</span><span class="sxs-lookup"><span data-stu-id="1c82f-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="1c82f-105">Voit esimerkiksi luoda uuden säännön, joka määrittää millä tarjouspyyntötapauksilla on tyhjä otsikko.</span><span class="sxs-lookup"><span data-stu-id="1c82f-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="1c82f-106">Kun tapauksissa käytetään otsikoita, ne on helppo tunnistaa ja niissä on helppo tehdä hakuja.</span><span class="sxs-lookup"><span data-stu-id="1c82f-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="1c82f-107">Tämä melko yksinkertainen esimerkki osoittaa, mitä optimointisäännöillä voi saavuttaa.</span><span class="sxs-lookup"><span data-stu-id="1c82f-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="1c82f-108">*Sääntö* tarkoittaa sovellustietojen tarkistusta.</span><span class="sxs-lookup"><span data-stu-id="1c82f-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="1c82f-109">Jos säännön arvioima ehto täyttyy, luodaan mahdollisuuksia prosessien optimointiin ja tietojen parannukseen.</span><span class="sxs-lookup"><span data-stu-id="1c82f-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="1c82f-110">Mahdollisuuksiin voidaan reagoida ja, valinnaisesti, toimintojen vaikutus voidaan mitata.</span><span class="sxs-lookup"><span data-stu-id="1c82f-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="1c82f-111">Voit luoda uuden säännön **optimointityökaluun** lisäämällä **DiagnosticRule**-määritteellä varustetun **SelfHealingRule**-abstraktiluokkaa laajentavan uuden luokan ja **IDiagnosticsRule**-liittymän toteutuksen.</span><span class="sxs-lookup"><span data-stu-id="1c82f-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="1c82f-112">Luokalla on myös **DiagnosticsRuleSubscription**-määritteellä varustettu menetelmä.</span><span class="sxs-lookup"><span data-stu-id="1c82f-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="1c82f-113">Yleensä se tehdään **opportunityTitle**-menetelmällä, joka käsitellään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="1c82f-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="1c82f-114">Tämä uusi luokka voidaan lisätä mukautettuun malliin, joka on riippuvainen **SelfHealingRules**-mallista.</span><span class="sxs-lookup"><span data-stu-id="1c82f-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="1c82f-115">Seuraavassa esimerkissä toteutetaan **RFQTitleSelfHealingRule**-niminen sääntö.</span><span class="sxs-lookup"><span data-stu-id="1c82f-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="1c82f-116">**SelfHealingRule**-abstraktiluokassa on abstraktimenetelmiä, jotka on toteutettava perivissä luokissa.</span><span class="sxs-lookup"><span data-stu-id="1c82f-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="1c82f-117">Ytimenä on **arviointimenetelmä**, joka palauttaa luettelon säännön tunnistamia mahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="1c82f-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="1c82f-118">Mahdollisuudet voivat olla yritys- tai järjestelmäkohtaisia.</span><span class="sxs-lookup"><span data-stu-id="1c82f-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

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

<span data-ttu-id="1c82f-119">Edellä oleva menetelmä hakee ja valitsee yrityksistä **findRFQCasesWithEmptyTitle**-menetelmällä tarjouspyyntötapauksia, joissa on tyhjiä otsikoita.</span><span class="sxs-lookup"><span data-stu-id="1c82f-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="1c82f-120">Jos vähintään yksi kyseinen tapaus löytyy, yrityskohtainen mahdollisuus luodaan **getOpportunityForCompany**-menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="1c82f-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="1c82f-121">Huomaa, että **SelfHealingOpportunity**-taulun **Tiedot**-kenttä on **Säilö**-tyyppinen ja siinä voi siksi olla tämän säännön logiikkaan liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="1c82f-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="1c82f-122">Kun **OpportunityDate** määritetään kuluvan hetken aikaleimalla, mahdollisuuden viimeisin arviointi rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="1c82f-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="1c82f-123">Mahdollisuudet voivat olla myös yritysten välisiä.</span><span class="sxs-lookup"><span data-stu-id="1c82f-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="1c82f-124">Siinä tapauksessa yritykset kattava haku ei ole välttämätöntä ja mahdollisuus on luotava **getOpportunityAcrossCompanies**-menetelmällä.</span><span class="sxs-lookup"><span data-stu-id="1c82f-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="1c82f-125">Seuraava koodi näyttää **findRFQCasesWithEmptyTitle**-menetelmän, joka palauttaa tyhjiä otsikoita sisältävien tarjouspyyntötapausten tunnukset.</span><span class="sxs-lookup"><span data-stu-id="1c82f-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

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

<span data-ttu-id="1c82f-126">**opportunityTitle** ja **opportunityDetails** ovat kaksi muuta toteutettavaa menetelmää.</span><span class="sxs-lookup"><span data-stu-id="1c82f-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="1c82f-127">Edellinen palauttaa mahdollisuuden lyhyen otsikon, kun taas jälkimmäinen palauttaa mahdollisuuden tarkan kuvauksen, joka voi sisältää myös tietoja.</span><span class="sxs-lookup"><span data-stu-id="1c82f-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="1c82f-128">**opportunityTitle**-menetelmän palauttava otsikko näkyy **Optimointityökalu**-työtilan **Optimointimahdollisuus**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1c82f-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="1c82f-129">Se näkyy myös sivuruudun otsikossa, jossa on lisätietoja mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="1c82f-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="1c82f-130">Yleensä tämä menetelmä on varustettu **DiagnosticRuleSubscription**-määritteellä, joka käyttää seuraavia argumentteja:</span><span class="sxs-lookup"><span data-stu-id="1c82f-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="1c82f-131">**Diagnosointialue** – Valintaluettelotyyppi **DiagnosticArea** kuvaa, mihin sovellusalueeseen sääntö kuuluu. Esimerkki: **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="1c82f-132">**Säännön nimi** – Merkkijono, jossa on säännön nimi.</span><span class="sxs-lookup"><span data-stu-id="1c82f-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="1c82f-133">Se näkyy **Säännön nimi** -sarakkeessa **Diagnostiikan vahvistussääntö** -lomakkeessa (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="1c82f-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="1c82f-134">**Suoritustiheys** – Valintaluettelotyyppi **DiagnosticRunFrequency** kuvaa, miten usein sääntö suoritetaan. Esimerkki: **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="1c82f-135">**Säännön kuvaus** – Merkkijono, jossa on säännön yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1c82f-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="1c82f-136">Se näkyy **Säännön kuvaus** -sarakkeessa **Diagnostiikan vahvistussääntö** -lomakkeessa (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="1c82f-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="1c82f-137">**DiagnosticRuleSubscription**-määrite on välttämätön säännön toiminnan kannalta.</span><span class="sxs-lookup"><span data-stu-id="1c82f-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="1c82f-138">Sitä käytetään yleensä **opportunityTitle**-menetelmässä, mutta se voi olla luokan minkä tahansa menetelmän varusteena.</span><span class="sxs-lookup"><span data-stu-id="1c82f-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="1c82f-139">Seuraavassa on esimerkkitoteutus.</span><span class="sxs-lookup"><span data-stu-id="1c82f-139">The following is an example implementation.</span></span> <span data-ttu-id="1c82f-140">Käsittelemättömiä merkkijonoja käytetään yksinkertaisuuden vuoksi, mutta oikea toteutus edellyttää otsikoita.</span><span class="sxs-lookup"><span data-stu-id="1c82f-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

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

<span data-ttu-id="1c82f-141">**opportunityDetails**-menetelmän palauttama kuvaus näkyy sivuruudussa ja siinä on lisätietoja mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="1c82f-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="1c82f-142">Se käyttää **SelfHealingOpportunity**-argumenttia, joka on **Tiedot**-kenttä ja jolla voi antaa lisätietoja mahdollisuudesta.</span><span class="sxs-lookup"><span data-stu-id="1c82f-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="1c82f-143">Esimerkissä menetelmä palauttaa tyhjän otsikon sisältävien tarjouspyyntötapausten tunnukset.</span><span class="sxs-lookup"><span data-stu-id="1c82f-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

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

<span data-ttu-id="1c82f-144">Jäljellä olevat kaksi toteutettavaa menetelmää ovat **provideHealingAction** ja **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="1c82f-145">**provideHealingAction** palauttaa tosi-arvon, jos korjaustoiminto annetaan. Muussa tapauksessa palautetaan epätosi.</span><span class="sxs-lookup"><span data-stu-id="1c82f-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="1c82f-146">Jos tosi palautetaan, menetelmä **performAction** on toteutettava tai tapahtuu virhe.</span><span class="sxs-lookup"><span data-stu-id="1c82f-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="1c82f-147">**performAction**-menetelmä käyttää **SelfHealingOpportunity**-argumenttia, jossa tietoja voi käyttää toimintaan.</span><span class="sxs-lookup"><span data-stu-id="1c82f-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="1c82f-148">Esimerkiksi toiminto avaa kohteen **PurchRFQCaseTableListPage** manuaalisesti korjattavaksi.</span><span class="sxs-lookup"><span data-stu-id="1c82f-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

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

<span data-ttu-id="1c82f-149">Säännön tietojen mukaan automaattinen toiminto voi olla mahdollista mahdollisuuden tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="1c82f-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="1c82f-150">Tässä esimerkissä järjestelmä voi luoda muodostaa tarjouspyyntötapausten otsikot automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1c82f-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="1c82f-151">**securityMenuItem** palauttaa toimintovalikkovaihtoehdon nimen siten, että sääntö näkyy vain käyttäjille, jotka voivat käyttää toiminnon valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="1c82f-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="1c82f-152">Suojaus voi edellyttää, että tietyt säännöt ja mahdollisuudet ovat vain valtuutettujen käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="1c82f-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="1c82f-153">Esimerkissä mahdollisuuden näkevät vain käyttäjät, joilla on **PurchRFQCaseTitleAction**-käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="1c82f-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="1c82f-154">Huomaa, että tämä toimintovalikkovaihtoehto luotiin tässä esimerkissä ja lisättiin **PurchRFQCaseTableMaintain**-suojausoikeuden aloituspisteeksi.</span><span class="sxs-lookup"><span data-stu-id="1c82f-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="1c82f-155">Kun sääntö on käännetty, saat sen näkyviin käyttöliittymään suorittamalla seuraava työ.</span><span class="sxs-lookup"><span data-stu-id="1c82f-155">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

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

<span data-ttu-id="1c82f-156">Sääntö näkyy **Diagnostiikan vahvistussääntö** -lomakkeessa, jonka voi avata valitsemalla **Järjestelmän hallinta** > **Kausittaiset tehtävät** > **Ylläpidä diagnostiikan vahvistussääntöä**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-156">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="1c82f-157">Voit arvioida sen valitsemalla ensin **Järjestelmän hallinta** > **Kausittaiset tehtävät** > **Aikatauluta diagnostiikan vahvistussääntö** ja sitten säännön tiheyden, kuten **Päivittäin**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-157">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="1c82f-158">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-158">Click **OK**.</span></span> <span data-ttu-id="1c82f-159">Voit tarkastella uutta mahdollisuutta valitsemalla **Järjestelmän hallinta** > **Optimointityökalu**.</span><span class="sxs-lookup"><span data-stu-id="1c82f-159">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="1c82f-160">Lisätietoja on lyhyessä YouTube-videossa:</span><span class="sxs-lookup"><span data-stu-id="1c82f-160">For more information, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

