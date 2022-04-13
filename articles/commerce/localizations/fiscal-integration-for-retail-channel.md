---
title: Commerce-kanavien kirjanpidon integroinnin yleiskatsaus
description: Tämä ohjeaihe on yleiskatsaus Dynamics 365 Commercen kirjanpidon integrointitoiminnoista.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 00c68155088ff2aabbe2fe0c4f431b665aebcd0a
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462520"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Commerce-kanavien kirjanpidon integroinnin yleiskatsaus

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe on yleiskatsaus Dynamics 365 Commercen kirjanpidon integrointitoiminnoista. 

Kirjanpidon integrointi sisältää sellaisten erilaisten kirjanpidon laitteiden ja palvelujen integroinnin, joilla kirjanpidon rekisteröinti voidaan ottaa myynnissä käyttöön paikallisten, vähittäismyyntialan veropetoksia estävän kirjanpitolainsäädännön mukaisesti. Kirjanpidon integraatiota voidaan esimerkiksi seuraavissa tyypillisissä skenaarioissa:

- Myynnin rekisteröinti kirjanpidon laitteessa, joka on liitetty myyntipisteeseen (POS), kuten kuittitulostimeen, ja verokuitin tulostaminen asiakkaalle.
- Retail POS:ssä suoritettuun myyntiin ja palautuksiin liittyvien tietojen lähettäminen turvallisesti ulkoiseen, veroviranomaisen ylläpitämään verkkopalveluun.
- Myynnin tapahtumatietojen muuttamattomuuden varmistaminen digitaalisella allekirjoituksella.

Kirjanpidon integrointitoiminto on kehikko, joka muodostaa yhteisen ratkaisun Retail POS:n sekä kirjanpidoin laitteiden ja palvelujen kehittämiselle ja mukauttamiselle edelleen. Toiminto sisältää myös kirjanpidon integrointimalleja, jotka tukevat tiettyjen maiden tai alueiden perusskenaariota ja joita voi käyttää tiettyjen kirjanpidon laitteiden tai palvelujen kanssa. Kirjanpidon integrointimalli koostuu useista Commerce-osien laajennuksista, ja se sisältyy SDK:hon. Lisätietoja kirjanpidon integroinnin esimerkeistä on kohdassa [Kirjanpidon integroinnin esimerkit – Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Lisätietoja Commerce SDK:n asentamisesta ja käytöstä on kohdassa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Jos haluat tukea skenaarioita, joita kirjanpidon integrointimalli ei tue, integroida Retail POS:n muiden kirjanpidon laitteiden ja palvelujen kanssa tai ottaa huomioon muiden maiden tai alueiden vaatimukset, sinun on joko laajennettava nykyistä kirjanpidon integrointimallia tai luotava uusi malli käyttämällä nykyistä mallia esimerkkinä.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden ja palveluiden kirjanpidon integrointimallit

Retail POS:n kirjanpidon rekisteröintiprosessissa on vähintään yksi vaihe. Kukin vaihe koskee tiettyjen transaktioiden tai -tapahtumien kirjanpidon rekisteröintiä yhdessä kirjanpidon laitteessa tai palvelussa. Seuraavan ratkaisun osat koskevat kirjanpidon rekisteröintiä kirjanpidon laitteessa tai palvelussa:

- **Veroasiakirjan toimittaja** – Tämä osa sarjoittaa transaktion tai tapahtuman tiedot siinä muodossa, jota käytetään myös tiedonsiirtoon kirjanpidon laitteen tai palvelun kanssa, jäsentää vastaukset kirjanpidon laitteesta tai palvelusta ja tallentaa vastaukset kanavatietokantaan. Lisäksi laajennus määrittää, mitkä transaktiot ja tapahtumat on rekisteröitävä.
- **Veroyhdistin** – Tämä osa käynnistää tiedonsiirron kirjanpidon laitteen tai palvelun kanssa, lähettää pyynnöt ja suorat komennot kirjanpidon laitteeseen tai palveluun kirjanpitoasiakirjasta haettujen transaktion tai tapahtuman tietojen perusteella sekä vastaanottaa vastaukset kirjanpidon laitteesta tai palvelusta.

Kirjanpidon integrointimalli saattaa sisältää kirjanpitoasiakirjan toimittajan ja Commerce runtime CRT-, Hardware station ja myyntipistelaajennukset. Lisäksi se sisältää seuraavien osien määritykset:

- **Kirjanpitoasiakirjan toimittajan määritys** – Tämä määritys määrittää kirjanpitoasiakirjojen tulostusmenetelmän ja -muodon. Lisäksi se sisältää verojen ja maksutapojen tietojen yhdistämisen, jotta Retail POS:n tiedot ovat yhteensopivia kirjanpidon laitteen tai palvelun laiteohjelmassa valmiiksi määritettyjen arvojen kanssa.
- **Kirjanpidon yhdistimen määritys** – Tämä määritys määrittää tietyn kirjanpidon laitteen tai palvelun fyysisen tiedonsiirron.

Tietyn kassakoneen kirjanpidon rekisteröintiprosessi määritetään myyntipisteen toimintaprofiilin vastaavalla asetuksella. Lisätietoja kirjanpidon rekisteröintiprosessin määrittämisestä, kirjanpitoasiakirjan toimittajan ja kirjanpidon yhdistimen määritysten lataamisesta sekä niiden määritysparametrien muuttamisesta on kohdassa [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Voit valita kassakoneita, joissa on verorekisteröinnin rajoituksia, kun sinun on toimitettava vain muita kuin verotoimintoja, kuten tuoteluettelohaku, asiakashaku tai tapahtumien luonnoksen luominen näillä laitteilla. Lisätietoja: [Kassakoneiden määrittäminen kirjanpidon rekisteröintirajoitusten mukaan](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions)

Seuraavassa tyypillisessä verorekisteröintityönkulussa alkaa myyntipisteen tapahtumalla (esimerkiksi myyntitapahtuman viimeisteleminen) ja otetaan käyttöön ennalta määritetty vaihesarja, joka sisältää muita Commerce-komponentteja (kuten CRT ja Hardware station).

1. Myyntipiste pyytää veroasiakirjaa fiscal integration framework (FIF) -kehyksestä.
1. FIF selvittää, edellyttääkö nykyinen tapahtuma kirjanpidon rekisteröintiä.
1. FIF tunnistaa kirjanpidon rekisteröintiprosessin asetusten perusteella kirjanpidon rekisteröinnissä käytettävän kirjanpidon yhdistimen ja vastaavan kirjanpitoasiakirjan toimittajan.
1. FIF suorittaa kirjanpitoasiakirjan toimittajan, joka luo transaktiota tai tapahtumaa edustavan kirjanpitoasiakirjan (kuten XML-asiakirjan).
1. FIF palauttaa luodun veroasiakirjan myyntipisteeseen.
1. Myyntipiste pyytää, että FIF lähettää veroasiakirjan verolaitteeseen tai -palveluun.
1. FIF station suorittaa kirjanpidon yhdistimen, joka käsittelee kirjanpitoasiakirjan ja lähettää sen kirjanpidon laitteeseen tai palveluun.
1. FIF palauttaa verovastauksen (verolaitteen tai -palvelun vastauksen) myyntipisteeseen.
1. Myyntipiste analysoi kirjanpidon vastauksen ja määrittää sen perusteella, onnistuiko kirjanpidon rekisteröinti. Tarvittaessa myyntipiste pyytää FIF:iä käsittelemään kaikki tapahtuneet virheet. 
1. Myyntipiste pyytää FIF:iä käsittelemään ja tallentamaan verovastauksen.
1. Veroasiakirjan toimittaja käsittelee verovastauksen. Veroasiakirjan tarjoaja jäsentää vastauksen ja poimii siitä laajennetut tiedot osana tätä käsittelyä.
1. FIF tallentaa vastauksen ja laajennetut tiedot kanavatietokantaan.
1. Tarvittaessa myyntipiste tulostaa kuitin tavallisen kuittitulostimen kautta, joka on liitetty Hardware stationiin. Kuitti voi sisältää verovastausta koskevat pakolliset tiedot.
 
Seuraavissa esimerkeissä on tyypillisiä kirjanpidon laitteiden tai palveluiden kirjanpidon rekisteröinnin työnkulkuja.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Verorekisteröinti tehdään Hardware stationiin liitetyllä laitteella.

Tätä konfiguraatiota käytetään, kun fyysinen verolaite, kuten verotulostin, on liitetty Hardware stationiin. Sitä voidaan käyttää myös silloin, kun tietoliikenne verolaitteen tai -palvelun kanssa tapahtuu Hardware stationiin asennetulla ohjelmistolla. Tässä tapauksessa veroasiakirjan tarjoaja sijaitsee CRT:ssä ja veroliitin sijaitsee Hardware stationissa.

![Verorekisteröinti tehdään Hardware stationiin liitetyllä laitteella.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Verorekisteröinti tehdään ulkoisen palvelun kautta.

Tätä konfiguraatiota käytetään, kun verorekisteröinti tehdään ulkoisella palvelulla, kuten verkkopalvelulla, joka on veroviranomaisen ylläpitämä. Tässä tapauksessa sekä veroasiakirjan tarjoaja että veroyhdistin sijaitsevat CRT:ssä.

![Verorekisteröinti ulkoisen palvelun kautta.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Verorekisteröinti tehdään sisäisesti CRT:ssä

Tätä konfiguraatiota käytetään, kun verorekisteröintiin ei tarvita ulkoista verolaitetta tai -palvelua. Sitä käytetään esimerkiksi verorekisteröinnin yhteydessä, kun allekirjoitetaan myyntitapahtumat digitaalisesti. Tässä tapauksessa sekä veroasiakirjan tarjoaja että veroyhdistin sijaitsevat CRT:ssä.

![Verorekisteröinti tehdään sisäisesti CRT:ssä.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Verorekisteröinti tehdään paikallisen verkon laitteen tai palvelun avulla.

Tätä konfiguraatiota käytetään, kun myymälän paikalliseen verkkoon kuuluu fyysinen verolaite tai veropalvelu, ja siinä on HTTPS-sovellusohjelmaliittymä. Tässä tapauksessa veroasiakirjan tarjoaja sijaitsee CRT:ssä ja veroliitin sijaitsee myyntipisteessä.

![Verorekisteröinti tehdään paikallisen verkon laitteen tai palvelun avulla.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Virheen käsittely

Kirjanpidon integrointikehikossa on seuraavat asetukset, joilla voi käsitellä kirjanpidon rekisteröinnin aikana tapahtuvia virheitä:

- **Yritä uudelleen** – Käyttäjät voivat käyttää tätä asetusta, kun virhe voidaan ratkaista nopeasti ja kirjanpidon rekisteröinti voidaan suorittaa uudelleen. Tätä asetusta voi käyttää esimerkiksi silloin, kun kirjanpidon laitetta ei ole liitetty, kuittitulostimessa ei ole paperia tai kuittitulostimessa on paperitukos.
- **Peruuta** – Käyttäjät voivat siirtää tällä asetuksella nykyisen transaktion tai tapahtuman kirjanpidon rekisteröinnin myöhemmäksi, jos se epäonnistuu. Kun rekisteröintiä on siirretty myöhemmäksi, käyttäjä voi jatkaa työskentelyä myyntipisteessä ja suorittaa loppuun toiminnot, joissa kirjanpidon rekisteröintiä ei tarvita. Kun myyntipisteessä tapahtuu kirjanpidon rekisteröintiä edellyttävä tapahtuma (avataan esimerkiksi uusi tapahtuma), virheen käsittelyn valintaikkuna avautuu automaattisesti ilmoittamaan, että edellistä tapahtumaan eri rekisteröity oikein. Valintaikkunassa on myös vaihtoehtoja virheen käsittelemiseen.
- **Ohita** – Käyttäjä voi käyttää tätä asetusta, kun kirjanpidon rekisteröinti voidaan jättää tekemättä tietyissä tilanteissa ja tavallisia toimintoja voidaan jatkaa myyntipisteessä. Tätä asetusta voidaan käyttää esimerkiksi silloin, kun se myyntitapahtuma, jonka kirjanpidon rekisteröinti epäonnistui, voidaan rekisteröidä erityiseen painettuun kirjauskansioon.
- **Merkitse rekisteröidyksi** – käyttäjät voivat käyttää tätä asetusta, kun tapahtuma kyllä rekisteröitiin kirjanpidon laitteeseen (esimerkiksi verokuitti tulostettiin), mutta virhe tapahtui, kun kirjanpidon vastausta tallennettiin kanavatietokantaan.
- **Viivytä** – Operaattorit voivat käyttää tätä vaihtoehtoa, kun tapahtumaa ei rekisteröidä, koska rekisteröintipalvelu ei ole ollut käytettävissä. 

> [!NOTE]
> **Ohita**-, **Merkitse rekisteröidyksi**- ja **Viivytä**-asetukset on aktivoitava kirjanpidon rekisteröintiprosessissa ennen käyttöä. Käyttäjille on myös myönnettävä vastaavat käyttöoikeudet.

**Ohita**-, **Merkitse rekisteröidyksi**- ja **Viivytä**-asetuksella otetaan käyttöön tietokoodit taltioimaan tiettyjä virhettä koskevia tietoja, kuten virheen syy tai oikeutus kirjanpidon rekisteröinnin ohittamiselle tai tapahtuman merkitsemiselle rekisteröidyksi. Lisätietoja virheen käsittelyparametrien määrittämisestä on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valinnainen kirjanpidon rekisteröinti

Kirjanpidon rekisteröinti voi olla pakollisista joillekin toiminnoille mutta valinnaista toisille. Tavallisen myynnin ja palautusten kirjanpidon rekisteröinti voi olla pakollista, kun taas asiakkaan talletuksiin liittyvien toimintojen kirjanpidon rekisteröinti voi olla valinnaista. Tässä tapauksessa myynnin kirjanpidon rekisteröinnin tekemättä jättäminen estää lisämyynnin, kun taas asiakkaan tallennuksen kirjanpidon rekisteröinnin tekemättä jättäminen ei estä lisämyyntiä. Pakollisten ja valinnaisten toimintojen erottamiseksi suositellaan, että ne käsitellään eri asiakirjatoimittajissa ja että kyseisille toimittajille määritetään erilliset kirjanpidon rekisteröintiprosessin vaiheet. **Jatka virheen ilmetessä** -parametri on otettava käyttöön kaikissa valinnaiseen kirjanpidon rekisteröintiin liittyvissä vaiheissa. Lisätietoja virheen käsittelyparametrien määrittämisestä on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Kirjanpidon rekisteröinnin suorittaminen uudelleen

Jos transaktion tai tapahtuman kirjanpidon rekisteröinti on lykätty virheen jälkeen (esimerkiksi silloin, kun toimittaja on valinnut **Peruuta** virheen käsittely valintaruudussa), voit suorittaa kirjanpidon rekisteröinnin manuaalisesti käynnistämällä vastaavan toiminnon. Lisätietoja on kohdassa [Lykätyn kirjanpidon rekisteröinnin manuaalisen suorittamisen ottaminen käyttöön](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Viivytä-vaihtoehto

**Viivytä**-vaihtoehdolla voit jatkaa verorekisteröintiprosessia, jos nykyinen vaihe epäonnistuu. Sitä voidaan käyttää, kun verorekisteröinnin varmistusvaihtoehto on käytössä.

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
> Kuntotarkastus suoritetaan vain, jos nykyinen toiminto edellyttää kirjanpidon rekisteröintiä ja jos **Jatka virheen ilmetessä** -parametri on poistettu kirjanpidon rekisteröintiprosessin nykyisessä vaiheessa käytöstä. Lisätietoja on kohdassa [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Kirjanpidon vastauksen tallentaminen kirjanpitotapahtumassa

Kun transaktion tai tapahtuman kirjanpidon rekisteröinti onnistuu, kirjanpitotapahtuma luodaan kanavatietokannassa ja linkitetään alkuperäiseen transaktioon tai tapahtumaan. Vastaavasti jos epäonnistuneelle kirjanpidon rekisteröinnille valitaan **Ohita**- tai **Merkitse rekisteröidyksi** -asetus, tämä tieto tallennetaan kirjanpitotapahtumaan. Kirjanpitotapahtuma säilyttää kirjanpidon laitteen tai palvelun kirjanpidon vastauksen. Jos kirjanpidon rekisteröintiprosessissa on useita vaiheita, kirjanpitotapahtuma luodaan jokaiselle prosessin vaiheelle, jonka seurauksena oli onnistunut tai epäonnistunut rekisteröinti.

*P-työ* siirtää kirjanpitotapahtumat Headquartersiin yhdessä vähittäismyyntitapahtumien kanssa. Voit tarkastella **Myymälän tapahtumat** -sivun **Tilikauden tapahtumat** -pikavälilehdellä tapahtumiin linkitettyjä kirjanpitotapahtumia.

Kirjanpitotapahtumaan tallennetaan seuraavat tiedot:

- Kirjanpidon rekisteröintiprosessin tiedot (kuten prosessi, yhdistinryhmä ja yhdistin). Siihen tallennetaan myös **Kassakoneen numero** -kentässä oleva kirjanpidon laitteen sarjanumero, jos tämä tieto sisältyy kirjanpidon vastaukseen.
- Kirjanpidon rekisteröinnin tila: **Valmis**, jos rekisteröinti onnistui, **Ohitettu**, jos käyttäjä valitsi epäonnistuneessa rekisteröinnissä **Ohita**-asetuksen, tai **Merkitty rekisteröidyksi**, jos käyttäjä valitse **Merkitse rekisteröidyksi** -asetuksen, tai **Viivytetty**, jos operaattori valitsi **Viivytä**-vaihtoehdon.
- Valittuun kirjanpitotapahtumaan liittyvät tietokooditapahtumat. Voit tarkastella tietokooditapahtumia valitsemalla **Verotapahtumat** -pikavälilehdessä ensin kirjanpitotapahtuman, jonka tila on **Ohitettu**, **Merkitty rekisteröidyksi** tai **Viivytetty**, ja sitten **Tietokooditapahtumat**.

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
- [Näyte kuittitulostimen integroinnista Venäjällä](./rus-fpi-sample.md)

Seuraava kirjanpidon integrointitoiminto otetaan käyttöön myös käyttämällä kirjanpidon integrointikehystä, mutta se on saatavana käyttövalmiina eikä se sisälly Commerce SDK:hon:

- [Brasilian tilikausirekisteröinti](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitaalinen allekirjoitus Ranskassa](./emea-fra-cash-registers.md)

Myös seuraava kirjanpidon integrointitoiminto on käytettävissä Commerce SDK:ssa, mutta se ei tällä hetkellä käytä kirjanpidon integrointikehikkoa. Tämä toiminto on tarkoitus siirtää kirjanpidon integrointikehikkoon myöhemmissä päivityksissä.

- [Digitaalinen allekirjoitus Norjassa](./emea-nor-cash-registers.md)

Seuraava vanha kirjanpidon integrointitoiminto, joka on käytettävissä Commerce SDK:ssa, ei käytä kirjanpidon integrointikehystä, ja se poistetaan käytöstä myöhemmissä päivityksissä:

- [Tarkistusyksikön integrointimalli – Ruotsi (vanha)](./retail-sdk-control-unit-sample.md)
- [Digitaalinen allekirjoitus Ranskassa (vanha)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
