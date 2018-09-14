--- 
title: "Arvonlisäveroviranomaisten määrittäminen"
description: "Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 909433a04c1185039938f6233b30c235e7b8ed8b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="df88f-103">Arvonlisäveroviranomaisten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="df88f-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df88f-104">Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan.</span><span class="sxs-lookup"><span data-stu-id="df88f-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="df88f-105">Yritys voi maksaa arvonlisäverot suoraan viranomaiselle tai arvonlisäveroviranomaiselle luodun toimittajatilin kautta.</span><span class="sxs-lookup"><span data-stu-id="df88f-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="df88f-106">Jos valitset tämän vaihtoehdon, yritys voi maksaa arvonlisäveroviranomaiselle ajoissa tavanomaista maksurutiinia käyttäen.</span><span class="sxs-lookup"><span data-stu-id="df88f-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="df88f-107">Jos veroviranomaista ei määritetä toimittajaksi, jonkun on laadittava maksut veroviranomaiselle manuaalisesti asianmukaisena eräpäivänä.</span><span class="sxs-lookup"><span data-stu-id="df88f-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="df88f-108">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="df88f-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="df88f-109">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroviranomaiset.</span><span class="sxs-lookup"><span data-stu-id="df88f-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="df88f-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="df88f-110">Click New.</span></span>
3. <span data-ttu-id="df88f-111">Kirjoita arvo Viranomainen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="df88f-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="df88f-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="df88f-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="df88f-113">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="df88f-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="df88f-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="df88f-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="df88f-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="df88f-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="df88f-116">Valitse maasi/alueesi raportin asettelu, jos sellainen on valittavissa.</span><span class="sxs-lookup"><span data-stu-id="df88f-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="df88f-117">Jos raportin asettelut eivät vastaa arvonlisäveroviranomaisen vaatimuksia, käytä oletusasettelua.</span><span class="sxs-lookup"><span data-stu-id="df88f-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="df88f-118">Määritä, miten veron maksettava kokonaissumma on pyöristettävä, syöttämällä arvo Pyöristystapa- ja Pyöristys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="df88f-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="df88f-119">Pyöristyserot kirjataan tileille kirjanpidolle määritettyjä automaattisia tapahtumia varten.</span><span class="sxs-lookup"><span data-stu-id="df88f-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="df88f-120">Syötä Pyöristys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="df88f-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="df88f-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="df88f-121">Click Save.</span></span>


