---
title: Käyttöomaisuusryhmien jälleenhankintahintojen ja vakuutusarvojen uudelleenlaskenta
description: Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9dd04072b4845fe5df2a918b64ba1835ea584dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187104"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a><span data-ttu-id="a7de9-103">Käyttöomaisuusryhmien jälleenhankintahintojen ja vakuutusarvojen uudelleenlaskenta</span><span class="sxs-lookup"><span data-stu-id="a7de9-103">Recalculate replacement costs and insured values for fixed asset groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7de9-104">Tässä artikkelissa on selostettu prosessia, jolla päivitetään käyttöomaisuuden jälleenhankintahinnat ja vakuutusarvot.</span><span class="sxs-lookup"><span data-stu-id="a7de9-104">This article explains the process to update the replacement costs and insured values for fixed assets.</span></span>

<span data-ttu-id="a7de9-105">Tiettyjen käyttöomaisuuserien jälleenhankintahinta tai vakuutusarvo voi toisinaan muuttua.</span><span class="sxs-lookup"><span data-stu-id="a7de9-105">Periodically, you might be notified that the cost to replace or insure specific fixed assets has changed.</span></span> <span data-ttu-id="a7de9-106">Esimies voi esimerkiksi ilmoittaa, että inflaatio on ollut viime vuonna 3 prosenttia, joten kaikkien käyttöomaisuuserien jälleenhankintahintaa täytyy korottaa 3 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a7de9-106">For example, your manager might inform you that inflation was 3 percent last year, so you need to increase the replacement cost of all fixed assets by 3 percent.</span></span> 

<span data-ttu-id="a7de9-107">Vaikka yksittäisten käyttöomaisuuserien jälleenhankintahintaa ja vakuutusarvoa voikin muokata **Käyttöomaisuudet**-sivulla, kokonaisen käyttöomaisuusryhmän arvot voi päivittää kerralla **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a7de9-107">Although you can edit the replacement cost and insured value for individual fixed assets in the **Fixed assets** page, you can use the **Update replacement costs and insured values** page to update these values for a group of assets at one time.</span></span> <span data-ttu-id="a7de9-108">Tässä ohjeessa kuvataan käyttöomaisuusryhmien tai tiettyjen ryhmän käyttöomaisuuksien arvojen päivittäminen.</span><span class="sxs-lookup"><span data-stu-id="a7de9-108">This information describes how to update values for fixed asset groups or for specific assets in the groups.</span></span>

## <a name="how-values-are-updated"></a><span data-ttu-id="a7de9-109"> Tietoja arvojen päivittämisestä</span><span class="sxs-lookup"><span data-stu-id="a7de9-109">How values are updated</span></span>
<span data-ttu-id="a7de9-110">Jos haluat laskea käyttöomaisuusryhmien jälleenhankintahinnan ja vakuutusarvon uudelleen, määritä ensin prosenttiosuus, jonka mukaisesti aiempia jälleenhankintahintoja ja vakuutusarvoja muutetaan, ja laske sitten varsinaiset arvot uudelleen suorittamalla kausittainen päivitys.</span><span class="sxs-lookup"><span data-stu-id="a7de9-110">To recalculate replacement costs and insured values for fixed asset groups, you must first specify the percentage by which to change the existing replacement costs and insured values, and then perform the periodic update to actually recalculate the values.</span></span> <span data-ttu-id="a7de9-111">Prosenttiosuus määritetään **Jälleenhankintahinnan kerroin**- ja **Vakuutusarvon kerroin** -kenttiin **Käyttöomaisuusryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a7de9-111">You specify the percentage in the **Replacement cost factor** and **Insured value factor** fields in the **Fixed asset groups** page.</span></span> <span data-ttu-id="a7de9-112">Vaikka nämä muutosluvut voikin määrittää koko käyttöomaisuusryhmälle, **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivua käyttäessäsi voit valita, että jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen vain ryhmän tietyille käyttöomaisuuserille.</span><span class="sxs-lookup"><span data-stu-id="a7de9-112">Although you specify these factors for the fixed asset group, when you use the **Update replacement costs and insured values** page, you can select to recalculate the replacement cost and insured value for only specific fixed assets in a group.</span></span> 

<span data-ttu-id="a7de9-113">Kun käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo lasketaan uudelleen **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla, järjestelmä käyttää seuraavia kaavoja:</span><span class="sxs-lookup"><span data-stu-id="a7de9-113">When you use the **Update replacement costs and insured values** page to recalculate the replacement cost and insured value for the assets, the following formulas are used:</span></span>

-   <span data-ttu-id="a7de9-114">\[(Käyttöomaisuusryhmän jälleenhankintahinnan muutos / 100) + 1\] \* Käyttöomaisuuserän nykyinen jälleenhankintahinta</span><span class="sxs-lookup"><span data-stu-id="a7de9-114">\[(Asset group's replacement cost factor / 100) + 1\] \* Asset's existing replacement cost</span></span>
-   <span data-ttu-id="a7de9-115">\[(Käyttöomaisuusryhmän vakuutusarvon muutos / 100) + 1\] \* Käyttöomaisuuserän nykyinen vakuutusarvo</span><span class="sxs-lookup"><span data-stu-id="a7de9-115">\[(Asset group's insured value factor / 100) + 1\] \* Asset's existing insured value</span></span>

> [!NOTE] 
> <span data-ttu-id="a7de9-116">Kun käytät **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla, valittujen käyttöomaisuuserien jälleenhankintahinta ja vakuutusarvo päivitetään; vain jommankumman arvon päivittäminen ei ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="a7de9-116">When you use the **Update replacement costs and insured values** page, both the replacement cost and insured value are updated for the selected assets; you cannot specify that only one value be updated.</span></span> <span data-ttu-id="a7de9-117">Jos haluat jättää yhden arvon ennalleen ja päivittää toisen arvon, lisää muutosluvuksi 0 (nolla) **Käyttöomaisuusryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a7de9-117">To leave one value the same and update the other value, enter 0 (zero) as the factor in the **Fixed asset groups** page.</span></span> <span data-ttu-id="a7de9-118">Jos kertoimen arvoksi määritetään nolla tai tyhjä, laskenta ohitetaan päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="a7de9-118">A zero or blank factor causes the calculation to be skipped in the update.</span></span> <span data-ttu-id="a7de9-119">Kausittainen päivitys ei vaikuta käyttöomaisuuserien kirjanpitoarvoon ja nettokirjanpitoarvoon.</span><span class="sxs-lookup"><span data-stu-id="a7de9-119">The book value and net book value of fixed assets are not affected by the periodic update.</span></span> 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a><span data-ttu-id="a7de9-120"> Tietoja päivitettävien nimikkeiden valitsemisesta päivämäärän perusteella</span><span class="sxs-lookup"><span data-stu-id="a7de9-120">How to use a date to select which items to update</span></span>
<span data-ttu-id="a7de9-121">Oletusarvon mukaan päivityskäsittely päivittää valitut käyttöomaisuuserät, joita ei ole päivitetty kuluvana päivämääränä, mutta jotka on voitu päivittää edeltäneinä päivämäärinä.</span><span class="sxs-lookup"><span data-stu-id="a7de9-121">By default, the update process updates the selected assets that have not been updated on the current day, but that might have been updated on previous days.</span></span> <span data-ttu-id="a7de9-122">Esimerkiksi &lt; kuluva päivämäärä merkitsee "aiemmin kuin tänään".</span><span class="sxs-lookup"><span data-stu-id="a7de9-122">For example, &lt; current date means “before today.”</span></span> <span data-ttu-id="a7de9-123">Voit muuttaa päivämäärää **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivun **Valitse**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="a7de9-123">You can change the date in the **Update replacement costs and insured values** page by clicking the **Select** button.</span></span> <span data-ttu-id="a7de9-124">Määrittämääsi päivämääräehtoa verrataan käyttöomaisuuserän edellisen kausittaisen päivityksen päivämäärään (**Käyttöomaisuudet**-sivun **Edellinen kausittainen arvon/hinnan päivitys** -kenttään).</span><span class="sxs-lookup"><span data-stu-id="a7de9-124">The date criteria that you specify is compared to the date of the last periodic update for the asset (the **Last periodic value/cost update** field in the **Fixed assets** page).</span></span> <span data-ttu-id="a7de9-125">Aina kun käyttöomaisuuserän jälleenhankintahinta tai vakuutusarvo päivitetään onnistuneesti, järjestelmä päivittää kuluvan päivämäärän automaattisesti **Edellinen kausittainen arvon/hinnan päivitys** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7de9-125">Each time that you successfully update the replacement cost or insured value for a fixed asset, the **Last periodic value/cost update** field is automatically updated with the current date.</span></span> 

<span data-ttu-id="a7de9-126">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="a7de9-126">Example</span></span> 

<span data-ttu-id="a7de9-127">Ajoneuvot-, Toimistokalusteet- ja Rakennuksen-ryhmien jälleenhankintahintaa päivitettiin eilen 5 prosenttia, ja ko. käyttöomaisuuksien päivitystä voidaan pitää oikeana.</span><span class="sxs-lookup"><span data-stu-id="a7de9-127">You updated the replacement cost of the Vehicles, Office Furniture, and Buildings groups by 5 percent yesterday, and you now consider these assets to be accurately updated.</span></span> <span data-ttu-id="a7de9-128">Nämä käyttöomaisuuserät voi jättää pois tämänpäiväisestä päivityksestä, jossa kaikki muut käyttöomaisuuserät päivitetään. Tämä tehdään lisäämällä eilistä päivää edeltävä päivämäärä (&lt; eilisen päivämäärä) **Edellinen kausittainen arvon/hinnan päivitys** -kenttään, koska **ajoneuvojen**, **toimistokalusteiden** ja **rakennusten** edellinen päivitys tapahtui määritettyjen päivämääräkriteerien ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="a7de9-128">To exclude these assets when you update all other fixed assets today, you enter a date in the **Last periodic value/cost update** field that is before yesterday (&lt; yesterday's date), because the last update for the **Vehicles**, **Office Furniture**, and **Buildings** groups occurred outside the date criteria you entered.</span></span>

## <a name="cumulative-effect-of-each-update"></a><span data-ttu-id="a7de9-129"> Kunkin päivityksen kumulatiivinen vaikutus</span><span class="sxs-lookup"><span data-stu-id="a7de9-129">Cumulative effect of each update</span></span>
<span data-ttu-id="a7de9-130">Kullakin päivityksellä on kumulatiivinen vaikutus.</span><span class="sxs-lookup"><span data-stu-id="a7de9-130">Each update has a cumulative effect.</span></span> <span data-ttu-id="a7de9-131">Siksi päivitykset kannattaa suunnitella tarkkaan.</span><span class="sxs-lookup"><span data-stu-id="a7de9-131">Therefore, you should plan your updates carefully.</span></span> <span data-ttu-id="a7de9-132">Jos esimerkiksi teet kaikkiin käyttöomaisuuseriin kolmen prosentin korotuksen tiistaina ja toimistokalusteisiin neljä prosentin korotuksen perjantaina, toimistokalusteiden kumulatiivinen kokonaiskorotus on tällöin 7,12 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a7de9-132">For example, if you increase all assets by 3 percent on Tuesday and then increase office furniture by 4 percent on Friday, office furniture will increase by a total of 7.12 percent.</span></span>

## <a name="scenario"></a><span data-ttu-id="a7de9-133">Skenaario</span><span class="sxs-lookup"><span data-stu-id="a7de9-133">Scenario</span></span>
<span data-ttu-id="a7de9-134">Esimies ilmoittaa seuraavista käyttöomaisuuseriin tulevista muutoksista:</span><span class="sxs-lookup"><span data-stu-id="a7de9-134">Your manager notifies you of the following changes to fixed assets:</span></span>
-   <span data-ttu-id="a7de9-135">Kaikkien käyttöomaisuuserien jälleenhankintahintaan tehdään 3,25 prosentin korotus tietokoneita lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="a7de9-135">Increase the replacement cost of all fixed assets, except computers, by 3.25 percent.</span></span>
-   <span data-ttu-id="a7de9-136">Kaikkien toimistokalusteiden jälleenhankintahintaan tehdään 1 prosentin lisäkorotus.</span><span class="sxs-lookup"><span data-stu-id="a7de9-136">Increase the replacement cost of all office furniture by an additional 1 percent.</span></span>
-   <span data-ttu-id="a7de9-137">Kaikkien tietokoneiden jälleenhankintahintaa ja vakuutusarvoa pienennetään 10 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a7de9-137">Decrease the replacement cost and insured value of all computers by 10 percent.</span></span>

<span data-ttu-id="a7de9-138">Teet seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="a7de9-138">You make the following changes:</span></span>
1.  <span data-ttu-id="a7de9-139">Kirjoita **Käyttöomaisuusryhmät**-sivulla **Jälleenhankintahinnan kerroin** -kenttään 3,25 ja **Vakuutusarvon kerroin** -kenttään 0 kaikille käyttöomaisuusryhmille **Toimistokalusteet**- ja **Tietokoneet**-ryhmiä lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="a7de9-139">In the **Fixed asset groups** page, for all fixed asset groups except the **Office Furniture** group and **Computers** group, you type 3.25 in the **Replacement cost factor** field and 0 in the **Insured value factor** field.</span></span>
2.  <span data-ttu-id="a7de9-140">**Toimistokalusteet**-ryhmän **Jälleenhankintahinnan kerroin** -kenttään kirjoitat 4,25 ja **Vakuutusarvon kerroin** -kenttään 0.</span><span class="sxs-lookup"><span data-stu-id="a7de9-140">For the **Office Furniture** group, you type 4.25 in the **Replacement cost factor** field and 0 in the **Insured value factor** field.</span></span>
3.  <span data-ttu-id="a7de9-141">**Tietokoneet**-ryhmän **Jälleenhankintahinnan kerroin** -kenttään kirjoitat -10 ja **Vakuutusarvon kerroin** -kenttään -10.</span><span class="sxs-lookup"><span data-stu-id="a7de9-141">For the **Computers** group, you type -10 in the **Replacement cost factor** field and -10 in the **Insured value factor** field.</span></span>
4.  <span data-ttu-id="a7de9-142">Suorita kaikkien käyttöomaisuuserien uudelleenlaskenta valitsemalla **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7de9-142">In the **Update replacement costs and insured values** page, you click **OK** to perform the recalculation for all fixed assets.</span></span>

<span data-ttu-id="a7de9-143">Seuraavana päivänä esimies ilmoittaa, että tietokoneiden pienennyksen oli tarkoitus olla 8 prosenttia 10 prosentin asemesta, joten jälleenhankintahintoihin ja vakuutusarvoihin täytyy tehdä oikaisu.</span><span class="sxs-lookup"><span data-stu-id="a7de9-143">The next day, your manager informs you that computers decreased 8 percent instead of 10 percent, so that you have to correct the replacement costs and insured values.</span></span> <span data-ttu-id="a7de9-144">Voit korjata virheen seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="a7de9-144">To fix the error, you can use either of two methods:</span></span>
-   <span data-ttu-id="a7de9-145">Muokkaa **Tietokoneet**-käyttöomaisuusryhmän jokaista käyttöomaisuuserää manuaalisesti **Käyttöomaisuudet**-sivun **Jälleenhankintahinta**- ja **Vakuutusarvo**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="a7de9-145">Manually change the **Insured value** and **Replacement cost** fields in the **Fixed assets** page for each fixed asset in the **Computers** fixed asset group.</span></span> <span data-ttu-id="a7de9-146">Laske ja lisää arvot manuaalisesti niin kuin olisit alun perin pienentänyt alkuperäistä summaa 8 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a7de9-146">Calculate and manually enter the values as if you had decreased the original amount by 8 percent.</span></span> <span data-ttu-id="a7de9-147">Tässä menetelmässä ei käytetä **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivua.</span><span class="sxs-lookup"><span data-stu-id="a7de9-147">By using this method, you do not use the **Update replacement costs and insured values** page.</span></span>
-   <span data-ttu-id="a7de9-148">Kirjoita jälleenhankintahinnan ja vakuutusarvon kertoimet **Tietokoneet**-ryhmän **Jälleenhankintahinnan kerroin**- ja **Vakuutusarvon kerroin** -kenttiin **Käyttöomaisuusryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a7de9-148">Enter replacement cost and insured value factors for the **Computers** group in the **Replacement cost factor** and **Insured value factor** fields in the **Fixed asset groups** page.</span></span> <span data-ttu-id="a7de9-149">Tämä tarkoittaa, että käyttöomaisuuserät palautetaan (10 prosentin vähennystä edeltävien) alkuperäisten arvojen mukaisiksi ja alkuperäistä arvoa pienennetään 8 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="a7de9-149">This will both reset the assets back to their original value (before the 10 percent decrease) and apply the 8 percent decrease to the original value.</span></span> <span data-ttu-id="a7de9-150">Laske sitten arvot uudelleen **Päivitä jälleenhankintahinnat ja vakuutusarvot** -sivulla ilmoitettujen arvojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a7de9-150">Then use the **Update replacement costs and insured values** page to recalculate the values, depending on the factors that you entered.</span></span>

> [!NOTE]  
> <span data-ttu-id="a7de9-151">Muutoslukua -10 ei voi peruuttaa lisäämällä positiivinen muutosluku 10 (tai kertoimella 2, joka on lukujen -10 ja -8 erotus), koska summat lasketaan tällöin eri tavalla kuin käyttäjä on tarkoittanut.</span><span class="sxs-lookup"><span data-stu-id="a7de9-151">You cannot reverse the -10 factor by entering a factor of positive 10 (or a factor of 2, the difference between -10 and -8), because the amounts will not be calculated as you intend.</span></span> 




