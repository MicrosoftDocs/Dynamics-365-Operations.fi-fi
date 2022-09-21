---
title: Tehtävien hallinta
description: Tässä artikkelissa kerrotaan Tehtävänhallinta-toiminnosta, joka on käytettävissä Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 09/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 29b547ff4f55b572ab774e7e70949ec8cb53ef42
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445891"
---
# <a name="task-management"></a>Tehtävienhallinta

[!INCLUDE [PEAP](../includes/peap-1.md)]

Tehtävänhallinnan avulla voit luoda tehtäviä, jotka on suoritettava, jotta työntekijöitä voi palkata (perehdyttäminen), lopettaa työsuhteen (poistuminen) ja siirtää (siirto). Tehtävänhallinnassa käytetään tarkistusluetteloiden käsitettä. Tarkistusluettelo on luettelo, joka sisältää perehdytys-, poistumis- ja siirtymistehtävät. Tehtävänhallinta ryhmittelee tehtävät yhteen tarkistusluetteloiden avulla sekä määrittää niitä yksittäisille henkilöille tai ryhmille. Tarkistusluettelotoiminnot ovat samankaltaisia perehdytykselle, poistumiselle ja siirtymiselle.

## <a name="checklist-overview"></a>Tarkistusluettelon yleiskuvaus

Tarkistusluettelo on tehtäväryhmä. Tarkistusluetteloiden avulla voit joustavasti ryhmitellä tehtävät, ja niitä voidaan käyttää uudelleen (esimerkiksi palkattaessa lisää työntekijöitä). Voit luoda niin monta tarkistusluetteloa kuin on tarpeen, ja voit määrittää samat tehtävät useisiin tarkistusluetteloihin.

### <a name="examples"></a>Esimerkkejä

Seuraavissa esimerkeissä esitetään, kuinka tarkistusluetteloita voidaan käyttää perehdytysprosessissa. Koska tarkistusluettelotoiminnot ovat samankaltaisia perehdytykselle, poistumiselle ja siirrolle, tiedot koskevat myös poistumis- ja siirtymisprosesseja.

Osana perehdytysprosessia henkilöstöhallinnon ammattilaiset voivat luoda tehtäviä, jotka seuraavat saapuvien ja viimeksi palkattujen työntekijöiden etenemistä. Koska työhönottoprosessi voi vaihdella työntekijän sijainnin tai maantieteellisen sijainnin mukaan, voit luoda useita työhönottojen tarkistusluetteloita eri palkkaustilanteita varten.

**Esimerkki 1**

Jokaisen Yhdysvalloissa palkatun työntekijän on suoritettava esimerkiksi veroennakonpidätyslomakkeiden täyttäminen. Esimerkiksi yritysauton määrittämiseen liittyvät tehtävät saattavat kuitenkin koskea vain johtotason henkilökuntaa. Tässä tapauksessa voidaan luoda kaksi perehdytyksen tarkistusluetteloa: **Työntekijät Yhdysvalloissa** ja **Vain johtajat**. Kun keskitason esimies sitten palkataan Yhdysvalloissa, valitaan **Työntekijät Yhdysvalloissa** -tarkistusluettelo. Kun johtaja on palkattu Yhdysvalloissa, valitaan molemmat tarkistusluettelot sen varmistamiseksi, että kaikki pakolliset perehdytystehtävät suoritetaan.

**Esimerkki 2**

Yrityksellä on sekä kausittaisia työntekijöitä että tavallisia kokoaikaisia työntekijöitä. Vaikka joitakin tehtäviä (esimerkiksi uuden työntekijän saapumisajan tarkistaminen) käytetään molemmissa tyypeissä, jotkin lisätehtävät koskevat vain tavallisia kokoaikaisia työntekijöitä. Tässä tapauksessa voit luoda kaksi tarkistusluetteloa. Molemmissa tarkistusluetteloissa on sekä kausittaisia että säännöllisiä kokoaikaisia työntekijöitä koskevat tehtävät, mutta vain yksi tarkistusluettelo sisältää tehtävät säännöllisille kokoaikaisille työntekijöille.

## <a name="task-management-workspace"></a>Tehtävienhallinnan työtila

**Tehtävän hallinta** -työtilassa on luettelo kaikista tehtävistä, jotka on määritetty käyttäjille, jotka ovat mukana perehdytys-, poistumis- ja siirtoprosesseissa. Jos haluat tarkastella prosessin tehtäviä, valitse soveltuva välilehti vasemmasta yläkulmasta: **Perehdytys**, **Poistuminen** tai **Siirtyminen**. Oletusarvon mukaan **tehtävänhallinnan** työtilaa voivat käyttää vain henkilöstöhallinnon asiantuntijat.

**Perehdytys**-välilehdessä on **Aloittaa pian** -luettelo, joka sisältää saapuvat työntekijät sekä **Viimeksi palkatut** -luettelon juuri palkatuista työntekijöistä. Molemmissa luetteloissa voit valita vain yhden työntekijän. Kun valitset työntekijän, kaikki tähän työntekijän perehdytykseen liittyvät tehtävät näkyvät sivun oikealla puolella. **Perehdytys**-välilehdessä on myös **Kaikki tehtävät** -luettelo, joka sisältää kaikkien saapuvien tai viimeksi palkattujen työntekijöiden tehtävät. Se sisältää myös erääntyneiden tehtävien luettelon sekä nykyiselle käyttäjälle määritettyjen tehtävien luettelon.

**Poistuminen**-välilehti sisältää luettelon yrityksestä poistuvista työntekijöistä sekä luettelon työntekijöistä, jotka ovat jo lähteneet yrityksestä. Molemmissa luetteloissa voit valita vain yhden työntekijän. Kun valitset työntekijän, kaikki tähän työntekijän poistumiseen liittyvät tehtävät näytetään. **Poistuminen**-välilehdessä on myös **Kaikki tehtävät** -luettelo, joka sisältää kaikkien poistuvien tai poistuneiden työntekijöiden tehtävät. Se sisältää myös erääntyneiden tehtävien luettelon sekä nykyiselle käyttäjälle määritettyjen tehtävien luettelon.

**Siirrot**-välilehti sisältää **Kaikki tehtävät** -luettelon, jossa näkyvät kaikkien toimia vaihtavien tai äskettäin vaihtaneiden työntekijöiden kaikki tehtävät. Se sisältää myös erääntyneiden tehtävien luettelon sekä nykyiselle käyttäjälle määritettyjen tehtävien luettelon.

Kaikissa kolmessa välilehdessä henkilöstöhallinnon avustajat ja esimiehet voivat suorittaa seuraavat tehtävät:
- Tarkistusluettelon kohdistaminen työntekijälle
- Tehtävän tilan päivittäminen
- Tehtävän määrittäminen uudelleen
- Tehtävän määräpäivän päivittäminen

> [!NOTE]
> **Perehdytys**-välilehdessä näytetään oletusarvoisesti työntekijät, jotka palkattiin edellisen seitsemän päivän aikana. Jos haluat muuttaa tätä asetusta, määritä aikaväli **Viimeksi palkatut** -kenttään **Henkilöstöhallinnon parametrit** -sivun **Yleiset**-välilehdestä. **Viimeksi palkatut** -luettelossa olevat tiedot voidaan näyttää tietyltä päivien, kuukausien tai vuosien ajalta. Jos haluat esimerkiksi nähdä edellisen 14 päivän aikana palkattujen työntekijöiden luettelon, määritä **Kausi**-kentän arvoksi **14** ja **Yksikkö**-kentän arvoksi **Päivät**.
> **Henkilöstöhallinnon parametrit** -sivulla voit myös päivittää poistuvien ja poistuneiden työntekijöiden luettelon päivämäärävälin, jotka näkyvät **Poistuminen**-välilehdessä. Nämä asetukset koskevat myös **Henkilöstöhallinta**-työtilaa.

## <a name="setting-up-tasks"></a>Tehtävien määritys

Voit luoda tehtävät yksitellen ja käyttää niitä uudelleen useissa tarkistusluetteloissa. Voit luoda tehtävän valitsemalla **Perehdytyksen asetukset** -sivun **Tehtävät**-välilehdessä **Uusi**.

Voit liittää luodun tehtävän useisiin tarkistusluetteloihin valitsemalla tehtävän ja valitsemalla sitten valikossa **Käytä valintaluetteloissa** -kohdan.

Voit myös lisätä tehtäviä suoraan tarkistusluetteloon. Voit lisätä tehtävän tarkistusluetteloon luomalla **Perehdytyksen asetukset** -sivun **Tarkistusluettelo**-välilehdessä uuden tarkistusluettelon, johon tehtävä lisätään, tai lisätä tehtävän aiemmin luotuun tarkistusluetteloon.

Jos haluat muokata tehtävää kirjastossa, valitse **Muokkaa** tehtäväkirjaston valikosta. Jos tehtävä on liitetty tarkistusluetteloihin, nämä tarkistusluettelot näkyvät **Muokkaa tehtävää** -sivulla. Jos haluat, että mille tahansa tarkistusluettelon tehtävälle päivitetään muokkaukset, valitse kyseiset tarkistusluettelot **Kohdista tarkistusluetteloihin** -osasta.

Voit poistaa tehtäviä kirjastosta valitsemalla **Poista**-vaihtoehdon. Jos tehtävä liittyy tarkistusluetteloon, tämä toiminto ei poista tehtävää tarkistusluettelosta. Tehtävä on poistettava tarkistusluettelosta erillisenä toimintona.

> [!NOTE]
> Jos lisäät tehtävän suoraan tarkistusluetteloon, et voi käyttää sitä uudelleen muissa tarkistusluetteloissa.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä, kun luot tehtävän jommankumman menetelmän mukaan.

| Kenttä           | Kuvaus |
|-----------------|-------------|
| Tehtävä            | Anna tehtävän nimi. |
| Kuvaus     | Syötä tehtävän kuvaus. |
| Valinnainen        | Määritä, onko tehtävä valinnainen ja vain tiedoksi. |
| Tehtävälinkki       | Kirjoita ulkoisen Internet-sivun tai sovelluksen tietyn sivun URL-osoite, jossa käyttäjän pitää suorittaa tehtävä. Lisätietoja on kohdassa [Tehtävän linkit](#task-links). |
| Määrityksen tyyppi | Tehtävät voidaan määrittää tietylle työntekijälle, toimelle tai toimiryhmälle, työntekijän (eli työntekijän, joka on osa perehdytys-, poistumis- ja siirtoprosessia) esimiehelle tai työntekijälle itselleen. Valitse määrityksen tyyppi. Lisätietoja on kohdassa [Määrityksen tyypit](#assignment-types). |
| Liitetty kohteelle     | Valitse tietty työntekijä, toimi tai toimiryhmä, jolle tehtävä määritetään. |
| Yhteyshenkilö  | Määritä henkilö, johon otetaan yhteyttä, jos tehtävästä on kysymyksiä. |
| Määräpäivän siirto | Määritä, kuinka monta päivää ennen perehdytys-, poistumis- ja siirtopäivää tai sen jälkeen tehtävä erääntyy. Lisätietoja: [Tehtävien määräpäivät ja Määräpäivän siirto -kenttä](#task-due-dates-and-the-due-date-offset-field). |
| Ohjeet    | Määritä tehtävän suorittamisen ohjeet. Lisätietoja on osassa [Ohjeet](#instructions). |

### <a name="task-links"></a>Tehtävälinkit

Tehtävälinkki antaa linkin ulkoiseen Internet-sivustoon tai Dynamics 365 -sovelluksen sivuun. Voit määrittää tehtävälinkin, jos tehtävään määritetyn henkilön on siirryttävä tietylle Internet-sivulle tai tietylle Dynamics 365 -sovelluksen sivulle tehtävän suorittamiseksi. Kun luot tehtävän linkin, voit valita yhden seuraavista vaihtoehdoista:

- **Valikkovaihtoehto** – Jos valitset tämän vaihtoehdon, näytössä on luettelo kaikista Dynamics 365 -sovelluksen sivuista. Valitse luettelosta sivu.
- **URL -osoite** – Jos valitset tämän vaihtoehdon, kirjoita Internet-sivun URL-osoite, jonne tehtävän suorittavan henkilön on siirryttävä. Määritetty sivu voi olla sivu, joka ei ole osa Dynamics 365 -sovellusta.
- **Työntekijän tiedot** – Jos valitset tämän vaihtoehdon, valitse jokin seuraavista vaihtoehdoista:

    - **Työntekijän itsepalvelutoiminnot** – Tässä vaihtoehdossa näkyy luettelo **työntekijöiden itsepalvelussa** käytettävissä olevista sivuista. Käytä sitä, jos perehtyvälle työntekijälle määritetty tehtävä on suoritettava **työntekijän itsepalvelussa**. Jos esimerkiksi haluat työntekijän syöttävän henkilökohtaiset yhteystietonsa, valitse **työntekijän itsepalvelutoiminnot** ja valitse sitten **Henkilökohtaiset tiedot&gt;Henkilökohtaiset tiedot**.
    - **Työntekijän hallintatoiminnot** – Tämä vaihtoehto näyttää luettelon sivuista, jotka liittyvät työntekijän tietueeseen mutta jotka eivät ole työntekijän käytettävissä. Jos esimerkiksi haluat, että tehtävän omistaja määrittää tiedot, jotka liittyvät perehdytettävään työntekijään, esimerkiksi kompensaatiotiedot, valitse **työntekijänhallinnan toimenpiteet** ja valitse sitten **Kompensaatio&gt;Kiinteä kompensaatio**.

### <a name="assignment-types"></a>Määrityksen tyypit

Kun työntekijä palkataan, irtisanotaan tai siirretään, voidaan valita yksi tai useampi tarkistusluettelo. Kun tarkistusluettelo on valittu ja työhönotto-, päättymis- tai siirtoprosessi on suoritettu, tehtävät luodaan ja määritetään käyttäjille, jotta voidaan seurata etenemistä.

Kun tehtävä luodaan, se määritetään tietylle käyttäjälle. Käyttäjä, jolle tehtävä on määritetty, riippuu tehtävälle valitusta määrityksen tyypistä. **Määrityksen tyyppi** -kentässä ovat käytettävissä seuraavat arvot:

- **Työntekijä** – Määritä tehtävä tietylle työntekijälle. Kun olet valinnut tämän arvon, valitse työntekijä **Määritetty kohteelle** -kentästä.
- **Toimi** – Määritä tehtävä tietylle toimelle. Kun olet valinnut tämän arvon, valitse toimi **Määritetty kohteelle** -kentästä.

    Esimerkiksi IT-insinööri on aina vastuussa kannettavan tietokoneen valmistelemisesta uudelle työntekijälle. Kun tässä tapauksessa luot kannettavan määritystehtävää, valitse ensin **Toimi** määritystyypiksi ja toimeksi **IT-insinööri**. Kun työntekijä palkataan ja tarkistusluettelo on määritetty, kannettavan tietokoneen konfigurointitehtävä määritetään sen mukaan, kuka työntekijä on IT-insinöörin toimessa, kun palkkaustoiminto käynnistetään.

- **Ryhmä**: Liitä tehtävä toimiryhmälle (määritysryhmä). Kun olet valinnut tämän arvon, valitse ryhmä **Määritetty kohteelle** -kentästä. Lisätietoja: [Määritysryhmien määritys (valinnainen)](#setting-up-assignment-groups-optional).
- **Esimies** – Määritä tehtävä sen työntekijän esimiehelle, joka on palkattu, irtisanottu tai siirretty.

    > [!IMPORTANT]
    > Jos tarkistusluetteloa käytetään ja jos toimea ei ole määritetty palkatulle, irtisanotulle tai siirretylle työntekijälle, esimiestä ei voi määrittää. Tällöin tehtävä määritetään tarkistusluettelon omistajalle. Lisätietoja: [Tarkistusluetteloiden määrittäminen](#setting-up-checklists).

- **Työntekijä** – Määritä työntekijä, joka palkataan, irtisanotaan tai siirretään.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Tehtävän määräpäivät ja Määräpäivän siirto -kenttä

Tehtävän eräpäivät perustuvat työsuhteen alkamispäivämäärään, päättymispäivään tai siirtopäivämäärään. Joitakin tehtäviä on suoritettava ennen työntekijän aloituspäivää, kun taas muut tehtävät voidaan suorittaa sen jälkeen. Tehtävää määritettäessä annetaan perehdytys-, poistumis- ja siirtopäivään suhteessa oleva määräpäivä **Määräpäivän siirtymä** -kentässä. Esimerkiksi IT-insinöörin on valmisteltava kannettava tietokone uudelle työntekijälle kaksi päivää ennen työntekijän aloituspäivää. Kun luot kannettavan tietokoneen konfigurointitehtävän, määritä **Määräpäivän siirtymä** -kentän arvoksi **-2**. Jos työntekijän aloituspäivä on 5. toukokuuta, tehtävä erääntyy 3. toukokuuta.

> [!NOTE]
> Eräpäiviä voi muokata myös tehtävän luomisen jälkeen.

Eräpäivät lasketaan tarkistusluetteloon liittyvän kalenterin perusteella. Lisätietoja: [Tarkistusluetteloiden määrittäminen](#setting-up-checklists).

### <a name="instructions"></a>Ohjeet

Monimutkaisissa tehtävissä saattaa olla useita vaiheita tai tehtäviä suorittavien henkilöiden täytyy mahdollisesti antaa lisätietoja. **Ohjeet**-kenttään voit antaa tehtävän suorittamista koskevia lisätietoja sille henkilölle, joka on määritetty tehtävän suorittajaksi.

## <a name="setting-up-checklists"></a>Tarkistusluetteloiden määrittäminen

Tarkistusluettelo on tehtäväryhmä. Voit luoda niin monta tarkistusluetteloa kuin on tarpeen, ja voit määrittää samat tehtävät useisiin tarkistusluetteloihin.

Voit luoda uuden tehtävän tarkistusluettelossa valitsemalla **Uusi**-kohdan **Tehtävät**-valikkorivillä. Kun luot uuden tehtävän, voit lisätä sen tehtäväkirjastoon ja jakaa tehtävän usean tarkistusluettelon välillä. Voit lisätä tehtävän kirjastoon vain, jos **Käytä tehtävää kirjastossa** -vaihtoehdon arvona on **Kyllä**. Jos lisäät tehtävän tehtäväkirjastoon, voit lisätä sen myös muihin tarkistusluetteloihin samalla kertaa valitsemalla nämä luettelot **Kohdista tarkistusluetteloihin** -osaa. Jos tehtävää ei lisätä kirjastoon, se on vain tarkistusluettelossa, jossa luot tehtävän.

Jos haluat muokata tehtävää tarkistusluettelossa, valitse **Muokkaa**. Jos tehtävä on liitetty tarkistusluetteloihin, nämä tarkistusluettelot näkyvät **Muokkaa tehtävää** -sivulla. Jos haluat, että mille tahansa tarkistusluettelon tehtävälle päivitetään muokkaukset, valitse kyseiset tarkistusluettelot **Kohdista tarkistusluetteloihin** -osasta.

Jos haluat poistaa tehtäviä tarkistusluettelosta, valitse **Poista**. Tämä toiminto vain siirtää tehtävät pois tarkistusluettelosta. Se ei poista niitä pysyvästi tehtäväkirjastosta. Jos haluat poistaa tehtävän kirjastosta pysyvästi, siirry tehtäväkirjaston sivulle ja valitse **Poista**.

Kun luot tarkistusluettelon, määrität omistajan ja kalenterin.

Jos tehtävän **Määrityksen tyyppi** -kentän arvona on **Toimi**, **Esimies** tai **Ryhmä**, mutta määrityksen tyypistä ei voi johtaa tiettyä henkilöä, tehtävä määritetään tarkistusluettelon omistajalle. Seuraavassa on esimerkkejä tilanteista, joissa tehtävät määritetään tarkistusluettelon omistajalle:

- Työntekijälle, joka palkataan tai irtisanotaan, ei ole määritetty toimea. Koska työntekijällä ei ole toimea, hänen esimiestään ei voi määrittää.
- **Määrityksen tyyppi** -kentän arvona on **Toimi**, mutta toimelle ei ole määritetty työntekijää tehtävän luomisen yhteydessä. Esimerkiksi **Kannettavan tietokoneen määrittäminen**  -tehtävä määritetään toiminumerolle 000876 (**Teknisen tuen asiantuntija**). Kun työntekijä palkataan, työntekijää ei ole määritetty toimeen 000876. Siksi tehtävä luodaan tarkistusluettelon omistajalle.
- **Määrityksen tyyppi** -kentän arvona on **Ryhmä**, mutta ryhmän toimille ei ole määritetty työntekijää tehtävän luomisen yhteydessä.

Tarkistusluettelolle määritettyä kalenteria käytetään tarkistusluettelon tehtävien eräpäivän laskemiseen. Työpäivät ja muut kuin työpäivät määritetään kalenteriasetuksissa. Työpäivät sisällytetään, kun tehtävien eräpäivä lasketaan ja muut kuin työpäivät jätetään pois. Muut kuin työpäivät sisältävät viikonloppuja ja lomia. 

Kun kalenteri on määritetty, se liitetään tarkistusluettelomalliin. Näin jokaisen tarkistusluettelon tehtävän eräpäivä lasketaan samalla tavalla. Voit määrittää useita kalentereita, mutta kuhunkin tarkistusluetteloon voidaan liittää vain yksi kalenteri.

## <a name="setting-up-assignment-groups-optional"></a>Määritysryhmien määrittäminen (valinnainen)

Joskus tehtävästä vastaa henkilöryhmä. IT-työntekijöiden ryhmä voi esimerkiksi olla vastuussa kannettavan tietokoneen valmistelemisesta uusille työntekijöille.

Määritä määritysryhmä noudattamalla seuraavia ohjeita.

1. Valitse **Ryhmän määritys** -sivulla **Uusi**.
1. Kirjoita ryhmän nimi (esimerkiksi **IT – kannettava tietokone**) ja kuvaus.
1. Valitse **Tallenna**.
1. Valitse **Jäsenet**-pikavälilehdessä **Lisää**.
1. Valitse **Toimet**-kentässä kaikki tehtävästä vastaavat toimet.

Kun määritysryhmä on luotu, sen voi valita, kun tehtävä luodaan. Jotta voit valita tehtävälle tietyn ryhmän, sinun on valittava **määrityksen tyypiksi** **Ryhmä**. Luomasi ryhmä on tämän jälkeen käytettävissä valintaa varten **Määritetty kohteelle** -kentässä.

> [!IMPORTANT]
> Jos tehtävä on määritetty ryhmälle, tehtävä merkitään **valmiiksi**, kun yksi ryhmän henkilö suorittaa sen valmiiksi. Tehtävät luodaan palkkaus-, päättymis- tai siirtovaiheessa. Ne luodaan käyttäjille, jotka on määritetty ryhmään sisältyviin toimiin.

## <a name="setting-up-task-groups-optional"></a>Tehtäväryhmien määrittäminen (valinnainen)

Perehdytys-, poistumis- ja siirtoprosessi voi sisältää useita tehtäviä. Voit luokitella aiheeseen liittyviä tehtäviä luomalla valinnaisia tehtäväryhmiä, jotta kaikki pakolliset tehtävät on helpompi määrittää tarkistusluetteloon. Esimerkiksi henkilöstöhallinnon, IT:n ja palkanlaskennan osastojen on suoritettava tietyt tehtävät uuden työntekijän palkkaamista varten. Luot siis seuraavat tehtäväryhmät: **henkilöstöhallinto**, **IT** ja **Palkanlaskenta**. Kun luot tehtävän, voit sitten liittää siihen jonkin näistä tehtäväryhmistä.

Kun haluat lisätä tehtävän tarkistusluetteloon, voit suodattaa tehtäväluettelon sen tehtäväryhmän mukaan, johon haluamasi tehtävä on määritetty. Kun esimerkiksi luot tarkistusluettelomallin, voit suodattaa luettelon siten, että vain **IT**-tehtäväryhmälle määritetyt IT-tehtävät näkyvät. Näin voit varmistaa, että vain tarvittavat IT-tehtävät valitaan.

## <a name="using-checklists"></a>Tarkistusluetteloiden käyttäminen

Kun työntekijä palkataan, irtisanotaan tai siirretään, voidaan valita yksi tai useampi tarkistusluettelo. Tehtävän eräpäivät ja työntekijän toimeksiannot luodaan sen jälkeen, kun palkkaus-, päättymis- tai siirtoprosessi on valmis. Kun esimerkiksi valitset **Työhönotto**- tai **Työhönotto ja lisätiedot** -painikkeen, tehtävät luodaan määrityksen tyypin mukaan yksittäisille käyttäjille.

Eräpäivä liitetään jokaiseen tehtävään lisäämällä tai vähentämällä määräpäivän siirtymä työntekijän aloituspäivästä. Lisätietoja: [Tehtävien määräpäivät ja Määräpäivän siirto -kenttä](#task-due-dates-and-the-due-date-offset-field).

Jos käytät henkilöstötoimintoja, tehtävät luodaan, kun **Valmis**-painike on valittuna tai toimenpide hyväksytään.

Voit ottaa **tehtävänhallinnan** työtilassa käyttöön tarkistusluettelon työntekijälle valitsemalla työntekijän yksinkertaiselta luettelosivulta tai tietosivulta ja valitsemalla sitten **Käytä tarkistusluetteloa**. **Kohdepäivämäärä**-kentän arvoa käytetään tehtävien eräpäivän laskemiseen. Tavoitepäivämäärän on yleensä vastattava työntekijän palkkaus-, työsuhteen päättymis- tai siirtopäivämäärää.

Voit kohdistaa tarkistusluettelon työntekijälle myös avaamalla **Työntekijä**-sivun ja valitsemalla **Tarkistusluettelot** valikosta.

## <a name="completing-tasks"></a>Tehtävien suorittaminen

Työntekijä voi tarkastella **työntekijän itsepalvelusivulla** kaikkia hänelle määritettyjä tehtäviä. Jokaiselle määritetylle tehtävälle näytetään **Tehtävä**-, **Kuvaus**-, **Ohjeet**- ja **Yhteyshenkilö**-arvot. Lisäksi työntekijä voi avata kunkin tehtävän ulkoisen Internet-sivun tai liittyvän sivun Dynamics 365 -sovelluksessa.

Tehtävät voidaan näyttää myös oletuskoontinäytössä. Tehtävien näyttäminen oletuskoontinäytössä:
1. Valitse **Käyttäjän asetukset – Asetukset – Tehtävänhallinta** 
2. Aseta **Näytä tehtävät oletuskoontinäytössä** -kohdan arvoksi **Käytössä**.  

>[!Note] 
>**Tehtävänhallinta**-toiminnon on oltava käytössä **ominaisuudenhallinnassa**, jotta se voidaan näyttää **käyttäjän asetuksissa**.

Tehtävät voidaan merkitä **keskeneräisiksi**, **peruutetuiksi** tai **valmiiksi**. Jos tehtävä on määritetty ryhmälle, se merkitään **valmiiksi**, kun yksi ryhmän henkilö suorittaa sen valmiiksi.

Tehtäviä voidaan myös määrittää uudelleen.
