---
title: "Tilausilmoitusten näyttäminen myyntipisteessä (POS)"
description: "Tässä ohjeaiheessa käsitellään tilausilmoitusten ottamista käyttöön myyntipisteessä ja ilmoituskehikkoa. Kehittäjät voivat jatkossa laajentaa nämä ilmoitukset tilausten täyttämistoimintojen lisäksi muihin toimintoihin."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41f16d13051f6095bdb04af1586ec06fe0ce93f6
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Tilausilmoitusten näyttäminen myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

Nykyaikaisessa vähittäismyyntiympäristössä myyjillä on monenlaisissa tehtäviä, kuten asiakaspalvelua, tapahtumien kirjaamista, inventointia ja tilausten vastaanottamista myymälässä. Myyntipisteen asiakasohjelma auttaa myyjiä tekemään nämä tehtävät ja paljon muuta yhdessä sovelluksessa. Koska myyjien on tehtävä päivän aikana monenlaisia tehtäviä, heille on ehkä erikseen ilmoitettava, jos heidän on hoidettava jokin tehtävä. Myyntipisteen ilmoituskehikko ratkaisee tämän ongelman niin, että jälleenmyyjät voivat määrittää roolipohjaisia ilmoituksia. Microsoft Dynamics 365 for Retailin sovelluspäivityksessä 5 nämä ilmoitukset voidaan määrittää vain myyntipistetoiminnoille.

Tällä hetkellä järjestelmä näyttää vain tilausten täyttämistoimintojen ilmoitukset. Koska kehikko on kuitenkin suunniteltu laajennettavaksi, kehittäjät voivat jatkossa kirjoittaa ilmoituskäsittelijän mille tahansa toiminnolle ja näyttää kyseisen toiminnon ilmoitukset myyntipisteessä.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Tilauksen täyttämistoimintojen ilmoitusten ottaminen käyttöön

Voit ottaa tilauksen täyttämistoimintojen ilmoituksen käyttöön seuraavasti.

1. Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Toiminnot**.
2. Etsi **Tilauksen täyttäminen** -toiminto ja valitse sen **Ota ilmoitukset käyttöön** -valintaruutu. Tämä määrittää, että ilmoituskehikon on tarkkailtava tämän toiminnon käsittelijää. Jos käsittelijä otetaan käyttöön, tämän toiminnon ilmoitukset näytetään sitten myyntipisteessä.
3. Valitse **Vähittäismyynti** &gt; **Työntekijät** &gt; **Työntekijät** &gt; ja avaa Vähittäismyynti-välilehdessä kyseiseen työntekijään liitetyt myyntipisteen käyttöoikeudet Laajenna **Ilmoitukset**-pikavälilehti, lisää **Tilauksen täyttäminen** -toiminto ja valitse **Näyttöjärjestys**-kentän arvoksi **1**. Jos ilmoituksia määritetään useita, ilmoitukset järjestetään tässä kentässä. Ilmoitukset, joiden **Näyttöjärjestys**-arvo on pienempi, näkyvät niiden ilmoitusten yläpuolella, joilla on suurempi arvo. Ilmoitukset, joiden **Näyttöjärjestys**-arvo on **1**, ovat ylimpänä.

    Vain niiden toimintojen ilmoitukset näytetään, jotka on lisätty **Ilmoitukset**-pikavälilehdessä. Voit lisätä toimintoja vain, jos kyseisten toimintojen **Ota ilmoitukset käyttöön** -valintaruutu on valittu **POS-toiminnot**-sivulla. Lisäksi toiminnon ilmoitukset näytetään työntekijöille vain, jos toiminto on lisätty kyseisten työntekijöiden myyntipisteen käyttöoikeuksiin.

    > [!NOTE]
    > Ilmoitukset voidaan ohittaa käyttäjätasolla. Avaa työntekijän tietue, valitse **Myyntipisteen käyttöoikeudet** ja muokkaa käyttäjän ilmoitusten tilausta.

4. Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **POS-profiilit** &gt; **Toimintoprofiilit**. Määritä **Ilmoitusväli**-kentässä, kuinka usein ilmoitukset noudetaan. Joissakin ilmoituksissa myyntipisteestä on tehtävä reaaliaikaisia soittoja taustasovellukseen. Nämä soitot kuluttavat taustasovelluksen tietojenkäsittelykapasiteettia. Ilmoitusväliä määritettäessä onkin tämän vuoksi harkittava liiketoiminnan tarpeita ja mietittävä, miten reaaliaikaiset soitot vaikuttavat taustasovellukseen. Arvo **0** (nolla) poistaa ilmoitukset käytöstä.
5. Siirry kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**. Synkronoi ilmoituksen tilausasetukset valitsemalla **1060** (**Henkilökunta**) ja valitse sitten **Suorita nyt**. Synkronoi seuraavaksi käyttöoikeusväli valitsemalla **1070** (**Kanavan konfigurointi**) ja valitse sitten **Suorita nyt**.

## <a name="view-notifications-in-the-pos"></a>Ilmoitusten tarkastelu myyntipisteessä

Kun edellä olevat vaiheet on tehty, työntekijät voivat katsoa ilmoituksia myyntipisteessä. Voit tarkastella ilmoituksia napsauttamalla ilmoituskuvaketta myyntipisteen oikeassa yläkulmassa. Avautuvassa ilmoituskeskuksessa näkyy tilauksen täyttämistoiminnon ilmoitukset. Seuraavien tilauksen täyttämistoiminnon ryhmien pitäisi näkyä ilmoituskeskuksessa:

- **Nouto myymälästä** – Tämä ryhmä näyttää niiden tilausten määrän, joiden toimitustapa on **Nouto** ja joiden nouto on aikataulutettu nykyisestä myymälästä. Voit avata **Tilauksen täyttäminen** -sivun painalla ryhmän numeroa. Tässä tapauksessa sivu suodatetaan siten, että se näyttää vain tilaukset, jotka on määritetty noudettaviksi nykyisestä myymälästä.
- **Myymälästä lähetys** – Tämä ryhmä näyttää niiden tilausten määrän, joiden toimitustapa on **Lähetys** ja joiden lähetys on aikataulutettu nykyisestä myymälästä. Voit avata **Tilauksen täyttäminen** -sivun painalla ryhmän numeroa. Tässä tapauksessa sivu suodatetaan siten, että se näyttää vain tilaukset, jotka on määritetty lähetettäväksi nykyisestä myymälästä.

Kun myymälään on määritetty täyttäväksi uusia tilauksia, muuttuva ilmoituskuvake ilmoittaa uusista ilmoituksista ja vastaavien ryhmien määrät päivittyvät. Vaikka ryhmät päivitetään säännöllisesti, myyntipistekäyttäjät voivat päivittää ryhmät koska tahansa manuaalisesti valitsemalla **Päivitä**-painikkeen ryhmän vieressä. Ja jos ryhmässä on uusi nimike, jota nykyinen käyttäjä ei ole katsonut, ryhmän purskekuvake ilmoittaa uudesta sisällöstä.

## <a name="enable-live-content-on-pos-buttons"></a>Live-sisällön ottaminen käyttöön POS-painikkeilla

POS-painikkeissa voi nyt näkyä lukua, joiden avulla työntekijöiden on helppo päätellä, mitkä tehtävät on tehtävä heti. Jos haluat, että tämä luku näkyy POS-painikkeessa, aiemmin tässä ohjeaiheessa selityt ilmoitusasetukset on tehtävä. (Toiminnon ilmoitukset on siis otettava käyttöön, ilmoitusväli määritettävä ja työntekijän myyntipisteen käyttöoikeusryhmä on päivitettävä.) Lisäksi on sinun on avattava painikeruudukon suunnittelutoiminto, tarkasteltava painikkeen ominaisuuksia ja valittava **Ota live-sisältö käyttöön** -valintaruutu. Voit valita **Sisällön tasaus** -kentässä, näkyykö luku painikkeen oikeassa yläkulmassa (**Ylös oikealle**) vai keskellä (**Keskelle**).

> [!NOTE]
> Live-sisältö voidaan ottaa toiminnoille käyttöön vain, jos **Ota ilmoitukset käyttöön** -valintaruutu on valittu niille **POS-toiminnot**-sivulla aiemmin tässä ohjeaiheessa kuvatulla tavalla.

Seuraavassa kuvassa on live-sisällön asetukset painikeruudukon suunnittelutoiminnossa.

![Painikeruudukon suunnittelutoiminnon Live-sisällön asetukset](./media/ButtonGridDesigner.png "Painikeruudukon suunnittelutoiminnon Live-sisällön asetukset")

Seuraavassa kuvassa näytetään, miten **Sisällön tasaus** -kentän **Ylös oikealle**- tai **Keskelle**-vaihtoehdon valinta vaikuttaa eri kokoisiin painikkeisiin.

![POS-painikkeiden live-sisältö](./media/ButtonsWithLiveContent.png "POS-painikkeiden live-sisältö")

