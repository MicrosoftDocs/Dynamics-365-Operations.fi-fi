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
ms.openlocfilehash: 65304216b579b8def493d1e4218174cb9617013d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652176"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="7986b-103">Joustava varastotason dimensionvarauskäytäntö</span><span class="sxs-lookup"><span data-stu-id="7986b-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7986b-104">Kun Erä alla\[sijainti\]-tyyppinen varastonvaraushierarkia yhdistetään tuotteisiin, eräseurattuja tuotteita myyvät ja niiden logistiikan Microsoft Dynamics 365 -varastonhallintajärjestelmävalmiilla (WMS) toiminnoilla toteuttavat yritykset eivät voi varata tiettyjä kyseisten tuotteiden eriä asiakkaiden myyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="7986b-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="7986b-105">Samalla tavalla tiettyjä rekisterikilpiä ei voi varata myyntitilausten tuotteille, kun nämä tuotteet on liitetty oletusvaraushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="7986b-106">Tässä ohjeaiheessa kuvataan varastonvarauskäytäntö, jonka avulla nämä yritykset varaavat tiettyjä eriä tai rekisterikilpiä, vaikka tuotteet on yhdistetty Erä alla\[sijainti\]-varaushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="7986b-107">Varastovaraushierarkia</span><span class="sxs-lookup"><span data-stu-id="7986b-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="7986b-108">Tässä osassa on yhteenveto olemassa olevasta varastonvaraushierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="7986b-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="7986b-109">Varastonvaraushierarkia määrää, että varastodimensioiden osalta kysyntätilaus sisältää pakolliset dimensiot toimipaikka, varasto ja varastotila. Varastologiikka taas vastaa sijainnin osoittamisesta pyydetyille määrille ja kyseisen sijainnin varaamisesta.</span><span class="sxs-lookup"><span data-stu-id="7986b-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="7986b-110">Toisin sanoen kysyntätilauksen ja varastotoimintojen välisissä vuorovaikutuksissa kysyntätilauksen oletetaan ilmaisevan, mistä tilaus on lähetettävä (eli mistä toimipaikasta ja varastosta).</span><span class="sxs-lookup"><span data-stu-id="7986b-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="7986b-111">Tämän jälkeen varasto tukeutuu logiikkaan löytääkseen vaaditun määrän varastotilasta.</span><span class="sxs-lookup"><span data-stu-id="7986b-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="7986b-112">Yrityksen toimintamallin heijastamista varten seurantadimensiot (erä- ja sarjanumerot) ovat joustavampia.</span><span class="sxs-lookup"><span data-stu-id="7986b-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="7986b-113">Varastonvaraushierarkia voi mukautua seuraavankaltaisiin tilanteisiin:</span><span class="sxs-lookup"><span data-stu-id="7986b-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="7986b-114">Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot, sen jälkeen, kun määrät on löydetty varaston säilytystilasta.</span><span class="sxs-lookup"><span data-stu-id="7986b-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="7986b-115">Tätä mallia kutsutaan usein nimellä *Erä alla\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="7986b-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="7986b-116">Sitä käytetään yleensä silloin, kun tuotteen erä- tai sarjanumeron tunnistus ei ole tärkeä asiakkaille, jotka tekevät pyynnön myyjäyritykselle.</span><span class="sxs-lookup"><span data-stu-id="7986b-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="7986b-117">Jos erä- tai sarjanumerot ovat osa asiakkaan tilausmääritystä ja ne tallennetaan kysyntätilaukseen, varastotoiminnot, jotka etsivät määrät varastosta, rajoitetaan tiettyihin pyydettyihin numeroihin, joita ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="7986b-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="7986b-118">Tätä mallia kutsutaan nimellä *Erä yllä\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="7986b-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="7986b-119">Näissä skenaarioissa haasteena on, että kullekin vapautetulle tuotteelle voidaan määrittää vain yksi varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="7986b-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="7986b-120">Siksi, jotta varastonhallintajärjestelmä määrittäisi hierarkian määrittämisen jälkeen, milloin erä- tai sarjanumero pitäisi varata (joko kun kysyntätilaus saadaan tai varaston keräilytyön aikana), kyseistä ajoitusta ei voi muuttaa tilannekohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="7986b-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="7986b-121">Eräseurattujen nimikkeiden joustava varaus</span><span class="sxs-lookup"><span data-stu-id="7986b-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="7986b-122">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="7986b-122">Business scenario</span></span>

<span data-ttu-id="7986b-123">Tässä skenaariossa yritys käyttää varastostrategiaa, jossa valmiita tavaroita seurataan eränumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="7986b-124">Yritys käyttää myös varastonhallinnan työkuormitusta.</span><span class="sxs-lookup"><span data-stu-id="7986b-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="7986b-125">Koska tässä työkuormituksessa on hyvin toimiva logiikka varaston keräily- ja lähetystoimintojen suunnittelulle ja suorittamiselle erämääräisiä nimikkeitä varten, useimmille valmiille nimikkeille määritetään Erä alla\[sijainti\] -varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="7986b-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="7986b-126">Tällaisen operatiivisen määrityksen etuna on, että päätöksiä (jotka ovat käytännössä varauspäätöksiä) siitä, mitkä erät kerätään ja mihin ne laitetaan varastossa, lykätään siihen asti, että varastoin keräilytoiminnot alkavat.</span><span class="sxs-lookup"><span data-stu-id="7986b-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="7986b-127">Niitä ei tehdä, kun asiakkaan tilaus saadaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="7986b-128">Vaikka Erä alla\[sijainti\] -varaushierarkia palvelee yrityksen liiketoimintatavoitteita hyvin, monet yrityksen vakiintuneista asiakkaista tarvitsevat aikaisemmin ostamansa erää, kun ne tilaavat tuotteita uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7986b-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="7986b-129">Siksi yritys etsii joustavuutta erävaraussääntöjen käsittelyyn, jotta asiakkaan samaa nimikettä koskevasta kysynnästä riippuen, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="7986b-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="7986b-130">Eränumero voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi muuttaa varastotoimintojen aikana ja/tai osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="7986b-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="7986b-131">Tämä auttaa takaamaan, että tilattu eränumero toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="7986b-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="7986b-132">Jos eränumerolla ei ole merkitystä asiakkaalle, varastotoiminnot voivat määrittää eränumeron keräilyn aikana, kun myyntitilauksen kirjaus ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="7986b-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="7986b-133">Tietyn erän myyntilaukselle varaamisen mahdollistaminen</span><span class="sxs-lookup"><span data-stu-id="7986b-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="7986b-134">Jotta haluttu erävarauksen joustavuus mahdollistetaan nimikkeille, joilla on Erä alla\[sijainti\] -varastonvaraushierarkia, varastopäällikköjen on valittava **Salli varaus kysyntätilauksessa** -valintaruutu **Eränumero** -tasolla sivulla **Varastonvaraushierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="7986b-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varastovarausten hierarkian joustavoittaminen](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="7986b-136">Kun hierarkian **Eränumero**-taso on valittuna, kaikki kyseisen tason yläpuolella olevat dimensiot aina **Sijainti**-tasolle valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7986b-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="7986b-137">(Oletusarvoisesti kaikki **Sijainti**-tason yläpuolella olevat dimensiot on esivalittu.) Tämä toiminta perustuu logiikkaan, jossa myös kaikki eränumeron ja sijainnin välisen alueen dimensiot varataan automaattisesti, kun varaat tietyn eränumeron tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="7986b-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="7986b-138">**Salli varaus kysyntätilauksessa** -valintaruutu pätee vain varaushierarkiatasoille, jotka ovat varastosijainnin dimension alapuolella.</span><span class="sxs-lookup"><span data-stu-id="7986b-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="7986b-139">**Eränumero** ja **rekisterikilpi** ovat hierarkian ainoat tasot, joihin joustavaa varauskäytäntöä voi soveltaa.</span><span class="sxs-lookup"><span data-stu-id="7986b-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="7986b-140">Toisin sanoen et voi valita **Salli varaus kysyntätilauksessa** -valintaruutua **Sijainti**- tai **Sarjanumero**-tasolle.</span><span class="sxs-lookup"><span data-stu-id="7986b-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="7986b-141">Jos varaushierarkia sisältää sarjanumerodimension (jonka on aina oltava **Eränumero**-tason alapuolella) ja jos olet ottanut eräkohtaisen varauksen käyttöön eränumerolle, järjestelmä jatkaa sarjanumeroiden varaus- ja keräilytoimintojen käsittelyä niiden sääntöjen perusteella, jotka pätevät Sarja alla\[sijainti\] -varauskäytäntöön.</span><span class="sxs-lookup"><span data-stu-id="7986b-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="7986b-142">Voit missä tahansa vaiheessa ottaa eräkohtaisenvarauksen käyttöön olemassa olevalle Erä alla\[sijainti\] -varaushierarkialle ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="7986b-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="7986b-143">Tämä muutos ei vaikuta varauksiin ja avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="7986b-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="7986b-144">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos varasto-ottotyypin **Varattu tilattu**, **Varattu fyysinen** tai **Tilattu** varastotapahtumia on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="7986b-145">Jos nimikkeen käytössä oleva varaushierarkia ei salli erän määritystä tilauksessa, voit siirtää sen varaushierarkiaan, joka sallii erän määrityksen, kunhan hierarkiatasorakenne on sama molemmissa hierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="7986b-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="7986b-146">Tee siirto toiminnolla **Muuta nimikkeiden varaushierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="7986b-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="7986b-147">Tästä muutoksesta voi olla hyötyä, kun haluat estää eräseurattujen nimikkeiden alijoukon joustavan erävarauksen, mutta sallia sen muun tuoteportfolion osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="7986b-148">Riippumatta siitä, oletko valinnut **Salli varaus kysyntätilauksessa** -valintaruudun, jos et halua varata nimikkeelle tiettyä eränumeroa tilausrivillä, oletusarvoinen varastotoimintologiikka, jota sovelletaan Erä alla\[sijainti\] -varaushierarkiaan, pätee edelleen.</span><span class="sxs-lookup"><span data-stu-id="7986b-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="7986b-149">Tietyn eränumeron varaaminen asiakastilausta varten</span><span class="sxs-lookup"><span data-stu-id="7986b-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="7986b-150">Kun eräseuratun nimikkeen Erä alla\[sijainti\] -varastonvaraushierarkia on määritetty sallimaan tiettyjen eränumeroiden varaaminen myyntitilauksissa, myyntitilausten käsittelijät voivat ottaa saman nimikkeen asiakastilauksia vastaan jollakin seuraavista tavoista asiakkaan pyynnöstä riippuen:</span><span class="sxs-lookup"><span data-stu-id="7986b-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="7986b-151">**Anna tilaustiedot ilman eränumeron määritystä** – Tätä menetelmää kannattaa käyttää, kun tuotteen erämääritys ei ole tärkeä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="7986b-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="7986b-152">Kaikki aiemmin luodut prosessit, jotka liittyvät tällaisen tilauksen käsittelyyn, eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="7986b-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="7986b-153">Käyttäjiltä ei vaadita lisätoimia.</span><span class="sxs-lookup"><span data-stu-id="7986b-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="7986b-154">**Anna tilaustiedot ja varaa tietty eränumero** – Tätä menetelmää kannattaa käyttää, kun asiakas pyytää tiettyä erää.</span><span class="sxs-lookup"><span data-stu-id="7986b-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="7986b-155">Yleensä asiakkaat pyytävät tiettyä erää, kun he tilaavat uudelleen aiemmin ostamaansa tuotetta.</span><span class="sxs-lookup"><span data-stu-id="7986b-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="7986b-156">Tällaista eräkohtaisia varausta kutsutaan nimellä *eräsidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="7986b-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="7986b-157">Seuraavat säännöt ovat voimassa, kun käsitellään määriä ja tietylle tilaukselle on määritetty eränumero:</span><span class="sxs-lookup"><span data-stu-id="7986b-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="7986b-158">Jotta tietyn eränumeron varaaminen nimikkeelle olisi mahdollista Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="7986b-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="7986b-159">Tähän väliin kuuluu yleensä myös rekisterikilpidimensio.</span><span class="sxs-lookup"><span data-stu-id="7986b-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="7986b-160">Sijaintidirektiivejä ei käytetä, kun keräilytyö luodaan myyntiriville, jossa käytetään tilaussidonnaista eränvarausta.</span><span class="sxs-lookup"><span data-stu-id="7986b-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="7986b-161">Tilaussidonnaisiin eriin kohdistuvan työn varastokäsittelyn aikana käyttäjä tai järjestelmä ei voi muuttaa eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="7986b-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="7986b-162">(Tämä käsittely sisältää poikkeuksen käsittelyn.)</span><span class="sxs-lookup"><span data-stu-id="7986b-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="7986b-163">Seuraavassa esimerkissä työnkulku näkyy kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="7986b-164">Esimerkkiskenaario: Eränumeron kohdistus</span><span class="sxs-lookup"><span data-stu-id="7986b-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="7986b-165">Esittelytietojen on oltava asennettuna tätä esimerkkiä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="7986b-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="7986b-166">Varastonvaraushierarkian määrittäminen sallimaan eräkohtainen varaus</span><span class="sxs-lookup"><span data-stu-id="7986b-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="7986b-167">Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="7986b-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="7986b-168">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-168">Select **New**.</span></span>
3. <span data-ttu-id="7986b-169">Anna nimi **Nimi**-kentässä (esim. **EräFlex**).</span><span class="sxs-lookup"><span data-stu-id="7986b-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="7986b-170">Anna kuvaus **Kuvaus**-kentässä (esim. **Erä joustavan alla**).</span><span class="sxs-lookup"><span data-stu-id="7986b-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="7986b-171">Valitse **Valittu**-kentässä **Sarjanumero** ja **Omistaja** ja siirrä ne sitten **Käytettävissä**-kenttään vasemman nuolipainikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="7986b-172">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7986b-172">Select **OK**.</span></span>
7. <span data-ttu-id="7986b-173">Valitse **Eränumero** -dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="7986b-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="7986b-174">Tasot **Rekisterikilpi** ja **Sijainti** valitaan automaattisesti eikä niiden valintaruutuja voi tyhjentää.</span><span class="sxs-lookup"><span data-stu-id="7986b-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="7986b-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7986b-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="7986b-176">Uuden julkaistun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="7986b-176">Create a new released product</span></span>

1. <span data-ttu-id="7986b-177">Määritä tuotteen kolme päätietoparametria käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="7986b-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="7986b-178">Valitse **Varastodimensioryhmä**-kentässä **Tavara**.</span><span class="sxs-lookup"><span data-stu-id="7986b-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="7986b-179">Valitse **Seurantadimensioryhmä**-kentässä **Erä-fyy**.</span><span class="sxs-lookup"><span data-stu-id="7986b-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="7986b-180">Valitse **Varaushierarkia** -kentässä **EräFlex**.</span><span class="sxs-lookup"><span data-stu-id="7986b-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="7986b-181">Luo kaksi eränumeroa, kuten**B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="7986b-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="7986b-182">Lisää nimekemääriä käytettävissä olevaan varastoon seuraavien arvojen avulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="7986b-183">Varasto</span><span class="sxs-lookup"><span data-stu-id="7986b-183">Warehouse</span></span> | <span data-ttu-id="7986b-184">Eränumero</span><span class="sxs-lookup"><span data-stu-id="7986b-184">Batch number</span></span> | <span data-ttu-id="7986b-185">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="7986b-185">Location</span></span> | <span data-ttu-id="7986b-186">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="7986b-186">License plate</span></span> | <span data-ttu-id="7986b-187">Määrä</span><span class="sxs-lookup"><span data-stu-id="7986b-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="7986b-188">24</span><span class="sxs-lookup"><span data-stu-id="7986b-188">24</span></span>        | <span data-ttu-id="7986b-189">B11</span><span class="sxs-lookup"><span data-stu-id="7986b-189">B11</span></span>          | <span data-ttu-id="7986b-190">BULKKI-001</span><span class="sxs-lookup"><span data-stu-id="7986b-190">BULK-001</span></span> | <span data-ttu-id="7986b-191">Ei ole</span><span class="sxs-lookup"><span data-stu-id="7986b-191">None</span></span>          | <span data-ttu-id="7986b-192">10</span><span class="sxs-lookup"><span data-stu-id="7986b-192">10</span></span>       |
    | <span data-ttu-id="7986b-193">24</span><span class="sxs-lookup"><span data-stu-id="7986b-193">24</span></span>        | <span data-ttu-id="7986b-194">B11</span><span class="sxs-lookup"><span data-stu-id="7986b-194">B11</span></span>          | <span data-ttu-id="7986b-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="7986b-195">FL-001</span></span>   | <span data-ttu-id="7986b-196">LP11</span><span class="sxs-lookup"><span data-stu-id="7986b-196">LP11</span></span>          | <span data-ttu-id="7986b-197">10</span><span class="sxs-lookup"><span data-stu-id="7986b-197">10</span></span>       |
    | <span data-ttu-id="7986b-198">24</span><span class="sxs-lookup"><span data-stu-id="7986b-198">24</span></span>        | <span data-ttu-id="7986b-199">B22</span><span class="sxs-lookup"><span data-stu-id="7986b-199">B22</span></span>          | <span data-ttu-id="7986b-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="7986b-200">FL-002</span></span>   | <span data-ttu-id="7986b-201">LP22</span><span class="sxs-lookup"><span data-stu-id="7986b-201">LP22</span></span>          | <span data-ttu-id="7986b-202">10</span><span class="sxs-lookup"><span data-stu-id="7986b-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="7986b-203">Syötä myyntitilaustiedot</span><span class="sxs-lookup"><span data-stu-id="7986b-203">Enter sales order details</span></span>

1. <span data-ttu-id="7986b-204">Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="7986b-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="7986b-205">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-205">Select **New**.</span></span>
3. <span data-ttu-id="7986b-206">Syötä myyntitilausotsikon **Asiakastili**-kenttään **US-003**.</span><span class="sxs-lookup"><span data-stu-id="7986b-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="7986b-207">Lisää rivi uutta nimikettä varten ja syötä määräksi **10**.</span><span class="sxs-lookup"><span data-stu-id="7986b-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="7986b-208">Varmista, että **Varasto**-kentän arvo on **24**.</span><span class="sxs-lookup"><span data-stu-id="7986b-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="7986b-209">Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto** ja sitten **Ylläpidä**-ryhmässä **Erävaraus**.</span><span class="sxs-lookup"><span data-stu-id="7986b-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="7986b-210">**Erävaraus**-sivulla näkyy luettelo eristä, jotka voidaan varata tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="7986b-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="7986b-211">Tässä esimerkissä määränä on **20** eränumerolle **B11** ja **10** eränumerolle **B22**.</span><span class="sxs-lookup"><span data-stu-id="7986b-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="7986b-212">Huomaa, että **Erävaraus**-sivua ei voi käyttää riviltä, jos rivin nimikkeelle on määritetty Erä alla\[sijainti\] -varaushierarkia, ellei sitä ole määritetty sallimaan eräkohtaista varausta.</span><span class="sxs-lookup"><span data-stu-id="7986b-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-213">Varataksesi ostotilaukselle tietyn erän sinun on käytettävä **Erävaraus** -sivua.</span><span class="sxs-lookup"><span data-stu-id="7986b-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="7986b-214">Jos syötät eränumeron suoraan myyntitilausriville, järjestelmä toimii siten kuin olisit syöttänyt tietyn eräarvon nimikkeelle, johon sovelletaan Erä alla\[sijainti\] -varauskäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="7986b-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="7986b-215">Kun tallennat rivin, näyttöön tulee varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="7986b-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="7986b-216">Jos vahvistat, että eränumero on määritettävä suoraan tilausrivillä, tavanomainen varastonhallintalogiikka ei käsittele kyseistä riviä.</span><span class="sxs-lookup"><span data-stu-id="7986b-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="7986b-217">Jos varaat määrän **Varaus**-sivulta, tiettyä erää ei varata ja rivin osalta sovelletaan varastotoimintojen suorittamiseen niitä sääntöjä, joita sovelletaan Erä alla\[sijainti\] -varastokäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="7986b-218">Yleensä tämä sivu toimii ja siihen sovelletaan samaa vuorovaikutusta kuin silloin, kun asianomaisille nimikkeille on määritetty Erä yllä\[sijainti\] -tyyppinen varaushierarkia.</span><span class="sxs-lookup"><span data-stu-id="7986b-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="7986b-219">Seuraavat poikkeukset kuitenkin pätevät:</span><span class="sxs-lookup"><span data-stu-id="7986b-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="7986b-220">**Lähderiville sidotut eränumerot** -pikavälilehdessä näkyvät tilausriville varatut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="7986b-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="7986b-221">Ruudukon eräarvot näkyvät koko tilausrivin toteutusjakson aikana, varaston käsittelyvaiheet mukaan luettuna.</span><span class="sxs-lookup"><span data-stu-id="7986b-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="7986b-222">**Yhteenveto**-pikavälilehdessä ruudukossa sen sijaan näkyy tavanomainen tilausrivin varaus (eli **Sijainti**-tason yläpuoleisille dimensioille tehtävä varaus) aina siihen asti, kun varastotyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="7986b-223">Tämän jälkeen rivinvaraus siirtyy työyksikölle, eikä rivinvaraus enää ole näkyvissä sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="7986b-224">**Lähderiviin sidotut eränumerot** -pikavälilehti auttaa sen varmistamisessa, että myyntitilausten käsittelijä näkee asiakkaan tilaukseen missä tahansa sen elinkaaren aikana aina laskutukseen asti sidotut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="7986b-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="7986b-225">Tietyn erän varauksen lisäksi käyttäjä voi valita erän sijainnin ja rekisterikilven manuaalisesti sen sijaan, että se antaisi järjestelmän valita ne automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7986b-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="7986b-226">Tämä ominaisuus liittyy tilaussidonnaisen erävarausmekanismin rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="7986b-227">Kuten aiemmin mainittiin, kun nimikkeelle varataan eränumero Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="7986b-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="7986b-228">Tämän vuoksi varastotyössä käytetään tilauksia käsitelleiden käyttäjien varaamia varastodimensioita, eivätkä ne aina välttämättä vastaa nimikkeen kätevää tai edes mahdollista varastointipaikkaa keräilytoimintoja varten.</span><span class="sxs-lookup"><span data-stu-id="7986b-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="7986b-229">Jos tilausten käsittelijät ovat tietoisia varaston rajoituksista, heidän saattaa kannattaa valita sijainnit ja rekisterikilvet manuaalisesti, kun he varaavat erää.</span><span class="sxs-lookup"><span data-stu-id="7986b-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="7986b-230">Tällöin käyttäjän on käytettävä **Näytä dimensiot** -toimintoa sivun otsikossa ja lisättävä sijainti ja rekisterikilpi **Yhteenveto**-pikavälilehden ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="7986b-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="7986b-231">Valitse **Erävaraus**-sivulla erän **B11** rivi ja sitten **Varaa rivi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="7986b-232">Sijaintien ja rekisterikilpien määritykselle ei ole omaa logiikkaansa automaattisen varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="7986b-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="7986b-233">Voit syöttää määrän manuaalisesti **Varaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7986b-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="7986b-234">Huomaa, että **Lähderiviin sidotut eränumerot**-pikavälilehdessä erän **B11** arvona on **Sidottu**.</span><span class="sxs-lookup"><span data-stu-id="7986b-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tietyn eränumeron sitominen myyntitilausriviin erävaraussivulla](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="7986b-236">Myyntitilausrivin määrä voidaan varata eri eristä.</span><span class="sxs-lookup"><span data-stu-id="7986b-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="7986b-237">Myös samaa erää voidaan varata useiden sijaintien ja rekisterikilpien perusteella (jos rekisterikilvet on sallittu sijainneille).</span><span class="sxs-lookup"><span data-stu-id="7986b-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="7986b-238">Tietyn erän varaaminen myyntitilausrivin määrälle voi olla myös osittaista.</span><span class="sxs-lookup"><span data-stu-id="7986b-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="7986b-239">Esimerkiksi 100 yksikön kokonaismäärä voidaan varata siten, että tietty erä on sidottu 20 yksikköön, kun taas 80 yksikköä varataan toimipaikka- ja varastotasolla mistä tahansa käytettävissä olevasta erästä.</span><span class="sxs-lookup"><span data-stu-id="7986b-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="7986b-240">Tässä tapauksessa varastonhallintajärjestelmä käsittelee keräilytoiminnot käyttäen kahta erillistä työriviä.</span><span class="sxs-lookup"><span data-stu-id="7986b-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="7986b-241">Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="7986b-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="7986b-242">Valitse nimikkeesi ja sitten **Hallitse varastoa** \> **Näytä** \> **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="7986b-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tilaussidonnainen varaus varastotapahtumatyyppinä](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="7986b-244">Tarkista nimikkeen varastotapahtumat, jotka liittyvät myyntitilausrivin varaukseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="7986b-245">Tapahtuma, jossa **Viite**-kentän arvona on **Myyntitilaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta **Sijainti**-tason yläpuolella olevien dimension osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="7986b-246">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat toimipaikka, varasto ja varastotila.</span><span class="sxs-lookup"><span data-stu-id="7986b-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="7986b-247">Tapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta määritetyn erän ja kaikkien sen yläpuolella olevien dimensioiden osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="7986b-248">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat eränumero ja sijainti.</span><span class="sxs-lookup"><span data-stu-id="7986b-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="7986b-249">Tässä esimerkissä sijainti on **Bulkki-001**.</span><span class="sxs-lookup"><span data-stu-id="7986b-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="7986b-250">Valitse myyntitilauksen otsikossa **Varasto** \> **Toiminnot** \> **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="7986b-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="7986b-251">Tilausrivi on nyt aallotettu, ja kuormitus ja työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="7986b-252">Niiden varastotöiden tarkistus ja käsittely, joilla on tilaussidonnaisia eränumeroita</span><span class="sxs-lookup"><span data-stu-id="7986b-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="7986b-253">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** \> **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="7986b-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="7986b-254">Työllä, joka käsittelee myyntitilausriviin sidottujen erämäärien keräilytoiminnon, on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="7986b-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="7986b-255">Järjestelmä käyttää työn luomisessa työmalleja, mutten sijaintidirektiivejä.</span><span class="sxs-lookup"><span data-stu-id="7986b-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="7986b-256">Kaikkia työmalleille määritettyjä vakioasetuksia, kuten keräilyrivien tai tietyn mittayksikön enimmäismäärää, käytetään sen määrittämisessä, milloin uusi työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="7986b-257">Keräilysijaintien tunnistamisen sijaintidirektiiveihin liittyviä sääntöjä ei kuitenkaan oteta huomioon, koska tilaussidonnaisessa varauksessa määritetään jo kaikki varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="7986b-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="7986b-258">Nämä varastodimensiot sisältävät varastosäilytystason dimensiot.</span><span class="sxs-lookup"><span data-stu-id="7986b-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="7986b-259">Siten työ perii kyseiset dimensiot ilman sijaintidirektiivien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="7986b-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="7986b-260">Eränumeroa ei näytetä keräilyrivillä (kuten työrivillä, joka luodaan nimikkeelle, johon liittyy Erä yllä\[sijainti\]-varaushierarkia). Sen sijaan kohteesta-eränumero ja kaikki muut varastodimensiot näkyvät työrivin työvarastotapahtumassa, joka perustuu tähän liittyviin varastotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="7986b-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Varaston varastotapahtuma töille, jotka perustuvat tilaussidonnaiseen varaukseen](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="7986b-262">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus**, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="7986b-263">Varastotapahtuma, jossa **Viite**-kentän arvona on **Työ**, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="7986b-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="7986b-264">Varastotoiminnot voivat seuraavaksi suorittaa työt tavanomaiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="7986b-265">Mobiililaitteen ohjeet kuitenkin ohjeistavat työntekijää keräilemään tiettyä eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="7986b-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="7986b-266">Varastoympäristöissä, joissa sijainteja hallitaan rekisterikilvillä, työntekijä voi keräillä mistä tahansa vielä varaamattomasta rekisterikilvestä (jota ei siis ole varattu toiselle tilaussidonnaiselle varaukselle tai työlle, joka perustuu tällaiselle varaukselle), kun hän saapuu sijainnille, jossa säilytetään samaa erää useissa rekisterikilvissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="7986b-267">Jos on epäkäytännöllistä keräillä työrivillä määritetystä sijainnista, varasto-operaattorit voivat käyttää jotakin seuraavista toiminnoista tietyn erän keräilyn siirtämiseen kätevämpään sijaintiin:</span><span class="sxs-lookup"><span data-stu-id="7986b-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="7986b-268">Vakiomuotoinen mobiililaitteen **Ohita toiminto** (jos varastotyöntekijän **Salli keräilysijainnin ohitus** -asetus on käytössä)</span><span class="sxs-lookup"><span data-stu-id="7986b-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="7986b-269">**Muuta sijaintia** -toiminto **Työluettelon tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="7986b-270">Lopeta työn keräily ja hyllytys mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="7986b-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="7986b-271">Eränumeroa **B11** on nyt kerätty määrä **10** myyntitilausriviä varten ja siirretty sijaintiin **Lastauspaikan ovi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="7986b-272">Tässä vaiheessa se on valmis lastattavaksi kuorma-autoon ja lähetettäväksi asiakkaan osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="7986b-273">Joustava rekisterikilven varaus</span><span class="sxs-lookup"><span data-stu-id="7986b-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="7986b-274">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="7986b-274">Business scenario</span></span>

<span data-ttu-id="7986b-275">Tässä skenaariossa yritys käyttää varastonhallintaa ja töiden käsittelyä ja käsittelee kuormituksen suunnittelun yksittäisten kuormalavojen/konttien tasolla Supply Chain Management -sovelluksen ulkopuolella ennen työn luomista.</span><span class="sxs-lookup"><span data-stu-id="7986b-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="7986b-276">Rekisterikilvet edustavat näitä kontteja varastodimensioissa.</span><span class="sxs-lookup"><span data-stu-id="7986b-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="7986b-277">Tämän vuoksi tietyt rekisterikilvet on määritettävä ennalta myyntitilausriveille ennen keräilytyön tekemistä.</span><span class="sxs-lookup"><span data-stu-id="7986b-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="7986b-278">Yritys toivoo joustavuutta rekisterikilpien varaussääntöjen käsittelyssä, jotta seuraava toiminta olisi mahdollista:</span><span class="sxs-lookup"><span data-stu-id="7986b-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="7986b-279">Rekisterikilpi voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="7986b-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="7986b-280">Tämä auttaa takaamaan, että suunniteltu rekisterikilpi toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="7986b-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="7986b-281">Jos rekisterikilpeä ei ole vielä määritetty myyntitilausriville, varaston henkilöstö voi valita rekisterikilven keräilyn aikana, kun myyntitilauksen rekisteröinti ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="7986b-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="7986b-282">Joustavan rekisterikilven varauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="7986b-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="7986b-283">Ennen kuin voit käyttää joustavaa rekisterikilpien varausta, kaksi ominaisuutta on otettava käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="7986b-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="7986b-284">Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="7986b-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="7986b-285">Ominaisuudet on otettava käyttöön seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="7986b-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="7986b-286">**Ominaisuuden nimi:** *Joustava varastotason dimensioiden varauskäytäntö*</span><span class="sxs-lookup"><span data-stu-id="7986b-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="7986b-287">**Ominaisuuden nimi:** *Joustava tilaussidonnainen rekisterikilven varaus*</span><span class="sxs-lookup"><span data-stu-id="7986b-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="7986b-288">Tietyn rekisterikilven varaus myyntitilauksessa</span><span class="sxs-lookup"><span data-stu-id="7986b-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="7986b-289">Jos haluat ottaa käyttöön rekisterikilven varauksen tilauksessa, valitse **Salli varaus kysyntätilauksessa** -valintaruutu **Rekisterikilpi**-tasolla **Varaston varaushierarkiat** -sivulla hierarkialle, joka on liitetty tiettyyn nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Joustavan rekisterikilven varaushierarkian Varaston varaushierarkiat -sivu](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="7986b-291">Voit ottaa rekisterikilven varauksen käyttöön tilauksessa missä tahansa käyttöönoton vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="7986b-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="7986b-292">Tämä muutos ei vaikuta varauksiin tai avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="7986b-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="7986b-293">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos avointen lähtevien varastotapahtumien varasto-ottotyyppi on *Tilauksessa*, *Varattu tilattu* tai *Varattu fyysinen* on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="7986b-294">Vaikka **Salli varaus kysyntätilauksessa** -valintaruutu olisi valittu **Rekisterikilpi**-tasolla, tilauksen tietyn rekisterikilven varaaminen *ei* silti ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="7986b-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="7986b-295">Tässä tapauksessa käytetään varaushierarkian oletusvarastotoimintojen logiikkaa.</span><span class="sxs-lookup"><span data-stu-id="7986b-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="7986b-296">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) -protokollaa. Sovelluksessa tämä varaus tehdään suoraan myyntitilauksesta käyttämällä **Tilaussidonnaisia varauksia rekisterikilpeä kohti** -asetusta **Avaa Excelissä** -komennolla.</span><span class="sxs-lookup"><span data-stu-id="7986b-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="7986b-297">Excel-lisäosassa avattaviin entiteettitietoihin on annettava seuraavat varaukseen liittyvät tiedot ja valittava sitten **Julkaise**, jotta tiedot lähetetään takaisin Supply Chain Management -sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="7986b-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="7986b-298">Viite (vain *Myyntitilaus*-arvoa tuetaan).</span><span class="sxs-lookup"><span data-stu-id="7986b-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="7986b-299">Tilausnumero (arvo voidaan johtaa erästä).</span><span class="sxs-lookup"><span data-stu-id="7986b-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="7986b-300">Erätunnus</span><span class="sxs-lookup"><span data-stu-id="7986b-300">Lot ID</span></span>
- <span data-ttu-id="7986b-301">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="7986b-301">License plate</span></span>
- <span data-ttu-id="7986b-302">Määrä</span><span class="sxs-lookup"><span data-stu-id="7986b-302">Quantity</span></span>

<span data-ttu-id="7986b-303">Jos sinun on varattava tietty eräseuratun nimikkeen rekisterikilpi, käytä **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="7986b-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="7986b-304">Kun varaston toiminnot ovat käsitelleet tilaussidonnaista rekisterikilven varausta käyttävän myyntitilausrivin, sijaintidirektiivejä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="7986b-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="7986b-305">Jos varaston työnimike sisältää rivejä, jotka vastaavat kokonaista lavaa ja joilla on rekisterikilpisidonnaisia määriä, voit optimoida keräysprosessin käyttämällä mobiililaitteen valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -vaihtoehdon arvoksi on määritetyt *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="7986b-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="7986b-306">Varastotyöntekijä voi sitten skannata rekisterikilven ja viimeistellä keräilyn sen sijaan, että työn nimikkeet skannattaisiin yksitellen.</span><span class="sxs-lookup"><span data-stu-id="7986b-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Mobiililaitteen valikon vaihtoehto, jossa Käsittele rekisterikilven mukaan -asetuksen arvoksi on määritetty Kyllä](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="7986b-308">Koska **Käsittele rekisterikilven mukaan** -toiminto ei tue työtä, joka koskee useita lavoja, eri rekisterikilville on paras olla erilliset työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="7986b-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="7986b-309">Jos haluat käyttää tätä menetelmää, lisää **Tilaussidonnaisen rekisterikilven tunnus** -kenttää työn otsikon katkaisuna **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="7986b-310">Esimerkkiskenaario: Tilaussidonnaisen rekisterikilven varauksen määrittäminen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="7986b-310">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="7986b-311">Tässä skenaariossa esitetään, miten tilaussidonnaisen rekisterikilven varaus määritetään ja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="7986b-311">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="7986b-312">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="7986b-312">Make demo data available</span></span>

<span data-ttu-id="7986b-313">Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Supply Chain Management -sovelluksen vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="7986b-313">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="7986b-314">Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, varmista, että käytät ympäristöä, johon on asennettu esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="7986b-314">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="7986b-315">Sinun on myös määritettävä yritykseksi **USMF**, ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="7986b-315">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="7986b-316">Luo varaston varaushierarkia, joka mahdollistaa rekisterikilven varauksen</span><span class="sxs-lookup"><span data-stu-id="7986b-316">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="7986b-317">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="7986b-317">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="7986b-318">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-318">Select **New**.</span></span>
1. <span data-ttu-id="7986b-319">Anna nimi **Nimi**-kenttään arvo (esimerkiksi *JoustavaRK*).</span><span class="sxs-lookup"><span data-stu-id="7986b-319">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="7986b-320">Anna kuvaus **Kuvaus**-kenttään arvo (esim. *Joustavan RK:n varaus*).</span><span class="sxs-lookup"><span data-stu-id="7986b-320">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="7986b-321">Valitse **Valittu**-luettelossa **Eränumero**, **Sarjanumero** ja **Omistaja**.</span><span class="sxs-lookup"><span data-stu-id="7986b-321">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="7986b-322">Valitse **Poista**-painike ![taaksepäin osoittava nuoli](media/backward-button.png), jos haluat siirtää valitut tietueet **käytettävissä olevien** luetteloon.</span><span class="sxs-lookup"><span data-stu-id="7986b-322">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="7986b-323">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7986b-323">Select **OK**.</span></span>
1. <span data-ttu-id="7986b-324">Valitse **Rekisterikilpi**-dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="7986b-324">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="7986b-325">**Sijainti**-taso valitaan automaattisesti, etkä voi tyhjentää sen valintaruutua.</span><span class="sxs-lookup"><span data-stu-id="7986b-325">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="7986b-326">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7986b-326">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="7986b-327">Kahden vapautetun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="7986b-327">Create two released products</span></span>

1. <span data-ttu-id="7986b-328">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="7986b-328">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7986b-329">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-329">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7986b-330">Aseta **Uusi vapautettu tuote** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7986b-330">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7986b-331">**Tuotenumero:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="7986b-331">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="7986b-332">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="7986b-332">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="7986b-333">**Nimikemalliryhmä:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="7986b-333">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="7986b-334">**Nimikeryhmä:** *Ääni*</span><span class="sxs-lookup"><span data-stu-id="7986b-334">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="7986b-335">**Varastodimensioryhmä:** *Kauppatavara*</span><span class="sxs-lookup"><span data-stu-id="7986b-335">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="7986b-336">**Seurantadimensioryhmä:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="7986b-336">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="7986b-337">**Varaushierarkia:** *JoustavaRK*</span><span class="sxs-lookup"><span data-stu-id="7986b-337">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="7986b-338">Valitse **OK** luodaksesi tuotteen. Sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="7986b-338">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="7986b-339">Uusi tuote avataan.</span><span class="sxs-lookup"><span data-stu-id="7986b-339">The new product is opened.</span></span> <span data-ttu-id="7986b-340">Määritä **Varasto**-pikavälilehden **Yksikön sarjaryhmän tunnus** -kenttään *kpl*.</span><span class="sxs-lookup"><span data-stu-id="7986b-340">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="7986b-341">Toista edelliset vaiheet ja luo toinen tuote, jolla on samat asetukset. Määritä kuitenkin **Tuotenumero**- ja **Nimiketunnus**-kenttien arvoksi *Nimike2*.</span><span class="sxs-lookup"><span data-stu-id="7986b-341">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="7986b-342">Valitse toimintoruudun **Varastonhallinta**-välilehden **Näytä**-ryhmässä **Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="7986b-342">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="7986b-343">Valitse sitten **Määrän oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="7986b-343">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="7986b-344">Oikaise uusien nimikkeiden käytettävissä olevaa varastoa seuravan taulukon mukaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-344">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="7986b-345">Kohde</span><span class="sxs-lookup"><span data-stu-id="7986b-345">Item</span></span>  | <span data-ttu-id="7986b-346">Varasto</span><span class="sxs-lookup"><span data-stu-id="7986b-346">Warehouse</span></span> | <span data-ttu-id="7986b-347">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="7986b-347">Location</span></span> | <span data-ttu-id="7986b-348">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="7986b-348">License plate</span></span> | <span data-ttu-id="7986b-349">Määrä</span><span class="sxs-lookup"><span data-stu-id="7986b-349">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="7986b-350">Nimike1</span><span class="sxs-lookup"><span data-stu-id="7986b-350">Item1</span></span> | <span data-ttu-id="7986b-351">24</span><span class="sxs-lookup"><span data-stu-id="7986b-351">24</span></span>        | <span data-ttu-id="7986b-352">FL-010</span><span class="sxs-lookup"><span data-stu-id="7986b-352">FL-010</span></span>   | <span data-ttu-id="7986b-353">RK01</span><span class="sxs-lookup"><span data-stu-id="7986b-353">LP01</span></span>          | <span data-ttu-id="7986b-354">10</span><span class="sxs-lookup"><span data-stu-id="7986b-354">10</span></span>       |
    | <span data-ttu-id="7986b-355">Nimike1</span><span class="sxs-lookup"><span data-stu-id="7986b-355">Item1</span></span> | <span data-ttu-id="7986b-356">24</span><span class="sxs-lookup"><span data-stu-id="7986b-356">24</span></span>        | <span data-ttu-id="7986b-357">FL-011</span><span class="sxs-lookup"><span data-stu-id="7986b-357">FL-011</span></span>   | <span data-ttu-id="7986b-358">RK02</span><span class="sxs-lookup"><span data-stu-id="7986b-358">LP02</span></span>          | <span data-ttu-id="7986b-359">10</span><span class="sxs-lookup"><span data-stu-id="7986b-359">10</span></span>       |
    | <span data-ttu-id="7986b-360">Nimike2</span><span class="sxs-lookup"><span data-stu-id="7986b-360">Item2</span></span> | <span data-ttu-id="7986b-361">24</span><span class="sxs-lookup"><span data-stu-id="7986b-361">24</span></span>        | <span data-ttu-id="7986b-362">FL-010</span><span class="sxs-lookup"><span data-stu-id="7986b-362">FL-010</span></span>   | <span data-ttu-id="7986b-363">RK01</span><span class="sxs-lookup"><span data-stu-id="7986b-363">LP01</span></span>          | <span data-ttu-id="7986b-364">5</span><span class="sxs-lookup"><span data-stu-id="7986b-364">5</span></span>        |
    | <span data-ttu-id="7986b-365">Nimike2</span><span class="sxs-lookup"><span data-stu-id="7986b-365">Item2</span></span> | <span data-ttu-id="7986b-366">24</span><span class="sxs-lookup"><span data-stu-id="7986b-366">24</span></span>        | <span data-ttu-id="7986b-367">FL-011</span><span class="sxs-lookup"><span data-stu-id="7986b-367">FL-011</span></span>   | <span data-ttu-id="7986b-368">RK02</span><span class="sxs-lookup"><span data-stu-id="7986b-368">LP02</span></span>          | <span data-ttu-id="7986b-369">5</span><span class="sxs-lookup"><span data-stu-id="7986b-369">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="7986b-370">Sinun on luotava kaksi rekisterikilpeä ja käytettävä sijainteja, joissa sallitaan yhdistetyt nimikkeet, kuten *FL-010* ja *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="7986b-370">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="7986b-371">Myyntitilauksen luominen ja tietyn rekisterikilven varaaminen</span><span class="sxs-lookup"><span data-stu-id="7986b-371">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="7986b-372">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="7986b-372">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7986b-373">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7986b-373">Select **New**.</span></span>
1. <span data-ttu-id="7986b-374">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7986b-374">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7986b-375">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7986b-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7986b-376">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="7986b-376">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="7986b-377">Valitse **OK** ja sulje **Luo myyntitilaus** -valintaikkuna. Avaa sitten uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="7986b-377">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="7986b-378">Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="7986b-378">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="7986b-379">**Nimiketunnus:** *Nimike1*</span><span class="sxs-lookup"><span data-stu-id="7986b-379">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="7986b-380">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="7986b-380">**Quantity:** *10*</span></span>

1. <span data-ttu-id="7986b-381">Lisää toinen myyntitilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="7986b-381">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="7986b-382">**Nimiketunnus:** *Nimike2*</span><span class="sxs-lookup"><span data-stu-id="7986b-382">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="7986b-383">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="7986b-383">**Quantity:** *5*</span></span>

1. <span data-ttu-id="7986b-384">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7986b-384">Select **Save**.</span></span>
1. <span data-ttu-id="7986b-385">Anna **Rivin tiedot** -pikavälilehdessä **Asetukset**-välilehdessä **Erätunnus**-arvo jokaiselle riville.</span><span class="sxs-lookup"><span data-stu-id="7986b-385">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="7986b-386">Nämä arvot ovat pakollisia tiettyjen rekisterikilpien varauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-386">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-387">Jos haluat varata tietyn rekisterikilven, sinun on käytettävä **tilaussidonnaisia varauksia rekisterikilpeä kohti** -tietoyksikköä.</span><span class="sxs-lookup"><span data-stu-id="7986b-387">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="7986b-388">Jos sinun on varattava tietyn rekisterikilven eräseurattu nimike, voit käyttää myös **Erän varaus** -sivua, kuten [Anna myyntitilauksen tiedot](#sales-order-details) -osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="7986b-388">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="7986b-389">Jos annat rekisterikilven suoraan myyntitilausriville ja vahvistat sen järjestelmässä, rivillä ei käytetä varastonhallinnan käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="7986b-389">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="7986b-390">Valitse **Avaa Microsoft Officessa**, valitse **Tilaussidonnaiset varaukset rekisterikilpeä kohti** ja lataa tiedosto.</span><span class="sxs-lookup"><span data-stu-id="7986b-390">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="7986b-391">Avaa ladattu tiedosto Excelissä ja valitse **Ota muokkaus käyttöön** -painike, jotta voit ajaa Excel-lisäosan.</span><span class="sxs-lookup"><span data-stu-id="7986b-391">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="7986b-392">Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan**.</span><span class="sxs-lookup"><span data-stu-id="7986b-392">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="7986b-393">Jos näet kirjautumisruudun, valitse **Kirjaudu sisään** samoilla tunnuksilla, joilla kirjaudut Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-393">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="7986b-394">Jos haluat varata nimikkeen tietystä rekisterikilvestä, valitse Excelin lisäosassa **Uusi** ja lisää varausrivi. Määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7986b-394">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="7986b-395">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike1*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="7986b-395">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="7986b-396">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="7986b-396">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="7986b-397">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="7986b-397">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="7986b-398">Lisää toinen varausrivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7986b-398">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="7986b-399">**Erätunnus:** Anna **Erätunnus**-arvo, joka on myyntitilausrivillä *Nimike2*-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="7986b-399">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="7986b-400">**Rekisterikilpi:** *RK02*</span><span class="sxs-lookup"><span data-stu-id="7986b-400">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="7986b-401">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="7986b-401">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="7986b-402">Valitse Excelin lisäosassa **Julkaise** ja lähetä tiedot takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-402">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-403">Varausrivi tulee näkyviin järjestelmään vain, jos julkaisemisessa ei ole tehty virheitä.</span><span class="sxs-lookup"><span data-stu-id="7986b-403">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="7986b-404">Siirry takaisin Supply Chain Management -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="7986b-404">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="7986b-405">Voit tarkistaa nimikkeen varauksen **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Ylläpidä \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="7986b-405">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="7986b-406">Ota huomioon, että *Nimike1* -kohdan myyntitilausrivillä varataan varastoa *10* ja *Nimike2*-kohdan myyntitilausrivillä varataan varastoa *5*.</span><span class="sxs-lookup"><span data-stu-id="7986b-406">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="7986b-407">Voit tarkastella varastotapahtumia, jotka liittyvät myyntitilausrivin varaukseen, **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa valitsemalla **Näytä \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="7986b-407">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="7986b-408">Huomaa, että varaukseen liittyy kaksi tapahtumaa. Toisen **Viite**-kentän arvoksi on määritetty *Myyntitilaus* ja toisen **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="7986b-408">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-409">Tapahtuma, jossa **Viite**-kentän arvoksi on määritetty *Myyntitilaus*, edustaa tilausrivin varausta varastodimensioissa, jotka ovat yli **Sijainti**-tason (toimipaikka, varasto ja varaston tila).</span><span class="sxs-lookup"><span data-stu-id="7986b-409">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="7986b-410">Tapahtuma, jonka **Viite**-kentän arvoksi on määritetty *Tilaussidonnainen varaus*, vastaa tietyn rekisterikilven ja sijainnin tilausrivin varausta.</span><span class="sxs-lookup"><span data-stu-id="7986b-410">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="7986b-411">Jos haluat vapauttaa myyntitilauksen, valitse toimintoruudun **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="7986b-411">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="7986b-412">Varaston työn tarkistaminen ja käsitteleminen määritettyjen tilaussidonnaisten rekisterikilpien avulla</span><span class="sxs-lookup"><span data-stu-id="7986b-412">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="7986b-413">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="7986b-413">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="7986b-414">Kun varaus on tehty tietylle erälle, järjestelmä ei käytä sijaintidirektiivejä, kun rekisterikilven varausta käyttävälle myyntitilaukselle luodaan työ.</span><span class="sxs-lookup"><span data-stu-id="7986b-414">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="7986b-415">Koska tilaussidonnainen varaus määrittää kaikki varastodimensiot, mukaan lukien sijainnin, sijaintidirektiivejä ei tarvitse käyttää, koska nämä varastodimensiot on juuri syötetty työhön.</span><span class="sxs-lookup"><span data-stu-id="7986b-415">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="7986b-416">Ne näkyvät **Varastodimensioista**-osassa **Työn varastotapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-416">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-417">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on *Tilaussidonnainen varaus*, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-417">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="7986b-418">Varastotapahtuma, jossa **Viite**-kentän arvona on *Työ*, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="7986b-418">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="7986b-419">Tee työn keräily ja hyllytys valmiiksi mobiililaitteessa käyttämällä valikon vaihtoehtoa, jossa **Käsittele rekisterikilven mukaan** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="7986b-419">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7986b-420">**Käsittele rekisterikilven mukaan** -toiminto auttaa koko rekisterikilven käsittelemisessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-420">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="7986b-421">Jos sinun on käsiteltävä rekisterikilven osa, et voi käyttää tätä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="7986b-421">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="7986b-422">On suositeltavaa, että kustakin rekisterikilvestä luodaan erilliset työt.</span><span class="sxs-lookup"><span data-stu-id="7986b-422">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="7986b-423">Voit saavuttaa tämän tuloksen käyttämällä **Työn otsikoiden katkaisut** -ominaisuutta **Työmalli**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-423">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="7986b-424">Rekisterikilpi *RK02* on nyt kerätty myyntitilausriveille ja hyllytetty *Lastausovi*-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="7986b-424">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="7986b-425">Tässä vaiheessa se on valmis lastattavaksi ja lähetettäväksi asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="7986b-425">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="7986b-426">Niiden varastotöiden poikkeustenkäsittely, joilla on tilaussidonnaiset eränumerot</span><span class="sxs-lookup"><span data-stu-id="7986b-426">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="7986b-427">Tilaussidonnaisten eränumeroiden keräilyn varastotyöhön sovelletaan samoja varaston poikkeustenkäsittelyä ja -toimintoja kuin tavanomaiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="7986b-427">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="7986b-428">Yleisesi ottaen avoin työ tai työrivi voidaan peruuttaa, se voidaan keskeyttää, koska käyttäjän sijainti on täynnä, siihen voidaan soveltaa lyhyttä keräilyä ja sitä voidaan päivittää siirron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="7986b-428">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="7986b-429">Samoin jo valmiiksi saatua keräiltyä työmäärää voidaan vähentää tai työ voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="7986b-429">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="7986b-430">Kaikkiin näihin poikkeusten käsittelyn toimintoihin sovelletaan seuraavaa keskeistä sääntöä: asiakkaalle varattua eränumeroa ei voi koskaan korvata toisella eränumerolla, mutta sen varastodimensioita (sijainti ja rekisterikilpi) voi muuttaa joko käyttäjän manuaalisella päivityksellä tai järjestelmän automaattisella päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="7986b-430">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="7986b-431">Automaattinen päivitys perustuu samaan varastodimensioiden satunnaiseen määrittämiseen, jota käytetään, kun tietty erä varataan automaattisesti mutta varastodimensioita ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="7986b-431">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="7986b-432">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="7986b-432">Example scenario</span></span>

<span data-ttu-id="7986b-433">Esimerkki tästä skenaariosta on tilanne, jossa aiemmin valmistuneiden töiden keräily perutaan **Vähennä keräiltyä määrää** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="7986b-433">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="7986b-434">Tässä esimerkissä oletetaan, että olet jo tehnyt [Esimerkkiskenaario: Eränumeron kohdistus](#Example-batch-allocation) -kohdassa kerrotut vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7986b-434">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="7986b-435">Se jatkuu kyseisestä esimerkistä.</span><span class="sxs-lookup"><span data-stu-id="7986b-435">It continues from that example.</span></span>

1. <span data-ttu-id="7986b-436">Siirry kohtaan **Varastonhallinta** \> **Kuormat** \> **Aktiiviset kuormat**.</span><span class="sxs-lookup"><span data-stu-id="7986b-436">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="7986b-437">Valitse kuorma, joka on luotu myyntitilauksen lähetyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-437">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="7986b-438">Valitse **Kuormatilauksen rivit** -pikavälilehdestä **Vähennä keräiltyä määrää**.</span><span class="sxs-lookup"><span data-stu-id="7986b-438">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="7986b-439">Valitse **Vähennä keräiltyä määrää** -sivun **Siirrä sijaintiin** -kentässä **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="7986b-439">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="7986b-440">Valitse **Siirrä rekisterikilvelle**-kentässä **LP33**.</span><span class="sxs-lookup"><span data-stu-id="7986b-440">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="7986b-441">Syötä **Peruttava keräilty varastomäärä** -kenttään arvo **10**.</span><span class="sxs-lookup"><span data-stu-id="7986b-441">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="7986b-442">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7986b-442">Select **OK**.</span></span>

<span data-ttu-id="7986b-443">Tässä ovat keräilyn perumisen tulokset:</span><span class="sxs-lookup"><span data-stu-id="7986b-443">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="7986b-444">Aiemmin suljetun työn tilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="7986b-444">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="7986b-445">Uusi **Varastonsiirto**-tyypin työ luodaan varastomäärälle **10** eränumerossa **B11**.</span><span class="sxs-lookup"><span data-stu-id="7986b-445">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="7986b-446">Tämä työ edustaa siirtoa sijainnista **Lastauspaikan ovi** rekisterikilvelle **LP33** sijainnissa **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="7986b-446">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="7986b-447">Tilaksi määritetään **Suljettu**.</span><span class="sxs-lookup"><span data-stu-id="7986b-447">The status is set to **Closed**.</span></span>
- <span data-ttu-id="7986b-448">Järjestelmä varaa uudelleen alun perin tilatun eränumeron ja määrittää sijainnin ja rekisterikilpitunnukset.</span><span class="sxs-lookup"><span data-stu-id="7986b-448">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="7986b-449">(Tämä prosessi vastaa **Vara rivi** -toiminnon suorittamista tietyn eränumeron tilausriville).</span><span class="sxs-lookup"><span data-stu-id="7986b-449">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="7986b-450">Tämän tuloksena erä **B11** näkyy sidottuna **Lähderiville sidotut eränumerot** -pikavälilehdessä sivulla **Erävaraus** ja **Varaus**-kentässä on määrä **10** eränumeron **B11** osalta.</span><span class="sxs-lookup"><span data-stu-id="7986b-450">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="7986b-451">Lisäksi **Sijainti**-kentän arvona on **FL-001** ja **Rekisterikilpi**-kentän arvona on **LP11**.</span><span class="sxs-lookup"><span data-stu-id="7986b-451">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="7986b-452">(Voit lisätä nämä kentät ruudukkoon, jos ne eivät ole näkyvissä.)</span><span class="sxs-lookup"><span data-stu-id="7986b-452">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="7986b-453">Seuraavissa taulukoissa on yhteenveto siitä, miten järjestelmä käsittelee tiettyjen varastotoimintojen tilaussidonnaisen erävarauksen.</span><span class="sxs-lookup"><span data-stu-id="7986b-453">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="7986b-454">Taulukkojen sisältöä tulkitaan olettamalla, että kukin varastotoiminnon suorittamiseen liittyy olemassa oleva tilaussidonnaiseen erävaraukseen perustuvaa työ tai että kunkin varastotoiminnon suorittaminen vaikuttaa kyseisentyyppiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="7986b-454">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="7986b-455">Näissä taulukoissa Erämäärä on käytettävissä -sarake ilmaisee, onko varastomäärää käytettävissä sen määrän lisäksi, joka on jo varattu kulloisillekin tilaussidonnaisille varauksille tai joka on varattu kyseisentyyppisiin varauksiin perustuvassa varastotyössä.</span><span class="sxs-lookup"><span data-stu-id="7986b-455">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="7986b-456">Avoimen työn keräilysijainnin ohitus</span><span class="sxs-lookup"><span data-stu-id="7986b-456">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-457">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-457">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-458">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-458">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-459">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-459">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-460">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-460">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-461">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-461">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-462"><strong>Salli keräilysijainnin ohitus</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="7986b-462">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="7986b-463">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-463">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-464">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastointisovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="7986b-464">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="7986b-465">Valitse <strong>Ehdota</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-465">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="7986b-466">Vahvista uusi sijainti, jota ehdotetaan erämäärän käytettävyyden perusteella.</span><span class="sxs-lookup"><span data-stu-id="7986b-466">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-467">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="7986b-467">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="7986b-468">Keräilyrivin sijainniksi päivittyy uusi sijainti.</span><span class="sxs-lookup"><span data-stu-id="7986b-468">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="7986b-469">(Jos sijainti on rekisterikilpihallittu, työvarastotapahtumalle määritetään satunnainen rekisterikilpi ja työntekijä voi keräillä mistä tahansa rekisterikilvestä, jossa määrää on käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="7986b-469">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="7986b-470">Jos määrää on uuden sijainnin useassa rekisterikilvessä, alkuperäinen keräilyrivi jaetaan useaan riviin, jotka vastaavat kutakin rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="7986b-470">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-471">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-471">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-472">Nro</span><span class="sxs-lookup"><span data-stu-id="7986b-472">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-473">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varastointisovelluksessa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="7986b-473">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="7986b-474">Määritä sijainti manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7986b-474">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-475"><strong>Ohita sijainti</strong> -toiminto ei ole mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="7986b-475">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="7986b-476">Se epäonnistuu, ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="7986b-476">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="7986b-477">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-477">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="7986b-478">Täysi-painike – Työrivin jakaminen käyttäjän sijainnin ylivuodon vuoksi</span><span class="sxs-lookup"><span data-stu-id="7986b-478">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-479">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-479">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-480">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-480">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-481">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-481">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-482">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-482">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-483">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-483">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7986b-484"><strong>Salli työn jakaminen</strong> -asetus on käytössä mobiililaitteen valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="7986b-484">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="7986b-485">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-485">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-486">Valitse valikkovaihtoehto <strong>Täysi</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-486">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="7986b-487">Syötä <strong>Keräilymäärä</strong>-kenttään tarvittavan keräilyn osamäärä ilmaisemaan täyttä kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="7986b-487">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-488">Kulloisessakin työssä määrä päivitetään vastaamaan jäljellä olevaa keräiltävää määrää.</span><span class="sxs-lookup"><span data-stu-id="7986b-488">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="7986b-489">Keräillylle määrälle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-489">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="7986b-490">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-490">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="7986b-491">Valmiin työn keräillyn määrän vähentäminen (kuormasta)</span><span class="sxs-lookup"><span data-stu-id="7986b-491">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-492">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-492">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-493">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-493">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-494">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-494">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-495">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-495">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-496">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-496">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-497">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-497">Not applicable</span></span></td>
<td><span data-ttu-id="7986b-498">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-498">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-499">Avaa <strong>Vähennä keräiltyä määrää</strong> -sivu kuormariviltä.</span><span class="sxs-lookup"><span data-stu-id="7986b-499">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="7986b-500">Syötä sen määrän kokonaisarvo, jonka keräily perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-500">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="7986b-501">Valitse "siirto kohteeseen" sijainti/rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="7986b-501">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="7986b-502">Kuormariviin liittyvä työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-502">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="7986b-503">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-503">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-504">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-504">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-505">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-505">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-506">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-506">No</span></span></td>
<td><span data-ttu-id="7986b-507">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-507">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-508">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-508">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-509">Määrä varataan uudelleen samalle erälle ja samalle sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu), jotka on syötetty keräilyn perumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-509">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="7986b-510">Nimikkeen siirtäminen varastossa</span><span class="sxs-lookup"><span data-stu-id="7986b-510">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="7986b-511">Tätä varastotoimintoa voidaan soveltaa vain **Työnluontiprosessi**-tyypin siirtoihin, ei mallin mukaiseen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="7986b-511">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-512">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-512">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-513">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-513">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-514">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-514">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-515">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-515">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-516">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-516">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-517"><strong>Salli työhön liitetyn varaston siirto</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="7986b-517">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="7986b-518">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-518">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-519">Aloita siirto varastointisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="7986b-519">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="7986b-520">Anna kohteesta- ja kohteeseen-sijainnit.</span><span class="sxs-lookup"><span data-stu-id="7986b-520">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="7986b-521">Kaikissa olemassa olevissa töissä, joihin siirto vaikuttaa, keräilysijainniksi päivitetään uusi kohteeseen-sijainti.</span><span class="sxs-lookup"><span data-stu-id="7986b-521">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="7986b-522">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-522">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-523">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-523">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-524">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-524">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-525">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-525">No</span></span></td>
<td><span data-ttu-id="7986b-526">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-526">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-527">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-527">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-528">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle ja uudelle kohteeseen-sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="7986b-528">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="7986b-529">Valmiin työn keräillyn määrän palauttaminen (kuormasta tai aallosta)</span><span class="sxs-lookup"><span data-stu-id="7986b-529">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-530">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-530">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-531">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-531">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-532">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-532">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-533">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-533">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-534">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-534">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="7986b-535">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-535">Not applicable</span></span></td>
<td><span data-ttu-id="7986b-536">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-536">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-537">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="7986b-537">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="7986b-538">Valitse pyyntösivulla vaihtoehto <strong>Jätä nimikkeet nykyiseen sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-538">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-539">Kaikki tähän Kuormariviin liittyvät työt perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-539">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="7986b-540">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-540">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-541">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-541">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-542">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-542">No</span></span></td>
<td><span data-ttu-id="7986b-543">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-543">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-544">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-544">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-545">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä jätettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-545">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-546">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-546">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-547">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="7986b-547">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="7986b-548">Valitse pyyntösivulla vaihtoehto <strong>Osoita nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-548">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-549">Nykyinen työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-549">The current work is canceled.</span></span></li>
<li><span data-ttu-id="7986b-550">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-550">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-551">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-551">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-552">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-552">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-553">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-553">No</span></span></td>
<td><span data-ttu-id="7986b-554">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-554">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-555">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-555">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-556">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä osoitettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-556">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-557">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="7986b-557">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-558">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="7986b-558">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="7986b-559">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-559">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-560">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="7986b-560">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="7986b-561">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-561">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-562">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="7986b-562">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-563">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="7986b-563">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="7986b-564">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet sijaintidirektiivien perusteella</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-564">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-565">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="7986b-565">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="7986b-566">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-566">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="7986b-567">Määrän lyhytkeräily – Rekisteröi määrä fyysisesti löytymättömäksi sijainnista/rekisterikilvestä, kun keräilytyötä suoritetaan</span><span class="sxs-lookup"><span data-stu-id="7986b-567">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-568">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-568">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-569">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-569">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-570">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-570">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-571">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-571">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-572">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-572">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-573">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-573">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="7986b-574">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-574">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-575">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-575">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-576">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-576">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-577">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-577">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-578">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-578">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="7986b-579"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="7986b-579">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-580">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-580">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-581">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-581">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-582">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-582">No</span></span></td>
<td><span data-ttu-id="7986b-583">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-583">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7986b-584">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="7986b-584">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="7986b-585">Olemassa oleva työ pysyy avoimena.</span><span class="sxs-lookup"><span data-stu-id="7986b-585">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-586">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-586">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-587">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-587">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="7986b-588">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-588">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-589">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-589">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-590">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-590">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-591">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-591">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-592">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-592">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="7986b-593"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="7986b-593">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-594">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-594">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-595">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-595">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-596">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-596">No</span></span></td>
<td><span data-ttu-id="7986b-597">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-597">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-598">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-598">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-599">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-599">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-600">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei/Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-600">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="7986b-601">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="7986b-601">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="7986b-602">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-602">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-603">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-603">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-604">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-604">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-605">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-605">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="7986b-606">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7986b-606">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-607">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="7986b-607">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="7986b-608">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-608">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="7986b-609">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-609">The put line is canceled.</span></span></li>
<li><span data-ttu-id="7986b-610">Uusi keräilyrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-610">A new pick line is created.</span></span> <span data-ttu-id="7986b-611">Siinä käytetään käyttäjän valitsemaa sijaintia/rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="7986b-611">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="7986b-612">Uusi hyllytysrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-612">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7986b-613"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="7986b-613">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-614">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-614">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-615">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-615">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="7986b-616">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="7986b-616">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="7986b-617">Nro</span><span class="sxs-lookup"><span data-stu-id="7986b-617">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-618">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-618">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-619">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-619">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-620">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-620">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-621">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="7986b-621">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="7986b-622">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-622">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-623">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-623">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="7986b-624">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="7986b-624">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="7986b-625">Nro</span><span class="sxs-lookup"><span data-stu-id="7986b-625">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-626">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-626">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-627">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-627">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-628">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-628">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="7986b-629">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7986b-629">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="7986b-630">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="7986b-630">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="7986b-631">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-631">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="7986b-632">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-632">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7986b-633"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="7986b-633">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="7986b-634">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin/rekisterikilven määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-634">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-635">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Automaattinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä/Ei</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä/Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-635">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="7986b-636">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-636">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-637">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varastointisovelluksessa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="7986b-637">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="7986b-638">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="7986b-638">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="7986b-639">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja automaattinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-639">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-640">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="7986b-640">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="7986b-641">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="7986b-641">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="7986b-642">Muuta varaston tilaa</span><span class="sxs-lookup"><span data-stu-id="7986b-642">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="7986b-643">Tämä varastotoiminto voidaan suorittaa useista aloituskohdista.</span><span class="sxs-lookup"><span data-stu-id="7986b-643">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="7986b-644">Tässä näkyvässä esimerkissä käytetään **Varaston tilanmuutos** -toimintoa **Käytettävissä sijainnin mukaan** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7986b-644">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7986b-645">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="7986b-645">Key setup parameter</span></span></th>
<th><span data-ttu-id="7986b-646">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="7986b-646">Batch quantity is available</span></span></th>
<th><span data-ttu-id="7986b-647">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="7986b-647">Key user steps</span></span></th>
<th><span data-ttu-id="7986b-648">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="7986b-648">Warehouse work</span></span></th>
<th><span data-ttu-id="7986b-649">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="7986b-649">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-650"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Varaukset</strong> tai <strong>Merkinnät ja varaukset</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-650">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="7986b-651">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-651">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-652">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="7986b-652">Select a specific location.</span></span></li>
<li><span data-ttu-id="7986b-653">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="7986b-653">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="7986b-654">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-654">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="7986b-655">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-655">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-656">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="7986b-656">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7986b-657">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-657">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-658">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-658">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="7986b-659">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="7986b-659">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="7986b-660"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="7986b-660">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7986b-661">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-661">No</span></span></td>
<td><span data-ttu-id="7986b-662">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-662">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-663">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="7986b-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="7986b-664">Varaus poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7986b-664">The reservation is removed.</span></span></li>
<li><span data-ttu-id="7986b-665">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="7986b-665">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="7986b-666"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="7986b-666">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="7986b-667"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Ei mitään</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-667">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="7986b-668">Kyllä</span><span class="sxs-lookup"><span data-stu-id="7986b-668">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="7986b-669">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="7986b-669">Select a specific location.</span></span></li>
<li><span data-ttu-id="7986b-670">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="7986b-670">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="7986b-671">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-671">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="7986b-672">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="7986b-672">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="7986b-673">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="7986b-673">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="7986b-674">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="7986b-674">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="7986b-675">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7986b-675">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7986b-676">Ei</span><span class="sxs-lookup"><span data-stu-id="7986b-676">No</span></span></td>
<td><span data-ttu-id="7986b-677">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="7986b-677">See the previous row.</span></span></td>
<td><span data-ttu-id="7986b-678">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="7986b-678">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="7986b-679">Varastotilan muutokset eivät ole sallittuja.</span><span class="sxs-lookup"><span data-stu-id="7986b-679">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="7986b-680">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="7986b-680">Limitations</span></span>

- <span data-ttu-id="7986b-681">Joustava varastotason dimensionvaraustoiminto ei tue seuraavia ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="7986b-681">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="7986b-682">Todellisen painon hallinta</span><span class="sxs-lookup"><span data-stu-id="7986b-682">Catch weight management</span></span>
    - <span data-ttu-id="7986b-683">Fyysinen negatiivinen varasto</span><span class="sxs-lookup"><span data-stu-id="7986b-683">Physical negative inventory</span></span>
    - <span data-ttu-id="7986b-684">Varaus tilatun tarjonnan perusteella</span><span class="sxs-lookup"><span data-stu-id="7986b-684">Reservation against ordered supply</span></span>
    - <span data-ttu-id="7986b-685">Siirtotilaukset ja raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="7986b-685">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="7986b-686">Kontin direktiiviyksiköittäin pakkaamisen konsolidointisäännöllä on rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="7986b-686">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="7986b-687">Tilaussidonnaisten varausten osalta suosittelemme välttämää sellaisten kontinrakennusmallien käyttöä, joissa **Pakkaa direktiiviyksiköittäin** -kenttä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="7986b-687">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="7986b-688">Nykyisessä ratkaisussa sijaintidirektiivejä ei käytetä varastotyön luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7986b-688">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="7986b-689">Siksi vain yksikön sarjaryhmän alinta yksikköä (varastoyksikköä) käytetään konttiinpakkauksen aaltovaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="7986b-689">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
