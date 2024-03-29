---
title: Vanhentuneiden tuotevarianttien etsiminen
description: Tässä menettelyssä kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13db6620575b4c97b3f8079ac94f5231a2fd9c1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577237"
---
# <a name="find-obsolete-product-variants"></a>Vanhentuneiden tuotevarianttien etsiminen 

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten vanhentuneita julkaistuja tuotteita tai tuotevariantteja etsitään ja miten tuotteen elinkaaren tila liitetään vanhentuneisiin tuotteisiin. Edellytys: Sinun on määritettävä vähintään yksi tuotteen elinkaaren tila, joka ei ole aktiivinen suunnittelua varten, ennen kuin voit toistaa tämän tehtäväoppaan.


## <a name="run-a-simulation"></a>Simuloinnin suorittaminen
1. Valitse Tuotetietojen hallinta > Kausittaiset tehtävät > Muuta vanhentuneiden tuotteiden elinkaaren tilaa.
2. Syötä tai valitse arvo Uusi tuotteen elinkaaren tila -kenttään.
3. Valitse Kyllä Suorita simulaatio päivittämättä tuotetietoja -kenttään.
4. Syötä Jätä pois tätä päivien määrää uudemmat tuotteet -kenttään numero.
5. Syötä Jätä pois tuotteet, joita on käytetty tapahtumissa (päivien määrän kuluessa) -kenttään numero.
6. Laajenna Tietueet-kohta ja sisällytä osaan.
7. Valitse Suodatin.
8. Merkitse valittu rivi luettelossa.
9. Kirjoita arvo Ehdot-kenttään.
10. Valitse OK.
11. Valitse OK.

> [!NOTE]
> Simulointi kannattaa suorittaa eräajona, jos haku tehdään suuresta tuotemäärästä. Varmista myös, että simulointia ei suoriteta yrityksen aktiivisena työaikana.  

## <a name="review-the-simulation-results"></a>Simuloinnin tulosten tarkistaminen
1. Valitse Tuotetietojen hallinta > Kyselyt ja raportit > Tuotteen elinkaaren tilan historia.
   
> [!NOTE]
> Tällä sivulla voit tarkastella simulointituloksia ja arvioida, miten useita tuotteita ja tuotevariantteja liitetään uuteen tuotteen elinkaaren tilaan, kun päivitys suoritetaan ilman simulointia.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Tuotteen elinkaaren tilan päivityksen suorittaminen vanhentuneille tuotteille
1. Sulje sivu.
2. Valitse Tuotetietojen hallinta > Kausittaiset tehtävät > Muuta vanhentuneiden tuotteiden elinkaaren tilaa.
3. Laajenna Tietueet-kohta ja sisällytä osaan.

> [!NOTE]
> Huomaa, että edellinen valinta on tallennettu.  

4. Valitse Ei Suorita simulaatio päivittämättä tuotetietoja -kenttään.
5. Laajenna Suorita taustalla -osa.

> [!NOTE]
> Tämä työ kannattaa ehkä suorittaa eräajona, jos tuotteita ja tuotevariantteja on paljon. Varmista, että et suorita suurta päivitystyötä yrityksen aktiivisimpana työaikana.  

6. Valitse OK.
7. Valitse Tuotetietojen hallinta > Kyselyt ja raportit > Tuotteen elinkaaren tilan historia.

> [!NOTE]
> Tarkista muutetut julkaistut tuotteet ja tuotevariantit.  

8. Etsi haluamasi tietue luettelosta ja valitse se.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]