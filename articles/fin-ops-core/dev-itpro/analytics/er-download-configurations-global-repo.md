---
title: Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta
description: Tässä ohjeaiheessa selitetään, miten sähköisiä raportointikokoonpanoja ladataan Configuration Service -palvelun yleisestä tietovarastosta.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c4f083163db72569d91825819a904319a0fe3123
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561899"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="3e488-103">Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta</span><span class="sxs-lookup"><span data-stu-id="3e488-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e488-104">Tässä ohjeaiheessa selitetään, miten [sähköisiä raportointikokoonpanoja](general-electronic-reporting.md#Configuration) ladataan palvelun yleisestä tietovarastosta.</span><span class="sxs-lookup"><span data-stu-id="3e488-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="3e488-105">Lisätietoja on kohdassa [Microsoft Dynamics 365 for Finance and Operations -Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="3e488-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="3e488-106">Konfiguraatiosäilön avaaminen</span><span class="sxs-lookup"><span data-stu-id="3e488-106">Open configurations repository</span></span>

1. <span data-ttu-id="3e488-107">Kirjaudu Dynamics 365 Finance -sovellukseen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="3e488-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="3e488-108">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="3e488-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="3e488-109">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="3e488-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="3e488-110">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="3e488-110">System administrator</span></span>

2. <span data-ttu-id="3e488-111">Valitse **Organisaation hallinto > Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="3e488-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="3e488-112">Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="3e488-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="3e488-113">Valitse **Microsoft**-ruudusta **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="3e488-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Sähköisen raportoinnin työtila](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="3e488-115">Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **Yleinen**.</span><span class="sxs-lookup"><span data-stu-id="3e488-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="3e488-116">Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="3e488-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="3e488-117">Valitse uusi säilö napsauttamalla **Lisää**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3e488-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="3e488-118">Valitse varastotyypiksi **Yleinen** ja valitse sitten **Luo säilö**.</span><span class="sxs-lookup"><span data-stu-id="3e488-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="3e488-119">Noudata luvananto-ohjeita tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="3e488-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="3e488-120">Kirjoita arkiston nimi ja kuvaus ja vahvista uusi tietovarastokohta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e488-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="3e488-121">Valitse ruudukossa uusi **Yleinen**-tyypin säilö.</span><span class="sxs-lookup"><span data-stu-id="3e488-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="3e488-122">Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="3e488-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Konfiguraatiosäilöjen sivu](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="3e488-124">Tuo yksi määritys</span><span class="sxs-lookup"><span data-stu-id="3e488-124">Import a single configuration</span></span>

1. <span data-ttu-id="3e488-125">**Valitse konfigurointisäilöt** -sivun konfiguraatiopuussa haluamasi ER-konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="3e488-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="3e488-126">Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.</span><span class="sxs-lookup"><span data-stu-id="3e488-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="3e488-127">Lataa valittu versio yleisestä säilöpalvelusta nykyiseen Finance-esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="3e488-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e488-128">**Tuo**-painike ei ole käytettävissä ER-määritysversioille, jotka on jo ladattu nykyiseen Finance-esiintymään.</span><span class="sxs-lookup"><span data-stu-id="3e488-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfiguraatiosäilön sivu](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="3e488-130">Tuo suodatetut määritykset</span><span class="sxs-lookup"><span data-stu-id="3e488-130">Import filtered configurations</span></span>

1. <span data-ttu-id="3e488-131">Laajenna **Konfigurointisäilöt** -sivun konfiguraatiot-puussa **Suodatin**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="3e488-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="3e488-132">Lisää tarvittavat Tunnisteet **Tunnisteet**-ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="3e488-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="3e488-133">Valitse **Maa- tai aluesoveltuvuus** -kentästä haluamasi maa-/aluekoodit ja valitse sitten **Käytä suodatinta**.</span><span class="sxs-lookup"><span data-stu-id="3e488-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e488-134">**Konfiguraatiot**-pikavälilehdessä näkyvät kaikki määritetyt valintaehdot täyttävät konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3e488-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="3e488-135">Lataa suodatetut konfiguraatiot yleisestä tietovarastosta nykyiseen esiintymään valitsemalla **Konfiguraatiot**-pikavälilehdessä **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="3e488-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="3e488-136">Voit tyhjentää määritetyt valintaehdot valitsemalla **Konfiguraatiot**-pikavälilehdessä **Nollaa suodatin**.</span><span class="sxs-lookup"><span data-stu-id="3e488-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfiguraatiosäilön sivu](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="3e488-138">ER-asetusten mukaan määritykset tarkistetaan tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3e488-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="3e488-139">Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista.</span><span class="sxs-lookup"><span data-stu-id="3e488-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="3e488-140">Ennen kuin voit käyttää tuotua konfiguraatioversiota, kyseiset ongelmat on ratkaistava.</span><span class="sxs-lookup"><span data-stu-id="3e488-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="3e488-141">Lisätietoja saat tähän aiheeseen liittyvistä resursseista.</span><span class="sxs-lookup"><span data-stu-id="3e488-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="3e488-142">ER-konfiguraatiot voidaan määrittää riippuvaisiksi muista konfiguraatioista.</span><span class="sxs-lookup"><span data-stu-id="3e488-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="3e488-143">Tämän vuoksi yhdessä valitun konfiguraation kanssa voidaan automaattisesti tuoda muita konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="3e488-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="3e488-144">Lisätietoja määritysten riippuvuuksista on kohdassa [ER-konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="3e488-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e488-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3e488-145">Additional resources</span></span>

[<span data-ttu-id="3e488-146">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3e488-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]