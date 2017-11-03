---
title: Puhelinpalvelun luettelot
description: "Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin luetteloiden puhelinkeskusta koskevat toiminnot."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5a97ab749259fcc97b269b0134792820ebf13af
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="839b3-103">Puhelinkeskuksen luettelot</span><span class="sxs-lookup"><span data-stu-id="839b3-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="839b3-104">Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin luetteloiden puhelinkeskusta koskevat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="839b3-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="839b3-105">Puhelinkeskuksessa voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="839b3-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="839b3-106">Puhelinkeskukset käyttävät yleensä tulostettuja luetteloita.</span><span class="sxs-lookup"><span data-stu-id="839b3-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="839b3-107">Tulostetun luettelon suunnittelu ja tuotanto käsitellään Dynamics 365 for Retailin ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="839b3-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="839b3-108">Voit kuitenkin luoda ja tallentaa luettelon digitaalisessa muodossa käyttämällä samoja sivuja, joilla määrität verkkoluettelot.</span><span class="sxs-lookup"><span data-stu-id="839b3-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="839b3-109">Ennen kuin voit luoda luettelon, sinun on asetettava tuotevalikoimat ja määritettävä valikoimat puhelinkeskukselle.</span><span class="sxs-lookup"><span data-stu-id="839b3-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="839b3-110">Lisäät sitten tuotteet luetteloon valitsemalla tuotteet näistä valikoimista.</span><span class="sxs-lookup"><span data-stu-id="839b3-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="839b3-111">Kun tuotteet on lisätty luetteloon ja luettelo on valmis, sen tiedot on varmennettava.</span><span class="sxs-lookup"><span data-stu-id="839b3-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="839b3-112">Tämän jälkeen sinun on lähetettävä luettelo arvioitaviksi ja hyväksyttäviksi.</span><span class="sxs-lookup"><span data-stu-id="839b3-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="839b3-113">Kun luettelo on hyväksytty, se voidaan julkaista.</span><span class="sxs-lookup"><span data-stu-id="839b3-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="839b3-114">Kun puhelinkeskusluettelo luodaan, voit ottaa tilannevedoksen luettelon tiedoista luettelon julkaisuhetkellä.</span><span class="sxs-lookup"><span data-stu-id="839b3-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="839b3-115">Tilannevedostoiminto mahdollistaa tietyn luetteloversion käyttämisen, vaikka luetteloa muutetaan ja päivitetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="839b3-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="839b3-116">Puhelinkeskuksen luettelot voidaan määrittää myös sisältämään seuraavat valinnaiset toiminnot:</span><span class="sxs-lookup"><span data-stu-id="839b3-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="839b3-117">**Lähdekoodit** – Lähdekoodeja käytetään asiakkailta tiettyihin luettelopostituksiin saatujen vastausten seuraamiseen.</span><span class="sxs-lookup"><span data-stu-id="839b3-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="839b3-118">**Ilmaiset tuotteet** – Tuotteet, joita voidaan sisällyttää asiakkaan tilaukseen ilman lisämaksua.</span><span class="sxs-lookup"><span data-stu-id="839b3-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="839b3-119">Nämä tuotteet lisätään tilaukseen automaattisesti, kun luettelon lähdekoodi kirjoitetaan tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="839b3-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="839b3-120">**Käsikirjoitukset** – Käsikirjoitukset ovat tekstejä, joita puhelinpalvelun työntekijä lukee asiakkaalle, kun myyntitilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="839b3-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="839b3-121">Komentosarjat voivat sisältää tervehdyksiä tai ostoehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="839b3-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="839b3-122">**Sivun asettelu** – Sivun asettelussa määritetään tuotteiden asettelun sivulla painetussa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="839b3-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="839b3-123">Näitä tietoja käytetään luettelon alueanalyysiraportissa.</span><span class="sxs-lookup"><span data-stu-id="839b3-123">This information is used for the catalog area analysis report.</span></span>





