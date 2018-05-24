---
title: "Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta"
description: "Tässä aiheessa neuvotaan, miten Microsoft Dynamics 365 for Operations -järjestelmän sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1a4e8c25fb65b35a52a0d1bc0f1a745c06ca53ab
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="469be-103">Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta</span><span class="sxs-lookup"><span data-stu-id="469be-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="469be-104">Tässä aiheessa neuvotaan, miten Microsoft Dynamics 365 for Operations -järjestelmän sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS).</span><span class="sxs-lookup"><span data-stu-id="469be-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="469be-105">Tässä oppaassa kuvataan uusimpien sähköisten raportoinnin (ER) konfiguraatioiden lataaminen Microsoft Dynamics Lifecycle Services -palvelusta (LCS).</span><span class="sxs-lookup"><span data-stu-id="469be-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="469be-106">Kirjaudu Finance and Operationsiin yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="469be-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="469be-107">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="469be-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="469be-108">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="469be-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="469be-109">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="469be-109">System administrator</span></span>

2.  <span data-ttu-id="469be-110">Siirry kohtaan **Organisaation hallinto** &gt; **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="469be-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="469be-111">Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="469be-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="469be-112">Napsauta **Microsoft**-ruudussa **Säilöt**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="469be-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="469be-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="469be-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="469be-114">Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **LCS**.</span><span class="sxs-lookup"><span data-stu-id="469be-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="469be-115">Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="469be-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="469be-116">Lisää uusi säilö napsauttamalla **Lisää**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="469be-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="469be-117">Valitse säilön tyypiksi **LCS**.</span><span class="sxs-lookup"><span data-stu-id="469be-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="469be-118">Valitse **Luo säilö**.</span><span class="sxs-lookup"><span data-stu-id="469be-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="469be-119">Noudata luvananto-ohjeita tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="469be-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="469be-120">Kirjoita säilön nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="469be-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="469be-121">Valitse **OK**, niin vahvistat uuden säilön luonnin.</span><span class="sxs-lookup"><span data-stu-id="469be-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="469be-122">Valitse ruudukossa uusi **LCS**-tyypin säilö.</span><span class="sxs-lookup"><span data-stu-id="469be-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="469be-123">Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="469be-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="469be-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="469be-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="469be-125">Valitse vasemman ruudun konfiguraatioiden puurakenteessa tarvitsemasi ER-konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="469be-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="469be-126">Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.</span><span class="sxs-lookup"><span data-stu-id="469be-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="469be-127">Lataa valittu versio LCS-palvelusta nykyiseen Finance and Operations -esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="469be-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="469be-128">**Huomautus:** **Tuo**-painike ei ole käytettävissä ER-konfiguraatioversioille, jotka on jo ladattu nykyiseen Finance and Operations -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="469be-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="469be-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="469be-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="469be-130">**Huomautus:** konfiguraatiot tarkistetaan tuonnin jälkeen ER-asetuksista riippuen.</span><span class="sxs-lookup"><span data-stu-id="469be-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="469be-131">Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista.</span><span class="sxs-lookup"><span data-stu-id="469be-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="469be-132">Kyseiset ongelmat on ratkaistava, ennen kuin voit käyttää tuotua konfiguraatioversiota.</span><span class="sxs-lookup"><span data-stu-id="469be-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="469be-133">Lisätietoja saat tähän aiheeseen liittyvistä artikkeleista.</span><span class="sxs-lookup"><span data-stu-id="469be-133">For more information, see the list of related articles for this topic.</span></span>

<a name="additional-resources"></a><span data-ttu-id="469be-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="469be-134">Additional resources</span></span>
--------

[<span data-ttu-id="469be-135">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="469be-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




