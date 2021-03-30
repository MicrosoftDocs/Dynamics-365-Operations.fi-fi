---
title: Poissulkevan konfiguraation määritepohjaiset myyntihinnat
description: Tässä ohjeaiheessa käsitellään sellaisten hintamallien muodostamista, joissa myyntihinnat perustuvat komponentteihin ja määritteisiin eikä fyysiseen tuoterakenteeseen ja reittiin.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65ab96c71fa44d6acad0bcb5cd7a65321109b93d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221964"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Poissulkevan konfiguraation määritepohjaiset myyntihinnat

Tässä ohjeaiheessa käsitellään sellaisten hintamallien muodostamista, joissa myyntihinnat perustuvat komponentteihin ja määritteisiin eikä fyysiseen tuoterakenteeseen ja reittiin. Kullekin tuotemääritysmallille voi muodostaa useita myyntihintamalleja.

## <a name="set-relevant-product-information-management-parameters"></a>Soveltuvien tuotetietojen hallintaparametrien määrittäminen

Ennen hintamallien muodostamisen aloittamista on määritettävä oletusvaluutta, jota käytetään myyntihintamalleja muodostettaessa. Voit myös valita, onko liitettävässä Microsoft Excel -tiedostossa tilauksen kaikkien rivien vai tarjousrivien hintaerittely. Hintaerittelyn avulla voidaan ilmaista tarkasti asiakkaalle, miten päädyttiin tiettyyn määritetyn tuotteen myyntihintaan.

Oletusvaluutan määrittäminen:

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotetietojen hallintaparametrit**.
1. Avaa **Rajoituspohjaiset tuotekonfiguraatiomallit** -välilehti
1. Avaa avattava **Oletusvaluutta**-luettelo ja valitse valuutta.

    ![Rajoituspohjaisen tuotekonfiguraation oletusvaluutan määrittäminen](media/prod-config-currency.png "Rajoituspohjaisen tuotekonfiguraation oletusvaluutan määrittäminen")

1. Jos halut liittää Excel-tiedoston, jossa on tilauksen kaikkien rivien tai tarjousrivien hintaerittely, määritä **Hintamalli**-osassa **Liitä**-asetukseksi *Kyllä*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Myyntihintamallien muodostaminen

Myyntihintamallin muodostaminen:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Valitse kohdetuotekonfiguraatiomalli.
1. Avaa toimintoruudussa **Malli**-välilehti ja valitse **Asetukset**-ryhmässä **Hintamallit**.
1. **Hintamallit**-sivu avautuu.
1. Valitse hintamalli tai lisää uusi malli ruudukkoon.
1. Avaa valitun mallin muokkaussivu valitsemalla **Muokkaa**. Sivulla on seuraavat ominaisuudet:
    - Valuutta näkyy lomakkeen otsikossa, ja voit lisätä uusia valuuttoja hinta-asetuksissa.
    - Tuotemallin kaikki komponentit ja käyttäjän vaatimukset näkyvät vasemmassa ruudussa. Jokaisessa tuotemallipuun solmussa voi olla yksi perushintalauseke ja valinnainen määrä lausekesääntöjä. Lausekesääntö kostuu ehdosta ja lausekkeesta, ja kukin lausekesääntö kattaa tuoteasetuksen, jolla voidaan hallita tuotteen hintaa.
    - Ehtoja ja lausekkeita muodostettaessa voit käyttää samoja operaattoreita, joita käytetään tuotemallin laskelmissa. Lauseke-editori tukee myös sekä ehtoja että lausekkeita.
1. Valitse vasemmassa sarakkeessa ensin solmu ja muodosta sitten sille hinnoittelusäännöt edellisessä vaiheessa kuvatuilla ominaisuuksilla. (Tutustu myös toimenpiteen jälkeen annettuun esimerkkiin.) Toista tämä vaihe tarvittaessa kunkin solmun osalta.

Seuraavassa esimerkissä on perushinta, jonka staattinen luku on 899,95 euroa. Tätä lukua voidaan muokata jollakin (tai useilla) seuraavista viidestä lausekesäännöistä asiakkaan valitseman määrityksen perusteella:

- Jos kaapissa valkoinen viimeistely, vähennä 59,95 euroa.
- Jos kulmat suojataan, lisää 35,95 euroa.
- Jos edessä metalliristikko, lisää 89,95 euroa.
- Jos kaapin palisanteriviimeistely, lisää 119,95 euroa.
- Lisää 12,95 euroa jokaiseen, kaiutinta varten korotettuun osaan.

![Hintamalliesimerkki](media/prod-config-rules-example.png "Hintamalliesimerkki")

## <a name="add-support-for-multiple-currencies"></a>Usean valuutan tuen lisääminen

Kun määritettävä tuote myydään, järjestelmä tarkistaa, onko hinnat määritetty nimenomaisesti asiakkaan valuuttana. Jos näin on, näitä nimenomaisia arvoja käytetään. Muussa tapauksessa järjestelmä käyttää valuutan vaihtokursseja, jotka on määritetty myyntiyritykselle oletusvaluutan arvon muuntamiseen asiakkaan valuutaksi.

Nimenomaisten hintojen lisääminen lisävaluutassa:

1. Avaa hintamallin muokkaussivu kohdan [Myyntihintamallien muodostaminen](#build-price-model) ohjeiden mukaisesti.
1. Avaa hintamallin otsikon **Lisää**-painikkeella avattava **Valuutat**-luettelo, joka sisältää käytettävissä olevat valuutat.
1. Valitse avattavaan **Valuutat**-luetteloon lisättävä valuutta ja valitse **OK**.
1. Avattavassa **Nykyinen valuutta** -luettelossa on nyt juuri lisätty valuutta sekä kaikki muuta mahdollisesti aiemmin lisätyt valuutat. Valitse uusi valuttaa ja kiinnitä huomiota siihen, että **Lausekesäännöt**-osan ruudukossa on nyt kaksi lausekekenttää:
    - **Lauseke** – näkyvissä on lauseke (tai rajoitusarvo), jolla etsitään hinta käyttämällä **Nykyinen valuutta** -kohdassa valittuna olevaa valuuttaa.
    - **Oletuslausekkeet** – näkyvissä on lauseke (tai rajoitusarvo), jolla etsitään hinta käyttämällä oletusvaluuttaa (joka näkyy **Oletusvaluutta**-kentässä).

    > [!NOTE]
    > Lausekesääntöjen **Ehto**-kentän omistaja on oletusvaluutta, joten muiden valuuttojen ehtoja ei voi muokata. Et voi myöskään lisätä uusia lausekesääntöjä, kun jokin muu kuin oletusvaluutta on valittuna **Nykyinen valuutta** -kohdassa.
1. Muokkaa nykyisen valuutan **Lauseke**-sarakkeen arvoja tarvittaessa.

Seuraavassa esimerkiksi _EUR_ on oletusvaluutta ja _USD_ on lisätty lisävaluuttana.

![Esimerkki useita valuuttoja sisältävästä mallista](media/prod-config-rules-currency-example.png "Esimerkki useita valuuttoja sisältävästä mallista")

> [!NOTE]
> Et voi lisätä vain muulle kuin oletusvaluutalle kuuluvia lausekesääntöjä. Jos haluat lausekesääntöjä, jotka koskevat vain muuta kuin oletusvaluuttaa, määritä oletusvaluutan hintalausekkeen arvoksi nolla. Määritä sitten sopiva lauseke muulle kuin oletusvaluutalle.

## <a name="test-your-price-model"></a>Hintamallin testaaminen

Voit testata myyntihintojen käyttöä määritysistunnossa avaamalla hintamallin muokkaussivun kohdan [Myyntihintamallien muodostaminen](#build-price-model) ohjeiden mukaisesti ja valitsemalla sitten toimintoruudussa **Testi**. Voit tehdä seuraavat toimet avautuvassa **Testaa tuotemallia** -valintaruudussa:

- Valitse tuotevaihtoehdot käytössä olevilla määritysasetuksilla ja tarkastele sitten, miten ne vaikuttavat **Hinta ja lähetyspäivä** -kohdassa näkyviin arvoihin.
- Valitsemalla **Näytä hintaerittely** voit ladata Excel-tiedoston, jossa on tarkat tiedot hinnan laskemisesta.

![Tuotemallin testaaminen](media/prod-config-test.png "Tuotemallin testaaminen")

Ladatussa laskentataulukossa näkyy sekä absoluuttinen arvo että kunkin aktiivisen hintaelementin prosenttiosuus. Jos **Liitä**-hintamalliasetus on määritetty **Tuotetietojen hallintaparametrit** -sivulla, tämä Excel-taulukko liitetään tilaus- tai tarjousriville.

![Hintaerittelyn sisältävä Excel-taulukko](media/prod-config-excel-example.png "Hintaerittelyn sisältävä Excel-taulukko")

## <a name="set-up-selection-criteria-for-price-models"></a>Hintamallien valintaehtojen määrittäminen

Kun hintamallit ovat valmiita, hintamallin poimintaa varten tarjouksen tai tilauksen määrittämisen yhteydessä on muodostettava ainakin yksi valintaehto. Se tehdään määrittämällä ainakin yksi kysely. Kyselyt ovat yhdessä vastaavien myyntihintamallien kanssa joustava tapa kohdistaa myyntihintoja tiettyjen asiakkaiden, alueiden, kausien ja muiden ehtojen perusteella.

Hintamallien valintaehtojen määrittäminen:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Valitse kohdetuotekonfiguraatiomalli.
1. Avaa toimintoruudussa **Malli**-välilehti ja valitse **Asetukset**-ryhmässä **Hintamallin ehdot**. **Hintamallin ehdot** -sivu avautuu.
1. Jos tarvittavaa kyselyriviä ei vielä ole, valitse toimintoruudussa **Uusi** ja lisää uusi riviruudukkoon. Määritä siinä myös seuraavat asetukset:
    - **Nimi** – anna riville nimi.
    - **Kuvaus** – anna lyhyt kyselyn ja sen tarkoituksen kuvaus.
    - **Hintamalli** – valitse [hintamalli](#build-price-model) (nykyisessä määritysmallissa), jota käynnistyvä kysely käyttää.
    - **Tilauksen tyyppi** – valitse tilauksen tyyppi, jossa kyselyä käytetään.
    - **Voimassaolo alkaa** – määritä ensimmäinen päivä, jolloin kyselyä käytetään.
    - **Vanhentuu** – määritä viimeinen päivä, jolloin kyselyä käytetään.

    ![Hintamalliehdot](media/prod-config-price-model-criteria.png "Hintamalliehdot")

1. Valitse kyselylle määritettävä rivi ja valitse sitten **toimintoruudussa** **Muokkaa**. Kyselyn suunnitteluohjelman valintaikkuna avautuu. Se toimii samalla tavoin useimmat kyselyn suunnitteluohjelmat Supply Chain Managementissa. Voit määrittää siinä ehdot, joiden mukaan valitun rivin hintamallia käytetään.

1. Toista vaiheet 4–5 kaikkien tarvittavien kyselyjen osalta.
    > [!TIP]
    > Voit säästää aikaa kopioimalla aiemmin luodun lisättävää riviä muistuttavan rivin. Tee se valitsemalla ensin kohderivi ja sitten toimintoruudussa **Monista**.

1. Kun ehtojen määritys on valmis, järjestä ne oikeaan järjestykseen **Hintamallin ehdot** -luettelossa. Voit muuttaa rivin paikka valitsemalla ensin sivun ja sitten **Ylös** tai **Alas** toimintoruudussa.

    > [!IMPORTANT]
    > Järjestelmä aloittaa haun määrityksen aikana luettelon yläreunasta ja käyttää ensimmäistä kyselyä, joka vastaa tarjous- tai tilausrivillä olevia tietoja. Tämän vuoksi tarkimmat kyselyt on asetettava ylimmäiseksi. Jos asetat yleisen kyselyn ylimmäiseksi luetteloon, sitä käytetään, vaikka alempana olisi tarkasti määrityksen asiakkaalle tai prospektille kohdistettu kysely.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Tuotemalliversion määritepohjaisten myyntihintojen määrittäminen

Viimeiseksi määritetään tuotemalliversion määritepohjaiset myyntihinnat. Toimi seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Valitse kohdetuotekonfiguraatiomalli.
1. Avaa toimintoruudussa **Malli**-välilehti ja valitse **Tuotemallin tiedot** -ryhmässä **Versiot**.
1. **Versiot** -sivu avautuu. Varmista, että **Hinnoittelumenetelmä**-asetuksena on **Määritepohjainen**.
    ![Hinnoittelumenetelmän määrittäminen määritepohjaiseksi](media/prod-config-versions.png "Hinnoittelumenetelmän määrittäminen määritepohjaiseksi")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]