---
title: Konfigurointiavaimet ja tietoyksiköt
description: Tässä ohjeaiheessa käsitellään konfigurointiavainten ja tietoyksiköiden välistä suhdetta.
author: Sunil-Garg
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 383b8664b7e8cc063b980c52997ddf273d363033
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569170"
---
# <a name="configuration-keys-and-data-entities"></a>Konfigurointiavaimet ja tietoyksiköt

[!include [banner](../includes/banner.md)]

Ennen tietojen tuontia tai vientiä tietoyksiköiden avulla kannattaa ensin selvittää, miten konfigurointiavaimet vaikuttavat tietoyksiköihin, joita aiot käyttää.

Lisätietoja konfigurointiavaimista on kohdassa [Käyttöoikeuskoodien ja konfigurointiavainten raportti](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Konfigurointiavainten määritykset
Konfigurointiavaimet voidaan määrittää yhdelle seuraavista tiedoista tai kaikille kyseisille tiedoille.

- Tietoyksiköt
- Tietolähteinä käytettävät taulut
- Taulukon kentät
- Tietoyksikkökentät

Seuraavassa taulussa on yhteenveto tavoista, joilla objektin taustalla olevien erilaisten tietojen konfigurointiavainten arvot muuttavat objektin odotettua toimintaa.

| Tietoyksikön konfigurointiavaimen asetus | Taulun konfigurointiavaimen asetus | Taulukentän konfigurointiavaimen asetus | Tietoyksikkökentän konfigurointiavaimen asetus | Odotettu toiminta |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Ei käytössä                                | Ei arvioitu                      | Ei arvioitu                            | Ei arvioitu                          | Jos tietoyksikön konfigurointiavain on poistettu käytöstä, tietoyksikköä ei voi käyttää. Sillä ei ole merkitystä, onko taustataulujen ja -kenttien konfigurointiavaimet otettu käyttöön vai ei. |
| Käytössä                                 | Ei käytössä                           | Ei arvioitu                            | Ei arvioitu                          | Jos tietoyksikön konfigurointiavain on otettu käyttöön, tietojen hallintakehys tarkistaa kunkin taustataulun konfigurointiavaimen. Jos taulun konfigurointiavain on poistettu käytöstä, taulu ei ole toiminnallisessa käytössä tietoyksikössä. Jos taulun konfigurointiavain on poistettu käytöstä, taulun ja tietoyksikön konfigurointiavaimen asetuksia ei arvioida. Jos yksikön ensisijaisen taulun konfigurointiavain on poistettu käytöstä, järjestelmä toimii samoin kuin jos yksikön konfigurointiavain olisi poistettu käytöstä. |
| Käytössä                                 | Käytössä                            | Ei käytössä                                 | Ei arvioitu                          | Jos tietoyksikön konfigurointiavain on otettu käyttöön ja taustataulujen konfigurointiavaimet ovat käytössä, tietojen hallintakehys tarkistaa taulujen kenttien konfigurointiavaimen. Jos kentän konfigurointiavain on poistettu käytöstä, kenttä ei ole toiminnallisessa käytössä tietoyksikössä, vaikka vastaavan tietoyksikkökentän konfigurointiavain on otettu käyttöön. |
| Käytössä                                 | Käytössä                            | Käytössä                                  | Ei käytössä                               | Jos konfigurointiavain on otettu käyttöön kaikilla muilla tasoilla mutta yksikkökentän konfigurointiavain ei ole käytössä, kenttää ei voi käyttää tietoyksikössä. |

> [!NOTE]
> Jos yksikössä on sitten toinen yksikkö tietolähteenä, edellä mainittua semantiikkaa käytetään rekursiivisesti.

### <a name="entity-list-refresh"></a>Yksikköluettelon päivitys
Kun yksikköluettelo päivitetään, tietojen hallintakehys muodostaa konfigurointiavaimen metatiedot suorituksenaikaista käyttöä varten. Nämä metatiedot muodostetaan edellä kuvan logiikan mukaisesti. Kannattaa ehdottomasti odottaa yksikköluettelon päivittymistä ennen tietojen hallintakehysten töiden ja yksiköiden käyttämistä. Jos et odota, konfigurointiavaimen metatiedot eivät ehkä ole ajan tasalla, mikä voi aiheuttaa odottamattomia tuloksia. Kun yksikköluetteloa päivitetään, yksikköluettelosivulla on seuraava sanoma.

![Yksikköluettelon päivitys](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Tietoyksikköluettelon sivu
Yksiköiden konfigurointiavainasetukset näkyvät Tietojenhallinnan työtilan tietoyksikköluettelon sivulla. Voit aloittaa tältä sivulta sen selvittämisen, miten konfigurointiavaimet vaikuttavat tietoyksikköön.

Nämä tiedot voidaan näyttää yksikön päivityksen aikana muodostettujen metatietojen avulla. Konfigurointiavaimen sarakkeessa on tietoyksikköön liitetyn konfigurointiavaimen nimi. Jos sarake on tyhjä, tietoyksikköön ei ole liitetty konfigurointiavainta. Konfigurointiavaimen tilasarakkeessa näytetään konfigurointiavaimen tila. Jos siinä on valintamerkki, avain on otettu käyttöön Jos se on tyhjä, avain on joko poistettu käytetty tai yhtään avainta ei ole liitetty.

![Yksikköluettelon sivu](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Kohdekentät
Seuraavaksi poraudutaan tietoyksikköön tarkastelemaan, miten konfigurointiavaimet vaikuttavat tauluihin ja kenttiin. Tietoyksikön kohdekenttälomake sisältää konfigurointiavaimen ja tietoyksikön liittyviin tauluihin ja kenttiin liittyvät avaimen tilatiedot. Jos itse tietoyksikön konfigurointiavain on poistettu käytöstä, avautuva varoitussanoma ilmoittaa, että tämän yksikön kohdekenttälomakkeen taulut ja kentät eivät lainkaan käytettävissä riippumatta siitä, mikä niiden konfigurointiavaimen tila on.

![Kohdekentät](./media/Target_fields_1.png)

### <a name="child-entities"></a>Aliyksiköt 
Tietyissä yksiköissä on muita yksikköjä tietolähteinä tai ne ovat yhdistelmätietoyksiköitä: näiden yksiköiden konfigurointiavaimen tiedot näytetään aliyksiköiden lomakkeessa. Käytä tätä lomaketta samoin kuin edellä kuvattua yksikköluettelosivua. Aliyksikön kohdekenttälomake toimii myös edellä kuvatulla tavalla.

![Kohdekentät](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Tietoyksiköiden käyttäminen
Kun tiedät, miten konfigurointiavaimet mahdollisesti vaikuttavat tietoyksiköihin, joita haluat käyttää, voit nyt siirtyä käyttämään tietoyksiköitä lisäämällä tietoprojekteihin. 

### <a name="run-time-validations-for-configuration-keys"></a>Konfigurointiavainten suorituksenaikaiset oikeellisuustarkistukset
Suoritustenaikaiset oikeellisuustarkistukset suoritetaan seuraavissa käyttötilanteissa käyttämällä yksikköluetteloiden päivitysten aikana muodostettujen konfigurointiavainten metatietoja.

- Kun tietoyksikkö lisätään työhön
- Kun käyttäjä valitsee yksikköluettelossa oikeellisuustarkistuksen
- Kun käyttäjä lataa tietopaketin tietoprojektiin
- Kun käyttäjä lataa mallin tietoprojektiin
- Kun aiemmin luotu tietoprojekti on ladattu
- Kun malli ladataan tietoprojektiin
- Ennen vienti- tai tuontityön suorittamista (erä, muu kuin erä, toistuva, OData)
- Kun käyttäjä luo määrityksen
- Kun käyttäjä yhdistää kentät määrityskäyttöliittymässä
- Kun käyttäjä lisää vain tuotavat kentät

### <a name="managing-configuration-key-changes"></a>Konfigurointiavainten muutosten hallinta
Aina kun päivität konfigurointiavaimet yksikkö-, taulu- tai kenttätasolla, tietojen hallintakehyksen yksikköluettelo on päivitettävä. Tämä prosessi varmistaa, että kehys poimii kaikki uusimmat konfigurointiavainasetukset. Seuraava sanoma näkyy yksikköluettelosivulla siihen saakka, että yksikköluettelo päivitetään. Päivitetyt konfigurointiavainmuutokset tulevat voimaan heti, kun yksikköluettelo on päivitetty. Aiemmin luodut tietoprojektit ja työt kannattaa tarkistaa ja varmistaa, että ne toimivat odotetusti sen jälkeen, kun konfigurointiavainmuutokset on otettu käyttöön.

![Kohdekentät](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]