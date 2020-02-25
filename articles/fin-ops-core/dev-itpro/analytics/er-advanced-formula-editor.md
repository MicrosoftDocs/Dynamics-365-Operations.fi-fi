---
title: Sähköisen raportoinnin kehittynyt kaavaeditori
description: Tässä ohjeaiheessa esitellään, miten kehittynyttä kaavaeditoria voidaan käyttää lausekkeiden määrittämiseen sähköisen raportoinnin (ER) mallin yhdistämismäärityksessä ja muotokomponenteissa.
author: NickSelin
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d183f77da1dda0c4f04e4e48ab3db0133f494a55
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015198"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="0d909-103">Sähköisen raportoinnin kehittynyt kaavaeditori</span><span class="sxs-lookup"><span data-stu-id="0d909-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0d909-104">[Sähköisen raportoinnin](general-electronic-reporting.md) [kaavaeditorin](general-electronic-reporting-formula-designer.md) lisäksi voit käyttää kehittynyttä sähköisen raportoinnin kaavaeditoria parantamaan sähköisen raportoinnin (ER) lausekkeiden määrittämisen kokemusta.</span><span class="sxs-lookup"><span data-stu-id="0d909-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="0d909-105">Kehittynyt editori on selainpohjainen ja perustuu [Monaco-editorille](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="0d909-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="0d909-106">Yleisimmin käytetyt kehittyneen editorin ominaisuudet kuvataan tässä ohjeaiheessa:</span><span class="sxs-lookup"><span data-stu-id="0d909-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="0d909-107">Koodin automaattinen muotoilu</span><span class="sxs-lookup"><span data-stu-id="0d909-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="0d909-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="0d909-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="0d909-109">Ennakoiva koodinsyöttö</span><span class="sxs-lookup"><span data-stu-id="0d909-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="0d909-110">Koodin selaus</span><span class="sxs-lookup"><span data-stu-id="0d909-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="0d909-111">Koodin jäsentäminen</span><span class="sxs-lookup"><span data-stu-id="0d909-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="0d909-112">Etsi ja korvaa</span><span class="sxs-lookup"><span data-stu-id="0d909-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="0d909-113">Tietojen liittäminen</span><span class="sxs-lookup"><span data-stu-id="0d909-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="0d909-114">Syntaksin värittäminen</span><span class="sxs-lookup"><span data-stu-id="0d909-114">Syntax colorization</span></span>](#SyntaxColorization)

## <span data-ttu-id="0d909-115"><a name="ActivateAdvEditor">Kehittyneen kaavaeditorin aktivointi</a></span><span class="sxs-lookup"><span data-stu-id="0d909-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="0d909-116">Suorita seuraavat vaiheet aloittaaksesi kehittyneen kaavaeditorin käytön Microsoft Dynamics 365 Finance -esiintymässäsi.</span><span class="sxs-lookup"><span data-stu-id="0d909-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="0d909-117">Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritykset**.</span><span class="sxs-lookup"><span data-stu-id="0d909-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="0d909-118">Valitse  **Määritykset** -sivun toimintoruudun  **Määritykset** -välilehden  **Lisämääritykset** -ryhmässä  **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="0d909-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="0d909-119">Määritä  **Suorituksen jäljitys**  -osan  **Käyttäjäparametrit** -valintaruudussa parametrin **Ota kehittynyt kaavaeditori** käyttöön arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0d909-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="0d909-120">[![Sähköisen raportoinnin konfiguroinnit -sivu](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="0d909-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0d909-121">Ota huomioon, että tämä parametri on käyttäjä- ja yrityskohtainen.</span><span class="sxs-lookup"><span data-stu-id="0d909-121">Be aware that this parameter is user specific and company specific.</span></span>

## <span data-ttu-id="0d909-122"><a name="Autoformatting">Koodin automaattinen muotoilu</a></span><span class="sxs-lookup"><span data-stu-id="0d909-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="0d909-123">Kun kirjoitat useista koodiriveistä koostuvan monimutkaisen lausekkeen, uuden kirjoitetun rivin sisennys perustuu automaattisesti edellisen rivin sisennykseen.</span><span class="sxs-lookup"><span data-stu-id="0d909-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="0d909-124">Voit valita rivejä ja muuttaa niiden sisennystä kirjoittamalla **Sarkain** tai **Vaihto+sarkain**.</span><span class="sxs-lookup"><span data-stu-id="0d909-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="0d909-125">[![ER-kaavaeditori](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="0d909-126">Automaattisen muotoilun avulla voit pitää koko lausekkeen hyvin muotoiltuna ja helpottaa sen ylläpitoa sekä yksinkertaistaa määritetyn logiikan ymmärtämistä.</span><span class="sxs-lookup"><span data-stu-id="0d909-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <span data-ttu-id="0d909-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="0d909-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="0d909-128">Editori tarjoaa automaattisen tekstinsyötön auttamaan lausekkeiden nopeammassa kirjoittamisessa ja kirjoitusvirheiden välttämisessä.</span><span class="sxs-lookup"><span data-stu-id="0d909-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="0d909-129">Kun aloitat uuden tekstin lisäämisen, editori tarjoaa automaattisesti luettelon toiminnoista, joita tuetaan syöttämäsi merkit sisältävissä ER-toiminnoissa.</span><span class="sxs-lookup"><span data-stu-id="0d909-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="0d909-130">Voit myös käynnistää IntelliSensen missä tahansa määritetyn lausekkeen kohdassa kirjoittamalla **Ctrl+välilyönti**.</span><span class="sxs-lookup"><span data-stu-id="0d909-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="0d909-131">[![ER-kaavaeditori](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <span data-ttu-id="0d909-132"><a name="CodeCompletion">Ennakoiva koodinsyöttö</a></span><span class="sxs-lookup"><span data-stu-id="0d909-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="0d909-133">Editori tarjoaa automaattisesti ennakoivaa koodinsyöttöä</span><span class="sxs-lookup"><span data-stu-id="0d909-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="0d909-134">Lisäämällä sulkevan sulkeen, kun avaava sulje syötetään. Kohdistin pysyy sulkeiden välissä.</span><span class="sxs-lookup"><span data-stu-id="0d909-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="0d909-135">Lisäämällä toisen lainausmerkin, kun ensimmäinen on syötetty. Kohdistin pysyy lainausmerkkien välissä.</span><span class="sxs-lookup"><span data-stu-id="0d909-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="0d909-136">Lisäämällä toisen kaksoislainausmerkin, kun ensimmäinen on syötetty. Kohdistin pysyy lainausmerkkien välissä.</span><span class="sxs-lookup"><span data-stu-id="0d909-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="0d909-137">[![ER-kaavaeditori](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="0d909-138">Kun osoitat kirjoitettua suljetta, sen pari korostetaan automaattisesti niiden tukeman rakenteen näyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="0d909-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <span data-ttu-id="0d909-139"><a name="CodeNavigation">Koodin selaus</a></span><span class="sxs-lookup"><span data-stu-id="0d909-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="0d909-140">Voit etsiä tarvittavia symboleja tai rivejä lausekkeestasi kirjoittamalla **Go to** -komennon komentopaletin tai kontekstivalikon avulla.</span><span class="sxs-lookup"><span data-stu-id="0d909-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="0d909-141">Voit esimerkiksi siirtyä riville **8** seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0d909-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="0d909-142">Paina **Ctrl+G** syötä arvo **8** ja paina sitten **Enter**.</span><span class="sxs-lookup"><span data-stu-id="0d909-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="0d909-143">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-143">-or-</span></span>

- <span data-ttu-id="0d909-144">Paina **F1**, kirjoita **G**, valitse **Siirry riville**, syötä arvo **8** ja paina **Enter**.</span><span class="sxs-lookup"><span data-stu-id="0d909-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="0d909-145">[![ER-kaavaeditori](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <span data-ttu-id="0d909-146"><a name="CodeStructuring">Koodin jäsentäminen</a></span><span class="sxs-lookup"><span data-stu-id="0d909-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="0d909-147">Joidenkin toimintojen, kuten [IF](er-functions-logical-if.md) tai [CASE](er-functions-logical-case.md), koodi jäsennetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0d909-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="0d909-148">Voit laajentaa ja tiivistää minkä tahansa tai kaikki tämän koodin piilotettavat alueet lausekkeen muokattavan osuuden pienentämiseksi ja vain siihen osaan keskittymiseksi, joka vaatii huomiota.</span><span class="sxs-lookup"><span data-stu-id="0d909-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="0d909-149">Siihen voidaan käyttää Piilota/näytä-komentojen valintaa.</span><span class="sxs-lookup"><span data-stu-id="0d909-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="0d909-150">Voit esimerkiksi piilottaa kaikki alueet seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0d909-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="0d909-151">Paina **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="0d909-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="0d909-152">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-152">-or-</span></span>

- <span data-ttu-id="0d909-153">Paina **F1**, paina **FO** valitse **Piilota kaikki** ja paina sitten **Enter**</span><span class="sxs-lookup"><span data-stu-id="0d909-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="0d909-154">Voit ottaa kaikki alueet näkyviin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0d909-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="0d909-155">Paina **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="0d909-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="0d909-156">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-156">-or-</span></span>
  
- <span data-ttu-id="0d909-157">Paina **F1**, kirjoita **UN** valitse **Näytä kaikki** ja paina sitten **Enter**</span><span class="sxs-lookup"><span data-stu-id="0d909-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="0d909-158">[![ER-kaavaeditori](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <span data-ttu-id="0d909-159"><a name="FindAndReplace">Etsi ja korvaa</a></span><span class="sxs-lookup"><span data-stu-id="0d909-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="0d909-160">Voit etsiä tietyn tekstin esiintymät valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="0d909-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d909-161">Paina **Ctrl+F** ja sitten **F3** löytääksesi valitun tekstin seuraavan esiintymän tai paina **Shift+F3** löytääksesi edellisen esiintymän.</span><span class="sxs-lookup"><span data-stu-id="0d909-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="0d909-162">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-162">-or-</span></span>
  
- <span data-ttu-id="0d909-163">Paina **F1**, kirjoita **F** ja valitse sitten tarvittava vaihtoehto valitun tekstin löytämiseksi.</span><span class="sxs-lookup"><span data-stu-id="0d909-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="0d909-164">Voit korvata tietyn tekstin esiintymiä valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="0d909-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d909-165">Paina **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="0d909-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="0d909-166">Kirjoita vaihtoehtoinen teksti ja valitse korvausvaihtoehto korvataksesi joko valitun tekstin tai kaikki kyseisen tekstin esiintymät kulloisessakin lausekkeessa.</span><span class="sxs-lookup"><span data-stu-id="0d909-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="0d909-167">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-167">-or-</span></span>
  
- <span data-ttu-id="0d909-168">Paina **F1**, kirjoita **R** ja valitse sitten tarvittava vaihtoehto valitun tekstin korvaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="0d909-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="0d909-169">Kirjoita vaihtoehtoinen teksti ja valitse korvausvaihtoehto korvataksesi joko valitun tekstin tai kaikki kyseisen tekstin esiintymät kulloisessakin lausekkeessa.</span><span class="sxs-lookup"><span data-stu-id="0d909-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="0d909-170">Voit muuttaa kaikkia tietyn tekstin esiintymiä valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="0d909-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="0d909-171">Paina **Ctrl+F2** ja kirjoita vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="0d909-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="0d909-172">-tai-</span><span class="sxs-lookup"><span data-stu-id="0d909-172">-or-</span></span>
  
- <span data-ttu-id="0d909-173">Paina **F1**, kirjoita **C** ja valitse sitten tarvittava vaihtoehto valitun tekstin muuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="0d909-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="0d909-174">Syötä vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="0d909-174">Enter the alternative text.</span></span>

<span data-ttu-id="0d909-175">[![ER-kaavaeditori](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <span data-ttu-id="0d909-176"><a name="DataPasting">Tietolähteiden ja toimintojen liittäminen</a></span><span class="sxs-lookup"><span data-stu-id="0d909-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="0d909-177">Voit valita **Lisää tietolähde**, jolla kulloiseenkin lausekkeeseen lisätään vasemmassa **Tietolähde**-ruudussa valittuna oleva tietolähde.</span><span class="sxs-lookup"><span data-stu-id="0d909-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="0d909-178">Voit myös valita **Lisää toiminto**, jolla kulloiseenkin lausekkeeseen lisätään oikeassa **Toiminnot**-ruudussa valittuna oleva toiminto.</span><span class="sxs-lookup"><span data-stu-id="0d909-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="0d909-179">Jos käytät ER-muotoeditoria, valittu toiminto tai valittu tietolähde liitetään aina määritetyn lausekkeen loppuun.</span><span class="sxs-lookup"><span data-stu-id="0d909-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="0d909-180">Kun käytät kehittynyttä ER-muotoeditoria, valittu toiminto tai valittu tietolähde voidaan liittää mihin tahansa kohtaan määritettyä lauseketta.</span><span class="sxs-lookup"><span data-stu-id="0d909-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="0d909-181">Sinun on käytettävä kohdistinta määrittääksesi, mihin haluat liittää tiedot.</span><span class="sxs-lookup"><span data-stu-id="0d909-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="0d909-182">[![ER-kaavaeditori](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="0d909-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <span data-ttu-id="0d909-183"><a name="SyntaxColorization">Syntaksin värittäminen</a></span><span class="sxs-lookup"><span data-stu-id="0d909-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="0d909-184">Tällä hetkellä eri värejä käytetään korostamaan seuraavia lausekkeiden osia:</span><span class="sxs-lookup"><span data-stu-id="0d909-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="0d909-185">Kaksoissulkeissa oleva teksti, joka voi edustaa tekstivakion etikettitunnusta.</span><span class="sxs-lookup"><span data-stu-id="0d909-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="0d909-186">[![ER-kaavaeditori](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="0d909-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d909-187">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0d909-187">Additional resources</span></span>

- [<span data-ttu-id="0d909-188">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0d909-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0d909-189">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="0d909-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="0d909-190">Monaco-editori</span><span class="sxs-lookup"><span data-stu-id="0d909-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
