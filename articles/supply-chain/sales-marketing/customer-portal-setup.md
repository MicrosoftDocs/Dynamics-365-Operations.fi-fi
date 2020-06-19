---
title: Asiakasportaalin asentaminen, määrittäminen ja päivittäminen
description: Tässä ohjeaiheessa on asiakasportaalin käyttöoikeustiedot ja asennusohjeet.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b9d1e742f78254d949dc49fda008d63b8bff4d65
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413958"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="6ac8d-103">Asiakasportaalin asentaminen, määrittäminen ja päivittäminen</span><span class="sxs-lookup"><span data-stu-id="6ac8d-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="6ac8d-104">Käyttöoikeusvaatimukset</span><span class="sxs-lookup"><span data-stu-id="6ac8d-104">Licensing requirements</span></span>

<span data-ttu-id="6ac8d-105">Asiakasportaalin käyttöönotto edellyttää, että sinulla on seuraavat käyttöoikeudet:</span><span class="sxs-lookup"><span data-stu-id="6ac8d-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="6ac8d-106">**Power Apps -portaalit** – Asiakasportaalin isännöintiin tarvitaan tämä käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="6ac8d-107">Portaalien käyttöoikeus perustuu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="6ac8d-108">Lisätietoja on kohdassa [Power Apps -portaalien käyttöoikeussopimuksen vaatimukset](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="6ac8d-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="6ac8d-109">**Kaksoiskirjoitus** – Sinulla on oltava tarvittavat käyttöoikeudet, jotta voit ottaa käyttöön Supply Chain Management -yksiköiden kaksoiskirjoituksen.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="6ac8d-110">Lisätietoja on kohdassa [kaksoiskirjoituksen järjestelmävaatimukset](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="6ac8d-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="6ac8d-111">Kaksoiskirjoituksen riippuvaisuudet ja Power Apps -portaalit</span><span class="sxs-lookup"><span data-stu-id="6ac8d-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="6ac8d-112">Asiakasportaali on riippuvainen Power Apps -portaaleista ja kaksoiskirjoittamisesta, kuten seuraavasta kuvasta näkyy.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

![![Asiakasportaalin riippuvuudet](media/customer-portal-elements.png "Asiakasportaalin riippuvuudet")](media/customer-portal-elements.png "Customer portal dependencies")

<span data-ttu-id="6ac8d-114">Toisin kuin muut Supply Chain Managementin ominaisuudet, asiakasportaalimalli sijaitsee Power Apps -portaaleissa.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="6ac8d-115">Tämän vuoksi asiakasportaalia rajoittaa Power Apps -portaalien ja kaksoiskirjoitusyritysten tarjoamat toiminnot ja ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="6ac8d-116">Asiakasportaalin käyttöön tarvittavat määritykset</span><span class="sxs-lookup"><span data-stu-id="6ac8d-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="6ac8d-117">Kun olet varma, että sinulla on tarvittavat käyttöoikeudet, voit määrittää kaksoiskirjoitustiedot, jotka on kuvattu kohdassa [kaksoiskirjoituksen alkuperäiset synkronointiohjeet](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="6ac8d-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="6ac8d-118">Muista ottaa seuraavat entiteettien yhdistämismääritykset käyttöön kaksoiskirjoitustilanteissa:</span><span class="sxs-lookup"><span data-stu-id="6ac8d-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="6ac8d-119">Myyntitilauksen otsikko</span><span class="sxs-lookup"><span data-stu-id="6ac8d-119">Sales Order Header</span></span>
- <span data-ttu-id="6ac8d-120">Myyntitilauksen tiedot</span><span class="sxs-lookup"><span data-stu-id="6ac8d-120">Sales Order Details</span></span>
- <span data-ttu-id="6ac8d-121">Tilit</span><span class="sxs-lookup"><span data-stu-id="6ac8d-121">Accounts</span></span>
- <span data-ttu-id="6ac8d-122">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="6ac8d-122">Contacts</span></span>
- <span data-ttu-id="6ac8d-123">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="6ac8d-123">Products</span></span>

<span data-ttu-id="6ac8d-124">Kun nämä määritykset on tehty, voit määrittää asiakasportaalin mallipohjan.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="6ac8d-125">Asiakasportaalin valmistelu</span><span class="sxs-lookup"><span data-stu-id="6ac8d-125">Provision the Customer portal</span></span>

<span data-ttu-id="6ac8d-126">Varmista ennen aloittamista, että olet jo määrittänyt [tarvittavat määritykset](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="6ac8d-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="6ac8d-127">Valmistele sitten asiakasportaali noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="6ac8d-128">Siirry kohtaan [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="6ac8d-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="6ac8d-129">Varmista, että käytät ympäristöä, jossa kaksoiskirjoitus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="6ac8d-130">Vieritä **Luo**-välilehdessä alaspäin **Aloita mallista** -osasta ja valitse malli, jonka nimi on **Supply Chain Managementin asiakas**.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Supply Chain Management Customer**.</span></span>
4. <span data-ttu-id="6ac8d-131">Noudata näytön ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="6ac8d-132">Kun valmistelu on tehty, voit käyttää asiakas portaalia **Koti**-sivun **Sovellukset**-osiossa.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="6ac8d-133">Jos kaksoiskirjoitusratkaisua ei asenneta ympäristössä, jossa työskentelet, näyttöön tulee virhesanoma eikä asiakasportaalia valmistella.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="6ac8d-134">Asiakasportaalin päivitys</span><span class="sxs-lookup"><span data-stu-id="6ac8d-134">Update the Customer portal</span></span>

<span data-ttu-id="6ac8d-135">Asiakasportaaliin voidaan lisätä toimintoja myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="6ac8d-136">Kaikki Microsoftin pohjana olevan ratkaisun komponentteihin tekemät muutokset tulevat automaattisesti näkyviin ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="6ac8d-137">Ympäristössäsi valmisteltu verkkosivusto ei kuitenkaan automaattisesti vastaa määritystietoihin tehtyjä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="6ac8d-138">Sinun on sovellettava näitä muutoksia manuaalisesti, jotta saat uuden mallin koodin ja voit yhdistää sen valmistellulla verkkosivustolla.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="resources"></a><span data-ttu-id="6ac8d-139">Resurssit</span><span class="sxs-lookup"><span data-stu-id="6ac8d-139">Resources</span></span>

<span data-ttu-id="6ac8d-140">Jos haluat tietää, miten asiakasportaali voidaan määrittää ja mukauttaa, aloita tarkastelemalla seuraavia tekniikoita koskevia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="6ac8d-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="6ac8d-141">Power Apps -portaalit -dokumentaatio</span><span class="sxs-lookup"><span data-stu-id="6ac8d-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="6ac8d-142">Kaksoiskirjoituksen dokumentointi</span><span class="sxs-lookup"><span data-stu-id="6ac8d-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="6ac8d-143">Portaalien tehokas hallinta edellyttää, että ymmärrät Power Apps -portaaleja ja Common Data Service -elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="6ac8d-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="6ac8d-144">Lisätietoja on seuraavissa resursseissa:</span><span class="sxs-lookup"><span data-stu-id="6ac8d-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="6ac8d-145">Tietoja portaalin elinkaaresta</span><span class="sxs-lookup"><span data-stu-id="6ac8d-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="6ac8d-146">Portaalin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="6ac8d-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="6ac8d-147">Portaalin konfiguraation siirtäminen</span><span class="sxs-lookup"><span data-stu-id="6ac8d-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="6ac8d-148">Ratkaisun elinkaaren hallinta: Dynamics 365 for Customer Engagement -sovellukset</span><span class="sxs-lookup"><span data-stu-id="6ac8d-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
