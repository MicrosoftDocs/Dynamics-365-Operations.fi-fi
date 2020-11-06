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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022073"
---
# <a name="social-share-module"></a><span data-ttu-id="77fda-103">Jako yhteisöpalveluissa -moduuli</span><span class="sxs-lookup"><span data-stu-id="77fda-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77fda-104">Tässä ohjeaiheessa on tietoja yhteisöpalveluissa jaon moduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="77fda-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="77fda-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="77fda-105">Overview</span></span>

<span data-ttu-id="77fda-106">Jako yhteisöpalveluissa -moduulien avulla käyttäjät voivat jakaa sähköisen kaupankäynnin sivuston sivujen URL-osoitteita yhteisöpalveluissa, kuten Facebookissa, Twitterissä, Pinterestissä ja LinkedInissä.</span><span class="sxs-lookup"><span data-stu-id="77fda-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="77fda-107">Sivuston sivun URL-osoitteita voi jakaa myös sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="77fda-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="77fda-108">Jako yhteisöpalveluissa -moduuleja käytetään yleisesti tuotetietosivuilla (PDP-sivuilla). Niiden avulla käyttäjät voivat jakaa tuotetietoja.</span><span class="sxs-lookup"><span data-stu-id="77fda-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="77fda-109">Kunkin Jako yhteisöpalveluissa -moduuli on säilö yhteisöpalveluiden jaon nimikkeiden moduuleille.</span><span class="sxs-lookup"><span data-stu-id="77fda-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="77fda-110">Kukin Jako yhteisöpalveluissa -nimikkeen moduuli voidaan määrittää niin, että se osoittaa tiettyyn yhteisöpalvelun sivustoon.</span><span class="sxs-lookup"><span data-stu-id="77fda-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="77fda-111">Integrointia Facebookin, Twitterin, Pinterestin, LinkedInin ja sähköpostin kanssa tuetaan. Se on valmis ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="77fda-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="77fda-112">Kun sivuston käyttäjä valitsee yhteisöpalvelun synbolin, vastaavassa yhteisöpalvelun sivustossa käynnistetään HTML-muotoinen iFrame-kehys.</span><span class="sxs-lookup"><span data-stu-id="77fda-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="77fda-113">IFrame-kehyksessä käyttäjä voi kirjautua sisään ja näyttää katsomansa sivun sisällön.</span><span class="sxs-lookup"><span data-stu-id="77fda-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="77fda-114">Kukin yhteisöpalvelun ympäristö voi seurata evästeitä. Tämä moduuli vaatii siis sivuston käyttäjiä hyväksymään evästeet. Tästä kerrotaan suostumuksesta kertovassa ilmoituksessa.</span><span class="sxs-lookup"><span data-stu-id="77fda-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="77fda-115">Kun evästeille ei anneta hyväksyntää, moduuli piilotetaan sivulla.</span><span class="sxs-lookup"><span data-stu-id="77fda-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="77fda-116">Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="77fda-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="77fda-117">Seuraavassa kuvassa on esimerkki tuotetietosivulla käytetystä Jako yhteisöpalveluissa -moduulista.</span><span class="sxs-lookup"><span data-stu-id="77fda-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Esimerkki Jako yhteisöpalveluissa -moduulista](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="77fda-119">Jako yhteisöpalveluissa -moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="77fda-119">Social share module properties</span></span>

| <span data-ttu-id="77fda-120">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="77fda-120">Property name</span></span>             | <span data-ttu-id="77fda-121">Arvo</span><span class="sxs-lookup"><span data-stu-id="77fda-121">Value</span></span>                 | <span data-ttu-id="77fda-122">kuvaus</span><span class="sxs-lookup"><span data-stu-id="77fda-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="77fda-123">Otsikko</span><span class="sxs-lookup"><span data-stu-id="77fda-123">Caption</span></span>                  | <span data-ttu-id="77fda-124">Teksti</span><span class="sxs-lookup"><span data-stu-id="77fda-124">Text</span></span> | <span data-ttu-id="77fda-125">Tämä ominaisuus määrittää moduulin kuvatekstin.</span><span class="sxs-lookup"><span data-stu-id="77fda-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="77fda-126">Suunta</span><span class="sxs-lookup"><span data-stu-id="77fda-126">Orientation</span></span> | <span data-ttu-id="77fda-127">**Vaaka** tai **pysty**</span><span class="sxs-lookup"><span data-stu-id="77fda-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="77fda-128">Tämä ominaisuus määrittää yhteisöpalveluiden nimikkeiden asettelun suunnan.</span><span class="sxs-lookup"><span data-stu-id="77fda-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="77fda-129">Jako yhteisöpalveluissa -nimikkeen moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="77fda-129">Social share item module properties</span></span>
| <span data-ttu-id="77fda-130">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="77fda-130">Property name</span></span>             | <span data-ttu-id="77fda-131">Arvo</span><span class="sxs-lookup"><span data-stu-id="77fda-131">Value</span></span>                 | <span data-ttu-id="77fda-132">kuvaus</span><span class="sxs-lookup"><span data-stu-id="77fda-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="77fda-133">Yhteisöpalvelut</span><span class="sxs-lookup"><span data-stu-id="77fda-133">Social media</span></span>              | <span data-ttu-id="77fda-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **sähköposti**</span><span class="sxs-lookup"><span data-stu-id="77fda-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span></span> | <span data-ttu-id="77fda-135">Avattava valikko, jossa on luettelo yhteisöpalvelun ympäristöistä.</span><span class="sxs-lookup"><span data-stu-id="77fda-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="77fda-136">Kuvake</span><span class="sxs-lookup"><span data-stu-id="77fda-136">Icon</span></span> |<span data-ttu-id="77fda-137">Kuva</span><span class="sxs-lookup"><span data-stu-id="77fda-137">Image</span></span>    | <span data-ttu-id="77fda-138">Tässä on kuva, joka näkyy vastaava yhteisöpalvelu.</span><span class="sxs-lookup"><span data-stu-id="77fda-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="77fda-139">Tietoja kunkin ympäristön kuvan käyttämisen parhaasta käytännöstä on yhteisöpalvelun ympäristön SDK:ssa.</span><span class="sxs-lookup"><span data-stu-id="77fda-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="77fda-140">Jako yhteisöpalveluissa -moduulin lisääminen ostoruutumoduuliin</span><span class="sxs-lookup"><span data-stu-id="77fda-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="77fda-141">Jos haluat lisätä Jako yhteisöpalveluissa -moduulin ostoruutumoduuliin, tee seuraavat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="77fda-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="77fda-142">Valitse Fabrikam-sivustossa **Sivut** ja valitse sitten **DefaultPDP** -sivu. Avaa tuotetietosivu.</span><span class="sxs-lookup"><span data-stu-id="77fda-142">In the Fabrikam site, select **Pages** , and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="77fda-143">Valitse kolme pistettä ( **...** ) **Ostoruutu (pakollinen)** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="77fda-143">In the **Buybox (required)** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77fda-144">Valitse **Lisää moduuli** -valintaikkunassa **Jako yhteisöpalvelussa** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="77fda-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="77fda-145">Valitse kolme pistettä ( **...** ) **Jako yhteisöpalveluissa** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="77fda-145">In the **Social Share** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77fda-146">Valitse **Lisää moduuli** -valintaikkunassa **SocialShare** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="77fda-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="77fda-147">Valitse **SocialShare** -moduulin ominaisuusikkunan **Suunta** -kohdassa **Vaaka**.</span><span class="sxs-lookup"><span data-stu-id="77fda-147">In the properties pane of the **SocialShare** module, under **Orientation** , select **Horizontal**.</span></span> <span data-ttu-id="77fda-148">Lisää kuvateksti tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="77fda-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="77fda-149">Valitse kolme pistettä ( **...** ) **SocialShare** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="77fda-149">In the **SocialShare** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77fda-150">Valitse **Lisää moduuli** -valintaikkunassa **SocialShareItem** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="77fda-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="77fda-151">Valitse **SocialShareItem** -moduulin ominaisuusikkunan **Yhteisöpalvelut** -kohdassa **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="77fda-151">In the properties pane of the **SocialShareItem** module, under **Social Media** , select **Facebook**.</span></span>
1. <span data-ttu-id="77fda-152">Valitse **SocialShareItem** -moduulin ominaisuusikkunan **Kuvake** -kohdassa **+ Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="77fda-152">In the properties pane of the **SocialShareItem** module, under **Icon** , select **+ Add an image**.</span></span>
1. <span data-ttu-id="77fda-153">Valitse **Mediasisällön valitsin** -valintaruudussa Facebook-logokuva ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="77fda-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="77fda-154">Jos Facebook-logokuvaa ei ole valittavissa, valitse **Lataa uusi medianimike** ja lataa logokuva.</span><span class="sxs-lookup"><span data-stu-id="77fda-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="77fda-155">Lisää **SocialShareItem** -moduuleja ja määritä niitä lisää tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="77fda-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="77fda-156">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="77fda-156">Select **Save** , and then select **Preview** to preview the page.</span></span> <span data-ttu-id="77fda-157">Sivulla näkyy Jako yhteisöpalveluissa -moduuli.</span><span class="sxs-lookup"><span data-stu-id="77fda-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="77fda-158">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="77fda-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77fda-159">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="77fda-159">Additional resources</span></span>

[<span data-ttu-id="77fda-160">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="77fda-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="77fda-161">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="77fda-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="77fda-162">Evästeen yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="77fda-162">Cookie compliance</span></span>](cookie-compliance.md)
