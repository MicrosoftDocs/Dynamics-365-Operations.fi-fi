---
title: Resurssien vika-analyysi
description: Tässä ohjeaiheessa kerrotaan resurssivikojen analyysista resurssien hallinnassa.
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
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918438"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="5ef39-103">Resurssien vika-analyysi</span><span class="sxs-lookup"><span data-stu-id="5ef39-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5ef39-104">Käyttöomaisuuden hallinnassa voit analysoida käyttöomaisuuden vikamerkintöjä, jolloin saat yleiskuvan tietyn kauden aikana rekisteröityjen vikojen kokonaismäärästä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="5ef39-105">Vikarekisteröintejä voidaan analysoida eri näkökulmista, esimerkiksi resurssien, resurssityyppien, toiminnallisten sijaintien, vian oireiden tai vikatyyppien näkökulmista.</span><span class="sxs-lookup"><span data-stu-id="5ef39-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="5ef39-106">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen analyysi**.</span><span class="sxs-lookup"><span data-stu-id="5ef39-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="5ef39-107">**Resurssin vika-analyysin laskenta** -valintaikkunassa voit määrittää **Taso** -kentän avulla, miten yksityiskohtaisia haluat käyttöomaisuusvirherivien olevan toiminnallisia sijainteja ajatellen.</span><span class="sxs-lookup"><span data-stu-id="5ef39-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="5ef39-108">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssivikarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="5ef39-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="5ef39-109">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="5ef39-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="5ef39-110">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät, virheiden syyt ja vikojen korjaukset **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="5ef39-111">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ef39-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="5ef39-112">Valitse **Resurssin vika-analyysi** -välilehdestä yksi tai useita painikkeita **Ryhmittely...** -toimintoruuturyhmissä, jolloin näkyviin tulee haluamasi yksityiskohtaisuuden taso.</span><span class="sxs-lookup"><span data-stu-id="5ef39-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="5ef39-113">Aktivoidut painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="5ef39-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="5ef39-114">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="5ef39-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="5ef39-115">Valitse **Päivitä laskelmat**, jos haluat näyttää valintasi näytössä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="5ef39-116">Joka kerta, kun aktivoit tai poistat **Ryhmittely...**-toimintoruuturyhmien painikkeita, muista napsauttaa **Päivitä laskelmat** -painiketta, kun olet muuttanut valintoja.</span><span class="sxs-lookup"><span data-stu-id="5ef39-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="5ef39-117">Tämä on tarpeen, koska suuri määrä tietoja käsitellään, kun virheiden todennäköisyys lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5ef39-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="5ef39-118">Vikamerkintöjä voi analysoida monella tavalla.</span><span class="sxs-lookup"><span data-stu-id="5ef39-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="5ef39-119">Alla on esimerkkejä viidessä kuvakaappauksessa, joissa eri tietojen valinnat antavat erilaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="5ef39-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="5ef39-120">Näet, miten eri valinnat tuottavat erilaisia tietoa ja yksityiskohtia, kun käyttöomaisuusvirheiden rekisteröintejä analysoidaan.</span><span class="sxs-lookup"><span data-stu-id="5ef39-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="5ef39-121">Alla olevassa kuvassa vain **Oire**-painike on valittuna.</span><span class="sxs-lookup"><span data-stu-id="5ef39-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="5ef39-122">Vikarekisteröintejä on tehty kolmesta vian oireesta: "Air leak", "Blown fuse" ja "Equipment jammed".</span><span class="sxs-lookup"><span data-stu-id="5ef39-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="5ef39-123">**Todennäköisyys-%**-sarakkeessa kaikki prosentit ovat yhteensä 100 %.</span><span class="sxs-lookup"><span data-stu-id="5ef39-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="5ef39-124">Todennäköisyys perustuu tämän vika-analyysin kaikkiin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="5ef39-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Kuva 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="5ef39-126">Alla olevassa kuvakaappauksessa lisätään **Vuosi** ja **Kuukausi**, joiden mukaan voit tarkastella vikamerkintöjä valitulta ajanjaksolta.</span><span class="sxs-lookup"><span data-stu-id="5ef39-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="5ef39-127">Vikaoireet näkyvät nyt rekisteröinteinä vuodessa/kuukaudessa.</span><span class="sxs-lookup"><span data-stu-id="5ef39-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="5ef39-128">Jos lisäät kullekin kuukaudelle kaikki prosentit **Todennäköisyys-%**-sarakkeeseen, ne ova yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="5ef39-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="5ef39-129">Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="5ef39-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="5ef39-130">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="5ef39-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Kuva 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="5ef39-132">Resurssin ja resurssityypin yhdistelmää käytetään seuraavien kolmen kuvaruudun laskelmien perustana, mikä lisää yksityiskohtaisuutta.</span><span class="sxs-lookup"><span data-stu-id="5ef39-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="5ef39-133">Yleisesti ottaen **Ryhmittele päivämäärän mukaan**-, **Ryhmittele resurssin mukaan**-, **Ryhmittele toiminnallisen sijainnin mukaan** toimintoruuturyhmät samoin kuin **Vika**-painike (vian tunnus) sisältävät kausia tai resurssisuhteita.</span><span class="sxs-lookup"><span data-stu-id="5ef39-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="5ef39-134">**Oire**-, **Alue**-, **Tyyppi**-, **Syy**- ja **Korjaus**-painikkeet ovat luokitteluja, joita käytetään vikojen hallinnassa analysoimaan vikarekisteröintejä ja merkitsemään ongelma-alueita.</span><span class="sxs-lookup"><span data-stu-id="5ef39-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="5ef39-135">Alla olevassa kuvakaappauksessa **Resurssi** ja **Resurssityyppi** on lisätty antamaan tarkempia tietoja vikarekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="5ef39-136">Vian oireet on nyt jaettu **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="5ef39-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="5ef39-137">Jos lisäät **Todennäköisyys-%**-sarakkeeseen kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ova yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="5ef39-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="5ef39-138">Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="5ef39-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="5ef39-139">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="5ef39-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Kuva 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="5ef39-141">Alla olevassa kuvakaappauksessa **Alue** lisättiin **Oire**-, **Resurssi**- ja **Resurssityyppi** -yhdistelmään antamaan tarkempia tietoja vikarekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="5ef39-142">Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="5ef39-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="5ef39-143">Todennäköisyys perustuu tämän vika-analyysin **Oire**- ja **Alue**-yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="5ef39-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="5ef39-144">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vika-alueista, joiden avulla voidaan selvittää, miten kyseisen vika-alueiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="5ef39-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Kuva 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="5ef39-146">Alla olevaan kuva kaappausruutuun lisättiin **Tyyppi**ja tässä esimerkissä näytetään tarkimmat laskennat.</span><span class="sxs-lookup"><span data-stu-id="5ef39-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="5ef39-147">Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="5ef39-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="5ef39-148">Todennäköisyys perustuu tämän vika-analyysin **Oire**-, **Alue**- ja **Tyyppi**-yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="5ef39-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="5ef39-149">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikatyypeistä, joiden avulla voidaan selvittää, miten kyseisen vikatyypin rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="5ef39-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Kuva 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="5ef39-151">Saat yleiskuvan kaikista työtilauksiin ja ylläpitopyyntöihin luoduista vikarekisteröinneistä valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**.</span><span class="sxs-lookup"><span data-stu-id="5ef39-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="5ef39-152">Valitse **Resurssin viat** -sivulla käyttöomaisuus virheiden kirjaaminen ja laajenna **Aiheeseen liittyviä tietoja** -ruutu, josta näet tietoja asiaan liittyvästä työtilauksesta tai ylläpitopyynnöstä.</span><span class="sxs-lookup"><span data-stu-id="5ef39-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

