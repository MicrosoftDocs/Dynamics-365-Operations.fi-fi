---
title: Konfiguroi kulujen hallinta
description: Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin matkalaskut määritetään.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570618"
---
# <a name="configure-expense-management"></a>Konfiguroi kulujen hallinta

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin matkalaskut määritetään. Matkalaskujen alueelle voit tallentaa esimerkiksi maksutapojen, matkustusehdotusten, kuluraporttien ja -käytäntöjen tiedot.

Koska monet päätökset, jotka teet kulujen hallinnan määrityksiä suunniteltaessa, perustuvat organisaatiohierarkiaan ja taloushallinnan rakenteeseen, sinun on tutustuttava kyseisten alueiden ohjeistukseen.

## <a name="intercompany-expenses"></a>Konsernin sisäiset kulut

Kun otat konsernin sisäiset kulut käyttöön, annat yrityksille ja työntekijöille oikeuden luoda kuluja toisen organisaation yrityksen puolesta tai kerätä siltä maksun. Esimerkiksi yrityksen A työntekijä suorittaa yrityksen B projektin, ja projektiin liittyy matkakuluja. Jos konsernin sisäiset kulut on otettu käyttöön, työntekijä voi sitten lähettää kuluraportin, joka kirjaa kulun yritykselle B, ja kulun maksaa hänelle yritys A. Jos organisaatiossa ei ole useita yrityksiä, konsernin sisäisiä kuluja ei tarvitse ottaa käyttöön.

**Päätös:** haluatko ottaa käyttöön konsernin sisäiset kulut?

## <a name="financial-management"></a>Taloushallinto

Kulujen hallinta on integroitu tiukasti organisaation taloushallintoon. Monet kulujen hallinnan määritykset perustuvat päätöksiin, joita olet tehnyt organisaation raha-asioista. Seuraavissa osissa käsitellään suunnittelua edellyttäviä alueita ja päätöksiä, jotka perustuvat organisaation taloudellisiin päätöksiin ja johtoryhmän opastukseen.

### <a name="per-diems"></a>Päivärahat

Organisaation myöntämät työntekijöiden päivärahat on määritettävä. Koska päivärahoja käytetään yleensä kulujen, kuten aterioiden, majoituksen ja muiden satunnaisten menojen korvaamiseen, voit luoda sääntöjä organisaation tarjoamille päivärahoille. Päivärahan suuruus voi perustua vuodenaikaan, matkan kohteeseen tai molempiin. Kun määritä päivärahasäännön, voit määrittää, mikä prosenttiosuus päivärahasta pidätetään, jos työntekijällä on käytettävissään ilmaisia aterioita tai palveluita. Voit myös määrittää päivärahatasot, joilla määritetään vähimmäis- ja enimmäismäärä tunteja, joilla tietyn suuruista päivärahaa voidaan käyttää työntekijän matkalla.

**Päätökset:**

- Oletusarvoinen päivärahasäännöt ensimmäiselle ja viimeiselle päivälle:

    - Mikä määrä tunteja työntekijän on vähintään ilmoitettava saadakseen päivärahan?
    - Onko ateriakorvaus pienempi ensimmäisenä ja viimeisenä päivänä? Jos on korvaus on pienempi, mikä on pienennyksen määrä?
    - Onko majoituskorvaus pienempi ensimmäisenä ja viimeisenä päivänä? Jos on korvaus on pienempi, mikä on pienennyksen määrä?
    - Onko muiden ensimmäisenä ja viimeisenä päivänä syntyvien kulujen korvaus pienempi? Jos on korvaus on pienempi, mikä on pienennyksen määrä?

- Oletusaroiset päivärahasäännöt:

    - Pieneneekö ateriakorvaus prosentuaalisesti, jos ateria on ilmainen? Jos on korvaus on pienempi, mikä on kutakin ateriaa koskevan pienennyksen määrä?
    - Lasketaanko ateriakorvauksen vähennys päivä- tai matkakohtaisesti vai päiväkohtaisten aterioiden määrän mukaan?
    - Tuleeko päivärahan summat pyöristää normaalisti vai ylöspäin?
    - Lasketaanko päivärahat 24 tunnin jaksolta vai kalenteripäivän mukaan?

- Sijaintiin perustuvat päivärahasäännöt:

    - Vaihteleeko päivärahan määrä sijainnin mukaan? Minkä sijaintien?
    - Jos päivärahat vaihtelevat sijainnin mukaan, mikä on kussakin sijainnissa annettavan päivärahan osuus seuraaville kuluille:

        - Ateriat
        - Hotelli
        - Muut kulut

### <a name="expense-management-journals-and-accounts"></a>Kulujen hallinnan kirjauskansiot ja tilit

Kulujen hallinta edellyttää useiden kirjauskansioiden ja tilien käyttöä. Sinun on esimerkiksi päätettävä, käytetäänkö samaa tiliä käteisennakoille ja luottokorttien riitautuksille.

**Päätökset:**

- Mihin kirjanpidon kirjauskansioon hyväksytyt kuluraportit kirjataan?
- Mitä tiliä käytetään käteisennakoille?
- Kirjataanko käteisennakot välittömästi?

### <a name="payment-methods"></a>Maksutavat

Jos työtekijöillä on mahdollisuus aiheuttaa kuluja yrityksen puolesta, sinun on määritettävä maksutavat, joita työntekijät saavat käyttää. Voit esimerkiksi sallia työntekijöille käteisen ja yrityksen luottokortin käytön. Voit myös sallia työntekijöiden omien luottokorttien käytön, joka hyvitetään sitten työntekijöille. Jokaisen sallitun maksutavan kohdalla on tehtävä seuraavat päätökset.

**Päätökset:**

- Mitkä maksutavat sallitaan?
- Kuka omistaa maksutavan kulut?
- Onko vastatilillä jokin tyyppi? Jos vastatili on, mikä tili se on?
- Jos vastatili on, mikä tili se on?
- Jos maksutapa on luottokortti, pitäisikö maksutapaa käyttää vain tuotujen tapahtumien yhteydessä?

### <a name="expense-categories-and-shared-categories"></a>Kululuokat ja jaetut luokat

Kun työntekijät luovat kuluraportin, jokainen heidän tallentamansa kulu on liitettävä kululuokkaan. Kululuokat johdetaan jaetuista luokista, jotka jaetaan kaikissa organisaation yrityksissä. Nämä luokat voidaan jakaa myös projektin hallinnassa ja kirjanpidossa sen mukaan, miten organisaatio on määritetty. Määritä organisaation määrityksen ja toteutusryhmän ohjeistuksen perusteella, käytetäänkö kulujen hallinnassa käytettyjä luokkia vain kuluissa vai jaetaanko ne projektinhallinnan ja kirjanpidon sekä kulujen kesken. Huomaa, että nämä luokat voidaan jakaa projektin ja kuljen tai projektin tai tuotannon kesken mutta ei kulujen ja tuotannon kesken. Jokaisen kululuokan kohdalla on tehtävä seuraavat päätökset.

**Päätökset:**

- Mikä on kululuokka? Esimerkkiluokkia ovat lennot, hotellit tai kilometrikorvaukset.
- Voiko tätä kululuokkaa käyttää myös projektinhallinnassa ja kirjapidossa?
- Mikä on kulutyyppi?
- Mikä on kululuokan oletusmaksutapa?
- Tuleeko kuluraportin kulujen olla eriteltyjä?
- Mikä on kululuokan oletuspäätili?
- Mikä on kululuokan oletusarvoinen nimikkeen arvonlisäveroryhmä?
- Salliiko kululuokka lisämaksutavat? Jos muut maksutavat ovat sallittuja, mitkä maksutavat?
- Onko kululuokalla alaluokkia? Jos alaluokkia on, tee lisäksi seuraavat päätökset:

    - Jätetäänkö alaluokat veronpalautusten ulkopuolelle?
    - Mikä on alaluokkien nimikkeiden arvonlisäveroryhmä?

Jos tätä kululuokkaa käytetään myös projektinhallinnassa ja kirjanpidossa, vastaa jäljellä oleviin kysymyksiin. Muussa tapauksessa siirry seuraavaan osaan.

- Mitä kustannustilejä käytetään seuraavissa kuluissa?

    - Kustannus
    - Palkanlaskennan kohdistus
    - KET - kustannusarvo
    - Kustannukset – nimike
    - KET - Kustannusarvo - Nimike
    - Jaksotettu tappio
    - KET– jaksotettu tappio

- Mitä tuottotilejä käytetään seuraavissa?

    - Laskutettu tuotto
    - Jaksotettu tuotto – myyntiarvo
    - KET – myyntiarvo
    - Jaksotettu tuotto – tuotanto
    - KET – tuotanto
    - Jaksotettu tuotto – voitto
    - KET – voitto
    - Jaksotettu tuotto – ylläpitosopimus
    - KET – ylläpitosopimus

### <a name="taxes"></a>Verot

Kuluihin liittyvissä veroissa on määritettävä, mitä sisällytetään tai otetaan käyttöön kuluraporteissa.

**Päätökset:**

- Sisältyykö arvonlisävero kulusummiin?
- Otetaanko veronpalautukset käyttöön kuluissa?

    > [!NOTE]
    > Jos olet päättänyt käyttää yhdysvaltain arvonlisä- ja käyttöverosääntöjä kirjanpidon suunnittelussa, et voi käyttää kuluissa veronpalautusta. (Jos haluat käyttää yhdysvaltain arvonlisä- ja käyttöverosääntöjä, määritä **Käytä arvonlisäverotuksen sääntöjä** -asetukseksi **Kyllä**.)

## <a name="policies"></a>Käytännöt

Voit luoda kuluraporttikäytäntöjä, joilla organisaatio voi säästää aikaa ja rahaa, kun työntekijät aiheuttavat kuluja yrityksen nimissä. Käytännöt varmistavat, että työntekijät noudattavat budjettia, antavat kaikki tarvittavat tiedot ja kuluttavat rahaa vain tarvittaessa. Seuraavat päätökset on tehtävä jokaisen kuluraporttikäytännön ja jokaisen luomasi kuluraportin hyväksyntäkäytännön kohdalla.

**Päätökset:**

- Mikä on käytännön nimi?
- Mitä on kulukäytännön tarkoitus?
- Jos olet aiemmin päättänyt ottaa konsernin sisäiset kulut käyttöön, missä organisaation yrityksissä käytäntöä käytetään?
- Mikä käytäntö otetaan käyttöön?
- Milloin käytäntö vanhentuu?
- Mikä on käytäntösääntö?
- Mikä on käytäntösäännön tulos?
