---
title: "Käyttöomaisuuden poisto"
description: "Tämä ohjeaihe sisältää käyttöomaisuuden poiston yleiskatsauksen."
author: twheeloc
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b1d4ced73ed3ce486c33a59ae1de40b8b8444673
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="5f329-103">Käyttöomaisuuden poisto</span><span class="sxs-lookup"><span data-stu-id="5f329-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f329-104">Tämä ohjeaihe sisältää käyttöomaisuuden poiston yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="5f329-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="5f329-105">Poisto on kausittainen tapahtuma, joka yleensä vähentää käyttöomaisuuserän tasearvoa ja kirjataan kuluksi tulostilille.</span><span class="sxs-lookup"><span data-stu-id="5f329-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="5f329-106">Tämän vuoksi päätiliä käytetään yleensä taseen kausittaisen poiston hyvittämiseen.</span><span class="sxs-lookup"><span data-stu-id="5f329-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="5f329-107">Vastatili on tilikartan tuloslaskelmaosaan kuuluva tili.</span><span class="sxs-lookup"><span data-stu-id="5f329-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="5f329-108">Poistojen oikaisu</span><span class="sxs-lookup"><span data-stu-id="5f329-108">Depreciation adjustment</span></span>
<span data-ttu-id="5f329-109">Poiston oikaisuksi kirjataan yleensä vain aiemmin kirjatun poistotapahtuman korjaus.</span><span class="sxs-lookup"><span data-stu-id="5f329-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="5f329-110">Siksi sekä pää- että vastatili määritetään samaan tapaan kuin poistoissa käytettävät tilit.</span><span class="sxs-lookup"><span data-stu-id="5f329-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="5f329-111">Poistojen oikaisun summa voi olla positiivinen tai negatiivinen, mutta päätili (tasetilinä) ja vastatili (yleensä tulostilinä) toimivat samaan tapaan.</span><span class="sxs-lookup"><span data-stu-id="5f329-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="5f329-112">Erikoispoisto</span><span class="sxs-lookup"><span data-stu-id="5f329-112">Extraordinary depreciation</span></span>
<span data-ttu-id="5f329-113">Erikoispoisto toimii samalla tavoin kuin peruspoisto.</span><span class="sxs-lookup"><span data-stu-id="5f329-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="5f329-114">Poistosumma hyvitetään taseeseen ja käyttöomaisuuserän arvoa vähennetään päätilin avulla.</span><span class="sxs-lookup"><span data-stu-id="5f329-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="5f329-115">Vastatili on tulostili, jolle tilikaudelta laskettu poisto kirjataan kuluna.</span><span class="sxs-lookup"><span data-stu-id="5f329-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="5f329-116">Erikoispoisto toimii peruspoistosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="5f329-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="5f329-117">Koska erikoispoisto on erillinen tapahtumatyyppi, se voidaan kirjata ja raportoida tavallisesta poistosta erillisenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="5f329-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="5f329-118">Erityinen poistovähennys</span><span class="sxs-lookup"><span data-stu-id="5f329-118">Special depreciation allowance</span></span>
<span data-ttu-id="5f329-119">Erityisillä poistovähennyksillä voidaan tehdä ylimääräisiä poistoja sinä vuonna, jona käyttöomaisuuserä otetaan käyttöön ja siitä tehdään poisto ensimmäistä kertaa.</span><span class="sxs-lookup"><span data-stu-id="5f329-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="5f329-120">Erityiset poistovähennykset on suoritettava ennen muiden poistojen laskemista.</span><span class="sxs-lookup"><span data-stu-id="5f329-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="5f329-121">Koska erityiset poistovähennykset tunnistetaan yleensä vasta myöhemmin käyttöomaisuuserän käyttöiän aikana, kannattaa käyttää tämäntyyppiseen poistoon kirjaa, jota ei kirjata kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="5f329-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="5f329-122">Voit käyttää kausittaista Poista kirjanpitoon kirjaamattomat tapahtumat -toimintoa ja poistaa aiempia tapahtumia näistä kirjoista.</span><span class="sxs-lookup"><span data-stu-id="5f329-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="5f329-123">Voit sitten poistaa poistohistorian kiinteän käyttöomaisuuden kirjasta, kirjata erityisen poiston, kun se on tunnistettu, ja kirjata jäljellä olevat vuoden poistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5f329-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="5f329-124">Erityisten poistovähennysten tietueita voidaan luoda rajattomasti.</span><span class="sxs-lookup"><span data-stu-id="5f329-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="5f329-125">Kun tietueet on määritetty käyttöomaisuusryhmän kirjaan, niitä käytetään käyttöomaisuuserän poistokirjassa.</span><span class="sxs-lookup"><span data-stu-id="5f329-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="5f329-126">Erityiset poistovähennykset kirjataan prosenttina tai kiinteänä summana.</span><span class="sxs-lookup"><span data-stu-id="5f329-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="5f329-127">Erityisiä poistovähennyksiä kirjattaessa tapahtumat kirjataan kirjaan poistotapahtumista erillisinä tapahtumina.</span><span class="sxs-lookup"><span data-stu-id="5f329-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="5f329-128"> Poistokalenterit</span><span class="sxs-lookup"><span data-stu-id="5f329-128">Depreciation calendars</span></span>
<span data-ttu-id="5f329-129">Jokaisessa kirjassa on kalenteri, jota käytetään käyttöomaisuuden poistoissa.</span><span class="sxs-lookup"><span data-stu-id="5f329-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="5f329-130">Kirja käyttää oletuksena kirjanpidon vuosikalenteria, jos kalenteria ei määritetä kirjassa.</span><span class="sxs-lookup"><span data-stu-id="5f329-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="5f329-131">Kirjalle on valittava kirjanpidon vuosikalenteri, kun kirjaan liitetty poistoprofiili käyttää kirjanpidollista poistovuotta.</span><span class="sxs-lookup"><span data-stu-id="5f329-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="5f329-132">Voit luoda yhteisiä kalentereita **Kirjanpidon kalenterit** -sivulla Kirjanpito-osiossa.</span><span class="sxs-lookup"><span data-stu-id="5f329-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="5f329-133">Lisätietoja on kohdassa [Poistomenetelmät ja -käytännöt](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="5f329-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>




