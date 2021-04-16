---
title: Power Portalin käyttö osapuolen tietomallin kanssa
description: Tässä ohjeaiheessa kuvataan Power Portalin verkkorooleihin kaksoiskirjoituksen osapuolen tietomallin vuoksi tehdyt muutokset.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833087"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="c99d3-103">Power Portalin käyttö osapuolen tietomallin kanssa</span><span class="sxs-lookup"><span data-stu-id="c99d3-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c99d3-104">Kaksoiskirjoituksen sovellusorkestrointiratkaisun versio 2.0.999.0 ja uudemmat sisältävät tietomallin muutokset Tili- ja Yhteyshenkilö-tauluihin osapuolen ja yleisessä osoitekirjassa.</span><span class="sxs-lookup"><span data-stu-id="c99d3-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="c99d3-105">Muutokset mahdollistavat monta-moneen-suhteet, jotka tukevat kehittyneitä liiketoimintaskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="c99d3-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="c99d3-106">Näitä muutoksia eivät tue portaalin verkkoroolit, mukaan lukien asiakasportaali, jotka toimitetaan käyttövalmiina tai jotka olivat ympäristössäsi ennen kaksoiskirjoituksen asentamista.</span><span class="sxs-lookup"><span data-stu-id="c99d3-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="c99d3-107">Jotta verkkoroolit toimisivat odotetulla tavalla, sinun on luotava uusia verkkorooleja uuden tietomallin avulla.</span><span class="sxs-lookup"><span data-stu-id="c99d3-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="c99d3-108">Yhteenvetona voidaan sanoa, että taulukoiden vuorovaikutus on muuttunut, mutta asiakasportaalin taulukon käyttöoikeudet eivät ole muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="c99d3-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="c99d3-109">Tässä ohjeaiheessa kerrotaan, miten luodaan uusia verkkorooleja, jotka toimivat uuden kehittyneen tietomallin kanssa.</span><span class="sxs-lookup"><span data-stu-id="c99d3-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="c99d3-110">Tässä kaaviossa esitetään taulukon yhteys **ilman** osapuolen ja yleisen osoitekirjan tietomallia:</span><span class="sxs-lookup"><span data-stu-id="c99d3-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![ilman osapuolimallia](media/without-party-model.PNG)

<span data-ttu-id="c99d3-112">Tässä kaaviossa esitetään taulukon yhteys osapuolen ja yleisen osoitekirjan tietomallin **kanssa**:</span><span class="sxs-lookup"><span data-stu-id="c99d3-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![osapuolimallin kanssa](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="c99d3-114">Uuden taulukon käyttöoikeuden luominen</span><span class="sxs-lookup"><span data-stu-id="c99d3-114">Create a new table permission</span></span>

<span data-ttu-id="c99d3-115">Voit luoda nämä uudet taulukon käyttöoikeudet seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c99d3-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="c99d3-116">Kirjaudu [Power Appsiin](https://make.powerapps.com) ja siirry sovelluksiisi.</span><span class="sxs-lookup"><span data-stu-id="c99d3-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="c99d3-117">Valitse Portaalin hallinta -sovellus.</span><span class="sxs-lookup"><span data-stu-id="c99d3-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="c99d3-118">Valitse sivupalkista **Suojaus > Taulukon käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="c99d3-119">Sinun on luotava kolme uutta käyttöoikeutta:</span><span class="sxs-lookup"><span data-stu-id="c99d3-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="c99d3-120">Yhteyshenkilö-Osapuoli-yhteys</span><span class="sxs-lookup"><span data-stu-id="c99d3-120">Contact to Party connection</span></span>
    + <span data-ttu-id="c99d3-121">Osapuoli-Tili-yhteys</span><span class="sxs-lookup"><span data-stu-id="c99d3-121">Party to Account connection</span></span>
    + <span data-ttu-id="c99d3-122">Tili-Tilaus-yhteys</span><span class="sxs-lookup"><span data-stu-id="c99d3-122">Account to Order connection</span></span>

4. <span data-ttu-id="c99d3-123">Luo ja tallenna Yhteyshenkilö-Osapuoli-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:</span><span class="sxs-lookup"><span data-stu-id="c99d3-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="c99d3-124">**Nimi**: Osapuoli-Tili-yhteys (tai valintasi)</span><span class="sxs-lookup"><span data-stu-id="c99d3-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c99d3-125">**Taulukon nimi**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="c99d3-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="c99d3-126">**Sivusto**: Asiakasportaali</span><span class="sxs-lookup"><span data-stu-id="c99d3-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c99d3-127">**Laajuus**: Yhteyshenkilö</span><span class="sxs-lookup"><span data-stu-id="c99d3-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="c99d3-128">**Oikeudet**: Valitse kaikki</span><span class="sxs-lookup"><span data-stu-id="c99d3-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c99d3-129">**Verkkoroolit**: Todennetut käyttäjät, asiakasedustaja (tai valintasi)</span><span class="sxs-lookup"><span data-stu-id="c99d3-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="c99d3-130">Luo ja tallenna Osapuoli-Tili-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:</span><span class="sxs-lookup"><span data-stu-id="c99d3-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="c99d3-131">**Nimi**: Osapuoli-Tili-yhteys (tai valintasi)</span><span class="sxs-lookup"><span data-stu-id="c99d3-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c99d3-132">**Taulukon nimi**: account</span><span class="sxs-lookup"><span data-stu-id="c99d3-132">**Table Name**: account</span></span>
    + <span data-ttu-id="c99d3-133">**Sivusto**: Asiakasportaali</span><span class="sxs-lookup"><span data-stu-id="c99d3-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c99d3-134">**Laajuus**: Ylätaso</span><span class="sxs-lookup"><span data-stu-id="c99d3-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="c99d3-135">**Oikeudet**: Valitse kaikki</span><span class="sxs-lookup"><span data-stu-id="c99d3-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c99d3-136">**Ylätason taulukon oikeudet**: Yhteyshenkilö-Osapuoli-yhteys</span><span class="sxs-lookup"><span data-stu-id="c99d3-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="c99d3-137">Luo ja tallenna Tili-Tilaus-yhteyden uusi käyttöoikeus ja määritä nämä parametrit:</span><span class="sxs-lookup"><span data-stu-id="c99d3-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="c99d3-138">**Nimi**: Tili-Tilaus-yhteys (tai valintasi)</span><span class="sxs-lookup"><span data-stu-id="c99d3-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="c99d3-139">**Taulukon nimi**: salesorder</span><span class="sxs-lookup"><span data-stu-id="c99d3-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="c99d3-140">**Sivusto**: Asiakasportaali</span><span class="sxs-lookup"><span data-stu-id="c99d3-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c99d3-141">**Laajuus**: Ylätaso</span><span class="sxs-lookup"><span data-stu-id="c99d3-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="c99d3-142">**Oikeudet**: Valitse kaikki</span><span class="sxs-lookup"><span data-stu-id="c99d3-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c99d3-143">**Ylätason taulukon oikeudet**: Osapuoli-Tili-yhteys</span><span class="sxs-lookup"><span data-stu-id="c99d3-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
