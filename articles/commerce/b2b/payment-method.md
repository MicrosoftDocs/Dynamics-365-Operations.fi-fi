---
title: Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille
description: Tässä aiheessa kuvataan, kuinka asiakastilin maksutapa konfiguroidaan yritysten välisissä (B2B) verkkokauppasivustoissa.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035901"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="05cab-103">Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="05cab-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05cab-104">Tässä aiheessa kuvataan, kuinka asiakastilin maksutapa konfiguroidaan yritysten välisissä (B2B) verkkokauppasivustoissa.</span><span class="sxs-lookup"><span data-stu-id="05cab-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="05cab-105">Vähittäismyyjät voivat hyväksyä useantyyppisiä maksutapoja verkkokauppakanavissaan myymistään tuotteista ja palveluista.</span><span class="sxs-lookup"><span data-stu-id="05cab-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="05cab-106">Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä Microsoft Dynamics 365 Commercessa, kun järjestelmä määritetään.</span><span class="sxs-lookup"><span data-stu-id="05cab-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="05cab-107">Asiakastilin (tai tilillä olevan) maksutavan on oltava tuettuna B2B-verkkokauppasivustoissa.</span><span class="sxs-lookup"><span data-stu-id="05cab-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="05cab-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="05cab-108">Prerequisites</span></span>

1. <span data-ttu-id="05cab-109">Lisää asiakastilin maksutapa Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="05cab-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="05cab-110">Liitä asiakastilin maksutapa sähköistä kaupankäyntikanavaa varten.</span><span class="sxs-lookup"><span data-stu-id="05cab-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="05cab-111">Varmista, että **Salli ennakkomaksu** on käytössä asiakkaalle Commerce headquarters -sovelluksessa kohdassa **Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat \> Maksujen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="05cab-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="05cab-112">Varmista myös, että **Luottoraja**-parametrit on määritetty oikein asiakkaalle Commerce headquarters -sovelluksen kohdassa **Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat \> Luotonvalvonta**.</span><span class="sxs-lookup"><span data-stu-id="05cab-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="05cab-113">Asiakastilin maksutavan ottaminen käyttöön Commercen sivustonmuodostimessa</span><span class="sxs-lookup"><span data-stu-id="05cab-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="05cab-114">Saat asiakastilin maksutavan otettua käyttöön Commercen sivustonmuodostimessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="05cab-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="05cab-115">Siirry kohtaan **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="05cab-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="05cab-116">Määritä **Ota käyttöön asiakastilin maksut** -ominaisuuden arvoksi **Käytössä B2B-asiakkaille**.</span><span class="sxs-lookup"><span data-stu-id="05cab-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="05cab-117">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="05cab-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="05cab-118">Uudet sivuston asetukset tulevat voimaan vasta, kun app.settings.json-tiedosto on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="05cab-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="05cab-119">Lisätietoja on ohjeaiheessa [SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="05cab-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="05cab-120">Asiakastilin maksutavan ottaminen käyttöön B2B-verkkokauppasivuston uloskuittaussivulla</span><span class="sxs-lookup"><span data-stu-id="05cab-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="05cab-121">Saat asiakastilin maksutavan otettua käyttöön B2B-verkkokauppasivuston uloskuittaussivulla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="05cab-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="05cab-122">Etsi ja muokkaa Commercen sivustonmuodostintyökalussa uloskuittaussivu tai katkelmassa, joka sisältää B2B-verkkokauppasivuston uloskuittausmoduulin.</span><span class="sxs-lookup"><span data-stu-id="05cab-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="05cab-123">Valitse **Kassaosiokontti**-paikassa **Lisää moduuli** ja lisää sitten **Asiakastilin maksu** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="05cab-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="05cab-124">Aseta **Asiakastilin maksu** -moduuli valitsemalla kolme pistettä (**...**) ja valitsemalla sitten **Siirrä ylös** tai **Siirrä alas** tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="05cab-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="05cab-125">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="05cab-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="05cab-126">Vahvista, että asiakastilin maksutapa on otettu käyttöön ja julkaistu</span><span class="sxs-lookup"><span data-stu-id="05cab-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="05cab-127">Voit vahvistaa, että asiakastilin maksutapa on otettu käyttöön ja julkaistu, seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="05cab-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="05cab-128">Kirjaudu sisään verkkokauppasivustoon.</span><span class="sxs-lookup"><span data-stu-id="05cab-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="05cab-129">Lisää tuote ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="05cab-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="05cab-130">Siirry kassasivulle.</span><span class="sxs-lookup"><span data-stu-id="05cab-130">Go to the checkout page.</span></span> <span data-ttu-id="05cab-131">Tässä pitäisi näkyä uusi **Asiakastili**-maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="05cab-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05cab-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="05cab-132">Additional resources</span></span>

[<span data-ttu-id="05cab-133">B2B-verkkokauppasivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="05cab-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="05cab-134">Organisaation mallinnushierarkioiden luominen B2B-organisaatioille</span><span class="sxs-lookup"><span data-stu-id="05cab-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="05cab-135">Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa</span><span class="sxs-lookup"><span data-stu-id="05cab-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="05cab-136">Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="05cab-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="05cab-137">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="05cab-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)
