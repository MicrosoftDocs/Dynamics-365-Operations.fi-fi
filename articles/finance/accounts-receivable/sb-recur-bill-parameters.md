---
title: Toistuvan sopimuksen laskutusparametrit
description: Tässä aiheessa kerrotaan, miten määritetään toistuvassa sopimuslaskutuksessa luotujen laskutusaikataulujen oletusarvot. Siinä kerrotaan myös, miten laskutusaikatauluryhmiä luodaan.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4c52095aa49962cbfc577faf71ab0d71929a386b
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629408"
---
# <a name="recurring-contract-billing-parameters"></a>Toistuvan sopimuksen laskutusparametrit

**Toistuvan sopimuksen laskutusparametrit** -sivulla voit määrittää toistuvassa sopimuslaskutuksessa luotujen laskutusaikataulujen oletusarvot. Kaikki luomasi laskutusaikataulut käyttävät aluksi näitä oletusarvoja. Voit kuitenkin muuttaa kunkin laskutusaikataulun arvoja tarpeen mukaan.

## <a name="general-tab"></a>Yleinen-välilehti

1. Valitse **Toistuvat sopimuksen laskutusparametrit** -sivun **Yleiset**-välilehden **Laskutusaikatauluryhmä**-kentästä laskutusaikatauluryhmä. Lisätietoja laskutusaikatauluryhmien määrittämisestä on tässä ohjeaiheessa myöhemmin olevassa [Laskutusaikatauluryhmien määrittäminen](#set-up-billing-schedule-groups) -osassa.
2. Valitse **Irtisanomistyyppi**-kentässä, kuinka lopullinen lasku lasketaan laskutusaikataulun päättämisen yhteydessä:

    - **Aikataulun oikaiseminen** – Voit poistaa laskutusaikataulun käytöstä irtisanomispäivänä, muuttaa aikataulun tilaksi **Edellinen laskutus** ja muuttaa siihen liittyvän lykkäysaikataulun peruuttamalla summan, jota ei enää saa tulouttaa. Jos laskutuksen alkamispäivämäärä on päättymispäivän jälkeen, jäljellä olevat laskutuskaudet poistuvat.
    - **Jäljellä oleva lasku** – Lisää laskutusaikataulun jäljellä olevat summat irtisanomiskauteen ja muuta aikataulun tilaksi **Viimeinen laskutus**, ja päivitä lykkäysaikataulu. Jos laskutuksen alkamispäivämäärä on päättymispäivämäärän jälkeen, kaikkien jäljellä olevien laskutuskausien kokonaissumma lisätään laskutuskauteen ja jäljellä olevat laskutuskaudet poistetaan.
    - **Ei oikaisua** – Voit lopettaa laskutusaikataulun päättymispäivänä. Laskutusaikatauluun ei tehdä muutoksia.

3. Valitse **Yksilöivä aikataulutyyppi** -kentässä **Ei mitään**, jos haluat määrittää, että asiakkaat rajoitetaan vain yhteen laskutusaikatauluun. Valitse **Per asiakas** tai **Per loppukäyttäjä**, jos haluat määrittää, että asiakkaat rajoitetaan yksilölliseen aikatauluun.
4. Jos haluat tasata laskutusaikataulun tietorivit kuukauden lopussa, määritä **Tasaa kuukauteen** -asetuksen arvoksi **Kyllä**, kun laskutusaikataulu luodaan tai päivitetään. Määritä sen arvoksi **Ei**, jos haluat käyttää lisäpäiviä.
5. Määritä **Osittaisten kausien suhteellinen jako** -arvoksi **Kyllä**, jos haluat kohdistaa laskutettavat summat kauden päivien määrän perusteella. Määritä arvoksi **Ei**, jos haluat, että kullakin laskutuskaudella on sama summa päivien määrästä riippumatta.
6. Jos määrität **Osittaisten kausien suhteellinen jako** -arvoksi **Kyllä**, määritä **Suhteellisen jaon menetelmä** -kentän arvoksi **Päivittäin**, jotta summat jaetaan kauden päivien määrän mukaan. Määritä arvoksi **Kuukausittain**, jos summa on sama joka kuukausi.
7. Määritä, ovatko juuri luodut laskutusaikataulut pidossa oletusarvon mukaan.

    > [!NOTE]
    > Jos haluat poistaa laskutusaikataulun pidosta, käyttäjän on kuuluttava käyttäjäryhmään. Valitse **Poista käyttäjäryhmältä pidon ohitus**, jos haluat määrittää käyttäjäryhmän, jossa **Salli pidon poistaminen** -asetus on käytössä.

8. Valitse **Laskutapahtuman tyyppi** -kentässä uusien laskutusaikataulujen laskutapahtumatyypin oletusarvo.
9. Määritä **Tasaa lykkäys laskutukseen** -asetuksen arvoksi **Kyllä**, jos haluat kohdistaa vastaavan lykkäysaikataulun niin, että se käyttää samoja päivämääriä kuin laskutusaikataulu. Määritä sen arvoksi **Ei**, jos haluat käyttää eri päiviä.
10. Jos käytät tuottojen jakotoimintoa, määritä **Luo tuoton jako automaattisesti** -asetuksen arvoksi **Kyllä**, kun nimikkeet lisätään laskutusaikatauluun. **Tuoton jako** -valintaruutu valitaan automaattisesti laskutusaikataulun rivillä, jos nimike on määritetty tuoton jaon nimikkeeksi. Valitse **Ei**-vaihtoehto, jos haluat valita **Tuoton jako** -valintaruudun manuaalisesti.
11. Määritä myyntitilauksen luonnin kentät:

    - Laskut voidaan konsolidoida kauden, asiakkaan tai nimikkeen mukaan. Mikä tahansa **Kyllä**- ja **Ei**-arvojen yhdistelmä voidaan määrittää. Laskut voidaan jakaa myös nimikeryhmän mukaan.
    - Seuraavat kirjausvaihtoehdot ovat saatavilla laskuille:

        - **Luo myyntitilaus** – Luo vain myyntitilaus.
        - **Näytä kirjauslasku** – Laskuta myyntitilaus ja avaa sivu, jolla voit kirjata laskun manuaalisesti.
        - **Luo vapaatekstilasku** – Valitse tämä vaihtoehto, jos käytät vapaatekstilaskuja.
        - **Kirjaa lasku automaattisesti** – Laskuta myyntitilaus ja kirjaa se automaattisesti.

    - Määritä **Lisää laskutuspäivämäärät nimikkeen kuvaukseen** -kohtaan **Kyllä**, kun haluat lisätä kuvauksen, joka sisältää laskutuksen alku- ja loppupäivämäärän.
    - Määritä **Jätä nolla-arvoinen kulutus pois** -asetuksen arvoksi **Kyllä**, jos haluat jättää pois laskutusaikataulun rivit, joissa ei ole kulutusta. Määritä sen arvoksi **Ei**, jos haluat sisällyttää nämä rivit myyntitilaukseen.
    - Määritä **Älä tulosta alinimikkeitä** -asetuksen arvoksi **Kyllä**, jos et halua tulostaa myyntitilaukseen jaetun tuoton alinimikkeitä. Laskussa näkyy vain päänimike. Jos (piilotettujen) alinimikkeiden nettosumma on muu kuin nolla, päärivin nettosumma näyttää yhteenvedon aliriveistä. Määritä myyntilaskussa **Ei**, kun haluat tulostaa kaikki päänimikkeen alapuolella olevat alinimikkeet.

12. Määritä tuen ja uusintojen kentät:

    - Määritä **Ota tuki ja uusiminen automaattisesti käyttöön** -arvoksi **Kyllä**, jos haluat käyttää myyntitilauksen tuen ja uusimisen toimintoa automaattisesti.
    - Valitse **Tuen ja uusimisen taso** -kentässä tuen ja uusimisen oletustaso.
    - Määritä **Tuen ja uusimisen määrä** -kentässä tuen ja uusimisen määrä.
    - Määritä **Tuen ja uusimisen oletusarvoinen alkamispäivä** -kentässä päivämäärä, jota käytetään tuen ja uusimisen oletusalkupäivämääränä:

        - **Tapahtumapäivä** – Käytä tapahtuman päivämäärää aloituspäivämääränä.
        - **Kuluvan kuukauden alku** – Käytä aloituspäivänä kuluvan kuukauden ensimmäistä päivää.
        - **Seuraavan kuukauden alku** – Käytä aloituspäivänä seuraavan kuukauden ensimmäistä päivää. Jos tapahtuman päivämäärä on ensimmäinen päivä, kuluva kuukauden ensimmäistä käytetään.
        - **15:n sääntö** – Jos tapahtuman päivämäärä on ensimmäisen ja viidennentoista päivän välissä, aloituspäivänä käytetään kuluvan kuukauden ensimmäistä. Jos tapahtumapäivämäärä on kuukauden kuudestoista tai myöhempi, aloituspäivämäärä on seuraavan kuukauden ensimmäinen päivä.

    - Määritä **Sisällytä alennus laskentaan** -asetuksen arvoksi **Kyllä**, jos haluat sisällyttää alennussumman tuen tai uusimisen summaan. Määritä sen arvoksi **Ei**, jos haluat jättää alennussumman pois.
    - Valitse **Tukitiheys** - ja **Uusimistiheys**-kentissä tiheys, joita käytetään, kun tuki- ja uusimisnimikkeitä lisätään laskutussuunnitelmaan: **Päivittäin**, **Kuukausittain**, **Neljännesvuosittain**, **Puolivuosittain** tai **Vuosittain**.
    - Määritä **Tasaa nimikeryhmän mukaan** - asetuksen arvoksi **Kyllä**, jos haluat kohdistaa uusien nimikkeiden aloitus- ja päättymispäivät aiemmin luotuihin nimikkeisiin nimikeryhmän perusteella.
    - Määritä **Tasaa seuraavaan laskuttamattomaan kauteen** -asetuksen arvoksi **Kyllä**, jos haluat määrittää uusimisnimikkeen kohdistuspäivämäärän seuraavan laskuttamattoman jakson päivämäärän perusteella uusimisen alkamisen jälkeen.
    - Määritä **Kopioi sarjanumero** -asetuksen arvoksi **Kyllä**, jos haluat kopioida nimikkeen sarjanumeron alkuperäiseltä myyntitilausriviltä vastaavalle laskutusaikataulun riville.

13. Jos käytät laskutusaikataulun eskalointia, valitse kulutushintaindeksin laskennassa käytettävä menetelmä.
14. Määritä **Hinnanmuutosten seuranta** - asetuksen arvoksi **Kyllä**, jos haluat kirjata hintamuutokset laskutusaikataulun riveille. Jos laskutusaikataulun rivi vaihdetaan manuaalisesti vakiosta kiinteäksi ja uusi hinta määritetään, kirjaustietoja seurataan laskutusaikataulun rivillä. Määritä arvoksi **Ei**, jos et halua seurata näitä muutoksia.
15. Määritä, suodatetaanko tietueet oletusarvoisesti aloitus- vai päättymispäivän mukaan **Luo lasku** -sivulla.
16. Jos käytät **Laskuttamaton tuotto** -toimintoa, määritä käytettävät asetukset:

    - Määritä **Kirjaa yleinen kirjauskansio automaattisesti** -asetuksen arvoksi **Kyllä**, jos haluat, että yleinen kirjauskansio luodaan ja kirjataan samanaikaisesti. Määritä arvoksi **Ei**, jos haluat luoda yleisen kirjauskansion ja kirjata sen sitten manuaalisesti.
    - Valitse **Kirjauskansion oletusnimi** -kentässä kirjauskansion oletusnimi, jota käytetään, kun yleinen kirjauskansio luodaan.
    - Valitse **Lyhytaikainen laskuttamaton menetelmä** -kentästä lyhytaikainen laskuttamaton menetelmä, jos sellainen on käytössä. Jos valitset **Ei mitään**, lyhyen aikavälin toimintoa ei käytetä laskuttamattoman tuoton kanssa. Valitse **Juoksevat kaudet** aina käyttämään 12 kuukautta tai **Kiinteä vuosi**, jos haluat käyttää jäljellä olevan tilivuoden.

17. Määritä asetukset, joita käytetään laskutusaikataulun ja sen rivien lopettamisen jälkeen:

    - **Myönnä hyvitys** – Luo hyvityslasku, kun laskutusaikataulu- tai laskutusaikataulurivi on päättynyt.
    - **Luotto-oikaisu** – Luo luotto-oikaisu laskutusaikataulua varten, kun rivi on päättynyt. Luotto-oikaisu näkyy laskutusaikataulun tulevalla laskutuskaudella. Kredit-oikaisu päivittää seuraavan laskutuskauden laskun summaa, kunnes hyvitys on otettu laskutusaikatauluun.
    - **Ei hyvitystä** – Älä luo luotto-oikaisua, kun laskutusaikataulu- tai laskutusaikataulurivi on päättynyt. Tämä vaihtoehto on käytettävissä vain, kun käytät **Ei oikaisua** -vaihtoehtoa laskutusaikataulun päättämiseen.

## <a name="sequence-number-tab"></a>Järjestysnumero-välilehti

Määritä laskutusaikataulun numeroiden oletusarvo **Toistuvan sopimuksen laskutusparametrit** -sivun **Järjestysnumero**-välilehdessä. Oletusarvot määritetään **Numerosarjat**-sivulla (**Organisaation hallinta \> Numerosarjat \> Numerosarjat**).

## <a name="set-up-billing-schedule-groups"></a>Määritä laskutusaikatauluryhmät

**Laskutusaikatauluryhmä**-sivulla voit luoda laskutusaikatauluryhmän toistuvaa sopimuslaskutusta varten. Kun uusi laskutusaikataulu luodaan ja siihen kohdistetaan laskutusaikatauluryhmä, laskutusaikataulun oletusarvoiksi määritetään **Laskutusaikatauluryhmä**-sivulla määritetyt arvot. Voit muuttaa mitä tahansa luotavan laskutusaikataulun oletusarvoja. Voit määrittää useita laskutusaikatauluryhmiä ja määrittää niistä yhden **toistuvan sopimuksen laskutusparametrien** sivulla laskutusaikataulun oletusryhmäksi.

Luo laskutusaikatauluryhmä toistuvan sopimuksen laskutusta varten noudattamalla seuraavia ohjeita.

1. Luo laskutusaikatauluryhmä valitsemalla **Laskutusaikatauluryhmä**-sivulla **Uusi**.
2. Kirjoita **Laskutusaikatauluryhmä**-kenttään yksilöivä tunnus.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Määritä **Laskutustiheys**-kentässä laskutusaikataulun laskutustiheys asiakkaalle: **kerran**, **päivittäin**, **kuukausittain**, **neljännesvuosittain**, **puolivuosittain** tai **vuosittain**.
5. Syötä laskutusväli **Laskutusväli**-kenttään. Voit esimerkiksi määrittää **Laskutustiheys**-kentän arvoksi **Kuukausittain** ja **Laskutusväli**-kentän arvoksi **2**, jos haluat laskuttaa joka toinen kuukausi.
6. Valitse laskutusaikataulun nimikkeiden **Hinnoittelutapa**-kentässä nimikkeiden oletushinnoittelutapa.

    - **Vakio** – Laske yksikköhinta syötetyn kokonaismäärän perusteella ja käytä Tuotetietojen hallinnan **Vapautetut tuotteet** -sivun vakiohinnoittelua.
    - **Kiinteä** – Käytä laskutusaikataulun riville syötettyä kiinteää hintaa.
    - **Taso** – Laske yksikköhinta käyttämällä kiinteää määrää eri hinnoitteluryhmissä. Jokainen taso on täytettävä, ennen kuin siirryt seuraavaan hinnoitteluryhmään.
    - **Kiinteä taso** – Laske yksikköhinta käyttämällä kiinteää määrää ja laajennettuja hintasummia eri hinnoitteluryhmissä. Laskutuskaudella veloitettava hinta käyttää laajennettua hintaa, joka vastaa laskutusmäärän tasoa.

7. Valitse **Nimiketyyppi**-kentästä laskutusryhmän nimikkeen tyyppi:

    - **Vakio** – Valitse tämä arvo, jos määrä on staattinen.
    - **Käyttö** – Valitse tämä arvo mitattaville tai kulutustyyppisille nimikkeille. Jos valitset tämän arvon, määritä **Käytön lukuasetus** -kentän arvoksi **Lukema** ja kirjoita laskutuskauden arvo (lukema) mittariin tai laitteeseen. Kulutettu arvo lasketaan edellisen laskutuskauden ja nykyisen lukeman perusteella.
    - **Tavoite** – Valitse tämä arvo, jos haluat käyttää tavoitteisiin perustuvan laskutuksen toimintoa. Jos valitset tämän arvon, valitse **Tavoitemalli**-kentästä tavoitemalli, jos käytät sellaista.
    - **Kulutus** – Valitse tämä arvo, jos haluat kirjoittaa laskutuskaudella kulutetun arvon.

8. Määritä **Laskuta erikseen** -asetuksen arvoksi **Kyllä** , kun haluat luoda yhdistelmän konsolidoiduista laskuista ja erillisistä laskuista samalle asiakkaalle. Asiakkaalla on esimerkiksi viisi laskutusaikataulua. Kolme niistä konsolidoidaan yhdelle laskulle, mutta kumpikin kahdesta muusta edellyttää erillistä laskua. Valitse **Ei**, jos haluat luoda asiakkaalle vain yhden konsolidoidun laskun.
9. Jos haluat uusia toistuvan laskutusaikataulun automaattisesti seuraavalle laskutuskaudelle, kun lasku luodaan, määritä **Uusi automaattisesti** -asetuksen arvoksi **Kyllä**. Anna arvoksi **Ei**, jos haluat uusia laskutusaikataulun manuaalisesti. Määritä **Uusintaa kohti lisättävät rivit** -kentässä, kuinka monta riviä haluat lisätä kuhunkin uusintaan.
10. Määritä **Eskalointi**-asetuksen arvoksi **Kyllä**, jos haluat käyttää *eskalaatioita* (hinnankorotuksia) tähän laskutusaikatauluryhmään liitettyihin laskutusaikatauluihin.
