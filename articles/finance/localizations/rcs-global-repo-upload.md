---
title: ER-määritysten luominen RCS:ssä ja niiden lataaminen yleiseen säilöön
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) sähköisen raportoinnin (ER) määrityksen luomista ja lataamista yleiseen säilöön.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834230"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="8a869-103">ER-määritysten luominen Regulatory Configuration Servicesissä (RCS) ja niiden lataaminen yleiseen säilöön</span><span class="sxs-lookup"><span data-stu-id="8a869-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a869-104">Microsoft Regulatory Configuration Servicesiä (RCS) voi käyttää sähköisen raportoinnin (ER) määritysten suunnitteluun ja niiden julkaisemiseen organisaatiossa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="8a869-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="8a869-105">Seuraavissa menettelyissä käsitellään tapaa, jolla järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda johdetun version RCS-esiintymässä määritetystä ER-määrityksestä ja jolla johdettu määritys sitten ladataan yleiseen säilöön.</span><span class="sxs-lookup"><span data-stu-id="8a869-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="8a869-106">Seuraavat ennakkoedellytykset on oltava suoritettuna, ennen kuin kyseiset menetelmät voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="8a869-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="8a869-107">RCS-esiintymän käyttäminen.</span><span class="sxs-lookup"><span data-stu-id="8a869-107">Access an RCS instance.</span></span>
- <span data-ttu-id="8a869-108">Aktiivisen määrityspalvelun luonti.</span><span class="sxs-lookup"><span data-stu-id="8a869-108">Create an active configuration provider.</span></span> <span data-ttu-id="8a869-109">Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8a869-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="8a869-110">Lisäksi on varmistettava, että RCS-ympäristö on valmisteltu yritykseen.</span><span class="sxs-lookup"><span data-stu-id="8a869-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="8a869-111">Valitse Finance and Operations -sovelluksessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="8a869-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="8a869-112">Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – ulkoinen määritys** -linkki ja valmistele sitten sellainen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8a869-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="8a869-113">Jos yritykseen on valmisteltu RCS-ympäristö, siirry siihen sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="8a869-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="8a869-114">Määrityksen johdetun version luominen RCS:ssä</span><span class="sxs-lookup"><span data-stu-id="8a869-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="8a869-115">Varmista **Sähköinen raportointi** -työtilassa, että organisaatiossa on aktiviinen määrityspalvelu.</span><span class="sxs-lookup"><span data-stu-id="8a869-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="8a869-116">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="8a869-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8a869-117">Valitse määritys, josta haluat johtaa uuden version.</span><span class="sxs-lookup"><span data-stu-id="8a869-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="8a869-118">Voit tarkentaa hakua käyttämällä puun yläpuolella olevaa suodatinkenttää.</span><span class="sxs-lookup"><span data-stu-id="8a869-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="8a869-119">Valitse **Luo konfiguraatio** \> **Johda nimestä**.</span><span class="sxs-lookup"><span data-stu-id="8a869-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="8a869-120">Anna nimi ja kuvaus ja luo sitten uusi johdettu versio valitsemalla **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="8a869-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="8a869-121">Valitse juuri johdettu konfiguraatio, lisää version kuvaus ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a869-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="8a869-122">Konfiguraation tila muuttuu ja uusi tila on **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="8a869-122">The status of the configuration to is changed to **Completed**.</span></span>

![Uusi RCS:n määritysversio](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="8a869-124">Kun määrityksen tila on muuttuu, yhdistettyihin sovelluksiin liittyvä tarkistusvirhesanoma voi tulla näkyviin.</span><span class="sxs-lookup"><span data-stu-id="8a869-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="8a869-125">Tarkistuksen voi poistaa käytöstä valitsemalla toimintoruudun **Konfiguraatiot**-välilehdessä **Käyttäjän parametrit** ja määrittämällä sitten **Ohita konfiguraation tilamuutoksen aikainen tarkistus ja perustaa uudelleen** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8a869-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="8a869-126">Määrityksen lataaminen yleiseen säilöön</span><span class="sxs-lookup"><span data-stu-id="8a869-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="8a869-127">Uusi tai johdettu määritys jaetaan organisaatiossa lataamalla se yleiseen säilöön.</span><span class="sxs-lookup"><span data-stu-id="8a869-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="8a869-128">Valitse ensin määrityksen valmis versio ja sitten **Lataa säilöön**.</span><span class="sxs-lookup"><span data-stu-id="8a869-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="8a869-129">Valitse ensin **Yleinen (Microsoft)** -vaihtoehto ja sitten **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="8a869-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Säilöön lataamisen asetukset](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="8a869-131">Valitse vahvistussanomaikkunassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8a869-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="8a869-132">Päivitä version kuvaus tarpeen mukaan ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a869-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="8a869-133">Määrityksen tilaksi päivitetään **Jako** ja määritys ladataan yleiseen säilöön.</span><span class="sxs-lookup"><span data-stu-id="8a869-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="8a869-134">Määritystä voi käyttää säilössä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8a869-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="8a869-135">Tuonti Dynamics 365 -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="8a869-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="8a869-136">Lisätietoja on kohdassa [(ER) Konfiguraatioiden tuonti RCS:stä](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)</span><span class="sxs-lookup"><span data-stu-id="8a869-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="8a869-137">Lisätietoja jakamisesta kolmannen osapuolen tai ulkoisen organisaation kanssa on kohdassa [RCS:n ulkoisten organisaatioiden kanssa jakamat sähköisen raportoinnin (ER) määritykset](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="8a869-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Johdettu Intrastat Contoso -määritysversio yleisessä säilössä.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="8a869-139">Poista määritys yleisestä säilöstä</span><span class="sxs-lookup"><span data-stu-id="8a869-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="8a869-140">Suorita seuraavat vaiheet poistaaksesi määrityksen, jonka organisaatiosi on luonut.</span><span class="sxs-lookup"><span data-stu-id="8a869-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="8a869-141">Varmista **Sähköinen raportointi** -työtilassa, että määrityspalvelusi on **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="8a869-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="8a869-142">Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8a869-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="8a869-143">Valitse aktiivisessa määrityspalvelussa **säilö**.</span><span class="sxs-lookup"><span data-stu-id="8a869-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="8a869-144">Valitse säilötyyppi **Yleinen** ja sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="8a869-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="8a869-145">Etsi poistettava määritys **Suodatin**-pikavälilehdessä käyttämällä **Suodata**-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="8a869-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="8a869-146">Valitse **Versio**-pikavälilehdessä määrityksen poistettava versio ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="8a869-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Määrityksen poistaminen yleisestä säilöstä](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="8a869-148">Valitse vahvistussanomaikkunassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8a869-148">In the confirmation message box, select **Yes**.</span></span>

    ![Määritysversion vahvistusviestin poistaminen](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="8a869-150">Määritysversio poistetaan ja vahvistusviesti näytetään.</span><span class="sxs-lookup"><span data-stu-id="8a869-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="8a869-151">Vain määritykset luonut määrityspalvelu voi poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="8a869-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="8a869-152">Jos määritys on jaettu toisen organisaation kanssa, määrityksen jakaminen on peruutettava ennen poistamista.</span><span class="sxs-lookup"><span data-stu-id="8a869-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
