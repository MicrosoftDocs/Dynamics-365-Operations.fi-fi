---
title: Kulutositteiden käsittely
description: Tässä ohjeaiheessa on tietoja optisen merkkien tunnistuksen (OCR) käytöstä tositteiden käsittelyssä. Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja Microsoft Dynamics 365 Financessa.
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
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
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027900"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="a60b1-104">Julkinen esikatselu: Kulutositteiden käsittely</span><span class="sxs-lookup"><span data-stu-id="a60b1-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="a60b1-105">Kulujen kirjausta on parannettu ottamalla käyttöön optinen merkkien tunnistus (OCR) tositteiden osalta.</span><span class="sxs-lookup"><span data-stu-id="a60b1-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="a60b1-106">Tämä ominaisuus on suunniteltu parantamaan käyttökokemusta, kun luodaan kuluraportteja.</span><span class="sxs-lookup"><span data-stu-id="a60b1-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="a60b1-107">Tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="a60b1-107">Key features</span></span>

- <span data-ttu-id="a60b1-108">Tositteista haetaan myyjän nimi, päivämäärä ja kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="a60b1-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="a60b1-109">Ominaisuus yrittää yhdistää liittämättömät tositteet liittämättömiin kulutapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="a60b1-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="a60b1-110">Käyttäjät voivat luoda tositteista manuaalisesti kirjattuja kulutapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a60b1-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="a60b1-111">Käyttöesimerkkejä</span><span class="sxs-lookup"><span data-stu-id="a60b1-111">Usage examples</span></span>

- <span data-ttu-id="a60b1-112">**Luottokorttitapahtumia sisältävien tositteiden automaattinen liittäminen, kun kuluraportti luodaan.**</span><span class="sxs-lookup"><span data-stu-id="a60b1-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="a60b1-113">Avaa **Kulujen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="a60b1-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="a60b1-114">Tarkista **Tositteet**-välilehdessä, että liittämättömiä tositteita on olemassa.</span><span class="sxs-lookup"><span data-stu-id="a60b1-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="a60b1-115">Voit myös ladata tositteita **Tositteet**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="a60b1-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="a60b1-116">Tarkista **Kulut**-välilehdessä, että liittämättömiä kuluja on olemassa.</span><span class="sxs-lookup"><span data-stu-id="a60b1-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="a60b1-117">Tavallisesti kulujen hallinnoija tuo nämä kulut luottokortin myöntäjältä.</span><span class="sxs-lookup"><span data-stu-id="a60b1-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="a60b1-118">Valitse **Uusi kuluraportti**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-118">Select **New expense report**.</span></span> <span data-ttu-id="a60b1-119">Huomaa, että voit nyt sisällyttää kuluja ja tositteita myös kuluraporttiin.</span><span class="sxs-lookup"><span data-stu-id="a60b1-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="a60b1-120">Jos lisäät sekä kuluja että tositteita, automaattinen tositteiden ja kulujen yhdistäminen käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="a60b1-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="a60b1-121">**Luo kulu tai yhdistä kulu tositteesta.**</span><span class="sxs-lookup"><span data-stu-id="a60b1-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="a60b1-122">Liitä tosite kuluraporttiin valitsemalla sen **Tositteet**-välilehdessä **Lisää tositteita**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="a60b1-123">Huomaa tositteen ladatun kuvan alla asetukset **Luo** ja **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="a60b1-124">Luo manuaalisesti kirjattu kulutapahtuma ja täytä tositteesta haetut arvot valitsemalla **Luo**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="a60b1-125">Jos valitset **Yhdistä**, järjestelmä yrittää yhdistää olemassa olevan kulun tositteeseen.</span><span class="sxs-lookup"><span data-stu-id="a60b1-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="a60b1-126">Asentaminen</span><span class="sxs-lookup"><span data-stu-id="a60b1-126">Installation</span></span>

<span data-ttu-id="a60b1-127">Tämä ominaisuus toimii yhdessä **Kuluraporttien uusi toteutus** -ominaisuuden kanssa yksinkertaistaen kulukokemusta.</span><span class="sxs-lookup"><span data-stu-id="a60b1-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="a60b1-128">Jos haluat käyttää näitä kehittyneitä kuluominaisuuksia, asenna Microsoftin Dynamics 365 Financen kulujenhallintapalvelu ja ota ominaisuudet käyttöön esiintymässäsi.</span><span class="sxs-lookup"><span data-stu-id="a60b1-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="a60b1-129">Voit käyttää lisäosaa projektistasi Microsoft Dynamicsin Lifecycle Servicesissä (LCS).</span><span class="sxs-lookup"><span data-stu-id="a60b1-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="a60b1-130">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="a60b1-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="a60b1-131">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="a60b1-132">Valitse **Ylläpito** tai selaa alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="a60b1-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="a60b1-133">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="a60b1-134">Valitse **Kulujenhallintapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="a60b1-135">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="a60b1-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="a60b1-136">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-136">Select **Install**.</span></span>

<span data-ttu-id="a60b1-137">Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="a60b1-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="a60b1-138">Kuluraporttien uusi toteutus</span><span class="sxs-lookup"><span data-stu-id="a60b1-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="a60b1-139">Automaattinen vastaavuus ja kulujen luonti kuitista</span><span class="sxs-lookup"><span data-stu-id="a60b1-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="a60b1-140">Kun otat nämä ominaisuudet käyttöön, seuraavat toiminnot toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="a60b1-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="a60b1-141">Aiemmin luotu **Kulujen hallinta** -työtila korvataan uudella työtilalla.</span><span class="sxs-lookup"><span data-stu-id="a60b1-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a60b1-142">Uusi kulukentän näkyvyyden valikkovaihtoehto lisätään.</span><span class="sxs-lookup"><span data-stu-id="a60b1-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a60b1-143">Voit edelleen avata aiemman **Kuluraportit** -sivun siirtymällä kohtaan **Kulujen hallinta > Omat kulut > Kuluraportit**.</span><span class="sxs-lookup"><span data-stu-id="a60b1-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="a60b1-144">Työn kulut ja hyväksynnät ovat edelleen olemassa kuluraportit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a60b1-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="a60b1-145">Tositteet käsitellään Microsoft Azure Cognitive Servicesin kautta ja metatietoja haetaan ja lisätään.</span><span class="sxs-lookup"><span data-stu-id="a60b1-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="a60b1-146">Järjestelmä lisää vaihtoehdon, jonka avulla voit luoda kuluraportin, joka sisältää yhdistetyt liittämättömät tositteet.</span><span class="sxs-lookup"><span data-stu-id="a60b1-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="a60b1-147">Kuluraportteihin lisättävä vaihtoehto mahdollistaa kulurivin luomisen tositteesta. Se voi myös yrittää yhdistää olemassa olevan tositteen olemassa olevaan kuluriviin.</span><span class="sxs-lookup"><span data-stu-id="a60b1-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="a60b1-148">Lisätietoja Kuluraporttien uusi toteutus -ominaisuudesta on kohdassa [Kuluraporttien uusi toteutus](ExpenseWorkspaceNew.md)</span><span class="sxs-lookup"><span data-stu-id="a60b1-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a60b1-149">Usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a60b1-149">Frequently asked questions</span></span>

<span data-ttu-id="a60b1-150">**Käyttääkö Microsoft tietojani mallejaan varten?**</span><span class="sxs-lookup"><span data-stu-id="a60b1-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="a60b1-151">Ei, Microsoft kehittänyt yleisen koneoppimismallin tositteiden käsittelypalveluaan varten.</span><span class="sxs-lookup"><span data-stu-id="a60b1-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="a60b1-152">Tämä malli ei perustu lataamiisi tositteisiin.</span><span class="sxs-lookup"><span data-stu-id="a60b1-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="a60b1-153">**Missä tämä ominaisuus on käytettävissä ja missä se käsitellään?**</span><span class="sxs-lookup"><span data-stu-id="a60b1-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="a60b1-154">Tällä hetkellä tuettuna on Yhdysvallat.</span><span class="sxs-lookup"><span data-stu-id="a60b1-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="a60b1-155">**Minne tositteeni menevät?**</span><span class="sxs-lookup"><span data-stu-id="a60b1-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="a60b1-156">Finance muodostaa yhteyden Cognitive Servicesiin hakeakseen kenttätiedot.</span><span class="sxs-lookup"><span data-stu-id="a60b1-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="a60b1-157">Cognitive Services säilyttää kopion tositteestasi käsittelyn yhteydessä jopa 24 tunnin ajan.</span><span class="sxs-lookup"><span data-stu-id="a60b1-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="a60b1-158">Kun käsittely on valmis, Cognitive Services poistaa tositteen.</span><span class="sxs-lookup"><span data-stu-id="a60b1-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="a60b1-159">Tositteet ovat edelleen tallennettuna Financessa.</span><span class="sxs-lookup"><span data-stu-id="a60b1-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="a60b1-160">Lisätietoja on kohdassa [Ota käyttöön tositteiden käsittely muodontunnistimen uudella ominaisuudella](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="a60b1-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>