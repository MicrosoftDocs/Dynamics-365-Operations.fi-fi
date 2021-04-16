---
title: Kustannusten ja päivämäärien hallinta
description: Tässä ohjeaiheessa kerrotaan kustannusten ja päivien hallinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d6f0a155b38b1d732d17bd2f964677862ff363e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808661"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="5482d-103">Kustannusten ja päivämäärien hallinta</span><span class="sxs-lookup"><span data-stu-id="5482d-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5482d-104">Käyttöomaisuuden hallinnassa voit laskea kustannuksia, jolloin saat yleiskuvan todellisista kustannuksista resurssien, toiminnallisten sijaintien tai työtilausten budjettikustannuksiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="5482d-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="5482d-105">Todelliset kustannukset perustuvat kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="5482d-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="5482d-106">Voit myös määrittää päivämäärän laskemisen, jos haluat verrata ajoitettuja alkamis- ja päättymispäiviä työtilausten todellisiin alkamis- ja päättymispäiviin.</span><span class="sxs-lookup"><span data-stu-id="5482d-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="5482d-107">Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="5482d-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="5482d-108">Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset.</span><span class="sxs-lookup"><span data-stu-id="5482d-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="5482d-109">Ainoa ero on, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa.</span><span class="sxs-lookup"><span data-stu-id="5482d-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="5482d-110">Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.</span><span class="sxs-lookup"><span data-stu-id="5482d-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="5482d-111">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien kustannusten hallinta** tai **Toiminnallisen sijainnin kustannusten hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen kustannusten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="5482d-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="5482d-112">Valitse laskettava aikaväli **Resurssien kustannusten hallinta**- / **Toiminnallisen sijainnin kustannusten hallinta**- / **Työtilauksen kustannusten hallinta** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="5482d-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="5482d-113">Valitse tarvittaessa taloushallinnon dimensioyhdistelmä, joka sisällytetään laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="5482d-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="5482d-114">Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.</span><span class="sxs-lookup"><span data-stu-id="5482d-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="5482d-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="5482d-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="5482d-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin kustannusten hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="5482d-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="5482d-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kustannusten hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="5482d-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="5482d-118">Valitse **Näytä avoin sidottu kustannus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää kyseisen sarakkeen laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="5482d-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="5482d-119">Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.</span><span class="sxs-lookup"><span data-stu-id="5482d-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="5482d-120">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="5482d-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="5482d-121">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5482d-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="5482d-122">Alla olevassa kuvassa on esimerkki **Resurssien kustannusten hallinta** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="5482d-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Resurssien kustannusten hallinnan valintaikkuna](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="5482d-124">Napsauta **Resurssien kustannusten hallinta** -sivulla **Ryhmittele**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="5482d-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5482d-125">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="5482d-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5482d-126">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="5482d-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="5482d-127">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5482d-127">Example</span></span>

<span data-ttu-id="5482d-128">Alla olevassa näyttökuvassa on esimerkki **Resurssien kustannusten hallinta** -laskennan tuloksista.</span><span class="sxs-lookup"><span data-stu-id="5482d-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="5482d-129">**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="5482d-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="5482d-130">**Sidottu kustannus** -kenttä näyttää kokonaiskustannukset, jonka yritys on sitoutunut maksamaan.</span><span class="sxs-lookup"><span data-stu-id="5482d-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="5482d-131">**Avoin sidottu kustannus** -kentässä näkyvät sitoumukset maksaa nimikkeistä, tunneista ja palveluista, jotka olet tilannut tai vastaanottanut mutta joita ei ole vielä maksettu.</span><span class="sxs-lookup"><span data-stu-id="5482d-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="5482d-132">**Toteutunut kustannus** -kentässä näkyvät asiaan liittyvät kulut, kun kaikki kulutusrekisteröinnit on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="5482d-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Esimerkki Resurssien kustannusten hallinnan laskutuloksista](media/02-controlling-and-reporting.png)

<span data-ttu-id="5482d-134">Toinen tapa määrittää kustannuslaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="5482d-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="5482d-135">Valitse sitten **Yleiset**-välilehden **Kustannusten hallinta** -painike. **Resurssien kustannusten hallinta**-valintaikkunassa valitut käyttöomaisuudet lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5482d-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="5482d-136">Valitse **OK**, niin valittujen käyttökohteiden kustannuslaskennat näytetään.</span><span class="sxs-lookup"><span data-stu-id="5482d-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="5482d-137">Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5482d-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="5482d-138">Työtilausten päivämäärien hallinta</span><span class="sxs-lookup"><span data-stu-id="5482d-138">Work order date control</span></span>

<span data-ttu-id="5482d-139">Tämän sivun avulla voit saada yleiskuvan suunnitelluista alkamis- ja päättymispäivistä verrattuna työtilausten todellisiin alkamis- ja päättymispäiviin.</span><span class="sxs-lookup"><span data-stu-id="5482d-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="5482d-140">Valitse **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen päivämäärien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="5482d-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="5482d-141">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="5482d-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="5482d-142">Valitse toiminnallinen sijainti **Toiminnallinen sijainti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5482d-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="5482d-143">Lisää aikaväli, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät).</span><span class="sxs-lookup"><span data-stu-id="5482d-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="5482d-144">Kaikki työtilaukset, joiden oletettu aloituspäivä osuu aikavälillä, otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="5482d-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="5482d-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5482d-145">Click **OK**.</span></span>

6. <span data-ttu-id="5482d-146">Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="5482d-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5482d-147">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="5482d-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5482d-148">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="5482d-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="5482d-149">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5482d-149">Example</span></span>

<span data-ttu-id="5482d-150">Alla olevassa näyttökuvassa on esimerkki **Työtilauksen päivämäärien hallinta** -laskennan tuloksista.</span><span class="sxs-lookup"><span data-stu-id="5482d-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="5482d-151">**Keskim. aloituksen viive** -kentässä näkyy työtilauksen suunnitellun alkamispäivän välinen ero suhteessa todelliseen alkamispäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5482d-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="5482d-152">Jos todellinen alkamispäivä on esimerkiksi kaksi päivää ennen ajoitettua alkamispäivää, kentässä näkyy "-2".</span><span class="sxs-lookup"><span data-stu-id="5482d-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="5482d-153">**Keskim. lopetuksen viive** -kentässä näkyy työtilauksen suunnitellun lopetuspäivän välinen ero suhteessa todelliseen lopetuspäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5482d-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="5482d-154">Jos todellinen lopetuspäivä on esimerkiksi kolme päivää ajoitetun lopetuspäivän jälkeen, kentässä näkyy "3".</span><span class="sxs-lookup"><span data-stu-id="5482d-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="5482d-155">**Esiintymiskerrat**-kentissä näkyy, kuinka monta kertaa poikkeama esiintyy suhteessa ajoitettuun ja todelliseen alkamispäivämäärään sekä työtilauksen ajoitettuun ja todelliseen päättymispäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5482d-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Esimerkki Työtilausten päivämäärien hallinnan laskutuloksista](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]