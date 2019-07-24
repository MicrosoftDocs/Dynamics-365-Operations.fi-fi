---
title: Talentin valmistelu
description: Tässä ohjeaiheessa kerrotaan Dynamics 365 for Talentin uuden ympäristön valmisteluprosessista.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: c249df697553cd42eccd59d3f2c3f5f083ead1cb
ms.sourcegitcommit: 15154b0aa86110ce5fad6f63e6763103a676a1d2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624604"
---
# <a name="provision-talent"></a>Talentin valmistelu

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Dynamics 365 for Talentin uuden tuotantoympäristön valmisteluprosessista. Ohjeaiheessa oletetaan, että olet ostanut Talent-sovelluksen pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla. Jos sinulla on Microsoft Dynamics 365 -käyttöoikeus, joka sisältää Talent-palvelusopimuksen, etkä pysty suorittamaan tämän ohjeaiheen vaiheita, ota yhteys tukeen.

Aluksi yleisen järjestelmänvalvojan tulee kirjautua [Microsoft Dynamics Lifecycle Servicesiin](https://lcs.dynamics.com) (LCS) ja luoda uusi Talent-projekti. Jos Talentin käyttämistä estävä ongelma ei liity käyttöoikeuteen, tuen tai Dynamics-palvelun kehityspalvelun edustajien apua ei tarvita.

## <a name="create-an-lcs-project"></a>LCS-projektin luominen
Luo ensin LCS-projekti, jotta voit hallinnoida Talent-ympäristöjä LCS:n avulla.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index) samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.
2. Luo projekti valitsemalla plusmerkki (**+**).
3. Valitse tuotteen nimeksi ja versioksi **Microsoft Dynamics 365 for Talent**.
4. Valitse **Dynamics 365 for Talent** -menetelmä.
5. Valitse **Luo**.

Lisätietoja Talent-sovelluksen aloittamisesta on uudelle projektille luomassasi **Talent**-metodologiassa. Kun projekti on valmis, noudata seuraavia ohjeita ja valmistele Talent-ympäristö.

## <a name="provision-a-talent-project"></a>Talent-projektin valmisteleminen
Kun LCS-projekti on luotu, voit valmistella Talent-sovelluksen ympäristöä varten.

1. Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.
2. Määritä, onko tämä Sandbox vai Talentin tuotantoesiintymä. Varhaisia esikatselutoimintoja voi olla käytettävissä Sandbox-esiintymissä, jotta varhainen palaute ja testaaminen olisi mahdollista. 
    > [!NOTE]
    > Talent-esiintymätyyppi on erillään PowerApps-ympäristön esiintymätyypistä, joka määritetään PowerAppsin hallintakeskuksesta.
3. Valitse **Sisällytä esittelytiedot** -vaihtoehto, jos haluat ympäristösi sisältävän saman esittelytietojoukon, jota käytetään Talent Test Drive -kokemuksessa. Tämä on hyödyllistä pitkän aikavälin esittely- tai koulutusympäristöissä, eikä sitä tule koskaan käyttää tuotantoympäristöissä.  Huomaa, että tämä asetus on valittava ensimmäisen käyttöönoton yhteydessä. Et voi päivittää aiemmin luotua käyttöönottoa myöhemmin.
4. Talent valmistellaan aina Microsoft PowerApps -ympäristössä, jotta PowerApps-integrointi ja laajennettavuus voidaan ottaa käyttöön. Lue tämän ohjeaiheen PowerApps-ympäristön valitseminen -osa, ennen kuin jatkat. Jos sinulla ei vielä ole PowerApps-ympäristöä, valitse Hallitse ympäristöjä LCS:ssä tai siirry PowerAppsin hallintakeskukseen. Noudata kohdan [PowerApps-ympäristön luominen](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment) ohjeita.

    > [!NOTE]
    > Voit tarkastella aiemmin luotuja ympäristöja tai luoda uusia ympäristöjä, kun Talent-sovelluksen valmistelevalle vuokraajan järjestelmänvalvojalle on määritetty PowerApps P2 -käyttöoikeus. Jos organisaatiolla ei ole PowerApps P2 -käyttöoikeutta, voit hankkia sen pilvipalveluratkaisujen toimittajalta tai [PowerApps-hinnoittelusivulta](https://powerapps.microsoft.com/en-us/pricing/).

5. Valitse ympäristö, johon Talent sisällytetään.
6. Hyväksy ehdot ja aloita käyttöönotto valitsemalla **Kyllä**.

    Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä muutaman minuutin. Jos valmisteluprosessi epäonnistuu, ota yhteys tukeen.

7. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Talentiin**.

    > [!NOTE]
    > Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Talentin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

    > Koska Talent-tilaukseen sallitaan vain kaksi LCS-ympäristöä, voit hyödyntää myös ilmaisen 60 päivän [Talent-kokeiluympäristön](https://dynamics.microsoft.com/en-us/talent/overview/). Vaikka kokeiluympäristön pyytänyt käyttäjä omistaa ympäristön, muita käyttäjiä voidaan kutsua henkilöstöhallinnon perusversion järjestelmänhallintakokemuksen kautta. Kokeiluympäristössä on kuvitteellisia tietoja, joiden avulla ohjelmaan voi tutustua turvallisesti. Niitä ei ole tarkoitettu käytettäväksi tuotantoympäristöinä. Huomaa, että kun kokeiluympäristö vanhenee 60 päivän kuluttua, sen kaikki tiedot poistetaan eikä niitä voi palauttaa. Voit rekisteröidä uuden kokeiluympäristön, kun aiemmin luotu ympäristö vanhenee.

## <a name="select-a-powerapps-environment"></a>PowerApps-ympäristön valinta

Talent- ja PowerApps-ympäristöjen välinen integrointi sallii Talent-tietojen integroinnin ja käytön laajentamisen PowerApps-työkaluilla. PowerApps-ympäristöjen tarkoituksen ymmärtäminen auttaa sekä laajentamaan Talentia sovelluksia muodostamalla että valitsemaan oikean ympäristön Talentia valmisteltaessa. Lisätietoja PowerApps-ympäristöistä, kuten ympäristön laajuudesta, ympäristön käytöstä sekä ympäristön luomisesta ja valitsemisesta, on kohdassa [PowerApps-ympäristöjen julkaiseminen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Määritä seuraavien ohjeiden avulla, missä PowerApps-ympäristössä Talent otetaan käyttöön: 

1. Valitse LCS-sovelluksessa **Ympäristöjen hallinta** tai siirry suoraan PowerApps-hallintakeskukseen, jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia ympäristöjä.
2. Yksittäinen Talent-ympäristö yhdistetään yksittäiseen PowerApps-ympäristöön.
3. PowerApps-ympäristö sisältää Talent-sovelluksen sekä vastaavat PowerApps-, Flow- ja Common Data Service -sovellukset. Jos PowerApps-ympäristö poistetaan, myös sen sovellukset poistetaan. Talent-ympäristöä valmisteltaessa voidaan valmistella joko kokeilu- tai tuotantoympäristö. Valitse ympäristön tyyppi ympäristön käyttötavan perusteella. 
4. Tietojen integrointi- ja testausstrategiat kannattaa ottaa huomioon, esimerkiksi Sandbox, hyväksyntätestaus ja tuotanto. On suositeltavaa pohtia, mitä vaikutuksia käyttöönotolla on, koska myöhemmin on hankala muuttaa PowerApps-ympäristöön yhdistettyä Talent-ympäristöä.
5. Seuraavia PowerApps-ympäristöjä ei voi käyttää Talentissa, ja ne suodatetaan valintaluetteloista LCS:ssä:
 
    - **PowerApps-oletusympäristöt** Vaikka jokainen vuokraaja valmistellaan automaattisesti PowerApps-oletusympäristössä, se ei välttämättä ole paras ympäristö Talent-sovelluksen käyttöönottoa varten, koska kaikilla vuokraajakäyttäjillä on PowerApps-ympäristön käyttöoikeus. Tuotantoympäristön tietoja voi vioittua epähuomiossa PowerApps- tai Flow-integrointien testaamisen ja tutkimisen yhteydessä.
   
    - **Kokeiluympäristöt** – Näitä ympäristöjä luotaessa määritetään voimassaolon päättymispäivämäärä. Tämän jälkeen ympäristö vanhenee ja kaikki ympäristön Talent-esiintymät poistetaan automaattisesti.
   
    - **Alueet, joita ei tueta** – Tällä hetkellä Talent-sovelluksella on tuki vain seuraavilla alueilla: Yhdysvallat, Eurooppa, Yhdistynyt kuningaskunta ja Australia.
  
6. Kun olet määrittänyt oikean ympäristön, voit jatkaa valmisteluprosessia. 
 
## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen
Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Sovelluksen muille käyttäjille käyttöoikeus on myönnettävä erikseen. Voit myöntää käyttöoikeuden lisäämällä käyttäjiä ja määrittämällä heille sopivat roolit Core HR -ympäristössä. Talentin käyttöönoton tehneen yleisen järjestelmänvalvojan on käynnistettävä sekä Attract- että Onboard-sovellukset alustuksen suorittamiseksi ja muiden vuokraajakäyttäjien pääsyn sallimiseksi.  Kunnes näin tapahtuu, muut käyttäjät eivät voi käyttää Attract- ja Onboard-sovelluksia, vaan ne näyttävät käyttöoikeusvirheitä. Lisätietoja on kohdassa [Uusien käyttäjien luonti](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Käyttäjien liittäminen käyttöoikeusrooleihin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
