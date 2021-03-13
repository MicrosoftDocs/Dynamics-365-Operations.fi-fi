---
title: Resurssien vika-analyysi
description: Tässä ohjeaiheessa kerrotaan resurssivikojen analyysista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 674e10b94711b00e526af4af0e0c0afddd05e62c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022374"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="f3d77-103">Resurssien vika-analyysi</span><span class="sxs-lookup"><span data-stu-id="f3d77-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f3d77-104">Käyttöomaisuuden hallinnassa voit analysoida käyttöomaisuuden vikamerkintöjä, jolloin saat yleiskuvan tietyn kauden aikana rekisteröityjen vikojen kokonaismäärästä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="f3d77-105">Vikarekisteröintejä voidaan analysoida eri näkökulmista, esimerkiksi resurssien, resurssityyppien, toiminnallisten sijaintien, vian oireiden tai vikatyyppien näkökulmista.</span><span class="sxs-lookup"><span data-stu-id="f3d77-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="f3d77-106">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen analyysi**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="f3d77-107">**Resurssin vika-analyysin laskenta** -valintaikkunassa voit määrittää **Taso** -kentän avulla, miten yksityiskohtaisia haluat käyttöomaisuusvirherivien olevan toiminnallisia sijainteja ajatellen.</span><span class="sxs-lookup"><span data-stu-id="f3d77-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="f3d77-108">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssivikarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="f3d77-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="f3d77-109">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="f3d77-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="f3d77-110">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät, virheiden syyt ja vikojen korjaukset **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="f3d77-111">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="f3d77-112">Valitse **Resurssin vika-analyysi** -välilehdestä yksi tai useita **Ryhmittely...** -painikkeita, jolloin näkyviin tulee haluamasi yksityiskohtaisuuden taso.</span><span class="sxs-lookup"><span data-stu-id="f3d77-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="f3d77-113">Aktivoidut painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="f3d77-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="f3d77-114">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="f3d77-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="f3d77-115">Valitse **Päivitä laskelmat**, jos haluat näyttää valintasi näytössä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="f3d77-116">Aina kun otat käyttöön **Ryhmittele...**-painikkeen tai poistat sellaisen käytöstä, muista napsauttaa **Päivitä laskelmat**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f3d77-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="f3d77-117">Tämä on tarpeen, koska suuri määrä tietoja käsitellään, kun virheiden todennäköisyys lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f3d77-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="f3d77-118">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="f3d77-118">Examples</span></span>

<span data-ttu-id="f3d77-119">Vikamerkintöjä voi analysoida monella tavalla.</span><span class="sxs-lookup"><span data-stu-id="f3d77-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="f3d77-120">Tämä osa sisältää viisi esimerkkiä siitä, miten erilaiset tietovalinnat voivat tuottaa erilaisia tietoa ja yksityiskohtia, kun käyttöomaisuusvirheiden rekisteröintejä analysoidaan.</span><span class="sxs-lookup"><span data-stu-id="f3d77-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="f3d77-121">Oireiden mukaan ryhmittely</span><span class="sxs-lookup"><span data-stu-id="f3d77-121">Group by symptoms</span></span>

<span data-ttu-id="f3d77-122">Alla olevassa kuvassa vain **Oire**-painike on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f3d77-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="f3d77-123">Vikarekisteröintejä on tehty kolmesta vian oireesta: "Air leak", "Blown fuse" ja "Equipment jammed".</span><span class="sxs-lookup"><span data-stu-id="f3d77-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="f3d77-124">**Todennäköisyys-%**-sarakkeessa kaikki prosentit ovat yhteensä 100 %.</span><span class="sxs-lookup"><span data-stu-id="f3d77-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="f3d77-125">Todennäköisyys perustuu tämän vika-analyysin kaikkiin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="f3d77-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Kuva 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="f3d77-127">Oireiden ja ajanjakson mukaan ryhmittely</span><span class="sxs-lookup"><span data-stu-id="f3d77-127">Group by symptoms and time period</span></span>

<span data-ttu-id="f3d77-128">Alla olevassa kuvakaappauksessa lisätään **Vuosi** ja **Kuukausi**, joiden mukaan voit tarkastella vikamerkintöjä valitulta ajanjaksolta.</span><span class="sxs-lookup"><span data-stu-id="f3d77-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="f3d77-129">Vikaoireet näkyvät nyt rekisteröinteinä vuodessa/kuukaudessa.</span><span class="sxs-lookup"><span data-stu-id="f3d77-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="f3d77-130">Jos lisäät kullekin kuukaudelle kaikki prosentit **Todennäköisyys-%**-sarakkeeseen, ne ova yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="f3d77-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="f3d77-131">Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="f3d77-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f3d77-132">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="f3d77-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Kuva 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="f3d77-134">Useiden oireiden ja resurssien mukaan ryhmittely</span><span class="sxs-lookup"><span data-stu-id="f3d77-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="f3d77-135">Resurssin ja resurssityypin yhdistelmää käytetään seuraavien kolmen kuvaruudun laskelmien perustana, mikä lisää yksityiskohtaisuutta.</span><span class="sxs-lookup"><span data-stu-id="f3d77-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="f3d77-136">Yleisesti ottaen **Ryhmittele päivämäärän mukaan**-, **Ryhmittele resurssin mukaan**- ja **Ryhmittele toiminnallisen sijainnin mukaan** -toimintoruuturyhmät samoin kuin **Vika**-painike (vian tunnus) sisältävät kausia tai resurssisuhteita.</span><span class="sxs-lookup"><span data-stu-id="f3d77-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="f3d77-137">**Oire**-, **Alue**-, **Tyyppi**-, **Syy**- ja **Korjaus**-painikkeet ovat luokitteluja, joita käytetään vikojen hallinnassa analysoimaan vikarekisteröintejä ja merkitsemään ongelma-alueita.</span><span class="sxs-lookup"><span data-stu-id="f3d77-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="f3d77-138">**Ryhmittele oireen, resurssin ja resurssityypin mukaan**</span><span class="sxs-lookup"><span data-stu-id="f3d77-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="f3d77-139">Alla olevassa kuvakaappauksessa **Resurssi** ja **Resurssityyppi** on lisätty antamaan tarkempia tietoja vikarekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f3d77-140">Vian oireet on nyt jaettu **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmiin.</span><span class="sxs-lookup"><span data-stu-id="f3d77-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="f3d77-141">Jos lisäät **Todennäköisyys-%**-sarakkeeseen kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ova yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="f3d77-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="f3d77-142">Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin.</span><span class="sxs-lookup"><span data-stu-id="f3d77-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f3d77-143">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="f3d77-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Kuva 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="f3d77-145">**Ryhmittele kahden oireen, resurssin ja resurssityypin mukaan**</span><span class="sxs-lookup"><span data-stu-id="f3d77-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="f3d77-146">Alla olevassa kuvakaappauksessa **Alue** lisättiin **Oire**-, **Resurssi**- ja **Resurssityyppi** -yhdistelmään antamaan tarkempia tietoja vikarekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f3d77-147">Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="f3d77-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f3d77-148">Todennäköisyys perustuu tämän vika-analyysin **Oire**- ja **Alue**-yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="f3d77-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="f3d77-149">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vika-alueista, joiden avulla voidaan selvittää, miten kyseisen vika-alueiden rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="f3d77-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Kuva 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="f3d77-151">**Ryhmittele kolmen oireen, resurssin ja resurssityypin mukaan**</span><span class="sxs-lookup"><span data-stu-id="f3d77-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="f3d77-152">Alla olevaan kuva kaappausruutuun lisättiin **Tyyppi** ja tässä esimerkissä näytetään tarkimmat laskennat.</span><span class="sxs-lookup"><span data-stu-id="f3d77-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="f3d77-153">Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %.</span><span class="sxs-lookup"><span data-stu-id="f3d77-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f3d77-154">Todennäköisyys perustuu tämän vika-analyysin **Oire**-, **Alue**- ja **Tyyppi**-yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="f3d77-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="f3d77-155">Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikatyypeistä, joiden avulla voidaan selvittää, miten kyseisen vikatyypin rekisteröinnin määrää voidaan rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="f3d77-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Kuva 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="f3d77-157">Saat yleiskuvan kaikista työtilauksiin ja ylläpitopyyntöihin luoduista vikarekisteröinneistä valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="f3d77-158">Valitse **Resurssin viat** -sivulla käyttöomaisuus virheiden kirjaaminen ja laajenna **Aiheeseen liittyviä tietoja** -ruutu, josta näet tietoja asiaan liittyvästä työtilauksesta tai ylläpitopyynnöstä.</span><span class="sxs-lookup"><span data-stu-id="f3d77-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

