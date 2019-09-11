---
title: Ennusteet, työtilaukset ja projektit
description: Tässä ohjeaiheessa selitetään ennusteiden ja työtilausten integrointi resurssien hallinnan Projektinhallinta ja kirjanpito -moduulin kanssa.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886813"
---
# <a name="forecasts-work-orders-and-projects"></a>Ennusteet, työtilaukset ja projektit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Resurssien hallinnassa integrointi **Projektinhallinta ja kirjanpito** -moduuliin tehdään, jotta voidaan optimoida kustannusten hallinta, jonka avulla käyttäjät voivat seurata kustannuksia huoltotyön tyyppien ennusteissa ja työtilaustöissä.

Kunnossapitotöiden tyyppien ennusteiden seuraamista varten on tehtävä kaksi asetusta:

1. Valitse projekti kohdassa **Resurssien hallinta** > **Asetukset** > **Resurssienhallinnan parametrit** > **Resurssit** -linkki > **Projekti** -pikavälilehti > **Ylläpitoennusteen projekti** -kenttä.

2. Kun **Ylläpitotyön tyyppien oletus** -kohdassa luot ylläpitotyötyypin oletusrivin, riville luodaan automaattisestitehtävänumero (**Resirssien hallinta** > **Asetukset** > **työt** > **Ylläpitotyön tyyppien oletukset**).

Kunnossapitotöiden tyypin ennusteissa on kaksi tarkoitusta: voit jäljittää ylläpitotyön tyyppien ennusteiden kustannukset **Projektinhallinta ja kirjanpito** -moduulissa. Lisäksi ennusteet siirretään automaattisesti työtilauksen työn projektiin, kun valitset kunnossapitotyön tyypin työtilaustyölle.

Jotta työtilausten töiden kustannukset voidaan jäljittää, on ensin määritettävä työtilausprojektit. Toimenpiteen kuvaus on kohdassa [Työtilauksen projektin määritys](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Työtilauksen työn projektit

Kun työtilaukseen luodaan työtilaustyö, työtilausprojekti määräytyy pääprojektin asetusten mukaan:**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset.**

Työtilauksen työprojektit luodaan seuraavien työtilaustietojen yhdistelmän avulla:

- Työtilauksessa valittu työtilaustyyppi 
- Työtilaustyön käyttöomaisuuteen liittyvä toiminnallinen sijainti
- Työtilaustyön käyttöomaisuuteen liittyvä resurssityyppi  
- Työtilaukseen määritetty odotettu alkamis- ja loppumisaika  

On mahdollista, että kaikkia edellä mainittuja tietoja ei löydy työtilauksesta. Näin ollen työtilauksen pääprojektin haku tehdään käyttämällä käytettävissä olevaa tietoyhdistelmää ja valitsemalla projektitunnus, joka vastaa työtilauksen tietoja.

Esimerkki: Alla olevassa kuvassa käyttöomaisuuden tyypin "Truck Engine" määritys tarkoittaa, että jokainen kyseiselle käyttöomaisuustyypille luotu työtilaustyö on projektitunnuksen "000186" aliprojekti.

![Kuva 1](media/01-integration-to-pma.png)

Työtilaustyön projektitunnuksen ja siihen liittyvän tehtävän numeron (**Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** > valitse työtilaus luettelosta > **rivin tiedot** -pikavälilehti > **Projektitunnus** -kenttä **Tehtävän numero** -kenttä) tarkoitus on seurata työtilaustyöhön liittyviä kustannuksia ja työtilaustyölle valittua käyttöomaisuutta **Projektinhallinta ja kirjanpito** -moduulissa. 

Alla olevassa kuvassa näkyy graafinen yleiskatsaus työtilausprojekteista ja niihin liittyvistä projektitehtävistä.

![Kuva 2](media/02-integration-to-pma.png)

Kun työtilaukseen luodaan uusi työtilaustyö, työtilausprojekti luodaan automaattisesti työlle. Työtilaus työhön liittyvän käyttöomaisuuserän taloushallinnon dimensiot siirretään automaattisesti työtilausprojektiin. Työtilaustyölle luodulle projektitehtävälle on liitetty siihen liittyviä tietoja, jotka koskevat kunnossapitotöiden tyyppiä, kunnossapitotöiden tyypin varianttia ja kauppaa. Näistä tiedoista on hyötyä esimerkiksi silloin, kun luot ostotilauksen työtilauksesta ( katso [Hankinta](../work-orders/procurement.md)) tai jos käytät **Projektinhallinta ja kirjanpito** -moduulia ajan rekisteröintiä varten.  

Jos käyttöomaisuus on asennettu toiminnallisessa sijainnissa ja kyseinen käyttöomaisuuserä on myöhemmin asennettu toiseen toimintosijaintiin, uuteen toimintosijaintiin liittyvät taloushallinnon dimensiot päivitetään automaattisesti käyttöomaisuuserälle. Kun luot käyttöomaisuudelle työtilaustyön, työtilaustyön työtilausprojekti saa automaattisesti käyttöomaisuus erään liittyvät taloushallinnon dimensiot. Tämä tarkoittaa, että kun käytät toiminnallisia sijainteja, kustannuksia voidaan aina seurata niissä toiminnallisissa sijainneissa, joissa käyttöomaisuuserä on asennettuna tiettynä aikana. Taloushallinnon dimensioiden automaattinen päivitys varmistaa projektinhallinnan ja raportoinnin kustannusten täydellisen jäljitettävyyden.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Työtilausprojektit, työtilausten elinkaaritilat, projektin vaiheet ja projektityypit

Voit varmistaa työtilausten elinkaaritilojen ja niihin liittyvien projektivaiheiden oikean käytön harkitsemalla riippuvuuksia suhteessa **Projektinhallinta ja kirjanpito** -moduuliin:

- **Projektinhallinta ja kirjanpito** -moduulissa projektin vaiheet määritetään **Projektinhallinnan ja kirjanpidon parametrit** asetuksissa määritetyille projektityypeille.  
- Muista **Projektinhallinnan ja kirjanpidon parametrit** -asetuksissa valita haluamasi projektivaiheen valintaruudut kaikille projektityypeille, joita aiot käyttää. Alla olevassa kuvassa on viisi vaihetta **Luotu** - **Arvioitu** - **Ajoitettu** - **Käynnissä** - **Valmis** valittu projektityypeille "Aika ja materiaali" sekä "Sisäinen". Nämä viisi vaihetta koskevat sekä sisäisiä ylläpitotöitä että palveluhuoltotöitä.  
- **Resurssien hallinnassa** projektityypit määritetään projektiryhmien mukaan, jotka määritetään **Työtilauksen projektiasetukset** -lomakkeessa > **Projektiryhmä**-linkin kautta.  
- **Työtilauksen projektiasetukset** -asetusten projektiryhmien asetuksia käytetään luotaessa työtilauksia. Kun työtilaus luodaan, työtilausprojekti luodaan automaattisesti työtilaukselle.  
- Työtilauksen elinkaaritiloilla on oltava siihen liittyvä projektivaihe.  
- Työtilauksen elinkaaren tilaan liittyvä projektin vaihe on määritettävä työtilausprojektissa määritetyn projektiryhmän aktiiviseksi vaiheeksi. Työtilausprojekti luodaan automaattisesti työtilaukseen.  
- Kun luot uuden työtilauksen, työtilausprojektin automaattinen kohdistus perustuu **Työtilauksen projektiasetukset** -kohdan asetuksiin (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset**).  

Alla olevissa kuvissa näkyvät työtilauksen projektiryhmien, liittyvien projektityyppien, projektin vaiheiden ja työtilausten elinkaaritilojen väliset kytkennät.  

![Kuva 3](media/03-integration-to-pma.png)

![Kuva 4](media/04-integration-to-pma.png)

![Kuva 5](media/05-integration-to-pma.png)

Katso [Työtilausprojektin asetukset](../setup-for-work-orders/work-order-project-setup.md) -kohta työtilausprojektien määrittämistä varten sekä [Työtilauksen elinkaaren tilat](../setup-for-work-orders/work-order-lifecycle-states.md) koskien työtilausten elinkaaritilojen luomista.

Alla olevassa kuvassa esitetään graafinen yleiskatsaus eri projekteista, jotka luodaan **Resurssien hallinta**- moduulissa, jotta saadaan integrointi **Projektinhallinta ja kirjanpito** -moduuliin sekä työprosessit, joihin projektit liittyvät.

![Kuva 6](media/06-integration-to-pma.png)

