---
title: Varastoasetusten käyttäminen
description: Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ae0195f63b123a345b0cdcd4976bfd25b3b3d6d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019075"
---
# <a name="apply-inventory-settings"></a>Varastoasetusten käyttäminen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.

Varastoasetukset määrittävät, tuleeko varasto tarkistaa, ennen kuin tuotteet lisätään kärryyn. Ne määrittävät myös varastoon liittyvät myynninedistämispalkkiosanomat, kuten "varastossa" ja "vain muutama jäljellä". Nämä asetukset varmistavat, että tuotetta ei voi ostaa, jos sitä ei ole varastossa.

Dynamics 365 Commerce sisältää arviot tuotteiden käytettävissä olevasta saatavuudesta. Lisätietoja arvioidun käytettävissä olevan käytettävyyden laskemisesta on kohdassa [Jälleenmyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).

Commercen sivustotyökalussa voidaan määrittää tuotteen tai luokan varastorajat ja -alueet. Ne määräävät, voidaanko varaston arvoksi luokitella varastossa, vähissä vai loppunut. Katso lisätietoja kohdasta [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

> [!NOTE]
> Varaston raja-arvojen ja alueiden tuki on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.

## <a name="inventory-settings"></a>Varastoasetukset

Commercessa varastoasetukset määritetään sivustotyökalussa kohdassa **Sivuston asetukset \> Laajennukset \> Varaston hallinta**. Varastoasetuksia on viisi, joista yksi on poistettu käytöstä (vanhentunut):

- **Ota käyttöön varastotarkistus sovelluksessa** – Tämä asetus ottaa tuotevaraston tarkistuksen pois käytöstä. Osta-ruutu, ostoskori ja nouto myymälästä -moduulit tarkistavat tuotevaraston ja sallivat tuotteen lisäämisen ostoskoriin vain, jos varasto on käytettävissä.
- **Varastotaso perustuu** – Tämä asetus määrittää, miten varastotasot lasketaan. Käytettävissä olevat arvot ovat **Käytettävissä olevat yhteensä**, **Fyysisesti käytettävissä olevat** ja **Loppu varastosta**. Commercessa varaston kynnysarvo ja alueet voidaan määritellä jokaiselle tuotteelle ja luokalle. Varasto-APIt palauttavat tuotevarastotiedot sekä **käytettävissä olevan kokonaismäärän** että **fyysisen käytettävissä olevan** ominaisuuden osalta. Jälleenmyyjä päättää, käytetäänkö **Käytettävissä olevaa** tai **Fyysisesti käytettävissä olevaa** arvoa varaston inventoinnin ja varasto- ja loppuvarastotilojen vastaavien alueiden määrittämiseen.

    **Loppunut varastosta** -arvo **Varastotason varaston kynnys arvo** asetuksen perusteella on vanha (aiempi), vanhentunut arvo. Kun se on valittu, varaston inventoinnit määräytyvät **Käytettävissä olevan** kokonaisarvon perusteella, mutta kynnys määritetään myöhemmin annetun luvun **Loppu varastosta** -arvon mukaan. Tämä raja-asetus koskee kaikkia tuotteita, jotka ovat verkkokauppasivustossa. Jos varasto on raja-arvon alapuolella, tuotetta ei pidetä varastossa. Muussa tapauksessa sitä pidetään varastossa. **Loppu varastosta** -arvo on rajallinen, emmekä suosittele sen käyttämistä versiossa 10.0.12 ja sitä uudemmissa.

- **Usean varaston varastotaso** – Tämän asetuksen avulla varastotaso voidaan laskea oletusvarastoa tai useita varastoja vasten. **Perustuu yksittäiseen varastoon** -vaihtoehto laskee varastotasot oletusvaraston perusteella. Sähköisen kaupankäynnin toimipiste voi myös helpottaa täyttämistä viitaten useisiin varastoihin. Tässä tapauksessa varaston käytettävyys ilmaistaan **lähetys- ja noutovarastojen koostamisen perusteella**. Jos asiakas esimerkiksi ostaa nimikkeen ja valitsee toimitustyypiksi "lähetys", nimike voidaan lähettää mistä tahansa täyttämisryhmän varastosta, jossa on käytettävissä oleva varasto. Tuotetietosivulla näkyy lähetyssanoma "Varastossa", jos täyttämisryhmän käytettävissä olevalla lähetysvarastolla on varastoa. 

> [!IMPORTANT] 
> **Usean varaston varastotaso** -asetus on käytettävissä Commerce-versiosta 10.0.19 lähtien. Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Varastoalueet** – Tämä asetus määrittää, mitkä varastoalueet, joille sanoma näytetään sivustomoduuleissa. Sitä voi käyttää vain, jos **Käytettävissä oleva kokonaisarvo** tai **Käytettävissä oleva fyysinen** arvo on valittu **Varastotaso perusteella** -asetukselle. Käytettävissä olevat arvot ovat **Kaikki**, **Alhaiset ja loppunut varastosta** ja **Loppunut varastosta**.

    - Kun **Kaikki** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta varastossa ("käytettävissä" oleva sanoma) kohteeseen loppunut varastosta ("loppunut varastosta").
    - Kun **Vähissä ja loppunut varastosta** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta paitsi varastossa ("käytettävissä" oleva sanoma).
    - Kun **Loppunut varastosta** on valittu, vain "loppunut varastosta" -sanoma tulee näkyviin.

- **Loppunut varastosta** – Tämä vanha numeerinen asetus tulee voimaan vain, jos **Loppunut varastosta** arvoksi on valittu **Varaston vähimmäisarvo** -asetuksen perusteella.

> [!IMPORTANT] 
> Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12. Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Varastoasetuksia käyttävät moduulit

Ostolaatikko, toivelista, myymälänvalitsin, ostoskori ja ostoskorin kuvakemoduulit käyttävät varastoasetuksia näyttämään varastoalueet ja sanomat.

Seuraavan kuvan esimerkissä PDP näyttää Varastossa (Käytettävissä) -sanoman.

![Esimerkki PDP-moduulista, jossa on varastossa oleva sanoma](./media/pdp-InStock.png)

Seuraavan kuvan esimerkissä PDP näyttää Loppunut varastosta (Käytettävissä) -sanoman.

![Esimerkki PDP-moduulista, jossa on loppunut varastosta -sanoma](./media/pdp-outofstock.png)

Seuraavan kuvan esimerkissä ostoskori näyttää Varastossa (Käytettävissä) -sanoman.

![Esimerkki ostoskorimoduulista, jossa on varastossa oleva sanoma](./media/cart-instock.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tilin hallintasivut ja -moduulit](account-management.md)

[Myymälän valitsinmoduuli](store-selector.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
