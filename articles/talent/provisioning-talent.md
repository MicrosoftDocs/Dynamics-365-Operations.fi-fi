---
title: Microsoft Dynamics 365 for Talentin valmisteleminen
description: "Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin uuden ympäristön valmisteluprosessista."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: fi-fi
ms.lasthandoff: 03/02/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talentin valmisteleminen

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin tuotantouuden ympäristön valmisteluprosessista. Ohjeaiheessa oletetaan, että olet ostanut Talent-sovelluksen pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. Jos sinulla on Microsoft Dynamics 365 -käyttöoikeus, joka sisältää Talent-palvelusopimuksen, etkä pysty suorittamaan tämän ohjeaiheen vaiheita, ota yhteys tukeen.

Aluksi yleisen järjestelmänvalvojan tulee kirjautua [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) -palveluun ja luoda uusi Talent-projekti. Jos Talentin käyttämistä estävä ongelma ei liity käyttöoikeuteen, tuen tai Dynamics-palvelun kehityspalvelun edustajien apua ei tarvita.

## <a name="create-an-lcs-project"></a>LCS-projektin luominen
Luo ensin LCS-projekti, jotta voit hallinnoida Talent-ympäristöjä LCS:n avulla.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index) samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.
2. Luo projekti valitsemalla plusmerkki (**+**).
3. Valitse tuotteen nimeksi ja versioksi **Microsoft Dynamics 365 for Talent**.
4. Valitse **Dynamics 365 for Talent** -metodologia.
5. Valitse **Luo**.

Lisätietoja Talent-sovelluksen aloittamisesta on uudelle projektille luomassasi **Talent**-metodologiassa. Kun projekti on valmis, noudata seuraavia ohjeita ja valmistele Talent-ympäristö.

## <a name="provision-a-talent-project"></a>Talent-projektin valmisteleminen
Kun LCS-projekti on luotu, voit valmistella Talent-sovelluksen ympäristöä varten.

1. Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.
2. Talent valmistellaan aina Microsoft PowerApps -ympäristössä, jotta PowerApps-integrointi ja laajennus saadaan käyttöön. Jos PowerApps-ympäristö ei ole käytössä, seuraa tämän ohjeaiheen Uuden PowerApps-ympäristön luominen (tarvittaessa) -osan vaiheita, ennen kuin jatkat.

    > [!NOTE]
    > Voit tarkastella aiemmin luotuja ympäristöja tai luoda uusia ympäristöjä, kun Talent-sovelluksen valmistelevalle vuokraajan järjestelmänvalvojalle on määritetty PowerApps P2 -käyttöoikeus. Jos organisaatiolla ei ole PowerApps P2 -käyttöoikeutta, voit hankkia sen pilvipalveluratkaisujen toimittajalta tai [PowerApps-hinnoittelusivulta](https://powerapps.microsoft.com/en-us/pricing/).

3. Valitse **Add** ja valitse sitten Talentiin valmisteltava ympäristö.
4. Hyväksy ehdot ja aloita käyttöönotto valitsemalla **Kyllä**.

    Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä vain muutaman minuutin. Jos valmisteluprosessi epäonnistuu, ota yhteys tukeen.

6. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Talentiin**.

> [!NOTE]
> Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Talentin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

> [!NOTE]
> LCS-palvelujen kautta valmistellut Talent-ympäristöt eivät sisällä henkilöstöhallintotehtäville määritettyjä demotietoja tai Talent-kohtaisia tietoja. Jos tarvitset demotiedot sisältävän ympäristön, on suositeltavaa rekisteröityä 60 vuorokauden maksuttomaan [Talent-kokeiluympäristöön](https://dynamics.microsoft.com/en-us/talent/overview/). Vaikka kokeiluympäristön pyytänyt käyttäjä omistaa ympäristön, muita käyttäjiä voidaan kutsua henkilöstöhallinnon perusversion järjestelmänhallintakokemuksen kautta. Kokeiluympäristössä on kuvitteellisia tietoja, joiden avulla ohjelmaan voi tutustua turvallisesti. Niitä ei ole tarkoitettu käytettäväksi tuotantoympäristöinä. Huomaa, että kun kokeiluympäristö vanhenee 60 päivän kuluttua, sen kaikki tiedot poistetaan eikä niitä voi palauttaa. Voit rekisteröidä uuden kokeiluympäristön, kun aiemmin luotu ympäristö vanhenee.

## <a name="create-a-new-powerapps-environment-if-required"></a>Uuden PowerApps-ympäristön luominen (tarvittaessa)
Talent- ja PowerApps-ympäristöjen välinen integrointi sallii Talent-tietojen integroinnin ja käytön laajentamisen PowerApps-työkaluilla. PowerApps-ympäristöjen tarkoituksen tiedostaminen auttaa luomaan sovelluksia, jotka vastaavat Talentin laajentamiseen liittyviä tarpeita. Lisätietoja PowerApps-ympäristöistä, kuten ympäristön laajuudesta, ympäristön käytöstä sekä ympäristön luomisesta ja valitsemisesta, on kohdassa [PowerApps-ympäristöjen julkaiseminen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Vaikka jokainen vuokraaja valmistellaan automaattisesti PowerApps-oletusympäristössä, se ei välttämättä ole paras ympäristö Talentin käyttöönottoon. Tietojen integrointia ja testausstrategioita on pohdittava tässä vaiheessa, joten käyttöönoton erilaiset vaikutukset kannattaa harkita tarkasti, sillä joitakin tehtyjä valintoja ei ole helppo tehdä myöhemmin. 

Vaikka jokainen vuokraaja valmistellaan automaattisesti PowerApps-oletusympäristössä, se ei välttämättä ole paras ympäristö Talentin käyttöönottoon. Tietojen integrointia ja testausstrategioita on pohdittava tämän vaiheen aikana. Tämän vuoksi on pohdittava, mitä vaikutuksia käyttöönotolla on, koska muutoksia on hankala tehdä myöhemmin PowerApps-ympäristössä.

1. Valitse LCS:ssä **Hallitse ympäristöjä**. Siirryt [PowerApps-hallintakeskukseen](https://preview.admin.powerapps.com/environments), jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia ympäristöjä.
2. Valitse**Uusi ympäristö**.
3. Anna ympäristölle yksilöivä nimi ja valitse sijainti, jossa se otetaan käyttöön.

    > [!NOTE]
    > Talent ei ole saatavilla kaikilla alueilla. Tarkista saatavuus, ennen kuin valitset ympäristön sijainnin.

4. Kun sinulta kysytään, haluatko luoda tietokannan, valitse **Luo tietokanta**, jolloin Common Data Service (CDS) -tietokanta. Se isännöi osaa Talentin tiedoista. Kun tietokanta on luotu, voit integroida PowerApps-sovellukset Talentin kanssa.
5. Sinulta kysytään, mitä käyttöoikeustasoa tietokannassa käytetään. On suositeltavaa valita **Rajoitettu käyttö**, koska tällöin Talent-käyttäjät eivät voi käyttää luottamuksellisia tietoja PowerApps-sovelluksen avulla suoraan.
6. Luotu CDS-tietokanta sisältää demotiedot, jotka lisäävät esimerkiksi passiivisia työntekijöitä ja kuvitteellisia osoitteita tuotantoympäristöön. Voit poistaa demotiedot seuraavien ohjeiden avulla sen jälkeen, kun CDS-tietokanta on luotu:

    > [!IMPORTANT]
    > Jos loit CDS-tietokannan aiemmin ja annoit tietokantaan yrityksen tuotantotietoja, nämä vaiheet poistavat **kaikki** valitun tietokannan tiedot, myös yrityksen tuotantotiedot.

    1. Kirjaudu [PowerApps](https://preview.web.powerapps.com/home)-sovellukseen.
    2. Valitse oikealla ylhäällä avattavassa luettelossa ympäristö, jonka loit vaiheessa 2.
    3. Laajenna **Common Data Service** vasemmassa siirtymisruudussa ja valitse sitten **Yksiköt**.
    4. Valitse sivun oikeassa reunassa ellipsipainike (**…**) ja valitse sitten **Tyhjennä kaikki tiedot**.
    5. Valitse **Poista tiedot**, kun haluat vahvistaa kaikkien tietojen poistamisen. Tämä toiminto poistaa kaikki CDS-tietokannan demotiedot oletusarvoisesti. Se poistaa myös kaikki muut kyseiseen tietokantaan syötetyt tiedot.

Nyt voit käyttää uutta ympäristöäsi.

## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen
Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Sovelluksen muille käyttäjille käyttöoikeus on myönnettävä erikseen. Voit myöntää käyttöoikeuden [lisäämällä käyttäjiä](../dev-itpro/sysadmin/tasks/create-new-users.md) ja [määrittämällä heille sopivat roolit](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) henkilöstöhallinnon perusympäristössä.. Kyseiset käyttäjät on lisättävä myös PowerApps-ympäristöön, jotta he voivat käyttää Attract- ja Onboard-sovelluksia. Menettely käsitellään täällä. Jos tarvitset apua vaiheiden suorittamiseen, lisätietoja on blogikirjoituksessa [PowerApps-hallintakeskuksen esittely](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Tämän menettelyn suorittaa Talent-ympäristön käyttöönottanut yleinen järjestelmänvalvoja.

1. Avaa [PowerApps-hallintakeskus](https://preview.admin.powerapps.com/environments).
2. Valitse soveltuvat ympäristöt.
3. Lisää **Suojaus**-välilehdessä tarvittavat käyttäjät **ympäristön tekijän** rooliin.

Huomaa, että tämä viimeinen käyttäjien manuaalinen lisäysvaihe PowerApps-ympäristöön on väliaikainen. Se suoritetaan lopuksi automaattisesti, kun käyttäjät lisätään henkilöstöhallinnon perusversioon.

