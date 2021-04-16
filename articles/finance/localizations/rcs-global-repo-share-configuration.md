---
title: RSC:n tai yleisen säilön ER-määritysten jakaminen ulkoisten organisaatioiden kanssa
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin tai yleisen säilön sähköisen raportoinnin (ER) määritysten jakamista suoraan ulkoisten organisaatioiden kanssa.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838742"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="3b32a-103">Microsoft Regulatory Configuration Servicesin yleisen säilön sähköisen raportoinnin (ER) määritysten jakaminen ulkoisten organisaatioiden kanssa</span><span class="sxs-lookup"><span data-stu-id="3b32a-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b32a-104">Microsoft Regulatory Configuration Servicesiä (RCS) voi käyttää sähköisen raportoinnin (ER) määritysten jakamiseen ja niiden julkaisemiseen ulkoisille organisaatioille.</span><span class="sxs-lookup"><span data-stu-id="3b32a-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="3b32a-105">Seuraavissa menettelyissä selitetään, miten RCS-käyttäjä voi jakaa RCS-esiintymässä määritetyn ER-määrityksen version ulkoisen organisaation kanssa.</span><span class="sxs-lookup"><span data-stu-id="3b32a-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="3b32a-106">Seuraavat ennakkoedellytykset on oltava suoritettuna, ennen kuin kyseiset menetelmät voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="3b32a-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="3b32a-107">RCS-esiintymän käyttäminen.</span><span class="sxs-lookup"><span data-stu-id="3b32a-107">Access an RCS instance.</span></span>
- <span data-ttu-id="3b32a-108">Aktiivisen määrityspalvelun luonti.</span><span class="sxs-lookup"><span data-stu-id="3b32a-108">Create an active configuration provider.</span></span> <span data-ttu-id="3b32a-109">Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3b32a-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="3b32a-110">Luo ja lataa ER-määrityksen uusi versio.</span><span class="sxs-lookup"><span data-stu-id="3b32a-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="3b32a-111">Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) määrityksen uuden version luominen ja lataaminen](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="3b32a-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="3b32a-112">Lisäksi on varmistettava, että RCS-ympäristö on valmisteltu yritykseen.</span><span class="sxs-lookup"><span data-stu-id="3b32a-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="3b32a-113">Valitse Finance and Operations -sovelluksessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3b32a-114">Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – ulkoinen määritys** -linkki ja valmistele sitten sellainen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3b32a-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="3b32a-115">Jos yritykseen on valmisteltu RCS-ympäristö, siirry siihen sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="3b32a-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="3b32a-116">Jaettavan määrityksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="3b32a-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="3b32a-117">Tarkista seuraavien ohjeiden avulla, että jaettava määritys on jo ladattu yleiseen säilöön.</span><span class="sxs-lookup"><span data-stu-id="3b32a-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="3b32a-118">Valitse **Sähköinen raportointi** -työtilassa oman määrityspalvelun **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfiguraation lähteet](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="3b32a-120">Valitse **Yleinen säilö** \> **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="3b32a-121">Hae jaettava määritys.</span><span class="sxs-lookup"><span data-stu-id="3b32a-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="3b32a-122">Voit tarkentaa hakua suodatinkentän avulla.</span><span class="sxs-lookup"><span data-stu-id="3b32a-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="3b32a-123">Jos määritystä ei löydy yleisestä säilöstä, noudata ohjeita kohdassa [Sähköisen raportoinnin (ER) määrityksen uuden version luominen ja lataaminen](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="3b32a-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="3b32a-124">ER-määritysten jakaminen ulkoisten organisaatioiden kanssa</span><span class="sxs-lookup"><span data-stu-id="3b32a-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="3b32a-125">Kun määritys on luotu määrityspalvelussa, voit jakaa sen suoraan ulkoisten organisaatioiden kanssa käyttämällä **Yleinen määrityssäilö** -sivun **Jaettu**-pikavälilehteä.</span><span class="sxs-lookup"><span data-stu-id="3b32a-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="3b32a-126">Valitse **Sähköinen raportointi** -työtilassa oman määrityspalvelun **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="3b32a-127">Valitse **Yleinen säilö** \> **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="3b32a-128">Valitse jaettava määritys.</span><span class="sxs-lookup"><span data-stu-id="3b32a-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="3b32a-129">Valitse **Jaettu**-pikavälilehdessä **Organisaatio**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Jaettu-pikavälilehti](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="3b32a-131">Anna valintaikkunassa ulkoisen organisaation toimialueen nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Jaa määritysversio ulkoisen organisaation kanssa -valintaikkuna](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="3b32a-133">Määritys jaetaan ulkoisen organisaation kanssa, ja se on kyseisen organisaation käytettävissä yleisessä säilössä.</span><span class="sxs-lookup"><span data-stu-id="3b32a-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="3b32a-134">Se voidaan tuoda sieltä organisaation RCS-esiintymään tai Finance and Operations -sovellusten esiintymiin.</span><span class="sxs-lookup"><span data-stu-id="3b32a-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="3b32a-135">Ulkoisen organisaation kanssa aiemmin jaetun määrityksen jakaminen poistetaan valitsemalla ensin määritys, sitten **Poista jako** ja lopuksi **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b32a-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]