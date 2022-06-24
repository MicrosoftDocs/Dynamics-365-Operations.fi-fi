---
title: Mukautettujen X++-komentosarjojen ajaminen ilman käyttökatkoa
description: Tässä artikkelissa kuvataan, kuinka voit ladata ja suorittaa käyttöön otettavat paketit, jotka sisältävät mukautettuja X++-komentosarjoja ilman järjestelmän keskeytystä.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867326"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Mukautettujen X++-komentosarjojen ajaminen ilman käyttökatkoa

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Tämän ominaisuuden avulla voit ladata ja suorittaa käyttöön otettavat paketit, jotka sisältävät mukautettuja X++-komentosarjoja ilman, että järjestelmän tarvitse käydä läpi Microsoft Dynamics Lifecycle Servicesiä (LCS) tai keskeyttää sitä. Näin ollen voit korjata pieniä tietojen epäyhtenäisyyksiä aiheuttamatta häiriöitä.

X++-komentosarjan käyttämisen etuna pienten tietoepäyhtenäisyyksien korjaamisessa on, että järjestelmä muuttaa automaattisesti kaikki liittyvät taulut tarpeen mukaan, kun komentosarja suoritetaan. Tämän menetelmän avulla voidaan varmistaa korjauksen eheys ja vähentää uusien ristiriitaisuuksien riskiä.

> [!IMPORTANT]
> Tämä ominaisuus on tarkoitettu vain pienien tietojen epäyhdenmukaisuuksien korjaamiseen. Sitä ei saa käyttää seuraaviin tarkoituksiin tai mihinkään muuhun tarkoitukseen:
>
> - Tietojenkeruu
> - Skeemamuutokset
> - Tietojen siirto tai muut pitkäkestoiset prosessit
> - Tietojen korjaus, joka voidaan korjata muilla keinoin, kuten tavallisilla liiketoimintaprosesseilla, tietojen yhtenäisyystyökaluilla tai muilla itsepalvelutyökaluilla
>
> Ominaisuuden avulla valtuutettu käyttäjä voi muuttaa entiteettejä ja niiden tietueita suoraan ilman, että näihin yksiköihin liittyvää liiketoimintalogiikkaa tarvitse suorittaa. Nämä muutokset voivat aiheuttaa tietojen eheyden ongelmia. Siksi organisaatiosi saattaa edellyttää, että saat hyväksynnän sisäisiltä ja ulkoisilta tilintarkastajilta (tai muulta vastaavalta ulkopuoliselta ulkopuoliselta sidosryhmältä) ennen komentosarjan ajoa ja/tai sen jälkeen. Yhteensopivuussyistä joihinkin ominaisuuksiin vaikuttavia muutoksia on ehkä luovutettava myös ulkoisiin raportteihin (kuten tilinpäätöksiin) tai viranomaisille raportoitavaksi. Organisaatiosi on täysin vastuussa muutoksista, jotka tehdään sen tietoihin tämän toiminnon kautta, hyväksynnästä tai muutosten ilmaisemisesta sekä sovellettavan lainsäädännön noudattamisesta. Vastaat kaikista tämän ominaisuuden käyttämiseen liittyvistä riskeistä.

Kaikki järjestelmään ladatut käyttöönotettavat paketit käyvät läpi pakollisen työnkulun. Turvatoimenpiteenä ja velvollisuudet ja tehtävien eriyttämisen varmistamiseksi käyttäjä, joka lataa käyttöön otettavan paketin, ei voi hyväksyä sitä työnkulun seuraavia vaiheita varten. Toisen käyttäjän on hyväksyttävä se. Kun paketti on hyväksytty, sen palvelimeen ladannut käyttäjä voi kuitenkin suorittaa loput vaiheet.

Järjestelmä edellyttää, että kaikki käyttöön otettavat paketit kulkevat testisuorituksen läpi. Ennen kuin komentosarjan voi suorittaa tuotantotiedoille, käyttäjän on vahvistettava tuloksen oikeellisuus valitsemalla **Hyväksy testiloki**. Jos tulos ei ole oikein, käyttäjän on merkittävä paketti epäonnistuneeksi valitsemalla **Hylkää**. Tässä tapauksessa komentosarjaa ei voi suorittaa tuotantotiedoille.

Jokainen palvelimeen ladattu paketti tallennetaan järjestelmään ja kulkee määritettyjen tapahtumien työnkulun läpi. Järjestelmä säilyttää kunkin tapahtuman lokin, joka sisältää aikaleiman sekä tapahtuman suorittavan henkilön henkilöllisyyden. Näin järjestelmä varmistaa, että kirjausketju on olemassa.

Seuraavassa kuvassa järjestelmä tarjoaa tietoja siitä, miten kukin käyttöönotettava paketti suoritettiin X++:ssa ja mihin yksiköihin on koskettu.

![Komentosarjan tiedot -sivu.](media/script-details.png "Komentosarjan tiedot -sivu")

## <a name="assign-duties-to-users-to-control-access"></a>Käyttöoikeuksien hallinta määrittämällä velvollisuuksia käyttäjille

Tämän toiminto tarjoaa seuraavat tehtävät. Järjestelmänvalvojat voivat näiden tehtävien avulla ohjata toiminnon käyttöä.

- **Ylläpidä mukautettuja komentosarjoja** – Tämä tehtävä myöntää mahdollisuuden ladata, testata, tarkistaa ja suorittaa mukautettuja X++-komentosarjoja ympäristöissä (käyttäjän hyväksyntätestaus \[UAT\] ja tuotanto).
- **Mukautettujen komentosarjojen hyväksyminen** – Tämä tehtävä myöntää mahdollisuuden hyväksyä ladattu mukautettu X++-komentotiedosto. Hyväksyntä on pakollinen vaihe, ennen kuin mitään komentosarjoja voi testata, vahvistaa tai suorittaa.

Jokaisen komentosarjan on nimenomaisesti hyväksyttävä toinen käyttäjä kuin sen palvelimeen ladannut käyttäjä, jotta vihamielisten toimien riskiä voidaan vähentää. Ennen kuin voit käyttää tätä toimintoa organisaatiossasi, järjestelmänvalvojan on määritettävä edeltävät velvollisuudet vähintään kahdelle tärkeälle ja erittäin luotettavalle käyttäjälle. Vaikka yhdellä käyttäjällä voi olla molempia tehtäviä, hän ei silti voi hyväksyä omia komentosarjojaan.

## <a name="create-a-deployable-package"></a>Käyttöönotettavan paketin luominen

Toiminto edellyttää säännöllisesti käyttöön otettavaa pakettia, joka voidaan luoda Visual Studiossa. Lisätietoja: [Mallien käyttöönottopakettien luominen](../deployment/create-apply-deployable-package.md).

Käyttöön otettavan paketin on sisällettävä tasan yksi runnable X++ -luokka. Toisin sanoen sillä on oltava yksi luokka, joka sisältää menetelmän, jolla on seuraava allekirjoitus.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Päämetodin nimen on oltava pienillä kirjaimilla.

## <a name="code-example"></a>Koodiesimerkki

Seuraavassa koodiesi esimerkissä näytetään, miten käyttöön otettavan paketin rakenne voidaan luoda.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Parhaat käytännöt

Seuraavassa luettelossa on kuvattu komentotiedoston onnistuneesti kirjoittamisen, toteuttamisen ja ajamisen parhaat menetelmät. Luettelo ei ole tyhjentävä, ja sitä tulee pitää vain ohjeena.

- **Kirjoita** komentotiedoston loppuun onnistumissanoma. Näin voit nähdä, että komentosarja on suoritettu ilman poikkeuksia.
- **Lisää** eksplisiittinen tapahtuman käyttöalueen käsittely.
- **Käytä** aiemmin luotua liiketoimintalogiikkaa, kuten `update()`-menetelmiä, mutta **älä** ohita liiketoimintalogiikkaa käyttämällä `doUpdate()`-, `doInsert()`- tai `doDelete()`-menetelmiä. Tämän menetelmän avulla voidaan varmistaa, että sidonnaiset tiedot käsitellään oikein. Se myös vähentää huomattavasti tietojen epäyhdenmukaisuuksien riskiä.
- **Määritä** yrityskonteksti. Tämä menetelmä paljastaa yleiset virheet komentotiedostoa suoritettaessa. Komentosarjan suorittamisesta käy esimerkiksi ilmi, että komentosarja suoritetaan väärässä yrityksessä.
- **Määritä** myös niin, että tietueiden määrä vastaa odotuksiasi. Tämä menetelmä ilmaisee, siirretäänkö tietoja odottamattomalla tavalla järjestelmässä komentosarjan valmistelemisen aikana.
- **Käytä** jokaisessa komentotiedostossa yksilöllisiä luokan nimiä (esimerkiksi nimessä viittaus työnimikkeeseen). Tämä menetelmä estää nimiristiriidat, kun lataat komentosarjan palvelimeen. Jos komentotiedoston uusi iteraatio on pakollinen, muista antaa sille uusi nimi.
- **Testaa** jokainen komentotiedosto ensin ei-tuotantoympäristössä. Tee testaus, jossa testataan aiottu vaikutus ja sivuvaikutukset liittyviin tietoihin. Varmista, että kaikki liiketoimintaprosessit, jotka voivat muuttua, voidaan suorittaa onnistuneesti ja kokonaan jälkeenpäin.

## <a name="upload-and-run-a-deployable-package"></a>Käyttöön otettavan paketin lataaminen palvelimeen ja ajaminen

Lataa ja suorita komentotiedosto seuraavia ohjeita noudattamalla.

1. Siirry taloushallinnon ja toimintojen sovelluksessa kohtaan **Järjestelmänvalvonta \> Kausittaiset tehtävät \> Tietokanta \> Mukautetut komentosarjat**.
1. Valitse **Lataa palvelimeen**.
1. Valitse käyttöön otettava paketti, joka on luotu aiemmin tässä artikkelissa kuvatulla tavalla. Näyttöön tule kehote määrittää komentosarjan tarkoitus.
1. Komentosarja pitää hyväksyttää nyt toisella käyttäjällä kuin sen palvelimeen ladannut käyttäjä. Hyväksyjän on noudatettava seuraavia ohjeita:

    1. Siirry kohtaan **Järjestelmänvalvonta \> Kausittaiset \> Tietokanta \> Mukautetut komentosarjat**.
    1. Valitse hyväksyttävä komentotiedosto ja valitse sitten **Tiedot**.
    1. Valitse toimintoruudun **Käsittele työnkulku** -välilehden **Aloita**-ryhmässä **Hyväksy** tai **Hylkää**. Jos valitset **Hyväksy**, komentosarja merkitään hyväksytyksi ja sen lukitus avataan testausta varten. Jos valitset **Hylkää**, komentosarja lukitaan. Molemmissa tapauksissa tapahtuma kirjataan lokiin ja komentosarjan kopio säilytetään järjestelmässä.

1. Komentosarja on testattava, jotta se toimii siten kuin se on tarkoitettu käytettäväksi. Testaaja voi olla sama kuin palvelimeen lataaja tai hyväksyjä, tai kolmas käyttäjä, jolla on tarvittavat käyttöoikeudet. Testaajan on noudatettava seuraavia ohjeita:

    1. Siirry kohtaan **Järjestelmänvalvonta \> Kausittaiset \> Tietokanta \> Mukautetut komentosarjat**.
    1. Valitse testattava komentotiedosto ja valitse sitten **Tiedot**.
    1. Valitse toimintoruudun **Käsittele työnkulku**-välilehden **Testaa**-ryhmässä **Suorita testi**. Komentosarja suoritetaan väliaikaisen tapahtuman sisällä, joka keskeytyy automaattisesti, kun järjestelmä kerää erilaisia lokeja ja SQL-lausekkeita.
    1. Kun komentosarja on suoritettu loppuun, tarkista lokit ja varmista, että tulokset vastaavat odotuksiasi. Noudata seuraavia ohjeita:

        - Jos olet tyytyväinen testitulokseen, salli komentosarjan ajo valitsemalla toimintoruudun **Prosessityönkulku**-välilehden **Testi**-ryhmästä **Hyväksy testiloki**. Tapahtumalokissa näkyy se, että komentosarja testattiin, ja se ilmaisee, kuka testasi sitä, ja milloin.
        - Jos et ole tyytyväinen testitulokseen, estä komentosarjan ajo valitsemalla toimintoruudun **Prosessityönkulku**-välilehden **Loppu**-ryhmästä **Hylkää**. Järjestelmä säilyttää komentosarjan kopion sekä sen historialokin.

1. Kun olet varma, että komentosarja vastaa odotuksiesi, suorita komento valitsemalla toimintoruudun **Prosessityönkulku**-välilehdessä **Suorita**-ryhmästä **Suorita**. Tämä komento tekee samanlaista kuin edellinen testiajo, mutta tapahtuma sidotaan lopuksi.
1. Kun komentosarja on suoritettu loppuun, tarkista tulos ja vahvista, että komentosarja toimi suunnitellulla tavalla. Noudata seuraavia ohjeita:

    - Jos olet tyytyväinen tulokseen, valitse **Tarkoitus ratkaistu** -toimintoruudun **Prosessityönkulku**-välilehden **Lopetus**-ryhmästä. Tapahtumalokissa näkyy se, että komentosarja suoritettiin onnistuneesti, ja se ilmaisee, kuka vahvisti komentosarjan ja milloin. Komentosarja tallennetaan, mutta se on nyt lukittu eikä sitä voi enää suorittaa.
    - Jos et ole tyytyväinen tulokseen, valitse **Tarkoitusta ei ratkaistu** -toimintoruudun **Prosessityönkulku**-välilehden **Lopetus**-ryhmästä. Tapahtumalokissa näkyy se, että komentosarja epäonnistui sen tarkoituksen täyttämisessä, ja se ilmaisee, kuka suoritti komentosarjan ja milloin. Komentosarja tallennetaan, mutta se on nyt lukittu eikä sitä voi enää suorittaa. Järjestelmä ei kuitenkaan kumoa komentosarjan toimintoa automaattisesti. Sinun on ehkä kirjoitettava, tuotava ja suoritettava uusi komentotiedosto, jonka avulla voit kumota järjestelmän epäonnistuneen komentosarjan vaikutuksen.

Viimeisessä vaiheessa valintasi määrittää komentotiedoston lopullisen tilan. Voit toistaa prosessin tarpeen mukaan.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Käyttöön otettavan paketin lataaminen palvelimeen ja ajaminen LCS:n kautta

Sen sijaan, että otat käyttöön käyttöönotettavan pakettisi taloushallinnon ja toimintojen sovelluksen käyttöliittymässä edellisessä osassa kuvatulla tavalla, voit ladata sen LCS-palveluun ja ottaa sen käyttöön tavallisen menetelmän avulla. Lisätietoja: [Käyttöönotettavien pakettien asentaminen komentoriviltä](../deployment/install-deployable-package.md).

Vaikka tällä menetelmällä on vähemmän rajoituksia, se antaa vähemmän virhesuojaa. Lisäksi, koska kaikki palvelimet on käynnistettävä uudelleen, se aiheuttaa käyttökatkoksen.
