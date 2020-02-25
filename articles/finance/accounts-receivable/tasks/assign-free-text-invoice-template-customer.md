---
title: Vapaatekstilaskumallin määrittäminen asiakkaalle
description: Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c64a00a839522ea14fc5fcdaca08ab17748f894
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000021"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="b4d16-103">Vapaatekstilaskumallin määrittäminen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="b4d16-103">Assign a free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4d16-104">Tässä tehtävässä kerrotaan, miten vapaatekstilaskun malli liitetään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4d16-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="b4d16-105">Tässä tehtävässä käytetään USMF-esittely-yritystä. Tehtävä on tarkoitettu myyntireskontran laskujen hallinnasta ja käsittelemisestä vastaavalle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="b4d16-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="b4d16-106">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="b4d16-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="b4d16-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b4d16-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b4d16-108">Valitse **toimintoruudussa** **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="b4d16-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="b4d16-109">Valitse **Toistuvat laskut**.</span><span class="sxs-lookup"><span data-stu-id="b4d16-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="b4d16-110">Tällä sivulla liitetään vapaatekstilaskun mallit asiakkaille ja määritetään, miten usein laskut lähetetään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4d16-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="b4d16-111">Valitse **Uusi**, kun haluat liittää asiakkaalle uuden mallin.</span><span class="sxs-lookup"><span data-stu-id="b4d16-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="b4d16-112">Valitse **Malli**-kentässä vapaatekstilaskun malli, jonka haluat liittää asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="b4d16-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="b4d16-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b4d16-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b4d16-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b4d16-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b4d16-115">Syötä **Laskutuksen aloituspäivämäärä** -kenttään ensimmäisen laskun luontipäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b4d16-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="b4d16-116">Määritä **Toisto päättyy** -osassa toiston päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b4d16-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="b4d16-117">Valitse jokin seuraavista vaihtoehdoista: Päättymispäivä puuttuu – Laskuja luodaan niin kauan kunnes malli poistetaan asiakkaan tililtä.</span><span class="sxs-lookup"><span data-stu-id="b4d16-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="b4d16-118">Laskutuksen päättymispäivämäärä – Valitse tämä vaihtoehto, kun haluat syöttää laskun luonnille viimeisen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="b4d16-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="b4d16-119">Syötä **Kumulatiivinen enimmäissumma** -kenttään suurin kumulatiivinen summa, jonka jälkeen laskun luonti pysähtyy.</span><span class="sxs-lookup"><span data-stu-id="b4d16-119">In the **Maximum cummulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="b4d16-120">Syötä suurin mahdollinen kumulatiivinen summa, joka valitun mallin avulla voidaan saavuttaa.</span><span class="sxs-lookup"><span data-stu-id="b4d16-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="b4d16-121">Jos esimerkiksi syötät arvioksi 1 000,00, ja kuukauden laskutus on 100,00, laskujen luominen päättyy kymmenennen laskun jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b4d16-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="b4d16-122">Valitse **Luo toistuvia laskuja käyttämällä oletusarvoja** -osassa vapaatekstilaskun malli tai asiakastili.</span><span class="sxs-lookup"><span data-stu-id="b4d16-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="b4d16-123">Valitse käytettäväksi vapaatekstilaskumalli tai asiakastili, kun laskujen luonnin yhteydessä määritetään oletusarvo kielelle, kirjausprofiilille, arvonlisäveroryhmälle, nimikkeen arvonlisäveroryhmälle, luettelokoodille, toimituksen maalle/alueelle, valuutalle, maksuehdoille, maksutavalle, maksumääritykselle, maksuaikataululle, käteisalennukselle, taloushallinnon dimensiolle ja tilisiirtolomakkeelle.</span><span class="sxs-lookup"><span data-stu-id="b4d16-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="b4d16-124">Valitse **Toistumisen kuvio** -kentässä toistumisen kuvio.</span><span class="sxs-lookup"><span data-stu-id="b4d16-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="b4d16-125">Päivittäin – Valitse tämä vaihtoehto ja syötä päivien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b4d16-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="b4d16-126">Jos syötät esimerkiksi luvun 15, asiakkaalle luodaan lasku 15 päivän välein.</span><span class="sxs-lookup"><span data-stu-id="b4d16-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="b4d16-127">Viikoittain – Valitse tämä vaihtoehto ja syötä viikkojen määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b4d16-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="b4d16-128">Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen viikko.</span><span class="sxs-lookup"><span data-stu-id="b4d16-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="b4d16-129">Kuukausittain – Valitse tämä vaihtoehto ja syötä kuukausien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b4d16-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="b4d16-130">Jos syötät esimerkiksi luvun 6, asiakkaalle luodaan lasku kuuden kuukauden välein.</span><span class="sxs-lookup"><span data-stu-id="b4d16-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="b4d16-131">Vuosittain– Valitse tämä vaihtoehto ja syötä vuosien määrä Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b4d16-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="b4d16-132">Jos syötät esimerkiksi luvun 2, asiakkaalle luodaan lasku joka toinen vuosi.</span><span class="sxs-lookup"><span data-stu-id="b4d16-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="b4d16-133">Syötä numero **Per**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b4d16-133">In the **Per** field, enter a number.</span></span>

