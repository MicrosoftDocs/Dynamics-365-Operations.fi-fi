---
title: Ajoitusmoduulin "Kapasiteettia ei löytynyt riittävästi" -virheen ja rajallisen kapasiteetin korjaaminen
description: Tässä artikkelissa on tietoja ajoitusmoduulin "Tuotantotilausta %1 ei voitu ajoittaa. Kapasiteettia ei löytynyt riittävästi" -virheen syistä ja ratkaisuista.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135596"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Ajoistusmoduulin "Kapasiteettia ei löytynyt riittävästi" -virheen korjaaminen

[!include [banner](../includes/banner.md)]

Kun suoritat ajoitusta, saatat saada seuraavan virhesanoman:

> Tuotantotilauksen %1 ajoitus epäonnistui. Riittävää kapasiteettia ei löytynyt.

Ajoitusmoduulin toiminnan epäonnistumiseen ja tähän virhesanomaan voi olla monia syitä. Tämä artikkeli sisältää ohjeita, joiden avulla voit löytää virheen juurisyyn ja korjata sen.

## <a name="review-the-applicable-resources"></a>Käytettävissä olevien resurssien tarkasteleminen

Virhe voi ilmetä, jos käytettävissä olevat resurssit eivät täytä tuotantotilaussijainnin työvaihevaatimuksia.

Voit tarkastella sovellettavia resursseja noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Tuotannon ohjaus \> Tuotantotilaukset \> Kaikki tuotantotilaukset** ja avaa tai valitse tuotantotilaus, jota ei voi ajoittaa.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Tuotantotiedot**-ryhmässä **Reititys**.
1. Valitse **Tuotantoreititys**-sivulla työvaihe ja valitse sitten toimintoruudusta **Sovellettavat resurssit**.
1. Määritä **Sovellettavat resurssit** -valintaikkunassa **Käytä vaatimuksia kohteelle** -kentän arvoksi *Työvaiheajoitus* tai *Työajoitus* riippuen käyttämästäsi ajoitustyypistä.
1. Varmista, että tuotantotilaussijainnissa on sovellettavia resursseja.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Resursseihin kohdistettujen kalentereiden tarkastelu

Virhe voi ilmetä, jos resurssiin tai resurssiryhmään ei ole liitetty kalenteria tai jos siihen liitettyä kalenteria ei ole määritetty oikein (jos siinä ei esimerkiksi ole työaikoja tai sen tehokkuus prosenttiosuutena on 0 \[nolla\]).

Noudattamalla seuraavia ohjeita voit tarkistaa, että resurssiin tai resurssiryhmään on liitetty kalenteri.

1. Siirry kohtaan **Tuotannon ohjaus \> Tuotantotilaukset \> Kaikki tuotantotilaukset** ja avaa tai valitse tuotantotilaus, jota ei voi ajoittaa.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Tuotantotiedot**-ryhmässä **Reititys**.
1. Valitse **Tuotantoreititys**-sivulla työvaihe ja valitse sitten toimintoruudusta **Sovellettavat resurssit**.
1. Valitse **Sovellettavat resurssit** -valintaikkunassa resurssi ja valitse sitten **Näytä resurssi**. Vaihtoehtoisesti voit valita ja pitää **Resurssiryhmä**- kenttää painettuna (tai napsauttaa sitä hiiren kakkospainikkeella) ja valita sitten **Näytä tiedot**.
1. Varmista **Resurssit**-sivun tai **Resurssiryhmät**-sivun **Kalenterit**-pikavälilehdessä, että resurssille tai resurssiryhmälle on kohdistettu kalenteri.

> [!NOTE]
> Jos virhe tapahtuu työvaiheiden ajoituksen aikana, varmista, että kaikille sovellettaville resurssiryhmille on kohdistettu kalenteri.

Voit tarkastella kalenterin määritystä noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Organisaationhallinta \> Määritys \> Kalenterit \> Kalenterit** ja valitse resurssille tai resurssiryhmälle kohdistettu kalenteri.
1. Valitse toimintoruudussa **Työajat**.
1. Varmista **Työajat**-sivulla, että sivu ei ole tyhjä. Varmista lisäksi haluamiesi päivien osalta, että **Ohjaus**-kentän arvo ei ole *Suljettu*, että työaikoja on olemassa ja ettei **Nykyisen tehokkuuden prosenttiarvo** -kentän arvona ei ole *0* (nolla).

Jos kalenteri on yhdistetty peruskalenteriin, sinun on tarkistettava myös peruskalenterin määritys.

> [!NOTE]
> Työvaiheiden ajoituksessa resurssiryhmän kalenteria käytetään määrittämään kunkin työvaiheen aloituksen ja päättymisen ajat ja päivämäärät. Se myös rajoittaa aikaa, jonka järjestelmä voi varata yhdelle tietylle työvaiheelle yhtenä tiettynä päivänä yhdessä tietyssä resurssiryhmässä. Jos esimerkiksi resurssiryhmän työajat ovat tiettynä päivänä klo 8.00–16.00, yhden työvaiheen resurssiryhmälle aiheuttama kuormitus ei saa ylittää kahdeksaan tuntiin mahtuvaa kuormitusta riippumatta resurssiryhmän käytettävissä olevan kapasiteetin määrästä kyseisenä päivänä. Käytettävissä oleva kapasiteetti voi kuitenkin rajoittaa kuormitusta entisestään.

## <a name="review-the-scheduling-parameters"></a>Ajoitusparametrien tarkistus

Hyvän suorituskyvyn takaamiseksi ajoitusmoduuli hakee resurssia vain tietylle aikamäärälle ja sallii vain tietyn määrän ajoitusristiriitoja.

Tarkista ajoitusparametrit seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Organisaationhallinta \> Määritys \> Ajoitusparametrit**.
1. Noudata seuraavia ohjeita:

    - Jos **Ajoituksen aikakatkaisu käytössä** -asetuksen arvona on *Ei*, siirry vaiheeseen 3.
    - Jos **Ajoituksen aikakatkaisu käytössä** -asetuksen arvona on *Kyllä*, suurenna **Jaksokohtainen enimmäisajoitusaika** -kentän arvoa, jotta käsittelyllä on enemmän aikaa valmistua.

1. Noudata seuraavia ohjeita:

    - Jos **Ajoituksen optimoinnin aikakatkaisu käytössä** -asetuksen arvona on *Ei*, siirry vaiheeseen 4.
    - Jos **Ajoituksen optimoinnin aikakatkaisu käytössä** -asetuksen arvona on *Kyllä*, suurenna **Optimointiyritysten aikakatkaisu** -kentän arvoa, jotta käsittelyllä on enemmän aikaa valmistua.

1. Jos ole muuttanut jotakin sivun asetuksista, yritä uudelleen ajoittamalla tilaus uudelleen.

## <a name="review-capacity"></a>Kapasiteetin tarkistus

Virhe voi ilmetä, kun suoritetaan rajallinen ajoitus, mutta vapaata kapasiteettia ei ole.

Voit suorittaa rajattoman kapasiteettiajoituksen seuraamalla seuraavia ohjeita.

1. Siirry kohtaan **Tuotannon ohjaus \> Tuotantotilaukset \> Kaikki tuotantotilaukset** ja valitse tai avaa tuotantotilaus, jota ei voi ajoittaa.
1. Valitse toimintoruudun **Tuotantotilaus**-ryhmän **Ajoita**-välilehdessä **Ajoita työvaiheita** tai **Ajoita töitä**.
1. Määritä valintaikkunassa **Työvaiheiden ajoitus** tai **Töiden ajoitus** **Rajallinen kapasiteetti** -asetuksen arvoksi *Ei*.
1. Ajoita tilaus valitsemalla **OK**.

Voit tarkistaa resurssin käytettävissä olevan kapasiteetin noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Organisaationhallinta \> Resurssit \> Resurssit** ja valitse resurssi, joka on sovellettavissa tilaukseen, jota ei voi ajoittaa.
1. Valitse toimintoruudun **Näytä**-ryhmän **Resurssi**-välilehdessä **Kapasiteetin kuormitus** tai **Kapasiteetin kuormitus, graafisesti** ja varmista, että kapasiteettia on käytettävissä.

Voit tarkistaa resurssiryhmän käytettävissä olevan kapasiteetin noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Organisaationhallinta \> Resurssit \> Resurssiryhmät** ja valitse resurssiryhmä, joka on sovellettavissa tilaukseen, jota ei voi ajoittaa.
1. Valitse toimintoruudun **Näytä**-ryhmän **Resurssiryhmä**-välilehdessä **Kapasiteetin kuormitus** tai **Kapasiteetin kuormitus, graafisesti** ja varmista, että kapasiteettia on käytettävissä.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Yleissuunnittelu kirjaa resurssin, kun resurssikalenteri on suljettu

Kun työvaiheita ajoitetaan, pääsuunnittelu suunnittelee kapasiteetin ensisijaisen resurssiryhmän kalenterin mukaisesti. Se kirjaa toissijaisen työvaiheen yhtä aikaa kuin ensisijainen työvaihe, eikä se ota huomioon toissijaisen työvaiheen kalentereita tai kapasiteettia. Tällöin tuotantotilaus ajoitetaan suljettuun kalenteriin tai kun toissijainen työvaihe ei ole käytettävissä (kalenteri suljettu, ei kapasiteettia).

Töiden ajoitusta käytettäessä pääsuunnittelu ottaa huomioon sekä ensisijaisen että toissijaisen työvaiheen kapasiteetin ja kalenterin tilausta ajoitettaessa. Jotta tilaus voidaan ajoittaa, molempien työvaiheiden resurssien kalenterien on oltava avoimia ja niiden kapasiteetti on oltava käytettävissä.

## <a name="maximum-job-lead-time-is-too-short"></a>Työn enimmäisläpimenoaika on liian lyhyt.

Ajoitusmoduuli ei voi aikatauluttaa tilausta, jos toimipaikalle määritetty **Työn enimmäisläpimenoaika** on lyhyempi kuin läpimenoaika, joka on määritetty nimikkeelle tilauksen tai kattavuuden oletusasetuksissa.

Toimipaikan **Työn enimmäisläpimenoaika** -asetusta voi tarkastella tai muokata valitsemalla **Tuotannonhallinta \> Määritys \> Tuotannonhallinnan parametrit** ja avaamalla **Yleiset**-välilehden.

Nimikkeen oletustilausasetuksia voi tarkastella tai muokata seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi soveltuva tuote luettelosta ja valitse se.
1. Avaa toimintoruudussa **Hallitse varastoa** -välilehti ja valitse **Tilauksen oletusasetukset**.
1. Laajenna **Varasto**-pikavälilehti ja tarkastele tai muokkaa **Varaston läpimenoaika** -asetuksia tarpeen mukaan.

Nimikkeen kattavuusasetuksia voi tarkastella tai muokata seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi soveltuva tuote luettelosta ja valitse se.
1. Avaa toimintoruudun **Suunnitelma**-välilehti ja valitse **Nimikkeen kattavuus**.
1. Avaa **Läpimenoaika**-välilehti ja tarkastele tai muokkaa **Tuotantoaika**-arvoa tarpeen mukaan.

## <a name="excessive-quantity-of-required-resources"></a>Liian suuri määrä vaadittuja resursseja

Moduuli yrittää täsmäyttää ajoituksen aikana reitityksen työvaiheelle määritetyn vaaditun resurssimäärän käytettävissä oleviin resursseihin työvaiheen resurssitarpeiden mukaisesti. Resurssin määrän määrittäminen liian suureksi voi johtaa siihen, että reititys ei ole mahdollista, mikä tuottaa aikataulutusvirheen.

Sekä määritetty määrä että valitussa tuotteessa, reitityksessä ja reitityksen työvaiheessa käytettävissä olevat resurssit voidaan tarkistaa seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi soveltuva tuote ruudukossa ja valitse se.
1. Avaa toimintoruudun **Suunnittele**-välilehti ja valitse **Reititys**.
1. Etsi soveltuva reititys ruudukossa ja valitse se.
1. Avaa **Yleiskatsaus**-välilehti sivun alareunassa.
1. Valitse työvaihe valittujen reitityksen työvaiheiden luettelosta.
1. Avaa valintaikkuna, jossa voi tarkastella valitun reitityksen työvaiheen käytettävissä olevia resursseja, valitsemalla **Käytettävissä olevat resurssit**.
1. Avaa **Resurssin kuormitus** -välilehti. Tässä **Määrä**-kenttää näyttää valitussa reitityksen työvaiheessa vaadittu resurssin määrä. Tarkastele ja/tai muokkaa sitä tarpeen mukaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
