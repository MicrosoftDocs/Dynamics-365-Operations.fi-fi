---
title: "Ostotilauksen hyväksymisen mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja ostotilauksen hyväksymisen mobiilityötilasta, jossa voit tarkastella ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 12f710caea987dec9a343774f060e7dd7ca03ec4
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="2d467-104">Ostotilauksen hyväksymisen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="2d467-104">Purchase order approval mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="2d467-105">Tässä ohjeaiheessa on tietoja **ostotilausten hyväksymisen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="2d467-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="2d467-106">Voit tarkastella työtilassa ostotilauksia ja vastata niihin eri toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="2d467-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="2d467-107">Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="2d467-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="2d467-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="2d467-108">Overview</span></span> 
<span data-ttu-id="2d467-109">Hyväksymistä edellyttävät ostotilaukset läpäisevät hyväksymistyönkulun.</span><span class="sxs-lookup"><span data-stu-id="2d467-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="2d467-110">Työnkulussa voi olla erilaisia vaiheita, jotka edellyttävät vähintään yhden henkilön tekemiä toimia.</span><span class="sxs-lookup"><span data-stu-id="2d467-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="2d467-111">Henkilön on ehkä esimerkiksi suoritettava tehtävä loppuun tai hyväksyttävä ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="2d467-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="2d467-112">**Ostotilauksen hyväksymisen** työtilassa on helppo tarkastella ostotilauksia ja reagoida niihin mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="2d467-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="2d467-113">Työtilassa voi myös tehdä samoja toimia kuin Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin verkkoasiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="2d467-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2d467-114">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="2d467-114">Prerequisites</span></span>
<span data-ttu-id="2d467-115">Edellytykset vaihtelevat sen mukaan, mikä Finance and Operationsin versio on otettu käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="2d467-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="2d467-116">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys</span><span class="sxs-lookup"><span data-stu-id="2d467-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span> 
<span data-ttu-id="2d467-117">Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **ostotilauksen hyväksymisen** mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="2d467-117">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="2d467-118">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="2d467-118">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="2d467-119">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611, johon on asennettu vähintään ympäristöpäivitys 3</span><span class="sxs-lookup"><span data-stu-id="2d467-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="2d467-120">Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="2d467-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2d467-121">Edellytys</span><span class="sxs-lookup"><span data-stu-id="2d467-121">Prerequisite</span></span></th>
<th><span data-ttu-id="2d467-122">Rooli</span><span class="sxs-lookup"><span data-stu-id="2d467-122">Role</span></span></th>
<th><span data-ttu-id="2d467-123">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2d467-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2d467-124">KB 4017918 -käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="2d467-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="2d467-125">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="2d467-125">System administrator</span></span></td>
<td><span data-ttu-id="2d467-126">KB 4017918 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>ostotilausten hyväksymisen</strong> mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="2d467-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="2d467-127">Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4017918 -päivityksen.</span><span class="sxs-lookup"><span data-stu-id="2d467-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="2d467-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="2d467-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="2d467-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</span><span class="sxs-lookup"><span data-stu-id="2d467-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="2d467-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</span><span class="sxs-lookup"><span data-stu-id="2d467-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="2d467-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="2d467-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d467-132">Vapauta <strong>ostotilauksen hyväksymisen</strong> mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="2d467-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="2d467-133">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="2d467-133">System administrator</span></span></td>
<td><span data-ttu-id="2d467-134">Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="2d467-134">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="2d467-135">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="2d467-135">Download and install the mobile app</span></span>
<span data-ttu-id="2d467-136">Lataa ja asenna Microsoft Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="2d467-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="2d467-137">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="2d467-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="2d467-138">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="2d467-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="2d467-139">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="2d467-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="2d467-140">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="2d467-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="2d467-141">Anna oman Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="2d467-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="2d467-142">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="2d467-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="2d467-143">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="2d467-143">Enter your credentials.</span></span>
4. <span data-ttu-id="2d467-144">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="2d467-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="2d467-145">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="2d467-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Ostotilauksen hyväksymisen työtila käytettävissä olevien työtilojen luettelossa](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="2d467-147">Käyttäjälle määritettyjen tilausten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="2d467-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="2d467-148">Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.</span><span class="sxs-lookup"><span data-stu-id="2d467-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="2d467-149">Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.</span><span class="sxs-lookup"><span data-stu-id="2d467-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="2d467-150">Valitse tilaus.</span><span class="sxs-lookup"><span data-stu-id="2d467-150">Select an order.</span></span> <span data-ttu-id="2d467-151">Näet **Tilauksen tiedot** -sivulla tilauksen otsikon tiedot ja rivit.</span><span class="sxs-lookup"><span data-stu-id="2d467-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="2d467-152">Työkulkutehtävässä on myös ohjeet.</span><span class="sxs-lookup"><span data-stu-id="2d467-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="2d467-153">Avaa **Otsikon kirjanpidollinen jako** -sivu valitsemalla **Kirjanpidolliset jaot**.</span><span class="sxs-lookup"><span data-stu-id="2d467-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="2d467-154">Palaa **Tilauksen tiedot** -sivulle ja valitse rivi.</span><span class="sxs-lookup"><span data-stu-id="2d467-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="2d467-155">Voit tilausrivin tiedoissa rivikohtaisiin kirjanpidollisiin jakoihin.</span><span class="sxs-lookup"><span data-stu-id="2d467-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="2d467-156">Ostotilauksen toiminnon viimeistely</span><span class="sxs-lookup"><span data-stu-id="2d467-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="2d467-157">Kun olet tarkastellut sinulle määritettyä ostotilausta ja lukenut työnkulun ohjeet, olet valmis tekemään toimintoja.</span><span class="sxs-lookup"><span data-stu-id="2d467-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="2d467-158">Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.</span><span class="sxs-lookup"><span data-stu-id="2d467-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="2d467-159">Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.</span><span class="sxs-lookup"><span data-stu-id="2d467-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="2d467-160">Valitse tilaus ja tutustu tietosivun tietoihin.</span><span class="sxs-lookup"><span data-stu-id="2d467-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="2d467-161">Tuo käytettävissä olevat toiminnot näkyviin valitsemalla **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="2d467-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="2d467-162">Käytettävissä olevat toiminnot määräytyvät sinulle määritetyn tehtävän mukaan.</span><span class="sxs-lookup"><span data-stu-id="2d467-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="2d467-163">Tehtävätoiminto</span><span class="sxs-lookup"><span data-stu-id="2d467-163">Task action</span></span>    | <span data-ttu-id="2d467-164">Hyväksymistoiminto</span><span class="sxs-lookup"><span data-stu-id="2d467-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="2d467-165">Kokonaistoimitus</span><span class="sxs-lookup"><span data-stu-id="2d467-165">Complete</span></span>       | <span data-ttu-id="2d467-166">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="2d467-166">Approve</span></span>          |
    | <span data-ttu-id="2d467-167">Palautus</span><span class="sxs-lookup"><span data-stu-id="2d467-167">Return</span></span>         | <span data-ttu-id="2d467-168">Hylkää</span><span class="sxs-lookup"><span data-stu-id="2d467-168">Reject</span></span>           |
    | <span data-ttu-id="2d467-169">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="2d467-169">Request change</span></span> | <span data-ttu-id="2d467-170">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="2d467-170">Request change</span></span>   |
    | <span data-ttu-id="2d467-171">Edustaja</span><span class="sxs-lookup"><span data-stu-id="2d467-171">Delegate</span></span>       | <span data-ttu-id="2d467-172">Edustaja</span><span class="sxs-lookup"><span data-stu-id="2d467-172">Delegate</span></span>         |

5. <span data-ttu-id="2d467-173">Valitse asianmukainen toiminto.</span><span class="sxs-lookup"><span data-stu-id="2d467-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="2d467-174">Kirjoita kommentti **Suorita tehtävä** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="2d467-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="2d467-175">Huomaa, että jos valitset **Delegoi**-toiminnon, sinun on valittava käyttäjä, jolle tehtävä delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="2d467-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="2d467-176">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="2d467-176">Select **Done**.</span></span> <span data-ttu-id="2d467-177">Kun päivität työtilan, ostotilaus ei ole enää luettelossasi.</span><span class="sxs-lookup"><span data-stu-id="2d467-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

