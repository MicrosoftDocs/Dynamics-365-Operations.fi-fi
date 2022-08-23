---
title: Hakutulosmoduuli
description: Tässä artikkelissa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: d10e9ed78dfc90833ff3c09021f863f6ef0b80d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286807"
---
# <a name="search-results-module"></a>Hakutulosmoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

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

Lisää hakutulosmoduuli luokkasivulle sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunassa nimi **Hakutulokset** ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (...) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Navigointipolku**-moduuli ja valitse sitten **OK**.
1. Anna sitten **Navigointipolku**-omiansiuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Hakutulokset**-moduuli ja valitse sitten **OK**.
1. Kirjoita **Hakutulokset**-ominaisuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä** ja määritä sitten muut hakutulosmoduulin pakolliset ominaisuudet. Kun määrität nämä ominaisuudet malliin, varmistat, että tietyn luokkasivun mukautukset sisältävät nämä asetukset automaattisesti.
1. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Luokkasivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdassa luomasi **Hakutulokset**-malli ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Varastotietoisuuden käyttöönotto hakutulosmoduulissa

Asiakkaat yleensä odottavat, että sähköisen kaupankäynnin verkkosivusto on varastotietoinen selauskokemuksen eri osissa, jotta he voivat päättää, mitä tehdä, jos tuotetta ei ole varastossa. Hakutulosmoduulia voidaan määrittää sisältämään varastotietoja, ja tarjoamaan seuraavat kokemukset:

- Näyttää varastosaatavuusotsikon tuotteen yhteydessä.
- Piilota varastosta loppuneet tuotteet tuoteluettelosta.
- Näytä varastosta loppuneet tuotteet tuoteluettelon lopussa.
- Suodata tuotteet hakutuloksissa varastotason mukaan.

Ennen kuin voit ottaa nämä kokemukset käyttöön , sinun on otettava **Parannettu sähköisen kaupankäynnin tuotteiden etsintä, joka ottaa varaston huomioon** -ominaisuus käyttöön **ominaisuudenhallinnan** työtilassa.

> [!NOTE]
> **Parannettu varastotietoinen sähköisen kaupankäynnin tuotteiden etsintä** -ominaisuus on käytettävissä Commercen version 10.0.20 julkaisusta alkaen.

Varastotietoinen tuotehaku käyttää tuotemääritteitä varaston käytettävyyden tietojen saamista varten. Toiminnon edellytyksenä on, että erilliset tuotemääritteet luodaan, niille on syötettävä varastotiedot ja ne on lisättävä online-kanavaan. 

Noudattamalla seuraavia ohjeita voit luoda erillisiä tuotemääritteitä, jotka tukevat varastotietoista hakutulosmoduulia.

1. Siirry headquartersissa kohtaan **Jälleenmyynti ja kaupankäynti \> Vähittäismyynnin ja kaupankäynnin IT \> Tuotteet ja varasto**.
1. Valitse ja avaa **Täytä tuotemääritteisiin varastotaso**.
1. Lisää seuraavat tiedot valintaikkunassa:

    1. Määritä **Tuotemääritteen ja tyypin nimi** -kentässä nimi erilliselle tuotemääritteelle, joka luodaan taltioimaan varastotiedot.
    1. Valitse **Varastosaatavuuden peruste** -kentässä määrätyyppi, johon varastotason laskenta perustuu (esimerkiksi **Saatavissa oleva fyysinen**). 

1. Suorita työ taustalla. Koska tuotteen varastosaatavuus muuttuu jatkuvasti monikanavaisessa ympäristössä, suosittelemme vahvasti tehtävän ajoittamista eräprosessin muodossa.

> [!NOTE]
> Jotta varastotaso laskettaisiin yhdenmukaisesti sähköisen kaupankäynnin sivuston sivuilla ja moduuleissa, valitse sama määrätyyppi sekä Commerce-pääkonttorisovelluksen **Varastosaatavuuden peruste** -asetuksessa että Commercen sivunmuodostimen **Varastotason peruste** -asetuksessa. Lisätietoja varastoasetusten ottamisesta käyttöön sivunmuodostimessa: [Varastoasetusten käyttäminen](inventory-settings.md).

Voit konfiguroida online-kanavan tuotemääritteet noudattamalla seuraavia vaiheita. 

1. Pääkonttorissa valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse online-kanava, jolle varastotietoinen hakutulosmoduuli luodaan.
1. Valitse ja avaa liittyvä määriteryhmä, ja lisää sitten juuri luotu tuotemäärite siihen.
1. Valitse Commerce-versiota 10.0.27 vanhemmissa versioissa **Määritä määritteen metatiedot**, valitse juuri lisätty tuotemäärite ja ota sitten käyttöön asetukset **Näytä määrite kanavassa**, **Noudettavissa**, **Voidaan tarkentaa** ja **Voidaan kysellä**.
1. Siirry kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1150 (luettelo)**. Jos ajoitat **Täytä tuotemääritteisiin varastotaso** -työn eräkäsittelynä, on suositeltavaa ajoittaa 1150-työ myös eräkäsittelyksi, joka suoritetaan samalla tiheydellä.

> [!NOTE]
> Hakutulosmoduulissa näkyvien tuotteiden varastotaso näytetään päätuotetasolla yksittäisen varianttitason sijaan. Sillä on vain kaksi mahdollista arvoa: "saatavilla" ja "loppu varastosta". Arvon todellinen selite haetaan [varastotason profiilin](inventory-buffers-levels.md) määritelmästä. Päätuotteen katsotaan loppuneen varastosta vain, kun kaikki sen variantit ovat loppuneet varastosta.

Kun kaikki edeltävät määritysvaiheet on suoritettu, hakutulossivujen tarkennukset näyttävät varastopohjaisen suodattimen ja hakutulosmoduuli hakee varastotiedot taustalla. Tämän jälkeen voit määrittää Commercen sivunmuodostimen **Tuoteluettelosivujen varastoasetukset** -asetuksen, jolla hallitaan sitä, miten hakutulosmoduuli näyttää varastosta loppuneet tuotteet. Lisätietoa kohdassa [Varastoasetusten käyttöönotto](inventory-settings.md).

## <a name="additional-resources"></a>Lisäresurssit

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Pikanäkymämoduuli](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
