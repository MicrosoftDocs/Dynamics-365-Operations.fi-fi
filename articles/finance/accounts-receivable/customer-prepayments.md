---
title: Asiakkaan ennakkomaksut
description: Tässä aiheessa kerrotaan, miten asiakkaan ennakkomaksut määritetään ja käsitellään (eli asiakkaan talletukset).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019417"
---
# <a name="customer-prepayments"></a><span data-ttu-id="dcc7d-103">Asiakkaan ennakkomaksut</span><span class="sxs-lookup"><span data-stu-id="dcc7d-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcc7d-104">Asiakkaan ennakkomaksuja käytetään, kun vastaanotat maksun asiakkaalta, mutta ei ole laskua, jota vasten maksun voi tilittää.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="dcc7d-105">Näitä maksutyyppejä kutsutaan myös asiakkaan talletuksiksi.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="dcc7d-106">Asiakkaan ennakkomaksujen määrittäminen ja käsitteleminen käsittää seuraavat perusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="dcc7d-107">Luo ennakkomaksujen asiakkaan kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="dcc7d-108">Määritä **Ennakkomaksukirjauskansion kirjausprofiili** -parametri.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="dcc7d-109">Luo asiakkaan maksukirjauskansio ja valitse kullekin riville **Ennakkomaksukirjauskansion tosite** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="dcc7d-110">Kirjaa asiakasmaksujen kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="dcc7d-111">Kun lasku on luotu, tilitä ennakkomaksu sen kanssa **Tilitä avoimet tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="dcc7d-112">Luo ennakkomaksujen asiakkaan kirjausprofiili</span><span class="sxs-lookup"><span data-stu-id="dcc7d-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="dcc7d-113">Yleensä kun hyväksyt asiakkaiden ennakkomaksut tai talletukset ennen tuotteiden tai palvelujen toimitusta tai ennen kuin järjestelmässä on lasku, haluat kirjata käteisen velkana varan sijaan tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="dcc7d-114">Näiden summien kirjanpitoon kirjaamista koskevat vaatimukset saattavat kuitenkin vaihdella maan tai alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="dcc7d-115">Varmista siksi, että kysyt kirjanpitäjiltäsi paikallisista säädöksistä.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="dcc7d-116">Ennakkomaksuissa käytettävä kirjausprofiilin luontiprosessi on yleensä sama kuin muiden kirjausprofiilien luontiprosessi.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="dcc7d-117">Ensisijainen ero on **Yhteenvetotili**-kentässä valittava päätili.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="dcc7d-118">Lisätietoja on kohdassa [Asiakkaan kirjausprofiilit](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="dcc7d-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="dcc7d-119">Asiakkaan ennakkomaksujen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dcc7d-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="dcc7d-120">Kaksi myyntireskontran pääparametria on otettava huomioon, kun asiakkaan ennakkomaksujen järjestelmää määritetään.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="dcc7d-121">Määritä parametrit näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="dcc7d-122">Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="dcc7d-123">Valinnainen: Määritä **Kirjanpito ja arvonlisävero** -välilehdessä **Maksu**-pikavälilehdessä **Ennakkomaksukirjauskansion tositteen arvonlisävero** -kohdan asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="dcc7d-124">Valitse **Ennakkomaksukirjauskansion kirjausprofiili** -kentässä asiakkaan kirjausprofiili, jota käytetään asiakkaan ennakkomaksuja kirjattaessa.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="dcc7d-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="dcc7d-126">Asiakkaan ennakkomaksutositteiden luominen</span><span class="sxs-lookup"><span data-stu-id="dcc7d-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="dcc7d-127">Kun luot asiakkaan maksukirjauskansion, jokaisen ennakkomaksun kohdalla on määritettävä **Ennakkomaksukirjauskansion tosite** -kohdan asetukseksi **Kyllä** **Asiakkaan maksukirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="dcc7d-128">Luo asiakkaan ennakkomaksu noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="dcc7d-129">Valitse **Myyntireskontra \> Maksut \> Asiakkaan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="dcc7d-130">Luo kirjauskansio valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="dcc7d-131">Valitse **Nimi**-kentästä käytettävä kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="dcc7d-132">Jos määrität **Ennakkomaksukirjauskansion tositteen arvonlisävero** -kohdan asetukseksi **Kyllä** edellisessä menetelmässä, sinun on valittava kirjauskansion nimi, jossa **Summa sisältää arvonlisäveron** -parametri on valittuna.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="dcc7d-133">Valinnainen: Anna kuvaus **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="dcc7d-134">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-134">Select **Lines**.</span></span>
6. <span data-ttu-id="dcc7d-135">Jos tyhjää riviä ei ole, luo rivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="dcc7d-136">Anna **Päivämäärä**-kenttään päivämäärä, jona ennakkomaksun kirjaus tulisi tehdä.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="dcc7d-137">Valitse **Tili**-kentässä asiakas ennakkomaksua varten.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="dcc7d-138">Valinnainen: Anna tapahtuman kuvaus **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="dcc7d-139">Syötä **Kredit**-kenttään ennakkomaksun summa.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="dcc7d-140">Valitse **Vastatili**-kentässä tili, jolle maksu vastakirjataan.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="dcc7d-141">Valitse esimerkiksi pankkitili tai päätili, jolle maksu kirjataan.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="dcc7d-142">Valitse **Maksutapa**-kentässä asiakkaan maksutapa.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="dcc7d-143">Määritä **Maksu**-välilehdessä **Ennakkomaksukirjauskansion tosite** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="dcc7d-144">Toista vaiheet 7–13 jokaiselle kirjattavalle lisäennakkomaksulle.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="dcc7d-145">Viimeistele kirjauskansio valitsemalla **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="dcc7d-146">Laskun sisältävien ennakkomaksujen tilittäminen</span><span class="sxs-lookup"><span data-stu-id="dcc7d-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="dcc7d-147">**Asiakasmaksut**-työtilan avulla voit helposti etsiä ja tilittää maksuja, joita ei ole tilitetty kokonaan.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="dcc7d-148">Valitse **Aloitussivu**-koontinäytössä **Asiakasmaksu**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="dcc7d-149">**Asiakastapahtumat**-osassa **Maksamattomat laskut** -välilehdessä etsi ja valitse tilitettävä maksu.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="dcc7d-150">Valitse **Selvitä tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="dcc7d-151">Valitse **Merkitse**-valintaruutu tilitettävän laskun ja maksun kohdalla.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="dcc7d-152">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="dcc7d-152">Select **Post**.</span></span>

<span data-ttu-id="dcc7d-153">Lisätietoja avointen tapahtumien tilityksestä on kohdassa [Tilityksen yleiskatsaus](/cash-bank-management/settlement-overview.md)</span><span class="sxs-lookup"><span data-stu-id="dcc7d-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
