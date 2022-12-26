---
title: Dynamics 365 Commercein esiversio 10.0.30 (Marraskuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercein 10.0.30 uusia tai muuttuneita toimintoja.
author: josaw1
ms.date: 12/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: a449c7eff21c059555f9659ea932705858d26275
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831744"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Dynamics 365 Commercein esiversio 10.0.30 (Marraskuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -esiversion 10.0.30 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1362. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** Syyskuu 2022
- **Version yleinen saatavuus (oma päivitys):** lokakuu 2022
- **Version yleinen saatavuus (automaattinen päivitys):** marraskuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---------|------------------|----------------|--------------| 
| Asiakaspalvelu   | Keskustelu sähköisen kaupankäynnin sivustolla Power Virtual Agents -botin avulla. | Tämän ominaisuuden avulla sähköisen kaupankäynnin sivuston käyttäjät voivat valita Power Virtual Agents -keskustelubotin tukipyyntöjä varten. | Järjestelmänvalvoja/tekijät antavat käyttäjille oikeudet |
| Merkitykselliset tiedot  |  Suoratoista myyntipisteen toiminnallisten merkityksellisten tietojen tapahtumat Application Insights -tilille. | [Application Insightsin lokien käyttäminen](../dev-itpro/operational-insights.md#enable-diagnostic-events-in-application-insights)   |  IT-ammattilaisen/-kehittäjän suostumus   |
|  Maksut  | PayPal-tilauksen tuki 29 päivän valtuutusjakson jälkeen. | PayPalin pisin valtuutusjakso on 29 päivää. Tämän jälkeen on luotava uusi valtuutus ja tilaustunnus. Vaihtoehtoisesti PayPal tarjoaa mahdollisuuden, jossa PayPal-tilaukseen voidaan viitata yleisenä tilauksena. Tämän ansiosta samalla tilaustunnuksella voi olla useita valtuutuksia ja sieppauksia sen sijaan, että uusi valtuutus ja tilaustunnus olisi luotava 29 päivän kuluttua. | Kun PayPalin maksuyhdistintä määritetään Commerce headquartersissa, **OrderIntent**-kenttä lisätään. Kentässä voi olla seuraavat kaksi arvoa:<p><p>- **Valtuuta** - Tämä määritys on oletusarvo (jos kenttä jätetään tyhjäksi **Valtuuta** on oletusarvo). Kun **OrderIntent**-kohdan arvoksi määritetään **Valtuuta**, se vastaa PayPalin **processing_instruction**-arvoa **NO_INSTRUCTION**-kohdassa. PayPal valtuuttaa tilauksen. Valtuutusta ei voi muuttaa, kun käytetään tätä arvoa.<p>- **Tallenna** - Kun **OrderIntent**-arvoksi määritetään **Tallenna**, arvo vastaa PayPalin **processing_instruction**-arvoa **ORDER_SAVED_EXPLICITLY**-kohdassa. Tilauksen viitteet tallennetaan PayPal-palveluun, kun tätä arvoa käytetään.  |
| Myyntipisteen sisäänkirjaus  | [Itsepalvelun diagnoosiominaisuuksien käyttöönotto myyntipisteen sisäänkirjauksessa](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Tämä ominaisuus mahdollistaa itsepalvelun diagnoosiominaisuuksien käyttämisen myyntipisteessä ja Commerce headquartersissa. Ominaisuuksien avulla myymälän työntekijät ja esimiehet voivat nopeasti määrittää myyntipisteen sisäänkirjauksen ongelmien syyt ja korjata ne.<p><p>- Myyntipisteen sisäänkirjausnäytössä näkyviä virhesanomia parannettiin niin, että niissä näkyvät konkreettisen syyn tiedot. Ne auttavat myyntipistettä käyttäviä myymälän työntekijöitä ymmärtämään, mikä epäonnistui, ja suorittamaan tarvittavat toiminnot ongelman ratkaisemiseksi.<p>- **Testisisäänkirjaus**-ominaisuus on käytettävissä **Työntekijät**-sivulla Commerce headquartersissa. Sen avulla myyntipisteen laitteet määrittäneet myymälän esimiehet voivat simuloida myyntipisteen sisäänkirjauksen. Jos sisäänkirjaus epäonnistuu, tämän ominaisuuden avulla esimiehet voivat käyttää toiminnallisia vianmääritysoppaita ja tarkistaa asiaankuuluvat määritykset, korjata ongelmia ja vahvistaa korjaukset.  | Käytössä oletusarvoisesti |


## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Dynamics 365 Finance 10.0.30 sisältää ympäristöpäivityksiä. Lisätietoja on kohdassa [Talous- ja toimintosovellusten käyttöympäristön päivitysversio 10.0.30](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.30 virheenkorjauksista eri päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja lukemalla [Knowledge Base -artikkelin](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2022wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-features"></a>Poistetut ja vanhentuneet ominaisuudet

Poistetut ja vanhentuneet Commerce-ominaisuudet on kuvattu artikkelissa [Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet](removed-deprecated-features-commerce.md).

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Commercein poistetut tai vanhentuneet toiminnot](removed-deprecated-features-commerce.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
