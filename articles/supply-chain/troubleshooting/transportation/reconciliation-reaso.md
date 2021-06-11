---
title: Täsmäytysssyistä voit lisätä vain päätilin kredit-tiliksi
description: Kun määrität täsmäytyksen syyn kuljetuksen hallinnassa, voit lisätä vain päätilin kredit-tiliksi.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026459"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="d62f6-103">Täsmäytysssyistä voit lisätä vain päätilin kredit-tiliksi</span><span class="sxs-lookup"><span data-stu-id="d62f6-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="d62f6-104">Tietopankin numero: 4603538</span><span class="sxs-lookup"><span data-stu-id="d62f6-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="d62f6-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="d62f6-105">Symptoms</span></span>

<span data-ttu-id="d62f6-106">Kun määrität täsmäytyksen syyn kuljetuksen hallinnassa, voit lisätä vain päätilin kredit-tiliksi.</span><span class="sxs-lookup"><span data-stu-id="d62f6-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="d62f6-107">Kustannuspaikkaa tai muuta dimensiota ei voi lisätä kredit-tiliksi.</span><span class="sxs-lookup"><span data-stu-id="d62f6-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="d62f6-108">Debet-tilin avulla voit kuitenkin valita muita dimensioita.</span><span class="sxs-lookup"><span data-stu-id="d62f6-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="d62f6-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d62f6-109">Resolution</span></span>

<span data-ttu-id="d62f6-110">Jos täsmäytystä ei ole tehty toimittajalle maksamiseksi vaan tietyn päätilin hyvittämiseksi, järjestelmä ei salli taloushallinnon dimension valitsemista kredit-tilille täsmäytyksen syytä määrittäessäsi.</span><span class="sxs-lookup"><span data-stu-id="d62f6-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="d62f6-111">Jos tilirakenne edellyttää tiettyä taloushallinnon dimension arvoa kredit-päätilille, tuloksena syntyvää toimittajakirjauskansiota ei voi kirjata automaattisesti, koska taloushallinnon dimension arvo puuttuu.</span><span class="sxs-lookup"><span data-stu-id="d62f6-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="d62f6-112">Siksi hyvitystili on määritettävä manuaalisesti **Laskukirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d62f6-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="d62f6-113">Koska kredit-tilille tarvitaan dimensioarvo, toimittajan laskukirjauskansiota ei voi kirjata automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d62f6-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="d62f6-114">Se on kirjattava manuaalisesti sen jälkeen, kun dimensioarvo on lisätty hyvitysrivin päätilille manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="d62f6-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>