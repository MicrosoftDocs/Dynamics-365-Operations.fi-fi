---
title: Sähköpostiasetusten määrittäminen Microsoft Dynamics 365 Talent – Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Attractista lähetettävien sähköpostien asetusten määrittämistä.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a457deec757a5d5a3e01c6903b2dd7a9d975ef0b
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551538"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="a5c7f-103">Sähköpostiasetusten määrittäminen Microsoft Dynamics 365 Talent – Attractissa</span><span class="sxs-lookup"><span data-stu-id="a5c7f-103">Configure email settings in Microsoft Dynamics 365 Talent - Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5c7f-104">Brändisi kasvattaa luottamusta ja auttaa luomaan suhteen ehdokkaisiin, ennen kuin he hakeva työpaikkaa.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="a5c7f-105">Positiivinen mielikuva brändistä houkuttelee parhaat työhakijat ja parantaa nykyisten työntekijöiden uskollisuutta.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="a5c7f-106">Microsoft Dynamics 365 Talent: Attractin avulla voit määrittää sähköpostit yrityksen brändin mukaisiksi.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="a5c7f-107">Tällä tavoin työpaikkaa hakevien kokemus pysyy yhtenäisenä koko hakuprosessin ajan.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="a5c7f-108">Attractin avulla voi tehdä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="a5c7f-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="a5c7f-109">Sähköpostiasetusten määrittäminen käyttämään yrityksen Microsoft Exchange -sähköpostipalvelun tiliä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="a5c7f-110">Tällä tavoin hakijat tietävät, että heidän sähköpostinsa ovat yrityksen lähettämiä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="a5c7f-111">Voit määrittää asetukset esimerkiksi siten, että hakijat saavat sähköpostia osoitteesta `recruiting@contoso.com` eikä `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="a5c7f-112">Yhtenäisen brändin luominen kaikelle sähköpostiviestinnälle määrittämällä yleinen ylä- ja alatunniste kaikkiin sähköpostimalleihin.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="a5c7f-113">Attractin määrittäminen käyttämään sähköpostin lähettämiseen yrityksen sähköpostitiliä edellyttää kattavan työhönottolaajennuksen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="a5c7f-114">Sähköpostipalvelun tilin liittäminen</span><span class="sxs-lookup"><span data-stu-id="a5c7f-114">Connect an email service account</span></span>

<span data-ttu-id="a5c7f-115">Liittämällä yrityksen sähköpostipalvelun tilin voi luoda työn hakijoille brändin mukaisen sähköpostikokemuksen.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="a5c7f-116">Jos et liitä yritystiliäsi, Attract käyttää oletusarvoista Microsoftin sähköpostipalvelun tiliä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="a5c7f-117">Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a5c7f-118">Valitse **sähköpostipalvelun tilien** **Sähköpostiasetukset**-välilehdessä **Liitä yritystili**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Yrityksen sähköpostipalvelun tilin liittäminen Attractissa](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="a5c7f-120">Lisätietoja jaetun sähköpostitilin luomisesta on kohdassa [Exchange Onlinen jaetut postilaatikot](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="a5c7f-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="a5c7f-121">Kirjaudu Microsoftin kirjautumisikkunassa sisään yrityksen tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="a5c7f-122">Jos et ole vielä määrittänyt sähköpostipalvelun tiliä tai jos haluat lisätä uuden tilin, valitse **Lisää uusi palvelun tili** ja anna sitten sähköpostin tiedot.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="a5c7f-123">Jos olet jo määrittänyt sähköpostipalvelun tilin, jota haluat käyttää, valitse se.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="a5c7f-124">Kun sähköpostipalvelun tili on määritetty, se näkyy **Sähköpostipalvelun tilit** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="a5c7f-125">Sähköpostipalvelun tilin yhteyden katkaiseminen</span><span class="sxs-lookup"><span data-stu-id="a5c7f-125">Disconnect an email service account</span></span>

<span data-ttu-id="a5c7f-126">Jos haluat lopettaa yrityksen toimialueen käyttämisen Attract-sähköpostiviestinnässä, voit katkaista sähköpostipalvelun tilin yhteyden.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="a5c7f-127">Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a5c7f-128">Valitse **sähköpostipalvelun tilien** **Sähköpostiasetukset**-välilehdessä **Lisää**-painike (kolme pistettä) sen sähköpostipalvelun tilin vieressä, jonka yhteyden haluat katkaista.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="a5c7f-129">Valitse **Katkaise sähköpostitilin yhteys**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-129">Select **Disconnect email account**.</span></span>

    ![Yrityksen sähköpostipalvelun tilin yhteyden katkaiseminen](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="a5c7f-131">Kun sinua pyydetään vahvistamaan toiminto, valitse **Katkaise yhteys**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Yrityksen sähköpostipalvelun tilin yhteyden katkaisemisen vahvistaminen](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="a5c7f-133">Jos et liitä jotain muuta sähköpostipalvelun tiliä, Attractista lähetettävät sähköpostit käyttävät oletusarvoista Microsoftin sähköpostipalvelun tiliä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="a5c7f-134">Sähköpostimallin asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a5c7f-134">Configure email template settings</span></span>

<span data-ttu-id="a5c7f-135">Voit ladata yrityksen logon kuvan ja muita tietoja sähköpostien brändin mukaiseksi ylätunnisteeksi.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="a5c7f-136">Voit myös muodostaa sähköpostin alatunnisteisiin linkkejä tietosuojakäytäntöön ja käyttöehtoihin.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="a5c7f-137">Sinun on noudatettava sekä kaikkia oman maasi tai alueesi sovellettavia lakeja että sen maan tai alueen lakeja, jotka koskevat sähköpostin vastaanottajaa.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="a5c7f-138">Nämä lait sisältävät roskapostisuojaa koskevia säädöksiä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="a5c7f-139">Valitse ensin **Asetukset** (rataskuvake oikeassa yläkulmassa) ja sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a5c7f-140">Vedä **Sähköpostimallin asetukset** -kohdan **Sähköpostiasetukset**-välilehdessä sähköpostin ylätunnisteena käytettävä kuva kuvaruutuun. Voit myös napsauttaa kuvaruutua ja siirtyä kyseiseen tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="a5c7f-141">Voit vaihtaa nykyisen kuva valitsemalla ensin sen vieressä **Poista**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="a5c7f-142">Kuvan on oltava JPEG-, JPG-, PNG- tai SVG-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="a5c7f-143">Suositeltu kuvakoko on leveydeltään 25–800 kuvapistettä ja korkeudeltaan 25–150 kuvapistettä.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="a5c7f-144">Ylätunnisteen kuvatiedoston enimmäiskoko on 1 megatavu (Mt).</span><span class="sxs-lookup"><span data-stu-id="a5c7f-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Yrityksen sähköpostin ylätunnisteen kuvan lisääminen](./media/attract-admin-email-header.png)

3. <span data-ttu-id="a5c7f-146">Lisää **Oma tietosuojakäytäntösi viestintää varten** -kohtaan linkki yrityksen tietosuojakäytäntöön.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="a5c7f-147">Lisää **Omat käyttöehtosi viestintää varten** -kohtaan linkki yrityksen käyttöohjeisiin.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Yrityksen tietosuojakäytännön ja käyttöehtojen linkin lisääminen sähköpostin alatunnisteeseen](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="a5c7f-149">Tallenna sähköpostimallin asetukset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-149">Select **Save** to save your email template settings.</span></span>
