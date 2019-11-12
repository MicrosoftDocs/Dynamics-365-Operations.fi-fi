---
title: Kulutuksen rekisteröinti
description: Tässä ohjeaiheessa kerrotaan, kuinka kulutus rekisteröidään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f14a1cbd016335b857fdff1147740b27d5c765
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653320"
---
# <a name="register-consumption"></a>Kulutuksen rekisteröinti

[!include [banner](../../includes/banner.md)]

 

Kun kunnossapitotyö on suoritettu työtilaukselle, seuraavaksi tehdään kulutusrekisteröinnit ja kirjataan kirjauskansiot. Voit tehdä rekisteröintejä seuraaville kulutustyypeille: tunnit, nimikkeet ja kulut. Eri kulutustyypit rekisteröidään ja kirjataan **Työtilauksen kirjauskansiot** -sivulla. **Resurssien hallinnan** kirjauskansion asetuksia käytetään luotaessa ja kirjattaessa erillisiä tunteja, nimikkeitä ja kuluja koskevia kirjauskansioita **Projektinhallinta ja kirjanpito** -moduulissa.

Joissakin tapauksissa voit lisätä tai poistaa työtilauksen ennusterivejä. Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata kirjauskansiorivejä. Lue lisää työtilausten elinkaaritiloista ja niihin liittyvistä projektin vaiheista kohdassa [Integrointi projektinhallintaan ja kirjanpitoon](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Kirjauskansioiden automaattisen kirjauksen voi määrittää työtilauksen elinkaaritilalle. Lisätietoja on kohdassa [Työtilauksen elinkaaren tilat](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus ja valitse **Kirjauskansiot**.

3. Siirrä kaikki työtilaukseen mahdollisesti liitetyt ennusterivit valitsemalla **Kopioi ennusteesta**. Voit valita, mitkä kulutustyypit haluat siirtää.

4. Tarvittaessa voit lisätä kulutusrivejä asianmukaiseen pikavälilehteen valitsemalla **Lisää rivi** ja täyttämällä rivin tiedot.

5. Valitse **Vahvista kirjauskansiot** vahvistaaksesi kirjauskansiorivit ennen kirjaamista.

6. Kirjaa kirjauskansion rivit valitsemalla **Kirjaa kirjauskansiot**.

7. Kun olet kirjannut kulutuksen kirjauskansiot, voit päivittää työtilauksen elinkaaren tilan. Voit esimerkiksi päivittää työtilauksen elinkaaren tilaksi "Päättynyt", kun se on suoritettu loppuun.

    - Valitse **Työtilauksen kirjauskansiot** -sivun yläosassa olevasta **Näytä**-kentästä, mitä kirjauskansiorivejä haluat tarkastella: **Kaikki**, **Ei kirjattu** tai **Kirjattu**. Kirjatuilla kirjauskansiolla on rasti **Kirjattu**-valintaruudussa.  
    - Kun nimikerivit luodaan työtilauskirjauskansiossa, nimikkeeseen liittyvät tuotedimensiot ja seurantadimensiot siirretään automaattisesti kirjauskansion riville.  

Alla oleva kuvakaappaus näyttää esimerkin tunti- ja nimikerekisteröinneistä työtilaukselle kohdassa **Työtilauksen kirjauskansiot**.

![Kuva 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Jaa työtilausten tunnit useisiin työtilaustöihin

Jos työtilaus sisältää useita työtilaustöitä, voit rekisteröidä työtunnit käyttämällä **Jaa tunnit** -toimintoa eli yksi tuntien rekisteröintirivi voidaan jakaa tasaisesti kullekin työtilaustyölle.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus ja valitse **Kirjauskansiot**.

3. Valitse jaettava tuntikirjausrivi ja valitse sitten **Jaa tunnit.**

4. **Jaa työtilauksen ylläpitotöiden tunnit** -valintaikkunassa näkyy automaattisesti **Työntekijä**-kentässä sisäänkirjautuneen työntekijän nimi. Voit valita toisen työntekijän tarvittaessa.

5. Valitse tuntirekisteröintien luokka **Luokka** -kentässä.

6. Lisää jaettavat työtunnit **Tunnit** -kenttään.

    ![Kuva 2](media/02-consumption.png)

7. Valitse **OK**.

*Esimerkki:* Alla olevassa kuvakaappauksessa näytetään kolme työtilaustyötä sisältävän työtilauksen kirjauskansiorivit. Ensimmäinen rivi, joka sisältää kolme työtuntia, on jaettu, ja kullekin työtilaustyölle rekisteröidään yksi työtunti. Kun kolmen tunnin kirjausrivit on luotu, voit päättää, mitä haluat tehdä alkuperäiselle tuntikirjausriville (esimerkin ensimmäinen rivi). Voit pitää sen sellaisena kuin se on tai poistaa sen. 

![Kuva 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Kulutusrekisteröintien taloushallinnon dimensiot

Kun teet kulutusmerkintöjä, eri rekisteröintityyppeihin liittyvät taloushallinnon dimensiot lisätään rekisteröinteihin tietyssä järjestyksessä. 

- *Tunti- ja kulurekisteröinnit* : Ensin lisätään kirjauskansion otsikon taloushallinnon dimensiot, jos sellaisia on. Seuraavaksi lisätään liittyvän työtilausprojektin taloushallinnon dimensiot. Lopuksi lisätään resurssin (työntekijän) taloushallinnon dimensiot.

- *Nimikerekisteröinnit* : Ensin lisätään kirjauskansion otsikon taloushallinnon dimensiot, jos sellaisia on. Sitten lisätään liittyvän työtilausprojektin taloushallinnon dimensiot. Seuraavaksi lisätään toimipaikan taloushallinnon dimensiot. Lopuksi lisätään nimikkeen taloushallinnon dimensiot.

>[!NOTE]
>Kaikkien kolmen kirjaustyypin osalta taloushallinnon dimensioyhdistelmä tarkistetaan ja virheelliset yhdistelmät poistetaan. Tämä on vakiomääritys muissa Finance and Operations -sovelluksissa.

