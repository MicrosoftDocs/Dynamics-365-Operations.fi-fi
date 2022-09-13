---
title: Varastoasetusten käyttäminen
description: Tässä artikkelissa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 49310a44f8b9c636734e04d4eed9445384b55791
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405317"
---
# <a name="apply-inventory-settings"></a>Varastoasetusten käyttäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.

Varastoasetukset määrittävät, tuleeko varasto tarkistaa, ennen kuin tuotteet lisätään kärryyn. Ne määrittävät myös varastoon liittyvät myynninedistämispalkkiosanomat, kuten "varastossa" ja "vain muutama jäljellä". Nämä asetukset varmistavat, että tuotetta ei voi ostaa, jos sitä ei ole varastossa.

Dynamics 365 Commerce sisältää arviot tuotteiden käytettävissä olevasta saatavuudesta. Lisätietoja arvioidun käytettävissä olevan käytettävyyden laskemisesta on kohdassa [Jälleenmyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).

Commercen sivustotyökalussa voidaan määrittää tuotteen tai luokan varastorajat ja -alueet. Ne määräävät, voidaanko varaston arvoksi luokitella varastossa, vähissä vai loppunut. Katso lisätietoja kohdasta [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

> [!NOTE]
> Varaston raja-arvojen ja alueiden tuki on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.

## <a name="inventory-settings"></a>Varastoasetukset

Commercessa varastoasetukset määritetään sivustotyökalussa kohdassa **Sivuston asetukset \> Laajennukset \> Varaston hallinta**. Varastoasetuksia on kuusi, joista yksi on poistettu käytöstä (vanhentunut):

- **Ota käyttöön varastotarkistus sovelluksessa** – Tämä asetus ottaa tuotevaraston tarkistuksen pois käytöstä. Osta-ruutu, ostoskori ja nouto myymälästä -moduulit tarkistavat tuotevaraston ja sallivat tuotteen lisäämisen ostoskoriin vain, jos varasto on käytettävissä.
- **Varastotaso perustuu** – Tämä asetus määrittää, miten varastotasot lasketaan. Käytettävissä olevat arvot ovat **Käytettävissä olevat yhteensä**, **Fyysisesti käytettävissä olevat** ja **Loppu varastosta**. Commercessa varaston kynnysarvo ja alueet voidaan määritellä jokaiselle tuotteelle ja luokalle. Varasto-APIt palauttavat tuotevarastotiedot sekä **käytettävissä olevan kokonaismäärän** että **fyysisen käytettävissä olevan** ominaisuuden osalta. Jälleenmyyjä päättää, käytetäänkö **Käytettävissä olevaa** tai **Fyysisesti käytettävissä olevaa** arvoa varaston inventoinnin ja varasto- ja loppuvarastotilojen vastaavien alueiden määrittämiseen.

    **Loppunut varastosta** -arvo **Varastotason varaston kynnys arvo** asetuksen perusteella on vanha (aiempi), vanhentunut arvo. Kun se on valittu, varaston inventoinnit määräytyvät **Käytettävissä olevan** kokonaisarvon perusteella, mutta kynnys määritetään myöhemmin annetun luvun **Loppu varastosta** -arvon mukaan. Tämä raja-asetus koskee kaikkia tuotteita, jotka ovat verkkokauppasivustossa. Jos varasto on raja-arvon alapuolella, tuotetta ei pidetä varastossa. Muussa tapauksessa sitä pidetään varastossa. **Loppu varastosta** -arvo on rajallinen, emmekä suosittele sen käyttämistä versiossa 10.0.12 ja sitä uudemmissa.

- **Usean varaston varastotaso** – Tämän asetuksen avulla varastotaso voidaan laskea oletusvarastoa tai useita varastoja vasten. **Perustuu yksittäiseen varastoon** -vaihtoehto laskee varastotasot oletusvaraston perusteella. Sähköisen kaupankäynnin toimipiste voi myös helpottaa täyttämistä viitaten useisiin varastoihin. Tässä tapauksessa varaston käytettävyys ilmaistaan **lähetys- ja noutovarastojen koostamisen perusteella**. Jos asiakas esimerkiksi ostaa nimikkeen ja valitsee toimitustyypiksi "lähetys", nimike voidaan lähettää mistä tahansa täyttämisryhmän varastosta, jossa on käytettävissä oleva varasto. Tuotetietosivulla näkyy lähetyssanoma "Varastossa", jos täyttämisryhmän käytettävissä olevalla lähetysvarastolla on varastoa. 

    > [!IMPORTANT] 
    > **Usean varaston varastotaso** -asetus on käytettävissä Commerce-versiosta 10.0.19 lähtien. Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Tuoteluettelosivujen varastoasetukset** – Tällä asetuksella määritetään, miten varastosta loppuneet tuotteet näkyvät tuotekokoelman ja hakutulosten moduulien muodostamisissa tuoteluetteloissa. Käytettävissä ovat arvot **Näytä tilauksessa muiden tuotteiden kanssa**, **Piilota varastosta loppuneet tuotteet luettelosta** ja **Näytä varastosta loppuneet tuotteet luettelon lopussa**. Tämän asetuksen käyttö edellyttää, että tietyt edellytysasetukset määritetään ensin Commerce-pääkonttorisovelluksessa. Lisätietoja on kohdassa [Varaston huomioon ottava tuoteluettelo](inventory-aware-product-listing.md).

    > [!IMPORTANT] 
    > **Tuoteluettelosivujen varastoasetukset** -asetus on käytettävissä Commerce-versiosta 10.0.20 lähtien. Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Varastoalueet** – Tämä asetus määrittää varastoalueen sanomat, jotka näytetään sivustomoduuleissa. Sitä voi käyttää vain, jos **Käytettävissä oleva kokonaisarvo** tai **Käytettävissä oleva fyysinen** arvo on valittu **Varastotaso perusteella** -asetukselle. Käytettävissä olevat arvot ovat **Kaikki**, **Alhaiset ja loppunut varastosta** ja **Loppunut varastosta**.

    - Kun **Kaikki** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta varastossa ("käytettävissä" oleva sanoma) kohteeseen loppunut varastosta ("loppunut varastosta").
    - Kun **Vähissä ja loppunut varastosta** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta paitsi varastossa ("käytettävissä" oleva sanoma).
    - Kun **Loppunut varastosta** on valittu, vain "loppunut varastosta" -sanoma tulee näkyviin.

- **Loppunut varastosta** – Tämä vanha numeerinen asetus tulee voimaan vain, jos **Loppunut varastosta** arvoksi on valittu **Varaston vähimmäisarvo** -asetuksen perusteella.

> [!IMPORTANT] 
> Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12. Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Varastoasetuksia käyttävät moduulit

Ostolaatikko, toivelista, myymälänvalitsin, ostoskori ja ostoskorin kuvakemoduulit käyttävät varastoasetuksia näyttämään varastoalueet ja sanomat.

Seuraavan kuvan esimerkissä PDP näyttää Varastossa (Käytettävissä) -sanoman.

![Esimerkki PDP-moduulista, jossa on Varastossa-sanoma.](./media/pdp-InStock.png)

Seuraavan kuvan esimerkissä PDP näyttää Loppunut varastosta (Käytettävissä) -sanoman.

![Esimerkki PDP-moduulista, jossa on Loppunut varastosta -sanoma.](./media/pdp-outofstock.png)

Seuraavan kuvan esimerkissä ostoskori näyttää Varastossa (Käytettävissä) -sanoman.

![Esimerkki ostoskorimoduulista, jossa on Varastossa-sanoma.](./media/cart-instock.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tilin hallintasivut ja -moduulit](account-management.md)

[Myymälän valitsinmoduuli](store-selector.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
