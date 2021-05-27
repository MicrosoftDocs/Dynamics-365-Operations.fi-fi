---
title: TDS-laskenta konserniyritysten välisille tapahtumille
description: Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.
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
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023211"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="41f2b-103">TDS-laskenta konserniyritysten välisille tapahtumille</span><span class="sxs-lookup"><span data-stu-id="41f2b-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41f2b-104">Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.</span><span class="sxs-lookup"><span data-stu-id="41f2b-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="41f2b-105">Kun konsernin sisäinen ostotilaus tai myyntitilaus luodaan, asiakkaalle tai toimittajalle määritettyä TDS-oletusryhmää käytetään TDS-summan laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="41f2b-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="41f2b-106">TDS-summa kirjataan palautetuille ostoreskontratileille laskun kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="41f2b-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="41f2b-107">Järjestelmä luo konsernin sisäisen myyntitilauksen tai ostotilauksen automaattisesti alkuperäiselle ostotilaukselle tai myyntitilaukselle.</span><span class="sxs-lookup"><span data-stu-id="41f2b-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="41f2b-108">Oletusarvoinen TDS-ryhmä näkyy konsernin sisäisessä tilauksessa, jotta TDS voidaan laskea.</span><span class="sxs-lookup"><span data-stu-id="41f2b-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="41f2b-109">Voit muuttaa TDS-ryhmää.</span><span class="sxs-lookup"><span data-stu-id="41f2b-109">You can change the TDS group.</span></span> <span data-ttu-id="41f2b-110">Laskun voi kirjata vain, jos konsernin sisäisen tilauksen nettolaskun summa, joka luodaan automaattisesti, vastaa alkuperäisen tilauksen nettolaskun summaa.</span><span class="sxs-lookup"><span data-stu-id="41f2b-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="41f2b-111">(Nettosumma on laskun summa, kun TDS on vähennetty.)</span><span class="sxs-lookup"><span data-stu-id="41f2b-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="41f2b-112">Myyntilasku luodaan esimerkiksi 50 000:lle ja siihen liitetään **10 %**:n TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="41f2b-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="41f2b-113">Kirjatun laskun summa on 45 000, ja myyntilaskun kirjattu TDS-summa on 5 000.</span><span class="sxs-lookup"><span data-stu-id="41f2b-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="41f2b-114">Konsernin sisäiselle myyntitilaukselle luodaan automaattisesti ostotilaus, ja siihen liitetään **10 %**:n TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="41f2b-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="41f2b-115">Jos TDS-ryhmä muutetaan **15 %**:iin, laskua ei voi kirjata, koska automaattisesti luodun konsernin sisäisen myyntitilauksen nettolaskun summa ei vastaa alkuperäisen myyntitilauksen nettolaskun summaa.</span><span class="sxs-lookup"><span data-stu-id="41f2b-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="41f2b-116">Järjestelmä kirjaa automaattisesti maksukirjauskansion, joka luodaan konsernin sisäiselle laskulle.</span><span class="sxs-lookup"><span data-stu-id="41f2b-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="41f2b-117">Kirjauskansion voi kirjata vain, jos sen nettomaksusumma vastaa alkuperäisen maksukirjauskansion nettomaksusummaa.</span><span class="sxs-lookup"><span data-stu-id="41f2b-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
