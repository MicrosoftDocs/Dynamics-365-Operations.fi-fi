---
title: Työtuntien hallinta
description: Tässä ohjeaiheessa kerrotaan työtuntien hallinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918369"
---
# <a name="work-hour-control"></a><span data-ttu-id="ea48f-103">Työtuntien hallinta</span><span class="sxs-lookup"><span data-stu-id="ea48f-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ea48f-104">Käyttöomaisuuden hallinnassa voit laskea tunteja, jolloin saat yleiskuvan todellisista tunneista resurssien, toiminnallisten sijaintien tai työtilausten budjettitunteihin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="ea48f-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="ea48f-105">Todelliset tunnit perustuvat kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="ea48f-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="ea48f-106">Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten työtuntien hallinta</span><span class="sxs-lookup"><span data-stu-id="ea48f-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="ea48f-107">Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset.</span><span class="sxs-lookup"><span data-stu-id="ea48f-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="ea48f-108">Ainoa ero on se, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa.</span><span class="sxs-lookup"><span data-stu-id="ea48f-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="ea48f-109">Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.</span><span class="sxs-lookup"><span data-stu-id="ea48f-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="ea48f-110">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssituntien hallinta** tai **Toiminnallisen sijainnin tuntien hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen tuntien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="ea48f-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="ea48f-111">**Resurssituntien hallinta** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="ea48f-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="ea48f-112">Valitse **Resurssituntien hallinta** / **Toiminnallisen sijainnin tuntien hallinta** / **Työtilauksen tuntien hallinta** -valintaikkunassa kausi, joka lasketaan **Päivämäärästä**- ja**Päivämäärään** -kenttien avulla.</span><span class="sxs-lookup"><span data-stu-id="ea48f-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="ea48f-113">Valitse tarvittaessa **Taloushallinnon dimensioyhdistelmä**, joka sisällytetään laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="ea48f-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="ea48f-114">Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla tuntia.</span><span class="sxs-lookup"><span data-stu-id="ea48f-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="ea48f-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia tuntien hallinnan riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="ea48f-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> <span data-ttu-id="ea48f-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin tuntien hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="ea48f-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="ea48f-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki tunetien hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="ea48f-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="ea48f-118">Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.</span><span class="sxs-lookup"><span data-stu-id="ea48f-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="ea48f-119">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ea48f-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="ea48f-120">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea48f-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="ea48f-121">Valitse **Resurssituntien hallinta** -sivun toimintoruudun **Ryhmittely ...**  -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="ea48f-121">On the **Asset hour control** page, in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="ea48f-122">Valitut toimintoruudun painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="ea48f-122">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="ea48f-123">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="ea48f-123">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="ea48f-124">Alla olevassa kuvassa on esimerkki **Resurssituntien hallinta** -laskennasta.</span><span class="sxs-lookup"><span data-stu-id="ea48f-124">The figure below shows an example of an **Asset hour control** calculation.</span></span>

![Kuva 1](media/04-controlling-and-reporting.png)

<span data-ttu-id="ea48f-126">Toinen tapa määrittää tuntilaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="ea48f-126">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="ea48f-127">Napsauta sitten **Yleiset**-pikavälilehden **Tuntien hallinta** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="ea48f-127">Then, you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="ea48f-128">Valitut resurssit lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea48f-128">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="ea48f-129">Valitse **Resurssituntien hallinta** -valintaikkunassa **OK** ja näkyviin tulee valittujen käyttöomaisuuserien laskelma.</span><span class="sxs-lookup"><span data-stu-id="ea48f-129">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="ea48f-130">Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="ea48f-130">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="ea48f-131">**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut tunnit.</span><span class="sxs-lookup"><span data-stu-id="ea48f-131">The **Original budget** field shows budget hours from the work order forecast.</span></span> <span data-ttu-id="ea48f-132">**Todelliset tunnit** -kentässä näkyvät työtilausten kirjatut tunnit.</span><span class="sxs-lookup"><span data-stu-id="ea48f-132">The **Actual hours** field shows posted hours on work orders.</span></span> <span data-ttu-id="ea48f-133">**Varatut tunnit** -kentässä näkyvät kokonaistunnit, joihin yritys on sitoutunut suhteessa työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ea48f-133">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

