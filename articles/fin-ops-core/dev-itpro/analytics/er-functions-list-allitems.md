---
title: ALLITEMS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ALLITEMS-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 15ab88512e49b51dbefa19056c3e1846715dcadb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687765"
---
# <a name="allitems-er-function"></a>ALLITEMS ER-funktio

[!include [banner](../includes/banner.md)]

`ALLITEMS`-funktio suoritetaan muistissa olevan valinnan mukaan ja se palauttaa uuden litistetty *Tietueluettelo*-arvon tietueluettelona, joka edustaa kaikkia määritettyä polkua vastaavia kohteita.

## <a name="syntax"></a>Syntaksi

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumentit

`path`: *Tietueluettelo*

*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.

## <a name="return-values"></a>Palautusarvot

*Tietueluettelo*

Tuloksena oleva tietueluettelo.

## <a name="usage-notes"></a>Käyttöhuomautukset

Polku on määritettävä sallituksi tietolähteen poluksi *Tietueluettelo*-tietotyypin tietolähteen elementtiin. Tietoelementit, kuten polun merkkijono ja päivämäärä, käynnistävät virheen sähköisen raportoinnin (ER) lausekkeenmuodostimessa suunnitteluaikana.

Tätä funktiota ei suositella käytettäväksi tapahtumatietolähteissä, jotka saattavat sisältää suuren määrän tietoja. Harkitse sen sijaan [ALLTEMSQUERY](er-functions-list-allitemsquery.md) -funktion käyttämistä.

## <a name="example-1"></a>Esimerkki 1

Jos syötät `SPLIT("abcdef" , 2)` tietolähteeksi **DS**, lauseke `COUNT( ALLITEMS (DS))` palauttaa arvon **3**.

## <a name="example-2"></a>Esimerkki 2

Jos syötät **Vend** *Tietueluettelon* tietotyypin tietolähteeksi, joka viittaa VendTable-sovellus tauluun, lauseke `ALLITEMS (Vend.'<Relations'.ContactPerson)` palauttaa litistetyn tietueluettelon, jossa on **ContactPerson**-taulukon rakenne ja joka sisältää kaikki yhteyshenkilöt, joita voi käyttää **ContactPerson.ContactForParty == VendTable.Party**-relaatio, ja joka on käytettävissä kaikille toimittajille viitatun toimittajan taulukosta.

## <a name="additional-resources"></a>Lisäresurssit

[Luettelotoiminnot](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]