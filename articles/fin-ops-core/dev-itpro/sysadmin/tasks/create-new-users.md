---
title: Uusien käyttäjien luominen
description: Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180941"
---
# <a name="create-new-users"></a><span data-ttu-id="b8fdb-103">Uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="b8fdb-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b8fdb-104">Käyttäjät ovat organisaation sisäisiä käyttäjiä tai ulkoisia asiakkaita ja toimittajia, jotka tarvitsevat järjestelmän käyttöoikeuden töidensä tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="b8fdb-105">Käyttäjän liittäminen käyttöoikeuteen (vain uudet käyttöoikeustyypit)</span><span class="sxs-lookup"><span data-stu-id="b8fdb-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="b8fdb-106">Sellaisten asiakkaiden käyttäjiin, joilla on jokin lokakuussa 2019 lisätyistä uusista käyttöoikeustyypeistä, on liitettävä käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="b8fdb-107">Käyttöoikeuteen liitetyt käyttäjät lisätään roolittomina järjestelmäkäyttäjinä, kun he kirjautuvat sisään ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="b8fdb-108">Käyttäjät, joihin ei ole liitetty käyttöoikeutta, saavat varoitussanoman.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="b8fdb-109">Järjestelmänvalvojat voivat [määrittää käyttöoikeuksia käyttäjille](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 -hallintakeskuksessa](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="b8fdb-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="b8fdb-110">Lisää uusi käyttäjä</span><span class="sxs-lookup"><span data-stu-id="b8fdb-110">Add a new user</span></span>
1. <span data-ttu-id="b8fdb-111">Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="b8fdb-112">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="b8fdb-113">Anna käyttäjän yksilöivä tunnus **Käyttäjätunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="b8fdb-114">Käyttäjätunnus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-114">A user ID is required.</span></span>  
4. <span data-ttu-id="b8fdb-115">Kirjoita käyttäjän nimi **Käyttäjän nimi** -kenttään toimittajan nimi.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="b8fdb-116">Kirjoita käyttäjän toimialue **Toimialue**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="b8fdb-117">Kirjoita käytättäjän alias **Alias**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="b8fdb-118">Valitse yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="b8fdb-119">[Määritä käyttöoikeusroolit käyttäjille](assign-users-security-roles.md) valitsemalla **Käyttäjän rooli** -pikavälilehdessä **Määritä rooleja**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="b8fdb-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-120">Select **OK**.</span></span>
10. <span data-ttu-id="b8fdb-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="b8fdb-122">Tuo käyttäjiä</span><span class="sxs-lookup"><span data-stu-id="b8fdb-122">Import users</span></span>
1. <span data-ttu-id="b8fdb-123">Valitse toimintoruudussa **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="b8fdb-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b8fdb-125">Valitse **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-125">Select **Import users**.</span></span>
4. <span data-ttu-id="b8fdb-126">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="b8fdb-126">Select **Close**.</span></span>

