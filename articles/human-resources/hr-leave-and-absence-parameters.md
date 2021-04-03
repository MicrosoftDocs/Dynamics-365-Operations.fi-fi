---
title: Loma- ja poissaoloparametrien määrittäminen
description: Määritä henkilöstöhallinnon parametrit lomaa ja poissaoloa varten Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db96073f0a16f1c710fbfebb2d08a1d693eab1e1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463379"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="f1a02-103">Loma- ja poissaoloparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f1a02-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f1a02-104">Ennen kuin määrität loma- ja poissaolosuunnitelmat Dynamics 365 Human Resources -ohjelmassa, kannattaa tarkistaa kaikkien liittyvien henkilöstöparametrien asetukset, kuten esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="f1a02-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="f1a02-105">Lomapyyntöjen numerosarja</span><span class="sxs-lookup"><span data-stu-id="f1a02-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="f1a02-106">Perhe- ja sairauspoissaolon säädös (FMLA) -asetukset</span><span class="sxs-lookup"><span data-stu-id="f1a02-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="f1a02-107">Työntekijän itsepalvelun asetukset loma- ja poissaolopyynnöille</span><span class="sxs-lookup"><span data-stu-id="f1a02-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="f1a02-108">Loman ja poissaolon parametrit</span><span class="sxs-lookup"><span data-stu-id="f1a02-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="f1a02-109">Tarkastele ja muuta henkilöstöparametreja</span><span class="sxs-lookup"><span data-stu-id="f1a02-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="f1a02-110">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f1a02-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f1a02-111">Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="f1a02-112">Tarkista **Numerosarjat**-välilehdessä **Numerosarjakoodi** **Lomapyynnön tunnusta** varten ja muuta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f1a02-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="f1a02-113">Tämä asetus määrittää järjestyksen, jota käytetään automaattisesti, kun tunnuksia annetaan lomapyyntöjä varten.</span><span class="sxs-lookup"><span data-stu-id="f1a02-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="f1a02-114">Tarkista **FMLA**-välilehdessä FMLA-asetukset ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f1a02-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="f1a02-115">Määritä **Työntekijän itsepalvelu** -välilehdessä, voivatko esimiehet kirjoittaa loma- ja poissaolopyyntöjä työntekijöidensä puolesta.</span><span class="sxs-lookup"><span data-stu-id="f1a02-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="f1a02-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="f1a02-117">Loman ja poissaolon tarkasteleminen yrityksissä tapahtuu nyt esikatselussa.</span><span class="sxs-lookup"><span data-stu-id="f1a02-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="f1a02-118">Se on otettava käyttöön **eristysympäristössä**, jotta loma- ja poissaolovaihtoehto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f1a02-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="f1a02-119">Lisätietoja esiversio-ominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="f1a02-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="f1a02-120">Human Resourcesin jaettujen parametrien tarkastelemien ja muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f1a02-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="f1a02-121">Valitse **Henkilöstön hallinta** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f1a02-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f1a02-122">Valitse **Määritys**-kohdasta **Human resourcesin jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="f1a02-123">Valitse **Laajennetut käyttöoikeudet** -välilehdessä **Kyllä** **Ota käyttöön yritystenvälinen lomanäkymä** -kohdassa, jos haluat loman olevan tarkasteltavissa eri yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="f1a02-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="f1a02-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="f1a02-125">Loma- ja poissaoloparametrien tarkasteleminen ja muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f1a02-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="f1a02-126">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f1a02-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f1a02-127">Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="f1a02-128">Määritä **Yleiset**-välilehdessä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="f1a02-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="f1a02-129">Määritä **Loma-ja poissaoloyksikkö** joko tunteina tai päivinä.</span><span class="sxs-lookup"><span data-stu-id="f1a02-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="f1a02-130">Jos valinta on päivät, voit valita **Ota käyttöön puolipäiväiset määritykset**, jolloin työntekijät voivat valita joko ensimmäisen tai toisen puolen päivästä lomapyynnöille.</span><span class="sxs-lookup"><span data-stu-id="f1a02-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="f1a02-131">Valitse **Palvelukuukausien voimaantulopäivä**, kun haluat määrittää, milloin jaksotusprosentit tulevat voimaan palvelukuukausien avulla.</span><span class="sxs-lookup"><span data-stu-id="f1a02-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="f1a02-132">Valitse **Saldon laskeminen**, kun haluat näyttää saldon kuluvan päivän ja jaksotuskauden mukaan.</span><span class="sxs-lookup"><span data-stu-id="f1a02-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="f1a02-133">Jos valitset **Saldo tänään** -vaihtoehdon, saldo näyttää kaikkien kertymien, oikaisujen ja pyyntöjen kokonaissumman tänään.</span><span class="sxs-lookup"><span data-stu-id="f1a02-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="f1a02-134">Jos valitset **Saldo jaksotuskaudelta**, saldo näyttää kaikkien jaksotusten, oikaisujen ja pyyntöjen kokonaissumman niiden jaksotuskauden mukaan, jotka on määritetty lomasuunnitelman frekvenssin mukaan.</span><span class="sxs-lookup"><span data-stu-id="f1a02-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="f1a02-135">Määritä siirtokirjauksen tekemisen vanhentumisen erätyön aloitusaika.</span><span class="sxs-lookup"><span data-stu-id="f1a02-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="f1a02-136">Valitse **Työntekijät voivat ostaa lomaa**- ja **Salli työntekijöiden myydä lomaa** -kohdissa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="f1a02-137">Jos valitse näissä vaihtoehdoissa **Kyllä**, voit luoda käytännöt loman vaihtamisesta rahaksi ja lomapalkan vaihtamisesta vapaaksi ja antaa työntekijöille mahdollisuuden lähettää loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="f1a02-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="f1a02-138">Määritä kalenteriparametrit</span><span class="sxs-lookup"><span data-stu-id="f1a02-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="f1a02-139">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f1a02-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f1a02-140">Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="f1a02-141">Muuta **Kalenteri**-välilehdessä asetukset tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f1a02-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="f1a02-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f1a02-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1a02-143">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f1a02-143">See also</span></span>

- [<span data-ttu-id="f1a02-144">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="f1a02-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]