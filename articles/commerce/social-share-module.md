---
title: Jako yhteisöpalveluissa -moduuli
description: Tässä ohjeaiheessa on tietoja yhteisöpalveluissa jaon moduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234314"
---
# <a name="social-share-module"></a><span data-ttu-id="520d1-103">Yhteisöpalvelujakamisen moduuli</span><span class="sxs-lookup"><span data-stu-id="520d1-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="520d1-104">Tässä ohjeaiheessa on tietoja yhteisöpalveluissa jaon moduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="520d1-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="520d1-105">Jako yhteisöpalveluissa -moduulien avulla käyttäjät voivat jakaa sähköisen kaupankäynnin sivuston sivujen URL-osoitteita yhteisöpalveluissa, kuten Facebookissa, Twitterissä, Pinterestissä ja LinkedInissä.</span><span class="sxs-lookup"><span data-stu-id="520d1-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="520d1-106">Sivuston sivun URL-osoitteita voi jakaa myös sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="520d1-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="520d1-107">Jako yhteisöpalveluissa -moduuleja käytetään yleisesti tuotetietosivuilla (PDP-sivuilla). Niiden avulla käyttäjät voivat jakaa tuotetietoja.</span><span class="sxs-lookup"><span data-stu-id="520d1-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="520d1-108">Kunkin Jako yhteisöpalveluissa -moduuli on säilö yhteisöpalveluiden jaon nimikkeiden moduuleille.</span><span class="sxs-lookup"><span data-stu-id="520d1-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="520d1-109">Kukin Jako yhteisöpalveluissa -nimikkeen moduuli voidaan määrittää niin, että se osoittaa tiettyyn yhteisöpalvelun sivustoon.</span><span class="sxs-lookup"><span data-stu-id="520d1-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="520d1-110">Integrointia Facebookin, Twitterin, Pinterestin, LinkedInin ja sähköpostin kanssa tuetaan. Se on valmis ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="520d1-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="520d1-111">Kun sivuston käyttäjä valitsee yhteisöpalvelun synbolin, vastaavassa yhteisöpalvelun sivustossa käynnistetään HTML-muotoinen iFrame-kehys.</span><span class="sxs-lookup"><span data-stu-id="520d1-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="520d1-112">IFrame-kehyksessä käyttäjä voi kirjautua sisään ja näyttää katsomansa sivun sisällön.</span><span class="sxs-lookup"><span data-stu-id="520d1-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="520d1-113">Kukin yhteisöpalvelun ympäristö voi seurata evästeitä. Tämä moduuli vaatii siis sivuston käyttäjiä hyväksymään evästeet. Tästä kerrotaan suostumuksesta kertovassa ilmoituksessa.</span><span class="sxs-lookup"><span data-stu-id="520d1-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="520d1-114">Kun evästeille ei anneta hyväksyntää, moduuli piilotetaan sivulla.</span><span class="sxs-lookup"><span data-stu-id="520d1-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="520d1-115">Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="520d1-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="520d1-116">Seuraavassa kuvassa on esimerkki tuotetietosivulla käytetystä Jako yhteisöpalveluissa -moduulista.</span><span class="sxs-lookup"><span data-stu-id="520d1-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Esimerkki Jako yhteisöpalveluissa -moduulista](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="520d1-118">Jako yhteisöpalveluissa -moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="520d1-118">Social share module properties</span></span>

| <span data-ttu-id="520d1-119">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="520d1-119">Property name</span></span>             | <span data-ttu-id="520d1-120">Arvo</span><span class="sxs-lookup"><span data-stu-id="520d1-120">Value</span></span>                 | <span data-ttu-id="520d1-121">kuvaus</span><span class="sxs-lookup"><span data-stu-id="520d1-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="520d1-122">Otsikko</span><span class="sxs-lookup"><span data-stu-id="520d1-122">Caption</span></span>                  | <span data-ttu-id="520d1-123">Teksti</span><span class="sxs-lookup"><span data-stu-id="520d1-123">Text</span></span> | <span data-ttu-id="520d1-124">Tämä ominaisuus määrittää moduulin kuvatekstin.</span><span class="sxs-lookup"><span data-stu-id="520d1-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="520d1-125">Suunta</span><span class="sxs-lookup"><span data-stu-id="520d1-125">Orientation</span></span> | <span data-ttu-id="520d1-126">**Vaaka** tai **pysty**</span><span class="sxs-lookup"><span data-stu-id="520d1-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="520d1-127">Tämä ominaisuus määrittää yhteisöpalveluiden nimikkeiden asettelun suunnan.</span><span class="sxs-lookup"><span data-stu-id="520d1-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="520d1-128">Jako yhteisöpalveluissa -nimikkeen moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="520d1-128">Social share item module properties</span></span>
| <span data-ttu-id="520d1-129">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="520d1-129">Property name</span></span>             | <span data-ttu-id="520d1-130">Arvo</span><span class="sxs-lookup"><span data-stu-id="520d1-130">Value</span></span>                 | <span data-ttu-id="520d1-131">kuvaus</span><span class="sxs-lookup"><span data-stu-id="520d1-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="520d1-132">Yhteisöpalvelut</span><span class="sxs-lookup"><span data-stu-id="520d1-132">Social media</span></span>              | <span data-ttu-id="520d1-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **sähköposti**</span><span class="sxs-lookup"><span data-stu-id="520d1-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="520d1-134">Avattava valikko, jossa on luettelo yhteisöpalvelun ympäristöistä.</span><span class="sxs-lookup"><span data-stu-id="520d1-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="520d1-135">Kuvake</span><span class="sxs-lookup"><span data-stu-id="520d1-135">Icon</span></span> |<span data-ttu-id="520d1-136">Kuva</span><span class="sxs-lookup"><span data-stu-id="520d1-136">Image</span></span>    | <span data-ttu-id="520d1-137">Tässä on kuva, joka näkyy vastaava yhteisöpalvelu.</span><span class="sxs-lookup"><span data-stu-id="520d1-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="520d1-138">Tietoja kunkin ympäristön kuvan käyttämisen parhaasta käytännöstä on yhteisöpalvelun ympäristön SDK:ssa.</span><span class="sxs-lookup"><span data-stu-id="520d1-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="520d1-139">Jako yhteisöpalveluissa -moduulin lisääminen ostoruutumoduuliin</span><span class="sxs-lookup"><span data-stu-id="520d1-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="520d1-140">Jos haluat lisätä Jako yhteisöpalveluissa -moduulin ostoruutumoduuliin, tee seuraavat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="520d1-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="520d1-141">Valitse Fabrikam-sivustossa **Sivut** ja valitse sitten **DefaultPDP**-sivu. Avaa tuotetietosivu.</span><span class="sxs-lookup"><span data-stu-id="520d1-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="520d1-142">Valitse kolme pistettä (**...**) **Ostoruutu (pakollinen)** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="520d1-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="520d1-143">Valitse **Lisää moduuli** -valintaikkunassa **Jako yhteisöpalvelussa** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="520d1-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="520d1-144">Valitse kolme pistettä (**...**) **Jako yhteisöpalveluissa** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="520d1-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="520d1-145">Valitse **Lisää moduuli** -valintaikkunassa **SocialShare**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="520d1-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="520d1-146">Valitse **SocialShare**-moduulin ominaisuusikkunan **Suunta**-kohdassa **Vaaka**.</span><span class="sxs-lookup"><span data-stu-id="520d1-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="520d1-147">Lisää kuvateksti tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="520d1-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="520d1-148">Valitse kolme pistettä (**...**) **SocialShare**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="520d1-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="520d1-149">Valitse **Lisää moduuli** -valintaikkunassa **SocialShareItem**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="520d1-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="520d1-150">Valitse **SocialShareItem**-moduulin ominaisuusikkunan **Yhteisöpalvelut**-kohdassa **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="520d1-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="520d1-151">Valitse **SocialShareItem**-moduulin ominaisuusikkunan **Kuvake**-kohdassa **+ Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="520d1-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="520d1-152">Valitse **Mediasisällön valitsin** -valintaruudussa Facebook-logokuva ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="520d1-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="520d1-153">Jos Facebook-logokuvaa ei ole valittavissa, valitse **Lataa uusi medianimike** ja lataa logokuva.</span><span class="sxs-lookup"><span data-stu-id="520d1-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="520d1-154">Lisää **SocialShareItem**-moduuleja ja määritä niitä lisää tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="520d1-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="520d1-155">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="520d1-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="520d1-156">Sivulla näkyy Jako yhteisöpalveluissa -moduuli.</span><span class="sxs-lookup"><span data-stu-id="520d1-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="520d1-157">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="520d1-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="520d1-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="520d1-158">Additional resources</span></span>

[<span data-ttu-id="520d1-159">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="520d1-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="520d1-160">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="520d1-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="520d1-161">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="520d1-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]