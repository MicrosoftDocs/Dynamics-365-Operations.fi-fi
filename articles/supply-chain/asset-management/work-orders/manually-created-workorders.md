---
title: Manuaalisesti luodut työtilaukset
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan manuaalisesti käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875629"
---
# <a name="manually-created-work-orders"></a>Manuaalisesti luodut työtilaukset

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Voit luoda työtilauksia manuaalisesti kahdella tavalla:

- kohdassa **Kaikki työtilaukset** ta **Aktiiviset työtilaukset**  
- kohdassa **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**  

## <a name="create-work-order"></a>Luo työtilaus

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse **Uusi**-painike.

3. Valitse avattavasta **Luo työtilaus** -luettelosta työtilauksen tyyppi.

4. Valitse kuvaus tarvittaessa.

5. Valitse työtilauksen resurssi sekä ylläpitotyön tyyppi.

>[!NOTE]
>Kun valitset resurssin, käytettävissä voi olla kolme välilehteä: **Omat resurssit** -väliehti sisältää resurssit, jotka liittyvät toiminnallisiin sijainteihin, joihin sinut voidaan (järjestelmään kirjautuneena kunnossapitotyöntekijänä) kohdistaa (määritetään kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md)). Jos [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md) -kohdassa ei ole määritetty toiminnallisia sijainteja työntekijälle, **Omat resurssit** -välilehti ei ole näkyvissä. **Aktiiviset resurssit** -välilehti sisältää luettelon kaikista resursseista, joiden elinkaaritila on Aktiivinen. **Resurssinäkymä** -väli ehdessä näkyy puunäkymä toiminnallisista sijainneista ja näihin sijainteihin asennetuista resursseista.

6. Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Toimiala**.

7. Jos tarpeen, voit muuttaa työtilauksen palvelutasoa **Palvelutaso**-kentässä.

8. Valitse liittyvissä kentissä odotetut alkamis- ja päättymispäivämäärät.

9. Luo uusi työtilaus valitsemalla **OK**.

10. Muokkaa työtilausta kohdassa **Kaikki työtilaukset** tarpeen mukaan.

- **Kaikki työtilaukset** -kohdassa voit lisätä useita käyttökohteita työtilaukseen Tiedot-näkymässä lisäämällä rivejä **Työtilauksen ylläpitotyöt** -pikavälilehteen. Voit valita resurssille vain ylläpitotyölajit, jotka liittyvät käyttöomaisuuserälle määritetyn resurssityypin asetuksiin.  
- Jos olet muuttanut käyttöomaisuuden palvelutasoa tai käyttöomaisuuden kriittisyyttä sen jälkeen, kun olet käyttänyt niitä työtilauksessa (katso lisätietoja kohdassa [Resurssien palvelutasot](../setup-for-objects/object-priorities.md) ja [Resurssien kriittisyydet](../setup-for-objects/object-criticalities.md)), työtilauksen palvelutasoa tai kriittisyyttä ei päivitetä vastaavasti.
- Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilausivi lisätään työtilaukseen tai poistetaan siitä.
- **Kaikki työtilaukset** -näkymän **Otsikko**-näkymän **Ajoita**-pikavälilehdessä voit valita vastuullisen huoltotyöntekijäryhmän tai vastuulisen kunnossapitotyöntekijän **Vastuullinen ryhmä**- tai **Vastuuhenkilö**-kentissä. Näitä asetuksia voidaan muuttaa niin kauan kuin työtilaus on aktiivinen – esimerkiksi silloin, kun työtilauksen elinkaaren tila muuttuu. Työtilauksen luonnin yhteydessä tehtävä automaattinen valinta perustuu **Vastaavat ylläpitotyöntekijät** -asetuksiin. Jos lisäät tai poistat työtilaustöitä työtilauksen luomisen jälkeen ja **Vastaava ryhmä** -kenttä ja **Vastuuhenkilö**-kenttä ovat tyhjiä, kun päivität työtilauksen, käyttöomaisuuden hallinta etsii mahdollisen vastineen asetuslomakkeesta vastuulliskesi huoltotyöntekijäryhmäksi tai vastaavaksi kunnossapitotyöntekijäksi. Jos **Vastuuryhmä**-kenttä tai **vastuuhenkilö**-kenttä on jo täytetty, kun päivität työtilauksen, muutoksia ei tehdä. 

- **Ylläpidon tila** -kohdassa saat laskennan avulla saat yleiskuvan saapuvien ja suoritettujen työtilausten kuormituksesta.  

- Lisää maantieteelliset koordinaatit työtilaustyössä valitulle käyttöomaisuudelle **Rivin tiedot** -pikavälilehden **Leveysaste**- ja **Pituusaste**-kenttien avulla.  

## <a name="create-related-work-order"></a>Luo tähän liittyvä työtilaus

Voit luoda liittyvän työtilauksen aiemmin luotuun työtilaukseen, jos haluat käyttää esimerkiksi ensisijaisia ja toissijaisia työtilauksia. Uusi työtilaus perustuu aiemmin luodun työtilauksen työtilaustyöhön.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, jolle haluat tehdä liittyvän työtilauksen.

3. Valitse **Liittyvä työtilaus**.

4. Valitse avattavasta **Luo liittyvä työtilaus** -valintaikkunasta työtilaustyö, jolle haluat luoda liittyvän työtilauksen **Työtilauksen työ** -kentässä.

5. Valitse ylläpitotyön tyyppi **Ylläpitotyön tyyppi** -kentässä ja tarvittaessa liittyvä kunnossapitotöiden tyypin variantti ja toimiala **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä.

6. Jos kyseessä on ensimmäinen liittyvä työtilaus, napsauta **Uusi työtilaus** -valintanappia.

7. Valitse **Työtilauksen tyyppi** ja **Kuvaus** liittyvissä kentissä.

8. Jos tarpeen, muuta työtilauksen palvelutasoa **Palvelutaso**-kentässä.

9. Lisää liittyvissä kentissä odotetut alkamis- ja päättymispäivämäärät.

10. Valitse **OK**. Uusi liittyvä työtilaus näkyy **Kaikki työtilaukset** -luettelossa.

11. Jos luot työtilaukseen liittyvän työtilauksen, johon on jo liitetty työtilauksia, voit lisätä työtilaustyön jo liittyvään työtilaukseen. Tämän voi tehdä valitsemalla vaiheessa 6 **Lisää liittyvään työtilaukseen** -valintanappi. Tämän jälkeen voit valita liittyvän työtilauksen, johon haluat lisätä uuden työtilaustyön. Muokkaa **Palvelutaso**-, **Odotettu aloitus**- ja **Odotettuja loppu** -kenttiä tarpeen mukaan ja valitse **OK**. Työtilauksen työ lisätään aiemmin luotuun työtilaukseen.


![Kuva 1](media/03-work-orders.png)

**Huomautus:** Jos olet määrittänyt liittyvän työtilauspeitteen **Resurssienhallinnan parametrit** > **Työtilaukset** -linkki > **Liittyvän työtilauksen peite** -kentässä, työtilaustunnukset luodaan peitteen asetusten mukaisesti. Jos liittyvää työtilauksen peitettä ei ole määritetty, seuraavaa käytettävissä olevaa työtilaustunnusta käytetään liittyvissä työtilauksissa.

## <a name="copy-work-order"></a>Kopioi työtilaus

Uuden työtilauksen voi luoda nopeasti aiemmin luodusta työtilauksesta. Tämä työtilausten käsittelytapa eroaa ylläpitosuunnitelmiin perustuvien työtilausten luonnista. Siitä on hyötyä esimerkiksi silloin, kun työtilaus sisältää useita työtilaustöitä, joissa on erilaisia töitä, jotka on suoritettava säännöllisin väliajoin.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, josta haluat kopioida sisältöä.

3. Valitse **Kopioi työtilaus**. Näkyviin tulee valitun työtilauksen asetukset. Voit tarvittaessa muokata joitakin kenttiä.

4. Luo uusi työtilaus valitsemalla **OK**.

5. Muokkaa työtilausta kohdassa **Kaikki työtilaukset** tarpeen mukaan.

>[!NOTE]
>Kun uusi työtilaus luodaan, osa tiedoista kopioidaan suoraan olemassa olevasta työtilauksesta. Ennusteita, työkaluja, ylläpidon tarkistuslistoja, toiminnallista sijaintia, osoitteita ja aikataulutusta koskevia tietoja ei kopioida, vaan ne alustetaan käyttöomaisuuden hallinnan nykyisistä asetuksista. Tämä merkitsee, että jos näihin tietoihin tehdään muutoksia ensimmäisen työtilauksen luomisajan kohdan jälkeen siihen saakka, kun työtilauksen kopio on tehty, muutokset sisällytetään uuteen työtilaukseen, jonka olet luonut. Esimerkkejä ovat ennusteiden tai päivitettyjen huoltotarkistusluetteloiden muutokset.


![Kuva 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Työtilauksen luominen ylläpitopyynnön perusteella

1. Valitse **Resurssien hallinta**  >  **yhteiset**  >  **Ylläpitopyynnöt**  >  **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt**.

2. Valitse ylläpitopyynnöt, joille haluat luoda työtilauksen, ja valitse sitten **Muokkaa**.

3. Valitse kohdassa **Kaikki pyynnnöt** **Työtilaus**.

4. Täytä avattava **Työtilaus**-luettelo. Jos kunnossapitotyön tyyppi on valittu ylläpitopyynnössä, voit tarvittaessa valita toisen kunnossapitotyön tyypin, kun luot työtilauksen.

5. Valitse **OK**. Näkyviin tulee sanoma, jossa ilmoitetaan, että työtilaus on luotu.

6. Jos haluat nähdä, mitkä työtilaukset on liitetty ylläpitopyyntöön, valitse ylläpitopyyntö kohdassa **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** ja valitse **Työtilaukset**-painike.


![Kuva 3](media/05-work-orders.png)


>[!NOTE]
>Työtilauksia voi luoda automaattisesti myös määrittämällä ylläpitosuunnitelman työt aikataulutuksen mukaan tai määrittämällä käyttöomaisuuserän huoltosuunnitelmat tai ylläpitokierrokset. **Ylläpitoaikataulu**-kohdassa lylläpitopyynnöistä uodut työtilaukset luodaan ylläpitopyynnöissä valituilla kunnossapitotöiden tyypeillä.

