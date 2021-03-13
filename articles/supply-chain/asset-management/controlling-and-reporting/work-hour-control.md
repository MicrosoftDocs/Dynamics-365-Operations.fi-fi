---
title: Työtuntien hallinta
description: Tässä ohjeaiheessa kerrotaan työtuntien hallinnasta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc4382d72e032fdfad05f2077ffe8e41e64c6a55
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018468"
---
# <a name="work-hour-control"></a><span data-ttu-id="99c13-103">Työtuntien hallinta</span><span class="sxs-lookup"><span data-stu-id="99c13-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="99c13-104">Käyttöomaisuuden hallinnassa voit laskea tunteja, jolloin saat yleiskuvan todellisista tunneista resurssien, toiminnallisten sijaintien tai työtilausten budjettitunteihin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="99c13-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="99c13-105">Todelliset tunnit perustuvat kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="99c13-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="99c13-106">Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten työtuntien hallinta</span><span class="sxs-lookup"><span data-stu-id="99c13-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="99c13-107">Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset.</span><span class="sxs-lookup"><span data-stu-id="99c13-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="99c13-108">Ainoa ero on se, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa.</span><span class="sxs-lookup"><span data-stu-id="99c13-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="99c13-109">Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.</span><span class="sxs-lookup"><span data-stu-id="99c13-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="99c13-110">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssituntien hallinta** tai **Toiminnallisen sijainnin tuntien hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen tuntien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="99c13-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="99c13-111">**Resurssituntien hallinta** -valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="99c13-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="99c13-112">Valitse **Resurssituntien hallinta** / **Toiminnallisen sijainnin tuntien hallinta** / **Työtilauksen tuntien hallinta** -valintaikkunassa kausi, joka lasketaan **Päivämäärästä**- ja **Päivämäärään** -kenttien avulla.</span><span class="sxs-lookup"><span data-stu-id="99c13-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="99c13-113">Valitse tarvittaessa **Taloushallinnon dimensioyhdistelmä**, joka sisällytetään laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="99c13-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="99c13-114">Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla tuntia.</span><span class="sxs-lookup"><span data-stu-id="99c13-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="99c13-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia tuntien hallinnan riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="99c13-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="99c13-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin tuntien hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="99c13-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="99c13-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki tunetien hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="99c13-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="99c13-118">Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.</span><span class="sxs-lookup"><span data-stu-id="99c13-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="99c13-119">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99c13-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="99c13-120">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="99c13-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="99c13-121">Napsauta **Resurssituntien hallinta** -sivulla **Ryhmittele**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="99c13-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="99c13-122">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="99c13-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="99c13-123">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="99c13-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="99c13-124">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="99c13-124">Example</span></span>

<span data-ttu-id="99c13-125">Alla olevassa näyttökuvassa on esimerkki **Resurssituntien hallinta** -laskennasta.</span><span class="sxs-lookup"><span data-stu-id="99c13-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="99c13-126">**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut tunnit.</span><span class="sxs-lookup"><span data-stu-id="99c13-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="99c13-127">**Todelliset tunnit** -kentässä näkyvät työtilausten kirjatut tunnit.</span><span class="sxs-lookup"><span data-stu-id="99c13-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="99c13-128">**Varatut tunnit** -kentässä näkyvät kokonaistunnit, joihin yritys on sitoutunut suhteessa työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="99c13-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Esimerkki Resurssituntien hallinnan laskennasta](media/04-controlling-and-reporting.png)

<span data-ttu-id="99c13-130">Toinen tapa määrittää tuntilaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="99c13-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="99c13-131">Napsauta sitten **Yleiset**-pikavälilehden **Tuntien hallinta** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="99c13-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="99c13-132">Valitut resurssit lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="99c13-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="99c13-133">Valitse **Resurssituntien hallinta** -valintaikkunassa **OK** ja näkyviin tulee valittujen käyttöomaisuuserien laskelma.</span><span class="sxs-lookup"><span data-stu-id="99c13-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="99c13-134">Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="99c13-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


