---
title: Toiminnosta riippuvaisten ER-kohteiden määrittäminen
description: Tässä artikkelissa käsitellään lähteviä asiakirjoja luomaan määritetyn sähköisen raportoinnin (ER) muodon toiminnosta riippuvaisten kohteiden määrittämistä.
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7dfd92fd9e256298c13dcbde4b6da3f07d250d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876831"
---
# <a name="configure-action-dependent-er-destinations"></a>Toiminnosta riippuvaisten ER-kohteiden määrittäminen

[!include [banner](../includes/banner.md)]

[Kohteet](electronic-reporting-destinations.md) voidaan määrittää kullekin [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muodon [määrityksen](general-electronic-reporting.md#Configuration) tulosteosalle (kansio tai tiedosto), jota käytetään lähtevän asiakirjan luontiin. Tämän tyyppisen ER-muodon suorittavat käyttäjät, joilla on soveltuvat käyttöoikeudet, voivat myös muuttaa määritettyjä kohdeasetuksia suorituksen aikana.

Microsoft Dynamics 365 Financen **versiossa 10.0.17 ja sitä uudemmissa versioissa** ER-muoto voidaan suorittaa [valmistelemalla](er-apis-app10-0-17.md) toimintokoodi, jonka käyttäjä suorittaa suorittamalla ER-muodon. Esimerkiksi **Myyntireskontra**-moduulin tulostuksen hallinta-asetuksissa voidaan valita ER-muoto, joka luo tietyn liiketoiminta-asiakirjan, kuten vapaatekstilaskun. Lasku voidaan sitten esikatsella valitsemalla **Näytä** tai lähettää tulostimeen valitsemalla **Tulosta**. Jos käyttäjän toiminto siirretään suoritettavaan ER-muotoon suorituksen aikana, eri käyttäjän toimien eri ER-kohteita voidaan määrittää. Tässä artikkelissa käsitellään tämän tyyppisen ER-muodon ER-kohteiden määrittämistä.

## <a name="make-action-dependent-er-destinations-available"></a>Toiminnosta riippuvaisten ER-kohteiden tuominen käyttöön

Toiminnosta riippuvaiset ER-kohteet voidaan määrittää nykyisessä Finance-esiintymässä ja [uusi](er-apis-app10-0-17.md) ER-ohjelmointirajapinta ottaa käyttöön avaamalla [Ominaisuuksien hallinta](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) -työtila ja ottamalla **Määritä eri PM-toiminnoissa käytettävät ER-kohteet** -toiminto käyttöön. [Tiettyjen](#reports-list-wave1) raporttien määritettyjen ER-kohteiden käyttäminen suorituksen aikana edellyttää, että **Reititä käyttäjän toimintokohtaisiin ER-kohteisiin perustuvien PM-raporttien tulos (aalto 1)** -toiminto otetaan käyttöön.

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

## <a name=""></a><a name="reports-list-wave1">Liiketoiminta-asiakirjojen luettelo (aalto 1)</a>

**Reititä käyttäjän toimintokohtaisiin ER-kohteisiin perustuvien PM-raporttien tulos (aalto 1)** -toiminto hallitsee seuraavia liiketoiminta-asiakirjoja:

- Myyntilasku (vapaatekstilasku)
- Myyntilasku (myyntilasku)
- Ostotilaus
- Ostotilauksen ostokysely
- Myyntitilausvahvistus
- Maksukehotus
- Korkolasku
- Toimittajan maksuehdotus
- Tarjouspyyntö

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportointikehyksen ohjelmointirajapinnan muutokset Application update 10.0.17 -päivitystä varten](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
