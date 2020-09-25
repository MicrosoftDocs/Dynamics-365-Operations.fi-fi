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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745390"
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
