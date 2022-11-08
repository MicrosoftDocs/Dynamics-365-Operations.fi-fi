---
title: Tilaushaun käyttöönotto vierailijoiden uloskuittauksessa
description: Tässä artikkelissa kuvataan, miten tilaushaku otetaan käyttöön vierailijoiden uloskuittauksessa Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 757e83887e318dd6aa54106fb78305f1d94e0f90
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734245"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Tilaushaun käyttöönotto vierailijoiden uloskuittauksessa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten tilaushaku otetaan käyttöön vierailijoiden uloskuittauksessa Microsoft Dynamics 365 Commercessa.

Vierailijoiden uloskuittauksen tilaushaun avulla asiakkaat, jotka suorittavat ostoksensa vieraskäyttäjänä, voivat hakea tilauksensa. Tilausten hakutoiminto on hyödyllinen, kun asiakkaat haluavat suorittaa toimintoja, kuten tarkistaa tilauksen tuotteiden täyttämisen tilan, tarkistaa osoitteen, johon tilaus lähetettiin, tilata tuotteen uudelleen tai vahvistaa kaupalle, että tilaus haetaan sieltä.

Asiakkaat, jotka tilaavat tilauksen rekisteröityinä käyttäjinä, näkevät tilaustietonsa sisään kirjauduttuaan, mutta asiakkaat, jotka käyttävät vierailijoiden uloskuittausta tilausten tekemiseen, eivät niitä näe. Kun taas vierailijoiden uloskuittauksen tilaushaku on käytössä, asiakkaat voivat hakea vierailijoina tekemiään tilauksia lomakkeen avulla. Tässä lomakkeessa asiakkaat syövät tilausvahvistuksen tunnuksen ja (valinnaisesti) sähköpostiosoitteen, jonka he antoivat uloskuittauksen yhteydessä.

Lisäksi linkki tai painike, joka vie asiakkaan suoraan tilauksen tietosivulle, voidaan sisällyttää mihin tahansa tilaukseen liittyvään tapahtumasähköpostiin. Tämä linkki tai painike toimii sekä rekisteröityneiden käyttäjien että vieraskäyttäjien tilauksissa.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Tarvittavien ominaisuuksien käyttöönotto Commerce-pääkonttorissa

Jotta voit ottaa tilaushaun käyttöön vierailijoiden uloskuittauksessa, seuraavat Commerce-pääkonttorin ominaisuudet on otettava käyttöön kohdassa **Työtilat \>Ominaisuuksien hallinta**.

| Ominaisuus | Tarkoitus |
|---------|---------|
| Retailin anonyymin käyttäjän hakutilauksen tietojen valitsemisen toiminto | Tämä ominaisuus avaa Commerce-parametrien käyttöliittymän, jonka avulla voit ottaa tilaushaun ohjelmointirajapinnan käyttöön varmentamattomille käyttäjille ja määrittää, miten henkilötiedot näytetään. |
| Ota käyttöön vahvemman kanavan viitetunnuksen luominen | Tämä ominaisuus luo turvallisemman 12-merkkisen kanavaviittaustunnuksen (tilausvahvistuksen tunnus), joka voidaan välittää kyselymerkkijonoon, kun tilausta haetaan. |
| Luo yhdenmukainen kanavan viitetunnuksen muoto eri kanavissa | Tämä ominaisuus luo suojatun kanavan viitetunnuksen tilauksille, jotka on tehty sähköisen kaupankäynnin sivustolla, vähittäismyyntipisteessä (POS) tai puhelinkeskuksen kautta. Ennen kuin tämä ominaisuus voidaan ottaa käyttöön, on otettava käyttöön **Salli vahvemman kanavaviittaustunnuksen luonti** -ominaisuus. |

Kun olet ottanut **Vähittäismyynnin käyttäjähaun tilaustietojen valitsemisominaisuus** -ominaisuuden, sinun on otettava käyttöön ohjelmointirajapinta, joka tukee varmentamattomien tilausten hakua Commerce-pääkonttorissa. Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Asiakastilaukset**. Määritä **Asiakastilaukset**-sivun **Tilaushaku**-pikavälilehdessä **Salli varmentamattomien tilausten haku** -asetuksen arvoksi **Kyllä**, kuten seuraavassa kuvassa näkyy.

## <a name="manage-the-display-of-personal-data"></a>Henkilötietojen näyttämisen hallinta

Commerce-pääkonttorin **Asiakastilaukset**-sivun **Tilaushaku**-pikavälilehti sisältää **Sisällytä henkilötiedot vierailijoiden tilaushakuun** -kentän, jolla voit valita, näytetäänkö asiakkaille henkilötietoja. Näitä henkilötietoja ovat asiakkaan toimitusosoite ja asiakkaan luottokortin numeron viimeiset neljä numeroa. Oletusarvoisesti henkilökohtaisia tietoja ei näytetä asiakkaille, kun varmentamattomien tilausten haku on käytössä. Seuraavassa taulukossa kuvataan käytettävissä olevat vaihtoehdot:

| Vaihtoehto | Tulos |
|--------|--------|
| Ei koskaan | Oletusarvo. Tilaushakujen yhteydessä ei näytetä henkilötietoja. Kun sisään kirjautuneet rekisteröityneet käyttäjät hakevat kirjautuneena tekemänsä tilauksen, he voivat nähdä henkilötietonsa. |
| Vain vierastilaukset | Henkilötietoja näytetään tilaushauissa sellaisten tilausten osalta, jotka asiakkaat ovat tehneet vierailijoina. Jos tilauksen on tehnyt rekisteröitynyt käyttäjä, hänen on kirjauduttava sisään nähdäkseen henkilötietonsa. |
| Kaikki tilaukset | Henkilötiedot näytetään kaikkien tilaushakujen yhteydessä. |

> [!NOTE]
> Nämä asetukset määrittävät, milloin henkilötietoja, kuten asiakkaan osoite ja asiakkaan luottokortin numeron neljä viimeitä numeroa, näytetään anonyymeille vieraskäyttäjille. Rekisteröityjen asiakkaiden yksityisyydensuojan edistämiseksi suosittelemme **Vain vierailijoiden tilaukset** -vaihtoehdon valitsemista. Turvallisin vaihtoehto on kuitenkin **Ei koskaan**.

Kun olet muuttanut **Sisällytä henkilötiedot vierailijoiden tilaushakuun**, sinun on suoritettava työ 1070 (**Kanavan määritys**) Commerce-pääkonttorissa siirtymällä kohtaan **Retail ja Commerce \> Retailin ja Commercen IT \> Jakeluaikataulu**.

## <a name="configure-the-order-lookup-module"></a>Määritä tilaushakumoduuli

Commerce-moduulikirjaston tilaushakumoduulin avulla hahmonnetaan lomake, jonka avulla vieraskäyttäjät voivat etsiä tilauksia. Tilaushakumoduulin voi sisällyttää minkä tahansa sellaisen sivun tekstiosapaikkaan, joka ei edellytä asiakkaan sisäänkirjautumista. Lisätietoja moduulin määrittämisestä: [Tilaushakumoduuli](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Tilauksen tietosivun konfiguroiminen

Ennen kuin vieraskäyttäjät voivat tarkastella tilaustietojaan, sähköisen kupankäynnin sivuston tilaustiedot on määritettävä niin, että se ei edellytä kirjautumista. Jos haluat poistaa tilaustietosivun kirjautumisvaatimuksen käytöstä, avaa Commerce-sivustonmuodostinsivu, valitse puunäkymästä **oletussivu (pakollinen)** ja poista Oikeanpuoleisen ominaisuusruudun alaosassa oleva **Vaatii kirjautumista?** -valintaruudun valinta.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Linkin lisääminen tapahtumasähköpostiviestien tilauseriin

Voit lähettää tilaukseen liittyviä sähköpostiviestejä linkin tai painikkeen, jonka avulla asiakkaat voivat avata tilauksen tietosivun. Voit lisätä tämän linkin tai painikkeen luomalla HTML-hyperlinkin, joka osoittaa sähköisen kauppasivuston tilaustietosivulle, ja siirrä tilausvahvistustunnus ja asiakkaan sähköpostiosoite URL-parametreiksi seuraavan esimerkin mukaisesti.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

> [!NOTE]
> Jos haluat ottaa tilausten hakutoiminnon käyttöön, varmista, että **Tarjoukset**-avain on käytössä kohdassa **Käyttöoikeuden konfiguraatio** > **Konfigurointiavaimet**.
>
>![Tarjousten käyttöoikeusavaimen konfiguraation täytyy olla käytössä](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tilaushakumoduuli](order-lookup-module.md)

[Sähköposti-ilmoitusprofiilin määrittäminen](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
