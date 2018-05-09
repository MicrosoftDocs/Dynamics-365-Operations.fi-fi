--- 
title: "Vapaatekstilaskumallin määrittäminen asiakkaalle"
description: "Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ea5f1ddd8f6be8a1dd2cee47b7746c4764ba28a4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="f36ed-103">Vapaatekstilaskumallin määrittäminen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="f36ed-103">Assign a free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f36ed-104">Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="f36ed-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="f36ed-105">Tässä tehtävässä käytetään USMF-esittely-yritystä. Tehtävä on tarkoitettu myyntireskontran laskujen hallinnasta ja käsittelemisestä vastaavalle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="f36ed-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="f36ed-106">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="f36ed-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="f36ed-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f36ed-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f36ed-108">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="f36ed-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="f36ed-109">Valitse Toistuvat laskut.</span><span class="sxs-lookup"><span data-stu-id="f36ed-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="f36ed-110">Tällä sivulla liitetään vapaatekstilaskun mallit asiakkaille ja määritetään, miten usein laskut lähetetään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="f36ed-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="f36ed-111">Valitse Uusi, kun haluat liittää asiakkaalle uuden mallin.</span><span class="sxs-lookup"><span data-stu-id="f36ed-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="f36ed-112">Valitse vapaatekstilaskun malli, jonka haluat liittää asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="f36ed-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="f36ed-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f36ed-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f36ed-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f36ed-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f36ed-115">Syötä ensimmäisen laskun luontipäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f36ed-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="f36ed-116">Määritä toiston päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f36ed-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="f36ed-117">Valitse jokin seuraavista vaihtoehdoista: Päättymispäivä puuttuu – Laskuja luodaan niin kauan kunnes malli poistetaan asiakkaan tililtä.</span><span class="sxs-lookup"><span data-stu-id="f36ed-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="f36ed-118">Laskutuksen päättymispäivämäärä – Valitse tämä vaihtoehto, kun haluat syöttää laskun luonnille viimeisen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="f36ed-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="f36ed-119">Suurin mahdollinen kumulatiivinen summa, jonka jälkeen laskujen luominen päättyy.</span><span class="sxs-lookup"><span data-stu-id="f36ed-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="f36ed-120">Syötä suurin mahdollinen kumulatiivinen summa, joka valitun mallin avulla voidaan saavuttaa.</span><span class="sxs-lookup"><span data-stu-id="f36ed-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="f36ed-121">Jos esimerkiksi syötät arvioksi 1 000,00, ja kuukauden laskutus on 100,00, laskujen luominen päättyy kymmenennen laskun jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f36ed-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="f36ed-122">Toistuvat laskut luodaan vapaatekstilaskun mallin tai asiakkaan tilin oletusarvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f36ed-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="f36ed-123">Valitse käytettäväksi vapaatekstilaskumalli tai asiakastili, kun laskujen luonnin yhteydessä määritetään oletusarvo kielelle, kirjausprofiilille, arvonlisäveroryhmälle, nimikkeen arvonlisäveroryhmälle, luettelokoodille, toimituksen maalle/alueelle, valuutalle, maksuehdoille, maksutavalle, maksumääritykselle, maksuaikataululle, käteisalennukselle, taloushallinnon dimensiolle ja tilisiirtolomakkeelle.</span><span class="sxs-lookup"><span data-stu-id="f36ed-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="f36ed-124">Valitse toistumismalli.</span><span class="sxs-lookup"><span data-stu-id="f36ed-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="f36ed-125">Päivittäin – Valitse tämä vaihtoehto ja syötä päivien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f36ed-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="f36ed-126">Jos syötät esimerkiksi luvun 15, asiakkaalle luodaan lasku 15 päivän välein.</span><span class="sxs-lookup"><span data-stu-id="f36ed-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="f36ed-127">Viikoittain – Valitse tämä vaihtoehto ja syötä viikkojen määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f36ed-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="f36ed-128">Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen viikko.</span><span class="sxs-lookup"><span data-stu-id="f36ed-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="f36ed-129">Kuukausittain – Valitse tämä vaihtoehto ja syötä kuukausien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f36ed-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="f36ed-130">Jos syötät esimerkiksi luvun 6, asiakkaalle luodaan lasku kuuden kuukauden välein.</span><span class="sxs-lookup"><span data-stu-id="f36ed-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="f36ed-131">Vuosittain– Valitse tämä vaihtoehto ja syötä vuosien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f36ed-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="f36ed-132">Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen vuosi.</span><span class="sxs-lookup"><span data-stu-id="f36ed-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="f36ed-133">Syötä numero Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f36ed-133">In the Per field, enter a number.</span></span>


