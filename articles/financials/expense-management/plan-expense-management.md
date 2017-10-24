---
title: Konfiguroi kulujen hallinta
description: "Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin 365 for Finance and Operations, Enterprise Editionin kulujenhallinta määritetään."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 198e37258f45966b92d963cc0c233d4790ca049e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="configure-expense-management"></a><span data-ttu-id="3caa6-103">Konfiguroi kulujen hallinta</span><span class="sxs-lookup"><span data-stu-id="3caa6-103">Configure expense management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3caa6-104">Tässä aiheessa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin 365 for Finance and Operations, Enterprise Editionin kulujenhallinta määritetään.</span><span class="sxs-lookup"><span data-stu-id="3caa6-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="3caa6-105">Matkalaskujen alueelle voit tallentaa esimerkiksi maksutapojen, matkustusehdotusten, kuluraporttien ja -käytäntöjen tiedot.</span><span class="sxs-lookup"><span data-stu-id="3caa6-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="3caa6-106">Koska monet päätökset, jotka teet kulujen hallinnan määrityksiä suunniteltaessa, perustuvat organisaatiohierarkiaan ja taloushallinnan rakenteeseen, sinun on tutustuttava kyseisten alueiden ohjeistukseen.</span><span class="sxs-lookup"><span data-stu-id="3caa6-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="3caa6-107">Konsernin sisäiset kulut</span><span class="sxs-lookup"><span data-stu-id="3caa6-107">Intercompany expenses</span></span>

<span data-ttu-id="3caa6-108">Kun otat konsernin sisäiset kulut käyttöön, annat yrityksille ja työntekijöille oikeuden luoda kuluja toisen organisaation yrityksen puolesta tai kerätä siltä maksun.</span><span class="sxs-lookup"><span data-stu-id="3caa6-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="3caa6-109">Esimerkiksi yrityksen A työntekijä suorittaa yrityksen B projektin, ja projektiin liittyy matkakuluja.</span><span class="sxs-lookup"><span data-stu-id="3caa6-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="3caa6-110">Jos konsernin sisäiset kulut on otettu käyttöön, työntekijä voi sitten lähettää kuluraportin, joka kirjaa kulun yritykselle B, ja kulun maksaa hänelle yritys A. Jos organisaatiossa ei ole useita yrityksiä, konsernin sisäisiä kuluja ei tarvitse ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="3caa6-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="3caa6-111">**Päätös:** haluatko ottaa käyttöön konsernin sisäiset kulut?</span><span class="sxs-lookup"><span data-stu-id="3caa6-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="3caa6-112">Taloushallinto</span><span class="sxs-lookup"><span data-stu-id="3caa6-112">Financial management</span></span>

<span data-ttu-id="3caa6-113">Kulujen hallinta on integroitu tiukasti organisaation taloushallintoon.</span><span class="sxs-lookup"><span data-stu-id="3caa6-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="3caa6-114">Monet kulujen hallinnan määritykset perustuvat päätöksiin, joita olet tehnyt organisaation raha-asioista.</span><span class="sxs-lookup"><span data-stu-id="3caa6-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="3caa6-115">Seuraavissa osissa käsitellään suunnittelua edellyttäviä alueita ja päätöksiä, jotka perustuvat organisaation taloudellisiin päätöksiin ja johtoryhmän opastukseen.</span><span class="sxs-lookup"><span data-stu-id="3caa6-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="3caa6-116">Päivärahat</span><span class="sxs-lookup"><span data-stu-id="3caa6-116">Per diems</span></span>

<span data-ttu-id="3caa6-117">Organisaation myöntämät työntekijöiden päivärahat on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="3caa6-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="3caa6-118">Koska päivärahoja käytetään yleensä kulujen, kuten aterioiden, majoituksen ja muiden satunnaisten menojen korvaamiseen, voit luoda sääntöjä organisaation tarjoamille päivärahoille.</span><span class="sxs-lookup"><span data-stu-id="3caa6-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="3caa6-119">Päivärahan suuruus voi perustua vuodenaikaan, matkan kohteeseen tai molempiin.</span><span class="sxs-lookup"><span data-stu-id="3caa6-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3caa6-120">Kun määritä päivärahasäännön, voit määrittää, mikä prosenttiosuus päivärahasta pidätetään, jos työntekijällä on käytettävissään ilmaisia aterioita tai palveluita.</span><span class="sxs-lookup"><span data-stu-id="3caa6-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3caa6-121">Voit myös määrittää päivärahatasot, joilla määritetään vähimmäis- ja enimmäismäärä tunteja, joilla tietyn suuruista päivärahaa voidaan käyttää työntekijän matkalla.</span><span class="sxs-lookup"><span data-stu-id="3caa6-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="3caa6-122">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-122">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-123">Oletusarvoinen päivärahasäännöt ensimmäiselle ja viimeiselle päivälle:</span><span class="sxs-lookup"><span data-stu-id="3caa6-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="3caa6-124">Mikä määrä tunteja työntekijän on vähintään ilmoitettava saadakseen päivärahan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="3caa6-125">Onko ateriakorvaus pienempi ensimmäisenä ja viimeisenä päivänä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="3caa6-126">Jos on korvaus on pienempi, mikä on pienennyksen määrä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3caa6-127">Onko majoituskorvaus pienempi ensimmäisenä ja viimeisenä päivänä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="3caa6-128">Jos on korvaus on pienempi, mikä on pienennyksen määrä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3caa6-129">Onko muiden ensimmäisenä ja viimeisenä päivänä syntyvien kulujen korvaus pienempi?</span><span class="sxs-lookup"><span data-stu-id="3caa6-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="3caa6-130">Jos on korvaus on pienempi, mikä on pienennyksen määrä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="3caa6-131">Oletusaroiset päivärahasäännöt:</span><span class="sxs-lookup"><span data-stu-id="3caa6-131">Default per diem rules:</span></span>

    - <span data-ttu-id="3caa6-132">Pieneneekö ateriakorvaus prosentuaalisesti, jos ateria on ilmainen?</span><span class="sxs-lookup"><span data-stu-id="3caa6-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="3caa6-133">Jos on korvaus on pienempi, mikä on kutakin ateriaa koskevan pienennyksen määrä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="3caa6-134">Lasketaanko ateriakorvauksen vähennys päivä- tai matkakohtaisesti vai päiväkohtaisten aterioiden määrän mukaan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="3caa6-135">Tuleeko päivärahan summat pyöristää normaalisti vai ylöspäin?</span><span class="sxs-lookup"><span data-stu-id="3caa6-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="3caa6-136">Lasketaanko päivärahat 24 tunnin jaksolta vai kalenteripäivän mukaan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="3caa6-137">Sijaintiin perustuvat päivärahasäännöt:</span><span class="sxs-lookup"><span data-stu-id="3caa6-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="3caa6-138">Vaihteleeko päivärahan määrä sijainnin mukaan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="3caa6-139">Minkä sijaintien?</span><span class="sxs-lookup"><span data-stu-id="3caa6-139">What locations are included?</span></span>
    - <span data-ttu-id="3caa6-140">Jos päivärahat vaihtelevat sijainnin mukaan, mikä on kussakin sijainnissa annettavan päivärahan osuus seuraaville kuluille:</span><span class="sxs-lookup"><span data-stu-id="3caa6-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="3caa6-141">Ateriat</span><span class="sxs-lookup"><span data-stu-id="3caa6-141">Meals</span></span>
        - <span data-ttu-id="3caa6-142">Hotelli</span><span class="sxs-lookup"><span data-stu-id="3caa6-142">Hotel</span></span>
        - <span data-ttu-id="3caa6-143">Muut kulut</span><span class="sxs-lookup"><span data-stu-id="3caa6-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="3caa6-144">Kulujen hallinnan kirjauskansiot ja tilit</span><span class="sxs-lookup"><span data-stu-id="3caa6-144">Expense management journals and accounts</span></span>

<span data-ttu-id="3caa6-145">Kulujen hallinta edellyttää useiden kirjauskansioiden ja tilien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="3caa6-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="3caa6-146">Sinun on esimerkiksi päätettävä, käytetäänkö samaa tiliä käteisennakoille ja luottokorttien riitautuksille.</span><span class="sxs-lookup"><span data-stu-id="3caa6-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="3caa6-147">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-147">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-148">Mihin kirjanpidon kirjauskansioon hyväksytyt kuluraportit kirjataan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="3caa6-149">Mitä tiliä käytetään käteisennakoille?</span><span class="sxs-lookup"><span data-stu-id="3caa6-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="3caa6-150">Kirjataanko käteisennakot välittömästi?</span><span class="sxs-lookup"><span data-stu-id="3caa6-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="3caa6-151">Maksutavat</span><span class="sxs-lookup"><span data-stu-id="3caa6-151">Payment methods</span></span>

<span data-ttu-id="3caa6-152">Jos työtekijöillä on mahdollisuus aiheuttaa kuluja yrityksen puolesta, sinun on määritettävä maksutavat, joita työntekijät saavat käyttää.</span><span class="sxs-lookup"><span data-stu-id="3caa6-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="3caa6-153">Voit esimerkiksi sallia työntekijöille käteisen ja yrityksen luottokortin käytön.</span><span class="sxs-lookup"><span data-stu-id="3caa6-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="3caa6-154">Voit myös sallia työntekijöiden omien luottokorttien käytön, joka hyvitetään sitten työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="3caa6-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="3caa6-155">Jokaisen sallitun maksutavan kohdalla on tehtävä seuraavat päätökset.</span><span class="sxs-lookup"><span data-stu-id="3caa6-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="3caa6-156">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-156">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-157">Mitkä maksutavat sallitaan?</span><span class="sxs-lookup"><span data-stu-id="3caa6-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="3caa6-158">Kuka omistaa maksutavan kulut?</span><span class="sxs-lookup"><span data-stu-id="3caa6-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="3caa6-159">Onko vastatilillä jokin tyyppi?</span><span class="sxs-lookup"><span data-stu-id="3caa6-159">Is there an offset account type?</span></span> <span data-ttu-id="3caa6-160">Jos vastatili on, mikä tili se on?</span><span class="sxs-lookup"><span data-stu-id="3caa6-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="3caa6-161">Jos vastatili on, mikä tili se on?</span><span class="sxs-lookup"><span data-stu-id="3caa6-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="3caa6-162">Jos maksutapa on luottokortti, pitäisikö maksutapaa käyttää vain tuotujen tapahtumien yhteydessä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="3caa6-163">Kululuokat ja jaetut luokat</span><span class="sxs-lookup"><span data-stu-id="3caa6-163">Expense categories and shared categories</span></span>

<span data-ttu-id="3caa6-164">Kun työntekijät luovat kuluraportin, jokainen heidän tallentamansa kulu on liitettävä kululuokkaan.</span><span class="sxs-lookup"><span data-stu-id="3caa6-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="3caa6-165">Kululuokat johdetaan jaetuista luokista, jotka jaetaan kaikissa organisaation yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="3caa6-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="3caa6-166">Nämä luokat voidaan jakaa myös projektin hallinnassa ja kirjanpidossa sen mukaan, miten organisaatio on määritetty.</span><span class="sxs-lookup"><span data-stu-id="3caa6-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="3caa6-167">Määritä organisaation määrityksen ja toteutusryhmän ohjeistuksen perusteella, käytetäänkö kulujen hallinnassa käytettyjä luokkia vain kuluissa vai jaetaanko ne projektinhallinnan ja kirjanpidon sekä kulujen kesken.</span><span class="sxs-lookup"><span data-stu-id="3caa6-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="3caa6-168">Huomaa, että nämä luokat voidaan jakaa projektin ja kuljen tai projektin tai tuotannon kesken mutta ei kulujen ja tuotannon kesken.</span><span class="sxs-lookup"><span data-stu-id="3caa6-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="3caa6-169">Jokaisen kululuokan kohdalla on tehtävä seuraavat päätökset.</span><span class="sxs-lookup"><span data-stu-id="3caa6-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="3caa6-170">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-170">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-171">Mikä on kululuokka?</span><span class="sxs-lookup"><span data-stu-id="3caa6-171">What is the expense category?</span></span> <span data-ttu-id="3caa6-172">Esimerkkiluokkia ovat lennot, hotellit tai kilometrikorvaukset.</span><span class="sxs-lookup"><span data-stu-id="3caa6-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="3caa6-173">Voiko tätä kululuokkaa käyttää myös projektinhallinnassa ja kirjapidossa?</span><span class="sxs-lookup"><span data-stu-id="3caa6-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="3caa6-174">Mikä on kulutyyppi?</span><span class="sxs-lookup"><span data-stu-id="3caa6-174">What is the expense type?</span></span>
- <span data-ttu-id="3caa6-175">Mikä on kululuokan oletusmaksutapa?</span><span class="sxs-lookup"><span data-stu-id="3caa6-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="3caa6-176">Tuleeko kuluraportin kulujen olla eriteltyjä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="3caa6-177">Mikä on kululuokan oletuspäätili?</span><span class="sxs-lookup"><span data-stu-id="3caa6-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="3caa6-178">Mikä on kululuokan oletusarvoinen nimikkeen arvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="3caa6-179">Salliiko kululuokka lisämaksutavat?</span><span class="sxs-lookup"><span data-stu-id="3caa6-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="3caa6-180">Jos muut maksutavat ovat sallittuja, mitkä maksutavat?</span><span class="sxs-lookup"><span data-stu-id="3caa6-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="3caa6-181">Onko kululuokalla alaluokkia?</span><span class="sxs-lookup"><span data-stu-id="3caa6-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="3caa6-182">Jos alaluokkia on, tee lisäksi seuraavat päätökset:</span><span class="sxs-lookup"><span data-stu-id="3caa6-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="3caa6-183">Jätetäänkö alaluokat veronpalautusten ulkopuolelle?</span><span class="sxs-lookup"><span data-stu-id="3caa6-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="3caa6-184">Mikä on alaluokkien nimikkeiden arvonlisäveroryhmä?</span><span class="sxs-lookup"><span data-stu-id="3caa6-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="3caa6-185">Jos tätä kululuokkaa käytetään myös projektinhallinnassa ja kirjanpidossa, vastaa jäljellä oleviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="3caa6-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="3caa6-186">Muussa tapauksessa siirry seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="3caa6-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="3caa6-187">Mitä kustannustilejä käytetään seuraavissa kuluissa?</span><span class="sxs-lookup"><span data-stu-id="3caa6-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="3caa6-188">Kustannus</span><span class="sxs-lookup"><span data-stu-id="3caa6-188">Cost</span></span>
    - <span data-ttu-id="3caa6-189">Palkanlaskennan kohdistus</span><span class="sxs-lookup"><span data-stu-id="3caa6-189">Payroll allocation</span></span>
    - <span data-ttu-id="3caa6-190">KET - kustannusarvo</span><span class="sxs-lookup"><span data-stu-id="3caa6-190">WIP-cost value</span></span>
    - <span data-ttu-id="3caa6-191">Kustannukset – nimike</span><span class="sxs-lookup"><span data-stu-id="3caa6-191">Cost-item</span></span>
    - <span data-ttu-id="3caa6-192">KET - Kustannusarvo - Nimike</span><span class="sxs-lookup"><span data-stu-id="3caa6-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="3caa6-193">Jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="3caa6-193">Accrued loss</span></span>
    - <span data-ttu-id="3caa6-194">KET– jaksotettu tappio</span><span class="sxs-lookup"><span data-stu-id="3caa6-194">WIP-accrued loss</span></span>

- <span data-ttu-id="3caa6-195">Mitä tuottotilejä käytetään seuraavissa?</span><span class="sxs-lookup"><span data-stu-id="3caa6-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="3caa6-196">Laskutettu tuotto</span><span class="sxs-lookup"><span data-stu-id="3caa6-196">Invoiced revenue</span></span>
    - <span data-ttu-id="3caa6-197">Jaksotettu tuotto – myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="3caa6-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="3caa6-198">KET – myyntiarvo</span><span class="sxs-lookup"><span data-stu-id="3caa6-198">WIP-sales value</span></span>
    - <span data-ttu-id="3caa6-199">Jaksotettu tuotto – tuotanto</span><span class="sxs-lookup"><span data-stu-id="3caa6-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="3caa6-200">KET – tuotanto</span><span class="sxs-lookup"><span data-stu-id="3caa6-200">WIP-production</span></span>
    - <span data-ttu-id="3caa6-201">Jaksotettu tuotto – voitto</span><span class="sxs-lookup"><span data-stu-id="3caa6-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="3caa6-202">KET – voitto</span><span class="sxs-lookup"><span data-stu-id="3caa6-202">WIP-profit</span></span>
    - <span data-ttu-id="3caa6-203">Jaksotettu tuotto – ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="3caa6-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="3caa6-204">KET – ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="3caa6-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="3caa6-205">Verot</span><span class="sxs-lookup"><span data-stu-id="3caa6-205">Taxes</span></span>

<span data-ttu-id="3caa6-206">Kuluihin liittyvissä veroissa on määritettävä, mitä sisällytetään tai otetaan käyttöön kuluraporteissa.</span><span class="sxs-lookup"><span data-stu-id="3caa6-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="3caa6-207">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-207">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-208">Sisältyykö arvonlisävero kulusummiin?</span><span class="sxs-lookup"><span data-stu-id="3caa6-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="3caa6-209">Otetaanko veronpalautukset käyttöön kuluissa?</span><span class="sxs-lookup"><span data-stu-id="3caa6-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="3caa6-210">Jos olet päättänyt käyttää yhdysvaltain arvonlisä- ja käyttöverosääntöjä kirjanpidon suunnittelussa, et voi käyttää kuluissa veronpalautusta.</span><span class="sxs-lookup"><span data-stu-id="3caa6-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="3caa6-211">(Jos haluat käyttää yhdysvaltain arvonlisä- ja käyttöverosääntöjä, määritä **Käytä arvonlisäverotuksen sääntöjä** -asetukseksi **Kyllä**.)</span><span class="sxs-lookup"><span data-stu-id="3caa6-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="3caa6-212">Käytännöt</span><span class="sxs-lookup"><span data-stu-id="3caa6-212">Policies</span></span>

<span data-ttu-id="3caa6-213">Voit luoda kuluraporttikäytäntöjä, joilla organisaatio voi säästää aikaa ja rahaa, kun työntekijät aiheuttavat kuluja yrityksen nimissä.</span><span class="sxs-lookup"><span data-stu-id="3caa6-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="3caa6-214">Käytännöt varmistavat, että työntekijät noudattavat budjettia, antavat kaikki tarvittavat tiedot ja kuluttavat rahaa vain tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="3caa6-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="3caa6-215">Seuraavat päätökset on tehtävä jokaisen kuluraporttikäytännön ja jokaisen luomasi kuluraportin hyväksyntäkäytännön kohdalla.</span><span class="sxs-lookup"><span data-stu-id="3caa6-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="3caa6-216">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="3caa6-216">**Decisions:**</span></span>

- <span data-ttu-id="3caa6-217">Mikä on käytännön nimi?</span><span class="sxs-lookup"><span data-stu-id="3caa6-217">What is the name of the policy?</span></span>
- <span data-ttu-id="3caa6-218">Mitä on kulukäytännön tarkoitus?</span><span class="sxs-lookup"><span data-stu-id="3caa6-218">What is the expense policy for?</span></span>
- <span data-ttu-id="3caa6-219">Jos olet aiemmin päättänyt ottaa konsernin sisäiset kulut käyttöön, missä organisaation yrityksissä käytäntöä käytetään?</span><span class="sxs-lookup"><span data-stu-id="3caa6-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="3caa6-220">Mikä käytäntö otetaan käyttöön?</span><span class="sxs-lookup"><span data-stu-id="3caa6-220">When does the policy become effective?</span></span>
- <span data-ttu-id="3caa6-221">Milloin käytäntö vanhentuu?</span><span class="sxs-lookup"><span data-stu-id="3caa6-221">When does the policy expire?</span></span>
- <span data-ttu-id="3caa6-222">Mikä on käytäntösääntö?</span><span class="sxs-lookup"><span data-stu-id="3caa6-222">What is the policy rule?</span></span>
- <span data-ttu-id="3caa6-223">Mikä on käytäntösäännön tulos?</span><span class="sxs-lookup"><span data-stu-id="3caa6-223">What is the outcome of the policy rule?</span></span>

