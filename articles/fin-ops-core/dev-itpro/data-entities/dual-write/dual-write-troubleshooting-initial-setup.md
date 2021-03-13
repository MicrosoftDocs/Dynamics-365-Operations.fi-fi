---
title: Ongelmien vianmääritys alkumäärityksen aikana
description: Tässä ohjeaiheessa on tietoja, joiden avulla voidaan korjata kaksoiskirjoituksen integroinnin alkuasennuksen aikana esiintyviä ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: cfbc1ab3ef6d47f6ec2d8ca4ca4b8940784e6e49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129978"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="0dba7-103">Ongelmien vianmääritys alkumäärityksen aikana</span><span class="sxs-lookup"><span data-stu-id="0dba7-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0dba7-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="0dba7-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0dba7-105">Erityisesti se tarjoaa tietoa vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä kaksoiskirjoituksen integroinnin alkuasennuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="0dba7-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0dba7-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="0dba7-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0dba7-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="0dba7-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="0dba7-108">Et voi linkittää Finance and Operations -sovellusta Dataverseen</span><span class="sxs-lookup"><span data-stu-id="0dba7-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="0dba7-109">**Kaksoiskirjoituksen asettamiseen vaadittava rooli:** Järjestelmän ylläpitäjä Finance and Operations -sovelluksissa ja Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="0dba7-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="0dba7-110">**Asennuslinkki Dataverseen** -sivulla olevat virheet johtuvat yleensä puutteellisista määritys- tai käyttöoikeusongelmista.</span><span class="sxs-lookup"><span data-stu-id="0dba7-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="0dba7-111">Varmista, että koko terveystarkistus siirtyy **Asennuslinkillä Dataverseen**, kuten seuraavasta kuvasta käy ilmi.</span><span class="sxs-lookup"><span data-stu-id="0dba7-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="0dba7-112">Kaksoiskirjoittamista ei voi linkittää, ellei koko terveystarkistus ole ohi.</span><span class="sxs-lookup"><span data-stu-id="0dba7-112">You can't link dual-write unless the whole health check passes.</span></span>

![Onnistunut kuntotarkistus](media/health_check.png)

<span data-ttu-id="0dba7-114">Sinulla on oltava Azure AD -vuokralaisen järjestelmänvalvojan käyttöoikeudet Finance and Operations- ja Dataverse -ympäristöjen linkittämiseen.</span><span class="sxs-lookup"><span data-stu-id="0dba7-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="0dba7-115">Kun olet linkittänyt ympäristöt, käyttäjät voivat kirjautua sisään käyttämällä tilinsä tunnistetietoja ja päivittää aiemmin luotua taulujen yhdistämiskarttaa.</span><span class="sxs-lookup"><span data-stu-id="0dba7-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="0dba7-116">Virhe avatessasi linkin Dataverse -sivulle</span><span class="sxs-lookup"><span data-stu-id="0dba7-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="0dba7-117">**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta</span><span class="sxs-lookup"><span data-stu-id="0dba7-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="0dba7-118">Näyttöön saattaa tulla seuraava virhesanoma, kun avaat **Linkin Dataverse** -sivulle Finance and Operations -sovelluksessa:</span><span class="sxs-lookup"><span data-stu-id="0dba7-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="0dba7-119">*Vastauksen tilakoodi ei tarkoita onnistumista: 404 (Ei löydetty).*</span><span class="sxs-lookup"><span data-stu-id="0dba7-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="0dba7-120">Tämä virhe ilmenee, kun suostumusvaihetta ei ole suoritettu.</span><span class="sxs-lookup"><span data-stu-id="0dba7-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="0dba7-121">Voit tarkistaa, onko suostumus vaihesuoritettu, kirjautumalla kohteeseen portal.Azure.com käyttämällä Azure AD -vuokralaisen järjestelmänvalvojan tiliä ja katsomalla, näkyykö kolmannen osapuolen sovellusta, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** Azure AD:ssa, **Yrityssovellukset**-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0dba7-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="0dba7-122">Jos näin ei ole, sinun on annettava sovelluksen suostumus.</span><span class="sxs-lookup"><span data-stu-id="0dba7-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="0dba7-123">Voit antaa sovelluksen suostumuksen noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0dba7-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="0dba7-124">Avaa seuraava URL-osoite käyttämällä järjestelmänvalvojan tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="0dba7-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="0dba7-125">Sinua pyydetään antamaan suostumus.</span><span class="sxs-lookup"><span data-stu-id="0dba7-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="0dba7-126">Valitse **Hyväksy**, jos haluat ilmaista suostumuksesi siihen, että asennat sovelluksen, jonka tunnus **33976c19-1db5-4c02-810e-c243db79efde** on vuokralaisella.</span><span class="sxs-lookup"><span data-stu-id="0dba7-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="0dba7-127">Tämä sovellus edellyttää Dataversen ja Finance and Operations -sovellusten linkittämistä.</span><span class="sxs-lookup"><span data-stu-id="0dba7-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="0dba7-128">Jos tässä vaiheessa ilmenee ongelmia, avaa selain incognito-tilassa (Google Chromessa) tai InPrivate-tilassa (Microsoft Edgessä).</span><span class="sxs-lookup"><span data-stu-id="0dba7-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="0dba7-129">Varmista, että yrityksen tiedot ja kaksoiskirjoitusryhmät on määritetty oikein linkittämisen aikana</span><span class="sxs-lookup"><span data-stu-id="0dba7-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="0dba7-130">Jos haluat varmistaa, että kaksoiskirjoitus toimii oikein, konfiguroinnin aikana valitsemasi yritykset luodaan Dataverse -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="0dba7-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="0dba7-131">Oletusarvon mukaan nämä yritykset ovat vain luku -tilassa ja **IsDualWriteEnable**-ominaisuuden arvo on **True**.</span><span class="sxs-lookup"><span data-stu-id="0dba7-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="0dba7-132">Lisäksi luodaan oletusarvon mukainen liiketoimintayksiköiden omistaja ja ryhmä ja lisätään yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="0dba7-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="0dba7-133">Ennen kuin otat kartat käyttöön, varmista, että ryhmän oletusomistaja on määritetty.</span><span class="sxs-lookup"><span data-stu-id="0dba7-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="0dba7-134">Voit etsiä **Yritykset (CDM\_Yritys)** -taulukon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0dba7-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="0dba7-135">Valitse Dynamics 365:n mallipohjaisen sovelluksen oikeasta yläkulmasta suodatin.</span><span class="sxs-lookup"><span data-stu-id="0dba7-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="0dba7-136">Valitse avattavasta luettelosta **Yritys**.</span><span class="sxs-lookup"><span data-stu-id="0dba7-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="0dba7-137">Voit tarkastella tuloksia valitsemalla **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="0dba7-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="0dba7-138">Valitse yritys, joka on linkitetty kaksoiskirjoituksen määrityksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0dba7-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="0dba7-139">Varmista, että **Omistavan oletusryhmän** -sarakkeessa on arvo.</span><span class="sxs-lookup"><span data-stu-id="0dba7-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="0dba7-140">Seuraavassa kuvassa **Omistavan oletusryhmän** -sarakkeen arvoksi on määritetty **USMF-kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="0dba7-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Omistavan oletusryhmän tarkistaminen](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="0dba7-142">Kaksoiskirjoittamiseen liittyvien lakitaulujen tai yritysten määrän rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="0dba7-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="0dba7-143">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität ottaa yhdistämismäärityksiä käyttöön:</span><span class="sxs-lookup"><span data-stu-id="0dba7-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="0dba7-144">*Kaksoiskirjoitusvirhe - Laajennuksen rekisteröiminen epäonnistui: \[(Osiokarttaa ei voitu saada projektille DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Virhe ylittää DWM-määrityksen enimmäisosiot DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], tapahtui virheitä.*</span><span class="sxs-lookup"><span data-stu-id="0dba7-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="0dba7-145">Tämänhetkinen raja-arvo, kun linkität ympäristöjä, on noin 40 lakitaulua.</span><span class="sxs-lookup"><span data-stu-id="0dba7-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="0dba7-146">Tämä virhe ilmenee, jos yrität ottaa käyttöön yhdistämisen ja yli 40 taulua linkitetään ympäristöjen välillä.</span><span class="sxs-lookup"><span data-stu-id="0dba7-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>
