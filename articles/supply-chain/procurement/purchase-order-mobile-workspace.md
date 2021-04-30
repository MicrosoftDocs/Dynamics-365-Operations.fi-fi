---
title: Ostotilauksen hyväksymisen mobiilityötila
description: Tässä ohjeaiheessa on tietoja ostotilauksen hyväksymisen mobiilityötilasta, jossa voit tarkastella ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26f0dc3b128daf8c7d8a05d6f3cacc5b7de0c756
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909105"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="58417-104">Ostotilauksen hyväksymisen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="58417-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58417-105">Tässä ohjeaiheessa on tietoja **ostotilausten hyväksymisen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="58417-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="58417-106">Voit tarkastella työtilassa ostotilauksia ja vastata niihin eri toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="58417-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="58417-107">Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="58417-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="58417-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="58417-108">Overview</span></span> 
<span data-ttu-id="58417-109">Hyväksymistä edellyttävät ostotilaukset läpäisevät hyväksymistyönkulun.</span><span class="sxs-lookup"><span data-stu-id="58417-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="58417-110">Työnkulussa voi olla erilaisia vaiheita, jotka edellyttävät vähintään yhden henkilön tekemiä toimia.</span><span class="sxs-lookup"><span data-stu-id="58417-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="58417-111">Henkilön on ehkä esimerkiksi suoritettava tehtävä loppuun tai hyväksyttävä ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="58417-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="58417-112">**Ostotilauksen hyväksymisen** työtilassa on helppo tarkastella ostotilauksia ja reagoida niihin mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="58417-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="58417-113">Työtilassa voi tehdä myös samoja toimia kuin verkkoasiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="58417-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58417-114">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="58417-114">Prerequisites</span></span>
<span data-ttu-id="58417-115">Edellytykset vaihtelevat sen mukaan, mikä Supply Chain Management -versio on otettu käyttöön organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="58417-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="58417-116">Supply Chain Managementin käytön edellytykset</span><span class="sxs-lookup"><span data-stu-id="58417-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="58417-117">Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Ostotilauksen hyväksyntä** -mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="58417-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="58417-118">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="58417-118">For instructions, see [Publish a mobile workspace](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="58417-119">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="58417-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="58417-120">Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="58417-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="58417-121">Edellytys</span><span class="sxs-lookup"><span data-stu-id="58417-121">Prerequisite</span></span></th>
<th><span data-ttu-id="58417-122">Rooli</span><span class="sxs-lookup"><span data-stu-id="58417-122">Role</span></span></th>
<th><span data-ttu-id="58417-123">kuvaus</span><span class="sxs-lookup"><span data-stu-id="58417-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58417-124">KB 4017918 -käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="58417-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="58417-125">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="58417-125">System administrator</span></span></td>
<td><span data-ttu-id="58417-126">KB 4017918 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>ostotilausten hyväksymisen</strong> mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="58417-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="58417-127">Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4017918 -päivityksen.</span><span class="sxs-lookup"><span data-stu-id="58417-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="58417-128"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="58417-128"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="58417-129"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</span><span class="sxs-lookup"><span data-stu-id="58417-129"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="58417-130"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</span><span class="sxs-lookup"><span data-stu-id="58417-130"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="58417-131"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="58417-131"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58417-132">Vapauta <strong>ostotilauksen hyväksymisen</strong> mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="58417-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="58417-133">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="58417-133">System administrator</span></span></td>
<td><span data-ttu-id="58417-134">Lisätietoja on ohjeaiheessa <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="58417-134">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="58417-135">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="58417-135">Download and install the mobile app</span></span>
<span data-ttu-id="58417-136">Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:</span><span class="sxs-lookup"><span data-stu-id="58417-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="58417-137">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="58417-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="58417-138">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="58417-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="58417-139">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="58417-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="58417-140">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="58417-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="58417-141">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="58417-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="58417-142">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="58417-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="58417-143">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="58417-143">Enter your credentials.</span></span>
4. <span data-ttu-id="58417-144">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="58417-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="58417-145">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="58417-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Ostotilauksen hyväksymisen työtila käytettävissä olevien työtilojen luettelossa](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="58417-147">Käyttäjälle määritettyjen tilausten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="58417-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="58417-148">Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.</span><span class="sxs-lookup"><span data-stu-id="58417-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="58417-149">Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.</span><span class="sxs-lookup"><span data-stu-id="58417-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="58417-150">Valitse tilaus.</span><span class="sxs-lookup"><span data-stu-id="58417-150">Select an order.</span></span> <span data-ttu-id="58417-151">Näet **Tilauksen tiedot** -sivulla tilauksen otsikon tiedot ja rivit.</span><span class="sxs-lookup"><span data-stu-id="58417-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="58417-152">Työkulkutehtävässä on myös ohjeet.</span><span class="sxs-lookup"><span data-stu-id="58417-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="58417-153">Avaa **Otsikon kirjanpidollinen jako** -sivu valitsemalla **Kirjanpidolliset jaot**.</span><span class="sxs-lookup"><span data-stu-id="58417-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="58417-154">Palaa **Tilauksen tiedot** -sivulle ja valitse rivi.</span><span class="sxs-lookup"><span data-stu-id="58417-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="58417-155">Voit tilausrivin tiedoissa rivikohtaisiin kirjanpidollisiin jakoihin.</span><span class="sxs-lookup"><span data-stu-id="58417-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="58417-156">Ostotilauksen toiminnon viimeistely</span><span class="sxs-lookup"><span data-stu-id="58417-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="58417-157">Kun olet tarkastellut sinulle määritettyä ostotilausta ja lukenut työnkulun ohjeet, olet valmis tekemään toimintoja.</span><span class="sxs-lookup"><span data-stu-id="58417-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="58417-158">Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.</span><span class="sxs-lookup"><span data-stu-id="58417-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="58417-159">Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.</span><span class="sxs-lookup"><span data-stu-id="58417-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="58417-160">Valitse tilaus ja tutustu tietosivun tietoihin.</span><span class="sxs-lookup"><span data-stu-id="58417-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="58417-161">Tuo käytettävissä olevat toiminnot näkyviin valitsemalla **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="58417-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="58417-162">Käytettävissä olevat toiminnot määräytyvät sinulle määritetyn tehtävän mukaan.</span><span class="sxs-lookup"><span data-stu-id="58417-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="58417-163">Tehtävätoiminto</span><span class="sxs-lookup"><span data-stu-id="58417-163">Task action</span></span>    | <span data-ttu-id="58417-164">Hyväksymistoiminto</span><span class="sxs-lookup"><span data-stu-id="58417-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="58417-165">Kokonaistoimitus</span><span class="sxs-lookup"><span data-stu-id="58417-165">Complete</span></span>       | <span data-ttu-id="58417-166">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="58417-166">Approve</span></span>          |
    | <span data-ttu-id="58417-167">Palautus</span><span class="sxs-lookup"><span data-stu-id="58417-167">Return</span></span>         | <span data-ttu-id="58417-168">Hylkää</span><span class="sxs-lookup"><span data-stu-id="58417-168">Reject</span></span>           |
    | <span data-ttu-id="58417-169">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="58417-169">Request change</span></span> | <span data-ttu-id="58417-170">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="58417-170">Request change</span></span>   |
    | <span data-ttu-id="58417-171">Edustaja</span><span class="sxs-lookup"><span data-stu-id="58417-171">Delegate</span></span>       | <span data-ttu-id="58417-172">Edustaja</span><span class="sxs-lookup"><span data-stu-id="58417-172">Delegate</span></span>         |

5. <span data-ttu-id="58417-173">Valitse asianmukainen toiminto.</span><span class="sxs-lookup"><span data-stu-id="58417-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="58417-174">Kirjoita kommentti **Suorita tehtävä** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="58417-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="58417-175">Huomaa, että jos valitset **Delegoi**-toiminnon, sinun on valittava käyttäjä, jolle tehtävä delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="58417-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="58417-176">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="58417-176">Select **Done**.</span></span> <span data-ttu-id="58417-177">Kun päivität työtilan, ostotilaus ei ole enää luettelossasi.</span><span class="sxs-lookup"><span data-stu-id="58417-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]