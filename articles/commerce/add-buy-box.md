---
title: Ostoruutumoduuli
description: Tässä artikkelissa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 7a3dfa347aac7b1ee7b318761c873beef8322bd9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270506"
---
# <a name="buy-box-module"></a>Ostoruutumoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Termi *ostoruutu* viittaa yleensä tuotetietosivun (PDP) alueeseen, joka on sivun yläosassa ja joka isännöi kaikkein tärkeimpiä tuotteen ostamisessa tarvittavia tietoja. (Alue, joka näkyy, kun sivu ladataan ensimmäisen kerran. Näin käyttäjien ei tarvitse vierittää sivua alaspäin nähdäkseen tiedot.)

Ostoruutumoduuli on erityinen säilö, jota käytetään kaikkien tuotetietosivun ostoruutualueella näkyvien moduulien isännöinnissä.

Tuotetietosivun URL-osoite sisältää tuotteen tunnuksen. Kaikki ostoruudun hahmontamisessa vaadittavat tiedot saadaan tästä tuotteen tunnuksesta. Jos tuotteen tunnusta ei ole annettu, ostoruutumoduulia ei hahmonneta sivulla oikein. Tämän vuoksi ostoruutumoduulia voidaan käyttää vain sivuilla, joilla on tuotekonteksti. Jos sitä halutaan käyttää sivulla, jolla ei ole tuotekontekstia (kuten aloitus- tai markkinointisivulla), sitä mukautettava lisää.

Seuraavassa kuvassa näkyy esimerkki ostoruutumoduulista tuotetietosivulla.

![Esimerkki ostoruutumoduulista.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Ostoruutumoduulin ominaisuudet ja paikat 

Ostoruutu jaetaan tuotetietosivulla kahteen alueeseen: media-alue vasemmalla ja sisältöalue oikealla. Oletusarvoisesti media-aluesarakkeen leveyden ja sisältöaluesarakkeen leveyden välinen suhde on 2:1. Mobiililaitteissa nämä kaksi aluetta pinotaan niin, että alueet näkyvät allekkain. Sarakeleveyksiä ja pinoamisjärjestystä voi mukauttaa teemojen avulla.

Ostoruutumoduuli hahmontaa tuotteen otsikon, kuvauksen, hinnan ja luokitukset. Lisäksi asiakkaat voivat valita sen avulla tuotevariantit, joilla on eri tuotemääritteet, kuten koko, tyyli ja väri. Kun tuotevariantti on valittuna, muut ostoruudun ominaisuudet (esimerkiksi tuotteen kuvaus ja kuvat) päivitetään muuttujan tietojen mukaisiksi. 

Asiakkaat voivat määrittää annetun määrävalitsimen avulla ostettavien nimikkeiden määrän. Sivuston asetuksissa voidaan määrittää suurin sallittu ostomäärä.

Asiakkaat voivat suorittaa ostoruudussa myös muita toimintoja, kuten lisätä tuotteen ostoskoriin tai toivelistalle ja valita noutosijainnin. Nämä toiminnot voidaan tehdä tuotteen tai tuotevariantin kohdalla. Jos asiakas haluaa lisätä tuotteen toivelistaan, hänen on oltava kirjautuneena sisään.

Teemojen avulla voidaan poistaa ostoruudun tuoteominaisuuksien ja toimintojen ohjausobjekteja tai muuttaa niiden järjestystä. 

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Otsikon tunniste** – Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen. Jos ostoruutu on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **h1**. 

- **Vastaavien tuotteiden ostosuositusten ottaminen käyttöön** - Tämän ominaisuuden avulla ostoruudussa voidaan näyttää linkkejä tuotteisiin, jotka ovat vastaavia kuin tällä hetkellä esillä oleva nimike. Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.13 ja uudemmissa versioissa.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduulit, joita voidaan käyttää ostoruutumoduulissa

- **Mediavalikoima** – Tämän moduulin avulla esitellään tuotteen kuvat tuotetietosivulla. Lisätietoja tästä moduulista on kohdassa [Mediavalikoimamoduuli](media-gallery-module.md).
- **Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa. Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin. Lisätietoja tästä moduulista on kohdassa [Myymälävalitsinmoduuli](store-selector.md).
- **Jako yhteisöpalveluissa** - Jos tämä moduuli lisätään ostoruutuun, käyttäjät voivat jakaa tuotetietoja yhteisöpalveluissa. Lisätietoja on kohdassa [Jako yhteisöpalveluissa -moduuli](social-share-module.md).

## <a name="buy-box-module-settings"></a>Ostoruutumoduulin asetukset

Seuraavat ostoruutumoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:

- **Ostoskorin rivien maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä. Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.
- **Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).
- **Lisää tuote ostoskoriin** – Katso lisätietoja **Lisää tuote ostoskoriin** -asetusten käyttöönotosta kohdasta [Lisää tuote ostoskoriin -asetukset](add-cart-settings.md).

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Ostoruutumoduulin määritelmälaajennukset Adventure Works -teemassa

Adventure Works -teeman tarjoamalla ostosuruutumoduulilla on moduulin määritelmälaajennus, joka tukee tuotemääritysmoduulin toteutusta PDP-sivun ostosruudun haitarimoduulissa. Jos haluat esitellä tuotemääritysten määritteitä PDP-sivun ostoruudussa, lisää tuotemääritysmoduuli ostoruudun haitarimoduulin paikkaan.


> [!IMPORTANT]
> Adventure Works -teema on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.


## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Ostoruutumoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen (API) avulla. Tuotetietosivulla olevaa tuotteen tunnusta käytetään kaikkien tietojen noutamisessa.

## <a name="add-a-buy-box-module-to-a-page"></a>Ostoruutumoduulin lisääminen sivulle

Voit lisätä ostoruutumoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi osa** -valintaikkunassa **Ostoruutu**-moduuli.
1. Kirjoita **Osan nimi** -kohtaan **Ostoruudun osa** ja valitse sitten **OK**.
1. Valitse ostoruutumoduulissa **Mediavalikoima**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Mediavalikoima**-moduuli ja valitse sitten **OK**.
1. Valitse ostoruutumoduulissa **Myymälävalitsin**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **PDP-malli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Valitse katkelma** -valintaikkunassa aiemmin luotu **Ostoruutuosa** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **PDP-sivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdan alla **PDP-malli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**.
1. Valitse uudella sivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Valitse katkelma** -valintaikkunassa aiemmin luotu **Ostoruutuosa** ja valitse sitten **OK**.
1. Tallenna ja esikatsele sivu. Lisää **?productid=&lt;tuotteen tunnus&gt;** -kyselymerkkijonoparametri esikatselusivun URL-osoitteeseen. Näin tuotekontekstia käytetään esikatselusivun lataamiseen ja käsittelemiseen.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**. Tuotetietosivulla näkyy ostoruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Mediavalikoimamoduuli](media-gallery-module.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)

[Yhteisöpalvelujakamisen moduuli](social-share-module.md)

[Lisää tuote ostoskoriin -asetukset](add-cart-settings.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
