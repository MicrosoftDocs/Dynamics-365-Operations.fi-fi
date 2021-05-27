---
title: Määritä jälkeen päin päivitetyt sekit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026202"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="b2765-103">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="b2765-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2765-104">Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b2765-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="b2765-105">Voit myös määrittää selvitystilit lähetetyille ja vastaanotetuille sekeille sekä ennakonpidätykselle.</span><span class="sxs-lookup"><span data-stu-id="b2765-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="b2765-106">Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten.</span><span class="sxs-lookup"><span data-stu-id="b2765-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="b2765-107">Voit määrittää, onko sekin näyttävä kirjanpidossa ennen sen erääntymispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="b2765-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="b2765-108">Tämä menettelyn rooli on Rahastonhoitaja.</span><span class="sxs-lookup"><span data-stu-id="b2765-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="b2765-109">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="b2765-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="b2765-110">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="b2765-110">Set up postdated checks</span></span>
1. <span data-ttu-id="b2765-111">Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.</span><span class="sxs-lookup"><span data-stu-id="b2765-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="b2765-112">Valitse Myöhemmäksi päivätyt sekit -välilehti.</span><span class="sxs-lookup"><span data-stu-id="b2765-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="b2765-113">Valitse Ota käyttöön myöhemmäksi päivätyt sekit -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="b2765-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="b2765-114">Valitse Myöhemmäksi päivättyjen sekkien kirjauskansiokirjaukset -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="b2765-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="b2765-115">Määritä Asetettujen sekkien siirtotili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="b2765-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="b2765-116">Määritä Vastaanotettujen sekkien siirtotili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="b2765-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="b2765-117">Kirjoita Siirtokirjausten kirjauskansio -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b2765-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="b2765-118">Kirjota Siirrä myöhemmäksi päivättyjä sekkejä tämän toimittajan maksukirjauskansioon -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b2765-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="b2765-119">Määritä Ennakonpidätyksen selvitystili -kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="b2765-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="b2765-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b2765-120">Click Save.</span></span>
11. <span data-ttu-id="b2765-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b2765-121">Close the page.</span></span>
12. <span data-ttu-id="b2765-122">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="b2765-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="b2765-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b2765-123">Click New.</span></span>
14. <span data-ttu-id="b2765-124">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b2765-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="b2765-125">Myöhemmäksi päivättyjen sekkien siirtokirjaus -vaihtoehdon valinta osoittaa, , että sekin summa kirjataan selvitystilille.</span><span class="sxs-lookup"><span data-stu-id="b2765-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="b2765-126">Valitse Tilityyppi-kentässä Pankki.</span><span class="sxs-lookup"><span data-stu-id="b2765-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="b2765-127">Maksutavan vastatili on pankki.</span><span class="sxs-lookup"><span data-stu-id="b2765-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="b2765-128">Määritä Maksutili-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="b2765-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="b2765-129">Valitse laskun summan vähennyksessä käytettävä pankkitili.</span><span class="sxs-lookup"><span data-stu-id="b2765-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="b2765-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b2765-130">Click Save.</span></span>
19. <span data-ttu-id="b2765-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b2765-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="b2765-132">Ennen kuin voit kirjata myöhemmäksi päivätyn sekin pankkitilille, kun istunnon päivämäärä on suurempi tai yhtä suuri kuin erääntymispäivä, ota käyttöön ominaisuus **Maksukirjauskansion erääntymispäivän vahvistus myöhemmäksi päivätyillä sekeillä pankkitilille**.</span><span class="sxs-lookup"><span data-stu-id="b2765-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="b2765-133">Tämän ominaisuuden avulla voit kirjata toimittajien tai asiakkaiden maksukirjauskansioita, joilla on myöhemmäksi päivättyjä sekkejä, kun istunnon päivämäärä on suurempi tai yhtä suuri kuin erääntymispäivä.</span><span class="sxs-lookup"><span data-stu-id="b2765-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="b2765-134">Kun määrität kohtaa **Maksutapa** (**Ostoreskontra > Maksun asetukset > Maksutavat**), älä täytä **Välitili**-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="b2765-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="b2765-135">Tällöin vastatiliksi määritetään pankkitili, joka on määritetty **Maksutapa**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="b2765-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="b2765-136">Kun toiminto on käytössä ja istunnon päivämäärä on erääntymispäivää pienempi, maksukirjauskansiota kirjattaessa näyttöön tulee seuraava virhesanoma: "Erääntymispäivämäärän on oltava yhtä suuri tai pienempi kuin istunnon päivämäärä, jos vastatilityyppinä on Pankki".</span><span class="sxs-lookup"><span data-stu-id="b2765-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="b2765-137">Jos toiminto ei ole käytössä, voit kirjata maksukirjauskansion, jossa on myöhemmäksi päivätty sekki, kun istunnon päivämäärä on pienempi kuin erääntymispäivä.</span><span class="sxs-lookup"><span data-stu-id="b2765-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
