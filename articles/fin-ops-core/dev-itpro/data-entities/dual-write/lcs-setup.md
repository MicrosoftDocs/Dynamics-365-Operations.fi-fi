---
title: Kaksoiskirjoituksen asetukset Lifecycle Services -sovelluksessa
description: Tässä ohjeaiheessa kerrotaan, miten kaksoiskirjoitusyhteys määritetään uuden Finance and Operations -ympäristön ja uuden Common Data Service -ympäristön välille Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172989"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="2ee55-103">Kaksoiskirjoituksen asetukset Lifecycle Services -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="2ee55-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="2ee55-104">Tässä ohjeaiheessa kerrotaan, miten kaksoiskirjoitusyhteys määritetään uuden Finance and Operations -ympäristön ja uuden Common Data Service -ympäristön välille Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2ee55-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ee55-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="2ee55-105">Prerequisites</span></span>

<span data-ttu-id="2ee55-106">Vain järjestelmänvalvoja voi määrittää kaksoiskirjoitusyhteyden.</span><span class="sxs-lookup"><span data-stu-id="2ee55-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="2ee55-107">Sinulla on oltava käyttöoikeus vuokraajaan.</span><span class="sxs-lookup"><span data-stu-id="2ee55-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="2ee55-108">Sinun on oltava järjestelmänvalvoja sekä Finance and Operations- että Common Data Service -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="2ee55-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="2ee55-109">Kaksoiskirjoitusyhteyden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2ee55-109">Set up a dual-write connection</span></span>

<span data-ttu-id="2ee55-110">Näiden ohjeiden avulla voit määrittää kaksoiskirjoitusyhteyden.</span><span class="sxs-lookup"><span data-stu-id="2ee55-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="2ee55-111">Siirry LCS-sovelluksessa projektiin.</span><span class="sxs-lookup"><span data-stu-id="2ee55-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="2ee55-112">Ota uusi ympäristö käyttöön valitsemalla **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="2ee55-113">Valitse versio.</span><span class="sxs-lookup"><span data-stu-id="2ee55-113">Select the version.</span></span> 
4. <span data-ttu-id="2ee55-114">Valitse topologia.</span><span class="sxs-lookup"><span data-stu-id="2ee55-114">Select the topology.</span></span> <span data-ttu-id="2ee55-115">Jos käytettävissä on vain yksi topologia, se valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="2ee55-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="2ee55-116">Suorita ensimmäiset vaiheet ohjatussa **Käyttöönoton asetukset** -toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="2ee55-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="2ee55-117">Tee jokin seuraavista vaiheista **Common Data Service** -välilehdessä:</span><span class="sxs-lookup"><span data-stu-id="2ee55-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="2ee55-118">Jos Common Data Service -ympäristö on jo valmisteltu vuokraajaa varten, voit valita sen.</span><span class="sxs-lookup"><span data-stu-id="2ee55-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="2ee55-119">Määritä **Määritä Common Data Service** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="2ee55-120">Valitse **Käytettävissä olevat ympäristöt** -kentässä Finance and Operations -tietojen kanssa integroitava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="2ee55-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="2ee55-121">Luettelo sisältää kaikki ympäristöt, joiden järjestelmänvalvojan oikeudet sinulla on.</span><span class="sxs-lookup"><span data-stu-id="2ee55-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="2ee55-122">Valitse **Hyväksyn**-valintaruutu, jolloin hyväksyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="2ee55-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service -välilehti, kun Common Data Service -ympäristö on jo valmisteltu vuokraajaa varten](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="2ee55-124">Jos vuokraajalla ei vielä ole Common Data Service -ympäristöä, uusi ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="2ee55-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="2ee55-125">Määritä **Määritä Common Data Service** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="2ee55-126">Anna Common Data Service -ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="2ee55-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="2ee55-127">Valitse alue, johon ympäristö otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2ee55-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="2ee55-128">Valitse ympäristön oletuskieli ja -valuutta.</span><span class="sxs-lookup"><span data-stu-id="2ee55-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="2ee55-129">Et voi muuttaa kieltä ja valuuttaa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="2ee55-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="2ee55-130">Valitse **Hyväksyn**-valintaruutu, jolloin hyväksyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="2ee55-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service -välilehti, kun vuokraajalla ei ole Common Data Service -ympäristöä](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="2ee55-132">Suorita jäljellä olevat vaiheet ohjatussa **Käyttöönoton asetukset** -toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="2ee55-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="2ee55-133">Kun ympäristön tila on **Otettu käyttöön**, avaa ympäristön tietojen sivu.</span><span class="sxs-lookup"><span data-stu-id="2ee55-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="2ee55-134">**Common Data Service -ympäristön tiedot** -osassa on linkitettyjen Finance and Operations- ja Common Data Service -ympäristöjen nimet.</span><span class="sxs-lookup"><span data-stu-id="2ee55-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service -ympäristön tietojen osa](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="2ee55-136">Finance and Operations -ympäristön järjestelmänvalvojan on kirjauduttava sisään LCS-sovellukseen ja valittava **Linkitä CDS for Apps -sovellukseen**, jotta linkitys on valmis.</span><span class="sxs-lookup"><span data-stu-id="2ee55-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="2ee55-137">Ympäristön tietojen sivulla näkyvät järjestelmänvalvojan yhteystiedot.</span><span class="sxs-lookup"><span data-stu-id="2ee55-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="2ee55-138">Kun linkki on valmis, tilaksi päivitetään **Ympäristön linkitys on suoritettu onnistuneesti**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="2ee55-139">Voit avata **Tietojen integrointi** -työtilan Finance and Operations -ympäristössä ja hallinnoida käytettävissä olevia malleja valitsemalla **Linkitä CDS for Apps -sovellukseen**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Linkitä CDS for Apps -sovellukseen -painike Common Data Service -ympäristön tietojen osassa](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="2ee55-141">Et voi poistaa ympäristöjen välistä linkitystä LCS-sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="2ee55-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="2ee55-142">Jos haluat poistaa linkityksen, avaa **Tietojen integrointi** -työtila Finance and Operations -ympäristössä ja valitse sitten **Poista linkitys**.</span><span class="sxs-lookup"><span data-stu-id="2ee55-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
