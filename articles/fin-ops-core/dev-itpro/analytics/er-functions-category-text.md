---
title: Luettelo tekstiluokan ER-funktioista
description: Tässä artikkelissa on tietoja sähköisen raportoinnin (ER) tukemista tekstifunktioista.
author: kfend
ms.date: 02/28/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e4c7885024586034c062304cce21a25e5b6c8c9b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268790"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Luettelo tekstiluokan ER-funktioista

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) tekstifunktioiden avulla voidaan suorittaa toimintoja *Merkkijono*-tietotyypin tietolähteille. Tässä artikkelissa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto | Kuvaus |
|----------|-------------|
| [Char](er-functions-text-char.md) | Tämä funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla. |
| [Liitä](er-functions-text-concatenate.md) | Tämä funktio palauttaa kaikki määritetyt tekstimerkkijonot *Merkkijono*-arvona sen jälkeen, kun ne on liitetty yhdeksi merkkijonoksi. |
| [Muoto](er-functions-text-format.md) | Tämä funktio palauttaa määritetyn *Merkkijono*-arvon sen jälkeen, kun se on muotoiltu korvaamalla kaikki **%N**-esiintymät *N*:llä argumentilla. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Tämä funktio etsii määritetystä luettelointitietolähteestä tiettyä *Enum*-arvoa käyttämällä *merkkijono*-arvona määritettyä luetteloinnin nimeä. Jos *Enum*-arvo löytyy, funktio palauttaa sen. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Tämä toiminto etsii tiettyä otsikkoa ja palauttaa *[merkkijono](er-formula-supported-data-types-primitive.md#string)* arvon, joka edustaa määritetyn otsikon käännöstä määritetyllä kielellä. |
| [GuidValue](er-functions-text-guidvalue.md) | Tämä funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *GUID*-tyypin tietokohteeksi. |
| [JsonValue](er-functions-text-jsonvalue.md) | Tämä funktio jäsentää tiedot JavaScript Object Notation (JSON) -muodossa, jota käytettään tietyssä polussa, ja se purkaa skalaariarvon, joka perustuu tiettyyn tunnukseen. Sen jälkeen se palauttaa puretut skalaariarvot *merkkijono*-arvona. |
| [Vasemmalle](er-functions-text-left.md) | Tämä funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon alusta. |
| [Len](er-functions-text-len.md) | Tämä funktio palauttaa määritetystä luettelosta *Kokonaisluku*-arvon, joka esittää merkkien määrän määritetyssä merkkijonossa. |
| [Alempi](er-functions-text-lower.md) | Tämä funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu pieniksi kirjaimiksi. |
| [Keskimmäinen](er-functions-text-mid.md) | Tämä funktio palauttaa määritetystä luettelosta *[Merkkijono](er-formula-supported-data-types-primitive.md#string)*-arvon, joka esittää määritetyn määrän merkkejä määrätystä merkkijonosta, alkaen määritellystä kohdasta. |
| [NewGUID](er-functions-text-newguid.md) | Tämä toiminto palauttaa juuri luodun *[GUID](er-formula-supported-data-types-primitive.md#guid)*-arvon. |
| [NumberFormat](er-functions-text-numberformat.md) | Tämä funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Tämä funktio palauttaa määritetyn numeron *Merkkijono*-arvona sen jälkeen, kun se on kirjoitettu (muunnetaan tekstimerkkijonoiksi) määritetyllä kielellä. |
| [PadLeft](er-functions-text-padleft.md) | Tämä funktio palauttaa määritetyn pituisen *merkkijonon*, jossa määritetyn merkkijonon alkuun lisätään yksi tai useampi määriteltyjen merkkien esiintymä. |
| [QrCode](er-functions-text-qrcode.md) | Tämä funktio palauttaa *Säilön* arvon, joka esittää määritetyn merkkijonon nopean vastauskoodin (QR Code) binaarimuodossa. |
| [Korvaa](er-functions-text-replace.md) | Tämä funktio palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun se kokonaan tai osa siitä on korvattu toisella merkkijonolla. |
| [Oikealle](er-functions-text-right.md) | Tämä funktio palauttaa määritetystä luettelosta *merkkijono*-arvon, joka esittää määritetyn määrän merkkejä määritetyn merkkijonon lopusta. |
| [Teksti](er-functions-text-text.md) | Tämä funktio palauttaa määritetyn *merkkijono*-arvon sen jälkeen, kun se on muunnettu tekstimerkkijonoksi, joka on alustettu nykyisen sovellusesiintymän palvelimen sijaintiasetusten mukaisesti. |
| [Käännä](er-functions-text-translate.md) | Tämä funktio palauttaa *Merkkijonon* arvon, joka sisältää korvaavan määritetyn tekstin merkkeinä toisen annetun merkkijoukon merkeissä. |
| [Trim](er-functions-text-trim.md) | Tämä toiminto palauttaa määritetyn tekstimerkkijonon *merkkijonona*, kun sarkain-, rivinvaihto-, rivisyöte- ja lomakesyötemerkit on korvattu yhdellä välilyönnillä, kun alun ja lopun välilyönnit on lyhennetty ja kun sanojen välistä on poistettu useat välilyönnit. |
| [Upper](er-functions-text-upper.md) | Tämä funktio palauttaa määritetyn tekstimerkkijonon *Merkkijono*-arvona sen jälkeen, kun se on muunnettu isoiksi kirjaimiksi. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
