---
title: Joustava varastotason dimensionvarauskäytäntö
description: Tässä ohjeaiheessa kuvataan varaston varauskäytäntö, joka mahdollistaa eräseurattuja tuotteita myyville ja niiden logistiikan varastonhallintajärjestelmän toiminnoilla toteuttaville yrityksille tiettyjen erien varaamisen asiakkaiden myyntitilauksille, vaikka tuotteiden varaushierarkia ei salli tiettyjen erien varausta.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: d75e6a8b48447a33156e03d50e990b8514bacda9
ms.sourcegitcommit: d540998ad6f9c894ca99498c045ae4b86b779806
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970700"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="25907-103">Joustava varastotason dimensionvarauskäytäntö</span><span class="sxs-lookup"><span data-stu-id="25907-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25907-104">Kun Erä alla\[sijainti\]-tyyppinen varastonvaraushierarkia yhdistetään tuotteisiin, eräseurattuja tuotteita myyvät ja niiden logistiikan Microsoft Dynamics 365 -varastonhallintajärjestelmävalmiilla (WMS) toiminnoilla toteuttavat yritykset eivät voi varata tiettyjä kyseisten tuotteiden eriä asiakkaiden myyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="25907-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="25907-105">Samalla tavalla tiettyjä rekisterikilpiä ei voi varata myyntitilausten tuotteille, kun nämä tuotteet on liitetty oletusvaraushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="25907-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="25907-106">Tässä ohjeaiheessa kuvataan varastonvarauskäytäntö, jonka avulla nämä yritykset varaavat tiettyjä eriä tai rekisterikilpiä, vaikka tuotteet on yhdistetty Erä alla\[sijainti\]-varaushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="25907-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="25907-107">Varastovaraushierarkia</span><span class="sxs-lookup"><span data-stu-id="25907-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="25907-108">Tässä osassa on yhteenveto olemassa olevasta varastonvaraushierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="25907-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="25907-109">Varastonvaraushierarkia määrää, että varastodimensioiden osalta kysyntätilaus sisältää pakolliset dimensiot toimipaikka, varasto ja varastotila. Varastologiikka taas vastaa sijainnin osoittamisesta pyydetyille määrille ja kyseisen sijainnin varaamisesta.</span><span class="sxs-lookup"><span data-stu-id="25907-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="25907-110">Toisin sanoen kysyntätilauksen ja varastotoimintojen välisissä vuorovaikutuksissa kysyntätilauksen oletetaan ilmaisevan, mistä tilaus on lähetettävä (eli mistä toimipaikasta ja varastosta).</span><span class="sxs-lookup"><span data-stu-id="25907-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="25907-111">Tämän jälkeen varasto tukeutuu logiikkaan löytääkseen vaaditun määrän varastotilasta.</span><span class="sxs-lookup"><span data-stu-id="25907-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="25907-112">Yrityksen toimintamallin heijastamista varten seurantadimensiot (erä- ja sarjanumerot) ovat joustavampia.</span><span class="sxs-lookup"><span data-stu-id="25907-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="25907-113">Varastonvaraushierarkia voi mukautua seuraavankaltaisiin tilanteisiin:</span><span class="sxs-lookup"><span data-stu-id="25907-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="25907-114">Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot, sen jälkeen, kun määrät on löydetty varaston säilytystilasta.</span><span class="sxs-lookup"><span data-stu-id="25907-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="25907-115">Tätä mallia kutsutaan usein nimellä *Erä alla\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="25907-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="25907-116">Sitä käytetään yleensä silloin, kun tuotteen erä- tai sarjanumeron tunnistus ei ole tärkeä asiakkaille, jotka tekevät pyynnön myyjäyritykselle.</span><span class="sxs-lookup"><span data-stu-id="25907-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="25907-117">Jos erä- tai sarjanumerot ovat osa asiakkaan tilausmääritystä ja ne tallennetaan kysyntätilaukseen, varastotoiminnot, jotka etsivät määrät varastosta, rajoitetaan tiettyihin pyydettyihin numeroihin, joita ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="25907-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="25907-118">Tätä mallia kutsutaan nimellä *Erä yllä\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="25907-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="25907-119">Näissä skenaarioissa haasteena on, että kullekin vapautetulle tuotteelle voidaan määrittää vain yksi varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="25907-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="25907-120">Siksi, jotta varastonhallintajärjestelmä määrittäisi hierarkian määrittämisen jälkeen, milloin erä- tai sarjanumero pitäisi varata (joko kun kysyntätilaus saadaan tai varaston keräilytyön aikana), kyseistä ajoitusta ei voi muuttaa tilannekohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="25907-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="25907-121">Eräseurattujen nimikkeiden joustava varaus</span><span class="sxs-lookup"><span data-stu-id="25907-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="25907-122">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="25907-122">Business scenario</span></span>

<span data-ttu-id="25907-123">Tässä skenaariossa yritys käyttää varastostrategiaa, jossa valmiita tavaroita seurataan eränumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="25907-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="25907-124">Yritys käyttää myös varastonhallinnan työkuormitusta.</span><span class="sxs-lookup"><span data-stu-id="25907-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="25907-125">Koska tässä työkuormituksessa on hyvin toimiva logiikka varaston keräily- ja lähetystoimintojen suunnittelulle ja suorittamiselle erämääräisiä nimikkeitä varten, useimmille valmiille nimikkeille määritetään Erä alla\[sijainti\] -varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="25907-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="25907-126">Tällaisen operatiivisen määrityksen etuna on, että päätöksiä (jotka ovat käytännössä varauspäätöksiä) siitä, mitkä erät kerätään ja mihin ne laitetaan varastossa, lykätään siihen asti, että varastoin keräilytoiminnot alkavat.</span><span class="sxs-lookup"><span data-stu-id="25907-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="25907-127">Niitä ei tehdä, kun asiakkaan tilaus saadaan.</span><span class="sxs-lookup"><span data-stu-id="25907-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="25907-128">Vaikka Erä alla\[sijainti\] -varaushierarkia palvelee yrityksen liiketoimintatavoitteita hyvin, monet yrityksen vakiintuneista asiakkaista tarvitsevat aikaisemmin ostamansa erää, kun ne tilaavat tuotteita uudelleen.</span><span class="sxs-lookup"><span data-stu-id="25907-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="25907-129">Siksi yritys etsii joustavuutta erävaraussääntöjen käsittelyyn, jotta asiakkaan samaa nimikettä koskevasta kysynnästä riippuen, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="25907-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="25907-130">Eränumero voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi muuttaa varastotoimintojen aikana ja/tai osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="25907-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="25907-131">Tämä auttaa takaamaan, että tilattu eränumero toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="25907-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="25907-132">Jos eränumerolla ei ole merkitystä asiakkaalle, varastotoiminnot voivat määrittää eränumeron keräilyn aikana, kun myyntitilauksen kirjaus ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="25907-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="25907-133">Tietyn erän myyntilaukselle varaamisen mahdollistaminen</span><span class="sxs-lookup"><span data-stu-id="25907-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="25907-134">Jotta haluttu erävarauksen joustavuus mahdollistetaan nimikkeille, joilla on Erä alla\[sijainti\] -varastonvaraushierarkia, varastopäällikköjen on valittava **Salli varaus kysyntätilauksessa** -valintaruutu **Eränumero** -tasolla sivulla **Varastonvaraushierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="25907-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varastovarausten hierarkian joustavoittaminen](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="25907-136">Kun hierarkian **Eränumero**-taso on valittuna, kaikki kyseisen tason yläpuolella olevat dimensiot aina **Sijainti**-tasolle valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="25907-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="25907-137">(Oletusarvoisesti kaikki **Sijainti**-tason yläpuolella olevat dimensiot on esivalittu.) Tämä toiminta perustuu logiikkaan, jossa myös kaikki eränumeron ja sijainnin välisen alueen dimensiot varataan automaattisesti, kun varaat tietyn eränumeron tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="25907-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="25907-138">**Salli varaus kysyntätilauksessa** -valintaruutu pätee vain varaushierarkiatasoille, jotka ovat varastosijainnin dimension alapuolella.</span><span class="sxs-lookup"><span data-stu-id="25907-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="25907-139">**Eränumero** ja **rekisterikilpi** ovat hierarkian ainoat tasot, joihin joustavaa varauskäytäntöä voi soveltaa.</span><span class="sxs-lookup"><span data-stu-id="25907-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="25907-140">Toisin sanoen et voi valita **Salli varaus kysyntätilauksessa** -valintaruutua **Sijainti**- tai **Sarjanumero**-tasolle.</span><span class="sxs-lookup"><span data-stu-id="25907-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="25907-141">Jos varaushierarkia sisältää sarjanumerodimension (jonka on aina oltava **Eränumero**-tason alapuolella) ja jos olet ottanut eräkohtaisen varauksen käyttöön eränumerolle, järjestelmä jatkaa sarjanumeroiden varaus- ja keräilytoimintojen käsittelyä niiden sääntöjen perusteella, jotka pätevät Sarja alla\[sijainti\] -varauskäytäntöön.</span><span class="sxs-lookup"><span data-stu-id="25907-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="25907-142">Voit missä tahansa vaiheessa ottaa eräkohtaisenvarauksen käyttöön olemassa olevalle Erä alla\[sijainti\] -varaushierarkialle ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="25907-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="25907-143">Tämä muutos ei vaikuta varauksiin ja avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="25907-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="25907-144">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos varasto-ottotyypin **Varattu tilattu**, **Varattu fyysinen** tai **Tilattu** varastotapahtumia on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="25907-145">Jos nimikkeen käytössä oleva varaushierarkia ei salli erän määritystä tilauksessa, voit siirtää sen varaushierarkiaan, joka sallii erän määrityksen, kunhan hierarkiatasorakenne on sama molemmissa hierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="25907-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="25907-146">Tee siirto toiminnolla **Muuta nimikkeiden varaushierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="25907-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="25907-147">Tästä muutoksesta voi olla hyötyä, kun haluat estää eräseurattujen nimikkeiden alijoukon joustavan erävarauksen, mutta sallia sen muun tuoteportfolion osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="25907-148">Riippumatta siitä, oletko valinnut **Salli varaus kysyntätilauksessa** -valintaruudun, jos et halua varata nimikkeelle tiettyä eränumeroa tilausrivillä, oletusarvoinen varastotoimintologiikka, jota sovelletaan Erä alla\[sijainti\] -varaushierarkiaan, pätee edelleen.</span><span class="sxs-lookup"><span data-stu-id="25907-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="25907-149">Tietyn eränumeron varaaminen asiakastilausta varten</span><span class="sxs-lookup"><span data-stu-id="25907-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="25907-150">Kun eräseuratun nimikkeen Erä alla\[sijainti\] -varastonvaraushierarkia on määritetty sallimaan tiettyjen eränumeroiden varaaminen myyntitilauksissa, myyntitilausten käsittelijät voivat ottaa saman nimikkeen asiakastilauksia vastaan jollakin seuraavista tavoista asiakkaan pyynnöstä riippuen:</span><span class="sxs-lookup"><span data-stu-id="25907-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="25907-151">**Anna tilaustiedot ilman eränumeron määritystä** – Tätä menetelmää kannattaa käyttää, kun tuotteen erämääritys ei ole tärkeä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="25907-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="25907-152">Kaikki aiemmin luodut prosessit, jotka liittyvät tällaisen tilauksen käsittelyyn, eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="25907-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="25907-153">Käyttäjiltä ei vaadita lisätoimia.</span><span class="sxs-lookup"><span data-stu-id="25907-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="25907-154">**Anna tilaustiedot ja varaa tietty eränumero** – Tätä menetelmää kannattaa käyttää, kun asiakas pyytää tiettyä erää.</span><span class="sxs-lookup"><span data-stu-id="25907-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="25907-155">Yleensä asiakkaat pyytävät tiettyä erää, kun he tilaavat uudelleen aiemmin ostamaansa tuotetta.</span><span class="sxs-lookup"><span data-stu-id="25907-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="25907-156">Tällaista eräkohtaisia varausta kutsutaan nimellä *eräsidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="25907-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="25907-157">Seuraavat säännöt ovat voimassa, kun käsitellään määriä ja tietylle tilaukselle on määritetty eränumero:</span><span class="sxs-lookup"><span data-stu-id="25907-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="25907-158">Jotta tietyn eränumeron varaaminen nimikkeelle olisi mahdollista Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="25907-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="25907-159">Tähän väliin kuuluu yleensä myös rekisterikilpidimensio.</span><span class="sxs-lookup"><span data-stu-id="25907-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="25907-160">Sijaintidirektiivejä ei käytetä, kun keräilytyö luodaan myyntiriville, jossa käytetään tilaussidonnaista eränvarausta.</span><span class="sxs-lookup"><span data-stu-id="25907-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="25907-161">Tilaussidonnaisiin eriin kohdistuvan työn varastokäsittelyn aikana käyttäjä tai järjestelmä ei voi muuttaa eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="25907-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="25907-162">(Tämä käsittely sisältää poikkeuksen käsittelyn.)</span><span class="sxs-lookup"><span data-stu-id="25907-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="25907-163">Seuraavassa esimerkissä työnkulku näkyy kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="25907-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="25907-164">Esimerkkiskenaario: Eränumeron kohdistus</span><span class="sxs-lookup"><span data-stu-id="25907-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="25907-165">Esittelytietojen on oltava asennettuna tätä esimerkkiä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="25907-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="25907-166">Varastonvaraushierarkian määrittäminen sallimaan eräkohtainen varaus</span><span class="sxs-lookup"><span data-stu-id="25907-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="25907-167">Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="25907-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="25907-168">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="25907-168">Select **New**.</span></span>
3. <span data-ttu-id="25907-169">Anna nimi **Nimi**-kentässä (esim. **EräFlex**).</span><span class="sxs-lookup"><span data-stu-id="25907-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="25907-170">Anna kuvaus **Kuvaus**-kentässä (esim. **Erä joustavan alla**).</span><span class="sxs-lookup"><span data-stu-id="25907-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="25907-171">Valitse **Valittu**-kentässä **Sarjanumero** ja **Omistaja** ja siirrä ne sitten **Käytettävissä**-kenttään vasemman nuolipainikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="25907-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="25907-172">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="25907-172">Select **OK**.</span></span>
7. <span data-ttu-id="25907-173">Valitse **Eränumero** -dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="25907-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="25907-174">Tasot **Rekisterikilpi** ja **Sijainti** valitaan automaattisesti eikä niiden valintaruutuja voi tyhjentää.</span><span class="sxs-lookup"><span data-stu-id="25907-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="25907-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="25907-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="25907-176">Uuden julkaistun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="25907-176">Create a new released product</span></span>

1. <span data-ttu-id="25907-177">Määritä tuotteen kolme päätietoparametria käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="25907-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="25907-178">Valitse **Varastodimensioryhmä**-kentässä **Tavara**.</span><span class="sxs-lookup"><span data-stu-id="25907-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="25907-179">Valitse **Seurantadimensioryhmä**-kentässä **Erä-fyy**.</span><span class="sxs-lookup"><span data-stu-id="25907-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="25907-180">Valitse **Varaushierarkia** -kentässä **EräFlex**.</span><span class="sxs-lookup"><span data-stu-id="25907-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="25907-181">Luo kaksi eränumeroa, kuten**B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="25907-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="25907-182">Lisää nimekemääriä käytettävissä olevaan varastoon seuraavien arvojen avulla.</span><span class="sxs-lookup"><span data-stu-id="25907-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="25907-183">Varasto</span><span class="sxs-lookup"><span data-stu-id="25907-183">Warehouse</span></span> | <span data-ttu-id="25907-184">Eränumero</span><span class="sxs-lookup"><span data-stu-id="25907-184">Batch number</span></span> | <span data-ttu-id="25907-185">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="25907-185">Location</span></span> | <span data-ttu-id="25907-186">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="25907-186">License plate</span></span> | <span data-ttu-id="25907-187">Määrä</span><span class="sxs-lookup"><span data-stu-id="25907-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="25907-188">24</span><span class="sxs-lookup"><span data-stu-id="25907-188">24</span></span>        | <span data-ttu-id="25907-189">B11</span><span class="sxs-lookup"><span data-stu-id="25907-189">B11</span></span>          | <span data-ttu-id="25907-190">BULKKI-001</span><span class="sxs-lookup"><span data-stu-id="25907-190">BULK-001</span></span> | <span data-ttu-id="25907-191">Ei ole</span><span class="sxs-lookup"><span data-stu-id="25907-191">None</span></span>          | <span data-ttu-id="25907-192">10</span><span class="sxs-lookup"><span data-stu-id="25907-192">10</span></span>       |
    | <span data-ttu-id="25907-193">24</span><span class="sxs-lookup"><span data-stu-id="25907-193">24</span></span>        | <span data-ttu-id="25907-194">B11</span><span class="sxs-lookup"><span data-stu-id="25907-194">B11</span></span>          | <span data-ttu-id="25907-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="25907-195">FL-001</span></span>   | <span data-ttu-id="25907-196">LP11</span><span class="sxs-lookup"><span data-stu-id="25907-196">LP11</span></span>          | <span data-ttu-id="25907-197">10</span><span class="sxs-lookup"><span data-stu-id="25907-197">10</span></span>       |
    | <span data-ttu-id="25907-198">24</span><span class="sxs-lookup"><span data-stu-id="25907-198">24</span></span>        | <span data-ttu-id="25907-199">B22</span><span class="sxs-lookup"><span data-stu-id="25907-199">B22</span></span>          | <span data-ttu-id="25907-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="25907-200">FL-002</span></span>   | <span data-ttu-id="25907-201">LP22</span><span class="sxs-lookup"><span data-stu-id="25907-201">LP22</span></span>          | <span data-ttu-id="25907-202">10</span><span class="sxs-lookup"><span data-stu-id="25907-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="25907-203">Syötä myyntitilaustiedot</span><span class="sxs-lookup"><span data-stu-id="25907-203">Enter sales order details</span></span>

1. <span data-ttu-id="25907-204">Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25907-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="25907-205">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="25907-205">Select **New**.</span></span>
3. <span data-ttu-id="25907-206">Syötä myyntitilausotsikon **Asiakastili**-kenttään **US-003**.</span><span class="sxs-lookup"><span data-stu-id="25907-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="25907-207">Lisää rivi uutta nimikettä varten ja syötä määräksi **10**.</span><span class="sxs-lookup"><span data-stu-id="25907-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="25907-208">Varmista, että **Varasto**-kentän arvo on **24**.</span><span class="sxs-lookup"><span data-stu-id="25907-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="25907-209">Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto** ja sitten **Ylläpidä**-ryhmässä **Erävaraus**.</span><span class="sxs-lookup"><span data-stu-id="25907-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="25907-210">**Erävaraus**-sivulla näkyy luettelo eristä, jotka voidaan varata tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="25907-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="25907-211">Tässä esimerkissä määränä on **20** eränumerolle **B11** ja **10** eränumerolle **B22**.</span><span class="sxs-lookup"><span data-stu-id="25907-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="25907-212">Huomaa, että **Erävaraus**-sivua ei voi käyttää riviltä, jos rivin nimikkeelle on määritetty Erä alla\[sijainti\] -varaushierarkia, ellei sitä ole määritetty sallimaan eräkohtaista varausta.</span><span class="sxs-lookup"><span data-stu-id="25907-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-213">Varataksesi ostotilaukselle tietyn erän sinun on käytettävä **Erävaraus** -sivua.</span><span class="sxs-lookup"><span data-stu-id="25907-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="25907-214">Jos syötät eränumeron suoraan myyntitilausriville, järjestelmä toimii siten kuin olisit syöttänyt tietyn eräarvon nimikkeelle, johon sovelletaan Erä alla\[sijainti\] -varauskäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="25907-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="25907-215">Kun tallennat rivin, näyttöön tulee varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="25907-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="25907-216">Jos vahvistat, että eränumero on määritettävä suoraan tilausrivillä, tavanomainen varastonhallintalogiikka ei käsittele kyseistä riviä.</span><span class="sxs-lookup"><span data-stu-id="25907-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="25907-217">Jos varaat määrän **Varaus**-sivulta, tiettyä erää ei varata ja rivin osalta sovelletaan varastotoimintojen suorittamiseen niitä sääntöjä, joita sovelletaan Erä alla\[sijainti\] -varastokäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="25907-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="25907-218">Yleensä tämä sivu toimii ja siihen sovelletaan samaa vuorovaikutusta kuin silloin, kun asianomaisille nimikkeille on määritetty Erä yllä\[sijainti\] -tyyppinen varaushierarkia.</span><span class="sxs-lookup"><span data-stu-id="25907-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="25907-219">Seuraavat poikkeukset kuitenkin pätevät:</span><span class="sxs-lookup"><span data-stu-id="25907-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="25907-220">**Lähderiville sidotut eränumerot** -pikavälilehdessä näkyvät tilausriville varatut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="25907-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="25907-221">Ruudukon eräarvot näkyvät koko tilausrivin toteutusjakson aikana, varaston käsittelyvaiheet mukaan luettuna.</span><span class="sxs-lookup"><span data-stu-id="25907-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="25907-222">**Yhteenveto**-pikavälilehdessä ruudukossa sen sijaan näkyy tavanomainen tilausrivin varaus (eli **Sijainti**-tason yläpuoleisille dimensioille tehtävä varaus) aina siihen asti, kun varastotyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="25907-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="25907-223">Tämän jälkeen rivinvaraus siirtyy työyksikölle, eikä rivinvaraus enää ole näkyvissä sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="25907-224">**Lähderiviin sidotut eränumerot** -pikavälilehti auttaa sen varmistamisessa, että myyntitilausten käsittelijä näkee asiakkaan tilaukseen missä tahansa sen elinkaaren aikana aina laskutukseen asti sidotut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="25907-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="25907-225">Tietyn erän varauksen lisäksi käyttäjä voi valita erän sijainnin ja rekisterikilven manuaalisesti sen sijaan, että se antaisi järjestelmän valita ne automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="25907-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="25907-226">Tämä ominaisuus liittyy tilaussidonnaisen erävarausmekanismin rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="25907-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="25907-227">Kuten aiemmin mainittiin, kun nimikkeelle varataan eränumero Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="25907-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="25907-228">Tämän vuoksi varastotyössä käytetään tilauksia käsitelleiden käyttäjien varaamia varastodimensioita, eivätkä ne aina välttämättä vastaa nimikkeen kätevää tai edes mahdollista varastointipaikkaa keräilytoimintoja varten.</span><span class="sxs-lookup"><span data-stu-id="25907-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="25907-229">Jos tilausten käsittelijät ovat tietoisia varaston rajoituksista, heidän saattaa kannattaa valita sijainnit ja rekisterikilvet manuaalisesti, kun he varaavat erää.</span><span class="sxs-lookup"><span data-stu-id="25907-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="25907-230">Tällöin käyttäjän on käytettävä **Näytä dimensiot** -toimintoa sivun otsikossa ja lisättävä sijainti ja rekisterikilpi **Yhteenveto**-pikavälilehden ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="25907-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="25907-231">Valitse **Erävaraus**-sivulla erän **B11** rivi ja sitten **Varaa rivi**.</span><span class="sxs-lookup"><span data-stu-id="25907-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="25907-232">Sijaintien ja rekisterikilpien määritykselle ei ole omaa logiikkaansa automaattisen varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="25907-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="25907-233">Voit syöttää määrän manuaalisesti **Varaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="25907-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="25907-234">Huomaa, että **Lähderiviin sidotut eränumerot**-pikavälilehdessä erän **B11** arvona on **Sidottu**.</span><span class="sxs-lookup"><span data-stu-id="25907-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tietyn eränumeron sitominen myyntitilausriviin erävaraussivulla](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="25907-236">Myyntitilausrivin määrä voidaan varata eri eristä.</span><span class="sxs-lookup"><span data-stu-id="25907-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="25907-237">Myös samaa erää voidaan varata useiden sijaintien ja rekisterikilpien perusteella (jos rekisterikilvet on sallittu sijainneille).</span><span class="sxs-lookup"><span data-stu-id="25907-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="25907-238">Tietyn erän varaaminen myyntitilausrivin määrälle voi olla myös osittaista.</span><span class="sxs-lookup"><span data-stu-id="25907-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="25907-239">Esimerkiksi 100 yksikön kokonaismäärä voidaan varata siten, että tietty erä on sidottu 20 yksikköön, kun taas 80 yksikköä varataan toimipaikka- ja varastotasolla mistä tahansa käytettävissä olevasta erästä.</span><span class="sxs-lookup"><span data-stu-id="25907-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="25907-240">Tässä tapauksessa varastonhallintajärjestelmä käsittelee keräilytoiminnot käyttäen kahta erillistä työriviä.</span><span class="sxs-lookup"><span data-stu-id="25907-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="25907-241">Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="25907-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="25907-242">Valitse nimikkeesi ja sitten **Hallitse varastoa** \> **Näytä** \> **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="25907-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tilaussidonnainen varaus varastotapahtumatyyppinä](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="25907-244">Tarkista nimikkeen varastotapahtumat, jotka liittyvät myyntitilausrivin varaukseen.</span><span class="sxs-lookup"><span data-stu-id="25907-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="25907-245">Tapahtuma, jossa **Viite**-kentän arvona on **Myyntitilaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta **Sijainti**-tason yläpuolella olevien dimension osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="25907-246">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat toimipaikka, varasto ja varastotila.</span><span class="sxs-lookup"><span data-stu-id="25907-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="25907-247">Tapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta määritetyn erän ja kaikkien sen yläpuolella olevien dimensioiden osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="25907-248">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat eränumero ja sijainti.</span><span class="sxs-lookup"><span data-stu-id="25907-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="25907-249">Tässä esimerkissä sijainti on **Bulkki-001**.</span><span class="sxs-lookup"><span data-stu-id="25907-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="25907-250">Valitse myyntitilauksen otsikossa **Varasto** \> **Toiminnot** \> **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="25907-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="25907-251">Tilausrivi on nyt aallotettu, ja kuormitus ja työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="25907-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="25907-252">Niiden varastotöiden tarkistus ja käsittely, joilla on tilaussidonnaisia eränumeroita</span><span class="sxs-lookup"><span data-stu-id="25907-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="25907-253">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** \> **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="25907-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="25907-254">Työllä, joka käsittelee myyntitilausriviin sidottujen erämäärien keräilytoiminnon, on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="25907-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="25907-255">Järjestelmä käyttää työn luomisessa työmalleja, mutten sijaintidirektiivejä.</span><span class="sxs-lookup"><span data-stu-id="25907-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="25907-256">Kaikkia työmalleille määritettyjä vakioasetuksia, kuten keräilyrivien tai tietyn mittayksikön enimmäismäärää, käytetään sen määrittämisessä, milloin uusi työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="25907-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="25907-257">Keräilysijaintien tunnistamisen sijaintidirektiiveihin liittyviä sääntöjä ei kuitenkaan oteta huomioon, koska tilaussidonnaisessa varauksessa määritetään jo kaikki varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="25907-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="25907-258">Nämä varastodimensiot sisältävät varastosäilytystason dimensiot.</span><span class="sxs-lookup"><span data-stu-id="25907-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="25907-259">Siten työ perii kyseiset dimensiot ilman sijaintidirektiivien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="25907-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="25907-260">Eränumeroa ei näytetä keräilyrivillä (kuten työrivillä, joka luodaan nimikkeelle, johon liittyy Erä yllä\[sijainti\]-varaushierarkia). Sen sijaan kohteesta-eränumero ja kaikki muut varastodimensiot näkyvät työrivin työvarastotapahtumassa, joka perustuu tähän liittyviin varastotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="25907-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Varaston varastotapahtuma töille, jotka perustuvat tilaussidonnaiseen varaukseen](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="25907-262">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus**, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="25907-263">Varastotapahtuma, jossa **Viite**-kentän arvona on **Työ**, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="25907-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="25907-264">Varastotoiminnot voivat seuraavaksi suorittaa työt tavanomaiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="25907-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="25907-265">Mobiililaitteen ohjeet kuitenkin ohjeistavat työntekijää keräilemään tiettyä eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="25907-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="25907-266">Varastoympäristöissä, joissa sijainteja hallitaan rekisterikilvillä, työntekijä voi keräillä mistä tahansa vielä varaamattomasta rekisterikilvestä (jota ei siis ole varattu toiselle tilaussidonnaiselle varaukselle tai työlle, joka perustuu tällaiselle varaukselle), kun hän saapuu sijainnille, jossa säilytetään samaa erää useissa rekisterikilvissä.</span><span class="sxs-lookup"><span data-stu-id="25907-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="25907-267">Jos on epäkäytännöllistä keräillä työrivillä määritetystä sijainnista, varasto-operaattorit voivat käyttää jotakin seuraavista toiminnoista tietyn erän keräilyn siirtämiseen kätevämpään sijaintiin:</span><span class="sxs-lookup"><span data-stu-id="25907-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="25907-268">Vakiomuotoinen mobiililaitteen **Ohita toiminto** (jos varastotyöntekijän **Salli keräilysijainnin ohitus** -asetus on käytössä)</span><span class="sxs-lookup"><span data-stu-id="25907-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="25907-269">**Muuta sijaintia** -toiminto **Työluettelon tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="25907-270">Lopeta työn keräily ja hyllytys mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="25907-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="25907-271">Eränumeroa **B11** on nyt kerätty määrä **10** myyntitilausriviä varten ja siirretty sijaintiin **Lastauspaikan ovi**.</span><span class="sxs-lookup"><span data-stu-id="25907-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="25907-272">Tässä vaiheessa se on valmis lastattavaksi kuorma-autoon ja lähetettäväksi asiakkaan osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="25907-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="25907-273">Joustava rekisterikilven varaus</span><span class="sxs-lookup"><span data-stu-id="25907-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="25907-274">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="25907-274">Business scenario</span></span>

<span data-ttu-id="25907-275">Tässä skenaariossa yritys käyttää varastonhallintaa ja töiden käsittelyä ja käsittelee kuormituksen suunnittelun yksittäisten kuormalavojen/konttien tasolla Supply Chain Management -sovelluksen ulkopuolella ennen työn luomista.</span><span class="sxs-lookup"><span data-stu-id="25907-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="25907-276">Rekisterikilvet edustavat näitä kontteja varastodimensioissa.</span><span class="sxs-lookup"><span data-stu-id="25907-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="25907-277">Tämän vuoksi tietyt rekisterikilvet on määritettävä ennalta myyntitilausriveille ennen keräilytyön tekemistä.</span><span class="sxs-lookup"><span data-stu-id="25907-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="25907-278">Yritys toivoo joustavuutta rekisterikilpien varaussääntöjen käsittelyssä, jotta seuraava toiminta olisi mahdollista:</span><span class="sxs-lookup"><span data-stu-id="25907-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="25907-279">Rekisterikilpi voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="25907-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="25907-280">Tämä auttaa takaamaan, että suunniteltu rekisterikilpi toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="25907-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="25907-281">Jos rekisterikilpeä ei ole vielä määritetty myyntitilausriville, varaston henkilöstö voi valita rekisterikilven keräilyn aikana, kun myyntitilauksen rekisteröinti ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="25907-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="25907-282">Joustavan rekisterikilven varauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="25907-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="25907-283">Ennen kuin voit käyttää joustavaa rekisterikilpien varausta, kaksi ominaisuutta on otettava käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="25907-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="25907-284">Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="25907-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="25907-285">Ominaisuudet on otettava käyttöön seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="25907-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="25907-286">**Ominaisuuden nimi:** *Joustava varastotason dimensioiden varauskäytäntö*</span><span class="sxs-lookup"><span data-stu-id="25907-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="25907-287">**Ominaisuuden nimi:** *Joustava tilaussidonnainen rekisterikilven varaus*</span><span class="sxs-lookup"><span data-stu-id="25907-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="25907-288">Tietyn rekisterikilven varaus myyntitilauksessa</span><span class="sxs-lookup"><span data-stu-id="25907-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="25907-289">Jos haluat ottaa käyttöön rekisterikilven varauksen tilauksessa, valitse **Salli varaus kysyntätilauksessa** -valintaruutu **Rekisterikilpi**-tasolla **Varaston varaushierarkiat** -sivulla hierarkialle, joka on liitetty tiettyyn nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="25907-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Joustavan rekisterikilven varaushierarkian Varaston varaushierarkiat -sivu](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="25907-291">Voit ottaa rekisterikilven varauksen käyttöön tilauksessa missä tahansa käyttöönoton vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="25907-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="25907-292">Tämä muutos ei vaikuta varauksiin tai avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="25907-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="25907-293">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos avointen lähtevien varastotapahtumien varasto-ottotyyppi on *Tilauksessa*, *Varattu tilattu* tai *Varattu fyysinen* on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="25907-294">Vaikka **Salli varaus kysyntätilauksessa** -valintaruutu olisi valittu **Rekisterikilpi**-tasolla, tilauksen tietyn rekisterikilven varaaminen *ei* silti ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="25907-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="25907-295">Tässä tapauksessa käytetään varaushierarkian oletusvarastotoimintojen logiikkaa.</span><span class="sxs-lookup"><span data-stu-id="25907-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="25907-296">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) -protokollaa. Sovelluksessa tämä varaus tehdään suoraan myyntitilauksesta käyttämällä **Tilaussidonnaisia varauksia rekisterikilpeä kohti** -asetusta **Avaa Excelissä** -komennolla.</span><span class="sxs-lookup"><span data-stu-id="25907-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="25907-297">Excel-lisäosassa avattaviin entiteettitietoihin on annettava seuraavat varaukseen liittyvät tiedot ja valittava sitten **Julkaise**, jotta tiedot lähetetään takaisin Supply Chain Management -sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="25907-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="25907-298">Viite (vain *Myyntitilaus*-arvoa tuetaan).</span><span class="sxs-lookup"><span data-stu-id="25907-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="25907-299">Tilausnumero (arvo voidaan johtaa erästä).</span><span class="sxs-lookup"><span data-stu-id="25907-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="25907-300">Erätunnus</span><span class="sxs-lookup"><span data-stu-id="25907-300">Lot ID</span></span>
- <span data-ttu-id="25907-301">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="25907-301">License plate</span></span>
- <span data-ttu-id="25907-302">Määrä</span><span class="sxs-lookup"><span data-stu-id="25907-302">Quantity</span></span>

<span data-ttu-id="25907-303">Jos sinun on varattava tietty eräseuratun nimikkeen rekisterikilpi, käytä **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="25907-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="25907-304">Kun varaston toiminnot ovat käsitelleet tilaussidonnaista rekisterikilven varausta käyttävän myyntitilausrivin, sijaintidirektiivejä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="25907-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="25907-305">Jos varaston työnimike sisältää rivejä, jotka vastaavat kokonaista lavaa ja joilla on rekisterikilpisidonnaisia määriä, voit optimoida keräysprosessin käyttämällä mobiililaitteen valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -vaihtoehdon arvoksi on määritetyt *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="25907-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="25907-306">Varastotyöntekijä voi sitten skannata rekisterikilven ja viimeistellä keräilyn sen sijaan, että työn nimikkeet skannattaisiin yksitellen.</span><span class="sxs-lookup"><span data-stu-id="25907-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Mobiililaitteen valikon vaihtoehto, jossa Käsittele rekisterikilven mukaan -asetuksen arvoksi on määritetty Kyllä](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="25907-308">Koska **Käsittele rekisterikilven mukaan** -toiminto ei tue työtä, joka koskee useita lavoja, eri rekisterikilville on paras olla erilliset työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="25907-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="25907-309">Jos haluat käyttää tätä menetelmää, lisää **Tilaussidonnaisen rekisterikilven tunnus** -kenttää työn otsikon katkaisuna **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="25907-310">Tilaussidonnaisessa työn luontiprosessissa tilaussidonnaisen varastodimension arvo määritetään työrivien poimimiseen eikä rekisterikilven arvoa voi tarkastella suoraan.</span><span class="sxs-lookup"><span data-stu-id="25907-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="25907-311">Vain *käyttäjäohjattua* prosessia tuetaan mobiililaitteen valikkovaihtoehtoa määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="25907-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="25907-312">Esimerkkiskenaario: Tilaussidonnaisen rekisterikilven varauksen määrittäminen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="25907-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="25907-313">Tässä skenaariossa esitetään, miten tilaussidonnaisen rekisterikilven varaus määritetään ja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="25907-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="25907-314">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="25907-314">Make demo data available</span></span>

<span data-ttu-id="25907-315">Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Supply Chain Management -sovelluksen vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="25907-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="25907-316">Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, varmista, että käytät ympäristöä, johon on asennettu esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="25907-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="25907-317">Sinun on myös määritettävä yritykseksi **USMF**, ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="25907-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="25907-318">Luo varaston varaushierarkia, joka mahdollistaa rekisterikilven varauksen</span><span class="sxs-lookup"><span data-stu-id="25907-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="25907-319">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="25907-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="25907-320">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="25907-320">Select **New**.</span></span>
1. <span data-ttu-id="25907-321">Anna nimi **Nimi**-kenttään arvo (esimerkiksi *JoustavaRK*).</span><span class="sxs-lookup"><span data-stu-id="25907-321">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="25907-322">Anna kuvaus **Kuvaus**-kenttään arvo (esim. *Joustavan RK:n varaus*).</span><span class="sxs-lookup"><span data-stu-id="25907-322">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="25907-323">Valitse **Valittu**-luettelossa **Eränumero**, **Sarjanumero** ja **Omistaja**.</span><span class="sxs-lookup"><span data-stu-id="25907-323">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="25907-324">Valitse **Poista**-painike ![taaksepäin osoittava nuoli](media/backward-button.png), jos haluat siirtää valitut tietueet **käytettävissä olevien** luetteloon.</span><span class="sxs-lookup"><span data-stu-id="25907-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="25907-325">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="25907-325">Select **OK**.</span></span>
1. <span data-ttu-id="25907-326">Valitse **Rekisterikilpi**-dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="25907-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="25907-327">**Sijainti**-taso valitaan automaattisesti, etkä voi tyhjentää sen valintaruutua.</span><span class="sxs-lookup"><span data-stu-id="25907-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="25907-328">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="25907-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="25907-329">Kahden vapautetun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="25907-329">Create two released products</span></span>

1. <span data-ttu-id="25907-330">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="25907-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="25907-331">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="25907-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="25907-332">Aseta **Uusi vapautettu tuote** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="25907-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="25907-333">**Tuotenumero:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="25907-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="25907-334">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="25907-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="25907-335">**Nimikemalliryhmä:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="25907-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="25907-336">**Nimikeryhmä:** *Ääni*</span><span class="sxs-lookup"><span data-stu-id="25907-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="25907-337">**Varastodimensioryhmä:** *Kauppatavara*</span><span class="sxs-lookup"><span data-stu-id="25907-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="25907-338">**Seurantadimensioryhmä:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="25907-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="25907-339">**Varaushierarkia:** *JoustavaRK*</span><span class="sxs-lookup"><span data-stu-id="25907-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="25907-340">Valitse **OK** luodaksesi tuotteen. Sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="25907-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="25907-341">Uusi tuote avataan.</span><span class="sxs-lookup"><span data-stu-id="25907-341">The new product is opened.</span></span> <span data-ttu-id="25907-342">Määritä **Varasto**-pikavälilehden **Yksikön sarjaryhmän tunnus** -kenttään *kpl*.</span><span class="sxs-lookup"><span data-stu-id="25907-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="25907-343">Toista edelliset vaiheet ja luo toinen tuote, jolla on samat asetukset. Määritä kuitenkin **Tuotenumero**- ja **Nimiketunnus**-kenttien arvoksi *Nimike2*.</span><span class="sxs-lookup"><span data-stu-id="25907-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="25907-344">Valitse toimintoruudun **Varastonhallinta**-välilehden **Näytä**-ryhmässä **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="25907-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="25907-345">Valitse sitten **Määrän oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="25907-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="25907-346">Oikaise uusien nimikkeiden käytettävissä olevaa varastoa seuravan taulukon mukaan.</span><span class="sxs-lookup"><span data-stu-id="25907-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="25907-347">Kohde</span><span class="sxs-lookup"><span data-stu-id="25907-347">Item</span></span>  | <span data-ttu-id="25907-348">Varasto</span><span class="sxs-lookup"><span data-stu-id="25907-348">Warehouse</span></span> | <span data-ttu-id="25907-349">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="25907-349">Location</span></span> | <span data-ttu-id="25907-350">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="25907-350">License plate</span></span> | <span data-ttu-id="25907-351">Määrä</span><span class="sxs-lookup"><span data-stu-id="25907-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="25907-352">Nimike1</span><span class="sxs-lookup"><span data-stu-id="25907-352">Item1</span></span> | <span data-ttu-id="25907-353">24</span><span class="sxs-lookup"><span data-stu-id="25907-353">24</span></span>        | <span data-ttu-id="25907-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="25907-354">FL-010</span></span>   | <span data-ttu-id="25907-355">RK01</span><span class="sxs-lookup"><span data-stu-id="25907-355">LP01</span></span>          | <span data-ttu-id="25907-356">10</span><span class="sxs-lookup"><span data-stu-id="25907-356">10</span></span>       |
    | <span data-ttu-id="25907-357">Nimike1</span><span class="sxs-lookup"><span data-stu-id="25907-357">Item1</span></span> | <span data-ttu-id="25907-358">24</span><span class="sxs-lookup"><span data-stu-id="25907-358">24</span></span>        | <span data-ttu-id="25907-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="25907-359">FL-011</span></span>   | <span data-ttu-id="25907-360">RK02</span><span class="sxs-lookup"><span data-stu-id="25907-360">LP02</span></span>          | <span data-ttu-id="25907-361">10</span><span class="sxs-lookup"><span data-stu-id="25907-361">10</span></span>       |
    | <span data-ttu-id="25907-362">Nimike2</span><span class="sxs-lookup"><span data-stu-id="25907-362">Item2</span></span> | <span data-ttu-id="25907-363">24</span><span class="sxs-lookup"><span data-stu-id="25907-363">24</span></span>        | <span data-ttu-id="25907-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="25907-364">FL-010</span></span>   | <span data-ttu-id="25907-365">RK01</span><span class="sxs-lookup"><span data-stu-id="25907-365">LP01</span></span>          | <span data-ttu-id="25907-366">5</span><span class="sxs-lookup"><span data-stu-id="25907-366">5</span></span>        |
    | <span data-ttu-id="25907-367">Nimike2</span><span class="sxs-lookup"><span data-stu-id="25907-367">Item2</span></span> | <span data-ttu-id="25907-368">24</span><span class="sxs-lookup"><span data-stu-id="25907-368">24</span></span>        | <span data-ttu-id="25907-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="25907-369">FL-011</span></span>   | <span data-ttu-id="25907-370">RK02</span><span class="sxs-lookup"><span data-stu-id="25907-370">LP02</span></span>          | <span data-ttu-id="25907-371">5</span><span class="sxs-lookup"><span data-stu-id="25907-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="25907-372">Sinun on luotava kaksi rekisterikilpeä ja käytettävä sijainteja, joissa sallitaan yhdistetyt nimikkeet, kuten *FL-010* ja *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="25907-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="25907-373">Myyntitilauksen luominen ja tietyn rekisterikilven varaaminen</span><span class="sxs-lookup"><span data-stu-id="25907-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="25907-374">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25907-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="25907-375">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="25907-375">Select **New**.</span></span>
1. <span data-ttu-id="25907-376">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="25907-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="25907-377">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="25907-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="25907-378">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="25907-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="25907-379">Valitse **OK** ja sulje **Luo myyntitilaus** -valintaikkuna. Avaa sitten uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="25907-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="25907-380">Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="25907-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="25907-381">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="25907-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="25907-382">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="25907-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="25907-383">Lisää toinen myyntitilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="25907-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="25907-384">**Nimiketunnus:** *Nimike2*</span><span class="sxs-lookup"><span data-stu-id="25907-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="25907-385">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="25907-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="25907-386">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="25907-386">Select **Save**.</span></span>
1. <span data-ttu-id="25907-387">Anna **Rivin tiedot** -pikavälilehdessä **Asetukset**-välilehdessä **Erätunnus**-arvo jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="25907-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="25907-388">Nämä arvot ovat pakollisia tiettyjen rekisterikilpien varauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-389">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä **tilaussidonnaisia varauksia rekisterikilpeä kohti** -tietoyksikköä.</span><span class="sxs-lookup"><span data-stu-id="25907-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="25907-390">Jos sinun on varattava tietyn rekisterikilven eräseurattu nimike, voit käyttää myös **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="25907-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="25907-391">Jos annat rekisterikilven suoraan myyntitilausriville ja vahvistat sen järjestelmässä, rivillä ei käytetä varastonhallinnan käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="25907-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="25907-392">Valitse **Avaa Microsoft Officessa**, valitse **Tilaussidonnaiset varaukset rekisterikilpeä kohti** ja lataa tiedosto.</span><span class="sxs-lookup"><span data-stu-id="25907-392">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="25907-393">Avaa ladattu tiedosto Excelissä ja valitse **Ota muokkaus käyttöön** -painike, jotta voit ajaa Excel-lisäosan.</span><span class="sxs-lookup"><span data-stu-id="25907-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="25907-394">Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan**.</span><span class="sxs-lookup"><span data-stu-id="25907-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="25907-395">Jos näet kirjautumisruudun, valitse **Kirjaudu sisään** samoilla tunnuksilla, joilla kirjaudut Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="25907-395">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="25907-396">Jos haluat varata nimikkeen tietystä rekisterikilvestä, valitse Excelin lisäosassa **Uusi** ja lisää varausrivi. Määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="25907-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="25907-397">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike1*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="25907-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="25907-398">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="25907-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="25907-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="25907-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="25907-400">Lisää toinen varausrivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="25907-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="25907-401">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike2*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="25907-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="25907-402">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="25907-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="25907-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="25907-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="25907-404">Valitse Excelin lisäosassa **Julkaise** ja lähetä tiedot takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="25907-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-405">Varausrivi tulee näkyviin järjestelmään vain, jos julkaisemisessa ei ole tehty virheitä.</span><span class="sxs-lookup"><span data-stu-id="25907-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="25907-406">Siirry takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="25907-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="25907-407">Voit tarkistaa nimikkeen varauksen **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Ylläpidä \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="25907-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="25907-408">Ota huomioon, että *Nimike1* -kohdan myyntitilausrivillä varataan varastoa *10* ja *Nimike2*-kohdan myyntitilausrivillä varataan varastoa *5*.</span><span class="sxs-lookup"><span data-stu-id="25907-408">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="25907-409">Voit tarkastella varastotapahtumia, jotka liittyvät myyntitilausrivin varaukseen, **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Näytä \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="25907-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="25907-410">Huomaa, että varaukseen liittyy kaksi tapahtumaa. Toisen **Viite**-kentän arvoksi on määritetty *Myyntitilaus* ja toisen **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="25907-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-411">Tapahtuma, jossa **Viite**-kentän arvoksi on määritetty *Myyntitilaus*, edustaa tilausrivin varausta varastodimensioissa, jotka ovat yli **Sijainti**-tason (toimipaikka, varasto ja varaston tila).</span><span class="sxs-lookup"><span data-stu-id="25907-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="25907-412">Tapahtuma, jonka **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*, vastaa tietyn rekisterikilven ja sijainnin tilausrivin varausta.</span><span class="sxs-lookup"><span data-stu-id="25907-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="25907-413">Jos haluat vapauttaa myyntitilauksen, valitse toimintoruudun **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="25907-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="25907-414">Varaston työn tarkistaminen ja käsitteleminen määritettyjen tilaussidonnaisten rekisterikilpien avulla</span><span class="sxs-lookup"><span data-stu-id="25907-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="25907-415">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="25907-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="25907-416">Kun varaus on tehty tietylle erälle, järjestelmä ei käytä sijaintidirektiivejä, kun rekisterikilven varausta käyttävälle myyntitilaukselle luodaan työ.</span><span class="sxs-lookup"><span data-stu-id="25907-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="25907-417">Koska tilaussidonnainen varaus määrittää kaikki varastodimensiot, mukaan lukien sijainnin, sijaintidirektiivejä ei tarvitse käyttää, koska nämä varastodimensiot on juuri syötetty työhön.</span><span class="sxs-lookup"><span data-stu-id="25907-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="25907-418">Ne näkyvät **Varastodimensioista**-osassa **Työn varastotapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-419">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on *Tilaussidonnainen varaus*, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="25907-420">Varastotapahtuma, jossa **Viite**-kentän arvona on *Työ*, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="25907-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="25907-421">Tee työn keräily ja hyllytys valmiiksi mobiililaitteessa käyttämällä valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="25907-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25907-422">**Käsittele rekisterikilven mukaan** -toiminto auttaa koko rekisterikilven käsittelemisessä.</span><span class="sxs-lookup"><span data-stu-id="25907-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="25907-423">Jos sinun on käsiteltävä rekisterikilven osa, et voi käyttää tätä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="25907-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="25907-424">On suositeltavaa, että kustakin rekisterikilvestä luodaan erilliset työt.</span><span class="sxs-lookup"><span data-stu-id="25907-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="25907-425">Voit saavuttaa tämän tuloksen käyttämällä **Työn otsikoiden katkaisut** -ominaisuutta **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="25907-426">Rekisterikilpi *RK02* on nyt kerätty myyntitilausriveille ja hyllytetty *Lastausovi*-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="25907-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="25907-427">Tässä vaiheessa se on valmis lastattavaksi ja lähetettäväksi asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="25907-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="25907-428">Niiden varastotöiden poikkeustenkäsittely, joilla on tilaussidonnaiset eränumerot</span><span class="sxs-lookup"><span data-stu-id="25907-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="25907-429">Tilaussidonnaisten eränumeroiden keräilyn varastotyöhön sovelletaan samoja varaston poikkeustenkäsittelyä ja -toimintoja kuin tavanomaiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="25907-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="25907-430">Yleisesi ottaen avoin työ tai työrivi voidaan peruuttaa, se voidaan keskeyttää, koska käyttäjän sijainti on täynnä, siihen voidaan soveltaa lyhyttä keräilyä ja sitä voidaan päivittää siirron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="25907-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="25907-431">Samoin jo valmiiksi saatua keräiltyä työmäärää voidaan vähentää tai työ voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="25907-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="25907-432">Kaikkiin näihin poikkeusten käsittelyn toimintoihin sovelletaan seuraavaa keskeistä sääntöä: asiakkaalle varattua eränumeroa ei voi koskaan korvata toisella eränumerolla, mutta sen varastodimensioita (sijainti ja rekisterikilpi) voi muuttaa joko käyttäjän manuaalisella päivityksellä tai järjestelmän automaattisella päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="25907-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="25907-433">Automaattinen päivitys perustuu samaan varastodimensioiden satunnaiseen määrittämiseen, jota käytetään, kun tietty erä varataan automaattisesti mutta varastodimensioita ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="25907-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="25907-434">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="25907-434">Example scenario</span></span>

<span data-ttu-id="25907-435">Esimerkki tästä skenaariosta on tilanne, jossa aiemmin valmistuneiden töiden keräily perutaan **Vähennä keräiltyä määrää** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="25907-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="25907-436">Tässä esimerkissä oletetaan, että olet jo tehnyt [Esimerkkiskenaario: Eränumeron kohdistus](#Example-batch-allocation) -kohdassa kerrotut vaiheet.</span><span class="sxs-lookup"><span data-stu-id="25907-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="25907-437">Se jatkuu kyseisestä esimerkistä.</span><span class="sxs-lookup"><span data-stu-id="25907-437">It continues from that example.</span></span>

1. <span data-ttu-id="25907-438">Siirry kohtaan **Varastonhallinta** \> **Kuormat** \> **Aktiiviset kuormat**.</span><span class="sxs-lookup"><span data-stu-id="25907-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="25907-439">Valitse kuorma, joka on luotu myyntitilauksen lähetyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="25907-440">Valitse **Kuormatilauksen rivit** -pikavälilehdestä **Vähennä keräiltyä määrää**.</span><span class="sxs-lookup"><span data-stu-id="25907-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="25907-441">Valitse **Vähennä keräiltyä määrää** -sivun **Siirrä sijaintiin** -kentässä **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="25907-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="25907-442">Valitse **Siirrä rekisterikilvelle**-kentässä **LP33**.</span><span class="sxs-lookup"><span data-stu-id="25907-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="25907-443">Syötä **Peruttava keräilty varastomäärä** -kenttään arvo **10**.</span><span class="sxs-lookup"><span data-stu-id="25907-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="25907-444">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="25907-444">Select **OK**.</span></span>

<span data-ttu-id="25907-445">Tässä ovat keräilyn perumisen tulokset:</span><span class="sxs-lookup"><span data-stu-id="25907-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="25907-446">Aiemmin suljetun työn tilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="25907-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="25907-447">Uusi **Varastonsiirto**-tyypin työ luodaan varastomäärälle **10** eränumerossa **B11**.</span><span class="sxs-lookup"><span data-stu-id="25907-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="25907-448">Tämä työ edustaa siirtoa sijainnista **Lastauspaikan ovi** rekisterikilvelle **LP33** sijainnissa **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="25907-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="25907-449">Tilaksi määritetään **Suljettu**.</span><span class="sxs-lookup"><span data-stu-id="25907-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="25907-450">Järjestelmä varaa uudelleen alun perin tilatun eränumeron ja määrittää sijainnin ja rekisterikilpitunnukset.</span><span class="sxs-lookup"><span data-stu-id="25907-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="25907-451">(Tämä prosessi vastaa **Vara rivi** -toiminnon suorittamista tietyn eränumeron tilausriville).</span><span class="sxs-lookup"><span data-stu-id="25907-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="25907-452">Tämän tuloksena erä **B11** näkyy sidottuna **Lähderiville sidotut eränumerot** -pikavälilehdessä sivulla **Erävaraus** ja **Varaus**-kentässä on määrä **10** eränumeron **B11** osalta.</span><span class="sxs-lookup"><span data-stu-id="25907-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="25907-453">Lisäksi **Sijainti**-kentän arvona on **FL-001** ja **Rekisterikilpi**-kentän arvona on **LP11**.</span><span class="sxs-lookup"><span data-stu-id="25907-453">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="25907-454">(Voit lisätä nämä kentät ruudukkoon, jos ne eivät ole näkyvissä.)</span><span class="sxs-lookup"><span data-stu-id="25907-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="25907-455">Seuraavissa taulukoissa on yhteenveto siitä, miten järjestelmä käsittelee tiettyjen varastotoimintojen tilaussidonnaisen erävarauksen.</span><span class="sxs-lookup"><span data-stu-id="25907-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="25907-456">Taulukkojen sisältöä tulkitaan olettamalla, että kukin varastotoiminnon suorittamiseen liittyy olemassa oleva tilaussidonnaiseen erävaraukseen perustuvaa työ tai että kunkin varastotoiminnon suorittaminen vaikuttaa kyseisentyyppiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="25907-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="25907-457">Näissä taulukoissa Erämäärä on käytettävissä -sarake ilmaisee, onko varastomäärää käytettävissä sen määrän lisäksi, joka on jo varattu kulloisillekin tilaussidonnaisille varauksille tai joka on varattu kyseisentyyppisiin varauksiin perustuvassa varastotyössä.</span><span class="sxs-lookup"><span data-stu-id="25907-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="25907-458">Avoimen työn keräilysijainnin ohitus</span><span class="sxs-lookup"><span data-stu-id="25907-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-459">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-460">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-461">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-461">Key user steps</span></span></th>
<th><span data-ttu-id="25907-462">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-462">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-463">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="25907-464"><strong>Salli keräilysijainnin ohitus</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="25907-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="25907-465">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-466">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastointisovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="25907-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="25907-467">Valitse <strong>Ehdota</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="25907-468">Vahvista uusi sijainti, jota ehdotetaan erämäärän käytettävyyden perusteella.</span><span class="sxs-lookup"><span data-stu-id="25907-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-469">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="25907-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="25907-470">Keräilyrivin sijainniksi päivittyy uusi sijainti.</span><span class="sxs-lookup"><span data-stu-id="25907-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="25907-471">(Jos sijainti on rekisterikilpihallittu, työvarastotapahtumalle määritetään satunnainen rekisterikilpi ja työntekijä voi keräillä mistä tahansa rekisterikilvestä, jossa määrää on käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="25907-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="25907-472">Jos määrää on uuden sijainnin useassa rekisterikilvessä, alkuperäinen keräilyrivi jaetaan useaan riviin, jotka vastaavat kutakin rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="25907-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-473">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-474">Nro</span><span class="sxs-lookup"><span data-stu-id="25907-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-475">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastointisovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="25907-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="25907-476">Määritä sijainti manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="25907-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-477"><strong>Ohita sijainti</strong> -toiminto ei ole mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="25907-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="25907-478">Se epäonnistuu, ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="25907-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="25907-479">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="25907-480">Täysi-painike – Työrivin jakaminen käyttäjän sijainnin ylivuodon vuoksi</span><span class="sxs-lookup"><span data-stu-id="25907-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-481">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-482">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-483">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-483">Key user steps</span></span></th>
<th><span data-ttu-id="25907-484">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-484">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-485">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="25907-486"><strong>Salli työn jakaminen</strong> -asetus on käytössä mobiililaitteen valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="25907-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="25907-487">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-488">Valitse valikkovaihtoehto <strong>Täysi</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="25907-489">Syötä <strong>Keräilymäärä</strong>-kenttään tarvittavan keräilyn osamäärä ilmaisemaan täyttä kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="25907-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-490">Kulloisessakin työssä määrä päivitetään vastaamaan jäljellä olevaa keräiltävää määrää.</span><span class="sxs-lookup"><span data-stu-id="25907-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="25907-491">Keräillylle määrälle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="25907-492">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="25907-493">Valmiin työn keräillyn määrän vähentäminen (kuormasta)</span><span class="sxs-lookup"><span data-stu-id="25907-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-494">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-495">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-496">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-496">Key user steps</span></span></th>
<th><span data-ttu-id="25907-497">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-497">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-498">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="25907-499">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-499">Not applicable</span></span></td>
<td><span data-ttu-id="25907-500">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-501">Avaa <strong>Vähennä keräiltyä määrää</strong> -sivu kuormariviltä.</span><span class="sxs-lookup"><span data-stu-id="25907-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="25907-502">Syötä sen määrän kokonaisarvo, jonka keräily perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="25907-503">Valitse "siirto kohteeseen" sijainti/rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="25907-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="25907-504">Kuormariviin liittyvä työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="25907-505">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-506">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-507">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-508">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-508">No</span></span></td>
<td><span data-ttu-id="25907-509">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-509">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-510">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-510">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-511">Määrä varataan uudelleen samalle erälle ja samalle sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu), jotka on syötetty keräilyn perumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="25907-512">Nimikkeen siirtäminen varastossa</span><span class="sxs-lookup"><span data-stu-id="25907-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="25907-513">Tätä varastotoimintoa voidaan soveltaa vain **Työnluontiprosessi**-tyypin siirtoihin, ei mallin mukaiseen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="25907-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-514">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-515">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-516">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-516">Key user steps</span></span></th>
<th><span data-ttu-id="25907-517">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-517">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-518">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="25907-519"><strong>Salli työhön liitetyn varaston siirto</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="25907-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="25907-520">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-521">Aloita siirto varastointisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="25907-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="25907-522">Anna kohteesta- ja kohteeseen-sijainnit.</span><span class="sxs-lookup"><span data-stu-id="25907-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="25907-523">Kaikissa olemassa olevissa töissä, joihin siirto vaikuttaa, keräilysijainniksi päivitetään uusi kohteeseen-sijainti.</span><span class="sxs-lookup"><span data-stu-id="25907-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="25907-524">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-525">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="25907-526">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-527">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-527">No</span></span></td>
<td><span data-ttu-id="25907-528">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-528">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-529">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-529">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-530">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle ja uudelle kohteeseen-sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="25907-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="25907-531">Valmiin työn keräillyn määrän palauttaminen (kuormasta tai aallosta)</span><span class="sxs-lookup"><span data-stu-id="25907-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-532">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-533">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-534">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-534">Key user steps</span></span></th>
<th><span data-ttu-id="25907-535">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-535">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-536">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="25907-537">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-537">Not applicable</span></span></td>
<td><span data-ttu-id="25907-538">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-539">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="25907-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="25907-540">Valitse pyyntösivulla vaihtoehto <strong>Jätä nimikkeet nykyiseen sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-541">Kaikki tähän Kuormariviin liittyvät työt perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="25907-542">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-543">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-544">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-544">No</span></span></td>
<td><span data-ttu-id="25907-545">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-545">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-546">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-546">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-547">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä jätettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-548">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-549">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="25907-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="25907-550">Valitse pyyntösivulla vaihtoehto <strong>Osoita nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-551">Nykyinen työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="25907-552">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-553">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-554">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-555">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-555">No</span></span></td>
<td><span data-ttu-id="25907-556">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-556">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-557">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-557">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-558">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä osoitettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-559">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="25907-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-560">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="25907-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="25907-561">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-562">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="25907-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="25907-563">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-564">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="25907-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-565">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="25907-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="25907-566">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet sijaintidirektiivien perusteella</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-567">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="25907-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="25907-568">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="25907-569">Määrän lyhytkeräily – Rekisteröi määrä fyysisesti löytymättömäksi sijainnista/rekisterikilvestä, kun keräilytyötä suoritetaan</span><span class="sxs-lookup"><span data-stu-id="25907-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-570">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-571">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-572">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-572">Key user steps</span></span></th>
<th><span data-ttu-id="25907-573">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-573">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-574">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="25907-575">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="25907-576">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-577">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-578">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-579">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-580">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="25907-581"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="25907-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-582">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-583">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-584">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-584">No</span></span></td>
<td><span data-ttu-id="25907-585">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="25907-586">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="25907-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="25907-587">Olemassa oleva työ pysyy avoimena.</span><span class="sxs-lookup"><span data-stu-id="25907-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-588">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="25907-589">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="25907-590">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-591">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-592">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-593">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-594">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="25907-595"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="25907-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-596">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="25907-597">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-598">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-598">No</span></span></td>
<td><span data-ttu-id="25907-599">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-599">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-600">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-600">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-601">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-602">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei/Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="25907-603">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="25907-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="25907-604">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-605">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-606">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-607">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="25907-608">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="25907-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-609">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="25907-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="25907-610">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="25907-611">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="25907-612">Uusi keräilyrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="25907-612">A new pick line is created.</span></span> <span data-ttu-id="25907-613">Siinä käytetään käyttäjän valitsemaa sijaintia/rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="25907-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="25907-614">Uusi hyllytysrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="25907-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="25907-615"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="25907-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-616">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-617">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="25907-618">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="25907-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="25907-619">Nro</span><span class="sxs-lookup"><span data-stu-id="25907-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-620">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-621">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-622">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-623">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="25907-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="25907-624">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-625">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="25907-626">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="25907-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="25907-627">Nro</span><span class="sxs-lookup"><span data-stu-id="25907-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-628">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-629">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-630">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="25907-631">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="25907-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="25907-632">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="25907-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="25907-633">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="25907-634">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="25907-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="25907-635"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="25907-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="25907-636">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin/rekisterikilven määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-637">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Automaattinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä/Ei</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä/Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="25907-638">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-639">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="25907-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="25907-640">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="25907-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="25907-641">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja automaattinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-642">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="25907-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="25907-643">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="25907-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="25907-644">Muuta varaston tilaa</span><span class="sxs-lookup"><span data-stu-id="25907-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="25907-645">Tämä varastotoiminto voidaan suorittaa useista aloituskohdista.</span><span class="sxs-lookup"><span data-stu-id="25907-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="25907-646">Tässä näkyvässä esimerkissä käytetään **Varaston tilanmuutos** -toimintoa **Käytettävissä sijainnin mukaan** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="25907-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="25907-647">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="25907-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="25907-648">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="25907-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="25907-649">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="25907-649">Key user steps</span></span></th>
<th><span data-ttu-id="25907-650">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="25907-650">Warehouse work</span></span></th>
<th><span data-ttu-id="25907-651">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="25907-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="25907-652"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Varaukset</strong> tai <strong>Merkinnät ja varaukset</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="25907-653">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-654">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="25907-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="25907-655">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="25907-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="25907-656">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="25907-657">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-658">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="25907-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="25907-659">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-660">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="25907-661">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="25907-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="25907-662"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="25907-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="25907-663">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-663">No</span></span></td>
<td><span data-ttu-id="25907-664">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-664">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-665">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="25907-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="25907-666">Varaus poistetaan.</span><span class="sxs-lookup"><span data-stu-id="25907-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="25907-667">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="25907-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="25907-668"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="25907-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="25907-669"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Ei mitään</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="25907-670">Kyllä</span><span class="sxs-lookup"><span data-stu-id="25907-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="25907-671">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="25907-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="25907-672">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="25907-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="25907-673">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="25907-674">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="25907-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="25907-675">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="25907-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="25907-676">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="25907-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="25907-677">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="25907-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="25907-678">Ei</span><span class="sxs-lookup"><span data-stu-id="25907-678">No</span></span></td>
<td><span data-ttu-id="25907-679">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="25907-679">See the previous row.</span></span></td>
<td><span data-ttu-id="25907-680">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="25907-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="25907-681">Varastotilan muutokset eivät ole sallittuja.</span><span class="sxs-lookup"><span data-stu-id="25907-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="25907-682">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="25907-682">Limitations</span></span>

- <span data-ttu-id="25907-683">Joustava varastotason dimensionvaraustoiminto ei tue seuraavia ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="25907-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="25907-684">Todellisen painon hallinta</span><span class="sxs-lookup"><span data-stu-id="25907-684">Catch weight management</span></span>
    - <span data-ttu-id="25907-685">Fyysinen negatiivinen varasto</span><span class="sxs-lookup"><span data-stu-id="25907-685">Physical negative inventory</span></span>
    - <span data-ttu-id="25907-686">Varaus tilatun tarjonnan perusteella</span><span class="sxs-lookup"><span data-stu-id="25907-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="25907-687">Siirtotilaukset ja raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="25907-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="25907-688">Kontin direktiiviyksiköittäin pakkaamisen konsolidointisäännöllä on rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="25907-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="25907-689">Tilaussidonnaisten varausten osalta suosittelemme välttämää sellaisten kontinrakennusmallien käyttöä, joissa **Pakkaa direktiiviyksiköittäin** -kenttä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="25907-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="25907-690">Nykyisessä ratkaisussa sijaintidirektiivejä ei käytetä varastotyön luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="25907-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="25907-691">Siksi vain yksikön sarjaryhmän alinta yksikköä (varastoyksikköä) käytetään konttiinpakkauksen aaltovaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="25907-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
