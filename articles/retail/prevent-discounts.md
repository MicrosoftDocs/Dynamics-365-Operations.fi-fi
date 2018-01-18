---
title: "Vähittäismyyntituotteiden alennusten estäminen"
description: "Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana."
author: jeffbl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: c13eef79830fc59ca79bd6f0e4fa5685372dde3a
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="prevent-discounts-for-retail-products"></a><span data-ttu-id="3e547-103">Vähittäismyyntituotteiden alennusten estäminen</span><span class="sxs-lookup"><span data-stu-id="3e547-103">Prevent discounts for retail products</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="3e547-104">Jälleenmyyjillä voi olla erilaisia syitä, miksi he haluavat estää joidenkin tuotteiden hintojen alentamisen joko kampanjan tai myyntipisteellä tapahtuvan myynnin aikana.</span><span class="sxs-lookup"><span data-stu-id="3e547-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="3e547-105">Seuraavat asetukset sijaitsevat vapautettujen tuotteiden **Vähittäismyynti**-välilehdissä, ja niiden avulla tuote voidaan määrittää estämään kaikki alennukset tai manuaaliset alennukset.</span><span class="sxs-lookup"><span data-stu-id="3e547-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="3e547-106">Asetukset voidaan määrittää myös vähittäismyynnin luokkahierarkian luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="3e547-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="3e547-107">**Estä kaikki alennukset**: Valitse tämä asetus, jos haluat estää kaikenlaisten alennusten käytön tässä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="3e547-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="3e547-108">Esto koskee kampanjoita, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä, samoin kuin manuaalisia rivi- ja tapahtuma-alennuksia, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana.</span><span class="sxs-lookup"><span data-stu-id="3e547-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="3e547-109">**Estä manuaaliset alennukset**: Valitse tämä asetus, jos haluat estää vain manuaaliset rivi- tai tapahtuma-alennukset, joita myyntipisteen käyttäjä käyttää myyntitapahtuman aikana.</span><span class="sxs-lookup"><span data-stu-id="3e547-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="3e547-110">Tuotteissa, joissa tämä asetus on valittu, voidaan edelleen käyttää kampanja-alennuksia, kuten yhdistelmä- ja määräalennuksia sekä alennuksia rajan ylittyessä.</span><span class="sxs-lookup"><span data-stu-id="3e547-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="3e547-111">**Huomautus**: nämä asetukset eivät rajoita hinnan ohitustoimintoa, koska se määrittää perushinnan, jota ei pidetä alennuksena.</span><span class="sxs-lookup"><span data-stu-id="3e547-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="3e547-112">[![estä alennukset -kenttä](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="3e547-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

