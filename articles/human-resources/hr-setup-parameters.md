---
title: Määritä Human Resourcesin parametrit
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää yrityskohtaisia parametreja Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889929"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="72080-103">Määritä Human Resourcesin parametrit</span><span class="sxs-lookup"><span data-stu-id="72080-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="72080-104">Joidenkin henkilöstöhallinnon parametrien asetukset ovat yhteisiä eri yrityksissä, kun taas muiden parametrien asetukset ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="72080-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="72080-105">Tässä ohjeaiheessa kerrotaan, miten voit määrittää yrityskohtaisia henkilöstöhallinnon parametreja.</span><span class="sxs-lookup"><span data-stu-id="72080-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="72080-106">Henkilöstöhallinnon parametrien määrittämiseen käytetään kahta sivua.</span><span class="sxs-lookup"><span data-stu-id="72080-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="72080-107">Käytä yhtiöiden kesken jaettujen parametrien määrittämiseen **Henkilöstöhallinnon jaetut parametrit** -sivua.</span><span class="sxs-lookup"><span data-stu-id="72080-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="72080-108">Käytä yhtiökohtaisten (ts. asetukset koskevat yhtä yhtiötä) parametrien määrittämiseen **Henkilöstöparametrit**-sivua.</span><span class="sxs-lookup"><span data-stu-id="72080-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Valitse Henkilöstöhallintoparametrit](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="72080-110">**Henkilöstöparametrit**-sivulla asetukset jaetaan kuudelle välilehdelle:</span><span class="sxs-lookup"><span data-stu-id="72080-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="72080-111">**Yleistä**</span><span class="sxs-lookup"><span data-stu-id="72080-111">**General**</span></span>
- <span data-ttu-id="72080-112">**Työhönotto** (Dynamics 365 Human Resources ei sisällä tätä välilehteä)</span><span class="sxs-lookup"><span data-stu-id="72080-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="72080-113">**Kompensaatio**</span><span class="sxs-lookup"><span data-stu-id="72080-113">**Compensation**</span></span>
- <span data-ttu-id="72080-114">**Numerosarjat**</span><span class="sxs-lookup"><span data-stu-id="72080-114">**Number sequences**</span></span>
- <span data-ttu-id="72080-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="72080-115">**FMLA**</span></span>
- <span data-ttu-id="72080-116">**Työntekijän itsepalvelu**</span><span class="sxs-lookup"><span data-stu-id="72080-116">**Employee self service**</span></span>
- <span data-ttu-id="72080-117">**Esimiehen itsepalvelu**</span><span class="sxs-lookup"><span data-stu-id="72080-117">**Manager self service**</span></span>
- <span data-ttu-id="72080-118">**Etujen hallinta**</span><span class="sxs-lookup"><span data-stu-id="72080-118">**Benefits management**</span></span>
- <span data-ttu-id="72080-119">**Loma ja poissaolo**</span><span class="sxs-lookup"><span data-stu-id="72080-119">**Leave and absence**</span></span>
- <span data-ttu-id="72080-120">**Maksutavat**</span><span class="sxs-lookup"><span data-stu-id="72080-120">**Payment methods**</span></span>

<span data-ttu-id="72080-121">Kukin välilehti sisältää yksittäistä yhtiötä koskevia tietoja.</span><span class="sxs-lookup"><span data-stu-id="72080-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="72080-122">Yleistä</span><span class="sxs-lookup"><span data-stu-id="72080-122">General</span></span>

<span data-ttu-id="72080-123">**Yleinen**-välilehdellä määritetään poissaoloja, tapaturmia ja sairaustapauksia sekä uusia työntekijöitä koskevien tietojen ulkonäkö.</span><span class="sxs-lookup"><span data-stu-id="72080-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="72080-124">Tämän välilehden asetukset määrittävät myös osan oletusarvoista, jotka tulevat näkyviin työskentelysi aikana.</span><span class="sxs-lookup"><span data-stu-id="72080-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="72080-125">Tässä välilehdessä voit tehdä erityisesti seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="72080-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="72080-126">Valitse avoimille poissaolotapahtumille käytettävä väri</span><span class="sxs-lookup"><span data-stu-id="72080-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="72080-127">Valitse raporteille käytettävä tyylisivu</span><span class="sxs-lookup"><span data-stu-id="72080-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="72080-128">Ota koulutuskurssien ja poissaolokirjauksen välinen integrointi käyttöön</span><span class="sxs-lookup"><span data-stu-id="72080-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="72080-129">Valitse poissaolokoodi, jota käytetään tämän integroinnin hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="72080-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="72080-130">Valitse, kuinka kauan haluat säilyttää loukkaantumis- ja sairaustapauksia.</span><span class="sxs-lookup"><span data-stu-id="72080-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="72080-131">Määritä oletusarvoinen tunnusnumero, joka näytetään, kun uusi työntekijä palkataan.</span><span class="sxs-lookup"><span data-stu-id="72080-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Yleinen-välilehti](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="72080-133">Työhönotto</span><span class="sxs-lookup"><span data-stu-id="72080-133">Recruitment</span></span>

<span data-ttu-id="72080-134">**Työhönotto**-välilehden asetukset määrittävät asiakirjatyypit, joita käytetään hakijoille automaattisesti lähetettävässä viestinnässä.</span><span class="sxs-lookup"><span data-stu-id="72080-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="72080-135">Voit myös valita avoimille hakemuksille käytettävän työhönottoprojektin.</span><span class="sxs-lookup"><span data-stu-id="72080-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="72080-136">Työhönottoprojektin vanhentumiselle määritetty ajanjakso määrittää työhönottoprojektit, jotka sisällytetään **Työhönoton hallinta** -työtilan **Vanhentuvat projektit** -ruutuun.</span><span class="sxs-lookup"><span data-stu-id="72080-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="72080-137">Hakemuksen määräajan varoitukselle määritettyä ajanjaksoa käytetään näyttämään työhönottoprojektit, jotka lähestyvät hakemuksille asetettua määräaikaansa **Työhönotto**-työtilan **Hakemuksen määräaika lähestyy** -ruudussa.</span><span class="sxs-lookup"><span data-stu-id="72080-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="72080-138">Lisätietoja työhönotosta on kohdassa [Ehdokkaiden työhönotto](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="72080-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="72080-139">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="72080-139">Compensation</span></span>

<span data-ttu-id="72080-140">Dynamics 365 Finance -sovelluksen **Kompensaatio**-välilehden asetukset määrittävät, onko käyttäjien vahvistettava, että he haluavat tallentaa joko kiinteän tai muuttuvan kompensaatiosuunnitelman tiedot.</span><span class="sxs-lookup"><span data-stu-id="72080-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="72080-141">Jos valitset **Otetaan vahvistuksen tallennus käyttöön** -asetuksen, käyttäjiltä kysytään, haluavatko he tallentaa tietueen, kun he sulkevat kompensaatioon liittyvän sivun.</span><span class="sxs-lookup"><span data-stu-id="72080-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="72080-142">Jotkin kompensaation hallinnan sivut eivät salli käyttäjien poistaa tietoja.</span><span class="sxs-lookup"><span data-stu-id="72080-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="72080-143">Kun pyydät käyttäjiä vahvistamaan, että he haluavat tallentaa tiedot, saatat pystyä rajoittamaan sellaisten tietojen määrää, jotka on tallennetaan, mutta joita ei voida poistaa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="72080-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="72080-144">Jos et valitse **Otetaan vahvistuksen tallennus käyttöön** -asetusta, tietueet tallennetaan välittömästi, mahdollisesti jo ennen kuin käyttäjä on valmis.</span><span class="sxs-lookup"><span data-stu-id="72080-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="72080-145">Jos käytät suorituskyvyn hallintaa, **Kompensaatio**-välilehti sallii sinun myös valita suorituskykyä arvioitaessa käytettävän arviointimallin kompensaatiosuunnitelmille määritetyn mallin sijaan.</span><span class="sxs-lookup"><span data-stu-id="72080-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="72080-146">Voit käyttää henkilöstöhallinnon **Kompensaatio**-välilehteä rajoittaaksesi kompensaatiosuunnitelmien käyttöoikeuksia ja määrittääksesi oletusvaluutan.</span><span class="sxs-lookup"><span data-stu-id="72080-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="72080-147">Lisätietoja kompensaatiosta on kohdassa [Kompensaatiosuunnitelmien yleiskuvaus](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Kompensaatiovälilehti](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="72080-149">Numerosarjat</span><span class="sxs-lookup"><span data-stu-id="72080-149">Number sequences</span></span>

<span data-ttu-id="72080-150">**Numerosarja**-välilehdessä olevat asetukset määrittävät järjestyksen, joita käytetään tunnusten kohdistamiseksi automaattisesti henkilöstöhallinnon nimikkeille, esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="72080-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="72080-151">Hakemukset</span><span class="sxs-lookup"><span data-stu-id="72080-151">Applications</span></span>
- <span data-ttu-id="72080-152">Poissaolokirjaukset</span><span class="sxs-lookup"><span data-stu-id="72080-152">Absence registrations</span></span>
- <span data-ttu-id="72080-153">Kompensaatioprosessin tulokset</span><span class="sxs-lookup"><span data-stu-id="72080-153">Compensation process results</span></span>
- <span data-ttu-id="72080-154">Tapausnumerot</span><span class="sxs-lookup"><span data-stu-id="72080-154">Case numbers</span></span>
- <span data-ttu-id="72080-155">Kurssit</span><span class="sxs-lookup"><span data-stu-id="72080-155">Courses</span></span>
- <span data-ttu-id="72080-156">Kurssin työjärjestykset</span><span class="sxs-lookup"><span data-stu-id="72080-156">Course agendas</span></span>

<span data-ttu-id="72080-157">Voit ylläpitää numerosarjojen viitteitä ja koodeja **Numerosarjat**-luettelosivulta (valitse **Organisaation hallinto > Numerosarjat > Numerosarjat**).</span><span class="sxs-lookup"><span data-stu-id="72080-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="72080-158">Lisätietoja on kohdassa [Numerosarjojen yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="72080-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="72080-159">Tehtyjen työtuntien määrä ei voi ylittää 1 250 tuntia, ja työsuhteen pituus ei voi ylittää 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="72080-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="72080-160">Nämä enimmäisarvot ovat Yhdysvaltojen liittovaltion lainsäädännön mukaiset.</span><span class="sxs-lookup"><span data-stu-id="72080-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Numerosarjat-välilehti](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="72080-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="72080-162">FMLA</span></span>

<span data-ttu-id="72080-163">Voit määrittää FMLA-kelpoisuusvaatimukset ja FMLA-korvausajat FMLA-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="72080-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="72080-164">Lisätietoja on kohdassa [Loma- ja poissaoloparametrien määrittäminen](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="72080-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA-välilehti](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="72080-166">Työntekijän itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="72080-166">Employee self service</span></span>

<span data-ttu-id="72080-167">**Työntekijän itsepalvelu** -välilehden asetukset vaikuttavat siihen, miten työntekijän itsepalvelu näytetään työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="72080-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="72080-168">Tästä välilehdestä voit suorittaa seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="72080-168">On this tab, you can:</span></span>

- <span data-ttu-id="72080-169">Anna työntekijän itsepalvelutyötilalle nimi</span><span class="sxs-lookup"><span data-stu-id="72080-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="72080-170">Valitse tiedot, joita esimies voi syöttää työntekijöille</span><span class="sxs-lookup"><span data-stu-id="72080-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="72080-171">Lisää hyödyllisiä linkkejä työntekijöille</span><span class="sxs-lookup"><span data-stu-id="72080-171">Add useful links for employees</span></span>
- <span data-ttu-id="72080-172">Estä työntekijöitä lisäämästä muokkaamasta yrityksen yhteystietoja.</span><span class="sxs-lookup"><span data-stu-id="72080-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="72080-173">Lisätietoja on kohdassa [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="72080-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="72080-174">Lisätietoja työntekijän itsepalvelun määrittämisestä on kohdassa [Työntekijän ja esimiehen itsepalvelun yleiskatsaus](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Työntekijän itsepalvelu -välilehti](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="72080-176">Esimiehen itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="72080-176">Manager self service</span></span>

<span data-ttu-id="72080-177">**Esimiehen itsepalvelu** -välilehden asetukset vaikuttavat siihen, mitä esimiehet näkevät esimiehen itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="72080-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="72080-178">Tästä välilehdestä voit määrittää seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="72080-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="72080-179">Vanhentuvien tietueiden ajanjakso</span><span class="sxs-lookup"><span data-stu-id="72080-179">The range for expiring records</span></span>
- <span data-ttu-id="72080-180">Tiedot, jotka esimiehet näkevät vanhentuvissa tietueissa</span><span class="sxs-lookup"><span data-stu-id="72080-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="72080-181">Voivatko esimiehet tarkastella laajennettujen raporttien avoimia toimia</span><span class="sxs-lookup"><span data-stu-id="72080-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="72080-182">Poistuvien työntekijöiden näkymät</span><span class="sxs-lookup"><span data-stu-id="72080-182">Views of exiting workers</span></span>
- <span data-ttu-id="72080-183">Hyödyllisiä linkkejä esimiehille</span><span class="sxs-lookup"><span data-stu-id="72080-183">Useful links for managers</span></span>

<span data-ttu-id="72080-184">Lisätietoja esimiehen itsepalvelun määrittämisestä on kohdassa [Työntekijän ja esimiehen itsepalvelun yleiskatsaus](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Esimiehen itsepalvelu -välilehti](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="72080-186">Etujen hallinta</span><span class="sxs-lookup"><span data-stu-id="72080-186">Benefits management</span></span>

<span data-ttu-id="72080-187">Voit määrittää etujen hallinnan sähköpostiasetukset Etujen hallinta -välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="72080-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="72080-188">Lisätietoja etujen hallinnan määrittämisestä ja käytöstä on kohdassa [Etujen hallinnan yleiskatsaus](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Etujen hallinta -välilehti](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="72080-190">Loma ja poissaolo</span><span class="sxs-lookup"><span data-stu-id="72080-190">Leave and absence</span></span>

<span data-ttu-id="72080-191">Lisätietoja lomien ja poissaolojen määrittämisestä ja käytöstä on kohdassa [Lomien ja poissaolojen yleiskatsaus](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="72080-192">Maksutavat</span><span class="sxs-lookup"><span data-stu-id="72080-192">Payment methods</span></span>

<span data-ttu-id="72080-193">Voit valita organisaatiosi tukemat maksutavat **Maksutavat**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="72080-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="72080-194">Lisätietoja kompensaation määrittämisestä on kohdassa [Kompensaatiosuunnitelmien yleiskuvaus](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72080-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Maksutavat-välilehti](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]