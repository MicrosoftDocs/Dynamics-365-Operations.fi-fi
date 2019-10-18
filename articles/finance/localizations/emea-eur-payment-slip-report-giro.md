---
title: Maksuluetteloraportti Euroopassa
description: Tässä aiheessa on tietoja maksuluetteloraporteista Euroopassa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cbbfa25252074cd371b271be2f0f03ad2a687944
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175745"
---
# <a name="payment-slip-report-for-europe"></a><span data-ttu-id="4a3e0-103">Maksuluetteloraportti Euroopassa</span><span class="sxs-lookup"><span data-stu-id="4a3e0-103">Payment slip report for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a3e0-104">Tässä aiheessa on tietoja maksuluetteloraporteista Euroopassa.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-104">This topic provides information about payment slip reports for Europe.</span></span>

<span data-ttu-id="4a3e0-105">Maksuluetteloraporttien toiminnot on käytettävissä yrityksille, joilla on ensisijainen osoite Tanskassa, Belgiassa, Norjassa, Sveitsissä tai Suomessa.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-105">The functionality for payment slip reports is available for legal entities that have their primary address in Denmark, Belgium, Norway, Switzerland, or Finland.</span></span> <span data-ttu-id="4a3e0-106">Yritykset usein liittävät usein asiakkaiden laskuihin tulostetun maksutositteen, jossa on maksuviite kirjaamista ja tilitystä varten.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-106">Businesses often attach printed payment slips to invoices to provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="4a3e0-107">Maksutositetta voidaan käyttää myynti- ja vapaatekstilaskujen lisäksi projekti- tai palvelulaskuissa, maksukehotteissa, korkolaskussa ja tiliotteissa.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-107">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span>

## <a name="set-up-a-creditor-id-number-denmark-only"></a><span data-ttu-id="4a3e0-108">Määritä laskuttajan tunnusnumero (vain Tanska)</span><span class="sxs-lookup"><span data-stu-id="4a3e0-108">Set up a creditor ID number (Denmark only)</span></span>
<span data-ttu-id="4a3e0-109">Anna yrityksesi luotonantajan tunnus (ID) -numero seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-109">Follow these steps to enter your company's creditor identification (ID) number.</span></span> <span data-ttu-id="4a3e0-110">Saat tämän numeron rahoituslaitokseltasi.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-110">Your financial institution provides this number.</span></span> <span data-ttu-id="4a3e0-111">Sitä käytetään viitteenä, kun asiakkaan maksut vastaanotetaan rahoituslaitosten kautta.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-111">It's used as a reference when customer payments are received through financial institutions.</span></span>

1.  <span data-ttu-id="4a3e0-112">Siirry kohtaan **Organisaation hallinto** &gt; **Asetukset** &gt; **Organisaatio** &gt; **Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-112">Click **Organization administration** &gt; **Setup** &gt; **Organization** &gt; **Legal entities**.</span></span>
2.  <span data-ttu-id="4a3e0-113">Anna **Pankkitilitiedot**-pikavälilehden **FI-luotonantajan tunnus** -kentässä 8-numeroinen yksilöllinen velkojan ID-tunnus.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-113">On the **Bank account information** FastTab, in the **FI-Creditor ID** field, enter your unique eight-digit creditor ID number.</span></span>
3.  <span data-ttu-id="4a3e0-114">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-114">Close the form to save your changes.</span></span>

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a><span data-ttu-id="4a3e0-115">Määritä maksutositteen muoto laskuille, korkolaskuille, maksukehotuksille ja tiliotteille</span><span class="sxs-lookup"><span data-stu-id="4a3e0-115">Set up a payment slip attachment format for invoices, interest notes, collection letters, and account statements</span></span>
<span data-ttu-id="4a3e0-116">Määritä myyntilaskujen, vapaatekstilaskujen, korkolaskujen, maksukehotusten ja tiliotteiden liitteenä lähetettävän maksutositteen muoto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-116">Follow these steps to set up a format for payment slip attachments that accompany sales invoices, free text invoices, interest notes, collection letters, and account statements.</span></span>

1.  <span data-ttu-id="4a3e0-117">Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Lomakkeet** &gt; **Lomakeasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-117">Click **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="4a3e0-118">Valitse **Lasku**-välilehden **Asiakkaan laskun liittyvä maksun liite** -kentässä maksutositteen liitetiedoston muoto.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-118">On the **Invoice** tab, in the **Associated payment attachment on customer invoice** field, select the payment slip attachment format.</span></span>
3.  <span data-ttu-id="4a3e0-119">Valitse **Vapaatekstilasku**-, **Korkolasku**-, **Maksukehotus**- ja **Tiliote**-välilehdissä, maksutositteen liitetiedoston muoto kullekin asiakirjatyypille.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-119">On the **Free text invoice**, **Interest note**, **Collection letter**, and **Account statement** tabs, select a payment slip attachment format for each document type.</span></span>
4.  <span data-ttu-id="4a3e0-120">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-120">Close the form to save your changes.</span></span>

<span data-ttu-id="4a3e0-121">Määritä maksutositeliitteiden muoto, joka liitetään projektilaskuihin, seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-121">Follow these steps to set up a format for payment slip attachments that accompany project invoices.</span></span>

1.  <span data-ttu-id="4a3e0-122">Valitse **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Lomakkeet** &gt; **Lomakeasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-122">Click **Project management and accounting** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="4a3e0-123">Valitse **Liittyvän maksun liite** -kentässä maksutositeliitteen muoto.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-123">In the **Associated payment attachment** field, select the payment slip attachment format.</span></span>

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a><span data-ttu-id="4a3e0-124">Maksukuittiliitteen muodon määrittäminen asiakastilille</span><span class="sxs-lookup"><span data-stu-id="4a3e0-124">Assign a payment slip attachment format to a customer account</span></span>
<span data-ttu-id="4a3e0-125">Kun olet määrittänyt maksutositeliitteen muodon myyntilaskuille, vapaatekstilaskuille, korkolaskuille, maksukehotuksille, tiliotteille ja projektilaskuille, voit määrittää valitun asiakkaan muotoilut.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-125">After you set up the payment slip attachment format for sales invoices, free text invoices, interest notes, collection letters, account statements, and project invoices, you can assign specific formats for a selected customer.</span></span>

1.  <span data-ttu-id="4a3e0-126">Valitse **Myyntireskontra** &gt; **Yleinen** &gt; **Asiakkaat** &gt; **Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-126">Click **Accounts receivable** &gt; **Common** &gt; **Customers** &gt; **All customers**.</span></span>
2.  <span data-ttu-id="4a3e0-127">Luo uusi asiakas tai valitse aiemmin määritetty asiakas.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-127">Create a new customer, or select an existing customer.</span></span>
3.  <span data-ttu-id="4a3e0-128">Valitse **Lasku ja toimitus** -pikavälilehden **Myyntilaskussa**-, **Vapaatekstilaskussa**-, **Korkolaskussa**-, **Maksukehotuksessa**-, **Projektilaskussa**- ja **Tiliotteessa**-kentissä muoto maksutositeliitteille, jotka liitetään valitulle asiakkaalle lähetettäviin eri tyyppisiin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-128">On the **Invoice and delivery** FastTab, in the **On a customer invoice**, **On a free text invoice**, **On an interest note**, **On a collection letter**, **On a project invoice**, and **On an account statement** fields, select the format for payment slip attachments that will accompany documents of each type that are sent to the selected customer.</span></span>
4.  <span data-ttu-id="4a3e0-129">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="4a3e0-129">Close the form to save your changes.</span></span>




