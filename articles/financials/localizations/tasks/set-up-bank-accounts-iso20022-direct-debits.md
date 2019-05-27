---
title: Määritä asiakas ja asiakkaan pankkitilit ISO20022-suoraveloituksia varten
description: Tässä tehtävässä kerrotaan, miten ISO20022-suoraveloituksen maksutiedostossa vaadittavat asiakkaan pankkitili ja asiakkaan suoraveloitusvaltakirja määritetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7d7d79b1d496223b027d800beca105ecaa0bd4c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552445"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="ce44c-103">Määritä asiakas ja asiakkaan pankkitilit ISO20022-suoraveloituksia varten</span><span class="sxs-lookup"><span data-stu-id="ce44c-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce44c-104">Tässä tehtävässä kerrotaan, miten ISO20022-suoraveloituksen maksutiedostossa vaadittavat asiakkaan pankkitili ja asiakkaan suoraveloitusvaltakirja määritetään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="ce44c-105">Määritetyistä asiakkaan maksumuodoista riippuu, tarvitaanko asiakkaalle tai asiakkaan pankkitilille tähän ohjeeseen kuulumattomia lisätietoja ja mitä ko. lisätiedot ovat.</span><span class="sxs-lookup"><span data-stu-id="ce44c-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="ce44c-106">Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="ce44c-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="ce44c-107">Tämä on neljäs viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="ce44c-108">Asiakkaan pankkitilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce44c-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="ce44c-109">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="ce44c-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="ce44c-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="ce44c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ce44c-111">Voit esimerkiksi suodattaa Tili-kenttää arvolla DE-010.</span><span class="sxs-lookup"><span data-stu-id="ce44c-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="ce44c-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ce44c-113">Valitse toimintoruudussa Asiakas.</span><span class="sxs-lookup"><span data-stu-id="ce44c-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="ce44c-114">Valitse Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="ce44c-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="ce44c-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce44c-115">Click New.</span></span>
7. <span data-ttu-id="ce44c-116">Kirjoita arvo Pankkitili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="ce44c-117">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ce44c-118">Kirjoita esimerkiksi 'EUR bank'.</span><span class="sxs-lookup"><span data-stu-id="ce44c-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="ce44c-119">Syötä tai valitse arvo Pankkiryhmät-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="ce44c-120">Syötä arvon IBAN-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="ce44c-121">Kirjoita esimerkiksi 'DE36200400000628808808'.</span><span class="sxs-lookup"><span data-stu-id="ce44c-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="ce44c-122">Syötä arvo SWIFT-koodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="ce44c-123">Esimerkki: Syötä COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="ce44c-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="ce44c-124">Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="ce44c-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="ce44c-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ce44c-125">Click Save.</span></span>
13. <span data-ttu-id="ce44c-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce44c-126">Close the page.</span></span>
14. <span data-ttu-id="ce44c-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="ce44c-127">Click Edit.</span></span>
15. <span data-ttu-id="ce44c-128">Laajenna Oletusmaksut-osa.</span><span class="sxs-lookup"><span data-stu-id="ce44c-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="ce44c-129">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="ce44c-130">Suoraveloitusvaltakirjan lisääminen</span><span class="sxs-lookup"><span data-stu-id="ce44c-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="ce44c-131">Laajenna Suoraveloitusvaltakirjat-osa.</span><span class="sxs-lookup"><span data-stu-id="ce44c-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="ce44c-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="ce44c-132">Click Add.</span></span>
3. <span data-ttu-id="ce44c-133">Syötä tai valitse arvo Laskuttajan pankkitili -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="ce44c-134">Voit valita esimerkiksi arvon DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="ce44c-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="ce44c-135">Syötä päivämäärä Allekirjoitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="ce44c-136">Vahvista päivämäärän päivitys valitsemalla Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ce44c-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="ce44c-137">Syötä tai valitse arvo Allekirjoitussijainti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="ce44c-138">Syötä numero Odotettu maksujen määrä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce44c-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="ce44c-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ce44c-139">Click OK.</span></span>
9. <span data-ttu-id="ce44c-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ce44c-140">Click Save.</span></span>

