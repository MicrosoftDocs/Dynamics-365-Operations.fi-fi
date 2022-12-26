---
title: Mukautettujen kenttien luominen ja käsitteleminen
description: Tässä artikkelissa käsitellään sitä, miten mukautettuja kenttiä luodaan käyttöliittymässä sovelluksen muokkaamiseksi yrityksen tarpeita vastaaviksi.
author: jasongre
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18e7e8525352e8fdc397621c381ed4297837e30c
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887284"
---
# <a name="create-and-work-with-custom-fields"></a>Mukautettujen kenttien luominen ja käsitteleminen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Vaikka käytettävissä on useita valmiita kenttiä monenlaisten liiketoimintaprosessien hallintaa varten, joskus yritysten on seurattava myös muita järjestelmässä olevia tietoja. Ohjelmoijia voidaan hyödyntää lisättäessä näitä kenttiä laajennuksina kehittäjän työkaluihin. Mukautettujen kenttien toiminnon avulla kentät voidaan lisätä suoraan käyttöliittymästä, ja käyttäjä voi räätälöidä sovellusta liiketoiminnan vaatimusten mukaan selaimessa.

*Vain käyttäjät, joilla on erityiset käyttöoikeudet, voivat käyttää tätä ominaisuutta.*

Seuraavassa videossa näytetään, miten mukautettu kenttä on helppo lisätä sivulle: [Mukautettujen kenttien lisääminen](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Mukautettujen kenttien luominen

Kun sovelluksessa seurattavat tiedot on määritetty, mukautettu kenttä voidaan luoda soveltuvaan tauluun ja kyseinen uusi kenttä tuoda näkyviin sivulle.

Seuraavissa ohjeissa käsitellään mukautetun kentän luontiprosessia ja kyseisen kentän sijoittamista sivulle.

1. Siirry sivulla kohtaan, jossa uutta kenttää tarvitaan.
2. Koska varsinaisena tavoitteena on tuoda mukautettu kenttä näkyviin lomakkeessa, mukautettujen kenttien luonnin aloituskohta on mukautuskokemuksessa. Avaa mukauttamisen työkalurivi valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**.
3. Valitse ensin **Lisää** ja sitten **Kenttä**.
4. Valitse lomakkeessa alue, jossa haluat uuden kentän näkyvän. Valinnan jälkeen **Lisää kenttiä** -valintaikkunassa on luettelo aiemmin luoduista kentistä, jotka voidaan lisätä valitulle sivualueelle.
5. Vahvista, että haluamasi kenttä ei ole jo luettelossa. Jos löydät sen, sinun tarvitsee vain valita ensin kenttä luettelossa ja valita sitten **Lisää**.
6. Käynnistä mukautetun kentän luontiprosessi valitsemalla luettelon yläpuolella **Luo uusi kenttä**. **Luo uusi kenttä** -valintaikkuna avautuu.

    Jos **Luo uusi kenttä** -painike ei ole näkyvissä, ominaisuuden käyttöön tarvittavia käyttöoikeuksia ei ole.

7. Anna seuraavat tiedot **Luo uusi kenttä** -valintaikkunassa.
   
    1. Valitse tietokantataulu, johon tämä kenttä lisätään. Huomaa, että vain mukautettuja kenttiä tukevat taulut näkyvät avattavassa luettelossa. Jäljempänä on tuettujen taulujen tekniset tiedot.

    2. Valitse uuden kentän tietotyyppi. Valittavana on seuraavat tietotyypit: valintaruutu, päivämäärä, päivämäärä ja aika, desimaali, luku, valintaluettelo ja teksti.

        - Jos tietotyypiksi tekstin, voit määrittää myös kenttään annettavan tekstin enimmäispituuden.
        - Jos valitset tietotyypiksi valintaluettelon, voit valita myös arvot, joita kentässä saa käyttää.

    3. Anna kentälle nimi, otsikko ja ohjeteksti. Nimi vastaa tietokannan fyysistä kenttänimeä, kun taas otsikko ja ohjeteksti ovat kentän käyttöliittymässä käytettäviä tekstejä.

8. Jos tämä on ainoa tälle sivulle luotava kenttä, valitse **Tallenna**. Jos kenttiä on luotava lisää, valitse **Tallenna ja uusi** ja palaa vaiheeseen 7. 

>[!Note] 
> Tällä hetkellä **taulussa saa olla enintään 20 mukautettua kenttää**.

9. Kun poistut **Luo uusi kenttä** -valintaikkunassa, palaat **Lisää kenttiä** -valintaikkunaan. Juuri lisätyt mukautetut kentät merkitään kenttäluettelossa automaattisesti sivulle lisättäviksi.
10. Lisää merkityt kentät valitulle sivualueelle valitsemalla **Lisää**.
11. **Valinnainen:** Ota **Siirrä**-tila käyttöön mukauttamisen työkalurivillä, jos haluat siirtää uudet kentät paikalleen valitulle alueelle. Kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md) on lisätietoja, miten erilaisten mukauttamistoimintojen avulla lomakkeen voi optimoida omaa käyttöä varten.

> [!WARNING]
> Sivuun lisätyn mukautetun kentän arvojen lisääminen riippuu siitä, voiko mukautettuun kenttään liittyvää taulua muokata vai vain lukea. Kun liittyvä taulu on vain luku -muotoinen, kaikki tauluun linkitetyt kentät, mukaan lukien mukautetut kentät, ovat myös vain luku -kenttiä.


## <a name="sharing-custom-fields-with-other-users"></a>Mukautettujen kenttien jakaminen muiden käyttäjien kanssa

Kun olet luonut mukautetun kentän ja se näkyy sivulla, haluat ehkä tuoda uuden kentän sisältävän päivitetyn sivunäkymän muiden järjestelmän käyttäjien saataville. Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:

- Suositeltava reitti on **julkaista [tallennettu näkymä](saved-views.md)**, jossa mukautettu kenttä lisätään sivulle sopivalle käyttäjäjoukolle. Jos tallennettuja näkymiä ei ole otettu käyttöön, järjestelmänvalvoja voi käyttää mukauttamista toivottujen käyttäjien osalta **Mukauttaminen**-sivulla. Lisätietoja on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).
- Vaihtoehtoisesti voit viedä muutokset (eli *mukautukset*), lähettää ne yhdelle tai usealle käyttäjälle ja pyytää heitä jokaista tuomaan muutokset. Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin **Hallinta**-asetuksella.

## <a name="managing-custom-fields"></a>Mukautettujen kenttien hallinta

Kaikkia mukautettuja kenttiä voidaan hallita järjestelmänhallintamoduulin **Mukautetut kentät** -sivulla. Tällä sivulla käyttäjät voivat käyttää monia toimintoja, kuten

- tarkastella luetteloa kaikista järjestelmän mukautetuista kentistä
- aiemmin luotujen mukautettujen kenttien rajallinen muokkaus
- mukautettujen kenttien poistaminen
- mukautettujen kenttien tuominen tietoyksiköiden nähtäville
- mukautettujen kenttien otsikoiden ja ohjetekstien kääntäminen.

### <a name="viewing-all-custom-fields"></a>Kaikkien mukautettujen kenttien tarkastelu

Kaikki järjestelmässä määritetyt mukautetut kentät ovat näkyvissä **Mukautetut kentät** -sivulla. Valitse sopiva taulu, jonka jälkeen sivu päivittyy näyttämään luettelon kyseiseen tauluun liitetyistä mukautetuista kentistä. Voit tarkastella kaikkia kentän tietoja valitsemalla mukautetun kentän luettelossa.

### <a name="editing-custom-fields"></a>Mukautettujen kenttien muokkaaminen

Kentän luonnin jälkeen vain tiettyjä mukautetun kentän tietoja voi muokata **Mukautetut kentät** -sivulla.

*Voit* muokata seuraavia määritteitä:

- Nimiö
- Ohjeteksti
- Pituus (tekstikentissä)

Seuraavia määritteitä *ei* voi muokata:

- Kentän nimi
- Tietotyyppi

Lisäksi mukautetuista kentistä valintaluettelokenttien arvojoukon järjestystä voi muokata ja uusia arvoja voi lisätä. Valintaluettelokentässä olevia arvoja ei kuitenkaan saa poistaa. Tallenna muutokset valitsemalla **Ota muutokset käyttöön**, kun lopetat tietyn taulun kenttien muokkaamisen.

### <a name="exposing-custom-fields-on-data-entities"></a>Mukautettujen kenttien tuominen tietoyksiköiden nähtäville

On myös tärkeää, että tietoyksiköt voivat havaita mukautetut kentät. Tietoyksiköitä käytetään [Office-integroinnin yleiskatsaus](../../dev-itpro/office-integration/office-integration.md) -ominaisuudessa sekä tietojen tuonti- ja vientiskenaarioissa.

Voit tuoda mukautetun kentän tietoyksikön nähtäville seuraavasti:

1. Valitse mukautettu kenttä **Mukautetut kentät** -sivulla.
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

    Jos haluat muokata valmista käännöstä, valitse valikossa kieli sekä muokkaa otsikon ja ohjetekstin arvoja.

    Napsauta muussa tapauksessa **Lisää kieli** -painiketta, valitse valikossa kieli ja anna otsikon ja ohjetekstin käännetyt arvot.

4. Valitse **OK**, kun olet valmis.

### <a name="deleting-custom-fields"></a>Mukautettujen kenttien poistaminen

Kun mukautettua kenttää ei enää tarvita, järjestelmänvalvoja voi päättää poistaa kentän **Mukautetut kentät** -sivulta. Mukautettu kenttä poistetaan valitsemalla ensin poistettava kenttä ja sitten **Poista** sekä vahvistamalla poistaminen valitsemalla **Kyllä**. Lopuksi valitaan **Ota muutokset käyttöön**.

> [!NOTE]
> Tätä toimintoa ei voi kumota. Lisäksi kenttään liitetyt tiedot poistetaan pysyvästi tietokannasta.

## <a name="appendix"></a>Liite

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Miksi en voi määrittää arvoa mukautetussa kentässä? 

Jos et voi kirjoittaa arvoa mukautettuun kenttään, kun sivu on **muokkaustilassa**, tämä voi johtua siitä, että taulu, johon kenttä lisättiin, on tällä hetkellä vain luku -tilassa. Taulun kaikista kentistä tulee luku -kenttiä vain, jos taustataulu on määritetty tällä hetkellä sivulla vain luku -muotoiseksi.   

### <a name="who-can-create-custom-fields"></a>Kenellä on oikeus luoda mukautettuja kenttiä?

Vain järjestelmänvalvojat voivat oletusarvoisesti luoda mukautettuja kenttiä. Organisaatio voi kuitenkin antaa tarvittaessa sopiville tehokäyttäjille mukautettujen kenttien luontioikeudet. Järjestelmänvalvojat voivat tehdä sen käyttämällä **Suorituksenaikainen mukautuksen tehokäyttäjä** -käyttöoikeusroolia. Vaikka käyttäjät, joilla ei ole tätä käyttöoikeusroolia, eivät voi luoda mukautettuja kenttiä, he voivat kuitenkin nähdä ja käyttää muiden järjestelmän käyttäjien lisäämiä mukautettuja kenttiä.

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

### <a name="how-can-i-move-custom-fields-between-environments"></a>Miten mukautettuja kenttiä siirretään ympäristöjen välillä? 

Tällä hetkellä mukautettujen kenttiä suositellaan siirtämään ympäristöjen välillä siten, että mukautetut kentät luodaan uudelleen manuaalisesti kohdeympäristössä. Tietyn taulukon täydellisen mukautettujen kenttien luettelon tarkasteleminen:
1. Siirry **Mukautetut kentät** -sivulle ja valitse kyseinen taulukko avattavassa luettelossa. 
2. Luo kukin kenttä kohdeympäristössä uudelleen tämän artikkelin ohjeiden mukaisesti. 
3. Kun kaikki kentät on luotu, valitse **Käytä muutoksia**.  
4. Siirrä kaikki mukautuksia sisältävät mukautetut kentät viemällä kyseiset mukautukset alkuperäisestä ympäristöstä ja tuomalla ne kohdeympäristöön.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
