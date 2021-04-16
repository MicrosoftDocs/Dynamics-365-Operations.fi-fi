---
title: Tilausilmoitusten näyttäminen myyntipisteessä (POS)
description: Tässä ohjeaiheessa käsitellään tilausilmoitusten ottamista käyttöön myyntipisteessä ja ilmoituskehikkoa.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7b28a33dff4af6bf2b97db825a5a8304213f3a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796483"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Tilausilmoitusten näyttäminen myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

Myyjille voidaan määrittää myymälässä erilaisia tehtäviä, kuten tilausten täyttäminen tai varaston vastaanottojen tai varaston inventointien suorittaminen. Myyntipisteen asiakasohjelma tarjoaa myyjille yhden sovelluksen, jossa he saavat ilmoituksia näistä tehtävistä. Myyntipisteen ilmoituskehikko ratkaisee tämän ongelman niin, että jälleenmyyjät voivat määrittää roolipohjaisia ilmoituksia. Nämä ilmoitukset voidaan määrittää myyntipistetoimintoihin alkaen Dynamics 365 Retailin sovelluspäivityksestä 5.

Järjestelmä voi näyttää *tilauksen täyttämisen* toiminnon ilmoitukset, ja Commerce-versiosta 10.0.18 ilmoitukset voi näyttää myös *peruuta tilaus* -toiminnolle. Koska kehikko on kuitenkin suunniteltu laajennettavaksi, kehittäjät voivat [kirjoittaa ilmoituskäsittelijän](dev-itpro/extend-pos-notification.md) mille tahansa toiminnolle ja näyttää kyseisen toiminnon ilmoitukset myyntipisteessä.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Tilauksen täyttämis- tai peruutustoimintojen ilmoitusten ottaminen käyttöön

Voit ottaa tilauksen täyttämis- tai peruutustoimintojen ilmoituksen käyttöön seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> Myyntipiste \> Toiminnot**.
1. Etsi **Tilauksen täyttäminen** -toiminto tai **Peruuta tilaus** -toiminto ja valitse toiminnolle **Ota ilmoitukset käyttöön**. Tämä määrittää, että ilmoituskehikon on tarkkailtava tämän toiminnon käsittelijää. Jos käsittelijä otetaan käyttöön, tämän toiminnon ilmoitukset näytetään sitten myyntipisteessä.
1. Siirry kohtaan **Retail ja Commerce \> Työntekijät \> Työntekijät**.
1. Valitse **Commerce**-välilehti, valitse työntekijärivi ja valitse sitten **Myyntipisteen käyttöoikeudet**. Valitse **Ilmoitukset**-pikavälilehti, jos haluat laajentaa sitä, ja lisää sitten toiminnot, joissa olet ottanut ilmoitukset käyttöön. Jos määrität työntekijälle yksittäisen ilmoituksen, varmista, että **Näyttöjärjestys**-arvoksi on määritetty **1**. Jos määrität useita toimintoja, määritä **Näyttöjärjestys**-arvot ilmaisemaan järjestys, jossa ilmoitukset näytetään. 

      Ilmoitukset näkyvät vain **Ilmoitukset**-pikavälilehteen lisätyissä toiminnoissa. Voit lisätä toimintoja tähän vain, jos näille toiminnoille on valittu **Ota ilmoitukset käyttöön** -valintaruutu **Myyntipisteen toiminnot** -sivulla. Lisäksi toiminnon ilmoitukset näytetään työntekijöille vain, jos toiminto on lisätty kyseisten työntekijöiden myyntipisteen käyttöoikeuksiin.

    > [!NOTE]
    > Ilmoitukset voidaan ohittaa käyttäjätasolla. Voit tehdä tämän avaamalla työntekijän tietueen, valitsemalla **Myyntipisteen käyttöoikeudet** ja muokkaamalla käyttäjän ilmoitusten tilausta.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Määritä **Ilmoitusväli**-kentässä, kuinka usein ilmoitukset noudetaan. Joissakin ilmoituksissa myyntipisteestä on tehtävä reaaliaikaisia soittoja taustasovellukseen. Nämä soitot kuluttavat taustasovelluksen tietojenkäsittelykapasiteettia. Ilmoitusväliä määritettäessä onkin tämän vuoksi harkittava liiketoiminnan tarpeita ja mietittävä, miten reaaliaikaiset soitot vaikuttavat taustasovellukseen. Arvo **0** (nolla) poistaa ilmoitukset käytöstä.
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**. Synkronoi ilmoituksen tilausasetukset valitsemalla **1060** (**Henkilökunta**) ja valitse sitten **Suorita nyt**. Synkronoi seuraavaksi käyttöoikeusväli valitsemalla **1070** (**Kanavan konfigurointi**) ja valitse sitten **Suorita nyt**.

## <a name="view-notifications-in-the-pos"></a>Ilmoitusten tarkastelu myyntipisteessä

Kun edellä olevat vaiheet on tehty, työntekijät voivat katsoa ilmoituksia myyntipisteessä. Voit tarkastella ilmoituksia valitsemalla ilmoituskuvakkeen myyntipisteen oikeassa yläkulmassa. Näyttöön tulee ilmoitusruutu, joka sisältää työntekijälle määritettyjen työvaiheiden ilmoitukset. 

**Tilauksen täyttämistoiminnolle** ilmoitusruudun pitäisi näyttää seuraavat ryhmät:

- **Nouto myymälästä** – Tämä ryhmä näyttää niiden yksittäisten tilausrivien määrän, joiden nouto on aikataulutettu nykyisestä myymälästä. Valitsemalla ryhmän numeron voit avata **Tilauksen täyttäminen** -toiminnon suodattimella siten, että siinä näkyvät vain ne aktiiviset tilausrivit, jotka on määritetty nykyisen myymälän noutoa varten.
- **Toimita myymälästä** – Tämä ryhmä näyttää käyttäjän nykyisestä myymälästä lähetystä varten määritettyjen yksittäisten tilausrivien määrän. Valitsemalla ryhmän numeron voit avata **Tilauksen täyttäminen** -toiminnon suodatetussa näkymässä, jossa näkyvät vain ne aktiiviset tilausrivit, jotka on määritetty nykyisestä myymälästä toimitusta varten.

**Tilauksen peruutustoiminnolle** ilmoitusruudun pitäisi näyttää seuraavat ryhmät:

- **Täytettävät tilaukset** – Tässä ryhmässä näkyy niiden tilausten määrä, jotka on konfiguroitu käyttäjän nykyisen myymälän noutoa tai toimitusta varten. Valitsemalla ryhmän numeron voit avata **Peruuta tilaus** -toiminnon suodatetussa näkymässä, jossa näkyvät vain ne avoimet tilaukset, jotka käyttäjän nykyisen myymälän on täytettävä myymälässä noutoa tai myymälästä lähetystä varten.
- **Noudettavat tilaukset** – Tämä ryhmä näyttää niiden tilausten määrän, joiden nouto on aikataulutettu nykyisestä myymälästä. Valitsemalla ryhmän numeron voit avata **Peruuta tilaus** -toiminnon suodatetussa näkymässä, jossa näkyvät vain ne avoimet tilaukset, jotka käyttäjän nykyisen myymälän on täytettävä asiakkaan noutoa varten.
- **Toimitettavat tilaukset** – Tässä ryhmässä näkyvät käyttäjän nykyisestä myymälästä lähetettävät tilaukset. Valitsemalla ryhmän numeron voit avata **Peruuta tilaus** -toiminnon suodatetussa näkymässä, jossa näkyvät vain ne avoimet tilaukset, jotka käyttäjän nykyisen myymälän on täytettävä toimitusta varten.

Sekä tilauksen täyttämiselle että peruuttamiselle, kun prosessi poimii uusia tilauksia, muuttuva ilmoituskuvake ilmoittaa uusista ilmoituksista ja vastaavien ryhmien määrät päivittyvät. Vaikka ryhmät päivitetään säännöllisesti, myyntipistekäyttäjät voivat päivittää ryhmät koska tahansa manuaalisesti valitsemalla **Päivitä** ryhmän vieressä. Ja jos ryhmässä on uusi nimike, jota nykyinen käyttäjä ei ole katsonut, ryhmän purskekuvake ilmoittaa uudesta sisällöstä.

## <a name="enable-live-content-on-pos-buttons"></a>Live-sisällön ottaminen käyttöön POS-painikkeilla

POS-painikkeissa voi nyt näkyä lukua, joiden avulla työntekijöiden on helppo päätellä, mitkä tehtävät on tehtävä heti. Jos haluat, että tämä luku näkyy POS-painikkeessa, aiemmin tässä ohjeaiheessa selityt ilmoitusasetukset on tehtävä. (Toiminnon ilmoitukset on siis otettava käyttöön, ilmoitusväli määritettävä ja työntekijän myyntipisteen käyttöoikeusryhmä on päivitettävä.) Lisäksi on sinun on avattava painikeruudukon suunnittelutoiminto, tarkasteltava painikkeen ominaisuuksia ja valittava **Ota live-sisältö käyttöön** -valintaruutu. Voit valita **Sisällön tasaus** -kentässä, näkyykö luku painikkeen oikeassa yläkulmassa (**Ylös oikealle**) vai keskellä (**Keskelle**).

> [!NOTE]
> Live-sisältö voidaan ottaa toiminnoille käyttöön vain, jos **Ota ilmoitukset käyttöön** -valintaruutu on valittu niille **POS-toiminnot**-sivulla aiemmin tässä ohjeaiheessa kuvatulla tavalla.

Seuraavassa kuvassa on live-sisällön asetukset painikeruudukon suunnittelutoiminnossa.

![Live Content -asetukset painikeruudukon suunnittelussa](./media/ButtonGridDesigner.png "Live Content -asetukset painikeruudukon suunnittelussa")

Jos haluat näyttää ilmoitusten määrän painikkeessa, varmista, että oikea näyttöasettelu päivitetään. Voit määrittää POS-sovelluksen käyttämän näytön asettelun valitsemalla **Asetukset**-kuvakkeen oikeasta yläkulmasta ja huomaamalla **Näytön asettelun tunnuksen** ja **Asettelun tarkkuuden**. Nyt käytettäessä Edge-selainta, siirry **Näytön asettelu** -sivulle, etsi **Näytön asettelun tunnus** ja **Asettelun resoluutio**, jotka on tunnistettu edellä ja valitse **Ota käyttöön Live-sisältö** -valintaruutu. Siirry **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu** ja suorita 1090 (Rekisterit) -työ, joka synkronoi asettelun muutokset.

![POS-järjestelmän käyttämän näyttöasettelun etsiminen](./media/Choose_screen_layout.png "Etsi näyttöasettelut")

Seuraavassa kuvassa näytetään, miten **Sisällön tasaus** -kentän **Ylös oikealle**- tai **Keskelle**-vaihtoehdon valinta vaikuttaa eri kokoisiin painikkeisiin.

![Live-sisältö POS-painikkeilla](./media/ButtonsWithLiveContent.png "Live-sisältö POS-painikkeilla")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
