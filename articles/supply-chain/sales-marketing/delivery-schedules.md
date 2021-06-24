---
title: Toimitusaikataulut
description: Toimitusaikataulujen avulla voit seurata tilausrivin määrää, kun käytät useita toimituksia yksittäistä myyntitilausta, myyntitarjousta tai ostotilausta varten.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193779"
---
# <a name="delivery-schedules"></a><span data-ttu-id="4ec99-103">Toimitusaikataulut</span><span class="sxs-lookup"><span data-stu-id="4ec99-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ec99-104">Toimitusaikataulujen avulla voit seurata tilausrivin määrää, kun käytät useita toimituksia yksittäistä myyntitilausta, myyntitarjousta tai ostotilausta varten.</span><span class="sxs-lookup"><span data-stu-id="4ec99-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="4ec99-105">Toimitusaikataulua käytetään, kun tilauksen kokonaismäärä tai tarjousrivi pitää toimittaa useissa lähetyksissä.</span><span class="sxs-lookup"><span data-stu-id="4ec99-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="4ec99-106">Toimitusrivit edustavat yksittäisiä lähetyksiä.</span><span class="sxs-lookup"><span data-stu-id="4ec99-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="4ec99-107">Jos toimitusrivejä on kaksi tai useampi, ne muodostavat yhden toimitusaikataulun.</span><span class="sxs-lookup"><span data-stu-id="4ec99-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="4ec99-108">Toimitusriveillä on eri toimituspäiviä, määriä, toimitustapoja ja varastodimensioita, kuten toimipaikka ja varasto.</span><span class="sxs-lookup"><span data-stu-id="4ec99-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="4ec99-109">**Esimerkki toimitusaikataulusta**</span><span class="sxs-lookup"><span data-stu-id="4ec99-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="4ec99-110">Nimike</span><span class="sxs-lookup"><span data-stu-id="4ec99-110">Item</span></span>                              | <span data-ttu-id="4ec99-111">Arvo</span><span class="sxs-lookup"><span data-stu-id="4ec99-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="4ec99-112">Kokonaistilaus (alkuperäinen tilausrivi)</span><span class="sxs-lookup"><span data-stu-id="4ec99-112">Total order (original order line)</span></span> | <span data-ttu-id="4ec99-113">600 tuolia</span><span class="sxs-lookup"><span data-stu-id="4ec99-113">600 chairs</span></span>                               |
| <span data-ttu-id="4ec99-114">Pyydetty toimitusaikataulu</span><span class="sxs-lookup"><span data-stu-id="4ec99-114">Requested delivery schedule</span></span>       | <span data-ttu-id="4ec99-115">100 tuolia kuukaudessa</span><span class="sxs-lookup"><span data-stu-id="4ec99-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="4ec99-116">Pyydetty toimituksen aikajakso</span><span class="sxs-lookup"><span data-stu-id="4ec99-116">Requested time frame for delivery</span></span> | <span data-ttu-id="4ec99-117">6 kuukautta, kunkin kuukauden ensimmäisenä päivänä</span><span class="sxs-lookup"><span data-stu-id="4ec99-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="4ec99-118">Tässä skenaariossa asiakas pyytää toimittamaan 600 tuolia 100 tuolin erissä kuuden kuukauden ajan.</span><span class="sxs-lookup"><span data-stu-id="4ec99-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="4ec99-119">Voit seurata toimitusvaatimuksia luomalla toimitusaikataulun.</span><span class="sxs-lookup"><span data-stu-id="4ec99-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="4ec99-120">Luo Toimitusaikataulu-sivulla kuusi erillistä toimitusriviä.</span><span class="sxs-lookup"><span data-stu-id="4ec99-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="4ec99-121">Kullakin toimitusrivillä on 100 tuolia sekä niiden toimituspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="4ec99-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="4ec99-122">Tässä tapauksessa kullekin riville luodaan vastakirjaus kuukauden ensimmäisenä päivänä kuutena peräkkäisenä kuukautena.</span><span class="sxs-lookup"><span data-stu-id="4ec99-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="4ec99-123">Kun luot toimitusaikataulun, alkuperäisen tilausrivin tyypiksi vaihtuu automaattisesti **Tilausrivi ja monta toimitusta**.</span><span class="sxs-lookup"><span data-stu-id="4ec99-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="4ec99-124">Tämäntyyppistä riviä kutsutaan kaupalliseksi riviksi, ja se on merkitty kuvakkeella.</span><span class="sxs-lookup"><span data-stu-id="4ec99-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="4ec99-125">Toimitusrivi on merkitty eri kuvakkeella.</span><span class="sxs-lookup"><span data-stu-id="4ec99-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="4ec99-126">Jos muutat toimitusrivillä olevaa määrää, kaupalliselle riville päivittyy toimitusaikataulun kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="4ec99-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="4ec99-127">Jos kauppasopimuksessa tilaukselle on määritetty kokonaisalennus, toimitusaikataulu varmistaa, että tilaus on oikeutettu kokonaisalennukseen, vaikka se jaettaisiinkin erillisiin toimituksiin.</span><span class="sxs-lookup"><span data-stu-id="4ec99-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="4ec99-128">Tilaukset, joilla on toimitusaikataulu, käsitellään toimitusrivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="4ec99-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="4ec99-129">Käsittely sisältää pakkausluetteloiden, tuotteen vastaanottojen ja laskutuksen kirjaamisen.</span><span class="sxs-lookup"><span data-stu-id="4ec99-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="4ec99-130">Asiakirjatulosteissa tilauksista ja tarjouksista, joilla on toimitusaikataulu, näkyvät vain toimitusrivit.</span><span class="sxs-lookup"><span data-stu-id="4ec99-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="4ec99-131">Niillä ei näy alkuperäisiä rivejä (kaupallisia rivejä).</span><span class="sxs-lookup"><span data-stu-id="4ec99-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="4ec99-132">**Huomautus:** Lisäksi näkyvät vain toimitusrivit, kun suoritat seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="4ec99-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="4ec99-133">Julkaise</span><span class="sxs-lookup"><span data-stu-id="4ec99-133">Post</span></span>
-   <span data-ttu-id="4ec99-134">kopioit sivuja</span><span class="sxs-lookup"><span data-stu-id="4ec99-134">Copy pages</span></span>
-   <span data-ttu-id="4ec99-135">selaat luettelosivuja ja raportteja.</span><span class="sxs-lookup"><span data-stu-id="4ec99-135">Browse list pages and reports</span></span>

<span data-ttu-id="4ec99-136">Kun vahvistat myyntitarjouksia, tuloksena muodostuvissa myyntitilauksissa näkyy koko toimitusaikataulu, myös tilausrivit, joihin sisältyy useita toimituksia.</span><span class="sxs-lookup"><span data-stu-id="4ec99-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="4ec99-137">Lisäksi koko toimitusaikataulu näkyy kaikilla tärkeimmillä sivuilla, kuten myyntitilauksissa, myyntitarjouksissa ja ostotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="4ec99-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]