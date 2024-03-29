---
title: Myymälän valitsinmoduuli
description: Tässä artikkelissa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268322"
---
# <a name="store-selector-module"></a>Myymälän valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Asiakkaat voivat käyttää myymälän valitsinmoduulia ja noutaa tuotteen valitusta myymälästä verkko-oston jälkeen. Commerce-versiossa 10.0.13 myymälän valitsinmoduuli sisältää myös lisäominaisuuksia, jotka voivat esitellä lähistöllä olevat myymälät näyttävän **Etsi myymälä** -sivun.

Myymälän valitsinmoduulin avulla käyttäjät voivat syöttää sijainnin (kaupunki, osavaltio, osoite jne.) ja etsiä myymälöitä hakusäteen avulla. Kun moduuli avataan ensimmäisen kerran, se käyttää asiakkaan selaimen sijaintia myymälöiden etsimiseen (jos suostumus on annettu).

## <a name="store-selector-module-usage"></a>Myymälän valitsinmoduulin käyttö

- Myymälän valitsinmoduulia voidaan käyttää tuotetietosivulla (PDP), kun halutaan valita noutopaikka.
- Myymälän valitsinmoduulia voidaan käyttää ostoskorisivulla, kun halutaan valita noutopaikka.
- Myymälän valitsinmoduulia voidaan käyttää erillisenä sivuna, jolla näytetään kaikki käytettävissä olevat myymälät.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Täydennysryhmien asetus Commerce headquarters -sovelluksessa

Jotta myymälän valitsin voisi näyttää käytettävissä olevat myymälät, täydennysryhmä on määritettävä Commerce Headquarters -sovelluksessa. Lisätietoja on kohdassa [Täydennysryhmien määrittäminen](customer-orders-overview.md#set-up-fulfillment-groups).

Lisäksi myymälän sijaintipaikka on määritettävä pääkonttorissa jokaiselle täydennysryhmän myymälälle.

Voit antaa myymälän sijainnin leveys- ja pituusasteet Commerce headquarters -sovelluksessa seuraavasti.

1. Mene **Varastonhallinta \> Asetukset \> Inventaarioanalyysi**.
1. Valitse varaston sijainti vasemmasta ruudusta.
1. Valitse **Osoitteet**-pikavälilehdestä **Lisäasetukset**.

    ![Esimerkki myymälän tiedoista pääkonttorissa.](./media/Store-address.png)

1. Valitse toimintoruudussa **Muokkaa**.
1. Kirjoita **Yleiset**-pikavälilehteen arvot kohteille **leveysaste** ja **pituusaste**.

    ![Esimerkki pääkonttorin myymälän leveysasteiden ja pituusasteiden määrityksestä.](./media/Store-latitude-longitude.png)

1. Valitse toimintoruudussa **Tallenna**. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Piilota myymälä myymälän valitsinmoduulista

Jotkin täytäntöönpanoryhmien myymälät eivät ehkä ole kelvollisia noutosijainteja. Noudata seuraavia ohjeita Commerce headquarters -kohdassa, kun haluat varmistaa, että myymälän valitsinmoduulissa vaihtoehdot näkyvät vain kelvolliset noutosijainnit.

1. Valitse **Retail and Commerce \> Pääkonttorin asetukset \> Täytäntöönpanoryhmät \> Kaikki myymälät**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Poista **Asetus**-kohdassa **On noutosijainti** -valintaruudun valinta aina, kun myymälällä ei ole kelvollista noutopaikkaa.
1. Valitse toimintoruudussa **Tallenna**.
1. Suorita 1070 **Kanavan määritys** -jakeluaikataulutyö.

## <a name="bing-maps-integration"></a>Bing Maps -integrointi

Myymälän valitsinmoduuli on integroitu [Bing Maps REST -sovelluksen ohjelmointirajapintoihin](/bingmaps/rest-services/). Niitä käytetään Bingin geokoodauksen ja automaattisten ehdotusten ominaisuuksien kanssa. Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin. Geokoodauksen ohjelmointirajapintaa käytetään sijainnin muuntamisessa leveys- ja pituusarvoiksi. Integrointia automaattisen ehdotuksen ohjelmointirajapinnan kanssa käytetään näytettäessä hakuehdotukset, kun käyttäjä syöttää sijainnit hakukenttään.

Automaattisen ehdotuksen REST-ohjelmointirajapintaa varten on varmistettava, että seuraavat URL-osoitteet ovat sallittuja sivuston sisällön suojauskäytännön (CSP) perusteella. Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri CSP-direktiiveihin sivustolle (esimerkiksi **img-src**). Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md). 

- Lisää **connect-src**-direktiiviin **&#42;.bing.com**.
- Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.
- Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Nouto myymälästä -tila

Myymälän valitsinmoduuli tukee **Nouto myymälästä** -tilaa. Se näyttää niiden myymälöiden luettelon, joissa tuotetta on noudettavana. Se näyttää myös kunkin luettelossa olevan myymälän aukioloajat ja tuotevaraston. Myymälän valitsinmoduuli edellyttää tuotteen kontekstin, jotta tuotteen saatavuus voidaan hahmontaa ja antaa käyttäjälle mahdollisuus lisätä tuote ostoskoriin, jos tuotteen toimitustavaksi on määritetty **nouto** valitusta myymälästä. Lisätietoja on kohdassa [Varastoasetukset](inventory-settings.md). 

Myymälän valitsinmoduuli voidaan lisätä ostoruutumoduuliin PDP:ssä. Näin näytetään myymälät, joissa tuote on noudettavissa. Se voidaan lisätä myös ostoskoriin. Tässä tapauksessa myymälän valitsinmoduuli näyttää noutovaihtoehdot kullekin ostoskorin rivinimikkeelle. Myymälän valitsinmoduuli voidaan myös lisätä muille sivuille tai moduuleihin laajennusten ja mukautuksien kautta.

Jotta tämä skenaario toimisi, tuotteet on konfiguroitava niin, että käytössä on **nouto**-toimitustapa. Muussa tapauksessa moduulia ei näytetä tuotesivuilla. Lisätietoja toimitustilan konfiguroinnista on kohdassa [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Seuraavassa kuvassa on esimerkki PDP:n käytössä olevasta myymälän valitsinmoduulista.

![Esimerkki PDP-sivulla käytetystä myymälän valitsinmoduulista.](./media/BOPIS.PNG)

> [!NOTE]
> Versiossa 10.0.16 ja uudemmissa versioissa voidaan ottaa käyttöön uusi toiminto, jonka avulla organisaatio voi määrittää asiakkaille useita toimituksen noutovaihtoehtoja.  Jos tämä toiminto on käytössä, myymälävalitsinta ja muita sähköisen kaupan käynnin moduuleja parannetaan, jotta ostaja voi valita mahdollisesti useista noutovaihtoehdoista.  Lisätietoja tästä ominaisuudesta on [tässä ohjeessa](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Etsi myymälät -tila

Myymälän valitsinmoduuli tukee myös **Etsi myymälät** -tilaa. Tämän tilan avulla voidaan luoda myymälän sijaintien sivu, jolla näkyvät käytettävissä olevat myymälät ja niiden tiedot. Tässä tilassa myymälän valitsinmoduuli toimii ilman tuotekontekstia. Sitä voi käyttää erillisenä moduulina millä tahansa sivuston sivulla. Jos lisäksi tarvittavat asetukset ovat käytössä moduulissa, käyttäjät voivat valita myymälän ensisijaiseksi myymäläksi. Kun myymälä valitaan käyttäjän ensisijaiseksi myymäläksi, myymälän tunnusta ylläpidetään selaimen evästeessä. Tämän vuoksi käyttäjän on hyväksyttävä evästeiden käyttöön suostumuksen antava sanoma.

Seuraavassa kuvassa on esimerkki myymälän valitsinmoduulista, jota käytetään yhdessä myymälän sijaintien sivun karttamoduulin kanssa.

![Esimerkki myymälän valitsinmoduulista ja karttamoduulista kaupan sijaintisivulla.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Kartan hahmontaminen

Myymälä valitsinmoduulia voidaan käyttää yhdessä karttamoduulin kanssa, kun halutaan näyttää myymälöiden sijainnit kartalla. Lisätietoja karttamoduulista on kohdassa [Karttamoduuli](map-module.md)

## <a name="store-selector-module-properties"></a>Myymälän valitsinmoduulin ominaisuudet

| Ominaisuuden nimi | Arvo | kuvaus |
|---------------|-------|-------------|
| Otsikko | Teksti | Moduulin otsikko. |
| Menetelmä | **Etsi myymälät** tai **Nouto myymälästä** | **Etsi myymälät** -tilassa näkyvät käytettävissä olevat myymälät. **Nouto myymälästä** -tilassa käyttäjät voivat valita myymälän, jossa nouto tapahtuu. |
| Tyyli | **Valintaikkuna** tai **Sisäinen** | Moduuli voidaan hahmontaa sisäisenä tai valintaikkunassa. |
| Määritä ensisijaiseksi myymäläksi | **Tosi** vai **Epätosi** | Kun tämän ominaisuuden arvo on **Tosi**, käyttäjät voivat määrittää ensisijaisen myymälän. Tämän ominaisuuden käyttäminen edellyttää, että käyttäjät hyväksyvät evästeiden käyttöön suostumuksen antavan sanoman. |
| Näytä kaikki myymälät | **Tosi** vai **Epätosi** | Kun tämän ominaisuuden arvo on **Tosi**, käyttäjät voivat ohittaa **Hakusäde**-ominaisuuden ja tarkastella kaikkia myymälöitä. |
| Automaattisen ehdotuksen asetukset: Tulosten enimmäismäärä | Numero | Tämä ominaisuus määrittää automaattisten ehdotusten tulosten enimmäismäärän, jotka näytetään Bingin automaattisten ehdotusten ohjelmointirajapinnan kautta. |
| Hakusäde | Numero | Tämä ominaisuus määrittää myymälöiden hakusäteen maileina. Jos arvoa ei määritetä, käytössä on oletushakusäde 50 mailia. |
| Palvelun käyttöehdot | URL-osoite |  Tämä ominaisuus määrittää Bing Maps -palvelun käyttämiseen vaadittavien palvelun käyttöehtojen URL-osoitteen. |

## <a name="site-settings"></a>Toimipaikan asetukset

Myymälän valintamoduuli noudattaa [Lisää tuote ostoskoriin -asetuksia](add-cart-settings.md). Kun ostoskoriin lisätään nimike myymälän valitsinmoduulista, sivuston käyttäjät näkevät asiaankuuluvat määritetyt työnkulut.

## <a name="add-a-store-selector-module-to-a-page"></a>Myymälän valitsinmoduulin lisääminen sivulle

**Nouto myymälästä** -tilassa moduulia voi käyttää vain PDP:n ja ostoskorisivun avulla. Määritä tilaksi **Nouto myymälästä** moduulin ominaisuusruudussa.

- Lisätietoja myymälän valitsinmoduulin lisäämisestä ostomoduuliin on kohdassa [Ostomoduuli](add-buy-box.md). 
- Lisätietoja myymälän valitsinmoduulin lisäämisestä ostoskorimoduuliin on kohdassa [Ostoskorimoduuli](add-cart-module.md)

Voit määrittää myymälöiden valitsinmoduulin aiemmin tämän artikkelin kuvassa osoitetulla tavalla. Tämän jälkeen myymälöiden sijaintien sivulla näkyvät käytettävissä olevat myymälät.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Markkinointimalli** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Myymälöiden sijainnit** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdassa luomasi **Markkinointimalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**. 
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Kontti ja 2 saraketta** -moduuli ja valitse sitten **OK**.
1. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Määritä **Erittäin pienen näkymäportin sarakkeen määritys** -kohdan arvoksi **100 %**.
1. Määritä **Pienen näkymäportin sarakkeen määritys** -kohdan arvoksi **100 %**.
1. Määritä **Keskikokoisen näkymäportin sarakkeen määritys** -kohdan arvoksi **33 % 67 %**.
1. Määritä **Suuren näkymäportin sarakkeen määritys** -kohdan arvoksi **33 % 67 %**.
1. Valitse **Kontti ja 2 saraketta** -paikassa kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.
1. Määritä moduulin ominaisuusruudussa **Tila**-kohdan arvoksi **Etsi myymälät**.
1. Määritä **Hakusäde**-arvo maileina.
1. Määritä halutessasi muita ominaisuuksia, kuten **Määritä ensisijaiseksi myymäläksi**, **Näytä kaikki myymälät** ja **Ota käyttöön automaattiset ehdotukset**.
1. Valitse **Kontti ja 2 saraketta** -paikassa kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kartta**-moduuli ja valitse sitten **OK**.
1. Määritä moduulin ominaisuusruudussa haluamiasi lisäominaisuuksia.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
 
## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[PDP:n esittely](quick-tour-pdp.md)

[Ostoskorin ja kassan pikaesittely](quick-tour-cart-checkout.md)

[Määritä toimitustavat](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Bing Maps -karttapalvelun hallinta organisaatiossa](dev-itpro/manage-bing-maps.md)

[Bing Maps REST -ohjelmointirajapinta](/bingmaps/rest-services/)

[Kartat-moduuli](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
