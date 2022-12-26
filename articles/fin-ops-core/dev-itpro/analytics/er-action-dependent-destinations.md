---
title: Toiminnosta riippuvaisten ER-kohteiden määrittäminen
description: Tässä artikkelissa käsitellään lähteviä asiakirjoja luomaan määritetyn sähköisen raportoinnin (ER) muodon toiminnosta riippuvaisten kohteiden määrittämistä.
author: kfend
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 80a432a431891c02e4bf5c71cfe2bd9642c41c75
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843794"
---
# <a name="configure-action-dependent-er-destinations"></a>Toiminnosta riippuvaisten ER-kohteiden määrittäminen

[!include [banner](../includes/banner.md)]

[Kohteet](electronic-reporting-destinations.md) voidaan määrittää kullekin [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muodon [määrityksen](general-electronic-reporting.md#Configuration) tulosteosalle (kansio tai tiedosto), jota käytetään lähtevän asiakirjan luontiin. Tämän tyyppisen ER-muodon suorittavat käyttäjät, joilla on soveltuvat käyttöoikeudet, voivat myös muuttaa määritettyjä kohdeasetuksia suorituksen aikana.

Microsoft Dynamics 365 Financen **versiossa 10.0.17 ja sitä uudemmissa versioissa** ER-muoto voidaan suorittaa [valmistelemalla](er-apis-app10-0-17.md) toimintokoodi, jonka käyttäjä suorittaa suorittamalla ER-muodon. Esimerkiksi **Myyntireskontra**-moduulin tulostuksen hallinta-asetuksissa voidaan valita ER-muoto, joka luo tietyn liiketoiminta-asiakirjan, kuten vapaatekstilaskun. Lasku voidaan sitten esikatsella valitsemalla **Näytä** tai lähettää tulostimeen valitsemalla **Tulosta**. Jos käyttäjän toiminto siirretään suoritettavaan ER-muotoon suorituksen aikana, eri käyttäjän toimien eri ER-kohteita voidaan määrittää. Tässä artikkelissa käsitellään tämän tyyppisen ER-muodon ER-kohteiden määrittämistä.

## <a name="make-action-dependent-er-destinations-available"></a>Toiminnosta riippuvaisten ER-kohteiden tuominen käyttöön

Toiminnosta riippuvaiset ER-kohteet voidaan määrittää nykyisessä Finance-esiintymässä ja [uusi](er-apis-app10-0-17.md) ER-ohjelmointirajapinta ottaa käyttöön avaamalla [Ominaisuuksien hallinta](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) -työtila ja ottamalla **Määritä eri PM-toiminnoissa käytettävät ER-kohteet** -toiminto käyttöön. Raporttien määritettyjen ER-kohteiden käyttäminen suorituksen aikana edellyttää, että **ER-kohteeseen perustuvien käyttäjätoimikohtaisten PM-raporttien reittituloste (aalto 1)** -toiminto otetaan käyttöön.

## <a name="configure-action-dependent-er-destinations"></a>Toiminnosta riippuvaisten ER-kohteiden määrittäminen

Kun **Määritä eri PM-toiminnoissa käytettävät ER-kohteet** -toiminto otetaan käyttöön, toiminnosta riippuvaiset ER-kohteet voidaan määrittää **Sähköisen raportoinnin kohde** -sivun **Tiedostokohde**-pikavälilehdessä. Kuhunkin osaan voidaan lisätä tietue ja ottaa tietyt ER-kohteet käyttöön. Kullekin tietueelle on määritettävä asiakirjatyyppi, jossa määritettyjä ER-kohteita käytetään. Valitse **Asiakirjatyyppi**-kentässä jokin seuraavista arvoista:

- Valitse **Sähköinen**, jota käytetään määritetyissä kohteissa, jos mitään käyttäjän toimintokoodia ei anneta suorituksen aikana.
- Valitse **Tulostuksenhallinta**, jota käytetään määritetyissä kohteissa, jos käyttäjän toimintokoodi annetaan suorituksen aikana.
- Valitse **Mikä tahansa**, jota käytetään määritetyissä kohteissa aina riippumatta siitä, annetaan toimintokoodi annetaan suorituksen aikana.

Jos asiakirjatyypiksi valitaan **Tulostuksenhallinta**, ne käyttäjän toiminnot on määritettävä, joissa määritettyjä ER-kohteita on käytettävä. Valitse **Tulostuksenhallinnan toiminto** -kentässä jokin seuraavista arvoista:

- Valitse **Näytä**, jota käytetään määritetyissä kohteissa, jos käyttäjän **Näytä**-toiminto annetaan suorituksen aikana.
- Valitse **Tulosta**, jota käytetään määritetyissä kohteissa, jos käyttäjän **Tulosta**-toiminto annetaan suorituksen aikana.
- Valitse **Lähetä**, jota käytetään määritetyissä kohteissa, jos käyttäjän **Lähetä**-toiminto annetaan suorituksen aikana.

> [!NOTE]
> Yhteen kohdetietueeseen voidaan valita useita toimintoja.

Jos asiakirjatyypiksi valitaan **Mikä tahansa**, käyttäjän toiminnoksi valitaan automaattisesti **Automaattinen tunnistus** **Tulostuksenhallinnan toiminto** -kentässä. Tämä jälkeen tapahtuu seuraavaa:

- Jos mitään käyttäjän toimintokoodia ei anneta suorituksen aikana, kaikkia määritettyjä ER-kohteita käytetään.
- Jos käyttäjän toimintokoodi annetaan suorituksen aikana, tietylle toiminnolle esimääritettyä ER-kohdetta käytetään **riippumatta siitä, mitä on otettu käyttöön**:

    - Jos **Näytä**-toiminto annetaan suorituksen aikana, **Näyttö**-ER-kohdetta käytetään.
    - Jos **Lähetä**-toiminto annetaan suorituksen aikana, **Sähköposti**-ER-kohdetta käytetään.
    - Jos **Tulosta**-toiminto annetaan suorituksen aikana, **Tulostin**-ER-kohdetta käytetään.

**Vapaatekstilasku (Excel)** -ER-muodolla voidaan esimerkiksi tulostaa [vapaatekstilasku](../../../finance/accounts-receivable/create-free-text-invoice-new.md), kun se kirjataan. Luodun asiakirjan reititys edellyttää, että tämän ER-muodon ER-kohteet määritetään. Esimerkiksi seuraavat ER-kohteet on ehkä määritettävä suorittamaan seuraavat luodussa asiakirjassa:

- Asiakirjan arkistointi, jos ER-muoto suoritetaan mutta mitään toimintokoodia ei anneta (kun asiakirja esimerkiksi lähetetään sähköisesti).
- Asiakirjan esikatselu selaimessa, kun käyttäjä suorittaa **Näytä**- toiminnon.
- Asiakirjan arkistointi ja tulostus, kun käyttäjä suorittaa **Tulosta**-toiminnon.
- Asiakirjan arkistointi ja lähettäminen sähköpostitse lähtevän sähköpostiviestin liitteenä, kun käyttäjä suorittaa **Lähetä**-toiminnon.

Seuraava kuva osoittaa, miten tämä on mahdollista määrittämällä ER-kohteet yksittäisten kohdetietueiden joukkona, kun jokaiselle tietueelle on määritetty yksittäinen käyttäjän toiminto:

![Sähköisen raportoinnin kohdesivulla on ER-muodon toiminnosta riippuvaiset kohdeasetukset, kun jokaiselle kohdetietueelle on määritetty yksittäinen käyttäjän toiminto.](./media/er-destination-action-dependent-01.png)

Seuraava kuva osoittaa, miten sama tulos saavutetaan myös määrittämällä ER-kohteet yksittäisten kohdetietueiden joukkona, kun jokaiselle tietueelle on määritetty yksittäinen kohde:

![Sähköisen raportoinnin kohdesivulla on ER-muodon toiminnosta riippuvaiset kohdeasetukset, kun jokaiselle kohdetietueelle on määritetty yksittäinen kohde.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Jos suoritettavalle ER-muodolle annetaan toimintokoodi mutta kyseiselle toimintokoodille ei ole määritetty kohdetta, käytössä on [oletusarvoinen](electronic-reporting-destinations.md#default-behavior) kohdetoiminta.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Toiminnosta riippuvaisten ER-kohteiden muuttaminen suorituksen aikana

Jos käyttäjän toiminnot valmistelleilla käyttäjillä on soveltuvat [käyttöoikeudet](electronic-reporting-destinations.md#security-considerations) määritettyjen kohdeasetusten muuttamiseen suorituksen aikana, ER-muotoa suoritettaessa avautuu valintaikkuna, jossa on vaihtoehto määritettyjen kohdeasetusten muuttamiseen. Tämä valintaikkuna on valinnainen, ja sen esiintyminen määräytyy sen mukaan, miten ER-muodon suorittamisen kutsuva ER-kehys on toteutettu. Jos tämä valintaikkuna avautuu, siinä olevat ER-kohteet otetaan käyttöön annetun käyttäjän toiminnon mukaisesti.

Seuraavassa kuvassa on esimerkki **Sähköisen raportointimuodon kohteet** -valintaikkunasta, joka avautuu, kun vapaatekstilasku [kirjataan](../../../finance/accounts-receivable/create-free-text-invoice-new.md) ja **Vapaatekstilasku (Excel)** -ER-muoto suoritetaan luomaan tämä asiakirja, jos **Tulostin**-toiminto oli valmisteltu ja ER-kohteet oli määritetty tällä muodolla aiemmin tässä artikkelissa kuvatulla tavalla.

![Valintaikkuna, jossa on vaihtoehto suoritettavan ER-muodon aluksi määritettyjen ER-kohteiden muuttamiseen.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Jos suoritettavan ER-muodon useille osille on määritetty ER-kohteita, vaihtoehto annetaan erikseen kullekin ER-muodon määritetylle osalle.

Jos valitun asiakirjan raporttimalleina on käytettävissä useita ER-muotoja, kaikkien käytettävien ER-raporttimallien kaikki ER-kohteet näytetään valintaikkunassa ja niihin voi tehdä manuaalisia muutoksia varten suorituspalvelussa.

Jos yksikään [SQL Server Reporting Services (SSRS)](SSRS-report.md) -raporttimalli ei ole käytettävissä valitussa asiakirjassa, tulostuksenhallinnan kohteiden vakiovalinta piilotetaan dynaamisesti.

Financen versiosta **10.0.31** alkaen määritettyjä ER-kohteita voidaan muuttaa suorituksen aikana manuaalisesti seuraavissa liiketoiminta-asiakirjoissa:

- Asiakkaan tiliote
- Korkolasku
- Maksukehotus
- Asiakkaan maksuehdotus
- Toimittajan maksuehdotus

Mahdollisuus muuttaa ER-kohteita suorituksen aikana aktivoidaan ottamalla **Salli ER-kohteiden muuttaminen suorituksen aikana** -toiminto käyttöön [Ominaisuuksien hallinta](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) -työtilassa.

> [!IMPORTANT]
> **Asiakkaan maksuehdotus**- ja **Toimittajan maksuehdotus** -raporteissa mahdollisuus muuttaa ER-kohteita manuaalisesti on käytettävissä vain, jos **ForcePrintJobSettings**-väliversio on otettu käyttöön.

[![ER-kohteiden suorituksenaikainen muuttaminen](./media/ERdestinaiotnChangeUI.jpg)](./media/ERdestinaiotnChangeUI.jpg)

> [!NOTE]
> Kun **Käytä tulostuksenhallinnan kohdetta** -asetuksena on **Kyllä**, järjestelmä käyttää tietyille ER-raporteille määritettyjä ER-oletuskohteita. Kaikki valintaikkunassa tehdyt manuaaliset muutokset ohitetaan. Määritä **Käytä tulostuksenhallinnan kohdetta** -asetukseksi **Ei**, jos ER-kohteisiin käsitellään asiakirjoja, jotka on määritetty valintaikkunassa juuri ennen raporttien suorittamista.

Seuraavia liiketoiminta-asiakirjoja suoritettaessa käyttäjän ei nimenomaisesti oleta valitsevan toimintoa:

- Asiakkaan tiliote
- Korkolasku
- Maksukehotus
- Asiakkaan maksuehdotus
- Toimittajan maksuehdotus

Seuraavan logiikan avulla päätellään käytettävä toiminto edellisiä raportteja käsiteltäessä:

- Jos **ForcePrintJobSettings**-väliversio on otettu käyttöön:

    - Jos **Käytä tulostuksenhallinnan kohdetta** -asetuksena on **Kyllä**, **Tulosta**-toimintoa käytetään.
    - Jos **Käytä tulostuksenhallinnan kohdetta** -asetuksena on **Ei**, **Näytä**-toimintoa käytetään.

- Jos **ForcePrintJobSettings**-väliversiota ei ole otettu käyttöön:

    - Jos **Käytä tulostuksenhallinnan kohdetta** -asetuksena on **Kyllä**, **Tulosta**-toimintoa käytetään **Asiakkaan maksuehdotus**- ja **Toimittajan maksuehdotus** -raporteissa.
    - Jos **Käytä tulostuksenhallinnan kohdetta** -asetuksena on **Ei**, **Asiakkaan maksuehdotus**- ja **Toimittajan maksuehdotus** -raporteissa käytetään aina SSRS-raporttimallia riippumatta siitä, mitä ER-asetuksia on määritetty.
    - **Tulosta**-toimintoa käytetään aina **Asiakkaan tiliote**-, **Korkolasku**- ja **Maksukehotus**-raporteissa.

Edeltävässä logiikassa **Tulosta**- tai **Näytä**-toimintoa voi käyttää toimintokohtaisten ER-raporttikohteiden määrittämiseen. Suorituksen aikana ER-kohteet määritetään vain tietylle valintaikkunassa suodatettavalle toiminnolle.

## <a name="verify-the-provided-user-action"></a>Annetun käyttäjän toiminnon tarkistaminen

Tiettyä käyttäjän toimintoa suoritettaessa voidaan tarkistaa, mikä käyttäjän toiminto on mahdollisesti annettu suoritettavaa ER-muotoa varten. Tämä tarkistus on tärkeä, kun on määritettävä toiminnosta riippuvaisia ER-kohteita mutta ei ole varmuutta siitä, onko jokin käyttäjän toimintokoodi mahdollisesti annettu. Esimerkiksi vapaatekstilaskun kirjaamista aloitettaessa ja määritettäessä **Tulosta lasku** -asetukseksi **Kyllä** **Kirjaa vapaatekstilasku** -valintaikkunassa, **Käytä tulostuksenhallinnan kohdetta** -asetukseksi voidaan valita **Kyllä** tai **Ei**.

Annettu käyttäjän toimintokoodi tarkistetaan seuraavasti:

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. [Määritä](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) **Käyttäjän parametrit** -valintaikkunassa **Suorita vianmääritystilassa** -valinnaksi **Kyllä**.
4. Suorita käyttäjän toiminto suorittamalla ER-muoto. Muista, että ER-käyttäjän parametrit ovat yritys- ja käyttäjäkohtaisia.
5. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.
6. Etsi ER-muodon ajoloki suodattamalla ER-suorituslokeja **Määritysten virheenkorjauslokit** -sivulla.
7. Tarkista lokimerkinnät, joiden on sisällettävä annetun käyttäjän toimintokoodin ilmaiseva tietue, jos ER-muodon suoritukselle on annettu jokin toiminto.

    ![Sähköisen raportoinnin ajolokit -sivulla on tietoja käyttäjän toimintokoodista, joka on annettu ER-muodon suodatetusta ajosta.](./media/er-destination-action-dependent-03.png)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportointikehyksen ohjelmointirajapinnan muutokset Application update 10.0.17 -päivitystä varten](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
