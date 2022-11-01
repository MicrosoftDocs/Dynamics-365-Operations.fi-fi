---
title: Myyntitilauksen toimituspäivien laskeminen saatavuudella
description: Saatavuus-toiminnolla voit antaa asiakkaille realistisia päivämääriä, jolloin voit luvata tiettyjä tuotteita. Tässä artikkelissa kuvaillaan, kuinka saatavuus määritetään ja kuinka sitä käytetään kullekin suunnittelumoduulille (suunnittelun optimointi ja sisäinen moduuli).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3b8e3dc9f0e7aaf019aa4d7284458206e7daadb2
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714857"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Myyntitilauksen toimituspäivien laskeminen saatavuudella

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Saatavuus-toiminnolla voit antaa asiakkaille realistisia päivämääriä, jolloin voit luvata tiettyjä tuotteita. Voit määrittää kullekin myyntiriville päivämäärän, jossa otetaan huomioon käytettävissä oleva varasto, tuotantokapasiteetti ja kuljetusajat.

Saatavuus laajentaa [Luvattavissa oleva määrä](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) -toimintoja ottamalla huomioon kapasiteettitiedot. ATP ottaa huomioon vain materiaalin saatavuuden ja olettaa, että kapasiteetit ovat rajattomia, kun taas saatavuudessa sekä raaka-aineiden että kapasiteetin saatavuus otetaan huomioon. Näin ollen se antaa realistisemman kuvan siitä, voiko kysyntää täyttää tietyn ajan kuluessa.

Saatavuus toimii hieman eri tavalla riippuen käyttämästäsi pääsuunnittelumoduulista (suunnittelun optimointi vai sisäinen moduuli). Tässä artikkelissa käsitellään sen määrittämistä kullekin moduulille. Saatavuus (CTP) suunnittelun optimointia varten tukee tällä hetkellä vain saatavuuden skenaarioiden alijoukkoa, joita sisäinen moduuli tukee.

## <a name="turn-on-ctp-for-planning-optimization"></a>Ota käyttöön saatavuus suunnittelun optimointia varten

Saatavuus sisäiselle pääsuunnittelumoduulille on aina saatavana. Jos kuitenkin haluat käyttää suunnittelun optimoinnissa saatavauutta, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Pääsuunnittelu*
- **Ominaisuuden nimi:** *(Esiversio) Saatavuus (CTP) suunnittelun optimointia varten*

## <a name="how-ctp-compares-to-atp"></a>Saatavuuden (CTP) vertautuminen ATP:hen

Saatavuus ja ATP ovat samankaltaisia, mutta saatavuuden tulokset voivat usein olla tarkempia, kuten seuraavassa esimerkissä näkyy.

Nimike A on nimike, joka koostuu nimikkeistä B ja C, ja nimikkeen A käytettävissä oleva määrä on 0 (nolla). Jos teet ATP-tarkastuksen, jossa otetaan huomioon vain materiaalit, ATP-määrä on myös 0 (nolla). Jos kuitenkin teet saatavuuden tarkistuksen, järjestelmä tarkistaa nimikkeiden B ja C saatavuuden, tarkistaa ne resurssit, joita tarvitaan niiden tekemiseen nimikkeeksi A, ja laskee, kuinka monta nimikettä A voidaan tehdä. Lisäksi saatavuuslaskenta voi tarkistaa resurssit ja materiaalit, joita tarvitaan nimikkeiden B ja C lisäämiseen, ja käyttää niitä lisänimikkeiden A tekemiseen.

Sekä materiaalit että resurssit huomioon ottava saatavuuslaskelma voi näyttää suuremman määrän kuin laskelma, jossa tarkistetaan vain materiaalit, erityisesti silloin, kun tarkistettava nimike on tilausta varten koottava nimike. Toisin sanoen saatavuustoiminto perustuu hajotustoimintoon, ja se voidaan suorittaa valitulle myyntitilausriville odotetun toimituspäivän laskettavaksi.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Kuinka saatavuus vaihtelee käytettävän pääsuunnittelumoduulin mukaan

Seuraavassa taulukossa on yhteenveto saatavuuden (CTP) suunnittelun optimointia varten ja saatavuuden sisäiselle pääsuunnittelumoduulille välisistä eroista.

| Elementti | Suunnittelun optimointi | Sisäinen pääsuunnittelumoduuli |
|---|---|---|
| Tilausten, tilausrivien ja tuotteiden **Toimituspäivän tarkistus** -asetus | *Saatavuus (CTP) suunnittelun optimointia varten* | *Saatavuus* |
| Laskenta-aika | Laskenta käynnistetään ajamalla dynaaminen suunnitelma ajoitetuksi tehtäväksi. | Laskenta käynnistyy heti aina, kun lisäät myyntitilausrivin tai päivität sitä. |
| **Saatavuus (CTP) suunnittelun optimointia varten** -kentän arvo | <p>*Ei valmis* -arvo näytetään tilauksille ja tilausriveille, joilla dynaamista suunnitelmaa ei ole suoritettu tilausten ja rivien luomisen tai edellisen päivityksen jälkeen.</p><p>*Valmis*-arvo näytetään tilauksille ja riveille, joilla saatavuuden avulla on laskettu vahvistetut toimituspäivämäärät suorittamalla dynaaminen suunnitelma.</p> | Näkyvissä on aina *Valmis*-arvo. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Aseta oletustoimituspäivämäärän tarkistusmenetelmät

Järjestelmä voi käyttää mitä tahansa useista menetelmistä kunkin tilauksen ja tilausrivin toimituspäivämääräarvioiden laskemiseen. Määritä toimituspäivän tarkistusmenetelmä, jota haluat käyttää useimmiten yleisenä oletusmenetelmänä. Voit myös määrittää yleisiä ohituksia kullekin tuotteelle. Voit myöhemmin ohittaa kunkin tilauksen ja/tai tilausrivin oletusmenetelmät tarpeen mukaan.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Aseta yleinen oletustoimituspäivämäärän tarkistus

Oletustoimituspäivän tarkistusmenetelmää käytetään kaikille uusille tilausriveille, joissa ohitus ei ole käytössä. Jos haluat valita yhden, toimi seuraavasti.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. Valitse **Lähetykset**-välilehden **Toimituksen tarkistus**-pikavälilehden **Toimituspäivän tarkistus** -kentästä menetelmä, jota haluat käyttää yrityksen oletusmenetelmänä:

    - *Ei mitään* – Älä laske toimituspäiviä.
    - *Myynnin läpimenoaika* – Myynnin läpimenoaika on myyntitilauksen luomisen ja nimikkeiden toimituksen välinen aika. Toimituspäivän laskenta perustuu päivien oletusmäärään eikä siinä oteta huomioon varastotilannetta, tiedettyä kysyntää eikä suunniteltua tarjontaa.
    - *Luvattavissa oleva määrä (ATP)* – ATP on nimikkeen käytettävissä oleva määrä, joka voidaan luvata asiakkaalle tiettynä päivänä. ATP-laskelmaan sisältyy varaamaton varasto, läpimenoajat, suunnitellut vastaanotot ja varasto-otot.
    - *ATP + toimitusmarginaali* – Lähetyspäivämäärä vastaa ATP-päivämäärää sekä nimikkeen toimitusmarginaalia. Toimitusmarginaali on lähetettävien nimikkeiden valmisteluun kuluva aika.
    - *Saatavuus (CTP)* – Käytä sisäisen pääsuunnittelumoduulin toimittamaa saatavuuslaskelmaa. Jos käytät suunnittelun optimointia, *saatavuuden (CTP)* toimituspäivän valvontamenetelmä ei ole sallittu, ja jos se on valittuna, se aiheuttaa virheen, kun laskenta suoritetaan.
    - *Saatavuus (CTP) suunnittelun optimointia varten* – Käytä suunnittelun optimoinnin mahdollistamia saatavuuslaskelmia. Tällä asetuksella ei ole vaikutusta, jos käytössä on sisäinen pääsuunnittelumoduuli.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Aseta toimituspäivän tarkistuksen ohitukset yksittäisille tuotteille

Voit määrittää ohitukset tietyille tuotteille, joissa haluat käyttää toimituspäivän tarkistusmenetelmää, jos se on muu kuin sellainen, joka on määritetty yleiseksi oletusmenetelmäksi.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, jonka haluat määrittää.
1. Valitse toimintoruudussa **Hallitse varastoa** -välilehden **Tilauksen asetukset** -ryhmästä **Tilauksen oletusasetukset**.
1. Määritä **Myyntitilaus**-pikavälilehden **Tilauksen oletusasetukset** -sivulla **Korvaa toimituksen tarkistus** -asetuksen arvoksi *Kyllä*.
1. Valitse **Toimituspäivän tarkistus** -kentästä menetelmä, jota valitulle tuotteelle käytetään. Samat asetukset, jotka on kuvattu [Aseta yleinen oletustoimituspäivämäärän tarkistus](#global-default) -osassa, ovat käytettävissä.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Saatavuus (CTP) suunnittelun optimointia varten -laskelmien ajoittaminen

Kun käytät Saatavuus (CTP) suunnittelun optimointia varten -toimintoa, järjestelmän on suoritettava dynaaminen suunnitelma, jotta järjestelmä käynnistetään suorittamaan saatavuuslaskelmat ja määrittää sitten kaikkien asiaankuuluvien tilausten vahvistetut lähetys- ja vastaanottopäivämäärät. Suunnitelmaan on sisällytettävä kaikki nimikkeet, joita varten tarvitaan vahvistettavat lähetys- ja vastaanottopäivämäärät. (Kun käytät saatavuutta sisäiselle suunnittelumoduulille, saatavuuslaskelmat tehdään välittömästi paikallisesti. Näin ollen dynaamista suunnitelmaa ei tarvitse suorittaa saatavuuden tulosten tarkastelemiseksi.)

On suositeltavaa määrittää erätyöt käyttämään suunnitelmia toistuvasti, jotta päivämäärät ovat kaikkien käyttäjien käytettävissä ajoissa. Jos esimerkiksi erätyö on määritetty suorittamaan dynaaminen suunnitelma 30 minuutin välein, vahvistettu lähetys- ja vastaanottopäivä määritetään 30 minuutin välein. Tämän vuoksi tilausten syöttävien ja tuovien käyttäjien on odotettava enintään 30 minuuttia saadakseen vahvistetut lähetys- ja vastaanottopäivät.

Kun haluat määrittää erätyön suorittamaan dynaamisen suunnitelman säännöllisesti, noudata seuraavia ohjeita.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Pääsuunnittelu**.
1. Määritä **Pääsuunnittelu**-valintaikkunan **Parametrit**-pikavälilehdessä **Pääsuunnitelma**-kenttään suoritettava dynaaminen suunnitelma.
1. Määritä **Suorita taustalla** -pikavälilehdessä **Erän käsittely** -kohdan arvoksi *Kyllä*.
1. Valitse **Toistuminen** ja määritä aikataulu tarpeen mukaan.
1. Valitse **OK** tallentaaksesi aikataulun.
1. Valitse **OK** luodaksesi erätyön. Sulje valintaikkuna.

## <a name="use-ctp-for-built-in-master-planning"></a>Käytä saatavuutta sisäiselle pääsuunnittelumoduulille

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Uuden tilauksen luominen käyttämällä saatavuutta sisäiselle pääsuunnittelumoduulille

Järjestelmä määrittää uuden myyntitilauksen tai tilausrivin lisäämisen yhteydessä oletustoimituspäivämäärän tarkistusmenetelmän. Tilauksen otsikko alkaa aina käyttäen yleistä oletusmenetelmää. Jos tilatulle nimikkeelle määritetään ohitus, uusi tilausrivi käyttää kyseistä ohitusta. Muussa tapauksessa uusi tilausrivi käyttää myös yleistä oletusmenetelmää. Siksi määritä oletusmenetelmät niin, että ne vastaavat toimituspäivän tarkistusmenetelmää, jota käytät useimmiten. Tilauksen luomisen jälkeen voit ohittaa oletusmenetelmän tilauksen otsikossa ja/tai tilausrivin tasolla tarpeen mukaan. Lisätietoja on kohdassa [Aseta oletustoimituspäivämäärän tarkistusmenetelmät](#default-methods) ja [Muuta aiemmin luodut myyntitilaukset käyttämään saatavuutta (CTP)](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Vahvistetut päivämäärät voidaan näyttää, kun käytät saatavuutta sisäiselle pääsuunnittelumoduulille

Jos käytössä on sisäinen pääsuunnittelumoduuli, saatavuuslaskentoja käytetään tilauksiin ja/tai tilausriveihin, joissa **Toimituspäivän tarkistus**- kentän arvoksi on määritetty *Saatavuus (CTP)*.

Jos myyntirivit käyttävät saatavuutta sisäiselle pääsuunnittelumoduulille, järjestelmä määrittää automaattisesti **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu vastaanottopäivämäärä**-kentät aina, kun myyntirivi tallennetaan. Jos myöhemmin teet asianmukaisen muutoksen myyntiriviin (esimerkiksi muuttamalla myyntirivin määrää tai toimipaikkaa), päivämäärät lasketaan heti uudelleen.

- Voit tarkastella myyntitilausrivin vahvistettuja toimituspäiviä avaamalla myyntitilauksen ja valitsemalla myyntirivin. Sitten tarkista **Toimitus**-välilehden **Rivin tiedot** -pikavälilehdessä **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu lähetyspäivämäärä** -kenttien arvot.
- Voit tarkastella koko tilauksen vahvistettuja toimituspäiviä avaamalla myyntitilauksen ja valitsemalla **Otsikko**-näkymän. Sitten tarkista **Toimitus**-välilehdessä **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu lähetyspäivämäärä** -kenttien arvot.

## <a name="use-ctp-for-planning-optimization"></a>Käytä saatavuutta (CTP) suunnittelun optimointia varten

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Uuden tilauksen luominen käyttämällä saatavuutta (CTP) suunnittelun optimointia varten

Järjestelmä määrittää uuden myyntitilauksen tai tilausrivin lisäämisen yhteydessä oletustoimituspäivämäärän tarkistusmenetelmän. Tilauksen otsikko alkaa aina käyttäen yleistä oletusmenetelmää. Jos tilatulle nimikkeelle määritetään ohitus, uusi tilausrivi käyttää kyseistä ohitusta. Muussa tapauksessa uusi tilausrivi käyttää myös yleistä oletusmenetelmää. Siksi määritä oletusmenetelmät niin, että ne vastaavat toimituspäivän tarkistusmenetelmää, jota käytät useimmiten. Tilauksen luomisen jälkeen voit ohittaa oletusmenetelmän tilauksen otsikossa ja/tai tilausrivin tasolla tarpeen mukaan. Lisätietoja on kohdassa [Aseta oletustoimituspäivämäärän tarkistusmenetelmät](#default-methods) ja [Muuta aiemmin luodut myyntitilaukset käyttämään saatavuutta (CTP)](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Vahvistettujen toimituspäivämäärien tarkasteleminen käytettäessä saatavuutta (CTP) suunnittelun optimointia varten

Jos käytössä on suunnittelun optimointi, saatavuuslaskentoja käytetään tilauksiin ja/tai tilausriveihin, joissa **Toimituspäivän tarkistus**- kentän arvoksi on määritetty *Saatavuus (CTP) suunnittelun optimointia varten*.

Jos myyntirivit käyttävät saatavuutta suunnittelun optimointia varten, **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu vastaanottopäivämäärä**-kentät ovat tyhjiä, kunnes suoritat asianmukaisen dynaamisen suunnitelman (tavallisesti käyttämällä kausittaista erätyötä). Tämän jälkeen ne määritetään automaattisesti. Lisätietoja on kohdassa [Saatavuus (CTP) suunnittelun optimointia varten -laskelmien ajoittaminen](#batch-job).

**Saatavuus (CTP) suunnittelun optimointia varten – tila** ilmaisee, onko vahvistetut päivämäärät laskettu jo jokaiselle saatavuutta suunnittelun optimointia varten käyttävälle riville. Kentässä näkyy arvo *Ei valmis* riveille ja tilauksille, joiden vahvistettuja toimituspäivämääriä ei ole vielä laskettu tai jotka eivät ole enää voimassa muiden muutosten vuoksi. Kentän arvo on *Valmis* riveille ja tilauksille, jotka on laskettu. Voit tarkastella kunkin rivin ja koko tilauksen tilaa.

- Voit tarkastella myyntitilausrivin tilaa avaamalla myyntitilauksen ja valitsemalla myyntirivin. Tarkista sitten **Toimitus**-välilehden **Rivin tiedot** -pikavälilehdessä **Saatavuus (CTP) suunnittelun optimointia varten – tila** -arvo. Myös rivin **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu vastaanottopäivä** -kentät näkyvät tässä välilehdessä, kun ne on laskettu.
- Voit tarkastella koko tilauksen tilaa avaamalla myyntitilauksen ja valitsemalla **Otsikko**-näkymän. Tarkista sitten **Toimitus**-pikavälilehdessä **Saatavuus (CTP) suunnittelun optimointia varten – tila** -arvo. Myös tilauksen **Vahvistettu lähetyspäivämäärä**- ja **Vahvistettu vastaanottopäivä** -kentät näkyvät tässä välilehdessä, kun ne on laskettu.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Jos päivität myyntitilausrivin, kun Saatavuus (CTP) suunnittelun optimointia varten on laskenut sille vahvistetut päivämäärät, järjestelmä tyhjentää päivämäärät siihen saakka, kunnes asianmukainen dynaaminen suunnitelma suoritetaan seuraavan kerran.
> - Jos muokkaat liittyvää asetusta, joka saattaa vaikuttaa aiemmin luotuihin vahvistettuihin päivämääriin (esimerkiksi muuttamalla läpimenoaikoja, varauksia tai merkintöjä), tyhjennä asianmukaisten tilausten vahvistetut päivämäärät. Tämä toimenpide muuttaa kunkin asiaankuuluvan rivin tilaksi *Ei valmis*. Tämä muutos taas aiheuttaa sen, että järjestelmä laskee vahvistetut päivämäärät uudelleen, kun se seuraavan kerran suorittaa dynaamisen suunnitelman.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Aiemmin luotujen myyntitilausten muuttaminen siten, että ne käyttävät saatavuutta

Voit muuttaa minkä tahansa avoimen tilauksen **Toimituspäivän tarkistus** -arvoa milloin tahansa. Voit muuttaa arvoa otsikkotasolla ja/tai jokaisella rivillä tarpeen mukaan.

### <a name="change-to-ctp-at-the-order-header-level"></a>Vaihda saatavuuteen tilauksen otsikkotasolla

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Jos haluat muuttaa tilausta niin, että se käyttää saatavuutta tilauksen otsikkotasolla, noudata seuraavia ohjeita.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.
1. Avaa määritettävä myyntitilaus tai luo uusi.
1. Valitse **Otsikko** avataksesi otsikon tiedot **Myyntitilauksen tiedot** -sivulla.
1. Määritä **Toimitus**-pikavälilehden **Toimituspäivän tarkistus** -kentän arvoksi jokin seuraavista arvoista käyttämäsi suunnittelumoduulin mukaan:

    - *Saatavuus (CTP)* – Käytä sisäisen pääsuunnittelumoduulin toimittamaa saatavuuslaskelmaa. Jos käytät suunnittelun optimointia, *saatavuuden (CTP)* toimituspäivämäärän tarkistusmenetelmä ei ole sallittu. Siksi jos valitset tämän arvon, laskennan suorituksessa tapahtuu virhe.
    - *Saatavuus (CTP) suunnittelun optimointia varten* – Käytä suunnittelun optimoinnin mahdollistamia saatavuuslaskelmia. Tällä asetuksella ei ole vaikutusta, jos käytössä on sisäinen pääsuunnittelumoduuli.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Ota muutokset käyttöön valitsemalla **OK**.

### <a name="change-to-ctp-at-the-order-line-level"></a>Vaihda saatavuuteen tilauksen rivitasolla

Jos olet luonut tilausrivin eri toimituspäivän tarkistusmenetelmän avulla, voit vaihtaa saatavuuteen milloin tahansa. Rivitasolla tekemäsi muutokset eivät vaikuta muihin riveihin. Yleistilauksen toimituspäivät voivat kuitenkin siirtyä eteenpäin tai taaksepäin sen mukaan, miten kukin päivitetty rivin laskenta muuttuu. <!-- KFM: Confirm this intro at next revision -->

Jos haluat muuttaa tilausta niin, että se käyttää saatavuutta sisäiselle pääsuunnittelumoduulille rivitasolla, noudata seuraavia ohjeita.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.
1. Avaa määritettävä myyntitilaus tai luo uusi.
1. Valitse **Myyntitilauksen tiedot** -sivun **Myyntitilausrivi**-pikavälilehdestä myyntitilausrivi, jonka haluat määrittää.
1. Määritä **Rivin tiedot** -pikavälilehden **Toimitus**-välilehdessä **Toimituspäivän tarkistus** -kentän arvoksi jokin seuraavista arvoista käyttämäsi suunnittelumoduulin mukaan:

    - *Saatavuus (CTP)* – Käytä sisäisen pääsuunnittelumoduulin toimittamaa saatavuuslaskelmaa. Jos käytät suunnittelun optimointia, *saatavuuden (CTP)* toimituspäivämäärän tarkistusmenetelmä ei ole sallittu. Siksi jos valitset tämän arvon, laskennan suorituksessa tapahtuu virhe.
    - *Saatavuus (CTP) suunnittelun optimointia varten* – Käytä suunnittelun optimoinnin mahdollistamia saatavuuslaskelmia. Tällä asetuksella ei ole vaikutusta, jos käytössä on sisäinen pääsuunnittelumoduuli.

    Näyttöön tulee **Käytettävissä olevat lähetys- ja vastaanottopäivämäärät** -valintaikkuna, jossa näkyvät käytettävissä olevat lähetys- ja vastaanottopäivät. Tämä valintaikkuna toimii samalla tavalla tilausriveillä kuin tilausotsikossa, kuten edellisessä osassa on kuvattu.

1. Valitse toimintoruudussa **Tallenna**.
