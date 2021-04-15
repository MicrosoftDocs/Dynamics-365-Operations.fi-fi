---
title: Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta
description: Tässä aiheessa neuvotaan, miten sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 418586113c038c3227f0704495a561eac319bdc9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745084"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="35bc6-103">Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="35bc6-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35bc6-104">Tässä aiheessa kerrotaan, miten [sähköisen raportoinnin konfiguraatioiden](general-electronic-reporting.md#Configuration) uusin versio ladataan [jaetusta resurssikirjastosta](../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="35bc6-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="35bc6-105">Kirjaudu sovellukseen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="35bc6-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="35bc6-106">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="35bc6-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="35bc6-107">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="35bc6-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="35bc6-108">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="35bc6-108">System administrator</span></span>

2. <span data-ttu-id="35bc6-109">Valitse **Organisaation hallinto** &gt; **Työtilat** &gt; **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="35bc6-110">Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="35bc6-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="35bc6-111">Valitse **Microsoft**-ruudusta **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="35bc6-112">[![Microsoft-ruutu lokalisointien konfiguraatioiden sivulla](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="35bc6-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="35bc6-113">Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **LCS**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="35bc6-114">Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="35bc6-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="35bc6-115">Valitse säilö valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="35bc6-116">Valitse säilön tyypiksi **LCS**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="35bc6-117">Valitse **Luo säilö**.</span><span class="sxs-lookup"><span data-stu-id="35bc6-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="35bc6-118">Jos järjestelmä pyytää lupaa, noudata näyttöön tulevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="35bc6-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="35bc6-119">Kirjoita säilön nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="35bc6-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="35bc6-120">Valitse **OK**, jos haluat vahvistaa uuden säilön luonnin.</span><span class="sxs-lookup"><span data-stu-id="35bc6-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="35bc6-121">Valitse ruudukossa uusi **LCS**-tyypin säilö.</span><span class="sxs-lookup"><span data-stu-id="35bc6-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="35bc6-122">Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="35bc6-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="35bc6-123">[![Konfiguraatiosäilöjen sivu](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="35bc6-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="35bc6-124">Jos et voi käyttää LCS-säilöä ja ladata konfiguraatioita LCS:n jaetusta resurssikirjastosta, voit ladata ne sen sijaan [yleisestä säilöstä](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="35bc6-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="35bc6-125">Valitse vasemman ruudun konfiguraatioiden puurakenteessa vaadittu sähköisen raportoinnin konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="35bc6-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="35bc6-126">Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.</span><span class="sxs-lookup"><span data-stu-id="35bc6-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="35bc6-127">Valitse **Tuo** ja lataa valittu versio LCS-palvelusta nykyiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="35bc6-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35bc6-128">**Tuo**-painike ei ole käytettävissä ER-määritysversioille, jotka on jo ladattu nykyiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="35bc6-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="35bc6-129">[![Konfiguraatiosäilön sivu](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="35bc6-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="35bc6-130">ER-asetusten mukaan määritykset tarkistetaan tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="35bc6-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="35bc6-131">Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista.</span><span class="sxs-lookup"><span data-stu-id="35bc6-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="35bc6-132">Kyseiset ongelmat on ratkaistava, ennen kuin voit käyttää tuotua konfiguraatioversiota.</span><span class="sxs-lookup"><span data-stu-id="35bc6-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="35bc6-133">Lisätietoja saat tähän aiheeseen liittyvistä aiheista.</span><span class="sxs-lookup"><span data-stu-id="35bc6-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35bc6-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="35bc6-134">Additional resources</span></span>

[<span data-ttu-id="35bc6-135">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="35bc6-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="35bc6-136">Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta</span><span class="sxs-lookup"><span data-stu-id="35bc6-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]