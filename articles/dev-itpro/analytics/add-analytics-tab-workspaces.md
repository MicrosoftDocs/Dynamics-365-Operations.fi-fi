---
title: "Analytiikan lisääminen työtiloihin Power BI Embeddedin avulla"
description: "Tässä ohjeaiheessa kerrotaan, miten Power BI -raportti upotetaan työtilan Analytiikka-välilehteen."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: bf2c6c9be05f2b1f941d99c90a681cb9951de875
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="206ec-103">Analytiikan lisääminen työtiloihin Power BI Embeddedin avulla</span><span class="sxs-lookup"><span data-stu-id="206ec-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="206ec-104">Ominaisuutta tuetaan Dynamics 365 for Finance and Operationsin versiossa 7.2 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="206ec-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

# <a name="introduction"></a><span data-ttu-id="206ec-105">Johdanto</span><span class="sxs-lookup"><span data-stu-id="206ec-105">Introduction</span></span>
<span data-ttu-id="206ec-106">Tässä ohjeaiheessa kerrotaan, miten Microsoft Power BI -raportti upotetaan työtilan **Analytiikka**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="206ec-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="206ec-107">Tässä esimerkissä Kuljetuskaluston hallinta -sovelluksen **Varausten hallinta** -työtila laajennetaan upottamaan analyysityötila **Analytiikka**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="206ec-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

# <a name="prerequisites"></a><span data-ttu-id="206ec-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="206ec-108">Prerequisites</span></span>
+ <span data-ttu-id="206ec-109">Ympäristön päivityksessä 8 tai sitä uudemmassa päivityksessä käytössä olevan kehitysympäristön käyttö.</span><span class="sxs-lookup"><span data-stu-id="206ec-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="206ec-110">Microsoft Power BI Desktopilla luotu analyysiraportti (.pbix-tiedosto), jonka tietomallin lähteenä on Yksikkösäilö-tietokanta.</span><span class="sxs-lookup"><span data-stu-id="206ec-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

# <a name="overview"></a><span data-ttu-id="206ec-111">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="206ec-111">Overview</span></span>
<span data-ttu-id="206ec-112">Riippumatta siitä laajennatko aiemmin luodun sovellustyötilan vai otatko käyttöön oman uuden työtilan, voit käyttää upotettuja analyysinäkymiä ja saada niiden kautta hyödyllistä ja vuorovaikutteista tietoa liiketoimintatiedoista.</span><span class="sxs-lookup"><span data-stu-id="206ec-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="206ec-113">Analyysityötilan välilehti lisätään neljässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="206ec-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="206ec-114">Lisää .pbix-tiedosto Dynamics 365 -resurssina.</span><span class="sxs-lookup"><span data-stu-id="206ec-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="206ec-115">Määritä analyysityötilan välilehti.</span><span class="sxs-lookup"><span data-stu-id="206ec-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="206ec-116">Upota .pbix-resurssi työtilan välilehteen.</span><span class="sxs-lookup"><span data-stu-id="206ec-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="206ec-117">Valinnainen: Lisää laajennuksia näkymää mukauttamalla.</span><span class="sxs-lookup"><span data-stu-id="206ec-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="206ec-118">Lisätietoja analyysiraporttien luomisesta on ohjeaiheessa [Power BI Desktopin käytön aloittaminen](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="206ec-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="206ec-119">Tällä sivulla on tietoja tavoista, joilla voit luoda vaikuttavia analyysiraporttiratkaisuja.</span><span class="sxs-lookup"><span data-stu-id="206ec-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

# <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="206ec-120">.pbix-tiedoston lisääminen resurssina</span><span class="sxs-lookup"><span data-stu-id="206ec-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="206ec-121">Ennen aloittamista on luotava tai haettava työtilaan upotettava Power BI -raportti.</span><span class="sxs-lookup"><span data-stu-id="206ec-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="206ec-122">Lisätietoja analyysiraporttien luomisesta on ohjeaiheessa [Power BI Desktopin käytön aloittaminen](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="206ec-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>
 
<span data-ttu-id="206ec-123">Lisää .pbix-tiedosto Visual Studio -projektin artefakti.</span><span class="sxs-lookup"><span data-stu-id="206ec-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="206ec-124">Luo uusi projekti sopivassa mallissa-</span><span class="sxs-lookup"><span data-stu-id="206ec-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="206ec-125">Valitse ratkaisunhallinnassa projekti, napsauta hiiren kakkospainikkeella ja valitse sitten **Lisää** > **Uusi nimike**.</span><span class="sxs-lookup"><span data-stu-id="206ec-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="206ec-126">Valitse **Lisää uusi nimike** -valintaikkunan **Toimintojen artefaktit** -kohdassa **Resurssi**-malli.</span><span class="sxs-lookup"><span data-stu-id="206ec-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="206ec-127">Anna nimi, jolla viitataan X++-metatietojen raporttiin ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="206ec-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Lisää uusi nimike -valintaikkuna](media/analytical-workspace-add.png)

5. <span data-ttu-id="206ec-129">Etsi analyysiraportin määritelmän sisältävä .pbix-tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="206ec-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Valitse resurssitiedosto -valintaikkuna](media/analytical-workspace-select-resource.png)
  
<span data-ttu-id="206ec-131">Nyt kun .pbix-tiedosto on lisätty Dynamics 365 -resurssina, voit upottaa raportteja työtiloihin ja lisätä suoria linkkejä valikkovaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="206ec-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

# <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="206ec-132">Välilehtiohjausobjektin lisääminen sovelluksen työtilaan</span><span class="sxs-lookup"><span data-stu-id="206ec-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="206ec-133">Tässä esimerkissä Kuljetuskaluston hallinta -mallin **Varausten hallinta** -työtilaa laajennetaan lisäämällä **Analytiikka**-välilehti **FMClerkWorkspace**-lomakkeen määritelmään.</span><span class="sxs-lookup"><span data-stu-id="206ec-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>
 
<span data-ttu-id="206ec-134">Seuraavassa kuvassa näytetään, miltä **FMClerkWorkspace**-lomake näyttää Microsoft Visual Studion suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="206ec-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![FMClerkWorkspace-lomake ennen muutoksia](media/analytical-workspace-definition-before.png)

<span data-ttu-id="206ec-136">Laajenna **Varausten hallinta** -työtilan lomakemääritystä seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="206ec-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="206ec-137">Laajenna suunnittelumääritelmä avaamalla lomakkeen suunnittelutila.</span><span class="sxs-lookup"><span data-stu-id="206ec-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="206ec-138">Valitse suunnittelumäärityksessä ylin elementti, jonka nimi on **Rakenne | Kuvio: työtila toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="206ec-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="206ec-139">Napsauta hiiren kakkospainikkeella, valitse **Uusi** > **Välilehti** ja lisää uusi **FormTabControl1**-niminen ohjausobjekti.</span><span class="sxs-lookup"><span data-stu-id="206ec-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="206ec-140">Valitse lomakkeen suunnittelutilassa **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="206ec-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="206ec-141">Napsauta hiiren kakkospainikkeella ja lisää uusi välilehtisivu valitsemalla **Uusi välilehtisivu**.</span><span class="sxs-lookup"><span data-stu-id="206ec-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="206ec-142">Anna välilehtisivulla uusi merkityksellinen nimi, kuten **Työtila**.</span><span class="sxs-lookup"><span data-stu-id="206ec-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="206ec-143">Valitse lomakkeen suunnittelutilassa **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="206ec-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="206ec-144">Napsauta hiiren kakkospainikkeella ja valitse sitten **Uusi välilehtisivu**.</span><span class="sxs-lookup"><span data-stu-id="206ec-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="206ec-145">Anna välilehtisivulla uusi merkityksellinen nimi, kuten **Analytiikka**.</span><span class="sxs-lookup"><span data-stu-id="206ec-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="206ec-146">Valitse lomakkeen suunnittelutilassa **Analytiikka (välilehtisivu)**.</span><span class="sxs-lookup"><span data-stu-id="206ec-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="206ec-147">Määritä **Otsikko**-ominaisuudeksi **Analytiikka**.</span><span class="sxs-lookup"><span data-stu-id="206ec-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="206ec-148">Napsauta ohjausobjektia hiiren kakkospainikkeella ja lisää sitten uusi lomakeryhmän ohjausobjekti valitsemalla **Uusi** > **Ryhmä**.</span><span class="sxs-lookup"><span data-stu-id="206ec-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="206ec-149">Anna lomakeryhmälle uusi merkityksellinen nimi, kuten **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="206ec-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="206ec-150">Valitse lomakkeen suunnittelutilassa **PanoramaBody (välilehti)** ja vedä ohjausobjekti sitten **Työtila**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="206ec-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="206ec-151">Valitse suunnittelumäärityksessä ylin elementti, jonka nimi on **Rakenne | Kuvio: työtila toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="206ec-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="206ec-152">Napsauta hiiren kakkospainikkeella ja valitse sitten **Poista kuvio**.</span><span class="sxs-lookup"><span data-stu-id="206ec-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="206ec-153">Napsauta hiiren kakkospainikkeella uudelleen ja valitse sitten **Lisää kuvio** > **Välilehdellinen työtila**.</span><span class="sxs-lookup"><span data-stu-id="206ec-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="206ec-154">Tarkista muutokset luomalla koontiversio.</span><span class="sxs-lookup"><span data-stu-id="206ec-154">Perform a build to verify your changes.</span></span>
 
<span data-ttu-id="206ec-155">Seuraava kuva osoittaa, miltä rakenne näyttää muutosten jälkeen.</span><span class="sxs-lookup"><span data-stu-id="206ec-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace muutosten jälkeen](media/analytical-workspace-definition-after.png)

<span data-ttu-id="206ec-157">Nyt kun työtilan raportin upottamiseen käytettävät lomakkeen ohjausobjektit on lisätty, pääohjausobjektin koko on määritettävä asetteluun sopivaksi.</span><span class="sxs-lookup"><span data-stu-id="206ec-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="206ec-158">Oletusarvoisesti sekä **Suodatinruutu**-sivu että **Välilehti**-sivu näkyvät raportissa.</span><span class="sxs-lookup"><span data-stu-id="206ec-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="206ec-159">Voit kuitenkin muuttaa näiden ohjausobjektien näkyvyyttä raportin kohdekäyttäjän mukaan.</span><span class="sxs-lookup"><span data-stu-id="206ec-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>
 
> [!NOTE]
> <span data-ttu-id="206ec-160">Upotetuissa työtiloissa kannattaa käyttää laajennuksia, jotka piilottavat yhdenmukaisuuden vuoksi sekä **Suodatinruutu**- että **Välilehti**-sivut.</span><span class="sxs-lookup"><span data-stu-id="206ec-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>
 
<span data-ttu-id="206ec-161">Olet nyt suorittanut sovelluksen lomakemäärityksen laajennustehtävän.</span><span class="sxs-lookup"><span data-stu-id="206ec-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="206ec-162">Lisätietoja mukautusten tekemisestä laajennusten avulla on ohjeaiheessa [Mukauttaminen: lisäykset ja laajennukset](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="206ec-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="206ec-163">Katseluohjausobjektin upottaminen lisäämällä X++-liiketoimintalogiikka</span><span class="sxs-lookup"><span data-stu-id="206ec-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="206ec-164">Lisää näiden ohjeiden mukaisesti liiketoimintalogiikka, joka käynnistää **Varausten hallinta** -työtilaan upotetun raportin katseluohjelman ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="206ec-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="206ec-165">Laajenna suunnittelumääritys avaamalla **FMClerkWorkspace**-lomakkeen suunnittelutila.</span><span class="sxs-lookup"><span data-stu-id="206ec-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="206ec-166">Käytä koodimäärityksen taustalla olevaa koodia F7-näppäimellä.</span><span class="sxs-lookup"><span data-stu-id="206ec-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="206ec-167">Lisää seuraava X++-koodi.</span><span class="sxs-lookup"><span data-stu-id="206ec-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="206ec-168">Tarkista muutokset luomalla koontiversio.</span><span class="sxs-lookup"><span data-stu-id="206ec-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="206ec-169">Olet nyt suorittanut tehtävän, jolla upotetun raportin katseluohjelman ohjausobjektin käynnistävä liiketoimintalogiikka lisätään.</span><span class="sxs-lookup"><span data-stu-id="206ec-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="206ec-170">Seuraava kuva osoittaa, miltä työtila näyttää muutosten jälkeen.</span><span class="sxs-lookup"><span data-stu-id="206ec-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Työtilaan upotettu raportti](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="206ec-172">Voit käyttää aiemmin luotua toimintonäkymää käyttämällä sivun otsikkoon kuuluvia työtilan välilehtiä.</span><span class="sxs-lookup"><span data-stu-id="206ec-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

# <a name="reference"></a><span data-ttu-id="206ec-173">Viite</span><span class="sxs-lookup"><span data-stu-id="206ec-173">Reference</span></span>

## <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="206ec-174">PBIReportHelper.initializeReportControl-menetelmä</span><span class="sxs-lookup"><span data-stu-id="206ec-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="206ec-175">Tässä osassa on tietoja aputoimintoluokasta, jolla Power BI -rapotti (.pbix-resurssi) upotetaan lomakeryhmän ohjausobjektiin.</span><span class="sxs-lookup"><span data-stu-id="206ec-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

### <a name="syntax"></a><span data-ttu-id="206ec-176">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="206ec-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a><span data-ttu-id="206ec-177">Parametrit</span><span class="sxs-lookup"><span data-stu-id="206ec-177">Parameters</span></span>

| <span data-ttu-id="206ec-178">Nimi</span><span class="sxs-lookup"><span data-stu-id="206ec-178">Name</span></span> | <span data-ttu-id="206ec-179">kuvaus</span><span class="sxs-lookup"><span data-stu-id="206ec-179">Description</span></span> |
|---|---|
| <span data-ttu-id="206ec-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="206ec-180">resourceName</span></span> | <span data-ttu-id="206ec-181">.pbix-resurssin nimi.</span><span class="sxs-lookup"><span data-stu-id="206ec-181">The name of the .pbix resource.</span></span> |
| <span data-ttu-id="206ec-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="206ec-182">formGroupControl</span></span> | <span data-ttu-id="206ec-183">Lomakeryhmän ohjausobjekti, johon Power BI -raportin ohjausobjektia käytetään.</span><span class="sxs-lookup"><span data-stu-id="206ec-183">The form group control to apply the Power BI report control to.</span></span> |
| <span data-ttu-id="206ec-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="206ec-184">defaultPageName</span></span> | <span data-ttu-id="206ec-185">Oletussivun nimi.</span><span class="sxs-lookup"><span data-stu-id="206ec-185">The default page name.</span></span> |
| <span data-ttu-id="206ec-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="206ec-186">showFilterPane</span></span> | <span data-ttu-id="206ec-187">Totuusarvo, joka ilmaisee, näytetäänkö suodatinruutu (**tosi**) vai piilotetaanko se (**epätosi**).</span><span class="sxs-lookup"><span data-stu-id="206ec-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="206ec-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="206ec-188">showNavPane</span></span> | <span data-ttu-id="206ec-189">Totuusarvo, joka ilmaisee, näytetäänkö siirtymisruutu (**tosi**) vai piilotetaanko se (**epätosi**).</span><span class="sxs-lookup"><span data-stu-id="206ec-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="206ec-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="206ec-190">defaultFilters</span></span> | <span data-ttu-id="206ec-191">Power BI -raportin oletussuodattimet.</span><span class="sxs-lookup"><span data-stu-id="206ec-191">The default filters for the Power BI report.</span></span> |

