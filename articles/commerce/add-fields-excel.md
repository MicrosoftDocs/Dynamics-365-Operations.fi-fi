---
title: Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten
description: Tässä aiheessa kerrotaan, miten kentät lisätään Microsoft Excel -työkirjaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ea5483ff1eea8922ffeb9e65768a0e5eab28890
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797692"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="eb1d0-103">Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="eb1d0-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb1d0-104">Tässä aiheessa kerrotaan, miten kentät lisätään Microsoft Excel -työkirjaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eb1d0-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="eb1d0-105">Overview</span></span>

<span data-ttu-id="eb1d0-106">Kun Excel-tiedosto luodaan niin, että vähittäismyyntitapahtumia voi muokata, jotkin oletuskentät täytetään tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="eb1d0-107">Jos päivitettävä kenttä ei näy oletusarvoisesti Excel-tiedostossa, voit lisätä sen.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="eb1d0-108">Kenttien lisääminen Excel-työkirjan laskentataulukkoon</span><span class="sxs-lookup"><span data-stu-id="eb1d0-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="eb1d0-109">Alla olevien ohjeiden avulla voit lisätä kenttiä Excel-työkirjaan niin, että vähittäismyyntitapahtumia on mahdollista muokata.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="eb1d0-110">Lataa ja avaa Excel-tiedosto **Laskelmat**-sivulla, **Vähittäismyyntitapahtumat**-sivulla tai **Tapahtuman tarkistusvirheet** -ruudussa **Myymälän taloustiedot** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="eb1d0-111">Valitse **Rakenne**.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-111">Select **Design**.</span></span>
1. <span data-ttu-id="eb1d0-112">Valitse halutun taulukon kynäsymboli ja etsi ja valitse sitten käytettävissä olevien kenttien luettelosta lisättävä kenttä.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="eb1d0-113">Valitse **Lisää** ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="eb1d0-114">Voit muuttaa kenttien järjestystä.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-114">You can reorder fields.</span></span>
1. <span data-ttu-id="eb1d0-115">Kun päivitys on tehty, nouda tiedot uuteen sarakkeeseen valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="eb1d0-116">Uusi kenttä ja sen tiedot ovat nyt muokattavissa Excelissä.</span><span class="sxs-lookup"><span data-stu-id="eb1d0-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb1d0-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="eb1d0-117">Additional resources</span></span>

[<span data-ttu-id="eb1d0-118">Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="eb1d0-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="eb1d0-119">Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="eb1d0-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="eb1d0-120">Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="eb1d0-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="eb1d0-121">Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="eb1d0-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]