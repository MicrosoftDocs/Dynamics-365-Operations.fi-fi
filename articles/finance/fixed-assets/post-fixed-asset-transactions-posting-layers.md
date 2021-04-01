---
title: Käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin
description: Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a52374d52b3dcd435c79033d462a2982316a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240855"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="dea76-103">Käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin</span><span class="sxs-lookup"><span data-stu-id="dea76-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dea76-104">Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="dea76-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="dea76-105">Käyttöomaisuus poistetaan yleensä eri tavoin eri tarkoituksissa.</span><span class="sxs-lookup"><span data-stu-id="dea76-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="dea76-106">Verotuksessa poisto lasketaan nykyisillä verosäännöillä, jotta poisto ennen veroja on suurin mahdollinen, mutta raportoinnissa poisto lasketaan kirjanpitolakien ja -standardien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dea76-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="dea76-107">Erilaiset poistot lasketaan ja kirjataan kirjaustasoille erikseen.</span><span class="sxs-lookup"><span data-stu-id="dea76-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="dea76-108">Kullekin käyttöomaisuuteen liitetylle kirjalle on määritetty tietty kirjanpitotaso, jolla on yleinen poistotavoite.</span><span class="sxs-lookup"><span data-stu-id="dea76-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="dea76-109">Kirjanpitotasoja on kymmenen: Nykyinen, Liiketoiminnot, Vero ja seitsemän mukautettua tasoa</span><span class="sxs-lookup"><span data-stu-id="dea76-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="dea76-110">Kirjanpitokirjaukset voi poistaa käytöstä asettamalla Kirjaa kirjanpitoon -kentän arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="dea76-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="dea76-111">Kirjanpitotaso -kenttään määritetään automaattisesti Ei.</span><span class="sxs-lookup"><span data-stu-id="dea76-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="dea76-112">Kirjoja, joita ei kirjata pääkirjanpitoon, käytetään yleensä veroraportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="dea76-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="dea76-113">Tämän ansiosta voit poistaa menneitä tapahtumia käyttöomaisuuskirjasta, koska niitä ei ole vahvistettu kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="dea76-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="dea76-114">Käyttöomaisuuden kirjauskansiot määritetään Kirjauskansionimet sivulla kohdassa kirjanpito > kirjauskansion asetukset > kirjauskansionimet.</span><span class="sxs-lookup"><span data-stu-id="dea76-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="dea76-115">Kukin kirjauskansio, johon poistoja voi kirjata, määritetään vain yhdelle kirjaustasolle sen kirjauskansionimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="dea76-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="dea76-116">Kirjauskansion kirjanpitotasoa ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="dea76-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="dea76-117">Tämän rajoituksen avulla varmistetaan, että kunkin kirjanpitotason tapahtumat säilytetään erillään.</span><span class="sxs-lookup"><span data-stu-id="dea76-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="dea76-118">Kullekin kirjaustasolle on luotava vähintään yksi kirjauskansionimi.</span><span class="sxs-lookup"><span data-stu-id="dea76-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="dea76-119">Jos käytät kirjoja, joita ei kirjata kirjanpitoon, sinun on luotava kirjauskansio, jossa kirjanpitotasoksi on määritetty Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="dea76-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="dea76-120">Voit määrittää kirjanpitotilejä käyttöomaisuustapahtumille Käyttöomaisuuserän kirjausprofiili -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dea76-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="dea76-121">Valitse kullekin kirjausprofiilille asianmukainen tapahtumatyyppi ja kirja ja määritä sitten kirjanpitotilit.</span><span class="sxs-lookup"><span data-stu-id="dea76-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="dea76-122">Määritä kirjausprofiilin tietue erikseen jokaiselle kirjalle, joka kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="dea76-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="dea76-123">Käyttöomaisuus voidaan syöttää vain asiakirjoihin, jotka tukevat **Nykyinen**-kirjaustasoa, kuten **ostotilaus**, **odottava toimittajan lasku**, **myyntitilaus** tai **vapaatekstilasku**.</span><span class="sxs-lookup"><span data-stu-id="dea76-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="dea76-124">Kun käyttöomaisuuserän tunnus valitaan jossakin näistä asiakirjoista, käyttöomaisuuskirja suodatetaan kirjassa **Nykyinen**-kirjaustason mukaan. Se täytetään automaattisesti kirjauksen aikana, kun järjestelmä tarkistaa, että käyttöomaisuuden kirjaustaso on **Nykyinen**.</span><span class="sxs-lookup"><span data-stu-id="dea76-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="dea76-125">Jos tätä vahvistusta ei voi suorittaa, kirjausprosessi pysäytetään.</span><span class="sxs-lookup"><span data-stu-id="dea76-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="dea76-126">Käyttämällä johdettuja arvomalleja voit kirjata tapahtumia eri kirjaustasoille samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="dea76-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="dea76-127">Ensisijaisen kirjan tapahtumat luodaan kirjauskansioon tai lähdeasiakirjaan, jonka kirjaustaso vastaa kirjan kirjaustasoa.</span><span class="sxs-lookup"><span data-stu-id="dea76-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="dea76-128">Kirjauksen aikana johdetun kirjan tapahtumat kirjataan asianmukaisille kirjaustasoille.</span><span class="sxs-lookup"><span data-stu-id="dea76-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="dea76-129">Lisätietoja on kohdassa [Johdetut kirjat](derived-books.md) ja [Kirjaaminen johdettujen kirjojen avulla](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="dea76-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]