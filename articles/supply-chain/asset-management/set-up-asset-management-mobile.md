---
title: Resurssien hallinnan mobiilityötilan määrittäminen
description: Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin ja Finance and Operations (Dynamics 365) -mobiilisovelluksen määrittämistä suorittamaan resurssien hallinnan mobiilityötila, jota työntekijät voivat käyttää resurssien hallintatehtävien suorittamiseen.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837774"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="be9fa-103">Resurssien hallinnan mobiilityötilan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="be9fa-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be9fa-104">Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin ja Finance and Operations (Dynamics 365) -mobiilisovelluksen määrittämistä suorittamaan **Resurssien hallinta** -mobiilityötila, jota työntekijät voivat käyttää resurssien hallintatehtävien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="be9fa-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="be9fa-105">Ylläpitotyöntekijäkäyttäjien määrittäminen Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="be9fa-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="be9fa-106">**Resurssien hallinta** -työtilan käyttöoikeus määritetään sitä tarvitseville käyttäjille seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="be9fa-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="be9fa-107">Valitse Supply Chain Managementissa **Henkilöstöhallinto \> Työntekijät** ja varmista, että määritettävällä käyttäjällä on työntekijätietue.</span><span class="sxs-lookup"><span data-stu-id="be9fa-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="be9fa-108">Luo tarvittaessa uusi työntekijätietue.</span><span class="sxs-lookup"><span data-stu-id="be9fa-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="be9fa-109">Valitse **Resurssien hallinta \> Asetukset \> Työntekijät \> Työntekijät** ja varmista, että edellisessä vaiheessa määritetty (tai luotu) työntekijätietue on yhdistetty ylläpitotyöntekijätietueeseen.</span><span class="sxs-lookup"><span data-stu-id="be9fa-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="be9fa-110">Luo tarvittaessa uusi ylläpitotyöntekijätietue ja määritä **Työntekijä**-kenttään edellisen vaiheen työntekijätietue.</span><span class="sxs-lookup"><span data-stu-id="be9fa-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="be9fa-111">Valitse **Resurssien hallinta \> Asetukset \> Työntekijät \> Ylläpitotyöntekijäryhmät** ja varmista, että edellisessä vaiheessa määritetty (tai luotu) ylläpitotyöntekijätietue on kuuluu ylläpitotyöntekijäryhmään.</span><span class="sxs-lookup"><span data-stu-id="be9fa-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="be9fa-112">Valitse **Järjestelmänhallinta \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="be9fa-113">Valitse sopiva käyttäjä ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="be9fa-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="be9fa-114">Määritä **Käyttäjän tiedot** -pikavälilehdessä **Henkilö**-kenttään työtekijätietue, joka halutaan liittää nykyiseen käyttäjätiliin.</span><span class="sxs-lookup"><span data-stu-id="be9fa-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="be9fa-115">Tämän työntekijätietueen on oltava vaiheessa yksi määritetty (tai luotu) työntekijätietue, joka yhdistetiin ylläpitotyöntekijätietueeseen vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="be9fa-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="be9fa-116">Käyttöoikeudet ja käyttöoikeusroolit koskevat **Resurssien hallinta** -mobiilityötilan toimintoja samalla tavoin kuin ne koskevat Supply Chain Management -käyttöliittymän toimintoja.</span><span class="sxs-lookup"><span data-stu-id="be9fa-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="be9fa-117">Niinpä jokaisella käyttäjällä, jolle määritetään **Resurssien hallinta** -työtilan käyttöoikeus, on oltava käyttöoikeusroolit, joita tarvitaan samanlaisten toimintojen suorittamiseen suoraan Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="be9fa-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="be9fa-118">Resurssien hallinnan mobiilityötilan julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="be9fa-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="be9fa-119">Resurssien hallinnan toimintojen käyttöönottaminen Finance and Operations (Dynamics 365) -mobiilisovelluksessa edellyttää **Resurssien hallinta** -mobiilityötilan julkaisemista.</span><span class="sxs-lookup"><span data-stu-id="be9fa-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="be9fa-120">Valitse Supply Chain Managementissa **Asetukset**-painike (rataskuvake oikeassa yläkulmassa) ja valitse sitten valikossa **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="be9fa-121">Etsi **Mobiilisovelluksen hallinta** -valintaikkunassa **Resurssien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="be9fa-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="be9fa-122">Jos siinä on teksti Metatiedoissa – ei julkaistu, työtilaa ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="be9fa-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="be9fa-123">Jos siinä on teksti Metatiedoissa – julkaistu, työtila on jo julkaistu ja tämän menettelyn muut vaiheet voidaan ohittaa.</span><span class="sxs-lookup"><span data-stu-id="be9fa-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="be9fa-124">![Mobiilisovelluksen hallinta -valintaikkuna](media/mobile-workspaces.png "Mobiilisovelluksen hallinta -valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="be9fa-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="be9fa-125">Valitse ensin **Resurssien hallinta** -ruutu ja sitten työkalurivillä **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="be9fa-126">Muutaman sekunnin kuluttua pitäisi avautua ilmoitus, jonka mukaan työtilan julkaisu on onnistunut.</span><span class="sxs-lookup"><span data-stu-id="be9fa-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="be9fa-127">Lisäksi ruudussa olevan tekstin pitäisi olla nyt Metatiedoissa – julkaistu.</span><span class="sxs-lookup"><span data-stu-id="be9fa-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="be9fa-128">Finance and Operations (Dynamics 365) -mobiilisovelluksen asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="be9fa-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="be9fa-129">Asenna **Microsoft Finance and Operations (Dynamics 365)** -sovellus mobiililaitteeseen siirtymällä johonkin seuraavista sovelluskaupoista:</span><span class="sxs-lookup"><span data-stu-id="be9fa-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="be9fa-130">Google Android -laitteet</span><span class="sxs-lookup"><span data-stu-id="be9fa-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="be9fa-131">Apple iOS -laitteet</span><span class="sxs-lookup"><span data-stu-id="be9fa-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="be9fa-132">Avaa Finance and Operations (Dynamics 365) -sovellus.</span><span class="sxs-lookup"><span data-stu-id="be9fa-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="be9fa-133">Kirjautumissivun pitäisi avautua.</span><span class="sxs-lookup"><span data-stu-id="be9fa-133">The sign-in page should appear.</span></span> <span data-ttu-id="be9fa-134">Anna **Kirjaudu sisään** -kentässä Supply Chain Managementin URL-osoite tai valitse viimeaikainen URL-osoite **Viimeisimmät ympäristöt** -luettelo ja valitse sitten **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="be9fa-135">![Kirjautumissivu](media/mobile-app-sign-in.png "Kirjautumissivu")</span><span class="sxs-lookup"><span data-stu-id="be9fa-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="be9fa-136">Jos yhteys pyydetään vahvistamaan, valitse **Ymmärrän**-valintaruutu ja valitse sitten **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="be9fa-137">Kirjaudu mobiilisovellukseen käyttämällä **Valitse tili** -sivulla Microsoft-tiliä.</span><span class="sxs-lookup"><span data-stu-id="be9fa-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="be9fa-138">**Työtilat**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="be9fa-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="be9fa-139">Siinä on luettelo kaikista mobiilityötiloista, jotka Supply Chain Management -esiintymä on julkaissut.</span><span class="sxs-lookup"><span data-stu-id="be9fa-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="be9fa-140">![Työtilojen luettelo](media/mobile-app-workspaces.png "Työtilojen luettelo")</span><span class="sxs-lookup"><span data-stu-id="be9fa-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="be9fa-141">Jos yritystä (yhtiötä) on vaihdettava, napauta vasemmassa yläkulmassa Valikko-painiketta (siinä useita allekkaisia viivoja) ja valitse sitten **Vaihda yritys**.</span><span class="sxs-lookup"><span data-stu-id="be9fa-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="be9fa-142">![Yrityksen vaihtaminen](media/mobile-app-change-comp.png "Yrityksen vaihtaminen")</span><span class="sxs-lookup"><span data-stu-id="be9fa-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="be9fa-143">Avaa **Työtilat**-sivulla työtila, jota haluat käyttää, valitsemalla se.</span><span class="sxs-lookup"><span data-stu-id="be9fa-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="be9fa-144">![Resurssien hallinnan mobiilityötila](media/mobile-app-asset-workspace.png "Resurssien hallinnan mobiilityötila")</span><span class="sxs-lookup"><span data-stu-id="be9fa-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="be9fa-145">Resurssien hallinnan mobiilityötilan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="be9fa-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="be9fa-146">Lisätietoja **Resurssien hallinta** -mobiilityötilan käyttämisestä on kohdassa [Resurssien hallinnan mobiilityötilan käyttäminen](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="be9fa-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="be9fa-147">Lisätietoja Finance and Operations (Dynamics 365) -mobiilisovelluksesta on kohdassa [Mobiilisovelluksen aloitussivu](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="be9fa-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]