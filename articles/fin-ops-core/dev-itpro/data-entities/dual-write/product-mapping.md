---
title: Yhtenäinen tuotekokemus
description: Tässä artikkelissa käsitellään tuotetietojen integraatiota talous- ja toimintosovellusten sekä Dataversen välillä.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1546cdaf3c63a7ff9a330ae8609595aaf48fbc48
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111483"
---
# <a name="unified-product-experience"></a>Yhtenäinen tuotekokemus

[!include [banner](../../includes/banner.md)]



Jos liiketoiminnan ekosysteemi muodostuu Dynamics 365 -sovelluksista, kuten Financesta, Supply Chain Managementista ja Salesista, yritykset käyttävät usein näitä sovelluksia tuotetietojen lähteenä. Tämä johtuu siitä, nämä sovellukset muodostavat toimivan tuoteinfrastruktuurin, jota kehittyneet hinnoittelukäsitteet ja tarkat käytettävissä olevan varaston tiedot täydentävät. Jos yritykset käyttävät ulkoista tuotteen elinkaaren hallinta- eli PLM-järjestelmää tuotetietojen lähteenä, he voivat kanavoida tuotteita talous- ja toimintosovelluksista muihin Dynamics 365 -sovelluksiin. Integroitu tuotetietomalli voidaan tuoda yhtenäisen tuotekokemuksen avulla Dataverseen, jolloin kaikki sovelluksen käyttäjät, myös Power Platform -käyttäjät, voivat hyödyntää talous- ja toimintosovelluksista saatavia monipuolisia tuotetietoja.

Salesin tuotetietomalli.

![CE-tuotetietomalli.](media/dual-write-product-4.jpg)

Talous- ja toimintosovellusten tuotetietomalli.

![Talous- ja toimintosovellusten tuotetietomalli.](media/dual-write-products-5.jpg)

Nämä kaksi tuotetietomallia on integroitu Dataversessä seuraavan kuvan osoittamalla tavalla.

![Dynamics 365 -sovellusten tuotetietomalli.](media/dual-write-products-6.jpg)

Tuotteiden kaksoiskirjoituksen taulukkokartat on suunniteltu vain yksisuuntaista tiedonkulkua varten, ja tieto kulkee talous- ja toimintosovelluksista Dataverseen lähes reaaliaikaisesti. Tuoteinfrastruktuuri on kuitenkin avoin, joten se voidaan tarvittaessa muuttaa kaksisuuntaiseksi. Vaikka voit mukauttaa sitä omalla vastuullasi, Microsoft ei suosittele tätä lähestymistapaa.

## <a name="templates"></a>Mallit

Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot. Seuraava taulukko osoittaa, miten taulukarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.

Taloushallinnon ja toimintojen sovellukset | Muut Dynamics 365 -sovellukset | Kuvaus
-----------------------|--------------------------------|---
[Kaikki tuotteet](mapping-reference.md#138) | msdyn_globalproducts | Kaikkien tuotteiden taulukko sisältää kaikki tuotteet, jotka ovat käytettävissä talous- ja toimintosovelluksessa – siis sekä vapautetut tuotteet että tuotteet, joita ei ole vapautettu.
[CDS-vapautetut erilliset tuotteet](mapping-reference.md#213) | Tuote | **Tuote**-taulun sarakkeet määrittävät tuotteen. Se sisältää yksittäisiä tuotteita (tuotteita, joissa on alatyypin tuote) ja tuotevariantteja. Yhdistämismääritykset ovat seuraavassa taulukossa.
[Värit](mapping-reference.md#170) | msdyn\_productcolors
[Konfiguraatiot](mapping-reference.md#171) | msdyn\_productconfigurations
[Tilauksen oletusasetukset](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Tuoteluokat](mapping-reference.md#166) | msdyn_productcategories | Kukin tuoteluokka sekä tiedot sen rakenteesta ja ominaisuuksista sisältyy tuoteluokkatauluun.
[Tuoteluokan määritykset](mapping-reference.md#167) | msdyn_productcategoryassignments | Tuote voidaan määrittää luokkaan tuoteluokan määritystaulun avulla.
[Tuoteluokkahierarkiat](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Tuotehierarkioiden avulla luokittelet tai ryhmittelet tuotteita. Luokkahierarkiat ovat käytettävissä Dataversessa tuoteluokkahierarkiataulun avulla.
[Tuoteluokkahierarkian roolit](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Tuotehierarkioita käytetään D365:n talous- ja toimintosovelluksissa eri rooleissa. Kussakin roolissa käytettävä luokkaa määritetään tuoteluokkahierarkiataulun avulla.
[Tuotteen oletustilausasetukset V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Tuotedimension ryhmät](mapping-reference.md#173) | msdyn\_productdimensiongroups | Tuotedimensioryhmä määrittää, mitkä tuotedimensiot määrittävät tuotteet.
[Päätuotteen värit](mapping-reference.md#187) | msdyn_sharedproductcolors | **Jaettu tuoteväri** -taulu ilmaisee värit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
[Päätuotteen konfiguraatiot](mapping-reference.md#188) | msdyn_sharedproductconfigurations | **Jaettu tuotekonfiguraatio** -taulu ilmaisee konfiguraatiot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
[Päätuotteen koot](mapping-reference.md#190) | msdyn_sharedproductsizes | **Jaettu tuotekoko** -taulu ilmaisee koot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
[Päätuotteen tyylit](mapping-reference.md#191) | msdyn_sharedproductstyles | **Jaettu tuotetyyli** -taulu ilmaisee tyylit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
[Tuotenumeron viivakoodi](mapping-reference.md#164) | msdyn\_productbarcodes | Tuotteen viivakoodeja käytetään tuotteiden yksilöimiseen.
[Tuotekohtaiset yksikkömuunnokset](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Vapautetut tuotteet V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails**-taulu sisältää ne talous- ja toimintosovellusten sarakkeet, jotka määrittävät tuotteen ja jotka sisältävät tuotteen talous- ja hallintotiedot.
[Koot](mapping-reference.md#174) | msdyn\_productsizes
[Varastodimensioryhmät](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Tuotteen varastodimensioryhmä ilmaisee menetelmän, jolla tuotteiden sijoittaminen varastoon määritetään.
[Tyylit](mapping-reference.md#178) | msdyn\_productstyles
[Seurantadimensioryhmät](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Tuotteen seurantadimensioryhmä ilmaisee menetelmän, jolla varastossa olevia tuotteita seurataan.
[Yksiköt](mapping-reference.md#219) | uoms
[Yksikkömuunnokset](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Tuotteiden integrointi

Tässä mallissa tuotetta vastaa kahden Dataversen taulun yhdistelmä: **tuote** ja **msdyn\_sharedproductdetails**. Siinä missä ensimmäinen taulu sisältää tuotteen määritelmän (tuotteen yksilöivän tunnisteen, tuotteen nimien ja kuvauksen), toinen taulu sisältää tuotetasolla tallennetut sarakkeet. Tuote määritetään näiden kahden taulun yhdistelmällä varastointiyksikkökäsitteen mukaisesti. Kunkin julkaistun tuotteen tiedot ovat näissä tauluissa (tuote ja jaetut tuotetiedot). Kaikkia tuotteita (julkaistuja ja julkaisemattomia) voidaan seurata **Tuotteet yleisesti** -taulun avulla.

Koska tuote ilmaista varastointiyksikkönä, käsitteet erilliset tuotteet, päätuotteet ja tuotevariantit voidaan tallentaa Dataverseen seuraavasti:

- **Tuotteet, joissa on alatyypin tuote** ovat itsensä määrittäviä tuotteita. Dimensioita ei tarvitse määrittää. Tällainen tuote on esimerkiksi tietty kirja. Näille tuotteille luodaan yksi rivi **Tuote**-taulussa ja yksi rivi **msdyn\_sharedproductdetails**-taulussa. Yhtään tuoteperheriviä ei luoda.
- **Päätuotteita** käytetään yleisinä tuotteina, joissa olevat säännöt ja määritelmä määrittävät liiketoimintaprosessien toiminnan. Näiden määritelmien perusteella voidaan luoda tuotevarianteiksi kutsuttuja erillisiä tuotteita. Esimerkiksi t-paita on päätuote, jonka dimensioita väri ja koko voivat olla. Julkaistavissa varianteissa voi olla erilaisia dimensioyhdistelmiä, kuten s-kokoinen sininen t-paita tai m-kokoinen vihreä t-paita. Integroinnissa tuotetauluun kullekin variantille luodaan yksi rivi. Tämä rivi sisältää varianttikohtaiset tiedot, kuten eri dimensiot. Tuotteen yleiset tiedot tallennetaan **msdyn\_sharedproductdetails**-tauluun. (Nämä yleiset tiedot on tallennettu päätuotteeseen.) Päätuotteen tiedot synkronoidaan Dataverseen heti, kun vapautettu päätuote luodaan (mutta ennen varianttien vapauttamista).
- **Erillisillä tuotteilla** tarkoitetaan kaikkia tuotteiden alatyypin tuotteita ja kaikkia tuotevariantteja.

![Tuotteiden tietomalli.](media/dual-write-product.png)

Kun kaksoiskirjoitustoiminto on käytössä, talous- ja toimintosovellusten tuotteet synkronoidaan muissa Dynamics 365 -tuotteissa **Luonnos**-tilassa. Ne lisätään ensimmäiseen hinnastoon siinä valuutassa, jota käytetään asiakkaiden aktivointisovelluksessa, ja käyttämällä aakkosellista lajittelua hinnaston nimen mukaan. Ne siis toisin sanoen lisätään ensimmäiseen Dynamics 365 -sovelluksen hinnastoon, joka vastaa sen yrityksen valuuttaa, jossa tuote vapautetaan talous- ja toimintosovelluksessa. Jos ilmoitetulla valuutalla ei ole hinnastoa, hinnasto luodaan automaattisesti ja tuote määritetään siihen.

Talous- ja toimintosovellukseen liittyvän valuutan yksikköhaun oletusarvoiseen hintaluetteloon liittävän kaksoiskirjoituksen laajennusten nykyinen toteutus ja asiakasvuorovaikutussovelluksen ensimmäinen hinnasto käyttävät aakkosellista lajittelua hinnaston nimessä. Jos haluat määrittää tietyn valuutan oletushintaluettelon, kun valuuttaa varten on useita hinnastoja, hintaluettelon nimi on päivitettävä aakkosjärjestyksessä aiempaan nimeen kuin muut saman valuutan hinnastoissa. Jos tietyllä valuutalla ei ole hinnastoa, uusi hinnasto luodaan.

Talous- ja toimintosovellusten oletustuotteet synkronoidaan muihin Dynamics 365 -sovelluksiin **Luonnos**-tilassa. Jos haluat synkronoida **Aktiivinen**-tilassa olevan tuotteen, jotta sitä voi käyttää esimerkiksi suoraan myyntitilauksen tarjouksissa, seuraavat asetukset on valittava: valitse ensin **Järjestelmä> Hallinto > Järjestelmän hallinta > Järjestelmäasetukset > Sales**-välilehti ja sitten **Luo tuotteet aktiivisessa tilassa = kyllä**.

Tuotteita synkronoitaessa on annettava arvo **Myyntiyksikkö**-kenttään talous- ja toimintosovelluksessa, koska se on pakollinen kenttä Salesissa.

Tuoteperheiden luomista Dynamics 365 Salesista ei tueta tuotteiden kaksoiskirjoituksen synkronoinnissa.

Tuotteet synkronoidaan talous- ja toimintosovelluksesta Dataverseen. Tämän vuoksi tuotetaulusarakkeet arvot voidaan muuttaa Dataversessa, mutta kun synkronointi käynnistyy (tuotesaraketta muokataan talous- ja toimintosovelluksessa), se korvaa Dataversen arvot.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[CDS-vapautetut erilliset tuotteet](mapping-reference.md#213) | Tuote |
[Vapautetut tuotteet V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Kaikki tuotteet](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Tuotedimensiot

Tuotedimensiot ovat ominaisuuksia, joilla voidaan tuotevariantti tunnistetaan. Neljä tuotedimensiota (väri, koko, tyyli ja konfiguraatio) yhdistetään myös Dataverseen määrittämää tuotevariantteja. Seuraavassa kuvassa on Väri-tuotedimension tietomalli. Samaa mallia käytetään myös kokojen, tyylien ja konfiguraatioiden osalta.

![Tuotedimensioiden tietomalli.](media/dual-write-product-two.png)

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Värit](mapping-reference.md#170) | msdyn\_productcolors
[Koot](mapping-reference.md#174) | msdyn\_productsizes
[Tyylit](mapping-reference.md#178) | msdyn\_productstyles
[Konfiguraatiot](mapping-reference.md#171) | msdyn\_productconfigurations

Kun tuotteella on erilaisia tuotedimensioita (esimerkiksi koko ja väri ovat päätuotteen tuotedimensioita), kukin erillinen tuote (toisin sanoen kukin tuotevariantti) määritetään kyseisten tuotedimensioiden yhdistelmänä. Esimerkiksi tuotenumero B0001 on XS-kokoinen musta t-paita, ja tuotenumero B0002 on S-kokoinen musta t-paita. Tässä tapauksessa määritetään aiemmin luodut tuotedimensioyhdistelmät. Esimerkiksi edellisen esimerkin t-paita voi olla XS-kokoinen ja musta, S-kokoinen ja musta, M-kokoinen ja musta tai L-kokoinen ja musta mutta se ei voi olla XL-kokoinen ja musta. Päätuotteessa käytettävät tuotedimensiot on siis määritetty, ja variantit voidaan vapauttaa näiden arvojen perusteella.

Päätuotteen käytössä olevien tuotedimensioiden seuraamista varten on luotu seuraavat taulut, jotka on yhdistetty kunkin tuotedimension osalta Dataverseen. Lisätietoja on kohdassa [Tuotetietojen yleiskatsaus](../../../../supply-chain/pim/product-information.md).

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Päätuotteen värit](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Päätuotteen konfiguraatiot](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Päätuotteen koot](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Päätuotteen tyylit](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Tuotenumeron viivakoodi](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tilauksen oletusasetukset ja tuotekohtaiset tilauksen oletusasetukset

Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Näitä tietoja voidaan käyttää Dataversessa käyttämällä tilauksen oletusasetusten ja tuotekohtaisen tilauksen oletusasetusten yksikön avulla. Lisätietoja toiminnosta on [Tilauksen oletusasetukset -artikkelissa](../../../../supply-chain/production-control/default-order-settings.md).

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Tilauksen oletusasetukset](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Tuotteen oletustilausasetukset V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mittayksikkö ja mittayksikön muunnokset

Mittayksikkö ja sen muunnos ovat käytettävissä Dataversessa seuraavassa kuvassa olevan tietomallin mukaisesti.

![Mittayksikön tietomalli.](media/dual-write-product-three.png)

Mittayksikkökäsite on integroitu talous- ja toimintosovellusten sekä muiden Dynamics 365 -sovellusten välillä. Kullekin talous- ja toimintosovelluksen yksikköluokalle luodaan Dynamics 365 -sovelluksessa yksikköryhmä, joka sisältää yksikköluokkaan kuuluvat yksiköt. Jokaiselle yksikköryhmälle luodaan myös oletusarvoinen perusyksikkö.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Tuotekohtaiset yksikkömuunnokset](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Yksiköt](mapping-reference.md#219) | uoms
[Yksikkömuunnokset](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Vastaavien yksiköiden tietojen ensimmäinen synkronointi talous- ja toimintosovellusten sekä Dataversen välillä

### <a name="initial-synchronization-of-units"></a>Yksiköiden ensimmäinen synkronointi

Kun kaksoiskirjoitus on otettu käyttöön talous- ja toimintosovellusten yksiköt synkronoidaan muihin Dynamics 365 -sovelluksiin. Talous- ja toimintosovelluksista Dataversessa synkronoiduilla yksikköryhmillä on merkintäjoukko, joka ilmaisee niiden olevan ulkoisesti ylläpidettyjä.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Talous- ja toimintosovellusten sekä muiden Dynamics 365 -sovellusten yksiköiden ja yksikköluokkien tai -ryhmien täsmäyttäminen

Ensinnäkin on tärkeää huomata, että yksikön integrointiavain on msdyn_symbol. Tämän vuoksi tämän arvon on oltava yksilöivä Dataversen tai muun Dynamics 365 -sovelluksen arvo. Koska muissa Dynamics 365 -sovelluksissa Yksikköryhmän tunnus- ja Nimi-pari määrittää yksikön yksilöllisyyden, talous- ja toimintosovellusten sekä Dataversen yksikkötietojen täsmäyttämisessä on otettava huomioon erilaisia skenaarioita.

Talous- ja toimintosovellusten sekä muiden Dynamics 365 -sovellusten samanlaiset tai päällekkäiset yksiköt:

+ **Yksikkö kuuluu johonkin muun Dynamics 365 -sovelluksen yksikköryhmään, joka vastaa talous- ja toimintosovellusten liitettyä luokkaa**. Tässä tapauksessa muiden Dynamics 365 -sovellusten msdyn_symbol-sarakkeeseen on täytettävä talous- ja toimintosovellusten yksikkösymboli. Tämän vuoksi tietoja täsmäytettäessä yksikköryhmä määritetään ulkoisesti ylläpidetyksi muissa Dynamics 365 -sovelluksissa.
+ **Yksikkö kuuluu johonkin muun Dynamics 365 -sovelluksen yksikköryhmään, joka ei vastaa talous- ja toimintosovellusten liitettyä luokkaa (talous- ja toimintosovelluksissa ei ole aiemmin luotua yksikköluokkaa muiden Dynamics 365 -sovellusten yksikköluokalle).** Tässä tapauksessa kenttään msdyn_symbol on täytettävä satunnainen merkkijono. Huomaa, että tämän arvon on oltava yksilöivä muissa Dynamics 365 -sovelluksissa.

Talous- ja toimintosovellusten yksiköitä ja yksikköluokkia ei ole muissa Dynamics 365 -sovelluksissa:

Kaksoiskirjoituksen osana talous- ja toimintosovellusten yksikköryhmät ja niitä vastaavat yksiköt luodaan ja synkronoidaan muissa Dynamics 365 -sovelluksissa ja Dataversessa. Lisäksi yksikköryhmä määritetään ulkoisesti ylläpidetyksi. Ylimääräisiä käynnistystoimia ei tarvita.

Muiden Dynamics 365 -sovellusten yksiköitä ei ole talous- ja toimintosovelluksissa:

Kaikkien yksiköiden msdyn_symbol-sarake on täytettävä. Yksiköt voidaan aina luoda talous- ja toimintosovellusten vastaavassa yksikköluokassa (jos sellainen on). Jos yksikköluokkaa ei ole, muiden Dynamics 365 -sovellusten yksikköryhmää vastaava ensimmäinen yksikköluokka on luotava. (Huomaa, että talous- ja toimintosovelluksissa ei voi luoda yksikköluokkaa muuten kuin laajentamalla, jos luettelointia laajennetaan.) Voit luoda sitten yksikön. Huomaa, että talous- ja toimintosovellusten yksikkösymbolin on oltava se msdyn_symbol, joka määritettiin yksikölle aiemmin muissa Dynamics 365 -sovelluksissa.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tuotekäytännöt: dimensio-, seuranta- ja varastoryhmät

Tuotekäytännöt ovat käytäntöjoukkoja, jolla määritetään varaston tuotteet ja niiden ominaisuudet. Tuotedimensioryhmää, tuotteen seurantadimensioryhmää ja varastodimensioryhmää voi etsiä tuotekäytäntöinä.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Tuotedimension ryhmät](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Varastodimensioryhmät](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Seurantadimensioryhmät](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Tuotehierarkiat

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset |
---|---
[Tuoteluokan määritykset](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Tuoteluokkahierarkiat](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Tuoteluokkahierarkian roolit](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Tuotteiden integrointiavain

Talous- ja toimintosovellusten sekä Dataversen väliseen tuotteiden yksilöivään tunnistamiseen käytetään integrointiavaimia.
Tuotteiden **(productnumber)** on yksilöivä avain, jolla tuote tunnistetaan Dataversessa. Se muodostetaan seuraavasta ketjutuksesta: **(yritys, msdyn_productnumber)**. **Yritys** ilmaisee talous- ja toimintosovellusten yrityksen, kun taas **msdyn_productnumber** ilmaisee tietyn tuotteen tuotenumeron talous- ja toimintosovelluksissa.

Muiden Dynamics 365 -sovellusten käyttäjät tunnistavat tuotteen käyttöliittymässä **msdyn_productnumber**-sarakkeen mukaan. (Huomaa, että sarakkeen otsikko on **Tuotenumero**.) Tuotelomakkeessa näkyy sekä yritys että msydn_productnumber. (productnumber)-saraketta eli tuotteen yksilöivää avainta ei kuitenkaan näytetä.

Jos muodostat sovelluksia Dataversessä, kiinnitä huomiota **productnumber**-kohdan (tuotteen yksilöivä tunnus) käyttämiseen integrointiavaimena. Älä käytä **msdyn_productnumber**-arvoa, koska se ei ole yksilöllinen.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Tuotteiden ensimmäinen synkronointi ja tietojen siirtäminen Dataversesta talous- ja toimintosovelluksiin

### <a name="initial-synchronization-of-products"></a>Tuotteiden ensimmäinen synkronointi

Kun kaksoiskirjoitus on otettu käyttöön, talous- ja toimintosovellusten tuotteet synkronoidaan Dataverseen ja muihin asiakkaan aktivointisovelluksiin. Dataversessa ja muissa Dynamics 365 -sovelluksissa ennen kaksoiskirjoituksen julkaisua luotuja tuotteita ei päivitetä eikä täsmäytetä talous- ja toimintosovellusten tuotetietojen kanssa.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Tuotetietojen täsmäyttäminen talous- ja toimintosovelluksista sekä muista Dynamics 365 -sovelluksista

Jos samat tuotteet säilytetään (päällekkäiset tai vastaavat) talous- ja toimintosovelluksissa, Dataversessa ja muissa Dynamics 365 -sovelluksissa, kun kaksoiskirjoitusta otetaan käyttöön, talous- ja toimintosovellusten tuotteiden synkronointi tehdään ja Dataversessa näkyy saman tuotteen rivien kaksoiskappaleita.
Jotta näin ei tapahtuisi siinä tapauksessa, että muissa Dynamics 365 -sovelluksissa on tuotteita, jotka ovat päällekkäisiä tai vastaavia kuin talous- ja toimintosovellusten tuotteet, kaksoiskirjoituksen käyttöönottavan järjestelmänvalvojan on käynnistettävä sarakkeet **Yritys** (esimerkki: USMF) ja **msdyn_productnumber** (esimerkki: 1234:Black:S), ennen kuin tuotteet synkronoidaan. Toisin sanoen näiden kahden Dataversen tuotteen sarakkeisiin on täytettävä se talous- ja toimintosovellusten yritys, johon tuote on täsmäytettävä, ja sen tuotenumero.

Kun synkronointi sitten otetaan käyttöön ja sitä käytetään, talous- ja toimintosovellusten tuotteet synkronoidaan vastaaviin Dataversen ja muiden Dynamics 365 -sovellusten tuotteisiin. Tämä koskee sekä erillisiä tuotteita että tuotevariantteja.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Tuotetietojen siirtäminen muista Dynamics 365 -sovelluksista talous- ja toimintosovelluksiin

Jos muissa Dynamics 365 -sovelluksissa on tuotteita, joita ei ole talous- ja toimintosovelluksissa, järjestelmänvalvoja voi tuoda kyseiset tuotteet talous- ja toimintosovelluksiin käyttämällä kohdetta **EcoResReleasedProductCreationV2Entity**. Sitten tuotetiedot on täsmättävä talous- ja toimintosovelluksista sekä muista Dynamics 365 -sovelluksista edellä kuvatulla tavalla.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

