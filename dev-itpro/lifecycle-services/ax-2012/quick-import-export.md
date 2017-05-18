---
title: "Pikatuonnin tai -viennin käyttäminen"
description: "Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 2012 R3 CU8
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f35e7b7d987d6caa19a32460259f07322f2b85cb
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a>Test Data Transfer Tool (beta-versio) -sovelluksen ajaminen Dynamics AX:ssä (AX 2012)

[!include[banner](../../includes/banner.md)]


Pikatuonti- ja vientitoiminnon tarkoitus on vähentää tuonti- ja vientivaiheita.

Pikatuonti- ja vientiomaisuus on lisätty, jotta käyttäjät voivat tuoda tai viedä yksinkertaisia, nopeasti suoritettavia töitä. Ihannetapauksessa tätä ominaisuutta käytetään skenaarioissa, joissa tiedosto yhdistetään automaattisesti järjestelmään eikä käyttäjän tarvitse käyttää yhdistämisen lisäasetuksia tai luoda toistuvia tuonti- tai vientitöitä.

-   Tämä ominaisuus tukee sekä käyttövalmiita että mukautettuja yksikköjä.
-   Tuonti on mahdollista tiedostoista tai, jos käytät ODBC-tietolähdettä, voi määrittää tuonnin valitsemalla kyselyn.
-   Sinulla on oltava aiemmin määritetyt AX- tai tiedostomuotoiset lähdetietomuodot ja sinun on tiedettävä niiden sijainti.
-   Pikatuontia tai -vientiä varten ei tarvitse luoda käsittelyryhmää, sillä järjestelmä luo sen automaattisesti tuonti- tai vientityön suorittamisen yhteydessä. Voit myös säilyttää halutessasi pikatuonnilla- tai viennillä tuotujen tietojen historiatiedot.

  Huomaa, että pikatuonti- ja vientitoiminto olettaa, että tunnet DIXF-käsitteet.




