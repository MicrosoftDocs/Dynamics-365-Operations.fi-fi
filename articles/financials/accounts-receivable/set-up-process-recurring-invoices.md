---
title: "Aseta ja käsittele toistuvia laskuja"
description: "Tässä artikkelissa kerrotaan, miten toistuvat laskut määritetään ja miten niitä käsitellään. Voit käyttää toistuvia laskuja, jos asiakkailta laskutetaan sama summa säännöllisesti."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 96a9075294c1f2a9cfde03be1aaaa26af90de4c2
ms.openlocfilehash: ac9e836b0baa24c40554844ea4f3288b80e0c654
ms.contentlocale: fi-fi
ms.lasthandoff: 09/04/2018

---

# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="0eb12-104">Aseta ja käsittele toistuvia laskuja</span><span class="sxs-lookup"><span data-stu-id="0eb12-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0eb12-105">Tässä artikkelissa kerrotaan, miten toistuvat laskut määritetään ja miten niitä käsitellään.</span><span class="sxs-lookup"><span data-stu-id="0eb12-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="0eb12-106">Voit käyttää toistuvia laskuja, jos asiakkailta laskutetaan sama summa säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="0eb12-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="0eb12-107">Luo malli toistuville vapaatekstilaskuille</span><span class="sxs-lookup"><span data-stu-id="0eb12-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="0eb12-108">Laskuttaaksesi samoja säännöllisin väliajoin palveluita käyttäviä asiakkaita, on määritettävä vapaa tekstimuotoinen laskutusmalli, jota voidaan käyttää uudelleen laskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="0eb12-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="0eb12-109">Tämä malli sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="0eb12-109">This template contains the following information:</span></span>

-   <span data-ttu-id="0eb12-110">Otsikkotiedot, kuten veroryhmät, maksuehdot ja maksutapa</span><span class="sxs-lookup"><span data-stu-id="0eb12-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="0eb12-111">Rivin tietoja, kuten palvelun kuvaus, tulostilit, yksikköhinta ja laskutussumma</span><span class="sxs-lookup"><span data-stu-id="0eb12-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="0eb12-112">Toimitus-tai käsittelymaksut</span><span class="sxs-lookup"><span data-stu-id="0eb12-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="0eb12-113">Kirjanpidolliset jaot sekä taloushallinnon dimension tiedot, kuten kustannuspaikat ja liiketoimintayksiköt</span><span class="sxs-lookup"><span data-stu-id="0eb12-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="0eb12-114">Itse asiassa luot koko laskun ja tallennat sen mallina.</span><span class="sxs-lookup"><span data-stu-id="0eb12-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="0eb12-115">Voit määrittää mallit käyttämällä **toistuvat laskut** -sivuja.</span><span class="sxs-lookup"><span data-stu-id="0eb12-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="0eb12-116">Määritä vapaatekstilaskun malli asiakkaalle ja syötä toistuvat yksityiskohdat</span><span class="sxs-lookup"><span data-stu-id="0eb12-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="0eb12-117">Mallin luonnin jälkeen malli on määritettävä niille asiakkaille, joita haluat laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="0eb12-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="0eb12-118">Lisäksi, sinun on määritettävä milloin ja kuinka usein laskua käytetään.</span><span class="sxs-lookup"><span data-stu-id="0eb12-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="0eb12-119">Voit määrittää malleja **lasku**-välilehdessä **asiakkaat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0eb12-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="0eb12-120">Lisää malli luetteloon ja päivitä seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="0eb12-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="0eb12-121">Alkamispäivämäärä ja halutessasi päättymispäivä toistuvaa laskutusta varten</span><span class="sxs-lookup"><span data-stu-id="0eb12-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="0eb12-122">Toistuvan laskutuksen käyttötiheys (esimerkiksi päivittäin tai kerran kuussa)</span><span class="sxs-lookup"><span data-stu-id="0eb12-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="0eb12-123">Laskutuksen enimmäissumma (jos tämä on pakollinen määritys)</span><span class="sxs-lookup"><span data-stu-id="0eb12-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="0eb12-124">Asiakkaalla voi olla useita malleja, joilla on eri maksutiheydet.</span><span class="sxs-lookup"><span data-stu-id="0eb12-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="0eb12-125">Luo toistuvat laskut</span><span class="sxs-lookup"><span data-stu-id="0eb12-125">Generate the recurring invoices</span></span>
<span data-ttu-id="0eb12-126">**Toistuvat laskut**-sivulla on tehtävä, joka käsittelee toistuvien laskujen malleja.</span><span class="sxs-lookup"><span data-stu-id="0eb12-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="0eb12-127">Määritä laskutuspäivämäärä ja malli laskujen luontia varten.</span><span class="sxs-lookup"><span data-stu-id="0eb12-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="0eb12-128">Laskut luodaan ja jokaiselle käsiteltävälle laskutusryhmälle määritetään yksi toistuva tunnusnumero.</span><span class="sxs-lookup"><span data-stu-id="0eb12-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="0eb12-129">Kirjaa toistuvat vapaatekstilaskut</span><span class="sxs-lookup"><span data-stu-id="0eb12-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="0eb12-130">Sen jälkeen kun toistuvat laskut on luotu, laskun toistuvat tunnukset näkyvät kirjaustehtävässä **toistuvat laskut**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0eb12-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="0eb12-131">Voit tarkastella kaikkia laskuja toistuvalle tunnukselle napsauttamalla linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0eb12-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="0eb12-132">Voit poistaa yksittäisiä laskuja toituvan tunnuksen laskujen tarkistuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="0eb12-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="0eb12-133">Asiakkaan toistumisasetukset palautetaan kyseiseen malliin niin, että se voidaan ottaa esille myöhemmin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0eb12-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="0eb12-134">Voit kirjata yhden, useita tai kaikki laskut toistuvalla tunnuksella.</span><span class="sxs-lookup"><span data-stu-id="0eb12-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="0eb12-135">Jos työnkulkuja on otettu käyttöön, sinun on valittava **lähetä** ennen kuin voit kirjata laskut.</span><span class="sxs-lookup"><span data-stu-id="0eb12-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="0eb12-136">Tulosta toistuvat vapaatekstilaskut</span><span class="sxs-lookup"><span data-stu-id="0eb12-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="0eb12-137">Sen jälkeen kun toistuvat laskut on kirjattu, voit tulostaa laskuja vapaan tekstimuotoisen laskun luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="0eb12-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="0eb12-138">Voit tulostaa laskut, jotka on valittu tai voit valita mitkä laskut haluat tulostaa.</span><span class="sxs-lookup"><span data-stu-id="0eb12-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>




