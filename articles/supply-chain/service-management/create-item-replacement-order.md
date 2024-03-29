---
title: Nimikkeen korvaavan tilauksen luominen
description: Nimikkeen korvaavat tilaukset luodaan yleensä tuotteen palautuksen ja tarkistuksen jälkeen.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14751fb0e0632ca986d6eddf55c93d44fbd68276
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015461"
---
# <a name="create-an-item-replacement-order"></a>Nimikkeen korvaavan tilauksen luominen 

[!include [banner](../includes/banner.md)]


Nimikkeen korvaavat tilaukset luodaan yleensä tuotteen palautuksen ja tarkistuksen jälkeen. Jos nimike kuitenkin on korvattava ennen sen palauttamista tai alkuperäistä nimikettä ei palauteta, voit luoda nimikkeen korvaavan tilauksen heti palautustilauksen luonnin jälkeen.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Korvaavan tilauksen luominen palautetun nimikkeen vastaanoton jälkeen

1.  Valitse **Myynti ja markkinointi** \> **Myyntipalautukset** \> **Kaikki palautustilaukset**.

2.  Luo uusi palautustilaus tai valitse palautettu tilaus luettelosta avataksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeen.

3.  Valitse **Palautusrivi**, ja valitse sitten **Korvaava nimike**.

4.  Valitse nimike, jolla palautettu nimike korvataan. Kirjoita nimikkeen tiedot ja valitse sitten **Käytä**.

5.  Voit luoda palautustilauksen pakkausluettelon napsauttamalla **Pakkausluettelo**. Valitsemallesi korvaavalle nimikkeelle luodaan myyntitilaus.
    
    Kun myyntitilaus on luotu korvaavalle nimikkeelle, järjestelmän myyntisopimuksista haetaan automaattisesti sopivaa myyntisopimusta ja jos tämä löytyy, sitä sovelletaan myyntitilaukseen.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Korvaavan tilauksen luonti ennen palautetun nimikkeen vastaanottamista

1.  Valitse **Myynti ja markkinointi** \> **Myyntipalautukset** \> **Kaikki palautustilaukset**.

2.  Luo uusi palautustilaus tai valitse palautustilaus luettelosta avataksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeen.

3.  Valitse **Etsi myyntitilaus** , jos haluat merkitä palautetun nimikkeen myyntitilauksen. Täytä **Etsi myyntitilaus** -lomake ja valitse **OK** sulkeaksesi lomakkeen ja palataksesi takaisin **Palautustilaus - palautusnumero: %1, %2** -lomakkeeseen. Palautetun nimikkeen myyntitilausrivi kopioidaan palautustilaukseen.

4.  Napsauta **Korvaava tilaus** avataksesi **Luo myyntitilaus** -lomakkeen.

5.  Valitse **Kopioi palautustilauksen rivit** -valintaruutu siirtääksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa valitsemasi palautustilauksen tiedot tähän myyntitilaukseen.

6.  Kirjoita tai muokkaa tiedot tarpeen mukaan.
    
    Jos tunnistit myyntitilauksen vaiheessa 3 ja jos palautetun nimikkeen myyntitilausrivi on yhdistetty myyntisopimukseen, nimikkeen korvaavan tilauksen soveltuvan myyntisopimuksen tunniste näkyy automaattisesti **Myyntisopimuksen tunnus** -kentässä.

7.  Napsauta **OK** sulkeaksesi **Luo myyntitilaus** -lomakkeen ja avataksesi **Myyntitilaus**-lomakkeen, jossa voit jatkaa uuden myyntitilauksen tietojen kirjoittamista. Kaikki sovellettavat palautustilauksen rivit kopioidaan uuteen myyntitilaukseen. 
    
    Jos myyntisopimuksen tunniste näytetään **Myyntitilauksen tunnus** -kentässä, tällöin myyntisopimus on yhdistetty myyntitilauksen otsikkoon nimikkeen korvaavalle tilaukselle. Jos myyntisopimuksessa on soveltuva sitoumus, jota ei ole vielä täytetty, ja myyntitilaus on luotu ennen myyntisopimuksen vanhenemista, myyntisopimusrivin ja myyntitilausrivin välille luodaan yhteys. Siksi myyntisopimuksen tiedot, kuten hinta, kopioidaan uudelle myyntitilausriville. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]