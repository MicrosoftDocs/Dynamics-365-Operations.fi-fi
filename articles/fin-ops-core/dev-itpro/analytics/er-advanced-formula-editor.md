---
title: Sähköisen raportoinnin kehittynyt kaavaeditori
description: Tässä ohjeaiheessa esitellään, miten kehittynyttä kaavaeditoria voidaan käyttää lausekkeiden määrittämiseen sähköisen raportoinnin (ER) mallin yhdistämismäärityksessä ja muotokomponenteissa.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
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
ms.openlocfilehash: df402bc20753d2ba14295592f4b40e20f9fdc7bf
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138895"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Sähköisen raportoinnin kehittynyt kaavaeditori

[!include [banner](../includes/banner.md)]

[Sähköisen raportoinnin](general-electronic-reporting.md) [kaavaeditorin](general-electronic-reporting-formula-designer.md) lisäksi voit käyttää kehittynyttä sähköisen raportoinnin kaavaeditoria parantamaan sähköisen raportoinnin (ER) lausekkeiden määrittämisen kokemusta. Kehittynyt editori on selainpohjainen ja perustuu [Monaco-editorille](https://microsoft.github.io/monaco-editor). Yleisimmin käytetyt kehittyneen editorin ominaisuudet kuvataan tässä ohjeaiheessa:

- [Koodin automaattinen muotoilu](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Ennakoiva koodinsyöttö](#CodeCompletion)
- [Koodin selaus](#CodeNavigation)
- [Koodin jäsentäminen](#CodeStructuring)
- [Etsi ja korvaa](#FindAndReplace)
- [Tietojen liittäminen](#DataPasting)
- [Syntaksin värittäminen](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Kehittyneen kaavaeditorin aktivointi</a>

Suorita seuraavat vaiheet aloittaaksesi kehittyneen kaavaeditorin käytön Microsoft Dynamics 365 Finance -esiintymässäsi.

1.  Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritykset**.
2.  Valitse  **Määritykset** -sivun toimintoruudun  **Määritykset** -välilehden  **Lisämääritykset** -ryhmässä  **Käyttäjäparametrit**.
3.  Määritä  **Suorituksen jäljitys**  -osan  **Käyttäjäparametrit** -valintaruudussa parametrin **Ota kehittynyt kaavaeditori** käyttöön arvoksi **Kyllä**.

[![Sähköisen raportoinnin konfiguroinnit -sivu](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Ota huomioon, että tämä parametri on käyttäjä- ja yrityskohtainen.

## <a name=""></a><a name="Autoformatting">Koodin automaattinen muotoilu</a>

Kun kirjoitat useista koodiriveistä koostuvan monimutkaisen lausekkeen, uuden kirjoitetun rivin sisennys perustuu automaattisesti edellisen rivin sisennykseen. Voit valita rivejä ja muuttaa niiden sisennystä kirjoittamalla **Sarkain** tai **Vaihto+sarkain**.

[![ER-kaavaeditori](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Automaattisen muotoilun avulla voit pitää koko lausekkeen hyvin muotoiltuna ja helpottaa sen ylläpitoa sekä yksinkertaistaa määritetyn logiikan ymmärtämistä.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Editori tarjoaa automaattisen tekstinsyötön auttamaan lausekkeiden nopeammassa kirjoittamisessa ja kirjoitusvirheiden välttämisessä. Kun aloitat uuden tekstin lisäämisen, editori tarjoaa automaattisesti luettelon toiminnoista, joita tuetaan syöttämäsi merkit sisältävissä ER-toiminnoissa. Voit myös käynnistää IntelliSensen missä tahansa määritetyn lausekkeen kohdassa kirjoittamalla **Ctrl+välilyönti**.

[![ER-kaavaeditori](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Ennakoiva koodinsyöttö</a>

Editori tarjoaa automaattisesti ennakoivaa koodinsyöttöä

- Lisäämällä sulkevan sulkeen, kun avaava sulje syötetään. Kohdistin pysyy sulkeiden välissä.
- Lisäämällä toisen lainausmerkin, kun ensimmäinen on syötetty. Kohdistin pysyy lainausmerkkien välissä.
- Lisäämällä toisen kaksoislainausmerkin, kun ensimmäinen on syötetty. Kohdistin pysyy lainausmerkkien välissä.

[![ER-kaavaeditori](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Kun osoitat kirjoitettua suljetta, sen pari korostetaan automaattisesti niiden tukeman rakenteen näyttämiseksi.

## <a name=""></a><a name="CodeNavigation">Koodin selaus</a>

Voit etsiä tarvittavia symboleja tai rivejä lausekkeestasi kirjoittamalla **Go to** -komennon komentopaletin tai kontekstivalikon avulla.

Voit esimerkiksi siirtyä riville **8** seuraavasti:

- Paina **Ctrl+G** syötä arvo **8** ja paina sitten **Enter**.

  -tai-

- Paina **F1**, kirjoita **G**, valitse **Siirry riville**, syötä arvo **8** ja paina **Enter**.

[![ER-kaavaeditori](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Koodin jäsentäminen</a>

Joidenkin toimintojen, kuten [IF](er-functions-logical-if.md) tai [CASE](er-functions-logical-case.md), koodi jäsennetään automaattisesti. Voit laajentaa ja tiivistää minkä tahansa tai kaikki tämän koodin piilotettavat alueet lausekkeen muokattavan osuuden pienentämiseksi ja vain siihen osaan keskittymiseksi, joka vaatii huomiota. Siihen voidaan käyttää Piilota/näytä-komentojen valintaa.

Voit esimerkiksi piilottaa kaikki alueet seuraavasti:

- Paina **Ctrl+K**

  -tai-

- Paina **F1**, paina **FO** valitse **Piilota kaikki** ja paina sitten **Enter**

Voit ottaa kaikki alueet näkyviin seuraavasti:

- Paina **Ctrl+J**

  -tai-
  
- Paina **F1**, kirjoita **UN** valitse **Näytä kaikki** ja paina sitten **Enter**

[![ER-kaavaeditori](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Etsi ja korvaa</a>

Voit etsiä tietyn tekstin esiintymät valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:

- Paina **Ctrl+F** ja sitten **F3** löytääksesi valitun tekstin seuraavan esiintymän tai paina **Shift+F3** löytääksesi edellisen esiintymän.

  -tai-
  
- Paina **F1**, kirjoita **F** ja valitse sitten tarvittava vaihtoehto valitun tekstin löytämiseksi.

Voit korvata tietyn tekstin esiintymiä valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:

- Paina **Ctrl+H**. Kirjoita vaihtoehtoinen teksti ja valitse korvausvaihtoehto korvataksesi joko valitun tekstin tai kaikki kyseisen tekstin esiintymät kulloisessakin lausekkeessa.

  -tai-
  
- Paina **F1**, kirjoita **R** ja valitse sitten tarvittava vaihtoehto valitun tekstin korvaamiseksi. Kirjoita vaihtoehtoinen teksti ja valitse korvausvaihtoehto korvataksesi joko valitun tekstin tai kaikki kyseisen tekstin esiintymät kulloisessakin lausekkeessa.

Voit muuttaa kaikkia tietyn tekstin esiintymiä valitsemalla lausekkeen tekstin ja tekemällä seuraavat toimet:

- Paina **Ctrl+F2** ja kirjoita vaihtoehtoinen teksti.

  -tai-
  
- Paina **F1**, kirjoita **C** ja valitse sitten tarvittava vaihtoehto valitun tekstin muuttamiseksi. Syötä vaihtoehtoinen teksti.

[![ER-kaavaeditori](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Tietolähteiden ja toimintojen liittäminen</a>

Voit valita **Lisää tietolähde**, jolla kulloiseenkin lausekkeeseen lisätään vasemmassa **Tietolähde**-ruudussa valittuna oleva tietolähde. Voit myös valita **Lisää toiminto**, jolla kulloiseenkin lausekkeeseen lisätään oikeassa **Toiminnot**-ruudussa valittuna oleva toiminto. Jos käytät ER-muotoeditoria, valittu toiminto tai valittu tietolähde liitetään aina määritetyn lausekkeen loppuun. Kun käytät kehittynyttä ER-muotoeditoria, valittu toiminto tai valittu tietolähde voidaan liittää mihin tahansa kohtaan määritettyä lauseketta. Sinun on käytettävä kohdistinta määrittääksesi, mihin haluat liittää tiedot.

[![ER-kaavaeditori](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Syntaksin värittäminen</a>

Tällä hetkellä eri värejä käytetään korostamaan seuraavia lausekkeiden osia:

- Kaksoissulkeissa oleva teksti, joka voi edustaa tekstivakion etikettitunnusta.

[![ER-kaavaeditori](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)
- [Monaco-editori](https://microsoft.github.io/monaco-editor)
