---
title: Konfiguroi kulujen hallinta
description: "Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics AX:n matkalaskut määritetään. Matkalaskujen alueelle voit tallentaa esimerkiksi maksutapojen, matkustusehdotusten, kuluraporttien ja -käytäntöjen tiedot."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 88cdf531b6da615034f9982d3503b9add0100479
ms.lasthandoff: 03/31/2017


---

# <a name="configure-expense-management"></a>Konfiguroi kulujen hallinta

Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics AX:n matkalaskut määritetään. Matkalaskujen alueelle voit tallentaa esimerkiksi maksutapojen, matkustusehdotusten, kuluraporttien ja -käytäntöjen tiedot. 

Koska monet päätökset, jotka teet kulujen hallinnan määrityksiä suunniteltaessa, perustuvat organisaatiohierarkiaan ja taloushallinnan rakenteeseen, sinun on tutustuttava kyseisten alueiden ohjeistukseen.

## <a name="intercompany-expenses"></a>Konsernin sisäiset kulut
Kun otat konsernin sisäiset kulut käyttöön, annat yrityksille ja työntekijöille oikeuden luoda kuluja toisen organisaation yrityksen puolesta tai kerätä siltä maksun. Esimerkiksi yrityksen A työntekijä suorittaa yrityksen B projektin. Jos konsernin sisäiset kulut on otettu käyttöön, työntekijä voi sitten lähettää aikaraportin yritykselle B, joka maksaa hänelle. Jos organisaatiossa ei ole useita yrityksiä, konsernin sisäisiä kuluja ei tarvitse ottaa käyttöön. **Päätös:** haluatko ottaa käyttöön konsernin sisäiset kulut?

## <a name="financial-management"></a>Taloushallinto
Kulujen hallinta on integroitu tiukasti organisaation taloushallintoon. Monet kulujen hallinnan määritykset perustuvat päätöksiin, joita olet tehnyt organisaation raha-asioista. Seuraavissa osissa käsitellään suunnittelua edellyttäviä alueita ja päätöksiä, jotka perustuvat organisaation taloudellisiin päätöksiin ja johtoryhmän opastukseen.

### <a name="per-diems"></a>Päivärahat

Organisaation myöntämät työntekijöiden päivärahat on määritettävä. Koska päivärahoja käytetään yleensä kulujen, kuten aterioiden, majoituksen ja muiden satunnaisten menojen korvaamiseen, voit luoda sääntöjä organisaation tarjoamille päivärahoille. Päivärahan suuruus voi perustua vuodenaikaan, matkan kohteeseen tai molempiin. Kun määritä päivärahasäännön, voit määrittää, mikä prosenttiosuus päivärahasta pidätetään, jos työntekijällä on käytettävissään ilmaisia aterioita tai palveluita. Voit myös määrittää päivärahatasot, joilla määritetään vähimmäis- ja enimmäismäärä tunteja, joilla tietyn suuruista päivärahaa voidaan käyttää työntekijän matkalla. **Päätökset: **

-   Oletusarvoinen päivärahasäännöt ensimmäiselle ja viimeiselle päivälle:
    -   Mikä määrä tunteja työntekijän on vähintään ilmoitettava saadakseen päivärahan?
    -   Onko ateriakorvaus pienempi ensimmäisenä ja viimeisenä päivänä? Jos näin on, millä prosentilla korvausta pienennetään?
    -   Onko majoituskorvaus pienempi ensimmäisenä ja viimeisenä päivänä? Jos näin on, millä prosentilla korvausta pienennetään?
    -   Onko muiden ensimmäisenä ja viimeisenä päivänä syntyvien kulujen korvaus pienempi? Jos näin on, millä prosentilla korvausta pienennetään?
-   Oletusaroiset päivärahasäännöt:
    -   Pieneneekö ateriakorvaus prosentuaalisesti, jos ateria on ilmainen? Jos näin on, mikä on kunkin aterian prosentuaalinen alennus?
    -   Lasketaanko ateriakorvauksen vähennys päivä- tai matkakohtaisesti vai päiväkohtaisten aterioiden määrän mukaan?
    -   Pyöristetäänkö päivärahasummat normaalisti vai ylöspäin?
    -   Lasketaanko päivärahat 24 tunnin jaksolta vai kalenteripäivän mukaan?
-   Sijaintiin perustuvat päivärahasäännöt:
    -   Vaihteleeko päivärahan suuruus sijainnin mukaan ja mitkä sijainnit ovat mukana?
    -   Jos päivärahan suuruus vaihtelee sijainnin mukaan, mikä prosenttiosuus määritetään kullekin sijainnille:
        -   ateriat
        -   hotelli
        -   muut kulut

### <a name="expense-management-journals-and-accounts"></a>Kulujen hallinnan kirjauskansiot ja tilit

Kulujen hallinta edellyttää useiden kirjauskansioiden ja tilien käyttöä. Sinun on esimerkiksi päätettävä, käytetäänkö samaa tiliä käteisennakoille ja luottokorttien riitautuksille. **Päätökset:**

-   Mihin kirjanpidon kirjauskansioon hyväksytyt kuluraportit kirjataan?
-   Mitä tiliä käytetään käteisennakoille?
-   Kirjataanko käteisennakot välittömästi?

### <a name="payment-methods"></a>Maksutavat

Jos työtekijöillä on mahdollisuus aiheuttaa kuluja yrityksen puolesta, sinun on määritettävä maksutavat, joita työntekijät saavat käyttää. Voit esimerkiksi sallia työntekijöille käteisen ja yrityksen luottokortin käytön. Voit myös sallia työntekijöiden omien luottokorttien käytön, joka hyvitetään sitten työntekijöille. Jokaisen sallitun maksutavan kohdalla on tehtävä seuraavat päätökset. **Päätökset:**

-   Mitkä maksutavat sallitaan?
-   Kuka omistaa maksutavan kulut?
-   Onko vastatilillä jokin tyyppi? Jos on, mikä se on?
-   Jos vastatili on, mikä tili se on?
-   Jos maksutapa on luottokortti, pitäisikö maksutapaa käyttää vain tuotujen tapahtumien yhteydessä?

### <a name="expense-categories-and-shared-categories"></a>Kululuokat ja jaetut luokat

Kun työntekijät luovat kuluraportin, jokainen heidän tallentamansa kulu on liitettävä kululuokkaan. Kululuokat johdetaan jaetuista luokista, jotka jaetaan kaikissa organisaation yrityksissä. Nämä luokat voidaan jakaa myös projektin hallinnassa ja kirjanpidossa sen mukaan, miten organisaatio on määritetty. Määritä organisaation määrityksen ja toteutusryhmän ohjeistuksen perusteella, käytetäänkö kulujen hallinnassa käytettyjä luokkia vain kuluissa vai jaetaanko ne projektin ja kulujen kesken. Huomaa, että nämä luokat voidaan jakaa projektin ja kuljen tai projektin tai tuotannon kesken mutta ei kulujen ja tuotannon kesken. Jokaisen kululuokan kohdalla on tehtävä seuraavat päätökset. **Päätökset:**

-   Mikä on kululuokka? Esimerkiksi lennot, hotelli tai kilometrimäärä.
-   Voiko tätä kululuokkaa käyttää myös projektinhallinnassa ja kirjapidossa?
-   Mikä on kulutyyppi?
-   Mikä on kululuokan oletusmaksutapa?
-   Onko tämän luokan kulut eriteltävä?
-   Mikä on kululuokan oletuspäätili?
-   Mikä on kululuokan oletusarvoinen nimikkeen arvonlisäveroryhmä?
-   Salliiko kululuokka lisämaksutavat? Jos näin on, mitä ne ovat?
-   Onko kululuokalla alaluokkia? Jos on:
    -   Jätetäänkö alaluokat veronpalautusten ulkopuolelle?
    -   Mikä on alaluokkien nimikkeiden arvonlisäveroryhmä?

    Jos tätä kululuokkaa käytetään myös projektinhallinnassa ja kirjanpidossa, vastaa jäljellä oleviin kysymyksiin. Muussa tapauksessa tämä osa on valmis.
-   Mitä kustannustilejä käytetään seuraavissa?
    -   Kustannus
    -   Palkanlaskennan kohdistus
    -   KET – kustannusarvo
    -   Kustannukset – nimike
    -   KET – kustannusarvo – nimike
    -   Jaksotettu tappio
    -   KET– jaksotettu tappio
-   Mitä tuottotilejä käytetään seuraavissa?
    -   Laskutettu tuotto
    -   Jaksotettu tuotto – myyntiarvo
    -   KET – myyntiarvo
    -   Jaksotettu tuotto – tuotanto
    -   KET – tuotanto
    -   Jaksotettu tuotto – voitto
    -   KET – voitto
    -   Jaksotettu tuotto – ylläpitosopimus
    -   KET – ylläpitosopimus

 

### <a name="taxes"></a>Verot

Kuluihin liittyvissä veroissa on määritettävä, mitä sisällytetään tai otetaan käyttöön kuluraporteissa. **Päätökset:**

-   Sisältyykö arvonlisävero kulusummiin?
-   Otetaanko veronpalautukset käyttöön kuluissa?

Huomaa, että jos olet päättänyt käyttää kirjanpidon suunnittelun aikana Yhdysvaltain arvonlisäverosääntöjä, mikä tehdään valitsemalla **Käytä arvonlisäverotuksen sääntöjä** -kentän arvoksi Kyllä, et voi ottaa käyttöön veronpalautuksia kuluissa.

## <a name="policies"></a>Käytännöt
Voit luoda kuluraporttikäytäntöjä, joilla organisaatio voi säästää aikaa ja rahaa, kun työntekijät aiheuttavat kuluja yrityksen nimissä. Käytännöt varmistavat, että työntekijät noudattavat budjettia, antavat kaikki tarvittavat tiedot ja kuluttavat rahaa vain tarvittaessa. Seuraavat päätökset on tehtävä jokaisen kuluraporttikäytännön ja jokaisen luomasi kuluraportin hyväksyntäkäytännön kohdalla. **Päätökset: **

-   Mikä on käytännön nimi?
-   Mitä on kulukäytännön tarkoitus?
-   Jos olet aiemmin päättänyt ottaa konsernin sisäiset kulut käyttöön, missä organisaation yrityksissä käytäntöä käytetään?
-   Mikä käytäntö otetaan käyttöön?
-   Milloin käytäntö vanhentuu?
-   Mikä on käytäntösääntö?
-   Mikä on käytäntösäännön tulos?



