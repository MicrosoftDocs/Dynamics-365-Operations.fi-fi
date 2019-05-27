---
title: Luottokorttitapahtumien tuonti ja ylläpito
description: Tässä ohjeaiheessa kerrotaan, miten kuluihin liittyviä luottokorttitapahtumia tuodaan ja ylläpidetään. Nämä tapahtumat voidaan määrittää niin, että ne tuodaan automaattisesti aikataulun mukaan, tai ne voidaan tuoda manuaalisesti tarvittaessa.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565110"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="3e6ae-104">Luottokorttitapahtumien tuonti ja ylläpito</span><span class="sxs-lookup"><span data-stu-id="3e6ae-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e6ae-105">Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää niin, että ne tuodaan automaattisesti aikataulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3e6ae-106">Tapahtumat voidaan myös tuoda manuaalisesti tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3e6ae-107">Luottokorttitapahtumat tuodaan Luottokorttitapahtumat-tietoyksikön välityksellä.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="3e6ae-108">Lisätietoja tietoyksiköistä on kohdassa [Tietoyksiköt](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="3e6ae-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3e6ae-109">Tuo luottokorttitapahtumat</span><span class="sxs-lookup"><span data-stu-id="3e6ae-109">Import credit card transactions</span></span>

1. <span data-ttu-id="3e6ae-110">Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3e6ae-111">Jos avaat tietojenhallinnan ensimmäisen kerran, järjestelmän on päivitettävä tietoyksiköiden luettelo ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3e6ae-112">Kirjoita tuontityölle yksilöivä nimi **Nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="3e6ae-113">Valitse **Lähdetietojen muoto** -kenttään sen tiedoston muoto, josta luottokorttitapahtumat tuodaan.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3e6ae-114">Valitse **Lataa** ja etsi tuotava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3e6ae-115">Kun tiedosto on ladattu, vahvista luottokorttitapahtumien tiedoston ja Luottokorttitapahtumat-tietoyksikön sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä määritys** -linkki.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3e6ae-116">Jos tuonnissa on määritysvirheitä tai määritystä on muutettava, voit tehdä yhdistämismuutokset joko **Yhdistämismääritysten visualisointi** tai **Yhdistämistiedot** -välilehdellä.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3e6ae-117">Luottokorttitapahtumien automatisointi tehdään valitsemalla **Luo toistuva tietotyö**.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3e6ae-118">Voit sitten määrittää toistovälin, jolla määritetään kuinka usein luottokorttitapahtumat tuodaan.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3e6ae-119">Kun olet valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3e6ae-120">Voit tuoda valitun tiedoston valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3e6ae-121">Jos tuonnin aikana tapahtuu virheitä, voit tarkastaa suorituslokista tai väliaikaisista tiedoista virheet, jotka on korjattava, jotta tuonti onnistuu.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3e6ae-122">Jos tuot useampaa tiedostomuotoa, luo kullekin tiedostomuodolle erilliset tuontityöt.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3e6ae-123">Poistettujen työntekijöiden luottokorttitapahtumien määrittäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="3e6ae-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3e6ae-124">Kun työntekijän tietue poistetaan, kyseisen työntekijän Active Directory -hakemistopalvelun (AD DS) tilin käyttö estetään.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3e6ae-125">Työntekijällä voi kuitenkin olla aktiivisia luottokorttitapahtumia, joiden kulut on kirjattava ja korvattava.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3e6ae-126">Voit käyttää **Luottokorttitapahtumat**-sivua ja määrittää työntekijälle minkä tahansa luottokorttitapahtuman, vaikka työntekijä on poistettu.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3e6ae-127">Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3e6ae-128">Valitse sitten toinen työntekijä, jolle luottokorttitapahtuma määritetään.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3e6ae-129">Kun olet siirtänyt luottokorttitapahtuman, ne voidaan valita kuluraporttiin ja maksaa kuluraportin hyväksynnän normaalimenettelyn kautta.</span><span class="sxs-lookup"><span data-stu-id="3e6ae-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
