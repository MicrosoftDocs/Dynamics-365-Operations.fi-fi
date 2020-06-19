---
title: Varastoasetusten käyttäminen
description: Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fc81c190806a0bdb50569f526589cfa1808ce0c
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417435"
---
# <a name="apply-inventory-settings"></a>Varastoasetusten käyttäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.

## <a name="overview"></a>Yleiskuvaus

Varastoasetukset määrittävät, tuleeko varasto tarkistaa, ennen kuin tuotteet lisätään kärryyn. Ne määrittävät myös varastoon liittyvät myynninedistämispalkkiosanomat, kuten "varastossa" ja "vain muutama jäljellä". Nämä asetukset varmistavat, että tuotetta ei voi ostaa, jos sitä ei ole varastossa.

Dynamics 365 Commerce sisältää arviot tuotteiden käytettävissä olevasta saatavuudesta. Lisätietoja arvioidun käytettävissä olevan käytettävyyden laskemisesta on kohdassa [Jälleenmyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).

Commercen sivustotyökalussa voidaan määrittää tuotteen tai luokan varastorajat ja -alueet. Ne määräävät, voidaanko varaston arvoksi luokitella varastossa, vähissä vai loppunut. Katso lisätietoja kohdasta [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

## <a name="inventory-settings"></a>Varastoasetukset

Commercessa varastoasetukset määritetään sivustotyökalussa kohdassa **Sivuston asetukset \> Laajennukset \> Varaston hallinta**. Varastoasetuksia on neljä, joista yksi on poistettu käytöstä (vanhentunut):

- **Ota käyttöön varastotarkistus sovelluksessa** – Tämä asetus ottaa tuotevaraston tarkistuksen pois käytöstä. Osta-ruutu, ostoskori ja nouto myymälästä -moduulit tarkistavat tuotevaraston ja sallivat tuotteen lisäämisen ostoskoriin vain, jos varasto on käytettävissä.
- **Varastotaso perustuu** – Tämä asetus määrittää, miten varastotasot lasketaan. Käytettävissä olevat arvot ovat **Käytettävissä olevat yhteensä**, **Fyysisesti käytettävissä olevat** ja **Loppu varastosta**. Commercessa varaston kynnysarvo ja alueet voidaan määritellä jokaiselle tuotteelle ja luokalle. Varasto-APIt palauttavat tuotevarastotiedot sekä **käytettävissä olevan kokonaismäärän** että **fyysisen käytettävissä olevan** ominaisuuden osalta. Jälleenmyyjä päättää, käytetäänkö **Käytettävissä olevaa** tai **Fyysisesti käytettävissä olevaa** arvoa varaston inventoinnin ja varasto- ja loppuvarastotilojen vastaavien alueiden määrittämiseen.

    **Loppunut varastosta** -arvo **Varastotason varaston kynnys arvo** asetuksen perusteella on vanha (aiempi), vanhentunut arvo. Kun se on valittu, varaston inventoinnit määräytyvät **Käytettävissä olevan** kokonaisarvon perusteella, mutta kynnys määritetään myöhemmin annetun luvun **Loppu varastosta** -arvon mukaan. Tämä raja-asetus koskee kaikkia tuotteita, jotka ovat verkkokauppasivustossa. Jos varasto on raja-arvon alapuolella, tuotetta ei pidetä varastossa. Muussa tapauksessa sitä pidetään varastossa. **Loppu varastosta** -arvo on rajallinen, emmekä suosittele sen käyttämistä versiossa 10.0.12 ja sitä uudemmissa.

- **Varastoalueet** – Tämä asetus määrittää, mitkä varastoalueet, joille sanoma näytetään sivustomoduuleissa. Sitä voi käyttää vain, jos **Käytettävissä oleva kokonaisarvo** tai **Käytettävissä oleva fyysinen** arvo on valittu **Varastotaso perusteella** -asetukselle. Käytettävissä olevat arvot ovat **Kaikki**, **Alhaiset ja loppunut varastosta** ja **Loppunut varastosta**.

    - Kun **Kaikki** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta varastossa ("käytettävissä" oleva sanoma) kohteeseen loppunut varastosta ("loppunut varastosta").
    - Kun **Vähissä ja loppunut varastosta** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta paitsi varastossa ("käytettävissä" oleva sanoma).
    - Kun **Loppunut varastosta** on valittu, vain "loppunut varastosta" -sanoma tulee näkyviin.

- **Loppunut varastosta** – Tämä vanha numeerinen asetus tulee voimaan vain, jos **Loppunut varastosta** arvoksi on valittu **Varaston vähimmäisarvo** -asetuksen perusteella.

## <a name="modules-that-use-inventory-settings"></a>Varastoasetuksia käyttävät moduulit

Ostolaatikko, toivelista, myymälänvalitsin, ostoskori ja ostoskorin kuvakemoduulit käyttävät varastoasetuksia näyttämään varastoalueet ja sanomat.

Seuraavassa kuvassa on esimerkki tuotetietosivusta (PDP), jossa näkyy varastossa oleva ("käytettävissä oleva") sanoma.

![Esimerkki PDP-moduulista, jossa on varastossa oleva sanoma](./media/pdp-InStock.png)

Seuraavassa kuvassa on esimerkki PDP:stä, jossa näkyy Loppunut varastosta -sanoma.

![Esimerkki PDP-moduulista, jossa on loppunut varastosta -sanoma](./media/pdp-outofstock.png)

Seuraavassa kuvassa on esimerkki ostoskorista, jossa näkyy Varastossa (Käytettävissä) -sanoma.

![Esimerkki ostoskorimoduulista, jossa on varastossa oleva sanoma](./media/cart-instock.png)

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tilin hallintasivut ja -moduulit](account-management.md)

[Myymälän valitsinmoduuli](store-selector.md)
