---
title: Microsoft Dynamics 365 for Talentin valmisteleminen
description: "Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin uuden ympäristön valmisteluprosessista."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: Talent
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
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talentin valmisteleminen
Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin uuden ympäristön valmisteluprosessista. Ohjeaiheessa oletetaan, että olet ostanut Talent-sovelluksen pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. Jos sinulla on Microsoft Dynamics 365 -käyttöoikeus, joka sisältää Talent-palvelusopimuksen, etkä pysty suorittamaan tämän ohjeaiheen vaiheita, ota yhteys tukeen.

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

    Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä vain muutaman minuutin. Jos valmisteleminen epäonnistuu, ota yhteys tukeen.

6. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Talentiin**.

> [!NOTE]
> Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Talentin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

## <a name="create-a-new-powerapps-environment-if-required"></a>Uuden PowerApps-ympäristön luominen (tarvittaessa)
1. Valitse LCS:n **Ympäristöjen hallinta**. Siirryt [PowerApps-hallintakeskukseen](https://preview.admin.powerapps.com/environments), jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia ympäristöjä.
2. Valitse (**+**) **Uusi ympäristö** -painike.
3. Anna ympäristölle yksilöivä nimi ja valitse sijainti, jossa se otetaan käyttöön.

    > [!NOTE]
    > Talent ei ole saatavilla kaikilla alueilla. Tarkista saatavuus, ennen kuin valitset ympäristön sijainnin.

4. Kun sinulta kysytään, haluatko luoda tietokannan, valitse **Luo tietokanta**, jolloin Common Data Service (CDS) -tietokanta. Se isännöi osaa Talentin tiedoista. Kun tietokanta on luotu, voit integroida PowerApps-sovellukset Talentin kanssa.
5. Sinulta kysytään käyttöoikeustaso, jolla haluat käyttää tietokantaa. On suositeltavaa valita **Rajoitettu käyttö**, koska tällöin Talent-käyttäjät eivät voi käyttää luottamuksellisia tietoja PowerApps-sovelluksen avulla suoraan.
6. Luotu CDS-tietokanta sisältää demotietoja. Demotiedot ovat hyödyllisiä, koska voit käyttää demotietojen yritystä testauksessa ja luoda tehtävätallenteita tai tehtäväoppaita. Ota huomioon, että demotiedot lisäävät esimerkiksi passiivisia työntekijöitä ja kuvitteellisia osoitteita tuotantoympäristöön. Voit poistaa demotiedot seuraavien ohjeiden avulla sen jälkeen, kun CDS-tietokanta on luotu:

    > [!IMPORTANT]
    > Jos loit CDS-tietokannan aiemmin ja syötit tietokantaan yrityksen tuotantotietoja, ota huomioon, että nämä vaiheet poistavat **kaikki** valitun tietokannan tiedot, myös yrityksen tuotantotiedot.

    1. Kirjaudu sisään [PowerApps-sovellukseen](https://preview.web.powerapps.com/home) ja siirry vaiheessa 2 luomaasi ympäristöön.
    2. Valitse **Yksiköt**. Valitse sivun oikeassa reunassa ellipsipainike (**…**) ja valitse sitten **Tyhjennä kaikki tiedot**.
    3. Valitse **Poista tiedot**, kun haluat vahvistaa kaikkien tietojen poistamisen. Tämä toiminto poistaa kaikki CDS-tietokannan demotiedot oletusarvoisesti. Se poistaa myös kaikki muut kyseiseen tietokantaan syötetyt tiedot.

Nyt voit käyttää uutta ympäristöäsi.

