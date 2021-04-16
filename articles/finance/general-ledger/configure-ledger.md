---
title: Kirjanpitojen määrittäminen
description: Tässä ohjeaiheessa on tietoja kirjanpitojen määrittämisestä jokaiselle yritykselle. Se sisältää tietoja siitä, miten valuutat, tilikauden kalenterit, tilikartta ja tilirakenteet, joita käytetään kussakin yrityksessä.
author: kweekley
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aad10770750d2614da804380a7bba03d348e8c9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826200"
---
# <a name="configure-ledgers"></a>Kirjanpitojen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja kirjanpitojen määrittämisestä jokaiselle yritykselle. Se sisältää tietoja siitä, miten valuutat, tilikauden kalenterit, tilikartta ja tilirakenteet, joita käytetään kussakin yrityksessä.

## <a name="selecting-the-chart-of-accounts"></a>Tilikartan valitseminen

Jokaiselle Microsoft Dynamics 365 Financen yritykselle on määritettävä kirjanpidon tiedot. **Kirjanpito**-sivulla voit valita tilikartan ja tilirakenteen, joita käytetään valitussa yrityksessä. Voit jakaa tilikartan ja -rakenteet määrittämällä **Kirjanpito**-sivun kussakin yrityksessä niin, että ne käyttävät samaa tilikarttaa ja -rakennetta. Voit myös jakaa osan määrityksestä kussakin yrityksessä ja määrittää jokaiselle yritykselle erityiset määritykset.

Jos yrityksellä on oltava erilaiset tilikartat tai -rakenteet, yrityksen korvaustoiminto voi olla hyödyllinen. Voit yksinkertaistaa ylläpitoa käyttämällä samaa tilikarttaa ja -rakenteita useissa yrityksissä ja hallitsemalla mahdollisia poikkeuksia yrityksen korvausten avulla.

Jos haluat määrittää yrityksen tilikartat, siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito**. Valitse **Kirjanpito**-sivulla **Tilikartta** ja valitse sitten käytettävä tilikartta. Ota huomioon, että tilikarttaa ei voi muuttaa sen jälkeen, kun yrityksessä on valittu arvo ja kirjattu tapahtumia.

Lisätietoja tilikartan ja päätilien suunnittelemisesta ja määrittämisestä on kohdassa [Tilikartan suunnitteleminen](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Tilirakenteiden valitseminen

Kaikki Dynamics 365 Financen yritykset voidaan määrittää niin, että ne käyttävät yhtä tai useaa tilirakennetta. Kukin tilirakenne määrittää taloushallinnon dimensiot sekä päätilien että taloushallinnon dimensioiden yhdistelmät, jotka ovat sallittuja tapahtumien kirjaamisen yhteydessä. Voit käyttää samoja tilirakenteita useassa yrityksessä.

Ota huomioon, että jos tilirakenteita on useita, voit valita vain tilirakenteen, joka ei ole päällekkäinen päätilien ja taloushallinnon dimensioiden yhdistelmien kanssa. Yksi tilirakenne voi olla määritetty esimerkiksi lisäämään päätilien liiketoimintayksikkö välille 1 000 ja 1 999. Toisessa tilirakenteessa olet lisännyt osaston taloushallinnon dimension päätileille, jotka alkavat luvulla 1. Tässä tapauksessa vain yksi tilirakenne voidaan lisätä samaan yritykseen.

Voit määrittää kirjanpidon tilirakenteet **Kirjanpito**-sivulla **Tilirakenteet**-pikavälilehdessä valitsemalla **Lisää** ja valitsemalla sitten tilirakenteen luettelosta. Valitse lopuksi **Valitse**. Tilirakenteiden lisääminen ja tallentaminen voi kestää joitakin minuutteja. Huomaa, että valitsemiesi tilirakenteiden on oltava aktiivisia. Muussa tapauksessa tilirakenteiden tiedot eivät ole käytössä yrityksissä, joihin ne on linkitetty.

Voit poistaa tilirakenteen **Kirjanpito**-sivun **Tilirakenteet**-pikavälilehdessä **Poista**. Huomaa, että jos poistat tilirakenteen kirjanpidosta, et poista tapahtumia, jotka on kirjattu käyttämällä kyseisen tilirakenteen määritystä.

Lisätietoja tilirakenteiden määrittämisestä on kohdassa [Tilirakenteiden määrittäminen](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Kalentereiden määrittäminen kirjanpitoa varten

Kirjanpidon toinen osa on tilikauden kalenteri. Tilikauden kalenteri on valittava jokaiselle yritykselle. Voit käyttää samaa tilikauden kalenteria useassa yrityksessä. Kun valitset tilikauden kalenterin kirjanpitoa varten, tehdään kopio. Tätä kopiota kutsutaan kirjanpidon kalenteriksi. Kirjanpidon kalenterin avulla voit valita kausien ja moduulien tilan kullakin kaudella.

Voit käyttää valitun yrityksen kalenteria ja päivittää sen valitsemalla **Kirjanpito**-sivun toimintoruudussa **Kirjapidon kalenteri**.

Jos haluat valita kalenterin, valitse **Tilikauden kalenterit** ja valitse sitten kalenteri luettelosta. Jos muutat tilikauden kalenteria sen jälkeen, kun tapahtumat on kirjattu yritykseen, valitse **Laske kirjanpidon kaudet uudelleen**. Tämän jälkeen voit päivittää kalenterin kausien kirjanpitosaldot näkyviin tulevassa valintaikkunassa. On suositeltavaa suorittaa **Laske kirjanpidon kaudet uudelleen** -prosessi **erätilassa**. Se kannattaa suorittaa silloin, kun järjestelmässä on käynnissä vain ei-kriittisiä prosesseja. Tapahtumien ja taloushallinnon dimension yhdistelmien määrästä tämä prosessi voi kestää jonkin aikaa.

Jos yrityksessä ei ole valittu tilikauden kalenteria, näkyviin tulee virhesanoma, kun yrität kirjata yrityksen tapahtumaa.

Lisätietoja on kohdassa [Tilikalenterit, tilikaudet ja kaudet](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Täsmäyttävän taloushallinnon dimension käyttäminen

Kun olet valinnut tilikartan ja lisännyt vähintään yhden tilirakenteen, voit vaihtoehtoisesti valita yhden taloushallinnon dimension, jota käytetään täsmäyttävänä taloushallinnon dimensiona. Valitun dimension on oltava kaikissa tilirakenteissa. Se on myös täsmäytettävä kaikissa kirjanpitomerkinnöissä. Toisin sanoen veloitusten ja hyvitysten on oltava samat päätilillä ja täsmäyttävässä taloushallinnon dimensiossa. Järjestelmä luo tapahtumat automaattisesti vientien täsmäyttämistä varten niiden päätilien perusteella, jotka on määritetty **Yksiköiden välinen - hyvitys**- ja **Yksiköiden välinen - veloitus** -kentissä **Automaattisen tapahtuman tilit** -sivulla.

Lisätietoja täsmäyttävistä vienneistä on kohdassa [Yksiköiden välisen kirjanpidon täsmäytetyt kirjauskansiot](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Valuuttojen määrittäminen kirjanpitoa varten

**Kirjanpito**-sivua käytetään myös niiden valuuttojen hallinnassa ja määrittämisessä, joita käytetään kirjattaessa tapahtumia kirjanpitoon. Määritä kirjanpitovaluutta, joka on kaikkien tositteiden kirjanpidon **Kirjanpitovaluutta**-sarakkeessa käytettävä valuutta. Lisäksi **Raportointivaluutta**-sarakkeessa voit vaihtoehtoisesti valita toisen valuutan. Jos valitset raportointivaluutan, kaikki tapahtumat tallennetaan tänä valuuttana kaikkien tositteiden kirjanpidon **Raportointivaluutta**-sarakkeessa.

Jos tapahtumat kirjataan eri valuuttana, järjestelmä muuntaa tapahtumasumman automaattisesti tapahtumavaluutasta kirjanpitovaluutaksi ja raportointivaluutaksi tositteessa. Valitse **Kirjanpito**-sivun **Kirjanpitovaluutan vaihtokurssin tyyppi** -kentässä vaihtokurssi, joka on määritetty niille vaihtokursseille, joita käytetään muunnettaessa tapahtumavaluutta kirjanpitovaluutaksi tositteessa. Jos valitset raportointivaluutan, määritä myös **Raportointivaluutan vaihtokurssin tyyppi** -kenttä. Näin osoitetaan vaihtokurssi, jota käytetään muunnettaessa arvot tapahtumavaluutasta raportointivaluutaksi tositteessa.

Jos käytät budjetointitoimintoa, voit määrittää myös **Budjetin vaihtokurssin tyyppi** -kentän. Se osoittaa vaihtokurssin, jota käytetään muunnettaessa budjettitapahtumat valuutasta toiseen.

Jos käytät kahta valuuttaa tai jos käytät yhtä valuuttaa, mutta tapahtumat kirjataan eri valuuttana, määritä **Uudelleenarvostettavat tilit** -pikavälilehti **Kirjanpito**-sivulla. Tässä pikavälilehdessä määritetään toteutuneet ja toteutumattomat voitto- ja tappiotilit, joita käytetään oletusarvoisesti tapahtumien kirjaamisen yhteydessä, jos **Valuutan uudelleenarvostustilit** -sivulla ei ole määritetty tiliä. (**Valuutan uudelleenarvostustilit** -sivua käytetään eri tilien määrittämisessä toteutuneille ja toteutumattomille voitoille ja tappioille kussakin valuutassa.)

Toteutuneet voitot ja tappiot ovat tuottoja ja menetyksiä, jotka on saatu valmiista tapahtumista. Ne tallennetaan tuloslaskelmaan. Toteutumattomat voitot ja tappiot ovat tuottoja ja menetyksiä, jotka ovat materialisoituneet, mutta tapahtuma ei ole valmis. Toisin sanoen esimerkiksi lasku on kirjattu, mutta sitä ei ole vielä selvitetty ja maksettu. Toteutumattomat voitot ja tappiot tallennetaan taseeseen.

Lisätietoja kahden valuutan käyttämisestä on kohdassa [Kaksoisvaluutta](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]