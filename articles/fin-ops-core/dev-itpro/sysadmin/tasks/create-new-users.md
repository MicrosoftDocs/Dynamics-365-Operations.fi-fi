---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679837"
---
# <a name="create-new-users"></a><span data-ttu-id="f75e9-103">Uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="f75e9-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f75e9-104">Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="f75e9-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f75e9-105">Käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)</span><span class="sxs-lookup"><span data-stu-id="f75e9-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="f75e9-106">Sellaisten asiakkaiden käyttäjiin, joilla on jokin lokakuussa 2019 lisätyistä uusista käyttöoikeustyypeistä, on liitettävä käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="f75e9-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="f75e9-107">Käyttöoikeuteen liitetyt käyttäjät lisätään roolittomina järjestelmäkäyttäjinä, kun he kirjautuvat sisään ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="f75e9-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="f75e9-108">Järjestelmänvalvojat voivat [määrittää käyttöoikeuksia käyttäjille](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="f75e9-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f75e9-109">Ulkoisen käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)</span><span class="sxs-lookup"><span data-stu-id="f75e9-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="f75e9-110">Sen vuokraajan ulkopuolisten käyttäjien, jolla ympäristö otettiin käyttöön, on oltava edustettuna isännän vuokraajahakemistossa (Azure Active Directory (Azure AD)), jotta käyttäjille voidaan myöntää käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="f75e9-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="f75e9-111">Nämä ulkoiset käyttäjät on lisättävä vuokraajalle Azure AD:ssä vieraskäyttäjinä, minkä jälkeen käyttäjille on määritettävä asianmukaiset käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="f75e9-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="f75e9-112">Lisätietoja on kohdassa [Lisää Azure Active Directoryn B2B-yhteistyön käyttäjiä Azure-portaaliin](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="f75e9-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="f75e9-113">Lisää uusi käyttäjä</span><span class="sxs-lookup"><span data-stu-id="f75e9-113">Add a new user</span></span>
1. <span data-ttu-id="f75e9-114">Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f75e9-115">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f75e9-116">Anna käyttäjän yksilöivä tunnus **Käyttäjätunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f75e9-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="f75e9-117">Käyttäjätunnus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="f75e9-117">A user ID is required.</span></span>  
4. <span data-ttu-id="f75e9-118">Kirjoita käyttäjän nimi **Käyttäjän nimi** -kenttään toimittajan nimi.</span><span class="sxs-lookup"><span data-stu-id="f75e9-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="f75e9-119">Kirjoita käyttäjän toimialue **Toimialue**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f75e9-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="f75e9-120">Kirjoita käytättäjän alias **Alias**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f75e9-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="f75e9-121">Valitse yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f75e9-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="f75e9-122">Määritä käyttöoikeusroolit käyttäjille valitsemalla **Käyttäjän rooli** -pikavälilehdessä **Määritä rooleja**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="f75e9-123">Lisätietoja on kohdassa [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f75e9-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="f75e9-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-124">Select **OK**.</span></span>
10. <span data-ttu-id="f75e9-125">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="f75e9-126">Tuo käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="f75e9-126">Import users</span></span>
1. <span data-ttu-id="f75e9-127">Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f75e9-128">Valitse toimintoruudussa **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="f75e9-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f75e9-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f75e9-130">Valitse **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-130">Select **Import users**.</span></span>
5. <span data-ttu-id="f75e9-131">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="f75e9-131">Select **Close**.</span></span>

