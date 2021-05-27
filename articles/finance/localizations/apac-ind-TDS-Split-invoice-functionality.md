---
title: Jaetun laskun toiminnot
description: Tässä aiheessa kuvataan asetuksia ja toimintoja laskujen jakamiseen toimitusosoitteen ja verotilinumeron (TAN) mukaan.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023213"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="ba09d-103">Jaetun laskun toiminnot</span><span class="sxs-lookup"><span data-stu-id="ba09d-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba09d-104">Tässä aiheessa kuvataan asetuksia ja toimintoja laskujen jakamiseen toimitusosoitteen ja verotilinumeron (TAN) mukaan.</span><span class="sxs-lookup"><span data-stu-id="ba09d-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="ba09d-105">Valitse **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdestä **Tuotevastaanotto**- tai **Lasku**-valintaruutu, kun haluat kirjata ja jakaa **Ostotilaus**-sivulla tuotteen vastaanoton tai laskun, jolla on eri toimitusosoitteet ja TAN-numerot.</span><span class="sxs-lookup"><span data-stu-id="ba09d-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="ba09d-106">Kirjattu lasku jaetaan tämän jälkeen toimitusosoitteen ja TAN-numeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="ba09d-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="ba09d-107">**Yhteenvedon päivitys** -välilehdessä **Jaon peruste** -pikavälilehden **Toimitustiedot**-rivillä määritä **Vahvistus**-, **Keräysluettelo**-, **Pakkausluettelo**- tai **Lasku**-vaihtoehdon arvoksi **Kyllä**, jos haluat kirjata ja jakaa vahvistuksen, keräysluettelon, pakkausluettelon tai laskun, jossa eri toimitusosoitteet ja TAN-numerot on määritetty eri laskuriveille **Myyntitilaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ba09d-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="ba09d-108">Lasku jaetaan ensin toimitusosoitteen ja sitten TAN-numeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="ba09d-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="ba09d-109">Jos **Toimitustiedot**-vaihtoehtojen asetuksena ei ole **Kyllä**, lasku kirjataan yhtenä laskuna.</span><span class="sxs-lookup"><span data-stu-id="ba09d-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="ba09d-110">Laskun jakoa ei tapahdu.</span><span class="sxs-lookup"><span data-stu-id="ba09d-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="ba09d-111">Jos haluat jakaa ja kirjata pakkausluettelon, jossa laskuriveillä on eri toimitusosoitteet ja TAN-numerot, määritä **Pakkausluettelo**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ba09d-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="ba09d-112">Jos haluat jakaa ja kirjata laskun, jossa laskuriveillä on eri toimitusosoitteet ja TAN-numerot, määritä **Lasku**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ba09d-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="ba09d-113">Jos haluat kirjata laskun, jossa laskuriveillä on eri toimitusosoitteet mutta samat TAN-numerot, määritä **Lasku**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ba09d-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="ba09d-114">Lasku jaetaan toimitusosoitteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ba09d-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="ba09d-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="ba09d-115">Example</span></span>

<span data-ttu-id="ba09d-116">Tässä esimerkissä **Lasku**-asetus on **Toimitustiedot**-kohdassa **Kyllä** **Ostoreskontran parametrit** -sivun **Yhteenvedon päivitys** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ba09d-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="ba09d-117">Ostolasku kirjataan, ja sen riveillä on seuraavat toimitusosoitteiden ja TAN-numeroiden asetukset:</span><span class="sxs-lookup"><span data-stu-id="ba09d-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="ba09d-118">**Nimikerivi 1:** Toimitusosoite 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="ba09d-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="ba09d-119">**Nimikerivi 2:** Toimitusosoite 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="ba09d-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="ba09d-120">**Nimikerivi 3:** Toimitusosoite 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="ba09d-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="ba09d-121">**Nimikerivi 4:** Toimitusosoite 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="ba09d-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="ba09d-122">Tällöin alkuperäinen lasku jaetaan kahteen laskuun ja kirjataan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ba09d-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="ba09d-123">Lasku 1 kirjataan nimikeriville 1 ja nimikeriville 2, koska molemmilla riveillä on sama toimitusosoite ja TAN.</span><span class="sxs-lookup"><span data-stu-id="ba09d-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="ba09d-124">Lasku 2 kirjataan nimikeriville 3.</span><span class="sxs-lookup"><span data-stu-id="ba09d-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="ba09d-125">Lasku 3 kirjataan nimikeriville 4.</span><span class="sxs-lookup"><span data-stu-id="ba09d-125">Invoice 3 is posted for item line 4.</span></span>
