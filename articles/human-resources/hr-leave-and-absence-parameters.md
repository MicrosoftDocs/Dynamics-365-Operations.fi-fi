---
title: Loma- ja poissaoloparametrien määrittäminen
description: Määritä henkilöstöhallinnon parametrit lomaa ja poissaoloa varten Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712373"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="de40b-103">Loma- ja poissaoloparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="de40b-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="de40b-104">Ennen kuin määrität loma- ja poissaolosuunnitelmat Dynamics 365 Human Resources -ohjelmassa, kannattaa tarkistaa kaikkien liittyvien henkilöstöparametrien asetukset, kuten esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="de40b-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="de40b-105">Lomapyyntöjen numerosarja</span><span class="sxs-lookup"><span data-stu-id="de40b-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="de40b-106">Perhe- ja sairauspoissaolon säädös (FMLA) -asetukset</span><span class="sxs-lookup"><span data-stu-id="de40b-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="de40b-107">Työntekijän itsepalvelun asetukset loma- ja poissaolopyynnöille</span><span class="sxs-lookup"><span data-stu-id="de40b-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="de40b-108">Loman ja poissaolon parametrit</span><span class="sxs-lookup"><span data-stu-id="de40b-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="de40b-109">Tarkastele ja muuta henkilöstöparametreja</span><span class="sxs-lookup"><span data-stu-id="de40b-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="de40b-110">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="de40b-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="de40b-111">Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.</span><span class="sxs-lookup"><span data-stu-id="de40b-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="de40b-112">Tarkista **Numerosarjat**-välilehdessä **Numerosarjakoodi** **Lomapyynnön tunnusta** varten ja muuta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="de40b-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="de40b-113">Tämä asetus määrittää järjestyksen, jota käytetään automaattisesti, kun tunnuksia annetaan lomapyyntöjä varten.</span><span class="sxs-lookup"><span data-stu-id="de40b-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="de40b-114">Tarkista **FMLA**-välilehdessä FMLA-asetukset ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="de40b-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="de40b-115">Määritä **Työntekijän itsepalvelu** -välilehdessä, voivatko esimiehet kirjoittaa loma- ja poissaolopyyntöjä työntekijöidensä puolesta.</span><span class="sxs-lookup"><span data-stu-id="de40b-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="de40b-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="de40b-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="de40b-117">Loma- ja poissaoloparametrien tarkasteleminen ja muuttaminen</span><span class="sxs-lookup"><span data-stu-id="de40b-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="de40b-118">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="de40b-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="de40b-119">Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.</span><span class="sxs-lookup"><span data-stu-id="de40b-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="de40b-120">Määritä **Yleiset**-välilehdessä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="de40b-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="de40b-121">Määritä **Loma-ja poissaoloyksikkö** joko tunteina tai päivinä.</span><span class="sxs-lookup"><span data-stu-id="de40b-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="de40b-122">Jos valinta on päivät, voit valita **Ota käyttöön puolipäiväiset määritykset**, jolloin työntekijät voivat valita joko ensimmäisen tai toisen puolen päivästä lomapyynnöille.</span><span class="sxs-lookup"><span data-stu-id="de40b-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="de40b-123">Valitse **Palvelukuukausien voimaantulopäivä**, kun haluat määrittää, milloin jaksotusprosentit tulevat voimaan palvelukuukausien avulla.</span><span class="sxs-lookup"><span data-stu-id="de40b-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="de40b-124">Valitse **Saldon laskeminen**, kun haluat näyttää saldon kuluvan päivän ja jaksotuskauden mukaan.</span><span class="sxs-lookup"><span data-stu-id="de40b-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="de40b-125">Jos valitset **Saldo tänään** -vaihtoehdon, saldo näyttää kaikkien kertymien, oikaisujen ja pyyntöjen kokonaissumman tänään.</span><span class="sxs-lookup"><span data-stu-id="de40b-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="de40b-126">Jos valitset **Saldo jaksotuskaudelta**, saldo näyttää kaikkien jaksotusten, oikaisujen ja pyyntöjen kokonaissumman niiden jaksotuskauden mukaan, jotka on määritetty lomasuunnitelman frekvenssin mukaan.</span><span class="sxs-lookup"><span data-stu-id="de40b-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="de40b-127">Määritä siirtokirjauksen tekemisen vanhentumisen erätyön aloitusaika.</span><span class="sxs-lookup"><span data-stu-id="de40b-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="de40b-128">Valitse **Työntekijät voivat ostaa lomaa**- ja **Salli työntekijöiden myydä lomaa** -kohdissa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="de40b-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="de40b-129">Jos valitse näissä vaihtoehdoissa **Kyllä**, voit luoda käytännöt loman vaihtamisesta rahaksi ja lomapalkan vaihtamisesta vapaaksi ja antaa työntekijöille mahdollisuuden lähettää loman rahaksi tai lomapalkan vapaaksi vaihtamispyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="de40b-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="de40b-130">Määritä kalenteriparametrit</span><span class="sxs-lookup"><span data-stu-id="de40b-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="de40b-131">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="de40b-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="de40b-132">Valitse **Asetukset**-kohdasta **Loma- ja poissaoloparametrit**.</span><span class="sxs-lookup"><span data-stu-id="de40b-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="de40b-133">Muuta **Kalenteri**-välilehdessä asetukset tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="de40b-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="de40b-134">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="de40b-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="de40b-135">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="de40b-135">See also</span></span>

- [<span data-ttu-id="de40b-136">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="de40b-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
