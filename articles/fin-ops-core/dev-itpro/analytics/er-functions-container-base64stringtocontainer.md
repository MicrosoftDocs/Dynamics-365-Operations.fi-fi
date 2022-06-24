---
title: Base64StringToContainer-ER-funktio
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) Base64StringToContainer-funktion käyttöä.
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bcbbead1155a7270a329c23055340492c73cdfda
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879917"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer-ER-funktio

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER`-[funktio](er-formula-language.md#Functions) muuntaa *Merkkijono*-tyypin määritetyn syötteen *[Säilö](er-functions-category-container.md)*-tyypin tietokohteeksi.

## <a name="syntax"></a>Syntaksi

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumentit

`input`: *Merkkijono*

*Merkkijono*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Säilö*

Näin tulokseksi saadaan BLOB-muotoinen binaariarvo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Parametri ei kelpaa -poikkeus annetaan, jos syöttömerkkijono ei sisällä oikeaa binaarin tekstiin koodaamisrakenteiden Base64-ryhmää.

## <a name="example"></a>Esimerkki

Määritä seuraavat tietolähteet omassa mallimäärityksessäsi:

- **DocuTypeGroup**-sovellusluettelointiin viittaava *Dynamics 365 for Operations / Luettelointi* -tyypin **DocuTypeGroupEnum**-juuritietolähde.
- **CustTable**-sovellustauluun viittaava *Dynamics 365 for Operations / Taulutietueet* -tyypin **Asiakas**-juuritietolähde
- Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#Media**-tietolähde:

    - Se lisätään **Asiakas**-tietolähteen alitietolähteenä.
    - Se sisältää lausekkeen `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#MediaAsBase64String**-tietolähde:

    - Se lisätään **Asiakas.\#Media**-tietolähteen alitietolähteenä.
    - Se sisältää lausekkeen `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Seuraavalla tavalla määritetyn *Laskettu kenttä* -tyypin **\#BlobFomBase64**-tietolähde:

    - Se lisätään **Asiakas.\#Media**-tietolähteen alitietolähteenä.
    - Se sisältää lausekkeen `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

Tässä esimerkissä **\#MediaAsBase64String**-tietolähde koodaa nykyisen medialiitteen binaarisisällön tekstinä, joka ilmaisee binaarin tekstiin koodaamisrakenteiden Base64-ryhmän. **\#BlobFomBase64**-tietolähde purkaa Base64-merkkijonon koodauksen ja palauttaa BLOB-muotoisen binaariarvon.

![ER-mallin yhdistämismäärityksen suunnitteluohjelman sivun näytetietolähde.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Lisäresurssit

[Säilöfunktiot](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
