---
title: Affordable Care -lain (ACA) mukaisten raporttien luominen
description: Affordable Care Act (ACA) -raportointi luo lomakkeita 1095-B ja 1095-C, mikä tukee Affordable Care Act (ACA) -lain **Työnantajan valtakirja** -osaa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053198"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="1d977-103">ACA-raporttien luominen</span><span class="sxs-lookup"><span data-stu-id="1d977-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1d977-104">Affordable Care Act (ACA) -raportointi luo lomakkeita 1095-B ja 1095-C, mikä tukee Affordable Care Act (ACA) -lain **Työnantajan valtakirja** -osaa.</span><span class="sxs-lookup"><span data-stu-id="1d977-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="1d977-105">ACA-raportointi on käytössä vain yrityksissä Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="1d977-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="1d977-106">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="1d977-106">Getting started</span></span>

<span data-ttu-id="1d977-107">Voit seurata 1095-B- ja 1095-C-lomakkeiden tietoja luomalla ensin yhden tai useita Affordable Care -kattavuusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="1d977-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="1d977-108">Affordable Care -kattavuusryhmät ilmaisevat:</span><span class="sxs-lookup"><span data-stu-id="1d977-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="1d977-109">Työntekijän kattavuustarjous</span><span class="sxs-lookup"><span data-stu-id="1d977-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="1d977-110">Työntekijän osuus pienimmän kustannuksen kuukausittaisen lisän kustannuksista, jos kustannukset ovat liittovaltion köyhyysrajan yläpuolella</span><span class="sxs-lookup"><span data-stu-id="1d977-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="1d977-111">Työnantajan käyttämä Safe Harbor (jos sovellettavissa)</span><span class="sxs-lookup"><span data-stu-id="1d977-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="1d977-112">Affordable Care Act -kattavuusryhmien avulla voit hallita näitä kenttiä koskevia tietoja ilman jokaisen työtekijätietueen muuttamista silloin, kun ehdot ovat samat.</span><span class="sxs-lookup"><span data-stu-id="1d977-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="1d977-113">Affordable Care -kattavuusryhmät voi helposti määrittää helposti yhdelle tai usealle työntekijälle sivun **Joukkomääritys**-toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="1d977-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="1d977-114">Kattavuusryhmän useiden versioiden ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="1d977-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="1d977-115">Voit ylläpitää useita versioita mistä tahansa kattavuusryhmästä.</span><span class="sxs-lookup"><span data-stu-id="1d977-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="1d977-116">Tämän toiminnon avulla voit tehdä muutoksia ilman, että sinun tarvitse luoda uutta ryhmää ja määrittää siihen työntekijöitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="1d977-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="1d977-117">Kun olet luonut ACA-kattavuusryhmät, voit määrittää ryhmät joukkotoimintona työntekijöille **Joukkomääritys**-vaihtoehdon avulla.</span><span class="sxs-lookup"><span data-stu-id="1d977-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="1d977-118">Voit myös määrittää erikseen, seurataanko ja raportoitaanko ACA-tietoja, ja määrittää työntekijän Affordable Care -kattavuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="1d977-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="1d977-119">Joitakin ACA-kattavuustietoja, kuten osa-aikatyöntekijöitä, ei tarvitse seurata.</span><span class="sxs-lookup"><span data-stu-id="1d977-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="1d977-120">Määritä tällöin **Raportin kattavuus** -kentän arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="1d977-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="1d977-121">Vaikka jokaiselle työntekijälle on määritettävä jäljitettävät ACA-tiedot Affordable Care -kattavuusryhmään, voit silti muuttaa seuraavia asetuksia kuukausille, joissa on eri arvoja:</span><span class="sxs-lookup"><span data-stu-id="1d977-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="1d977-122">**Kattavuustarjous**</span><span class="sxs-lookup"><span data-stu-id="1d977-122">**Offer of coverage**</span></span>
- <span data-ttu-id="1d977-123">**Työntekijän osa kustannuksista**</span><span class="sxs-lookup"><span data-stu-id="1d977-123">**Employee share of cost**</span></span>
- <span data-ttu-id="1d977-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="1d977-124">**Safe Harbor**</span></span>

<span data-ttu-id="1d977-125">Voit määrittää Affordable Care -kattavuusryhmän arvoille poikkeuksille napsauttamalla **Työntekijän tiedot** -sivulla **Affordable Care -kattavuus** -linkkiä. Tämä linkki sijaitsee **Työsuhde**-välilehden **Lisätiedot**-osassa.</span><span class="sxs-lookup"><span data-stu-id="1d977-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="1d977-126">Terveydenhuollon kattavuuden raportointi</span><span class="sxs-lookup"><span data-stu-id="1d977-126">Reporting health care coverage</span></span>

<span data-ttu-id="1d977-127">Sen lisäksi että seurataan minkä laajuinen terveydenhuolto kokopäiväisille työntekijöille on mahdollisesti tarjottu, lisätietoja on raportoiva 1095-C-lomakkeella, jos työntekijä tarjoaa työnantajan sponsoroimaa omakustanteista terveydenhuoltoa, johon työntekijä on rekisteröity (riippumatta siitä, onko kyse koko- vai osa-aikaisesta työntekijästä).</span><span class="sxs-lookup"><span data-stu-id="1d977-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="1d977-128">Jokainen työntekijä (ja heidän huollettavansa), jonka työnantajan sponsoroimat etusuunnitelmat kattavat, on sisällytettävä raporttiin niiden kuukausien ajalta, joita kattavuus koskee.</span><span class="sxs-lookup"><span data-stu-id="1d977-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="1d977-129">Voit ilmaista, onko kukin etusuunnitelma raportoiva, valitsemalla **ACA-raportoitavien** valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="1d977-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="1d977-130">Jos työtekijät ovat lisäksi valinneet, että etu kattaa myös jonkin heidän huollettavansa, voit ilmaista **etujen ylläpitosivulla** kunkin työntekijän kohdalla päivämäärät, jolloin he olivat katettuna..</span><span class="sxs-lookup"><span data-stu-id="1d977-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="1d977-131">Voit ilmaista, että etu kattaa huollettavat, valitsemalla **Huollettavat**-pikavälilehden toimintoruudussa **Muokkaa**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="1d977-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="1d977-132">Voit ilmoittaa **Huollettavaa koskevien kattavuuspäivämäärien hallinta** -sivulla päivämäärät, jolloin etu kattoi huollettavan.</span><span class="sxs-lookup"><span data-stu-id="1d977-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="1d977-133">Kun tällä sivulla annetaan päivämääriä, **Katettu**-valintaruutu valitaan automaattisesti **Etujen ylläpito** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1d977-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="1d977-134">Luo 1095-B- ja 1095-C-lomakkeita</span><span class="sxs-lookup"><span data-stu-id="1d977-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="1d977-135">Voit luoda 1095-B- ja 1095-C-lomakkeita myös tuotteesta ja jakaa ne työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="1d977-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="1d977-136">Järjestelmä voi myös luoda sähköisesti 1095-C-lomakkeita ja 1094-C IRS -siirtotiedostoja.</span><span class="sxs-lookup"><span data-stu-id="1d977-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="1d977-137">Anna 1095-C-lomaketta luotaessa oikea verovuosi ja ilmaise, onko sosiaaliturvatunnukset peitettävä.</span><span class="sxs-lookup"><span data-stu-id="1d977-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="1d977-138">Jos tulostat 1095-C-lomakkeet yli 500 työntekijälle, PDF-tiedostoja on useita.</span><span class="sxs-lookup"><span data-stu-id="1d977-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="1d977-139">Lisäksi suositellaan, että **Tiedoston enimmäiskoko** -asetukseksi määritetään **Tiedostonhallintaparametrit**-ikkunassa 150 Mt.</span><span class="sxs-lookup"><span data-stu-id="1d977-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="1d977-140">Tietojen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="1d977-140">Viewing information</span></span>

<span data-ttu-id="1d977-141">Voit tarkistaa **Työntekijän Affordable Care -kattavuus** -sivulla kuhunkin kattavuusryhmään määritetyt työntekijät, työntekijät, joita ei tarvitse sisällyttää raporttiin, ja määrittämättömät työntekijät.</span><span class="sxs-lookup"><span data-stu-id="1d977-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="1d977-142">Jos jokin Affordable Care -kattavuusryhmän oletusarvoista on korvattu, muutetun arvon vieressä näkyy tähtimerkki.</span><span class="sxs-lookup"><span data-stu-id="1d977-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="1d977-143">Jos jokaisen 12 kuukauden arvo on sama eikä sitä ole korvattu, arvo tulostuu **Kaikki 12 kuukautta** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1d977-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="1d977-144">Kyselyikkunan avulla voit myös ymmärtää, mitkä työntekijät on merkitty siten ettei niitä ilmoiteta ACA:n mukaan.</span><span class="sxs-lookup"><span data-stu-id="1d977-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="1d977-145">Sinun ei tarvitse seurata, onko kattavuus tarjottu heille, eikä heille tarvitse antaa 1095-C-lomaketta vuoden lopussa.</span><span class="sxs-lookup"><span data-stu-id="1d977-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="1d977-146">Jos valitset **Suodatus**-kentästä **Ei ACA-raporttia**, näyttöön tulee luettelo kaikista työntekijöistä, jotka eivät saa 1095-C-lomaketta.</span><span class="sxs-lookup"><span data-stu-id="1d977-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="1d977-147">Sen lisäksi voit tarkastella määrittämättömiä työntekijöitä (**ACA-raportoinnin kattavuuden** kenttä on tyhjä) tai työntekijöitä, jotka on määritetty **Vuosi**-kentässä valittuna vuonna vanhentuneeseen Affordable Care -kattavuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="1d977-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="1d977-148">Voit viedä erilaisilla suodatusvalinnoilla luodun työntekijäluettelon Exceliin.</span><span class="sxs-lookup"><span data-stu-id="1d977-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="1d977-149">Jos sinun on raportoitava kattavuuteen kuuluvat henkilöt itsevakuutettujen kattavuuden vuoksi, voit tarkastella kaikkia huollettavia, jotka on katettu **ACA-raportoitaviksi** merkityissä etusuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="1d977-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="1d977-150">Valitse toimintoruudussa **Näytä huollettavien kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="1d977-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="1d977-151">Vain **ACA-raportoitavat** etusuunnitelmat näkyvät kyselyikkunassa.</span><span class="sxs-lookup"><span data-stu-id="1d977-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]