---
title: Määritä yrityksen pankkitilit ISO20022-suoraveloituksia varten
description: Tässä tehtävässä kerrotaan, miten asiakkaan maksutiedostojen luomisessa vaadittavat yrityskohtaisen pankkitilin tiedot määritetään.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819453"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="931cd-103">Määritä yrityksen pankkitilit ISO20022-suoraveloituksia varten</span><span class="sxs-lookup"><span data-stu-id="931cd-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="931cd-104">Tässä tehtävässä kerrotaan, miten asiakkaan maksutiedostojen luomisessa vaadittavat yrityskohtaisen pankkitilin tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="931cd-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="931cd-105">Näissä ohjeissa käytetään esimerkkinä ISO 20022 -suoraveloitusmuotoa.</span><span class="sxs-lookup"><span data-stu-id="931cd-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="931cd-106">Muissa muodoissa voidaan vaatia lisämäärityksiä, kuten yrityksen tunnus tai lajittelukoodi.</span><span class="sxs-lookup"><span data-stu-id="931cd-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="931cd-107">Tämän tehtävän luomisessa käytettiin esittelytietojen DEMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="931cd-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="931cd-108">Tämä on toinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="931cd-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="931cd-109">IBAN- ja SWIFT-koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="931cd-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="931cd-110">Siirry kohtaan Maksuliikenteen hallinta > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="931cd-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="931cd-111">Pikasuodattimen avulla voit suodattaa Pankkitili-kentän DEMF OPER -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="931cd-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="931cd-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="931cd-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="931cd-113">Esimerkki: valitse DEMF OPER, kun haluat avata pankkitilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="931cd-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="931cd-114">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="931cd-114">Click Edit.</span></span>
5. <span data-ttu-id="931cd-115">Laajenna tai tiivistä Lisätunnus-osa.</span><span class="sxs-lookup"><span data-stu-id="931cd-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="931cd-116">Syötä arvon IBAN-kenttään.</span><span class="sxs-lookup"><span data-stu-id="931cd-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="931cd-117">Kirjoita esimerkiksi 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="931cd-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="931cd-118">Syötä arvo SWIFT-koodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="931cd-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="931cd-119">Esimerkki: kirjoita "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="931cd-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="931cd-120">Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="931cd-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="931cd-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="931cd-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="931cd-122">Yrityksen pankkitilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="931cd-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="931cd-123">Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.</span><span class="sxs-lookup"><span data-stu-id="931cd-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="931cd-124">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="931cd-124">Click Edit.</span></span>
3. <span data-ttu-id="931cd-125">Laajenna tai tiivistä Pankkitilin tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="931cd-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="931cd-126">Avaa haku valitsemalla Pankkitili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="931cd-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="931cd-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="931cd-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="931cd-128">Esimerkki: valitse pankkitili "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="931cd-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="931cd-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="931cd-129">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]