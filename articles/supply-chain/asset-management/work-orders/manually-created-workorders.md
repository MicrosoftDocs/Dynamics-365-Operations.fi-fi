---
title: Manuaalisesti luodut työtilaukset
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan manuaalisesti käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 80593ddaaa5f327513781dbdd4e3163de4212ced
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208106"
---
# <a name="manually-created-work-orders"></a>Manuaalisesti luodut työtilaukset

[!include [banner](../../includes/banner.md)]


Voit luoda työtilauksia manuaalisesti kahdella tavalla:

- Sivulla **Kaikki työtilaukset** tai **Aktiiviset työtilaukset** 
- Sivulla **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt** 

## <a name="create-work-order"></a>Luo työtilaus

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse **Uusi**.

3. Valitse työtilaustyyppi **Luo työtilaus**-valintaikkunan **Työtilaustyyppi**-kentässä.

4. Valitse tarvittaessa **Kuvaus**.

5. Valitse resurssi **Resurssi**-kentässä.

>[!NOTE]
>Kun valitset resurssin, avattavassa **Resurssi**-välilehdellä voi olla käytettävissä kolme välilehteä: 

- **Aktiiviset resurssit** – Tämä välilehti sisältää luettelon kaikista resursseista, joiden elinkaaritila on aktiivinen. 
- **Resurssinäkymä** – Tässä välilehdessä näkyy puunäkymä toiminnallisista sijainneista ja niihin asennetuista resursseista.
- **Omat resurssit** – Tämä välilehti sisältää resursseja, jotka liittyvät niihin toiminnallisiin sijainteihin, joille sinut (järjestelmään kirjautunut työntekijä) voidaan kohdentaa. (Lisätietoja määrityksestä esitetään kohdassa [Ylläpitotyöntekijät ja -työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)Jos työntekijälle ei ole määritetty toiminnallisia sijainteja kohdassa [Ylläpitotyöntekijät ja -työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md), **Omat resurssit** -välilehti ei ole käytettävissä. 

6. Valitse **Ylläpitotyön tyyppi** -kentässä ylläpitotyön tyyppi työtilaukselle.

7. Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Toimiala**.

8. Jos tarpeen, voit muuttaa työtilauksen palvelutasoa **Palvelutaso**-kentässä.

9. Valitse päivämäärät kentissä **Odotettu alku** ja **Odotettu loppu**.

10. Luo työtilaus valitsemalla **OK**.

11. **Kaikki työtilaukset** -luettelosivulla voit muokata työtilausta tarpeen mukaan.

Huomaa seuraavat seikat:

- **Kaikki työtilaukset** -luettelosivun tietonäkymässä voit lisätä useita käyttökohteita työtilaukseen lisäämällä rivejä **Työtilauksen ylläpitotyöt** -pikavälilehteen. Resurssille voi valita vain sellaisia ylläpitotyötyyppejä, jotka on määritetty resurssille vallitulle resurssityypille.  

- Jos muutat resurssin palvelutasoa tai kriittisyyttä sen jälkeen, kun resurssia on käytetty työtilauksessa, työtilauksen palvelutasoa tai kriittisyyttä ei päivitetä vastaavasti. Lisätietoja palvelutasoista ja kriittisyydestä esitetään kohdissa [Resurssien palvelutasot](../setup-for-objects/object-priorities.md) ja [Resurssien kriittisyystyypit](../setup-for-objects/object-criticalities.md).

- Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilaustehtävä lisätään työtilaukseen tai poistetaan siitä.

- Siirry **Kaikki työtilaukset** -tietonäkymän > **Otsikko**-välilehden > **Aikataulu**-pikavälilehteen, jonka kentässä **Vastuuryhmä** tai **Vastuuhenkilö** voit valita vastaavan ylläpitotyöntekijäryhmän tai vastaavan ylläpitotyöntekijän. Näitä asetuksia voi muuttaa, kun työtilaus on aktiivinen. Niitä voi muuttaa esimerkiksi, kun työtilauksen elinkaaren tila muuttuu. Työtilauksen luonnin yhteydessä tehtävä automaattinen valinta perustuu **Vastaavat ylläpitotyöntekijät** -sivun määrityksiin. Jos lisäät tai poistat työtilaustehtäviä työtilauksen luomisen jälkeen ja kentät **Vastuuryhmä** ja **Vastuuhenkilö** ovat tyhjiä, kun päivität työtilauksen, resurssienhallinta etsii määrityssivulta mahdollisen vastineen vastuulliskesi ylläpitotyöntekijäryhmäksi tai vastaavaksi ylläpitopitotyöntekijäksi. Jos kenttä **Vastuuryhmä** tai **Vastuuhenkilö** on jo määritetty, kun päivität työtilauksen, muutoksia ei tehdä. Lisätietoja vastaavista ylläpitotyöntekijöistä ja työntekijäryhmistä esitetään kohdassa [Vastaavat ylläpitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).

- [Ylläpidon tila](../controlling-and-reporting/maintenance-status.md) -sivulla voit suorittaa laskutoimituksen saadaksesi yleiskuvan saapuvien ja suoritettujen työtilausten kuormituksesta.  

- **Kaikki työtilaukset**-sivun tietonäkymän **Rivitiedot**-pikavälilehdessä voit käyttää kenttiä **Leveyspiiri** ja **Pituuspiiri** lisätäksesi maantieteelliset koordinaatit työtilaustehtävässä valitulle resurssille.  


## <a name="create-related-work-order"></a>Luo tähän liittyvä työtilaus

Voit luoda työtilauksen, joka liittyy olemassa olevaan työtilaukseen. Tämä ominaisuus on käytännöllinen, jos esimerkiksi haluat käyttää ensisijaisia ja toissijaisia työtilauksia. Uusi työtilaus perustuu aiemmin luodun työtilauksen työtilaustyöhön.

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, jolle luodaan liittyvä työtilaus.

3. Valitse toimintoruudun **Työtilaus**-välilehden **Uusi**-ryhmässä **Liittyvä työtilaus**.

4. Valitse avattavasta **Luo liittyvä työtilaus** -valintaikkunan **Työtilaustehtävä** -kentässä työtilaustehtävä, jolle haluat luoda liittyvän työtilauksen.

5. Valitse ylläpitotyön tyyppi **Ylläpitotyön tyyppi** -kentässä.

6. Valitse **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä tarpeen mukaan ylläpitotyön tyypin variantti ja toimiala.

7. Jos tämä työtilaus on ensimmäinen valitulle työtilaukselle luotu liittyvä työtilaus, toimi seuraavasti:
    1. Valitse **Uusi työtilaus**.
    2. Valitse **Työtilaustyyppi**-kentässä työtilauksen tyyppi.
    3. Syötä **Kuvaus**-kenttään kuvaus.
    4. Muuta tarvittaessa työtilauksen palvelutasoa **Palvelutaso**-kentässä.
    5. Valitse alkamis- ja päättymispäivämäärät kentissä **Odotettu alku** ja **Odotettu loppu**.
    6. Valitse **OK**. Uusi liittyvä työtilaus näkyy **Kaikki työtilaukset** -luettelosivulla.  

8. Jos työtilauksella, jolle luot liittyvää työtilausta, on jo liittyviä työtilauksia, lisää olemassa olevaan liittyvään työtilaukseen uusi työtilaustehtävä seuraavalla tavalla:
    1. Valitse **Lisää liittyvään työtilaukseen**.
    2. Valitse **Työtilaus**-kentässä se liittyvä työtilaus, jolle lisätään uusi työtilaustehtävä.
    3. Muuta tarvittaessa työtilauksen palvelutasoa **Palvelutaso**-kentässä.
    4. Muuta tarvittaessa odotettuja alkamis- ja päättymispäivämääriä kentissä **Odotettu alku** ja **Odotettu loppu**.
    5. Valitse **OK**. Työtilauksen työ lisätään aiemmin luotuun työtilaukseen.

Seuraavassa kuvassa on esimerkki **Luo liittyvä työtilaus** -valintaikkunasta.

![Kuva 1](media/03-work-orders.png)

>[!NOTE]
>Jos olet määrittänyt liittyvän työtilauspeitteen kentässä **Resurssienhallinnan parametrit** > **Työtilaukset** > **Liittyvä työtilauspeite**, työtilaustunnukset luodaan peitemäärityksen mukaisesti. Jos liittyvää työtilauksen peitettä ei ole määritetty, seuraavaa käytettävissä olevaa työtilaustunnusta käytetään liittyvissä työtilauksissa.

## <a name="copy-a-work-order"></a>Työtilauksen kopiointi

Uuden työtilauksen voi luoda nopeasti aiemmin luodusta työtilauksesta. Tämä tapa käyttää työtilauksia eroaa työtilausten luomisesta [ylläpitosuunnitelmien](../preventive-and-reactive-maintenance/maintenance-plans.md) perusteella. Siitä on hyötyä, jos työtilaus esimerkiksi sisältää useita työtilaustehtäviä ja nämä eri tehtävät on suoritettava eri resursseille säännöllisin väliajoin.

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, josta sisältöä kopioidaan.

3. Valitse toimintoruudun **Työtilaus**-välilehden **Uusi**-ryhmässä **Kopioi työtilaus**.

4. Näkyviin tulee valitun työtilauksen asetukset. Voit muokata osaa kentistä tarpeen mukaan.

5. Luo uusi työtilaus valitsemalla **OK**.

6. **Kaikki työtilaukset** -luettelosivulla voit muokata työtilausta tarpeen mukaan.

>[!NOTE]
>Kun uusi työtilaus luodaan, osa tiedoista kopioidaan suoraan olemassa olevasta työtilauksesta. Ennusteita, työkaluja ylläpidon tarkistuslistoja, toiminnallista sijaintia, osoitteita ja aikatauluja koskevia tietoja ei kopioida. Sen sijaan ne perustuvat resurssienhallinnan kulloisiinkin määrityksiin. Siten, jos kyseisiä tietoja on muutettu ensimmäisen työtilauksen luomisen ja työtilauksen kopioinnin välisenä aikana, muutokset sisällytetään uuteen työtilaukseen. Esimerkkejä ovat muutokset ennusteisiin ja päivitykset ylläpidon tarkistuslistoihin.

Seuraavassa kuvassa on esimerkki **Kopioi työtilaus** -valintaikkunasta.

![Kuva 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Työtilauksen luominen ylläpitopyynnön perusteella

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Ylläpitopyynnöt** > **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt**.

2. Valitse ylläpitopyyntö, jolle luodaan työtilaus, ja valitse sitten **Muokkaa**.

3. Valitse toimintoruudun **Ylläpitopyyntö**-välilehden **Uusi**-ryhmässä **Työtilaus**.

4. Määritä kentät **Työtilaus**-valintaikkunassa. Jos ylläpitotyön tyyppi on valittu ylläpitopyynnössä, voit tarvittaessa valita toisen kunnossapitotyön tyypin, kun luot työtilauksen.

5. Valitse **OK**. Saat ilmoituksen työtilauksen luomisesta.

6. Valitsemalla ylläpitopyynnön luettelosivulla **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** voit tarkastella ylläpitopyyntöön liittyviä työtilauksia. Valitse sitten toimintoruudun **Ylläpitopyyntö**-välilehden **Näytä**-ryhmässä **Työtilaukset**.


Seuraavassa kuvassa on esimerkki **Luo työtilaus** -valintaikkunasta.

![Kuva 3](media/05-work-orders.png)


>[!NOTE]
>Työtilauksia voi luoda automaattisesti myös ajoittamalla ylläpitosuunnitelman töitä tai määrittämällä resurssien [ylläpitosuunnitelmien](../preventive-and-reactive-maintenance/maintenance-plans.md) tai [ylläpitokierrosten](../preventive-and-reactive-maintenance/maintenance-rounds.md) automaattinen luonti. **Kaikki ylläpitoaikataulut**-luettelosivulla ylläpitopyynnöistä luoduilla työtilauksilla on ylläpitopyynnöissä valitut ylläpitotyötyypit.

