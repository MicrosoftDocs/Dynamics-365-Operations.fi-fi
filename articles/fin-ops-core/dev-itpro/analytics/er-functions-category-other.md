---
title: Luettelo ER-funktioista liiketoiminta-aluekohtaisessa luokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista liiketoiminta-aluekohtaisista funktioista.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3d2055be7a755e35d0e88230e19038cf2d02ccc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748012"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Luettelo ER-funktioista liiketoiminta-aluekohtaisessa luokassa

[!include [banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) toimialuekohtaisia funktioita voidaan käyttää suorittamaan laskutoimituksia ja tietojenkäyttöpyyntöjä, jotka koskevat Microsoft Dynamics 365 Financen toteutusta. Tässä aiheessa on yhteenveto näistä funktioista.

## <a name="list-of-supported-functions"></a>Luettelo tuetuista toiminnoista

| Toiminto| Kuvaus |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Tämä funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta MOD10-lausekkeena määritetyn laskunumeron numeroiden perusteella. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Tämä funktio palauttaa *merkkijono*-arvon, joka edustaa yksittäistä taloushallinnon dimension tunnusta, joka on otettu määritetystä merkkijonosta. Määrätty merkkijono näyttää kaikki ulottuvuudet pilkulla erotettuna tunnusten luettelona. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Tämä funktio palauttaa *todellisen* arvon, joka edustaa tulosta muuntamalla määritetty rahasumma määritetystä lähdevaluutasta määritettyyn kohdevaluuttaan käyttämällä määritetyn yrityksen asetuksia tiettynä päivänä. |
| [CurCredRef](er-functions-other-curcredref.md) | Tämä funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta määritetyn laskunumeron numeroiden perusteella. |
| [FA_Balance](er-functions-other-fabalance.md) | Tämä funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu määritetyn käyttöomaisuuserän, arvomallin koodin, raportointivuoden ja raportointipäivämäärän käyttöomaisuussaldon tiedoista. |
| [FA_Sum](er-functions-other-fasum.md) | Tämä funktio palauttaa *Säilö (tietue)*-arvon, joka koostuu tietyn käyttöomaisuushyödykkeen kiinteän omaisuuden määrien tiedoista, arvomallikoodista ja päivämääräajanjaksosta. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Tämä funktio palauttaa *Merkkijono*-arvon siltä yritykseltä, johon käyttäjä on tällä hetkellä kirjautunut. |
| [ISOCredRef](er-functions-other-isocredref.md) | Tämä funktio palauttaa *Merkkijono*-arvon, joka edustaa laskuttajan ISO (International Organization for Standardization) -viitettä määritetyn laskunumeron lukujen ja kirjainmerkkien perusteella. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Tämä funktio palauttaa *totuusarvon* **TOSI**, jos määritetty merkkijono vastaa kelvollista kansainvälistä tilinumeroa (IBAN). Muussa tapauksessa se palauttaa *totuusarvon* **EPÄTOSI**. |
| [Mod_97](er-functions-other-mod97.md) | Tämä funktio palauttaa *merkkijono*-arvon, joka vastaa velkojan viittausta MOD97-lausekkeena määritetyn laskunumeron numeroiden perusteella. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Tämä funktio palauttaa *merkkijono*-arvon, joka edustaa numerosarjan uutta luotua arvoa määritetyn numerosarjan, laajuuden ja vaikutusalueen tunnuksen perusteella. Aluetunnus on sama kuin yrityksen koodi, joka toimitetaan kontekstissa, jossa ER-muoto suoritetaan. |
| [RoundAmount](er-functions-other-roundamount.md) | Tämä funktio palauttaa *todellisen* arvon, joka edustaa tulosta pyöristettynä määritetty luku tietyn desimaalin tarkkuudella määritetyn pyöristyssäännön mukaisesti. |
| [TableName2ID](er-functions-other-tablename2id.md) | Tämä funktio palauttaa määritetyn taulukon nimen numeerisen esityksen taulukon tunnukselle *kokonaisluku*-arvona. |

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin kaavakieli](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]