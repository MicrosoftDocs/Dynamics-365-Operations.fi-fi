---
title: Hakutulosmoduuli
description: Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919471"
---
# <a name="search-results-module"></a>Hakutulosmoduuli

[!include [banner](includes/banner.md)]


Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Hakutulosmoduuli palauttaa tuotehaun tulokset ja luettelon tuotteisiin käytettävistä tarkennuksista. Dynamics 365 Commerce -sivustojen hakutulosmoduulien avulla voit muodostaa sivuja seuraavissa tilanteissa:

- Käyttäjähaun käynnistämät hakutulokset
- Hakutulokset, jotka näyttävät tietyn tuotejoukon, kuten "Ota samankaltaisia tuotteita"
- Luettelo tuotteista, jotka kuuluvat luokkaan

Lisätietoja luokka- ja hakutulossivuista on ohjeessa [Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md).

Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston luokan hakutulossivusta.

![Esimerkki hakutulossivusta Fabrikam-sivustolla.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Hakutulosmoduulin ominaisuudet

Seuraavassa taulukossa luetellaan hakutulosmoduulien ominaisuudet sekä niiden arvot ja kuvaukset.

| Ominaisuus | Arvot | kuvaus |
|----------|--------|-------------|
| Tuotteita sivulla | Kokonaisluku | Kullakin sivulla näkyvien nimikkeiden määrä. |
| Salli varmuuskopiointi PDP-kohteessa | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi määritetään **Tosi**, kun käyttäjä valitsee tuotteen hakutulossivulta, avautuvan tuotetietosivun (PDP) siirtymispolku näyttää Takaisin tuloksiin -linkin. |
| Laajenna tarkennukset | **Kaikki**, **1**, **2**, **3** tai **4** | Tärkeimpien tarkentajien määrä, jotka tulisi laajentaa, kun sivu ladataan. Jos ominaisuuden arvoksi määritetään esimerkiksi **3**, sivun ensimmäiset kolme tarkentajaa laajennetaan. |
| Piilota luokkahierarkian näyttö | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, sivulla näkyvä luokkahierarkia piilotetaan. Tämän ominaisuuden arvoksi tulee määrittää **Tosi**, jos luokkahierarkian näyttämiseen käytetään [siirtymispolkumoduulia](add-breadcrumb.md).|
| Sisällytä tuotemääritteet hakutuloksiin | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, tuotteiden määritteet palautetaan hakutuloksissa. Vaikka nämä määritteet voidaankin näyttää Commerce-sivustossa, laajennus on pakollinen.|
| Näytä liitoksen hinnat | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi määritetään **Tosi**, tuotteiden liittyvät hinnat näkyvät tuloksissa, kun kirjautunut käyttäjä selaa sivua. |
| Päivitä tarkentajapaneeli | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, tarkentajapaneeli päivitetään, kun tarkentajat valitaan. Tässä tilassa jotkin monivalintaiset tarkentajat käyttäytyvät kuin yhden valinnan tarkentajat, kun tarkentajapaneeli päivitetään. |

> [!IMPORTANT]
> Commercen versiossa 10.0.16 ja sitä myöhemmissä versioissa **Näytä liittyvät hinnat** -konfiguraatiota voidaan käyttää liittyvien hintojen näyttämiseen sivulla.
>
> Commerce version 10.0.20 -versiossa ja sitä myöhemmässä versiossa **päivitys tarkentajapaneeliin** -konfiguraatiota voidaan käyttää päivittämään tarkentajapaneelin valinnan aikana.

## <a name="supported-modules"></a>Tuetut moduulit

Hakutulosmoduuli tukee [pikanäkymämoduulia](quick-view-module.md), jonka avulla käyttäjät voivat tarkastella tuotetietoja ja lisätä nimikkeitä ostoskoriin hakutulossivulta.

## <a name="add-a-search-results-module-to-a-category-page"></a>Hakutulosmoduulin lisääminen luokkasivulle

Voit lisätä luokkasivulle hakutulosmoduulin seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunassa nimi **Hakutulokset** ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (...) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.
1. Anna sitten **Navigointipolku**-omiansiuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Hakutulokset**-moduuli ja valitse sitten **OK**.
1. Kirjoita **Hakutulokset**-ominaisuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä** ja määritä sitten muut hakutulosmoduulin pakolliset ominaisuudet. Kun määrität nämä ominaisuudet malliin, varmistat, että tietyn luokkasivun mukautukset sisältävät nämä asetukset automaattisesti.
1. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa luomasi **Hakutulokset**-malli, kirjoita **sivun nimeksi** **Luokkasivu** ja valitse sitten **OK**. Koska kaikki arvot on määritetty mallissa, sivu on valmis julkaistavaksi.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Varastotietoisuuden käyttöönotto hakutulosmoduulissa

Asiakkaat yleensä odottavat, että sähköisen kaupankäynnin sivusto on varastotietoinen selauskokemuksen eri osissa, jotta he voivat päättää, mitä tehdä, jos tuotetta ei ole varastossa. Hakutulosmoduulia voidaan parantaa siten, että se sisältää varastotietoja, ja tarjoaa seuraavat kokemukset:

- Näyttää varastosaatavuusotsikon tuotteiden yhteydessä.
- Varastosta loppuneiden tuotteiden piilotus.
- Näytä varastosta loppuneet tuotteet hakutulosluettelon lopussa.
    
Näiden kokemusten käyttöönottoa varten on määritettävä seuraavat edellytysasetukset Commerce-pääkonttorisovelluksessa.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Parannetun varastotietoisen sähköisen kaupankäynnin tuotteiden etsintäominaisuuden käyttöönotto

> [!NOTE]
> **Parannettu varastotietoinen sähköisen kaupankäynnin tuotteiden etsintä** -ominaisuus on käytettävissä Commercen version 10.0.20 julkaisusta alkaen.

**Parannettu varastotietoinen sähköisen kaupankäynnin tuotteiden etsintä** -ominaisuus otetaan käyttöön Commerce-pääkonttorisovelluksessa seuraavasti.

1. Valitse **Työtilat \> Ominaisuuden hallinta**.
1. Hae **Parannettu varastotietoinen sähköisen kaupankäynnin tuotteiden etsintä** -ominaisuutta ja ota se käyttöön.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Täytä tuotemääritteisiin varastotaso -tehtävän määrittäminen

**Täytä tuotemääritteisiin varastotaso** -tehtävä luo uuden tuotemääritteen, jolla taltioidaan varastosaatavuus, ja määrittää tämän määritteen sitten kunkin päätuotteen viimeisimpään varastotason arvoon. Koska myytävän tuotteen tai valikoiman varastosaatavuus muuttuu jatkuvasti, suosittelemme vahvasti tehtävän ajoittamista eräprosessin muodossa.

**Täytä tuotemääritteisiin varastotaso** -tehtävä määritetään Commerce-pääkonttorisovelluksessa seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Tuotteet ja varasto**.
1. Valitse **Täytä tuotemääritteisiin varastotaso**.
1. Toimi **Täytä tuotemääritteisiin varastotaso** -valintaikkunassa seuraavasti:

    1. Määritä **Parametrit**-kohdan **Tuotemääritteen ja tyypin nimi** -kentässä nimi erilliselle tuotemääritteelle, joka luodaan taltioimaan varastosaatavuus.
    1. Valitse **Parametrit**-kohdan **Varastosaatavuuden peruste** -kentässä määrä, johon varastotason laskenta perustuu (esimerkiksi **Saatavissa oleva fyysinen**).
    1. Määritä **Suorita taustalla** -kohdassa tehtävä suoritettavaksi taustalla ja ota valinnaisesti käyttöön **Eräkäsittely**-asetus. 

> [!NOTE]
> Jotta varastotaso laskettaisiin yhdenmukaisesti sähköisen kaupankäynnin sivuston PDP-sivuilla ja tuoteluettelosivuilla, valitse sama määräasetus sekä Commerce-pääkonttorisovelluksen **Varastosaatavuuden peruste** -asetuksessa että Commercen sivunmuodostimen **Varastotason peruste** -asetuksessa. Lisätietoja varastoasetusten ottamisesta käyttöön sivunmuodostimessa: [Varastoasetusten käyttäminen](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Uuden tuotemääritteen määrittäminen

Kun **Täytä tuotemääritteisiin varastotaso** -tehtävä on suoritettu, juuri luotu tuotemäärite on määritettävä sillä sähköisen kaupankäynnin sivustolla, jossa haluat ottaa hakutulosmoduulin varastotietoisuuden käyttöön.

Uusi tuotemäärite määritetään Commerce-pääkonttorisovelluksessa seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet** ja valitse sitten sähköisen kaupankäynnin sivusto.
1. Valitse ja avaa liittyvä määriteryhmä, lisää juuri luotu tuotemäärite siihen ja sulje sivu.
1. Valitse **Määritä määritteen metatiedot**, valitse juuri lisätty tuotemäärite ja ota sitten käyttöön asetukset **Näytä määrite kanavassa**, **Noudettavissa**, **Voidaan tarkentaa** ja **Voidaan kysellä**.

> [!NOTE]
> Hakutulosmoduulissa näkyvien tuotteiden varastotaso syötetään päätuotetasolla yksittäisen varianttitason sijaan. Sillä on vain kaksi mahdollista arvoa: "saatavilla" ja "loppu varastosta". Arvojen todellinen teksti haetaan [varastotason profiilin](inventory-buffers-levels.md) määritelmästä. Päätuotteen katsotaan loppuneen varastosta vain, kun kaikki sen variantit ovat loppuneet varastosta. Variantin varastotaso määritetään tuotteen varastotason profiilin määritelmän perusteella. 

Kun kaikki edeltävät määritysvaiheet on suoritettu, hakutulossivujen tarkennukset näyttävät varastopohjaisen suodattimen ja hakutulosmoduuli hakee varastotiedot taustalla. Tämän jälkeen voit määrittää Commercen sivunmuodostimen **Tuoteluettelosivujen varastoasetukset** -asetuksen, jolla hallitaan sitä, miten hakutulosmoduuli näyttää varastosta loppuneet tuotteet. Lisätietoa kohdassa [Varastoasetusten käyttöönotto](inventory-settings.md).

## <a name="additional-resources"></a>Lisäresurssit

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Pikanäkymämoduuli](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
