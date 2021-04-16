---
title: Kirjaaminen johdettujen kirjojen avulla
description: Tässä artikkelissa kerrotaan, miten johdettuja kirjoja käytetään.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6556965a1356522de5f4c17ddeab378a128fbe3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833015"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="96b87-103">Kirjaaminen johdettujen kirjojen avulla</span><span class="sxs-lookup"><span data-stu-id="96b87-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96b87-104">Tässä artikkelissa kerrotaan, miten johdettuja kirjoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="96b87-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="96b87-105">Kun tapahtuma kirjataan kirjaan, joka sisältää johdettuja kirjoja, johdettua kirjaa koskevat tapahtumat kirjautuvat automaattisesti kirjauskansioihin, ostotilauksiin tai vapaatekstilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="96b87-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="96b87-106">Jos kuitenkin valmistelet ensisijaisen kirjan tapahtumat Käyttöomaisuus-kansioon, voit tarkastella ja muuttaa johdettujen tapahtumien määriä ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="96b87-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="96b87-107">Tietyt tilit, kuten arvonlisävero-, asiakas- tai toimittajatilit, päivittyvät vain kerran ensisijaisen kirjan kirjauksilla.</span><span class="sxs-lookup"><span data-stu-id="96b87-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="96b87-108">Johdetun kirjan tapahtumat kirjautuvat tileille, jotka on määritetty johdetulle kirjalle Käyttöomaisuuserän kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="96b87-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="96b87-109">Hankinta on usein käytetty johdetun kirjan tapahtumalaji.</span><span class="sxs-lookup"><span data-stu-id="96b87-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="96b87-110">Sitä voidaan käyttää, kun kirja ja johdettu kirja olisi liitettävä käyttöomaisuuserään omaisuuserän hankintahetkestä alkaen.</span><span class="sxs-lookup"><span data-stu-id="96b87-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="96b87-111">Myös muita tapahtumatyypin arvoja voi olla käytössä.</span><span class="sxs-lookup"><span data-stu-id="96b87-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="96b87-112">Jos esimerkiksi ensisijaisella kirjalla ja johdetuilla kirjalla on samat myyntiä tai luovutusta koskevat aikavälit, kaikki käyttöomaisuuden tapahtumatyypit ovat käytettävissä johdettua poistokirjaa määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="96b87-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="96b87-113">Johdetussa kirjassa kirjattu poisto on saman suuruinen kuin ensisijaiselle kirjalle kirjattu poisto.</span><span class="sxs-lookup"><span data-stu-id="96b87-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="96b87-114">Jos kahden kirjan poistomenetelmät eivät ole samanlaiset, poistotapahtumia ei pitäisi luoda johdettua prosessia käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="96b87-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="96b87-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96b87-115">Example</span></span> 
<span data-ttu-id="96b87-116">Seuraavaksi kuvataan, miten hankintatapahtumat määritetään johdetun kirjan toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="96b87-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="96b87-117">Luo kirjat Kirjat-sivulle.</span><span class="sxs-lookup"><span data-stu-id="96b87-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="96b87-118">Kirja kirjanpitoa varten: AM 1, Nykyinen kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="96b87-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="96b87-119">Kirja verotusta varten: AM 2, Verotuksen kirjanpitotaso</span><span class="sxs-lookup"><span data-stu-id="96b87-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="96b87-120">Valitse AM 1:ssä Johdetut kirjat -välilehti ja valitse Kirja-kentästä AM 2 ja Tapahtumatyyppi-kentästä Hankinta.</span><span class="sxs-lookup"><span data-stu-id="96b87-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="96b87-121">Kirjat voidaan sitten liittää tiettyihin käyttöomaisuuseriin.</span><span class="sxs-lookup"><span data-stu-id="96b87-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="96b87-122">Kun hankintahinta kirjataan käyttöomaisuudelle, jonka kirja on AM 1, hankintahinta ei kirjaudu vain AM 1:een, vaan myös johdettuun kirjaan AM 2.</span><span class="sxs-lookup"><span data-stu-id="96b87-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="96b87-123">Kummankin käyttöomaisuuskirjan tilaksi päivitetään yleensä Avoin.</span><span class="sxs-lookup"><span data-stu-id="96b87-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="96b87-124">Jos et käytä johdettuja poistokirjoja, sinun on tehtävä käyttöomaisuuden hankintahinnan kirjaus sekä kirjaa AM 1 että kirjaa AM 2 varten.</span><span class="sxs-lookup"><span data-stu-id="96b87-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="96b87-125">Lisätietoja on kohdassa [Johdetut kirjat](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="96b87-125">For more information, see [Derived books](derived-books.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]