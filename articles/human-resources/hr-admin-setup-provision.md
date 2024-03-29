---
title: Valmistele Human Resources
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmisteluprosessista.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc44b52e2f7662fc6be609562cec903a8755d1b
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178500"
---
# <a name="provision-human-resources"></a>Valmistele Human Resources

_**Kohde:** Human Resources itsenäisessä infrastruktuurissa_ 

> [!NOTE]
> Kesäkuusta 2022 alkaen Human Resources -ympäristöt voidaan käyttöön vain talous- ja toimintosovellusinfrastruktuurissa. Lisätietoja kohdassa [Human Resourcesin valmisteleminen talous- ja toimintosovellusinfrastruktuurissa](hr-admin-setup-provision-fo.md).

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uuden tuotantoympäristön valmisteluprosessista. 

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on toteuduttava, ennen kuin tuotantoympäristön valmistelu voidaan aloittaa:

- Human Resources on ostettu pilvipalveluratkaisujen toimittajalta (CSP) tai yritysarkkitehtuurisopimuksen (EA) avulla. Jos sinulla on Microsoft Dynamics 365 -käyttöoikeus, joka sisältää Human Resourcesin palvelusopimuksen, etkä pysty suorittamaan tämän artikkelin vaiheita, ota yhteys tukeen.

- Yleinen järjestelmänvalvoja on kirjautunut [Microsoft Dynamics Lifecycle Servicesiin](https://lcs.dynamics.com) (LCS) ja luonut uuden Human Resources -projekti. 

## <a name="provision-a-human-resources-trial-environment"></a>Henkilöstöhallinnon koeympäristön valmistelu

>[!NOTE]
> Human Resourcesin koeympäristöt eivät ole käytettävissä itsenäisissä sovelluksissa huhtikuussa 2022. Mahdolliset asiakkaat, jotka haluavat arvioida Human Resourcesin ominaisuuksia talous- ja toimintosovellusten avulla, voivat käyttää ilmaista 30 päivän kokeiluversiota ja esittelytietoja. Dynamics 365 Finance sisältää Human Resources -ominaisuudet, jotka tuodaan Finance-infrastruktuuriin yhdistäen itsenäisen sovelluksen. Lisätietoja on kohdassa [HR-tuotteiden yhdistäminen tuo ominaisuudet samaan paikkaan asiakkaalle](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Lisätietoja Dynamics 365 Finance -kokeiluversioista on vaiheittaisessa [oppaassa](../fin-ops-core/fin-ops/get-started/before-you-buy.md). 


Ennen ensimmäisen tuotantoympäristön tai tuotantoympäristön varausta voit varata [henkilöstöhallinnon koeympäristön](https://go.microsoft.com/fwlink/p/?LinkId=2115962) henkilöstöhallinnon toimintojen tarkistamista varten. Kokeiluympäristössä on kuvitteellisia tietoja, joiden avulla ohjelmaan voi tutustua turvallisesti. Vaikka kokeiluympäristön pyytänyt käyttäjä omistaa ympäristön, muita käyttäjiä voidaan kutsua henkilöstöhallinnon järjestelmänhallintakokemuksen kautta. 

Kokeiluympäristöt helpottavat henkilönhallintatoimintojen arviointia niiden henkilöiden osalta, joilla ei ole vielä Human Resources -ympäristön käyttöoikeutta. Jos olet valmistelemassa koeympäristöä ja todennetulla käyttäjällä on jo käyttöoikeus yhteen tai useampaan olemassa olevaan henkilöstöresurssiympäristöön, käyttäjä ohjataan aiemmin luotuun ympäristöön tai ympäristöjen luetteloon.

Koeympäristöjä ei ole tarkoitettu käytettäväksi tuotantoympäristöinä. Koeajan kesto on enintään 30 päivää. Kun kokeiluympäristö vanhenee, ympäristö ja sen kaikki tiedot poistetaan, eikä niitä voi palauttaa. Ympäristöä ei voi muuntaa eristys- tai tuotantoympäristöksi. Voit rekisteröidä uuden kokeiluympäristön, kun aiemmin luotu ympäristö vanhenee.

Kun luot henkilöstöhallinnon koeympäristön, vuokraajalla luodaan myös Power Apps -koeympäristö, joka linkitetään henkilöstöhallinnon ympäristöön. Power Apps -ympäristöllä, jonka nimi on TestDrive, on sama koeaika kuin henkilöstöhallinnon ympäristöllä.

> [!NOTE]
> Henkilöstöhallinnon koeympäristön valmistelu epäonnistuu, jos varmennetulla käyttäjällä ei ole oikeutta luoda Power Apps -koeympäristöjä. Käyttäjän on kuuluttava käyttäjäryhmään, joka voi luoda koeympäristöjä Power Platformin hallintakeskuksessa. Lisätietoja [Hallitse sitä, kuka voi luoda ja hallita ympäristöjä Power Platformin hallintakeskuksessa](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Human Resources -ympäristöjen suunnitteleminen

Ennen ensimmäisen Human Resources -ympäristön luontia sinun tulee suunnitella huolellisesti projektin ympäristötarpeet. Human Resourcesin perustilaus sisältää kaksi ympäristöä: tuotantoympäristön ja eristysympäristön. Projektin monimutkaisuuden mukaan projektitoimintojen tueksi voi olla tarpeen ostaa lisäeristysympäristöjä. 

Lisäympäristöjä koskevia lisähuomioita:

- **Tietojen siirto**; Tietojen siirtämisen avulla eristysympäristöä voidaan käyttää testaustarkoituksiin koko projektin ajan. Lisäympäristön ansiosta tietojen siirtotoiminnot voivat jatkua, kun testaus- ja konfigurointitoiminnot tapahtuvat samanaikaisesti toisessa ympäristössä.
- **Integrointi**: Integrointien määrittäminen ja testaus voi koskea alkuperäisiä integrointeja, kuten Ceridian Dayforcea, tai mukautettuja integrointeja.
- **Koulutus**: työntekijöiden kouluttaminen uuden järjestelmän käyttäjäksi voi edellyttää erillistä ympäristönä, jossa on käytössä koulutustietojoukko. 
- **Monivaiheinen projekti**: määritysten, tietosiirtämisen, testauksen tai muiden aktiviteettien tukeminen projektin siinä vaiheessa, joka on tarkoitus suorittaa projektin ensimmäisen julkaisun jälkeen.

 > [!IMPORTANT]
 > Ympäristöä harkittaessa kannattaa ottaa seuraavat huomioon:
 > - Käytä tuotantoympäristöä koko projektin ajan GOLD-määritysympäristönä. Tämä on tärkeää, koska et voi kopioida eristysympäristöä tuotantoympäristöön. Kun siis julkaiset ratkaisun, GOLD-ympäristösi on tuotantoympäristösi, ja sinun tulee suorittaa käyttöönotto tässä ympäristössä.</br></br>
 > - Käytä eristysympäristöä tai muuta ympäristöä harjoittelemaan käyttöönottoa ennen julkaisua. Voit tehdä tämän päivittämällä tuotantoympäristön GOLD-konfiguraatiolla eristysympäristöön.</br></br>
 > - Käytä yksityiskohtaista käyttöönoton tarkistusluetteloa. Tämä luettelo sisältää kaikki tietopaketit, joita tarvitaan lopullisten tietojen siirtämiseen tuotantoympäristöön siirtymisprosessin aikana.</br></br>
 > - Käytä eristysympäristöä koko projektin ajan TEST-määritysympäristönä. Jos tarvitset lisää ympäristöjä, organisaatiosi voi ostaa niitä lisäkustannuksilla.</br></br>

## <a name="create-an-lcs-project"></a>LCS-projektin luominen

Luo ensin LCS-projekti, jotta voit hallinnoida Human Resources -ympäristöjä LCS:n avulla.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.

   > [!NOTE]
   > Onnistuneen valmistelun varmistamiseksi Human Resources -ympäristön valmisteluun käytetyn tilin on oltava määritettynä joko **Järjestelmänvalvoja**- tai **Järjestelmän mukauttaja** -roolille Power Apps -ympäristössä, joka liittyy Human Resources -ympäristöön. Lisätietoja käyttöoikeusroolien määrittämisestä käyttäjille Power Platformissa: [Käyttöoikeuksien määritys resursseille](/power-platform/admin/database-security).

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
    > Human Resources -esiintymätyyppiä ei voi muuttaa, kun se on määritetty. Tarkista, että oikea ilmentymätyyppi on valittuna, ennen kuin jatkat.</br></br>
    > Human Resources -esiintymätyyppi on erillään Microsoft Power Apps-ympäristön esiintymätyypistä, jonka määrität Power Apps-hallintakeskuksesta.
    
3. Valitse **Sisällytä esittelytiedot** -vaihtoehto, jos haluat ympäristön sisältävän saman esittelytietojoukon, jota käytetään Human Resources -kokeiluympäristönä. Esittelytiedot ovat hyödyllisiä pitkän aikavälin esittely- tai koulutusympäristöissä, eikä niitä tule koskaan käyttää tuotantoympäristöissä. Tämä asetus on valittava ensimmäisen käyttöönoton yhteydessä. Et voi päivittää aiemmin luotua käyttöönottoa myöhemmin.

4. Human Resources valmistellaan aina Microsoft Power Apps -ympäristössä, jotta Power Apps-integrointi ja laajennettavuus voidaan ottaa käyttöön. Lue tämän artikkelin ”Power Apps-ympäristön valitseminen” -osio ennen kuin jatkat. Jos sinulla ei vielä ole Power Apps-ympäristöä, valitse Hallitse ympäristöjä LCS:ssä tai siirry Power Apps-hallintakeskukseen. Noudata kohdan [Power Apps-ympäristön luominen](/powerapps/administrator/create-environment) ohjeita.

5. Valitse ympäristö, johon Human Resources sisällytetään.

6. Hyväksy ehdot ja aloita käyttöönotto valitsemalla **Kyllä**.

   Uusi ympäristö näkyy ympäristöluettelossa vasemmassa siirtymisruudussa. Voit kuitenkin alkaa käyttää ympäristöä vasta, kun käyttöönoton tilaksi on päivitetty **Otettu käyttöön**. Tämä prosessi kestää yleensä muutaman minuutin. Jos valmisteluprosessi epäonnistuu, ota yhteys tukeen.

7. Voit käyttää uutta ympäristöä valitsemalla **Kirjaudu Human Resourcesiin**.

    > [!NOTE]
    > Jos et ole vielä hyväksynyt lopullisia vaatimuksia, voit ottaa projektissa käyttöön Human Resourcesin testausesiintymän. Voit testata esiintymässä ratkaisuasi siihen asti, että hyväksyntä on tehty. Jos käytät uutta ympäristöä testaukseen, nämä menettelytavat on toistettava tuotantoympäristön luomista varten.

## <a name="select-a-power-apps-environment"></a>Valitse Power Apps-ympäristö

Voit integroida henkilöstöhallinnon tiedot ja laajentaa niiden käyttöä Power Apps -työkalujen avulla. Lisätietoja Power Apps-ympäristöistä, kuten ympäristön laajuudesta, ympäristön käytöstä sekä ympäristön luomisesta ja valitsemisesta, on kohdassa [Power Apps-ympäristöjen julkaiseminen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Määritä seuraavien ohjeiden avulla, missä Power Apps-ympäristössä Human Resources otetaan käyttöön: 

1. Valitse LCS:ssä **Hallitse ympäristöjä**. Voit myös siirtyä suoraan Power Apps -hallintakeskukseen, jossa voit tarkastella aiemmin luotuja ympäristöjä ja luoda uusia.

2. Yksittäinen Human Resources -ympäristö yhdistetään yksittäiseen Power Apps-ympäristöön.

3. Power Apps-ympäristö sisältää Human Resources -sovelluksen sekä vastaavat Power Apps-, Power Automate- ja Dataverse -sovellukset. Jos Power Apps-ympäristö poistetaan, myös sen sovellukset poistetaan. Human Resources -ympäristöä valmisteltaessa voit valmistella joko **kokeilu**- tai **tuotanto** ympäristön. Valitse ympäristön tyyppi ympäristön käyttötavan perusteella. 

4. Tietojen integrointi- ja testausstrategiat kannattaa ottaa huomioon, esimerkiksi Sandbox, hyväksyntätestaus ja tuotanto. On suositeltavaa pohtia, mitä vaikutuksia käyttöönotolla on, koska on hankala muuttaa Power Apps-ympäristöön yhdistettyä Human Resources -ympäristöä.

5. Human Resources ei voi hyödyntää seuraavia Power Apps -ympäristöjä. Ne suodatetaan LCS:n valintaluettelosta:
 
    - **Power Appsin oletusympäristöt** – Kun jokainen vuokralainen on automaattisesti varustettu Power Apps -oletusympäristöllä, emme suosittele niiden käyttämistä henkilöstöresurssien kanssa. Kaikki vuokralaisen käyttäjät voivat käyttää Power Apps -ympäristöä ja vioittaa tuotantotietoja tahattomasti testattaessa ja tarkasteltaessa Power Apps- tai Power Automate -integrointia.
   
    - **Kokeiluympäristöt** - Näille ympäristöille luodaan vanhentumispäivä. Kun voimassaolo päättyy, ympäristösi ja sen sisältämät henkilöstöresurssien esiintymät poistetaan automaattisesti.
   
    - **Maantieteelliset alueet, joita ei tueta** - Ympäristön on oltava tuetulla maantieteellisellä alueella. Lisätietoja on kohdassa [Tuetut maantieteelliset alueet](hr-admin-setup-provision.md#supported-geographies).

6. Kaksoiskirjoitustoimintoa voidaan käyttää henkilöstötietojen integroimiseen Power Apps -ympäristön kanssa vain, jos **Ota käyttöön Dynamics 365 -sovellukset** -vaihtoehto on valittu ympäristölle. Lisätietoja on kohdassa [Kaksoiskirjoituksen aloitussivu](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md).

    > [!NOTE]
    > **Ota käyttöön Dynamics 365 -sovellukset** -vaihtoehdon on oltava valittuna sillä hetkellä, kun Power Apps -ympäristö luodaan. Jos vaihtoehto ei ole valittuna valmistelun aikana, et voi käyttää kaksoiskirjoitusta integroidaksesi tietoja Dynamics 365 Human Resourcesin ja Power Apps -ympäristön välillä, etkä voi asentaa Dynamics 365 -sovelluksia (kuten Dynamics 365 Sales, Field Service) ympäristöön. Tätä vaihtoehtoa ei voi perua. 
    > -  Human Resources ei tue linkitetyn Dataverse-esiintymän muuttamista sen jälkeen, kun Human Resources on otettu käyttöön esiintymässä. </br></br>
    > Lisätietoja löytyy kohdasta [Huomioon otettavia asioita uutta ympäristöä luotaessa](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) Power Platform -ohjesivustolla.  

7. Kun olet määrittänyt oikean ympäristön, voit jatkaa valmisteluprosessia. 

### <a name="supported-geographies"></a>Tuetut maantieteelliset alueet

Human Resources tukee tällä hetkellä seuraavia maantieteellisiä alueita:

- Yhdysvallat
- Eurooppa
- Iso-Britannia
- Australia
- Kanada
- Aasia 

Kun luot Human Resources -ympäristön, valitset Power Apps -ympäristön, joka liitetään Human Resources -ympäristöön. Human Resources -ympäristö valmistellaan tämän jälkeen samaan Azuren maantieteelliseen alueeseen kuin valittu Power Apps -ympäristö. Voit valita, missä Human Resources -ympäristö ja tietokanta sijaitsevat fyysisesti valitsemalla maantieteellisen alueen, kun luot Human Resources -ympäristöön liittyvää Power Apps -ympäristöä.

Voit valita Azuren *maantieteellisen alueen*, johon ympäristö valmistellaan, mutta et voi valita tiettyä Azuren *aluetta*. Automaatio määrittää tietyn alueen maantieteellisell alueella, jossa ympäristö luodaan kuormituksen tasaamisen ja suorituskyvyn optimoimiseksi. Tietoa Azuren maantieteellisistä alueista ja alueista on dokumentaatiossa [Azuren maantieteelliset alueet](https://azure.microsoft.com/global-infrastructure/geographies).

Human Resources -ympäristön tiedot sisältyvät aina siihen Azuren maantieteelliseen alueeseen, jossa se luotiin. Se ei kuitenkaan aina sisälly samaan Azure-alueeseen. Järjestelmäpalautusta varten tiedot replikoidaan sekä ensisijaisella Azure-alueella että toissijaisella vikasietoalueella maantieteellisellä alueella.

 > [!NOTE]
 > Human Resources -ympäristön siirtämistä yhdeltä Azure-alueelta toiselle ei tueta.

## <a name="grant-access-to-the-environment"></a>Ympäristön käyttöoikeuksien myöntäminen

Oletusarvoisesti vain ympäristön luonut yleinen järjestelmänvalvoja voi käyttää sitä. Käyttöoikeus on myönnettävä sovelluksen muille käyttäjille erikseen. Sinun on lisättävä käyttäjiä ja määritettävä heille sopivat roolit henkilöstöhallintoympäristössä. Lisätietoja on kohdassa [Uusien käyttäjien luonti](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Käyttäjien liittäminen käyttöoikeusrooleihin](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

