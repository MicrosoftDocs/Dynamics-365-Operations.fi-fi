---
title: Commerce-kanavien kirjanpidon integroinnin yleiskatsaus
description: Tämä ohjeaihe on yleiskatsaus Dynamics 365 Commercen kirjanpidon integrointitoiminnoista.
author: EvgenyPopovMBS
manager: annbe
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 35612714f9443f1f37b744d87eda373df84aaadd
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343284"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Commerce-kanavien kirjanpidon integroinnin yleiskatsaus

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe on yleiskatsaus Dynamics 365 Commercen kirjanpidon integrointitoiminnoista. 

Kirjanpidon integrointi sisältää sellaisten erilaisten kirjanpidon laitteiden ja palvelujen integroinnin, joilla kirjanpidon rekisteröinti voidaan ottaa myynnissä käyttöön paikallisten, vähittäismyyntialan veropetoksia estävän kirjanpitolainsäädännön mukaisesti. Kirjanpidon integraatiota voidaan esimerkiksi seuraavissa tyypillisissä skenaarioissa:

- Myynnin rekisteröinti kirjanpidon laitteessa, joka on liitetty myyntipisteeseen (POS), kuten kuittitulostimeen, ja verokuitin tulostaminen asiakkaalle.
- Retail POS:ssä suoritettuun myyntiin ja palautuksiin liittyvien tietojen lähettäminen turvallisesti ulkoiseen, veroviranomaisen ylläpitämään verkkopalveluun.
- Myynnin tapahtumatietojen muuttamattomuuden takaaminen digitaalisella allekirjoituksella.

Kirjanpidon integrointitoiminto on kehikko, joka muodostaa yhteisen ratkaisun Retail POS:n sekä kirjanpidoin laitteiden ja palvelujen kehittämiselle ja mukauttamiselle edelleen. Toiminto sisältää myös kirjanpidon integrointimalleja, jotka tukevat tiettyjen maiden tai alueiden perusskenaariota ja joita voi käyttää tiettyjen kirjanpidon laitteiden tai palvelujen kanssa. Kirjanpidon integrointimalli koostuu useista Commerce-osien laajennuksista, ja se sisältyy SDK:hon. Lisätietoja kirjanpidon integroinnin esimerkeistä on kohdassa [Kirjanpidon integroinnin esimerkit – Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Lisätietoja Commerce SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Jos haluat tukea skenaarioita, joita kirjanpidon integrointimalli ei tue, integroida Retail POS:n muiden kirjanpidon laitteiden ja palvelujen kanssa tai ottaa huomioon muiden maiden tai alueiden vaatimukset, sinun on joko laajennettava nykyistä kirjanpidon integrointimallia tai luotava uusi malli käyttämällä nykyistä mallia esimerkkinä.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden kirjanpidon integrointimallit

Retail POS:n kirjanpidon rekisteröintiprosessissa on vähintään yksi vaihe. Kukin vaihe koskee tiettyjen transaktioiden tai -tapahtumien kirjanpidon rekisteröintiä yhdessä kirjanpidon laitteessa tai palvelussa. Seuraavan ratkaisun osat koskevat kirjanpidon rekisteröintiä laiteasemaan yhdistetyssä kirjanpidon laitteessa:

- **Commerce runtime (CRT) -laajennus** – Tämä osa sarjoittaa transaktion tai tapahtuman tiedot siinä muodossa, jota käytetään myös tiedonsiirtoon kirjanpidon laitteen kanssa, jäsentää vastaukset kirjanpidon laitteesta ja tallentaa vastaukset kanavatietokantaan. Lisäksi laajennus määrittää, mitkä transaktiot ja tapahtumat on rekisteröitävä. Tätä osa kutsutaan usein *kirjanpitoasiakirjan toimittajaksi*.
- **Hardware station -laajennus** – Tämä osa käynnistää tiedonsiirron kirjanpidon laitteen kanssa, lähettää pyynnöt ja suorat komennot kirjanpidon laitteeseen kirjanpitoasiakirjasta haettujen transaktion tai tapahtuman tietojen perusteella sekä vastaanottaa vastaukset kirjanpidon laitteesta. Tätä osa kutsutaan usein *kirjanpidon yhdistimeksi*.

Kirjanpidon laitteen kirjanpidon integrointimalli sisältää kirjanpitoasiakirjan toimittajan ja kirjanpidon yhdistimen CRT- ja Hardware station -laajennukset. Lisäksi se sisältää seuraavien osien määritykset:

- **Kirjanpitoasiakirjan toimittajan määritys** – Tämä määritys määrittää kirjanpitoasiakirjojen tulostusmenetelmän ja -muodon. Lisäksi se sisältää verojen ja maksutapojen tietojen yhdistämisen, jotta Retail POS:n tiedot ovat yhteensopivia kirjanpidon laitteen laiteohjelmassa valmiiksi määritettyjen arvojen kanssa.
- **Kirjanpidon yhdistimen määritys** – Tämä määritys määrittää tietyn kirjanpidon laitteen fyysisen tiedonsiirron.

Tietyn kassakoneen kirjanpidon rekisteröintiprosessi määritetään myyntipisteen toimintaprofiilin vastaavalla asetuksella. Lisätietoja kirjanpidon rekisteröintiprosessin määrittämisestä, kirjanpitoasiakirjan toimittajan ja kirjanpidon yhdistimen määritysten lataamisesta sekä niiden parametrien muuttamisesta on kohdassa [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Seuraavassa esimerkissä on tyypillinen kirjanpidon laitteen kirjanpidon rekisteröinnin työnkulku. Työnkulku alkaa myyntipisteen tapahtumalla (kuten myyntitapahtuman päättämisellä), ja siinä toteutetaan seuraavat vaiheet mainitussa järjestyksessä:

1. Myyntipiste pyytää kirjanpitoasiakirjan CRT:stä.
1. CRT selvittää, edellyttääkö nykyinen tapahtuma kirjanpidon rekisteröintiä.
1. CRT tunnistaa kirjanpidon rekisteröintiprosessin asetusten perusteella kirjanpidon rekisteröinnissä käytettävän kirjanpidon yhdistimen ja vastaavan kirjanpitoasiakirjan toimittajan.
1. CRT suorittaa kirjanpitoasiakirjan toimittajan, joka luo transaktiota tai tapahtuvaa edustavan kirjanpitoasiakirjan (kuten XML-asiakirjan).
1. Myyntipiste lähettää CRT:n valmisteleman kirjanpitoasiakirjan Hardware station -laajennukseen.
1. Hardware station suorittaa kirjanpidon yhdistimen, joka käsittelee kirjanpitoasiakirjan ja välittää sen kirjanpidon laitteeseen tai palveluun.
1. Myyntipiste analysoi kirjanpidon laitteen ja palvelun vastauksen ja määrittää sen perusteella, onnistuiko kirjanpidon rekisteröinti.
1. CRT tallentaa vastauksen kanavatietokantaan.

![Ratkaisumalli.](media/emea-fiscal-integration-solution.png "Ratkaisumalli")

## <a name="error-handling"></a>Virheen käsittely

Kirjanpidon integrointikehikossa on seuraavat asetukset, joilla voi käsitellä kirjanpidon rekisteröinnin aikana tapahtuvia virheitä:

- **Yritä uudelleen** – Käyttäjät voivat käyttää tätä asetusta, kun virhe voidaan ratkaista nopeasti ja kirjanpidon rekisteröinti voidaan suorittaa uudelleen. Tätä asetusta voi käyttää esimerkiksi silloin, kun kirjanpidon laitetta ei ole liitetty, kuittitulostimessa ei ole paperia tai kuittitulostimessa on paperitukos.
- **Peruuta** – Käyttäjät voivat siirtää tällä asetuksella nykyisen transaktion tai tapahtuman kirjanpidon rekisteröinnin myöhemmäksi, jos se epäonnistuu. Kun rekisteröintiä on siirretty myöhemmäksi, käyttäjä voi jatkaa työskentelyä myyntipisteessä ja suorittaa loppuun toiminnot, joissa kirjanpidon rekisteröintiä ei tarvita. Kun myyntipisteessä tapahtuu kirjanpidon rekisteröintiä edellyttävä tapahtuma (avataan esimerkiksi uusi tapahtuma), virheen käsittelyn valintaikkuna avautuu automaattisesti ilmoittamaan, että edellistä tapahtumaan eri rekisteröity oikein. Valintaikkunassa on myös vaihtoehtoja virheen käsittelemiseen.
- **Ohita** – Käyttäjä voi käyttää tätä asetusta, kun kirjanpidon rekisteröinti voidaan jättää tekemättä tietyissä tilanteissa ja tavallisia toimintoja voidaan jatkaa myyntipisteessä. Tätä asetusta voidaan käyttää esimerkiksi silloin, kun se myyntitapahtuma, jonka kirjanpidon rekisteröinti epäonnistui, voidaan rekisteröidä erityiseen painettuun kirjauskansioon.
- **Merkitse rekisteröidyksi** – käyttäjät voivat käyttää tätä asetusta, kun tapahtuma kyllä rekisteröitiin kirjanpidon laitteeseen (esimerkiksi verokuitti tulostettiin), mutta virhe tapahtui, kun kirjanpidon vastausta tallennettiin kanavatietokantaan.

> [!NOTE]
> **Ohita**- ja **Merkitse rekisteröidyksi** -asetukset on aktivoitava kirjanpidon rekisteröintiprosessissa ennen käyttöä. Käyttäjille on myös myönnettävä vastaavat käyttöoikeudet.

**Ohita**- ja **Merkitse rekisteröidyksi** -asetuksella otetaan käyttöön tietokoodit taltioimaan tiettyjä virhettä koskevia tietoja, kuten virheen syy tai oikeutus kirjanpidon rekisteröinnin ohittamiselle tai tapahtuman merkitsemiselle rekisteröidyksi. Lisätietoja virheen käsittelyparametrien määrittämisestä on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valinnainen kirjanpidon rekisteröinti

Kirjanpidon rekisteröinti voi olla pakollisista joillekin toiminnoille mutta valinnaista toisille. Tavallisen myynnin ja palautusten kirjanpidon rekisteröinti voi olla pakollista, kun taas asiakkaan talletuksiin liittyvien toimintojen kirjanpidon rekisteröinti voi olla valinnaista. Tässä tapauksessa myynnin kirjanpidon rekisteröinnin tekemättä jättäminen estää lisämyynnin, kun taas asiakkaan tallennuksen kirjanpidon rekisteröinnin tekemättä jättäminen ei estä lisämyyntiä. Pakollisten ja valinnaisten toimintojen erottamiseksi suositellaan, että ne käsitellään eri asiakirjatoimittajissa ja että kyseisille toimittajille määritetään erilliset kirjanpidon rekisteröintiprosessin vaiheet. **Jatka virheen ilmetessä** -parametri on otettava käyttöön kaikissa valinnaiseen kirjanpidon rekisteröintiin liittyvissä vaiheissa. Lisätietoja virheen käsittelyparametrien määrittämisestä on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Kirjanpidon rekisteröinnin suorittaminen manuaalisesti

Jos transaktion tai tapahtuman kirjanpidon rekisteröinti on lykätty virheen jälkeen (esimerkiksi silloin, kun toimittaja on valinnut **Peruuta** virheen käsittely valintaruudussa), voit suorittaa kirjanpidon rekisteröinnin manuaalisesti käynnistämällä vastaavan toiminnon. Lisätietoja on kohdassa [Lykätyn kirjanpidon rekisteröinnin manuaalisen suorittamisen ottaminen käyttöön](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Kirjanpidon rekisteröinnin kuntotarkastus

Kirjanpidon rekisteröintien kuntotarkastusmenettely tarkistaa, että kirjanpidon laite tai palvelu on käytettävissä tietyn tapahtuman tapahtuessa. Jos kirjanpidon rekisteröintiä ei suorittaa tällä hetkellä loppuun, käyttäjälle ilmoitetaan siitä etukäteen.

Myyntipiste suorittaa kuntotarkastuksen seuraavien tapahtumien yhteydessä:

- Uusi tapahtuma avataan.
- Keskeytettyä tapahtumaa jatketaan.
- Myynti- tai palautustapahtuma viimeistellään.

Jos kuntotarkastus epäonnistuu, kuntotarkastuksen valintaikkuna avautuu myyntipisteeseen. Valintaikkunassa on seuraavat painikkeet:

- **OK** – Toimittaja voi ohittaa tällä painikkeella kuntotarkastuksen virheen ja jatkaa toiminnon käsittelyä. Käyttäjät voivat valita tämän painikkeen vain, jos **Salli kuntotarkistuksen virheen ohitus** -käyttöoikeus on otettu heille käyttöön.
- **Peruuta** – Jos käyttäjä valitsee tämän painikkeen, myyntipiste peruuttaa viimeisimmän toiminnon. (Nimikettä ei esimerkiksi lisätä uuteen toimintoon.)

> [!NOTE]
> Kuntotarkastus suorittaan vain, jos nykyinen toiminto edellyttää kirjanpidon rekisteröintiä ja jos **Jatka virheen ilmetessä** -parametri on poistettu kirjanpidon rekisteröintiprosessin nykyisessä vaiheessa käytöstä. Lisätietoja on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Kirjanpidon vastauksen tallentaminen kirjanpitotapahtumassa

Kun transaktion tai tapahtuman kirjanpidon rekisteröinti onnistuu, kirjanpitotapahtuma luodaan kanavatietokannassa ja linkitetään alkuperäiseen transaktioon tai tapahtumaan. Vastaavasti jos epäonnistuneelle kirjanpidon rekisteröinnille valitaan **Ohita**- tai **Merkitse rekisteröidyksi** -asetus, tämä tieto tallennetaan kirjanpitotapahtumaan. Kirjanpitotapahtuma säilyttää kirjanpidon laitteen tai palvelun kirjanpidon vastauksen. Jos kirjanpidon rekisteröintiprosessissa on useita vaiheita, kirjanpitotapahtuma luodaan jokaiselle prosessin vaiheelle, jonka seurauksena oli onnistunut tai epäonnistunut rekisteröinti.

*P-työ* siirtää kirjanpitotapahtumat Headquartersiin yhdessä vähittäismyyntitapahtumien kanssa. Voit tarkastella **Myymälän tapahtumat** -sivun **Tilikauden tapahtumat** -pikavälilehdellä tapahtumiin linkitettyjä kirjanpitotapahtumia.

Kirjanpitotapahtumaan tallennetaan seuraavat tiedot:

- Kirjanpidon rekisteröintiprosessin tiedot (kuten prosessi, yhdistinryhmä ja yhdistin). Siihen tallennetaan myös **Kassakoneen numero** -kentässä oleva kirjanpidon laitteen sarjanumero, jos tämä tieto sisältyy kirjanpidon vastaukseen.
- Kirjanpidon rekisteröinnin tila: **Valmis**, jos rekisteröinti onnistui, **Ohitettu**, jos käyttäjä valitsi epäonnistuneessa rekisteröinnissä **Ohita**-asetuksen, tai **Merkitty rekisteröidyksi**, jos käyttäjä valitse **Merkitse rekisteröidyksi** -asetuksen.
- Valittuun kirjanpitotapahtumaan liittyvät tietokooditapahtumat. Voit tarkastella tietokooditapahtumia valitsemalla **Tilikauden tapahtumat** -pikavälilehdessä ensin kirjanpitotapahtuman, jonka tila on **Ohitettu** tai **Merkitty rekisteröidyksi**, ja sitten **Tietokooditapahtumat**.

Valitsemalla **Laajennetut tiedot** voidaan tarkastella joitakin kirjanpitotapahtuman ominaisuuksia. Tarkasteltava ominaisuusluettelo koskee kirjanpitotapahtuman luoneen kirjanpidon rekisteröintitoimintoja. Esimerkiksi Ranskan digitaalisen allekirjoitustoiminnon digitaalista allekirjoitusta, järjestysnumeroa, varmenteen pikkukuvaa, hajautusalgoritmin tunnusta ja muita kirjanpitotapahtuman ominaisuuksia voidaan tarkastella.

## <a name="fiscal-texts-for-discounts"></a>Alennusten kirjanpitotekstit

Joissakin maissa tai joillakin alueilla on verokuitteihin tulostettavia lisätekstejä koskevia erityisvaatimuksia, kuten käytössä on erilaisia alennuksia. Kirjanpidon integrointitoiminnolla voi määrittää alennusta koskevan erityistekstin, joka tulostetaan verokuitin alennusrivin jälkeen. Jos kyse on manuaalisesti tehtävistä alennuksista, voit määrittää tietokoodin kirjanpitotekstin myyntipisteen toimintaprofiilissa **Tuotealennus**-tietokoodina. Lisätietoja alennusten kirjanpitotekstin määrittämisestä on kohdassa [Alennusten kirjanpitotekstien määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Kuitti X- ja kuitti Z -raporttien tulostaminen

Kirjanpidon integrointitoiminto tukee tiettyä integroidun kirjanpidon laitetta tai palvelua koskevan päivän lopun laskelmien luontia:

- Uudet painikkeet, joilla kyseiset toiminnot suoritetaan, on lisättävä myyntipisteen näyttöasetteluun. Lisätietoja on kohdassa [Kirjanpidon X/Z-raporttien määrittäminen myyntipisteessä](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Kirjanpidon integrointimallissa nämä toiminnot on täsmäytettävä kirjanpidon laitteen vastaaviin toimintoihin.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Commerce SDK:n kirjanpidon integrointimallit

Seuraavat kirjanpidon integrointimallit ovat käytettävissä Commerce SDK:ssa:

- [Näyte verotusta varten olevan tulostimen integroinnista Italiassa](./emea-ita-fpi-sample.md)
- [Näyte verotusta varten olevan tulostimen integroinnista Puolassa](./emea-pol-fpi-sample.md)
- [Itävallan tilikausirekisteröintipalvelun integroinnin malli](./emea-aut-fi-sample.md)
- [Tšekin tasavallan tilikausirekisteröintipalvelun integroinnin malli](./emea-cze-fi-sample.md)
- [Tarkistusyksikön integrointimalli – Ruotsi](./emea-swe-fi-sample.md)
- [Saksan tilikausirekisteröintipalvelun integroinnin malli](./emea-deu-fi-sample.md)

Seuraava kirjanpidon integrointitoiminto otetaan käyttöön myös käyttämällä kirjanpidon integrointikehystä, mutta se on saatavana käyttövalmiina eikä se sisälly Commerce SDK:hon:

- [Brasilian tilikausirekisteröinti](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitaalinen allekirjoitus Ranskassa](./emea-fra-cash-registers.md)

Myös seuraava kirjanpidon integrointitoiminto on käytettävissä Commerce SDK:ssa, mutta se ei tällä hetkellä käytä kirjanpidon integrointikehikkoa. Tämä toiminto on tarkoitus siirtää kirjanpidon integrointikehikkoon myöhemmissä päivityksissä.

- [Digitaalinen allekirjoitus Norjassa](./emea-nor-cash-registers.md)

Seuraava vanha kirjanpidon integrointitoiminto, joka on käytettävissä Commerce SDK:ssa, ei käytä kirjanpidon integrointikehystä, ja se poistetaan käytöstä myöhemmissä päivityksissä:

- [Tarkistusyksikön integrointimalli – Ruotsi (vanha)](./retail-sdk-control-unit-sample.md)
- [Digitaalinen allekirjoitus Ranskassa (vanha)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
