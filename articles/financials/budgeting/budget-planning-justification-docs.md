---
title: Budjettisuunnitelman perusteluasiakirjat
description: Perusteluasiakirjat tarjoavat budjettia pyytäville henkilöille kertomuksen siitä, miksi tietty budjetti on tarpeellinen.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5c7db2c10572ad7b5fd18381d139259c08182586
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834316"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="6e5f8-103">Budjettisuunnitelman perusteluasiakirjat</span><span class="sxs-lookup"><span data-stu-id="6e5f8-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e5f8-104">Perusteluasiakirjat tarjoavat budjettia pyytäville henkilöille kertomuksen siitä, miksi tietty budjetti on tarpeellinen.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="6e5f8-105">Budjettisuunnitelman mallin luo budjettipäällikkö Microsoft Wordissa ja malli määritetään nykyiseen budjetin suunnitteluprosessiin.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="6e5f8-106">Budjetin omistajat voivat sitten avata mallin ja tiedot täytetään automaattisesti Wordissa perustuen heidän budjettipyyntöönsä.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="6e5f8-107">Sitten he voivat lisätä lisätekstiä tai tietoja ennen tallentamista ja liittää mukautetun perusteluasiakirjan budjettisuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="6e5f8-108">Microsoft Dynamics Office -apuohjelman määritys Microsoft Wordissa</span><span class="sxs-lookup"><span data-stu-id="6e5f8-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="6e5f8-109">Avaa uusi Microsoft Word -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="6e5f8-110">Valitse valintanauhassa **Lisää** ja **Kauppa**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="6e5f8-111">Etsi Microsoft Dynamics Office -apuohjelma ja valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="6e5f8-112">Oikeanpuoleisessa ruudussa, valitse Wordissa **Lisää palvelimen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="6e5f8-113">Kirjoita tai liitä palvelimen URL-osoite ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="6e5f8-114">Perustelumallin määrittäminen Microsoft Wordissa</span><span class="sxs-lookup"><span data-stu-id="6e5f8-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="6e5f8-115">Valitse **Rakenne** Microsoft Dynamics Office -apuohjelmassa, kun olet kirjautunut.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="6e5f8-116">Käytä **Lisää kenttiä** -painiketta otsikkotietoihin.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="6e5f8-117">Valitse kohteen BudgetPlanJustification yksikkötietolähde ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="6e5f8-118">**Huomautus:** Tämä yksikkö on pakollinen kaikissa perusteluasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="6e5f8-119">Voidaan käyttää muita yksiköitä, mutta lataaminen Microsoft Dynamics 365 for Finance and Operationsiin epäonnistuu, jos tämä yksikkö ei ole mukana.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="6e5f8-120">Lisää Word-asiakirjaan seuraavat otsikot ja arvot: BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="6e5f8-121">**Huomautus:** voit tarvittaessa käyttää omia mukautettuja otsikoita vakio-otsikoiden sijaan.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="6e5f8-122">Valitse **Valmis** viimeistelläksesi otsikko-osan.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="6e5f8-123">Voit lisätä budjettisuunnitelman summat rivitasolle klikkaamalla **Lisää taulu**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="6e5f8-124">Valitse jälleen kohteen BudgetPlanJustification yksikkötietolähde ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="6e5f8-125">Lisää kentät kohteille EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="6e5f8-126">**Huomautus:** Jos kommentit ovat lisättävissä budjettisuunnitelman yksittäisissä riveissä, ne voidaan lisätä tähän taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="6e5f8-127">Lisää mahdolliset muut lisäohjeet loppukäyttäjälle ja suorita tarvittavat muotoilut ja tyylimuutokset asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="6e5f8-128">Tallenna tiedosto paikalliseen tietokoneeseen, ja sulje tiedosto ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="6e5f8-129">Määritä budjettisuunnitteluprosessi käyttämään perustelumallia</span><span class="sxs-lookup"><span data-stu-id="6e5f8-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="6e5f8-130">Siirry Finance and Operationsissa kohtaan **Budjetointi** &gt; **Asetukset** &gt; **Budjettisuunnittelu** &gt; **Perusteluasiakirjan mallit**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="6e5f8-131">Valitse **Uusi** ja siirry juuri luotuun Microsoft Word -asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="6e5f8-132">Syötä mallin näyttönimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-132">Enter a template display name and description.</span></span> <span data-ttu-id="6e5f8-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-133">Click **OK**.</span></span>
4.  <span data-ttu-id="6e5f8-134">Siirry kohtaan **Budjetointi** &gt; **Asetukset** &gt; **Budjetti** **suunnittelu** &gt; **Budjettisuunnitteluprosessi**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="6e5f8-135">Valitse prosessi, jossa perustelumallia tulee käyttää ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="6e5f8-136">Valitse **Perusteluasiakirjan malli** -kentässä sopiva malli ja tallenna.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="6e5f8-137">Muokkaa ja tallenna mukautetut perusteluasiakirjat</span><span class="sxs-lookup"><span data-stu-id="6e5f8-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="6e5f8-138">Luo Finance and Operationsissa uusi budjettisuunnitelma tai avaa olemassa oleva budjettisuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="6e5f8-139">Valitse avattavasta **Perustelut** -valikosta **Luo uusi perustelu**.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="6e5f8-140">Kun olet täyttänyt tiedot, valitse mukautetun asiakirjan lataaminen avattavasta **Perustelut**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>




