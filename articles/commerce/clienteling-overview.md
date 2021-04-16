---
title: Asiakashallinnan yleiskatsaus
description: Tässä ohjeaiheessa on myymäläsovellukseen sisältyvien uusienasiakashallinnan ominaisuuksien yleiskatsaus.
author: bebeale
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 8a809b81504fdc31d8f9e0529048269dd7e0c5cc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800444"
---
# <a name="clienteling-overview"></a>Asiakashallinnan yleiskuvaus

[!include [banner](includes/banner.md)]


Monet etenkin laadukkaiden erikoismyymälöiden jälleenmyyjät haluat, että myyjät muodostavat pitkäaikaisen asiakassuhteen avainasiakkaiden kanssa. Myyjien odotetaan tietävän, mistä nämä asiakkaat pitävät ja mistä eivät, minkälainen ostohistoria heillä on ja minkälaiset tuotemieltymyksensä ovat. Lisäksi myyjien odotetaan muistavan tärkeät päivämäärät, kuten vuosi- ja syntymäpäivät. Myyjät tarvitsevat paikan, johon he voivat tallentaa nämä tiedot ja josta ne löytyvät helposti tarvittaessa. Jos nämä tiedot ovat nähtävillä yhdellä silmäyksellä, myyjien on helppo kohdistaa myynti tietyt ehdot täyttäville asiakkaille. He voivat esimerkiksi etsiä kaikki asiakkaat, jotka ostavat mielellään käsilaukkuja, tai asiakkaat, joilla on tulossa tärkeä tapahtuma, kuten syntymä- tai vuosipäivä.

## <a name="client-book"></a>Asiakaskirja

Microsoft Dynamics 365 Commercen asiakaskirjatoiminnon avulla jälleenmyyjät voivat auttaa myymälän myyjiä muodostamaan pitkäaikaisia asiakassuhteita avainasiakkaiden kanssa.

Asiakaskirjassa on asiakaskortteja, joissa on kunkin asiakkaan yhteystiedot sekä kolme lisäparametria, jotka jälleenmyyjä määrittää Headquartersissa. Jälleenmyyjät voivat päättää, mitkä ovat kolme tärkeintä asiaa, jotka myyjien on tiedettävä asiakkaasta. Esimerkiksi kultasepänliikkeen kannattaa sisällyttää tärkeät päivämäärät, kuten merkkipäivät ja syntymäpäivät, koska ne ovat tapahtumia, jolloin asiakas voi olla kiinnostunut ostamaan koruja. Vastaavasti muotoliikkeessä kannattaa ehkä sisällyttää asiakasta kiinnostavat ostokset ja tuotemerkit.

Myyjät voivat käyttää asiakaskirjaa myös suodattamaan luetteloa siten, että näkyvissä on vain tietyt ehdot täyttävät asiakkaat. Myymälään on voinut esimerkiksi saapua uusi erä kenkiä ja myyjä haluaa ilmoittaa siitä asiakkaille, jotka ostavat mielellään kenkiä. Siinä tapauksessa myyjä voi etsiä sopivia asiakkaita suodattamalla asiakaskirjaa ja toimia sitten saadun tuloksen perusteella.

Jos jotain asiakasta ei enää pidetä jostain syystä avainasiakkaana eikä tällainen tarkka hallinta ole enää välttämätöntä, myyjä voi poistaa hänet asiakaskirjasta.

Osa jälleenmyyjistä ei halua hallita asiakkaita myyjätasolla. He haluavat sen sijaan hallita avainasiakkaiden luetteloa myymälätasolla. Siinä tapauksessa he voivat tarkastella asiakkaita myymälän asiakaskirjoissa. Tämän vaihtoehdon avulla jälleenmyyjät voivat tarkastella asiakkaita kaikista niiden myyjien asiakaskirjoista, joiden osoitekirja vastaa valitun myymälän osoitekirjaa. Jos myyjä työskentelee yrityksen useissa myymälöissä, tällä tavoin asiakaskirjassa näkyy kaikkien kyseisten myymälöiden asiakkaat. Toiminto myös muita ominaisuuksia. Asiakkaat voidaan esimerkiksi määrittää uudelleen myyjältä toiselle. Tästä ominaisuudesta on hyötyä myyjien saadessa siirron tai vaihtaessa työpaikkaa.

Kullakin myyjällä on yksi yrityskohtainen asiakaskirja, ja myyjät voivat lisätä asiakaskirjaan yhden asiakkaan tai useita asiakkaita. Asiakas voidaan lisätä Commercessa tällä hetkellä vain yhteen asiakaskirjaan. Microsoft suunnittelee kuitenkin sellaisen toiminnon lisäämistä, jolla yksittäinen asiakas voidaan lisätä useaan asiakaskirjaan.

> [!NOTE]
> Asiakashausta poiketen asiakaskirja ei suodata asiakastietueita myymälän osoitekirjojen mukaan.

## <a name="activities-and-notes"></a>Tehtävät ja huomautukset

Jälleenmyyjät saavat verkkokanavien kautta tietoa asiakkaiden mieltymyksistä ilman, että asiakkaiden olisi nimenomaisesti annettava nämä tiedot. Kun asiakkaat sen sijaan ovat myymälässä vuorovaikutuksessa myyjien kanssa, he kertovat mieltymyksistään tietoisesti. Valitettavasti nämä tiedot ehkä unohtuvat, kun myyntitapahtuma päättyy. Jos nämä tiedot kuitenkin tallennetaan, ne auttavat jälleenmyyjiä ymmärtämään asiakkaitaan paremmin, mikä puolestaan mahdollistaa parempien suositusten tekemisen ja koko ostoskokemuksen parantamisen.

Myyjät voivat tallentaa asiakkaiden jakamat tärkeät tiedot asiakaskirjan määritteiden lisäksi myös tehtävä- ja huomautustoiminnoilla. Jälleenmyyjät voivat määrittää tehtävätyyppejä, kuten tiedot myymäläkäynnistä, sähköpostiosoite, puhelinnumero ja tapaamiset. Myyjän luomia tehtäviä voi tarkastella myyntipisteessä aikajanamuodossa. Niitä voi tarkastella myös Headquartersin **Kaikki asiakkaat \> Yleiset** -sivun **Tehtävät**-välilehdessä.

Myyjät voivat tallentaa yleisiä asiakastietoja huomautuksiin, joita voi tarkastella ennen kutakin asiakastilannetta. Nämä huomautukset tallennetaan Headquartersiin, ja niitä voidaan tarkastella asiakasprofiilissa tai puhelinkeskuksen asiakastietosivulla.

> [!NOTE]
> Tällä hetkellä kuka tahansa yrityksessä työskentelevä myyjä, joka voi katsoa asiakastietosivuja, voi tarkastella kaikki huomautuksia tai tehtäviä. Huomautukset ja tehtävät eivät rajoitu myyjään, joka lisäsi asiakkaan asiakaskirjaan.

## <a name="integration-with-dynamics-365-customer-insights"></a>Integrointi Dynamics 365 Customer Insights:n kanssa

Dynamics 365 Customer Insights -sovelluksen avulla jälleenmyyjät voivat kerätä tietoja erilaisista järjestelmistä, joiden kautta asiakkaat ovat vuorovaikutuksessa jälleenmyyjän brändin kanssa. He voivat luoda näiden tietojen avulla yhden näkymän asiakkaasta ja saada tällä tavoin merkityksellisiä tietoja. Customer Insightsin ja Commercen ansiosta jälleenmyyjät voivat valita vähintään yhden mittarin asiakaskirjan asiakaskortissa näytettäväksi. Jälleenmyyjät voivat esimerkiksi laskea Customer Insightsin tietojen avulla asiakkaan vaihtuvuustodennäköisyyden ja määrittää parhaan seuraavan toiminnon. Jos nämä arvot määritetään mittareiksi, ne voidaan näyttää asiakaskortissa antamaan olennaisia tietoja myyjälle. Lisätietoja Customer Insightsista on [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview) -dokumentaatiossa. Lisätietoja mittareista on kohdassa [Mittarit](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Asiakashallinnan määrittäminen

Ota asiakashallintatoiminnot käyttöön ympäristössä seuraavien ohjeiden mukaisesti:

1. Suodata toimintoja **Toimintojen hallinta** -työtilassa **Vähittäismyynti ja kauppa** -moduulin perusteella.

    ![Asiakashallinta Commerce-moduulin toimintoluettelossa](./media/Enable_clienteling.png "Asiakashallinta Vähittäismyynti ja kauppa -moduulin toimintoluettelossa")

2. Ota **Asiakashallinta**-toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
3. Valitse **Commercen parametrit** -sivun **Numerosarja**-välilehdessä **Asiakaskirjan tunniste** -rivi. Valitse sitten numerosarja **Numerosarjan koodi** -kentässä. Järjestelmä määrittää asiakaskirjojen tunnuksen tämän numerosarjan perusteella.
4. Valitse **Tallenna**.
5. Luo uusi määriteryhmä. Se sisältää määritteet, jotka tallennetaan asiakaskirjoissa hallituista asiakkaista. Lisätietoja on kohdassa [Määritteet ja määriteryhmät](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Määritä pakolliset määritteet **Voidaan tarkentaa** -muodossa. Myyjät voivat suodattaa asiakaskirjaa näiden määritteiden avulla.
    - Määritä määritteiden näyttöjärjestys. Näyttöjärjestys määrittää, mitkä määritteet näytetään asiakaskirjan asiakaskortissa. Näyttöjärjestys 1 on korkeampi kuin näyttöjärjestys 2. Tämän vuoksi määrite, jonka näyttöjärjestys on 1, näytetään ennen määritettä, jonka näyttöjärjestys on 2.

    > [!NOTE]
    > Voit määrittää Customer Insightsin käytettäväksi samalta sivulta. Azuren sovellustunnus ja salauskoodi on kuitenkin luotava todennusta varten. (Lisätietoja on vaatimuksista on jäljempänä tässä ohjeaiheessa kohdassa [Customer Insightsin ja Commercen integroinnin ottaminen käyttöön](#turn-on-the-integration-of-customer-insights-with-commerce).) Jos Customer Insights on otettu käyttöön ja valitset asiakaskortissa näytettävät mittarit, kyseiset mittarit näytetään ensin. Seuraavaksi näytetään asiakaskirjan määriteryhmät näyttöjärjestyksen mukaisesti. Jos valitset esimerkiksi kaksi mittaria Customer Insightsista, nämä kaksi mittaria ja yksi asiakaskirjan määrite näytetään asiakaskortissa. (Näytettävä asiakaskirjan määrite on määrite, jolla on korkein näyttöjärjestys.)

6. Valitse **Commercen parametrit** -sivun **Asiakashallinta**-välilehden **Asiakaskirjan määriteryhmä** -kentässä juuri luotu määriteryhmä.

    ![Asiakaskirjan määriteryhmä valittuna](./media/Client%20book%20attributes.png "Asiakaskirjan määriteryhmä valittuna")

7. Jos haluat tallentaa myyntipisteessä tapahtuvia tehtäviä, määritä tehtävätyypit **Tehtävätyypit**-sivulla (**Retail ja Commerce \> Asiakkaat \> Tehtävätyypit**).

    > [!NOTE]
    > Commerce Scale Unit hakee tehtävätyypit, kun se tekee reaaliaikaisen kutsun ensimmäisen kerran. Kun tehtävät haetaan, ne tallennetaan välimuistiin muutamaksi tunniksi. Jos muutat aktiviteettityyppejä, odota, kunnes välimuistin tietoja ei enää käytetä. Vaihtoehtoisesti Commerce Scale Unit -palvelun voi käynnistää uudelleen ei-tuotantoympäristössä.

8. Lisää kaksi painiketta kyseiseen myyntipisteen näyttöasetteluun siten, että myyjät voivat tarkastella omaa asiakaskirjaansa ja myymälän asiakaskirjaan. (Myymälän asiakaskirjassa on asiakkaita kaikkien myymälän osoitekirjan jakavien myyjien asiakaskirjoista.) Näiden toimintojen nimet ovat **Näytä asiakaskirjan asiakkaat** ja **Näytä myymälän asiakaskirjojen asiakkaat**. Lisäksi käytettävissä on kolme asiakaskirjoihin liittyvää toimintoa. Nämä toiminnot määrittävät myyjät, jotka saavat lisätä, poistaa ja määrittää uudelleen asiakaskirjan asiakkaita. Näiden toimintojen nimet ovat **Lisää asiakas asiakaskirjaan**, **Poista asiakas asiakaskirjasta** ja **Määritä asiakkaat uudelleen asiakaskirjaan**.
9. Suorita seuraavat jakeluaikataulun työt: 1040, 1150, 1110 ja 1090.

Kun olet suorittanut tämän menettelyn, myyjät voivat avata asiakastietosivun myyntipisteessä ja lisätä asiakkaita omaan asiakaskirjaansa, tarkastella ja tallentaa asiakkaita koskevia tehtäviä ja huomautuksia sekä tehdä kohdistuksia asiakkaille suodattamalla asiakaskirjaa asiakkaan ja asiakaskirjan määritteillä. Seuraavassa kuvassa on esimerkki asiakaskirjassa.

![Esimerkki asiakaskirjasta](./media/client_book.png "Esimerkki asiakaskirjasta")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Customer Insightsin ja Commercen integroinnin ottaminen käyttöön

Customer Insightsin ja Commercen integrointi edellyttää, että sinulla on aktiivinen Customer Insights -esiintyjä siinä vuokraajassa, jossa Commerce on valmisteltu. Tarvitset myös Azure Active Directory (Azure AD) -käyttäjätilin, jossa on Azure-tilaus.

Määritä integrointi noudattamalla seuraavia ohjeita:

1. Rekisteröi uusi sovellus Azure-portaalissa ja kirjoita muistiin sovelluksen nimi, sovelluksen tunnus ja salainen koodi. Näitä tietoja käytetään Commerce- ja Customer Insights -palveluiden väliseen todennukseen. Merkitse salainen koodi muistiin turvallisesti, koska on tallennettava avainsäilöön. Käytä seuraavassa esimerkissä CI_Access_name, CI_Access_AppID ja CI_Access_Secret sovelluksen nimelle, tunnukselle ja salaiselle koodille. Lisätietoja: [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Varmista menettely, jonka avulla muistat muuttaa salauskoodin ennen sen vanhentumista. Muussa tapauksessa integrointi päättyy odottamatta.

2. Siirry Customer Insights -instanssiin ja hae yllä luodun sovelluksen nimeä (tässä esimerkissä CI_Access_name).
3. Luo Azure Key Vault ja ota muistiin nimi ja URL (tässä esimerkissä "KeyVaultName", "KeyVaultURL"). Lisätietoja on kohdassa [Pika-aloitus: Salauskoodin määrittäminen ja sen noutaminen Azure Key Vaultista Azure-portaalin avulla](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Tallenna salainen koodi (tässä esimerkissä "CI_Access_Secret") säilöön. Kun salainen koodi tallennetaan säilössä, se saa nimen. Merkitse muistiin salaisen koodin nimi (tässä esimerkissä SecretName).
5. Voit käyttää salaista koodia Azure Key Vaultissa luomalla toisen sovelluksen, jolla on sovellustunnus ja salainen koodi (tässä esimerkissä "KeyVault_Access_AppID" ja "KeyVault_Access_Secret"). Merkitse salainen koodi muistiin huolellisesti, koska sitä enää näytetä.
6. Seuraavaksi sinun on annettava sovellukselle oikeudet käyttää Key Vault -säilöä Commercesta API-liittymien avulla. Siirry Azure-portaalissa sovellussivulle. Valitse **Hallinta**-kohdasta **Ohjelmointirajapinnan käyttöoikeudet**. Lisää käyttöoikeus **Azure Key Vault** -säilön käyttöön. Valitse tälle käyttöoikeudelle **Käyttöoikeuskäytäntö**. Valitse malli nimellä **Salaisen koodin hallinta** ja valitse **Hae**-, **Luetteloi**-, **Pura salaus**- ja **Salaa**-vaihtoehdot. 
5. Valitse Commerce headquartersissa **Järjestelmän hallinta \> Asetukset \> Avainsäilön parametrit** ja anna tarvittavat avainsäilön tiedot. Anna sitten **Avainsäilön asiakas** -kentässä sovelluksen tunnus, jota käytit vaiheessa 4. Tällä tavoin Commerce voi käyttää avainsäilössä olevia salauskoodeja.
6. Voit lisätä vaiheessa 1 luodun sovelluksen turvallisten sovellusten luetteloon (jota kutsutaan joskus turvallisten luetteloksi) siirtymällä Customer Insightsiin ja antamalla sovellukselle **katseluoikeuden**. Lisätietoja on kohdassa [Käyttöoikeudet](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. Päivitä **Järjestelmänvalvonta > Määritä > Avainsäilön parametrit** -sivulla Commerce HQ -sovelluksessa kentät alla kuvatulla tavalla: 

- **Key Vault – URL-osoite**: "KeyVaultURL" (edellä olevasta vaiheesta 3).
- **Key Vault – asiakasohjelma**: "KeyVault_Access_AppID" (edellä olevasta vaiheesta 5).
- **Key Vault – salainenn avain**: "KeyVault_Access_Secret" (edellä olevasta vaiheesta 5).
- Kohdassa **Salauskoodit**:
    - **Nimi**: Mikä tahansa nimi, esimerkiksi "CISecret".
    - **Kuvaus**: Mikä tahansa arvo.
    - **Salainen koodi**: **vault**://<Name of key vault>/<name of secret>> Tässä esimerkissä se on "vault://KeyVaultName/SecretName".

Kun olet päivittänyt kentät, varmista valitsemalla **Vahvista**, että Commerce-sovellus voi käyttää salaista koodia.

8. Määritä Commercen **Commercen parametrit** -sivun **Asiakashallinta** -välilehden **Dynamics 365 Customer Insights** -pikavälilehdessä **Sovelluksen tunnus** -kentän arvoksi "CI_Access_AppID" (edellä olevasta vaiheesta 1). Valitse **salaisen koodin nimelle** edellä olevassa vaiheessa 7 syötetty nimi ("CISecret"). Määritä **Ota Customer Insights käyttöön** -asetukseksi **Kyllä**. Jos asetukset eivät jostain syystä onnistu, näet virhesanoman ja tämän asetuksen arvoksi määritetään **Ei**. 

Customer Insightsissa voi olla useita ympäristöjä, kuten testi- ja tuotantoympäristöt. Kirjoita **Ympäristön esiintymätunnus** -kenttään asianmukainen ympäristö. Anna **Vaihtoehtoinen asiakastunnus** -kenttään se Customer Insights -ominaisuus, joka yhdistetään asiakastilin numeroon. (Commercessa asiakkaan tilinumero on asiakkaan tunnus.) Muut kolme ominaisuutta ovat mitat, jotka näkyvät asiakaskirjan asiakaskortissa. Voit valita enintään kolme asiakaskortissa näytettävää mittaria. Mittoja ei kuitenkaan tarvitse valita. Kuten aiemmin on mainittu, järjestelmä näyttää ensin nämä arvot ja näyttää sitten asiakaskirjan määriteryhmän arvot.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
