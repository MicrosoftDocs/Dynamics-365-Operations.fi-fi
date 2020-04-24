---
title: Tavaralähetyksen määrittäminen
description: Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 51f7d6b0402ebbed417554978fc8d927f6b9c606
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207206"
---
# <a name="set-up-consignment"></a><span data-ttu-id="28ab4-103">Tavaralähetyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="28ab4-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28ab4-104">Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja.</span><span class="sxs-lookup"><span data-stu-id="28ab4-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="28ab4-105">Tavaralähetysvarasto on varasto, joka on toimittajan omistaa mutta joka on varastoituna yrityksesi toimipaikalle.</span><span class="sxs-lookup"><span data-stu-id="28ab4-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="28ab4-106">Kun haluat käyttää osan varastosta tai koko varaston, varaston omistajuus siirtyy yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="28ab4-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="28ab4-107">Tässä aiheessa kuvataan tarvittavat asetukset tavaralähetysprosessien käyttöönottoon.</span><span class="sxs-lookup"><span data-stu-id="28ab4-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="28ab4-108">Lisätietoja tavaralähetysprosesseista on kohdassa [Tavaralähetyksen määrittäminen](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="28ab4-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="28ab4-109">Varaston omistajat</span><span class="sxs-lookup"><span data-stu-id="28ab4-109">Inventory owners</span></span>
<span data-ttu-id="28ab4-110">Saapuvien lähetyksen fyysisen varaston kirjaamiseksi täytyy määrittää toimittajan omistaja.</span><span class="sxs-lookup"><span data-stu-id="28ab4-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="28ab4-111">Tämä tehdään **varaston omistaja** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="28ab4-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="28ab4-112">Kun valitset **toimittajatili** tämä luo oletusarvot **nimi** ja **omistaja** -kenttiin.</span><span class="sxs-lookup"><span data-stu-id="28ab4-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="28ab4-113">Arvo **omistaja**-kentässä näytetään toimittajalle, joten voit halutessasi muuttaa sitä, jos ulkoisten käyttäjien ei ole helppoa tunnistaa toimittajan tilin nimiä.</span><span class="sxs-lookup"><span data-stu-id="28ab4-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="28ab4-114">Voit muokata **omistaja** -kenttää ainoastaan siihen asti, kun olet tallentanut **varaston omistaja** -tietueen.</span><span class="sxs-lookup"><span data-stu-id="28ab4-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="28ab4-115">**Nimi**-kenttä täytetään sen osapuolen tiedoilla, joihin toimittajatili liittyy, eikä sitä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="28ab4-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="28ab4-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="28ab4-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="28ab4-117">Seurantadimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="28ab4-117">Tracking dimension group</span></span>
<span data-ttu-id="28ab4-118">Nimikkeet, jotka on tarkoitus käyttää lähetysprosesseissa, on yhdistettävä **seurantadimensioryhmään** jossa **omistaja** dimension arvo määritetään **aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="28ab4-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="28ab4-119">Omistaja-dimensiossa **Varastotilanne** ja **kirjanpitovarasto** -asetukset ovat aina valittuina.</span><span class="sxs-lookup"><span data-stu-id="28ab4-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="28ab4-120">**Kattavuussuunnitelma dimension mukaan** ei ole koskaan valittuna.</span><span class="sxs-lookup"><span data-stu-id="28ab4-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="28ab4-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="28ab4-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="28ab4-122">Varaston omistajuuden muutoksen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="28ab4-122">Inventory ownership change journal</span></span>
<span data-ttu-id="28ab4-123">**Varaston omistajuuden muutos** -kirjauskansiota käytetään muuttamaan tavaralähetysvaraston omistajuus toimittajalta yritykselle, joka käyttää varastoa.</span><span class="sxs-lookup"><span data-stu-id="28ab4-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="28ab4-124">Jokaiselle varastokirjauskansiolle on määritettävä nimi.</span><span class="sxs-lookup"><span data-stu-id="28ab4-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="28ab4-125">Nämä nimet luodaan **Varastokirjauskansion nimet** -sivulla ja **kirjauskansiotyypiksi** on määritettävä **Omistajuuden muutos**.</span><span class="sxs-lookup"><span data-stu-id="28ab4-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="28ab4-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="28ab4-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="28ab4-127">Toimittajayhteistyö tavaralähetysprosessissa</span><span class="sxs-lookup"><span data-stu-id="28ab4-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="28ab4-128">Jos toimittajat käyttävät toimittajayhteistyöliittymää, he voivat valvoa sen avulla toimipaikan varaston kulutusta.</span><span class="sxs-lookup"><span data-stu-id="28ab4-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="28ab4-129">Lisätietoja toimittajien määrittämisestä käyttämään toimittajayhteistyötä on kohdassa [Toimittajaportaalin käyttäjän suojaus](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="28ab4-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>
