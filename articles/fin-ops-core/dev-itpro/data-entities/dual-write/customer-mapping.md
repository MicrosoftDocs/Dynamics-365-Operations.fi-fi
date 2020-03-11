---
title: Integroidut asiakkaiden päätiedot
description: Tässä aiheessa kuvataan asiakastietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019763"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="c3f5d-103">Integroidut asiakkaan päätiedot</span><span class="sxs-lookup"><span data-stu-id="c3f5d-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="c3f5d-104">On tyypillistä, että asiakastietueet voidaan masteroida useammassa kuin yhdessä sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="c3f5d-105">Esimerkiksi myyntiaktiviteetti voi tuoda kaupallisia asiakastietueita myyntisovelluksen kautta, ja e-Commerce- tai vähittäismyynti voi tuoda asiakastietueita Finance and Operations -sovelluksen kautta.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="c3f5d-106">Riippumatta siitä, mistä asiakastietueet ovat peräisin, ne on integroitu taustalla sovellusten rajojen ja infrastruktuurin erojen välillä.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="c3f5d-107">Integroidut asiakkaiden päätiedot auttavat käsittelemään monimasterointiskenaarioita ja tarjoaa kattavan näkymän asiakkaasta Dynamics 365 -sovelluspakettiin.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="c3f5d-108">Asiakastietojen virta</span><span class="sxs-lookup"><span data-stu-id="c3f5d-108">Customer data flow</span></span>

<span data-ttu-id="c3f5d-109">*Asiakas* on hyvin määritelty käsite sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="c3f5d-110">Siksi asiakastietojen integrointi edellyttää vain asiakkaan käsitteen yhtenäistämistä kahden sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="c3f5d-111">Seuraavassa on kuvattu asiakastietojen virta.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-111">The following illustration shows the customer data flow.</span></span>

![Asiakastietojen virta](media/dual-write-customer-data-flow.png)

<span data-ttu-id="c3f5d-113">Asiakkaat voidaan luokitella laajasti kahteen eri luokkaan: kaupalliset/organisaation asiakkaat ja kuluttajat/loppukäyttäjät.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="c3f5d-114">Nämä kaksiasiakas tyyppiä tallennetaan ja käsitellään eri tavalla Finance and Operationsissa ja Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="c3f5d-115">Finance and Operationsissa sekä kaupalliset/organisaation asiakkaat että kuluttajat/loppukäyttäjät hallittaan yhdessä taulukossa, jonka nimi on **CustTable** (CustomerCustomerV3Entity), ja ne luokitellaan **Tyyppi**-määritteen avulla.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="c3f5d-116">(Jos **tyypiksi** on määritetty **Organisaatio**, asiakas on kaupallinen/organisaation asiakas ja jos **tyypiksi** on määritetty **Henkilö**, asiakas on kuluttaja/loppukäyttäjä.) Ensisijaisen yhteyshenkilön tietoja käsitellään SMMContactPersonEntity-entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="c3f5d-117">Common Data Servicessa kaupalliset/organisatoriset asiakkaat ovat masteroitu Asiakas-entiteetissä ja tunnistetaan asiakkaiksi , kun **RelationshipType** -määritteeksi onmääritetty **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="c3f5d-118">Yhteyshenkilö-entiteetti edustaa sekä kuluttajia/loppukäyttäjiä että yhteyshenkilöitä.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="c3f5d-119">Jotta kuluttajan/loppukäyttäjän ja yhteyshenkilön välillä olisi selvä ero **Yhteysenkilö**-entiteetissä on Boolean-merkintä nimeltään **Myytävissä**.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="c3f5d-120">Kun **Myytävissä**-arvo on **Tosi**, kontakti on kuluttaja/loppukäyttäjä ja tarjouksia ja tilauksia voidaan luoda kyseiselle kontaktille.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="c3f5d-121">Kun **Myytävissä**-arvo **Epätosi**, kontakti on vain asiakkaan ensisijainen yhteyshenkilö.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="c3f5d-122">Kun ei-Myytävissä oleva kontakti osallistuu tarjous- tai tilausprosessiin, **Myytävissä**-arvoksi annetaan **Tosi**, jotta merkitään kontakti myytävissä olevaksi kontaktiksi.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="c3f5d-123">Kontakti, josta on tullut Myytävissä oleva kontakti, on edelleen Myytävissä oleva kontakti.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="c3f5d-124">Mallit</span><span class="sxs-lookup"><span data-stu-id="c3f5d-124">Templates</span></span>

<span data-ttu-id="c3f5d-125">Asiakkaan tiedot sisältävät kaikki asiakkaan tiedot, kuten asiakasryhmän, osoitteet, yhteystiedot, maksuprofiilin, laskutusprofiilin ja kanta-asiakkuuden tilan.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="c3f5d-126">Entiteettikarttojen kokoelma toimii yhdessä asiakastietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c3f5d-127">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="c3f5d-127">Finance and Operations apps</span></span> | <span data-ttu-id="c3f5d-128">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="c3f5d-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="c3f5d-129">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="c3f5d-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="c3f5d-130">CDS-yhteyshenkilöt V2</span><span class="sxs-lookup"><span data-stu-id="c3f5d-130">CDS Contacts V2</span></span>             | <span data-ttu-id="c3f5d-131">yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="c3f5d-131">contacts</span></span>                        | <span data-ttu-id="c3f5d-132">Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="c3f5d-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-133">Asiakasryhmät</span><span class="sxs-lookup"><span data-stu-id="c3f5d-133">Customer groups</span></span>             | <span data-ttu-id="c3f5d-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="c3f5d-134">msdyn_customergroups</span></span>            | <span data-ttu-id="c3f5d-135">Tämä malli synkronoi asiakasryhmän tiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="c3f5d-136">Asiakkaan maksutapa</span><span class="sxs-lookup"><span data-stu-id="c3f5d-136">Customer payment method</span></span>     | <span data-ttu-id="c3f5d-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="c3f5d-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="c3f5d-138">Tämä malli synkronoi asiakkaan maksutavan tiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="c3f5d-139">Asiakkaat V3</span><span class="sxs-lookup"><span data-stu-id="c3f5d-139">Customers V3</span></span>                | <span data-ttu-id="c3f5d-140">tilit</span><span class="sxs-lookup"><span data-stu-id="c3f5d-140">accounts</span></span>                        | <span data-ttu-id="c3f5d-141">Tämä malli synkronoi asiakkaiden päätiedot kaupallisten asiakkaiden ja organisaatioasiakkaiden tiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="c3f5d-142">Asiakkaat V3</span><span class="sxs-lookup"><span data-stu-id="c3f5d-142">Customers V3</span></span>                | <span data-ttu-id="c3f5d-143">yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="c3f5d-143">contacts</span></span>                        | <span data-ttu-id="c3f5d-144">Tämä malli synkronoi asiakkaiden päätiedot kuluttajille ja loppukäyttäjille.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="c3f5d-145">Kanta-asiakaskortti</span><span class="sxs-lookup"><span data-stu-id="c3f5d-145">Loyalty card</span></span>                | <span data-ttu-id="c3f5d-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="c3f5d-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="c3f5d-147">Tämä malli synkronoi asiakkaan kanta-asiakaskortin tiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="c3f5d-148">Nimen jälkiliitteet</span><span class="sxs-lookup"><span data-stu-id="c3f5d-148">Name affixes</span></span>                | <span data-ttu-id="c3f5d-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="c3f5d-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="c3f5d-150">Tämä malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-151">CDS V2 -maksupäivärivit</span><span class="sxs-lookup"><span data-stu-id="c3f5d-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="c3f5d-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="c3f5d-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="c3f5d-153">Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-154">CDS-maksupäivät</span><span class="sxs-lookup"><span data-stu-id="c3f5d-154">Payment days CDS</span></span>            | <span data-ttu-id="c3f5d-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="c3f5d-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="c3f5d-156">Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-157">Maksusuunnitelmarivit</span><span class="sxs-lookup"><span data-stu-id="c3f5d-157">Payment schedule lines</span></span>      | <span data-ttu-id="c3f5d-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="c3f5d-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="c3f5d-159">Synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-160">Maksusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="c3f5d-160">Payment schedule</span></span>            | <span data-ttu-id="c3f5d-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="c3f5d-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="c3f5d-162">Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c3f5d-163">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="c3f5d-163">Terms of payment</span></span>            | <span data-ttu-id="c3f5d-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="c3f5d-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="c3f5d-165">Tämä malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen (maksuehdot) viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]