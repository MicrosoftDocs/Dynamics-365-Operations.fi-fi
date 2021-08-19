---
title: Kuormitusriviä ei voi päivittää, koska julkaistu määrä on negatiivinen
description: Tämä ongelma ilmenee, kun kuormitusrivin päivittäminen tai poistaminen aiheuttaa negatiivisen julkaistun määrän.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728456"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Kuormitusriviä ei voi päivittää, koska julkaistu määrä on negatiivinen

Virhekoodi: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun kuormitusrivin päivittäminen tai poistaminen aiheuttaa negatiivisen julkaistun määrän. Tässä tapauksessa järjestelmä näyttää seuraavan virhesanoman, kun yrität päivittää tai poistaa kuormariviä:

> Vapautettu määrä ei voi olla negatiivinen nimikkeelle %1, erä %2.

Siksi kuormariviä ei voi päivittää tai poistaa.

## <a name="cause"></a>Syy

Kun olet päivittänyt tai poistanut kuormarivin, järjestelmä päivittää liittyvän myyntirivin julkaistun määrän (*whsSalesLine.ReleaseQty*). Järjestelmä arvioi julkaistun määrän, ja jos järjestelmä havaitsee, että rivin julkaistu määrä on päivityksen jälkeen negatiivinen, riviä ei päivitetä eikä poisteta. Tämä oikeellisuustarkistus tehdään, kun kuormitusrivin määrää tai mittayksikköä yritetään päivittää erilaisilla toimenpiteellä, kuten kuormarivin poistaminen, lähetyksen poistaminen, kuormitusrivin määrän muuttaminen, kerätyn määrän pienentäminen ja lyhyt keräily.

Yleisin tämän ongelman syy on avointen kuormarivien yksikkömuunnoksen muutos. Esimerkiksi yksikkömuunnos myyntitilauksen vapautettaessa oli *50 Ea = 1 PL*. Ennen liittyvän kuormalähetyksen viimeistelyä yksikön muuntaminen muutettiin muotoon *100 Ea = 1 PL*.

## <a name="resolution"></a>Ratkaisu

Ongelmana on palauttaa yksikkömuunnosmuutokset, päivittää tai poistaa kuormitusrivi ja ottaa muunto uudelleen käyttöön. Sinun on estettävä muut kuormitukset, jotka sisältävät sen nimikkeen, joka on aiheuttanut ongelman käsittelemisen, ennen kuin ongelma on korjattu. Muussa tapauksessa uusia muunnoksia voidaan käyttää muissa jo avoinna olevissa kuormissa.

Voit korjata ongelman tekemällä seuraavat toimet:

1. Tarkista kuormarivillä käytetty yksikkömuunnos.
2. Tarkista nimikkeen nykyinen yksikkömuunnos ja tee korjaukset, joiden avulla kuormariviä voi päivittää tai poistaa.
3. Päivitä tai poista kuormitusrivi ja palauta yksikkömuunnosoikaisut.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Tarkista kuormarivillä käytetty yksikkömuunnos

Seuraavia ohjeita noudattamalla voit tarkistaa kuormarivit ja tehdä huomautuksen kuormarivillä käytetystä yksikkömuunnoksesta.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, joka sisältää kuormarivin, jota ei voi poistaa tai päivittää.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Valitse ylemmästä ruudukosta työtunnus.
1. Laske sivun alaosan **Yleiset**-välilehdessä **varaston työmäärän** arvon ja **työmäärän** arvon välinen muuntokerroin. Kirjoita korko muistiin.
1. Toista nämä vaiheet kaikille asiaankuuluville työtunnuksille, jotta voit varmistaa, että samaa muunnosta on käytetty.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Tarkista nimikkeen nykyinen yksikkömuunnos ja tee tarvittavat muutokset

Tarkista tuotteen yksikkömuunnos seuraavalla tavalla ja tee tarvittavat muutokset varmistaaksesi, että yksikkömuunnos on linjassa kuormituslinjan kanssa.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa liittyvä tuote mennäksesi sen **Julkaistun tuotteen tiedot** -sivulle.
1. Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Yksikkömuunnokset**.
1. Valitse yksikköjen välinen muunnos ja tee muutokset käyttämällä edellisessä osassa löytämääsi muunnosta.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Päivitä tai poista kuormitusrivi ja palauta yksikkömuunnosoikaisut

Seuraavia ohjeita noudattamalla voit käsitellä kuormarivin tarpeen mukaan ja palauttaa yksikkömuunnokset.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Avaa kuorma, joka sisältää kuormarivin, jota ei voi poistaa tai päivittää.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Jatka tarvittaessa tarvittavia toimenpiteitä. (Poista esimerkiksi kuormarivi tai muuta sen määrää.)
1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa liittyvä tuote mennäksesi sen **Julkaistun tuotteen tiedot** -sivulle.
1. Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Yksikkömuunnokset**.
1. Valitse yksikköjen välinen muunnos ja peru muutokset, jotka teit edellisessä osassa.
