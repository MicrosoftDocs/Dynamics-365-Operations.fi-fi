---
title: Hybridit asiakastilaukset
description: Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c2105aa99e0489d7643d076e84123eec628679e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022460"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="0d8e1-103">Hybridit asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="0d8e1-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d8e1-104">Hybridi asiakastilaus on yksittäinen tilaus, joka sisältää tuotteita, jotka asiakas voi kuljettaa ulos myymälästä, sekä tuotteita, jotka kerätään tai toimitetaan myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="0d8e1-105">Voit toteuttaa kaupankäynnissä kaikki asiakastilauksen tuotteet tai vain valitut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="0d8e1-106">Tuotteen rivit, jotka on merkitty asiakkaan kuljetettaviksi, automaattisesti laskutetaan tilauksen luonnin jälkeen. Samoin tämä toimii tilauksessa, joka on kerätään sen jälkeen, kun tilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="0d8e1-107">Erääntynyt summa hybriditilauksissa määritetään lisäämällä talletusprosentti poiminnan ja toimituksen tuotteiden riveillä, asiakkaan kuljettamien tuotteiden rivien kokonaissumman kanssa.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="0d8e1-108">Hybriditilauksille järjestelmän tila muuttuu asiakkaan tilauksen tilan ja itsepalvelutukkutilan välillä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0d8e1-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="0d8e1-109">Jos ostoskorin kaikki tuotteet ovat **asiakkaan kuljettamia**, tilausta käsitellään kuin itsepalvelutukkutapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="0d8e1-110">Jos ostoskorin mille tahansa riville on määritetty joko **Kerää** tai **Lähetä toimitus**, tilaus käsitellään asiakastilaustapahtumana.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="0d8e1-111">Jos valitun myyntikorin rivi on valittu ja on myös **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** valittuna, vain tämä tietty ostoskorin rivi on määritetty kyseiselle toimitustavalle.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="0d8e1-112">Tässä tapauksessa prosessi jatkuu tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="0d8e1-113">Kuitenkin jos **Kerää valitut**, **Toimita valitut** tai **Asiakas kuljettaa valitut** on valittu, mutta myyntikorin riviä ei, uusi sivu avautuu, jossa luetellaan kaikki ostoskorin rivit.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="0d8e1-114">Tällä näytöllä voit valita useita rivejä kerralla toimitustavan asettamiseen.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="0d8e1-115">Kun kyseistä menetelmää käytetään rivin valitsemiseen, ohitetaan edelliset toimitustavat, jotka on määritetty riville.</span><span class="sxs-lookup"><span data-stu-id="0d8e1-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d8e1-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0d8e1-116">Additional resources</span></span>

[<span data-ttu-id="0d8e1-117">Modernin myyntipisteen (MPOS) asiakastilaukset</span><span class="sxs-lookup"><span data-stu-id="0d8e1-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)