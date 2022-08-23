---
title: Kanavien välisen jakamisen ottaminen käyttöön ja käyttäminen
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -sivustonmuodostimen kanavienvälisen jakamistoiminnon ottamista käyttöön ja sen käyttämistä.
author: josaw1
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: c05da17327e61d6f61883ab97a403bf2cf8a68f1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270070"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Kanavien välisen jakamisen ottaminen käyttöön ja käyttäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -sivustonmuodostimen kanavienvälisen jakamistoiminnon ottamista käyttöön ja sen käyttämistä.

Kanavienvälisen jakamisen ansiosta vähittäismyyjät voivat käyttää sisältöä uudelleen ja jakaa sen sivuston kanavien kesken. Tämä on kätevä ominaisuus, jos sivustokanavilla on yhteensopiva peruskieli ja jos niillä on useita yhteisiä sisältökohteita.

Kanavienvälisen jakamiseen tarvitaan oletuskanava, josta haetaan käytettävissä olevaa sisältöä, kun pyydetyn sisällön kanavakohtaista versiota ei löydy. Kanavien välillä jaettavaksi tarkoitettu sisältö luodaan oletuskanavassa. Sisältö voidaan lokalisoida mille tahansa kielelle, jota käytetään jossakin sivustokanavassa.

## <a name="when-to-use-cross-channel-sharing"></a>Kanavienvälisen jakamisen käyttötilanteet

Kanavienvälinen jakaminen on hyödyllistä silloin, kun useat kanavat voivat jakaa sisältöä samassa sivustossa. Esimerkiksi vähittäismyyjä, jolla on useita yhteen sivustoon ryhmiteltyjä brändejä ja myymälöitä, voi jakaa osan sisällöstä joidenkin tai kaikkien myymälöiden kanssa. Tämä jaettu sisältö voi sisältää käyttöehtojen, maksuehtojen, toimitustapojen ja usein kysyttyjen kysymysten sivuja.

Kanavienvälinen jakaminen tukee myös osia. Tämän vuoksi kanavakohtaisia osia sisältävä sivu voidaan luoda kanavienvälisenä sisältönä. Vaikka tässä tapauksessa suurin osa sisällöstä jaetaan kanavien kesken, kanavienvälisen sivun kanavakohtaiset osat hahmonnetaan vain, kun niitä pyydetään vastaavasta myymäläkanavasta.

Kanavienvälisestä jakamisesta ei ole hyötyä sivustoissa, joissa on vain yksi kanava, tai sivustoissa, joissa on useita kanavia mutta jotka eivät voi jakaa sisältöä.

## <a name="enable-cross-channel-sharing"></a>Kanavienvälisen jakamisen käyttöönottaminen

Kanavienvälinen jakaminen otetaan käyttöön sivustotasolla. Tämä toiminto on yksisuuntainen. Niinpä kun kanavienvälinen jakaminen otetaan käyttöön, sitä ei voi poistaa käytöstä.

Kanavienvälinen jakaminen otetaan käyttöön Commercen sivustonmuodostimessa seuraavasti:

1. Valitse **Sivuston asetukset \> Ominaisuudet**.
1. Määritä **Kanavienvälinen**-ominaisuuden asetukseksi **Käytössä**.

    ![Kanavienvälinen-asetus käytössä Commerce-sivuston luontiohjelmassa.](./media/enabling-cross-channel-sharing.png)

Kun kanavienvälinen jakaminen on otettu käyttöön, kanavienväliset tiedot näkyvät **Kanavat**-osan kohdassa **Sivuston asetukset \> Ominaisuudet**, kuten seuraavassa kuvassa.

![Kanavat tiedot näkyvissä kanavienvälisen jakamisen käyttöönoton jälkeen.](./media/channels-cross-channel.png)

Lisäksi sen jälkeen kun kanavienvälinen jakaminen on otettu käyttöön, **Kanava**-kenttä Commerce-sivustonmuodostimen oikeassa yläkulmassa sisältää **Kanavienvälinen verkkokauppa** vaihtoehdon, jolla voi hallita kanavienvälistä sisältöä seuraavassa kuvassa näytetyllä tavalla.

![Kanavienvälinen verkkokauppa -vaihtoehto Kanavat-kentässä kanavienvälisen jakamisen käyttöönoton jälkeen.](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Kanavienvälisen sisällön luominen ja käyttäminen

Voit luoda ja käyttää kanavienvälistä sisältöä monilla tavoilla. Voit esimerkiksi luoda kanavienvälisiä osia, luoda kanavienvälistä ja kanavakohtaista sisältöä käyttäviä kanavienvälisiä sivuja sekä ohittaa kanavienväliset osat osien kanavakohtaisilla versioilla.

### <a name="create-a-cross-channel-fragment"></a>Kanavienvälisen osan luominen

Luo kanavienvälinen osa Commercen sivustonmuodostimessa seuraavasti:

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Uusi osa** -valintaikkunassa **Kampanjapalkki**-moduuli ja anna sitten **Osan nimi** -kohdassa nimi (kuten **Kanavienvälinen palkki**). Valitse sitten **OK**.
1. Valitse **Kampanjapalkki**-moduulin ominaisuusruudussa **Lisää sanoma** ja valitse sitten **Sanoma**.
1. Lisää **Sanoma**-valintaikkunan **Teksti**-kohtaan **Kanavienvälinen** ja valitse sitten **OK**. 
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

Tätä kanavienvälistä osaa voidaan käyttää kanavienvälisillä ja kanavakohtaisilla sivuilla, jotka on luotu jossain sivustokanavassa.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Kanavienvälistä sisältöä käyttävän kanavienvälisen sivun luominen

Kanavienvälisiä sivuja voidaan käyttää missä tahansa sivuston kanavassa. Tämän vuoksi voit luoda jaetun sisältösivun kerran ja tehdä päivitykset jatkossa yhdessä paikassa. Esimerkiksi kanavienvälinen **Käyttöehdot**-sivu, jonka URL-osoite on `/toc`, voidaan jakaa kaikkien sivuston kanavien kanssa. Jos sivustokanavien URL-perusosoitteet ovat `www.fabrikam.com/brand1` ja `www.fabrikam.com/brand2`, sama kanavienvälinen jaettu **Käyttöehdot**-sivu on saatavana molemmissa sivustokanavan URL-osoitteissa (`www.fabrikam.com/brand1/toc` ja `www.fabrikam.com/brand2/toc`). Jos **Käyttöehdot**-sivu on päivitettävä myöhemmin, vain yksi jaettu sivu on päivitettävä.

Voit luoda Commerce-sivustonmuodostimessa kanavienvälistä sisältöä käyttävän kanavienvälisen sivun seuraavasti:

1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa malli, kuten **Markkinointi**.
1. Anna **Sivun nimi** -kenttään sivun nimi (kuten **Kanavienvälinen sivu**).
1. Anna **Sivun URL-osoite** -kenttään sivun URL-osoite (kuten **examplepage**) ja valitse sitten **OK**.
1. Valitse uudella sivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Lisää osa** -valintaikkunassa aiemmin luotu kanavienvälinen osa, jossa on kampanjapalkki, ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Näkyvissä pitäisi olla kampanjapalkki, jossa on teksti Kanavienvälinen.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Kanavienvälistä sisältöä käyttävän kanavakohtaisen sivun luominen

Käyttämällä kanavienvälistä sisältöä kanavakohtaisilla sivuilla voit luoda jaetun sisältöosan kerran ja käyttää sitä sitten kanavakohtaisilla sivuilla. Tämä yhden lähteen käyttäminen on kätevää jaetun sisällön, kuten käyttöehtojen, maksuehtojen tai yhteystietojen, osalta.

Voit luoda Commerce-sivustonmuodostimessa kanavienvälistä sisältöä käyttävän kanavakohtaisen sivun seuraavasti:

1. Valitse tietyssä kanavassa, kuten **Laajennettu Fabrikam-verkkokauppa**, **Sivut** ja luo sitten uusi sivu valitsemalla **Uusi**.
1. Valitse **Valitse malli** -valintaikkunassa malli, kuten **Markkinointi**.
1. Anna **Sivun nimi** -kenttään sivun nimi (kuten **Kanavakohtainen sivu**).
1. Anna **Sivun URL-osoite** -kenttään sivun URL-osoite (kuten **channelspecificpage**) ja valitse sitten **OK**.
1. Valitse uudella sivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Lisää osa** -valintaikkunan **Kanava**-kohdassa **Kanavienvälinen verkkokauppa**. Aiemmin luodun kanavienvälisen osan pitäisi näkyä luettelossa. Valitse ensin se ja sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Näkyvissä pitäisi olla kampanjapalkki, jossa on teksti Kanavienvälinen.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Kanavienvälisen sivun kanavakohtaisen version luominen

Kanavienvälinen jakaminen tukee kanavienvälisen sisällön ohittamista Esimerkiksi yhtä lukuun ottamatta sivuston kanavat jakavat saman sisällön osan. Tämä yksi sivuston kanava tarvitsee eri sisällön. Eri sisältö otetaan siinä käyttöön korvaamalla kanavienvälinen sisältö kanavakohtaisella sisällöllä luomalla kanavakohtainen versio kanavienvälisestä sivusta.

Voit luoda Commerce-sivustonmuodostimessa kanavienvälisen sivun kanavakohtaisen version seuraavasti:

1. Valitse **Kanava**-kentässä oikeassa yläkulmassa **Kanavienvälinen verkkokauppa**.
1. Avaa aiemmin luotu kanavienvälinen sivu.
1. Valitse **Kanava**-kentässä oikeassa yläkulmassa kanava, jolla on oltava oma sisältö. Sivueditorissa näkyy sanoma, joka pyytää luomaan uusi sivuvariantti.
1. Valitse **Luo sivuvariantti**.
1. Valitse sivuvariantin **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kampanjapalkki**-moduuli ja valitse sitten **OK**.
1. Valitse **Kampanjapalkki**-moduulin ominaisuusruudussa **Lisää sanoma** ja valitse sitten **Sanoma**.
1. Lisää **Sanoma**-valintaikkunan **Teksti**-kohtaan **Kanavakohtainen** ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Näkyvissä pitäisi olla kampanjapalkki, jossa on teksti Kanavakohtainen.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

Jos nyt käytät kanavan URL-perusosoitetta ja siirryt kyseisen sivuston kanavienvälisen sivun URL-osoitteeseen, näkyvissä on kanavakohtaista sisältöä eikä kanavienvälistä sisältöä.

## <a name="additional-resources"></a>Lisäresurssit

[Tapoja lisästä sisältöä](add-manage-content.md)

[Sivumallisanasto](page-elements-overview.md)

[Asiakirjan tilat ja elinkaari](document-states-overview.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
