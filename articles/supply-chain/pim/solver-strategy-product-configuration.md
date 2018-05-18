---
title: Tuotekonfiguraation Solver-strategia
description: "Tässä ohjeaiheessa käsitellään tuotekonfiguraation tehostamista Solver-strategian avulla."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4544128e580b30b14a6236a9a6147ff0a8641d72
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---

# <a name="solver-strategy-for-product-configuration"></a>Tuotekonfiguraation Solver-strategia

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tuotekonfiguraation tehostamista Solver-strategian avulla.

Solver-strategian käsite esiteltiin ensimmäisen kerran Microsoft Dynamics AX 2012 R2:n kumulatiivisessa päivityksessä 7 (CU7). Sitä laajennettiin Microsoft Dynamics AX 2012 R3:n kumulatiivisessa päivityksessä 8 (CU8) ja Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3:ssa.

Solver-strategian käsite sisältää nyt seuraavat strategiat:

- Oletusarvo
- Minimitoimialueet ensin
- Ylhäältä alas
- Z3

## <a name="solver-strategy"></a>Solver-strategia 

[Rajoitetyytyväisyysongelmana (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) muotoiltu tuotekonfigurointimalli. Microsoft Solver Foundationilla (MSF) on kahdenlaisia tuotekonfigurointimalleista käytettäviä Solver-strategioita CSP-ongelmien ratkaisemiseen. Nämä Solver-strategiat perustuvat [heuristiikkaan](https://techterms.com/definition/heuristic) ja niiden avulla määritetään järjestys, jossa CSP-ongelmien muuttujat käsitellään ongelmaa ratkaistaessa. Heuristiikkaa voi vaikuttaa suorituskykyyn huomattavasti ongelmaa tai ongelmaluokkaa ratkaistaessa.

Tuotekonfiguraatiomallien Solver-strategia määrittää Finance and Operationsissa, mitä selvitystä heuristiikan kanssa käytetään. **Oletus**-, **Minimitoimialueet ensin**- ja **Ylhäältä alas** -strategiat käyttävät kahta MSF:n selvitystä, kun taas**Z3**-strategia käyttää Z3-selvitystä. 

Todellisia asiakastoteutuksia koskevat tutkimukset ovat osoittaneet, että tuotekonfiguraatiomallin Solver-strategian vaihtaminen voi lyhentää vasteajan minuuteista millisekunteihin. Niinpä erilaisia Solver-strategioita kannattaa kokeilla, jotta tuotekonfiguraatiomallin kannalta tehokkain Solver-strategia löytyisi.

## <a name="change-the-settings-for-the-solver-strategy"></a>Solver-strategian asetusten muuttaminen

Voit vaihtaa Solver-strategian valitsemalla **Tuotekonfiguraation mallit** -sivun toimintoruudussa **Mallin ominaisuudet**. Valitse sitten **Muokkaa mallin tietoja** -valintaikkunassa Solver-strategia.

[![Solver-strategian vaihtaminen](./media/solver-strategy.png)](./media/solver-strategy.png)

Tällä hetkellä mikään logiikka ei tunnista automaattisesti, mikä on tehokkain poissulkevan tuotekonfiguraation Solver-strategia. Tämän vuoksi Solver-strategioita on kokeiltava yksi kerrallaan.

Seuraavassa taulukossa on suosituksia eri tilanteissa käytettävistä Solver-strategioista.

| Solver-strategia      | Strategian käyttöskenaario |
|----------------------|-----------------------------------|
| Oletusarvo              | **Oletus**-strategia on optimoitu selvittämään taulurajoitteisiin luottavia malleja. Asiakastoteutuksia koskevat tutkimukset ovat osoittaneet, että tämä strategia on tehokkain tilanteissa, joissa taulurajoitteita käytetään runsaasti. |
| Minimitoimialueet ensin | **Minimitoimialueet ensin**- ja **Ylhäältä alas** -strategiat liittyvät läheisesti toisiinsa. Asiakastoteutustutkimukset ovat osoittaneet, että CU8:ssa esitelty **Ylhäältä alas** -strategia toimii paremmin kuin **Minimitoimialueet ensin** -strategia. **Minimitoimialueet ensin** -strategia on kuitenkin säilytetty tuotteessa, jotta yhteensopivuus aikaisempien versioiden kanssa säilyy. Kummankin Solver-strategian on osoitettu selvittävän tehokkaasti malleja, joissa on useita aritmeettisia lausekkeita eikä taulurajoituksia käytetä. Joissakin tilanteissa **Oletus**-strategia on näitä kahta strategiaa tehokkaampi. Muista tämän vuoksi kokeile jokaista strategiaa. |
| Ylhäältä alas             | **Minimitoimialueet ensin**- ja **Ylhäältä alas** -strategiat liittyvät läheisesti toisiinsa. Asiakastoteutustutkimukset ovat osoittaneet, että CU8:ssa esitelty **Ylhäältä alas** -strategia toimii paremmin kuin **Minimitoimialueet ensin** -strategia. **Minimitoimialueet ensin** -strategia on kuitenkin säilytetty tuotteessa, jotta yhteensopivuus aikaisempien versioiden kanssa säilyy. Kummankin Solver-strategian on osoitettu selvittävän tehokkaasti malleja, joissa on useita aritmeettisia lausekkeita eikä taulurajoituksia käytetä. Joissakin tilanteissa **Oletus**-strategia on näitä kahta strategiaa tehokkaampi. Muista tämän vuoksi kokeile jokaista strategiaa. |
| Z3                   | **Z3**-strategian käyttö Solver-oletusstrategiana on suositeltavaa. Jos olet huolestunut suorituskyvystä ja skaalautuvuudesta, voit arvioida muut strategiat. |

## <a name="additional-resources"></a>Lisäresurssit

[Tuotekonfiguraatiomallin luominen](build-product-configuration-model.md)

[Heuristiikka](https://techterms.com/definition/heuristic)

[Rajoitustyytyväisyysongelma](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

