---
title: Luotonhallinnan määritys
description: Tässä ohjeaiheessa kuvataan luottohallinnan edellyttämät määritykset.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c54c74af6f2c1be9aedfa792d0676d1165fb0ab8
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015209"
---
# <a name="credit-management-setup"></a><span data-ttu-id="ca4fc-103">Luotonhallinnan määritys</span><span class="sxs-lookup"><span data-stu-id="ca4fc-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="ca4fc-104">Luotonhallinnan työnkulut</span><span class="sxs-lookup"><span data-stu-id="ca4fc-104">Credit management workflows</span></span>

<span data-ttu-id="ca4fc-105">Siirry kohtaan **Luotonvalvonta \> Määritys \> Luotonhallinnan työnkulut** määrittämään työnkulut, joita käytetään luottorajojen muutoksiin.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="ca4fc-106">Voit luoda työnkulun, jonka avulla voit hyväksyä luottorajojen muutoksia erittäin yhdellä hyväksynnällä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="ca4fc-107">Voit lisätä työnkulun rivitasolla, jolloin luottorajan muutokset voidaan hyväksyä yksitellen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="ca4fc-108">Voit luoda vapauttavat työnkulun, joka ohjaa pidot automaattisesti työnkulkuprosessiin.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="ca4fc-109">Estosäännöt</span><span class="sxs-lookup"><span data-stu-id="ca4fc-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="ca4fc-110">Maksuehtojen järjestäminen</span><span class="sxs-lookup"><span data-stu-id="ca4fc-110">Ranking payment terms</span></span>

<span data-ttu-id="ca4fc-111">Voit asettaa myyntitilauksen pitoon, jos sen maksuehdot eivät vastaa asiakkaan oletusarvoisia maksuehtoja.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="ca4fc-112">Joskus maksuehdot kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="ca4fc-113">Voit järjestää maksuehtoja siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="ca4fc-114">Jos maksuehtojen järjestysnumerot ovat käytössä, myyntitilaukset siirretään pitoon, jos tilauksen maksuehdot ovat järjestyksessä asiakkaan oletusmaksuehtoja korkeammalla.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="ca4fc-115">Tilitysalennusten järjestäminen</span><span class="sxs-lookup"><span data-stu-id="ca4fc-115">Ranking settlement discounts</span></span>

<span data-ttu-id="ca4fc-116">Voit asettaa myyntitilauksen pitoon, jos sen käteisalennus ei vastaa asiakkaan oletusarvoista käteisalennusta.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="ca4fc-117">Joskus käteisalennukset kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="ca4fc-118">Voit järjestää käteisalennuksia siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="ca4fc-119">Jos käteisalennusten järjestysnumerot ovat käytössä, myyntitilaukset siirretään pitoon, jos tilauksen käteisalennus on järjestyksessä asiakkaan oletuskäteisalennusta korkeammalla.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="ca4fc-120">Syyt</span><span class="sxs-lookup"><span data-stu-id="ca4fc-120">Reasons</span></span>

<span data-ttu-id="ca4fc-121">Luotonhallinnassa käytetään monenlaisia syitä:</span><span class="sxs-lookup"><span data-stu-id="ca4fc-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="ca4fc-122">Pidon syyt ilmaisevat, miksi myyntitilaus on asetettu pitoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="ca4fc-123">Vapautuksen syyt määritetään tilaukselle, kun se vapautetaan pidosta.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="ca4fc-124">Tilan syyt ilmaisevat, miksi asiakkaalle on määritetty tietty tilin tila.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="ca4fc-125">Voit määrittää syitä **Luotonhallinnan syyt** -sivulla (**Luotonhallinta \> Määritys \> Luotonhallinta \> Luotonhallinnan syyt**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="ca4fc-126">Valitse **Syyn tyyppi** -kentässä syyn tyyppi: **Pito**, **Vapautus** tai **Tila**.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="ca4fc-127">Syötä **Syy**-kenttään syyn nimi.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="ca4fc-128">Anna **Kuvaus**-kentässä syykoodin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="ca4fc-129">Luotonhallinnan ryhmät</span><span class="sxs-lookup"><span data-stu-id="ca4fc-129">Credit management groups</span></span>

<span data-ttu-id="ca4fc-130">Luotonhallintaryhmiä käytetään sellaisten asiakkaiden tai asiakasryhmien tunnistamineen, joilla on samat luotonhallinnan ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="ca4fc-131">Luotonhallintaryhmien avulla voidaan esimerkiksi määrittää asiakkaiden estävät ja poissulkevat luotonhallintasäännöt.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="ca4fc-132">Voit luoda luotonhallintaryhmiä **Luotonhallintaryhmät**-sivulla (**Luotonhallinta \> Määritys> Ryhmien määritys \> Luotonhallinnan ryhmät**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="ca4fc-133">Valitse **Uusi** luodaksesi rivin.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="ca4fc-134">Syötä ryhmälle tunnus.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-134">Enter an ID for the group.</span></span> <span data-ttu-id="ca4fc-135">Tunnuksessa voi olla jopa 10 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="ca4fc-136">Syötä ryhmälle nimi **Kuvaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="ca4fc-137">Nimessä voi olla jopa 60 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="ca4fc-138">Luotonhallintaryhmä osoitetaan asiakkaalle **Luotonvalvonta**-pikavälilehdessä sivulla **Kaikki asiakkaat** (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="ca4fc-139">Tilin tilat</span><span class="sxs-lookup"><span data-stu-id="ca4fc-139">Account statuses</span></span>

<span data-ttu-id="ca4fc-140">Voit luoda tilitiloja asiakastilin luottokelpoisuuden tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="ca4fc-141">Voit määrittää tilan ja sen vaikutuksen laskutuksen ja toimituksen pidossa oleviin prosesseihin.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="ca4fc-142">Tilitiloja voi käyttää myös asiakkaan esto ääntöjen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="ca4fc-143">Voit luoda tilitiloja **Tilitilat**-sivulla (**Luotonhallinta \> Määritys> Ryhmien määritys \> Tilitilat**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="ca4fc-144">Lisää tilitila ja anna sille kuvaus, joka edustaa asiakkaan luottokelpoisuutta.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="ca4fc-145">Käytä esimerkiksi tilaa **Normaali** ilmaisemaan, että asiakkaan kelpoisuus on hyvä ja että avoimiin tilauksiin sovelletaan tavanomaista luotonhallintakäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="ca4fc-146">Valitse kentissä **Laskutus** ja **Toimitus pidossa** pidon tyyppi, joka toteutetaan niiden asiakkaiden osalta, joilla on tämä tilitila.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="ca4fc-147">Voit asettaa kaiken käsittelyn pitoon, asettaa pitoon vain laskujen käsittelyn tai olla asettamatta pitoon mitään käsittelyä, kun luottorajasääntöjä sovelletaan.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="ca4fc-148">Pisteytysryhmät</span><span class="sxs-lookup"><span data-stu-id="ca4fc-148">Scoring groups</span></span>

<span data-ttu-id="ca4fc-149">Voit määrittää pisteytysryhmiä määrittämään riskitekijöitä sekä kriteerejä, joiden perusteella niitä mitataan.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="ca4fc-150">Kun asiakasta koskevia tietoja käytetään pisteytysryhmässä, kullekin riskitekijälle lasketaan pistemäärä, jonka perusteella asiakas asetetaan riskiryhmään.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="ca4fc-151">Riskiryhmää voidaan käyttää luottokelpoisuuden tunnistamiseen ja automaattisten luottorajojen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="ca4fc-152">Vuot luoda pisteytysryhmiä **Pisteytysryhmät** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Pisteytysryhmät**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="ca4fc-153">Luo pisteytysryhmä ja anna sille nimi.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="ca4fc-154">Anna kuvaus tarkempia pisteytysryhmän tietoja varten.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="ca4fc-155">Valitse ryhmätyyppi.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-155">Select a group type.</span></span> <span data-ttu-id="ca4fc-156">Esimääritettyjä tyyppejä on kahdeksan.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-156">There are eight predefined types.</span></span> <span data-ttu-id="ca4fc-157">Voit myös määrittää paremmin organisaatiollesi sopivan ryhmätyypin valitsemalla **Käyttäjän määrittämä**.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="ca4fc-158">Valitse pistetyyppi määrittääksesi, miten pisteytysryhmä laskee riskipisteet.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="ca4fc-159">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ca4fc-159">The following options are available:</span></span>

    - <span data-ttu-id="ca4fc-160">**Alue** – Tämän vaihtoehdon avulla voit määrittää arvoalueen, jota käytetään pistemäärän laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="ca4fc-161">**Käyttäjän määrittämä** – Tämän vaihtoehdon avulla voit määrittää manuaalisesti arvoluettelon, jota käytetään pistemäärän laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="ca4fc-162">Jos valitsit pistetyypiksi **Alue**, lisää rivejä arvoalueen ja sitä vastaavien pisteiden määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="ca4fc-163">Määritä **Arvosta**-kentässä alueen alhaisin arvo.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="ca4fc-164">Määritä **Arvoon**-kentässä alueen korkein arvo.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="ca4fc-165">Syötä **Pistemäärä**-kenttään se pistemäärä, joka osoitetaan, kun annettu arvo on alueella Arvosta–Arvoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="ca4fc-166">Jos valitsit pistetyypiksi **Käyttäjän määrittämä**, lisää rivejä arvoalueen ja käyttäjän määrittämien pisteiden määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="ca4fc-167">Syötä **Arvo**-kenttään se käyttäjän määrittämä arvo, joka pitäisi saada asiakastiedoista.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="ca4fc-168">Syötä **Pistemäärä**-kenttään se pistemäärä, joka osoitetaan, kun annettu arvo on alueella Arvosta–Arvoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="ca4fc-169">Riskinarvioinnit</span><span class="sxs-lookup"><span data-stu-id="ca4fc-169">Risk assessments</span></span>

<span data-ttu-id="ca4fc-170">Voit määrittää riskinarviointeja, jotka voidaan osoittaa asiakkaille niiden riskipisteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="ca4fc-171">Riskipisteet lasketaan vertaamalla asiakkaan tietoja kuhunkin pisteytysryhmään.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="ca4fc-172">Tulokset lasketaan yhteen ja kokonaispistemäärää verrataan riskiryhmän määrityksiin, jotta asiakkaan edustama riskiryhmä voidaan tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="ca4fc-173">Riskiryhmän pistemäärää käytetään sitten luotonhallinnan esto- ja poissulkemissääntöjen määrittämiseen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="ca4fc-174">Voit määrittää riskiryhmiä **Riskinarvioinnit** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Riskinarvioinnit**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="ca4fc-175">Syötä riskiryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="ca4fc-176">Anna kuvaus tarkempia riskiryhmän tietoja varten.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="ca4fc-177">Määritä pistealue, jota käytetään sen selvittämiseen, mitkä asiakkaat kuuluvat riskiryhmään.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="ca4fc-178">Valitse riskiryhmän ilmaisin valitaksesi symbolin, joka edustaa riskiryhmää.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="ca4fc-179">Takaus-/vakuutustyypit</span><span class="sxs-lookup"><span data-stu-id="ca4fc-179">Guarantee/insurance types</span></span>

<span data-ttu-id="ca4fc-180">Voit määrittää takaus-/vakuutustyyppejä **Takaus-/vakuutustyypit**-sivulla (**Luotonhallinta \> Määritys \> Takausten/vakuutuksien määritys \> Takaus-/vakuutustyypit**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="ca4fc-181">Määritä takaus- tai vakuutustyyppi, joka ilmaisee takaajan tai vakuutuksenvälittäjän nimen.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="ca4fc-182">Anna takaajalle/vakuutuksenvälittäjälle kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="ca4fc-183">Kattavuustyypit</span><span class="sxs-lookup"><span data-stu-id="ca4fc-183">Coverage types</span></span>

<span data-ttu-id="ca4fc-184">Kattavuustyyppejä voidaan käyttää vakuutuskäytäntöjen tarkempaan luokitteluun.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="ca4fc-185">Niitä ei voi käyttää takuiden yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="ca4fc-186">Voit lisätä kattavuustyyppejä **Kattavuustyypit**-sivulla (**Luotonhallinta \> Määritys \> Takuun/vakuutuksen määritys \> Coverage types**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="ca4fc-187">Anna kattavuustyyppi sen kattavuustyypin määrittämiseksi, joka lisätään vakuutuksena tai takuuna.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="ca4fc-188">Anna kattavuustyypille kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="ca4fc-189">Automaattiset luottorajat</span><span class="sxs-lookup"><span data-stu-id="ca4fc-189">Automatic credit limits</span></span>

<span data-ttu-id="ca4fc-190">Voit luoda automaattisten luottorajojen kriteerejä **Automaattiset luottorajat** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Automaattiset luottorajat**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="ca4fc-191">Valitse riskiryhmä, jolle automaattinen luottoraja määritetään.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="ca4fc-192">Valitse automaattisen luottorajan valuutta.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="ca4fc-193">Voit luoda useita automaattisia luottorajoja eri valuutoissa samalle riskiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="ca4fc-194">Syötä se tuottosumma, joka edustaa suurinta yrityksen tuottoa, jota tässä automaattisessa luottorajassa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="ca4fc-195">Kun luottorajoja luodaan, tuottosummaa verrataan tuottoarvoon **Taloushallinto** -sivulla (**Myyntireskontra \> Kaikki asiakkaat \> Valitse asiakas \> Yleistä \> Tilastot \> Talous**).</span><span class="sxs-lookup"><span data-stu-id="ca4fc-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="ca4fc-196">Järjestelmä käyttää **Yleiskatsaus**-osan viimeisintä arvoa.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="ca4fc-197">Seuraavien vaiheiden avulla voit lisätä valittujen kriteerien perusteella luotavaa luottorajaa edustavia rivejä.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="ca4fc-198">Valitse pisteytysryhmä, joka määrittää luottorajan laskemisessa käytettävät asiakastiedot.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="ca4fc-199">Valitse vertailuoperaattori, joka määrittää, miten pisteytysryhmän tiedot arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="ca4fc-200">Määritä arvo, jota verrataan pisteytysryhmälle määritettyyn arvoon.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="ca4fc-201">Määritä luottoraja, joka määritetään, jos asiakastiedot vastaavat pisteytysryhmälle määritettyä arvoa.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="ca4fc-202">Voit esimerkiksi luoda automaattisen luottorajan **Alahainen pistemäärä** -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="ca4fc-203">Jos toiminta-aika on yksi pisteytysryhmistä, voit määrittää yhden rivin, joka määrittää luottorajaksi 100 000, jos asiakas on toiminut viisi vuotta ja toisen rivin, joka määrittää luottorajaksi 200 000, jos asiakas on toiminut 10 vuoden ajan.</span><span class="sxs-lookup"><span data-stu-id="ca4fc-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
