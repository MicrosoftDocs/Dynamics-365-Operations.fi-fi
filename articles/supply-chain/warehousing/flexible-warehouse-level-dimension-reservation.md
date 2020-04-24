---
title: Joustava varastotason dimensionvarauskäytäntö
description: Tässä ohjeaiheessa kuvataan varaston varauskäytäntö, joka mahdollistaa eräseurattuja tuotteita myyville ja niiden logistiikan varastonhallintajärjestelmän toiminnoilla toteuttaville yrityksille tiettyjen erien varaamisen asiakkaiden myyntitilauksille, vaikka tuotteiden varaushierarkia ei salli tiettyjen erien varausta.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0fe9ed9f2bebe8683f3b8bb37b33e8a63b9521f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205664"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="bae56-103">Joustava varastotason dimensionvarauskäytäntö</span><span class="sxs-lookup"><span data-stu-id="bae56-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bae56-104">Kun Erä alla\[sijainti\]-tyyppinen varastonvaraushierarkia yhdistetään tuotteisiin, eräseurattuja tuotteita myyvät ja niiden logistiikan Microsoft Dynamics 365 -varastonhallintajärjestelmävalmiilla (WMS) toiminnoilla toteuttavat yritykset eivät voi varata tiettyjä kyseisten tuotteiden eriä asiakkaiden myyntitilauksille.</span><span class="sxs-lookup"><span data-stu-id="bae56-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="bae56-105">Tässä ohjeaiheessa kuvataan varastonvarauskäytäntö, jonka avulla nämä yritykset varaavat tiettyjä eriä, vaikka tuotteet on yhdistetty Erä alla\[sijainti\]-varaushierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="bae56-106">Varastovaraushierarkia</span><span class="sxs-lookup"><span data-stu-id="bae56-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="bae56-107">Tässä osassa on yhteenveto olemassa olevasta varastonvaraushierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="bae56-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="bae56-108">Se keskittyy tapaan, jolla erä- ja sarjaseurattuja kohteita käsitellään.</span><span class="sxs-lookup"><span data-stu-id="bae56-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="bae56-109">Varastonvaraushierarkia määrää, että varastodimensioiden osalta kysyntätilaus sisältää pakolliset dimensiot toimipaikka, varasto ja varastotila. Varastologiikka taas vastaa sijainnin osoittamisesta pyydetyille määrille ja kyseisen sijainnin varaamisesta.</span><span class="sxs-lookup"><span data-stu-id="bae56-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="bae56-110">Toisin sanoen kysyntätilauksen ja varastotoimintojen välisissä vuorovaikutuksissa kysyntätilauksen oletetaan ilmaisevan, mistä tilaus on lähetettävä (eli mistä toimipaikasta ja varastosta).</span><span class="sxs-lookup"><span data-stu-id="bae56-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="bae56-111">Tämän jälkeen varasto tukeutuu logiikkaan löytääkseen vaaditun määrän varastotilasta.</span><span class="sxs-lookup"><span data-stu-id="bae56-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="bae56-112">Yrityksen toimintamallin heijastamista varten seurantadimensiot (erä- ja sarjanumerot) ovat joustavampia.</span><span class="sxs-lookup"><span data-stu-id="bae56-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="bae56-113">Varastonvaraushierarkia voi mukautua seuraavankaltaisiin tilanteisiin:</span><span class="sxs-lookup"><span data-stu-id="bae56-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="bae56-114">Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot, sen jälkeen, kun määrät on löydetty varaston säilytystilasta.</span><span class="sxs-lookup"><span data-stu-id="bae56-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="bae56-115">Tätä mallia kutsutaan usein nimellä *Erä alla\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="bae56-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="bae56-116">Sitä käytetään yleensä silloin, kun tuotteen erä- tai sarjanumeron tunnistus ei ole tärkeä asiakkaille, jotka tekevät pyynnön myyjäyritykselle.</span><span class="sxs-lookup"><span data-stu-id="bae56-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="bae56-117">Jos erä- tai sarjanumerot ovat osa asiakkaan tilausmääritystä ja ne tallennetaan kysyntätilaukseen, varastotoiminnot, jotka etsivät määrät varastosta, rajoitetaan tiettyihin pyydettyihin numeroihin, joita ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="bae56-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="bae56-118">Tätä mallia kutsutaan nimellä *Erä yllä\[sijainti\]*.</span><span class="sxs-lookup"><span data-stu-id="bae56-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="bae56-119">Näissä skenaarioissa haasteena on, että kullekin vapautetulle tuotteelle voidaan määrittää vain yksi varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="bae56-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="bae56-120">Siksi, jotta varastonhallintajärjestelmä määrittäisi hierarkian määrittämisen jälkeen, milloin erä- tai sarjanumero pitäisi varata (joko kun kysyntätilaus saadaan tai varaston keräilytyön aikana), kyseistä ajoitusta ei voi muuttaa tilannekohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="bae56-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="bae56-121">Eräseurattujen nimikkeiden joustava varaus</span><span class="sxs-lookup"><span data-stu-id="bae56-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="bae56-122">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="bae56-122">Business scenario</span></span>

<span data-ttu-id="bae56-123">Tässä skenaariossa yritys käyttää varastostrategiaa, jossa valmiita tavaroita seurataan eränumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="bae56-124">Yritys käyttää myös varastonhallinnan työkuormitusta.</span><span class="sxs-lookup"><span data-stu-id="bae56-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="bae56-125">Koska tässä työkuormituksessa on hyvin toimiva logiikka varaston keräily- ja lähetystoimintojen suunnittelulle ja suorittamiselle erämääräisiä nimikkeitä varten, useimmille valmiille nimikkeille määritetään Erä alla\[sijainti\] -varastonvaraushierarkia.</span><span class="sxs-lookup"><span data-stu-id="bae56-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="bae56-126">Tällaisen operatiivisen määrityksen etuna on, että päätöksiä (jotka ovat käytännössä varauspäätöksiä) siitä, mitkä erät kerätään ja mihin ne laitetaan varastossa, lykätään siihen asti, että varastoin keräilytoiminnot alkavat.</span><span class="sxs-lookup"><span data-stu-id="bae56-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="bae56-127">Niitä ei tehdä, kun asiakkaan tilaus saadaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="bae56-128">Vaikka Erä alla\[sijainti\] -varaushierarkia palvelee yrityksen liiketoimintatavoitteita hyvin, monet yrityksen vakiintuneista asiakkaista tarvitsevat aikaisemmin ostamansa erää, kun ne tilaavat tuotteita uudelleen.</span><span class="sxs-lookup"><span data-stu-id="bae56-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="bae56-129">Siksi yritys etsii joustavuutta erävaraussääntöjen käsittelyyn, jotta asiakkaan samaa nimikettä koskevasta kysynnästä riippuen, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="bae56-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="bae56-130">Eränumero voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi muuttaa varastotoimintojen aikana ja/tai osoittaa muille kysynnöille.</span><span class="sxs-lookup"><span data-stu-id="bae56-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="bae56-131">Tämä auttaa takaamaan, että tilattu eränumero toimitetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="bae56-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="bae56-132">Jos eränumerolla ei ole merkitystä asiakkaalle, varastotoiminnot voivat määrittää eränumeron keräilyn aikana, kun myyntitilauksen kirjaus ja varaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="bae56-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="bae56-133">Tietyn erän myyntilaukselle varaamisen mahdollistaminen</span><span class="sxs-lookup"><span data-stu-id="bae56-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="bae56-134">Jotta haluttu erävarauksen joustavuus mahdollistetaan nimikkeille, joilla on Erä alla\[sijainti\] -varastonvaraushierarkia, varastopäällikköjen on valittava **Salli varaus kysyntätilauksessa** -valintaruutu **Eränumero** -tasolla sivulla **Varastonvaraushierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="bae56-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varastovarausten hierarkian joustavoittaminen](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="bae56-136">Kun hierarkian **Eränumero**-taso on valittuna, kaikki kyseisen tason yläpuolella olevat dimensiot aina **Sijainti**-tasolle valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bae56-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="bae56-137">(Oletusarvoisesti kaikki **Sijainti**-tason yläpuolella olevat dimensiot on esivalittu.) Tämä toiminta perustuu logiikkaan, jossa myös kaikki eränumeron ja sijainnin välisen alueen dimensiot varataan automaattisesti, kun varaat tietyn eränumeron tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="bae56-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="bae56-138">**Salli varaus kysyntätilauksessa** -valintaruutu pätee vain varaushierarkiatasoille, jotka ovat varastosijainnin dimension alapuolella.</span><span class="sxs-lookup"><span data-stu-id="bae56-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="bae56-139">**Eränumero** on hierarkian ainoa taso, johon joustavaa varauskäytäntöä voi soveltaa.</span><span class="sxs-lookup"><span data-stu-id="bae56-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="bae56-140">Toisin sanoen et voi valita **Salli varaus kysyntätilauksessa** -valintaruutua tasoille **Sijainti**, **Rekisterikilpi** tai **Sarjanumero**.</span><span class="sxs-lookup"><span data-stu-id="bae56-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="bae56-141">Jos varaushierarkia sisältää sarjanumerodimension (jonka on aina oltava **Eränumero**-tason alapuolella) ja jos olet ottanut eräkohtaisen varauksen käyttöön eränumerolle, järjestelmä jatkaa sarjanumeroiden varaus- ja keräilytoimintojen käsittelyä niiden sääntöjen perusteella, jotka pätevät Sarja alla\[sijainti\] -varauskäytäntöön.</span><span class="sxs-lookup"><span data-stu-id="bae56-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="bae56-142">Voit missä tahansa vaiheessa ottaa eräkohtaisenvarauksen käyttöön olemassa olevalle Erä alla\[sijainti\] -varaushierarkialle ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="bae56-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="bae56-143">Tämä muutos ei vaikuta varauksiin ja avoimiin varastotöihin, jotka on luotu ennen muutosta.</span><span class="sxs-lookup"><span data-stu-id="bae56-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="bae56-144">**Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos varasto-ottotyypin **Varattu tilattu**, **Varattu fyysinen** tai **Tilattu** varastotapahtumia on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.</span><span class="sxs-lookup"><span data-stu-id="bae56-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="bae56-145">Jos nimikkeen käytössä oleva varaushierarkia ei salli erän määritystä tilauksessa, voit siirtää sen varaushierarkiaan, joka sallii erän määrityksen, kunhan hierarkiatasorakenne on sama molemmissa hierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="bae56-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="bae56-146">Tee siirto toiminnolla **Muuta nimikkeiden varaushierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="bae56-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="bae56-147">Tästä muutoksesta voi olla hyötyä, kun haluat estää eräseurattujen nimikkeiden alijoukon joustavan erävarauksen, mutta sallia sen muun tuoteportfolion osalta.</span><span class="sxs-lookup"><span data-stu-id="bae56-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="bae56-148">Riippumatta siitä, oletko valinnut **Salli varaus kysyntätilauksessa** -valintaruudun, jos et halua varata nimikkeelle tiettyä eränumeroa tilausrivillä, oletusarvoinen varastotoimintologiikka, jota sovelletaan Erä alla\[sijainti\] -varaushierarkiaan, pätee edelleen.</span><span class="sxs-lookup"><span data-stu-id="bae56-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="bae56-149">Tietyn eränumeron varaaminen asiakastilausta varten</span><span class="sxs-lookup"><span data-stu-id="bae56-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="bae56-150">Kun eräseuratun nimikkeen Erä alla\[sijainti\] -varastonvaraushierarkia on määritetty sallimaan tiettyjen eränumeroiden varaaminen myyntitilauksissa, myyntitilausten käsittelijät voivat ottaa saman nimikkeen asiakastilauksia vastaan jollakin seuraavista tavoista asiakkaan pyynnöstä riippuen:</span><span class="sxs-lookup"><span data-stu-id="bae56-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="bae56-151">**Anna tilaustiedot ilman eränumeron määritystä** – Tätä menetelmää kannattaa käyttää, kun tuotteen erämääritys ei ole tärkeä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="bae56-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="bae56-152">Kaikki aiemmin luodut prosessit, jotka liittyvät tällaisen tilauksen käsittelyyn, eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="bae56-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="bae56-153">Käyttäjiltä ei vaadita lisätoimia.</span><span class="sxs-lookup"><span data-stu-id="bae56-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="bae56-154">**Anna tilaustiedot ja varaa tietty eränumero** – Tätä menetelmää kannattaa käyttää, kun asiakas pyytää tiettyä erää.</span><span class="sxs-lookup"><span data-stu-id="bae56-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="bae56-155">Yleensä asiakkaat pyytävät tiettyä erää, kun he tilaavat uudelleen aiemmin ostamaansa tuotetta.</span><span class="sxs-lookup"><span data-stu-id="bae56-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="bae56-156">Tällaista eräkohtaisia varausta kutsutaan nimellä *eräsidonnainen varaus*.</span><span class="sxs-lookup"><span data-stu-id="bae56-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="bae56-157">Seuraavat säännöt ovat voimassa, kun käsitellään määriä ja tietylle tilaukselle on määritetty eränumero:</span><span class="sxs-lookup"><span data-stu-id="bae56-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="bae56-158">Jotta tietyn eränumeron varaaminen nimikkeelle olisi mahdollista Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="bae56-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="bae56-159">Tähän väliin kuuluu yleensä myös rekisterikilpidimensio.</span><span class="sxs-lookup"><span data-stu-id="bae56-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="bae56-160">Sijaintidirektiivejä ei käytetä, kun keräilytyö luodaan myyntiriville, jossa käytetään tilaussidonnaista eränvarausta.</span><span class="sxs-lookup"><span data-stu-id="bae56-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="bae56-161">Tilaussidonnaisiin eriin kohdistuvan työn varastokäsittelyn aikana käyttäjä tai järjestelmä ei voi muuttaa eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="bae56-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="bae56-162">(Tämä käsittely sisältää poikkeuksen käsittelyn.)</span><span class="sxs-lookup"><span data-stu-id="bae56-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="bae56-163">Seuraavassa esimerkissä työnkulku näkyy kokonaisuudessaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bae56-164">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="bae56-164">Example scenario</span></span>

<span data-ttu-id="bae56-165">Esittelytietojen on oltava asennettuna tätä esimerkkiä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="bae56-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="bae56-166">Varastonvaraushierarkian määrittäminen sallimaan eräkohtainen varaus</span><span class="sxs-lookup"><span data-stu-id="bae56-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="bae56-167">Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto \> Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="bae56-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="bae56-168">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bae56-168">Select **New**.</span></span>
3. <span data-ttu-id="bae56-169">Anna nimi **Nimi**-kentässä (esim. **EräFlex**).</span><span class="sxs-lookup"><span data-stu-id="bae56-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="bae56-170">Anna kuvaus **Kuvaus**-kentässä (esim. **Erä joustavan alla**).</span><span class="sxs-lookup"><span data-stu-id="bae56-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="bae56-171">Valitse **Valittu**-kentässä **Sarjanumero** ja **Omistaja** ja siirrä ne sitten **Käytettävissä**-kenttään vasemman nuolipainikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="bae56-172">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bae56-172">Select **OK**.</span></span>
7. <span data-ttu-id="bae56-173">Valitse **Eränumero** -dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**.</span><span class="sxs-lookup"><span data-stu-id="bae56-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="bae56-174">Tasot **Rekisterikilpi** ja **Sijainti** valitaan automaattisesti eikä niiden valintaruutuja voi tyhjentää.</span><span class="sxs-lookup"><span data-stu-id="bae56-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="bae56-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="bae56-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="bae56-176">Uuden julkaistun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="bae56-176">Create a new released product</span></span>

1. <span data-ttu-id="bae56-177">Määritä tuotteen kolme päätietoparametria käyttämällä seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="bae56-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="bae56-178">Valitse **Varastodimensioryhmä**-kentässä **Tavara**.</span><span class="sxs-lookup"><span data-stu-id="bae56-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="bae56-179">Valitse **Seurantadimensioryhmä**-kentässä **Erä-fyy**.</span><span class="sxs-lookup"><span data-stu-id="bae56-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="bae56-180">Valitse **Varaushierarkia** -kentässä **EräFlex**.</span><span class="sxs-lookup"><span data-stu-id="bae56-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="bae56-181">Luo kaksi eränumeroa, kuten**B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="bae56-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="bae56-182">Lisää nimekemääriä käytettävissä olevaan varastoon seuraavien arvojen avulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="bae56-183">Varasto</span><span class="sxs-lookup"><span data-stu-id="bae56-183">Warehouse</span></span> | <span data-ttu-id="bae56-184">Eränumero</span><span class="sxs-lookup"><span data-stu-id="bae56-184">Batch number</span></span> | <span data-ttu-id="bae56-185">Toimipaikka</span><span class="sxs-lookup"><span data-stu-id="bae56-185">Location</span></span> | <span data-ttu-id="bae56-186">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="bae56-186">License plate</span></span> | <span data-ttu-id="bae56-187">Määrä</span><span class="sxs-lookup"><span data-stu-id="bae56-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="bae56-188">24</span><span class="sxs-lookup"><span data-stu-id="bae56-188">24</span></span>        | <span data-ttu-id="bae56-189">B11</span><span class="sxs-lookup"><span data-stu-id="bae56-189">B11</span></span>          | <span data-ttu-id="bae56-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="bae56-190">BULK-001</span></span> | <span data-ttu-id="bae56-191">Ei ole</span><span class="sxs-lookup"><span data-stu-id="bae56-191">None</span></span>          | <span data-ttu-id="bae56-192">10</span><span class="sxs-lookup"><span data-stu-id="bae56-192">10</span></span>       |
    | <span data-ttu-id="bae56-193">24</span><span class="sxs-lookup"><span data-stu-id="bae56-193">24</span></span>        | <span data-ttu-id="bae56-194">B11</span><span class="sxs-lookup"><span data-stu-id="bae56-194">B11</span></span>          | <span data-ttu-id="bae56-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="bae56-195">FL-001</span></span>   | <span data-ttu-id="bae56-196">LP11</span><span class="sxs-lookup"><span data-stu-id="bae56-196">LP11</span></span>          | <span data-ttu-id="bae56-197">10</span><span class="sxs-lookup"><span data-stu-id="bae56-197">10</span></span>       |
    | <span data-ttu-id="bae56-198">24</span><span class="sxs-lookup"><span data-stu-id="bae56-198">24</span></span>        | <span data-ttu-id="bae56-199">B22</span><span class="sxs-lookup"><span data-stu-id="bae56-199">B22</span></span>          | <span data-ttu-id="bae56-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="bae56-200">FL-002</span></span>   | <span data-ttu-id="bae56-201">LP22</span><span class="sxs-lookup"><span data-stu-id="bae56-201">LP22</span></span>          | <span data-ttu-id="bae56-202">10</span><span class="sxs-lookup"><span data-stu-id="bae56-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="bae56-203">Syötä myyntitilaustiedot</span><span class="sxs-lookup"><span data-stu-id="bae56-203">Enter sales order details</span></span>

1. <span data-ttu-id="bae56-204">Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="bae56-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="bae56-205">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bae56-205">Select **New**.</span></span>
3. <span data-ttu-id="bae56-206">Syötä myyntitilausotsikon **Asiakastili**-kenttään **US-003**.</span><span class="sxs-lookup"><span data-stu-id="bae56-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="bae56-207">Lisää rivi uutta nimikettä varten ja syötä määräksi **10**.</span><span class="sxs-lookup"><span data-stu-id="bae56-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="bae56-208">Varmista, että **Varasto**-kentän arvo on **24**.</span><span class="sxs-lookup"><span data-stu-id="bae56-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="bae56-209">Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto** ja sitten **Ylläpidä**-ryhmässä **Erävaraus**.</span><span class="sxs-lookup"><span data-stu-id="bae56-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="bae56-210">**Erävaraus**-sivulla näkyy luettelo eristä, jotka voidaan varata tilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="bae56-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="bae56-211">Tässä esimerkissä määränä on **20** eränumerolle **B11** ja **10** eränumerolle **B22**.</span><span class="sxs-lookup"><span data-stu-id="bae56-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="bae56-212">Huomaa, että **Erävaraus**-sivua ei voi käyttää riviltä, jos rivin nimikkeelle on määritetty Erä alla\[sijainti\] -varaushierarkia, ellei sitä ole määritetty sallimaan eräkohtaista varausta.</span><span class="sxs-lookup"><span data-stu-id="bae56-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bae56-213">Varataksesi ostotilaukselle tietyn erän sinun on käytettävä **Erävaraus** -sivua.</span><span class="sxs-lookup"><span data-stu-id="bae56-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="bae56-214">Jos syötät eränumeron suoraan myyntitilausriville, järjestelmä toimii siten kuin olisit syöttänyt tietyn eräarvon nimikkeelle, johon sovelletaan Erä alla\[sijainti\] -varauskäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="bae56-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="bae56-215">Kun tallennat rivin, näyttöön tulee varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="bae56-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="bae56-216">Jos vahvistat, että eränumero on määritettävä suoraan tilausrivillä, tavanomainen varastonhallintalogiikka ei käsittele kyseistä riviä.</span><span class="sxs-lookup"><span data-stu-id="bae56-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="bae56-217">Jos varaat määrän **Varaus**-sivulta, tiettyä erää ei varata ja rivin osalta sovelletaan varastotoimintojen suorittamiseen niitä sääntöjä, joita sovelletaan Erä alla\[sijainti\] -varastokäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="bae56-218">Yleensä tämä sivu toimii ja siihen sovelletaan samaa vuorovaikutusta kuin silloin, kun asianomaisille nimikkeille on määritetty Erä yllä\[sijainti\] -tyyppinen varaushierarkia.</span><span class="sxs-lookup"><span data-stu-id="bae56-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="bae56-219">Seuraavat poikkeukset kuitenkin pätevät:</span><span class="sxs-lookup"><span data-stu-id="bae56-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="bae56-220">**Lähderiville sidotut eränumerot** -pikavälilehdessä näkyvät tilausriville varatut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="bae56-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="bae56-221">Ruudukon eräarvot näkyvät koko tilausrivin toteutusjakson aikana, varaston käsittelyvaiheet mukaan luettuna.</span><span class="sxs-lookup"><span data-stu-id="bae56-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="bae56-222">**Yhteenveto**-pikavälilehdessä ruudukossa sen sijaan näkyy tavanomainen tilausrivin varaus (eli **Sijainti**-tason yläpuoleisille dimensioille tehtävä varaus) aina siihen asti, kun varastotyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="bae56-223">Tämän jälkeen rivinvaraus siirtyy työyksikölle, eikä rivinvaraus enää ole näkyvissä sivulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="bae56-224">**Lähderiviin sidotut eränumerot** -pikavälilehti auttaa sen varmistamisessa, että myyntitilausten käsittelijä näkee asiakkaan tilaukseen missä tahansa sen elinkaaren aikana aina laskutukseen asti sidotut eränumerot.</span><span class="sxs-lookup"><span data-stu-id="bae56-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="bae56-225">Tietyn erän varauksen lisäksi käyttäjä voi valita erän sijainnin ja rekisterikilven manuaalisesti sen sijaan, että se antaisi järjestelmän valita ne automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bae56-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="bae56-226">Tämä ominaisuus liittyy tilaussidonnaisen erävarausmekanismin rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="bae56-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="bae56-227">Kuten aiemmin mainittiin, kun nimikkeelle varataan eränumero Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti.</span><span class="sxs-lookup"><span data-stu-id="bae56-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="bae56-228">Tämän vuoksi varastotyössä käytetään tilauksia käsitelleiden käyttäjien varaamia varastodimensioita, eivätkä ne aina välttämättä vastaa nimikkeen kätevää tai edes mahdollista varastointipaikkaa keräilytoimintoja varten.</span><span class="sxs-lookup"><span data-stu-id="bae56-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="bae56-229">Jos tilausten käsittelijät ovat tietoisia varaston rajoituksista, heidän saattaa kannattaa valita sijainnit ja rekisterikilvet manuaalisesti, kun he varaavat erää.</span><span class="sxs-lookup"><span data-stu-id="bae56-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="bae56-230">Tällöin käyttäjän on käytettävä **Näytä dimensiot** -toimintoa sivun otsikossa ja lisättävä sijainti ja rekisterikilpi **Yhteenveto**-pikavälilehden ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="bae56-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="bae56-231">Valitse **Erävaraus**-sivulla erän **B11** rivi ja sitten **Varaa rivi**.</span><span class="sxs-lookup"><span data-stu-id="bae56-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="bae56-232">Sijaintien ja rekisterikilpien määritykselle ei ole omaa logiikkaansa automaattisen varauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="bae56-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="bae56-233">Voit syöttää määrän manuaalisesti **Varaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bae56-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="bae56-234">Huomaa, että **Lähderiviin sidotut eränumerot**-pikavälilehdessä erän **B11** arvona on **Sidottu**.</span><span class="sxs-lookup"><span data-stu-id="bae56-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Tietyn eränumeron sitominen myyntitilausriviin erävaraussivulla](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="bae56-236">Myyntitilausrivin määrä voidaan varata eri eristä.</span><span class="sxs-lookup"><span data-stu-id="bae56-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="bae56-237">Myös samaa erää voidaan varata useiden sijaintien ja rekisterikilpien perusteella (jos rekisterikilvet on sallittu sijainneille).</span><span class="sxs-lookup"><span data-stu-id="bae56-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="bae56-238">Tietyn erän varaaminen myyntitilausrivin määrälle voi olla myös osittaista.</span><span class="sxs-lookup"><span data-stu-id="bae56-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="bae56-239">Esimerkiksi 100 yksikön kokonaismäärä voidaan varata siten, että tietty erä on sidottu 20 yksikköön, kun taas 80 yksikköä varataan toimipaikka- ja varastotasolla mistä tahansa käytettävissä olevasta erästä.</span><span class="sxs-lookup"><span data-stu-id="bae56-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="bae56-240">Tässä tapauksessa varastonhallintajärjestelmä käsittelee keräilytoiminnot käyttäen kahta erillistä työriviä.</span><span class="sxs-lookup"><span data-stu-id="bae56-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="bae56-241">Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="bae56-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="bae56-242">Valitse nimikkeesi ja sitten **Hallitse varastoa** \> **Näytä** \> **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="bae56-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tilaussidonnainen varaus varastotapahtumatyyppinä](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="bae56-244">Tarkista nimikkeen varastotapahtumat, jotka liittyvät myyntitilausrivin varaukseen.</span><span class="sxs-lookup"><span data-stu-id="bae56-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="bae56-245">Tapahtuma, jossa **Viite**-kentän arvona on **Myyntitilaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta **Sijainti**-tason yläpuolella olevien dimension osalta.</span><span class="sxs-lookup"><span data-stu-id="bae56-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="bae56-246">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat toimipaikka, varasto ja varastotila.</span><span class="sxs-lookup"><span data-stu-id="bae56-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="bae56-247">Tapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta määritetyn erän ja kaikkien sen yläpuolella olevien dimensioiden osalta.</span><span class="sxs-lookup"><span data-stu-id="bae56-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="bae56-248">Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat eränumero ja sijainti.</span><span class="sxs-lookup"><span data-stu-id="bae56-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="bae56-249">Tässä esimerkissä sijainti on **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="bae56-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="bae56-250">Valitse myyntitilauksen otsikossa **Varasto** \> **Toiminnot** \> **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="bae56-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="bae56-251">Tilausrivi on nyt aallotettu, ja kuormitus ja työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="bae56-252">Niiden varastotöiden tarkistus ja käsittely, joilla on tilaussidonnaisia eränumeroita</span><span class="sxs-lookup"><span data-stu-id="bae56-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="bae56-253">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** \> **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="bae56-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="bae56-254">Työllä, joka käsittelee myyntitilausriviin sidottujen erämäärien keräilytoiminnon, on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="bae56-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="bae56-255">Järjestelmä käyttää työn luomisessa työmalleja, mutten sijaintidirektiivejä.</span><span class="sxs-lookup"><span data-stu-id="bae56-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="bae56-256">Kaikkia työmalleille määritettyjä vakioasetuksia, kuten keräilyrivien tai tietyn mittayksikön enimmäismäärää, käytetään sen määrittämisessä, milloin uusi työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="bae56-257">Keräilysijaintien tunnistamisen sijaintidirektiiveihin liittyviä sääntöjä ei kuitenkaan oteta huomioon, koska tilaussidonnaisessa varauksessa määritetään jo kaikki varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="bae56-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="bae56-258">Nämä varastodimensiot sisältävät varastosäilytystason dimensiot.</span><span class="sxs-lookup"><span data-stu-id="bae56-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="bae56-259">Siten työ perii kyseiset dimensiot ilman sijaintidirektiivien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="bae56-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="bae56-260">Eränumeroa ei näytetä keräilyrivillä (kuten työrivillä, joka luodaan nimikkeelle, johon liittyy Erä yllä\[sijainti\]-varaushierarkia). Sen sijaan kohteesta-eränumero ja kaikki muut varastodimensiot näkyvät työrivin työvarastotapahtumassa, joka perustuu tähän liittyviin varastotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="bae56-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Varaston varastotapahtuma töille, jotka perustuvat tilaussidonnaiseen varaukseen](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="bae56-262">Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus**, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="bae56-263">Varastotapahtuma, jossa **Viite**-kentän arvona on **Työ**, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.</span><span class="sxs-lookup"><span data-stu-id="bae56-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="bae56-264">Varastotoiminnot voivat seuraavaksi suorittaa työt tavanomaiseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="bae56-265">Mobiililaitteen ohjeet kuitenkin ohjeistavat työntekijää keräilemään tiettyä eränumeroa.</span><span class="sxs-lookup"><span data-stu-id="bae56-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="bae56-266">Varastoympäristöissä, joissa sijainteja hallitaan rekisterikilvillä, työntekijä voi keräillä mistä tahansa vielä varaamattomasta rekisterikilvestä (jota ei siis ole varattu toiselle tilaussidonnaiselle varaukselle tai työlle, joka perustuu tällaiselle varaukselle), kun hän saapuu sijainnille, jossa säilytetään samaa erää useissa rekisterikilvissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="bae56-267">Jos on epäkäytännöllistä keräillä työrivillä määritetystä sijainnista, varasto-operaattorit voivat käyttää jotakin seuraavista toiminnoista tietyn erän keräilyn siirtämiseen kätevämpään sijaintiin:</span><span class="sxs-lookup"><span data-stu-id="bae56-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="bae56-268">Vakiomuotoinen mobiililaitteen **Ohita toiminto** (jos varastotyöntekijän **Salli keräilysijainnin ohitus** -asetus on käytössä)</span><span class="sxs-lookup"><span data-stu-id="bae56-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="bae56-269">**Muuta sijaintia** -toiminto **Työluettelon tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="bae56-270">Lopeta työn keräily ja hyllytys mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="bae56-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="bae56-271">Eränumeroa **B11** on nyt kerätty määrä **10** myyntitilausriviä varten ja siirretty sijaintiin **Lastauspaikan ovi**.</span><span class="sxs-lookup"><span data-stu-id="bae56-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="bae56-272">Tässä vaiheessa se on valmis lastattavaksi kuorma-autoon ja lähetettäväksi asiakkaan osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="bae56-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="bae56-273">Niiden varastotöiden poikkeustenkäsittely, joilla on tilaussidonnaiset eränumerot</span><span class="sxs-lookup"><span data-stu-id="bae56-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="bae56-274">Tilaussidonnaisten eränumeroiden keräilyn varastotyöhön sovelletaan samoja varaston poikkeustenkäsittelyä ja -toimintoja kuin tavanomaiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="bae56-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="bae56-275">Yleisesi ottaen avoin työ tai työrivi voidaan peruuttaa, se voidaan keskeyttää, koska käyttäjän sijainti on täynnä, siihen voidaan soveltaa lyhyttä keräilyä ja sitä voidaan päivittää siirron vuoksi.</span><span class="sxs-lookup"><span data-stu-id="bae56-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="bae56-276">Samoin jo valmiiksi saatua keräiltyä työmäärää voidaan vähentää tai työ voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="bae56-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="bae56-277">Kaikkiin näihin poikkeusten käsittelyn toimintoihin sovelletaan seuraavaa keskeistä sääntöä: asiakkaalle varattua eränumeroa ei voi koskaan korvata toisella eränumerolla, mutta sen varastodimensioita (sijainti ja rekisterikilpi) voi muuttaa joko käyttäjän manuaalisella päivityksellä tai järjestelmän automaattisella päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="bae56-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="bae56-278">Automaattinen päivitys perustuu samaan varastodimensioiden satunnaiseen määrittämiseen, jota käytetään, kun tietty erä varataan automaattisesti mutta varastodimensioita ei määritetä.</span><span class="sxs-lookup"><span data-stu-id="bae56-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="bae56-279">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="bae56-279">Example scenario</span></span>

<span data-ttu-id="bae56-280">Esimerkki tästä skenaariosta on tilanne, jossa aiemmin valmistuneiden töiden keräily perutaan **Vähennä keräiltyä määrää** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="bae56-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="bae56-281">Tämä esimerkki jatkaa tämän aiheen edellistä esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="bae56-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="bae56-282">Siirry kohtaan **Varastonhallinta** \> **Kuormat** \> **Aktiiviset kuormat**.</span><span class="sxs-lookup"><span data-stu-id="bae56-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="bae56-283">Valitse kuorma, joka on luotu myyntitilauksen lähetyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bae56-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="bae56-284">Valitse **Kuormatilauksen rivit** -pikavälilehdestä **Vähennä keräiltyä määrää**.</span><span class="sxs-lookup"><span data-stu-id="bae56-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="bae56-285">Valitse **Vähennä keräiltyä määrää** -sivun **Siirrä sijaintiin** -kentässä **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="bae56-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="bae56-286">Valitse **Siirrä rekisterikilvelle**-kentässä **LP33**.</span><span class="sxs-lookup"><span data-stu-id="bae56-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="bae56-287">Syötä **Peruttava keräilty varastomäärä** -kenttään arvo **10**.</span><span class="sxs-lookup"><span data-stu-id="bae56-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="bae56-288">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bae56-288">Select **OK**.</span></span>

<span data-ttu-id="bae56-289">Tässä ovat keräilyn perumisen tulokset:</span><span class="sxs-lookup"><span data-stu-id="bae56-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="bae56-290">Aiemmin suljetun työn tilaksi määritetään **Peruttu**.</span><span class="sxs-lookup"><span data-stu-id="bae56-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="bae56-291">Uusi **Varastonsiirto**-tyypin työ luodaan varastomäärälle **10** eränumerossa **B11**.</span><span class="sxs-lookup"><span data-stu-id="bae56-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="bae56-292">Tämä työ edustaa siirtoa sijainnista **Lastauspaikan ovi** rekisterikilvelle **LP33** sijainnissa **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="bae56-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="bae56-293">Tilaksi määritetään **Suljettu**.</span><span class="sxs-lookup"><span data-stu-id="bae56-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="bae56-294">Järjestelmä varaa uudelleen alun perin tilatun eränumeron ja määrittää sijainnin ja rekisterikilpitunnukset.</span><span class="sxs-lookup"><span data-stu-id="bae56-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="bae56-295">(Tämä prosessi vastaa **Vara rivi** -toiminnon suorittamista tietyn eränumeron tilausriville).</span><span class="sxs-lookup"><span data-stu-id="bae56-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="bae56-296">Tämän tuloksena erä **B11** näkyy sidottuna **Lähderiville sidotut eränumerot** -pikavälilehdessä sivulla **Erävaraus** ja **Varaus**-kentässä on määrä **10** eränumeron **B11** osalta.</span><span class="sxs-lookup"><span data-stu-id="bae56-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="bae56-297">Lisäksi **Sijainti**-kentän arvona on **FL-001** ja **Rekisterikilpi**-kentän arvona on **LP11**.</span><span class="sxs-lookup"><span data-stu-id="bae56-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="bae56-298">(Voit lisätä nämä kentät ruudukkoon, jos ne eivät ole näkyvissä.)</span><span class="sxs-lookup"><span data-stu-id="bae56-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="bae56-299">Seuraavissa taulukoissa on yhteenveto siitä, miten järjestelmä käsittelee tiettyjen varastotoimintojen tilaussidonnaisen erävarauksen.</span><span class="sxs-lookup"><span data-stu-id="bae56-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="bae56-300">Taulukkojen sisältöä tulkitaan olettamalla, että kukin varastotoiminnon suorittamiseen liittyy olemassa oleva tilaussidonnaiseen erävaraukseen perustuvaa työ tai että kunkin varastotoiminnon suorittaminen vaikuttaa kyseisentyyppiseen työhön.</span><span class="sxs-lookup"><span data-stu-id="bae56-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="bae56-301">Näissä taulukoissa Erämäärä on käytettävissä -sarake ilmaisee, onko varastomäärää käytettävissä sen määrän lisäksi, joka on jo varattu kulloisillekin tilaussidonnaisille varauksille tai joka on varattu kyseisentyyppisiin varauksiin perustuvassa varastotyössä.</span><span class="sxs-lookup"><span data-stu-id="bae56-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="bae56-302">Avoimen työn keräilysijainnin ohitus</span><span class="sxs-lookup"><span data-stu-id="bae56-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-303">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-304">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-305">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-305">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-306">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-306">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-307">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-308"><strong>Salli keräilysijainnin ohitus</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="bae56-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="bae56-309">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-310">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varaston mobiilisovelluksessa (WMA), kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="bae56-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="bae56-311">Valitse <strong>Ehdota</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="bae56-312">Vahvista uusi sijainti, jota ehdotetaan erämäärän käytettävyyden perusteella.</span><span class="sxs-lookup"><span data-stu-id="bae56-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-313">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="bae56-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="bae56-314">Keräilyrivin sijainniksi päivittyy uusi sijainti.</span><span class="sxs-lookup"><span data-stu-id="bae56-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="bae56-315">(Jos sijainti on rekisterikilpihallittu, työvarastotapahtumalle määritetään satunnainen rekisterikilpi ja työntekijä voi keräillä mistä tahansa rekisterikilvestä, jossa määrää on käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="bae56-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="bae56-316">Jos määrää on uuden sijainnin useassa rekisterikilvessä, alkuperäinen keräilyrivi jaetaan useaan riviin, jotka vastaavat kutakin rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="bae56-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-317">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-318">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-319">Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varaston WMA:ssa, kun aloitat keräilytyön.</span><span class="sxs-lookup"><span data-stu-id="bae56-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="bae56-320">Määritä sijainti manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="bae56-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-321"><strong>Ohita sijainti</strong> -toiminto ei ole mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="bae56-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="bae56-322">Se epäonnistuu, ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="bae56-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="bae56-323">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="bae56-324">Täysi-painike – Työrivin jakaminen käyttäjän sijainnin ylivuodon vuoksi</span><span class="sxs-lookup"><span data-stu-id="bae56-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-325">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-326">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-327">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-327">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-328">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-328">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-329">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bae56-330"><strong>Salli työn jakaminen</strong> -asetus on käytössä mobiililaitteen valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="bae56-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="bae56-331">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-332">Valitse valikkovaihtoehto <strong>Täysi</strong> varaston WMA:ssa, kun käsittelet keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="bae56-333">Syötä <strong>Keräilymäärä</strong>-kenttään tarvittavan keräilyn osamäärä ilmaisemaan täyttä kapasiteettia.</span><span class="sxs-lookup"><span data-stu-id="bae56-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-334">Kulloisessakin työssä määrä päivitetään vastaamaan jäljellä olevaa keräiltävää määrää.</span><span class="sxs-lookup"><span data-stu-id="bae56-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="bae56-335">Keräillylle määrälle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="bae56-336">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="bae56-337">Valmiin työn keräillyn määrän vähentäminen (kuormasta)</span><span class="sxs-lookup"><span data-stu-id="bae56-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-338">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-339">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-340">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-340">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-341">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-341">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-342">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-343">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-343">Not applicable</span></span></td>
<td><span data-ttu-id="bae56-344">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-345">Avaa <strong>Vähennä keräiltyä määrää</strong> -sivu kuormariviltä.</span><span class="sxs-lookup"><span data-stu-id="bae56-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="bae56-346">Syötä sen määrän kokonaisarvo, jonka keräily perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="bae56-347">Valitse "siirto kohteeseen" sijainti/rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="bae56-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="bae56-348">Kuormariviin liittyvä työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="bae56-349">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-350">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-351">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-352">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-352">No</span></span></td>
<td><span data-ttu-id="bae56-353">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-353">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-354">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-354">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-355">Määrä varataan uudelleen samalle erälle ja samalle sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu), jotka on syötetty keräilyn perumisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bae56-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="bae56-356">Nimikkeen siirtäminen varastossa</span><span class="sxs-lookup"><span data-stu-id="bae56-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="bae56-357">Tätä varastotoimintoa voidaan soveltaa vain **Työnluontiprosessi**-tyypin siirtoihin, ei mallin mukaiseen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="bae56-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-358">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-359">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-360">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-360">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-361">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-361">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-362">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-363"><strong>Salli työhön liitetyn varaston siirto</strong> -asetus on käytössä työntekijällä.</span><span class="sxs-lookup"><span data-stu-id="bae56-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="bae56-364">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-365">Aloita siirto WMA:lla.</span><span class="sxs-lookup"><span data-stu-id="bae56-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="bae56-366">Anna kohteesta- ja kohteeseen-sijainnit.</span><span class="sxs-lookup"><span data-stu-id="bae56-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="bae56-367">Kaikissa olemassa olevissa töissä, joihin siirto vaikuttaa, keräilysijainniksi päivitetään uusi kohteeseen-sijainti.</span><span class="sxs-lookup"><span data-stu-id="bae56-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="bae56-368">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-369">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-370">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-371">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-371">No</span></span></td>
<td><span data-ttu-id="bae56-372">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-372">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-373">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-373">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-374">Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle ja uudelle kohteeseen-sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="bae56-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="bae56-375">Valmiin työn keräillyn määrän palauttaminen (kuormasta tai aallosta)</span><span class="sxs-lookup"><span data-stu-id="bae56-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-376">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-377">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-378">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-378">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-379">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-379">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-380">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="bae56-381">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-381">Not applicable</span></span></td>
<td><span data-ttu-id="bae56-382">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-383">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="bae56-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="bae56-384">Valitse pyyntösivulla vaihtoehto <strong>Jätä nimikkeet nykyiseen sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-385">Kaikki tähän Kuormariviin liittyvät työt perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="bae56-386">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-387">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-388">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-388">No</span></span></td>
<td><span data-ttu-id="bae56-389">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-389">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-390">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-390">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-391">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä jätettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bae56-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-392">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-393">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="bae56-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="bae56-394">Valitse pyyntösivulla vaihtoehto <strong>Osoita nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-395">Nykyinen työ perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="bae56-396">Varastosiirrolle luodaan uusi työ ja se suljetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-397">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-398">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-399">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-399">No</span></span></td>
<td><span data-ttu-id="bae56-400">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-400">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-401">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-401">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-402">Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä osoitettiin palautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bae56-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-403">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="bae56-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-404">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="bae56-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="bae56-405">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet tähän sijaintiin</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-406">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="bae56-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="bae56-407">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-408">Kyllä/ei</span><span class="sxs-lookup"><span data-stu-id="bae56-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-409">Avaa <strong>Työn palautus</strong> -sivu.</span><span class="sxs-lookup"><span data-stu-id="bae56-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="bae56-410">Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet sijaintidirektiivien perusteella</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-411">Palautusta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="bae56-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="bae56-412">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="bae56-413">Määrän lyhytkeräily – Rekisteröi määrä fyysisesti löytymättömäksi sijainnista/rekisterikilvestä, kun keräilytyötä suoritetaan</span><span class="sxs-lookup"><span data-stu-id="bae56-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-414">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-415">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-416">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-416">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-417">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-417">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-418">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-419">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="bae56-420">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-421">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-422">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-423">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-424">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="bae56-425"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="bae56-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-426">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-427">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-428">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-428">No</span></span></td>
<td><span data-ttu-id="bae56-429">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="bae56-430">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="bae56-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="bae56-431">Olemassa oleva työ pysyy avoimena.</span><span class="sxs-lookup"><span data-stu-id="bae56-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-432">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-433">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="bae56-434">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-435">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-436">Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-437">Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-438">Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="bae56-439"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="bae56-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-440">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-441">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-442">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-442">No</span></span></td>
<td><span data-ttu-id="bae56-443">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-443">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-444">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-444">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-445">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-446">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei/Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="bae56-447">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="bae56-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="bae56-448">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-449">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-450">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-451">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="bae56-452">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="bae56-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-453">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="bae56-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="bae56-454">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="bae56-455">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="bae56-456">Uusi keräilyrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-456">A new pick line is created.</span></span> <span data-ttu-id="bae56-457">Siinä käytetään käyttäjän valitsemaa sijaintia/rekisterikilpeä.</span><span class="sxs-lookup"><span data-stu-id="bae56-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="bae56-458">Uusi hyllytysrivi luodaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="bae56-459"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="bae56-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-460">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-461">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="bae56-462">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="bae56-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="bae56-463">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-464">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-465">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-466">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-467">Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</span><span class="sxs-lookup"><span data-stu-id="bae56-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="bae56-468">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-469">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="bae56-470">Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="bae56-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="bae56-471">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-472">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-473">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-474">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="bae56-475">Valitsee sijainti/rekisterikilpi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="bae56-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="bae56-476">Seuraavat toiminnot tapahtuvat kulloisessakin työssä:</span><span class="sxs-lookup"><span data-stu-id="bae56-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="bae56-477">Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="bae56-478">Hyllytysrivi perutaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="bae56-479"><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</span><span class="sxs-lookup"><span data-stu-id="bae56-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bae56-480">Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin/rekisterikilven määräoikaisu vaikuttaa, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-481">Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Automaattinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä/Ei</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä/Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="bae56-482">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-483">Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</span><span class="sxs-lookup"><span data-stu-id="bae56-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="bae56-484">Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</span><span class="sxs-lookup"><span data-stu-id="bae56-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="bae56-485">Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja automaattinen uudelleenkohdistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-486">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="bae56-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="bae56-487">Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</span><span class="sxs-lookup"><span data-stu-id="bae56-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="bae56-488">Muuta varaston tilaa</span><span class="sxs-lookup"><span data-stu-id="bae56-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="bae56-489">Tämä varastotoiminto voidaan suorittaa useista aloituskohdista.</span><span class="sxs-lookup"><span data-stu-id="bae56-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="bae56-490">Tässä näkyvässä esimerkissä käytetään **Varaston tilanmuutos** -toimintoa **Käytettävissä sijainnin mukaan** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bae56-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bae56-491">Keskeiset määritysparametrit</span><span class="sxs-lookup"><span data-stu-id="bae56-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="bae56-492">Erämäärä on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="bae56-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="bae56-493">Keskeiset käyttäjän vaiheet</span><span class="sxs-lookup"><span data-stu-id="bae56-493">Key user steps</span></span></th>
<th><span data-ttu-id="bae56-494">Varastotyö</span><span class="sxs-lookup"><span data-stu-id="bae56-494">Warehouse work</span></span></th>
<th><span data-ttu-id="bae56-495">Tilaussidonnainen erävaraus</span><span class="sxs-lookup"><span data-stu-id="bae56-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-496"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Varaukset</strong> tai <strong>Merkinnät ja varaukset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="bae56-497">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-498">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="bae56-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="bae56-499">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="bae56-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="bae56-500">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="bae56-501">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-502">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="bae56-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="bae56-503">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-504">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="bae56-505">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="bae56-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="bae56-506"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="bae56-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="bae56-507">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-507">No</span></span></td>
<td><span data-ttu-id="bae56-508">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-508">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-509">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="bae56-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="bae56-510">Varaus poistetaan.</span><span class="sxs-lookup"><span data-stu-id="bae56-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="bae56-511">Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</span><span class="sxs-lookup"><span data-stu-id="bae56-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="bae56-512"><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</span><span class="sxs-lookup"><span data-stu-id="bae56-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="bae56-513"><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Ei mitään</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="bae56-514">Kyllä</span><span class="sxs-lookup"><span data-stu-id="bae56-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="bae56-515">Valitse tietty sijainti.</span><span class="sxs-lookup"><span data-stu-id="bae56-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="bae56-516">Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</span><span class="sxs-lookup"><span data-stu-id="bae56-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="bae56-517">Valitse <strong>Varaston tilanmuutos</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="bae56-518">Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae56-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="bae56-519">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="bae56-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="bae56-520">Määrä varataan uudelleen samalle erälle.</span><span class="sxs-lookup"><span data-stu-id="bae56-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="bae56-521">Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bae56-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bae56-522">Ei</span><span class="sxs-lookup"><span data-stu-id="bae56-522">No</span></span></td>
<td><span data-ttu-id="bae56-523">Katso edellinen rivi.</span><span class="sxs-lookup"><span data-stu-id="bae56-523">See the previous row.</span></span></td>
<td><span data-ttu-id="bae56-524">Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</span><span class="sxs-lookup"><span data-stu-id="bae56-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="bae56-525">Varastotilan muutokset eivät ole sallittuja.</span><span class="sxs-lookup"><span data-stu-id="bae56-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="bae56-526">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="bae56-526">Limitations</span></span>

- <span data-ttu-id="bae56-527">Joustava varastotason dimensionvaraustoiminto ei tue seuraavia ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="bae56-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="bae56-528">Todellisen painon hallinta</span><span class="sxs-lookup"><span data-stu-id="bae56-528">Catch weight management</span></span>
    - <span data-ttu-id="bae56-529">Fyysinen negatiivinen varasto</span><span class="sxs-lookup"><span data-stu-id="bae56-529">Physical negative inventory</span></span>
    - <span data-ttu-id="bae56-530">Varaus tilatun tarjonnan perusteella</span><span class="sxs-lookup"><span data-stu-id="bae56-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="bae56-531">Siirtotilaukset ja raaka-aineiden keräily</span><span class="sxs-lookup"><span data-stu-id="bae56-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="bae56-532">Kontin direktiiviyksiköittäin pakkaamisen konsolidointisäännöllä on rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="bae56-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="bae56-533">Tilaussidonnaisten varausten osalta suosittelemme välttämää sellaisten kontinrakennusmallien käyttöä, joissa **Pakkaa direktiiviyksiköittäin** -kenttä on käytössä.</span><span class="sxs-lookup"><span data-stu-id="bae56-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="bae56-534">Nykyisessä ratkaisussa sijaintidirektiivejä ei käytetä varastotyön luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bae56-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="bae56-535">Siksi vain yksikön sarjaryhmän alinta yksikköä (varastoyksikköä) käytetään konttiinpakkauksen aaltovaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="bae56-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
