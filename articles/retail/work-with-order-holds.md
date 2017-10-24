---
title: Tilausten pidot
description: "Tämän ohjeaihe kuvaa tilausten pitoja Dynamics 365 for Retailissa."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="order-holds"></a><span data-ttu-id="214e3-103">Tilausten pidot</span><span class="sxs-lookup"><span data-stu-id="214e3-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="214e3-104">Tämän ohjeaihe kuvaa tilausten pitoja Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="214e3-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="214e3-105">Tilaus voidaan asettaa pitoon monesta eri syystä.</span><span class="sxs-lookup"><span data-stu-id="214e3-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="214e3-106">Saatat esimerkiksi asettaa tilauksen pitoon, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa, tai kunnes päällikkö voi tarkistaa asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="214e3-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="214e3-107">Myyntiprosessin aikana on tilanteita, jolloin myyntitilauksia on asetettava pitoon.</span><span class="sxs-lookup"><span data-stu-id="214e3-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="214e3-108">Myyntitilaus saatetaan esimerkiksi asettaa pitoon asiakkaan maksuun liittyvien ongelmien tai petosepäilyn vuoksi, tai esimiehen tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="214e3-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="214e3-109">Kun ostotilaus asetetaan pitoon, sille liitetään tilauksen pitokoodi ilmaisemaan pidossa olon syy.</span><span class="sxs-lookup"><span data-stu-id="214e3-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="214e3-110">Myyntitilausteen pitokoodit määritetään kohdassa **Myynti ja markkinointi** &gt; **Asetukset** &gt; **Myyntitilaukset** &gt; **Tilauksen pitokoodit**.</span><span class="sxs-lookup"><span data-stu-id="214e3-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="214e3-111">Myyntitilaus voidaan asettaa pitoon manuaalisesti tilauksen luonnin yhteydessä tai myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="214e3-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="214e3-112">Tilaus voidaan myös asettaa pitoon automaattisesti petossääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="214e3-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="214e3-113">Myyntitilauksen ollessa pidossa, sitä saattaa olla tarpeen päivittää lisätiedoilla.</span><span class="sxs-lookup"><span data-stu-id="214e3-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="214e3-114">Voit vaihtoehtoisesti tarkistaa myyntitilauksen samalla, kun jatkat sen työstämistä.</span><span class="sxs-lookup"><span data-stu-id="214e3-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="214e3-115">Voit kuitata myyntitilauksen ulos, kirjata sen uudelleen sisään ja jopa korvata toisen käyttäjän uloskirjauksen käyttämällä tilauksen pidon työtilaa (**Vähittäismyynti ja kauppa** &gt; **Asiakkaat** &gt; **Tilausten pidot**).</span><span class="sxs-lookup"><span data-stu-id="214e3-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="214e3-116">Kun tilaus on valmis viimeisteltäväksi, sinun on poistettava pito ennen, kuin voit viimeistellä tilausprosessin.</span><span class="sxs-lookup"><span data-stu-id="214e3-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




