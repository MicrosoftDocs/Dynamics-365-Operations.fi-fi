---
title: Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille
description: Tämä ohjeaihe kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti. Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117358"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="9ee98-104">Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille</span><span class="sxs-lookup"><span data-stu-id="9ee98-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ee98-105">Tämä ohjeaihe kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="9ee98-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="9ee98-106">Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="9ee98-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="9ee98-107">Eräiden maiden tai alueiden tapahtumatyyppien kohdalle voit myös lisätä Microsoft Dynamics AX -tietokannan kenttien tekstejä, jotka liittyvät kyseisiin tapahtumatyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="9ee98-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="9ee98-108">Luettelo tapahtumatyypeistä, maista ja alueista esitetään myöhemmin tässä aiheessa kohdassa [Valinnainen: Lisää muuta tekstiä oletuskuvauksiin](#optional-add-other-text-to-default-descriptions).</span><span class="sxs-lookup"><span data-stu-id="9ee98-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="9ee98-109">Oletuskuvausten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9ee98-109">Set up default descriptions</span></span>

1. <span data-ttu-id="9ee98-110">Siirty kohtaan **Organisaation hallinta** \> **Asetukset** \> **Oletuskuvaukset**</span><span class="sxs-lookup"><span data-stu-id="9ee98-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="9ee98-111">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9ee98-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="9ee98-112">Valitse **Kuvaus**-kentästä tapahtumatyyppi, jolle haluat luoda oletuskuvauksen.</span><span class="sxs-lookup"><span data-stu-id="9ee98-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="9ee98-113">Valitse **Kieli**-kentässä kieli, jota tämä kuvaus koskee.</span><span class="sxs-lookup"><span data-stu-id="9ee98-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="9ee98-114">Kirjoita **Teksti**-kenttään oletuskuvaus.</span><span class="sxs-lookup"><span data-stu-id="9ee98-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="9ee98-115">Voit kirjoittaa tekstiä kenttään, tai voit käyttää yhtä tai useita seuraavista vapaan tekstin muuttujista:</span><span class="sxs-lookup"><span data-stu-id="9ee98-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="9ee98-116">**%1** – Lisää tapahtumapäivä.</span><span class="sxs-lookup"><span data-stu-id="9ee98-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="9ee98-117">**%2** – Lisää tunniste, joka vastaa kirjanpitoon kirjattavan asiakirjan tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="9ee98-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="9ee98-118">Esimerkiksi laskuihin liittyviin tapahtumatyyppeihin **%2**-muuttuja lisää laskunumeron.</span><span class="sxs-lookup"><span data-stu-id="9ee98-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="9ee98-119">**%3** – Lisää tunniste, joka liittyy kirjanpitoon kirjattavan asiakirjan tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="9ee98-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="9ee98-120">Esimerkiksi laskuihin liittyviin tapahtumatyyppeihin **%3**-muuttuja lisää asiakkaan tilinumeron.</span><span class="sxs-lookup"><span data-stu-id="9ee98-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="9ee98-121">Valinnainen: Lisää muuta tekstä oletuskuvauksiin</span><span class="sxs-lookup"><span data-stu-id="9ee98-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="9ee98-122">Joissakin tapahtumatyypeissä joissakin maissa tai joillakin alueilla oletuskuvaukset voivat sisältää tekstiä, joka perustuu kyseisten tapahtumatyyppien tietojen kenttiin.</span><span class="sxs-lookup"><span data-stu-id="9ee98-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="9ee98-123">Seuraavassa luettelossa näkyvät tapahtumatyypit ja maat tai alueet, joissa tämä vaihtoehto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="9ee98-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="9ee98-124">**Tapahtumatyypit**</span><span class="sxs-lookup"><span data-stu-id="9ee98-124">**Transaction types**</span></span>

<span data-ttu-id="9ee98-125">Voit lisätä tekstiä oletuskuvauksiin tapahtumatyypeille, jotka liittyvät seuraavat asiakirjamalleja:</span><span class="sxs-lookup"><span data-stu-id="9ee98-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="9ee98-126">Myyntilaskut</span><span class="sxs-lookup"><span data-stu-id="9ee98-126">Customer invoices</span></span>
- <span data-ttu-id="9ee98-127">Asiakkaan hyvityslaskut</span><span class="sxs-lookup"><span data-stu-id="9ee98-127">Customer credit notes</span></span>
- <span data-ttu-id="9ee98-128">Asiakkaan käteismaksut</span><span class="sxs-lookup"><span data-stu-id="9ee98-128">Customer cash payments</span></span>
- <span data-ttu-id="9ee98-129">Toimittajan maksut</span><span class="sxs-lookup"><span data-stu-id="9ee98-129">Vendor payments</span></span>
- <span data-ttu-id="9ee98-130">Myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="9ee98-130">Sales orders</span></span>
- <span data-ttu-id="9ee98-131">Ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="9ee98-131">Purchase orders</span></span>
- <span data-ttu-id="9ee98-132">Varastokirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="9ee98-132">Inventory journals</span></span>
- <span data-ttu-id="9ee98-133">Pääsuunnittelu</span><span class="sxs-lookup"><span data-stu-id="9ee98-133">Master planning (MRP)</span></span>
- <span data-ttu-id="9ee98-134">Käyttöomaisuuserät</span><span class="sxs-lookup"><span data-stu-id="9ee98-134">Fixed assets</span></span>

<span data-ttu-id="9ee98-135">**Maat ja alueet**</span><span class="sxs-lookup"><span data-stu-id="9ee98-135">**Countries and regions**</span></span>

<span data-ttu-id="9ee98-136">Tämä vaihtoehto on käytettävissä seuraavissa maissa ja seuraavilla alueilla:</span><span class="sxs-lookup"><span data-stu-id="9ee98-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="9ee98-137">Brasilia</span><span class="sxs-lookup"><span data-stu-id="9ee98-137">Brazil</span></span>
- <span data-ttu-id="9ee98-138">Kiina</span><span class="sxs-lookup"><span data-stu-id="9ee98-138">China</span></span>
- <span data-ttu-id="9ee98-139">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="9ee98-139">Czech Republic</span></span>
- <span data-ttu-id="9ee98-140">Itä-Eurooppa</span><span class="sxs-lookup"><span data-stu-id="9ee98-140">Eastern Europe</span></span>
- <span data-ttu-id="9ee98-141">Unkari</span><span class="sxs-lookup"><span data-stu-id="9ee98-141">Hungary</span></span>
- <span data-ttu-id="9ee98-142">Intia</span><span class="sxs-lookup"><span data-stu-id="9ee98-142">India</span></span>
- <span data-ttu-id="9ee98-143">Japani</span><span class="sxs-lookup"><span data-stu-id="9ee98-143">Japan</span></span>
- <span data-ttu-id="9ee98-144">Liettua</span><span class="sxs-lookup"><span data-stu-id="9ee98-144">Lithuania</span></span>
- <span data-ttu-id="9ee98-145">Latvia</span><span class="sxs-lookup"><span data-stu-id="9ee98-145">Latvia</span></span>
- <span data-ttu-id="9ee98-146">Puola</span><span class="sxs-lookup"><span data-stu-id="9ee98-146">Poland</span></span>
- <span data-ttu-id="9ee98-147">Venäjä</span><span class="sxs-lookup"><span data-stu-id="9ee98-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="9ee98-148">Lisää tekstiä oletuskuvauksiin</span><span class="sxs-lookup"><span data-stu-id="9ee98-148">Add text to default descriptions</span></span>

<span data-ttu-id="9ee98-149">Kun olet suorittanut aiemmin tässä ohjeaiheessa kuvatun kohdan [Oletuskuvausten määrittäminen](#set-up-default-descriptions) vaiheet, lisää tekstiä oletuskuvauksiin tekemällä seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="9ee98-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="9ee98-150">Valitse **Parametrit**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9ee98-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="9ee98-151">Valitse **Viitetaulukko**-kentästä tietokantataulukko, josta parametritietoja lisätään kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="9ee98-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="9ee98-152">Valitse **Viitekenttä**-kentästä kenttä, josta parametritietoja lisätään kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="9ee98-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="9ee98-153">Voit lisätä muita parametrejä tekemällä kohtien 1–3 toimet uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9ee98-153">Repeat steps 1 through 3 to add more parameters.</span></span>
