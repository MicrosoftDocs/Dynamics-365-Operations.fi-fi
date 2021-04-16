---
title: Hintojen, alennusten, sopimusten ja ostohyvitysten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita hintojen, alennusten, sopimusten ja ostohyvitysten käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 12bc3cbccb1577c278489f640299510b3ced17e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811083"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="722ed-103">Hintojen, alennusten, sopimusten ja ostohyvitysten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="722ed-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="722ed-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita hintojen, alennusten, sopimusten ja ostohyvitysten käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="722ed-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="722ed-105">En saa linkitettyä ostotilausta ostotilausriviin, kun ostotilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="722ed-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="722ed-106">Ostosopimus on yhdistettävä ostotilaukseen, kun ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="722ed-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="722ed-107">Muussa tapauksessa ostotilausrivejä ei voi liittää ostosopimusriveihin.</span><span class="sxs-lookup"><span data-stu-id="722ed-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="722ed-108">Mikä tarkistus tuottaa sanoman "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja"?</span><span class="sxs-lookup"><span data-stu-id="722ed-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="722ed-109">Kun muutat lähetyspäivämäärää, näyttöön voi tulla sanoma "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja"</span><span class="sxs-lookup"><span data-stu-id="722ed-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="722ed-110">Saat tämän sanoman, koska jos lähetyspäivämäärää muutetaan, muu kauppa- tai myyntisopimus saattaa tulla voimaan ja aiheuttaa hinnanmuutoksen.</span><span class="sxs-lookup"><span data-stu-id="722ed-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="722ed-111">Toimituspäivämäärän muuttaminen voi vaikuttaa myös fyysisen varastoinnin aikatauluihin ja liittyviin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="722ed-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="722ed-112">Sanoma luodaan, kun jokin päivämääristä tai muista parametreista muuttuu.</span><span class="sxs-lookup"><span data-stu-id="722ed-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="722ed-113">Sanoman tarkoitus on varmistaa, että olet tietoinen hinnanmuutoksista, joita voi aiheutua kyseisistä muutoksista.</span><span class="sxs-lookup"><span data-stu-id="722ed-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="722ed-114">Sanoma on kauppasopimuksen arviointi (TAE) -kehote.</span><span class="sxs-lookup"><span data-stu-id="722ed-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="722ed-115">Täydellinen kuvaus [Kauppasopimuksen arviointikäytännöt](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="722ed-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="722ed-116">Ostotilauksen kuitti ei sisällä kaikkia maksuja.</span><span class="sxs-lookup"><span data-stu-id="722ed-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="722ed-117">Ongelman toistaminen</span><span class="sxs-lookup"><span data-stu-id="722ed-117">Reproduce the issue</span></span>

<span data-ttu-id="722ed-118">Seuraavassa esitetään yksi tapa ongelman toistamiseen.</span><span class="sxs-lookup"><span data-stu-id="722ed-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="722ed-119">Varmista **Osto- ja hankintaparametrit** -sivun **Toimitus**-välilehdessä, että **Luo maksuja tuotteen vastaanottamisen yhteyteen** -asetuksen arvona on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="722ed-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="722ed-120">Luo ostotilaus, joka sisältää maksuja.</span><span class="sxs-lookup"><span data-stu-id="722ed-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="722ed-121">Vahvista ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="722ed-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="722ed-122">Vastaanota ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="722ed-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="722ed-123">Tarkista kuitin kokonaissumma ja vertaa sitä odotettuun summaan.</span><span class="sxs-lookup"><span data-stu-id="722ed-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="722ed-124">Huomaa, että kaikki maksut eivät sisälly ostotilauksen kuittiin.</span><span class="sxs-lookup"><span data-stu-id="722ed-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="722ed-125">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="722ed-125">Issue resolution</span></span>

<span data-ttu-id="722ed-126">Ratkaisu riippuu siitä, miten muut maksut on määritetty.</span><span class="sxs-lookup"><span data-stu-id="722ed-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="722ed-127">Lisätietoja muiden maksujen määrittämisestä vastaamaan tarpeitasi on seuraavassa blogikirjoituksessa: [Kirjaa muut kulut tuotteen vastaanoton yhteydessä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="722ed-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="722ed-128">Kauppasopimuksen hintoja ja alennuksia ei käytetä myynti- tai ostotilausriveillä, jotka tuodaan tiedonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="722ed-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="722ed-129">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="722ed-129">Issue description</span></span>

<span data-ttu-id="722ed-130">Myynti- tai ostotilausriveissä käytettäviä kauppasopimuksia ei käytetä riveillä, jotka tuodaan tiedonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="722ed-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="722ed-131">Samoja kauppasopimuksia käytetään kuitenkin manuaalisesti luoduissa myynti- tai ostotilausriveissä.</span><span class="sxs-lookup"><span data-stu-id="722ed-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="722ed-132">Ongelman syy</span><span class="sxs-lookup"><span data-stu-id="722ed-132">Reason for the issue</span></span>

<span data-ttu-id="722ed-133">Jos tiedonhallinnan kautta tuotavat ostotilausrivit sisältävät jo hintatietoja, kauppasopimusta ei arvioida uudelleen kyseisten rivien osalta.</span><span class="sxs-lookup"><span data-stu-id="722ed-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="722ed-134">Jos riville on määritetty **Rivialennusprosentti** tai jokin hinnan ja alennuksen arvoista, kauppasopimuksia ei etsitä kyseiselle riville.</span><span class="sxs-lookup"><span data-stu-id="722ed-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="722ed-135">Ongelman kiertotapa</span><span class="sxs-lookup"><span data-stu-id="722ed-135">Issue workaround</span></span>

<span data-ttu-id="722ed-136">Tämä toiminta on odotettavissa, ja se on samanlainen sekä myynti- että ostotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="722ed-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="722ed-137">Kiertotapana voit tuoda ostotilausrivit määrittämättä hintatietoja.</span><span class="sxs-lookup"><span data-stu-id="722ed-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="722ed-138">Tällöin sovelletaan kauppasopimuksia ja ostotilausrivit päivitetään määritettyjen kauppasopimusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="722ed-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="722ed-139">Toimittajan ostohyvitystä ei kerry laskujen perusteella.</span><span class="sxs-lookup"><span data-stu-id="722ed-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="722ed-140">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="722ed-140">Issue description</span></span>

<span data-ttu-id="722ed-141">Jos kirjatuilla laskuilla on eri eräpäivät, laskut eivät näy toimittajan ostohyvityksissä, jotka on luotu niiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="722ed-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="722ed-142">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="722ed-142">Issue resolution</span></span>

<span data-ttu-id="722ed-143">Eräpäivää ei tarkoituksella oteta huomioon toimittajan ostohyvitystä laskettaessa.</span><span class="sxs-lookup"><span data-stu-id="722ed-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="722ed-144">Harkitse järjestelmän mukauttamista siten, että eräpäivä ja suhde ovat ilmeisempiä todellisen toimittajan ostohyvityksen osalta.</span><span class="sxs-lookup"><span data-stu-id="722ed-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="722ed-145">Ostotilausten yksikköhintoja ei lasketa yksikkömuunnoksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="722ed-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="722ed-146">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="722ed-146">Issue description</span></span>

<span data-ttu-id="722ed-147">Kun yksikköä muutetaan ostotilauksessa, kauppasopimuksen hintoja ei lasketa uudelleen yksikkömuunnoksen määritysten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="722ed-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="722ed-148">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="722ed-148">Issue resolution</span></span>

<span data-ttu-id="722ed-149">Hinnat perustuvat aina kauppasopimuksiin (tai muihin järjestelmän hinta-asetuksiin, kuten myyntisopimuksiin tai nimikkeiden hintoihin), ja ne on määritetään yksikkökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="722ed-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="722ed-150">Jos yksikköä muutetaan tilausrivillä, järjestelmä hakee hinnan uudelle nimikkeelle ja soveltaa sitä.</span><span class="sxs-lookup"><span data-stu-id="722ed-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="722ed-151">Jos yksikölle ei löydy hintaa, järjestelmä ei käytä hintaa.</span><span class="sxs-lookup"><span data-stu-id="722ed-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="722ed-152">Yksikkömuunnosta ei voi käyttää hinnan uudelleenlaskemiseen toiseen yksikköön.</span><span class="sxs-lookup"><span data-stu-id="722ed-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="722ed-153">Teoriassa yhden laatikon hinta ei ehkä vastaa kymmentä kertaa yhden laatikon hintaa.</span><span class="sxs-lookup"><span data-stu-id="722ed-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="722ed-154">Ongelman kiertotapa</span><span class="sxs-lookup"><span data-stu-id="722ed-154">Issue workaround</span></span>

<span data-ttu-id="722ed-155">Yksi tapa kiertää tämä ongelma on varmistaa, että nimikkeen tilausriveillä käytetään odottamiasi yksiköitä koskevia kauppasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="722ed-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="722ed-156">Kauppasopimuksissa esiintyy valuutanmuunto-ongelmia.</span><span class="sxs-lookup"><span data-stu-id="722ed-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="722ed-157">Kauppasopimusten hintoja ei lasketa uudelleen valuutan mukaan, kun valuutta on ostotilauksessa eri.</span><span class="sxs-lookup"><span data-stu-id="722ed-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="722ed-158">*Yleinen valuutta* -toiminnon avulla voit määrittää hinnat ja alennukset vain yhdessä valuutassa.</span><span class="sxs-lookup"><span data-stu-id="722ed-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="722ed-159">Tällöin voit muuntaa muihin valuuttoihin tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="722ed-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="722ed-160">Lisäksi kun muunnos on tehty, toiminto voi automaattisesti käyttää taktista pyöristystä.</span><span class="sxs-lookup"><span data-stu-id="722ed-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="722ed-161">Kun avaan ostosopimussivun rivinäkymätilassa, en voi mukauttaa sivua lisäämällä hintayksikön kenttää rivin yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="722ed-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="722ed-162">Osaa sopimuskehyksen yhteisiä kenttiä ei voi sisällyttää yksilöinteihin.</span><span class="sxs-lookup"><span data-stu-id="722ed-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="722ed-163">Tämä rajoitus ilmenee käytettävän tietomallin vuoksi.</span><span class="sxs-lookup"><span data-stu-id="722ed-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="722ed-164">Siksi et voi mukauttaa **Hintayksikkö**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="722ed-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="722ed-165">Ostosopimuksen yläraja ei ole päde ostoehdotukseen.</span><span class="sxs-lookup"><span data-stu-id="722ed-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="722ed-166">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="722ed-166">Issue description</span></span>

<span data-ttu-id="722ed-167">Kun ostoehdotus linkitetään ostosopimukseen, ostosopimuksen yläraja ei päde ostoehdotukseen.</span><span class="sxs-lookup"><span data-stu-id="722ed-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="722ed-168">Oletushintatiedot on syötetty oikein, mutta ostoehdotuksella voit tilata ostosopimuksen ylärajan ylittävän määrän.</span><span class="sxs-lookup"><span data-stu-id="722ed-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="722ed-169">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="722ed-169">Issue resolution</span></span>

<span data-ttu-id="722ed-170">Tämä toiminta on tarkoituksellista.</span><span class="sxs-lookup"><span data-stu-id="722ed-170">This behavior is expected.</span></span> <span data-ttu-id="722ed-171">Koska ehdotuksia ei aina hyväksytä, määrää tai summaa ei pitäisi varata ostosopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="722ed-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="722ed-172">Siksi ostosopimuksen ylärajaa ei saavuteta.</span><span class="sxs-lookup"><span data-stu-id="722ed-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="722ed-173">Kauppasopimuksia voi luoda hylätyistä tarjouspyynnöistä.</span><span class="sxs-lookup"><span data-stu-id="722ed-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="722ed-174">Siksi järjestelmä ei estä kauppasopimusten kirjauskansioiden luomista, jos tarjouspyyntöriviä ei ole hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="722ed-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="722ed-175">Voit luoda kauppasopimuksia mille tahansa tarjouspyynnön vastaukselle riippumatta siitä, hyväksyttiinkö vai hylättiinkö vastaus.</span><span class="sxs-lookup"><span data-stu-id="722ed-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="722ed-176">Lisätietoja: [Tarjouspyyntöjen yleiskatsaus](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="722ed-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]