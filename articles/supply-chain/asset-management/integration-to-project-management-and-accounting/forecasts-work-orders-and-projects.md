---
title: Ennusteet, työtilaukset ja projektit
description: Tässä ohjeaiheessa selitetään ennusteiden ja työtilausten integrointi resurssien hallinnan Projektinhallinta ja kirjanpito -moduulin kanssa.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426961"
---
# <a name="forecasts-work-orders-and-projects"></a>Ennusteet, työtilaukset ja projektit

[!include [banner](../../includes/banner.md)]

 

Resurssien hallinnassa integrointi **Projektinhallinta ja kirjanpito** -moduuliin auttaa optimoimaan kustannusten hallinnan, jolloin käyttäjät voivat seurata kustannuksia huoltotyön tyyppien ennusteissa ja työtilaustöissä.

Kunnossapitotöiden tyyppien ennusteiden seuraamista varten on tehtävä kaksi asetusta:

1. Valitse projekti kohdassa **Resurssien hallinta** > **Asetukset** > **Resurssienhallinnan parametrit** ja sitten kohdassa **Resurssit** -välilehti > **Projekti**-pikavälilehdessä **Ylläpitoennusteen projekti** -kentässä.

2. Kun **Ylläpitotyön tyyppien oletus** -kohdassa luot ylläpitotyötyypin oletusrivin, riville luodaan automaattisesti tehtävänumero (**Resurssien hallinta** > **Asetukset** > **Työt** > **Ylläpitotyön tyyppien oletukset**).

Kunnossapitotöiden tyypin ennusteita käytetään kahteen tarkoitukseen: 

- Voit jäljittää kunnossapidon työtyypin ennusteiden kustannuksia **Projektinhallinta ja kirjanpito** -moduulissa. 
- Ennusteet siirretään automaattisesti työtilauksen työn projektiin, kun valitset kunnossapitotyön tyypin työtilaustyölle.

Jotta työtilausten töiden kustannukset voidaan jäljittää, on ensin määritettävä työtilausprojektit. Lisätietoja on kohdassa [Työtilauksen projektin määritys](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Työtilauksen työn projektit

Kun työtilaukseen luodaan työtilaustyö, työtilausprojekti määräytyy pääprojektin asetusten mukaan **Työtilauksen projektiasetukset** -sivulla (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset**).

Työtilauksen työprojektit luodaan seuraavien työtilaustietojen yhdistelmän avulla:

- Työtilauksessa valittu työtilaustyyppi 
- Työtilaustyön käyttöomaisuuteen liittyvä toiminnallinen sijainti
- Työtilaustyön käyttöomaisuuteen liittyvä resurssityyppi  
- Työtilaukseen määritetty odotettu alkamis- ja loppumisaika  

Joitakin näistä tiedoista ei ehkä löydy työtilauksesta. Näin ollen työtilauksen pääprojektin haku tehdään käyttämällä käytettävissä olevaa tietoyhdistelmää ja valitsemalla projektitunnus, joka vastaa työtilauksen tietoja.

Esimerkiksi seuraavassa kuvassa **Truck Engine** -käyttöomaisuustyypin määritystavan vuoksi jokainen työtilaustyö, joka luodaan **Truck Engine** -käyttöomaisuustyypillä, on projektitunnuksen 000186 aliprojekti.

![Kuva 1](media/01-integration-to-pma.png)

Työtilaustyön projektitunnuksen ja siihen liittyvän tehtävän numeron tarkoitus on jäljittää työtilaustyöhön liittyvät kustannukset ja sille valittu käyttöomaisuuserä **Projektinhallinta ja kirjanpito** -moduulissa. (Voit tarkastella projektin tunnusta ja tehtävän numeroa valitsemalla **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** ja valitsemalla sitten työtilauksen. **Rivin tiedot**-pikavälilehdessä **Projektitunnus**-kentässä näkyy projektin tunnus, ja **Tehtävän numero** -kentässä näkyy tehtävä numero.) Lisätietoja käyttöomaisuuden hallinnan kustannusten hallinnasta on kohdassa [Kustannusten ja päivämäärien hallinta](../controlling-and-reporting/cost-and-date-control.md).

Seuraavassaolevassa kuvassa näkyy graafinen yleiskatsaus työtilausprojekteista ja niihin liittyvistä projektitehtävistä.

![Kuva 2](media/02-integration-to-pma.png)

Kun työtilaukseen luodaan uusi työtilaustyö, työtilausprojekti luodaan automaattisesti työlle. Työtilaus työhön liittyvän käyttöomaisuuserän taloushallinnon dimensiot siirretään automaattisesti työtilausprojektiin.

Työtilaustyölle luodulle projektitehtävälle on liitetty siihen liittyviä tietoja. Nämä tiedot koskevat kunnossapitotöiden tyyppiä, kunnossapitotöiden tyypin varianttia ja kauppaa. Näistä tiedoista on hyötyä esimerkiksi silloin, kun luot ostotilauksen työtilauksesta ( katso [Hankinta](../work-orders/procurement.md)) tai jos käytät **Projektinhallinta ja kirjanpito** -moduulia ajan rekisteröintiä varten.

Jos käyttöomaisuus on asennettu toiminnallisessa sijainnissa, mutta kyseinen käyttöomaisuuserä on myöhemmin asennettu toiseen toimintosijaintiin, uuteen toimintosijaintiin liittyvät taloushallinnon dimensiot päivitetään automaattisesti käyttöomaisuuserälle. Kun luot käyttöomaisuudelle työtilaustyön, työtilaustyön työtilausprojekti saa automaattisesti käyttöomaisuuserään liittyvät taloushallinnon dimensiot. Tämä tarkoittaa, että kun käytät toiminnallisia sijainteja, kustannuksia voidaan aina seurata niissä toiminnallisissa sijainneissa, joissa käyttöomaisuuserä on asennettuna tiettynä aikana. Taloushallinnon dimensioiden automaattinen päivitys auttaa varmistamaan projektinhallinnan ja raportoinnin kustannusten täydellisen jäljitettävyyden.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Työtilausprojektit, työtilausten elinkaaritilat, projektin vaiheet ja projektityypit

Voit auttaa varmistamaan työtilausten elinkaaritilojen ja niihin liittyvien projektivaiheiden oikean käytön harkitsemalla riippuvuuksia suhteessa **Projektinhallinta ja kirjanpito** -moduuliin:

- **Projektinhallinta ja kirjanpito** -moduulissa projektin vaiheet määritetään **Projektinhallinnan ja kirjanpidon parametrit** -sivulla määritetyille projektityypeille.  
- Muista **Projektinhallinnan ja kirjanpidon parametrit** -asetuksissa valita haluamasi projektivaiheiden valintaruudut kaikille projektityypeille, joita aiot käyttää. Seuraavissa kuvissa viisi vaihetta (**Luotu**, **Arvioitu**, **Ajoitettu**, **Käynnissä**, **Valmis**) on valittu projektityypeille **Aika ja materiaali** sekä **Sisäinen**. Nämä viisi vaihetta koskevat sekä sisäisiä ylläpitotöitä että palveluhuoltotöitä.
- **Resurssien hallinta** -moduulissa projektityypit määritetään projektiryhmien mukaan, jotka määritetään **Työtilauksen projektinasetukset** -sivun **Projektiryhmä** -välilehdessä (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset**).  
- **Työtilauksen projektiasetukset** -sivulla määritettyjä projektiryhmien asetuksia käytetään luotaessa työtilauksia. Kun työtilaus luodaan, työtilausprojekti luodaan automaattisesti työtilaukselle.  
- Kullakin työtilauksen elinkaaritilalla on oltava siihen liittyvä projektivaihe.  
- Työtilauksen elinkaaren tilaan liittyvä projektin vaihe on määritettävä työtilausprojektissa määritetyn projektiryhmän aktiiviseksi vaiheeksi. Työtilausprojekti luodaan automaattisesti työtilaukseen.
- Kun luot uuden työtilauksen, työtilausprojektin automaattinen kohdistus perustuu **Työtilauksen projektiasetukset** -sivun asetuksiin.  

Alla olevissa kuvissa näkyvät työtilauksen projektiryhmien, liittyvien projektityyppien, projektin vaiheiden ja työtilausten elinkaaritilojen väliset kytkennät.

![Kuva 3](media/03-integration-to-pma.png)

![Kuva 4](media/04-integration-to-pma.png)

![Kuva 5](media/05-integration-to-pma.png)

Lisätietoja työtilausprojektien määrittämisestä on kohdassa [Työtilausprojektin asetukset](../setup-for-work-orders/work-order-project-setup.md). Lisätietoja työtilausten elinkaaritilojen luomisesta on kohdassa [Työtilauksen elinkaaren tilat](../setup-for-work-orders/work-order-lifecycle-states.md).

Seuraavassa kuvassa on graafinen yleiskatsaus eri projekteista, jotka on luotu **Resurssien hallinta** -moduulissa, jotta integrointi **Projektinhallinta ja kirjanpito** -moduuliin voidaan ottaa käyttöön. Siinä näkyvät myös työprosessit, joihin projektit liittyvät.

![Kuva 6](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]