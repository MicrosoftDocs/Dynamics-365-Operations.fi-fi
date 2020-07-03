---
title: Tehtävätallenteiden suojausdiagnostiikka
description: Tässä ohjeaiheessa on tietoja siitä, miten voidaan analysoida ja hallita tehtävän tallennukseen perustuvia käyttöoikeusvaatimuksia.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: fada3abb9362426c7c9ec33f5d25552edf3ef630
ms.sourcegitcommit: 71fec2553158c332ce4d4bfcedc2c1ab58c1a1a5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340672"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="0a4ae-103">Tehtävätallenteiden suojausdiagnostiikka</span><span class="sxs-lookup"><span data-stu-id="0a4ae-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="0a4ae-104">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="0a4ae-104">Before you begin</span></span>

<span data-ttu-id="0a4ae-105">Tässä ohjeaiheessa on tietoja siitä, miten voidaan analysoida ja hallita tehtävän tallennukseen perustuvia käyttöoikeusvaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="0a4ae-106">Ennen tämän ohjeaiheen vaiheiden suorittamista sinun on määritettävä analysoitavan liiketoimintaprosessin tehtävätallennus.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="0a4ae-107">Jos haluat tallentaa liiketoimintaprosessin, katso [Tehtävän tallennusresurssit](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="0a4ae-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="0a4ae-108">Tehtävätallenteen suojauksenhallinta</span><span class="sxs-lookup"><span data-stu-id="0a4ae-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="0a4ae-109">Siirry kohtaan **Järjestelmänhallinta** > **Suojaus** > **Suojauksen vianmääritys tehtävätallennusta varten**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="0a4ae-110">Avaa tehtävätallennus sen sijainnista.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-110">Open the task recording from its location.</span></span> <span data-ttu-id="0a4ae-111">Valitse **Avaa tästä tietokoneesta** tai **Avaa Lifecycle Servicesistä** ja valitse sitten **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="0a4ae-112">Tämä avaa **Suojausvalikkovaihtoehdon tiedot** -sivun, jossa luetellaan prosessin edellyttämät suojausobjektit.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="0a4ae-113">**Toiminto**- ja **Tuloste**-valikon vaihtoehdot eivät sisälly luetteloon.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="0a4ae-114">Valitse käyttäjä **Käyttäjätunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="0a4ae-115">Jos käyttäjällä ei ole joidenkin valikkovaihtoehtojen käyttöoikeuksia, **Puuttuvat käyttöoikeudet** -kentän arvoksi päivittyy **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Suojausvalikkokohteen tiedot -sivu](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="0a4ae-117">Valitse **Lisää viite**, jos haluat nähdä luettelon suojausobjekteista, kuten rooleista, velvollisuuksista ja oikeuksista, jotka myöntävät puuttuvan käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="0a4ae-118">Valitse luettelosta suojausobjekti:</span><span class="sxs-lookup"><span data-stu-id="0a4ae-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="0a4ae-119">Jos **Rooli** on valittuna, valitse **Lisää rooli käyttäjään**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="0a4ae-120">Tämä avaa **Määritä käyttäjät rooleihin** -sivun.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="0a4ae-121">Lisätietoja on [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md) -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="0a4ae-122">Jos valittuna on **Velvollisuus**, valitse **Lisää velvollisuus rooliin**, valitse roolit, joihin vero lisätään, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="0a4ae-123">Jos valittuna on **Oikeus**, valitse **Lisää oikeus velvollisuuksiin**, valitse roolit, joihin vero lisätään, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4ae-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>