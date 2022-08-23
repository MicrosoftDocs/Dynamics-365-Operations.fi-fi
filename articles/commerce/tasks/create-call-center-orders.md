---
title: Luo puhelinkeskustilauksia
description: Tässä artikkelissa esitellään esimerkkimenettely, jossa puhelinkeskuksen käyttäjä etsii asiakasta, luo uuden tilauksen, hakee tuotetta ja perii maksun asiakkaalta Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228507"
---
# <a name="create-call-center-orders"></a>Luo puhelinkeskustilauksia

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään esimerkkimenettely, jossa puhelinkeskuksen käyttäjä etsii asiakasta, luo uuden tilauksen, hakee tuotetta ja perii maksun asiakkaalta Microsoft Dynamics 365 Commercessa. Tässä menettelyssä käytetään esittely-yritystä USRT. Tämä on tarkoitettu myyntitilauksia käsittelevälle assistentille. 

## <a name="prerequisites"></a>Edellytykset

Käyttäjä on määritettävä puhelinkeskuksen käyttäjäksi, jotta tämän menettelyn voi suorittaa. Vaihtoehtoisesti Fabrikamin puolivuosittainen luettelo voidaan julkaista vähintään yhdellä lähdekoodilla.

### <a name="add-yourself-as-a-call-center-user"></a>Itsesi lisääminen puhelinkeskuksen käyttäjäksi

Voit lisätä itsesi puhelinkeskuksen käyttäjäksi seuraavasti.

1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.
1. Valitse **Käyttäjät**-kentästä **Kanavan käyttäjät**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Käyttäjätunnus** -kenttään käyttäjätunnuksesi.
1. Syötä **Nimi**-kenttään käyttäjänimesi. Käyttäjänimi voi olla sama kuin käyttäjätunnus.
1. Valitse toimintoruudussa **Tallenna**.
1. Siirry takaisin kohtaan **Retail ja Commerce \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.
1. Valitse puhelinkeskuksen vähittäismyyntikanavan tunnus.
1. Vahvista, että **Ota käyttöön tilausten viimeistely** -asetuksen arvona on **Kyllä**. Jos vaihtoehto ei ole näkyvissä, voit ohittaa tämän vaiheen.

## <a name="complete-the-example-call-center-procedure"></a>Suorita puhelinkeskuksen mallimenettely.

Voit suorittaa puhelinkeskuksen mallimenettelyn noudattamalla seuraavia vaiheita.

1. Valitse **Retail ja Commerce \> Asiakkaat \> Asiakaspalvelu**.
1. Anna **Asiakashaku**-välilehteen hakuehdot, joilla etsit asiakasta. Valitse tässä mallimenettelyssä **Karen**.
1. Valitse **Haku**. Näyttöön tulee **Asiakashaku**-valintaikkuna, jossa näkyvät hakutulokset.
1. Valitse **Karen Bergin** asiakastietue, jonka asiakastili on **2001**, ja valitse sitten **Valitse**.
1. Valitse toimintoruudussa **Uusi myyntitilaus**.
1. Valitse oikealla **Otsikko**-välilehti.
1. Valitse **Toimitus**-pikavälilehden **Toimitustapa**-kentässä **99 vakio**.

    ![Toimitustavan valinta.](../media/Select_Mode_of_Delivery.png)

1. Valitse oikealla **Rivit**-välilehti.
1. Kirjoita uuden myyntirivin uuden rivin **Myyntitilausrivit**-osan **Nimiketunnus**-kenttään nimiketunnus, mitä haluat hakea. Tässä esimerkkimenettelyssä syötä arvo **81327** ja lisää se myyntitilaukseen valitsemalla tuote avattavasta luettelosta.
1. Syötä myyntimäärä **Määrä**-kenttään.
1. Valitse **Lähdekoodi**-kentässä hakemiston lähdekoodi. Jos aktiivisia lähdekoodeja ei ole, voit ohittaa tämän vaiheen.
1. Valitse toimintoruudussa **Valmis**, kun haluat tarkistaa asiakkaan maksun. Tämä toimenpide avaa **Myyntitilauksen yhteenveto** -valintaikkunan, jossa näkyy erääntyvä kokonaissumma. Toimenpide myös käynnistää kaikkien kulujen, kuten lähetyksen ja käsittelyn, laskemisen ja näyttää ne **Myyntitilauksen yhteenveto** -valintaikkunassa.

    ![Valmis-painike.](../media/Complete_button.png)

1. Valitse **Myyntitilauksen yhteenveto** -valintaikkunassa **Maksut**-pikavälilehdessä valitse **Lisää**, kun haluat siepata maksut.

    ![Myyntitilauksen yhteenveto -valintaikkuna.](../media/order_summary.png)

1. Valitse **Lisää asiakkaan maksutiedot** -valintaikkunan **Maksutapa**-kentässä maksutapa. Valitse tässä mallimenettelyssä **Käteinen**.
1. Syötä **Maksun summa** -kenttään maksun summa. Tässä esimerkissä syötä **120,00**, joka on sama kuin **Myyntitilauksen yhteenveto** -valintaikkunassa näkyvä tilauksen saldo. Syöttämällä tämän summan voit määrittää tilauksen kokonaan maksetuksi.
1. Valitse **OK**.
1. Valitse **Lähetä**.

## <a name="additional-resources"></a>Lisäresurssit

[Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](../customize-email-delivery-mode.md)

[Toimitustavan muuttaminen myyntipisteessä](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
