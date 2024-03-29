---
title: Optimointiavustajan yleiskuvaus
description: Tässä artikkelissa käsitellään optimaalisten talous- ja toimintosovellusten määritysten varmistamista optimointityökalun avulla.
author: kamaybac
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: f24e8dfecb04f928994bb5a197d32a7279022512
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281352"
---
# <a name="optimization-advisor-overview"></a>Optimointiavustajan yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään optimaalisten talous- ja toimintosovellusten määritysten varmistamista optimointityökalun avulla.

## <a name="overview"></a>Yleiskuvaus

Moduulin virheellinen määritys ja asetukset voivat vaikuttaa haitallisesti sovelluksen toimintoihin, järjestelmän suorituskykyyn ja liiketoimintaprosessien sujuvaan toimintaan. Liiketoimintatietojen laatu (kuten tietojen oikeellisuus, täydellisyys ja puhtaus) vaikuttaa myös järjestelmän suorituskykyyn sekä organisaation päätöksentekoon, tuottavuuteen jne.

**Optimointityökalu**-työtila on työkalu, jolla tehokäyttäjät, yritysanalyytikot, toiminnalliset konsultit ja IT-tukitoiminnot voivat tunnistaa moduulin määrityksiin ja liiketoimintatietoihin liittyvät ongelmat. Optimointiavustaja ehdottaa moduulin määritykselle parhaat käytännöt ja tunnistaa vanhentuneet tai virheelliset liiketoimintatiedot.

Optimointiavustaja suorittaa säännöllisesti parhaiden käytäntöjen säännöt. Oletussääntöjoukko on käytettävissä, mutta käyttäjät voivat luoda myös mukautuksia, riippumattomien ohjelmistotoimittajien ratkaisuja ja liiketoimintatietoja koskevia sääntöjä. Lisätietoja sääntöjen luomisesta on kohdassa [Optimointiavustajan sääntöjen luominen](./create-rules-optimization-advisor.md).

Kun sääntörikkomus havaitaan, luotava optimointimahdollisuus tulee näkyviin **Optimointityökalu**-työtilaan. Käyttäjä voi suorittaa korjaustoiminnot suoraan **Optimointityökalu**-työtilassa.

Mahdollisuudet voivat olla yrityskohtaisia tai yritysten välisiä tarkistettavien tietojen asetusten tyypin mukaan. Yritysten välisiä mahdollisuuksia voidaan katsella kaikista yrityksistä. Voit tarkastella tietyn yrityksen mahdollisuuksia valitsemalla ensin yrityksen.

Normaalit suojauskäytännöt koskevat optimointimahdollisuuksia. Esimerkiksi **Varastonhallinta**-moduuliin liittyvät optimointimahdollisuudet näkyvät vain käyttäjille, joilla on varastonhallinnan käyttöoikeus. He myös voivat muuttaa varastonhallinnan asetuksia.

Kun käytät joitain optimointimahdollisuuksia, järjestelmä laskee mahdollisuuden vaikutuksen liiketoimintaprosessien suorittamiseen kuluvan ajan vähennyksenä. Tämä ominaisuus ei ole valitettavasti käytettävissä kaikissa optimointimahdollisuuksissa.

Lisätietoja optimointineuvojasta on lyhyessä [Dynamics 365 Financein optimointineuvoja.](https://www.youtube.com/watch?v=MRsAzgFCUSQ) -videossa.

## <a name="optimization-rules"></a>Optimointisäännöt

Voit tarkastella optimointityökalun täydellistä sääntöluetteloa ja sääntöjen arviointivälejä valitsemalla **Järjestelmän hallinta** &gt; **Kausittaiset tehtävät** &gt; **Ylläpidä diagnostiikan vahvistussääntöä**. Vain säännöt, joiden tila on **Aktiivinen**, arvioidaan. Arviointiväliksi voidaan valita **Päivittäin**, **Viikoittain**, **Kuukausittain** tai **Ajastamaton**.

Voit käynnistää ajoittamattomien sääntöjen arvioinnin tai kausittaisten sääntöjen uudelleenarvioinnin määritetyn aikataulun ulkopuolella valitsemalla **Järjestelmän hallinta** &gt; **Kausittaiset tehtävät** &gt; **Aikatauluta diagnostiikan vahvistussääntö**. Valitse seuraavaksi **Diagnostiikkasäännön tarkistus** -valintaikkunassa arviointiväli. Kaikki säännöt, joilla on määritetty toistoväli, on arvioitava uudelleen.

Nykyiset optimointisäännöt voidaan jakaa seuraaviin luokkiin.

### <a name="module-configuration-and-setup"></a>Moduulin määritys ja asetukset

Varastonhallinnan määrittäminen on monimutkainen prosessi. Prosessin helpottamiseksi käyttöön on otettu sääntöjä, joilla voi tarkistaa asetusten oikeellisuuden. Esimerkiksi yksi sääntö tarkistaa tuotevarianttien kiinteiden sijaintien varaston sijaintidirektiivit myynti- ja siirtotilauksille.

Jotkin säännöt myös tarkistavat, ovatko käyttöön otetut toiminnot todella käytössä. Esimerkiksi yksi sääntö määrittää, onko käytössä **Pääsuunnittelu**-moduuli. Jos sääntö määrittää, että moduuli ei ole käytössä, luodaan suunnitteluprosessien käytöstäpoistoa ehdottava optimointimahdollisuus.

### <a name="system-configuration"></a>Järjestelmän konfigurointi

Jos tiettyjä konfigurointiavaimen ohjaamia toimintoja ei käytetä, luodaan konfigurointiavaimen käytöstäpoistoa ehdottava optimointimahdollisuus. Konfigurointiavainten esimerkkejä ovat **todellinen paino**, **budjetin suunnittelu**, **projekti** ja **hyväksyttyjen toimittajien luettelo**.

### <a name="business-data-consistency-and-cleanup"></a>Liiketoimintatietojen yhdenmukaisuus ja tyhjennys

Jos päätiedot eivät ole oikein (jos esimerkiksi yksiköiden mittayksikön muunnoksia ei ole määritetty tai jos mittayksikön muunnokset yrittävät jakaa luvulla 0 \[nolla\]), luodaan tietojen korjaamista ehdottava optimointimahdollisuus. 

Jos esimerkiksi erätyön historiamerkintöjä, vanhentuneita nimikkeitä ja varastoa käyttävien nimikkeiden suljettuja varastosaldomerkintöjä on liikaa tai jos nämä merkinnät ja nimikkeet ovat liian vanhoja, luodaan tietojen tyhjennystä ehdottavat optimointimahdollisuudet. Tietojen pitäminen puhtaina auttaa järjestelmän yleisen suorituskyvyn parantamisessa.

### <a name="best-practices"></a>Parhaat käytännöt

Optimointimahdollisuudet osoittavat parhaat käytännöt ja pyytävät noudattamaan niitä, jos joitakin liiketoimintaprosesseja ei suoriteta parhaiden käytäntöjen mukaan (jos esimerkiksi suoritetaan varaston sulkeminen ennakkoon ennen varaston sulkemista tai jos alareskontran kirjauskansion eräsiirrossa käytetään ajoitettua erää).

## <a name="optimization-opportunities"></a>Optimointimahdollisuudet

Voit tarkastella optimointisääntöjen arvioinnin aikana muodostettuja optimointimahdollisuuksia avaamalla **Optimointityökalu**-työkalun.

Näet mahdollisuutta koskevia lisätietoja tässä työtilassa, kun valitset **Lisätietoja**. Jos haluat, että järjestelmä esimerkiksi korjaa asetukset ja tyhjentää tiedot, jolloin sinun ei tarvitse avata kyseisiä sivuja itse, valitse **Suorita toiminto**.

Optimointimahdollisuuksilla ei ole työnkulkua. Kun olet valinnut **Suorita toiminto** -kohdan tai käyttänyt **Lisätietoja**-ikkunan siirtymispolkua, luettelon optimointimahdollisuus tulee näkyviin. Jos korjaava toiminto ei ratkaise ongelmaa kokonaan, mahdollisuus luodaan uudelleen taas, kun sääntö arvioidaan seuraavan kerran.

Jos mahdollisuus ei koske rooliasi, voit valita **Piilota luettelossa**. Vaikka tämän mahdollisuuden taustalla oleva sääntö käynnistetään jälleen, mahdollisuus ei näy luettelossa.

Voit poistaa tiettyjen sääntöjen aktivoinnin valitsemalla ensin säännön muodostaneen mahdollisuuden ja sitten **Poista analyysin aktivointi**.

## <a name="additional-resources"></a>Lisäresurssit

[Optimointiavustajan sääntöjen luominen](./create-rules-optimization-advisor.md)

[Dynamics 365 Financen optimointineuvoja (video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
