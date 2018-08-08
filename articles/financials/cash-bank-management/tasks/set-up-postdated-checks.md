--- 
title: "Määritä jälkeen päin päivitetyt sekit"
description: "Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5b1988ee50dae686ae860305cd785deacae94a72
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="6e45c-103">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="6e45c-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e45c-104">Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen.</span><span class="sxs-lookup"><span data-stu-id="6e45c-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="6e45c-105">Voit myös määrittää selvitystilit lähetetyille ja vastaanotetuille sekeille sekä ennakonpidätykselle.</span><span class="sxs-lookup"><span data-stu-id="6e45c-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="6e45c-106">Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten.</span><span class="sxs-lookup"><span data-stu-id="6e45c-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="6e45c-107">Voit määrittää, onko sekin näyttävä kirjanpidossa ennen sen erääntymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="6e45c-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="6e45c-108">Tämä menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="6e45c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="6e45c-109">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="6e45c-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="6e45c-110">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="6e45c-110">Set up postdated checks</span></span>
1. <span data-ttu-id="6e45c-111">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="6e45c-112">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="6e45c-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="6e45c-113">Valitse Ota käyttöön myöhemmäksi päivätyt sekit -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="6e45c-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="6e45c-114">Valitse Myöhemmäksi päivättyjen sekkien kirjauskansiokirjaukset -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="6e45c-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="6e45c-115">Määritä Asetettujen sekkien siirtotili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="6e45c-116">Määritä Vastaanotettujen sekkien siirtotili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="6e45c-117">Kirjoita Siirtokirjausten kirjauskansio -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6e45c-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="6e45c-118">Kirjota Siirrä myöhemmäksi päivättyjä sekkejä tämän toimittajan maksukirjauskansioon -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6e45c-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="6e45c-119">Määritä Ennakonpidätyksen selvitystili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="6e45c-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6e45c-120">Click Save.</span></span>
11. <span data-ttu-id="6e45c-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6e45c-121">Close the page.</span></span>
12. <span data-ttu-id="6e45c-122">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="6e45c-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="6e45c-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6e45c-123">Click New.</span></span>
14. <span data-ttu-id="6e45c-124">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6e45c-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="6e45c-125">Myöhemmäksi päivättyjen sekkien siirtokirjaus -vaihtoehdon valinta osoittaa, , että sekin summa kirjataan selvitystilille.</span><span class="sxs-lookup"><span data-stu-id="6e45c-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="6e45c-126">Valitse Tilityyppi-kentässä Pankki.</span><span class="sxs-lookup"><span data-stu-id="6e45c-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="6e45c-127">Maksutavan vastatili on pankki.</span><span class="sxs-lookup"><span data-stu-id="6e45c-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="6e45c-128">Määritä Maksutili-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="6e45c-129">Valitse laskun summan vähennyksessä käytettävä pankkitili.</span><span class="sxs-lookup"><span data-stu-id="6e45c-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="6e45c-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6e45c-130">Close the page.</span></span>
19. <span data-ttu-id="6e45c-131">Valitse Myyntireskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="6e45c-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="6e45c-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6e45c-132">Click New.</span></span>
21. <span data-ttu-id="6e45c-133">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6e45c-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="6e45c-134">Myöhemmäksi päivättyjen sekkien siirtokirjaus -vaihtoehdon valinta osoittaa, , että sekin summa kirjataan selvitystilille.</span><span class="sxs-lookup"><span data-stu-id="6e45c-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="6e45c-135">Valitse Tilityyppi-kentässä Pankki.</span><span class="sxs-lookup"><span data-stu-id="6e45c-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="6e45c-136">Maksutavan vastatili on pankki.</span><span class="sxs-lookup"><span data-stu-id="6e45c-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="6e45c-137">Määritä Maksutili-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="6e45c-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="6e45c-138">Valitse laskun summan vähennyksessä käytettävä pankkitili.</span><span class="sxs-lookup"><span data-stu-id="6e45c-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="6e45c-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6e45c-139">Close the page.</span></span>


