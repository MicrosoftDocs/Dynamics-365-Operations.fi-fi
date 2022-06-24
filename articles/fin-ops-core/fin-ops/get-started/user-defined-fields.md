---
title: Mukautettujen kenttien luominen ja käsitteleminen
description: Tässä artikkelissa käsitellään sitä, miten mukautettuja kenttiä luodaan käyttöliittymässä sovelluksen muokkaamiseksi yrityksen tarpeita vastaaviksi.
author: jasongre
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: fdb4d0065bd12fc721ce55314c0a46fe8d17c6ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847125"
---
# <a name="create-and-work-with-custom-fields"></a>Mukautettujen kenttien luominen ja käsitteleminen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Vaikka käytettävissä on useita valmiita kenttiä monenlaisten liiketoimintaprosessien hallintaa varten, joskus yritysten on seurattava myös muita tietoja järjestelmässä. Ohjelmoijia voidaan käyttää näiden kenttien lisäämisessä laajennuksina kehittäjän työkaluihin. Mukautettujen kenttien toiminnon avulla kentät voidaan lisätä suoraan käyttöliittymästä. Näin käyttäjä voi räätälöidä sovellusta liiketoiminnan vaatimusten mukaan selaimessa.

*Vain käyttäjät, joilla on erityiset käyttöoikeudet, voivat käyttää tätä ominaisuutta.*

Tässä videossa näytetään, miten helppoa mukautetun kentän lisääminen sivulle on: [Mukautettujen kenttien lisääminen](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Mukautettujen kenttien luominen

Kun olet tunnistanut tiedot, joita haluat seurata sovelluksessa, voit luoda mukautetun kentän soveltuvaan tauluun ja tuoda kyseisen uuden kentän näkyviin sivulle.

Seuraavissa ohjeissa käsitellään mukautetun kentän luontiprosessi ja kyseisen kentän sijoittaminen lomakkeeseen.

1. Siirry lomakkeessa kohtaan, jossa uutta kenttää tarvitaan.
2. Koska varsinaisena tavoitteena on tuoda mukautettu kenttä näkyviin lomakkeessa, mukautettujen kenttien luonnin aloituskohta on mukautuskokemuksessa. Avaa mukauttamisen työkalurivi valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**.
3. Valitse ensin **Lisää** ja sitten **Kenttä**.
4. Valitse lomakkeessa alue, jossa haluat uuden kentän näkyvän. Valinnan jälkeen **Lisää kenttiä** -valintaikkunassa on luettelo aiemmin luoduista kentistä, jotka voidaan lisätä valitulle lomake-alueelle.
5. Varmista, että haluamasi kenttä ei ole jo luettelossa. Jos löydät sen, sinun tarvitsee vain valita ensin kenttä luettelossa ja valita sitten **Lisää**.
6. Käynnistä mukautetun kentän luontiprosessi valitsemalla luettelon yläpuolella **Luo uusi kenttä**. **Luo uusi kenttä** -valintaikkuna avautuu.

    Jos **Luo uusi kenttä** -painike ei ole näkyvissä, sinulla ei ole ominaisuuden käyttöön tarvittavia käyttöoikeuksia.

7. Anna seuraavat tiedot **Luo uusi kenttä** -valintaikkunassa.
   
    1. Valitse tietokantataulu, johon tämä kenttä lisätään. Huomaa, että vain mukautettuja kenttiä tukevat taulut näkyvät avattavassa luettelossa. Jäljempänä on tuettujen taulujen tekniset tiedot.

    2. Valitse uuden kentän tietotyyppi. Valittavana on seuraavat tietotyypit: valintaruutu, päivämäärä, päivämäärä ja aika, desimaali, luku, valintaluettelo ja teksti.

        - Jos tietotyypiksi tekstin, voit määrittää myös kenttään annettavan tekstin enimmäispituuden.
        - Jos valitset tietotyypiksi valintaluettelon, voit valita myös arvot, joita kentässä saa käyttää.

    3. Anna kentälle nimi, otsikko ja ohjeteksti. Nimi vastaa tietokannan fyysistä kenttänimeä, kun taas otsikko ja ohjeteksti ovat kentän käyttöliittymässä käytettäviä tekstejä.

8. Jos tämä on ainoa tähän lomakkeeseen luotava kenttä, valitse **Tallenna**. Jos kenttiä on luotava lisää, valitse **Tallenna ja uusi** ja palaa vaiheeseen 7. Huomaa, että tällä hetkellä **taulussa saa olla enintään 20 mukautettua kenttää**.
9. Kun poistut **Luo uusi kenttä** -valintaikkunassa, palaat **Lisää kenttiä** -valintaikkunaan. Juuri lisätyt mukautetut kentät merkitään kenttäluettelossa automaattisesti lomakkeeseen lisättäviksi.
10. Lisää merkityt kentät valitulle lomakealueelle valitsemalla **Lisää**.
11. **Valinnainen:** Ota **Siirrä**-tila käyttöön mukauttamisen työkalurivillä, jos haluat siirtää uudet kentät paikalleen valitulle alueelle. Kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md) on lisätietoja, miten erilaisten mukauttamistoimintojen avulla lomakkeen voi optimoida omaa käyttöä varten.

> [!WARNING]
> Sivuun lisätyn mukautetun kentän arvojen lisääminen riippuu siitä, voiko mukautettuun kenttään liittyvää taulua muokata vai vain lukea. Kun liittyvä taulu on vain luku -muotoinen, kaikki tauluun linkitetyt kentät, mukaan lukien mukautetut kentät, ovat myös vain luku -kenttiä.


## <a name="sharing-custom-fields-with-other-users"></a>Mukautettujen kenttien jakaminen muiden käyttäjien kanssa

Kun olet luonut mukautetun kentän ja se näkyy sivulla, haluat ehkä tuoda uuden kentän sisältävän päivitetyn sivunäkymän muiden järjestelmän käyttäjien saataville. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suositeltava reitti on **julkaista [tallennettu näkymä](saved-views.md)**, jossa mukautettu kenttä lisätään sivulle sopivalle käyttäjäjoukolle. Jos tallennettujen näkymien toiminto ei ole käytössä, järjestelmänvalvoja voi käyttää mukauttamista haluamallesi käyttäjälle Mukauttaminen-lomakkeessa. Lisätietoja on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).
- Vaihtoehtoisesti voit viedä muutokset (eli *mukautukset*), lähettää ne yhdelle tai usealle käyttäjälle ja pyytää heitä jokaista tuomaan muutokset. Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin **Hallinta**-asetuksella.

## <a name="managing-custom-fields"></a>Mukautettujen kenttien hallinta

Järjestelmän kaikkia mukautettuja kenttiä voi hallita järjestelmänhallintamoduulin **Mukautetut kentät** -sivulla. Tällä sivulla käyttäjät voivat käyttää monia toimintoja, kuten

- tarkastella luetteloa kaikista järjestelmän mukautetuista kentistä
- aiemmin luotujen mukautettujen kenttien rajallinen muokkaus
- mukautettujen kenttien poistaminen
- mukautettujen kenttien tuominen tietoyksiköiden nähtäville
- mukautettujen kenttien otsikoiden ja ohjetekstien kääntäminen.

### <a name="viewing-all-custom-fields"></a>Kaikkien mukautettujen kenttien tarkastelu

Kaikki järjestelmässä määritetyt mukautetut kentät ovat näkyvissä **Mukautetut kentät** -sivulla. Valitse vain sopiva taulu ja päivittyvällä sivulla on luettelo kyseiseen tauluun liitetyistä mukautetuista kentistä. Voit tarkastella kaikkia kentän tietoja valitsemalla mukautetun kentän luettelossa.

### <a name="editing-custom-fields"></a>Mukautettujen kenttien muokkaaminen

Kentän luonnin jälkeen vain tiettyjä mukautetun kentän tietoja voi muokata **Mukautetut kentät** -sivulla.

*Voit* muokata seuraavia määritteitä:

- Nimiö
- Ohjeteksti
- Pituus (tekstikentissä)

*ET* voi muokata seuraavia määritteitä:

- Kentän nimi
- Tietotyyppi

Lisäksi mukautetuista kentistä valintaluettelokenttien arvojoukon järjestystä voi muokata ja uusia arvoja voi lisätä. Valintaluettelokentässä olevia arvoja ei kuitenkaan saa poistaa. Muista tallentaa muutokset valitsemalla **Ota muutokset käyttöön**, kun lopetat tietyn taulun kenttien muokkaamisen.

### <a name="exposing-custom-fields-on-data-entities"></a>Mukautettujen kenttien tuominen tietoyksiköiden nähtäville

On myös tärkeää, että tietoyksiköt voivat havaita mukautetut kentät. Tietoyksiköitä käytetään [Office-integroinnin yleiskatsaus](../../dev-itpro/office-integration/office-integration.md) -toiminnossa sekä tietojen tuonti- ja vientiskenaarioissa.

Voit tuoda mukautetun kentän tietoyksikön nähtäville seuraavasti:

1. Valitse mukautettu kenttä **Mukautetut kentät** -lomakkeessa.
2. Tuo soveltuvat yksiköt näkyviin laajentamalla **Yksiköt**-osa.
3. Napsauta **Muokkaa**-painiketta.
4. Muokkaa kullekin yksikölle valittavaa **Käytössä**-kenttää, jonka on tuotava tämä kenttä näkyviin.
5. Tallenna valinnat valitsemalla **Ota muutokset käyttöön**.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Mukautettujen kenttien näyttämisen salliminen muilla kielillä

Koska eri kieltä käyttävien käyttäjien on ehkä voitava käyttää mukautettuja kenttiä, **Mukautetut kentät** -sivulla on mekanismi, jolla mukautetun kentän otsikko ja ohjeteksti voidaan kääntää muille kielille.

Mukautetut kentät voidaan kääntää muille kielille seuraavasti:

1. Valitse mukautettu kenttä **Mukautetut kentät** -sivulla.
2. Valitse toimintoruudussa **Käännökset**-painike. Kentän aiemmat käännökset sisältävä avattava valikko avautuu.
3. Avattavassa **Kieli**-luettelossa on kielet, joille on jo tehty käännöksiä.

    Jos haluat muokata valmista käännöstä, valitse valikossa kieli ja muokkaa otsikon ja ohjetekstin arvoja.

    Napsauta muussa tapauksessa **Lisää kieli** -painiketta, valitse valikossa kieli ja anna otsikon ja ohjetekstin käännetyt arvot.

4. Valitse **OK**, kun olet valmis.

### <a name="deleting-custom-fields"></a>Mukautettujen kenttien poistaminen

Joskus harvoin voi käydä niin, että mukautettua kenttää ei enää tarvita. Järjestelmänvalvoja voi päättää silloin poistaa kentän **Mukautetut kentät** -sivulta. Varmista siinä tapauksessa, että oikea kenttä on valittu. Valitse sitten **Poista** ja vahvista poista valitsemalla **Kyllä**. Valitse lopuksi **Ota muutokset käyttöön**.

> [!NOTE]
> Tätä toimintoa ei voi peruuttaa. Lisäksi kenttään liitetyt tiedot poistetaan pysyvästi tietokannasta.

## <a name="appendix"></a>Liite

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Miksi en voi määrittää arvoa mukautetussa kentässä? 

Jos et voi kirjoittaa arvoa mukautettuun kenttään, kun sivu on muokkaustilassa, tämä voi johtua siitä, että taulu, jonne kenttä lisättiin, on tällä hetkellä vain luku -tilassa. Taulun kaikista kentistä tulee luku -kenttiä vain, jos taustataulu on määritetty tällä hetkellä sivulla vain luku -muotoiseksi.   

### <a name="who-can-create-custom-fields"></a>Kenellä on oikeus luoda mukautettuja kenttiä?

Järjestelmän suojaamiseksi vain järjestelmänvalvojat voivat oletusarvoisesti luoda mukautettuja kenttiä. Organisaatio voi kuitenkin antaa tarvittaessa sopiville tehokäyttäjille mukautettujen kenttien luontioikeudet. Järjestelmänvalvojat voivat tehdä sen käyttämällä **Suorituksenaikainen mukautuksen tehokäyttäjä** -käyttöoikeusroolia. Vaikka käyttäjät, joilla ei ole tätä käyttöoikeusroolia, eivät voi luoda mukautettuja kenttiä, he voivat kuitenkin nähdä ja käyttää muiden järjestelmän käyttäjien lisäämiä mukautettuja kenttiä.

### <a name="what-tables-support-custom-fields"></a>Mitkä taulukot tukevat mukautettuja kenttiä?

Suorituskyvyn ja teknisten syiden vuoksi vain seuraavat ehdot täyttävät taulut sallivat tällä hetkellä mukautettujen kenttien lisäämisen.

- Taulun on luotava merkitty joksikin seuraavista ryhmistä:

    - Ryhmä
    - WorksheetHeader
    - Otsikko
    - Muut
    - Parametri
    - Viite
    - TransactionHeader

- Taulu ei voi laajentaa toista taulua.
- Taulua ei voi merkitä järjestelmätauluksi.
- Taulu ei voi olla väliaikainen taulu.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Voinko viitata mukautettuihin kenttiin kehittäjän työkaluissa?  

Mukautettuja kenttiä voi hallinnoida vain käyttöliittymässä. Niihin ei voi viitata koodilla. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
