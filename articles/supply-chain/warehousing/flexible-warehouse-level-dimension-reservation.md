---
title: Joustava varastotason dimensionvarauskäytäntö
description: Tässä ohjeaiheessa kuvataan varaston varauskäytäntö, joka mahdollistaa eräseurattuja tuotteita myyville ja niiden logistiikan varastonhallintajärjestelmän toiminnoilla toteuttaville yrityksille tiettyjen erien varaamisen asiakkaiden myyntitilauksille, vaikka tuotteiden varaushierarkia ei salli tiettyjen erien varausta.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 13b81459fe3449a90839dac7637118f09afe2e55
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910230"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="e2b22-103">Joustava varastotason dimensioiden varauskäytäntö</span><span class="sxs-lookup"><span data-stu-id="e2b22-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2b22-104">Kun *Erä alla\[sijainti\]*-tyyppinen varastonvaraushierarkia yhdistetään tuotteisiin, eräseurattuja tuotteita myyvät ja niiden logistiikan Microsoft Dynamics 365 -varastonhallintajärjestelmävalmiilla (WMS) toiminnoilla toteuttavat yritykset eivät voi varata tiettyjä kyseisten tuotteiden eriä asiakkaiden myyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="e2b22-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="e2b22-105">Samalla tavalla tiettyjä rekisterikilpiä ei voi varata myyntitilausten tuotteille, kun nämä tuotteet on liitetty oletusvaraushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="e2b22-106">Tässä ohjeaiheessa kuvataan varastonvarauskäytäntö, jonka avulla nämä yritykset varaavat tiettyjä eriä tai rekisterikilpiä, vaikka tuotteet on yhdistetty *\[Erä alla\]sijainti*-varaushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="e2b22-107">Varastovaraushierarkia</span><span class="sxs-lookup"><span data-stu-id="e2b22-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="e2b22-108">Tässä osassa on yhteenveto olemassa olevasta varastonvaraushierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="e2b22-109">Varaston varaushierarkia määrittää, että varastodimensioiden osalta kysyntätilauksella on toimipaikan, varaston ja varaston tilan pakolliset dimensiot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="e2b22-110">Pakolliset dimensiot ovat toisin sanoen kaikki varaushierarkian sijaintidimension yläpuolella olevat dimensiot, kun taas varastologiikka vastaa sijainnin määrittämisestä pyydetyille määrille ja sijainnin varaamisesta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="e2b22-111">Kysyntätilauksen ja varastotoimintojen välisissä vuorovaikutuksissa kysyntätilauksen oletetaan ilmaisevan, mistä tilaus on lähetettävä (eli mistä toimipaikasta ja varastosta).</span><span class="sxs-lookup"><span data-stu-id="e2b22-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="e2b22-112">Tämän jälkeen varasto tukeutuu logiikkaan löytääkseen vaaditun määrän varastotilasta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="e2b22-113">Yrityksen toimintamallin heijastamista varten seurantadimensiot (erä- ja sarjanumerot) ovat joustavampia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="e2b22-114">Varastonvaraushierarkia voi mukautua seuraavankaltaisiin tilanteisiin:</span><span class="sxs-lookup"><span data-stu-id="e2b22-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="e2b22-115">Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot, sen *jälkeen*, kun määrät on löydetty varaston säilytystilasta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="e2b22-116">Tätä mallia kutsutaan usein nimellä *\[Erä alla\]sijainti* tai *Sarja alla\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="e2b22-117">Sitä käytetään yleensä silloin, kun tuotteen erä- tai sarjanumeron tunnistus ei ole tärkeä asiakkaille, jotka tekevät pyynnön myyjäyritykselle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="e2b22-118">Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot *ennen* kuin määrät on löydetty varaston säilytystilasta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="e2b22-119">Jos erä- tai sarjanumerot ovat välttämätön osa asiakkaan tilausmääritystä ja ne tallennetaan kysyntätilaukseen, varastotoiminnot, jotka etsivät määrät varastosta, eivät voi muuttaa niitä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="e2b22-120">Tätä mallia kutsutaan nimellä *\[Erä yläpuolella\]sijainti* tai *Sarja yläpuolella\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="e2b22-121">Koska sijainnin yläpuolella olevat dimensiot ovat niiden vaatimusten erityisvaatimuksia, jotka on täytettävä, varastointilogiikka ei kohdista niitä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="e2b22-122">Nämä dimensiot **pitää** aina määrittää kysyntätilauksessa tai siihen liittyvissä varauksissa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="e2b22-123">Näissä skenaarioissa haasteena on, että kullekin vapautetulle tuotteelle voidaan määrittää vain yksi varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="e2b22-124">Siksi, jotta varastonhallintajärjestelmä määrittäisi hierarkian määrittämisen jälkeen, milloin erä- tai sarjanumero pitäisi varata (joko kun kysyntätilaus saadaan tai varaston keräilytyön aikana), kyseistä ajoitusta ei voi muuttaa tilannekohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="e2b22-125">Eräseurattujen nimikkeiden joustava varaus</span><span class="sxs-lookup"><span data-stu-id="e2b22-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="e2b22-126">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="e2b22-126">Business scenario</span></span>

<span data-ttu-id="e2b22-127">Tässä skenaariossa yritys käyttää varastostrategiaa, jossa valmiita tavaroita seurataan eränumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="e2b22-128">Yritys käyttää myös varastonhallinnan työkuormitusta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="e2b22-129">Koska tässä työkuormituksessa on hyvin toimiva logiikka varaston keräily- ja lähetystoimintojen suunnittelulle ja suorittamiselle erämääräisiä nimikkeitä varten, useimmille valmiille nimikkeille määritetään *Erä alla\[sijainti\]* -varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="e2b22-130">Tällaisen operatiivisen määrityksen etuna on, että päätöksiä (jotka ovat käytännössä varauspäätöksiä) siitä, mitkä erät kerätään ja mihin ne laitetaan varastossa, lykätään siihen asti, että varastoin keräilytoiminnot alkavat.</span><span class="sxs-lookup"><span data-stu-id="e2b22-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="e2b22-131">Niitä ei tehdä, kun asiakkaan tilaus saadaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="e2b22-132">Vaikka *Erä alla\[sijainti\]* -varaushierarkia palvelee yrityksen liiketoimintatavoitteita hyvin, monet yrityksen vakiintuneista asiakkaista tarvitsevat aikaisemmin ostamansa erää, kun ne tilaavat tuotteita uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="e2b22-133">Siksi yritys etsii joustavuutta erävaraussääntöjen käsittelyyn, jotta asiakkaan samaa nimikettä koskevasta kysynnästä riippuen, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="e2b22-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="e2b22-134">Eränumero voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi muuttaa varastotoimintojen aikana ja/tai osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="e2b22-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="e2b22-135">Tämä auttaa takaamaan, että tilattu eränumero toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="e2b22-136">Jos eränumerolla ei ole merkitystä asiakkaalle, varastotoiminnot voivat määrittää eränumeron keräilyn aikana, kun myyntitilauksen kirjaus ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="e2b22-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="e2b22-137">Tietyn erän myyntilaukselle varaamisen mahdollistaminen</span><span class="sxs-lookup"><span data-stu-id="e2b22-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="e2b22-138">Jotta haluttu erävarauksen joustavuus mahdollistetaan nimikkeille, joilla on *Erä alla\[sijainti\]* -varastonvaraushierarkia, varastopäällikköjen on valittava **Salli varaus kysyntätilauksessa** -valintaruutu **Eränumero** -tasolla sivulla **Varastonvaraushierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varastovarausten hierarkian joustavoittaminen](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="e2b22-140">Kun hierarkian **Eränumero**-taso on valittuna, kaikki kyseisen tason yläpuolella olevat dimensiot aina **Sijainti**-tasolle valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="e2b22-141">(Oletusarvoisesti kaikki **Sijainti**-tason yläpuolella olevat dimensiot on esivalittu.) Tämä toiminta perustuu logiikkaan, jossa myös kaikki eränumeron ja sijainnin välisen alueen dimensiot varataan automaattisesti, kun varaat tietyn eränumeron tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-142">**Salli varaus kysyntätilauksessa** -valintaruutu pätee vain varaushierarkiatasoille, jotka ovat varastosijainnin dimension alapuolella.</span><span class="sxs-lookup"><span data-stu-id="e2b22-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="e2b22-143">**Eränumero** ja **rekisterikilpi** ovat hierarkian ainoat tasot, joihin joustavaa varauskäytäntöä voi soveltaa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="e2b22-144">Toisin sanoen et voi valita **Salli varaus kysyntätilauksessa** -valintaruutua **Sijainti**- tai **Sarjanumero**-tasolle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="e2b22-145">Jos varaushierarkia sisältää sarjanumerodimension (jonka on aina oltava **Eränumero**-tason alapuolella) ja jos olet ottanut eräkohtaisen varauksen käyttöön eränumerolle, järjestelmä jatkaa sarjanumeroiden varaus- ja keräilytoimintojen käsittelyä niiden sääntöjen perusteella, jotka pätevät *Sarja alla\[sijainti\]* -varauskäytäntöön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="e2b22-146">Voit missä tahansa vaiheessa ottaa eräkohtaisenvarauksen käyttöön olemassa olevalle *Erä alla\[sijainti\]* -varaushierarkialle ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="e2b22-147">Tämä muutos ei vaikuta varauksiin ja avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="e2b22-148">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos varasto-ottotyypin **Varattu tilattu**, **Varattu fyysinen** tai **Tilattu** varastotapahtumia on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-149">Jos nimikkeen käytössä oleva varaushierarkia ei salli erän määritystä tilauksessa, voit siirtää sen varaushierarkiaan, joka sallii erän määrityksen, kunhan hierarkiatasorakenne on sama molemmissa hierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="e2b22-150">Tee siirto toiminnolla **Muuta nimikkeiden varaushierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="e2b22-151">Tästä muutoksesta voi olla hyötyä, kun haluat estää eräseurattujen nimikkeiden alijoukon joustavan erävarauksen, mutta sallia sen muun tuoteportfolion osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="e2b22-152">Riippumatta siitä, oletko valinnut **Salli varaus kysyntätilauksessa** -valintaruudun, jos et halua varata nimikkeelle tiettyä eränumeroa tilausrivillä, oletusarvoinen varastotoimintologiikka, jota sovelletaan *Erä alla\[sijainti\]* -varaushierarkiaan, pätee edelleen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="e2b22-153">Tietyn eränumeron varaaminen asiakastilausta varten</span><span class="sxs-lookup"><span data-stu-id="e2b22-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="e2b22-154">Kun eräseuratun nimikkeen *Erä alla\[sijainti\]* -varastonvaraushierarkia on määritetty sallimaan tiettyjen eränumeroiden varaaminen myyntitilauksissa, myyntitilausten käsittelijät voivat ottaa saman nimikkeen asiakastilauksia vastaan jollakin seuraavista tavoista asiakkaan pyynnöstä riippuen:</span><span class="sxs-lookup"><span data-stu-id="e2b22-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="e2b22-155">**Anna tilaustiedot ilman eränumeron määritystä** – Tätä menetelmää kannattaa käyttää, kun tuotteen erämääritys ei ole tärkeä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="e2b22-156">Kaikki aiemmin luodut prosessit, jotka liittyvät tällaisen tilauksen käsittelyyn, eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="e2b22-157">Käyttäjiltä ei vaadita lisätoimia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="e2b22-158">**Anna tilaustiedot ja varaa tietty eränumero** – Tätä menetelmää kannattaa käyttää, kun asiakas pyytää tiettyä erää.</span><span class="sxs-lookup"><span data-stu-id="e2b22-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="e2b22-159">Yleensä asiakkaat pyytävät tiettyä erää, kun he tilaavat uudelleen aiemmin ostamaansa tuotetta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="e2b22-160">Tällaista eräkohtaisia varausta kutsutaan nimellä *eräsidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="e2b22-161">Seuraavat säännöt ovat voimassa, kun käsitellään määriä ja tietylle tilaukselle on määritetty eränumero:</span><span class="sxs-lookup"><span data-stu-id="e2b22-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="e2b22-162">Jotta tietyn eränumeron varaaminen nimikkeelle olisi mahdollista *Erä alla\[sijainti\]* -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="e2b22-163">Tähän väliin kuuluu yleensä myös rekisterikilpidimensio.</span><span class="sxs-lookup"><span data-stu-id="e2b22-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="e2b22-164">Sijaintidirektiivejä ei käytetä, kun keräilytyö luodaan myyntiriville, jossa käytetään tilaussidonnaista eränvarausta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="e2b22-165">Tilaussidonnaisiin eriin kohdistuvan työn varastokäsittelyn aikana käyttäjä tai järjestelmä ei voi muuttaa eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="e2b22-166">(Tämä käsittely sisältää poikkeuksen käsittelyn.)</span><span class="sxs-lookup"><span data-stu-id="e2b22-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="e2b22-167">Seuraavassa esimerkissä työnkulku näkyy kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="e2b22-168">Esimerkkiskenaario: Eränumeron kohdistus</span><span class="sxs-lookup"><span data-stu-id="e2b22-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="e2b22-169">Esittelytietojen on oltava asennettuna tätä esimerkkiä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="e2b22-170">Varastonvaraushierarkian määrittäminen sallimaan eräkohtainen varaus</span><span class="sxs-lookup"><span data-stu-id="e2b22-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="e2b22-171">Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="e2b22-172">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-172">Select **New**.</span></span>
3. <span data-ttu-id="e2b22-173">Anna nimi **Nimi**-kentässä (esim. **EräFlex**).</span><span class="sxs-lookup"><span data-stu-id="e2b22-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="e2b22-174">Anna kuvaus **Kuvaus**-kentässä (esim. **Erä joustavan alla**).</span><span class="sxs-lookup"><span data-stu-id="e2b22-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="e2b22-175">Valitse **Valittu**-kentässä **Sarjanumero** ja **Omistaja** ja siirrä ne sitten **Käytettävissä**-kenttään vasemman nuolipainikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="e2b22-176">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-176">Select **OK**.</span></span>
7. <span data-ttu-id="e2b22-177">Valitse **Eränumero** -dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="e2b22-178">Tasot **Rekisterikilpi** ja **Sijainti** valitaan automaattisesti eikä niiden valintaruutuja voi tyhjentää.</span><span class="sxs-lookup"><span data-stu-id="e2b22-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="e2b22-179">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="e2b22-180">Uuden julkaistun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="e2b22-180">Create a new released product</span></span>

1. <span data-ttu-id="e2b22-181">Määritä tuotteen kolme päätietoparametria käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="e2b22-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="e2b22-182">Valitse **Varastodimensioryhmä**-kentässä **Tavara**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="e2b22-183">Valitse **Seurantadimensioryhmä**-kentässä **Erä-fyy**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="e2b22-184">Valitse **Varaushierarkia** -kentässä **EräFlex**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="e2b22-185">Luo kaksi eränumeroa, kuten **B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="e2b22-186">Lisää nimekemääriä käytettävissä olevaan varastoon seuraavien arvojen avulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="e2b22-187">Varasto</span><span class="sxs-lookup"><span data-stu-id="e2b22-187">Warehouse</span></span> | <span data-ttu-id="e2b22-188">Eränumero</span><span class="sxs-lookup"><span data-stu-id="e2b22-188">Batch number</span></span> | <span data-ttu-id="e2b22-189">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="e2b22-189">Location</span></span> | <span data-ttu-id="e2b22-190">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="e2b22-190">License plate</span></span> | <span data-ttu-id="e2b22-191">Määrä</span><span class="sxs-lookup"><span data-stu-id="e2b22-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="e2b22-192">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-192">24</span></span>        | <span data-ttu-id="e2b22-193">B11</span><span class="sxs-lookup"><span data-stu-id="e2b22-193">B11</span></span>          | <span data-ttu-id="e2b22-194">BULKKI-001</span><span class="sxs-lookup"><span data-stu-id="e2b22-194">BULK-001</span></span> | <span data-ttu-id="e2b22-195">Ei ole</span><span class="sxs-lookup"><span data-stu-id="e2b22-195">None</span></span>          | <span data-ttu-id="e2b22-196">10</span><span class="sxs-lookup"><span data-stu-id="e2b22-196">10</span></span>       |
    | <span data-ttu-id="e2b22-197">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-197">24</span></span>        | <span data-ttu-id="e2b22-198">B11</span><span class="sxs-lookup"><span data-stu-id="e2b22-198">B11</span></span>          | <span data-ttu-id="e2b22-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="e2b22-199">FL-001</span></span>   | <span data-ttu-id="e2b22-200">LP11</span><span class="sxs-lookup"><span data-stu-id="e2b22-200">LP11</span></span>          | <span data-ttu-id="e2b22-201">10</span><span class="sxs-lookup"><span data-stu-id="e2b22-201">10</span></span>       |
    | <span data-ttu-id="e2b22-202">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-202">24</span></span>        | <span data-ttu-id="e2b22-203">B22</span><span class="sxs-lookup"><span data-stu-id="e2b22-203">B22</span></span>          | <span data-ttu-id="e2b22-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="e2b22-204">FL-002</span></span>   | <span data-ttu-id="e2b22-205">LP22</span><span class="sxs-lookup"><span data-stu-id="e2b22-205">LP22</span></span>          | <span data-ttu-id="e2b22-206">10</span><span class="sxs-lookup"><span data-stu-id="e2b22-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="e2b22-207">Syötä myyntitilaustiedot</span><span class="sxs-lookup"><span data-stu-id="e2b22-207">Enter sales order details</span></span>

1. <span data-ttu-id="e2b22-208">Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="e2b22-209">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-209">Select **New**.</span></span>
3. <span data-ttu-id="e2b22-210">Syötä myyntitilausotsikon **Asiakastili**-kenttään **US-003**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="e2b22-211">Lisää rivi uutta nimikettä varten ja syötä määräksi **10**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="e2b22-212">Varmista, että **Varasto**-kentän arvo on **24**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="e2b22-213">Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto** ja sitten **Ylläpidä**-ryhmässä **Erävaraus**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="e2b22-214">**Erävaraus**-sivulla näkyy luettelo eristä, jotka voidaan varata tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="e2b22-215">Tässä esimerkissä määränä on **20** eränumerolle **B11** ja **10** eränumerolle **B22**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="e2b22-216">Huomaa, että **Erävaraus**-sivua ei voi käyttää riviltä, jos rivin nimikkeelle on määritetty *Erä alla\[sijainti\]* -varaushierarkia, ellei sitä ole määritetty sallimaan eräkohtaista varausta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-217">Varataksesi ostotilaukselle tietyn erän sinun on käytettävä **Erävaraus** -sivua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="e2b22-218">Jos syötät eränumeron suoraan myyntitilausriville, järjestelmä toimii siten kuin olisit syöttänyt tietyn eräarvon nimikkeelle, johon sovelletaan *Erä alla\[sijainti\]* -varauskäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="e2b22-219">Kun tallennat rivin, näyttöön tulee varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="e2b22-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="e2b22-220">Jos vahvistat, että eränumero on määritettävä suoraan tilausrivillä, tavanomainen varastonhallintalogiikka ei käsittele kyseistä riviä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="e2b22-221">Jos varaat määrän **Varaus**-sivulta, tiettyä erää ei varata ja rivin osalta sovelletaan varastotoimintojen suorittamiseen niitä sääntöjä, joita sovelletaan *Erä alla\[sijainti\]* -varastokäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="e2b22-222">Yleensä tämä sivu toimii ja siihen sovelletaan samaa vuorovaikutusta kuin silloin, kun asianomaisille nimikkeille on määritetty *Erä yllä\[sijainti\]* -tyyppinen varaushierarkia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="e2b22-223">Seuraavat poikkeukset kuitenkin pätevät:</span><span class="sxs-lookup"><span data-stu-id="e2b22-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="e2b22-224">**Lähderiville sidotut eränumerot** -pikavälilehdessä näkyvät tilausriville varatut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="e2b22-225">Ruudukon eräarvot näkyvät koko tilausrivin toteutusjakson aikana, varaston käsittelyvaiheet mukaan luettuna.</span><span class="sxs-lookup"><span data-stu-id="e2b22-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="e2b22-226">**Yhteenveto**-pikavälilehdessä ruudukossa sen sijaan näkyy tavanomainen tilausrivin varaus (eli **Sijainti**-tason yläpuoleisille dimensioille tehtävä varaus) aina siihen asti, kun varastotyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="e2b22-227">Tämän jälkeen rivinvaraus siirtyy työyksikölle, eikä rivinvaraus enää ole näkyvissä sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="e2b22-228">**Lähderiviin sidotut eränumerot** -pikavälilehti auttaa sen varmistamisessa, että myyntitilausten käsittelijä näkee asiakkaan tilaukseen missä tahansa sen elinkaaren aikana aina laskutukseen asti sidotut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="e2b22-229">Tietyn erän varauksen lisäksi käyttäjä voi valita erän sijainnin ja rekisterikilven manuaalisesti sen sijaan, että se antaisi järjestelmän valita ne automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="e2b22-230">Tämä ominaisuus liittyy tilaussidonnaisen erävarausmekanismin rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="e2b22-231">Kuten aiemmin mainittiin, kun nimikkeelle varataan eränumero *Erä alla\[sijainti\]* -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="e2b22-232">Tämän vuoksi varastotyössä käytetään tilauksia käsitelleiden käyttäjien varaamia varastodimensioita, eivätkä ne aina välttämättä vastaa nimikkeen kätevää tai edes mahdollista varastointipaikkaa keräilytoimintoja varten.</span><span class="sxs-lookup"><span data-stu-id="e2b22-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="e2b22-233">Jos tilausten käsittelijät ovat tietoisia varaston rajoituksista, heidän saattaa kannattaa valita sijainnit ja rekisterikilvet manuaalisesti, kun he varaavat erää.</span><span class="sxs-lookup"><span data-stu-id="e2b22-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="e2b22-234">Tällöin käyttäjän on käytettävä **Näytä dimensiot** -toimintoa sivun otsikossa ja lisättävä sijainti ja rekisterikilpi **Yhteenveto**-pikavälilehden ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="e2b22-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="e2b22-235">Valitse **Erävaraus**-sivulla erän **B11** rivi ja sitten **Varaa rivi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="e2b22-236">Sijaintien ja rekisterikilpien määritykselle ei ole omaa logiikkaansa automaattisen varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e2b22-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="e2b22-237">Voit syöttää määrän manuaalisesti **Varaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e2b22-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="e2b22-238">Huomaa, että **Lähderiviin sidotut eränumerot**-pikavälilehdessä erän **B11** arvona on **Sidottu**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tietyn eränumeron sitominen myyntitilausriviin erävaraussivulla](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="e2b22-240">Myyntitilausrivin määrä voidaan varata eri eristä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="e2b22-241">Myös samaa erää voidaan varata useiden sijaintien ja rekisterikilpien perusteella (jos rekisterikilvet on sallittu sijainneille).</span><span class="sxs-lookup"><span data-stu-id="e2b22-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="e2b22-242">Tietyn erän varaaminen myyntitilausrivin määrälle voi olla myös osittaista.</span><span class="sxs-lookup"><span data-stu-id="e2b22-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="e2b22-243">Esimerkiksi 100 yksikön kokonaismäärä voidaan varata siten, että tietty erä on sidottu 20 yksikköön, kun taas 80 yksikköä varataan toimipaikka- ja varastotasolla mistä tahansa käytettävissä olevasta erästä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="e2b22-244">Tässä tapauksessa varastonhallintajärjestelmä käsittelee keräilytoiminnot käyttäen kahta erillistä työriviä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="e2b22-245">Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="e2b22-246">Valitse nimikkeesi ja sitten **Hallitse varastoa** \> **Näytä** \> **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tilaussidonnainen varaus varastotapahtumatyyppinä](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="e2b22-248">Tarkista nimikkeen varastotapahtumat, jotka liittyvät myyntitilausrivin varaukseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="e2b22-249">Tapahtuma, jossa **Viite**-kentän arvona on **Myyntitilaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta **Sijainti**-tason yläpuolella olevien dimension osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="e2b22-250">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat toimipaikka, varasto ja varastotila.</span><span class="sxs-lookup"><span data-stu-id="e2b22-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="e2b22-251">Tapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta määritetyn erän ja kaikkien sen yläpuolella olevien dimensioiden osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="e2b22-252">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat eränumero ja sijainti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="e2b22-253">Tässä esimerkissä sijainti on **Bulkki-001**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="e2b22-254">Valitse myyntitilauksen otsikossa **Varasto** \> **Toiminnot** \> **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="e2b22-255">Tilausrivi on nyt aallotettu, ja kuormitus ja työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="e2b22-256">Niiden varastotöiden tarkistus ja käsittely, joilla on tilaussidonnaisia eränumeroita</span><span class="sxs-lookup"><span data-stu-id="e2b22-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="e2b22-257">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** \> **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="e2b22-258">Työllä, joka käsittelee myyntitilausriviin sidottujen erämäärien keräilytoiminnon, on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="e2b22-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="e2b22-259">Järjestelmä käyttää työn luomisessa työmalleja, mutten sijaintidirektiivejä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="e2b22-260">Kaikkia työmalleille määritettyjä vakioasetuksia, kuten keräilyrivien tai tietyn mittayksikön enimmäismäärää, käytetään sen määrittämisessä, milloin uusi työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="e2b22-261">Keräilysijaintien tunnistamisen sijaintidirektiiveihin liittyviä sääntöjä ei kuitenkaan oteta huomioon, koska tilaussidonnaisessa varauksessa määritetään jo kaikki varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="e2b22-262">Nämä varastodimensiot sisältävät varastosäilytystason dimensiot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="e2b22-263">Siten työ perii kyseiset dimensiot ilman sijaintidirektiivien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="e2b22-264">Eränumeroa ei näytetä keräilyrivillä (kuten työrivillä, joka luodaan nimikkeelle, johon liittyy *Erä yllä\[sijainti\]*-varaushierarkia). Sen sijaan kohteesta-eränumero ja kaikki muut varastodimensiot näkyvät työrivin työvarastotapahtumassa, joka perustuu tähän liittyviin varastotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="e2b22-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Varaston varastotapahtuma töille, jotka perustuvat tilaussidonnaiseen varaukseen](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="e2b22-266">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus**, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="e2b22-267">Varastotapahtuma, jossa **Viite**-kentän arvona on **Työ**, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="e2b22-268">Varastotoiminnot voivat seuraavaksi suorittaa työt tavanomaiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="e2b22-269">Mobiililaitteen ohjeet kuitenkin ohjeistavat työntekijää keräilemään tiettyä eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="e2b22-270">Varastoympäristöissä, joissa sijainteja hallitaan rekisterikilvillä, työntekijä voi keräillä mistä tahansa vielä varaamattomasta rekisterikilvestä (jota ei siis ole varattu toiselle tilaussidonnaiselle varaukselle tai työlle, joka perustuu tällaiselle varaukselle), kun hän saapuu sijainnille, jossa säilytetään samaa erää useissa rekisterikilvissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="e2b22-271">Jos on epäkäytännöllistä keräillä työrivillä määritetystä sijainnista, varasto-operaattorit voivat käyttää jotakin seuraavista toiminnoista tietyn erän keräilyn siirtämiseen kätevämpään sijaintiin:</span><span class="sxs-lookup"><span data-stu-id="e2b22-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="e2b22-272">Vakiomuotoinen mobiililaitteen **Ohita toiminto** (jos varastotyöntekijän **Salli keräilysijainnin ohitus** -asetus on käytössä)</span><span class="sxs-lookup"><span data-stu-id="e2b22-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="e2b22-273">**Muuta sijaintia** -toiminto **Työluettelon tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="e2b22-274">Lopeta työn keräily ja hyllytys mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="e2b22-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="e2b22-275">Eränumeroa **B11** on nyt kerätty määrä **10** myyntitilausriviä varten ja siirretty sijaintiin **Lastauspaikan ovi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="e2b22-276">Tässä vaiheessa se on valmis lastattavaksi kuorma-autoon ja lähetettäväksi asiakkaan osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="e2b22-277">Joustava rekisterikilven varaus</span><span class="sxs-lookup"><span data-stu-id="e2b22-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="e2b22-278">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="e2b22-278">Business scenario</span></span>

<span data-ttu-id="e2b22-279">Tässä skenaariossa yritys käyttää varastonhallintaa ja töiden käsittelyä ja käsittelee kuormituksen suunnittelun yksittäisten kuormalavojen/konttien tasolla Supply Chain Management -sovelluksen ulkopuolella ennen työn luomista.</span><span class="sxs-lookup"><span data-stu-id="e2b22-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="e2b22-280">Rekisterikilvet edustavat näitä kontteja varastodimensioissa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="e2b22-281">Tämän vuoksi tietyt rekisterikilvet on määritettävä ennalta myyntitilausriveille ennen keräilytyön tekemistä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="e2b22-282">Yritys toivoo joustavuutta rekisterikilpien varaussääntöjen käsittelyssä, jotta seuraava toiminta olisi mahdollista:</span><span class="sxs-lookup"><span data-stu-id="e2b22-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="e2b22-283">Rekisterikilpi voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="e2b22-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="e2b22-284">Tämä auttaa takaamaan, että suunniteltu rekisterikilpi toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="e2b22-285">Jos rekisterikilpeä ei ole vielä määritetty myyntitilausriville, varaston henkilöstö voi valita rekisterikilven keräilyn aikana, kun myyntitilauksen rekisteröinti ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="e2b22-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="e2b22-286">Joustavan rekisterikilven varauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e2b22-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="e2b22-287">Ennen kuin voit käyttää joustavaa rekisterikilpien varausta, kaksi ominaisuutta on otettava käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="e2b22-288">Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="e2b22-289">Ominaisuudet on otettava käyttöön seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="e2b22-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="e2b22-290">**Ominaisuuden nimi:** *Joustava varastotason dimensioiden varauskäytäntö*</span><span class="sxs-lookup"><span data-stu-id="e2b22-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="e2b22-291">**Ominaisuuden nimi:** *Joustava tilaussidonnainen rekisterikilven varaus*</span><span class="sxs-lookup"><span data-stu-id="e2b22-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="e2b22-292">Tietyn rekisterikilven varaus myyntitilauksessa</span><span class="sxs-lookup"><span data-stu-id="e2b22-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="e2b22-293">Jos haluat ottaa käyttöön rekisterikilven varauksen tilauksessa, valitse **Salli varaus kysyntätilauksessa** -valintaruutu **Rekisterikilpi**-tasolla **Varaston varaushierarkiat** -sivulla hierarkialle, joka on liitetty tiettyyn nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Joustavan rekisterikilven varaushierarkian Varaston varaushierarkiat -sivu](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="e2b22-295">Voit ottaa rekisterikilven varauksen käyttöön tilauksessa missä tahansa käyttöönoton vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="e2b22-296">Tämä muutos ei vaikuta varauksiin tai avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="e2b22-297">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos avointen lähtevien varastotapahtumien varasto-ottotyyppi on *Tilauksessa*, *Varattu tilattu* tai *Varattu fyysinen* on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="e2b22-298">Vaikka **Salli varaus kysyntätilauksessa** -valintaruutu olisi valittu **Rekisterikilpi**-tasolla, tilauksen tietyn rekisterikilven varaaminen *ei* silti ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="e2b22-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="e2b22-299">Tässä tapauksessa käytetään varaushierarkian oletusvarastotoimintojen logiikkaa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="e2b22-300">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) -prosessia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="e2b22-301">Sovelluksessa voit tehdä varauksen suoraan myyntitilauksesta Käyttämällä **Avaa Excelissä** -komennon **Tilaussidonnaiset varaukset rekisterikilpeä kohti** -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="e2b22-302">Excel-lisäosassa avattaviin entiteettitietoihin on annettava seuraavat varaukseen liittyvät tiedot ja valittava sitten **Julkaise**, jotta tiedot lähetetään takaisin Supply Chain Management -sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="e2b22-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="e2b22-303">Viite (vain *Myyntitilaus*-arvoa tuetaan).</span><span class="sxs-lookup"><span data-stu-id="e2b22-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="e2b22-304">Tilausnumero (arvo voidaan johtaa erästä).</span><span class="sxs-lookup"><span data-stu-id="e2b22-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="e2b22-305">Erätunnus</span><span class="sxs-lookup"><span data-stu-id="e2b22-305">Lot ID</span></span>
- <span data-ttu-id="e2b22-306">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="e2b22-306">License plate</span></span>
- <span data-ttu-id="e2b22-307">Määrä</span><span class="sxs-lookup"><span data-stu-id="e2b22-307">Quantity</span></span>

<span data-ttu-id="e2b22-308">Jos sinun on varattava tietty eräseuratun nimikkeen rekisterikilpi, käytä **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="e2b22-309">Kun varaston toiminnot ovat käsitelleet tilaussidonnaista rekisterikilven varausta käyttävän myyntitilausrivin, sijaintidirektiivejä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="e2b22-310">Jos varaston työnimike sisältää rivejä, jotka vastaavat kokonaista lavaa ja joilla on rekisterikilpisidonnaisia määriä, voit optimoida keräysprosessin käyttämällä mobiililaitteen valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -vaihtoehdon arvoksi on määritetyt *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="e2b22-311">Varastotyöntekijä voi sitten skannata rekisterikilven ja viimeistellä keräilyn sen sijaan, että työn nimikkeet skannattaisiin yksitellen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Mobiililaitteen valikon vaihtoehto, jossa Käsittele rekisterikilven mukaan -asetuksen arvoksi on määritetty Kyllä](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="e2b22-313">Koska **Käsittele rekisterikilven mukaan** -toiminto ei tue työtä, joka koskee useita lavoja, eri rekisterikilville on paras olla erilliset työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="e2b22-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="e2b22-314">Jos haluat käyttää tätä menetelmää, lisää **Tilaussidonnaisen rekisterikilven tunnus** -kenttää työn otsikon katkaisuna **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-315">Tilaussidonnaisessa työn luontiprosessissa tilaussidonnaisen varastodimension arvo määritetään työrivien poimimiseen eikä rekisterikilven arvoa voi tarkastella suoraan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="e2b22-316">Vain *käyttäjäohjattua* prosessia tuetaan mobiililaitteen valikkovaihtoehtoa määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="e2b22-317">Esimerkkiskenaario: Tilaussidonnaisen rekisterikilven varauksen määrittäminen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="e2b22-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="e2b22-318">Tässä skenaariossa esitetään, miten tilaussidonnaisen rekisterikilven varaus määritetään ja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="e2b22-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e2b22-319">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e2b22-319">Make demo data available</span></span>

<span data-ttu-id="e2b22-320">Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Supply Chain Management -sovelluksen vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="e2b22-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="e2b22-321">Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, varmista, että käytät ympäristöä, johon on asennettu esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="e2b22-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="e2b22-322">Sinun on myös määritettävä yritykseksi **USMF**, ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="e2b22-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="e2b22-323">Luo varaston varaushierarkia, joka mahdollistaa rekisterikilven varauksen</span><span class="sxs-lookup"><span data-stu-id="e2b22-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="e2b22-324">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="e2b22-325">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-325">Select **New**.</span></span>
1. <span data-ttu-id="e2b22-326">Anna nimi **Nimi**-kenttään arvo (esimerkiksi *JoustavaRK*).</span><span class="sxs-lookup"><span data-stu-id="e2b22-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="e2b22-327">Anna kuvaus **Kuvaus**-kenttään arvo (esim. *Joustavan RK:n varaus*).</span><span class="sxs-lookup"><span data-stu-id="e2b22-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="e2b22-328">Valitse **Valittu**-luettelossa **Eränumero**, **Sarjanumero** ja **Omistaja**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="e2b22-329">Valitse **Poista**-painike ![taaksepäin osoittava nuoli](media/backward-button.png), jos haluat siirtää valitut tietueet **käytettävissä olevien** luetteloon.</span><span class="sxs-lookup"><span data-stu-id="e2b22-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="e2b22-330">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-330">Select **OK**.</span></span>
1. <span data-ttu-id="e2b22-331">Valitse **Rekisterikilpi**-dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="e2b22-332">**Sijainti**-taso valitaan automaattisesti, etkä voi tyhjentää sen valintaruutua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="e2b22-333">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="e2b22-334">Kahden vapautetun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="e2b22-334">Create two released products</span></span>

1. <span data-ttu-id="e2b22-335">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e2b22-336">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e2b22-337">Aseta **Uusi vapautettu tuote** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e2b22-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e2b22-338">**Tuotenumero:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="e2b22-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="e2b22-339">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="e2b22-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="e2b22-340">**Nimikemalliryhmä:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="e2b22-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="e2b22-341">**Nimikeryhmä:** *Ääni*</span><span class="sxs-lookup"><span data-stu-id="e2b22-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="e2b22-342">**Varastodimensioryhmä:** *Kauppatavara*</span><span class="sxs-lookup"><span data-stu-id="e2b22-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="e2b22-343">**Seurantadimensioryhmä:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="e2b22-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="e2b22-344">**Varaushierarkia:** *JoustavaRK*</span><span class="sxs-lookup"><span data-stu-id="e2b22-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="e2b22-345">Valitse **OK** luodaksesi tuotteen. Sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="e2b22-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="e2b22-346">Uusi tuote avataan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-346">The new product is opened.</span></span> <span data-ttu-id="e2b22-347">Määritä **Varasto**-pikavälilehden **Yksikön sarjaryhmän tunnus** -kenttään *kpl*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="e2b22-348">Toista edelliset vaiheet ja luo toinen tuote, jolla on samat asetukset. Määritä kuitenkin **Tuotenumero**- ja **Nimiketunnus**-kenttien arvoksi *Nimike2*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="e2b22-349">Valitse toimintoruudun **Varastonhallinta**-välilehden **Näytä**-ryhmässä **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="e2b22-350">Valitse sitten **Määrän oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="e2b22-351">Oikaise uusien nimikkeiden käytettävissä olevaa varastoa seuravan taulukon mukaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="e2b22-352">Kohde</span><span class="sxs-lookup"><span data-stu-id="e2b22-352">Item</span></span>  | <span data-ttu-id="e2b22-353">Varasto</span><span class="sxs-lookup"><span data-stu-id="e2b22-353">Warehouse</span></span> | <span data-ttu-id="e2b22-354">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="e2b22-354">Location</span></span> | <span data-ttu-id="e2b22-355">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="e2b22-355">License plate</span></span> | <span data-ttu-id="e2b22-356">Määrä</span><span class="sxs-lookup"><span data-stu-id="e2b22-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="e2b22-357">Nimike1</span><span class="sxs-lookup"><span data-stu-id="e2b22-357">Item1</span></span> | <span data-ttu-id="e2b22-358">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-358">24</span></span>        | <span data-ttu-id="e2b22-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="e2b22-359">FL-010</span></span>   | <span data-ttu-id="e2b22-360">RK01</span><span class="sxs-lookup"><span data-stu-id="e2b22-360">LP01</span></span>          | <span data-ttu-id="e2b22-361">10</span><span class="sxs-lookup"><span data-stu-id="e2b22-361">10</span></span>       |
    | <span data-ttu-id="e2b22-362">Nimike1</span><span class="sxs-lookup"><span data-stu-id="e2b22-362">Item1</span></span> | <span data-ttu-id="e2b22-363">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-363">24</span></span>        | <span data-ttu-id="e2b22-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="e2b22-364">FL-011</span></span>   | <span data-ttu-id="e2b22-365">RK02</span><span class="sxs-lookup"><span data-stu-id="e2b22-365">LP02</span></span>          | <span data-ttu-id="e2b22-366">10</span><span class="sxs-lookup"><span data-stu-id="e2b22-366">10</span></span>       |
    | <span data-ttu-id="e2b22-367">Nimike2</span><span class="sxs-lookup"><span data-stu-id="e2b22-367">Item2</span></span> | <span data-ttu-id="e2b22-368">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-368">24</span></span>        | <span data-ttu-id="e2b22-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="e2b22-369">FL-010</span></span>   | <span data-ttu-id="e2b22-370">RK01</span><span class="sxs-lookup"><span data-stu-id="e2b22-370">LP01</span></span>          | <span data-ttu-id="e2b22-371">5</span><span class="sxs-lookup"><span data-stu-id="e2b22-371">5</span></span>        |
    | <span data-ttu-id="e2b22-372">Nimike2</span><span class="sxs-lookup"><span data-stu-id="e2b22-372">Item2</span></span> | <span data-ttu-id="e2b22-373">24</span><span class="sxs-lookup"><span data-stu-id="e2b22-373">24</span></span>        | <span data-ttu-id="e2b22-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="e2b22-374">FL-011</span></span>   | <span data-ttu-id="e2b22-375">RK02</span><span class="sxs-lookup"><span data-stu-id="e2b22-375">LP02</span></span>          | <span data-ttu-id="e2b22-376">5</span><span class="sxs-lookup"><span data-stu-id="e2b22-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="e2b22-377">Sinun on luotava kaksi rekisterikilpeä ja käytettävä sijainteja, joissa sallitaan yhdistetyt nimikkeet, kuten *FL-010* ja *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="e2b22-378">Myyntitilauksen luominen ja tietyn rekisterikilven varaaminen</span><span class="sxs-lookup"><span data-stu-id="e2b22-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="e2b22-379">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e2b22-380">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-380">Select **New**.</span></span>
1. <span data-ttu-id="e2b22-381">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e2b22-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e2b22-382">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e2b22-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e2b22-383">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="e2b22-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="e2b22-384">Valitse **OK** ja sulje **Luo myyntitilaus** -valintaikkuna. Avaa sitten uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e2b22-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="e2b22-385">Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2b22-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="e2b22-386">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="e2b22-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="e2b22-387">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="e2b22-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="e2b22-388">Lisää toinen myyntitilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2b22-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="e2b22-389">**Nimiketunnus:** *Nimike2*</span><span class="sxs-lookup"><span data-stu-id="e2b22-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="e2b22-390">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="e2b22-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="e2b22-391">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-391">Select **Save**.</span></span>
1. <span data-ttu-id="e2b22-392">Anna **Rivin tiedot** -pikavälilehdessä **Asetukset**-välilehdessä **Erätunnus**-arvo jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="e2b22-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="e2b22-393">Nämä arvot ovat pakollisia tiettyjen rekisterikilpien varauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-394">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä **tilaussidonnaisia varauksia rekisterikilpeä kohti** -tietoyksikköä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="e2b22-395">Jos sinun on varattava tietyn rekisterikilven eräseurattu nimike, voit käyttää myös **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="e2b22-396">Jos annat rekisterikilven suoraan myyntitilausriville ja vahvistat sen järjestelmässä, rivillä ei käytetä varastonhallinnan käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="e2b22-397">Valitse **Avaa Microsoft Officessa**, valitse **Tilaussidonnaiset varaukset rekisterikilpeä kohti** ja lataa tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e2b22-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="e2b22-398">Avaa ladattu tiedosto Excelissä ja valitse **Ota muokkaus käyttöön** -painike, jotta voit ajaa Excel-lisäosan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="e2b22-399">Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="e2b22-400">Jos näet kirjautumisruudun, valitse **Kirjaudu sisään** samoilla tunnuksilla, joilla kirjaudut Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="e2b22-401">Jos haluat varata nimikkeen tietystä rekisterikilvestä, valitse Excelin lisäosassa **Uusi** ja lisää varausrivi. Määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e2b22-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="e2b22-402">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike1*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="e2b22-403">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="e2b22-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="e2b22-404">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="e2b22-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="e2b22-405">Lisää toinen varausrivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="e2b22-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="e2b22-406">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike2*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="e2b22-407">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="e2b22-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="e2b22-408">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="e2b22-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="e2b22-409">Valitse Excelin lisäosassa **Julkaise** ja lähetä tiedot takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-410">Varausrivi tulee näkyviin järjestelmään vain, jos julkaisemisessa ei ole tehty virheitä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="e2b22-411">Siirry takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="e2b22-412">Voit tarkistaa nimikkeen varauksen **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Ylläpidä \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="e2b22-413">Ota huomioon, että *Nimike1* -kohdan myyntitilausrivillä varataan varastoa *10* ja *Nimike2*-kohdan myyntitilausrivillä varataan varastoa *5*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="e2b22-414">Voit tarkastella varastotapahtumia, jotka liittyvät myyntitilausrivin varaukseen, **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Näytä \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="e2b22-415">Huomaa, että varaukseen liittyy kaksi tapahtumaa. Toisen **Viite**-kentän arvoksi on määritetty *Myyntitilaus* ja toisen **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="e2b22-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-416">Tapahtuma, jossa **Viite**-kentän arvoksi on määritetty *Myyntitilaus*, edustaa tilausrivin varausta varastodimensioissa, jotka ovat yli **Sijainti**-tason (toimipaikka, varasto ja varaston tila).</span><span class="sxs-lookup"><span data-stu-id="e2b22-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="e2b22-417">Tapahtuma, jonka **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*, vastaa tietyn rekisterikilven ja sijainnin tilausrivin varausta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="e2b22-418">Jos haluat vapauttaa myyntitilauksen, valitse toimintoruudun **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="e2b22-419">Varaston työn tarkistaminen ja käsitteleminen määritettyjen tilaussidonnaisten rekisterikilpien avulla</span><span class="sxs-lookup"><span data-stu-id="e2b22-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="e2b22-420">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="e2b22-421">Kun varaus on tehty tietylle erälle, järjestelmä ei käytä sijaintidirektiivejä, kun rekisterikilven varausta käyttävälle myyntitilaukselle luodaan työ.</span><span class="sxs-lookup"><span data-stu-id="e2b22-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="e2b22-422">Koska tilaussidonnainen varaus määrittää kaikki varastodimensiot, mukaan lukien sijainnin, sijaintidirektiivejä ei tarvitse käyttää, koska nämä varastodimensiot on juuri syötetty työhön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="e2b22-423">Ne näkyvät **Varastodimensioista**-osassa **Työn varastotapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-424">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on *Tilaussidonnainen varaus*, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="e2b22-425">Varastotapahtuma, jossa **Viite**-kentän arvona on *Työ*, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="e2b22-426">Tee työn keräily ja hyllytys valmiiksi mobiililaitteessa käyttämällä valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="e2b22-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2b22-427">**Käsittele rekisterikilven mukaan** -toiminto auttaa koko rekisterikilven käsittelemisessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="e2b22-428">Jos sinun on käsiteltävä rekisterikilven osa, et voi käyttää tätä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="e2b22-429">On suositeltavaa, että kustakin rekisterikilvestä luodaan erilliset työt.</span><span class="sxs-lookup"><span data-stu-id="e2b22-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="e2b22-430">Voit saavuttaa tämän tuloksen käyttämällä **Työn otsikoiden katkaisut** -ominaisuutta **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="e2b22-431">Rekisterikilpi *RK02* on nyt kerätty myyntitilausriveille ja hyllytetty *Lastausovi*-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="e2b22-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="e2b22-432">Tässä vaiheessa se on valmis lastattavaksi ja lähetettäväksi asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="e2b22-433">Niiden varastotöiden poikkeustenkäsittely, joilla on tilaussidonnaiset eränumerot</span><span class="sxs-lookup"><span data-stu-id="e2b22-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="e2b22-434">Tilaussidonnaisten eränumeroiden keräilyn varastotyöhön sovelletaan samoja varaston poikkeustenkäsittelyä ja -toimintoja kuin tavanomaiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="e2b22-435">Yleisesi ottaen avoin työ tai työrivi voidaan peruuttaa, se voidaan keskeyttää, koska käyttäjän sijainti on täynnä, siihen voidaan soveltaa lyhyttä keräilyä ja sitä voidaan päivittää siirron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="e2b22-436">Samoin jo valmiiksi saatua keräiltyä työmäärää voidaan vähentää tai työ voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="e2b22-437">Kaikkiin näihin poikkeusten käsittelyn toimintoihin sovelletaan seuraavaa keskeistä sääntöä: asiakkaalle varattua eränumeroa ei voi koskaan korvata toisella eränumerolla, mutta sen varastodimensioita (sijainti ja rekisterikilpi) voi muuttaa joko käyttäjän manuaalisella päivityksellä tai järjestelmän automaattisella päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="e2b22-438">Automaattinen päivitys perustuu samaan varastodimensioiden satunnaiseen määrittämiseen, jota käytetään, kun tietty erä varataan automaattisesti mutta varastodimensioita ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="e2b22-439">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="e2b22-439">Example scenario</span></span>

<span data-ttu-id="e2b22-440">Esimerkki tästä skenaariosta on tilanne, jossa aiemmin valmistuneiden töiden keräily perutaan **Vähennä keräiltyä määrää** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="e2b22-441">Tässä esimerkissä oletetaan, että olet jo tehnyt [Esimerkkiskenaario: Eränumeron kohdistus](#Example-batch-allocation) -kohdassa kerrotut vaiheet.</span><span class="sxs-lookup"><span data-stu-id="e2b22-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="e2b22-442">Se jatkuu kyseisestä esimerkistä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-442">It continues from that example.</span></span>

1. <span data-ttu-id="e2b22-443">Siirry kohtaan **Varastonhallinta** \> **Kuormat** \> **Aktiiviset kuormat**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="e2b22-444">Valitse kuorma, joka on luotu myyntitilauksen lähetyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="e2b22-445">Valitse **Kuormatilauksen rivit** -pikavälilehdestä **Vähennä keräiltyä määrää**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="e2b22-446">Valitse **Vähennä keräiltyä määrää** -sivun **Siirrä sijaintiin** -kentässä **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="e2b22-447">Valitse **Siirrä rekisterikilvelle**-kentässä **LP33**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="e2b22-448">Syötä **Peruttava keräilty varastomäärä** -kenttään arvo **10**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="e2b22-449">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-449">Select **OK**.</span></span>

<span data-ttu-id="e2b22-450">Tässä ovat keräilyn perumisen tulokset:</span><span class="sxs-lookup"><span data-stu-id="e2b22-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="e2b22-451">Aiemmin suljetun työn tilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="e2b22-452">Uusi **Varastonsiirto**-tyypin työ luodaan varastomäärälle **10** eränumerossa **B11**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="e2b22-453">Tämä työ edustaa siirtoa sijainnista **Lastauspaikan ovi** rekisterikilvelle **LP33** sijainnissa **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="e2b22-454">Tilaksi määritetään **Suljettu**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="e2b22-455">Järjestelmä varaa uudelleen alun perin tilatun eränumeron ja määrittää sijainnin ja rekisterikilpitunnukset.</span><span class="sxs-lookup"><span data-stu-id="e2b22-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="e2b22-456">(Tämä prosessi vastaa **Vara rivi** -toiminnon suorittamista tietyn eränumeron tilausriville).</span><span class="sxs-lookup"><span data-stu-id="e2b22-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="e2b22-457">Tämän tuloksena erä **B11** näkyy sidottuna **Lähderiville sidotut eränumerot** -pikavälilehdessä sivulla **Erävaraus** ja **Varaus**-kentässä on määrä **10** eränumeron **B11** osalta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="e2b22-458">Lisäksi **Sijainti**-kentän arvona on **FL-001** ja **Rekisterikilpi**-kentän arvona on **LP11**.</span><span class="sxs-lookup"><span data-stu-id="e2b22-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="e2b22-459">(Voit lisätä nämä kentät ruudukkoon, jos ne eivät ole näkyvissä.)</span><span class="sxs-lookup"><span data-stu-id="e2b22-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="e2b22-460">Seuraavissa taulukoissa on yhteenveto siitä, miten järjestelmä käsittelee tiettyjen varastotoimintojen tilaussidonnaisen erävarauksen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="e2b22-461">Taulukkojen sisältöä tulkitaan olettamalla, että kukin varastotoiminnon suorittamiseen liittyy olemassa oleva tilaussidonnaiseen erävaraukseen perustuvaa työ tai että kunkin varastotoiminnon suorittaminen vaikuttaa kyseisentyyppiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-462">Näissä taulukoissa Erämäärä on käytettävissä -sarake ilmaisee, onko varastomäärää käytettävissä sen määrän lisäksi, joka on jo varattu kulloisillekin tilaussidonnaisille varauksille tai joka on varattu kyseisentyyppisiin varauksiin perustuvassa varastotyössä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="e2b22-463">Avoimen työn keräilysijainnin ohitus</span><span class="sxs-lookup"><span data-stu-id="e2b22-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-464">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-465">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-466">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-466">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-467">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-467">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-468">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-469"><strong>Salli keräilysijainnin ohitus</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="e2b22-470">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-471">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastonhallintasovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="e2b22-472">Valitse <strong>Ehdota</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="e2b22-473">Vahvista uusi sijainti, jota ehdotetaan erämäärän käytettävyyden perusteella.</span><span class="sxs-lookup"><span data-stu-id="e2b22-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-474">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="e2b22-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="e2b22-475">Keräilyrivin sijainniksi päivittyy uusi sijainti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="e2b22-476">(Jos sijainti on rekisterikilpihallittu, työvarastotapahtumalle määritetään satunnainen rekisterikilpi ja työntekijä voi keräillä mistä tahansa rekisterikilvestä, jossa määrää on käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="e2b22-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="e2b22-477">Jos määrää on uuden sijainnin useassa rekisterikilvessä, alkuperäinen keräilyrivi jaetaan useaan riviin, jotka vastaavat kutakin rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-478">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-479">Nro</span><span class="sxs-lookup"><span data-stu-id="e2b22-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-480">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastonhallintasovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="e2b22-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="e2b22-481">Määritä sijainti manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-482"><strong>Ohita sijainti</strong> -toiminto ei ole mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="e2b22-483">Se epäonnistuu, ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="e2b22-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="e2b22-484">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="e2b22-485">Täysi-painike – Työrivin jakaminen käyttäjän sijainnin ylivuodon vuoksi</span><span class="sxs-lookup"><span data-stu-id="e2b22-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-486">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-487">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-488">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-488">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-489">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-489">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-490">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e2b22-491"><strong>Salli työn jakaminen</strong> -asetus on käytössä mobiililaitteen valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="e2b22-492">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-493">Valitse valikkovaihtoehto <strong>Täysi</strong> varastonhallintasovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="e2b22-494">Syötä <strong>Keräilymäärä</strong>-kenttään tarvittavan keräilyn osamäärä ilmaisemaan täyttä kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-495">Kulloisessakin työssä määrä päivitetään vastaamaan jäljellä olevaa keräiltävää määrää.</span><span class="sxs-lookup"><span data-stu-id="e2b22-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="e2b22-496">Keräillylle määrälle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="e2b22-497">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="e2b22-498">Valmiin työn keräillyn määrän vähentäminen (kuormasta)</span><span class="sxs-lookup"><span data-stu-id="e2b22-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-499">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-500">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-501">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-501">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-502">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-502">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-503">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-504">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-504">Not applicable</span></span></td>
<td><span data-ttu-id="e2b22-505">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-506">Avaa <strong>Vähennä keräiltyä määrää</strong> -sivu kuormariviltä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="e2b22-507">Syötä sen määrän kokonaisarvo, jonka keräily perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="e2b22-508">Valitse "siirto kohteeseen" sijainti/rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="e2b22-509">Kuormariviin liittyvä työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="e2b22-510">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-511">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-512">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-513">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-513">No</span></span></td>
<td><span data-ttu-id="e2b22-514">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-514">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-515">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-515">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-516">Määrä varataan uudelleen samalle erälle ja samalle sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu), jotka on syötetty keräilyn perumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="e2b22-517">Nimikkeen siirtäminen varastossa</span><span class="sxs-lookup"><span data-stu-id="e2b22-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-518">Tätä varastotoimintoa voidaan soveltaa vain **Työnluontiprosessi**-tyypin siirtoihin, ei mallin mukaiseen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="e2b22-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-519">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-520">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-521">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-521">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-522">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-522">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-523">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-524"><strong>Salli työhön liitetyn varaston siirto</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="e2b22-525">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-526">Aloita siirto varastonhallinnan mobiilisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="e2b22-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="e2b22-527">Anna kohteesta- ja kohteeseen-sijainnit.</span><span class="sxs-lookup"><span data-stu-id="e2b22-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="e2b22-528">Kaikissa olemassa olevissa töissä, joihin siirto vaikuttaa, keräilysijainniksi päivitetään uusi kohteeseen-sijainti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="e2b22-529">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-530">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-531">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-532">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-532">No</span></span></td>
<td><span data-ttu-id="e2b22-533">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-533">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-534">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-534">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-535">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle ja uudelle kohteeseen-sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="e2b22-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="e2b22-536">Valmiin työn keräillyn määrän palauttaminen (kuormasta tai aallosta)</span><span class="sxs-lookup"><span data-stu-id="e2b22-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-537">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-538">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-539">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-539">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-540">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-540">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-541">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="e2b22-542">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-542">Not applicable</span></span></td>
<td><span data-ttu-id="e2b22-543">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-544">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="e2b22-545">Valitse pyyntösivulla vaihtoehto <strong>Jätä nimikkeet nykyiseen sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-546">Kaikki tähän Kuormariviin liittyvät työt perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="e2b22-547">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-548">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-549">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-549">No</span></span></td>
<td><span data-ttu-id="e2b22-550">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-550">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-551">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-551">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-552">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä jätettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-553">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-554">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="e2b22-555">Valitse pyyntösivulla vaihtoehto <strong>Osoita nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-556">Nykyinen työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="e2b22-557">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-558">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-559">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-560">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-560">No</span></span></td>
<td><span data-ttu-id="e2b22-561">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-561">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-562">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-562">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-563">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä osoitettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-564">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-565">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="e2b22-566">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-567">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="e2b22-568">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-569">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-570">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="e2b22-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="e2b22-571">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet sijaintidirektiivien perusteella</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-572">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="e2b22-573">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="e2b22-574">Määrän lyhytkeräily – Rekisteröi määrä fyysisesti löytymättömäksi sijainnista/rekisterikilvestä, kun keräilytyötä suoritetaan</span><span class="sxs-lookup"><span data-stu-id="e2b22-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-575">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-576">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-577">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-577">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-578">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-578">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-579">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-580">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="e2b22-581">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-582">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-583">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-584">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-585">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="e2b22-586"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-587">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-588">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-589">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-589">No</span></span></td>
<td><span data-ttu-id="e2b22-590">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e2b22-591">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="e2b22-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="e2b22-592">Olemassa oleva työ pysyy avoimena.</span><span class="sxs-lookup"><span data-stu-id="e2b22-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-593">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-594">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="e2b22-595">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-596">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-597">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-598">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-599">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="e2b22-600"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-601">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-602">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-603">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-603">No</span></span></td>
<td><span data-ttu-id="e2b22-604">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-604">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-605">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-605">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-606">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-607">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei/Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="e2b22-608">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="e2b22-609">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-610">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-611">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-612">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="e2b22-613">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-614">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="e2b22-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="e2b22-615">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="e2b22-616">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="e2b22-617">Uusi keräilyrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-617">A new pick line is created.</span></span> <span data-ttu-id="e2b22-618">Siinä käytetään käyttäjän valitsemaa sijaintia/rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="e2b22-619">Uusi hyllytysrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="e2b22-620"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-621">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-622">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="e2b22-623">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="e2b22-624">Nro</span><span class="sxs-lookup"><span data-stu-id="e2b22-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-625">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-626">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-627">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-628">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="e2b22-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="e2b22-629">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-630">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="e2b22-631">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="e2b22-632">Nro</span><span class="sxs-lookup"><span data-stu-id="e2b22-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-633">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-634">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-635">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="e2b22-636">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="e2b22-637">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="e2b22-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="e2b22-638">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="e2b22-639">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="e2b22-640"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="e2b22-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e2b22-641">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin/rekisterikilven määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-642">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Automaattinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä/Ei</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä/Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="e2b22-643">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-644">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastonhallintasovelluksessa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="e2b22-645">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="e2b22-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="e2b22-646">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja automaattinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-647">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="e2b22-648">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="e2b22-649">Muuta varaston tilaa</span><span class="sxs-lookup"><span data-stu-id="e2b22-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="e2b22-650">Tämä varastotoiminto voidaan suorittaa useista aloituskohdista.</span><span class="sxs-lookup"><span data-stu-id="e2b22-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="e2b22-651">Tässä näkyvässä esimerkissä käytetään **Varaston tilanmuutos** -toimintoa **Käytettävissä sijainnin mukaan** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e2b22-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e2b22-652">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="e2b22-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="e2b22-653">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2b22-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="e2b22-654">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="e2b22-654">Key user steps</span></span></th>
<th><span data-ttu-id="e2b22-655">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="e2b22-655">Warehouse work</span></span></th>
<th><span data-ttu-id="e2b22-656">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="e2b22-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-657"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Varaukset</strong> tai <strong>Merkinnät ja varaukset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="e2b22-658">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-659">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="e2b22-660">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="e2b22-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="e2b22-661">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="e2b22-662">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-663">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e2b22-664">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-665">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="e2b22-666">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="e2b22-667"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-668">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-668">No</span></span></td>
<td><span data-ttu-id="e2b22-669">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-669">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-670">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e2b22-671">Varaus poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e2b22-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="e2b22-672">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="e2b22-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="e2b22-673"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="e2b22-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="e2b22-674"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Ei mitään</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="e2b22-675">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e2b22-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e2b22-676">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="e2b22-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="e2b22-677">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="e2b22-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="e2b22-678">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="e2b22-679">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2b22-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="e2b22-680">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="e2b22-681">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="e2b22-682">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e2b22-683">Ei</span><span class="sxs-lookup"><span data-stu-id="e2b22-683">No</span></span></td>
<td><span data-ttu-id="e2b22-684">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="e2b22-684">See the previous row.</span></span></td>
<td><span data-ttu-id="e2b22-685">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="e2b22-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="e2b22-686">Varastotilan muutokset eivät ole sallittuja.</span><span class="sxs-lookup"><span data-stu-id="e2b22-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="e2b22-687">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="e2b22-687">Limitations</span></span>

- <span data-ttu-id="e2b22-688">Joustava varastotason dimensionvaraustoiminto ei tue seuraavia ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="e2b22-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="e2b22-689">Todellisen painon hallinta</span><span class="sxs-lookup"><span data-stu-id="e2b22-689">Catch weight management</span></span>
    - <span data-ttu-id="e2b22-690">Fyysinen negatiivinen varasto</span><span class="sxs-lookup"><span data-stu-id="e2b22-690">Physical negative inventory</span></span>
    - <span data-ttu-id="e2b22-691">Varaus tilatun tarjonnan perusteella</span><span class="sxs-lookup"><span data-stu-id="e2b22-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="e2b22-692">Siirtotilaukset ja raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="e2b22-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="e2b22-693">Kontin direktiiviyksiköittäin pakkaamisen konsolidointisäännöllä on rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="e2b22-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="e2b22-694">Tilaussidonnaisten varausten osalta suosittelemme välttämää sellaisten kontinrakennusmallien käyttöä, joissa **Pakkaa direktiiviyksiköittäin** -kenttä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="e2b22-695">Nykyisessä ratkaisussa sijaintidirektiivejä ei käytetä varastotyön luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e2b22-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="e2b22-696">Siksi vain yksikön sarjaryhmän alinta yksikköä (varastoyksikköä) käytetään konttiinpakkauksen aaltovaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="e2b22-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2b22-697">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e2b22-697">See also</span></span>

- [<span data-ttu-id="e2b22-698">Eränumerot varastonhallinnassa</span><span class="sxs-lookup"><span data-stu-id="e2b22-698">Batch numbers in Warehouse management</span></span>](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="e2b22-699">Saman erän varaaminen myyntitilausta varten</span><span class="sxs-lookup"><span data-stu-id="e2b22-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="e2b22-700">Mobiililaitteen vanhimman erän kerääminen</span><span class="sxs-lookup"><span data-stu-id="e2b22-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="e2b22-701">Erän ja rekisterikilven tiedot</span><span class="sxs-lookup"><span data-stu-id="e2b22-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="e2b22-702">Varastonhallinnan varausten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e2b22-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]