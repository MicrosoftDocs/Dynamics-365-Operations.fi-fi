---
title: Talentin valmistelu
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
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 2fc4119f3b33aa583274f4d823e296752cdde41d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="provision-talent"></a>Talentin valmistelu

[!include [banner](includes/banner.md)]

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
2. Talent valmistellaan aina Microsoft PowerApps -ympäristössä, jotta PowerApps-integrointi ja laajennus saadaan käyttöön. Lue tämän ohjeaiheen PowerApps-ympäristön valitseminen -osa, ennen kuin jatkat. 
3. Jos PowerApps-ympäristö ei ole käytössä, seuraa tämän ohjeaiheen Uuden PowerApps-ympäristön luominen (tarvittaessa) -osan vaiheita, ennen kuin jatkat.

    > [!NOTE]
    > Voit tarkastella aiemmin luotuja ympäristöja tai luoda uusia ympäristöjä, kun Talent-sovelluksen valmistelevalle vuokraajan järjestelmänvalvojalle on määritetty PowerApps P2 -käyttöoikeus. Jos organisaatiolla ei ole PowerApps P2 -käyttöoikeutta, voit hankkia sen pilvipalveluratkaisujen toimittajalta tai [PowerApps-hinnoittelusivulta](https://powerapps.microsoft.com/en-us/pricing/).

4. Valitse **Add** ja valitse sitten Talentiin valmisteltava ympäristö.
5. Valitse Sisällytä esittelytiedot -vaihtoehto, jos haluat ympäristösi sisältävän saman esittelytietojoukon, jota käytetään Talent Test Drive -kokemuksessa.  Tämä on hyödyllistä pitkän aikavälin esittely- tai koulutusympäristöissä, eikä sitä tule koskaan käyttää tuotantoympäristöissä.  Huomaa, että sinun on valittava tämä vaihtoehto ensimmäisen käyttöönoton yhteydessä etkä voi päivittää nykyistä käyttöönottoa myöhemmin.
6. Hyväksy ehdot ja aloita käyttöönotto valitsemalla **Kyllä**.

    Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä vain muutaman minuutin. Jos valmisteluprosessi epäonnistuu, ota yhteys tukeen.

7. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Talentiin**.

> [!NOTE]
> Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Talentin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

> [!NOTE]
> Koska Talent-tilaukseen sallitaan vain kaksi LCS-ympäristöä, voit hyödyntää myös ilmaisen 60 päivän [Talent-kokeiluympäristön](https://dynamics.microsoft.com/en-us/talent/overview/). Vaikka kokeiluympäristön pyytänyt käyttäjä omistaa ympäristön, muita käyttäjiä voidaan kutsua henkilöstöhallinnon perusversion järjestelmänhallintakokemuksen kautta. Kokeiluympäristössä on kuvitteellisia tietoja, joiden avulla ohjelmaan voi tutustua turvallisesti. Niitä ei ole tarkoitettu käytettäväksi tuotantoympäristöinä. Huomaa, että kun kokeiluympäristö vanhenee 60 päivän kuluttua, sen kaikki tiedot poistetaan eikä niitä voi palauttaa. Voit rekisteröidä uuden kokeiluympäristön, kun aiemmin luotu ympäristö vanhenee.

## <a name="select-a-powerapps-environment"></a>PowerApps-ympäristön valinta

Talent- ja PowerApps-ympäristöjen välinen integrointi sallii Talent-tietojen integroinnin ja käytön laajentamisen PowerApps-työkaluilla. PowerApps-ympäristöjen tarkoituksen ymmärtäminen auttaa sekä laajentamaan Talentia sovelluksia muodostamalla että valitsemaan oikean ympäristön Talentia valmisteltaessa. Lisätietoja PowerApps-ympäristöistä, kuten ympäristön laajuudesta, ympäristön käytöstä sekä ympäristön luomisesta ja valitsemisesta, on kohdassa [PowerApps-ympäristöjen julkaiseminen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Määritä seuraavien ohjeiden avulla, missä PowerApps-ympäristössä Talent otetaan käyttöön: 
1. Valitse LCS-sovelluksessa Ympäristöjen hallinta tai siirry suoraan PowerApps-hallintakeskukseen, jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia ympäristöjä.
2. Yksittäinen Talent-ympäristö yhdistetään yksittäiseen PowerApps-ympäristöön.
3. PowerApps-ympäristö sisältää Talent-sovelluksen sekä vastaavat PowerApps-, Flow- ja CDS-sovellukset. Jos PowerApps-ympäristö poistetaan, myös sen sovellukset poistetaan.
4. Tietojen integrointi- ja testausstrategiat kannattaa ottaa huomioon. Esimerkit: Sandbox, hyväksyntätestaus, tuotanto. Tämän vuoksi on pohdittava, mitä vaikutuksia käyttöönotolla on, koska myöhemmin on hankala muuttaa PowerApps-ympäristöön yhdistettyä Talent-ympäristöä.
5. Seuraavia PowerApps-ympäristöjä ei voi käyttää Talentissa, ja ne suodatetaan valintaluetteloista LCS:ssä:
 
    **CDS 2.0 -ympäristöt** CDS 2.0 on saatavana 21.3.2018. Talent ei kuitenkaan vielä tue CDS 2.0 -ympäristöä. Vaikka voit katsella ja luoda CDS 2.0 -tietokantoja PowerAppsin hallintakeskuksessa, niitä ei voi käyttää Talentissa. CDS 2.0 -ympäristöjen käyttö Talent-käyttöönotoissa tulee mahdolliseksi myöhemmin.
   
   > [!Note]
   > Voit erottaa CDS 1.0- ja 2.0-ympäristöt toisiinsa hallintaportaalissa valitsemalla ympäristön ja tarkastelemalla **tietoja**. CDS 2.0 -ympäristöissä kaikki viittaa siihen, että asetuksia voi hallita Dynamics 365:n hallintakeskuksessa, käytössä on esiintymän versio eikä Tietokanta-välilehteä ole. 
 
   **PowerApps-oletusympäristöt** Vaikka jokainen vuokraaja valmistellaan automaattisesti PowerApps-oletusympäristössä, se ei välttämättä ole paras ympäristö Talent-sovelluksen käyttöönottoa varten, koska kaikilla vuokraajakäyttäjillä on PowerApps-ympäristön käyttöoikeus. Tuotantoympäristön tietoja voi vioittua epähuomiossa PowerApps- tai Flow-integrointien testaamisen ja tutkimisen yhteydessä.
   
   <strong>Testaa ympäristöt</strong> Ympäristöillä, joilla on TestDrive – alias@domain -tyyppinen nimi, on 60 päivän pituinen voimassaolon päättymiskausi. Tämän jälkeen ympäristö vanhenee ja se poistetaan automaattisesti.
   
   **Alueet, joita ei tueta** Tällä hetkellä Talent-sovelluksella on tuki vain seuraavilla alueilla: Yhdysvallat, Eurooppa ja Australia.
  
6. Mitään tiettyä toimintoa ei tarvitse tehdä sen jälkeen, kun olet määrittänyt oikean käytettävän ympäristön. Jatka varausprosessia. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Uuden PowerApps-ympäristön luominen (tarvittaessa)

Suorita PowerShell-komentosarja, kun haluat luoda uuden PowerApps-ympäristön Talent-sovelluksessa sellaisen vuokraajan järjestelmänvalvojalle, jolla on PowerApps -palvelupaketin 2 käyttöoikeus. Komentosarja automatisoi seuraavat vaiheet:


 + PowerApps-ympäristön luominen
 + CDS 1.0 -tietokannan luominen
 + CDS 1.0 -tietokannan kaikkien esimerkkitietojen tyhjennys


Täytä seuraavat komentosarjan suoritusta koskevat ohjeet:

1. Lataa ProvisionCDSEnvironment.zip-tiedosto seuraavasta sijainnista: [ProvisionCDSEnvironment-komentosarjat](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Napsauta hiiren kakkospainikkeella Lataukset-kansiossa olevaa ProvisionCDSEnvironment.zip-tiedostoa, jonka juuri latasit, ja valitse **Ominaisuudet**.  Jos valintaikkunan alareunassa näkyy suojausilmoitus "Tämä tiedosto on peräisin toisesta tietokoneesta, ja se on estetty tietokoneen suojaamiseksi", valitse **Salli**-valintaruutu ja napsauta sitten **Käytä** ja **OK**.

3. Pura ProvisionCDSEnvironment.zip-tiedoston koko sisältö kansioon, joka ei ole tietokoneen juurikansio.

4. Suorita Windows PowerShell- tai Windows PowerShell ISE -ohjelma järjestelmänvalvojana.

   Lisätietoja komentosarjojen suorittamisen sallivan suorituskäytännön määrittämisestä on kohdassa [Suorituskäytännön määrittäminen](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6). Suosittelemme, että käytät "Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process" -menetelmää, mutta noudata yrityksesi suojauskäytäntöjä ja sulje PowerShell-ikkuna toiminnon päätteeksi. 
  
5. Siirry PowerShellissä kansioon, johon purit tiedoston, ja suorita seuraavat komento korvaamalla arvot annettujen ohjeiden mukaan:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** korvataan ympäristön nimellä. Tämä nimi näkyy LCS:ssä ja tulee näkyviin, kun käyttäjät valitsevat käytettävän Talent-ympäristön. 

   **YourLocation** korvataan jollakin Talent-sovelluksen tuetun alueen arvolla: Yhdysvallat, Eurooppa tai Australia. 

   **-Yksityiskohtainen** on valinnainen. Sen avulla voit tuottaa yksityiskohtaisia tietoja ja lähettää ne mahdollisen ongelman tueksi.

6. Jatka varausprosessia.
 

## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen
Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Sovelluksen muille käyttäjille käyttöoikeus on myönnettävä erikseen. Voit myöntää käyttöoikeuden [lisäämällä käyttäjiä](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [määrittämällä heille sopivat roolit](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) henkilöstöhallinnon perusympäristössä.. Talentin käyttöönoton tehneen yleisen järjestelmänvalvojan on käynnistettävä sekä Attract- että Onboard-sovellukset alustuksen suorittamiseksi ja muiden vuokraajakäyttäjien pääsyn sallimiseksi.  Kunnes näin tapahtuu, muut käyttäjät eivät voi käyttää Attract- ja Onboard-sovelluksia, vaan ne näyttävät käyttöoikeusvirheitä.


