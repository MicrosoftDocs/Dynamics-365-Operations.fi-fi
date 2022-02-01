---
title: Ajoitusmoduulin "Kapasiteettia ei löytynyt riittävästi" -virheen ja rajallisen kapasiteetin korjaaminen
description: Tässä ohjeaiheessa on tietoja ajoitusmoduulin "Tuotantotilausta %1 ei voitu ajoittaa. Kapasiteettia ei löytynyt riittävästi" -virheen syistä ja ratkaisuista.
author: ChristianRytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: becd537d37a8ba8931f2598dccbae8554a4d168e
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985027"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Ajoistusmoduulin "Kapasiteettia ei löytynyt riittävästi" -virheen korjaaminen

[!include [banner](../includes/banner.md)]

Kun suoritat ajoitusta, saatat saada seuraavan virhesanoman:

> Tuotantotilauksen %1 ajoitus epäonnistui. Riittävää kapasiteettia ei löytynyt.

Ajoitusmoduulin toiminnan epäonnistumiseen ja tähän virhesanomaan voi olla monia syitä. Tämä ohjeaihe sisältää ohjeita, joiden avulla voit löytää virheen juurisyyn ja korjata sen.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
