---
title: Käyttöomaisuuserän luovutuskirjaustilit
description: Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d9c386b5da90918226e8b1a224bf628c65702b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988999"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="a37a2-103">Käyttöomaisuuserän luovutuskirjaustilit</span><span class="sxs-lookup"><span data-stu-id="a37a2-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a37a2-104">Tässä ohjeaiheessa kuvataan, kuinka määritetään kirjanpitotilejä käyttöomaisuuden luovuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="a37a2-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="a37a2-105">Määritä kirjanpitoon kirjaukset valitsemalla Käyttöomaisuuden kirjausprofiilit -sivulla Poistomyynti tai Poistohävikki.</span><span class="sxs-lookup"><span data-stu-id="a37a2-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="a37a2-106">Molempien tapahtumalajien kohdalla kirjanpitotiliä hyvitetään käyttöomaisuuserän luovutusarvolla.</span><span class="sxs-lookup"><span data-stu-id="a37a2-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="a37a2-107">Debet kirjataan vastatilille, joka voi olla esimerkiksi pankkitili.</span><span class="sxs-lookup"><span data-stu-id="a37a2-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="a37a2-108">Jos käyttöomaisuuserä myydään asiakkaalle, vastatilin asemesta käytetään asiakastiliä.</span><span class="sxs-lookup"><span data-stu-id="a37a2-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="a37a2-109">Valitse Luovutus, valitse Myynti tai Hävikki ja määritä sitten yksityiskohtaiset tilit käyttöomaisuuserän nettokirjanpitoarvon vähentämistä varten.</span><span class="sxs-lookup"><span data-stu-id="a37a2-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="a37a2-110">Voit syöttää tietoja myös Luovutusparametrit-sivun Kirjausarvo- ja Myyntiarvo-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="a37a2-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="a37a2-111">Arvoltaan vähäisen käyttöomaisuuden ryhmässä olevan käyttöomaisuuserän poistotapahtuma vähentää arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvoa vain poistetulla summalla.</span><span class="sxs-lookup"><span data-stu-id="a37a2-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="a37a2-112">Jos käyttöomaisuuserän myyntisumma on kuitenkin suurempi kuin arvoltaan vähäisen käyttöomaisuuden ryhmän nettokirjanpitoarvo, nettokirjanpitoarvo vähennetään nollaan.</span><span class="sxs-lookup"><span data-stu-id="a37a2-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





