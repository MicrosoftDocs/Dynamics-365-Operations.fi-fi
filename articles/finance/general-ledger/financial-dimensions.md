---
title: Taloushallinnon dimensiot
description: Tässä artikkelissa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä.
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9b07831ab789b570963ff5f425f149ba5a564a38
ms.sourcegitcommit: e700528679a821237e644b3e21058c36ae1323c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2022
ms.locfileid: "9680355"
---
# <a name="financial-dimensions"></a>Taloushallinnon dimensiot

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään erityyppisiä taloushallinnon dimensioita ja niiden määrittämistä.

Luo **Taloushallinnon dimensiot** -sivun avulla tilikartan tilisegmentteinä käytettäviä taloushallinnon dimensioita. Taloushallinnon dimensioita on kahdenlaisia: mukautettuja ja yksikön tukemia dimensioita. Mukautetut dimensiot jaetaan yritysten välillä, ja käyttäjät vastaavat arvojen antamisesta ja ylläpidosta. Arvot määritetään yksikön tukemille dimensioille muualla järjestelmässä, esimerkiksi Asiakkaat- tai Myymälät-yksiköissä. Jotkin yksikön tukemat dimensiot jaetaan yritysten välillä, kun taas toiset yksikön tukemat dimensiot ovat yrityskohtaisia.

Kun taloushallinnon dimensiot on luotu, voit liittää jokaiselle taloushallinnon dimensiolle lisää ominaisuuksia **Taloushallinnon dimension arvot** -sivulla.

Voit käyttää taloushallinnon dimensiota yritysten esittämiseen. Sinun ei tarvitse luoda yrityksiä Dynamics 365 Financessa. Taloushallinnon dimensioita ei kuitenkaan ole suunniteltu käsittelemään yritysten operatiivisia tai liiketoiminnan tarpeita. Financen yksiköiden välisen kirjanpidon toiminnallisuus on suunniteltu käsittelemään vain jokaisen tapahtuman luomat kirjanpitomerkinnät.

Ennen kuin määrität taloushallinnon dimensiot yrityksiksi, arvioi liiketoimintaprosessisi seuraavilla alueilla ja selvitä, voiko tätä asetusta käyttää organisaatiossasi:

- Varasto
- Myynnit ja ostot taloushallinnon dimensioiden ja yritysten välillä
- Arvonlisäveron laskenta ja ilmoittaminen
- Toiminnan raportointi

Seuraavassa on joitakin rajoituksia:

- Voit käyttää arvonlisäverotoimintoa ainoastaan yritysten kanssa, et taloushallinnon dimensioiden.
- Jotkin raportit eivät sisällä taloushallinnon dimensioita. Tämän vuoksi raportteja on ehkä muokattava taloushallinnon dimension mukaista raportointia varten.

## <a name="custom-dimensions"></a>Mukautetut dimensiot

Voit luoda käyttäjän määrittämän taloushallinnon dimension valitsemalla **Käytä arvoja kohteesta** -kentässä **Mukautettu dimensio**.

Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä. Voit antaa jokaisessa dimensioarvossa samana pysyviä arvoja, kuten kirjaimia tai yhdysviivan (-). Voit myös antaa numeromerkkejä (\#) ja et-merkkejä (&) kirjasinten paikkamerkkeinä, jotka muuttuvat aina dimensioarvon luonnin yhteydessä. Käytä numeromerkkiä (\#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä. Muotoilupeitteen kenttä on käytettävissä vain, kun valitset **Mukautettu dimensio** **Käytä arvoja kohteesta** -kentässä.

**Esimerkki**

Jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, anna muotoilupeitteeksi **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Yksikön tukemat dimensiot

Voit luoda yksikön tukeman taloushallinnon dimension valitsemalla **Käytä arvojaa** -kenttään järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio perustuu. Taloushallinnon dimensioarvot luodaan sitten tästä yksiköstä. Voit esimerkiksi luoda projektien dimensioarvot valitsemalla **Projektit**. Jokaiselle projektin nimelle luodaan sitten dimensioarvo. Yksikön arvot näkyvät **Taloushallinnon dimension arvot** -sivulla. Jos nämä arvot ovat yrityskohtaisia, myös yritys näkyy sivulla.

## <a name="activating-dimensions"></a>Dimensioiden aktivointi

Kun aktivoit taloushallinnon dimension, taulu päivitetään sisältämään taloushallinnon dimension nimen. Poistetut dimensiot poistetaan. Voit antaa dimensioarvot ennen taloushallinnon dimension aktivointia. Taloushallinnon dimensiota ei voi kuitenkaan kuluttaa missään, ennen kuin se on aktivoitu. Et voi esimerkiksi lisätä taloushallinnon dimensiota tilirakenteeseen ennen dimension aktivointia. Kun valitset **Aktivoi**, kaikki dimensiot päivitetään ja ne näyttävät tilan muutokset.

## <a name="translations"></a>Käännökset

Voit kirjoittaa valitun taloushallinnon dimension **Tekstin käännös** -sivulla erikielistä tekstiä. Voit kirjoittaa päätilille erikielistä tekstiä **Päätilin käännös** -sivulla. 

## <a name="legal-entity-overrides"></a>Yrityksen ohitukset

Kaikkia dimensioita ei voi käyttää kaikissa yrityksissä. Lisäksi jotkin dimensiot voivat liittyä vain tiettyyn jaksoon. Näissä tapauksissa voit määrittää **Yrityksen ohitukset** -osassa yritykset, joissa dimension käyttö pitäisi keskeyttää, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.

## <a name="deleting-financial-dimensions"></a>Taloushallinnon dimensioiden poistaminen

Tietojen viitteiden eheyden varmistamiseksi taloushallinnon dimensiot voi vain harvoin poistaa. Jos yrität poistaa taloushallinnon dimension, seuraavat ehdot arvioidaan:

- Onko taloushallinnon dimensiota käytetty jossakin kirjatussa tai kirjaamattomassa tapahtumassa tai jossain dimensioarvoyhdistelmän tyypissä?
- Onko taloushallinnon dimensiota käytettä missään aktiivisessa tilirakenteessa, lisäasetuksia käyttävässä sääntörakenteessa tai taloushallinnon dimensiojoukossa?
- Onko taloushallinnon dimensio osa oletusarvoista taloushallinnon dimension integrointimuotoa?
- Onko taloushallinnon dimensio määritetty oletusdimensioksi?
- Onko taloushallinnon dimension valinta poistettu Financial Reporting -asetuksista? 

Jos jokin ehdoista täyttyy, et voi poistaa taloushallinnon dimensiota.

> [!NOTE]
> Finance-versiosta 10.0.27 alkaen taloushallinnon dimensioita ei enää valita automaattisesti Financial Reporting -asetuksille, kun ne luodaan.

## <a name="default-dimension-values"></a>Oletusdimension arvot

Voit käyttää arvoja tietueiden, kuten asiakkaan ja toimittajan tietuiden, hallintaan uusien dimensioiden oletusarvoina. Kun uusia dimensioita luodaan, näille päätietuille syötetään dimensioarvot. Esimerkiksi kun luot uuden asiakkaan, asiakastunnus syötetään asiakasdimensioon. Kun luot myyntitilauksia, laskuja tai muita asiakirjoja, jotka vaativat asiakastunnusta, käytetään nykyisiä oletussääntöjä ja asiakastunnus lisätään asiakirjaan.

Tätä toimintoa ohjataan dimension asetuksella. Tämä asetus on nimeltään **Kopioi arvot tähän dimensioon kullekin uudelle luodulle dimension nimelle**, jossa **dimension nimi** on dimension nimi. Asetus on oletusarvoisesti poissa käytöstä. Se voidaan kuitenkin ottaa käyttöön milloin tahansa.

Jos tietueet ovat jo olemassa dimensiossa, päätietueet päivitetään, kun otat toiminnon käyttöön. Nykyisiä asiakirjoja ja tapahtumia ei kuitenkaan päivitetä.

Jos luot päätietueen mallin avulla, varmista, että mallin päädimension arvo on tyhjä. Jos luot esimerkiksi asiakkaita mallista, varmista, että mallin asiakasdimensio on tyhjä. Asiakasdimension arvo tulee oletusarvoisesti uudesta asiakasnumerosta, kun luot uuden asiakkaan.  

## <a name="derived-dimensions"></a>Johdetut dimensiot

Voit määrittää dimension siten, että siihen syötetään automaattisesti muiden dimensioiden tiedot, kun syötät tämän dimension asiakirjaan. Jos syötät esimerkiksi kustannuspaikan 10, arvo **20** voidaan automaattisesti syöttää osaston dimensioon.

Voit määrittää johdetut arvot dimensioiden sivulla.

1. Valitse dimensio ja valitse sitten **Johdetut dimensiot**.

    **Johdetut dimensiot** -sivulla on ruudukko. Valitun dimension segmentti on tämän ruudukon ensimmäinen sarake.

2. Lisää segmentit, joista johdetaan. Kukin segmentti näkyy sarakkeena.

Syötä dimensioyhdistelmät, jotka on johdettava dimensiosta ensimmäisessä sarakkeessa. Jos esimerkiksi haluat käyttää kustannuspaikkaa dimensiona, josta osasto ja sijainti johdetaan, syötä kustannuspaikka 10, osasto 20 ja sijainti 30. Kun sitten syötät kustannuspaikan 10 päätietueessa tai tapahtuman sivulla, osasto 20 ja sijainti 30 sijainti syötetään oletusarvoisesti.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Nykyisten arvojen korvaaminen johdetuilla dimensioilla
 
Johdettu dimensioprosessi ei oletusarvoisesti korvaa johdettujen dimensioiden nykyisiä arvoja. Esimerkiksi jos syötät kustannuspaikan 10, etkä syötä mitään muuta dimensiota, osasto 20 ja sijainti 30 syötetään oletusarvoisesti. Jos kuitenkin muutat kustannuspaikkaa, jo määritettyjä arvoja ei muuteta. Voit siten määrittää oletusdimensiot päätietueisiin, eivätkä johdetut dimensiot muuta näitä dimensioita.

Voit muuttaa johdettujen dimensioiden toimintaa korvaamalla aiemmat arvot valitsemalla **Korvaa nykyiset dimension arvot johdetuilla arvoilla** -valintaruutu **Johdetut dimensiot** -sivulla. Jos tämä kenttä on valittu, voit antaa dimension, jossa on johdetun dimension arvot, ja nämä johdetun dimension arvot korvaavat kaikki aiemmat arvot. Jos edellisessä esimerkissä annat kustannuspaikan 10 etkä mitään muuta dimensiota, osasto 20 ja sijainti 30 annetaan oletusarvoisesti. Jos arvoina on kuitenkin jo osasto 50 ja sijainti 60, arvot ovat nyt muuttuneet ja osastona on nyt 20 ja sijaintina 30.
 
Tällä asetuksella johdetut dimensiot eivät automaattisesti korvaa aiempia dimension oletusarvoja, kun dimension arvot ovat oletusarvoja. Dimension arvot korvataan vain, kun annat sivulla uuden dimension arvon ja sivulla on kyseisen dimension aiemmin johdettuja arvoja.

### <a name="preventing-changes-with-derived-dimensions"></a>Muutosten estäminen johdettujen dimensioiden avulla
 
Kun lisäät segmenttejä johdettuna dimensiona valitsemalla **Lisää segmentti** **Johdetut dimensiot** -sivulla, **Lisää segmentti** -sivun alaosassa on asetus, jolla voit estää kyseisen dimension muutokset, kun se johdettuna sivulla. Oletusarvoisesti asetus ei ole käytössä, joten se ei estä johdetun dimension arvojen muuttamista. Vaihda asetukseksi **Kyllä**, jos haluat estää dimension muuttamisen sen jälkeen, kun se on johdettu. Esimerkki: Jos osastodimension arvo on johdettu kustannuspaikkadimension arvosta, osaston arvoa ei voi muuttaa, jos **Estä muutokset** -asetus on **Kyllä**. 
 
Asetus ei estä muutoksia, jos dimension arvo on kelvollinen mutta sitä ei ole mainittu johdettujen dimensioiden luettelossa. Esimerkki: Jos osasto 20 on johdettu kustannuspaikasta 10 ja annat kustannuspaikan 10, et voi muokata osastoa 20. Jos kuitenkin annat kustannuspaikan 20 eikä sitä ole kustannuspaikan johdettujen dimensioiden luettelossa, voit muokata osaston arvoa. 
 
Tilin arvo ja kaikki dimensioiden arvot voidaan kaikissa tapauksissa tarkistaa tilirakenteiden perusteella, kun johdettujen dimensioiden arvoja on käytetty. Jos käytät johdettuja dimensioita eivätkä ne läpäise tarkistusta, kun niitä käytetään sivulla, johdettujen dimensioiden arvot on muutettava johdettujen dimensioiden sivulla, ennen kuin voit käyttää niitä tapahtumissa. 
 
Kun muutat dimensioita **Taloushallinnon dimensiot** -pikavälilehdessä, muutokset estämään merkittyä dimensiota ei voi muokata. Jos olet antamassa sivulla tilin ja dimensiot segmentoituun merkinnän ohjausobjektiin, dimensioita voi muokata. Kun kuitenkin siirrät korostuksen pois segmentoidusta merkinnän ohjausobjektista ja siirryt toiseen kenttään tai teet toiminnon, tili ja dimensiot tarkistetaan johdettujen dimensioiden luettelon ja tilirakenteiden perusteella. Näin varmistetaan, että olet antanut asianmukaiset arvot. 

### <a name="derived-dimensions-and-entities"></a>Johdetut dimensiot ja yksiköt

Voit määrittää johdetut dimensioiden segmentit ja arvot yksikköjen avulla.

- Johdettujen dimensioiden yksikkö määrittää ohjaavat dimensiot ja segmentit, joita käytetään näitä dimensioita varten.
- Johdetun dimension arvon yksikön avulla voit tuoda arvot, jotka on johdettava kullekin ohjaavalle dimensiolle.

Kun käytät yksikköä tietojen tuontiin, jos tämä yksikkö tuo dimensioita, tuonnin aikana sovelletaan johdetun dimension sääntöjä, jollei yksikkö nimenomaisesti korvaa näitä dimensioita.

Lisätietoja on seuraavissa aiheissa:

- [Määritä taloushallinnon dimensiot](tasks/define-financial-dimensions.md)
- [Ylläpidä taloushallinnon dimension oletusmalleja](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
