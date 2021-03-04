---
title: Materiaalipoikkeusten näkyvyys
description: Tässä aiheessa käsitellään tuotantotilausten ja erätilausten materiaalipoikkeusten näkyvyyden parantamista.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, WHSProdWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 0c17997d9dd04559fb7022fe39bb2b961c1cfc4a
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427420"
---
# <a name="visibility-into-material-exceptions"></a>Materiaalipoikkeusten näkyvyys

[!include [banner](../includes/banner.md)]

**Tuotannon hallinta** -työtilassa on kolme ruutua, jotka parantavat tuotanto- ja erätilausten materiaalipoikkeusten näkyvyyttä:

- Vapauttamattomat materiaalirivit, jotka vaativat huomiota
- Käsittelemättömät aallot, jotka vaativat huomiota
- Avoin varastotyö, joka vaatii huomiota

Kaikissa kolmessa ruudussa tuotantorakenne- ja reseptirivien raaka-ainepäivämäärää verrataan sekä työtilan päivämäärään että **Tuotantoyksikkö**-, **Resurssiryhmä**- ja **Resurssi**-suodattimiin. Nämä suodattimet määritetään **Määritä oma työtila** -valikossa. Työtilan päivämäärä on oletusarvoisesti kuluva päivä, mutta sitä voi muuttaa.

Vapauttamaton tuoterakenne- tai reseptirivi on otettava huomioon, jos rivin raaka-ainepäivämäärä on sama tai aiempi kuin työtilan päivämäärä ja jos se vastaa työtilan suodattimien määrittämiä ehtoja.

Seuraavassa kuvassa sininen palkki vastaa tuotantotyötä, joka on aikataulutettu resurssissa. Työ on ajoitettu alkamaan 1. toukokuuta 2019 (1.5.2017). Tämä päivämäärä raaka-aineen päivämäärä. Toisin sanoen työlle tuoterakenne- tai reseptirivillä määritettyjen materiaalien on oltava valmiina kyseisenä päivänä. Kuvan toinen päivämäärä, 6. toukokuuta (5.6.2017) vastaa työtilan päivämäärää. Tässä esimerkissä raaka-aineen päivämäärä on aiempi kuin työtilan päivämäärä. Näin ollen päivämäärä, jolloin raaka-aineen kulutuksen oli tarkoitus alkaa, on ohitettu ja tuoterakenne- ja reseptirivit vastaavat huomion vaatimisen ehtoja.

![Esimerkki tuotantotyöstä, jossa raaka-aineen päivämäärä on aiempi kuin työtilan päivämäärä](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Vapauttamattomat materiaalirivit, jotka vaativat huomiota

Tuoterakenne- tai reseptirivi voidaan vapauttaa varastoon kolmella tavalla:

- Tuotanto- tai erätilauksen vapautuksen osana
- Manuaalisena vapautuksena
- Automaattisesti erätyön kautta

Lisätietoja on kohdassa [Tuoterakenne- ja reseptirivien vapauttaminen varastoon](releasing-bom-and-formula-lines-to-warehouse.md). 

Jos tuoterakenne- tai reseptiriviä ei ole vapautettu tai se on vapautettu vain osittain ja jos työtilan päivämäärä- ja suodatusehdot täyttyvät, rivi sisältyy **Vapauttamattomat materiaalirivit, jotka vaativat huomiota** -ruudussa näkyvän luvun laskentaan.

Kun valitse ruudun, **Vapauta varastoon** -sivu avautuu. Tällä sivulla näkyy vapauttamattomien tuoterakenne- ja reseptirivien määrä, jonka ruudussa näkyvä numero osoittaa. Vapauttamattomat rivit näkyvät yläruudukossa. Tämä ruudukossa näkyy riville alun perin arvioitu määrä, jo vapautettu määrä ja vielä vapautettava jäljellä oleva määrä. Voit lisätä rivejä yläruudukosta alaruudukkoon. Voit sitten vapauttaa valitut rivit alaruudukosta varastoon. Voit myös säätää alaruudukossa vapauttavien määrää siten, että määrästä vapautetaan vain osa.

## <a name="unprocessed-waves-needing-attention"></a>Käsittelemättömät aallot, jotka vaativat huomiota

Kun tuoterakenne- tai reseptirivi vapautetaan, se lisätään joko uuteen tuotantoaaltoon tai aiemmin luotuun avoimeen aaltoon tuotantoaaltomallin määritysten mukaan. Voit määrittää aaltomallin määrityksissä aallon myös siten, että se käsitellään automaattisesti, kun tuoterakenne- tai reseptirivi vapautetaan. Kun aalto käsitellään, raaka-aineen keräilylle luodaan varastotyö. Jos aaltomalli on määritetty siten, että aaltoja ei käsitellä vapautuksen yhteydessä, aalto jää käsittelemättömään tilaan. **Käsittelemättömät aallot, jotka vaativat huomiota** -ruudussa on näkyvissä tuoterakenne- ja reseptirivit, jotka on vapautettu varastoon käsittelemättöminä aaltoina ja joiden raaka-aineen päivämäärä on sama tai aiempi kuin työtilan päivämäärä. Lisäksi sen toimintoresurssin on kulutettava rivit, joka käyttää työtilan suodatinta.

Kun ruutu on valittu, kun **Kaikki tuotantoaallot** -sivu avautuu. Tämä sivu suodatetaan niiden avoimien aaltojen määrällä, joissa on ruudun ehdot täyttäviä vapautettujen tuoterakenne- ja kaavarivien aaltorivejä. Voit käsitellä aallon manuaalisesti **Kaikki tuotantoaallot** -sivulla.

## <a name="open-warehouse-work-needing-attention"></a>Avoin varastotyö, joka vaatii huomiota

**Avoin varastotyö, joka vaatii huomiota** -ruudussa on näkyvissä tuoterakenne- ja reseptirivit, jotka on vapautettu varastoon käsittelemättömänä työnä ja joiden raaka-aineen päivämäärä on sama tai aiempi kuin työtilan päivämäärä. Lisäksi sen toimintoresurssin on kulutettava rivit, joka käyttää työtilan suodatinta.

Kun ruutu on valittu, kun **Kaikki työ** -sivu avautuu. Tämä sivu suodatetaan niiden avoimien työn otsikoiden määrällä, joissa on ruudun ehdot täyttäviä vapautettujen tuoterakenne- ja kaavarivien työrivejä. Voit käsitellä työn manuaalisesti **Kaikki työ** -sivulla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]