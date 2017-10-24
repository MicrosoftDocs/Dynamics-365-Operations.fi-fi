---
title: "Käteisalennukset"
description: "Käteisalennukset määritetään ja jaetaan osto- ja myyntireskontrassa.  Käytettävissä oleva käteisalennus voidaan määrittää myyntilaskulla tai toimittajan laskulla. Se käytetään, jos lasku maksetaan käteisalennuksen päivänä."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 668e3ebdd2729efb48e2833fd5beec3cefdb17b0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="cash-discounts"></a><span data-ttu-id="946bc-104">Käteisalennukset</span><span class="sxs-lookup"><span data-stu-id="946bc-104">Cash discounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="946bc-105">Käteisalennukset määritetään ja jaetaan osto- ja myyntireskontrassa.</span><span class="sxs-lookup"><span data-stu-id="946bc-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="946bc-106">Käytettävissä oleva käteisalennus voidaan määrittää myyntilaskulla tai toimittajan laskulla. Se käytetään, jos lasku maksetaan käteisalennuksen päivänä.</span><span class="sxs-lookup"><span data-stu-id="946bc-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="946bc-107">Käteisalennukset</span><span class="sxs-lookup"><span data-stu-id="946bc-107">Cash discounts</span></span>
--------------

<span data-ttu-id="946bc-108">Asiakkaiden ja toimittajien käteisalennuksia luodaan Käteisalennukset-sivulla.</span><span class="sxs-lookup"><span data-stu-id="946bc-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="946bc-109">Voit lisäksi määrittää Seuraava alennuskoodi -kentässä sarjan peräkkäisiä käteisalennuksia, jotka tulevat voimaan, kun edellisen vanhenee.</span><span class="sxs-lookup"><span data-stu-id="946bc-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="946bc-110">Lisätietoja on myöhemmin tässä aiheessa kohdassa Esimerkki: käteisalennussarja.</span><span class="sxs-lookup"><span data-stu-id="946bc-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="946bc-111">Jos lasku, hyvitystapahtuma (maksu tai hyvityslasku) tai molemmat annetaan jonain muuna valuuttana kuin yrityksen kirjanpitovaluuttana, käteisalennus lasketaan käyttämällä vaihtokurssia, joka perustuu maksun tai hyvityslaskun päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="946bc-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="946bc-112">Jos lasku tai luottoasiakirja annetaan eri yrityksille ja jos yrityksillä on eri kirjanpitovaluutat, vaihtokurssi haetaan laskun yrityksestä luottoasiakirjan päivämäärällä.</span><span class="sxs-lookup"><span data-stu-id="946bc-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="946bc-113">Lisätietoja on myöhemmin tässä aiheessa kohdassa Esimerkki: käteisalennusten vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="946bc-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="946bc-114">Käteisalennuksen päätilin oletusjärjestys</span><span class="sxs-lookup"><span data-stu-id="946bc-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="946bc-115">Jos lasku maksetaan käteisalennukseen oikeuttavassa määräajassa, käteisalennus kirjataan automaattisesti käteisalennuksen päätilille seuraavassa oletusjärjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="946bc-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="946bc-116">Asiakkaan Tilitä avoimet tapahtumat -sivun tai toimittajan Tilitä avoimet tapahtumat -sivun Vaihtoehtoinen käteisalennustili -kentässä määritetty päätili.</span><span class="sxs-lookup"><span data-stu-id="946bc-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="946bc-117">Päätili, joka on määritetty sen kirjanpidon kirjausryhmän Asiakkaan käteisalennus- tai Toimittajan käteisalennus -kentässä, joka on liitetty laskun arvonlisäverokoodiin.</span><span class="sxs-lookup"><span data-stu-id="946bc-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="946bc-118">Määritä kirjanpidon kirjausryhmät Kirjanpidon kirjausryhmät -sivulla ja määritä ne Arvolisäverokoodi-sivun arvonlisäverokoodeihin.</span><span class="sxs-lookup"><span data-stu-id="946bc-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="946bc-119">Pääkirjaustili, joka on tilitetyssä laskussa olevan käteisalennuskoodin Käteisalennukset-sivun Asiakkaan alennusten päätili- tai Toimittajan alennusten päätili -kentässä.</span><span class="sxs-lookup"><span data-stu-id="946bc-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="946bc-120">Automaattisten tapahtumien tilit -sivulla määritetty käteisalennusten päätili.</span><span class="sxs-lookup"><span data-stu-id="946bc-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="946bc-121"> Esimerkki: käteisalennussarja</span><span class="sxs-lookup"><span data-stu-id="946bc-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="946bc-122">Määritä kolme käteisalennuskoodia seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="946bc-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="946bc-123">Koodi 5D10% – 10 %:n käteisalennus, jos lasku maksetaan 5 päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="946bc-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="946bc-124">Koodi 10D5% – 5 %:n käteisalennus, jos lasku maksetaan 10 päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="946bc-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="946bc-125">Koodi 14D2% – 2 %:n käteisalennus, jos lasku maksetaan 14 päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="946bc-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="946bc-126">Seuraava alennuskoodi -kenttä:</span><span class="sxs-lookup"><span data-stu-id="946bc-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="946bc-127">Valitse koodille 5D10% vaihtoehto 10D5%.</span><span class="sxs-lookup"><span data-stu-id="946bc-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="946bc-128">Valitse koodille 10D5% vaihtoehto 14D2%.</span><span class="sxs-lookup"><span data-stu-id="946bc-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="946bc-129">Jätä 14P2%-koodin osalta Seuraava alennuskoodi -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="946bc-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="946bc-130">Kolme käteisalennusta seuraavat toisiaan, kun maksupäivä ylittää laskun edellisen käteisalennuspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="946bc-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="946bc-131">Laskua maksettaessa voi käyttää vain yhtä alennuskoodia sen perusteella, mikä käteisalennussarjan käteisalennuspäivämäärä toteutuu.</span><span class="sxs-lookup"><span data-stu-id="946bc-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="946bc-132"> Esimerkki: käteisalennusten vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="946bc-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="946bc-133">Yrityksen kirjanpitovaluutta on euro ja Yhdysvaltain dollarille on määritetty seuraavat vaihtokurssit:</span><span class="sxs-lookup"><span data-stu-id="946bc-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="946bc-134">1. helmikuuta = 110.</span><span class="sxs-lookup"><span data-stu-id="946bc-134">February 1 = 110</span></span>
-   <span data-ttu-id="946bc-135">1. maaliskuuta = 80</span><span class="sxs-lookup"><span data-stu-id="946bc-135">March 1 = 80</span></span>

<span data-ttu-id="946bc-136">1 000 dollarin lasku kirjataan 15.2. käteisalennusehdolla 20D2%.</span><span class="sxs-lookup"><span data-stu-id="946bc-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="946bc-137">Laskun summa kirjanpitovaluutassa on 1 100 EUR</span><span class="sxs-lookup"><span data-stu-id="946bc-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="946bc-138">980 dollarin maksu täsmäytetään laskun kanssa 1.3.</span><span class="sxs-lookup"><span data-stu-id="946bc-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="946bc-139">Käteisalennussumma on 20 dollaria.</span><span class="sxs-lookup"><span data-stu-id="946bc-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="946bc-140">Maksun summa kirjanpitovaluuttana on 784 euroa.</span><span class="sxs-lookup"><span data-stu-id="946bc-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="946bc-141">Käteisalennuksen summa kirjanpitovaluuttana lasketaan käyttämällä maaliskuun 1. päivän vaihtokurssia : 20 \* 80 / 100 = 16 euroa.</span><span class="sxs-lookup"><span data-stu-id="946bc-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>
| <span data-ttu-id="946bc-142">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="946bc-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946bc-143">Jos Myyntireskontran parametrit- tai Ostoreskontran parametrit -sivulla valitaan Laske käteisalennukset osamaksuille -vaihtoehto, käytetään osamaksun maksupäivänä voimassaolevaa vaihtokurssia.</span><span class="sxs-lookup"><span data-stu-id="946bc-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




