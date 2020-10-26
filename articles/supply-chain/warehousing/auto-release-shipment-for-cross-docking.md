---
title: Lähetyksen automaattinen vapautus cross-dockingia varten
description: Tässä aiheessa kuvataan cross-docking-strategia, jolla voit automaattisesti vapauttaa kysyntätilauksen varastoon, kun kysyntämäärän toimittava tuotantotilaus ilmoitetaan suoritetuksi. Tällöin määrä siirretään suoraan tuotossijainnista lähtevien sijaintiin.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b86fe2f3ea4321dbe598233018934187ba0d713a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983976"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Lähetyksen automaattinen vapautus cross-dockingia varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan cross-docking-strategia, jolla voit automaattisesti vapauttaa kysyntätilauksen varastoon, kun kysyntämäärän toimittava tuotantotilaus ilmoitetaan suoritetuksi. Tällöin kysyntätilauksen täyttämiseen vaadittava määrä siirretään suoraan tuotannon tuotossijainnista lähtevien sijaintiin.

Cross-docking on varaston käsittelykulku, jossa lähtevän tilauksen täyttämiseen vaadittava määrä ohjataan saapuvan tilauksen vastaanottosijainnista tilauksen lähtevien laiturille tai koontialueelle. (Saapuva tilaus voi olla ostotilaus, siirtotilaus tai tuotantotilaus.) Edistynyt cross-docking-toiminto tukee kaikkia tarjonta- ja kysyntätilauksia ja edellyttää, että lähtevä kysyntä vapautetaan ennen cross-docking-tilaisuuden tunnistamista. Lähetyksen automaattisen vapautuksen toiminnolla taas on seuraavat ominaisuudet:

- Se tukee tarjontana vain tuotantotilauksia ja kysyntänä vain myyntitilauksia ja siirtotilauksia.
- Cross-docking-työvaihe voidaan aloittaa, vaikka kysyntätilausta ei vapautettu varastoon ennen tarjonnan vastaanoton rekisteröimistä (eli ennen tuotannon suoritetuksi ilmoittamista).

Tällä cross-docking-toiminnolla on kaksi etua:

- Varastotyövaiheessa voidaan ohittaa vaihe, jossa valmiin tavaran määriä siirretään tavalliselle varastointialueelle, jos kyseiset määrät vain kerätään uudelleen lähtevän tilauksen täyttämistä varten. Sen sijaan määrät voidaan siirtää kerran tuotossijainnista pakkaus-/lähetyssijaintiin. Siten toiminto auttaa pitämään varaston käsittelyjen määrän mahdollisimman pieninä ja saavuttamaan mahdollisimman suuria aika- ja tilasäästöjä varaston tuotannon puolella.
- Varastotyövaiheissa myynti- ja siirtotilausten vapauttamista varastoon voidaan lykätä, kunnes niihin liittyvän tuotantotilauksen valmiiden tavaroiden tuotos on ilmoitettu valmiiksi. Tämä etu voi olla erityisen merkittävä tilauksesta valmistamisen tuotantoympäristöissä, joissa tuotannon läpimenoajat ovat yleensä pidempiä kuin varastoon valmistamisen ympäristöissä.

## <a name="prerequisites"></a>Edellytykset

| Edellytys | Kuvaus |
|---|---|
| Kohde | Nimike on otettava käyttöön varastonhallintaprosesseille.<p>**Huomautus:** Tavaroita, joissa sovelletaan todellista painoa, ei voi sisällyttää cross-docking-prosesseihin.</p> |
| Varasto | Varastossa on oltava käytössä varastonhallintaprosessit. |
| Cross-docking-mallit | Jokaisessa varastossa on oltava käytössä vähintään yksi cross-docking-malli, jossa käytetään kysynnän vapautuskäytäntöä **Tarjonnan vastaanoton yhteydessä**. |
| Työluokka | **Cross-docking**-työtilaustyypille on luotava cross-docking-työluokan tunnus. |
| Työmallit | **Cross-docking**-työtilaustyypin työmallien on luotava cross-dockingin keräily- ja asetustöitä. |
| Sijaintidirektiivit | **Cross-docking**-työtilaustyypin sijaintidirektiivien on ohjattava asetustyö niihin sijainteihin, joissa myyntitilausten määrät pakataan ja lähetetään. |
| Kysyntätilausten ja tuotantotilausten merkitseminen | Varastojärjestelmä voi käynnistää lähtevän tilauksen lähetyksen vapautuksen automaattisesti ja luoda cross-docking-työn ilmoita valmiiksi -toiminnon tuotossijainnissa vain, jos myyntitilaukset ja siirtotilaukset on varattu ja merkitty vastaamaan tuotantotilausta. |

## <a name="example-cross-docking-flow"></a>Esimerkki cross-docking-kulusta

Tyypillinen cross-docking-kulku koostuu seuraavista päävaiheista.

1. Myyntitilauksen vastaanottaja luo myyntilauksen tilauksesta valmistettavalle tuotteelle. Yleensä pyydettyä määrää ei ole käytettävissä, ja se on ensin tuotettava.
2. Myyntitilauksen vastaanottaja luo tuotantotilauksen suoraan myyntilauksen rivin perusteella. Siten myyntitilauksen vastaanottaja varaa ja merkitsee myyntitilauksen määrän vastaamaan tuotantotilauksen määrää. 

    Vaihtoehtoisesti tuotantosuunnittelija voi määrittää, että merkintä on päivitettävä, kun suunniteltuja tilauksia vahvistetaan.

3. Tuotantotilaus kulkee seuraavien vaiheiden läpi:

    1. Tuotantosuunnittelija arvioi ja vapauttaa tuotantotilauksen. (Arvio sisältää raaka-aineiden varauksen ja vapautukseen kuuluu vapautus varastoon.)
    2. Varastotyöntekijä aloittaa ja suorittaa raaka-aineiden keräilyn varastointipaikasta tuotannon syöttösijaintiin tuotannon keräilytyön mukaisesti.
    3. Tuotantotyöntekijä käynnistää tuotantotilauksen.
    4. Viimeisessä toiminnossa koneenkäyttäjä ilmoittaa tuotantotilauksen valmiiksi mobiililaitteella.

4. Järjestelmä käyttää määritystä tunnistaakseen cross-docking-tapahtuman kahdelle toisiinsa liittyvälle tilaukselle ja suorittaa seuraavat tehtävät:

    1. Myyntitilauksen vapauttaminen varastoon lähetyksen luomista varten.
    2. Sellaisen cross-docking-työn automaattinen luonti, joka sisältää ohjeet valmiiden tavaroiden keräilyyn tuotossijainnista ja siirtämiseen cross-docking-sijaintidirektiivien myyntitilaukselle osoittamaan lähtösijaintiin.
    3. Pyynnön esittäminen koneenkäyttäjälle cross-docking-työn välittömäksi suorittamiseksi, kun tuotantotilaus on ilmoitettu valmiiksi.

5. Kun cross-docking-työ on saatu valmiiksi, kaikki määrät lastataan ajoneuvoon ja lähtevien varastosuunnittelija vahvistaa myyntilähetyksen.

## <a name="example-scenario"></a>Esimerkkiskenaario

Demotietojen on oltava asennettuja tässä skenaariossa, ja sinun on käytettävä **USMF**-demotietoyritystä.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Lähetyksen automaattisen vapautuksen toimintoa käyttävän cross-docking-työn määritys

#### <a name="cross-docking-template"></a>Cross-docking-malli

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Työ** \> **Cross-docking-mallilt**.
2. Valitse **Uusi**.
3. Syötä **Järjestysnumero**-kenttään arvo **1**.
4. Syötä **Cross-docking-mallin tunnus** kenttään nimi, kuten **XDock\_RAF**.
5. Valitse **Kysynnän vapautuskäytäntö** -kentässä **Tarjonnan vastaanoton yhteydessä**.
6. Syötä **Varasto**-kenttään sen varaston numero, jolle haluat määrittää cross-docking-prosessin. Valitse tässä esimerkissä **51**.

    > [!NOTE]
    > Heti kun valitset mallin kysynnän vapautuskäytännöksi **Tarjonnan vastaanoton yhteydessä**, kaikki muut sivun kentät poistuvat käytöstä. Et myöskään voi määrittää tarjontalähteitä. Tämä tapahtuu, koska lähetyksen automaattisen vapautuksen toimintoa käyttävä cross-docking tukee tarjontalähteinä vain tuotantotilauksia ja edellyttää myyntitilausten ja tuotantotilausten toisiaan vastaavia merkintöjä. Jos valitset kysynnän vapautuskäytännöksi **Ennen tarjonnan vastaanottoa**, välilehtien **Suunnittelu** ja **Tarjontalähteet** kentät ovat käytettävissä ja muokattavissa.

#### <a name="work-classes"></a>Työluokat

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Työ** \> **Työluokat**.
2. Valitse **Uusi**.
3. Syötä **Työluokan tunnus** -kenttään nimi, kuten **CrossDock**.
4. Valitse **Työtilaustyyppi**-kentässä **Cross-docking**.

Voit rajoittaa cross-dockingin kohteena olevien valmiiden tavaroiden sijoituspaikkojen tyyppejä määrittämällä vähintään yhden kelvollisen sijaintityypin.

#### <a name="work-templates"></a>Työmallit

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Työ** \> **Työmallit**.
2. Valitse **Työtilaustyyppi**-kentässä **Cross-docking**.
3. Valitse **Uusi**.
4. Syötä **Järjestysnumero**-kenttään arvo **1**.
5. Syötä **Työmalli** -kenttään nimi, kuten **CrossDock\_51**.
6. Valitse **Tallenna**.
7. Valitse **Työmallin tiedot** -osiosta **Uusi**.
8. Valitse **Työtyyppi**-kentän uudelle riville arvoksi **Keräily**. Valitse **Työluokan tunnus** -kentässä arvo**CrossDock**.
9. Valitse **Uusi**.
10. Valitse **Työtyyppi**-kentän uudelle riville arvoksi **Asetus**. Valitse **Työluokan tunnus** -kentässä arvo**CrossDock**.

#### <a name="location-directives"></a>Sijaintidirektiivit

Vakiomuotoinen valmiiden tavaroiden poispanoprosessi edellyttää **Asetus**-sijaintidirektiiviä ohjaamaan keräiltyjen tuotantomäärien siirtämistä tavalliseen varastointitilaan. Sinun on myös määritettävä **Asetus**-sijaintidirektiivi cross-dockingille ohjeeksi valmiin määrän asettamiselle määritettyyn lähtösijaintiin, jossa myyntitilauksen lähettäminen käsitellään.

Cross-dockingia tai tavallista valmiiden tavaroiden poispanoa varten sinun ei tarvitse luoda sijaintidirektiiviä keräilytyölle, koska tuotossijainti on annettu. Lisäksi oletetaan, että tämä tuotossijainti määritetään joko oletustuotossijainniksi jossakin resurssiin liittyvässä tietueessa (eli resurssissa, resurssiryhmän suhteissa tai resurssiryhmässä) tai varaston oletusarvoiseksi tuotannon valmiiden tavaroiden sijainniksi.

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Sijaintidirektiivit**.
2. Valitse **Työtilaustyyppi**-kentässä **Cross-docking**.
3. Valitse **Uusi**.
4. Syötä **Järjestysnumero**-kenttään arvo **1**.
5. Syötä **Nimi**-kenttään nimi, kuten **Baydoor**.
6. Valitse **Työtyyppi**-kentässä **Määritä**.
7. Valitse **Toimipaikka**-kentässä **5**.
8. Valitse **Varasto**-kentässä **51**.
9. Valitse **Rivit**-pikavälilehdessä **Uusi**.
10. Syötä **Määrään**-kenttään suurin sallittu määrä, kuten **1000000**.
11. Valitse **Tallenna**.
12. Valitse **Sijaintidirektiivien toiminnot** -pikavälilehdessä **Uusi**.
13. Syötä **Nimi**-kenttään nimi, kuten **Baydoor**.
14. Valitse **Tallenna**.
15. Voit käyttää kyselyn vakiosijaintia rajoittamaan asetussijainnit vähintään yhteen tiettyyn sijaintiin. Valitse **Muokkaa kyselyä** ja valitse **51** kriteeriksi **Varasto**-kentälle **Sijainnit**-taulukossa.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Valmiiden tavaroiden cross-docking lähtösijaintiin

Valmiin tavaramäärän cross-docking myyntitilauksen lähtösijaintiin tapahtuu seuraavia vaiheita noudattaen.

1. Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Valitse myyntitilausotsikolle asiakastili **US-001** ja varasto, joka on määritetty cross-dockingia varten ja käyttää lähetyksen automaattisen vapautuksen toimintoa.
4. Lisää rivi valmista tuotetta varten ja syötä määräksi **10**.
5. Valitse **Myyntitilausrivit**-osassa **Tuote ja tarjonta** \> **Tuotantotilaus**.
6. Tarkista oletusarvot **Luo tuotantotilaus** -valinta-ikkunassa ja valitse **Luo**. Uusi tuotantotilaus luodaan ja linkitetään myyntitilaukseen (eli se on varattu ja merkitty).
7. Valinnaista: Muuta **Määrä**-kentän arvo sitä arvoa suuremmaksi, joka tarvitaan myyntitilauksen täyttämiseksi. Kun tuotantomäärä ilmoitetaan valmiiksi, järjestelmä luo cross-docking-työn merkitylle määrälle ja poispanotyön jäljelle jäävälle määrälle valmiiden tavaroiden poispanon käsittelyn tavanomaisen menettelyn mukaisesti.

    Kuten aiemmin mainittiin, myyntitilauksella ja tuotantotilauksella on oltava toisiaan vastaava merkintä. Muuten cross-docking ei toimi. Merkintä voidaan luoda useilla tavoilla:

    - Järjestelmä voi luoda merkinnän automaattisesti seuraavissa tilanteissa:

        - Tuotantotilaus luodaan manuaalisesti suoraan myyntitilauksen rivin perusteella (katso vaihe 6).
        - Suunniteltuja tuotantotilauksia vahvistetaan ja **Päivitä merkintä** -kentän arvo on **Vakio**.

    - Käyttäjä voi luoda merkinnän manuaalisesti avaamalla kysyntätilauksen riviltä **Merkintä**-sivun.

    > [!NOTE]
    > Merkintää ei voi luoda manuaalisesti sellaisille nimikkeille, jotka on määritetty käyttämään varastomalleina vakio- ja painotettua keskiarvoa.

8. Valitse **Tuotantotilaus**-sivun toimintoruudun **Tuotantotilaus**-välilehden **Prosessi**-ryhmässä **Arvio** ja sitten **OK**. Tilaus arvioidaan ja raaka-ainemäärä varataan tuotantoon.
9. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Prosessi**-ryhmässä **Vapautus** ja sitten **OK**. Raaka-aineille luodaan varaston keräilytyö.
10. Avaa ja tarkista työ. Valitse toimintoruudun **Varasto**-välilehden **Yleinen**-ryhmässä **Työn tiedot**. Kirjoita työn tunnus muistiin.
11. Kirjaudu sisään varastosovellukseen ja suorita työ varastossa 51.
12. Siirry kohtaan **Tuotanto** \> **Tuotannon keräily**.
13. Aloita ja suorita raaka-aineiden keräily syöttämällä työn tunnus. 

    Kun työ on ilmoitettu valmiiksi, raaka-ainemäärä on saatavilla tuotannon syöttösijainnissa (**005** USMF-demotiedoissa) ja tuotantotilauksen täyttäminen voi alkaa.

14. Valitse **Tuotantotilaus**-sivun toimintoruudun **Tuotantotilaus**-välilehden **Prosessi**-ryhmässä **Aloita** ja sitten **OK**.
15. Siirry sovelluksessa kohtaan **Tuotanto** \> **Ilmoita valmiiksi ja pane pois**.
16. Syötä **Tuotetunnus**-kenttään tuotantotilauksen numero ja muut pakolliset tiedot ja valitse sitten **OK**.

Tällöin tapahtuu seuraavaa:

- Vapautus varastoon käynnistyy myyntitilauksen osalta.
- Vapautuksen perusteella luodaan lähetys- ja cross-docking-työ. Tämä työ kehottaa varastotyöntekijää keräilemään myyntitilauksen täyttämiseen tarvittavat määrät ja asettamaan ne cross-dockingin sijaintidirektiivissä määritettyyn lähtösijaintiin.
- Jos tuotantotilauksen määrä ylittää myyntitilauksen edellyttämän määrän, luodaan tavallinen poispanotyö. Tämä työ kehottaa varastotyöntekijää keräilemään cross-dockingin jälkeen jäljelle jääneet valmiit tavarat ja siirtämään ne tavalliseen varastointitilaan sijaintidirektiivin mukaisesti.
