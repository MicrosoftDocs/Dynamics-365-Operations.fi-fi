---
title: Regulatory Configuration Services (RCS) – globalisointiominaisuudet
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) ja yleisen säilön käyttöä globalisointitoiminnon luontiin ja käyttöön.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002783"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) – globalisointiominaisuudet

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Servicesin (RCS) avulla voit luoda globalisointitoiminnon, jota voidaan käyttää esimerkiksi verkkolaskupalveluissa. RCS-toiminnon avulla voit suorittaa seuraavat tehtävät:

- Määritä ominaisuuden liittyvät komponentit.
- Hallitse ominaisuuden elinkaarta toiminnon tilan avulla.
- Määritä ominaisuus käytettäviksi määritetyille ympäristöille.
- Jaa ominaisuus muiden organisaatioiden kanssa.

Seuraavissa ohjeissa selitetään, kuinka RCS-käyttäjä voi lisätä globalisaatiotoiminnon ja siihen liittyvät komponentit, päivittää toiminnon tilan ja määrittää toiminnon käytettäväksi, jotta sitä voidaan käyttää globalisointipalveluissa.

Ennen kuin suoritat toimenpiteet, sinun on suoritettava seuraaviin tehtäviin liittyvät vaiheet:

- Pääsy RCS-esiintymään.
- Konfigurointipalvelun luominen ja aktivoiminen. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Noudata seuraavia ohjeita Finance and Operations -sovellusesiintymässä.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – määritys** -linkki ja valmistele sellainen ohjeiden mukaisesti.

> [!NOTE]
> Jos yritykseen on valmisteltu RCS-ympäristö, siirry ympäristöön sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.

## <a name="turn-on-the-globalization-features"></a>Globalisaatio-ominaisuuksien ottaminen käyttöön

1. Valitse RCS-esiintymässä **Ominaisuuksien hallinta** -ruutu.
2. **Valitse ominaisuuksien hallinta** -työtilassa luettelosta **globalisaation ominaisuudet** ja valitse sitten **Ota käyttöön nyt**.

    ![Globalisaatio-ominaisuudet ominaisuuksien hallinnassa](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalisaatio-ominaisuudet

Jos haluat käyttää globalisointiominaisuutta, sinun on ensin tuotava se yleisestä tietovarastosta ja luotava sen oma versio. Voit lisätä globalisaatiotoimintoja kahdella tavalla:

- Lisää johdettu ominaisuus, joka perustuu aiemmin julkaistuun tai jaettuun toimintoon.
- Lisää uusi luomasi ominaisuus tyhjästä.

## <a name="access-globalization-features"></a>Globalisaatio-ominaisuuksien käyttäminen

1. Varmista, että **globalisointitoiminnot** -toiminto on otettu käyttöön ominaisuuksien hallinnassa aiemmin tässä ohjeaiheessa kuvatulla tavalla.
2. Avaa uusi **globalisointitoiminnot** -työtila ja valitse sitten **Ominaisuudet**-kohdan **sähköinen laskutus** -ruutu.

    ![Yleiset ominaisuudet -työtila](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    **Sähköisen laskutuksen ominaisuudet** -sivu avautuu.

    ![Sähköisen laskutuksen ominaisuudet -sivu](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Johdetun globalisaatiotoiminnon lisääminen

Voit lisätä uuden globalisaatiotoiminnon määrittämällä sen aiemmin julkaistusta tai jaetusta toiminnosta.

1. Valitse **Tuo** avataksesi **Tuo toiminto yleisestä tietovarastosta**-sivun.

    ![Tuo toiminto yleiseltä tietovarastosivulta](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Saat uusimmat ominaisuudet valitsemalla **Synkronoi**.

    Synkronoidussa luettelossa on toimintoja, jotka ovat käytettävissä joko sen vuoksi, että Microsoft on julkaissut ne tai että toinen konfiguraatiotoimittaja on jakanut ne.

    ![Synkronoitu ominaisuuksien luettelo](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Valitse tuotavat ominaisuudet luettelosta ja valitse sitten **Tuo**. Näyttöön tulee sanoma, kun valittujen toimintojen tuominen onnistui.

    ![Sanoma onnistuneesta tuonnista](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Valitse **Lisää** ja valitse sitten avattavasta valintaikkunasta **Aiemmin luodun version perusteella** -vaihtoehto.
5. Kirjoita ominaisuuden nimi ja kuvaus.
6. Valitse käytettävissä olevien ominaisuuksien luettelosta ominaisuuden perusversio ja valitse sitten **Luo ominaisuus**.

    ![Johdetun ominaisuuden lisääminen](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Lisäämäsi ominaisuus luodaan, ja sen tila on **Luonnos**.

    ![Johdettu toiminto, jonka tila on luonnos](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Tarkista ominaisuuksien osista, tarvitaanko päivityksiä:

    - Tarkista konfiguraatiot, jos sinun on mukautettava sähköisen raportoinnin muotoja ja niiden sidontaa ominaisuusversion muotokartoituksilla.
    - Tarkista asetukset, jos sinun on mukautettava **Toiminnot**-välilehteä, **Soveltuvuussäännöt**-välilehteä tai ominaisuusversion **Muuttujat**-välilehteä.

8. Valitse **Versiot**-välilehdessä **Voimassa olon alkamispäivämäärä** ja kirjoita kuvaus, jos **Kuvaus**-kenttä on tyhjä.
9. Viimeistele toiminto valitsemalla **Muuta tilaa**. Valmiit toiminnot ovat käytettävissä tietyssä ympäristössä, jotta niitä voidaan käyttää globalisointipalveluissa tai ne voidaan julkaista yleiseen tietovarastoon.

> [!NOTE]
> Ominaisuudet, joiden **Ominaisuusversion tilan** arvo on **julkaistu**, voidaan jakaa ulkoisten organisaatioiden kanssa.

## <a name="add-a-new-globalization-feature"></a>Uuden globalisaatiotoiminnon lisääminen

Voit lisätä uuden globalisaatiotoiminnon luomalla sen alusta alkaen.

1. Valitse **Tuo toiminto yleisestä tietovarastosta** -sivulta **Lisää** ja valitse sitten avattavasta valintaikkunasta **Uusi ominaisuus** -vaihtoehto.
2. Kirjoita ominaisuuden nimi ja kuvaus.
3. Valitse **Luo ominaisuus**.

    ![Uuden ominaisuuden lisääminen](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Valitse **Versiot**-välilehdestä **Voimaantulo**-päivämäärä ja suorita sitten toiminto valitsemalla **Muuta tilaa**. Valmiit toiminnot ovat käytettävissä tietyssä ympäristössä, jotta niitä voidaan käyttää globalisointipalveluissa tai ne voidaan julkaista yleiseen tietovarastoon.

> [!NOTE]
> Ominaisuudet, joiden **Ominaisuusversion tilan** arvo on **julkaistu**, voidaan jakaa ulkoisten organisaatioiden kanssa.

## <a name="feature-component-overview"></a>Ominaisuuksien komponenttien yleiskatsaus

Globalisaatio-ominaisuuksilla on useita komponentteja:

- **Versio** – Tämä komponentti tukee ominaisuuksien elinkaaren hallintaa, ja sen avulla käyttäjät voivat hallita toiminnon eri versioiden tilaa.
- **Kokoonpanot** – Tämän komponentin avulla käyttäjät voivat hallita, tarkastella ja muokata toisiinsa liittyviä ER-muotoja ja muotomäärityksiä.
- **Asetukset** – Tämän osan avulla voit hallita järjestelmän palveluiden, kuten sähköisen laskutuspalvelun käyttäjien hallintatoimintoja. Näin ollen se tukee viestintä- ja vastaussääntöjen joustavaa rakentamista.
- **Ympäristö** – Tämän komponentin avulla voit käyttää globalisointipalveluja, kuten sähköistä laskutuspalvelua, hallita ympäristöä, jossa toiminnon version asetuksia käytetään, ja myöntää käyttöoikeuden käyttäjille, joilla on oikeus käyttää sitä.
- **Organisaatiot** – Tämän osan avulla käyttäjät voivat jakaa ominaisuuden ulkoisten organisaatioiden kanssa.

## <a name="configuring-feature-components"></a>Ominaisuuskomponenttien määrittäminen

### <a name="version-and-status"></a>Versio ja tila

Version avulla hallitaan globalisointitoiminnon elinkaarta.

Tilaa voi muuttaa **Versio**-välilehden **Tila**-kentässä. Käytettävissä ovat seuraavat tilat:

- **Vedos** – Ominaisuutta voi muokata vain, jos se on tässä tilassa.
- **Valmis** – Toiminto ja kaikki siihen liittyvät komponentit on viimeistelty (valmis), eikä niitä voi muokata.
- **Julkaistu** – Ominaisuus ja kaikki siihen liittyvät komponentit on julkaistu yleisessä tietovarastossa.
- **Jaettu** – Toiminto ja kaikki siihen liittyvät komponentit on jaettu ulkoisten organisaatioiden kanssa.
- **Käytössä** – Ominaisuus ja kaikki siihen liittyvät komponentit on otettu käyttöön globalisointipalvelussa, kuten sähköisen laskutuksen palvelussa.

> [!NOTE]
> Toimintojen on siirryttävä peräkkäin joihinkin näistä tiloista. Näin ollen kaikki tilat eivät välttämättä ole käytettävissä kaikissa elinkaarivaiheissa.

### <a name="configurations"></a>Konfiguraatiot

Konfiguroinneissa ovat käytettävissä seuraavat toiminnot:

- **Näytä** – Tarkastele pohjana olevia ominaisuuskonfiguraatioita, jotka eivät vaadi päivitystä.
- **Muokkaa** – Luo valitusta konfiguraatiosta luonnosversio, jotta voit muokata muotoa tai muotomääritystä muodon suunnittelijassa.
- **Poista** – Poista valittu konfiguraatio ominaisuudesta.
- **Uudelleenkäytä** – Ominaisuuden uudelleenkäyttäminen. Lisätietoja on jäljempänä tämän ohjeaiheen kohdassa [Uudelleenkäytä johdettuja globalisointiominaisuuksia](#rebase).

### <a name="setups"></a>Asetukset

Ominaisuuksien asennuksissa ovat käytettävissä seuraavat toiminnot:

- **Lisää** – Luo uusi ominaisuusasetus. Tämä ominaisuusmääritys voidaan määrittää aiemmin luodusta toimintomäärityksestä tai siitä, että se luodaan tyhjästä.
- **Poista** – Poista valitut ominaisuusmääritykset.
- **Näytä** – Tarkastele perusominaisuuksien asetuksia, jotka eivät edellytä muutoksia.
- **Muokkaa** – Luo, poista tai muokkaa ominaisuuksien asetusten kolmen pääkomponentin määritteitä:

    - Toimenpiteet ja niiden parametrit
    - Soveltuvuussäännöt
    - Muuttujat

![Ominaisuusversion asetussivu](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Ympäristöt

Ympäristöissä ovat käytettävissä seuraavat toiminnot:

- **Ota käyttöön** – Jos kyseessä on valittu toimintoversio, valitse julkaistu ympäristö ja valitse **voimassa olon alkamispäivämäärä**, kun se on käytettävissä. Lisätietoja on jäljempänä tämän ohjeaiheen kohdassa [Määritä ympäristöjä aktivointia varten](#configureenvironment).
- **Peruuta** – Poista ominaisuusasetusten ympäristö.

### <a name="organizations"></a>Organisaatiot

Voit jakaa globalisaatiotoiminnon ulkoisen organisaation kanssa noudattamalla seuraavia ohjeita.

1. **Valitse sähköisen laskutuksen ominaisuudet** -sivulla toiminto ja jaettava ominaisuusversio.
2. Valitse **Organisaatiot**-välilehdestä **Jaa seuraavan kanssa** -vaihtoehto ja kirjoita sitten avattavaan valintaikkunaan organisaation toimialueen nimi.
3. Valitse **Jaa**.

    ![Ominaisuuden jakaminen organisaation kanssa.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Ominaisuus jaetaan valitun organisaation kanssa, ja se on kyseisen organisaation käytettävissä yleisessä säilössä. Tällöin toiminto voidaan tuoda organisaation RCS-esiintymään tai Dynamics 365 Financeen niin, että sitä voidaan käyttää.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Johdettujen globalisaatiotoimintojen pohjustaminen

Voit määrittää uudelleen johdetun globalisaatiotoiminnon uuteen tai päivitettyyn perustoiminnon versioon. Näin perusversiossa tapahtuneet muutokset voidaan päivittää automaattisesti. Alkuperäinen konfigurointipalvelu luo päivitetyn perusominaisuuden version, jonka jälkeen se julkaistaan tai jaetaan.

![Päivitetty perustoiminnon versio](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Jos esimerkiksi haluat määrittää uudelleen luomasi ominaisuuden johdetun version, saat ensin toiminnon uusimman version tuomalla sen yleisestä tietovarastosta.

1. Valitse **sähköisen laskutuksen ominaisuudet** -sivulla **Tuo**.
2. Saat uusimmat ominaisuudet valitsemalla **Synkronoi**.
3. Valitse ominaisuusluettelosta tuotavat ominaisuudet ja valitse sitten **Tuo**.

    ![Toiminnon uusimman version tuominen](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Valitse ominaisuuksien luettelosta uudelleenperustoiminto.
5. Luo luonnosversio valitsemalla **Versio**-välilehdestä **Uusi**.

    ![Uusi luonnosversio on laadittu](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Valitse **Pohjusta**.
7. Valitse **Pohjusta**-valintaikkunassa sen toiminnon uusin versio, johon haluat pohjustaa uudelleen.

    ![Pohjusta-valintaikkuna](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Valitse **OK**.
9. Tarkista ominaisuuden komponentit ja tee tarvittavat muutokset.
10. Viimeistele pohjustettu toiminto valitsemalla **Muuta tilaa**. Kun pohjustus on saatu valmiiksi, voit suorittaa lisätoimenpiteitä. Voit esimerkiksi julkaista ominaisuuden ja määrittää sen käytettäviksi globalisointipalveluissa.

    ![Toiminnon tila päivitetty valmiiksi](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Ympäristöjen määrittäminen globalisaation ominaisuuksille

Globalisointipalveluiden käyttäjät voivat hallita ympäristöä niin, että ne määrittävät globalisointiominaisuuden ja myöntävät valtuutuksen muille käyttäjille, joilla on oikeus käyttää sitä.

1. Valitse **globalisointitoiminnot**-työtila ja **Ympäristöt**-kohdan **sähköinen laskutus** -ruutu.

    ![Globalisointiominaisuudet -työtila](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Valitse **Avainsäilöparametrit** ja luo Azure avainsäilön salaisuus valitsemalla **Uusi**.
3. Kirjoita avainsäilön nimi ja kuvaus ja kirjoita sitten **Avainsäilön URI** -kenttään URL-osoite, joka yksilöi avainsäilöresurssin Azure-tietokannassa.
4. Lisää sertifikaatti valitsemalla **sertifikaatit**-pikavälilehdessä **Lisää** ja kirjoita kunkin sertifikaatin nimi ja kuvaus.

    ![Sertifikaatti lisätty](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Luo uusi ympäristö valitsemalla **Uusi**.
6. Kirjoita nimi, kuvaus ja jaetun käyttöoikeuden allekirjoituksen tunnussanoma, jota tallennus edellyttää.
7. Lisää käyttäjä, jolla on oikeus käyttää tätä ympäristöä, valitsemalla **Käyttäjät**-pikavälilehdessä **Uusi**.
8. Kirjoita käyttäjän käyttäjätunnus ja sähköpostiosoite.
9. Voit lisätä muita käyttäjiä tekemällä kohtien 7 ja 8 toimet uudelleen.
10. Julkaise ympäristö valitsemalla **Julkaise**.

    ![Julkaistu ympäristö](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]