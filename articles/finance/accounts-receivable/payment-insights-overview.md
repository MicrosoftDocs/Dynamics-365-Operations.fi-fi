---
title: Asiakasmaksujen tiedot (esiversio)
description: Täsäs ohjeaiheessa kerrotaan maksun tietojen ominaisuudesta. Sen avulla saadaan lisätietoja yksittäisten asiakkaiden tyypillistä maksukäytännöistä. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit voidaan aloittaa tapauksissa, joissa muuten et niin tekisi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644630"
---
# <a name="customer-payment-insights-preview"></a>Asiakasmaksujen tiedot (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Täsäs ohjeaiheessa kerrotaan maksun tietojen ominaisuudesta. Sen avulla saadaan lisätietoja yksittäisten asiakkaiden tyypillistä maksukäytännöistä. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit voidaan aloittaa tapauksissa, joissa muuten et niin tekisi. 

## <a name="overview"></a>Yleiskuvaus

Joskus voi olla haastavaa ennustaa, milloin asiakkaat maksavat laskut. Tämän tiedon puute heikentää kassavirtaennusteiden tarkkuutta sekä johtaa liian myöhään käynnistyviin perintäprosesseihin ja tilausten vapauttamiseen asiakkaille, jotka voivat jättää laskut maksamatta. Asiakkaan maksujen tiedot (esiversio) auttaa organisaatioita ennustamaan, milloin myyntilasku maksetaan. Näiden tietojen avulla organisaatiot voivat luoda perintästrategioita, jotka parantavat ajoissa maksettavan maksun todennäköisyyttä. 

## <a name="predictions"></a>Ennusteet

Maksuennusteiden avulla organisaatiot voivat parantaa liiketoimintaprosesseja, sillä organisaatioiden on helppo tunnistaa laskut, joiden maksu todennäköisesti myöhästyy. Lisäksi organisaatiot voivat käyttöön toimenpiteitä, jotka parantavat todennäköisyyttä, että maksu maksetaan ajoissa.

Asiakasmaksujen tiedot (esiversio) käyttää historiallisia laskuja, maksuja ja asiakastietoja hyödyntävää koneoppimismallia, mikä tarkentaa sen ennustamista, milloin asiakas maksaa jäljellä olevan laskun.

Asiakkaan maksutavat (esiversio) voi ennustaa kolme maksun todennäköisyyttä kullekin avoimelle laskulle:

-   Todennäköisyys sille, että maksu suoritetaan ajoissa 
-   Todennäköisyys sille, että maksu suoritetaan myöhässä
-   Todennäköisyys sille, että maksu suoritetaan erittäin paljon myöhässä

Asiakasmaksujen tiedot (esiversio) -toiminnossa on myös koostenäkymä odotetuista maksuista. Sen avulla organisaatiot saavat paremman käsityksen siitä maksun kokonaissummasta, jonka ne voivat odottaa asiakkaan maksavan, sen perusteella, mihin jaksoon asiakas sijoittuu (ajoissa, myöhässä ja erittäin paljon myöhässä).

[![Maksuennusteiden koostenäkymä](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Lisäksi kullekin laskulle määritetään todennäköisyys ajoissa maksamisesta. Jos maksun todennäköisyys on alle 50 %, laskuihin lisätään punainen ympyrä osoittamaan, että lasku on ehkä lähetettävä perintään. 

[![Maksun todennäköisyyksien luettelo](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Asiakasmaksujen tiedot (esiversio) sisältää myös kontekstitietoja, jotka selventävät ennustetta. Niitä ovat esimerkiksi tärkeimmät ennusteeseen vaikuttaneet seikat, asiakkaan liikesuhteen nykyinen tila ja asiakkaan historialliset maksutiedot. Monissa yrityksissä perintäprosessi on reaktiivista, jolloin perintäprosessi alkaa vasta, kun laskut erääntyvät. 

Asiakasmaksujen tiedot (esiversio) antaa organisaatioille mahdollisuuden toimia perinnän suhteen ennakoivasti. Niiden ei enää tarvitse odottaa, että tapahtuvat erääntyvät ennen perintäprosessin aloittamista. Sen sijaan ne voivat selvittää maksuennusteominaisuuden avulla, parantaako ennakkoiva perintä todennäköisyyttä ajoissa tapahtuvasta maksun maksamisesta. Yritykset saavat maksuennusteen avulla myös tietoja, joita ne tarvitsevat perustelemaan etukäteen aloitettavaa perintäprosessia.

## <a name="methodology"></a>Metodologia

Tekoälyratkaisun kehittäminen ja käyttöönotto on vaikeaa. Sitä varten tarvitaan ryhmä, jossa on datatieteilijöitä, aihealueen asiantuntijoita ja teknikoita, jotka käyttävät paljon aikaa käyttökelpoisen tekoälyratkaisun muotoiluun, kehittämiseen, käyttöönottamiseen ja ylläpitoon. Tekoälyratkaisujen käyttöönottaminen ja käyttö Financessa on kuitenkin helppoa. Finance sisältää valmiiksi pakattuja tekoälyratkaisuja, jotka on muodostettu Microsoft AI Builderin pohjalta. Loppukäyttäjä voi ottaa yhdellä napsautuksella käyttöön tekoälyratkaisun ja aloittaa älykkäistä ennusteista saatavien etujen hyödyntämisen. Jos organisaatio ei ole tyytyväinen ennusteiden tarkkuuteen, tehokäyttäjä voi lisätä taas yhdellä napsautuksella AI Builderin laajennuskokemuksen ja sitten valita ennusteiden muodostamiseen käytettäviä kenttiä tai poistaa niiden valinnan. Kun muutokset on tehty, muutokset voidaan kouluttaa ja julkaista, minkä jälkeen uusi koulutettu malli valitaan Financessa automaattisesti ennusteisiin.

## <a name="how-to-get-customer-payment-insights-preview"></a>Asiakasmaksujen tiedot (esiversio) -toiminnon hankkiminen

Lähetä sähköpostia osoitteeseen [Asiakasmaksujen tiedot (esiversio)](mailto:fiap@microsoft.com), jos haluat kokeilla Asiakasmaksun tiedot (esiversio) -sovellusta.

## <a name="privacy-notice"></a>Tietosuojatiedot

Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]