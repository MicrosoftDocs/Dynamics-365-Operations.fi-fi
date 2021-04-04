---
title: Tehtävienhallinnan määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtävienhallintatoiminnot määritetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478041"
---
# <a name="configure-task-management"></a><span data-ttu-id="60e9a-103">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="60e9a-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60e9a-104">Tässä ohjeaiheessa kerrotaan, miten tehtävienhallintatoiminnot määritetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="60e9a-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="60e9a-105">Ennen kuin Dynamics 365 Commercen päälliköt ja työntekijät voivat käyttää tehtävienhallintatoimintoja Commercessa, tehtävienhallinta on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="60e9a-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="60e9a-106">Määritysvaiheet sisältävät käyttöoikeuksien myöntämisen päälliköille ja työntekijöille, käyttöoikeuksien jakelun myyntipisteen asiakassovelluksille, myyntipisteen ilmoitusten määrittämisen ja myyntipistesovelluksen aloitussivun **Tehtävät**-ruudun määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="60e9a-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="60e9a-107">Myymäläpäälliköiden käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="60e9a-107">Configure permissions for store managers</span></span>

<span data-ttu-id="60e9a-108">Jokainen määritetyn myymälän työntekijä voi tarkastella kaikkia myymälälle määritettyjä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="60e9a-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="60e9a-109">He voivat myös päivittää heille määritettyjen tehtävien tilan.</span><span class="sxs-lookup"><span data-stu-id="60e9a-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="60e9a-110">Esimerkiksi myymäläpäälliköillä on oltava tehtävienhallinnan käyttöoikeudet, jotta he voivat hallita myymälälle määritettyjä tehtäviä ja luoda yhden tarkoituksen tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="60e9a-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="60e9a-111">Voit määrittää myymäläpäälliköiden tehtävienhallinnan käyttöoikeudet seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="60e9a-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="60e9a-112">Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttöoikeusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="60e9a-113">Valitse tietty käyttöoikeusryhmä (esimerkiksi **Päällikkö**) ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="60e9a-114">Määritä **Käyttöoikeudet**-pikavälilehdessä **Salli tehtävienhallinta** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="60e9a-115">Lisää **Ilmoitukset**-pikavälilehdessä **Tehtävienhallinta**-toiminto ja anna arvo **Näyttöjärjestys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60e9a-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="60e9a-116">Anna esimerkiksi arvo **2**, jos **Tilauksen täyttäminen** -toiminnon **Näyttöjärjestys**-kohdan arvo on jo **1**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="60e9a-117">Jos muulla kuin päälliköllä on oltava tehtävienhallinnan käyttöoikeudet myyntipisteessä, voit myöntää tälle henkilölle käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="60e9a-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="60e9a-118">Vaihtoehtoisesti voit luoda uuden käyttöoikeusryhmän muille kuin päälliköille ja määrittää **Salli tehtävienhallinta** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="60e9a-119">Seuraavassa kuvassa näkyy, miten myymäläpäälliköiden tehtävienhallinnan käyttöoikeudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="60e9a-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Myymäläpäälliköiden tehtävienhallinnan käyttöoikeuksien määrittäminen](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="60e9a-121">Työntekijöiden käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="60e9a-121">Configure permissions for employees</span></span>

<span data-ttu-id="60e9a-122">Työntekijöillä on oltava oikeus luoda tehtäväluetteloita, hallita määritysehtoja ja määrittää minkä tahansa tehtäväluettelon toistuminen.</span><span class="sxs-lookup"><span data-stu-id="60e9a-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="60e9a-123">Jos haluat määrittää nämä käyttöoikeudet, määritä työntekijöille **vähittäismyynnin tehtävienhallinnan** rooli.</span><span class="sxs-lookup"><span data-stu-id="60e9a-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="60e9a-124">Voit määrittää työntekijälle käyttöoikeudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60e9a-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="60e9a-125">Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="60e9a-126">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="60e9a-126">Select an employee.</span></span>
1. <span data-ttu-id="60e9a-127">Valitse **Käyttäjän roolit** -pikavälilehdessä **Määritä roolit**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="60e9a-128">Valitse **Määritä roolit käyttäjälle** -valintaikkunassa **vähittäismyynnin tehtävienhallinnan** rooli ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="60e9a-129">Käyttöoikeuksien jakelu myyntipisteen asiakassovelluksille</span><span class="sxs-lookup"><span data-stu-id="60e9a-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="60e9a-130">Ennen kuin työntekijät voivat käyttää myyntipisteen asiakassovelluksia, niille on jaettava käyttöoikeudet ja käyttöoikeudet on synkronoitava.</span><span class="sxs-lookup"><span data-stu-id="60e9a-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="60e9a-131">Voit jakaa myyntipisteen asiakassovellusten käyttöoikeudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60e9a-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="60e9a-132">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="60e9a-133">Valitse **1060** (**Henkilöstö**) -jakeluaikataulu ja valitse sitten **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="60e9a-134">Valitse **1070** (**Kanavan määritys**) -jakeluaikataulu ja valitse sitten **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="60e9a-135">Myyntipisteen ilmoitusten määrittäminen tehtäville</span><span class="sxs-lookup"><span data-stu-id="60e9a-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="60e9a-136">Tehtävienhallinta on määritettävä niin, että ilmoitukset ovat käytettävissä myyntipistesovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="60e9a-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="60e9a-137">Voit määrittää myyntipisteen ilmoitukset tehtäville seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60e9a-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="60e9a-138">Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="60e9a-139">Etsi toiminto **1400** (**Tehtävienhallinta**) ja valitse sen **Ota ilmoitukset käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="60e9a-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="60e9a-140">Seuraavassa kuvassa on **Tehtävienhallinta**-toiminto **Myyntipistetoiminnot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="60e9a-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Tehtävienhallintatoiminto Myyntipistetoiminnot-sivulla](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="60e9a-142">Lisärtietoja myyntipisteen ilmoitusten määrittämisestä on kohdassa [Tilausilmoitusten näyttäminen myyntipisteessä](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="60e9a-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="60e9a-143">Tehtävät-ruudun määrittäminen myyntipistesovelluksen aloitussivulla</span><span class="sxs-lookup"><span data-stu-id="60e9a-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="60e9a-144">Ennen kuin voit määrittää **Tehtävät**-ruudun myyntipistesovelluksen aloitussivulla, katso lisätietoja myyntipisteen näytön asettelun uusien painikkeiden määrittämisestä ja lisäämisestä kohdasta [Myyntipisteen näytön asettelut](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="60e9a-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="60e9a-145">Määritä **Tehtävät**-ruutu myyntipistesovelluksen aloitussivulla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60e9a-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="60e9a-146">Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="60e9a-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="60e9a-147">Valitse näytön asettelu. Valitse asettelun koko ja valitse sitten painikeruudukko.</span><span class="sxs-lookup"><span data-stu-id="60e9a-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="60e9a-148">Valitse **Painikeruudukot**-pikavälilehdessä **Suunnittelutoiminto**, jos haluat muokata valittua painikeruudukkoa.</span><span class="sxs-lookup"><span data-stu-id="60e9a-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="60e9a-149">Lisää **Tehtävät**-ruutu aloitussivun soveltuvaan osaan.</span><span class="sxs-lookup"><span data-stu-id="60e9a-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="60e9a-150">Seuraavassa kuvassa on esimerkki **Tehtävät**-ruudusta myyntipisteen aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="60e9a-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Myyntipisteen aloitussivun Tehtävät-ruutu](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="60e9a-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="60e9a-152">Additional resources</span></span>

[<span data-ttu-id="60e9a-153">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="60e9a-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="60e9a-154">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="60e9a-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="60e9a-155">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="60e9a-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="60e9a-156">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="60e9a-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
