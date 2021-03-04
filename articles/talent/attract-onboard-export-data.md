---
title: Tietojen vienti Attractista ja Onboardista
description: Tietojen vienti Dynamics 365 Talent – Attractista ja Onboardista.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460988"
---
# <a name="export-data-from-attract-and-onboard"></a>Tietojen vienti Attractista ja Onboardista

[!include [banner](includes/banner.md)]

Kuten kohdassa [Dynamics 365 Talent: Attract- ja Dynamics 365 Talent: Onboard -sovellusten poistaminen käytöstä](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) ilmoitettiin, Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard poistetaan käytöstä 1.2.2022. Kummassakin sovelluksessa on nyt tietojen vientiominaisuus, mikä helpottaa siirtymistä toiseen tuotteeseen.

## <a name="export-data-from-attract"></a>Tietojen vienti Attractista

Voit viedä tietoja ilman, että ympäristön käyttöoikeutta on rajoitettava. Se kannattaa ehkä tehdä testauksen vuoksi tai tietorakenteen selvittämiseksi. Kun olet valmis siirtoon, rajoita Attract-ympäristön käyttöä tämän menettelyn jälkeen annettujen ohjeiden mukaisesti. Muista viedä tiedot uudelleen. 

1. Siirry osoitteeseen [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Valitse **Pyydä tietojen vientiä** **Tietojen vienti** -kohdassa.

   ![[Tietojen viennin pyytäminen Attractista](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Kun **Pyyntöä käsitellään** -sanomaruutu avautuu, valitse **OK**. Tietojen vienti voi kestää 20 minuuttia viennin koon mukaan.

4. Kun vienti valmistuu, valitse vieressä oleva **Lataa**-painiketta. 

   >[!NOTE]
   >Kaikki tietojen viennit ovat käytettävissä seitsemän päivää, jonka jälkeen **Lataa**-linkki vanhenee.</br>
   
Latauksen .zip-tiedostossa on Attract-tietoja, mukaan lukien seuraavat kansiot:

| Kansion nimi | Kuvaus |
| --- | --- |
| Järjestelmänvalvojan asetukset | Attract-hallintakeskuksen määritykset. |
| Ehdokkaat | Kaikki töihin tai kykypooleihin lisätyt ehdokkaat. |
| Sähköpostimallit | Kaikki ympäristöön määritetyt sähköpostimallit. |
| Työntarjouspakettien mallit | Kaikki luodut työtarjouspakettien mallit sekä niihin liitetyt määritykset. |
| Työtarjouksen sääntöjoukot |  Kaikki tarjouksenhallintaa ladatut sääntöjoukkotiedostot. |
| Työntarjousmallit | Kaikki ympäristöön luodut työtarjouksen asiakirjamallit. |
| Avoimet työpaikat | Kaikki luodut työt. Poistettuja töitä ei viedä. Alikansiot sisältävät ehdokkaiden hakemukset. Lisäksi hakemusten liitteille ja tarjouspaketeille on tarvittaessa omat alikansiot. |
| Avoimien työpaikkojen mallit | Ympäristössä määritetyt töiden käsittelymallit. |
| Kykypoolit | Kaikki luodut kykypoolit, niiden osallistujaluettelot ja kykypoolien ehdokasluettelot. |
| Työntekijät | Luettelo kaikista ympäristössä olevista työntekijöistä sekä heidän rooleistaan. |
| (pääkansio) | Tietorakennekenttiä kuvaava JSON-rakennetiedosto. |

### <a name="restrict-access-to-attract"></a>Attractin käytön rajoittaminen

Kun olet valmis siirtoon, rajoita muiden kuin järjestelmänvalvojien Attract-ympäristön käyttöoikeutta ja vie tiedot.

>[!IMPORTANT]
>Attract-ympäristön käyttöoikeus rajoitetaan pysyvästi, eikä rajoitusta voi peruuttaa. Jos haluat, että muut kuin järjestelmänvalvojat voivat jatkaa ympäristön käyttöä, ohita tämä vaihe.

1. Siirry osoitteeseen [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Voit rajoittaa muiden kuin järjestelmänvalvojien Attract-ympäristön käyttöä valitsemalla **Rajoita käyttö nyt** **Rajoita tämän sovelluksen käyttöä** -kohdassa. Käytön rajoittaminen aiheuttaa myös kaikkien julkaistujen aktiivisten työpaikkojen julkaisujen poistaminen.

   ![[Muiden kuin järjestelmänvalvojien Attractin käytön rajoittaminen](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Kun varoitus **Tämä on pysyvä muutos** tulee näkyviin, valitse **Rajoita käyttöä**, jonka jälkeen muut kuin järjestelmänvalvojat eivät voi enää käyttää tätä ympäristöä. Jos et ole valmis tekemään tätä vaihetta, valitse **Peruuta**.

   ![[Varoitus siitä, että käytön rajoittaminen on pysyvä muutos](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Järjestelmänvalvojat voivat jatkaa tietojen viennin ja henkilöraporttisivujen käyttöä sen jälkeen, kun Attract-ympäristön käyttöä on rajoitettu.

## <a name="export-data-from-onboard"></a>Tietojen vienti Onboardista

Kun olet valmis, voit ladata mallit, oppaat ja ehdokastiedot Onboardista.

1. Siirry osoitteeseen [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Valitse **Pyydä tietojen vientiä** **Tietojen vienti** -kohdassa. 

   ![[Tietojen viennin pyytäminen Onboardista](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Kun **Pyyntöä käsitellään** -sanomaruutu avautuu, valitse **OK**. Tietojen vienti voi kestää 20 minuuttia viennin koon mukaan.

4. Kun vienti valmistuu, valitse vieressä oleva **Lataa**-painiketta. 

   ![[Tietojen viennin lataaminen Onboardista](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Tietojen vienti on käytettävissä seitsemän päivän ajan. **Lataa**-linkki vanhenee seitsemän päivän kuluttua, jonka jälkeen on pyydettävä uusi vienti, jos tiedot on ladattava uudelleen. Kun aloitat uuden tietojen viennin, aiemmin tehdyt lataukset vanhentuvat, kun uusi vienti on valmis.

Ladattavan .zip-tiedoston sisältö:

- **Mallit**-kansio, joka sisältää Word-muotoiset Onboard-mallit.

- **Opas**-kansio, joka sisältää Word-muotoiset Onboard-oppaat.

## <a name="see-also"></a>Lisätietoja

[Dynamics 365 Talent: Attract- ja Dynamics 365 Talent: Onboard -sovellusten poistaminen käytöstä](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]