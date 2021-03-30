---
title: Kunnon arviointi
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda kuntoarviointimallin ja rekisteröinnin resurssiin resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d84520413659db32713711ad5ac980f1e8b5519
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217170"
---
# <a name="condition-assessment"></a><span data-ttu-id="63783-103">Kunnon arviointi</span><span class="sxs-lookup"><span data-stu-id="63783-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="63783-104">Tässä ohjeaiheessa kerrotaan, kuinka voit luoda kuntoarviointimallin ja rekisteröinnin resurssiin resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="63783-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="63783-105">Kunnon arviointi suoritetaan säännöllisin väliajoin, ja ensisijaisena tavoitteena on luoda ja ylläpitää resurssien kuntotietoja.</span><span class="sxs-lookup"><span data-stu-id="63783-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="63783-106">Ennakoivan kunnossapidon näkökulmasta katsottuna on tärkeää valvoa keskeisiä tietoja, kuten nykykuntoa ja jäljellä olevaa elinikää.</span><span class="sxs-lookup"><span data-stu-id="63783-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="63783-107">Lisäksi, jos teet kunnon arvioinnin säännöllisin väliajoin, pystyt seuraamaan ja vertailemaan tehtaasi koneiden kuntoa.</span><span class="sxs-lookup"><span data-stu-id="63783-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="63783-108">Kunnon arvioinnin avulla voidaan mitata ja valvoa monia laitteiston kunnon osa-alueita.</span><span class="sxs-lookup"><span data-stu-id="63783-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="63783-109">Esimerkki: Voit mitata koneen tärinää.</span><span class="sxs-lookup"><span data-stu-id="63783-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="63783-110">Kun olet rekisteröinyt resurssien hallinnassa värähtelymittauksia erityyppisille laitteille, voit etsiä viimeisintä rekisteröityä arviointia ja tarkastella tärinän mittauksia.</span><span class="sxs-lookup"><span data-stu-id="63783-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="63783-111">Kunnon arvioinnit luodaan resursseille.</span><span class="sxs-lookup"><span data-stu-id="63783-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="63783-112">Voit määrittää kuunon arviointimallin resurssityypille ennen kuntoarviointimenettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="63783-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="63783-113">Syy arviointimallien käyttämiseen on välttää samanlaisiin resursseihin kuuluvien kuntotietojen vaihtelu.</span><span class="sxs-lookup"><span data-stu-id="63783-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="63783-114">Kunnon arvioinnin määrittäminen ja käyttäminen järjestys resurssien hallinnassa on: ensin määritetään tarvittavat kunnon arviointimallit.</span><span class="sxs-lookup"><span data-stu-id="63783-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="63783-115">Liitä seuraavaksi mallit liitetään resurssityyppeihin **Resurssityypit**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="63783-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="63783-116">Lopuksi voit luoda kunnon arvioinnin rekisteröinnit resurssille **resurssi**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="63783-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="63783-117">Luo kunnon arviointimalli</span><span class="sxs-lookup"><span data-stu-id="63783-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="63783-118">Valitse **resurssien hallinta** > **Asetukset** > **resurssityypit** > **Kunnon arviointi**.</span><span class="sxs-lookup"><span data-stu-id="63783-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="63783-119">Luo uusi malli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="63783-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="63783-120">Kirjoita **Malli**-kenttään mallin tunnus.</span><span class="sxs-lookup"><span data-stu-id="63783-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="63783-121">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="63783-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="63783-122">Lisää **Kunnon arviointirivit** -pikavälilehdessä kunnon arviointiin tarvittavat rivit, mukaan lukien asianmukaisen kuntotyypin ja mittayksikön valinta.</span><span class="sxs-lookup"><span data-stu-id="63783-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="63783-123">Lisää **resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi käyttää kunnon arviointimallia.</span><span class="sxs-lookup"><span data-stu-id="63783-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="63783-124">Näytön yläreunassa olevan **Tiedot** -ryhmän kentissä **rivit** ja **resurssityypit** näkyy valittuun kunnon arviointimalliin liittyvien arviointirivien ja resurssityyppien määrä.</span><span class="sxs-lookup"><span data-stu-id="63783-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="63783-125">Luo resurssille kunnon arvioinnin rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="63783-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="63783-126">Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="63783-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="63783-127">Valitse luettelosta resurssi, jolle haluat luoda kunnon arvioinnin rekisteröinnin.</span><span class="sxs-lookup"><span data-stu-id="63783-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="63783-128">Valitse **Yleiset**-välilehdestä **Kunnon arviointi**.</span><span class="sxs-lookup"><span data-stu-id="63783-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="63783-129">Lisää uusi rekisteröinti valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="63783-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="63783-130">Valitse kunnon arvioinnin päivämäärä **Päivämäärä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63783-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="63783-131">Valitse työntekijä, joka suoritti arvioinnin rekisteröinnin **Työntekijä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63783-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="63783-132">**Rivit**-kentässä näkyy kunnon arviointiin asetettujen arviointirivien määrä.</span><span class="sxs-lookup"><span data-stu-id="63783-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="63783-133">Valitse kunnon arvioinnin malli **Malli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63783-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="63783-134">Mallin nimi lisätään automaattisesti **nimi**-kenttään, ja siihen liittyvät rekisteröintirivit lisätään **Kunnon arviointirivit** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="63783-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="63783-135">Voit lisätä valittuun kunnon arviointiin liittyviä muistiinpanoja **Huomautukset**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="63783-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="63783-136">Lisää jokaiselle kunnon arviointiriville mittaustiedot **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63783-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="63783-137">Voit lisätä valittuun rekisteröintiriviin liittyvän kommentin **Kunnon arviointirivit** -pikavälilehden **Kommentit**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="63783-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="63783-138">Jos lisäät riville kommentin, **Kommentti**-valintaruutu valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="63783-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="63783-139">Kun olet tehnyt kunnon arvioinnin rekisteröinnin resurssille, voit tulostaa kunnon arviointiraportin.</span><span class="sxs-lookup"><span data-stu-id="63783-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="63783-140">Voit myös rekisteröidä kunnon arvioinnintyötilaukselle (**resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** > **Kunnon arviointi** -painike).</span><span class="sxs-lookup"><span data-stu-id="63783-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]