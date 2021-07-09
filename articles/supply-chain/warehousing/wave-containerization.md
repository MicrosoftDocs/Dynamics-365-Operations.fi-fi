---
title: Konttiinpakkaus
description: Tässä aiheessa kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen. Automaattinen konttiin pakkaus luo kontit ja keräilytyön lähetyksille aallon käsittelyn yhteydessä.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 88e38989e3d3e46d0c43779659bc6ea2e29f08e2
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292734"
---
# <a name="containerization"></a>Konttiinpakkaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen. Automaattinen konttiin pakkaus luo kontit ja keräilytyön lähetyksille aallon käsittelyn yhteydessä.

Jos haluat määrittää konttiin pakkauksen, sinun on luotava seuraavat:

- **Kontin tyyppi** – Määritä konttien fyysiset ominaisuudet. Käytä konttityyppejä varastonimikkeiden pakkaamiseen tiettyyn pakkaustyyppiin ja kokoon, kuten lokeroihin tai kuormalavoihin.
- **Konttiryhmät** – Luo samankaltaisten konttityyppien ryhmiä. Esimerkiksi konttiryhmä voi sisältää sellaiset konttityypit, joilla on samankaltaiset kokodimensiot. Konttiryhmä määrittelee järjestyksen, jossa kontit pakataan, sekä jokaisen kontin täyttöasteen.
- **Kontin koontiversiomalli** – Luo malleja, jotka määrittävät konttiinpakkauksen säännöt. Esimerkiksi säännöt varaston sekoittamiseksi ja muut pakkausstrategiat.
- **Aaltomallit** – Määritä vähintään yksi aaltomalli, jotta voit luoda konttiinpakkauksen keräilytyön.

## <a name="create-wave-templates-for-containerization"></a>Luo aaltomalleja konttiinpakkausta varten

Sinun on asetettava vähintään yksi lähetyksen aaltomalli konttiinpakkausta varten. Aaltomallit sisältävät kriteerit, jotka määrittävät seuraavat:

- Aaltojen käsittely. Tämä voi olla joko manuaalinen tai automaattinen.
- Miten keräystyö luodaan. Aaltomenetelmät määrittävät tämän. Aaltomallin on sisällettävä **konttiinpakkaus**-menetelmä.
- Nimikkeiden tai kohdistusrivien täsmääminen aallon kanssa.

Lisätietoja on kohdassa [Aaltomallit](wave-templates.md).

## <a name="create-container-types"></a>Konttityyppien luominen

Käytä konttityyppejä konttien kuvausten luomiseen, mukaan lukien fyysisten mittojen ja painokapasiteetin enimmäismäärät. Kun konttiin pakattua aaltoa käsitellään, kontit luodaan konttityypin tietojen perusteella.

Voit määrittää konttityypin noudattamalla seuraavia ohjeita:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttityypit**.
1. Luo uusi konttityyppi valitsemalla **Uusi**.
1. Kirjoita kontin tyypin yksilöllinen tunniste ja kuvaus.
1. Valitse **Taarapaino**-kentästä kontin todelliset tai arvioidut painot.
1. Kirjoita **Enimmäispaino**-kenttään konttiin sijoitettava enimmäispaino.
1. Määritä säilön fyysiset mitat **Kontin enimmäistilavuus**-, **Kontin enimmäispituus**-, **Kontin enimmäisleveys**- ja **Kontin enimmäiskorkeus** -kentissä.

    > [!NOTE]
    > Pituus- ja leveysarvot ovat vaihdettavissa keskenään. Tämä tarkoittaa, että voit kääntää nimikkeitä tarvittaessa sivusuunnassa tai x-akselilla. Jos esimerkiksi pituus on 2 jalkaa ja leveys on 1 jalka, voit vaihtaa pituuden 1 jalaksi ja leveyden 2 jalaksi. Huomaa, että tämä ei vaikuta korkeusdimensioon. Et voi muuttaa korkeusarvoa nimikkeen kiertämiseksi pystysuunnassa.

1. Valitse kontin mukautettujen arvojen määritteet kentissä. Määritteet ovat mukautettuja arvoja, joita käytetään nimikkeiden suodattamiseen tai lajitteluun sellaisen arvon perusteella, joka ei muutoin ole käytettävissä. Esimerkiksi jos haluat pakata nimikkeet tietylle asiakkaalle, voit luoda määritteen asiakkaan nimelle. Voit luoda määritteitä **Kontin määritteet**-sivulla.

## <a name="create-container-groups"></a>Konttiryhmien luominen

Voit määrittää konttityyppien loogiset ryhmät. Voit määrittää kullekin ryhmälle järjestyksen, jossa kontit pakataan, sekä jokaisen kontin täyttöasteen. Nimikkeen kokodimensioiden avulla määritetään, mahtuuko nimike konttiin. Järjestelmä valitsee kontin, jonka kokodimensiot ovat lähimpänä nimikettä. Jos ryhmässä on useita konttityyppejä, suosittelemme, että järjestät järjestyksen koon mukaan niin, että suurin kontti on ensimmäinen, numero 1 sarjassa, ja pienin kontti on viimeinen.

Voit määrittää konttiryhmän noudattamalla seuraavia ohjeita:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttiryhmät**.
1. Luo konttiryhmä valitsemalla **Uusi**.
1. Kirjoita konttiryhmälle yksilöllinen tunnus ja kuvaus.
1. Lisää konttityyppi ryhmään valitsemalla **Tiedot**-pikavälilehdellä **Uusi**.
1. Valitse **Kontin tyyppi**-kentässä konttityyppi.
1. Valitse **Siirrä ylös** tai **Siirrä alas** määrittääksesi järjestyksen, jossa konttityypit pakataan.

## <a name="create-container-build-templates"></a>Luo kontin koontimalleja

Voit määrittää säännöt kontitusprosessiin, esimerkiksi varaston sekoittamisen säännöt ja muut pakkausstrategiat. Voit esimerkiksi määrittää säännön, jotta työntekijät eivät voi pakata kohdistusrivejä, jotka edustavat myyntitilauksia eri asiakkailta samassa kontissa.

Voit määrittää kontin muodostusmallin noudattamalla seuraavia ohjeita:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Kontin koontimalli**.
1. Luo uusi kontin rakennusmalli.
1. Kirjoita **Konttiinpakkauksen nimi** - ja **Järjestysnumero** -kenttiin konttiinpakkauksen malli ja tilaus, joka täsmätään kohdistusriveihin.

    > [!NOTE]
    > Järjestelmä käyttää ensimmäistä mallia, jonka kyselyehdot kohdistusrivi täyttää. Aseta tämän vuoksi luettelon kärkeen se malli, jonka ehto on tarkin. Mitä laajempi ehto on, sitä todennäköisemmin kohdistusrivi vastaa ehtoa. Tämä saattaa johtaa siihen, että rivit määritetään väärään konttiin. Voit tarvittaessa muuttaa mallien järjestystä valitsemalla **Siirrä ylös** tai **Siirrä alas**.

1. Valitse **Konttiryhmän tunnus** -kentässä konttiryhmä, josta kontit luodaan.
1. Valitse **Peruskyselytyypit** -kentässä kyselytyyppi, joka määrittää pakattavat kohteet ja suodattimen perusteen. Käytettävissä ovat seuraavat asetukset:

      - **Myynnin kohdistusrivi** – Paketoi myyntitilauksille luodut kohdistusrivit.
      - **Siirron kohdistusrivi** – Paketoi siirtotilauksille luodut kohdistusrivit.
      - **Kontti** – Pakkaa kontti, jonka konttiinpakkaus on jo luonut. Tätä käytetään esimerkiksi konttien asettamiseksi sisäkkäin.

        > [!NOTE]
        > Käyttäessäsi sisäkkäisiä kontteja sinun on tehtävä konttipakkausmenetelmästä toistettava. Lisätietoja on kohdassa [Aaltomallit](wave-templates.md).

1. Kirjoita **Yleiset**-pikavälilehden **Aallon vaihekoodi** -kenttään aallon käsittelymenetelmän yksilöivä tunniste, joka linkittää kontin rakennusmallin aaltomallin vaiheisiin.
1. Valitsemalla **Salli jaetut keräilyt** -valintaruudun voit sallia työntekijöiden pakata työtilauksen nimikkeitä eri kontteihin. Tämä edellyttää, että koko määrä sopii konttiin. Kohdistusrivin suurinta mittayksikköä käytetään aina.
1. Valitse **Pakkaa yksiköittäin** -kentässä nimikkeen mittayksikkö, joka edustaa konttia. Voit esimerkiksi määrittää, että tapaus on kontti. Jos pakkaat mukaan mittayksikön, et voi myöskään määrittää konttiryhmää koska mittayksikkö on kontti.
1. Valitse **Kontin pakkausstrategia** -kenttään käytettävä pakkausstrategia. Käytettävissä ovat seuraavat asetukset:

    > [!NOTE]
    > Strategia koskee vain myynnin kohdistusrivejä ja siirron kohdistusrivejä.

      - **Pakkaa kaikkiin avoimiin kontteihin** – Järjestelmä arvioi, sopiiko kohdistusrivi mihinkään konttiinpakkausjakson aikana luotuun konttiin.
      - **Pakkaa vain nykyiseen konttiin** – Järjestelmä arvioi vain, sopiiko kohdistusrivi viimeksi luotuun konttiin.

    Lisätietoja ja esimerkkejä konttien pakkausstrategioiden käytöstä on kohdassa [Säilön pakkausstrategiat](container-packing-strategy-overview.md).

1. Valitsemalla **Yhdistämislogiikan keskeytykset** voit määrittää sääntöjä pakkauksen kohdistusriveille konteissa. Voit esimerkiksi luoda säännön, joka antaa työntekijöiden pakata kohdistusrivejä kahdelle eri nimikkeelle samassa kontissa. Voit määrittää yhdistämissäännön seuraavasti:

    1. Valitse **Yhdistämislogiikan keskeytykset** -sivulla **Uusi**.
    1. Valitse **Taulu**-kentässä taulu, joka sisältää yhdistämislogiikan keskeytyksen ehtona käytettävän kentän.
    1. Valitse **Kentän valinta** -kentässä yhdistämislogiikan keskeytyksen ehtona käytettävä kenttä.
    1. Toista nämä vaiheet, kunnes olet lisännyt kaikki yhdistämislogiikan taukokriteerit.

    > [!NOTE]
    > Jos käytät yhdistämislogiikkaa, on suositeltavaa lajitella samojen kyselyn suodattimen ehtokenttien mukaan. Tämä vähentää luotujen konttien määrää.
