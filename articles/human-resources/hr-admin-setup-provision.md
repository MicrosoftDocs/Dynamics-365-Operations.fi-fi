---
title: Valmistele Human Resources
description: Tässä artikkelissa kerrotaan Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmisteluprosessista.
author: andreabichsel
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 88a0be50a9b861190e7ce9b3f56bb4e583b791d1
ms.sourcegitcommit: 33685a5cc37081a189279e917def7f122d3beaef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/24/2020
ms.locfileid: "3285486"
---
# <a name="provision-human-resources"></a>Valmistele Human Resources

Tässä artikkelissa kerrotaan Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmisteluprosessista. Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. Jos sinulla on Microsoft Dynamics 365 -käyttöoikeus, joka sisältää Human Resourcesin palvelusopimuksen, etkä pysty suorittamaan tämän artikkelin vaiheita, ota yhteys tukeen.

Aluksi yleisen järjestelmänvalvojan tulee kirjautua [Microsoft Dynamics Lifecycle Servicesiin](https://lcs.dynamics.com) (LCS) ja luoda uusi Human Resources -projekti. Jos Human Resourcesin käyttämistä estävä ongelma ei liity käyttöoikeuteen, tuen tai Dynamics-palvelun kehityspalvelun edustajien apua ei tarvita.

## <a name="create-an-lcs-project"></a>LCS-projektin luominen

Luo ensin LCS-projekti, jotta voit hallinnoida Human Resources -ympäristöjä LCS:n avulla.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.

2. Luo projekti valitsemalla plusmerkki (**+**).

3. Valitse tuotteen nimeksi ja versioksi **Microsoft Dynamics 365 Human Resources**.

4. Valitse **Dynamics 365 Human Resources** -menetelmä.

5. Valitse **Luo**.

Lisätietoja Human Resources -sovelluksen aloittamisesta on uudelle projektille luomassasi **Human Resources** -metodologiassa. Kun projekti on valmis, noudata seuraavia ohjeita ja valmistele Human Resources -ympäristö.

## <a name="provision-a-human-resources-project"></a>Human Resources -projektin valmisteleminen

Kun LCS-projekti on luotu, voit valmistella Human Resources -sovelluksen ympäristöä varten.

1. Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.

2. Määritä, onko tämä ympäristö Human Resourcesin eristys- vai tuotantoesiintymä. Varhaisia esikatselutoimintoja voi olla käytettävissä Sandbox-esiintymissä, jotta varhainen palaute ja testaaminen olisi mahdollista.
   
    > [!NOTE]
    > Human Resources-ilmentymätyyppiä ei voi muuttaa kerran määritettynä. Tarkista, että oikea ilmentymätyyppi on valittuna, ennen kuin jatkat.</br></br>
    > Human Resources -esiintymätyyppi on erillään Microsoft Power Apps-ympäristön esiintymätyypistä, jonka määrität Power Apps-hallintakeskuksesta.
    
3. Valitse **Sisällytä esittelytiedot** -vaihtoehto, jos haluat ympäristösi sisältävän saman esittelytietojoukon, jota käytetään Human Resources Test Drive -kokemuksessa. Esittelytiedot ovat hyödyllisiä pitkän aikavälin esittely- tai koulutusympäristöissä, eikä niitä tule koskaan käyttää tuotantoympäristöissä. Tämä asetus on valittava ensimmäisen käyttöönoton yhteydessä. Et voi päivittää aiemmin luotua käyttöönottoa myöhemmin.

4. Human Resources valmistellaan aina Microsoft Power Apps -ympäristössä, jotta Power Apps-integrointi ja laajennettavuus voidaan ottaa käyttöön. Lue tämän artikkelin ”Power Apps-ympäristön valitseminen” -osio ennen kuin jatkat. Jos sinulla ei vielä ole Power Apps-ympäristöä, valitse Hallitse ympäristöjä LCS:ssä tai siirry Power Apps-hallintakeskukseen. Noudata kohdan [Power Apps-ympäristön luominen](https://docs.microsoft.com/powerapps/administrator/create-environment) ohjeita.

5. Valitse ympäristö, johon Human Resources sisällytetään.

6. Hyväksy ehdot ja aloita käyttöönotto valitsemalla **Kyllä**.

   Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä muutaman minuutin. Jos valmisteluprosessi epäonnistuu, ota yhteys tukeen.

7. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Human Resourcesiin**.

    > [!NOTE]
    > Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Human Resourcesin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

    > Kannattaa harkita maksuttoman 60 päivän [Human Resources -kokeiluympäristön](https://go.microsoft.com/fwlink/p/?LinkId=2115962) käyttöä. Vaikka kokeiluympäristön pyytänyt käyttäjä omistaa ympäristön, muita käyttäjiä voidaan kutsua henkilöstöhallinnon järjestelmänhallintakokemuksen kautta. Kokeiluympäristössä on kuvitteellisia tietoja, joiden avulla ohjelmaan voi tutustua turvallisesti. Niitä ei ole tarkoitettu käytettäväksi tuotantoympäristöinä. Huomaa, että kun kokeiluympäristö vanhenee 60 päivän kuluttua, sen kaikki tiedot poistetaan eikä niitä voi palauttaa. Voit rekisteröidä uuden kokeiluympäristön, kun aiemmin luotu ympäristö vanhenee.

## <a name="select-a-power-apps-environment"></a>Valitse Power Apps-ympäristö

Voit integroida henkilöstöhallinnon tiedot ja laajentaa niiden käyttöä Power Apps -työkalujen avulla. Lisätietoja Power Apps-ympäristöistä, kuten ympäristön laajuudesta, ympäristön käytöstä sekä ympäristön luomisesta ja valitsemisesta, on kohdassa [Power Apps-ympäristöjen julkaiseminen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Määritä seuraavien ohjeiden avulla, missä Power Apps-ympäristössä Human Resources otetaan käyttöön: 

1. Valitse LCS:ssä **Hallitse ympäristöjä**. Voit myös siirtyä suoraan Power Apps -hallintakeskukseen, jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia.

2. Yksittäinen Human Resources -ympäristö yhdistetään yksittäiseen Power Apps-ympäristöön.

3. Power Apps-ympäristö sisältää Human Resources -sovelluksen sekä vastaavat Power Apps-, Power Automate- ja Common Data Service -sovellukset. Jos Power Apps-ympäristö poistetaan, myös sen sovellukset poistetaan. Human Resources -ympäristöä valmisteltaessa voit valmistella joko **kokeilu**- tai **tuotanto**ympäristön. Valitse ympäristön tyyppi ympäristön käyttötavan perusteella. 

4. Tietojen integrointi- ja testausstrategiat kannattaa ottaa huomioon, esimerkiksi Sandbox, hyväksyntätestaus ja tuotanto. On suositeltavaa pohtia, mitä vaikutuksia käyttöönotolla on, koska on hankala muuttaa Power Apps-ympäristöön yhdistettyä Human Resources -ympäristöä.

5. Seuraavia Power Apps -ympäristöjä ei voi käyttää henkilöstöhallinnossa. Ne suodatetaan LCS:n valintaluettelosta:
 
    - **Power Appsin oletusympäristöt** – Kun jokainen vuokralainen on automaattisesti varustettu Power Apps -oletusympäristöllä, emme suosittele niiden käyttämistä henkilöstöresurssien kanssa. Kaikki vuokralaisen käyttäjät voivat käyttää Power Apps -ympäristöä ja vioittaa tuotantotietoja tahattomasti testattaessa ja tarkasteltaessa Power Apps- tai Power Automate -integrointia.
   
    - **Kokeiluympäristöt** - Näille ympäristöille luodaan vanhentumispäivä. Kun voimassaolo päättyy, ympäristösi ja sen sisältämät henkilöstöresurssien esiintymät poistetaan automaattisesti.
   
    - **Alueet, joita ei tueta** – Tällä hetkellä Human Resourcesia tuetaan vain seuraavilla alueilla: Yhdysvallat, Eurooppa, Iso-Britannia, Australia, Kanada ja Aasia.

    > [!NOTE]
    > Human Resources -ympäristö valmistellaan samalla alueella, jolla Power Apps -ympäristö on valmisteltu. Human Resources -ympäristön siirtämistä toiselle alueelle ei tueta.

6. Kun olet määrittänyt oikean ympäristön, voit jatkaa valmisteluprosessia. 
 
## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen

Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Käyttöoikeus on myönnettävä sovelluksen muille käyttäjille erikseen. Sinun on lisättävä käyttäjiä ja määritettävä heille sopivat roolit henkilöstöhallintoympäristössä. Human Resourcesin käyttöönoton tehneen yleisen järjestelmänvalvojan on käynnistettävä sekä Attract että Onboard alustuksen suorittamiseksi ja muiden vuokraajakäyttäjien pääsyn sallimiseksi. Kunnes näin tapahtuu, muut käyttäjät eivät voi käyttää Attractia ja Onboardia, vaan ne näyttävät käyttöoikeusvirheitä. Lisätietoja on kohdassa [Uusien käyttäjien luonti](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Käyttäjien liittäminen käyttöoikeusrooleihin](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
