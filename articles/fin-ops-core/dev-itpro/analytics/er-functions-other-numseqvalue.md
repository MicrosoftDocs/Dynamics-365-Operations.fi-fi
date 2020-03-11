---
title: NUMSEQVALUE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMSEQVALUE-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbe5e5ac17af743f8293e4255d9713b528182f66
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041305"
---
# <a name="NUMSEQVALUE">NUMSEQVALUE ER -funktio</a>

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE`-funktio palauttaa *merkkijono*-arvon, joka edustaa numerosarjan uutta luotua arvoa määritetyn numerosarjan, laajuuden ja vaikutusalueen tunnuksen perusteella. Aluetunnus on sama kuin yrityksen koodi, joka toimitetaan kontekstissa, jossa sähköisen raportoinnin (ER) muoto suoritetaan.

## <a name="syntax-1"></a>Syntaksi 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntaksi 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntaksi 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumentit

`number sequence code`: *Merkkijono*

Tekstiarvo, joka edustaa sen numerosarjan koodia, jossa uusi arvo vaaditaan.

`number sequence record ID`: *Int64*

*Int64*-arvo, joka vastaa NumberSequenceTable-taulun tietueen tunnusta, joka sisältää sen numerosarjan määritelmän, jossa uusi arvo vaaditaan.

`scope type`: *Enum-arvo*

**ERExpressionNumberSequenceScopeType**-luetteloinnin luettelointiarvo, joka määrittää sen numerosarjan laajuuden, jossa uusi arvo vaaditaan. Käytettävissä olevat aluetyypit ovat **Jaettu**, **Yritys**ja **Yhtiö**.

`scope ID`: *Merkkijono*

*Merkkijono*-arvo, joka määrittää vaikutusalueen määritetyn aluetyypin perusteella.

## <a name="return-values"></a>Palautusarvot

*merkkijono*

Tulokseksi saatava tekstiarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Määritä **Jaettu**-vaikutusalueen tyypille tyhjä merkkijono vaikutusalueen tunnuksena.

Määritä **Yhtiö**- ja **Yritys**-vaikutusalueen tyypin yhtiön koodi vaikutusalueen tunnuksena. Jos määrität tyhjän merkkijonon vaikutusalueen tunnukseksi näille vaikutusaluetyypeille, käytetään nykyistä yritystunnusta.

Kun käytetään syntaksia 1, numerosarjaa pyydetään **yrityksen** aluetyypille, ja yrityksen koodin toimittaa konteksti, jossa ER-muoto suoritetaan.

## <a name="example-1"></a>Esimerkki 1

ER-muodossa voit määrittää *käyttäjän syötteen parametri*-tyypin **AskNumSeq**-tietolähteen. Tämä tietolähde viittaa **kuvauksen** laajennettuun tietotyyppiin (EDT). Seuraavaksi määritetään **lasketun kenttätyypin** *numseq*-tietolähde. Tässä tietolähteessä on lauseke `NUMSEQVALUE (AskNumSeq)`. Kun **NumSeq**-tietolähdettä kutsutaan, se palauttaa suorituksen aikana määritetyn numerosarjan uuden luodun arvon syöttämällä sen koodin valintaikkunaan. Numerosarjaa pyydetään **yrityksen** vaikutusaluetyypille. Yrityksen koodin toimittaa konteksti, jossa ER-muoto suoritetaan.

## <a name="example-2"></a>Esimerkki 2

Seuraavat tietolähteet määritetään omassa mallimäärityksessäsi:

- *Taulu*-tyypin **LedgerParms**-tietolähde. Tämä tietolähde viittaa LedgerParameters-tauluun.
- *Laskettu kenttä* -tyypin **NumSeq**-tietolähde. Tässä tietolähteessä on lauseke `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun numerosarjan arvon. Tämä arvo määritettiin sen yrityksen kirjanpitoparametreissa, ja se antaa kontekstin, jossa ER-muoto suoritetaan. Tämä numerosarja yksilöi kirjauskansiot ja toimii tapahtumat yhteen liittävänä eränumerona.

## <a name="example-3"></a>Esimerkki 3

Seuraavat tietolähteet määritetään omassa mallimäärityksessäsi:

- Microsoft Dynamics 365 Financen *luettelointi*-tyypin **enumScope**-tietolähde. Tämä tietolähde viittaa **ERExpressionNumberSequenceScopeType**-luettelointiin.
- *Laskettu kenttä* -tyypin **NumSeq**-tietolähde. Tässä tietolähteessä on lauseke `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Kun **NumSeq**-tietolähde kutsutaan, se palauttaa juuri luodun **Gene\_1**-numerosarjan arvon. Tämä arvo määritettiin yritykselle, ja se antaa kontekstin, jossa ER-muoto suoritetaan.

## <a name="additional-resources"></a>Lisäresurssit

[Muut (liiketoiminnan toimialuekohtaiset) toiminnot](er-functions-category-other.md)
