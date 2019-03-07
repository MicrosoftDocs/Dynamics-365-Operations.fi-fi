---
title: Johdetut kirjat
description: Tässä artikkelissa on yleiskuvaus johdetun kirjan toiminnoista.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "313908"
---
# <a name="derived-books"></a><span data-ttu-id="80664-103">Johdetut kirjat</span><span class="sxs-lookup"><span data-stu-id="80664-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80664-104">Tässä artikkelissa on yleiskuvaus johdetun kirjan toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="80664-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="80664-105">Johdettujen kirjojen avulla voidaan yksinkertaistaa säännöllisesti ajoitettujen käyttöomaisuuden kirjatapahtumien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="80664-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="80664-106">Voit valita yhden kirjan ensisijaiseksi kirjaksi.</span><span class="sxs-lookup"><span data-stu-id="80664-106">You choose one book as the primary book.</span></span> <span data-ttu-id="80664-107">Valinta on yleensä kirjanpidon poistossa käytettävä kirja.</span><span class="sxs-lookup"><span data-stu-id="80664-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="80664-108">Tämän jälkeen se liitetään muihin kirjoihin, jotka on määritetty kirjaamaan tapahtumat samoille aikaväleille kuin ensisijainen kirja.</span><span class="sxs-lookup"><span data-stu-id="80664-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="80664-109">Verotuksen poistojen kirjat määritetään usein johdettuina kirjoina.</span><span class="sxs-lookup"><span data-stu-id="80664-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="80664-110">Yleisimmät johdettuihin kirjoihin kirjattavaksi määritettävät tapahtumat ovat hankinnat, hankintaoikaisut ja luovutukset.</span><span class="sxs-lookup"><span data-stu-id="80664-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="80664-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="80664-111">Example</span></span>

<span data-ttu-id="80664-112">Hankinta-tapahtumatyypin kirjan A johdetuiksi kirjoiksi on määritetty kirjat B ja C.</span><span class="sxs-lookup"><span data-stu-id="80664-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="80664-113">Kirjalle A syötetään käyttöomaisuuserän 123 hankintatapahtuma, jonka summa on 1 500,00.</span><span class="sxs-lookup"><span data-stu-id="80664-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="80664-114">Kun tapahtuma kirjataan, hankintatapahtuma luodaan ja kirjataan käyttöomaisuuserälle 123 sekä kirjaan B että kirjaan C summalla 1 500,00.</span><span class="sxs-lookup"><span data-stu-id="80664-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="80664-115">Kun valmistelet ensisijaisen kirjan tapahtumia käyttöomaisuuden kirjauskansioon kirjaamista varten, voit tarkastella ja muokata myös johdettujen kirjojen tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="80664-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="80664-116">Jos valmistelet ensisijaisen kirjan tapahtumia toisessa kirjauskansiossa, et voi tarkastella johdettujen arvojen tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="80664-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="80664-117">Ne kirjataan määritetyille tileille ja määritettyihin kirjanpitotasoihin, kun ensisijaisen kirjan tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="80664-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="80664-118">Kirjat, joihin on määritetty tapahtumien kirjaus jollakin muulla aikavälillä kuin ensisijaisessa kirjassa, on liitettävä käyttöomaisuuserään erillisinä kirjoina, ei johdettuina kirjoina.</span><span class="sxs-lookup"><span data-stu-id="80664-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="80664-119">Lisätietoja on kohdassa [Kirjaaminen johdetuissa kirjoissa](post-derived-value-models.md)</span><span class="sxs-lookup"><span data-stu-id="80664-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



