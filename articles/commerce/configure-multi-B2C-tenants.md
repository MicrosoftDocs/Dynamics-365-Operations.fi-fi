---
title: Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä
description: Tässä ohjeaiheessa kerrotaan, milloin ja miten usean kanavan Microsoft Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään käyttäjän todennusta varten määritetyssä Dynamics 365 Commerce -ympäristössä.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0b14e0c662af74464768b66c1c86d03d2944014
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976013"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="3fdc5-103">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="3fdc5-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3fdc5-104">Tässä ohjeaiheessa kerrotaan, milloin ja miten usean Microsoft Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään kanavaa kohti käyttäjän todennusta varten määritetyssä Dynamics 365 Commerce -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="3fdc5-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="3fdc5-105">Overview</span></span>

<span data-ttu-id="3fdc5-106">Dynamics 365 Commerce käyttää Azure AD B2C:n pilven tunnistetietopalvelua käyttäjän todennustietojen tukemisessa ja todennuksen työnkuluissa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="3fdc5-107">Käyttäjät voivat rekisteröityä, kirjautua sisään ja palauttaa salasanan todennuksen työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="3fdc5-108">Azure AD B2C tallentaa käyttäjän luottamukselliset todennustiedot, kuten käyttäjätunnuksen ja salasanan.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="3fdc5-109">Käyttäjätietue on yksilöllinen jokaiselle B2C-vuokraajalle. Se käyttää joko käyttäjänimeä (sähköpostiosoitetta) tai yhteisöpalvelujen tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="3fdc5-110">Useimmissa tapauksissa yksittäistä Azure AD B2C -vuokraajaa käytetään Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="3fdc5-111">Tämän jälkeen Commerce-asiakkaat voivat luoda ja julkaista useita sivustoja samassa Commerce-ympäristössä. Samoja asiakastietoja käytetään kaikissa sivustoissa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="3fdc5-112">Jos ympäristön sivustoja on kuitenkin käsiteltävä erillisinä brändeinä ja ne näkyvät käyttäjille erillisinä yrityksinä, B2C-vuokraaja voidaan määrittää kanavalle, jota käytetään sivuston/brändin erittelyssä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="3fdc5-113">Huomioitavaa, kun kanavaa kohden on määritetty useita B2C-vuokraajia</span><span class="sxs-lookup"><span data-stu-id="3fdc5-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="3fdc5-114">Usein, kun kanavaa tai sivustoa käsitellään erillisenä yrityksenä, paras vaihtoehto käyttäjän tunnistamisen työnkulkujen kannalta on käyttää erillisiä yrityksiä Commercessa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="3fdc5-115">Jos kuitenkin haluat pitää kunkin kanavan/sivuston samassa ympäristössä ja yrityksessä, mutta haluat jokaiselle sivustolle erillisen käyttäjän todennuksen, on tärkeää ottaa huomioon seuraavat seikat ennen jatkamista:</span><span class="sxs-lookup"><span data-stu-id="3fdc5-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="3fdc5-116">Käyttäjillä on omat erilliset tunnistetiedot kullekin kanavalle/sivustolle.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="3fdc5-117">Samalla henkilöllä voi olla kaksi erillistä tiliä kanavaa/sivustoa kohti, koska jokainen tili on yksilöivä merkintä eriliseen B2C-vuokraajaan.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="3fdc5-118">Microsoft Dynamics -ympäristössä erilliset asiakastietueet palautetaan yleisiin tietuehakuihin.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="3fdc5-119">Jos käyttäjä käyttää samaa sähköpostiosoitetta eri kanavissa/sivustoissa, yleiset asiakashaut palauttavat tulokset jokaiselle kanavalle/sivustolle.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="3fdc5-120">(Näkyviin tulee kanavan ilmaisin.)</span><span class="sxs-lookup"><span data-stu-id="3fdc5-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="3fdc5-121">Osoitekirjaa voidaan käyttää käyttäjien ryhmittelyssä. Näin heitä voidaan seurata kanavakohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="3fdc5-122">Asiakastietueiden määrä kanavaa kohti voi nousta. Tämä nousu voi vaikuttaa yleisten asiakashakujen suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="3fdc5-123">B2C-vuokraajat on yhdistettävä huolellisesti kanavaan. Näin vältetään tilanteet, joissa asiakkaat rekisteröityvät väärään vuokraajaan.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="3fdc5-124">Muussa tapauksessa saattaa ilmetä sekaannuksia tai ongelmia seuraamisessa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="3fdc5-125">Seuraavassa kuvassa näkyy useita B2C-vuokraajia Commerce-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Useita B2C-vuokraajia Commerce-ympäristössä](media/MultiB2C_In_Environment.png)

<span data-ttu-id="3fdc5-127">Jos päätät, että yrityksesi edellyttää erillisiä B2C-vuokraajia kanavaa kohden samassa Commerce-ympäristössä, voit pyytää tätä toimintoa suorittamalla seuraavissa osissa olevat toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="3fdc5-128">Pyydä, että ympäristössä otetaan käyttöön B2C kanavaa kohti</span><span class="sxs-lookup"><span data-stu-id="3fdc5-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="3fdc5-129">Jos tällä hetkellä haluat, että samassa Commerce-ympäristössä on käytettävissä erilliset B2C-vuokraajat kanavaa kohti, lähetä pyyntö Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="3fdc5-130">Lisätietoja on kohdassa [Lifecycle Services (LCS) -tuen hankkiminen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md). Voit myös pyytää lisätietoja Commerce-ratkaisujen yhteyshenkilöltä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="3fdc5-131">B2C-vuokraajan määrittäminen ympäristössä</span><span class="sxs-lookup"><span data-stu-id="3fdc5-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="3fdc5-132">Jos haluat määrittää B2C-vuokraajat ympäristössä, tee tässä osassa mainitut tarvittavat toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="3fdc5-133">Azure AD B2C -vuokraajan lisääminen</span><span class="sxs-lookup"><span data-stu-id="3fdc5-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="3fdc5-134">Voit lisätä Azure AD B2C -vuokraajan ympäristöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="3fdc5-135">Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="3fdc5-136">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="3fdc5-137">Valitse ensin **B2C-asetukset** ja sitten **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="3fdc5-138">Valitse **Lisää B2C-sovellus** ja syötä sitten seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="3fdc5-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="3fdc5-139">**Sovelluksen nimi**: Syötä nimi, jota sovelluksessa käytetään Commercessa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="3fdc5-140">On suositeltavaa käyttää valittua sovelluksen nimeä, kun määrität Azure AD B2C -sovelluksen määrittämisajankohdan Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="3fdc5-141">Näin voit auttaa vähentämään sekaannuksia, kun hallitset B2C-vuokraajaa Commercessa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="3fdc5-142">**Vuokraajan nimi**: Anna B2C-vuokraajan nimi samalla tavalla kuin se näkyy Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="3fdc5-143">**Unohdetun salasanan käytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).</span><span class="sxs-lookup"><span data-stu-id="3fdc5-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="3fdc5-144">**SignUp SignIn -käytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).</span><span class="sxs-lookup"><span data-stu-id="3fdc5-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="3fdc5-145">**Asiakasohjelman GUID**: Syötä Azure AD B2C -vuokraajan tunnus niin kuin se näkyy Azure-portaalissa (ei sovelluksen tunnus B2C-vuokraajalle).</span><span class="sxs-lookup"><span data-stu-id="3fdc5-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="3fdc5-146">**Profiilin muokkauskäytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).</span><span class="sxs-lookup"><span data-stu-id="3fdc5-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="3fdc5-147">Kun olet syöttänyt nämä tiedot, tallenna muutokset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="3fdc5-148">Jätä kentät, kuten **Laajuus**, **Ei-interaktiivisen käytännön tunnus**, **Ei-interaktiivisen asiakasohjelman tunnus**, **Sisäänkirjauksen mukautettu toimialue** ja **Rekisteröitymisen käytännön tunnus** tyhjiksi, jos Dynamics 365 Commerce -ryhmä ei ohjeista määrittämään niitä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="3fdc5-149">Uusi Azure AD B2C -vuokraaja näkyy nyt luettelossa **Hallitse B2C-sovelluksia** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="3fdc5-150">Azure AD B2C -vuokraajan hallinta tai poistaminen</span><span class="sxs-lookup"><span data-stu-id="3fdc5-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="3fdc5-151">Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="3fdc5-152">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="3fdc5-153">Valitse ensin **B2C-asetukset** ja sitten **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="3fdc5-154">Jos haluat muokata B2C-vuokraajaa, valitse sen vieressä oleva kynäsymboli.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="3fdc5-155">Jos haluat poistaa B2C-vuokraajan, valitse sen vieressä oleva roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="3fdc5-156">Valitse **Tallenna** ja aktivoi muutoksesi valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="3fdc5-157">Kun B2C-vuokraaja määritetään reaaliaikaista/julkaistua sivustoa varten, käyttäjien on ehkä rekisteröidyttävä vuokraajan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="3fdc5-158">Jos poistat määritetyn vuokraajan **Vuokraajan asetukset \> B2C-vuokraaja** -valikosta, poistat kyseisen B2C-vuokraajan liitoksen sivustoista, jotka on liitetty vuokraajan kanaviin.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="3fdc5-159">Tässä tapauksessa käyttäjät eivät ehkä enää voi kirjautua tileille.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="3fdc5-160">Ole sen vuoksi hyvin varovainen, kun poistat määritetyn vuokraajan.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="3fdc5-161">Kun määritetty vuokralainen poistetaan, B2C-vuokraajaa ja tietueita ylläpidetään yhä, mutta kyseisen vuokraajan Commerce-järjestelmämääritystä muutetaan tai se poistetaan.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="3fdc5-162">Käyttäjät, jotka yrittävät rekisteröityä tai kirjautua sivustoon, luovat uuden asiakastietueen oletusarvoisessa tai juuri liitetyssä B2C-vuokraajassa, joka on määritetty sivuston kanavalle.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="3fdc5-163">Kanavan määrittäminen B2C-vuokraajan avulla</span><span class="sxs-lookup"><span data-stu-id="3fdc5-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="3fdc5-164">Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="3fdc5-165">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="3fdc5-166">Valitse **Kanavat** ja valitse sitten kanava, jonka haluat määrittää.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="3fdc5-167">Valitse oikeanpuoleisessa ominaisuusruudun **Valitse B2C-sovellus** -kentässä määritetty Azure AD B2C -vuokraaja, jos haluat käyttää tätä kanavaa.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="3fdc5-168">Vahvista uusi tai päivitetty konfigurointi valitsemalla komentopalkissa **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="3fdc5-169">Jos muutat B2C-sovellusta, joka on liitetty kanavaan, poistat nykyiset ympäristöön jo rekisteröityneiden käyttäjien viitteet.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="3fdc5-170">Tässä tapauksessa mitkään tällä hetkellä B2C-sovellukseen liitetyt tunnistetiedot eivät ole käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="3fdc5-171">Tämän vuoksi kanavan Azure AD B2C -määritystä kannattaa muuttaa vain, jos olet määrittämässä kanavaa ensimmäistä kertaa, eikä käyttäjiä ole vielä rekisteröitynyt sen käyttäjiksi.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="3fdc5-172">Muussa tapauksessa käyttäjien on ehkä rekisteröidyttävä uudelleen ja luotava tietue uuteen Azure AD B2C -vuokralaiseen.</span><span class="sxs-lookup"><span data-stu-id="3fdc5-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="3fdc5-173">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3fdc5-173">Additional resources</span></span>

[<span data-ttu-id="3fdc5-174">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3fdc5-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3fdc5-175">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="3fdc5-175">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3fdc5-176">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="3fdc5-176">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3fdc5-177">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="3fdc5-177">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3fdc5-178">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="3fdc5-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3fdc5-179">URL-osoitteen uudelleenohjausten lataaminen joukkona</span><span class="sxs-lookup"><span data-stu-id="3fdc5-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3fdc5-180">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="3fdc5-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3fdc5-181">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="3fdc5-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3fdc5-182">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="3fdc5-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3fdc5-183">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="3fdc5-183">Enable location-based store detection</span></span>](enable-store-detection.md)
