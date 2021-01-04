---
title: Maksulaskujen luominen
description: Tässä ohjeaiheessa käsitellään kuukausittaisia vuokrauksen laskuja. Voit luoda laskuja yksittäisille vuokrasopimuksille tai voit luoda eräkäsittelyn avulla useita vuokrasopimuksia.
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
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442956"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="39212-104">Maksulaskujen luominen</span><span class="sxs-lookup"><span data-stu-id="39212-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39212-105">Voit luoda kuukausittaisia laskuja yksittäisille vuokrasopimuksille tai voit luoda eräkäsittelyn avulla useita vuokrasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="39212-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="39212-106">Seuraavassa kuvataan, miten yksittäisen vuokravienti voidaan luoda, kun **Maksa toimittajalle** -parametri **Vuokrasopimuksen kirjan asetukset** -sivulla on käytössä.</span><span class="sxs-lookup"><span data-stu-id="39212-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="39212-107">Valitse **Vuokrasopimusyhteenveto**-sivulla vuokrasopimus ja valitse sitten **Kirjat \> Maksuaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="39212-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="39212-108">Valitse suoritettava maksu ja valitse sitten **Luo kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="39212-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="39212-109">Näyttöön tulee sanoma, joka osoittaa, että valitulle maksulle on luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="39212-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="39212-110">Valitse **Laskun kirjauskansiot** ja valitse sitten maksettava lasku.</span><span class="sxs-lookup"><span data-stu-id="39212-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="39212-111">Tarkista **Rivit**-välilehdessä kirjauskansiovienti ennen sen kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="39212-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39212-112">Oletusarvon mukaan luotavat toimittajan laskurivit käyttävät toimittajan kirjausprofiilia **Ostoreskontran parametrit** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="39212-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="39212-113">Valitse oikea kirjauskansio ja valitse sitten maksettava lasku.</span><span class="sxs-lookup"><span data-stu-id="39212-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="39212-114">Tässä esimerkissä vuokrasopimuksen kirjan **Maksa toimittajalle** -parametri on käytössä.</span><span class="sxs-lookup"><span data-stu-id="39212-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="39212-115">Näin ollen lasku on laskun kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="39212-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="39212-116">**Yleiskatsaus**-osassa näkyy kirjauskansioviennin yhteenveto, ja **Rivit**-osassa näkyvät todellisten kirjauskansiorivien tiedot.</span><span class="sxs-lookup"><span data-stu-id="39212-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39212-117">Jos **Maksa toimittajalle** -parametri on poistettu käytöstä, maksun kirjauskansioviennit ovat vuokrasopimuksen kirjan **Resurssin vuokraus** -sivulla. Järjestelmä luo resurssin vuokrauksen viennin laskun sijaan.</span><span class="sxs-lookup"><span data-stu-id="39212-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="39212-118">Vuokravienti kirjataan kirjauskansioon, joka määritetään **Kuukausittaisen vuokrauksen kirjauskansio** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="39212-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="39212-119">Kun tapahtuma on kirjattu, voit tarkastella tapahtuman tietoja ja vuokrasopimusvelan arvoa valitsemalla **Velkatapahtumat** vuokrasopimuksen kirjassa.</span><span class="sxs-lookup"><span data-stu-id="39212-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="39212-120">Maksuaikataulussa valitaan **Kirjauskansio kirjattu** -valintaruutu. Rivi näkyy laskun kirjauskansion numerossa.</span><span class="sxs-lookup"><span data-stu-id="39212-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="39212-121">Kun olet luonut kirjauskansion ja viennin luodulle kirjauskansiolle, vienti on peruutettava ennen kuin se voidaan luoda uudelleen.</span><span class="sxs-lookup"><span data-stu-id="39212-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
