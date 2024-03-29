---
title: Vuokrasopimuksen lisääminen tai kopioiminen (esiversio)
description: Tässä artikkelissa kuvataan, miten uusi vuokrasopimus luodaan antamalla sille tietoja resurssin vuokrauksesta tai kopioimalla tiedot olemassa olevasta vuokrasopimuksesta.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880929"
---
# <a name="add-or-copy-leases-preview"></a>Vuokrasopimuksen lisääminen tai kopioiminen (esiversio)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten vuokrasopimus luodaan alusta alkaen resurssin vuokrauksessa ja miten vuokrasopimus luodaan kopioimalla olemassa oleva vuokrasopimus. Vuokrasopimuksen luontiprosessi alusta alkaen sisältää uuden vuokrasopimuksen tietojen syöttämisen ja uuden vuokrasopimusaikataulun luomisen. Kun vähintään yksi vuokrasopimus on määritetty, voi olla helpompaa kopioida tietoja olemassa olevasta vuokrasopimuksesta ja muokata sitten tietoja tarpeen mukaan uuden vuokrasopimuksen luomiseksi.

## <a name="create-a-lease"></a>Vuokrasopimuksen luominen

Näiden ohjeiden avulla voit luoda vuokrasopimuksen resurssin vuokrauksessa.

1. Valitse **Vuokrasopimusyhteenveto**-sivun toimintoruudussa **Uusi**.
2. Syötä vuokrasopimuksen tiedot. Pakollisilla kentillä on punaiset reunat.

Vuokramaksun alkamispäivämäärä ei voi olla ennen vuokrasopimuksen alkamispäivämäärää. Jos syötät vuokramaksun alkamispäivämäärän, joka on aiempi kuin vuokrasopimuksen alkamispäivämäärä, saat virhesanoman.

Oletusarvon mukaan **Vuokran tiedot** -sivun **Yleiset**-pikavälilehden **Erittelymaksusumma**-asetus on **Ei**, jos **Käyttöomaisuuden parametrit** -sivun **Salli maksuerittely** -asetus on **Kyllä**. 

Jos **Maksun erittelysumma** -asetus on **Kyllä**, **Maksusuunnitelmarivit**-pikavälilehden **Maksun summa** -kenttä on lukittu. Sen arvoksi määritetään maksun loppusummat, jotka syötetään myöhemmin **maksun summan erittely** -luetteloon.

Valitse **Maksun summan erittely**, kun haluat avata sivun, jolla voit lisätä eritettyjä maksutyyppejä. **Lisää kokonaissummat maksun summa** -painike siirtää summat **Maksun summa** -kenttään.

> [!NOTE]
> Jos lisäät eritellyn maksun summan ja valitset sitten **Esc**-näppäimen, määritettyjä summia ei lisätä **Maksuaikataulun rivit** -pikavälilehden **Maksusumma**-kenttään. Sen sijaan ne tallennetaan **Maksun summan erittely** -valintaikkunaan. Jos haluat, että valintaikkunassa näytetään kokonaissumma, valitse **Summa**-sarake, pidä painettuna (tai napsauta hiiren kakkospainikkeella) ja valitse sitten **Yhteensä tämä sarake**. 

**Kopioi rivi** -painike kopioi eritellyn maksuerittelyn.

## <a name="create-a-lease-schedule"></a>Vuokrasopimusaikataulun luominen

Kun olet syöttänyt vuokrasopimuksen tiedot, luo vuokrasopimusaikataulu seuraavasti.

> [!NOTE]
> Taloushallinnon dimensiot voivat muuttua mukautettujen taloushallinnon dimensioiden perusteella.

1. Luo vuokrauskirjat valitsemalla **Luo aikataulut**. Vuokrauskirjoja ovat maksu, kuoletus, poisto ja kuluaikataulut.
2. Jos haluat käyttää vuokrauskirjoja ja tarkastella juuri luotuja aikatauluja, valitse **Kirjat**-välilehti.

    **Kirjan tiedot** -sivulla on tietoja vuokrasopimuksen kirjaamisesta kirjoihin, jotka on kohdistettu sille. Tässä voit tarkastella vuokrasopimusaikatauluja.

    Maksuaikataulu sisältää syötteet **Maksuaikataulurivit**-välilehdestä **Lisää vuokrasopimus** -sivulla. Voit kuitenkin muuttaa kunkin maksusumman ja muuttuvan maksun. Vuokrasopimusvelka lasketaan muutetun maksuaikataulun mukaan.

    > [!NOTE]
    > Vuokranmaksun alkamispäivämäärän on oltava sama tai myöhempi kuin vuokran aloituspäivämäärä. Jos syötät vuokramaksun alkamispäivämäärän, joka on aiempi kuin vuokrasopimuksen alkamispäivämäärä, saat virhesanoman. 

4. Kun maksuaikataulun tarkastelu on päättynyt, valitse **Vahvista aikataulu**. Kun aikataulu on vahvistettu, vuokrasopimusta ei enää voi muokata.

    > [!NOTE]
    > Järjestelmä laskee automaattisesti vuokra-ajan maksuaikatauluriveiltä **Lisää vuokrasopimus** -sivulla.
    >
    > Jos haluat laskea vuokra-ajan kuukausina, järjestelmä löytää alkamis- ja päättymispäivämäärän välisen eron tietyltä maksuaikatauluriviltä. Sen jälkeen se siirtyy seuraavalle maksuaikatauluriville ja löytää eron uudelleen. Järjestelmä laskee lopuksi kaikki summat ja määrittää vuokra-ajan kuukausina.

5. Jos haluat tarkastella laskettuja kauden korkokuluja, avaa **Velan kuoletusaikataulu** -sivu. Jos haluat tarkastella laskettua tasapoistoa, avaa **Käyttöomaisuuden poistoaikataulu** -sivu.
6. Kun olet tarkistanut lasketun summan, voit luoda alkuperäisen tuloutuksen kirjauskansioviennin **Alkuperäinen tuloutus** -sivulla. Näyttöön tulee sanoma, joka ilmaisee, että kirjauskansio on luotu.

    > [!NOTE]
    > Kirjauskansiovienti kirjataan kirjanpitoon manuaalisesti.

7. Voit tarkistaa ehdotetun alkuperäisen tuloutuksen viennin ennen kirjaamista valitsemalla **Resurssin leasingkirjauskansio**.

    > [!NOTE]
    > Resurssin leasingkirjauskansiota ei voi luoda manuaalisesti. Se luodaan automaattisesti, kun vuokrasopimuksen aikataulut luodaan.

8. Kun olet tarkistanut alkuperäisen tuloutuksen kirjauskansioviennin ja se on valmis kirjattavaksi, valitse **Kirjaa** ja kirjaa käyttöoikeusomaisuuserä ja vuokrasopimusvelka kirjanpitoon.

## <a name="copy-a-lease"></a>Vuokrasopimuksen muokkaaminen

Käyttöomaisuuden vuokrauksen avulla voit kopioida vuokrasopimuksen tiedot ja luoda uuden vuokrasopimuksen samoilla tiedoilla. Tämän jälkeen voit muuttaa vuokrasopimuksen kenttiä, ennen kuin luot kopioidun vuokrasopimuksen aikataulut.

1. Valitse **Vuokrasopimusyhteenveto**-sivulla kopioita vuokrasopimus ja valitse sitten toimintoruudussa **Kopioi vuokrasopimus**.

    > [!NOTE]
    > Jos **Manuaalinen**-parametri on poistettu käytöstä vuokrasopimusten tunnusten numerojärjestystä varten, seuraava numero luodaan automaattisesti kopioidun vuokrasopimuksen tunnukselle. Jos **Manuaalinen**-parametri on otettu käyttöön, näytössä on sanoma, jossa pyydetään syöttämään vuokrasopimuksen tunnus ennen vuokrasopimuksen kopioimista.

2. Valitse **Kopioi**. Valitun vuokrasopimuksen tiedot kopioidaan uuteen vuokrasopimukseen. Tämän jälkeen voit muokata uuden vuokrasopimuksen tietoja ennen sen tallentamista. Voit myös luoda vuokrasopimuksen aikataulut.

## <a name="asset-leasing-journal"></a>Resurssin leasingkirjauskansio

Kaikki resurssin vuokrauksessa luodut kirjauskansioviennit sisältyvät resurssin leasingkirjauskansioon. **Resurssin leasingkirjauskansio** -sivulla (**Resurssin vuokraus \> Kirjauskansioviennit \> Resurssin leasingkirjauskansio**) voit suodattaa kirjauksen tilan mukaan, tarkastella tiettyjä kirjauskansiovientejä ja tositteita ja kirjata kirjaamattomia kirjauskansiovientejä.

> [!NOTE]
> Resurssin leasingkirjauskansiota ei voi luoda manuaalisesti. Se luodaan automaattisesti, kun vuokrasopimuksen aikataulut luodaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
