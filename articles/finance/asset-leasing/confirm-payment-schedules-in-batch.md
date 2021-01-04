---
title: Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina
description: Tässä ohjeaiheessa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5a90b96ac598d145e2b0697627de04731b55f59
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442971"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="52aa3-103">Resurssin vuokrauksen maksuaikataulujen vahvistaminen eräprosessina</span><span class="sxs-lookup"><span data-stu-id="52aa3-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52aa3-104">Tässä ohjeaiheessa kerrotaan, kuinka useita maksuaikatauluja vahvistetaan eräprosessina.</span><span class="sxs-lookup"><span data-stu-id="52aa3-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="52aa3-105">Maksuaikataulut vahvistetaan joko vuokrasopimuksittain tai vahvistuseräprosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="52aa3-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="52aa3-106">Kirjauskansiovienti voidaan kirjata vain vuokrasopimukselle, jolla on vahvistettu maksuaikataulu.</span><span class="sxs-lookup"><span data-stu-id="52aa3-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="52aa3-107">Maksuaikataulun vahvistainen toimii vuokrasopimuksen taloustietojen lopullisena hyväksyntänä.</span><span class="sxs-lookup"><span data-stu-id="52aa3-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="52aa3-108">Kaikkia vuokrasopimuksen taloudellisten tietojen tulevia muutoksia, kuten maksuja ja vuokra-aikoja, pidetään vuokrasopimuksen oikaisuina. Ne on käsiteltävä oikaisuina.</span><span class="sxs-lookup"><span data-stu-id="52aa3-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="52aa3-109">Voit vahvistaa useita maksuaikatauluja noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="52aa3-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="52aa3-110">Siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Vahvistuserä**.</span><span class="sxs-lookup"><span data-stu-id="52aa3-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="52aa3-111">Valitse **Vahvistuserä**-sivulla **Vahvistuserä**.</span><span class="sxs-lookup"><span data-stu-id="52aa3-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="52aa3-112">Suodata näkyviin tulevassa valintaikkunassa ne kirjat, jotka haluat vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="52aa3-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="52aa3-113">Voit vahvistaa kaikki tietyn vuokraryhmän kirjat valitsemalla ryhmän **Vuokraryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="52aa3-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="52aa3-114">Vahvista tietyt kirjat valitsemalla kirjat **Kirjan tunnus**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="52aa3-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="52aa3-115">Vahvista kaikki kirjat ottamalla käyttöön **Kaikille kirjoille** -parametri.</span><span class="sxs-lookup"><span data-stu-id="52aa3-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="52aa3-116">Juuri vahvistettujen kirjojen tiedot näkyvät **Vahvistetut kirjat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="52aa3-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="52aa3-117">Kun maksuaikataulut on vahvistettu, alkuperäiset tuloutuksen kirjauskansioviennit voidaan kirjata vuokrauksille.</span><span class="sxs-lookup"><span data-stu-id="52aa3-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
