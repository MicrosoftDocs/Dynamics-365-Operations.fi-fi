---
title: "Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana"
description: "Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 67aa0b89eed1f82290659029dfcce92ca3710aea
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="f67ff-103">Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana</span><span class="sxs-lookup"><span data-stu-id="f67ff-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f67ff-104">Yksi laskujen täsmäytyksen tarkistamisen tyyppi on laskusummien täsmäytys.</span><span class="sxs-lookup"><span data-stu-id="f67ff-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="f67ff-105">Määritä järjestelmä suorittamaan laskusummien täsmäytys **Ostoreskontran parametrit** sivun **Laskun oikeellisuustarkistus** -välilehdellä asettamalla **Täsmäytä laskusummat** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f67ff-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="f67ff-106">Voit käyttää laskujen kokonaissummien täsmäytystä varmistamaan, että laskujen kokonaissummien ja odotettujen summien erot ovat hyväksyttävän toleranssin sisällä.</span><span class="sxs-lookup"><span data-stu-id="f67ff-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="f67ff-107">Kuutta kokonaissummaa verrataan **Laskusummien täsmäytyksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f67ff-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="f67ff-108">Jos mikään loppusummista eroaa vastaavan ostotilaussumman odotetusta määrästä, merkitään täsmäytysristiriita.</span><span class="sxs-lookup"><span data-stu-id="f67ff-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="f67ff-109">Voit tarkastella laskua, jolla on loppusumman täsmäytysristiriita, **Toimittajan laskun syöttö** -työtilassa valitsemalla **Odottavat laskut** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f67ff-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="f67ff-110">Valitse sitten Toimintoruudun **Tarkista**-välilehdellä **Täsmäytyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f67ff-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="f67ff-111">Jos täsmäytysristiriitoja on havaittu, laskun summan viereen ilmestyy varoituskuvake.</span><span class="sxs-lookup"><span data-stu-id="f67ff-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="f67ff-112">Voit tarkastella summia yksityiskohtaisemmin tarkastelemalla laskusummien täsmäytyksen tietoja.</span><span class="sxs-lookup"><span data-stu-id="f67ff-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="f67ff-113">Kun olet löytänyt ristiriidan, sinun on ehkä otettava yhteys toimittajaan, jos laskun tiedot ovat mielestäsi virheelliset.</span><span class="sxs-lookup"><span data-stu-id="f67ff-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="f67ff-114">Suorita sitten jokin seuraavista toimista sen mukaan, millaiseen sopimukseen pääset toimittajan kanssa:</span><span class="sxs-lookup"><span data-stu-id="f67ff-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="f67ff-115">Hyväksy hintojen ero ja kirjaa täsmäytysristiriitoja sisältävä lasku.</span><span class="sxs-lookup"><span data-stu-id="f67ff-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="f67ff-116">Järjestelmäsi saattaa olla määritetty edellyttämään hyväksynnän ennen laskun kirjaamista, jos sillä on täsmäytysristiriitoja.</span><span class="sxs-lookup"><span data-stu-id="f67ff-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="f67ff-117">Tässä tapauksessa sinun on hyväksyttävä täsmäytysristiriita ja valinnaisesti syöttää hyväksyntää koskeva kommentti.</span><span class="sxs-lookup"><span data-stu-id="f67ff-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="f67ff-118">Voit sitten valita laskun kirjaamisen.</span><span class="sxs-lookup"><span data-stu-id="f67ff-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="f67ff-119">Muuta laskun summa odotetun summan mukaiseksi ja kirjaa lasku.</span><span class="sxs-lookup"><span data-stu-id="f67ff-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="f67ff-120">Pyydä toimittajalta täysi hyvitys ja uusi korjattu lasku.</span><span class="sxs-lookup"><span data-stu-id="f67ff-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="f67ff-121">Lisätietoja on ohjeaiheessa [Poikkeusten tutkiminen ja selvittäminen](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="f67ff-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



