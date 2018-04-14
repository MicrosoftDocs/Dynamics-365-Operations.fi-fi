---
title: "Käyttöomaisuuden hankintojen kirjaustilit"
description: "Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden hankkimista varten."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1e30d9f8ee4c7d6aea2da33975cd7f353cdc62eb
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="35444-103">Käyttöomaisuuden hankintojen kirjaustilit</span><span class="sxs-lookup"><span data-stu-id="35444-103">Fixed asset acquisition posting accounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="35444-104">Tässä artikkelissa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden hankkimista varten.</span><span class="sxs-lookup"><span data-stu-id="35444-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="35444-105">Käyttöomaisuuden hankintojen kirjaamiseen käytetyt tilit voivat vaihdella sen mukaan, millä tavalla käyttöomaisuus hankitaan.</span><span class="sxs-lookup"><span data-stu-id="35444-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="35444-106">Valitsemalla Käyttöomaisuuserän kirjausprofiili -sivun Kirjanpitotilit -välilehdessä Hankinta ja Hankintaoikaisu voit määrittää käyttöomaisuustilit kirjanpitoon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="35444-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="35444-107">Kirjanpitotili on kirjauskansioissa ja ostotilauksissa yleensä tasetili, jota hyvitetään uuden käyttöomaisuuserän hankinta-arvolla.</span><span class="sxs-lookup"><span data-stu-id="35444-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="35444-108">Tätä tiliä ei näytetä kirjauskansiossa, eikä sitä voi korvata tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="35444-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="35444-109">Myös vastatili on tasetili.</span><span class="sxs-lookup"><span data-stu-id="35444-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="35444-110">Kirjauskansiossa ja käyttöomaisuuskirjauskansiossa tämä tili on usein pankkitili, jota käytetään käyttöomaisuuserän hankintahinnan maksamiseen.</span><span class="sxs-lookup"><span data-stu-id="35444-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="35444-111">Vastatili on kirjauskansioissa ehdotettava oletustili.</span><span class="sxs-lookup"><span data-stu-id="35444-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="35444-112">Se voidaan vaihtaa kirjauskansiossa toiseksi tilikartan tiliksi tai toimittajatiliksi, jos käyttöomaisuuserä oli osto toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="35444-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="35444-113">Käytettäessä ostoreskontran Laskukirjauskansio- tai Ostotilaukset-toimintoa käyttöomaisuuden hankintaan, käyttöomaisuustapahtuman vastatili korvataan tapahtumalle valitulla toimittajatilillä.</span><span class="sxs-lookup"><span data-stu-id="35444-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="35444-114">Kirjanpito-osan Siirto varastosta käyttöomaisuuteen -kirjauskansion avulla kirjattavien hankintojen osalta käyttöomaisuuserää ei osteta ulkoisesta lähteestä, vaan se siirretään yrityksen omasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="35444-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="35444-115">Tämän vuoksi vastatili on varasto-ottotili varastonimikkeelle varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="35444-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="35444-116">Lisätietoja on ohjeaiheessa [Hankkia omaisuuseriä hankintojen kautta](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="35444-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>




