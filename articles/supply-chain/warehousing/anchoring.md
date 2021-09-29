---
title: Ankkurointi
description: Tässä aiheessa kerrotaan, miten ankkurointi otetaan käyttöön ja miten ankkurointia käytetään.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505565"
---
# <a name="anchoring"></a>Ankkurointi

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää tietoja ankkurointiprosessista. Se kuvaa vaadittavan konfiguraation ja suoritettavan logiikan, kun varastotyöntekijä muuttaa joko vaiheistus- tai lastaussijaintia.

Ankkurointitoiminnon avulla voit ohittaa vaiheistus- tai lastaussijainnin. Kaikki avoimet sijoitukset ohjataan sitten määrittämääsi uuteen vaiheistus- tai lastaussijaintiin.

Tämä ominaisuus voi auttaa työntekijöitä tehostamaan tuotteiden toimittamista. Seuraavassa on muutamia esimerkkejä:

- Työntekijä, jonka on pantava nimikkeitä tilaukselle 1 laiturin 1 vaiheistussijainnissa, ei voi tehdä työtään, koska edellinen kuorma ei ole poistunut sijainnista. Sen sijaan, että hän odottaisi laiturin 1 vaiheistussijainnin vapautumista, työntekijä päättää käyttää laiturin 2 vaiheistussijaintia. Näin ollen työntekijä korvaa ehdotetun vaiheistussijainnin. Työtilauksen sijoitussijainti kaikille työtilauksen jäljellä oleville nimikkeille päivitetään laiturin 2 vaiheistussijaintiin.
- Työntekijän, jonka on suoritettava useita poimintoja samaan toimitukseen, voi olla varma, että kaikki nimikkeet kootaan samaan paikkaan. Siksi nimikkeiden kuorma-autoon lastaamiseen tarvitaan vähemmän aikaa.

Voit määrittää ankkuroinnin mobiililaitteen valikkonimikkeille käyttämällä **Ankkuri**-vaihtoehtoa. Jos valitset *Kyllä*, voit käyttää **Ankkuroi**-kenttää määrittääksesi, haluatko ankkuroida lähetyksen vai kuorman mukaan. Jos määrität **Ankkuroi**-kentälle arvon *Lähetys*, kyseisen lähetyksen myöhemmät avoimet sijoitukset muutetaan uudelle sijainnille. Jos määrität kentän arvoon *Kuorma*, kyseisen kuorman myöhemmät avoimet sijoitukset muutetaan uudelle sijainnille.

> [!IMPORTANT]
> Seuraavien avointen sijoitusten sijaintia muutetaan vain niistä työriveistä, jotka luodaan samalta työmalliriviltä. Toisin sanoen järjestelmä ankkuroi sijoitusrivit, jotka ovat peräisin samasta työmallirivistä.

Tässä aiheessa esitellään skenaario, joka näyttää, miten ankkurointi toimii. Tämän skenaarion aikana luodaan myyntitilausjoukko, ja joukko vapautetaan varastoon. Tämän jälkeen ohitat ehdotetun vaiheistussijainnin ja varmistat, että kaikki jäljellä olevat hyllytystyöt on kohdistettu uuteen sijaintiin.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Skenaarion edellytykset: Esittelytietojen käyttö

Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu *USMF* ennen aloittamista.

## <a name="scenario-setup"></a>Skenaarion määrittäminen

Ennen kuin käyt läpi esimerkkiskenaarion, sinun on otettava käyttöön ankkurointi asiaankuuluvaa mobiililaitteen valikkonimikettä varten.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Määritä mobiililaitteen valikkonimike ottaaksesi ankkuroinnin käyttöön

Noudattamalla näitä ohjeita voit ottaa käyttöön ankkuroinnin mobiililaitteen valikkonimikettä varten.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Myynnin keräily*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista tai määritä tietueelle seuraavat arvot:

    - **Valikkokohteen nimi:** *Myynnin keräily*
    - **Nimike:** *Myynnin keräily*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*
    - **Ohjaus:** *Käyttäjän ohjaama*
    - **Ankkurointi:** *Kyllä*

        Tämä asetus aiheuttaa sen, että järjestelmä ankkuroi useita työtilausrivejä yhteen myynnin keräilyn aikana.

    - **Ankkuroi:** *Kuorma*

        Tämä asetus aiheuttaa sen, että järjestelmä ankkuroi kuorman mukaan.

    - **Ohita kohderekisterikilpi:** *Kyllä*
    - **Ohita rekisterikilpi asetuksen aikana:** *Kyllä*
    - **Pidä työ käyttäjän lukitsemana:** *Kyllä*
    - **Salli ylikeräily:** *Kyllä*

### <a name="set-up-a-work-template-to-enable-staging"></a>Määritä työmalli ottaaksesi vaiheistuksen käyttöön

Seuraavia ohjeita noudattamalla voit määrittää työmallin ottaaksesi vaiheistamisen käytöön. Tämä konfigurointi tukee skenaariota, jossa työntekijä laittaa nimikkeitä tilaukseen vaiheistamissijainnissa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.
1. Valitse ruudukossa **61 SO Stage** -työmalli.
1. Varmista **Työmallin tiedot** -osassa, että seuraavat rivit ovat olemassa ja että ne on konfiguroitu seuraavasti:

    - Rivi 1:

        - **Työtyyppi:** *Poiminta*
        - **Pakollinen:** valittu (= *Kyllä*)
        - **Työluokan tunnus:** *Myyntitilauksen keräily*

    - Rivi 2:

        - **Työtyyppi:** *Aseta*
        - **Pakollinen:** valittu (= *Kyllä*)
        - **Direktiivin koodi:** *Vaihe*
        - **Työluokan tunnus:** *Myyntitilauksen keräily*

    - Rivi 3:

        - **Työtyyppi:** *Poiminta*
        - **Pakollinen:** valittu (= *Kyllä*)
        - **Pysäytä työ:** *Kyllä*
        - **Työluokan tunnus:** *SO Load*

    - Rivi 4:

        - **Työtyyppi:** *Aseta*
        - **Pakollinen:** valittu (= *Kyllä*)
        - **Direktiivin koodi:** *Baydoor*
        - **Työluokan tunnus:** *SO Load*

1. Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata kyselyeditorin.
1. Varmista **Alue** -välilehdessä, että seuraava rivi on olemassa:

    - **Taulukko:** *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
    - **Kenttä:** *Varasto*
    - **Ehdot:** *61*

1. Varmista **Lajittelu** -välilehdessä, että seuraava rivi on olemassa:

    - **Taulukko:** *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
    - **Kenttä:** *Lähetyksen tunnus*
    - **Hakusuunta:** *Laskeva*

1. Ota asetukset käyttöön valitsemalla **OK** ja sulje kyselyeditori. Hyväksy muutokset, jos näyttöön tulee kehote.
1. Valitse toimintoruudussa **Työn otsikoiden katkaisut**.
1. Varmista rivillä, jolla **Kentän nimi** -kenttä on määritetty arvoon *Lähetyksen tunnus*, että **Ryhmittele tämän kentän mukaan** -valintaruutu on valittuna.

### <a name="set-up-license-plates-locations-and-inventory"></a>Määritä rekisterikilvet, sijainnit ja varasto

Ennen myyntitilausten ja lähetysten luontia sinun on varmistettava, että tarvittavat sijainnit, rekisterikilvet ja varasto ovat olemassa.

1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varasto \> Rekisterikilvet** ja luo kaksi rekisterikilpeä:

    - MyLP1
    - MyLP2

1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varasto \> Sijainnit** ja luo seuraavat sijainnit, jos ne eivät ole jo olemassa.

    | Varasto | Toimipaikka   | Sijainnin profiilitunnus | Vyöhyketunnus   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | KERROS     |
    | 61        | 06A01R3S1B | PICK-06             | KERROS     |
    | 61        | STAGE01    | STAGE               | *(Tyhjä)* |
    | 61        | STAGE02    | STAGE               | *(Tyhjä)* |
    | 61        | STAGE03    | STAGE               | *(Tyhjä)* |
    | 61        | STAGE04    | STAGE               | *(Tyhjä)* |

1. Varmista, että seuraava varasto on käytössä. Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta.

    | Nimiketunnus | Määrä | Varasto | Toimipaikka   | Rekisterikilpi |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Luo kysyntää

Ennen kuin voit kokeilla ankkurointitoimintoa, sinun on luotava kysyntää. Tässä skenaariossa luot samalle asiakkaalle kolme myyntitilausta.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse **Uusi** luodaksesi ensimmäisen myyntitilauksen.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-001*
    - **Varasto**: *61*

1. Valitse **OK**.
1. Uusi myyntitilaus avataan. Se sisältää tyhjän rivin **Myyntitilausrivit**-pikavälilehdessä. Määritä seuraavat tämän rivin arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *1*

1. Lisää työkalupalkissa toinen ostotilausrivi valitsemalla ruudukon yläpuolelta **Lisää rivi** ja määritä sille seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *1*

1. Varaa varastoa noudattamalla seuraavia vaiheita tilauksen kunkin tilausrivin osalta:

    1. Valitse **Myyntitilausrivit**-pikavälilehdessä myyntitilausrivi.
    1. Valitse työkaluriviltä **Varasto \> Varaus**.
    1. Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.
    1. Valitse toimintoruudussa **Tallenna**.

1. Luo toinen myyntitilaus toistamalla vaiheet 2–6. Määritä sille seuraavat arvot:

    - **Luo myyntitilaus** -valintaikkunassa:

        - **Asiakastili:** *US-001*
        - **Varasto**: *61*

    - Myyntitilausrivillä 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *2*

    - Myyntitilausrivillä 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *2*

1. Toista vaihe 7, jos haluat varata kunkin rivin myyntitilauksessa 2.
1. Luo kolmas myyntitilaus toistamalla vaiheet 2–6. Määritä sille seuraavat arvot:

    - **Luo myyntitilaus** -valintaikkunassa:

        - **Asiakastili:** *US-001*
        - **Varasto**: *61*

    - Myyntitilausrivillä 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *3*

    - Myyntitilausrivillä 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *3*

1. Toista vaihe 7, jos haluat varata kunkin rivin myyntitilauksessa 3.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Käytä kuormasuunnittelun workbenchiä luodaksesi kuorman ja vapauttaaksesi sen varastoon

Noudata seuraavia vaiheita luodaksesi kuorman tilauksille, jotka loit tälle skenaariolle ja vapauta se sitten varastoon.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Hae ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit myyntitilaukselle 1 ja myyntitilaukselle 2.
1. Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**.
1. Valitse **Lataa mallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *Vakiokuormamalli*.
1. Sulje valintaikkuna valitsemalla **OK**.
1. Etsi ja valitse luotu kuorma **Kuormat**-osassa.
1. Valitse työkalurivillä **Vapauta \> Vapauta varastoon**.
1. Vapauta valittu kuorma varastoon valitsemalla **Vapauta kuorma varastoon** -valintaikkunassa **OK**.
1. Voit tarkastella luotua työtä valitsemalla **Varastonhallinta \> Työ \> Kaikki työt**. Sinun pitäisi nyt nähdä kaksi uutta työtunnusta, yksi molemmille lähetyksille. Jokaisella työtunnuksella on keräys- ja sijoitusrivit, jotka vievät varaston keräyssijainnista vaiheistussijaintiin ja vaiheistussijainnista ovelle. Kirjoita ensimmäisen lähetyksen **Työtunnus**-arvo muistiin, sillä sitä tarvitaan seuraavassa menettelyssä.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Ensimmäisen lähetyksen myyntitilauksen keräily vaiheistussijaintiin

1. Kirjaudu Warehouse Managementin mobiilisovellukseen työntekijänä varastossa *61*. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella _61_ ja salasanalla _1_.)
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Myynnin keräily**.
1. Valitse **Tunnus**-kenttä ja syötä sitten ensimmäisen lähetyksen työtunnus.
1. Vahvista kirjaus.
1. Syötä **LP**-kentässä ensimmäisen nimikkeen rekisterikilven numero (*MyLP1*).
1. Vahvista kirjaus.
1. Syötä **Kohteen LP** -kenttään mikä tahansa numero (kohteen rekisterikilven numeron ei tarvitse olla vielä olemassa).

    Voit kerätä kaikki käsitellystä aallosta luodut rivit samaan kohderekisterikilpeen.

1. Vahvista kirjaus.
1. Syötä **LP**-kentässä toisen nimikkeen rekisterikilven numero (*MyLP2*).
1. Vahvista kirjaus.

    Kuvittele, että työntekijä on nyt kerännyt tilauksen, mutta kun hän tulee työssä määritettyyn vaiheistussijaintiin, hän havaitsee, että paikka on jo varattu. Työntekijä näkee kuitenkin, että toinen lähellä oleva sijainti (*STAGE03*) on käytettävissä. Niinpä hän pyytää muutosta vaiheistussijaintiin. Koska ankkurointitoiminto on käytössä, järjestelmä päivittää vaiheistussijainnin automaattisesti tähän työhön ja kaikkiin liittyviin töihin.

1. Valitse **Ohita sijainti** ohittaaksesi ehdotetun vaiheistussijainnin.
1. Määritä **Työn poikkeukset** -kentässä *Vaiheistuslinja muutettu*.
1. Syötä **Sijainti**-kenttään uusi vaiheistussijainti (*STAGE03*).
1. Vahvista kirjaus. Näyttöön tulee Työ valmis -sanoma.
1. Valitse **Varastonhallinta \> Työ\> Kaikki työt**.
1. Avaa ensimmäisen lähetyksen työtunnus. Tarkista, että vaiheistussijainti päivitettiin uuteen sijaintiin (*STAGE03*), joka on määritettiin mobiililaitteella.
1. Avaa toisen lähetyksen työtunnus. Tarkista, että vaiheistussijainti päivitettiin uuteen vaiheistussijaintiin (*STAGE03*) ankkurointimäärityksen vuoksi.

> [!NOTE]
> Kaikkien jäljellä olevien avointen sijoitustyörivien, joilla on sama vaiheistussijainti ja jotka muodostettiin samasta työmallirivistä, sijannit päivitetään uuteen sijaintiin.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Lisää uusi myyntitilaus aiemmin luotuun kuormaan kuormitussuunnittelun workbenchin avulla

Seuraavia ohjeita noudattamalla voit lisätä tilauksen kuormaan ja vapauttaa sen sitten varastoon.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Hae ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit myyntitilaukselle 3.
1. Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää** -ryhmässä **Aiemmin luotuun kuormaan** lisätäksesi valitut tilausrivit aiemmin luotuun kuormaan.
1. Sulje valintaikkuna valitsemalla **OK**.
1. Etsi ja valitse edellisissä vaiheissa luotu kuorma **Kuormat**-osassa.
1. Valitse **Vapauta \> Vapauta varastoon**.
1. Vapauta valittu kuorma varastoon valitsemalla **Vapauta kuorma varastoon** -valintaikkunassa **OK**.
1. Voit tarkastella luotua työtä valitsemalla **Varastonhallinta \> Työ \> Kaikki työt**. Kirjoita **Työtunnus**-arvo muistiin, sillä sitä tarvitaan seuraavassa menettelyssä.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Kolmannen lähetyksen myyntitilauksen keräily vaiheistussijaintiin

1. Kirjaudu mobiilisovellukseen työntekijänä varastossa *61*.
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Myynnin keräily**.
1. Valitse **Tunnus**-kenttä ja syötä sitten kolmannen lähetyksen työtunnus.
1. Vahvista kirjaus.
1. Syötä **LP**-kentässä ensimmäisen nimikkeen rekisterikilven numero (*MyLP1*).
1. Vahvista kirjaus.
1. Syötä **Kohteen LP** -kenttään mikä tahansa numero (kohteen rekisterikilven numeron ei tarvitse olla vielä olemassa).
1. Vahvista kirjaus.
1. Syötä **LP**-kentässä toisen nimikkeen rekisterikilven numero (*MyLP2*).
1. Vahvista kirjaus.

    Kuten ensimmäisessä kuormassa, kuvittele, että työntekijä löytää määritetyn vaiheistussijainnin, joka ei ole käytettävissä. Siksi hän haluaa käyttää eri vaiheistussijaintia (*STAGE04*).

1. Valitse **Ohita sijainti** ohittaaksesi ehdotetun vaiheistussijainnin.
1. Määritä **Työn poikkeukset** -kentässä *Vaiheistuslinja muutettu*.
1. Syötä **Sijainti**-kenttään uusi vaiheistussijainti (*STAGE04*).
1. Vahvista kirjaus. Näyttöön tulee Työ valmis -sanoma.
1. Valitse **Varastonhallinta \> Työ\> Kaikki työt**.
1. Avaa ensimmäisen lähetyksen työtunnus. Varmista, ettei vaiheistussijaintia päivitetty uuteen vaiheistussijaintiin (*STAGE04*), koska jäljellä oleva avoin sijoitusrivi ei vastaa valmiin sijoitusrivin työmalliriviä.
1. Avaa toisen lähetyksen työtunnus. Varmista, ettei vaiheistussijaintia päivitetty uuteen vaiheistussijaintiin (*STAGE04*), koska vaiheistussijainti ei vastaa valmiin sijoitusrivin vaiheistussijaintia. Toisin sanoen valmiilla sijoitustyörivillä ja jäljellä olevalla avoimella työrivillä on eri vaiheistussijainnit, ja tällöin päivitetään vain rivit, joissa on samat vaiheistussijainnit.
1. Avaa kolmannen lähetyksen työtunnus. Tarkista, että vaiheistussijainti päivitettiin uuteen vaiheistussijaintiin (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
