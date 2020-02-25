---
title: Yritysten luominen
description: Tässä ohjeaiheessa käsitellään yritysten luontia Microsoft Dynamics 365 Commercessa, sillä yritykset on luotava ja määritettävä ennen kanavien luontia.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002401"
---
# <a name="create-legal-entities"></a><span data-ttu-id="835f5-103">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="835f5-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="835f5-104">Tässä ohjeaiheessa käsitellään yritysten luontia Microsoft Dynamics 365 Commercessa, sillä yritykset on luotava ja määritettävä ennen kanavien luontia.</span><span class="sxs-lookup"><span data-stu-id="835f5-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="835f5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="835f5-105">Overview</span></span>

<span data-ttu-id="835f5-106">Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne.</span><span class="sxs-lookup"><span data-stu-id="835f5-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="835f5-107">Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista.</span><span class="sxs-lookup"><span data-stu-id="835f5-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="835f5-108">Yritys on tietyntyyppinen oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="835f5-108">A company is a type of legal entity.</span></span> <span data-ttu-id="835f5-109">Tällä hetkellä yritykset ovat ainoita luotavia oikeushenkilöitä ja jokainen oikeushenkilö on liitetty yritystunnukseen.</span><span class="sxs-lookup"><span data-stu-id="835f5-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="835f5-110">Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai *DataAreaId*-tunnusta tietomalleissaan.</span><span class="sxs-lookup"><span data-stu-id="835f5-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="835f5-111">Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana.</span><span class="sxs-lookup"><span data-stu-id="835f5-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="835f5-112">Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.</span><span class="sxs-lookup"><span data-stu-id="835f5-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="835f5-113">Kanavaa luotaessa on määritettävä, mihin yritykseen kanava kuuluu.</span><span class="sxs-lookup"><span data-stu-id="835f5-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="835f5-114">Uuden yrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="835f5-114">Create a new legal entity</span></span>

<span data-ttu-id="835f5-115">Luo uusi yritys Dynamics 365 Commercessa seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="835f5-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="835f5-116">Valitse siirtymisruudussa **Moduulit \> Pääkonttorin asetukset \> Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="835f5-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="835f5-117">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="835f5-117">On the action pane, select **New**.</span></span> <span data-ttu-id="835f5-118">Oikealle tulee **Uusi yritys** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="835f5-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="835f5-119">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="835f5-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="835f5-120">Kirjoita arvo **Yritys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="835f5-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="835f5-121">Syötä tai valitse arvo **Maa/alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="835f5-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="835f5-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="835f5-122">Select **OK**.</span></span> 

   ![Yrityksen luominen](media/legal-entities.png)

1. <span data-ttu-id="835f5-124">Anna **Yleiset**-osassa seuraavat yleistiedot yrityksestä:</span><span class="sxs-lookup"><span data-stu-id="835f5-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="835f5-125">Kirjoita hakunimi, jos hakunimi on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="835f5-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="835f5-126">Hakunimi on vaihtoehtoinen nimi, jota voidaan käyttää tämän yrityksen etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="835f5-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="835f5-127">Valitse käytetäänkö tätä oikeushenkilöä konsolidointiyrityksenä.</span><span class="sxs-lookup"><span data-stu-id="835f5-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="835f5-128">Valitse käytetäänkö tätä oikeushenkilöä eliminointiyrityksenä.</span><span class="sxs-lookup"><span data-stu-id="835f5-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="835f5-129">Valitse entiteetin **oletuskieli**.</span><span class="sxs-lookup"><span data-stu-id="835f5-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="835f5-130">Valitse entiteetin **aikavyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="835f5-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="835f5-131">Valitse **Osoitteet**-osassa **Muokkaa** ja anna osoitetiedot, kuten kadun nimi ja numero sekä postinumero ja postitoimipaikka.</span><span class="sxs-lookup"><span data-stu-id="835f5-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="835f5-132">Kirjoita **Yhteystiedot**-osaan tiedot viestintämenetelmistä, kuten sähköpostiosoitteet, URL-osoitteet ja puhelinnumerot.</span><span class="sxs-lookup"><span data-stu-id="835f5-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="835f5-133">Kirjoita **Lakisääteinen raportointi** -osaan rekisterinumerot, joita käytetään lakisääteisiin ilmoituksiin.</span><span class="sxs-lookup"><span data-stu-id="835f5-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="835f5-134">Kirjoita **Rekisteröintinumerot**-osaan kaikki yrityksestä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="835f5-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="835f5-135">Kirjoita **Pankkitilin tiedot** -osaan yrityksen pankkitilien numerot ja reititysnumerot.</span><span class="sxs-lookup"><span data-stu-id="835f5-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="835f5-136">Kirjoita **Ulkomaankauppa ja -logistiikka** osaan yrityksen lähetystiedot.</span><span class="sxs-lookup"><span data-stu-id="835f5-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="835f5-137">**Numerosarjat**-osassa voit tarkastella yritykseen liitettyjä numerosarjoja.</span><span class="sxs-lookup"><span data-stu-id="835f5-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="835f5-138">Tämä on aluksi tyhjä.</span><span class="sxs-lookup"><span data-stu-id="835f5-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="835f5-139">**Koontinäytön kuva** -osassa voit tarkastella yritykseen liitettyä logoa ja koontinäytön kuvaa sekä vaihtaa sen.</span><span class="sxs-lookup"><span data-stu-id="835f5-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="835f5-140">Kirjoita **Verorekisteröinti**-osaan rekisterinumerot, joita käytetään raportoitaessa veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="835f5-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="835f5-141">Kirjoita **Vero 1099** -osaan yrityksen 1099-tiedot.</span><span class="sxs-lookup"><span data-stu-id="835f5-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="835f5-142">Anna yrityksen verotiedot **Verotiedot**-osaan.</span><span class="sxs-lookup"><span data-stu-id="835f5-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="835f5-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="835f5-143">Select **Save**.</span></span>

<span data-ttu-id="835f5-144">Seuraavassa kuvassa näkyy esimerkkiyrityksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="835f5-144">The following image shows details of an example legal entity.</span></span>

![Yrityksen yleinen osa](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="835f5-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="835f5-146">Additional resources</span></span>

[<span data-ttu-id="835f5-147">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="835f5-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="835f5-148">Organisaatiohierarkian suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="835f5-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="835f5-149">Organisaatiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="835f5-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="835f5-150">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="835f5-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="835f5-151">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="835f5-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
