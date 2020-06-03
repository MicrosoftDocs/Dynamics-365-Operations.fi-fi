---
title: Kulutositteiden käsittely
description: Tässä ohjeaiheessa on tietoja optisen merkkien tunnistuksen (OCR) käytöstä tositteiden käsittelyssä. Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja Microsoft Dynamics 365 Financessa.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378228"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="247ee-104">Kulukuittien käsittely</span><span class="sxs-lookup"><span data-stu-id="247ee-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="247ee-105">Kulujen kirjausta on parannettu ottamalla käyttöön optinen merkkien tunnistus (OCR) tositteiden osalta.</span><span class="sxs-lookup"><span data-stu-id="247ee-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="247ee-106">Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja.</span><span class="sxs-lookup"><span data-stu-id="247ee-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="247ee-107">Tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="247ee-107">Key features</span></span>

- <span data-ttu-id="247ee-108">Tositteista haetaan myyjän nimi, päivämäärä ja kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="247ee-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="247ee-109">Ominaisuus yrittää yhdistää liittämättömät tositteet liittämättömiin kulutapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="247ee-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="247ee-110">Käyttäjät voivat luoda tositteista manuaalisesti kirjattuja kulutapahtumia.</span><span class="sxs-lookup"><span data-stu-id="247ee-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="247ee-111">Käyttöesimerkkejä</span><span class="sxs-lookup"><span data-stu-id="247ee-111">Usage examples</span></span>

<span data-ttu-id="247ee-112">Luottokorttitapahtumia sisältävien tositteiden automaattinen liittäminen, kun kuluraportti luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="247ee-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="247ee-113">Avaa **Kulujen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="247ee-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="247ee-114">Tarkista **Tositteet**-välilehdessä, että liittämättömiä tositteita on olemassa.</span><span class="sxs-lookup"><span data-stu-id="247ee-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="247ee-115">Voit myös ladata tositteita **Tositteet**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="247ee-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="247ee-116">Tarkista **Kulut**-välilehdessä, että liittämättömiä kuluja on olemassa.</span><span class="sxs-lookup"><span data-stu-id="247ee-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="247ee-117">Tavallisesti kulujen hallinnoija tuo nämä kulut luottokortin myöntäjältä.</span><span class="sxs-lookup"><span data-stu-id="247ee-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="247ee-118">Valitse **Uusi kuluraportti**.</span><span class="sxs-lookup"><span data-stu-id="247ee-118">Select **New expense report**.</span></span> <span data-ttu-id="247ee-119">Huomaa, että voit nyt sisällyttää kuluja ja tositteita myös kuluraporttiin.</span><span class="sxs-lookup"><span data-stu-id="247ee-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="247ee-120">Jos lisäät sekä kuluja että tositteita, automaattinen tositteiden ja kulujen yhdistäminen käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="247ee-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="247ee-121">Kulu luodaan tai täsmäytetään tositteesta seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="247ee-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="247ee-122">Liitä tosite kuluraporttiin valitsemalla sen **Tositteet**-välilehdessä **Lisää tositteita**.</span><span class="sxs-lookup"><span data-stu-id="247ee-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="247ee-123">Huomaa tositteen ladatun kuvan alla asetukset **Luo** ja **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="247ee-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="247ee-124">Luo manuaalisesti kirjattu kulutapahtuma ja täytä tositteesta haetut arvot valitsemalla **Luo**.</span><span class="sxs-lookup"><span data-stu-id="247ee-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="247ee-125">Jos valitset **Yhdistä**, järjestelmä yrittää yhdistää olemassa olevan kulun tositteeseen.</span><span class="sxs-lookup"><span data-stu-id="247ee-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="247ee-126">Asentaminen</span><span class="sxs-lookup"><span data-stu-id="247ee-126">Installation</span></span>

<span data-ttu-id="247ee-127">Tämä ominaisuus toimii yhdessä **Kuluraporttien uusi toteutus** -ominaisuuden kanssa yksinkertaistaen kulukokemusta.</span><span class="sxs-lookup"><span data-stu-id="247ee-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="247ee-128">Toiminto on käytettävissä vain tasoa 2 korkeammissa ympäristöissä eli eristys- ja tuotantoympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="247ee-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="247ee-129">Jos haluat käyttää näitä kehittyneitä kuluominaisuuksia, asenna Microsoftin Dynamics 365 Financen kulujenhallintapalvelu ja ota ominaisuudet käyttöön esiintymässäsi.</span><span class="sxs-lookup"><span data-stu-id="247ee-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="247ee-130">Voit käyttää lisäosaa projektistasi Microsoft Dynamicsin Lifecycle Servicesissä (LCS).</span><span class="sxs-lookup"><span data-stu-id="247ee-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="247ee-131">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="247ee-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="247ee-132">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="247ee-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="247ee-133">Valitse **Ylläpito** tai selaa alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="247ee-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="247ee-134">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="247ee-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="247ee-135">Valitse **Kulujenhallintapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="247ee-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="247ee-136">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="247ee-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="247ee-137">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="247ee-137">Select **Install**.</span></span>

<span data-ttu-id="247ee-138">Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="247ee-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="247ee-139">Kuluraporttien uusi toteutus</span><span class="sxs-lookup"><span data-stu-id="247ee-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="247ee-140">Automaattinen vastaavuus ja kulujen luonti kuitista</span><span class="sxs-lookup"><span data-stu-id="247ee-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="247ee-141">Kun otat nämä ominaisuudet käyttöön, seuraavat toiminnot toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="247ee-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="247ee-142">Aiemmin luotu **Kulujen hallinta** -työtila korvataan uudella työtilalla.</span><span class="sxs-lookup"><span data-stu-id="247ee-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="247ee-143">Uusi kulukentän näkyvyyden valikkovaihtoehto lisätään.</span><span class="sxs-lookup"><span data-stu-id="247ee-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="247ee-144">Voit edelleen avata aiemman **Kuluraportit** -sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.</span><span class="sxs-lookup"><span data-stu-id="247ee-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="247ee-145">Työn kulut ja hyväksynnät ovat edelleen olemassa kuluraportit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="247ee-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="247ee-146">Tositteet käsitellään Microsoft Azure Cognitive Servicesin kautta ja metatietoja haetaan ja lisätään.</span><span class="sxs-lookup"><span data-stu-id="247ee-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="247ee-147">Järjestelmä lisää vaihtoehdon, jonka avulla voit luoda kuluraportin, joka sisältää yhdistetyt liittämättömät tositteet.</span><span class="sxs-lookup"><span data-stu-id="247ee-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="247ee-148">Kuluraportteihin lisättävä vaihtoehto mahdollistaa kulurivin luomisen tositteesta. Se voi myös yrittää yhdistää olemassa olevan tositteen olemassa olevaan kuluriviin.</span><span class="sxs-lookup"><span data-stu-id="247ee-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="247ee-149">Lisätietoja Kuluraporttien uusi toteutus -ominaisuudesta on kohdassa [Kuluraporttien uusi toteutus](ExpenseWorkspaceNew.md)</span><span class="sxs-lookup"><span data-stu-id="247ee-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="247ee-150">Usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="247ee-150">Frequently asked questions</span></span>

<span data-ttu-id="247ee-151">**Käyttääkö Microsoft tietojani mallejaan varten?**</span><span class="sxs-lookup"><span data-stu-id="247ee-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="247ee-152">Ei, Microsoft kehittänyt yleisen koneoppimismallin tositteiden käsittelypalveluaan varten.</span><span class="sxs-lookup"><span data-stu-id="247ee-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="247ee-153">Tämä malli ei perustu lataamiisi tositteisiin.</span><span class="sxs-lookup"><span data-stu-id="247ee-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="247ee-154">**Missä tämä ominaisuus on käytettävissä ja missä se käsitellään?**</span><span class="sxs-lookup"><span data-stu-id="247ee-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="247ee-155">Tällä hetkellä tuettuna on Yhdysvallat.</span><span class="sxs-lookup"><span data-stu-id="247ee-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="247ee-156">**Minne tositteeni menevät?**</span><span class="sxs-lookup"><span data-stu-id="247ee-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="247ee-157">Finance muodostaa yhteyden Cognitive Servicesiin hakeakseen kenttätiedot.</span><span class="sxs-lookup"><span data-stu-id="247ee-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="247ee-158">Cognitive Services säilyttää kopion tositteestasi käsittelyn yhteydessä jopa 24 tunnin ajan.</span><span class="sxs-lookup"><span data-stu-id="247ee-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="247ee-159">Kun käsittely on valmis, Cognitive Services poistaa tositteen.</span><span class="sxs-lookup"><span data-stu-id="247ee-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="247ee-160">Tositteet ovat edelleen tallennettuna Financessa.</span><span class="sxs-lookup"><span data-stu-id="247ee-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="247ee-161">Lisätietoja on kohdassa [Ota käyttöön tositteiden käsittely muodontunnistimen uudella ominaisuudella](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="247ee-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
