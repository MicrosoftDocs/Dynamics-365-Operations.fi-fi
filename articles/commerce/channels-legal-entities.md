---
title: Luo oikeushenkilöt
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478209"
---
# <a name="create-legal-entities"></a><span data-ttu-id="9f625-103">Luo oikeushenkilöt</span><span class="sxs-lookup"><span data-stu-id="9f625-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f625-104">Tässä ohjeaiheessa käsitellään yritysten luontia Microsoft Dynamics 365 Commercessa, sillä yritykset on luotava ja määritettävä ennen kanavien luontia.</span><span class="sxs-lookup"><span data-stu-id="9f625-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="9f625-105">Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne.</span><span class="sxs-lookup"><span data-stu-id="9f625-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="9f625-106">Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista.</span><span class="sxs-lookup"><span data-stu-id="9f625-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="9f625-107">Yritys on tietyntyyppinen oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="9f625-107">A company is a type of legal entity.</span></span> <span data-ttu-id="9f625-108">Tällä hetkellä yritykset ovat ainoita luotavia oikeushenkilöitä ja jokainen oikeushenkilö on liitetty yritystunnukseen.</span><span class="sxs-lookup"><span data-stu-id="9f625-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="9f625-109">Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai *DataAreaId*-tunnusta tietomalleissaan.</span><span class="sxs-lookup"><span data-stu-id="9f625-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="9f625-110">Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana.</span><span class="sxs-lookup"><span data-stu-id="9f625-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="9f625-111">Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.</span><span class="sxs-lookup"><span data-stu-id="9f625-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="9f625-112">Kanavaa luotaessa on määritettävä, mihin yritykseen kanava kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9f625-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="9f625-113">Uuden yrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="9f625-113">Create a new legal entity</span></span>

<span data-ttu-id="9f625-114">Luo uusi yritys Dynamics 365 Commercessa seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="9f625-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9f625-115">Valitse siirtymisruudussa **Moduulit \> Pääkonttorin asetukset \> Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="9f625-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="9f625-116">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9f625-116">On the action pane, select **New**.</span></span> <span data-ttu-id="9f625-117">Oikealle tulee **Uusi yritys** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="9f625-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="9f625-118">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9f625-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="9f625-119">Kirjoita arvo **Yritys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f625-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="9f625-120">Syötä tai valitse arvo **Maa/alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9f625-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="9f625-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f625-121">Select **OK**.</span></span> 

   ![Yrityksen luominen](media/legal-entities.png)

1. <span data-ttu-id="9f625-123">Anna **Yleiset**-osassa seuraavat yleistiedot yrityksestä:</span><span class="sxs-lookup"><span data-stu-id="9f625-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="9f625-124">Kirjoita hakunimi, jos hakunimi on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="9f625-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="9f625-125">Hakunimi on vaihtoehtoinen nimi, jota voidaan käyttää tämän yrityksen etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="9f625-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="9f625-126">Valitse käytetäänkö tätä oikeushenkilöä konsolidointiyrityksenä.</span><span class="sxs-lookup"><span data-stu-id="9f625-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="9f625-127">Valitse käytetäänkö tätä oikeushenkilöä eliminointiyrityksenä.</span><span class="sxs-lookup"><span data-stu-id="9f625-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="9f625-128">Valitse entiteetin **oletuskieli**.</span><span class="sxs-lookup"><span data-stu-id="9f625-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="9f625-129">Valitse entiteetin **aikavyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="9f625-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="9f625-130">Valitse **Osoitteet**-osassa **Muokkaa** ja anna osoitetiedot, kuten kadun nimi ja numero sekä postinumero ja postitoimipaikka.</span><span class="sxs-lookup"><span data-stu-id="9f625-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="9f625-131">Kirjoita **Yhteystiedot**-osaan tiedot viestintämenetelmistä, kuten sähköpostiosoitteet, URL-osoitteet ja puhelinnumerot.</span><span class="sxs-lookup"><span data-stu-id="9f625-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="9f625-132">Kirjoita **Lakisääteinen raportointi** -osaan rekisterinumerot, joita käytetään lakisääteisiin ilmoituksiin.</span><span class="sxs-lookup"><span data-stu-id="9f625-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="9f625-133">Kirjoita **Rekisteröintinumerot**-osaan kaikki yrityksestä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="9f625-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="9f625-134">Kirjoita **Pankkitilin tiedot** -osaan yrityksen pankkitilien numerot ja reititysnumerot.</span><span class="sxs-lookup"><span data-stu-id="9f625-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="9f625-135">Kirjoita **Ulkomaankauppa ja -logistiikka** osaan yrityksen lähetystiedot.</span><span class="sxs-lookup"><span data-stu-id="9f625-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="9f625-136">**Numerosarjat**-osassa voit tarkastella yritykseen liitettyjä numerosarjoja.</span><span class="sxs-lookup"><span data-stu-id="9f625-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="9f625-137">Tämä on aluksi tyhjä.</span><span class="sxs-lookup"><span data-stu-id="9f625-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="9f625-138">**Koontinäytön kuva** -osassa voit tarkastella yritykseen liitettyä logoa ja koontinäytön kuvaa sekä vaihtaa sen.</span><span class="sxs-lookup"><span data-stu-id="9f625-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="9f625-139">Kirjoita **Verorekisteröinti**-osaan rekisterinumerot, joita käytetään raportoitaessa veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="9f625-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="9f625-140">Kirjoita **Vero 1099** -osaan yrityksen 1099-tiedot.</span><span class="sxs-lookup"><span data-stu-id="9f625-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="9f625-141">Anna yrityksen verotiedot **Verotiedot**-osaan.</span><span class="sxs-lookup"><span data-stu-id="9f625-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="9f625-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9f625-142">Select **Save**.</span></span>

<span data-ttu-id="9f625-143">Seuraavassa kuvassa näkyy esimerkkiyrityksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="9f625-143">The following image shows details of an example legal entity.</span></span>

![Yrityksen yleinen osa](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="9f625-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9f625-145">Additional resources</span></span>

[<span data-ttu-id="9f625-146">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9f625-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9f625-147">Organisaatiohierarkian suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="9f625-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9f625-148">Organisaatiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="9f625-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="9f625-149">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9f625-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9f625-150">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="9f625-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
